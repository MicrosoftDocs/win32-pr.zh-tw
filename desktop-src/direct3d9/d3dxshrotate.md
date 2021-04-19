---
description: 將球形調和 (SH) 向量旋轉指定的矩陣。
ms.assetid: 9e319725-6cbb-441e-b996-ec2c6f66e5df
title: 'D3DXSHRotate 函式 (D3dx9math) '
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- D3DXSHRotate
api_type:
- LibDef
api_location:
- d3dx9.lib
- d3dx9.dll
ms.openlocfilehash: 606ef1909237fd9c0277c5d7112284f6b7018e0e
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 03/15/2021
ms.locfileid: "106992312"
---
# <a name="d3dxshrotate-function-d3dx9mathh"></a><span data-ttu-id="2bf66-103">D3DXSHRotate 函式 (D3dx9math) </span><span class="sxs-lookup"><span data-stu-id="2bf66-103">D3DXSHRotate function (D3dx9math.h)</span></span>

<span data-ttu-id="2bf66-104">將球形調和 (SH) 向量旋轉指定的矩陣。</span><span class="sxs-lookup"><span data-stu-id="2bf66-104">Rotates the spherical harmonic (SH) vector by the given matrix.</span></span>

## <a name="syntax"></a><span data-ttu-id="2bf66-105">語法</span><span class="sxs-lookup"><span data-stu-id="2bf66-105">Syntax</span></span>


```C++
FLOAT* D3DXSHRotate(
  _Out_       FLOAT      *pOut,
  _In_        UINT       Order,
  _In_  const D3DXMATRIX *pMatrix,
  _In_  const FLOAT      *pIn
);
```



## <a name="parameters"></a><span data-ttu-id="2bf66-106">參數</span><span class="sxs-lookup"><span data-stu-id="2bf66-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="2bf66-107">*不悅* \[擴展\]</span><span class="sxs-lookup"><span data-stu-id="2bf66-107">*pOut* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="2bf66-108">類型： **[ **FLOAT**](../winprog/windows-data-types.md)\***</span><span class="sxs-lookup"><span data-stu-id="2bf66-108">Type: **[**FLOAT**](../winprog/windows-data-types.md)\***</span></span>

<span data-ttu-id="2bf66-109">球面調和 (SH) 輸出係數的指標。</span><span class="sxs-lookup"><span data-stu-id="2bf66-109">Pointer to Spherical harmonic (SH) output coefficients.</span></span> <span data-ttu-id="2bf66-110">評估會產生順序²係數。</span><span class="sxs-lookup"><span data-stu-id="2bf66-110">The evaluation generates Order² coefficients.</span></span> <span data-ttu-id="2bf66-111">此指標不應使用 *pIn* 別名。</span><span class="sxs-lookup"><span data-stu-id="2bf66-111">This pointer should not alias with *pIn*.</span></span> <span data-ttu-id="2bf66-112">請參閱＜備註＞。</span><span class="sxs-lookup"><span data-stu-id="2bf66-112">See Remarks.</span></span>

</dd> <dt>

<span data-ttu-id="2bf66-113">*訂單* \[在\]</span><span class="sxs-lookup"><span data-stu-id="2bf66-113">*Order* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="2bf66-114">類型： **[ **UINT**](../winprog/windows-data-types.md)**</span><span class="sxs-lookup"><span data-stu-id="2bf66-114">Type: **[**UINT**](../winprog/windows-data-types.md)**</span></span>

<span data-ttu-id="2bf66-115">SH 評估的順序。</span><span class="sxs-lookup"><span data-stu-id="2bf66-115">Order of the SH evaluation.</span></span> <span data-ttu-id="2bf66-116">必須在 [D3DXSH \_ MINORDER](other-d3dx-constants.md) 到 D3DXSH \_ MAXORDER （含）的範圍內。</span><span class="sxs-lookup"><span data-stu-id="2bf66-116">Must be in the range of [D3DXSH\_MINORDER](other-d3dx-constants.md) to D3DXSH\_MAXORDER, inclusive.</span></span> <span data-ttu-id="2bf66-117">評估會產生順序²係數。</span><span class="sxs-lookup"><span data-stu-id="2bf66-117">The evaluation generates Order² coefficients.</span></span> <span data-ttu-id="2bf66-118">評估的程度是順序-1。</span><span class="sxs-lookup"><span data-stu-id="2bf66-118">The degree of the evaluation is Order - 1.</span></span>

</dd> <dt>

<span data-ttu-id="2bf66-119">*pMatrix* \[在\]</span><span class="sxs-lookup"><span data-stu-id="2bf66-119">*pMatrix* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="2bf66-120">Type： **Const [**D3DXMATRIX**](d3dxmatrix.md) \***</span><span class="sxs-lookup"><span data-stu-id="2bf66-120">Type: **const [**D3DXMATRIX**](d3dxmatrix.md)\***</span></span>

