---
description: 從四元數建立旋轉矩陣。
ms.assetid: dcbf8696-b959-4475-a250-6094dd5fe358
title: 'D3DXMatrixRotationQuaternion 函式 (D3DX10Math) '
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
- D3DX10.lib
- D3DX10.dll
ms.openlocfilehash: 44cd4a5982b322c2d207263fb490c898ed9fa76e
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 03/15/2021
ms.locfileid: "106992345"
---
# <a name="d3dxmatrixrotationquaternion-function-d3dx10mathh"></a><span data-ttu-id="d8ccd-103">D3DXMatrixRotationQuaternion 函式 (D3DX10Math) </span><span class="sxs-lookup"><span data-stu-id="d8ccd-103">D3DXMatrixRotationQuaternion function (D3DX10Math.h)</span></span>

<span data-ttu-id="d8ccd-104">從四元數建立旋轉矩陣。</span><span class="sxs-lookup"><span data-stu-id="d8ccd-104">Builds a rotation matrix from a quaternion.</span></span>

## <a name="syntax"></a><span data-ttu-id="d8ccd-105">語法</span><span class="sxs-lookup"><span data-stu-id="d8ccd-105">Syntax</span></span>


```C++
D3DXMATRIX* D3DXMatrixRotationQuaternion(
  _Inout_       D3DXMATRIX     *pOut,
  _In_    const D3DXQUATERNION *pQ
);
```



## <a name="parameters"></a><span data-ttu-id="d8ccd-106">參數</span><span class="sxs-lookup"><span data-stu-id="d8ccd-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="d8ccd-107">*不悅* \[in、out\]</span><span class="sxs-lookup"><span data-stu-id="d8ccd-107">*pOut* \[in, out\]</span></span>
</dt> <dd>

<span data-ttu-id="d8ccd-108">類型： **[ **D3DXMATRIX**](../direct3d9/d3dxmatrix.md)\***</span><span class="sxs-lookup"><span data-stu-id="d8ccd-108">Type: **[**D3DXMATRIX**](../direct3d9/d3dxmatrix.md)\***</span></span>

<span data-ttu-id="d8ccd-109">[**D3DXMATRIX**](d3d10-d3dxmatrix.md)結構的指標，此結構是作業的結果。</span><span class="sxs-lookup"><span data-stu-id="d8ccd-109">Pointer to the [**D3DXMATRIX**](d3d10-d3dxmatrix.md) structure that is the result of the operation.</span></span>

</dd> <dt>

<span data-ttu-id="d8ccd-110">*pQ* \[在\]</span><span class="sxs-lookup"><span data-stu-id="d8ccd-110">*pQ* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="d8ccd-111">Type： **Const [**D3DXQUATERNION**](../direct3d9/d3dxquaternion.md) \***</span><span class="sxs-lookup"><span data-stu-id="d8ccd-111">Type: **const [**D3DXQUATERNION**](../direct3d9/d3dxquaternion.md)\***</span></span>

<span data-ttu-id="d8ccd-112">來源 D3DXQUATERNION 結構的指標。</span><span class="sxs-lookup"><span data-stu-id="d8ccd-112">Pointer to the source D3DXQUATERNION structure.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="d8ccd-113">傳回值</span><span class="sxs-lookup"><span data-stu-id="d8ccd-113">Return value</span></span>

<span data-ttu-id="d8ccd-114">類型： **[ **D3DXMATRIX**](../direct3d9/d3dxmatrix.md)\***</span><span class="sxs-lookup"><span data-stu-id="d8ccd-114">Type: **[**D3DXMATRIX**](../direct3d9/d3dxmatrix.md)\***</span></span>

<span data-ttu-id="d8ccd-115">從來源四元數建立之 D3DXMATRIX 結構的指標。</span><span class="sxs-lookup"><span data-stu-id="d8ccd-115">Pointer to a D3DXMATRIX structure built from the source quaternion.</span></span>

## <a name="remarks"></a><span data-ttu-id="d8ccd-116">備註</span><span class="sxs-lookup"><span data-stu-id="d8ccd-116">Remarks</span></span>

<span data-ttu-id="d8ccd-117">此函式的傳回值與不悅參數中所傳回的值相同。</span><span class="sxs-lookup"><span data-stu-id="d8ccd-117">The return value for this function is the same value returned in the pOut parameter.</span></span> <span data-ttu-id="d8ccd-118">如此一來，D3DXMatrixRotationQuaternion 函式就可以用來做為另一個函式的參數。</span><span class="sxs-lookup"><span data-stu-id="d8ccd-118">In this way, the D3DXMatrixRotationQuaternion function can be used as a parameter for another function.</span></span>

<span data-ttu-id="d8ccd-119">如需如何從方向向量計算四元數值 ( x、y、z ) 和旋轉角度的詳細資訊，請參閱 [**D3DXQUATERNION**](d3d10-d3dxquaternion.md)。</span><span class="sxs-lookup"><span data-stu-id="d8ccd-119">For information about how to calculate quaternion values from a direction vector ( x, y, z ) and an angle of rotation, see [**D3DXQUATERNION**](d3d10-d3dxquaternion.md).</span></span>

## <a name="requirements"></a><span data-ttu-id="d8ccd-120">規格需求</span><span class="sxs-lookup"><span data-stu-id="d8ccd-120">Requirements</span></span>



| <span data-ttu-id="d8ccd-121">需求</span><span class="sxs-lookup"><span data-stu-id="d8ccd-121">Requirement</span></span> | <span data-ttu-id="d8ccd-122">值</span><span class="sxs-lookup"><span data-stu-id="d8ccd-122">Value</span></span> |
|--------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="d8ccd-123">標頭</span><span class="sxs-lookup"><span data-stu-id="d8ccd-123">Header</span></span><br/>  | <dl> <span data-ttu-id="d8ccd-124"><dt>D3DX10Math。h</dt></span><span class="sxs-lookup"><span data-stu-id="d8ccd-124"><dt>D3DX10Math.h</dt></span></span> </dl> |
| <span data-ttu-id="d8ccd-125">程式庫</span><span class="sxs-lookup"><span data-stu-id="d8ccd-125">Library</span></span><br/> | <dl> <span data-ttu-id="d8ccd-126"><dt>D3DX10 .lib</dt></span><span class="sxs-lookup"><span data-stu-id="d8ccd-126"><dt>D3DX10.lib</dt></span></span> </dl>   |



## <a name="see-also"></a><span data-ttu-id="d8ccd-127">另請參閱</span><span class="sxs-lookup"><span data-stu-id="d8ccd-127">See also</span></span>

<dl> <dt>

[<span data-ttu-id="d8ccd-128">數學函數</span><span class="sxs-lookup"><span data-stu-id="d8ccd-128">Math Functions</span></span>](d3d10-graphics-reference-d3dx10-functions-math.md)
</dt> </dl>

 

 
