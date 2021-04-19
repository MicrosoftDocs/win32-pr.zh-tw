---
description: 從螢幕空間將向量投射到物件空間。
ms.assetid: c96d732d-0594-42b4-bc54-458a313f153e
title: 'D3DXVec3Unproject 函式 (D3DX10Math) '
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- D3DXVec3Unproject
api_type:
- HeaderDef
api_location:
- D3DX10Math.h
ms.openlocfilehash: 21916392c689bcac794d44ec2c42c3e0b39abb0c
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 03/15/2021
ms.locfileid: "106988193"
---
# <a name="d3dxvec3unproject-function-d3dx10mathh"></a><span data-ttu-id="f04bb-103">D3DXVec3Unproject 函式 (D3DX10Math) </span><span class="sxs-lookup"><span data-stu-id="f04bb-103">D3DXVec3Unproject function (D3DX10Math.h)</span></span>

<span data-ttu-id="f04bb-104">從螢幕空間將向量投射到物件空間。</span><span class="sxs-lookup"><span data-stu-id="f04bb-104">Projects a vector from screen space into object space.</span></span>

## <a name="syntax"></a><span data-ttu-id="f04bb-105">語法</span><span class="sxs-lookup"><span data-stu-id="f04bb-105">Syntax</span></span>


```C++
D3DXVECTOR3* D3DXVec3Unproject(
  _Inout_       D3DXVECTOR3    *pOut,
  _In_    const D3DXVECTOR3    *pV,
  _In_    const D3D10_VIEWPORT *pViewport,
  _In_    const D3DXMATRIX     *pProjection,
  _In_    const D3DXMATRIX     *pView,
  _In_    const D3DXMATRIX     *pWorld
);
```



## <a name="parameters"></a><span data-ttu-id="f04bb-106">參數</span><span class="sxs-lookup"><span data-stu-id="f04bb-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="f04bb-107">*不悅* \[in、out\]</span><span class="sxs-lookup"><span data-stu-id="f04bb-107">*pOut* \[in, out\]</span></span>
</dt> <dd>

<span data-ttu-id="f04bb-108">類型： **[ **D3DXVECTOR3**](../direct3d9/d3dxvector3.md)\***</span><span class="sxs-lookup"><span data-stu-id="f04bb-108">Type: **[**D3DXVECTOR3**](../direct3d9/d3dxvector3.md)\***</span></span>

<span data-ttu-id="f04bb-109">作業結果之 [**D3DXVECTOR3**](d3d10-d3dxvector3.md) 的指標。</span><span class="sxs-lookup"><span data-stu-id="f04bb-109">Pointer to the [**D3DXVECTOR3**](d3d10-d3dxvector3.md) that is the result of the operation.</span></span>

</dd> <dt>

<span data-ttu-id="f04bb-110">*pV* \[在\]</span><span class="sxs-lookup"><span data-stu-id="f04bb-110">*pV* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="f04bb-111">Type： **Const [**D3DXVECTOR3**](../direct3d9/d3dxvector3.md) \***</span><span class="sxs-lookup"><span data-stu-id="f04bb-111">Type: **const [**D3DXVECTOR3**](../direct3d9/d3dxvector3.md)\***</span></span>

<span data-ttu-id="f04bb-112">來源 D3DXVECTOR3 結構的指標。</span><span class="sxs-lookup"><span data-stu-id="f04bb-112">Pointer to the source D3DXVECTOR3 structure.</span></span>

</dd> <dt>

<span data-ttu-id="f04bb-113">*pViewport* \[在\]</span><span class="sxs-lookup"><span data-stu-id="f04bb-113">*pViewport* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="f04bb-114">Type： **Const [**D3D10 \_ 視口**](/windows/desktop/api/D3D10/ns-d3d10-d3d10_viewport) \***</span><span class="sxs-lookup"><span data-stu-id="f04bb-114">Type: **const [**D3D10\_VIEWPORT**](/windows/desktop/api/D3D10/ns-d3d10-d3d10_viewport)\***</span></span>

<span data-ttu-id="f04bb-115">[**D3D10 \_ 區**](/windows/desktop/api/D3D10/ns-d3d10-d3d10_viewport)的指標，表示區。</span><span class="sxs-lookup"><span data-stu-id="f04bb-115">Pointer to a [**D3D10\_VIEWPORT**](/windows/desktop/api/D3D10/ns-d3d10-d3d10_viewport), representing the viewport.</span></span>

</dd> <dt>

<span data-ttu-id="f04bb-116">*pProjection* \[在\]</span><span class="sxs-lookup"><span data-stu-id="f04bb-116">*pProjection* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="f04bb-117">Type： **Const [**D3DXMATRIX**](../direct3d9/d3dxmatrix.md) \***</span><span class="sxs-lookup"><span data-stu-id="f04bb-117">Type: **const [**D3DXMATRIX**](../direct3d9/d3dxmatrix.md)\***</span></span>

