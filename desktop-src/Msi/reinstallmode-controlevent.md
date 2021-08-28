---
description: 允許作者在重新安裝期間指定驗證模式，以及在目前的對話方塊正在執行時指定模式。
ms.assetid: d7cd41c6-c019-49d6-b593-a1d31c8f5a81
title: ReinstallMode ControlEvent
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 1b21b8f73ddd001d4eea994f3bd159545c39a370caba0a1a625334f3ce08b1b0
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/11/2021
ms.locfileid: "119381008"
---
# <a name="reinstallmode-controlevent"></a>ReinstallMode ControlEvent

ReinstallMode 會 ControlEventallows 作者來指定重新安裝期間的驗證模式或模式，以及目前的對話方塊正在執行。

這個事件可以透過 [按鈕控制項](pushbutton-control.md) 或 [SelectionTree 控制項](selectiontree-control.md)來發行。 此事件應該撰寫至 [ControlEvent 資料表](controlevent-table.md)中，而且需要在 [*完整的 UI*](f-gly.md) 層級執行使用者介面。 此事件無法搭配 [*縮減的 ui*](r-gly.md) 或 [*基本 ui*](b-gly.md)來使用。 如需詳細資訊，請參閱 [消費者介面層級](user-interface-levels.md)。

## <a name="published-by"></a>發佈者

此 ControlEvent 是由安裝程式所發佈。

## <a name="argument"></a>引數

字串。 如需可能值的清單，請參閱 [**REINSTALLMODE**](reinstallmode.md) 屬性。

## <a name="action-on-subscribers"></a>訂閱者的動作

此 ControlEvent 不會在訂閱者上執行動作。

## <a name="typical-use"></a>一般用法

此事件會系結至強制回應對話方塊上的 [按鈕](pushbutton-control.md) 控制項。 相同的 [按鈕](pushbutton-control.md) 控制項也應系結至 [重新安裝](reinstall-controlevent.md) ControlEvent。

 

 



