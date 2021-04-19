---
description: 建立右手的正向投射矩陣。
ms.assetid: 6b9b50d5-0307-4fc7-a28d-8f42d2a21bf0
title: 'D3DXMatrixOrthoRH 函式 (D3dx9math) '
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- D3DXMatrixOrthoRH
api_type:
- LibDef
api_location:
- d3dx9.lib
- d3dx9.dll
ms.openlocfilehash: 00df0ee06768e4d57a68291dd1716e4a4574507e
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 03/15/2021
ms.locfileid: "107001476"
---
# <a name="d3dxmatrixorthorh-function-d3dx9mathh"></a><span data-ttu-id="55dcc-103">D3DXMatrixOrthoRH 函式 (D3dx9math) </span><span class="sxs-lookup"><span data-stu-id="55dcc-103">D3DXMatrixOrthoRH function (D3dx9math.h)</span></span>

<span data-ttu-id="55dcc-104">建立右手的正向投射矩陣。</span><span class="sxs-lookup"><span data-stu-id="55dcc-104">Builds a right-handed orthographic projection matrix.</span></span>

## <a name="syntax"></a><span data-ttu-id="55dcc-105">語法</span><span class="sxs-lookup"><span data-stu-id="55dcc-105">Syntax</span></span>


```C++
D3DXMATRIX* D3DXMatrixOrthoRH(
  _Inout_ D3DXMATRIX *pOut,
  _In_    FLOAT      w,
  _In_    FLOAT      h,
  _In_    FLOAT      zn,
  _In_    FLOAT      zf
);
```



## <a name="parameters"></a><span data-ttu-id="55dcc-106">參數</span><span class="sxs-lookup"><span data-stu-id="55dcc-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="55dcc-107">*不悅* \[in、out\]</span><span class="sxs-lookup"><span data-stu-id="55dcc-107">*pOut* \[in, out\]</span></span>
</dt> <dd>

<span data-ttu-id="55dcc-108">類型： **[ **D3DXMATRIX**](d3dxmatrix.md)\***</span><span class="sxs-lookup"><span data-stu-id="55dcc-108">Type: **[**D3DXMATRIX**](d3dxmatrix.md)\***</span></span>

<span data-ttu-id="55dcc-109">產生之 [**D3DXMATRIX**](../direct3d10/d3d10-d3dxmatrix.md)的指標。</span><span class="sxs-lookup"><span data-stu-id="55dcc-109">Pointer to the resulting [**D3DXMATRIX**](../direct3d10/d3d10-d3dxmatrix.md).</span></span>

</dd> <dt>

<span data-ttu-id="55dcc-110">*w* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="55dcc-110">*w* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="55dcc-111">類型： **[ **FLOAT**](../winprog/windows-data-types.md)**</span><span class="sxs-lookup"><span data-stu-id="55dcc-111">Type: **[**FLOAT**](../winprog/windows-data-types.md)**</span></span>

<span data-ttu-id="55dcc-112">視圖音量的寬度。</span><span class="sxs-lookup"><span data-stu-id="55dcc-112">Width of the view volume.</span></span>

</dd> <dt>

<span data-ttu-id="55dcc-113">*h* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="55dcc-113">*h* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="55dcc-114">類型： **[ **FLOAT**](../winprog/windows-data-types.md)**</span><span class="sxs-lookup"><span data-stu-id="55dcc-114">Type: **[**FLOAT**](../winprog/windows-data-types.md)**</span></span>

<span data-ttu-id="55dcc-115">視圖音量的高度。</span><span class="sxs-lookup"><span data-stu-id="55dcc-115">Height of the view volume.</span></span>

</dd> <dt>

<span data-ttu-id="55dcc-116">*zn* \[在\]</span><span class="sxs-lookup"><span data-stu-id="55dcc-116">*zn* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="55dcc-117">類型： **[ **FLOAT**](../winprog/windows-data-types.md)**</span><span class="sxs-lookup"><span data-stu-id="55dcc-117">Type: **[**FLOAT**](../winprog/windows-data-types.md)**</span></span>

<span data-ttu-id="55dcc-118">視圖音量的最小 z 值。</span><span class="sxs-lookup"><span data-stu-id="55dcc-118">Minimum z-value of the view volume.</span></span>

</dd> <dt>

<span data-ttu-id="55dcc-119">*zf* \[在\]</span><span class="sxs-lookup"><span data-stu-id="55dcc-119">*zf* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="55dcc-120">類型： **[ **FLOAT**](../winprog/windows-data-types.md)**</span><span class="sxs-lookup"><span data-stu-id="55dcc-120">Type: **[**FLOAT**](../winprog/windows-data-types.md)**</span></span>

<span data-ttu-id="55dcc-121">視圖音量的最大 z 值。</span><span class="sxs-lookup"><span data-stu-id="55dcc-121">Maximum z-value of the view volume.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="55dcc-122">傳回值</span><span class="sxs-lookup"><span data-stu-id="55dcc-122">Return value</span></span>

