package areacalculation;

abstract class shape{
    public abstract double calculatearea();
}
class circle extends shape{
    private double radius;
    public circle(double radius){
        this.radius=radius;
    }
    @Override
    public double calculatearea(){
        return Math.PI*radius*radius;
    }
}
class rectangle extends shape{
    private double length,width;
    public rectangle(double length,double width){
       this.length=length;
       this.width=width;
    }
    @Override
    public double calculatearea(){
        return length*width;
    }
}
class square extends shape{
    private double side;
    public square(double side){
        this.side=side;
    }
    @Override
    public double calculatearea(){
        return side*side;
    }
 }
class triangle extends shape{
    private double base,height;
    public triangle(double base,double height){
        this.base=base;
        this.height=height;
    }
    @Override
    public double calculatearea(){
        return 0.5*base*height;
    }
}
public class shapeinheritanceexample {    
    public static void main(String[] args) {
       shape circle=new circle(7);
       shape rectangle=new rectangle(4,5);
       shape square=new square(3);
       shape triangle=new triangle(1,2);
       System.out.println("Circle area:"+circle.calculatearea());
       System.out.println("recatngle area:"+rectangle.calculatearea());
       System.out.println("square area:"+square.calculatearea());
       System.out.println("triangle area:"+triangle.calculatearea());
    }
    
}

output
Circle area:153.93804002589985
recatngle area:20.0
square area:9.0
triangle area:1.0
