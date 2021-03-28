---
title: RWTexture3D：： GetDimensions 函數
description: 傳回資源的維度。 |RWTexture3D：： GetDimensions 函數
ms.assetid: ba70b955-1e80-4f27-84f1-fc9d26a1f1ab
keywords:
- GetDimensions 函式 HLSL
topic_type:
- apiref
api_name:
- GetDimensions
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
api_location: ''
ms.openlocfilehash: 499ab493851257030921e9d55f4873eef8726915
ms.sourcegitcommit: 92e74c99f8f4d097676959d0c317f533c2400a80
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 03/09/2021
ms.locfileid: "104322163"
---
# <a name="rwtexture3dgetdimensions-function"></a><span data-ttu-id="ed633-105">RWTexture3D：： GetDimensions 函數</span><span class="sxs-lookup"><span data-stu-id="ed633-105">RWTexture3D::GetDimensions function</span></span>

<span data-ttu-id="ed633-106">傳回資源的維度。</span><span class="sxs-lookup"><span data-stu-id="ed633-106">Returns the dimensions of the resource.</span></span>

## <a name="syntax"></a><span data-ttu-id="ed633-107">語法</span><span class="sxs-lookup"><span data-stu-id="ed633-107">Syntax</span></span>

``` syntax
void GetDimensions(
  out UINT Width,
  out UINT Height,
  out UINT Depth
);
```

## <a name="parameters"></a><span data-ttu-id="ed633-108">參數</span><span class="sxs-lookup"><span data-stu-id="ed633-108">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="ed633-109">*寬度* \[擴展\]</span><span class="sxs-lookup"><span data-stu-id="ed633-109">*Width* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="ed633-110">類型： **[ **UINT**](/windows/desktop/WinProg/windows-data-types)**</span><span class="sxs-lookup"><span data-stu-id="ed633-110">Type: **[**UINT**](/windows/desktop/WinProg/windows-data-types)**</span></span>

<span data-ttu-id="ed633-111">資源寬度，以材質。</span><span class="sxs-lookup"><span data-stu-id="ed633-111">The resource width, in texels.</span></span>

</dd> <dt>

<span data-ttu-id="ed633-112">*高度* \[擴展\]</span><span class="sxs-lookup"><span data-stu-id="ed633-112">*Height* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="ed633-113">類型： **[ **UINT**](/windows/desktop/WinProg/windows-data-types)**</span><span class="sxs-lookup"><span data-stu-id="ed633-113">Type: **[**UINT**](/windows/desktop/WinProg/windows-data-types)**</span></span>

<span data-ttu-id="ed633-114">資源高度，以材質。</span><span class="sxs-lookup"><span data-stu-id="ed633-114">The resource height, in texels.</span></span>

</dd> <dt>

<span data-ttu-id="ed633-115">*深度* \[擴展\]</span><span class="sxs-lookup"><span data-stu-id="ed633-115">*Depth* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="ed633-116">類型： **[ **UINT**](/windows/desktop/WinProg/windows-data-types)**</span><span class="sxs-lookup"><span data-stu-id="ed633-116">Type: **[**UINT**](/windows/desktop/WinProg/windows-data-types)**</span></span>

<span data-ttu-id="ed633-117">資源深度，以材質。</span><span class="sxs-lookup"><span data-stu-id="ed633-117">The resource depth, in texels.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="ed633-118">傳回值</span><span class="sxs-lookup"><span data-stu-id="ed633-118">Return value</span></span>

<span data-ttu-id="ed633-119">此函式不會傳回值。</span><span class="sxs-lookup"><span data-stu-id="ed633-119">This function does not return a value.</span></span>

## <a name="remarks"></a><span data-ttu-id="ed633-120">備註</span><span class="sxs-lookup"><span data-stu-id="ed633-120">Remarks</span></span>

<span data-ttu-id="ed633-121">這是此方法的多載版本清單。</span><span class="sxs-lookup"><span data-stu-id="ed633-121">This is a list of the overloaded versions of this method.</span></span>


```
void GetDimensions (out UINT Width,
  out UINT Height,
  out UINT Depth);

void GetDimensions(out float Width,
  out float Height,
  out float Depth);
```



<span data-ttu-id="ed633-122">下列著色器類型支援此函數：</span><span class="sxs-lookup"><span data-stu-id="ed633-122">This function is supported for the following types of shaders:</span></span>



| <span data-ttu-id="ed633-123">頂點</span><span class="sxs-lookup"><span data-stu-id="ed633-123">Vertex</span></span> | <span data-ttu-id="ed633-124">船體</span><span class="sxs-lookup"><span data-stu-id="ed633-124">Hull</span></span> | <span data-ttu-id="ed633-125">網域</span><span class="sxs-lookup"><span data-stu-id="ed633-125">Domain</span></span> | <span data-ttu-id="ed633-126">幾何</span><span class="sxs-lookup"><span data-stu-id="ed633-126">Geometry</span></span> | <span data-ttu-id="ed633-127">像素</span><span class="sxs-lookup"><span data-stu-id="ed633-127">Pixel</span></span> | <span data-ttu-id="ed633-128">計算</span><span class="sxs-lookup"><span data-stu-id="ed633-128">Compute</span></span> |
|--------|------|--------|----------|-------|---------|
|        |      |        |          | <span data-ttu-id="ed633-129">x</span><span class="sxs-lookup"><span data-stu-id="ed633-129">x</span></span>     | <span data-ttu-id="ed633-130">x</span><span class="sxs-lookup"><span data-stu-id="ed633-130">x</span></span>       |



 

## <a name="see-also"></a><span data-ttu-id="ed633-131">另請參閱</span><span class="sxs-lookup"><span data-stu-id="ed633-131">See also</span></span>

<dl> <dt>

[<span data-ttu-id="ed633-132">RWTexture3D</span><span class="sxs-lookup"><span data-stu-id="ed633-132">RWTexture3D</span></span>](sm5-object-rwtexture3d.md)
</dt> <dt>

[<span data-ttu-id="ed633-133">著色器模型5</span><span class="sxs-lookup"><span data-stu-id="ed633-133">Shader Model 5</span></span>](d3d11-graphics-reference-sm5.md)
</dt> </dl>

 

 
