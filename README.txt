THE PLATE COST COUNTER — free giveaway from "Build It With AI" (Episode 27)

What it is
----------
One HTML page that prices every dish on your menu from the packs you actually buy.
Paste three CSV exports — ingredients, recipes, sales — type your target food-cost
percent, and click "Price the menu". It converts units inside their own family,
divides by yield (trim and cook loss), flags dishes over your target, weighs the
result by what actually sold, and — where a number cannot be trusted — refuses,
with the row and the reason, instead of guessing. If its own audit fails, it
prints DO NOT TRUST THESE PLATE COSTS across the top.

How to use it
-------------
1. Open index.html in any browser (double-click it). Nothing is uploaded anywhere;
   it runs entirely on your machine.
2. Click "Load the sample menu" to see it working on the fictional Harrow & Vine
   restaurant, or paste your own three files:
   - ingredients: ingredient, pack size, pack unit, pack price, yield %
   - recipes:     dish, menu price, ingredient, qty, unit
   - sales:       dish, sold
3. Units it accepts: g, kg, oz, lb · ml, l, tsp, tbsp, fl oz, cup, qt, gal · each, dozen.
   A recipe line in a different unit family from how the ingredient is bought gets
   refused (no density table — a cup of something bought by the pound would be a guess).

In the bundle (Plate_Cost_Counter_BUNDLE.zip)
---------------------------------------------
- index.html            the tool (same file as the live page)
- sample_ingredients.csv, sample_recipes.csv, sample_sales.csv
- checker.py            independent Python checker, written from the rules alone —
                        run: python3 checker.py sample_ingredients.csv sample_recipes.csv sample_sales.csv 30
- v1_wrong_build.html   the first build from the episode — WRONG, kept as a museum piece
- v2_wrong_build.html   the second build — closer, still wrong three ways; also a museum piece
- PROMPTS.txt           the three prompts, word for word, in the order they were sent

Honest limits
-------------
It reads your exports, not your POS. It holds no density table. Labor, packaging
and overhead are not in these numbers — packs, plates, yields and sold counts are.
Sample data is fictional. Not accounting advice.
