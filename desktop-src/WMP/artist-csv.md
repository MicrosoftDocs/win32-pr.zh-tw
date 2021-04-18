---
title: artist.csv
description: artist.csv
ms.assetid: 50cf2fbc-28cc-4b13-988e-4c02eb821cfd
keywords:
- Windows Media Player 線上商店，artist.csv
- 線上商店、artist.csv
- 輸入1個線上商店，artist.csv
- artist.csv
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 4f548c419f01d23b76172c44cd6e50263c4e9197
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 09/16/2019
ms.locfileid: "104311349"
---
# <a name="artistcsv"></a>artist.csv

此檔案包含目錄中每個演出者的專案。 每個專案都是由下表所述定位字元分隔欄位所組成的資料列。 欄位必須依列出的順序出現。

artist.csv 中的所有欄位都是必要的。

下表中的 Format 資料行描述每個 Unicode 文字欄位的格式化方式。 它不會參考內容的資料類型。 例如，如果 [格式] 資料行中指出了整數，則表示該欄位包含表示整數值的 Unicode 字串，而不是實際的整數。



| 欄位                  | 格式                                            | 描述                                                                                                |
|------------------------|---------------------------------------------------|------------------------------------------------------------------------------------------------------------|
| ArtistID               | 非負整數。 範例：65832              | 演出者的唯一識別碼，artist.csv 中唯一的識別碼。 必須小於 2 ^ 32。                        |
| ArtistName             | Unicode 字串。範例： Don Funk<br/>       | 演出者的顯示名稱。                                                                               |
| LinkedGenreID          | 非負整數。範例：313<br/>      | 演出者主要內容類型的 GenreID。 必須是主要的類型，而不是 subgenre。 只允許一個值。 |
| LinkedSimilarArtistIDs | N/A                                               | 未在此版本中使用。 應為空白。                                                                 |
| 熱門程度             | 可以是整數或十進位值。 範例：1252.25 | 熱門等級。 依熱門程度排序時，可以是清單中的位置。                             |
| FeedsAvailable         | 布林值。 格式： \[ 0 \| 1 \] 範例：0<br/>    | 未在此版本中使用。 應為空白。                                                                 |



 

 

 





