---
description: D3DXQuaternionExp 函數 (D3dx9math) -計算指數。
ms.assetid: 648aeaf1-ead3-4b21-819f-cd2a70881a13
title: 'D3DXQuaternionExp 函式 (D3dx9math) '
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- D3DXQuaternionExp
api_type:
- LibDef
api_location:
- d3dx9.lib
- d3dx9.dll
ms.openlocfilehash: 30e48e21e2dc6af487f1fb076af3b3f2df57f9f3
ms.sourcegitcommit: 95685061d5b0333bbf9e6ebd208dde8190f97005
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 04/28/2021
ms.locfileid: "108094096"
---
# <a name="d3dxquaternionexp-function-d3dx9mathh"></a><span data-ttu-id="f8879-103">D3DXQuaternionExp 函式 (D3dx9math) </span><span class="sxs-lookup"><span data-stu-id="f8879-103">D3DXQuaternionExp function (D3dx9math.h)</span></span>

<span data-ttu-id="f8879-104">計算指數。</span><span class="sxs-lookup"><span data-stu-id="f8879-104">Calculates the exponential.</span></span>

## <a name="syntax"></a><span data-ttu-id="f8879-105">語法</span><span class="sxs-lookup"><span data-stu-id="f8879-105">Syntax</span></span>


```C++
D3DXQUATERNION* D3DXQuaternionExp(
  _Inout_       D3DXQUATERNION *pOut,
  _In_    const D3DXQUATERNION *pQ
);
```



## <a name="parameters"></a><span data-ttu-id="f8879-106">參數</span><span class="sxs-lookup"><span data-stu-id="f8879-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="f8879-107">*不悅* \[in、out\]</span><span class="sxs-lookup"><span data-stu-id="f8879-107">*pOut* \[in, out\]</span></span>
</dt> <dd>

<span data-ttu-id="f8879-108">類型： **[ **D3DXQUATERNION**](d3dxquaternion.md)\***</span><span class="sxs-lookup"><span data-stu-id="f8879-108">Type: **[**D3DXQUATERNION**](d3dxquaternion.md)\***</span></span>

<span data-ttu-id="f8879-109">[**D3DXQUATERNION**](d3dxquaternion.md)結構的指標，此結構是作業的結果。</span><span class="sxs-lookup"><span data-stu-id="f8879-109">Pointer to the [**D3DXQUATERNION**](d3dxquaternion.md) structure that is the result of the operation.</span></span>

</dd> <dt>

<span data-ttu-id="f8879-110">*pQ* \[在\]</span><span class="sxs-lookup"><span data-stu-id="f8879-110">*pQ* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="f8879-111">Type： **Const [**D3DXQUATERNION**](d3dxquaternion.md) \***</span><span class="sxs-lookup"><span data-stu-id="f8879-111">Type: **const [**D3DXQUATERNION**](d3dxquaternion.md)\***</span></span>

<span data-ttu-id="f8879-112">來源 [**D3DXQUATERNION**](d3dxquaternion.md) 結構的指標。</span><span class="sxs-lookup"><span data-stu-id="f8879-112">Pointer to the source [**D3DXQUATERNION**](d3dxquaternion.md) structure.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="f8879-113">傳回值</span><span class="sxs-lookup"><span data-stu-id="f8879-113">Return value</span></span>

<span data-ttu-id="f8879-114">類型： **[ **D3DXQUATERNION**](d3dxquaternion.md)\***</span><span class="sxs-lookup"><span data-stu-id="f8879-114">Type: **[**D3DXQUATERNION**](d3dxquaternion.md)\***</span></span>

<span data-ttu-id="f8879-115">[**D3DXQUATERNION**](d3dxquaternion.md)結構的指標，其為指數。</span><span class="sxs-lookup"><span data-stu-id="f8879-115">Pointer to a [**D3DXQUATERNION**](d3dxquaternion.md) structure that is the exponential.</span></span>

## <a name="remarks"></a><span data-ttu-id="f8879-116">備註</span><span class="sxs-lookup"><span data-stu-id="f8879-116">Remarks</span></span>

