# Coffee Machine
นางสาวภัทชราพร บุปผาสิงห์ 683450059-3

classDiagram class Program { +static void Main(string[] args) } class CoffeeMachine { -int coffee -int water -int chocolate -int milk +CoffeeMachine(int coffee, int water, int chocolate, int milk) +void Buyblackcoffee(int amount) +void Buymocha(int amount) +void Buylatte(int amount) +void Buychocolate(int amount) +void ShowStock() +void IncreaseStock(int coffee, int water, int chocolate, int milk) } Program --> CoffeeMachine
