---
description: D3DXQuaternionSlerp 函式 (D3DX10Math) -使用球面線性插補，在兩個四元數之間進行插補。
ms.assetid: 487e1df1-bf20-49cb-ad14-61fcf1300904
title: 'D3DXQuaternionSlerp 函式 (D3DX10Math) '
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- D3DXQuaternionSlerp
api_type:
- LibDef
api_location:
- D3DX10.lib
- D3DX10.dll
ms.openlocfilehash: 04cd3d82e4ca4e3f3357ab0114b57602f7e8a543
ms.sourcegitcommit: 95685061d5b0333bbf9e6ebd208dde8190f97005
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 04/28/2021
ms.locfileid: "108103116"
---
# <a name="d3dxquaternionslerp-function-d3dx10mathh"></a><span data-ttu-id="9d5b6-103">D3DXQuaternionSlerp 函式 (D3DX10Math) </span><span class="sxs-lookup"><span data-stu-id="9d5b6-103">D3DXQuaternionSlerp function (D3DX10Math.h)</span></span>

<span data-ttu-id="9d5b6-104">使用球面線性插補，在兩個四元數間進行插補。</span><span class="sxs-lookup"><span data-stu-id="9d5b6-104">Interpolates between two quaternions, using spherical linear interpolation.</span></span>

## <a name="syntax"></a><span data-ttu-id="9d5b6-105">語法</span><span class="sxs-lookup"><span data-stu-id="9d5b6-105">Syntax</span></span>


```C++
D3DXQUATERNION* D3DXQuaternionSlerp(
  _Inout_       D3DXQUATERNION *pOut,
  _In_    const D3DXQUATERNION *pQ1,
  _In_    const D3DXQUATERNION *pQ2,
  _In_          FLOAT          t
);
```



## <a name="parameters"></a><span data-ttu-id="9d5b6-106">參數</span><span class="sxs-lookup"><span data-stu-id="9d5b6-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="9d5b6-107">*不悅* \[in、out\]</span><span class="sxs-lookup"><span data-stu-id="9d5b6-107">*pOut* \[in, out\]</span></span>
</dt> <dd>

<span data-ttu-id="9d5b6-108">類型： **[ **D3DXQUATERNION**](../direct3d9/d3dxquaternion.md)\***</span><span class="sxs-lookup"><span data-stu-id="9d5b6-108">Type: **[**D3DXQUATERNION**](../direct3d9/d3dxquaternion.md)\***</span></span>

<span data-ttu-id="9d5b6-109">作業結果之 [**D3DXQUATERNION**](d3d10-d3dxquaternion.md) 的指標。</span><span class="sxs-lookup"><span data-stu-id="9d5b6-109">Pointer to the [**D3DXQUATERNION**](d3d10-d3dxquaternion.md) that is the result of the operation.</span></span>

</dd> <dt>

<span data-ttu-id="9d5b6-110">*pQ1* \[在\]</span><span class="sxs-lookup"><span data-stu-id="9d5b6-110">*pQ1* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="9d5b6-111">Type： **Const [**D3DXQUATERNION**](../direct3d9/d3dxquaternion.md) \***</span><span class="sxs-lookup"><span data-stu-id="9d5b6-111">Type: **const [**D3DXQUATERNION**](../direct3d9/d3dxquaternion.md)\***</span></span>

<span data-ttu-id="9d5b6-112">來源 D3DXQUATERNION 結構的指標。</span><span class="sxs-lookup"><span data-stu-id="9d5b6-112">Pointer to a source D3DXQUATERNION structure.</span></span>

</dd> <dt>

<span data-ttu-id="9d5b6-113">*pQ2* \[在\]</span><span class="sxs-lookup"><span data-stu-id="9d5b6-113">*pQ2* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="9d5b6-114">Type： **Const [**D3DXQUATERNION**](../direct3d9/d3dxquaternion.md) \***</span><span class="sxs-lookup"><span data-stu-id="9d5b6-114">Type: **const [**D3DXQUATERNION**](../direct3d9/d3dxquaternion.md)\***</span></span>

<span data-ttu-id="9d5b6-115">來源 D3DXQUATERNION 結構的指標。</span><span class="sxs-lookup"><span data-stu-id="9d5b6-115">Pointer to a source D3DXQUATERNION structure.</span></span>

</dd> <dt>

