---
description: 評估在球體上兩個色彩之間的線性插補之間的光線。
ms.assetid: c5815f12-f706-40f6-bf5e-78a211cfbbea
title: 'D3DXSHEvalHemisphereLight 函式 (D3dx9math) '
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
- d3dx9.lib
- d3dx9.dll
ms.openlocfilehash: bdb94fc10ddadc7048f7bb911df089d6f84b0829
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 03/15/2021
ms.locfileid: "104562835"
---
# <a name="d3dxshevalhemispherelight-function-d3dx9mathh"></a><span data-ttu-id="43b27-103">D3DXSHEvalHemisphereLight 函式 (D3dx9math) </span><span class="sxs-lookup"><span data-stu-id="43b27-103">D3DXSHEvalHemisphereLight function (D3dx9math.h)</span></span>

<span data-ttu-id="43b27-104">評估在球體上兩個色彩之間的線性插補之間的光線。</span><span class="sxs-lookup"><span data-stu-id="43b27-104">Evaluates a light that is a linear interpolation between two colors over the sphere.</span></span>

## <a name="syntax"></a><span data-ttu-id="43b27-105">語法</span><span class="sxs-lookup"><span data-stu-id="43b27-105">Syntax</span></span>


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



## <a name="parameters"></a><span data-ttu-id="43b27-106">參數</span><span class="sxs-lookup"><span data-stu-id="43b27-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="43b27-107">*訂單* \[在\]</span><span class="sxs-lookup"><span data-stu-id="43b27-107">*Order* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="43b27-108">類型： **[ **UINT**](../winprog/windows-data-types.md)**</span><span class="sxs-lookup"><span data-stu-id="43b27-108">Type: **[**UINT**](../winprog/windows-data-types.md)**</span></span>

<span data-ttu-id="43b27-109">球形調和 (SH) 評估的順序。</span><span class="sxs-lookup"><span data-stu-id="43b27-109">Order of the spherical harmonic (SH) evaluation.</span></span> <span data-ttu-id="43b27-110">必須在 [D3DXSH \_ MINORDER](other-d3dx-constants.md) 到 D3DXSH \_ MAXORDER （含）的範圍內。</span><span class="sxs-lookup"><span data-stu-id="43b27-110">Must be in the range of [D3DXSH\_MINORDER](other-d3dx-constants.md) to D3DXSH\_MAXORDER, inclusive.</span></span> <span data-ttu-id="43b27-111">評估會產生順序²係數。</span><span class="sxs-lookup"><span data-stu-id="43b27-111">The evaluation generates Order² coefficients.</span></span> <span data-ttu-id="43b27-112">評估的程度是順序-1。</span><span class="sxs-lookup"><span data-stu-id="43b27-112">The degree of the evaluation is Order - 1.</span></span>

</dd> <dt>

<span data-ttu-id="43b27-113">*pDir* \[在\]</span><span class="sxs-lookup"><span data-stu-id="43b27-113">*pDir* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="43b27-114">Type： **Const [**D3DXVECTOR3**](d3dxvector3.md) \***</span><span class="sxs-lookup"><span data-stu-id="43b27-114">Type: **const [**D3DXVECTOR3**](d3dxvector3.md)\***</span></span>

<span data-ttu-id="43b27-115">要在其中評估 SH 基礎函數的 (x，y，z) 半球軸方向向量的指標。</span><span class="sxs-lookup"><span data-stu-id="43b27-115">Pointer to the (x, y, z) hemisphere axis direction vector in which to evaluate the SH basis functions.</span></span> <span data-ttu-id="43b27-116">請參閱＜備註＞。</span><span class="sxs-lookup"><span data-stu-id="43b27-116">See Remarks.</span></span>

</dd> <dt>

<span data-ttu-id="43b27-117">*頂端* \[在\]</span><span class="sxs-lookup"><span data-stu-id="43b27-117">*Top* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="43b27-118">類型： **[ **D3DXCOLOR**](d3dxcolor.md)**</span><span class="sxs-lookup"><span data-stu-id="43b27-118">Type: **[**D3DXCOLOR**](d3dxcolor.md)**</span></span>

