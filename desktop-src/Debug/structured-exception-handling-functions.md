---
description: 下列函數用於結構化例外狀況處理。
ms.assetid: 61cf055b-eb9a-4e56-9d36-21fc95adea77
title: 結構化例外狀況處理函式
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: c70b431be2961a55bba28bdfe07723e93b95ac69
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/07/2021
ms.locfileid: "106972334"
---
# <a name="structured-exception-handling-functions"></a><span data-ttu-id="f1499-103">結構化例外狀況處理函式</span><span class="sxs-lookup"><span data-stu-id="f1499-103">Structured Exception Handling Functions</span></span>

<span data-ttu-id="f1499-104">下列函數用於結構化例外狀況處理。</span><span class="sxs-lookup"><span data-stu-id="f1499-104">The following functions are used in structured exception handling.</span></span>

-   [<span data-ttu-id="f1499-105">**AbnormalTermination**</span><span class="sxs-lookup"><span data-stu-id="f1499-105">**AbnormalTermination**</span></span>](abnormaltermination.md)

    <span data-ttu-id="f1499-106">指出終止處理常式的 **\_ \_ try** 區塊是否正常終止。</span><span class="sxs-lookup"><span data-stu-id="f1499-106">Indicates whether the **\_\_try** block of a termination handler terminated normally.</span></span>

-   [<span data-ttu-id="f1499-107">**AddVectoredContinueHandler**</span><span class="sxs-lookup"><span data-stu-id="f1499-107">**AddVectoredContinueHandler**</span></span>](/windows/win32/api/errhandlingapi/nf-errhandlingapi-addvectoredcontinuehandler)

    <span data-ttu-id="f1499-108">註冊向量 continue 處理常式。</span><span class="sxs-lookup"><span data-stu-id="f1499-108">Registers a vectored continue handler.</span></span>

-   [<span data-ttu-id="f1499-109">**AddVectoredExceptionHandler**</span><span class="sxs-lookup"><span data-stu-id="f1499-109">**AddVectoredExceptionHandler**</span></span>](/windows/win32/api/errhandlingapi/nf-errhandlingapi-addvectoredexceptionhandler)

    <span data-ttu-id="f1499-110">註冊向量式例外狀況處理常式。</span><span class="sxs-lookup"><span data-stu-id="f1499-110">Registers a vectored exception handler.</span></span>

-   [<span data-ttu-id="f1499-111">**GetExceptionCode**</span><span class="sxs-lookup"><span data-stu-id="f1499-111">**GetExceptionCode**</span></span>](getexceptioncode.md)

    <span data-ttu-id="f1499-112">抓取可識別發生之例外狀況類型的程式碼。</span><span class="sxs-lookup"><span data-stu-id="f1499-112">Retrieves a code that identifies the type of exception that occurred.</span></span>

-   [<span data-ttu-id="f1499-113">**GetExceptionInformation**</span><span class="sxs-lookup"><span data-stu-id="f1499-113">**GetExceptionInformation**</span></span>](getexceptioninformation.md)

    <span data-ttu-id="f1499-114">抓取與電腦無關的例外狀況描述，以及發生例外狀況時，針對執行緒所存在之電腦狀態的相關資訊。</span><span class="sxs-lookup"><span data-stu-id="f1499-114">Retrieves a machine-independent description of an exception, and information about the machine state that existed for the thread when the exception occurred.</span></span>

-   [<span data-ttu-id="f1499-115">**RaiseException**</span><span class="sxs-lookup"><span data-stu-id="f1499-115">**RaiseException**</span></span>](/windows/win32/api/errhandlingapi/nf-errhandlingapi-raiseexception)

    <span data-ttu-id="f1499-116">在呼叫執行緒中引發例外狀況。</span><span class="sxs-lookup"><span data-stu-id="f1499-116">Raises an exception in the calling thread.</span></span>

-   [<span data-ttu-id="f1499-117">**RemoveVectoredContinueHandler**</span><span class="sxs-lookup"><span data-stu-id="f1499-117">**RemoveVectoredContinueHandler**</span></span>](/windows/win32/api/errhandlingapi/nf-errhandlingapi-removevectoredcontinuehandler)

    <span data-ttu-id="f1499-118">取消註冊向量 continue 處理常式。</span><span class="sxs-lookup"><span data-stu-id="f1499-118">Unregisters a vectored continue handler.</span></span>

-   [<span data-ttu-id="f1499-119">**RemoveVectoredExceptionHandler**</span><span class="sxs-lookup"><span data-stu-id="f1499-119">**RemoveVectoredExceptionHandler**</span></span>](/windows/win32/api/errhandlingapi/nf-errhandlingapi-removevectoredexceptionhandler)

    <span data-ttu-id="f1499-120">取消註冊向量例外狀況處理常式。</span><span class="sxs-lookup"><span data-stu-id="f1499-120">Unregisters a vectored exception handler.</span></span>

-   [<span data-ttu-id="f1499-121">**RtlAddGrowableFunctionTable**</span><span class="sxs-lookup"><span data-stu-id="f1499-121">**RtlAddGrowableFunctionTable**</span></span>](/windows/desktop/api/WinNT/nf-winnt-rtladdgrowablefunctiontable)

    <span data-ttu-id="f1499-122">通知系統有動態函式資料表，代表包含程式碼的記憶體區域。</span><span class="sxs-lookup"><span data-stu-id="f1499-122">Informs the system of a dynamic function table representing a region of memory containing code.</span></span>

