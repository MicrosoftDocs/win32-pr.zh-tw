---
description: 使用指定的縮放比例調整平面。
ms.assetid: 3a0454ef-2821-472f-b7a4-5e49bb5f556e
title: 'D3DXPlaneScale 函式 (D3dx9math) '
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- D3DXPlaneScale
api_type:
- LibDef
api_location:
- d3dx9.lib
- d3dx9.dll
ms.openlocfilehash: 39bd80ceebaee915b8175f2adf13b3b200000fa6
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 03/15/2021
ms.locfileid: "106989181"
---
# <a name="d3dxplanescale-function"></a><span data-ttu-id="93cb3-103">D3DXPlaneScale 函式</span><span class="sxs-lookup"><span data-stu-id="93cb3-103">D3DXPlaneScale function</span></span>

<span data-ttu-id="93cb3-104">使用指定的縮放比例調整平面。</span><span class="sxs-lookup"><span data-stu-id="93cb3-104">Scale the plane with the given scaling factor.</span></span>

## <a name="syntax"></a><span data-ttu-id="93cb3-105">語法</span><span class="sxs-lookup"><span data-stu-id="93cb3-105">Syntax</span></span>


```C++
D3DXPLANE* D3DXPlaneScale(
  _Inout_       D3DXPLANE *pOut,
  _In_    const D3DXPLANE *pP,
  _In_          FLOAT     s
);
```



## <a name="parameters"></a><span data-ttu-id="93cb3-106">參數</span><span class="sxs-lookup"><span data-stu-id="93cb3-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="93cb3-107">*不悅* \[in、out\]</span><span class="sxs-lookup"><span data-stu-id="93cb3-107">*pOut* \[in, out\]</span></span>
</dt> <dd>

<span data-ttu-id="93cb3-108">類型： **[ **D3DXPLANE**](d3dxplane.md)\***</span><span class="sxs-lookup"><span data-stu-id="93cb3-108">Type: **[**D3DXPLANE**](d3dxplane.md)\***</span></span>

<span data-ttu-id="93cb3-109">[**D3DXPLANE**](d3dxplane.md)結構的指標，此結構是作業的結果。</span><span class="sxs-lookup"><span data-stu-id="93cb3-109">Pointer to the [**D3DXPLANE**](d3dxplane.md) structure that is the result of the operation.</span></span>

</dd> <dt>

<span data-ttu-id="93cb3-110">*pP* \[在\]</span><span class="sxs-lookup"><span data-stu-id="93cb3-110">*pP* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="93cb3-111">Type： **Const [**D3DXPLANE**](d3dxplane.md) \***</span><span class="sxs-lookup"><span data-stu-id="93cb3-111">Type: **const [**D3DXPLANE**](d3dxplane.md)\***</span></span>

<span data-ttu-id="93cb3-112">來源 [**D3DXPLANE**](d3dxplane.md) 結構的指標。</span><span class="sxs-lookup"><span data-stu-id="93cb3-112">Pointer to the source [**D3DXPLANE**](d3dxplane.md) structure.</span></span>

</dd> <dt>

<span data-ttu-id="93cb3-113"> \[ 中的 s\]</span><span class="sxs-lookup"><span data-stu-id="93cb3-113">*s* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="93cb3-114">類型： **[ **FLOAT**](../winprog/windows-data-types.md)**</span><span class="sxs-lookup"><span data-stu-id="93cb3-114">Type: **[**FLOAT**](../winprog/windows-data-types.md)**</span></span>

<span data-ttu-id="93cb3-115">比例因數。</span><span class="sxs-lookup"><span data-stu-id="93cb3-115">Scale factor.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="93cb3-116">傳回值</span><span class="sxs-lookup"><span data-stu-id="93cb3-116">Return value</span></span>

<span data-ttu-id="93cb3-117">類型： **[ **D3DXPLANE**](d3dxplane.md)\***</span><span class="sxs-lookup"><span data-stu-id="93cb3-117">Type: **[**D3DXPLANE**](d3dxplane.md)\***</span></span>

<span data-ttu-id="93cb3-118">[**D3DXPLANE**](d3dxplane.md)結構的指標，表示縮放的平面。</span><span class="sxs-lookup"><span data-stu-id="93cb3-118">Pointer to a [**D3DXPLANE**](d3dxplane.md) structure that represents the scaled plane.</span></span>

## <a name="remarks"></a><span data-ttu-id="93cb3-119">備註</span><span class="sxs-lookup"><span data-stu-id="93cb3-119">Remarks</span></span>

<span data-ttu-id="93cb3-120">此函式的傳回值與 *不悅* 參數中所傳回的值相同。</span><span class="sxs-lookup"><span data-stu-id="93cb3-120">The return value for this function is the same value returned in the *pOut* parameter.</span></span> <span data-ttu-id="93cb3-121">因此，此函式可以當做另一個函式的參數使用。</span><span class="sxs-lookup"><span data-stu-id="93cb3-121">Therefore, this function can be used as a parameter for another function.</span></span>

## <a name="requirements"></a><span data-ttu-id="93cb3-122">規格需求</span><span class="sxs-lookup"><span data-stu-id="93cb3-122">Requirements</span></span>



| <span data-ttu-id="93cb3-123">需求</span><span class="sxs-lookup"><span data-stu-id="93cb3-123">Requirement</span></span> | <span data-ttu-id="93cb3-124">值</span><span class="sxs-lookup"><span data-stu-id="93cb3-124">Value</span></span> |
|--------------------|----------------------------------------------------------------------------------------|
| <span data-ttu-id="93cb3-125">標頭</span><span class="sxs-lookup"><span data-stu-id="93cb3-125">Header</span></span><br/>  | <dl> <span data-ttu-id="93cb3-126"><dt>D3dx9math。h</dt></span><span class="sxs-lookup"><span data-stu-id="93cb3-126"><dt>D3dx9math.h</dt></span></span> </dl> |
| <span data-ttu-id="93cb3-127">程式庫</span><span class="sxs-lookup"><span data-stu-id="93cb3-127">Library</span></span><br/> | <dl> <span data-ttu-id="93cb3-128"><dt>D3dx9 .lib</dt></span><span class="sxs-lookup"><span data-stu-id="93cb3-128"><dt>D3dx9.lib</dt></span></span> </dl>   |



## <a name="see-also"></a><span data-ttu-id="93cb3-129">另請參閱</span><span class="sxs-lookup"><span data-stu-id="93cb3-129">See also</span></span>

<dl> <dt>

[<span data-ttu-id="93cb3-130">數學函數</span><span class="sxs-lookup"><span data-stu-id="93cb3-130">Math Functions</span></span>](dx9-graphics-reference-d3dx-functions-math.md)
</dt> </dl>

 

 
