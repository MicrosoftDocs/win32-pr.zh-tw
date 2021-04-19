---
description: .
ms.assetid: fe19e337-3109-42d6-a704-70662ac7c684
title: 啟用 Intel AVX 的 Windows 7 支援
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 440c71c5fd6aa65b5e56b8dfb0b6eab134418192
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/08/2021
ms.locfileid: "106987804"
---
# <a name="enable-windows-7-support-for-intel-avx"></a><span data-ttu-id="913fd-103">啟用 Intel AVX 的 Windows 7 支援</span><span class="sxs-lookup"><span data-stu-id="913fd-103">Enable Windows 7 Support for Intel AVX</span></span>

## <a name="affected-platforms"></a><span data-ttu-id="913fd-104">受影響的平臺</span><span class="sxs-lookup"><span data-stu-id="913fd-104">Affected Platforms</span></span>

 <span data-ttu-id="913fd-105">**客戶** 端-WINDOWS 7 SP1</span><span class="sxs-lookup"><span data-stu-id="913fd-105">**Clients** - Windows 7 SP1</span></span>  
<span data-ttu-id="913fd-106">**伺服器** -Windows Server 2008 R2 SP1</span><span class="sxs-lookup"><span data-stu-id="913fd-106">**Servers** - Windows Server 2008 R2 SP1</span></span>  


## <a name="feature-impact"></a><span data-ttu-id="913fd-107">功能影響</span><span class="sxs-lookup"><span data-stu-id="913fd-107">Feature Impact</span></span>

 <span data-ttu-id="913fd-108">**嚴重性** -低</span><span class="sxs-lookup"><span data-stu-id="913fd-108">**Severity** - Low</span></span>  
<span data-ttu-id="913fd-109">**頻率** -低</span><span class="sxs-lookup"><span data-stu-id="913fd-109">**Frequency** - Low</span></span>  





## <a name="description"></a><span data-ttu-id="913fd-110">Description</span><span class="sxs-lookup"><span data-stu-id="913fd-110">Description</span></span>

<span data-ttu-id="913fd-111">Intel<sup>？</sup></span><span class="sxs-lookup"><span data-stu-id="913fd-111">Intel<sup>?</sup></span></span> <span data-ttu-id="913fd-112">Advanced Vector Extensions (AVX) <sup>？</sup></span><span class="sxs-lookup"><span data-stu-id="913fd-112">Advanced Vector Extensions (AVX)<sup>?</sup></span></span> <span data-ttu-id="913fd-113">是 Intel 架構的256位 SIMD 浮點數向量延伸。</span><span class="sxs-lookup"><span data-stu-id="913fd-113">is a 256-bit SIMD floating-point vector extension of Intel architecture.</span></span> <span data-ttu-id="913fd-114">它包含指令和註冊集合的延伸。</span><span class="sxs-lookup"><span data-stu-id="913fd-114">It includes extensions to both instruction and register sets.</span></span>

<span data-ttu-id="913fd-115">Microsoft 開發了一些 API 增強功能（例如 XState 函式），可讓應用程式存取和操作擴充的處理器功能資訊和狀態，包括 AVX。</span><span class="sxs-lookup"><span data-stu-id="913fd-115">Microsoft has developed some API enhancements, such as XState functions, that enable applications to access and manipulate extended processor feature information and state, including AVX.</span></span>

## <a name="usage-scenarios"></a><span data-ttu-id="913fd-116">使用案例</span><span class="sxs-lookup"><span data-stu-id="913fd-116">Usage Scenarios</span></span>

<span data-ttu-id="913fd-117">有三個一般層級的潛在影響。</span><span class="sxs-lookup"><span data-stu-id="913fd-117">There are three general levels of potential impact.</span></span>

<span data-ttu-id="913fd-118">**層級1：** 即使應用程式呼叫程式庫，或使用間接使用或產生 Intel AVX 擴充功能的編譯器，未直接使用 Intel AVX 的應用程式也不會看到其功能的任何影響。</span><span class="sxs-lookup"><span data-stu-id="913fd-118">**Level 1:** Applications that do not directly use Intel AVX will not see any impact to their functionality even if they call into libraries or use compilers that indirectly use or generate Intel AVX extensions.</span></span> <span data-ttu-id="913fd-119">這代表大部分的應用程式。</span><span class="sxs-lookup"><span data-stu-id="913fd-119">This represents by far the majority of applications.</span></span>

