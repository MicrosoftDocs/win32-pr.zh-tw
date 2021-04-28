---
description: D3DXMatrixPerspectiveFovRH 函式 (D3dx9math) -根據視圖的欄位建立右手的透視圖投影矩陣。
ms.assetid: 3f4bc5d8-90af-4fdc-bc0c-931407cd7a9b
title: 'D3DXMatrixPerspectiveFovRH 函式 (D3dx9math) '
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
- d3dx9.lib
- d3dx9.dll
ms.openlocfilehash: e8860a5d9fed13e8acdedfe67ed94a97911a6de0
ms.sourcegitcommit: 95685061d5b0333bbf9e6ebd208dde8190f97005
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 04/28/2021
ms.locfileid: "108118326"
---
# <a name="d3dxmatrixperspectivefovrh-function-d3dx9mathh"></a><span data-ttu-id="c2ea2-103">D3DXMatrixPerspectiveFovRH 函式 (D3dx9math) </span><span class="sxs-lookup"><span data-stu-id="c2ea2-103">D3DXMatrixPerspectiveFovRH function (D3dx9math.h)</span></span>

<span data-ttu-id="c2ea2-104">根據視野範圍建置右手透視投影矩陣。</span><span class="sxs-lookup"><span data-stu-id="c2ea2-104">Builds a right-handed perspective projection matrix based on a field of view.</span></span>

## <a name="syntax"></a><span data-ttu-id="c2ea2-105">語法</span><span class="sxs-lookup"><span data-stu-id="c2ea2-105">Syntax</span></span>


```C++
D3DXMATRIX* D3DXMatrixPerspectiveFovRH(
  _Inout_ D3DXMATRIX *pOut,
  _In_    FLOAT      fovy,
  _In_    FLOAT      Aspect,
  _In_    FLOAT      zn,
  _In_    FLOAT      zf
);
```



## <a name="parameters"></a><span data-ttu-id="c2ea2-106">參數</span><span class="sxs-lookup"><span data-stu-id="c2ea2-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="c2ea2-107">*不悅* \[in、out\]</span><span class="sxs-lookup"><span data-stu-id="c2ea2-107">*pOut* \[in, out\]</span></span>
</dt> <dd>

<span data-ttu-id="c2ea2-108">類型： **[ **D3DXMATRIX**](d3dxmatrix.md)\***</span><span class="sxs-lookup"><span data-stu-id="c2ea2-108">Type: **[**D3DXMATRIX**](d3dxmatrix.md)\***</span></span>

<span data-ttu-id="c2ea2-109">[**D3DXMATRIX**](d3dxmatrix.md)結構的指標，此結構是作業的結果。</span><span class="sxs-lookup"><span data-stu-id="c2ea2-109">Pointer to the [**D3DXMATRIX**](d3dxmatrix.md) structure that is the result of the operation.</span></span>

</dd> <dt>

<span data-ttu-id="c2ea2-110">*fovy* \[在\]</span><span class="sxs-lookup"><span data-stu-id="c2ea2-110">*fovy* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="c2ea2-111">類型： **[ **FLOAT**](../winprog/windows-data-types.md)**</span><span class="sxs-lookup"><span data-stu-id="c2ea2-111">Type: **[**FLOAT**](../winprog/windows-data-types.md)**</span></span>

<span data-ttu-id="c2ea2-112">Y 方向的視圖欄位，以弧度為單位。</span><span class="sxs-lookup"><span data-stu-id="c2ea2-112">Field of view in the y direction, in radians.</span></span>

</dd> <dt>

<span data-ttu-id="c2ea2-113">*外觀* \[在\]</span><span class="sxs-lookup"><span data-stu-id="c2ea2-113">*Aspect* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="c2ea2-114">類型： **[ **FLOAT**](../winprog/windows-data-types.md)**</span><span class="sxs-lookup"><span data-stu-id="c2ea2-114">Type: **[**FLOAT**](../winprog/windows-data-types.md)**</span></span>

