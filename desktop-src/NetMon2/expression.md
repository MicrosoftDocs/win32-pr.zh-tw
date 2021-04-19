---
description: 包含評估為對等的 ANDEXP 陣列群組。
ms.assetid: 14fa568c-9535-4415-923d-7e93ba4d2e80
title: " (Netmon. h) 的運算式結構"
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- EXPRESSION
api_type:
- HeaderDef
api_location:
- Netmon.h
ms.openlocfilehash: b6565c294c0d8e0a7a277769404cb8b1b206380e
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/07/2021
ms.locfileid: "106971173"
---
# <a name="expression-structure"></a><span data-ttu-id="901ff-103">運算式結構</span><span class="sxs-lookup"><span data-stu-id="901ff-103">EXPRESSION structure</span></span>

<span data-ttu-id="901ff-104">**運算式** 結構包含 **ANDEXP** 陣列的群組，其會評估為邏輯 AND 運算式中的對等，其格式為</span><span class="sxs-lookup"><span data-stu-id="901ff-104">The **EXPRESSION** structure contains a group of **ANDEXP** arrays evaluated as peers in logical AND expressions, which have the format</span></span>

<span data-ttu-id="901ff-105"> (ANDEXP 1 && ANDEXP 2 && ANDEXP 3) 。</span><span class="sxs-lookup"><span data-stu-id="901ff-105">(ANDEXP 1 && ANDEXP 2 && ANDEXP 3).</span></span>

## <a name="syntax"></a><span data-ttu-id="901ff-106">語法</span><span class="sxs-lookup"><span data-stu-id="901ff-106">Syntax</span></span>


```C++
typedef struct _EXPRESSION {
  DWORD  nAndExps;
  ANDEXP AndExp[MAX_PATTERNS];
} EXPRESSION, *LPEXPRESSION;
```



## <a name="members"></a><span data-ttu-id="901ff-107">成員</span><span class="sxs-lookup"><span data-stu-id="901ff-107">Members</span></span>

<dl> <dt>

<span data-ttu-id="901ff-108">**nAndExps**</span><span class="sxs-lookup"><span data-stu-id="901ff-108">**nAndExps**</span></span>
</dt> <dd>

<span data-ttu-id="901ff-109">**ANDEXP** 模式的數目。</span><span class="sxs-lookup"><span data-stu-id="901ff-109">Number of **ANDEXP** patterns.</span></span>

</dd> <dt>

<span data-ttu-id="901ff-110">**AndExp**</span><span class="sxs-lookup"><span data-stu-id="901ff-110">**AndExp**</span></span>
</dt> <dd>

<span data-ttu-id="901ff-111">**ANDEXP** 模式的陣列。</span><span class="sxs-lookup"><span data-stu-id="901ff-111">Array of **ANDEXP** patterns.</span></span> <span data-ttu-id="901ff-112">Capture 篩選器會將這個陣列的所有資料列都排列成邏輯和語句。</span><span class="sxs-lookup"><span data-stu-id="901ff-112">The capture filter arranges all rows of this array as logical AND statements.</span></span> <span data-ttu-id="901ff-113">請注意，每個運算式結構最多可包含四個 **ANDEXP** 模式。</span><span class="sxs-lookup"><span data-stu-id="901ff-113">Be aware that each EXPRESSION structure can contain a maximum of four **ANDEXP** patterns.</span></span>

</dd> </dl>

## <a name="remarks"></a><span data-ttu-id="901ff-114">備註</span><span class="sxs-lookup"><span data-stu-id="901ff-114">Remarks</span></span>

<span data-ttu-id="901ff-115">如需將此結構實作為 capture 篩選器一部分的詳細資訊，請參閱「 [捕獲篩選](capture-filters.md)條件」。</span><span class="sxs-lookup"><span data-stu-id="901ff-115">For more information about implementing this structure as part of a capture filter, see [Capture Filters](capture-filters.md).</span></span>

## <a name="requirements"></a><span data-ttu-id="901ff-116">規格需求</span><span class="sxs-lookup"><span data-stu-id="901ff-116">Requirements</span></span>



| <span data-ttu-id="901ff-117">需求</span><span class="sxs-lookup"><span data-stu-id="901ff-117">Requirement</span></span> | <span data-ttu-id="901ff-118">值</span><span class="sxs-lookup"><span data-stu-id="901ff-118">Value</span></span> |
|-------------------------------------|-------------------------------------------------------------------------------------|
| <span data-ttu-id="901ff-119">最低支援的用戶端</span><span class="sxs-lookup"><span data-stu-id="901ff-119">Minimum supported client</span></span><br/> | <span data-ttu-id="901ff-120">Windows 2000 Professional \[僅限傳統型應用程式\]</span><span class="sxs-lookup"><span data-stu-id="901ff-120">Windows 2000 Professional \[desktop apps only\]</span></span><br/>                          |
| <span data-ttu-id="901ff-121">最低支援的伺服器</span><span class="sxs-lookup"><span data-stu-id="901ff-121">Minimum supported server</span></span><br/> | <span data-ttu-id="901ff-122">Windows 2000 Server \[僅限傳統型應用程式\]</span><span class="sxs-lookup"><span data-stu-id="901ff-122">Windows 2000 Server \[desktop apps only\]</span></span><br/>                                |
| <span data-ttu-id="901ff-123">標頭</span><span class="sxs-lookup"><span data-stu-id="901ff-123">Header</span></span><br/>                   | <dl> <span data-ttu-id="901ff-124"><dt>Netmon</dt></span><span class="sxs-lookup"><span data-stu-id="901ff-124"><dt>Netmon.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="901ff-125">另請參閱</span><span class="sxs-lookup"><span data-stu-id="901ff-125">See also</span></span>

<dl> <dt>

[<span data-ttu-id="901ff-126">ANDEXP</span><span class="sxs-lookup"><span data-stu-id="901ff-126">ANDEXP</span></span>](andexp.md)
</dt> <dt>

[<span data-ttu-id="901ff-127">CAPTUREFILTER</span><span class="sxs-lookup"><span data-stu-id="901ff-127">CAPTUREFILTER</span></span>](capturefilter.md)
</dt> </dl>

 

 




