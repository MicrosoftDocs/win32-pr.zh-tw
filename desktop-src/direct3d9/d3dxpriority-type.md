---
description: 定義要指派動畫播放軌的優先順序類型。
ms.assetid: 7bd83e31-09c4-4376-a22d-ed8023b78e84
title: 'D3DXPRIORITY_TYPE 列舉 (D3dx9anim .h) '
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- D3DXPRIORITY_TYPE
api_type:
- HeaderDef
api_location:
- d3dx9anim.h
ms.openlocfilehash: 5e6d82807cbd0e93e7a1127db80726c0ec06b5da
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 03/15/2021
ms.locfileid: "104386449"
---
# <a name="d3dxpriority_type-enumeration"></a><span data-ttu-id="b1ac7-103">D3DXPRIORITY \_ 類型列舉</span><span class="sxs-lookup"><span data-stu-id="b1ac7-103">D3DXPRIORITY\_TYPE enumeration</span></span>

<span data-ttu-id="b1ac7-104">定義要指派動畫播放軌的優先順序類型。</span><span class="sxs-lookup"><span data-stu-id="b1ac7-104">Defines the priority type to which an animation track is assigned.</span></span>

## <a name="syntax"></a><span data-ttu-id="b1ac7-105">Syntax</span><span class="sxs-lookup"><span data-stu-id="b1ac7-105">Syntax</span></span>


```C++
typedef enum D3DXPRIORITY_TYPE { 
  D3DXPRIORITY_LOW          = 0,
  D3DXPRIORITY_HIGH         = 1,
  D3DXPRIORITY_FORCE_DWORD  = 0x7fffffff
} D3DXPRIORITY_TYPE, *LPD3DXPRIORITY_TYPE;
```



## <a name="constants"></a><span data-ttu-id="b1ac7-106">常數</span><span class="sxs-lookup"><span data-stu-id="b1ac7-106">Constants</span></span>

<dl> <dt>

<span data-ttu-id="b1ac7-107"><span id="D3DXPRIORITY_LOW"></span><span id="d3dxpriority_low"></span>**D3DXPRIORITY \_ 低**</span><span class="sxs-lookup"><span data-stu-id="b1ac7-107"><span id="D3DXPRIORITY_LOW"></span><span id="d3dxpriority_low"></span>**D3DXPRIORITY\_LOW**</span></span>
</dt> <dd>

<span data-ttu-id="b1ac7-108">在低優先順序 blend 與高優先順序 blend 混合之前，應該先混合所有低優先順序的追蹤。</span><span class="sxs-lookup"><span data-stu-id="b1ac7-108">Track should be blended with all the low-priority tracks before the low-priority blend is mixed with the high-priority blend.</span></span>

</dd> <dt>

<span data-ttu-id="b1ac7-109"><span id="D3DXPRIORITY_HIGH"></span><span id="d3dxpriority_high"></span>**D3DXPRIORITY \_ HIGH**</span><span class="sxs-lookup"><span data-stu-id="b1ac7-109"><span id="D3DXPRIORITY_HIGH"></span><span id="d3dxpriority_high"></span>**D3DXPRIORITY\_HIGH**</span></span>
</dt> <dd>

<span data-ttu-id="b1ac7-110">在高優先順序 blend 與低優先順序 blend 混合之前，應該先混合所有高優先順序的追蹤。</span><span class="sxs-lookup"><span data-stu-id="b1ac7-110">Track should be blended with all the high-priority tracks before the high-priority blend is mixed with the low-priority blend.</span></span>

</dd> <dt>

<span data-ttu-id="b1ac7-111"><span id="D3DXPRIORITY_FORCE_DWORD"></span><span id="d3dxpriority_force_dword"></span>**D3DXPRIORITY \_ 強制 \_ DWORD**</span><span class="sxs-lookup"><span data-stu-id="b1ac7-111"><span id="D3DXPRIORITY_FORCE_DWORD"></span><span id="d3dxpriority_force_dword"></span>**D3DXPRIORITY\_FORCE\_DWORD**</span></span>
</dt> <dd>

<span data-ttu-id="b1ac7-112">強制此列舉的大小編譯為32位。</span><span class="sxs-lookup"><span data-stu-id="b1ac7-112">Forces this enumeration to compile to 32 bits in size.</span></span> <span data-ttu-id="b1ac7-113">如果沒有這個值，某些編譯器會允許此列舉編譯成32位以外的大小。</span><span class="sxs-lookup"><span data-stu-id="b1ac7-113">Without this value, some compilers would allow this enumeration to compile to a size other than 32 bits.</span></span> <span data-ttu-id="b1ac7-114">不使用這個值。</span><span class="sxs-lookup"><span data-stu-id="b1ac7-114">This value is not used.</span></span>

</dd> </dl>

## <a name="remarks"></a><span data-ttu-id="b1ac7-115">備註</span><span class="sxs-lookup"><span data-stu-id="b1ac7-115">Remarks</span></span>

<span data-ttu-id="b1ac7-116">具有相同優先權的追蹤會混合在一起，而這兩個結果值接著會使用優先順序 blend 因數進行混合。</span><span class="sxs-lookup"><span data-stu-id="b1ac7-116">Tracks with the same priority are blended together, and the two resulting values are then blended using the priority blend factor.</span></span>

## <a name="requirements"></a><span data-ttu-id="b1ac7-117">規格需求</span><span class="sxs-lookup"><span data-stu-id="b1ac7-117">Requirements</span></span>



| <span data-ttu-id="b1ac7-118">需求</span><span class="sxs-lookup"><span data-stu-id="b1ac7-118">Requirement</span></span> | <span data-ttu-id="b1ac7-119">值</span><span class="sxs-lookup"><span data-stu-id="b1ac7-119">Value</span></span> |
|-------------------|----------------------------------------------------------------------------------------|
| <span data-ttu-id="b1ac7-120">標頭</span><span class="sxs-lookup"><span data-stu-id="b1ac7-120">Header</span></span><br/> | <dl> <span data-ttu-id="b1ac7-121"><dt>D3dx9anim。h</dt></span><span class="sxs-lookup"><span data-stu-id="b1ac7-121"><dt>D3dx9anim.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="b1ac7-122">另請參閱</span><span class="sxs-lookup"><span data-stu-id="b1ac7-122">See also</span></span>

<dl> <dt>

[<span data-ttu-id="b1ac7-123">D3DX 列舉</span><span class="sxs-lookup"><span data-stu-id="b1ac7-123">D3DX Enumerations</span></span>](dx9-graphics-reference-d3dx-enums.md)
</dt> </dl>

 

 




