private 变量

对于一些一定要用而且基本不改变的组件比如rigidbody 2D animatior 可以用private申明

然后一开始在start里面调用  public Rigidbody2D move;

改成private  Rigidbody2D move;

start里面就 move = getcomponent<rigidbody 2D>（）；

如果要可以看见 可以加上 [serializefield]在private前面