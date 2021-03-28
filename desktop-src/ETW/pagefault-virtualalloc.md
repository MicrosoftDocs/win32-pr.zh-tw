---
description: 這個類別是虛擬配置事件的事件種類類別。 以下是從 MOF 程式碼簡化的語法。
ms.assetid: 037d33e0-da94-4834-bc02-814c1cae1d8d
title: PageFault_VirtualAlloc 類別
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- PageFault_VirtualAlloc
- PageFault_VirtualAlloc.BaseAddress
- PageFault_VirtualAlloc.RegionSize
- PageFault_VirtualAlloc.ProcessId
- PageFault_VirtualAlloc.Flags
api_type:
- NA
api_location: ''
ms.openlocfilehash: f9e754bc3dc09f492682d5a522a6489cfde27ceb
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/07/2021
ms.locfileid: "104318576"
---
# <a name="pagefault_virtualalloc-class"></a><span data-ttu-id="1f093-104">PageFault \_ VirtualAlloc 類別</span><span class="sxs-lookup"><span data-stu-id="1f093-104">PageFault\_VirtualAlloc class</span></span>

<span data-ttu-id="1f093-105">這個類別是虛擬配置事件的事件種類類別。</span><span class="sxs-lookup"><span data-stu-id="1f093-105">This class is the event type class for virtual allocation events.</span></span>

<span data-ttu-id="1f093-106">以下是從 MOF 程式碼簡化的語法。</span><span class="sxs-lookup"><span data-stu-id="1f093-106">The following syntax is simplified from MOF code.</span></span>

## <a name="syntax"></a><span data-ttu-id="1f093-107">語法</span><span class="sxs-lookup"><span data-stu-id="1f093-107">Syntax</span></span>

``` syntax
[EventType{98, 99}, EventTypeName{"VirtualAlloc", "VirtualFree"}]
class PageFault_VirtualAlloc : PageFault_V2
{
  uint32 BaseAddress;
  object RegionSize;
  uint32 ProcessId;
  uint32 Flags;
};
```

## <a name="members"></a><span data-ttu-id="1f093-108">成員</span><span class="sxs-lookup"><span data-stu-id="1f093-108">Members</span></span>

<span data-ttu-id="1f093-109">**PageFault \_ VirtualAlloc** 類別具有下列類型的成員：</span><span class="sxs-lookup"><span data-stu-id="1f093-109">The **PageFault\_VirtualAlloc** class has these types of members:</span></span>

