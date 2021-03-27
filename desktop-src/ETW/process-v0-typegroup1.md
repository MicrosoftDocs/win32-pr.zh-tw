---
description: 這個類別是處理事件的事件種類類別。 以下是從 MOF 程式碼簡化的語法。
ms.assetid: fcf2897d-32b4-42b9-892c-f0106687d3c2
title: Process_V0_TypeGroup1 類別
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Process_V0_TypeGroup1
- Process_V0_TypeGroup1.ProcessId
- Process_V0_TypeGroup1.ParentId
- Process_V0_TypeGroup1.UserSID
- Process_V0_TypeGroup1.ImageFileName
api_type:
- NA
api_location: ''
ms.openlocfilehash: 2889feb05bfc396f2c2018ca59d2cf46fba8ec13
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/07/2021
ms.locfileid: "104972224"
---
# <a name="process_v0_typegroup1-class"></a><span data-ttu-id="c5434-104">Process \_ V0 \_ TypeGroup1 類別</span><span class="sxs-lookup"><span data-stu-id="c5434-104">Process\_V0\_TypeGroup1 class</span></span>

<span data-ttu-id="c5434-105">這個類別是處理事件的事件種類類別。</span><span class="sxs-lookup"><span data-stu-id="c5434-105">This class is the event type class for process events.</span></span>

<span data-ttu-id="c5434-106">以下是從 MOF 程式碼簡化的語法。</span><span class="sxs-lookup"><span data-stu-id="c5434-106">The following syntax is simplified from MOF code.</span></span>

## <a name="syntax"></a><span data-ttu-id="c5434-107">語法</span><span class="sxs-lookup"><span data-stu-id="c5434-107">Syntax</span></span>

``` syntax
[EventType{1, 2, 3, 4}, EventTypeName{"Start", "End", "DCStart", "DCEnd"}]
class Process_V0_TypeGroup1 : Process_V0
{
  uint32 ProcessId;
  uint32 ParentId;
  object UserSID;
  string ImageFileName;
};
```

## <a name="members"></a><span data-ttu-id="c5434-108">成員</span><span class="sxs-lookup"><span data-stu-id="c5434-108">Members</span></span>

<span data-ttu-id="c5434-109">**Process \_ V0 \_ TypeGroup1** 類別具有下列類型的成員：</span><span class="sxs-lookup"><span data-stu-id="c5434-109">The **Process\_V0\_TypeGroup1** class has these types of members:</span></span>

