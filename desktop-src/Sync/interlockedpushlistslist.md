---
UID: ''
title: InterlockedPushListSList 函式
description: 在另一個單一連結清單的前方插入單一連結清單。
old-location: ''
ms.assetid: na
ms.date: 04/10/2019
ms.keywords: InterlockedPushListSListEx
ms.topic: reference
req.header:
- WinBase.h on Windows Vista, Windows 7, Windows Server 2008 and Windows Server 2008 R2
- InterlockedAPI.h on Windows 8 and Windows Server 2012
req.include-header: Windows.h
req.target-type: Windows
req.target-min-winverclnt: Windows Vista [desktop apps only]
req.target-min-winversvr: Windows Server 2008 [desktop apps only]
req.kmdf-ver: ''
req.umdf-ver: ''
req.ddi-compliance: ''
req.unicode-ansi: ''
req.idl: ''
req.max-support: ''
req.namespace: ''
req.assembly: ''
req.type-library: ''
req.lib: Kernel32.lib
req.dll: API-MS-Win-Core-interlocked-l1-1-0.dll
req.irql: ''
topic_type:
- APIRef
api_type: ''
api_location:
- API-MS-Win-Core-interlocked-l1-1-0.dll
api_name:
- InterlockedPushListSList
targetos: Windows
req.typenames: ''
req.redist: ''
ms.openlocfilehash: ccecdae3af5119a86594c31856dac11ecb4507bc
ms.sourcegitcommit: be77ed1f97d3be57a2f42070589de21b66034adf
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 05/29/2020
ms.locfileid: "104374836"
---
# <a name="interlockedpushlistslist-function"></a><span data-ttu-id="020f8-103">InterlockedPushListSList 函式</span><span class="sxs-lookup"><span data-stu-id="020f8-103">InterlockedPushListSList function</span></span>

## <a name="description"></a><span data-ttu-id="020f8-104">Description</span><span class="sxs-lookup"><span data-stu-id="020f8-104">Description</span></span>

<span data-ttu-id="020f8-105">在另一個單一連結清單的前方插入單一連結清單。</span><span class="sxs-lookup"><span data-stu-id="020f8-105">Inserts a singly-linked list at the front of another singly linked list.</span></span>
<span data-ttu-id="020f8-106">系統會在多處理器系統上同步處理清單的存取。</span><span class="sxs-lookup"><span data-stu-id="020f8-106">Access to the lists is synchronized on a multiprocessor system.</span></span>

```cpp
PSLIST_ENTRY  FASTCALL InterlockedPushListSList(
  _Inout_ PSLIST_HEADER ListHead,
  _Inout_ PSLIST_ENTRY  List,
  _Inout_ PSLIST_ENTRY  ListEnd,
  _In_    ULONG         Count
);
```

## <a name="parameters"></a><span data-ttu-id="020f8-107">參數</span><span class="sxs-lookup"><span data-stu-id="020f8-107">Parameters</span></span>

### <a name="listhead-in-out"></a><span data-ttu-id="020f8-108">ListHead [in，out]</span><span class="sxs-lookup"><span data-stu-id="020f8-108">ListHead [in, out]</span></span>

<span data-ttu-id="020f8-109">**SLIST_HEADER** 結構的指標，表示單一連結清單的標頭。</span><span class="sxs-lookup"><span data-stu-id="020f8-109">Pointer to an **SLIST_HEADER** structure that represents the head of a singly linked list.</span></span>
<span data-ttu-id="020f8-110">*清單* 和 *ListEnd* 參數所指定的清單會插入此清單的前面。</span><span class="sxs-lookup"><span data-stu-id="020f8-110">The list specified by the *List* and *ListEnd* parameters is inserted at the front of this list.</span></span>

### <a name="list-in-out"></a><span data-ttu-id="020f8-111">清單 [in，out]</span><span class="sxs-lookup"><span data-stu-id="020f8-111">List [in, out]</span></span>

<span data-ttu-id="020f8-112">[SLIST_ENTRY](/windows/win32/api/winnt/ns-winnt-slist_entry)結構的指標，代表要插入清單中的第一個專案。</span><span class="sxs-lookup"><span data-stu-id="020f8-112">Pointer to an [SLIST_ENTRY](/windows/win32/api/winnt/ns-winnt-slist_entry) structure that represents the first item in the list to be inserted.</span></span>

### <a name="listend-in-out"></a><span data-ttu-id="020f8-113">ListEnd [in，out]</span><span class="sxs-lookup"><span data-stu-id="020f8-113">ListEnd [in, out]</span></span>

<span data-ttu-id="020f8-114">[SLIST_ENTRY](/windows/win32/api/winnt/ns-winnt-slist_entry)結構的指標，代表要插入清單中的最後一個專案。</span><span class="sxs-lookup"><span data-stu-id="020f8-114">Pointer to an [SLIST_ENTRY](/windows/win32/api/winnt/ns-winnt-slist_entry) structure that represents the last item in the list to be inserted.</span></span>

