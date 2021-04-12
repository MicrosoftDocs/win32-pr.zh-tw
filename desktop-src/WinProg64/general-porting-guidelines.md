---
title: 一般移植指導方針
description: 將32位應用程式移植到64位 Microsoft Windows 將比將16位應用程式移植到32位 Windows 更容易。 但是，透過一些審慎的規劃，移動會更順暢。 以下是一些一般的指導方針。
ms.assetid: 28c1656e-93a2-441b-8946-18017e0b2b29
keywords:
- 將32位應用程式移植到64位 Windows 64 位 Windows 程式設計
- 64位 Windows 程式設計指南64位 Windows 程式設計，移植指導方針
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: d31734edd8b85bd61b8b84cb2c66d835f0085ac1
ms.sourcegitcommit: 35bb565804eaeed7ac5503595753f59d120076dd
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 02/09/2021
ms.locfileid: "104195670"
---
# <a name="general-porting-guidelines"></a><span data-ttu-id="a3d5e-107">一般移植指導方針</span><span class="sxs-lookup"><span data-stu-id="a3d5e-107">General Porting Guidelines</span></span>

<span data-ttu-id="a3d5e-108">將32位應用程式移植到64位 Microsoft Windows 將比將16位應用程式移植到32位 Windows 更容易。</span><span class="sxs-lookup"><span data-stu-id="a3d5e-108">Porting 32-bit applications to 64-bit Microsoft Windows will be easier than it was porting 16-bit applications to 32-bit Windows.</span></span> <span data-ttu-id="a3d5e-109">但是，透過一些審慎的規劃，移動會更順暢。</span><span class="sxs-lookup"><span data-stu-id="a3d5e-109">However, the move will go more smoothly with some careful planning.</span></span> <span data-ttu-id="a3d5e-110">以下是一些一般的指導方針。</span><span class="sxs-lookup"><span data-stu-id="a3d5e-110">The following are some general guidelines.</span></span>

## <a name="planning"></a><span data-ttu-id="a3d5e-111">規劃</span><span class="sxs-lookup"><span data-stu-id="a3d5e-111">Planning</span></span>

-   <span data-ttu-id="a3d5e-112">判斷埠所需的工作量量。</span><span class="sxs-lookup"><span data-stu-id="a3d5e-112">Determine the magnitude of the effort required for the port.</span></span> <span data-ttu-id="a3d5e-113">藉由識別下列專案來量測涉及多少工作：</span><span class="sxs-lookup"><span data-stu-id="a3d5e-113">Gauge how much work is involved by identifying the following items:</span></span>
    -   <span data-ttu-id="a3d5e-114">問題 32-位代碼。</span><span class="sxs-lookup"><span data-stu-id="a3d5e-114">Problem 32-bit code.</span></span> <span data-ttu-id="a3d5e-115">使用64位編譯器編譯您的32位程式碼，並檢查錯誤和警告的範圍。</span><span class="sxs-lookup"><span data-stu-id="a3d5e-115">Compile your 32-bit code with the 64-bit compiler and examine the extent of the errors and warnings.</span></span>
    -   <span data-ttu-id="a3d5e-116">共用元件或相依性。</span><span class="sxs-lookup"><span data-stu-id="a3d5e-116">Shared components or dependencies.</span></span> <span data-ttu-id="a3d5e-117">判斷您應用程式中的哪些元件源自其他小組，以及這些小組是否計畫開發64位版本的程式碼。</span><span class="sxs-lookup"><span data-stu-id="a3d5e-117">Determine which components in your application originate from other teams and whether those teams plan to develop 64-bit versions of their code.</span></span>
    -   <span data-ttu-id="a3d5e-118">舊版或元件代碼。</span><span class="sxs-lookup"><span data-stu-id="a3d5e-118">Legacy or assembly code.</span></span> <span data-ttu-id="a3d5e-119">16位的 Windows 應用程式不會在64位的 Windows 上執行，而且必須重寫。</span><span class="sxs-lookup"><span data-stu-id="a3d5e-119">16-bit Windows-based applications do not run on 64-bit Windows and must be rewritten.</span></span> <span data-ttu-id="a3d5e-120">在 WOW64 中執行 x86 程式碼時，您可能會想要重寫此程式碼，以利用 Intel Itanium 架構的速度。</span><span class="sxs-lookup"><span data-stu-id="a3d5e-120">While x86 assembly code runs in WOW64, you may want to rewrite this code to take advantage of the speed of the Intel Itanium architecture.</span></span>
