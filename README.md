# nutritional-shake-optimizer
This project formulates a linear programming model using Pyomo to optimize the ingredient mix for a nutritionally complete strawberry shake while minimizing cost. The model ensures that all caloric, fat, vitamin, taste, and thickness constraints are satisfied.

## Key Constraints
- **Calories**: 380-420 kcal
- **Fat calories**: ≤20% of total
- **Vitamins**: ≥50 mg
- **Taste**: ≥2 tbsp Strawberry per tbsp Sweetener
- **Thickness**: Exactly 15 mg thickeners

## Ingredients & Costs
| Ingredient           | Variable | Cost ($/tbsp) |
|----------------------|----------|---------------|
| Strawberry Flavoring | S        | 10            |
| Cream                | C        | 8             |
| Vitamin Supplement   | V        | 25            |
| Artificial Sweetener | A        | 15            |
| Thickening Agent     | T        | 6             |

## Mathematical Formulation
**Objective**:  
Minimize Cost = `10S + 8C + 25V + 15A + 6T`

**Constraints**:
1. Calories: `380 ≤ 50S + 100C + 120A + 80T ≤ 420`
2. Fat: `10(S + 75C + 30T) ≤ 2(50S + 100C + 120A + 80T)`
3. Vitamins: `20S + 50V + 2T ≥ 50`
4. Taste: `S ≥ 2A`
5. Thickness: `3S + 8C + V + 2A + 25T = 15`

## Results

After running the model, the optimal ingredient quantities and the minimized cost will be displayed in the output.

## License

This project is open-source and available for modification and use under an MIT license.

## Contributors

If you have any suggestions or improvements, feel free to contribute! 🚀


