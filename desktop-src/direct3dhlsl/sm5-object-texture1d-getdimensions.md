---
title: Texture1D：： GetDimensions 函數
description: 傳回資源的維度。 |Texture1D：： GetDimensions 函數
ms.assetid: eb8fc02f-01c8-44b9-9d7e-faf59660c287
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
ms.openlocfilehash: fdd9b79a1cc1fa2a5a8db3e0db7a7163878b066b
ms.sourcegitcommit: 92e74c99f8f4d097676959d0c317f533c2400a80
ms.translationtype: HT
ms.contentlocale: zh-TW
ms.lasthandoff: 03/09/2021
ms.locfileid: "104514464"
---
# <a name="texture1dgetdimensions-function"></a><span data-ttu-id="c2e9d-105">Texture1D：： GetDimensions 函數</span><span class="sxs-lookup"><span data-stu-id="c2e9d-105">Texture1D::GetDimensions function</span></span>

<span data-ttu-id="c2e9d-106">傳回資源的維度。</span><span class="sxs-lookup"><span data-stu-id="c2e9d-106">Returns the dimensions of the resource.</span></span>

## <a name="syntax"></a><span data-ttu-id="c2e9d-107">語法</span><span class="sxs-lookup"><span data-stu-id="c2e9d-107">Syntax</span></span>

``` syntax
void GetDimensions(
  in  UINT MipLevel,
  out UINT Width,
  out UINT NumberOfLevels
);
```

## <a name="parameters"></a><span data-ttu-id="c2e9d-108">參數</span><span class="sxs-lookup"><span data-stu-id="c2e9d-108">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="c2e9d-109">*MipLevel* \[在\]</span><span class="sxs-lookup"><span data-stu-id="c2e9d-109">*MipLevel* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="c2e9d-110">類型： **[ **UINT**](/windows/desktop/WinProg/windows-data-types)**</span><span class="sxs-lookup"><span data-stu-id="c2e9d-110">Type: **[**UINT**](/windows/desktop/WinProg/windows-data-types)**</span></span>

<span data-ttu-id="c2e9d-111">選擇性。</span><span class="sxs-lookup"><span data-stu-id="c2e9d-111">Optional.</span></span> <span data-ttu-id="c2e9d-112">如果) 使用 *NumberOfLevels* ，則必須指定 Mipmap 層級 (。</span><span class="sxs-lookup"><span data-stu-id="c2e9d-112">Mipmap level (must be specified if *NumberOfLevels* is used).</span></span>

</dd> <dt>

<span data-ttu-id="c2e9d-113">*寬度* \[擴展\]</span><span class="sxs-lookup"><span data-stu-id="c2e9d-113">*Width* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="c2e9d-114">類型： **[ **UINT**](/windows/desktop/WinProg/windows-data-types)**</span><span class="sxs-lookup"><span data-stu-id="c2e9d-114">Type: **[**UINT**](/windows/desktop/WinProg/windows-data-types)**</span></span>

<span data-ttu-id="c2e9d-115">資源寬度，以材質。</span><span class="sxs-lookup"><span data-stu-id="c2e9d-115">The resource width, in texels.</span></span>

</dd> <dt>

<span data-ttu-id="c2e9d-116">*NumberOfLevels* \[擴展\]</span><span class="sxs-lookup"><span data-stu-id="c2e9d-116">*NumberOfLevels* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="c2e9d-117">類型： **[ **UINT**](/windows/desktop/WinProg/windows-data-types)**</span><span class="sxs-lookup"><span data-stu-id="c2e9d-117">Type: **[**UINT**](/windows/desktop/WinProg/windows-data-types)**</span></span>

<span data-ttu-id="c2e9d-118"> (的 mipmap 層級數目需要 *MipLevel* 也) 。</span><span class="sxs-lookup"><span data-stu-id="c2e9d-118">The number of mipmap levels (requires *MipLevel* also).</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="c2e9d-119">傳回值</span><span class="sxs-lookup"><span data-stu-id="c2e9d-119">Return value</span></span>

<span data-ttu-id="c2e9d-120">此函式不會傳回值。</span><span class="sxs-lookup"><span data-stu-id="c2e9d-120">This function does not return a value.</span></span>

## <a name="remarks"></a><span data-ttu-id="c2e9d-121">備註</span><span class="sxs-lookup"><span data-stu-id="c2e9d-121">Remarks</span></span>

<span data-ttu-id="c2e9d-122">這是此方法的多載版本清單。</span><span class="sxs-lookup"><span data-stu-id="c2e9d-122">This is a list of the overloaded versions of this method.</span></span>


```
void GetDimensions(UINT MipLevel, 
  out UINT Width,
  out UINT NumberOfLevels);

void GetDimensions (out UINT Width);

void GetDimensions(UINT MipLevel,
  out float Width,
  out float NumberOfLevels);

void GetDimensions(out float Width);
```



<span data-ttu-id="c2e9d-123">下列著色器類型支援此函數：</span><span class="sxs-lookup"><span data-stu-id="c2e9d-123">This function is supported for the following types of shaders:</span></span>



| <span data-ttu-id="c2e9d-124">頂點</span><span class="sxs-lookup"><span data-stu-id="c2e9d-124">Vertex</span></span> | <span data-ttu-id="c2e9d-125">船體</span><span class="sxs-lookup"><span data-stu-id="c2e9d-125">Hull</span></span> | <span data-ttu-id="c2e9d-126">網域</span><span class="sxs-lookup"><span data-stu-id="c2e9d-126">Domain</span></span> | <span data-ttu-id="c2e9d-127">幾何</span><span class="sxs-lookup"><span data-stu-id="c2e9d-127">Geometry</span></span> | <span data-ttu-id="c2e9d-128">像素</span><span class="sxs-lookup"><span data-stu-id="c2e9d-128">Pixel</span></span> | <span data-ttu-id="c2e9d-129">計算</span><span class="sxs-lookup"><span data-stu-id="c2e9d-129">Compute</span></span> |
|--------|------|--------|----------|-------|---------|
|        |      |        |          | <span data-ttu-id="c2e9d-130">x</span><span class="sxs-lookup"><span data-stu-id="c2e9d-130">x</span></span>     | <span data-ttu-id="c2e9d-131">x</span><span class="sxs-lookup"><span data-stu-id="c2e9d-131">x</span></span>       |



 

## <a name="see-also"></a><span data-ttu-id="c2e9d-132">另請參閱</span><span class="sxs-lookup"><span data-stu-id="c2e9d-132">See also</span></span>

<dl> <dt>

[<span data-ttu-id="c2e9d-133">Texture1D</span><span class="sxs-lookup"><span data-stu-id="c2e9d-133">Texture1D</span></span>](sm5-object-texture1d.md)
</dt> <dt>

[<span data-ttu-id="c2e9d-134">著色器模型5</span><span class="sxs-lookup"><span data-stu-id="c2e9d-134">Shader Model 5</span></span>](d3d11-graphics-reference-sm5.md)
</dt> </dl>

 

 
