---
description: 建立圍繞 Z 軸旋轉的矩陣。
ms.assetid: 73db43e6-3831-4867-8eda-80127b61e169
title: 'D3DXMatrixRotationZ 函式 (D3dx9math) '
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
- d3dx9.lib
- d3dx9.dll
ms.openlocfilehash: 61d94df676016c0e22e7c0842eebe9af05b9ff71
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 03/15/2021
ms.locfileid: "106991485"
---
# <a name="d3dxmatrixrotationz-function-d3dx9mathh"></a><span data-ttu-id="a1ab6-103">D3DXMatrixRotationZ 函式 (D3dx9math) </span><span class="sxs-lookup"><span data-stu-id="a1ab6-103">D3DXMatrixRotationZ function (D3dx9math.h)</span></span>

<span data-ttu-id="a1ab6-104">建立圍繞 Z 軸旋轉的矩陣。</span><span class="sxs-lookup"><span data-stu-id="a1ab6-104">Builds a matrix that rotates around the z-axis.</span></span>

## <a name="syntax"></a><span data-ttu-id="a1ab6-105">語法</span><span class="sxs-lookup"><span data-stu-id="a1ab6-105">Syntax</span></span>


```C++
D3DXMATRIX* D3DXMatrixRotationZ(
  _Inout_ D3DXMATRIX *pOut,
  _In_    FLOAT      Angle
);
```



## <a name="parameters"></a><span data-ttu-id="a1ab6-106">參數</span><span class="sxs-lookup"><span data-stu-id="a1ab6-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="a1ab6-107">*不悅* \[in、out\]</span><span class="sxs-lookup"><span data-stu-id="a1ab6-107">*pOut* \[in, out\]</span></span>
</dt> <dd>

<span data-ttu-id="a1ab6-108">類型： **[ **D3DXMATRIX**](d3dxmatrix.md)\***</span><span class="sxs-lookup"><span data-stu-id="a1ab6-108">Type: **[**D3DXMATRIX**](d3dxmatrix.md)\***</span></span>

<span data-ttu-id="a1ab6-109">[**D3DXMATRIX**](d3dxmatrix.md)結構的指標，此結構是作業的結果。</span><span class="sxs-lookup"><span data-stu-id="a1ab6-109">Pointer to the [**D3DXMATRIX**](d3dxmatrix.md) structure that is the result of the operation.</span></span>

</dd> <dt>

<span data-ttu-id="a1ab6-110">*角度* \[在\]</span><span class="sxs-lookup"><span data-stu-id="a1ab6-110">*Angle* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="a1ab6-111">類型： **[ **FLOAT**](../winprog/windows-data-types.md)**</span><span class="sxs-lookup"><span data-stu-id="a1ab6-111">Type: **[**FLOAT**](../winprog/windows-data-types.md)**</span></span>

<span data-ttu-id="a1ab6-112">旋轉的角度，以弧度為單位。</span><span class="sxs-lookup"><span data-stu-id="a1ab6-112">Angle of rotation, in radians.</span></span> <span data-ttu-id="a1ab6-113">從旋轉軸觀看旋轉軸 (正面) 朝原點時，會順時針測量角度。</span><span class="sxs-lookup"><span data-stu-id="a1ab6-113">Angles are measured clockwise when viewed from the rotation axis (positive side) toward the origin.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="a1ab6-114">傳回值</span><span class="sxs-lookup"><span data-stu-id="a1ab6-114">Return value</span></span>

<span data-ttu-id="a1ab6-115">類型： **[ **D3DXMATRIX**](d3dxmatrix.md)\***</span><span class="sxs-lookup"><span data-stu-id="a1ab6-115">Type: **[**D3DXMATRIX**](d3dxmatrix.md)\***</span></span>

<span data-ttu-id="a1ab6-116">圍繞 Z 軸旋轉之 [**D3DXMATRIX**](d3dxmatrix.md) 結構的指標。</span><span class="sxs-lookup"><span data-stu-id="a1ab6-116">Pointer to a [**D3DXMATRIX**](d3dxmatrix.md) structure rotated around the z-axis.</span></span>

