#Loci Mating Model/Lek Paradox Prof Dan and LRM

##############HOW TO USE GIT##########
#OPEN READ ME PROJECT FROM FILE TITLED READ ME. THEN GO TO THE GIT TAB, STAGE BOX READ ME, PRESS COMMIT, EDIT THE MESSAGE, THEN PUSH! 

#Packages
install.packages("gitcreds")
install.packages("credentials")
install.packages("usethis")
library(ggplot2)
##Update Keys
gitcreds::gitcreds_set()

#####Things to do (needed)######

#Female Agents choose to reproduce with males that have greater than or equal to at least 1 loci value.
#Figure out how to make drop downs for cleanliness

########Things to add (possibly?)#############
#Agents with 2 sets of values on one characterstic (Done)
#1-20 maybe dont use Excel, only for the first run (Done)
#Make females agents choose male agents that is greater than or equal to tvpreference value (WIP)
#Add a mutant chance generator (WIP)
###Could be something that , on X chance, right before a gene is chosen from a given loci to regenerate a value on the chosen loci. 

#EX. Birth of new agent wouldve gotten the 15/20 from parent, but mutation chance ticked and the 15/20 was rerolled to a 4/20. Could have a mutation chance spectrum/range
#IE 15 can only be changed from 13-17 or a value of 7 can only be changed from 5 to 9.

#Could the female agents also have a random set of trait values as well? And females that are above a mates trait value will try to get the highest etc (meant to mimic and check the mating market value hypothesis? Might be getting to far ahead of myself here)
#Whilst females that are below a mates trait value will try to choose them as well?
#Could make it so there is only a 1 to 2 ratio? 1 F to 2 M?


###########Read Files and Set Directories


########Model Parameters##########

modelloops<-10

#######Agent Parameters#########
popsize<-20

n<-popsize

maxdates<-1

locithreshold<-15
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
  
  agents<-data.frame(ID,sex,tvmaleloci1,tvmaleloci2,tvpreference)

  return(agents)
  
}

bettersample<-function(x,size,replace=False,prob=NULL){
  
  
  #If the sample vecotr has more than 1 element
  if(length(x)>1){
    
    #Use sample just like normal
    x<-sample(x,size,replace,prob)
    
  }
  
  return(x)
}

 
##########Model Start############

#(MAJOR WIP)results<-data.frame('rand'=rep(NA,modelloops),'nonrand'=rep(NA,modelloops))

###Life Cycle###
  
#Repeat until all females have chosen a male
  while(length(pairedfemales)<nrow(females)){
  #mate
  
  #females choose males, not the other way around
  fdate<-bettersample(females$ID[!(females$ID %in% pairedfemales)],1)
  
  #Track number of mate decisions and keep it at 2 per female
  
  females$numdates[date]<-females$numdates[fdate]+1
  
    
    #Offer#
    
    #Determine how selective agents will be based on number of dates completed so far
    
    fchoosy<-((maxdates+1)-females$numdates[fdate])/maxdates

     #Prevent choosiness values less than 0
    fchoosy<-ifelse(fchoosy>0,fchoosy,0)
    
    #Set the probability of a commitment offer based on date attractiveness
    #and agent selectiveness
    
    fp<-((males$tvmaleloci1,tvmaleloci2[mdate]^3)/1000)^fchoosy

    

females<-agentgenerate(popsize/2,"female")
males<-agentgenerate(popsize/2,"male")


#Maybe useful, not sure yet?
pairedfemales<-c()
pairedmales<-c()

###################################### WIP Line, Everything below this is code that is WIP
###################################### Or does not work due to errors.

results<-data.frame(matrix(NA,modelloops,2))

colnames(results)<-c("R","NR")

for(i in 1:modelloops){

######Life Cycle##### 

#Define Loci Preference for all females

#Agent females choose males with Loci Preference
#Have the female agent decide whether to reproduce depending on loci value
    reproduce<-females$tvpreference[tvpreference>=(tvmaleloci1,tvmaleloci2)]
    
#males that are chosen reproduce and create offspring with loci values similar (refer to lines 24- 28) to themselves. 

#Males that are not chosen die and are replaced by new males with different loci values, new set of females is created.

#Repeat and see how to trait values chosen change over generations?
    
    
switchguess<-doors$number[!(doors$number%in%c(startguess,reveal))]

 movedecision[a]<-assessment<threshold




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