<span data-ttu-id="2bf66-121">旋轉矩陣的指標。</span><span class="sxs-lookup"><span data-stu-id="2bf66-121">Pointer to the rotation matrix.</span></span> <span data-ttu-id="2bf66-122">旋轉子矩陣必須是垂直的，且具有單位行列式。</span><span class="sxs-lookup"><span data-stu-id="2bf66-122">The rotation sub-matrix must be orthogonal, with a unit determinant.</span></span>

</dd> <dt>

<span data-ttu-id="2bf66-123">*pIn* \[在\]</span><span class="sxs-lookup"><span data-stu-id="2bf66-123">*pIn* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="2bf66-124">Type： **Const [**FLOAT**](../winprog/windows-data-types.md) \***</span><span class="sxs-lookup"><span data-stu-id="2bf66-124">Type: **const [**FLOAT**](../winprog/windows-data-types.md)\***</span></span>

<span data-ttu-id="2bf66-125">旋轉的 SH 係數指標。</span><span class="sxs-lookup"><span data-stu-id="2bf66-125">Pointer to rotated SH coefficients.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="2bf66-126">傳回值</span><span class="sxs-lookup"><span data-stu-id="2bf66-126">Return value</span></span>

<span data-ttu-id="2bf66-127">類型： **[ **FLOAT**](../winprog/windows-data-types.md)\***</span><span class="sxs-lookup"><span data-stu-id="2bf66-127">Type: **[**FLOAT**](../winprog/windows-data-types.md)\***</span></span>

<span data-ttu-id="2bf66-128">SH 輸出係數的指標。</span><span class="sxs-lookup"><span data-stu-id="2bf66-128">Pointer to SH output coefficients.</span></span>

## <a name="remarks"></a><span data-ttu-id="2bf66-129">備註</span><span class="sxs-lookup"><span data-stu-id="2bf66-129">Remarks</span></span>

<span data-ttu-id="2bf66-130">基礎函數 Ylm 的每個係數都會儲存在記憶體位置 l ² + m + l，其中：</span><span class="sxs-lookup"><span data-stu-id="2bf66-130">Each coefficient of the basis function Yₗₘ is stored at memory location l² + m + l, where:</span></span>

-   <span data-ttu-id="2bf66-131">l 是基礎函數的程度。</span><span class="sxs-lookup"><span data-stu-id="2bf66-131">l is the degree of the basis function.</span></span>
-   <span data-ttu-id="2bf66-132">m 是指定 l 值的基礎函數索引，範圍從-l 到 l （含）。</span><span class="sxs-lookup"><span data-stu-id="2bf66-132">m is the basis function index for the given l value and ranges from -l to l, inclusive.</span></span>

## <a name="requirements"></a><span data-ttu-id="2bf66-133">規格需求</span><span class="sxs-lookup"><span data-stu-id="2bf66-133">Requirements</span></span>



| <span data-ttu-id="2bf66-134">需求</span><span class="sxs-lookup"><span data-stu-id="2bf66-134">Requirement</span></span> | <span data-ttu-id="2bf66-135">值</span><span class="sxs-lookup"><span data-stu-id="2bf66-135">Value</span></span> |
|--------------------|----------------------------------------------------------------------------------------|
| <span data-ttu-id="2bf66-136">標頭</span><span class="sxs-lookup"><span data-stu-id="2bf66-136">Header</span></span><br/>  | <dl> <span data-ttu-id="2bf66-137"><dt>D3dx9math。h</dt></span><span class="sxs-lookup"><span data-stu-id="2bf66-137"><dt>D3dx9math.h</dt></span></span> </dl> |
| <span data-ttu-id="2bf66-138">程式庫</span><span class="sxs-lookup"><span data-stu-id="2bf66-138">Library</span></span><br/> | <dl> <span data-ttu-id="2bf66-139"><dt>D3dx9 .lib</dt></span><span class="sxs-lookup"><span data-stu-id="2bf66-139"><dt>D3dx9.lib</dt></span></span> </dl>   |



## <a name="see-also"></a><span data-ttu-id="2bf66-140">另請參閱</span><span class="sxs-lookup"><span data-stu-id="2bf66-140">See also</span></span>

<dl> <dt>

[<span data-ttu-id="2bf66-141">數學函數</span><span class="sxs-lookup"><span data-stu-id="2bf66-141">Math Functions</span></span>](dx9-graphics-reference-d3dx-functions-math.md)
</dt> <dt>

[<span data-ttu-id="2bf66-142">預先計算 Radiance Transfer (Direct3D 9) </span><span class="sxs-lookup"><span data-stu-id="2bf66-142">Precomputed Radiance Transfer (Direct3D 9)</span></span>](precomputed-radiance-transfer.md)
</dt> </dl>

 

 
