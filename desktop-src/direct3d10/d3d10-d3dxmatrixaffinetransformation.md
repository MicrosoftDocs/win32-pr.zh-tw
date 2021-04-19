---
description: 建立3D 仿射轉換矩陣。 Null 引數會被視為身分識別轉換。
ms.assetid: 36044272-a8ce-47db-8f52-30dc680f8174
title: 'D3DXMatrixAffineTransformation 函式 (D3DX10Math) '
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
- D3DX10.lib
- D3DX10.dll
ms.openlocfilehash: 27fee5a620d75c3930b1bc2f8a85415db1320a47
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 03/15/2021
ms.locfileid: "106988213"
---
# <a name="d3dxmatrixaffinetransformation-function-d3dx10mathh"></a><span data-ttu-id="41830-104">D3DXMatrixAffineTransformation 函式 (D3DX10Math) </span><span class="sxs-lookup"><span data-stu-id="41830-104">D3DXMatrixAffineTransformation function (D3DX10Math.h)</span></span>

<span data-ttu-id="41830-105">建立3D 仿射轉換矩陣。</span><span class="sxs-lookup"><span data-stu-id="41830-105">Builds a 3D affine transformation matrix.</span></span> <span data-ttu-id="41830-106">**Null** 引數會被視為身分識別轉換。</span><span class="sxs-lookup"><span data-stu-id="41830-106">**NULL** arguments are treated as identity transformations.</span></span>

## <a name="syntax"></a><span data-ttu-id="41830-107">語法</span><span class="sxs-lookup"><span data-stu-id="41830-107">Syntax</span></span>


```C++
D3DXMATRIX* D3DXMatrixAffineTransformation(
  _In_       D3DXMATRIX     *pOut,
  _In_       FLOAT          Scaling,
  _In_ const D3DXVECTOR3    *pRotationCenter,
  _In_ const D3DXQUATERNION *pRotation,
  _In_ const D3DXVECTOR3    *pTranslation
);
```



## <a name="parameters"></a><span data-ttu-id="41830-108">參數</span><span class="sxs-lookup"><span data-stu-id="41830-108">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="41830-109">*不悅* \[在\]</span><span class="sxs-lookup"><span data-stu-id="41830-109">*pOut* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="41830-110">類型： **[ **D3DXMATRIX**](../direct3d9/d3dxmatrix.md)\***</span><span class="sxs-lookup"><span data-stu-id="41830-110">Type: **[**D3DXMATRIX**](../direct3d9/d3dxmatrix.md)\***</span></span>

<span data-ttu-id="41830-111">作業結果之 [**D3DXMATRIX**](d3d10-d3dxmatrix.md) 的指標。</span><span class="sxs-lookup"><span data-stu-id="41830-111">Pointer to the [**D3DXMATRIX**](d3d10-d3dxmatrix.md) that is the result of the operation.</span></span>

</dd> <dt>

<span data-ttu-id="41830-112">*調整* \[在\]</span><span class="sxs-lookup"><span data-stu-id="41830-112">*Scaling* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="41830-113">類型： **[ **FLOAT**](../winprog/windows-data-types.md)**</span><span class="sxs-lookup"><span data-stu-id="41830-113">Type: **[**FLOAT**](../winprog/windows-data-types.md)**</span></span>

<span data-ttu-id="41830-114">調整係數。</span><span class="sxs-lookup"><span data-stu-id="41830-114">Scaling factor.</span></span>

</dd> <dt>

<span data-ttu-id="41830-115">*pRotationCenter* \[在\]</span><span class="sxs-lookup"><span data-stu-id="41830-115">*pRotationCenter* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="41830-116">Type： **Const [**D3DXVECTOR3**](../direct3d9/d3dxvector3.md) \***</span><span class="sxs-lookup"><span data-stu-id="41830-116">Type: **const [**D3DXVECTOR3**](../direct3d9/d3dxvector3.md)\***</span></span>

