---
description: 指出 \_ \_ 終止處理常式的 try 區塊是否正常終止。 函數只能從 \_ \_ 終止處理常式的 finally 區塊內呼叫。
ms.assetid: 0ddaef1f-03f0-45fc-9c5e-8d6a26a73245
title: AbnormalTermination 宏
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- AbnormalTermination
api_type:
- NA
api_location: ''
ms.openlocfilehash: 7c4869f36d8ba70c8dcd8ca526949d489f455e8c
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/07/2021
ms.locfileid: "103936442"
---
# <a name="abnormaltermination-macro"></a><span data-ttu-id="d5677-104">AbnormalTermination 宏</span><span class="sxs-lookup"><span data-stu-id="d5677-104">AbnormalTermination macro</span></span>

<span data-ttu-id="d5677-105">指出終止處理常式的 **\_ \_ try** 區塊是否正常終止。</span><span class="sxs-lookup"><span data-stu-id="d5677-105">Indicates whether the **\_\_try** block of a termination handler terminated normally.</span></span> <span data-ttu-id="d5677-106">函數只能從終止處理常式的 **\_ \_ finally** 區塊內呼叫。</span><span class="sxs-lookup"><span data-stu-id="d5677-106">The function can be called only from within the **\_\_finally** block of a termination handler.</span></span>

> [!Note]  
> <span data-ttu-id="d5677-107">Microsoft C/c + + 優化編譯器會將此函式解釋為關鍵字，而在適當的例外狀況處理語法外部使用會產生編譯器錯誤。</span><span class="sxs-lookup"><span data-stu-id="d5677-107">The Microsoft C/C++ Optimizing Compiler interprets this function as a keyword, and its use outside the appropriate exception-handling syntax generates a compiler error.</span></span>

 

## <a name="syntax"></a><span data-ttu-id="d5677-108">語法</span><span class="sxs-lookup"><span data-stu-id="d5677-108">Syntax</span></span>


```C++
BOOL AbnormalTermination(void);
```



## <a name="parameters"></a><span data-ttu-id="d5677-109">參數</span><span class="sxs-lookup"><span data-stu-id="d5677-109">Parameters</span></span>

<span data-ttu-id="d5677-110">這個宏沒有任何參數。</span><span class="sxs-lookup"><span data-stu-id="d5677-110">This macro has no parameters.</span></span>

## <a name="return-value"></a><span data-ttu-id="d5677-111">傳回值</span><span class="sxs-lookup"><span data-stu-id="d5677-111">Return value</span></span>

<span data-ttu-id="d5677-112">如果 **\_ \_ try** 區塊異常終止，則傳回值為非零值。</span><span class="sxs-lookup"><span data-stu-id="d5677-112">If the **\_\_try** block terminated abnormally, the return value is nonzero.</span></span>

<span data-ttu-id="d5677-113">如果 **\_ \_ try** 區塊正常終止，則傳回值為零。</span><span class="sxs-lookup"><span data-stu-id="d5677-113">If the **\_\_try** block terminated normally, the return value is zero.</span></span>

## <a name="remarks"></a><span data-ttu-id="d5677-114">備註</span><span class="sxs-lookup"><span data-stu-id="d5677-114">Remarks</span></span>

<span data-ttu-id="d5677-115">只有在執行區塊中的最後一個語句之後，才會將 **\_ \_ try** 區塊依序結束。</span><span class="sxs-lookup"><span data-stu-id="d5677-115">The **\_\_try** block terminates normally only if execution leaves the block sequentially after executing the last statement in the block.</span></span> <span data-ttu-id="d5677-116">語句 (例如 **return**、 **goto**、 **continue** 或 **break**) 導致執行離開 **\_ \_ try** 區塊會導致區塊異常終止。</span><span class="sxs-lookup"><span data-stu-id="d5677-116">Statements (such as **return**, **goto**, **continue**, or **break**) that cause execution to leave the **\_\_try** block result in abnormal termination of the block.</span></span> <span data-ttu-id="d5677-117">即使這類的語句是 **\_ \_ try** 區塊中的最後一個語句，還是會發生這種情況。</span><span class="sxs-lookup"><span data-stu-id="d5677-117">This is the case even if such a statement is the last statement in the **\_\_try** block.</span></span>

