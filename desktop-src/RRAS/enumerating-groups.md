---
title: " (RRAS) 列舉群組"
description: 下表摘要說明路由通訊協定與多播群組管理員之間互動的一連串步驟。
ms.assetid: 30a81946-fa60-4424-9a16-a9b4dfe1961e
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 6d3860c6876ed6ea5caef4941efcdd949eb9890d
ms.sourcegitcommit: 40a1246849dba8ececf54c716b2794b99c96ad50
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 11/12/2019
ms.locfileid: "104462605"
---
# <a name="enumerating-groups"></a><span data-ttu-id="d3e9f-103">列舉群組</span><span class="sxs-lookup"><span data-stu-id="d3e9f-103">Enumerating Groups</span></span>

<span data-ttu-id="d3e9f-104">下表摘要說明路由通訊協定與多播群組管理員之間互動的一連串步驟。</span><span class="sxs-lookup"><span data-stu-id="d3e9f-104">The following table summarizes a series of steps in an interaction between a routing protocol and the multicast group manager.</span></span> <span data-ttu-id="d3e9f-105">第一個資料行描述路由通訊協定執行的動作，以及路由通訊協定對多播群組管理員的回應。</span><span class="sxs-lookup"><span data-stu-id="d3e9f-105">The first column describes the actions that the routing protocol performs and the routing protocol's responses to the multicast group manager.</span></span> <span data-ttu-id="d3e9f-106">第二個數據行描述多播群組管理員對路由通訊協定的回應。</span><span class="sxs-lookup"><span data-stu-id="d3e9f-106">The second column describes the multicast group manager's responses to the routing protocol.</span></span> <span data-ttu-id="d3e9f-107">第三個數據行顯示任何其他資訊。</span><span class="sxs-lookup"><span data-stu-id="d3e9f-107">The third column presents any additional information.</span></span>

<span data-ttu-id="d3e9f-108">資料表的每個資料列都代表一個步驟。</span><span class="sxs-lookup"><span data-stu-id="d3e9f-108">Each row of the table represents one step.</span></span>



| <span data-ttu-id="d3e9f-109">路由通訊協定動作</span><span class="sxs-lookup"><span data-stu-id="d3e9f-109">Routing protocol action</span></span>                                                                                                                                                    | <span data-ttu-id="d3e9f-110">多播群組管理員動作</span><span class="sxs-lookup"><span data-stu-id="d3e9f-110">Multicast group manager action</span></span>                                                                                                                                                                                                                                                                               |
|----------------------------------------------------------------------------------------------------------------------------------------------------------------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="d3e9f-111">使用 [**MgmGroupEnumerationStart**](/windows/desktop/api/Mgm/nf-mgm-mgmgroupenumerationstart) 函數取得列舉的控制碼。</span><span class="sxs-lookup"><span data-stu-id="d3e9f-111">Obtain a handle to an enumeration using the [**MgmGroupEnumerationStart**](/windows/desktop/api/Mgm/nf-mgm-mgmgroupenumerationstart) function.</span></span>                                                         | <span data-ttu-id="d3e9f-112">傳回控制碼。</span><span class="sxs-lookup"><span data-stu-id="d3e9f-112">Return a handle.</span></span>                                                                                                                                                                                                                                                                                             |
| <span data-ttu-id="d3e9f-113">使用 [**MgmGroupEnumerationGetNext**](/windows/desktop/api/Mgm/nf-mgm-mgmgroupenumerationgetnext) 函數取得一或多個群組。</span><span class="sxs-lookup"><span data-stu-id="d3e9f-113">Obtain one or more groups using the [**MgmGroupEnumerationGetNext**](/windows/desktop/api/Mgm/nf-mgm-mgmgroupenumerationgetnext) function.</span></span>                                                             | <span data-ttu-id="d3e9f-114">傳回用戶端所提供之緩衝區中的任意數量群組。</span><span class="sxs-lookup"><span data-stu-id="d3e9f-114">Return as many groups as fit in the buffer supplied by the client.</span></span> <span data-ttu-id="d3e9f-115">如果在提供的緩衝區中無法傳回任何群組，則會傳回錯誤的 \_ \_ 緩衝區和傳回一個群組所需的緩衝區大小。</span><span class="sxs-lookup"><span data-stu-id="d3e9f-115">If no groups can be returned in the supplied buffer, return ERROR\_INSUFFICIENT\_BUFFER and the size of the buffer that is needed to return one group.</span></span><br/> <span data-ttu-id="d3e9f-116">如果沒有 \_ 其他 \_ 群組，就會傳回錯誤 \_ 的專案。</span><span class="sxs-lookup"><span data-stu-id="d3e9f-116">Return ERROR\_NO\_MORE\_ITEMS when there are no more groups.</span></span><br/> |
| <span data-ttu-id="d3e9f-117">如果 \_ \_ 接收到緩衝區不足的錯誤，請使用指定大小的緩衝區再次呼叫 [**MgmGroupEnumerationGetNext**](/windows/desktop/api/Mgm/nf-mgm-mgmgroupenumerationgetnext) 函數。</span><span class="sxs-lookup"><span data-stu-id="d3e9f-117">If ERROR\_INSUFFICIENT\_BUFFER is received, call the [**MgmGroupEnumerationGetNext**](/windows/desktop/api/Mgm/nf-mgm-mgmgroupenumerationgetnext) function again using a buffer of the size indicated.</span></span> |                                                                                                                                                                                                                                                                                                              |
| <span data-ttu-id="d3e9f-118">繼續呼叫 [**MgmGroupEnumerationGetNext**](/windows/desktop/api/Mgm/nf-mgm-mgmgroupenumerationgetnext) 函式，直到錯誤 \_ 不再 \_ 收到任何專案為止 \_ 。</span><span class="sxs-lookup"><span data-stu-id="d3e9f-118">Continue calling the [**MgmGroupEnumerationGetNext**](/windows/desktop/api/Mgm/nf-mgm-mgmgroupenumerationgetnext) function until ERROR\_NO\_MORE\_ITEMS is received.</span></span>                                   |                                                                                                                                                                                                                                                                                                              |
| <span data-ttu-id="d3e9f-119">使用 [**MgmGroupEnumerationEnd**](/windows/desktop/api/Mgm/nf-mgm-mgmgroupenumerationend) 函數結束列舉程式。</span><span class="sxs-lookup"><span data-stu-id="d3e9f-119">End the enumeration process using the [**MgmGroupEnumerationEnd**](/windows/desktop/api/Mgm/nf-mgm-mgmgroupenumerationend) function.</span></span>                                                                   | <span data-ttu-id="d3e9f-120">終結控制碼。</span><span class="sxs-lookup"><span data-stu-id="d3e9f-120">Destroy the handle.</span></span>                                                                                                                                                                                                                                                                                          |



 

 

 





