---
title: 列舉已註冊的實體
description: 在用戶端註冊之後，用戶端可以取得已向路由表管理員註冊的所有其他用戶端清單。 如果偵測到特定類型的用戶端存在，某些用戶端必須執行某些作業。
ms.assetid: d94de573-7c1e-4179-a41f-5836d2c5d44a
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 2ac92ccf89336d3fbca378209b9e79877d9b426a
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 09/16/2019
ms.locfileid: "104021499"
---
# <a name="enumerating-registered-entities"></a><span data-ttu-id="d4ff6-104">列舉已註冊的實體</span><span class="sxs-lookup"><span data-stu-id="d4ff6-104">Enumerating Registered Entities</span></span>

<span data-ttu-id="d4ff6-105">在用戶端註冊之後，用戶端可以取得已向路由表管理員註冊的所有其他用戶端清單。</span><span class="sxs-lookup"><span data-stu-id="d4ff6-105">After a client has registered, the client can obtain a list of all the other clients that have registered with the routing table manager.</span></span> <span data-ttu-id="d4ff6-106">如果偵測到特定類型的用戶端存在，某些用戶端必須執行某些作業。</span><span class="sxs-lookup"><span data-stu-id="d4ff6-106">Some clients must perform certain operations if the presence of a particular type of client is detected.</span></span>

<span data-ttu-id="d4ff6-107">用戶端可以呼叫 [**RtmGetRegisteredEntities**](/windows/desktop/api/Rtmv2/nf-rtmv2-rtmgetregisteredentities) 函數。</span><span class="sxs-lookup"><span data-stu-id="d4ff6-107">The client can call the [**RtmGetRegisteredEntities**](/windows/desktop/api/Rtmv2/nf-rtmv2-rtmgetregisteredentities) function.</span></span> <span data-ttu-id="d4ff6-108">傳回 [**RTM \_ 實體 \_ 資訊**](/windows/desktop/api/Rtmv2/ns-rtmv2-rtm_entity_info) 結構的緩衝區。</span><span class="sxs-lookup"><span data-stu-id="d4ff6-108">A buffer of [**RTM\_ENTITY\_INFO**](/windows/desktop/api/Rtmv2/ns-rtmv2-rtm_entity_info) structures is returned.</span></span> <span data-ttu-id="d4ff6-109">在用戶端處理這項資訊之後，用戶端應該呼叫 [**RtmReleaseEntities**](/windows/desktop/api/Rtmv2/nf-rtmv2-rtmreleaseentities) ，以釋放 **RTM \_ 實體 \_ 資訊** 結構中的控制碼。</span><span class="sxs-lookup"><span data-stu-id="d4ff6-109">After the client has processed this information, the client should call [**RtmReleaseEntities**](/windows/desktop/api/Rtmv2/nf-rtmv2-rtmreleaseentities) to release the handles in the **RTM\_ENTITY\_INFO** structures.</span></span>

<span data-ttu-id="d4ff6-110">如果路由表管理員用戶端在呼叫 [**RtmRegisterEntity**](/windows/desktop/api/Rtmv2/nf-rtmv2-rtmregisterentity)時提供了回呼函式，當任何其他用戶端註冊或取消註冊時，就會通知用戶端。</span><span class="sxs-lookup"><span data-stu-id="d4ff6-110">If the routing table manager client supplied a callback function in the call to [**RtmRegisterEntity**](/windows/desktop/api/Rtmv2/nf-rtmv2-rtmregisterentity), the client is notified when any other clients register or unregister.</span></span>

<span data-ttu-id="d4ff6-111">如需示範如何使用這些函數的範例程式碼，請參閱 [列舉已註冊的實體](enumerate-the-registered-entities.md) 並 [使用事件通知回呼](use-the-event-notification-callback.md)。</span><span class="sxs-lookup"><span data-stu-id="d4ff6-111">For sample code that shows how to use these functions, see [Enumerate the Registered Entities](enumerate-the-registered-entities.md) and [Use the Event Notification Callback](use-the-event-notification-callback.md).</span></span>

 

 




