---
description: D3DXPlaneNormalize 函式 (D3dx9math) -正規化平面係數，讓平面法線具有單位長度。
ms.assetid: 9c595986-e1f8-4153-ba23-1fa6e583a050
title: 'D3DXPlaneNormalize 函式 (D3dx9math) '
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
- d3dx9.lib
- d3dx9.dll
ms.openlocfilehash: d38ccbc3f688ed61779cf48a77e97dfb544c686e
ms.sourcegitcommit: 95685061d5b0333bbf9e6ebd208dde8190f97005
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 04/28/2021
ms.locfileid: "108094146"
---
# <a name="d3dxplanenormalize-function-d3dx9mathh"></a><span data-ttu-id="258d1-103">D3DXPlaneNormalize 函式 (D3dx9math) </span><span class="sxs-lookup"><span data-stu-id="258d1-103">D3DXPlaneNormalize function (D3dx9math.h)</span></span>

<span data-ttu-id="258d1-104">正規化平面係數，讓平面法線具有單位長度。</span><span class="sxs-lookup"><span data-stu-id="258d1-104">Normalizes the plane coefficients so that the plane normal has unit length.</span></span>

## <a name="syntax"></a><span data-ttu-id="258d1-105">語法</span><span class="sxs-lookup"><span data-stu-id="258d1-105">Syntax</span></span>


```C++
D3DXPLANE* D3DXPlaneNormalize(
  _Inout_       D3DXPLANE *pOut,
  _In_    const D3DXPLANE *pP
);
```



## <a name="parameters"></a><span data-ttu-id="258d1-106">參數</span><span class="sxs-lookup"><span data-stu-id="258d1-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="258d1-107">*不悅* \[in、out\]</span><span class="sxs-lookup"><span data-stu-id="258d1-107">*pOut* \[in, out\]</span></span>
</dt> <dd>

<span data-ttu-id="258d1-108">類型： **[ **D3DXPLANE**](d3dxplane.md)\***</span><span class="sxs-lookup"><span data-stu-id="258d1-108">Type: **[**D3DXPLANE**](d3dxplane.md)\***</span></span>

<span data-ttu-id="258d1-109">[**D3DXPLANE**](d3dxplane.md)結構的指標，此結構是作業的結果。</span><span class="sxs-lookup"><span data-stu-id="258d1-109">Pointer to the [**D3DXPLANE**](d3dxplane.md) structure that is the result of the operation.</span></span>

</dd> <dt>

<span data-ttu-id="258d1-110">*pP* \[在\]</span><span class="sxs-lookup"><span data-stu-id="258d1-110">*pP* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="258d1-111">Type： **Const [**D3DXPLANE**](d3dxplane.md) \***</span><span class="sxs-lookup"><span data-stu-id="258d1-111">Type: **const [**D3DXPLANE**](d3dxplane.md)\***</span></span>

<span data-ttu-id="258d1-112">來源 [**D3DXPLANE**](d3dxplane.md) 結構的指標。</span><span class="sxs-lookup"><span data-stu-id="258d1-112">Pointer to the source [**D3DXPLANE**](d3dxplane.md) structure.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="258d1-113">傳回值</span><span class="sxs-lookup"><span data-stu-id="258d1-113">Return value</span></span>

<span data-ttu-id="258d1-114">類型： **[ **D3DXPLANE**](d3dxplane.md)\***</span><span class="sxs-lookup"><span data-stu-id="258d1-114">Type: **[**D3DXPLANE**](d3dxplane.md)\***</span></span>

<span data-ttu-id="258d1-115">[**D3DXPLANE**](d3dxplane.md)結構的指標，代表平面的一般。</span><span class="sxs-lookup"><span data-stu-id="258d1-115">Pointer to a [**D3DXPLANE**](d3dxplane.md) structure that represents the normal of the plane.</span></span>

## <a name="remarks"></a><span data-ttu-id="258d1-116">備註</span><span class="sxs-lookup"><span data-stu-id="258d1-116">Remarks</span></span>

<span data-ttu-id="258d1-117">此函式會將平面正規化，使 \| a、b、c \| = = 1。</span><span class="sxs-lookup"><span data-stu-id="258d1-117">This function normalizes a plane so that \|a,b,c\| == 1.</span></span>

<span data-ttu-id="258d1-118">此函式的傳回值與 *不悅* 參數中所傳回的值相同。</span><span class="sxs-lookup"><span data-stu-id="258d1-118">The return value for this function is the same value returned in the *pOut* parameter.</span></span> <span data-ttu-id="258d1-119">如此一來，此函式就可以用來做為另一個函式的參數。</span><span class="sxs-lookup"><span data-stu-id="258d1-119">In this way, this function can be used as a parameter for another function.</span></span>

## <a name="requirements"></a><span data-ttu-id="258d1-120">規格需求</span><span class="sxs-lookup"><span data-stu-id="258d1-120">Requirements</span></span>



| <span data-ttu-id="258d1-121">需求</span><span class="sxs-lookup"><span data-stu-id="258d1-121">Requirement</span></span> | <span data-ttu-id="258d1-122">值</span><span class="sxs-lookup"><span data-stu-id="258d1-122">Value</span></span> |
|--------------------|----------------------------------------------------------------------------------------|
| <span data-ttu-id="258d1-123">標頭</span><span class="sxs-lookup"><span data-stu-id="258d1-123">Header</span></span><br/>  | <dl> <span data-ttu-id="258d1-124"><dt>D3dx9math。h</dt></span><span class="sxs-lookup"><span data-stu-id="258d1-124"><dt>D3dx9math.h</dt></span></span> </dl> |
| <span data-ttu-id="258d1-125">程式庫</span><span class="sxs-lookup"><span data-stu-id="258d1-125">Library</span></span><br/> | <dl> <span data-ttu-id="258d1-126"><dt>D3dx9 .lib</dt></span><span class="sxs-lookup"><span data-stu-id="258d1-126"><dt>D3dx9.lib</dt></span></span> </dl>   |



## <a name="see-also"></a><span data-ttu-id="258d1-127">另請參閱</span><span class="sxs-lookup"><span data-stu-id="258d1-127">See also</span></span>

<dl> <dt>

[<span data-ttu-id="258d1-128">數學函數</span><span class="sxs-lookup"><span data-stu-id="258d1-128">Math Functions</span></span>](dx9-graphics-reference-d3dx-functions-math.md)
</dt> </dl>

 

 




