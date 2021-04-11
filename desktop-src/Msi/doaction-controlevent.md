---
description: Dataadapter.doaction ControlEvent 會通知安裝程式執行自訂動作。 這個事件可以透過按鈕控制項、CheckBox 控制項或 SelectionTree 控制項來發行。 此事件應該撰寫至 ControlEvent 資料表。
ms.assetid: 9a855330-8241-4912-84da-4fca43f1d240
title: Dataadapter.doaction ControlEvent
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 74cc16c918522408e4cdf046e95d3d822ba3ac5c
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/07/2021
ms.locfileid: "104112272"
---
# <a name="doaction-controlevent"></a>Dataadapter.doaction ControlEvent

Dataadapter.doaction ControlEvent 會通知安裝程式執行自訂動作。 這個事件可以透過 [按鈕](pushbutton-control.md) 控制項、 [CheckBox](checkbox-control.md) 控制項或 [SelectionTree](selectiontree-control.md) 控制項來發行。 此事件應該撰寫至 [ControlEvent](controlevent-table.md) 資料表。

請注意，Dataadapter.doaction ControlEvent 啟動的自訂動作可以傳送具有 [**Message 方法**](session-message.md)的訊息，但無法傳送具有 [**MsiProcessMessage**](/windows/desktop/api/Msiquery/nf-msiquery-msiprocessmessage)的訊息。 在 Windows Server 2003 之前的系統上，由 Dataadapter.doaction ControlEvent 啟動的自訂動作無法使用 **MsiProcessMessage** 或 **Message 方法** 傳送訊息。 如需詳細資訊，請參閱 [使用 MsiProcessMessage 將訊息傳送至 Windows Installer](sending-messages-to-windows-installer-using-msiprocessmessage.md)。

此 ControlEvent 要求使用者介面必須在 [*完整的 UI*](f-gly.md) 層級上執行。 此事件將無法用於 [*縮減 ui*](r-gly.md) 或 [*基本 ui*](b-gly.md)。 如需詳細資訊，請參閱 [消費者介面層級](user-interface-levels.md)。

## <a name="published-by"></a>發佈者

此 ControlEvent 是由安裝程式所發佈。

## <a name="argument"></a>引數

字串，這是要執行之自訂動作的名稱。

## <a name="action-on-subscribers"></a>訂閱者的動作

此 ControlEvent 不會在訂閱者上執行動作。

## <a name="typical-use"></a>一般用法

對話方塊中的 [按鈕](pushbutton-control.md) 控制項會系結至 [ControlEvent](controlevent-table.md) 資料表中的這個事件，以叫用自訂動作。

 

 



