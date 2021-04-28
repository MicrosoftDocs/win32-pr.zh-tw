---
description: D3DXSHAdd 函式 (D3DX10) -新增兩個球面調和 (SH) 向量;換句話說，不悅 \[ i \] = pA \[ i \] + pB \[ i \] 。
ms.assetid: dbfea12b-c110-42a7-84b6-0dff3d958032
title: 'D3DXSHAdd 函式 (D3DX10) '
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
- D3DX10.lib
- D3DX10.dll
ms.openlocfilehash: 8d39940fef4ad611ea530d95efea29c74266d22a
ms.sourcegitcommit: 95685061d5b0333bbf9e6ebd208dde8190f97005
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 04/28/2021
ms.locfileid: "108108656"
---
# <a name="d3dxshadd-function-d3dx10h"></a><span data-ttu-id="2e729-103">D3DXSHAdd 函式 (D3DX10) </span><span class="sxs-lookup"><span data-stu-id="2e729-103">D3DXSHAdd function (D3DX10.h)</span></span>

<span data-ttu-id="2e729-104">將兩個球面調和新增 (SH) 向量;換句話說，不悅 \[ i \] = pA \[ i \] + pB \[ i \] 。</span><span class="sxs-lookup"><span data-stu-id="2e729-104">Adds two spherical harmonic (SH) vectors; in other words, pOut\[i\] = pA\[i\] + pB\[i\].</span></span>

## <a name="syntax"></a><span data-ttu-id="2e729-105">語法</span><span class="sxs-lookup"><span data-stu-id="2e729-105">Syntax</span></span>


```C++
FLOAT* D3DXSHAdd(
  _In_       FLOAT *pOut,
  _In_       UINT  Order,
  _In_ const FLOAT *pA,
  _In_ const FLOAT *pB
);
```



## <a name="parameters"></a><span data-ttu-id="2e729-106">參數</span><span class="sxs-lookup"><span data-stu-id="2e729-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="2e729-107">*不悅* \[在\]</span><span class="sxs-lookup"><span data-stu-id="2e729-107">*pOut* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="2e729-108">類型： **[ **FLOAT**](../winprog/windows-data-types.md)\***</span><span class="sxs-lookup"><span data-stu-id="2e729-108">Type: **[**FLOAT**](../winprog/windows-data-types.md)\***</span></span>

<span data-ttu-id="2e729-109">SH 輸出係數的指標。</span><span class="sxs-lookup"><span data-stu-id="2e729-109">Pointer to SH output coefficients.</span></span> <span data-ttu-id="2e729-110">評估會產生順序²係數。</span><span class="sxs-lookup"><span data-stu-id="2e729-110">The evaluation generates Order² coefficients.</span></span> <span data-ttu-id="2e729-111">請參閱＜備註＞。</span><span class="sxs-lookup"><span data-stu-id="2e729-111">See Remarks.</span></span>

</dd> <dt>

<span data-ttu-id="2e729-112">*訂單* \[在\]</span><span class="sxs-lookup"><span data-stu-id="2e729-112">*Order* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="2e729-113">類型： **[ **UINT**](../winprog/windows-data-types.md)**</span><span class="sxs-lookup"><span data-stu-id="2e729-113">Type: **[**UINT**](../winprog/windows-data-types.md)**</span></span>

<span data-ttu-id="2e729-114">SH 評估的順序。</span><span class="sxs-lookup"><span data-stu-id="2e729-114">Order of the SH evaluation.</span></span> <span data-ttu-id="2e729-115">必須在 D3DXSH \_ MINORDER 到 D3DXSH \_ MAXORDER （含）的範圍內。</span><span class="sxs-lookup"><span data-stu-id="2e729-115">Must be in the range of D3DXSH\_MINORDER to D3DXSH\_MAXORDER, inclusive.</span></span> <span data-ttu-id="2e729-116">評估會產生順序²係數。</span><span class="sxs-lookup"><span data-stu-id="2e729-116">The evaluation generates Order² coefficients.</span></span> <span data-ttu-id="2e729-117">評估的程度是順序-1。</span><span class="sxs-lookup"><span data-stu-id="2e729-117">The degree of the evaluation is Order - 1.</span></span>

</dd> <dt>

