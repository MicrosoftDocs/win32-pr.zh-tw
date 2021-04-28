---
description: D3DXMatrixPerspectiveRH 函式 (D3dx9math) -建立右手角的透視圖投影矩陣。
ms.assetid: dd9b041b-922b-43df-a6e9-46c97204338a
title: 'D3DXMatrixPerspectiveRH 函式 (D3dx9math) '
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- D3DXMatrixPerspectiveRH
api_type:
- LibDef
api_location:
- d3dx9.lib
- d3dx9.dll
ms.openlocfilehash: 3c583b74366a0a00054bbeced1ece2bd3d1c1cd2
ms.sourcegitcommit: 95685061d5b0333bbf9e6ebd208dde8190f97005
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 04/28/2021
ms.locfileid: "108118236"
---
# <a name="d3dxmatrixperspectiverh-function-d3dx9mathh"></a><span data-ttu-id="41263-103">D3DXMatrixPerspectiveRH 函式 (D3dx9math) </span><span class="sxs-lookup"><span data-stu-id="41263-103">D3DXMatrixPerspectiveRH function (D3dx9math.h)</span></span>

<span data-ttu-id="41263-104">建置右手透視投影矩陣。</span><span class="sxs-lookup"><span data-stu-id="41263-104">Builds a right-handed perspective projection matrix.</span></span>

## <a name="syntax"></a><span data-ttu-id="41263-105">語法</span><span class="sxs-lookup"><span data-stu-id="41263-105">Syntax</span></span>


```C++
D3DXMATRIX* D3DXMatrixPerspectiveRH(
  _Inout_ D3DXMATRIX *pOut,
  _In_    FLOAT      w,
  _In_    FLOAT      h,
  _In_    FLOAT      zn,
  _In_    FLOAT      zf
);
```



## <a name="parameters"></a><span data-ttu-id="41263-106">參數</span><span class="sxs-lookup"><span data-stu-id="41263-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="41263-107">*不悅* \[in、out\]</span><span class="sxs-lookup"><span data-stu-id="41263-107">*pOut* \[in, out\]</span></span>
</dt> <dd>

<span data-ttu-id="41263-108">類型： **[ **D3DXMATRIX**](d3dxmatrix.md)\***</span><span class="sxs-lookup"><span data-stu-id="41263-108">Type: **[**D3DXMATRIX**](d3dxmatrix.md)\***</span></span>

<span data-ttu-id="41263-109">[**D3DXMATRIX**](d3dxmatrix.md)結構的指標，此結構是作業的結果。</span><span class="sxs-lookup"><span data-stu-id="41263-109">Pointer to the [**D3DXMATRIX**](d3dxmatrix.md) structure that is the result of the operation.</span></span>

</dd> <dt>

<span data-ttu-id="41263-110">*w* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="41263-110">*w* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="41263-111">類型： **[ **FLOAT**](../winprog/windows-data-types.md)**</span><span class="sxs-lookup"><span data-stu-id="41263-111">Type: **[**FLOAT**](../winprog/windows-data-types.md)**</span></span>

<span data-ttu-id="41263-112">接近 view 平面的視圖音量寬度。</span><span class="sxs-lookup"><span data-stu-id="41263-112">Width of the view volume at the near view-plane.</span></span>

</dd> <dt>

<span data-ttu-id="41263-113">*h* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="41263-113">*h* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="41263-114">類型： **[ **FLOAT**](../winprog/windows-data-types.md)**</span><span class="sxs-lookup"><span data-stu-id="41263-114">Type: **[**FLOAT**](../winprog/windows-data-types.md)**</span></span>

<span data-ttu-id="41263-115">接近 view 平面的視圖音量高度。</span><span class="sxs-lookup"><span data-stu-id="41263-115">Height of the view volume at the near view-plane.</span></span>

</dd> <dt>

<span data-ttu-id="41263-116">*zn* \[在\]</span><span class="sxs-lookup"><span data-stu-id="41263-116">*zn* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="41263-117">類型： **[ **FLOAT**](../winprog/windows-data-types.md)**</span><span class="sxs-lookup"><span data-stu-id="41263-117">Type: **[**FLOAT**](../winprog/windows-data-types.md)**</span></span>

<span data-ttu-id="41263-118">接近視圖平面的 Z 值。</span><span class="sxs-lookup"><span data-stu-id="41263-118">Z-value of the near view-plane.</span></span>

</dd> <dt>

<span data-ttu-id="41263-119">*zf* \[在\]</span><span class="sxs-lookup"><span data-stu-id="41263-119">*zf* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="41263-120">類型： **[ **FLOAT**](../winprog/windows-data-types.md)**</span><span class="sxs-lookup"><span data-stu-id="41263-120">Type: **[**FLOAT**](../winprog/windows-data-types.md)**</span></span>

<span data-ttu-id="41263-121">最遠的視圖平面的 Z 值。</span><span class="sxs-lookup"><span data-stu-id="41263-121">Z-value of the far view-plane.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="41263-122">傳回值</span><span class="sxs-lookup"><span data-stu-id="41263-122">Return value</span></span>

<span data-ttu-id="41263-123">類型： **[ **D3DXMATRIX**](d3dxmatrix.md)\***</span><span class="sxs-lookup"><span data-stu-id="41263-123">Type: **[**D3DXMATRIX**](d3dxmatrix.md)\***</span></span>

