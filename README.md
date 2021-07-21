# mariar
import tellurium as te
r = te.loada ("""
ext S1, S3;
J1: S1 -> S2; k1*S1
J2: S2 -> S3; k2*S2

at (S2 > 10): S2 = 1

k1 = 0.1; k2 = 0.05; S1 = 10
""")
m = r.simulate(0, 100, 1000)
r.plot()
