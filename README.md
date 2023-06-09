# ERAV1BACKPROPAGATION

BACKPROPAGATION
We have the error E=E1+E2 & we will try to minimize the error through backpropagation . calculating the values we have to use for back propgation:

STEP 1 :

h1=w1i1+w2i2 h2=w3i1+w4i2 a_h1=σ(h1)=1/(1+exp(-h1)) a_h2=σ(h2) o1=w5a_h1+w6a_h2 o2=w7a_h1+w8a_h2 a_o1=σ(o1) a_o2=σ(o2) E_total=E1+E2 E1=1/2*(t1-a_o1)^2 E2=1/2*(t2-a_o2)^2

STEP 2:

∂E_total/∂w5=∂(E1+E2)/∂w5 ∂E_total/∂w5=∂E1/∂w5 ∂E_total/∂w5=∂E1/∂w5=∂E1/∂a_o1∂a_01/∂o1∂o1/∂w5 ∂E1/∂a_o1=∂(1/2*(t1-a_o1)^2)/∂a_o1=(a_01-t1) ∂a_o1/∂o1=∂(σ(o1))/∂o1=a_o1*(1-a_o1) ∂o1/∂w5=a_h1

STEP 3:

∂E_total/∂w5=(a_01-t1)a_01(1-a_o1)*a_h1 ∂E_total/∂w6=(a_01-t1)a_01(1-a_o1)*a_h2 ∂E_total/∂w7=(a_02-t2)a_02(1-a_o2)*a_h1 ∂E_total/∂w8=(a_02-t2)a_02(1-a_o2)*a_h2

STEP 4 :

∂E1/∂a_h1=(a_01-t1)a_01(1-a_01)*w5 ∂E1/∂a_h1=(a_02-t2)a_02(1-a_02)*w7 ∂E_total/∂a_h1=(a_01-t1)a_o1(1-a_o1)*w5+(a_02-t2)a_o2(1-a_o2)*w7 ∂E_total/∂a_h2=(a_01-t1)a_o1(1-a_o1)*w6+(a_02-t2)a_o2(1-a_o2)*w8

STEP 5 :

∂E_total/∂w1=∂E_total/∂a_h1∂a_h1/∂h1∂h1/∂w1 ∂E_total/∂w2=∂E_total/∂a_h1∂a_h1/∂h1∂h1/∂w2 ∂E_total/∂w3=∂E_total/∂a_h2∂a_h2/∂h2∂h2/∂w3

STEP 6 :

∂E_total/∂w1=((a_01-t1)a_o1(1-a_o1)*w5+(a_o2-t2)a_o2(1-a_o2)*w7)a_h1(1-a_h1)*i1 ∂E_total/∂w2=((a_01-t1)a_o1(1-a_o1)*w5+(a_o2-t2)a_o2(1-a_o2)*w7)a_h1(1-a_h1)*i2 ∂E_total/∂w3=((a_01-t1)a_o1(1-a_o1)*w6+(a_o2-t2)a_o2(1-a_o2)*w8)a_h2(1-a_h2)*i1 ∂E_total/∂w4=((a_01-t1)a_o1(1-a_o1)*w6+(a_o2-t2)a_o2(1-a_o2)*w8)a_h2(1-a_h2)*i2

CACLCULATION 1ST STEP(1ST ROW OF EXCEL)

Now I have taken some random value of t1=0.01,t2=0.99,i1=0.5,i2=0.1,w1=0.15,w2=0.2,w3=0.25,w4=0.3,w5=0.4,w6=0.45,w7=0.5,w8=0.55 All the other values (h1,a_h1,h2,a_h2,o1,a_o1,o2,a_o2,E1,E2,E,∂E/∂w1,∂E/∂w2,∂E/∂w3,∂E/∂w4,∂E/∂w5,∂E/∂w6,∂E/∂w7,∂E/∂w8

CALCULATION 2ND STEO (2ND TO MORE ROWS OF EXCEL)

t1=0.01,t2=0.99,i1=0.5,i2=0.01 shall be fixed w1,w2,w3,w4,w5,w6,w7,w8 shall change as per formula (w-(learning rate* ∂E/∂w)) accordingly all the other values changes as per above mentioned formula & same goes for multiple iteration.

SNAPSHOT OF EXCEL :

![image](https://github.com/RAMGUNJAN/ERAV1BACKPROPAGATION/assets/47599939/585aa219-7497-400e-8a99-11b1618ae45b)


loss graph (For lerning rate 0.1,0.2,0.5,0.8,1,2)

![image](https://github.com/RAMGUNJAN/ERAV1BACKPROPAGATION/assets/47599939/1542c7ad-555b-4518-bbc8-9a715ab084d1)

![image](https://github.com/RAMGUNJAN/ERAV1BACKPROPAGATION/assets/47599939/8c747077-f01f-4764-a37e-78c9b445f164)

![image](https://github.com/RAMGUNJAN/ERAV1BACKPROPAGATION/assets/47599939/d4de80a4-3824-4672-bc6d-381f2eb4d05c)

![image](https://github.com/RAMGUNJAN/ERAV1BACKPROPAGATION/assets/47599939/8fe9f96d-857d-4760-8bcb-478d6fe212c7)

![image](https://github.com/RAMGUNJAN/ERAV1BACKPROPAGATION/assets/47599939/7ed7c0fe-1287-467d-b62b-7d3643f08347)

![image](https://github.com/RAMGUNJAN/ERAV1BACKPROPAGATION/assets/47599939/53baca81-51c8-4cd2-9fdd-a7bcc575f626)

![image](https://github.com/RAMGUNJAN/ERAV1BACKPROPAGATION/assets/47599939/f625495f-04c1-400b-8ac7-f2d9c37cf720)


With more iteration loss converges to lower.

We can change random value of t1=0.01,t2=0.99,i1=0.5,i2=0.01 & have look.
