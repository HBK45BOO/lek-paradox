# lek-paradox
#This is a line from RStudio
#Line added from GitLab

#Packages
install.packages("gitcreds")
install.packages("credentials")
install.packages("usethis")
##Update Keys

gitcreds::gitcreds_set()


########Things to add
#Agents with 2 sets of values on one characterstic
#1-20 maybe dont use Excel, only for the first run
#Add a mutant chance generator
###Could be something that , on X chance, right before a gene is chosen from a given loci to regenerate a value on the chosen loci. 

#EX. Birth of new agent wouldve gotten the 15/20 from parent, but mutation chance ticked and the 15/20 was rerolled to a 4/20. Could have a mutation chance spectrum/range
#IE 15 can only be changed from 13-17 or a value of 7 can only be changed from 5 to 9.

#Could the female agents also have a random set of trait values as well? And females that are above a mates trait value will try to get the highest etc
#Whilst females that are below a mates trait value will try to choose them as well?
#Could make it so there is only a 1 to 2 ratio? 1 F to 2 M?

###########Read Files and Set Directories


########Model Parameters##########
#######Agent Parameters#########
popsize<-1000


agentgenerate<-function(n){

#Assign Agent a random gender
  gender<-sample(c("male","female"),n,replace=T)

#Assign Randon trait value for men
  tvmale1<-sample(c("1"-"20"),n,replace=T)
  tvmale2<-sample(c("1"-"20"),n,replace=T)
#Assign Random trait preference for woman
  tvpreference<-sample(c("1"-"20"),n,replace=T)

  agents<-data.frame(gender,tvmale1,tvmale2,tvpreference)



Agents$Chosen<- if else (Agents$Picked >= 0, "NR", "R" )


#NR= No Reproduce R= Reproduce

#Set up: choosing randomly between 2 genes of a trait at a single loci
#Set up: Create new matrix of agents with the new set of vtrait values
#Repeat?

sexydata$orientationtruecode<- ifelse(sexydata$relationship_orientation >= 0, "STM", "LTM")
table(sexydata$orientationtruecode) 

if else ()