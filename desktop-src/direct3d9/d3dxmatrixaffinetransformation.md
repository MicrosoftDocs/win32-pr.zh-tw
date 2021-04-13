---
description: 建立3D 仿射轉換矩陣。 Null 引數會被視為身分識別轉換。
ms.assetid: 54eac78f-57be-4a24-8dfb-0b519e97d6ca
title: 'D3DXMatrixAffineTransformation 函式 (D3dx9math) '
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- D3DXMatrixAffineTransformation
api_type:
- LibDef
api_location:
- d3dx9.lib
- d3dx9.dll
ms.openlocfilehash: 025485f0015e6f2d85851c8f0919f5462b2bdc3e
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 03/15/2021
ms.locfileid: "104323152"
---
# <a name="d3dxmatrixaffinetransformation-function-d3dx9mathh"></a><span data-ttu-id="2a45a-104">D3DXMatrixAffineTransformation 函式 (D3dx9math) </span><span class="sxs-lookup"><span data-stu-id="2a45a-104">D3DXMatrixAffineTransformation function (D3dx9math.h)</span></span>

<span data-ttu-id="2a45a-105">建立3D 仿射轉換矩陣。</span><span class="sxs-lookup"><span data-stu-id="2a45a-105">Builds a 3D affine transformation matrix.</span></span> <span data-ttu-id="2a45a-106">**Null** 引數會被視為身分識別轉換。</span><span class="sxs-lookup"><span data-stu-id="2a45a-106">**NULL** arguments are treated as identity transformations.</span></span>

## <a name="syntax"></a><span data-ttu-id="2a45a-107">語法</span><span class="sxs-lookup"><span data-stu-id="2a45a-107">Syntax</span></span>


```C++
D3DXMATRIX* D3DXMatrixAffineTransformation(
  _Inout_       D3DXMATRIX     *pOut,
  _In_          FLOAT          Scaling,
  _In_    const D3DXVECTOR3    *pRotationCenter,
  _In_    const D3DXQUATERNION *pRotation,
  _In_    const D3DXVECTOR3    *pTranslation
);
```



## <a name="parameters"></a><span data-ttu-id="2a45a-108">參數</span><span class="sxs-lookup"><span data-stu-id="2a45a-108">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="2a45a-109">*不悅* \[in、out\]</span><span class="sxs-lookup"><span data-stu-id="2a45a-109">*pOut* \[in, out\]</span></span>
</dt> <dd>

<span data-ttu-id="2a45a-110">類型： **[ **D3DXMATRIX**](d3dxmatrix.md)\***</span><span class="sxs-lookup"><span data-stu-id="2a45a-110">Type: **[**D3DXMATRIX**](d3dxmatrix.md)\***</span></span>

<span data-ttu-id="2a45a-111">[**D3DXMATRIX**](d3dxmatrix.md)結構的指標，此結構是作業的結果。</span><span class="sxs-lookup"><span data-stu-id="2a45a-111">Pointer to the [**D3DXMATRIX**](d3dxmatrix.md) structure that is the result of the operation.</span></span>

</dd> <dt>

<span data-ttu-id="2a45a-112">*調整* \[在\]</span><span class="sxs-lookup"><span data-stu-id="2a45a-112">*Scaling* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="2a45a-113">類型： **[ **FLOAT**](../winprog/windows-data-types.md)**</span><span class="sxs-lookup"><span data-stu-id="2a45a-113">Type: **[**FLOAT**](../winprog/windows-data-types.md)**</span></span>

<span data-ttu-id="2a45a-114">調整係數。</span><span class="sxs-lookup"><span data-stu-id="2a45a-114">Scaling factor.</span></span>

</dd> <dt>

<span data-ttu-id="2a45a-115">*pRotationCenter* \[在\]</span><span class="sxs-lookup"><span data-stu-id="2a45a-115">*pRotationCenter* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="2a45a-116">Type： **Const [**D3DXVECTOR3**](d3dxvector3.md) \***</span><span class="sxs-lookup"><span data-stu-id="2a45a-116">Type: **const [**D3DXVECTOR3**](d3dxvector3.md)\***</span></span>

<span data-ttu-id="2a45a-117">[**D3DXVECTOR3**](d3dxvector3.md)結構的指標，也就是識別旋轉中心的點。</span><span class="sxs-lookup"><span data-stu-id="2a45a-117">Pointer to a [**D3DXVECTOR3**](d3dxvector3.md) structure, a point identifying the center of rotation.</span></span> <span data-ttu-id="2a45a-118">如果此引數為 **Null**，則會將身分識別 M <sub>rc</sub> 矩陣套用至備註中的公式。</span><span class="sxs-lookup"><span data-stu-id="2a45a-118">If this argument is **NULL**, an identity M<sub>rc</sub> matrix is applied to the formula in Remarks.</span></span>

