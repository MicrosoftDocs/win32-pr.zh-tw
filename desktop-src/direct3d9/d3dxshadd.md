---
description: D3DXSHAdd 函式 (D3dx9math) -新增兩個球面調和 (SH) 向量;換句話說，不悅 \[ i \] = pA \[ i \] + pB \[ i \] 。
ms.assetid: 12775c90-ed9d-4931-a449-2571816dd079
title: 'D3DXSHAdd 函式 (D3dx9math) '
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- D3DXSHAdd
api_type:
- LibDef
api_location:
- d3dx9.lib
- d3dx9.dll
ms.openlocfilehash: 7333d1803b9f7ea7b056ff78ffd053bd6086184b
ms.sourcegitcommit: 95685061d5b0333bbf9e6ebd208dde8190f97005
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 04/28/2021
ms.locfileid: "108117956"
---
# <a name="d3dxshadd-function-d3dx9mathh"></a><span data-ttu-id="3206e-103">D3DXSHAdd 函式 (D3dx9math) </span><span class="sxs-lookup"><span data-stu-id="3206e-103">D3DXSHAdd function (D3dx9math.h)</span></span>

<span data-ttu-id="3206e-104">將兩個球面調和新增 (SH) 向量;換句話說，不悅 \[ i \] = pA \[ i \] + pB \[ i \] 。</span><span class="sxs-lookup"><span data-stu-id="3206e-104">Adds two spherical harmonic (SH) vectors; in other words, pOut\[i\] = pA\[i\] + pB\[i\].</span></span>

## <a name="syntax"></a><span data-ttu-id="3206e-105">語法</span><span class="sxs-lookup"><span data-stu-id="3206e-105">Syntax</span></span>


```C++
FLOAT* D3DXSHAdd(
  _Out_       FLOAT *pOut,
  _In_        UINT  Order,
  _In_  const FLOAT *pA,
  _In_  const FLOAT *pB
);
```



## <a name="parameters"></a><span data-ttu-id="3206e-106">參數</span><span class="sxs-lookup"><span data-stu-id="3206e-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="3206e-107">*不悅* \[擴展\]</span><span class="sxs-lookup"><span data-stu-id="3206e-107">*pOut* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="3206e-108">類型： **[ **FLOAT**](../winprog/windows-data-types.md)\***</span><span class="sxs-lookup"><span data-stu-id="3206e-108">Type: **[**FLOAT**](../winprog/windows-data-types.md)\***</span></span>

<span data-ttu-id="3206e-109">SH 輸出係數的指標。</span><span class="sxs-lookup"><span data-stu-id="3206e-109">Pointer to SH output coefficients.</span></span> <span data-ttu-id="3206e-110">評估會產生順序²係數。</span><span class="sxs-lookup"><span data-stu-id="3206e-110">The evaluation generates Order² coefficients.</span></span> <span data-ttu-id="3206e-111">請參閱＜備註＞。</span><span class="sxs-lookup"><span data-stu-id="3206e-111">See Remarks.</span></span>

</dd> <dt>

<span data-ttu-id="3206e-112">*訂單* \[在\]</span><span class="sxs-lookup"><span data-stu-id="3206e-112">*Order* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="3206e-113">類型： **[ **UINT**](../winprog/windows-data-types.md)**</span><span class="sxs-lookup"><span data-stu-id="3206e-113">Type: **[**UINT**](../winprog/windows-data-types.md)**</span></span>

<span data-ttu-id="3206e-114">SH 評估的順序。</span><span class="sxs-lookup"><span data-stu-id="3206e-114">Order of the SH evaluation.</span></span> <span data-ttu-id="3206e-115">必須在 [D3DXSH \_ MINORDER](other-d3dx-constants.md) 到 D3DXSH \_ MAXORDER （含）的範圍內。</span><span class="sxs-lookup"><span data-stu-id="3206e-115">Must be in the range of [D3DXSH\_MINORDER](other-d3dx-constants.md) to D3DXSH\_MAXORDER, inclusive.</span></span> <span data-ttu-id="3206e-116">評估會產生順序²係數。</span><span class="sxs-lookup"><span data-stu-id="3206e-116">The evaluation generates Order² coefficients.</span></span> <span data-ttu-id="3206e-117">評估的程度是順序-1。</span><span class="sxs-lookup"><span data-stu-id="3206e-117">The degree of the evaluation is Order - 1.</span></span>

</dd> <dt>

