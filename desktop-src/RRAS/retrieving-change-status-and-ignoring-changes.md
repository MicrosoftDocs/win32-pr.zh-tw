---
title: 正在捕獲變更狀態並忽略變更
description: 用戶端可以藉由呼叫 RtmGetChangeStatus 來查詢路由表管理員，以找出目的地變更的通知是否暫止。 此函式會傳回 TRUE，直到呼叫端透過呼叫 RtmGetChangedDests 來抓取此變更為止。
ms.assetid: 778279ac-00c5-4de0-9ac7-eca1ac7fec6a
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: e7a339cbf9ba4e97dfef25b2ebc2020ff94f8e20
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 09/16/2019
ms.locfileid: "103672268"
---
# <a name="retrieving-change-status-and-ignoring-changes"></a><span data-ttu-id="0522e-104">正在捕獲變更狀態並忽略變更</span><span class="sxs-lookup"><span data-stu-id="0522e-104">Retrieving Change Status and Ignoring Changes</span></span>

<span data-ttu-id="0522e-105">用戶端可以藉由呼叫 [**RtmGetChangeStatus**](/windows/desktop/api/Rtmv2/nf-rtmv2-rtmgetchangestatus)來查詢路由表管理員，以找出目的地變更的通知是否暫止。</span><span class="sxs-lookup"><span data-stu-id="0522e-105">The client can query the routing table manager to find out if a notification of a change to a destination is pending by calling [**RtmGetChangeStatus**](/windows/desktop/api/Rtmv2/nf-rtmv2-rtmgetchangestatus).</span></span> <span data-ttu-id="0522e-106">此函式會傳回 **TRUE** ，直到呼叫端透過呼叫 [**RtmGetChangedDests**](/windows/desktop/api/Rtmv2/nf-rtmv2-rtmgetchangeddests)來抓取此變更為止。</span><span class="sxs-lookup"><span data-stu-id="0522e-106">This function returns **TRUE** until the caller retrieves this change by calling [**RtmGetChangedDests**](/windows/desktop/api/Rtmv2/nf-rtmv2-rtmgetchangeddests).</span></span>

<span data-ttu-id="0522e-107">用戶端可以使用此查詢來避免執行在接收和處理變更通知之後必須復原的動作。</span><span class="sxs-lookup"><span data-stu-id="0522e-107">A client can use this query to avoid performing an action that would have to be undone after the change notification is received and processed.</span></span> <span data-ttu-id="0522e-108">使用這項功能可讓用戶端將某些作業延後到較晚的時間，以有效率地工作。</span><span class="sxs-lookup"><span data-stu-id="0522e-108">Using this feature allows the client to work efficiently by deferring certain operations to a later time.</span></span>

<span data-ttu-id="0522e-109">用戶端也可以呼叫 [**RtmIgnoreChangedDests**](/windows/desktop/api/Rtmv2/nf-rtmv2-rtmignorechangeddests)，以忽略目的地的暫止變更通知。</span><span class="sxs-lookup"><span data-stu-id="0522e-109">The client can also ignore a pending change notification for a destination by calling [**RtmIgnoreChangedDests**](/windows/desktop/api/Rtmv2/nf-rtmv2-rtmignorechangeddests).</span></span> <span data-ttu-id="0522e-110">除非在呼叫 [**RtmIgnoreChangedDests**](/windows/desktop/api/Rtmv2/nf-rtmv2-rtmignorechangeddests)之後發生其他變更，否則 [**RtmGetChangedDests**](/windows/desktop/api/Rtmv2/nf-rtmv2-rtmgetchangeddests)的後續呼叫不會傳回此目的地。</span><span class="sxs-lookup"><span data-stu-id="0522e-110">A later call to [**RtmGetChangedDests**](/windows/desktop/api/Rtmv2/nf-rtmv2-rtmgetchangeddests) does not return this destination unless another change occurs after the call to [**RtmIgnoreChangedDests**](/windows/desktop/api/Rtmv2/nf-rtmv2-rtmignorechangeddests).</span></span>

 

 




