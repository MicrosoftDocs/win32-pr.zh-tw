---
title: Texture2DArray：： GetDimensions 函數
description: 傳回資源的維度。 |Texture2DArray：： GetDimensions 函數
ms.assetid: 0f6d88b3-195d-4f8c-ac31-ac90129a233e
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
ms.openlocfilehash: b3a78bd12f6924c85d4d395c3cdf73443ae51478
ms.sourcegitcommit: 92e74c99f8f4d097676959d0c317f533c2400a80
ms.translationtype: HT
ms.contentlocale: zh-TW
ms.lasthandoff: 03/09/2021
ms.locfileid: "104973908"
---
# <a name="texture2darraygetdimensions-function"></a><span data-ttu-id="8a55f-105">Texture2DArray：： GetDimensions 函數</span><span class="sxs-lookup"><span data-stu-id="8a55f-105">Texture2DArray::GetDimensions function</span></span>

<span data-ttu-id="8a55f-106">傳回資源的維度。</span><span class="sxs-lookup"><span data-stu-id="8a55f-106">Returns the dimensions of the resource.</span></span>

## <a name="syntax"></a><span data-ttu-id="8a55f-107">語法</span><span class="sxs-lookup"><span data-stu-id="8a55f-107">Syntax</span></span>

``` syntax
void GetDimensions(
  in  UINT MipLevel,
  out UINT Width,
  out UINT Height,
  out UINT Elements,
  out UINT NumberOfLevels
);
```

## <a name="parameters"></a><span data-ttu-id="8a55f-108">參數</span><span class="sxs-lookup"><span data-stu-id="8a55f-108">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="8a55f-109">*MipLevel* \[在\]</span><span class="sxs-lookup"><span data-stu-id="8a55f-109">*MipLevel* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="8a55f-110">類型： **[ **UINT**](/windows/desktop/WinProg/windows-data-types)**</span><span class="sxs-lookup"><span data-stu-id="8a55f-110">Type: **[**UINT**](/windows/desktop/WinProg/windows-data-types)**</span></span>

