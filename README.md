# Coffee Machine
นางสาวภัทชราพร บุปผาสิงห์ 683450059-3
classDiagram
    %% ======== Classes ========
    class CoffeeMachine {
      -Resources resources
      -Menu menu
      -Transaction transaction
      +start()
      +selectCoffee()
      +processOrder()
    }

    class Menu {
      -List~Coffee~ coffeeList
      +getItems()
      +findCoffee(name)
    }

    class Coffee {
      -String name
      -int water
      -int milk
      -int coffee
      -float price
      +getCost()
      +requiredIngredients()
    }

    class Resources {
      -int water
      -int milk
      -int coffee
      -float money
      +checkAvailability(Coffee)
      +deduct(Coffee)
      +report()
    }

    class Transaction {
      -float moneyReceived
      +processCoins()
      +isSufficient(Coffee)
      +calculateChange()
    }

    %% ======== Relationships ========
    CoffeeMachine "1" *-- "1" Menu : has
    CoffeeMachine "1" *-- "1" Resources : has
    CoffeeMachine "1" *-- "1" Transaction : has
    Menu "1" o-- "*" Coffee : provides
