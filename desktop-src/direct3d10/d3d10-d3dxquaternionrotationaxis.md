---
description: D3DXQuaternionRotationAxis 函式 (D3DX10Math) -圍繞任意軸旋轉四元數。
ms.assetid: 9673ef89-458f-4a25-960e-8f03179e78ba
title: 'D3DXQuaternionRotationAxis 函式 (D3DX10Math) '
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- D3DXQuaternionRotationAxis
api_type:
- LibDef
api_location:
- D3DX10.lib
- D3DX10.dll
ms.openlocfilehash: 509df80023427a20125e1b5603e85424851a640e
ms.sourcegitcommit: 95685061d5b0333bbf9e6ebd208dde8190f97005
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 04/28/2021
ms.locfileid: "108108766"
---
# <a name="d3dxquaternionrotationaxis-function-d3dx10mathh"></a><span data-ttu-id="e26d3-103">D3DXQuaternionRotationAxis 函式 (D3DX10Math) </span><span class="sxs-lookup"><span data-stu-id="e26d3-103">D3DXQuaternionRotationAxis function (D3DX10Math.h)</span></span>

<span data-ttu-id="e26d3-104">旋轉有關任意軸的四元數。</span><span class="sxs-lookup"><span data-stu-id="e26d3-104">Rotates a quaternion about an arbitrary axis.</span></span>

## <a name="syntax"></a><span data-ttu-id="e26d3-105">語法</span><span class="sxs-lookup"><span data-stu-id="e26d3-105">Syntax</span></span>


```C++
D3DXQUATERNION* D3DXQuaternionRotationAxis(
  _Inout_       D3DXQUATERNION *pOut,
  _In_    const D3DXVECTOR3    *pV,
  _In_          FLOAT          Angle
);
```



## <a name="parameters"></a><span data-ttu-id="e26d3-106">參數</span><span class="sxs-lookup"><span data-stu-id="e26d3-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="e26d3-107">*不悅* \[in、out\]</span><span class="sxs-lookup"><span data-stu-id="e26d3-107">*pOut* \[in, out\]</span></span>
</dt> <dd>

<span data-ttu-id="e26d3-108">類型： **[ **D3DXQUATERNION**](../direct3d9/d3dxquaternion.md)\***</span><span class="sxs-lookup"><span data-stu-id="e26d3-108">Type: **[**D3DXQUATERNION**](../direct3d9/d3dxquaternion.md)\***</span></span>

<span data-ttu-id="e26d3-109">作業結果之 [**D3DXQUATERNION**](d3d10-d3dxquaternion.md) 的指標。</span><span class="sxs-lookup"><span data-stu-id="e26d3-109">Pointer to the [**D3DXQUATERNION**](d3d10-d3dxquaternion.md) that is the result of the operation.</span></span>

</dd> <dt>

<span data-ttu-id="e26d3-110">*pV* \[在\]</span><span class="sxs-lookup"><span data-stu-id="e26d3-110">*pV* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="e26d3-111">Type： **Const [**D3DXVECTOR3**](../direct3d9/d3dxvector3.md) \***</span><span class="sxs-lookup"><span data-stu-id="e26d3-111">Type: **const [**D3DXVECTOR3**](../direct3d9/d3dxvector3.md)\***</span></span>

<span data-ttu-id="e26d3-112">識別要用來旋轉四元數之軸的 [**D3DXVECTOR3**](d3d10-d3dxvector3.md) 指標。</span><span class="sxs-lookup"><span data-stu-id="e26d3-112">Pointer to the [**D3DXVECTOR3**](d3d10-d3dxvector3.md) that identifies the axis about which to rotate the quaternion.</span></span>

</dd> <dt>

<span data-ttu-id="e26d3-113">*角度* \[在\]</span><span class="sxs-lookup"><span data-stu-id="e26d3-113">*Angle* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="e26d3-114">類型： **[ **FLOAT**](../winprog/windows-data-types.md)**</span><span class="sxs-lookup"><span data-stu-id="e26d3-114">Type: **[**FLOAT**](../winprog/windows-data-types.md)**</span></span>

