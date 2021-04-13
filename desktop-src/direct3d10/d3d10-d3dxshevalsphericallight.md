---
description: 評估球面燈，並傳回光譜的球面調和 (SH) 資料。
ms.assetid: e2a2b998-285a-46ef-99fe-ccc923013e9a
title: 'D3DXSHEvalSphericalLight 函式 (D3DX10) '
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- D3DXSHEvalSphericalLight
api_type:
- LibDef
api_location:
- D3DX10.lib
- D3DX10.dll
ms.openlocfilehash: c658480a08360fe8489cfc86319a689e828c0a1e
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 03/15/2021
ms.locfileid: "104323211"
---
# <a name="d3dxshevalsphericallight-function-d3dx10h"></a><span data-ttu-id="560cb-103">D3DXSHEvalSphericalLight 函式 (D3DX10) </span><span class="sxs-lookup"><span data-stu-id="560cb-103">D3DXSHEvalSphericalLight function (D3DX10.h)</span></span>

<span data-ttu-id="560cb-104">評估球面燈，並傳回光譜的球面調和 (SH) 資料。</span><span class="sxs-lookup"><span data-stu-id="560cb-104">Evaluates a spherical light and returns spectral spherical harmonic (SH) data.</span></span>

## <a name="syntax"></a><span data-ttu-id="560cb-105">語法</span><span class="sxs-lookup"><span data-stu-id="560cb-105">Syntax</span></span>


```C++
HRESULT D3DXSHEvalSphericalLight(
  _In_       UINT        Order,
  _In_ const D3DXVECTOR3 *pPos,
  _In_       FLOAT       Radius,
  _In_       FLOAT       RIntensity,
  _In_       FLOAT       GIntensity,
  _In_       FLOAT       BIntensity,
  _In_       FLOAT       *pROut,
  _In_       FLOAT       *pGOut,
  _In_       FLOAT       *pBOut
);
```



## <a name="parameters"></a><span data-ttu-id="560cb-106">參數</span><span class="sxs-lookup"><span data-stu-id="560cb-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="560cb-107">*訂單* \[在\]</span><span class="sxs-lookup"><span data-stu-id="560cb-107">*Order* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="560cb-108">類型： **[ **UINT**](../winprog/windows-data-types.md)**</span><span class="sxs-lookup"><span data-stu-id="560cb-108">Type: **[**UINT**](../winprog/windows-data-types.md)**</span></span>

<span data-ttu-id="560cb-109">SH 評估的順序。</span><span class="sxs-lookup"><span data-stu-id="560cb-109">Order of the SH evaluation.</span></span> <span data-ttu-id="560cb-110">必須在 D3DXSH \_ MINORDER 到 D3DXSH \_ MAXORDER （含）的範圍內。</span><span class="sxs-lookup"><span data-stu-id="560cb-110">Must be in the range of D3DXSH\_MINORDER to D3DXSH\_MAXORDER, inclusive.</span></span> <span data-ttu-id="560cb-111">評估會產生順序²係數。</span><span class="sxs-lookup"><span data-stu-id="560cb-111">The evaluation generates Order² coefficients.</span></span> <span data-ttu-id="560cb-112">評估的程度是順序-1。</span><span class="sxs-lookup"><span data-stu-id="560cb-112">The degree of the evaluation is Order - 1.</span></span>

</dd> <dt>

<span data-ttu-id="560cb-113">*pPos* \[在\]</span><span class="sxs-lookup"><span data-stu-id="560cb-113">*pPos* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="560cb-114">Type： **Const [**D3DXVECTOR3**](../direct3d9/d3dxvector3.md) \***</span><span class="sxs-lookup"><span data-stu-id="560cb-114">Type: **const [**D3DXVECTOR3**](../direct3d9/d3dxvector3.md)\***</span></span>

<span data-ttu-id="560cb-115">光線位置的指標。</span><span class="sxs-lookup"><span data-stu-id="560cb-115">Pointer to the light position.</span></span>

</dd> <dt>

<span data-ttu-id="560cb-116">*Radius* \[在\]</span><span class="sxs-lookup"><span data-stu-id="560cb-116">*Radius* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="560cb-117">類型： **[ **FLOAT**](../winprog/windows-data-types.md)**</span><span class="sxs-lookup"><span data-stu-id="560cb-117">Type: **[**FLOAT**](../winprog/windows-data-types.md)**</span></span>

