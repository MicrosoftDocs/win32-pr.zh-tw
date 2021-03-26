---
description: 此類別是就緒執行緒事件的事件種類類別。 以下是從 MOF 程式碼簡化的語法。
ms.assetid: 861ab070-5536-4897-b523-9b09a7d59b3e
title: ReadyThread 類別
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- ReadyThread
- ReadyThread.TThreadId
- ReadyThread.AdjustReason
- ReadyThread.AdjustIncrement
- ReadyThread.Flag
- ReadyThread.Reserved
api_type:
- NA
api_location: ''
ms.openlocfilehash: e10029c0397c16a5a5eb30be6e3db64c0baec596
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/07/2021
ms.locfileid: "103848170"
---
# <a name="readythread-class"></a><span data-ttu-id="4a4ef-104">ReadyThread 類別</span><span class="sxs-lookup"><span data-stu-id="4a4ef-104">ReadyThread class</span></span>

<span data-ttu-id="4a4ef-105">此類別是就緒執行緒事件的事件種類類別。</span><span class="sxs-lookup"><span data-stu-id="4a4ef-105">This class is the event type class for ready thread events.</span></span>

<span data-ttu-id="4a4ef-106">以下是從 MOF 程式碼簡化的語法。</span><span class="sxs-lookup"><span data-stu-id="4a4ef-106">The following syntax is simplified from MOF code.</span></span>

## <a name="syntax"></a><span data-ttu-id="4a4ef-107">語法</span><span class="sxs-lookup"><span data-stu-id="4a4ef-107">Syntax</span></span>

``` syntax
[EventType{50}, EventTypeName{"ReadyThread"}]
class ReadyThread : Thread_V2
{
  uint32 TThreadId;
  sint8  AdjustReason;
  sint8  AdjustIncrement;
  sint8  Flag;
  sint8  Reserved;
};
```

## <a name="members"></a><span data-ttu-id="4a4ef-108">成員</span><span class="sxs-lookup"><span data-stu-id="4a4ef-108">Members</span></span>

<span data-ttu-id="4a4ef-109">**ReadyThread** 類別具有下列類型的成員：</span><span class="sxs-lookup"><span data-stu-id="4a4ef-109">The **ReadyThread** class has these types of members:</span></span>

