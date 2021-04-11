---
description: 依據矩陣轉換平面的陣列。 描述每個平面的向量必須正規化。
ms.assetid: 9529b06a-0575-4115-8d35-fc35a7bfb0bd
title: 'D3DXPlaneTransformArray 函式 (D3DX10Math) '
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- D3DXPlaneTransformArray
api_type:
- LibDef
api_location:
- D3DX10.lib
- D3DX10.dll
ms.openlocfilehash: 128b9c8c73db81faa877295e993504a7a510cd4a
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 03/15/2021
ms.locfileid: "104035390"
---
# <a name="d3dxplanetransformarray-function-d3dx10mathh"></a><span data-ttu-id="bdf7c-104">D3DXPlaneTransformArray 函式 (D3DX10Math) </span><span class="sxs-lookup"><span data-stu-id="bdf7c-104">D3DXPlaneTransformArray function (D3DX10Math.h)</span></span>

<span data-ttu-id="bdf7c-105">依據矩陣轉換平面的陣列。</span><span class="sxs-lookup"><span data-stu-id="bdf7c-105">Transforms an array of planes by a matrix.</span></span> <span data-ttu-id="bdf7c-106">描述每個平面的向量必須正規化。</span><span class="sxs-lookup"><span data-stu-id="bdf7c-106">The vectors that describe each plane must be normalized.</span></span>

## <a name="syntax"></a><span data-ttu-id="bdf7c-107">語法</span><span class="sxs-lookup"><span data-stu-id="bdf7c-107">Syntax</span></span>


```C++
D3DXPLANE* D3DXPlaneTransformArray(
  _Inout_       D3DXPLANE  *pOut,
  _In_          UINT       OutStride,
  _In_    const D3DXPLANE  *pP,
  _In_          UINT       PStride,
  _In_    const D3DXMATRIX *pM,
  _In_          UINT       n
);
```



## <a name="parameters"></a><span data-ttu-id="bdf7c-108">參數</span><span class="sxs-lookup"><span data-stu-id="bdf7c-108">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="bdf7c-109">*不悅* \[in、out\]</span><span class="sxs-lookup"><span data-stu-id="bdf7c-109">*pOut* \[in, out\]</span></span>
</dt> <dd>

<span data-ttu-id="bdf7c-110">類型： **[ **D3DXPLANE**](../direct3d9/d3dxplane.md)\***</span><span class="sxs-lookup"><span data-stu-id="bdf7c-110">Type: **[**D3DXPLANE**](../direct3d9/d3dxplane.md)\***</span></span>

<span data-ttu-id="bdf7c-111">[**D3DXPLANE**](d3d10-d3dxplane.md)結構的指標，其中包含所產生的已轉換平面。</span><span class="sxs-lookup"><span data-stu-id="bdf7c-111">Pointer to the [**D3DXPLANE**](d3d10-d3dxplane.md) structure that contains the resulting transformed plane.</span></span> <span data-ttu-id="bdf7c-112">請參閱範例。</span><span class="sxs-lookup"><span data-stu-id="bdf7c-112">See Example.</span></span>

</dd> <dt>

<span data-ttu-id="bdf7c-113">*OutStride* \[在\]</span><span class="sxs-lookup"><span data-stu-id="bdf7c-113">*OutStride* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="bdf7c-114">類型： **[ **UINT**](../winprog/windows-data-types.md)**</span><span class="sxs-lookup"><span data-stu-id="bdf7c-114">Type: **[**UINT**](../winprog/windows-data-types.md)**</span></span>

<span data-ttu-id="bdf7c-115">每個轉換平面的 stride。</span><span class="sxs-lookup"><span data-stu-id="bdf7c-115">The stride of each transformed plane.</span></span>

</dd> <dt>

<span data-ttu-id="bdf7c-116">*pP* \[在\]</span><span class="sxs-lookup"><span data-stu-id="bdf7c-116">*pP* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="bdf7c-117">Type： **Const [**D3DXPLANE**](../direct3d9/d3dxplane.md) \***</span><span class="sxs-lookup"><span data-stu-id="bdf7c-117">Type: **const [**D3DXPLANE**](../direct3d9/d3dxplane.md)\***</span></span>

