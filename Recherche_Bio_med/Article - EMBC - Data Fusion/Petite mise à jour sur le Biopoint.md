#### Condensateur entre l'ECG et l'EMG
Il y a une électrode commune entre l'ECG et l'EMG. Je crois qu'elle a été retiré.

#### Chemin basse impédance entre les électrodes BIO-Z
L'accumulation de sueur entre les électrodes utilisées pour la mesure de la BIO-Z créerait un chemin de faible impédance entre celle-ci ce qui serait grandement nuisible. C'est ce qui pourrait expliquer la bonne lecture lorsque la peau est sèche et le dérive par la suite !

#### Atténuation causé par le filtre Low-Pass du DAC
Le filtre LOW-PASS de troisième ordre suivant le DAC a été retiré pour une certaine raison. Probablement qu'il atténuait trop le signal, mais je trouve cela très étrange. 

#### 1 Meg -> 100k pour le gain de transimpedance

#### Amélioration de l'algo de détection d'enveloppe "software"

#### Bio amplificateur
On tombe dans la région d'instabilité pour les fréquences au-delà de 40 kHz (40 est correct). 80 kHz semble excéder ce qui est possible d'utiliser. Donc on a une certaine limitation pour la fréquence injectée.

#### Stack vs Heap.

Pour l'IMU, un algorithme de sensor fusion est utilisé. C'est en fait un librairie fournie qui est employé. Gab G-T pense que la librairie fait trop d'allocation dynamique et que ça dépasse l'espace allouée à Heap et que ça se retrouve donc dans la stack ce qui "briserait" le device. 
