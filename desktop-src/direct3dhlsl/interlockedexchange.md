---
title: 'InterlockedExchange 函式 (HLSL 參考) '
description: 將值指派給 dest，並傳回原始值。
ms.assetid: 1e7ce7ff-9e23-47fa-8e76-713f6bf57abf
keywords:
- InterlockedExchange 函式 HLSL
topic_type:
- apiref
api_name:
- InterlockedExchange
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
api_location: ''
ms.openlocfilehash: 7c39dc4f68429fa3f070d446f998fd528a99af01
ms.sourcegitcommit: 12e9b14501d51641b690ee0cf764e2b91eb9a140
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 02/06/2020
ms.locfileid: "104971664"
---
# <a name="interlockedexchange-function-hlsl-reference"></a><span data-ttu-id="ac521-104">InterlockedExchange 函式 (HLSL 參考) </span><span class="sxs-lookup"><span data-stu-id="ac521-104">InterlockedExchange function (HLSL reference)</span></span>

<span data-ttu-id="ac521-105">將值指派給 dest，並傳回原始值。</span><span class="sxs-lookup"><span data-stu-id="ac521-105">Assigns value to dest and returns the original value.</span></span>

## <a name="syntax"></a><span data-ttu-id="ac521-106">語法</span><span class="sxs-lookup"><span data-stu-id="ac521-106">Syntax</span></span>

``` syntax
void InterlockedExchange(
  in  R dest,
  in  T value,
  out T original_value
);
```

## <a name="parameters"></a><span data-ttu-id="ac521-107">參數</span><span class="sxs-lookup"><span data-stu-id="ac521-107">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="ac521-108">*目的地* \[在\]</span><span class="sxs-lookup"><span data-stu-id="ac521-108">*dest* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="ac521-109">類型： **R**</span><span class="sxs-lookup"><span data-stu-id="ac521-109">Type: **R**</span></span>

<span data-ttu-id="ac521-110">目的地位址。</span><span class="sxs-lookup"><span data-stu-id="ac521-110">The destination address.</span></span>

</dd> <dt>

<span data-ttu-id="ac521-111">*值* \[在\]</span><span class="sxs-lookup"><span data-stu-id="ac521-111">*value* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="ac521-112">類型： **T**</span><span class="sxs-lookup"><span data-stu-id="ac521-112">Type: **T**</span></span>

<span data-ttu-id="ac521-113">輸入值。</span><span class="sxs-lookup"><span data-stu-id="ac521-113">The input value.</span></span>

</dd> <dt>

<span data-ttu-id="ac521-114">*原始 \_ 值* \[ 輸出\]</span><span class="sxs-lookup"><span data-stu-id="ac521-114">*original\_value* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="ac521-115">類型： **T**</span><span class="sxs-lookup"><span data-stu-id="ac521-115">Type: **T**</span></span>

<span data-ttu-id="ac521-116">原始的值。</span><span class="sxs-lookup"><span data-stu-id="ac521-116">The original value.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="ac521-117">傳回值</span><span class="sxs-lookup"><span data-stu-id="ac521-117">Return value</span></span>

<span data-ttu-id="ac521-118">此函式不會傳回值。</span><span class="sxs-lookup"><span data-stu-id="ac521-118">This function does not return a value.</span></span>

## <a name="remarks"></a><span data-ttu-id="ac521-119">備註</span><span class="sxs-lookup"><span data-stu-id="ac521-119">Remarks</span></span>

<span data-ttu-id="ac521-120">這種作業只能對純量類型的資源和共用記憶體變數執行。</span><span class="sxs-lookup"><span data-stu-id="ac521-120">This operation can only be performed on scalar-typed resources and shared memory variables.</span></span> <span data-ttu-id="ac521-121">此函式有兩種可能的用途。</span><span class="sxs-lookup"><span data-stu-id="ac521-121">There are two possible uses for this function.</span></span> <span data-ttu-id="ac521-122">第一個是當 R 是共用記憶體變數型別時。</span><span class="sxs-lookup"><span data-stu-id="ac521-122">The first is when R is a shared memory variable type.</span></span> <span data-ttu-id="ac521-123">在此情況下，此函式會在 dest 所參考的共用記憶體暫存器上執行作業。</span><span class="sxs-lookup"><span data-stu-id="ac521-123">In this case, the function performs the operation on the shared memory register referenced by dest.</span></span> <span data-ttu-id="ac521-124">第二個案例是 R 是資源變數類型。</span><span class="sxs-lookup"><span data-stu-id="ac521-124">The second scenario is when R is a resource variable type.</span></span> <span data-ttu-id="ac521-125">在此案例中，此函式會在 dest 所參考的資源位置上執行作業。</span><span class="sxs-lookup"><span data-stu-id="ac521-125">In this scenario, the function performs the operation on the resource location referenced by dest.</span></span> <span data-ttu-id="ac521-126">只有當 R 可讀取和寫入時，才能使用此作業。</span><span class="sxs-lookup"><span data-stu-id="ac521-126">This operation is only available when R is readable and writable.</span></span>

