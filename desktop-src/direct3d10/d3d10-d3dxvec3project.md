---
description: 將物件空間中的3D 向量投射到螢幕空間。
ms.assetid: 6fc59788-c3f7-4f47-a345-9108105e820e
title: 'D3DXVec3Project 函式 (D3DX10Math) '
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- D3DXVec3Project
api_type:
- HeaderDef
api_location:
- D3DX10Math.h
ms.openlocfilehash: c8d86949f754afb7639a0c28ff6d8b14c0e40ff0
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 03/15/2021
ms.locfileid: "104322967"
---
# <a name="d3dxvec3project-function-d3dx10mathh"></a><span data-ttu-id="75e2e-103">D3DXVec3Project 函式 (D3DX10Math) </span><span class="sxs-lookup"><span data-stu-id="75e2e-103">D3DXVec3Project function (D3DX10Math.h)</span></span>

<span data-ttu-id="75e2e-104">將物件空間中的3D 向量投射到螢幕空間。</span><span class="sxs-lookup"><span data-stu-id="75e2e-104">Projects a 3D vector from object space into screen space.</span></span>

## <a name="syntax"></a><span data-ttu-id="75e2e-105">語法</span><span class="sxs-lookup"><span data-stu-id="75e2e-105">Syntax</span></span>


```C++
D3DXVECTOR3* D3DXVec3Project(
  _Inout_       D3DXVECTOR3    *pOut,
  _In_    const D3DXVECTOR3    *pV,
  _In_    const D3D10_VIEWPORT *pViewport,
  _In_    const D3DXMATRIX     *pProjection,
  _In_    const D3DXMATRIX     *pView,
  _In_    const D3DXMATRIX     *pWorld
);
```



## <a name="parameters"></a><span data-ttu-id="75e2e-106">參數</span><span class="sxs-lookup"><span data-stu-id="75e2e-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="75e2e-107">*不悅* \[in、out\]</span><span class="sxs-lookup"><span data-stu-id="75e2e-107">*pOut* \[in, out\]</span></span>
</dt> <dd>

<span data-ttu-id="75e2e-108">類型： **[ **D3DXVECTOR3**](../direct3d9/d3dxvector3.md)\***</span><span class="sxs-lookup"><span data-stu-id="75e2e-108">Type: **[**D3DXVECTOR3**](../direct3d9/d3dxvector3.md)\***</span></span>

<span data-ttu-id="75e2e-109">作業結果之 [**D3DXVECTOR3**](d3d10-d3dxvector3.md) 的指標。</span><span class="sxs-lookup"><span data-stu-id="75e2e-109">Pointer to the [**D3DXVECTOR3**](d3d10-d3dxvector3.md) that is the result of the operation.</span></span>

</dd> <dt>

<span data-ttu-id="75e2e-110">*pV* \[在\]</span><span class="sxs-lookup"><span data-stu-id="75e2e-110">*pV* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="75e2e-111">Type： **Const [**D3DXVECTOR3**](../direct3d9/d3dxvector3.md) \***</span><span class="sxs-lookup"><span data-stu-id="75e2e-111">Type: **const [**D3DXVECTOR3**](../direct3d9/d3dxvector3.md)\***</span></span>

<span data-ttu-id="75e2e-112">來源 D3DXVECTOR3 結構的指標。</span><span class="sxs-lookup"><span data-stu-id="75e2e-112">Pointer to the source D3DXVECTOR3 structure.</span></span>

</dd> <dt>

<span data-ttu-id="75e2e-113">*pViewport* \[在\]</span><span class="sxs-lookup"><span data-stu-id="75e2e-113">*pViewport* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="75e2e-114">Type： **Const [**D3D10 \_ 視口**](/windows/desktop/api/D3D10/ns-d3d10-d3d10_viewport) \***</span><span class="sxs-lookup"><span data-stu-id="75e2e-114">Type: **const [**D3D10\_VIEWPORT**](/windows/desktop/api/D3D10/ns-d3d10-d3d10_viewport)\***</span></span>

<span data-ttu-id="75e2e-115">[**D3D10 \_ 區**](/windows/desktop/api/D3D10/ns-d3d10-d3d10_viewport)的指標，表示區。</span><span class="sxs-lookup"><span data-stu-id="75e2e-115">Pointer to a [**D3D10\_VIEWPORT**](/windows/desktop/api/D3D10/ns-d3d10-d3d10_viewport), representing the viewport.</span></span>

</dd> <dt>

<span data-ttu-id="75e2e-116">*pProjection* \[在\]</span><span class="sxs-lookup"><span data-stu-id="75e2e-116">*pProjection* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="75e2e-117">Type： **Const [**D3DXMATRIX**](../direct3d9/d3dxmatrix.md) \***</span><span class="sxs-lookup"><span data-stu-id="75e2e-117">Type: **const [**D3DXMATRIX**](../direct3d9/d3dxmatrix.md)\***</span></span>

