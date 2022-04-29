## SOLID PRINCIPLES
**Single Responsibility**
-  A class should only have one responsibility. This principle help us with this benefits:

    | Testing     | Fewer test cases |
    | ----------- | ----------- |
    | Lower coupling      | Fewer dependencies       |
    | Organization    | Easier to search        |
    
    For example this method which only serves to print.
    ```
    void printText(String Text){
      System.out.print(Text);
    }
    ```

**Open/Closed**
- Classes should be open for extension but closed for modification.
    
    For example if we have this class.
    ```
    public class Car {
      private float speed;
      private String brand;
      private String model;
    }
    ```
    And we want to add another one, we shouldn't modify the class to avoid errors and bugs, we will have to extend from it.
    ```
    public class Turbo extends Car {
      private boolean turbo;
    }
    ```
**Liskov Substitution**
- a

**Interface Segregation**
- a

**Dependency Inversion**
- a
