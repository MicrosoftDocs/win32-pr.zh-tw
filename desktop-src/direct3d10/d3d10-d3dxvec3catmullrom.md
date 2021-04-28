---
description: D3DXVec3CatmullRom 函式 (D3DX10Math) -使用指定的3D 向量執行 Catmull-Rom 插補。
ms.assetid: 324bd4b5-b0df-4dd3-b370-3c365c9f2db1
title: 'D3DXVec3CatmullRom 函式 (D3DX10Math) '
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- D3DXVec3CatmullRom
api_type:
- HeaderDef
api_location:
- D3DX10Math.h
ms.openlocfilehash: a09d61e9c43624f441975eca1a131a82f8092587
ms.sourcegitcommit: 95685061d5b0333bbf9e6ebd208dde8190f97005
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 04/28/2021
ms.locfileid: "108108216"
---
# <a name="d3dxvec3catmullrom-function-d3dx10mathh"></a><span data-ttu-id="86012-103">D3DXVec3CatmullRom 函式 (D3DX10Math) </span><span class="sxs-lookup"><span data-stu-id="86012-103">D3DXVec3CatmullRom function (D3DX10Math.h)</span></span>

<span data-ttu-id="86012-104">使用指定的3D 向量，執行 Catmull-Rom 插補。</span><span class="sxs-lookup"><span data-stu-id="86012-104">Performs a Catmull-Rom interpolation, using the specified 3D vectors.</span></span>

## <a name="syntax"></a><span data-ttu-id="86012-105">語法</span><span class="sxs-lookup"><span data-stu-id="86012-105">Syntax</span></span>


```C++
D3DXVECTOR3* D3DXVec3CatmullRom(
  _Inout_       D3DXVECTOR3 *pOut,
  _In_    const D3DXVECTOR3 *pV0,
  _In_    const D3DXVECTOR3 *pV1,
  _In_    const D3DXVECTOR3 *pV2,
  _In_    const D3DXVECTOR3 *pV3,
  _In_          FLOAT       s
);
```



## <a name="parameters"></a><span data-ttu-id="86012-106">參數</span><span class="sxs-lookup"><span data-stu-id="86012-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="86012-107">*不悅* \[in、out\]</span><span class="sxs-lookup"><span data-stu-id="86012-107">*pOut* \[in, out\]</span></span>
</dt> <dd>

<span data-ttu-id="86012-108">類型： **[ **D3DXVECTOR3**](../direct3d9/d3dxvector3.md)\***</span><span class="sxs-lookup"><span data-stu-id="86012-108">Type: **[**D3DXVECTOR3**](../direct3d9/d3dxvector3.md)\***</span></span>

<span data-ttu-id="86012-109">作業結果之 [**D3DXVECTOR3**](d3d10-d3dxvector3.md) 的指標。</span><span class="sxs-lookup"><span data-stu-id="86012-109">Pointer to the [**D3DXVECTOR3**](d3d10-d3dxvector3.md) that is the result of the operation.</span></span>

</dd> <dt>

<span data-ttu-id="86012-110">*pV0* \[在\]</span><span class="sxs-lookup"><span data-stu-id="86012-110">*pV0* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="86012-111">Type： **Const [**D3DXVECTOR3**](../direct3d9/d3dxvector3.md) \***</span><span class="sxs-lookup"><span data-stu-id="86012-111">Type: **const [**D3DXVECTOR3**](../direct3d9/d3dxvector3.md)\***</span></span>

<span data-ttu-id="86012-112">來源 D3DXVECTOR3 結構的指標，也就是位置向量。</span><span class="sxs-lookup"><span data-stu-id="86012-112">Pointer to a source D3DXVECTOR3 structure, a position vector.</span></span>

</dd> <dt>

