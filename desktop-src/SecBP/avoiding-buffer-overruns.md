---
description: 提供一些緩衝區溢位情況的簡介，並提供一些構想和資源，協助您避免建立新的風險並減輕現有的風險。
ms.assetid: 713fd6de-16af-49d2-8940-763c4a6e414b
title: 避免緩衝區溢位
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 3c8a3456384e799380fa0041172fb2b2ea09c0c3
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/08/2021
ms.locfileid: "106990354"
---
# <a name="avoiding-buffer-overruns"></a><span data-ttu-id="f6d8d-103">避免緩衝區溢位</span><span class="sxs-lookup"><span data-stu-id="f6d8d-103">Avoiding Buffer Overruns</span></span>

<span data-ttu-id="f6d8d-104">緩衝區溢位是最常見的安全性風險來源之一。</span><span class="sxs-lookup"><span data-stu-id="f6d8d-104">A buffer overrun is one of the most common sources of security risk.</span></span> <span data-ttu-id="f6d8d-105">緩衝區溢位的原因基本上是將未選取的外部輸入視為值得信任的資料。</span><span class="sxs-lookup"><span data-stu-id="f6d8d-105">A buffer overrun is essentially caused by treating unchecked, external input as trustworthy data.</span></span> <span data-ttu-id="f6d8d-106">使用 [**CopyMemory**](/previous-versions/windows/desktop/legacy/aa366535(v=vs.85))、 **strcat**、 **strcpy** 或 **wcscpy** 等作業來複製此資料的動作，可能會產生非預期的結果，以允許系統損毀。</span><span class="sxs-lookup"><span data-stu-id="f6d8d-106">The act of copying this data, using operations such as [**CopyMemory**](/previous-versions/windows/desktop/legacy/aa366535(v=vs.85)), **strcat**, **strcpy**, or **wcscpy**, can create unanticipated results, which allows for system corruption.</span></span> <span data-ttu-id="f6d8d-107">在最佳情況下，您的應用程式將會中止，併發生核心傾印、分割錯誤或存取違規。</span><span class="sxs-lookup"><span data-stu-id="f6d8d-107">In the best of cases, your application will abort with a core dump, segmentation fault, or access violation.</span></span> <span data-ttu-id="f6d8d-108">在最糟的情況下，攻擊者可以在您的程式中引進和執行其他惡意程式碼，以利用緩衝區溢位。</span><span class="sxs-lookup"><span data-stu-id="f6d8d-108">In the worst of cases, an attacker can exploit the buffer overrun by introducing and executing other malicious code in your process.</span></span> <span data-ttu-id="f6d8d-109">將未選取的輸入資料複製到以堆疊為基礎的緩衝區是可被利用的錯誤最常見的原因。</span><span class="sxs-lookup"><span data-stu-id="f6d8d-109">Copying unchecked, input data into a stack-based buffer is the most common cause of exploitable faults.</span></span>

<span data-ttu-id="f6d8d-110">緩衝區溢位可能會以各種不同的方式發生。</span><span class="sxs-lookup"><span data-stu-id="f6d8d-110">Buffer overruns can occur in a variety of ways.</span></span> <span data-ttu-id="f6d8d-111">下列清單提供一些緩衝區溢位情況的簡介，並提供一些構想和資源，協助您避免建立新的風險並減輕現有的風險：</span><span class="sxs-lookup"><span data-stu-id="f6d8d-111">The following list provides a brief introduction to a few types of buffer overrun situations and offers some ideas and resources to help you avoid creating new risks and mitigate existing ones:</span></span>

<dl> <dt>

<span data-ttu-id="f6d8d-112"><span id="Static_buffer_overruns"></span><span id="static_buffer_overruns"></span><span id="STATIC_BUFFER_OVERRUNS"></span>靜態緩衝區溢出</span><span class="sxs-lookup"><span data-stu-id="f6d8d-112"><span id="Static_buffer_overruns"></span><span id="static_buffer_overruns"></span><span id="STATIC_BUFFER_OVERRUNS"></span>Static buffer overruns</span></span>
</dt> <dd>

<span data-ttu-id="f6d8d-113">當已在堆疊上宣告的緩衝區寫入的資料量超過配置用來保存的緩衝區時，就會發生靜態緩衝區溢出。</span><span class="sxs-lookup"><span data-stu-id="f6d8d-113">A static buffer overrun occurs when a buffer, which has been declared on the stack, is written to with more data than it was allocated to hold.</span></span> <span data-ttu-id="f6d8d-114">當未驗證的使用者輸入資料直接複製到靜態變數時，會發生此錯誤的較不明顯版本，進而造成潛在的堆疊損毀。</span><span class="sxs-lookup"><span data-stu-id="f6d8d-114">The less apparent versions of this error occur when unverified user input data is copied directly to a static variable, causing potential stack corruption.</span></span>

</dd> <dt>

