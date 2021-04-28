---
description: D3DXQuaternionSquadSetup 函式 (D3DX10Math) -設定球形四邊形插補的控制點。
ms.assetid: c66227bd-8cc1-4173-9dc2-5aab9d57301e
title: 'D3DXQuaternionSquadSetup 函式 (D3DX10Math) '
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- D3DXQuaternionSquadSetup
api_type:
- LibDef
api_location:
- D3DX10.lib
- D3DX10.dll
ms.openlocfilehash: 8d8a778473c0b07ef984facce9c42f947755a74a
ms.sourcegitcommit: 95685061d5b0333bbf9e6ebd208dde8190f97005
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 04/28/2021
ms.locfileid: "108108716"
---
# <a name="d3dxquaternionsquadsetup-function-d3dx10mathh"></a><span data-ttu-id="66e49-103">D3DXQuaternionSquadSetup 函式 (D3DX10Math) </span><span class="sxs-lookup"><span data-stu-id="66e49-103">D3DXQuaternionSquadSetup function (D3DX10Math.h)</span></span>

<span data-ttu-id="66e49-104">設定球形四邊形插補的控制點。</span><span class="sxs-lookup"><span data-stu-id="66e49-104">Sets up control points for spherical quadrangle interpolation.</span></span>

## <a name="syntax"></a><span data-ttu-id="66e49-105">語法</span><span class="sxs-lookup"><span data-stu-id="66e49-105">Syntax</span></span>


```C++
void D3DXQuaternionSquadSetup(
  _In_       D3DXQUATERNION *pAOut,
  _In_       D3DXQUATERNION *pBOut,
  _In_       D3DXQUATERNION *pCOut,
  _In_ const D3DXQUATERNION *pQ0,
  _In_ const D3DXQUATERNION *pQ1,
  _In_ const D3DXQUATERNION *pQ2,
  _In_ const D3DXQUATERNION *pQ3
);
```



## <a name="parameters"></a><span data-ttu-id="66e49-106">參數</span><span class="sxs-lookup"><span data-stu-id="66e49-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="66e49-107">*pAOut* \[在\]</span><span class="sxs-lookup"><span data-stu-id="66e49-107">*pAOut* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="66e49-108">類型： **[ **D3DXQUATERNION**](../direct3d9/d3dxquaternion.md)\***</span><span class="sxs-lookup"><span data-stu-id="66e49-108">Type: **[**D3DXQUATERNION**](../direct3d9/d3dxquaternion.md)\***</span></span>

<span data-ttu-id="66e49-109">有關的指標。</span><span class="sxs-lookup"><span data-stu-id="66e49-109">Pointer to AOut.</span></span>

</dd> <dt>

<span data-ttu-id="66e49-110">*pBOut* \[在\]</span><span class="sxs-lookup"><span data-stu-id="66e49-110">*pBOut* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="66e49-111">類型： **[ **D3DXQUATERNION**](../direct3d9/d3dxquaternion.md)\***</span><span class="sxs-lookup"><span data-stu-id="66e49-111">Type: **[**D3DXQUATERNION**](../direct3d9/d3dxquaternion.md)\***</span></span>

<span data-ttu-id="66e49-112">Bout about 的指標。</span><span class="sxs-lookup"><span data-stu-id="66e49-112">Pointer to BOut.</span></span>

</dd> <dt>

<span data-ttu-id="66e49-113">*pCOut* \[在\]</span><span class="sxs-lookup"><span data-stu-id="66e49-113">*pCOut* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="66e49-114">類型： **[ **D3DXQUATERNION**](../direct3d9/d3dxquaternion.md)\***</span><span class="sxs-lookup"><span data-stu-id="66e49-114">Type: **[**D3DXQUATERNION**](../direct3d9/d3dxquaternion.md)\***</span></span>

<span data-ttu-id="66e49-115">COut 的指標。</span><span class="sxs-lookup"><span data-stu-id="66e49-115">Pointer to COut.</span></span>

</dd> <dt>

<span data-ttu-id="66e49-116">*pQ0* \[在\]</span><span class="sxs-lookup"><span data-stu-id="66e49-116">*pQ0* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="66e49-117">Type： **Const [**D3DXQUATERNION**](../direct3d9/d3dxquaternion.md) \***</span><span class="sxs-lookup"><span data-stu-id="66e49-117">Type: **const [**D3DXQUATERNION**](../direct3d9/d3dxquaternion.md)\***</span></span>

<span data-ttu-id="66e49-118">輸入控制點的指標，Q0。</span><span class="sxs-lookup"><span data-stu-id="66e49-118">Pointer to the input control point, Q0.</span></span>

</dd> <dt>

<span data-ttu-id="66e49-119">*pQ1* \[在\]</span><span class="sxs-lookup"><span data-stu-id="66e49-119">*pQ1* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="66e49-120">Type： **Const [**D3DXQUATERNION**](../direct3d9/d3dxquaternion.md) \***</span><span class="sxs-lookup"><span data-stu-id="66e49-120">Type: **const [**D3DXQUATERNION**](../direct3d9/d3dxquaternion.md)\***</span></span>

