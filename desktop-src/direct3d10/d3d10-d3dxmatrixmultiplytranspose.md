---
description: D3DXMatrixMultiplyTranspose 函式 (D3DX10Math) -計算兩個矩陣的轉換乘積。
ms.assetid: 3db4138c-407c-47b5-b8b9-04af8771e98e
title: 'D3DXMatrixMultiplyTranspose 函式 (D3DX10Math) '
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- D3DXMatrixMultiplyTranspose
api_type:
- LibDef
api_location:
- D3DX10.lib
- D3DX10.dll
ms.openlocfilehash: fcf3d5578aa6e2ad13bd3f91dfd2206d6eaf0b13
ms.sourcegitcommit: 95685061d5b0333bbf9e6ebd208dde8190f97005
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 04/28/2021
ms.locfileid: "108103415"
---
# <a name="d3dxmatrixmultiplytranspose-function-d3dx10mathh"></a><span data-ttu-id="50b7e-103">D3DXMatrixMultiplyTranspose 函式 (D3DX10Math) </span><span class="sxs-lookup"><span data-stu-id="50b7e-103">D3DXMatrixMultiplyTranspose function (D3DX10Math.h)</span></span>

<span data-ttu-id="50b7e-104">計算兩個矩陣的轉換乘積。</span><span class="sxs-lookup"><span data-stu-id="50b7e-104">Calculates the transposed product of two matrices.</span></span>

## <a name="syntax"></a><span data-ttu-id="50b7e-105">語法</span><span class="sxs-lookup"><span data-stu-id="50b7e-105">Syntax</span></span>


```C++
D3DXMATRIX* D3DXMatrixMultiplyTranspose(
  _Inout_       D3DXMATRIX *pOut,
  _In_    const D3DXMATRIX *pM1,
  _In_    const D3DXMATRIX *pM2
);
```



## <a name="parameters"></a><span data-ttu-id="50b7e-106">參數</span><span class="sxs-lookup"><span data-stu-id="50b7e-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="50b7e-107">*不悅* \[in、out\]</span><span class="sxs-lookup"><span data-stu-id="50b7e-107">*pOut* \[in, out\]</span></span>
</dt> <dd>

<span data-ttu-id="50b7e-108">類型： **[ **D3DXMATRIX**](../direct3d9/d3dxmatrix.md)\***</span><span class="sxs-lookup"><span data-stu-id="50b7e-108">Type: **[**D3DXMATRIX**](../direct3d9/d3dxmatrix.md)\***</span></span>

<span data-ttu-id="50b7e-109">[**D3DXMATRIX**](d3d10-d3dxmatrix.md)結構的指標，此結構是作業的結果。</span><span class="sxs-lookup"><span data-stu-id="50b7e-109">Pointer to the [**D3DXMATRIX**](d3d10-d3dxmatrix.md) structure that is the result of the operation.</span></span>

</dd> <dt>

<span data-ttu-id="50b7e-110">*pM1* \[在\]</span><span class="sxs-lookup"><span data-stu-id="50b7e-110">*pM1* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="50b7e-111">Type： **Const [**D3DXMATRIX**](../direct3d9/d3dxmatrix.md) \***</span><span class="sxs-lookup"><span data-stu-id="50b7e-111">Type: **const [**D3DXMATRIX**](../direct3d9/d3dxmatrix.md)\***</span></span>

<span data-ttu-id="50b7e-112">來源 D3DXMATRIX 結構的指標 (左手邊) 。</span><span class="sxs-lookup"><span data-stu-id="50b7e-112">Pointer to a source D3DXMATRIX structure (left hand side).</span></span>

</dd> <dt>

<span data-ttu-id="50b7e-113">*pM2* \[在\]</span><span class="sxs-lookup"><span data-stu-id="50b7e-113">*pM2* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="50b7e-114">Type： **Const [**D3DXMATRIX**](../direct3d9/d3dxmatrix.md) \***</span><span class="sxs-lookup"><span data-stu-id="50b7e-114">Type: **const [**D3DXMATRIX**](../direct3d9/d3dxmatrix.md)\***</span></span>