<span data-ttu-id="f6d8d-115"><span id="Heap_overruns"></span><span id="heap_overruns"></span><span id="HEAP_OVERRUNS"></span>堆積溢出</span><span class="sxs-lookup"><span data-stu-id="f6d8d-115"><span id="Heap_overruns"></span><span id="heap_overruns"></span><span id="HEAP_OVERRUNS"></span>Heap overruns</span></span>
</dt> <dd>

<span data-ttu-id="f6d8d-116">堆積溢出（例如靜態緩衝區溢出）可能會導致記憶體和堆疊損毀。</span><span class="sxs-lookup"><span data-stu-id="f6d8d-116">Heap overruns, like static buffer overruns, can lead to memory and stack corruption.</span></span> <span data-ttu-id="f6d8d-117">由於堆積溢出發生在堆積記憶體中，而不是在堆疊上，有些人認為它們比較不能造成嚴重的問題;然而，堆積溢出需要真正的程式設計護理，而且能夠讓系統的風險成為靜態緩衝區溢出。</span><span class="sxs-lookup"><span data-stu-id="f6d8d-117">Because heap overruns occur in heap memory rather than on the stack, some people consider them to be less able to cause serious problems; nevertheless, heap overruns require real programming care and are just as able to allow system risks as static buffer overruns.</span></span>

</dd> <dt>

<span data-ttu-id="f6d8d-118"><span id="Array_indexing_errors"></span><span id="array_indexing_errors"></span><span id="ARRAY_INDEXING_ERRORS"></span>陣列索引錯誤</span><span class="sxs-lookup"><span data-stu-id="f6d8d-118"><span id="Array_indexing_errors"></span><span id="array_indexing_errors"></span><span id="ARRAY_INDEXING_ERRORS"></span>Array indexing errors</span></span>
</dt> <dd>

<span data-ttu-id="f6d8d-119">陣列索引錯誤也是記憶體溢出的來源。</span><span class="sxs-lookup"><span data-stu-id="f6d8d-119">Array indexing errors also are a source of memory overruns.</span></span> <span data-ttu-id="f6d8d-120">謹慎的界限檢查和索引管理將有助於防止這種類型的記憶體溢出。</span><span class="sxs-lookup"><span data-stu-id="f6d8d-120">Careful bounds checking and index management will help prevent this type of memory overrun.</span></span>

</dd> </dl>

<span data-ttu-id="f6d8d-121">避免緩衝區溢位主要是關於撰寫良好的程式碼。</span><span class="sxs-lookup"><span data-stu-id="f6d8d-121">Preventing buffer overruns is primarily about writing good code.</span></span> <span data-ttu-id="f6d8d-122">請一律驗證所有輸入，並在必要時正常失敗。</span><span class="sxs-lookup"><span data-stu-id="f6d8d-122">Always validate all your inputs and fail gracefully when necessary.</span></span> <span data-ttu-id="f6d8d-123">如需撰寫安全程式碼的詳細資訊，請參閱下列資源：</span><span class="sxs-lookup"><span data-stu-id="f6d8d-123">For more information about writing secure code, see the following resources:</span></span>

-   <span data-ttu-id="f6d8d-124">Maguire、Steve \[ 1993 \] 、 *撰寫穩固* 的程式碼、ISBN 1-55615-551-4、Microsoft 按壓、Redmond、華盛頓州。</span><span class="sxs-lookup"><span data-stu-id="f6d8d-124">Maguire, Steve \[1993\], *Writing Solid Code*, ISBN 1-55615-551-4, Microsoft Press, Redmond, Washington.</span></span>
-   <span data-ttu-id="f6d8d-125">Howard、Michael 和 LeBlanc、David \[ 2003 \] 、 *撰寫安全* 的程式碼、2d ed、ISBN 0-7356-1722-8、Microsoft 按壓、Redmond、華盛頓州。</span><span class="sxs-lookup"><span data-stu-id="f6d8d-125">Howard, Michael and LeBlanc, David \[2003\], *Writing Secure Code*, 2d ed., ISBN 0-7356-1722-8, Microsoft Press, Redmond, Washington.</span></span>

> [!Note]  
> <span data-ttu-id="f6d8d-126">某些語言和國家/地區可能無法使用這些資源。</span><span class="sxs-lookup"><span data-stu-id="f6d8d-126">These resources may not be available in some languages and countries.</span></span>

 

<span data-ttu-id="f6d8d-127">安全字串處理是一種長期的問題，可繼續透過下列良好的程式設計實務來解決這兩個問題，而且通常會使用安全的字串處理函式來修整現有的系統。</span><span class="sxs-lookup"><span data-stu-id="f6d8d-127">Safe string handling is a long-standing issue that continues to be addressed both by following good programming practices and often by using and retrofitting existing systems with secure, string-handling functions.</span></span> <span data-ttu-id="f6d8d-128">適用于 Windows shell 的這類一組函式範例會以 [**StringCbCat**](/windows/win32/api/strsafe/nf-strsafe-stringcbcata)開始。</span><span class="sxs-lookup"><span data-stu-id="f6d8d-128">An example of such a set of functions for the Windows shell starts with [**StringCbCat**](/windows/win32/api/strsafe/nf-strsafe-stringcbcata).</span></span>

 

 
