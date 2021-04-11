---
description: 計算兩個球形諧波函式的乘積 (f 和 g) 。 這兩個函數的順序都是 N = 4。
ms.assetid: 05427a18-447e-45d7-a851-e580298c9a1f
title: 'D3DXSHMultiply4 函式 (D3DX10Math) '
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- D3DXSHMultiply4
api_type:
- LibDef
api_location:
- D3DX10.lib
- D3DX10.dll
ms.openlocfilehash: 13e8b62674ccbabbb03259f06b79f330424ddf84
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 03/15/2021
ms.locfileid: "104196365"
---
# <a name="d3dxshmultiply4-function"></a><span data-ttu-id="f900f-104">D3DXSHMultiply4 函式</span><span class="sxs-lookup"><span data-stu-id="f900f-104">D3DXSHMultiply4 function</span></span>

<span data-ttu-id="f900f-105">計算兩個球形諧波函式的乘積 (*f* 和 *g*) 。</span><span class="sxs-lookup"><span data-stu-id="f900f-105">Computes the product of two spherical harmonics functions (*f* and *g*).</span></span> <span data-ttu-id="f900f-106">這兩個函數的順序都是 N = 4。</span><span class="sxs-lookup"><span data-stu-id="f900f-106">Both functions are of order N = 4.</span></span>

## <a name="syntax"></a><span data-ttu-id="f900f-107">語法</span><span class="sxs-lookup"><span data-stu-id="f900f-107">Syntax</span></span>


```C++
FLOAT* D3DXSHMultiply4(
  _In_       FLOAT *pOut,
  _In_ const FLOAT *pF,
  _In_ const FLOAT *pG
);
```



## <a name="parameters"></a><span data-ttu-id="f900f-108">參數</span><span class="sxs-lookup"><span data-stu-id="f900f-108">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="f900f-109">*不悅* \[在\]</span><span class="sxs-lookup"><span data-stu-id="f900f-109">*pOut* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="f900f-110">類型： **[ **FLOAT**](../winprog/windows-data-types.md)\***</span><span class="sxs-lookup"><span data-stu-id="f900f-110">Type: **[**FLOAT**](../winprog/windows-data-types.md)\***</span></span>

<span data-ttu-id="f900f-111">輸出 SH 係數的指標-基礎函數 *Y* lm 會儲存在 l ² + *m* + l。</span><span class="sxs-lookup"><span data-stu-id="f900f-111">Pointer to the output SH coefficients — basis function *Y* ₗₘ is stored at l² + *m* + l.</span></span> <span data-ttu-id="f900f-112">順序 *N* 決定陣列的長度，其中應該一律為 *N*²係數。</span><span class="sxs-lookup"><span data-stu-id="f900f-112">The order *N* determines the length of the array, where there should always be *N*² coefficients.</span></span>

</dd> <dt>

<span data-ttu-id="f900f-113">*pF* \[在\]</span><span class="sxs-lookup"><span data-stu-id="f900f-113">*pF* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="f900f-114">Type： **Const [**FLOAT**](../winprog/windows-data-types.md) \***</span><span class="sxs-lookup"><span data-stu-id="f900f-114">Type: **const [**FLOAT**](../winprog/windows-data-types.md)\***</span></span>

<span data-ttu-id="f900f-115">第一個函數的輸入 SH 係數。</span><span class="sxs-lookup"><span data-stu-id="f900f-115">Input SH coefficients for first function.</span></span>

</dd> <dt>

<span data-ttu-id="f900f-116">*pG* \[在\]</span><span class="sxs-lookup"><span data-stu-id="f900f-116">*pG* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="f900f-117">Type： **Const [**FLOAT**](../winprog/windows-data-types.md) \***</span><span class="sxs-lookup"><span data-stu-id="f900f-117">Type: **const [**FLOAT**](../winprog/windows-data-types.md)\***</span></span>

