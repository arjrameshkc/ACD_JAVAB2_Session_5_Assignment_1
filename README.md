# ACD_JAVAB2_Session_5_Assignment_1
package Session5_Assignment;

public  abstract class Figure {
	double dim1;

	public Figure(double dim1) {
		super();
		this.dim1 = dim1;
	}
	public abstract void findArea();
	public abstract void findPerimeter();
}

package Session5_Assignment;

public class Circle extends Figure {
          
	public Circle(double dim1) {
		super(dim1);
		// TODO Auto-generated constructor stub
	}

	@Override
	public void findArea() {
		// TODO Auto-generated method stub
	    double radius = dim1/2;
	    double area = 3.14*radius*radius;
	    System.out.println("Area of rectangle is:" +" "+area);
		
	}
		
	@Override
	public void findPerimeter() {
		// TODO Auto-generated method stub
		double radius = dim1/2;
		double perimeter = 2*3.14*radius;
		System.out.println("Perimeter of circle is:" +" "+perimeter);
	}

}

package Session5_Assignment;

public class Rectangle extends Figure{
	double length;
    double breadth;
    public Rectangle(double dim1,double length,double breadth) {
		super(dim1);
		this.breadth = breadth;
		this.length = length;		
	}

	@Override
	public void findArea() {
		// TODO Auto-generated method stub
		double area = length * breadth;
		System.out.println("Area of rectangle is:" +" "+area);
		
	}

	@Override
	public void findPerimeter() {
		// TODO Auto-generated method stub
		 double perimeter = 2 * (length + breadth);
		System.out.println("Perimeter of rectangle is:" +" "+perimeter);
	}

}

package Session5_Assignment;

public class Triangle extends Figure {
   double base,height;
	public Triangle(double dim1) {
		super(dim1);
		// TODO Auto-generated constructor stub
	}

	@Override
	public void findArea() {
		// TODO Auto-generated method stub
		double area = 0.5 * base * height;		
		System.out.println("Area of triangle  is:" +" "+area);
		
	}

	@Override
	public void findPerimeter() {
		// TODO Auto-generated method stub
		double hypotenuse = Math.pow(Math.pow(base, 2) 
				+ Math.pow(height, 2),0.5);
	  double perimeter = base + height + hypotenuse;
	  System.out.println("Area of triangle is:" +" "+perimeter);
		
		
	}

}

package Session5_Assignment;

import java.util.Scanner;

public class MainFigure {

	public static void main(String[] args) {
		// TODO Auto-generated method stub
		Scanner sc = new Scanner(System.in);		
		System.out.println("Enter diameterof circle:");
		double dim1 = sc.nextDouble();
		Circle figone = new Circle(dim1);
		figone.findArea();
		figone.findPerimeter();
		System.out.println("Enter length of rectangle:");
		double length = sc.nextDouble();
		System.out.println("Enter breadth of rectangle:");
		double breadth = sc.nextDouble();
		Rectangle figTwo = new Rectangle(dim1,length,breadth);
		figTwo.findArea();
		figTwo.findPerimeter();
		System.out.println("Enter base Triangle:");
		double base = sc.nextDouble();
		System.out.println("Enter height of triangle:");
		double height = sc.nextDouble();
		Rectangle figThree = new Rectangle(dim1,base,height);
		figThree.findArea();
		figThree.findPerimeter();
				
			

	}

}


