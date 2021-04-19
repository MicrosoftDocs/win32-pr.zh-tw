---
description: 計算兩個矩陣的轉換乘積。
ms.assetid: 43927500-9413-41a4-a6ee-974d85dd1054
title: 'D3DXMatrixMultiplyTranspose 函式 (D3dx9math) '
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
- d3dx9.lib
- d3dx9.dll
ms.openlocfilehash: b599453ae108a5a8bab8ee896858760c85799948
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 03/15/2021
ms.locfileid: "106982191"
---
# <a name="d3dxmatrixmultiplytranspose-function-d3dx9mathh"></a><span data-ttu-id="c4c2d-103">D3DXMatrixMultiplyTranspose 函式 (D3dx9math) </span><span class="sxs-lookup"><span data-stu-id="c4c2d-103">D3DXMatrixMultiplyTranspose function (D3dx9math.h)</span></span>

<span data-ttu-id="c4c2d-104">計算兩個矩陣的轉換乘積。</span><span class="sxs-lookup"><span data-stu-id="c4c2d-104">Calculates the transposed product of two matrices.</span></span>

## <a name="syntax"></a><span data-ttu-id="c4c2d-105">語法</span><span class="sxs-lookup"><span data-stu-id="c4c2d-105">Syntax</span></span>


```C++
D3DXMATRIX* D3DXMatrixMultiplyTranspose(
  _Inout_       D3DXMATRIX *pOut,
  _In_    const D3DXMATRIX *pM1,
  _In_    const D3DXMATRIX *pM2
);
```



## <a name="parameters"></a><span data-ttu-id="c4c2d-106">參數</span><span class="sxs-lookup"><span data-stu-id="c4c2d-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="c4c2d-107">*不悅* \[in、out\]</span><span class="sxs-lookup"><span data-stu-id="c4c2d-107">*pOut* \[in, out\]</span></span>
</dt> <dd>

<span data-ttu-id="c4c2d-108">類型： **[ **D3DXMATRIX**](d3dxmatrix.md)\***</span><span class="sxs-lookup"><span data-stu-id="c4c2d-108">Type: **[**D3DXMATRIX**](d3dxmatrix.md)\***</span></span>

<span data-ttu-id="c4c2d-109">[**D3DXMATRIX**](d3dxmatrix.md)結構的指標，此結構是作業的結果。</span><span class="sxs-lookup"><span data-stu-id="c4c2d-109">Pointer to the [**D3DXMATRIX**](d3dxmatrix.md) structure that is the result of the operation.</span></span>

</dd> <dt>

<span data-ttu-id="c4c2d-110">*pM1* \[在\]</span><span class="sxs-lookup"><span data-stu-id="c4c2d-110">*pM1* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="c4c2d-111">Type： **Const [**D3DXMATRIX**](d3dxmatrix.md) \***</span><span class="sxs-lookup"><span data-stu-id="c4c2d-111">Type: **const [**D3DXMATRIX**](d3dxmatrix.md)\***</span></span>

<span data-ttu-id="c4c2d-112">來源 [**D3DXMATRIX**](d3dxmatrix.md) 結構的指標。</span><span class="sxs-lookup"><span data-stu-id="c4c2d-112">Pointer to a source [**D3DXMATRIX**](d3dxmatrix.md) structure.</span></span>

</dd> <dt>

<span data-ttu-id="c4c2d-113">*pM2* \[在\]</span><span class="sxs-lookup"><span data-stu-id="c4c2d-113">*pM2* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="c4c2d-114">Type： **Const [**D3DXMATRIX**](d3dxmatrix.md) \***</span><span class="sxs-lookup"><span data-stu-id="c4c2d-114">Type: **const [**D3DXMATRIX**](d3dxmatrix.md)\***</span></span>

<span data-ttu-id="c4c2d-115">來源 [**D3DXMATRIX**](d3dxmatrix.md) 結構的指標。</span><span class="sxs-lookup"><span data-stu-id="c4c2d-115">Pointer to a source [**D3DXMATRIX**](d3dxmatrix.md) structure.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="c4c2d-116">傳回值</span><span class="sxs-lookup"><span data-stu-id="c4c2d-116">Return value</span></span>

