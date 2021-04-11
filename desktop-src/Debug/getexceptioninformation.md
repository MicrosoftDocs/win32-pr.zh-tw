---
description: 抓取與電腦無關的例外狀況描述，以及發生例外狀況時，執行緒存在的電腦狀態相關資訊。 您只能從例外狀況處理常式的篩選運算式內呼叫這個函數。
ms.assetid: e982794a-d5f1-4fb4-a2b9-aa8da18cb8ae
title: GetExceptionInformation 宏
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- GetExceptionInformation
api_type:
- NA
api_location: ''
ms.openlocfilehash: 243831a94a26b86df29d3a50413bfa9d6830a0e3
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/07/2021
ms.locfileid: "103689123"
---
# <a name="getexceptioninformation-macro"></a><span data-ttu-id="95d57-104">GetExceptionInformation 宏</span><span class="sxs-lookup"><span data-stu-id="95d57-104">GetExceptionInformation macro</span></span>

<span data-ttu-id="95d57-105">抓取與電腦無關的例外狀況描述，以及發生例外狀況時，執行緒存在的電腦狀態相關資訊。</span><span class="sxs-lookup"><span data-stu-id="95d57-105">Retrieves a computer-independent description of an exception, and information about the computer state that exists for the thread when the exception occurs.</span></span> <span data-ttu-id="95d57-106">您只能從例外狀況處理常式的篩選運算式內呼叫這個函數。</span><span class="sxs-lookup"><span data-stu-id="95d57-106">This function can be called only from within the filter expression of an exception handler.</span></span>

> [!Note]  
> <span data-ttu-id="95d57-107">Microsoft C/c + + 優化編譯器會將此函式解釋為關鍵字，而在適當的例外狀況處理語法外部使用會產生編譯器錯誤。</span><span class="sxs-lookup"><span data-stu-id="95d57-107">The Microsoft C/C++ Optimizing Compiler interprets this function as a keyword, and its use outside the appropriate exception-handling syntax generates a compiler error.</span></span>

 

## <a name="syntax"></a><span data-ttu-id="95d57-108">語法</span><span class="sxs-lookup"><span data-stu-id="95d57-108">Syntax</span></span>


```C++
LPEXCEPTION_POINTERS GetExceptionInformation(void);
```



## <a name="parameters"></a><span data-ttu-id="95d57-109">參數</span><span class="sxs-lookup"><span data-stu-id="95d57-109">Parameters</span></span>

<span data-ttu-id="95d57-110">這個宏沒有任何參數。</span><span class="sxs-lookup"><span data-stu-id="95d57-110">This macro has no parameters.</span></span>

## <a name="return-value"></a><span data-ttu-id="95d57-111">傳回值</span><span class="sxs-lookup"><span data-stu-id="95d57-111">Return value</span></span>

<span data-ttu-id="95d57-112">[**例外狀況 \_ 指標**](/windows/desktop/api/WinNT/ns-winnt-exception_pointers)結構的指標，其中包含下列兩個結構的指標：</span><span class="sxs-lookup"><span data-stu-id="95d57-112">A pointer to an [**EXCEPTION\_POINTERS**](/windows/desktop/api/WinNT/ns-winnt-exception_pointers) structure that contains pointers to the following two structures:</span></span>

-   <span data-ttu-id="95d57-113">[**例外 \_ 狀況**](/windows/desktop/api/WinNT/ns-winnt-exception_record) 包含例外狀況描述的記錄結構。</span><span class="sxs-lookup"><span data-stu-id="95d57-113">[**EXCEPTION\_RECORD**](/windows/desktop/api/WinNT/ns-winnt-exception_record) structure that contains a description of the exception.</span></span>
-   <span data-ttu-id="95d57-114">包含電腦狀態資訊的 [**內容**](/windows/desktop/api/WinNT/ns-winnt-arm64_nt_context)結構。</span><span class="sxs-lookup"><span data-stu-id="95d57-114">[**CONTEXT**](/windows/desktop/api/WinNT/ns-winnt-arm64_nt_context) structure that contains the computer state information.</span></span>

## <a name="remarks"></a><span data-ttu-id="95d57-115">備註</span><span class="sxs-lookup"><span data-stu-id="95d57-115">Remarks</span></span>

<span data-ttu-id="95d57-116">用來呼叫函式的篩選運算式 () 如果在 **\_ \_ try** 區塊執行期間發生例外狀況，則會進行評估，而且它會判斷 **\_ \_ except** 區塊是否執行。</span><span class="sxs-lookup"><span data-stu-id="95d57-116">The filter expression (from which the function is called) is evaluated if an exception occurs during execution of the **\_\_try** block, and it determines whether or not the **\_\_except** block is executed.</span></span>

<span data-ttu-id="95d57-117">篩選運算式可以叫用篩選函數。</span><span class="sxs-lookup"><span data-stu-id="95d57-117">The filter expression can invoke a filter function.</span></span> <span data-ttu-id="95d57-118">篩選函數無法呼叫 **GetExceptionInformation**。</span><span class="sxs-lookup"><span data-stu-id="95d57-118">The filter function cannot call **GetExceptionInformation**.</span></span> <span data-ttu-id="95d57-119">不過， **GetExceptionInformation** 的傳回值可以做為參數傳遞至篩選函數。</span><span class="sxs-lookup"><span data-stu-id="95d57-119">However, the return value of **GetExceptionInformation** can be passed as a parameter to a filter function.</span></span>

