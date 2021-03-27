---
description: 這個類別是執行緒結束事件的事件種類類別。 以下是從 MOF 程式碼簡化的語法。
ms.assetid: c495bf22-04ce-4285-8e7e-152e4ab65823
title: Thread_V1_TypeGroup2 類別
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Thread_V1_TypeGroup2
- Thread_V1_TypeGroup2.ProcessId
- Thread_V1_TypeGroup2.TThreadId
api_type:
- NA
api_location: ''
ms.openlocfilehash: 3e56590127b2317813d7431a1cc646fbe76e35a9
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/07/2021
ms.locfileid: "104512188"
---
# <a name="thread_v1_typegroup2-class"></a><span data-ttu-id="09710-104">Thread \_ V1 \_ TypeGroup2 類別</span><span class="sxs-lookup"><span data-stu-id="09710-104">Thread\_V1\_TypeGroup2 class</span></span>

<span data-ttu-id="09710-105">這個類別是執行緒結束事件的事件種類類別。</span><span class="sxs-lookup"><span data-stu-id="09710-105">This class is the event type class for thread end events.</span></span>

<span data-ttu-id="09710-106">以下是從 MOF 程式碼簡化的語法。</span><span class="sxs-lookup"><span data-stu-id="09710-106">The following syntax is simplified from MOF code.</span></span>

## <a name="syntax"></a><span data-ttu-id="09710-107">語法</span><span class="sxs-lookup"><span data-stu-id="09710-107">Syntax</span></span>

``` syntax
[EventType{2, 4}, EventTypeName{"End", "DCEnd"}]
class Thread_V1_TypeGroup2 : Thread_V1
{
  uint32 ProcessId;
  uint32 TThreadId;
};
```

## <a name="members"></a><span data-ttu-id="09710-108">成員</span><span class="sxs-lookup"><span data-stu-id="09710-108">Members</span></span>

<span data-ttu-id="09710-109">**Thread \_ V1 \_ TypeGroup2** 類別具有下列類型的成員：</span><span class="sxs-lookup"><span data-stu-id="09710-109">The **Thread\_V1\_TypeGroup2** class has these types of members:</span></span>

-   [<span data-ttu-id="09710-110">屬性</span><span class="sxs-lookup"><span data-stu-id="09710-110">Properties</span></span>](#properties)

### <a name="properties"></a><span data-ttu-id="09710-111">屬性</span><span class="sxs-lookup"><span data-stu-id="09710-111">Properties</span></span>

<span data-ttu-id="09710-112">**Thread \_ V1 \_ TypeGroup2** 類別具有這些屬性。</span><span class="sxs-lookup"><span data-stu-id="09710-112">The **Thread\_V1\_TypeGroup2** class has these properties.</span></span>

<dl> <dt>

<span data-ttu-id="09710-113">ProcessId</span><span class="sxs-lookup"><span data-stu-id="09710-113">ProcessId</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="09710-114">資料類型： **uint32**</span><span class="sxs-lookup"><span data-stu-id="09710-114">Data type: **uint32**</span></span>
</dt> <dt>

<span data-ttu-id="09710-115">存取類型：唯讀</span><span class="sxs-lookup"><span data-stu-id="09710-115">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="09710-116">限定詞： WmiDataId (1) </span><span class="sxs-lookup"><span data-stu-id="09710-116">Qualifiers: WmiDataId(1)</span></span>
</dt> </dl>

<span data-ttu-id="09710-117">事件所涉及之執行緒的處理序識別碼。</span><span class="sxs-lookup"><span data-stu-id="09710-117">Process identifier of the thread involved in the event.</span></span>

<span data-ttu-id="09710-118">**Windows Server 2003：** 包含 ( "x" ) 限定詞的格式。</span><span class="sxs-lookup"><span data-stu-id="09710-118">**Windows Server 2003:** Contains the Format("x") qualifier.</span></span>

</dd> <dt>

<span data-ttu-id="09710-119">TThreadId</span><span class="sxs-lookup"><span data-stu-id="09710-119">TThreadId</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="09710-120">資料類型： **uint32**</span><span class="sxs-lookup"><span data-stu-id="09710-120">Data type: **uint32**</span></span>
</dt> <dt>

<span data-ttu-id="09710-121">存取類型：唯讀</span><span class="sxs-lookup"><span data-stu-id="09710-121">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="09710-122">限定詞： WmiDataId (2) </span><span class="sxs-lookup"><span data-stu-id="09710-122">Qualifiers: WmiDataId(2)</span></span>
</dt> </dl>

<span data-ttu-id="09710-123">事件所涉及之執行緒的執行緒識別碼。</span><span class="sxs-lookup"><span data-stu-id="09710-123">Thread identifier of the thread involved in the event.</span></span>

<span data-ttu-id="09710-124">**Windows Server 2003：** 包含 ( "x" ) 限定詞的格式。</span><span class="sxs-lookup"><span data-stu-id="09710-124">**Windows Server 2003:** Contains the Format("x") qualifier.</span></span>

</dd> </dl>

## <a name="requirements"></a><span data-ttu-id="09710-125">規格需求</span><span class="sxs-lookup"><span data-stu-id="09710-125">Requirements</span></span>



| <span data-ttu-id="09710-126">需求</span><span class="sxs-lookup"><span data-stu-id="09710-126">Requirement</span></span> | <span data-ttu-id="09710-127">值</span><span class="sxs-lookup"><span data-stu-id="09710-127">Value</span></span> |
|-------------------------------------|------------------------------------------------------|
| <span data-ttu-id="09710-128">最低支援的用戶端</span><span class="sxs-lookup"><span data-stu-id="09710-128">Minimum supported client</span></span><br/> | <span data-ttu-id="09710-129">\[僅限 WINDOWS XP desktop 應用程式\]</span><span class="sxs-lookup"><span data-stu-id="09710-129">Windows XP \[desktop apps only\]</span></span><br/>          |
| <span data-ttu-id="09710-130">最低支援的伺服器</span><span class="sxs-lookup"><span data-stu-id="09710-130">Minimum supported server</span></span><br/> | <span data-ttu-id="09710-131">僅限 Windows Server 2003 \[ desktop 應用程式\]</span><span class="sxs-lookup"><span data-stu-id="09710-131">Windows Server 2003 \[desktop apps only\]</span></span><br/> |



## <a name="see-also"></a><span data-ttu-id="09710-132">另請參閱</span><span class="sxs-lookup"><span data-stu-id="09710-132">See also</span></span>

<dl> <dt>

[<span data-ttu-id="09710-133">**執行緒 \_ V1**</span><span class="sxs-lookup"><span data-stu-id="09710-133">**Thread\_V1**</span></span>](thread-v1.md)
</dt> </dl>

 

 




