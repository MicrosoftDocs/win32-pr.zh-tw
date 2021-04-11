---
description: 建立圍繞任意軸旋轉的矩陣。
ms.assetid: dc4b8b3f-e1d2-475f-9dcb-622ada9fae6b
title: 'D3DXMatrixRotationAxis 函式 (D3DX10Math) '
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- D3DXMatrixRotationAxis
api_type:
- LibDef
api_location:
- D3DX10.lib
- D3DX10.dll
ms.openlocfilehash: bba74aa7258b39b8fdbbb8cab09684a14bfbda91
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 03/15/2021
ms.locfileid: "104035412"
---
# <a name="d3dxmatrixrotationaxis-function-d3dx10mathh"></a><span data-ttu-id="160ef-103">D3DXMatrixRotationAxis 函式 (D3DX10Math) </span><span class="sxs-lookup"><span data-stu-id="160ef-103">D3DXMatrixRotationAxis function (D3DX10Math.h)</span></span>

<span data-ttu-id="160ef-104">建立圍繞任意軸旋轉的矩陣。</span><span class="sxs-lookup"><span data-stu-id="160ef-104">Builds a matrix that rotates around an arbitrary axis.</span></span>

## <a name="syntax"></a><span data-ttu-id="160ef-105">語法</span><span class="sxs-lookup"><span data-stu-id="160ef-105">Syntax</span></span>


```C++
D3DXMATRIX* D3DXMatrixRotationAxis(
  _Inout_       D3DXMATRIX  *pOut,
  _In_    const D3DXVECTOR3 *pV,
  _In_          FLOAT       Angle
);
```



## <a name="parameters"></a><span data-ttu-id="160ef-106">參數</span><span class="sxs-lookup"><span data-stu-id="160ef-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="160ef-107">*不悅* \[in、out\]</span><span class="sxs-lookup"><span data-stu-id="160ef-107">*pOut* \[in, out\]</span></span>
</dt> <dd>

<span data-ttu-id="160ef-108">類型： **[ **D3DXMATRIX**](../direct3d9/d3dxmatrix.md)\***</span><span class="sxs-lookup"><span data-stu-id="160ef-108">Type: **[**D3DXMATRIX**](../direct3d9/d3dxmatrix.md)\***</span></span>

<span data-ttu-id="160ef-109">[**D3DXMATRIX**](d3d10-d3dxmatrix.md)結構的指標，此結構是作業的結果。</span><span class="sxs-lookup"><span data-stu-id="160ef-109">Pointer to the [**D3DXMATRIX**](d3d10-d3dxmatrix.md) structure that is the result of the operation.</span></span>

</dd> <dt>

<span data-ttu-id="160ef-110">*pV* \[在\]</span><span class="sxs-lookup"><span data-stu-id="160ef-110">*pV* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="160ef-111">Type： **Const [**D3DXVECTOR3**](../direct3d9/d3dxvector3.md) \***</span><span class="sxs-lookup"><span data-stu-id="160ef-111">Type: **const [**D3DXVECTOR3**](../direct3d9/d3dxvector3.md)\***</span></span>

<span data-ttu-id="160ef-112">任意軸的指標。</span><span class="sxs-lookup"><span data-stu-id="160ef-112">Pointer to the arbitrary axis.</span></span> <span data-ttu-id="160ef-113">請參閱 [**D3DXVECTOR3**](d3d10-d3dxvector3.md)。</span><span class="sxs-lookup"><span data-stu-id="160ef-113">See [**D3DXVECTOR3**](d3d10-d3dxvector3.md).</span></span>

</dd> <dt>

<span data-ttu-id="160ef-114">*角度* \[在\]</span><span class="sxs-lookup"><span data-stu-id="160ef-114">*Angle* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="160ef-115">類型： **[ **FLOAT**](../winprog/windows-data-types.md)**</span><span class="sxs-lookup"><span data-stu-id="160ef-115">Type: **[**FLOAT**](../winprog/windows-data-types.md)**</span></span>

<span data-ttu-id="160ef-116">旋轉的角度，以弧度為單位。</span><span class="sxs-lookup"><span data-stu-id="160ef-116">Angle of rotation in radians.</span></span> <span data-ttu-id="160ef-117">沿著旋轉軸向原點方向看時，角度是順時針方向測量。</span><span class="sxs-lookup"><span data-stu-id="160ef-117">Angles are measured clockwise when looking along the rotation axis toward the origin.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="160ef-118">傳回值</span><span class="sxs-lookup"><span data-stu-id="160ef-118">Return value</span></span>

<span data-ttu-id="160ef-119">類型： **[ **D3DXMATRIX**](../direct3d9/d3dxmatrix.md)\***</span><span class="sxs-lookup"><span data-stu-id="160ef-119">Type: **[**D3DXMATRIX**](../direct3d9/d3dxmatrix.md)\***</span></span>

<span data-ttu-id="160ef-120">圍繞指定軸旋轉之 D3DXMATRIX 結構的指標。</span><span class="sxs-lookup"><span data-stu-id="160ef-120">Pointer to a D3DXMATRIX structure rotated around the specified axis.</span></span>

## <a name="remarks"></a><span data-ttu-id="160ef-121">備註</span><span class="sxs-lookup"><span data-stu-id="160ef-121">Remarks</span></span>

<span data-ttu-id="160ef-122">此函式的傳回值與不悅參數中所傳回的值相同。</span><span class="sxs-lookup"><span data-stu-id="160ef-122">The return value for this function is the same value returned in the pOut parameter.</span></span> <span data-ttu-id="160ef-123">如此一來，D3DXMatrixRotationAxis 函式就可以用來做為另一個函式的參數。</span><span class="sxs-lookup"><span data-stu-id="160ef-123">In this way, the D3DXMatrixRotationAxis function can be used as a parameter for another function.</span></span>

## <a name="requirements"></a><span data-ttu-id="160ef-124">規格需求</span><span class="sxs-lookup"><span data-stu-id="160ef-124">Requirements</span></span>



| <span data-ttu-id="160ef-125">需求</span><span class="sxs-lookup"><span data-stu-id="160ef-125">Requirement</span></span> | <span data-ttu-id="160ef-126">值</span><span class="sxs-lookup"><span data-stu-id="160ef-126">Value</span></span> |
|--------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="160ef-127">標頭</span><span class="sxs-lookup"><span data-stu-id="160ef-127">Header</span></span><br/>  | <dl> <span data-ttu-id="160ef-128"><dt>D3DX10Math。h</dt></span><span class="sxs-lookup"><span data-stu-id="160ef-128"><dt>D3DX10Math.h</dt></span></span> </dl> |
| <span data-ttu-id="160ef-129">程式庫</span><span class="sxs-lookup"><span data-stu-id="160ef-129">Library</span></span><br/> | <dl> <span data-ttu-id="160ef-130"><dt>D3DX10 .lib</dt></span><span class="sxs-lookup"><span data-stu-id="160ef-130"><dt>D3DX10.lib</dt></span></span> </dl>   |



## <a name="see-also"></a><span data-ttu-id="160ef-131">另請參閱</span><span class="sxs-lookup"><span data-stu-id="160ef-131">See also</span></span>

<dl> <dt>

[<span data-ttu-id="160ef-132">數學函數</span><span class="sxs-lookup"><span data-stu-id="160ef-132">Math Functions</span></span>](d3d10-graphics-reference-d3dx10-functions-math.md)
</dt> </dl>

 

 
