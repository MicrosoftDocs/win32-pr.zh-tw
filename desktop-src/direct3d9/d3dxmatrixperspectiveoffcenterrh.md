---
description: D3DXMatrixPerspectiveOffCenterRH 函式 (D3dx9math) -建立自訂、右手的透視圖投影矩陣。
ms.assetid: e6826e46-fc80-41fa-b0d8-45b6797df76f
title: 'D3DXMatrixPerspectiveOffCenterRH 函式 (D3dx9math) '
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- D3DXMatrixPerspectiveOffCenterRH
api_type:
- LibDef
api_location:
- d3dx9.lib
- d3dx9.dll
ms.openlocfilehash: 3d051894a6706cf8d58b81a85003666513f2a956
ms.sourcegitcommit: 95685061d5b0333bbf9e6ebd208dde8190f97005
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 04/28/2021
ms.locfileid: "108118276"
---
# <a name="d3dxmatrixperspectiveoffcenterrh-function-d3dx9mathh"></a><span data-ttu-id="fa330-103">D3DXMatrixPerspectiveOffCenterRH 函式 (D3dx9math) </span><span class="sxs-lookup"><span data-stu-id="fa330-103">D3DXMatrixPerspectiveOffCenterRH function (D3dx9math.h)</span></span>

<span data-ttu-id="fa330-104">建立自訂、右手右手的透視圖投影矩陣。</span><span class="sxs-lookup"><span data-stu-id="fa330-104">Builds a customized, right-handed perspective projection matrix.</span></span>

## <a name="syntax"></a><span data-ttu-id="fa330-105">語法</span><span class="sxs-lookup"><span data-stu-id="fa330-105">Syntax</span></span>


```C++
D3DXMATRIX* D3DXMatrixPerspectiveOffCenterRH(
  _Inout_ D3DXMATRIX *pOut,
  _In_    FLOAT      l,
  _In_    FLOAT      r,
  _In_    FLOAT      b,
  _In_    FLOAT      t,
  _In_    FLOAT      zn,
  _In_    FLOAT      zf
);
```



## <a name="parameters"></a><span data-ttu-id="fa330-106">參數</span><span class="sxs-lookup"><span data-stu-id="fa330-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="fa330-107">*不悅* \[in、out\]</span><span class="sxs-lookup"><span data-stu-id="fa330-107">*pOut* \[in, out\]</span></span>
</dt> <dd>

<span data-ttu-id="fa330-108">類型： **[ **D3DXMATRIX**](d3dxmatrix.md)\***</span><span class="sxs-lookup"><span data-stu-id="fa330-108">Type: **[**D3DXMATRIX**](d3dxmatrix.md)\***</span></span>

<span data-ttu-id="fa330-109">[**D3DXMATRIX**](d3dxmatrix.md)結構的指標，此結構是作業的結果。</span><span class="sxs-lookup"><span data-stu-id="fa330-109">Pointer to the [**D3DXMATRIX**](d3dxmatrix.md) structure that is the result of the operation.</span></span>

</dd> <dt>

<span data-ttu-id="fa330-110">*l* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="fa330-110">*l* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="fa330-111">類型： **[ **FLOAT**](../winprog/windows-data-types.md)**</span><span class="sxs-lookup"><span data-stu-id="fa330-111">Type: **[**FLOAT**](../winprog/windows-data-types.md)**</span></span>

<span data-ttu-id="fa330-112">視圖音量的最小 x 值。</span><span class="sxs-lookup"><span data-stu-id="fa330-112">Minimum x-value of the view volume.</span></span>

</dd> <dt>

<span data-ttu-id="fa330-113">*r* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="fa330-113">*r* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="fa330-114">類型： **[ **FLOAT**](../winprog/windows-data-types.md)**</span><span class="sxs-lookup"><span data-stu-id="fa330-114">Type: **[**FLOAT**](../winprog/windows-data-types.md)**</span></span>

<span data-ttu-id="fa330-115">視圖音量的最大 x 值。</span><span class="sxs-lookup"><span data-stu-id="fa330-115">Maximum x-value of the view volume.</span></span>

