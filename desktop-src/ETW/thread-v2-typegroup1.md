---
description: Thread_V2_TypeGroup1 類別-這個類別是執行緒開始和結束事件的事件種類類別。 以下是從 MOF 程式碼簡化的語法。
ms.assetid: c24b4bc9-2a05-444c-be41-b4dfd0511b93
title: Thread_V2_TypeGroup1 類別
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Thread_V2_TypeGroup1
- Thread_V2_TypeGroup1.ProcessId
- Thread_V2_TypeGroup1.TThreadId
- Thread_V2_TypeGroup1.StackBase
- Thread_V2_TypeGroup1.StackLimit
- Thread_V2_TypeGroup1.UserStackBase
- Thread_V2_TypeGroup1.UserStackLimit
- Thread_V2_TypeGroup1.StartAddr
- Thread_V2_TypeGroup1.Win32StartAddr
- Thread_V2_TypeGroup1.TebBase
- Thread_V2_TypeGroup1.SubProcessTag
api_type:
- NA
api_location: ''
ms.openlocfilehash: 24ac4655fc374c40eb530828229a319f9ee1375e
ms.sourcegitcommit: 95685061d5b0333bbf9e6ebd208dde8190f97005
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 04/28/2021
ms.locfileid: "108105656"
---
# <a name="thread_v2_typegroup1-class"></a><span data-ttu-id="44e10-104">執行緒 \_ V2 \_ TypeGroup1 類別</span><span class="sxs-lookup"><span data-stu-id="44e10-104">Thread\_V2\_TypeGroup1 class</span></span>

<span data-ttu-id="44e10-105">這個類別是執行緒開始和結束事件的事件種類類別。</span><span class="sxs-lookup"><span data-stu-id="44e10-105">This class is the event type class for thread start and end events.</span></span>

<span data-ttu-id="44e10-106">以下是從 MOF 程式碼簡化的語法。</span><span class="sxs-lookup"><span data-stu-id="44e10-106">The following syntax is simplified from MOF code.</span></span>

## <a name="syntax"></a><span data-ttu-id="44e10-107">語法</span><span class="sxs-lookup"><span data-stu-id="44e10-107">Syntax</span></span>

``` syntax
[EventType{1, 2, 3, 4}, EventTypeName{"Start", "End", "DCStart", "DCEnd"}]
class Thread_V2_TypeGroup1 : Thread_V2
{
  uint32 ProcessId;
  uint32 TThreadId;
  uint32 StackBase;
  uint32 StackLimit;
  uint32 UserStackBase;
  uint32 UserStackLimit;
  uint32 StartAddr;
  uint32 Win32StartAddr;
  uint32 TebBase;
  uint32 SubProcessTag;
};
```

## <a name="members"></a><span data-ttu-id="44e10-108">成員</span><span class="sxs-lookup"><span data-stu-id="44e10-108">Members</span></span>

<span data-ttu-id="44e10-109">**執行緒 \_ V2 \_ TypeGroup1** 類別具有下列類型的成員：</span><span class="sxs-lookup"><span data-stu-id="44e10-109">The **Thread\_V2\_TypeGroup1** class has these types of members:</span></span>

