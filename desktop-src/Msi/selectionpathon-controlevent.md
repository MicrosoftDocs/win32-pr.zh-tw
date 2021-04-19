---
description: SelectionTree 控制項會使用 SelectionPathOn 事件來發佈布林值，指出是否有與目前選取之功能相關聯的選取路徑。 此事件應該撰寫于 EventMapping 資料表中。
ms.assetid: 441b9416-066a-429b-92d2-555584a20fa2
title: SelectionPathOn ControlEvent
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 9882ea534a0d4c91a0107ce3949363350a17fbea
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/08/2021
ms.locfileid: "106971651"
---
# <a name="selectionpathon-controlevent"></a>SelectionPathOn ControlEvent

[SelectionTree 控制項](selectiontree-control.md)會使用 SelectionPathOn 事件來發佈布林值，指出是否有與目前選取之功能相關聯的選取路徑。 此事件應該撰寫于 [EventMapping 資料表](eventmapping-table.md)中。

此事件只會影響與 SelectionTree 控制項位於相同對話方塊的控制項。

此 ControlEvent 要求使用者介面必須在 [*完整的 UI*](f-gly.md) 層級上執行。 此事件將無法用於 [*縮減 ui*](r-gly.md) 或 [*基本 ui*](b-gly.md)。 如需詳細資訊，請參閱 [消費者介面層級](user-interface-levels.md)。

在 [維護安裝](maintenance-installation.md)期間，SelectionPathOn ControlEvent 永遠不會發行。

## <a name="published-by"></a>發佈者

[SelectionTree](selectiontree-control.md)

## <a name="argument"></a>引數

無。

## <a name="action-on-subscribers"></a>訂閱者的動作

無。

## <a name="typical-use"></a>一般用法

在與 SelectionTree 相同的強制回應對話方塊上， [文字](text-control.md) 控制項應透過 [EventMapping 資料表](eventmapping-table.md)訂閱事件。 文字控制項會顯示選取路徑的標題。 此文字控制項會根據事件顯示或隱藏。

 

 



