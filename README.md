// Main class to demonstrate the cascading method calls
public class CascadingExample {

    public static void main(String[] args) {
        // Create a Person object and configure it using method chaining
        Person person1 = new Person()
            .setName("Alice")
            .setAge(30)
            .display(); // The display() method is also part of the chain

        System.out.println("\n--- Another Person ---");

        // A second example showing the fluent interface on a new object
        new Person()
            .setName("Bob")
            .setAge(25)
            .display();
} 
}
class Person {
    private String name;
    private int age;

    /**
     * Sets the name of the person.
     * @return The current Person object to allow for method chaining.
     */
    public Person setName(String name) {
        System.out.println("Setting name to: " + name);
        this.name = name;
        return this; // Returns the instance to enable chaining
    }

    /**
     * Sets the age of the person.
     * @return The current Person object to allow for method chaining.
     */
    public Person setAge(int age) {
        System.out.println("Setting age to: " + age);
        this.age = age;
        return this; // Returns the instance to enable chaining
    }

    /**
     * Displays the person's details to the console.
     * @return The current Person object to allow for further chaining.
     */
    public Person display() {
        System.out.println("Person Details -> Name: " + this.name + ", Age: " + this.age);
        return this;
    }
}

