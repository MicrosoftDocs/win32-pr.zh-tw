---
description: 做為主控台應用程式的服務可以註冊主控台控制處理常式，以便在使用者登出時收到通知。
ms.assetid: 86ace8b8-c1cb-4646-bc92-86bd578a82c5
title: 接收服務中的事件
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: b95f7329383ffc8aea08102a2fe8cf8b49e0ef9d
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/08/2021
ms.locfileid: "104514048"
---
# <a name="receiving-events-in-a-service"></a>接收服務中的事件

做為主控台應用程式的服務可以註冊 [主控台控制處理常式](/windows/console/console-control-handlers) ，以便在使用者登出時收到通知。 不過，當互動式使用者登入時，並不會傳送任何的主控台事件。 如需使用者登入時收到通知的相關資訊，請參閱 [建立 Winlogon 通知套件](/windows/desktop/SecAuthN/creating-a-winlogon-notification-package)。

系統會將裝置變更事件廣播到所有服務。 服務可以在視窗程式或其服務控制處理常式中接收這些事件。 若要指定您的服務應該接收哪些事件，請使用 [**RegisterDeviceNotification**](/windows/desktop/api/winuser/nf-winuser-registerdevicenotificationa) 函數。

請務必儘快處理隨插即用的裝置事件。 否則，系統可能會變成沒有回應。 如果您的事件處理常式是執行可能會封鎖執行 (例如 i/o) 的作業，最好先啟動另一個執行緒，以非同步方式執行作業。

當服務呼叫 [**RegisterDeviceNotification**](/windows/desktop/api/winuser/nf-winuser-registerdevicenotificationa)時，服務也會指定視窗控制碼或服務狀態控制碼。 如果服務指定視窗控制碼，則視窗程式會收到通知事件。 如果服務指定其服務狀態控制碼，則其服務控制處理常式會收到通知事件。 如需詳細資訊，請參閱 [**HandlerEx**](/windows/desktop/api/WinSvc/nc-winsvc-lphandler_function_ex)。

當您不再需要 [**RegisterDeviceNotification**](/windows/desktop/api/winuser/nf-winuser-registerdevicenotificationa) 時，必須呼叫 [**UnregisterDeviceNotification**](/windows/desktop/api/winuser/nf-winuser-unregisterdevicenotification) 函式來關閉裝置通知控制碼。

 

 
