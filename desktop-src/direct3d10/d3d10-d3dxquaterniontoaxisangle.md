---
description: D3DXQuaternionToAxisAngle 函數 (D3DX10Math) -計算四元數的軸和旋轉角度。
ms.assetid: 1e81b88b-071d-46f1-b640-c70d063a14d1
title: 'D3DXQuaternionToAxisAngle 函式 (D3DX10Math) '
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- D3DXQuaternionToAxisAngle
api_type:
- LibDef
api_location:
- D3DX10.lib
- D3DX10.dll
ms.openlocfilehash: 51f704aa839ff210b3c2de57767cb32ec609232f
ms.sourcegitcommit: 95685061d5b0333bbf9e6ebd208dde8190f97005
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 04/28/2021
ms.locfileid: "108108696"
---
# <a name="d3dxquaterniontoaxisangle-function-d3dx10mathh"></a><span data-ttu-id="74f0a-103">D3DXQuaternionToAxisAngle 函式 (D3DX10Math) </span><span class="sxs-lookup"><span data-stu-id="74f0a-103">D3DXQuaternionToAxisAngle function (D3DX10Math.h)</span></span>

<span data-ttu-id="74f0a-104">計算四元數的軸和旋轉角度。</span><span class="sxs-lookup"><span data-stu-id="74f0a-104">Computes a quaternion's axis and angle of rotation.</span></span>

## <a name="syntax"></a><span data-ttu-id="74f0a-105">語法</span><span class="sxs-lookup"><span data-stu-id="74f0a-105">Syntax</span></span>


```C++
void D3DXQuaternionToAxisAngle(
  _In_    const D3DXQUATERNION *pQ,
  _Inout_       D3DXVECTOR3    *pAxis,
  _Inout_       FLOAT          *pAngle
);
```



## <a name="parameters"></a><span data-ttu-id="74f0a-106">參數</span><span class="sxs-lookup"><span data-stu-id="74f0a-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="74f0a-107">*pQ* \[在\]</span><span class="sxs-lookup"><span data-stu-id="74f0a-107">*pQ* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="74f0a-108">Type： **Const [**D3DXQUATERNION**](../direct3d9/d3dxquaternion.md) \***</span><span class="sxs-lookup"><span data-stu-id="74f0a-108">Type: **const [**D3DXQUATERNION**](../direct3d9/d3dxquaternion.md)\***</span></span>

<span data-ttu-id="74f0a-109">來源 [**D3DXQUATERNION**](d3d10-d3dxquaternion.md)的指標。</span><span class="sxs-lookup"><span data-stu-id="74f0a-109">Pointer to the source [**D3DXQUATERNION**](d3d10-d3dxquaternion.md).</span></span>

</dd> <dt>

<span data-ttu-id="74f0a-110">*pAxis* \[in、out\]</span><span class="sxs-lookup"><span data-stu-id="74f0a-110">*pAxis* \[in, out\]</span></span>
</dt> <dd>

<span data-ttu-id="74f0a-111">類型： **[ **D3DXVECTOR3**](../direct3d9/d3dxvector3.md)\***</span><span class="sxs-lookup"><span data-stu-id="74f0a-111">Type: **[**D3DXVECTOR3**](../direct3d9/d3dxvector3.md)\***</span></span>

<span data-ttu-id="74f0a-112">此函式會傳回 [**D3DXVECTOR3**](d3d10-d3dxvector3.md) 的指標，以識別四元數的旋轉軸。</span><span class="sxs-lookup"><span data-stu-id="74f0a-112">This function returns a pointer to a [**D3DXVECTOR3**](d3d10-d3dxvector3.md) that identifies the quaternion's axis of rotation.</span></span>

</dd> <dt>

<span data-ttu-id="74f0a-113">*pAngle* \[in、out\]</span><span class="sxs-lookup"><span data-stu-id="74f0a-113">*pAngle* \[in, out\]</span></span>
</dt> <dd>

<span data-ttu-id="74f0a-114">類型： **[ **FLOAT**](../winprog/windows-data-types.md)\***</span><span class="sxs-lookup"><span data-stu-id="74f0a-114">Type: **[**FLOAT**](../winprog/windows-data-types.md)\***</span></span>

<span data-ttu-id="74f0a-115">此函式會傳回浮點值的指標，此值會識別四元數的旋轉角度（以弧度為單位）。</span><span class="sxs-lookup"><span data-stu-id="74f0a-115">This function returns a pointer to a FLOAT value that identifies the quaternion's angle of rotation in radians.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="74f0a-116">傳回值</span><span class="sxs-lookup"><span data-stu-id="74f0a-116">Return value</span></span>

<span data-ttu-id="74f0a-117">沒有傳回值。</span><span class="sxs-lookup"><span data-stu-id="74f0a-117">No return value.</span></span>

## <a name="remarks"></a><span data-ttu-id="74f0a-118">備註</span><span class="sxs-lookup"><span data-stu-id="74f0a-118">Remarks</span></span>

<span data-ttu-id="74f0a-119">針對尚未正規化的任何四元數輸入，請使用 [**D3DXQuaternionNormalize**](d3d10-d3dxquaternionnormalize.md) 。</span><span class="sxs-lookup"><span data-stu-id="74f0a-119">Use [**D3DXQuaternionNormalize**](d3d10-d3dxquaternionnormalize.md) for any quaternion input that is not already normalized.</span></span>

## <a name="requirements"></a><span data-ttu-id="74f0a-120">規格需求</span><span class="sxs-lookup"><span data-stu-id="74f0a-120">Requirements</span></span>



| <span data-ttu-id="74f0a-121">需求</span><span class="sxs-lookup"><span data-stu-id="74f0a-121">Requirement</span></span> | <span data-ttu-id="74f0a-122">值</span><span class="sxs-lookup"><span data-stu-id="74f0a-122">Value</span></span> |
|--------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="74f0a-123">標頭</span><span class="sxs-lookup"><span data-stu-id="74f0a-123">Header</span></span><br/>  | <dl> <span data-ttu-id="74f0a-124"><dt>D3DX10Math。h</dt></span><span class="sxs-lookup"><span data-stu-id="74f0a-124"><dt>D3DX10Math.h</dt></span></span> </dl> |
| <span data-ttu-id="74f0a-125">程式庫</span><span class="sxs-lookup"><span data-stu-id="74f0a-125">Library</span></span><br/> | <dl> <span data-ttu-id="74f0a-126"><dt>D3DX10 .lib</dt></span><span class="sxs-lookup"><span data-stu-id="74f0a-126"><dt>D3DX10.lib</dt></span></span> </dl>   |



## <a name="see-also"></a><span data-ttu-id="74f0a-127">另請參閱</span><span class="sxs-lookup"><span data-stu-id="74f0a-127">See also</span></span>

<dl> <dt>

[<span data-ttu-id="74f0a-128">數學函數</span><span class="sxs-lookup"><span data-stu-id="74f0a-128">Math Functions</span></span>](d3d10-graphics-reference-d3dx10-functions-math.md)
</dt> </dl>

 

 