<span data-ttu-id="86012-113">*pV1* \[在\]</span><span class="sxs-lookup"><span data-stu-id="86012-113">*pV1* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="86012-114">Type： **Const [**D3DXVECTOR3**](../direct3d9/d3dxvector3.md) \***</span><span class="sxs-lookup"><span data-stu-id="86012-114">Type: **const [**D3DXVECTOR3**](../direct3d9/d3dxvector3.md)\***</span></span>

<span data-ttu-id="86012-115">來源 D3DXVECTOR3 結構的指標，也就是位置向量。</span><span class="sxs-lookup"><span data-stu-id="86012-115">Pointer to a source D3DXVECTOR3 structure, a position vector.</span></span>

</dd> <dt>

<span data-ttu-id="86012-116">*pV2* \[在\]</span><span class="sxs-lookup"><span data-stu-id="86012-116">*pV2* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="86012-117">Type： **Const [**D3DXVECTOR3**](../direct3d9/d3dxvector3.md) \***</span><span class="sxs-lookup"><span data-stu-id="86012-117">Type: **const [**D3DXVECTOR3**](../direct3d9/d3dxvector3.md)\***</span></span>

<span data-ttu-id="86012-118">來源 D3DXVECTOR3 結構的指標，也就是位置向量。</span><span class="sxs-lookup"><span data-stu-id="86012-118">Pointer to a source D3DXVECTOR3 structure, a position vector.</span></span>

</dd> <dt>

<span data-ttu-id="86012-119">*pV3* \[在\]</span><span class="sxs-lookup"><span data-stu-id="86012-119">*pV3* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="86012-120">Type： **Const [**D3DXVECTOR3**](../direct3d9/d3dxvector3.md) \***</span><span class="sxs-lookup"><span data-stu-id="86012-120">Type: **const [**D3DXVECTOR3**](../direct3d9/d3dxvector3.md)\***</span></span>

<span data-ttu-id="86012-121">來源 D3DXVECTOR3 結構的指標，也就是位置向量。</span><span class="sxs-lookup"><span data-stu-id="86012-121">Pointer to a source D3DXVECTOR3 structure, a position vector.</span></span>

</dd> <dt>

<span data-ttu-id="86012-122"> \[ 中的 s\]</span><span class="sxs-lookup"><span data-stu-id="86012-122">*s* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="86012-123">類型： **[ **FLOAT**](../winprog/windows-data-types.md)**</span><span class="sxs-lookup"><span data-stu-id="86012-123">Type: **[**FLOAT**](../winprog/windows-data-types.md)**</span></span>

<span data-ttu-id="86012-124">加權係數。</span><span class="sxs-lookup"><span data-stu-id="86012-124">Weighting factor.</span></span> <span data-ttu-id="86012-125">請參閱＜備註＞。</span><span class="sxs-lookup"><span data-stu-id="86012-125">See Remarks.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="86012-126">傳回值</span><span class="sxs-lookup"><span data-stu-id="86012-126">Return value</span></span>

<span data-ttu-id="86012-127">類型： **[ **D3DXVECTOR3**](../direct3d9/d3dxvector3.md)\***</span><span class="sxs-lookup"><span data-stu-id="86012-127">Type: **[**D3DXVECTOR3**](../direct3d9/d3dxvector3.md)\***</span></span>

<span data-ttu-id="86012-128">D3DXVECTOR3 結構的指標，此結構是 Catmull-Rom 插補的結果。</span><span class="sxs-lookup"><span data-stu-id="86012-128">Pointer to a D3DXVECTOR3 structure that is the result of the Catmull-Rom interpolation.</span></span>

## <a name="remarks"></a><span data-ttu-id="86012-129">備註</span><span class="sxs-lookup"><span data-stu-id="86012-129">Remarks</span></span>

<span data-ttu-id="86012-130">假設有四個點 (p1、p2、p3、p4) 、找出函式 Q (s) ，如下所示：</span><span class="sxs-lookup"><span data-stu-id="86012-130">Given four points (p1, p2, p3, p4), find a function Q(s) such that:</span></span>


