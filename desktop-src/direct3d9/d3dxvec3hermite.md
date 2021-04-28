---
description: D3DXVec3Hermite 函式 (D3dx9math) -使用指定的3D 向量執行 Hermite 曲線插補。
ms.assetid: d45b1179-0e11-4f58-8d50-432236cb88ca
title: 'D3DXVec3Hermite 函式 (D3dx9math) '
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- D3DXVec3Hermite
api_type:
- LibDef
api_location:
- d3dx9.lib
- d3dx9.dll
ms.openlocfilehash: fd45851108d3700446a2b7f27aa00a4cc61ca39b
ms.sourcegitcommit: 95685061d5b0333bbf9e6ebd208dde8190f97005
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 04/28/2021
ms.locfileid: "108097866"
---
# <a name="d3dxvec3hermite-function-d3dx9mathh"></a><span data-ttu-id="63826-103">D3DXVec3Hermite 函式 (D3dx9math) </span><span class="sxs-lookup"><span data-stu-id="63826-103">D3DXVec3Hermite function (D3dx9math.h)</span></span>

<span data-ttu-id="63826-104">使用指定的3D 向量，執行 Hermite 曲線插補。</span><span class="sxs-lookup"><span data-stu-id="63826-104">Performs a Hermite spline interpolation, using the specified 3D vectors.</span></span>

## <a name="syntax"></a><span data-ttu-id="63826-105">語法</span><span class="sxs-lookup"><span data-stu-id="63826-105">Syntax</span></span>


```C++
D3DXVECTOR3* D3DXVec3Hermite(
  _Inout_       D3DXVECTOR3 *pOut,
  _In_    const D3DXVECTOR3 *pV1,
  _In_    const D3DXVECTOR3 *pT1,
  _In_    const D3DXVECTOR3 *pV2,
  _In_    const D3DXVECTOR3 *pT2,
  _In_          FLOAT       s
);
```



## <a name="parameters"></a><span data-ttu-id="63826-106">參數</span><span class="sxs-lookup"><span data-stu-id="63826-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="63826-107">*不悅* \[in、out\]</span><span class="sxs-lookup"><span data-stu-id="63826-107">*pOut* \[in, out\]</span></span>
</dt> <dd>

<span data-ttu-id="63826-108">類型： **[ **D3DXVECTOR3**](d3dxvector3.md)\***</span><span class="sxs-lookup"><span data-stu-id="63826-108">Type: **[**D3DXVECTOR3**](d3dxvector3.md)\***</span></span>

<span data-ttu-id="63826-109">[**D3DXVECTOR3**](d3dxvector3.md)結構的指標，此結構是作業的結果。</span><span class="sxs-lookup"><span data-stu-id="63826-109">Pointer to the [**D3DXVECTOR3**](d3dxvector3.md) structure that is the result of the operation.</span></span>

</dd> <dt>

<span data-ttu-id="63826-110">*pV1* \[在\]</span><span class="sxs-lookup"><span data-stu-id="63826-110">*pV1* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="63826-111">Type： **Const [**D3DXVECTOR3**](d3dxvector3.md) \***</span><span class="sxs-lookup"><span data-stu-id="63826-111">Type: **const [**D3DXVECTOR3**](d3dxvector3.md)\***</span></span>

<span data-ttu-id="63826-112">來源 [**D3DXVECTOR3**](d3dxvector3.md) 結構的指標，也就是位置向量。</span><span class="sxs-lookup"><span data-stu-id="63826-112">Pointer to a source [**D3DXVECTOR3**](d3dxvector3.md) structure, a position vector.</span></span>

</dd> <dt>

<span data-ttu-id="63826-113">*pT1* \[在\]</span><span class="sxs-lookup"><span data-stu-id="63826-113">*pT1* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="63826-114">Type： **Const [**D3DXVECTOR3**](d3dxvector3.md) \***</span><span class="sxs-lookup"><span data-stu-id="63826-114">Type: **const [**D3DXVECTOR3**](d3dxvector3.md)\***</span></span>

<span data-ttu-id="63826-115">來源 [**D3DXVECTOR3**](d3dxvector3.md) 結構的指標，也就是正切向量。</span><span class="sxs-lookup"><span data-stu-id="63826-115">Pointer to a source [**D3DXVECTOR3**](d3dxvector3.md) structure, a tangent vector.</span></span>

</dd> <dt>

<span data-ttu-id="63826-116">*pV2* \[在\]</span><span class="sxs-lookup"><span data-stu-id="63826-116">*pV2* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="63826-117">Type： **Const [**D3DXVECTOR3**](d3dxvector3.md) \***</span><span class="sxs-lookup"><span data-stu-id="63826-117">Type: **const [**D3DXVECTOR3**](d3dxvector3.md)\***</span></span>