<span data-ttu-id="75e2e-118">[**D3DXMATRIX**](d3d10-d3dxmatrix.md)結構的指標，表示投射矩陣。</span><span class="sxs-lookup"><span data-stu-id="75e2e-118">Pointer to a [**D3DXMATRIX**](d3d10-d3dxmatrix.md) structure, representing the projection matrix.</span></span>

</dd> <dt>

<span data-ttu-id="75e2e-119">*pView* \[在\]</span><span class="sxs-lookup"><span data-stu-id="75e2e-119">*pView* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="75e2e-120">Type： **Const [**D3DXMATRIX**](../direct3d9/d3dxmatrix.md) \***</span><span class="sxs-lookup"><span data-stu-id="75e2e-120">Type: **const [**D3DXMATRIX**](../direct3d9/d3dxmatrix.md)\***</span></span>

<span data-ttu-id="75e2e-121">D3DXMATRIX 結構的指標，代表視圖矩陣。</span><span class="sxs-lookup"><span data-stu-id="75e2e-121">Pointer to a D3DXMATRIX structure, representing the view matrix.</span></span>

</dd> <dt>

<span data-ttu-id="75e2e-122">*pWorld* \[在\]</span><span class="sxs-lookup"><span data-stu-id="75e2e-122">*pWorld* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="75e2e-123">Type： **Const [**D3DXMATRIX**](../direct3d9/d3dxmatrix.md) \***</span><span class="sxs-lookup"><span data-stu-id="75e2e-123">Type: **const [**D3DXMATRIX**](../direct3d9/d3dxmatrix.md)\***</span></span>

<span data-ttu-id="75e2e-124">D3DXMATRIX 結構的指標，代表世界矩陣。</span><span class="sxs-lookup"><span data-stu-id="75e2e-124">Pointer to a D3DXMATRIX structure, representing the world matrix.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="75e2e-125">傳回值</span><span class="sxs-lookup"><span data-stu-id="75e2e-125">Return value</span></span>

<span data-ttu-id="75e2e-126">類型： **[ **D3DXVECTOR3**](../direct3d9/d3dxvector3.md)\***</span><span class="sxs-lookup"><span data-stu-id="75e2e-126">Type: **[**D3DXVECTOR3**](../direct3d9/d3dxvector3.md)\***</span></span>

<span data-ttu-id="75e2e-127">D3DXVECTOR3 結構的指標，此結構是從物件空間到螢幕空間投射的向量。</span><span class="sxs-lookup"><span data-stu-id="75e2e-127">Pointer to a D3DXVECTOR3 structure that is the vector projected from object space to screen space.</span></span>

## <a name="remarks"></a><span data-ttu-id="75e2e-128">備註</span><span class="sxs-lookup"><span data-stu-id="75e2e-128">Remarks</span></span>

<span data-ttu-id="75e2e-129">此函式的傳回值與不悅參數中所傳回的值相同。</span><span class="sxs-lookup"><span data-stu-id="75e2e-129">The return value for this function is the same value returned in the pOut parameter.</span></span> <span data-ttu-id="75e2e-130">如此一來，D3DXVec3Project 函式就可以用來做為另一個函式的參數。</span><span class="sxs-lookup"><span data-stu-id="75e2e-130">In this way, the D3DXVec3Project function can be used as a parameter for another function.</span></span>

## <a name="requirements"></a><span data-ttu-id="75e2e-131">規格需求</span><span class="sxs-lookup"><span data-stu-id="75e2e-131">Requirements</span></span>



| <span data-ttu-id="75e2e-132">需求</span><span class="sxs-lookup"><span data-stu-id="75e2e-132">Requirement</span></span> | <span data-ttu-id="75e2e-133">值</span><span class="sxs-lookup"><span data-stu-id="75e2e-133">Value</span></span> |
|-------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="75e2e-134">標頭</span><span class="sxs-lookup"><span data-stu-id="75e2e-134">Header</span></span><br/> | <dl> <span data-ttu-id="75e2e-135"><dt>D3DX10Math。h</dt></span><span class="sxs-lookup"><span data-stu-id="75e2e-135"><dt>D3DX10Math.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="75e2e-136">另請參閱</span><span class="sxs-lookup"><span data-stu-id="75e2e-136">See also</span></span>

<dl> <dt>

[<span data-ttu-id="75e2e-137">數學函數</span><span class="sxs-lookup"><span data-stu-id="75e2e-137">Math Functions</span></span>](d3d10-graphics-reference-d3dx10-functions-math.md)
</dt> </dl>

 

 