<span data-ttu-id="c4c2d-117">類型： **[ **D3DXMATRIX**](d3dxmatrix.md)\***</span><span class="sxs-lookup"><span data-stu-id="c4c2d-117">Type: **[**D3DXMATRIX**](d3dxmatrix.md)\***</span></span>

<span data-ttu-id="c4c2d-118">[**D3DXMATRIX**](d3dxmatrix.md)結構的指標，這是兩個矩陣的乘積。</span><span class="sxs-lookup"><span data-stu-id="c4c2d-118">Pointer to a [**D3DXMATRIX**](d3dxmatrix.md) structure that is the product of two matrices.</span></span>

## <a name="remarks"></a><span data-ttu-id="c4c2d-119">備註</span><span class="sxs-lookup"><span data-stu-id="c4c2d-119">Remarks</span></span>

<span data-ttu-id="c4c2d-120">結果會是兩個轉換矩陣的乘積，Out = T (M1 \* M2) 。</span><span class="sxs-lookup"><span data-stu-id="c4c2d-120">The result is the transposed of the product of two transformation matrices, Out = T(M1\*M2).</span></span>

<span data-ttu-id="c4c2d-121">此函式的傳回值與 *不悅* 參數中所傳回的值相同。</span><span class="sxs-lookup"><span data-stu-id="c4c2d-121">The return value for this function is the same value returned in the *pOut* parameter.</span></span> <span data-ttu-id="c4c2d-122">如此一來， **D3DXMatrixMultiplyTranspose** 函式就可以用來做為另一個函式的參數。</span><span class="sxs-lookup"><span data-stu-id="c4c2d-122">In this way, the **D3DXMatrixMultiplyTranspose** function can be used as a parameter for another function.</span></span>

<span data-ttu-id="c4c2d-123">此函數有助於將矩陣設定為頂點和圖元著色器的常數。</span><span class="sxs-lookup"><span data-stu-id="c4c2d-123">This function is useful to set matrices as constants for vertex and pixel shaders.</span></span>

## <a name="requirements"></a><span data-ttu-id="c4c2d-124">規格需求</span><span class="sxs-lookup"><span data-stu-id="c4c2d-124">Requirements</span></span>



| <span data-ttu-id="c4c2d-125">需求</span><span class="sxs-lookup"><span data-stu-id="c4c2d-125">Requirement</span></span> | <span data-ttu-id="c4c2d-126">值</span><span class="sxs-lookup"><span data-stu-id="c4c2d-126">Value</span></span> |
|--------------------|----------------------------------------------------------------------------------------|
| <span data-ttu-id="c4c2d-127">標頭</span><span class="sxs-lookup"><span data-stu-id="c4c2d-127">Header</span></span><br/>  | <dl> <span data-ttu-id="c4c2d-128"><dt>D3dx9math。h</dt></span><span class="sxs-lookup"><span data-stu-id="c4c2d-128"><dt>D3dx9math.h</dt></span></span> </dl> |
| <span data-ttu-id="c4c2d-129">程式庫</span><span class="sxs-lookup"><span data-stu-id="c4c2d-129">Library</span></span><br/> | <dl> <span data-ttu-id="c4c2d-130"><dt>D3dx9 .lib</dt></span><span class="sxs-lookup"><span data-stu-id="c4c2d-130"><dt>D3dx9.lib</dt></span></span> </dl>   |



## <a name="see-also"></a><span data-ttu-id="c4c2d-131">另請參閱</span><span class="sxs-lookup"><span data-stu-id="c4c2d-131">See also</span></span>

<dl> <dt>

[<span data-ttu-id="c4c2d-132">數學函數</span><span class="sxs-lookup"><span data-stu-id="c4c2d-132">Math Functions</span></span>](dx9-graphics-reference-d3dx-functions-math.md)
</dt> <dt>

[<span data-ttu-id="c4c2d-133">**D3DXMatrixMultiply**</span><span class="sxs-lookup"><span data-stu-id="c4c2d-133">**D3DXMatrixMultiply**</span></span>](d3dxmatrixmultiply.md)
</dt> <dt>

[<span data-ttu-id="c4c2d-134">**D3DXQuaternionMultiply**</span><span class="sxs-lookup"><span data-stu-id="c4c2d-134">**D3DXQuaternionMultiply**</span></span>](d3dxquaternionmultiply.md)
</dt> </dl>

 

 




