---
description: 定義描述填滿模式的常數。
ms.assetid: be835432-e8d5-4afb-a810-2dac25bdc9dc
title: 'D3DFILLMODE 列舉 (D3D9Types) '
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- D3DFILLMODE
api_type:
- HeaderDef
api_location:
- D3D9Types.h
ms.openlocfilehash: 33cf03258933055aa18aecb42fffe4d8f33b1e51
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 03/15/2021
ms.locfileid: "106992758"
---
# <a name="d3dfillmode-enumeration"></a><span data-ttu-id="9fe67-103">D3DFILLMODE 列舉</span><span class="sxs-lookup"><span data-stu-id="9fe67-103">D3DFILLMODE enumeration</span></span>

<span data-ttu-id="9fe67-104">定義描述填滿模式的常數。</span><span class="sxs-lookup"><span data-stu-id="9fe67-104">Defines constants describing the fill mode.</span></span>

## <a name="syntax"></a><span data-ttu-id="9fe67-105">Syntax</span><span class="sxs-lookup"><span data-stu-id="9fe67-105">Syntax</span></span>


```C++
typedef enum D3DFILLMODE { 
  D3DFILL_POINT        = 1,
  D3DFILL_WIREFRAME    = 2,
  D3DFILL_SOLID        = 3,
  D3DFILL_FORCE_DWORD  = 0x7fffffff
} D3DFILLMODE, *LPD3DFILLMODE;
```



## <a name="constants"></a><span data-ttu-id="9fe67-106">常數</span><span class="sxs-lookup"><span data-stu-id="9fe67-106">Constants</span></span>

<dl> <dt>

<span data-ttu-id="9fe67-107"><span id="D3DFILL_POINT"></span><span id="d3dfill_point"></span>**D3DFILL \_ 點**</span><span class="sxs-lookup"><span data-stu-id="9fe67-107"><span id="D3DFILL_POINT"></span><span id="d3dfill_point"></span>**D3DFILL\_POINT**</span></span>
</dt> <dd>

<span data-ttu-id="9fe67-108">填滿點。</span><span class="sxs-lookup"><span data-stu-id="9fe67-108">Fill points.</span></span>

</dd> <dt>

<span data-ttu-id="9fe67-109"><span id="D3DFILL_WIREFRAME"></span><span id="d3dfill_wireframe"></span>**D3DFILL \_ 線框**</span><span class="sxs-lookup"><span data-stu-id="9fe67-109"><span id="D3DFILL_WIREFRAME"></span><span id="d3dfill_wireframe"></span>**D3DFILL\_WIREFRAME**</span></span>
</dt> <dd>

<span data-ttu-id="9fe67-110">填滿框線。</span><span class="sxs-lookup"><span data-stu-id="9fe67-110">Fill wireframes.</span></span>

</dd> <dt>

<span data-ttu-id="9fe67-111"><span id="D3DFILL_SOLID"></span><span id="d3dfill_solid"></span>**D3DFILL \_ 固態**</span><span class="sxs-lookup"><span data-stu-id="9fe67-111"><span id="D3DFILL_SOLID"></span><span id="d3dfill_solid"></span>**D3DFILL\_SOLID**</span></span>
</dt> <dd>

<span data-ttu-id="9fe67-112">填滿純色。</span><span class="sxs-lookup"><span data-stu-id="9fe67-112">Fill solids.</span></span>

</dd> <dt>

<span data-ttu-id="9fe67-113"><span id="D3DFILL_FORCE_DWORD"></span><span id="d3dfill_force_dword"></span>**D3DFILL \_ 強制 \_ DWORD**</span><span class="sxs-lookup"><span data-stu-id="9fe67-113"><span id="D3DFILL_FORCE_DWORD"></span><span id="d3dfill_force_dword"></span>**D3DFILL\_FORCE\_DWORD**</span></span>
</dt> <dd>

<span data-ttu-id="9fe67-114">強制此列舉的大小編譯為32位。</span><span class="sxs-lookup"><span data-stu-id="9fe67-114">Forces this enumeration to compile to 32 bits in size.</span></span> <span data-ttu-id="9fe67-115">如果沒有這個值，某些編譯器會允許此列舉編譯成32位以外的大小。</span><span class="sxs-lookup"><span data-stu-id="9fe67-115">Without this value, some compilers would allow this enumeration to compile to a size other than 32 bits.</span></span> <span data-ttu-id="9fe67-116">不使用這個值。</span><span class="sxs-lookup"><span data-stu-id="9fe67-116">This value is not used.</span></span>

</dd> </dl>

## <a name="remarks"></a><span data-ttu-id="9fe67-117">備註</span><span class="sxs-lookup"><span data-stu-id="9fe67-117">Remarks</span></span>

<span data-ttu-id="9fe67-118">D3DRS FILLMODE 轉譯狀態會使用這個列舉型別中的值 \_ 。</span><span class="sxs-lookup"><span data-stu-id="9fe67-118">The values in this enumerated type are used by the D3DRS\_FILLMODE render state.</span></span>

## <a name="requirements"></a><span data-ttu-id="9fe67-119">規格需求</span><span class="sxs-lookup"><span data-stu-id="9fe67-119">Requirements</span></span>



| <span data-ttu-id="9fe67-120">需求</span><span class="sxs-lookup"><span data-stu-id="9fe67-120">Requirement</span></span> | <span data-ttu-id="9fe67-121">值</span><span class="sxs-lookup"><span data-stu-id="9fe67-121">Value</span></span> |
|-------------------|----------------------------------------------------------------------------------------|
| <span data-ttu-id="9fe67-122">標頭</span><span class="sxs-lookup"><span data-stu-id="9fe67-122">Header</span></span><br/> | <dl> <span data-ttu-id="9fe67-123"><dt>D3D9Types。h</dt></span><span class="sxs-lookup"><span data-stu-id="9fe67-123"><dt>D3D9Types.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="9fe67-124">另請參閱</span><span class="sxs-lookup"><span data-stu-id="9fe67-124">See also</span></span>

<dl> <dt>

[<span data-ttu-id="9fe67-125">Direct3D 列舉</span><span class="sxs-lookup"><span data-stu-id="9fe67-125">Direct3D Enumerations</span></span>](dx9-graphics-reference-d3d-enums.md)
</dt> <dt>

[<span data-ttu-id="9fe67-126">**D3DRENDERSTATETYPE**</span><span class="sxs-lookup"><span data-stu-id="9fe67-126">**D3DRENDERSTATETYPE**</span></span>](./d3drenderstatetype.md)
</dt> </dl>

 

 
