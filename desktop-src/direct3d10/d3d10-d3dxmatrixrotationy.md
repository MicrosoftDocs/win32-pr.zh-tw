---
description: D3DXMatrixRotationY 函式 (D3DX10Math) -建立圍繞 y 軸旋轉的矩陣。
ms.assetid: b58def9b-29dc-4c7d-89a3-188ef9b9f94f
title: 'D3DXMatrixRotationY 函式 (D3DX10Math) '
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
- D3DX10.lib
- D3DX10.dll
ms.openlocfilehash: 570179fadc9008c5f919acf657541e53ab399ac8
ms.sourcegitcommit: 95685061d5b0333bbf9e6ebd208dde8190f97005
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 04/28/2021
ms.locfileid: "108108966"
---
# <a name="d3dxmatrixrotationy-function-d3dx10mathh"></a><span data-ttu-id="f1acd-103">D3DXMatrixRotationY 函式 (D3DX10Math) </span><span class="sxs-lookup"><span data-stu-id="f1acd-103">D3DXMatrixRotationY function (D3DX10Math.h)</span></span>

<span data-ttu-id="f1acd-104">建立圍繞 y 軸旋轉的矩陣。</span><span class="sxs-lookup"><span data-stu-id="f1acd-104">Builds a matrix that rotates around the y-axis.</span></span>

## <a name="syntax"></a><span data-ttu-id="f1acd-105">語法</span><span class="sxs-lookup"><span data-stu-id="f1acd-105">Syntax</span></span>


```C++
D3DXMATRIX* D3DXMatrixRotationY(
  _Inout_ D3DXMATRIX *pOut,
  _In_    FLOAT      Angle
);
```



## <a name="parameters"></a><span data-ttu-id="f1acd-106">參數</span><span class="sxs-lookup"><span data-stu-id="f1acd-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="f1acd-107">*不悅* \[in、out\]</span><span class="sxs-lookup"><span data-stu-id="f1acd-107">*pOut* \[in, out\]</span></span>
</dt> <dd>

<span data-ttu-id="f1acd-108">類型： **[ **D3DXMATRIX**](../direct3d9/d3dxmatrix.md)\***</span><span class="sxs-lookup"><span data-stu-id="f1acd-108">Type: **[**D3DXMATRIX**](../direct3d9/d3dxmatrix.md)\***</span></span>

<span data-ttu-id="f1acd-109">[**D3DXMATRIX**](d3d10-d3dxmatrix.md)結構的指標，此結構是作業的結果。</span><span class="sxs-lookup"><span data-stu-id="f1acd-109">Pointer to the [**D3DXMATRIX**](d3d10-d3dxmatrix.md) structure that is the result of the operation.</span></span>

</dd> <dt>

<span data-ttu-id="f1acd-110">*角度* \[在\]</span><span class="sxs-lookup"><span data-stu-id="f1acd-110">*Angle* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="f1acd-111">類型： **[ **FLOAT**](../winprog/windows-data-types.md)**</span><span class="sxs-lookup"><span data-stu-id="f1acd-111">Type: **[**FLOAT**](../winprog/windows-data-types.md)**</span></span>

<span data-ttu-id="f1acd-112">旋轉的角度，以弧度為單位。</span><span class="sxs-lookup"><span data-stu-id="f1acd-112">Angle of rotation in radians.</span></span> <span data-ttu-id="f1acd-113">沿著旋轉軸向原點方向看時，角度是順時針方向測量。</span><span class="sxs-lookup"><span data-stu-id="f1acd-113">Angles are measured clockwise when looking along the rotation axis toward the origin.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="f1acd-114">傳回值</span><span class="sxs-lookup"><span data-stu-id="f1acd-114">Return value</span></span>

<span data-ttu-id="f1acd-115">類型： **[ **D3DXMATRIX**](../direct3d9/d3dxmatrix.md)\***</span><span class="sxs-lookup"><span data-stu-id="f1acd-115">Type: **[**D3DXMATRIX**](../direct3d9/d3dxmatrix.md)\***</span></span>

<span data-ttu-id="f1acd-116">圍繞 y 軸旋轉之 D3DXMATRIX 結構的指標。</span><span class="sxs-lookup"><span data-stu-id="f1acd-116">Pointer to a D3DXMATRIX structure rotated around the y-axis.</span></span>

## <a name="remarks"></a><span data-ttu-id="f1acd-117">備註</span><span class="sxs-lookup"><span data-stu-id="f1acd-117">Remarks</span></span>

<span data-ttu-id="f1acd-118">此函式的傳回值與不悅參數中所傳回的值相同。</span><span class="sxs-lookup"><span data-stu-id="f1acd-118">The return value for this function is the same value returned in the pOut parameter.</span></span> <span data-ttu-id="f1acd-119">如此一來，D3DXMatrixRotationY 函式就可以用來做為另一個函式的參數。</span><span class="sxs-lookup"><span data-stu-id="f1acd-119">In this way, the D3DXMatrixRotationY function can be used as a parameter for another function.</span></span>

## <a name="requirements"></a><span data-ttu-id="f1acd-120">規格需求</span><span class="sxs-lookup"><span data-stu-id="f1acd-120">Requirements</span></span>



| <span data-ttu-id="f1acd-121">需求</span><span class="sxs-lookup"><span data-stu-id="f1acd-121">Requirement</span></span> | <span data-ttu-id="f1acd-122">值</span><span class="sxs-lookup"><span data-stu-id="f1acd-122">Value</span></span> |
|--------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="f1acd-123">標頭</span><span class="sxs-lookup"><span data-stu-id="f1acd-123">Header</span></span><br/>  | <dl> <span data-ttu-id="f1acd-124"><dt>D3DX10Math。h</dt></span><span class="sxs-lookup"><span data-stu-id="f1acd-124"><dt>D3DX10Math.h</dt></span></span> </dl> |
| <span data-ttu-id="f1acd-125">程式庫</span><span class="sxs-lookup"><span data-stu-id="f1acd-125">Library</span></span><br/> | <dl> <span data-ttu-id="f1acd-126"><dt>D3DX10 .lib</dt></span><span class="sxs-lookup"><span data-stu-id="f1acd-126"><dt>D3DX10.lib</dt></span></span> </dl>   |



## <a name="see-also"></a><span data-ttu-id="f1acd-127">另請參閱</span><span class="sxs-lookup"><span data-stu-id="f1acd-127">See also</span></span>

<dl> <dt>

[<span data-ttu-id="f1acd-128">數學函數</span><span class="sxs-lookup"><span data-stu-id="f1acd-128">Math Functions</span></span>](d3d10-graphics-reference-d3dx10-functions-math.md)
</dt> </dl>

 

 
