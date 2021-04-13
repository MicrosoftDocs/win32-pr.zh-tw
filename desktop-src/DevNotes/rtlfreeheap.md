---
description: 釋放由 RtlAllocateHeap 從堆積配置的記憶體區塊。
ms.assetid: 0A08FB6B-23A3-450B-8745-AEB927CEB7BB
title: 'RtlFreeHeap 函式 (Ntifs) '
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- RtlFreeHeap
api_type:
- DllExport
api_location:
- Ntdll.dll
ms.openlocfilehash: e51994c4bcd941bc96575eb3fdbb45d4111c1aeb
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/07/2021
ms.locfileid: "104510558"
---
# <a name="rtlfreeheap-function"></a><span data-ttu-id="b56c1-103">RtlFreeHeap 函式</span><span class="sxs-lookup"><span data-stu-id="b56c1-103">RtlFreeHeap function</span></span>

<span data-ttu-id="b56c1-104">釋放由 [**RtlAllocateHeap**](/windows-hardware/drivers/ddi/ntifs/nf-ntifs-rtlallocateheap)從堆積配置的記憶體區塊。</span><span class="sxs-lookup"><span data-stu-id="b56c1-104">Frees a memory block that was allocated from a heap by [**RtlAllocateHeap**](/windows-hardware/drivers/ddi/ntifs/nf-ntifs-rtlallocateheap).</span></span>

## <a name="syntax"></a><span data-ttu-id="b56c1-105">語法</span><span class="sxs-lookup"><span data-stu-id="b56c1-105">Syntax</span></span>


```C++
BOOLEAN RtlFreeHeap(
  _In_     PVOID HeapHandle,
  _In_opt_ ULONG Flags,
  _In_     PVOID HeapBase
);
```



## <a name="parameters"></a><span data-ttu-id="b56c1-106">參數</span><span class="sxs-lookup"><span data-stu-id="b56c1-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="b56c1-107">*HeapHandle* \[在\]</span><span class="sxs-lookup"><span data-stu-id="b56c1-107">*HeapHandle* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="b56c1-108">要釋放其記憶體區塊之堆積的控制碼。</span><span class="sxs-lookup"><span data-stu-id="b56c1-108">A handle for the heap whose memory block is to be freed.</span></span> <span data-ttu-id="b56c1-109">此參數是 [**RtlCreateHeap**](/windows-hardware/drivers/ddi/ntifs/nf-ntifs-rtlcreateheap)所傳回的控制碼。</span><span class="sxs-lookup"><span data-stu-id="b56c1-109">This parameter is a handle returned by [**RtlCreateHeap**](/windows-hardware/drivers/ddi/ntifs/nf-ntifs-rtlcreateheap).</span></span>

</dd> <dt>

<span data-ttu-id="b56c1-110">*旗標* \[在中，選擇性\]</span><span class="sxs-lookup"><span data-stu-id="b56c1-110">*Flags* \[in, optional\]</span></span>
</dt> <dd>

<span data-ttu-id="b56c1-111">一組旗標，可控制釋放記憶體區塊的各個層面。</span><span class="sxs-lookup"><span data-stu-id="b56c1-111">A set of flags that controls aspects of freeing a memory block.</span></span> <span data-ttu-id="b56c1-112">指定下列值，可覆寫 [**RtlCreateHeap**](/windows-hardware/drivers/ddi/ntifs/nf-ntifs-rtlcreateheap)建立堆積時，*旗標* 參數中所指定的對應值。</span><span class="sxs-lookup"><span data-stu-id="b56c1-112">Specifying the following value overrides the corresponding value that was specified in the *Flags* parameter when the heap was created by [**RtlCreateHeap**](/windows-hardware/drivers/ddi/ntifs/nf-ntifs-rtlcreateheap).</span></span>



| <span data-ttu-id="b56c1-113">旗標</span><span class="sxs-lookup"><span data-stu-id="b56c1-113">Flag</span></span>                           | <span data-ttu-id="b56c1-114">意義</span><span class="sxs-lookup"><span data-stu-id="b56c1-114">Meaning</span></span>                                                                                   |
|--------------------------------|-------------------------------------------------------------------------------------------|
| <span data-ttu-id="b56c1-115">堆積 \_ 無 \_ 序列化</span><span class="sxs-lookup"><span data-stu-id="b56c1-115">HEAP\_NO\_SERIALIZE</span></span><br/> | <span data-ttu-id="b56c1-116">當 **RtlFreeHeap** 存取堆積時，不會使用相互排除。</span><span class="sxs-lookup"><span data-stu-id="b56c1-116">Mutual exclusion will not be used when **RtlFreeHeap** is accessing the heap.</span></span> <br/> |



 

</dd> <dt>

<span data-ttu-id="b56c1-117">*HeapBase* \[在\]</span><span class="sxs-lookup"><span data-stu-id="b56c1-117">*HeapBase* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="b56c1-118">要釋放之記憶體區塊的指標。</span><span class="sxs-lookup"><span data-stu-id="b56c1-118">A pointer to the memory block to free.</span></span> <span data-ttu-id="b56c1-119">[**RtlAllocateHeap**](/windows-hardware/drivers/ddi/ntifs/nf-ntifs-rtlallocateheap)會傳回這個指標。</span><span class="sxs-lookup"><span data-stu-id="b56c1-119">This pointer is returned by [**RtlAllocateHeap**](/windows-hardware/drivers/ddi/ntifs/nf-ntifs-rtlallocateheap).</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="b56c1-120">傳回值</span><span class="sxs-lookup"><span data-stu-id="b56c1-120">Return value</span></span>