<span data-ttu-id="f04bb-118">[**D3DXMATRIX**](d3d10-d3dxmatrix.md)結構的指標，表示投射矩陣。</span><span class="sxs-lookup"><span data-stu-id="f04bb-118">Pointer to a [**D3DXMATRIX**](d3d10-d3dxmatrix.md) structure, representing the projection matrix.</span></span>

</dd> <dt>

<span data-ttu-id="f04bb-119">*pView* \[在\]</span><span class="sxs-lookup"><span data-stu-id="f04bb-119">*pView* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="f04bb-120">Type： **Const [**D3DXMATRIX**](../direct3d9/d3dxmatrix.md) \***</span><span class="sxs-lookup"><span data-stu-id="f04bb-120">Type: **const [**D3DXMATRIX**](../direct3d9/d3dxmatrix.md)\***</span></span>

<span data-ttu-id="f04bb-121">D3DXMATRIX 結構的指標，代表視圖矩陣。</span><span class="sxs-lookup"><span data-stu-id="f04bb-121">Pointer to a D3DXMATRIX structure, representing the view matrix.</span></span>

</dd> <dt>

<span data-ttu-id="f04bb-122">*pWorld* \[在\]</span><span class="sxs-lookup"><span data-stu-id="f04bb-122">*pWorld* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="f04bb-123">Type： **Const [**D3DXMATRIX**](../direct3d9/d3dxmatrix.md) \***</span><span class="sxs-lookup"><span data-stu-id="f04bb-123">Type: **const [**D3DXMATRIX**](../direct3d9/d3dxmatrix.md)\***</span></span>

<span data-ttu-id="f04bb-124">D3DXMATRIX 結構的指標，代表世界矩陣。</span><span class="sxs-lookup"><span data-stu-id="f04bb-124">Pointer to a D3DXMATRIX structure, representing the world matrix.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="f04bb-125">傳回值</span><span class="sxs-lookup"><span data-stu-id="f04bb-125">Return value</span></span>

<span data-ttu-id="f04bb-126">類型： **[ **D3DXVECTOR3**](../direct3d9/d3dxvector3.md)\***</span><span class="sxs-lookup"><span data-stu-id="f04bb-126">Type: **[**D3DXVECTOR3**](../direct3d9/d3dxvector3.md)\***</span></span>

<span data-ttu-id="f04bb-127">D3DXVECTOR3 結構的指標，此結構是從螢幕空間到物件空間所投射的向量。</span><span class="sxs-lookup"><span data-stu-id="f04bb-127">Pointer to a D3DXVECTOR3 structure that is the vector projected from screen space to object space.</span></span>

## <a name="remarks"></a><span data-ttu-id="f04bb-128">備註</span><span class="sxs-lookup"><span data-stu-id="f04bb-128">Remarks</span></span>

<span data-ttu-id="f04bb-129">此函式的傳回值與不悅參數中所傳回的值相同。</span><span class="sxs-lookup"><span data-stu-id="f04bb-129">The return value for this function is the same value returned in the pOut parameter.</span></span> <span data-ttu-id="f04bb-130">如此一來，D3DXVec3Unproject 函式就可以用來做為另一個函式的參數。</span><span class="sxs-lookup"><span data-stu-id="f04bb-130">In this way, the D3DXVec3Unproject function can be used as a parameter for another function.</span></span>

## <a name="requirements"></a><span data-ttu-id="f04bb-131">規格需求</span><span class="sxs-lookup"><span data-stu-id="f04bb-131">Requirements</span></span>



| <span data-ttu-id="f04bb-132">需求</span><span class="sxs-lookup"><span data-stu-id="f04bb-132">Requirement</span></span> | <span data-ttu-id="f04bb-133">值</span><span class="sxs-lookup"><span data-stu-id="f04bb-133">Value</span></span> |
|-------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="f04bb-134">標頭</span><span class="sxs-lookup"><span data-stu-id="f04bb-134">Header</span></span><br/> | <dl> <span data-ttu-id="f04bb-135"><dt>D3DX10Math。h</dt></span><span class="sxs-lookup"><span data-stu-id="f04bb-135"><dt>D3DX10Math.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="f04bb-136">另請參閱</span><span class="sxs-lookup"><span data-stu-id="f04bb-136">See also</span></span>

<dl> <dt>

[<span data-ttu-id="f04bb-137">數學函數</span><span class="sxs-lookup"><span data-stu-id="f04bb-137">Math Functions</span></span>](d3d10-graphics-reference-d3dx10-functions-math.md)
</dt> </dl>

 

 
