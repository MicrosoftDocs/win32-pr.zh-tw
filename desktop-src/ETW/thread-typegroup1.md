---
description: 這個類別是執行緒開始和結束事件的事件種類類別。 以下是從 MOF 程式碼簡化的語法。
ms.assetid: d9e3e33a-0e59-4753-a8d8-5320cbae9d95
title: Thread_TypeGroup1 類別
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Thread_TypeGroup1
- Thread_TypeGroup1.ProcessId
- Thread_TypeGroup1.TThreadId
- Thread_TypeGroup1.StackBase
- Thread_TypeGroup1.StackLimit
- Thread_TypeGroup1.UserStackBase
- Thread_TypeGroup1.UserStackLimit
- Thread_TypeGroup1.Affinity
- Thread_TypeGroup1.Win32StartAddr
- Thread_TypeGroup1.TebBase
- Thread_TypeGroup1.SubProcessTag
- Thread_TypeGroup1.BasePriority
- Thread_TypeGroup1.PagePriority
- Thread_TypeGroup1.IoPriority
- Thread_TypeGroup1.ThreadFlags
api_type:
- NA
api_location: ''
ms.openlocfilehash: 75352efbe044f5fee837c496c394fe28e2dbbbfb
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/07/2021
ms.locfileid: "104114589"
---
# <a name="thread_typegroup1-class"></a><span data-ttu-id="41c34-104">Thread \_ TypeGroup1 類別</span><span class="sxs-lookup"><span data-stu-id="41c34-104">Thread\_TypeGroup1 class</span></span>

<span data-ttu-id="41c34-105">這個類別是執行緒開始和結束事件的事件種類類別。</span><span class="sxs-lookup"><span data-stu-id="41c34-105">This class is the event type class for thread start and end events.</span></span>

<span data-ttu-id="41c34-106">以下是從 MOF 程式碼簡化的語法。</span><span class="sxs-lookup"><span data-stu-id="41c34-106">The following syntax is simplified from MOF code.</span></span>

## <a name="syntax"></a><span data-ttu-id="41c34-107">語法</span><span class="sxs-lookup"><span data-stu-id="41c34-107">Syntax</span></span>

``` syntax
[EventType{1, 2, 3, 4}, EventTypeName{"Start", "End", "DCStart", "DCEnd"}]
class Thread_TypeGroup1 : Thread
{
  uint32 ProcessId;
  uint32 TThreadId;
  uint32 StackBase;
  uint32 StackLimit;
  uint32 UserStackBase;
  uint32 UserStackLimit;
  uint32 Affinity;
  uint32 Win32StartAddr;
  uint32 TebBase;
  uint32 SubProcessTag;
  uint8  BasePriority;
  uint8  PagePriority;
  uint8  IoPriority;
  uint8  ThreadFlags;
};
```

## <a name="members"></a><span data-ttu-id="41c34-108">成員</span><span class="sxs-lookup"><span data-stu-id="41c34-108">Members</span></span>

<span data-ttu-id="41c34-109">**Thread \_ TypeGroup1** 類別具有下列類型的成員：</span><span class="sxs-lookup"><span data-stu-id="41c34-109">The **Thread\_TypeGroup1** class has these types of members:</span></span>

