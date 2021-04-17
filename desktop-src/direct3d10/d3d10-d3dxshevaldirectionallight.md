---
description: 評估方向輕量，並傳回光譜的球面調和 (SH) 資料。
ms.assetid: b5c657f5-d291-4e53-908c-670b29a1888a
title: 'D3DXSHEvalDirectionalLight 函式 (D3DX10) '
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- D3DXSHEvalDirectionalLight
api_type:
- LibDef
api_location:
- D3DX10.lib
- D3DX10.dll
ms.openlocfilehash: 9c6b5c9590132d9fe3d0fc07ae419d442144079a
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 03/15/2021
ms.locfileid: "104558941"
---
# <a name="d3dxshevaldirectionallight-function-d3dx10h"></a><span data-ttu-id="5317e-103">D3DXSHEvalDirectionalLight 函式 (D3DX10) </span><span class="sxs-lookup"><span data-stu-id="5317e-103">D3DXSHEvalDirectionalLight function (D3DX10.h)</span></span>

<span data-ttu-id="5317e-104">評估方向輕量，並傳回光譜的球面調和 (SH) 資料。</span><span class="sxs-lookup"><span data-stu-id="5317e-104">Evaluates a directional light and returns spectral spherical harmonic (SH) data.</span></span>

## <a name="syntax"></a><span data-ttu-id="5317e-105">語法</span><span class="sxs-lookup"><span data-stu-id="5317e-105">Syntax</span></span>


```C++
HRESULT D3DXSHEvalDirectionalLight(
  _In_       UINT        Order,
  _In_ const D3DXVECTOR3 *pDir,
  _In_       FLOAT       RIntensity,
  _In_       FLOAT       GIntensity,
  _In_       FLOAT       BIntensity,
  _In_       FLOAT       *pROut,
  _In_       FLOAT       *pGOut,
  _In_       FLOAT       *pBOut
);
```



## <a name="parameters"></a><span data-ttu-id="5317e-106">參數</span><span class="sxs-lookup"><span data-stu-id="5317e-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="5317e-107">*訂單* \[在\]</span><span class="sxs-lookup"><span data-stu-id="5317e-107">*Order* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="5317e-108">類型： **[ **UINT**](../winprog/windows-data-types.md)**</span><span class="sxs-lookup"><span data-stu-id="5317e-108">Type: **[**UINT**](../winprog/windows-data-types.md)**</span></span>

<span data-ttu-id="5317e-109">SH 評估的順序。</span><span class="sxs-lookup"><span data-stu-id="5317e-109">Order of the SH evaluation.</span></span> <span data-ttu-id="5317e-110">必須在 D3DXSH \_ MINORDER 到 D3DXSH \_ MAXORDER （含）的範圍內。</span><span class="sxs-lookup"><span data-stu-id="5317e-110">Must be in the range of D3DXSH\_MINORDER to D3DXSH\_MAXORDER, inclusive.</span></span> <span data-ttu-id="5317e-111">評估會產生順序²係數。</span><span class="sxs-lookup"><span data-stu-id="5317e-111">The evaluation generates Order² coefficients.</span></span> <span data-ttu-id="5317e-112">評估的程度是順序-1。</span><span class="sxs-lookup"><span data-stu-id="5317e-112">The degree of the evaluation is Order - 1.</span></span>

</dd> <dt>

<span data-ttu-id="5317e-113">*pDir* \[在\]</span><span class="sxs-lookup"><span data-stu-id="5317e-113">*pDir* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="5317e-114">Type： **Const [**D3DXVECTOR3**](../direct3d9/d3dxvector3.md) \***</span><span class="sxs-lookup"><span data-stu-id="5317e-114">Type: **const [**D3DXVECTOR3**](../direct3d9/d3dxvector3.md)\***</span></span>

<span data-ttu-id="5317e-115">要在其中評估 SH 基礎函數的 (x，y，z) 半球軸方向向量的指標。</span><span class="sxs-lookup"><span data-stu-id="5317e-115">Pointer to the (x, y, z) hemisphere axis direction vector in which to evaluate the SH basis functions.</span></span> <span data-ttu-id="5317e-116">請參閱＜備註＞。</span><span class="sxs-lookup"><span data-stu-id="5317e-116">See Remarks.</span></span>

