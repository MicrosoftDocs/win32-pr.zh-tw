---
description: 群組開啟 .。。
ms.assetid: 37f027c1-c2af-4d62-8b5f-918499fc2d7c
title: 分組依據 .。。OVER .。。聲明
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: df21bb53babd25ae3e407032c6cf9d3774323e85
ms.sourcegitcommit: 61a4c522182aa1cacbf5669683d9570a3bf043b2
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/26/2021
ms.locfileid: "122882019"
---
# <a name="group-on--over--statement"></a>分組依據 .。。OVER .。。聲明

群組開啟 .。。OVER .。。語句會傳回階層式資料列集，其中會根據指定的資料行和選擇性的群組範圍，將搜尋結果劃分成群組。 如果您 [將 [system.string] 資料行群組](../properties/props-system-kind.md) 在一起，則結果集會分成多個群組：一個用於檔、一個用於通訊等等。 如果您群組的是 [ [系統大小](../properties/props-system-size.md) ] 和 [群組範圍 100 KB]，結果集會分為三個群組：大小 < 100 KB 的專案、大小 >= 100 KB 的專案，以及沒有大小值的專案。 您也可以使用函數來匯總群組。

本主題涵蓋下列主題：

-   [語法](#syntax)
-   [群組範圍](#group-ranges)
-   [標記群組](#labeling-groups)
-   [排序群組](#ordering-groups)
-   [嵌套群組](#nesting-groups)
-   [向量屬性上的分組](#grouping-on-vector-properties)
-   [更多範例](#more-examples)
-   [相關主題](#related-topics)

## <a name="syntax"></a>Syntax

群組開啟 .。。OVER .。。語句具有下列語法：


```
GROUP ON <column> ['['<group ranges>']']] 
[AGGREGATE <aggregate_function>] 
[ORDER BY <column> [<direction>]] | [ORDER IN GROUP '<group name>' BY <column> [<direction>]]
    OVER (GROUP ON... | SELECT... ] )
```



群組範圍定義如下：


```
<group ranges> := <range limit> [/'<label>'] | <range limit> [/'<label>'], <group ranges>
<range limit> := (<number> | <date> | '<string>' | BEFORE('<string>') | AFTER('<string>')) 
```



[群組依據] 資料 &lt; 行 &gt; 可以是屬性存放區中屬性的一般或分隔 [識別碼](-search-sql-identifiers.md) 。

選擇性 <group ranges> 是一個或多個值的清單， (數位、日期或字串) 用來將結果分割成群組。 會 <range limit> 識別所傳回結果集中的除法點，並 <label> 識別群組的使用者易記標籤。 您可以將結果集分成多個所需的群組。

第一個結果群組包含的專案具有指定屬性的最小可能值，但不包括第一個範圍限制。 您可以使用 MINVALUE 關鍵字來參考這個群組。 第二個群組可以參考範圍限制規範本身，並且包含其值為指定屬性等於或大於範圍限制的專案。 最後會傳回任何沒有指定屬性值的專案，而且可以使用 **Null** 關鍵字來參考這些專案。

例如， [DateCreated](../properties/props-system-datecreated.md) 屬性 ' 2006-01-01 ' 的範圍限制會將結果集分割為 2006-01-01 (MINVALUE group) 、日期等於或晚于 2006-01-01 (2006-01-01 group) 的專案，以及沒有日期 (**Null** 群組) 的專案。

在每個群組內，依預設會依 [群組依據] 資料行中的值來排序結果。 選擇性的 [ORDER BY](-search-sql-orderby.md) 子句可以包含 ASC 的方向規範，以遞增 (低至高) 或 DESC (高至低) ，而且 [GROUP BY 子句中的順序](-search-sql-orderingroup.md) 可以使用不同的規則排序每個群組。 如需詳細資訊，請參閱下方的 [訂購群組](#ordering-groups) 一節。

## <a name="group-ranges"></a>群組範圍

下表將示範如何根據範圍限制將結果分成群組：



|  (資料 &lt; 行 &gt; \[ 群組範圍的範例 \])         | 結果                                                                                                                                                                                                                                                                         |
|--------------------------------------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| System. Size \[ 1000、5000\]                       | 結果會分成四個 bucket： **MINVALUE**： Size < 1000<br/> **1000：** 1000 <= Size < 5000<br/> **5000：** 大小 >= 5000<br/> **Null：** 沒有大小的值<br/>                                                                      |
| System. Author \[ ( ' ) ，在 ( ' r ' ) \]         | 結果會分成四個值區： **MINVALUE：** Author "m" 之前 < 字元<br/> **m：** "m" 之前的字元 <= "r" 之後的作者 < 字元<br/> **r：** "r" 之後的字元 <= Author<br/> **Null：** 沒有作者的值<br/>      |
| System. Author \[ MINVALUE/' a to l '，"m"/m 至 z '\] | 結果會分成三個值區： **a 到 l：** Author < "m"<br/> **m 至 z：** "m" <= Author <br/> **Null：** 沒有作者的值<br/>                                                                                                               |
| System. DateCreated \[ ' 2005-1-01 '，' 2006-6-01 '\]   | 結果會分成四個 bucket：<br/> **MINVALUE：** DateCreated < 2005-1-01<br/> **2005-1-01：** 2005-1-01 <= DateCreated < 2006-6-01<br/> **2006-1-01：** DateCreated >= 2006-6-01<br/> **Null：** DateCreated 沒有任何值<br/> |



 

 

> [!IMPORTANT]
>
> 錯誤： `GROUP ON System.Author['m','z','a']`
>
> 正確： `GROUP ON System.Author['a','m','z']`

 

 

## <a name="labeling-groups"></a>標記群組

若要改善可讀性，您可以使用下列語法來標記群組：


```
GROUP ON <column> [<range limit>/'<label>',<range limit>/'<label>']
```



標籤會與範圍限制分隔，並以斜線標示，並以單引號括住。 如果您未指定標籤，組名就是範圍限制字串。

以下是標籤群組的範例：


```
GROUP ON System.Size [(MINVALUE/'Small','100')/'Medium','50000'/'Large']
    OVER (SELECT System.Size FROM SystemIndex)
```



在 Windows 7 或更新版本中，您也可以使用一般的 \[ 其他 \] 標籤來合併多個群組範圍。 所有使用此標籤識別的群組所產生的結果，將會合並成一個具有此標籤的群組。 此結果群組會在所有其他群組之後傳回，但 **Null** 群組除外。 **Null** 群組包含沒有指定屬性值之專案的結果。 在 Windows 7 之前， \[ 其他 \] 標籤的處理方式就像任何其他群組標籤一樣。

下列程式碼是使用 \[ \] Windows 7 或更新版本中建立之群組的其他標籤的範例：


```
GROUP ON System.Author ['0', 'A'/'[OTHER]', 'I', 'Q', 'W'/'[OTHER]', 'Y']
    OVER (SELECT System.DateCreated FROM SystemIndex)
```



下表顯示在 Windows 7 或更新版本中，先前分組程式碼所建立的群組。



| Group     | System.Author | System.string |
|-----------|---------------|-----------------|
| 0         | 1Bill         | Lorem.docx      |
| Q         | 女王         | Ipsum.docx      |
|           | Robin         | dolor.docx      |
| Y         | Zara          | amet.docx       |
| \[其他\] | Abner         | nonummy.docx    |
|           | Bob           | laoreet.docx    |
|           | Xaria         | magna.docx      |
| **NULL**  |               | aliquam.docx    |



 

## <a name="ordering-groups"></a>排序群組

有三種方式可排序群組中的專案：

-   預設排序：如果未指定，則會依 [群組依據] 資料行中的值，以遞增順序來排序結果。
-   ORDER BY：您可以在 ORDER BY 子句中指定遞減順序。 您必須依 [群組依據] 資料行來排序結果。
-   ORDER IN GROUP BY：您可以為每個群組指定不同的順序。 如果您在 [[系統](../properties/props-system-kind.md)] 上分組，您可以依 [系統]、[[作者](../properties/props-system-author.md)] 和 [音樂] 將檔[排序。](../properties/props-system-music-artist.md)

如需排序結果的詳細資訊，請參閱 [ORDER By 子句](-search-sql-orderby.md) 和 [GROUP 子句參考頁面中的 order IN](-search-sql-orderingroup.md) 。

## <a name="nesting-groups"></a>嵌套群組

您可以使用多個 GROUP ON 子句來嵌套群組。 查詢中指定的順序會直接反映在輸出群組階層中，如下列範例所示。


```
GROUP ON <System.Kind> 
      OVER (GROUP ON <System.Author> 
                  OVER (SELECT <System.DateCreated>))
```





| System.string    | System.Author | System. DateCreated |
|----------------|---------------|--------------------|
| 文件      | 威拉         | 2006-01-02         |
|                |               | 2006-01-05         |
|                | Zara          | 2007-06-02         |
|                |               | 2007-09-10         |
| 通訊 | Abner         | 2006-04-16         |
|                | 珍          | 2007-02-20         |
|                | 威拉         | 2006-10-15         |
|                | Zara          | 2008-01-02         |



 

 

## <a name="grouping-on-vector-properties"></a>向量屬性上的分組

在向量屬性、可以同時包含一或多個值的屬性上進行分組，預設會個別比較向量值。 例如，如果有一份檔，Lorem.docx，並以 system.string 屬性為 "Theresa;Zara "和另一個檔，Ipsum.docx，將 Author 屬性設為" Zara "，查詢會傳回兩個群組中的結果集，如下所示：


```
GROUP ON <System.Author> 
      OVER (SELECT <System.FileName>)
```





| System.Author | System.string |
|---------------|-----------------|
| 德蕾莎       | Lorem.docx      |
| Zara          | Lorem.docx      |
|               | Ipsum.docx      |



 

如您所見，vector 屬性的分組會傳回重複的資料列。 Lorem.docx 會出現兩次，因為它有兩個作者。

 

## <a name="more-examples"></a>更多範例


```
GROUP ON System.Photo.ISOSpeed [0,10,100] 
      OVER (SELECT System.ItemName, System.Size, System.ItemUrl FROM SystemIndex)
            
GROUP ON System.DateCreated['2005/01/01 00:00:00', '2005/12/30 23:00:00'] 
      OVER (SELECT System.ItemName, System.Size, System.ItemUrl FROM SystemIndex)
            
GROUP ON System.Author ORDER BY System.Author DESC 
      OVER (GROUP ON System.DateCreated ORDER BY System.DateCreated ASC 
                  OVER (SELECT System.FileName, System.DateCreated, System.Size FROM SystemIndex 
                        WHERE CONTAINS(*, 'text')))

GROUP ON System.ItemName [before('a'), 'a', before ('c'), 'd', after('d')] 
      OVER (SELECT System.ItemName, System.ItemUrl FROM SystemIndex ORDER BY System.ItemName)                        
                        
GROUP ON System.ItemNameDisplay ['a' / 'col_a','c' / 'col_c'] 
      OVER (SELECT System.ItemNameDisplay FROM SystemIndex 
            ORDER BY System.ItemNameDisplay)

GROUP ON System.Size[1,2] 
      OVER (GROUP ON System.Author['a','f','mc','x'] 
                  OVER (GROUP ON System.DateCreated['2005/07/25 07:00:00', '2005/08/25 07:00:00']
                        ORDER BY System.DateCreated DESC 
                              OVER (SELECT System.FileName FROM SystemIndex 
                                    WHERE CONTAINS('text'))))   
```



## <a name="related-topics"></a>相關主題

<dl> <dt>

[彙總函式](-search-sql-aggregates.md)
</dt> <dt>

[ORDER BY 子句](-search-sql-orderby.md)
</dt> <dt>

[ORDER IN GROUP 子句](-search-sql-orderingroup.md)
</dt> </dl>

 

 
