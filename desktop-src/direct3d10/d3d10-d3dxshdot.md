---
description: D3DXSHDot 函數 (D3DX10) -計算兩個球面調和 (SH) 向量的點乘積。
ms.assetid: 30f0e858-4c31-4b25-9979-754d996a7d48
title: 'D3DXSHDot 函式 (D3DX10) '
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- D3DXSHDot
api_type:
- LibDef
api_location:
- D3DX10.lib
- D3DX10.dll
ms.openlocfilehash: 3ea3e839ff7a5fc038cf40a6402db4a358da8b39
ms.sourcegitcommit: 95685061d5b0333bbf9e6ebd208dde8190f97005
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 04/28/2021
ms.locfileid: "108108626"
---
# <a name="d3dxshdot-function-d3dx10h"></a><span data-ttu-id="b6dd4-103">D3DXSHDot 函式 (D3DX10) </span><span class="sxs-lookup"><span data-stu-id="b6dd4-103">D3DXSHDot function (D3DX10.h)</span></span>

<span data-ttu-id="b6dd4-104">計算兩個球形調和 (SH) 向量的點乘積。</span><span class="sxs-lookup"><span data-stu-id="b6dd4-104">Computes the dot product of two spherical harmonic (SH) vectors.</span></span>

## <a name="syntax"></a><span data-ttu-id="b6dd4-105">語法</span><span class="sxs-lookup"><span data-stu-id="b6dd4-105">Syntax</span></span>


```C++
FLOAT D3DXSHDot(
  _In_       UINT  Order,
  _In_ const FLOAT *pA,
  _In_ const FLOAT *pB
);
```



## <a name="parameters"></a><span data-ttu-id="b6dd4-106">參數</span><span class="sxs-lookup"><span data-stu-id="b6dd4-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="b6dd4-107">*訂單* \[在\]</span><span class="sxs-lookup"><span data-stu-id="b6dd4-107">*Order* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="b6dd4-108">類型： **[ **UINT**](../winprog/windows-data-types.md)**</span><span class="sxs-lookup"><span data-stu-id="b6dd4-108">Type: **[**UINT**](../winprog/windows-data-types.md)**</span></span>

<span data-ttu-id="b6dd4-109">球形調和 (SH) 評估的順序。</span><span class="sxs-lookup"><span data-stu-id="b6dd4-109">Order of the spherical harmonic (SH) evaluation.</span></span> <span data-ttu-id="b6dd4-110">必須在 D3DXSH \_ MINORDER 到 D3DXSH \_ MAXORDER （含）的範圍內。</span><span class="sxs-lookup"><span data-stu-id="b6dd4-110">Must be in the range of D3DXSH\_MINORDER to D3DXSH\_MAXORDER, inclusive.</span></span> <span data-ttu-id="b6dd4-111">評估會產生順序²係數。</span><span class="sxs-lookup"><span data-stu-id="b6dd4-111">The evaluation generates Order² coefficients.</span></span> <span data-ttu-id="b6dd4-112">評估的程度是順序-1。</span><span class="sxs-lookup"><span data-stu-id="b6dd4-112">The degree of the evaluation is Order - 1.</span></span>

</dd> <dt>

<span data-ttu-id="b6dd4-113">*pA* \[在\]</span><span class="sxs-lookup"><span data-stu-id="b6dd4-113">*pA* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="b6dd4-114">Type： **Const [**FLOAT**](../winprog/windows-data-types.md) \***</span><span class="sxs-lookup"><span data-stu-id="b6dd4-114">Type: **const [**FLOAT**](../winprog/windows-data-types.md)\***</span></span>

<span data-ttu-id="b6dd4-115">第一個 SH 向量的指標。</span><span class="sxs-lookup"><span data-stu-id="b6dd4-115">Pointer to the first SH vector.</span></span>

</dd> <dt>

