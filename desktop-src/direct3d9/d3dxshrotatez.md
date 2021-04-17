---
description: 將球形調和 (SH) 向量旋轉指定角度的 Z 軸。
ms.assetid: 1f471183-4c8e-4fa8-9a42-f6cc2bb1b0f2
title: 'D3DXSHRotateZ 函式 (D3dx9math) '
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- D3DXSHRotateZ
api_type:
- LibDef
api_location:
- d3dx9.lib
- d3dx9.dll
ms.openlocfilehash: ac13cff212aaabdd8a9586b88e3152779bcfaf85
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 03/15/2021
ms.locfileid: "104386453"
---
# <a name="d3dxshrotatez-function-d3dx9mathh"></a><span data-ttu-id="7775a-103">D3DXSHRotateZ 函式 (D3dx9math) </span><span class="sxs-lookup"><span data-stu-id="7775a-103">D3DXSHRotateZ function (D3dx9math.h)</span></span>

<span data-ttu-id="7775a-104">將球形調和 (SH) 向量旋轉指定角度的 Z 軸。</span><span class="sxs-lookup"><span data-stu-id="7775a-104">Rotates the spherical harmonic (SH) vector in the z-axis by the given angle.</span></span>

## <a name="syntax"></a><span data-ttu-id="7775a-105">語法</span><span class="sxs-lookup"><span data-stu-id="7775a-105">Syntax</span></span>


```C++
FLOAT* D3DXSHRotateZ(
  _Out_       FLOAT *pOut,
  _In_        UINT  Order,
  _In_        FLOAT Angle,
  _In_  const FLOAT *pIn
);
```



## <a name="parameters"></a><span data-ttu-id="7775a-106">參數</span><span class="sxs-lookup"><span data-stu-id="7775a-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="7775a-107">*不悅* \[擴展\]</span><span class="sxs-lookup"><span data-stu-id="7775a-107">*pOut* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="7775a-108">類型： **[ **FLOAT**](../winprog/windows-data-types.md)\***</span><span class="sxs-lookup"><span data-stu-id="7775a-108">Type: **[**FLOAT**](../winprog/windows-data-types.md)\***</span></span>

<span data-ttu-id="7775a-109">球面調和 (SH) 輸出係數的指標。</span><span class="sxs-lookup"><span data-stu-id="7775a-109">Pointer to Spherical harmonic (SH) output coefficients.</span></span> <span data-ttu-id="7775a-110">評估會產生順序²係數。</span><span class="sxs-lookup"><span data-stu-id="7775a-110">The evaluation generates Order² coefficients.</span></span> <span data-ttu-id="7775a-111">此指標不應使用 *pIn* 別名。</span><span class="sxs-lookup"><span data-stu-id="7775a-111">This pointer should not alias with *pIn*.</span></span> <span data-ttu-id="7775a-112">請參閱＜備註＞。</span><span class="sxs-lookup"><span data-stu-id="7775a-112">See Remarks.</span></span>

</dd> <dt>

<span data-ttu-id="7775a-113">*訂單* \[在\]</span><span class="sxs-lookup"><span data-stu-id="7775a-113">*Order* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="7775a-114">類型： **[ **UINT**](../winprog/windows-data-types.md)**</span><span class="sxs-lookup"><span data-stu-id="7775a-114">Type: **[**UINT**](../winprog/windows-data-types.md)**</span></span>

<span data-ttu-id="7775a-115">SH 評估的順序。</span><span class="sxs-lookup"><span data-stu-id="7775a-115">Order of the SH evaluation.</span></span> <span data-ttu-id="7775a-116">必須在 [D3DXSH \_ MINORDER](other-d3dx-constants.md) 到 D3DXSH \_ MAXORDER （含）的範圍內。</span><span class="sxs-lookup"><span data-stu-id="7775a-116">Must be in the range of [D3DXSH\_MINORDER](other-d3dx-constants.md) to D3DXSH\_MAXORDER, inclusive.</span></span> <span data-ttu-id="7775a-117">評估會產生順序²係數。</span><span class="sxs-lookup"><span data-stu-id="7775a-117">The evaluation generates Order² coefficients.</span></span> <span data-ttu-id="7775a-118">評估的程度是順序-1。</span><span class="sxs-lookup"><span data-stu-id="7775a-118">The degree of the evaluation is Order - 1.</span></span>

</dd> <dt>

<span data-ttu-id="7775a-119">*角度* \[在\]</span><span class="sxs-lookup"><span data-stu-id="7775a-119">*Angle* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="7775a-120">類型： **[ **FLOAT**](../winprog/windows-data-types.md)**</span><span class="sxs-lookup"><span data-stu-id="7775a-120">Type: **[**FLOAT**](../winprog/windows-data-types.md)**</span></span>

