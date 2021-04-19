---
description: 在 x-y 平面中建立2D 仿射轉換矩陣。 Null 引數會被視為身分識別轉換。
ms.assetid: f46a307c-4566-42c8-8def-fb189116144e
title: 'D3DXMatrixAffineTransformation2D 函式 (D3DX10Math) '
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- D3DXMatrixAffineTransformation2D
api_type:
- LibDef
api_location:
- D3DX10.lib
- D3DX10.dll
ms.openlocfilehash: 223ef5d2d9a68c993553d52f5d4cf63e8b95dd3b
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 03/15/2021
ms.locfileid: "106999306"
---
# <a name="d3dxmatrixaffinetransformation2d-function-d3dx10mathh"></a><span data-ttu-id="23c58-104">D3DXMatrixAffineTransformation2D 函式 (D3DX10Math) </span><span class="sxs-lookup"><span data-stu-id="23c58-104">D3DXMatrixAffineTransformation2D function (D3DX10Math.h)</span></span>

<span data-ttu-id="23c58-105">在 x-y 平面中建立2D 仿射轉換矩陣。</span><span class="sxs-lookup"><span data-stu-id="23c58-105">Builds a 2D affine transformation matrix in the x-y plane.</span></span> <span data-ttu-id="23c58-106">**Null** 引數會被視為身分識別轉換。</span><span class="sxs-lookup"><span data-stu-id="23c58-106">**NULL** arguments are treated as identity transformations.</span></span>

## <a name="syntax"></a><span data-ttu-id="23c58-107">語法</span><span class="sxs-lookup"><span data-stu-id="23c58-107">Syntax</span></span>


```C++
D3DXMATRIX* D3DXMatrixAffineTransformation2D(
  _In_       D3DXMATRIX  *pOut,
  _In_       FLOAT       Scaling,
  _In_ const D3DXVECTOR2 *pRotationCenter,
  _In_       FLOAT       Rotation,
  _In_ const D3DXVECTOR2 *pTranslation
);
```



## <a name="parameters"></a><span data-ttu-id="23c58-108">參數</span><span class="sxs-lookup"><span data-stu-id="23c58-108">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="23c58-109">*不悅* \[在\]</span><span class="sxs-lookup"><span data-stu-id="23c58-109">*pOut* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="23c58-110">類型： **[ **D3DXMATRIX**](../direct3d9/d3dxmatrix.md)\***</span><span class="sxs-lookup"><span data-stu-id="23c58-110">Type: **[**D3DXMATRIX**](../direct3d9/d3dxmatrix.md)\***</span></span>

<span data-ttu-id="23c58-111">作業結果之 [**D3DXMATRIX**](d3d10-d3dxmatrix.md) 的指標。</span><span class="sxs-lookup"><span data-stu-id="23c58-111">Pointer to the [**D3DXMATRIX**](d3d10-d3dxmatrix.md) that is the result of the operation.</span></span>

</dd> <dt>

<span data-ttu-id="23c58-112">*調整* \[在\]</span><span class="sxs-lookup"><span data-stu-id="23c58-112">*Scaling* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="23c58-113">類型： **[ **FLOAT**](../winprog/windows-data-types.md)**</span><span class="sxs-lookup"><span data-stu-id="23c58-113">Type: **[**FLOAT**](../winprog/windows-data-types.md)**</span></span>

<span data-ttu-id="23c58-114">調整係數。</span><span class="sxs-lookup"><span data-stu-id="23c58-114">Scaling factor.</span></span>

</dd> <dt>

<span data-ttu-id="23c58-115">*pRotationCenter* \[在\]</span><span class="sxs-lookup"><span data-stu-id="23c58-115">*pRotationCenter* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="23c58-116">Type： **Const [**D3DXVECTOR2**](../direct3d9/d3dxvector2.md) \***</span><span class="sxs-lookup"><span data-stu-id="23c58-116">Type: **const [**D3DXVECTOR2**](../direct3d9/d3dxvector2.md)\***</span></span>

