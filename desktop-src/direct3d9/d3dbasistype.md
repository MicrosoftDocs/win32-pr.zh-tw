---
description: 定義高序位修補程式介面的基礎類型。
ms.assetid: 18c31c77-7ba3-449c-af4a-717b8c1dced1
title: 'D3DBASISTYPE 列舉 (D3D9Types) '
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- D3DBASISTYPE
api_type:
- HeaderDef
api_location:
- D3D9Types.h
ms.openlocfilehash: 7e166f56aa2625c868d3e2e2223efbb577e05bf5
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 03/15/2021
ms.locfileid: "104116189"
---
# <a name="d3dbasistype-enumeration"></a><span data-ttu-id="94f9f-103">D3DBASISTYPE 列舉</span><span class="sxs-lookup"><span data-stu-id="94f9f-103">D3DBASISTYPE enumeration</span></span>

<span data-ttu-id="94f9f-104">定義高序位修補程式介面的基礎類型。</span><span class="sxs-lookup"><span data-stu-id="94f9f-104">Defines the basis type of a high-order patch surface.</span></span>

## <a name="syntax"></a><span data-ttu-id="94f9f-105">Syntax</span><span class="sxs-lookup"><span data-stu-id="94f9f-105">Syntax</span></span>


```C++
typedef enum D3DBASISTYPE { 
  D3DBASIS_BEZIER       = 0,
  D3DBASIS_BSPLINE      = 1,
  D3DBASIS_CATMULL_ROM  = 2,
  D3DBASIS_FORCE_DWORD  = 0x7fffffff
} D3DBASISTYPE, *LPD3DBASISTYPE;
```



## <a name="constants"></a><span data-ttu-id="94f9f-106">常數</span><span class="sxs-lookup"><span data-stu-id="94f9f-106">Constants</span></span>

<dl> <dt>

<span data-ttu-id="94f9f-107"><span id="D3DBASIS_BEZIER"></span><span id="d3dbasis_bezier"></span>**D3DBASIS \_ 貝塞爾**</span><span class="sxs-lookup"><span data-stu-id="94f9f-107"><span id="D3DBASIS_BEZIER"></span><span id="d3dbasis_bezier"></span>**D3DBASIS\_BEZIER**</span></span>
</dt> <dd>

<span data-ttu-id="94f9f-108">輸入頂點會被視為一連串的貝塞爾修補程式。</span><span class="sxs-lookup"><span data-stu-id="94f9f-108">Input vertices are treated as a series of Bézier patches.</span></span> <span data-ttu-id="94f9f-109">指定的頂點數目必須可被4整除。</span><span class="sxs-lookup"><span data-stu-id="94f9f-109">The number of vertices specified must be divisible by 4.</span></span> <span data-ttu-id="94f9f-110">這項準則以外的網格部分將不會呈現。</span><span class="sxs-lookup"><span data-stu-id="94f9f-110">Portions of the mesh beyond this criterion will not be rendered.</span></span> <span data-ttu-id="94f9f-111">在每次呼叫所轉譯之介面內部的子修補程式之間，會採用完整的持續性。</span><span class="sxs-lookup"><span data-stu-id="94f9f-111">Full continuity is assumed between sub-patches in the interior of the surface rendered by each call.</span></span> <span data-ttu-id="94f9f-112">只保證每個子修補角落角落的頂點都位於產生的介面上。</span><span class="sxs-lookup"><span data-stu-id="94f9f-112">Only the vertices at the corners of each sub-patch are guaranteed to lie on the resulting surface.</span></span>

</dd> <dt>

<span data-ttu-id="94f9f-113"><span id="D3DBASIS_BSPLINE"></span><span id="d3dbasis_bspline"></span>**D3DBASIS \_ BSPLINE**</span><span class="sxs-lookup"><span data-stu-id="94f9f-113"><span id="D3DBASIS_BSPLINE"></span><span id="d3dbasis_bspline"></span>**D3DBASIS\_BSPLINE**</span></span>
</dt> <dd>

<span data-ttu-id="94f9f-114">輸入頂點會被視為 B 曲線介面的控制點。</span><span class="sxs-lookup"><span data-stu-id="94f9f-114">Input vertices are treated as control points of a B-spline surface.</span></span> <span data-ttu-id="94f9f-115">轉譯的 apertures 數目會比該方向的 apertures 數少兩倍。</span><span class="sxs-lookup"><span data-stu-id="94f9f-115">The number of apertures rendered is two fewer than the number of apertures in that direction.</span></span> <span data-ttu-id="94f9f-116">一般情況下，產生的介面不包含指定的控制項頂點。</span><span class="sxs-lookup"><span data-stu-id="94f9f-116">In general, the generated surface does not contain the control vertices specified.</span></span>

