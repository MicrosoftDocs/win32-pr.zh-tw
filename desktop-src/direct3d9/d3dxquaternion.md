---
description: 描述四元數。
ms.assetid: 3d88ed17-5b0a-46d5-8fe6-d66e1fa26c13
title: 'D3DXQUATERNION 結構 (D3dx9math .h) '
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
- d3dx9math.h
ms.openlocfilehash: 59d3f147e8eb233b9197394bad738d19d9ceba5d
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 03/15/2021
ms.locfileid: "106997383"
---
# <a name="d3dxquaternion-structure-d3dx9mathh"></a><span data-ttu-id="25fb0-103">D3DXQUATERNION 結構 (D3dx9math .h) </span><span class="sxs-lookup"><span data-stu-id="25fb0-103">D3DXQUATERNION structure (D3dx9math.h)</span></span>

<span data-ttu-id="25fb0-104">描述四元數。</span><span class="sxs-lookup"><span data-stu-id="25fb0-104">Describes a quaternion.</span></span>

## <a name="syntax"></a><span data-ttu-id="25fb0-105">語法</span><span class="sxs-lookup"><span data-stu-id="25fb0-105">Syntax</span></span>


```C++
typedef struct D3DXQUATERNION {
  FLOAT x;
  FLOAT y;
  FLOAT z;
  FLOAT w;
} D3DXQUATERNION, *LPD3DXQUATERNION;
```



## <a name="members"></a><span data-ttu-id="25fb0-106">成員</span><span class="sxs-lookup"><span data-stu-id="25fb0-106">Members</span></span>

<dl> <dt>

<span data-ttu-id="25fb0-107">**x**</span><span class="sxs-lookup"><span data-stu-id="25fb0-107">**x**</span></span>
</dt> <dd>

<span data-ttu-id="25fb0-108">類型： **[ **FLOAT**](../winprog/windows-data-types.md)**</span><span class="sxs-lookup"><span data-stu-id="25fb0-108">Type: **[**FLOAT**](../winprog/windows-data-types.md)**</span></span>

</dd> <dd>

<span data-ttu-id="25fb0-109">X 元件。</span><span class="sxs-lookup"><span data-stu-id="25fb0-109">The x-component.</span></span>

</dd> <dt>

<span data-ttu-id="25fb0-110">**y**</span><span class="sxs-lookup"><span data-stu-id="25fb0-110">**y**</span></span>
</dt> <dd>

<span data-ttu-id="25fb0-111">類型： **[ **FLOAT**](../winprog/windows-data-types.md)**</span><span class="sxs-lookup"><span data-stu-id="25fb0-111">Type: **[**FLOAT**](../winprog/windows-data-types.md)**</span></span>

</dd> <dd>

<span data-ttu-id="25fb0-112">Y 元件。</span><span class="sxs-lookup"><span data-stu-id="25fb0-112">The y-component.</span></span>

</dd> <dt>

<span data-ttu-id="25fb0-113">**Z**</span><span class="sxs-lookup"><span data-stu-id="25fb0-113">**z**</span></span>
</dt> <dd>

<span data-ttu-id="25fb0-114">類型： **[ **FLOAT**](../winprog/windows-data-types.md)**</span><span class="sxs-lookup"><span data-stu-id="25fb0-114">Type: **[**FLOAT**](../winprog/windows-data-types.md)**</span></span>

</dd> <dd>

<span data-ttu-id="25fb0-115">Z 元件。</span><span class="sxs-lookup"><span data-stu-id="25fb0-115">The z-component.</span></span>

</dd> <dt>

<span data-ttu-id="25fb0-116">**w**</span><span class="sxs-lookup"><span data-stu-id="25fb0-116">**w**</span></span>
</dt> <dd>

<span data-ttu-id="25fb0-117">類型： **[ **FLOAT**](../winprog/windows-data-types.md)**</span><span class="sxs-lookup"><span data-stu-id="25fb0-117">Type: **[**FLOAT**](../winprog/windows-data-types.md)**</span></span>

</dd> <dd>

<span data-ttu-id="25fb0-118">W 元件。</span><span class="sxs-lookup"><span data-stu-id="25fb0-118">The w-component.</span></span>

</dd> </dl>

## <a name="remarks"></a><span data-ttu-id="25fb0-119">備註</span><span class="sxs-lookup"><span data-stu-id="25fb0-119">Remarks</span></span>

<span data-ttu-id="25fb0-120">四元數會將第四個元素新增至 \[ 定義向量的 x、y、z \] 值，進而產生任意的4d 向量。</span><span class="sxs-lookup"><span data-stu-id="25fb0-120">Quaternions add a fourth element to the \[ x, y, z\] values that define a vector, resulting in arbitrary 4D vectors.</span></span> <span data-ttu-id="25fb0-121">但是，下列說明單元四元數的每個元素如何與軸角度旋轉相關聯 (其中 q 代表單位四元數 (x、y、z、w) 、軸已正規化，而 theta 則是所需的 y 軸) 的 CCW 旋轉：</span><span class="sxs-lookup"><span data-stu-id="25fb0-121">However, the following illustrates how each element of a unit quaternion relates to an axis-angle rotation (where q represents a unit quaternion (x, y, z, w), axis is normalized, and theta is the desired CCW rotation about the axis):</span></span>


```
q.x = sin(theta/2) * axis.x
q.y = sin(theta/2) * axis.y
q.z = sin(theta/2) * axis.z
q.w = cos(theta/2)
```



<span data-ttu-id="25fb0-122">C + + 程式設計人員可以利用 [**D3DXQUATERNION 擴充**](d3dxquaternion-extensions.md)功能來利用運算子多載和類型轉換，以執行多載的函式和指派、一元和二元 (，包括相等) 運算子。</span><span class="sxs-lookup"><span data-stu-id="25fb0-122">C++ programmers can take advantage of operator overloading and type casting with the [**D3DXQUATERNION Extensions**](d3dxquaternion-extensions.md), which implement overloaded constructors and assignment, unary, and binary (including equality) operators.</span></span>

## <a name="requirements"></a><span data-ttu-id="25fb0-123">規格需求</span><span class="sxs-lookup"><span data-stu-id="25fb0-123">Requirements</span></span>



| <span data-ttu-id="25fb0-124">需求</span><span class="sxs-lookup"><span data-stu-id="25fb0-124">Requirement</span></span> | <span data-ttu-id="25fb0-125">值</span><span class="sxs-lookup"><span data-stu-id="25fb0-125">Value</span></span> |
|-------------------|----------------------------------------------------------------------------------------|
| <span data-ttu-id="25fb0-126">標頭</span><span class="sxs-lookup"><span data-stu-id="25fb0-126">Header</span></span><br/> | <dl> <span data-ttu-id="25fb0-127"><dt>D3dx9math。h</dt></span><span class="sxs-lookup"><span data-stu-id="25fb0-127"><dt>D3dx9math.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="25fb0-128">另請參閱</span><span class="sxs-lookup"><span data-stu-id="25fb0-128">See also</span></span>

<dl> <dt>

[<span data-ttu-id="25fb0-129">D3DX 結構</span><span class="sxs-lookup"><span data-stu-id="25fb0-129">D3DX Structures</span></span>](dx9-graphics-reference-d3dx-structures.md)
</dt> <dt>

[<span data-ttu-id="25fb0-130"> (Direct3D 9 的向量、頂點和四元數) </span><span class="sxs-lookup"><span data-stu-id="25fb0-130">Vectors, Vertices, and Quaternions (Direct3D 9)</span></span>](vectors--vertices--and-quaternions.md)
</dt> </dl>

 

 
