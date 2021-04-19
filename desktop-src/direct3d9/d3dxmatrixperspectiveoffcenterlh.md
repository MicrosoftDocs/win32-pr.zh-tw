---
description: 建立自訂的左手向透視圖投影矩陣。
ms.assetid: de2732dd-a4f2-47bc-9509-de16f1ca85c2
title: 'D3DXMatrixPerspectiveOffCenterLH 函式 (D3dx9math) '
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- D3DXMatrixPerspectiveOffCenterLH
api_type:
- LibDef
api_location:
- d3dx9.lib
- d3dx9.dll
ms.openlocfilehash: 15743af16be84587fd8dc03e845ffcd8bd8dbc2b
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 03/15/2021
ms.locfileid: "106974835"
---
# <a name="d3dxmatrixperspectiveoffcenterlh-function-d3dx9mathh"></a><span data-ttu-id="69a3b-103">D3DXMatrixPerspectiveOffCenterLH 函式 (D3dx9math) </span><span class="sxs-lookup"><span data-stu-id="69a3b-103">D3DXMatrixPerspectiveOffCenterLH function (D3dx9math.h)</span></span>

<span data-ttu-id="69a3b-104">建立自訂的左手向透視圖投影矩陣。</span><span class="sxs-lookup"><span data-stu-id="69a3b-104">Builds a customized, left-handed perspective projection matrix.</span></span>

## <a name="syntax"></a><span data-ttu-id="69a3b-105">語法</span><span class="sxs-lookup"><span data-stu-id="69a3b-105">Syntax</span></span>


```C++
D3DXMATRIX* D3DXMatrixPerspectiveOffCenterLH(
  _Inout_ D3DXMATRIX *pOut,
  _In_    FLOAT      l,
  _In_    FLOAT      r,
  _In_    FLOAT      b,
  _In_    FLOAT      t,
  _In_    FLOAT      zn,
  _In_    FLOAT      zf
);
```



## <a name="parameters"></a><span data-ttu-id="69a3b-106">參數</span><span class="sxs-lookup"><span data-stu-id="69a3b-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="69a3b-107">*不悅* \[in、out\]</span><span class="sxs-lookup"><span data-stu-id="69a3b-107">*pOut* \[in, out\]</span></span>
</dt> <dd>

<span data-ttu-id="69a3b-108">類型： **[ **D3DXMATRIX**](d3dxmatrix.md)\***</span><span class="sxs-lookup"><span data-stu-id="69a3b-108">Type: **[**D3DXMATRIX**](d3dxmatrix.md)\***</span></span>

<span data-ttu-id="69a3b-109">[**D3DXMATRIX**](d3dxmatrix.md)結構的指標，此結構是作業的結果。</span><span class="sxs-lookup"><span data-stu-id="69a3b-109">Pointer to the [**D3DXMATRIX**](d3dxmatrix.md) structure that is the result of the operation.</span></span>

</dd> <dt>

<span data-ttu-id="69a3b-110">*l* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="69a3b-110">*l* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="69a3b-111">類型： **[ **FLOAT**](../winprog/windows-data-types.md)**</span><span class="sxs-lookup"><span data-stu-id="69a3b-111">Type: **[**FLOAT**](../winprog/windows-data-types.md)**</span></span>

<span data-ttu-id="69a3b-112">視圖音量的最小 x 值。</span><span class="sxs-lookup"><span data-stu-id="69a3b-112">Minimum x-value of the view volume.</span></span>

</dd> <dt>

<span data-ttu-id="69a3b-113">*r* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="69a3b-113">*r* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="69a3b-114">類型： **[ **FLOAT**](../winprog/windows-data-types.md)**</span><span class="sxs-lookup"><span data-stu-id="69a3b-114">Type: **[**FLOAT**](../winprog/windows-data-types.md)**</span></span>

<span data-ttu-id="69a3b-115">視圖音量的最大 x 值。</span><span class="sxs-lookup"><span data-stu-id="69a3b-115">Maximum x-value of the view volume.</span></span>

</dd> <dt>