<span data-ttu-id="66e49-121">輸入控制點的指標，Q1。</span><span class="sxs-lookup"><span data-stu-id="66e49-121">Pointer to the input control point, Q1.</span></span>

</dd> <dt>

<span data-ttu-id="66e49-122">*pQ2* \[在\]</span><span class="sxs-lookup"><span data-stu-id="66e49-122">*pQ2* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="66e49-123">Type： **Const [**D3DXQUATERNION**](../direct3d9/d3dxquaternion.md) \***</span><span class="sxs-lookup"><span data-stu-id="66e49-123">Type: **const [**D3DXQUATERNION**](../direct3d9/d3dxquaternion.md)\***</span></span>

<span data-ttu-id="66e49-124">輸入控制點的指標，Q2。</span><span class="sxs-lookup"><span data-stu-id="66e49-124">Pointer to the input control point, Q2.</span></span>

</dd> <dt>

<span data-ttu-id="66e49-125">*pQ3* \[在\]</span><span class="sxs-lookup"><span data-stu-id="66e49-125">*pQ3* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="66e49-126">Type： **Const [**D3DXQUATERNION**](../direct3d9/d3dxquaternion.md) \***</span><span class="sxs-lookup"><span data-stu-id="66e49-126">Type: **const [**D3DXQUATERNION**](../direct3d9/d3dxquaternion.md)\***</span></span>

<span data-ttu-id="66e49-127">輸入控制點的指標，第3季。</span><span class="sxs-lookup"><span data-stu-id="66e49-127">Pointer to the input control point, Q3.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="66e49-128">傳回值</span><span class="sxs-lookup"><span data-stu-id="66e49-128">Return value</span></span>

<span data-ttu-id="66e49-129">無。</span><span class="sxs-lookup"><span data-stu-id="66e49-129">None.</span></span>

## <a name="remarks"></a><span data-ttu-id="66e49-130">備註</span><span class="sxs-lookup"><span data-stu-id="66e49-130">Remarks</span></span>

<span data-ttu-id="66e49-131">此函式會採用四個控制點，提供給輸入 pQ0、pQ1、pQ2 和 pQ3。</span><span class="sxs-lookup"><span data-stu-id="66e49-131">This function takes four control points, which are supplied to the inputs pQ0, pQ1, pQ2, and pQ3.</span></span> <span data-ttu-id="66e49-132">然後，此函式會改變這些值，以找出沿著最短路徑流動的曲線。</span><span class="sxs-lookup"><span data-stu-id="66e49-132">The function then alters these values to find a curve that flows along the shortest path.</span></span> <span data-ttu-id="66e49-133">Q0、q2 和 q3 的值的計算方式如下所示。</span><span class="sxs-lookup"><span data-stu-id="66e49-133">The values of q0, q2, and q3 are calculated as shown below.</span></span>


```
q0 = |Q0 + Q1| < |Q0 - Q1| ? -Q0 : Q0
q2 = |Q1 + Q2| < |Q1 - Q2| ? -Q2 : Q2
q3 = |Q2 + Q3| < |Q2 - Q3| ? -Q3 : Q3
```



<span data-ttu-id="66e49-134">在計算新的 Q 值之後，有關、Bout about 和 COut 的值的計算方式如下：</span><span class="sxs-lookup"><span data-stu-id="66e49-134">Having calculated the new Q values, the values for AOut, BOut, and COut are calculated as follows:</span></span>

<span data-ttu-id="66e49-135">有關 = q1 \* e<sup> \[ -0.25 \ \* ( \ Ln \[ exp (q1) \* q2 \] \ + \ ln \[ exp (q1) \* q0 \] \ ) \ \] </sup></span><span class="sxs-lookup"><span data-stu-id="66e49-135">AOut = q1 \* e<sup>\[-0.25\ \*(\ Ln\[Exp(q1)\*q2\]\ +\ Ln\[Exp(q1)\*q0\]\ )\ \]</sup></span></span>

<span data-ttu-id="66e49-136">Bout about = q2 \* e<sup> \[ -0.25 \ \* ( \ Ln \[ Exp (q2) \* q3 \ \] + \ ln \[ exp (q2) \* q1 \] \ ) \ \] </sup></span><span class="sxs-lookup"><span data-stu-id="66e49-136">BOut = q2 \* e<sup>\[-0.25\ \*(\ Ln\[Exp(q2)\*q3\]\ +\ Ln\[Exp(q2)\*q1\]\ )\ \]</sup></span></span>

<span data-ttu-id="66e49-137">COut = q2</span><span class="sxs-lookup"><span data-stu-id="66e49-137">COut = q2</span></span>

