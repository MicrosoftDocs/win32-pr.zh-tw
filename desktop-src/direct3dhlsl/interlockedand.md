---
title: 'InterlockedAnd 函式 (HLSL 參考) '
description: 執行保證的不可部分完成和。
ms.assetid: 7dc5185a-ea37-493d-975d-dbb803c886d3
keywords:
- InterlockedAnd 函式 HLSL
topic_type:
- apiref
api_name:
- InterlockedAnd
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
api_location: ''
ms.openlocfilehash: 487a7daaffe25e4e8bb22aec5805ded2a8091161
ms.sourcegitcommit: 12e9b14501d51641b690ee0cf764e2b91eb9a140
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 02/06/2020
ms.locfileid: "104990879"
---
# <a name="interlockedand-function-hlsl-reference"></a><span data-ttu-id="d02ad-104">InterlockedAnd 函式 (HLSL 參考) </span><span class="sxs-lookup"><span data-stu-id="d02ad-104">InterlockedAnd function (HLSL reference)</span></span>

<span data-ttu-id="d02ad-105">執行保證的不可部分完成和。</span><span class="sxs-lookup"><span data-stu-id="d02ad-105">Performs a guaranteed atomic and.</span></span>

## <a name="syntax"></a><span data-ttu-id="d02ad-106">語法</span><span class="sxs-lookup"><span data-stu-id="d02ad-106">Syntax</span></span>

``` syntax
void InterlockedAnd(
  in  R dest,
  in  T value,
  out T original_value
);
```

## <a name="parameters"></a><span data-ttu-id="d02ad-107">參數</span><span class="sxs-lookup"><span data-stu-id="d02ad-107">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="d02ad-108">*目的地* \[在\]</span><span class="sxs-lookup"><span data-stu-id="d02ad-108">*dest* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="d02ad-109">類型： **R**</span><span class="sxs-lookup"><span data-stu-id="d02ad-109">Type: **R**</span></span>

<span data-ttu-id="d02ad-110">目的地位址。</span><span class="sxs-lookup"><span data-stu-id="d02ad-110">The destination address.</span></span>

</dd> <dt>

<span data-ttu-id="d02ad-111">*值* \[在\]</span><span class="sxs-lookup"><span data-stu-id="d02ad-111">*value* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="d02ad-112">類型： **T**</span><span class="sxs-lookup"><span data-stu-id="d02ad-112">Type: **T**</span></span>

<span data-ttu-id="d02ad-113">輸入值。</span><span class="sxs-lookup"><span data-stu-id="d02ad-113">The input value.</span></span>

</dd> <dt>

<span data-ttu-id="d02ad-114">*原始 \_ 值* \[ 輸出\]</span><span class="sxs-lookup"><span data-stu-id="d02ad-114">*original\_value* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="d02ad-115">類型： **T**</span><span class="sxs-lookup"><span data-stu-id="d02ad-115">Type: **T**</span></span>

<span data-ttu-id="d02ad-116">選擇性。</span><span class="sxs-lookup"><span data-stu-id="d02ad-116">Optional.</span></span> <span data-ttu-id="d02ad-117">原始的輸入值。</span><span class="sxs-lookup"><span data-stu-id="d02ad-117">The original input value.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="d02ad-118">傳回值</span><span class="sxs-lookup"><span data-stu-id="d02ad-118">Return value</span></span>

<span data-ttu-id="d02ad-119">此函式不會傳回值。</span><span class="sxs-lookup"><span data-stu-id="d02ad-119">This function does not return a value.</span></span>

## <a name="remarks"></a><span data-ttu-id="d02ad-120">備註</span><span class="sxs-lookup"><span data-stu-id="d02ad-120">Remarks</span></span>

<span data-ttu-id="d02ad-121">此作業只能在 int 或 uint 型別資源和共用記憶體變數上執行。</span><span class="sxs-lookup"><span data-stu-id="d02ad-121">This operation can only be performed on int or uint typed resources and shared memory variables.</span></span> <span data-ttu-id="d02ad-122">此函式有兩種可能的用途。</span><span class="sxs-lookup"><span data-stu-id="d02ad-122">There are two possible uses for this function.</span></span> <span data-ttu-id="d02ad-123">第一個是當 R 是共用記憶體變數型別時。</span><span class="sxs-lookup"><span data-stu-id="d02ad-123">The first is when R is a shared memory variable type.</span></span> <span data-ttu-id="d02ad-124">在此情況下，此函式會針對 dest 所參考的共用記憶體暫存器執行不可部分完成的值。</span><span class="sxs-lookup"><span data-stu-id="d02ad-124">In this case, the function performs an atomic and of value to the shared memory register referenced by dest.</span></span> <span data-ttu-id="d02ad-125">第二個案例是 R 是資源變數類型。</span><span class="sxs-lookup"><span data-stu-id="d02ad-125">The second scenario is when R is a resource variable type.</span></span> <span data-ttu-id="d02ad-126">在此案例中，此函式會針對 dest 所參考的資源位置執行不可部分完成的值。</span><span class="sxs-lookup"><span data-stu-id="d02ad-126">In this scenario, the function performs an atomic and of value to the resource location referenced by dest.</span></span> <span data-ttu-id="d02ad-127">多載函式有額外的輸出變數，其會設定為目的地的原始值。</span><span class="sxs-lookup"><span data-stu-id="d02ad-127">The overloaded function has an additional output variable which will be set to the original value of dest.</span></span> <span data-ttu-id="d02ad-128">只有在 R 可讀取和可寫入時，才能使用此多載作業。</span><span class="sxs-lookup"><span data-stu-id="d02ad-128">This overloaded operation is only available when R is readable and writable.</span></span>

