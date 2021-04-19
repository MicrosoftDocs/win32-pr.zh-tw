---
description: 建立2D 轉換矩陣，表示 xy 平面中的轉換。 Null 引數會被視為身分識別轉換。
ms.assetid: 671d3d67-b474-4fc1-9913-d21f05d66d9a
title: 'D3DXMatrixTransformation2D 函式 (D3dx9math) '
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- D3DXMatrixTransformation2D
api_type:
- LibDef
api_location:
- d3dx9.lib
- d3dx9.dll
ms.openlocfilehash: ead4d403917b5328776b33563bc477c28983d6ef
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 03/15/2021
ms.locfileid: "106991460"
---
# <a name="d3dxmatrixtransformation2d-function-d3dx9mathh"></a><span data-ttu-id="4b130-104">D3DXMatrixTransformation2D 函式 (D3dx9math) </span><span class="sxs-lookup"><span data-stu-id="4b130-104">D3DXMatrixTransformation2D function (D3dx9math.h)</span></span>

<span data-ttu-id="4b130-105">建立2D 轉換矩陣，表示 xy 平面中的轉換。</span><span class="sxs-lookup"><span data-stu-id="4b130-105">Builds a 2D transformation matrix that represents transformations in the xy plane.</span></span> <span data-ttu-id="4b130-106">**Null** 引數會被視為身分識別轉換。</span><span class="sxs-lookup"><span data-stu-id="4b130-106">**NULL** arguments are treated as identity transformations.</span></span>

## <a name="syntax"></a><span data-ttu-id="4b130-107">語法</span><span class="sxs-lookup"><span data-stu-id="4b130-107">Syntax</span></span>


```C++
D3DXMATRIX* D3DXMatrixTransformation2D(
  _Inout_       D3DXMATRIX  *pOut,
  _In_    const D3DXVECTOR2 *pScalingCenter,
  _In_          FLOAT       pScalingRotation,
  _In_    const D3DXVECTOR2 *pScaling,
  _In_    const D3DXVECTOR2 *pRotationCenter,
  _In_          FLOAT       Rotation,
  _In_    const D3DXVECTOR2 *pTranslation
);
```



## <a name="parameters"></a><span data-ttu-id="4b130-108">參數</span><span class="sxs-lookup"><span data-stu-id="4b130-108">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="4b130-109">*不悅* \[in、out\]</span><span class="sxs-lookup"><span data-stu-id="4b130-109">*pOut* \[in, out\]</span></span>
</dt> <dd>

<span data-ttu-id="4b130-110">類型： **[ **D3DXMATRIX**](d3dxmatrix.md)\***</span><span class="sxs-lookup"><span data-stu-id="4b130-110">Type: **[**D3DXMATRIX**](d3dxmatrix.md)\***</span></span>

<span data-ttu-id="4b130-111">[**D3DXMATRIX**](d3dxmatrix.md)結構的指標，其中包含轉換的結果。</span><span class="sxs-lookup"><span data-stu-id="4b130-111">Pointer to the [**D3DXMATRIX**](d3dxmatrix.md) structure that contains the result of the transformations.</span></span>

</dd> <dt>

<span data-ttu-id="4b130-112">*pScalingCenter* \[在\]</span><span class="sxs-lookup"><span data-stu-id="4b130-112">*pScalingCenter* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="4b130-113">Type： **Const [**D3DXVECTOR2**](d3dxvector2.md) \***</span><span class="sxs-lookup"><span data-stu-id="4b130-113">Type: **const [**D3DXVECTOR2**](d3dxvector2.md)\***</span></span>

<span data-ttu-id="4b130-114">[**D3DXVECTOR2**](d3dxvector2.md)結構的指標，也就是識別縮放中心的點。</span><span class="sxs-lookup"><span data-stu-id="4b130-114">Pointer to a [**D3DXVECTOR2**](d3dxvector2.md) structure, a point identifying the scaling center.</span></span> <span data-ttu-id="4b130-115">如果這個引數是 **Null**，則會將身分識別 M <sub>sc</sub> 矩陣套用至備註中的公式。</span><span class="sxs-lookup"><span data-stu-id="4b130-115">If this argument is **NULL**, an identity M<sub>sc</sub> matrix is applied to the formula in Remarks.</span></span>

