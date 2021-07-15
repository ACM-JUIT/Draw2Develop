# Draw2Develop - Deep Learning & Web Development
Draw2Develop is a website that is built to help people generate basic HTML & CSS code without going through the hassle of actually writing it.


## About The Model
This project makes use of deep learning concepts, mainly Convolutional Neural Networks (CNN), to read a hand-drawn image of a website provided by the user and then identify the components present in the drawing to create a basic HTML & CSS based single-page website. 
The deep learning model uses functional API and presents us with 4 outputs coresponding to the 4 components of the web page which are discussed later here.

### Technologies Used
* **Pandas:** It is a fast, powerful, flexible and easy to use open source data analysis and manipulation tool, built on top of the Python programming language.

* **TensorFlow:** TensorFlow is an end-to-end open source platform for machine learning. It has a comprehensive, flexible ecosystem of tools, libraries and community resources that lets researchers push the state-of-the-art in ML and developers easily build and deploy ML powered applications.

* **TensorFlow (keras):** Keras is the high-level API of TensorFlow 2, an approachable, highly-productive interface for solving machine learning problems, with a focus on modern deep learning. It provides essential abstractions and building blocks for developing and shipping machine learning solutions with high iteration velocity.

### Activation Functions 
* **Exponential Linear Unit (ELU):** It is a function that tends to converge cost to zero faster and produce more accurate results. Different to other activation functions, ELU has a extra alpha constant which should be positive number.

![](https://i.imgur.com/qHW79Vk.png)


* **Sigmoid:** It is normally used to refer specifically to the logistic function, also called the logistic sigmoid function. All sigmoid functions have the property that they map the entire number line into a small range such as between 0 and 1, or -1 and 1.

![](https://i.imgur.com/kGVHm7e.png)






## Dataset
Our team has collectively made over 80 hand-drawn and digital images consisting of multiple variations of the 4 major components.

### Components 
Our final website will consist of 4 major components:
* Navigation Bar
* Main Section
* Side-Bar
* Footer

We have made 4 types of variations from the above-mentioned components namely:

**1. Single Component Images**
* Navigation Bar
* Main Section
* Side-Bar
* Footer

**Example:**

![](https://i.imgur.com/hvg4K0M.png)




**2. Dual Component Images**
* Navigation Bar, Side-Bar
* Navigation Bar, Footer
* Main Section, Side-Bar
* Main Section, Footer
* Main Section, Navigation Bar
* Side-Bar, Footer

**Example:**

![](https://i.imgur.com/eOdliTL.png)



**3. Triple Component Images**
* Navigation Bar, Side-Bar, Footer
* Navigation Bar, Footer, Main Section 
* Main Section, Side-Bar, Navigation Bar
* Main Section, Side-Bar, Footer

**Example:**

![](https://i.imgur.com/BifIWFE.png)


**4. Quad Component Image (Full Page)**

**Example:**

![](https://i.imgur.com/dzBSW3c.png)




### Rules
For better functioning of our model, we have used different rules and patterns to help it recognize the components more efficiently. These rules are also to be followed by the user while drawing out the web page. These rules are as follows:

**1. Nav Bar:** The nav-bar is to be made on top of the drawing page. It does not consist of any kind of pattern. The space inside the bounding box of the nav bar is to be left empty.

**2. Main Section:** This is the biggest section of the website so it should look its part in the drawing also. The space inside the bounding box of the main section has a cross (X) pattern made up of lines connecting the opposite ends of the bounding box.

**3. Side Bar:** The side-bar is to be placed parallel to the main section and to the right of the drawing. The pattern inside the bounding box consists of multiple vertical lines running from top to bottom (or vice versa) of the bounding box and parallel to each other.

**4. Footer:** The footer is to be placed at the bottom of the drawing. The pattern inside the bounding box consists of horizontal lines running from left to right (or vice versa) of the bounding box and parallel to each other.

## Results
Val-loss = 0.55

![](https://i.imgur.com/Xhf1Eto.png)



### Test Images Results

| [1 0 0 0] | [0 0 1 0] | [0 1 0 0] |
| -------- | -------- | -------- |
| ![](https://i.imgur.com/9n2lyzH.png)  | ![](https://i.imgur.com/UhTkuXO.jpg)     | ![](https://i.imgur.com/TKKBQzi.png)    |


|[0 0 0 1] | [1 1 0 0] | [1 1 1 1] |
| -------- | -------- | -------- |
| ![](https://i.imgur.com/LAKoBBI.png)   | ![](https://i.imgur.com/nAfzpsE.png)  |![](https://i.imgur.com/1UR4pkh.jpg)   |
