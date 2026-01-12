# Coffee Machine
นางสาวภัทชราพร บุปผาสิงห์ 683450059-3

classDiagram
    class CoffeeMachine {
        -int coffee
        -int water
        -int chocolate
        -int milk
        +CoffeeMachine(int coffee, int water, int chocolate, int milk)
        +Buyblackcoffee(int amount)
        +Buymocha(int amount)
        +Buylatte(int amount)
        +Buychocolate(int amount)
        +ShowStock()
        +IncreaseStock(int coffee, int water, int chocolate, int milk)
    }
    class Program {
        +Main(string[] args)
    }
    Program --> CoffeeMachine : creates
