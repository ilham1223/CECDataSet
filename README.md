# 中選會選舉資料開放資料集

本次資料整理是以中選會開放資料網站上 http://data.cec.gov.tw/votedata.zip
的資料為基礎，經過重新整理並清除錯誤資料後（感謝中選會協助更正）。彙整台灣過去
從 1994 年以來的共 108 次選舉歷史資料，包括了各次選舉的參選人基本資料、各級
地區的選舉人口概況、選舉票數記錄（到各投票所）。

此次資料彙整主要目的在於提供一個較為方便讀取與應用的開放資料集，以供需要的人
自由應用。若有不完備或是缺漏之處也請見諒，並以中選會所正式公佈的資料為主。


## 資料彙整流程

```
                                       elbase.csv -+
                                       elcand.csv  |
中選會 votedata ---> RawData -+->      elpaty.csv  | --->        VoteRecords.csv       ---> ALL_VoteRecords.csv
                              |        elctks.csv -+
                              |
                              +->      elbase.csv -+ --->        VoteRegionProfile.csv ---> ALL_VoteRegionProfile.csv
                              +->      elprof.csv -+

```




## 資料集合包括以下 108 次選舉

* 83年區域直轄市議員選舉(1994)
* 83年區域臺灣省議員選舉(1994)
* 83年原住民直轄市議員選舉(1994)
* 83年山地原住民臺灣省議員選舉(1994)
* 83年平地原住民北區臺灣省議員選舉(1994)
* 83年平地原住民南區臺灣省議員選舉(1994)
* 83年直轄市長選舉(1994)
* 83年臺灣省長選舉(1994)
* 第03屆區域立法委員選舉(1995)
* 第03屆山地原住民立法委員選舉(1995)
* 第03屆平地原住民立法委員選舉(1995)
* 第03屆區域國大代表選舉(1996)
* 第03屆山地原住民國大代表選舉(1996)
* 第03屆平地原住民國大代表選舉(1996)
* 第09任總統（副總統）選舉(1996)
* 86年縣市長選舉(1997)
* 87年區域直轄市議員選舉(1998)
* 87年區域縣市議員選舉(1998)
* 87年原住民直轄市議員選舉(1998)
* 87年山地原住民縣市議員選舉(1998)
* 87年平地原住民縣市議員選舉(1998)
* 87年直轄市長選舉(1998)
* 87年鄉鎮市長選舉(1998)
* 第04屆區域立法委員選舉(1998)
* 第04屆山地原住民立法委員選舉(1998)
* 第04屆平地原住民立法委員選舉(1998)
* 第10任總統（副總統）選舉(2000)
* 90年縣市長選舉(2001)
* 第05屆區域立法委員選舉(2001)
* 第05屆山地原住民立法委員選舉(2001)
* 第05屆平地原住民立法委員選舉(2001)
* 91年區域直轄市議員選舉(2002)
* 91年區域縣市議員選舉(2002)
* 91年原住民直轄市議員選舉(2002)
* 91年山地原住民縣市議員選舉(2002)
* 91年平地原住民縣市議員選舉(2002)
* 91年直轄市長選舉(2002)
* 91年鄉鎮市長選舉(2002)
* 第06屆區域立法委員選舉(2004)
* 第06屆山地原住民立法委員選舉(2004)
* 第06屆平地原住民立法委員選舉(2004)
* 第11任總統（副總統）選舉(2004)
* 94年任務型國大代表選舉(2005)
* 94年區域縣市議員選舉(2005)
* 94年山地原住民縣市議員選舉(2005)
* 94年平地原住民縣市議員選舉(2005)
* 94年縣市長選舉(2005)
* 94年鄉鎮市長選舉(2005)
* 95年區域直轄市議員選舉(2006)
* 95年原住民直轄市議員選舉(2006)
* 95年直轄市長選舉(2006)
* 第07屆區域立法委員選舉(2008)
* 第07屆山地原住民立法委員選舉(2008)
* 第07屆平地原住民立法委員選舉(2008)
* 第12任總統（副總統）選舉(2008)
* 98年區域縣市議員選舉(2009)
* 98年山地原住民縣市議員選舉(2009)
* 98年平地原住民縣市議員選舉(2009)
* 98年縣市長選舉(2009)
* 98年鄉鎮市長選舉(2009)
* 第7屆立委南投縣第1選區補選(2009)
* 第7屆立委臺北市第6選區補選(2009)
* 第7屆立委苗栗縣第1選區補選(2009)
* 第7屆立委雲林縣第2選區補選(2009)
* 99年區域直轄市議員選舉(2010)
* 99年山地原住民直轄市議員選舉(2010)
* 99年平地原住民直轄市議員選舉(2010)
* 99年直轄市里長選舉(2010)
* 99年直轄市長選舉(2010)
* 99年縣市村里長選舉(2010)
* 99年鄉鎮市民代表選舉(2010)
* 第7屆立委嘉義縣第2選區補選(2010)
* 第7屆立委新竹縣補選(2010)
* 第7屆立委桃園縣第2選區補選(2010)
* 第7屆立委桃園縣第3選區補選(2010)
* 103年村里長選舉(2014)
* 第7屆立委臺中縣第3選區補選(2010)
* 第7屆立委臺東縣補選(2010)
* 第7屆立委花蓮縣補選(2010)
* 第7屆立委臺南市第4選區補選(2011)
* 第7屆立委高雄市第4選區補選(2011)
* 第08屆區域立法委員選舉(2012)
* 第08屆山地原住民立法委員選舉(2012)
* 第08屆平地原住民立法委員選舉(2012)
* 第13任總統（副總統）選舉(2012)
* 第8屆立委臺中市第2選區補選(2013)
* 103年區域直轄市市議員選舉(2014)
* 103年區域縣市議員選舉(2014)
* 103年區域鄉鎮市民代表選舉(2014)
* 103年山地原住民直轄市市議員選舉(2014)
* 103年山地原住民縣市議員選舉(2014)
* 103年平地原住民直轄市市議員選舉(2014)
* 103年平地原住民縣市議員選舉(2014)
* 103年平地原住民鄉鎮市民代表選舉(2014)
* 103年直轄市區民代表選舉(2014)
* 103年直轄市區長選舉(2014)
* 103年直轄市長選舉(2014)
* 103年縣市長選舉(2014)
* 103年鄉鎮市長選舉(2014)
* 第8屆立委南投縣第2選區缺額補選(2015)
* 第8屆立法委員屏東縣第3選舉區缺額補選(2015)
* 第8屆立法委員彰化縣第4選舉區缺額補選(2015)
* 第8屆立法委員臺中市第6選舉區缺額補選(2015)
* 第8屆立法委員苗栗縣第2選舉區缺額補選(2015)
* 第09屆區域立法委員選舉(2016)
* 第09屆山地原住民立法委員選舉(2016)
* 第09屆平地原住民立法委員選舉(2016)
* 第14任總統（副總統）選舉(2016)


# 資料整合聲明

國立高雄大學資訊管理學系
2016.07