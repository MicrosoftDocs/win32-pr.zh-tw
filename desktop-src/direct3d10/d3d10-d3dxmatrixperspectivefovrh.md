---
description: 根據視野範圍建置右手透視投影矩陣。
ms.assetid: a75e6666-e6c0-4a54-bc88-835fa012542f
title: 'D3DXMatrixPerspectiveFovRH 函式 (D3DX10Math) '
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- D3DXMatrixPerspectiveFovRH
api_type:
- LibDef
api_location:
- D3DX10.lib
- D3DX10.dll
ms.openlocfilehash: baad02b5840af8e244cd562def4aeb8f9ac2988a
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 03/15/2021
ms.locfileid: "103946176"
---
# <a name="d3dxmatrixperspectivefovrh-function-d3dx10mathh"></a><span data-ttu-id="28ba1-103">D3DXMatrixPerspectiveFovRH 函式 (D3DX10Math) </span><span class="sxs-lookup"><span data-stu-id="28ba1-103">D3DXMatrixPerspectiveFovRH function (D3DX10Math.h)</span></span>

<span data-ttu-id="28ba1-104">根據視野範圍建置右手透視投影矩陣。</span><span class="sxs-lookup"><span data-stu-id="28ba1-104">Builds a right-handed perspective projection matrix based on a field of view.</span></span>

## <a name="syntax"></a><span data-ttu-id="28ba1-105">語法</span><span class="sxs-lookup"><span data-stu-id="28ba1-105">Syntax</span></span>


```C++
D3DXMATRIX* D3DXMatrixPerspectiveFovRH(
  _Inout_ D3DXMATRIX *pOut,
  _In_    FLOAT      fovy,
  _In_    FLOAT      Aspect,
  _In_    FLOAT      zn,
  _In_    FLOAT      zf
);
```



## <a name="parameters"></a><span data-ttu-id="28ba1-106">參數</span><span class="sxs-lookup"><span data-stu-id="28ba1-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="28ba1-107">*不悅* \[in、out\]</span><span class="sxs-lookup"><span data-stu-id="28ba1-107">*pOut* \[in, out\]</span></span>
</dt> <dd>

<span data-ttu-id="28ba1-108">類型： **[ **D3DXMATRIX**](../direct3d9/d3dxmatrix.md)\***</span><span class="sxs-lookup"><span data-stu-id="28ba1-108">Type: **[**D3DXMATRIX**](../direct3d9/d3dxmatrix.md)\***</span></span>

<span data-ttu-id="28ba1-109">[**D3DXMATRIX**](d3d10-d3dxmatrix.md)結構的指標，此結構是作業的結果。</span><span class="sxs-lookup"><span data-stu-id="28ba1-109">Pointer to the [**D3DXMATRIX**](d3d10-d3dxmatrix.md) structure that is the result of the operation.</span></span>

</dd> <dt>

<span data-ttu-id="28ba1-110">*fovy* \[在\]</span><span class="sxs-lookup"><span data-stu-id="28ba1-110">*fovy* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="28ba1-111">類型： **[ **FLOAT**](../winprog/windows-data-types.md)**</span><span class="sxs-lookup"><span data-stu-id="28ba1-111">Type: **[**FLOAT**](../winprog/windows-data-types.md)**</span></span>

<span data-ttu-id="28ba1-112">Y 方向的視圖欄位，以弧度為單位。</span><span class="sxs-lookup"><span data-stu-id="28ba1-112">Field of view in the y direction, in radians.</span></span>

</dd> <dt>

<span data-ttu-id="28ba1-113">*外觀* \[在\]</span><span class="sxs-lookup"><span data-stu-id="28ba1-113">*Aspect* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="28ba1-114">類型： **[ **FLOAT**](../winprog/windows-data-types.md)**</span><span class="sxs-lookup"><span data-stu-id="28ba1-114">Type: **[**FLOAT**](../winprog/windows-data-types.md)**</span></span>

<span data-ttu-id="28ba1-115">外觀比例，定義為視圖空間寬度除以高度。</span><span class="sxs-lookup"><span data-stu-id="28ba1-115">Aspect ratio, defined as view space width divided by height.</span></span>

</dd> <dt>

<span data-ttu-id="28ba1-116">*zn* \[在\]</span><span class="sxs-lookup"><span data-stu-id="28ba1-116">*zn* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="28ba1-117">類型： **[ **FLOAT**](../winprog/windows-data-types.md)**</span><span class="sxs-lookup"><span data-stu-id="28ba1-117">Type: **[**FLOAT**](../winprog/windows-data-types.md)**</span></span>

