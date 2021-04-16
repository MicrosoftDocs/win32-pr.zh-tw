---
title: 正在抓取變更
description: 一旦用戶端註冊了特定變更的通知，且發生一或多個這些變更，用戶端就會收到來自路由表管理員的通知。
ms.assetid: 5ddebf2d-e3cb-451c-b082-708d2c7d0f79
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 30ccf66d8a1df671cbd9059c444cf26321911bb1
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 09/16/2019
ms.locfileid: "104507136"
---
# <a name="retrieving-changes"></a><span data-ttu-id="898e9-103">正在抓取變更</span><span class="sxs-lookup"><span data-stu-id="898e9-103">Retrieving Changes</span></span>

<span data-ttu-id="898e9-104">一旦用戶端註冊了特定變更的通知，且發生一或多個這些變更，用戶端就會收到來自路由表管理員的通知。</span><span class="sxs-lookup"><span data-stu-id="898e9-104">Once a client has registered for notification of certain changes and one or more of these changes occurs, the client receives a notification from the routing table manager.</span></span> <span data-ttu-id="898e9-105">路由表管理員會使用先前呼叫 [**RtmRegisterEntity**](/windows/desktop/api/Rtmv2/nf-rtmv2-rtmregisterentity)所提供的 [**RTM \_ 事件 \_ 回呼**](/windows/win32/api/rtmv2/nc-rtmv2-_event_callback)回呼。</span><span class="sxs-lookup"><span data-stu-id="898e9-105">The routing table manager uses the [**RTM\_EVENT\_CALLBACK**](/windows/win32/api/rtmv2/nc-rtmv2-_event_callback) callback that was supplied in a previous call to [**RtmRegisterEntity**](/windows/desktop/api/Rtmv2/nf-rtmv2-rtmregisterentity).</span></span> <span data-ttu-id="898e9-106">路由表管理員指出 \_ \_ 已發生 RTM 變更通知事件。</span><span class="sxs-lookup"><span data-stu-id="898e9-106">The routing table manager indicates that a RTM\_CHANGE\_NOTIFICATION event has occurred.</span></span>

<span data-ttu-id="898e9-107">如需示範如何使用這些函數的範例程式碼，請參閱 [使用事件通知回呼](use-the-event-notification-callback.md)。</span><span class="sxs-lookup"><span data-stu-id="898e9-107">For sample code that shows how to use these functions, see [Use the Event Notification Callback](use-the-event-notification-callback.md).</span></span>

 

 