<span data-ttu-id="e26d3-115">旋轉的角度，以弧度為單位。</span><span class="sxs-lookup"><span data-stu-id="e26d3-115">Angle of rotation, in radians.</span></span> <span data-ttu-id="e26d3-116">沿著旋轉軸向原點方向看時，角度是順時針方向測量。</span><span class="sxs-lookup"><span data-stu-id="e26d3-116">Angles are measured clockwise when looking along the rotation axis toward the origin.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="e26d3-117">傳回值</span><span class="sxs-lookup"><span data-stu-id="e26d3-117">Return value</span></span>

<span data-ttu-id="e26d3-118">類型： **[ **D3DXQUATERNION**](../direct3d9/d3dxquaternion.md)\***</span><span class="sxs-lookup"><span data-stu-id="e26d3-118">Type: **[**D3DXQUATERNION**](../direct3d9/d3dxquaternion.md)\***</span></span>

<span data-ttu-id="e26d3-119">圍繞指定軸旋轉之 D3DXQUATERNION 結構的指標。</span><span class="sxs-lookup"><span data-stu-id="e26d3-119">Pointer to a D3DXQUATERNION structure rotated around the specified axis.</span></span>

## <a name="remarks"></a><span data-ttu-id="e26d3-120">備註</span><span class="sxs-lookup"><span data-stu-id="e26d3-120">Remarks</span></span>

<span data-ttu-id="e26d3-121">此函式的傳回值與不悅參數中所傳回的值相同。</span><span class="sxs-lookup"><span data-stu-id="e26d3-121">The return value for this function is the same value returned in the pOut parameter.</span></span> <span data-ttu-id="e26d3-122">如此一來，D3DXQuaternionRotationAxis 函式就可以用來做為另一個函式的參數。</span><span class="sxs-lookup"><span data-stu-id="e26d3-122">In this way, the D3DXQuaternionRotationAxis function can be used as a parameter for another function.</span></span>

<span data-ttu-id="e26d3-123">針對尚未正規化的任何四元數輸入，請使用 [**D3DXQuaternionNormalize**](d3d10-d3dxquaternionnormalize.md) 。</span><span class="sxs-lookup"><span data-stu-id="e26d3-123">Use [**D3DXQuaternionNormalize**](d3d10-d3dxquaternionnormalize.md) for any quaternion input that is not already normalized.</span></span>

## <a name="requirements"></a><span data-ttu-id="e26d3-124">規格需求</span><span class="sxs-lookup"><span data-stu-id="e26d3-124">Requirements</span></span>



| <span data-ttu-id="e26d3-125">需求</span><span class="sxs-lookup"><span data-stu-id="e26d3-125">Requirement</span></span> | <span data-ttu-id="e26d3-126">值</span><span class="sxs-lookup"><span data-stu-id="e26d3-126">Value</span></span> |
|--------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="e26d3-127">標頭</span><span class="sxs-lookup"><span data-stu-id="e26d3-127">Header</span></span><br/>  | <dl> <span data-ttu-id="e26d3-128"><dt>D3DX10Math。h</dt></span><span class="sxs-lookup"><span data-stu-id="e26d3-128"><dt>D3DX10Math.h</dt></span></span> </dl> |
| <span data-ttu-id="e26d3-129">程式庫</span><span class="sxs-lookup"><span data-stu-id="e26d3-129">Library</span></span><br/> | <dl> <span data-ttu-id="e26d3-130"><dt>D3DX10 .lib</dt></span><span class="sxs-lookup"><span data-stu-id="e26d3-130"><dt>D3DX10.lib</dt></span></span> </dl>   |



## <a name="see-also"></a><span data-ttu-id="e26d3-131">另請參閱</span><span class="sxs-lookup"><span data-stu-id="e26d3-131">See also</span></span>

<dl> <dt>

[<span data-ttu-id="e26d3-132">數學函數</span><span class="sxs-lookup"><span data-stu-id="e26d3-132">Math Functions</span></span>](d3d10-graphics-reference-d3dx10-functions-math.md)
</dt> </dl>

 

 
