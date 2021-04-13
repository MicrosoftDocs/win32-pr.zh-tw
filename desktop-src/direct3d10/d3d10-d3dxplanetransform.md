---
description: 依矩陣轉換平面。 輸入矩陣是實際轉換的反向變換。
ms.assetid: ded06eac-4086-47e8-bc55-c37959afc22d
title: 'D3DXPlaneTransform 函式 (D3DX10Math) '
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- D3DXPlaneTransform
api_type:
- LibDef
api_location:
- D3DX10.lib
- D3DX10.dll
ms.openlocfilehash: 1b3c3390d84cd0d9c876afac6243ab90ca515e11
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 03/15/2021
ms.locfileid: "104323215"
---
# <a name="d3dxplanetransform-function-d3dx10mathh"></a><span data-ttu-id="1aa5c-104">D3DXPlaneTransform 函式 (D3DX10Math) </span><span class="sxs-lookup"><span data-stu-id="1aa5c-104">D3DXPlaneTransform function (D3DX10Math.h)</span></span>

<span data-ttu-id="1aa5c-105">依矩陣轉換平面。</span><span class="sxs-lookup"><span data-stu-id="1aa5c-105">Transforms a plane by a matrix.</span></span> <span data-ttu-id="1aa5c-106">輸入矩陣是實際轉換的反向變換。</span><span class="sxs-lookup"><span data-stu-id="1aa5c-106">The input matrix is the inverse transpose of the actual transformation.</span></span>

## <a name="syntax"></a><span data-ttu-id="1aa5c-107">語法</span><span class="sxs-lookup"><span data-stu-id="1aa5c-107">Syntax</span></span>


```C++
D3DXPLANE* D3DXPlaneTransform(
  _Inout_       D3DXPLANE  *pOut,
  _In_    const D3DXPLANE  *pP,
  _In_    const D3DXMATRIX *pM
);
```



## <a name="parameters"></a><span data-ttu-id="1aa5c-108">參數</span><span class="sxs-lookup"><span data-stu-id="1aa5c-108">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="1aa5c-109">*不悅* \[in、out\]</span><span class="sxs-lookup"><span data-stu-id="1aa5c-109">*pOut* \[in, out\]</span></span>
</dt> <dd>

<span data-ttu-id="1aa5c-110">類型： **[ **D3DXPLANE**](../direct3d9/d3dxplane.md)\***</span><span class="sxs-lookup"><span data-stu-id="1aa5c-110">Type: **[**D3DXPLANE**](../direct3d9/d3dxplane.md)\***</span></span>

<span data-ttu-id="1aa5c-111">[**D3DXPLANE**](d3d10-d3dxplane.md)的指標，其中包含所產生的已轉換平面。</span><span class="sxs-lookup"><span data-stu-id="1aa5c-111">Pointer to the [**D3DXPLANE**](d3d10-d3dxplane.md) that contains the resulting transformed plane.</span></span> <span data-ttu-id="1aa5c-112">請參閱範例。</span><span class="sxs-lookup"><span data-stu-id="1aa5c-112">See example.</span></span>

</dd> <dt>

<span data-ttu-id="1aa5c-113">*pP* \[在\]</span><span class="sxs-lookup"><span data-stu-id="1aa5c-113">*pP* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="1aa5c-114">Type： **Const [**D3DXPLANE**](../direct3d9/d3dxplane.md) \***</span><span class="sxs-lookup"><span data-stu-id="1aa5c-114">Type: **const [**D3DXPLANE**](../direct3d9/d3dxplane.md)\***</span></span>

<span data-ttu-id="1aa5c-115">輸入 D3DXPLANE 結構的指標，其中包含將轉換的平面。</span><span class="sxs-lookup"><span data-stu-id="1aa5c-115">Pointer to the input D3DXPLANE structure, which contains the plane that will be transformed.</span></span> <span data-ttu-id="1aa5c-116">在呼叫此函式之前，必須先正規化向量 (a，b，c) 來描述平面。</span><span class="sxs-lookup"><span data-stu-id="1aa5c-116">The vector (a,b,c) that describes the plane must be normalized before this function is called.</span></span> <span data-ttu-id="1aa5c-117">請參閱範例。</span><span class="sxs-lookup"><span data-stu-id="1aa5c-117">See example.</span></span>

</dd> <dt>

<span data-ttu-id="1aa5c-118">*pM* \[在\]</span><span class="sxs-lookup"><span data-stu-id="1aa5c-118">*pM* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="1aa5c-119">Type： **Const [**D3DXMATRIX**](../direct3d9/d3dxmatrix.md) \***</span><span class="sxs-lookup"><span data-stu-id="1aa5c-119">Type: **const [**D3DXMATRIX**](../direct3d9/d3dxmatrix.md)\***</span></span>

<span data-ttu-id="1aa5c-120">來源 [**D3DXMATRIX**](d3d10-d3dxmatrix.md) 結構的指標，其中包含轉換值。</span><span class="sxs-lookup"><span data-stu-id="1aa5c-120">Pointer to the source [**D3DXMATRIX**](d3d10-d3dxmatrix.md) structure, which contains the transformation values.</span></span> <span data-ttu-id="1aa5c-121">此矩陣必須包含轉換值的反向變換。</span><span class="sxs-lookup"><span data-stu-id="1aa5c-121">This matrix must contain the inverse transpose of the transformation values.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="1aa5c-122">傳回值</span><span class="sxs-lookup"><span data-stu-id="1aa5c-122">Return value</span></span>

