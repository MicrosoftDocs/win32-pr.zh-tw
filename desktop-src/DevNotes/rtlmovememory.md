---
description: 將來源記憶體區塊的內容複寫到目的地記憶體區塊，並支援重迭的來源和目的地記憶體區塊。
ms.assetid: D374F14D-24C7-4771-AD40-3AC37E7A2D2F
title: 'RtlMoveMemory 函式 (Wdm) '
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- RtlMoveMemory
api_type:
- DllExport
api_location:
- Ntdll.dll
ms.openlocfilehash: 65f8c8490224213e0bef27fab5239a21eca24344
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/07/2021
ms.locfileid: "106973569"
---
# <a name="rtlmovememory-function"></a><span data-ttu-id="c38db-103">RtlMoveMemory 函式</span><span class="sxs-lookup"><span data-stu-id="c38db-103">RtlMoveMemory function</span></span>

<span data-ttu-id="c38db-104">將來源記憶體區塊的內容複寫到目的地記憶體區塊，並支援重迭的來源和目的地記憶體區塊。</span><span class="sxs-lookup"><span data-stu-id="c38db-104">Copies the contents of a source memory block to a destination memory block, and supports overlapping source and destination memory blocks.</span></span>

## <a name="syntax"></a><span data-ttu-id="c38db-105">語法</span><span class="sxs-lookup"><span data-stu-id="c38db-105">Syntax</span></span>


```C++
VOID RtlMoveMemory(
  _Out_       VOID UNALIGNED *Destination,
  _In_  const VOID UNALIGNED *Source,
  _In_        SIZE_T         Length
);
```



## <a name="parameters"></a><span data-ttu-id="c38db-106">參數</span><span class="sxs-lookup"><span data-stu-id="c38db-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="c38db-107">*目的地* \[擴展\]</span><span class="sxs-lookup"><span data-stu-id="c38db-107">*Destination* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="c38db-108">要將位元組複製到其中之目的地記憶體區塊的指標。</span><span class="sxs-lookup"><span data-stu-id="c38db-108">A pointer to the destination memory block to copy the bytes to.</span></span>

</dd> <dt>

<span data-ttu-id="c38db-109">*來源* \[在\]</span><span class="sxs-lookup"><span data-stu-id="c38db-109">*Source* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="c38db-110">要從中複製位元組之來源記憶體區塊的指標。</span><span class="sxs-lookup"><span data-stu-id="c38db-110">A pointer to the source memory block to copy the bytes from.</span></span>

</dd> <dt>

<span data-ttu-id="c38db-111">*長度* \[在\]</span><span class="sxs-lookup"><span data-stu-id="c38db-111">*Length* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="c38db-112">要從來源複製到目的地的位元組數目。</span><span class="sxs-lookup"><span data-stu-id="c38db-112">The number of bytes to copy from the source to the destination.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="c38db-113">傳回值</span><span class="sxs-lookup"><span data-stu-id="c38db-113">Return value</span></span>

<span data-ttu-id="c38db-114">無</span><span class="sxs-lookup"><span data-stu-id="c38db-114">None</span></span>

## <a name="remarks"></a><span data-ttu-id="c38db-115">備註</span><span class="sxs-lookup"><span data-stu-id="c38db-115">Remarks</span></span>

<span data-ttu-id="c38db-116">來源記憶體區塊是由 *來源* 和 *長度* 所定義，可以重迭目的地記憶體區塊（由 *目的地* 和 *長度* 所定義）。</span><span class="sxs-lookup"><span data-stu-id="c38db-116">The source memory block, which is defined by *Source* and *Length*, can overlap the destination memory block, which is defined by *Destination* and *Length*.</span></span>

<span data-ttu-id="c38db-117">[**RtlCopyMemory**](/windows-hardware/drivers/ddi/wdm/nf-wdm-rtlcopymemory)常式的執行速度比 **RtlMoveMemory** 快，但 **RtlCopyMemory** 需要來源和目的地記憶體區塊不重迭。</span><span class="sxs-lookup"><span data-stu-id="c38db-117">The [**RtlCopyMemory**](/windows-hardware/drivers/ddi/wdm/nf-wdm-rtlcopymemory) routine runs faster than **RtlMoveMemory**, but **RtlCopyMemory** requires that the source and destination memory blocks do not overlap.</span></span>