<span data-ttu-id="c2ea2-115">外觀比例，定義為視圖空間寬度除以高度。</span><span class="sxs-lookup"><span data-stu-id="c2ea2-115">Aspect ratio, defined as view space width divided by height.</span></span>

</dd> <dt>

<span data-ttu-id="c2ea2-116">*zn* \[在\]</span><span class="sxs-lookup"><span data-stu-id="c2ea2-116">*zn* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="c2ea2-117">類型： **[ **FLOAT**](../winprog/windows-data-types.md)**</span><span class="sxs-lookup"><span data-stu-id="c2ea2-117">Type: **[**FLOAT**](../winprog/windows-data-types.md)**</span></span>

<span data-ttu-id="c2ea2-118">接近視圖平面的 Z 值。</span><span class="sxs-lookup"><span data-stu-id="c2ea2-118">Z-value of the near view-plane.</span></span>

</dd> <dt>

<span data-ttu-id="c2ea2-119">*zf* \[在\]</span><span class="sxs-lookup"><span data-stu-id="c2ea2-119">*zf* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="c2ea2-120">類型： **[ **FLOAT**](../winprog/windows-data-types.md)**</span><span class="sxs-lookup"><span data-stu-id="c2ea2-120">Type: **[**FLOAT**](../winprog/windows-data-types.md)**</span></span>

<span data-ttu-id="c2ea2-121">最遠的視圖平面的 Z 值。</span><span class="sxs-lookup"><span data-stu-id="c2ea2-121">Z-value of the far view-plane.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="c2ea2-122">傳回值</span><span class="sxs-lookup"><span data-stu-id="c2ea2-122">Return value</span></span>

<span data-ttu-id="c2ea2-123">類型： **[ **D3DXMATRIX**](d3dxmatrix.md)\***</span><span class="sxs-lookup"><span data-stu-id="c2ea2-123">Type: **[**D3DXMATRIX**](d3dxmatrix.md)\***</span></span>

<span data-ttu-id="c2ea2-124">[**D3DXMATRIX**](d3dxmatrix.md)結構的指標，此結構是右手向的透視圖投影矩陣。</span><span class="sxs-lookup"><span data-stu-id="c2ea2-124">Pointer to a [**D3DXMATRIX**](d3dxmatrix.md) structure that is a right-handed perspective projection matrix.</span></span>

## <a name="remarks"></a><span data-ttu-id="c2ea2-125">備註</span><span class="sxs-lookup"><span data-stu-id="c2ea2-125">Remarks</span></span>

<span data-ttu-id="c2ea2-126">此函式的傳回值與 *不悅* 參數中所傳回的值相同。</span><span class="sxs-lookup"><span data-stu-id="c2ea2-126">The return value for this function is the same value returned in the *pOut* parameter.</span></span> <span data-ttu-id="c2ea2-127">如此一來， **D3DXMatrixPerspectiveFovRH** 函式就可以用來做為另一個函式的參數。</span><span class="sxs-lookup"><span data-stu-id="c2ea2-127">In this way, the **D3DXMatrixPerspectiveFovRH** function can be used as a parameter for another function.</span></span>

<span data-ttu-id="c2ea2-128">若要變更外觀比例軸，請使用計算公式： fovy = 2 \* math. atan (數學. tan (fovy \* 0.5) /外觀) 。</span><span class="sxs-lookup"><span data-stu-id="c2ea2-128">To change the aspect ratio axis, use the calculation formula: fovy = 2 \* math.atan(math.tan(fovy \* 0.5) / aspect).</span></span> <span data-ttu-id="c2ea2-129">或者，在結構中加入 X 和 Y 外觀比例變數以調整垂直視圖空間： fovy = 2 \* math. atan (math. tan (fovy \* 0.5) /aspectY) ，外觀 = aspectX \* 外觀 Y。</span><span class="sxs-lookup"><span data-stu-id="c2ea2-129">Alternatively, add X and Y aspect ratio variables in the structure to scale the vertical view space: fovy = 2 \* math.atan(math.tan(fovy \* 0.5) / aspectY), aspect = aspectX \* aspect Y.</span></span>

