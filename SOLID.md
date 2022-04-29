## SOLID PRINCIPLES
**Single Responsibility**
-  A class should only have one responsibility. This principle help us with this benefits:

    | Testing     | Fewer test cases |
    | ----------- | ----------- |
    | Lower coupling      | Fewer dependencies       |
    | Organization    | Easier to search        |
    
    For example this method which only serves to print:
    ```
    void printText(String Text){
      System.out.print(Text);
    }
    ```

**Open/Closed**
- Classes should be open for extension but closed for modification.
    
    For example if we have this class:
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
    
    For example if we have this interface:
    ```
    public interface Car {

    void turnOnEngine();
    void accelerate();
    }
    ```
    And we implement our interface:
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
- Larger interfaces should be split into smaller ones. By doing so, we can ensure that implementing classes only need to be concerned about the methods that are of       interest to them.
    
    For example instead of doing this:
    ```
    public interface BearKeeper {
        void washTheBear();
        void feedTheBear();
        void petTheBear();
    }
    ```
    We should do this:
    ```
    public interface BearCleaner {
        void washTheBear();
    }

    public interface BearFeeder {
        void feedTheBear();
    }

    public interface BearPetter {
        void petTheBear();
    }
    ```
    Now, thanks to interface segregation, we're free to implement only the methods that matter to us.

**Dependency Inversion**
- It refers to the decoupling of software modules. This way, instead of high-level modules depending on low-level modules, both will depend on abstractions.

    For example if we have this code:
    ```
    public class Windows98Machine {

        private final StandardKeyboard keyboard;
        private final Monitor monitor;

        public Windows98Machine() {
            monitor = new Monitor();
            keyboard = new StandardKeyboard();
        }
    }
    ```
    By declaring the StandardKeyboard and Monitor with the new keyword, we've tightly coupled these three classes together. Thereby it's hard to test and we've lost       the ability to switch out our StandardKeyboard class with a different one.
    So if we do this:
    ```
    public interface Keyboard { }
    ```
    ```
    public class Windows98Machine{

        private final Keyboard keyboard;
        private final Monitor monitor;

        public Windows98Machine(Keyboard keyboard, Monitor monitor) {
            this.keyboard = keyboard;
            this.monitor = monitor;
        }
    }
    ```
    We're using dependence injection to facilitate adding the Keyboard dependency into the Windows98Machine class.
    Let's also modify our StandardKeyboard class to implement the Keyboard interface:
    ```
    public class StandardKeyboard implements Keyboard { }
    ```
    Now our classes are decoupled and communicate through the Keyboard abstraction.
    
