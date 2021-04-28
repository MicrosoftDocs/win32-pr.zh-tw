---
description: D3DXMatrixRotationYawPitchRoll 函式 (D3DX10Math) -建立具有指定之偏擺、音調和變換的矩陣。
ms.assetid: a3ef2b57-275f-484a-88fc-aaa5e470717c
title: 'D3DXMatrixRotationYawPitchRoll 函式 (D3DX10Math) '
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
- D3DX10.lib
- D3DX10.dll
ms.openlocfilehash: ae00865c45878159dbf86a6f829e9d1cf50337e3
ms.sourcegitcommit: 95685061d5b0333bbf9e6ebd208dde8190f97005
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 04/28/2021
ms.locfileid: "108108946"
---
# <a name="d3dxmatrixrotationyawpitchroll-function-d3dx10mathh"></a><span data-ttu-id="58076-103">D3DXMatrixRotationYawPitchRoll 函式 (D3DX10Math) </span><span class="sxs-lookup"><span data-stu-id="58076-103">D3DXMatrixRotationYawPitchRoll function (D3DX10Math.h)</span></span>

<span data-ttu-id="58076-104">建立具有指定之偏擺、音調和變換的矩陣。</span><span class="sxs-lookup"><span data-stu-id="58076-104">Builds a matrix with a specified yaw, pitch, and roll.</span></span>

## <a name="syntax"></a><span data-ttu-id="58076-105">語法</span><span class="sxs-lookup"><span data-stu-id="58076-105">Syntax</span></span>


```C++
D3DXMATRIX* D3DXMatrixRotationYawPitchRoll(
  _Inout_ D3DXMATRIX *pOut,
  _In_    FLOAT      Yaw,
  _In_    FLOAT      Pitch,
  _In_    FLOAT      Roll
);
```



## <a name="parameters"></a><span data-ttu-id="58076-106">參數</span><span class="sxs-lookup"><span data-stu-id="58076-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="58076-107">*不悅* \[in、out\]</span><span class="sxs-lookup"><span data-stu-id="58076-107">*pOut* \[in, out\]</span></span>
</dt> <dd>

<span data-ttu-id="58076-108">類型： **[ **D3DXMATRIX**](../direct3d9/d3dxmatrix.md)\***</span><span class="sxs-lookup"><span data-stu-id="58076-108">Type: **[**D3DXMATRIX**](../direct3d9/d3dxmatrix.md)\***</span></span>

<span data-ttu-id="58076-109">[**D3DXMATRIX**](d3d10-d3dxmatrix.md)結構的指標，此結構是作業的結果。</span><span class="sxs-lookup"><span data-stu-id="58076-109">Pointer to the [**D3DXMATRIX**](d3d10-d3dxmatrix.md) structure that is the result of the operation.</span></span>

</dd> <dt>

<span data-ttu-id="58076-110">*偏擺* \[在\]</span><span class="sxs-lookup"><span data-stu-id="58076-110">*Yaw* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="58076-111">類型： **[ **FLOAT**](../winprog/windows-data-types.md)**</span><span class="sxs-lookup"><span data-stu-id="58076-111">Type: **[**FLOAT**](../winprog/windows-data-types.md)**</span></span>

<span data-ttu-id="58076-112">偏擺圍繞 y 軸，以弧度為單位。</span><span class="sxs-lookup"><span data-stu-id="58076-112">Yaw around the y-axis, in radians.</span></span>

</dd> <dt>

<span data-ttu-id="58076-113">*推銷* \[在\]</span><span class="sxs-lookup"><span data-stu-id="58076-113">*Pitch* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="58076-114">類型： **[ **FLOAT**](../winprog/windows-data-types.md)**</span><span class="sxs-lookup"><span data-stu-id="58076-114">Type: **[**FLOAT**](../winprog/windows-data-types.md)**</span></span>

<span data-ttu-id="58076-115">X 軸的間距，以弧度為單位。</span><span class="sxs-lookup"><span data-stu-id="58076-115">Pitch around the x-axis, in radians.</span></span>

</dd> <dt>

<span data-ttu-id="58076-116">*滾動* \[在\]</span><span class="sxs-lookup"><span data-stu-id="58076-116">*Roll* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="58076-117">類型： **[ **FLOAT**](../winprog/windows-data-types.md)**</span><span class="sxs-lookup"><span data-stu-id="58076-117">Type: **[**FLOAT**](../winprog/windows-data-types.md)**</span></span>

