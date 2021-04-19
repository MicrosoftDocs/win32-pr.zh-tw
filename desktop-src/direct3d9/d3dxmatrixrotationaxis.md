---
description: 建立圍繞任意軸旋轉的矩陣。
ms.assetid: 368c8f64-7709-4200-94d3-3dbc92a960c1
title: 'D3DXMatrixRotationAxis 函式 (D3dx9math) '
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
- d3dx9.lib
- d3dx9.dll
ms.openlocfilehash: fffc4a5bdd287c79352beb3ee0eeaf97b0573753
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 03/15/2021
ms.locfileid: "106993856"
---
# <a name="d3dxmatrixrotationaxis-function-d3dx9mathh"></a><span data-ttu-id="ef284-103">D3DXMatrixRotationAxis 函式 (D3dx9math) </span><span class="sxs-lookup"><span data-stu-id="ef284-103">D3DXMatrixRotationAxis function (D3dx9math.h)</span></span>

<span data-ttu-id="ef284-104">建立圍繞任意軸旋轉的矩陣。</span><span class="sxs-lookup"><span data-stu-id="ef284-104">Builds a matrix that rotates around an arbitrary axis.</span></span>

## <a name="syntax"></a><span data-ttu-id="ef284-105">語法</span><span class="sxs-lookup"><span data-stu-id="ef284-105">Syntax</span></span>


```C++
D3DXMATRIX* D3DXMatrixRotationAxis(
  _Inout_       D3DXMATRIX  *pOut,
  _In_    const D3DXVECTOR3 *pV,
  _In_          FLOAT       Angle
);
```



## <a name="parameters"></a><span data-ttu-id="ef284-106">參數</span><span class="sxs-lookup"><span data-stu-id="ef284-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="ef284-107">*不悅* \[in、out\]</span><span class="sxs-lookup"><span data-stu-id="ef284-107">*pOut* \[in, out\]</span></span>
</dt> <dd>

<span data-ttu-id="ef284-108">類型： **[ **D3DXMATRIX**](d3dxmatrix.md)\***</span><span class="sxs-lookup"><span data-stu-id="ef284-108">Type: **[**D3DXMATRIX**](d3dxmatrix.md)\***</span></span>

<span data-ttu-id="ef284-109">[**D3DXMATRIX**](d3dxmatrix.md)結構的指標，此結構是作業的結果。</span><span class="sxs-lookup"><span data-stu-id="ef284-109">Pointer to the [**D3DXMATRIX**](d3dxmatrix.md) structure that is the result of the operation.</span></span>

</dd> <dt>

<span data-ttu-id="ef284-110">*pV* \[在\]</span><span class="sxs-lookup"><span data-stu-id="ef284-110">*pV* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="ef284-111">Type： **Const [**D3DXVECTOR3**](d3dxvector3.md) \***</span><span class="sxs-lookup"><span data-stu-id="ef284-111">Type: **const [**D3DXVECTOR3**](d3dxvector3.md)\***</span></span>

<span data-ttu-id="ef284-112">任意軸的指標。</span><span class="sxs-lookup"><span data-stu-id="ef284-112">Pointer to the arbitrary axis.</span></span> <span data-ttu-id="ef284-113">請參閱 [**D3DXVECTOR3**](d3dxvector3.md)。</span><span class="sxs-lookup"><span data-stu-id="ef284-113">See [**D3DXVECTOR3**](d3dxvector3.md).</span></span>

</dd> <dt>

<span data-ttu-id="ef284-114">*角度* \[在\]</span><span class="sxs-lookup"><span data-stu-id="ef284-114">*Angle* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="ef284-115">類型： **[ **FLOAT**](../winprog/windows-data-types.md)**</span><span class="sxs-lookup"><span data-stu-id="ef284-115">Type: **[**FLOAT**](../winprog/windows-data-types.md)**</span></span>

<span data-ttu-id="ef284-116">旋轉的角度，以弧度為單位。</span><span class="sxs-lookup"><span data-stu-id="ef284-116">Angle of rotation in radians.</span></span> <span data-ttu-id="ef284-117">沿著旋轉軸向原點方向看時，角度是順時針方向測量。</span><span class="sxs-lookup"><span data-stu-id="ef284-117">Angles are measured clockwise when looking along the rotation axis toward the origin.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="ef284-118">傳回值</span><span class="sxs-lookup"><span data-stu-id="ef284-118">Return value</span></span>

