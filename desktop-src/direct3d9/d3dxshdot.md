---
description: 計算兩個球形調和 (SH) 向量的點乘積。
ms.assetid: 71b7480d-ddac-4b02-bca7-d9318823d03e
title: 'D3DXSHDot 函式 (D3dx9math) '
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
- d3dx9.lib
- d3dx9.dll
ms.openlocfilehash: a69ee929c889232cb29ff1b556dd08ab65a0d6d1
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 03/15/2021
ms.locfileid: "104386454"
---
# <a name="d3dxshdot-function-d3dx9mathh"></a><span data-ttu-id="27722-103">D3DXSHDot 函式 (D3dx9math) </span><span class="sxs-lookup"><span data-stu-id="27722-103">D3DXSHDot function (D3dx9math.h)</span></span>

<span data-ttu-id="27722-104">計算兩個球形調和 (SH) 向量的點乘積。</span><span class="sxs-lookup"><span data-stu-id="27722-104">Computes the dot product of two spherical harmonic (SH) vectors.</span></span>

## <a name="syntax"></a><span data-ttu-id="27722-105">語法</span><span class="sxs-lookup"><span data-stu-id="27722-105">Syntax</span></span>


```C++
FLOAT D3DXSHDot(
  _In_       UINT  Order,
  _In_ const FLOAT *pA,
  _In_ const FLOAT *pB
);
```



## <a name="parameters"></a><span data-ttu-id="27722-106">參數</span><span class="sxs-lookup"><span data-stu-id="27722-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="27722-107">*訂單* \[在\]</span><span class="sxs-lookup"><span data-stu-id="27722-107">*Order* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="27722-108">類型： **[ **UINT**](../winprog/windows-data-types.md)**</span><span class="sxs-lookup"><span data-stu-id="27722-108">Type: **[**UINT**](../winprog/windows-data-types.md)**</span></span>

<span data-ttu-id="27722-109">球形調和 (SH) 評估的順序。</span><span class="sxs-lookup"><span data-stu-id="27722-109">Order of the spherical harmonic (SH) evaluation.</span></span> <span data-ttu-id="27722-110">必須在 [D3DXSH \_ MINORDER](other-d3dx-constants.md) 到 D3DXSH \_ MAXORDER （含）的範圍內。</span><span class="sxs-lookup"><span data-stu-id="27722-110">Must be in the range of [D3DXSH\_MINORDER](other-d3dx-constants.md) to D3DXSH\_MAXORDER, inclusive.</span></span> <span data-ttu-id="27722-111">評估會產生順序²係數。</span><span class="sxs-lookup"><span data-stu-id="27722-111">The evaluation generates Order² coefficients.</span></span> <span data-ttu-id="27722-112">評估的程度是順序-1。</span><span class="sxs-lookup"><span data-stu-id="27722-112">The degree of the evaluation is Order - 1.</span></span>

</dd> <dt>

<span data-ttu-id="27722-113">*pA* \[在\]</span><span class="sxs-lookup"><span data-stu-id="27722-113">*pA* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="27722-114">Type： **Const [**FLOAT**](../winprog/windows-data-types.md) \***</span><span class="sxs-lookup"><span data-stu-id="27722-114">Type: **const [**FLOAT**](../winprog/windows-data-types.md)\***</span></span>

<span data-ttu-id="27722-115">第一個 SH 向量的指標。</span><span class="sxs-lookup"><span data-stu-id="27722-115">Pointer to the first SH vector.</span></span>

</dd> <dt>

<span data-ttu-id="27722-116">*pB* \[在\]</span><span class="sxs-lookup"><span data-stu-id="27722-116">*pB* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="27722-117">Type： **Const [**FLOAT**](../winprog/windows-data-types.md) \***</span><span class="sxs-lookup"><span data-stu-id="27722-117">Type: **const [**FLOAT**](../winprog/windows-data-types.md)\***</span></span>

<span data-ttu-id="27722-118">第二個 SH 向量的指標。</span><span class="sxs-lookup"><span data-stu-id="27722-118">Pointer to the second SH vector.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="27722-119">傳回值</span><span class="sxs-lookup"><span data-stu-id="27722-119">Return value</span></span>

<span data-ttu-id="27722-120">類型： **[ **FLOAT**](../winprog/windows-data-types.md)**</span><span class="sxs-lookup"><span data-stu-id="27722-120">Type: **[**FLOAT**](../winprog/windows-data-types.md)**</span></span>

<span data-ttu-id="27722-121">SH 輸出係數。</span><span class="sxs-lookup"><span data-stu-id="27722-121">SH output coefficients.</span></span>

## <a name="remarks"></a><span data-ttu-id="27722-122">備註</span><span class="sxs-lookup"><span data-stu-id="27722-122">Remarks</span></span>

<span data-ttu-id="27722-123">基礎函數 Ylm 的每個係數都會儲存在記憶體位置 l ² + m + l，其中：</span><span class="sxs-lookup"><span data-stu-id="27722-123">Each coefficient of the basis function Yₗₘ is stored at memory location l² + m + l, where:</span></span>

-   <span data-ttu-id="27722-124">l 是基礎函數的程度。</span><span class="sxs-lookup"><span data-stu-id="27722-124">l is the degree of the basis function.</span></span>
-   <span data-ttu-id="27722-125">m 是指定 l 值的基礎函數索引，範圍從-l 到 l （含）。</span><span class="sxs-lookup"><span data-stu-id="27722-125">m is the basis function index for the given l value and ranges from -l to l, inclusive.</span></span>

## <a name="requirements"></a><span data-ttu-id="27722-126">規格需求</span><span class="sxs-lookup"><span data-stu-id="27722-126">Requirements</span></span>



| <span data-ttu-id="27722-127">需求</span><span class="sxs-lookup"><span data-stu-id="27722-127">Requirement</span></span> | <span data-ttu-id="27722-128">值</span><span class="sxs-lookup"><span data-stu-id="27722-128">Value</span></span> |
|--------------------|----------------------------------------------------------------------------------------|
| <span data-ttu-id="27722-129">標頭</span><span class="sxs-lookup"><span data-stu-id="27722-129">Header</span></span><br/>  | <dl> <span data-ttu-id="27722-130"><dt>D3dx9math。h</dt></span><span class="sxs-lookup"><span data-stu-id="27722-130"><dt>D3dx9math.h</dt></span></span> </dl> |
| <span data-ttu-id="27722-131">程式庫</span><span class="sxs-lookup"><span data-stu-id="27722-131">Library</span></span><br/> | <dl> <span data-ttu-id="27722-132"><dt>D3dx9 .lib</dt></span><span class="sxs-lookup"><span data-stu-id="27722-132"><dt>D3dx9.lib</dt></span></span> </dl>   |



## <a name="see-also"></a><span data-ttu-id="27722-133">另請參閱</span><span class="sxs-lookup"><span data-stu-id="27722-133">See also</span></span>

<dl> <dt>

[<span data-ttu-id="27722-134">數學函數</span><span class="sxs-lookup"><span data-stu-id="27722-134">Math Functions</span></span>](dx9-graphics-reference-d3dx-functions-math.md)
</dt> <dt>

[<span data-ttu-id="27722-135">預先計算 Radiance Transfer (Direct3D 9) </span><span class="sxs-lookup"><span data-stu-id="27722-135">Precomputed Radiance Transfer (Direct3D 9)</span></span>](precomputed-radiance-transfer.md)
</dt> </dl>

 

 