<span data-ttu-id="bdf7c-118">輸入 D3DXPLANE 結構的指標，其中包含要轉換之平面的陣列。</span><span class="sxs-lookup"><span data-stu-id="bdf7c-118">Pointer to the input D3DXPLANE structure, which contains the array of planes to transform.</span></span> <span data-ttu-id="bdf7c-119">在呼叫此函式之前，必須先正規化向量 (a，b，c) 來描述平面。</span><span class="sxs-lookup"><span data-stu-id="bdf7c-119">The vector (a, b, c) that describes the plane must be normalized before this function is called.</span></span> <span data-ttu-id="bdf7c-120">請參閱範例。</span><span class="sxs-lookup"><span data-stu-id="bdf7c-120">See Example.</span></span>

</dd> <dt>

<span data-ttu-id="bdf7c-121">*PStride* \[在\]</span><span class="sxs-lookup"><span data-stu-id="bdf7c-121">*PStride* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="bdf7c-122">類型： **[ **UINT**](../winprog/windows-data-types.md)**</span><span class="sxs-lookup"><span data-stu-id="bdf7c-122">Type: **[**UINT**](../winprog/windows-data-types.md)**</span></span>

<span data-ttu-id="bdf7c-123">每個未轉換平面的 stride。</span><span class="sxs-lookup"><span data-stu-id="bdf7c-123">The stride of each non-transformed plane.</span></span>

</dd> <dt>

<span data-ttu-id="bdf7c-124">*pM* \[在\]</span><span class="sxs-lookup"><span data-stu-id="bdf7c-124">*pM* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="bdf7c-125">Type： **Const [**D3DXMATRIX**](../direct3d9/d3dxmatrix.md) \***</span><span class="sxs-lookup"><span data-stu-id="bdf7c-125">Type: **const [**D3DXMATRIX**](../direct3d9/d3dxmatrix.md)\***</span></span>

<span data-ttu-id="bdf7c-126">來源 [**D3DXMATRIX**](d3d10-d3dxmatrix.md) 結構的指標，其中包含轉換值的反向變換。</span><span class="sxs-lookup"><span data-stu-id="bdf7c-126">Pointer to the source [**D3DXMATRIX**](d3d10-d3dxmatrix.md) structure, which contains the inverse transpose of the transformation values.</span></span>

</dd> <dt>

<span data-ttu-id="bdf7c-127">*n* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="bdf7c-127">*n* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="bdf7c-128">類型： **[ **UINT**](../winprog/windows-data-types.md)**</span><span class="sxs-lookup"><span data-stu-id="bdf7c-128">Type: **[**UINT**](../winprog/windows-data-types.md)**</span></span>

<span data-ttu-id="bdf7c-129">要轉換的平面數目。</span><span class="sxs-lookup"><span data-stu-id="bdf7c-129">The number of planes to transform.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="bdf7c-130">傳回值</span><span class="sxs-lookup"><span data-stu-id="bdf7c-130">Return value</span></span>

<span data-ttu-id="bdf7c-131">類型： **[ **D3DXPLANE**](../direct3d9/d3dxplane.md)\***</span><span class="sxs-lookup"><span data-stu-id="bdf7c-131">Type: **[**D3DXPLANE**](../direct3d9/d3dxplane.md)\***</span></span>

<span data-ttu-id="bdf7c-132">D3DXPLANE 結構的指標，代表已轉換的平面。</span><span class="sxs-lookup"><span data-stu-id="bdf7c-132">Pointer to a D3DXPLANE structure, representing the transformed plane.</span></span> <span data-ttu-id="bdf7c-133">這是在不悅參數中傳回的相同值，因此可以使用此函式作為其他函式的參數。</span><span class="sxs-lookup"><span data-stu-id="bdf7c-133">This is the same value returned in the pOut parameter so that this function can be used as a parameter for another function.</span></span>

## <a name="remarks"></a><span data-ttu-id="bdf7c-134">備註</span><span class="sxs-lookup"><span data-stu-id="bdf7c-134">Remarks</span></span>

<span data-ttu-id="bdf7c-135">此範例會藉由套用非統一比例來轉換一個平面。</span><span class="sxs-lookup"><span data-stu-id="bdf7c-135">This example transforms one plane by applying a non-uniform scale.</span></span>