-   [<span data-ttu-id="44e10-110">屬性</span><span class="sxs-lookup"><span data-stu-id="44e10-110">Properties</span></span>](#properties)

### <a name="properties"></a><span data-ttu-id="44e10-111">屬性</span><span class="sxs-lookup"><span data-stu-id="44e10-111">Properties</span></span>

<span data-ttu-id="44e10-112">**執行緒 \_ V2 \_ TypeGroup1** 類別具有這些屬性。</span><span class="sxs-lookup"><span data-stu-id="44e10-112">The **Thread\_V2\_TypeGroup1** class has these properties.</span></span>

<dl> <dt>

<span data-ttu-id="44e10-113">ProcessId</span><span class="sxs-lookup"><span data-stu-id="44e10-113">ProcessId</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="44e10-114">資料類型： **uint32**</span><span class="sxs-lookup"><span data-stu-id="44e10-114">Data type: **uint32**</span></span>
</dt> <dt>

<span data-ttu-id="44e10-115">存取類型：唯讀</span><span class="sxs-lookup"><span data-stu-id="44e10-115">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="44e10-116">限定詞： WmiDataId (1) ，格式 ( "x" ) </span><span class="sxs-lookup"><span data-stu-id="44e10-116">Qualifiers: WmiDataId(1), Format("x")</span></span>
</dt> </dl>

<span data-ttu-id="44e10-117">事件所涉及之執行緒的處理序識別碼。</span><span class="sxs-lookup"><span data-stu-id="44e10-117">Process identifier of the thread involved in the event.</span></span>

</dd> <dt>

<span data-ttu-id="44e10-118">StackBase</span><span class="sxs-lookup"><span data-stu-id="44e10-118">StackBase</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="44e10-119">資料類型： **uint32**</span><span class="sxs-lookup"><span data-stu-id="44e10-119">Data type: **uint32**</span></span>
</dt> <dt>

<span data-ttu-id="44e10-120">存取類型：唯讀</span><span class="sxs-lookup"><span data-stu-id="44e10-120">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="44e10-121">限定詞： WmiDataId (3) ，指標</span><span class="sxs-lookup"><span data-stu-id="44e10-121">Qualifiers: WmiDataId(3), Pointer</span></span>
</dt> </dl>

<span data-ttu-id="44e10-122">執行緒堆疊的基底位址。</span><span class="sxs-lookup"><span data-stu-id="44e10-122">Base address of the thread's stack.</span></span>

</dd> <dt>

<span data-ttu-id="44e10-123">StackLimit</span><span class="sxs-lookup"><span data-stu-id="44e10-123">StackLimit</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="44e10-124">資料類型： **uint32**</span><span class="sxs-lookup"><span data-stu-id="44e10-124">Data type: **uint32**</span></span>
</dt> <dt>

<span data-ttu-id="44e10-125">存取類型：唯讀</span><span class="sxs-lookup"><span data-stu-id="44e10-125">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="44e10-126">限定詞： WmiDataId (4) ，指標</span><span class="sxs-lookup"><span data-stu-id="44e10-126">Qualifiers: WmiDataId(4), Pointer</span></span>
</dt> </dl>

<span data-ttu-id="44e10-127">執行緒堆疊的限制。</span><span class="sxs-lookup"><span data-stu-id="44e10-127">Limit of the thread's stack.</span></span>

</dd> <dt>

<span data-ttu-id="44e10-128">StartAddr</span><span class="sxs-lookup"><span data-stu-id="44e10-128">StartAddr</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="44e10-129">資料類型： **uint32**</span><span class="sxs-lookup"><span data-stu-id="44e10-129">Data type: **uint32**</span></span>
</dt> <dt>

<span data-ttu-id="44e10-130">存取類型：唯讀</span><span class="sxs-lookup"><span data-stu-id="44e10-130">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="44e10-131">限定詞： WmiDataId (7) ，指標</span><span class="sxs-lookup"><span data-stu-id="44e10-131">Qualifiers: WmiDataId(7), Pointer</span></span>
</dt> </dl>

<span data-ttu-id="44e10-132">追蹤開始的記憶體位址。</span><span class="sxs-lookup"><span data-stu-id="44e10-132">Memory address at which the trace starts.</span></span>

</dd> <dt>

<span data-ttu-id="44e10-133">SubProcessTag</span><span class="sxs-lookup"><span data-stu-id="44e10-133">SubProcessTag</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="44e10-134">資料類型： **uint32**</span><span class="sxs-lookup"><span data-stu-id="44e10-134">Data type: **uint32**</span></span>
</dt> <dt>

<span data-ttu-id="44e10-135">存取類型：唯讀</span><span class="sxs-lookup"><span data-stu-id="44e10-135">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="44e10-136">限定詞： WmiDataId (10) ，格式 ( "x" ) </span><span class="sxs-lookup"><span data-stu-id="44e10-136">Qualifiers: WmiDataId(10), Format("x")</span></span>
</dt> </dl>

<span data-ttu-id="44e10-137">識別服務（如果執行緒是由服務所擁有）;否則為零。</span><span class="sxs-lookup"><span data-stu-id="44e10-137">Identifies the service if the thread is owned by a service; otherwise, zero.</span></span>

</dd> <dt>

<span data-ttu-id="44e10-138">TebBase</span><span class="sxs-lookup"><span data-stu-id="44e10-138">TebBase</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="44e10-139">資料類型： **uint32**</span><span class="sxs-lookup"><span data-stu-id="44e10-139">Data type: **uint32**</span></span>
</dt> <dt>

<span data-ttu-id="44e10-140">存取類型：唯讀</span><span class="sxs-lookup"><span data-stu-id="44e10-140">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="44e10-141">限定詞： WmiDataId (9) ，指標</span><span class="sxs-lookup"><span data-stu-id="44e10-141">Qualifiers: WmiDataId(9), Pointer</span></span>
</dt> </dl>

<span data-ttu-id="44e10-142">執行緒環境區塊基底位址。</span><span class="sxs-lookup"><span data-stu-id="44e10-142">Thread environment block base address.</span></span>

</dd> <dt>

<span data-ttu-id="44e10-143">TThreadId</span><span class="sxs-lookup"><span data-stu-id="44e10-143">TThreadId</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="44e10-144">資料類型： **uint32**</span><span class="sxs-lookup"><span data-stu-id="44e10-144">Data type: **uint32**</span></span>
</dt> <dt>

<span data-ttu-id="44e10-145">存取類型：唯讀</span><span class="sxs-lookup"><span data-stu-id="44e10-145">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="44e10-146">限定詞： WmiDataId (2) ，格式 ( "x" ) </span><span class="sxs-lookup"><span data-stu-id="44e10-146">Qualifiers: WmiDataId(2), Format("x")</span></span>
</dt> </dl>

<span data-ttu-id="44e10-147">事件所涉及之執行緒的執行緒識別碼。</span><span class="sxs-lookup"><span data-stu-id="44e10-147">Thread identifier of the thread involved in the event.</span></span>

</dd> <dt>

<span data-ttu-id="44e10-148">UserStackBase</span><span class="sxs-lookup"><span data-stu-id="44e10-148">UserStackBase</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="44e10-149">資料類型： **uint32**</span><span class="sxs-lookup"><span data-stu-id="44e10-149">Data type: **uint32**</span></span>
</dt> <dt>

<span data-ttu-id="44e10-150">存取類型：唯讀</span><span class="sxs-lookup"><span data-stu-id="44e10-150">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="44e10-151">限定詞： WmiDataId (5) ，指標</span><span class="sxs-lookup"><span data-stu-id="44e10-151">Qualifiers: WmiDataId(5), Pointer</span></span>
</dt> </dl>

<span data-ttu-id="44e10-152">執行緒使用者模式堆疊的基底位址。</span><span class="sxs-lookup"><span data-stu-id="44e10-152">Base address of the thread's user-mode stack.</span></span>

</dd> <dt>

<span data-ttu-id="44e10-153">UserStackLimit</span><span class="sxs-lookup"><span data-stu-id="44e10-153">UserStackLimit</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="44e10-154">資料類型： **uint32**</span><span class="sxs-lookup"><span data-stu-id="44e10-154">Data type: **uint32**</span></span>
</dt> <dt>

<span data-ttu-id="44e10-155">存取類型：唯讀</span><span class="sxs-lookup"><span data-stu-id="44e10-155">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="44e10-156">限定詞： WmiDataId (6) ，指標</span><span class="sxs-lookup"><span data-stu-id="44e10-156">Qualifiers: WmiDataId(6), Pointer</span></span>
</dt> </dl>

<span data-ttu-id="44e10-157">執行緒使用者模式堆疊的限制。</span><span class="sxs-lookup"><span data-stu-id="44e10-157">Limit of the thread's user-mode stack.</span></span>

</dd> <dt>

<span data-ttu-id="44e10-158">Win32StartAddr</span><span class="sxs-lookup"><span data-stu-id="44e10-158">Win32StartAddr</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="44e10-159">資料類型： **uint32**</span><span class="sxs-lookup"><span data-stu-id="44e10-159">Data type: **uint32**</span></span>
</dt> <dt>

<span data-ttu-id="44e10-160">存取類型：唯讀</span><span class="sxs-lookup"><span data-stu-id="44e10-160">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="44e10-161">限定詞： WmiDataId (8) ，指標</span><span class="sxs-lookup"><span data-stu-id="44e10-161">Qualifiers: WmiDataId(8), Pointer</span></span>
</dt> </dl>

<span data-ttu-id="44e10-162">此執行緒要執行之函式的起始位址。</span><span class="sxs-lookup"><span data-stu-id="44e10-162">Starting address of the function to be executed by this thread.</span></span>

</dd> </dl>

## <a name="remarks"></a><span data-ttu-id="44e10-163">備註</span><span class="sxs-lookup"><span data-stu-id="44e10-163">Remarks</span></span>

<span data-ttu-id="44e10-164">DCStart 和 DCEnd 事件種類會列舉核心會話開始和結束時，目前正在執行的執行緒。</span><span class="sxs-lookup"><span data-stu-id="44e10-164">The DCStart and DCEnd event types enumerate the threads that are currently running at the time the kernel session starts and ends, respectively.</span></span>

## <a name="requirements"></a><span data-ttu-id="44e10-165">規格需求</span><span class="sxs-lookup"><span data-stu-id="44e10-165">Requirements</span></span>



| <span data-ttu-id="44e10-166">需求</span><span class="sxs-lookup"><span data-stu-id="44e10-166">Requirement</span></span> | <span data-ttu-id="44e10-167">值</span><span class="sxs-lookup"><span data-stu-id="44e10-167">Value</span></span> |
|-------------------------------------|------------------------------------------------------|
| <span data-ttu-id="44e10-168">最低支援的用戶端</span><span class="sxs-lookup"><span data-stu-id="44e10-168">Minimum supported client</span></span><br/> | <span data-ttu-id="44e10-169">\[僅限 Windows Vista 桌面應用程式\]</span><span class="sxs-lookup"><span data-stu-id="44e10-169">Windows Vista \[desktop apps only\]</span></span><br/>       |
| <span data-ttu-id="44e10-170">最低支援的伺服器</span><span class="sxs-lookup"><span data-stu-id="44e10-170">Minimum supported server</span></span><br/> | <span data-ttu-id="44e10-171">僅限 Windows Server 2008 \[ desktop 應用程式\]</span><span class="sxs-lookup"><span data-stu-id="44e10-171">Windows Server 2008 \[desktop apps only\]</span></span><br/> |



## <a name="see-also"></a><span data-ttu-id="44e10-172">另請參閱</span><span class="sxs-lookup"><span data-stu-id="44e10-172">See also</span></span>

<dl> <dt>

[<span data-ttu-id="44e10-173">**執行緒**</span><span class="sxs-lookup"><span data-stu-id="44e10-173">**Thread**</span></span>](thread.md)
</dt> <dt>

[<span data-ttu-id="44e10-174">**執行緒 \_ V2**</span><span class="sxs-lookup"><span data-stu-id="44e10-174">**Thread\_V2**</span></span>](thread-v2.md)
</dt> </dl>

 

 




