---
description: D3DXSHEvalConeLight 函式 (D3DX10) -評估的光線是固定強度的錐形，並傳回光譜的球面調和 (SH) 資料。
ms.assetid: ad2b9c86-cf1a-426e-88e6-4c543519e002
title: 'D3DXSHEvalConeLight 函式 (D3DX10) '
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- D3DXSHEvalConeLight
api_type:
- LibDef
api_location:
- D3DX10.lib
- D3DX10.dll
ms.openlocfilehash: fc11e7bab4cbbd6c8a685b289d4bde476cd465ca
ms.sourcegitcommit: 95685061d5b0333bbf9e6ebd208dde8190f97005
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 04/28/2021
ms.locfileid: "108108606"
---
# <a name="d3dxshevalconelight-function-d3dx10h"></a><span data-ttu-id="9fb5f-103">D3DXSHEvalConeLight 函式 (D3DX10) </span><span class="sxs-lookup"><span data-stu-id="9fb5f-103">D3DXSHEvalConeLight function (D3DX10.h)</span></span>

<span data-ttu-id="9fb5f-104">評估屬於常數濃度的光線，並傳回光譜的球面調和 (SH) 資料。</span><span class="sxs-lookup"><span data-stu-id="9fb5f-104">Evaluates a light that is a cone of constant intensity and returns spectral spherical harmonic (SH) data.</span></span>

## <a name="syntax"></a><span data-ttu-id="9fb5f-105">語法</span><span class="sxs-lookup"><span data-stu-id="9fb5f-105">Syntax</span></span>


```C++
HRESULT D3DXSHEvalConeLight(
  _In_       UINT        Order,
  _In_ const D3DXVECTOR3 *pDir,
  _In_       FLOAT       Radius,
  _In_       FLOAT       RIntensity,
  _In_       FLOAT       GIntensity,
  _In_       FLOAT       BIntensity,
  _In_       FLOAT       *pROut,
  _In_       FLOAT       *pGOut,
  _In_       FLOAT       *pBOut
);
```



## <a name="parameters"></a><span data-ttu-id="9fb5f-106">參數</span><span class="sxs-lookup"><span data-stu-id="9fb5f-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="9fb5f-107">*訂單* \[在\]</span><span class="sxs-lookup"><span data-stu-id="9fb5f-107">*Order* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="9fb5f-108">類型： **[ **UINT**](../winprog/windows-data-types.md)**</span><span class="sxs-lookup"><span data-stu-id="9fb5f-108">Type: **[**UINT**](../winprog/windows-data-types.md)**</span></span>

<span data-ttu-id="9fb5f-109">SH 評估的順序。</span><span class="sxs-lookup"><span data-stu-id="9fb5f-109">Order of the SH evaluation.</span></span> <span data-ttu-id="9fb5f-110">必須在 D3DXSH \_ MINORDER 到 D3DXSH \_ MAXORDER （含）的範圍內。</span><span class="sxs-lookup"><span data-stu-id="9fb5f-110">Must be in the range of D3DXSH\_MINORDER to D3DXSH\_MAXORDER, inclusive.</span></span> <span data-ttu-id="9fb5f-111">評估會產生順序²係數。</span><span class="sxs-lookup"><span data-stu-id="9fb5f-111">The evaluation generates Order² coefficients.</span></span> <span data-ttu-id="9fb5f-112">評估的程度是順序-1。</span><span class="sxs-lookup"><span data-stu-id="9fb5f-112">The degree of the evaluation is Order - 1.</span></span>

</dd> <dt>

<span data-ttu-id="9fb5f-113">*pDir* \[在\]</span><span class="sxs-lookup"><span data-stu-id="9fb5f-113">*pDir* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="9fb5f-114">Type： **Const [**D3DXVECTOR3**](../direct3d9/d3dxvector3.md) \***</span><span class="sxs-lookup"><span data-stu-id="9fb5f-114">Type: **const [**D3DXVECTOR3**](../direct3d9/d3dxvector3.md)\***</span></span>

<span data-ttu-id="9fb5f-115">要在其中評估 SH 基礎函數的 (x，y，z) 半球軸方向向量的指標。</span><span class="sxs-lookup"><span data-stu-id="9fb5f-115">Pointer to the (x, y, z) hemisphere axis direction vector in which to evaluate the SH basis functions.</span></span> <span data-ttu-id="9fb5f-116">請參閱＜備註＞。</span><span class="sxs-lookup"><span data-stu-id="9fb5f-116">See Remarks.</span></span>

</dd> <dt>

<span data-ttu-id="9fb5f-117">*Radius* \[在\]</span><span class="sxs-lookup"><span data-stu-id="9fb5f-117">*Radius* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="9fb5f-118">類型： **[ **FLOAT**](../winprog/windows-data-types.md)**</span><span class="sxs-lookup"><span data-stu-id="9fb5f-118">Type: **[**FLOAT**](../winprog/windows-data-types.md)**</span></span>

