---
description: SelectionTree 控制項會使用 SelectionDescription 事件來發行包含反白專案之描述的字串。 此字串是功能資料表的描述欄位。 此事件應該撰寫于 EventMapping 資料表中。
ms.assetid: 29ae9aec-764f-4ff2-9c08-805538130cb1
title: SelectionDescription ControlEvent
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 901db4efbed03341243d1b978dab0b8759fbc02c
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/08/2021
ms.locfileid: "106979197"
---
# <a name="selectiondescription-controlevent"></a>SelectionDescription ControlEvent

[SelectionTree 控制項](selectiontree-control.md)會使用 SelectionDescription 事件來發行包含反白專案之描述的字串。 此字串是 [功能資料表](feature-table.md)的 **描述** 欄位。 此事件應該撰寫于 [EventMapping 資料表](eventmapping-table.md)中。

此事件只會影響與 [SelectionTree 控制項](selectiontree-control.md)位於相同對話方塊的控制項。

此 ControlEvent 要求使用者介面必須在 [*完整的 UI*](f-gly.md) 層級上執行。 此事件將無法用於 [*縮減 ui*](r-gly.md) 或 [*基本 ui*](b-gly.md)。 如需詳細資訊，請參閱 [消費者介面層級](user-interface-levels.md)。

## <a name="published-by"></a>發佈者

[SelectionTree](selectiontree-control.md)

## <a name="argument"></a>引數

無。

## <a name="action-on-subscribers"></a>訂閱者的動作

無。

## <a name="typical-use"></a>一般用法

與 SelectionTree 透過[EventMapping 資料表](eventmapping-table.md)訂閱這個 ControlEvent 的相同強制回應對話方塊上的[文字](text-control.md)控制項。 文字控制項會使用此事件來顯示反白專案的描述。

 

 



