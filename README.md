# RTKBase
From c. 2011 I began creating solutions for survey and hydrography. 
This repo is a rewrite from 2023, with a spec for the simplest RTK Base configuration I can envisage.
It uses str2str from RTKLIB and Linux shell scripts.
It is intended for use with a Raspberry Pi, either at a remote site by a surveyed-in base, or at a fixed, permanent site.

1. [Parts list](RPiBase/parts.md)
2. [Build instructions](RPiBase/build.md)
3. [GNSS configuration](RPiBase/gnss_configuration.md)
4. [Survey the antenna location](AntennaSurvey/Survey.md)
5. [Using SNIP](AntennaSurvey/Snip.md)

# Results
## 02MAY21 2000 with L1/L2 antenna using corrections from CORS Malin as

+55.1668509200°
-7.4351960980°
168.908

X 3620757.028  
Y -472516.118  
Z 5212154.001


## 10JUL23 1800 with L1/L2 antenna using corrections from CORS Malin as

+55.16685117
-7.43519619
168.8739203

## 10JUL23 1800 with L1/L2 antenna using corrections from CORS Foyle as

+55.16685079
-7.435195974
168.9064907


