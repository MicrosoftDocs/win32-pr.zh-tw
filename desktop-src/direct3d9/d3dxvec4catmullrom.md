---
description: D3DXVec4CatmullRom 函式 (D3dx9math) -使用指定的4D 向量執行 Catmull-Rom 插補。
ms.assetid: 24c26e70-b02c-4621-8b7e-db16f99dddb5
title: 'D3DXVec4CatmullRom 函式 (D3dx9math) '
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- D3DXVec4CatmullRom
api_type:
- LibDef
api_location:
- d3dx9.lib
- d3dx9.dll
ms.openlocfilehash: 06ba24374ee2ad4e6fd008d90c55d2990dc166f6
ms.sourcegitcommit: 95685061d5b0333bbf9e6ebd208dde8190f97005
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 04/28/2021
ms.locfileid: "108115526"
---
# <a name="d3dxvec4catmullrom-function-d3dx9mathh"></a><span data-ttu-id="8fb9b-103">D3DXVec4CatmullRom 函式 (D3dx9math) </span><span class="sxs-lookup"><span data-stu-id="8fb9b-103">D3DXVec4CatmullRom function (D3dx9math.h)</span></span>

<span data-ttu-id="8fb9b-104">使用指定的4D 向量，執行 Catmull-Rom 插補。</span><span class="sxs-lookup"><span data-stu-id="8fb9b-104">Performs a Catmull-Rom interpolation, using the specified 4D vectors.</span></span>

## <a name="syntax"></a><span data-ttu-id="8fb9b-105">語法</span><span class="sxs-lookup"><span data-stu-id="8fb9b-105">Syntax</span></span>


```C++
D3DXVECTOR4* D3DXVec4CatmullRom(
  _Inout_       D3DXVECTOR4 *pOut,
  _In_    const D3DXVECTOR4 *pV0,
  _In_    const D3DXVECTOR4 *pV1,
  _In_    const D3DXVECTOR4 *pV2,
  _In_    const D3DXVECTOR4 *pV3,
  _In_          FLOAT       s
);
```



## <a name="parameters"></a><span data-ttu-id="8fb9b-106">參數</span><span class="sxs-lookup"><span data-stu-id="8fb9b-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="8fb9b-107">*不悅* \[in、out\]</span><span class="sxs-lookup"><span data-stu-id="8fb9b-107">*pOut* \[in, out\]</span></span>
</dt> <dd>

<span data-ttu-id="8fb9b-108">類型： **[ **D3DXVECTOR4**](d3dxvector4.md)\***</span><span class="sxs-lookup"><span data-stu-id="8fb9b-108">Type: **[**D3DXVECTOR4**](d3dxvector4.md)\***</span></span>

<span data-ttu-id="8fb9b-109">[**D3DXVECTOR4**](d3dxvector4.md)結構的指標，此結構是作業的結果。</span><span class="sxs-lookup"><span data-stu-id="8fb9b-109">Pointer to the [**D3DXVECTOR4**](d3dxvector4.md) structure that is the result of the operation.</span></span>

</dd> <dt>

<span data-ttu-id="8fb9b-110">*pV0* \[在\]</span><span class="sxs-lookup"><span data-stu-id="8fb9b-110">*pV0* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="8fb9b-111">Type： **Const [**D3DXVECTOR4**](d3dxvector4.md) \***</span><span class="sxs-lookup"><span data-stu-id="8fb9b-111">Type: **const [**D3DXVECTOR4**](d3dxvector4.md)\***</span></span>

<span data-ttu-id="8fb9b-112">來源 [**D3DXVECTOR4**](d3dxvector4.md) 結構的指標，也就是位置向量。</span><span class="sxs-lookup"><span data-stu-id="8fb9b-112">Pointer to a source [**D3DXVECTOR4**](d3dxvector4.md) structure, a position vector.</span></span>

</dd> <dt>

<span data-ttu-id="8fb9b-113">*pV1* \[在\]</span><span class="sxs-lookup"><span data-stu-id="8fb9b-113">*pV1* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="8fb9b-114">Type： **Const [**D3DXVECTOR4**](d3dxvector4.md) \***</span><span class="sxs-lookup"><span data-stu-id="8fb9b-114">Type: **const [**D3DXVECTOR4**](d3dxvector4.md)\***</span></span>

<span data-ttu-id="8fb9b-115">來源 [**D3DXVECTOR4**](d3dxvector4.md) 結構的指標，也就是位置向量。</span><span class="sxs-lookup"><span data-stu-id="8fb9b-115">Pointer to a source [**D3DXVECTOR4**](d3dxvector4.md) structure, a position vector.</span></span>

