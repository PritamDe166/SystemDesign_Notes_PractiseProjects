# Strategy Pattern Practice

This exercise deliberately contains two implementations:

## 01 - Without Strategy

The shipping calculator contains a growing `switch` statement. This version
shows the problem: adding a provider requires modifying the calculator.

## 02 - With Strategy and Dependency Injection

Each provider is an independent strategy behind `IShippingStrategy`. The
calculator depends on the abstraction, and the application composes the
concrete strategies through dependency injection.

The two versions should solve the same problem so the design difference is
easy to compare.


## 03 - Structure
Practise/
└── StrategyPatternPractice/
    ├── README.md
    ├── 01-WithoutStrategy/
    │   └── Models/
    │       └── Order.cs
    │   └── ShippingCostCalculator.cs
    └── 02-WithStrategyAndDI/
        ├── Models/
        │   └── Order.cs
        ├── Strategies/
        │   ├── IShippingStrategy.cs
        │   ├── FedExShippingStrategy.cs
        │   └── UpsShippingStrategy.cs
        ├── Services/
        │   └── ShippingCostCalculator.cs
        └── Program.cs
