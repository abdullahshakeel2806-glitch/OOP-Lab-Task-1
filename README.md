# OOP-Lab-Task-1

class Shape {

    void area() {
        System.out.println("Area of Shape");
    }

    // Method overloading: Square
    void area(int side) {
        System.out.println("Area of Square: " + (side * side));
    }

    // Method overloading: Rectangle
    void area(int length, int width) {
        System.out.println("Area of Rectangle: " + (length * width));
    }
}

class Rectangle extends Shape {

    // Method overriding
    @Override
    void area() {
        System.out.println("This is Rectangle Area");
    }
}

public class Main {
    public static void main(String[] args) {

        Shape s = new Shape();

        s.area();
        s.area(5);
        s.area(10, 5);

        Rectangle r = new Rectangle();
        r.area();
    }
}
