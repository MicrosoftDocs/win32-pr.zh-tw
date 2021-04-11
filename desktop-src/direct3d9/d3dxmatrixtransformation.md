---
description: 建立轉換矩陣。 Null 引數會被視為身分識別轉換。
ms.assetid: 39042fc6-f489-4e44-ad3f-858ca395575d
title: 'D3DXMatrixTransformation 函式 (D3dx9math) '
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- D3DXMatrixTransformation
api_type:
- LibDef
api_location:
- d3dx9.lib
- d3dx9.dll
ms.openlocfilehash: f2174329e01e3e624ef27608ca56b33181b770db
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 03/15/2021
ms.locfileid: "104035330"
---
# <a name="d3dxmatrixtransformation-function-d3dx9mathh"></a><span data-ttu-id="f8c53-104">D3DXMatrixTransformation 函式 (D3dx9math) </span><span class="sxs-lookup"><span data-stu-id="f8c53-104">D3DXMatrixTransformation function (D3dx9math.h)</span></span>

<span data-ttu-id="f8c53-105">建立轉換矩陣。</span><span class="sxs-lookup"><span data-stu-id="f8c53-105">Builds a transformation matrix.</span></span> <span data-ttu-id="f8c53-106">**Null** 引數會被視為身分識別轉換。</span><span class="sxs-lookup"><span data-stu-id="f8c53-106">**NULL** arguments are treated as identity transformations.</span></span>

## <a name="syntax"></a><span data-ttu-id="f8c53-107">語法</span><span class="sxs-lookup"><span data-stu-id="f8c53-107">Syntax</span></span>


```C++
D3DXMATRIX* D3DXMatrixTransformation(
  _Inout_       D3DXMATRIX     *pOut,
  _In_    const D3DXVECTOR3    *pScalingCenter,
  _In_    const D3DXQUATERNION *pScalingRotation,
  _In_    const D3DXVECTOR3    *pScaling,
  _In_    const D3DXVECTOR3    *pRotationCenter,
  _In_    const D3DXQUATERNION *pRotation,
  _In_    const D3DXVECTOR3    *pTranslation
);
```



## <a name="parameters"></a><span data-ttu-id="f8c53-108">參數</span><span class="sxs-lookup"><span data-stu-id="f8c53-108">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="f8c53-109">*不悅* \[in、out\]</span><span class="sxs-lookup"><span data-stu-id="f8c53-109">*pOut* \[in, out\]</span></span>
</dt> <dd>

<span data-ttu-id="f8c53-110">類型： **[ **D3DXMATRIX**](d3dxmatrix.md)\***</span><span class="sxs-lookup"><span data-stu-id="f8c53-110">Type: **[**D3DXMATRIX**](d3dxmatrix.md)\***</span></span>

<span data-ttu-id="f8c53-111">[**D3DXMATRIX**](d3dxmatrix.md)結構的指標，此結構是作業的結果。</span><span class="sxs-lookup"><span data-stu-id="f8c53-111">Pointer to the [**D3DXMATRIX**](d3dxmatrix.md) structure that is the result of the operation.</span></span>

</dd> <dt>

<span data-ttu-id="f8c53-112">*pScalingCenter* \[在\]</span><span class="sxs-lookup"><span data-stu-id="f8c53-112">*pScalingCenter* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="f8c53-113">Type： **Const [**D3DXVECTOR3**](d3dxvector3.md) \***</span><span class="sxs-lookup"><span data-stu-id="f8c53-113">Type: **const [**D3DXVECTOR3**](d3dxvector3.md)\***</span></span>

<span data-ttu-id="f8c53-114">[**D3DXVECTOR3**](d3dxvector3.md)結構的指標，可識別縮放中心點。</span><span class="sxs-lookup"><span data-stu-id="f8c53-114">Pointer to a [**D3DXVECTOR3**](d3dxvector3.md) structure, identifying the scaling center point.</span></span> <span data-ttu-id="f8c53-115">如果這個引數是 **Null**，則會將身分識別 M <sub>sc</sub> 矩陣套用至備註中的公式。</span><span class="sxs-lookup"><span data-stu-id="f8c53-115">If this argument is **NULL**, an identity M<sub>sc</sub> matrix is applied to the formula in Remarks.</span></span>

</dd> <dt>

