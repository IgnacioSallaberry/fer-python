# -*- coding: utf-8 -*-
"""
Created on Fri Jan 24 15:51:39 2020

@author: LEC
"""

import numpy as np
import re
import matplotlib.pyplot as plt

plt.close()

with open('C:\\Users\\LEC\\Desktop\\fer.txt') as fobj:
    DATA= fobj.read()
fer = re.split('\t|\n', DATA)
nombres = []
i=1
while i<8:
    nombres.append(fer[i])
    i+=1
del fer[0:9]
i=7
q=1
while q<7:
    del fer[i*q]
    
    q+=1

valores=[]
i=0
fer.remove('')
while i < len(fer):
    valores.append(np.float(fer[i]))
    print(valores[i])
    i+=1    
    

datos = np.asarray(valores)
datos= datos.reshape(7,7)
fig, ax = plt.subplots()
im = ax.imshow(datos, cmap='Oranges_r')
# We want to show all ticks...
ax.set_xticks(np.arange(len(nombres)))
ax.set_yticks(np.arange(len(nombres)))
# ... and label them with the respective list entries
ax.set_xticklabels(nombres)
ax.set_yticklabels(nombres)

# Rotate the tick labels and set their alignment.
plt.setp(ax.get_xticklabels(), rotation=45, ha="right",
         rotation_mode="anchor")

# Loop over data dimensions and create text annotations.
for i in range(len(nombres)):
    for j in range(len(nombres)):
        text = ax.text(j, i, datos[i, j],
                       ha="center", va="center", color="w")

ax.set_title('LA MATRIZ QUE MÁS VAS A QUERER EN EL MUNDO')
fig.tight_layout()
plt.show()