<span data-ttu-id="d5677-118">**\_ \_ Try** 區塊的異常終止會導致系統向後搜尋所有堆疊框架，以判斷是否必須呼叫任何終止處理常式。</span><span class="sxs-lookup"><span data-stu-id="d5677-118">Abnormal termination of a **\_\_try** block causes the system to search backward through all stack frames to determine whether any termination handlers must be called.</span></span> <span data-ttu-id="d5677-119">這可能會導致執行數百個指令，因此請務必避免因 **return**、 **goto**、 **continue** 或 **break** 語句而導致 **\_ \_ try** 區塊的異常終止。</span><span class="sxs-lookup"><span data-stu-id="d5677-119">This can result in the execution of hundreds of instructions, so it is important to avoid abnormal termination of a **\_\_try** block due to a **return**, **goto**, **continue**, or **break** statement.</span></span> <span data-ttu-id="d5677-120">請注意，即使終止不正常，這些語句也不會產生例外狀況。</span><span class="sxs-lookup"><span data-stu-id="d5677-120">Note that these statements do not generate an exception, even though the termination is abnormal.</span></span>

<span data-ttu-id="d5677-121">為了避免異常終止，執行應會繼續到區塊結尾。</span><span class="sxs-lookup"><span data-stu-id="d5677-121">To avoid abnormal termination, execution should continue to the end of the block.</span></span> <span data-ttu-id="d5677-122">您也可以執行 **\_ \_ leave** 語句。</span><span class="sxs-lookup"><span data-stu-id="d5677-122">You can also execute the **\_\_leave** statement.</span></span> <span data-ttu-id="d5677-123">**\_ \_ Leave** 語句允許立即終止 **\_ \_ try** 區塊，而不會造成異常終止和其效能負面影響。</span><span class="sxs-lookup"><span data-stu-id="d5677-123">The **\_\_leave** statement allows for immediate termination of the **\_\_try** block without causing abnormal termination and its performance penalty.</span></span> <span data-ttu-id="d5677-124">請檢查您的編譯器檔，以判斷是否支援 **\_ \_ leave** 語句。</span><span class="sxs-lookup"><span data-stu-id="d5677-124">Check your compiler documentation to determine if the **\_\_leave** statement is supported.</span></span>

## <a name="requirements"></a><span data-ttu-id="d5677-125">規格需求</span><span class="sxs-lookup"><span data-stu-id="d5677-125">Requirements</span></span>



| <span data-ttu-id="d5677-126">需求</span><span class="sxs-lookup"><span data-stu-id="d5677-126">Requirement</span></span> | <span data-ttu-id="d5677-127">值</span><span class="sxs-lookup"><span data-stu-id="d5677-127">Value</span></span> |
|-------------------------------------|------------------------------------------------------|
| <span data-ttu-id="d5677-128">最低支援的用戶端</span><span class="sxs-lookup"><span data-stu-id="d5677-128">Minimum supported client</span></span><br/> | <span data-ttu-id="d5677-129">\[僅限 WINDOWS XP desktop 應用程式\]</span><span class="sxs-lookup"><span data-stu-id="d5677-129">Windows XP \[desktop apps only\]</span></span><br/>          |
| <span data-ttu-id="d5677-130">最低支援的伺服器</span><span class="sxs-lookup"><span data-stu-id="d5677-130">Minimum supported server</span></span><br/> | <span data-ttu-id="d5677-131">僅限 Windows Server 2003 \[ desktop 應用程式\]</span><span class="sxs-lookup"><span data-stu-id="d5677-131">Windows Server 2003 \[desktop apps only\]</span></span><br/> |



## <a name="see-also"></a><span data-ttu-id="d5677-132">另請參閱</span><span class="sxs-lookup"><span data-stu-id="d5677-132">See also</span></span>

<dl> <dt>

[<span data-ttu-id="d5677-133">結構化例外狀況處理函式</span><span class="sxs-lookup"><span data-stu-id="d5677-133">Structured Exception Handling Functions</span></span>](structured-exception-handling-functions.md)
</dt> <dt>

[<span data-ttu-id="d5677-134">結構化例外狀況處理總覽</span><span class="sxs-lookup"><span data-stu-id="d5677-134">Structured Exception Handling Overview</span></span>](structured-exception-handling.md)
</dt> </dl>

 

 




