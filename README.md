# Cr-a-D-co-Conception-d-Int-rieur-G-n-r-e-par-IA
Créa-Déco utilise l'IA générative et la diffusion stable pour créer des designs d'intérieur personnalisés en fonction des goûts et du budget des utilisateurs, révolutionnant la décoration d'intérieur.
import random

# Simulated Database of Design Styles
design_styles = ['Modern', 'Minimalist', 'Industrial', 'Scandinavian', 'Traditional', 'Rustic']

# Budget Categories
budget_categories = {
    'Low': 'up to $1,000',
    'Medium': '$1,000 to $5,000',
    'High': 'over $5,000'
}

# Example Items for Each Style
design_elements = {
    'Modern': ['sleek sofa', 'abstract art pieces', 'glass coffee table'],
    'Minimalist': ['functional furniture', 'neutral color palette', 'minimal decor items'],
    'Industrial': ['exposed brick walls', 'metal light fixtures', 'wood and metal furniture'],
    'Scandinavian': ['light woods', 'soft textiles', 'plants'],
    'Traditional': ['classic furniture', 'elegant decor items', 'rich color schemes'],
    'Rustic': ['reclaimed wood furniture', 'stone fireplace', 'natural textures']
}

def generate_design_preference():
    """Simulate a user input for design preferences."""
    print("Welcome to Créa-Déco!")
    style = input(f"Choose your design style ({', '.join(design_styles)}): ")
    budget = input(f"Choose your budget (Low, Medium, High): ")
    return style, budget

def generate_design(style, budget):
    """Generate a personalized interior design based on the user's preferences."""
    elements = design_elements.get(style, ['generic design elements'])
    budget_range = budget_categories.get(budget, 'No budget selected')
    
    print("\nBased on your preferences, here is your personalized interior design concept:")
    print(f"Style: {style}")
    print(f"Budget: {budget_range}")
    print("Design Elements Suggested:")
    for element in elements:
        print(f"- {element}")

def main():
    style, budget = generate_design_preference()
    if style in design_styles and budget in budget_categories:
        generate_design(style, budget)
    else:
        print("Sorry, it seems there was an error with the inputs. Please try again.")

if __name__ == "__main__":
    main()
