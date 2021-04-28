---
description: Process_V2_TypeGroup1 類別-這個類別是處理事件的事件種類類別。 以下是從 MOF 程式碼簡化的語法。
ms.assetid: ff5c1f64-2087-4238-81f9-6283f0f0e68a
title: Process_V2_TypeGroup1 類別
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Process_V2_TypeGroup1
- Process_V2_TypeGroup1.UniqueProcessKey
- Process_V2_TypeGroup1.ProcessId
- Process_V2_TypeGroup1.ParentId
- Process_V2_TypeGroup1.SessionId
- Process_V2_TypeGroup1.ExitStatus
- Process_V2_TypeGroup1.UserSID
- Process_V2_TypeGroup1.ImageFileName
- Process_V2_TypeGroup1.CommandLine
api_type:
- NA
api_location: ''
ms.openlocfilehash: b587a07f33b066cfd7dbeebc44d7277b33c6bee8
ms.sourcegitcommit: 95685061d5b0333bbf9e6ebd208dde8190f97005
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 04/28/2021
ms.locfileid: "108106306"
---
# <a name="process_v2_typegroup1-class"></a><span data-ttu-id="e12b6-104">進程 \_ V2 \_ TypeGroup1 類別</span><span class="sxs-lookup"><span data-stu-id="e12b6-104">Process\_V2\_TypeGroup1 class</span></span>

<span data-ttu-id="e12b6-105">這個類別是處理事件的事件種類類別。</span><span class="sxs-lookup"><span data-stu-id="e12b6-105">This class is the event type class for process events.</span></span>

<span data-ttu-id="e12b6-106">以下是從 MOF 程式碼簡化的語法。</span><span class="sxs-lookup"><span data-stu-id="e12b6-106">The following syntax is simplified from MOF code.</span></span>

## <a name="syntax"></a><span data-ttu-id="e12b6-107">語法</span><span class="sxs-lookup"><span data-stu-id="e12b6-107">Syntax</span></span>

``` syntax
[EventType{1, 2, 3, 4, 39}, EventTypeName{"Start", "End", "DCStart", "DCEnd", "Defunct"}]
class Process_V2_TypeGroup1 : Process_V2
{
  uint32 UniqueProcessKey;
  uint32 ProcessId;
  uint32 ParentId;
  uint32 SessionId;
  sint32 ExitStatus;
  object UserSID;
  string ImageFileName;
  string CommandLine;
};
```

## <a name="members"></a><span data-ttu-id="e12b6-108">成員</span><span class="sxs-lookup"><span data-stu-id="e12b6-108">Members</span></span>

<span data-ttu-id="e12b6-109">**Process \_ V2 \_ TypeGroup1** 類別具有下列類型的成員：</span><span class="sxs-lookup"><span data-stu-id="e12b6-109">The **Process\_V2\_TypeGroup1** class has these types of members:</span></span>

