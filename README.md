# design-patterns-Golang

1. [FactoryMethod](https://github.com/ishan16696/design-patterns-Golang/tree/main/factoryMethod)
   - Define an interface for creating an object, but let subclasses/Methods decide which class to instantiate. Defer the instantiation to subclasses/Methods.

       * Interface defination:
           ```go
               type Factory interface {
                   NewPerson() *person
                   NewAgent() *secretAgent
               }
           ```
       * Defer the instantiation to subclasses/Methods:
           ```go
               fact := factory.NewFactory(config)

               // with factory method, we can construct the instances of both person/agent.
               person := fact.NewPerson()
               agent := fact.NewAgent()
           ```