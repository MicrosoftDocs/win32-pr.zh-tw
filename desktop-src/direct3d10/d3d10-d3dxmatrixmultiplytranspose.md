---
description: 計算兩個矩陣的轉換乘積。
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
ms.openlocfilehash: 187912a4117ab502ea7b0b1b3fc1ea105ecbc3e7
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 03/15/2021
ms.locfileid: "106981851"
---
# <a name="d3dxmatrixmultiplytranspose-function-d3dx10mathh"></a><span data-ttu-id="4248c-103">D3DXMatrixMultiplyTranspose 函式 (D3DX10Math) </span><span class="sxs-lookup"><span data-stu-id="4248c-103">D3DXMatrixMultiplyTranspose function (D3DX10Math.h)</span></span>

<span data-ttu-id="4248c-104">計算兩個矩陣的轉換乘積。</span><span class="sxs-lookup"><span data-stu-id="4248c-104">Calculates the transposed product of two matrices.</span></span>

## <a name="syntax"></a><span data-ttu-id="4248c-105">語法</span><span class="sxs-lookup"><span data-stu-id="4248c-105">Syntax</span></span>


```C++
D3DXMATRIX* D3DXMatrixMultiplyTranspose(
  _Inout_       D3DXMATRIX *pOut,
  _In_    const D3DXMATRIX *pM1,
  _In_    const D3DXMATRIX *pM2
);
```



## <a name="parameters"></a><span data-ttu-id="4248c-106">參數</span><span class="sxs-lookup"><span data-stu-id="4248c-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="4248c-107">*不悅* \[in、out\]</span><span class="sxs-lookup"><span data-stu-id="4248c-107">*pOut* \[in, out\]</span></span>
</dt> <dd>

<span data-ttu-id="4248c-108">類型： **[ **D3DXMATRIX**](../direct3d9/d3dxmatrix.md)\***</span><span class="sxs-lookup"><span data-stu-id="4248c-108">Type: **[**D3DXMATRIX**](../direct3d9/d3dxmatrix.md)\***</span></span>

<span data-ttu-id="4248c-109">[**D3DXMATRIX**](d3d10-d3dxmatrix.md)結構的指標，此結構是作業的結果。</span><span class="sxs-lookup"><span data-stu-id="4248c-109">Pointer to the [**D3DXMATRIX**](d3d10-d3dxmatrix.md) structure that is the result of the operation.</span></span>

</dd> <dt>

<span data-ttu-id="4248c-110">*pM1* \[在\]</span><span class="sxs-lookup"><span data-stu-id="4248c-110">*pM1* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="4248c-111">Type： **Const [**D3DXMATRIX**](../direct3d9/d3dxmatrix.md) \***</span><span class="sxs-lookup"><span data-stu-id="4248c-111">Type: **const [**D3DXMATRIX**](../direct3d9/d3dxmatrix.md)\***</span></span>

<span data-ttu-id="4248c-112">來源 D3DXMATRIX 結構的指標 (左手邊) 。</span><span class="sxs-lookup"><span data-stu-id="4248c-112">Pointer to a source D3DXMATRIX structure (left hand side).</span></span>

</dd> <dt>

<span data-ttu-id="4248c-113">*pM2* \[在\]</span><span class="sxs-lookup"><span data-stu-id="4248c-113">*pM2* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="4248c-114">Type： **Const [**D3DXMATRIX**](../direct3d9/d3dxmatrix.md) \***</span><span class="sxs-lookup"><span data-stu-id="4248c-114">Type: **const [**D3DXMATRIX**](../direct3d9/d3dxmatrix.md)\***</span></span>

<span data-ttu-id="4248c-115">指向來源 D3DXMATRIX 結構 (右手邊) 的指標。</span><span class="sxs-lookup"><span data-stu-id="4248c-115">Pointer to a source D3DXMATRIX structure (right hand side).</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="4248c-116">傳回值</span><span class="sxs-lookup"><span data-stu-id="4248c-116">Return value</span></span>

<span data-ttu-id="4248c-117">類型： **[ **D3DXMATRIX**](../direct3d9/d3dxmatrix.md)\***</span><span class="sxs-lookup"><span data-stu-id="4248c-117">Type: **[**D3DXMATRIX**](../direct3d9/d3dxmatrix.md)\***</span></span>

<span data-ttu-id="4248c-118">D3DXMATRIX 結構的指標，這是兩個矩陣的乘積。</span><span class="sxs-lookup"><span data-stu-id="4248c-118">Pointer to a D3DXMATRIX structure that is the product of two matrices.</span></span>

## <a name="remarks"></a><span data-ttu-id="4248c-119">備註</span><span class="sxs-lookup"><span data-stu-id="4248c-119">Remarks</span></span>

<span data-ttu-id="4248c-120">結果會是兩個轉換矩陣的乘積，Out = T (M1 \* M2) 。</span><span class="sxs-lookup"><span data-stu-id="4248c-120">The result is the transposed of the product of two transformation matrices, Out = T(M1\*M2).</span></span>

<span data-ttu-id="4248c-121">此函式的傳回值與不悅參數中所傳回的值相同。</span><span class="sxs-lookup"><span data-stu-id="4248c-121">The return value for this function is the same value returned in the pOut parameter.</span></span> <span data-ttu-id="4248c-122">如此一來，D3DXMatrixMultiplyTranspose 函式就可以用來做為另一個函式的參數。</span><span class="sxs-lookup"><span data-stu-id="4248c-122">In this way, the D3DXMatrixMultiplyTranspose function can be used as a parameter for another function.</span></span>

<span data-ttu-id="4248c-123">此函數有助於將矩陣設定為頂點和圖元著色器的常數。</span><span class="sxs-lookup"><span data-stu-id="4248c-123">This function is useful to set matrices as constants for vertex and pixel shaders.</span></span>

## <a name="requirements"></a><span data-ttu-id="4248c-124">規格需求</span><span class="sxs-lookup"><span data-stu-id="4248c-124">Requirements</span></span>



| <span data-ttu-id="4248c-125">需求</span><span class="sxs-lookup"><span data-stu-id="4248c-125">Requirement</span></span> | <span data-ttu-id="4248c-126">值</span><span class="sxs-lookup"><span data-stu-id="4248c-126">Value</span></span> |
|--------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="4248c-127">標頭</span><span class="sxs-lookup"><span data-stu-id="4248c-127">Header</span></span><br/>  | <dl> <span data-ttu-id="4248c-128"><dt>D3DX10Math。h</dt></span><span class="sxs-lookup"><span data-stu-id="4248c-128"><dt>D3DX10Math.h</dt></span></span> </dl> |
| <span data-ttu-id="4248c-129">程式庫</span><span class="sxs-lookup"><span data-stu-id="4248c-129">Library</span></span><br/> | <dl> <span data-ttu-id="4248c-130"><dt>D3DX10 .lib</dt></span><span class="sxs-lookup"><span data-stu-id="4248c-130"><dt>D3DX10.lib</dt></span></span> </dl>   |



## <a name="see-also"></a><span data-ttu-id="4248c-131">另請參閱</span><span class="sxs-lookup"><span data-stu-id="4248c-131">See also</span></span>

<dl> <dt>

[<span data-ttu-id="4248c-132">數學函數</span><span class="sxs-lookup"><span data-stu-id="4248c-132">Math Functions</span></span>](d3d10-graphics-reference-d3dx10-functions-math.md)
</dt> </dl>

 

 
