---
description: 保留的 \_ 資料行名稱 RowState 代表與安裝程式資料庫資料表中的每個資料表資料列相關聯的非持續性狀態。
ms.assetid: ff570b47-7c16-47ae-b1c2-2ecad9266372
title: _RowState 資料行
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: e61a2964d7d11c1c2429ad95e9de2b8bdb148954
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/07/2021
ms.locfileid: "104026650"
---
# <a name="_rowstate-column"></a>\_RowState 資料行

保留的 \_ 資料行名稱 RowState 代表與安裝程式資料庫資料表中的每個資料表資料列相關聯的非持續性狀態。 虛擬資料行的類型為 [整數](integer.md)，而值則由一組位旗標所組成。 所有的位都是可讀取的，但只能設定使用者資訊和暫存位。 只有當資料表已鎖定或在使用中時，才可以使用此資料 (也就是說，包含資料表的視圖) 存在。 下表顯示資料列可以有的屬性。



| Name           | 值 | 意義                                                        |
|----------------|-------|----------------------------------------------------------------|
| iraUserInfo    | 0x01  | 屬性可供外部使用。 您可以更新此值。  |
| iraTemporary   | 0x02  | 資料列不是持續性。 您可以更新此值。          |
| iraModified    | 0x04  | 已更新資料列。                                        |
| iraInserted    | 0x08  | 已插入資料列。                                       |
| iraMergeFailed | 0x0F  | 嘗試合併不相同的非索引鍵資料。 |



 

保留的位6到8。

 

 