</dd> <dt>

<span data-ttu-id="94f9f-117"><span id="D3DBASIS_CATMULL_ROM"></span><span id="d3dbasis_catmull_rom"></span>**D3DBASIS \_ CATMULL \_ ROM**</span><span class="sxs-lookup"><span data-stu-id="94f9f-117"><span id="D3DBASIS_CATMULL_ROM"></span><span id="d3dbasis_catmull_rom"></span>**D3DBASIS\_CATMULL\_ROM**</span></span>
</dt> <dd>

<span data-ttu-id="94f9f-118">插插值基礎會定義介面，讓介面能通過指定的所有輸入頂點。</span><span class="sxs-lookup"><span data-stu-id="94f9f-118">An interpolating basis defines the surface so that the surface goes through all the input vertices specified.</span></span> <span data-ttu-id="94f9f-119">在 DirectX 8 中，這是 D3DBASIS 的 \_ 插補。</span><span class="sxs-lookup"><span data-stu-id="94f9f-119">In DirectX 8, this was D3DBASIS\_INTERPOLATE.</span></span>

</dd> <dt>

<span data-ttu-id="94f9f-120"><span id="D3DBASIS_FORCE_DWORD"></span><span id="d3dbasis_force_dword"></span>**D3DBASIS \_ 強制 \_ DWORD**</span><span class="sxs-lookup"><span data-stu-id="94f9f-120"><span id="D3DBASIS_FORCE_DWORD"></span><span id="d3dbasis_force_dword"></span>**D3DBASIS\_FORCE\_DWORD**</span></span>
</dt> <dd>

<span data-ttu-id="94f9f-121">強制此列舉的大小編譯為32位。</span><span class="sxs-lookup"><span data-stu-id="94f9f-121">Forces this enumeration to compile to 32 bits in size.</span></span> <span data-ttu-id="94f9f-122">如果沒有這個值，某些編譯器會允許此列舉編譯成32位以外的大小。</span><span class="sxs-lookup"><span data-stu-id="94f9f-122">Without this value, some compilers would allow this enumeration to compile to a size other than 32 bits.</span></span> <span data-ttu-id="94f9f-123">不使用這個值。</span><span class="sxs-lookup"><span data-stu-id="94f9f-123">This value is not used.</span></span>

</dd> </dl>

## <a name="remarks"></a><span data-ttu-id="94f9f-124">備註</span><span class="sxs-lookup"><span data-stu-id="94f9f-124">Remarks</span></span>

<span data-ttu-id="94f9f-125">**D3DBASISTYPE** 的成員會指定在鑲嵌期間用來評估高序位修補程式介面基本的形式。</span><span class="sxs-lookup"><span data-stu-id="94f9f-125">The members of **D3DBASISTYPE** specify the formulation to be used in evaluating the high-order patch surface primitive during tessellation.</span></span>

## <a name="requirements"></a><span data-ttu-id="94f9f-126">規格需求</span><span class="sxs-lookup"><span data-stu-id="94f9f-126">Requirements</span></span>



| <span data-ttu-id="94f9f-127">需求</span><span class="sxs-lookup"><span data-stu-id="94f9f-127">Requirement</span></span> | <span data-ttu-id="94f9f-128">值</span><span class="sxs-lookup"><span data-stu-id="94f9f-128">Value</span></span> |
|-------------------|----------------------------------------------------------------------------------------|
| <span data-ttu-id="94f9f-129">標頭</span><span class="sxs-lookup"><span data-stu-id="94f9f-129">Header</span></span><br/> | <dl> <span data-ttu-id="94f9f-130"><dt>D3D9Types。h</dt></span><span class="sxs-lookup"><span data-stu-id="94f9f-130"><dt>D3D9Types.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="94f9f-131">另請參閱</span><span class="sxs-lookup"><span data-stu-id="94f9f-131">See also</span></span>

<dl> <dt>

[<span data-ttu-id="94f9f-132">Direct3D 列舉</span><span class="sxs-lookup"><span data-stu-id="94f9f-132">Direct3D Enumerations</span></span>](dx9-graphics-reference-d3d-enums.md)
</dt> <dt>

[<span data-ttu-id="94f9f-133">**D3DRECTPATCH \_ 資訊**</span><span class="sxs-lookup"><span data-stu-id="94f9f-133">**D3DRECTPATCH\_INFO**</span></span>](d3drectpatch-info.md)
</dt> <dt>

[<span data-ttu-id="94f9f-134">**D3DTRIPATCH \_ 資訊**</span><span class="sxs-lookup"><span data-stu-id="94f9f-134">**D3DTRIPATCH\_INFO**</span></span>](d3dtripatch-info.md)
</dt> </dl>

 

 




