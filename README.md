# H.Polymorphism_Composition-W13D2

## Polymorphism


1. What does the word 'polymorphism' mean?
A. It means that something has or occurs in different/many forms

2. What does it mean when we apply polymorphism to OO design? Give a simple Java example.
A. It means we have classes that belong to more than one type.

```
public abstract class Animal{
}
```

```
public Interface IMammal{
}
```

```
public class Pig extends Animal implements IMammal{
}
```

In the above code Pig is both an Animal type and an IMammal type.



3. What can we use to implement polymorphism in Java?
A. We can use both inheritance and interfaces.

4. How many 'forms' can an object take when using polymorphism?
A. An object may have as many forms as the programer wants.

5. Give an example of when you could use polymorphism.
A. Imagine we have multiple electronic devices that can connect to a computer via a USB3.0 and we wanted to have an ArrayList inside computer class that holds a list of all the devices. Each device will be it's own class with it's own attributes and methods. Therefore we could not add them all into the ArrayList. If we were to introduce an interface in which all eletronic devices could be a part of (since they all use electricity), then we could create our ArrayList of  "devicesThatUseElectricity" in which all the different electronic devices could be added.

## Composition and Aggregation

6. What do we mean by 'composition' in reference to object-oriented programming?
A. Composition in java OOP means it has a "has-a" relationship to another object. This is achieved when a class or object contains another object in which the enclosed object cannot exist without the existance of the primary object (Like a Human object with a Heart and Lung Object attribute - without the  the Heart and Lung objects, the Human object would not exist).

7. When would you use composition? Provide a simple example in Java.

```
public abstract class Human{

  private Lung lung;
  private Heart heart;
}
```

```
public class Lung{
}
```

```
public class Heart{
}
```

In the code above, both Heart and Lung are classes and may exist by themsleves. However, a Human object requires a Heart and Lung object to exist.


8. Give a difference between composition and aggregation?
A. Composition relation is when the an object requires another object to exist/function while aggregation relation means that it could have a particular object to function but, it can also not have it and still function/exist. For example:

A Car class requires an Engine and Wheels class to function. This is a composition. The same car can function however without a MusicPlayer class. This means that the Car and Engine/Wheels have a composition relation while the Car and MusicPlayer have an aggregate relation. In this example the Car can exist/function without the MusicPlayer.

9. What is/are the advantage(s) of using composition/aggregation?
A. It can make objects have a particular method or attribute that does not need to be shared with other objects. In the instance of inheritance, there is always going to be one main superclass, so any objects inheriting from that superclass will have all the attributes and methods of their parent class. This means that some objects can have unused code, or code that does not specifically relate to that object. With composition/aggregation we can make sure that we maintain our code DRY and achieve polymorphism.

10. When using composition, when an object is destroyed, what happens to all the objects it is composed of?
A. The objects are also destroyed.

11. When using aggregation, when an object is destroyed, what happens to all the objects it is composed of?
A. Can still function on their own.