```
Q(s) is a cubic function. 
Q(s) interpolates between p2 and p3 as s ranges from 0 to 1. 
Q(s) is parallel to the line joining p1 to p3 when s is 0. 
Q(s) is parallel to the line joining p2 to p4 when s is 1. 
```



<span data-ttu-id="86012-131">您可以藉由設定下列各項，從 Hermite 曲線衍生出 Catmull-Rom 曲線：</span><span class="sxs-lookup"><span data-stu-id="86012-131">The Catmull-Rom spline can be derived from the Hermite spline by setting:</span></span>


```
v1 = p2
v2 = p3
t1 = (p3 - p1) / 2
t2 = (p4 - p2) / 2
```



<span data-ttu-id="86012-132">其中：</span><span class="sxs-lookup"><span data-stu-id="86012-132">where:</span></span>

<span data-ttu-id="86012-133">v1 是 pV0 的內容。</span><span class="sxs-lookup"><span data-stu-id="86012-133">v1 is the contents of pV0.</span></span>

<span data-ttu-id="86012-134">v2 是 pV1 的內容。</span><span class="sxs-lookup"><span data-stu-id="86012-134">v2 is the contents of pV1.</span></span>

<span data-ttu-id="86012-135">p3 是 pV2 的內容。</span><span class="sxs-lookup"><span data-stu-id="86012-135">p3 is the contents of pV2.</span></span>

<span data-ttu-id="86012-136">p4 是 pV3 的內容。</span><span class="sxs-lookup"><span data-stu-id="86012-136">p4 is the contents of pV3.</span></span>

<span data-ttu-id="86012-137">使用 Hermite 曲線方程式：</span><span class="sxs-lookup"><span data-stu-id="86012-137">Using the Hermite spline equation:</span></span>


```
Q(s) = (2s3 - 3s2 + 1)v1 + (-2s3 + 3s2)v2 + (s3 - 2s2 + s)t1 + (s3 - s2)t2
```



<span data-ttu-id="86012-138">而以 v1、v2、t1 替代，t2 會產生：</span><span class="sxs-lookup"><span data-stu-id="86012-138">and substituting for v1, v2, t1, t2 yields:</span></span>


```
Q(s) = (2s3 - 3s2 + 1)p2 + (-2s3 + 3s2)p3 + (s3 - 2s2 + s)(p3 - p1) / 2 + (s3 - s2)(p4 - p2) / 2
```



<span data-ttu-id="86012-139">這可以重新排列為：</span><span class="sxs-lookup"><span data-stu-id="86012-139">This can be rearranged as:</span></span>


```
Q(s) = [(-s3 + 2s2 - s)p1 + (3s3 - 5s2 + 2)p2 + (-3s3 + 4s2 + s)p3 + (s3 - s2)p4] / 2
```



## <a name="requirements"></a><span data-ttu-id="86012-140">規格需求</span><span class="sxs-lookup"><span data-stu-id="86012-140">Requirements</span></span>



| <span data-ttu-id="86012-141">需求</span><span class="sxs-lookup"><span data-stu-id="86012-141">Requirement</span></span> | <span data-ttu-id="86012-142">值</span><span class="sxs-lookup"><span data-stu-id="86012-142">Value</span></span> |
|-------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="86012-143">標頭</span><span class="sxs-lookup"><span data-stu-id="86012-143">Header</span></span><br/> | <dl> <span data-ttu-id="86012-144"><dt>D3DX10Math。h</dt></span><span class="sxs-lookup"><span data-stu-id="86012-144"><dt>D3DX10Math.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="86012-145">另請參閱</span><span class="sxs-lookup"><span data-stu-id="86012-145">See also</span></span>

<dl> <dt>

[<span data-ttu-id="86012-146">數學函數</span><span class="sxs-lookup"><span data-stu-id="86012-146">Math Functions</span></span>](d3d10-graphics-reference-d3dx10-functions-math.md)
</dt> </dl>

 

 
