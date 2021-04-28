---
description: D3DXMatrixRotationYawPitchRoll 函式 (D3dx9math) -建立具有指定之偏擺、音調和變換的矩陣。
ms.assetid: efaab508-34ed-4373-a8d0-3bc459d75f39
title: 'D3DXMatrixRotationYawPitchRoll 函式 (D3dx9math) '
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- D3DXMatrixRotationYawPitchRoll
api_type:
- LibDef
api_location:
- d3dx9.lib
- d3dx9.dll
ms.openlocfilehash: 789812b6e94efd40ff71209348f0c9727088c253
ms.sourcegitcommit: 95685061d5b0333bbf9e6ebd208dde8190f97005
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 04/28/2021
ms.locfileid: "108118146"
---
# <a name="d3dxmatrixrotationyawpitchroll-function-d3dx9mathh"></a><span data-ttu-id="18af2-103">D3DXMatrixRotationYawPitchRoll 函式 (D3dx9math) </span><span class="sxs-lookup"><span data-stu-id="18af2-103">D3DXMatrixRotationYawPitchRoll function (D3dx9math.h)</span></span>

<span data-ttu-id="18af2-104">建立具有指定之偏擺、音調和變換的矩陣。</span><span class="sxs-lookup"><span data-stu-id="18af2-104">Builds a matrix with a specified yaw, pitch, and roll.</span></span>

## <a name="syntax"></a><span data-ttu-id="18af2-105">語法</span><span class="sxs-lookup"><span data-stu-id="18af2-105">Syntax</span></span>


```C++
D3DXMATRIX* D3DXMatrixRotationYawPitchRoll(
  _Inout_ D3DXMATRIX *pOut,
  _In_    FLOAT      Yaw,
  _In_    FLOAT      Pitch,
  _In_    FLOAT      Roll
);
```



## <a name="parameters"></a><span data-ttu-id="18af2-106">參數</span><span class="sxs-lookup"><span data-stu-id="18af2-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="18af2-107">*不悅* \[in、out\]</span><span class="sxs-lookup"><span data-stu-id="18af2-107">*pOut* \[in, out\]</span></span>
</dt> <dd>

<span data-ttu-id="18af2-108">類型： **[ **D3DXMATRIX**](d3dxmatrix.md)\***</span><span class="sxs-lookup"><span data-stu-id="18af2-108">Type: **[**D3DXMATRIX**](d3dxmatrix.md)\***</span></span>

<span data-ttu-id="18af2-109">[**D3DXMATRIX**](d3dxmatrix.md)結構的指標，此結構是作業的結果。</span><span class="sxs-lookup"><span data-stu-id="18af2-109">Pointer to the [**D3DXMATRIX**](d3dxmatrix.md) structure that is the result of the operation.</span></span>

</dd> <dt>

<span data-ttu-id="18af2-110">*偏擺* \[在\]</span><span class="sxs-lookup"><span data-stu-id="18af2-110">*Yaw* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="18af2-111">類型： **[ **FLOAT**](../winprog/windows-data-types.md)**</span><span class="sxs-lookup"><span data-stu-id="18af2-111">Type: **[**FLOAT**](../winprog/windows-data-types.md)**</span></span>

<span data-ttu-id="18af2-112">偏擺圍繞 y 軸，以弧度為單位。</span><span class="sxs-lookup"><span data-stu-id="18af2-112">Yaw around the y-axis, in radians.</span></span>

</dd> <dt>

<span data-ttu-id="18af2-113">*推銷* \[在\]</span><span class="sxs-lookup"><span data-stu-id="18af2-113">*Pitch* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="18af2-114">類型： **[ **FLOAT**](../winprog/windows-data-types.md)**</span><span class="sxs-lookup"><span data-stu-id="18af2-114">Type: **[**FLOAT**](../winprog/windows-data-types.md)**</span></span>

<span data-ttu-id="18af2-115">X 軸的間距，以弧度為單位。</span><span class="sxs-lookup"><span data-stu-id="18af2-115">Pitch around the x-axis, in radians.</span></span>

</dd> <dt>

<span data-ttu-id="18af2-116">*滾動* \[在\]</span><span class="sxs-lookup"><span data-stu-id="18af2-116">*Roll* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="18af2-117">類型： **[ **FLOAT**](../winprog/windows-data-types.md)**</span><span class="sxs-lookup"><span data-stu-id="18af2-117">Type: **[**FLOAT**](../winprog/windows-data-types.md)**</span></span>

<span data-ttu-id="18af2-118">以弧度為單位，圍繞 Z 軸。</span><span class="sxs-lookup"><span data-stu-id="18af2-118">Roll around the z-axis, in radians.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="18af2-119">傳回值</span><span class="sxs-lookup"><span data-stu-id="18af2-119">Return value</span></span>

<span data-ttu-id="18af2-120">類型： **[ **D3DXMATRIX**](d3dxmatrix.md)\***</span><span class="sxs-lookup"><span data-stu-id="18af2-120">Type: **[**D3DXMATRIX**](d3dxmatrix.md)\***</span></span>