<span data-ttu-id="8a55f-111">選擇性。</span><span class="sxs-lookup"><span data-stu-id="8a55f-111">Optional.</span></span> <span data-ttu-id="8a55f-112">如果) 使用 *NumberOfLevels* ，則必須指定 mipmap 層級 (。</span><span class="sxs-lookup"><span data-stu-id="8a55f-112">The mipmap level (must be specified if *NumberOfLevels* is used).</span></span>

</dd> <dt>

<span data-ttu-id="8a55f-113">*寬度* \[擴展\]</span><span class="sxs-lookup"><span data-stu-id="8a55f-113">*Width* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="8a55f-114">類型： **[ **UINT**](/windows/desktop/WinProg/windows-data-types)**</span><span class="sxs-lookup"><span data-stu-id="8a55f-114">Type: **[**UINT**](/windows/desktop/WinProg/windows-data-types)**</span></span>

<span data-ttu-id="8a55f-115">資源寬度，以材質。</span><span class="sxs-lookup"><span data-stu-id="8a55f-115">The resource width, in texels.</span></span>

</dd> <dt>

<span data-ttu-id="8a55f-116">*高度* \[擴展\]</span><span class="sxs-lookup"><span data-stu-id="8a55f-116">*Height* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="8a55f-117">類型： **[ **UINT**](/windows/desktop/WinProg/windows-data-types)**</span><span class="sxs-lookup"><span data-stu-id="8a55f-117">Type: **[**UINT**](/windows/desktop/WinProg/windows-data-types)**</span></span>

<span data-ttu-id="8a55f-118">資源高度，以材質。</span><span class="sxs-lookup"><span data-stu-id="8a55f-118">The resource height, in texels.</span></span>

</dd> <dt>

<span data-ttu-id="8a55f-119">*元素* \[擴展\]</span><span class="sxs-lookup"><span data-stu-id="8a55f-119">*Elements* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="8a55f-120">類型： **[ **UINT**](/windows/desktop/WinProg/windows-data-types)**</span><span class="sxs-lookup"><span data-stu-id="8a55f-120">Type: **[**UINT**](/windows/desktop/WinProg/windows-data-types)**</span></span>

<span data-ttu-id="8a55f-121">陣列中的項目數。</span><span class="sxs-lookup"><span data-stu-id="8a55f-121">The number of elements in the array.</span></span>

</dd> <dt>

<span data-ttu-id="8a55f-122">*NumberOfLevels* \[擴展\]</span><span class="sxs-lookup"><span data-stu-id="8a55f-122">*NumberOfLevels* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="8a55f-123">類型： **[ **UINT**](/windows/desktop/WinProg/windows-data-types)**</span><span class="sxs-lookup"><span data-stu-id="8a55f-123">Type: **[**UINT**](/windows/desktop/WinProg/windows-data-types)**</span></span>

<span data-ttu-id="8a55f-124"> (的 mipmap 層級數目需要 *MipLevel* 也) 。</span><span class="sxs-lookup"><span data-stu-id="8a55f-124">The number of mipmap levels (requires *MipLevel* also).</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="8a55f-125">傳回值</span><span class="sxs-lookup"><span data-stu-id="8a55f-125">Return value</span></span>

<span data-ttu-id="8a55f-126">Nothing</span><span class="sxs-lookup"><span data-stu-id="8a55f-126">Nothing</span></span>

## <a name="remarks"></a><span data-ttu-id="8a55f-127">備註</span><span class="sxs-lookup"><span data-stu-id="8a55f-127">Remarks</span></span>

<span data-ttu-id="8a55f-128">這是此方法的多載版本清單。</span><span class="sxs-lookup"><span data-stu-id="8a55f-128">This is a list of the overloaded versions of this method.</span></span>


```
void GetDimensions(UINT MipLevel, 
  out UINT Width,
  out UINT Height,
  out UINT Elements,
  out UINT NumberOfLevels);

void GetDimensions (out UINT Width,
  out float Height,
  out float Elements);

void GetDimensions(UINT MipLevel,
  out float Width,
  out float Height,
  out float Elements,
  out float NumberOfLevels);

void GetDimensions(out float Width,
  out float Height,
  out float Elements);
```



<span data-ttu-id="8a55f-129">下列著色器類型支援此函數：</span><span class="sxs-lookup"><span data-stu-id="8a55f-129">This function is supported for the following types of shaders:</span></span>



| <span data-ttu-id="8a55f-130">頂點</span><span class="sxs-lookup"><span data-stu-id="8a55f-130">Vertex</span></span> | <span data-ttu-id="8a55f-131">船體</span><span class="sxs-lookup"><span data-stu-id="8a55f-131">Hull</span></span> | <span data-ttu-id="8a55f-132">網域</span><span class="sxs-lookup"><span data-stu-id="8a55f-132">Domain</span></span> | <span data-ttu-id="8a55f-133">幾何</span><span class="sxs-lookup"><span data-stu-id="8a55f-133">Geometry</span></span> | <span data-ttu-id="8a55f-134">像素</span><span class="sxs-lookup"><span data-stu-id="8a55f-134">Pixel</span></span> | <span data-ttu-id="8a55f-135">計算</span><span class="sxs-lookup"><span data-stu-id="8a55f-135">Compute</span></span> |
|--------|------|--------|----------|-------|---------|
|        |      |        |          | <span data-ttu-id="8a55f-136">x</span><span class="sxs-lookup"><span data-stu-id="8a55f-136">x</span></span>     | <span data-ttu-id="8a55f-137">x</span><span class="sxs-lookup"><span data-stu-id="8a55f-137">x</span></span>       |



 

## <a name="see-also"></a><span data-ttu-id="8a55f-138">另請參閱</span><span class="sxs-lookup"><span data-stu-id="8a55f-138">See also</span></span>

<dl> <dt>

[<span data-ttu-id="8a55f-139">Texture2DArray</span><span class="sxs-lookup"><span data-stu-id="8a55f-139">Texture2DArray</span></span>](sm5-object-texture2darray.md)
</dt> <dt>

[<span data-ttu-id="8a55f-140">著色器模型5</span><span class="sxs-lookup"><span data-stu-id="8a55f-140">Shader Model 5</span></span>](d3d11-graphics-reference-sm5.md)
</dt> </dl>

 

 
