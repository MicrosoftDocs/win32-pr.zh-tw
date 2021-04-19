---
description: 正規化平面係數，讓平面法線具有單位長度。
ms.assetid: 52ae36a7-e37b-457a-9832-e62900a85bde
title: 'D3DXPlaneNormalize 函式 (D3DX10Math) '
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- D3DXPlaneNormalize
api_type:
- LibDef
api_location:
- D3DX10.lib
- D3DX10.dll
ms.openlocfilehash: 44d5e9d810653b2cdae233dec803383c74563d08
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 03/15/2021
ms.locfileid: "106992743"
---
# <a name="d3dxplanenormalize-function-d3dx10mathh"></a><span data-ttu-id="4a5ae-103">D3DXPlaneNormalize 函式 (D3DX10Math) </span><span class="sxs-lookup"><span data-stu-id="4a5ae-103">D3DXPlaneNormalize function (D3DX10Math.h)</span></span>

<span data-ttu-id="4a5ae-104">正規化平面係數，讓平面法線具有單位長度。</span><span class="sxs-lookup"><span data-stu-id="4a5ae-104">Normalizes the plane coefficients so that the plane normal has unit length.</span></span>

## <a name="syntax"></a><span data-ttu-id="4a5ae-105">語法</span><span class="sxs-lookup"><span data-stu-id="4a5ae-105">Syntax</span></span>


```C++
D3DXPLANE* D3DXPlaneNormalize(
  _Inout_       D3DXPLANE *pOut,
  _In_    const D3DXPLANE *pP
);
```



## <a name="parameters"></a><span data-ttu-id="4a5ae-106">參數</span><span class="sxs-lookup"><span data-stu-id="4a5ae-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="4a5ae-107">*不悅* \[in、out\]</span><span class="sxs-lookup"><span data-stu-id="4a5ae-107">*pOut* \[in, out\]</span></span>
</dt> <dd>

<span data-ttu-id="4a5ae-108">類型： **[ **D3DXPLANE**](../direct3d9/d3dxplane.md)\***</span><span class="sxs-lookup"><span data-stu-id="4a5ae-108">Type: **[**D3DXPLANE**](../direct3d9/d3dxplane.md)\***</span></span>

<span data-ttu-id="4a5ae-109">作業結果之 [**D3DXPLANE**](d3d10-d3dxplane.md) 的指標。</span><span class="sxs-lookup"><span data-stu-id="4a5ae-109">Pointer to the [**D3DXPLANE**](d3d10-d3dxplane.md) that is the result of the operation.</span></span>

</dd> <dt>

<span data-ttu-id="4a5ae-110">*pP* \[在\]</span><span class="sxs-lookup"><span data-stu-id="4a5ae-110">*pP* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="4a5ae-111">Type： **Const [**D3DXPLANE**](../direct3d9/d3dxplane.md) \***</span><span class="sxs-lookup"><span data-stu-id="4a5ae-111">Type: **const [**D3DXPLANE**](../direct3d9/d3dxplane.md)\***</span></span>

<span data-ttu-id="4a5ae-112">來源 D3DXPLANE 結構的指標。</span><span class="sxs-lookup"><span data-stu-id="4a5ae-112">Pointer to the source D3DXPLANE structure.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="4a5ae-113">傳回值</span><span class="sxs-lookup"><span data-stu-id="4a5ae-113">Return value</span></span>

<span data-ttu-id="4a5ae-114">類型： **[ **D3DXPLANE**](../direct3d9/d3dxplane.md)\***</span><span class="sxs-lookup"><span data-stu-id="4a5ae-114">Type: **[**D3DXPLANE**](../direct3d9/d3dxplane.md)\***</span></span>

<span data-ttu-id="4a5ae-115">D3DXPLANE 結構的指標，代表平面的一般。</span><span class="sxs-lookup"><span data-stu-id="4a5ae-115">Pointer to a D3DXPLANE structure that represents the normal of the plane.</span></span>

## <a name="remarks"></a><span data-ttu-id="4a5ae-116">備註</span><span class="sxs-lookup"><span data-stu-id="4a5ae-116">Remarks</span></span>

<span data-ttu-id="4a5ae-117">此函式會將平面正規化，使 \| a、b、c \| = = 1。</span><span class="sxs-lookup"><span data-stu-id="4a5ae-117">This function normalizes a plane so that \|a,b,c\| == 1.</span></span>

<span data-ttu-id="4a5ae-118">此函式的傳回值與不悅參數中所傳回的值相同。</span><span class="sxs-lookup"><span data-stu-id="4a5ae-118">The return value for this function is the same value returned in the pOut parameter.</span></span> <span data-ttu-id="4a5ae-119">如此一來，此函式就可以用來做為另一個函式的參數。</span><span class="sxs-lookup"><span data-stu-id="4a5ae-119">In this way, this function can be used as a parameter for another function.</span></span>

## <a name="requirements"></a><span data-ttu-id="4a5ae-120">規格需求</span><span class="sxs-lookup"><span data-stu-id="4a5ae-120">Requirements</span></span>



| <span data-ttu-id="4a5ae-121">需求</span><span class="sxs-lookup"><span data-stu-id="4a5ae-121">Requirement</span></span> | <span data-ttu-id="4a5ae-122">值</span><span class="sxs-lookup"><span data-stu-id="4a5ae-122">Value</span></span> |
|--------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="4a5ae-123">標頭</span><span class="sxs-lookup"><span data-stu-id="4a5ae-123">Header</span></span><br/>  | <dl> <span data-ttu-id="4a5ae-124"><dt>D3DX10Math。h</dt></span><span class="sxs-lookup"><span data-stu-id="4a5ae-124"><dt>D3DX10Math.h</dt></span></span> </dl> |
| <span data-ttu-id="4a5ae-125">程式庫</span><span class="sxs-lookup"><span data-stu-id="4a5ae-125">Library</span></span><br/> | <dl> <span data-ttu-id="4a5ae-126"><dt>D3DX10 .lib</dt></span><span class="sxs-lookup"><span data-stu-id="4a5ae-126"><dt>D3DX10.lib</dt></span></span> </dl>   |



## <a name="see-also"></a><span data-ttu-id="4a5ae-127">另請參閱</span><span class="sxs-lookup"><span data-stu-id="4a5ae-127">See also</span></span>

<dl> <dt>

[<span data-ttu-id="4a5ae-128">數學函數</span><span class="sxs-lookup"><span data-stu-id="4a5ae-128">Math Functions</span></span>](d3d10-graphics-reference-d3dx10-functions-math.md)
</dt> </dl>

 

 
