# Regression Testing
__regression testing, basic process of regression testing, defjavu, four different steps, basic metric: when is it better to use regression test or retest everything
Test case prioritization, why, what is the basic metric we use to figure out best prioritization, average percentage of faults elected__
1. Construct representation G for P
2. Associate test cases in T with entities in G
3. Build G' and compare G and G' to find dangerous entities
4. Select test cases based on dangerous entities

# Potential Test Case Prioritizations
- Total number of statements executed
- Additional number of statements covered
- Total number of branches covered
- Additional number of branches covered
- Total/Additional for any coverage metric
# Fault Exposing Potential
The fault-exposing potential (FEP) for a statement s in a program P is the probability that, when P is executed with a test, a fault at s will cause P to fail
