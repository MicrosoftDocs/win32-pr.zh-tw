---
description: 定義 Direct3D 所支援的基本類型。
ms.assetid: 89e697f9-02b9-4ae1-9e86-6178da0cb008
title: 'D3DPRIMITIVETYPE 列舉 (D3D9Types) '
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- D3DPRIMITIVETYPE
api_type:
- HeaderDef
api_location:
- D3D9Types.h
ms.openlocfilehash: 933bbec72950bd2c73fda8b3781dd46393ca4c96
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 03/15/2021
ms.locfileid: "104116241"
---
# <a name="d3dprimitivetype-enumeration"></a><span data-ttu-id="9fcd4-103">D3DPRIMITIVETYPE 列舉</span><span class="sxs-lookup"><span data-stu-id="9fcd4-103">D3DPRIMITIVETYPE enumeration</span></span>

<span data-ttu-id="9fcd4-104">定義 Direct3D 所支援的基本類型。</span><span class="sxs-lookup"><span data-stu-id="9fcd4-104">Defines the primitives supported by Direct3D.</span></span>

## <a name="syntax"></a><span data-ttu-id="9fcd4-105">Syntax</span><span class="sxs-lookup"><span data-stu-id="9fcd4-105">Syntax</span></span>


```C++
typedef enum D3DPRIMITIVETYPE { 
  D3DPT_POINTLIST      = 1,
  D3DPT_LINELIST       = 2,
  D3DPT_LINESTRIP      = 3,
  D3DPT_TRIANGLELIST   = 4,
  D3DPT_TRIANGLESTRIP  = 5,
  D3DPT_TRIANGLEFAN    = 6,
  D3DPT_FORCE_DWORD    = 0x7fffffff
} D3DPRIMITIVETYPE, *LPD3DPRIMITIVETYPE;
```



## <a name="constants"></a><span data-ttu-id="9fcd4-106">常數</span><span class="sxs-lookup"><span data-stu-id="9fcd4-106">Constants</span></span>

<dl> <dt>

<span data-ttu-id="9fcd4-107"><span id="D3DPT_POINTLIST"></span><span id="d3dpt_pointlist"></span>**D3DPT \_ POINTLIST**</span><span class="sxs-lookup"><span data-stu-id="9fcd4-107"><span id="D3DPT_POINTLIST"></span><span id="d3dpt_pointlist"></span>**D3DPT\_POINTLIST**</span></span>
</dt> <dd>

<span data-ttu-id="9fcd4-108">將頂點轉譯為隔離點的集合。</span><span class="sxs-lookup"><span data-stu-id="9fcd4-108">Renders the vertices as a collection of isolated points.</span></span> <span data-ttu-id="9fcd4-109">索引的基本專案不支援此值。</span><span class="sxs-lookup"><span data-stu-id="9fcd4-109">This value is unsupported for indexed primitives.</span></span>

</dd> <dt>

<span data-ttu-id="9fcd4-110"><span id="D3DPT_LINELIST"></span><span id="d3dpt_linelist"></span>**D3DPT \_ LINELIST**</span><span class="sxs-lookup"><span data-stu-id="9fcd4-110"><span id="D3DPT_LINELIST"></span><span id="d3dpt_linelist"></span>**D3DPT\_LINELIST**</span></span>
</dt> <dd>

<span data-ttu-id="9fcd4-111">將頂點轉譯為獨立直線線段的清單。</span><span class="sxs-lookup"><span data-stu-id="9fcd4-111">Renders the vertices as a list of isolated straight line segments.</span></span>

</dd> <dt>

<span data-ttu-id="9fcd4-112"><span id="D3DPT_LINESTRIP"></span><span id="d3dpt_linestrip"></span>**D3DPT \_ LINESTRIP**</span><span class="sxs-lookup"><span data-stu-id="9fcd4-112"><span id="D3DPT_LINESTRIP"></span><span id="d3dpt_linestrip"></span>**D3DPT\_LINESTRIP**</span></span>
</dt> <dd>

