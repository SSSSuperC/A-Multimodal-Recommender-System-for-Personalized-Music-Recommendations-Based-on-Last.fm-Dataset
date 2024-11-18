---
Topic:
    - 影视娱乐

Field:
    - 推荐系统/广告/搜索

License:
    - CC0 公共领域共享

Ext:
    - .zip

DatasetUsage:
    - 2587204
---

## **背景描述**
这个数据集包含社交网络、标签和音乐艺术家从一组2K个用户中收听的信息。[fm在线音乐系统](http://www.last.fm)
该数据集是在第5届ACM推荐系统会议([RecSys 2011](http://recsys.acm.org/2011 ))，第2届国际推荐系统信息异构与融合研讨会([HetRec 2011]( http://ir.ii.uam.es/hetrec2011))框架下发布的。

## **数据说明**
**数据量**
* 1892 users
* 17632 artists
* 12717双向用户朋友关系，即25434 (user_i, user_j)对
	* 平均每个用户13.443个好友关系
* 92834用户收听艺术家关系，即元组[user, artist, listeningCount]        
	* 平均每位用户最常收听49.067位艺术家的作品
	* 平均每位艺术家有5.265名收听用户
* 11946 tags  
* 186479标签分配(tas)，即元组[用户，标签，艺术家]
	* 平均每个用户98.562个标签分配
	* 平均每位艺术家14.891个标签分配
	* 平均8.764个不同的标签用于每个用户
	* 平均8.764个不同的标签用于每个艺术家

**文件信息**
数据包含5个dat格式的文件：				 
* artists.dat
	* 该文件包含用户收听和标记的音乐艺术家的信息
* tags.dat
	* 这个文件包含数据集中可用的一组标记。
* user_artists.dat
	* 这个文件包含每个用户收听的艺术家。它还为每一对 [user, artist]提供了一个监听计数。
* user_taggedartists.dat - user_taggedartists-timestamps.dat
  * 这些文件包含每个特定用户提供的艺术家的标签分配。它们还包含标签分配完成时的时间戳。
* user_friends.dat
	* 这些文件包含数据库中用户之间的朋友关系。 

**数据格式**
数据格式化为每行一个条目如下(tap分隔，“\t”):
* artists.dat
   `id \t name \t url \t pictureURL`
> 示例:
> 707	Metallica	http://www.last.fm/music/Metallica	http://userserve-ak.last.fm/serve/252/7560709.jpg
* tags.dat
`tagID \t tagValue`
> 示例：
> 1  metal
* user_artists.dat
`userID \t artistID \t weight`
> 示例：      
> 2  51  13883
* user_taggedartists.dat
`userID \t artistID \t tagID \t day \t month \t year`
> 示例：
> 2 	52	13  1	4 	2009  
* user_taggedartists-timestamps.dat
`userID \t artistID \t tagID \t timestamp`
> 示例：
> 2	 52	 13	 1238536800000
* user_friends.dat
`userID \t friendID`
> 示例：
> 2  275
   	

## **数据来源**
数据来自[grouplens](https://grouplens.org/datasets/hetrec-2011/)
使用此数据集时，应引用:

> Last.fm website, http://www.lastfm.com

亦可引用 HetRec'11 workshop 的内容如下:
> @inproceedings{Cantador:RecSys2011,
>       author = {Cantador, Iv\'{a}n and Brusilovsky, Peter and Kuflik, Tsvi},
>       title = {2nd Workshop on Information Heterogeneity and Fusion in Recommender Systems (HetRec 2011)},
>       booktitle = {Proceedings of the 5th ACM conference on Recommender systems},
>       series = {RecSys 2011},
>       year = {2011},
>       location = {Chicago, IL, USA},
>       publisher = {ACM},
>       address = {New York, NY, USA},
>       keywords = {information heterogeneity, information integration, recommender systems},
>    } 


## **问题描述**
该数据可用于推荐系统相关研究

## **引用格式**
```
@misc{music2836,
    title = { Last.fm音乐推荐数据集 },
    author = { Vivian },
    howpublished = { \url{https://www.heywhale.com/mw/dataset/5cfe0526e727f8002c36b9d9} },
    year = { 2019 },
}
```