<span data-ttu-id="2e729-118">*pA* \[在\]</span><span class="sxs-lookup"><span data-stu-id="2e729-118">*pA* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="2e729-119">Type： **Const [**FLOAT**](../winprog/windows-data-types.md) \***</span><span class="sxs-lookup"><span data-stu-id="2e729-119">Type: **const [**FLOAT**](../winprog/windows-data-types.md)\***</span></span>

<span data-ttu-id="2e729-120">第一個 SH 向量的指標。</span><span class="sxs-lookup"><span data-stu-id="2e729-120">Pointer to the first SH vector.</span></span>

</dd> <dt>

<span data-ttu-id="2e729-121">*pB* \[在\]</span><span class="sxs-lookup"><span data-stu-id="2e729-121">*pB* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="2e729-122">Type： **Const [**FLOAT**](../winprog/windows-data-types.md) \***</span><span class="sxs-lookup"><span data-stu-id="2e729-122">Type: **const [**FLOAT**](../winprog/windows-data-types.md)\***</span></span>

<span data-ttu-id="2e729-123">第二個 SH 向量的指標。</span><span class="sxs-lookup"><span data-stu-id="2e729-123">Pointer to the second SH vector.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="2e729-124">傳回值</span><span class="sxs-lookup"><span data-stu-id="2e729-124">Return value</span></span>

<span data-ttu-id="2e729-125">類型： **[ **FLOAT**](../winprog/windows-data-types.md)\***</span><span class="sxs-lookup"><span data-stu-id="2e729-125">Type: **[**FLOAT**](../winprog/windows-data-types.md)\***</span></span>

<span data-ttu-id="2e729-126">SH 輸出係數的指標。</span><span class="sxs-lookup"><span data-stu-id="2e729-126">Pointer to SH output coefficients.</span></span>

## <a name="remarks"></a><span data-ttu-id="2e729-127">備註</span><span class="sxs-lookup"><span data-stu-id="2e729-127">Remarks</span></span>

<span data-ttu-id="2e729-128">基礎函數 Ylm 的每個係數都會儲存在記憶體位置 l ² + m + l，其中：</span><span class="sxs-lookup"><span data-stu-id="2e729-128">Each coefficient of the basis function Yₗₘ is stored at memory location l² + m + l, where:</span></span>

-   <span data-ttu-id="2e729-129">l 是基礎函數的程度。</span><span class="sxs-lookup"><span data-stu-id="2e729-129">l is the degree of the basis function.</span></span>
-   <span data-ttu-id="2e729-130">m 是指定 l 值的基礎函數索引，範圍從-l 到 l （含）。</span><span class="sxs-lookup"><span data-stu-id="2e729-130">m is the basis function index for the given l value and ranges from -l to l, inclusive.</span></span>

## <a name="requirements"></a><span data-ttu-id="2e729-131">規格需求</span><span class="sxs-lookup"><span data-stu-id="2e729-131">Requirements</span></span>



| <span data-ttu-id="2e729-132">需求</span><span class="sxs-lookup"><span data-stu-id="2e729-132">Requirement</span></span> | <span data-ttu-id="2e729-133">值</span><span class="sxs-lookup"><span data-stu-id="2e729-133">Value</span></span> |
|--------------------|---------------------------------------------------------------------------------------|
| <span data-ttu-id="2e729-134">標頭</span><span class="sxs-lookup"><span data-stu-id="2e729-134">Header</span></span><br/>  | <dl> <span data-ttu-id="2e729-135"><dt>D3DX10。h</dt></span><span class="sxs-lookup"><span data-stu-id="2e729-135"><dt>D3DX10.h</dt></span></span> </dl>   |
| <span data-ttu-id="2e729-136">程式庫</span><span class="sxs-lookup"><span data-stu-id="2e729-136">Library</span></span><br/> | <dl> <span data-ttu-id="2e729-137"><dt>D3DX10 .lib</dt></span><span class="sxs-lookup"><span data-stu-id="2e729-137"><dt>D3DX10.lib</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="2e729-138">另請參閱</span><span class="sxs-lookup"><span data-stu-id="2e729-138">See also</span></span>

<dl> <dt>

[<span data-ttu-id="2e729-139">數學函數</span><span class="sxs-lookup"><span data-stu-id="2e729-139">Math Functions</span></span>](d3d10-graphics-reference-d3dx10-functions-math.md)
</dt> </dl>

 

 
