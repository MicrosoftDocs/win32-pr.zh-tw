---
description: D3DXSHScale 函式 (D3dx9math) -調整球形調和 (SH) 向量;換句話說，不悅 \[ i \] = pA \[ i \] \* 尺規。
ms.assetid: e7b08b55-e2e7-4f13-bbee-10b844d3ef91
title: 'D3DXSHScale 函式 (D3dx9math) '
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- D3DXSHScale
api_type:
- LibDef
api_location:
- d3dx9.lib
- d3dx9.dll
ms.openlocfilehash: 6a91c3ea1cb49c4c501ab847cb63fe8a39d66665
ms.sourcegitcommit: 95685061d5b0333bbf9e6ebd208dde8190f97005
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 04/28/2021
ms.locfileid: "108093856"
---
# <a name="d3dxshscale-function-d3dx9mathh"></a><span data-ttu-id="0bba0-103">D3DXSHScale 函式 (D3dx9math) </span><span class="sxs-lookup"><span data-stu-id="0bba0-103">D3DXSHScale function (D3dx9math.h)</span></span>

<span data-ttu-id="0bba0-104">調整球形調和 (SH) 向量;換句話說，不悅 \[ i \] = pA \[ i \] \* 尺規。</span><span class="sxs-lookup"><span data-stu-id="0bba0-104">Scales a spherical harmonic (SH) vector; in other words, pOut\[i\] = pA\[i\]\*Scale.</span></span>

## <a name="syntax"></a><span data-ttu-id="0bba0-105">語法</span><span class="sxs-lookup"><span data-stu-id="0bba0-105">Syntax</span></span>


```C++
FLOAT* D3DXSHScale(
  _Out_       FLOAT *pOut,
  _In_        UINT  Order,
  _In_  const FLOAT *pIn,
  _In_  const FLOAT *Scale
);
```



## <a name="parameters"></a><span data-ttu-id="0bba0-106">參數</span><span class="sxs-lookup"><span data-stu-id="0bba0-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="0bba0-107">*不悅* \[擴展\]</span><span class="sxs-lookup"><span data-stu-id="0bba0-107">*pOut* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="0bba0-108">類型： **[ **FLOAT**](../winprog/windows-data-types.md)\***</span><span class="sxs-lookup"><span data-stu-id="0bba0-108">Type: **[**FLOAT**](../winprog/windows-data-types.md)\***</span></span>

<span data-ttu-id="0bba0-109">球面調和 (SH) 輸出係數的指標。</span><span class="sxs-lookup"><span data-stu-id="0bba0-109">Pointer to Spherical harmonic (SH) output coefficients.</span></span> <span data-ttu-id="0bba0-110">評估會產生順序²係數。</span><span class="sxs-lookup"><span data-stu-id="0bba0-110">The evaluation generates Order² coefficients.</span></span> <span data-ttu-id="0bba0-111">請參閱＜備註＞。</span><span class="sxs-lookup"><span data-stu-id="0bba0-111">See Remarks.</span></span>

</dd> <dt>

<span data-ttu-id="0bba0-112">*訂單* \[在\]</span><span class="sxs-lookup"><span data-stu-id="0bba0-112">*Order* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="0bba0-113">類型： **[ **UINT**](../winprog/windows-data-types.md)**</span><span class="sxs-lookup"><span data-stu-id="0bba0-113">Type: **[**UINT**](../winprog/windows-data-types.md)**</span></span>

<span data-ttu-id="0bba0-114">SH 評估的順序。</span><span class="sxs-lookup"><span data-stu-id="0bba0-114">Order of the SH evaluation.</span></span> <span data-ttu-id="0bba0-115">必須在 [D3DXSH \_ MINORDER](other-d3dx-constants.md) 到 D3DXSH \_ MAXORDER （含）的範圍內。</span><span class="sxs-lookup"><span data-stu-id="0bba0-115">Must be in the range of [D3DXSH\_MINORDER](other-d3dx-constants.md) to D3DXSH\_MAXORDER, inclusive.</span></span> <span data-ttu-id="0bba0-116">評估會產生順序²係數。</span><span class="sxs-lookup"><span data-stu-id="0bba0-116">The evaluation generates Order² coefficients.</span></span> <span data-ttu-id="0bba0-117">評估的程度是順序-1。</span><span class="sxs-lookup"><span data-stu-id="0bba0-117">The degree of the evaluation is Order - 1.</span></span>

</dd> <dt>

<span data-ttu-id="0bba0-118">*pIn* \[在\]</span><span class="sxs-lookup"><span data-stu-id="0bba0-118">*pIn* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="0bba0-119">Type： **Const [**FLOAT**](../winprog/windows-data-types.md) \***</span><span class="sxs-lookup"><span data-stu-id="0bba0-119">Type: **const [**FLOAT**](../winprog/windows-data-types.md)\***</span></span>

