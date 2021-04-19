---
description: 定義樣板緩衝區作業。
ms.assetid: 338a3b7f-236a-484f-96b8-1e6bfb014484
title: 'D3DSTENCILOP 列舉 (D3D9Types) '
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- D3DSTENCILOP
api_type:
- HeaderDef
api_location:
- D3D9Types.h
ms.openlocfilehash: 34784a57d3afd3862d380554040f3909ec905898
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 03/15/2021
ms.locfileid: "106977133"
---
# <a name="d3dstencilop-enumeration"></a><span data-ttu-id="8de4b-103">D3DSTENCILOP 列舉</span><span class="sxs-lookup"><span data-stu-id="8de4b-103">D3DSTENCILOP enumeration</span></span>

<span data-ttu-id="8de4b-104">定義樣板緩衝區作業。</span><span class="sxs-lookup"><span data-stu-id="8de4b-104">Defines stencil-buffer operations.</span></span>

## <a name="syntax"></a><span data-ttu-id="8de4b-105">Syntax</span><span class="sxs-lookup"><span data-stu-id="8de4b-105">Syntax</span></span>


```C++
typedef enum D3DSTENCILOP { 
  D3DSTENCILOP_KEEP         = 1,
  D3DSTENCILOP_ZERO         = 2,
  D3DSTENCILOP_REPLACE      = 3,
  D3DSTENCILOP_INCRSAT      = 4,
  D3DSTENCILOP_DECRSAT      = 5,
  D3DSTENCILOP_INVERT       = 6,
  D3DSTENCILOP_INCR         = 7,
  D3DSTENCILOP_DECR         = 8,
  D3DSTENCILOP_FORCE_DWORD  = 0x7fffffff
} D3DSTENCILOP, *LPD3DSTENCILOP;
```



## <a name="constants"></a><span data-ttu-id="8de4b-106">常數</span><span class="sxs-lookup"><span data-stu-id="8de4b-106">Constants</span></span>

<dl> <dt>

<span data-ttu-id="8de4b-107"><span id="D3DSTENCILOP_KEEP"></span><span id="d3dstencilop_keep"></span>**D3DSTENCILOP \_ 保留**</span><span class="sxs-lookup"><span data-stu-id="8de4b-107"><span id="D3DSTENCILOP_KEEP"></span><span id="d3dstencilop_keep"></span>**D3DSTENCILOP\_KEEP**</span></span>
</dt> <dd>

<span data-ttu-id="8de4b-108">請勿更新樣板緩衝區中的專案。</span><span class="sxs-lookup"><span data-stu-id="8de4b-108">Do not update the entry in the stencil buffer.</span></span> <span data-ttu-id="8de4b-109">這是預設值。</span><span class="sxs-lookup"><span data-stu-id="8de4b-109">This is the default value.</span></span>

</dd> <dt>

<span data-ttu-id="8de4b-110"><span id="D3DSTENCILOP_ZERO"></span><span id="d3dstencilop_zero"></span>**D3DSTENCILOP \_ 零**</span><span class="sxs-lookup"><span data-stu-id="8de4b-110"><span id="D3DSTENCILOP_ZERO"></span><span id="d3dstencilop_zero"></span>**D3DSTENCILOP\_ZERO**</span></span>
</dt> <dd>

<span data-ttu-id="8de4b-111">將樣板緩衝區專案設定為0。</span><span class="sxs-lookup"><span data-stu-id="8de4b-111">Set the stencil-buffer entry to 0.</span></span>

</dd> <dt>

<span data-ttu-id="8de4b-112"><span id="D3DSTENCILOP_REPLACE"></span><span id="d3dstencilop_replace"></span>**D3DSTENCILOP \_ REPLACE**</span><span class="sxs-lookup"><span data-stu-id="8de4b-112"><span id="D3DSTENCILOP_REPLACE"></span><span id="d3dstencilop_replace"></span>**D3DSTENCILOP\_REPLACE**</span></span>
</dt> <dd>

<span data-ttu-id="8de4b-113">將樣板緩衝區專案取代為參考值。</span><span class="sxs-lookup"><span data-stu-id="8de4b-113">Replace the stencil-buffer entry with a reference value.</span></span>

</dd> <dt>

<span data-ttu-id="8de4b-114"><span id="D3DSTENCILOP_INCRSAT"></span><span id="d3dstencilop_incrsat"></span>**D3DSTENCILOP \_ INCRSAT**</span><span class="sxs-lookup"><span data-stu-id="8de4b-114"><span id="D3DSTENCILOP_INCRSAT"></span><span id="d3dstencilop_incrsat"></span>**D3DSTENCILOP\_INCRSAT**</span></span>
</dt> <dd>

<span data-ttu-id="8de4b-115">將樣板緩衝區專案遞增，固定為最大值。</span><span class="sxs-lookup"><span data-stu-id="8de4b-115">Increment the stencil-buffer entry, clamping to the maximum value.</span></span>

</dd> <dt>

<span data-ttu-id="8de4b-116"><span id="D3DSTENCILOP_DECRSAT"></span><span id="d3dstencilop_decrsat"></span>**D3DSTENCILOP \_ DECRSAT**</span><span class="sxs-lookup"><span data-stu-id="8de4b-116"><span id="D3DSTENCILOP_DECRSAT"></span><span id="d3dstencilop_decrsat"></span>**D3DSTENCILOP\_DECRSAT**</span></span>
</dt> <dd>