<span data-ttu-id="43b27-119">天空色彩。</span><span class="sxs-lookup"><span data-stu-id="43b27-119">The sky color.</span></span>

</dd> <dt>

<span data-ttu-id="43b27-120">*底部* \[在\]</span><span class="sxs-lookup"><span data-stu-id="43b27-120">*Bottom* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="43b27-121">類型： **[ **D3DXCOLOR**](d3dxcolor.md)**</span><span class="sxs-lookup"><span data-stu-id="43b27-121">Type: **[**D3DXCOLOR**](d3dxcolor.md)**</span></span>

<span data-ttu-id="43b27-122">地面色彩。</span><span class="sxs-lookup"><span data-stu-id="43b27-122">The ground color.</span></span>

</dd> <dt>

<span data-ttu-id="43b27-123">*pROut* \[在\]</span><span class="sxs-lookup"><span data-stu-id="43b27-123">*pROut* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="43b27-124">類型： **[ **FLOAT**](../winprog/windows-data-types.md)\***</span><span class="sxs-lookup"><span data-stu-id="43b27-124">Type: **[**FLOAT**](../winprog/windows-data-types.md)\***</span></span>

<span data-ttu-id="43b27-125">紅色元件的輸出 SH 向量指標。</span><span class="sxs-lookup"><span data-stu-id="43b27-125">Pointer to the output SH vector for the red component.</span></span>

</dd> <dt>

<span data-ttu-id="43b27-126">*pGOut* \[在\]</span><span class="sxs-lookup"><span data-stu-id="43b27-126">*pGOut* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="43b27-127">類型： **[ **FLOAT**](../winprog/windows-data-types.md)\***</span><span class="sxs-lookup"><span data-stu-id="43b27-127">Type: **[**FLOAT**](../winprog/windows-data-types.md)\***</span></span>

<span data-ttu-id="43b27-128">綠色元件的輸出 SH 向量指標。</span><span class="sxs-lookup"><span data-stu-id="43b27-128">Pointer to the output SH vector for the green component.</span></span>

</dd> <dt>

<span data-ttu-id="43b27-129">*pBOut* \[在\]</span><span class="sxs-lookup"><span data-stu-id="43b27-129">*pBOut* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="43b27-130">類型： **[ **FLOAT**](../winprog/windows-data-types.md)\***</span><span class="sxs-lookup"><span data-stu-id="43b27-130">Type: **[**FLOAT**](../winprog/windows-data-types.md)\***</span></span>

<span data-ttu-id="43b27-131">藍色元件的輸出 SH 向量指標。</span><span class="sxs-lookup"><span data-stu-id="43b27-131">Pointer to the output SH vector for the blue component.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="43b27-132">傳回值</span><span class="sxs-lookup"><span data-stu-id="43b27-132">Return value</span></span>

