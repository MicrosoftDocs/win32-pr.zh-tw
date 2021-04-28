---
description: D3DXMatrixMultiplyTranspose 函式 (D3dx9math) -計算兩個矩陣的轉換乘積。
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
ms.openlocfilehash: 87aaa45e7a7a16884d17ab340f0bf1efeccd93bb
ms.sourcegitcommit: 95685061d5b0333bbf9e6ebd208dde8190f97005
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 04/28/2021
ms.locfileid: "108107536"
---
# <a name="d3dxmatrixmultiplytranspose-function-d3dx9mathh"></a><span data-ttu-id="7282c-103">D3DXMatrixMultiplyTranspose 函式 (D3dx9math) </span><span class="sxs-lookup"><span data-stu-id="7282c-103">D3DXMatrixMultiplyTranspose function (D3dx9math.h)</span></span>

<span data-ttu-id="7282c-104">計算兩個矩陣的轉換乘積。</span><span class="sxs-lookup"><span data-stu-id="7282c-104">Calculates the transposed product of two matrices.</span></span>

## <a name="syntax"></a><span data-ttu-id="7282c-105">語法</span><span class="sxs-lookup"><span data-stu-id="7282c-105">Syntax</span></span>


```C++
D3DXMATRIX* D3DXMatrixMultiplyTranspose(
  _Inout_       D3DXMATRIX *pOut,
  _In_    const D3DXMATRIX *pM1,
  _In_    const D3DXMATRIX *pM2
);
```



## <a name="parameters"></a><span data-ttu-id="7282c-106">參數</span><span class="sxs-lookup"><span data-stu-id="7282c-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="7282c-107">*不悅* \[in、out\]</span><span class="sxs-lookup"><span data-stu-id="7282c-107">*pOut* \[in, out\]</span></span>
</dt> <dd>

<span data-ttu-id="7282c-108">類型： **[ **D3DXMATRIX**](d3dxmatrix.md)\***</span><span class="sxs-lookup"><span data-stu-id="7282c-108">Type: **[**D3DXMATRIX**](d3dxmatrix.md)\***</span></span>

<span data-ttu-id="7282c-109">[**D3DXMATRIX**](d3dxmatrix.md)結構的指標，此結構是作業的結果。</span><span class="sxs-lookup"><span data-stu-id="7282c-109">Pointer to the [**D3DXMATRIX**](d3dxmatrix.md) structure that is the result of the operation.</span></span>

</dd> <dt>

<span data-ttu-id="7282c-110">*pM1* \[在\]</span><span class="sxs-lookup"><span data-stu-id="7282c-110">*pM1* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="7282c-111">Type： **Const [**D3DXMATRIX**](d3dxmatrix.md) \***</span><span class="sxs-lookup"><span data-stu-id="7282c-111">Type: **const [**D3DXMATRIX**](d3dxmatrix.md)\***</span></span>

<span data-ttu-id="7282c-112">來源 [**D3DXMATRIX**](d3dxmatrix.md) 結構的指標。</span><span class="sxs-lookup"><span data-stu-id="7282c-112">Pointer to a source [**D3DXMATRIX**](d3dxmatrix.md) structure.</span></span>

</dd> <dt>

<span data-ttu-id="7282c-113">*pM2* \[在\]</span><span class="sxs-lookup"><span data-stu-id="7282c-113">*pM2* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="7282c-114">Type： **Const [**D3DXMATRIX**](d3dxmatrix.md) \***</span><span class="sxs-lookup"><span data-stu-id="7282c-114">Type: **const [**D3DXMATRIX**](d3dxmatrix.md)\***</span></span>

<span data-ttu-id="7282c-115">來源 [**D3DXMATRIX**](d3dxmatrix.md) 結構的指標。</span><span class="sxs-lookup"><span data-stu-id="7282c-115">Pointer to a source [**D3DXMATRIX**](d3dxmatrix.md) structure.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="7282c-116">傳回值</span><span class="sxs-lookup"><span data-stu-id="7282c-116">Return value</span></span>

