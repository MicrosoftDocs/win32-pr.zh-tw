---
description: 計算兩個球形諧波函式的乘積 (f 和 g) 。 這兩個函數的順序都是 N = 6。
ms.assetid: 3b68b238-c1ae-4ab8-89ed-bdf815463143
title: 'D3DXSHMultiply6 函式 (D3DX10Math) '
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- D3DXSHMultiply6
api_type:
- LibDef
api_location:
- D3DX10.lib
- D3DX10.dll
ms.openlocfilehash: 0768bb8be1f2f23693a431a2c0ea8f3d5a6846d2
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 03/15/2021
ms.locfileid: "106985897"
---
# <a name="d3dxshmultiply6-function"></a><span data-ttu-id="caa04-104">D3DXSHMultiply6 函式</span><span class="sxs-lookup"><span data-stu-id="caa04-104">D3DXSHMultiply6 function</span></span>

<span data-ttu-id="caa04-105">計算兩個球形諧波函式的乘積 (f 和 g) 。</span><span class="sxs-lookup"><span data-stu-id="caa04-105">Computes the product of two spherical harmonics functions (f and g).</span></span> <span data-ttu-id="caa04-106">這兩個函數的順序都是 N = 6。</span><span class="sxs-lookup"><span data-stu-id="caa04-106">Both functions are of order N = 6.</span></span>

## <a name="syntax"></a><span data-ttu-id="caa04-107">語法</span><span class="sxs-lookup"><span data-stu-id="caa04-107">Syntax</span></span>


```C++
FLOAT* D3DXSHMultiply6(
  _In_       FLOAT *pOut,
  _In_ const FLOAT *pF,
  _In_ const FLOAT *pG
);
```



## <a name="parameters"></a><span data-ttu-id="caa04-108">參數</span><span class="sxs-lookup"><span data-stu-id="caa04-108">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="caa04-109">*不悅* \[在\]</span><span class="sxs-lookup"><span data-stu-id="caa04-109">*pOut* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="caa04-110">類型： **[ **FLOAT**](../winprog/windows-data-types.md)\***</span><span class="sxs-lookup"><span data-stu-id="caa04-110">Type: **[**FLOAT**](../winprog/windows-data-types.md)\***</span></span>

<span data-ttu-id="caa04-111">輸出 SH 係數的指標-基礎函數 *Y* lm 會儲存在 l ² + *m* + l。</span><span class="sxs-lookup"><span data-stu-id="caa04-111">Pointer to the output SH coefficients — the basis function *Y* ₗₘ is stored at l² + *m* + l.</span></span> <span data-ttu-id="caa04-112">順序 *N* 決定陣列的長度，其中應該一律為 *N*²係數。</span><span class="sxs-lookup"><span data-stu-id="caa04-112">The order *N* determines the length of the array, where there should always be *N*² coefficients.</span></span>

</dd> <dt>

<span data-ttu-id="caa04-113">*pF* \[在\]</span><span class="sxs-lookup"><span data-stu-id="caa04-113">*pF* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="caa04-114">Type： **Const [**FLOAT**](../winprog/windows-data-types.md) \***</span><span class="sxs-lookup"><span data-stu-id="caa04-114">Type: **const [**FLOAT**](../winprog/windows-data-types.md)\***</span></span>

<span data-ttu-id="caa04-115">第一個函數的輸入 SH 係數。</span><span class="sxs-lookup"><span data-stu-id="caa04-115">Input SH coefficients for first function.</span></span>

</dd> <dt>

<span data-ttu-id="caa04-116">*pG* \[在\]</span><span class="sxs-lookup"><span data-stu-id="caa04-116">*pG* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="caa04-117">Type： **Const [**FLOAT**](../winprog/windows-data-types.md) \***</span><span class="sxs-lookup"><span data-stu-id="caa04-117">Type: **const [**FLOAT**](../winprog/windows-data-types.md)\***</span></span>