<span data-ttu-id="f8c53-116">*pScalingRotation* \[在\]</span><span class="sxs-lookup"><span data-stu-id="f8c53-116">*pScalingRotation* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="f8c53-117">Type： **Const [**D3DXQUATERNION**](d3dxquaternion.md) \***</span><span class="sxs-lookup"><span data-stu-id="f8c53-117">Type: **const [**D3DXQUATERNION**](d3dxquaternion.md)\***</span></span>

<span data-ttu-id="f8c53-118">指定縮放旋轉之 [**D3DXQUATERNION**](d3dxquaternion.md) 結構的指標。</span><span class="sxs-lookup"><span data-stu-id="f8c53-118">Pointer to a [**D3DXQUATERNION**](d3dxquaternion.md) structure that specifies the scaling rotation.</span></span> <span data-ttu-id="f8c53-119">如果這個引數是 **Null**，則會將身分識別 M <sub>sr</sub> 矩陣套用至備註中的公式。</span><span class="sxs-lookup"><span data-stu-id="f8c53-119">If this argument is **NULL**, an identity M<sub>sr</sub> matrix is applied to the formula in Remarks.</span></span>

</dd> <dt>

<span data-ttu-id="f8c53-120">*pScaling* \[在\]</span><span class="sxs-lookup"><span data-stu-id="f8c53-120">*pScaling* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="f8c53-121">Type： **Const [**D3DXVECTOR3**](d3dxvector3.md) \***</span><span class="sxs-lookup"><span data-stu-id="f8c53-121">Type: **const [**D3DXVECTOR3**](d3dxvector3.md)\***</span></span>

<span data-ttu-id="f8c53-122">[**D3DXVECTOR3**](d3dxvector3.md)結構的指標，也就是縮放向量。</span><span class="sxs-lookup"><span data-stu-id="f8c53-122">Pointer to a [**D3DXVECTOR3**](d3dxvector3.md) structure, the scaling vector.</span></span> <span data-ttu-id="f8c53-123">如果這個引數是 **Null**，則會將身分識別 Ms 矩陣套用至備註中的公式。</span><span class="sxs-lookup"><span data-stu-id="f8c53-123">If this argument is **NULL**, an identity Mₛ matrix is applied to the formula in Remarks.</span></span>

</dd> <dt>

<span data-ttu-id="f8c53-124">*pRotationCenter* \[在\]</span><span class="sxs-lookup"><span data-stu-id="f8c53-124">*pRotationCenter* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="f8c53-125">Type： **Const [**D3DXVECTOR3**](d3dxvector3.md) \***</span><span class="sxs-lookup"><span data-stu-id="f8c53-125">Type: **const [**D3DXVECTOR3**](d3dxvector3.md)\***</span></span>

<span data-ttu-id="f8c53-126">[**D3DXVECTOR3**](d3dxvector3.md)結構的指標，也就是識別旋轉中心的點。</span><span class="sxs-lookup"><span data-stu-id="f8c53-126">Pointer to a [**D3DXVECTOR3**](d3dxvector3.md) structure, a point that identifies the center of rotation.</span></span> <span data-ttu-id="f8c53-127">如果此引數為 **Null**，則會將身分識別 M <sub>rc</sub> 矩陣套用至備註中的公式。</span><span class="sxs-lookup"><span data-stu-id="f8c53-127">If this argument is **NULL**, an identity M<sub>rc</sub> matrix is applied to the formula in Remarks.</span></span>

</dd> <dt>

<span data-ttu-id="f8c53-128">*pRotation* \[在\]</span><span class="sxs-lookup"><span data-stu-id="f8c53-128">*pRotation* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="f8c53-129">Type： **Const [**D3DXQUATERNION**](d3dxquaternion.md) \***</span><span class="sxs-lookup"><span data-stu-id="f8c53-129">Type: **const [**D3DXQUATERNION**](d3dxquaternion.md)\***</span></span>

<span data-ttu-id="f8c53-130">指定旋轉之 [**D3DXQUATERNION**](d3dxquaternion.md) 結構的指標。</span><span class="sxs-lookup"><span data-stu-id="f8c53-130">Pointer to a [**D3DXQUATERNION**](d3dxquaternion.md) structure that specifies the rotation.</span></span> <span data-ttu-id="f8c53-131">如果這個引數是 **Null**，則會將身分識別 M <sub>r</sub> 矩陣套用至備註中的公式。</span><span class="sxs-lookup"><span data-stu-id="f8c53-131">If this argument is **NULL**, an identity M<sub>r</sub> matrix is applied to the formula in Remarks.</span></span>

