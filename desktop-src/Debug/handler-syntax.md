---
description: 本節說明在 Microsoft C/c + + 優化編譯器中執行時，結構化例外狀況處理的語法和用法。 編譯器會將下列關鍵字解釋為結構化例外狀況處理機制的一部分。
ms.assetid: 22190b75-417c-49d3-83fe-546018fb61ea
title: 處理常式語法
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 411c50b8d12a74312c8b0a843ea300d23e278e88
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/07/2021
ms.locfileid: "103847072"
---
# <a name="handler-syntax"></a><span data-ttu-id="624f8-104">處理常式語法</span><span class="sxs-lookup"><span data-stu-id="624f8-104">Handler Syntax</span></span>

<span data-ttu-id="624f8-105">本節說明在 Microsoft C/c + + 優化編譯器中執行時，結構化例外狀況處理的語法和用法。</span><span class="sxs-lookup"><span data-stu-id="624f8-105">This section describes the syntax and usage of structured exception handling as implemented in the Microsoft C/C++ Optimizing Compiler.</span></span> <span data-ttu-id="624f8-106">編譯器會將下列關鍵字解釋為結構化例外狀況處理機制的一部分。</span><span class="sxs-lookup"><span data-stu-id="624f8-106">The following keywords are interpreted by the compiler as part of the structured exception-handling mechanism.</span></span>



| <span data-ttu-id="624f8-107">關鍵字</span><span class="sxs-lookup"><span data-stu-id="624f8-107">Keyword</span></span>         | <span data-ttu-id="624f8-108">描述</span><span class="sxs-lookup"><span data-stu-id="624f8-108">Description</span></span>                                                                                                                                                                                                                                      |
|-----------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="624f8-109">**\_\_嘗試**</span><span class="sxs-lookup"><span data-stu-id="624f8-109">**\_\_try**</span></span>     | <span data-ttu-id="624f8-110">開始受保護的程式碼主體。</span><span class="sxs-lookup"><span data-stu-id="624f8-110">Begins a guarded body of code.</span></span> <span data-ttu-id="624f8-111">使用 with **\_ \_ except** 關鍵字來建立例外狀況 [處理常式](exception-handler-syntax.md)，或使用 **\_ \_ finally** 關鍵字來建立 [終止處理常式](termination-handler-syntax.md)。</span><span class="sxs-lookup"><span data-stu-id="624f8-111">Used with the **\_\_except** keyword to construct an [exception handler](exception-handler-syntax.md), or with the **\_\_finally** keyword to construct a [termination handler](termination-handler-syntax.md).</span></span> |
| <span data-ttu-id="624f8-112">**\_\_除了**</span><span class="sxs-lookup"><span data-stu-id="624f8-112">**\_\_except**</span></span>  | <span data-ttu-id="624f8-113">開始程式碼區塊，此程式碼只會在其相關聯的 **\_ \_ try** 區塊中發生例外狀況時才執行。</span><span class="sxs-lookup"><span data-stu-id="624f8-113">Begins a block of code that is executed only when an exception occurs within its associated **\_\_try** block.</span></span>                                                                                                                                   |
| <span data-ttu-id="624f8-114">**\_\_最後**</span><span class="sxs-lookup"><span data-stu-id="624f8-114">**\_\_finally**</span></span> | <span data-ttu-id="624f8-115">開始一段程式碼，每當控制項的流程離開其相關聯的 **\_ \_ try** 區塊時，就會執行此程式碼區塊。</span><span class="sxs-lookup"><span data-stu-id="624f8-115">Begins a block of code that is executed whenever the flow of control leaves its associated **\_\_try** block.</span></span>                                                                                                                                    |
| <span data-ttu-id="624f8-116">**\_\_離開**</span><span class="sxs-lookup"><span data-stu-id="624f8-116">**\_\_leave**</span></span>   | <span data-ttu-id="624f8-117">允許立即終止 **\_ \_ try** 區塊，而不會造成異常終止和效能損失。</span><span class="sxs-lookup"><span data-stu-id="624f8-117">Allows for immediate termination of the **\_\_try** block without causing abnormal termination and its performance penalty.</span></span>                                                                                                                      |



 

