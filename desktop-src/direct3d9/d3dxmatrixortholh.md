---
description: 建立左手向的正射投射矩陣。
ms.assetid: e42151bd-2302-491b-a211-7d5a4b8e437f
title: 'D3DXMatrixOrthoLH 函式 (D3dx9math) '
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- D3DXMatrixOrthoLH
api_type:
- LibDef
api_location:
- d3dx9.lib
- d3dx9.dll
ms.openlocfilehash: 4aaf4a1a770ba0200a6afe389d37e248b9f4c7de
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 03/15/2021
ms.locfileid: "104323147"
---
# <a name="d3dxmatrixortholh-function-d3dx9mathh"></a><span data-ttu-id="ac856-103">D3DXMatrixOrthoLH 函式 (D3dx9math) </span><span class="sxs-lookup"><span data-stu-id="ac856-103">D3DXMatrixOrthoLH function (D3dx9math.h)</span></span>

<span data-ttu-id="ac856-104">建立左手向的正射投射矩陣。</span><span class="sxs-lookup"><span data-stu-id="ac856-104">Builds a left-handed orthographic projection matrix.</span></span>

## <a name="syntax"></a><span data-ttu-id="ac856-105">語法</span><span class="sxs-lookup"><span data-stu-id="ac856-105">Syntax</span></span>


```C++
D3DXMATRIX* D3DXMatrixOrthoLH(
  _Inout_ D3DXMATRIX *pOut,
  _In_    FLOAT      w,
  _In_    FLOAT      h,
  _In_    FLOAT      zn,
  _In_    FLOAT      zf
);
```



## <a name="parameters"></a><span data-ttu-id="ac856-106">參數</span><span class="sxs-lookup"><span data-stu-id="ac856-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="ac856-107">*不悅* \[in、out\]</span><span class="sxs-lookup"><span data-stu-id="ac856-107">*pOut* \[in, out\]</span></span>
</dt> <dd>

<span data-ttu-id="ac856-108">類型： **[ **D3DXMATRIX**](d3dxmatrix.md)\***</span><span class="sxs-lookup"><span data-stu-id="ac856-108">Type: **[**D3DXMATRIX**](d3dxmatrix.md)\***</span></span>

<span data-ttu-id="ac856-109">產生之 [**D3DXMATRIX**](../direct3d10/d3d10-d3dxmatrix.md)的指標。</span><span class="sxs-lookup"><span data-stu-id="ac856-109">Pointer to the resulting [**D3DXMATRIX**](../direct3d10/d3d10-d3dxmatrix.md).</span></span>

</dd> <dt>

<span data-ttu-id="ac856-110">*w* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="ac856-110">*w* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="ac856-111">類型： **[ **FLOAT**](../winprog/windows-data-types.md)**</span><span class="sxs-lookup"><span data-stu-id="ac856-111">Type: **[**FLOAT**](../winprog/windows-data-types.md)**</span></span>

<span data-ttu-id="ac856-112">視圖音量的寬度。</span><span class="sxs-lookup"><span data-stu-id="ac856-112">Width of the view volume.</span></span>

</dd> <dt>

<span data-ttu-id="ac856-113">*h* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="ac856-113">*h* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="ac856-114">類型： **[ **FLOAT**](../winprog/windows-data-types.md)**</span><span class="sxs-lookup"><span data-stu-id="ac856-114">Type: **[**FLOAT**](../winprog/windows-data-types.md)**</span></span>

<span data-ttu-id="ac856-115">視圖音量的高度。</span><span class="sxs-lookup"><span data-stu-id="ac856-115">Height of the view volume.</span></span>

</dd> <dt>

<span data-ttu-id="ac856-116">*zn* \[在\]</span><span class="sxs-lookup"><span data-stu-id="ac856-116">*zn* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="ac856-117">類型： **[ **FLOAT**](../winprog/windows-data-types.md)**</span><span class="sxs-lookup"><span data-stu-id="ac856-117">Type: **[**FLOAT**](../winprog/windows-data-types.md)**</span></span>

<span data-ttu-id="ac856-118">視圖音量的最小 z 值，稱為「z-近」。</span><span class="sxs-lookup"><span data-stu-id="ac856-118">Minimum z-value of the view volume which is referred to as z-near.</span></span>

</dd> <dt>

<span data-ttu-id="ac856-119">*zf* \[在\]</span><span class="sxs-lookup"><span data-stu-id="ac856-119">*zf* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="ac856-120">類型： **[ **FLOAT**](../winprog/windows-data-types.md)**</span><span class="sxs-lookup"><span data-stu-id="ac856-120">Type: **[**FLOAT**](../winprog/windows-data-types.md)**</span></span>

<span data-ttu-id="ac856-121">View 磁片區的最大 z 值，稱為「z-遠」。</span><span class="sxs-lookup"><span data-stu-id="ac856-121">Maximum z-value of the view volume which is referred to as z-far.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="ac856-122">傳回值</span><span class="sxs-lookup"><span data-stu-id="ac856-122">Return value</span></span>

