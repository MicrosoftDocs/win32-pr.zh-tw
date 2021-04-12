---
description: Conjugates 和 renormalizes 四元數。
ms.assetid: 25407a60-f7c0-4063-8d1d-2d6d03bdb217
title: 'D3DXQuaternionInverse 函式 (D3dx9math) '
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- D3DXQuaternionInverse
api_type:
- LibDef
api_location:
- d3dx9.lib
- d3dx9.dll
ms.openlocfilehash: b2f830b7f8f797e4ed94eb22b4c2a05c3bd3e4cd
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 03/15/2021
ms.locfileid: "104386503"
---
# <a name="d3dxquaternioninverse-function-d3dx9mathh"></a><span data-ttu-id="90217-103">D3DXQuaternionInverse 函式 (D3dx9math) </span><span class="sxs-lookup"><span data-stu-id="90217-103">D3DXQuaternionInverse function (D3dx9math.h)</span></span>

<span data-ttu-id="90217-104">Conjugates 和 renormalizes 四元數。</span><span class="sxs-lookup"><span data-stu-id="90217-104">Conjugates and renormalizes a quaternion.</span></span>

## <a name="syntax"></a><span data-ttu-id="90217-105">語法</span><span class="sxs-lookup"><span data-stu-id="90217-105">Syntax</span></span>


```C++
D3DXQUATERNION* D3DXQuaternionInverse(
  _Inout_       D3DXQUATERNION *pOut,
  _In_    const D3DXQUATERNION *pQ
);
```



## <a name="parameters"></a><span data-ttu-id="90217-106">參數</span><span class="sxs-lookup"><span data-stu-id="90217-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="90217-107">*不悅* \[in、out\]</span><span class="sxs-lookup"><span data-stu-id="90217-107">*pOut* \[in, out\]</span></span>
</dt> <dd>

<span data-ttu-id="90217-108">類型： **[ **D3DXQUATERNION**](d3dxquaternion.md)\***</span><span class="sxs-lookup"><span data-stu-id="90217-108">Type: **[**D3DXQUATERNION**](d3dxquaternion.md)\***</span></span>

<span data-ttu-id="90217-109">[**D3DXQUATERNION**](d3dxquaternion.md)結構的指標，此結構是作業的結果。</span><span class="sxs-lookup"><span data-stu-id="90217-109">Pointer to the [**D3DXQUATERNION**](d3dxquaternion.md) structure that is the result of the operation.</span></span>

</dd> <dt>

<span data-ttu-id="90217-110">*pQ* \[在\]</span><span class="sxs-lookup"><span data-stu-id="90217-110">*pQ* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="90217-111">Type： **Const [**D3DXQUATERNION**](d3dxquaternion.md) \***</span><span class="sxs-lookup"><span data-stu-id="90217-111">Type: **const [**D3DXQUATERNION**](d3dxquaternion.md)\***</span></span>

<span data-ttu-id="90217-112">來源 [**D3DXQUATERNION**](d3dxquaternion.md) 結構的指標。</span><span class="sxs-lookup"><span data-stu-id="90217-112">Pointer to the source [**D3DXQUATERNION**](d3dxquaternion.md) structure.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="90217-113">傳回值</span><span class="sxs-lookup"><span data-stu-id="90217-113">Return value</span></span>

<span data-ttu-id="90217-114">類型： **[ **D3DXQUATERNION**](d3dxquaternion.md)\***</span><span class="sxs-lookup"><span data-stu-id="90217-114">Type: **[**D3DXQUATERNION**](d3dxquaternion.md)\***</span></span>

<span data-ttu-id="90217-115">[**D3DXQUATERNION**](d3dxquaternion.md)結構的指標，此結構是四元數的反向四元數。</span><span class="sxs-lookup"><span data-stu-id="90217-115">Pointer to a [**D3DXQUATERNION**](d3dxquaternion.md) structure that is the inverse quaternion of the quaternion.</span></span>

## <a name="remarks"></a><span data-ttu-id="90217-116">備註</span><span class="sxs-lookup"><span data-stu-id="90217-116">Remarks</span></span>


```
A unit quaternion, is defined by:
Q == (cos(theta), sin(theta) * v) where |v| = 1
The natural logarithm of Q is, ln(Q) = (0, theta * v)
```



<span data-ttu-id="90217-117">此函式的傳回值與 *不悅* 參數中所傳回的值相同。</span><span class="sxs-lookup"><span data-stu-id="90217-117">The return value for this function is the same value returned in the *pOut* parameter.</span></span> <span data-ttu-id="90217-118">如此一來， **D3DXQuaternionInverse** 函式就可以用來做為另一個函式的參數。</span><span class="sxs-lookup"><span data-stu-id="90217-118">In this way, the **D3DXQuaternionInverse** function can be used as a parameter for another function.</span></span>

<span data-ttu-id="90217-119">針對尚未正規化的任何四元數輸入，請使用 [**D3DXQuaternionNormalize**](d3dxquaternionnormalize.md) 。</span><span class="sxs-lookup"><span data-stu-id="90217-119">Use [**D3DXQuaternionNormalize**](d3dxquaternionnormalize.md) for any quaternion input that is not already normalized.</span></span>

## <a name="requirements"></a><span data-ttu-id="90217-120">規格需求</span><span class="sxs-lookup"><span data-stu-id="90217-120">Requirements</span></span>



| <span data-ttu-id="90217-121">需求</span><span class="sxs-lookup"><span data-stu-id="90217-121">Requirement</span></span> | <span data-ttu-id="90217-122">值</span><span class="sxs-lookup"><span data-stu-id="90217-122">Value</span></span> |
|--------------------|----------------------------------------------------------------------------------------|
| <span data-ttu-id="90217-123">標頭</span><span class="sxs-lookup"><span data-stu-id="90217-123">Header</span></span><br/>  | <dl> <span data-ttu-id="90217-124"><dt>D3dx9math。h</dt></span><span class="sxs-lookup"><span data-stu-id="90217-124"><dt>D3dx9math.h</dt></span></span> </dl> |
| <span data-ttu-id="90217-125">程式庫</span><span class="sxs-lookup"><span data-stu-id="90217-125">Library</span></span><br/> | <dl> <span data-ttu-id="90217-126"><dt>D3dx9 .lib</dt></span><span class="sxs-lookup"><span data-stu-id="90217-126"><dt>D3dx9.lib</dt></span></span> </dl>   |



## <a name="see-also"></a><span data-ttu-id="90217-127">另請參閱</span><span class="sxs-lookup"><span data-stu-id="90217-127">See also</span></span>

<dl> <dt>

[<span data-ttu-id="90217-128">數學函數</span><span class="sxs-lookup"><span data-stu-id="90217-128">Math Functions</span></span>](dx9-graphics-reference-d3dx-functions-math.md)
</dt> <dt>

[<span data-ttu-id="90217-129">**D3DXQuaternionConjugate**</span><span class="sxs-lookup"><span data-stu-id="90217-129">**D3DXQuaternionConjugate**</span></span>](d3dxquaternionconjugate.md)
</dt> <dt>

[<span data-ttu-id="90217-130">**D3DXQuaternionNormalize**</span><span class="sxs-lookup"><span data-stu-id="90217-130">**D3DXQuaternionNormalize**</span></span>](d3dxquaternionnormalize.md)
</dt> </dl>

 

 




