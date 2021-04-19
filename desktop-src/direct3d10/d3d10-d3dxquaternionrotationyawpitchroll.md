---
description: 使用指定的偏擺、音調和變換建立四元數。
ms.assetid: c929d9d4-b9cb-4de6-86c1-26fec3617846
title: 'D3DXQuaternionRotationYawPitchRoll 函式 (D3DX10Math) '
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- D3DXQuaternionRotationYawPitchRoll
api_type:
- LibDef
api_location:
- D3DX10.lib
- D3DX10.dll
ms.openlocfilehash: 7d894be61f5f22322f83c4e4a6c6a724de4b9da4
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 03/15/2021
ms.locfileid: "106992129"
---
# <a name="d3dxquaternionrotationyawpitchroll-function-d3dx10mathh"></a><span data-ttu-id="93506-103">D3DXQuaternionRotationYawPitchRoll 函式 (D3DX10Math) </span><span class="sxs-lookup"><span data-stu-id="93506-103">D3DXQuaternionRotationYawPitchRoll function (D3DX10Math.h)</span></span>

<span data-ttu-id="93506-104">使用指定的偏擺、音調和變換建立四元數。</span><span class="sxs-lookup"><span data-stu-id="93506-104">Builds a quaternion with the given yaw, pitch, and roll.</span></span>

## <a name="syntax"></a><span data-ttu-id="93506-105">語法</span><span class="sxs-lookup"><span data-stu-id="93506-105">Syntax</span></span>


```C++
D3DXQUATERNION* D3DXQuaternionRotationYawPitchRoll(
  _Inout_ D3DXQUATERNION *pOut,
  _In_    FLOAT          Yaw,
  _In_    FLOAT          Pitch,
  _In_    FLOAT          Roll
);
```



## <a name="parameters"></a><span data-ttu-id="93506-106">參數</span><span class="sxs-lookup"><span data-stu-id="93506-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="93506-107">*不悅* \[in、out\]</span><span class="sxs-lookup"><span data-stu-id="93506-107">*pOut* \[in, out\]</span></span>
</dt> <dd>

<span data-ttu-id="93506-108">類型： **[ **D3DXQUATERNION**](../direct3d9/d3dxquaternion.md)\***</span><span class="sxs-lookup"><span data-stu-id="93506-108">Type: **[**D3DXQUATERNION**](../direct3d9/d3dxquaternion.md)\***</span></span>

<span data-ttu-id="93506-109">作業結果之 [**D3DXQUATERNION**](d3d10-d3dxquaternion.md) 的指標。</span><span class="sxs-lookup"><span data-stu-id="93506-109">Pointer to the [**D3DXQUATERNION**](d3d10-d3dxquaternion.md) that is the result of the operation.</span></span>

</dd> <dt>

<span data-ttu-id="93506-110">*偏擺* \[在\]</span><span class="sxs-lookup"><span data-stu-id="93506-110">*Yaw* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="93506-111">類型： **[ **FLOAT**](../winprog/windows-data-types.md)**</span><span class="sxs-lookup"><span data-stu-id="93506-111">Type: **[**FLOAT**](../winprog/windows-data-types.md)**</span></span>

<span data-ttu-id="93506-112">偏擺圍繞 y 軸，以弧度為單位。</span><span class="sxs-lookup"><span data-stu-id="93506-112">Yaw around the y-axis, in radians.</span></span>

</dd> <dt>

<span data-ttu-id="93506-113">*推銷* \[在\]</span><span class="sxs-lookup"><span data-stu-id="93506-113">*Pitch* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="93506-114">類型： **[ **FLOAT**](../winprog/windows-data-types.md)**</span><span class="sxs-lookup"><span data-stu-id="93506-114">Type: **[**FLOAT**](../winprog/windows-data-types.md)**</span></span>

<span data-ttu-id="93506-115">X 軸的間距，以弧度為單位。</span><span class="sxs-lookup"><span data-stu-id="93506-115">Pitch around the x-axis, in radians.</span></span>

</dd> <dt>