<span data-ttu-id="caa04-118">第二組輸入 SH 係數。</span><span class="sxs-lookup"><span data-stu-id="caa04-118">Second set of input SH coefficients.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="caa04-119">傳回值</span><span class="sxs-lookup"><span data-stu-id="caa04-119">Return value</span></span>

<span data-ttu-id="caa04-120">類型： **[ **FLOAT**](../winprog/windows-data-types.md)\***</span><span class="sxs-lookup"><span data-stu-id="caa04-120">Type: **[**FLOAT**](../winprog/windows-data-types.md)\***</span></span>

<span data-ttu-id="caa04-121">SH 輸出係數的指標。</span><span class="sxs-lookup"><span data-stu-id="caa04-121">Pointer to SH output coefficients.</span></span>

## <a name="remarks"></a><span data-ttu-id="caa04-122">備註</span><span class="sxs-lookup"><span data-stu-id="caa04-122">Remarks</span></span>

<span data-ttu-id="caa04-123">Order N = 6 的兩個 SH 函數的乘積會產生 order 2 × *n-1* = 11 的 sh 函式，但結果會被截斷。</span><span class="sxs-lookup"><span data-stu-id="caa04-123">The product of two SH functions of order N = 6 generates an SH function of order 2 × *N* - 1 = 11, but the results are truncated.</span></span> <span data-ttu-id="caa04-124">這表示產品與 ( *f* × *g*  =  *g* × *f* ) 但不會關聯 ( *f* x ( *g* × *h* ) ≠ ( *f* × *g* ) × *h* ) 。</span><span class="sxs-lookup"><span data-stu-id="caa04-124">This means that the product commutes ( *f* × *g* = *g* × *f* ) but doesn't associate ( *f* × ( *g* × *h* ) ≠ ( *f* × *g* ) × *h* ).</span></span>

<span data-ttu-id="caa04-125">此函式會使用下列方程式：</span><span class="sxs-lookup"><span data-stu-id="caa04-125">This function uses the following equation:</span></span>


```
pOut[i] = int(y_i(s) * f(s) * g(s))
```



<span data-ttu-id="caa04-126">其中，y \_ i (s) 是第 i 個 sh 基礎函式，其中 f (s) 和 g () 使用下列 SH 函數：</span><span class="sxs-lookup"><span data-stu-id="caa04-126">where y\_i(s) is the ith SH basis function, and where f(s) and g(s) use the following SH function:</span></span>


```
sum_i(y_i(s)*c_i)
```



## <a name="requirements"></a><span data-ttu-id="caa04-127">規格需求</span><span class="sxs-lookup"><span data-stu-id="caa04-127">Requirements</span></span>



| <span data-ttu-id="caa04-128">需求</span><span class="sxs-lookup"><span data-stu-id="caa04-128">Requirement</span></span> | <span data-ttu-id="caa04-129">值</span><span class="sxs-lookup"><span data-stu-id="caa04-129">Value</span></span> |
|--------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="caa04-130">標頭</span><span class="sxs-lookup"><span data-stu-id="caa04-130">Header</span></span><br/>  | <dl> <span data-ttu-id="caa04-131"><dt>D3DX10Math。h</dt></span><span class="sxs-lookup"><span data-stu-id="caa04-131"><dt>D3DX10Math.h</dt></span></span> </dl> |
| <span data-ttu-id="caa04-132">程式庫</span><span class="sxs-lookup"><span data-stu-id="caa04-132">Library</span></span><br/> | <dl> <span data-ttu-id="caa04-133"><dt>D3DX10 .lib</dt></span><span class="sxs-lookup"><span data-stu-id="caa04-133"><dt>D3DX10.lib</dt></span></span> </dl>   |



## <a name="see-also"></a><span data-ttu-id="caa04-134">另請參閱</span><span class="sxs-lookup"><span data-stu-id="caa04-134">See also</span></span>

<dl> <dt>

[<span data-ttu-id="caa04-135">數學函數</span><span class="sxs-lookup"><span data-stu-id="caa04-135">Math Functions</span></span>](d3d10-graphics-reference-d3dx10-functions-math.md)
</dt> </dl>

 

 
