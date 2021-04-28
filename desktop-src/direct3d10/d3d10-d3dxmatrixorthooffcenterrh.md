---
description: D3DXMatrixOrthoOffCenterRH 函式 (D3DX10Math) -建立自訂、右手的正向投射矩陣。
ms.assetid: 01d4d61e-de7b-4431-a168-68a50b1d6021
title: 'D3DXMatrixOrthoOffCenterRH 函式 (D3DX10Math) '
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- D3DXMatrixOrthoOffCenterRH
api_type:
- LibDef
api_location:
- D3DX10.lib
- D3DX10.dll
ms.openlocfilehash: 0b41038021cc34cb02961cb9894415995955404c
ms.sourcegitcommit: 95685061d5b0333bbf9e6ebd208dde8190f97005
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 04/28/2021
ms.locfileid: "108113076"
---
# <a name="d3dxmatrixorthooffcenterrh-function-d3dx10mathh"></a><span data-ttu-id="e1b72-103">D3DXMatrixOrthoOffCenterRH 函式 (D3DX10Math) </span><span class="sxs-lookup"><span data-stu-id="e1b72-103">D3DXMatrixOrthoOffCenterRH function (D3DX10Math.h)</span></span>

<span data-ttu-id="e1b72-104">建立自訂、右手的正向投射矩陣。</span><span class="sxs-lookup"><span data-stu-id="e1b72-104">Builds a customized, right-handed orthographic projection matrix.</span></span>

## <a name="syntax"></a><span data-ttu-id="e1b72-105">語法</span><span class="sxs-lookup"><span data-stu-id="e1b72-105">Syntax</span></span>


```C++
D3DXMATRIX* D3DXMatrixOrthoOffCenterRH(
  _Inout_ D3DXMATRIX *pOut,
  _In_    FLOAT      l,
  _In_    FLOAT      r,
  _In_    FLOAT      b,
  _In_    FLOAT      t,
  _In_    FLOAT      zn,
  _In_    FLOAT      zf
);
```



## <a name="parameters"></a><span data-ttu-id="e1b72-106">參數</span><span class="sxs-lookup"><span data-stu-id="e1b72-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="e1b72-107">*不悅* \[in、out\]</span><span class="sxs-lookup"><span data-stu-id="e1b72-107">*pOut* \[in, out\]</span></span>
</dt> <dd>

<span data-ttu-id="e1b72-108">類型： **[ **D3DXMATRIX**](../direct3d9/d3dxmatrix.md)\***</span><span class="sxs-lookup"><span data-stu-id="e1b72-108">Type: **[**D3DXMATRIX**](../direct3d9/d3dxmatrix.md)\***</span></span>

<span data-ttu-id="e1b72-109">產生之 [**D3DXMATRIX**](d3d10-d3dxmatrix.md)的指標。</span><span class="sxs-lookup"><span data-stu-id="e1b72-109">Pointer to the resulting [**D3DXMATRIX**](d3d10-d3dxmatrix.md).</span></span>

</dd> <dt>

<span data-ttu-id="e1b72-110">*l* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="e1b72-110">*l* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="e1b72-111">類型： **[ **FLOAT**](../winprog/windows-data-types.md)**</span><span class="sxs-lookup"><span data-stu-id="e1b72-111">Type: **[**FLOAT**](../winprog/windows-data-types.md)**</span></span>

<span data-ttu-id="e1b72-112">視圖量的最小 x 值。</span><span class="sxs-lookup"><span data-stu-id="e1b72-112">Minimum x-value of view volume.</span></span>

</dd> <dt>

<span data-ttu-id="e1b72-113">*r* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="e1b72-113">*r* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="e1b72-114">類型： **[ **FLOAT**](../winprog/windows-data-types.md)**</span><span class="sxs-lookup"><span data-stu-id="e1b72-114">Type: **[**FLOAT**](../winprog/windows-data-types.md)**</span></span>

<span data-ttu-id="e1b72-115">視圖量的最大 x 值。</span><span class="sxs-lookup"><span data-stu-id="e1b72-115">Maximum x-value of view volume.</span></span>

