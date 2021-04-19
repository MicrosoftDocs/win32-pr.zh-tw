---
description: 計算平面和4D 向量的點乘積。
ms.assetid: e6232ca8-52cc-472d-8bdb-4f8dfc520d4f
title: 'D3DXPlaneDot 函式 (D3dx9math) '
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- D3DXPlaneDot
api_type:
- LibDef
api_location:
- d3dx9.lib
- d3dx9.dll
ms.openlocfilehash: b6f33e591df364151a7090e5b4a9dd0773f5788a
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 03/15/2021
ms.locfileid: "106974832"
---
# <a name="d3dxplanedot-function"></a><span data-ttu-id="02e59-103">D3DXPlaneDot 函式</span><span class="sxs-lookup"><span data-stu-id="02e59-103">D3DXPlaneDot function</span></span>

<span data-ttu-id="02e59-104">計算平面和4D 向量的點乘積。</span><span class="sxs-lookup"><span data-stu-id="02e59-104">Computes the dot product of a plane and a 4D vector.</span></span>

## <a name="syntax"></a><span data-ttu-id="02e59-105">語法</span><span class="sxs-lookup"><span data-stu-id="02e59-105">Syntax</span></span>


```C++
FLOAT D3DXPlaneDot(
  _In_ const D3DXPLANE   *pP,
  _In_ const D3DXVECTOR4 *pV
);
```



## <a name="parameters"></a><span data-ttu-id="02e59-106">參數</span><span class="sxs-lookup"><span data-stu-id="02e59-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="02e59-107">*pP* \[在\]</span><span class="sxs-lookup"><span data-stu-id="02e59-107">*pP* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="02e59-108">Type： **Const [**D3DXPLANE**](d3dxplane.md) \***</span><span class="sxs-lookup"><span data-stu-id="02e59-108">Type: **const [**D3DXPLANE**](d3dxplane.md)\***</span></span>

<span data-ttu-id="02e59-109">來源 [**D3DXPLANE**](d3dxplane.md) 結構的指標。</span><span class="sxs-lookup"><span data-stu-id="02e59-109">Pointer to a source [**D3DXPLANE**](d3dxplane.md) structure.</span></span>

</dd> <dt>

<span data-ttu-id="02e59-110">*pV* \[在\]</span><span class="sxs-lookup"><span data-stu-id="02e59-110">*pV* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="02e59-111">Type： **Const [**D3DXVECTOR4**](d3dxvector4.md) \***</span><span class="sxs-lookup"><span data-stu-id="02e59-111">Type: **const [**D3DXVECTOR4**](d3dxvector4.md)\***</span></span>

<span data-ttu-id="02e59-112">[**D3DXVECTOR4**](d3dxvector4.md)結構的指標。</span><span class="sxs-lookup"><span data-stu-id="02e59-112">Pointer to a [**D3DXVECTOR4**](d3dxvector4.md) structure.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="02e59-113">傳回值</span><span class="sxs-lookup"><span data-stu-id="02e59-113">Return value</span></span>

<span data-ttu-id="02e59-114">類型： **[ **FLOAT**](../winprog/windows-data-types.md)**</span><span class="sxs-lookup"><span data-stu-id="02e59-114">Type: **[**FLOAT**](../winprog/windows-data-types.md)**</span></span>

<span data-ttu-id="02e59-115">平面和4D 向量的點乘積。</span><span class="sxs-lookup"><span data-stu-id="02e59-115">The dot product of the plane and 4D vector.</span></span>

## <a name="remarks"></a><span data-ttu-id="02e59-116">備註</span><span class="sxs-lookup"><span data-stu-id="02e59-116">Remarks</span></span>

<span data-ttu-id="02e59-117">給定平面 (a、b、c、d) 和4D 向量 (x、y、z、w) 此函式的傳回值為 \* x + b \* y + c \* z + d \* w。</span><span class="sxs-lookup"><span data-stu-id="02e59-117">Given a plane (a, b, c, d) and a 4D vector (x, y, z, w) the return value of this function is a\*x + b\*y + c\*z + d\*w.</span></span> <span data-ttu-id="02e59-118">**D3DXPlaneDot** 函數適合用來判斷平面與同質座標之間的關聯性。</span><span class="sxs-lookup"><span data-stu-id="02e59-118">The **D3DXPlaneDot** function is useful for determining the plane's relationship with a homogeneous coordinate.</span></span> <span data-ttu-id="02e59-119">例如，您可以使用這個函式來判斷特定的座標是否在特定的平面上，或特定平面的哪一端。</span><span class="sxs-lookup"><span data-stu-id="02e59-119">For example, this function could be used to determine if a particular coordinate is on a particular plane, or on which side of a particular plane a particular coordinate lies.</span></span>

## <a name="requirements"></a><span data-ttu-id="02e59-120">規格需求</span><span class="sxs-lookup"><span data-stu-id="02e59-120">Requirements</span></span>



| <span data-ttu-id="02e59-121">需求</span><span class="sxs-lookup"><span data-stu-id="02e59-121">Requirement</span></span> | <span data-ttu-id="02e59-122">值</span><span class="sxs-lookup"><span data-stu-id="02e59-122">Value</span></span> |
|--------------------|----------------------------------------------------------------------------------------|
| <span data-ttu-id="02e59-123">標頭</span><span class="sxs-lookup"><span data-stu-id="02e59-123">Header</span></span><br/>  | <dl> <span data-ttu-id="02e59-124"><dt>D3dx9math。h</dt></span><span class="sxs-lookup"><span data-stu-id="02e59-124"><dt>D3dx9math.h</dt></span></span> </dl> |
| <span data-ttu-id="02e59-125">程式庫</span><span class="sxs-lookup"><span data-stu-id="02e59-125">Library</span></span><br/> | <dl> <span data-ttu-id="02e59-126"><dt>D3dx9 .lib</dt></span><span class="sxs-lookup"><span data-stu-id="02e59-126"><dt>D3dx9.lib</dt></span></span> </dl>   |



## <a name="see-also"></a><span data-ttu-id="02e59-127">另請參閱</span><span class="sxs-lookup"><span data-stu-id="02e59-127">See also</span></span>

<dl> <dt>

[<span data-ttu-id="02e59-128">數學函數</span><span class="sxs-lookup"><span data-stu-id="02e59-128">Math Functions</span></span>](dx9-graphics-reference-d3dx-functions-math.md)
</dt> <dt>

[<span data-ttu-id="02e59-129">**D3DXPlaneDotCoord**</span><span class="sxs-lookup"><span data-stu-id="02e59-129">**D3DXPlaneDotCoord**</span></span>](d3dxplanedotcoord.md)
</dt> <dt>

[<span data-ttu-id="02e59-130">**D3DXPlaneDotNormal**</span><span class="sxs-lookup"><span data-stu-id="02e59-130">**D3DXPlaneDotNormal**</span></span>](d3dxplanedotnormal.md)
</dt> </dl>

 

 
