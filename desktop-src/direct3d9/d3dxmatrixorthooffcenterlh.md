---
description: D3DXMatrixOrthoOffCenterLH 函式 (D3dx9math) -建立自訂的左手投影投射矩陣。
ms.assetid: e4f087e5-63d9-49ca-9d8e-3a25070e1a51
title: 'D3DXMatrixOrthoOffCenterLH 函式 (D3dx9math) '
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- D3DXMatrixOrthoOffCenterLH
api_type:
- LibDef
api_location:
- d3dx9.lib
- d3dx9.dll
ms.openlocfilehash: 704bdab1d486399b28117cd078f556beb1347f7b
ms.sourcegitcommit: 95685061d5b0333bbf9e6ebd208dde8190f97005
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 04/28/2021
ms.locfileid: "108107486"
---
# <a name="d3dxmatrixorthooffcenterlh-function-d3dx9mathh"></a><span data-ttu-id="75d09-103">D3DXMatrixOrthoOffCenterLH 函式 (D3dx9math) </span><span class="sxs-lookup"><span data-stu-id="75d09-103">D3DXMatrixOrthoOffCenterLH function (D3dx9math.h)</span></span>

<span data-ttu-id="75d09-104">建立自訂、左方的正向投射矩陣。</span><span class="sxs-lookup"><span data-stu-id="75d09-104">Builds a customized, left-handed orthographic projection matrix.</span></span>

## <a name="syntax"></a><span data-ttu-id="75d09-105">語法</span><span class="sxs-lookup"><span data-stu-id="75d09-105">Syntax</span></span>


```C++
D3DXMATRIX* D3DXMatrixOrthoOffCenterLH(
  _Inout_ D3DXMATRIX *pOut,
  _In_    FLOAT      l,
  _In_    FLOAT      r,
  _In_    FLOAT      b,
  _In_    FLOAT      t,
  _In_    FLOAT      zn,
  _In_    FLOAT      zf
);
```



## <a name="parameters"></a><span data-ttu-id="75d09-106">參數</span><span class="sxs-lookup"><span data-stu-id="75d09-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="75d09-107">*不悅* \[in、out\]</span><span class="sxs-lookup"><span data-stu-id="75d09-107">*pOut* \[in, out\]</span></span>
</dt> <dd>

<span data-ttu-id="75d09-108">類型： **[ **D3DXMATRIX**](d3dxmatrix.md)\***</span><span class="sxs-lookup"><span data-stu-id="75d09-108">Type: **[**D3DXMATRIX**](d3dxmatrix.md)\***</span></span>

<span data-ttu-id="75d09-109">產生之 [**D3DXMATRIX**](../direct3d10/d3d10-d3dxmatrix.md)的指標。</span><span class="sxs-lookup"><span data-stu-id="75d09-109">Pointer to the resulting [**D3DXMATRIX**](../direct3d10/d3d10-d3dxmatrix.md).</span></span>

</dd> <dt>

<span data-ttu-id="75d09-110">*l* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="75d09-110">*l* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="75d09-111">類型： **[ **FLOAT**](../winprog/windows-data-types.md)**</span><span class="sxs-lookup"><span data-stu-id="75d09-111">Type: **[**FLOAT**](../winprog/windows-data-types.md)**</span></span>

<span data-ttu-id="75d09-112">視圖量的最小 x 值。</span><span class="sxs-lookup"><span data-stu-id="75d09-112">Minimum x-value of view volume.</span></span>

</dd> <dt>

<span data-ttu-id="75d09-113">*r* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="75d09-113">*r* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="75d09-114">類型： **[ **FLOAT**](../winprog/windows-data-types.md)**</span><span class="sxs-lookup"><span data-stu-id="75d09-114">Type: **[**FLOAT**](../winprog/windows-data-types.md)**</span></span>

<span data-ttu-id="75d09-115">視圖量的最大 x 值。</span><span class="sxs-lookup"><span data-stu-id="75d09-115">Maximum x-value of view volume.</span></span>

</dd> <dt>

