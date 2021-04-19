---
description: 建立圍繞 X 軸旋轉的矩陣。
ms.assetid: 895079bf-b807-4bfd-9222-a7c1251d7d1e
title: 'D3DXMatrixRotationX 函式 (D3DX10Math) '
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- D3DXMatrixRotationX
api_type:
- LibDef
api_location:
- D3DX10.lib
- D3DX10.dll
ms.openlocfilehash: 5eade695a3b410877665557bd42d61d1d89b18e2
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 03/15/2021
ms.locfileid: "107000365"
---
# <a name="d3dxmatrixrotationx-function-d3dx10mathh"></a><span data-ttu-id="5dd77-103">D3DXMatrixRotationX 函式 (D3DX10Math) </span><span class="sxs-lookup"><span data-stu-id="5dd77-103">D3DXMatrixRotationX function (D3DX10Math.h)</span></span>

<span data-ttu-id="5dd77-104">建立圍繞 X 軸旋轉的矩陣。</span><span class="sxs-lookup"><span data-stu-id="5dd77-104">Builds a matrix that rotates around the x-axis.</span></span>

## <a name="syntax"></a><span data-ttu-id="5dd77-105">語法</span><span class="sxs-lookup"><span data-stu-id="5dd77-105">Syntax</span></span>


```C++
D3DXMATRIX* D3DXMatrixRotationX(
  _Inout_ D3DXMATRIX *pOut,
  _In_    FLOAT      Angle
);
```



## <a name="parameters"></a><span data-ttu-id="5dd77-106">參數</span><span class="sxs-lookup"><span data-stu-id="5dd77-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="5dd77-107">*不悅* \[in、out\]</span><span class="sxs-lookup"><span data-stu-id="5dd77-107">*pOut* \[in, out\]</span></span>
</dt> <dd>

<span data-ttu-id="5dd77-108">類型： **[ **D3DXMATRIX**](../direct3d9/d3dxmatrix.md)\***</span><span class="sxs-lookup"><span data-stu-id="5dd77-108">Type: **[**D3DXMATRIX**](../direct3d9/d3dxmatrix.md)\***</span></span>

<span data-ttu-id="5dd77-109">[**D3DXMATRIX**](d3d10-d3dxmatrix.md)結構的指標，此結構是作業的結果。</span><span class="sxs-lookup"><span data-stu-id="5dd77-109">Pointer to the [**D3DXMATRIX**](d3d10-d3dxmatrix.md) structure that is the result of the operation.</span></span>

</dd> <dt>

<span data-ttu-id="5dd77-110">*角度* \[在\]</span><span class="sxs-lookup"><span data-stu-id="5dd77-110">*Angle* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="5dd77-111">類型： **[ **FLOAT**](../winprog/windows-data-types.md)**</span><span class="sxs-lookup"><span data-stu-id="5dd77-111">Type: **[**FLOAT**](../winprog/windows-data-types.md)**</span></span>

<span data-ttu-id="5dd77-112">旋轉的角度，以弧度為單位。</span><span class="sxs-lookup"><span data-stu-id="5dd77-112">Angle of rotation in radians.</span></span> <span data-ttu-id="5dd77-113">沿著旋轉軸向原點方向看時，角度是順時針方向測量。</span><span class="sxs-lookup"><span data-stu-id="5dd77-113">Angles are measured clockwise when looking along the rotation axis toward the origin.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="5dd77-114">傳回值</span><span class="sxs-lookup"><span data-stu-id="5dd77-114">Return value</span></span>

<span data-ttu-id="5dd77-115">類型： **[ **D3DXMATRIX**](../direct3d9/d3dxmatrix.md)\***</span><span class="sxs-lookup"><span data-stu-id="5dd77-115">Type: **[**D3DXMATRIX**](../direct3d9/d3dxmatrix.md)\***</span></span>

<span data-ttu-id="5dd77-116">圍繞 X 軸旋轉之 D3DXMATRIX 結構的指標。</span><span class="sxs-lookup"><span data-stu-id="5dd77-116">Pointer to a D3DXMATRIX structure rotated around the x-axis.</span></span>

## <a name="remarks"></a><span data-ttu-id="5dd77-117">備註</span><span class="sxs-lookup"><span data-stu-id="5dd77-117">Remarks</span></span>

<span data-ttu-id="5dd77-118">此函式的傳回值與不悅參數中所傳回的值相同。</span><span class="sxs-lookup"><span data-stu-id="5dd77-118">The return value for this function is the same value returned in the pOut parameter.</span></span> <span data-ttu-id="5dd77-119">如此一來，D3DXMatrixRotationX 函式就可以用來做為另一個函式的參數。</span><span class="sxs-lookup"><span data-stu-id="5dd77-119">In this way, the D3DXMatrixRotationX function can be used as a parameter for another function.</span></span>

## <a name="requirements"></a><span data-ttu-id="5dd77-120">規格需求</span><span class="sxs-lookup"><span data-stu-id="5dd77-120">Requirements</span></span>



| <span data-ttu-id="5dd77-121">需求</span><span class="sxs-lookup"><span data-stu-id="5dd77-121">Requirement</span></span> | <span data-ttu-id="5dd77-122">值</span><span class="sxs-lookup"><span data-stu-id="5dd77-122">Value</span></span> |
|--------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="5dd77-123">標頭</span><span class="sxs-lookup"><span data-stu-id="5dd77-123">Header</span></span><br/>  | <dl> <span data-ttu-id="5dd77-124"><dt>D3DX10Math。h</dt></span><span class="sxs-lookup"><span data-stu-id="5dd77-124"><dt>D3DX10Math.h</dt></span></span> </dl> |
| <span data-ttu-id="5dd77-125">程式庫</span><span class="sxs-lookup"><span data-stu-id="5dd77-125">Library</span></span><br/> | <dl> <span data-ttu-id="5dd77-126"><dt>D3DX10 .lib</dt></span><span class="sxs-lookup"><span data-stu-id="5dd77-126"><dt>D3DX10.lib</dt></span></span> </dl>   |



## <a name="see-also"></a><span data-ttu-id="5dd77-127">另請參閱</span><span class="sxs-lookup"><span data-stu-id="5dd77-127">See also</span></span>

<dl> <dt>

[<span data-ttu-id="5dd77-128">數學函數</span><span class="sxs-lookup"><span data-stu-id="5dd77-128">Math Functions</span></span>](d3d10-graphics-reference-d3dx10-functions-math.md)
</dt> </dl>

 

 
