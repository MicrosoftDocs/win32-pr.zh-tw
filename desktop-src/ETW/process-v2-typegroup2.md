---
description: 這個類別是處理常式計數器事件的事件種類類別。 以下是從 MOF 程式碼簡化的語法。
ms.assetid: 7f1fa1c4-a2ff-4a1c-ac9d-e922a13c99a1
title: Process_V2_TypeGroup2 類別
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Process_V2_TypeGroup2
- Process_V2_TypeGroup2.ProcessId
- Process_V2_TypeGroup2.PageFaultCount
- Process_V2_TypeGroup2.HandleCount
- Process_V2_TypeGroup2.Reserved
- Process_V2_TypeGroup2.PeakVirtualSize
- Process_V2_TypeGroup2.PeakWorkingSetSize
- Process_V2_TypeGroup2.PeakPagefileUsage
- Process_V2_TypeGroup2.QuotaPeakPagedPoolUsage
- Process_V2_TypeGroup2.QuotaPeakNonPagedPoolUsage
- Process_V2_TypeGroup2.VirtualSize
- Process_V2_TypeGroup2.WorkingSetSize
- Process_V2_TypeGroup2.PagefileUsage
- Process_V2_TypeGroup2.QuotaPagedPoolUsage
- Process_V2_TypeGroup2.QuotaNonPagedPoolUsage
- Process_V2_TypeGroup2.PrivatePageCount
api_type:
- NA
api_location: ''
ms.openlocfilehash: 284b77da03b53f9c2662c8729a7bf6606c45630a
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/08/2021
ms.locfileid: "103851591"
---
# <a name="process_v2_typegroup2-class"></a><span data-ttu-id="0d561-104">進程 \_ V2 \_ TypeGroup2 類別</span><span class="sxs-lookup"><span data-stu-id="0d561-104">Process\_V2\_TypeGroup2 class</span></span>

<span data-ttu-id="0d561-105">這個類別是處理常式計數器事件的事件種類類別。</span><span class="sxs-lookup"><span data-stu-id="0d561-105">This class is the event type class for process counter events.</span></span>

<span data-ttu-id="0d561-106">以下是從 MOF 程式碼簡化的語法。</span><span class="sxs-lookup"><span data-stu-id="0d561-106">The following syntax is simplified from MOF code.</span></span>

## <a name="syntax"></a><span data-ttu-id="0d561-107">語法</span><span class="sxs-lookup"><span data-stu-id="0d561-107">Syntax</span></span>

``` syntax
[EventType{32, 33}, EventTypeName{"PerfCtr", PerfCtrRundown"}]
class Process_V2_TypeGroup2 : Process_V2
{
  uint32 ProcessId;
  uint32 PageFaultCount;
  uint32 HandleCount;
  uint32 Reserved;
  object PeakVirtualSize;
  object PeakWorkingSetSize;
  object PeakPagefileUsage;
  object QuotaPeakPagedPoolUsage;
  object QuotaPeakNonPagedPoolUsage;
  object VirtualSize;
  object WorkingSetSize;
  object PagefileUsage;
  object QuotaPagedPoolUsage;
  object QuotaNonPagedPoolUsage;
  object PrivatePageCount;
};
```

## <a name="members"></a><span data-ttu-id="0d561-108">成員</span><span class="sxs-lookup"><span data-stu-id="0d561-108">Members</span></span>

<span data-ttu-id="0d561-109">**Process \_ V2 \_ TypeGroup2** 類別具有下列類型的成員：</span><span class="sxs-lookup"><span data-stu-id="0d561-109">The **Process\_V2\_TypeGroup2** class has these types of members:</span></span>

