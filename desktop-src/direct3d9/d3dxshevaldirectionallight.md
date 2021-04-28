---
description: D3DXSHEvalDirectionalLight 函式 (D3dx9math) -評估方向輕量，並傳回光譜的球面調和 (SH) 資料。
ms.assetid: 6e2e9b02-13bb-4cef-ae9d-343fbf64e5d7
title: 'D3DXSHEvalDirectionalLight 函式 (D3dx9math) '
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
- d3dx9.lib
- d3dx9.dll
ms.openlocfilehash: 488682eca230c8da6cc5048aded4a7a1e7f71bfd
ms.sourcegitcommit: 95685061d5b0333bbf9e6ebd208dde8190f97005
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 04/28/2021
ms.locfileid: "108117906"
---
# <a name="d3dxshevaldirectionallight-function-d3dx9mathh"></a><span data-ttu-id="a9d1e-103">D3DXSHEvalDirectionalLight 函式 (D3dx9math) </span><span class="sxs-lookup"><span data-stu-id="a9d1e-103">D3DXSHEvalDirectionalLight function (D3dx9math.h)</span></span>

<span data-ttu-id="a9d1e-104">評估 [方向輕](light-types.md) 量，並傳回光譜的球面調和 (SH) 資料。</span><span class="sxs-lookup"><span data-stu-id="a9d1e-104">Evaluates a [directional light](light-types.md) and returns spectral spherical harmonic (SH) data.</span></span>

## <a name="syntax"></a><span data-ttu-id="a9d1e-105">語法</span><span class="sxs-lookup"><span data-stu-id="a9d1e-105">Syntax</span></span>


```C++
HRESULT D3DXSHEvalDirectionalLight(
  _In_        UINT        Order,
  _In_  const D3DXVECTOR3 *pDir,
  _In_        FLOAT       RIntensity,
  _In_        FLOAT       GIntensity,
  _In_        FLOAT       BIntensity,
  _Out_       FLOAT       *pROut,
  _Out_       FLOAT       *pGOut,
  _Out_       FLOAT       *pBOut
);
```



## <a name="parameters"></a><span data-ttu-id="a9d1e-106">參數</span><span class="sxs-lookup"><span data-stu-id="a9d1e-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="a9d1e-107">*訂單* \[在\]</span><span class="sxs-lookup"><span data-stu-id="a9d1e-107">*Order* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="a9d1e-108">類型： **[ **UINT**](../winprog/windows-data-types.md)**</span><span class="sxs-lookup"><span data-stu-id="a9d1e-108">Type: **[**UINT**](../winprog/windows-data-types.md)**</span></span>

<span data-ttu-id="a9d1e-109">SH 評估的順序。</span><span class="sxs-lookup"><span data-stu-id="a9d1e-109">Order of the SH evaluation.</span></span> <span data-ttu-id="a9d1e-110">必須在 [D3DXSH \_ MINORDER](other-d3dx-constants.md) 到 D3DXSH \_ MAXORDER （含）的範圍內。</span><span class="sxs-lookup"><span data-stu-id="a9d1e-110">Must be in the range of [D3DXSH\_MINORDER](other-d3dx-constants.md) to D3DXSH\_MAXORDER, inclusive.</span></span> <span data-ttu-id="a9d1e-111">評估會產生順序²係數。</span><span class="sxs-lookup"><span data-stu-id="a9d1e-111">The evaluation generates Order² coefficients.</span></span> <span data-ttu-id="a9d1e-112">評估的程度是順序-1。</span><span class="sxs-lookup"><span data-stu-id="a9d1e-112">The degree of the evaluation is Order - 1.</span></span>

</dd> <dt>

<span data-ttu-id="a9d1e-113">*pDir* \[在\]</span><span class="sxs-lookup"><span data-stu-id="a9d1e-113">*pDir* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="a9d1e-114">Type： **Const [**D3DXVECTOR3**](d3dxvector3.md) \***</span><span class="sxs-lookup"><span data-stu-id="a9d1e-114">Type: **const [**D3DXVECTOR3**](d3dxvector3.md)\***</span></span>

<span data-ttu-id="a9d1e-115">要在其中評估 SH 基礎函數的 (x，y，z) 半球軸方向向量的指標。</span><span class="sxs-lookup"><span data-stu-id="a9d1e-115">Pointer to the (x, y, z) hemisphere axis direction vector in which to evaluate the SH basis functions.</span></span> <span data-ttu-id="a9d1e-116">請參閱＜備註＞。</span><span class="sxs-lookup"><span data-stu-id="a9d1e-116">See Remarks.</span></span>

</dd> <dt>

