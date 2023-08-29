# Finally movement

+ ==细节还需自己消化，但是这个写法我认为可以背板==

```c#
public class Playcontroller : MonoBehaviour
{
    private Rigidbody2D rb;
    private Collider2D coll;
    private Animator anim;
    public float speed, jumpForce;
    public Transform groundCheck;
    public LayerMask ground;
    public bool isGround, isJump;//控制动画效果
    bool jumpPressed;
    int jumpCount;
    void Start()
    {
        rb = GetComponent<Rigidbody2D>();
        coll = GetComponent<Collider2D>();
        anim = GetComponent<Animator>();
    }

    void Update()
    {
       if(Input.GetButtonDown("Jump") && jumpCount > 0)
        {
            jumpPressed = true;
        }
    }

    private void FixedUpdate()
    {
        isGround = Physics2D.OverlapCircle(groundCheck.position, 0.1f, ground);

        GroundMovement();

        Jump();

        SwitchAnim();
    }
    void GroundMovement()
    {
        float horizontalMove = Input.GetAxisRaw("Horizontal");
        rb.velocity = new Vector2(horizontalMove * speed, rb.velocity.y);
        
        if(horizontalMove!=0)
        {
            transform.localScale = new Vector3(horizontalMove, 1, 1);
        }
    }

    void Jump()
    {
        if(isGround)
        {
            jumpCount = 2;
            isJump = false;
        }
        if(jumpPressed && isGround)
        {
            isJump = true;
            rb.velocity = new Vector2(rb.velocity.x, jumpForce);
            jumpCount--;
            jumpPressed = false;
        }
        else if(jumpPressed &&jumpCount > 0 && isJump)
        {
            rb.velocity = new Vector2(rb.velocity.x, jumpForce);
            jumpCount--;
            jumpPressed = false;
        }
    }

    void SwitchAnim()
    {
        anim.SetFloat("running", Mathf.Abs(rb.velocity.x));

        if(isGround)
        {
            anim.SetBool("falling", false);
        }
        else if(!isGround && rb.velocity.y > 0)
        {
            anim.SetBool("jumping", true);
        }    
        else if(rb.velocity.y<0)
        {
            anim.SetBool("falling", true);
            anim.SetBool("jumping", false);
        }
    }
}
```