<span data-ttu-id="43b27-133">類型： **[ **HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**</span><span class="sxs-lookup"><span data-stu-id="43b27-133">Type: **[**HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**</span></span>

<span data-ttu-id="43b27-134">如果函式成功，則傳回值為「D3D \_ 正常」。</span><span class="sxs-lookup"><span data-stu-id="43b27-134">If the function succeeds, the return value is D3D\_OK.</span></span> <span data-ttu-id="43b27-135">如果函式失敗，則傳回值可以是： D3DERR \_ INVALIDCALL。</span><span class="sxs-lookup"><span data-stu-id="43b27-135">If the function fails, the return value can be: D3DERR\_INVALIDCALL.</span></span>

## <a name="remarks"></a><span data-ttu-id="43b27-136">備註</span><span class="sxs-lookup"><span data-stu-id="43b27-136">Remarks</span></span>

<span data-ttu-id="43b27-137">插補會在兩個點之間以線性方式完成，而不是在球體的表面上 (也就是，如果軸是 (0，0，1) 它是 Z 中的線性，而不是 azimuthal 角度) 。</span><span class="sxs-lookup"><span data-stu-id="43b27-137">The interpolation is done linearly between the two points, not over the surface of the sphere (that is, if the axis was (0,0,1) it is linear in Z, not in the azimuthal angle).</span></span> <span data-ttu-id="43b27-138">產生的球形光源函式會正規化，如此一來，完全擴散表面上的點不會有遮蔽，而且方向 *pDir* 的一般指示會導致結束 radiance 值為 1 (如果最上層色彩為白色，而底部的色彩為黑色) 。</span><span class="sxs-lookup"><span data-stu-id="43b27-138">The resulting spherical lighting function is normalized so that a point on a perfectly diffuse surface with no shadowing and a normal pointed in the direction *pDir* would result in exit radiance with a value of 1 (if the top color was white and the bottom color was black).</span></span> <span data-ttu-id="43b27-139">這是非常簡單的模型，其中 *Top* 代表「天空」的濃度，而 *底部* 代表「地面」的強度。</span><span class="sxs-lookup"><span data-stu-id="43b27-139">This is a very simple model where *Top* represents the intensity of the "sky" and *Bottom* represents the intensity of the "ground."</span></span>

<span data-ttu-id="43b27-140">如下圖所示，在具有單位半徑的球體上，可以只使用 theta、 [右邊](coordinate-systems.md)的 Z 軸角度和 phi （z 的角度）來指定方向。</span><span class="sxs-lookup"><span data-stu-id="43b27-140">On the sphere with unit radius, as shown in the following illustration, direction can be specified simply with theta, the angle about the z-axis in the [right-handed direction](coordinate-systems.md), and phi, the angle from z.</span></span>

![具有單位半徑之球體的圖例](images/spherical-coordinates.png)

<span data-ttu-id="43b27-142">下列方會顯示笛卡兒 (x、y、z) 和球面 (theta 之間的關聯性，以及單位球體上的 phi) 座標。</span><span class="sxs-lookup"><span data-stu-id="43b27-142">The following equations show the relationship between Cartesian (x, y, z) and spherical (theta, phi) coordinates on the unit sphere.</span></span> <span data-ttu-id="43b27-143">角度 theta 會因0到 2 pi 的範圍而異，而 phi 則是從0到 pi 的變化。</span><span class="sxs-lookup"><span data-stu-id="43b27-143">The angle theta varies over the range of 0 to 2 pi, while phi varies from 0 to pi.</span></span>

![笛卡兒和球面座標之間關聯性的方程式](images/spherical-coordinates-equations.png)

## <a name="requirements"></a><span data-ttu-id="43b27-145">規格需求</span><span class="sxs-lookup"><span data-stu-id="43b27-145">Requirements</span></span>



| <span data-ttu-id="43b27-146">需求</span><span class="sxs-lookup"><span data-stu-id="43b27-146">Requirement</span></span> | <span data-ttu-id="43b27-147">值</span><span class="sxs-lookup"><span data-stu-id="43b27-147">Value</span></span> |
|--------------------|----------------------------------------------------------------------------------------|
| <span data-ttu-id="43b27-148">標頭</span><span class="sxs-lookup"><span data-stu-id="43b27-148">Header</span></span><br/>  | <dl> <span data-ttu-id="43b27-149"><dt>D3dx9math。h</dt></span><span class="sxs-lookup"><span data-stu-id="43b27-149"><dt>D3dx9math.h</dt></span></span> </dl> |
| <span data-ttu-id="43b27-150">程式庫</span><span class="sxs-lookup"><span data-stu-id="43b27-150">Library</span></span><br/> | <dl> <span data-ttu-id="43b27-151"><dt>D3dx9 .lib</dt></span><span class="sxs-lookup"><span data-stu-id="43b27-151"><dt>D3dx9.lib</dt></span></span> </dl>   |



## <a name="see-also"></a><span data-ttu-id="43b27-152">另請參閱</span><span class="sxs-lookup"><span data-stu-id="43b27-152">See also</span></span>

<dl> <dt>

[<span data-ttu-id="43b27-153">數學函數</span><span class="sxs-lookup"><span data-stu-id="43b27-153">Math Functions</span></span>](dx9-graphics-reference-d3dx-functions-math.md)
</dt> <dt>

[<span data-ttu-id="43b27-154">預先計算 Radiance Transfer (Direct3D 9) </span><span class="sxs-lookup"><span data-stu-id="43b27-154">Precomputed Radiance Transfer (Direct3D 9)</span></span>](precomputed-radiance-transfer.md)
</dt> </dl>

 

 