-   <span data-ttu-id="a3d5e-121">移植整個應用程式，而不只是部分的應用程式。</span><span class="sxs-lookup"><span data-stu-id="a3d5e-121">Port the entire application, not just portions of it.</span></span>

    <span data-ttu-id="a3d5e-122">雖然您可以將應用程式的部分或限制程式碼限制為使用/LARGEADDRESSAWARE：否，但這項策略會針對長期難題交易短期的取得。</span><span class="sxs-lookup"><span data-stu-id="a3d5e-122">Although it is possible to port pieces of an application or to limit code to 2G with /LARGEADDRESSAWARE:NO, this strategy trades short-term gain for long-term pain.</span></span>

    > [!Note]  
    > <span data-ttu-id="a3d5e-123">/LARGEADDRESSAWARE： ARM64 二進位檔的 NO 會被忽略。</span><span class="sxs-lookup"><span data-stu-id="a3d5e-123">/LARGEADDRESSAWARE:NO is ignored for an ARM64 binary.</span></span>

     

-   <span data-ttu-id="a3d5e-124">尋找不會移植的技術替代。</span><span class="sxs-lookup"><span data-stu-id="a3d5e-124">Find substitutes for technologies that will not be ported.</span></span>

    <span data-ttu-id="a3d5e-125">某些技術（包括 DAO (資料存取物件) 和 Jet Red database engine）將不會移植到64位的 Windows。</span><span class="sxs-lookup"><span data-stu-id="a3d5e-125">Some technologies, including DAO (Data Access Object) and the Jet Red database engine, will not be ported to 64-bit Windows.</span></span>

-   <span data-ttu-id="a3d5e-126">將您的64位版本視為個別的產品版本。</span><span class="sxs-lookup"><span data-stu-id="a3d5e-126">Treat your 64-bit version as a separate product release.</span></span>

    <span data-ttu-id="a3d5e-127">雖然您的64位產品可能與您的32位共用相同的程式碼基底，但它需要額外的測試，而且可能會有其他的發行考慮。</span><span class="sxs-lookup"><span data-stu-id="a3d5e-127">Even though your 64-bit product may share the same code base as your 32-bit, it needs additional testing and may have other release considerations.</span></span>

## <a name="development"></a><span data-ttu-id="a3d5e-128">部署</span><span class="sxs-lookup"><span data-stu-id="a3d5e-128">Development</span></span>

-   <span data-ttu-id="a3d5e-129">立即開始開發符合規範的程式碼。</span><span class="sxs-lookup"><span data-stu-id="a3d5e-129">Start developing compliant code now.</span></span>

    <span data-ttu-id="a3d5e-130">開發人員可以使用最新的 Windows 標頭檔和新的資料類型來開始撰寫符合規範的程式碼，而不會對32位的產品開發造成負面影響。</span><span class="sxs-lookup"><span data-stu-id="a3d5e-130">Developers can start writing compliant code by using the latest Windows header files and the new data types with no adverse effects on 32-bit product development.</span></span> <span data-ttu-id="a3d5e-131">如需詳細資訊，請參閱 [準備開始64位 Windows](getting-ready-for-64-bit-windows.md)。</span><span class="sxs-lookup"><span data-stu-id="a3d5e-131">For more information, see [Getting Ready for 64-bit Windows](getting-ready-for-64-bit-windows.md).</span></span>

