---
description: 重迭 i/o 的導入需要一種機制，讓應用程式明確地建立傳送和接收要求與其後續完成指示之間的關聯。
ms.assetid: 944d87bd-388f-420d-ac7d-69c4a28f8a5c
title: " (Windows 通訊端 2) 的事件物件"
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 34820d7df92704d86f7dbdc100816789488426e2fdd553456be94da921811c3f
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/11/2021
ms.locfileid: "119132591"
---
# <a name="event-objects-windows-sockets-2"></a> (Windows 通訊端 2) 的事件物件

重迭 i/o 的導入需要一種機制，讓應用程式明確地建立傳送和接收要求與其後續完成指示之間的關聯。 在 Windows 通訊端2中，這是透過在 Windows 事件之後模型化的事件物件來完成。 Windows通訊端事件物件是相當簡單的結構，可建立和關閉、設定和清除，以及等候和輪詢。 其主要的公用程式是讓應用程式封鎖並等候一或多個事件物件變成設定的能力。

應用程式會使用 [**WSACreateEvent**](/windows/desktop/api/Winsock2/nf-winsock2-wsacreateevent) 來取得事件物件控制碼，該控制碼接著可作為必要參數提供給傳送和接收呼叫的重迭版本， ( [**WSASend**](/windows/desktop/api/Winsock2/nf-winsock2-wsasend)、 [**WSASendTo**](/windows/desktop/api/Winsock2/nf-winsock2-wsasendto)、 [**WSARecv**](/windows/desktop/api/Winsock2/nf-winsock2-wsarecv)、 [**WSARecvFrom**](/windows/desktop/api/Winsock2/nf-winsock2-wsarecvfrom)) 。 在第一次建立時清除的事件物件，會在相關聯的重迭 i/o 作業已完成 (成功或) 錯誤時，由傳輸提供者設定。 **WSACreateEvent** 所建立的每個事件物件都應該有相符的 [**WSACloseEvent**](/windows/desktop/api/Winsock2/nf-winsock2-wsacloseevent)來終結它。

事件物件也會在 [**WSAEventSelect**](/windows/desktop/api/Winsock2/nf-winsock2-wsaeventselect) 中用來將一個或多個 FD \_ XXX 網路事件與事件物件產生關聯。 這在 [使用事件物件的非同步通知](asynchronous-notification-using-event-objects-2.md)中有描述。

在32位環境中，與事件物件相關的函式（包括 [**WSACreateEvent**](/windows/desktop/api/Winsock2/nf-winsock2-wsacreateevent)、 [**WSACloseEvent**](/windows/desktop/api/Winsock2/nf-winsock2-wsacloseevent)、 [**WSASetEvent**](/windows/desktop/api/Winsock2/nf-winsock2-wsasetevent)、 [**WSAResetEvent**](/windows/desktop/api/Winsock2/nf-winsock2-wsaresetevent)和 [**WSAWaitForMultipleEvents**](/windows/desktop/api/Winsock2/nf-winsock2-wsawaitformultipleevents) ）會使用相同的函式名稱直接對應至對應的原生 Windows 函式，但不含 WSA 前置詞。

 

 



