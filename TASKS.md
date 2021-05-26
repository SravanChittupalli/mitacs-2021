# Task 1
The task at hand is to get the bounding boxes around 3 objects
* Ripe strawberries  
* Unripe strawberries  
* Flowers  


To find the best method to do the above task, I will be doing a comparative study between 3 methods:  
- [*] Basic Image Processing  
- [ ] YOLO/ YOLO tiny  
- [ ] U-Net  

# Task 2

% ripeness of strawberry

## 1st Method

After getting detections from the trained model, basic image processing can be done to find the area that is red and the area that is green.   

`% ripeness = Area red / Total area`  


## 2nd method 

Instead of giving the percentage of ripeness we can give it 4 stages like unripe, partially ripe, almost ripe and ripe.  


From the detection that we get from the trained network we can apply a Red and Green mask over the strawberry and then plot a histogram. We can weigh both the histogram mean and classify the result into one of the classes mentioned above.  
