# hse_hw3_chromhmm

Мною была выбрана клеточная линия A549, так как Loucy, которую я рассматривала в прошлом дз, отсутствовала. 

### Гистоновые метки
Гистоновая метка | Имя файла 
---|---
wgEncodeBroadHistoneA549H2azEtoh02AlnRep2.bam | H2az1.bam
wgEncodeBroadHistoneA549H2azDex100nmAlnRep1.bam | H2az2.bam
wgEncodeBroadHistoneA549H3k04me1Dex100nmAlnRep1.bam | H3k04me1.bam
wgEncodeBroadHistoneA549H3k04me1Etoh02AlnRep1.bam | H3k04me2.bam
wgEncodeBroadHistoneA549H3k04me2Dex100nmAlnRep1.bam | H3k04me3.bam
wgEncodeBroadHistoneA549H3k04me2Etoh02AlnRep1.bam | H3k04me4.bam
wgEncodeBroadHistoneA549H3k04me3Dex100nmAlnRep2.bam | H3k04me5.bam
wgEncodeBroadHistoneA549H3k04me3Etoh02AlnRep1.bam | H3k04me6.bam
wgEncodeBroadHistoneA549H3k09acEtoh02AlnRep2.bam | H3k09ac.bam
wgEncodeBroadHistoneA549H3k09me3Etoh02AlnRep1.bam | H3k09me.bam

Файл [cellmarkfiletable.txt]()

### ChromHMM
[Результаты](https://github.com/ruanmik/hse_hw3_chromhmm/blob/main/img/webpage_10.html) запуска ChromHMM

RefSeqTES neighborhood | RefSeqTSS neighborhood
---|---
![](https://github.com/ruanmik/hse_hw3_chromhmm/blob/main/img/A549_10_RefSeqTES_neighborhood.png) | ![](https://github.com/ruanmik/hse_hw3_chromhmm/blob/main/img/A549_10_RefSeqTSS_neighborhood.png)

A549 overlap | emissions | transitions
---|---|---
![](https://github.com/ruanmik/hse_hw3_chromhmm/blob/main/img/A549_10_overlap.png) | ![](https://github.com/ruanmik/hse_hw3_chromhmm/blob/main/img/emissions_10.png) | ![](https://github.com/ruanmik/hse_hw3_chromhmm/blob/main/img/transitions_10.png)

### Genome Browser

![](https://github.com/ruanmik/hse_hw3_chromhmm/blob/main/img/1.png) ![](https://github.com/ruanmik/hse_hw3_chromhmm/blob/main/img/2.png)

![](https://github.com/ruanmik/hse_hw3_chromhmm/blob/main/img/3.png) ![](https://github.com/ruanmik/hse_hw3_chromhmm/blob/main/img/4.png)

![](https://github.com/ruanmik/hse_hw3_chromhmm/blob/main/img/5.png)


Состояние | Название | Описание
---|---|---
1 | Promoter | Имеет средний сигнал, почти не пересекается с выбранными гистоновыми метками,
2 | Promoter | Cигнал средний, пересекается с большинством гистоновых модификаций
3 | Active Promoter | Сгнал либо высокий, либо его почти нет, попадает в учатки интронов и экзонов. 
4 | Enhancer | Сигнал высокий, встречается во всех гистоновых модификациях
5 | Repressed | Попадает на участок репрессированного гетерохроматима (тк ассоциировано с довольно большим процентом ядерной ламиной судя по рисунку ChromHMM overlap), сигнал сильный, встречается во всех модификациях примерно одинаково. 
6 | Strong enhancer | Состояние встречается стерди 6 гистоновых меток, попадает на интроны обладает высоким сигналом
7 | Weak enhancer | Обладает средним сигналом, встречается у 3 гистоновых меток
8 | Heterochromatin | Попадает на участок репрессированного гетерохроматима (тк ассоциировано с большим процентом ядерной ламиной судя по рисунку ChromHMM overlap), имеет низкий сигнал, почти не пересекается с гистоновыми модификациями. 
9 | Heterochromatin | Чаще всего встречается в геноме, имеет низкий сигнал, почти не пересекается с выбранными гистоновыми метками, попадает на участок репрессированного гетерохроматима (тк ассоциировано с большим процентом ядерной ламиной)
10 | Transcribed | Попадает на участок репрессированного гетерохроматима (тк ассоциировано с большим процентом ядерной ламиной), попадает на участки интронов, имеет низкий сигнал и пересечение с гистоновыми метками с небольшой вероятностью

### Список всех запущенных команд

[Colab](https://colab.research.google.com/drive/1XvI6FHqtYL4c97fP4vCT44esRl-DoqAg?usp=sharing), где выполнялась работа

### Бонус 

![](https://github.com/ruanmik/hse_hw3_chromhmm/blob/main/img/bonus.png)


