---
description: 只有在使用完整的 UI 層級來安裝應用程式時，安裝程式才會執行範例的安裝精靈順序。
ms.assetid: 323d62ae-333b-49fd-96a1-55b228c8ab2c
title: 在安裝結束時新增控制項事件以執行啟動
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: c0cf2a32a30187ea263bd2e3530e6eaae7d236e111826cbcab2461746d9c8e48
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/11/2021
ms.locfileid: "120078218"
---
# <a name="adding-a-control-event-at-the-end-of-the-installation-to-run-launch"></a>在安裝結束時新增控制項事件以執行啟動

只有在使用 [*完整的 UI*](f-gly.md) 層級來安裝應用程式時，安裝程式才會執行範例的安裝精靈順序。 範例對話順序的最後一個對話方塊是名為 ExitDialog 的結束 [對話](exit-dialog.md) 。 當使用者與 ExitDialog 上的 [確定] 按鈕互動時，會先發佈將控制權傳回給安裝程式的 [EndDialog ControlEvent](enddialog-controlevent.md) 。 然後，控制項會發佈執行啟動自訂動作的 [Dataadapter.doaction ControlEvent](doaction-controlevent.md) 。 每個控制項事件都需要 [ControlEvent 資料表](controlevent-table.md)中的記錄。 請參閱 [ControlEvent 總覽](controlevent-overview.md)。

[ControlEvent 資料表](controlevent-table.md)



| 對話     | 控制項\_ | 事件     | 引數 | 條件                     | 排序 |
|------------|-----------|-----------|----------|-------------------------------|----------|
| ExitDialog | 確定        | EndDialog | 傳回   | 1                             | 1        |
| ExitDialog | 確定        | Dataadapter.doaction  | 啟動   | 未安裝且 $Tutorial = 3 | 2        |



 

Dataadapter.doaction 控制項上的條件可確保自訂動作只會在第一次安裝應用程式時執行，而且會安裝在本機。 片語 $Tutorial = 3 表示教學課程元件的動作狀態是設定為 [本機]。 請參閱 [條件陳述式語法](conditional-statement-syntax.md)。

這會完成範例。

 

 



