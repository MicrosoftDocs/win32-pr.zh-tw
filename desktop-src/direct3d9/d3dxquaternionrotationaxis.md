---
description: 旋轉有關任意軸的四元數。
ms.assetid: 9ff0fe2c-54d6-482c-84e1-f38e3c57d8dd
title: 'D3DXQuaternionRotationAxis 函式 (D3dx9math) '
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
- d3dx9.lib
- d3dx9.dll
ms.openlocfilehash: 7974a1199c468ac762042ae41af59f5a3b66bafd
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 03/15/2021
ms.locfileid: "106997382"
---
# <a name="d3dxquaternionrotationaxis-function-d3dx9mathh"></a><span data-ttu-id="2d36d-103">D3DXQuaternionRotationAxis 函式 (D3dx9math) </span><span class="sxs-lookup"><span data-stu-id="2d36d-103">D3DXQuaternionRotationAxis function (D3dx9math.h)</span></span>

<span data-ttu-id="2d36d-104">旋轉有關任意軸的四元數。</span><span class="sxs-lookup"><span data-stu-id="2d36d-104">Rotates a quaternion about an arbitrary axis.</span></span>

## <a name="syntax"></a><span data-ttu-id="2d36d-105">語法</span><span class="sxs-lookup"><span data-stu-id="2d36d-105">Syntax</span></span>


```C++
D3DXQUATERNION* D3DXQuaternionRotationAxis(
  _Inout_       D3DXQUATERNION *pOut,
  _In_    const D3DXVECTOR3    *pV,
  _In_          FLOAT          Angle
);
```



## <a name="parameters"></a><span data-ttu-id="2d36d-106">參數</span><span class="sxs-lookup"><span data-stu-id="2d36d-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="2d36d-107">*不悅* \[in、out\]</span><span class="sxs-lookup"><span data-stu-id="2d36d-107">*pOut* \[in, out\]</span></span>
</dt> <dd>

<span data-ttu-id="2d36d-108">類型： **[ **D3DXQUATERNION**](d3dxquaternion.md)\***</span><span class="sxs-lookup"><span data-stu-id="2d36d-108">Type: **[**D3DXQUATERNION**](d3dxquaternion.md)\***</span></span>

<span data-ttu-id="2d36d-109">[**D3DXQUATERNION**](d3dxquaternion.md)結構的指標，此結構是作業的結果。</span><span class="sxs-lookup"><span data-stu-id="2d36d-109">Pointer to the [**D3DXQUATERNION**](d3dxquaternion.md) structure that is the result of the operation.</span></span>

</dd> <dt>

<span data-ttu-id="2d36d-110">*pV* \[在\]</span><span class="sxs-lookup"><span data-stu-id="2d36d-110">*pV* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="2d36d-111">Type： **Const [**D3DXVECTOR3**](d3dxvector3.md) \***</span><span class="sxs-lookup"><span data-stu-id="2d36d-111">Type: **const [**D3DXVECTOR3**](d3dxvector3.md)\***</span></span>

<span data-ttu-id="2d36d-112">[**D3DXVECTOR3**](d3dxvector3.md)結構的指標，此結構會識別要用來旋轉四元數的軸。</span><span class="sxs-lookup"><span data-stu-id="2d36d-112">Pointer to the [**D3DXVECTOR3**](d3dxvector3.md) structure that identifies the axis about which to rotate the quaternion.</span></span>

</dd> <dt>

<span data-ttu-id="2d36d-113">*角度* \[在\]</span><span class="sxs-lookup"><span data-stu-id="2d36d-113">*Angle* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="2d36d-114">類型： **[ **FLOAT**](../winprog/windows-data-types.md)**</span><span class="sxs-lookup"><span data-stu-id="2d36d-114">Type: **[**FLOAT**](../winprog/windows-data-types.md)**</span></span>

<span data-ttu-id="2d36d-115">旋轉的角度，以弧度為單位。</span><span class="sxs-lookup"><span data-stu-id="2d36d-115">Angle of rotation, in radians.</span></span> <span data-ttu-id="2d36d-116">沿著旋轉軸向原點方向看時，角度是順時針方向測量。</span><span class="sxs-lookup"><span data-stu-id="2d36d-116">Angles are measured clockwise when looking along the rotation axis toward the origin.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="2d36d-117">傳回值</span><span class="sxs-lookup"><span data-stu-id="2d36d-117">Return value</span></span>

