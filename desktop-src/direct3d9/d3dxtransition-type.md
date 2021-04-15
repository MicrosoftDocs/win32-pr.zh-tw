---
description: 定義網格動畫值之間的轉換樣式。
ms.assetid: 4416ef28-ba6b-47ca-be7d-831daad619e5
title: 'D3DXTRANSITION_TYPE 列舉 (D3dx9anim .h) '
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- D3DXTRANSITION_TYPE
api_type:
- HeaderDef
api_location:
- d3dx9anim.h
ms.openlocfilehash: 0ca6ef7f9dcee8e865a1cd4089aecd1bc239d5d4
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 03/15/2021
ms.locfileid: "103946086"
---
# <a name="d3dxtransition_type-enumeration"></a><span data-ttu-id="ffed9-103">D3DXTRANSITION \_ 類型列舉</span><span class="sxs-lookup"><span data-stu-id="ffed9-103">D3DXTRANSITION\_TYPE enumeration</span></span>

<span data-ttu-id="ffed9-104">定義網格動畫值之間的轉換樣式。</span><span class="sxs-lookup"><span data-stu-id="ffed9-104">Defines the transition style between values of a mesh animation.</span></span>

## <a name="syntax"></a><span data-ttu-id="ffed9-105">Syntax</span><span class="sxs-lookup"><span data-stu-id="ffed9-105">Syntax</span></span>


```C++
typedef enum D3DXTRANSITION_TYPE { 
  D3DXTRANSITION_LINEAR         = 0x000,
  D3DXTRANSITION_EASEINEASEOUT  = 0x001,
  D3DXTRANSITION_FORCE_DWORD    = 0x7fffffff
} D3DXTRANSITION_TYPE, *LPD3DXTRANSITION_TYPE;
```



## <a name="constants"></a><span data-ttu-id="ffed9-106">常數</span><span class="sxs-lookup"><span data-stu-id="ffed9-106">Constants</span></span>

<dl> <dt>

<span data-ttu-id="ffed9-107"><span id="D3DXTRANSITION_LINEAR"></span><span id="d3dxtransition_linear"></span>**D3DXTRANSITION \_ 線性**</span><span class="sxs-lookup"><span data-stu-id="ffed9-107"><span id="D3DXTRANSITION_LINEAR"></span><span id="d3dxtransition_linear"></span>**D3DXTRANSITION\_LINEAR**</span></span>
</dt> <dd>

<span data-ttu-id="ffed9-108">值之間的線性轉換。</span><span class="sxs-lookup"><span data-stu-id="ffed9-108">Linear transition between values.</span></span>

</dd> <dt>

<span data-ttu-id="ffed9-109"><span id="D3DXTRANSITION_EASEINEASEOUT"></span><span id="d3dxtransition_easeineaseout"></span>**D3DXTRANSITION \_ EASEINEASEOUT**</span><span class="sxs-lookup"><span data-stu-id="ffed9-109"><span id="D3DXTRANSITION_EASEINEASEOUT"></span><span id="d3dxtransition_easeineaseout"></span>**D3DXTRANSITION\_EASEINEASEOUT**</span></span>
</dt> <dd>

<span data-ttu-id="ffed9-110">在值之間進行輕鬆、容易放大的曲線轉換。</span><span class="sxs-lookup"><span data-stu-id="ffed9-110">Ease-in, ease-out spline transition between values.</span></span>

</dd> <dt>

<span data-ttu-id="ffed9-111"><span id="D3DXTRANSITION_FORCE_DWORD"></span><span id="d3dxtransition_force_dword"></span>**D3DXTRANSITION \_ 強制 \_ DWORD**</span><span class="sxs-lookup"><span data-stu-id="ffed9-111"><span id="D3DXTRANSITION_FORCE_DWORD"></span><span id="d3dxtransition_force_dword"></span>**D3DXTRANSITION\_FORCE\_DWORD**</span></span>
</dt> <dd>

<span data-ttu-id="ffed9-112">強制此列舉的大小編譯為32位。</span><span class="sxs-lookup"><span data-stu-id="ffed9-112">Forces this enumeration to compile to 32 bits in size.</span></span> <span data-ttu-id="ffed9-113">如果沒有這個值，某些編譯器會允許此列舉編譯成32位以外的大小。</span><span class="sxs-lookup"><span data-stu-id="ffed9-113">Without this value, some compilers would allow this enumeration to compile to a size other than 32 bits.</span></span> <span data-ttu-id="ffed9-114">不使用這個值。</span><span class="sxs-lookup"><span data-stu-id="ffed9-114">This value is not used.</span></span>

</dd> </dl>

## <a name="remarks"></a><span data-ttu-id="ffed9-115">備註</span><span class="sxs-lookup"><span data-stu-id="ffed9-115">Remarks</span></span>

<span data-ttu-id="ffed9-116">從輕鬆放大到簡化的遞增計算方式如下所示：</span><span class="sxs-lookup"><span data-stu-id="ffed9-116">The calculation for the ramp from ease in to ease out is calculated as follows:</span></span>

<dl> <span data-ttu-id="ffed9-117">Q (t) = 2 (x-y) t ³ + 3 (y-x) t ² + x</span><span class="sxs-lookup"><span data-stu-id="ffed9-117">Q(t) = 2(x - y)t³ + 3(y - x)t² + x</span></span>  
</dl>

