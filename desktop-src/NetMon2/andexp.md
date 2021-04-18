---
description: ANDEXP 結構包含用來評估框架資料的模式比對陣列。
ms.assetid: e5f4c030-eb2b-4cc9-9032-9ad4701b6503
title: 'ANDEXP 結構 (Netmon. h) '
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- ANDEXP
api_type:
- HeaderDef
api_location:
- Netmon.h
ms.openlocfilehash: 1d27d5bdd51a45b31f518271053f44b45917cdeb
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/08/2021
ms.locfileid: "104319711"
---
# <a name="andexp-structure"></a><span data-ttu-id="8d63d-103">ANDEXP 結構</span><span class="sxs-lookup"><span data-stu-id="8d63d-103">ANDEXP structure</span></span>

<span data-ttu-id="8d63d-104">**ANDEXP** 結構包含用來評估框架資料的模式比對陣列。</span><span class="sxs-lookup"><span data-stu-id="8d63d-104">The **ANDEXP** structure contains an array of pattern matches used to evaluate frame data.</span></span>

## <a name="syntax"></a><span data-ttu-id="8d63d-105">語法</span><span class="sxs-lookup"><span data-stu-id="8d63d-105">Syntax</span></span>


```C++
typedef struct _ANDEXP {
  DWORD        nPatternMatches;
  PATTERNMATCH PatternMatch[MAX_PATTERNS];
} ANDEXP, *LPANDEXP;
```



## <a name="members"></a><span data-ttu-id="8d63d-106">成員</span><span class="sxs-lookup"><span data-stu-id="8d63d-106">Members</span></span>

<dl> <dt>

<span data-ttu-id="8d63d-107">**nPatternMatches**</span><span class="sxs-lookup"><span data-stu-id="8d63d-107">**nPatternMatches**</span></span>
</dt> <dd>

<span data-ttu-id="8d63d-108">模式相符專案的數目。</span><span class="sxs-lookup"><span data-stu-id="8d63d-108">Number of pattern matches.</span></span>

</dd> <dt>

<span data-ttu-id="8d63d-109">**PatternMatch**</span><span class="sxs-lookup"><span data-stu-id="8d63d-109">**PatternMatch**</span></span>
</dt> <dd>

<span data-ttu-id="8d63d-110">模式比對元素的陣列。</span><span class="sxs-lookup"><span data-stu-id="8d63d-110">Array of pattern match elements.</span></span> <span data-ttu-id="8d63d-111">請注意，每個 **ANDEXP** 結構最多可包含四個模式 match 元素。</span><span class="sxs-lookup"><span data-stu-id="8d63d-111">Note that each **ANDEXP** structure can contain up to four pattern match elements.</span></span> <span data-ttu-id="8d63d-112">如需此成員的詳細資訊，請參閱「 [捕獲篩選準則](capture-filters.md)」。</span><span class="sxs-lookup"><span data-stu-id="8d63d-112">For more information about this member, see [Capture Filters](capture-filters.md).</span></span>

</dd> </dl>

## <a name="remarks"></a><span data-ttu-id="8d63d-113">備註</span><span class="sxs-lookup"><span data-stu-id="8d63d-113">Remarks</span></span>

<span data-ttu-id="8d63d-114">**PatternMatch** \[ MAX 模式陣列中的 \_ 模式 \] 會聯結為邏輯 OR 語句中的對等，格式為</span><span class="sxs-lookup"><span data-stu-id="8d63d-114">The patterns in the **PatternMatch**\[MAX\_PATTERNS\] array are joined as peers in logical OR statements in the format</span></span>

<span data-ttu-id="8d63d-115"> (模式 1 \| \| 模式2模式 \| \| 3) 。</span><span class="sxs-lookup"><span data-stu-id="8d63d-115">(Pattern 1 \|\| Pattern 2 \|\| Pattern 3).</span></span>

<span data-ttu-id="8d63d-116">如需有關如何執行此結構的詳細資訊，請參閱「 [捕獲篩選準則](capture-filters.md) 」。</span><span class="sxs-lookup"><span data-stu-id="8d63d-116">For more information about implementing this structure, see [Capture Filters](capture-filters.md) .</span></span>

## <a name="requirements"></a><span data-ttu-id="8d63d-117">規格需求</span><span class="sxs-lookup"><span data-stu-id="8d63d-117">Requirements</span></span>



| <span data-ttu-id="8d63d-118">需求</span><span class="sxs-lookup"><span data-stu-id="8d63d-118">Requirement</span></span> | <span data-ttu-id="8d63d-119">值</span><span class="sxs-lookup"><span data-stu-id="8d63d-119">Value</span></span> |
|-------------------------------------|-------------------------------------------------------------------------------------|
| <span data-ttu-id="8d63d-120">最低支援的用戶端</span><span class="sxs-lookup"><span data-stu-id="8d63d-120">Minimum supported client</span></span><br/> | <span data-ttu-id="8d63d-121">Windows 2000 Professional \[僅限傳統型應用程式\]</span><span class="sxs-lookup"><span data-stu-id="8d63d-121">Windows 2000 Professional \[desktop apps only\]</span></span><br/>                          |
| <span data-ttu-id="8d63d-122">最低支援的伺服器</span><span class="sxs-lookup"><span data-stu-id="8d63d-122">Minimum supported server</span></span><br/> | <span data-ttu-id="8d63d-123">Windows 2000 Server \[僅限傳統型應用程式\]</span><span class="sxs-lookup"><span data-stu-id="8d63d-123">Windows 2000 Server \[desktop apps only\]</span></span><br/>                                |
| <span data-ttu-id="8d63d-124">標頭</span><span class="sxs-lookup"><span data-stu-id="8d63d-124">Header</span></span><br/>                   | <dl> <span data-ttu-id="8d63d-125"><dt>Netmon</dt></span><span class="sxs-lookup"><span data-stu-id="8d63d-125"><dt>Netmon.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="8d63d-126">另請參閱</span><span class="sxs-lookup"><span data-stu-id="8d63d-126">See also</span></span>

<dl> <dt>

[<span data-ttu-id="8d63d-127">PATTERNMATCH</span><span class="sxs-lookup"><span data-stu-id="8d63d-127">PATTERNMATCH</span></span>](patternmatch.md)
</dt> </dl>

 

 