<span data-ttu-id="55dcc-123">類型： **[ **D3DXMATRIX**](d3dxmatrix.md)\***</span><span class="sxs-lookup"><span data-stu-id="55dcc-123">Type: **[**D3DXMATRIX**](d3dxmatrix.md)\***</span></span>

<span data-ttu-id="55dcc-124">產生之 [**D3DXMATRIX**](../direct3d10/d3d10-d3dxmatrix.md)的指標。</span><span class="sxs-lookup"><span data-stu-id="55dcc-124">Pointer to the resulting [**D3DXMATRIX**](../direct3d10/d3d10-d3dxmatrix.md).</span></span>

## <a name="remarks"></a><span data-ttu-id="55dcc-125">備註</span><span class="sxs-lookup"><span data-stu-id="55dcc-125">Remarks</span></span>

<span data-ttu-id="55dcc-126">**D3DXMatrixOrthoRH** 函數的所有參數都是相機空間中的距離。</span><span class="sxs-lookup"><span data-stu-id="55dcc-126">All the parameters of the **D3DXMatrixOrthoRH** function are distances in camera space.</span></span> <span data-ttu-id="55dcc-127">參數描述視圖磁片區的維度。</span><span class="sxs-lookup"><span data-stu-id="55dcc-127">The parameters describe the dimensions of the view volume.</span></span>

<span data-ttu-id="55dcc-128">此函式的傳回值與 *不悅* 參數中所傳回的值相同。</span><span class="sxs-lookup"><span data-stu-id="55dcc-128">The return value for this function is the same value returned in the *pOut* parameter.</span></span> <span data-ttu-id="55dcc-129">如此一來， **D3DXMatrixOrthoRH** 函式就可以用來做為另一個函式的參數。</span><span class="sxs-lookup"><span data-stu-id="55dcc-129">In this way, the **D3DXMatrixOrthoRH** function can be used as a parameter for another function.</span></span>

<span data-ttu-id="55dcc-130">此函數會使用下列公式來計算傳回的矩陣。</span><span class="sxs-lookup"><span data-stu-id="55dcc-130">This function uses the following formula to compute the returned matrix.</span></span>


```
2/w  0    0           0
0    2/h  0           0
0    0    1/(zn-zf)   0
0    0    zn/(zn-zf)  1
```



## <a name="requirements"></a><span data-ttu-id="55dcc-131">規格需求</span><span class="sxs-lookup"><span data-stu-id="55dcc-131">Requirements</span></span>



| <span data-ttu-id="55dcc-132">需求</span><span class="sxs-lookup"><span data-stu-id="55dcc-132">Requirement</span></span> | <span data-ttu-id="55dcc-133">值</span><span class="sxs-lookup"><span data-stu-id="55dcc-133">Value</span></span> |
|--------------------|----------------------------------------------------------------------------------------|
| <span data-ttu-id="55dcc-134">標頭</span><span class="sxs-lookup"><span data-stu-id="55dcc-134">Header</span></span><br/>  | <dl> <span data-ttu-id="55dcc-135"><dt>D3dx9math。h</dt></span><span class="sxs-lookup"><span data-stu-id="55dcc-135"><dt>D3dx9math.h</dt></span></span> </dl> |
| <span data-ttu-id="55dcc-136">程式庫</span><span class="sxs-lookup"><span data-stu-id="55dcc-136">Library</span></span><br/> | <dl> <span data-ttu-id="55dcc-137"><dt>D3dx9 .lib</dt></span><span class="sxs-lookup"><span data-stu-id="55dcc-137"><dt>D3dx9.lib</dt></span></span> </dl>   |



## <a name="see-also"></a><span data-ttu-id="55dcc-138">另請參閱</span><span class="sxs-lookup"><span data-stu-id="55dcc-138">See also</span></span>

<dl> <dt>

[<span data-ttu-id="55dcc-139">數學函數</span><span class="sxs-lookup"><span data-stu-id="55dcc-139">Math Functions</span></span>](dx9-graphics-reference-d3dx-functions-math.md)
</dt> <dt>

[<span data-ttu-id="55dcc-140">**D3DXMatrixOrthoLH**</span><span class="sxs-lookup"><span data-stu-id="55dcc-140">**D3DXMatrixOrthoLH**</span></span>](d3dxmatrixortholh.md)
</dt> <dt>

[<span data-ttu-id="55dcc-141">**D3DXMatrixOrthoOffCenterRH**</span><span class="sxs-lookup"><span data-stu-id="55dcc-141">**D3DXMatrixOrthoOffCenterRH**</span></span>](d3dxmatrixorthooffcenterrh.md)
</dt> <dt>

[<span data-ttu-id="55dcc-142">**D3DXMatrixOrthoOffCenterLH**</span><span class="sxs-lookup"><span data-stu-id="55dcc-142">**D3DXMatrixOrthoOffCenterLH**</span></span>](d3dxmatrixorthooffcenterlh.md)
</dt> </dl>

 

 