</dd> <dt>

<span data-ttu-id="4b130-116">*pScalingRotation* \[在\]</span><span class="sxs-lookup"><span data-stu-id="4b130-116">*pScalingRotation* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="4b130-117">類型： **[ **FLOAT**](../winprog/windows-data-types.md)**</span><span class="sxs-lookup"><span data-stu-id="4b130-117">Type: **[**FLOAT**](../winprog/windows-data-types.md)**</span></span>

<span data-ttu-id="4b130-118">縮放旋轉係數。</span><span class="sxs-lookup"><span data-stu-id="4b130-118">The scaling rotation factor.</span></span>

</dd> <dt>

<span data-ttu-id="4b130-119">*pScaling* \[在\]</span><span class="sxs-lookup"><span data-stu-id="4b130-119">*pScaling* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="4b130-120">Type： **Const [**D3DXVECTOR2**](d3dxvector2.md) \***</span><span class="sxs-lookup"><span data-stu-id="4b130-120">Type: **const [**D3DXVECTOR2**](d3dxvector2.md)\***</span></span>

<span data-ttu-id="4b130-121">[**D3DXVECTOR2**](d3dxvector2.md)結構的指標，也就是識別尺規的點。</span><span class="sxs-lookup"><span data-stu-id="4b130-121">Pointer to a [**D3DXVECTOR2**](d3dxvector2.md) structure, a point identifying the scale.</span></span> <span data-ttu-id="4b130-122">如果這個引數是 **Null**，則會將身分識別 Ms 矩陣套用至備註中的公式。</span><span class="sxs-lookup"><span data-stu-id="4b130-122">If this argument is **NULL**, an identity Mₛ matrix is applied to the formula in Remarks.</span></span>

</dd> <dt>

<span data-ttu-id="4b130-123">*pRotationCenter* \[在\]</span><span class="sxs-lookup"><span data-stu-id="4b130-123">*pRotationCenter* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="4b130-124">Type： **Const [**D3DXVECTOR2**](d3dxvector2.md) \***</span><span class="sxs-lookup"><span data-stu-id="4b130-124">Type: **const [**D3DXVECTOR2**](d3dxvector2.md)\***</span></span>

<span data-ttu-id="4b130-125">[**D3DXVECTOR2**](d3dxvector2.md)結構的指標，也就是識別旋轉中心的點。</span><span class="sxs-lookup"><span data-stu-id="4b130-125">Pointer to a [**D3DXVECTOR2**](d3dxvector2.md) structure, a point identifying the rotation center.</span></span> <span data-ttu-id="4b130-126">如果此引數為 **Null**，則會將身分識別 M <sub>rc</sub> 矩陣套用至備註中的公式。</span><span class="sxs-lookup"><span data-stu-id="4b130-126">If this argument is **NULL**, an identity M<sub>rc</sub> matrix is applied to the formula in Remarks.</span></span>

</dd> <dt>

<span data-ttu-id="4b130-127">*旋轉* \[在\]</span><span class="sxs-lookup"><span data-stu-id="4b130-127">*Rotation* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="4b130-128">類型： **[ **FLOAT**](../winprog/windows-data-types.md)**</span><span class="sxs-lookup"><span data-stu-id="4b130-128">Type: **[**FLOAT**](../winprog/windows-data-types.md)**</span></span>

<span data-ttu-id="4b130-129">旋轉的角度，以弧度為單位。</span><span class="sxs-lookup"><span data-stu-id="4b130-129">The angle of rotation in radians.</span></span>

</dd> <dt>

<span data-ttu-id="4b130-130">*pTranslation* \[在\]</span><span class="sxs-lookup"><span data-stu-id="4b130-130">*pTranslation* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="4b130-131">Type： **Const [**D3DXVECTOR2**](d3dxvector2.md) \***</span><span class="sxs-lookup"><span data-stu-id="4b130-131">Type: **const [**D3DXVECTOR2**](d3dxvector2.md)\***</span></span>