<span data-ttu-id="560cb-118">球形燈光來源的半徑。</span><span class="sxs-lookup"><span data-stu-id="560cb-118">Radius of spherical light source.</span></span>

</dd> <dt>

<span data-ttu-id="560cb-119">*RIntensity* \[在\]</span><span class="sxs-lookup"><span data-stu-id="560cb-119">*RIntensity* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="560cb-120">類型： **[ **FLOAT**](../winprog/windows-data-types.md)**</span><span class="sxs-lookup"><span data-stu-id="560cb-120">Type: **[**FLOAT**](../winprog/windows-data-types.md)**</span></span>

<span data-ttu-id="560cb-121">光線的紅色濃度。</span><span class="sxs-lookup"><span data-stu-id="560cb-121">The red intensity of the light.</span></span>

</dd> <dt>

<span data-ttu-id="560cb-122">*GIntensity* \[在\]</span><span class="sxs-lookup"><span data-stu-id="560cb-122">*GIntensity* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="560cb-123">類型： **[ **FLOAT**](../winprog/windows-data-types.md)**</span><span class="sxs-lookup"><span data-stu-id="560cb-123">Type: **[**FLOAT**](../winprog/windows-data-types.md)**</span></span>

<span data-ttu-id="560cb-124">光線的綠色濃度。</span><span class="sxs-lookup"><span data-stu-id="560cb-124">The green intensity of the light.</span></span>

</dd> <dt>

<span data-ttu-id="560cb-125">*BIntensity* \[在\]</span><span class="sxs-lookup"><span data-stu-id="560cb-125">*BIntensity* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="560cb-126">類型： **[ **FLOAT**](../winprog/windows-data-types.md)**</span><span class="sxs-lookup"><span data-stu-id="560cb-126">Type: **[**FLOAT**](../winprog/windows-data-types.md)**</span></span>

<span data-ttu-id="560cb-127">光線的藍色濃度。</span><span class="sxs-lookup"><span data-stu-id="560cb-127">The blue intensity of the light.</span></span>

</dd> <dt>

<span data-ttu-id="560cb-128">*pROut* \[在\]</span><span class="sxs-lookup"><span data-stu-id="560cb-128">*pROut* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="560cb-129">類型： **[ **FLOAT**](../winprog/windows-data-types.md)\***</span><span class="sxs-lookup"><span data-stu-id="560cb-129">Type: **[**FLOAT**](../winprog/windows-data-types.md)\***</span></span>

<span data-ttu-id="560cb-130">紅色元件的輸出 SH 向量指標。</span><span class="sxs-lookup"><span data-stu-id="560cb-130">Pointer to the output SH vector for the red component.</span></span>

</dd> <dt>

<span data-ttu-id="560cb-131">*pGOut* \[在\]</span><span class="sxs-lookup"><span data-stu-id="560cb-131">*pGOut* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="560cb-132">類型： **[ **FLOAT**](../winprog/windows-data-types.md)\***</span><span class="sxs-lookup"><span data-stu-id="560cb-132">Type: **[**FLOAT**](../winprog/windows-data-types.md)\***</span></span>

<span data-ttu-id="560cb-133">綠色元件的輸出 SH 向量指標。</span><span class="sxs-lookup"><span data-stu-id="560cb-133">Pointer to the output SH vector for the green component.</span></span>

</dd> <dt>

<span data-ttu-id="560cb-134">*pBOut* \[在\]</span><span class="sxs-lookup"><span data-stu-id="560cb-134">*pBOut* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="560cb-135">類型： **[ **FLOAT**](../winprog/windows-data-types.md)\***</span><span class="sxs-lookup"><span data-stu-id="560cb-135">Type: **[**FLOAT**](../winprog/windows-data-types.md)\***</span></span>

<span data-ttu-id="560cb-136">藍色元件的輸出 SH 向量指標。</span><span class="sxs-lookup"><span data-stu-id="560cb-136">Pointer to the output SH vector for the blue component.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="560cb-137">傳回值</span><span class="sxs-lookup"><span data-stu-id="560cb-137">Return value</span></span>

