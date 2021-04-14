---
description: WMI 會在關聯類別的參考屬性中使用物件路徑，以識別相關的物件，以及在多個方法的輸入或輸出參數中使用物件路徑。
ms.assetid: 07fee6f8-810e-4dec-8f0f-787756ee3beb
ms.tgt_platform: multiple
title: WMI 物件路徑需求
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: e2b46195eae3e8351c9c611a34c28cc9d5dd58d6
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/07/2021
ms.locfileid: "104386179"
---
# <a name="wmi-object-path-requirements"></a>WMI 物件路徑需求

WMI 會在關聯類別的參考屬性中使用物件路徑，以識別相關的物件，以及在多個方法的輸入或輸出參數中使用物件路徑。 因為會將物件路徑視為字串來進行查閱和比較，所以當做參考屬性使用時，物件路徑的值一律是字串本身，而不是已取值的物件。 處理物件路徑的字串比較一律不區分大小寫。

物件路徑可以使用下列語法：

-   以單引號括住的字串。
-   斜線作為分隔符號。
-   以反斜線作為分隔符號。
-   整數的十六進位常數。
-   具有採用布林值之索引鍵的類別布林常數。
-   代表非列印字元的 URL 標記法，例如空白空間的 %20。

此外，物件路徑字串必須遵守下列限制：

-   假設的本機伺服器具有部分命名空間路徑。 因此，指定根和預設命名空間表示本機伺服器上的根和預設命名空間。
-   元素內或元素之間沒有空白字元。
-   允許在物件路徑中使用內嵌引號，但必須以 escape 字元分隔引號，如同在 C 或 c + + 應用程式中一樣。
-   只有十進位值會被辨識為索引鍵的數位部分。

 

 