<span data-ttu-id="41830-117">[**D3DXVECTOR3**](d3d10-d3dxvector3.md)的指標，也就是識別旋轉中心的點。</span><span class="sxs-lookup"><span data-stu-id="41830-117">Pointer to a [**D3DXVECTOR3**](d3d10-d3dxvector3.md), a point identifying the center of rotation.</span></span> <span data-ttu-id="41830-118">如果此引數為 **Null**，則會將身分識別 M <sub>rc</sub> 矩陣套用至備註中的公式。</span><span class="sxs-lookup"><span data-stu-id="41830-118">If this argument is **NULL**, an identity M<sub>rc</sub> matrix is applied to the formula in Remarks.</span></span>

</dd> <dt>

<span data-ttu-id="41830-119">*pRotation* \[在\]</span><span class="sxs-lookup"><span data-stu-id="41830-119">*pRotation* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="41830-120">Type： **Const [**D3DXQUATERNION**](../direct3d9/d3dxquaternion.md) \***</span><span class="sxs-lookup"><span data-stu-id="41830-120">Type: **const [**D3DXQUATERNION**](../direct3d9/d3dxquaternion.md)\***</span></span>

<span data-ttu-id="41830-121">指定旋轉之 [**D3DXQUATERNION**](d3d10-d3dxquaternion.md) 的指標。</span><span class="sxs-lookup"><span data-stu-id="41830-121">Pointer to a [**D3DXQUATERNION**](d3d10-d3dxquaternion.md) that specifies the rotation.</span></span> <span data-ttu-id="41830-122">如果這個引數是 **Null**，則會將身分識別 M <sub>r</sub> 矩陣套用至備註中的公式。</span><span class="sxs-lookup"><span data-stu-id="41830-122">If this argument is **NULL**, an identity M<sub>r</sub> matrix is applied to the formula in Remarks.</span></span>

</dd> <dt>

<span data-ttu-id="41830-123">*pTranslation* \[在\]</span><span class="sxs-lookup"><span data-stu-id="41830-123">*pTranslation* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="41830-124">Type： **Const [**D3DXVECTOR3**](../direct3d9/d3dxvector3.md) \***</span><span class="sxs-lookup"><span data-stu-id="41830-124">Type: **const [**D3DXVECTOR3**](../direct3d9/d3dxvector3.md)\***</span></span>

<span data-ttu-id="41830-125">表示轉譯之 D3DXVECTOR3 結構的指標。</span><span class="sxs-lookup"><span data-stu-id="41830-125">Pointer to a D3DXVECTOR3 structure representing the translation.</span></span> <span data-ttu-id="41830-126">如果此引數為 **Null**，則會將身分識別 Mt 矩陣套用至備註中的公式。</span><span class="sxs-lookup"><span data-stu-id="41830-126">If this argument is **NULL**, an identity Mₜ matrix is applied to the formula in Remarks.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="41830-127">傳回值</span><span class="sxs-lookup"><span data-stu-id="41830-127">Return value</span></span>

<span data-ttu-id="41830-128">類型： **[ **D3DXMATRIX**](../direct3d9/d3dxmatrix.md)\***</span><span class="sxs-lookup"><span data-stu-id="41830-128">Type: **[**D3DXMATRIX**](../direct3d9/d3dxmatrix.md)\***</span></span>

<span data-ttu-id="41830-129">D3DXMATRIX 結構的指標，此結構是仿射轉換矩陣。</span><span class="sxs-lookup"><span data-stu-id="41830-129">Pointer to a D3DXMATRIX structure that is an affine transformation matrix.</span></span>

## <a name="remarks"></a><span data-ttu-id="41830-130">備註</span><span class="sxs-lookup"><span data-stu-id="41830-130">Remarks</span></span>

<span data-ttu-id="41830-131">此函式會使用下列公式來計算仿射轉換矩陣，並以由左至右順序評估矩陣串連：</span><span class="sxs-lookup"><span data-stu-id="41830-131">This function calculates the affine transformation matrix with the following formula, with matrix concatenation evaluated in left-to-right order:</span></span>

