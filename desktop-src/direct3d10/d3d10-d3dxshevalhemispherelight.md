---
description: 評估在球體上兩個色彩之間的線性插補之間的光線。
ms.assetid: 7523ff42-c81d-4857-a50d-7efa213214b8
title: 'D3DXSHEvalHemisphereLight 函式 (D3DX10) '
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- D3DXSHEvalHemisphereLight
api_type:
- LibDef
api_location:
- D3DX10.lib
- D3DX10.dll
ms.openlocfilehash: c6ff3359ce0629eec472e4da24a31c24196c7f15
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 03/15/2021
ms.locfileid: "104323107"
---
# <a name="d3dxshevalhemispherelight-function-d3dx10h"></a><span data-ttu-id="9c6ea-103">D3DXSHEvalHemisphereLight 函式 (D3DX10) </span><span class="sxs-lookup"><span data-stu-id="9c6ea-103">D3DXSHEvalHemisphereLight function (D3DX10.h)</span></span>

<span data-ttu-id="9c6ea-104">評估在球體上兩個色彩之間的線性插補之間的光線。</span><span class="sxs-lookup"><span data-stu-id="9c6ea-104">Evaluates a light that is a linear interpolation between two colors over the sphere.</span></span>

## <a name="syntax"></a><span data-ttu-id="9c6ea-105">語法</span><span class="sxs-lookup"><span data-stu-id="9c6ea-105">Syntax</span></span>


```C++
HRESULT D3DXSHEvalHemisphereLight(
  _In_       UINT        Order,
  _In_ const D3DXVECTOR3 *pDir,
  _In_       D3DXCOLOR   Top,
  _In_       D3DXCOLOR   Bottom,
  _In_       FLOAT       *pROut,
  _In_       FLOAT       *pGOut,
  _In_       FLOAT       *pBOut
);
```



## <a name="parameters"></a><span data-ttu-id="9c6ea-106">參數</span><span class="sxs-lookup"><span data-stu-id="9c6ea-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="9c6ea-107">*訂單* \[在\]</span><span class="sxs-lookup"><span data-stu-id="9c6ea-107">*Order* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="9c6ea-108">類型： **[ **UINT**](../winprog/windows-data-types.md)**</span><span class="sxs-lookup"><span data-stu-id="9c6ea-108">Type: **[**UINT**](../winprog/windows-data-types.md)**</span></span>

<span data-ttu-id="9c6ea-109">球形調和 (SH) 評估的順序。</span><span class="sxs-lookup"><span data-stu-id="9c6ea-109">Order of the spherical harmonic (SH) evaluation.</span></span> <span data-ttu-id="9c6ea-110">必須在 D3DXSH \_ MINORDER 到 D3DXSH \_ MAXORDER （含）的範圍內。</span><span class="sxs-lookup"><span data-stu-id="9c6ea-110">Must be in the range of D3DXSH\_MINORDER to D3DXSH\_MAXORDER, inclusive.</span></span> <span data-ttu-id="9c6ea-111">評估會產生順序²係數。</span><span class="sxs-lookup"><span data-stu-id="9c6ea-111">The evaluation generates Order² coefficients.</span></span> <span data-ttu-id="9c6ea-112">評估的程度是順序-1。</span><span class="sxs-lookup"><span data-stu-id="9c6ea-112">The degree of the evaluation is Order - 1.</span></span>

</dd> <dt>

<span data-ttu-id="9c6ea-113">*pDir* \[在\]</span><span class="sxs-lookup"><span data-stu-id="9c6ea-113">*pDir* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="9c6ea-114">Type： **Const [**D3DXVECTOR3**](../direct3d9/d3dxvector3.md) \***</span><span class="sxs-lookup"><span data-stu-id="9c6ea-114">Type: **const [**D3DXVECTOR3**](../direct3d9/d3dxvector3.md)\***</span></span>

<span data-ttu-id="9c6ea-115">要在其中評估 SH 基礎函數的 (x，y，z) 半球軸方向向量的指標。</span><span class="sxs-lookup"><span data-stu-id="9c6ea-115">Pointer to the (x, y, z) hemisphere axis direction vector in which to evaluate the SH basis functions.</span></span> <span data-ttu-id="9c6ea-116">請參閱＜備註＞。</span><span class="sxs-lookup"><span data-stu-id="9c6ea-116">See Remarks.</span></span>

</dd> <dt>

