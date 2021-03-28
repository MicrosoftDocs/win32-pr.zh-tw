---
title: 'InterlockedMax 函式 (HLSL 參考) '
description: 執行保證的不可部分完成上限。
ms.assetid: ea2c67ef-3133-424d-9cc3-81da79aee87e
keywords:
- InterlockedMax 函式 HLSL
topic_type:
- apiref
api_name:
- InterlockedMax
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
api_location: ''
ms.openlocfilehash: 997641b086625532b99e3ae8d17be49cd71ae21f
ms.sourcegitcommit: 12e9b14501d51641b690ee0cf764e2b91eb9a140
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 02/06/2020
ms.locfileid: "104374230"
---
# <a name="interlockedmax-function-hlsl-reference"></a><span data-ttu-id="5cece-104">InterlockedMax 函式 (HLSL 參考) </span><span class="sxs-lookup"><span data-stu-id="5cece-104">InterlockedMax function (HLSL reference)</span></span>

<span data-ttu-id="5cece-105">執行保證的不可部分完成上限。</span><span class="sxs-lookup"><span data-stu-id="5cece-105">Performs a guaranteed atomic max.</span></span>

## <a name="syntax"></a><span data-ttu-id="5cece-106">語法</span><span class="sxs-lookup"><span data-stu-id="5cece-106">Syntax</span></span>

``` syntax
void InterlockedMax(
  in  R dest,
  in  T value,
  out T original_value
);
```

## <a name="parameters"></a><span data-ttu-id="5cece-107">參數</span><span class="sxs-lookup"><span data-stu-id="5cece-107">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="5cece-108">*目的地* \[在\]</span><span class="sxs-lookup"><span data-stu-id="5cece-108">*dest* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="5cece-109">類型： **R**</span><span class="sxs-lookup"><span data-stu-id="5cece-109">Type: **R**</span></span>

<span data-ttu-id="5cece-110">目的地位址。</span><span class="sxs-lookup"><span data-stu-id="5cece-110">The destination address.</span></span>

</dd> <dt>

<span data-ttu-id="5cece-111">*值* \[在\]</span><span class="sxs-lookup"><span data-stu-id="5cece-111">*value* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="5cece-112">類型： **T**</span><span class="sxs-lookup"><span data-stu-id="5cece-112">Type: **T**</span></span>

<span data-ttu-id="5cece-113">輸入值。</span><span class="sxs-lookup"><span data-stu-id="5cece-113">The input value.</span></span>

</dd> <dt>

<span data-ttu-id="5cece-114">*原始 \_ 值* \[ 輸出\]</span><span class="sxs-lookup"><span data-stu-id="5cece-114">*original\_value* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="5cece-115">類型： **T**</span><span class="sxs-lookup"><span data-stu-id="5cece-115">Type: **T**</span></span>

<span data-ttu-id="5cece-116">選擇性。</span><span class="sxs-lookup"><span data-stu-id="5cece-116">Optional.</span></span> <span data-ttu-id="5cece-117">原始的輸入值。</span><span class="sxs-lookup"><span data-stu-id="5cece-117">The original input value.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="5cece-118">傳回值</span><span class="sxs-lookup"><span data-stu-id="5cece-118">Return value</span></span>

<span data-ttu-id="5cece-119">此函式不會傳回值。</span><span class="sxs-lookup"><span data-stu-id="5cece-119">This function does not return a value.</span></span>

## <a name="remarks"></a><span data-ttu-id="5cece-120">備註</span><span class="sxs-lookup"><span data-stu-id="5cece-120">Remarks</span></span>

<span data-ttu-id="5cece-121">此作業只能在 int 和 uint 具類型的資源和共用記憶體變數上執行。</span><span class="sxs-lookup"><span data-stu-id="5cece-121">This operation can only be performed on int and uint typed resources and shared memory variables.</span></span> <span data-ttu-id="5cece-122">此函式有兩種可能的用途。</span><span class="sxs-lookup"><span data-stu-id="5cece-122">There are two possible uses for this function.</span></span> <span data-ttu-id="5cece-123">第一個是當 R 是共用記憶體變數型別時。</span><span class="sxs-lookup"><span data-stu-id="5cece-123">The first is when R is a shared memory variable type.</span></span> <span data-ttu-id="5cece-124">在此情況下，此函式會針對 dest 所參考的共用記憶體暫存器執行最小值的最大值。</span><span class="sxs-lookup"><span data-stu-id="5cece-124">In this case, the function performs an atomic max of value to the shared memory register referenced by dest.</span></span> <span data-ttu-id="5cece-125">第二個案例是 R 是資源變數類型。</span><span class="sxs-lookup"><span data-stu-id="5cece-125">The second scenario is when R is a resource variable type.</span></span> <span data-ttu-id="5cece-126">在此案例中，此函式會針對 dest 所參考的資源位置執行最小值的最大值。</span><span class="sxs-lookup"><span data-stu-id="5cece-126">In this scenario, the function performs an atomic max of value to the resource location referenced by dest.</span></span> <span data-ttu-id="5cece-127">多載函式有額外的輸出變數，其會設定為目的地的原始值。</span><span class="sxs-lookup"><span data-stu-id="5cece-127">The overloaded function has an additional output variable which will be set to the original value of dest.</span></span> <span data-ttu-id="5cece-128">只有在 R 可讀取和可寫入時，才能使用此多載作業。</span><span class="sxs-lookup"><span data-stu-id="5cece-128">This overloaded operation is only available when R is readable and writable.</span></span>