-   [<span data-ttu-id="1f093-110">屬性</span><span class="sxs-lookup"><span data-stu-id="1f093-110">Properties</span></span>](#properties)

### <a name="properties"></a><span data-ttu-id="1f093-111">屬性</span><span class="sxs-lookup"><span data-stu-id="1f093-111">Properties</span></span>

<span data-ttu-id="1f093-112">**PageFault \_ VirtualAlloc** 類別具有這些屬性。</span><span class="sxs-lookup"><span data-stu-id="1f093-112">The **PageFault\_VirtualAlloc** class has these properties.</span></span>

<dl> <dt>

<span data-ttu-id="1f093-113">**BaseAddress**</span><span class="sxs-lookup"><span data-stu-id="1f093-113">**BaseAddress**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="1f093-114">資料類型： **uint32**</span><span class="sxs-lookup"><span data-stu-id="1f093-114">Data type: **uint32**</span></span>
</dt> <dt>

<span data-ttu-id="1f093-115">存取類型：唯讀</span><span class="sxs-lookup"><span data-stu-id="1f093-115">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="1f093-116">限定詞： WmiDataId (1) ，指標</span><span class="sxs-lookup"><span data-stu-id="1f093-116">Qualifiers: WmiDataId(1), Pointer</span></span>
</dt> </dl>

<span data-ttu-id="1f093-117">配置或釋放記憶體的起始位址。</span><span class="sxs-lookup"><span data-stu-id="1f093-117">The starting address at which memory was allocated or freed.</span></span>

</dd> <dt>

<span data-ttu-id="1f093-118">**旗標**</span><span class="sxs-lookup"><span data-stu-id="1f093-118">**Flags**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="1f093-119">資料類型： **uint32**</span><span class="sxs-lookup"><span data-stu-id="1f093-119">Data type: **uint32**</span></span>
</dt> <dt>

<span data-ttu-id="1f093-120">存取類型：唯讀</span><span class="sxs-lookup"><span data-stu-id="1f093-120">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="1f093-121">限定詞： WmiDataId (4) ，格式 ( "x" ) </span><span class="sxs-lookup"><span data-stu-id="1f093-121">Qualifiers: WmiDataId(4), Format("x")</span></span>
</dt> </dl>

<span data-ttu-id="1f093-122">已執行之記憶體配置的類型。</span><span class="sxs-lookup"><span data-stu-id="1f093-122">The type of memory allocation that was performed.</span></span> <span data-ttu-id="1f093-123">如需可能的值，請參閱 [**VirtualAllocEx**](/windows/win32/api/memoryapi/nf-memoryapi-virtualallocex)函數的 *flAllocationType* 參數。</span><span class="sxs-lookup"><span data-stu-id="1f093-123">For possible values, see the *flAllocationType* parameter of the [**VirtualAllocEx**](/windows/win32/api/memoryapi/nf-memoryapi-virtualallocex) function.</span></span>

</dd> <dt>

<span data-ttu-id="1f093-124">**進程**</span><span class="sxs-lookup"><span data-stu-id="1f093-124">**ProcessId**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="1f093-125">資料類型： **uint32**</span><span class="sxs-lookup"><span data-stu-id="1f093-125">Data type: **uint32**</span></span>
</dt> <dt>

<span data-ttu-id="1f093-126">存取類型：唯讀</span><span class="sxs-lookup"><span data-stu-id="1f093-126">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="1f093-127">限定詞： WmiDataId (3) </span><span class="sxs-lookup"><span data-stu-id="1f093-127">Qualifiers: WmiDataId(3)</span></span>
</dt> </dl>

<span data-ttu-id="1f093-128">擁有記憶體 (的進程可能與執行配置) 的執行緒不同。</span><span class="sxs-lookup"><span data-stu-id="1f093-128">The process that owned the memory (can be different from the thread that performed the allocation).</span></span>

</dd> <dt>

<span data-ttu-id="1f093-129">**RegionSize**</span><span class="sxs-lookup"><span data-stu-id="1f093-129">**RegionSize**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="1f093-130">資料類型： **物件**</span><span class="sxs-lookup"><span data-stu-id="1f093-130">Data type: **object**</span></span>
</dt> <dt>

<span data-ttu-id="1f093-131">存取類型：唯讀</span><span class="sxs-lookup"><span data-stu-id="1f093-131">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="1f093-132">限定詞： WmiDataId (2) ，副檔名 ( "SizeT" ) </span><span class="sxs-lookup"><span data-stu-id="1f093-132">Qualifiers: WmiDataId(2), Extension("SizeT")</span></span>
</dt> </dl>

<span data-ttu-id="1f093-133">已配置或釋放之記憶體的大小（以位元組為單位）。</span><span class="sxs-lookup"><span data-stu-id="1f093-133">The size, in bytes, of the memory that was allocated or freed.</span></span>

</dd> </dl>

## <a name="requirements"></a><span data-ttu-id="1f093-134">規格需求</span><span class="sxs-lookup"><span data-stu-id="1f093-134">Requirements</span></span>



| <span data-ttu-id="1f093-135">需求</span><span class="sxs-lookup"><span data-stu-id="1f093-135">Requirement</span></span> | <span data-ttu-id="1f093-136">值</span><span class="sxs-lookup"><span data-stu-id="1f093-136">Value</span></span> |
|-------------------------------------|---------------------------------------------------------|
| <span data-ttu-id="1f093-137">最低支援的用戶端</span><span class="sxs-lookup"><span data-stu-id="1f093-137">Minimum supported client</span></span><br/> | <span data-ttu-id="1f093-138">\[僅限 Windows 7 桌面應用程式\]</span><span class="sxs-lookup"><span data-stu-id="1f093-138">Windows 7 \[desktop apps only\]</span></span><br/>              |
| <span data-ttu-id="1f093-139">最低支援的伺服器</span><span class="sxs-lookup"><span data-stu-id="1f093-139">Minimum supported server</span></span><br/> | <span data-ttu-id="1f093-140">僅限 Windows Server 2008 R2 \[ desktop 應用程式\]</span><span class="sxs-lookup"><span data-stu-id="1f093-140">Windows Server 2008 R2 \[desktop apps only\]</span></span><br/> |



## <a name="see-also"></a><span data-ttu-id="1f093-141">另請參閱</span><span class="sxs-lookup"><span data-stu-id="1f093-141">See also</span></span>

<dl> <dt>

[<span data-ttu-id="1f093-142">**PageFault \_ V2**</span><span class="sxs-lookup"><span data-stu-id="1f093-142">**PageFault\_V2**</span></span>](pagefault-v2.md)
</dt> </dl>

 

 