<span data-ttu-id="3206e-118">*pA* \[在\]</span><span class="sxs-lookup"><span data-stu-id="3206e-118">*pA* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="3206e-119">Type： **Const [**FLOAT**](../winprog/windows-data-types.md) \***</span><span class="sxs-lookup"><span data-stu-id="3206e-119">Type: **const [**FLOAT**](../winprog/windows-data-types.md)\***</span></span>

<span data-ttu-id="3206e-120">第一個 SH 向量的指標。</span><span class="sxs-lookup"><span data-stu-id="3206e-120">Pointer to the first SH vector.</span></span>

</dd> <dt>

<span data-ttu-id="3206e-121">*pB* \[在\]</span><span class="sxs-lookup"><span data-stu-id="3206e-121">*pB* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="3206e-122">Type： **Const [**FLOAT**](../winprog/windows-data-types.md) \***</span><span class="sxs-lookup"><span data-stu-id="3206e-122">Type: **const [**FLOAT**](../winprog/windows-data-types.md)\***</span></span>

<span data-ttu-id="3206e-123">第二個 SH 向量的指標。</span><span class="sxs-lookup"><span data-stu-id="3206e-123">Pointer to the second SH vector.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="3206e-124">傳回值</span><span class="sxs-lookup"><span data-stu-id="3206e-124">Return value</span></span>

<span data-ttu-id="3206e-125">類型： **[ **FLOAT**](../winprog/windows-data-types.md)\***</span><span class="sxs-lookup"><span data-stu-id="3206e-125">Type: **[**FLOAT**](../winprog/windows-data-types.md)\***</span></span>

<span data-ttu-id="3206e-126">SH 輸出係數的指標。</span><span class="sxs-lookup"><span data-stu-id="3206e-126">Pointer to SH output coefficients.</span></span>

## <a name="remarks"></a><span data-ttu-id="3206e-127">備註</span><span class="sxs-lookup"><span data-stu-id="3206e-127">Remarks</span></span>

<span data-ttu-id="3206e-128">基礎函數 Ylm 的每個係數都會儲存在記憶體位置 l ² + m + l，其中：</span><span class="sxs-lookup"><span data-stu-id="3206e-128">Each coefficient of the basis function Yₗₘ is stored at memory location l² + m + l, where:</span></span>

-   <span data-ttu-id="3206e-129">l 是基礎函數的程度。</span><span class="sxs-lookup"><span data-stu-id="3206e-129">l is the degree of the basis function.</span></span>
-   <span data-ttu-id="3206e-130">m 是指定 l 值的基礎函數索引，範圍從-l 到 l （含）。</span><span class="sxs-lookup"><span data-stu-id="3206e-130">m is the basis function index for the given l value and ranges from -l to l, inclusive.</span></span>

## <a name="requirements"></a><span data-ttu-id="3206e-131">規格需求</span><span class="sxs-lookup"><span data-stu-id="3206e-131">Requirements</span></span>



| <span data-ttu-id="3206e-132">需求</span><span class="sxs-lookup"><span data-stu-id="3206e-132">Requirement</span></span> | <span data-ttu-id="3206e-133">值</span><span class="sxs-lookup"><span data-stu-id="3206e-133">Value</span></span> |
|--------------------|----------------------------------------------------------------------------------------|
| <span data-ttu-id="3206e-134">標頭</span><span class="sxs-lookup"><span data-stu-id="3206e-134">Header</span></span><br/>  | <dl> <span data-ttu-id="3206e-135"><dt>D3dx9math。h</dt></span><span class="sxs-lookup"><span data-stu-id="3206e-135"><dt>D3dx9math.h</dt></span></span> </dl> |
| <span data-ttu-id="3206e-136">程式庫</span><span class="sxs-lookup"><span data-stu-id="3206e-136">Library</span></span><br/> | <dl> <span data-ttu-id="3206e-137"><dt>D3dx9 .lib</dt></span><span class="sxs-lookup"><span data-stu-id="3206e-137"><dt>D3dx9.lib</dt></span></span> </dl>   |



## <a name="see-also"></a><span data-ttu-id="3206e-138">另請參閱</span><span class="sxs-lookup"><span data-stu-id="3206e-138">See also</span></span>

<dl> <dt>

[<span data-ttu-id="3206e-139">數學函數</span><span class="sxs-lookup"><span data-stu-id="3206e-139">Math Functions</span></span>](dx9-graphics-reference-d3dx-functions-math.md)
</dt> <dt>

[<span data-ttu-id="3206e-140">預先計算 Radiance Transfer (Direct3D 9) </span><span class="sxs-lookup"><span data-stu-id="3206e-140">Precomputed Radiance Transfer (Direct3D 9)</span></span>](precomputed-radiance-transfer.md)
</dt> </dl>

 

 
