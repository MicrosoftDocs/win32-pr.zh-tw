---
description: 以 SH (f 和 g) ，計算兩個函式的乘積。
ms.assetid: 632400a4-2ac9-438d-85f7-869101f350c8
title: 'D3DXSHMultiply2 函式 (D3dx9math) '
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- D3DXSHMultiply2
- D3DXSHMultiply3
- D3DXSHMultiply4
- D3DXSHMultiply5
- D3DXSHMultiply6
api_type:
- HeaderDef
api_location:
- d3dx9math.h
ms.openlocfilehash: f7b9adaf5caf7b4b2d35035fd5c2a916298b0c8c
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 03/15/2021
ms.locfileid: "106985875"
---
# <a name="d3dxshmultiply2-function-d3dx9mathh"></a><span data-ttu-id="be868-103">D3DXSHMultiply2 函式 (D3dx9math) </span><span class="sxs-lookup"><span data-stu-id="be868-103">D3DXSHMultiply2 function (D3dx9math.h)</span></span>

<span data-ttu-id="be868-104">以 SH (f 和 g) ，計算兩個函式的乘積。</span><span class="sxs-lookup"><span data-stu-id="be868-104">Computes the product of two functions represented using SH (f and g).</span></span>

## <a name="syntax"></a><span data-ttu-id="be868-105">語法</span><span class="sxs-lookup"><span data-stu-id="be868-105">Syntax</span></span>


```C++
FLOAT* D3DXSHMultiply2(
  _In_       FLOAT *pOut,
  _In_ const FLOAT *pF,
  _In_ const FLOAT *pG
);
```



## <a name="parameters"></a><span data-ttu-id="be868-106">參數</span><span class="sxs-lookup"><span data-stu-id="be868-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="be868-107">*不悅* \[在\]</span><span class="sxs-lookup"><span data-stu-id="be868-107">*pOut* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="be868-108">類型： **[ **FLOAT**](../winprog/windows-data-types.md)\***</span><span class="sxs-lookup"><span data-stu-id="be868-108">Type: **[**FLOAT**](../winprog/windows-data-types.md)\***</span></span>

<span data-ttu-id="be868-109">輸出 SH 係數-基礎函數 Ylm 的指標會儲存在 l \* l + m + l。</span><span class="sxs-lookup"><span data-stu-id="be868-109">Pointer to the output SH coefficients - basis function Ylm is stored at l\*l + m+l.</span></span>

</dd> <dt>

<span data-ttu-id="be868-110">*pF* \[在\]</span><span class="sxs-lookup"><span data-stu-id="be868-110">*pF* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="be868-111">Type： **Const [**FLOAT**](../winprog/windows-data-types.md) \***</span><span class="sxs-lookup"><span data-stu-id="be868-111">Type: **const [**FLOAT**](../winprog/windows-data-types.md)\***</span></span>

<span data-ttu-id="be868-112">輸入 SH coeffs for first 函數。</span><span class="sxs-lookup"><span data-stu-id="be868-112">Input SH coeffs for first function.</span></span>

</dd> <dt>

<span data-ttu-id="be868-113">*pG* \[在\]</span><span class="sxs-lookup"><span data-stu-id="be868-113">*pG* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="be868-114">Type： **Const [**FLOAT**](../winprog/windows-data-types.md) \***</span><span class="sxs-lookup"><span data-stu-id="be868-114">Type: **const [**FLOAT**](../winprog/windows-data-types.md)\***</span></span>

<span data-ttu-id="be868-115">第二組輸入 SH coeffs。</span><span class="sxs-lookup"><span data-stu-id="be868-115">Second set of input SH coeffs.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="be868-116">傳回值</span><span class="sxs-lookup"><span data-stu-id="be868-116">Return value</span></span>

<span data-ttu-id="be868-117">類型： **[ **FLOAT**](../winprog/windows-data-types.md)\***</span><span class="sxs-lookup"><span data-stu-id="be868-117">Type: **[**FLOAT**](../winprog/windows-data-types.md)\***</span></span>