</dd> <dt>

<span data-ttu-id="f8c53-132">*pTranslation* \[在\]</span><span class="sxs-lookup"><span data-stu-id="f8c53-132">*pTranslation* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="f8c53-133">Type： **Const [**D3DXVECTOR3**](d3dxvector3.md) \***</span><span class="sxs-lookup"><span data-stu-id="f8c53-133">Type: **const [**D3DXVECTOR3**](d3dxvector3.md)\***</span></span>

<span data-ttu-id="f8c53-134">[**D3DXVECTOR3**](d3dxvector3.md)結構的指標，表示轉譯。</span><span class="sxs-lookup"><span data-stu-id="f8c53-134">Pointer to a [**D3DXVECTOR3**](d3dxvector3.md) structure, representing the translation.</span></span> <span data-ttu-id="f8c53-135">如果此引數為 **Null**，則會將身分識別 Mt 矩陣套用至備註中的公式。</span><span class="sxs-lookup"><span data-stu-id="f8c53-135">If this argument is **NULL**, an identity Mₜ matrix is applied to the formula in Remarks.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="f8c53-136">傳回值</span><span class="sxs-lookup"><span data-stu-id="f8c53-136">Return value</span></span>

<span data-ttu-id="f8c53-137">類型： **[ **D3DXMATRIX**](d3dxmatrix.md)\***</span><span class="sxs-lookup"><span data-stu-id="f8c53-137">Type: **[**D3DXMATRIX**](d3dxmatrix.md)\***</span></span>

<span data-ttu-id="f8c53-138">[**D3DXMATRIX**](d3dxmatrix.md)結構的指標，此結構是轉換矩陣。</span><span class="sxs-lookup"><span data-stu-id="f8c53-138">Pointer to a [**D3DXMATRIX**](d3dxmatrix.md) structure that is the transformation matrix.</span></span>

## <a name="remarks"></a><span data-ttu-id="f8c53-139">備註</span><span class="sxs-lookup"><span data-stu-id="f8c53-139">Remarks</span></span>

<span data-ttu-id="f8c53-140">此函式會使用下列公式來計算轉換矩陣，並以由左至右順序評估矩陣串連：</span><span class="sxs-lookup"><span data-stu-id="f8c53-140">This function calculates the transformation matrix with the following formula, with matrix concatenation evaluated in left-to-right order:</span></span>

<span data-ttu-id="f8c53-141">M<sub>out</sub> = (m<sub>sc</sub>) ⁻¹ \* (M<sub>sr</sub>) ⁻¹ \* Ms \* M<sub>sr</sub> \* M<sub>sc</sub> \* (M<sub>rc</sub>) ⁻¹ \* m<sub>r</sub> \* m<sub>rc</sub> \* Mt</span><span class="sxs-lookup"><span data-stu-id="f8c53-141">M<sub>out</sub> = (M<sub>sc</sub>)⁻¹ \* (M<sub>sr</sub>)⁻¹\* Mₛ \* M<sub>sr</sub> \* M<sub>sc</sub> \* (M<sub>rc</sub>)⁻¹\* M<sub>r</sub> \* M<sub>rc</sub> \* Mt</span></span>

<span data-ttu-id="f8c53-142">其中：</span><span class="sxs-lookup"><span data-stu-id="f8c53-142">where:</span></span>

<span data-ttu-id="f8c53-143">M <sub>out</sub> = 輸出矩陣 (*不悅*) </span><span class="sxs-lookup"><span data-stu-id="f8c53-143">M <sub>out</sub> = output matrix (*pOut*)</span></span>

<span data-ttu-id="f8c53-144">M <sub>sc</sub> = 縮放中心矩陣 (*pScalingCenter*) </span><span class="sxs-lookup"><span data-stu-id="f8c53-144">M <sub>sc</sub> = scaling center matrix (*pScalingCenter*)</span></span>

<span data-ttu-id="f8c53-145">M <sub>sr</sub> = 調整旋轉矩陣 (*pScalingRotation*) </span><span class="sxs-lookup"><span data-stu-id="f8c53-145">M <sub>sr</sub> = scaling rotation matrix (*pScalingRotation*)</span></span>

