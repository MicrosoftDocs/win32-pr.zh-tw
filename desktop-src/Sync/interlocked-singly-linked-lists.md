---
description: 連鎖的單向連結清單 (SList) 可簡化從連結清單插入和刪除的工作。
ms.assetid: 35463ace-33ab-4eb9-9901-2504a92456e2
title: 連鎖單向連結清單
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 9af39847fa2fd1b1873c661d6ec904783e0139b9
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/08/2021
ms.locfileid: "106980563"
---
# <a name="interlocked-singly-linked-lists"></a><span data-ttu-id="e92cb-103">連鎖單向連結清單</span><span class="sxs-lookup"><span data-stu-id="e92cb-103">Interlocked Singly Linked Lists</span></span>

<span data-ttu-id="e92cb-104">*連鎖的單向連結清單* (SList) 可簡化從連結清單插入和刪除的工作。</span><span class="sxs-lookup"><span data-stu-id="e92cb-104">An *interlocked singly linked list* (SList) eases the task of insertion and deletion from a linked list.</span></span> <span data-ttu-id="e92cb-105">SLists 是使用非封鎖演算法來執行，以提供不可部分完成的同步處理、提高系統效能，並避免發生優先順序反轉和鎖定群組等問題。</span><span class="sxs-lookup"><span data-stu-id="e92cb-105">SLists are implemented using a nonblocking algorithm to provide atomic synchronization, increase system performance, and avoid problems such as priority inversion and lock convoys.</span></span>

<span data-ttu-id="e92cb-106">SLists 可直接在32位程式碼中執行和使用。</span><span class="sxs-lookup"><span data-stu-id="e92cb-106">SLists are straightforward to implement and use in 32-bit code.</span></span> <span data-ttu-id="e92cb-107">不過，在64位程式碼中執行它們是很困難的，因為原生連鎖交換基本專案所交換的資料量不是位址大小的兩倍，因為它是在32位程式碼中。</span><span class="sxs-lookup"><span data-stu-id="e92cb-107">However, it is challenging to implement them in 64-bit code because the amount of data exchangeable by the native interlocked exchange primitives is not double the address size, as it is in 32-bit code.</span></span> <span data-ttu-id="e92cb-108">因此，SLists 可以將高階可調整演算法移植到 Windows。</span><span class="sxs-lookup"><span data-stu-id="e92cb-108">Therefore, SLists enable porting high-end scalable algorithms to Windows.</span></span>

<span data-ttu-id="e92cb-109">**Windows 8：** 從 Windows 8 開始，適當的原生連鎖交換基本專案適用于64位程式碼，例如 [**InterlockedCompare64Exchange128**](/previous-versions/windows/desktop/legacy/ms683553(v=vs.85))。</span><span class="sxs-lookup"><span data-stu-id="e92cb-109">**Windows 8:** Starting in Windows 8 the appropriate native interlocked exchange primitives are available for 64-bit code, for example [**InterlockedCompare64Exchange128**](/previous-versions/windows/desktop/legacy/ms683553(v=vs.85)).</span></span>

<span data-ttu-id="e92cb-110">應用程式可以透過呼叫 [**InitializeSListHead**](/windows/win32/api/interlockedapi/nf-interlockedapi-initializeslisthead) 函式來初始化清單的開頭，以使用 SLists。</span><span class="sxs-lookup"><span data-stu-id="e92cb-110">Applications can use SLists by calling the [**InitializeSListHead**](/windows/win32/api/interlockedapi/nf-interlockedapi-initializeslisthead) function to initialize the head of the list.</span></span> <span data-ttu-id="e92cb-111">若要將專案插入清單中，請使用 [**InterlockedPushEntrySList**](/windows/win32/api/interlockedapi/nf-interlockedapi-interlockedpushentryslist) 函數。</span><span class="sxs-lookup"><span data-stu-id="e92cb-111">To insert items into the list, use the [**InterlockedPushEntrySList**](/windows/win32/api/interlockedapi/nf-interlockedapi-interlockedpushentryslist) function.</span></span> <span data-ttu-id="e92cb-112">若要從清單中刪除專案，請使用 [**InterlockedPopEntrySList**](/windows/win32/api/interlockedapi/nf-interlockedapi-interlockedpopentryslist) 函數。</span><span class="sxs-lookup"><span data-stu-id="e92cb-112">To delete items from the list, use the [**InterlockedPopEntrySList**](/windows/win32/api/interlockedapi/nf-interlockedapi-interlockedpopentryslist) function.</span></span>

<span data-ttu-id="e92cb-113">所有清單專案都必須在 **記憶體 \_ 配置 \_ 對齊** 界限上對齊。</span><span class="sxs-lookup"><span data-stu-id="e92cb-113">All list items must be aligned on a **MEMORY\_ALLOCATION\_ALIGNMENT** boundary.</span></span> <span data-ttu-id="e92cb-114">未對齊的專案可能會導致無法預期的結果。</span><span class="sxs-lookup"><span data-stu-id="e92cb-114">Unaligned items can cause unpredictable results.</span></span> <span data-ttu-id="e92cb-115">請參閱 **\_ 對齊的 \_ malloc**。</span><span class="sxs-lookup"><span data-stu-id="e92cb-115">See **\_aligned\_malloc**.</span></span>