-   [<span data-ttu-id="e12b6-110">屬性</span><span class="sxs-lookup"><span data-stu-id="e12b6-110">Properties</span></span>](#properties)

### <a name="properties"></a><span data-ttu-id="e12b6-111">屬性</span><span class="sxs-lookup"><span data-stu-id="e12b6-111">Properties</span></span>

<span data-ttu-id="e12b6-112">**Process \_ V2 \_ TypeGroup1** 類別具有這些屬性。</span><span class="sxs-lookup"><span data-stu-id="e12b6-112">The **Process\_V2\_TypeGroup1** class has these properties.</span></span>

<dl> <dt>

<span data-ttu-id="e12b6-113">CommandLine</span><span class="sxs-lookup"><span data-stu-id="e12b6-113">CommandLine</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="e12b6-114">資料類型： **字串**</span><span class="sxs-lookup"><span data-stu-id="e12b6-114">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="e12b6-115">存取類型：唯讀</span><span class="sxs-lookup"><span data-stu-id="e12b6-115">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="e12b6-116">限定詞： WmiDataId (8) 、StringTermination ( "NullTerminated" ) 、Format ( "w" ) </span><span class="sxs-lookup"><span data-stu-id="e12b6-116">Qualifiers: WmiDataId(8), StringTermination("NullTerminated"), Format("w")</span></span>
</dt> </dl>

<span data-ttu-id="e12b6-117">進程的完整命令列。</span><span class="sxs-lookup"><span data-stu-id="e12b6-117">Full command line of the process.</span></span>

</dd> <dt>

<span data-ttu-id="e12b6-118">ExitStatus</span><span class="sxs-lookup"><span data-stu-id="e12b6-118">ExitStatus</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="e12b6-119">資料類型： **sint32**</span><span class="sxs-lookup"><span data-stu-id="e12b6-119">Data type: **sint32**</span></span>
</dt> <dt>

<span data-ttu-id="e12b6-120">存取類型：唯讀</span><span class="sxs-lookup"><span data-stu-id="e12b6-120">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="e12b6-121">限定詞： WmiDataId (5) </span><span class="sxs-lookup"><span data-stu-id="e12b6-121">Qualifiers: WmiDataId(5)</span></span>
</dt> </dl>

<span data-ttu-id="e12b6-122">已停止進程的結束狀態。</span><span class="sxs-lookup"><span data-stu-id="e12b6-122">Exit status of the stopped process.</span></span>

</dd> <dt>

<span data-ttu-id="e12b6-123">ImageFileName</span><span class="sxs-lookup"><span data-stu-id="e12b6-123">ImageFileName</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="e12b6-124">資料類型： **字串**</span><span class="sxs-lookup"><span data-stu-id="e12b6-124">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="e12b6-125">存取類型：唯讀</span><span class="sxs-lookup"><span data-stu-id="e12b6-125">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="e12b6-126">限定詞： WmiDataId (7) ，StringTermination ( "NullTerminated" ) </span><span class="sxs-lookup"><span data-stu-id="e12b6-126">Qualifiers: WmiDataId(7), StringTermination("NullTerminated")</span></span>
</dt> </dl>

<span data-ttu-id="e12b6-127">進程可執行檔的路徑。</span><span class="sxs-lookup"><span data-stu-id="e12b6-127">Path to the executable file of the process.</span></span>

</dd> <dt>

<span data-ttu-id="e12b6-128">ParentId</span><span class="sxs-lookup"><span data-stu-id="e12b6-128">ParentId</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="e12b6-129">資料類型： **uint32**</span><span class="sxs-lookup"><span data-stu-id="e12b6-129">Data type: **uint32**</span></span>
</dt> <dt>

<span data-ttu-id="e12b6-130">存取類型：唯讀</span><span class="sxs-lookup"><span data-stu-id="e12b6-130">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="e12b6-131">限定詞： WmiDataId (3) ，格式 ( "x" ) </span><span class="sxs-lookup"><span data-stu-id="e12b6-131">Qualifiers: WmiDataId(3), Format("x")</span></span>
</dt> </dl>

<span data-ttu-id="e12b6-132">建立此進程之進程的唯一識別碼。</span><span class="sxs-lookup"><span data-stu-id="e12b6-132">Unique identifier of the process that creates this process.</span></span> <span data-ttu-id="e12b6-133">系統會重複使用處理序識別碼，因此它們只會在該進程的存留期內找出處理常式。</span><span class="sxs-lookup"><span data-stu-id="e12b6-133">Process identifier numbers are reused, so they only identify a process for the lifetime of that process.</span></span> <span data-ttu-id="e12b6-134">ParentProcessId 所識別的進程可能會終止，因此 ParentProcessId 可能不會參考執行中的進程。</span><span class="sxs-lookup"><span data-stu-id="e12b6-134">It is possible that the process identified by ParentProcessId is terminated, so ParentProcessId may not refer to a running process.</span></span> <span data-ttu-id="e12b6-135">ParentProcessId 也可能不正確地參考重複使用處理序識別碼的進程。</span><span class="sxs-lookup"><span data-stu-id="e12b6-135">It is also possible that ParentProcessId incorrectly refers to a process that reuses a process identifier.</span></span>

</dd> <dt>

<span data-ttu-id="e12b6-136">ProcessId</span><span class="sxs-lookup"><span data-stu-id="e12b6-136">ProcessId</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="e12b6-137">資料類型： **uint32**</span><span class="sxs-lookup"><span data-stu-id="e12b6-137">Data type: **uint32**</span></span>
</dt> <dt>

<span data-ttu-id="e12b6-138">存取類型：唯讀</span><span class="sxs-lookup"><span data-stu-id="e12b6-138">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="e12b6-139">限定詞： WmiDataId (2) ，格式 ( "x" ) </span><span class="sxs-lookup"><span data-stu-id="e12b6-139">Qualifiers: WmiDataId(2), Format("x")</span></span>
</dt> </dl>

<span data-ttu-id="e12b6-140">您可以用來識別進程的全域處理序識別碼。</span><span class="sxs-lookup"><span data-stu-id="e12b6-140">Global process identifier that you can use to identify a process.</span></span> <span data-ttu-id="e12b6-141">此值從建立進程到終止之前都有效。</span><span class="sxs-lookup"><span data-stu-id="e12b6-141">The value is valid from the time a process is created until it is terminated.</span></span>

</dd> <dt>

<span data-ttu-id="e12b6-142">SessionId</span><span class="sxs-lookup"><span data-stu-id="e12b6-142">SessionId</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="e12b6-143">資料類型： **uint32**</span><span class="sxs-lookup"><span data-stu-id="e12b6-143">Data type: **uint32**</span></span>
</dt> <dt>

<span data-ttu-id="e12b6-144">存取類型：唯讀</span><span class="sxs-lookup"><span data-stu-id="e12b6-144">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="e12b6-145">限定詞： WmiDataId (4) </span><span class="sxs-lookup"><span data-stu-id="e12b6-145">Qualifiers: WmiDataId(4)</span></span>
</dt> </dl>

<span data-ttu-id="e12b6-146">作業系統在建立新的會話時所產生的唯一識別碼。</span><span class="sxs-lookup"><span data-stu-id="e12b6-146">Unique identifier that an operating system generates when it creates a new session.</span></span> <span data-ttu-id="e12b6-147">會話從登入到從特定系統登出的一段時間。</span><span class="sxs-lookup"><span data-stu-id="e12b6-147">A session spans a period of time from log on until log off from a specific system.</span></span>

</dd> <dt>

<span data-ttu-id="e12b6-148">UniqueProcessKey</span><span class="sxs-lookup"><span data-stu-id="e12b6-148">UniqueProcessKey</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="e12b6-149">資料類型： **uint32**</span><span class="sxs-lookup"><span data-stu-id="e12b6-149">Data type: **uint32**</span></span>
</dt> <dt>

<span data-ttu-id="e12b6-150">存取類型：唯讀</span><span class="sxs-lookup"><span data-stu-id="e12b6-150">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="e12b6-151">限定詞： WmiDataId (1) ，指標</span><span class="sxs-lookup"><span data-stu-id="e12b6-151">Qualifiers: WmiDataId(1), Pointer</span></span>
</dt> </dl>

<span data-ttu-id="e12b6-152">核心中處理常式物件的位址。</span><span class="sxs-lookup"><span data-stu-id="e12b6-152">The address of the process object in the kernel.</span></span>

</dd> <dt>

<span data-ttu-id="e12b6-153">UserSID</span><span class="sxs-lookup"><span data-stu-id="e12b6-153">UserSID</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="e12b6-154">資料類型： **物件**</span><span class="sxs-lookup"><span data-stu-id="e12b6-154">Data type: **object**</span></span>
</dt> <dt>

<span data-ttu-id="e12b6-155">存取類型：唯讀</span><span class="sxs-lookup"><span data-stu-id="e12b6-155">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="e12b6-156">限定詞： WmiDataId (6) ，副檔名 ( "Sid" ) </span><span class="sxs-lookup"><span data-stu-id="e12b6-156">Qualifiers: WmiDataId(6), Extension("Sid")</span></span>
</dt> </dl>

<span data-ttu-id="e12b6-157">安全性識別元 (SID) 用於事件發生所在的使用者內容。</span><span class="sxs-lookup"><span data-stu-id="e12b6-157">Security identifier (SID) for the user context under which the event happens.</span></span>

</dd> </dl>

## <a name="remarks"></a><span data-ttu-id="e12b6-158">備註</span><span class="sxs-lookup"><span data-stu-id="e12b6-158">Remarks</span></span>

<span data-ttu-id="e12b6-159">DCStart 和 DCEnd 事件種類會列舉目前正在執行的進程，包括每次核心會話開始和結束時的閒置和系統進程。</span><span class="sxs-lookup"><span data-stu-id="e12b6-159">The DCStart and DCEnd event types enumerate the process that are currently running, including idle and system process, at the time the kernel session starts and ends, respectively.</span></span>

## <a name="requirements"></a><span data-ttu-id="e12b6-160">規格需求</span><span class="sxs-lookup"><span data-stu-id="e12b6-160">Requirements</span></span>



| <span data-ttu-id="e12b6-161">需求</span><span class="sxs-lookup"><span data-stu-id="e12b6-161">Requirement</span></span> | <span data-ttu-id="e12b6-162">值</span><span class="sxs-lookup"><span data-stu-id="e12b6-162">Value</span></span> |
|-------------------------------------|------------------------------------------------------------|
| <span data-ttu-id="e12b6-163">最低支援的用戶端</span><span class="sxs-lookup"><span data-stu-id="e12b6-163">Minimum supported client</span></span><br/> | <span data-ttu-id="e12b6-164">Windows 2000 Professional \[僅限傳統型應用程式\]</span><span class="sxs-lookup"><span data-stu-id="e12b6-164">Windows 2000 Professional \[desktop apps only\]</span></span><br/> |
| <span data-ttu-id="e12b6-165">最低支援的伺服器</span><span class="sxs-lookup"><span data-stu-id="e12b6-165">Minimum supported server</span></span><br/> | <span data-ttu-id="e12b6-166">Windows 2000 Server \[僅限傳統型應用程式\]</span><span class="sxs-lookup"><span data-stu-id="e12b6-166">Windows 2000 Server \[desktop apps only\]</span></span><br/>       |



## <a name="see-also"></a><span data-ttu-id="e12b6-167">另請參閱</span><span class="sxs-lookup"><span data-stu-id="e12b6-167">See also</span></span>

<dl> <dt>

[<span data-ttu-id="e12b6-168">**進程 \_ V2**</span><span class="sxs-lookup"><span data-stu-id="e12b6-168">**Process\_V2**</span></span>](process-v2.md)
</dt> </dl>

 

 