<span data-ttu-id="58076-118">以弧度為單位，圍繞 Z 軸。</span><span class="sxs-lookup"><span data-stu-id="58076-118">Roll around the z-axis, in radians.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="58076-119">傳回值</span><span class="sxs-lookup"><span data-stu-id="58076-119">Return value</span></span>

<span data-ttu-id="58076-120">類型： **[ **D3DXMATRIX**](../direct3d9/d3dxmatrix.md)\***</span><span class="sxs-lookup"><span data-stu-id="58076-120">Type: **[**D3DXMATRIX**](../direct3d9/d3dxmatrix.md)\***</span></span>

<span data-ttu-id="58076-121">D3DXMATRIX 結構的指標，該結構具有指定的偏擺、音調和滾動。</span><span class="sxs-lookup"><span data-stu-id="58076-121">Pointer to a D3DXMATRIX structure with the specified yaw, pitch, and roll.</span></span>

## <a name="remarks"></a><span data-ttu-id="58076-122">備註</span><span class="sxs-lookup"><span data-stu-id="58076-122">Remarks</span></span>

<span data-ttu-id="58076-123">此函式的傳回值與不悅參數中所傳回的值相同。</span><span class="sxs-lookup"><span data-stu-id="58076-123">The return value for this function is the same value returned in the pOut parameter.</span></span> <span data-ttu-id="58076-124">如此一來，D3DXMatrixRotationYawPitchRoll 函式就可以用來做為另一個函式的參數。</span><span class="sxs-lookup"><span data-stu-id="58076-124">In this way, the D3DXMatrixRotationYawPitchRoll function can be used as a parameter for another function.</span></span>

<span data-ttu-id="58076-125">轉換順序會優先擲出，然後再偏擺。</span><span class="sxs-lookup"><span data-stu-id="58076-125">The order of transformations is roll first, then pitch, then yaw.</span></span> <span data-ttu-id="58076-126">相對於物件的本機座標軸，這相當於圍繞 Z 軸的旋轉，後面接著圍繞 X 軸旋轉，後面接著旋轉 y 軸（如下圖所示）。</span><span class="sxs-lookup"><span data-stu-id="58076-126">Relative to the object's local coordinate axis, this is equivalent to rotation around the z-axis, followed by rotation around the x-axis, followed by rotation around the y-axis, as shown in the following illustration.</span></span>

![捲軸、音調和偏擺的圖例，作為三個軸的旋轉](images/pitchyawroll.png)

## <a name="requirements"></a><span data-ttu-id="58076-128">規格需求</span><span class="sxs-lookup"><span data-stu-id="58076-128">Requirements</span></span>



| <span data-ttu-id="58076-129">需求</span><span class="sxs-lookup"><span data-stu-id="58076-129">Requirement</span></span> | <span data-ttu-id="58076-130">值</span><span class="sxs-lookup"><span data-stu-id="58076-130">Value</span></span> |
|--------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="58076-131">標頭</span><span class="sxs-lookup"><span data-stu-id="58076-131">Header</span></span><br/>  | <dl> <span data-ttu-id="58076-132"><dt>D3DX10Math。h</dt></span><span class="sxs-lookup"><span data-stu-id="58076-132"><dt>D3DX10Math.h</dt></span></span> </dl> |
| <span data-ttu-id="58076-133">程式庫</span><span class="sxs-lookup"><span data-stu-id="58076-133">Library</span></span><br/> | <dl> <span data-ttu-id="58076-134"><dt>D3DX10 .lib</dt></span><span class="sxs-lookup"><span data-stu-id="58076-134"><dt>D3DX10.lib</dt></span></span> </dl>   |



## <a name="see-also"></a><span data-ttu-id="58076-135">另請參閱</span><span class="sxs-lookup"><span data-stu-id="58076-135">See also</span></span>

<dl> <dt>

[<span data-ttu-id="58076-136">數學函數</span><span class="sxs-lookup"><span data-stu-id="58076-136">Math Functions</span></span>](d3d10-graphics-reference-d3dx10-functions-math.md)
</dt> </dl>

 

 
