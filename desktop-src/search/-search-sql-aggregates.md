---
description: 彙總函式會對一組值執行計算，並傳回值。 這麼做可讓您產生多層級群組的摘要統計資料，而不會產生太多負荷。
ms.assetid: 82a93f57-8273-45bf-81d7-50a673845ae1
title: 彙總函式
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: da68ad1104c93e8ae04f7ec37cbbde5020109336
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/07/2021
ms.locfileid: "104563534"
---
# <a name="aggregate-functions"></a>彙總函式

彙總函式會對一組值執行計算，並傳回值。 這麼做可讓您產生多層級群組的摘要統計資料，而不會產生太多負荷。

## <a name="about-aggregate-functions"></a>關於彙總函式

Windows Search 結構化查詢語言 (SQL)  (SQL) 中的彙總函式具有下列語法：


```
AGGREGATE <function> [AS <label>] [,<function> [AS <label>]]*
```



函數部分可以包含下列任何函數和語法：



| 函式                                                              | 描述                                                                                                                                                                                                 |
|-----------------------------------------------------------------------|-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| 平均 (<column>)                                                    | 傳回群組中的值的平均值。 只適用于數位。                                                                                                                                      |
| BYFREQUENCY (<column> ， <N>)                                 | 從群組中的結果傳回最常出現的 N 個數據行值。 也包含每個值發生次數的計數，以及包含每個傳回值之結果的檔識別碼。 |
| CHILDCOUNT ()                                                           | 傳回群組中的專案數 (排除子群組) 。 如果有多個群組層級，這會傳回直屬子群組的數目。                                                  |
| 計數 ()                                                                | 傳回群組和所有子群組中的專案數。                                                                                                                                                   |
| DATERANGE (<column>)                                              | 傳回在群組結果群組中找到之資料行值的下限和上限。 只有 filetime 屬性才有效。                                                                               |
| 第一個 (<column> ， <N>)                                       | 從群組中找到的分葉結果傳回前 N 個數據行值。                                                                                                                                       |
| 最大 (<column>)                                                    | 傳回運算式中的最大值。 只適用于數位或日期。                                                                                                                              |
| 最小 (<column>)                                                    | 傳回運算式中的最小值。 只適用于數位或日期。                                                                                                                              |
| REPRESENTATIVEOF (<column> 、 <idRepresentative> <N>)  | 傳回 N 個 idRepresentative 值，每個值都是從具有唯一資料行值的其中一個結果子集選取。 每個值也會以具有 idRepresentative 值的檔識別碼傳回。 |
| SUM (<column>)                                                    | 傳回群組中值的總和。 只適用于數位。                                                                                                                                          |



 

 

> [!Note]  
> 匯總會以個別資料行傳回。 它們大多是簡單類型，除了 ByFrequency、First、DateRange 和 RepresentativeOf，會以複合類型傳回。

 

您可以針對匯總使用任何數值或日期資料行，而不只是 SELECT 子句中的資料行。 不過，您無法將匯總分組。 如果傳入的資料行引數不是數值或日期類型，就會傳回語法錯誤。

標籤部分是選擇性的，並為標籤提供更容易讀取的別名。 如果您未包含別名標籤，則 Windows Search 會將函式和資料行名稱轉換成標籤。 例如，MAX (System.Doc>ument。WordCount) 會變成 MAX \_ SystemDocumentWordCount。

## <a name="multi-level-groups-and-counting"></a>多層級群組和計數

匯總是定義在葉上，並且會重複。 匯總會以群組的形式來輸入群組，將它定義 (檔) ，而非其子群組的子群組。 這項功能稱為多重層級群組。

除了定義于保留和重複的匯總外，這些匯總只會計算一次。 雖然同一份檔可能會在一個群組下表示多次，但匯總只會考慮一次。 下圖說明這個概念。

![圖表顯示匯總是定義于保留和重複的，而且只會計算一次](images/aggregates.png)

## <a name="aggregate-examples"></a>匯總範例

以下是 GROUP ON 子句內的彙總函式範例：


```
GROUP ON System.Sender ['d','m','r'] 
    AGGREGATE COUNT() as 'Total',
              MAX(System.Size) as 'Max Size',
              MIN(System.Size) as 'Min Size'
    OVER (SELECT System.Subject FROM systemindex)
              
GROUP ON System.Sender ['d', 'm', 'r']
      AGGREGATE MAX(System.Search.Rank) as 'MaxRank', 
                MIN(System.Search.Rank) as 'MinRank'
      OVER (GROUP ON system.conversationID
                  OVER (SELECT workid, System.ItemUrl FROM systemindex
                        WHERE CONTAINS (*, 'sometext')
                        ORDER BY System.DateCreated))
               
GROUP ON System.FileName [before('a'),before('z')] 
      AGGREGATE MAX(System.Size) as 'maxsize', MIN(System.Size) as 'MinSize' 
      OVER (SELECT System.FileName FROM systemindex
            ORDER BY System.FileName)      
            
GROUP ON System.author 
      AGGREGATE MAX(System.size) as 'maxsize' 
      ORDER BY min(System.Size) 
      OVER (GROUP ON System.DateCreated 
                  AGGREGATE Count() 
                  ORDER BY MAX(System.size) 
                  OVER (SELECT filename, System.DateCreated, System.Size FROM systemindex
                        WHERE CONTAINS('text')))
```



## <a name="return-value"></a>傳回值

傳回值是在資料列集上找到作為自訂屬性的 variant，可作為指定的別名，如果未指定別名標籤，則為「匯總」。

 

 