</dd> <dt>

<span data-ttu-id="5317e-117">*RIntensity* \[在\]</span><span class="sxs-lookup"><span data-stu-id="5317e-117">*RIntensity* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="5317e-118">類型： **[ **FLOAT**](../winprog/windows-data-types.md)**</span><span class="sxs-lookup"><span data-stu-id="5317e-118">Type: **[**FLOAT**](../winprog/windows-data-types.md)**</span></span>

<span data-ttu-id="5317e-119">光線的紅色濃度。</span><span class="sxs-lookup"><span data-stu-id="5317e-119">The red intensity of the light.</span></span>

</dd> <dt>

<span data-ttu-id="5317e-120">*GIntensity* \[在\]</span><span class="sxs-lookup"><span data-stu-id="5317e-120">*GIntensity* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="5317e-121">類型： **[ **FLOAT**](../winprog/windows-data-types.md)**</span><span class="sxs-lookup"><span data-stu-id="5317e-121">Type: **[**FLOAT**](../winprog/windows-data-types.md)**</span></span>

<span data-ttu-id="5317e-122">光線的綠色濃度。</span><span class="sxs-lookup"><span data-stu-id="5317e-122">The green intensity of the light.</span></span>

</dd> <dt>

<span data-ttu-id="5317e-123">*BIntensity* \[在\]</span><span class="sxs-lookup"><span data-stu-id="5317e-123">*BIntensity* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="5317e-124">類型： **[ **FLOAT**](../winprog/windows-data-types.md)**</span><span class="sxs-lookup"><span data-stu-id="5317e-124">Type: **[**FLOAT**](../winprog/windows-data-types.md)**</span></span>

<span data-ttu-id="5317e-125">光線的藍色濃度。</span><span class="sxs-lookup"><span data-stu-id="5317e-125">The blue intensity of the light.</span></span>

</dd> <dt>

<span data-ttu-id="5317e-126">*pROut* \[在\]</span><span class="sxs-lookup"><span data-stu-id="5317e-126">*pROut* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="5317e-127">類型： **[ **FLOAT**](../winprog/windows-data-types.md)\***</span><span class="sxs-lookup"><span data-stu-id="5317e-127">Type: **[**FLOAT**](../winprog/windows-data-types.md)\***</span></span>

<span data-ttu-id="5317e-128">紅色元件的輸出 SH 向量指標。</span><span class="sxs-lookup"><span data-stu-id="5317e-128">Pointer to the output SH vector for the red component.</span></span>

</dd> <dt>

<span data-ttu-id="5317e-129">*pGOut* \[在\]</span><span class="sxs-lookup"><span data-stu-id="5317e-129">*pGOut* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="5317e-130">類型： **[ **FLOAT**](../winprog/windows-data-types.md)\***</span><span class="sxs-lookup"><span data-stu-id="5317e-130">Type: **[**FLOAT**](../winprog/windows-data-types.md)\***</span></span>

<span data-ttu-id="5317e-131">綠色元件之輸出 SH 向量的選擇性指標。</span><span class="sxs-lookup"><span data-stu-id="5317e-131">Optional pointer to the output SH vector for the green component.</span></span>

</dd> <dt>

<span data-ttu-id="5317e-132">*pBOut* \[在\]</span><span class="sxs-lookup"><span data-stu-id="5317e-132">*pBOut* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="5317e-133">類型： **[ **FLOAT**](../winprog/windows-data-types.md)\***</span><span class="sxs-lookup"><span data-stu-id="5317e-133">Type: **[**FLOAT**](../winprog/windows-data-types.md)\***</span></span>

<span data-ttu-id="5317e-134">藍色元件之輸出 SH 向量的選擇性指標。</span><span class="sxs-lookup"><span data-stu-id="5317e-134">Optional pointer to the output SH vector for the blue component.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="5317e-135">傳回值</span><span class="sxs-lookup"><span data-stu-id="5317e-135">Return value</span></span>

