---
description: D3DXMatrixRotationAxis 函式 (D3dx9math) -建立可圍繞任意軸旋轉的矩陣。
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
ms.openlocfilehash: 720ac4d3bdae2910cee7913b9c34316d72526688
ms.sourcegitcommit: 95685061d5b0333bbf9e6ebd208dde8190f97005
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 04/28/2021
ms.locfileid: "108118186"
---
# <a name="d3dxmatrixrotationaxis-function-d3dx9mathh"></a><span data-ttu-id="e33fd-103">D3DXMatrixRotationAxis 函式 (D3dx9math) </span><span class="sxs-lookup"><span data-stu-id="e33fd-103">D3DXMatrixRotationAxis function (D3dx9math.h)</span></span>

<span data-ttu-id="e33fd-104">建立圍繞任意軸旋轉的矩陣。</span><span class="sxs-lookup"><span data-stu-id="e33fd-104">Builds a matrix that rotates around an arbitrary axis.</span></span>

## <a name="syntax"></a><span data-ttu-id="e33fd-105">語法</span><span class="sxs-lookup"><span data-stu-id="e33fd-105">Syntax</span></span>


```C++
D3DXMATRIX* D3DXMatrixRotationAxis(
  _Inout_       D3DXMATRIX  *pOut,
  _In_    const D3DXVECTOR3 *pV,
  _In_          FLOAT       Angle
);
```



## <a name="parameters"></a><span data-ttu-id="e33fd-106">參數</span><span class="sxs-lookup"><span data-stu-id="e33fd-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="e33fd-107">*不悅* \[in、out\]</span><span class="sxs-lookup"><span data-stu-id="e33fd-107">*pOut* \[in, out\]</span></span>
</dt> <dd>

<span data-ttu-id="e33fd-108">類型： **[ **D3DXMATRIX**](d3dxmatrix.md)\***</span><span class="sxs-lookup"><span data-stu-id="e33fd-108">Type: **[**D3DXMATRIX**](d3dxmatrix.md)\***</span></span>

<span data-ttu-id="e33fd-109">[**D3DXMATRIX**](d3dxmatrix.md)結構的指標，此結構是作業的結果。</span><span class="sxs-lookup"><span data-stu-id="e33fd-109">Pointer to the [**D3DXMATRIX**](d3dxmatrix.md) structure that is the result of the operation.</span></span>

</dd> <dt>

<span data-ttu-id="e33fd-110">*pV* \[在\]</span><span class="sxs-lookup"><span data-stu-id="e33fd-110">*pV* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="e33fd-111">Type： **Const [**D3DXVECTOR3**](d3dxvector3.md) \***</span><span class="sxs-lookup"><span data-stu-id="e33fd-111">Type: **const [**D3DXVECTOR3**](d3dxvector3.md)\***</span></span>

<span data-ttu-id="e33fd-112">任意軸的指標。</span><span class="sxs-lookup"><span data-stu-id="e33fd-112">Pointer to the arbitrary axis.</span></span> <span data-ttu-id="e33fd-113">請參閱 [**D3DXVECTOR3**](d3dxvector3.md)。</span><span class="sxs-lookup"><span data-stu-id="e33fd-113">See [**D3DXVECTOR3**](d3dxvector3.md).</span></span>

</dd> <dt>

<span data-ttu-id="e33fd-114">*角度* \[在\]</span><span class="sxs-lookup"><span data-stu-id="e33fd-114">*Angle* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="e33fd-115">類型： **[ **FLOAT**](../winprog/windows-data-types.md)**</span><span class="sxs-lookup"><span data-stu-id="e33fd-115">Type: **[**FLOAT**](../winprog/windows-data-types.md)**</span></span>

<span data-ttu-id="e33fd-116">旋轉的角度，以弧度為單位。</span><span class="sxs-lookup"><span data-stu-id="e33fd-116">Angle of rotation in radians.</span></span> <span data-ttu-id="e33fd-117">沿著旋轉軸向原點方向看時，角度是順時針方向測量。</span><span class="sxs-lookup"><span data-stu-id="e33fd-117">Angles are measured clockwise when looking along the rotation axis toward the origin.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="e33fd-118">傳回值</span><span class="sxs-lookup"><span data-stu-id="e33fd-118">Return value</span></span>

<span data-ttu-id="e33fd-119">類型： **[ **D3DXMATRIX**](d3dxmatrix.md)\***</span><span class="sxs-lookup"><span data-stu-id="e33fd-119">Type: **[**D3DXMATRIX**](d3dxmatrix.md)\***</span></span>

