---
description: D3DXQuaternionNormalize 函數 (D3DX10Math) -計算單位長度四元數。
ms.assetid: 6735a632-64d7-4bc1-b63e-d0cd27f5a29b
title: 'D3DXQuaternionNormalize 函式 (D3DX10Math) '
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- D3DXQuaternionNormalize
api_type:
- LibDef
api_location:
- D3DX10.lib
- D3DX10.dll
ms.openlocfilehash: 6d031dfc63cb92d43a9cca27813c9425e2ff1acb
ms.sourcegitcommit: 95685061d5b0333bbf9e6ebd208dde8190f97005
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 04/28/2021
ms.locfileid: "108103136"
---
# <a name="d3dxquaternionnormalize-function-d3dx10mathh"></a><span data-ttu-id="6ceb3-103">D3DXQuaternionNormalize 函式 (D3DX10Math) </span><span class="sxs-lookup"><span data-stu-id="6ceb3-103">D3DXQuaternionNormalize function (D3DX10Math.h)</span></span>

<span data-ttu-id="6ceb3-104">計算單位長度四元數。</span><span class="sxs-lookup"><span data-stu-id="6ceb3-104">Computes a unit length quaternion.</span></span>

## <a name="syntax"></a><span data-ttu-id="6ceb3-105">語法</span><span class="sxs-lookup"><span data-stu-id="6ceb3-105">Syntax</span></span>


```C++
D3DXQUATERNION* D3DXQuaternionNormalize(
  _Inout_       D3DXQUATERNION *pOut,
  _In_    const D3DXQUATERNION *pQ
);
```



## <a name="parameters"></a><span data-ttu-id="6ceb3-106">參數</span><span class="sxs-lookup"><span data-stu-id="6ceb3-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="6ceb3-107">*不悅* \[in、out\]</span><span class="sxs-lookup"><span data-stu-id="6ceb3-107">*pOut* \[in, out\]</span></span>
</dt> <dd>

<span data-ttu-id="6ceb3-108">類型： **[ **D3DXQUATERNION**](../direct3d9/d3dxquaternion.md)\***</span><span class="sxs-lookup"><span data-stu-id="6ceb3-108">Type: **[**D3DXQUATERNION**](../direct3d9/d3dxquaternion.md)\***</span></span>

<span data-ttu-id="6ceb3-109">作業結果之 [**D3DXQUATERNION**](d3d10-d3dxquaternion.md) 的指標。</span><span class="sxs-lookup"><span data-stu-id="6ceb3-109">Pointer to the [**D3DXQUATERNION**](d3d10-d3dxquaternion.md) that is the result of the operation.</span></span>

</dd> <dt>

<span data-ttu-id="6ceb3-110">*pQ* \[在\]</span><span class="sxs-lookup"><span data-stu-id="6ceb3-110">*pQ* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="6ceb3-111">Type： **Const [**D3DXQUATERNION**](../direct3d9/d3dxquaternion.md) \***</span><span class="sxs-lookup"><span data-stu-id="6ceb3-111">Type: **const [**D3DXQUATERNION**](../direct3d9/d3dxquaternion.md)\***</span></span>

<span data-ttu-id="6ceb3-112">來源 D3DXQUATERNION 結構的指標。</span><span class="sxs-lookup"><span data-stu-id="6ceb3-112">Pointer to the source D3DXQUATERNION structure.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="6ceb3-113">傳回值</span><span class="sxs-lookup"><span data-stu-id="6ceb3-113">Return value</span></span>

<span data-ttu-id="6ceb3-114">類型： **[ **D3DXQUATERNION**](../direct3d9/d3dxquaternion.md)\***</span><span class="sxs-lookup"><span data-stu-id="6ceb3-114">Type: **[**D3DXQUATERNION**](../direct3d9/d3dxquaternion.md)\***</span></span>

<span data-ttu-id="6ceb3-115">D3DXQUATERNION 結構的指標，此結構是四元數的標準。</span><span class="sxs-lookup"><span data-stu-id="6ceb3-115">Pointer to a D3DXQUATERNION structure that is the normal of the quaternion.</span></span>

## <a name="remarks"></a><span data-ttu-id="6ceb3-116">備註</span><span class="sxs-lookup"><span data-stu-id="6ceb3-116">Remarks</span></span>

<span data-ttu-id="6ceb3-117">此函式的傳回值與不悅參數中所傳回的值相同。</span><span class="sxs-lookup"><span data-stu-id="6ceb3-117">The return value for this function is the same value returned in the pOut parameter.</span></span> <span data-ttu-id="6ceb3-118">如此一來，D3DXQuaternionNormalize 函式就可以用來做為另一個函式的參數。</span><span class="sxs-lookup"><span data-stu-id="6ceb3-118">In this way, the D3DXQuaternionNormalize function can be used as a parameter for another function.</span></span>

## <a name="requirements"></a><span data-ttu-id="6ceb3-119">規格需求</span><span class="sxs-lookup"><span data-stu-id="6ceb3-119">Requirements</span></span>



| <span data-ttu-id="6ceb3-120">需求</span><span class="sxs-lookup"><span data-stu-id="6ceb3-120">Requirement</span></span> | <span data-ttu-id="6ceb3-121">值</span><span class="sxs-lookup"><span data-stu-id="6ceb3-121">Value</span></span> |
|--------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="6ceb3-122">標頭</span><span class="sxs-lookup"><span data-stu-id="6ceb3-122">Header</span></span><br/>  | <dl> <span data-ttu-id="6ceb3-123"><dt>D3DX10Math。h</dt></span><span class="sxs-lookup"><span data-stu-id="6ceb3-123"><dt>D3DX10Math.h</dt></span></span> </dl> |
| <span data-ttu-id="6ceb3-124">程式庫</span><span class="sxs-lookup"><span data-stu-id="6ceb3-124">Library</span></span><br/> | <dl> <span data-ttu-id="6ceb3-125"><dt>D3DX10 .lib</dt></span><span class="sxs-lookup"><span data-stu-id="6ceb3-125"><dt>D3DX10.lib</dt></span></span> </dl>   |



## <a name="see-also"></a><span data-ttu-id="6ceb3-126">另請參閱</span><span class="sxs-lookup"><span data-stu-id="6ceb3-126">See also</span></span>

<dl> <dt>

[<span data-ttu-id="6ceb3-127">數學函數</span><span class="sxs-lookup"><span data-stu-id="6ceb3-127">Math Functions</span></span>](d3d10-graphics-reference-d3dx10-functions-math.md)
</dt> </dl>

 

 
