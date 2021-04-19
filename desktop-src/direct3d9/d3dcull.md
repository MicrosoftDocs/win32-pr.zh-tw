---
description: 定義支援的剔除模式。
ms.assetid: b669307c-0d40-4ecb-8a2e-8bd1d9c65647
title: 'D3DCULL 列舉 (D3D9Types) '
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- D3DCULL
api_type:
- HeaderDef
api_location:
- D3D9Types.h
ms.openlocfilehash: e88aa1baf86b2b03177cc686bf83299311065283
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 03/15/2021
ms.locfileid: "106991962"
---
# <a name="d3dcull-enumeration"></a><span data-ttu-id="0c49d-103">D3DCULL 列舉</span><span class="sxs-lookup"><span data-stu-id="0c49d-103">D3DCULL enumeration</span></span>

<span data-ttu-id="0c49d-104">定義支援的剔除模式。</span><span class="sxs-lookup"><span data-stu-id="0c49d-104">Defines the supported culling modes.</span></span>

## <a name="syntax"></a><span data-ttu-id="0c49d-105">Syntax</span><span class="sxs-lookup"><span data-stu-id="0c49d-105">Syntax</span></span>


```C++
typedef enum D3DCULL { 
  D3DCULL_NONE         = 1,
  D3DCULL_CW           = 2,
  D3DCULL_CCW          = 3,
  D3DCULL_FORCE_DWORD  = 0x7fffffff
} D3DCULL, *LPD3DCULL;
```



## <a name="constants"></a><span data-ttu-id="0c49d-106">常數</span><span class="sxs-lookup"><span data-stu-id="0c49d-106">Constants</span></span>

<dl> <dt>

<span data-ttu-id="0c49d-107"><span id="D3DCULL_NONE"></span><span id="d3dcull_none"></span>**D3DCULL \_ 無**</span><span class="sxs-lookup"><span data-stu-id="0c49d-107"><span id="D3DCULL_NONE"></span><span id="d3dcull_none"></span>**D3DCULL\_NONE**</span></span>
</dt> <dd>

<span data-ttu-id="0c49d-108">請勿挑選背面的臉部。</span><span class="sxs-lookup"><span data-stu-id="0c49d-108">Do not cull back faces.</span></span>

</dd> <dt>

<span data-ttu-id="0c49d-109"><span id="D3DCULL_CW"></span><span id="d3dcull_cw"></span>**D3DCULL \_ CW**</span><span class="sxs-lookup"><span data-stu-id="0c49d-109"><span id="D3DCULL_CW"></span><span id="d3dcull_cw"></span>**D3DCULL\_CW**</span></span>
</dt> <dd>

<span data-ttu-id="0c49d-110">以順時針頂點挑選背面的臉部。</span><span class="sxs-lookup"><span data-stu-id="0c49d-110">Cull back faces with clockwise vertices.</span></span>

</dd> <dt>

<span data-ttu-id="0c49d-111"><span id="D3DCULL_CCW"></span><span id="d3dcull_ccw"></span>**D3DCULL \_ CCW**</span><span class="sxs-lookup"><span data-stu-id="0c49d-111"><span id="D3DCULL_CCW"></span><span id="d3dcull_ccw"></span>**D3DCULL\_CCW**</span></span>
</dt> <dd>

<span data-ttu-id="0c49d-112">使用逆時針頂點來挑選背面的臉部。</span><span class="sxs-lookup"><span data-stu-id="0c49d-112">Cull back faces with counterclockwise vertices.</span></span>

</dd> <dt>

<span data-ttu-id="0c49d-113"><span id="D3DCULL_FORCE_DWORD"></span><span id="d3dcull_force_dword"></span>**D3DCULL \_ 強制 \_ DWORD**</span><span class="sxs-lookup"><span data-stu-id="0c49d-113"><span id="D3DCULL_FORCE_DWORD"></span><span id="d3dcull_force_dword"></span>**D3DCULL\_FORCE\_DWORD**</span></span>
</dt> <dd>

<span data-ttu-id="0c49d-114">強制此列舉的大小編譯為32位。</span><span class="sxs-lookup"><span data-stu-id="0c49d-114">Forces this enumeration to compile to 32 bits in size.</span></span> <span data-ttu-id="0c49d-115">如果沒有這個值，某些編譯器會允許此列舉編譯成32位以外的大小。</span><span class="sxs-lookup"><span data-stu-id="0c49d-115">Without this value, some compilers would allow this enumeration to compile to a size other than 32 bits.</span></span> <span data-ttu-id="0c49d-116">不使用這個值。</span><span class="sxs-lookup"><span data-stu-id="0c49d-116">This value is not used.</span></span>

</dd> </dl>

## <a name="remarks"></a><span data-ttu-id="0c49d-117">備註</span><span class="sxs-lookup"><span data-stu-id="0c49d-117">Remarks</span></span>

<span data-ttu-id="0c49d-118">D3DRS CULLMODE 轉譯狀態會使用這個列舉型別中的值 \_ 。</span><span class="sxs-lookup"><span data-stu-id="0c49d-118">The values in this enumerated type are used by the D3DRS\_CULLMODE render state.</span></span> <span data-ttu-id="0c49d-119">[剔除] 模式會定義呈現幾何時，如何挑選背面的臉部。</span><span class="sxs-lookup"><span data-stu-id="0c49d-119">The culling modes define how back faces are culled when rendering a geometry.</span></span>

## <a name="requirements"></a><span data-ttu-id="0c49d-120">規格需求</span><span class="sxs-lookup"><span data-stu-id="0c49d-120">Requirements</span></span>



| <span data-ttu-id="0c49d-121">需求</span><span class="sxs-lookup"><span data-stu-id="0c49d-121">Requirement</span></span> | <span data-ttu-id="0c49d-122">值</span><span class="sxs-lookup"><span data-stu-id="0c49d-122">Value</span></span> |
|-------------------|----------------------------------------------------------------------------------------|
| <span data-ttu-id="0c49d-123">標頭</span><span class="sxs-lookup"><span data-stu-id="0c49d-123">Header</span></span><br/> | <dl> <span data-ttu-id="0c49d-124"><dt>D3D9Types。h</dt></span><span class="sxs-lookup"><span data-stu-id="0c49d-124"><dt>D3D9Types.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="0c49d-125">另請參閱</span><span class="sxs-lookup"><span data-stu-id="0c49d-125">See also</span></span>

<dl> <dt>

[<span data-ttu-id="0c49d-126">Direct3D 列舉</span><span class="sxs-lookup"><span data-stu-id="0c49d-126">Direct3D Enumerations</span></span>](dx9-graphics-reference-d3d-enums.md)
</dt> <dt>

[<span data-ttu-id="0c49d-127">**D3DCAPS9**</span><span class="sxs-lookup"><span data-stu-id="0c49d-127">**D3DCAPS9**</span></span>](/windows/desktop/api/D3D9Caps/ns-d3d9caps-d3dcaps9)
</dt> <dt>

[<span data-ttu-id="0c49d-128">**D3DRENDERSTATETYPE**</span><span class="sxs-lookup"><span data-stu-id="0c49d-128">**D3DRENDERSTATETYPE**</span></span>](./d3drenderstatetype.md)
</dt> </dl>

 

 