</dd> <dt>

<span data-ttu-id="2a45a-119">*pRotation* \[在\]</span><span class="sxs-lookup"><span data-stu-id="2a45a-119">*pRotation* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="2a45a-120">Type： **Const [**D3DXQUATERNION**](d3dxquaternion.md) \***</span><span class="sxs-lookup"><span data-stu-id="2a45a-120">Type: **const [**D3DXQUATERNION**](d3dxquaternion.md)\***</span></span>

<span data-ttu-id="2a45a-121">指定旋轉之 [**D3DXQUATERNION**](d3dxquaternion.md) 結構的指標。</span><span class="sxs-lookup"><span data-stu-id="2a45a-121">Pointer to a [**D3DXQUATERNION**](d3dxquaternion.md) structure that specifies the rotation.</span></span> <span data-ttu-id="2a45a-122">如果這個引數是 **Null**，則會將身分識別 M <sub>r</sub> 矩陣套用至備註中的公式。</span><span class="sxs-lookup"><span data-stu-id="2a45a-122">If this argument is **NULL**, an identity M<sub>r</sub> matrix is applied to the formula in Remarks.</span></span>

</dd> <dt>

<span data-ttu-id="2a45a-123">*pTranslation* \[在\]</span><span class="sxs-lookup"><span data-stu-id="2a45a-123">*pTranslation* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="2a45a-124">Type： **Const [**D3DXVECTOR3**](d3dxvector3.md) \***</span><span class="sxs-lookup"><span data-stu-id="2a45a-124">Type: **const [**D3DXVECTOR3**](d3dxvector3.md)\***</span></span>

<span data-ttu-id="2a45a-125">表示轉譯之 [**D3DXVECTOR3**](d3dxvector3.md) 結構的指標。</span><span class="sxs-lookup"><span data-stu-id="2a45a-125">Pointer to a [**D3DXVECTOR3**](d3dxvector3.md) structure representing the translation.</span></span> <span data-ttu-id="2a45a-126">如果此引數為 **Null**，則會將身分識別 Mt 矩陣套用至備註中的公式。</span><span class="sxs-lookup"><span data-stu-id="2a45a-126">If this argument is **NULL**, an identity Mₜ matrix is applied to the formula in Remarks.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="2a45a-127">傳回值</span><span class="sxs-lookup"><span data-stu-id="2a45a-127">Return value</span></span>

<span data-ttu-id="2a45a-128">類型： **[ **D3DXMATRIX**](d3dxmatrix.md)\***</span><span class="sxs-lookup"><span data-stu-id="2a45a-128">Type: **[**D3DXMATRIX**](d3dxmatrix.md)\***</span></span>

<span data-ttu-id="2a45a-129">[**D3DXMATRIX**](d3dxmatrix.md)結構的指標，此結構是仿射轉換矩陣。</span><span class="sxs-lookup"><span data-stu-id="2a45a-129">Pointer to a [**D3DXMATRIX**](d3dxmatrix.md) structure that is an affine transformation matrix.</span></span>

## <a name="remarks"></a><span data-ttu-id="2a45a-130">備註</span><span class="sxs-lookup"><span data-stu-id="2a45a-130">Remarks</span></span>

<span data-ttu-id="2a45a-131">此函式會使用下列公式來計算仿射轉換矩陣，並以由左至右順序評估矩陣串連：</span><span class="sxs-lookup"><span data-stu-id="2a45a-131">This function calculates the affine transformation matrix with the following formula, with matrix concatenation evaluated in left-to-right order:</span></span>

<span data-ttu-id="2a45a-132">M<sub>out</sub> = Ms \* (M<sub>rc</sub>) ⁻¹ \* m<sub>r</sub> \* m<sub>rc</sub> \* Mt</span><span class="sxs-lookup"><span data-stu-id="2a45a-132">M<sub>out</sub> = Mₛ \* (M<sub>rc</sub>)⁻¹ \* M<sub>r</sub> \* M<sub>rc</sub> \* Mₜ</span></span>

<span data-ttu-id="2a45a-133">其中：</span><span class="sxs-lookup"><span data-stu-id="2a45a-133">where:</span></span>

