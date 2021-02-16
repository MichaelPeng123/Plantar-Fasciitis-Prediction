# Plantar Fasciitis Prediction Diagnosis Tool

Plantar fasciitis risk diagnosis with machine learning analysis to encourage safe and efficient running form

Names: Michael Peng and Ricky Wang

Background Information:
Plantar fasciitis is an extremely common heel condition that inhibits the lives of over 1% of the adult US population, with athletes being especially prone to injury. Plantar fasciitis could take over 6 months to recover from while under active treatment, and in worst cases, surgery is required, extending the recovery time to over 9 months. Currently, there is no method of determining whether an athlete’s running mechanics contribute to their risk of getting plantar fasciitis, despite poor running mechanics being a key cause of the condition.

Introduction:
Our project functions as a pre-diagnosis tool for plantar fasciitis that takes attributes of one's stride as input, and outputs the user's risk of contracting the condition. If successful, an athlete can determine whether they need to adjust their running mechanics and take preventative measures such as strength training, possibly preventing an injury that would’ve been season or even career ending.

Methods:
Because poor running mechanics are a proven cause of plantar fasciitis, we used attributes of an athlete’s stride—shoe size, resultant impulse from each step, and max force per step—as the baseline to predict their risk of plantar fasciitis. The code uploaded into the arduino circuit collects force values measured by the sensor every few milliseconds, writes it onto the SD card, and also calculates and parses the collected data into sections: maximum force and impulse. In the Jupyter Notebook, the logistic regression model is then trained with a 65%-35% split in the data. Ridge regularization was used to avoid overfitting the training data and limited-memory BFGS was the descent algorithm used to determine the global minimum of the cost function. Attributes of the model are then evaluated and various graphs, which can be analyzed to determine which factor contributed most to an athlete's risk of plantar fasciitis, are graphed.

Results:
Our model found that the impulse and maximum force values reached when the foot of a runner strikes the ground are contributing factors to plantar fasciitis, as they exhibit a strong positive linear relationship with the probability of runners contracting plantar fasciitis. Contact area, which was measured through shoe size, exhibits a less obvious correlation. Our model ultimately predicted the test data set with an accuracy of 82.9%, which is high considering that predictions were based solely off of attributes of running mechanics. In addition to a diagnosis and risk factor, we provide visualization tools that offer insight into the main variables that contribute to plantar fasciitis, specific to each athlete's condition. Applying our studies to running mechanics, we concluded that preventing heel striking and increasing stride speed are possible solutions to preventing variables analyzed in causing plantar fasciitis, as these two tecniques minimize max force and impulse.
f
Further Research:
1. Other diseases such as shin splints, heel spur, etc.
2. Multiclass logistic regression for multiple injuries
3. Accelerometer on arduino for more variable measurements

Instructions For Usage:
1. Download Both Datasets
2. Make sure they are named synopsisData.csv and usingData.csv
3. Open Code in Jupyter Notebook using Anaconda Navigator (It must be opened using
Jupyter because the code is divided into sections)
4. Run each section, as you run you will notice there will be certain output values,
ignore those
5. You will eventually see graphs with visualization of all the data
6. The graphs at the bottom is the segment of code that athletes run for project usage

Demo Video:
https://www.youtube.com/watch?v=Rtc5fLSZ0dc

Detailed Project Design Found here:
https://drive.google.com/drive/folders/1y8hjC2oPE6Y8HEOHJ2Pa9vK9DwhGrNgd?usp=sharing