<span data-ttu-id="e33fd-120">圍繞指定軸旋轉之 [**D3DXMATRIX**](d3dxmatrix.md) 結構的指標。</span><span class="sxs-lookup"><span data-stu-id="e33fd-120">Pointer to a [**D3DXMATRIX**](d3dxmatrix.md) structure rotated around the specified axis.</span></span>

## <a name="remarks"></a><span data-ttu-id="e33fd-121">備註</span><span class="sxs-lookup"><span data-stu-id="e33fd-121">Remarks</span></span>

<span data-ttu-id="e33fd-122">此函式的傳回值與 *不悅* 參數中所傳回的值相同。</span><span class="sxs-lookup"><span data-stu-id="e33fd-122">The return value for this function is the same value returned in the *pOut* parameter.</span></span> <span data-ttu-id="e33fd-123">如此一來， **D3DXMatrixRotationAxis** 函式就可以用來做為另一個函式的參數。</span><span class="sxs-lookup"><span data-stu-id="e33fd-123">In this way, the **D3DXMatrixRotationAxis** function can be used as a parameter for another function.</span></span>

## <a name="requirements"></a><span data-ttu-id="e33fd-124">規格需求</span><span class="sxs-lookup"><span data-stu-id="e33fd-124">Requirements</span></span>



| <span data-ttu-id="e33fd-125">需求</span><span class="sxs-lookup"><span data-stu-id="e33fd-125">Requirement</span></span> | <span data-ttu-id="e33fd-126">值</span><span class="sxs-lookup"><span data-stu-id="e33fd-126">Value</span></span> |
|--------------------|----------------------------------------------------------------------------------------|
| <span data-ttu-id="e33fd-127">標頭</span><span class="sxs-lookup"><span data-stu-id="e33fd-127">Header</span></span><br/>  | <dl> <span data-ttu-id="e33fd-128"><dt>D3dx9math。h</dt></span><span class="sxs-lookup"><span data-stu-id="e33fd-128"><dt>D3dx9math.h</dt></span></span> </dl> |
| <span data-ttu-id="e33fd-129">程式庫</span><span class="sxs-lookup"><span data-stu-id="e33fd-129">Library</span></span><br/> | <dl> <span data-ttu-id="e33fd-130"><dt>D3dx9 .lib</dt></span><span class="sxs-lookup"><span data-stu-id="e33fd-130"><dt>D3dx9.lib</dt></span></span> </dl>   |



## <a name="see-also"></a><span data-ttu-id="e33fd-131">另請參閱</span><span class="sxs-lookup"><span data-stu-id="e33fd-131">See also</span></span>

<dl> <dt>

[<span data-ttu-id="e33fd-132">數學函數</span><span class="sxs-lookup"><span data-stu-id="e33fd-132">Math Functions</span></span>](dx9-graphics-reference-d3dx-functions-math.md)
</dt> <dt>

[<span data-ttu-id="e33fd-133">**D3DXMatrixRotationQuaternion**</span><span class="sxs-lookup"><span data-stu-id="e33fd-133">**D3DXMatrixRotationQuaternion**</span></span>](d3dxmatrixrotationquaternion.md)
</dt> <dt>

[<span data-ttu-id="e33fd-134">**D3DXMatrixRotationX**</span><span class="sxs-lookup"><span data-stu-id="e33fd-134">**D3DXMatrixRotationX**</span></span>](d3dxmatrixrotationx.md)
</dt> <dt>

[<span data-ttu-id="e33fd-135">**D3DXMatrixRotationY**</span><span class="sxs-lookup"><span data-stu-id="e33fd-135">**D3DXMatrixRotationY**</span></span>](d3dxmatrixrotationy.md)
</dt> <dt>

[<span data-ttu-id="e33fd-136">**D3DXMatrixRotationYawPitchRoll**</span><span class="sxs-lookup"><span data-stu-id="e33fd-136">**D3DXMatrixRotationYawPitchRoll**</span></span>](d3dxmatrixrotationyawpitchroll.md)
</dt> <dt>

[<span data-ttu-id="e33fd-137">**D3DXMatrixRotationZ**</span><span class="sxs-lookup"><span data-stu-id="e33fd-137">**D3DXMatrixRotationZ**</span></span>](d3dxmatrixrotationz.md)
</dt> </dl>

 

 
