---
description: 使用指定的4D 向量執行 Hermite 曲線插補。
ms.assetid: 687d4dcf-ee75-4dda-b6d2-5ba0b5281a64
title: 'D3DXVec4Hermite 函式 (D3dx9math) '
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- D3DXVec4Hermite
api_type:
- LibDef
api_location:
- d3dx9.lib
- d3dx9.dll
ms.openlocfilehash: 85cf60150606a37c2e68ebf72bd4a3772d346660
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 03/15/2021
ms.locfileid: "104196295"
---
# <a name="d3dxvec4hermite-function-d3dx9mathh"></a><span data-ttu-id="8197d-103">D3DXVec4Hermite 函式 (D3dx9math) </span><span class="sxs-lookup"><span data-stu-id="8197d-103">D3DXVec4Hermite function (D3dx9math.h)</span></span>

<span data-ttu-id="8197d-104">使用指定的4D 向量執行 Hermite 曲線插補。</span><span class="sxs-lookup"><span data-stu-id="8197d-104">Performs a Hermite spline interpolation, using the specified 4D vectors.</span></span>

## <a name="syntax"></a><span data-ttu-id="8197d-105">語法</span><span class="sxs-lookup"><span data-stu-id="8197d-105">Syntax</span></span>


```C++
D3DXVECTOR4* D3DXVec4Hermite(
  _Inout_       D3DXVECTOR4 *pOut,
  _In_    const D3DXVECTOR4 *pV1,
  _In_    const D3DXVECTOR4 *pT1,
  _In_    const D3DXVECTOR4 *pV2,
  _In_    const D3DXVECTOR4 *pT2,
  _In_          FLOAT       s
);
```



## <a name="parameters"></a><span data-ttu-id="8197d-106">參數</span><span class="sxs-lookup"><span data-stu-id="8197d-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="8197d-107">*不悅* \[in、out\]</span><span class="sxs-lookup"><span data-stu-id="8197d-107">*pOut* \[in, out\]</span></span>
</dt> <dd>

<span data-ttu-id="8197d-108">類型： **[ **D3DXVECTOR4**](d3dxvector4.md)\***</span><span class="sxs-lookup"><span data-stu-id="8197d-108">Type: **[**D3DXVECTOR4**](d3dxvector4.md)\***</span></span>

<span data-ttu-id="8197d-109">[**D3DXVECTOR4**](d3dxvector4.md)結構的指標，此結構是作業的結果。</span><span class="sxs-lookup"><span data-stu-id="8197d-109">Pointer to the [**D3DXVECTOR4**](d3dxvector4.md) structure that is the result of the operation.</span></span>

</dd> <dt>

<span data-ttu-id="8197d-110">*pV1* \[在\]</span><span class="sxs-lookup"><span data-stu-id="8197d-110">*pV1* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="8197d-111">Type： **Const [**D3DXVECTOR4**](d3dxvector4.md) \***</span><span class="sxs-lookup"><span data-stu-id="8197d-111">Type: **const [**D3DXVECTOR4**](d3dxvector4.md)\***</span></span>

<span data-ttu-id="8197d-112">來源 [**D3DXVECTOR4**](d3dxvector4.md) 結構的指標，也就是位置向量。</span><span class="sxs-lookup"><span data-stu-id="8197d-112">Pointer to a source [**D3DXVECTOR4**](d3dxvector4.md) structure, a position vector.</span></span>

</dd> <dt>

<span data-ttu-id="8197d-113">*pT1* \[在\]</span><span class="sxs-lookup"><span data-stu-id="8197d-113">*pT1* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="8197d-114">Type： **Const [**D3DXVECTOR4**](d3dxvector4.md) \***</span><span class="sxs-lookup"><span data-stu-id="8197d-114">Type: **const [**D3DXVECTOR4**](d3dxvector4.md)\***</span></span>

<span data-ttu-id="8197d-115">來源 [**D3DXVECTOR4**](d3dxvector4.md) 結構的指標，也就是正切向量。</span><span class="sxs-lookup"><span data-stu-id="8197d-115">Pointer to a source [**D3DXVECTOR4**](d3dxvector4.md) structure, a tangent vector.</span></span>

</dd> <dt>

<span data-ttu-id="8197d-116">*pV2* \[在\]</span><span class="sxs-lookup"><span data-stu-id="8197d-116">*pV2* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="8197d-117">Type： **Const [**D3DXVECTOR4**](d3dxvector4.md) \***</span><span class="sxs-lookup"><span data-stu-id="8197d-117">Type: **const [**D3DXVECTOR4**](d3dxvector4.md)\***</span></span>

<span data-ttu-id="8197d-118">來源 [**D3DXVECTOR4**](d3dxvector4.md) 結構的指標，也就是位置向量。</span><span class="sxs-lookup"><span data-stu-id="8197d-118">Pointer to a source [**D3DXVECTOR4**](d3dxvector4.md) structure, a position vector.</span></span>

