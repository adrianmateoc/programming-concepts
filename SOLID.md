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
- If class A is a subtype of class B, we should be able to replace B with A without disrupting the behavior of our program.
    
    For example if we have this interface.
    ```
    public interface Car {

    void turnOnEngine();
    void accelerate();
    }
    ```
    And we implement our interface
    ```
    public class MotorCar implements Car {

        private Engine engine;

        //Constructors, getters + setters

        public void turnOnEngine() {
            //turn on the engine!
            engine.on();
        }

        public void accelerate() {
            //move forward!
            engine.powerOn(1000);
        }
    }
    ```
    And now we want to use a car without engine as a electrical car, we are inherently changing the behavior of our program. Then we should rework our model into an       interface that take into account this engine-less state.

**Interface Segregation**
- a

**Dependency Inversion**
- a
