## Routes 
- GET `/recipes` - Récupérer toutees les recettes
- GET `/recipes/:recipeId` - Récupérer une recette
- POST `/cuisines/add` - Ajouter une cuisine
    - Body : `{name: String}`
- POST `recipes/add` - Ajouter une recette 
    - Body : `{ "recipe_name": "Riz cantonais", "recipe_description": "Riz cantonais rapide en 10mn", "image_url": "/riz-cantonais.jpg", "cuisine_id": 6, "goal_name": "Weight Loss", "dietary_info_names": [], "allergies_info_names": [], "ingredients_data": [ { "ingredient_id": 11, "quantity": 1 } ], "instructions": [ { "step_number": 1, "StepInstruction": "Faire bouillir l'eau" }, { "step_number": 2, "StepInstruction": "Emincer l'oignon" }, { "step_number": 3, "StepInstruction": "Mélanger et servir chaud" } ] }`

- POST `/recipes/:recideId/add/ingredients` - Ajouter un ingrédient à la recette
    - Body : `{ "name": "Rice", "quantity": 300, "unit": "grams" }`

- PUT `/recipes/:recipeId/instructions/:stepNumber/update` - Modifier une       instruction d'une recette
    - Body : `{ "StepInstruction": "Faire bouillir l'eau" }`

- DELETE `recipes/:recipeId/ingredients/:ingredientId/delete` - Supprimer un ingrédient d'une recette

- DELETE `/recipes/:recipeId/instructions/:instructionId/delete` - Supprimer une instruction d'une recette

- DELETE `/cuisines/:cuisineId/delete` - Supprimer une cuisine

- DELETE `/recipes/:recipeId/delete` - Supprimer une recette

- PUT `recipes/:recipeId/update` - Modifier une recette
    - Body : `{"recipe_id": 10, "recipe_name" : "Tolma",
    "recipe_description": "Une nouvelle description", "goal_id": 2
    }`
