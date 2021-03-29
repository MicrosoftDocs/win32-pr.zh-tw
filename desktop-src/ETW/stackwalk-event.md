---
description: 這個類別是堆疊追蹤事件的事件種類類別。
ms.assetid: 05117bd6-a39c-42f3-8aed-c6f758f946c6
title: StackWalk_Event 類別
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- StackWalk_Event
- StackWalk_Event.EventTimeStamp
- StackWalk_Event.StackProcess
- StackWalk_Event.StackThread
- StackWalk_Event.Stack1
- StackWalk_Event.Stack192
api_type:
- NA
api_location: ''
ms.openlocfilehash: 746a7f2a9b5f6bb6316bf0d0e20e5645cea15a7e
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: HT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/08/2021
ms.locfileid: "104973413"
---
# <a name="stackwalk_event-class"></a><span data-ttu-id="aac9d-103">StackWalk \_ 事件類別</span><span class="sxs-lookup"><span data-stu-id="aac9d-103">StackWalk\_Event class</span></span>

<span data-ttu-id="aac9d-104">這個類別是堆疊追蹤事件的事件種類類別。</span><span class="sxs-lookup"><span data-stu-id="aac9d-104">This class is the event type class for stack tracing events.</span></span>

<span data-ttu-id="aac9d-105">下列語法是簡化自 MOF 程式碼，且包含所有繼承的屬性。</span><span class="sxs-lookup"><span data-stu-id="aac9d-105">The following syntax is simplified from MOF code and includes all inherited properties.</span></span>

## <a name="syntax"></a><span data-ttu-id="aac9d-106">語法</span><span class="sxs-lookup"><span data-stu-id="aac9d-106">Syntax</span></span>

``` syntax
[EventType{32}, EventTypeName{"Stack"}]
class StackWalk_Event : StackWalk
{
  uint64 EventTimeStamp;
  uint32 StackProcess;
  uint32 StackThread;
  uint32 Stack1;
  uint32 Stack192;
};
```

## <a name="members"></a><span data-ttu-id="aac9d-107">成員</span><span class="sxs-lookup"><span data-stu-id="aac9d-107">Members</span></span>

<span data-ttu-id="aac9d-108">**StackWalk \_ 事件** 類別具有下列類型的成員：</span><span class="sxs-lookup"><span data-stu-id="aac9d-108">The **StackWalk\_Event** class has these types of members:</span></span>

