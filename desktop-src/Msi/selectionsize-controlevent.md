---
description: SelectionTree 控制項會使用 SelectionSize 事件來發佈反白專案的大小。
ms.assetid: 1ef161b6-f127-45ad-a312-d2adcb5124ef
title: SelectionSize ControlEvent
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 24c8733c0155adc085343c0a5db1a42e3aa219719babb5b342781c5bb9923ed0
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/11/2021
ms.locfileid: "120040358"
---
# <a name="selectionsize-controlevent"></a>SelectionSize ControlEvent

[SelectionTree 控制項](selectiontree-control.md)會使用 SelectionSize 事件來發佈反白專案的大小。 如果它是父代專案，則也會一併發行選取的子係數目。 字串是 [SelParentCostNegPos 資料表](uitext-table.md)中的其中一個 **SelChildCostPos**、 **SelChildCostNeg**、 **SelParentCostPosPos**、 **SelParentCostPosNeg**、 **SelParentCostNegNeg** 或 **UIText** 字串。 此事件應該撰寫于 [EventMapping 資料表](eventmapping-table.md)中。

此 ControlEvent 要求使用者介面必須在 [*完整的 UI*](f-gly.md) 層級上執行。 此事件將無法用於 [*縮減 ui*](r-gly.md) 或 [*基本 ui*](b-gly.md)。 如需詳細資訊，請參閱 [消費者介面層級](user-interface-levels.md)。

此事件只會影響與 SelectionTree 控制項位於相同對話方塊的控制項。

## <a name="published-by"></a>發佈者

[SelectionTree](selectiontree-control.md)

## <a name="argument"></a>引數

無。

## <a name="action-on-subscribers"></a>訂閱者的動作

無。

## <a name="typical-use"></a>一般用法

在與 SelectionTree 控制項相同的強制回應對話方塊上，透過[EventMapping 資料表](eventmapping-table.md)的[文字](text-control.md)控制項。 文字控制項會使用此事件來顯示反白專案的大小。

 

 



