To evaluate the impact of varying hyperparameter configurations and the choice of different
convex regularizers in both stochastic and deterministic settings of Approximate policy mirror descent(APMD) introduced by Guanghui Lan [2022], we have designed a
controlled numerical experiment implemented in Python using the Pytorch library. The
primary objective is to evaluate and compare the performance of these setups against the
optimal policy and optimal value obtained through policy iteration (Puterman [1994], 6.4)
in an unregularized setting. The aim of considering an unregularized optimal value function
and policy is to assess how regularized and potentially biased frameworks perform
compared to the actual problem setup.
This experiment has been conducted in both exact and stochastic frameworks. The experiment
utilizes the Approximate Policy Mirror Descent algorithm, as detailed in (4.1.5).
APMD is employed with different convex functions and hyperparameter settings to explore
their effects on learning dynamics and overall performance. Also, entropy-regularized
PMD as an instance of APMD has been implemented.
To measure and compare the performance of considered settings, we have used four
different metrics. The first performance metric is the expected cumulative cost gap, which
assesses the long-term efficiency and effectiveness of each policy under the optimal steadystate
distribution. The second metric uses the KL-divergence to measure how quickly and
reliably each setup approaches the optimal policy during the iterative optimization process.
The third metric is expected entropy, which quantifies the entropy of each obtained
policy, allowing us to compare the relative degree of exploration across setups. The final
metric evaluates the distribution mismatch between steady-state distribution of optimal
policy and returned policies, as described in (3.4), offering insights into how closely these
two distributions over state space align.

For more information refer to the uploaded pdf file "Mirror Descent Methods in
Reinforcement Learning", for information regarding the experimental setup, see chapter 6.