<span data-ttu-id="28ba1-118">接近視圖平面的 Z 值。</span><span class="sxs-lookup"><span data-stu-id="28ba1-118">Z-value of the near view-plane.</span></span>

</dd> <dt>

<span data-ttu-id="28ba1-119">*zf* \[在\]</span><span class="sxs-lookup"><span data-stu-id="28ba1-119">*zf* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="28ba1-120">類型： **[ **FLOAT**](../winprog/windows-data-types.md)**</span><span class="sxs-lookup"><span data-stu-id="28ba1-120">Type: **[**FLOAT**](../winprog/windows-data-types.md)**</span></span>

<span data-ttu-id="28ba1-121">最遠的視圖平面的 Z 值。</span><span class="sxs-lookup"><span data-stu-id="28ba1-121">Z-value of the far view-plane.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="28ba1-122">傳回值</span><span class="sxs-lookup"><span data-stu-id="28ba1-122">Return value</span></span>

<span data-ttu-id="28ba1-123">類型： **[ **D3DXMATRIX**](../direct3d9/d3dxmatrix.md)\***</span><span class="sxs-lookup"><span data-stu-id="28ba1-123">Type: **[**D3DXMATRIX**](../direct3d9/d3dxmatrix.md)\***</span></span>

<span data-ttu-id="28ba1-124">D3DXMATRIX 結構的指標，此結構是右手向的透視圖投影矩陣。</span><span class="sxs-lookup"><span data-stu-id="28ba1-124">Pointer to a D3DXMATRIX structure that is a right-handed perspective projection matrix.</span></span>

## <a name="remarks"></a><span data-ttu-id="28ba1-125">備註</span><span class="sxs-lookup"><span data-stu-id="28ba1-125">Remarks</span></span>

<span data-ttu-id="28ba1-126">此函式的傳回值與不悅參數中所傳回的值相同。</span><span class="sxs-lookup"><span data-stu-id="28ba1-126">The return value for this function is the same value returned in the pOut parameter.</span></span> <span data-ttu-id="28ba1-127">如此一來，D3DXMatrixPerspectiveFovRH 函式就可以用來做為另一個函式的參數。</span><span class="sxs-lookup"><span data-stu-id="28ba1-127">In this way, the D3DXMatrixPerspectiveFovRH function can be used as a parameter for another function.</span></span>

<span data-ttu-id="28ba1-128">此函數會計算傳回的矩陣，如下所示。</span><span class="sxs-lookup"><span data-stu-id="28ba1-128">This function computes the returned matrix as shown.</span></span>


```
xScale     0          0              0
0        yScale       0              0
0          0      zf/(zn-zf)        -1
0          0      zn*zf/(zn-zf)      0
where:
yScale = cot(fovY/2)
    
xScale = yScale / aspect ratio
```



## <a name="requirements"></a><span data-ttu-id="28ba1-129">規格需求</span><span class="sxs-lookup"><span data-stu-id="28ba1-129">Requirements</span></span>



| <span data-ttu-id="28ba1-130">需求</span><span class="sxs-lookup"><span data-stu-id="28ba1-130">Requirement</span></span> | <span data-ttu-id="28ba1-131">值</span><span class="sxs-lookup"><span data-stu-id="28ba1-131">Value</span></span> |
|--------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="28ba1-132">標頭</span><span class="sxs-lookup"><span data-stu-id="28ba1-132">Header</span></span><br/>  | <dl> <span data-ttu-id="28ba1-133"><dt>D3DX10Math。h</dt></span><span class="sxs-lookup"><span data-stu-id="28ba1-133"><dt>D3DX10Math.h</dt></span></span> </dl> |
| <span data-ttu-id="28ba1-134">程式庫</span><span class="sxs-lookup"><span data-stu-id="28ba1-134">Library</span></span><br/> | <dl> <span data-ttu-id="28ba1-135"><dt>D3DX10 .lib</dt></span><span class="sxs-lookup"><span data-stu-id="28ba1-135"><dt>D3DX10.lib</dt></span></span> </dl>   |



## <a name="see-also"></a><span data-ttu-id="28ba1-136">另請參閱</span><span class="sxs-lookup"><span data-stu-id="28ba1-136">See also</span></span>

<dl> <dt>

[<span data-ttu-id="28ba1-137">數學函數</span><span class="sxs-lookup"><span data-stu-id="28ba1-137">Math Functions</span></span>](d3d10-graphics-reference-d3dx10-functions-math.md)
</dt> </dl>

 

 
