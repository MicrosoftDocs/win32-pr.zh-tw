---
description: 計算平面和3D 向量的點乘積。 向量的 w 參數會假設為0。
ms.assetid: 7aba1e94-6531-4c07-83b0-6100805e8bbd
title: 'D3DXPlaneDotNormal 函式 (D3dx9math) '
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- D3DXPlaneDotNormal
api_type:
- LibDef
api_location:
- d3dx9.lib
- d3dx9.dll
ms.openlocfilehash: 28903fc8ce0073e4014ae6ce75df636222ce32f0
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 03/15/2021
ms.locfileid: "106985529"
---
# <a name="d3dxplanedotnormal-function"></a><span data-ttu-id="2208d-104">D3DXPlaneDotNormal 函式</span><span class="sxs-lookup"><span data-stu-id="2208d-104">D3DXPlaneDotNormal function</span></span>

<span data-ttu-id="2208d-105">計算平面和3D 向量的點乘積。</span><span class="sxs-lookup"><span data-stu-id="2208d-105">Computes the dot product of a plane and a 3D vector.</span></span> <span data-ttu-id="2208d-106">向量的 w 參數會假設為0。</span><span class="sxs-lookup"><span data-stu-id="2208d-106">The w parameter of the vector is assumed to be 0.</span></span>

## <a name="syntax"></a><span data-ttu-id="2208d-107">語法</span><span class="sxs-lookup"><span data-stu-id="2208d-107">Syntax</span></span>


```C++
FLOAT D3DXPlaneDotNormal(
  _In_ const D3DXPLANE   *pP,
  _In_ const D3DXVECTOR3 *pV
);
```



## <a name="parameters"></a><span data-ttu-id="2208d-108">參數</span><span class="sxs-lookup"><span data-stu-id="2208d-108">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="2208d-109">*pP* \[在\]</span><span class="sxs-lookup"><span data-stu-id="2208d-109">*pP* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="2208d-110">Type： **Const [**D3DXPLANE**](d3dxplane.md) \***</span><span class="sxs-lookup"><span data-stu-id="2208d-110">Type: **const [**D3DXPLANE**](d3dxplane.md)\***</span></span>

<span data-ttu-id="2208d-111">來源 [**D3DXPLANE**](d3dxplane.md) 結構的指標。</span><span class="sxs-lookup"><span data-stu-id="2208d-111">Pointer to a source [**D3DXPLANE**](d3dxplane.md) structure.</span></span>

</dd> <dt>

<span data-ttu-id="2208d-112">*pV* \[在\]</span><span class="sxs-lookup"><span data-stu-id="2208d-112">*pV* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="2208d-113">Type： **Const [**D3DXVECTOR3**](d3dxvector3.md) \***</span><span class="sxs-lookup"><span data-stu-id="2208d-113">Type: **const [**D3DXVECTOR3**](d3dxvector3.md)\***</span></span>

<span data-ttu-id="2208d-114">來源 [**D3DXVECTOR3**](d3dxvector3.md) 結構的指標。</span><span class="sxs-lookup"><span data-stu-id="2208d-114">Pointer to a source [**D3DXVECTOR3**](d3dxvector3.md) structure.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="2208d-115">傳回值</span><span class="sxs-lookup"><span data-stu-id="2208d-115">Return value</span></span>

<span data-ttu-id="2208d-116">類型： **[ **FLOAT**](../winprog/windows-data-types.md)**</span><span class="sxs-lookup"><span data-stu-id="2208d-116">Type: **[**FLOAT**](../winprog/windows-data-types.md)**</span></span>

<span data-ttu-id="2208d-117">平面和3D 向量的點乘積。</span><span class="sxs-lookup"><span data-stu-id="2208d-117">The dot product of the plane and 3D vector.</span></span>

## <a name="remarks"></a><span data-ttu-id="2208d-118">備註</span><span class="sxs-lookup"><span data-stu-id="2208d-118">Remarks</span></span>

<span data-ttu-id="2208d-119">給定平面 (a、b、c、d) 和3D 向量 (x、y、z) 此函式的傳回值為 \* x + b \* y + c \* z + d \* 0。</span><span class="sxs-lookup"><span data-stu-id="2208d-119">Given a plane (a, b, c, d) and a 3D vector (x, y, z) the return value of this function is a\*x + b\*y + c\*z + d\*0.</span></span> <span data-ttu-id="2208d-120">**D3DXPlaneDotNormal** 函式可用來計算平面法線之間的角度，另一個則是正常的。</span><span class="sxs-lookup"><span data-stu-id="2208d-120">The **D3DXPlaneDotNormal** function is useful for calculating the angle between the normal of the plane, and another normal.</span></span>

## <a name="requirements"></a><span data-ttu-id="2208d-121">規格需求</span><span class="sxs-lookup"><span data-stu-id="2208d-121">Requirements</span></span>



| <span data-ttu-id="2208d-122">需求</span><span class="sxs-lookup"><span data-stu-id="2208d-122">Requirement</span></span> | <span data-ttu-id="2208d-123">值</span><span class="sxs-lookup"><span data-stu-id="2208d-123">Value</span></span> |
|--------------------|----------------------------------------------------------------------------------------|
| <span data-ttu-id="2208d-124">標頭</span><span class="sxs-lookup"><span data-stu-id="2208d-124">Header</span></span><br/>  | <dl> <span data-ttu-id="2208d-125"><dt>D3dx9math。h</dt></span><span class="sxs-lookup"><span data-stu-id="2208d-125"><dt>D3dx9math.h</dt></span></span> </dl> |
| <span data-ttu-id="2208d-126">程式庫</span><span class="sxs-lookup"><span data-stu-id="2208d-126">Library</span></span><br/> | <dl> <span data-ttu-id="2208d-127"><dt>D3dx9 .lib</dt></span><span class="sxs-lookup"><span data-stu-id="2208d-127"><dt>D3dx9.lib</dt></span></span> </dl>   |



## <a name="see-also"></a><span data-ttu-id="2208d-128">另請參閱</span><span class="sxs-lookup"><span data-stu-id="2208d-128">See also</span></span>

<dl> <dt>

[<span data-ttu-id="2208d-129">數學函數</span><span class="sxs-lookup"><span data-stu-id="2208d-129">Math Functions</span></span>](dx9-graphics-reference-d3dx-functions-math.md)
</dt> <dt>

[<span data-ttu-id="2208d-130">**D3DXPlaneDot**</span><span class="sxs-lookup"><span data-stu-id="2208d-130">**D3DXPlaneDot**</span></span>](d3dxplanedot.md)
</dt> <dt>

[<span data-ttu-id="2208d-131">**D3DXPlaneDotCoord**</span><span class="sxs-lookup"><span data-stu-id="2208d-131">**D3DXPlaneDotCoord**</span></span>](d3dxplanedotcoord.md)
</dt> </dl>

 

 
