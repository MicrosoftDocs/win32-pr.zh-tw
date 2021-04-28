---
description: D3DXSHRotateZ 函式 (D3DX10) -將球形調和 (SH) 向量在 Z 軸中的指定角度旋轉。
ms.assetid: 7c4bec55-4a4c-4f7e-8849-1cac373a2340
title: 'D3DXSHRotateZ 函式 (D3DX10) '
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
- D3DX10.lib
- D3DX10.dll
ms.openlocfilehash: 55e4663057bd25ac9768a5913963a5511b662f11
ms.sourcegitcommit: 95685061d5b0333bbf9e6ebd208dde8190f97005
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 04/28/2021
ms.locfileid: "108108526"
---
# <a name="d3dxshrotatez-function-d3dx10h"></a><span data-ttu-id="2234e-103">D3DXSHRotateZ 函式 (D3DX10) </span><span class="sxs-lookup"><span data-stu-id="2234e-103">D3DXSHRotateZ function (D3DX10.h)</span></span>

<span data-ttu-id="2234e-104">將球形調和 (SH) 向量旋轉指定角度的 Z 軸。</span><span class="sxs-lookup"><span data-stu-id="2234e-104">Rotates the spherical harmonic (SH) vector in the z-axis by the given angle.</span></span>

## <a name="syntax"></a><span data-ttu-id="2234e-105">語法</span><span class="sxs-lookup"><span data-stu-id="2234e-105">Syntax</span></span>


```C++
FLOAT* D3DXSHRotateZ(
  _In_       FLOAT *pOut,
  _In_       UINT  Order,
  _In_       FLOAT Angle,
  _In_ const FLOAT *pIn
);
```



## <a name="parameters"></a><span data-ttu-id="2234e-106">參數</span><span class="sxs-lookup"><span data-stu-id="2234e-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="2234e-107">*不悅* \[在\]</span><span class="sxs-lookup"><span data-stu-id="2234e-107">*pOut* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="2234e-108">類型： **[ **FLOAT**](../winprog/windows-data-types.md)\***</span><span class="sxs-lookup"><span data-stu-id="2234e-108">Type: **[**FLOAT**](../winprog/windows-data-types.md)\***</span></span>

<span data-ttu-id="2234e-109">球面調和 (SH) 輸出係數的指標。</span><span class="sxs-lookup"><span data-stu-id="2234e-109">Pointer to Spherical harmonic (SH) output coefficients.</span></span> <span data-ttu-id="2234e-110">評估會產生順序²係數。</span><span class="sxs-lookup"><span data-stu-id="2234e-110">The evaluation generates Order² coefficients.</span></span> <span data-ttu-id="2234e-111">此指標不應使用 pIn 別名。</span><span class="sxs-lookup"><span data-stu-id="2234e-111">This pointer should not alias with pIn.</span></span> <span data-ttu-id="2234e-112">請參閱＜備註＞。</span><span class="sxs-lookup"><span data-stu-id="2234e-112">See Remarks.</span></span>

</dd> <dt>

<span data-ttu-id="2234e-113">*訂單* \[在\]</span><span class="sxs-lookup"><span data-stu-id="2234e-113">*Order* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="2234e-114">類型： **[ **UINT**](../winprog/windows-data-types.md)**</span><span class="sxs-lookup"><span data-stu-id="2234e-114">Type: **[**UINT**](../winprog/windows-data-types.md)**</span></span>

<span data-ttu-id="2234e-115">SH 評估的順序。</span><span class="sxs-lookup"><span data-stu-id="2234e-115">Order of the SH evaluation.</span></span> <span data-ttu-id="2234e-116">必須在 D3DXSH \_ MINORDER 到 D3DXSH \_ MAXORDER （含）的範圍內。</span><span class="sxs-lookup"><span data-stu-id="2234e-116">Must be in the range of D3DXSH\_MINORDER to D3DXSH\_MAXORDER, inclusive.</span></span> <span data-ttu-id="2234e-117">評估會產生順序²係數。</span><span class="sxs-lookup"><span data-stu-id="2234e-117">The evaluation generates Order² coefficients.</span></span> <span data-ttu-id="2234e-118">評估的程度是順序-1。</span><span class="sxs-lookup"><span data-stu-id="2234e-118">The degree of the evaluation is Order - 1.</span></span>

</dd> <dt>