<span data-ttu-id="9c6ea-117">*頂端* \[在\]</span><span class="sxs-lookup"><span data-stu-id="9c6ea-117">*Top* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="9c6ea-118">類型： **[ **D3DXCOLOR**](../direct3d9/d3dxcolor.md)**</span><span class="sxs-lookup"><span data-stu-id="9c6ea-118">Type: **[**D3DXCOLOR**](../direct3d9/d3dxcolor.md)**</span></span>

<span data-ttu-id="9c6ea-119">天空色彩。</span><span class="sxs-lookup"><span data-stu-id="9c6ea-119">The sky color.</span></span>

</dd> <dt>

<span data-ttu-id="9c6ea-120">*底部* \[在\]</span><span class="sxs-lookup"><span data-stu-id="9c6ea-120">*Bottom* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="9c6ea-121">類型： **[ **D3DXCOLOR**](../direct3d9/d3dxcolor.md)**</span><span class="sxs-lookup"><span data-stu-id="9c6ea-121">Type: **[**D3DXCOLOR**](../direct3d9/d3dxcolor.md)**</span></span>

<span data-ttu-id="9c6ea-122">地面色彩。</span><span class="sxs-lookup"><span data-stu-id="9c6ea-122">The ground color.</span></span>

</dd> <dt>

<span data-ttu-id="9c6ea-123">*pROut* \[在\]</span><span class="sxs-lookup"><span data-stu-id="9c6ea-123">*pROut* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="9c6ea-124">類型： **[ **FLOAT**](../winprog/windows-data-types.md)\***</span><span class="sxs-lookup"><span data-stu-id="9c6ea-124">Type: **[**FLOAT**](../winprog/windows-data-types.md)\***</span></span>

<span data-ttu-id="9c6ea-125">紅色元件的輸出 SH 向量指標。</span><span class="sxs-lookup"><span data-stu-id="9c6ea-125">Pointer to the output SH vector for the red component.</span></span>

</dd> <dt>

<span data-ttu-id="9c6ea-126">*pGOut* \[在\]</span><span class="sxs-lookup"><span data-stu-id="9c6ea-126">*pGOut* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="9c6ea-127">類型： **[ **FLOAT**](../winprog/windows-data-types.md)\***</span><span class="sxs-lookup"><span data-stu-id="9c6ea-127">Type: **[**FLOAT**](../winprog/windows-data-types.md)\***</span></span>

<span data-ttu-id="9c6ea-128">綠色元件的輸出 SH 向量指標。</span><span class="sxs-lookup"><span data-stu-id="9c6ea-128">Pointer to the output SH vector for the green component.</span></span>

</dd> <dt>

<span data-ttu-id="9c6ea-129">*pBOut* \[在\]</span><span class="sxs-lookup"><span data-stu-id="9c6ea-129">*pBOut* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="9c6ea-130">類型： **[ **FLOAT**](../winprog/windows-data-types.md)\***</span><span class="sxs-lookup"><span data-stu-id="9c6ea-130">Type: **[**FLOAT**](../winprog/windows-data-types.md)\***</span></span>

<span data-ttu-id="9c6ea-131">藍色元件的輸出 SH 向量指標。</span><span class="sxs-lookup"><span data-stu-id="9c6ea-131">Pointer to the output SH vector for the blue component.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="9c6ea-132">傳回值</span><span class="sxs-lookup"><span data-stu-id="9c6ea-132">Return value</span></span>

