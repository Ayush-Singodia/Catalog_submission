# Catalog_submission

How the Solution Works
1. parseInput Function
The first step is to extract the data from the JSON input. This function does that job — it reads the x values directly from the keys and then decodes the y values based on the base that’s provided.

Inputs: The function takes in the JSON string.
Outputs: It returns an array of points in the form {x, y} and also k (though k doesn’t actually get used in the current version).


2. lagrangeInterpolation Function
This is the main mathematical part. Using the points, the function performs Lagrange interpolation to compute the constant term (i.e., the value of the polynomial when x = 0). It does this by calculating what’s called the Lagrange basis polynomial for each point and combining the results.

Inputs: An array of points {x, y}.
Outputs: The constant term, which is essentially the y-intercept.


3. findConstantTerm Function
This function ties everything together. It calls parseInput to get the points and then uses lagrangeInterpolation to find the constant term (the final result). It’s like the main "driver" of the program.



Inputs: A JSON string with points and encoded y values.
Outputs: The constant term, which is the result of the interpolation.
