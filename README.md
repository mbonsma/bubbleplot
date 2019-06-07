# bubbleplot
Simulating bacteria with a CRISPR immune system interacting with phages.

## About

The [Jupyter notebook](https://github.com/mbonsma/bubbleplot/blob/master/evolution_bubble_animation.ipynb) 
in this repo contains code to visualize the results of a simulation of 
bacteria interacting with phages. Running the notebook from top to bottom 
generates a gif and a .mp4 video of successive time points from the simulation 
results in the data folder. 

## Bacteria-phage interactions

Bacteria are one of the most abundant life forms on earth, and phages (virues
which infect bacteria) are bacteria's oldest and greatest enemies. Bacteria
have evolved many tricks to avoid being killed by phages, but nearly all involve
being born with a lucky mutation that provides resistance. There is one notable
exception, however: the CRISPR immune system is *adaptive* - bacteria with
CRISPR can learn from past phage infections by storing small pieces of phage DNA
in their own DNA like a list of mugshots. Bacteria can use these mugshots to 
recognize and destroy those phages if similar ones return to infect again. 
But phages can mutate their DNA, like putting on
a disguise so that the bacteria can no longer recognize them using their mugshots. 
When phages "escape" by mutating, bacteria can "catch up" by capturing a new mugshot, 
and so begins an evolutionary arms race.

This movie visualizes a simulation of bacteria interacting with phages as they 
each evolve to try to outsmart the other. The simulation starts with a population 
of "naive" bacteria that are all the same and that don't have any CRISPR mugshots, and a population of phages 
that are all identical to each other as well. The black circle at the centre shows the number of original phages; 
the naive bacteria are not shown. 
As time goes on, phages infect bacteria and reproduce, and they sometimes mutate to a 
new DNA sequence. New phage sequences are shown in different colours and positions around the
original black circle - the grey lines connect phages to their "parent" phage population.
Each mutation takes that new phage population one step further away from the centre of the
circle. 

While phages are reproducing and mutating, bacteria can acquire mugshots that match a particular phage
population. The number of bacteria with a particular mugshot is represented by the size and 
colour of each circle on the left panel of the movie.

The specific colour of each sub-population is not meaningful by itself:
we assume that each phage mutation is equally good, and if a bacterium has a mugshot, 
all that matters is whether or not that mugshot matches a phage (which is true when 
a bacteria and phage sub-population are the same colour). Likewise, the position of each
circle does not relate to actual position in space (which we don't consider in these 
simulations); the position in the movie is only a representation of how many phage 
mutations have taken place since the start of the simulation. 

This method of visualizing these simulations reveals a few interesting things. First, the 
arms race never ends: new phages are always appearing, and older ones are continuously going extinct. 
No one sub-population sticks around forever. 
Second, bacteria are following along quite closely: when a phage population starts to grow
large, a population of bacteria with a matching mugshot will quickly appear.Watching these movies 
has helped us get intuition for what’s going on when bacteria and phages interact and co-evolve. 
