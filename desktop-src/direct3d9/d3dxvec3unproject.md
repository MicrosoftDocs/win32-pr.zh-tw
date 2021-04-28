---
description: D3DXVec3Unproject 函式 (D3dx9math) -將螢幕空間的向量投射到物件空間。
ms.assetid: 9fd69cae-1d9c-4fae-9e15-8eb9950b4850
title: 'D3DXVec3Unproject 函式 (D3dx9math) '
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- D3DXVec3Unproject
api_type:
- LibDef
api_location:
- d3dx9.lib
- d3dx9.dll
ms.openlocfilehash: 2c3ea6ec1aa60f48589b10575e279bed81b2c94f
ms.sourcegitcommit: 95685061d5b0333bbf9e6ebd208dde8190f97005
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 04/28/2021
ms.locfileid: "108115556"
---
# <a name="d3dxvec3unproject-function-d3dx9mathh"></a><span data-ttu-id="2ff2f-103">D3DXVec3Unproject 函式 (D3dx9math) </span><span class="sxs-lookup"><span data-stu-id="2ff2f-103">D3DXVec3Unproject function (D3dx9math.h)</span></span>

<span data-ttu-id="2ff2f-104">從螢幕空間將向量投射到物件空間。</span><span class="sxs-lookup"><span data-stu-id="2ff2f-104">Projects a vector from screen space into object space.</span></span>

## <a name="syntax"></a><span data-ttu-id="2ff2f-105">語法</span><span class="sxs-lookup"><span data-stu-id="2ff2f-105">Syntax</span></span>


```C++
D3DXVECTOR3* D3DXVec3Unproject(
  _Inout_       D3DXVECTOR3  *pOut,
  _In_    const D3DXVECTOR3  *pV,
  _In_    const D3DVIEWPORT9 *pViewport,
  _In_    const D3DXMATRIX   *pProjection,
  _In_    const D3DXMATRIX   *pView,
  _In_    const D3DXMATRIX   *pWorld
);
```



## <a name="parameters"></a><span data-ttu-id="2ff2f-106">參數</span><span class="sxs-lookup"><span data-stu-id="2ff2f-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="2ff2f-107">*不悅* \[in、out\]</span><span class="sxs-lookup"><span data-stu-id="2ff2f-107">*pOut* \[in, out\]</span></span>
</dt> <dd>

<span data-ttu-id="2ff2f-108">類型： **[ **D3DXVECTOR3**](d3dxvector3.md)\***</span><span class="sxs-lookup"><span data-stu-id="2ff2f-108">Type: **[**D3DXVECTOR3**](d3dxvector3.md)\***</span></span>

<span data-ttu-id="2ff2f-109">[**D3DXVECTOR3**](d3dxvector3.md)結構的指標，此結構是作業的結果。</span><span class="sxs-lookup"><span data-stu-id="2ff2f-109">Pointer to the [**D3DXVECTOR3**](d3dxvector3.md) structure that is the result of the operation.</span></span>

</dd> <dt>

<span data-ttu-id="2ff2f-110">*pV* \[在\]</span><span class="sxs-lookup"><span data-stu-id="2ff2f-110">*pV* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="2ff2f-111">Type： **Const [**D3DXVECTOR3**](d3dxvector3.md) \***</span><span class="sxs-lookup"><span data-stu-id="2ff2f-111">Type: **const [**D3DXVECTOR3**](d3dxvector3.md)\***</span></span>

<span data-ttu-id="2ff2f-112">來源 [**D3DXVECTOR3**](d3dxvector3.md) 結構的指標。</span><span class="sxs-lookup"><span data-stu-id="2ff2f-112">Pointer to the source [**D3DXVECTOR3**](d3dxvector3.md) structure.</span></span>

</dd> <dt>

<span data-ttu-id="2ff2f-113">*pViewport* \[在\]</span><span class="sxs-lookup"><span data-stu-id="2ff2f-113">*pViewport* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="2ff2f-114">Type： **Const [**D3DVIEWPORT9**](d3dviewport9.md) \***</span><span class="sxs-lookup"><span data-stu-id="2ff2f-114">Type: **const [**D3DVIEWPORT9**](d3dviewport9.md)\***</span></span>

<span data-ttu-id="2ff2f-115">[**D3DVIEWPORT9**](d3dviewport9.md)結構的指標，表示區。</span><span class="sxs-lookup"><span data-stu-id="2ff2f-115">Pointer to a [**D3DVIEWPORT9**](d3dviewport9.md) structure, representing the viewport.</span></span>

</dd> <dt>

<span data-ttu-id="2ff2f-116">*pProjection* \[在\]</span><span class="sxs-lookup"><span data-stu-id="2ff2f-116">*pProjection* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="2ff2f-117">Type： **Const [**D3DXMATRIX**](d3dxmatrix.md) \***</span><span class="sxs-lookup"><span data-stu-id="2ff2f-117">Type: **const [**D3DXMATRIX**](d3dxmatrix.md)\***</span></span>

<span data-ttu-id="2ff2f-118">[**D3DXMATRIX**](d3dxmatrix.md)結構的指標，表示投射矩陣。</span><span class="sxs-lookup"><span data-stu-id="2ff2f-118">Pointer to a [**D3DXMATRIX**](d3dxmatrix.md) structure, representing the projection matrix.</span></span>