-   [<span data-ttu-id="aac9d-109">屬性</span><span class="sxs-lookup"><span data-stu-id="aac9d-109">Properties</span></span>](#properties)

### <a name="properties"></a><span data-ttu-id="aac9d-110">屬性</span><span class="sxs-lookup"><span data-stu-id="aac9d-110">Properties</span></span>

<span data-ttu-id="aac9d-111">**StackWalk \_ 事件** 類別具有這些屬性。</span><span class="sxs-lookup"><span data-stu-id="aac9d-111">The **StackWalk\_Event** class has these properties.</span></span>

<dl> <dt>

<span data-ttu-id="aac9d-112">**EventTimeStamp**</span><span class="sxs-lookup"><span data-stu-id="aac9d-112">**EventTimeStamp**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="aac9d-113">資料類型： **uint64**</span><span class="sxs-lookup"><span data-stu-id="aac9d-113">Data type: **uint64**</span></span>
</dt> <dt>

<span data-ttu-id="aac9d-114">存取類型：唯讀</span><span class="sxs-lookup"><span data-stu-id="aac9d-114">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="aac9d-115">限定詞： WmiDataId (1) </span><span class="sxs-lookup"><span data-stu-id="aac9d-115">Qualifiers: WmiDataId(1)</span></span>
</dt> </dl>

<span data-ttu-id="aac9d-116">事件標頭中的原始事件時間戳記。</span><span class="sxs-lookup"><span data-stu-id="aac9d-116">Original event time stamp from the event header.</span></span> <span data-ttu-id="aac9d-117">您可以使用此時間戳記，將堆疊與事件進行比對。</span><span class="sxs-lookup"><span data-stu-id="aac9d-117">Use this time stamp to match the stack to an event.</span></span>

</dd> <dt>

<span data-ttu-id="aac9d-118">**Stack1**</span><span class="sxs-lookup"><span data-stu-id="aac9d-118">**Stack1**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="aac9d-119">資料類型： **uint32**</span><span class="sxs-lookup"><span data-stu-id="aac9d-119">Data type: **uint32**</span></span>
</dt> <dt>

<span data-ttu-id="aac9d-120">存取類型：唯讀</span><span class="sxs-lookup"><span data-stu-id="aac9d-120">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="aac9d-121">限定詞： WmiDataId (4) ，指標</span><span class="sxs-lookup"><span data-stu-id="aac9d-121">Qualifiers: WmiDataId(4), pointer</span></span>
</dt> </dl>

<span data-ttu-id="aac9d-122">呼叫的位址。</span><span class="sxs-lookup"><span data-stu-id="aac9d-122">Address of the call.</span></span>

</dd> <dt>

<span data-ttu-id="aac9d-123">**Stack192**</span><span class="sxs-lookup"><span data-stu-id="aac9d-123">**Stack192**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="aac9d-124">資料類型： **uint32**</span><span class="sxs-lookup"><span data-stu-id="aac9d-124">Data type: **uint32**</span></span>
</dt> <dt>

<span data-ttu-id="aac9d-125">存取類型：唯讀</span><span class="sxs-lookup"><span data-stu-id="aac9d-125">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="aac9d-126">限定詞： WmiDataId (195) ，指標</span><span class="sxs-lookup"><span data-stu-id="aac9d-126">Qualifiers: WmiDataId(195), pointer</span></span>
</dt> </dl>

<span data-ttu-id="aac9d-127">呼叫的位址。</span><span class="sxs-lookup"><span data-stu-id="aac9d-127">Address of the call.</span></span>

</dd> <dt>

<span data-ttu-id="aac9d-128">**StackProcess**</span><span class="sxs-lookup"><span data-stu-id="aac9d-128">**StackProcess**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="aac9d-129">資料類型： **uint32**</span><span class="sxs-lookup"><span data-stu-id="aac9d-129">Data type: **uint32**</span></span>
</dt> <dt>

<span data-ttu-id="aac9d-130">存取類型：唯讀</span><span class="sxs-lookup"><span data-stu-id="aac9d-130">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="aac9d-131">限定詞： WmiDataId (2) ，格式 ( "x" ) </span><span class="sxs-lookup"><span data-stu-id="aac9d-131">Qualifiers: WmiDataId(2), format("x")</span></span>
</dt> </dl>

<span data-ttu-id="aac9d-132">原始事件的處理序識別碼。</span><span class="sxs-lookup"><span data-stu-id="aac9d-132">The process identifier of the original event.</span></span>

</dd> <dt>

<span data-ttu-id="aac9d-133">**StackThread**</span><span class="sxs-lookup"><span data-stu-id="aac9d-133">**StackThread**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="aac9d-134">資料類型： **uint32**</span><span class="sxs-lookup"><span data-stu-id="aac9d-134">Data type: **uint32**</span></span>
</dt> <dt>

<span data-ttu-id="aac9d-135">存取類型：唯讀</span><span class="sxs-lookup"><span data-stu-id="aac9d-135">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="aac9d-136">限定詞： WmiDataId (3) </span><span class="sxs-lookup"><span data-stu-id="aac9d-136">Qualifiers: WmiDataId(3)</span></span>
</dt> </dl>

<span data-ttu-id="aac9d-137">原始事件的執行緒識別碼。</span><span class="sxs-lookup"><span data-stu-id="aac9d-137">The thread identifier of the original event.</span></span>

</dd> </dl>

## <a name="remarks"></a><span data-ttu-id="aac9d-138">備註</span><span class="sxs-lookup"><span data-stu-id="aac9d-138">Remarks</span></span>

<span data-ttu-id="aac9d-139">請注意，此類別不會顯示存在於 **Stack1** 與 **Stack192** 之間的所有 **Stack \* n**\* 屬性。</span><span class="sxs-lookup"><span data-stu-id="aac9d-139">Note that the class does not show all of the **Stack\*n**\* properties that exist between **Stack1** and **Stack192**.</span></span> <span data-ttu-id="aac9d-140">使用事件的大小，判斷有多少 **Stack \* n**\* 屬性包含有效的位址。</span><span class="sxs-lookup"><span data-stu-id="aac9d-140">Use the size of the event to determine how many **Stack\*n**\* properties contain valid addresses.</span></span>

## <a name="requirements"></a><span data-ttu-id="aac9d-141">規格需求</span><span class="sxs-lookup"><span data-stu-id="aac9d-141">Requirements</span></span>



| <span data-ttu-id="aac9d-142">需求</span><span class="sxs-lookup"><span data-stu-id="aac9d-142">Requirement</span></span> | <span data-ttu-id="aac9d-143">值</span><span class="sxs-lookup"><span data-stu-id="aac9d-143">Value</span></span> |
|-------------------------------------|---------------------------------------------------------|
| <span data-ttu-id="aac9d-144">最低支援的用戶端</span><span class="sxs-lookup"><span data-stu-id="aac9d-144">Minimum supported client</span></span><br/> | <span data-ttu-id="aac9d-145">\[僅限 Windows 7 桌面應用程式\]</span><span class="sxs-lookup"><span data-stu-id="aac9d-145">Windows 7 \[desktop apps only\]</span></span><br/>              |
| <span data-ttu-id="aac9d-146">最低支援的伺服器</span><span class="sxs-lookup"><span data-stu-id="aac9d-146">Minimum supported server</span></span><br/> | <span data-ttu-id="aac9d-147">僅限 Windows Server 2008 R2 \[ desktop 應用程式\]</span><span class="sxs-lookup"><span data-stu-id="aac9d-147">Windows Server 2008 R2 \[desktop apps only\]</span></span><br/> |



 

 




