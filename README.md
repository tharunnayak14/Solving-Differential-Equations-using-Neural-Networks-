# Solving-Differential-Equations-using-Neural-Networks-

Consider the first order ODE: 
 	dΨ(x)/dx = f(x, Ψ)   (1)
 </br> </br>
with x ∈ [0, 1] and with the Initial Condition Ψ(0) = A. </br> </br>
A trial solution is written as:  Ψtrial(x) = A + xN(x, p) </br>
where N(x, p) is the output of a ANN with one input unit for x and weights p.  </br>
Now all we need is a loss function, Ψtrial(x) is the solution of the differential equation </br> </br>
	d Ψtrial(x) /dx ≈ f(x, Ψtrial) </br>
 d Ψtrial(x) /dx - f(x, Ψtrial) ≈ 0  (2)  </br></br>
 we are trying to do is get (2) close to zero, then our trial solution approximates the analytical solution to a great accuracy.</br>

So we define the loss function as:</br></br>
	
	LOSS = ∑{ (d Ψtrial(x) /dx) - f(x, Ψtrial) }2    for all x ∈ [0, 1]

Now we can use this loss to compute the gradients and do weight updation</br>

</br>
<p><b>Question 1</b></p></br>

![question1](https://user-images.githubusercontent.com/52671445/144845678-7f79dba2-0ef6-4049-8a48-52c5e3ebcba5.jpg)
<p>&emsp; Ψ(0) = 0 and x ∈ [0, 2]</p>

![2021-12-03 13 34 43 localhost a9f9d05fcd77](https://user-images.githubusercontent.com/52671445/144845699-74492e0d-fbcb-4ee6-b8f6-d87f75329301.png)

</br>
<p><b>Question 2</b></p></br>

![qu2](https://user-images.githubusercontent.com/52671445/144846039-b05a72bb-7eff-419a-bea2-84f191df98c5.jpg)
<p>&emsp; Ψ(0) = 1 and x ∈ [0, 1]</p>
 

![2021-12-03 13 36 30 localhost 768b914a053a](https://user-images.githubusercontent.com/52671445/144846051-1c3eb64c-2f6e-42ad-a89d-65e380f2d78c.png)
</br>

Consider the 2nd order ode:</br>
 	<p>d<sup>2</sup>Ψ(x)/dx<sup>2</sup> = f(x, Ψ, dΨ/dx) </p></br>
	
![2021-12-01 21 47 34 arxiv org 46bf989a93d7](https://user-images.githubusercontent.com/52671445/144848088-2623a12b-6430-4f49-b044-ef3cb1090f4f.png)


 ![2021-12-01 21 44 45 arxiv org 482d49c0b910](https://user-images.githubusercontent.com/52671445/144847972-6782f59a-6db6-46f1-a2e1-07121ced0b39.png)

 
The loss function is same as in the case of first order ode</br>

</br>
<p><b>Question 3</b></p></br>

![2021-12-01 21 41 29 arxiv org d6d2402de42c](https://user-images.githubusercontent.com/52671445/144846131-77d16208-d9be-4a0e-99d3-dd0513e63bc4.png)
<p>&emsp; Ψ(0) = 1, dΨ(0)/dx = 1, x ∈ [0, 2]</p>



![2021-12-03 13 38 59 localhost 7b533322a39a](https://user-images.githubusercontent.com/52671445/144846155-304e11ba-72c6-4d68-983c-6f113eaef24f.png)

</br>
<p><b>Question 4</b></p></br>

![2021-12-01 21 41 29 arxiv org d6d2402de42c](https://user-images.githubusercontent.com/52671445/144846167-ef1fc5c3-81d6-4882-9298-f12a0ce6c295.png)
<p>&emsp; Ψ(0) = 1, Ψ(1) = sin(1)*e^(-1/5), x ∈ [0, 1]</p>


![2021-12-03 13 43 36 localhost bf27478d0ae6](https://user-images.githubusercontent.com/52671445/144846168-8bdd144c-9f2c-449b-9e11-beb35693f369.png)
