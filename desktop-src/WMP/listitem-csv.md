---
title: listitem.csv
description: listitem.csv
ms.assetid: d8f4bdb3-e7a5-4080-9ae7-555bf3695e9c
keywords:
- Windows Media Player 線上商店，listitem.csv
- 線上商店、listitem.csv
- 輸入1個線上商店，listitem.csv
- listitem.csv
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: fe080c5b9426d5394a7d05c1bd293bba84014b0e
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 09/16/2019
ms.locfileid: "104372055"
---
# <a name="listitemcsv"></a>listitem.csv

此檔案包含清單中所包含之每個專案的專案。 每個專案都是由下表所述定位字元分隔欄位所組成的資料列。 欄位必須依列出的順序出現。

所有欄位皆為必填項目。

下表中的 Format 資料行描述每個 Unicode 文字欄位的格式化方式。 它不會參考內容的資料類型。 例如，如果 [格式] 資料行中指出了整數，則表示該欄位包含表示整數值的 Unicode 字串，而不是實際的整數。



| 欄位              | 格式                                          | 描述                                                                                                            |
|--------------------|-------------------------------------------------|------------------------------------------------------------------------------------------------------------------------|
| 連結的 \_ ListID     | 非負整數。範例：465<br/>    | 此專案所屬清單的識別碼。                                                                               |
| 連結 \_ 的   | 非負整數。範例：684793<br/> | 項目的 ID。 可以是曲目的識別碼、專輯、演出者、內容類型、subgenre、廣播或其他清單。 |
| ItemPositionInList | 非負整數。範例：5<br/>      | 專案在其清單中的位置。 清單中的第一個專案位於位置0。                                   |



 

 

 