### <a name="minimum-shader-model"></a><span data-ttu-id="ac521-127">最小著色器模型</span><span class="sxs-lookup"><span data-stu-id="ac521-127">Minimum Shader Model</span></span>

<span data-ttu-id="ac521-128">下列著色器模型支援此函數。</span><span class="sxs-lookup"><span data-stu-id="ac521-128">This function is supported in the following shader models.</span></span>



| <span data-ttu-id="ac521-129">著色器模型</span><span class="sxs-lookup"><span data-stu-id="ac521-129">Shader Model</span></span>                                                                | <span data-ttu-id="ac521-130">支援</span><span class="sxs-lookup"><span data-stu-id="ac521-130">Supported</span></span> |
|-----------------------------------------------------------------------------|-----------|
| <span data-ttu-id="ac521-131">[著色器模型 5](d3d11-graphics-reference-sm5.md) 和更新版本的著色器模型</span><span class="sxs-lookup"><span data-stu-id="ac521-131">[Shader Model 5](d3d11-graphics-reference-sm5.md) and higher shader models</span></span> | <span data-ttu-id="ac521-132">是</span><span class="sxs-lookup"><span data-stu-id="ac521-132">yes</span></span>       |



 

<span data-ttu-id="ac521-133">下列著色器類型支援此函數：</span><span class="sxs-lookup"><span data-stu-id="ac521-133">This function is supported in the following types of shaders:</span></span>



| <span data-ttu-id="ac521-134">頂點</span><span class="sxs-lookup"><span data-stu-id="ac521-134">Vertex</span></span> | <span data-ttu-id="ac521-135">船體</span><span class="sxs-lookup"><span data-stu-id="ac521-135">Hull</span></span> | <span data-ttu-id="ac521-136">網域</span><span class="sxs-lookup"><span data-stu-id="ac521-136">Domain</span></span> | <span data-ttu-id="ac521-137">幾何</span><span class="sxs-lookup"><span data-stu-id="ac521-137">Geometry</span></span> | <span data-ttu-id="ac521-138">像素</span><span class="sxs-lookup"><span data-stu-id="ac521-138">Pixel</span></span> | <span data-ttu-id="ac521-139">計算</span><span class="sxs-lookup"><span data-stu-id="ac521-139">Compute</span></span> |
|--------|------|--------|----------|-------|---------|
| <span data-ttu-id="ac521-140">x</span><span class="sxs-lookup"><span data-stu-id="ac521-140">x</span></span>      |  <span data-ttu-id="ac521-141">x</span><span class="sxs-lookup"><span data-stu-id="ac521-141">x</span></span>   | <span data-ttu-id="ac521-142">x</span><span class="sxs-lookup"><span data-stu-id="ac521-142">x</span></span>      |  <span data-ttu-id="ac521-143">x</span><span class="sxs-lookup"><span data-stu-id="ac521-143">x</span></span>       | <span data-ttu-id="ac521-144">x</span><span class="sxs-lookup"><span data-stu-id="ac521-144">x</span></span>     | <span data-ttu-id="ac521-145">x</span><span class="sxs-lookup"><span data-stu-id="ac521-145">x</span></span>       |



 

## <a name="see-also"></a><span data-ttu-id="ac521-146">另請參閱</span><span class="sxs-lookup"><span data-stu-id="ac521-146">See also</span></span>

<dl> <dt>

[<span data-ttu-id="ac521-147">內建函式</span><span class="sxs-lookup"><span data-stu-id="ac521-147">Intrinsic Functions</span></span>](dx-graphics-hlsl-intrinsic-functions.md)
</dt> <dt>

[<span data-ttu-id="ac521-148">著色器模型5</span><span class="sxs-lookup"><span data-stu-id="ac521-148">Shader Model 5</span></span>](d3d11-graphics-reference-sm5.md)
</dt> </dl>

 

 




