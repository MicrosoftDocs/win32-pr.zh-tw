---
description: 從輸入方向向量評估球面調和 (SH) 基礎函數。
ms.assetid: f30ba32c-d6b0-4e4e-b5cd-839ed7821855
title: 'D3DXSHEvalDirection 函式 (D3dx9math) '
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- D3DXSHEvalDirection
api_type:
- LibDef
api_location:
- d3dx9.lib
- d3dx9.dll
ms.openlocfilehash: 005785667d25888550dea38c765a96ea56646d76
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 03/15/2021
ms.locfileid: "104558017"
---
# <a name="d3dxshevaldirection-function-d3dx9mathh"></a><span data-ttu-id="b2427-103">D3DXSHEvalDirection 函式 (D3dx9math) </span><span class="sxs-lookup"><span data-stu-id="b2427-103">D3DXSHEvalDirection function (D3dx9math.h)</span></span>

<span data-ttu-id="b2427-104">從輸入方向向量評估球面調和 (SH) 基礎函數。</span><span class="sxs-lookup"><span data-stu-id="b2427-104">Evaluates the spherical harmonic (SH) basis functions from an input direction vector.</span></span>

## <a name="syntax"></a><span data-ttu-id="b2427-105">語法</span><span class="sxs-lookup"><span data-stu-id="b2427-105">Syntax</span></span>


```C++
FLOAT* D3DXSHEvalDirection(
  _Out_       FLOAT       *pOut,
  _In_        UINT        Order,
  _In_  const D3DXVECTOR3 *pDir
);
```



## <a name="parameters"></a><span data-ttu-id="b2427-106">參數</span><span class="sxs-lookup"><span data-stu-id="b2427-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="b2427-107">*不悅* \[擴展\]</span><span class="sxs-lookup"><span data-stu-id="b2427-107">*pOut* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="b2427-108">類型： **[ **FLOAT**](../winprog/windows-data-types.md)\***</span><span class="sxs-lookup"><span data-stu-id="b2427-108">Type: **[**FLOAT**](../winprog/windows-data-types.md)\***</span></span>

<span data-ttu-id="b2427-109">球面調和 (SH) 輸出係數的指標。</span><span class="sxs-lookup"><span data-stu-id="b2427-109">Pointer to Spherical harmonic (SH) output coefficients.</span></span> <span data-ttu-id="b2427-110">評估會產生順序²係數。</span><span class="sxs-lookup"><span data-stu-id="b2427-110">The evaluation generates Order² coefficients.</span></span> <span data-ttu-id="b2427-111">請參閱＜備註＞。</span><span class="sxs-lookup"><span data-stu-id="b2427-111">See Remarks.</span></span>

</dd> <dt>

<span data-ttu-id="b2427-112">*訂單* \[在\]</span><span class="sxs-lookup"><span data-stu-id="b2427-112">*Order* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="b2427-113">類型： **[ **UINT**](../winprog/windows-data-types.md)**</span><span class="sxs-lookup"><span data-stu-id="b2427-113">Type: **[**UINT**](../winprog/windows-data-types.md)**</span></span>

<span data-ttu-id="b2427-114">SH 評估的順序。</span><span class="sxs-lookup"><span data-stu-id="b2427-114">Order of the SH evaluation.</span></span> <span data-ttu-id="b2427-115">必須在 [D3DXSH \_ MINORDER](other-d3dx-constants.md) 到 D3DXSH \_ MAXORDER （含）的範圍內。</span><span class="sxs-lookup"><span data-stu-id="b2427-115">Must be in the range of [D3DXSH\_MINORDER](other-d3dx-constants.md) to D3DXSH\_MAXORDER, inclusive.</span></span> <span data-ttu-id="b2427-116">評估會產生順序²係數。</span><span class="sxs-lookup"><span data-stu-id="b2427-116">The evaluation generates Order² coefficients.</span></span> <span data-ttu-id="b2427-117">評估的程度是順序-1。</span><span class="sxs-lookup"><span data-stu-id="b2427-117">The degree of the evaluation is Order - 1.</span></span>

</dd> <dt>

<span data-ttu-id="b2427-118">*pDir* \[在\]</span><span class="sxs-lookup"><span data-stu-id="b2427-118">*pDir* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="b2427-119">Type： **Const [**D3DXVECTOR3**](d3dxvector3.md) \***</span><span class="sxs-lookup"><span data-stu-id="b2427-119">Type: **const [**D3DXVECTOR3**](d3dxvector3.md)\***</span></span>

<span data-ttu-id="b2427-120"> (x，y，z) 方向向量，用來評估 SH 基礎函數。</span><span class="sxs-lookup"><span data-stu-id="b2427-120">(x, y, z) direction vector in which to evaluate the SH basis functions.</span></span> <span data-ttu-id="b2427-121">必須正規化。</span><span class="sxs-lookup"><span data-stu-id="b2427-121">Must be normalized.</span></span> <span data-ttu-id="b2427-122">請參閱＜備註＞。</span><span class="sxs-lookup"><span data-stu-id="b2427-122">See Remarks.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="b2427-123">傳回值</span><span class="sxs-lookup"><span data-stu-id="b2427-123">Return value</span></span>