<span data-ttu-id="f8c53-146">Ms = 調整矩陣 (*pScaling*) </span><span class="sxs-lookup"><span data-stu-id="f8c53-146">Mₛ = scaling matrix (*pScaling*)</span></span>

<span data-ttu-id="f8c53-147">M <sub>rc</sub> = 旋轉矩陣的中心 (*pRotationCenter*) </span><span class="sxs-lookup"><span data-stu-id="f8c53-147">M <sub>rc</sub> = center of rotation matrix (*pRotationCenter*)</span></span>

<span data-ttu-id="f8c53-148">M <sub>r</sub> = 旋轉矩陣 (*pRotation*) </span><span class="sxs-lookup"><span data-stu-id="f8c53-148">M <sub>r</sub> = rotation matrix (*pRotation*)</span></span>

<span data-ttu-id="f8c53-149">Mt = 轉譯矩陣 (*pTranslation*) </span><span class="sxs-lookup"><span data-stu-id="f8c53-149">Mₜ = translation matrix (*pTranslation*)</span></span>

<span data-ttu-id="f8c53-150">此函式的傳回值與 *不悅* 參數中所傳回的值相同。</span><span class="sxs-lookup"><span data-stu-id="f8c53-150">The return value for this function is the same value returned in the *pOut* parameter.</span></span> <span data-ttu-id="f8c53-151">如此一來， **D3DXMatrixTransformation** 函式就可以用來做為另一個函式的參數。</span><span class="sxs-lookup"><span data-stu-id="f8c53-151">In this way, the **D3DXMatrixTransformation** function can be used as a parameter for another function.</span></span>

<span data-ttu-id="f8c53-152">若是2D 轉換，請使用 [**D3DXMatrixTransformation2D**](d3dxmatrixtransformation2d.md)。</span><span class="sxs-lookup"><span data-stu-id="f8c53-152">For 2D transformations, use [**D3DXMatrixTransformation2D**](d3dxmatrixtransformation2d.md).</span></span>

## <a name="requirements"></a><span data-ttu-id="f8c53-153">規格需求</span><span class="sxs-lookup"><span data-stu-id="f8c53-153">Requirements</span></span>



| <span data-ttu-id="f8c53-154">需求</span><span class="sxs-lookup"><span data-stu-id="f8c53-154">Requirement</span></span> | <span data-ttu-id="f8c53-155">值</span><span class="sxs-lookup"><span data-stu-id="f8c53-155">Value</span></span> |
|--------------------|----------------------------------------------------------------------------------------|
| <span data-ttu-id="f8c53-156">標頭</span><span class="sxs-lookup"><span data-stu-id="f8c53-156">Header</span></span><br/>  | <dl> <span data-ttu-id="f8c53-157"><dt>D3dx9math。h</dt></span><span class="sxs-lookup"><span data-stu-id="f8c53-157"><dt>D3dx9math.h</dt></span></span> </dl> |
| <span data-ttu-id="f8c53-158">程式庫</span><span class="sxs-lookup"><span data-stu-id="f8c53-158">Library</span></span><br/> | <dl> <span data-ttu-id="f8c53-159"><dt>D3dx9 .lib</dt></span><span class="sxs-lookup"><span data-stu-id="f8c53-159"><dt>D3dx9.lib</dt></span></span> </dl>   |



## <a name="see-also"></a><span data-ttu-id="f8c53-160">另請參閱</span><span class="sxs-lookup"><span data-stu-id="f8c53-160">See also</span></span>

<dl> <dt>

[<span data-ttu-id="f8c53-161">數學函數</span><span class="sxs-lookup"><span data-stu-id="f8c53-161">Math Functions</span></span>](dx9-graphics-reference-d3dx-functions-math.md)
</dt> <dt>

[<span data-ttu-id="f8c53-162">**D3DXMatrixAffineTransformation**</span><span class="sxs-lookup"><span data-stu-id="f8c53-162">**D3DXMatrixAffineTransformation**</span></span>](d3dxmatrixaffinetransformation.md)
</dt> <dt>

[<span data-ttu-id="f8c53-163">轉換 (Direct3D 9) </span><span class="sxs-lookup"><span data-stu-id="f8c53-163">Transforms (Direct3D 9)</span></span>](transforms.md)
</dt> </dl>

 

 