-   [<span data-ttu-id="4a4ef-110">屬性</span><span class="sxs-lookup"><span data-stu-id="4a4ef-110">Properties</span></span>](#properties)

### <a name="properties"></a><span data-ttu-id="4a4ef-111">屬性</span><span class="sxs-lookup"><span data-stu-id="4a4ef-111">Properties</span></span>

<span data-ttu-id="4a4ef-112">**ReadyThread** 類別具有這些屬性。</span><span class="sxs-lookup"><span data-stu-id="4a4ef-112">The **ReadyThread** class has these properties.</span></span>

<dl> <dt>

<span data-ttu-id="4a4ef-113">AdjustIncrement</span><span class="sxs-lookup"><span data-stu-id="4a4ef-113">AdjustIncrement</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="4a4ef-114">資料類型： **sint8**</span><span class="sxs-lookup"><span data-stu-id="4a4ef-114">Data type: **sint8**</span></span>
</dt> <dt>

<span data-ttu-id="4a4ef-115">存取類型：唯讀</span><span class="sxs-lookup"><span data-stu-id="4a4ef-115">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="4a4ef-116">限定詞： WmiDataId (3) </span><span class="sxs-lookup"><span data-stu-id="4a4ef-116">Qualifiers: WmiDataId(3)</span></span>
</dt> </dl>

<span data-ttu-id="4a4ef-117">要調整優先順序的值。</span><span class="sxs-lookup"><span data-stu-id="4a4ef-117">The value by which the priority is being adjusted.</span></span>

</dd> <dt>

<span data-ttu-id="4a4ef-118">AdjustReason</span><span class="sxs-lookup"><span data-stu-id="4a4ef-118">AdjustReason</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="4a4ef-119">資料類型： **sint8**</span><span class="sxs-lookup"><span data-stu-id="4a4ef-119">Data type: **sint8**</span></span>
</dt> <dt>

<span data-ttu-id="4a4ef-120">存取類型：唯讀</span><span class="sxs-lookup"><span data-stu-id="4a4ef-120">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="4a4ef-121">限定詞： WmiDataId (2) </span><span class="sxs-lookup"><span data-stu-id="4a4ef-121">Qualifiers: WmiDataId(2)</span></span>
</dt> </dl>

<span data-ttu-id="4a4ef-122">提高優先順序的原因。</span><span class="sxs-lookup"><span data-stu-id="4a4ef-122">The reason for the priority boost.</span></span>



| <span data-ttu-id="4a4ef-123">值</span><span class="sxs-lookup"><span data-stu-id="4a4ef-123">Value</span></span>                                                                        | <span data-ttu-id="4a4ef-124">意義</span><span class="sxs-lookup"><span data-stu-id="4a4ef-124">Meaning</span></span>                                                                                                                 |
|------------------------------------------------------------------------------|-------------------------------------------------------------------------------------------------------------------------|
| <dl> <span data-ttu-id="4a4ef-125"><dt>0</dt></span><span class="sxs-lookup"><span data-stu-id="4a4ef-125"><dt>0</dt></span></span> </dl> | <span data-ttu-id="4a4ef-126">略過增量。</span><span class="sxs-lookup"><span data-stu-id="4a4ef-126">Ignore the increment.</span></span><br/>                                                                                        |
| <dl> <span data-ttu-id="4a4ef-127"><dt>1</dt></span><span class="sxs-lookup"><span data-stu-id="4a4ef-127"><dt>1</dt></span></span> </dl> | <span data-ttu-id="4a4ef-128">套用增量，這會在每個量子的結尾以累加方式衰減。</span><span class="sxs-lookup"><span data-stu-id="4a4ef-128">Apply the increment, which will decay incrementally at the end of each quantum.</span></span><br/>                              |
| <dl> <span data-ttu-id="4a4ef-129"><dt>2</dt></span><span class="sxs-lookup"><span data-stu-id="4a4ef-129"><dt>2</dt></span></span> </dl> | <span data-ttu-id="4a4ef-130">套用增量作為提升，在量子 (通常會在優先順序捐贈) 中全面衰減。</span><span class="sxs-lookup"><span data-stu-id="4a4ef-130">Apply the increment as a boost that will decay in its entirety at quantum (typically for priority donation).</span></span><br/> |



 

</dd> <dt>

<span data-ttu-id="4a4ef-131">旗標</span><span class="sxs-lookup"><span data-stu-id="4a4ef-131">Flag</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="4a4ef-132">資料類型： **sint8**</span><span class="sxs-lookup"><span data-stu-id="4a4ef-132">Data type: **sint8**</span></span>
</dt> <dt>

<span data-ttu-id="4a4ef-133">存取類型：唯讀</span><span class="sxs-lookup"><span data-stu-id="4a4ef-133">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="4a4ef-134">限定詞： WmiDataId (4) </span><span class="sxs-lookup"><span data-stu-id="4a4ef-134">Qualifiers: WmiDataId(4)</span></span>
</dt> </dl>

<span data-ttu-id="4a4ef-135">以下是可能的狀態旗標：</span><span class="sxs-lookup"><span data-stu-id="4a4ef-135">The following are the possible state flags:</span></span>



| <span data-ttu-id="4a4ef-136">值</span><span class="sxs-lookup"><span data-stu-id="4a4ef-136">Value</span></span>                                                                          | <span data-ttu-id="4a4ef-137">意義</span><span class="sxs-lookup"><span data-stu-id="4a4ef-137">Meaning</span></span>                                                                    |
|--------------------------------------------------------------------------------|----------------------------------------------------------------------------|
| <dl> <span data-ttu-id="4a4ef-138"><dt>0x1</dt></span><span class="sxs-lookup"><span data-stu-id="4a4ef-138"><dt>0x1</dt></span></span> </dl> | <span data-ttu-id="4a4ef-139">已經從 DPC 準備好執行緒 (延後程序呼叫) 。</span><span class="sxs-lookup"><span data-stu-id="4a4ef-139">The thread has been readied from DPC (deferred procedure call).</span></span><br/> |
| <dl> <span data-ttu-id="4a4ef-140"><dt>0x2</dt></span><span class="sxs-lookup"><span data-stu-id="4a4ef-140"><dt>0x2</dt></span></span> </dl> | <span data-ttu-id="4a4ef-141">核心堆疊目前已交換。</span><span class="sxs-lookup"><span data-stu-id="4a4ef-141">The kernel stack is currently swapped out.</span></span><br/>                      |
| <dl> <span data-ttu-id="4a4ef-142"><dt>0x4</dt></span><span class="sxs-lookup"><span data-stu-id="4a4ef-142"><dt>0x4</dt></span></span> </dl> | <span data-ttu-id="4a4ef-143">進程位址空間已交換。</span><span class="sxs-lookup"><span data-stu-id="4a4ef-143">The process address space is swapped out.</span></span><br/>                       |



 

<span data-ttu-id="4a4ef-144">請注意，當核心堆疊或進程位址空間已交換時，會在核心堆疊或進程位址空間交換之後，還有一個額外的 ReadyThread 事件，並讓執行緒準備好分派。</span><span class="sxs-lookup"><span data-stu-id="4a4ef-144">Note that when the kernel stack or the process address space is swapped out, there will be an additional ReadyThread event after the kernel stack or the process address space has been swapped back in and the thread is made ready to be dispatched.</span></span>

</dd> <dt>

<span data-ttu-id="4a4ef-145">保留</span><span class="sxs-lookup"><span data-stu-id="4a4ef-145">Reserved</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="4a4ef-146">資料類型： **sint8**</span><span class="sxs-lookup"><span data-stu-id="4a4ef-146">Data type: **sint8**</span></span>
</dt> <dt>

<span data-ttu-id="4a4ef-147">存取類型：唯讀</span><span class="sxs-lookup"><span data-stu-id="4a4ef-147">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="4a4ef-148">限定詞： WmiDataId (5) </span><span class="sxs-lookup"><span data-stu-id="4a4ef-148">Qualifiers: WmiDataId(5)</span></span>
</dt> </dl>

<span data-ttu-id="4a4ef-149">保留的。</span><span class="sxs-lookup"><span data-stu-id="4a4ef-149">Reserved.</span></span>

</dd> <dt>

<span data-ttu-id="4a4ef-150">TThreadId</span><span class="sxs-lookup"><span data-stu-id="4a4ef-150">TThreadId</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="4a4ef-151">資料類型： **uint32**</span><span class="sxs-lookup"><span data-stu-id="4a4ef-151">Data type: **uint32**</span></span>
</dt> <dt>

<span data-ttu-id="4a4ef-152">存取類型：唯讀</span><span class="sxs-lookup"><span data-stu-id="4a4ef-152">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="4a4ef-153">限定詞： WmiDataId (1) ，格式 ( "x" ) </span><span class="sxs-lookup"><span data-stu-id="4a4ef-153">Qualifiers: WmiDataId(1), Format("x")</span></span>
</dt> </dl>

<span data-ttu-id="4a4ef-154">要準備好執行之執行緒的執行緒識別碼。</span><span class="sxs-lookup"><span data-stu-id="4a4ef-154">The thread identifier of the thread being readied for execution.</span></span>

</dd> </dl>

## <a name="requirements"></a><span data-ttu-id="4a4ef-155">規格需求</span><span class="sxs-lookup"><span data-stu-id="4a4ef-155">Requirements</span></span>



| <span data-ttu-id="4a4ef-156">需求</span><span class="sxs-lookup"><span data-stu-id="4a4ef-156">Requirement</span></span> | <span data-ttu-id="4a4ef-157">值</span><span class="sxs-lookup"><span data-stu-id="4a4ef-157">Value</span></span> |
|-------------------------------------|------------------------------------------------------------|
| <span data-ttu-id="4a4ef-158">最低支援的用戶端</span><span class="sxs-lookup"><span data-stu-id="4a4ef-158">Minimum supported client</span></span><br/> | <span data-ttu-id="4a4ef-159">Windows 2000 Professional \[僅限傳統型應用程式\]</span><span class="sxs-lookup"><span data-stu-id="4a4ef-159">Windows 2000 Professional \[desktop apps only\]</span></span><br/> |
| <span data-ttu-id="4a4ef-160">最低支援的伺服器</span><span class="sxs-lookup"><span data-stu-id="4a4ef-160">Minimum supported server</span></span><br/> | <span data-ttu-id="4a4ef-161">Windows 2000 Server \[僅限傳統型應用程式\]</span><span class="sxs-lookup"><span data-stu-id="4a4ef-161">Windows 2000 Server \[desktop apps only\]</span></span><br/>       |



## <a name="see-also"></a><span data-ttu-id="4a4ef-162">另請參閱</span><span class="sxs-lookup"><span data-stu-id="4a4ef-162">See also</span></span>

<dl> <dt>

[<span data-ttu-id="4a4ef-163">**執行緒 \_ V2**</span><span class="sxs-lookup"><span data-stu-id="4a4ef-163">**Thread\_V2**</span></span>](thread-v2.md)
</dt> </dl>

 

 