<span data-ttu-id="23c58-117">[**D3DXVECTOR2**](d3d10-d3dxvector2.md)的指標，也就是識別旋轉中心的點。</span><span class="sxs-lookup"><span data-stu-id="23c58-117">Pointer to a [**D3DXVECTOR2**](d3d10-d3dxvector2.md), a point identifying the center of rotation.</span></span> <span data-ttu-id="23c58-118">如果此引數為 **Null**，則會將身分識別 M <sub>rc</sub> 矩陣套用至備註中的公式。</span><span class="sxs-lookup"><span data-stu-id="23c58-118">If this argument is **NULL**, an identity M<sub>rc</sub> matrix is applied to the formula in Remarks.</span></span>

</dd> <dt>

<span data-ttu-id="23c58-119">*旋轉* \[在\]</span><span class="sxs-lookup"><span data-stu-id="23c58-119">*Rotation* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="23c58-120">類型： **[ **FLOAT**](../winprog/windows-data-types.md)**</span><span class="sxs-lookup"><span data-stu-id="23c58-120">Type: **[**FLOAT**](../winprog/windows-data-types.md)**</span></span>

<span data-ttu-id="23c58-121">旋轉的角度。</span><span class="sxs-lookup"><span data-stu-id="23c58-121">The angle of rotation.</span></span>

</dd> <dt>

<span data-ttu-id="23c58-122">*pTranslation* \[在\]</span><span class="sxs-lookup"><span data-stu-id="23c58-122">*pTranslation* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="23c58-123">Type： **Const [**D3DXVECTOR2**](../direct3d9/d3dxvector2.md) \***</span><span class="sxs-lookup"><span data-stu-id="23c58-123">Type: **const [**D3DXVECTOR2**](../direct3d9/d3dxvector2.md)\***</span></span>

<span data-ttu-id="23c58-124">[**D3DXVECTOR2**](d3d10-d3dxvector2.md)的指標，表示轉譯。</span><span class="sxs-lookup"><span data-stu-id="23c58-124">Pointer to a [**D3DXVECTOR2**](d3d10-d3dxvector2.md), representing the translation.</span></span> <span data-ttu-id="23c58-125">如果此引數為 **Null**，則會將身分識別 Mt 矩陣套用至備註中的公式。</span><span class="sxs-lookup"><span data-stu-id="23c58-125">If this argument is **NULL**, an identity Mₜ matrix is applied to the formula in Remarks.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="23c58-126">傳回值</span><span class="sxs-lookup"><span data-stu-id="23c58-126">Return value</span></span>

<span data-ttu-id="23c58-127">類型： **[ **D3DXMATRIX**](../direct3d9/d3dxmatrix.md)\***</span><span class="sxs-lookup"><span data-stu-id="23c58-127">Type: **[**D3DXMATRIX**](../direct3d9/d3dxmatrix.md)\***</span></span>

<span data-ttu-id="23c58-128">D3DXMATRIX 結構的指標，此結構是仿射轉換矩陣。</span><span class="sxs-lookup"><span data-stu-id="23c58-128">Pointer to a D3DXMATRIX structure that is an affine transformation matrix.</span></span>

## <a name="remarks"></a><span data-ttu-id="23c58-129">備註</span><span class="sxs-lookup"><span data-stu-id="23c58-129">Remarks</span></span>

<span data-ttu-id="23c58-130">此函式會使用下列公式來計算仿射轉換矩陣，並以由左至右順序評估矩陣串連：</span><span class="sxs-lookup"><span data-stu-id="23c58-130">This function calculates the affine transformation matrix with the following formula, with matrix concatenation evaluated in left-to-right order:</span></span>

<span data-ttu-id="23c58-131">M<sub>out</sub> = Ms \* (M<sub>rc</sub>) -1 \* M<sub>r</sub> \* m<sub>rc</sub> \* Mt</span><span class="sxs-lookup"><span data-stu-id="23c58-131">M<sub>out</sub> = Mₛ \* (M<sub>rc</sub>)-1 \* M<sub>r</sub> \* M<sub>rc</sub> \* Mₜ</span></span>