<span data-ttu-id="b2427-124">類型： **[ **FLOAT**](../winprog/windows-data-types.md)\***</span><span class="sxs-lookup"><span data-stu-id="b2427-124">Type: **[**FLOAT**](../winprog/windows-data-types.md)\***</span></span>

<span data-ttu-id="b2427-125">SH 輸出係數的指標。</span><span class="sxs-lookup"><span data-stu-id="b2427-125">Pointer to SH output coefficients.</span></span> <span data-ttu-id="b2427-126">請參閱＜備註＞。</span><span class="sxs-lookup"><span data-stu-id="b2427-126">See Remarks.</span></span>

## <a name="remarks"></a><span data-ttu-id="b2427-127">備註</span><span class="sxs-lookup"><span data-stu-id="b2427-127">Remarks</span></span>

<span data-ttu-id="b2427-128">基礎函數 Ylm 的每個係數都會儲存在記憶體位置 l ² + m + l，其中：</span><span class="sxs-lookup"><span data-stu-id="b2427-128">Each coefficient of the basis function Yₗₘ is stored at memory location l² + m + l, where:</span></span>

-   <span data-ttu-id="b2427-129">l 是基礎函數的程度。</span><span class="sxs-lookup"><span data-stu-id="b2427-129">l is the degree of the basis function.</span></span>
-   <span data-ttu-id="b2427-130">m 是指定 l 值的基礎函數索引，範圍從-l 到 l （含）。</span><span class="sxs-lookup"><span data-stu-id="b2427-130">m is the basis function index for the given l value and ranges from -l to l, inclusive.</span></span>

<span data-ttu-id="b2427-131">如下圖所示，在具有單位半徑的球體上，可以只使用 theta、 [右邊](coordinate-systems.md)的 Z 軸角度和 phi （z 的角度）來指定方向。</span><span class="sxs-lookup"><span data-stu-id="b2427-131">On the sphere with unit radius, as shown in the following illustration, direction can be specified simply with theta, the angle about the z-axis in the [right-handed direction](coordinate-systems.md), and phi, the angle from z.</span></span>

![具有單位半徑之球體的圖例](images/spherical-coordinates.png)

<span data-ttu-id="b2427-133">下列方會顯示笛卡兒 (x、y、z) 和球面 (theta 之間的關聯性，以及單位球體上的 phi) 座標。</span><span class="sxs-lookup"><span data-stu-id="b2427-133">The following equations show the relationship between Cartesian (x, y, z) and spherical (theta, phi) coordinates on the unit sphere.</span></span> <span data-ttu-id="b2427-134">角度 theta 會因0到 2 pi 的範圍而異，而 phi 則是從0到 pi 的變化。</span><span class="sxs-lookup"><span data-stu-id="b2427-134">The angle theta varies over the range of 0 to 2 pi, while phi varies from 0 to pi.</span></span>

![笛卡兒和球面座標之間關聯性的方程式](images/spherical-coordinates-equations.png)

## <a name="requirements"></a><span data-ttu-id="b2427-136">規格需求</span><span class="sxs-lookup"><span data-stu-id="b2427-136">Requirements</span></span>



| <span data-ttu-id="b2427-137">需求</span><span class="sxs-lookup"><span data-stu-id="b2427-137">Requirement</span></span> | <span data-ttu-id="b2427-138">值</span><span class="sxs-lookup"><span data-stu-id="b2427-138">Value</span></span> |
|--------------------|----------------------------------------------------------------------------------------|
| <span data-ttu-id="b2427-139">標頭</span><span class="sxs-lookup"><span data-stu-id="b2427-139">Header</span></span><br/>  | <dl> <span data-ttu-id="b2427-140"><dt>D3dx9math。h</dt></span><span class="sxs-lookup"><span data-stu-id="b2427-140"><dt>D3dx9math.h</dt></span></span> </dl> |
| <span data-ttu-id="b2427-141">程式庫</span><span class="sxs-lookup"><span data-stu-id="b2427-141">Library</span></span><br/> | <dl> <span data-ttu-id="b2427-142"><dt>D3dx9 .lib</dt></span><span class="sxs-lookup"><span data-stu-id="b2427-142"><dt>D3dx9.lib</dt></span></span> </dl>   |



## <a name="see-also"></a><span data-ttu-id="b2427-143">另請參閱</span><span class="sxs-lookup"><span data-stu-id="b2427-143">See also</span></span>

<dl> <dt>

[<span data-ttu-id="b2427-144">數學函數</span><span class="sxs-lookup"><span data-stu-id="b2427-144">Math Functions</span></span>](dx9-graphics-reference-d3dx-functions-math.md)
</dt> <dt>

[<span data-ttu-id="b2427-145">預先計算 Radiance Transfer (Direct3D 9) </span><span class="sxs-lookup"><span data-stu-id="b2427-145">Precomputed Radiance Transfer (Direct3D 9)</span></span>](precomputed-radiance-transfer.md)
</dt> </dl>

 

 
