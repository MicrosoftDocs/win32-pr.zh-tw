---
description: D3DXVec3Project 函式 (D3dx9math) -從物件空間將3D 向量投射到螢幕空間。
ms.assetid: b012771d-052f-4bf9-b39c-387d8a63fa59
title: 'D3DXVec3Project 函式 (D3dx9math) '
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- D3DXVec3Project
api_type:
- LibDef
api_location:
- d3dx9.lib
- d3dx9.dll
ms.openlocfilehash: a5a9abcb54c883d74bde831570b9df0b40fedfae
ms.sourcegitcommit: 95685061d5b0333bbf9e6ebd208dde8190f97005
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 04/28/2021
ms.locfileid: "108115646"
---
# <a name="d3dxvec3project-function-d3dx9mathh"></a><span data-ttu-id="4cc9b-103">D3DXVec3Project 函式 (D3dx9math) </span><span class="sxs-lookup"><span data-stu-id="4cc9b-103">D3DXVec3Project function (D3dx9math.h)</span></span>

<span data-ttu-id="4cc9b-104">將物件空間中的3D 向量投射到螢幕空間。</span><span class="sxs-lookup"><span data-stu-id="4cc9b-104">Projects a 3D vector from object space into screen space.</span></span>

## <a name="syntax"></a><span data-ttu-id="4cc9b-105">語法</span><span class="sxs-lookup"><span data-stu-id="4cc9b-105">Syntax</span></span>


```C++
D3DXVECTOR3* D3DXVec3Project(
  _Inout_       D3DXVECTOR3  *pOut,
  _In_    const D3DXVECTOR3  *pV,
  _In_    const D3DVIEWPORT9 *pViewport,
  _In_    const D3DXMATRIX   *pProjection,
  _In_    const D3DXMATRIX   *pView,
  _In_    const D3DXMATRIX   *pWorld
);
```



## <a name="parameters"></a><span data-ttu-id="4cc9b-106">參數</span><span class="sxs-lookup"><span data-stu-id="4cc9b-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="4cc9b-107">*不悅* \[in、out\]</span><span class="sxs-lookup"><span data-stu-id="4cc9b-107">*pOut* \[in, out\]</span></span>
</dt> <dd>

<span data-ttu-id="4cc9b-108">類型： **[ **D3DXVECTOR3**](d3dxvector3.md)\***</span><span class="sxs-lookup"><span data-stu-id="4cc9b-108">Type: **[**D3DXVECTOR3**](d3dxvector3.md)\***</span></span>

<span data-ttu-id="4cc9b-109">[**D3DXVECTOR3**](d3dxvector3.md)結構的指標，此結構是作業的結果。</span><span class="sxs-lookup"><span data-stu-id="4cc9b-109">Pointer to the [**D3DXVECTOR3**](d3dxvector3.md) structure that is the result of the operation.</span></span>

</dd> <dt>

<span data-ttu-id="4cc9b-110">*pV* \[在\]</span><span class="sxs-lookup"><span data-stu-id="4cc9b-110">*pV* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="4cc9b-111">Type： **Const [**D3DXVECTOR3**](d3dxvector3.md) \***</span><span class="sxs-lookup"><span data-stu-id="4cc9b-111">Type: **const [**D3DXVECTOR3**](d3dxvector3.md)\***</span></span>

<span data-ttu-id="4cc9b-112">來源 [**D3DXVECTOR3**](d3dxvector3.md) 結構的指標。</span><span class="sxs-lookup"><span data-stu-id="4cc9b-112">Pointer to the source [**D3DXVECTOR3**](d3dxvector3.md) structure.</span></span>

</dd> <dt>

<span data-ttu-id="4cc9b-113">*pViewport* \[在\]</span><span class="sxs-lookup"><span data-stu-id="4cc9b-113">*pViewport* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="4cc9b-114">Type： **Const [**D3DVIEWPORT9**](d3dviewport9.md) \***</span><span class="sxs-lookup"><span data-stu-id="4cc9b-114">Type: **const [**D3DVIEWPORT9**](d3dviewport9.md)\***</span></span>

<span data-ttu-id="4cc9b-115">[**D3DVIEWPORT9**](d3dviewport9.md)結構的指標，表示區。</span><span class="sxs-lookup"><span data-stu-id="4cc9b-115">Pointer to a [**D3DVIEWPORT9**](d3dviewport9.md) structure, representing the viewport.</span></span>

</dd> <dt>

<span data-ttu-id="4cc9b-116">*pProjection* \[在\]</span><span class="sxs-lookup"><span data-stu-id="4cc9b-116">*pProjection* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="4cc9b-117">Type： **Const [**D3DXMATRIX**](d3dxmatrix.md) \***</span><span class="sxs-lookup"><span data-stu-id="4cc9b-117">Type: **const [**D3DXMATRIX**](d3dxmatrix.md)\***</span></span>

<span data-ttu-id="4cc9b-118">[**D3DXMATRIX**](d3dxmatrix.md)結構的指標，表示投射矩陣。</span><span class="sxs-lookup"><span data-stu-id="4cc9b-118">Pointer to a [**D3DXMATRIX**](d3dxmatrix.md) structure, representing the projection matrix.</span></span>

