---
description: D3DXMatrixRotationY 函式 (D3dx9math) -建立圍繞 y 軸旋轉的矩陣。
ms.assetid: 80449e5d-f9bb-48c0-a787-a5e5a9d1c9a3
title: 'D3DXMatrixRotationY 函式 (D3dx9math) '
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- D3DXMatrixRotationY
api_type:
- LibDef
api_location:
- d3dx9.lib
- d3dx9.dll
ms.openlocfilehash: 902325890b02416e796940388bca7a6548773be5
ms.sourcegitcommit: 95685061d5b0333bbf9e6ebd208dde8190f97005
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 04/28/2021
ms.locfileid: "108118126"
---
# <a name="d3dxmatrixrotationy-function-d3dx9mathh"></a><span data-ttu-id="b5aa7-103">D3DXMatrixRotationY 函式 (D3dx9math) </span><span class="sxs-lookup"><span data-stu-id="b5aa7-103">D3DXMatrixRotationY function (D3dx9math.h)</span></span>

<span data-ttu-id="b5aa7-104">建立圍繞 y 軸旋轉的矩陣。</span><span class="sxs-lookup"><span data-stu-id="b5aa7-104">Builds a matrix that rotates around the y-axis.</span></span>

## <a name="syntax"></a><span data-ttu-id="b5aa7-105">語法</span><span class="sxs-lookup"><span data-stu-id="b5aa7-105">Syntax</span></span>


```C++
D3DXMATRIX* D3DXMatrixRotationY(
  _Inout_ D3DXMATRIX *pOut,
  _In_    FLOAT      Angle
);
```



## <a name="parameters"></a><span data-ttu-id="b5aa7-106">參數</span><span class="sxs-lookup"><span data-stu-id="b5aa7-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="b5aa7-107">*不悅* \[in、out\]</span><span class="sxs-lookup"><span data-stu-id="b5aa7-107">*pOut* \[in, out\]</span></span>
</dt> <dd>

<span data-ttu-id="b5aa7-108">類型： **[ **D3DXMATRIX**](d3dxmatrix.md)\***</span><span class="sxs-lookup"><span data-stu-id="b5aa7-108">Type: **[**D3DXMATRIX**](d3dxmatrix.md)\***</span></span>

<span data-ttu-id="b5aa7-109">[**D3DXMATRIX**](d3dxmatrix.md)結構的指標，此結構是作業的結果。</span><span class="sxs-lookup"><span data-stu-id="b5aa7-109">Pointer to the [**D3DXMATRIX**](d3dxmatrix.md) structure that is the result of the operation.</span></span>

</dd> <dt>

<span data-ttu-id="b5aa7-110">*角度* \[在\]</span><span class="sxs-lookup"><span data-stu-id="b5aa7-110">*Angle* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="b5aa7-111">類型： **[ **FLOAT**](../winprog/windows-data-types.md)**</span><span class="sxs-lookup"><span data-stu-id="b5aa7-111">Type: **[**FLOAT**](../winprog/windows-data-types.md)**</span></span>

<span data-ttu-id="b5aa7-112">旋轉的角度，以弧度為單位。</span><span class="sxs-lookup"><span data-stu-id="b5aa7-112">Angle of rotation in radians.</span></span> <span data-ttu-id="b5aa7-113">沿著旋轉軸向原點方向看時，角度是順時針方向測量。</span><span class="sxs-lookup"><span data-stu-id="b5aa7-113">Angles are measured clockwise when looking along the rotation axis toward the origin.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="b5aa7-114">傳回值</span><span class="sxs-lookup"><span data-stu-id="b5aa7-114">Return value</span></span>

<span data-ttu-id="b5aa7-115">類型： **[ **D3DXMATRIX**](d3dxmatrix.md)\***</span><span class="sxs-lookup"><span data-stu-id="b5aa7-115">Type: **[**D3DXMATRIX**](d3dxmatrix.md)\***</span></span>

<span data-ttu-id="b5aa7-116">圍繞 y 軸旋轉之 [**D3DXMATRIX**](d3dxmatrix.md) 結構的指標。</span><span class="sxs-lookup"><span data-stu-id="b5aa7-116">Pointer to a [**D3DXMATRIX**](d3dxmatrix.md) structure rotated around the y-axis.</span></span>

