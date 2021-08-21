---
description: 此事件會通知安裝程式將強制回應對話方塊轉換成另一個對話方塊。 安裝程式會移除目前的對話方塊，並使用引數中指出的名稱建立新的對話方塊。
ms.assetid: bd1aa465-55a0-4983-8c71-7e7075ee9dfb
title: NewDialog ControlEvent
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: aed643272bf5cb329e04dc73426d5448ad71cca781bd129992e29f03b02b9dd6
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/11/2021
ms.locfileid: "119519718"
---
# <a name="newdialog-controlevent"></a>NewDialog ControlEvent

此事件會通知安裝程式將強制回應對話方塊轉換成另一個對話方塊。 安裝程式會移除目前的對話方塊，並使用引數中指出的名稱建立新的對話方塊。

這個事件可以透過 [按鈕控制項](pushbutton-control.md)或 [SelectionTree 控制項](selectiontree-control.md)來發行。 此事件應該撰寫至 [ControlEvent 資料表](controlevent-table.md)。

此 ControlEvent 要求使用者介面必須在 [*完整的 UI*](f-gly.md) 層級上執行。 此事件將無法用於 [*縮減 ui*](r-gly.md) 或 [*基本 ui*](b-gly.md)。 如需詳細資訊，請參閱 [消費者介面層級](user-interface-levels.md)。

## <a name="published-by"></a>發佈者

此 ControlEvent 是由安裝程式所發佈。

## <a name="argument"></a>引數

字串，這是新對話方塊的名稱。

## <a name="action-on-subscribers"></a>訂閱者的動作

此 ControlEvent 不會在訂閱者上執行動作。

## <a name="typical-use"></a>一般用法

強制回應對話方塊上的 [按鈕](pushbutton-control.md) 控制項會系結至 [ControlEvent](controlevent-table.md) 資料表中的這個事件，以指示轉換至相同 wizard 順序的下一個或上一個對話方塊。

 

 



