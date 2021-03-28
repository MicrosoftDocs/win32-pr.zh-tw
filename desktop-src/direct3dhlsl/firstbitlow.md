---
title: firstbitlow 函式
description: 傳回第一個設定位的位置，從最小的順序位開始，然後每個元件向上處理。
ms.assetid: 204250f3-1a9b-445d-bd16-4cc9a5d9d60a
keywords:
- firstbitlow 函式 HLSL
topic_type:
- apiref
api_name:
- firstbitlow
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
api_location: ''
ms.openlocfilehash: a647314383bc022b7c3b3e1b5a255a42a099c620
ms.sourcegitcommit: 592c9bbd22ba69802dc353bcb5eb30699f9e9403
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/20/2020
ms.locfileid: "104023669"
---
# <a name="firstbitlow-function"></a><span data-ttu-id="019d2-104">firstbitlow 函式</span><span class="sxs-lookup"><span data-stu-id="019d2-104">firstbitlow function</span></span>

<span data-ttu-id="019d2-105">傳回第一個設定位的位置，從最小的順序位開始，然後每個元件向上處理。</span><span class="sxs-lookup"><span data-stu-id="019d2-105">Returns the location of the first set bit starting from the lowest order bit and working upward, per component.</span></span>

## <a name="syntax"></a><span data-ttu-id="019d2-106">語法</span><span class="sxs-lookup"><span data-stu-id="019d2-106">Syntax</span></span>

``` syntax
int firstbitlow(
  in int value
);
```

## <a name="parameters"></a><span data-ttu-id="019d2-107">參數</span><span class="sxs-lookup"><span data-stu-id="019d2-107">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="019d2-108">*值* \[在\]</span><span class="sxs-lookup"><span data-stu-id="019d2-108">*value* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="019d2-109">類型： **[ **int**](/windows/desktop/WinProg/windows-data-types)**</span><span class="sxs-lookup"><span data-stu-id="019d2-109">Type: **[**int**](/windows/desktop/WinProg/windows-data-types)**</span></span>

<span data-ttu-id="019d2-110">輸入值。</span><span class="sxs-lookup"><span data-stu-id="019d2-110">The input value.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="019d2-111">傳回值</span><span class="sxs-lookup"><span data-stu-id="019d2-111">Return value</span></span>

<span data-ttu-id="019d2-112">類型： **[ **int**](/windows/desktop/WinProg/windows-data-types)**</span><span class="sxs-lookup"><span data-stu-id="019d2-112">Type: **[**int**](/windows/desktop/WinProg/windows-data-types)**</span></span>

<span data-ttu-id="019d2-113">第一個設定位的位置。</span><span class="sxs-lookup"><span data-stu-id="019d2-113">The location of the first set bit.</span></span>

## <a name="remarks"></a><span data-ttu-id="019d2-114">備註</span><span class="sxs-lookup"><span data-stu-id="019d2-114">Remarks</span></span>

<span data-ttu-id="019d2-115">您也可以使用下列多載版本：</span><span class="sxs-lookup"><span data-stu-id="019d2-115">The following overloaded versions are also available:</span></span>

``` syntax
uint2 firstbitlow(uint2 value);
uint3 firstbitlow(uint3 value);
uint4 firstbitlow(uint4 value);
```

### <a name="minimum-shader-model"></a><span data-ttu-id="019d2-116">最小著色器模型</span><span class="sxs-lookup"><span data-stu-id="019d2-116">Minimum Shader Model</span></span>

<span data-ttu-id="019d2-117">下列著色器模型支援此函數。</span><span class="sxs-lookup"><span data-stu-id="019d2-117">This function is supported in the following shader models.</span></span>



| <span data-ttu-id="019d2-118">著色器模型</span><span class="sxs-lookup"><span data-stu-id="019d2-118">Shader Model</span></span>                                                                | <span data-ttu-id="019d2-119">支援</span><span class="sxs-lookup"><span data-stu-id="019d2-119">Supported</span></span> |
|-----------------------------------------------------------------------------|-----------|
| <span data-ttu-id="019d2-120">[著色器模型 5](d3d11-graphics-reference-sm5.md) 和更新版本的著色器模型</span><span class="sxs-lookup"><span data-stu-id="019d2-120">[Shader Model 5](d3d11-graphics-reference-sm5.md) and higher shader models</span></span> | <span data-ttu-id="019d2-121">是</span><span class="sxs-lookup"><span data-stu-id="019d2-121">yes</span></span>       |



 

<span data-ttu-id="019d2-122">下列著色器類型支援此函數：</span><span class="sxs-lookup"><span data-stu-id="019d2-122">This function is supported in the following types of shaders:</span></span>



| <span data-ttu-id="019d2-123">頂點</span><span class="sxs-lookup"><span data-stu-id="019d2-123">Vertex</span></span> | <span data-ttu-id="019d2-124">船體</span><span class="sxs-lookup"><span data-stu-id="019d2-124">Hull</span></span> | <span data-ttu-id="019d2-125">網域</span><span class="sxs-lookup"><span data-stu-id="019d2-125">Domain</span></span> | <span data-ttu-id="019d2-126">幾何</span><span class="sxs-lookup"><span data-stu-id="019d2-126">Geometry</span></span> | <span data-ttu-id="019d2-127">像素</span><span class="sxs-lookup"><span data-stu-id="019d2-127">Pixel</span></span> | <span data-ttu-id="019d2-128">計算</span><span class="sxs-lookup"><span data-stu-id="019d2-128">Compute</span></span> |
|--------|------|--------|----------|-------|---------|
| <span data-ttu-id="019d2-129">x</span><span class="sxs-lookup"><span data-stu-id="019d2-129">x</span></span>      | <span data-ttu-id="019d2-130">x</span><span class="sxs-lookup"><span data-stu-id="019d2-130">x</span></span>    | <span data-ttu-id="019d2-131">x</span><span class="sxs-lookup"><span data-stu-id="019d2-131">x</span></span>      | <span data-ttu-id="019d2-132">x</span><span class="sxs-lookup"><span data-stu-id="019d2-132">x</span></span>        | <span data-ttu-id="019d2-133">x</span><span class="sxs-lookup"><span data-stu-id="019d2-133">x</span></span>     | <span data-ttu-id="019d2-134">x</span><span class="sxs-lookup"><span data-stu-id="019d2-134">x</span></span>       |



 

## <a name="see-also"></a><span data-ttu-id="019d2-135">另請參閱</span><span class="sxs-lookup"><span data-stu-id="019d2-135">See also</span></span>

<dl> <dt>

[<span data-ttu-id="019d2-136">內建函式</span><span class="sxs-lookup"><span data-stu-id="019d2-136">Intrinsic Functions</span></span>](dx-graphics-hlsl-intrinsic-functions.md)
</dt> <dt>

[<span data-ttu-id="019d2-137">著色器模型5</span><span class="sxs-lookup"><span data-stu-id="019d2-137">Shader Model 5</span></span>](d3d11-graphics-reference-sm5.md)
</dt> </dl>

 

 