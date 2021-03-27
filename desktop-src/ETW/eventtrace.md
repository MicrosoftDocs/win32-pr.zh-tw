---
description: 從中衍生所有事件追蹤類別的抽象類別。
ms.assetid: 03eea902-5050-4ab2-8a72-9bff7777e234
title: EventTrace 類別
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- EventTrace
- EventTrace.EventSize
- EventTrace.ReservedHeaderField
- EventTrace.EventType
- EventTrace.TraceLevel
- EventTrace.TraceVersion
- EventTrace.ThreadId
- EventTrace.TimeStamp
- EventTrace.EventGuid
- EventTrace.KernelTime
- EventTrace.UserTime
- EventTrace.InstanceId
- EventTrace.ParentGuid
- EventTrace.ParentInstanceId
- EventTrace.MofData
- EventTrace.MofLength
api_type:
- NA
api_location: ''
ms.openlocfilehash: f04399942b39a2da5b746933884a436a65bb370c
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/07/2021
ms.locfileid: "103690880"
---
# <a name="eventtrace-class"></a><span data-ttu-id="280c5-103">EventTrace 類別</span><span class="sxs-lookup"><span data-stu-id="280c5-103">EventTrace class</span></span>

<span data-ttu-id="280c5-104">從中衍生所有事件追蹤類別的抽象類別。</span><span class="sxs-lookup"><span data-stu-id="280c5-104">An abstract class from which all event trace classes are derived.</span></span>

<span data-ttu-id="280c5-105">以下是從 MOF 程式碼簡化的語法。</span><span class="sxs-lookup"><span data-stu-id="280c5-105">The following syntax is simplified from MOF code.</span></span>

## <a name="syntax"></a><span data-ttu-id="280c5-106">語法</span><span class="sxs-lookup"><span data-stu-id="280c5-106">Syntax</span></span>

``` syntax
[abstract]
class EventTrace
{
  uint16 EventSize;
  uint16 ReservedHeaderField;
  uint8  EventType;
  uint8  TraceLevel;
  uint16 TraceVersion;
  uint64 ThreadId;
  uint64 TimeStamp;
  uint8  EventGuid[];
  uint32 KernelTime;
  uint32 UserTime;
  uint32 InstanceId;
  uint8  ParentGuid[];
  uint32 ParentInstanceId;
  uint32 MofData;
  uint32 MofLength;
};
```

## <a name="members"></a><span data-ttu-id="280c5-107">成員</span><span class="sxs-lookup"><span data-stu-id="280c5-107">Members</span></span>

<span data-ttu-id="280c5-108">**EventTrace** 類別具有下列類型的成員：</span><span class="sxs-lookup"><span data-stu-id="280c5-108">The **EventTrace** class has these types of members:</span></span>

