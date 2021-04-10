---
title: 向路由表管理員註冊
description: 在用戶端可以存取路由表之前，它必須先使用 RtmRegisterEntity 函式向路由表管理員註冊。
ms.assetid: 9bdbe138-d31b-42bb-9c51-5f1c5e8a4ca7
keywords:
- 路由表管理員第2版 RRAS，註冊
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: f1ce5a1b350ec5420b3fc32a4e5a68a213a61151
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 09/16/2019
ms.locfileid: "104183431"
---
# <a name="registering-with-the-routing-table-manager"></a><span data-ttu-id="c07ee-104">向路由表管理員註冊</span><span class="sxs-lookup"><span data-stu-id="c07ee-104">Registering with the Routing Table Manager</span></span>

<span data-ttu-id="c07ee-105">在用戶端可以存取路由表之前，它必須先使用 [**RtmRegisterEntity**](/windows/desktop/api/Rtmv2/nf-rtmv2-rtmregisterentity) 函式向路由表管理員註冊。</span><span class="sxs-lookup"><span data-stu-id="c07ee-105">Before a client can access the routing table, it first must register with the routing table manager using the [**RtmRegisterEntity**](/windows/desktop/api/Rtmv2/nf-rtmv2-rtmregisterentity) function.</span></span>

<span data-ttu-id="c07ee-106">當用戶端註冊時，它會將 [**RTM \_ 實體 \_ 資訊**](/windows/desktop/api/Rtmv2/ns-rtmv2-rtm_entity_info) 結構傳遞給路由表管理員。</span><span class="sxs-lookup"><span data-stu-id="c07ee-106">When a client registers, it passes to the routing table manager an [**RTM\_ENTITY\_INFO**](/windows/desktop/api/Rtmv2/ns-rtmv2-rtm_entity_info) structure.</span></span> <span data-ttu-id="c07ee-107">此結構包含可唯一識別用戶端、位址系列，以及用戶端所註冊的路由表管理員實例的資訊。</span><span class="sxs-lookup"><span data-stu-id="c07ee-107">This structure contains the information that uniquely identifies a client, the address family, and the instance of the routing table manager with which the client is registering.</span></span> <span data-ttu-id="c07ee-108">用戶端也可以建立 [**RTM \_ 事件 \_ 回呼**](/windows/win32/api/rtmv2/nc-rtmv2-_event_callback) 回呼。</span><span class="sxs-lookup"><span data-stu-id="c07ee-108">A client can also establish the [**RTM\_EVENT\_CALLBACK**](/windows/win32/api/rtmv2/nc-rtmv2-_event_callback) callback.</span></span> <span data-ttu-id="c07ee-109">路由表管理員將使用此回呼來通知用戶端事件，例如變更通知和用戶端註冊。</span><span class="sxs-lookup"><span data-stu-id="c07ee-109">The routing table manager will use this callback to notify the client of events such as change notifications and client registrations.</span></span>

<span data-ttu-id="c07ee-110">路由表管理員完成其註冊處理，並將控制碼傳回給用戶端。</span><span class="sxs-lookup"><span data-stu-id="c07ee-110">The routing table manager completes its registration processing and returns a handle to the client.</span></span> <span data-ttu-id="c07ee-111">用戶端必須對 RTMv2 函式的所有後續呼叫使用這個控制碼。</span><span class="sxs-lookup"><span data-stu-id="c07ee-111">The client must use this handle for all subsequent calls to RTMv2 functions.</span></span>

<span data-ttu-id="c07ee-112">RTMv2 中使用的 [**RtmRegisterEntity**](/windows/desktop/api/Rtmv2/nf-rtmv2-rtmregisterentity) 函數類似于 RTMv1 中使用的 [**RtmRegisterClient**](rtmregisterclient.md) 函數。</span><span class="sxs-lookup"><span data-stu-id="c07ee-112">The [**RtmRegisterEntity**](/windows/desktop/api/Rtmv2/nf-rtmv2-rtmregisterentity) function that is used in RTMv2 is analogous to the [**RtmRegisterClient**](rtmregisterclient.md) function that is used in RTMv1.</span></span> <span data-ttu-id="c07ee-113">**RtmRegisterClient** 函式已過時，但使用 IPX 的用戶端除外。</span><span class="sxs-lookup"><span data-stu-id="c07ee-113">The **RtmRegisterClient** function is obsolete, except for clients using IPX.</span></span>

<span data-ttu-id="c07ee-114">一旦用戶端完成與路由表管理員的互動之後，就必須呼叫 [**RtmDeregisterEntity**](/windows/desktop/api/Rtmv2/nf-rtmv2-rtmderegisterentity)。</span><span class="sxs-lookup"><span data-stu-id="c07ee-114">Once a client has finished interacting with the routing table manager, it must call [**RtmDeregisterEntity**](/windows/desktop/api/Rtmv2/nf-rtmv2-rtmderegisterentity).</span></span> <span data-ttu-id="c07ee-115">路由表管理員會損毀與用戶端相關聯的控制碼。</span><span class="sxs-lookup"><span data-stu-id="c07ee-115">The routing table manager destroys the handle associated with the client.</span></span> <span data-ttu-id="c07ee-116">為了避免記憶體流失，用戶端必須確保它會在呼叫 **RtmDeregisterEntity** 之前，釋放所有的控制碼並刪除其所擁有的所有路由和下一個躍點。</span><span class="sxs-lookup"><span data-stu-id="c07ee-116">To avoid memory leaks, the client must ensure that it releases all handles and deletes all the routes and next hops that it owns before calling **RtmDeregisterEntity**.</span></span>

<span data-ttu-id="c07ee-117">如需示範如何使用這些函數的範例程式碼，請參閱 [向路由表管理員註冊](register-with-the-routing-table-manager.md) ，並 [使用事件通知回呼](use-the-event-notification-callback.md)。</span><span class="sxs-lookup"><span data-stu-id="c07ee-117">For sample code that shows how to use these functions, see [Register with the Routing Table Manager](register-with-the-routing-table-manager.md) and [Use the Event Notification Callback](use-the-event-notification-callback.md).</span></span>

 

 