<span data-ttu-id="5317e-136">類型： **[ **HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**</span><span class="sxs-lookup"><span data-stu-id="5317e-136">Type: **[**HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**</span></span>

<span data-ttu-id="5317e-137">如果函式成功，則傳回值為「D3D \_ 正常」。</span><span class="sxs-lookup"><span data-stu-id="5317e-137">If the function succeeds, the return value is D3D\_OK.</span></span> <span data-ttu-id="5317e-138">如果函式失敗，則傳回值可以是： D3DERR \_ INVALIDCALL。</span><span class="sxs-lookup"><span data-stu-id="5317e-138">If the function fails, the return value can be: D3DERR\_INVALIDCALL.</span></span>

## <a name="remarks"></a><span data-ttu-id="5317e-139">備註</span><span class="sxs-lookup"><span data-stu-id="5317e-139">Remarks</span></span>

<span data-ttu-id="5317e-140">輸出向量會進行計算，如此一來，如果濃度比率 R/G/B 等於1，則在 >albedo 為1的擴散物件上，點正下方的結果結束 radiance 會是1.0。</span><span class="sxs-lookup"><span data-stu-id="5317e-140">The output vector is computed so that if the intensity ratio R/G/B is equal to 1, the resulting exit radiance of a point directly under the light on a diffuse object with an albedo of 1 would be 1.0.</span></span> <span data-ttu-id="5317e-141">這會計算三個光譜範例;將會傳回 pROut，同時會傳回 pGOut 和 pBOut。</span><span class="sxs-lookup"><span data-stu-id="5317e-141">This will compute three spectral samples; pROut will be returned, while pGOut and pBOut may be returned.</span></span>

<span data-ttu-id="5317e-142">如下圖所示，在具有單位半徑的球體上，可以只使用 theta、右邊的 Z 軸角度和 phi （z 的角度）來指定方向。</span><span class="sxs-lookup"><span data-stu-id="5317e-142">On the sphere with unit radius, as shown in the following illustration, direction can be specified simply with theta, the angle about the z-axis in the right-handed direction, and phi, the angle from z.</span></span>

![具有單位半徑之球體的圖例](images/spherical-coordinates.png)

<span data-ttu-id="5317e-144">下列方會顯示笛卡兒 (x、y、z) 和球面 (theta 之間的關聯性，以及單位球體上的 phi) 座標。</span><span class="sxs-lookup"><span data-stu-id="5317e-144">The following equations show the relationship between Cartesian (x, y, z) and spherical (theta, phi) coordinates on the unit sphere.</span></span> <span data-ttu-id="5317e-145">角度 theta 會因0到 2 pi 的範圍而異，而 phi 則是從0到 pi 的變化。</span><span class="sxs-lookup"><span data-stu-id="5317e-145">The angle theta varies over the range of 0 to 2 pi, while phi varies from 0 to pi.</span></span>

![笛卡兒和球面座標之間關聯性的方程式](images/spherical-coordinates-equations.png)

## <a name="requirements"></a><span data-ttu-id="5317e-147">規格需求</span><span class="sxs-lookup"><span data-stu-id="5317e-147">Requirements</span></span>



| <span data-ttu-id="5317e-148">需求</span><span class="sxs-lookup"><span data-stu-id="5317e-148">Requirement</span></span> | <span data-ttu-id="5317e-149">值</span><span class="sxs-lookup"><span data-stu-id="5317e-149">Value</span></span> |
|--------------------|---------------------------------------------------------------------------------------|
| <span data-ttu-id="5317e-150">標頭</span><span class="sxs-lookup"><span data-stu-id="5317e-150">Header</span></span><br/>  | <dl> <span data-ttu-id="5317e-151"><dt>D3DX10。h</dt></span><span class="sxs-lookup"><span data-stu-id="5317e-151"><dt>D3DX10.h</dt></span></span> </dl>   |
| <span data-ttu-id="5317e-152">程式庫</span><span class="sxs-lookup"><span data-stu-id="5317e-152">Library</span></span><br/> | <dl> <span data-ttu-id="5317e-153"><dt>D3DX10 .lib</dt></span><span class="sxs-lookup"><span data-stu-id="5317e-153"><dt>D3DX10.lib</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="5317e-154">另請參閱</span><span class="sxs-lookup"><span data-stu-id="5317e-154">See also</span></span>

<dl> <dt>

[<span data-ttu-id="5317e-155">數學函數</span><span class="sxs-lookup"><span data-stu-id="5317e-155">Math Functions</span></span>](d3d10-graphics-reference-d3dx10-functions-math.md)
</dt> </dl>

 

 