<span data-ttu-id="c38db-118">如果來源和目的地記憶體區塊是在非分頁系統記憶體中， **RtlMoveMemory** 的呼叫端可以在任何 IRQL 執行。</span><span class="sxs-lookup"><span data-stu-id="c38db-118">Callers of **RtlMoveMemory** can be running at any IRQL if the source and destination memory blocks are in nonpaged system memory.</span></span> <span data-ttu-id="c38db-119">否則，呼叫端必須在 IRQL <= APC \_ 層級執行。</span><span class="sxs-lookup"><span data-stu-id="c38db-119">Otherwise, the caller must be running at IRQL <= APC\_LEVEL.</span></span>

## <a name="requirements"></a><span data-ttu-id="c38db-120">規格需求</span><span class="sxs-lookup"><span data-stu-id="c38db-120">Requirements</span></span>



| <span data-ttu-id="c38db-121">需求</span><span class="sxs-lookup"><span data-stu-id="c38db-121">Requirement</span></span> | <span data-ttu-id="c38db-122">值</span><span class="sxs-lookup"><span data-stu-id="c38db-122">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="c38db-123">最低支援的用戶端</span><span class="sxs-lookup"><span data-stu-id="c38db-123">Minimum supported client</span></span><br/> | <span data-ttu-id="c38db-124">Windows 2000 Professional \[僅限傳統型應用程式\]</span><span class="sxs-lookup"><span data-stu-id="c38db-124">Windows 2000 Professional \[desktop apps only\]</span></span><br/>                                                                              |
| <span data-ttu-id="c38db-125">最低支援的伺服器</span><span class="sxs-lookup"><span data-stu-id="c38db-125">Minimum supported server</span></span><br/> | <span data-ttu-id="c38db-126">Windows 2000 Server \[僅限傳統型應用程式\]</span><span class="sxs-lookup"><span data-stu-id="c38db-126">Windows 2000 Server \[desktop apps only\]</span></span><br/>                                                                                    |
| <span data-ttu-id="c38db-127">目標平台</span><span class="sxs-lookup"><span data-stu-id="c38db-127">Target platform</span></span><br/>          | <dl> <span data-ttu-id="c38db-128"><dt>[通用](https://msdn.microsoft.com/Library/Windows/Hardware/EB2264A4-BAE8-446B-B9A5-19893936DDCA)</dt></span><span class="sxs-lookup"><span data-stu-id="c38db-128"><dt>[Universal](https://msdn.microsoft.com/Library/Windows/Hardware/EB2264A4-BAE8-446B-B9A5-19893936DDCA)</dt></span></span> </dl> |
| <span data-ttu-id="c38db-129">標頭</span><span class="sxs-lookup"><span data-stu-id="c38db-129">Header</span></span><br/>                   | <dl> <span data-ttu-id="c38db-130"><dt>Wdm (包括 Wdm、Ntddk .h 或 Ntifs. h) </dt></span><span class="sxs-lookup"><span data-stu-id="c38db-130"><dt>Wdm.h (include Wdm.h, Ntddk.h, or Ntifs.h)</dt></span></span> </dl>                   |
| <span data-ttu-id="c38db-131">程式庫</span><span class="sxs-lookup"><span data-stu-id="c38db-131">Library</span></span><br/>                  | <dl> <span data-ttu-id="c38db-132"><dt>Ntdll.dll .lib</dt></span><span class="sxs-lookup"><span data-stu-id="c38db-132"><dt>Ntdll.lib</dt></span></span> </dl>                                                    |
| <span data-ttu-id="c38db-133">DLL</span><span class="sxs-lookup"><span data-stu-id="c38db-133">DLL</span></span><br/>                      | <dl> <span data-ttu-id="c38db-134"><dt>Ntdll.dll</dt></span><span class="sxs-lookup"><span data-stu-id="c38db-134"><dt>Ntdll.dll</dt></span></span> </dl>                                                    |



## <a name="see-also"></a><span data-ttu-id="c38db-135">另請參閱</span><span class="sxs-lookup"><span data-stu-id="c38db-135">See also</span></span>

<dl> <dt>

[<span data-ttu-id="c38db-136">**RtlCopyMemory**</span><span class="sxs-lookup"><span data-stu-id="c38db-136">**RtlCopyMemory**</span></span>](/windows-hardware/drivers/ddi/wdm/nf-wdm-rtlcopymemory)
</dt> </dl>

 

 