<span data-ttu-id="41830-132">M<sub>out</sub> = Ms \* (M<sub>rc</sub>) -1 \* M<sub>r</sub> \* m<sub>rc</sub> \* Mt</span><span class="sxs-lookup"><span data-stu-id="41830-132">M<sub>out</sub> = Mₛ \* (M<sub>rc</sub>)-1 \* M<sub>r</sub> \* M<sub>rc</sub> \* Mₜ</span></span>

<span data-ttu-id="41830-133">其中：</span><span class="sxs-lookup"><span data-stu-id="41830-133">where:</span></span>

<span data-ttu-id="41830-134">M<sub>out</sub> = 輸出矩陣 (不悅) </span><span class="sxs-lookup"><span data-stu-id="41830-134">M<sub>out</sub> = output matrix (pOut)</span></span>

<span data-ttu-id="41830-135">Ms = 調整矩陣 (調整) </span><span class="sxs-lookup"><span data-stu-id="41830-135">Mₛ = scaling matrix (Scaling)</span></span>

<span data-ttu-id="41830-136">M<sub>rc</sub> = 旋轉矩陣的中心 (pRotationCenter) </span><span class="sxs-lookup"><span data-stu-id="41830-136">M<sub>rc</sub> = center of rotation matrix (pRotationCenter)</span></span>

<span data-ttu-id="41830-137">M<sub>r</sub> = 旋轉矩陣 (pRotation) </span><span class="sxs-lookup"><span data-stu-id="41830-137">M<sub>r</sub> = rotation matrix (pRotation)</span></span>

<span data-ttu-id="41830-138">Mt = 轉譯矩陣 (pTranslation) </span><span class="sxs-lookup"><span data-stu-id="41830-138">Mₜ = translation matrix (pTranslation)</span></span>

<span data-ttu-id="41830-139">此函式的傳回值與不悅參數中所傳回的值相同。</span><span class="sxs-lookup"><span data-stu-id="41830-139">The return value for this function is the same value returned in the pOut parameter.</span></span> <span data-ttu-id="41830-140">如此一來，D3DXMatrixAffineTransformation 函式就可以用來做為另一個函式的參數。</span><span class="sxs-lookup"><span data-stu-id="41830-140">In this way, the D3DXMatrixAffineTransformation function can be used as a parameter for another function.</span></span>

<span data-ttu-id="41830-141">若是2D 仿射轉換，請使用 D3DXMatrixAffineTransformation2D。</span><span class="sxs-lookup"><span data-stu-id="41830-141">For 2D affine transformations, use D3DXMatrixAffineTransformation2D.</span></span>

## <a name="requirements"></a><span data-ttu-id="41830-142">規格需求</span><span class="sxs-lookup"><span data-stu-id="41830-142">Requirements</span></span>



| <span data-ttu-id="41830-143">需求</span><span class="sxs-lookup"><span data-stu-id="41830-143">Requirement</span></span> | <span data-ttu-id="41830-144">值</span><span class="sxs-lookup"><span data-stu-id="41830-144">Value</span></span> |
|--------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="41830-145">標頭</span><span class="sxs-lookup"><span data-stu-id="41830-145">Header</span></span><br/>  | <dl> <span data-ttu-id="41830-146"><dt>D3DX10Math。h</dt></span><span class="sxs-lookup"><span data-stu-id="41830-146"><dt>D3DX10Math.h</dt></span></span> </dl> |
| <span data-ttu-id="41830-147">程式庫</span><span class="sxs-lookup"><span data-stu-id="41830-147">Library</span></span><br/> | <dl> <span data-ttu-id="41830-148"><dt>D3DX10 .lib</dt></span><span class="sxs-lookup"><span data-stu-id="41830-148"><dt>D3DX10.lib</dt></span></span> </dl>   |



## <a name="see-also"></a><span data-ttu-id="41830-149">另請參閱</span><span class="sxs-lookup"><span data-stu-id="41830-149">See also</span></span>

<dl> <dt>

[<span data-ttu-id="41830-150">數學函數</span><span class="sxs-lookup"><span data-stu-id="41830-150">Math Functions</span></span>](d3d10-graphics-reference-d3dx10-functions-math.md)
</dt> </dl>

 

 