</dd> <dt>

<span data-ttu-id="e1b72-116">*b* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="e1b72-116">*b* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="e1b72-117">類型： **[ **FLOAT**](../winprog/windows-data-types.md)**</span><span class="sxs-lookup"><span data-stu-id="e1b72-117">Type: **[**FLOAT**](../winprog/windows-data-types.md)**</span></span>

<span data-ttu-id="e1b72-118">View volume 的最小 y 值。</span><span class="sxs-lookup"><span data-stu-id="e1b72-118">Minimum y-value of view volume.</span></span>

</dd> <dt>

<span data-ttu-id="e1b72-119"> \[ 中的 t\]</span><span class="sxs-lookup"><span data-stu-id="e1b72-119">*t* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="e1b72-120">類型： **[ **FLOAT**](../winprog/windows-data-types.md)**</span><span class="sxs-lookup"><span data-stu-id="e1b72-120">Type: **[**FLOAT**](../winprog/windows-data-types.md)**</span></span>

<span data-ttu-id="e1b72-121">視圖量的最大 y 值。</span><span class="sxs-lookup"><span data-stu-id="e1b72-121">Maximum y-value of view volume.</span></span>

</dd> <dt>

<span data-ttu-id="e1b72-122">*zn* \[在\]</span><span class="sxs-lookup"><span data-stu-id="e1b72-122">*zn* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="e1b72-123">類型： **[ **FLOAT**](../winprog/windows-data-types.md)**</span><span class="sxs-lookup"><span data-stu-id="e1b72-123">Type: **[**FLOAT**](../winprog/windows-data-types.md)**</span></span>

<span data-ttu-id="e1b72-124">視圖音量的最小 z 值。</span><span class="sxs-lookup"><span data-stu-id="e1b72-124">Minimum z-value of the view volume.</span></span>

</dd> <dt>

<span data-ttu-id="e1b72-125">*zf* \[在\]</span><span class="sxs-lookup"><span data-stu-id="e1b72-125">*zf* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="e1b72-126">類型： **[ **FLOAT**](../winprog/windows-data-types.md)**</span><span class="sxs-lookup"><span data-stu-id="e1b72-126">Type: **[**FLOAT**](../winprog/windows-data-types.md)**</span></span>

<span data-ttu-id="e1b72-127">視圖音量的最大 z 值。</span><span class="sxs-lookup"><span data-stu-id="e1b72-127">Maximum z-value of the view volume.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="e1b72-128">傳回值</span><span class="sxs-lookup"><span data-stu-id="e1b72-128">Return value</span></span>

<span data-ttu-id="e1b72-129">類型： **[ **D3DXMATRIX**](../direct3d9/d3dxmatrix.md)\***</span><span class="sxs-lookup"><span data-stu-id="e1b72-129">Type: **[**D3DXMATRIX**](../direct3d9/d3dxmatrix.md)\***</span></span>

<span data-ttu-id="e1b72-130">產生之 [**D3DXMATRIX**](d3d10-d3dxmatrix.md)的指標。</span><span class="sxs-lookup"><span data-stu-id="e1b72-130">Pointer to the resulting [**D3DXMATRIX**](d3d10-d3dxmatrix.md).</span></span>

## <a name="remarks"></a><span data-ttu-id="e1b72-131">備註</span><span class="sxs-lookup"><span data-stu-id="e1b72-131">Remarks</span></span>

<span data-ttu-id="e1b72-132">[**D3DXMatrixOrthoRH**](d3d10-d3dxmatrixorthorh.md)函式是 D3DXMatrixOrthoOffCenterRH 函數的特殊案例。</span><span class="sxs-lookup"><span data-stu-id="e1b72-132">The [**D3DXMatrixOrthoRH**](d3d10-d3dxmatrixorthorh.md) function is a special case of the D3DXMatrixOrthoOffCenterRH function.</span></span> <span data-ttu-id="e1b72-133">若要使用 D3DXMatrixOrthoOffCenterRH 建立相同的投射，請使用下列值：</span><span class="sxs-lookup"><span data-stu-id="e1b72-133">To create the same projection using D3DXMatrixOrthoOffCenterRH, use the following values:</span></span>