<span data-ttu-id="f8879-117">這個方法會將純四元數轉換成單位四元數。</span><span class="sxs-lookup"><span data-stu-id="f8879-117">This method converts a pure quaternion to a unit quaternion.</span></span> <span data-ttu-id="f8879-118">**D3DXQuaternionExp** 需要純四元數，其中 w 會忽略計算 (w = = 0) 。</span><span class="sxs-lookup"><span data-stu-id="f8879-118">**D3DXQuaternionExp** expects a pure quaternion, where w is ignored in the calculation (w == 0).</span></span>


```
Given a pure quaternion defined by:
q = (0, theta * v); 
    
This method calculates the exponential result.
exp(Q) = (cos(theta), sin(theta) * v)
```



<span data-ttu-id="f8879-119">其中 v 是四元數的向量部分。</span><span class="sxs-lookup"><span data-stu-id="f8879-119">where v is the vector portion of a quaternion.</span></span>

<span data-ttu-id="f8879-120">此函式的傳回值與 *不悅* 參數中所傳回的值相同。</span><span class="sxs-lookup"><span data-stu-id="f8879-120">The return value for this function is the same value returned in the *pOut* parameter.</span></span> <span data-ttu-id="f8879-121">如此一來， **D3DXQuaternionExp** 函式就可以用來做為另一個函式的參數。</span><span class="sxs-lookup"><span data-stu-id="f8879-121">In this way, the **D3DXQuaternionExp** function can be used as a parameter for another function.</span></span>

<span data-ttu-id="f8879-122">[**D3DXQuaternionSquadSetup**](d3dxquaternionsquadsetup.md)方法也可以用來設定四元數的控制點。</span><span class="sxs-lookup"><span data-stu-id="f8879-122">The [**D3DXQuaternionSquadSetup**](d3dxquaternionsquadsetup.md) method can also be used to set up the control points of a quaternion.</span></span>

<span data-ttu-id="f8879-123">針對尚未正規化的任何四元數輸入，請使用 [**D3DXQuaternionNormalize**](d3dxquaternionnormalize.md) 。</span><span class="sxs-lookup"><span data-stu-id="f8879-123">Use [**D3DXQuaternionNormalize**](d3dxquaternionnormalize.md) for any quaternion input that is not already normalized.</span></span>

## <a name="requirements"></a><span data-ttu-id="f8879-124">規格需求</span><span class="sxs-lookup"><span data-stu-id="f8879-124">Requirements</span></span>



| <span data-ttu-id="f8879-125">需求</span><span class="sxs-lookup"><span data-stu-id="f8879-125">Requirement</span></span> | <span data-ttu-id="f8879-126">值</span><span class="sxs-lookup"><span data-stu-id="f8879-126">Value</span></span> |
|--------------------|----------------------------------------------------------------------------------------|
| <span data-ttu-id="f8879-127">標頭</span><span class="sxs-lookup"><span data-stu-id="f8879-127">Header</span></span><br/>  | <dl> <span data-ttu-id="f8879-128"><dt>D3dx9math。h</dt></span><span class="sxs-lookup"><span data-stu-id="f8879-128"><dt>D3dx9math.h</dt></span></span> </dl> |
| <span data-ttu-id="f8879-129">程式庫</span><span class="sxs-lookup"><span data-stu-id="f8879-129">Library</span></span><br/> | <dl> <span data-ttu-id="f8879-130"><dt>D3dx9 .lib</dt></span><span class="sxs-lookup"><span data-stu-id="f8879-130"><dt>D3dx9.lib</dt></span></span> </dl>   |



## <a name="see-also"></a><span data-ttu-id="f8879-131">另請參閱</span><span class="sxs-lookup"><span data-stu-id="f8879-131">See also</span></span>

<dl> <dt>

[<span data-ttu-id="f8879-132">數學函數</span><span class="sxs-lookup"><span data-stu-id="f8879-132">Math Functions</span></span>](dx9-graphics-reference-d3dx-functions-math.md)
</dt> <dt>

[<span data-ttu-id="f8879-133">**D3DXQuaternionLn**</span><span class="sxs-lookup"><span data-stu-id="f8879-133">**D3DXQuaternionLn**</span></span>](d3dxquaternionln.md)
</dt> <dt>

[<span data-ttu-id="f8879-134">**D3DXQuaternionSquad**</span><span class="sxs-lookup"><span data-stu-id="f8879-134">**D3DXQuaternionSquad**</span></span>](d3dxquaternionsquad.md)
</dt> </dl>

 

 