<span data-ttu-id="41263-124">[**D3DXMATRIX**](d3dxmatrix.md)結構的指標，此結構是右手向的透視圖投影矩陣。</span><span class="sxs-lookup"><span data-stu-id="41263-124">Pointer to a [**D3DXMATRIX**](d3dxmatrix.md) structure that is a right-handed perspective projection matrix.</span></span>

## <a name="remarks"></a><span data-ttu-id="41263-125">備註</span><span class="sxs-lookup"><span data-stu-id="41263-125">Remarks</span></span>

<span data-ttu-id="41263-126">**D3DXMatrixPerspectiveRH** 函數的所有參數都是相機空間中的距離。</span><span class="sxs-lookup"><span data-stu-id="41263-126">All the parameters of the **D3DXMatrixPerspectiveRH** function are distances in camera space.</span></span> <span data-ttu-id="41263-127">參數描述視圖磁片區的維度。</span><span class="sxs-lookup"><span data-stu-id="41263-127">The parameters describe the dimensions of the view volume.</span></span>

<span data-ttu-id="41263-128">此函式的傳回值與 *不悅* 參數中所傳回的值相同。</span><span class="sxs-lookup"><span data-stu-id="41263-128">The return value for this function is the same value returned in the *pOut* parameter.</span></span> <span data-ttu-id="41263-129">如此一來， **D3DXMatrixPerspectiveRH** 函式就可以用來做為另一個函式的參數。</span><span class="sxs-lookup"><span data-stu-id="41263-129">In this way, the **D3DXMatrixPerspectiveRH** function can be used as a parameter for another function.</span></span>

<span data-ttu-id="41263-130">此函數會使用下列公式來計算傳回的矩陣。</span><span class="sxs-lookup"><span data-stu-id="41263-130">This function uses the following formula to compute the returned matrix.</span></span>


```
2*zn/w  0       0              0
0       2*zn/h  0              0
0       0       zf/(zn-zf)    -1
0       0       zn*zf/(zn-zf)  0
```



## <a name="requirements"></a><span data-ttu-id="41263-131">規格需求</span><span class="sxs-lookup"><span data-stu-id="41263-131">Requirements</span></span>



| <span data-ttu-id="41263-132">需求</span><span class="sxs-lookup"><span data-stu-id="41263-132">Requirement</span></span> | <span data-ttu-id="41263-133">值</span><span class="sxs-lookup"><span data-stu-id="41263-133">Value</span></span> |
|--------------------|----------------------------------------------------------------------------------------|
| <span data-ttu-id="41263-134">標頭</span><span class="sxs-lookup"><span data-stu-id="41263-134">Header</span></span><br/>  | <dl> <span data-ttu-id="41263-135"><dt>D3dx9math。h</dt></span><span class="sxs-lookup"><span data-stu-id="41263-135"><dt>D3dx9math.h</dt></span></span> </dl> |
| <span data-ttu-id="41263-136">程式庫</span><span class="sxs-lookup"><span data-stu-id="41263-136">Library</span></span><br/> | <dl> <span data-ttu-id="41263-137"><dt>D3dx9 .lib</dt></span><span class="sxs-lookup"><span data-stu-id="41263-137"><dt>D3dx9.lib</dt></span></span> </dl>   |



## <a name="see-also"></a><span data-ttu-id="41263-138">另請參閱</span><span class="sxs-lookup"><span data-stu-id="41263-138">See also</span></span>

<dl> <dt>

[<span data-ttu-id="41263-139">數學函數</span><span class="sxs-lookup"><span data-stu-id="41263-139">Math Functions</span></span>](dx9-graphics-reference-d3dx-functions-math.md)
</dt> <dt>

[<span data-ttu-id="41263-140">**D3DXMatrixPerspectiveLH**</span><span class="sxs-lookup"><span data-stu-id="41263-140">**D3DXMatrixPerspectiveLH**</span></span>](d3dxmatrixperspectivelh.md)
</dt> <dt>

[<span data-ttu-id="41263-141">**D3DXMatrixPerspectiveFovRH**</span><span class="sxs-lookup"><span data-stu-id="41263-141">**D3DXMatrixPerspectiveFovRH**</span></span>](d3dxmatrixperspectivefovrh.md)
</dt> <dt>

[<span data-ttu-id="41263-142">**D3DXMatrixPerspectiveFovLH**</span><span class="sxs-lookup"><span data-stu-id="41263-142">**D3DXMatrixPerspectiveFovLH**</span></span>](d3dxmatrixperspectivefovlh.md)
</dt> <dt>

[<span data-ttu-id="41263-143">**D3DXMatrixPerspectiveOffCenterRH**</span><span class="sxs-lookup"><span data-stu-id="41263-143">**D3DXMatrixPerspectiveOffCenterRH**</span></span>](d3dxmatrixperspectiveoffcenterrh.md)
</dt> <dt>

[<span data-ttu-id="41263-144">**D3DXMatrixPerspectiveOffCenterLH**</span><span class="sxs-lookup"><span data-stu-id="41263-144">**D3DXMatrixPerspectiveOffCenterLH**</span></span>](d3dxmatrixperspectiveoffcenterlh.md)
</dt> </dl>

 

 