### <a name="count-in"></a><span data-ttu-id="020f8-115">計數 [in]</span><span class="sxs-lookup"><span data-stu-id="020f8-115">Count [in]</span></span>

<span data-ttu-id="020f8-116">清單中要插入的專案數目。</span><span class="sxs-lookup"><span data-stu-id="020f8-116">The number of items in the list to be inserted.</span></span>

## <a name="returns"></a><span data-ttu-id="020f8-117">傳回</span><span class="sxs-lookup"><span data-stu-id="020f8-117">Returns</span></span>

<span data-ttu-id="020f8-118">傳回值是 *ListHead* 參數所指定清單中的前一個專案。</span><span class="sxs-lookup"><span data-stu-id="020f8-118">The return value is the previous first item in the list specified by the *ListHead* parameter.</span></span>
<span data-ttu-id="020f8-119">如果清單之前是空的，則傳回值為 **Null**。</span><span class="sxs-lookup"><span data-stu-id="020f8-119">If the list was previously empty, the return value is **NULL**.</span></span>

## <a name="remarks"></a><span data-ttu-id="020f8-120">備註</span><span class="sxs-lookup"><span data-stu-id="020f8-120">Remarks</span></span>

<span data-ttu-id="020f8-121">所有清單專案都必須對齊 **MEMORY_ALLOCATION_ALIGNMENT** 界限;否則，此函式將會以無法預期的方式運作。</span><span class="sxs-lookup"><span data-stu-id="020f8-121">All list items must be aligned on a **MEMORY_ALLOCATION_ALIGNMENT** boundary; otherwise, this function will behave unpredictably.</span></span>
<span data-ttu-id="020f8-122">請參閱 **_aligned_malloc**。</span><span class="sxs-lookup"><span data-stu-id="020f8-122">See **_aligned_malloc**.</span></span>

<span data-ttu-id="020f8-123">**Windows 8 和 Windows Server 2012：**  此函數已被 [InterlockedPushListSListEx](/windows/desktop/api/interlockedapi/nf-interlockedapi-interlockedpushlistslistex)取代。</span><span class="sxs-lookup"><span data-stu-id="020f8-123">**Windows 8 and Windows Server 2012:**  This function has been superceded by [InterlockedPushListSListEx](/windows/desktop/api/interlockedapi/nf-interlockedapi-interlockedpushlistslistex).</span></span>
<span data-ttu-id="020f8-124">當使用 **NTDDI_VERSION** 設定為 **NTDDI_WIN8** 或更高版本進行編譯時，對 **InterlockedPushListSList** 的呼叫會改為移至 **InterlockedPushListSListEx** 。</span><span class="sxs-lookup"><span data-stu-id="020f8-124">When compiling with **NTDDI_VERSION** set to **NTDDI_WIN8** or greater, calls to **InterlockedPushListSList** will go to **InterlockedPushListSListEx** instead.</span></span>

## <a name="see-also"></a><span data-ttu-id="020f8-125">另請參閱</span><span class="sxs-lookup"><span data-stu-id="020f8-125">See also</span></span>

[<span data-ttu-id="020f8-126">連鎖單向連結清單</span><span class="sxs-lookup"><span data-stu-id="020f8-126">Interlocked Singly Linked Lists</span></span>](/windows/desktop/Sync/interlocked-singly-linked-lists)

[<span data-ttu-id="020f8-127">InterlockedPopEntrySList</span><span class="sxs-lookup"><span data-stu-id="020f8-127">InterlockedPopEntrySList</span></span>](/windows/desktop/api/interlockedapi/nf-interlockedapi-interlockedpopentryslist)

[<span data-ttu-id="020f8-128">InterlockedPushEntrySList</span><span class="sxs-lookup"><span data-stu-id="020f8-128">InterlockedPushEntrySList</span></span>](/windows/desktop/api/interlockedapi/nf-interlockedapi-interlockedpushentryslist)

[<span data-ttu-id="020f8-129">InterlockedPushListSListEx</span><span class="sxs-lookup"><span data-stu-id="020f8-129">InterlockedPushListSListEx</span></span>](/windows/desktop/api/interlockedapi/nf-interlockedapi-interlockedpushlistslistex)

[<span data-ttu-id="020f8-130">InterlockedFlushSList</span><span class="sxs-lookup"><span data-stu-id="020f8-130">InterlockedFlushSList</span></span>](/windows/desktop/api/interlockedapi/nf-interlockedapi-interlockedflushslist)

[<span data-ttu-id="020f8-131">SLIST_ENTRY</span><span class="sxs-lookup"><span data-stu-id="020f8-131">SLIST_ENTRY</span></span>](/windows/win32/api/winnt/ns-winnt-slist_entry)

[<span data-ttu-id="020f8-132">使用單向連結清單</span><span class="sxs-lookup"><span data-stu-id="020f8-132">Using Singly Linked Lists</span></span>](/windows/desktop/Sync/using-singly-linked-lists)
