---
description: 依據矩陣轉換平面的陣列。 描述每個平面的向量必須正規化。
ms.assetid: e82e830b-efbb-4bdc-b370-7bfa4326a669
title: 'D3DXPlaneTransformArray 函式 (D3dx9math) '
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
- d3dx9.lib
- d3dx9.dll
ms.openlocfilehash: a9a213b17aca9999ef0028fdceb4bb4321d47660
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 03/15/2021
ms.locfileid: "106981985"
---
# <a name="d3dxplanetransformarray-function-d3dx9mathh"></a><span data-ttu-id="c7455-104">D3DXPlaneTransformArray 函式 (D3dx9math) </span><span class="sxs-lookup"><span data-stu-id="c7455-104">D3DXPlaneTransformArray function (D3dx9math.h)</span></span>

<span data-ttu-id="c7455-105">依據矩陣轉換平面的陣列。</span><span class="sxs-lookup"><span data-stu-id="c7455-105">Transforms an array of planes by a matrix.</span></span> <span data-ttu-id="c7455-106">描述每個平面的向量必須正規化。</span><span class="sxs-lookup"><span data-stu-id="c7455-106">The vectors that describe each plane must be normalized.</span></span>

## <a name="syntax"></a><span data-ttu-id="c7455-107">語法</span><span class="sxs-lookup"><span data-stu-id="c7455-107">Syntax</span></span>


```C++
D3DXPLANE* D3DXPlaneTransformArray(
  _Inout_       D3DXPLANE  *pOut,
  _Out_         UINT       OutStride,
  _In_    const D3DXPLANE  *pP,
  _In_          UINT       PStride,
  _In_    const D3DXMATRIX *pM,
  _In_          UINT       n
);
```



## <a name="parameters"></a><span data-ttu-id="c7455-108">參數</span><span class="sxs-lookup"><span data-stu-id="c7455-108">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="c7455-109">*不悅* \[in、out\]</span><span class="sxs-lookup"><span data-stu-id="c7455-109">*pOut* \[in, out\]</span></span>
</dt> <dd>

<span data-ttu-id="c7455-110">類型： **[ **D3DXPLANE**](d3dxplane.md)\***</span><span class="sxs-lookup"><span data-stu-id="c7455-110">Type: **[**D3DXPLANE**](d3dxplane.md)\***</span></span>

<span data-ttu-id="c7455-111">[**D3DXPLANE**](d3dxplane.md)結構的指標，其中包含所產生的已轉換平面。</span><span class="sxs-lookup"><span data-stu-id="c7455-111">Pointer to the [**D3DXPLANE**](d3dxplane.md) structure that contains the resulting transformed plane.</span></span> <span data-ttu-id="c7455-112">請參閱範例。</span><span class="sxs-lookup"><span data-stu-id="c7455-112">See Example.</span></span>

</dd> <dt>

<span data-ttu-id="c7455-113">*OutStride* \[擴展\]</span><span class="sxs-lookup"><span data-stu-id="c7455-113">*OutStride* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="c7455-114">類型： **[ **UINT**](../winprog/windows-data-types.md)**</span><span class="sxs-lookup"><span data-stu-id="c7455-114">Type: **[**UINT**](../winprog/windows-data-types.md)**</span></span>

<span data-ttu-id="c7455-115">每個轉換平面的 stride。</span><span class="sxs-lookup"><span data-stu-id="c7455-115">The stride of each transformed plane.</span></span>

</dd> <dt>

<span data-ttu-id="c7455-116">*pP* \[在\]</span><span class="sxs-lookup"><span data-stu-id="c7455-116">*pP* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="c7455-117">Type： **Const [**D3DXPLANE**](d3dxplane.md) \***</span><span class="sxs-lookup"><span data-stu-id="c7455-117">Type: **const [**D3DXPLANE**](d3dxplane.md)\***</span></span>

<span data-ttu-id="c7455-118">輸入 [**D3DXPLANE**](d3dxplane.md) 結構的指標，其中包含要轉換之平面的陣列。</span><span class="sxs-lookup"><span data-stu-id="c7455-118">Pointer to the input [**D3DXPLANE**](d3dxplane.md) structure, which contains the array of planes to transform.</span></span> <span data-ttu-id="c7455-119">在呼叫此函式之前，必須先正規化向量 (a，b，c) 來描述平面。</span><span class="sxs-lookup"><span data-stu-id="c7455-119">The vector (a,b,c) that describes the plane must be normalized before this function is called.</span></span> <span data-ttu-id="c7455-120">請參閱範例。</span><span class="sxs-lookup"><span data-stu-id="c7455-120">See Example.</span></span>