<span data-ttu-id="624f8-118">編譯器也會將 [**GetExceptionCode**](getexceptioncode.md)、 [**GetExceptionInformation**](getexceptioninformation.md)和 [**AbnormalTermination**](abnormaltermination.md) 函式解釋為關鍵字，而在適當的例外狀況處理語法外部使用，會產生編譯器錯誤。</span><span class="sxs-lookup"><span data-stu-id="624f8-118">The compiler also interprets the [**GetExceptionCode**](getexceptioncode.md), [**GetExceptionInformation**](getexceptioninformation.md), and [**AbnormalTermination**](abnormaltermination.md) functions as keywords, and their use outside the appropriate exception-handling syntax generates a compiler error.</span></span> <span data-ttu-id="624f8-119">以下是這些函數的簡短說明。</span><span class="sxs-lookup"><span data-stu-id="624f8-119">The following are brief descriptions of these functions.</span></span>



| <span data-ttu-id="624f8-120">函式</span><span class="sxs-lookup"><span data-stu-id="624f8-120">Function</span></span>                                                   | <span data-ttu-id="624f8-121">描述</span><span class="sxs-lookup"><span data-stu-id="624f8-121">Description</span></span>                                                                                                                                                                                                                                             |
|------------------------------------------------------------|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [<span data-ttu-id="624f8-122">**GetExceptionCode**</span><span class="sxs-lookup"><span data-stu-id="624f8-122">**GetExceptionCode**</span></span>](getexceptioncode.md)               | <span data-ttu-id="624f8-123">傳回識別例外狀況類型的代碼。</span><span class="sxs-lookup"><span data-stu-id="624f8-123">Returns a code that identifies the type of exception.</span></span> <span data-ttu-id="624f8-124">您只能從篩選運算式或例外狀況處理常式區塊內呼叫這個函數。</span><span class="sxs-lookup"><span data-stu-id="624f8-124">This function can be called only from within the filter expression or the exception-handler block.</span></span>                                                                                                |
| [<span data-ttu-id="624f8-125">**GetExceptionInformation**</span><span class="sxs-lookup"><span data-stu-id="624f8-125">**GetExceptionInformation**</span></span>](getexceptioninformation.md) | <span data-ttu-id="624f8-126">傳回 [**例外狀況 \_ 指標**](/windows/desktop/api/WinNT/ns-winnt-exception_pointers) 結構的指標，其中包含內容記錄的指標和例外狀況記錄。</span><span class="sxs-lookup"><span data-stu-id="624f8-126">Returns a pointer to an [**EXCEPTION\_POINTERS**](/windows/desktop/api/WinNT/ns-winnt-exception_pointers) structure containing pointers to the context record and the exception record.</span></span> <span data-ttu-id="624f8-127">您只能從例外狀況處理常式的篩選運算式內呼叫這個函數。</span><span class="sxs-lookup"><span data-stu-id="624f8-127">This function can be called only from within the filter expression of an exception handler.</span></span> |
| [<span data-ttu-id="624f8-128">**AbnormalTermination**</span><span class="sxs-lookup"><span data-stu-id="624f8-128">**AbnormalTermination**</span></span>](abnormaltermination.md)         | <span data-ttu-id="624f8-129">指出在執行區塊中的最後一個語句之後，控制項的流程是否會依序離開相關聯的 **\_ \_ try** 區塊。</span><span class="sxs-lookup"><span data-stu-id="624f8-129">Indicates whether the flow of control left the associated **\_\_try** block sequentially after executing the last statement in the block.</span></span> <span data-ttu-id="624f8-130">您只能從終止處理常式的 **\_ \_ finally** 區塊內呼叫這個函數。</span><span class="sxs-lookup"><span data-stu-id="624f8-130">This function can be called only from within the **\_\_finally** block of a termination handler.</span></span>              |



 

 

 