</dd> <dt>

<span data-ttu-id="fa330-116">*b* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="fa330-116">*b* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="fa330-117">類型： **[ **FLOAT**](../winprog/windows-data-types.md)**</span><span class="sxs-lookup"><span data-stu-id="fa330-117">Type: **[**FLOAT**](../winprog/windows-data-types.md)**</span></span>

<span data-ttu-id="fa330-118">視圖音量的最小 y 值。</span><span class="sxs-lookup"><span data-stu-id="fa330-118">Minimum y-value of the view volume.</span></span>

</dd> <dt>

<span data-ttu-id="fa330-119"> \[ 中的 t\]</span><span class="sxs-lookup"><span data-stu-id="fa330-119">*t* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="fa330-120">類型： **[ **FLOAT**](../winprog/windows-data-types.md)**</span><span class="sxs-lookup"><span data-stu-id="fa330-120">Type: **[**FLOAT**](../winprog/windows-data-types.md)**</span></span>

<span data-ttu-id="fa330-121">視圖音量的最大 y 值。</span><span class="sxs-lookup"><span data-stu-id="fa330-121">Maximum y-value of the view volume.</span></span>

</dd> <dt>

<span data-ttu-id="fa330-122">*zn* \[在\]</span><span class="sxs-lookup"><span data-stu-id="fa330-122">*zn* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="fa330-123">類型： **[ **FLOAT**](../winprog/windows-data-types.md)**</span><span class="sxs-lookup"><span data-stu-id="fa330-123">Type: **[**FLOAT**](../winprog/windows-data-types.md)**</span></span>

<span data-ttu-id="fa330-124">視圖音量的最小 z 值。</span><span class="sxs-lookup"><span data-stu-id="fa330-124">Minimum z-value of the view volume.</span></span>

</dd> <dt>

<span data-ttu-id="fa330-125">*zf* \[在\]</span><span class="sxs-lookup"><span data-stu-id="fa330-125">*zf* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="fa330-126">類型： **[ **FLOAT**](../winprog/windows-data-types.md)**</span><span class="sxs-lookup"><span data-stu-id="fa330-126">Type: **[**FLOAT**](../winprog/windows-data-types.md)**</span></span>

<span data-ttu-id="fa330-127">視圖音量的最大 z 值。</span><span class="sxs-lookup"><span data-stu-id="fa330-127">Maximum z-value of the view volume.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="fa330-128">傳回值</span><span class="sxs-lookup"><span data-stu-id="fa330-128">Return value</span></span>

<span data-ttu-id="fa330-129">類型： **[ **D3DXMATRIX**](d3dxmatrix.md)\***</span><span class="sxs-lookup"><span data-stu-id="fa330-129">Type: **[**D3DXMATRIX**](d3dxmatrix.md)\***</span></span>

<span data-ttu-id="fa330-130">[**D3DXMATRIX**](d3dxmatrix.md)結構的指標，此結構是自訂、右手右手的透視圖投影矩陣。</span><span class="sxs-lookup"><span data-stu-id="fa330-130">Pointer to a [**D3DXMATRIX**](d3dxmatrix.md) structure that is a customized, right-handed perspective projection matrix.</span></span>

## <a name="remarks"></a><span data-ttu-id="fa330-131">備註</span><span class="sxs-lookup"><span data-stu-id="fa330-131">Remarks</span></span>

<span data-ttu-id="fa330-132">**D3DXMatrixPerspectiveOffCenterRH** 函數的所有參數都是相機空間中的距離。</span><span class="sxs-lookup"><span data-stu-id="fa330-132">All the parameters of the **D3DXMatrixPerspectiveOffCenterRH** function are distances in camera space.</span></span> <span data-ttu-id="fa330-133">參數描述視圖磁片區的維度。</span><span class="sxs-lookup"><span data-stu-id="fa330-133">The parameters describe the dimensions of the view volume.</span></span>