<span data-ttu-id="9fb5f-119">以弧度為單位的錐形半徑。</span><span class="sxs-lookup"><span data-stu-id="9fb5f-119">Radius of cone in radians.</span></span>

</dd> <dt>

<span data-ttu-id="9fb5f-120">*RIntensity* \[在\]</span><span class="sxs-lookup"><span data-stu-id="9fb5f-120">*RIntensity* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="9fb5f-121">類型： **[ **FLOAT**](../winprog/windows-data-types.md)**</span><span class="sxs-lookup"><span data-stu-id="9fb5f-121">Type: **[**FLOAT**](../winprog/windows-data-types.md)**</span></span>

<span data-ttu-id="9fb5f-122">光線的紅色濃度。</span><span class="sxs-lookup"><span data-stu-id="9fb5f-122">The red intensity of the light.</span></span>

</dd> <dt>

<span data-ttu-id="9fb5f-123">*GIntensity* \[在\]</span><span class="sxs-lookup"><span data-stu-id="9fb5f-123">*GIntensity* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="9fb5f-124">類型： **[ **FLOAT**](../winprog/windows-data-types.md)**</span><span class="sxs-lookup"><span data-stu-id="9fb5f-124">Type: **[**FLOAT**](../winprog/windows-data-types.md)**</span></span>

<span data-ttu-id="9fb5f-125">光線的綠色濃度。</span><span class="sxs-lookup"><span data-stu-id="9fb5f-125">The green intensity of the light.</span></span>

</dd> <dt>

<span data-ttu-id="9fb5f-126">*BIntensity* \[在\]</span><span class="sxs-lookup"><span data-stu-id="9fb5f-126">*BIntensity* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="9fb5f-127">類型： **[ **FLOAT**](../winprog/windows-data-types.md)**</span><span class="sxs-lookup"><span data-stu-id="9fb5f-127">Type: **[**FLOAT**](../winprog/windows-data-types.md)**</span></span>

<span data-ttu-id="9fb5f-128">光線的藍色濃度。</span><span class="sxs-lookup"><span data-stu-id="9fb5f-128">The blue intensity of the light.</span></span>

</dd> <dt>

<span data-ttu-id="9fb5f-129">*pROut* \[在\]</span><span class="sxs-lookup"><span data-stu-id="9fb5f-129">*pROut* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="9fb5f-130">類型： **[ **FLOAT**](../winprog/windows-data-types.md)\***</span><span class="sxs-lookup"><span data-stu-id="9fb5f-130">Type: **[**FLOAT**](../winprog/windows-data-types.md)\***</span></span>

<span data-ttu-id="9fb5f-131">紅色元件的輸出 SH 向量指標。</span><span class="sxs-lookup"><span data-stu-id="9fb5f-131">Pointer to the output SH vector for the red component.</span></span>

</dd> <dt>

<span data-ttu-id="9fb5f-132">*pGOut* \[在\]</span><span class="sxs-lookup"><span data-stu-id="9fb5f-132">*pGOut* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="9fb5f-133">類型： **[ **FLOAT**](../winprog/windows-data-types.md)\***</span><span class="sxs-lookup"><span data-stu-id="9fb5f-133">Type: **[**FLOAT**](../winprog/windows-data-types.md)\***</span></span>

<span data-ttu-id="9fb5f-134">綠色元件的輸出 SH 向量指標。</span><span class="sxs-lookup"><span data-stu-id="9fb5f-134">Pointer to the output SH vector for the green component.</span></span>

</dd> <dt>

<span data-ttu-id="9fb5f-135">*pBOut* \[在\]</span><span class="sxs-lookup"><span data-stu-id="9fb5f-135">*pBOut* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="9fb5f-136">類型： **[ **FLOAT**](../winprog/windows-data-types.md)\***</span><span class="sxs-lookup"><span data-stu-id="9fb5f-136">Type: **[**FLOAT**](../winprog/windows-data-types.md)\***</span></span>

<span data-ttu-id="9fb5f-137">藍色元件的輸出 SH 向量指標。</span><span class="sxs-lookup"><span data-stu-id="9fb5f-137">Pointer to the output SH vector for the blue component.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="9fb5f-138">傳回值</span><span class="sxs-lookup"><span data-stu-id="9fb5f-138">Return value</span></span>

