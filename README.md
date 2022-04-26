# Grafico_Cutecharts
Gráfico cirado no Python com a biblioteca cutecharts e pandas.
## Importar bibliotecas
import pandas as pd
import cutecharts.charts as ctc
## Andamento de código
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
