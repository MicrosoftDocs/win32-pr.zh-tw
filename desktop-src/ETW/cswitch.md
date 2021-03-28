---
description: 這個類別是內容切換事件的事件種類類別。 以下是從 MOF 程式碼簡化的語法。
ms.assetid: 3f9f84d0-18a9-493c-b104-8236b2bd8404
title: CSwitch 類別
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CSwitch
- CSwitch.NewThreadId
- CSwitch.OldThreadId
- CSwitch.NewThreadPriority
- CSwitch.OldThreadPriority
- CSwitch.PreviousCState
- CSwitch.SpareByte
- CSwitch.OldThreadWaitReason
- CSwitch.OldThreadWaitMode
- CSwitch.OldThreadState
- CSwitch.OldThreadWaitIdealProcessor
- CSwitch.NewThreadWaitTime
- CSwitch.Reserved
api_type:
- NA
api_location: ''
ms.openlocfilehash: 91004ca276140271e8d73c3fc226e83c4e03d1fc
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/07/2021
ms.locfileid: "104191611"
---
# <a name="cswitch-class"></a><span data-ttu-id="d8ebc-104">CSwitch 類別</span><span class="sxs-lookup"><span data-stu-id="d8ebc-104">CSwitch class</span></span>

<span data-ttu-id="d8ebc-105">這個類別是內容切換事件的事件種類類別。</span><span class="sxs-lookup"><span data-stu-id="d8ebc-105">This class is the event type class for context switch events.</span></span>

<span data-ttu-id="d8ebc-106">以下是從 MOF 程式碼簡化的語法。</span><span class="sxs-lookup"><span data-stu-id="d8ebc-106">The following syntax is simplified from MOF code.</span></span>

## <a name="syntax"></a><span data-ttu-id="d8ebc-107">語法</span><span class="sxs-lookup"><span data-stu-id="d8ebc-107">Syntax</span></span>

``` syntax
[EventType{36}, EventTypeName{"CSwitch"}]
class CSwitch : Thread_V2
{
  uint32 NewThreadId;
  uint32 OldThreadId;
  sint8  NewThreadPriority;
  sint8  OldThreadPriority;
  uint8  PreviousCState;
  sint8  SpareByte;
  sint8  OldThreadWaitReason;
  sint8  OldThreadWaitMode;
  sint8  OldThreadState;
  sint8  OldThreadWaitIdealProcessor;
  uint32 NewThreadWaitTime;
  uint32 Reserved;
};
```

## <a name="members"></a><span data-ttu-id="d8ebc-108">成員</span><span class="sxs-lookup"><span data-stu-id="d8ebc-108">Members</span></span>

<span data-ttu-id="d8ebc-109">**CSwitch** 類別具有下列類型的成員：</span><span class="sxs-lookup"><span data-stu-id="d8ebc-109">The **CSwitch** class has these types of members:</span></span>