```
#define ARRAYSIZE 4
D3DXPLANE planeNew[ARRAYSIZE];
D3DXPLANE plane[ARRAYSIZE];

for(int i = 0; i < ARRAYSIZE; i++)
{
    plane = D3DXPLANE( 0.0f, 1.0f, 1.0f, 0.0f );
    D3DXPlaneNormalize( &plane[i], &plane[i] );
}

D3DXMATRIX  matrix;
D3DXMatrixScaling( &matrix, 1.0f, 2.0f, 3.0f ); 
D3DXMatrixInverse( &matrix, NULL, &matrix );
D3DXMatrixTranspose( &matrix, &matrix );
D3DXPlaneTransformArray( &planeNew, sizeof (D3DXPLANE), &plane, 
                         sizeof (D3DXPLANE), &matrix, ARRAYSIZE );
```



<span data-ttu-id="bdf7c-136">依 ax +、+ cz + dw = 0 描述的平面。</span><span class="sxs-lookup"><span data-stu-id="bdf7c-136">A plane is described by ax + by + cz + dw = 0.</span></span> <span data-ttu-id="bdf7c-137">第一個平面是以 (a、b、c、d) = (0、1、1、0) 來建立，而這是 y + z = 0 所描述的平面。</span><span class="sxs-lookup"><span data-stu-id="bdf7c-137">The first plane is created with (a,b,c,d) = (0,1,1,0), which is a plane described by y + z = 0.</span></span> <span data-ttu-id="bdf7c-138">調整之後，新的平面會包含 (a、b、c、d) = (0、0.353 f、0.235 f、0) ，以顯示 0.353 y + 0.235 z = 0 所要描述的新平面。</span><span class="sxs-lookup"><span data-stu-id="bdf7c-138">After scaling, the new plane contains (a,b,c,d) = (0, 0.353f, 0.235f, 0), which shows the new plane to be described by 0.353y + 0.235z = 0.</span></span>

<span data-ttu-id="bdf7c-139">參數 pM 包含轉換矩陣的反向變換。</span><span class="sxs-lookup"><span data-stu-id="bdf7c-139">The parameter pM, contains the inverse transpose of the transformation matrix.</span></span> <span data-ttu-id="bdf7c-140">這個方法需要反向變換，如此一來，已轉換之平面的一般向量也可以正確轉換。</span><span class="sxs-lookup"><span data-stu-id="bdf7c-140">The inverse transpose is required by this method so that the normal vector of the transformed plane can be correctly transformed as well.</span></span>

## <a name="requirements"></a><span data-ttu-id="bdf7c-141">規格需求</span><span class="sxs-lookup"><span data-stu-id="bdf7c-141">Requirements</span></span>



| <span data-ttu-id="bdf7c-142">需求</span><span class="sxs-lookup"><span data-stu-id="bdf7c-142">Requirement</span></span> | <span data-ttu-id="bdf7c-143">值</span><span class="sxs-lookup"><span data-stu-id="bdf7c-143">Value</span></span> |
|--------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="bdf7c-144">標頭</span><span class="sxs-lookup"><span data-stu-id="bdf7c-144">Header</span></span><br/>  | <dl> <span data-ttu-id="bdf7c-145"><dt>D3DX10Math。h</dt></span><span class="sxs-lookup"><span data-stu-id="bdf7c-145"><dt>D3DX10Math.h</dt></span></span> </dl> |
| <span data-ttu-id="bdf7c-146">程式庫</span><span class="sxs-lookup"><span data-stu-id="bdf7c-146">Library</span></span><br/> | <dl> <span data-ttu-id="bdf7c-147"><dt>D3DX10 .lib</dt></span><span class="sxs-lookup"><span data-stu-id="bdf7c-147"><dt>D3DX10.lib</dt></span></span> </dl>   |



## <a name="see-also"></a><span data-ttu-id="bdf7c-148">另請參閱</span><span class="sxs-lookup"><span data-stu-id="bdf7c-148">See also</span></span>

<dl> <dt>

[<span data-ttu-id="bdf7c-149">數學函數</span><span class="sxs-lookup"><span data-stu-id="bdf7c-149">Math Functions</span></span>](d3d10-graphics-reference-d3dx10-functions-math.md)
</dt> </dl>

 

 
