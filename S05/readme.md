# S5-Assignment Solution
### Name: Tony James


## Step 1 - start from a decent point

####  Targets:
  1. we need to start at some point so start with some model close to 10 K params and see how things go
  2. reach 99.4 in 15 epochs 
  3. run for 15 epochs(to save time) and see how things goes
  4. no data agumentation for now
  
####  Results:
  1. Parameters: 10,790
  2. Best Train Accuracy: 98.59 (15th Epoch)
  3. Best Test Accuracy: 98.29 (14th Epoch)
    
####  Analysis:
  1. model did not reach the targets, 
  2. slight  over-fitting ??
  3. need to see how bad the last FC layer and remove it


  
## Step 2 - Add  Batch Norm and Regaularisation

####  Targets:
  1. Add batch norm to increase model efficency
  2. add dropoout to fix the difference between testing and training accuracy 
  3. run for 15 epochs(to save time) and see how things goes
  4. no data agumentation for now
  5. Conv --> Relu --> BN --> dropout seems to be the proper order
  
####  Results:
  1. Parameters: 10,970
  2. Best Train Accuracy: 95.22 (15th Epoch)
  3. Best Test Accuracy: 99.28 (10th Epoch)
    
####  Analysis:
  1. model did not reach the targets, 
  2. seems like model is under fitting
  3. remove the last FC layer and repalce it with efficient layers
  
  
## Step 3 - Add  Batch Norm and Regaularisation (reversed order)

####  Targets:
  1. Add batch norm to increase model efficency
  2. add dropoout to fix the difference between testing and training accuracy 
  3. run for 15 epochs(to save time) and see how things goes
  4. no data agumentation for now
  5. Conv --> Relu --> dropout --> BN 
  
####  Results:
  1. Parameters: 10,970
  2. Best Train Accuracy: 95.25 (15th Epoch)
  3. Best Test Accuracy: 99.30 (15th Epoch)
    
####  Analysis:
  1. model did not reach the targets, 
  2. seems like model is under fitting
  3. remove the last FC layer and repalce it with efficient layers
  4. here we got consitency in testing results,
     may be we should follow this order
     
## Step 4 - GAP, add layers and increase kernel size to match capacity

####  Targets:
  1. Add GAP
  2. run for 15 epochs(to save time) and see how things goes
  3. no data agumentation for now
  4. add layers to compensate for GAP
  
####  Results:
  1. Parameters: 9,118
  2. Best Train Accuracy: 98.50 (15th Epoch)
  3. Best Test Accuracy: 98.68 (10th Epoch)
    
####  Analysis:
  1. model did not reach the targets, 
  2. seems like model is under fitting
  
## Step 5 - add more layers, augmentation

####  Targets:
  1. add more layers
  2. run for 15 epochs(to save time) and see how things goes
  3. try image agumentation also
  
####  Results:
  1. Parameters: 10,094
  2. Best Train Accuracy: 98.34 (15th Epoch)
  3. Best Test Accuracy: 99.04 (10th Epoch)
    
####  Analysis:
  1. model did not reach the targets, 
  

