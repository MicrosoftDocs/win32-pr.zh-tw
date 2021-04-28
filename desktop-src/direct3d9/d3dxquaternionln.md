---
description: D3DXQuaternionLn 函數 (D3dx9math) -計算自然對數。
ms.assetid: 73ca7d13-1e20-48fc-b0ed-0d3127d094a7
title: 'D3DXQuaternionLn 函式 (D3dx9math) '
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- D3DXQuaternionLn
api_type:
- LibDef
api_location:
- d3dx9.lib
- d3dx9.dll
ms.openlocfilehash: d1a529c1c6ca4d7f81bf4d41fcdb4a7c7179874b
ms.sourcegitcommit: 95685061d5b0333bbf9e6ebd208dde8190f97005
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 04/28/2021
ms.locfileid: "108094056"
---
# <a name="d3dxquaternionln-function-d3dx9mathh"></a><span data-ttu-id="c8e7e-103">D3DXQuaternionLn 函式 (D3dx9math) </span><span class="sxs-lookup"><span data-stu-id="c8e7e-103">D3DXQuaternionLn function (D3dx9math.h)</span></span>

<span data-ttu-id="c8e7e-104">計算自然對數。</span><span class="sxs-lookup"><span data-stu-id="c8e7e-104">Calculates the natural logarithm.</span></span>

## <a name="syntax"></a><span data-ttu-id="c8e7e-105">語法</span><span class="sxs-lookup"><span data-stu-id="c8e7e-105">Syntax</span></span>


```C++
D3DXQUATERNION* D3DXQuaternionLn(
  _Inout_       D3DXQUATERNION *pOut,
  _In_    const D3DXQUATERNION *pQ
);
```



## <a name="parameters"></a><span data-ttu-id="c8e7e-106">參數</span><span class="sxs-lookup"><span data-stu-id="c8e7e-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="c8e7e-107">*不悅* \[in、out\]</span><span class="sxs-lookup"><span data-stu-id="c8e7e-107">*pOut* \[in, out\]</span></span>
</dt> <dd>

<span data-ttu-id="c8e7e-108">類型： **[ **D3DXQUATERNION**](d3dxquaternion.md)\***</span><span class="sxs-lookup"><span data-stu-id="c8e7e-108">Type: **[**D3DXQUATERNION**](d3dxquaternion.md)\***</span></span>

<span data-ttu-id="c8e7e-109">[**D3DXQUATERNION**](d3dxquaternion.md)結構的指標，此結構是作業的結果。</span><span class="sxs-lookup"><span data-stu-id="c8e7e-109">Pointer to the [**D3DXQUATERNION**](d3dxquaternion.md) structure that is the result of the operation.</span></span>

</dd> <dt>

<span data-ttu-id="c8e7e-110">*pQ* \[在\]</span><span class="sxs-lookup"><span data-stu-id="c8e7e-110">*pQ* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="c8e7e-111">Type： **Const [**D3DXQUATERNION**](d3dxquaternion.md) \***</span><span class="sxs-lookup"><span data-stu-id="c8e7e-111">Type: **const [**D3DXQUATERNION**](d3dxquaternion.md)\***</span></span>

<span data-ttu-id="c8e7e-112">來源 [**D3DXQUATERNION**](d3dxquaternion.md) 結構的指標。</span><span class="sxs-lookup"><span data-stu-id="c8e7e-112">Pointer to the source [**D3DXQUATERNION**](d3dxquaternion.md) structure.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="c8e7e-113">傳回值</span><span class="sxs-lookup"><span data-stu-id="c8e7e-113">Return value</span></span>

<span data-ttu-id="c8e7e-114">類型： **[ **D3DXQUATERNION**](d3dxquaternion.md)\***</span><span class="sxs-lookup"><span data-stu-id="c8e7e-114">Type: **[**D3DXQUATERNION**](d3dxquaternion.md)\***</span></span>

<span data-ttu-id="c8e7e-115">[**D3DXQUATERNION**](d3dxquaternion.md)結構的指標，此結構是自然對數。</span><span class="sxs-lookup"><span data-stu-id="c8e7e-115">Pointer to a [**D3DXQUATERNION**](d3dxquaternion.md) structure that is the natural logarithm.</span></span>