</dd> <dt>

<span data-ttu-id="8fb9b-116">*pV2* \[在\]</span><span class="sxs-lookup"><span data-stu-id="8fb9b-116">*pV2* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="8fb9b-117">Type： **Const [**D3DXVECTOR4**](d3dxvector4.md) \***</span><span class="sxs-lookup"><span data-stu-id="8fb9b-117">Type: **const [**D3DXVECTOR4**](d3dxvector4.md)\***</span></span>

<span data-ttu-id="8fb9b-118">來源 [**D3DXVECTOR4**](d3dxvector4.md) 結構的指標，也就是位置向量。</span><span class="sxs-lookup"><span data-stu-id="8fb9b-118">Pointer to a source [**D3DXVECTOR4**](d3dxvector4.md) structure, a position vector.</span></span>

</dd> <dt>

<span data-ttu-id="8fb9b-119">*pV3* \[在\]</span><span class="sxs-lookup"><span data-stu-id="8fb9b-119">*pV3* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="8fb9b-120">Type： **Const [**D3DXVECTOR4**](d3dxvector4.md) \***</span><span class="sxs-lookup"><span data-stu-id="8fb9b-120">Type: **const [**D3DXVECTOR4**](d3dxvector4.md)\***</span></span>

<span data-ttu-id="8fb9b-121">來源 [**D3DXVECTOR4**](d3dxvector4.md) 結構的指標，也就是位置向量。</span><span class="sxs-lookup"><span data-stu-id="8fb9b-121">Pointer to a source [**D3DXVECTOR4**](d3dxvector4.md) structure, a position vector.</span></span>

</dd> <dt>

<span data-ttu-id="8fb9b-122"> \[ 中的 s\]</span><span class="sxs-lookup"><span data-stu-id="8fb9b-122">*s* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="8fb9b-123">類型： **[ **FLOAT**](../winprog/windows-data-types.md)**</span><span class="sxs-lookup"><span data-stu-id="8fb9b-123">Type: **[**FLOAT**](../winprog/windows-data-types.md)**</span></span>

<span data-ttu-id="8fb9b-124">加權係數。</span><span class="sxs-lookup"><span data-stu-id="8fb9b-124">Weighting factor.</span></span> <span data-ttu-id="8fb9b-125">請參閱＜備註＞。</span><span class="sxs-lookup"><span data-stu-id="8fb9b-125">See Remarks.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="8fb9b-126">傳回值</span><span class="sxs-lookup"><span data-stu-id="8fb9b-126">Return value</span></span>

<span data-ttu-id="8fb9b-127">類型： **[ **D3DXVECTOR4**](d3dxvector4.md)\***</span><span class="sxs-lookup"><span data-stu-id="8fb9b-127">Type: **[**D3DXVECTOR4**](d3dxvector4.md)\***</span></span>

<span data-ttu-id="8fb9b-128">[**D3DXVECTOR4**](d3dxvector4.md)結構的指標，此結構是 Catmull-Rom 插補的結果。</span><span class="sxs-lookup"><span data-stu-id="8fb9b-128">Pointer to a [**D3DXVECTOR4**](d3dxvector4.md) structure that is the result of the Catmull-Rom interpolation.</span></span>

## <a name="remarks"></a><span data-ttu-id="8fb9b-129">備註</span><span class="sxs-lookup"><span data-stu-id="8fb9b-129">Remarks</span></span>

<span data-ttu-id="8fb9b-130">假設有四個點 (p1、p2、p3、p4) 、找出函式 Q (s) ，如下所示：</span><span class="sxs-lookup"><span data-stu-id="8fb9b-130">Given four points (p1, p2, p3, p4), find a function Q(s) such that:</span></span>


```
Q(s) is a cubic function. 
Q(s) interpolates between p2 and p3 as s ranges from 0 to 1. 
Q(s) is parallel to the line joining p1 to p3 when s is 0. 
Q(s) is parallel to the line joining p2 to p4 when s is 1. 
```



<span data-ttu-id="8fb9b-131">您可以藉由設定下列各項，從 Hermite 曲線衍生出 Catmull-Rom 曲線：</span><span class="sxs-lookup"><span data-stu-id="8fb9b-131">The Catmull-Rom spline can be derived from the Hermite spline by setting:</span></span>


```
v1 = p2
v2 = p3
t1 = (p3 - p1) / 2
t2 = (p4 - p2) / 2
```