<span data-ttu-id="560cb-138">類型： **[ **HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**</span><span class="sxs-lookup"><span data-stu-id="560cb-138">Type: **[**HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**</span></span>

<span data-ttu-id="560cb-139">如果函式成功，則傳回值為「D3D \_ 正常」。</span><span class="sxs-lookup"><span data-stu-id="560cb-139">If the function succeeds, the return value is D3D\_OK.</span></span> <span data-ttu-id="560cb-140">如果函式失敗，則傳回值可以是： D3DERR \_ INVALIDCALL。</span><span class="sxs-lookup"><span data-stu-id="560cb-140">If the function fails, the return value can be: D3DERR\_INVALIDCALL.</span></span>

## <a name="remarks"></a><span data-ttu-id="560cb-141">備註</span><span class="sxs-lookup"><span data-stu-id="560cb-141">Remarks</span></span>

<span data-ttu-id="560cb-142">評估球面燈並傳回光譜 SH 資料。</span><span class="sxs-lookup"><span data-stu-id="560cb-142">Evaluates a spherical light and returns spectral SH data.</span></span> <span data-ttu-id="560cb-143">這種光線的亮度沒有正規化，就像方向燈一樣，所以在指定濃度時必須小心。</span><span class="sxs-lookup"><span data-stu-id="560cb-143">There is no normalization of the intensity of the light like there is for directional lights, so care has to be taken when specifying the intensities.</span></span> <span data-ttu-id="560cb-144">這會計算三個光譜範例;將會傳回 pROut，同時會傳回 pGOut 和 pBOut。</span><span class="sxs-lookup"><span data-stu-id="560cb-144">This will compute three spectral samples; pROut will be returned, while pGOut and pBOut may be returned.</span></span>

<span data-ttu-id="560cb-145">如下圖所示，在具有單位半徑的球體上，可以只使用 theta、右邊的 Z 軸角度和 phi （z 的角度）來指定方向。</span><span class="sxs-lookup"><span data-stu-id="560cb-145">On the sphere with unit radius, as shown in the following illustration, direction can be specified simply with theta, the angle about the z-axis in the right-handed direction, and phi, the angle from z.</span></span>

![具有單位半徑之球體的圖例](images/spherical-coordinates.png)

<span data-ttu-id="560cb-147">下列方會顯示笛卡兒 (x、y、z) 和球面 (theta 之間的關聯性，以及單位球體上的 phi) 座標。</span><span class="sxs-lookup"><span data-stu-id="560cb-147">The following equations show the relationship between Cartesian (x, y, z) and spherical (theta, phi) coordinates on the unit sphere.</span></span> <span data-ttu-id="560cb-148">角度 theta 會因0到 2 pi 的範圍而異，而 phi 則是從0到 pi 的變化。</span><span class="sxs-lookup"><span data-stu-id="560cb-148">The angle theta varies over the range of 0 to 2 pi, while phi varies from 0 to pi.</span></span>

![笛卡兒和球面座標之間關聯性的方程式](images/spherical-coordinates-equations.png)

## <a name="requirements"></a><span data-ttu-id="560cb-150">規格需求</span><span class="sxs-lookup"><span data-stu-id="560cb-150">Requirements</span></span>



| <span data-ttu-id="560cb-151">需求</span><span class="sxs-lookup"><span data-stu-id="560cb-151">Requirement</span></span> | <span data-ttu-id="560cb-152">值</span><span class="sxs-lookup"><span data-stu-id="560cb-152">Value</span></span> |
|--------------------|---------------------------------------------------------------------------------------|
| <span data-ttu-id="560cb-153">標頭</span><span class="sxs-lookup"><span data-stu-id="560cb-153">Header</span></span><br/>  | <dl> <span data-ttu-id="560cb-154"><dt>D3DX10。h</dt></span><span class="sxs-lookup"><span data-stu-id="560cb-154"><dt>D3DX10.h</dt></span></span> </dl>   |
| <span data-ttu-id="560cb-155">程式庫</span><span class="sxs-lookup"><span data-stu-id="560cb-155">Library</span></span><br/> | <dl> <span data-ttu-id="560cb-156"><dt>D3DX10 .lib</dt></span><span class="sxs-lookup"><span data-stu-id="560cb-156"><dt>D3DX10.lib</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="560cb-157">另請參閱</span><span class="sxs-lookup"><span data-stu-id="560cb-157">See also</span></span>

<dl> <dt>

[<span data-ttu-id="560cb-158">數學函數</span><span class="sxs-lookup"><span data-stu-id="560cb-158">Math Functions</span></span>](d3d10-graphics-reference-d3dx10-functions-math.md)
</dt> </dl>

 

 