<span data-ttu-id="50b7e-115">指向來源 D3DXMATRIX 結構 (右手邊) 的指標。</span><span class="sxs-lookup"><span data-stu-id="50b7e-115">Pointer to a source D3DXMATRIX structure (right hand side).</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="50b7e-116">傳回值</span><span class="sxs-lookup"><span data-stu-id="50b7e-116">Return value</span></span>

<span data-ttu-id="50b7e-117">類型： **[ **D3DXMATRIX**](../direct3d9/d3dxmatrix.md)\***</span><span class="sxs-lookup"><span data-stu-id="50b7e-117">Type: **[**D3DXMATRIX**](../direct3d9/d3dxmatrix.md)\***</span></span>

<span data-ttu-id="50b7e-118">D3DXMATRIX 結構的指標，這是兩個矩陣的乘積。</span><span class="sxs-lookup"><span data-stu-id="50b7e-118">Pointer to a D3DXMATRIX structure that is the product of two matrices.</span></span>

## <a name="remarks"></a><span data-ttu-id="50b7e-119">備註</span><span class="sxs-lookup"><span data-stu-id="50b7e-119">Remarks</span></span>

<span data-ttu-id="50b7e-120">結果會是兩個轉換矩陣的乘積，Out = T (M1 \* M2) 。</span><span class="sxs-lookup"><span data-stu-id="50b7e-120">The result is the transposed of the product of two transformation matrices, Out = T(M1\*M2).</span></span>

<span data-ttu-id="50b7e-121">此函式的傳回值與不悅參數中所傳回的值相同。</span><span class="sxs-lookup"><span data-stu-id="50b7e-121">The return value for this function is the same value returned in the pOut parameter.</span></span> <span data-ttu-id="50b7e-122">如此一來，D3DXMatrixMultiplyTranspose 函式就可以用來做為另一個函式的參數。</span><span class="sxs-lookup"><span data-stu-id="50b7e-122">In this way, the D3DXMatrixMultiplyTranspose function can be used as a parameter for another function.</span></span>

<span data-ttu-id="50b7e-123">此函數有助於將矩陣設定為頂點和圖元著色器的常數。</span><span class="sxs-lookup"><span data-stu-id="50b7e-123">This function is useful to set matrices as constants for vertex and pixel shaders.</span></span>

## <a name="requirements"></a><span data-ttu-id="50b7e-124">規格需求</span><span class="sxs-lookup"><span data-stu-id="50b7e-124">Requirements</span></span>



| <span data-ttu-id="50b7e-125">需求</span><span class="sxs-lookup"><span data-stu-id="50b7e-125">Requirement</span></span> | <span data-ttu-id="50b7e-126">值</span><span class="sxs-lookup"><span data-stu-id="50b7e-126">Value</span></span> |
|--------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="50b7e-127">標頭</span><span class="sxs-lookup"><span data-stu-id="50b7e-127">Header</span></span><br/>  | <dl> <span data-ttu-id="50b7e-128"><dt>D3DX10Math。h</dt></span><span class="sxs-lookup"><span data-stu-id="50b7e-128"><dt>D3DX10Math.h</dt></span></span> </dl> |
| <span data-ttu-id="50b7e-129">程式庫</span><span class="sxs-lookup"><span data-stu-id="50b7e-129">Library</span></span><br/> | <dl> <span data-ttu-id="50b7e-130"><dt>D3DX10 .lib</dt></span><span class="sxs-lookup"><span data-stu-id="50b7e-130"><dt>D3DX10.lib</dt></span></span> </dl>   |



## <a name="see-also"></a><span data-ttu-id="50b7e-131">另請參閱</span><span class="sxs-lookup"><span data-stu-id="50b7e-131">See also</span></span>

<dl> <dt>

[<span data-ttu-id="50b7e-132">數學函數</span><span class="sxs-lookup"><span data-stu-id="50b7e-132">Math Functions</span></span>](d3d10-graphics-reference-d3dx10-functions-math.md)
</dt> </dl>

 

 
