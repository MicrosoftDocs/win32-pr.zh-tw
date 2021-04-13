---
title: 變更通知旗標
description: 變更通知旗標
ms.assetid: 1f1aef71-a2b7-49ad-a0bc-f61f10b701c9
keywords:
- 變更
- 變更通知旗標
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: f3e6d3015be29c84b6b93b47b373d05f96f4388b
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 09/16/2019
ms.locfileid: "104301024"
---
# <a name="change-notification-flags"></a><span data-ttu-id="498c5-105">變更通知旗標</span><span class="sxs-lookup"><span data-stu-id="498c5-105">Change Notification Flags</span></span>



| <span data-ttu-id="498c5-106">常數</span><span class="sxs-lookup"><span data-stu-id="498c5-106">Constant</span></span>                         | <span data-ttu-id="498c5-107">值</span><span class="sxs-lookup"><span data-stu-id="498c5-107">Value</span></span>      | <span data-ttu-id="498c5-108">描述</span><span class="sxs-lookup"><span data-stu-id="498c5-108">Description</span></span>                                                                                                                                                           |
|----------------------------------|------------|-----------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="498c5-109">RTM \_ 數目 \_ 變更 \_ 類型</span><span class="sxs-lookup"><span data-stu-id="498c5-109">RTM\_NUM\_CHANGE\_TYPES</span></span>          | <span data-ttu-id="498c5-110">3</span><span class="sxs-lookup"><span data-stu-id="498c5-110">3</span></span>          | <span data-ttu-id="498c5-111">指定路由表管理員目前使用的變更類型數目。</span><span class="sxs-lookup"><span data-stu-id="498c5-111">Specifies the number of change types that are currently used by the routing table manager.</span></span>                                                                            |
| <span data-ttu-id="498c5-112">RTM \_ 變更 \_ 類型 \_ 全部</span><span class="sxs-lookup"><span data-stu-id="498c5-112">RTM\_CHANGE\_TYPE\_ALL</span></span>           | <span data-ttu-id="498c5-113">0x0001</span><span class="sxs-lookup"><span data-stu-id="498c5-113">0x0001</span></span>     | <span data-ttu-id="498c5-114">通知用戶端對目的地的任何變更。</span><span class="sxs-lookup"><span data-stu-id="498c5-114">Notifies the client of any change to a destination.</span></span>                                                                                                                   |
| <span data-ttu-id="498c5-115">RTM \_ 變更 \_ 類型 \_ 最佳</span><span class="sxs-lookup"><span data-stu-id="498c5-115">RTM\_CHANGE\_TYPE\_BEST</span></span>          | <span data-ttu-id="498c5-116">0x0002</span><span class="sxs-lookup"><span data-stu-id="498c5-116">0x0002</span></span>     | <span data-ttu-id="498c5-117">通知用戶端最適合路由的變更，或當最佳路由變更時。</span><span class="sxs-lookup"><span data-stu-id="498c5-117">Notifies the client of changes to the best route, or when the best route changes.</span></span>                                                                                     |
| <span data-ttu-id="498c5-118">RTM \_ 變更 \_ 類型 \_ 轉送</span><span class="sxs-lookup"><span data-stu-id="498c5-118">RTM\_CHANGE\_TYPE\_FORWARDING</span></span>    | <span data-ttu-id="498c5-119">0x0004</span><span class="sxs-lookup"><span data-stu-id="498c5-119">0x0004</span></span>     | <span data-ttu-id="498c5-120">通知用戶端任何會影響轉送 (的最佳路由變更，例如下一個躍點變更) 。</span><span class="sxs-lookup"><span data-stu-id="498c5-120">Notifies the client of any best route changes that affect forwarding (such as next hop changes).</span></span>                                                                      |
| <span data-ttu-id="498c5-121">RTM \_ 通知 \_ 僅 \_ 標示為 \_ DESTS</span><span class="sxs-lookup"><span data-stu-id="498c5-121">RTM\_NOTIFY\_ONLY\_MARKED\_DESTS</span></span> | <span data-ttu-id="498c5-122">0x00010000</span><span class="sxs-lookup"><span data-stu-id="498c5-122">0x00010000</span></span> | <span data-ttu-id="498c5-123">通知用戶端變更用戶端已標示的目的地。</span><span class="sxs-lookup"><span data-stu-id="498c5-123">Notifies the client of changes to destinations that the client has marked.</span></span> <span data-ttu-id="498c5-124">如果未指定此旗標，則會傳送所有目的地的變更通知訊息。</span><span class="sxs-lookup"><span data-stu-id="498c5-124">If this flag is not specified, change notification messages for all destinations are sent.</span></span> |



 

 

 