### <a name="minimum-shader-model"></a><span data-ttu-id="d02ad-129">最小著色器模型</span><span class="sxs-lookup"><span data-stu-id="d02ad-129">Minimum Shader Model</span></span>

<span data-ttu-id="d02ad-130">下列著色器模型支援此函數。</span><span class="sxs-lookup"><span data-stu-id="d02ad-130">This function is supported in the following shader models.</span></span>



| <span data-ttu-id="d02ad-131">著色器模型</span><span class="sxs-lookup"><span data-stu-id="d02ad-131">Shader Model</span></span>                                                                | <span data-ttu-id="d02ad-132">支援</span><span class="sxs-lookup"><span data-stu-id="d02ad-132">Supported</span></span> |
|-----------------------------------------------------------------------------|-----------|
| <span data-ttu-id="d02ad-133">[著色器模型 5](d3d11-graphics-reference-sm5.md) 和更新版本的著色器模型</span><span class="sxs-lookup"><span data-stu-id="d02ad-133">[Shader Model 5](d3d11-graphics-reference-sm5.md) and higher shader models</span></span> | <span data-ttu-id="d02ad-134">是</span><span class="sxs-lookup"><span data-stu-id="d02ad-134">yes</span></span>       |



 

<span data-ttu-id="d02ad-135">下列著色器類型支援此函數：</span><span class="sxs-lookup"><span data-stu-id="d02ad-135">This function is supported in the following types of shaders:</span></span>



| <span data-ttu-id="d02ad-136">頂點</span><span class="sxs-lookup"><span data-stu-id="d02ad-136">Vertex</span></span> | <span data-ttu-id="d02ad-137">船體</span><span class="sxs-lookup"><span data-stu-id="d02ad-137">Hull</span></span> | <span data-ttu-id="d02ad-138">網域</span><span class="sxs-lookup"><span data-stu-id="d02ad-138">Domain</span></span> | <span data-ttu-id="d02ad-139">幾何</span><span class="sxs-lookup"><span data-stu-id="d02ad-139">Geometry</span></span> | <span data-ttu-id="d02ad-140">像素</span><span class="sxs-lookup"><span data-stu-id="d02ad-140">Pixel</span></span> | <span data-ttu-id="d02ad-141">計算</span><span class="sxs-lookup"><span data-stu-id="d02ad-141">Compute</span></span> |
|--------|------|--------|----------|-------|---------|
| <span data-ttu-id="d02ad-142">x</span><span class="sxs-lookup"><span data-stu-id="d02ad-142">x</span></span>      |  <span data-ttu-id="d02ad-143">x</span><span class="sxs-lookup"><span data-stu-id="d02ad-143">x</span></span>   |  <span data-ttu-id="d02ad-144">x</span><span class="sxs-lookup"><span data-stu-id="d02ad-144">x</span></span>     |  <span data-ttu-id="d02ad-145">x</span><span class="sxs-lookup"><span data-stu-id="d02ad-145">x</span></span>       | <span data-ttu-id="d02ad-146">x</span><span class="sxs-lookup"><span data-stu-id="d02ad-146">x</span></span>     | <span data-ttu-id="d02ad-147">x</span><span class="sxs-lookup"><span data-stu-id="d02ad-147">x</span></span>       |



 

## <a name="see-also"></a><span data-ttu-id="d02ad-148">另請參閱</span><span class="sxs-lookup"><span data-stu-id="d02ad-148">See also</span></span>

<dl> <dt>

[<span data-ttu-id="d02ad-149">內建函式</span><span class="sxs-lookup"><span data-stu-id="d02ad-149">Intrinsic Functions</span></span>](dx-graphics-hlsl-intrinsic-functions.md)
</dt> <dt>

[<span data-ttu-id="d02ad-150">著色器模型5</span><span class="sxs-lookup"><span data-stu-id="d02ad-150">Shader Model 5</span></span>](d3d11-graphics-reference-sm5.md)
</dt> </dl>

 

 




