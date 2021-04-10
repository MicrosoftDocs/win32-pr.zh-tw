---
description: 網路監視器 SDK 包含建立專家所需的函式和範例程式碼。 不過，您也可以使用現有的工具，包括對話方塊編輯器。
ms.assetid: 6a3834b7-753f-42cc-986f-3d7e8bf79fd9
title: 設計專家
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: df633d971558f9b14374680b09a22771e10ea0d8
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/07/2021
ms.locfileid: "104115345"
---
# <a name="programming-an-expert"></a><span data-ttu-id="df6f4-104">設計專家</span><span class="sxs-lookup"><span data-stu-id="df6f4-104">Programming an Expert</span></span>

<span data-ttu-id="df6f4-105">網路監視器 SDK 包含建立專家所需的函式和範例程式碼。</span><span class="sxs-lookup"><span data-stu-id="df6f4-105">The Network Monitor SDK includes the functions and sample code you need to build experts.</span></span> <span data-ttu-id="df6f4-106">不過，您也可以使用現有的工具，包括對話方塊編輯器。</span><span class="sxs-lookup"><span data-stu-id="df6f4-106">However, you can also use existing tools, including a dialog editor.</span></span>

## <a name="minimum-requirements-to-run-an-expert"></a><span data-ttu-id="df6f4-107">執行專家的最低需求</span><span class="sxs-lookup"><span data-stu-id="df6f4-107">Minimum Requirements to Run an Expert</span></span>

<span data-ttu-id="df6f4-108">下表列出您必須用來建立專家的 DLL 進入點和專家功能。</span><span class="sxs-lookup"><span data-stu-id="df6f4-108">The following table lists the DLL entry points and expert functions you must use to build an expert.</span></span>



| <span data-ttu-id="df6f4-109">名稱</span><span class="sxs-lookup"><span data-stu-id="df6f4-109">Name</span></span>                                                 | <span data-ttu-id="df6f4-110">類型</span><span class="sxs-lookup"><span data-stu-id="df6f4-110">Type</span></span>               | <span data-ttu-id="df6f4-111">必要項？</span><span class="sxs-lookup"><span data-stu-id="df6f4-111">Required?</span></span>                                       |
|------------------------------------------------------|--------------------|-------------------------------------------------|
| [<span data-ttu-id="df6f4-112">**DllMain**</span><span class="sxs-lookup"><span data-stu-id="df6f4-112">**DllMain**</span></span>](dllmain-expert.md)                    | <span data-ttu-id="df6f4-113">DLL 輸入函式</span><span class="sxs-lookup"><span data-stu-id="df6f4-113">DLL entry function</span></span> | <span data-ttu-id="df6f4-114">Yes</span><span class="sxs-lookup"><span data-stu-id="df6f4-114">Yes</span></span>                                             |
| [<span data-ttu-id="df6f4-115">**註冊專家**</span><span class="sxs-lookup"><span data-stu-id="df6f4-115">**Register Expert**</span></span>](register-expert.md)           | <span data-ttu-id="df6f4-116">DLL 輸入函式</span><span class="sxs-lookup"><span data-stu-id="df6f4-116">DLL entry function</span></span> | <span data-ttu-id="df6f4-117">Yes</span><span class="sxs-lookup"><span data-stu-id="df6f4-117">Yes</span></span>                                             |
| [<span data-ttu-id="df6f4-118">**執行**</span><span class="sxs-lookup"><span data-stu-id="df6f4-118">**Run**</span></span>](run.md)                                   | <span data-ttu-id="df6f4-119">DLL 輸入函式</span><span class="sxs-lookup"><span data-stu-id="df6f4-119">DLL entry function</span></span> | <span data-ttu-id="df6f4-120">Yes</span><span class="sxs-lookup"><span data-stu-id="df6f4-120">Yes</span></span>                                             |
| [<span data-ttu-id="df6f4-121">**設定**</span><span class="sxs-lookup"><span data-stu-id="df6f4-121">**Configure**</span></span>](configure.md)                       | <span data-ttu-id="df6f4-122">DLL 輸入函式</span><span class="sxs-lookup"><span data-stu-id="df6f4-122">DLL entry function</span></span> | <span data-ttu-id="df6f4-123">只有當專家提供使用者設定。</span><span class="sxs-lookup"><span data-stu-id="df6f4-123">Only if the expert provides user configuration.</span></span> |
| [<span data-ttu-id="df6f4-124">**ExpertIndicateStatus**</span><span class="sxs-lookup"><span data-stu-id="df6f4-124">**ExpertIndicateStatus**</span></span>](expertindicatestatus.md) | <span data-ttu-id="df6f4-125">專家功能</span><span class="sxs-lookup"><span data-stu-id="df6f4-125">Expert function</span></span>    | <span data-ttu-id="df6f4-126">Yes</span><span class="sxs-lookup"><span data-stu-id="df6f4-126">Yes</span></span>                                             |
| [<span data-ttu-id="df6f4-127">**ExpertSubmitEvent**</span><span class="sxs-lookup"><span data-stu-id="df6f4-127">**ExpertSubmitEvent**</span></span>](expertsubmitevent.md)       | <span data-ttu-id="df6f4-128">專家功能</span><span class="sxs-lookup"><span data-stu-id="df6f4-128">Expert function</span></span>    | <span data-ttu-id="df6f4-129">Yes</span><span class="sxs-lookup"><span data-stu-id="df6f4-129">Yes</span></span>                                             |



 