<span data-ttu-id="ac856-123">類型： **[ **D3DXMATRIX**](d3dxmatrix.md)\***</span><span class="sxs-lookup"><span data-stu-id="ac856-123">Type: **[**D3DXMATRIX**](d3dxmatrix.md)\***</span></span>

<span data-ttu-id="ac856-124">產生之 [**D3DXMATRIX**](../direct3d10/d3d10-d3dxmatrix.md)的指標。</span><span class="sxs-lookup"><span data-stu-id="ac856-124">Pointer to the resulting [**D3DXMATRIX**](../direct3d10/d3d10-d3dxmatrix.md).</span></span>

## <a name="remarks"></a><span data-ttu-id="ac856-125">備註</span><span class="sxs-lookup"><span data-stu-id="ac856-125">Remarks</span></span>

<span data-ttu-id="ac856-126">**D3DXMatrixOrthoLH** 函數的所有參數都是相機空間中的距離。</span><span class="sxs-lookup"><span data-stu-id="ac856-126">All the parameters of the **D3DXMatrixOrthoLH** function are distances in camera space.</span></span> <span data-ttu-id="ac856-127">參數描述視圖磁片區的維度。</span><span class="sxs-lookup"><span data-stu-id="ac856-127">The parameters describe the dimensions of the view volume.</span></span>

<span data-ttu-id="ac856-128">此函式的傳回值與 *不悅* 參數中所傳回的值相同。</span><span class="sxs-lookup"><span data-stu-id="ac856-128">The return value for this function is the same value returned in the *pOut* parameter.</span></span> <span data-ttu-id="ac856-129">如此一來， **D3DXMatrixOrthoLH** 函式就可以用來做為另一個函式的參數。</span><span class="sxs-lookup"><span data-stu-id="ac856-129">In this way, the **D3DXMatrixOrthoLH** function can be used as a parameter for another function.</span></span>

<span data-ttu-id="ac856-130">此函數會使用下列公式來計算傳回的矩陣。</span><span class="sxs-lookup"><span data-stu-id="ac856-130">This function uses the following formula to compute the returned matrix.</span></span>


```
2/w  0    0           0
0    2/h  0           0
0    0    1/(zf-zn)   0
0    0   -zn/(zf-zn)  1
```



## <a name="requirements"></a><span data-ttu-id="ac856-131">規格需求</span><span class="sxs-lookup"><span data-stu-id="ac856-131">Requirements</span></span>



| <span data-ttu-id="ac856-132">需求</span><span class="sxs-lookup"><span data-stu-id="ac856-132">Requirement</span></span> | <span data-ttu-id="ac856-133">值</span><span class="sxs-lookup"><span data-stu-id="ac856-133">Value</span></span> |
|--------------------|----------------------------------------------------------------------------------------|
| <span data-ttu-id="ac856-134">標頭</span><span class="sxs-lookup"><span data-stu-id="ac856-134">Header</span></span><br/>  | <dl> <span data-ttu-id="ac856-135"><dt>D3dx9math。h</dt></span><span class="sxs-lookup"><span data-stu-id="ac856-135"><dt>D3dx9math.h</dt></span></span> </dl> |
| <span data-ttu-id="ac856-136">程式庫</span><span class="sxs-lookup"><span data-stu-id="ac856-136">Library</span></span><br/> | <dl> <span data-ttu-id="ac856-137"><dt>D3dx9 .lib</dt></span><span class="sxs-lookup"><span data-stu-id="ac856-137"><dt>D3dx9.lib</dt></span></span> </dl>   |



## <a name="see-also"></a><span data-ttu-id="ac856-138">另請參閱</span><span class="sxs-lookup"><span data-stu-id="ac856-138">See also</span></span>

<dl> <dt>

[<span data-ttu-id="ac856-139">數學函數</span><span class="sxs-lookup"><span data-stu-id="ac856-139">Math Functions</span></span>](dx9-graphics-reference-d3dx-functions-math.md)
</dt> <dt>

[<span data-ttu-id="ac856-140">**D3DXMatrixOrthoRH**</span><span class="sxs-lookup"><span data-stu-id="ac856-140">**D3DXMatrixOrthoRH**</span></span>](d3dxmatrixorthorh.md)
</dt> <dt>

[<span data-ttu-id="ac856-141">**D3DXMatrixOrthoOffCenterRH**</span><span class="sxs-lookup"><span data-stu-id="ac856-141">**D3DXMatrixOrthoOffCenterRH**</span></span>](d3dxmatrixorthooffcenterrh.md)
</dt> <dt>

[<span data-ttu-id="ac856-142">**D3DXMatrixOrthoOffCenterLH**</span><span class="sxs-lookup"><span data-stu-id="ac856-142">**D3DXMatrixOrthoOffCenterLH**</span></span>](d3dxmatrixorthooffcenterlh.md)
</dt> </dl>

 

 
