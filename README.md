# Java-for-Android-Coursera
Programming Assignments answer 
WEEK 1// GEOMETRY CALCULATIONS AUTO GRADED ....

Ans :
public static double rectangleArea(double length, double width)
    {
        return length*width;
    }
    public static double rectanglePerimeter(double length, double width)
    {
        return 2*(length+width);
    }
    public static double circleArea(double radius)
    {
        return Math.PI*Math.pow(radius,2);
    }
    public static double circleCircumference(double radius)
    {
        return 2*Math.PI*radius;
    }
    public static double rightTriangleArea(double base, double height)
    {
        return 0.5*base*height;
    }
    public static double rightTrianglePerimeter(double base, double height)
    {
        double perimeter=Math.sqrt(base*base+height*height);
        return perimeter+base+height;
    }
    public static double boxVolume(double length, double width, double depth)
    {
        return length*width*depth;
    }
    public static double boxSurfaceArea(double length, double width,
                                        double depth)
    {
        return 2*(length*width+width*depth+length*depth);
    }
    public static double sphereVolume(double radius)
    {
        return ( 4.0 / 3.0 ) * Math.PI * Math.pow( radius,3);
    }
    public static double sphereSurfaceArea(double radius)
    {
        return 4*Math.PI*radius*radius;
    }


}