<span data-ttu-id="2a45a-134">M <sub>out</sub> = 輸出矩陣 (*不悅*) </span><span class="sxs-lookup"><span data-stu-id="2a45a-134">M <sub>out</sub> = output matrix (*pOut*)</span></span>

<span data-ttu-id="2a45a-135">Ms = 調整矩陣 (*調整*) </span><span class="sxs-lookup"><span data-stu-id="2a45a-135">Mₛ = scaling matrix (*Scaling*)</span></span>

<span data-ttu-id="2a45a-136">M <sub>rc</sub> = 旋轉矩陣的中心 (*pRotationCenter*) </span><span class="sxs-lookup"><span data-stu-id="2a45a-136">M <sub>rc</sub> = center of rotation matrix (*pRotationCenter*)</span></span>

<span data-ttu-id="2a45a-137">M <sub>r</sub> = 旋轉矩陣 (*pRotation*) </span><span class="sxs-lookup"><span data-stu-id="2a45a-137">M <sub>r</sub> = rotation matrix (*pRotation*)</span></span>

<span data-ttu-id="2a45a-138">Mt = 轉譯矩陣 (*pTranslation*) </span><span class="sxs-lookup"><span data-stu-id="2a45a-138">Mₜ = translation matrix (*pTranslation*)</span></span>

<span data-ttu-id="2a45a-139">此函式的傳回值與不悅參數中所傳回的值相同。</span><span class="sxs-lookup"><span data-stu-id="2a45a-139">The return value for this function is the same value returned in the pOut parameter.</span></span> <span data-ttu-id="2a45a-140">如此一來， **D3DXMatrixAffineTransformation** 函式就可以用來做為另一個函式的參數。</span><span class="sxs-lookup"><span data-stu-id="2a45a-140">In this way, the **D3DXMatrixAffineTransformation** function can be used as a parameter for another function.</span></span>

<span data-ttu-id="2a45a-141">若是2D 仿射轉換，請使用 [**D3DXMatrixAffineTransformation2D**](d3dxmatrixaffinetransformation2d.md)。</span><span class="sxs-lookup"><span data-stu-id="2a45a-141">For 2D affine transformations, use [**D3DXMatrixAffineTransformation2D**](d3dxmatrixaffinetransformation2d.md).</span></span>

## <a name="requirements"></a><span data-ttu-id="2a45a-142">規格需求</span><span class="sxs-lookup"><span data-stu-id="2a45a-142">Requirements</span></span>



| <span data-ttu-id="2a45a-143">需求</span><span class="sxs-lookup"><span data-stu-id="2a45a-143">Requirement</span></span> | <span data-ttu-id="2a45a-144">值</span><span class="sxs-lookup"><span data-stu-id="2a45a-144">Value</span></span> |
|--------------------|----------------------------------------------------------------------------------------|
| <span data-ttu-id="2a45a-145">標頭</span><span class="sxs-lookup"><span data-stu-id="2a45a-145">Header</span></span><br/>  | <dl> <span data-ttu-id="2a45a-146"><dt>D3dx9math。h</dt></span><span class="sxs-lookup"><span data-stu-id="2a45a-146"><dt>D3dx9math.h</dt></span></span> </dl> |
| <span data-ttu-id="2a45a-147">程式庫</span><span class="sxs-lookup"><span data-stu-id="2a45a-147">Library</span></span><br/> | <dl> <span data-ttu-id="2a45a-148"><dt>D3dx9 .lib</dt></span><span class="sxs-lookup"><span data-stu-id="2a45a-148"><dt>D3dx9.lib</dt></span></span> </dl>   |



## <a name="see-also"></a><span data-ttu-id="2a45a-149">另請參閱</span><span class="sxs-lookup"><span data-stu-id="2a45a-149">See also</span></span>

<dl> <dt>

[<span data-ttu-id="2a45a-150">數學函數</span><span class="sxs-lookup"><span data-stu-id="2a45a-150">Math Functions</span></span>](dx9-graphics-reference-d3dx-functions-math.md)
</dt> <dt>

[<span data-ttu-id="2a45a-151">**D3DXMatrixTransformation**</span><span class="sxs-lookup"><span data-stu-id="2a45a-151">**D3DXMatrixTransformation**</span></span>](d3dxmatrixtransformation.md)
</dt> <dt>

[<span data-ttu-id="2a45a-152">轉換 (Direct3D 9) </span><span class="sxs-lookup"><span data-stu-id="2a45a-152">Transforms (Direct3D 9)</span></span>](transforms.md)
</dt> </dl>

 

 
