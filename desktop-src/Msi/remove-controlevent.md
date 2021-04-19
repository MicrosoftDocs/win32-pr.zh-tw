---
description: 當選取要移除的功能或所有功能，同時讓目前的對話方塊執行時，安裝程式會收到此事件的通知。
ms.assetid: dabe44f7-97dd-4037-80e5-f289bab6d4b3
title: 移除 ControlEvent
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 9f214330fc16704fd4eef50bc8c75fc10fc2823d
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/07/2021
ms.locfileid: "106977329"
---
# <a name="remove-controlevent"></a>移除 ControlEvent

當選取要移除的功能或所有功能，同時讓目前的對話方塊執行時，安裝程式會收到此事件的通知。

這個事件可以透過 [按鈕控制項](pushbutton-control.md)、 [CheckBox 控制項](checkbox-control.md)或 [SelectionTree 控制項](selectiontree-control.md)來發行。 此事件應該撰寫至 [ControlEvent 資料表](controlevent-table.md)。

此 ControlEvent 要求使用者介面必須在 [*完整的 UI*](f-gly.md) 層級上執行。 此事件將無法用於 [*縮減 ui*](r-gly.md) 或 [*基本 ui*](b-gly.md)。 如需詳細資訊，請參閱 [消費者介面層級](user-interface-levels.md)。

## <a name="published-by"></a>發佈者

此 ControlEvent 是由安裝程式所發佈。

## <a name="argument"></a>引數

字串，該字串為功能的名稱或 "ALL"。

## <a name="action-on-subscribers"></a>訂閱者的動作

此 ControlEvent 不會在訂閱者上執行動作。

## <a name="action-by-publisher-when-subscriber-activated"></a>訂閱者在訂閱者啟用時的動作

安裝程式會將目前的對話方塊保持在執行狀態，並通知安裝程式。

## <a name="typical-use"></a>一般用法

系結至這個事件的強制回應對話方塊上的 [按鈕](pushbutton-control.md) 控制項。

 

 



