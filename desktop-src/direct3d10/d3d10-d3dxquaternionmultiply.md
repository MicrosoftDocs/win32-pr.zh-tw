---
description: D3DXQuaternionMultiply 函數 (D3DX10Math) -將兩個四元數相乘。
ms.assetid: f549e383-9c39-47a9-84e4-82365bdf1155
title: 'D3DXQuaternionMultiply 函式 (D3DX10Math) '
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- D3DXQuaternionMultiply
api_type:
- LibDef
api_location:
- D3DX10.lib
- D3DX10.dll
ms.openlocfilehash: 4f84ecac1eb910f4b3c97aba6ed42691c70b5b1f
ms.sourcegitcommit: 95685061d5b0333bbf9e6ebd208dde8190f97005
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 04/28/2021
ms.locfileid: "108103156"
---
# <a name="d3dxquaternionmultiply-function-d3dx10mathh"></a><span data-ttu-id="d2238-103">D3DXQuaternionMultiply 函式 (D3DX10Math) </span><span class="sxs-lookup"><span data-stu-id="d2238-103">D3DXQuaternionMultiply function (D3DX10Math.h)</span></span>

<span data-ttu-id="d2238-104">將兩個四元數相乘。</span><span class="sxs-lookup"><span data-stu-id="d2238-104">Multiplies two quaternions.</span></span>

## <a name="syntax"></a><span data-ttu-id="d2238-105">語法</span><span class="sxs-lookup"><span data-stu-id="d2238-105">Syntax</span></span>


```C++
D3DXQUATERNION* D3DXQuaternionMultiply(
  _Inout_       D3DXQUATERNION *pOut,
  _In_    const D3DXQUATERNION *pQ1,
  _In_    const D3DXQUATERNION *pQ2
);
```



## <a name="parameters"></a><span data-ttu-id="d2238-106">參數</span><span class="sxs-lookup"><span data-stu-id="d2238-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="d2238-107">*不悅* \[in、out\]</span><span class="sxs-lookup"><span data-stu-id="d2238-107">*pOut* \[in, out\]</span></span>
</dt> <dd>

<span data-ttu-id="d2238-108">類型： **[ **D3DXQUATERNION**](d3d10-d3dxquaternion.md)\***</span><span class="sxs-lookup"><span data-stu-id="d2238-108">Type: **[**D3DXQUATERNION**](d3d10-d3dxquaternion.md)\***</span></span>

<span data-ttu-id="d2238-109">作業結果之 [**D3DXQUATERNION**](d3d10-d3dxquaternion.md) 的指標。</span><span class="sxs-lookup"><span data-stu-id="d2238-109">Pointer to the [**D3DXQUATERNION**](d3d10-d3dxquaternion.md) that is the result of the operation.</span></span>

</dd> <dt>

<span data-ttu-id="d2238-110">*pQ1* \[在\]</span><span class="sxs-lookup"><span data-stu-id="d2238-110">*pQ1* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="d2238-111">Type： **Const [**D3DXQUATERNION**](d3d10-d3dxquaternion.md) \***</span><span class="sxs-lookup"><span data-stu-id="d2238-111">Type: **const [**D3DXQUATERNION**](d3d10-d3dxquaternion.md)\***</span></span>

<span data-ttu-id="d2238-112">來源 [**D3DXQUATERNION**](d3d10-d3dxquaternion.md) 結構的指標。</span><span class="sxs-lookup"><span data-stu-id="d2238-112">Pointer to a source [**D3DXQUATERNION**](d3d10-d3dxquaternion.md) structure.</span></span>

</dd> <dt>

<span data-ttu-id="d2238-113">*pQ2* \[在\]</span><span class="sxs-lookup"><span data-stu-id="d2238-113">*pQ2* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="d2238-114">Type： **Const [**D3DXQUATERNION**](d3d10-d3dxquaternion.md) \***</span><span class="sxs-lookup"><span data-stu-id="d2238-114">Type: **const [**D3DXQUATERNION**](d3d10-d3dxquaternion.md)\***</span></span>

<span data-ttu-id="d2238-115">來源 [**D3DXQUATERNION**](d3d10-d3dxquaternion.md) 結構的指標。</span><span class="sxs-lookup"><span data-stu-id="d2238-115">Pointer to a source [**D3DXQUATERNION**](d3d10-d3dxquaternion.md) structure.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="d2238-116">傳回值</span><span class="sxs-lookup"><span data-stu-id="d2238-116">Return value</span></span>

<span data-ttu-id="d2238-117">類型： **[ **D3DXQUATERNION**](../direct3d9/d3dxquaternion.md)\***</span><span class="sxs-lookup"><span data-stu-id="d2238-117">Type: **[**D3DXQUATERNION**](../direct3d9/d3dxquaternion.md)\***</span></span>

<span data-ttu-id="d2238-118">[**D3DXQUATERNION**](d3d10-d3dxquaternion.md)結構的指標，這是兩個四元數的乘積。</span><span class="sxs-lookup"><span data-stu-id="d2238-118">Pointer to a [**D3DXQUATERNION**](d3d10-d3dxquaternion.md) structure that is the product of two quaternions.</span></span>