<span data-ttu-id="2d36d-118">類型： **[ **D3DXQUATERNION**](d3dxquaternion.md)\***</span><span class="sxs-lookup"><span data-stu-id="2d36d-118">Type: **[**D3DXQUATERNION**](d3dxquaternion.md)\***</span></span>

<span data-ttu-id="2d36d-119">圍繞指定軸旋轉之 [**D3DXQUATERNION**](d3dxquaternion.md) 結構的指標。</span><span class="sxs-lookup"><span data-stu-id="2d36d-119">Pointer to a [**D3DXQUATERNION**](d3dxquaternion.md) structure rotated around the specified axis.</span></span>

## <a name="remarks"></a><span data-ttu-id="2d36d-120">備註</span><span class="sxs-lookup"><span data-stu-id="2d36d-120">Remarks</span></span>

<span data-ttu-id="2d36d-121">此函式的傳回值與 *不悅* 參數中所傳回的值相同。</span><span class="sxs-lookup"><span data-stu-id="2d36d-121">The return value for this function is the same value returned in the *pOut* parameter.</span></span> <span data-ttu-id="2d36d-122">如此一來， **D3DXQuaternionRotationAxis** 函式就可以用來做為另一個函式的參數。</span><span class="sxs-lookup"><span data-stu-id="2d36d-122">In this way, the **D3DXQuaternionRotationAxis** function can be used as a parameter for another function.</span></span>

<span data-ttu-id="2d36d-123">針對尚未正規化的任何四元數輸入，請使用 [**D3DXQuaternionNormalize**](d3dxquaternionnormalize.md) 。</span><span class="sxs-lookup"><span data-stu-id="2d36d-123">Use [**D3DXQuaternionNormalize**](d3dxquaternionnormalize.md) for any quaternion input that is not already normalized.</span></span>

## <a name="requirements"></a><span data-ttu-id="2d36d-124">規格需求</span><span class="sxs-lookup"><span data-stu-id="2d36d-124">Requirements</span></span>



| <span data-ttu-id="2d36d-125">需求</span><span class="sxs-lookup"><span data-stu-id="2d36d-125">Requirement</span></span> | <span data-ttu-id="2d36d-126">值</span><span class="sxs-lookup"><span data-stu-id="2d36d-126">Value</span></span> |
|--------------------|----------------------------------------------------------------------------------------|
| <span data-ttu-id="2d36d-127">標頭</span><span class="sxs-lookup"><span data-stu-id="2d36d-127">Header</span></span><br/>  | <dl> <span data-ttu-id="2d36d-128"><dt>D3dx9math。h</dt></span><span class="sxs-lookup"><span data-stu-id="2d36d-128"><dt>D3dx9math.h</dt></span></span> </dl> |
| <span data-ttu-id="2d36d-129">程式庫</span><span class="sxs-lookup"><span data-stu-id="2d36d-129">Library</span></span><br/> | <dl> <span data-ttu-id="2d36d-130"><dt>D3dx9 .lib</dt></span><span class="sxs-lookup"><span data-stu-id="2d36d-130"><dt>D3dx9.lib</dt></span></span> </dl>   |



## <a name="see-also"></a><span data-ttu-id="2d36d-131">另請參閱</span><span class="sxs-lookup"><span data-stu-id="2d36d-131">See also</span></span>

<dl> <dt>

[<span data-ttu-id="2d36d-132">數學函數</span><span class="sxs-lookup"><span data-stu-id="2d36d-132">Math Functions</span></span>](dx9-graphics-reference-d3dx-functions-math.md)
</dt> <dt>

[<span data-ttu-id="2d36d-133">**D3DXQuaternionRotationMatrix**</span><span class="sxs-lookup"><span data-stu-id="2d36d-133">**D3DXQuaternionRotationMatrix**</span></span>](d3dxquaternionrotationmatrix.md)
</dt> <dt>

[<span data-ttu-id="2d36d-134">**D3DXQuaternionRotationYawPitchRoll**</span><span class="sxs-lookup"><span data-stu-id="2d36d-134">**D3DXQuaternionRotationYawPitchRoll**</span></span>](d3dxquaternionrotationyawpitchroll.md)
</dt> </dl>

 

 