-   <span data-ttu-id="a3d5e-132">確定您的程式碼可以同時針對 32-和64位 Windows 進行編譯。</span><span class="sxs-lookup"><span data-stu-id="a3d5e-132">Ensure that your code can be compiled for both 32- and 64-bit Windows.</span></span>

    <span data-ttu-id="a3d5e-133">新的資料模型的設計目的，是為了允許從單一程式碼基底建立32和64位應用程式，但只需進行一些修改。</span><span class="sxs-lookup"><span data-stu-id="a3d5e-133">The new data model was designed to allow 32- and 64-bit applications to be built from a single code base with few modifications.</span></span> <span data-ttu-id="a3d5e-134">SQL Server 和 Windows 開發團隊正在從相同的程式碼基底開發32和64位版本的產品。</span><span class="sxs-lookup"><span data-stu-id="a3d5e-134">The SQL Server and Windows development teams are developing 32- and 64-bit versions of their products from the same code base.</span></span>

-   <span data-ttu-id="a3d5e-135">使用編譯器的新優化功能，以獲得最佳效能。</span><span class="sxs-lookup"><span data-stu-id="a3d5e-135">Use the compiler's new optimization features for best performance.</span></span>

    <span data-ttu-id="a3d5e-136">Intel Itanium 處理器的程式碼優化比針對 x86 更為重要。</span><span class="sxs-lookup"><span data-stu-id="a3d5e-136">Code optimization for Intel Itanium processors is more important than it was for the x86.</span></span> <span data-ttu-id="a3d5e-137">編譯器會假設有許多先前由微處理器處理的優化函數。</span><span class="sxs-lookup"><span data-stu-id="a3d5e-137">The compiler assumes many of the optimization functions previously handled by the microprocessor.</span></span> <span data-ttu-id="a3d5e-138">您可以使用編譯器的兩項新優化功能，將64位應用程式的效能最大化：特性 *指引優化* 和 *整個程式優化*。</span><span class="sxs-lookup"><span data-stu-id="a3d5e-138">You can maximize the performance of a 64-bit application by using two new optimization features of the compiler: *Profile Guided Optimization* and *Whole Program Optimization*.</span></span> <span data-ttu-id="a3d5e-139">這兩項功能會導致組建時間更長，且需要早期開發良好的測試案例。</span><span class="sxs-lookup"><span data-stu-id="a3d5e-139">Both features result in longer build times and require the early development of good test scenarios.</span></span>

    <span data-ttu-id="a3d5e-140">特性 *指引優化* 牽涉到兩個步驟的編譯流程。</span><span class="sxs-lookup"><span data-stu-id="a3d5e-140">*Profile Guided Optimization* involves a two-step compile process.</span></span> <span data-ttu-id="a3d5e-141">在第一次編譯期間，會檢測程式碼來捕捉執行行為。</span><span class="sxs-lookup"><span data-stu-id="a3d5e-141">During the first compile, the code is instrumented to capture the execution behavior.</span></span> <span data-ttu-id="a3d5e-142">這項資訊會在第二個編譯期間用來引導所有的優化功能。</span><span class="sxs-lookup"><span data-stu-id="a3d5e-142">This information is used during the second compile to guide all optimization features.</span></span>

    <span data-ttu-id="a3d5e-143">*整個程式優化* 會分析所有應用程式檔中的程式碼，而不只是單一檔案。</span><span class="sxs-lookup"><span data-stu-id="a3d5e-143">*Whole Program Optimization* analyzes the code in all application files, not just a single one.</span></span> <span data-ttu-id="a3d5e-144">這種方法會以數種方式提高效能，包括更佳的內嵌，以及改善的副作用分析和自訂呼叫慣例。</span><span class="sxs-lookup"><span data-stu-id="a3d5e-144">This approach increases performance in several ways, including better inlining, as well as improved side-effect analysis and custom calling conventions.</span></span>

## <a name="testing"></a><span data-ttu-id="a3d5e-145">測試</span><span class="sxs-lookup"><span data-stu-id="a3d5e-145">Testing</span></span>

