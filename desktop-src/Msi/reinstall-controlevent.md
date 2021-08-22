---
description: 允許作者在目前的對話方塊正在執行時，起始部分或所有功能的重新安裝。
ms.assetid: bc667f20-3abe-4ef3-b51e-dc74da63f651
title: 重新安裝 ControlEvent
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 1f943d7e5950c9455909dad2d1a4677178a6608d4d8fe9bdfbd4cbf7ef752f2a
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/11/2021
ms.locfileid: "119339718"
---
# <a name="reinstall-controlevent"></a>重新安裝 ControlEvent

重新安裝 ControlEventallows 作者，在目前的對話方塊正在執行時，起始部分或所有功能的重新安裝。

這個事件可以透過 [按鈕控制項](pushbutton-control.md) 或 [SelectionTree 控制項](selectiontree-control.md)來發行。 此事件應該撰寫至 [ControlEvent 資料表](controlevent-table.md)中，而且需要在 [*完整的 UI*](f-gly.md) 層級執行使用者介面。 此事件無法搭配 [*縮減的 ui*](r-gly.md) 或 [*基本 ui*](b-gly.md)來使用。 如需詳細資訊，請參閱 [消費者介面層級](user-interface-levels.md)。

## <a name="published-by"></a>發佈者

此 ControlEvent 是由安裝程式所發佈。

## <a name="argument"></a>引數

字串，該字串為功能的名稱或 "ALL"。

## <a name="action-on-subscribers"></a>訂閱者的動作

此 ControlEvent 不會在訂閱者上執行動作。

## <a name="typical-use"></a>一般用法

此事件會系結至強制回應對話方塊上的 [按鈕](pushbutton-control.md) 控制項。 相同的 [按鈕](pushbutton-control.md) 控制項也應系結至 [ReinstallMode](reinstallmode-controlevent.md) ControlEvent。

 

 