-   [<span data-ttu-id="d8ebc-110">屬性</span><span class="sxs-lookup"><span data-stu-id="d8ebc-110">Properties</span></span>](#properties)

### <a name="properties"></a><span data-ttu-id="d8ebc-111">屬性</span><span class="sxs-lookup"><span data-stu-id="d8ebc-111">Properties</span></span>

<span data-ttu-id="d8ebc-112">**CSwitch** 類別具有這些屬性。</span><span class="sxs-lookup"><span data-stu-id="d8ebc-112">The **CSwitch** class has these properties.</span></span>

<dl> <dt>

<span data-ttu-id="d8ebc-113">**NewThreadId**</span><span class="sxs-lookup"><span data-stu-id="d8ebc-113">**NewThreadId**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="d8ebc-114">資料類型： **uint32**</span><span class="sxs-lookup"><span data-stu-id="d8ebc-114">Data type: **uint32**</span></span>
</dt> <dt>

<span data-ttu-id="d8ebc-115">存取類型：唯讀</span><span class="sxs-lookup"><span data-stu-id="d8ebc-115">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="d8ebc-116">限定詞： WmiDataId (1) ，格式 ( "x" ) </span><span class="sxs-lookup"><span data-stu-id="d8ebc-116">Qualifiers: WmiDataId(1), Format("x")</span></span>
</dt> </dl>

<span data-ttu-id="d8ebc-117">切換後的新執行緒識別碼。</span><span class="sxs-lookup"><span data-stu-id="d8ebc-117">New thread ID after the switch.</span></span>

</dd> <dt>

<span data-ttu-id="d8ebc-118">**NewThreadPriority**</span><span class="sxs-lookup"><span data-stu-id="d8ebc-118">**NewThreadPriority**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="d8ebc-119">資料類型： **sint8**</span><span class="sxs-lookup"><span data-stu-id="d8ebc-119">Data type: **sint8**</span></span>
</dt> <dt>

<span data-ttu-id="d8ebc-120">存取類型：唯讀</span><span class="sxs-lookup"><span data-stu-id="d8ebc-120">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="d8ebc-121">限定詞： WmiDataId (3) </span><span class="sxs-lookup"><span data-stu-id="d8ebc-121">Qualifiers: WmiDataId(3)</span></span>
</dt> </dl>

<span data-ttu-id="d8ebc-122">新執行緒的執行緒優先權。</span><span class="sxs-lookup"><span data-stu-id="d8ebc-122">Thread priority of the new thread.</span></span>

</dd> <dt>

<span data-ttu-id="d8ebc-123">**NewThreadWaitTime**</span><span class="sxs-lookup"><span data-stu-id="d8ebc-123">**NewThreadWaitTime**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="d8ebc-124">資料類型： **uint32**</span><span class="sxs-lookup"><span data-stu-id="d8ebc-124">Data type: **uint32**</span></span>
</dt> <dt>

<span data-ttu-id="d8ebc-125">存取類型：唯讀</span><span class="sxs-lookup"><span data-stu-id="d8ebc-125">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="d8ebc-126">限定詞： WmiDataId (11) ，格式 ( "x" ) </span><span class="sxs-lookup"><span data-stu-id="d8ebc-126">Qualifiers: WmiDataId(11), Format("x")</span></span>
</dt> </dl>

<span data-ttu-id="d8ebc-127">新執行緒的等候時間。</span><span class="sxs-lookup"><span data-stu-id="d8ebc-127">Wait time for the new thread.</span></span>

</dd> <dt>

<span data-ttu-id="d8ebc-128">**OldThreadId**</span><span class="sxs-lookup"><span data-stu-id="d8ebc-128">**OldThreadId**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="d8ebc-129">資料類型： **uint32**</span><span class="sxs-lookup"><span data-stu-id="d8ebc-129">Data type: **uint32**</span></span>
</dt> <dt>

<span data-ttu-id="d8ebc-130">存取類型：唯讀</span><span class="sxs-lookup"><span data-stu-id="d8ebc-130">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="d8ebc-131">限定詞： WmiDataId (2) ，格式 ( "x" ) </span><span class="sxs-lookup"><span data-stu-id="d8ebc-131">Qualifiers: WmiDataId(2), Format("x")</span></span>
</dt> </dl>

<span data-ttu-id="d8ebc-132">先前的執行緒識別碼。</span><span class="sxs-lookup"><span data-stu-id="d8ebc-132">Previous thread ID.</span></span>

</dd> <dt>

<span data-ttu-id="d8ebc-133">**OldThreadPriority**</span><span class="sxs-lookup"><span data-stu-id="d8ebc-133">**OldThreadPriority**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="d8ebc-134">資料類型： **sint8**</span><span class="sxs-lookup"><span data-stu-id="d8ebc-134">Data type: **sint8**</span></span>
</dt> <dt>

<span data-ttu-id="d8ebc-135">存取類型：唯讀</span><span class="sxs-lookup"><span data-stu-id="d8ebc-135">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="d8ebc-136">限定詞： WmiDataId (4) </span><span class="sxs-lookup"><span data-stu-id="d8ebc-136">Qualifiers: WmiDataId(4)</span></span>
</dt> </dl>

<span data-ttu-id="d8ebc-137">先前線程的執行緒優先權。</span><span class="sxs-lookup"><span data-stu-id="d8ebc-137">Thread priority of the previous thread.</span></span>

</dd> <dt>

<span data-ttu-id="d8ebc-138">**OldThreadState**</span><span class="sxs-lookup"><span data-stu-id="d8ebc-138">**OldThreadState**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="d8ebc-139">資料類型： **sint8**</span><span class="sxs-lookup"><span data-stu-id="d8ebc-139">Data type: **sint8**</span></span>
</dt> <dt>

<span data-ttu-id="d8ebc-140">存取類型：唯讀</span><span class="sxs-lookup"><span data-stu-id="d8ebc-140">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="d8ebc-141">限定詞： WmiDataId (9) </span><span class="sxs-lookup"><span data-stu-id="d8ebc-141">Qualifiers: WmiDataId(9)</span></span>
</dt> </dl>

<span data-ttu-id="d8ebc-142">先前線程的狀態。</span><span class="sxs-lookup"><span data-stu-id="d8ebc-142">State of the previous thread.</span></span> <span data-ttu-id="d8ebc-143">以下是可能的狀態值：</span><span class="sxs-lookup"><span data-stu-id="d8ebc-143">The following are the possible state values:</span></span>

| <span data-ttu-id="d8ebc-144">州</span><span class="sxs-lookup"><span data-stu-id="d8ebc-144">State</span></span> | <span data-ttu-id="d8ebc-145">描述</span><span class="sxs-lookup"><span data-stu-id="d8ebc-145">Description</span></span>                                   |
|-------|-----------------------------------------------|
| <span data-ttu-id="d8ebc-146">0</span><span class="sxs-lookup"><span data-stu-id="d8ebc-146">0</span></span>     | <span data-ttu-id="d8ebc-147">Initialized</span><span class="sxs-lookup"><span data-stu-id="d8ebc-147">Initialized</span></span>                                   |
| <span data-ttu-id="d8ebc-148">1</span><span class="sxs-lookup"><span data-stu-id="d8ebc-148">1</span></span>     | <span data-ttu-id="d8ebc-149">就緒</span><span class="sxs-lookup"><span data-stu-id="d8ebc-149">Ready</span></span>                                         |
| <span data-ttu-id="d8ebc-150">2</span><span class="sxs-lookup"><span data-stu-id="d8ebc-150">2</span></span>     | <span data-ttu-id="d8ebc-151">執行中</span><span class="sxs-lookup"><span data-stu-id="d8ebc-151">Running</span></span>                                       |
| <span data-ttu-id="d8ebc-152">3</span><span class="sxs-lookup"><span data-stu-id="d8ebc-152">3</span></span>     | <span data-ttu-id="d8ebc-153">待命</span><span class="sxs-lookup"><span data-stu-id="d8ebc-153">Standby</span></span>                                       |
| <span data-ttu-id="d8ebc-154">4</span><span class="sxs-lookup"><span data-stu-id="d8ebc-154">4</span></span>     | <span data-ttu-id="d8ebc-155">已終止</span><span class="sxs-lookup"><span data-stu-id="d8ebc-155">Terminated</span></span>                                    |
| <span data-ttu-id="d8ebc-156">5</span><span class="sxs-lookup"><span data-stu-id="d8ebc-156">5</span></span>     | <span data-ttu-id="d8ebc-157">等候中</span><span class="sxs-lookup"><span data-stu-id="d8ebc-157">Waiting</span></span>                                       |
| <span data-ttu-id="d8ebc-158">6</span><span class="sxs-lookup"><span data-stu-id="d8ebc-158">6</span></span>     | <span data-ttu-id="d8ebc-159">轉換</span><span class="sxs-lookup"><span data-stu-id="d8ebc-159">Transition</span></span>                                    |
| <span data-ttu-id="d8ebc-160">7</span><span class="sxs-lookup"><span data-stu-id="d8ebc-160">7</span></span>     | <span data-ttu-id="d8ebc-161">DeferredReady (為 Windows Server 2003) 新增</span><span class="sxs-lookup"><span data-stu-id="d8ebc-161">DeferredReady (added for Windows Server 2003)</span></span> |



 

</dd> <dt>

<span data-ttu-id="d8ebc-162">**OldThreadWaitIdealProcessor**</span><span class="sxs-lookup"><span data-stu-id="d8ebc-162">**OldThreadWaitIdealProcessor**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="d8ebc-163">資料類型： **sint8**</span><span class="sxs-lookup"><span data-stu-id="d8ebc-163">Data type: **sint8**</span></span>
</dt> <dt>

<span data-ttu-id="d8ebc-164">存取類型：唯讀</span><span class="sxs-lookup"><span data-stu-id="d8ebc-164">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="d8ebc-165">限定詞： WmiDataId (10) ，格式 ( "x" ) </span><span class="sxs-lookup"><span data-stu-id="d8ebc-165">Qualifiers: WmiDataId(10), Format("x")</span></span>
</dt> </dl>

<span data-ttu-id="d8ebc-166">先前線程的理想等候時間。</span><span class="sxs-lookup"><span data-stu-id="d8ebc-166">Ideal wait time of the previous thread.</span></span>

</dd> <dt>

<span data-ttu-id="d8ebc-167">**OldThreadWaitMode**</span><span class="sxs-lookup"><span data-stu-id="d8ebc-167">**OldThreadWaitMode**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="d8ebc-168">資料類型： **sint8**</span><span class="sxs-lookup"><span data-stu-id="d8ebc-168">Data type: **sint8**</span></span>
</dt> <dt>

<span data-ttu-id="d8ebc-169">存取類型：唯讀</span><span class="sxs-lookup"><span data-stu-id="d8ebc-169">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="d8ebc-170">限定詞： WmiDataId (8) </span><span class="sxs-lookup"><span data-stu-id="d8ebc-170">Qualifiers: WmiDataId(8)</span></span>
</dt> </dl>

<span data-ttu-id="d8ebc-171">先前線程的等候模式。</span><span class="sxs-lookup"><span data-stu-id="d8ebc-171">Wait mode for the previous thread.</span></span> <span data-ttu-id="d8ebc-172">以下是可能的值：</span><span class="sxs-lookup"><span data-stu-id="d8ebc-172">The following are the possible values:</span></span>

| <span data-ttu-id="d8ebc-173">州</span><span class="sxs-lookup"><span data-stu-id="d8ebc-173">State</span></span> | <span data-ttu-id="d8ebc-174">描述</span><span class="sxs-lookup"><span data-stu-id="d8ebc-174">Description</span></span> |
|-------|-------------|
| <span data-ttu-id="d8ebc-175">0</span><span class="sxs-lookup"><span data-stu-id="d8ebc-175">0</span></span>     | <span data-ttu-id="d8ebc-176">KernelMode</span><span class="sxs-lookup"><span data-stu-id="d8ebc-176">KernelMode</span></span>  |
| <span data-ttu-id="d8ebc-177">1</span><span class="sxs-lookup"><span data-stu-id="d8ebc-177">1</span></span>     | <span data-ttu-id="d8ebc-178">UserMode</span><span class="sxs-lookup"><span data-stu-id="d8ebc-178">UserMode</span></span>    |



 

</dd> <dt>

<span data-ttu-id="d8ebc-179">**OldThreadWaitReason**</span><span class="sxs-lookup"><span data-stu-id="d8ebc-179">**OldThreadWaitReason**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="d8ebc-180">資料類型： **sint8**</span><span class="sxs-lookup"><span data-stu-id="d8ebc-180">Data type: **sint8**</span></span>
</dt> <dt>

<span data-ttu-id="d8ebc-181">存取類型：唯讀</span><span class="sxs-lookup"><span data-stu-id="d8ebc-181">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="d8ebc-182">限定詞： WmiDataId (7) </span><span class="sxs-lookup"><span data-stu-id="d8ebc-182">Qualifiers: WmiDataId(7)</span></span>
</dt> </dl>

<span data-ttu-id="d8ebc-183">先前線程的等候原因。</span><span class="sxs-lookup"><span data-stu-id="d8ebc-183">Wait reason for the previous thread.</span></span> <span data-ttu-id="d8ebc-184">以下是可能的值：</span><span class="sxs-lookup"><span data-stu-id="d8ebc-184">The following are the possible values:</span></span>

| <span data-ttu-id="d8ebc-185">州</span><span class="sxs-lookup"><span data-stu-id="d8ebc-185">State</span></span> | <span data-ttu-id="d8ebc-186">描述</span><span class="sxs-lookup"><span data-stu-id="d8ebc-186">Description</span></span>       |
|-------|-------------------|
| <span data-ttu-id="d8ebc-187">0</span><span class="sxs-lookup"><span data-stu-id="d8ebc-187">0</span></span>     | <span data-ttu-id="d8ebc-188">高階主管</span><span class="sxs-lookup"><span data-stu-id="d8ebc-188">Executive</span></span>         |
| <span data-ttu-id="d8ebc-189">1</span><span class="sxs-lookup"><span data-stu-id="d8ebc-189">1</span></span>     | <span data-ttu-id="d8ebc-190">FreePage</span><span class="sxs-lookup"><span data-stu-id="d8ebc-190">FreePage</span></span>          |
| <span data-ttu-id="d8ebc-191">2</span><span class="sxs-lookup"><span data-stu-id="d8ebc-191">2</span></span>     | <span data-ttu-id="d8ebc-192">PageIn</span><span class="sxs-lookup"><span data-stu-id="d8ebc-192">PageIn</span></span>            |
| <span data-ttu-id="d8ebc-193">3</span><span class="sxs-lookup"><span data-stu-id="d8ebc-193">3</span></span>     | <span data-ttu-id="d8ebc-194">PoolAllocation</span><span class="sxs-lookup"><span data-stu-id="d8ebc-194">PoolAllocation</span></span>    |
| <span data-ttu-id="d8ebc-195">4</span><span class="sxs-lookup"><span data-stu-id="d8ebc-195">4</span></span>     | <span data-ttu-id="d8ebc-196">DelayExecution</span><span class="sxs-lookup"><span data-stu-id="d8ebc-196">DelayExecution</span></span>    |
| <span data-ttu-id="d8ebc-197">5</span><span class="sxs-lookup"><span data-stu-id="d8ebc-197">5</span></span>     | <span data-ttu-id="d8ebc-198">暫止</span><span class="sxs-lookup"><span data-stu-id="d8ebc-198">Suspended</span></span>         |
| <span data-ttu-id="d8ebc-199">6</span><span class="sxs-lookup"><span data-stu-id="d8ebc-199">6</span></span>     | <span data-ttu-id="d8ebc-200">UserRequest</span><span class="sxs-lookup"><span data-stu-id="d8ebc-200">UserRequest</span></span>       |
| <span data-ttu-id="d8ebc-201">7</span><span class="sxs-lookup"><span data-stu-id="d8ebc-201">7</span></span>     | <span data-ttu-id="d8ebc-202">WrExecutive</span><span class="sxs-lookup"><span data-stu-id="d8ebc-202">WrExecutive</span></span>       |
| <span data-ttu-id="d8ebc-203">8</span><span class="sxs-lookup"><span data-stu-id="d8ebc-203">8</span></span>     | <span data-ttu-id="d8ebc-204">WrFreePage</span><span class="sxs-lookup"><span data-stu-id="d8ebc-204">WrFreePage</span></span>        |
| <span data-ttu-id="d8ebc-205">9</span><span class="sxs-lookup"><span data-stu-id="d8ebc-205">9</span></span>     | <span data-ttu-id="d8ebc-206">WrPageIn</span><span class="sxs-lookup"><span data-stu-id="d8ebc-206">WrPageIn</span></span>          |
| <span data-ttu-id="d8ebc-207">10</span><span class="sxs-lookup"><span data-stu-id="d8ebc-207">10</span></span>    | <span data-ttu-id="d8ebc-208">WrPoolAllocation</span><span class="sxs-lookup"><span data-stu-id="d8ebc-208">WrPoolAllocation</span></span>  |
| <span data-ttu-id="d8ebc-209">11</span><span class="sxs-lookup"><span data-stu-id="d8ebc-209">11</span></span>    | <span data-ttu-id="d8ebc-210">WrDelayExecution</span><span class="sxs-lookup"><span data-stu-id="d8ebc-210">WrDelayExecution</span></span>  |
| <span data-ttu-id="d8ebc-211">12</span><span class="sxs-lookup"><span data-stu-id="d8ebc-211">12</span></span>    | <span data-ttu-id="d8ebc-212">WrSuspended</span><span class="sxs-lookup"><span data-stu-id="d8ebc-212">WrSuspended</span></span>       |
| <span data-ttu-id="d8ebc-213">13</span><span class="sxs-lookup"><span data-stu-id="d8ebc-213">13</span></span>    | <span data-ttu-id="d8ebc-214">WrUserRequest</span><span class="sxs-lookup"><span data-stu-id="d8ebc-214">WrUserRequest</span></span>     |
| <span data-ttu-id="d8ebc-215">14</span><span class="sxs-lookup"><span data-stu-id="d8ebc-215">14</span></span>    | <span data-ttu-id="d8ebc-216">WrEventPair</span><span class="sxs-lookup"><span data-stu-id="d8ebc-216">WrEventPair</span></span>       |
| <span data-ttu-id="d8ebc-217">15</span><span class="sxs-lookup"><span data-stu-id="d8ebc-217">15</span></span>    | <span data-ttu-id="d8ebc-218">WrQueue</span><span class="sxs-lookup"><span data-stu-id="d8ebc-218">WrQueue</span></span>           |
| <span data-ttu-id="d8ebc-219">16</span><span class="sxs-lookup"><span data-stu-id="d8ebc-219">16</span></span>    | <span data-ttu-id="d8ebc-220">WrLpcReceive</span><span class="sxs-lookup"><span data-stu-id="d8ebc-220">WrLpcReceive</span></span>      |
| <span data-ttu-id="d8ebc-221">17</span><span class="sxs-lookup"><span data-stu-id="d8ebc-221">17</span></span>    | <span data-ttu-id="d8ebc-222">WrLpcReply</span><span class="sxs-lookup"><span data-stu-id="d8ebc-222">WrLpcReply</span></span>        |
| <span data-ttu-id="d8ebc-223">18</span><span class="sxs-lookup"><span data-stu-id="d8ebc-223">18</span></span>    | <span data-ttu-id="d8ebc-224">WrVirtualMemory</span><span class="sxs-lookup"><span data-stu-id="d8ebc-224">WrVirtualMemory</span></span>   |
| <span data-ttu-id="d8ebc-225">19</span><span class="sxs-lookup"><span data-stu-id="d8ebc-225">19</span></span>    | <span data-ttu-id="d8ebc-226">WrPageOut</span><span class="sxs-lookup"><span data-stu-id="d8ebc-226">WrPageOut</span></span>         |
| <span data-ttu-id="d8ebc-227">20</span><span class="sxs-lookup"><span data-stu-id="d8ebc-227">20</span></span>    | <span data-ttu-id="d8ebc-228">WrRendezvous</span><span class="sxs-lookup"><span data-stu-id="d8ebc-228">WrRendezvous</span></span>      |
| <span data-ttu-id="d8ebc-229">21</span><span class="sxs-lookup"><span data-stu-id="d8ebc-229">21</span></span>    | <span data-ttu-id="d8ebc-230">WrKeyedEvent</span><span class="sxs-lookup"><span data-stu-id="d8ebc-230">WrKeyedEvent</span></span>      |
| <span data-ttu-id="d8ebc-231">22</span><span class="sxs-lookup"><span data-stu-id="d8ebc-231">22</span></span>    | <span data-ttu-id="d8ebc-232">WrTerminated</span><span class="sxs-lookup"><span data-stu-id="d8ebc-232">WrTerminated</span></span>      |
| <span data-ttu-id="d8ebc-233">23</span><span class="sxs-lookup"><span data-stu-id="d8ebc-233">23</span></span>    | <span data-ttu-id="d8ebc-234">WrProcessInSwap</span><span class="sxs-lookup"><span data-stu-id="d8ebc-234">WrProcessInSwap</span></span>   |
| <span data-ttu-id="d8ebc-235">24</span><span class="sxs-lookup"><span data-stu-id="d8ebc-235">24</span></span>    | <span data-ttu-id="d8ebc-236">WrCpuRateControl</span><span class="sxs-lookup"><span data-stu-id="d8ebc-236">WrCpuRateControl</span></span>  |
| <span data-ttu-id="d8ebc-237">25</span><span class="sxs-lookup"><span data-stu-id="d8ebc-237">25</span></span>    | <span data-ttu-id="d8ebc-238">WrCalloutStack</span><span class="sxs-lookup"><span data-stu-id="d8ebc-238">WrCalloutStack</span></span>    |
| <span data-ttu-id="d8ebc-239">26</span><span class="sxs-lookup"><span data-stu-id="d8ebc-239">26</span></span>    | <span data-ttu-id="d8ebc-240">WrKernel</span><span class="sxs-lookup"><span data-stu-id="d8ebc-240">WrKernel</span></span>          |
| <span data-ttu-id="d8ebc-241">27</span><span class="sxs-lookup"><span data-stu-id="d8ebc-241">27</span></span>    | <span data-ttu-id="d8ebc-242">WrResource</span><span class="sxs-lookup"><span data-stu-id="d8ebc-242">WrResource</span></span>        |
| <span data-ttu-id="d8ebc-243">28</span><span class="sxs-lookup"><span data-stu-id="d8ebc-243">28</span></span>    | <span data-ttu-id="d8ebc-244">WrPushLock</span><span class="sxs-lookup"><span data-stu-id="d8ebc-244">WrPushLock</span></span>        |
| <span data-ttu-id="d8ebc-245">29</span><span class="sxs-lookup"><span data-stu-id="d8ebc-245">29</span></span>    | <span data-ttu-id="d8ebc-246">WrMutex</span><span class="sxs-lookup"><span data-stu-id="d8ebc-246">WrMutex</span></span>           |
| <span data-ttu-id="d8ebc-247">30</span><span class="sxs-lookup"><span data-stu-id="d8ebc-247">30</span></span>    | <span data-ttu-id="d8ebc-248">WrQuantumEnd</span><span class="sxs-lookup"><span data-stu-id="d8ebc-248">WrQuantumEnd</span></span>      |
| <span data-ttu-id="d8ebc-249">31</span><span class="sxs-lookup"><span data-stu-id="d8ebc-249">31</span></span>    | <span data-ttu-id="d8ebc-250">WrDispatchInt</span><span class="sxs-lookup"><span data-stu-id="d8ebc-250">WrDispatchInt</span></span>     |
| <span data-ttu-id="d8ebc-251">32</span><span class="sxs-lookup"><span data-stu-id="d8ebc-251">32</span></span>    | <span data-ttu-id="d8ebc-252">WrPreempted</span><span class="sxs-lookup"><span data-stu-id="d8ebc-252">WrPreempted</span></span>       |
| <span data-ttu-id="d8ebc-253">33</span><span class="sxs-lookup"><span data-stu-id="d8ebc-253">33</span></span>    | <span data-ttu-id="d8ebc-254">WrYieldExecution</span><span class="sxs-lookup"><span data-stu-id="d8ebc-254">WrYieldExecution</span></span>  |
| <span data-ttu-id="d8ebc-255">34</span><span class="sxs-lookup"><span data-stu-id="d8ebc-255">34</span></span>    | <span data-ttu-id="d8ebc-256">WrFastMutex</span><span class="sxs-lookup"><span data-stu-id="d8ebc-256">WrFastMutex</span></span>       |
| <span data-ttu-id="d8ebc-257">35</span><span class="sxs-lookup"><span data-stu-id="d8ebc-257">35</span></span>    | <span data-ttu-id="d8ebc-258">WrGuardedMutex</span><span class="sxs-lookup"><span data-stu-id="d8ebc-258">WrGuardedMutex</span></span>    |
| <span data-ttu-id="d8ebc-259">36</span><span class="sxs-lookup"><span data-stu-id="d8ebc-259">36</span></span>    | <span data-ttu-id="d8ebc-260">WrRundown</span><span class="sxs-lookup"><span data-stu-id="d8ebc-260">WrRundown</span></span>         |
| <span data-ttu-id="d8ebc-261">37</span><span class="sxs-lookup"><span data-stu-id="d8ebc-261">37</span></span>    | <span data-ttu-id="d8ebc-262">MaximumWaitReason</span><span class="sxs-lookup"><span data-stu-id="d8ebc-262">MaximumWaitReason</span></span> |



 

</dd> <dt>

<span data-ttu-id="d8ebc-263">**PreviousCState**</span><span class="sxs-lookup"><span data-stu-id="d8ebc-263">**PreviousCState**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="d8ebc-264">資料類型： **uint8**</span><span class="sxs-lookup"><span data-stu-id="d8ebc-264">Data type: **uint8**</span></span>
</dt> <dt>

<span data-ttu-id="d8ebc-265">存取類型：唯讀</span><span class="sxs-lookup"><span data-stu-id="d8ebc-265">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="d8ebc-266">限定詞： WmiDataId (5) </span><span class="sxs-lookup"><span data-stu-id="d8ebc-266">Qualifiers: WmiDataId(5)</span></span>
</dt> </dl>

<span data-ttu-id="d8ebc-267">處理器最後使用之 C 狀態的索引。</span><span class="sxs-lookup"><span data-stu-id="d8ebc-267">The index of the C-state that was last used by the processor.</span></span> <span data-ttu-id="d8ebc-268">值為0表示最亮的閒置狀態，具有較高的值表示更深層的 C 狀態。</span><span class="sxs-lookup"><span data-stu-id="d8ebc-268">A value of 0 represents the lightest idle state with higher values representing deeper C-states.</span></span>

</dd> <dt>

<span data-ttu-id="d8ebc-269">**已保留**</span><span class="sxs-lookup"><span data-stu-id="d8ebc-269">**Reserved**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="d8ebc-270">資料類型： **uint32**</span><span class="sxs-lookup"><span data-stu-id="d8ebc-270">Data type: **uint32**</span></span>
</dt> <dt>

<span data-ttu-id="d8ebc-271">存取類型：唯讀</span><span class="sxs-lookup"><span data-stu-id="d8ebc-271">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="d8ebc-272">限定詞： WmiDataId (12) </span><span class="sxs-lookup"><span data-stu-id="d8ebc-272">Qualifiers: WmiDataId(12)</span></span>
</dt> </dl>

<span data-ttu-id="d8ebc-273">保留的。</span><span class="sxs-lookup"><span data-stu-id="d8ebc-273">Reserved.</span></span>

</dd> <dt>

<span data-ttu-id="d8ebc-274">**SpareByte**</span><span class="sxs-lookup"><span data-stu-id="d8ebc-274">**SpareByte**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="d8ebc-275">資料類型： **sint8**</span><span class="sxs-lookup"><span data-stu-id="d8ebc-275">Data type: **sint8**</span></span>
</dt> <dt>

<span data-ttu-id="d8ebc-276">存取類型：唯讀</span><span class="sxs-lookup"><span data-stu-id="d8ebc-276">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="d8ebc-277">限定詞： WmiDataId (6) </span><span class="sxs-lookup"><span data-stu-id="d8ebc-277">Qualifiers: WmiDataId(6)</span></span>
</dt> </dl>

<span data-ttu-id="d8ebc-278">未使用。</span><span class="sxs-lookup"><span data-stu-id="d8ebc-278">Not used.</span></span>

</dd> </dl>

## <a name="remarks"></a><span data-ttu-id="d8ebc-279">備註</span><span class="sxs-lookup"><span data-stu-id="d8ebc-279">Remarks</span></span>

<span data-ttu-id="d8ebc-280">這些事件會產生大量的事件。</span><span class="sxs-lookup"><span data-stu-id="d8ebc-280">These events produce a high volume of events.</span></span>

## <a name="requirements"></a><span data-ttu-id="d8ebc-281">規格需求</span><span class="sxs-lookup"><span data-stu-id="d8ebc-281">Requirements</span></span>



| <span data-ttu-id="d8ebc-282">需求</span><span class="sxs-lookup"><span data-stu-id="d8ebc-282">Requirement</span></span> | <span data-ttu-id="d8ebc-283">值</span><span class="sxs-lookup"><span data-stu-id="d8ebc-283">Value</span></span> |
|-------------------------------------|------------------------------------------------------|
| <span data-ttu-id="d8ebc-284">最低支援的用戶端</span><span class="sxs-lookup"><span data-stu-id="d8ebc-284">Minimum supported client</span></span><br/> | <span data-ttu-id="d8ebc-285">\[僅限 Windows Vista 桌面應用程式\]</span><span class="sxs-lookup"><span data-stu-id="d8ebc-285">Windows Vista \[desktop apps only\]</span></span><br/>       |
| <span data-ttu-id="d8ebc-286">最低支援的伺服器</span><span class="sxs-lookup"><span data-stu-id="d8ebc-286">Minimum supported server</span></span><br/> | <span data-ttu-id="d8ebc-287">僅限 Windows Server 2008 \[ desktop 應用程式\]</span><span class="sxs-lookup"><span data-stu-id="d8ebc-287">Windows Server 2008 \[desktop apps only\]</span></span><br/> |



## <a name="see-also"></a><span data-ttu-id="d8ebc-288">另請參閱</span><span class="sxs-lookup"><span data-stu-id="d8ebc-288">See also</span></span>

<dl> <dt>

[<span data-ttu-id="d8ebc-289">**執行緒**</span><span class="sxs-lookup"><span data-stu-id="d8ebc-289">**Thread**</span></span>](thread.md)
</dt> <dt>

[<span data-ttu-id="d8ebc-290">**執行緒 \_ V2**</span><span class="sxs-lookup"><span data-stu-id="d8ebc-290">**Thread\_V2**</span></span>](thread-v2.md)
</dt> </dl>

 

 