<span data-ttu-id="4b130-132">[**D3DXVECTOR2**](d3dxvector2.md)結構的指標，識別翻譯。</span><span class="sxs-lookup"><span data-stu-id="4b130-132">Pointer to a [**D3DXVECTOR2**](d3dxvector2.md) structure, identifying the translation.</span></span> <span data-ttu-id="4b130-133">如果此引數為 **Null**，則會將身分識別 Mt 矩陣套用至備註中的公式。</span><span class="sxs-lookup"><span data-stu-id="4b130-133">If this argument is **NULL**, an identity Mₜ matrix is applied to the formula in Remarks.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="4b130-134">傳回值</span><span class="sxs-lookup"><span data-stu-id="4b130-134">Return value</span></span>

<span data-ttu-id="4b130-135">類型： **[ **D3DXMATRIX**](d3dxmatrix.md)\***</span><span class="sxs-lookup"><span data-stu-id="4b130-135">Type: **[**D3DXMATRIX**](d3dxmatrix.md)\***</span></span>

<span data-ttu-id="4b130-136">[**D3DXMATRIX**](d3dxmatrix.md)結構的指標，其中包含轉換矩陣。</span><span class="sxs-lookup"><span data-stu-id="4b130-136">Pointer to a [**D3DXMATRIX**](d3dxmatrix.md) structure that contains the transformation matrix.</span></span>

## <a name="remarks"></a><span data-ttu-id="4b130-137">備註</span><span class="sxs-lookup"><span data-stu-id="4b130-137">Remarks</span></span>

<span data-ttu-id="4b130-138">此函式會使用下列公式來計算轉換矩陣，並以由左至右順序評估矩陣串連：</span><span class="sxs-lookup"><span data-stu-id="4b130-138">This function calculates the transformation matrix with the following formula, with matrix concatenation evaluated in left-to-right order:</span></span>

<span data-ttu-id="4b130-139">M<sub>out</sub> = (m<sub>sc</sub>) ⁻¹ \* (M<sub>sr</sub>) ⁻¹ \* Ms \* M<sub>sr</sub> \* M<sub>sc</sub> \* (M<sub>rc</sub>) ⁻¹ \* m<sub>r</sub> \* m<sub>rc</sub> \* Mt</span><span class="sxs-lookup"><span data-stu-id="4b130-139">M<sub>out</sub> = (M<sub>sc</sub>)⁻¹\* (M<sub>sr</sub>)⁻¹\* Mₛ \* M<sub>sr</sub> \* M<sub>sc</sub> \* (M<sub>rc</sub>)⁻¹\* M<sub>r</sub> \* M<sub>rc</sub> \* Mₜ</span></span>

<span data-ttu-id="4b130-140">其中：</span><span class="sxs-lookup"><span data-stu-id="4b130-140">where:</span></span>

<span data-ttu-id="4b130-141">M <sub>out</sub> = 輸出矩陣 (*不悅*) </span><span class="sxs-lookup"><span data-stu-id="4b130-141">M <sub>out</sub> = output matrix (*pOut*)</span></span>

<span data-ttu-id="4b130-142">M <sub>sc</sub> = 縮放中心矩陣 (*pScalingCenter*) </span><span class="sxs-lookup"><span data-stu-id="4b130-142">M <sub>sc</sub> = scaling center matrix (*pScalingCenter*)</span></span>

<span data-ttu-id="4b130-143">M <sub>sr</sub> = 調整旋轉矩陣 (*pScalingRotation*) </span><span class="sxs-lookup"><span data-stu-id="4b130-143">M <sub>sr</sub> = scaling rotation matrix (*pScalingRotation*)</span></span>

<span data-ttu-id="4b130-144">Ms = 調整矩陣 (*pScaling*) </span><span class="sxs-lookup"><span data-stu-id="4b130-144">Mₛ = scaling matrix (*pScaling*)</span></span>