<span data-ttu-id="63826-118">來源 [**D3DXVECTOR3**](d3dxvector3.md) 結構的指標，也就是位置向量。</span><span class="sxs-lookup"><span data-stu-id="63826-118">Pointer to a source [**D3DXVECTOR3**](d3dxvector3.md) structure, a position vector.</span></span>

</dd> <dt>

<span data-ttu-id="63826-119">*pT2* \[在\]</span><span class="sxs-lookup"><span data-stu-id="63826-119">*pT2* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="63826-120">Type： **Const [**D3DXVECTOR3**](d3dxvector3.md) \***</span><span class="sxs-lookup"><span data-stu-id="63826-120">Type: **const [**D3DXVECTOR3**](d3dxvector3.md)\***</span></span>

<span data-ttu-id="63826-121">來源 [**D3DXVECTOR3**](d3dxvector3.md) 結構的指標，也就是正切向量。</span><span class="sxs-lookup"><span data-stu-id="63826-121">Pointer to a source [**D3DXVECTOR3**](d3dxvector3.md) structure, a tangent vector.</span></span>

</dd> <dt>

<span data-ttu-id="63826-122"> \[ 中的 s\]</span><span class="sxs-lookup"><span data-stu-id="63826-122">*s* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="63826-123">類型： **[ **FLOAT**](../winprog/windows-data-types.md)**</span><span class="sxs-lookup"><span data-stu-id="63826-123">Type: **[**FLOAT**](../winprog/windows-data-types.md)**</span></span>

<span data-ttu-id="63826-124">加權係數。</span><span class="sxs-lookup"><span data-stu-id="63826-124">Weighting factor.</span></span> <span data-ttu-id="63826-125">請參閱＜備註＞。</span><span class="sxs-lookup"><span data-stu-id="63826-125">See Remarks.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="63826-126">傳回值</span><span class="sxs-lookup"><span data-stu-id="63826-126">Return value</span></span>

<span data-ttu-id="63826-127">類型： **[ **D3DXVECTOR3**](d3dxvector3.md)\***</span><span class="sxs-lookup"><span data-stu-id="63826-127">Type: **[**D3DXVECTOR3**](d3dxvector3.md)\***</span></span>

<span data-ttu-id="63826-128">[**D3DXVECTOR3**](d3dxvector3.md)結構的指標，此結構是 Hermite 曲線插補的結果。</span><span class="sxs-lookup"><span data-stu-id="63826-128">Pointer to a [**D3DXVECTOR3**](d3dxvector3.md) structure that is the result of the Hermite spline interpolation.</span></span>

## <a name="remarks"></a><span data-ttu-id="63826-129">備註</span><span class="sxs-lookup"><span data-stu-id="63826-129">Remarks</span></span>

<span data-ttu-id="63826-130">**D3DXVec3Hermite** 函式會將 (PositionA、tangentA) 從 (PositionB、tangentB) （使用 Hermite 曲線插補）進行插補。</span><span class="sxs-lookup"><span data-stu-id="63826-130">The **D3DXVec3Hermite** function interpolates from (positionA, tangentA) to (positionB, tangentB) using Hermite spline interpolation.</span></span>

<span data-ttu-id="63826-131">曲線插補是一種容易簡化的曲線一般化。</span><span class="sxs-lookup"><span data-stu-id="63826-131">The spline interpolation is a generalization of the ease-in, ease-out spline.</span></span> <span data-ttu-id="63826-132">此曲線是 Q (s 的函式) 具有下列屬性。</span><span class="sxs-lookup"><span data-stu-id="63826-132">The ramp is a function of Q(s) with the following properties.</span></span>

<span data-ttu-id="63826-133">Q (s) = ³ + Bs ² + Cs + D (因此，Q ' (s) = 3 ² + 2Bs + C) </span><span class="sxs-lookup"><span data-stu-id="63826-133">Q(s) = As³ + Bs² + Cs + D (and therefore, Q'(s) = 3As² + 2Bs + C)</span></span>

<span data-ttu-id="63826-134">a) Q (0) = v1，所以 Q ' (0) = t1</span><span class="sxs-lookup"><span data-stu-id="63826-134">a) Q(0) = v1, so Q'(0) = t1</span></span>

<span data-ttu-id="63826-135">b) Q (1) = v2，因此 Q ' (1) = t2</span><span class="sxs-lookup"><span data-stu-id="63826-135">b) Q(1) = v2, so Q'(1) = t2</span></span>

<span data-ttu-id="63826-136">v1 是 pV1 的內容，v2 在 pV2 的內容中，t1 是 pT1 的內容，而 t2 是 pT2 的內容。</span><span class="sxs-lookup"><span data-stu-id="63826-136">v1 is the contents of pV1, v2 in the contents of pV2, t1 is the contents of pT1, and t2 is the contents of pT2.</span></span>

<span data-ttu-id="63826-137">這些屬性是用來解決 A、B、C、D。</span><span class="sxs-lookup"><span data-stu-id="63826-137">These properties are used to solve for A, B, C, D.</span></span>