</dd> <dt>

<span data-ttu-id="4cc9b-119">*pView* \[在\]</span><span class="sxs-lookup"><span data-stu-id="4cc9b-119">*pView* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="4cc9b-120">Type： **Const [**D3DXMATRIX**](d3dxmatrix.md) \***</span><span class="sxs-lookup"><span data-stu-id="4cc9b-120">Type: **const [**D3DXMATRIX**](d3dxmatrix.md)\***</span></span>

<span data-ttu-id="4cc9b-121">[**D3DXMATRIX**](d3dxmatrix.md)結構的指標，代表視圖矩陣。</span><span class="sxs-lookup"><span data-stu-id="4cc9b-121">Pointer to a [**D3DXMATRIX**](d3dxmatrix.md) structure, representing the view matrix.</span></span>

</dd> <dt>

<span data-ttu-id="4cc9b-122">*pWorld* \[在\]</span><span class="sxs-lookup"><span data-stu-id="4cc9b-122">*pWorld* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="4cc9b-123">Type： **Const [**D3DXMATRIX**](d3dxmatrix.md) \***</span><span class="sxs-lookup"><span data-stu-id="4cc9b-123">Type: **const [**D3DXMATRIX**](d3dxmatrix.md)\***</span></span>

<span data-ttu-id="4cc9b-124">[**D3DXMATRIX**](d3dxmatrix.md)結構的指標，代表世界矩陣。</span><span class="sxs-lookup"><span data-stu-id="4cc9b-124">Pointer to a [**D3DXMATRIX**](d3dxmatrix.md) structure, representing the world matrix.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="4cc9b-125">傳回值</span><span class="sxs-lookup"><span data-stu-id="4cc9b-125">Return value</span></span>

<span data-ttu-id="4cc9b-126">類型： **[ **D3DXVECTOR3**](d3dxvector3.md)\***</span><span class="sxs-lookup"><span data-stu-id="4cc9b-126">Type: **[**D3DXVECTOR3**](d3dxvector3.md)\***</span></span>

<span data-ttu-id="4cc9b-127">[**D3DXVECTOR3**](d3dxvector3.md)結構的指標，此結構是從物件空間到螢幕空間投射的向量。</span><span class="sxs-lookup"><span data-stu-id="4cc9b-127">Pointer to a [**D3DXVECTOR3**](d3dxvector3.md) structure that is the vector projected from object space to screen space.</span></span>

## <a name="remarks"></a><span data-ttu-id="4cc9b-128">備註</span><span class="sxs-lookup"><span data-stu-id="4cc9b-128">Remarks</span></span>

<span data-ttu-id="4cc9b-129">此函式的傳回值與 *不悅* 參數中所傳回的值相同。</span><span class="sxs-lookup"><span data-stu-id="4cc9b-129">The return value for this function is the same value returned in the *pOut* parameter.</span></span> <span data-ttu-id="4cc9b-130">如此一來， **D3DXVec3Project** 函式就可以用來做為另一個函式的參數。</span><span class="sxs-lookup"><span data-stu-id="4cc9b-130">In this way, the **D3DXVec3Project** function can be used as a parameter for another function.</span></span>

## <a name="requirements"></a><span data-ttu-id="4cc9b-131">規格需求</span><span class="sxs-lookup"><span data-stu-id="4cc9b-131">Requirements</span></span>



| <span data-ttu-id="4cc9b-132">需求</span><span class="sxs-lookup"><span data-stu-id="4cc9b-132">Requirement</span></span> | <span data-ttu-id="4cc9b-133">值</span><span class="sxs-lookup"><span data-stu-id="4cc9b-133">Value</span></span> |
|--------------------|----------------------------------------------------------------------------------------|
| <span data-ttu-id="4cc9b-134">標頭</span><span class="sxs-lookup"><span data-stu-id="4cc9b-134">Header</span></span><br/>  | <dl> <span data-ttu-id="4cc9b-135"><dt>D3dx9math。h</dt></span><span class="sxs-lookup"><span data-stu-id="4cc9b-135"><dt>D3dx9math.h</dt></span></span> </dl> |
| <span data-ttu-id="4cc9b-136">程式庫</span><span class="sxs-lookup"><span data-stu-id="4cc9b-136">Library</span></span><br/> | <dl> <span data-ttu-id="4cc9b-137"><dt>D3dx9 .lib</dt></span><span class="sxs-lookup"><span data-stu-id="4cc9b-137"><dt>D3dx9.lib</dt></span></span> </dl>   |



## <a name="see-also"></a><span data-ttu-id="4cc9b-138">另請參閱</span><span class="sxs-lookup"><span data-stu-id="4cc9b-138">See also</span></span>

<dl> <dt>

[<span data-ttu-id="4cc9b-139">數學函數</span><span class="sxs-lookup"><span data-stu-id="4cc9b-139">Math Functions</span></span>](dx9-graphics-reference-d3dx-functions-math.md)
</dt> <dt>

[<span data-ttu-id="4cc9b-140">**D3DXVec3Unproject**</span><span class="sxs-lookup"><span data-stu-id="4cc9b-140">**D3DXVec3Unproject**</span></span>](d3dxvec3unproject.md)
</dt> </dl>

 

 




