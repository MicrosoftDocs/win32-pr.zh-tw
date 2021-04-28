---
description: D3DXMatrixRotationZ 函式 (D3DX10Math) -建立圍繞 Z 軸旋轉的矩陣。
ms.assetid: a168ea24-0cec-4e1b-a128-e9dadedf190b
title: 'D3DXMatrixRotationZ 函式 (D3DX10Math) '
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- D3DXMatrixRotationZ
api_type:
- LibDef
api_location:
- D3DX10.lib
- D3DX10.dll
ms.openlocfilehash: b952e310dd463d07a35fb294c4a50168361658a7
ms.sourcegitcommit: 95685061d5b0333bbf9e6ebd208dde8190f97005
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 04/28/2021
ms.locfileid: "108108936"
---
# <a name="d3dxmatrixrotationz-function-d3dx10mathh"></a><span data-ttu-id="24f9f-103">D3DXMatrixRotationZ 函式 (D3DX10Math) </span><span class="sxs-lookup"><span data-stu-id="24f9f-103">D3DXMatrixRotationZ function (D3DX10Math.h)</span></span>

<span data-ttu-id="24f9f-104">建立圍繞 Z 軸旋轉的矩陣。</span><span class="sxs-lookup"><span data-stu-id="24f9f-104">Builds a matrix that rotates around the z-axis.</span></span>

## <a name="syntax"></a><span data-ttu-id="24f9f-105">語法</span><span class="sxs-lookup"><span data-stu-id="24f9f-105">Syntax</span></span>


```C++
D3DXMATRIX* D3DXMatrixRotationZ(
  _Inout_ D3DXMATRIX *pOut,
  _In_    FLOAT      Angle
);
```



## <a name="parameters"></a><span data-ttu-id="24f9f-106">參數</span><span class="sxs-lookup"><span data-stu-id="24f9f-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="24f9f-107">*不悅* \[in、out\]</span><span class="sxs-lookup"><span data-stu-id="24f9f-107">*pOut* \[in, out\]</span></span>
</dt> <dd>

<span data-ttu-id="24f9f-108">類型： **[ **D3DXMATRIX**](../direct3d9/d3dxmatrix.md)\***</span><span class="sxs-lookup"><span data-stu-id="24f9f-108">Type: **[**D3DXMATRIX**](../direct3d9/d3dxmatrix.md)\***</span></span>

<span data-ttu-id="24f9f-109">[**D3DXMATRIX**](d3d10-d3dxmatrix.md)結構的指標，此結構是作業的結果。</span><span class="sxs-lookup"><span data-stu-id="24f9f-109">Pointer to the [**D3DXMATRIX**](d3d10-d3dxmatrix.md) structure that is the result of the operation.</span></span>

</dd> <dt>

<span data-ttu-id="24f9f-110">*角度* \[在\]</span><span class="sxs-lookup"><span data-stu-id="24f9f-110">*Angle* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="24f9f-111">類型： **[ **FLOAT**](../winprog/windows-data-types.md)**</span><span class="sxs-lookup"><span data-stu-id="24f9f-111">Type: **[**FLOAT**](../winprog/windows-data-types.md)**</span></span>

<span data-ttu-id="24f9f-112">旋轉的角度，以弧度為單位。</span><span class="sxs-lookup"><span data-stu-id="24f9f-112">Angle of rotation, in radians.</span></span> <span data-ttu-id="24f9f-113">從旋轉軸觀看旋轉軸 (正面) 朝原點時，會順時針測量角度。</span><span class="sxs-lookup"><span data-stu-id="24f9f-113">Angles are measured clockwise when viewed from the rotation axis (positive side) toward the origin.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="24f9f-114">傳回值</span><span class="sxs-lookup"><span data-stu-id="24f9f-114">Return value</span></span>

<span data-ttu-id="24f9f-115">類型： **[ **D3DXMATRIX**](../direct3d9/d3dxmatrix.md)\***</span><span class="sxs-lookup"><span data-stu-id="24f9f-115">Type: **[**D3DXMATRIX**](../direct3d9/d3dxmatrix.md)\***</span></span>

<span data-ttu-id="24f9f-116">圍繞 Z 軸旋轉之 D3DXMATRIX 結構的指標。</span><span class="sxs-lookup"><span data-stu-id="24f9f-116">Pointer to a D3DXMATRIX structure rotated around the z-axis.</span></span>

## <a name="remarks"></a><span data-ttu-id="24f9f-117">備註</span><span class="sxs-lookup"><span data-stu-id="24f9f-117">Remarks</span></span>

<span data-ttu-id="24f9f-118">此函式的傳回值與不悅參數中所傳回的值相同。</span><span class="sxs-lookup"><span data-stu-id="24f9f-118">The return value for this function is the same value returned in the pOut parameter.</span></span> <span data-ttu-id="24f9f-119">如此一來，D3DXMatrixRotationZ 函式就可以用來做為另一個函式的參數。</span><span class="sxs-lookup"><span data-stu-id="24f9f-119">In this way, the D3DXMatrixRotationZ function can be used as a parameter for another function.</span></span>

## <a name="requirements"></a><span data-ttu-id="24f9f-120">規格需求</span><span class="sxs-lookup"><span data-stu-id="24f9f-120">Requirements</span></span>



| <span data-ttu-id="24f9f-121">需求</span><span class="sxs-lookup"><span data-stu-id="24f9f-121">Requirement</span></span> | <span data-ttu-id="24f9f-122">值</span><span class="sxs-lookup"><span data-stu-id="24f9f-122">Value</span></span> |
|--------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="24f9f-123">標頭</span><span class="sxs-lookup"><span data-stu-id="24f9f-123">Header</span></span><br/>  | <dl> <span data-ttu-id="24f9f-124"><dt>D3DX10Math。h</dt></span><span class="sxs-lookup"><span data-stu-id="24f9f-124"><dt>D3DX10Math.h</dt></span></span> </dl> |
| <span data-ttu-id="24f9f-125">程式庫</span><span class="sxs-lookup"><span data-stu-id="24f9f-125">Library</span></span><br/> | <dl> <span data-ttu-id="24f9f-126"><dt>D3DX10 .lib</dt></span><span class="sxs-lookup"><span data-stu-id="24f9f-126"><dt>D3DX10.lib</dt></span></span> </dl>   |



## <a name="see-also"></a><span data-ttu-id="24f9f-127">另請參閱</span><span class="sxs-lookup"><span data-stu-id="24f9f-127">See also</span></span>

<dl> <dt>

[<span data-ttu-id="24f9f-128">數學函數</span><span class="sxs-lookup"><span data-stu-id="24f9f-128">Math Functions</span></span>](d3d10-graphics-reference-d3dx10-functions-math.md)
</dt> </dl>

 

 
