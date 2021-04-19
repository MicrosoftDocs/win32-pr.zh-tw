---
description: 設定球形四邊形插補的控制點。
ms.assetid: f800d457-8546-49a1-800e-e5c27af96710
title: 'D3DXQuaternionSquadSetup 函式 (D3dx9math) '
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
- d3dx9.lib
- d3dx9.dll
ms.openlocfilehash: 04bae9dafbb9df90fdcccee830a1eecb64c1430f
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 03/15/2021
ms.locfileid: "106997381"
---
# <a name="d3dxquaternionsquadsetup-function-d3dx9mathh"></a><span data-ttu-id="527f0-103">D3DXQuaternionSquadSetup 函式 (D3dx9math) </span><span class="sxs-lookup"><span data-stu-id="527f0-103">D3DXQuaternionSquadSetup function (D3dx9math.h)</span></span>

<span data-ttu-id="527f0-104">設定球形四邊形插補的控制點。</span><span class="sxs-lookup"><span data-stu-id="527f0-104">Sets up control points for spherical quadrangle interpolation.</span></span>

## <a name="syntax"></a><span data-ttu-id="527f0-105">語法</span><span class="sxs-lookup"><span data-stu-id="527f0-105">Syntax</span></span>


```C++
void D3DXQuaternionSquadSetup(
  _Out_       D3DXQUATERNION *pAOut,
  _Out_       D3DXQUATERNION *pBOut,
  _Out_       D3DXQUATERNION *pCOut,
  _In_  const D3DXQUATERNION *pQ0,
  _In_  const D3DXQUATERNION *pQ1,
  _In_  const D3DXQUATERNION *pQ2,
  _In_  const D3DXQUATERNION *pQ3
);
```



## <a name="parameters"></a><span data-ttu-id="527f0-106">參數</span><span class="sxs-lookup"><span data-stu-id="527f0-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="527f0-107">*pAOut* \[擴展\]</span><span class="sxs-lookup"><span data-stu-id="527f0-107">*pAOut* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="527f0-108">類型： **[ **D3DXQUATERNION**](d3dxquaternion.md)\***</span><span class="sxs-lookup"><span data-stu-id="527f0-108">Type: **[**D3DXQUATERNION**](d3dxquaternion.md)\***</span></span>

<span data-ttu-id="527f0-109">有關的指標。</span><span class="sxs-lookup"><span data-stu-id="527f0-109">Pointer to AOut.</span></span>

</dd> <dt>

<span data-ttu-id="527f0-110">*pBOut* \[擴展\]</span><span class="sxs-lookup"><span data-stu-id="527f0-110">*pBOut* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="527f0-111">類型： **[ **D3DXQUATERNION**](d3dxquaternion.md)\***</span><span class="sxs-lookup"><span data-stu-id="527f0-111">Type: **[**D3DXQUATERNION**](d3dxquaternion.md)\***</span></span>

<span data-ttu-id="527f0-112">Bout about 的指標。</span><span class="sxs-lookup"><span data-stu-id="527f0-112">Pointer to BOut.</span></span>

</dd> <dt>

<span data-ttu-id="527f0-113">*pCOut* \[擴展\]</span><span class="sxs-lookup"><span data-stu-id="527f0-113">*pCOut* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="527f0-114">類型： **[ **D3DXQUATERNION**](d3dxquaternion.md)\***</span><span class="sxs-lookup"><span data-stu-id="527f0-114">Type: **[**D3DXQUATERNION**](d3dxquaternion.md)\***</span></span>

<span data-ttu-id="527f0-115">COut 的指標。</span><span class="sxs-lookup"><span data-stu-id="527f0-115">Pointer to COut.</span></span>

</dd> <dt>

<span data-ttu-id="527f0-116">*pQ0* \[在\]</span><span class="sxs-lookup"><span data-stu-id="527f0-116">*pQ0* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="527f0-117">Type： **Const [**D3DXQUATERNION**](d3dxquaternion.md) \***</span><span class="sxs-lookup"><span data-stu-id="527f0-117">Type: **const [**D3DXQUATERNION**](d3dxquaternion.md)\***</span></span>

<span data-ttu-id="527f0-118">輸入控制點的指標，Q0。</span><span class="sxs-lookup"><span data-stu-id="527f0-118">Pointer to the input control point, Q0.</span></span>

</dd> <dt>

<span data-ttu-id="527f0-119">*pQ1* \[在\]</span><span class="sxs-lookup"><span data-stu-id="527f0-119">*pQ1* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="527f0-120">Type： **Const [**D3DXQUATERNION**](d3dxquaternion.md) \***</span><span class="sxs-lookup"><span data-stu-id="527f0-120">Type: **const [**D3DXQUATERNION**](d3dxquaternion.md)\***</span></span>