<span data-ttu-id="be868-118">SH 輸出係數的指標。</span><span class="sxs-lookup"><span data-stu-id="be868-118">Pointer to SH output coefficients.</span></span>

## <a name="remarks"></a><span data-ttu-id="be868-119">備註</span><span class="sxs-lookup"><span data-stu-id="be868-119">Remarks</span></span>

<span data-ttu-id="be868-120">順序是介於2和6（含）之間的數位。</span><span class="sxs-lookup"><span data-stu-id="be868-120">The order is a number between 2 and 6 inclusive.</span></span> <span data-ttu-id="be868-121">因此，此頁面實際上記載了數個函數： D3DXSHMultiply2、D3DXSHMultiply3、.。。D3DXSHMultiply6.</span><span class="sxs-lookup"><span data-stu-id="be868-121">So this page actually documents several functions: D3DXSHMultiply2, D3DXSHMultiply3, ... D3DXSHMultiply6.</span></span>

<span data-ttu-id="be868-122">使用 SH (f 和 g) 來計算兩個函式的乘積，其中 *不悅* \[ i \] = int (y \_ i (s) \* f (s) \* g (s) ) ，其中的 y \_ i () 是第 i 個 sh 基礎函式，f (s) 和 g (s) 是 SH 函式 (sum i (y () \_ \_ \* c \_ i) ) 。</span><span class="sxs-lookup"><span data-stu-id="be868-122">Computes the product of two functions represented using SH (f and g), where *pOut*\[i\] = int(y\_i(s) \* f(s) \* g(s)), where y\_i(s) is the ith SH basis function, f(s) and g(s) are SH functions (sum\_i(y\_i(s)\*c\_i)).</span></span> <span data-ttu-id="be868-123">順序 O 決定陣列的長度，其中應該一律為 O ^ 2 係數。</span><span class="sxs-lookup"><span data-stu-id="be868-123">The order O determines the lengths of the arrays, where there should always be O^2 coefficients.</span></span> <span data-ttu-id="be868-124">一般而言，order O 的兩個 SH 函數的乘積會產生 order 2 的 SH 函 \* 式，但結果會被截斷。</span><span class="sxs-lookup"><span data-stu-id="be868-124">In general the product of two SH functions of order O generates an SH function of order 2\*O - 1, but the results are truncated.</span></span> <span data-ttu-id="be868-125">這表示產品與 (f \* g = = g \* f) 但不會將 (f \* (g \* h) ！ = (f \* g) h \* 相關聯。</span><span class="sxs-lookup"><span data-stu-id="be868-125">This means that the product commutes (f\*g == g\*f) but doesn't associate (f\*(g\*h) != (f\*g)\*h.</span></span>

## <a name="requirements"></a><span data-ttu-id="be868-126">規格需求</span><span class="sxs-lookup"><span data-stu-id="be868-126">Requirements</span></span>



| <span data-ttu-id="be868-127">需求</span><span class="sxs-lookup"><span data-stu-id="be868-127">Requirement</span></span> | <span data-ttu-id="be868-128">值</span><span class="sxs-lookup"><span data-stu-id="be868-128">Value</span></span> |
|-------------------|----------------------------------------------------------------------------------------|
| <span data-ttu-id="be868-129">標頭</span><span class="sxs-lookup"><span data-stu-id="be868-129">Header</span></span><br/> | <dl> <span data-ttu-id="be868-130"><dt>D3dx9math。h</dt></span><span class="sxs-lookup"><span data-stu-id="be868-130"><dt>D3dx9math.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="be868-131">另請參閱</span><span class="sxs-lookup"><span data-stu-id="be868-131">See also</span></span>

<dl> <dt>

[<span data-ttu-id="be868-132">數學函數</span><span class="sxs-lookup"><span data-stu-id="be868-132">Math Functions</span></span>](dx9-graphics-reference-d3dx-functions-math.md)
</dt> </dl>

 

 