<span data-ttu-id="69a3b-116">*b* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="69a3b-116">*b* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="69a3b-117">類型： **[ **FLOAT**](../winprog/windows-data-types.md)**</span><span class="sxs-lookup"><span data-stu-id="69a3b-117">Type: **[**FLOAT**](../winprog/windows-data-types.md)**</span></span>

<span data-ttu-id="69a3b-118">視圖音量的最小 y 值。</span><span class="sxs-lookup"><span data-stu-id="69a3b-118">Minimum y-value of the view volume.</span></span>

</dd> <dt>

<span data-ttu-id="69a3b-119"> \[ 中的 t\]</span><span class="sxs-lookup"><span data-stu-id="69a3b-119">*t* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="69a3b-120">類型： **[ **FLOAT**](../winprog/windows-data-types.md)**</span><span class="sxs-lookup"><span data-stu-id="69a3b-120">Type: **[**FLOAT**](../winprog/windows-data-types.md)**</span></span>

<span data-ttu-id="69a3b-121">視圖音量的最大 y 值。</span><span class="sxs-lookup"><span data-stu-id="69a3b-121">Maximum y-value of the view volume.</span></span>

</dd> <dt>

<span data-ttu-id="69a3b-122">*zn* \[在\]</span><span class="sxs-lookup"><span data-stu-id="69a3b-122">*zn* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="69a3b-123">類型： **[ **FLOAT**](../winprog/windows-data-types.md)**</span><span class="sxs-lookup"><span data-stu-id="69a3b-123">Type: **[**FLOAT**](../winprog/windows-data-types.md)**</span></span>

<span data-ttu-id="69a3b-124">視圖音量的最小 z 值。</span><span class="sxs-lookup"><span data-stu-id="69a3b-124">Minimum z-value of the view volume.</span></span>

</dd> <dt>

<span data-ttu-id="69a3b-125">*zf* \[在\]</span><span class="sxs-lookup"><span data-stu-id="69a3b-125">*zf* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="69a3b-126">類型： **[ **FLOAT**](../winprog/windows-data-types.md)**</span><span class="sxs-lookup"><span data-stu-id="69a3b-126">Type: **[**FLOAT**](../winprog/windows-data-types.md)**</span></span>

<span data-ttu-id="69a3b-127">視圖音量的最大 z 值。</span><span class="sxs-lookup"><span data-stu-id="69a3b-127">Maximum z-value of the view volume.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="69a3b-128">傳回值</span><span class="sxs-lookup"><span data-stu-id="69a3b-128">Return value</span></span>

<span data-ttu-id="69a3b-129">類型： **[ **D3DXMATRIX**](d3dxmatrix.md)\***</span><span class="sxs-lookup"><span data-stu-id="69a3b-129">Type: **[**D3DXMATRIX**](d3dxmatrix.md)\***</span></span>

<span data-ttu-id="69a3b-130">[**D3DXMATRIX**](d3dxmatrix.md)結構的指標，此結構是自訂、左方的透視圖投影矩陣。</span><span class="sxs-lookup"><span data-stu-id="69a3b-130">Pointer to a [**D3DXMATRIX**](d3dxmatrix.md) structure that is a customized, left-handed perspective projection matrix.</span></span>

## <a name="remarks"></a><span data-ttu-id="69a3b-131">備註</span><span class="sxs-lookup"><span data-stu-id="69a3b-131">Remarks</span></span>

<span data-ttu-id="69a3b-132">**D3DXMatrixPerspectiveOffCenterLH** 函數的所有參數都是相機空間中的距離。</span><span class="sxs-lookup"><span data-stu-id="69a3b-132">All the parameters of the **D3DXMatrixPerspectiveOffCenterLH** function are distances in camera space.</span></span> <span data-ttu-id="69a3b-133">參數描述視圖磁片區的維度。</span><span class="sxs-lookup"><span data-stu-id="69a3b-133">The parameters describe the dimensions of the view volume.</span></span>

