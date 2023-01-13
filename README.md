# hearingaid-personalization
A dataset for hearing aid personalization.
# Personalizing Over-the-Counter Hearing Aids using Pairwise Comparisons 

**Dhruv Vyas, Ryan Brummet, Yumna Anwar, Justin Jensen, Erik Jorgen
Jorgensen, Yu-Hsiang Wu, and Octav Chipara**

Over-the-counter hearing aids enable more affordable and accessible
hearing health care by shifting the burden of configuring the device
from trained audiologists to end-users. A critical challenge is to
provide users with an easy-to-use method for personalizing the many
parameters which control sound amplification based on their preferences.
This paper presents a novel approach to fitting hearing aids that
provides a higher degree of personalization than existing methods by
using user feedback more efficiently. Our approach divides the fitting
problem into two parts. First, we discretize an initial 24-dimensional
space of possible configurations into a small number of presets. Presets
are constructed to ensure that they can meet the hearing needs of a
large fraction of Americans with mild-to-moderate hearing loss. Then, an
online agent learns the best preset by asking a sequence of pairwise
comparisons. This learning problem is an instance of the multi-armed
bandit problem. We performed a 35-user study to understand the factors
that affect user preferences and evaluate the efficacy of multi-armed
bandit algorithms. Most notably, we identified a new relationship
between a user's preference and presets: a user's preference can be
represented as one or more preference points in the initial
configuration space with stronger preferences expressed for nearby
presets (as measured by the Euclidean distance). Based on this
observation, we have developed a Two-Phase Personalizing algorithm that
significantly reduces the number of comparisons required to identify a
user's preferred preset. Simulation results indicate that the proposed
algorithm can find the best configuration with a median of 25
comparisons, reducing by half the comparisons required by the best
baseline. These results indicate that it is feasible to configure
over-the-counter hearing aids using a small number of pairwise
comparisons without the help of professionals.

You can download the data from the study described in the paper below.

## Description:

This folder contains five different files.

1.  [Audiogram-data.csv](Audiogram-data.csv)
2.  [REAR-data.csv](REAR-data.csv)
3.  [Comparison-data.csv](Comparison-data.csv)
4.  [Borda-scores.csv](Borda-scores.csv)
5.  [Presets.csv](Presets.csv)

### Audiogram data description:

This file contains audiogram data of study participants.

Columns description :

-   Subject Id : Id of participants recruited for the Study
-   Right 250 - 8000 : Hearing loss in dB at 250, 500, 1000, 2000, 3000,
    4000, 6000, 8000 Hz
-   Left 250 - 8000 : Hearing loss in dB at 250, 500, 1000, 2000, 3000,
    4000, 6000, 8000 Hz

### REAR prescriptions obtained using NAL-NL2: {#rear-data-descriptions}

Columns description :

-   Subject Id : Id of participants recruited for the Study
-   REAR frequencies 250 - 8000 : REAR at 65 dB SPL at 250, 500, 1000,
    2000, 3000, 4000, 6000, 8000 Hz
-   Test Ear : Ear used for study (Left or Right)

### Comparison data description:

Columns description :

-   Subject Ids : Id of participants recruited for the Study
-   B_a\_b : Probabilities of the participating preferring REAR a over b
    REAR in a pairwise comparison.\
    Please refer to our paper for more details ([Personalizing
    over-the-counter hearing aids using pairwise
    comparisons](https://www.sciencedirect.com/science/article/pii/S2352648321000507))

### Borda-scores data description:

Columns description :

-   Subject Ids : Id of participants recruited for the Study
-   B_x : Borda scores of x REAR after exhaustive pairwise comparison. :

### REAR of the presets: {#presets}

Columns description :

-   Preset ID : Preset ID given to the REAR
-   Freq 250 - 8000 : REAR at 65 dB SPL at 250, 500, 1000, 2000, 3000,
    4000, 6000, 8000 Hz for given preset ID.

For questions please email Octav Chipara at <octav-chipara@uiowa.edu>
