---
description: 建立沿著 X 軸、y 軸和 Z 軸縮放的矩陣。
ms.assetid: 1804bf41-26de-4be1-ad62-7a871d7408e6
title: 'D3DXMatrixScaling 函式 (D3DX10Math) '
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- D3DXMatrixScaling
api_type:
- LibDef
api_location:
- D3DX10.lib
- D3DX10.dll
ms.openlocfilehash: adb1becb67a561778b31c90ea3d6c96e776c9a67
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 03/15/2021
ms.locfileid: "104323216"
---
# <a name="d3dxmatrixscaling-function-d3dx10mathh"></a><span data-ttu-id="9a32d-103">D3DXMatrixScaling 函式 (D3DX10Math) </span><span class="sxs-lookup"><span data-stu-id="9a32d-103">D3DXMatrixScaling function (D3DX10Math.h)</span></span>

<span data-ttu-id="9a32d-104">建立沿著 X 軸、y 軸和 Z 軸縮放的矩陣。</span><span class="sxs-lookup"><span data-stu-id="9a32d-104">Builds a matrix that scales along the x-axis, the y-axis, and the z-axis.</span></span>

## <a name="syntax"></a><span data-ttu-id="9a32d-105">語法</span><span class="sxs-lookup"><span data-stu-id="9a32d-105">Syntax</span></span>


```C++
D3DXMATRIX* D3DXMatrixScaling(
  _Inout_ D3DXMATRIX *pOut,
  _In_    FLOAT      sx,
  _In_    FLOAT      sy,
  _In_    FLOAT      sz
);
```



## <a name="parameters"></a><span data-ttu-id="9a32d-106">參數</span><span class="sxs-lookup"><span data-stu-id="9a32d-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="9a32d-107">*不悅* \[in、out\]</span><span class="sxs-lookup"><span data-stu-id="9a32d-107">*pOut* \[in, out\]</span></span>
</dt> <dd>

<span data-ttu-id="9a32d-108">類型： **[ **D3DXMATRIX**](../direct3d9/d3dxmatrix.md)\***</span><span class="sxs-lookup"><span data-stu-id="9a32d-108">Type: **[**D3DXMATRIX**](../direct3d9/d3dxmatrix.md)\***</span></span>

<span data-ttu-id="9a32d-109">[**D3DXMATRIX**](d3d10-d3dxmatrix.md)結構的指標，此結構是作業的結果。</span><span class="sxs-lookup"><span data-stu-id="9a32d-109">Pointer to the [**D3DXMATRIX**](d3d10-d3dxmatrix.md) structure that is the result of the operation.</span></span>

</dd> <dt>

<span data-ttu-id="9a32d-110">*sx* \[在\]</span><span class="sxs-lookup"><span data-stu-id="9a32d-110">*sx* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="9a32d-111">類型： **[ **FLOAT**](../winprog/windows-data-types.md)**</span><span class="sxs-lookup"><span data-stu-id="9a32d-111">Type: **[**FLOAT**](../winprog/windows-data-types.md)**</span></span>

<span data-ttu-id="9a32d-112">沿著 X 軸套用的縮放係數。</span><span class="sxs-lookup"><span data-stu-id="9a32d-112">Scaling factor that is applied along the x-axis.</span></span>

</dd> <dt>

<span data-ttu-id="9a32d-113">*sy* \[在\]</span><span class="sxs-lookup"><span data-stu-id="9a32d-113">*sy* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="9a32d-114">類型： **[ **FLOAT**](../winprog/windows-data-types.md)**</span><span class="sxs-lookup"><span data-stu-id="9a32d-114">Type: **[**FLOAT**](../winprog/windows-data-types.md)**</span></span>

<span data-ttu-id="9a32d-115">沿著 y 軸套用的縮放係數。</span><span class="sxs-lookup"><span data-stu-id="9a32d-115">Scaling factor that is applied along the y-axis.</span></span>

</dd> <dt>

<span data-ttu-id="9a32d-116">*sz* \[在\]</span><span class="sxs-lookup"><span data-stu-id="9a32d-116">*sz* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="9a32d-117">類型： **[ **FLOAT**](../winprog/windows-data-types.md)**</span><span class="sxs-lookup"><span data-stu-id="9a32d-117">Type: **[**FLOAT**](../winprog/windows-data-types.md)**</span></span>

<span data-ttu-id="9a32d-118">沿著 Z 軸套用的縮放係數。</span><span class="sxs-lookup"><span data-stu-id="9a32d-118">Scaling factor that is applied along the z-axis.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="9a32d-119">傳回值</span><span class="sxs-lookup"><span data-stu-id="9a32d-119">Return value</span></span>

<span data-ttu-id="9a32d-120">類型： **[ **D3DXMATRIX**](../direct3d9/d3dxmatrix.md)\***</span><span class="sxs-lookup"><span data-stu-id="9a32d-120">Type: **[**D3DXMATRIX**](../direct3d9/d3dxmatrix.md)\***</span></span>

<span data-ttu-id="9a32d-121">縮放轉換 D3DXMATRIX 的指標。</span><span class="sxs-lookup"><span data-stu-id="9a32d-121">Pointer to the scaling transformation D3DXMATRIX.</span></span>

## <a name="remarks"></a><span data-ttu-id="9a32d-122">備註</span><span class="sxs-lookup"><span data-stu-id="9a32d-122">Remarks</span></span>

<span data-ttu-id="9a32d-123">此函式的傳回值與不悅參數中所傳回的值相同。</span><span class="sxs-lookup"><span data-stu-id="9a32d-123">The return value for this function is the same value returned in the pOut parameter.</span></span> <span data-ttu-id="9a32d-124">如此一來，D3DXMatrixScaling 函式就可以用來做為另一個函式的參數。</span><span class="sxs-lookup"><span data-stu-id="9a32d-124">In this way, the D3DXMatrixScaling function can be used as a parameter for another function.</span></span>

## <a name="requirements"></a><span data-ttu-id="9a32d-125">規格需求</span><span class="sxs-lookup"><span data-stu-id="9a32d-125">Requirements</span></span>



| <span data-ttu-id="9a32d-126">需求</span><span class="sxs-lookup"><span data-stu-id="9a32d-126">Requirement</span></span> | <span data-ttu-id="9a32d-127">值</span><span class="sxs-lookup"><span data-stu-id="9a32d-127">Value</span></span> |
|--------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="9a32d-128">標頭</span><span class="sxs-lookup"><span data-stu-id="9a32d-128">Header</span></span><br/>  | <dl> <span data-ttu-id="9a32d-129"><dt>D3DX10Math。h</dt></span><span class="sxs-lookup"><span data-stu-id="9a32d-129"><dt>D3DX10Math.h</dt></span></span> </dl> |
| <span data-ttu-id="9a32d-130">程式庫</span><span class="sxs-lookup"><span data-stu-id="9a32d-130">Library</span></span><br/> | <dl> <span data-ttu-id="9a32d-131"><dt>D3DX10 .lib</dt></span><span class="sxs-lookup"><span data-stu-id="9a32d-131"><dt>D3DX10.lib</dt></span></span> </dl>   |



## <a name="see-also"></a><span data-ttu-id="9a32d-132">另請參閱</span><span class="sxs-lookup"><span data-stu-id="9a32d-132">See also</span></span>

<dl> <dt>

[<span data-ttu-id="9a32d-133">數學函數</span><span class="sxs-lookup"><span data-stu-id="9a32d-133">Math Functions</span></span>](d3d10-graphics-reference-d3dx10-functions-math.md)
</dt> </dl>

 

 