> [!Note]  
> <span data-ttu-id="66e49-138">Ln 是 API 方法 [**D3DXQuaternionLn**](d3d10-d3dxquaternionln.md) ，而 EXP 是 Api 方法 [**D3DXQuaternionExp**](d3d10-d3dxquaternionexp.md)。</span><span class="sxs-lookup"><span data-stu-id="66e49-138">Ln is the API method [**D3DXQuaternionLn**](d3d10-d3dxquaternionln.md) and Exp is the API method [**D3DXQuaternionExp**](d3d10-d3dxquaternionexp.md).</span></span>

 

<span data-ttu-id="66e49-139">針對尚未正規化的任何四元數輸入，請使用 [**D3DXQuaternionNormalize**](d3d10-d3dxquaternionnormalize.md) 。</span><span class="sxs-lookup"><span data-stu-id="66e49-139">Use [**D3DXQuaternionNormalize**](d3d10-d3dxquaternionnormalize.md) for any quaternion input that is not already normalized.</span></span>

### <a name="examples"></a><span data-ttu-id="66e49-140">範例</span><span class="sxs-lookup"><span data-stu-id="66e49-140">Examples</span></span>

<span data-ttu-id="66e49-141">下列範例示範如何使用一組四元數索引鍵 (Q0、Q1、Q2、Q3) 來計算內部四邊形點 (A，B，C) 。</span><span class="sxs-lookup"><span data-stu-id="66e49-141">The following example shows how to use a set of quaternion keys (Q0, Q1, Q2, Q3) to compute the inner quadrangle points (A, B, C).</span></span> <span data-ttu-id="66e49-142">這可確保相鄰區段之間的切線是連續的。</span><span class="sxs-lookup"><span data-stu-id="66e49-142">This ensures that the tangents are continuous across adjacent segments.</span></span>


```
      A     B
Q0    Q1    Q2    Q3
```



<span data-ttu-id="66e49-143">下列程式碼範例將示範如何在 Q1 和 Q2 之間進行插補。</span><span class="sxs-lookup"><span data-stu-id="66e49-143">The following code example demonstrates how you can interpolate between Q1 and Q2.</span></span>


```
// Rotation about the z-axis
D3DXQUATERNION Q0 = D3DXQUATERNION(0,  0, 0.707f, -.707f);
D3DXQUATERNION Q1 = D3DXQUATERNION(0,  0, 0.000f, 1.000f);
D3DXQUATERNION Q2 = D3DXQUATERNION(0,  0, 0.707f, 0.707f);
D3DXQUATERNION Q3 = D3DXQUATERNION(0,  0, 1.000f, 0.000f);
D3DXQUATERNION A, B, C, Qt;
FLOAT time = 0.5f;

D3DXQuaternionSquadSetup(&A, &B, &C, &Q0, &Q1, &Q2, &Q3);
D3DXQuaternionSquad(&Qt, &Q1, &A, &B, &C, time);
```



> [!Note]
>
> -   <span data-ttu-id="66e49-144">C 是 +/-Q2，視函數的結果而定。</span><span class="sxs-lookup"><span data-stu-id="66e49-144">C is +/- Q2 depending on the result of the function.</span></span>
> -   <span data-ttu-id="66e49-145">Qt 是函數的結果。</span><span class="sxs-lookup"><span data-stu-id="66e49-145">Qt is the result of the function.</span></span>
>
> <span data-ttu-id="66e49-146">結果是時間 = 0.5 的 Z 軸周圍的45度旋轉。</span><span class="sxs-lookup"><span data-stu-id="66e49-146">The result is a rotation of 45 degrees around the z-axis for time = 0.5.</span></span>

 

## <a name="requirements"></a><span data-ttu-id="66e49-147">規格需求</span><span class="sxs-lookup"><span data-stu-id="66e49-147">Requirements</span></span>



| <span data-ttu-id="66e49-148">需求</span><span class="sxs-lookup"><span data-stu-id="66e49-148">Requirement</span></span> | <span data-ttu-id="66e49-149">值</span><span class="sxs-lookup"><span data-stu-id="66e49-149">Value</span></span> |
|--------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="66e49-150">標頭</span><span class="sxs-lookup"><span data-stu-id="66e49-150">Header</span></span><br/>  | <dl> <span data-ttu-id="66e49-151"><dt>D3DX10Math。h</dt></span><span class="sxs-lookup"><span data-stu-id="66e49-151"><dt>D3DX10Math.h</dt></span></span> </dl> |
| <span data-ttu-id="66e49-152">程式庫</span><span class="sxs-lookup"><span data-stu-id="66e49-152">Library</span></span><br/> | <dl> <span data-ttu-id="66e49-153"><dt>D3DX10 .lib</dt></span><span class="sxs-lookup"><span data-stu-id="66e49-153"><dt>D3DX10.lib</dt></span></span> </dl>   |



## <a name="see-also"></a><span data-ttu-id="66e49-154">另請參閱</span><span class="sxs-lookup"><span data-stu-id="66e49-154">See also</span></span>

<dl> <dt>

[<span data-ttu-id="66e49-155">數學函數</span><span class="sxs-lookup"><span data-stu-id="66e49-155">Math Functions</span></span>](d3d10-graphics-reference-d3dx10-functions-math.md)
</dt> </dl>

 

 