<span data-ttu-id="b56c1-121">如果成功釋放區塊，則傳回 **TRUE** ;否則 **為 FALSE** 。</span><span class="sxs-lookup"><span data-stu-id="b56c1-121">Returns **TRUE** if the block was freed successfully; **FALSE** otherwise.</span></span>

> [!Note]  
> <span data-ttu-id="b56c1-122">從 Windows 8 開始，傳回值的類型為 **LOGICAL**，其大小與 **布林** 值不同。</span><span class="sxs-lookup"><span data-stu-id="b56c1-122">Starting with Windows 8 the return value is typed as **LOGICAL**, which has a different size than **BOOLEAN**.</span></span>

 

## <a name="requirements"></a><span data-ttu-id="b56c1-123">規格需求</span><span class="sxs-lookup"><span data-stu-id="b56c1-123">Requirements</span></span>



| <span data-ttu-id="b56c1-124">需求</span><span class="sxs-lookup"><span data-stu-id="b56c1-124">Requirement</span></span> | <span data-ttu-id="b56c1-125">值</span><span class="sxs-lookup"><span data-stu-id="b56c1-125">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="b56c1-126">最低支援的用戶端</span><span class="sxs-lookup"><span data-stu-id="b56c1-126">Minimum supported client</span></span><br/> | <span data-ttu-id="b56c1-127">Windows 2000 Professional \[僅限傳統型應用程式\]</span><span class="sxs-lookup"><span data-stu-id="b56c1-127">Windows 2000 Professional \[desktop apps only\]</span></span><br/>                                                                              |
| <span data-ttu-id="b56c1-128">最低支援的伺服器</span><span class="sxs-lookup"><span data-stu-id="b56c1-128">Minimum supported server</span></span><br/> | <span data-ttu-id="b56c1-129">Windows 2000 Server \[僅限傳統型應用程式\]</span><span class="sxs-lookup"><span data-stu-id="b56c1-129">Windows 2000 Server \[desktop apps only\]</span></span><br/>                                                                                    |
| <span data-ttu-id="b56c1-130">目標平台</span><span class="sxs-lookup"><span data-stu-id="b56c1-130">Target platform</span></span><br/>          | <dl> <span data-ttu-id="b56c1-131"><dt>[通用](https://msdn.microsoft.com/Library/Windows/Hardware/EB2264A4-BAE8-446B-B9A5-19893936DDCA)</dt></span><span class="sxs-lookup"><span data-stu-id="b56c1-131"><dt>[Universal](https://msdn.microsoft.com/Library/Windows/Hardware/EB2264A4-BAE8-446B-B9A5-19893936DDCA)</dt></span></span> </dl> |
| <span data-ttu-id="b56c1-132">標頭</span><span class="sxs-lookup"><span data-stu-id="b56c1-132">Header</span></span><br/>                   | <dl> <span data-ttu-id="b56c1-133"><dt>Ntifs (包含 Ntifs) </dt></span><span class="sxs-lookup"><span data-stu-id="b56c1-133"><dt>Ntifs.h (include Ntifs.h)</dt></span></span> </dl>                                    |
| <span data-ttu-id="b56c1-134">程式庫</span><span class="sxs-lookup"><span data-stu-id="b56c1-134">Library</span></span><br/>                  | <dl> <span data-ttu-id="b56c1-135"><dt>Ntdll.dll .lib</dt></span><span class="sxs-lookup"><span data-stu-id="b56c1-135"><dt>Ntdll.lib</dt></span></span> </dl>                                                    |
| <span data-ttu-id="b56c1-136">DLL</span><span class="sxs-lookup"><span data-stu-id="b56c1-136">DLL</span></span><br/>                      | <dl> <span data-ttu-id="b56c1-137"><dt>Ntdll.dll</dt></span><span class="sxs-lookup"><span data-stu-id="b56c1-137"><dt>Ntdll.dll</dt></span></span> </dl>                                                    |



## <a name="see-also"></a><span data-ttu-id="b56c1-138">另請參閱</span><span class="sxs-lookup"><span data-stu-id="b56c1-138">See also</span></span>

<dl> <dt>

[<span data-ttu-id="b56c1-139">**RtlAllocateHeap**</span><span class="sxs-lookup"><span data-stu-id="b56c1-139">**RtlAllocateHeap**</span></span>](/windows-hardware/drivers/ddi/ntifs/nf-ntifs-rtlallocateheap)
</dt> <dt>

[<span data-ttu-id="b56c1-140">**RtlCreateHeap**</span><span class="sxs-lookup"><span data-stu-id="b56c1-140">**RtlCreateHeap**</span></span>](/windows-hardware/drivers/ddi/ntifs/nf-ntifs-rtlcreateheap)
</dt> <dt>

[<span data-ttu-id="b56c1-141">**RtlDestroyHeap**</span><span class="sxs-lookup"><span data-stu-id="b56c1-141">**RtlDestroyHeap**</span></span>](/windows-hardware/drivers/ddi/ntifs/nf-ntifs-rtldestroyheap)
</dt> </dl>

 

 
