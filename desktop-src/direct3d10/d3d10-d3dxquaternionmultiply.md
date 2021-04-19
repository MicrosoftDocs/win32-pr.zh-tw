---
description: 將兩個四元數相乘。
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
ms.openlocfilehash: 74e10117bf27d922480418e5aa0b8ea60a13528c
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 03/15/2021
ms.locfileid: "106974881"
---
# <a name="d3dxquaternionmultiply-function-d3dx10mathh"></a><span data-ttu-id="654c3-103">D3DXQuaternionMultiply 函式 (D3DX10Math) </span><span class="sxs-lookup"><span data-stu-id="654c3-103">D3DXQuaternionMultiply function (D3DX10Math.h)</span></span>

<span data-ttu-id="654c3-104">將兩個四元數相乘。</span><span class="sxs-lookup"><span data-stu-id="654c3-104">Multiplies two quaternions.</span></span>

## <a name="syntax"></a><span data-ttu-id="654c3-105">語法</span><span class="sxs-lookup"><span data-stu-id="654c3-105">Syntax</span></span>


```C++
D3DXQUATERNION* D3DXQuaternionMultiply(
  _Inout_       D3DXQUATERNION *pOut,
  _In_    const D3DXQUATERNION *pQ1,
  _In_    const D3DXQUATERNION *pQ2
);
```



## <a name="parameters"></a><span data-ttu-id="654c3-106">參數</span><span class="sxs-lookup"><span data-stu-id="654c3-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="654c3-107">*不悅* \[in、out\]</span><span class="sxs-lookup"><span data-stu-id="654c3-107">*pOut* \[in, out\]</span></span>
</dt> <dd>

<span data-ttu-id="654c3-108">類型： **[ **D3DXQUATERNION**](d3d10-d3dxquaternion.md)\***</span><span class="sxs-lookup"><span data-stu-id="654c3-108">Type: **[**D3DXQUATERNION**](d3d10-d3dxquaternion.md)\***</span></span>

<span data-ttu-id="654c3-109">作業結果之 [**D3DXQUATERNION**](d3d10-d3dxquaternion.md) 的指標。</span><span class="sxs-lookup"><span data-stu-id="654c3-109">Pointer to the [**D3DXQUATERNION**](d3d10-d3dxquaternion.md) that is the result of the operation.</span></span>

</dd> <dt>

<span data-ttu-id="654c3-110">*pQ1* \[在\]</span><span class="sxs-lookup"><span data-stu-id="654c3-110">*pQ1* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="654c3-111">Type： **Const [**D3DXQUATERNION**](d3d10-d3dxquaternion.md) \***</span><span class="sxs-lookup"><span data-stu-id="654c3-111">Type: **const [**D3DXQUATERNION**](d3d10-d3dxquaternion.md)\***</span></span>

<span data-ttu-id="654c3-112">來源 [**D3DXQUATERNION**](d3d10-d3dxquaternion.md) 結構的指標。</span><span class="sxs-lookup"><span data-stu-id="654c3-112">Pointer to a source [**D3DXQUATERNION**](d3d10-d3dxquaternion.md) structure.</span></span>

</dd> <dt>

<span data-ttu-id="654c3-113">*pQ2* \[在\]</span><span class="sxs-lookup"><span data-stu-id="654c3-113">*pQ2* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="654c3-114">Type： **Const [**D3DXQUATERNION**](d3d10-d3dxquaternion.md) \***</span><span class="sxs-lookup"><span data-stu-id="654c3-114">Type: **const [**D3DXQUATERNION**](d3d10-d3dxquaternion.md)\***</span></span>

<span data-ttu-id="654c3-115">來源 [**D3DXQUATERNION**](d3d10-d3dxquaternion.md) 結構的指標。</span><span class="sxs-lookup"><span data-stu-id="654c3-115">Pointer to a source [**D3DXQUATERNION**](d3d10-d3dxquaternion.md) structure.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="654c3-116">傳回值</span><span class="sxs-lookup"><span data-stu-id="654c3-116">Return value</span></span>

<span data-ttu-id="654c3-117">類型： **[ **D3DXQUATERNION**](../direct3d9/d3dxquaternion.md)\***</span><span class="sxs-lookup"><span data-stu-id="654c3-117">Type: **[**D3DXQUATERNION**](../direct3d9/d3dxquaternion.md)\***</span></span>

<span data-ttu-id="654c3-118">[**D3DXQUATERNION**](d3d10-d3dxquaternion.md)結構的指標，這是兩個四元數的乘積。</span><span class="sxs-lookup"><span data-stu-id="654c3-118">Pointer to a [**D3DXQUATERNION**](d3d10-d3dxquaternion.md) structure that is the product of two quaternions.</span></span>

## <a name="remarks"></a><span data-ttu-id="654c3-119">備註</span><span class="sxs-lookup"><span data-stu-id="654c3-119">Remarks</span></span>

