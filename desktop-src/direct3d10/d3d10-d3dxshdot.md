---
description: 計算兩個球形調和 (SH) 向量的點乘積。
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
ms.openlocfilehash: 20f0896168dae0e2a779625c683777938c8e2df2
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 03/15/2021
ms.locfileid: "106988205"
---
# <a name="d3dxshdot-function-d3dx10h"></a><span data-ttu-id="36f95-103">D3DXSHDot 函式 (D3DX10) </span><span class="sxs-lookup"><span data-stu-id="36f95-103">D3DXSHDot function (D3DX10.h)</span></span>

<span data-ttu-id="36f95-104">計算兩個球形調和 (SH) 向量的點乘積。</span><span class="sxs-lookup"><span data-stu-id="36f95-104">Computes the dot product of two spherical harmonic (SH) vectors.</span></span>

## <a name="syntax"></a><span data-ttu-id="36f95-105">語法</span><span class="sxs-lookup"><span data-stu-id="36f95-105">Syntax</span></span>


```C++
FLOAT D3DXSHDot(
  _In_       UINT  Order,
  _In_ const FLOAT *pA,
  _In_ const FLOAT *pB
);
```



## <a name="parameters"></a><span data-ttu-id="36f95-106">參數</span><span class="sxs-lookup"><span data-stu-id="36f95-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="36f95-107">*訂單* \[在\]</span><span class="sxs-lookup"><span data-stu-id="36f95-107">*Order* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="36f95-108">類型： **[ **UINT**](../winprog/windows-data-types.md)**</span><span class="sxs-lookup"><span data-stu-id="36f95-108">Type: **[**UINT**](../winprog/windows-data-types.md)**</span></span>

<span data-ttu-id="36f95-109">球形調和 (SH) 評估的順序。</span><span class="sxs-lookup"><span data-stu-id="36f95-109">Order of the spherical harmonic (SH) evaluation.</span></span> <span data-ttu-id="36f95-110">必須在 D3DXSH \_ MINORDER 到 D3DXSH \_ MAXORDER （含）的範圍內。</span><span class="sxs-lookup"><span data-stu-id="36f95-110">Must be in the range of D3DXSH\_MINORDER to D3DXSH\_MAXORDER, inclusive.</span></span> <span data-ttu-id="36f95-111">評估會產生順序²係數。</span><span class="sxs-lookup"><span data-stu-id="36f95-111">The evaluation generates Order² coefficients.</span></span> <span data-ttu-id="36f95-112">評估的程度是順序-1。</span><span class="sxs-lookup"><span data-stu-id="36f95-112">The degree of the evaluation is Order - 1.</span></span>

</dd> <dt>

<span data-ttu-id="36f95-113">*pA* \[在\]</span><span class="sxs-lookup"><span data-stu-id="36f95-113">*pA* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="36f95-114">Type： **Const [**FLOAT**](../winprog/windows-data-types.md) \***</span><span class="sxs-lookup"><span data-stu-id="36f95-114">Type: **const [**FLOAT**](../winprog/windows-data-types.md)\***</span></span>

<span data-ttu-id="36f95-115">第一個 SH 向量的指標。</span><span class="sxs-lookup"><span data-stu-id="36f95-115">Pointer to the first SH vector.</span></span>

</dd> <dt>

<span data-ttu-id="36f95-116">*pB* \[在\]</span><span class="sxs-lookup"><span data-stu-id="36f95-116">*pB* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="36f95-117">Type： **Const [**FLOAT**](../winprog/windows-data-types.md) \***</span><span class="sxs-lookup"><span data-stu-id="36f95-117">Type: **const [**FLOAT**](../winprog/windows-data-types.md)\***</span></span>

<span data-ttu-id="36f95-118">第二個 SH 向量的指標。</span><span class="sxs-lookup"><span data-stu-id="36f95-118">Pointer to the second SH vector.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="36f95-119">傳回值</span><span class="sxs-lookup"><span data-stu-id="36f95-119">Return value</span></span>

<span data-ttu-id="36f95-120">類型： **[ **FLOAT**](../winprog/windows-data-types.md)**</span><span class="sxs-lookup"><span data-stu-id="36f95-120">Type: **[**FLOAT**](../winprog/windows-data-types.md)**</span></span>

<span data-ttu-id="36f95-121">SH 輸出係數。</span><span class="sxs-lookup"><span data-stu-id="36f95-121">SH output coefficients.</span></span>

## <a name="remarks"></a><span data-ttu-id="36f95-122">備註</span><span class="sxs-lookup"><span data-stu-id="36f95-122">Remarks</span></span>

<span data-ttu-id="36f95-123">基礎函數 Ylm 的每個係數都會儲存在記憶體位置 l ² + m + l，其中：</span><span class="sxs-lookup"><span data-stu-id="36f95-123">Each coefficient of the basis function Yₗₘ is stored at memory location l² + m + l, where:</span></span>

-   <span data-ttu-id="36f95-124">l 是基礎函數的程度。</span><span class="sxs-lookup"><span data-stu-id="36f95-124">l is the degree of the basis function.</span></span>
-   <span data-ttu-id="36f95-125">m 是指定 l 值的基礎函數索引，範圍從-l 到 l （含）。</span><span class="sxs-lookup"><span data-stu-id="36f95-125">m is the basis function index for the given l value and ranges from -l to l, inclusive.</span></span>

## <a name="requirements"></a><span data-ttu-id="36f95-126">規格需求</span><span class="sxs-lookup"><span data-stu-id="36f95-126">Requirements</span></span>



| <span data-ttu-id="36f95-127">需求</span><span class="sxs-lookup"><span data-stu-id="36f95-127">Requirement</span></span> | <span data-ttu-id="36f95-128">值</span><span class="sxs-lookup"><span data-stu-id="36f95-128">Value</span></span> |
|--------------------|---------------------------------------------------------------------------------------|
| <span data-ttu-id="36f95-129">標頭</span><span class="sxs-lookup"><span data-stu-id="36f95-129">Header</span></span><br/>  | <dl> <span data-ttu-id="36f95-130"><dt>D3DX10。h</dt></span><span class="sxs-lookup"><span data-stu-id="36f95-130"><dt>D3DX10.h</dt></span></span> </dl>   |
| <span data-ttu-id="36f95-131">程式庫</span><span class="sxs-lookup"><span data-stu-id="36f95-131">Library</span></span><br/> | <dl> <span data-ttu-id="36f95-132"><dt>D3DX10 .lib</dt></span><span class="sxs-lookup"><span data-stu-id="36f95-132"><dt>D3DX10.lib</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="36f95-133">另請參閱</span><span class="sxs-lookup"><span data-stu-id="36f95-133">See also</span></span>

<dl> <dt>

[<span data-ttu-id="36f95-134">數學函數</span><span class="sxs-lookup"><span data-stu-id="36f95-134">Math Functions</span></span>](d3d10-graphics-reference-d3dx10-functions-math.md)
</dt> </dl>

 

 
