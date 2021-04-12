---
description: 下列 helper 函式只能由匯出執行或設定函數的專家呼叫。
ms.assetid: 6890087c-7c94-41ff-bb5c-4bf88a4e07cc
title: 專家功能
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 7441289008c7dcd647775c2932e210ccd09b24bb
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/07/2021
ms.locfileid: "103847745"
---
# <a name="expert-functions"></a><span data-ttu-id="dbe4e-103">專家功能</span><span class="sxs-lookup"><span data-stu-id="dbe4e-103">Expert Functions</span></span>

<span data-ttu-id="dbe4e-104">下列 helper 函式只能由匯出 [執行](run.md) 或 [設定](configure.md) 函數的專家呼叫。</span><span class="sxs-lookup"><span data-stu-id="dbe4e-104">The following helper functions can only be called by experts that export the [Run](run.md) or [Configure](configure.md) function.</span></span>



| <span data-ttu-id="dbe4e-105">函式</span><span class="sxs-lookup"><span data-stu-id="dbe4e-105">Function</span></span>                                         | <span data-ttu-id="dbe4e-106">描述</span><span class="sxs-lookup"><span data-stu-id="dbe4e-106">Description</span></span>                                                                             |
|--------------------------------------------------|-----------------------------------------------------------------------------------------|
| [<span data-ttu-id="dbe4e-107">ExpertGetFrame</span><span class="sxs-lookup"><span data-stu-id="dbe4e-107">ExpertGetFrame</span></span>](expertgetframe.md)             | <span data-ttu-id="dbe4e-108">從捕捉中取出指定的框架。</span><span class="sxs-lookup"><span data-stu-id="dbe4e-108">Retrieves a given frame from the capture.</span></span>                                               |
| [<span data-ttu-id="dbe4e-109">ExpertIndicateStatus</span><span class="sxs-lookup"><span data-stu-id="dbe4e-109">ExpertIndicateStatus</span></span>](expertindicatestatus.md) | <span data-ttu-id="dbe4e-110">指出專家的「capture」分析完成的百分比。</span><span class="sxs-lookup"><span data-stu-id="dbe4e-110">Indicates the percentage of completion of the expert's analysis of capture.</span></span>             |
| [<span data-ttu-id="dbe4e-111">ExpertGetStartupInfo</span><span class="sxs-lookup"><span data-stu-id="dbe4e-111">ExpertGetStartupInfo</span></span>](expertgetstartupinfo.md) | <span data-ttu-id="dbe4e-112">抓取專家的啟動資訊。</span><span class="sxs-lookup"><span data-stu-id="dbe4e-112">Retrieves the startup information for the expert.</span></span>                                       |
| [<span data-ttu-id="dbe4e-113">ExpertMemorySize</span><span class="sxs-lookup"><span data-stu-id="dbe4e-113">ExpertMemorySize</span></span>](expertmemorysize.md)         | <span data-ttu-id="dbe4e-114">抓取 **ExpertAllocMemory** 函式的呼叫所配置的記憶體大小。</span><span class="sxs-lookup"><span data-stu-id="dbe4e-114">Retrieves the size of memory allocated by a call to the **ExpertAllocMemory** function.</span></span> |
| [<span data-ttu-id="dbe4e-115">ExpertSubmitEvent</span><span class="sxs-lookup"><span data-stu-id="dbe4e-115">ExpertSubmitEvent</span></span>](expertsubmitevent.md)       | <span data-ttu-id="dbe4e-116">指出問題，並抓取問題的相關資訊（如果有的話）。</span><span class="sxs-lookup"><span data-stu-id="dbe4e-116">Indicates a problem and retrieves information about the problem if one exists.</span></span>          |
| [<span data-ttu-id="dbe4e-117">ExpertAllocMemory</span><span class="sxs-lookup"><span data-stu-id="dbe4e-117">ExpertAllocMemory</span></span>](expertallocmemory.md)       | <span data-ttu-id="dbe4e-118">配置專家的記憶體。</span><span class="sxs-lookup"><span data-stu-id="dbe4e-118">Allocates memory for the expert.</span></span>                                                        |
| [<span data-ttu-id="dbe4e-119">ExpertReallocMemory</span><span class="sxs-lookup"><span data-stu-id="dbe4e-119">ExpertReallocMemory</span></span>](expertreallocmemory.md)   | <span data-ttu-id="dbe4e-120">變更 **ExpertAllocMemory** 函式所配置的記憶體大小。</span><span class="sxs-lookup"><span data-stu-id="dbe4e-120">Changes the size of the memory allocated by the **ExpertAllocMemory** function.</span></span>         |
| [<span data-ttu-id="dbe4e-121">ExpertFreeMemory</span><span class="sxs-lookup"><span data-stu-id="dbe4e-121">ExpertFreeMemory</span></span>](expertfreememory.md)         | <span data-ttu-id="dbe4e-122">釋出專家所配置的記憶體。</span><span class="sxs-lookup"><span data-stu-id="dbe4e-122">Frees memory allocated by the expert.</span></span>                                                   |



 

<span data-ttu-id="dbe4e-123">如需匯出函式、專家和剖析器、結構和列舉可呼叫的 helper 函式的詳細資訊，請參閱下列主題：</span><span class="sxs-lookup"><span data-stu-id="dbe4e-123">For information about export functions, helper functions that can be called by experts and parsers, structures, and enumerations, see the following topics:</span></span>



| <span data-ttu-id="dbe4e-124">如需下列資訊</span><span class="sxs-lookup"><span data-stu-id="dbe4e-124">For information about</span></span>                                             | <span data-ttu-id="dbe4e-125">請參閱</span><span class="sxs-lookup"><span data-stu-id="dbe4e-125">See</span></span>                                                                          |
|-------------------------------------------------------------------|------------------------------------------------------------------------------|
| <span data-ttu-id="dbe4e-126">由專家匯出的功能</span><span class="sxs-lookup"><span data-stu-id="dbe4e-126">Functions that are exported by experts</span></span>                            | [<span data-ttu-id="dbe4e-127">專家 DLL 匯出函式</span><span class="sxs-lookup"><span data-stu-id="dbe4e-127">Expert DLL Export Functions</span></span>](expert-dll-export-functions.md)               |
| <span data-ttu-id="dbe4e-128">專家函式所使用的結構</span><span class="sxs-lookup"><span data-stu-id="dbe4e-128">Structures that are used by expert functions</span></span>                      | [<span data-ttu-id="dbe4e-129">專家結構</span><span class="sxs-lookup"><span data-stu-id="dbe4e-129">Expert Structures</span></span>](expert-structures.md)                                   |
| <span data-ttu-id="dbe4e-130">專家結構和函數所使用的列舉</span><span class="sxs-lookup"><span data-stu-id="dbe4e-130">Enumerations used by expert structures and functions</span></span>              | [<span data-ttu-id="dbe4e-131">專家列舉</span><span class="sxs-lookup"><span data-stu-id="dbe4e-131">Expert Enumerations</span></span>](expert-enumerations.md)                               |
| <span data-ttu-id="dbe4e-132">專家和剖析器可呼叫的一般協助程式函式</span><span class="sxs-lookup"><span data-stu-id="dbe4e-132">Common helper functions that can be called by experts and parsers</span></span> | [<span data-ttu-id="dbe4e-133">專家和剖析器一般函數</span><span class="sxs-lookup"><span data-stu-id="dbe4e-133">Expert and Parser Common Functions</span></span>](expert-and-parser-common-functions.md) |



 

 

 



