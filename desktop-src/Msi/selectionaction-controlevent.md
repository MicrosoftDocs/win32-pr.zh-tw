---
description: SelectionTree 控制項會使用這個事件來發佈描述反白顯示專案的字串。 字串是 &0034 的其中一個 \# ;\* & \# UIText 資料表中的 Sel 0034; 字串。 此事件應該撰寫于 EventMapping 資料表中。
ms.assetid: 7770b46f-21c7-459f-9778-a86de70d467f
title: SelectionAction ControlEvent
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: eda06826f6ac649e2278441c944cdea0332689af
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/08/2021
ms.locfileid: "106981696"
---
# <a name="selectionaction-controlevent"></a>SelectionAction ControlEvent

[SelectionTree 控制項](selectiontree-control.md)會使用這個事件來發佈描述反白顯示專案的字串。 字串是 \* [UIText 資料表](uitext-table.md)中的其中一個「Sel」字串。 此事件應該撰寫于 [EventMapping 資料表](eventmapping-table.md)中。

此 ControlEvent 要求使用者介面必須在 [*完整的 UI*](f-gly.md) 層級上執行。 此事件將無法用於 [*縮減 ui*](r-gly.md) 或 [*基本 ui*](b-gly.md)。 如需詳細資訊，請參閱 [消費者介面層級](user-interface-levels.md)。

此事件只會影響與 SelectionTree 控制項位於相同對話方塊的控制項。

## <a name="published-by"></a>發佈者

[SelectionTree](selectiontree-control.md)

## <a name="argument"></a>引數

無。

## <a name="action-on-subscribers"></a>訂閱者的動作

無。

## <a name="typical-use"></a>一般用法

與 SelectionTree 相同的強制回應對話方塊中的 [文字](text-control.md) 控制項，應該透過 [EventMapping 資料表](eventmapping-table.md)訂閱此事件。 文字控制項會顯示所選取專案的說明。

 

 