<span data-ttu-id="a9d1e-117">*RIntensity* \[在\]</span><span class="sxs-lookup"><span data-stu-id="a9d1e-117">*RIntensity* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="a9d1e-118">類型： **[ **FLOAT**](../winprog/windows-data-types.md)**</span><span class="sxs-lookup"><span data-stu-id="a9d1e-118">Type: **[**FLOAT**](../winprog/windows-data-types.md)**</span></span>

<span data-ttu-id="a9d1e-119">光線的紅色濃度。</span><span class="sxs-lookup"><span data-stu-id="a9d1e-119">The red intensity of the light.</span></span>

</dd> <dt>

<span data-ttu-id="a9d1e-120">*GIntensity* \[在\]</span><span class="sxs-lookup"><span data-stu-id="a9d1e-120">*GIntensity* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="a9d1e-121">類型： **[ **FLOAT**](../winprog/windows-data-types.md)**</span><span class="sxs-lookup"><span data-stu-id="a9d1e-121">Type: **[**FLOAT**](../winprog/windows-data-types.md)**</span></span>

<span data-ttu-id="a9d1e-122">光線的綠色濃度。</span><span class="sxs-lookup"><span data-stu-id="a9d1e-122">The green intensity of the light.</span></span>

</dd> <dt>

<span data-ttu-id="a9d1e-123">*BIntensity* \[在\]</span><span class="sxs-lookup"><span data-stu-id="a9d1e-123">*BIntensity* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="a9d1e-124">類型： **[ **FLOAT**](../winprog/windows-data-types.md)**</span><span class="sxs-lookup"><span data-stu-id="a9d1e-124">Type: **[**FLOAT**](../winprog/windows-data-types.md)**</span></span>

<span data-ttu-id="a9d1e-125">光線的藍色濃度。</span><span class="sxs-lookup"><span data-stu-id="a9d1e-125">The blue intensity of the light.</span></span>

</dd> <dt>

<span data-ttu-id="a9d1e-126">*pROut* \[擴展\]</span><span class="sxs-lookup"><span data-stu-id="a9d1e-126">*pROut* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="a9d1e-127">類型： **[ **FLOAT**](../winprog/windows-data-types.md)\***</span><span class="sxs-lookup"><span data-stu-id="a9d1e-127">Type: **[**FLOAT**](../winprog/windows-data-types.md)\***</span></span>

<span data-ttu-id="a9d1e-128">紅色元件的輸出 SH 向量指標。</span><span class="sxs-lookup"><span data-stu-id="a9d1e-128">Pointer to the output SH vector for the red component.</span></span>

</dd> <dt>

<span data-ttu-id="a9d1e-129">*pGOut* \[擴展\]</span><span class="sxs-lookup"><span data-stu-id="a9d1e-129">*pGOut* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="a9d1e-130">類型： **[ **FLOAT**](../winprog/windows-data-types.md)\***</span><span class="sxs-lookup"><span data-stu-id="a9d1e-130">Type: **[**FLOAT**](../winprog/windows-data-types.md)\***</span></span>

<span data-ttu-id="a9d1e-131">綠色元件之輸出 SH 向量的選擇性指標。</span><span class="sxs-lookup"><span data-stu-id="a9d1e-131">Optional pointer to the output SH vector for the green component.</span></span>

</dd> <dt>

<span data-ttu-id="a9d1e-132">*pBOut* \[擴展\]</span><span class="sxs-lookup"><span data-stu-id="a9d1e-132">*pBOut* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="a9d1e-133">類型： **[ **FLOAT**](../winprog/windows-data-types.md)\***</span><span class="sxs-lookup"><span data-stu-id="a9d1e-133">Type: **[**FLOAT**](../winprog/windows-data-types.md)\***</span></span>

<span data-ttu-id="a9d1e-134">藍色元件之輸出 SH 向量的選擇性指標。</span><span class="sxs-lookup"><span data-stu-id="a9d1e-134">Optional pointer to the output SH vector for the blue component.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="a9d1e-135">傳回值</span><span class="sxs-lookup"><span data-stu-id="a9d1e-135">Return value</span></span>

