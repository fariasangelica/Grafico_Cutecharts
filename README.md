# Grafico_Cutecharts
Gráfico criado no Python com as bibliotecas cutecharts e pandas.

Os dados são fictícios de consumo de café, onde os recursos são dias, esta semana e semana passada. O gáfico tem o consumo de café da última semana.
## Importar bibliotecas
import pandas as pd

import cutecharts.charts as ctc
## Andamento do código
data = {'Day': ['Mon', 'Tue', 'Wed', 'Thu', 'Fri', 'Sat', 'Sun'],
       'This week': [12, 10, 9, 9, 10, 3, 3],
       'Last week': [15, 12, 8, 9, 11, 4, 3]
       }
 df_coffee = pd.DataFrame(data, columns = ['Day', 'This week', 'Last week'])
       
chart = cc.Radar(' Cup od coffee consumed per day')
chart.set_options(
labels=list(df_coffee['Day']),
is_show_legends=True,
legends_pos='upRight'
 )
chart.add_series('This Week', list(df_coffee['This week']))
chart.add_series('Last Week', list(df_coffee[df_coffee['Last week']))
chart.render_noebook()

![image](https://user-images.githubusercontent.com/98922466/165405046-c0674f6d-3e77-49f7-af0a-d1694a786bd2.png)