### <a name="minimum-shader-model"></a><span data-ttu-id="5cece-129">最小著色器模型</span><span class="sxs-lookup"><span data-stu-id="5cece-129">Minimum Shader Model</span></span>

<span data-ttu-id="5cece-130">下列著色器模型支援此函數。</span><span class="sxs-lookup"><span data-stu-id="5cece-130">This function is supported in the following shader models.</span></span>



| <span data-ttu-id="5cece-131">著色器模型</span><span class="sxs-lookup"><span data-stu-id="5cece-131">Shader Model</span></span>                                                                | <span data-ttu-id="5cece-132">支援</span><span class="sxs-lookup"><span data-stu-id="5cece-132">Supported</span></span> |
|-----------------------------------------------------------------------------|-----------|
| <span data-ttu-id="5cece-133">[著色器模型 5](d3d11-graphics-reference-sm5.md) 和更新版本的著色器模型</span><span class="sxs-lookup"><span data-stu-id="5cece-133">[Shader Model 5](d3d11-graphics-reference-sm5.md) and higher shader models</span></span> | <span data-ttu-id="5cece-134">是</span><span class="sxs-lookup"><span data-stu-id="5cece-134">yes</span></span>       |



 

<span data-ttu-id="5cece-135">下列著色器類型支援此函數：</span><span class="sxs-lookup"><span data-stu-id="5cece-135">This function is supported in the following types of shaders:</span></span>



| <span data-ttu-id="5cece-136">頂點</span><span class="sxs-lookup"><span data-stu-id="5cece-136">Vertex</span></span> | <span data-ttu-id="5cece-137">船體</span><span class="sxs-lookup"><span data-stu-id="5cece-137">Hull</span></span> | <span data-ttu-id="5cece-138">網域</span><span class="sxs-lookup"><span data-stu-id="5cece-138">Domain</span></span> | <span data-ttu-id="5cece-139">幾何</span><span class="sxs-lookup"><span data-stu-id="5cece-139">Geometry</span></span> | <span data-ttu-id="5cece-140">像素</span><span class="sxs-lookup"><span data-stu-id="5cece-140">Pixel</span></span> | <span data-ttu-id="5cece-141">計算</span><span class="sxs-lookup"><span data-stu-id="5cece-141">Compute</span></span> |
|--------|------|--------|----------|-------|---------|
| <span data-ttu-id="5cece-142">x</span><span class="sxs-lookup"><span data-stu-id="5cece-142">x</span></span>      |  <span data-ttu-id="5cece-143">x</span><span class="sxs-lookup"><span data-stu-id="5cece-143">x</span></span>   |  <span data-ttu-id="5cece-144">x</span><span class="sxs-lookup"><span data-stu-id="5cece-144">x</span></span>     |  <span data-ttu-id="5cece-145">x</span><span class="sxs-lookup"><span data-stu-id="5cece-145">x</span></span>       | <span data-ttu-id="5cece-146">x</span><span class="sxs-lookup"><span data-stu-id="5cece-146">x</span></span>     | <span data-ttu-id="5cece-147">x</span><span class="sxs-lookup"><span data-stu-id="5cece-147">x</span></span>       |



 

## <a name="see-also"></a><span data-ttu-id="5cece-148">另請參閱</span><span class="sxs-lookup"><span data-stu-id="5cece-148">See also</span></span>

<dl> <dt>

[<span data-ttu-id="5cece-149">內建函式</span><span class="sxs-lookup"><span data-stu-id="5cece-149">Intrinsic Functions</span></span>](dx-graphics-hlsl-intrinsic-functions.md)
</dt> <dt>

[<span data-ttu-id="5cece-150">著色器模型5</span><span class="sxs-lookup"><span data-stu-id="5cece-150">Shader Model 5</span></span>](d3d11-graphics-reference-sm5.md)
</dt> </dl>

 

 




