---
description: 這個類別是處理事件的事件種類類別。 以下是從 MOF 程式碼簡化的語法。
ms.assetid: b114d7fd-c308-4f21-8f1a-ab27dc93abc5
title: Process_V1_TypeGroup1 類別
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Process_V1_TypeGroup1
- Process_V1_TypeGroup1.PageDirectoryBase
- Process_V1_TypeGroup1.ProcessId
- Process_V1_TypeGroup1.ParentId
- Process_V1_TypeGroup1.SessionId
- Process_V1_TypeGroup1.ExitStatus
- Process_V1_TypeGroup1.UserSID
- Process_V1_TypeGroup1.ImageFileName
api_type:
- NA
api_location: ''
ms.openlocfilehash: fc2308965de5c06a25858a138d4536763613a4d0
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/08/2021
ms.locfileid: "104320112"
---
# <a name="process_v1_typegroup1-class"></a><span data-ttu-id="a07c5-104">Process \_ V1 \_ TypeGroup1 類別</span><span class="sxs-lookup"><span data-stu-id="a07c5-104">Process\_V1\_TypeGroup1 class</span></span>

<span data-ttu-id="a07c5-105">這個類別是處理事件的事件種類類別。</span><span class="sxs-lookup"><span data-stu-id="a07c5-105">This class is the event type class for process events.</span></span>

<span data-ttu-id="a07c5-106">以下是從 MOF 程式碼簡化的語法。</span><span class="sxs-lookup"><span data-stu-id="a07c5-106">The following syntax is simplified from MOF code.</span></span>

## <a name="syntax"></a><span data-ttu-id="a07c5-107">語法</span><span class="sxs-lookup"><span data-stu-id="a07c5-107">Syntax</span></span>

``` syntax
[EventType{1, 2, 3, 4}, EventTypeName{"Start", "End", "DCStart", "DCEnd"}]
class Process_V1_TypeGroup1 : Process_V1
{
  uint32 PageDirectoryBase;
  uint32 ProcessId;
  uint32 ParentId;
  uint32 SessionId;
  sint32 ExitStatus;
  object UserSID;
  string ImageFileName;
};
```

## <a name="members"></a><span data-ttu-id="a07c5-108">成員</span><span class="sxs-lookup"><span data-stu-id="a07c5-108">Members</span></span>

<span data-ttu-id="a07c5-109">**Process \_ V1 \_ TypeGroup1** 類別具有下列類型的成員：</span><span class="sxs-lookup"><span data-stu-id="a07c5-109">The **Process\_V1\_TypeGroup1** class has these types of members:</span></span>