<span data-ttu-id="75d09-116">*b* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="75d09-116">*b* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="75d09-117">類型： **[ **FLOAT**](../winprog/windows-data-types.md)**</span><span class="sxs-lookup"><span data-stu-id="75d09-117">Type: **[**FLOAT**](../winprog/windows-data-types.md)**</span></span>

<span data-ttu-id="75d09-118">View volume 的最小 y 值。</span><span class="sxs-lookup"><span data-stu-id="75d09-118">Minimum y-value of view volume.</span></span>

</dd> <dt>

<span data-ttu-id="75d09-119"> \[ 中的 t\]</span><span class="sxs-lookup"><span data-stu-id="75d09-119">*t* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="75d09-120">類型： **[ **FLOAT**](../winprog/windows-data-types.md)**</span><span class="sxs-lookup"><span data-stu-id="75d09-120">Type: **[**FLOAT**](../winprog/windows-data-types.md)**</span></span>

<span data-ttu-id="75d09-121">視圖量的最大 y 值。</span><span class="sxs-lookup"><span data-stu-id="75d09-121">Maximum y-value of view volume.</span></span>

</dd> <dt>

<span data-ttu-id="75d09-122">*zn* \[在\]</span><span class="sxs-lookup"><span data-stu-id="75d09-122">*zn* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="75d09-123">類型： **[ **FLOAT**](../winprog/windows-data-types.md)**</span><span class="sxs-lookup"><span data-stu-id="75d09-123">Type: **[**FLOAT**](../winprog/windows-data-types.md)**</span></span>

<span data-ttu-id="75d09-124">視圖音量的最小 z 值。</span><span class="sxs-lookup"><span data-stu-id="75d09-124">Minimum z-value of the view volume.</span></span>

</dd> <dt>

<span data-ttu-id="75d09-125">*zf* \[在\]</span><span class="sxs-lookup"><span data-stu-id="75d09-125">*zf* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="75d09-126">類型： **[ **FLOAT**](../winprog/windows-data-types.md)**</span><span class="sxs-lookup"><span data-stu-id="75d09-126">Type: **[**FLOAT**](../winprog/windows-data-types.md)**</span></span>

<span data-ttu-id="75d09-127">視圖音量的最大 z 值。</span><span class="sxs-lookup"><span data-stu-id="75d09-127">Maximum z-value of the view volume.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="75d09-128">傳回值</span><span class="sxs-lookup"><span data-stu-id="75d09-128">Return value</span></span>

<span data-ttu-id="75d09-129">類型： **[ **D3DXMATRIX**](d3dxmatrix.md)\***</span><span class="sxs-lookup"><span data-stu-id="75d09-129">Type: **[**D3DXMATRIX**](d3dxmatrix.md)\***</span></span>

<span data-ttu-id="75d09-130">產生之 [**D3DXMATRIX**](../direct3d10/d3d10-d3dxmatrix.md)的指標。</span><span class="sxs-lookup"><span data-stu-id="75d09-130">Pointer to the resulting [**D3DXMATRIX**](../direct3d10/d3d10-d3dxmatrix.md).</span></span>

## <a name="remarks"></a><span data-ttu-id="75d09-131">備註</span><span class="sxs-lookup"><span data-stu-id="75d09-131">Remarks</span></span>

<span data-ttu-id="75d09-132">[**D3DXMatrixOrthoLH**](d3dxmatrixortholh.md)函式是 **D3DXMatrixOrthoOffCenterLH** 函數的特殊案例。</span><span class="sxs-lookup"><span data-stu-id="75d09-132">The [**D3DXMatrixOrthoLH**](d3dxmatrixortholh.md) function is a special case of the **D3DXMatrixOrthoOffCenterLH** function.</span></span> <span data-ttu-id="75d09-133">若要使用 **D3DXMatrixOrthoOffCenterLH** 建立相同的投射，請使用下列值： l =-w/2，r = w/2，b =-h/2，以及 t = h/2。</span><span class="sxs-lookup"><span data-stu-id="75d09-133">To create the same projection using **D3DXMatrixOrthoOffCenterLH**, use the following values: l = -w/2, r = w/2, b = -h/2, and t = h/2.</span></span>

