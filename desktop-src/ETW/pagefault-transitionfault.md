---
description: 此類別是分頁錯誤事件的事件種類類別。 以下是從 MOF 程式碼簡化的語法。
ms.assetid: cc2b7a93-6974-4872-98f3-d6cb81861ae5
title: PageFault_TransitionFault 類別
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- PageFault_TransitionFault
- PageFault_TransitionFault.VirtualAddress
- PageFault_TransitionFault.ProgramCounter
api_type:
- NA
api_location: ''
ms.openlocfilehash: 4721e2d342750b12baa58bb69f72606511c14143
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/08/2021
ms.locfileid: "103850308"
---
# <a name="pagefault_transitionfault-class"></a><span data-ttu-id="6fb6b-104">PageFault \_ TransitionFault 類別</span><span class="sxs-lookup"><span data-stu-id="6fb6b-104">PageFault\_TransitionFault class</span></span>

<span data-ttu-id="6fb6b-105">此類別是分頁錯誤事件的事件種類類別。</span><span class="sxs-lookup"><span data-stu-id="6fb6b-105">This class is the event type class for page fault events.</span></span>

<span data-ttu-id="6fb6b-106">以下是從 MOF 程式碼簡化的語法。</span><span class="sxs-lookup"><span data-stu-id="6fb6b-106">The following syntax is simplified from MOF code.</span></span>

## <a name="syntax"></a><span data-ttu-id="6fb6b-107">語法</span><span class="sxs-lookup"><span data-stu-id="6fb6b-107">Syntax</span></span>

``` syntax
[EventType{10, 11, 12, 13, 14}, EventTypeName{"TransitionFault", "DemandZeroFault", "CopyOnWrite", "GuardPageFault", "HardPageFault"}]
class PageFault_TransitionFault : PageFault_V2
{
  uint32 VirtualAddress;
  uint32 ProgramCounter;
};
```

## <a name="members"></a><span data-ttu-id="6fb6b-108">成員</span><span class="sxs-lookup"><span data-stu-id="6fb6b-108">Members</span></span>

<span data-ttu-id="6fb6b-109">**PageFault \_ TransitionFault** 類別具有下列類型的成員：</span><span class="sxs-lookup"><span data-stu-id="6fb6b-109">The **PageFault\_TransitionFault** class has these types of members:</span></span>

-   [<span data-ttu-id="6fb6b-110">屬性</span><span class="sxs-lookup"><span data-stu-id="6fb6b-110">Properties</span></span>](#properties)

### <a name="properties"></a><span data-ttu-id="6fb6b-111">屬性</span><span class="sxs-lookup"><span data-stu-id="6fb6b-111">Properties</span></span>

<span data-ttu-id="6fb6b-112">**PageFault \_ TransitionFault** 類別具有這些屬性。</span><span class="sxs-lookup"><span data-stu-id="6fb6b-112">The **PageFault\_TransitionFault** class has these properties.</span></span>

<dl> <dt>

<span data-ttu-id="6fb6b-113">ProgramCounter</span><span class="sxs-lookup"><span data-stu-id="6fb6b-113">ProgramCounter</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="6fb6b-114">資料類型： **uint32**</span><span class="sxs-lookup"><span data-stu-id="6fb6b-114">Data type: **uint32**</span></span>
</dt> <dt>

<span data-ttu-id="6fb6b-115">存取類型：唯讀</span><span class="sxs-lookup"><span data-stu-id="6fb6b-115">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="6fb6b-116">限定詞： WmiDataId (2) ，指標</span><span class="sxs-lookup"><span data-stu-id="6fb6b-116">Qualifiers: WmiDataId(2), Pointer</span></span>
</dt> </dl>

<span data-ttu-id="6fb6b-117">正在執行的目前指令指標。</span><span class="sxs-lookup"><span data-stu-id="6fb6b-117">Pointer to the current instruction being executed.</span></span>

</dd> <dt>

<span data-ttu-id="6fb6b-118">VirtualAddress</span><span class="sxs-lookup"><span data-stu-id="6fb6b-118">VirtualAddress</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="6fb6b-119">資料類型： **uint32**</span><span class="sxs-lookup"><span data-stu-id="6fb6b-119">Data type: **uint32**</span></span>
</dt> <dt>

<span data-ttu-id="6fb6b-120">存取類型：唯讀</span><span class="sxs-lookup"><span data-stu-id="6fb6b-120">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="6fb6b-121">限定詞： WmiDataId (1) ，指標</span><span class="sxs-lookup"><span data-stu-id="6fb6b-121">Qualifiers: WmiDataId(1), Pointer</span></span>
</dt> </dl>

<span data-ttu-id="6fb6b-122">造成分頁錯誤之頁面的虛擬位址。</span><span class="sxs-lookup"><span data-stu-id="6fb6b-122">Virtual address of the page that caused the page fault.</span></span>

</dd> </dl>

## <a name="requirements"></a><span data-ttu-id="6fb6b-123">規格需求</span><span class="sxs-lookup"><span data-stu-id="6fb6b-123">Requirements</span></span>



| <span data-ttu-id="6fb6b-124">需求</span><span class="sxs-lookup"><span data-stu-id="6fb6b-124">Requirement</span></span> | <span data-ttu-id="6fb6b-125">值</span><span class="sxs-lookup"><span data-stu-id="6fb6b-125">Value</span></span> |
|-------------------------------------|------------------------------------------------------------|
| <span data-ttu-id="6fb6b-126">最低支援的用戶端</span><span class="sxs-lookup"><span data-stu-id="6fb6b-126">Minimum supported client</span></span><br/> | <span data-ttu-id="6fb6b-127">Windows 2000 Professional \[僅限傳統型應用程式\]</span><span class="sxs-lookup"><span data-stu-id="6fb6b-127">Windows 2000 Professional \[desktop apps only\]</span></span><br/> |
| <span data-ttu-id="6fb6b-128">最低支援的伺服器</span><span class="sxs-lookup"><span data-stu-id="6fb6b-128">Minimum supported server</span></span><br/> | <span data-ttu-id="6fb6b-129">Windows 2000 Server \[僅限傳統型應用程式\]</span><span class="sxs-lookup"><span data-stu-id="6fb6b-129">Windows 2000 Server \[desktop apps only\]</span></span><br/>       |



## <a name="see-also"></a><span data-ttu-id="6fb6b-130">另請參閱</span><span class="sxs-lookup"><span data-stu-id="6fb6b-130">See also</span></span>

<dl> <dt>

[<span data-ttu-id="6fb6b-131">**PageFault \_ V2**</span><span class="sxs-lookup"><span data-stu-id="6fb6b-131">**PageFault\_V2**</span></span>](pagefault-v2.md)
</dt> </dl>

 

 