-   [<span data-ttu-id="280c5-109">屬性</span><span class="sxs-lookup"><span data-stu-id="280c5-109">Properties</span></span>](#properties)

### <a name="properties"></a><span data-ttu-id="280c5-110">屬性</span><span class="sxs-lookup"><span data-stu-id="280c5-110">Properties</span></span>

<span data-ttu-id="280c5-111">**EventTrace** 類別具有這些屬性。</span><span class="sxs-lookup"><span data-stu-id="280c5-111">The **EventTrace** class has these properties.</span></span>

<dl> <dt>

<span data-ttu-id="280c5-112">**EventGuid**</span><span class="sxs-lookup"><span data-stu-id="280c5-112">**EventGuid**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="280c5-113">資料類型： **uint8** 陣列</span><span class="sxs-lookup"><span data-stu-id="280c5-113">Data type: **uint8** array</span></span>
</dt> <dt>

<span data-ttu-id="280c5-114">存取類型：唯讀</span><span class="sxs-lookup"><span data-stu-id="280c5-114">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="280c5-115">限定詞： **WmiDataId** (8) ， **最大** (16) </span><span class="sxs-lookup"><span data-stu-id="280c5-115">Qualifiers: **WmiDataId** (8), **Max** (16)</span></span>
</dt> </dl>

<span data-ttu-id="280c5-116">此事件的事件追蹤類別 GUID。</span><span class="sxs-lookup"><span data-stu-id="280c5-116">Event trace class GUID of this event.</span></span>

</dd> <dt>

<span data-ttu-id="280c5-117">**EventSize**</span><span class="sxs-lookup"><span data-stu-id="280c5-117">**EventSize**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="280c5-118">資料類型： **uint16**</span><span class="sxs-lookup"><span data-stu-id="280c5-118">Data type: **uint16**</span></span>
</dt> <dt>

<span data-ttu-id="280c5-119">存取類型：唯讀</span><span class="sxs-lookup"><span data-stu-id="280c5-119">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="280c5-120">限定詞： **WmiDataId** (1) </span><span class="sxs-lookup"><span data-stu-id="280c5-120">Qualifiers: **WmiDataId** (1)</span></span>
</dt> </dl>

<span data-ttu-id="280c5-121">事件的位元組總數。</span><span class="sxs-lookup"><span data-stu-id="280c5-121">Total number of bytes of the event.</span></span>

</dd> <dt>

<span data-ttu-id="280c5-122">**EventType**</span><span class="sxs-lookup"><span data-stu-id="280c5-122">**EventType**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="280c5-123">資料類型： **uint8**</span><span class="sxs-lookup"><span data-stu-id="280c5-123">Data type: **uint8**</span></span>
</dt> <dt>

<span data-ttu-id="280c5-124">存取類型：唯讀</span><span class="sxs-lookup"><span data-stu-id="280c5-124">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="280c5-125">限定詞： **WmiDataId** (3) </span><span class="sxs-lookup"><span data-stu-id="280c5-125">Qualifiers: **WmiDataId** (3)</span></span>
</dt> </dl>

<span data-ttu-id="280c5-126">提供者定義的事件種類。</span><span class="sxs-lookup"><span data-stu-id="280c5-126">Provider-defined event type.</span></span> <span data-ttu-id="280c5-127">告訴您要使用哪一個事件種類類別來解密提供者定義的事件資料 (**MofData** 所指向的資料。</span><span class="sxs-lookup"><span data-stu-id="280c5-127">Tells you which event type class to use to decipher the provider-defined event data (the data pointed to by **MofData**.</span></span>

</dd> <dt>

<span data-ttu-id="280c5-128">**InstanceId**</span><span class="sxs-lookup"><span data-stu-id="280c5-128">**InstanceId**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="280c5-129">資料類型： **uint32**</span><span class="sxs-lookup"><span data-stu-id="280c5-129">Data type: **uint32**</span></span>
</dt> <dt>

<span data-ttu-id="280c5-130">存取類型：唯讀</span><span class="sxs-lookup"><span data-stu-id="280c5-130">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="280c5-131">限定詞： **WmiDataId** (11) </span><span class="sxs-lookup"><span data-stu-id="280c5-131">Qualifiers: **WmiDataId** (11)</span></span>
</dt> </dl>

<span data-ttu-id="280c5-132">此事件實例的識別碼。</span><span class="sxs-lookup"><span data-stu-id="280c5-132">Identifier of this event instance.</span></span>

</dd> <dt>

<span data-ttu-id="280c5-133">**KernelTime**</span><span class="sxs-lookup"><span data-stu-id="280c5-133">**KernelTime**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="280c5-134">資料類型： **uint32**</span><span class="sxs-lookup"><span data-stu-id="280c5-134">Data type: **uint32**</span></span>
</dt> <dt>

<span data-ttu-id="280c5-135">存取類型：唯讀</span><span class="sxs-lookup"><span data-stu-id="280c5-135">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="280c5-136">限定詞： **WmiDataId** (9) </span><span class="sxs-lookup"><span data-stu-id="280c5-136">Qualifiers: **WmiDataId** (9)</span></span>
</dt> </dl>

<span data-ttu-id="280c5-137">核心模式指令的經過執行時間，以 CPU 滴答為單位。</span><span class="sxs-lookup"><span data-stu-id="280c5-137">Elapsed execution time for kernel-mode instructions, in CPU ticks.</span></span>

</dd> <dt>

<span data-ttu-id="280c5-138">**MofData**</span><span class="sxs-lookup"><span data-stu-id="280c5-138">**MofData**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="280c5-139">資料類型： **uint32**</span><span class="sxs-lookup"><span data-stu-id="280c5-139">Data type: **uint32**</span></span>
</dt> <dt>

<span data-ttu-id="280c5-140">存取類型：唯讀</span><span class="sxs-lookup"><span data-stu-id="280c5-140">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="280c5-141">限定詞： **WmiDataId** (14) ， **指標**</span><span class="sxs-lookup"><span data-stu-id="280c5-141">Qualifiers: **WmiDataId** (14), **Pointer**</span></span>
</dt> </dl>

<span data-ttu-id="280c5-142">提供者特定事件資料的指標。</span><span class="sxs-lookup"><span data-stu-id="280c5-142">Pointer to the provider-specific event data.</span></span>

</dd> <dt>

<span data-ttu-id="280c5-143">**MofLength**</span><span class="sxs-lookup"><span data-stu-id="280c5-143">**MofLength**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="280c5-144">資料類型： **uint32**</span><span class="sxs-lookup"><span data-stu-id="280c5-144">Data type: **uint32**</span></span>
</dt> <dt>

<span data-ttu-id="280c5-145">存取類型：唯讀</span><span class="sxs-lookup"><span data-stu-id="280c5-145">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="280c5-146">限定詞： **WmiDataId** (15) </span><span class="sxs-lookup"><span data-stu-id="280c5-146">Qualifiers: **WmiDataId** (15)</span></span>
</dt> </dl>

<span data-ttu-id="280c5-147">提供者特定事件資料的長度。</span><span class="sxs-lookup"><span data-stu-id="280c5-147">Length of the provider-specific event data.</span></span>

</dd> <dt>

<span data-ttu-id="280c5-148">**ParentGuid**</span><span class="sxs-lookup"><span data-stu-id="280c5-148">**ParentGuid**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="280c5-149">資料類型： **uint8** 陣列</span><span class="sxs-lookup"><span data-stu-id="280c5-149">Data type: **uint8** array</span></span>
</dt> <dt>

<span data-ttu-id="280c5-150">存取類型：唯讀</span><span class="sxs-lookup"><span data-stu-id="280c5-150">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="280c5-151">限定詞： **WmiDataId** (12) ， **最大** (16) </span><span class="sxs-lookup"><span data-stu-id="280c5-151">Qualifiers: **WmiDataId** (12), **Max** (16)</span></span>
</dt> </dl>

<span data-ttu-id="280c5-152">父實例的事件追蹤類別 GUID。</span><span class="sxs-lookup"><span data-stu-id="280c5-152">Event trace class GUID of the parent instance.</span></span>

</dd> <dt>

<span data-ttu-id="280c5-153">**ParentInstanceId**</span><span class="sxs-lookup"><span data-stu-id="280c5-153">**ParentInstanceId**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="280c5-154">資料類型： **uint32**</span><span class="sxs-lookup"><span data-stu-id="280c5-154">Data type: **uint32**</span></span>
</dt> <dt>

<span data-ttu-id="280c5-155">存取類型：唯讀</span><span class="sxs-lookup"><span data-stu-id="280c5-155">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="280c5-156">限定詞： **WmiDataId** (13) </span><span class="sxs-lookup"><span data-stu-id="280c5-156">Qualifiers: **WmiDataId** (13)</span></span>
</dt> </dl>

<span data-ttu-id="280c5-157">父實例資料的識別碼。</span><span class="sxs-lookup"><span data-stu-id="280c5-157">Identifier of the parent instance data.</span></span>

</dd> <dt>

<span data-ttu-id="280c5-158">**ReservedHeaderField**</span><span class="sxs-lookup"><span data-stu-id="280c5-158">**ReservedHeaderField**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="280c5-159">資料類型： **uint16**</span><span class="sxs-lookup"><span data-stu-id="280c5-159">Data type: **uint16**</span></span>
</dt> <dt>

<span data-ttu-id="280c5-160">存取類型：唯讀</span><span class="sxs-lookup"><span data-stu-id="280c5-160">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="280c5-161">限定詞： **WmiDataId** (2) </span><span class="sxs-lookup"><span data-stu-id="280c5-161">Qualifiers: **WmiDataId** (2)</span></span>
</dt> </dl>

<span data-ttu-id="280c5-162">保留的。</span><span class="sxs-lookup"><span data-stu-id="280c5-162">Reserved.</span></span>

</dd> <dt>

<span data-ttu-id="280c5-163">**ThreadId**</span><span class="sxs-lookup"><span data-stu-id="280c5-163">**ThreadId**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="280c5-164">資料類型： **uint64**</span><span class="sxs-lookup"><span data-stu-id="280c5-164">Data type: **uint64**</span></span>
</dt> <dt>

<span data-ttu-id="280c5-165">存取類型：唯讀</span><span class="sxs-lookup"><span data-stu-id="280c5-165">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="280c5-166">限定詞： **WmiDataId** (6) ， **指標**</span><span class="sxs-lookup"><span data-stu-id="280c5-166">Qualifiers: **WmiDataId** (6), **Pointer**</span></span>
</dt> </dl>

<span data-ttu-id="280c5-167">識別已產生事件的執行緒。</span><span class="sxs-lookup"><span data-stu-id="280c5-167">Identifies the thread that generated the event.</span></span>

</dd> <dt>

<span data-ttu-id="280c5-168">**時間 戳**</span><span class="sxs-lookup"><span data-stu-id="280c5-168">**TimeStamp**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="280c5-169">資料類型： **uint64**</span><span class="sxs-lookup"><span data-stu-id="280c5-169">Data type: **uint64**</span></span>
</dt> <dt>

<span data-ttu-id="280c5-170">存取類型：唯讀</span><span class="sxs-lookup"><span data-stu-id="280c5-170">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="280c5-171">限定詞： **WmiDataId** (7) </span><span class="sxs-lookup"><span data-stu-id="280c5-171">Qualifiers: **WmiDataId** (7)</span></span>
</dt> </dl>

<span data-ttu-id="280c5-172">包含發生事件的日期和時間。</span><span class="sxs-lookup"><span data-stu-id="280c5-172">Contains the date and time when the event occurred.</span></span>

</dd> <dt>

<span data-ttu-id="280c5-173">**TraceLevel**</span><span class="sxs-lookup"><span data-stu-id="280c5-173">**TraceLevel**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="280c5-174">資料類型： **uint8**</span><span class="sxs-lookup"><span data-stu-id="280c5-174">Data type: **uint8**</span></span>
</dt> <dt>

<span data-ttu-id="280c5-175">存取類型：唯讀</span><span class="sxs-lookup"><span data-stu-id="280c5-175">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="280c5-176">限定詞： **WmiDataId** (4) </span><span class="sxs-lookup"><span data-stu-id="280c5-176">Qualifiers: **WmiDataId** (4)</span></span>
</dt> </dl>

<span data-ttu-id="280c5-177">提供者定義的值，定義用來產生事件的嚴重性層級。</span><span class="sxs-lookup"><span data-stu-id="280c5-177">Provider-defined value that defines the severity level used to generate the event.</span></span>

</dd> <dt>

<span data-ttu-id="280c5-178">**TraceVersion**</span><span class="sxs-lookup"><span data-stu-id="280c5-178">**TraceVersion**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="280c5-179">資料類型： **uint16**</span><span class="sxs-lookup"><span data-stu-id="280c5-179">Data type: **uint16**</span></span>
</dt> <dt>

<span data-ttu-id="280c5-180">存取類型：唯讀</span><span class="sxs-lookup"><span data-stu-id="280c5-180">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="280c5-181">限定詞： **WmiDataId** (5) </span><span class="sxs-lookup"><span data-stu-id="280c5-181">Qualifiers: **WmiDataId** (5)</span></span>
</dt> </dl>

<span data-ttu-id="280c5-182">用來產生事件之事件追蹤類別的提供者定義版本號碼。</span><span class="sxs-lookup"><span data-stu-id="280c5-182">Provider-defined version number of the event trace class used to generate the event.</span></span>

</dd> <dt>

<span data-ttu-id="280c5-183">**UserTime**</span><span class="sxs-lookup"><span data-stu-id="280c5-183">**UserTime**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="280c5-184">資料類型： **uint32**</span><span class="sxs-lookup"><span data-stu-id="280c5-184">Data type: **uint32**</span></span>
</dt> <dt>

<span data-ttu-id="280c5-185">存取類型：唯讀</span><span class="sxs-lookup"><span data-stu-id="280c5-185">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="280c5-186">限定詞： **WmiDataId** (10) </span><span class="sxs-lookup"><span data-stu-id="280c5-186">Qualifiers: **WmiDataId** (10)</span></span>
</dt> </dl>

<span data-ttu-id="280c5-187">使用者模式指示的經過執行時間，以 CPU 滴答為單位。</span><span class="sxs-lookup"><span data-stu-id="280c5-187">Elapsed execution time for user-mode instructions, in CPU ticks.</span></span>

</dd> </dl>

## <a name="remarks"></a><span data-ttu-id="280c5-188">備註</span><span class="sxs-lookup"><span data-stu-id="280c5-188">Remarks</span></span>

<span data-ttu-id="280c5-189">請勿使用這些屬性。</span><span class="sxs-lookup"><span data-stu-id="280c5-189">Do not use these properties.</span></span>

## <a name="requirements"></a><span data-ttu-id="280c5-190">規格需求</span><span class="sxs-lookup"><span data-stu-id="280c5-190">Requirements</span></span>



| <span data-ttu-id="280c5-191">需求</span><span class="sxs-lookup"><span data-stu-id="280c5-191">Requirement</span></span> | <span data-ttu-id="280c5-192">值</span><span class="sxs-lookup"><span data-stu-id="280c5-192">Value</span></span> |
|-------------------------------------|------------------------------------------------------------------------------------|
| <span data-ttu-id="280c5-193">最低支援的用戶端</span><span class="sxs-lookup"><span data-stu-id="280c5-193">Minimum supported client</span></span><br/> | <span data-ttu-id="280c5-194">Windows 2000 Professional \[僅限傳統型應用程式\]</span><span class="sxs-lookup"><span data-stu-id="280c5-194">Windows 2000 Professional \[desktop apps only\]</span></span><br/>                         |
| <span data-ttu-id="280c5-195">最低支援的伺服器</span><span class="sxs-lookup"><span data-stu-id="280c5-195">Minimum supported server</span></span><br/> | <span data-ttu-id="280c5-196">Windows 2000 Server \[僅限傳統型應用程式\]</span><span class="sxs-lookup"><span data-stu-id="280c5-196">Windows 2000 Server \[desktop apps only\]</span></span><br/>                               |
| <span data-ttu-id="280c5-197">MOF</span><span class="sxs-lookup"><span data-stu-id="280c5-197">MOF</span></span><br/>                      | <dl> <span data-ttu-id="280c5-198"><dt>Wmi. mof</dt></span><span class="sxs-lookup"><span data-stu-id="280c5-198"><dt>Wmi.mof</dt></span></span> </dl> |



 

 