</dd> <dt>

<span data-ttu-id="c7455-121">*PStride* \[在\]</span><span class="sxs-lookup"><span data-stu-id="c7455-121">*PStride* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="c7455-122">類型： **[ **UINT**](../winprog/windows-data-types.md)**</span><span class="sxs-lookup"><span data-stu-id="c7455-122">Type: **[**UINT**](../winprog/windows-data-types.md)**</span></span>

<span data-ttu-id="c7455-123">每個未轉換平面的 stride。</span><span class="sxs-lookup"><span data-stu-id="c7455-123">The stride of each non-transformed plane.</span></span>

</dd> <dt>

<span data-ttu-id="c7455-124">*pM* \[在\]</span><span class="sxs-lookup"><span data-stu-id="c7455-124">*pM* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="c7455-125">Type： **Const [**D3DXMATRIX**](d3dxmatrix.md) \***</span><span class="sxs-lookup"><span data-stu-id="c7455-125">Type: **const [**D3DXMATRIX**](d3dxmatrix.md)\***</span></span>

<span data-ttu-id="c7455-126">來源 [**D3DXMATRIX**](d3dxmatrix.md) 結構的指標，其中包含轉換值的反向變換。</span><span class="sxs-lookup"><span data-stu-id="c7455-126">Pointer to the source [**D3DXMATRIX**](d3dxmatrix.md) structure, which contains the inverse transpose of the transformation values.</span></span>

</dd> <dt>

<span data-ttu-id="c7455-127">*n* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="c7455-127">*n* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="c7455-128">類型： **[ **UINT**](../winprog/windows-data-types.md)**</span><span class="sxs-lookup"><span data-stu-id="c7455-128">Type: **[**UINT**](../winprog/windows-data-types.md)**</span></span>

<span data-ttu-id="c7455-129">要轉換的平面數目。</span><span class="sxs-lookup"><span data-stu-id="c7455-129">The number of planes to transform.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="c7455-130">傳回值</span><span class="sxs-lookup"><span data-stu-id="c7455-130">Return value</span></span>

<span data-ttu-id="c7455-131">類型： **[ **D3DXPLANE**](d3dxplane.md)\***</span><span class="sxs-lookup"><span data-stu-id="c7455-131">Type: **[**D3DXPLANE**](d3dxplane.md)\***</span></span>

<span data-ttu-id="c7455-132">[**D3DXPLANE**](d3dxplane.md)結構的指標，代表已轉換的平面。</span><span class="sxs-lookup"><span data-stu-id="c7455-132">Pointer to a [**D3DXPLANE**](d3dxplane.md) structure, representing the transformed plane.</span></span> <span data-ttu-id="c7455-133">這是在 *不悅* 參數中傳回的相同值，因此可以使用此函式作為其他函式的參數。</span><span class="sxs-lookup"><span data-stu-id="c7455-133">This is the same value returned in the *pOut* parameter so that this function can be used as a parameter for another function.</span></span>

## <a name="remarks"></a><span data-ttu-id="c7455-134">備註</span><span class="sxs-lookup"><span data-stu-id="c7455-134">Remarks</span></span>

<span data-ttu-id="c7455-135">此範例會藉由套用非統一比例來轉換一個平面。</span><span class="sxs-lookup"><span data-stu-id="c7455-135">This example transforms one plane by applying a non-uniform scale.</span></span>


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



<span data-ttu-id="c7455-136">依 ax +、+ cz + dw = 0 描述的平面。</span><span class="sxs-lookup"><span data-stu-id="c7455-136">A plane is described by ax + by + cz + dw = 0.</span></span> <span data-ttu-id="c7455-137">第一個平面是以 (a、b、c、d) = (0、1、1、0) 來建立，而這是 y + z = 0 所描述的平面。</span><span class="sxs-lookup"><span data-stu-id="c7455-137">The first plane is created with (a,b,c,d) = (0,1,1,0), which is a plane described by y + z = 0.</span></span> <span data-ttu-id="c7455-138">調整之後，新的平面會包含 (a、b、c、d) = (0、0.353 f、0.235 f、0) ，以顯示 0.353 y + 0.235 z = 0 所要描述的新平面。</span><span class="sxs-lookup"><span data-stu-id="c7455-138">After scaling, the new plane contains (a,b,c,d) = (0, 0.353f, 0.235f, 0), which shows the new plane to be described by 0.353y + 0.235z = 0.</span></span>