</dd> <dt>

<span data-ttu-id="2ff2f-119">*pView* \[在\]</span><span class="sxs-lookup"><span data-stu-id="2ff2f-119">*pView* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="2ff2f-120">Type： **Const [**D3DXMATRIX**](d3dxmatrix.md) \***</span><span class="sxs-lookup"><span data-stu-id="2ff2f-120">Type: **const [**D3DXMATRIX**](d3dxmatrix.md)\***</span></span>

<span data-ttu-id="2ff2f-121">[**D3DXMATRIX**](d3dxmatrix.md)結構的指標，代表視圖矩陣。</span><span class="sxs-lookup"><span data-stu-id="2ff2f-121">Pointer to a [**D3DXMATRIX**](d3dxmatrix.md) structure, representing the view matrix.</span></span>

</dd> <dt>

<span data-ttu-id="2ff2f-122">*pWorld* \[在\]</span><span class="sxs-lookup"><span data-stu-id="2ff2f-122">*pWorld* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="2ff2f-123">Type： **Const [**D3DXMATRIX**](d3dxmatrix.md) \***</span><span class="sxs-lookup"><span data-stu-id="2ff2f-123">Type: **const [**D3DXMATRIX**](d3dxmatrix.md)\***</span></span>

<span data-ttu-id="2ff2f-124">[**D3DXMATRIX**](d3dxmatrix.md)結構的指標，代表世界矩陣。</span><span class="sxs-lookup"><span data-stu-id="2ff2f-124">Pointer to a [**D3DXMATRIX**](d3dxmatrix.md) structure, representing the world matrix.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="2ff2f-125">傳回值</span><span class="sxs-lookup"><span data-stu-id="2ff2f-125">Return value</span></span>

<span data-ttu-id="2ff2f-126">類型： **[ **D3DXVECTOR3**](d3dxvector3.md)\***</span><span class="sxs-lookup"><span data-stu-id="2ff2f-126">Type: **[**D3DXVECTOR3**](d3dxvector3.md)\***</span></span>

<span data-ttu-id="2ff2f-127">[**D3DXVECTOR3**](d3dxvector3.md)結構的指標，此結構是從螢幕空間到物件空間所投射的向量。</span><span class="sxs-lookup"><span data-stu-id="2ff2f-127">Pointer to a [**D3DXVECTOR3**](d3dxvector3.md) structure that is the vector projected from screen space to object space.</span></span>

## <a name="remarks"></a><span data-ttu-id="2ff2f-128">備註</span><span class="sxs-lookup"><span data-stu-id="2ff2f-128">Remarks</span></span>

<span data-ttu-id="2ff2f-129">此函式的傳回值與 *不悅* 參數中所傳回的值相同。</span><span class="sxs-lookup"><span data-stu-id="2ff2f-129">The return value for this function is the same value returned in the *pOut* parameter.</span></span> <span data-ttu-id="2ff2f-130">如此一來， **D3DXVec3Unproject** 函式就可以用來做為另一個函式的參數。</span><span class="sxs-lookup"><span data-stu-id="2ff2f-130">In this way, the **D3DXVec3Unproject** function can be used as a parameter for another function.</span></span>

## <a name="requirements"></a><span data-ttu-id="2ff2f-131">規格需求</span><span class="sxs-lookup"><span data-stu-id="2ff2f-131">Requirements</span></span>



| <span data-ttu-id="2ff2f-132">需求</span><span class="sxs-lookup"><span data-stu-id="2ff2f-132">Requirement</span></span> | <span data-ttu-id="2ff2f-133">值</span><span class="sxs-lookup"><span data-stu-id="2ff2f-133">Value</span></span> |
|--------------------|----------------------------------------------------------------------------------------|
| <span data-ttu-id="2ff2f-134">標頭</span><span class="sxs-lookup"><span data-stu-id="2ff2f-134">Header</span></span><br/>  | <dl> <span data-ttu-id="2ff2f-135"><dt>D3dx9math。h</dt></span><span class="sxs-lookup"><span data-stu-id="2ff2f-135"><dt>D3dx9math.h</dt></span></span> </dl> |
| <span data-ttu-id="2ff2f-136">程式庫</span><span class="sxs-lookup"><span data-stu-id="2ff2f-136">Library</span></span><br/> | <dl> <span data-ttu-id="2ff2f-137"><dt>D3dx9 .lib</dt></span><span class="sxs-lookup"><span data-stu-id="2ff2f-137"><dt>D3dx9.lib</dt></span></span> </dl>   |



## <a name="see-also"></a><span data-ttu-id="2ff2f-138">另請參閱</span><span class="sxs-lookup"><span data-stu-id="2ff2f-138">See also</span></span>

<dl> <dt>

[<span data-ttu-id="2ff2f-139">數學函數</span><span class="sxs-lookup"><span data-stu-id="2ff2f-139">Math Functions</span></span>](dx9-graphics-reference-d3dx-functions-math.md)
</dt> <dt>

[<span data-ttu-id="2ff2f-140">**D3DXVec3Project**</span><span class="sxs-lookup"><span data-stu-id="2ff2f-140">**D3DXVec3Project**</span></span>](d3dxvec3project.md)
</dt> </dl>

 

 




