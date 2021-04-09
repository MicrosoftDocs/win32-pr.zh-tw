---
description: WSAEventSelect 和 WSAEnumNetworkEvents 函式的目的是為了容納應用程式，例如沒有使用者介面 (的守護程式和服務，因此不會使用 Windows 控制碼) 。
ms.assetid: 4254937c-7ee6-49a3-9f30-09aebaf2265b
title: 使用事件物件的非同步通知
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 7d0495507eacf0960dc98f31594d7f4881d51488
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/07/2021
ms.locfileid: "103848027"
---
# <a name="asynchronous-notification-using-event-objects"></a><span data-ttu-id="e4338-103">使用事件物件的非同步通知</span><span class="sxs-lookup"><span data-stu-id="e4338-103">Asynchronous Notification Using Event Objects</span></span>

<span data-ttu-id="e4338-104">[**WSAEventSelect**](/windows/desktop/api/Winsock2/nf-winsock2-wsaeventselect)和 [**WSAEnumNetworkEvents**](/windows/desktop/api/Winsock2/nf-winsock2-wsaenumnetworkevents)函式的目的是為了容納應用程式，例如沒有使用者介面 (的守護程式和服務，因此不會使用 Windows 控制碼) 。</span><span class="sxs-lookup"><span data-stu-id="e4338-104">The [**WSAEventSelect**](/windows/desktop/api/Winsock2/nf-winsock2-wsaeventselect) and [**WSAEnumNetworkEvents**](/windows/desktop/api/Winsock2/nf-winsock2-wsaenumnetworkevents) functions are provided to accommodate applications such as daemons and services that have no user interface (and hence do not use Windows handles).</span></span> <span data-ttu-id="e4338-105">**WSAEventSelect** 函式的行為與 [**WSAAsyncSelect**](/windows/desktop/api/winsock/nf-winsock-wsaasyncselect)函數完全相同。</span><span class="sxs-lookup"><span data-stu-id="e4338-105">The **WSAEventSelect** function behaves exactly like the [**WSAAsyncSelect**](/windows/desktop/api/winsock/nf-winsock-wsaasyncselect) function.</span></span> <span data-ttu-id="e4338-106">但是，不會在發生 FD XXX 網路事件時傳送 Windows 訊息 \_ (例如，fd \_ READ 和 FD \_ WRITE) ，會設定應用程式指定的事件物件。</span><span class="sxs-lookup"><span data-stu-id="e4338-106">However, instead of causing a Windows message to be sent on the occurrence of an FD\_XXX network event (for example, FD\_READ and FD\_WRITE), an application-designated event object is set.</span></span>

<span data-ttu-id="e4338-107">此外， \_ 服務提供者還會記住特定的 FD XXX 網路事件。</span><span class="sxs-lookup"><span data-stu-id="e4338-107">Also, the fact that a particular FD\_XXX network event has occurred is remembered by the service provider.</span></span> <span data-ttu-id="e4338-108">應用程式可以呼叫 [**WSAEnumNetworkEvents**](/windows/desktop/api/Winsock2/nf-winsock2-wsaeventselect) ，將網路事件記憶體的目前內容複寫到應用程式提供的緩衝區，並自動清除網路事件記憶體。</span><span class="sxs-lookup"><span data-stu-id="e4338-108">The application can call [**WSAEnumNetworkEvents**](/windows/desktop/api/Winsock2/nf-winsock2-wsaeventselect) to have the current contents of the network event memory copied to an application-supplied buffer and to have the network event memory automatically cleared.</span></span> <span data-ttu-id="e4338-109">如有需要，應用程式也可以指定已清除的特定事件物件，以及網路事件記憶體。</span><span class="sxs-lookup"><span data-stu-id="e4338-109">If needed, the application can also designate a particular event object that is cleared along with the network event memory.</span></span>

 

 