## <a name="remarks"></a><span data-ttu-id="d2238-119">備註</span><span class="sxs-lookup"><span data-stu-id="d2238-119">Remarks</span></span>

<span data-ttu-id="d2238-120">結果代表旋轉 Q1，後面接著旋轉 Q2 (Out = Q2 \* q1) 。</span><span class="sxs-lookup"><span data-stu-id="d2238-120">The result represents the rotation Q1 followed by the rotation Q2 (Out = Q2 \* Q1).</span></span> <span data-ttu-id="d2238-121">這樣做的目的是為了讓 **D3DXQuaternionMultiply** 維持與 [**D3DXMatrixMultiply**](d3d10-d3dxmatrixmultiply.md) 相同的語義，因為可以將單元四元數視為另一種表示旋轉矩陣的方式。</span><span class="sxs-lookup"><span data-stu-id="d2238-121">This is done so that **D3DXQuaternionMultiply** maintain the same semantics as [**D3DXMatrixMultiply**](d3d10-d3dxmatrixmultiply.md) because unit quaternions can be considered as another way to represent rotation matrices.</span></span>

<span data-ttu-id="d2238-122">**D3DXQuaternionMultiply** 和 [**D3DXMatrixMultiply**](d3d10-d3dxmatrixmultiply.md)函數的轉換會以相同順序串連。</span><span class="sxs-lookup"><span data-stu-id="d2238-122">Transformations are concatenated in the same order for both the **D3DXQuaternionMultiply** and [**D3DXMatrixMultiply**](d3d10-d3dxmatrixmultiply.md) Functions.</span></span> <span data-ttu-id="d2238-123">例如，假設 mX 和 mY 表示與 qX 和 qY 相同的旋轉，則 m 和 q 都代表相同的旋轉。</span><span class="sxs-lookup"><span data-stu-id="d2238-123">For example, assuming mX and mY represent the same rotations as qX and qY, both m and q will represent the same rotations.</span></span>


```
D3DXMatrixMultiply(&m, &mX, &mY);
D3DXQuaternionMultiply(&q, &qX, &qY);
```



<span data-ttu-id="d2238-124">四元數的乘法不是可交換的。</span><span class="sxs-lookup"><span data-stu-id="d2238-124">The multiplication of quaternions is not commutative.</span></span>

<span data-ttu-id="d2238-125">此函式的傳回值與不悅參數中所傳回的值相同。</span><span class="sxs-lookup"><span data-stu-id="d2238-125">The return value for this function is the same value returned in the pOut parameter.</span></span> <span data-ttu-id="d2238-126">如此一來， **D3DXQuaternionMultiply** 函式就可以用來做為另一個函式的參數。</span><span class="sxs-lookup"><span data-stu-id="d2238-126">In this way, the **D3DXQuaternionMultiply** function can be used as a parameter for another function.</span></span>

<span data-ttu-id="d2238-127">針對尚未正規化的任何四元數輸入，請使用 [**D3DXQuaternionNormalize**](d3d10-d3dxquaternionnormalize.md) 。</span><span class="sxs-lookup"><span data-stu-id="d2238-127">Use [**D3DXQuaternionNormalize**](d3d10-d3dxquaternionnormalize.md) for any quaternion input that is not already normalized.</span></span>

## <a name="requirements"></a><span data-ttu-id="d2238-128">規格需求</span><span class="sxs-lookup"><span data-stu-id="d2238-128">Requirements</span></span>



| <span data-ttu-id="d2238-129">需求</span><span class="sxs-lookup"><span data-stu-id="d2238-129">Requirement</span></span> | <span data-ttu-id="d2238-130">值</span><span class="sxs-lookup"><span data-stu-id="d2238-130">Value</span></span> |
|--------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="d2238-131">標頭</span><span class="sxs-lookup"><span data-stu-id="d2238-131">Header</span></span><br/>  | <dl> <span data-ttu-id="d2238-132"><dt>D3DX10Math。h</dt></span><span class="sxs-lookup"><span data-stu-id="d2238-132"><dt>D3DX10Math.h</dt></span></span> </dl> |
| <span data-ttu-id="d2238-133">程式庫</span><span class="sxs-lookup"><span data-stu-id="d2238-133">Library</span></span><br/> | <dl> <span data-ttu-id="d2238-134"><dt>D3DX10 .lib</dt></span><span class="sxs-lookup"><span data-stu-id="d2238-134"><dt>D3DX10.lib</dt></span></span> </dl>   |



## <a name="see-also"></a><span data-ttu-id="d2238-135">另請參閱</span><span class="sxs-lookup"><span data-stu-id="d2238-135">See also</span></span>

<dl> <dt>

[<span data-ttu-id="d2238-136">數學函數</span><span class="sxs-lookup"><span data-stu-id="d2238-136">Math Functions</span></span>](d3d10-graphics-reference-d3dx10-functions-math.md)
</dt> </dl>

 

 
