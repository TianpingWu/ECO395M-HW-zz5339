Exercise 2
==========

By Chong Wang, Tianping Wu, Zhenning Zhao

|         | AVG RMSE |
|---------|:--------:|
| model 1 | 66449.78 |
| model 2 | 66240.06 |
| model 3 | 60237.71 |
| model 4 | 60178.42 |
| model 5 | 59470.66 |
| model 6 | 59828.10 |
| model 7 | 60585.05 |

``` r
table1 = summary(lm(price ~ landValue + 
                      lotSize*(bedrooms + bathrooms) + 
                      livingArea*(fuel+ heating + centralAir) + 
                      pctCollege*(fireplaces+age) + 
                      rooms, data=data))

kable(table1["coefficients"])
```

<table class="kable_wrapper">
<tbody>
<tr>
<td>
|                                   |       Estimate|    Std. Error|     t value|  Pr(&gt;|t|)|
|-----------------------------------|--------------:|-------------:|-----------:|------------:|
| (Intercept)                       |  -8.643001e+03|  1.770303e+04|  -0.4882215|    0.6254558|
| landValue                         |   8.332313e-01|  4.815750e-02|  17.3022099|    0.0000000|
| lotSize                           |   8.886326e+03|  8.083021e+03|   1.0993817|    0.2717569|
| bedrooms                          |  -9.010594e+03|  3.051553e+03|  -2.9527897|    0.0031923|
| bathrooms                         |   2.423306e+04|  3.872891e+03|   6.2571003|    0.0000000|
| livingArea                        |   9.013328e+01|  5.689994e+00|  15.8406634|    0.0000000|
| fuelelectric                      |  -4.945208e+04|  4.874015e+04|  -1.0146066|    0.3104374|
| fueloil                           |   3.908867e+04|  1.311235e+04|   2.9810578|    0.0029133|
| heatinghot water/steam            |   1.277797e+04|  1.276971e+04|   1.0006468|    0.3171397|
| heatingelectric                   |   4.673921e+04|  4.935837e+04|   0.9469359|    0.3438057|
| centralAirNo                      |   3.461381e+04|  1.046454e+04|   3.3077241|    0.0009602|
| pctCollege                        |   1.982960e+01|  2.603112e+02|   0.0761765|    0.9392876|
| fireplaces                        |   4.139041e+04|  1.479376e+04|   2.7978287|    0.0052026|
| age                               |  -5.979931e+02|  2.613114e+02|  -2.2884313|    0.0222343|
| rooms                             |   2.539648e+03|  9.776609e+02|   2.5976782|    0.0094665|
| lotSize:bedrooms                  |   1.639476e+03|  2.742749e+03|   0.5977493|    0.5500866|
| lotSize:bathrooms                 |  -3.076214e+03|  3.420065e+03|  -0.8994609|    0.3685343|
| livingArea:fuelelectric           |   2.420885e+01|  2.803848e+01|   0.8634150|    0.3880308|
| livingArea:fueloil                |  -2.464235e+01|  7.454578e+00|  -3.3056672|    0.0009672|
| livingArea:heatinghot water/steam |  -1.068582e+01|  6.773995e+00|  -1.5774770|    0.1148714|
| livingArea:heatingelectric        |  -2.824654e+01|  2.859791e+01|  -0.9877132|    0.3234334|
| livingArea:centralAirNo           |  -2.527276e+01|  5.479314e+00|  -4.6123959|    0.0000043|
| pctCollege:fireplaces             |  -7.022711e+02|  2.601372e+02|  -2.6996180|    0.0070106|
| pctCollege:age                    |   1.042842e+01|  4.879803e+00|   2.1370580|    0.0327353|

</td>
</tr>
</tbody>
</table>