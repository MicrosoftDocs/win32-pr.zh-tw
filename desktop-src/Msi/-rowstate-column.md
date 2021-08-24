---
description: 保留的 \_ 資料行名稱 RowState 代表與安裝程式資料庫資料表中的每個資料表資料列相關聯的非持續性狀態。
ms.assetid: ff570b47-7c16-47ae-b1c2-2ecad9266372
title: _RowState 資料行
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 42e0164b76589dfa76deb8754df3e11a8b8250a43d791dec92d0fee65dfb719b
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/11/2021
ms.locfileid: "119146091"
---
# <a name="_rowstate-column"></a>\_RowState 資料行

保留的 \_ 資料行名稱 RowState 代表與安裝程式資料庫資料表中的每個資料表資料列相關聯的非持續性狀態。 虛擬資料行的類型為 [整數](integer.md)，而值則由一組位旗標所組成。 所有的位都是可讀取的，但只能設定使用者資訊和暫存位。 只有當資料表已鎖定或在使用中時，才可以使用此資料 (也就是說，包含資料表的視圖) 存在。 下表顯示資料列可以有的屬性。



| 名稱           | 值 | 意義                                                        |
|----------------|-------|----------------------------------------------------------------|
| iraUserInfo    | 0x01  | 屬性可供外部使用。 您可以更新此值。  |
| iraTemporary   | 0x02  | 資料列不是持續性。 您可以更新此值。          |
| iraModified    | 0x04  | 已更新資料列。                                        |
| iraInserted    | 0x08  | 已插入資料列。                                       |
| iraMergeFailed | 0x0F  | 嘗試合併不相同的非索引鍵資料。 |



 

保留的位6到8。

 

 



