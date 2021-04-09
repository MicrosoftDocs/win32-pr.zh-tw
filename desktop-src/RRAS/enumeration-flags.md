---
title: 列舉旗標
description: 列舉旗標
ms.assetid: d5677e3a-c0c1-4768-aae4-f6564a40ee99
keywords:
- 列舉型別
- 列舉旗標
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 9a1cbec08496ccd6338de77ebdddf76547a48258
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 09/16/2019
ms.locfileid: "103932223"
---
# <a name="enumeration-flags"></a><span data-ttu-id="967d0-105">列舉旗標</span><span class="sxs-lookup"><span data-stu-id="967d0-105">Enumeration Flags</span></span>



| <span data-ttu-id="967d0-106">常數</span><span class="sxs-lookup"><span data-stu-id="967d0-106">Constant</span></span>               | <span data-ttu-id="967d0-107">值</span><span class="sxs-lookup"><span data-stu-id="967d0-107">Value</span></span>      | <span data-ttu-id="967d0-108">描述</span><span class="sxs-lookup"><span data-stu-id="967d0-108">Description</span></span>                                                                                                                                               |
|------------------------|------------|-----------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="967d0-109">RTM \_ 列舉 \_ 啟動</span><span class="sxs-lookup"><span data-stu-id="967d0-109">RTM\_ENUM\_START</span></span>       | <span data-ttu-id="967d0-110">0x00000000</span><span class="sxs-lookup"><span data-stu-id="967d0-110">0x00000000</span></span> | <span data-ttu-id="967d0-111">列舉從0/0 開始的路由或目的地。</span><span class="sxs-lookup"><span data-stu-id="967d0-111">Enumerate routes or destinations starting at 0/0.</span></span>                                                                                                         |
| <span data-ttu-id="967d0-112">RTM \_ 列舉 \_ 接下來</span><span class="sxs-lookup"><span data-stu-id="967d0-112">RTM\_ENUM\_NEXT</span></span>        | <span data-ttu-id="967d0-113">0x00000001</span><span class="sxs-lookup"><span data-stu-id="967d0-113">0x00000001</span></span> | <span data-ttu-id="967d0-114">從指定的位址/遮罩長度開始列舉路由或目的地 (例如 10/8) 。</span><span class="sxs-lookup"><span data-stu-id="967d0-114">Enumerate routes or destinations starting at the specified address/mask length (such as 10/8).</span></span> <span data-ttu-id="967d0-115">列舉會繼續至路由表的結尾。</span><span class="sxs-lookup"><span data-stu-id="967d0-115">The enumeration continues to the end of the routing table.</span></span> |
| <span data-ttu-id="967d0-116">RTM \_ 列舉 \_ 範圍</span><span class="sxs-lookup"><span data-stu-id="967d0-116">RTM\_ENUM\_RANGE</span></span>       | <span data-ttu-id="967d0-117">0x00000002</span><span class="sxs-lookup"><span data-stu-id="967d0-117">0x00000002</span></span> | <span data-ttu-id="967d0-118">列舉位址/遮罩長度所指定子樹中的路由或目的地 (例如 10/8) 。</span><span class="sxs-lookup"><span data-stu-id="967d0-118">Enumerate routes or destinations in the specified subtree specified by the address/mask length (such as 10/8).</span></span>                                            |
| <span data-ttu-id="967d0-119">RTM \_ 列舉 \_ 所有 \_ DESTS</span><span class="sxs-lookup"><span data-stu-id="967d0-119">RTM\_ENUM\_ALL\_DESTS</span></span>  | <span data-ttu-id="967d0-120">0x00000000</span><span class="sxs-lookup"><span data-stu-id="967d0-120">0x00000000</span></span> | <span data-ttu-id="967d0-121">傳回所有目的地。</span><span class="sxs-lookup"><span data-stu-id="967d0-121">Return all destinations.</span></span>                                                                                                                                  |
| <span data-ttu-id="967d0-122">RTM \_ 列舉 \_ 專屬 \_ DESTS</span><span class="sxs-lookup"><span data-stu-id="967d0-122">RTM\_ENUM\_OWN\_DESTS</span></span>  | <span data-ttu-id="967d0-123">0x01000000</span><span class="sxs-lookup"><span data-stu-id="967d0-123">0x01000000</span></span> | <span data-ttu-id="967d0-124">只傳回用戶端所擁有的目的地。</span><span class="sxs-lookup"><span data-stu-id="967d0-124">Return only those destinations that the client owns.</span></span>                                                                                                      |
| <span data-ttu-id="967d0-125">RTM \_ 列舉 \_ 所有 \_ 路由</span><span class="sxs-lookup"><span data-stu-id="967d0-125">RTM\_ENUM\_ALL\_ROUTES</span></span> | <span data-ttu-id="967d0-126">0x00000000</span><span class="sxs-lookup"><span data-stu-id="967d0-126">0x00000000</span></span> | <span data-ttu-id="967d0-127">傳回所有路由。</span><span class="sxs-lookup"><span data-stu-id="967d0-127">Return all routes.</span></span>                                                                                                                                        |
| <span data-ttu-id="967d0-128">RTM \_ 列舉 \_ 自己的 \_ 路由</span><span class="sxs-lookup"><span data-stu-id="967d0-128">RTM\_ENUM\_OWN\_ROUTES</span></span> | <span data-ttu-id="967d0-129">0x00010000</span><span class="sxs-lookup"><span data-stu-id="967d0-129">0x00010000</span></span> | <span data-ttu-id="967d0-130">只傳回用戶端所擁有的路由。</span><span class="sxs-lookup"><span data-stu-id="967d0-130">Return only those routes that the client owns.</span></span>                                                                                                            |



 

 

 