<span data-ttu-id="913fd-120">**層級2：** 明確使用 Intel AVX 指令集的 Advanced 應用程式將能夠在發生硬體例外狀況時存取及變更 AVX 暫存器內容。</span><span class="sxs-lookup"><span data-stu-id="913fd-120">**Level 2:** Advanced applications that explicitly use the Intel AVX instruction set will be able to access and change AVX register contents when a hardware exception is raised.</span></span> <span data-ttu-id="913fd-121">許多應用程式都屬於此類別，因為它表示在例外狀況發生時所執行之指令資料流程的相關知識，例如以組合語言撰寫的應用程式，或是在執行時間產生電腦程式代碼的應用程式 (例如，具有即時編譯) 的 managed 程式碼執行時間。</span><span class="sxs-lookup"><span data-stu-id="913fd-121">A very small number of applications would fall into this category, as it implies an intimate knowledge of the instruction stream executing at the time of the exception, such as applications with sections written in assembly language or those that generate machine code at runtime (for example, managed code runtimes with just-in-time compilation).</span></span>

<span data-ttu-id="913fd-122">**層級3：** 偵錯工具應用程式將能夠在所要進行的應用程式中存取和操作 AVX 狀態。</span><span class="sxs-lookup"><span data-stu-id="913fd-122">**Level 3:** Debugger applications will be able to access and manipulate the AVX state in the application being debugged.</span></span>

## <a name="how-to-leverage-feature-capabilities"></a><span data-ttu-id="913fd-123">如何運用功能功能</span><span class="sxs-lookup"><span data-stu-id="913fd-123">How to Leverage Feature Capabilities</span></span>

<span data-ttu-id="913fd-124">**層級1：** 應用程式不需要採取任何動作，就能使用 Intel AVX。</span><span class="sxs-lookup"><span data-stu-id="913fd-124">**Level 1:** No action is necessary for applications to use Intel AVX.</span></span>

<span data-ttu-id="913fd-125">**層級2：** 此類別中的應用程式可以選擇在例外狀況發生時，從例外狀況篩選準則中存取和操作 AVX 狀態。</span><span class="sxs-lookup"><span data-stu-id="913fd-125">**Level 2:** Applications in this category have the option to access and manipulate AVX state at the time of the exception from within their exception filters.</span></span> <span data-ttu-id="913fd-126">透過 GetExceptionInformation 取得基底處理器內容之後，篩選準則應：</span><span class="sxs-lookup"><span data-stu-id="913fd-126">After obtaining the base processor context via GetExceptionInformation, filters should:</span></span>

 <span data-ttu-id="913fd-127">**1.** 檢查 **內容 \_ XSTATE** 旗標的值。</span><span class="sxs-lookup"><span data-stu-id="913fd-127">**1.** Check the value of the **CONTEXT\_XSTATE** flag.</span></span> <span data-ttu-id="913fd-128">此旗標表示內容中至少存在一個 XState 功能。</span><span class="sxs-lookup"><span data-stu-id="913fd-128">This flag indicates the presence of at least one XState feature in the context.</span></span>  
<span data-ttu-id="913fd-129">**2.** 如果是這種情況，請呼叫 **GetXStateFeaturesMask** ，然後在傳回的遮罩中測試 **XSTATE \_ AVX** 旗標的值。</span><span class="sxs-lookup"><span data-stu-id="913fd-129">**2.** If this is the case, call **GetXStateFeaturesMask** and test the value of the **XSTATE\_AVX** flag in the returned mask.</span></span> <span data-ttu-id="913fd-130">這表示內容中的 AVX 狀態是否存在。</span><span class="sxs-lookup"><span data-stu-id="913fd-130">This indicates the presence of AVX state in the context.</span></span>  
<span data-ttu-id="913fd-131">**3.** 呼叫 **LocateXStateFeature** 來取出儲存 AVX 狀態的實際位置。</span><span class="sxs-lookup"><span data-stu-id="913fd-131">**3.** Call **LocateXStateFeature** to retrieve the actual location where the AVX state is stored.</span></span>  

<span data-ttu-id="913fd-132">**層級3：** 除非您想要存取 Intel AVX 註冊，否則不需要更新現有的偵錯工具應用程式：</span><span class="sxs-lookup"><span data-stu-id="913fd-132">**Level 3:** It is not necessary to update existing debugger applications unless they wish access the Intel AVX registers:</span></span>

