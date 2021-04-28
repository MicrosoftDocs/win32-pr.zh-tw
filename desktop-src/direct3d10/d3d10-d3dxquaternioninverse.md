---
description: D3DXQuaternionInverse 函數 (D3DX10Math) -Conjugates 和 renormalizes 四元數。
ms.assetid: 8e1bba91-8895-43a2-805b-1368050f8e82
title: 'D3DXQuaternionInverse 函式 (D3DX10Math) '
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
- D3DX10.lib
- D3DX10.dll
ms.openlocfilehash: 84816ac72841dcda0aef726535b7f5219d5467e4
ms.sourcegitcommit: 95685061d5b0333bbf9e6ebd208dde8190f97005
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 04/28/2021
ms.locfileid: "108103196"
---
# <a name="d3dxquaternioninverse-function-d3dx10mathh"></a><span data-ttu-id="a7f7f-103">D3DXQuaternionInverse 函式 (D3DX10Math) </span><span class="sxs-lookup"><span data-stu-id="a7f7f-103">D3DXQuaternionInverse function (D3DX10Math.h)</span></span>

<span data-ttu-id="a7f7f-104">Conjugates 和 renormalizes 四元數。</span><span class="sxs-lookup"><span data-stu-id="a7f7f-104">Conjugates and renormalizes a quaternion.</span></span>

## <a name="syntax"></a><span data-ttu-id="a7f7f-105">語法</span><span class="sxs-lookup"><span data-stu-id="a7f7f-105">Syntax</span></span>


```C++
D3DXQUATERNION* D3DXQuaternionInverse(
  _Inout_       D3DXQUATERNION *pOut,
  _In_    const D3DXQUATERNION *pQ
);
```



## <a name="parameters"></a><span data-ttu-id="a7f7f-106">參數</span><span class="sxs-lookup"><span data-stu-id="a7f7f-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="a7f7f-107">*不悅* \[in、out\]</span><span class="sxs-lookup"><span data-stu-id="a7f7f-107">*pOut* \[in, out\]</span></span>
</dt> <dd>

<span data-ttu-id="a7f7f-108">類型： **[ **D3DXQUATERNION**](../direct3d9/d3dxquaternion.md)\***</span><span class="sxs-lookup"><span data-stu-id="a7f7f-108">Type: **[**D3DXQUATERNION**](../direct3d9/d3dxquaternion.md)\***</span></span>

<span data-ttu-id="a7f7f-109">作業結果之 [**D3DXQUATERNION**](d3d10-d3dxquaternion.md) 的指標。</span><span class="sxs-lookup"><span data-stu-id="a7f7f-109">Pointer to the [**D3DXQUATERNION**](d3d10-d3dxquaternion.md) that is the result of the operation.</span></span>

</dd> <dt>

<span data-ttu-id="a7f7f-110">*pQ* \[在\]</span><span class="sxs-lookup"><span data-stu-id="a7f7f-110">*pQ* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="a7f7f-111">Type： **Const [**D3DXQUATERNION**](../direct3d9/d3dxquaternion.md) \***</span><span class="sxs-lookup"><span data-stu-id="a7f7f-111">Type: **const [**D3DXQUATERNION**](../direct3d9/d3dxquaternion.md)\***</span></span>

<span data-ttu-id="a7f7f-112">來源 D3DXQUATERNION 結構的指標。</span><span class="sxs-lookup"><span data-stu-id="a7f7f-112">Pointer to the source D3DXQUATERNION structure.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="a7f7f-113">傳回值</span><span class="sxs-lookup"><span data-stu-id="a7f7f-113">Return value</span></span>

<span data-ttu-id="a7f7f-114">類型： **[ **D3DXQUATERNION**](../direct3d9/d3dxquaternion.md)\***</span><span class="sxs-lookup"><span data-stu-id="a7f7f-114">Type: **[**D3DXQUATERNION**](../direct3d9/d3dxquaternion.md)\***</span></span>

<span data-ttu-id="a7f7f-115">D3DXQUATERNION 結構的指標，此結構是四元數的反向四元數。</span><span class="sxs-lookup"><span data-stu-id="a7f7f-115">Pointer to a D3DXQUATERNION structure that is the inverse quaternion of the quaternion.</span></span>

## <a name="remarks"></a><span data-ttu-id="a7f7f-116">備註</span><span class="sxs-lookup"><span data-stu-id="a7f7f-116">Remarks</span></span>


```
A unit quaternion, is defined by:
Q == (cos(theta), sin(theta) * v) where |v| = 1
The natural logarithm of Q is, ln(Q) = (0, theta * v)
```



<span data-ttu-id="a7f7f-117">此函式的傳回值與不悅參數中所傳回的值相同。</span><span class="sxs-lookup"><span data-stu-id="a7f7f-117">The return value for this function is the same value returned in the pOut parameter.</span></span> <span data-ttu-id="a7f7f-118">如此一來，D3DXQuaternionInverse 函式就可以用來做為另一個函式的參數。</span><span class="sxs-lookup"><span data-stu-id="a7f7f-118">In this way, the D3DXQuaternionInverse function can be used as a parameter for another function.</span></span>

<span data-ttu-id="a7f7f-119">針對尚未正規化的任何四元數輸入，請使用 [**D3DXQuaternionNormalize**](d3d10-d3dxquaternionnormalize.md) 。</span><span class="sxs-lookup"><span data-stu-id="a7f7f-119">Use [**D3DXQuaternionNormalize**](d3d10-d3dxquaternionnormalize.md) for any quaternion input that is not already normalized.</span></span>

## <a name="requirements"></a><span data-ttu-id="a7f7f-120">規格需求</span><span class="sxs-lookup"><span data-stu-id="a7f7f-120">Requirements</span></span>



| <span data-ttu-id="a7f7f-121">需求</span><span class="sxs-lookup"><span data-stu-id="a7f7f-121">Requirement</span></span> | <span data-ttu-id="a7f7f-122">值</span><span class="sxs-lookup"><span data-stu-id="a7f7f-122">Value</span></span> |
|--------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="a7f7f-123">標頭</span><span class="sxs-lookup"><span data-stu-id="a7f7f-123">Header</span></span><br/>  | <dl> <span data-ttu-id="a7f7f-124"><dt>D3DX10Math。h</dt></span><span class="sxs-lookup"><span data-stu-id="a7f7f-124"><dt>D3DX10Math.h</dt></span></span> </dl> |
| <span data-ttu-id="a7f7f-125">程式庫</span><span class="sxs-lookup"><span data-stu-id="a7f7f-125">Library</span></span><br/> | <dl> <span data-ttu-id="a7f7f-126"><dt>D3DX10 .lib</dt></span><span class="sxs-lookup"><span data-stu-id="a7f7f-126"><dt>D3DX10.lib</dt></span></span> </dl>   |



## <a name="see-also"></a><span data-ttu-id="a7f7f-127">另請參閱</span><span class="sxs-lookup"><span data-stu-id="a7f7f-127">See also</span></span>

<dl> <dt>

[<span data-ttu-id="a7f7f-128">數學函數</span><span class="sxs-lookup"><span data-stu-id="a7f7f-128">Math Functions</span></span>](d3d10-graphics-reference-d3dx10-functions-math.md)
</dt> </dl>

 

 