<span data-ttu-id="8fb9b-132">其中：</span><span class="sxs-lookup"><span data-stu-id="8fb9b-132">where:</span></span>

<span data-ttu-id="8fb9b-133">v1 是 pV0 的內容。</span><span class="sxs-lookup"><span data-stu-id="8fb9b-133">v1 is the contents of pV0.</span></span>

<span data-ttu-id="8fb9b-134">pV1 內容中的 v2。</span><span class="sxs-lookup"><span data-stu-id="8fb9b-134">v2 in the contents of pV1.</span></span>

<span data-ttu-id="8fb9b-135">p3 是 pV2 的內容。</span><span class="sxs-lookup"><span data-stu-id="8fb9b-135">p3 is the contents of pV2.</span></span>

<span data-ttu-id="8fb9b-136">p4 是 pV3 的內容。</span><span class="sxs-lookup"><span data-stu-id="8fb9b-136">p4 is the contents of pV3.</span></span>

<span data-ttu-id="8fb9b-137">使用 Hermite 曲線方程式：</span><span class="sxs-lookup"><span data-stu-id="8fb9b-137">Using the Hermite spline equation:</span></span>


```
Q(s) = (2s3 - 3s2 + 1)v1 + (-2s3 + 3s2)v2 + (s3 - 2s2 + s)t1 + (s3 - s2)t2
```



<span data-ttu-id="8fb9b-138">而以 v1、v2、t1 替代，t2 會產生：</span><span class="sxs-lookup"><span data-stu-id="8fb9b-138">and substituting for v1, v2, t1, t2 yields:</span></span>


```
Q(s) = (2s3 - 3s2 + 1)p2 + (-2s3 + 3s2)p3 + (s3 - 2s2 + s)(p3 - p1) / 2 + (s3 - s2)(p4 - p2) / 2
```



<span data-ttu-id="8fb9b-139">這可以重新排列為：</span><span class="sxs-lookup"><span data-stu-id="8fb9b-139">This can be rearranged as:</span></span>


```
Q(s) = [(-s3 + 2s2 - s)p1 + (3s3 - 5s2 + 2)p2 + (-3s3 + 4s2 + s)p3 + (s3 - s2)p4] / 2
```



## <a name="requirements"></a><span data-ttu-id="8fb9b-140">規格需求</span><span class="sxs-lookup"><span data-stu-id="8fb9b-140">Requirements</span></span>



| <span data-ttu-id="8fb9b-141">需求</span><span class="sxs-lookup"><span data-stu-id="8fb9b-141">Requirement</span></span> | <span data-ttu-id="8fb9b-142">值</span><span class="sxs-lookup"><span data-stu-id="8fb9b-142">Value</span></span> |
|--------------------|----------------------------------------------------------------------------------------|
| <span data-ttu-id="8fb9b-143">標頭</span><span class="sxs-lookup"><span data-stu-id="8fb9b-143">Header</span></span><br/>  | <dl> <span data-ttu-id="8fb9b-144"><dt>D3dx9math。h</dt></span><span class="sxs-lookup"><span data-stu-id="8fb9b-144"><dt>D3dx9math.h</dt></span></span> </dl> |
| <span data-ttu-id="8fb9b-145">程式庫</span><span class="sxs-lookup"><span data-stu-id="8fb9b-145">Library</span></span><br/> | <dl> <span data-ttu-id="8fb9b-146"><dt>D3dx9 .lib</dt></span><span class="sxs-lookup"><span data-stu-id="8fb9b-146"><dt>D3dx9.lib</dt></span></span> </dl>   |



## <a name="see-also"></a><span data-ttu-id="8fb9b-147">另請參閱</span><span class="sxs-lookup"><span data-stu-id="8fb9b-147">See also</span></span>

<dl> <dt>

[<span data-ttu-id="8fb9b-148">數學函數</span><span class="sxs-lookup"><span data-stu-id="8fb9b-148">Math Functions</span></span>](dx9-graphics-reference-d3dx-functions-math.md)
</dt> <dt>

[<span data-ttu-id="8fb9b-149">**D3DXVec2CatmullRom**</span><span class="sxs-lookup"><span data-stu-id="8fb9b-149">**D3DXVec2CatmullRom**</span></span>](d3dxvec2catmullrom.md)
</dt> <dt>

[<span data-ttu-id="8fb9b-150">**D3DXVec3CatmullRom**</span><span class="sxs-lookup"><span data-stu-id="8fb9b-150">**D3DXVec3CatmullRom**</span></span>](d3dxvec3catmullrom.md)
</dt> </dl>

 

 
