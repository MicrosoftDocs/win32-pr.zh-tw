---
title: radio.csv
description: radio.csv
ms.assetid: 8b0a1852-b6c9-4598-b1ab-c679362794b3
keywords:
- Windows Media Player 線上商店，radio.csv
- 線上商店、radio.csv
- 輸入1個線上商店，radio.csv
- radio.csv
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 5271f3a87b32d27996f61e444723f537a09cb827
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 09/16/2019
ms.locfileid: "104301547"
---
# <a name="radiocsv"></a>radio.csv

此檔案包含目錄中所包含之每個收音機饋送的專案。 每個專案都是由下表所述定位字元分隔欄位所組成的資料列。 欄位必須依列出的順序出現。

下表中的 Format 資料行描述每個 Unicode 文字欄位的格式化方式。 它不會參考內容的資料類型。 例如，如果 [格式] 資料行中指出了整數，則表示該欄位包含表示整數值的 Unicode 字串，而不是實際的整數。



| 欄位              | 必要 | 格式                                                                                                               | 描述                                                                                                                        |
|--------------------|----------|----------------------------------------------------------------------------------------------------------------------|------------------------------------------------------------------------------------------------------------------------------------|
| RadioID            | Yes      | 非負整數。                                                                                                | radio.csv 中唯一的廣播摘要識別碼。                                                                             |
| RadioTitle         | Yes      | Unicode 字串。範例：基本點擊次數<br/>                                                                    | 收音機提要標題。                                                                                                                  |
| RadioSubtitle      | No       | Unicode 字串。 範例：美國排行榜。                                                                                     | 收音機摘要副標題。 通常是內容類型或 subgenre 名稱。                                                                               |
| [程式設計人員]         | Yes      | Unicode 字串。 範例： Terri 先生 Duffy                                                                             | 電臺程式設計人員的名稱。 建議此欄位不超過32個字元。                                     |
| PrimaryGenre       | Yes      | 非負整數。                                                                                                | 主要類型的識別碼。 只允許一個值。                                                                            |
| 心情               | Yes      | Unicode 字串。範例：有趣;amiable;energetic;款旺盛<br/>                                       | 描述音樂的一系列形容詞。 最後一個形容詞之後沒有尾端分號。                                    |
| 類別           | Yes      | Unicode 字串                                                                                                       | 未在此版本中使用。 應為空白。                                                                                         |
| 描述        | 否       | Unicode 字串。範例：樂觀不會 disappoint 的已試用和真實演出者的可信賴物件音樂。<br/> | 顯示在屬性頁中的易記描述。 建議此欄位不超過256個字元。                   |
| 熱門程度         | Yes      | 非負整數或十進位值。範例：31<br/>                                                         | 收音機摘要之間的熱門等級。 可以是0。                                                                                    |
| >system.starrating.average         | No       | Float。範例：3.21<br/>                                                                                       | 選擇性。 值（通常介於0和5之間）會舍入至最接近的1/4，以在使用者介面中顯示。                   |
| IsSubscriptionOnly | Yes      | 布林值。 可以是0或1。                                                                                              | 指出饋送是否僅供訂用帳戶使用。                                                                      |
| IsRecentlyAdded    | Yes      | 布林值。 可以是0或1。                                                                                              | 指出是否最近新增此摘要。                                                                                    |
| IsFeatured         | Yes      | 布林值。 可以是0或1。                                                                                              | 指出摘要是否為精選。                                                                                            |
| EditorialGlyph     | Yes      | 非負整數。 應為0。                                                                                   | 未在此版本中使用。 應為0。                                                                                             |
| SortOrderRank      | Yes      | 非負整數。                                                                                                | 當所有電臺都列在使用者介面時，可以使用來決定排序次序。 如果未使用此欄位，則應為0。 |



 

 

 