</dd> <dt>

<span data-ttu-id="8197d-119">*pT2* \[在\]</span><span class="sxs-lookup"><span data-stu-id="8197d-119">*pT2* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="8197d-120">Type： **Const [**D3DXVECTOR4**](d3dxvector4.md) \***</span><span class="sxs-lookup"><span data-stu-id="8197d-120">Type: **const [**D3DXVECTOR4**](d3dxvector4.md)\***</span></span>

<span data-ttu-id="8197d-121">來源 [**D3DXVECTOR4**](d3dxvector4.md) 結構的指標，也就是正切向量。</span><span class="sxs-lookup"><span data-stu-id="8197d-121">Pointer to a source [**D3DXVECTOR4**](d3dxvector4.md) structure, a tangent vector.</span></span>

</dd> <dt>

<span data-ttu-id="8197d-122"> \[ 中的 s\]</span><span class="sxs-lookup"><span data-stu-id="8197d-122">*s* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="8197d-123">類型： **[ **FLOAT**](../winprog/windows-data-types.md)**</span><span class="sxs-lookup"><span data-stu-id="8197d-123">Type: **[**FLOAT**](../winprog/windows-data-types.md)**</span></span>

<span data-ttu-id="8197d-124">加權係數。</span><span class="sxs-lookup"><span data-stu-id="8197d-124">Weighting factor.</span></span> <span data-ttu-id="8197d-125">請參閱＜備註＞。</span><span class="sxs-lookup"><span data-stu-id="8197d-125">See Remarks.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="8197d-126">傳回值</span><span class="sxs-lookup"><span data-stu-id="8197d-126">Return value</span></span>

<span data-ttu-id="8197d-127">類型： **[ **D3DXVECTOR4**](d3dxvector4.md)\***</span><span class="sxs-lookup"><span data-stu-id="8197d-127">Type: **[**D3DXVECTOR4**](d3dxvector4.md)\***</span></span>

<span data-ttu-id="8197d-128">[**D3DXVECTOR4**](d3dxvector4.md)結構的指標，此結構是 Hermite 曲線插補的結果。</span><span class="sxs-lookup"><span data-stu-id="8197d-128">Pointer to a [**D3DXVECTOR4**](d3dxvector4.md) structure that is the result of the Hermite spline interpolation.</span></span>

## <a name="remarks"></a><span data-ttu-id="8197d-129">備註</span><span class="sxs-lookup"><span data-stu-id="8197d-129">Remarks</span></span>

<span data-ttu-id="8197d-130">**D3DXVec4Hermite** 函式會將 (PositionA、tangentA) 從 (PositionB、tangentB) （使用 Hermite 曲線插補）進行插補。</span><span class="sxs-lookup"><span data-stu-id="8197d-130">The **D3DXVec4Hermite** function interpolates from (positionA, tangentA) to (positionB, tangentB) using Hermite spline interpolation.</span></span>

<span data-ttu-id="8197d-131">曲線插補是一種容易簡化的曲線一般化。</span><span class="sxs-lookup"><span data-stu-id="8197d-131">The spline interpolation is a generalization of the ease-in, ease-out spline.</span></span> <span data-ttu-id="8197d-132">此曲線是 Q (s 的函式) 具有下列屬性。</span><span class="sxs-lookup"><span data-stu-id="8197d-132">The ramp is a function of Q(s) with the following properties.</span></span>

<span data-ttu-id="8197d-133">Q (s) = ³ + Bs ² + Cs + D (因此，Q ' (s) = 3 ² + 2Bs + C) </span><span class="sxs-lookup"><span data-stu-id="8197d-133">Q(s) = As³ + Bs² + Cs + D (and therefore, Q'(s) = 3As² + 2Bs + C)</span></span>

<span data-ttu-id="8197d-134">a) Q (0) = v1，所以 Q ' (0) = t1</span><span class="sxs-lookup"><span data-stu-id="8197d-134">a) Q(0) = v1, so Q'(0) = t1</span></span>

<span data-ttu-id="8197d-135">b) Q (1) = v2，因此 Q ' (1) = t2</span><span class="sxs-lookup"><span data-stu-id="8197d-135">b) Q(1) = v2, so Q'(1) = t2</span></span>

<span data-ttu-id="8197d-136">v1 是 pV1 的內容，v2 在 pV2 的內容中，t1 是 pT1 的內容，而 t2 是 pT2 的內容。</span><span class="sxs-lookup"><span data-stu-id="8197d-136">v1 is the contents of pV1, v2 in the contents of pV2, t1 is the contents of pT1, and t2 is the contents of pT2.</span></span>