<span data-ttu-id="b6dd4-116">*pB* \[在\]</span><span class="sxs-lookup"><span data-stu-id="b6dd4-116">*pB* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="b6dd4-117">Type： **Const [**FLOAT**](../winprog/windows-data-types.md) \***</span><span class="sxs-lookup"><span data-stu-id="b6dd4-117">Type: **const [**FLOAT**](../winprog/windows-data-types.md)\***</span></span>

<span data-ttu-id="b6dd4-118">第二個 SH 向量的指標。</span><span class="sxs-lookup"><span data-stu-id="b6dd4-118">Pointer to the second SH vector.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="b6dd4-119">傳回值</span><span class="sxs-lookup"><span data-stu-id="b6dd4-119">Return value</span></span>

<span data-ttu-id="b6dd4-120">類型： **[ **FLOAT**](../winprog/windows-data-types.md)**</span><span class="sxs-lookup"><span data-stu-id="b6dd4-120">Type: **[**FLOAT**](../winprog/windows-data-types.md)**</span></span>

<span data-ttu-id="b6dd4-121">SH 輸出係數。</span><span class="sxs-lookup"><span data-stu-id="b6dd4-121">SH output coefficients.</span></span>

## <a name="remarks"></a><span data-ttu-id="b6dd4-122">備註</span><span class="sxs-lookup"><span data-stu-id="b6dd4-122">Remarks</span></span>

<span data-ttu-id="b6dd4-123">基礎函數 Ylm 的每個係數都會儲存在記憶體位置 l ² + m + l，其中：</span><span class="sxs-lookup"><span data-stu-id="b6dd4-123">Each coefficient of the basis function Yₗₘ is stored at memory location l² + m + l, where:</span></span>

-   <span data-ttu-id="b6dd4-124">l 是基礎函數的程度。</span><span class="sxs-lookup"><span data-stu-id="b6dd4-124">l is the degree of the basis function.</span></span>
-   <span data-ttu-id="b6dd4-125">m 是指定 l 值的基礎函數索引，範圍從-l 到 l （含）。</span><span class="sxs-lookup"><span data-stu-id="b6dd4-125">m is the basis function index for the given l value and ranges from -l to l, inclusive.</span></span>

## <a name="requirements"></a><span data-ttu-id="b6dd4-126">規格需求</span><span class="sxs-lookup"><span data-stu-id="b6dd4-126">Requirements</span></span>



| <span data-ttu-id="b6dd4-127">需求</span><span class="sxs-lookup"><span data-stu-id="b6dd4-127">Requirement</span></span> | <span data-ttu-id="b6dd4-128">值</span><span class="sxs-lookup"><span data-stu-id="b6dd4-128">Value</span></span> |
|--------------------|---------------------------------------------------------------------------------------|
| <span data-ttu-id="b6dd4-129">標頭</span><span class="sxs-lookup"><span data-stu-id="b6dd4-129">Header</span></span><br/>  | <dl> <span data-ttu-id="b6dd4-130"><dt>D3DX10。h</dt></span><span class="sxs-lookup"><span data-stu-id="b6dd4-130"><dt>D3DX10.h</dt></span></span> </dl>   |
| <span data-ttu-id="b6dd4-131">程式庫</span><span class="sxs-lookup"><span data-stu-id="b6dd4-131">Library</span></span><br/> | <dl> <span data-ttu-id="b6dd4-132"><dt>D3DX10 .lib</dt></span><span class="sxs-lookup"><span data-stu-id="b6dd4-132"><dt>D3DX10.lib</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="b6dd4-133">另請參閱</span><span class="sxs-lookup"><span data-stu-id="b6dd4-133">See also</span></span>

<dl> <dt>

[<span data-ttu-id="b6dd4-134">數學函數</span><span class="sxs-lookup"><span data-stu-id="b6dd4-134">Math Functions</span></span>](d3d10-graphics-reference-d3dx10-functions-math.md)
</dt> </dl>

 

 
