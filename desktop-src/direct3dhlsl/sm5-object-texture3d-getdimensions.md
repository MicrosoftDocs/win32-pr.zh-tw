---
title: Texture3D：： GetDimensions 函數
description: 傳回資源的維度。 |Texture3D：： GetDimensions 函數
ms.assetid: 4a08f14f-7489-4ed1-bf94-4f63f1002eab
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
ms.openlocfilehash: 7a700e0ff065e5f4758241ee0c8252965209a21f
ms.sourcegitcommit: 92e74c99f8f4d097676959d0c317f533c2400a80
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 03/09/2021
ms.locfileid: "104992107"
---
# <a name="texture3dgetdimensions-function"></a><span data-ttu-id="e9b38-105">Texture3D：： GetDimensions 函數</span><span class="sxs-lookup"><span data-stu-id="e9b38-105">Texture3D::GetDimensions function</span></span>

<span data-ttu-id="e9b38-106">傳回資源的維度。</span><span class="sxs-lookup"><span data-stu-id="e9b38-106">Returns the dimensions of the resource.</span></span>

## <a name="syntax"></a><span data-ttu-id="e9b38-107">語法</span><span class="sxs-lookup"><span data-stu-id="e9b38-107">Syntax</span></span>

``` syntax
void GetDimensions(
  in  UINT MipLevel,
  out UINT Width,
  out UINT Height,
  out UINT Depth,
  out UINT NumberOfLevels
);
```

## <a name="parameters"></a><span data-ttu-id="e9b38-108">參數</span><span class="sxs-lookup"><span data-stu-id="e9b38-108">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="e9b38-109">*MipLevel* \[在\]</span><span class="sxs-lookup"><span data-stu-id="e9b38-109">*MipLevel* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="e9b38-110">類型： **[ **UINT**](/windows/desktop/WinProg/windows-data-types)**</span><span class="sxs-lookup"><span data-stu-id="e9b38-110">Type: **[**UINT**](/windows/desktop/WinProg/windows-data-types)**</span></span>

