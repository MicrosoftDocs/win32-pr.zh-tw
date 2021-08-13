---
description: 此事件會通知安裝程式，同時讓目前的對話保持執行狀態，以在本機執行功能或所有功能。
ms.assetid: 074f347e-37d3-4365-a25d-caa0392a0dbc
title: AddLocal ControlEvent
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: cfb2db93bea39d167d5b8f08af2cdecfcb07194fb68d4c1e39f5511e2a09f8c4
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/11/2021
ms.locfileid: "118639558"
---
# <a name="addlocal-controlevent"></a>AddLocal ControlEvent

此事件會通知安裝程式，同時讓目前的對話保持執行狀態，以在本機執行功能或所有功能。 這個事件可以透過 [按鈕控制項](pushbutton-control.md)、 [Checkbox 控制項](checkbox-control.md)或 [SelectionTree 控制項](selectiontree-control.md)來發行。 此事件應該撰寫至 [ControlEvent 資料表](controlevent-table.md)。

此 ControlEvent 要求使用者介面必須在 [*完整的 UI*](f-gly.md) 層級上執行。 此事件將無法用於 [*縮減 ui*](r-gly.md) 或 [*基本 ui*](b-gly.md)。 如需詳細資訊，請參閱 [消費者介面層級](user-interface-levels.md)。

## <a name="published-by"></a>發佈者

此 ControlEvent 是由安裝程式所發佈。

## <a name="argument"></a>引數

字串，也就是功能的名稱或 "ALL"。

## <a name="action-on-subscribers"></a>訂閱者的動作

此 ControlEvent 不會在訂閱者上執行動作。

## <a name="typical-use"></a>一般用法

強制回應對話方塊上的 [按鈕](pushbutton-control.md) 控制項系結至此事件，用來通知安裝程式，而不需停止對話方塊。

 

 