<span data-ttu-id="e1b72-134">l =-w/2，</span><span class="sxs-lookup"><span data-stu-id="e1b72-134">l = -w/2,</span></span>

<span data-ttu-id="e1b72-135">r = w/2，</span><span class="sxs-lookup"><span data-stu-id="e1b72-135">r = w/2,</span></span>

<span data-ttu-id="e1b72-136">b =-h/2，和</span><span class="sxs-lookup"><span data-stu-id="e1b72-136">b = -h/2, and</span></span>

<span data-ttu-id="e1b72-137">t = h/2。</span><span class="sxs-lookup"><span data-stu-id="e1b72-137">t = h/2.</span></span>

<span data-ttu-id="e1b72-138">D3DXMatrixOrthoOffCenterRH 函數的所有參數都是相機空間中的距離。</span><span class="sxs-lookup"><span data-stu-id="e1b72-138">All the parameters of the D3DXMatrixOrthoOffCenterRH function are distances in camera space.</span></span> <span data-ttu-id="e1b72-139">參數描述視圖磁片區的維度。</span><span class="sxs-lookup"><span data-stu-id="e1b72-139">The parameters describe the dimensions of the view volume.</span></span>

<span data-ttu-id="e1b72-140">此函式的傳回值與不悅參數中所傳回的值相同。</span><span class="sxs-lookup"><span data-stu-id="e1b72-140">The return value for this function is the same value returned in the pOut parameter.</span></span> <span data-ttu-id="e1b72-141">如此一來，D3DXMatrixOrthoOffCenterRH 函式就可以用來做為另一個函式的參數。</span><span class="sxs-lookup"><span data-stu-id="e1b72-141">In this way, the D3DXMatrixOrthoOffCenterRH function can be used as a parameter for another function.</span></span>

<span data-ttu-id="e1b72-142">此函數會使用下列公式來計算傳回的矩陣。</span><span class="sxs-lookup"><span data-stu-id="e1b72-142">This function uses the following formula to compute the returned matrix.</span></span>


```
2/(r-l)      0            0           0
0            2/(t-b)      0           0
0            0            1/(zn-zf)   0
(l+r)/(l-r)  (t+b)/(b-t)  zn/(zn-zf)  1
```



## <a name="requirements"></a><span data-ttu-id="e1b72-143">規格需求</span><span class="sxs-lookup"><span data-stu-id="e1b72-143">Requirements</span></span>



| <span data-ttu-id="e1b72-144">需求</span><span class="sxs-lookup"><span data-stu-id="e1b72-144">Requirement</span></span> | <span data-ttu-id="e1b72-145">值</span><span class="sxs-lookup"><span data-stu-id="e1b72-145">Value</span></span> |
|--------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="e1b72-146">標頭</span><span class="sxs-lookup"><span data-stu-id="e1b72-146">Header</span></span><br/>  | <dl> <span data-ttu-id="e1b72-147"><dt>D3DX10Math。h</dt></span><span class="sxs-lookup"><span data-stu-id="e1b72-147"><dt>D3DX10Math.h</dt></span></span> </dl> |
| <span data-ttu-id="e1b72-148">程式庫</span><span class="sxs-lookup"><span data-stu-id="e1b72-148">Library</span></span><br/> | <dl> <span data-ttu-id="e1b72-149"><dt>D3DX10 .lib</dt></span><span class="sxs-lookup"><span data-stu-id="e1b72-149"><dt>D3DX10.lib</dt></span></span> </dl>   |



## <a name="see-also"></a><span data-ttu-id="e1b72-150">另請參閱</span><span class="sxs-lookup"><span data-stu-id="e1b72-150">See also</span></span>

<dl> <dt>

[<span data-ttu-id="e1b72-151">數學函數</span><span class="sxs-lookup"><span data-stu-id="e1b72-151">Math Functions</span></span>](d3d10-graphics-reference-d3dx10-functions-math.md)
</dt> </dl>

 

 
