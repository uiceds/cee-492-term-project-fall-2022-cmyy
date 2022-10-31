
A persuasive prediction model needs to be trained on the data with enough scale. Thus, before we move to the model part, we need to figure out the distribution of data itself.

First, we want to know the amount of data of each breed. Notice that many mixed breed dogs miss their secondary breed, so instead of considering secondary breeds, we only focus on their primary breeds. The sorted amount of each primary breed is shown in Figure 1.

![Figure 1](/Users/kevinlin/Desktop/UIUC/2022 Fall/CEE492 Data Science for CEE/Team Project/Figure 1.png)
Figure 1. Amount of each Primary Breed

There are 203 primary breeds, however, most of them do not have enough data to support for a meaningful model. We choose those amount that are larger than 1000, which is shown in Table 1.


|      Primary Breed      |   Amount   |
|-------------------------|------------|
|   Labrador Retriever    |    3625    |
|     Pit Bull Terrier    |    3077    |
|        Chihuahua        |    1740    |
|       Mixed Breed       |    1454    |
|         Terrier         |    1264    |
|          Hound          |    1112    |
|          Boxer          |    1080    |
|     German shepherd     |    1029    |

Table 1. Amount of each Primary Breed (Only shows those amount that are larger than 1000)

After sorting the amount, we want to have a brief knowledge of each breed with their children friendliness tend. Here, we made a group bar plot that shows the fraction of children friendliness with respect to their primary breed. 

![Figure 2](/Users/kevinlin/Desktop/UIUC/2022 Fall/CEE492 Data Science for CEE/Team Project/Figure 2.jpg)
Figure 2. Children-Friendliness by Breed

We also want to know how efficient the actions (fixing or house training) would be to make each breed to be friendly with children. Thus, we collected those dogs with and without fixed or trained to make another grouped bar plot. We only show data without any actions, the actions process would be the same as this. 

![Figure 3](/Users/kevinlin/Desktop/UIUC/2022 Fall/CEE492 Data Science for CEE/Team Project/Figure 3.png)
Figure 3. Children-Friendliness by Breed without actions

Finally, considering some breeds might be larger on size, or the amount of data in particular age, particular sex and particular size might be very small. Thus, we need to know the distribution of our data in each combination. Here we only show the distribution of “Labrador Retriever”, the process is the same in other breeds.

![Figure 4](/Users/kevinlin/Desktop/UIUC/2022 Fall/CEE492 Data Science for CEE/Team Project/Figure 4.png)
Figure 4. The distribution of “Labrador Retriever” in each combination

We could know that the size of “Labrador Retriever” usually “Large” or “Extra Large”, so we could only focus on these sizes when establishing the prediction model of this breed. 

We could also realize that the fixed “Labrador Retriever” is much more than unfixed (around 20%). But considering the scale of our dataset (3625), we could still have 725 data. We say that this is enough to establish a persuasive prediction model.