-   [<span data-ttu-id="c5434-110">屬性</span><span class="sxs-lookup"><span data-stu-id="c5434-110">Properties</span></span>](#properties)

### <a name="properties"></a><span data-ttu-id="c5434-111">屬性</span><span class="sxs-lookup"><span data-stu-id="c5434-111">Properties</span></span>

<span data-ttu-id="c5434-112">**Process \_ V0 \_ TypeGroup1** 類別具有這些屬性。</span><span class="sxs-lookup"><span data-stu-id="c5434-112">The **Process\_V0\_TypeGroup1** class has these properties.</span></span>

<dl> <dt>

<span data-ttu-id="c5434-113">ImageFileName</span><span class="sxs-lookup"><span data-stu-id="c5434-113">ImageFileName</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="c5434-114">資料類型： **字串**</span><span class="sxs-lookup"><span data-stu-id="c5434-114">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="c5434-115">存取類型：唯讀</span><span class="sxs-lookup"><span data-stu-id="c5434-115">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="c5434-116">限定詞： WmiDataId (4) ，StringTermination ( "NullTerminated" ) </span><span class="sxs-lookup"><span data-stu-id="c5434-116">Qualifiers: WmiDataId(4), StringTermination("NullTerminated")</span></span>
</dt> </dl>

<span data-ttu-id="c5434-117">進程可執行檔的路徑。</span><span class="sxs-lookup"><span data-stu-id="c5434-117">Path to the executable file of the process.</span></span>

</dd> <dt>

<span data-ttu-id="c5434-118">ParentId</span><span class="sxs-lookup"><span data-stu-id="c5434-118">ParentId</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="c5434-119">資料類型： **uint32**</span><span class="sxs-lookup"><span data-stu-id="c5434-119">Data type: **uint32**</span></span>
</dt> <dt>

<span data-ttu-id="c5434-120">存取類型：唯讀</span><span class="sxs-lookup"><span data-stu-id="c5434-120">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="c5434-121">限定詞： WmiDataId (2) ，指標</span><span class="sxs-lookup"><span data-stu-id="c5434-121">Qualifiers: WmiDataId(2), Pointer</span></span>
</dt> </dl>

<span data-ttu-id="c5434-122">建立進程之進程的唯一識別碼。</span><span class="sxs-lookup"><span data-stu-id="c5434-122">Unique identifier of the process that creates a process.</span></span> <span data-ttu-id="c5434-123">系統會重複使用處理序識別碼，因此它們只會在該進程的存留期內找出處理常式。</span><span class="sxs-lookup"><span data-stu-id="c5434-123">Process identifier numbers are reused, so they only identify a process for the lifetime of that process.</span></span> <span data-ttu-id="c5434-124">ParentProcessId 所識別的進程可能會終止，因此 ParentProcessId 可能不會參考執行中的進程。</span><span class="sxs-lookup"><span data-stu-id="c5434-124">It is possible that the process identified by ParentProcessId is terminated, so ParentProcessId may not refer to a running process.</span></span> <span data-ttu-id="c5434-125">ParentProcessId 也可能不正確地參考重複使用處理序識別碼的進程。</span><span class="sxs-lookup"><span data-stu-id="c5434-125">It is also possible that ParentProcessId incorrectly refers to a process that reuses a process identifier.</span></span>

</dd> <dt>

<span data-ttu-id="c5434-126">ProcessId</span><span class="sxs-lookup"><span data-stu-id="c5434-126">ProcessId</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="c5434-127">資料類型： **uint32**</span><span class="sxs-lookup"><span data-stu-id="c5434-127">Data type: **uint32**</span></span>
</dt> <dt>

<span data-ttu-id="c5434-128">存取類型：唯讀</span><span class="sxs-lookup"><span data-stu-id="c5434-128">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="c5434-129">限定詞： WmiDataId (1) ，指標</span><span class="sxs-lookup"><span data-stu-id="c5434-129">Qualifiers: WmiDataId(1), Pointer</span></span>
</dt> </dl>

<span data-ttu-id="c5434-130">您可以用來識別進程的全域處理序識別碼。</span><span class="sxs-lookup"><span data-stu-id="c5434-130">Global process identifier that you can use to identify a process.</span></span> <span data-ttu-id="c5434-131">此值從建立進程到終止之前都有效。</span><span class="sxs-lookup"><span data-stu-id="c5434-131">The value is valid from the time a process is created until it is terminated.</span></span>

</dd> <dt>

<span data-ttu-id="c5434-132">UserSID</span><span class="sxs-lookup"><span data-stu-id="c5434-132">UserSID</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="c5434-133">資料類型： **物件**</span><span class="sxs-lookup"><span data-stu-id="c5434-133">Data type: **object**</span></span>
</dt> <dt>

<span data-ttu-id="c5434-134">存取類型：唯讀</span><span class="sxs-lookup"><span data-stu-id="c5434-134">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="c5434-135">限定詞： WmiDataId (3) ，副檔名 ( "Sid" ) </span><span class="sxs-lookup"><span data-stu-id="c5434-135">Qualifiers: WmiDataId(3), Extension("Sid")</span></span>
</dt> </dl>

<span data-ttu-id="c5434-136">安全性識別元 (SID) 用於事件發生所在的使用者內容。</span><span class="sxs-lookup"><span data-stu-id="c5434-136">Security identifier (SID) for the user context under which the event happens.</span></span>

</dd> </dl>

## <a name="requirements"></a><span data-ttu-id="c5434-137">規格需求</span><span class="sxs-lookup"><span data-stu-id="c5434-137">Requirements</span></span>



| <span data-ttu-id="c5434-138">需求</span><span class="sxs-lookup"><span data-stu-id="c5434-138">Requirement</span></span> | <span data-ttu-id="c5434-139">值</span><span class="sxs-lookup"><span data-stu-id="c5434-139">Value</span></span> |
|-------------------------------------|------------------------------------------------------|
| <span data-ttu-id="c5434-140">最低支援的用戶端</span><span class="sxs-lookup"><span data-stu-id="c5434-140">Minimum supported client</span></span><br/> | <span data-ttu-id="c5434-141">\[僅限 WINDOWS XP desktop 應用程式\]</span><span class="sxs-lookup"><span data-stu-id="c5434-141">Windows XP \[desktop apps only\]</span></span><br/>          |
| <span data-ttu-id="c5434-142">最低支援的伺服器</span><span class="sxs-lookup"><span data-stu-id="c5434-142">Minimum supported server</span></span><br/> | <span data-ttu-id="c5434-143">僅限 Windows Server 2003 \[ desktop 應用程式\]</span><span class="sxs-lookup"><span data-stu-id="c5434-143">Windows Server 2003 \[desktop apps only\]</span></span><br/> |



## <a name="see-also"></a><span data-ttu-id="c5434-144">另請參閱</span><span class="sxs-lookup"><span data-stu-id="c5434-144">See also</span></span>

<dl> <dt>

[<span data-ttu-id="c5434-145">**進程 \_ V0**</span><span class="sxs-lookup"><span data-stu-id="c5434-145">**Process\_V0**</span></span>](process-v0.md)
</dt> </dl>

 

 




