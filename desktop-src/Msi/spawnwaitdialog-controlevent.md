---
description: 如果 [條件] 資料行中的運算式評估為 FALSE，SpawnWaitDialog ControlEvent 就會觸發 ControlEvent 資料表的 Argument 資料行所指定的對話方塊。
ms.assetid: 38a5d896-2c11-4ce9-b829-104a882723b6
title: SpawnWaitDialog ControlEvent
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: b20059c936a8534d00799c93dfbe3408a19c6dbe
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/07/2021
ms.locfileid: "103943530"
---
# <a name="spawnwaitdialog-controlevent"></a>SpawnWaitDialog ControlEvent

如果 [條件] 資料行中的運算式評估為 FALSE，SpawnWaitDialog ControlEvent 就會觸發 [ControlEvent 資料表](controlevent-table.md)的 Argument 資料行所指定的對話方塊。 只要條件運算式維持 FALSE，對話方塊就會保持開啟狀態，而且只要條件運算式評估為 TRUE，就會移除此對話方塊。

這個事件可以透過 [按鈕控制項](pushbutton-control.md)或 [SelectionTree 控制項](selectiontree-control.md)來發行。 此事件應該撰寫至 [ControlEvent 資料表](controlevent-table.md)。

此 ControlEvent 要求使用者介面必須在 [*完整的 UI*](f-gly.md) 層級上執行。 此事件將無法用於 [*縮減 ui*](r-gly.md) 或 [*基本 ui*](b-gly.md)。 如需詳細資訊，請參閱 [消費者介面層級](user-interface-levels.md)。

## <a name="published-by"></a>發佈者

此 ControlEvent 是由安裝程式所發佈。

## <a name="argument"></a>引數

[對話方塊資料表](dialog-table.md)中的對話方塊。

## <a name="action-on-subscribers"></a>訂閱者的動作

無。

## <a name="typical-use"></a>一般用法

您可以使用 SpawnWaitDialog ControlEvent 來等候任何背景工作完成，該工作可以使用條件運算式（例如屬性的狀態）進行測試。 如需使用 SpawnWaitDialog ControlEvent 的範例，請參閱 [撰寫條件式「請稍候 ...」一節。訊息方塊](authoring-a-conditional-please-wait-------message-box.md)。

 

 



