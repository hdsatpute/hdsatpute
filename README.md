import math

# Given data
E = 210000  # Modulus of elasticity in kg/cm^2
h = 15  # Thickness of the slab in cm
mu = 0.13  # Poisson’s ratio

# Modulus of subgrade reaction for two cases
K_values = [3.0, 7.5]  # in kg/cm^3

# Formula to compute radius of relative stiffness
def compute_radius_of_stiffness(E, h, mu, K):
    l = ((E * h**3) / (12 * (1 - mu**2) * K))**0.25
    return l

# Compute for both values of K
radii = [compute_radius_of_stiffness(E, h, mu, K) for K in K_values]

# Display the results
for i, K in enumerate(K_values):
    print(f"Radius of relative stiffness for K = {K} kg/cm^3: {radii[i]:.2f} cm")

<!---
hdsatpute/hdsatpute is a ✨ special ✨ repository because its `README.md` (this file) appears on your GitHub profile.
You can click the Preview link to take a look at your changes.
--->
