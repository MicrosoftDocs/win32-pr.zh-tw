---
description: D3DXQUATERNION 結構 (D3DX10Math) -描述四元數。
ms.assetid: e6cb45b2-3132-4315-b02d-a3dfc444f8cc
title: 'D3DXQUATERNION 結構 (D3DX10Math .h) '
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- D3DXQUATERNION
api_type:
- HeaderDef
api_location:
- D3DX10Math.h
ms.openlocfilehash: dac880607cf482b409c407b43992747af4aa39a9
ms.sourcegitcommit: 95685061d5b0333bbf9e6ebd208dde8190f97005
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 04/28/2021
ms.locfileid: "108103246"
---
# <a name="d3dxquaternion-structure-d3dx10mathh"></a><span data-ttu-id="35a61-103">D3DXQUATERNION 結構 (D3DX10Math .h) </span><span class="sxs-lookup"><span data-stu-id="35a61-103">D3DXQUATERNION structure (D3DX10Math.h)</span></span>

<span data-ttu-id="35a61-104">描述四元數。</span><span class="sxs-lookup"><span data-stu-id="35a61-104">Describes a quaternion.</span></span>

## <a name="syntax"></a><span data-ttu-id="35a61-105">語法</span><span class="sxs-lookup"><span data-stu-id="35a61-105">Syntax</span></span>


```C++
typedef struct D3DXQUATERNION {
  FLOAT x;
  FLOAT y;
  FLOAT z;
  FLOAT w;
} D3DXQUATERNION, *LPD3DXQUATERNION;
```



## <a name="members"></a><span data-ttu-id="35a61-106">成員</span><span class="sxs-lookup"><span data-stu-id="35a61-106">Members</span></span>

<dl> <dt>

<span data-ttu-id="35a61-107">**x**</span><span class="sxs-lookup"><span data-stu-id="35a61-107">**x**</span></span>
</dt> <dd>

<span data-ttu-id="35a61-108">類型： **[ **FLOAT**](../winprog/windows-data-types.md)**</span><span class="sxs-lookup"><span data-stu-id="35a61-108">Type: **[**FLOAT**](../winprog/windows-data-types.md)**</span></span>

</dd> <dd>

<span data-ttu-id="35a61-109">X 元件。</span><span class="sxs-lookup"><span data-stu-id="35a61-109">The x-component.</span></span>

</dd> <dt>

<span data-ttu-id="35a61-110">**y**</span><span class="sxs-lookup"><span data-stu-id="35a61-110">**y**</span></span>
</dt> <dd>

<span data-ttu-id="35a61-111">類型： **[ **FLOAT**](../winprog/windows-data-types.md)**</span><span class="sxs-lookup"><span data-stu-id="35a61-111">Type: **[**FLOAT**](../winprog/windows-data-types.md)**</span></span>

</dd> <dd>

<span data-ttu-id="35a61-112">Y 元件。</span><span class="sxs-lookup"><span data-stu-id="35a61-112">The y-component.</span></span>

</dd> <dt>

<span data-ttu-id="35a61-113">**Z**</span><span class="sxs-lookup"><span data-stu-id="35a61-113">**z**</span></span>
</dt> <dd>

<span data-ttu-id="35a61-114">類型： **[ **FLOAT**](../winprog/windows-data-types.md)**</span><span class="sxs-lookup"><span data-stu-id="35a61-114">Type: **[**FLOAT**](../winprog/windows-data-types.md)**</span></span>

</dd> <dd>

<span data-ttu-id="35a61-115">Z 元件。</span><span class="sxs-lookup"><span data-stu-id="35a61-115">The z-component.</span></span>

</dd> <dt>

<span data-ttu-id="35a61-116">**w**</span><span class="sxs-lookup"><span data-stu-id="35a61-116">**w**</span></span>
</dt> <dd>

<span data-ttu-id="35a61-117">類型： **[ **FLOAT**](../winprog/windows-data-types.md)**</span><span class="sxs-lookup"><span data-stu-id="35a61-117">Type: **[**FLOAT**](../winprog/windows-data-types.md)**</span></span>

</dd> <dd>

<span data-ttu-id="35a61-118">W 元件。</span><span class="sxs-lookup"><span data-stu-id="35a61-118">The w-component.</span></span>

</dd> </dl>

## <a name="remarks"></a><span data-ttu-id="35a61-119">備註</span><span class="sxs-lookup"><span data-stu-id="35a61-119">Remarks</span></span>

<span data-ttu-id="35a61-120">四元數會將第四個元素新增至 \[ 定義向量的 x、y、z \] 值，進而產生任意的4d 向量。</span><span class="sxs-lookup"><span data-stu-id="35a61-120">Quaternions add a fourth element to the \[ x, y, z\] values that define a vector, resulting in arbitrary 4D vectors.</span></span> <span data-ttu-id="35a61-121">但是，下列說明單元四元數的每個元素如何與軸角度旋轉相關聯 (其中 q 代表單位四元數 (x、y、z、w) 、軸已正規化，而 theta 則是所需的 y 軸) 的 CCW 旋轉：</span><span class="sxs-lookup"><span data-stu-id="35a61-121">However, the following illustrates how each element of a unit quaternion relates to an axis-angle rotation (where q represents a unit quaternion (x, y, z, w), axis is normalized, and theta is the desired CCW rotation about the axis):</span></span>


```
q.x = sin(theta/2) * axis.x
q.y = sin(theta/2) * axis.y
q.z = sin(theta/2) * axis.z
q.w = cos(theta/2)
```



## <a name="requirements"></a><span data-ttu-id="35a61-122">規格需求</span><span class="sxs-lookup"><span data-stu-id="35a61-122">Requirements</span></span>



| <span data-ttu-id="35a61-123">需求</span><span class="sxs-lookup"><span data-stu-id="35a61-123">Requirement</span></span> | <span data-ttu-id="35a61-124">值</span><span class="sxs-lookup"><span data-stu-id="35a61-124">Value</span></span> |
|-------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="35a61-125">標頭</span><span class="sxs-lookup"><span data-stu-id="35a61-125">Header</span></span><br/> | <dl> <span data-ttu-id="35a61-126"><dt>D3DX10Math。h</dt></span><span class="sxs-lookup"><span data-stu-id="35a61-126"><dt>D3DX10Math.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="35a61-127">另請參閱</span><span class="sxs-lookup"><span data-stu-id="35a61-127">See also</span></span>

<dl> <dt>

[<span data-ttu-id="35a61-128">D3DX 結構</span><span class="sxs-lookup"><span data-stu-id="35a61-128">D3DX Structures</span></span>](d3d10-graphics-reference-d3dx10-structures.md)
</dt> </dl>

 

 