<span data-ttu-id="4b130-145">M <sub>rc</sub> = 旋轉矩陣的中心 (*pRotationCenter*) </span><span class="sxs-lookup"><span data-stu-id="4b130-145">M <sub>rc</sub> = center of rotation matrix (*pRotationCenter*)</span></span>

<span data-ttu-id="4b130-146">M <sub>r</sub> = 旋轉矩陣 (*旋轉*) </span><span class="sxs-lookup"><span data-stu-id="4b130-146">M <sub>r</sub> = rotation matrix (*Rotation*)</span></span>

<span data-ttu-id="4b130-147">Mt = 轉譯矩陣 (*pTranslation*) </span><span class="sxs-lookup"><span data-stu-id="4b130-147">Mₜ = translation matrix (*pTranslation*)</span></span>

<span data-ttu-id="4b130-148">此函式的傳回值與不悅參數中所傳回的值相同。</span><span class="sxs-lookup"><span data-stu-id="4b130-148">The return value for this function is the same value returned in the pOut parameter.</span></span> <span data-ttu-id="4b130-149">如此一來， **D3DXMatrixTransformation2D** 函式就可以用來做為另一個函式的參數。</span><span class="sxs-lookup"><span data-stu-id="4b130-149">In this way, the **D3DXMatrixTransformation2D** function can be used as a parameter for another function.</span></span>

<span data-ttu-id="4b130-150">若為3D 轉換，請使用 [**D3DXMatrixTransformation**](d3dxmatrixtransformation.md)。</span><span class="sxs-lookup"><span data-stu-id="4b130-150">For 3D transformations, use [**D3DXMatrixTransformation**](d3dxmatrixtransformation.md).</span></span>

## <a name="requirements"></a><span data-ttu-id="4b130-151">規格需求</span><span class="sxs-lookup"><span data-stu-id="4b130-151">Requirements</span></span>



| <span data-ttu-id="4b130-152">需求</span><span class="sxs-lookup"><span data-stu-id="4b130-152">Requirement</span></span> | <span data-ttu-id="4b130-153">值</span><span class="sxs-lookup"><span data-stu-id="4b130-153">Value</span></span> |
|--------------------|----------------------------------------------------------------------------------------|
| <span data-ttu-id="4b130-154">標頭</span><span class="sxs-lookup"><span data-stu-id="4b130-154">Header</span></span><br/>  | <dl> <span data-ttu-id="4b130-155"><dt>D3dx9math。h</dt></span><span class="sxs-lookup"><span data-stu-id="4b130-155"><dt>D3dx9math.h</dt></span></span> </dl> |
| <span data-ttu-id="4b130-156">程式庫</span><span class="sxs-lookup"><span data-stu-id="4b130-156">Library</span></span><br/> | <dl> <span data-ttu-id="4b130-157"><dt>D3dx9 .lib</dt></span><span class="sxs-lookup"><span data-stu-id="4b130-157"><dt>D3dx9.lib</dt></span></span> </dl>   |



## <a name="see-also"></a><span data-ttu-id="4b130-158">另請參閱</span><span class="sxs-lookup"><span data-stu-id="4b130-158">See also</span></span>

<dl> <dt>

[<span data-ttu-id="4b130-159">數學函數</span><span class="sxs-lookup"><span data-stu-id="4b130-159">Math Functions</span></span>](dx9-graphics-reference-d3dx-functions-math.md)
</dt> <dt>

[<span data-ttu-id="4b130-160">**D3DXMatrixAffineTransformation2D**</span><span class="sxs-lookup"><span data-stu-id="4b130-160">**D3DXMatrixAffineTransformation2D**</span></span>](d3dxmatrixaffinetransformation2d.md)
</dt> <dt>

[<span data-ttu-id="4b130-161">轉換 (Direct3D 9) </span><span class="sxs-lookup"><span data-stu-id="4b130-161">Transforms (Direct3D 9)</span></span>](transforms.md)
</dt> </dl>

 

 