<span data-ttu-id="9d5b6-116"> \[ 中的 t\]</span><span class="sxs-lookup"><span data-stu-id="9d5b6-116">*t* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="9d5b6-117">類型： **[ **FLOAT**](../winprog/windows-data-types.md)**</span><span class="sxs-lookup"><span data-stu-id="9d5b6-117">Type: **[**FLOAT**](../winprog/windows-data-types.md)**</span></span>

<span data-ttu-id="9d5b6-118">指出在四元數之間插離的參數。</span><span class="sxs-lookup"><span data-stu-id="9d5b6-118">Parameter that indicates how far to interpolate between the quaternions.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="9d5b6-119">傳回值</span><span class="sxs-lookup"><span data-stu-id="9d5b6-119">Return value</span></span>

<span data-ttu-id="9d5b6-120">類型： **[ **D3DXQUATERNION**](../direct3d9/d3dxquaternion.md)\***</span><span class="sxs-lookup"><span data-stu-id="9d5b6-120">Type: **[**D3DXQUATERNION**](../direct3d9/d3dxquaternion.md)\***</span></span>

<span data-ttu-id="9d5b6-121">D3DXQUATERNION 結構的指標，此結構是插補的結果。</span><span class="sxs-lookup"><span data-stu-id="9d5b6-121">Pointer to a D3DXQUATERNION structure that is the result of the interpolation.</span></span>

## <a name="remarks"></a><span data-ttu-id="9d5b6-122">備註</span><span class="sxs-lookup"><span data-stu-id="9d5b6-122">Remarks</span></span>

<span data-ttu-id="9d5b6-123">此函式的傳回值與不悅參數中所傳回的值相同。</span><span class="sxs-lookup"><span data-stu-id="9d5b6-123">The return value for this function is the same value returned in the pOut parameter.</span></span> <span data-ttu-id="9d5b6-124">如此一來，D3DXQuaternionSlerp 函式就可以用來做為另一個函式的參數。</span><span class="sxs-lookup"><span data-stu-id="9d5b6-124">In this way, the D3DXQuaternionSlerp function can be used as a parameter for another function.</span></span>

<span data-ttu-id="9d5b6-125">針對尚未正規化的任何四元數輸入，請使用 [**D3DXQuaternionNormalize**](d3d10-d3dxquaternionnormalize.md) 。</span><span class="sxs-lookup"><span data-stu-id="9d5b6-125">Use [**D3DXQuaternionNormalize**](d3d10-d3dxquaternionnormalize.md) for any quaternion input that is not already normalized.</span></span>

## <a name="requirements"></a><span data-ttu-id="9d5b6-126">規格需求</span><span class="sxs-lookup"><span data-stu-id="9d5b6-126">Requirements</span></span>



| <span data-ttu-id="9d5b6-127">需求</span><span class="sxs-lookup"><span data-stu-id="9d5b6-127">Requirement</span></span> | <span data-ttu-id="9d5b6-128">值</span><span class="sxs-lookup"><span data-stu-id="9d5b6-128">Value</span></span> |
|--------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="9d5b6-129">標頭</span><span class="sxs-lookup"><span data-stu-id="9d5b6-129">Header</span></span><br/>  | <dl> <span data-ttu-id="9d5b6-130"><dt>D3DX10Math。h</dt></span><span class="sxs-lookup"><span data-stu-id="9d5b6-130"><dt>D3DX10Math.h</dt></span></span> </dl> |
| <span data-ttu-id="9d5b6-131">程式庫</span><span class="sxs-lookup"><span data-stu-id="9d5b6-131">Library</span></span><br/> | <dl> <span data-ttu-id="9d5b6-132"><dt>D3DX10 .lib</dt></span><span class="sxs-lookup"><span data-stu-id="9d5b6-132"><dt>D3DX10.lib</dt></span></span> </dl>   |



## <a name="see-also"></a><span data-ttu-id="9d5b6-133">另請參閱</span><span class="sxs-lookup"><span data-stu-id="9d5b6-133">See also</span></span>

<dl> <dt>

[<span data-ttu-id="9d5b6-134">數學函數</span><span class="sxs-lookup"><span data-stu-id="9d5b6-134">Math Functions</span></span>](d3d10-graphics-reference-d3dx10-functions-math.md)
</dt> </dl>

 

 
