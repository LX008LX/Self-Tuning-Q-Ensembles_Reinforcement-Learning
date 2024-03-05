# Self-tuning Q-ensembles (STQE): Using Monte-Carlo Estimates for Adaptive Overestimation Bias Reduction
!! upload rwth jupyter organized plots
## Abstract
Deep Reinforcement Learning (DRL) shows state-of-the-art performance in challenging domains such as gameplay and robotic control (Haarnoja et al., 2019). However, the Q-function estimation method used in DRL intrinsically introduces bias. This phenomenon of overestimation bias is well known but persisting: it has been studied for the past 3 decades, and numerous research has shown the severe impact of overestimation, as it can lead to performance degradation or even divergence of reinforcement learning (RL) approaches. In this work, we address this issue by combining different recent developments in RL: we combine two effective algorithms: Aggressive Q-Learning with Ensembles (AQE) that utilizes Q-ensembles with Adaptively Calibrated Critic Estimates (ACC) that auto-tunes the quantile of chosen critics during the training, such that the resulting algorithm, Self-tuning Q-ensembles (STQE), is able to adjust the number of critics used to calculate the temporal difference (TD) target automatically throughout the training process.

## Introduction
The use of Q-ensembles in deep reinforcement learning (DRL) has been successful
despite its simplicity. A single Q-function computes the expected sum of future rewards
for a given state s and an action a, assuming that the current policy π is followed after
this step; whereas a Q-ensemble employs multiple networks, one for each Q-function output. Many state-of-the-art algorithms, renownedly Randomized Ensembled Double QLearning
(REDQ) and aggressive Q-Learning with Ensembles (AQE), both make use of
this streamlined yet powerful mechanism. In particular, AQE achieves the overall stateof-
the-art performance as of today, by averaging over the most pessimistic quantile of
critics in the Q-ensemble, leading to a more efficient ensemble usage.
However, the problem of overestimation still persists, as the optimal number of Qensembles
used when calculating the targets might change during training, while AQE
remains robust as it fixes the number of dropped Q-ensembles. In this paper, we
propose a novel algorithm, Self-tuning Q-ensembles (STQE), that further enhances the
performance of AQE in terms of bias reduction. We approach this goal by combing AQE
with Adaptively Calibrated Critic Estimates (ACC) - a new general algorithm that
performs bias correction with the aid of the most recent observed on-policy returns, such
that the quantile of critics chosen for target calculation can be adjusted automatically
and instantaneously throughout the training. The resulting STQE algorithm
demonstrates the feasibility of combining ACC with AQE by providing promising first
results as a proof of concept, further supported by theoretical results. Moreover, our
research further demonstrates the generality of ACC in bias reduction by applying it to
AQE.

## Background
Please access the rest of the research paper via the file "STQE Paper Final.pdf" in this repository. Happy to discuss any further details.
