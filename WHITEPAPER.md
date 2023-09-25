## Abstract

## Introduction
# 2.1 Decentralized Autonomous Organizations (DAOs)
# 2.2 Challenges of Decentralized Governance
# 2.3 Sawt's Approach to Decentralized Governance

## Ways of Negotiating
# 3.1 Top-Down Approach
# 3.2 Bottom-Up Approach
# 3.3 Flexible Top-Bottom Approach

## The Median Mechanism as a Voting Rule for DAOs
# 4.1 The Geometric Median in Bargaining Theory

## Strategic Properties of the Median Mechanism
# 5.1 Existence
# 5.2 Uniqueness
# 5.3 Robustness
# 5.4 Truthfulness

## Set-up
# 6.1 Private Values of Participants
# 6.2 Mechanism Mapping

In the pursuit of the wisdom the crowd, the game theoretical properties of Median Voting Rule applied to DAO governance
                                Sawt @ ETH-GLOBAL, NEW YORK September 23, 2023
Abstract
As DAOs grow, communication ways reveal inefficiencies, necessitating innovative solutions. The study highlights the median mechanism as a voting rule that minimizes discontent within a group, satisfying desirable properties like robustness to outliers and truthfulness. The practical applications of these theoretical concepts can be used in use cases in price discovery mechanisms for grant allocations, treasury management, counter-proposal mechanisms and more.
Introduction
Decentralized Autonomous Organizations (DAOs) represent a novel form of internet-native communities based on cooperation. Vitalik Buterin defined DAOs as “a virtual entity that has a certain set of members or sharehold- ers which, perhaps with a 67% majority, have the right to spend the entity’s funds and modify its code.” Decentralized governance reveals to be limited by the complexity of decision making when the number of participants increases, especially when dealing with complex problems that require certain areas of expertise.
One of the key principles underlying DAOs is ensuring no single point of failure, achieved through decentralization that enhances resilience across social (governance) and technical (code) layers. While this increases security, it also leads to slow decision-making and high technical costs, limiting efficiency [2]. Sawt aims to introduce a negotiation tool for decentralized governance designed for business efficiency. Built around a voting mechanism leveraging the wisdom of the crowd, we seek to empower the decentralized market.Ways of negotiating
We have identified 3 ways of negotiating a price with a group. We partition them by top down, bottom up or a mixture of both.
• Top-down approach: One participant proposes its preference, the rest vote yes or no.
• Bottom up approach: Every participant of the group proposes it’s prefer- ence in a simultaneous or sequential way, and then a voting rule aggregates all preferences to come up with a value.
• Flexible Top-Bottom approach: Every participant of the group delegate his preference in a simultaneous way. Each participant then proposes it’s preference in a simultaneous or sequential way. A voting rule aggregates all preferences to come up with a value.
Often, DAO contributors have raised their voices about the feeling of not being represented by one proposal maker. Hence, sometimes the top-down ap- proach is not ideal. See the communities contention around the price discovery in the FEI and RARI merger [3]. Relying on current top-down voting mechanisms (yes/no) reveal to be undemocratic, going against the ethos of decentralization. A lot of issues are being discussed today behind closed doors in a centralized way. We will highlight in a first part the median mechanism as a collabora- tive way to reach agreement on numerical and categorical parameters and then discuss the complexity of decision making in a second part.
The median mechanism as a voting rule for DAOs
In bargaining theory and voting, The geometric median, the solution of the Weber problem, can be seen as an optimal outcome and represents a compromise that minimizes overall discontent.
Voters choose points in a space, symbolizing their preferred outcomes. The Geometric Median of these points minimizes the sum of the distances to all chosen points, yielding a compromise that reflects the least collective discontent.
It assures a minimum satisfaction in the group of 50%. The property of the geometric median that it minimizes the sum of the distances to all chosen points is its defining characteristic.
Add Proof.
Strategic Properties of the Median Mechanism
1. Existence: For any finite set of points in a Euclidean space, a Geometric Median exists.
Proof:Add Proof
2. Uniqueness: The Geometric Median is unique whenever the points are not collinear.
Proof: Add Proof
3. Robustness: The geometric median has a breakdown point of 0.5 (or up to quorum). That is, up to half of the sample data may be arbitrarily cor- rupted, and the median of the samples will still provide a robust estimator for the location of the uncorrupted data. Proof: Add Proof
4. Truthfulness: Demonstrating that the Nash equilibrium of the median mechanism is reached when participants truthfully report their individual values involves illustrating that no player can improve their outcome by deviating from truth-telling, given that all other players are also reporting truthfully. Here’s a step-by-step breakdown: Proof: Add Proof
Set-up
Each participant i has a private value vi drawn from an interval I of real numbers. The mechanism M maps from In (the set of all possible private value profiles) to I. In the median mechanism, M(v1, v2, . . . , vn) is the median of the values v1,v2,...,vn.
Consider that all participants can report values di↵erent than vi (let’s call i t v i0 ) .
• If vi < M(v) and vi0 > vi, the outcome stays the same or increases.
– Base Case: n = 3, In a 3-player game with ascending values (v1 v2 v3)andmedianv2,ifaplayerwithavaluev1 <v2 increases their reported value to v10 , the median stays v2 as long as v10 v2. If v10 > v2, the median might increase, which does not benefit the player who wanted a lower median.
– Inductive Hypothesis: In a n-player game with ascending values (v1 v2 ... vn) and median vdn/2e, if a player i with a value vi < vdn/2e increases their reported value to vi0, the median stays vdn/2e as long as vi0 vdn/2e. If vi0 > vdn/2e, the median might increase, which does not benefit the player who wanted a lower median.
– Inductive Step: We now need to show that the statement holds for n + 1 players. Consider a (n + 1)-player game with ascending values (v1 v2 . . . vn vn+1). The median is vd(n+1)/2e. Let’s consider a player i such that vi < vd(n+1)/2e. If vi changes their reported value to vi0 > vi, two scenarios can occur:
(a) If vi0 vd(n+1)/2e , the median remains vd(n+1)/2e , which is analogous to the n-player game from the inductive hypothesis.