<span data-ttu-id="df6f4-130">請參閱網路監視器 SDK 中的專家和剖析器參考主題，以更新您的原始程式碼，然後使用這些主題中提供的範例程式碼和程式：</span><span class="sxs-lookup"><span data-stu-id="df6f4-130">Review the expert and parser reference topics in the Network Monitor SDK to update your source code and then use the sample code and procedures provided in these topics:</span></span>

-   [<span data-ttu-id="df6f4-131">打造專家</span><span class="sxs-lookup"><span data-stu-id="df6f4-131">Building an Expert</span></span>](building-an-expert.md)
-   [<span data-ttu-id="df6f4-132">安裝專家</span><span class="sxs-lookup"><span data-stu-id="df6f4-132">Installing an Expert</span></span>](installing-an-expert-to-network-monitor-2-1.md)
-   [<span data-ttu-id="df6f4-133">錯專家</span><span class="sxs-lookup"><span data-stu-id="df6f4-133">Debugging an Expert</span></span>](debugging-an-expert.md)

<span data-ttu-id="df6f4-134">因為函式是透過使用覆迭的函式指標來呼叫，所以專家 Dll 需要 C，而不是 c + + 的呼叫慣例。</span><span class="sxs-lookup"><span data-stu-id="df6f4-134">Expert DLLs require the C, not the C++, calling convention because functions are called through function pointers by using an overlay.</span></span> <span data-ttu-id="df6f4-135">透過一組專門的專家功能，專家可以存取 capture 中的框架。</span><span class="sxs-lookup"><span data-stu-id="df6f4-135">Through a set of specialized expert functions, the expert has access to the frames in the capture.</span></span> <span data-ttu-id="df6f4-136">專家可以使用大部分的網路監視器 API 來操作傳回的資料。</span><span class="sxs-lookup"><span data-stu-id="df6f4-136">The expert can use most of the Network Monitor API to manipulate the returned data.</span></span> <span data-ttu-id="df6f4-137">當專家找到要傳送給使用者的資訊時，它會封裝事件資料結構中的資訊，並將其提交給網路監視器，然後在專家輸出視窗中顯示資訊。</span><span class="sxs-lookup"><span data-stu-id="df6f4-137">When an expert finds information to send to the user, it packages the information in an event data structure and submits it to Network Monitor, which then displays the information in an expert output window.</span></span> <span data-ttu-id="df6f4-138">專家必須定期更新網路監視器，其中包含 [**ExpertIndicateStatus**](expertindicatestatus.md) 函式所提供的百分比-完成狀態資訊。</span><span class="sxs-lookup"><span data-stu-id="df6f4-138">The expert must periodically update Network Monitor with percentage-completion status information, which is provided by the [**ExpertIndicateStatus**](expertindicatestatus.md) function.</span></span>

<span data-ttu-id="df6f4-139">專家匯出的函式的呼叫如下：</span><span class="sxs-lookup"><span data-stu-id="df6f4-139">The expert's exported functions are called as follows:</span></span>

-   <span data-ttu-id="df6f4-140">當網路監視器正在建立要提供給使用者的專家清單時，網路監視器會呼叫 [**註冊專家**](register-expert.md) 功能。</span><span class="sxs-lookup"><span data-stu-id="df6f4-140">When Network Monitor is creating the list of experts to present to the user, Network Monitor calls the [**Register Expert**](register-expert.md) function.</span></span>
-   <span data-ttu-id="df6f4-141">**註冊註冊** 之後，如果專家可以設定，網路監視器會呼叫 [**Configure**](configure.md)函數。</span><span class="sxs-lookup"><span data-stu-id="df6f4-141">After the call to **Register**, if the expert is configurable, Network Monitor calls the [**Configure**](configure.md) function.</span></span>
-   <span data-ttu-id="df6f4-142">當網路監視器使用者按一下 [ **執行專家**] 時，網路監視器會呼叫 [**run**](run.md) 函數。</span><span class="sxs-lookup"><span data-stu-id="df6f4-142">When the Network Monitor user clicks **Run Expert**, Network Monitor calls the [**Run**](run.md) function.</span></span>

<span data-ttu-id="df6f4-143">當專家分析要求的畫面並找出問題時，他們會使用 [**ExpertSubmitEvent**](expertsubmitevent.md) 來提交包含問題相關資訊的事件。</span><span class="sxs-lookup"><span data-stu-id="df6f4-143">When experts analyze the requested frames and find a problem, they use [**ExpertSubmitEvent**](expertsubmitevent.md) to submit an event that contains information about the problem.</span></span> <span data-ttu-id="df6f4-144">網路監視器會將事件發佈至標準 (共用) 事件檢視器或 (如果專家註冊) 至私用事件檢視器。</span><span class="sxs-lookup"><span data-stu-id="df6f4-144">Network Monitor distributes the event to either the standard (shared) Event Viewer or (if the expert registers for it) to a private Event Viewer.</span></span>

 

 