<span data-ttu-id="527f0-121">輸入控制點的指標，Q1。</span><span class="sxs-lookup"><span data-stu-id="527f0-121">Pointer to the input control point, Q1.</span></span>

</dd> <dt>

<span data-ttu-id="527f0-122">*pQ2* \[在\]</span><span class="sxs-lookup"><span data-stu-id="527f0-122">*pQ2* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="527f0-123">Type： **Const [**D3DXQUATERNION**](d3dxquaternion.md) \***</span><span class="sxs-lookup"><span data-stu-id="527f0-123">Type: **const [**D3DXQUATERNION**](d3dxquaternion.md)\***</span></span>

<span data-ttu-id="527f0-124">輸入控制點的指標，Q2。</span><span class="sxs-lookup"><span data-stu-id="527f0-124">Pointer to the input control point, Q2.</span></span>

</dd> <dt>

<span data-ttu-id="527f0-125">*pQ3* \[在\]</span><span class="sxs-lookup"><span data-stu-id="527f0-125">*pQ3* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="527f0-126">Type： **Const [**D3DXQUATERNION**](d3dxquaternion.md) \***</span><span class="sxs-lookup"><span data-stu-id="527f0-126">Type: **const [**D3DXQUATERNION**](d3dxquaternion.md)\***</span></span>

<span data-ttu-id="527f0-127">輸入控制點的指標，第3季。</span><span class="sxs-lookup"><span data-stu-id="527f0-127">Pointer to the input control point, Q3.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="527f0-128">傳回值</span><span class="sxs-lookup"><span data-stu-id="527f0-128">Return value</span></span>

<span data-ttu-id="527f0-129">無。</span><span class="sxs-lookup"><span data-stu-id="527f0-129">None.</span></span>

## <a name="remarks"></a><span data-ttu-id="527f0-130">備註</span><span class="sxs-lookup"><span data-stu-id="527f0-130">Remarks</span></span>

<span data-ttu-id="527f0-131">此函式會採用四個控制點，提供給輸入 pQ0、pQ1、pQ2 和 pQ3。</span><span class="sxs-lookup"><span data-stu-id="527f0-131">This function takes four control points, which are supplied to the inputs pQ0, pQ1, pQ2, and pQ3.</span></span> <span data-ttu-id="527f0-132">然後，此函式會改變這些值，以找出沿著最短路徑流動的曲線。</span><span class="sxs-lookup"><span data-stu-id="527f0-132">The function then alters these values to find a curve that flows along the shortest path.</span></span> <span data-ttu-id="527f0-133">Q0、q2 和 q3 的值的計算方式如下所示。</span><span class="sxs-lookup"><span data-stu-id="527f0-133">The values of q0, q2, and q3 are calculated as shown below.</span></span>


```
q0 = |Q0 + Q1| < |Q0 - Q1| ? -Q0 : Q0
q2 = |Q1 + Q2| < |Q1 - Q2| ? -Q2 : Q2
q3 = |Q2 + Q3| < |Q2 - Q3| ? -Q3 : Q3
```



<span data-ttu-id="527f0-134">在計算新的 Q 值之後，有關、Bout about 和 COut 的值的計算方式如下：</span><span class="sxs-lookup"><span data-stu-id="527f0-134">Having calculated the new Q values, the values for AOut, BOut, and COut are calculated as follows:</span></span>

<span data-ttu-id="527f0-135">有關 = q1 \* e<sup> \[ -0.25 \ \* ( \ Ln \[ exp (q1) \* q2 \] \ + \ ln \[ exp (q1) \* q0 \] \ ) \ \] </sup></span><span class="sxs-lookup"><span data-stu-id="527f0-135">AOut = q1 \* e<sup>\[-0.25\ \*(\ Ln\[Exp(q1)\*q2\]\ +\ Ln\[Exp(q1)\*q0\]\ )\ \]</sup></span></span>

<span data-ttu-id="527f0-136">Bout about = q2 \* e<sup> \[ -0.25 \ \* ( \ Ln \[ Exp (q2) \* q3 \ \] + \ ln \[ exp (q2) \* q1 \] \ ) \ \] </sup></span><span class="sxs-lookup"><span data-stu-id="527f0-136">BOut = q2 \* e<sup>\[-0.25\ \*(\ Ln\[Exp(q2)\*q3\]\ +\ Ln\[Exp(q2)\*q1\]\ )\ \]</sup></span></span>

<span data-ttu-id="527f0-137">COut = q2</span><span class="sxs-lookup"><span data-stu-id="527f0-137">COut = q2</span></span>