-   [<span data-ttu-id="0d561-110">屬性</span><span class="sxs-lookup"><span data-stu-id="0d561-110">Properties</span></span>](#properties)

### <a name="properties"></a><span data-ttu-id="0d561-111">屬性</span><span class="sxs-lookup"><span data-stu-id="0d561-111">Properties</span></span>

<span data-ttu-id="0d561-112">**Process \_ V2 \_ TypeGroup2** 類別具有這些屬性。</span><span class="sxs-lookup"><span data-stu-id="0d561-112">The **Process\_V2\_TypeGroup2** class has these properties.</span></span>

<dl> <dt>

<span data-ttu-id="0d561-113">**HandleCount**</span><span class="sxs-lookup"><span data-stu-id="0d561-113">**HandleCount**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="0d561-114">資料類型： **uint32**</span><span class="sxs-lookup"><span data-stu-id="0d561-114">Data type: **uint32**</span></span>
</dt> <dt>

<span data-ttu-id="0d561-115">存取類型：唯讀</span><span class="sxs-lookup"><span data-stu-id="0d561-115">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="0d561-116">限定詞： WmiDataId (3) </span><span class="sxs-lookup"><span data-stu-id="0d561-116">Qualifiers: WmiDataId(3)</span></span>
</dt> </dl>

<span data-ttu-id="0d561-117">使用的控制碼計數。</span><span class="sxs-lookup"><span data-stu-id="0d561-117">Count of used handles.</span></span>

</dd> <dt>

<span data-ttu-id="0d561-118">**PageFaultCount**</span><span class="sxs-lookup"><span data-stu-id="0d561-118">**PageFaultCount**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="0d561-119">資料類型： **uint32**</span><span class="sxs-lookup"><span data-stu-id="0d561-119">Data type: **uint32**</span></span>
</dt> <dt>

<span data-ttu-id="0d561-120">存取類型：唯讀</span><span class="sxs-lookup"><span data-stu-id="0d561-120">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="0d561-121">限定詞： WmiDataId (2) </span><span class="sxs-lookup"><span data-stu-id="0d561-121">Qualifiers: WmiDataId(2)</span></span>
</dt> </dl>

<span data-ttu-id="0d561-122">分頁錯誤的計數。</span><span class="sxs-lookup"><span data-stu-id="0d561-122">Count of page faults.</span></span>

</dd> <dt>

<span data-ttu-id="0d561-123">**PagefileUsage**</span><span class="sxs-lookup"><span data-stu-id="0d561-123">**PagefileUsage**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="0d561-124">資料類型： **物件**</span><span class="sxs-lookup"><span data-stu-id="0d561-124">Data type: **object**</span></span>
</dt> <dt>

<span data-ttu-id="0d561-125">存取類型：唯讀</span><span class="sxs-lookup"><span data-stu-id="0d561-125">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="0d561-126">限定詞： WmiDataId (12) ，副檔名 ( "SizeT" ) </span><span class="sxs-lookup"><span data-stu-id="0d561-126">Qualifiers: WmiDataId(12), Extension("SizeT")</span></span>
</dt> </dl>

<span data-ttu-id="0d561-127">目前的分頁檔案使用方式。</span><span class="sxs-lookup"><span data-stu-id="0d561-127">Current page file usage.</span></span>

</dd> <dt>

<span data-ttu-id="0d561-128">**PeakPagefileUsage**</span><span class="sxs-lookup"><span data-stu-id="0d561-128">**PeakPagefileUsage**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="0d561-129">資料類型： **物件**</span><span class="sxs-lookup"><span data-stu-id="0d561-129">Data type: **object**</span></span>
</dt> <dt>

<span data-ttu-id="0d561-130">存取類型：唯讀</span><span class="sxs-lookup"><span data-stu-id="0d561-130">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="0d561-131">限定詞： WmiDataId (7) ，副檔名 ( "SizeT" ) </span><span class="sxs-lookup"><span data-stu-id="0d561-131">Qualifiers: WmiDataId(7), Extension("SizeT")</span></span>
</dt> </dl>

<span data-ttu-id="0d561-132">使用了最大的頁面檔案大小。</span><span class="sxs-lookup"><span data-stu-id="0d561-132">Largest page file size used.</span></span>

</dd> <dt>

<span data-ttu-id="0d561-133">**PeakVirtualSize**</span><span class="sxs-lookup"><span data-stu-id="0d561-133">**PeakVirtualSize**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="0d561-134">資料類型： **物件**</span><span class="sxs-lookup"><span data-stu-id="0d561-134">Data type: **object**</span></span>
</dt> <dt>

<span data-ttu-id="0d561-135">存取類型：唯讀</span><span class="sxs-lookup"><span data-stu-id="0d561-135">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="0d561-136">限定詞： WmiDataId (5) ，副檔名 ( "SizeT" ) </span><span class="sxs-lookup"><span data-stu-id="0d561-136">Qualifiers: WmiDataId(5), Extension("SizeT")</span></span>
</dt> </dl>

<span data-ttu-id="0d561-137">使用的虛擬頁面大小最大。</span><span class="sxs-lookup"><span data-stu-id="0d561-137">Largest virtual page size used.</span></span>

</dd> <dt>

<span data-ttu-id="0d561-138">**PeakWorkingSetSize**</span><span class="sxs-lookup"><span data-stu-id="0d561-138">**PeakWorkingSetSize**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="0d561-139">資料類型： **物件**</span><span class="sxs-lookup"><span data-stu-id="0d561-139">Data type: **object**</span></span>
</dt> <dt>

<span data-ttu-id="0d561-140">存取類型：唯讀</span><span class="sxs-lookup"><span data-stu-id="0d561-140">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="0d561-141">限定詞： WmiDataId (6) ，副檔名 ( "SizeT" ) </span><span class="sxs-lookup"><span data-stu-id="0d561-141">Qualifiers: WmiDataId(6), Extension("SizeT")</span></span>
</dt> </dl>

<span data-ttu-id="0d561-142">使用了最大的工作集大小。</span><span class="sxs-lookup"><span data-stu-id="0d561-142">Largest working set size used.</span></span>

</dd> <dt>

<span data-ttu-id="0d561-143">**PrivatePageCount**</span><span class="sxs-lookup"><span data-stu-id="0d561-143">**PrivatePageCount**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="0d561-144">資料類型： **物件**</span><span class="sxs-lookup"><span data-stu-id="0d561-144">Data type: **object**</span></span>
</dt> <dt>

<span data-ttu-id="0d561-145">存取類型：唯讀</span><span class="sxs-lookup"><span data-stu-id="0d561-145">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="0d561-146">限定詞： WmiDataId (15) ，副檔名 ( "SizeT" ) </span><span class="sxs-lookup"><span data-stu-id="0d561-146">Qualifiers: WmiDataId(15), Extension("SizeT")</span></span>
</dt> </dl>

<span data-ttu-id="0d561-147">目前的私人實體頁面計數。</span><span class="sxs-lookup"><span data-stu-id="0d561-147">Current private physical page count.</span></span>

</dd> <dt>

<span data-ttu-id="0d561-148">ProcessId</span><span class="sxs-lookup"><span data-stu-id="0d561-148">ProcessId</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="0d561-149">資料類型： **uint32**</span><span class="sxs-lookup"><span data-stu-id="0d561-149">Data type: **uint32**</span></span>
</dt> <dt>

<span data-ttu-id="0d561-150">存取類型：唯讀</span><span class="sxs-lookup"><span data-stu-id="0d561-150">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="0d561-151">限定詞： WmiDataId (1) ，格式 ( "x" ) </span><span class="sxs-lookup"><span data-stu-id="0d561-151">Qualifiers: WmiDataId(1), Format("x")</span></span>
</dt> </dl>

<span data-ttu-id="0d561-152">您可以用來識別進程的全域處理序識別碼。</span><span class="sxs-lookup"><span data-stu-id="0d561-152">Global process identifier that you can use to identify a process.</span></span> <span data-ttu-id="0d561-153">此值從建立進程到終止之前都有效。</span><span class="sxs-lookup"><span data-stu-id="0d561-153">The value is valid from the time a process is created until it is terminated.</span></span>

</dd> <dt>

<span data-ttu-id="0d561-154">**QuotaNonPagedPoolUsage**</span><span class="sxs-lookup"><span data-stu-id="0d561-154">**QuotaNonPagedPoolUsage**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="0d561-155">資料類型： **物件**</span><span class="sxs-lookup"><span data-stu-id="0d561-155">Data type: **object**</span></span>
</dt> <dt>

<span data-ttu-id="0d561-156">存取類型：唯讀</span><span class="sxs-lookup"><span data-stu-id="0d561-156">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="0d561-157">限定詞： WmiDataId (14) ，副檔名 ( "SizeT" ) </span><span class="sxs-lookup"><span data-stu-id="0d561-157">Qualifiers: WmiDataId(14), Extension("SizeT")</span></span>
</dt> </dl>

<span data-ttu-id="0d561-158">目前認可的非分頁式記憶體使用量。</span><span class="sxs-lookup"><span data-stu-id="0d561-158">Current committed non-paged memory usage.</span></span>

</dd> <dt>

<span data-ttu-id="0d561-159">**QuotaPagedPoolUsage**</span><span class="sxs-lookup"><span data-stu-id="0d561-159">**QuotaPagedPoolUsage**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="0d561-160">資料類型： **物件**</span><span class="sxs-lookup"><span data-stu-id="0d561-160">Data type: **object**</span></span>
</dt> <dt>

<span data-ttu-id="0d561-161">存取類型：唯讀</span><span class="sxs-lookup"><span data-stu-id="0d561-161">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="0d561-162">限定詞： WmiDataId (13) ，副檔名 ( "SizeT" ) </span><span class="sxs-lookup"><span data-stu-id="0d561-162">Qualifiers: WmiDataId(13), Extension("SizeT")</span></span>
</dt> </dl>

<span data-ttu-id="0d561-163">目前已認可的分頁記憶體使用量。</span><span class="sxs-lookup"><span data-stu-id="0d561-163">Current committed paged memory usage.</span></span>

</dd> <dt>

<span data-ttu-id="0d561-164">**QuotaPeakNonPagedPoolUsage**</span><span class="sxs-lookup"><span data-stu-id="0d561-164">**QuotaPeakNonPagedPoolUsage**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="0d561-165">資料類型： **物件**</span><span class="sxs-lookup"><span data-stu-id="0d561-165">Data type: **object**</span></span>
</dt> <dt>

<span data-ttu-id="0d561-166">存取類型：唯讀</span><span class="sxs-lookup"><span data-stu-id="0d561-166">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="0d561-167">限定詞： WmiDataId (9) ，副檔名 ( "SizeT" ) </span><span class="sxs-lookup"><span data-stu-id="0d561-167">Qualifiers: WmiDataId(9), Extension("SizeT")</span></span>
</dt> </dl>

<span data-ttu-id="0d561-168">使用的最大認可非分頁式記憶體。</span><span class="sxs-lookup"><span data-stu-id="0d561-168">Largest committed non-paged memory used.</span></span>

</dd> <dt>

<span data-ttu-id="0d561-169">**QuotaPeakPagedPoolUsage**</span><span class="sxs-lookup"><span data-stu-id="0d561-169">**QuotaPeakPagedPoolUsage**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="0d561-170">資料類型： **物件**</span><span class="sxs-lookup"><span data-stu-id="0d561-170">Data type: **object**</span></span>
</dt> <dt>

<span data-ttu-id="0d561-171">存取類型：唯讀</span><span class="sxs-lookup"><span data-stu-id="0d561-171">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="0d561-172">限定詞： WmiDataId (8) ，副檔名 ( "SizeT" ) </span><span class="sxs-lookup"><span data-stu-id="0d561-172">Qualifiers: WmiDataId(8), Extension("SizeT")</span></span>
</dt> </dl>

<span data-ttu-id="0d561-173">使用的最大認可分頁記憶體。</span><span class="sxs-lookup"><span data-stu-id="0d561-173">Largest committed paged memory used.</span></span>

</dd> <dt>

<span data-ttu-id="0d561-174">**已保留**</span><span class="sxs-lookup"><span data-stu-id="0d561-174">**Reserved**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="0d561-175">資料類型： **uint32**</span><span class="sxs-lookup"><span data-stu-id="0d561-175">Data type: **uint32**</span></span>
</dt> <dt>

<span data-ttu-id="0d561-176">存取類型：唯讀</span><span class="sxs-lookup"><span data-stu-id="0d561-176">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="0d561-177">限定詞： WmiDataId (4) </span><span class="sxs-lookup"><span data-stu-id="0d561-177">Qualifiers: WmiDataId(4)</span></span>
</dt> </dl>

<span data-ttu-id="0d561-178">保留的。</span><span class="sxs-lookup"><span data-stu-id="0d561-178">Reserved.</span></span>

</dd> <dt>

<span data-ttu-id="0d561-179">**VirtualSize**</span><span class="sxs-lookup"><span data-stu-id="0d561-179">**VirtualSize**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="0d561-180">資料類型： **物件**</span><span class="sxs-lookup"><span data-stu-id="0d561-180">Data type: **object**</span></span>
</dt> <dt>

<span data-ttu-id="0d561-181">存取類型：唯讀</span><span class="sxs-lookup"><span data-stu-id="0d561-181">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="0d561-182">限定詞： WmiDataId (10) ，副檔名 ( "SizeT" ) </span><span class="sxs-lookup"><span data-stu-id="0d561-182">Qualifiers: WmiDataId(10), Extension("SizeT")</span></span>
</dt> </dl>

<span data-ttu-id="0d561-183">目前的虛擬頁面大小。</span><span class="sxs-lookup"><span data-stu-id="0d561-183">Current virtual page size.</span></span>

</dd> <dt>

<span data-ttu-id="0d561-184">**WorkingSetSize**</span><span class="sxs-lookup"><span data-stu-id="0d561-184">**WorkingSetSize**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="0d561-185">資料類型： **物件**</span><span class="sxs-lookup"><span data-stu-id="0d561-185">Data type: **object**</span></span>
</dt> <dt>

<span data-ttu-id="0d561-186">存取類型：唯讀</span><span class="sxs-lookup"><span data-stu-id="0d561-186">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="0d561-187">限定詞： WmiDataId (11) ，副檔名 ( "SizeT" ) </span><span class="sxs-lookup"><span data-stu-id="0d561-187">Qualifiers: WmiDataId(11), Extension("SizeT")</span></span>
</dt> </dl>

<span data-ttu-id="0d561-188">目前的工作集大小。</span><span class="sxs-lookup"><span data-stu-id="0d561-188">Current working set size.</span></span>

</dd> </dl>

## <a name="remarks"></a><span data-ttu-id="0d561-189">備註</span><span class="sxs-lookup"><span data-stu-id="0d561-189">Remarks</span></span>

<span data-ttu-id="0d561-190">當進程結束時，會記錄這些事件。</span><span class="sxs-lookup"><span data-stu-id="0d561-190">These events are logged when the process ends.</span></span> <span data-ttu-id="0d561-191">此事件表示進程處理記憶體使用量的方式。</span><span class="sxs-lookup"><span data-stu-id="0d561-191">The event indicates how a process handled memory usage.</span></span>

## <a name="requirements"></a><span data-ttu-id="0d561-192">規格需求</span><span class="sxs-lookup"><span data-stu-id="0d561-192">Requirements</span></span>



| <span data-ttu-id="0d561-193">需求</span><span class="sxs-lookup"><span data-stu-id="0d561-193">Requirement</span></span> | <span data-ttu-id="0d561-194">值</span><span class="sxs-lookup"><span data-stu-id="0d561-194">Value</span></span> |
|-------------------------------------|------------------------------------------------------|
| <span data-ttu-id="0d561-195">最低支援的用戶端</span><span class="sxs-lookup"><span data-stu-id="0d561-195">Minimum supported client</span></span><br/> | <span data-ttu-id="0d561-196">\[僅限 Windows Vista 桌面應用程式\]</span><span class="sxs-lookup"><span data-stu-id="0d561-196">Windows Vista \[desktop apps only\]</span></span><br/>       |
| <span data-ttu-id="0d561-197">最低支援的伺服器</span><span class="sxs-lookup"><span data-stu-id="0d561-197">Minimum supported server</span></span><br/> | <span data-ttu-id="0d561-198">僅限 Windows Server 2008 \[ desktop 應用程式\]</span><span class="sxs-lookup"><span data-stu-id="0d561-198">Windows Server 2008 \[desktop apps only\]</span></span><br/> |



## <a name="see-also"></a><span data-ttu-id="0d561-199">另請參閱</span><span class="sxs-lookup"><span data-stu-id="0d561-199">See also</span></span>

<dl> <dt>

[<span data-ttu-id="0d561-200">**進程 \_ V2**</span><span class="sxs-lookup"><span data-stu-id="0d561-200">**Process\_V2**</span></span>](process-v2.md)
</dt> </dl>

 

 