<span data-ttu-id="0bba0-120">要調整的 SH 向量指標。</span><span class="sxs-lookup"><span data-stu-id="0bba0-120">Pointer to the SH vector to scale.</span></span>

</dd> <dt>

<span data-ttu-id="0bba0-121">*調整規模* \[在\]</span><span class="sxs-lookup"><span data-stu-id="0bba0-121">*Scale* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="0bba0-122">Type： **Const [**FLOAT**](../winprog/windows-data-types.md) \***</span><span class="sxs-lookup"><span data-stu-id="0bba0-122">Type: **const [**FLOAT**](../winprog/windows-data-types.md)\***</span></span>

<span data-ttu-id="0bba0-123">刻度值的指標。</span><span class="sxs-lookup"><span data-stu-id="0bba0-123">Pointer to the scale value.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="0bba0-124">傳回值</span><span class="sxs-lookup"><span data-stu-id="0bba0-124">Return value</span></span>

<span data-ttu-id="0bba0-125">類型： **[ **FLOAT**](../winprog/windows-data-types.md)\***</span><span class="sxs-lookup"><span data-stu-id="0bba0-125">Type: **[**FLOAT**](../winprog/windows-data-types.md)\***</span></span>

<span data-ttu-id="0bba0-126">SH 輸出係數的指標。</span><span class="sxs-lookup"><span data-stu-id="0bba0-126">Pointer to SH output coefficients.</span></span>

## <a name="remarks"></a><span data-ttu-id="0bba0-127">備註</span><span class="sxs-lookup"><span data-stu-id="0bba0-127">Remarks</span></span>

<span data-ttu-id="0bba0-128">基礎函數 Ylm 的每個係數都會儲存在記憶體位置 l ² + m + l，其中：</span><span class="sxs-lookup"><span data-stu-id="0bba0-128">Each coefficient of the basis function Yₗₘ is stored at memory location l² + m + l, where:</span></span>

-   <span data-ttu-id="0bba0-129">l 是基礎函數的程度。</span><span class="sxs-lookup"><span data-stu-id="0bba0-129">l is the degree of the basis function.</span></span>
-   <span data-ttu-id="0bba0-130">m 是指定 l 值的基礎函數索引，範圍從-l 到 l （含）。</span><span class="sxs-lookup"><span data-stu-id="0bba0-130">m is the basis function index for the given l value and ranges from -l to l, inclusive.</span></span>

## <a name="requirements"></a><span data-ttu-id="0bba0-131">規格需求</span><span class="sxs-lookup"><span data-stu-id="0bba0-131">Requirements</span></span>



| <span data-ttu-id="0bba0-132">需求</span><span class="sxs-lookup"><span data-stu-id="0bba0-132">Requirement</span></span> | <span data-ttu-id="0bba0-133">值</span><span class="sxs-lookup"><span data-stu-id="0bba0-133">Value</span></span> |
|--------------------|----------------------------------------------------------------------------------------|
| <span data-ttu-id="0bba0-134">標頭</span><span class="sxs-lookup"><span data-stu-id="0bba0-134">Header</span></span><br/>  | <dl> <span data-ttu-id="0bba0-135"><dt>D3dx9math。h</dt></span><span class="sxs-lookup"><span data-stu-id="0bba0-135"><dt>D3dx9math.h</dt></span></span> </dl> |
| <span data-ttu-id="0bba0-136">程式庫</span><span class="sxs-lookup"><span data-stu-id="0bba0-136">Library</span></span><br/> | <dl> <span data-ttu-id="0bba0-137"><dt>D3dx9 .lib</dt></span><span class="sxs-lookup"><span data-stu-id="0bba0-137"><dt>D3dx9.lib</dt></span></span> </dl>   |



## <a name="see-also"></a><span data-ttu-id="0bba0-138">另請參閱</span><span class="sxs-lookup"><span data-stu-id="0bba0-138">See also</span></span>

<dl> <dt>

[<span data-ttu-id="0bba0-139">數學函數</span><span class="sxs-lookup"><span data-stu-id="0bba0-139">Math Functions</span></span>](dx9-graphics-reference-d3dx-functions-math.md)
</dt> <dt>

[<span data-ttu-id="0bba0-140">預先計算 Radiance Transfer (Direct3D 9) </span><span class="sxs-lookup"><span data-stu-id="0bba0-140">Precomputed Radiance Transfer (Direct3D 9)</span></span>](precomputed-radiance-transfer.md)
</dt> </dl>

 

 