<span data-ttu-id="9fcd4-113">將頂點轉譯為單一折線。</span><span class="sxs-lookup"><span data-stu-id="9fcd4-113">Renders the vertices as a single polyline.</span></span>

</dd> <dt>

<span data-ttu-id="9fcd4-114"><span id="D3DPT_TRIANGLELIST"></span><span id="d3dpt_trianglelist"></span>**D3DPT \_ TRIANGLELIST**</span><span class="sxs-lookup"><span data-stu-id="9fcd4-114"><span id="D3DPT_TRIANGLELIST"></span><span id="d3dpt_trianglelist"></span>**D3DPT\_TRIANGLELIST**</span></span>
</dt> <dd>

<span data-ttu-id="9fcd4-115">將指定的頂點轉譯為一系列的隔離三角形。</span><span class="sxs-lookup"><span data-stu-id="9fcd4-115">Renders the specified vertices as a sequence of isolated triangles.</span></span> <span data-ttu-id="9fcd4-116">三個頂點的每個群組都會定義個別的三角形。</span><span class="sxs-lookup"><span data-stu-id="9fcd4-116">Each group of three vertices defines a separate triangle.</span></span>

<span data-ttu-id="9fcd4-117">背面的剔除會受到目前繞組順序轉譯狀態的影響。</span><span class="sxs-lookup"><span data-stu-id="9fcd4-117">Back-face culling is affected by the current winding-order render state.</span></span>

</dd> <dt>

<span data-ttu-id="9fcd4-118"><span id="D3DPT_TRIANGLESTRIP"></span><span id="d3dpt_trianglestrip"></span>**D3DPT \_ TRIANGLESTRIP**</span><span class="sxs-lookup"><span data-stu-id="9fcd4-118"><span id="D3DPT_TRIANGLESTRIP"></span><span id="d3dpt_trianglestrip"></span>**D3DPT\_TRIANGLESTRIP**</span></span>
</dt> <dd>

<span data-ttu-id="9fcd4-119">將頂點轉譯為三角形帶。</span><span class="sxs-lookup"><span data-stu-id="9fcd4-119">Renders the vertices as a triangle strip.</span></span> <span data-ttu-id="9fcd4-120">背面剔除旗標會自動在偶數三角形上翻轉。</span><span class="sxs-lookup"><span data-stu-id="9fcd4-120">The backface-culling flag is automatically flipped on even-numbered triangles.</span></span>

</dd> <dt>

<span data-ttu-id="9fcd4-121"><span id="D3DPT_TRIANGLEFAN"></span><span id="d3dpt_trianglefan"></span>**D3DPT \_ TRIANGLEFAN**</span><span class="sxs-lookup"><span data-stu-id="9fcd4-121"><span id="D3DPT_TRIANGLEFAN"></span><span id="d3dpt_trianglefan"></span>**D3DPT\_TRIANGLEFAN**</span></span>
</dt> <dd>

<span data-ttu-id="9fcd4-122">以三角形風扇的形式呈現頂點。</span><span class="sxs-lookup"><span data-stu-id="9fcd4-122">Renders the vertices as a triangle fan.</span></span>

</dd> <dt>

<span data-ttu-id="9fcd4-123"><span id="D3DPT_FORCE_DWORD"></span><span id="d3dpt_force_dword"></span>**D3DPT \_ 強制 \_ DWORD**</span><span class="sxs-lookup"><span data-stu-id="9fcd4-123"><span id="D3DPT_FORCE_DWORD"></span><span id="d3dpt_force_dword"></span>**D3DPT\_FORCE\_DWORD**</span></span>
</dt> <dd>

<span data-ttu-id="9fcd4-124">強制此列舉的大小編譯為32位。</span><span class="sxs-lookup"><span data-stu-id="9fcd4-124">Forces this enumeration to compile to 32 bits in size.</span></span> <span data-ttu-id="9fcd4-125">如果沒有這個值，某些編譯器會允許此列舉編譯成32位以外的大小。</span><span class="sxs-lookup"><span data-stu-id="9fcd4-125">Without this value, some compilers would allow this enumeration to compile to a size other than 32 bits.</span></span> <span data-ttu-id="9fcd4-126">不使用這個值。</span><span class="sxs-lookup"><span data-stu-id="9fcd4-126">This value is not used.</span></span>

