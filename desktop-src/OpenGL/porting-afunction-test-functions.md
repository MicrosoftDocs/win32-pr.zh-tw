---
title: 移植 afunction 測試函式
description: 下表列出可用的鳶尾花 GL Alpha 測試函式及其對等的 OpenGL 函數。
ms.assetid: cd4082fe-2fd6-43d8-a9a7-37fd448c084b
keywords:
- 鳶尾花 GL 移植，afunction 測試函式
- 從鳶尾花 GL、afunction 測試函式進行移植
- 從鳶尾花 GL 移植至 OpenGL，afunction 測試函式
- 從鳶尾花 GL afunction 測試函式的 OpenGL 移植
- afunction 測試函式
- Alpha 測試函式
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 3abfd3ba46d99f8b70ecfb97c0160efea944ccd2
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 09/16/2019
ms.locfileid: "103840764"
---
# <a name="porting-afunction-test-functions"></a><span data-ttu-id="8c85b-109">移植 afunction 測試函式</span><span class="sxs-lookup"><span data-stu-id="8c85b-109">Porting afunction Test Functions</span></span>

<span data-ttu-id="8c85b-110">下表列出可用的鳶尾花 GL Alpha 測試函式及其對等的 OpenGL 函數。</span><span class="sxs-lookup"><span data-stu-id="8c85b-110">The following table lists the available IRIS GL alpha test functions and their equivalent OpenGL functions.</span></span>



| <span data-ttu-id="8c85b-111">afunction</span><span class="sxs-lookup"><span data-stu-id="8c85b-111">afunction</span></span>    | <span data-ttu-id="8c85b-112">glAlphaFunc</span><span class="sxs-lookup"><span data-stu-id="8c85b-112">glAlphaFunc</span></span>  |
|--------------|--------------|
| <span data-ttu-id="8c85b-113">AF \_ NOTEQUAL</span><span class="sxs-lookup"><span data-stu-id="8c85b-113">AF\_NOTEQUAL</span></span> | <span data-ttu-id="8c85b-114">GL \_ NOTEQUAL</span><span class="sxs-lookup"><span data-stu-id="8c85b-114">GL\_NOTEQUAL</span></span> |
| <span data-ttu-id="8c85b-115">AF \_ 永遠</span><span class="sxs-lookup"><span data-stu-id="8c85b-115">AF\_ALWAYS</span></span>   | <span data-ttu-id="8c85b-116">GL \_ 一律</span><span class="sxs-lookup"><span data-stu-id="8c85b-116">GL\_ALWAYS</span></span>   |
| <span data-ttu-id="8c85b-117">AF \_ 永不</span><span class="sxs-lookup"><span data-stu-id="8c85b-117">AF\_NEVER</span></span>    | <span data-ttu-id="8c85b-118">GL \_ 永不</span><span class="sxs-lookup"><span data-stu-id="8c85b-118">GL\_NEVER</span></span>    |
| <span data-ttu-id="8c85b-119">AF \_ LESS</span><span class="sxs-lookup"><span data-stu-id="8c85b-119">AF\_LESS</span></span>     | <span data-ttu-id="8c85b-120">GL \_ LESS</span><span class="sxs-lookup"><span data-stu-id="8c85b-120">GL\_LESS</span></span>     |
| <span data-ttu-id="8c85b-121">AF \_ 等於</span><span class="sxs-lookup"><span data-stu-id="8c85b-121">AF\_EQUAL</span></span>    | <span data-ttu-id="8c85b-122">GL \_ 相等</span><span class="sxs-lookup"><span data-stu-id="8c85b-122">GL\_EQUAL</span></span>    |
| <span data-ttu-id="8c85b-123">AF \_ LEQUAL</span><span class="sxs-lookup"><span data-stu-id="8c85b-123">AF\_LEQUAL</span></span>   | <span data-ttu-id="8c85b-124">GL \_ LEQUAL</span><span class="sxs-lookup"><span data-stu-id="8c85b-124">GL\_LEQUAL</span></span>   |
| <span data-ttu-id="8c85b-125">AF \_ 更大</span><span class="sxs-lookup"><span data-stu-id="8c85b-125">AF\_GREATER</span></span>  | <span data-ttu-id="8c85b-126">GL \_ 更高</span><span class="sxs-lookup"><span data-stu-id="8c85b-126">GL\_GREATER</span></span>  |
| <span data-ttu-id="8c85b-127">AF \_ GEQUAL</span><span class="sxs-lookup"><span data-stu-id="8c85b-127">AF\_GEQUAL</span></span>   | <span data-ttu-id="8c85b-128">GL \_ GEQUAL</span><span class="sxs-lookup"><span data-stu-id="8c85b-128">GL\_GEQUAL</span></span>   |



 

 

 




