---
description: Process_TypeGroup1 類別-這個類別是處理事件的事件種類類別。 以下是從 MOF 程式碼簡化的語法。
ms.assetid: 4f06e1af-3f9a-4346-aa50-50f3ee82cd98
title: Process_TypeGroup1 類別
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Process_TypeGroup1
- Process_TypeGroup1.UniqueProcessKey
- Process_TypeGroup1.ProcessId
- Process_TypeGroup1.ParentId
- Process_TypeGroup1.SessionId
- Process_TypeGroup1.ExitStatus
- Process_TypeGroup1.DirectoryTableBase
- Process_TypeGroup1.UserSID
- Process_TypeGroup1.ImageFileName
- Process_TypeGroup1.CommandLine
api_type:
- NA
api_location: ''
ms.openlocfilehash: bd67059f5257dad9b66e1c21f642fef04f03719e
ms.sourcegitcommit: 95685061d5b0333bbf9e6ebd208dde8190f97005
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 04/28/2021
ms.locfileid: "108106376"
---
# <a name="process_typegroup1-class"></a><span data-ttu-id="db892-104">進程 \_ TypeGroup1 類別</span><span class="sxs-lookup"><span data-stu-id="db892-104">Process\_TypeGroup1 class</span></span>

<span data-ttu-id="db892-105">這個類別是處理事件的事件種類類別。</span><span class="sxs-lookup"><span data-stu-id="db892-105">This class is the event type class for process events.</span></span>

<span data-ttu-id="db892-106">以下是從 MOF 程式碼簡化的語法。</span><span class="sxs-lookup"><span data-stu-id="db892-106">The following syntax is simplified from MOF code.</span></span>

## <a name="syntax"></a><span data-ttu-id="db892-107">語法</span><span class="sxs-lookup"><span data-stu-id="db892-107">Syntax</span></span>

``` syntax
[EventType{1, 2, 3, 4, 39}, EventTypeName{"Start", "End", "DCStart", "DCEnd", "Defunct"}]
class Process_TypeGroup1 : Process
{
  uint32 UniqueProcessKey;
  uint32 ProcessId;
  uint32 ParentId;
  uint32 SessionId;
  sint32 ExitStatus;
  uint32 DirectoryTableBase;
  object UserSID;
  string ImageFileName;
  string CommandLine;
};
```

## <a name="members"></a><span data-ttu-id="db892-108">成員</span><span class="sxs-lookup"><span data-stu-id="db892-108">Members</span></span>

<span data-ttu-id="db892-109">**Process \_ TypeGroup1** 類別具有下列類型的成員：</span><span class="sxs-lookup"><span data-stu-id="db892-109">The **Process\_TypeGroup1** class has these types of members:</span></span>

