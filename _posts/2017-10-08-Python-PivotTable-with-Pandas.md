---
layout: post
title:  "Python : Pivot table with Pandas"
date:   2017-10-08 23:50:00
categories: Python
---


passenger_class_fares = titanic_survival.pivot_table(index="pclass", values="fare", aggfunc=numpy.mean)

passenger_survival = titanic_survival.pivot_table(index="pclass", values="survived") 

passenger_age = titanic_survival.pivot_table(index="pclass", values="age")

print(passenger_class_fares)
print(passenger_survival)
print(passenger_age)

import numpy as np

port_stats = titanic_survival.pivot_table(index="embarked", values=["fare","survived"], aggfunc=numpy.sum)

print(port_stats) 






Drop all rows in `titanic_survival` where the columns `age` or `sex` have missing values

{% highlight ruby %}

new_titanic_survival = titanic_survival.dropna(axis=0,subset=["age", "sex"])

{% endhighlight %}