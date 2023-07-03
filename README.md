# lek-paradox
#This is a line from RStudio
#Line added from GitLab

#Packages
install.packages("gitcreds")
install.packages("credentials")
install.packages("usethis")
library(ggplot2)
##Update Keys

gitcreds::gitcreds_set()


########Things to add (possibly?)
#Agents with 2 sets of values on one characterstic
#1-20 maybe dont use Excel, only for the first run
#Add a mutant chance generator
###Could be something that , on X chance, right before a gene is chosen from a given loci to regenerate a value on the chosen loci. 

#EX. Birth of new agent wouldve gotten the 15/20 from parent, but mutation chance ticked and the 15/20 was rerolled to a 4/20. Could have a mutation chance spectrum/range
#IE 15 can only be changed from 13-17 or a value of 7 can only be changed from 5 to 9.

#Could the female agents also have a random set of trait values as well? And females that are above a mates trait value will try to get the highest etc (meant to mimic and checl the mating market value hypothesis)
#Whilst females that are below a mates trait value will try to choose them as well?
#Could make it so there is only a 1 to 2 ratio? 1 F to 2 M?

###########Read Files and Set Directories


########Model Parameters##########

modelloops<-100

#######Agent Parameters#########
popsize<-20
locithreshold<-15
n<-popsize


#locithreshold is the preference value in which mates will always be chosen to reproduce. FOR EX if an agent is 16:5 on a tv value then they will be chosen to r. If 14:5 then they will not be chosen 

############agent###########
agentgenerate<-function(n,sex){


#To Track Agent
  ID<-1:n
  
#Random Loci Assignment for the Males
  tvmaleloci1<-sample(c(1:20),n,replace=T)
  tvmaleloci2<-sample(c(1:20),n,replace=T)
  
#Random Loci Assignment for Females
  tvpreference<-sample(c(1:20),n,replace=T)
  
  agents<-data.frame(sex,tvmaleloci1,tvmaleloci2,tvpreference)

  return(agents)
  
}

 
#########Model Start

females<-agentgenerate(popsize/2,"female")
males<-agentgenerate(popsize/2,"male")

#Maybe
pairedfemales<-c()
pairedmales<-c()

######Life Cycle#####


results<-data.frame(matrix(NA,modelloops,2))

#Agent females choose males with Loci Preference
colnames(results)<-c("R","NR")

for(i in 1:modelloops){

#Female chooses male with loci preference


#Have the agent decide whether to reproduce depending on loci value
    reproduce<-females$tvpreference[tvpreference>=(tvmaleloci1,tvmaleloci2)]
    
    
    
    
switchguess<-doors$number[!(doors$number%in%c(startguess,reveal))]

 movedecision[a]<-assessment<threshold
#Define Loci Preference for all females



#Date#

#Pair random agents
#Must be opposite sex
#Must be unpaired

sample(females$ID[!(females$ID %in% pairedfemales)],1)
sample(males$ID[!(males$ID %in% pairedfemales)],1)













Chosen<-c()



generation 1<-data.frame(agents)

#Set up: choosing randomly(? or threshold) between 2 genes of a trait at a single loci
#Set up: Create new matrix of agents with the new set of vtrait values
#Repeat?

2+2
sexydata$orientationtruecode<- ifelse(sexydata$relationship_orientation >= 0, "STM", "LTM")
table(sexydata$orientationtruecode) 

if else ()


















agentgenerate<-function(n){

#Assign Agent a random gender
  gender<-sample(c("male","female"),n,replace=T)
  
#generate an ID number for each agent
  ID<-1:n

#Assign Randon trait value for men (make it choose only men)
  tvmaleloci1<-sample(c(1:20),n,replace=T)
  tvmaleloci2<-sample(c(1:20),n,replace=T)
  
#Assign Random trait preference for woman (make it only women)
  tvpreference<-sample(c(1:20),n,replace=T)
 
  agents<-data.frame(gender,tvmaleloci1,tvmaleloci2,tvpreference)

  return(agents)
}

agents

