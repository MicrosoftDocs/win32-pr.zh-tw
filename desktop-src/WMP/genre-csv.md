---
title: genre.csv
description: genre.csv
ms.assetid: e05517f4-a69b-4db7-943d-3490253b92f3
keywords:
- Windows Media Player 線上商店，genre.csv
- 線上商店、genre.csv
- 輸入1個線上商店，genre.csv
- genre.csv
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 3a077cadccc0b2da318e60ca2e0636d96319e5b0
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 09/16/2019
ms.locfileid: "103932424"
---
# <a name="genrecsv"></a>genre.csv

此檔案包含目錄中所代表之每個類型的專案。 每個專案都是由下表所述定位字元分隔欄位所組成的資料列。 欄位必須依列出的順序出現。

genre.csv 中的所有欄位都是必要的。

下表中的 Format 資料行描述每個 Unicode 文字欄位的格式化方式。 它不會參考內容的資料類型。 例如，如果 [格式] 資料行中指出了整數，則表示該欄位包含表示整數值的 Unicode 字串，而不是實際的整數。



| 欄位             | 格式                                                    | 描述                                                                                                                                        |
|-------------------|-----------------------------------------------------------|----------------------------------------------------------------------------------------------------------------------------------------------------|
| 內容類型 \_ 識別碼         | 非負整數。範例：22<br/>               | 內容類型識別碼，在 genre.csv 中是唯一的。 必須小於 2 ^ 32。 最多可以有64的內容。                                             |
| GenreTitle        | Unicode 字串。範例：搖滾<br/>                   | 內容類型顯示名稱。                                                                                                                                |
| FeedsAreAvailable | 布林值。格式： \[ 0 \| 1\]<br/> 範例：0<br/> | 藉由跳至摘要來指出是否可以使用「無線電播放」行為。                                                                          |
| HasComposer       | 布林值。格式： \[ 0 \| 1\]<br/> 範例：1<br/> | 如果此類型應該將編輯器資訊儲存在目錄中，則為 True。 如果未設定，則會忽略編輯器資訊，而不會將它編譯成類別目錄。 |



 

 

 





