---
description: 此事件會通知安裝程式移除強制回應對話方塊。 在所有情況下，安裝程式都會移除目前的對話方塊。
ms.assetid: 74a28696-6387-4d62-8955-4708ba5872bb
title: EndDialog ControlEvent
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: f0f6e61ab12f072e31d6e4efc5f3d2b27ef8629c933baad65fb101b1078ca1f0
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/11/2021
ms.locfileid: "118378250"
---
# <a name="enddialog-controlevent"></a>EndDialog ControlEvent

此事件會通知安裝程式移除強制回應對話方塊。 在所有情況下，安裝程式都會移除目前的對話方塊。

這個事件可以透過 [按鈕控制項](pushbutton-control.md)或 [SelectionTree 控制項](selectiontree-control.md)來發行。 此事件應該撰寫至 [ControlEvent 資料表](controlevent-table.md)。

此 ControlEvent 要求使用者介面必須在 [*完整的 UI*](f-gly.md) 層級上執行。 此事件將無法用於 [*縮減 ui*](r-gly.md) 或 [*基本 ui*](b-gly.md)。 如需詳細資訊，請參閱 [消費者介面層級](user-interface-levels.md)。

下表列出在 [ControlEvent 資料表](controlevent-table.md)中輸入不同引數所產生之事件的動作。



| 引數 | 安裝程式的動作                                                                                                                                                             |
|----------|-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| 結束     | Wizard 順序已關閉，而控制項會傳回具有 UserExit 值的安裝程式。 這個引數不能用在另一個對話方塊子系的對話方塊中。 |
| 重試    | 嚮導順序已關閉，且控制項以暫停值返回安裝程式。 這個引數不能用在另一個對話方塊子系的對話方塊中。  |
| 忽略   | 嚮導順序已關閉，且控制項以已完成的值返回安裝程式。 這個引數不能用在另一個對話方塊子系的對話方塊中。 |
| 傳回   | 控制項會回到目前對話方塊的父系，如果沒有父代，控制項會返回具有 Success 值的安裝程式。                                 |



 

## <a name="published-by"></a>發佈者

此 ControlEvent 是由安裝程式所發佈。

## <a name="argument"></a>引數

在一般對話方塊上， [ControlEvent 資料表](controlevent-table.md) 的 Argument 資料行可以是 "Return"、"Exit"、"Retry" 或 "Ignore"。

在錯誤對話方塊中， [ControlEvent 資料表](controlevent-table.md) 的 Argument 資料行可以是 "ErrorOk"、"ErrorCancel"、"ErrorAbort"、"ErrorRetry"、"ErrorIgnore"、"ErrorYes" 或 "ErrorNo"。

## <a name="action-on-subscribers"></a>訂閱者的動作

無。

## <a name="typical-use"></a>一般用法

強制回應對話方塊上的 [按鈕](pushbutton-control.md) 控制項會系結至 [ControlEvent](controlevent-table.md) 資料表中的這個事件，以關閉對話方塊。

 

 



