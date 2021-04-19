---
description: 建立沿著 X 軸、y 軸和 Z 軸縮放的矩陣。
ms.assetid: f51baa4e-0aec-4de8-b746-24cb52f318d6
title: 'D3DXMatrixScaling 函式 (D3dx9math) '
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
- d3dx9.lib
- d3dx9.dll
ms.openlocfilehash: 7cfc14fc1d514f68f2881d26c4729440d709af93
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 03/15/2021
ms.locfileid: "106990014"
---
# <a name="d3dxmatrixscaling-function-d3dx9mathh"></a><span data-ttu-id="fbc33-103">D3DXMatrixScaling 函式 (D3dx9math) </span><span class="sxs-lookup"><span data-stu-id="fbc33-103">D3DXMatrixScaling function (D3dx9math.h)</span></span>

<span data-ttu-id="fbc33-104">建立沿著 X 軸、y 軸和 Z 軸縮放的矩陣。</span><span class="sxs-lookup"><span data-stu-id="fbc33-104">Builds a matrix that scales along the x-axis, the y-axis, and the z-axis.</span></span>

## <a name="syntax"></a><span data-ttu-id="fbc33-105">語法</span><span class="sxs-lookup"><span data-stu-id="fbc33-105">Syntax</span></span>


```C++
D3DXMATRIX* D3DXMatrixScaling(
  _Inout_ D3DXMATRIX *pOut,
  _In_    FLOAT      sx,
  _In_    FLOAT      sy,
  _In_    FLOAT      sz
);
```



## <a name="parameters"></a><span data-ttu-id="fbc33-106">參數</span><span class="sxs-lookup"><span data-stu-id="fbc33-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="fbc33-107">*不悅* \[in、out\]</span><span class="sxs-lookup"><span data-stu-id="fbc33-107">*pOut* \[in, out\]</span></span>
</dt> <dd>

<span data-ttu-id="fbc33-108">類型： **[ **D3DXMATRIX**](d3dxmatrix.md)\***</span><span class="sxs-lookup"><span data-stu-id="fbc33-108">Type: **[**D3DXMATRIX**](d3dxmatrix.md)\***</span></span>

<span data-ttu-id="fbc33-109">[**D3DXMATRIX**](d3dxmatrix.md)結構的指標，此結構是作業的結果。</span><span class="sxs-lookup"><span data-stu-id="fbc33-109">Pointer to the [**D3DXMATRIX**](d3dxmatrix.md) structure that is the result of the operation.</span></span>

</dd> <dt>

<span data-ttu-id="fbc33-110">*sx* \[在\]</span><span class="sxs-lookup"><span data-stu-id="fbc33-110">*sx* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="fbc33-111">類型： **[ **FLOAT**](../winprog/windows-data-types.md)**</span><span class="sxs-lookup"><span data-stu-id="fbc33-111">Type: **[**FLOAT**](../winprog/windows-data-types.md)**</span></span>

<span data-ttu-id="fbc33-112">沿著 X 軸套用的縮放係數。</span><span class="sxs-lookup"><span data-stu-id="fbc33-112">Scaling factor that is applied along the x-axis.</span></span>

</dd> <dt>

<span data-ttu-id="fbc33-113">*sy* \[在\]</span><span class="sxs-lookup"><span data-stu-id="fbc33-113">*sy* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="fbc33-114">類型： **[ **FLOAT**](../winprog/windows-data-types.md)**</span><span class="sxs-lookup"><span data-stu-id="fbc33-114">Type: **[**FLOAT**](../winprog/windows-data-types.md)**</span></span>

<span data-ttu-id="fbc33-115">沿著 y 軸套用的縮放係數。</span><span class="sxs-lookup"><span data-stu-id="fbc33-115">Scaling factor that is applied along the y-axis.</span></span>

</dd> <dt>

<span data-ttu-id="fbc33-116">*sz* \[在\]</span><span class="sxs-lookup"><span data-stu-id="fbc33-116">*sz* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="fbc33-117">類型： **[ **FLOAT**](../winprog/windows-data-types.md)**</span><span class="sxs-lookup"><span data-stu-id="fbc33-117">Type: **[**FLOAT**](../winprog/windows-data-types.md)**</span></span>

<span data-ttu-id="fbc33-118">沿著 Z 軸套用的縮放係數。</span><span class="sxs-lookup"><span data-stu-id="fbc33-118">Scaling factor that is applied along the z-axis.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="fbc33-119">傳回值</span><span class="sxs-lookup"><span data-stu-id="fbc33-119">Return value</span></span>

<span data-ttu-id="fbc33-120">類型： **[ **D3DXMATRIX**](d3dxmatrix.md)\***</span><span class="sxs-lookup"><span data-stu-id="fbc33-120">Type: **[**D3DXMATRIX**](d3dxmatrix.md)\***</span></span>

<span data-ttu-id="fbc33-121">縮放轉換 [**D3DXMATRIX**](d3dxmatrix.md)的指標。</span><span class="sxs-lookup"><span data-stu-id="fbc33-121">Pointer to the scaling transformation [**D3DXMATRIX**](d3dxmatrix.md).</span></span>

## <a name="remarks"></a><span data-ttu-id="fbc33-122">備註</span><span class="sxs-lookup"><span data-stu-id="fbc33-122">Remarks</span></span>

<span data-ttu-id="fbc33-123">此函式的傳回值與 *不悅* 參數中所傳回的值相同。</span><span class="sxs-lookup"><span data-stu-id="fbc33-123">The return value for this function is the same value returned in the *pOut* parameter.</span></span> <span data-ttu-id="fbc33-124">如此一來， **D3DXMatrixScaling** 函式就可以用來做為另一個函式的參數。</span><span class="sxs-lookup"><span data-stu-id="fbc33-124">In this way, the **D3DXMatrixScaling** function can be used as a parameter for another function.</span></span>

## <a name="requirements"></a><span data-ttu-id="fbc33-125">規格需求</span><span class="sxs-lookup"><span data-stu-id="fbc33-125">Requirements</span></span>



| <span data-ttu-id="fbc33-126">需求</span><span class="sxs-lookup"><span data-stu-id="fbc33-126">Requirement</span></span> | <span data-ttu-id="fbc33-127">值</span><span class="sxs-lookup"><span data-stu-id="fbc33-127">Value</span></span> |
|--------------------|----------------------------------------------------------------------------------------|
| <span data-ttu-id="fbc33-128">標頭</span><span class="sxs-lookup"><span data-stu-id="fbc33-128">Header</span></span><br/>  | <dl> <span data-ttu-id="fbc33-129"><dt>D3dx9math。h</dt></span><span class="sxs-lookup"><span data-stu-id="fbc33-129"><dt>D3dx9math.h</dt></span></span> </dl> |
| <span data-ttu-id="fbc33-130">程式庫</span><span class="sxs-lookup"><span data-stu-id="fbc33-130">Library</span></span><br/> | <dl> <span data-ttu-id="fbc33-131"><dt>D3dx9 .lib</dt></span><span class="sxs-lookup"><span data-stu-id="fbc33-131"><dt>D3dx9.lib</dt></span></span> </dl>   |



## <a name="see-also"></a><span data-ttu-id="fbc33-132">另請參閱</span><span class="sxs-lookup"><span data-stu-id="fbc33-132">See also</span></span>

<dl> <dt>

[<span data-ttu-id="fbc33-133">數學函數</span><span class="sxs-lookup"><span data-stu-id="fbc33-133">Math Functions</span></span>](dx9-graphics-reference-d3dx-functions-math.md)
</dt> </dl>

 

 