-   <span data-ttu-id="a3d5e-146">判斷您是否要測試在 WOW64 中執行的64或32位程式碼。</span><span class="sxs-lookup"><span data-stu-id="a3d5e-146">Determine whether you'll test 64- or 32-bit code running in WOW64.</span></span>

    <span data-ttu-id="a3d5e-147">某些應用程式包括原生64位程式碼和在 WOW64 中執行的32位程式碼。</span><span class="sxs-lookup"><span data-stu-id="a3d5e-147">Some applications include both native 64-bit code and 32-bit code running in WOW64.</span></span> <span data-ttu-id="a3d5e-148">在開發測試計劃時仔細調查，並決定您的測試控管應為64位、32位或組合。</span><span class="sxs-lookup"><span data-stu-id="a3d5e-148">Investigate this closely while developing a test plan, and decide whether your test tools should be 64-bit, 32-bit, or a combination.</span></span> <span data-ttu-id="a3d5e-149">您通常需要在64位的 Windows 上測試應用程式的64和32位版本。</span><span class="sxs-lookup"><span data-stu-id="a3d5e-149">You will often need to test both the 64- and 32-bit versions of your application on 64-bit Windows.</span></span>

-   <span data-ttu-id="a3d5e-150">測試經常使用的32位元件。</span><span class="sxs-lookup"><span data-stu-id="a3d5e-150">Test frequently used 32-bit components.</span></span>

    <span data-ttu-id="a3d5e-151">首先，將您的程式碼重新編譯為64位並進行測試。</span><span class="sxs-lookup"><span data-stu-id="a3d5e-151">First, recompile your code to 64-bit and test.</span></span> <span data-ttu-id="a3d5e-152">其次，修正問題，在32位中重新編譯，然後進行測試。</span><span class="sxs-lookup"><span data-stu-id="a3d5e-152">Second, fix problems, recompile in 32-bits, and then test.</span></span> <span data-ttu-id="a3d5e-153">第三，重新編譯為64位並進行測試。</span><span class="sxs-lookup"><span data-stu-id="a3d5e-153">Third, recompile to 64-bit and test.</span></span>

-   <span data-ttu-id="a3d5e-154">測試 COM 和 RPC 元件。</span><span class="sxs-lookup"><span data-stu-id="a3d5e-154">Test COM and RPC components.</span></span>

    <span data-ttu-id="a3d5e-155">請確定32和64位 COM 和 RPC 元件都能正確地通訊。</span><span class="sxs-lookup"><span data-stu-id="a3d5e-155">Make sure that both 32- and 64-bit COM and RPC components communicate correctly.</span></span> <span data-ttu-id="a3d5e-156">您可能也必須透過網路測試與16位元件之間的通訊。</span><span class="sxs-lookup"><span data-stu-id="a3d5e-156">You may also have to test communications with 16-bit components over a network.</span></span>

-   <span data-ttu-id="a3d5e-157">在64位 Windows 上測試您的32位版本。</span><span class="sxs-lookup"><span data-stu-id="a3d5e-157">Test your 32-bit version on 64-bit Windows.</span></span>

    <span data-ttu-id="a3d5e-158">客戶可以在64位 Windows 上繼續使用32位應用程式，其中的效能和記憶體問題不是主要考慮。</span><span class="sxs-lookup"><span data-stu-id="a3d5e-158">Customers can continue to use 32-bit applications on 64-bit Windows where performance and memory issues are not major considerations.</span></span>

-   <span data-ttu-id="a3d5e-159">測試不同的記憶體設定。</span><span class="sxs-lookup"><span data-stu-id="a3d5e-159">Test different memory configurations.</span></span>

    <span data-ttu-id="a3d5e-160">在伺服器上新增海量儲存體時，有時會在應用程式或作業系統中顯示先前未察覺的問題。</span><span class="sxs-lookup"><span data-stu-id="a3d5e-160">Adding large amounts of memory on the server sometimes exposes previously unnoticed problems in either the application or the operating system.</span></span>

 

 