</dd> </dl>

## <a name="remarks"></a><span data-ttu-id="9fcd4-127">備註</span><span class="sxs-lookup"><span data-stu-id="9fcd4-127">Remarks</span></span>

<span data-ttu-id="9fcd4-128">使用 [三角形的條紋](triangle-strips.md) 或 [三角形風扇 (Direct3D 9) ](triangle-fans.md) 通常比使用三角形清單更有效率，因為較少的頂點會重複。</span><span class="sxs-lookup"><span data-stu-id="9fcd4-128">Using [Triangle Strips](triangle-strips.md) or [Triangle Fans (Direct3D 9)](triangle-fans.md) is often more efficient than using triangle lists because fewer vertices are duplicated.</span></span>

## <a name="requirements"></a><span data-ttu-id="9fcd4-129">規格需求</span><span class="sxs-lookup"><span data-stu-id="9fcd4-129">Requirements</span></span>



| <span data-ttu-id="9fcd4-130">需求</span><span class="sxs-lookup"><span data-stu-id="9fcd4-130">Requirement</span></span> | <span data-ttu-id="9fcd4-131">值</span><span class="sxs-lookup"><span data-stu-id="9fcd4-131">Value</span></span> |
|-------------------|----------------------------------------------------------------------------------------|
| <span data-ttu-id="9fcd4-132">標頭</span><span class="sxs-lookup"><span data-stu-id="9fcd4-132">Header</span></span><br/> | <dl> <span data-ttu-id="9fcd4-133"><dt>D3D9Types。h</dt></span><span class="sxs-lookup"><span data-stu-id="9fcd4-133"><dt>D3D9Types.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="9fcd4-134">另請參閱</span><span class="sxs-lookup"><span data-stu-id="9fcd4-134">See also</span></span>

<dl> <dt>

[<span data-ttu-id="9fcd4-135">Direct3D 列舉</span><span class="sxs-lookup"><span data-stu-id="9fcd4-135">Direct3D Enumerations</span></span>](dx9-graphics-reference-d3d-enums.md)
</dt> <dt>

[<span data-ttu-id="9fcd4-136">**IDirect3DDevice9::DrawIndexedPrimitive**</span><span class="sxs-lookup"><span data-stu-id="9fcd4-136">**IDirect3DDevice9::DrawIndexedPrimitive**</span></span>](/windows/win32/api/d3d9helper/nf-d3d9helper-idirect3ddevice9-drawindexedprimitive)
</dt> <dt>

[<span data-ttu-id="9fcd4-137">**IDirect3DDevice9::DrawIndexedPrimitiveUP**</span><span class="sxs-lookup"><span data-stu-id="9fcd4-137">**IDirect3DDevice9::DrawIndexedPrimitiveUP**</span></span>](/windows/win32/api/d3d9helper/nf-d3d9helper-idirect3ddevice9-drawindexedprimitiveup)
</dt> <dt>

[<span data-ttu-id="9fcd4-138">**IDirect3DDevice9::DrawPrimitive**</span><span class="sxs-lookup"><span data-stu-id="9fcd4-138">**IDirect3DDevice9::DrawPrimitive**</span></span>](/windows/win32/api/d3d9helper/nf-d3d9helper-idirect3ddevice9-drawprimitive)
</dt> <dt>

[<span data-ttu-id="9fcd4-139">**IDirect3DDevice9::DrawPrimitiveUP**</span><span class="sxs-lookup"><span data-stu-id="9fcd4-139">**IDirect3DDevice9::DrawPrimitiveUP**</span></span>](/windows/win32/api/d3d9helper/nf-d3d9helper-idirect3ddevice9-drawprimitiveup)
</dt> </dl>

 

 
