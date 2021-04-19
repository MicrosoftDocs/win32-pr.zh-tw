---
title: album.csv
description: album.csv
ms.assetid: 7308e849-7227-480e-937a-8e9091bdec98
keywords:
- Windows Media Player 線上商店，album.csv
- 線上商店、album.csv
- 輸入1個線上商店，album.csv
- album.csv
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: b8f8b71dc080e6983817d4e6f146249875887ed9
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 09/16/2019
ms.locfileid: "106968025"
---
# <a name="albumcsv"></a>album.csv

此檔案包含目錄中所包含之每個專輯的專案。 每個專案都是由下表所述定位字元分隔欄位所組成的資料列。 欄位必須依列出的順序出現。

album.csv 中的所有欄位都是必要的。

下表中的 Format 資料行描述每個 Unicode 文字欄位的格式化方式。 它不會參考內容的資料類型。 例如，如果 [格式] 資料行中指出了整數，則表示該欄位包含表示整數值的 Unicode 字串，而不是實際的整數。



| 欄位             | 格式                                                                   | 描述                                                                                                                                                                                                                                          |
|-------------------|--------------------------------------------------------------------------|------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| AlbumID           | 非負整數。範例：789456<br/>                          | 專輯的識別碼，在 album.csv 中是唯一的。 必須小於 2 ^ 32。                                                                                                                                                                           |
| AlbumName         | Unicode 字串。範例：最大點擊率<br/>                         | 專輯標題                                                                                                                                                                                                                                          |
| AlbumArtist       | 非負整數。範例：34331<br/>                           | 演出者的 ArtistID。 只允許一個值。 可以是「各種演出者」或類似的識別碼。                                                                                                                                                    |
| AlbumLabel        | Unicode 字串。 應為空白。                                         | 未在此版本中使用。 應為空白。                                                                                                                                                                                                           |
| ReleaseDate       | Unicode 字串，格式為 YYYY-MM-DD。範例：2005-0-0<br/>        | 發行日期。 天或月允許值0。                                                                                                                                                                                               |
| AlbumPrice        | Unicode stringExample： $12.49<br/>                                 | 專輯價格。 應包含貨幣符號。 空字串0和-具有特殊意義。 空字串表示未知的價格。 ' 0 ' 表示曲目是免費的。 連字號 ( '-' ) 表示無法購買專輯。 |
| LinkedGenreID     | 非負整數。範例：12<br/>                              | 專輯之主要類型的識別碼。 只允許一個值。                                                                                                                                                                                        |
| LinkedSubGenreIDs | 格式： n; n; n;範例： 32; 44; 663;<br/>                             | 相關聯 subgenre 識別碼的清單。 清單結尾允許使用尾端分號。                                                                                                                                                             |
| 熱門程度        | 可以是非負整數或十進位值。範例：1256.24<br/> | 由服務決定的熱門等級。 可以是此專輯在依熱門程度排序的專輯清單中的排名。 允許0。                                                                                                              |
| IsRecentlyAdded   | 布林值。 可以是0或1。                                                  | 旗標，表示最近新增的專輯，由服務決定。                                                                                                                                                                    |
| IsFeatured        | 布林值。 可以是0或1。                                                  | 表示這是精選專輯的旗標。                                                                                                                                                                                                      |
| EditorialGlyph    | 非負整數。 應為0。                                       | 未使用的是 release。 應為0。                                                                                                                                                                                                                    |
| FeedsAreAvailable | 布林值。 可以是0或1。                                                  | 未在此版本中使用。 應為0。                                                                                                                                                                                                               |



 

 

 





