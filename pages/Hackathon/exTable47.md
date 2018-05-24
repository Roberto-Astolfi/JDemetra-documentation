---
layout: left-menu
title: exTable47
order: 1
---

**TRAMO specification options for manual identification of the ARIMA model.**

**Option**


* [Automatic](#automatic)
* [Mean](#mean)
* [P](#p)
* [phi](#phi)
* [D](#d)
* [Q](#q)
* [theta](#theta)
* [BP](#bp)
* [Bphi](#bphi)
* [BD](#bd)
* [BQ](#bq)
* [Btheta](#btheta)

### Automatic
*automdl; ami;idif, inic* 

When marked it enables an automatic modelling of the ARIMA model to be performed.

#### Mean
*mean;imean*
	
When marked it is considered that the mean is part of the ARIMA model (it highly depends on the chosen model). lue defined by the user.

#### P
*arima; p*	

The order of the non-seasonal autoregressive polynomial. The maximum order of the non-seasonal autoregressive polynomial is 4. The default value is 0.

#### phi
*arima; phi, jpr*	
Coefficients of the non-seasonal, autoregressive polynomial (AR). If used, each non-seasonal AR parameter in the model requires a label that indicates the procedure of its estimation. The choice can be made from:
* Undefined - estimates a parameter without the use of any user defined input (the default value).
* Initial - estimates a parameter using as initial condition the value defined by the user.
* Fixed - holds a parameter fixed during estimation at the value defined by the user.

#### D
*arima; d*	

Non-seasonal differencing order. The maximum number of non-seasonal differences is 2. The default value is 1.

#### Q
*arima; q*	

The order of the non-seasonal moving average polynomial. The maximum order of the non-seasonal moving average polynomial is 4. The default value is 1.

#### theta
*arima; th, jqr*

Coefficients of the parameters of the non-seasonal, moving average polynomial (MA). If used, to each non-seasonal MA parameter in the model a label that indicates the procedure of its estimation should be assigned. The choice can be made from:
* Undefined - estimates a parameter without the use of any user defined input (the default value).
* Initial - estimates a parameter using as initial condition the value defined by the user.
* Fixed - holds a parameter fixed during estimation at the value defined by the user.

#### BP
*arima; bp*

The order of the seasonal autoregressive polynomial. The default value is 0.

#### Bphi 

*arima;bphi, jps*

Coefficients of the seasonal autoregressive polynomial (AR). If used, to each seasonal AR parameter in the model a label that indicates the procedure of its estimation should be assigned. The choice can be made from:
* Undefined - estimates a parameter without the use of any user defined input (the default value).
* Initial - estimates a parameter using as initial condition the value defined by the user.
* Fixed - holds a parameter fixed during estimation at the value defined by the user.

#### BD
*arima; bd*

Seasonal differencing order. The maximum number of seasonal differences is 1. The default value is 1.

#### BQ
*arima; bq*

The order of the seasonal moving average polynomial. The maximum order of the seasonal moving average polynomial is 1. The default value is 1.

#### Btheta
*arima; bth, jqs*

Coefficients of the parameters of the seasonal moving average polynomial (MA). If used, each seasonal MA parameter in the model requires a label that indicates the procedure of its estimation. The choice can be made from:
* Undefined - estimates a parameter without the use of any user defined input (the default value).
* Initial - estimates a parameter using as initial condition the value defined by the user.
* Fixed - holds a parameter fixed during estimation at the value defined by the user.