<span data-ttu-id="f900f-118">第二組輸入 SH 係數。</span><span class="sxs-lookup"><span data-stu-id="f900f-118">Second set of input SH coefficients.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="f900f-119">傳回值</span><span class="sxs-lookup"><span data-stu-id="f900f-119">Return value</span></span>

<span data-ttu-id="f900f-120">類型： **[ **FLOAT**](../winprog/windows-data-types.md)\***</span><span class="sxs-lookup"><span data-stu-id="f900f-120">Type: **[**FLOAT**](../winprog/windows-data-types.md)\***</span></span>

<span data-ttu-id="f900f-121">SH 輸出係數的指標。</span><span class="sxs-lookup"><span data-stu-id="f900f-121">Pointer to SH output coefficients.</span></span>

## <a name="remarks"></a><span data-ttu-id="f900f-122">備註</span><span class="sxs-lookup"><span data-stu-id="f900f-122">Remarks</span></span>

<span data-ttu-id="f900f-123">Order N = 4 的兩個 SH 函數的乘積會產生 order 2 × *n-1* = 7 的 sh 函式，但結果會被截斷。</span><span class="sxs-lookup"><span data-stu-id="f900f-123">The product of two SH functions of order N = 4 generates an SH function of order 2 × *N* - 1 = 7, but the results are truncated.</span></span> <span data-ttu-id="f900f-124">這表示產品與 ( *f* × *g*  =  *g* × *f* ) 但不會關聯 ( *f* x ( *g* × *h* ) ≠ ( *f* × *g* ) × *h* ) 。</span><span class="sxs-lookup"><span data-stu-id="f900f-124">This means that the product commutes ( *f* × *g* = *g* × *f* ) but doesn't associate ( *f* × ( *g* × *h* ) ≠ ( *f* × *g* ) × *h* ).</span></span>

<span data-ttu-id="f900f-125">此函式會使用下列方程式：</span><span class="sxs-lookup"><span data-stu-id="f900f-125">This function uses the following equation:</span></span>


```
pOut[i] = int(y_i(s) * f(s) * g(s))
```



<span data-ttu-id="f900f-126">其中，y \_ i (s) 是第 i 個 sh 基礎函式，其中 f (s) 和 g () 使用下列 SH 函數：</span><span class="sxs-lookup"><span data-stu-id="f900f-126">where y\_i(s) is the ith SH basis function, and where f(s) and g(s) use the following SH function:</span></span>


```
sum_i(y_i(s)*c_i)
```



## <a name="requirements"></a><span data-ttu-id="f900f-127">規格需求</span><span class="sxs-lookup"><span data-stu-id="f900f-127">Requirements</span></span>



| <span data-ttu-id="f900f-128">需求</span><span class="sxs-lookup"><span data-stu-id="f900f-128">Requirement</span></span> | <span data-ttu-id="f900f-129">值</span><span class="sxs-lookup"><span data-stu-id="f900f-129">Value</span></span> |
|--------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="f900f-130">標頭</span><span class="sxs-lookup"><span data-stu-id="f900f-130">Header</span></span><br/>  | <dl> <span data-ttu-id="f900f-131"><dt>D3DX10Math。h</dt></span><span class="sxs-lookup"><span data-stu-id="f900f-131"><dt>D3DX10Math.h</dt></span></span> </dl> |
| <span data-ttu-id="f900f-132">程式庫</span><span class="sxs-lookup"><span data-stu-id="f900f-132">Library</span></span><br/> | <dl> <span data-ttu-id="f900f-133"><dt>D3DX10 .lib</dt></span><span class="sxs-lookup"><span data-stu-id="f900f-133"><dt>D3DX10.lib</dt></span></span> </dl>   |



## <a name="see-also"></a><span data-ttu-id="f900f-134">另請參閱</span><span class="sxs-lookup"><span data-stu-id="f900f-134">See also</span></span>

<dl> <dt>

[<span data-ttu-id="f900f-135">數學函數</span><span class="sxs-lookup"><span data-stu-id="f900f-135">Math Functions</span></span>](d3d10-graphics-reference-d3dx10-functions-math.md)
</dt> </dl>

 

 