<span data-ttu-id="ef284-119">類型： **[ **D3DXMATRIX**](d3dxmatrix.md)\***</span><span class="sxs-lookup"><span data-stu-id="ef284-119">Type: **[**D3DXMATRIX**](d3dxmatrix.md)\***</span></span>

<span data-ttu-id="ef284-120">圍繞指定軸旋轉之 [**D3DXMATRIX**](d3dxmatrix.md) 結構的指標。</span><span class="sxs-lookup"><span data-stu-id="ef284-120">Pointer to a [**D3DXMATRIX**](d3dxmatrix.md) structure rotated around the specified axis.</span></span>

## <a name="remarks"></a><span data-ttu-id="ef284-121">備註</span><span class="sxs-lookup"><span data-stu-id="ef284-121">Remarks</span></span>

<span data-ttu-id="ef284-122">此函式的傳回值與 *不悅* 參數中所傳回的值相同。</span><span class="sxs-lookup"><span data-stu-id="ef284-122">The return value for this function is the same value returned in the *pOut* parameter.</span></span> <span data-ttu-id="ef284-123">如此一來， **D3DXMatrixRotationAxis** 函式就可以用來做為另一個函式的參數。</span><span class="sxs-lookup"><span data-stu-id="ef284-123">In this way, the **D3DXMatrixRotationAxis** function can be used as a parameter for another function.</span></span>

## <a name="requirements"></a><span data-ttu-id="ef284-124">規格需求</span><span class="sxs-lookup"><span data-stu-id="ef284-124">Requirements</span></span>



| <span data-ttu-id="ef284-125">需求</span><span class="sxs-lookup"><span data-stu-id="ef284-125">Requirement</span></span> | <span data-ttu-id="ef284-126">值</span><span class="sxs-lookup"><span data-stu-id="ef284-126">Value</span></span> |
|--------------------|----------------------------------------------------------------------------------------|
| <span data-ttu-id="ef284-127">標頭</span><span class="sxs-lookup"><span data-stu-id="ef284-127">Header</span></span><br/>  | <dl> <span data-ttu-id="ef284-128"><dt>D3dx9math。h</dt></span><span class="sxs-lookup"><span data-stu-id="ef284-128"><dt>D3dx9math.h</dt></span></span> </dl> |
| <span data-ttu-id="ef284-129">程式庫</span><span class="sxs-lookup"><span data-stu-id="ef284-129">Library</span></span><br/> | <dl> <span data-ttu-id="ef284-130"><dt>D3dx9 .lib</dt></span><span class="sxs-lookup"><span data-stu-id="ef284-130"><dt>D3dx9.lib</dt></span></span> </dl>   |



## <a name="see-also"></a><span data-ttu-id="ef284-131">另請參閱</span><span class="sxs-lookup"><span data-stu-id="ef284-131">See also</span></span>

<dl> <dt>

[<span data-ttu-id="ef284-132">數學函數</span><span class="sxs-lookup"><span data-stu-id="ef284-132">Math Functions</span></span>](dx9-graphics-reference-d3dx-functions-math.md)
</dt> <dt>

[<span data-ttu-id="ef284-133">**D3DXMatrixRotationQuaternion**</span><span class="sxs-lookup"><span data-stu-id="ef284-133">**D3DXMatrixRotationQuaternion**</span></span>](d3dxmatrixrotationquaternion.md)
</dt> <dt>

[<span data-ttu-id="ef284-134">**D3DXMatrixRotationX**</span><span class="sxs-lookup"><span data-stu-id="ef284-134">**D3DXMatrixRotationX**</span></span>](d3dxmatrixrotationx.md)
</dt> <dt>

[<span data-ttu-id="ef284-135">**D3DXMatrixRotationY**</span><span class="sxs-lookup"><span data-stu-id="ef284-135">**D3DXMatrixRotationY**</span></span>](d3dxmatrixrotationy.md)
</dt> <dt>

[<span data-ttu-id="ef284-136">**D3DXMatrixRotationYawPitchRoll**</span><span class="sxs-lookup"><span data-stu-id="ef284-136">**D3DXMatrixRotationYawPitchRoll**</span></span>](d3dxmatrixrotationyawpitchroll.md)
</dt> <dt>

[<span data-ttu-id="ef284-137">**D3DXMatrixRotationZ**</span><span class="sxs-lookup"><span data-stu-id="ef284-137">**D3DXMatrixRotationZ**</span></span>](d3dxmatrixrotationz.md)
</dt> </dl>

 

 