<span data-ttu-id="2234e-119">*角度* \[在\]</span><span class="sxs-lookup"><span data-stu-id="2234e-119">*Angle* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="2234e-120">類型： **[ **FLOAT**](../winprog/windows-data-types.md)**</span><span class="sxs-lookup"><span data-stu-id="2234e-120">Type: **[**FLOAT**](../winprog/windows-data-types.md)**</span></span>

<span data-ttu-id="2234e-121">旋轉角度（以弧度為單位）。</span><span class="sxs-lookup"><span data-stu-id="2234e-121">Rotation angle in radians.</span></span> <span data-ttu-id="2234e-122">旋轉是圍繞 Z 軸來執行。</span><span class="sxs-lookup"><span data-stu-id="2234e-122">The rotation is performed around the z-axis.</span></span>

</dd> <dt>

<span data-ttu-id="2234e-123">*pIn* \[在\]</span><span class="sxs-lookup"><span data-stu-id="2234e-123">*pIn* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="2234e-124">Type： **Const [**FLOAT**](../winprog/windows-data-types.md) \***</span><span class="sxs-lookup"><span data-stu-id="2234e-124">Type: **const [**FLOAT**](../winprog/windows-data-types.md)\***</span></span>

<span data-ttu-id="2234e-125">旋轉的 SH 係數指標。</span><span class="sxs-lookup"><span data-stu-id="2234e-125">Pointer to rotated SH coefficients.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="2234e-126">傳回值</span><span class="sxs-lookup"><span data-stu-id="2234e-126">Return value</span></span>

<span data-ttu-id="2234e-127">類型： **[ **FLOAT**](../winprog/windows-data-types.md)\***</span><span class="sxs-lookup"><span data-stu-id="2234e-127">Type: **[**FLOAT**](../winprog/windows-data-types.md)\***</span></span>

<span data-ttu-id="2234e-128">SH 輸出係數的指標。</span><span class="sxs-lookup"><span data-stu-id="2234e-128">Pointer to SH output coefficients.</span></span>

## <a name="remarks"></a><span data-ttu-id="2234e-129">備註</span><span class="sxs-lookup"><span data-stu-id="2234e-129">Remarks</span></span>

<span data-ttu-id="2234e-130">基礎函數 Ylm 的每個係數都會儲存在記憶體位置 l ² + m + l，其中：</span><span class="sxs-lookup"><span data-stu-id="2234e-130">Each coefficient of the basis function Yₗₘ is stored at memory location l² + m + l, where:</span></span>

-   <span data-ttu-id="2234e-131">l 是基礎函數的程度。</span><span class="sxs-lookup"><span data-stu-id="2234e-131">l is the degree of the basis function.</span></span>
-   <span data-ttu-id="2234e-132">m 是指定 l 值的基礎函數索引，範圍從-l 到 l （含）。</span><span class="sxs-lookup"><span data-stu-id="2234e-132">m is the basis function index for the given l value and ranges from -l to l, inclusive.</span></span>

## <a name="requirements"></a><span data-ttu-id="2234e-133">規格需求</span><span class="sxs-lookup"><span data-stu-id="2234e-133">Requirements</span></span>



| <span data-ttu-id="2234e-134">需求</span><span class="sxs-lookup"><span data-stu-id="2234e-134">Requirement</span></span> | <span data-ttu-id="2234e-135">值</span><span class="sxs-lookup"><span data-stu-id="2234e-135">Value</span></span> |
|--------------------|---------------------------------------------------------------------------------------|
| <span data-ttu-id="2234e-136">標頭</span><span class="sxs-lookup"><span data-stu-id="2234e-136">Header</span></span><br/>  | <dl> <span data-ttu-id="2234e-137"><dt>D3DX10。h</dt></span><span class="sxs-lookup"><span data-stu-id="2234e-137"><dt>D3DX10.h</dt></span></span> </dl>   |
| <span data-ttu-id="2234e-138">程式庫</span><span class="sxs-lookup"><span data-stu-id="2234e-138">Library</span></span><br/> | <dl> <span data-ttu-id="2234e-139"><dt>D3DX10 .lib</dt></span><span class="sxs-lookup"><span data-stu-id="2234e-139"><dt>D3DX10.lib</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="2234e-140">另請參閱</span><span class="sxs-lookup"><span data-stu-id="2234e-140">See also</span></span>

<dl> <dt>

[<span data-ttu-id="2234e-141">數學函數</span><span class="sxs-lookup"><span data-stu-id="2234e-141">Math Functions</span></span>](d3d10-graphics-reference-d3dx10-functions-math.md)
</dt> </dl>

 

 