<span data-ttu-id="913fd-133">**1.** 若要判斷是否已啟用 AVX，偵錯工具應該使用：</span><span class="sxs-lookup"><span data-stu-id="913fd-133">**1.** To determine if AVX is enabled, the debugger should use:</span></span>

-   <span data-ttu-id="913fd-134">GetEnabledXStateFeatures 在 x86 或 x64 處理器上取得啟用的 XState 功能遮罩，以在使用 XState 處理器功能或嘗試操作 XState 內容之前，判斷系統上存在和啟用的功能</span><span class="sxs-lookup"><span data-stu-id="913fd-134">GetEnabledXStateFeatures to get a mask of enabled XState features on x86 or x64 processors to determine what features are present and enabled on the system before using an XState processor feature or attempting to manipulate XState contexts</span></span>

  
<span data-ttu-id="913fd-135">**2.** 如果有 AVX，而且您想要從正在進行調試的應用程式取出並操作 AVX 狀態 (例如 GetThreadCoNtext 和 SetThreadCoNtext) ，偵錯工具應該使用：</span><span class="sxs-lookup"><span data-stu-id="913fd-135">**2.** If AVX is present and you wish to retrieve and manipulate the AVX state from the application being debugged (for example, GetThreadContext and SetThreadContext), the debugger should use:</span></span>

-   <span data-ttu-id="913fd-136">InitializeCoNtext 函式，可在緩衝區內以所需的大小和對齊方式初始化內容結構</span><span class="sxs-lookup"><span data-stu-id="913fd-136">InitializeContext Function to Initialize a context structure inside a buffer with the necessary size and alignment</span></span>
-   <span data-ttu-id="913fd-137">CopyCoNtext 函式，用來複製來源內容結構 (包括任何 XState) 至初始化的目的地內容結構</span><span class="sxs-lookup"><span data-stu-id="913fd-137">CopyContext Function to copy a source context structure (including any XState) onto an initialized destination context structure</span></span>

  
<span data-ttu-id="913fd-138">**3.** 若要測試、設定及找出處理器內容中的 AVX 狀態，偵錯工具應該使用：</span><span class="sxs-lookup"><span data-stu-id="913fd-138">**3.** To test, set and locate the AVX state within a processor context, the debugger should use:</span></span>

-   <span data-ttu-id="913fd-139">LocateXStateFeature，以取得內容結構內個別 XState 功能的處理器狀態指標</span><span class="sxs-lookup"><span data-stu-id="913fd-139">LocateXStateFeature to retrieve a pointer to the processor state for an individual XState feature within a context structure</span></span>
-   <span data-ttu-id="913fd-140">GetXStateFeaturesMask，以傳回在內容結構內設定之 XState 功能的遮罩</span><span class="sxs-lookup"><span data-stu-id="913fd-140">GetXStateFeaturesMask to return the mask of XState features set within a context structure</span></span>
-   <span data-ttu-id="913fd-141">SetXStateFeaturesMask，以設定在內容結構內設定之 XState 功能的遮罩</span><span class="sxs-lookup"><span data-stu-id="913fd-141">SetXStateFeaturesMask to set the mask of XState features set within a context structure</span></span>

  


## <a name="links-to-other-resources"></a><span data-ttu-id="913fd-142">其他資源的連結</span><span class="sxs-lookup"><span data-stu-id="913fd-142">Links to Other Resources</span></span>

-   <span data-ttu-id="913fd-143">如需 Windows SDK 中 XState 函式的詳細資訊，請參閱 [偵錯工具功能](../debug/debugging-functions.md)。</span><span class="sxs-lookup"><span data-stu-id="913fd-143">For information about the XState functions in the Windows SDK, see [Debugging Functions](../debug/debugging-functions.md).</span></span>
-   <span data-ttu-id="913fd-144">如需 Intel AVX 的指示和功能概述，請參閱 [INTEL AVX：效能改進和能源效率的新新領域](https://software.intel.com/articles/intel-avx-new-frontiers-in-performance-improvements-and-energy-efficiency/)。</span><span class="sxs-lookup"><span data-stu-id="913fd-144">For an overview of the instructions and capabilities of the Intel AVX, see [Intel AVX: New Frontiers in Performance Improvements and Energy Efficiency](https://software.intel.com/articles/intel-avx-new-frontiers-in-performance-improvements-and-energy-efficiency/).</span></span>

 

 