<span data-ttu-id="93506-116">*滾動* \[在\]</span><span class="sxs-lookup"><span data-stu-id="93506-116">*Roll* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="93506-117">類型： **[ **FLOAT**](../winprog/windows-data-types.md)**</span><span class="sxs-lookup"><span data-stu-id="93506-117">Type: **[**FLOAT**](../winprog/windows-data-types.md)**</span></span>

<span data-ttu-id="93506-118">以弧度為單位，圍繞 Z 軸。</span><span class="sxs-lookup"><span data-stu-id="93506-118">Roll around the z-axis, in radians.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="93506-119">傳回值</span><span class="sxs-lookup"><span data-stu-id="93506-119">Return value</span></span>

<span data-ttu-id="93506-120">類型： **[ **D3DXQUATERNION**](../direct3d9/d3dxquaternion.md)\***</span><span class="sxs-lookup"><span data-stu-id="93506-120">Type: **[**D3DXQUATERNION**](../direct3d9/d3dxquaternion.md)\***</span></span>

<span data-ttu-id="93506-121">D3DXQUATERNION 結構的指標，該結構具有指定的偏擺、音調和滾動。</span><span class="sxs-lookup"><span data-stu-id="93506-121">Pointer to a D3DXQUATERNION structure with the specified yaw, pitch, and roll.</span></span>

## <a name="remarks"></a><span data-ttu-id="93506-122">備註</span><span class="sxs-lookup"><span data-stu-id="93506-122">Remarks</span></span>

<span data-ttu-id="93506-123">此函式的傳回值與不悅參數中所傳回的值相同。</span><span class="sxs-lookup"><span data-stu-id="93506-123">The return value for this function is the same value returned in the pOut parameter.</span></span> <span data-ttu-id="93506-124">如此一來，D3DXQuaternionRotationYawPitchRoll 函式就可以用來做為另一個函式的參數。</span><span class="sxs-lookup"><span data-stu-id="93506-124">In this way, the D3DXQuaternionRotationYawPitchRoll function can be used as a parameter for another function.</span></span>

<span data-ttu-id="93506-125">針對尚未正規化的任何四元數輸入，請使用 [**D3DXQuaternionNormalize**](d3d10-d3dxquaternionnormalize.md) 。</span><span class="sxs-lookup"><span data-stu-id="93506-125">Use [**D3DXQuaternionNormalize**](d3d10-d3dxquaternionnormalize.md) for any quaternion input that is not already normalized.</span></span>

## <a name="requirements"></a><span data-ttu-id="93506-126">規格需求</span><span class="sxs-lookup"><span data-stu-id="93506-126">Requirements</span></span>



| <span data-ttu-id="93506-127">需求</span><span class="sxs-lookup"><span data-stu-id="93506-127">Requirement</span></span> | <span data-ttu-id="93506-128">值</span><span class="sxs-lookup"><span data-stu-id="93506-128">Value</span></span> |
|--------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="93506-129">標頭</span><span class="sxs-lookup"><span data-stu-id="93506-129">Header</span></span><br/>  | <dl> <span data-ttu-id="93506-130"><dt>D3DX10Math。h</dt></span><span class="sxs-lookup"><span data-stu-id="93506-130"><dt>D3DX10Math.h</dt></span></span> </dl> |
| <span data-ttu-id="93506-131">程式庫</span><span class="sxs-lookup"><span data-stu-id="93506-131">Library</span></span><br/> | <dl> <span data-ttu-id="93506-132"><dt>D3DX10 .lib</dt></span><span class="sxs-lookup"><span data-stu-id="93506-132"><dt>D3DX10.lib</dt></span></span> </dl>   |



## <a name="see-also"></a><span data-ttu-id="93506-133">另請參閱</span><span class="sxs-lookup"><span data-stu-id="93506-133">See also</span></span>

<dl> <dt>

[<span data-ttu-id="93506-134">數學函數</span><span class="sxs-lookup"><span data-stu-id="93506-134">Math Functions</span></span>](d3d10-graphics-reference-d3dx10-functions-math.md)
</dt> </dl>

 

 
