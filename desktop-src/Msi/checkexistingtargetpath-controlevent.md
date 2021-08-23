---
description: 此事件會通知安裝程式，它必須確認選取的路徑是可寫入的。 如果無法寫入路徑，事件就會封鎖與控制項相關聯的進一步工作。
ms.assetid: 4672e2e4-a789-4050-81b9-92ec491745ac
title: CheckExistingTargetPath ControlEvent
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: d523d04eba4ede88ca1382c17c5d40d48dadadbc9520d766b5cfca2b26b77fb5
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/11/2021
ms.locfileid: "119520188"
---
# <a name="checkexistingtargetpath-controlevent"></a>CheckExistingTargetPath ControlEvent

此事件會通知安裝程式，它必須確認選取的路徑是可寫入的。 如果無法寫入路徑，事件就會封鎖與控制項相關聯的進一步工作。

這個事件可以透過 [按鈕控制項](pushbutton-control.md)或 [SelectionTree 控制項](selectiontree-control.md)來發行。 此事件應該撰寫至 [ControlEvent 資料表](controlevent-table.md)。

此 ControlEvent 要求使用者介面必須在 [*完整的 UI*](f-gly.md) 層級上執行。 此事件將無法用於 [*縮減 ui*](r-gly.md) 或 [*基本 ui*](b-gly.md)。 如需詳細資訊，請參閱 [消費者介面層級](user-interface-levels.md)。

## <a name="published-by"></a>發佈者

此 ControlEvent 是由安裝程式所發佈。

## <a name="argument"></a>引數

包含路徑之屬性的名稱。 如果屬性是 indirected，則屬性名稱會以方括弧括住。

## <a name="action-on-subscribers"></a>訂閱者的動作

此 ControlEvent 不會在訂閱者上執行動作。

## <a name="typical-use"></a>一般用法

流覽對話方塊上的 [按鈕](pushbutton-control.md) 控制項會系結至 [ControlEvent](controlevent-table.md) 資料表中的這個事件，以檢查選取的路徑，然後再返回選取專案對話方塊。

 

 



