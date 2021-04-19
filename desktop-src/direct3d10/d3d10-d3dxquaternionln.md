---
description: 計算自然對數。
ms.assetid: 576cf676-bb42-45ec-8e45-4612a7cdb167
title: 'D3DXQuaternionLn 函式 (D3DX10Math) '
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
- D3DX10.lib
- D3DX10.dll
ms.openlocfilehash: 07b081e0e2063d18ab8f2bb010e2b436c38df097
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 03/15/2021
ms.locfileid: "106986533"
---
# <a name="d3dxquaternionln-function-d3dx10mathh"></a><span data-ttu-id="5a73e-103">D3DXQuaternionLn 函式 (D3DX10Math) </span><span class="sxs-lookup"><span data-stu-id="5a73e-103">D3DXQuaternionLn function (D3DX10Math.h)</span></span>

<span data-ttu-id="5a73e-104">計算自然對數。</span><span class="sxs-lookup"><span data-stu-id="5a73e-104">Calculates the natural logarithm.</span></span>

## <a name="syntax"></a><span data-ttu-id="5a73e-105">語法</span><span class="sxs-lookup"><span data-stu-id="5a73e-105">Syntax</span></span>


```C++
D3DXQUATERNION* D3DXQuaternionLn(
  _Inout_       D3DXQUATERNION *pOut,
  _In_    const D3DXQUATERNION *pQ
);
```



## <a name="parameters"></a><span data-ttu-id="5a73e-106">參數</span><span class="sxs-lookup"><span data-stu-id="5a73e-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="5a73e-107">*不悅* \[in、out\]</span><span class="sxs-lookup"><span data-stu-id="5a73e-107">*pOut* \[in, out\]</span></span>
</dt> <dd>

<span data-ttu-id="5a73e-108">類型： **[ **D3DXQUATERNION**](../direct3d9/d3dxquaternion.md)\***</span><span class="sxs-lookup"><span data-stu-id="5a73e-108">Type: **[**D3DXQUATERNION**](../direct3d9/d3dxquaternion.md)\***</span></span>

<span data-ttu-id="5a73e-109">作業結果之 [**D3DXQUATERNION**](d3d10-d3dxquaternion.md) 的指標。</span><span class="sxs-lookup"><span data-stu-id="5a73e-109">Pointer to the [**D3DXQUATERNION**](d3d10-d3dxquaternion.md) that is the result of the operation.</span></span>

</dd> <dt>

<span data-ttu-id="5a73e-110">*pQ* \[在\]</span><span class="sxs-lookup"><span data-stu-id="5a73e-110">*pQ* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="5a73e-111">Type： **Const [**D3DXQUATERNION**](../direct3d9/d3dxquaternion.md) \***</span><span class="sxs-lookup"><span data-stu-id="5a73e-111">Type: **const [**D3DXQUATERNION**](../direct3d9/d3dxquaternion.md)\***</span></span>

<span data-ttu-id="5a73e-112">來源 D3DXQUATERNION 結構的指標。</span><span class="sxs-lookup"><span data-stu-id="5a73e-112">Pointer to the source D3DXQUATERNION structure.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="5a73e-113">傳回值</span><span class="sxs-lookup"><span data-stu-id="5a73e-113">Return value</span></span>

<span data-ttu-id="5a73e-114">類型： **[ **D3DXQUATERNION**](../direct3d9/d3dxquaternion.md)\***</span><span class="sxs-lookup"><span data-stu-id="5a73e-114">Type: **[**D3DXQUATERNION**](../direct3d9/d3dxquaternion.md)\***</span></span>

<span data-ttu-id="5a73e-115">D3DXQUATERNION 結構的指標，此結構是自然對數。</span><span class="sxs-lookup"><span data-stu-id="5a73e-115">Pointer to a D3DXQUATERNION structure that is the natural logarithm.</span></span>

## <a name="remarks"></a><span data-ttu-id="5a73e-116">備註</span><span class="sxs-lookup"><span data-stu-id="5a73e-116">Remarks</span></span>

<span data-ttu-id="5a73e-117">D3DXQuaternionLn 函數僅適用于單元四元數。</span><span class="sxs-lookup"><span data-stu-id="5a73e-117">The D3DXQuaternionLn function works only for unit quaternions.</span></span>


```
A unit quaternion, is defined by:
Q == (cos(theta), sin(theta) * v) where |v| = 1
The natural logarithm of Q is, ln(Q) = (0, theta * v)
```



<span data-ttu-id="5a73e-118">此函式的傳回值與不悅參數中所傳回的值相同。</span><span class="sxs-lookup"><span data-stu-id="5a73e-118">The return value for this function is the same value returned in the pOut parameter.</span></span> <span data-ttu-id="5a73e-119">如此一來，D3DXQuaternionLn 函式就可以用來做為另一個函式的參數。</span><span class="sxs-lookup"><span data-stu-id="5a73e-119">In this way, the D3DXQuaternionLn function can be used as a parameter for another function.</span></span>

<span data-ttu-id="5a73e-120">針對尚未正規化的任何四元數輸入，請使用 [**D3DXQuaternionNormalize**](d3d10-d3dxquaternionnormalize.md) 。</span><span class="sxs-lookup"><span data-stu-id="5a73e-120">Use [**D3DXQuaternionNormalize**](d3d10-d3dxquaternionnormalize.md) for any quaternion input that is not already normalized.</span></span>

## <a name="requirements"></a><span data-ttu-id="5a73e-121">規格需求</span><span class="sxs-lookup"><span data-stu-id="5a73e-121">Requirements</span></span>



| <span data-ttu-id="5a73e-122">需求</span><span class="sxs-lookup"><span data-stu-id="5a73e-122">Requirement</span></span> | <span data-ttu-id="5a73e-123">值</span><span class="sxs-lookup"><span data-stu-id="5a73e-123">Value</span></span> |
|--------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="5a73e-124">標頭</span><span class="sxs-lookup"><span data-stu-id="5a73e-124">Header</span></span><br/>  | <dl> <span data-ttu-id="5a73e-125"><dt>D3DX10Math。h</dt></span><span class="sxs-lookup"><span data-stu-id="5a73e-125"><dt>D3DX10Math.h</dt></span></span> </dl> |
| <span data-ttu-id="5a73e-126">程式庫</span><span class="sxs-lookup"><span data-stu-id="5a73e-126">Library</span></span><br/> | <dl> <span data-ttu-id="5a73e-127"><dt>D3DX10 .lib</dt></span><span class="sxs-lookup"><span data-stu-id="5a73e-127"><dt>D3DX10.lib</dt></span></span> </dl>   |



## <a name="see-also"></a><span data-ttu-id="5a73e-128">另請參閱</span><span class="sxs-lookup"><span data-stu-id="5a73e-128">See also</span></span>

<dl> <dt>

[<span data-ttu-id="5a73e-129">數學函數</span><span class="sxs-lookup"><span data-stu-id="5a73e-129">Math Functions</span></span>](d3d10-graphics-reference-d3dx10-functions-math.md)
</dt> </dl>

 

 
