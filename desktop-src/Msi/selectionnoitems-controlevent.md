---
description: SelectionTree 控制項會使用 SelectionNoItems 事件來刪除過時的專案描述文字，或停用變成無用的按鈕。 此事件應該撰寫于 EventMapping 資料表中。
ms.assetid: a79abd77-a6e5-4a1f-8a63-51644151404a
title: SelectionNoItems ControlEvent
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 6544dfcaad3d22b63d71703ea95d1aa4f09a1efd
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/08/2021
ms.locfileid: "106983934"
---
# <a name="selectionnoitems-controlevent"></a>SelectionNoItems ControlEvent

[SelectionTree 控制項](selectiontree-control.md)會使用 SelectionNoItems 事件來刪除過時的專案描述文字，或停用變成無用的按鈕。 此事件應該撰寫于 [EventMapping 資料表](eventmapping-table.md)中。

此 ControlEvent 要求使用者介面必須在 [*完整的 UI*](f-gly.md) 層級上執行。 此事件將無法用於 [*縮減 ui*](r-gly.md) 或 [*基本 ui*](b-gly.md)。 如需詳細資訊，請參閱 [消費者介面層級](user-interface-levels.md)。

此事件只會影響與 SelectionTree 控制項位於相同對話方塊的控制項。

## <a name="published-by"></a>發佈者

如果選取專案沒有節點，則為[SelectionTree 控制項](selectiontree-control.md)。

## <a name="argument"></a>引數

無。

## <a name="action-on-subscribers"></a>訂閱者的動作

刪除過時的專案描述文字或停用已淘汰的按鈕。

## <a name="typical-use"></a>一般用法

可用來停用選取專案對話方塊上的 [下一步]、[重設] 和 [DiskCost []](selection-dialog.md) 按鈕。

 

 



