---
description: 此類別是分頁錯誤事件的事件種類類別。 以下是從 MOF 程式碼簡化的語法。
ms.assetid: 59cb1091-af21-4fe6-87b8-17a262cc4467
title: PageFault_TypeGroup1 類別
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- PageFault_TypeGroup1
- PageFault_TypeGroup1.VirtualAddress
- PageFault_TypeGroup1.ProgramCounter
api_type:
- NA
api_location: ''
ms.openlocfilehash: 4bf1f49c909833d75af844c8f2f943a01b6a5d6d
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/08/2021
ms.locfileid: "104193517"
---
# <a name="pagefault_typegroup1-class"></a><span data-ttu-id="e7ac0-104">PageFault \_ TypeGroup1 類別</span><span class="sxs-lookup"><span data-stu-id="e7ac0-104">PageFault\_TypeGroup1 class</span></span>

<span data-ttu-id="e7ac0-105">此類別是分頁錯誤事件的事件種類類別。</span><span class="sxs-lookup"><span data-stu-id="e7ac0-105">This class is the event type class for page fault events.</span></span>

<span data-ttu-id="e7ac0-106">以下是從 MOF 程式碼簡化的語法。</span><span class="sxs-lookup"><span data-stu-id="e7ac0-106">The following syntax is simplified from MOF code.</span></span>

## <a name="syntax"></a><span data-ttu-id="e7ac0-107">語法</span><span class="sxs-lookup"><span data-stu-id="e7ac0-107">Syntax</span></span>

``` syntax
[EventType{10, 11, 12, 13, 14, 15}, EventTypeName{"TransitionFault", "DemandZeroFault", "CopyOnWrite", "GuardPageFault", "HardPageFault", "AccessViolation"}]
class PageFault_TypeGroup1 : PageFault_V2
{
  uint32 VirtualAddress;
  uint32 ProgramCounter;
};
```

## <a name="members"></a><span data-ttu-id="e7ac0-108">成員</span><span class="sxs-lookup"><span data-stu-id="e7ac0-108">Members</span></span>

<span data-ttu-id="e7ac0-109">**PageFault \_ TypeGroup1** 類別具有下列類型的成員：</span><span class="sxs-lookup"><span data-stu-id="e7ac0-109">The **PageFault\_TypeGroup1** class has these types of members:</span></span>

-   [<span data-ttu-id="e7ac0-110">屬性</span><span class="sxs-lookup"><span data-stu-id="e7ac0-110">Properties</span></span>](#properties)

### <a name="properties"></a><span data-ttu-id="e7ac0-111">屬性</span><span class="sxs-lookup"><span data-stu-id="e7ac0-111">Properties</span></span>

<span data-ttu-id="e7ac0-112">**PageFault \_ TypeGroup1** 類別具有這些屬性。</span><span class="sxs-lookup"><span data-stu-id="e7ac0-112">The **PageFault\_TypeGroup1** class has these properties.</span></span>

<dl> <dt>

<span data-ttu-id="e7ac0-113">ProgramCounter</span><span class="sxs-lookup"><span data-stu-id="e7ac0-113">ProgramCounter</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="e7ac0-114">資料類型： **uint32**</span><span class="sxs-lookup"><span data-stu-id="e7ac0-114">Data type: **uint32**</span></span>
</dt> <dt>

<span data-ttu-id="e7ac0-115">存取類型：唯讀</span><span class="sxs-lookup"><span data-stu-id="e7ac0-115">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="e7ac0-116">限定詞： WmiDataId (2) ，指標</span><span class="sxs-lookup"><span data-stu-id="e7ac0-116">Qualifiers: WmiDataId(2), Pointer</span></span>
</dt> </dl>

<span data-ttu-id="e7ac0-117">正在執行的目前指令指標。</span><span class="sxs-lookup"><span data-stu-id="e7ac0-117">Pointer to the current instruction being executed.</span></span>

</dd> <dt>

<span data-ttu-id="e7ac0-118">VirtualAddress</span><span class="sxs-lookup"><span data-stu-id="e7ac0-118">VirtualAddress</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="e7ac0-119">資料類型： **uint32**</span><span class="sxs-lookup"><span data-stu-id="e7ac0-119">Data type: **uint32**</span></span>
</dt> <dt>

<span data-ttu-id="e7ac0-120">存取類型：唯讀</span><span class="sxs-lookup"><span data-stu-id="e7ac0-120">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="e7ac0-121">限定詞： WmiDataId (1) ，指標</span><span class="sxs-lookup"><span data-stu-id="e7ac0-121">Qualifiers: WmiDataId(1), Pointer</span></span>
</dt> </dl>

<span data-ttu-id="e7ac0-122">造成分頁錯誤之頁面的虛擬位址。</span><span class="sxs-lookup"><span data-stu-id="e7ac0-122">Virtual address of the page that caused the page fault.</span></span>

</dd> </dl>

## <a name="remarks"></a><span data-ttu-id="e7ac0-123">備註</span><span class="sxs-lookup"><span data-stu-id="e7ac0-123">Remarks</span></span>

<span data-ttu-id="e7ac0-124">如果找不到在記憶體快取中找出的頁面，而且必須從記憶體中的其他位置取出 (軟錯誤) 或從磁片 (硬性錯誤) ，就會發生分頁錯誤。</span><span class="sxs-lookup"><span data-stu-id="e7ac0-124">A page fault occurs when a page sought in the memory cache is not found there and must be retrieved from elsewhere in memory (a soft fault) or from disk (a hard fault).</span></span>

## <a name="requirements"></a><span data-ttu-id="e7ac0-125">規格需求</span><span class="sxs-lookup"><span data-stu-id="e7ac0-125">Requirements</span></span>



| <span data-ttu-id="e7ac0-126">需求</span><span class="sxs-lookup"><span data-stu-id="e7ac0-126">Requirement</span></span> | <span data-ttu-id="e7ac0-127">值</span><span class="sxs-lookup"><span data-stu-id="e7ac0-127">Value</span></span> |
|-------------------------------------|------------------------------------------------------|
| <span data-ttu-id="e7ac0-128">最低支援的用戶端</span><span class="sxs-lookup"><span data-stu-id="e7ac0-128">Minimum supported client</span></span><br/> | <span data-ttu-id="e7ac0-129">\[僅限 Windows Vista 桌面應用程式\]</span><span class="sxs-lookup"><span data-stu-id="e7ac0-129">Windows Vista \[desktop apps only\]</span></span><br/>       |
| <span data-ttu-id="e7ac0-130">最低支援的伺服器</span><span class="sxs-lookup"><span data-stu-id="e7ac0-130">Minimum supported server</span></span><br/> | <span data-ttu-id="e7ac0-131">僅限 Windows Server 2008 \[ desktop 應用程式\]</span><span class="sxs-lookup"><span data-stu-id="e7ac0-131">Windows Server 2008 \[desktop apps only\]</span></span><br/> |



## <a name="see-also"></a><span data-ttu-id="e7ac0-132">另請參閱</span><span class="sxs-lookup"><span data-stu-id="e7ac0-132">See also</span></span>

<dl> <dt>

[<span data-ttu-id="e7ac0-133">**PageFault \_ V2**</span><span class="sxs-lookup"><span data-stu-id="e7ac0-133">**PageFault\_V2**</span></span>](pagefault-v2.md)
</dt> </dl>

 

 




