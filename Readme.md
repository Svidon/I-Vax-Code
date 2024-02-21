# I-Vax Game

---

This repository contains the data and the code of the analysis for the I-Vax game presented in [this paper](paper link).

In the game, the players could take the decision of vaccinating against a fictional disease, which spread through Bluetooth contacts of their smartphones.


## Data Structure

Given this context, the data in `Anonymized Data` is structured in the following way (* stands for the number of round played):
* `end_of_wave_status_*.csv`: Final state of the players at the end of each round. More in detail, remaining points, state and decision to vaccinate. The timestamp of the vaccination and of the creation of this digest are also present
* `wave*_feedback_eow.csv`: Feedback given to the players at the end of rounds. This is only present for the feedback conditions in which players received information about the local or global environment. Columns with `*_interactions` refer to the number of vaccinated/infected/recovered players the user had interactions with (to be used for rounds 5-8); columns with `*_all` refer to the total population (to be used for rounds 9-12). We also include the total number of interactions
* `wave*_every_feedback.csv`: These are the daily feedbacks given to players during the rounds 5-12. Same as the previous format, but we also have the `day` column


## Analysis Code

The notebook `Analysis.Rmd` contains the code to run the analysis described in the paper, along with some instructions. We also share `Analysis.nb.html` as the HTML version.

The first code cell includes the library dependencies used. The notebook follows the same structure as the paper, with a first part which structures the data so that it is fit for the models used