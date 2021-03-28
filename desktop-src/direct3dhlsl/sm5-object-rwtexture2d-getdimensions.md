---
title: RWTexture2D：： GetDimensions 函數
description: 傳回資源的維度。 |RWTexture2D：： GetDimensions 函數
ms.assetid: bc55622d-fbff-4aeb-aceb-4eb2cfc7ac28
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
ms.openlocfilehash: 19a6711e8f04afdb2f5ec66ff33c8aaf1d59b40c
ms.sourcegitcommit: 92e74c99f8f4d097676959d0c317f533c2400a80
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 03/09/2021
ms.locfileid: "104116148"
---
# <a name="rwtexture2dgetdimensions-function"></a><span data-ttu-id="b4e64-105">RWTexture2D：： GetDimensions 函數</span><span class="sxs-lookup"><span data-stu-id="b4e64-105">RWTexture2D::GetDimensions function</span></span>

<span data-ttu-id="b4e64-106">傳回資源的維度。</span><span class="sxs-lookup"><span data-stu-id="b4e64-106">Returns the dimensions of the resource.</span></span>

## <a name="syntax"></a><span data-ttu-id="b4e64-107">語法</span><span class="sxs-lookup"><span data-stu-id="b4e64-107">Syntax</span></span>

``` syntax
void GetDimensions(
  out UINT Width,
  out UINT Height
);
```

## <a name="parameters"></a><span data-ttu-id="b4e64-108">參數</span><span class="sxs-lookup"><span data-stu-id="b4e64-108">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="b4e64-109">*寬度* \[擴展\]</span><span class="sxs-lookup"><span data-stu-id="b4e64-109">*Width* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="b4e64-110">類型： **[ **UINT**](/windows/desktop/WinProg/windows-data-types)**</span><span class="sxs-lookup"><span data-stu-id="b4e64-110">Type: **[**UINT**](/windows/desktop/WinProg/windows-data-types)**</span></span>

<span data-ttu-id="b4e64-111">資源寬度，以材質。</span><span class="sxs-lookup"><span data-stu-id="b4e64-111">The resource width, in texels.</span></span>

</dd> <dt>

<span data-ttu-id="b4e64-112">*高度* \[擴展\]</span><span class="sxs-lookup"><span data-stu-id="b4e64-112">*Height* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="b4e64-113">類型： **[ **UINT**](/windows/desktop/WinProg/windows-data-types)**</span><span class="sxs-lookup"><span data-stu-id="b4e64-113">Type: **[**UINT**](/windows/desktop/WinProg/windows-data-types)**</span></span>

<span data-ttu-id="b4e64-114">資源高度，以材質。</span><span class="sxs-lookup"><span data-stu-id="b4e64-114">The resource height, in texels.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="b4e64-115">傳回值</span><span class="sxs-lookup"><span data-stu-id="b4e64-115">Return value</span></span>

<span data-ttu-id="b4e64-116">此函式不會傳回值。</span><span class="sxs-lookup"><span data-stu-id="b4e64-116">This function does not return a value.</span></span>

## <a name="remarks"></a><span data-ttu-id="b4e64-117">備註</span><span class="sxs-lookup"><span data-stu-id="b4e64-117">Remarks</span></span>

<span data-ttu-id="b4e64-118">這是此方法的多載版本清單。</span><span class="sxs-lookup"><span data-stu-id="b4e64-118">This is a list of the overloaded versions of this method.</span></span>


```
void GetDimensions (out UINT Width,
  out UINT Height);

void GetDimensions(out float Width,
  out float Height);
```



<span data-ttu-id="b4e64-119">下列著色器類型支援此函數：</span><span class="sxs-lookup"><span data-stu-id="b4e64-119">This function is supported for the following types of shaders:</span></span>



| <span data-ttu-id="b4e64-120">頂點</span><span class="sxs-lookup"><span data-stu-id="b4e64-120">Vertex</span></span> | <span data-ttu-id="b4e64-121">船體</span><span class="sxs-lookup"><span data-stu-id="b4e64-121">Hull</span></span> | <span data-ttu-id="b4e64-122">網域</span><span class="sxs-lookup"><span data-stu-id="b4e64-122">Domain</span></span> | <span data-ttu-id="b4e64-123">幾何</span><span class="sxs-lookup"><span data-stu-id="b4e64-123">Geometry</span></span> | <span data-ttu-id="b4e64-124">像素</span><span class="sxs-lookup"><span data-stu-id="b4e64-124">Pixel</span></span> | <span data-ttu-id="b4e64-125">計算</span><span class="sxs-lookup"><span data-stu-id="b4e64-125">Compute</span></span> |
|--------|------|--------|----------|-------|---------|
|        |      |        |          | <span data-ttu-id="b4e64-126">x</span><span class="sxs-lookup"><span data-stu-id="b4e64-126">x</span></span>     | <span data-ttu-id="b4e64-127">x</span><span class="sxs-lookup"><span data-stu-id="b4e64-127">x</span></span>       |



 

## <a name="see-also"></a><span data-ttu-id="b4e64-128">另請參閱</span><span class="sxs-lookup"><span data-stu-id="b4e64-128">See also</span></span>

<dl> <dt>

[<span data-ttu-id="b4e64-129">RWTexture2D</span><span class="sxs-lookup"><span data-stu-id="b4e64-129">RWTexture2D</span></span>](sm5-object-rwtexture2d.md)
</dt> <dt>

[<span data-ttu-id="b4e64-130">著色器模型5</span><span class="sxs-lookup"><span data-stu-id="b4e64-130">Shader Model 5</span></span>](d3d11-graphics-reference-sm5.md)
</dt> </dl>

 

 
