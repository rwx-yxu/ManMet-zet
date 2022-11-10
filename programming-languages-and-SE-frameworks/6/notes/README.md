# Design patterns
A design pattern is a general repeatable solution to a commonly
occurring problem in software design.

Following design patterns often ensures good practise are followed to
make code more maintainable and easier to read.

A design pattern is *not* a solution to a problem but rather a template
that can be used in many situations.

## Singleton pattern
A singleton is used when only one instance of a class can exist. Once
the instance is created, all subsequent requests return the same
object.

This can be seen as a globally accessible object that is read only. The
singleton must provide a global access point to get the instance of the
class.

A singleton is used for logging, drivers objects, caching and thread
pool.

Should be careful with multi threaded environments to ensure that
threads will not create the same object several times.

Singletons must be kept atomic. It is bad design if singletons become
too large and take too many responsibilities.

## Factory method
A factory method is used when there is logic required to decide which
subclass an instance should be.

Since the factory method returns a new instance, we do not instantiate
instances directly.

Factory method avoids tight coupling. We would rename the subclasses and
it won't affect any code.

The logic for deciding the subclass stays within the superclass and not
the client code.

Use the factory method when you do not know before hand the exact type
and dependencies of the objects you code should work with.

Use factory method when you want to provide users of your library a way
to extend its internal components.

Use factory method when you want to reuse existing objects instead of
rebuilding them each time.

Code may be more complicated since we create a lot of new subclasses to
implement.

## Adaptor pattern
Used to convert one interface into another interface.

Adaptor pattern allows for classes to interact with each other that
normally wouldn't if they are from different libraries for instance.

Use the adapter class when you want to use some existing class but its
interface isn't compatible with the rest of your code.

Use when you want to reuse several existing subclasses that lack some
common functionality that can't be added to the superclass.

## Decorator
Used to enhance functionality with extra behaviour.

The decorator has the same base type as the original class.

Holds a wrapped instance to delegate to the original functionality.

Use when you need to be able to assign extra behaviours to objects at
runtime without breaking the code that uses these objects.

Use when it's not possible to extend an objects behaviour using
inheritance.

It's hard to remove a specific wrapper from a wrappers stack.

Hard to implement a decorator that its behaviour doesn't depend on the
order in the decorators stack.

Initial boiler plate may be difficult to read.
