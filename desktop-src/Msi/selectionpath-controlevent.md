---
description: SelectionTree 控制項會使用 SelectionPath 事件來發佈反白專案的路徑。
ms.assetid: 755e5bf2-42c4-4213-9bb7-4f15ad22041f
title: SelectionPath ControlEvent
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 8314b12d14e10ccf96c7db9db32e63172050c0bc
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/08/2021
ms.locfileid: "103944421"
---
# <a name="selectionpath-controlevent"></a>SelectionPath ControlEvent

[SelectionTree 控制項](selectiontree-control.md)會使用 SelectionPath 事件來發佈反白專案的路徑。 如果已選取要從來源執行的專案，則這是來源的路徑。 如果選取的專案不存在，則字串會是 [UIText 資料表](uitext-table.md)中的 **AbsentPath** 字串。 此事件應該撰寫于 [EventMapping 資料表](eventmapping-table.md)中。

此 ControlEvent 要求使用者介面必須在 [*完整的 UI*](f-gly.md) 層級上執行。 此事件將無法用於 [*縮減 ui*](r-gly.md) 或 [*基本 ui*](b-gly.md)。 如需詳細資訊，請參閱 [消費者介面層級](user-interface-levels.md)。

此事件只會影響與 SelectionTree 控制項位於相同對話方塊的控制項。

## <a name="published-by"></a>發佈者

[SelectionTree](selectiontree-control.md)

## <a name="argument"></a>引數

無。

## <a name="action-on-subscribers"></a>訂閱者的動作

無。

## <a name="typical-use"></a>一般用法

在與 SelectionTree 相同的強制回應對話方塊上， [文字](text-control.md) 控制項應透過 [EventMapping 資料表](eventmapping-table.md)訂閱事件。 文字控制項會顯示反白專案的路徑。

 

 



