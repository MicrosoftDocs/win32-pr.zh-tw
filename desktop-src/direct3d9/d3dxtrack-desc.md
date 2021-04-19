---
description: 描述動畫播放軌，並指定在指定時間的軌跡粗細、速度和位置。
ms.assetid: f1469b6f-861f-4b7d-a187-933092a5d257
title: 'D3DXTRACK_DESC 結構 (D3dx9anim .h) '
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- D3DXTRACK_DESC
api_type:
- HeaderDef
api_location:
- d3dx9anim.h
ms.openlocfilehash: 12f1604cf954bcdd6a2a898fec5410804112e498
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 03/15/2021
ms.locfileid: "106986507"
---
# <a name="d3dxtrack_desc-structure"></a><span data-ttu-id="65a1f-103">D3DXTRACK \_ DESC 結構</span><span class="sxs-lookup"><span data-stu-id="65a1f-103">D3DXTRACK\_DESC structure</span></span>

<span data-ttu-id="65a1f-104">描述動畫播放軌，並指定在指定時間的軌跡粗細、速度和位置。</span><span class="sxs-lookup"><span data-stu-id="65a1f-104">Describes an animation track and specifies blending weight, speed, and position for the track at a given time.</span></span>

## <a name="syntax"></a><span data-ttu-id="65a1f-105">語法</span><span class="sxs-lookup"><span data-stu-id="65a1f-105">Syntax</span></span>


```C++
typedef struct D3DXTRACK_DESC {
  D3DXPRIORITY_TYPE Priority;
  FLOAT             Weight;
  FLOAT             Speed;
  DOUBLE            Position;
  BOOL              Enable;
} D3DXTRACK_DESC, *LPD3DXTRACK_DESC;
```



## <a name="members"></a><span data-ttu-id="65a1f-106">成員</span><span class="sxs-lookup"><span data-stu-id="65a1f-106">Members</span></span>

<dl> <dt>

<span data-ttu-id="65a1f-107">**優先順序**</span><span class="sxs-lookup"><span data-stu-id="65a1f-107">**Priority**</span></span>
</dt> <dd>

<span data-ttu-id="65a1f-108">類型： **[ **D3DXPRIORITY \_ 類型**](./d3dxpriority-type.md)**</span><span class="sxs-lookup"><span data-stu-id="65a1f-108">Type: **[**D3DXPRIORITY\_TYPE**](./d3dxpriority-type.md)**</span></span>

</dd> <dd>

<span data-ttu-id="65a1f-109">優先權類型，如 [**D3DXPRIORITY \_ 類型**](./d3dxpriority-type.md)中所定義。</span><span class="sxs-lookup"><span data-stu-id="65a1f-109">Priority type, as defined in [**D3DXPRIORITY\_TYPE**](./d3dxpriority-type.md).</span></span>

</dd> <dt>

<span data-ttu-id="65a1f-110">**Weight**</span><span class="sxs-lookup"><span data-stu-id="65a1f-110">**Weight**</span></span>
</dt> <dd>

<span data-ttu-id="65a1f-111">類型： **[ **FLOAT**](../winprog/windows-data-types.md)**</span><span class="sxs-lookup"><span data-stu-id="65a1f-111">Type: **[**FLOAT**](../winprog/windows-data-types.md)**</span></span>

</dd> <dd>

<span data-ttu-id="65a1f-112">加權值。</span><span class="sxs-lookup"><span data-stu-id="65a1f-112">Weight value.</span></span> <span data-ttu-id="65a1f-113">權數會決定此追蹤與其他追蹤的比例。</span><span class="sxs-lookup"><span data-stu-id="65a1f-113">The weight determines the proportion of this track to blend with other tracks.</span></span>

</dd> <dt>

<span data-ttu-id="65a1f-114">**速度**</span><span class="sxs-lookup"><span data-stu-id="65a1f-114">**Speed**</span></span>
</dt> <dd>

<span data-ttu-id="65a1f-115">類型： **[ **FLOAT**](../winprog/windows-data-types.md)**</span><span class="sxs-lookup"><span data-stu-id="65a1f-115">Type: **[**FLOAT**](../winprog/windows-data-types.md)**</span></span>

</dd> <dd>