<span data-ttu-id="e9b38-111">選擇性。</span><span class="sxs-lookup"><span data-stu-id="e9b38-111">Optional.</span></span> <span data-ttu-id="e9b38-112">如果) 使用 *NumberOfLevels* ，則必須指定 Mipmap 層級 (。</span><span class="sxs-lookup"><span data-stu-id="e9b38-112">Mipmap level (must be specified if *NumberOfLevels* is used).</span></span>

</dd> <dt>

<span data-ttu-id="e9b38-113">*寬度* \[擴展\]</span><span class="sxs-lookup"><span data-stu-id="e9b38-113">*Width* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="e9b38-114">類型： **[ **UINT**](/windows/desktop/WinProg/windows-data-types)**</span><span class="sxs-lookup"><span data-stu-id="e9b38-114">Type: **[**UINT**](/windows/desktop/WinProg/windows-data-types)**</span></span>

<span data-ttu-id="e9b38-115">資源寬度，以材質。</span><span class="sxs-lookup"><span data-stu-id="e9b38-115">The resource width, in texels.</span></span>

</dd> <dt>

<span data-ttu-id="e9b38-116">*高度* \[擴展\]</span><span class="sxs-lookup"><span data-stu-id="e9b38-116">*Height* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="e9b38-117">類型： **[ **UINT**](/windows/desktop/WinProg/windows-data-types)**</span><span class="sxs-lookup"><span data-stu-id="e9b38-117">Type: **[**UINT**](/windows/desktop/WinProg/windows-data-types)**</span></span>

<span data-ttu-id="e9b38-118">資源高度，以材質。</span><span class="sxs-lookup"><span data-stu-id="e9b38-118">The resource height, in texels.</span></span>

</dd> <dt>

<span data-ttu-id="e9b38-119">*深度* \[擴展\]</span><span class="sxs-lookup"><span data-stu-id="e9b38-119">*Depth* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="e9b38-120">類型： **[ **UINT**](/windows/desktop/WinProg/windows-data-types)**</span><span class="sxs-lookup"><span data-stu-id="e9b38-120">Type: **[**UINT**](/windows/desktop/WinProg/windows-data-types)**</span></span>

<span data-ttu-id="e9b38-121">資源深度，以材質。</span><span class="sxs-lookup"><span data-stu-id="e9b38-121">The resource depth, in texels.</span></span>

</dd> <dt>

<span data-ttu-id="e9b38-122">*NumberOfLevels* \[擴展\]</span><span class="sxs-lookup"><span data-stu-id="e9b38-122">*NumberOfLevels* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="e9b38-123">類型： **[ **UINT**](/windows/desktop/WinProg/windows-data-types)**</span><span class="sxs-lookup"><span data-stu-id="e9b38-123">Type: **[**UINT**](/windows/desktop/WinProg/windows-data-types)**</span></span>

<span data-ttu-id="e9b38-124"> (的 mipmap 層級數目需要 *MipLevel* 也) 。</span><span class="sxs-lookup"><span data-stu-id="e9b38-124">The number of mipmap levels (requires *MipLevel* also).</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="e9b38-125">傳回值</span><span class="sxs-lookup"><span data-stu-id="e9b38-125">Return value</span></span>

<span data-ttu-id="e9b38-126">Nothing</span><span class="sxs-lookup"><span data-stu-id="e9b38-126">Nothing</span></span>

## <a name="remarks"></a><span data-ttu-id="e9b38-127">備註</span><span class="sxs-lookup"><span data-stu-id="e9b38-127">Remarks</span></span>

<span data-ttu-id="e9b38-128">這是此方法的多載版本清單。</span><span class="sxs-lookup"><span data-stu-id="e9b38-128">This is a list of the overloaded versions of this method.</span></span>


```
void GetDimensions(UINT MipLevel, 
  out UINT Width,
  out UINT Height,
  out UINT Depth,
  out UINT NumberOfLevels);

void GetDimensions (out UINT Width,
  out UINT Height,
  out UINT Depth);

void GetDimensions(UINT MipLevel,
  out float Width,
  out float Height,
  out float Depth,
  out float NumberOfLevels);

void GetDimensions(out float Width,
  out float Height,
  out float Depth);
```



<span data-ttu-id="e9b38-129">下列著色器類型支援此函數：</span><span class="sxs-lookup"><span data-stu-id="e9b38-129">This function is supported for the following types of shaders:</span></span>



| <span data-ttu-id="e9b38-130">頂點</span><span class="sxs-lookup"><span data-stu-id="e9b38-130">Vertex</span></span> | <span data-ttu-id="e9b38-131">船體</span><span class="sxs-lookup"><span data-stu-id="e9b38-131">Hull</span></span> | <span data-ttu-id="e9b38-132">網域</span><span class="sxs-lookup"><span data-stu-id="e9b38-132">Domain</span></span> | <span data-ttu-id="e9b38-133">幾何</span><span class="sxs-lookup"><span data-stu-id="e9b38-133">Geometry</span></span> | <span data-ttu-id="e9b38-134">像素</span><span class="sxs-lookup"><span data-stu-id="e9b38-134">Pixel</span></span> | <span data-ttu-id="e9b38-135">計算</span><span class="sxs-lookup"><span data-stu-id="e9b38-135">Compute</span></span> |
|--------|------|--------|----------|-------|---------|
|        |      |        |          | <span data-ttu-id="e9b38-136">x</span><span class="sxs-lookup"><span data-stu-id="e9b38-136">x</span></span>     | <span data-ttu-id="e9b38-137">x</span><span class="sxs-lookup"><span data-stu-id="e9b38-137">x</span></span>       |



 

## <a name="see-also"></a><span data-ttu-id="e9b38-138">另請參閱</span><span class="sxs-lookup"><span data-stu-id="e9b38-138">See also</span></span>

<dl> <dt>

[<span data-ttu-id="e9b38-139">Texture3D</span><span class="sxs-lookup"><span data-stu-id="e9b38-139">Texture3D</span></span>](sm5-object-texture3d.md)
</dt> <dt>

[<span data-ttu-id="e9b38-140">著色器模型5</span><span class="sxs-lookup"><span data-stu-id="e9b38-140">Shader Model 5</span></span>](d3d11-graphics-reference-sm5.md)
</dt> </dl>

 

 