<span data-ttu-id="75d09-134">**D3DXMatrixOrthoOffCenterLH** 函數的所有參數都是相機空間中的距離。</span><span class="sxs-lookup"><span data-stu-id="75d09-134">All the parameters of the **D3DXMatrixOrthoOffCenterLH** function are distances in camera space.</span></span> <span data-ttu-id="75d09-135">參數描述視圖磁片區的維度。</span><span class="sxs-lookup"><span data-stu-id="75d09-135">The parameters describe the dimensions of the view volume.</span></span>

<span data-ttu-id="75d09-136">此函式的傳回值與 *不悅* 參數中所傳回的值相同。</span><span class="sxs-lookup"><span data-stu-id="75d09-136">The return value for this function is the same value returned in the *pOut* parameter.</span></span> <span data-ttu-id="75d09-137">如此一來， **D3DXMatrixOrthoOffCenterLH** 函式就可以用來做為另一個函式的參數。</span><span class="sxs-lookup"><span data-stu-id="75d09-137">In this way, the **D3DXMatrixOrthoOffCenterLH** function can be used as a parameter for another function.</span></span>

<span data-ttu-id="75d09-138">此函數會使用下列公式來計算傳回的矩陣。</span><span class="sxs-lookup"><span data-stu-id="75d09-138">This function uses the following formula to compute the returned matrix.</span></span>


```
2/(r-l)      0            0           0
0            2/(t-b)      0           0
0            0            1/(zf-zn)   0
(l+r)/(l-r)  (t+b)/(b-t)  zn/(zn-zf)  1
```



## <a name="requirements"></a><span data-ttu-id="75d09-139">規格需求</span><span class="sxs-lookup"><span data-stu-id="75d09-139">Requirements</span></span>



| <span data-ttu-id="75d09-140">需求</span><span class="sxs-lookup"><span data-stu-id="75d09-140">Requirement</span></span> | <span data-ttu-id="75d09-141">值</span><span class="sxs-lookup"><span data-stu-id="75d09-141">Value</span></span> |
|--------------------|----------------------------------------------------------------------------------------|
| <span data-ttu-id="75d09-142">標頭</span><span class="sxs-lookup"><span data-stu-id="75d09-142">Header</span></span><br/>  | <dl> <span data-ttu-id="75d09-143"><dt>D3dx9math。h</dt></span><span class="sxs-lookup"><span data-stu-id="75d09-143"><dt>D3dx9math.h</dt></span></span> </dl> |
| <span data-ttu-id="75d09-144">程式庫</span><span class="sxs-lookup"><span data-stu-id="75d09-144">Library</span></span><br/> | <dl> <span data-ttu-id="75d09-145"><dt>D3dx9 .lib</dt></span><span class="sxs-lookup"><span data-stu-id="75d09-145"><dt>D3dx9.lib</dt></span></span> </dl>   |



## <a name="see-also"></a><span data-ttu-id="75d09-146">另請參閱</span><span class="sxs-lookup"><span data-stu-id="75d09-146">See also</span></span>

<dl> <dt>

[<span data-ttu-id="75d09-147">數學函數</span><span class="sxs-lookup"><span data-stu-id="75d09-147">Math Functions</span></span>](dx9-graphics-reference-d3dx-functions-math.md)
</dt> <dt>

[<span data-ttu-id="75d09-148">**D3DXMatrixOrthoRH**</span><span class="sxs-lookup"><span data-stu-id="75d09-148">**D3DXMatrixOrthoRH**</span></span>](d3dxmatrixorthorh.md)
</dt> <dt>

[<span data-ttu-id="75d09-149">**D3DXMatrixOrthoLH**</span><span class="sxs-lookup"><span data-stu-id="75d09-149">**D3DXMatrixOrthoLH**</span></span>](d3dxmatrixortholh.md)
</dt> <dt>

[<span data-ttu-id="75d09-150">**D3DXMatrixOrthoOffCenterRH**</span><span class="sxs-lookup"><span data-stu-id="75d09-150">**D3DXMatrixOrthoOffCenterRH**</span></span>](d3dxmatrixorthooffcenterrh.md)
</dt> </dl>

 

 