-   [<span data-ttu-id="db892-110">屬性</span><span class="sxs-lookup"><span data-stu-id="db892-110">Properties</span></span>](#properties)

### <a name="properties"></a><span data-ttu-id="db892-111">屬性</span><span class="sxs-lookup"><span data-stu-id="db892-111">Properties</span></span>

<span data-ttu-id="db892-112">**Process \_ TypeGroup1** 類別具有這些屬性。</span><span class="sxs-lookup"><span data-stu-id="db892-112">The **Process\_TypeGroup1** class has these properties.</span></span>

<dl> <dt>

<span data-ttu-id="db892-113">CommandLine</span><span class="sxs-lookup"><span data-stu-id="db892-113">CommandLine</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="db892-114">資料類型： **字串**</span><span class="sxs-lookup"><span data-stu-id="db892-114">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="db892-115">存取類型：唯讀</span><span class="sxs-lookup"><span data-stu-id="db892-115">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="db892-116">限定詞： WmiDataId (9) 、StringTermination ( "NullTerminated" ) 、Format ( "w" ) </span><span class="sxs-lookup"><span data-stu-id="db892-116">Qualifiers: WmiDataId(9), StringTermination("NullTerminated"), Format("w")</span></span>
</dt> </dl>

<span data-ttu-id="db892-117">進程的完整命令列。</span><span class="sxs-lookup"><span data-stu-id="db892-117">Full command line of the process.</span></span>

</dd> <dt>

<span data-ttu-id="db892-118">DirectoryTableBase</span><span class="sxs-lookup"><span data-stu-id="db892-118">DirectoryTableBase</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="db892-119">資料類型： **uint32**</span><span class="sxs-lookup"><span data-stu-id="db892-119">Data type: **uint32**</span></span>
</dt> <dt>

<span data-ttu-id="db892-120">存取類型：唯讀</span><span class="sxs-lookup"><span data-stu-id="db892-120">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="db892-121">限定詞： WmiDataId (6) ，指標</span><span class="sxs-lookup"><span data-stu-id="db892-121">Qualifiers: WmiDataId(6), Pointer</span></span>
</dt> </dl>

<span data-ttu-id="db892-122">進程之頁面資料表的實體位址。</span><span class="sxs-lookup"><span data-stu-id="db892-122">The physical address of the page table of the process.</span></span>

</dd> <dt>

<span data-ttu-id="db892-123">ExitStatus</span><span class="sxs-lookup"><span data-stu-id="db892-123">ExitStatus</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="db892-124">資料類型： **sint32**</span><span class="sxs-lookup"><span data-stu-id="db892-124">Data type: **sint32**</span></span>
</dt> <dt>

<span data-ttu-id="db892-125">存取類型：唯讀</span><span class="sxs-lookup"><span data-stu-id="db892-125">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="db892-126">限定詞： WmiDataId (5) </span><span class="sxs-lookup"><span data-stu-id="db892-126">Qualifiers: WmiDataId(5)</span></span>
</dt> </dl>

<span data-ttu-id="db892-127">已停止進程的結束狀態。</span><span class="sxs-lookup"><span data-stu-id="db892-127">Exit status of the stopped process.</span></span>

</dd> <dt>

<span data-ttu-id="db892-128">ImageFileName</span><span class="sxs-lookup"><span data-stu-id="db892-128">ImageFileName</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="db892-129">資料類型： **字串**</span><span class="sxs-lookup"><span data-stu-id="db892-129">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="db892-130">存取類型：唯讀</span><span class="sxs-lookup"><span data-stu-id="db892-130">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="db892-131">限定詞： WmiDataId (8) ，StringTermination ( "NullTerminated" ) </span><span class="sxs-lookup"><span data-stu-id="db892-131">Qualifiers: WmiDataId(8), StringTermination("NullTerminated")</span></span>
</dt> </dl>

<span data-ttu-id="db892-132">進程可執行檔的路徑。</span><span class="sxs-lookup"><span data-stu-id="db892-132">Path to the executable file of the process.</span></span>

</dd> <dt>

<span data-ttu-id="db892-133">ParentId</span><span class="sxs-lookup"><span data-stu-id="db892-133">ParentId</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="db892-134">資料類型： **uint32**</span><span class="sxs-lookup"><span data-stu-id="db892-134">Data type: **uint32**</span></span>
</dt> <dt>

<span data-ttu-id="db892-135">存取類型：唯讀</span><span class="sxs-lookup"><span data-stu-id="db892-135">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="db892-136">限定詞： WmiDataId (3) ，格式 ( "x" ) </span><span class="sxs-lookup"><span data-stu-id="db892-136">Qualifiers: WmiDataId(3), Format("x")</span></span>
</dt> </dl>

<span data-ttu-id="db892-137">建立此進程之進程的唯一識別碼。</span><span class="sxs-lookup"><span data-stu-id="db892-137">Unique identifier of the process that creates this process.</span></span> <span data-ttu-id="db892-138">系統會重複使用處理序識別碼，因此它們只會在該進程的存留期內找出處理常式。</span><span class="sxs-lookup"><span data-stu-id="db892-138">Process identifier numbers are reused, so they only identify a process for the lifetime of that process.</span></span> <span data-ttu-id="db892-139">ParentProcessId 所識別的進程可能會終止，因此 ParentProcessId 可能不會參考執行中的進程。</span><span class="sxs-lookup"><span data-stu-id="db892-139">It is possible that the process identified by ParentProcessId is terminated, so ParentProcessId may not refer to a running process.</span></span> <span data-ttu-id="db892-140">ParentProcessId 也可能不正確地參考重複使用處理序識別碼的進程。</span><span class="sxs-lookup"><span data-stu-id="db892-140">It is also possible that ParentProcessId incorrectly refers to a process that reuses a process identifier.</span></span>

</dd> <dt>

<span data-ttu-id="db892-141">ProcessId</span><span class="sxs-lookup"><span data-stu-id="db892-141">ProcessId</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="db892-142">資料類型： **uint32**</span><span class="sxs-lookup"><span data-stu-id="db892-142">Data type: **uint32**</span></span>
</dt> <dt>

<span data-ttu-id="db892-143">存取類型：唯讀</span><span class="sxs-lookup"><span data-stu-id="db892-143">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="db892-144">限定詞： WmiDataId (2) ，格式 ( "x" ) </span><span class="sxs-lookup"><span data-stu-id="db892-144">Qualifiers: WmiDataId(2), Format("x")</span></span>
</dt> </dl>

<span data-ttu-id="db892-145">您可以用來識別進程的全域處理序識別碼。</span><span class="sxs-lookup"><span data-stu-id="db892-145">Global process identifier that you can use to identify a process.</span></span> <span data-ttu-id="db892-146">此值從建立進程到終止之前都有效。</span><span class="sxs-lookup"><span data-stu-id="db892-146">The value is valid from the time a process is created until it is terminated.</span></span>

</dd> <dt>

<span data-ttu-id="db892-147">SessionId</span><span class="sxs-lookup"><span data-stu-id="db892-147">SessionId</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="db892-148">資料類型： **uint32**</span><span class="sxs-lookup"><span data-stu-id="db892-148">Data type: **uint32**</span></span>
</dt> <dt>

<span data-ttu-id="db892-149">存取類型：唯讀</span><span class="sxs-lookup"><span data-stu-id="db892-149">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="db892-150">限定詞： WmiDataId (4) </span><span class="sxs-lookup"><span data-stu-id="db892-150">Qualifiers: WmiDataId(4)</span></span>
</dt> </dl>

<span data-ttu-id="db892-151">作業系統在建立新的會話時所產生的唯一識別碼。</span><span class="sxs-lookup"><span data-stu-id="db892-151">Unique identifier that an operating system generates when it creates a new session.</span></span> <span data-ttu-id="db892-152">會話從登入到從特定系統登出的一段時間。</span><span class="sxs-lookup"><span data-stu-id="db892-152">A session spans a period of time from log on until log off from a specific system.</span></span>

</dd> <dt>

<span data-ttu-id="db892-153">UniqueProcessKey</span><span class="sxs-lookup"><span data-stu-id="db892-153">UniqueProcessKey</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="db892-154">資料類型： **uint32**</span><span class="sxs-lookup"><span data-stu-id="db892-154">Data type: **uint32**</span></span>
</dt> <dt>

<span data-ttu-id="db892-155">存取類型：唯讀</span><span class="sxs-lookup"><span data-stu-id="db892-155">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="db892-156">限定詞： WmiDataId (1) ，指標</span><span class="sxs-lookup"><span data-stu-id="db892-156">Qualifiers: WmiDataId(1), Pointer</span></span>
</dt> </dl>

<span data-ttu-id="db892-157">核心中處理常式物件的位址。</span><span class="sxs-lookup"><span data-stu-id="db892-157">The address of the process object in the kernel.</span></span>

</dd> <dt>

<span data-ttu-id="db892-158">UserSID</span><span class="sxs-lookup"><span data-stu-id="db892-158">UserSID</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="db892-159">資料類型： **物件**</span><span class="sxs-lookup"><span data-stu-id="db892-159">Data type: **object**</span></span>
</dt> <dt>

<span data-ttu-id="db892-160">存取類型：唯讀</span><span class="sxs-lookup"><span data-stu-id="db892-160">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="db892-161">限定詞： WmiDataId (7) ，副檔名 ( "Sid" ) </span><span class="sxs-lookup"><span data-stu-id="db892-161">Qualifiers: WmiDataId(7), Extension("Sid")</span></span>
</dt> </dl>

<span data-ttu-id="db892-162">安全性識別元 (SID) 用於事件發生所在的使用者內容。</span><span class="sxs-lookup"><span data-stu-id="db892-162">Security identifier (SID) for the user context under which the event happens.</span></span>

</dd> </dl>

## <a name="remarks"></a><span data-ttu-id="db892-163">備註</span><span class="sxs-lookup"><span data-stu-id="db892-163">Remarks</span></span>

<span data-ttu-id="db892-164">DCStart 和 DCEnd 事件種類會列舉目前正在執行的進程，包括每次核心會話開始和結束時的閒置和系統進程。</span><span class="sxs-lookup"><span data-stu-id="db892-164">The DCStart and DCEnd event types enumerate the process that are currently running, including idle and system process, at the time the kernel session starts and ends, respectively.</span></span>

## <a name="requirements"></a><span data-ttu-id="db892-165">規格需求</span><span class="sxs-lookup"><span data-stu-id="db892-165">Requirements</span></span>



| <span data-ttu-id="db892-166">需求</span><span class="sxs-lookup"><span data-stu-id="db892-166">Requirement</span></span> | <span data-ttu-id="db892-167">值</span><span class="sxs-lookup"><span data-stu-id="db892-167">Value</span></span> |
|-------------------------------------|------------------------------------------------------------|
| <span data-ttu-id="db892-168">最低支援的用戶端</span><span class="sxs-lookup"><span data-stu-id="db892-168">Minimum supported client</span></span><br/> | <span data-ttu-id="db892-169">Windows 2000 Professional \[僅限傳統型應用程式\]</span><span class="sxs-lookup"><span data-stu-id="db892-169">Windows 2000 Professional \[desktop apps only\]</span></span><br/> |
| <span data-ttu-id="db892-170">最低支援的伺服器</span><span class="sxs-lookup"><span data-stu-id="db892-170">Minimum supported server</span></span><br/> | <span data-ttu-id="db892-171">Windows 2000 Server \[僅限傳統型應用程式\]</span><span class="sxs-lookup"><span data-stu-id="db892-171">Windows 2000 Server \[desktop apps only\]</span></span><br/>       |



## <a name="see-also"></a><span data-ttu-id="db892-172">另請參閱</span><span class="sxs-lookup"><span data-stu-id="db892-172">See also</span></span>

<dl> <dt>

[<span data-ttu-id="db892-173">**處理序**</span><span class="sxs-lookup"><span data-stu-id="db892-173">**Process**</span></span>](process.md)
</dt> </dl>

 

 