<span data-ttu-id="95d57-120">若要將 [**例外狀況 \_ 指標**](/windows/desktop/api/WinNT/ns-winnt-exception_pointers) 資訊傳遞給例外狀況處理常式區塊，篩選運算式或篩選函數必須將指標或資料複製到可供處理常式稍後存取的安全儲存區。</span><span class="sxs-lookup"><span data-stu-id="95d57-120">To pass the [**EXCEPTION\_POINTERS**](/windows/desktop/api/WinNT/ns-winnt-exception_pointers) information to the exception-handler block, the filter expression or filter function must copy the pointer or the data to safe storage that the handler can later access.</span></span>

<span data-ttu-id="95d57-121">在嵌套處理常式的情況下，會評估每個篩選運算式，直到一個評估為 **例外狀況 \_ 執行 \_ 處理常式** 或 **例外狀況 \_ 繼續 \_ 執行** 為止。</span><span class="sxs-lookup"><span data-stu-id="95d57-121">In the case of nested handlers, each filter expression is evaluated until one is evaluated as **EXCEPTION\_EXECUTE\_HANDLER** or **EXCEPTION\_CONTINUE\_EXECUTION**.</span></span> <span data-ttu-id="95d57-122">每個篩選運算式都可以叫用 **GetExceptionInformation** 來取得例外狀況資訊。</span><span class="sxs-lookup"><span data-stu-id="95d57-122">Each filter expression can invoke **GetExceptionInformation** to get exception information.</span></span>

## <a name="requirements"></a><span data-ttu-id="95d57-123">規格需求</span><span class="sxs-lookup"><span data-stu-id="95d57-123">Requirements</span></span>



| <span data-ttu-id="95d57-124">需求</span><span class="sxs-lookup"><span data-stu-id="95d57-124">Requirement</span></span> | <span data-ttu-id="95d57-125">值</span><span class="sxs-lookup"><span data-stu-id="95d57-125">Value</span></span> |
|-------------------------------------|------------------------------------------------------|
| <span data-ttu-id="95d57-126">最低支援的用戶端</span><span class="sxs-lookup"><span data-stu-id="95d57-126">Minimum supported client</span></span><br/> | <span data-ttu-id="95d57-127">\[僅限 WINDOWS XP desktop 應用程式\]</span><span class="sxs-lookup"><span data-stu-id="95d57-127">Windows XP \[desktop apps only\]</span></span><br/>          |
| <span data-ttu-id="95d57-128">最低支援的伺服器</span><span class="sxs-lookup"><span data-stu-id="95d57-128">Minimum supported server</span></span><br/> | <span data-ttu-id="95d57-129">僅限 Windows Server 2003 \[ desktop 應用程式\]</span><span class="sxs-lookup"><span data-stu-id="95d57-129">Windows Server 2003 \[desktop apps only\]</span></span><br/> |



## <a name="see-also"></a><span data-ttu-id="95d57-130">另請參閱</span><span class="sxs-lookup"><span data-stu-id="95d57-130">See also</span></span>

<dl> <dt>

[<span data-ttu-id="95d57-131">**上下文**</span><span class="sxs-lookup"><span data-stu-id="95d57-131">**CONTEXT**</span></span>](/windows/desktop/api/WinNT/ns-winnt-arm64_nt_context)
</dt> <dt>

[<span data-ttu-id="95d57-132">**例外狀況 \_ 指標**</span><span class="sxs-lookup"><span data-stu-id="95d57-132">**EXCEPTION\_POINTERS**</span></span>](/windows/desktop/api/WinNT/ns-winnt-exception_pointers)
</dt> <dt>

[<span data-ttu-id="95d57-133">**例外狀況 \_ 記錄**</span><span class="sxs-lookup"><span data-stu-id="95d57-133">**EXCEPTION\_RECORD**</span></span>](/windows/desktop/api/WinNT/ns-winnt-exception_record)
</dt> <dt>

[<span data-ttu-id="95d57-134">**GetExceptionCode**</span><span class="sxs-lookup"><span data-stu-id="95d57-134">**GetExceptionCode**</span></span>](getexceptioncode.md)
</dt> <dt>

[<span data-ttu-id="95d57-135">**GetXStateFeaturesMask**</span><span class="sxs-lookup"><span data-stu-id="95d57-135">**GetXStateFeaturesMask**</span></span>](/windows/desktop/api/WinBase/nf-winbase-getxstatefeaturesmask)
</dt> <dt>

[<span data-ttu-id="95d57-136">結構化例外狀況處理函式</span><span class="sxs-lookup"><span data-stu-id="95d57-136">Structured Exception Handling Functions</span></span>](structured-exception-handling-functions.md)
</dt> <dt>

[<span data-ttu-id="95d57-137">結構化例外狀況處理總覽</span><span class="sxs-lookup"><span data-stu-id="95d57-137">Structured Exception Handling Overview</span></span>](structured-exception-handling.md)
</dt> <dt>

[<span data-ttu-id="95d57-138">啟用 Intel AVX 的 Windows 支援</span><span class="sxs-lookup"><span data-stu-id="95d57-138">Enable Windows Support for Intel AVX</span></span>](../win7appqual/enable-windows-7-support-for-intel-avx.md)
</dt> </dl>

 

 
