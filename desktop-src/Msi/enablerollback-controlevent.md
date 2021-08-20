---
description: 這個 ControlEvent 可以用來開啟或關閉安裝程式的復原功能。
ms.assetid: 5279151c-a7cd-4f66-8d1b-d688b3b1cf82
title: EnableRollback ControlEvent
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 1d3b0cd93a65a9402c915606585f3eb1cd43c058847e2907b1134e1c84982b76
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/11/2021
ms.locfileid: "118143109"
---
# <a name="enablerollback-controlevent"></a>EnableRollback ControlEvent

這個 ControlEvent 可以用來開啟或關閉安裝程式的復原功能。

這個事件可以透過 [按鈕控制項](pushbutton-control.md)或 [SelectionTree 控制項](selectiontree-control.md)來發行。 此事件應該撰寫至 [ControlEvent 資料表](controlevent-table.md)。

此 ControlEvent 要求使用者介面必須在 [*完整的 UI*](f-gly.md) 層級上執行。 此事件將無法用於 [*縮減 ui*](r-gly.md) 或 [*基本 ui*](b-gly.md)。 如需詳細資訊，請參閱 [消費者介面層級](user-interface-levels.md)。

## <a name="published-by"></a>發佈者

此 ControlEvent 是由安裝程式所發佈。

## <a name="argument"></a>引數

False 關閉安裝程式的復原功能。 True 會開啟安裝程式的復原功能。

## <a name="action-on-subscribers"></a>訂閱者的動作

此 ControlEvent 不會在訂閱者上執行動作。

## <a name="typical-use"></a>一般用法

如果安裝程式偵測到沒有足夠的可用磁碟空間來完成安裝，可以使用來關閉復原功能。 在此情況下，ControlEvent 應該與 [**OutOfDiskSpace**](outofdiskspace.md)、 [**OutOfNoRbDiskSpace**](outofnorbdiskspace.md)和 [**PROMPTROLLBACKCOST**](promptrollbackcost.md) 屬性搭配使用。

 

 