## <a name="remarks"></a><span data-ttu-id="b5aa7-117">備註</span><span class="sxs-lookup"><span data-stu-id="b5aa7-117">Remarks</span></span>

<span data-ttu-id="b5aa7-118">此函式的傳回值與 *不悅* 參數中所傳回的值相同。</span><span class="sxs-lookup"><span data-stu-id="b5aa7-118">The return value for this function is the same value returned in the *pOut* parameter.</span></span> <span data-ttu-id="b5aa7-119">如此一來， **D3DXMatrixRotationY** 函式就可以用來做為另一個函式的參數。</span><span class="sxs-lookup"><span data-stu-id="b5aa7-119">In this way, the **D3DXMatrixRotationY** function can be used as a parameter for another function.</span></span>

## <a name="requirements"></a><span data-ttu-id="b5aa7-120">規格需求</span><span class="sxs-lookup"><span data-stu-id="b5aa7-120">Requirements</span></span>



| <span data-ttu-id="b5aa7-121">需求</span><span class="sxs-lookup"><span data-stu-id="b5aa7-121">Requirement</span></span> | <span data-ttu-id="b5aa7-122">值</span><span class="sxs-lookup"><span data-stu-id="b5aa7-122">Value</span></span> |
|--------------------|----------------------------------------------------------------------------------------|
| <span data-ttu-id="b5aa7-123">標頭</span><span class="sxs-lookup"><span data-stu-id="b5aa7-123">Header</span></span><br/>  | <dl> <span data-ttu-id="b5aa7-124"><dt>D3dx9math。h</dt></span><span class="sxs-lookup"><span data-stu-id="b5aa7-124"><dt>D3dx9math.h</dt></span></span> </dl> |
| <span data-ttu-id="b5aa7-125">程式庫</span><span class="sxs-lookup"><span data-stu-id="b5aa7-125">Library</span></span><br/> | <dl> <span data-ttu-id="b5aa7-126"><dt>D3dx9 .lib</dt></span><span class="sxs-lookup"><span data-stu-id="b5aa7-126"><dt>D3dx9.lib</dt></span></span> </dl>   |



## <a name="see-also"></a><span data-ttu-id="b5aa7-127">另請參閱</span><span class="sxs-lookup"><span data-stu-id="b5aa7-127">See also</span></span>

<dl> <dt>

[<span data-ttu-id="b5aa7-128">數學函數</span><span class="sxs-lookup"><span data-stu-id="b5aa7-128">Math Functions</span></span>](dx9-graphics-reference-d3dx-functions-math.md)
</dt> <dt>

[<span data-ttu-id="b5aa7-129">**D3DXMatrixRotationAxis**</span><span class="sxs-lookup"><span data-stu-id="b5aa7-129">**D3DXMatrixRotationAxis**</span></span>](d3dxmatrixrotationaxis.md)
</dt> <dt>

[<span data-ttu-id="b5aa7-130">**D3DXMatrixRotationQuaternion**</span><span class="sxs-lookup"><span data-stu-id="b5aa7-130">**D3DXMatrixRotationQuaternion**</span></span>](d3dxmatrixrotationquaternion.md)
</dt> <dt>

[<span data-ttu-id="b5aa7-131">**D3DXMatrixRotationX**</span><span class="sxs-lookup"><span data-stu-id="b5aa7-131">**D3DXMatrixRotationX**</span></span>](d3dxmatrixrotationx.md)
</dt> <dt>

[<span data-ttu-id="b5aa7-132">**D3DXMatrixRotationYawPitchRoll**</span><span class="sxs-lookup"><span data-stu-id="b5aa7-132">**D3DXMatrixRotationYawPitchRoll**</span></span>](d3dxmatrixrotationyawpitchroll.md)
</dt> <dt>

[<span data-ttu-id="b5aa7-133">**D3DXMatrixRotationZ**</span><span class="sxs-lookup"><span data-stu-id="b5aa7-133">**D3DXMatrixRotationZ**</span></span>](d3dxmatrixrotationz.md)
</dt> </dl>

 

 