<span data-ttu-id="654c3-120">結果代表旋轉 Q1，後面接著旋轉 Q2 (Out = Q2 \* q1) 。</span><span class="sxs-lookup"><span data-stu-id="654c3-120">The result represents the rotation Q1 followed by the rotation Q2 (Out = Q2 \* Q1).</span></span> <span data-ttu-id="654c3-121">這樣做的目的是為了讓 **D3DXQuaternionMultiply** 維持與 [**D3DXMatrixMultiply**](d3d10-d3dxmatrixmultiply.md) 相同的語義，因為可以將單元四元數視為另一種表示旋轉矩陣的方式。</span><span class="sxs-lookup"><span data-stu-id="654c3-121">This is done so that **D3DXQuaternionMultiply** maintain the same semantics as [**D3DXMatrixMultiply**](d3d10-d3dxmatrixmultiply.md) because unit quaternions can be considered as another way to represent rotation matrices.</span></span>

<span data-ttu-id="654c3-122">**D3DXQuaternionMultiply** 和 [**D3DXMatrixMultiply**](d3d10-d3dxmatrixmultiply.md)函數的轉換會以相同順序串連。</span><span class="sxs-lookup"><span data-stu-id="654c3-122">Transformations are concatenated in the same order for both the **D3DXQuaternionMultiply** and [**D3DXMatrixMultiply**](d3d10-d3dxmatrixmultiply.md) Functions.</span></span> <span data-ttu-id="654c3-123">例如，假設 mX 和 mY 表示與 qX 和 qY 相同的旋轉，則 m 和 q 都代表相同的旋轉。</span><span class="sxs-lookup"><span data-stu-id="654c3-123">For example, assuming mX and mY represent the same rotations as qX and qY, both m and q will represent the same rotations.</span></span>


```
D3DXMatrixMultiply(&m, &mX, &mY);
D3DXQuaternionMultiply(&q, &qX, &qY);
```



<span data-ttu-id="654c3-124">四元數的乘法不是可交換的。</span><span class="sxs-lookup"><span data-stu-id="654c3-124">The multiplication of quaternions is not commutative.</span></span>

<span data-ttu-id="654c3-125">此函式的傳回值與不悅參數中所傳回的值相同。</span><span class="sxs-lookup"><span data-stu-id="654c3-125">The return value for this function is the same value returned in the pOut parameter.</span></span> <span data-ttu-id="654c3-126">如此一來， **D3DXQuaternionMultiply** 函式就可以用來做為另一個函式的參數。</span><span class="sxs-lookup"><span data-stu-id="654c3-126">In this way, the **D3DXQuaternionMultiply** function can be used as a parameter for another function.</span></span>

<span data-ttu-id="654c3-127">針對尚未正規化的任何四元數輸入，請使用 [**D3DXQuaternionNormalize**](d3d10-d3dxquaternionnormalize.md) 。</span><span class="sxs-lookup"><span data-stu-id="654c3-127">Use [**D3DXQuaternionNormalize**](d3d10-d3dxquaternionnormalize.md) for any quaternion input that is not already normalized.</span></span>

## <a name="requirements"></a><span data-ttu-id="654c3-128">規格需求</span><span class="sxs-lookup"><span data-stu-id="654c3-128">Requirements</span></span>



| <span data-ttu-id="654c3-129">需求</span><span class="sxs-lookup"><span data-stu-id="654c3-129">Requirement</span></span> | <span data-ttu-id="654c3-130">值</span><span class="sxs-lookup"><span data-stu-id="654c3-130">Value</span></span> |
|--------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="654c3-131">標頭</span><span class="sxs-lookup"><span data-stu-id="654c3-131">Header</span></span><br/>  | <dl> <span data-ttu-id="654c3-132"><dt>D3DX10Math。h</dt></span><span class="sxs-lookup"><span data-stu-id="654c3-132"><dt>D3DX10Math.h</dt></span></span> </dl> |
| <span data-ttu-id="654c3-133">程式庫</span><span class="sxs-lookup"><span data-stu-id="654c3-133">Library</span></span><br/> | <dl> <span data-ttu-id="654c3-134"><dt>D3DX10 .lib</dt></span><span class="sxs-lookup"><span data-stu-id="654c3-134"><dt>D3DX10.lib</dt></span></span> </dl>   |



## <a name="see-also"></a><span data-ttu-id="654c3-135">另請參閱</span><span class="sxs-lookup"><span data-stu-id="654c3-135">See also</span></span>

<dl> <dt>

[<span data-ttu-id="654c3-136">數學函數</span><span class="sxs-lookup"><span data-stu-id="654c3-136">Math Functions</span></span>](d3d10-graphics-reference-d3dx10-functions-math.md)
</dt> </dl>

 

 
