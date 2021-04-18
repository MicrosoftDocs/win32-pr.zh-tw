---
description: ORDER IN GROUP 子句會搭配 GROUP ON 語句使用，後者會傳回群組中的結果集。
ms.assetid: edfa2037-3360-411d-8a12-cdb9680222f2
title: ORDER IN GROUP 子句
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: d3b4a3a39ffeb2704a099389a6668a075fb4a24f
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/07/2021
ms.locfileid: "104318156"
---
# <a name="order-in-group-clause"></a>ORDER IN GROUP 子句

ORDER IN GROUP 子句會搭配 [GROUP ON](-search-sql-group-on-over.md) 語句使用，後者會傳回群組中的結果集。 ORDER IN GROUP 子句可讓您以不同的方式排序每個傳回的群組。 例如，如果您以 system.string 分組，則可以 System.Doc>ument 來排序所有檔。LastAuthor，AlbumArtist 的所有音樂檔案，以及所有的電子郵件 FromName。

## <a name="syntax"></a>Syntax

以下是 GROUP 子句中 ORDER IN 的語法：


```
GROUP ON <group column and optional ranges>
OVER (SELECT ... FROM SystemIndex
    ORDER 
        IN GROUP '<group name>' BY <column> [<direction>] [,<column> [<direction>]]
        [IN GROUP '<group name>' BY <column> [<direction>] [,<column> [<direction>]] ]
        [BY <column> [<direction>] [,<column> [<direction>]] ])
```



組名規範是群組資料行中的範圍或已知值（如 GROUP ON 語句中所指定）。 例如，ISOSpeed 的已知值會包含 ' ISO-100 '、' ISO-200 ' 等等。 DateTaken 的範圍會包含 ' 2006-1-1 ' 和 ' 2007-1-1 ' 的語句，例如 ItemDate \[ ' 2006-1-1 '、' 2007-1-1 ' 上的群組 \] 。

資料行規范必須是在群組 ON 或 SELECT 語句中指定的有效資料行。 您可以包含一個以上的資料行，並以逗號分隔。 例如，如果您將 ISOSpeed 群組在一起，您可以先 ShutterSpeed 所有的 ISO-100 相片，然後再按 []，然後再按 []。

選擇性的方向規範可以是 ASC 的遞增 (低至高) 或 DESC （遞減 (高至低) ）。 如果您未提供方向規範，則會使用預設值 [遞增]。 如果您指定一個以上的資料行，但未指定所有方向，則您指定的最後一個方向會套用至每個連續的資料行，直到您明確變更方向為止。

未在 ORDER 群組 IN 子句中明確指定的範圍或值，會依 [群組依據] 資料行中的值，以遞增順序排序。

## <a name="examples"></a>範例

下列範例會依 System.object 屬性將結果分組。 此查詢會依應用程式名稱和「音樂」群組依專輯標題和曲目編號來排序「程式」群組。 **Null** 群組將依專案名稱排序。 所有其他群組會依專案日期排序。


```
GROUP ON System.Kind 
OVER (SELECT System.ItemUrl, System.Music.AlbumTitle, System.Music.TrackNumber, System.ItemName, System.ItemDate, System.Kind FROM SystemIndex
    ORDER 
        IN GROUP 'program' BY System.ApplicationName ASC
        IN GROUP 'music' BY System.Music.AlbumTitle ASC, System.Music.TrackNumber ASC
        IN GROUP NULL BY System.ItemName
        BY System.ItemDate DESC)
```



下列範例會依 ItemDate 屬性將結果分組，然後依專案 URL、種類或名稱來排序每個群組。


```
GROUP ON System.ItemDate ['2006-1-1', '2007-1-1', '2008-1-1'] 
OVER (SELECT System.ItemUrl, System.ItemName, System.ItemDate System.Kind FROM SystemIndex
    ORDER 
        IN GROUP MINVALUE BY System.ItemUrl ASC
        IN GROUP '2007-1-1' BY System.Kind
        IN GROUP NULL BY System.ItemName)
```



上述查詢的結果會以五個群組傳回，並依下表所述進行排序。



| 群組    | 描述                                               | 排序依據                                    |
|----------|-----------------------------------------------------------|----------------------------------------------|
| MINVALUE | 日期早于2006-1-1 的專案                          | 依專案的 URL 排序（以遞增順序） |
| 2006-1-1 | 日期等於或晚于2006-1-1 但在2007-1-1 之前的專案 | 依專案日期以遞增順序排序      |
| 2007-1-1 | 日期等於或晚于2007-1-1 但在2008-1-1 之前的專案 | 依種類值以遞增順序排序     |
| 2008-1-1 | 日期等於或晚于2008-1-1 的專案                     | 依專案日期以遞增順序排序      |
| **NULL** | ItemDate 資料行中沒有值的專案         | 依專案名稱以遞增順序排序      |



 

## <a name="related-topics"></a>相關主題

<dl> <dt>

**參考**
</dt> <dt>

[分組依據 .。。OVER .。。聲明](-search-sql-group-on-over.md)
</dt> <dt>

[ORDER BY 子句](-search-sql-orderby.md)
</dt> </dl>

 

 