<span data-ttu-id="9fb5f-139">類型： **[ **HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**</span><span class="sxs-lookup"><span data-stu-id="9fb5f-139">Type: **[**HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**</span></span>

<span data-ttu-id="9fb5f-140">如果函式成功，則傳回值為「D3D \_ 正常」。</span><span class="sxs-lookup"><span data-stu-id="9fb5f-140">If the function succeeds, the return value is D3D\_OK.</span></span> <span data-ttu-id="9fb5f-141">如果函式失敗，則傳回值可以是： D3DERR \_ INVALIDCALL。</span><span class="sxs-lookup"><span data-stu-id="9fb5f-141">If the function fails, the return value can be: D3DERR\_INVALIDCALL.</span></span>

## <a name="remarks"></a><span data-ttu-id="9fb5f-142">備註</span><span class="sxs-lookup"><span data-stu-id="9fb5f-142">Remarks</span></span>

<span data-ttu-id="9fb5f-143">評估屬於固定強度的光線，並傳回光譜 SH 資料。</span><span class="sxs-lookup"><span data-stu-id="9fb5f-143">Evaluates a light that is a cone of constant intensity and returns spectral SH data.</span></span> <span data-ttu-id="9fb5f-144">輸出向量會進行計算，如此一來，如果濃度比率 R/G/B 等於1，則在 (光線下的 radiance 方向的結束1.0 會在 >albedo 為 1) 的擴散物件上以錐形方向表示。</span><span class="sxs-lookup"><span data-stu-id="9fb5f-144">The output vector is computed so that if the intensity ratio R/G/B is equal to 1, the exit radiance of a point directly under the light (oriented in the cone direction on a diffuse object with an albedo of 1) would be 1.0.</span></span> <span data-ttu-id="9fb5f-145">這會計算三個光譜範例;將會傳回 pROut，同時會傳回 pGOut 和 pBOut。</span><span class="sxs-lookup"><span data-stu-id="9fb5f-145">This will compute three spectral samples; pROut will be returned, while pGOut and pBOut may be returned.</span></span>

<span data-ttu-id="9fb5f-146">如下圖所示，在具有單位半徑的球體上，可以只使用 theta、右邊的 Z 軸角度和 phi （z 的角度）來指定方向。</span><span class="sxs-lookup"><span data-stu-id="9fb5f-146">On the sphere with unit radius, as shown in the following illustration, direction can be specified simply with theta, the angle about the z-axis in the right-handed direction, and phi, the angle from z.</span></span>

![具有單位半徑之球體的圖例](images/spherical-coordinates.png)

<span data-ttu-id="9fb5f-148">下列方會顯示笛卡兒 (x、y、z) 和球面 (theta 之間的關聯性，以及單位球體上的 phi) 座標。</span><span class="sxs-lookup"><span data-stu-id="9fb5f-148">The following equations show the relationship between Cartesian (x, y, z) and spherical (theta, phi) coordinates on the unit sphere.</span></span> <span data-ttu-id="9fb5f-149">角度 theta 會因0到 2 pi 的範圍而異，而 phi 則是從0到 pi 的變化。</span><span class="sxs-lookup"><span data-stu-id="9fb5f-149">The angle theta varies over the range of 0 to 2 pi, while phi varies from 0 to pi.</span></span>

![笛卡兒和球面座標之間關聯性的方程式](images/spherical-coordinates-equations.png)

## <a name="requirements"></a><span data-ttu-id="9fb5f-151">規格需求</span><span class="sxs-lookup"><span data-stu-id="9fb5f-151">Requirements</span></span>



| <span data-ttu-id="9fb5f-152">需求</span><span class="sxs-lookup"><span data-stu-id="9fb5f-152">Requirement</span></span> | <span data-ttu-id="9fb5f-153">值</span><span class="sxs-lookup"><span data-stu-id="9fb5f-153">Value</span></span> |
|--------------------|---------------------------------------------------------------------------------------|
| <span data-ttu-id="9fb5f-154">標頭</span><span class="sxs-lookup"><span data-stu-id="9fb5f-154">Header</span></span><br/>  | <dl> <span data-ttu-id="9fb5f-155"><dt>D3DX10。h</dt></span><span class="sxs-lookup"><span data-stu-id="9fb5f-155"><dt>D3DX10.h</dt></span></span> </dl>   |
| <span data-ttu-id="9fb5f-156">程式庫</span><span class="sxs-lookup"><span data-stu-id="9fb5f-156">Library</span></span><br/> | <dl> <span data-ttu-id="9fb5f-157"><dt>D3DX10 .lib</dt></span><span class="sxs-lookup"><span data-stu-id="9fb5f-157"><dt>D3DX10.lib</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="9fb5f-158">另請參閱</span><span class="sxs-lookup"><span data-stu-id="9fb5f-158">See also</span></span>

<dl> <dt>

[<span data-ttu-id="9fb5f-159">數學函數</span><span class="sxs-lookup"><span data-stu-id="9fb5f-159">Math Functions</span></span>](d3d10-graphics-reference-d3dx10-functions-math.md)
</dt> </dl>

 

 
