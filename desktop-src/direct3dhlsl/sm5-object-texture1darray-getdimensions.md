---
title: Texture1DArray：： GetDimensions 函數
description: 傳回資源的維度。 |Texture1DArray：： GetDimensions 函數
ms.assetid: a15f1808-296d-43ac-80c0-5cbec0bcb801
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
ms.openlocfilehash: 46cc7e93fc01e14ff34091da4549308730d7cd7c
ms.sourcegitcommit: 92e74c99f8f4d097676959d0c317f533c2400a80
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 03/09/2021
ms.locfileid: "103696458"
---
# <a name="texture1darraygetdimensions-function"></a><span data-ttu-id="b0f65-105">Texture1DArray：： GetDimensions 函數</span><span class="sxs-lookup"><span data-stu-id="b0f65-105">Texture1DArray::GetDimensions function</span></span>

<span data-ttu-id="b0f65-106">傳回資源的維度。</span><span class="sxs-lookup"><span data-stu-id="b0f65-106">Returns the dimensions of the resource.</span></span>

## <a name="syntax"></a><span data-ttu-id="b0f65-107">語法</span><span class="sxs-lookup"><span data-stu-id="b0f65-107">Syntax</span></span>

``` syntax
void GetDimensions(
  in  UINT MipLevel,
  out UINT Width,
  out UINT Elements,
  out UINT NumberOfLevels
);
```

## <a name="parameters"></a><span data-ttu-id="b0f65-108">參數</span><span class="sxs-lookup"><span data-stu-id="b0f65-108">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="b0f65-109">*MipLevel* \[在\]</span><span class="sxs-lookup"><span data-stu-id="b0f65-109">*MipLevel* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="b0f65-110">類型： **[ **UINT**](/windows/desktop/WinProg/windows-data-types)**</span><span class="sxs-lookup"><span data-stu-id="b0f65-110">Type: **[**UINT**](/windows/desktop/WinProg/windows-data-types)**</span></span>

<span data-ttu-id="b0f65-111">選擇性。</span><span class="sxs-lookup"><span data-stu-id="b0f65-111">Optional.</span></span> <span data-ttu-id="b0f65-112">如果) 使用 *NumberOfLevels* ，則必須指定 Mipmap 層級 (。</span><span class="sxs-lookup"><span data-stu-id="b0f65-112">Mipmap level (must be specified if *NumberOfLevels* is used).</span></span>

</dd> <dt>

<span data-ttu-id="b0f65-113">*寬度* \[擴展\]</span><span class="sxs-lookup"><span data-stu-id="b0f65-113">*Width* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="b0f65-114">類型： **[ **UINT**](/windows/desktop/WinProg/windows-data-types)**</span><span class="sxs-lookup"><span data-stu-id="b0f65-114">Type: **[**UINT**](/windows/desktop/WinProg/windows-data-types)**</span></span>

<span data-ttu-id="b0f65-115">資源寬度，以材質。</span><span class="sxs-lookup"><span data-stu-id="b0f65-115">The resource width, in texels.</span></span>

</dd> <dt>

<span data-ttu-id="b0f65-116">*元素* \[擴展\]</span><span class="sxs-lookup"><span data-stu-id="b0f65-116">*Elements* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="b0f65-117">類型： **[ **UINT**](/windows/desktop/WinProg/windows-data-types)**</span><span class="sxs-lookup"><span data-stu-id="b0f65-117">Type: **[**UINT**](/windows/desktop/WinProg/windows-data-types)**</span></span>

<span data-ttu-id="b0f65-118">陣列中的項目數。</span><span class="sxs-lookup"><span data-stu-id="b0f65-118">The number of elements in the array.</span></span>

</dd> <dt>

<span data-ttu-id="b0f65-119">*NumberOfLevels* \[擴展\]</span><span class="sxs-lookup"><span data-stu-id="b0f65-119">*NumberOfLevels* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="b0f65-120">類型： **[ **UINT**](/windows/desktop/WinProg/windows-data-types)**</span><span class="sxs-lookup"><span data-stu-id="b0f65-120">Type: **[**UINT**](/windows/desktop/WinProg/windows-data-types)**</span></span>

<span data-ttu-id="b0f65-121"> (的 mipmap 層級數目需要 *MipLevel* 也) 。</span><span class="sxs-lookup"><span data-stu-id="b0f65-121">The number of mipmap levels (requires *MipLevel* also).</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="b0f65-122">傳回值</span><span class="sxs-lookup"><span data-stu-id="b0f65-122">Return value</span></span>

<span data-ttu-id="b0f65-123">此函式不會傳回值。</span><span class="sxs-lookup"><span data-stu-id="b0f65-123">This function does not return a value.</span></span>

## <a name="remarks"></a><span data-ttu-id="b0f65-124">備註</span><span class="sxs-lookup"><span data-stu-id="b0f65-124">Remarks</span></span>

<span data-ttu-id="b0f65-125">這是此方法的多載版本清單。</span><span class="sxs-lookup"><span data-stu-id="b0f65-125">This is a list of the overloaded versions of this method.</span></span>


```
void GetDimensions(UINT MipLevel, 
  out UINT Width,
  out UINT Elements,
  out UINT NumberOfLevels);

void GetDimensions (out UINT Width,
  out UINT Elements);

void GetDimensions(UINT MipLevel,
  out float Width,
  out UINT Elements,
  out float NumberOfLevels);

void GetDimensions(out float Width,
  out UINT Elements);
```



<span data-ttu-id="b0f65-126">下列著色器類型支援此函數：</span><span class="sxs-lookup"><span data-stu-id="b0f65-126">This function is supported for the following types of shaders:</span></span>



| <span data-ttu-id="b0f65-127">頂點</span><span class="sxs-lookup"><span data-stu-id="b0f65-127">Vertex</span></span> | <span data-ttu-id="b0f65-128">船體</span><span class="sxs-lookup"><span data-stu-id="b0f65-128">Hull</span></span> | <span data-ttu-id="b0f65-129">網域</span><span class="sxs-lookup"><span data-stu-id="b0f65-129">Domain</span></span> | <span data-ttu-id="b0f65-130">幾何</span><span class="sxs-lookup"><span data-stu-id="b0f65-130">Geometry</span></span> | <span data-ttu-id="b0f65-131">像素</span><span class="sxs-lookup"><span data-stu-id="b0f65-131">Pixel</span></span> | <span data-ttu-id="b0f65-132">計算</span><span class="sxs-lookup"><span data-stu-id="b0f65-132">Compute</span></span> |
|--------|------|--------|----------|-------|---------|
|        |      |        |          | <span data-ttu-id="b0f65-133">x</span><span class="sxs-lookup"><span data-stu-id="b0f65-133">x</span></span>     | <span data-ttu-id="b0f65-134">x</span><span class="sxs-lookup"><span data-stu-id="b0f65-134">x</span></span>       |



 

## <a name="see-also"></a><span data-ttu-id="b0f65-135">另請參閱</span><span class="sxs-lookup"><span data-stu-id="b0f65-135">See also</span></span>

<dl> <dt>

[<span data-ttu-id="b0f65-136">Texture1DArray</span><span class="sxs-lookup"><span data-stu-id="b0f65-136">Texture1DArray</span></span>](sm5-object-texture1darray.md)
</dt> <dt>

[<span data-ttu-id="b0f65-137">著色器模型5</span><span class="sxs-lookup"><span data-stu-id="b0f65-137">Shader Model 5</span></span>](d3d11-graphics-reference-sm5.md)
</dt> </dl>

 

 
