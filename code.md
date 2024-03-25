---
layout: page
title: Code
tagline: Relevant code-snips
permalink: /code.html
ref: code
order: 2
---

{% highlight ruby %}
import pandas as pd
from matplotlib import pyplot as plt
import seaborn as sns
import numpy as np
{% endhighlight %}

{% highlight ruby %}
df = pd.read_csv('data/sf_data.csv')
steal_crimes = ['STOLEN PROPERTY', 'ROBBERY', 'BURGLARY', 'VEHICLE THEFT', 'LARCENY/THEFT']
df = df.loc[df['Category'].isin(steal_crimes)]
df['Date'] = pd.to_datetime(df['Date'])
df = df[df['Date'].dt.year < 2018]
{% endhighlight %}

[Go to the Home Page]({{ '/' | absolute_url }})
