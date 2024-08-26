# reduced_form_credit

A reduced form model for credit risk in fixed income focuses on modeling the probability of default and credit spreads without explicitly modeling the firm's asset value. Instead of determining default based on a company’s asset value (as in structural models), reduced form models treat default as a random event governed by an exogenously specified intensity or hazard rate.

Hazard Rate (Default Intensity):
The hazard rate or default intensity represents the instantaneous risk of default at a given time. It can be time-dependent or influenced by external factors (covariates). A common form is:
lambda(t) = a + b * X(t)
Where:
lambda(t) is the hazard rate at time t.
a is a base hazard rate (constant part).
b is the sensitivity of the hazard rate to the covariate X(t).
X(t) is an external factor or covariate that affects the hazard rate.

Survival Probability:
The survival probability is the probability that the firm has not defaulted by time T. It is given by:
P(T) = exp(-∫_0^T lambda(t) dt)
For a constant hazard rate lambda, the survival probability simplifies to:
P(T) = exp(-lambda * T)
Where:
P(T) is the survival probability by time T.
lambda is the constant hazard rate.
T is the time horizon.

Default Probability:
The default probability over a period T is simply 1 - P(T), where P(T) is the survival probability:
Default Probability = 1 - P(T) = 1 - exp(-lambda * T)

Credit Spread:
The credit spread is the additional yield over the risk-free rate that compensates investors for the risk of default. It can be estimated as:
Credit Spread = (1 - Recovery Rate) * lambda
Where:
lambda is the hazard rate.
Recovery Rate is the proportion of the bond's value that is expected to be recovered in the event of default.



Hazard Rate (Default Intensity):
lambda(t) = a + b * X(t)

Survival Probability:
P(T) = exp(-lambda * T)

Default Probability:
Default Probability = 1 - exp(-lambda * T)

Credit Spread:
Credit Spread = (1 - Recovery Rate) * lambda

In reduced form models, the default event is modeled as occurring at a random time, governed by the hazard rate (lambda). The survival probability is the chance that the firm does not default up to a certain time, while the default probability is the complementary probability that the firm defaults. The credit spread is a direct function of the hazard rate and reflects the risk premium required by investors to compensate for the risk of default.
