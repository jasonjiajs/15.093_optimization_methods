# Is Just-in-Time really the most profitable supply chain strategy for Nike in an uncertain world?

Final Project, MIT 15.093 - Optimization Methods <br>
Team Members: [Jason Jia](https://www.linkedin.com/in/jasonjiajs/), [Virginia Maguire](https://www.linkedin.com/in/virginia-maguire/)

<img src="https://github.com/jasonjiajs/just-in-time-nike/assets/90637415/a14c461a-9610-4110-bf76-25fbedee8895" width="550" />

## Summary
Even with a blunt robust strategy, it can be more profitable for firms to maintain healthier inventory levels and source from more diverse suppliers. While costly to guard against supply chain uncertainty, the benefits come through during disruptions such as Covid-19, which should not be dismissed as a one-off event. If businesses such as Nike are still adopting a Just-in-Time model, they should take immediate action to transition towards a more resilient, “Just-in-Case” strategy.

## Problem and Motivation
The Just-in-Time (JIT) system is a well-known lean manufacturing system pioneered by Toyota that seeks to eliminate waste, which often implied minimizing inventory levels and finding the lowest cost suppliers. While many businesses have pursued JIT as their supply chain strategy, low inventory levels and supplier concentration caused severe shortages when factories and transportation routes were shut down during Covid-19. As seen from a spike in supply chain resilience articles from McKinsey, Bain and BCG during 2021-2023, the missed sales opportunity and reputational damage from unmet demand has generated strong business interest to re-evaluate if JIT is truly the best supply chain strategy.

<p float="left">
  <img src="https://github.com/jasonjiajs/just-in-time-nike/assets/90637415/683a1987-ded7-44be-9673-80ed619f78b8" width="500" />
  <img src="https://github.com/jasonjiajs/just-in-time-nike/assets/90637415/9330242a-baad-4c6f-9b37-fd90b7f2855d" width="500" /> 
  <img src="https://github.com/jasonjiajs/just-in-time-nike/assets/90637415/bd11641c-d8f4-4822-85d8-66838ada9e61" width="380" />
</p>

However, to the best of our knowledge, there is no publicly available research quantifying the potential profitability improvements under different conditions. This is why we want to explore to what extent do disruptions in supply (modelled by ε) and penalties for unmet demand (modelled by α) affect differentially robust supply chain strategies for Nike (modelled by δ), in terms of profit, inventory levels and concentration of suppliers.

## Data

We use 3 main data sources for this project: Nike Factory Worker Data, Nike 10-K Reports, Drewry World Container Index (for shipping costs).

<img width="1200" alt="image" src="https://github.com/jasonjiajs/just-in-time-nike/assets/90637415/d748b638-2feb-4e02-acab-f5708eec553b">

## Methods

### Decision Variables
<img width="922" alt="image" src="https://github.com/jasonjiajs/just-in-time-nike/assets/90637415/e9536bc8-541f-4cc3-95d5-199ba32114b4">

### Notation
<img width="922" alt="image" src="https://github.com/jasonjiajs/just-in-time-nike/assets/90637415/8dfd91c6-61da-4ca4-8d0e-6060b536575a">

<img width="922" alt="image" src="https://github.com/jasonjiajs/just-in-time-nike/assets/90637415/c56df364-ce35-4c24-a1db-0b2532cfe290">

<img width="922" alt="image" src="https://github.com/jasonjiajs/just-in-time-nike/assets/90637415/a38de80e-02e5-4680-a0e2-b384abe165c0">

## Model

### Starting formulation

<img width="922" alt="image" src="https://github.com/jasonjiajs/just-in-time-nike/assets/90637415/e22d36c9-55a7-4fe5-b2f3-8c08671c32cb">

### Robustness: Incorporating Uncertainty in Availability

<img width="922" alt="image" src="https://github.com/jasonjiajs/just-in-time-nike/assets/90637415/a1aeb0ef-ef16-4838-bc8b-17e0fe90cf5a">

### Evaluation of various strategies under different settings

<img width="922" alt="image" src="https://github.com/jasonjiajs/just-in-time-nike/assets/90637415/1496210a-b88f-4d97-b821-e7f6e03a7e5d">

## Key Findings
1. With greater unexpected supply chain disruptions, a somewhat robust strategy almost always performs better than a non-robust strategy. As ε increases, the percentage profit improvement of a δ-robust strategy compared to a non-robust strategy (δ = 0) tends to be increasingly positive.

<img width="922" alt="image" src="./output/profit_improvement.png">

2. In line with expectations, inventory levels right before Covid-19 rise as Nike’s supply chain strategy becomes more robust, up to a point.

<img width="922" alt="image" src="./output/inventory_2020.png">

3. Also in line with expectations, regional Herfindahls right before Covid-19 decrease as Nike’s supply chain strategy becomes more robust, up to a point. This points to regionalization, a strategy to pursue greater supplier diversification at a regional level.

<img width="922" alt="image" src="./output/herfindahl_2020.png">

## Impact and Conclusion
Our model showed that even with a blunt robust strategy, it can be more profitable to maintain healthier inventory levels and source from more diverse suppliers. In practice, this could involve actions such as dual sourcing of raw materials, increasing inventory of critical products, near-shoring and increasing supplier base, as well as regionalization.
While costly to guard against supply chain uncertainty, the benefits come through during disruptions such as Covid-19, which should not be dismissed as a one-off event. If businesses such as Nike are still adopting a Just-in-Time model, they should take immediate action to transition towards a more resilient, “Just-in-Case” strategy.
