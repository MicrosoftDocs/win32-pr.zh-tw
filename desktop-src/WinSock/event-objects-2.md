---
description: 重迭 i/o 的導入需要一種機制，讓應用程式明確地建立傳送和接收要求與其後續完成指示之間的關聯。
ms.assetid: 944d87bd-388f-420d-ac7d-69c4a28f8a5c
title: " (Windows 通訊端 2) 的事件物件"
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: e72b60442f9c56ae2c8e9af905bd14b6536b8e10
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/07/2021
ms.locfileid: "104318384"
---
# <a name="event-objects-windows-sockets-2"></a><span data-ttu-id="7b773-103"> (Windows 通訊端 2) 的事件物件</span><span class="sxs-lookup"><span data-stu-id="7b773-103">Event Objects (Windows Sockets 2)</span></span>

<span data-ttu-id="7b773-104">重迭 i/o 的導入需要一種機制，讓應用程式明確地建立傳送和接收要求與其後續完成指示之間的關聯。</span><span class="sxs-lookup"><span data-stu-id="7b773-104">Introducing overlapped I/O requires a mechanism for applications to unambiguously associate send and receive requests with their subsequent completion indications.</span></span> <span data-ttu-id="7b773-105">在 Windows 通訊端2中，這是透過在 Windows 事件之後模型化的事件物件來完成。</span><span class="sxs-lookup"><span data-stu-id="7b773-105">In Windows Sockets 2, this is accomplished with event objects that are modeled after Windows events.</span></span> <span data-ttu-id="7b773-106">Windows 通訊端事件物件是相當簡單的結構，可建立和關閉、設定和清除，以及等候和輪詢。</span><span class="sxs-lookup"><span data-stu-id="7b773-106">Windows Sockets event objects are fairly simple constructs that can be created and closed, set and cleared, and waited upon and polled.</span></span> <span data-ttu-id="7b773-107">其主要的公用程式是讓應用程式封鎖並等候一或多個事件物件變成設定的能力。</span><span class="sxs-lookup"><span data-stu-id="7b773-107">Their prime utility is the ability of an application to block and wait until one or more event objects become set.</span></span>

<span data-ttu-id="7b773-108">應用程式會使用 [**WSACreateEvent**](/windows/desktop/api/Winsock2/nf-winsock2-wsacreateevent) 來取得事件物件控制碼，該控制碼接著可作為必要參數提供給傳送和接收呼叫的重迭版本， ( [**WSASend**](/windows/desktop/api/Winsock2/nf-winsock2-wsasend)、 [**WSASendTo**](/windows/desktop/api/Winsock2/nf-winsock2-wsasendto)、 [**WSARecv**](/windows/desktop/api/Winsock2/nf-winsock2-wsarecv)、 [**WSARecvFrom**](/windows/desktop/api/Winsock2/nf-winsock2-wsarecvfrom)) 。</span><span class="sxs-lookup"><span data-stu-id="7b773-108">Applications use [**WSACreateEvent**](/windows/desktop/api/Winsock2/nf-winsock2-wsacreateevent) to obtain an event object handle that can then be supplied as a required parameter to the overlapped versions of send and receive calls ( [**WSASend**](/windows/desktop/api/Winsock2/nf-winsock2-wsasend), [**WSASendTo**](/windows/desktop/api/Winsock2/nf-winsock2-wsasendto), [**WSARecv**](/windows/desktop/api/Winsock2/nf-winsock2-wsarecv), [**WSARecvFrom**](/windows/desktop/api/Winsock2/nf-winsock2-wsarecvfrom)).</span></span> <span data-ttu-id="7b773-109">在第一次建立時清除的事件物件，會在相關聯的重迭 i/o 作業已完成 (成功或) 錯誤時，由傳輸提供者設定。</span><span class="sxs-lookup"><span data-stu-id="7b773-109">The event object, which is cleared when first created, is set by the transport providers when the associated overlapped I/O operation has completed (either successfully or with errors).</span></span> <span data-ttu-id="7b773-110">**WSACreateEvent** 所建立的每個事件物件都應該有相符的 [**WSACloseEvent**](/windows/desktop/api/Winsock2/nf-winsock2-wsacloseevent)來終結它。</span><span class="sxs-lookup"><span data-stu-id="7b773-110">Each event object created by **WSACreateEvent** should have a matching [**WSACloseEvent**](/windows/desktop/api/Winsock2/nf-winsock2-wsacloseevent) to destroy it.</span></span>

<span data-ttu-id="7b773-111">事件物件也會在 [**WSAEventSelect**](/windows/desktop/api/Winsock2/nf-winsock2-wsaeventselect) 中用來將一個或多個 FD \_ XXX 網路事件與事件物件產生關聯。</span><span class="sxs-lookup"><span data-stu-id="7b773-111">Event objects are also used in [**WSAEventSelect**](/windows/desktop/api/Winsock2/nf-winsock2-wsaeventselect) to associate one or more FD\_XXX network events with an event object.</span></span> <span data-ttu-id="7b773-112">這在 [使用事件物件的非同步通知](asynchronous-notification-using-event-objects-2.md)中有描述。</span><span class="sxs-lookup"><span data-stu-id="7b773-112">This is described in [Asynchronous Notification Using Event Objects](asynchronous-notification-using-event-objects-2.md).</span></span>

<span data-ttu-id="7b773-113">在32位環境中，與事件物件相關的函式（包括 [**WSACreateEvent**](/windows/desktop/api/Winsock2/nf-winsock2-wsacreateevent)、 [**WSACloseEvent**](/windows/desktop/api/Winsock2/nf-winsock2-wsacloseevent)、 [**WSASetEvent**](/windows/desktop/api/Winsock2/nf-winsock2-wsasetevent)、 [**WSAResetEvent**](/windows/desktop/api/Winsock2/nf-winsock2-wsaresetevent)和 [**WSAWaitForMultipleEvents**](/windows/desktop/api/Winsock2/nf-winsock2-wsawaitformultipleevents) ）會使用相同的函式名稱（但不含 WSA 前置詞）直接對應至對應的原生 Windows 函數。</span><span class="sxs-lookup"><span data-stu-id="7b773-113">In 32-bit environments, event object–related functions, including [**WSACreateEvent**](/windows/desktop/api/Winsock2/nf-winsock2-wsacreateevent), [**WSACloseEvent**](/windows/desktop/api/Winsock2/nf-winsock2-wsacloseevent), [**WSASetEvent**](/windows/desktop/api/Winsock2/nf-winsock2-wsasetevent), [**WSAResetEvent**](/windows/desktop/api/Winsock2/nf-winsock2-wsaresetevent), and [**WSAWaitForMultipleEvents**](/windows/desktop/api/Winsock2/nf-winsock2-wsawaitformultipleevents) are directly mapped to the corresponding native Windows functions, using the same function name, but without the WSA prefix.</span></span>

 

 



