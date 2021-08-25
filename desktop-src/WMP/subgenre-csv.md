---
title: subgenre.csv
description: subgenre.csv
ms.assetid: 3ba51cda-0c29-4ce9-9237-8444225349c8
keywords:
- Windows Media Player 線上商店，subgenre.csv
- 線上商店、subgenre.csv
- 輸入1個線上商店，subgenre.csv
- subgenre.csv
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: a10242e955423d75174d04899285dcd3dc20ea2ea4a761d2ab3ba53561c4d41c
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/11/2021
ms.locfileid: "120122938"
---
# <a name="subgenrecsv"></a>subgenre.csv

此檔案包含目錄中所代表之每個 subgenre 的專案。 每個專案都是由下表所述定位字元分隔欄位所組成的資料列。 欄位必須依列出的順序出現。

下表中的 Format 資料行描述每個 Unicode 文字欄位的格式化方式。 它不會參考內容的資料類型。 例如，如果 [格式] 資料行中指出了整數，則表示該欄位包含表示整數值的 Unicode 字串，而不是實際的整數。



| 欄位             | 必要 | 格式                                                                                            | 描述                                                                                                                                               |
|-------------------|----------|---------------------------------------------------------------------------------------------------|-----------------------------------------------------------------------------------------------------------------------------------------------------------|
| SubGenreID        | Yes      | 非負整數。                                                                             | Subgenre 識別碼 (識別碼) ，在 subgenre.csv 中是唯一的。 最多允許 1024 subgenres。                                                                   |
| SubGenreTitle     | Yes      | Unicode 字串。範例：智慧型 Dance 音樂 (IDM) <br/>                                  | Subgenre 顯示名稱。                                                                                                                                    |
| SubGenreSubtitle  | No       | Unicode 字串。範例： New、percussive 電子音樂，不是單純的技術。<br/> | 描述 subgenre 顯示名稱的意義。 應小於64個字元。                                                                     |
| FeedsAreAvailable | Yes      | 布林值。格式： \[ 0 \| 1\]<br/> 範例：0<br/>                                         | 藉由跳至摘要來指出是否可以使用「無線電播放」。                                                                                          |
| 連結的 \_ GenreID   | Yes      | 非負整數 (GenreID) 。範例：12<br/>                                             | 父類型的 GenreID。 只允許一個父系。                                                                                              |
| SortOrderRank     | Yes      | 非負整數。範例：23<br/>                                                       | 在使用者介面中用來排序 subgenres 的排名，最好是唯一的。 如果父類型有10個 subgenres，則這可能是從1到10的整數。 |



 

 

 