> [!Note]  
> <span data-ttu-id="527f0-138">Ln 是 API 方法 [**D3DXQuaternionLn**](d3dxquaternionln.md) ，而 EXP 是 Api 方法 [**D3DXQuaternionExp**](d3dxquaternionexp.md)。</span><span class="sxs-lookup"><span data-stu-id="527f0-138">Ln is the API method [**D3DXQuaternionLn**](d3dxquaternionln.md) and Exp is the API method [**D3DXQuaternionExp**](d3dxquaternionexp.md).</span></span>

 

<span data-ttu-id="527f0-139">針對尚未正規化的任何四元數輸入，請使用 [**D3DXQuaternionNormalize**](d3dxquaternionnormalize.md) 。</span><span class="sxs-lookup"><span data-stu-id="527f0-139">Use [**D3DXQuaternionNormalize**](d3dxquaternionnormalize.md) for any quaternion input that is not already normalized.</span></span>

### <a name="examples"></a><span data-ttu-id="527f0-140">範例</span><span class="sxs-lookup"><span data-stu-id="527f0-140">Examples</span></span>

<span data-ttu-id="527f0-141">下列範例示範如何使用一組四元數索引鍵 (Q0、Q1、Q2、Q3) 來計算內部四邊形點 (A，B，C) 。</span><span class="sxs-lookup"><span data-stu-id="527f0-141">The following example shows how to use a set of quaternion keys (Q0, Q1, Q2, Q3) to compute the inner quadrangle points (A, B, C).</span></span> <span data-ttu-id="527f0-142">這可確保相鄰區段之間的切線是連續的。</span><span class="sxs-lookup"><span data-stu-id="527f0-142">This ensures that the tangents are continuous across adjacent segments.</span></span>


```
      A     B
Q0    Q1    Q2    Q3
```



<span data-ttu-id="527f0-143">下列程式碼範例將示範如何在 Q1 和 Q2 之間進行插補。</span><span class="sxs-lookup"><span data-stu-id="527f0-143">The following code example demonstrates how you can interpolate between Q1 and Q2.</span></span>


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
> -   <span data-ttu-id="527f0-144">C 是 +/-Q2，視函數的結果而定。</span><span class="sxs-lookup"><span data-stu-id="527f0-144">C is +/- Q2 depending on the result of the function.</span></span>
> -   <span data-ttu-id="527f0-145">Qt 是函數的結果。</span><span class="sxs-lookup"><span data-stu-id="527f0-145">Qt is the result of the function.</span></span>
>
> <span data-ttu-id="527f0-146">結果是時間 = 0.5 的 Z 軸周圍的45度旋轉。</span><span class="sxs-lookup"><span data-stu-id="527f0-146">The result is a rotation of 45 degrees around the z-axis for time = 0.5.</span></span>

 

## <a name="requirements"></a><span data-ttu-id="527f0-147">規格需求</span><span class="sxs-lookup"><span data-stu-id="527f0-147">Requirements</span></span>



| <span data-ttu-id="527f0-148">需求</span><span class="sxs-lookup"><span data-stu-id="527f0-148">Requirement</span></span> | <span data-ttu-id="527f0-149">值</span><span class="sxs-lookup"><span data-stu-id="527f0-149">Value</span></span> |
|--------------------|----------------------------------------------------------------------------------------|
| <span data-ttu-id="527f0-150">標頭</span><span class="sxs-lookup"><span data-stu-id="527f0-150">Header</span></span><br/>  | <dl> <span data-ttu-id="527f0-151"><dt>D3dx9math。h</dt></span><span class="sxs-lookup"><span data-stu-id="527f0-151"><dt>D3dx9math.h</dt></span></span> </dl> |
| <span data-ttu-id="527f0-152">程式庫</span><span class="sxs-lookup"><span data-stu-id="527f0-152">Library</span></span><br/> | <dl> <span data-ttu-id="527f0-153"><dt>D3dx9 .lib</dt></span><span class="sxs-lookup"><span data-stu-id="527f0-153"><dt>D3dx9.lib</dt></span></span> </dl>   |



## <a name="see-also"></a><span data-ttu-id="527f0-154">另請參閱</span><span class="sxs-lookup"><span data-stu-id="527f0-154">See also</span></span>

<dl> <dt>

[<span data-ttu-id="527f0-155">數學函數</span><span class="sxs-lookup"><span data-stu-id="527f0-155">Math Functions</span></span>](dx9-graphics-reference-d3dx-functions-math.md)
</dt> <dt>

[<span data-ttu-id="527f0-156">**D3DXQuaternionSquad**</span><span class="sxs-lookup"><span data-stu-id="527f0-156">**D3DXQuaternionSquad**</span></span>](d3dxquaternionsquad.md)
</dt> </dl>

 

 