<span data-ttu-id="c7455-139">參數 *pM* 包含轉換矩陣的反向變換。</span><span class="sxs-lookup"><span data-stu-id="c7455-139">The parameter *pM* contains the inverse transpose of the transformation matrix.</span></span> <span data-ttu-id="c7455-140">這個方法需要反向變換，如此一來，已轉換之平面的一般向量也可以正確轉換。</span><span class="sxs-lookup"><span data-stu-id="c7455-140">The inverse transpose is required by this method so that the normal vector of the transformed plane can be correctly transformed as well.</span></span>

## <a name="requirements"></a><span data-ttu-id="c7455-141">規格需求</span><span class="sxs-lookup"><span data-stu-id="c7455-141">Requirements</span></span>



| <span data-ttu-id="c7455-142">需求</span><span class="sxs-lookup"><span data-stu-id="c7455-142">Requirement</span></span> | <span data-ttu-id="c7455-143">值</span><span class="sxs-lookup"><span data-stu-id="c7455-143">Value</span></span> |
|--------------------|----------------------------------------------------------------------------------------|
| <span data-ttu-id="c7455-144">標頭</span><span class="sxs-lookup"><span data-stu-id="c7455-144">Header</span></span><br/>  | <dl> <span data-ttu-id="c7455-145"><dt>D3dx9math。h</dt></span><span class="sxs-lookup"><span data-stu-id="c7455-145"><dt>D3dx9math.h</dt></span></span> </dl> |
| <span data-ttu-id="c7455-146">程式庫</span><span class="sxs-lookup"><span data-stu-id="c7455-146">Library</span></span><br/> | <dl> <span data-ttu-id="c7455-147"><dt>D3dx9 .lib</dt></span><span class="sxs-lookup"><span data-stu-id="c7455-147"><dt>D3dx9.lib</dt></span></span> </dl>   |



## <a name="see-also"></a><span data-ttu-id="c7455-148">另請參閱</span><span class="sxs-lookup"><span data-stu-id="c7455-148">See also</span></span>

<dl> <dt>

[<span data-ttu-id="c7455-149">數學函數</span><span class="sxs-lookup"><span data-stu-id="c7455-149">Math Functions</span></span>](dx9-graphics-reference-d3dx-functions-math.md)
</dt> <dt>

[<span data-ttu-id="c7455-150">**D3DXPlaneNormalize**</span><span class="sxs-lookup"><span data-stu-id="c7455-150">**D3DXPlaneNormalize**</span></span>](d3dxplanenormalize.md)
</dt> <dt>

[<span data-ttu-id="c7455-151">**D3DXMatrixRotationX**</span><span class="sxs-lookup"><span data-stu-id="c7455-151">**D3DXMatrixRotationX**</span></span>](d3dxmatrixrotationx.md)
</dt> <dt>

[<span data-ttu-id="c7455-152">**D3DXMatrixRotationY**</span><span class="sxs-lookup"><span data-stu-id="c7455-152">**D3DXMatrixRotationY**</span></span>](d3dxmatrixrotationy.md)
</dt> <dt>

[<span data-ttu-id="c7455-153">**D3DXMatrixRotationZ**</span><span class="sxs-lookup"><span data-stu-id="c7455-153">**D3DXMatrixRotationZ**</span></span>](d3dxmatrixrotationz.md)
</dt> <dt>

[<span data-ttu-id="c7455-154">**D3DXMatrixInverse**</span><span class="sxs-lookup"><span data-stu-id="c7455-154">**D3DXMatrixInverse**</span></span>](d3dxmatrixinverse.md)
</dt> <dt>

[<span data-ttu-id="c7455-155">**D3DXMatrixTranspose**</span><span class="sxs-lookup"><span data-stu-id="c7455-155">**D3DXMatrixTranspose**</span></span>](d3dxmatrixtranspose.md)
</dt> </dl>

 

 