## <a name="remarks"></a><span data-ttu-id="c8e7e-116">備註</span><span class="sxs-lookup"><span data-stu-id="c8e7e-116">Remarks</span></span>

<span data-ttu-id="c8e7e-117">**D3DXQuaternionLn** 函數僅適用于單元四元數。</span><span class="sxs-lookup"><span data-stu-id="c8e7e-117">The **D3DXQuaternionLn** function works only for unit quaternions.</span></span>


```
A unit quaternion, is defined by:
Q == (cos(theta), sin(theta) * v) where |v| = 1
The natural logarithm of Q is, ln(Q) = (0, theta * v)
```



<span data-ttu-id="c8e7e-118">此函式的傳回值與 *不悅* 參數中所傳回的值相同。</span><span class="sxs-lookup"><span data-stu-id="c8e7e-118">The return value for this function is the same value returned in the *pOut* parameter.</span></span> <span data-ttu-id="c8e7e-119">如此一來， **D3DXQuaternionLn** 函式就可以用來做為另一個函式的參數。</span><span class="sxs-lookup"><span data-stu-id="c8e7e-119">In this way, the **D3DXQuaternionLn** function can be used as a parameter for another function.</span></span>

<span data-ttu-id="c8e7e-120">針對尚未正規化的任何四元數輸入，請使用 [**D3DXQuaternionNormalize**](d3dxquaternionnormalize.md) 。</span><span class="sxs-lookup"><span data-stu-id="c8e7e-120">Use [**D3DXQuaternionNormalize**](d3dxquaternionnormalize.md) for any quaternion input that is not already normalized.</span></span>

## <a name="requirements"></a><span data-ttu-id="c8e7e-121">規格需求</span><span class="sxs-lookup"><span data-stu-id="c8e7e-121">Requirements</span></span>



| <span data-ttu-id="c8e7e-122">需求</span><span class="sxs-lookup"><span data-stu-id="c8e7e-122">Requirement</span></span> | <span data-ttu-id="c8e7e-123">值</span><span class="sxs-lookup"><span data-stu-id="c8e7e-123">Value</span></span> |
|--------------------|----------------------------------------------------------------------------------------|
| <span data-ttu-id="c8e7e-124">標頭</span><span class="sxs-lookup"><span data-stu-id="c8e7e-124">Header</span></span><br/>  | <dl> <span data-ttu-id="c8e7e-125"><dt>D3dx9math。h</dt></span><span class="sxs-lookup"><span data-stu-id="c8e7e-125"><dt>D3dx9math.h</dt></span></span> </dl> |
| <span data-ttu-id="c8e7e-126">程式庫</span><span class="sxs-lookup"><span data-stu-id="c8e7e-126">Library</span></span><br/> | <dl> <span data-ttu-id="c8e7e-127"><dt>D3dx9 .lib</dt></span><span class="sxs-lookup"><span data-stu-id="c8e7e-127"><dt>D3dx9.lib</dt></span></span> </dl>   |



## <a name="see-also"></a><span data-ttu-id="c8e7e-128">另請參閱</span><span class="sxs-lookup"><span data-stu-id="c8e7e-128">See also</span></span>

<dl> <dt>

[<span data-ttu-id="c8e7e-129">數學函數</span><span class="sxs-lookup"><span data-stu-id="c8e7e-129">Math Functions</span></span>](dx9-graphics-reference-d3dx-functions-math.md)
</dt> <dt>

[<span data-ttu-id="c8e7e-130">**D3DXQuaternionExp**</span><span class="sxs-lookup"><span data-stu-id="c8e7e-130">**D3DXQuaternionExp**</span></span>](d3dxquaternionexp.md)
</dt> <dt>

[<span data-ttu-id="c8e7e-131">**D3DXQuaternionSquad**</span><span class="sxs-lookup"><span data-stu-id="c8e7e-131">**D3DXQuaternionSquad**</span></span>](d3dxquaternionsquad.md)
</dt> </dl>

 

 