-   [<span data-ttu-id="a07c5-110">屬性</span><span class="sxs-lookup"><span data-stu-id="a07c5-110">Properties</span></span>](#properties)

### <a name="properties"></a><span data-ttu-id="a07c5-111">屬性</span><span class="sxs-lookup"><span data-stu-id="a07c5-111">Properties</span></span>

<span data-ttu-id="a07c5-112">**Process \_ V1 \_ TypeGroup1** 類別具有這些屬性。</span><span class="sxs-lookup"><span data-stu-id="a07c5-112">The **Process\_V1\_TypeGroup1** class has these properties.</span></span>

<dl> <dt>

<span data-ttu-id="a07c5-113">ExitStatus</span><span class="sxs-lookup"><span data-stu-id="a07c5-113">ExitStatus</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="a07c5-114">資料類型： **sint32**</span><span class="sxs-lookup"><span data-stu-id="a07c5-114">Data type: **sint32**</span></span>
</dt> <dt>

<span data-ttu-id="a07c5-115">存取類型：唯讀</span><span class="sxs-lookup"><span data-stu-id="a07c5-115">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="a07c5-116">限定詞： WmiDataId (5) </span><span class="sxs-lookup"><span data-stu-id="a07c5-116">Qualifiers: WmiDataId(5)</span></span>
</dt> </dl>

<span data-ttu-id="a07c5-117">已停止進程的結束狀態。</span><span class="sxs-lookup"><span data-stu-id="a07c5-117">Exit status of the stopped process.</span></span>

</dd> <dt>

<span data-ttu-id="a07c5-118">ImageFileName</span><span class="sxs-lookup"><span data-stu-id="a07c5-118">ImageFileName</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="a07c5-119">資料類型： **字串**</span><span class="sxs-lookup"><span data-stu-id="a07c5-119">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="a07c5-120">存取類型：唯讀</span><span class="sxs-lookup"><span data-stu-id="a07c5-120">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="a07c5-121">限定詞： WmiDataId (7) ，StringTermination ( "NullTerminated" ) </span><span class="sxs-lookup"><span data-stu-id="a07c5-121">Qualifiers: WmiDataId(7), StringTermination("NullTerminated")</span></span>
</dt> </dl>

<span data-ttu-id="a07c5-122">進程可執行檔的路徑。</span><span class="sxs-lookup"><span data-stu-id="a07c5-122">Path to the executable file of the process.</span></span>

</dd> <dt>

<span data-ttu-id="a07c5-123">PageDirectoryBase</span><span class="sxs-lookup"><span data-stu-id="a07c5-123">PageDirectoryBase</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="a07c5-124">資料類型： **uint32**</span><span class="sxs-lookup"><span data-stu-id="a07c5-124">Data type: **uint32**</span></span>
</dt> <dt>

<span data-ttu-id="a07c5-125">存取類型：唯讀</span><span class="sxs-lookup"><span data-stu-id="a07c5-125">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="a07c5-126">限定詞： WmiDataId (1) ，指標</span><span class="sxs-lookup"><span data-stu-id="a07c5-126">Qualifiers: WmiDataId(1), Pointer</span></span>
</dt> </dl>

<span data-ttu-id="a07c5-127">保留的。</span><span class="sxs-lookup"><span data-stu-id="a07c5-127">Reserved.</span></span>

</dd> <dt>

<span data-ttu-id="a07c5-128">ParentId</span><span class="sxs-lookup"><span data-stu-id="a07c5-128">ParentId</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="a07c5-129">資料類型： **uint32**</span><span class="sxs-lookup"><span data-stu-id="a07c5-129">Data type: **uint32**</span></span>
</dt> <dt>

<span data-ttu-id="a07c5-130">存取類型：唯讀</span><span class="sxs-lookup"><span data-stu-id="a07c5-130">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="a07c5-131">限定詞： WmiDataId (3) </span><span class="sxs-lookup"><span data-stu-id="a07c5-131">Qualifiers: WmiDataId(3)</span></span>
</dt> </dl>

<span data-ttu-id="a07c5-132">建立此進程之進程的唯一識別碼。</span><span class="sxs-lookup"><span data-stu-id="a07c5-132">Unique identifier of the process that creates this process.</span></span> <span data-ttu-id="a07c5-133">系統會重複使用處理序識別碼，因此它們只會在該進程的存留期內找出處理常式。</span><span class="sxs-lookup"><span data-stu-id="a07c5-133">Process identifier numbers are reused, so they only identify a process for the lifetime of that process.</span></span> <span data-ttu-id="a07c5-134">ParentProcessId 所識別的進程可能會終止，因此 ParentProcessId 可能不會參考執行中的進程。</span><span class="sxs-lookup"><span data-stu-id="a07c5-134">It is possible that the process identified by ParentProcessId is terminated, so ParentProcessId may not refer to a running process.</span></span> <span data-ttu-id="a07c5-135">ParentProcessId 也可能不正確地參考重複使用處理序識別碼的進程。</span><span class="sxs-lookup"><span data-stu-id="a07c5-135">It is also possible that ParentProcessId incorrectly refers to a process that reuses a process identifier.</span></span>

<span data-ttu-id="a07c5-136">**Windows Server 2003：** 包含 ( "x" ) 限定詞的格式。</span><span class="sxs-lookup"><span data-stu-id="a07c5-136">**Windows Server 2003:** Includes the Format("x") qualifier.</span></span>

</dd> <dt>

<span data-ttu-id="a07c5-137">ProcessId</span><span class="sxs-lookup"><span data-stu-id="a07c5-137">ProcessId</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="a07c5-138">資料類型： **uint32**</span><span class="sxs-lookup"><span data-stu-id="a07c5-138">Data type: **uint32**</span></span>
</dt> <dt>

<span data-ttu-id="a07c5-139">存取類型：唯讀</span><span class="sxs-lookup"><span data-stu-id="a07c5-139">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="a07c5-140">限定詞： WmiDataId (2) </span><span class="sxs-lookup"><span data-stu-id="a07c5-140">Qualifiers: WmiDataId(2)</span></span>
</dt> </dl>

<span data-ttu-id="a07c5-141">您可以用來識別進程的全域處理序識別碼。</span><span class="sxs-lookup"><span data-stu-id="a07c5-141">Global process identifier that you can use to identify a process.</span></span> <span data-ttu-id="a07c5-142">此值從建立進程到終止之前都有效。</span><span class="sxs-lookup"><span data-stu-id="a07c5-142">The value is valid from the time a process is created until it is terminated.</span></span>

<span data-ttu-id="a07c5-143">**Windows Server 2003：** 包含 ( "x" ) 限定詞的格式。</span><span class="sxs-lookup"><span data-stu-id="a07c5-143">**Windows Server 2003:** Includes the Format("x") qualifier.</span></span>

</dd> <dt>

<span data-ttu-id="a07c5-144">SessionId</span><span class="sxs-lookup"><span data-stu-id="a07c5-144">SessionId</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="a07c5-145">資料類型： **uint32**</span><span class="sxs-lookup"><span data-stu-id="a07c5-145">Data type: **uint32**</span></span>
</dt> <dt>

<span data-ttu-id="a07c5-146">存取類型：唯讀</span><span class="sxs-lookup"><span data-stu-id="a07c5-146">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="a07c5-147">限定詞： WmiDataId (4) </span><span class="sxs-lookup"><span data-stu-id="a07c5-147">Qualifiers: WmiDataId(4)</span></span>
</dt> </dl>

<span data-ttu-id="a07c5-148">作業系統在建立新的會話時所產生的唯一識別碼。</span><span class="sxs-lookup"><span data-stu-id="a07c5-148">Unique identifier that an operating system generates when it creates a new session.</span></span> <span data-ttu-id="a07c5-149">會話從登入到從特定系統登出的一段時間。</span><span class="sxs-lookup"><span data-stu-id="a07c5-149">A session spans a period of time from log on until log off from a specific system.</span></span>

</dd> <dt>

<span data-ttu-id="a07c5-150">UserSID</span><span class="sxs-lookup"><span data-stu-id="a07c5-150">UserSID</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="a07c5-151">資料類型： **物件**</span><span class="sxs-lookup"><span data-stu-id="a07c5-151">Data type: **object**</span></span>
</dt> <dt>

<span data-ttu-id="a07c5-152">存取類型：唯讀</span><span class="sxs-lookup"><span data-stu-id="a07c5-152">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="a07c5-153">限定詞： WmiDataId (6) ，副檔名 ( "Sid" ) </span><span class="sxs-lookup"><span data-stu-id="a07c5-153">Qualifiers: WmiDataId(6), Extension("Sid")</span></span>
</dt> </dl>

<span data-ttu-id="a07c5-154">安全性識別元 (SID) 用於事件發生所在的使用者內容。</span><span class="sxs-lookup"><span data-stu-id="a07c5-154">Security identifier (SID) for the user context under which the event happens.</span></span>

</dd> </dl>

## <a name="requirements"></a><span data-ttu-id="a07c5-155">規格需求</span><span class="sxs-lookup"><span data-stu-id="a07c5-155">Requirements</span></span>



| <span data-ttu-id="a07c5-156">需求</span><span class="sxs-lookup"><span data-stu-id="a07c5-156">Requirement</span></span> | <span data-ttu-id="a07c5-157">值</span><span class="sxs-lookup"><span data-stu-id="a07c5-157">Value</span></span> |
|-------------------------------------|------------------------------------------------------|
| <span data-ttu-id="a07c5-158">最低支援的用戶端</span><span class="sxs-lookup"><span data-stu-id="a07c5-158">Minimum supported client</span></span><br/> | <span data-ttu-id="a07c5-159">\[僅限 WINDOWS XP desktop 應用程式\]</span><span class="sxs-lookup"><span data-stu-id="a07c5-159">Windows XP \[desktop apps only\]</span></span><br/>          |
| <span data-ttu-id="a07c5-160">最低支援的伺服器</span><span class="sxs-lookup"><span data-stu-id="a07c5-160">Minimum supported server</span></span><br/> | <span data-ttu-id="a07c5-161">僅限 Windows Server 2003 \[ desktop 應用程式\]</span><span class="sxs-lookup"><span data-stu-id="a07c5-161">Windows Server 2003 \[desktop apps only\]</span></span><br/> |



## <a name="see-also"></a><span data-ttu-id="a07c5-162">另請參閱</span><span class="sxs-lookup"><span data-stu-id="a07c5-162">See also</span></span>

<dl> <dt>

[<span data-ttu-id="a07c5-163">**進程 \_ V1**</span><span class="sxs-lookup"><span data-stu-id="a07c5-163">**Process\_V1**</span></span>](process.md)
</dt> <dt>

[<span data-ttu-id="a07c5-164">**進程 \_ V1**</span><span class="sxs-lookup"><span data-stu-id="a07c5-164">**Process\_V1**</span></span>](process-v1.md)
</dt> </dl>

 

 




