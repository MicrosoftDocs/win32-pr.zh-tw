---
description: 採用兩個2D 向量的交叉乘積來傳回 z 元件。
ms.assetid: daec19f2-cd0f-4a68-affc-9a42bda8912c
title: 'D3DXVec2CCW 函式 (D3dx9math) '
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- D3DXVec2CCW
api_type:
- LibDef
api_location:
- d3dx9.lib
- d3dx9.dll
ms.openlocfilehash: 71c6e14171a9e7d12d86c30f05885cecf50ce973
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 03/15/2021
ms.locfileid: "106982878"
---
# <a name="d3dxvec2ccw-function"></a><span data-ttu-id="9376d-103">D3DXVec2CCW 函式</span><span class="sxs-lookup"><span data-stu-id="9376d-103">D3DXVec2CCW function</span></span>

<span data-ttu-id="9376d-104">採用兩個2D 向量的交叉乘積來傳回 z 元件。</span><span class="sxs-lookup"><span data-stu-id="9376d-104">Returns the z-component by taking the cross product of two 2D vectors.</span></span>

## <a name="syntax"></a><span data-ttu-id="9376d-105">語法</span><span class="sxs-lookup"><span data-stu-id="9376d-105">Syntax</span></span>


```C++
FLOAT D3DXVec2CCW(
  _In_ const D3DXVECTOR2 *pV1,
  _In_ const D3DXVECTOR2 *pV2
);
```



## <a name="parameters"></a><span data-ttu-id="9376d-106">參數</span><span class="sxs-lookup"><span data-stu-id="9376d-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="9376d-107">*pV1* \[在\]</span><span class="sxs-lookup"><span data-stu-id="9376d-107">*pV1* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="9376d-108">Type： **Const [**D3DXVECTOR2**](d3dxvector2.md) \***</span><span class="sxs-lookup"><span data-stu-id="9376d-108">Type: **const [**D3DXVECTOR2**](d3dxvector2.md)\***</span></span>

<span data-ttu-id="9376d-109">來源 [**D3DXVECTOR2**](d3dxvector2.md) 結構的指標。</span><span class="sxs-lookup"><span data-stu-id="9376d-109">Pointer to a source [**D3DXVECTOR2**](d3dxvector2.md) structure.</span></span>

</dd> <dt>

<span data-ttu-id="9376d-110">*pV2* \[在\]</span><span class="sxs-lookup"><span data-stu-id="9376d-110">*pV2* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="9376d-111">Type： **Const [**D3DXVECTOR2**](d3dxvector2.md) \***</span><span class="sxs-lookup"><span data-stu-id="9376d-111">Type: **const [**D3DXVECTOR2**](d3dxvector2.md)\***</span></span>

<span data-ttu-id="9376d-112">來源 [**D3DXVECTOR2**](d3dxvector2.md) 結構的指標。</span><span class="sxs-lookup"><span data-stu-id="9376d-112">Pointer to a source [**D3DXVECTOR2**](d3dxvector2.md) structure.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="9376d-113">傳回值</span><span class="sxs-lookup"><span data-stu-id="9376d-113">Return value</span></span>

<span data-ttu-id="9376d-114">類型： **[ **FLOAT**](../winprog/windows-data-types.md)**</span><span class="sxs-lookup"><span data-stu-id="9376d-114">Type: **[**FLOAT**](../winprog/windows-data-types.md)**</span></span>

<span data-ttu-id="9376d-115">Z 元件。</span><span class="sxs-lookup"><span data-stu-id="9376d-115">The z-component.</span></span>

## <a name="remarks"></a><span data-ttu-id="9376d-116">備註</span><span class="sxs-lookup"><span data-stu-id="9376d-116">Remarks</span></span>

<span data-ttu-id="9376d-117">此函式會根據下列公式來判斷交叉乘積，以決定 z 元件： ( (x1、y1、0) cross (x2、y2、0) ) 。</span><span class="sxs-lookup"><span data-stu-id="9376d-117">This function determines the z-component by determining the cross-product based on the following formula: ((x1,y1,0) cross (x2,y2,0)).</span></span> <span data-ttu-id="9376d-118">或者，如下列範例所示。</span><span class="sxs-lookup"><span data-stu-id="9376d-118">Or as shown in the following example.</span></span>


```
pV1->x * pV2->y - pV1->y * pV2->x
```



<span data-ttu-id="9376d-119">如果 z 元件的值是正數，則向量 V2 會從向量 V1 中逆時針。</span><span class="sxs-lookup"><span data-stu-id="9376d-119">If the value of the z-component is positive, the vector V2 is counterclockwise from the vector V1.</span></span> <span data-ttu-id="9376d-120">這項資訊適用于背面的挑選。</span><span class="sxs-lookup"><span data-stu-id="9376d-120">This information is useful for back-face culling.</span></span>

## <a name="requirements"></a><span data-ttu-id="9376d-121">規格需求</span><span class="sxs-lookup"><span data-stu-id="9376d-121">Requirements</span></span>



| <span data-ttu-id="9376d-122">需求</span><span class="sxs-lookup"><span data-stu-id="9376d-122">Requirement</span></span> | <span data-ttu-id="9376d-123">值</span><span class="sxs-lookup"><span data-stu-id="9376d-123">Value</span></span> |
|--------------------|----------------------------------------------------------------------------------------|
| <span data-ttu-id="9376d-124">標頭</span><span class="sxs-lookup"><span data-stu-id="9376d-124">Header</span></span><br/>  | <dl> <span data-ttu-id="9376d-125"><dt>D3dx9math。h</dt></span><span class="sxs-lookup"><span data-stu-id="9376d-125"><dt>D3dx9math.h</dt></span></span> </dl> |
| <span data-ttu-id="9376d-126">程式庫</span><span class="sxs-lookup"><span data-stu-id="9376d-126">Library</span></span><br/> | <dl> <span data-ttu-id="9376d-127"><dt>D3dx9 .lib</dt></span><span class="sxs-lookup"><span data-stu-id="9376d-127"><dt>D3dx9.lib</dt></span></span> </dl>   |



## <a name="see-also"></a><span data-ttu-id="9376d-128">另請參閱</span><span class="sxs-lookup"><span data-stu-id="9376d-128">See also</span></span>

<dl> <dt>

[<span data-ttu-id="9376d-129">數學函數</span><span class="sxs-lookup"><span data-stu-id="9376d-129">Math Functions</span></span>](dx9-graphics-reference-d3dx-functions-math.md)
</dt> <dt>

[<span data-ttu-id="9376d-130">**D3DXVec2Dot**</span><span class="sxs-lookup"><span data-stu-id="9376d-130">**D3DXVec2Dot**</span></span>](d3dxvec2dot.md)
</dt> </dl>

 

 
