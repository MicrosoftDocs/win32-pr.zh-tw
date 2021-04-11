---
description: 系統會將一組預設裝置變更事件廣播至所有應用程式和服務。
ms.assetid: 672ad753-210b-41c3-b8c7-e041ce7b1671
title: 裝置通知
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 7caeee8ba50a62a3bc393172347be09d1ac58085
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/07/2021
ms.locfileid: "104111177"
---
# <a name="device-notifications"></a>裝置通知

系統會將一組預設裝置變更事件廣播至所有應用程式和服務。 您不需要註冊來接收這些預設事件。 如需詳細資訊，請參閱 [**RegisterDeviceNotification**](/windows/desktop/api/Winuser/nf-winuser-registerdevicenotificationa) 中的「備註」一節。 若要指定您的應用程式或服務應該接收的其他事件，請使用 **RegisterDeviceNotification** 函數。

當應用程式或服務呼叫 [**RegisterDeviceNotification**](/windows/desktop/api/Winuser/nf-winuser-registerdevicenotificationa)時，它也會指定將接收通知事件的視窗。 服務可以指定服務狀態控制碼，而不是視窗控制碼。 如果服務指定其服務狀態控制碼，則其服務控制處理常式會收到通知事件。 如需詳細資訊，請參閱 [**HandlerEx**](/windows/desktop/api/winsvc/nc-winsvc-lphandler_function_ex)。

請務必儘快處理隨插即用的裝置事件。 否則，系統可能會變成沒有回應。 如果您的事件處理常式是執行可能會封鎖執行 (例如 i/o) 的作業，最好先啟動另一個執行緒，以非同步方式執行作業。

當您不再需要 [**RegisterDeviceNotification**](/windows/desktop/api/Winuser/nf-winuser-registerdevicenotificationa) 時，必須呼叫 [**UnregisterDeviceNotification**](/windows/desktop/api/Winuser/nf-winuser-unregisterdevicenotification) 函式來關閉裝置通知控制碼。

## <a name="related-topics"></a>相關主題

<dl> <dt>

[註冊裝置通知](registering-for-device-notification.md)
</dt> </dl>

 

 