<span data-ttu-id="23c58-132">其中：</span><span class="sxs-lookup"><span data-stu-id="23c58-132">where:</span></span>

<span data-ttu-id="23c58-133">M<sub>out</sub> = 輸出矩陣 (不悅) </span><span class="sxs-lookup"><span data-stu-id="23c58-133">M<sub>out</sub> = output matrix (pOut)</span></span>

<span data-ttu-id="23c58-134">Ms = 調整矩陣 (調整) </span><span class="sxs-lookup"><span data-stu-id="23c58-134">Mₛ = scaling matrix (Scaling)</span></span>

<span data-ttu-id="23c58-135">M<sub>rc</sub> = 旋轉矩陣的中心 (pRotationCenter) </span><span class="sxs-lookup"><span data-stu-id="23c58-135">M<sub>rc</sub> = center of rotation matrix (pRotationCenter)</span></span>

<span data-ttu-id="23c58-136">M<sub>r</sub> = 旋轉矩陣 (旋轉) </span><span class="sxs-lookup"><span data-stu-id="23c58-136">M<sub>r</sub> = rotation matrix (Rotation)</span></span>

<span data-ttu-id="23c58-137">Mt = 轉譯矩陣 (pTranslation) </span><span class="sxs-lookup"><span data-stu-id="23c58-137">Mₜ = translation matrix (pTranslation)</span></span>

<span data-ttu-id="23c58-138">此函式的傳回值與不悅參數中所傳回的值相同。</span><span class="sxs-lookup"><span data-stu-id="23c58-138">The return value for this function is the same value returned in the pOut parameter.</span></span> <span data-ttu-id="23c58-139">如此一來，D3DXMatrixAffineTransformation2D 函式就可以用來做為另一個函式的參數。</span><span class="sxs-lookup"><span data-stu-id="23c58-139">In this way, the D3DXMatrixAffineTransformation2D function can be used as a parameter for another function.</span></span>

<span data-ttu-id="23c58-140">若為3D 仿射轉換，請使用 D3DXMatrixAffineTransformation。</span><span class="sxs-lookup"><span data-stu-id="23c58-140">For 3D affine transformations, use D3DXMatrixAffineTransformation.</span></span>

## <a name="requirements"></a><span data-ttu-id="23c58-141">規格需求</span><span class="sxs-lookup"><span data-stu-id="23c58-141">Requirements</span></span>



| <span data-ttu-id="23c58-142">需求</span><span class="sxs-lookup"><span data-stu-id="23c58-142">Requirement</span></span> | <span data-ttu-id="23c58-143">值</span><span class="sxs-lookup"><span data-stu-id="23c58-143">Value</span></span> |
|--------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="23c58-144">標頭</span><span class="sxs-lookup"><span data-stu-id="23c58-144">Header</span></span><br/>  | <dl> <span data-ttu-id="23c58-145"><dt>D3DX10Math。h</dt></span><span class="sxs-lookup"><span data-stu-id="23c58-145"><dt>D3DX10Math.h</dt></span></span> </dl> |
| <span data-ttu-id="23c58-146">程式庫</span><span class="sxs-lookup"><span data-stu-id="23c58-146">Library</span></span><br/> | <dl> <span data-ttu-id="23c58-147"><dt>D3DX10 .lib</dt></span><span class="sxs-lookup"><span data-stu-id="23c58-147"><dt>D3DX10.lib</dt></span></span> </dl>   |



## <a name="see-also"></a><span data-ttu-id="23c58-148">另請參閱</span><span class="sxs-lookup"><span data-stu-id="23c58-148">See also</span></span>

<dl> <dt>

[<span data-ttu-id="23c58-149">數學函數</span><span class="sxs-lookup"><span data-stu-id="23c58-149">Math Functions</span></span>](d3d10-graphics-reference-d3dx10-functions-math.md)
</dt> </dl>

 

 