-   [<span data-ttu-id="f1499-123">**RtlDeleteGrowableFunctionTable**</span><span class="sxs-lookup"><span data-stu-id="f1499-123">**RtlDeleteGrowableFunctionTable**</span></span>](/windows/desktop/api/WinNT/nf-winnt-rtldeletegrowablefunctiontable)

    <span data-ttu-id="f1499-124">通知系統，先前報告的動態函式資料表已不再使用中。</span><span class="sxs-lookup"><span data-stu-id="f1499-124">Informs the system that a previously reported dynamic function table is no longer in use.</span></span>

-   [<span data-ttu-id="f1499-125">**RtlGrowFunctionTable**</span><span class="sxs-lookup"><span data-stu-id="f1499-125">**RtlGrowFunctionTable**</span></span>](/windows/desktop/api/WinNT/nf-winnt-rtlgrowfunctiontable)

    <span data-ttu-id="f1499-126">動態函式資料表大小已增加的報告。</span><span class="sxs-lookup"><span data-stu-id="f1499-126">Reports that a dynamic function table has increased in size.</span></span>

-   [<span data-ttu-id="f1499-127">**SetUnhandledExceptionFilter**</span><span class="sxs-lookup"><span data-stu-id="f1499-127">**SetUnhandledExceptionFilter**</span></span>](/windows/win32/api/errhandlingapi/nf-errhandlingapi-setunhandledexceptionfilter)

    <span data-ttu-id="f1499-128">讓應用程式取代每個執行緒和進程的最上層例外狀況處理常式。</span><span class="sxs-lookup"><span data-stu-id="f1499-128">Enables an application to supersede the top-level exception handler of each thread and process.</span></span>

-   [<span data-ttu-id="f1499-129">**UnhandledExceptionFilter**</span><span class="sxs-lookup"><span data-stu-id="f1499-129">**UnhandledExceptionFilter**</span></span>](/windows/win32/api/errhandlingapi/nf-errhandlingapi-unhandledexceptionfilter)

    <span data-ttu-id="f1499-130">如果正在調試進程，則將未處理的例外狀況傳遞至偵錯工具。</span><span class="sxs-lookup"><span data-stu-id="f1499-130">Passes unhandled exceptions to the debugger, if the process is being debugged.</span></span>

-   [<span data-ttu-id="f1499-131">**VectoredHandler**</span><span class="sxs-lookup"><span data-stu-id="f1499-131">**VectoredHandler**</span></span>](/windows/desktop/api/WinNT/nc-winnt-pvectored_exception_handler)

    <span data-ttu-id="f1499-132">應用程式定義的函數，做為向量例外狀況處理常式。</span><span class="sxs-lookup"><span data-stu-id="f1499-132">An application-defined function that serves as a vectored exception handler.</span></span>

<span data-ttu-id="f1499-133">下列函式僅適用于64位 Windows。</span><span class="sxs-lookup"><span data-stu-id="f1499-133">The following functions are used only on 64-bit Windows.</span></span>

-   [<span data-ttu-id="f1499-134">**RtlAddFunctionTable**</span><span class="sxs-lookup"><span data-stu-id="f1499-134">**RtlAddFunctionTable**</span></span>](/windows/desktop/api/WinNT/nf-winnt-rtladdfunctiontable)

    <span data-ttu-id="f1499-135">將動態函數資料表加入至動態函數資料表清單。</span><span class="sxs-lookup"><span data-stu-id="f1499-135">Adds a dynamic function table to the dynamic function table list.</span></span>

-   [<span data-ttu-id="f1499-136">**RtlCaptureCoNtext**</span><span class="sxs-lookup"><span data-stu-id="f1499-136">**RtlCaptureContext**</span></span>](/windows/desktop/api/WinNT/nf-winnt-rtlcapturecontext)

    <span data-ttu-id="f1499-137">在呼叫端的內容中捕獲內容記錄。</span><span class="sxs-lookup"><span data-stu-id="f1499-137">Retrieves a context record in the context of the caller.</span></span>

-   [<span data-ttu-id="f1499-138">**RtlDeleteFunctionTable**</span><span class="sxs-lookup"><span data-stu-id="f1499-138">**RtlDeleteFunctionTable**</span></span>](/windows/desktop/api/WinNT/nf-winnt-rtldeletefunctiontable)

    <span data-ttu-id="f1499-139">從動態函數資料表清單中移除動態函式資料表。</span><span class="sxs-lookup"><span data-stu-id="f1499-139">Removes a dynamic function table from the dynamic function table list.</span></span>

-   [<span data-ttu-id="f1499-140">**RtlInstallFunctionTableCallback**</span><span class="sxs-lookup"><span data-stu-id="f1499-140">**RtlInstallFunctionTableCallback**</span></span>](/windows/desktop/api/WinNT/nf-winnt-rtlinstallfunctiontablecallback)

    <span data-ttu-id="f1499-141">將動態函數資料表加入至動態函數資料表清單。</span><span class="sxs-lookup"><span data-stu-id="f1499-141">Adds a dynamic function table to the dynamic function table list.</span></span>

-   [<span data-ttu-id="f1499-142">**RtlRestoreCoNtext**</span><span class="sxs-lookup"><span data-stu-id="f1499-142">**RtlRestoreContext**</span></span>](/windows/desktop/api/WinNT/nf-winnt-rtlrestorecontext)

    <span data-ttu-id="f1499-143">將呼叫端的內容還原至指定的內容記錄。</span><span class="sxs-lookup"><span data-stu-id="f1499-143">Restores the context of the caller to the specified context record.</span></span>

 

 
