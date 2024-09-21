# ESGInvest
# ESG Company Recommender System Using Genetic Algorithm

This project implements a simple recommender system that selects companies based on their **Environmental, Social, and Governance (ESG)** scores using a **Genetic Algorithm (GA)**. The system works on a dataset of companies and their corresponding ESG ratings to suggest a subset of companies with optimized ESG risk scores.

## Project Overview

The recommender system is designed to maximize the selection of companies with low ESG risk, while considering multiple columns related to environmental, social, and governance factors. The key challenge is handling conflicting columns, such as Environment Risk Score, Governance Risk Score, and Social Risk Score, which may have different influences on the total ESG risk.

### Dataset

The dataset contains the following key columns:
- `Symbol`: Stock symbol of the company.
- `Name`: Full name of the company.
- `Total ESG Risk score`: A combined ESG risk score.
- `Environment Risk Score`: Environmental impact risk.
- `Governance Risk Score`: Governance-related risk.
- `Social Risk Score`: Social impact risk.
- `Controversy Score`: Risk related to company controversies.

This dataset also includes additional columns like sector, industry, number of employees, and company description, which could be utilized for more granular filtering.

### Approach

A **Genetic Algorithm (GA)** is used to evolve subsets of companies, optimizing for those with better ESG scores. Each individual in the GA population represents a potential subset of companies, and the fitness function is based on minimizing the **Normalized ESG Risk Score**.

The algorithm involves:
1. **Initial Population**: Random subsets of companies.
2. **Selection**: Choosing subsets based on their fitness scores.
3. **Crossover**: Combining two subsets to form new ones.
4. **Mutation**: Introducing variability by randomly replacing companies in a subset.

### Features
- **Genetic Algorithm** for optimizing the selection of companies based on ESG criteria.
- **Fitness function** based on normalized ESG scores.
- **Future-Proof** design to accommodate conflicting ESG scores from different factors (environment, governance, social).

## Future Scope

In future iterations of this project, I plan to incorporate a more advanced multi-objective optimization algorithm such as **NSGA-II** (Non-dominated Sorting Genetic Algorithm II). This will allow the system to handle conflicts between columns like **Environment Risk Score**, **Governance Risk Score**, and **Social Risk Score**, where minimizing one score might increase another.

The use of NSGA-II will provide a **Pareto optimal front**, offering multiple solutions where trade-offs between different ESG factors can be better managed.

## Tech Stack
- **Python**: Core programming language for the implementation.
- **pymoo**: A Python framework for multi-objective optimization algorithms, including GA and NSGA-II.
  
![pymoo](https://img.shields.io/badge/pymoo-v0.4.2-brightgreen)

## License
This project is licensed under the MIT License.

## Acknowledgments
- Inspiration for multi-objective optimization from the **pymoo** library.
- Special thanks to open-source libraries and the developer community for guidance and resources.