<span data-ttu-id="c2ea2-130">此函數會計算傳回的矩陣，如下所示。</span><span class="sxs-lookup"><span data-stu-id="c2ea2-130">This function computes the returned matrix as shown.</span></span>


```
xScale     0          0              0
0        yScale       0              0
0        0        zf/(zn-zf)        -1
0        0        zn*zf/(zn-zf)      0
where:
yScale = cot(fovY/2)
    
xScale = yScale / aspect ratio
```



## <a name="requirements"></a><span data-ttu-id="c2ea2-131">規格需求</span><span class="sxs-lookup"><span data-stu-id="c2ea2-131">Requirements</span></span>



| <span data-ttu-id="c2ea2-132">需求</span><span class="sxs-lookup"><span data-stu-id="c2ea2-132">Requirement</span></span> | <span data-ttu-id="c2ea2-133">值</span><span class="sxs-lookup"><span data-stu-id="c2ea2-133">Value</span></span> |
|--------------------|----------------------------------------------------------------------------------------|
| <span data-ttu-id="c2ea2-134">標頭</span><span class="sxs-lookup"><span data-stu-id="c2ea2-134">Header</span></span><br/>  | <dl> <span data-ttu-id="c2ea2-135"><dt>D3dx9math。h</dt></span><span class="sxs-lookup"><span data-stu-id="c2ea2-135"><dt>D3dx9math.h</dt></span></span> </dl> |
| <span data-ttu-id="c2ea2-136">程式庫</span><span class="sxs-lookup"><span data-stu-id="c2ea2-136">Library</span></span><br/> | <dl> <span data-ttu-id="c2ea2-137"><dt>D3dx9 .lib</dt></span><span class="sxs-lookup"><span data-stu-id="c2ea2-137"><dt>D3dx9.lib</dt></span></span> </dl>   |



## <a name="see-also"></a><span data-ttu-id="c2ea2-138">另請參閱</span><span class="sxs-lookup"><span data-stu-id="c2ea2-138">See also</span></span>

<dl> <dt>

[<span data-ttu-id="c2ea2-139">數學函數</span><span class="sxs-lookup"><span data-stu-id="c2ea2-139">Math Functions</span></span>](dx9-graphics-reference-d3dx-functions-math.md)
</dt> <dt>

[<span data-ttu-id="c2ea2-140">**D3DXMatrixPerspectiveRH**</span><span class="sxs-lookup"><span data-stu-id="c2ea2-140">**D3DXMatrixPerspectiveRH**</span></span>](d3dxmatrixperspectiverh.md)
</dt> <dt>

[<span data-ttu-id="c2ea2-141">**D3DXMatrixPerspectiveLH**</span><span class="sxs-lookup"><span data-stu-id="c2ea2-141">**D3DXMatrixPerspectiveLH**</span></span>](d3dxmatrixperspectivelh.md)
</dt> <dt>

[<span data-ttu-id="c2ea2-142">**D3DXMatrixPerspectiveFovLH**</span><span class="sxs-lookup"><span data-stu-id="c2ea2-142">**D3DXMatrixPerspectiveFovLH**</span></span>](d3dxmatrixperspectivefovlh.md)
</dt> <dt>

[<span data-ttu-id="c2ea2-143">**D3DXMatrixPerspectiveOffCenterRH**</span><span class="sxs-lookup"><span data-stu-id="c2ea2-143">**D3DXMatrixPerspectiveOffCenterRH**</span></span>](d3dxmatrixperspectiveoffcenterrh.md)
</dt> <dt>

[<span data-ttu-id="c2ea2-144">**D3DXMatrixPerspectiveOffCenterLH**</span><span class="sxs-lookup"><span data-stu-id="c2ea2-144">**D3DXMatrixPerspectiveOffCenterLH**</span></span>](d3dxmatrixperspectiveoffcenterlh.md)
</dt> </dl>

 

 