<span data-ttu-id="9c6ea-133">類型： **[ **HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**</span><span class="sxs-lookup"><span data-stu-id="9c6ea-133">Type: **[**HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**</span></span>

<span data-ttu-id="9c6ea-134">如果函式成功，則傳回值為「D3D \_ 正常」。</span><span class="sxs-lookup"><span data-stu-id="9c6ea-134">If the function succeeds, the return value is D3D\_OK.</span></span> <span data-ttu-id="9c6ea-135">如果函式失敗，則傳回值可以是： D3DERR \_ INVALIDCALL。</span><span class="sxs-lookup"><span data-stu-id="9c6ea-135">If the function fails, the return value can be: D3DERR\_INVALIDCALL.</span></span>

## <a name="remarks"></a><span data-ttu-id="9c6ea-136">備註</span><span class="sxs-lookup"><span data-stu-id="9c6ea-136">Remarks</span></span>

<span data-ttu-id="9c6ea-137">插補會在兩個點之間以線性方式完成，而不是在球體的表面上 (也就是，如果軸是 (0，0，1) 它是 Z 中的線性，而不是 azimuthal 角度) 。</span><span class="sxs-lookup"><span data-stu-id="9c6ea-137">The interpolation is done linearly between the two points, not over the surface of the sphere (that is, if the axis was (0,0,1) it is linear in Z, not in the azimuthal angle).</span></span> <span data-ttu-id="9c6ea-138">產生的球形光源函式會正規化，如此一來，完全擴散表面上的點不會有遮蔽，而且方向 pDir 的一般指示會導致結束 radiance 值為 1 (如果最上層色彩為白色，而底部的色彩為黑色) 。</span><span class="sxs-lookup"><span data-stu-id="9c6ea-138">The resulting spherical lighting function is normalized so that a point on a perfectly diffuse surface with no shadowing and a normal pointed in the direction pDir would result in exit radiance with a value of 1 (if the top color was white and the bottom color was black).</span></span> <span data-ttu-id="9c6ea-139">這是非常簡單的模型，其中 Top 代表「天空」的濃度，而底部代表「地面」的強度。</span><span class="sxs-lookup"><span data-stu-id="9c6ea-139">This is a very simple model where Top represents the intensity of the "sky" and Bottom represents the intensity of the "ground."</span></span>

<span data-ttu-id="9c6ea-140">如下圖所示，在具有單位半徑的球體上，可以只使用 theta、右邊的 Z 軸角度和 phi （z 的角度）來指定方向。</span><span class="sxs-lookup"><span data-stu-id="9c6ea-140">On the sphere with unit radius, as shown in the following illustration, direction can be specified simply with theta, the angle about the z-axis in the right-handed direction, and phi, the angle from z.</span></span>

![具有單位半徑之球體的圖例](images/spherical-coordinates.png)

<span data-ttu-id="9c6ea-142">下列方會顯示笛卡兒 (x、y、z) 和球面 (theta 之間的關聯性，以及單位球體上的 phi) 座標。</span><span class="sxs-lookup"><span data-stu-id="9c6ea-142">The following equations show the relationship between Cartesian (x, y, z) and spherical (theta, phi) coordinates on the unit sphere.</span></span> <span data-ttu-id="9c6ea-143">角度 theta 會因0到 2 pi 的範圍而異，而 phi 則是從0到 pi 的變化。</span><span class="sxs-lookup"><span data-stu-id="9c6ea-143">The angle theta varies over the range of 0 to 2 pi, while phi varies from 0 to pi.</span></span>

![笛卡兒和球面座標之間關聯性的方程式](images/spherical-coordinates-equations.png)

## <a name="requirements"></a><span data-ttu-id="9c6ea-145">規格需求</span><span class="sxs-lookup"><span data-stu-id="9c6ea-145">Requirements</span></span>



| <span data-ttu-id="9c6ea-146">需求</span><span class="sxs-lookup"><span data-stu-id="9c6ea-146">Requirement</span></span> | <span data-ttu-id="9c6ea-147">值</span><span class="sxs-lookup"><span data-stu-id="9c6ea-147">Value</span></span> |
|--------------------|---------------------------------------------------------------------------------------|
| <span data-ttu-id="9c6ea-148">標頭</span><span class="sxs-lookup"><span data-stu-id="9c6ea-148">Header</span></span><br/>  | <dl> <span data-ttu-id="9c6ea-149"><dt>D3DX10。h</dt></span><span class="sxs-lookup"><span data-stu-id="9c6ea-149"><dt>D3DX10.h</dt></span></span> </dl>   |
| <span data-ttu-id="9c6ea-150">程式庫</span><span class="sxs-lookup"><span data-stu-id="9c6ea-150">Library</span></span><br/> | <dl> <span data-ttu-id="9c6ea-151"><dt>D3DX10 .lib</dt></span><span class="sxs-lookup"><span data-stu-id="9c6ea-151"><dt>D3DX10.lib</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="9c6ea-152">另請參閱</span><span class="sxs-lookup"><span data-stu-id="9c6ea-152">See also</span></span>

<dl> <dt>

[<span data-ttu-id="9c6ea-153">數學函數</span><span class="sxs-lookup"><span data-stu-id="9c6ea-153">Math Functions</span></span>](d3d10-graphics-reference-d3dx10-functions-math.md)
</dt> </dl>

 

 