<span data-ttu-id="e92cb-116">如需範例，請參閱 [使用單一連結清單](using-singly-linked-lists.md)。</span><span class="sxs-lookup"><span data-stu-id="e92cb-116">For an example, see [Using Singly Linked Lists](using-singly-linked-lists.md).</span></span>

<span data-ttu-id="e92cb-117">下表列出 SList 函數。</span><span class="sxs-lookup"><span data-stu-id="e92cb-117">The following table lists the SList functions.</span></span>



| <span data-ttu-id="e92cb-118">函式</span><span class="sxs-lookup"><span data-stu-id="e92cb-118">Function</span></span>                                                         | <span data-ttu-id="e92cb-119">描述</span><span class="sxs-lookup"><span data-stu-id="e92cb-119">Description</span></span>                                                                                                                                               |
|------------------------------------------------------------------|-----------------------------------------------------------------------------------------------------------------------------------------------------------|
| [<span data-ttu-id="e92cb-120">**InitializeSListHead**</span><span class="sxs-lookup"><span data-stu-id="e92cb-120">**InitializeSListHead**</span></span>](/windows/win32/api/interlockedapi/nf-interlockedapi-initializeslisthead)               | <span data-ttu-id="e92cb-121">初始化單一連結清單的標頭。</span><span class="sxs-lookup"><span data-stu-id="e92cb-121">Initializes the head of a singly linked list.</span></span>                                                                                                             |
| [<span data-ttu-id="e92cb-122">**InterlockedFlushSList**</span><span class="sxs-lookup"><span data-stu-id="e92cb-122">**InterlockedFlushSList**</span></span>](/windows/win32/api/interlockedapi/nf-interlockedapi-interlockedflushslist)           | <span data-ttu-id="e92cb-123">清除單一連結清單中的整個專案清單。</span><span class="sxs-lookup"><span data-stu-id="e92cb-123">Flushes the entire list of items in a singly linked list.</span></span>                                                                                                 |
| [<span data-ttu-id="e92cb-124">**InterlockedPopEntrySList**</span><span class="sxs-lookup"><span data-stu-id="e92cb-124">**InterlockedPopEntrySList**</span></span>](/windows/win32/api/interlockedapi/nf-interlockedapi-interlockedpopentryslist)     | <span data-ttu-id="e92cb-125">移除單一連結清單前面的專案。</span><span class="sxs-lookup"><span data-stu-id="e92cb-125">Removes an item from the front of a singly linked list.</span></span>                                                                                                   |
| [<span data-ttu-id="e92cb-126">**InterlockedPushEntrySList**</span><span class="sxs-lookup"><span data-stu-id="e92cb-126">**InterlockedPushEntrySList**</span></span>](/windows/win32/api/interlockedapi/nf-interlockedapi-interlockedpushentryslist)   | <span data-ttu-id="e92cb-127">將專案插入單向連結清單的前面。</span><span class="sxs-lookup"><span data-stu-id="e92cb-127">Inserts an item at the front of a singly linked list.</span></span>                                                                                                     |
| <span data-ttu-id="e92cb-128">[**InterlockedPushListSList**](/previous-versions/windows/desktop/legacy/hh448545(v=vs.85))</span><span class="sxs-lookup"><span data-stu-id="e92cb-128">[**InterlockedPushListSList**](/previous-versions/windows/desktop/legacy/hh448545(v=vs.85))</span></span>     | <span data-ttu-id="e92cb-129">在另一個單一連結清單的前方插入單一連結清單。</span><span class="sxs-lookup"><span data-stu-id="e92cb-129">Inserts a singly-linked list at the front of another singly linked list.</span></span>                                                                                  |
| [<span data-ttu-id="e92cb-130">**InterlockedPushListSListEx**</span><span class="sxs-lookup"><span data-stu-id="e92cb-130">**InterlockedPushListSListEx**</span></span>](/windows/desktop/api/interlockedapi/nf-interlockedapi-interlockedpushlistslistex) | <span data-ttu-id="e92cb-131">在另一個單一連結清單的前方插入單一連結清單。</span><span class="sxs-lookup"><span data-stu-id="e92cb-131">Inserts a singly-linked list at the front of another singly linked list.</span></span> <span data-ttu-id="e92cb-132">此版本的方法不會使用 **\_ \_ fastcall** 呼叫慣例。</span><span class="sxs-lookup"><span data-stu-id="e92cb-132">This version of the method does not use the **\_\_fastcall** calling convention.</span></span> |
| [<span data-ttu-id="e92cb-133">**RtlFirstEntrySList**</span><span class="sxs-lookup"><span data-stu-id="e92cb-133">**RtlFirstEntrySList**</span></span>](/windows/desktop/api/WinNT/nf-winnt-rtlfirstentryslist)                 | <span data-ttu-id="e92cb-134">抓取單一連結清單中的第一個專案。</span><span class="sxs-lookup"><span data-stu-id="e92cb-134">Retrieves the first entry in a singly linked list.</span></span>                                                                                                        |
| [<span data-ttu-id="e92cb-135">**QueryDepthSList**</span><span class="sxs-lookup"><span data-stu-id="e92cb-135">**QueryDepthSList**</span></span>](/windows/win32/api/interlockedapi/nf-interlockedapi-querydepthslist)                       | <span data-ttu-id="e92cb-136">抓取指定的單向連結清單中的專案數。</span><span class="sxs-lookup"><span data-stu-id="e92cb-136">Retrieves the number of entries in the specified singly linked list.</span></span>                                                                                      |



 

 

 
