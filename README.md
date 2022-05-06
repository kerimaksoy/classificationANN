
<h4 align="left">In this project, binary classification is made by using artificial neural networks on the 'day_28_flg' attribute, which includes the information whether the patient died within 28 days, among a total of 44 attributes of 1776 patients hospitalized in the intensive care unit.</h4>
<p align="left">
</p>


><h3 align="left">Languages and Tools:</h3><h2 align="center">Python, Jupyter Notebook</h2><p align="center"> <a href="https://www.python.org" target="_blank" rel="noreferrer"> <img src="https://raw.githubusercontent.com/devicons/devicon/master/icons/python/python-original.svg" alt="python" width="40" height="40"/> </a> </p>

<h2 align="center">Dataset</h2>
<b>The dataset used in this project includes total of 44 attributes such as age, gender, weight, body mass index, body temperature, heart rate, potassium ratio in the blood of 1776 patients taken from the Physionet MIMIC-II database.</b>

<b>When the data distributions of the 4 attributes with the most null values in the data set are plotted:</b>

 ![1](https://user-images.githubusercontent.com/46629380/167046812-7ce770b9-81be-4428-86c6-3388da0e1e51.png)

It is seen that the data containing null values generally show a flattened distribution from the right side in the graph. Therefore, the blank values in the data set are filled with the median values of the data.

<b>Considering the distribution of 0 and 1 values included in the "28_day_flg" attribute on which we classify on the data set, which is 1 in cases where the patient died within 28 days, and it is 0 when the patient was alive:</b>

![2](https://user-images.githubusercontent.com/46629380/167047233-20b141d5-2a2a-44c5-87da-d2252c5c86b5.png)
 
 It can be seen that there is a large number difference between the cases where the data takes the values of 1 and 0. Since training our model with these data will negatively affect the model performance, an equal number of samples with 1 and 0 values are taken and a classification is made on a total of 566 data.
 
 <h2 align="center">Activation Function</h2>
 
 <b>First, let's compare the graphs of the accuracy values of 4 different activation functions to choose which activation function to use in the hidden layer of our neural network model:</b>
 
 ![3](https://user-images.githubusercontent.com/46629380/167047417-e8444931-ad89-4fe0-af41-452039fb282b.png)


<b>Then compare the graphs of the training and testing loss of these 4 activation functions:</b>

![4](https://user-images.githubusercontent.com/46629380/167047594-66a05fe2-6b12-4a23-b035-eedfe309c18e.png)

As can be seen from the graphs, although the 4 activation functions have similar accuracy values, we choose the activation function <b>"sigmoid"</b>, which is the activation function with the lowest error rate.
 
 <h2 align="center">Momentum Coefficient</h2> 

<b>In order to choose which momentum coefficient to use in our model, let's compare the graphs of the accuracy values ​​by giving the momentum values ​​of "0.1", "0.3", "0.6", "0.9" to our model with the sigmoid function, respectively:</b>

 ![5](https://user-images.githubusercontent.com/46629380/167047886-263147a2-dc01-4b91-a274-ff7e8aa9accc.png)
 
 <b>Then compare the graphs of the training and testing loss of these 4 momentum coefficients:</b>
 
 ![6](https://user-images.githubusercontent.com/46629380/167047949-f40af50e-8861-4261-ace3-628a678c5a2f.png)
 
As can be seen from the graphs, although 4 different momentum coefficients have similar accuracy values, we choose the momentum coefficient with the lowest error rate, which is the <b>“0.9”</b>.

 <h2 align="center">Learning Rate</h2> 
<b>We can choose which learning rate to use in our model with checking the graphs of the accuracy values by giving the learning rate values of “1”,”0.5”,“0.1”,“0.01” to our model with the sigmoid activation function and the momentum coefficient of 0.9, respectively:</b>

![7](https://user-images.githubusercontent.com/46629380/167048165-749fda5e-ad31-4aa4-868b-a31ade6628bf.png)

<b>Then compare the graphs of the training and testing loss for these 4 learning rates:</b>

![8](https://user-images.githubusercontent.com/46629380/167048214-abfad49e-d7c2-48b3-b393-fb40e1bbcc61.png)

As can be seen from the graphs, although 4 different learning rates have similar accuracy values, we choose the value <b>“0.01”</b>, which is the learning rate with the lowest error rate.

 <h2 align="center">Hidden Layer</h2> 
<b>After choosing the activation function, learning rate and momentum coefficient in our model, let's compare the accuracy and error values of the models with 1 and 2 hidden layers to decide how many hidden layers we will use in our model:</b>


<b>Model's accuracy and the training and testing loss which has only 1 Hidden Layer:</b>

![xx](https://user-images.githubusercontent.com/46629380/167048953-f32134ef-44cd-4f41-a212-e9ec6cdeb3c2.png)

<b>Model's accuracy and the training and testing loss which has 2 Hidden Layer:</b>

![gd](https://user-images.githubusercontent.com/46629380/167049276-c9d78835-1704-4066-a328-c7bee2a3ecf4.png)

<h2 align="center">Result</h2>
When the accuracy and error values are compared, it is seen that the model with 1 hidden layer has higher accuracy value and lower error value. Therefore, the artificial neural networks model that gives the best results with <b>%96.62 accuracy</b> is the model with <b>1 hidden layer, using the “sigmoid” activation function, a momentum coefficient of 0.9 and a learning rate of 0.01.</b>

The complexity matrix of the model:

![cn](https://user-images.githubusercontent.com/46629380/167049965-62d0cb14-a6fe-4362-9cee-56ae09c4045b.png)


<h2 align="center">Source</h2>
The dataset used in this project can be found on https://physionet.org/content/mimic2-iaccd/1.0/ 