<span data-ttu-id="1aa5c-123">類型： **[ **D3DXPLANE**](../direct3d9/d3dxplane.md)\***</span><span class="sxs-lookup"><span data-stu-id="1aa5c-123">Type: **[**D3DXPLANE**](../direct3d9/d3dxplane.md)\***</span></span>

<span data-ttu-id="1aa5c-124">D3DXPLANE 結構的指標，代表已轉換的平面。</span><span class="sxs-lookup"><span data-stu-id="1aa5c-124">Pointer to a D3DXPLANE structure, representing the transformed plane.</span></span> <span data-ttu-id="1aa5c-125">這是在不悅參數中傳回的相同值，因此可以使用此函式作為其他函式的參數。</span><span class="sxs-lookup"><span data-stu-id="1aa5c-125">This is the same value returned in the pOut parameter so that this function can be used as a parameter for another function.</span></span>

## <a name="remarks"></a><span data-ttu-id="1aa5c-126">備註</span><span class="sxs-lookup"><span data-stu-id="1aa5c-126">Remarks</span></span>

### <a name="examples"></a><span data-ttu-id="1aa5c-127">範例</span><span class="sxs-lookup"><span data-stu-id="1aa5c-127">Examples</span></span>

<span data-ttu-id="1aa5c-128">此範例會套用非統一比例來轉換平面。</span><span class="sxs-lookup"><span data-stu-id="1aa5c-128">This example transforms a plane by applying a non-uniform scale.</span></span>


```
D3DXPLANE   planeNew;
D3DXPLANE   plane(0,1,1,0);
D3DXPlaneNormalize(&plane, &plane);

D3DXMATRIX  matrix;
D3DXMatrixScaling(&matrix, 1.0f,2.0f,3.0f); 
D3DXMatrixInverse(&matrix, NULL, &matrix);
D3DXMatrixTranspose(&matrix, &matrix);
D3DXPlaneTransform(&planeNew, &plane, &matrix);
```



<span data-ttu-id="1aa5c-129">依 ax +、+ cz + dw = 0 描述的平面。</span><span class="sxs-lookup"><span data-stu-id="1aa5c-129">A plane is described by ax + by + cz + dw = 0.</span></span> <span data-ttu-id="1aa5c-130">第一個平面是以 (a、b、c、d) = (0、1、1、0) 來建立，而這是 y + z = 0 所描述的平面。</span><span class="sxs-lookup"><span data-stu-id="1aa5c-130">The first plane is created with (a,b,c,d) = (0,1,1,0), which is a plane described by y + z = 0.</span></span> <span data-ttu-id="1aa5c-131">調整之後，新的平面會包含 (a、b、c、d) = (0、0.353 f、0.235 f、0) ，以顯示 0.353 y + 0.235 z = 0 所要描述的新平面。</span><span class="sxs-lookup"><span data-stu-id="1aa5c-131">After scaling, the new plane contains (a,b,c,d) = (0, 0.353f, 0.235f, 0), which shows the new plane to be described by 0.353y + 0.235z = 0.</span></span>

<span data-ttu-id="1aa5c-132">參數 pM 包含轉換矩陣的反向變換。</span><span class="sxs-lookup"><span data-stu-id="1aa5c-132">The parameter pM contains the inverse transpose of the transformation matrix.</span></span> <span data-ttu-id="1aa5c-133">這個方法需要反向變換，如此一來，已轉換之平面的一般向量也可以正確轉換。</span><span class="sxs-lookup"><span data-stu-id="1aa5c-133">The inverse transpose is required by this method so that the normal vector of the transformed plane can be correctly transformed as well.</span></span>

## <a name="requirements"></a><span data-ttu-id="1aa5c-134">規格需求</span><span class="sxs-lookup"><span data-stu-id="1aa5c-134">Requirements</span></span>



| <span data-ttu-id="1aa5c-135">需求</span><span class="sxs-lookup"><span data-stu-id="1aa5c-135">Requirement</span></span> | <span data-ttu-id="1aa5c-136">值</span><span class="sxs-lookup"><span data-stu-id="1aa5c-136">Value</span></span> |
|--------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="1aa5c-137">標頭</span><span class="sxs-lookup"><span data-stu-id="1aa5c-137">Header</span></span><br/>  | <dl> <span data-ttu-id="1aa5c-138"><dt>D3DX10Math。h</dt></span><span class="sxs-lookup"><span data-stu-id="1aa5c-138"><dt>D3DX10Math.h</dt></span></span> </dl> |
| <span data-ttu-id="1aa5c-139">程式庫</span><span class="sxs-lookup"><span data-stu-id="1aa5c-139">Library</span></span><br/> | <dl> <span data-ttu-id="1aa5c-140"><dt>D3DX10 .lib</dt></span><span class="sxs-lookup"><span data-stu-id="1aa5c-140"><dt>D3DX10.lib</dt></span></span> </dl>   |



## <a name="see-also"></a><span data-ttu-id="1aa5c-141">另請參閱</span><span class="sxs-lookup"><span data-stu-id="1aa5c-141">See also</span></span>

<dl> <dt>

[<span data-ttu-id="1aa5c-142">數學函數</span><span class="sxs-lookup"><span data-stu-id="1aa5c-142">Math Functions</span></span>](d3d10-graphics-reference-d3dx10-functions-math.md)
</dt> </dl>

 

 