<span data-ttu-id="7282c-117">類型： **[ **D3DXMATRIX**](d3dxmatrix.md)\***</span><span class="sxs-lookup"><span data-stu-id="7282c-117">Type: **[**D3DXMATRIX**](d3dxmatrix.md)\***</span></span>

<span data-ttu-id="7282c-118">[**D3DXMATRIX**](d3dxmatrix.md)結構的指標，這是兩個矩陣的乘積。</span><span class="sxs-lookup"><span data-stu-id="7282c-118">Pointer to a [**D3DXMATRIX**](d3dxmatrix.md) structure that is the product of two matrices.</span></span>

## <a name="remarks"></a><span data-ttu-id="7282c-119">備註</span><span class="sxs-lookup"><span data-stu-id="7282c-119">Remarks</span></span>

<span data-ttu-id="7282c-120">結果會是兩個轉換矩陣的乘積，Out = T (M1 \* M2) 。</span><span class="sxs-lookup"><span data-stu-id="7282c-120">The result is the transposed of the product of two transformation matrices, Out = T(M1\*M2).</span></span>

<span data-ttu-id="7282c-121">此函式的傳回值與 *不悅* 參數中所傳回的值相同。</span><span class="sxs-lookup"><span data-stu-id="7282c-121">The return value for this function is the same value returned in the *pOut* parameter.</span></span> <span data-ttu-id="7282c-122">如此一來， **D3DXMatrixMultiplyTranspose** 函式就可以用來做為另一個函式的參數。</span><span class="sxs-lookup"><span data-stu-id="7282c-122">In this way, the **D3DXMatrixMultiplyTranspose** function can be used as a parameter for another function.</span></span>

<span data-ttu-id="7282c-123">此函數有助於將矩陣設定為頂點和圖元著色器的常數。</span><span class="sxs-lookup"><span data-stu-id="7282c-123">This function is useful to set matrices as constants for vertex and pixel shaders.</span></span>

## <a name="requirements"></a><span data-ttu-id="7282c-124">規格需求</span><span class="sxs-lookup"><span data-stu-id="7282c-124">Requirements</span></span>



| <span data-ttu-id="7282c-125">需求</span><span class="sxs-lookup"><span data-stu-id="7282c-125">Requirement</span></span> | <span data-ttu-id="7282c-126">值</span><span class="sxs-lookup"><span data-stu-id="7282c-126">Value</span></span> |
|--------------------|----------------------------------------------------------------------------------------|
| <span data-ttu-id="7282c-127">標頭</span><span class="sxs-lookup"><span data-stu-id="7282c-127">Header</span></span><br/>  | <dl> <span data-ttu-id="7282c-128"><dt>D3dx9math。h</dt></span><span class="sxs-lookup"><span data-stu-id="7282c-128"><dt>D3dx9math.h</dt></span></span> </dl> |
| <span data-ttu-id="7282c-129">程式庫</span><span class="sxs-lookup"><span data-stu-id="7282c-129">Library</span></span><br/> | <dl> <span data-ttu-id="7282c-130"><dt>D3dx9 .lib</dt></span><span class="sxs-lookup"><span data-stu-id="7282c-130"><dt>D3dx9.lib</dt></span></span> </dl>   |



## <a name="see-also"></a><span data-ttu-id="7282c-131">另請參閱</span><span class="sxs-lookup"><span data-stu-id="7282c-131">See also</span></span>

<dl> <dt>

[<span data-ttu-id="7282c-132">數學函數</span><span class="sxs-lookup"><span data-stu-id="7282c-132">Math Functions</span></span>](dx9-graphics-reference-d3dx-functions-math.md)
</dt> <dt>

[<span data-ttu-id="7282c-133">**D3DXMatrixMultiply**</span><span class="sxs-lookup"><span data-stu-id="7282c-133">**D3DXMatrixMultiply**</span></span>](d3dxmatrixmultiply.md)
</dt> <dt>

[<span data-ttu-id="7282c-134">**D3DXQuaternionMultiply**</span><span class="sxs-lookup"><span data-stu-id="7282c-134">**D3DXQuaternionMultiply**</span></span>](d3dxquaternionmultiply.md)
</dt> </dl>

 

 




