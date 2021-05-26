# SI_lab2_193057
Втора лабораториска вежба по Софтверско инженерство
## Control Flow Graph

![SI_CFG](https://user-images.githubusercontent.com/75999222/119683037-a4172a80-be43-11eb-91b9-3c6e09631ab5.png)

https://github.com/bojchevd/SI_lab2_193057/issues/1#issue-902520233

## Цикломатска комплексност
Цикломатската комплекност на кодот е 8. Се добива по формулата E-V+2, каде што Е е бројот на рабови и V е бројот на јазли.

## Test cases според критериумот Multiple Condiitons

- if(hr<0 || hr>24)
  - hr < 0 || anything **hr=-1 min=10 sec=10**
  - hr > 0 && hr>24 **hr=25 min=10 sec=10**
  - hr>0 && hr <24 **hr=10 min=10 sec=10**
- if(min<0 || min>59)
  - min < 0 || anything **hr=10 min =-5 sec=10**
  - min > 59 **hr=10 min=60 sec=10**
  - min>0 && min<59 **hr=10 min=25 sec=25**
- if(sec>=0 && sec<=59)
  - sec>=0 && sec<=59 **hr=10 min=10 sec=10)**
  - sec>=59 **hr=10 min=10 sec=60)**
  - sec<=0 || anything **hr=10 min=10 sec=-5)**
- else if(hr==24 && min==0 && sec==0)
  - hr==24 && min==0 && sec==0 **hr=24 min=0 sec=0**
  - hr==24 && min!=0 || anything **hr=24 min=24 sec=24**
  - hr==24 && min==0 && sec!=0 **hr=24 min=0 sec=24**
  - hr!=24 || anything **hr=5 min=24 sec=24** // ne moze da se sluci ovoj test case
  
