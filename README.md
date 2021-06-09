# hse21_H3K9ac_ZDNA_human

## Сохраненная сессия в UCSC GenomeBrowser: 
http://genome.ucsc.edu/s/egbaydarov1/hse21_H3K4me3_ZDNA_human

![alt text](https://github.com/egbaydarov/hse21_H3K9ac_ZDNA_human/raw/main/images/ucsc_screenshot.png)


## Гистограммы длин участков для каждого эксперимента до и после конвертации к нужной версии генома
<img src="https://github.com/egbaydarov/hse21_H3K9ac_ZDNA_human/raw/main/images/len_hist.H3K9ac_H1.ENCFF584EB0.hg19.jpg" width="450"><img src="https://github.com/egbaydarov/hse21_H3K9ac_ZDNA_human/raw/main/images/len_hist.H3K9ac_H1.ENCFF584EB0.hg38.jpg" width="450"><img src="https://github.com/egbaydarov/hse21_H3K9ac_ZDNA_human/raw/main/images/len_hist.H3K9ac_H1.ENCFF754YLR.hg19.jpg" width="450"><img src="https://github.com/egbaydarov/hse21_H3K9ac_ZDNA_human/raw/main/images/len_hist.H3K9ac_H1.ENCFF754YLR.hg38.jpg" width="450">

## Гистограммы распределения длин пиков после фильтрации
<img src="https://github.com/egbaydarov/hse21_H3K9ac_ZDNA_human/raw/main/images/filter_peaks.H3K9ac_H1.ENCFF584EB0.hg19.init.hist.jpg" width="450"><img src="https://github.com/egbaydarov/hse21_H3K9ac_ZDNA_human/raw/main/images/filter_peaks.H3K9ac_H1.ENCFF584EB0.hg19.filtered.hist.jpg" width="450"><img src="https://github.com/egbaydarov/hse21_H3K9ac_ZDNA_human/raw/main/images/filter_peaks.H3K9ac_H1.ENCFF754YLR.hg19.init.hist.jpg" width="450"><img src="https://github.com/egbaydarov/hse21_H3K9ac_ZDNA_human/raw/main/images/filter_peaks.H3K9ac_H1.ENCFF754YLR.hg19.filtered.hist.jpg" width="450">

## Расположение пиков гистоновой метки относительно аннотированных генов
![alt text](https://github.com/egbaydarov/hse21_H3K9ac_ZDNA_human/raw/main/images/chip_seeker.H3K9ac_H1.ENCFF754YLR.hg19.filtered.plotAnnoPie.png)
![alt text](https://github.com/egbaydarov/hse21_H3K9ac_ZDNA_human/raw/main/images/chip_seeker.H3K9ac_H1.ENCFF584EB0.hg19.filtered.plotAnnoPie.png)

## Гистограмма стр-ры ДНК
![alt text](https://github.com/egbaydarov/hse21_H3K9ac_ZDNA_human/raw/main/images/len_hist.DeepZ.jpg)

## Расположение участков стр-ры ДНК относительно аннотированных генов
![alt text](https://github.com/egbaydarov/hse21_H3K9ac_ZDNA_human/raw/main/images/chip_seeker.DeepZ.plotAnnoPie.png)

## Расположение пересечения гистоновой метки и участков стр-ры ДНК
![alt text](https://github.com/egbaydarov/hse21_H3K9ac_ZDNA_human/raw/main/images/chip_seeker.H3K9ac_H1.intersect_with_DeepZ.plotAnnoPie.png)

## Результаты Ассоциирование полученных пересечений с ближайшими генами

```Кол-во пиков, которые удалось проассоциировать с генами - 8942```

```Общее кол-во уникальных генов - 5826```

## Результат GO-анализа

### top-10 lowest FDR

```cellular metabolic process (GO:0044237)```

```nitrogen compound metabolic process (GO:0006807)```

```primary metabolic process (GO:0044238)```

```metabolic process (GO:0008152)```

```macromolecule metabolic process (GO:0043170)```

```organic substance metabolic process (GO:0071704)```

```cellular macromolecule metabolic process (GO:0044260)```

```cellular nitrogen compound metabolic process (GO:0034641)```

```nucleic acid metabolic process (GO:0090304)```


## Команды

для конвертации hg38 => hg19:

```wget https://hgdownload.cse.ucsc.edu/goldenpath/hg38/liftOver/hg38ToHg19.over.chain.gz```

```liftOver   H3K4me3_A549.ENCFF832EOL.hg38.bed   hg38ToHg19.over.chain.gz   H3K4me3_A549.ENCFF832EOL.hg19.bed   H3K4me3_A549.ENCFF832EOL.unmapped.bed```

Объединяем два набора отфильтрованных ChIP-seq пиков

```cat  *.filtered.bed  |   sort -k1,1 -k2,2n   |   bedtools merge   >  H3K4me3_A549.merge.hg19.bed ```