<span data-ttu-id="18af2-121">[**D3DXMATRIX**](d3dxmatrix.md)結構的指標，該結構具有指定的偏擺、音調和滾動。</span><span class="sxs-lookup"><span data-stu-id="18af2-121">Pointer to a [**D3DXMATRIX**](d3dxmatrix.md) structure with the specified yaw, pitch, and roll.</span></span>

## <a name="remarks"></a><span data-ttu-id="18af2-122">備註</span><span class="sxs-lookup"><span data-stu-id="18af2-122">Remarks</span></span>

<span data-ttu-id="18af2-123">此函式的傳回值與 *不悅* 參數中所傳回的值相同。</span><span class="sxs-lookup"><span data-stu-id="18af2-123">The return value for this function is the same value returned in the *pOut* parameter.</span></span> <span data-ttu-id="18af2-124">如此一來， **D3DXMatrixRotationYawPitchRoll** 函式就可以用來做為另一個函式的參數。</span><span class="sxs-lookup"><span data-stu-id="18af2-124">In this way, the **D3DXMatrixRotationYawPitchRoll** function can be used as a parameter for another function.</span></span>

<span data-ttu-id="18af2-125">轉換順序會優先擲出，然後再偏擺。</span><span class="sxs-lookup"><span data-stu-id="18af2-125">The order of transformations is roll first, then pitch, then yaw.</span></span> <span data-ttu-id="18af2-126">相對於物件的本機座標軸，這相當於圍繞 Z 軸的旋轉，後面接著圍繞 X 軸旋轉，後面接著旋轉 y 軸（如下圖所示）。</span><span class="sxs-lookup"><span data-stu-id="18af2-126">Relative to the object's local coordinate axis, this is equivalent to rotation around the z-axis, followed by rotation around the x-axis, followed by rotation around the y-axis, as shown in the following illustration.</span></span>

![捲軸、音調和偏擺的圖例，作為三個軸的旋轉](images/pitchyawroll.png)

## <a name="requirements"></a><span data-ttu-id="18af2-128">規格需求</span><span class="sxs-lookup"><span data-stu-id="18af2-128">Requirements</span></span>



| <span data-ttu-id="18af2-129">需求</span><span class="sxs-lookup"><span data-stu-id="18af2-129">Requirement</span></span> | <span data-ttu-id="18af2-130">值</span><span class="sxs-lookup"><span data-stu-id="18af2-130">Value</span></span> |
|--------------------|----------------------------------------------------------------------------------------|
| <span data-ttu-id="18af2-131">標頭</span><span class="sxs-lookup"><span data-stu-id="18af2-131">Header</span></span><br/>  | <dl> <span data-ttu-id="18af2-132"><dt>D3dx9math。h</dt></span><span class="sxs-lookup"><span data-stu-id="18af2-132"><dt>D3dx9math.h</dt></span></span> </dl> |
| <span data-ttu-id="18af2-133">程式庫</span><span class="sxs-lookup"><span data-stu-id="18af2-133">Library</span></span><br/> | <dl> <span data-ttu-id="18af2-134"><dt>D3dx9 .lib</dt></span><span class="sxs-lookup"><span data-stu-id="18af2-134"><dt>D3dx9.lib</dt></span></span> </dl>   |



## <a name="see-also"></a><span data-ttu-id="18af2-135">另請參閱</span><span class="sxs-lookup"><span data-stu-id="18af2-135">See also</span></span>

<dl> <dt>

[<span data-ttu-id="18af2-136">數學函數</span><span class="sxs-lookup"><span data-stu-id="18af2-136">Math Functions</span></span>](dx9-graphics-reference-d3dx-functions-math.md)
</dt> <dt>

[<span data-ttu-id="18af2-137">**D3DXMatrixRotationAxis**</span><span class="sxs-lookup"><span data-stu-id="18af2-137">**D3DXMatrixRotationAxis**</span></span>](d3dxmatrixrotationaxis.md)
</dt> <dt>

[<span data-ttu-id="18af2-138">**D3DXMatrixRotationQuaternion**</span><span class="sxs-lookup"><span data-stu-id="18af2-138">**D3DXMatrixRotationQuaternion**</span></span>](d3dxmatrixrotationquaternion.md)
</dt> <dt>

[<span data-ttu-id="18af2-139">**D3DXMatrixRotationX**</span><span class="sxs-lookup"><span data-stu-id="18af2-139">**D3DXMatrixRotationX**</span></span>](d3dxmatrixrotationx.md)
</dt> <dt>

[<span data-ttu-id="18af2-140">**D3DXMatrixRotationY**</span><span class="sxs-lookup"><span data-stu-id="18af2-140">**D3DXMatrixRotationY**</span></span>](d3dxmatrixrotationy.md)
</dt> <dt>

[<span data-ttu-id="18af2-141">**D3DXMatrixRotationZ**</span><span class="sxs-lookup"><span data-stu-id="18af2-141">**D3DXMatrixRotationZ**</span></span>](d3dxmatrixrotationz.md)
</dt> </dl>

 

 