## <a name="remarks"></a><span data-ttu-id="a1ab6-117">備註</span><span class="sxs-lookup"><span data-stu-id="a1ab6-117">Remarks</span></span>

<span data-ttu-id="a1ab6-118">此函式的傳回值與 *不悅* 參數中所傳回的值相同。</span><span class="sxs-lookup"><span data-stu-id="a1ab6-118">The return value for this function is the same value returned in the *pOut* parameter.</span></span> <span data-ttu-id="a1ab6-119">如此一來， **D3DXMatrixRotationZ** 函式就可以用來做為另一個函式的參數。</span><span class="sxs-lookup"><span data-stu-id="a1ab6-119">In this way, the **D3DXMatrixRotationZ** function can be used as a parameter for another function.</span></span>

## <a name="requirements"></a><span data-ttu-id="a1ab6-120">規格需求</span><span class="sxs-lookup"><span data-stu-id="a1ab6-120">Requirements</span></span>



| <span data-ttu-id="a1ab6-121">需求</span><span class="sxs-lookup"><span data-stu-id="a1ab6-121">Requirement</span></span> | <span data-ttu-id="a1ab6-122">值</span><span class="sxs-lookup"><span data-stu-id="a1ab6-122">Value</span></span> |
|--------------------|----------------------------------------------------------------------------------------|
| <span data-ttu-id="a1ab6-123">標頭</span><span class="sxs-lookup"><span data-stu-id="a1ab6-123">Header</span></span><br/>  | <dl> <span data-ttu-id="a1ab6-124"><dt>D3dx9math。h</dt></span><span class="sxs-lookup"><span data-stu-id="a1ab6-124"><dt>D3dx9math.h</dt></span></span> </dl> |
| <span data-ttu-id="a1ab6-125">程式庫</span><span class="sxs-lookup"><span data-stu-id="a1ab6-125">Library</span></span><br/> | <dl> <span data-ttu-id="a1ab6-126"><dt>D3dx9 .lib</dt></span><span class="sxs-lookup"><span data-stu-id="a1ab6-126"><dt>D3dx9.lib</dt></span></span> </dl>   |



## <a name="see-also"></a><span data-ttu-id="a1ab6-127">另請參閱</span><span class="sxs-lookup"><span data-stu-id="a1ab6-127">See also</span></span>

<dl> <dt>

[<span data-ttu-id="a1ab6-128">數學函數</span><span class="sxs-lookup"><span data-stu-id="a1ab6-128">Math Functions</span></span>](dx9-graphics-reference-d3dx-functions-math.md)
</dt> <dt>

[<span data-ttu-id="a1ab6-129">**D3DXMatrixRotationAxis**</span><span class="sxs-lookup"><span data-stu-id="a1ab6-129">**D3DXMatrixRotationAxis**</span></span>](d3dxmatrixrotationaxis.md)
</dt> <dt>

[<span data-ttu-id="a1ab6-130">**D3DXMatrixRotationQuaternion**</span><span class="sxs-lookup"><span data-stu-id="a1ab6-130">**D3DXMatrixRotationQuaternion**</span></span>](d3dxmatrixrotationquaternion.md)
</dt> <dt>

[<span data-ttu-id="a1ab6-131">**D3DXMatrixRotationX**</span><span class="sxs-lookup"><span data-stu-id="a1ab6-131">**D3DXMatrixRotationX**</span></span>](d3dxmatrixrotationx.md)
</dt> <dt>

[<span data-ttu-id="a1ab6-132">**D3DXMatrixRotationY**</span><span class="sxs-lookup"><span data-stu-id="a1ab6-132">**D3DXMatrixRotationY**</span></span>](d3dxmatrixrotationy.md)
</dt> <dt>

[<span data-ttu-id="a1ab6-133">**D3DXMatrixRotationYawPitchRoll**</span><span class="sxs-lookup"><span data-stu-id="a1ab6-133">**D3DXMatrixRotationYawPitchRoll**</span></span>](d3dxmatrixrotationyawpitchroll.md)
</dt> </dl>

 

 