``` syntax
D = v1  (from a)
C = t1  (from a)
3A + 2B = t2 - t1 (substituting for C)
A + B = v2 - v1 - t1 (substituting for C and D)
```

<span data-ttu-id="63826-138">插入 A、B、C 和 D 的解決方案，以產生 Q (s) 。</span><span class="sxs-lookup"><span data-stu-id="63826-138">Plug in the solutions for A,B,C and D to generate Q(s).</span></span>

``` syntax
A = 2v1 - 2v2 + t2 + t1 
B = 3v2 - 3v1 - 2t1 - t2
C = t1 
D = v1
```

<span data-ttu-id="63826-139">這會產生：</span><span class="sxs-lookup"><span data-stu-id="63826-139">This yields:</span></span>

<span data-ttu-id="63826-140">Q (s) = (2v1-2v2 + t2 + t1) s ³ + (3v2-3v1-2t1-t2) s ² + t1s + v1</span><span class="sxs-lookup"><span data-stu-id="63826-140">Q(s) = (2v1 - 2v2 + t2 + t1)s³ + (3v2 - 3v1 - 2t1 - t2)s² + t1s + v1</span></span>

<span data-ttu-id="63826-141">可以重新排列為：</span><span class="sxs-lookup"><span data-stu-id="63826-141">Which can be rearranged as:</span></span>

<span data-ttu-id="63826-142">Q (s) = (2 秒³-3 秒² + 1) v1 + (-2 ³ + 3 秒²) v2 + (s ³-2-2 ² + s) t1 + (s ³-s ²) t2</span><span class="sxs-lookup"><span data-stu-id="63826-142">Q(s) = (2s³ - 3s² + 1)v1 + (-2s³ + 3s²)v2 + (s³ - 2s² + s)t1 + (s³ - s²)t2</span></span>

<span data-ttu-id="63826-143">Hermite 曲線適合用來控制動畫，因為曲線會透過所有控制點來執行。</span><span class="sxs-lookup"><span data-stu-id="63826-143">Hermite splines are useful for controlling animation because the curve runs through all the control points.</span></span> <span data-ttu-id="63826-144">此外，因為位置和正切函數是在每個區段的結尾明確指定，所以只要您確定起始位置和正切值符合最後一個區段的結束值，就很容易建立 C2 連續曲線。</span><span class="sxs-lookup"><span data-stu-id="63826-144">Also, because the position and tangent are explicitly specified at the ends of each segment, it is easy to create a C2 continuous curve as long as you make sure that your starting position and tangent match the ending values of the last segment.</span></span>

<span data-ttu-id="63826-145">此函式的傳回值與不悅參數中所傳回的值相同。</span><span class="sxs-lookup"><span data-stu-id="63826-145">The return value for this function is the same value returned in the pOut parameter.</span></span> <span data-ttu-id="63826-146">如此一來， **D3DXVec3Hermite** 函式就可以用來做為另一個函式的參數。</span><span class="sxs-lookup"><span data-stu-id="63826-146">In this way, the **D3DXVec3Hermite** function can be used as a parameter for another function.</span></span>

## <a name="requirements"></a><span data-ttu-id="63826-147">規格需求</span><span class="sxs-lookup"><span data-stu-id="63826-147">Requirements</span></span>



| <span data-ttu-id="63826-148">需求</span><span class="sxs-lookup"><span data-stu-id="63826-148">Requirement</span></span> | <span data-ttu-id="63826-149">值</span><span class="sxs-lookup"><span data-stu-id="63826-149">Value</span></span> |
|--------------------|----------------------------------------------------------------------------------------|
| <span data-ttu-id="63826-150">標頭</span><span class="sxs-lookup"><span data-stu-id="63826-150">Header</span></span><br/>  | <dl> <span data-ttu-id="63826-151"><dt>D3dx9math。h</dt></span><span class="sxs-lookup"><span data-stu-id="63826-151"><dt>D3dx9math.h</dt></span></span> </dl> |
| <span data-ttu-id="63826-152">程式庫</span><span class="sxs-lookup"><span data-stu-id="63826-152">Library</span></span><br/> | <dl> <span data-ttu-id="63826-153"><dt>D3dx9 .lib</dt></span><span class="sxs-lookup"><span data-stu-id="63826-153"><dt>D3dx9.lib</dt></span></span> </dl>   |



## <a name="see-also"></a><span data-ttu-id="63826-154">另請參閱</span><span class="sxs-lookup"><span data-stu-id="63826-154">See also</span></span>

<dl> <dt>

[<span data-ttu-id="63826-155">數學函數</span><span class="sxs-lookup"><span data-stu-id="63826-155">Math Functions</span></span>](dx9-graphics-reference-d3dx-functions-math.md)
</dt> </dl>

 

 