<span data-ttu-id="a9d1e-136">類型： **[ **HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**</span><span class="sxs-lookup"><span data-stu-id="a9d1e-136">Type: **[**HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**</span></span>

<span data-ttu-id="a9d1e-137">如果函式成功，則傳回值為「D3D \_ 正常」。</span><span class="sxs-lookup"><span data-stu-id="a9d1e-137">If the function succeeds, the return value is D3D\_OK.</span></span> <span data-ttu-id="a9d1e-138">如果函式失敗，則傳回值可以是： D3DERR \_ INVALIDCALL。</span><span class="sxs-lookup"><span data-stu-id="a9d1e-138">If the function fails, the return value can be: D3DERR\_INVALIDCALL.</span></span>

## <a name="remarks"></a><span data-ttu-id="a9d1e-139">備註</span><span class="sxs-lookup"><span data-stu-id="a9d1e-139">Remarks</span></span>

<span data-ttu-id="a9d1e-140">輸出向量會進行計算，如此一來，如果濃度比率 R/G/B 等於1，則在 >albedo 為1的擴散物件上，點正下方的結果結束 radiance 會是1.0。</span><span class="sxs-lookup"><span data-stu-id="a9d1e-140">The output vector is computed so that if the intensity ratio R/G/B is equal to 1, the resulting exit radiance of a point directly under the light on a diffuse object with an albedo of 1 would be 1.0.</span></span> <span data-ttu-id="a9d1e-141">這會計算三個光譜範例;將會傳回 *pROut* ，同時會傳回 *pGOut* 和 *pBOut* 。</span><span class="sxs-lookup"><span data-stu-id="a9d1e-141">This will compute three spectral samples; *pROut* will be returned, while *pGOut* and *pBOut* may be returned.</span></span>

<span data-ttu-id="a9d1e-142">如下圖所示，在具有單位半徑的球體上，可以只使用 theta、 [右邊](coordinate-systems.md)的 Z 軸角度和 phi （z 的角度）來指定方向。</span><span class="sxs-lookup"><span data-stu-id="a9d1e-142">On the sphere with unit radius, as shown in the following illustration, direction can be specified simply with theta, the angle about the z-axis in the [right-handed direction](coordinate-systems.md), and phi, the angle from z.</span></span>

![具有單位半徑之球體的圖例](images/spherical-coordinates.png)

<span data-ttu-id="a9d1e-144">下列方會顯示笛卡兒 (x、y、z) 和球面 (theta 之間的關聯性，以及單位球體上的 phi) 座標。</span><span class="sxs-lookup"><span data-stu-id="a9d1e-144">The following equations show the relationship between Cartesian (x, y, z) and spherical (theta, phi) coordinates on the unit sphere.</span></span> <span data-ttu-id="a9d1e-145">角度 theta 會因0到 2 pi 的範圍而異，而 phi 則是從0到 pi 的變化。</span><span class="sxs-lookup"><span data-stu-id="a9d1e-145">The angle theta varies over the range of 0 to 2 pi, while phi varies from 0 to pi.</span></span>

![笛卡兒和球面座標之間關聯性的方程式](images/spherical-coordinates-equations.png)

## <a name="requirements"></a><span data-ttu-id="a9d1e-147">規格需求</span><span class="sxs-lookup"><span data-stu-id="a9d1e-147">Requirements</span></span>



| <span data-ttu-id="a9d1e-148">需求</span><span class="sxs-lookup"><span data-stu-id="a9d1e-148">Requirement</span></span> | <span data-ttu-id="a9d1e-149">值</span><span class="sxs-lookup"><span data-stu-id="a9d1e-149">Value</span></span> |
|--------------------|----------------------------------------------------------------------------------------|
| <span data-ttu-id="a9d1e-150">標頭</span><span class="sxs-lookup"><span data-stu-id="a9d1e-150">Header</span></span><br/>  | <dl> <span data-ttu-id="a9d1e-151"><dt>D3dx9math。h</dt></span><span class="sxs-lookup"><span data-stu-id="a9d1e-151"><dt>D3dx9math.h</dt></span></span> </dl> |
| <span data-ttu-id="a9d1e-152">程式庫</span><span class="sxs-lookup"><span data-stu-id="a9d1e-152">Library</span></span><br/> | <dl> <span data-ttu-id="a9d1e-153"><dt>D3dx9 .lib</dt></span><span class="sxs-lookup"><span data-stu-id="a9d1e-153"><dt>D3dx9.lib</dt></span></span> </dl>   |



## <a name="see-also"></a><span data-ttu-id="a9d1e-154">另請參閱</span><span class="sxs-lookup"><span data-stu-id="a9d1e-154">See also</span></span>

<dl> <dt>

[<span data-ttu-id="a9d1e-155">數學函數</span><span class="sxs-lookup"><span data-stu-id="a9d1e-155">Math Functions</span></span>](dx9-graphics-reference-d3dx-functions-math.md)
</dt> <dt>

[<span data-ttu-id="a9d1e-156">預先計算 Radiance Transfer (Direct3D 9) </span><span class="sxs-lookup"><span data-stu-id="a9d1e-156">Precomputed Radiance Transfer (Direct3D 9)</span></span>](precomputed-radiance-transfer.md)
</dt> </dl>

 

 
