---
description: D3DXMatrixRotationQuaternion function (D3dx9math) -從四元數建立旋轉矩陣。
ms.assetid: e590058c-772b-4eef-aab0-a12bb04c299a
title: 'D3DXMatrixRotationQuaternion 函式 (D3dx9math) '
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- D3DXMatrixRotationQuaternion
api_type:
- LibDef
api_location:
- d3dx9.lib
- d3dx9.dll
ms.openlocfilehash: 4b30de0c45c8d78b2e07d6ff57a4e94b9753298a
ms.sourcegitcommit: 95685061d5b0333bbf9e6ebd208dde8190f97005
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 04/28/2021
ms.locfileid: "108118196"
---
# <a name="d3dxmatrixrotationquaternion-function-d3dx9mathh"></a><span data-ttu-id="19aa6-103">D3DXMatrixRotationQuaternion 函式 (D3dx9math) </span><span class="sxs-lookup"><span data-stu-id="19aa6-103">D3DXMatrixRotationQuaternion function (D3dx9math.h)</span></span>

<span data-ttu-id="19aa6-104">從四元數建立旋轉矩陣。</span><span class="sxs-lookup"><span data-stu-id="19aa6-104">Builds a rotation matrix from a quaternion.</span></span>

## <a name="syntax"></a><span data-ttu-id="19aa6-105">語法</span><span class="sxs-lookup"><span data-stu-id="19aa6-105">Syntax</span></span>


```C++
D3DXMATRIX* D3DXMatrixRotationQuaternion(
  _Inout_       D3DXMATRIX     *pOut,
  _In_    const D3DXQUATERNION *pQ
);
```



## <a name="parameters"></a><span data-ttu-id="19aa6-106">參數</span><span class="sxs-lookup"><span data-stu-id="19aa6-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="19aa6-107">*不悅* \[in、out\]</span><span class="sxs-lookup"><span data-stu-id="19aa6-107">*pOut* \[in, out\]</span></span>
</dt> <dd>

<span data-ttu-id="19aa6-108">類型： **[ **D3DXMATRIX**](d3dxmatrix.md)\***</span><span class="sxs-lookup"><span data-stu-id="19aa6-108">Type: **[**D3DXMATRIX**](d3dxmatrix.md)\***</span></span>

<span data-ttu-id="19aa6-109">[**D3DXMATRIX**](d3dxmatrix.md)結構的指標，此結構是作業的結果。</span><span class="sxs-lookup"><span data-stu-id="19aa6-109">Pointer to the [**D3DXMATRIX**](d3dxmatrix.md) structure that is the result of the operation.</span></span>

</dd> <dt>

<span data-ttu-id="19aa6-110">*pQ* \[在\]</span><span class="sxs-lookup"><span data-stu-id="19aa6-110">*pQ* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="19aa6-111">Type： **Const [**D3DXQUATERNION**](d3dxquaternion.md) \***</span><span class="sxs-lookup"><span data-stu-id="19aa6-111">Type: **const [**D3DXQUATERNION**](d3dxquaternion.md)\***</span></span>

<span data-ttu-id="19aa6-112">來源 [**D3DXQUATERNION**](d3dxquaternion.md) 結構的指標。</span><span class="sxs-lookup"><span data-stu-id="19aa6-112">Pointer to the source [**D3DXQUATERNION**](d3dxquaternion.md) structure.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="19aa6-113">傳回值</span><span class="sxs-lookup"><span data-stu-id="19aa6-113">Return value</span></span>

<span data-ttu-id="19aa6-114">類型： **[ **D3DXMATRIX**](d3dxmatrix.md)\***</span><span class="sxs-lookup"><span data-stu-id="19aa6-114">Type: **[**D3DXMATRIX**](d3dxmatrix.md)\***</span></span>

<span data-ttu-id="19aa6-115">從來源四元數建立之 [**D3DXMATRIX**](d3dxmatrix.md) 結構的指標。</span><span class="sxs-lookup"><span data-stu-id="19aa6-115">Pointer to a [**D3DXMATRIX**](d3dxmatrix.md) structure built from the source quaternion.</span></span>

## <a name="remarks"></a><span data-ttu-id="19aa6-116">備註</span><span class="sxs-lookup"><span data-stu-id="19aa6-116">Remarks</span></span>