-   [<span data-ttu-id="41c34-110">屬性</span><span class="sxs-lookup"><span data-stu-id="41c34-110">Properties</span></span>](#properties)

### <a name="properties"></a><span data-ttu-id="41c34-111">屬性</span><span class="sxs-lookup"><span data-stu-id="41c34-111">Properties</span></span>

<span data-ttu-id="41c34-112">**Thread \_ TypeGroup1** 類別具有這些屬性。</span><span class="sxs-lookup"><span data-stu-id="41c34-112">The **Thread\_TypeGroup1** class has these properties.</span></span>

<dl> <dt>

<span data-ttu-id="41c34-113">親和性</span><span class="sxs-lookup"><span data-stu-id="41c34-113">Affinity</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="41c34-114">資料類型： **uint32**</span><span class="sxs-lookup"><span data-stu-id="41c34-114">Data type: **uint32**</span></span>
</dt> <dt>

<span data-ttu-id="41c34-115">存取類型：唯讀</span><span class="sxs-lookup"><span data-stu-id="41c34-115">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="41c34-116">限定詞： WmiDataId (7) ，指標</span><span class="sxs-lookup"><span data-stu-id="41c34-116">Qualifiers: WmiDataId(7), Pointer</span></span>
</dt> </dl>

<span data-ttu-id="41c34-117">允許執行緒執行的一組處理器。</span><span class="sxs-lookup"><span data-stu-id="41c34-117">The set of processors on which the thread is allowed to run.</span></span>

</dd> <dt>

<span data-ttu-id="41c34-118">根據 basepriority</span><span class="sxs-lookup"><span data-stu-id="41c34-118">BasePriority</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="41c34-119">資料類型： **uint8**</span><span class="sxs-lookup"><span data-stu-id="41c34-119">Data type: **uint8**</span></span>
</dt> <dt>

<span data-ttu-id="41c34-120">存取類型：唯讀</span><span class="sxs-lookup"><span data-stu-id="41c34-120">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="41c34-121">限定詞： WmiDataId (11) </span><span class="sxs-lookup"><span data-stu-id="41c34-121">Qualifiers: WmiDataId(11)</span></span>
</dt> </dl>

<span data-ttu-id="41c34-122">執行緒的排程器優先權 (查看 [**SetThreadPriority**](/windows/win32/api/processthreadsapi/nf-processthreadsapi-setthreadpriority) 函數) 。</span><span class="sxs-lookup"><span data-stu-id="41c34-122">The scheduler priority of the thread (see the [**SetThreadPriority**](/windows/win32/api/processthreadsapi/nf-processthreadsapi-setthreadpriority) function).</span></span>

</dd> <dt>

<span data-ttu-id="41c34-123">IoPriority</span><span class="sxs-lookup"><span data-stu-id="41c34-123">IoPriority</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="41c34-124">資料類型： **uint8**</span><span class="sxs-lookup"><span data-stu-id="41c34-124">Data type: **uint8**</span></span>
</dt> <dt>

<span data-ttu-id="41c34-125">存取類型：唯讀</span><span class="sxs-lookup"><span data-stu-id="41c34-125">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="41c34-126">限定詞： WmiDataId (13) </span><span class="sxs-lookup"><span data-stu-id="41c34-126">Qualifiers: WmiDataId(13)</span></span>
</dt> </dl>

<span data-ttu-id="41c34-127">用於排程由執行緒產生之 IOs 的 IO 優先權提示。</span><span class="sxs-lookup"><span data-stu-id="41c34-127">An IO priority hint for scheduling IOs generated by the thread.</span></span>

</dd> <dt>

<span data-ttu-id="41c34-128">PagePriority</span><span class="sxs-lookup"><span data-stu-id="41c34-128">PagePriority</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="41c34-129">資料類型： **uint8**</span><span class="sxs-lookup"><span data-stu-id="41c34-129">Data type: **uint8**</span></span>
</dt> <dt>

<span data-ttu-id="41c34-130">存取類型：唯讀</span><span class="sxs-lookup"><span data-stu-id="41c34-130">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="41c34-131">限定詞： WmiDataId (12) </span><span class="sxs-lookup"><span data-stu-id="41c34-131">Qualifiers: WmiDataId(12)</span></span>
</dt> </dl>

<span data-ttu-id="41c34-132">執行緒所存取記憶體頁面的記憶體頁面優先權提示。</span><span class="sxs-lookup"><span data-stu-id="41c34-132">A memory page priority hint for memory pages accessed by the thread.</span></span>

</dd> <dt>

<span data-ttu-id="41c34-133">ProcessId</span><span class="sxs-lookup"><span data-stu-id="41c34-133">ProcessId</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="41c34-134">資料類型： **uint32**</span><span class="sxs-lookup"><span data-stu-id="41c34-134">Data type: **uint32**</span></span>
</dt> <dt>

<span data-ttu-id="41c34-135">存取類型：唯讀</span><span class="sxs-lookup"><span data-stu-id="41c34-135">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="41c34-136">限定詞： WmiDataId (1) ，格式 ( "x" ) </span><span class="sxs-lookup"><span data-stu-id="41c34-136">Qualifiers: WmiDataId(1), Format("x")</span></span>
</dt> </dl>

<span data-ttu-id="41c34-137">事件所涉及之執行緒的處理序識別碼。</span><span class="sxs-lookup"><span data-stu-id="41c34-137">Process identifier of the thread involved in the event.</span></span>

</dd> <dt>

<span data-ttu-id="41c34-138">StackBase</span><span class="sxs-lookup"><span data-stu-id="41c34-138">StackBase</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="41c34-139">資料類型： **uint32**</span><span class="sxs-lookup"><span data-stu-id="41c34-139">Data type: **uint32**</span></span>
</dt> <dt>

<span data-ttu-id="41c34-140">存取類型：唯讀</span><span class="sxs-lookup"><span data-stu-id="41c34-140">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="41c34-141">限定詞： WmiDataId (3) ，指標</span><span class="sxs-lookup"><span data-stu-id="41c34-141">Qualifiers: WmiDataId(3), Pointer</span></span>
</dt> </dl>

<span data-ttu-id="41c34-142">執行緒堆疊的基底位址。</span><span class="sxs-lookup"><span data-stu-id="41c34-142">Base address of the thread's stack.</span></span>

</dd> <dt>

<span data-ttu-id="41c34-143">StackLimit</span><span class="sxs-lookup"><span data-stu-id="41c34-143">StackLimit</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="41c34-144">資料類型： **uint32**</span><span class="sxs-lookup"><span data-stu-id="41c34-144">Data type: **uint32**</span></span>
</dt> <dt>

<span data-ttu-id="41c34-145">存取類型：唯讀</span><span class="sxs-lookup"><span data-stu-id="41c34-145">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="41c34-146">限定詞： WmiDataId (4) ，指標</span><span class="sxs-lookup"><span data-stu-id="41c34-146">Qualifiers: WmiDataId(4), Pointer</span></span>
</dt> </dl>

<span data-ttu-id="41c34-147">執行緒堆疊的限制。</span><span class="sxs-lookup"><span data-stu-id="41c34-147">Limit of the thread's stack.</span></span>

</dd> <dt>

<span data-ttu-id="41c34-148">SubProcessTag</span><span class="sxs-lookup"><span data-stu-id="41c34-148">SubProcessTag</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="41c34-149">資料類型： **uint32**</span><span class="sxs-lookup"><span data-stu-id="41c34-149">Data type: **uint32**</span></span>
</dt> <dt>

<span data-ttu-id="41c34-150">存取類型：唯讀</span><span class="sxs-lookup"><span data-stu-id="41c34-150">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="41c34-151">限定詞： WmiDataId (10) ，格式 ( "x" ) </span><span class="sxs-lookup"><span data-stu-id="41c34-151">Qualifiers: WmiDataId(10), Format("x")</span></span>
</dt> </dl>

<span data-ttu-id="41c34-152">識別服務（如果執行緒是由服務所擁有）;否則為零。</span><span class="sxs-lookup"><span data-stu-id="41c34-152">Identifies the service if the thread is owned by a service; otherwise, zero.</span></span>

</dd> <dt>

<span data-ttu-id="41c34-153">TebBase</span><span class="sxs-lookup"><span data-stu-id="41c34-153">TebBase</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="41c34-154">資料類型： **uint32**</span><span class="sxs-lookup"><span data-stu-id="41c34-154">Data type: **uint32**</span></span>
</dt> <dt>

<span data-ttu-id="41c34-155">存取類型：唯讀</span><span class="sxs-lookup"><span data-stu-id="41c34-155">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="41c34-156">限定詞： WmiDataId (9) ，指標</span><span class="sxs-lookup"><span data-stu-id="41c34-156">Qualifiers: WmiDataId(9), Pointer</span></span>
</dt> </dl>

<span data-ttu-id="41c34-157">執行緒環境區塊基底位址。</span><span class="sxs-lookup"><span data-stu-id="41c34-157">Thread environment block base address.</span></span>

</dd> <dt>

<span data-ttu-id="41c34-158">ThreadFlags</span><span class="sxs-lookup"><span data-stu-id="41c34-158">ThreadFlags</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="41c34-159">資料類型： **uint8**</span><span class="sxs-lookup"><span data-stu-id="41c34-159">Data type: **uint8**</span></span>
</dt> <dt>

<span data-ttu-id="41c34-160">存取類型：唯讀</span><span class="sxs-lookup"><span data-stu-id="41c34-160">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="41c34-161">限定詞： WmiDataId (14) </span><span class="sxs-lookup"><span data-stu-id="41c34-161">Qualifiers: WmiDataId(14)</span></span>
</dt> </dl>

<span data-ttu-id="41c34-162">未使用。</span><span class="sxs-lookup"><span data-stu-id="41c34-162">Not used.</span></span>

</dd> <dt>

<span data-ttu-id="41c34-163">TThreadId</span><span class="sxs-lookup"><span data-stu-id="41c34-163">TThreadId</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="41c34-164">資料類型： **uint32**</span><span class="sxs-lookup"><span data-stu-id="41c34-164">Data type: **uint32**</span></span>
</dt> <dt>

<span data-ttu-id="41c34-165">存取類型：唯讀</span><span class="sxs-lookup"><span data-stu-id="41c34-165">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="41c34-166">限定詞： WmiDataId (2) ，格式 ( "x" ) </span><span class="sxs-lookup"><span data-stu-id="41c34-166">Qualifiers: WmiDataId(2), Format("x")</span></span>
</dt> </dl>

<span data-ttu-id="41c34-167">事件所涉及之執行緒的執行緒識別碼。</span><span class="sxs-lookup"><span data-stu-id="41c34-167">Thread identifier of the thread involved in the event.</span></span>

</dd> <dt>

<span data-ttu-id="41c34-168">UserStackBase</span><span class="sxs-lookup"><span data-stu-id="41c34-168">UserStackBase</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="41c34-169">資料類型： **uint32**</span><span class="sxs-lookup"><span data-stu-id="41c34-169">Data type: **uint32**</span></span>
</dt> <dt>

<span data-ttu-id="41c34-170">存取類型：唯讀</span><span class="sxs-lookup"><span data-stu-id="41c34-170">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="41c34-171">限定詞： WmiDataId (5) ，指標</span><span class="sxs-lookup"><span data-stu-id="41c34-171">Qualifiers: WmiDataId(5), Pointer</span></span>
</dt> </dl>

<span data-ttu-id="41c34-172">執行緒使用者模式堆疊的基底位址。</span><span class="sxs-lookup"><span data-stu-id="41c34-172">Base address of the thread's user-mode stack.</span></span>

</dd> <dt>

<span data-ttu-id="41c34-173">UserStackLimit</span><span class="sxs-lookup"><span data-stu-id="41c34-173">UserStackLimit</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="41c34-174">資料類型： **uint32**</span><span class="sxs-lookup"><span data-stu-id="41c34-174">Data type: **uint32**</span></span>
</dt> <dt>

<span data-ttu-id="41c34-175">存取類型：唯讀</span><span class="sxs-lookup"><span data-stu-id="41c34-175">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="41c34-176">限定詞： WmiDataId (6) ，指標</span><span class="sxs-lookup"><span data-stu-id="41c34-176">Qualifiers: WmiDataId(6), Pointer</span></span>
</dt> </dl>

<span data-ttu-id="41c34-177">執行緒使用者模式堆疊的限制。</span><span class="sxs-lookup"><span data-stu-id="41c34-177">Limit of the thread's user-mode stack.</span></span>

</dd> <dt>

<span data-ttu-id="41c34-178">Win32StartAddr</span><span class="sxs-lookup"><span data-stu-id="41c34-178">Win32StartAddr</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="41c34-179">資料類型： **uint32**</span><span class="sxs-lookup"><span data-stu-id="41c34-179">Data type: **uint32**</span></span>
</dt> <dt>

<span data-ttu-id="41c34-180">存取類型：唯讀</span><span class="sxs-lookup"><span data-stu-id="41c34-180">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="41c34-181">限定詞： WmiDataId (8) ，指標</span><span class="sxs-lookup"><span data-stu-id="41c34-181">Qualifiers: WmiDataId(8), Pointer</span></span>
</dt> </dl>

<span data-ttu-id="41c34-182">此執行緒要執行之函式的起始位址。</span><span class="sxs-lookup"><span data-stu-id="41c34-182">Starting address of the function to be executed by this thread.</span></span>

</dd> </dl>

## <a name="remarks"></a><span data-ttu-id="41c34-183">備註</span><span class="sxs-lookup"><span data-stu-id="41c34-183">Remarks</span></span>

<span data-ttu-id="41c34-184">DCStart 和 DCEnd 事件種類會列舉核心會話開始和結束時，目前正在執行的執行緒。</span><span class="sxs-lookup"><span data-stu-id="41c34-184">The DCStart and DCEnd event types enumerate the threads that are currently running at the time the kernel session starts and ends, respectively.</span></span>

## <a name="requirements"></a><span data-ttu-id="41c34-185">規格需求</span><span class="sxs-lookup"><span data-stu-id="41c34-185">Requirements</span></span>



| <span data-ttu-id="41c34-186">需求</span><span class="sxs-lookup"><span data-stu-id="41c34-186">Requirement</span></span> | <span data-ttu-id="41c34-187">值</span><span class="sxs-lookup"><span data-stu-id="41c34-187">Value</span></span> |
|-------------------------------------|------------------------------------------------------|
| <span data-ttu-id="41c34-188">最低支援的用戶端</span><span class="sxs-lookup"><span data-stu-id="41c34-188">Minimum supported client</span></span><br/> | <span data-ttu-id="41c34-189">\[僅限 Windows Vista 桌面應用程式\]</span><span class="sxs-lookup"><span data-stu-id="41c34-189">Windows Vista \[desktop apps only\]</span></span><br/>       |
| <span data-ttu-id="41c34-190">最低支援的伺服器</span><span class="sxs-lookup"><span data-stu-id="41c34-190">Minimum supported server</span></span><br/> | <span data-ttu-id="41c34-191">僅限 Windows Server 2008 \[ desktop 應用程式\]</span><span class="sxs-lookup"><span data-stu-id="41c34-191">Windows Server 2008 \[desktop apps only\]</span></span><br/> |



## <a name="see-also"></a><span data-ttu-id="41c34-192">另請參閱</span><span class="sxs-lookup"><span data-stu-id="41c34-192">See also</span></span>

<dl> <dt>

[<span data-ttu-id="41c34-193">**執行緒**</span><span class="sxs-lookup"><span data-stu-id="41c34-193">**Thread**</span></span>](thread.md)
</dt> </dl>

 

 