<span data-ttu-id="8197d-137">這些屬性是用來解決 A、B、C、D。</span><span class="sxs-lookup"><span data-stu-id="8197d-137">These properties are used to solve for A, B, C, D.</span></span>

<span data-ttu-id="8197d-138">插入 A、B、C 和 D 的解決方案，以產生 Q (s) 。</span><span class="sxs-lookup"><span data-stu-id="8197d-138">Plug in the solutions for A,B,C and D to generate Q(s).</span></span>

``` syntax
A = 2v1 - 2v2 + t2 + t1 
B = 3v2 - 3v1 - 2t1 - t2
C = t1 
D = v1
```

<span data-ttu-id="8197d-139">這會產生：</span><span class="sxs-lookup"><span data-stu-id="8197d-139">This yields:</span></span>

<span data-ttu-id="8197d-140">Q (s) = (2v1-2v2 + t2 + t1) s ³ + (3v2-3v1-2t1-t2) s ² + t1s + v1</span><span class="sxs-lookup"><span data-stu-id="8197d-140">Q(s) = (2v1 - 2v2 + t2 + t1)s³ + (3v2 - 3v1 - 2t1 - t2)s² + t1s + v1</span></span>

<span data-ttu-id="8197d-141">可以重新排列為：</span><span class="sxs-lookup"><span data-stu-id="8197d-141">Which can be rearranged as:</span></span>

<span data-ttu-id="8197d-142">Q (s) = (2 秒³-3 秒² + 1) v1 + (-2 ³ + 3 秒²) v2 + (s ³-2-2 ² + s) t1 + (s ³-s ²) t2</span><span class="sxs-lookup"><span data-stu-id="8197d-142">Q(s) = (2s³ - 3s² + 1)v1 + (-2s³ + 3s²)v2 + (s³ - 2s² + s)t1 + (s³ - s²)t2</span></span>

<span data-ttu-id="8197d-143">Hermite 曲線適合用來控制動畫，因為曲線會透過所有控制點來執行。</span><span class="sxs-lookup"><span data-stu-id="8197d-143">Hermite splines are useful for controlling animation because the curve runs through all the control points.</span></span> <span data-ttu-id="8197d-144">此外，因為位置和正切函數是在每個區段的結尾明確指定，所以只要您確定起始位置和正切值符合最後一個區段的結束值，就很容易建立 C2 連續曲線。</span><span class="sxs-lookup"><span data-stu-id="8197d-144">Also, because the position and tangent are explicitly specified at the ends of each segment, it is easy to create a C2 continuous curve as long as you make sure that your starting position and tangent match the ending values of the last segment.</span></span>

<span data-ttu-id="8197d-145">此函式的傳回值與不悅參數中所傳回的值相同。</span><span class="sxs-lookup"><span data-stu-id="8197d-145">The return value for this function is the same value returned in the pOut parameter.</span></span> <span data-ttu-id="8197d-146">如此一來， **D3DXVec4Hermite** 函式就可以用來做為另一個函式的參數。</span><span class="sxs-lookup"><span data-stu-id="8197d-146">In this way, the **D3DXVec4Hermite** function can be used as a parameter for another function.</span></span>

## <a name="requirements"></a><span data-ttu-id="8197d-147">規格需求</span><span class="sxs-lookup"><span data-stu-id="8197d-147">Requirements</span></span>



| <span data-ttu-id="8197d-148">需求</span><span class="sxs-lookup"><span data-stu-id="8197d-148">Requirement</span></span> | <span data-ttu-id="8197d-149">值</span><span class="sxs-lookup"><span data-stu-id="8197d-149">Value</span></span> |
|--------------------|----------------------------------------------------------------------------------------|
| <span data-ttu-id="8197d-150">標頭</span><span class="sxs-lookup"><span data-stu-id="8197d-150">Header</span></span><br/>  | <dl> <span data-ttu-id="8197d-151"><dt>D3dx9math。h</dt></span><span class="sxs-lookup"><span data-stu-id="8197d-151"><dt>D3dx9math.h</dt></span></span> </dl> |
| <span data-ttu-id="8197d-152">程式庫</span><span class="sxs-lookup"><span data-stu-id="8197d-152">Library</span></span><br/> | <dl> <span data-ttu-id="8197d-153"><dt>D3dx9 .lib</dt></span><span class="sxs-lookup"><span data-stu-id="8197d-153"><dt>D3dx9.lib</dt></span></span> </dl>   |



## <a name="see-also"></a><span data-ttu-id="8197d-154">另請參閱</span><span class="sxs-lookup"><span data-stu-id="8197d-154">See also</span></span>

<dl> <dt>

[<span data-ttu-id="8197d-155">數學函數</span><span class="sxs-lookup"><span data-stu-id="8197d-155">Math Functions</span></span>](dx9-graphics-reference-d3dx-functions-math.md)
</dt> </dl>

 

 