<span data-ttu-id="69a3b-134">此函式的傳回值與 *不悅* 參數中所傳回的值相同。</span><span class="sxs-lookup"><span data-stu-id="69a3b-134">The return value for this function is the same value returned in the *pOut* parameter.</span></span> <span data-ttu-id="69a3b-135">如此一來， **D3DXMatrixPerspectiveOffCenterLH** 函式就可以用來做為另一個函式的參數。</span><span class="sxs-lookup"><span data-stu-id="69a3b-135">In this way, the **D3DXMatrixPerspectiveOffCenterLH** function can be used as a parameter for another function.</span></span>

<span data-ttu-id="69a3b-136">此函數會使用下列公式來計算傳回的矩陣。</span><span class="sxs-lookup"><span data-stu-id="69a3b-136">This function uses the following formula to compute the returned matrix.</span></span>


```
2*zn/(r-l)   0            0              0
0            2*zn/(t-b)   0              0
(l+r)/(l-r)  (t+b)/(b-t)  zf/(zf-zn)     1
0            0            zn*zf/(zn-zf)  0
```



## <a name="requirements"></a><span data-ttu-id="69a3b-137">規格需求</span><span class="sxs-lookup"><span data-stu-id="69a3b-137">Requirements</span></span>



| <span data-ttu-id="69a3b-138">需求</span><span class="sxs-lookup"><span data-stu-id="69a3b-138">Requirement</span></span> | <span data-ttu-id="69a3b-139">值</span><span class="sxs-lookup"><span data-stu-id="69a3b-139">Value</span></span> |
|--------------------|----------------------------------------------------------------------------------------|
| <span data-ttu-id="69a3b-140">標頭</span><span class="sxs-lookup"><span data-stu-id="69a3b-140">Header</span></span><br/>  | <dl> <span data-ttu-id="69a3b-141"><dt>D3dx9math。h</dt></span><span class="sxs-lookup"><span data-stu-id="69a3b-141"><dt>D3dx9math.h</dt></span></span> </dl> |
| <span data-ttu-id="69a3b-142">程式庫</span><span class="sxs-lookup"><span data-stu-id="69a3b-142">Library</span></span><br/> | <dl> <span data-ttu-id="69a3b-143"><dt>D3dx9 .lib</dt></span><span class="sxs-lookup"><span data-stu-id="69a3b-143"><dt>D3dx9.lib</dt></span></span> </dl>   |



## <a name="see-also"></a><span data-ttu-id="69a3b-144">另請參閱</span><span class="sxs-lookup"><span data-stu-id="69a3b-144">See also</span></span>

<dl> <dt>

[<span data-ttu-id="69a3b-145">數學函數</span><span class="sxs-lookup"><span data-stu-id="69a3b-145">Math Functions</span></span>](dx9-graphics-reference-d3dx-functions-math.md)
</dt> <dt>

[<span data-ttu-id="69a3b-146">**D3DXMatrixPerspectiveRH**</span><span class="sxs-lookup"><span data-stu-id="69a3b-146">**D3DXMatrixPerspectiveRH**</span></span>](d3dxmatrixperspectiverh.md)
</dt> <dt>

[<span data-ttu-id="69a3b-147">**D3DXMatrixPerspectiveLH**</span><span class="sxs-lookup"><span data-stu-id="69a3b-147">**D3DXMatrixPerspectiveLH**</span></span>](d3dxmatrixperspectivelh.md)
</dt> <dt>

[<span data-ttu-id="69a3b-148">**D3DXMatrixPerspectiveFovRH**</span><span class="sxs-lookup"><span data-stu-id="69a3b-148">**D3DXMatrixPerspectiveFovRH**</span></span>](d3dxmatrixperspectivefovrh.md)
</dt> <dt>

[<span data-ttu-id="69a3b-149">**D3DXMatrixPerspectiveFovLH**</span><span class="sxs-lookup"><span data-stu-id="69a3b-149">**D3DXMatrixPerspectiveFovLH**</span></span>](d3dxmatrixperspectivefovlh.md)
</dt> <dt>

[<span data-ttu-id="69a3b-150">**D3DXMatrixPerspectiveOffCenterRH**</span><span class="sxs-lookup"><span data-stu-id="69a3b-150">**D3DXMatrixPerspectiveOffCenterRH**</span></span>](d3dxmatrixperspectiveoffcenterrh.md)
</dt> </dl>

 

 