<span data-ttu-id="fa330-134">此函式的傳回值與 *不悅* 參數中所傳回的值相同。</span><span class="sxs-lookup"><span data-stu-id="fa330-134">The return value for this function is the same value returned in the *pOut* parameter.</span></span> <span data-ttu-id="fa330-135">如此一來， **D3DXMatrixPerspectiveOffCenterRH** 函式就可以用來做為另一個函式的參數。</span><span class="sxs-lookup"><span data-stu-id="fa330-135">In this way, the **D3DXMatrixPerspectiveOffCenterRH** function can be used as a parameter for another function.</span></span>

<span data-ttu-id="fa330-136">此函數會使用下列公式來計算傳回的矩陣。</span><span class="sxs-lookup"><span data-stu-id="fa330-136">This function uses the following formula to compute the returned matrix.</span></span>


```
2*zn/(r-l)   0            0                0
0            2*zn/(t-b)   0                0
(l+r)/(r-l)  (t+b)/(t-b)  zf/(zn-zf)      -1
0            0            zn*zf/(zn-zf)    0
```



## <a name="requirements"></a><span data-ttu-id="fa330-137">規格需求</span><span class="sxs-lookup"><span data-stu-id="fa330-137">Requirements</span></span>



| <span data-ttu-id="fa330-138">需求</span><span class="sxs-lookup"><span data-stu-id="fa330-138">Requirement</span></span> | <span data-ttu-id="fa330-139">值</span><span class="sxs-lookup"><span data-stu-id="fa330-139">Value</span></span> |
|--------------------|----------------------------------------------------------------------------------------|
| <span data-ttu-id="fa330-140">標頭</span><span class="sxs-lookup"><span data-stu-id="fa330-140">Header</span></span><br/>  | <dl> <span data-ttu-id="fa330-141"><dt>D3dx9math。h</dt></span><span class="sxs-lookup"><span data-stu-id="fa330-141"><dt>D3dx9math.h</dt></span></span> </dl> |
| <span data-ttu-id="fa330-142">程式庫</span><span class="sxs-lookup"><span data-stu-id="fa330-142">Library</span></span><br/> | <dl> <span data-ttu-id="fa330-143"><dt>D3dx9 .lib</dt></span><span class="sxs-lookup"><span data-stu-id="fa330-143"><dt>D3dx9.lib</dt></span></span> </dl>   |



## <a name="see-also"></a><span data-ttu-id="fa330-144">另請參閱</span><span class="sxs-lookup"><span data-stu-id="fa330-144">See also</span></span>

<dl> <dt>

[<span data-ttu-id="fa330-145">數學函數</span><span class="sxs-lookup"><span data-stu-id="fa330-145">Math Functions</span></span>](dx9-graphics-reference-d3dx-functions-math.md)
</dt> <dt>

[<span data-ttu-id="fa330-146">**D3DXMatrixPerspectiveRH**</span><span class="sxs-lookup"><span data-stu-id="fa330-146">**D3DXMatrixPerspectiveRH**</span></span>](d3dxmatrixperspectiverh.md)
</dt> <dt>

[<span data-ttu-id="fa330-147">**D3DXMatrixPerspectiveLH**</span><span class="sxs-lookup"><span data-stu-id="fa330-147">**D3DXMatrixPerspectiveLH**</span></span>](d3dxmatrixperspectivelh.md)
</dt> <dt>

[<span data-ttu-id="fa330-148">**D3DXMatrixPerspectiveFovRH**</span><span class="sxs-lookup"><span data-stu-id="fa330-148">**D3DXMatrixPerspectiveFovRH**</span></span>](d3dxmatrixperspectivefovrh.md)
</dt> <dt>

[<span data-ttu-id="fa330-149">**D3DXMatrixPerspectiveFovLH**</span><span class="sxs-lookup"><span data-stu-id="fa330-149">**D3DXMatrixPerspectiveFovLH**</span></span>](d3dxmatrixperspectivefovlh.md)
</dt> <dt>

[<span data-ttu-id="fa330-150">**D3DXMatrixPerspectiveOffCenterLH**</span><span class="sxs-lookup"><span data-stu-id="fa330-150">**D3DXMatrixPerspectiveOffCenterLH**</span></span>](d3dxmatrixperspectiveoffcenterlh.md)
</dt> </dl>

 

 
