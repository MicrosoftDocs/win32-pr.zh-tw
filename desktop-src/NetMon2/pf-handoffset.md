---
description: PF \_ HANDOFFSET 結構會定義交給剖析器的通訊協定，或剖析器所用的通訊協定。
ms.assetid: 2fda399d-a09e-47b4-bb2e-95996de9f950
title: 'PF_HANDOFFSET 結構 (Netmon) '
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- PF_HANDOFFSET
api_type:
- HeaderDef
api_location:
- Netmon.h
ms.openlocfilehash: 1b5dc9620f3b1860b27af973432aa4218c05b63b
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/08/2021
ms.locfileid: "106984970"
---
# <a name="pf_handoffset-structure"></a><span data-ttu-id="c0c7a-103">PF \_ HANDOFFSET 結構</span><span class="sxs-lookup"><span data-stu-id="c0c7a-103">PF\_HANDOFFSET structure</span></span>

<span data-ttu-id="c0c7a-104">**PF \_ HANDOFFSET** 結構會定義交給剖析器的通訊協定，或剖析器所用的通訊協定。</span><span class="sxs-lookup"><span data-stu-id="c0c7a-104">The **PF\_HANDOFFSET** structure defines the protocols that hand off to the parser, or the protocols that the parser hands off to.</span></span>

## <a name="syntax"></a><span data-ttu-id="c0c7a-105">語法</span><span class="sxs-lookup"><span data-stu-id="c0c7a-105">Syntax</span></span>


```C++
typedef struct _PF_HANDOFFSET {
  DWORD           nEntries;
  PF_HANDOFFENTRY Entry[];
} PF_HANDOFFSET, *PPF_HANDOFFSET;
```



## <a name="members"></a><span data-ttu-id="c0c7a-106">成員</span><span class="sxs-lookup"><span data-stu-id="c0c7a-106">Members</span></span>

<dl> <dt>

<span data-ttu-id="c0c7a-107">**nEntries**</span><span class="sxs-lookup"><span data-stu-id="c0c7a-107">**nEntries**</span></span>
</dt> <dd>

<span data-ttu-id="c0c7a-108">通訊協定數目。</span><span class="sxs-lookup"><span data-stu-id="c0c7a-108">Number of protocols.</span></span>

</dd> <dt>

<span data-ttu-id="c0c7a-109">**進入**</span><span class="sxs-lookup"><span data-stu-id="c0c7a-109">**Entry**</span></span>
</dt> <dd>

<span data-ttu-id="c0c7a-110">定義每個通訊協定的 [PF \_ HANDOFFENTRY](pf-handoffentry.md) 結構陣列。</span><span class="sxs-lookup"><span data-stu-id="c0c7a-110">An array of [PF\_HANDOFFENTRY](pf-handoffentry.md) structures that define each protocol.</span></span>

</dd> </dl>

## <a name="remarks"></a><span data-ttu-id="c0c7a-111">備註</span><span class="sxs-lookup"><span data-stu-id="c0c7a-111">Remarks</span></span>

<span data-ttu-id="c0c7a-112">[Pf \_ PARSERINFO](pf-parserinfo.md)結構會使用 **pf \_ HANDOFFSET** 結構來列出下列各項：</span><span class="sxs-lookup"><span data-stu-id="c0c7a-112">The [PF\_PARSERINFO](pf-parserinfo.md) structure uses the **PF\_HANDOFFSET** structure to list the following:</span></span>

-   <span data-ttu-id="c0c7a-113">哪些通訊協定會交給剖析器。</span><span class="sxs-lookup"><span data-stu-id="c0c7a-113">Which protocols hand off to the parser.</span></span>
-   <span data-ttu-id="c0c7a-114">剖析器所要關閉的通訊協定。</span><span class="sxs-lookup"><span data-stu-id="c0c7a-114">Which protocols the parser hands off to.</span></span>

<span data-ttu-id="c0c7a-115">您必須使用 **HeapAlloc** 來配置 **PF \_ HANDOFFSET** 結構。</span><span class="sxs-lookup"><span data-stu-id="c0c7a-115">The **PF\_HANDOFFSET** structure must be allocated using **HeapAlloc**.</span></span>

## <a name="requirements"></a><span data-ttu-id="c0c7a-116">規格需求</span><span class="sxs-lookup"><span data-stu-id="c0c7a-116">Requirements</span></span>



| <span data-ttu-id="c0c7a-117">需求</span><span class="sxs-lookup"><span data-stu-id="c0c7a-117">Requirement</span></span> | <span data-ttu-id="c0c7a-118">值</span><span class="sxs-lookup"><span data-stu-id="c0c7a-118">Value</span></span> |
|-------------------------------------|-------------------------------------------------------------------------------------|
| <span data-ttu-id="c0c7a-119">最低支援的用戶端</span><span class="sxs-lookup"><span data-stu-id="c0c7a-119">Minimum supported client</span></span><br/> | <span data-ttu-id="c0c7a-120">Windows 2000 Professional \[僅限傳統型應用程式\]</span><span class="sxs-lookup"><span data-stu-id="c0c7a-120">Windows 2000 Professional \[desktop apps only\]</span></span><br/>                          |
| <span data-ttu-id="c0c7a-121">最低支援的伺服器</span><span class="sxs-lookup"><span data-stu-id="c0c7a-121">Minimum supported server</span></span><br/> | <span data-ttu-id="c0c7a-122">Windows 2000 Server \[僅限傳統型應用程式\]</span><span class="sxs-lookup"><span data-stu-id="c0c7a-122">Windows 2000 Server \[desktop apps only\]</span></span><br/>                                |
| <span data-ttu-id="c0c7a-123">標頭</span><span class="sxs-lookup"><span data-stu-id="c0c7a-123">Header</span></span><br/>                   | <dl> <span data-ttu-id="c0c7a-124"><dt>Netmon</dt></span><span class="sxs-lookup"><span data-stu-id="c0c7a-124"><dt>Netmon.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="c0c7a-125">另請參閱</span><span class="sxs-lookup"><span data-stu-id="c0c7a-125">See also</span></span>

<dl> <dt>

[<span data-ttu-id="c0c7a-126">PF \_ PARSERINFO</span><span class="sxs-lookup"><span data-stu-id="c0c7a-126">PF\_PARSERINFO</span></span>](pf-parserinfo.md)
</dt> <dt>

[<span data-ttu-id="c0c7a-127">PF \_ HANDOFFENTRY</span><span class="sxs-lookup"><span data-stu-id="c0c7a-127">PF\_HANDOFFENTRY</span></span>](pf-handoffentry.md)
</dt> </dl>

 

 