<span data-ttu-id="8de4b-117">遞減樣板緩衝區專案，固定為零。</span><span class="sxs-lookup"><span data-stu-id="8de4b-117">Decrement the stencil-buffer entry, clamping to zero.</span></span>

</dd> <dt>

<span data-ttu-id="8de4b-118"><span id="D3DSTENCILOP_INVERT"></span><span id="d3dstencilop_invert"></span>**D3DSTENCILOP \_ 反轉**</span><span class="sxs-lookup"><span data-stu-id="8de4b-118"><span id="D3DSTENCILOP_INVERT"></span><span id="d3dstencilop_invert"></span>**D3DSTENCILOP\_INVERT**</span></span>
</dt> <dd>

<span data-ttu-id="8de4b-119">反轉樣板緩衝區專案中的位。</span><span class="sxs-lookup"><span data-stu-id="8de4b-119">Invert the bits in the stencil-buffer entry.</span></span>

</dd> <dt>

<span data-ttu-id="8de4b-120"><span id="D3DSTENCILOP_INCR"></span><span id="d3dstencilop_incr"></span>**D3DSTENCILOP \_ 增量**</span><span class="sxs-lookup"><span data-stu-id="8de4b-120"><span id="D3DSTENCILOP_INCR"></span><span id="d3dstencilop_incr"></span>**D3DSTENCILOP\_INCR**</span></span>
</dt> <dd>

<span data-ttu-id="8de4b-121">如果新值超過最大值，則將樣板緩衝區專案遞增，並將其換成零。</span><span class="sxs-lookup"><span data-stu-id="8de4b-121">Increment the stencil-buffer entry, wrapping to zero if the new value exceeds the maximum value.</span></span>

</dd> <dt>

<span data-ttu-id="8de4b-122"><span id="D3DSTENCILOP_DECR"></span><span id="d3dstencilop_decr"></span>**D3DSTENCILOP \_ operators.decr**</span><span class="sxs-lookup"><span data-stu-id="8de4b-122"><span id="D3DSTENCILOP_DECR"></span><span id="d3dstencilop_decr"></span>**D3DSTENCILOP\_DECR**</span></span>
</dt> <dd>

<span data-ttu-id="8de4b-123">遞減樣板緩衝區專案，如果新值小於零，則會換行到最大值。</span><span class="sxs-lookup"><span data-stu-id="8de4b-123">Decrement the stencil-buffer entry, wrapping to the maximum value if the new value is less than zero.</span></span>

</dd> <dt>

<span data-ttu-id="8de4b-124"><span id="D3DSTENCILOP_FORCE_DWORD"></span><span id="d3dstencilop_force_dword"></span>**D3DSTENCILOP \_ 強制 \_ DWORD**</span><span class="sxs-lookup"><span data-stu-id="8de4b-124"><span id="D3DSTENCILOP_FORCE_DWORD"></span><span id="d3dstencilop_force_dword"></span>**D3DSTENCILOP\_FORCE\_DWORD**</span></span>
</dt> <dd>

<span data-ttu-id="8de4b-125">強制此列舉的大小編譯為32位。</span><span class="sxs-lookup"><span data-stu-id="8de4b-125">Forces this enumeration to compile to 32 bits in size.</span></span> <span data-ttu-id="8de4b-126">如果沒有這個值，某些編譯器會允許此列舉編譯成32位以外的大小。</span><span class="sxs-lookup"><span data-stu-id="8de4b-126">Without this value, some compilers would allow this enumeration to compile to a size other than 32 bits.</span></span> <span data-ttu-id="8de4b-127">不使用這個值。</span><span class="sxs-lookup"><span data-stu-id="8de4b-127">This value is not used.</span></span>

</dd> </dl>

## <a name="remarks"></a><span data-ttu-id="8de4b-128">備註</span><span class="sxs-lookup"><span data-stu-id="8de4b-128">Remarks</span></span>

<span data-ttu-id="8de4b-129">樣板-緩衝區專案是整數值，範圍從0到2ⁿ-1，其中 n 是樣板緩衝區的位深度。</span><span class="sxs-lookup"><span data-stu-id="8de4b-129">Stencil-buffer entries are integer values ranging from 0 through 2ⁿ - 1, where n is the bit depth of the stencil buffer.</span></span>

## <a name="requirements"></a><span data-ttu-id="8de4b-130">規格需求</span><span class="sxs-lookup"><span data-stu-id="8de4b-130">Requirements</span></span>



| <span data-ttu-id="8de4b-131">需求</span><span class="sxs-lookup"><span data-stu-id="8de4b-131">Requirement</span></span> | <span data-ttu-id="8de4b-132">值</span><span class="sxs-lookup"><span data-stu-id="8de4b-132">Value</span></span> |
|-------------------|----------------------------------------------------------------------------------------|
| <span data-ttu-id="8de4b-133">標頭</span><span class="sxs-lookup"><span data-stu-id="8de4b-133">Header</span></span><br/> | <dl> <span data-ttu-id="8de4b-134"><dt>D3D9Types。h</dt></span><span class="sxs-lookup"><span data-stu-id="8de4b-134"><dt>D3D9Types.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="8de4b-135">另請參閱</span><span class="sxs-lookup"><span data-stu-id="8de4b-135">See also</span></span>

<dl> <dt>

[<span data-ttu-id="8de4b-136">Direct3D 列舉</span><span class="sxs-lookup"><span data-stu-id="8de4b-136">Direct3D Enumerations</span></span>](dx9-graphics-reference-d3d-enums.md)
</dt> </dl>

 

 