<span data-ttu-id="ffed9-118">其中的斜坡是函數 Q (t) 具有下列屬性：</span><span class="sxs-lookup"><span data-stu-id="ffed9-118">where the ramp is a function Q(t) with the following properties:</span></span>

-   <span data-ttu-id="ffed9-119">Q (t) 是三個曲線。</span><span class="sxs-lookup"><span data-stu-id="ffed9-119">Q(t) is a cubic spline.</span></span>
-   <span data-ttu-id="ffed9-120">問 (t) 在 x 和 y 之間進行插補，作為 t 範圍從0到1。</span><span class="sxs-lookup"><span data-stu-id="ffed9-120">Q(t) interpolates between x and y as t ranges from 0 to 1.</span></span>
-   <span data-ttu-id="ffed9-121">Q (t) 是在 t = 0 和 t = 1 時水準。</span><span class="sxs-lookup"><span data-stu-id="ffed9-121">Q(t) is horizontal when t = 0 and t = 1.</span></span>

<span data-ttu-id="ffed9-122">這會以數學方式轉譯成：</span><span class="sxs-lookup"><span data-stu-id="ffed9-122">Mathematically, this translates into:</span></span>

<dl> <span data-ttu-id="ffed9-123">問 (t) = At ³ + Bt ² + Ct + D (因此，Q ' (t) = 3At ² + 2Bt + C) </span><span class="sxs-lookup"><span data-stu-id="ffed9-123">Q(t) = At³ + Bt² + Ct + D (and therefore, Q'(t) = 3At² + 2Bt + C)</span></span>  
<span data-ttu-id="ffed9-124">2a) Q (0) = x</span><span class="sxs-lookup"><span data-stu-id="ffed9-124">2a) Q(0) = x</span></span>  
<span data-ttu-id="ffed9-125">2b) Q (1) = y</span><span class="sxs-lookup"><span data-stu-id="ffed9-125">2b) Q(1) = y</span></span>  
<span data-ttu-id="ffed9-126">3a) Q ' (0) = 0</span><span class="sxs-lookup"><span data-stu-id="ffed9-126">3a) Q'(0) = 0</span></span>  
<span data-ttu-id="ffed9-127">3b) Q ' (1) = 0</span><span class="sxs-lookup"><span data-stu-id="ffed9-127">3b) Q'(1) = 0</span></span>  
</dl>

<span data-ttu-id="ffed9-128">解決 A、B、C、D：</span><span class="sxs-lookup"><span data-stu-id="ffed9-128">Solving for A, B, C, D:</span></span>

<dl> <span data-ttu-id="ffed9-129">D = x 從 2a)  (</span><span class="sxs-lookup"><span data-stu-id="ffed9-129">D = x (from 2a)</span></span>  
<span data-ttu-id="ffed9-130">從 3a) 的 C = 0 (</span><span class="sxs-lookup"><span data-stu-id="ffed9-130">C = 0 (from 3a)</span></span>  
<span data-ttu-id="ffed9-131">3A + 2B = 0 (自 3b) </span><span class="sxs-lookup"><span data-stu-id="ffed9-131">3A + 2B = 0 (from 3b)</span></span>  
<span data-ttu-id="ffed9-132">A + B = y x (從2b 和 D = x) </span><span class="sxs-lookup"><span data-stu-id="ffed9-132">A + B = y - x (from 2b and D = x)</span></span>  
</dl>

<span data-ttu-id="ffed9-133">因此：</span><span class="sxs-lookup"><span data-stu-id="ffed9-133">Therefore:</span></span>

<dl> <span data-ttu-id="ffed9-134">A = 2 (x-y) ，B = 3 (y-x) ，C = 0，D = x</span><span class="sxs-lookup"><span data-stu-id="ffed9-134">A = 2(x - y), B = 3(y - x), C = 0, D = x</span></span>  
</dl>

## <a name="requirements"></a><span data-ttu-id="ffed9-135">規格需求</span><span class="sxs-lookup"><span data-stu-id="ffed9-135">Requirements</span></span>



| <span data-ttu-id="ffed9-136">需求</span><span class="sxs-lookup"><span data-stu-id="ffed9-136">Requirement</span></span> | <span data-ttu-id="ffed9-137">值</span><span class="sxs-lookup"><span data-stu-id="ffed9-137">Value</span></span> |
|-------------------|----------------------------------------------------------------------------------------|
| <span data-ttu-id="ffed9-138">標頭</span><span class="sxs-lookup"><span data-stu-id="ffed9-138">Header</span></span><br/> | <dl> <span data-ttu-id="ffed9-139"><dt>D3dx9anim。h</dt></span><span class="sxs-lookup"><span data-stu-id="ffed9-139"><dt>D3dx9anim.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="ffed9-140">另請參閱</span><span class="sxs-lookup"><span data-stu-id="ffed9-140">See also</span></span>

<dl> <dt>

[<span data-ttu-id="ffed9-141">D3DX 列舉</span><span class="sxs-lookup"><span data-stu-id="ffed9-141">D3DX Enumerations</span></span>](dx9-graphics-reference-d3dx-enums.md)
</dt> </dl>

 

 