<span data-ttu-id="65a1f-116">速度值。</span><span class="sxs-lookup"><span data-stu-id="65a1f-116">Speed value.</span></span> <span data-ttu-id="65a1f-117">這種方式類似于乘數，可用來調整追蹤的期間。</span><span class="sxs-lookup"><span data-stu-id="65a1f-117">This is used similarly to a multiplier to scale the period of the track.</span></span>

</dd> <dt>

<span data-ttu-id="65a1f-118">**位置**</span><span class="sxs-lookup"><span data-stu-id="65a1f-118">**Position**</span></span>
</dt> <dd>

<span data-ttu-id="65a1f-119">類型： **[ **DOUBLE**](../winprog/windows-data-types.md)**</span><span class="sxs-lookup"><span data-stu-id="65a1f-119">Type: **[**DOUBLE**](../winprog/windows-data-types.md)**</span></span>

</dd> <dd>

<span data-ttu-id="65a1f-120">曲目的時間位置，以目前動畫集的當地時間範圍為限。</span><span class="sxs-lookup"><span data-stu-id="65a1f-120">Time position of the track, in the local timeframe of its current animation set.</span></span>

</dd> <dt>

<span data-ttu-id="65a1f-121">**啟用**</span><span class="sxs-lookup"><span data-stu-id="65a1f-121">**Enable**</span></span>
</dt> <dd>

<span data-ttu-id="65a1f-122">類型： **[ **BOOL**](../winprog/windows-data-types.md)**</span><span class="sxs-lookup"><span data-stu-id="65a1f-122">Type: **[**BOOL**](../winprog/windows-data-types.md)**</span></span>

</dd> <dd>

<span data-ttu-id="65a1f-123">追蹤啟用/停用。</span><span class="sxs-lookup"><span data-stu-id="65a1f-123">Track enable/disable.</span></span> <span data-ttu-id="65a1f-124">若要啟用，請將設定為 **TRUE**。</span><span class="sxs-lookup"><span data-stu-id="65a1f-124">To enable, set to **TRUE**.</span></span> <span data-ttu-id="65a1f-125">若要停用，請設定為 **FALSE**。</span><span class="sxs-lookup"><span data-stu-id="65a1f-125">To disable, set to **FALSE**.</span></span>

</dd> </dl>

## <a name="remarks"></a><span data-ttu-id="65a1f-126">備註</span><span class="sxs-lookup"><span data-stu-id="65a1f-126">Remarks</span></span>

<span data-ttu-id="65a1f-127">具有相同優先權的追蹤會混合在一起，而這兩個結果值接著會使用優先順序 blend 因數進行混合。</span><span class="sxs-lookup"><span data-stu-id="65a1f-127">Tracks with the same priority are blended together, and the two resulting values are then blended using the priority blend factor.</span></span> <span data-ttu-id="65a1f-128">播放軌必須有一個動畫集 (另存) 與其相關聯。</span><span class="sxs-lookup"><span data-stu-id="65a1f-128">A track must have an animation set (stored separately) associated with it.</span></span>

## <a name="requirements"></a><span data-ttu-id="65a1f-129">規格需求</span><span class="sxs-lookup"><span data-stu-id="65a1f-129">Requirements</span></span>



| <span data-ttu-id="65a1f-130">需求</span><span class="sxs-lookup"><span data-stu-id="65a1f-130">Requirement</span></span> | <span data-ttu-id="65a1f-131">值</span><span class="sxs-lookup"><span data-stu-id="65a1f-131">Value</span></span> |
|-------------------|----------------------------------------------------------------------------------------|
| <span data-ttu-id="65a1f-132">標頭</span><span class="sxs-lookup"><span data-stu-id="65a1f-132">Header</span></span><br/> | <dl> <span data-ttu-id="65a1f-133"><dt>D3dx9anim。h</dt></span><span class="sxs-lookup"><span data-stu-id="65a1f-133"><dt>D3dx9anim.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="65a1f-134">另請參閱</span><span class="sxs-lookup"><span data-stu-id="65a1f-134">See also</span></span>

<dl> <dt>

[<span data-ttu-id="65a1f-135">D3DX 結構</span><span class="sxs-lookup"><span data-stu-id="65a1f-135">D3DX Structures</span></span>](dx9-graphics-reference-d3dx-structures.md)
</dt> </dl>

 

 
