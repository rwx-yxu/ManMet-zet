# Design patterns
A design pattern is a general repeatable solution to a commonly
occurring problem in software design.

Following design patterns often ensures good practise are followed to
make code more maintainable and easier to read.

A design pattern is not a solution to a problem but rather a template
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
it won’t affect any code.

The logic for deciding the subclass stays within the superclass and not
the client code.

Use the factory method when you do not know before hand the exact type
and dependencies of the objects you code should work with.