<span data-ttu-id="19aa6-117">此函式的傳回值與 *不悅* 參數中所傳回的值相同。</span><span class="sxs-lookup"><span data-stu-id="19aa6-117">The return value for this function is the same value returned in the *pOut* parameter.</span></span> <span data-ttu-id="19aa6-118">如此一來， **D3DXMatrixRotationQuaternion** 函式就可以用來做為另一個函式的參數。</span><span class="sxs-lookup"><span data-stu-id="19aa6-118">In this way, the **D3DXMatrixRotationQuaternion** function can be used as a parameter for another function.</span></span>

<span data-ttu-id="19aa6-119">如需如何從方向向量計算四元數值 ( x、y、z ) 和旋轉角度的詳細資訊，請參閱 [**D3DXQUATERNION**](d3dxquaternion.md)。</span><span class="sxs-lookup"><span data-stu-id="19aa6-119">For information about how to calculate quaternion values from a direction vector ( x, y, z ) and an angle of rotation, see [**D3DXQUATERNION**](d3dxquaternion.md).</span></span>

## <a name="requirements"></a><span data-ttu-id="19aa6-120">規格需求</span><span class="sxs-lookup"><span data-stu-id="19aa6-120">Requirements</span></span>



| <span data-ttu-id="19aa6-121">需求</span><span class="sxs-lookup"><span data-stu-id="19aa6-121">Requirement</span></span> | <span data-ttu-id="19aa6-122">值</span><span class="sxs-lookup"><span data-stu-id="19aa6-122">Value</span></span> |
|--------------------|----------------------------------------------------------------------------------------|
| <span data-ttu-id="19aa6-123">標頭</span><span class="sxs-lookup"><span data-stu-id="19aa6-123">Header</span></span><br/>  | <dl> <span data-ttu-id="19aa6-124"><dt>D3dx9math。h</dt></span><span class="sxs-lookup"><span data-stu-id="19aa6-124"><dt>D3dx9math.h</dt></span></span> </dl> |
| <span data-ttu-id="19aa6-125">程式庫</span><span class="sxs-lookup"><span data-stu-id="19aa6-125">Library</span></span><br/> | <dl> <span data-ttu-id="19aa6-126"><dt>D3dx9 .lib</dt></span><span class="sxs-lookup"><span data-stu-id="19aa6-126"><dt>D3dx9.lib</dt></span></span> </dl>   |



## <a name="see-also"></a><span data-ttu-id="19aa6-127">另請參閱</span><span class="sxs-lookup"><span data-stu-id="19aa6-127">See also</span></span>

<dl> <dt>

[<span data-ttu-id="19aa6-128">數學函數</span><span class="sxs-lookup"><span data-stu-id="19aa6-128">Math Functions</span></span>](dx9-graphics-reference-d3dx-functions-math.md)
</dt> <dt>

[<span data-ttu-id="19aa6-129">**D3DXMatrixRotationAxis**</span><span class="sxs-lookup"><span data-stu-id="19aa6-129">**D3DXMatrixRotationAxis**</span></span>](d3dxmatrixrotationaxis.md)
</dt> <dt>

[<span data-ttu-id="19aa6-130">**D3DXMatrixRotationX**</span><span class="sxs-lookup"><span data-stu-id="19aa6-130">**D3DXMatrixRotationX**</span></span>](d3dxmatrixrotationx.md)
</dt> <dt>

[<span data-ttu-id="19aa6-131">**D3DXMatrixRotationY**</span><span class="sxs-lookup"><span data-stu-id="19aa6-131">**D3DXMatrixRotationY**</span></span>](d3dxmatrixrotationy.md)
</dt> <dt>

[<span data-ttu-id="19aa6-132">**D3DXMatrixRotationYawPitchRoll**</span><span class="sxs-lookup"><span data-stu-id="19aa6-132">**D3DXMatrixRotationYawPitchRoll**</span></span>](d3dxmatrixrotationyawpitchroll.md)
</dt> <dt>

[<span data-ttu-id="19aa6-133">**D3DXMatrixRotationZ**</span><span class="sxs-lookup"><span data-stu-id="19aa6-133">**D3DXMatrixRotationZ**</span></span>](d3dxmatrixrotationz.md)
</dt> </dl>

 

 




