Parameterized classes were added to Puppet in version 2.6.0. You may find some of their effects suprising.

Notice that the examples in this chapter all use resource-like declarations instead of the `include` function. Use of `include` conflicts with the idea that a class is completely defined by its declaration -- a single class with multiple definitions has ambiguous attributes. For that reason, we do not implement `include` in parameterized classes.

Parameterized classes make this problem more obvious, but it has always existed. A common pattern for passing information into a class is to retrieve an external variable with dynamically-scoped lookup. If a low-level class manages its own dependences through includes, it might have multiple scope chains resolving to different values. The include that takes effect first determines the behavior of the class. It is difficult to determine which includes are functional and which have been ignored.
