# tournamentSimulator

Sports Tournament Simulation
This program simulates a sports tournament and calculates each team's chances of winning based on the simulation results. The simulation uses the Elo rating system, which is commonly used to rate chess players but can be applied to other sports as well.

Requirements
Python 3.x
Usage
The program takes one argument: the filename of the CSV file containing the team data. Run the program using the following command:

Copy code
python tournament.py FILENAME
where FILENAME is the name of the CSV file.

Input
The program expects a CSV file with the following columns:

team: the name of the team
rating: the Elo rating of the team
Output
The program prints each team's chances of winning, according to the simulation. The output is sorted by the likelihood of winning, with the most likely winner at the top.

Simulation Details
The program simulates a round-robin tournament using the Elo rating system. In each round, each team plays one game against every other team. The simulation calculates the probability of each team winning each game based on their Elo ratings, and then randomly determines the winner based on those probabilities.

The simulation is run N times (where N is a constant defined in the code), and the number of wins for each team is recorded. The program then calculates the percentage of simulations in which each team won the tournament, which is printed as the output.

Code Structure
The code is organized as follows:

The main function is the entry point of the program. It reads in the team data from the CSV file and calls the simulate_tournament function to run the simulation.
The simulate_tournament function simulates a tournament using the Elo rating system. It calls the simulate_round function to simulate each round of the tournament, and continues until there is only one team left (the winner).
The simulate_round function simulates a round of games. It calls the simulate_game function to simulate each individual game.
The simulate_game function simulates a single game between two teams using the Elo rating system. It calculates the probability of each team winning based on their Elo ratings and randomly determines the winner based on those probabilities.
