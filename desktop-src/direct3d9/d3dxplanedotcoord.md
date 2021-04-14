---
description: 計算平面和3D 向量的點乘積。 向量的 w 參數會假設為1。
ms.assetid: 634de6bc-b631-493d-a7a6-292a3c3253d6
title: 'D3DXPlaneDotCoord 函式 (D3dx9math) '
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- D3DXPlaneDotCoord
api_type:
- LibDef
api_location:
- d3dx9.lib
- d3dx9.dll
ms.openlocfilehash: 99ee9db7df541dcf74867b828a73ede80f11e22b
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 03/15/2021
ms.locfileid: "104196178"
---
# <a name="d3dxplanedotcoord-function"></a><span data-ttu-id="c50aa-104">D3DXPlaneDotCoord 函式</span><span class="sxs-lookup"><span data-stu-id="c50aa-104">D3DXPlaneDotCoord function</span></span>

<span data-ttu-id="c50aa-105">計算平面和3D 向量的點乘積。</span><span class="sxs-lookup"><span data-stu-id="c50aa-105">Computes the dot product of a plane and a 3D vector.</span></span> <span data-ttu-id="c50aa-106">向量的 w 參數會假設為1。</span><span class="sxs-lookup"><span data-stu-id="c50aa-106">The w parameter of the vector is assumed to be 1.</span></span>

## <a name="syntax"></a><span data-ttu-id="c50aa-107">語法</span><span class="sxs-lookup"><span data-stu-id="c50aa-107">Syntax</span></span>


```C++
FLOAT D3DXPlaneDotCoord(
  _In_ const D3DXPLANE   *pP,
  _In_ const D3DXVECTOR3 *pV
);
```



## <a name="parameters"></a><span data-ttu-id="c50aa-108">參數</span><span class="sxs-lookup"><span data-stu-id="c50aa-108">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="c50aa-109">*pP* \[在\]</span><span class="sxs-lookup"><span data-stu-id="c50aa-109">*pP* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="c50aa-110">Type： **Const [**D3DXPLANE**](d3dxplane.md) \***</span><span class="sxs-lookup"><span data-stu-id="c50aa-110">Type: **const [**D3DXPLANE**](d3dxplane.md)\***</span></span>

<span data-ttu-id="c50aa-111">來源 [**D3DXPLANE**](d3dxplane.md) 結構的指標。</span><span class="sxs-lookup"><span data-stu-id="c50aa-111">Pointer to a source [**D3DXPLANE**](d3dxplane.md) structure.</span></span>

</dd> <dt>

<span data-ttu-id="c50aa-112">*pV* \[在\]</span><span class="sxs-lookup"><span data-stu-id="c50aa-112">*pV* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="c50aa-113">Type： **Const [**D3DXVECTOR3**](d3dxvector3.md) \***</span><span class="sxs-lookup"><span data-stu-id="c50aa-113">Type: **const [**D3DXVECTOR3**](d3dxvector3.md)\***</span></span>

<span data-ttu-id="c50aa-114">來源 [**D3DXVECTOR3**](d3dxvector3.md) 結構的指標。</span><span class="sxs-lookup"><span data-stu-id="c50aa-114">Pointer to a source [**D3DXVECTOR3**](d3dxvector3.md) structure.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="c50aa-115">傳回值</span><span class="sxs-lookup"><span data-stu-id="c50aa-115">Return value</span></span>

<span data-ttu-id="c50aa-116">類型： **[ **FLOAT**](../winprog/windows-data-types.md)**</span><span class="sxs-lookup"><span data-stu-id="c50aa-116">Type: **[**FLOAT**](../winprog/windows-data-types.md)**</span></span>

<span data-ttu-id="c50aa-117">平面和3D 向量的點乘積。</span><span class="sxs-lookup"><span data-stu-id="c50aa-117">The dot product of the plane and 3D vector.</span></span>

## <a name="remarks"></a><span data-ttu-id="c50aa-118">備註</span><span class="sxs-lookup"><span data-stu-id="c50aa-118">Remarks</span></span>

<span data-ttu-id="c50aa-119">給定平面 (a、b、c、d) 和3D 向量 (x、y、z) 此函式的傳回值為 \* x + b \* y + c \* z + d \* 1。</span><span class="sxs-lookup"><span data-stu-id="c50aa-119">Given a plane (a, b, c, d) and a 3D vector (x, y, z) the return value of this function is a\*x + b\*y + c\*z + d\*1.</span></span> <span data-ttu-id="c50aa-120">**D3DXPlaneDotCoord** 函數適合用來判斷平面在3d 空間中的座標關聯性。</span><span class="sxs-lookup"><span data-stu-id="c50aa-120">The **D3DXPlaneDotCoord** function is useful for determining the plane's relationship with a coordinate in 3D space.</span></span>

## <a name="requirements"></a><span data-ttu-id="c50aa-121">規格需求</span><span class="sxs-lookup"><span data-stu-id="c50aa-121">Requirements</span></span>



| <span data-ttu-id="c50aa-122">需求</span><span class="sxs-lookup"><span data-stu-id="c50aa-122">Requirement</span></span> | <span data-ttu-id="c50aa-123">值</span><span class="sxs-lookup"><span data-stu-id="c50aa-123">Value</span></span> |
|--------------------|----------------------------------------------------------------------------------------|
| <span data-ttu-id="c50aa-124">標頭</span><span class="sxs-lookup"><span data-stu-id="c50aa-124">Header</span></span><br/>  | <dl> <span data-ttu-id="c50aa-125"><dt>D3dx9math。h</dt></span><span class="sxs-lookup"><span data-stu-id="c50aa-125"><dt>D3dx9math.h</dt></span></span> </dl> |
| <span data-ttu-id="c50aa-126">程式庫</span><span class="sxs-lookup"><span data-stu-id="c50aa-126">Library</span></span><br/> | <dl> <span data-ttu-id="c50aa-127"><dt>D3dx9 .lib</dt></span><span class="sxs-lookup"><span data-stu-id="c50aa-127"><dt>D3dx9.lib</dt></span></span> </dl>   |



## <a name="see-also"></a><span data-ttu-id="c50aa-128">另請參閱</span><span class="sxs-lookup"><span data-stu-id="c50aa-128">See also</span></span>

<dl> <dt>

[<span data-ttu-id="c50aa-129">數學函數</span><span class="sxs-lookup"><span data-stu-id="c50aa-129">Math Functions</span></span>](dx9-graphics-reference-d3dx-functions-math.md)
</dt> <dt>

[<span data-ttu-id="c50aa-130">**D3DXPlaneDot**</span><span class="sxs-lookup"><span data-stu-id="c50aa-130">**D3DXPlaneDot**</span></span>](d3dxplanedot.md)
</dt> <dt>

[<span data-ttu-id="c50aa-131">**D3DXPlaneDotNormal**</span><span class="sxs-lookup"><span data-stu-id="c50aa-131">**D3DXPlaneDotNormal**</span></span>](d3dxplanedotnormal.md)
</dt> </dl>

 

 