<span data-ttu-id="7775a-121">旋轉角度（以弧度為單位）。</span><span class="sxs-lookup"><span data-stu-id="7775a-121">Rotation angle in radians.</span></span> <span data-ttu-id="7775a-122">旋轉是圍繞 Z 軸來執行。</span><span class="sxs-lookup"><span data-stu-id="7775a-122">The rotation is performed around the z-axis.</span></span>

</dd> <dt>

<span data-ttu-id="7775a-123">*pIn* \[在\]</span><span class="sxs-lookup"><span data-stu-id="7775a-123">*pIn* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="7775a-124">Type： **Const [**FLOAT**](../winprog/windows-data-types.md) \***</span><span class="sxs-lookup"><span data-stu-id="7775a-124">Type: **const [**FLOAT**](../winprog/windows-data-types.md)\***</span></span>

<span data-ttu-id="7775a-125">旋轉的 SH 係數指標。</span><span class="sxs-lookup"><span data-stu-id="7775a-125">Pointer to rotated SH coefficients.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="7775a-126">傳回值</span><span class="sxs-lookup"><span data-stu-id="7775a-126">Return value</span></span>

<span data-ttu-id="7775a-127">類型： **[ **FLOAT**](../winprog/windows-data-types.md)\***</span><span class="sxs-lookup"><span data-stu-id="7775a-127">Type: **[**FLOAT**](../winprog/windows-data-types.md)\***</span></span>

<span data-ttu-id="7775a-128">SH 輸出係數的指標。</span><span class="sxs-lookup"><span data-stu-id="7775a-128">Pointer to SH output coefficients.</span></span>

## <a name="remarks"></a><span data-ttu-id="7775a-129">備註</span><span class="sxs-lookup"><span data-stu-id="7775a-129">Remarks</span></span>

<span data-ttu-id="7775a-130">基礎函數 Ylm 的每個係數都會儲存在記憶體位置 l ² + m + l，其中：</span><span class="sxs-lookup"><span data-stu-id="7775a-130">Each coefficient of the basis function Yₗₘ is stored at memory location l² + m + l, where:</span></span>

-   <span data-ttu-id="7775a-131">l 是基礎函數的程度。</span><span class="sxs-lookup"><span data-stu-id="7775a-131">l is the degree of the basis function.</span></span>
-   <span data-ttu-id="7775a-132">m 是指定 l 值的基礎函數索引，範圍從-l 到 l （含）。</span><span class="sxs-lookup"><span data-stu-id="7775a-132">m is the basis function index for the given l value and ranges from -l to l, inclusive.</span></span>

## <a name="requirements"></a><span data-ttu-id="7775a-133">規格需求</span><span class="sxs-lookup"><span data-stu-id="7775a-133">Requirements</span></span>



| <span data-ttu-id="7775a-134">需求</span><span class="sxs-lookup"><span data-stu-id="7775a-134">Requirement</span></span> | <span data-ttu-id="7775a-135">值</span><span class="sxs-lookup"><span data-stu-id="7775a-135">Value</span></span> |
|--------------------|----------------------------------------------------------------------------------------|
| <span data-ttu-id="7775a-136">標頭</span><span class="sxs-lookup"><span data-stu-id="7775a-136">Header</span></span><br/>  | <dl> <span data-ttu-id="7775a-137"><dt>D3dx9math。h</dt></span><span class="sxs-lookup"><span data-stu-id="7775a-137"><dt>D3dx9math.h</dt></span></span> </dl> |
| <span data-ttu-id="7775a-138">程式庫</span><span class="sxs-lookup"><span data-stu-id="7775a-138">Library</span></span><br/> | <dl> <span data-ttu-id="7775a-139"><dt>D3dx9 .lib</dt></span><span class="sxs-lookup"><span data-stu-id="7775a-139"><dt>D3dx9.lib</dt></span></span> </dl>   |



## <a name="see-also"></a><span data-ttu-id="7775a-140">另請參閱</span><span class="sxs-lookup"><span data-stu-id="7775a-140">See also</span></span>

<dl> <dt>

[<span data-ttu-id="7775a-141">數學函數</span><span class="sxs-lookup"><span data-stu-id="7775a-141">Math Functions</span></span>](dx9-graphics-reference-d3dx-functions-math.md)
</dt> <dt>

[<span data-ttu-id="7775a-142">預先計算 Radiance Transfer (Direct3D 9) </span><span class="sxs-lookup"><span data-stu-id="7775a-142">Precomputed Radiance Transfer (Direct3D 9)</span></span>](precomputed-radiance-transfer.md)
</dt> </dl>

 

 
