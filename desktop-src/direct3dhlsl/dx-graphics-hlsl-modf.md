---
title: 'modf (Corecrt \_ math .h) '
description: 將值 x 分割成小數和整數部分，每個部分都具有與 x 相同的正負號。
ms.assetid: 0cac1cf3-f0da-4b0a-ba30-4af5d65b04b2
keywords:
- modf HLSL
topic_type:
- apiref
api_name:
- modf
api_location:
- corecrt_math.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 5079549e70414f8237fd33a5e263dd8f17dcb9e3
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 03/15/2021
ms.locfileid: "103946141"
---
# <a name="modf"></a><span data-ttu-id="378d9-104">modf</span><span class="sxs-lookup"><span data-stu-id="378d9-104">modf</span></span>

<span data-ttu-id="378d9-105">將值 x 分割成小數和整數部分，每個部分都具有與 x 相同的正負號。</span><span class="sxs-lookup"><span data-stu-id="378d9-105">Splits the value x into fractional and integer parts, each of which has the same sign as x.</span></span>



| <span data-ttu-id="378d9-106">ret modf (x，輸出 ip) </span><span class="sxs-lookup"><span data-stu-id="378d9-106">ret modf(x, out ip)</span></span> |
|---------------------|



 

## <a name="parameters"></a><span data-ttu-id="378d9-107">參數</span><span class="sxs-lookup"><span data-stu-id="378d9-107">Parameters</span></span>



| <span data-ttu-id="378d9-108">項目</span><span class="sxs-lookup"><span data-stu-id="378d9-108">Item</span></span>                                                      | <span data-ttu-id="378d9-109">描述</span><span class="sxs-lookup"><span data-stu-id="378d9-109">Description</span></span>                                    |
|-----------------------------------------------------------|------------------------------------------------|
| <span data-ttu-id="378d9-110"><span id="x"></span><span id="X"></span>*X*</span><span class="sxs-lookup"><span data-stu-id="378d9-110"><span id="x"></span><span id="X"></span>*x*</span></span><br/>    | <span data-ttu-id="378d9-111">\[在 \] [x 輸入值] 中。</span><span class="sxs-lookup"><span data-stu-id="378d9-111">\[in\] The x input value.</span></span><br/>           |
| <span data-ttu-id="378d9-112"><span id="ip"></span><span id="IP"></span>*Ip*</span><span class="sxs-lookup"><span data-stu-id="378d9-112"><span id="ip"></span><span id="IP"></span>*ip*</span></span><br/> | <span data-ttu-id="378d9-113">\[\] *x* 的整數部分。</span><span class="sxs-lookup"><span data-stu-id="378d9-113">\[out\] The integer portion of *x*.</span></span><br/> |



 

## <a name="return-value"></a><span data-ttu-id="378d9-114">傳回值</span><span class="sxs-lookup"><span data-stu-id="378d9-114">Return Value</span></span>

<span data-ttu-id="378d9-115">X 的帶正負號小數部分。</span><span class="sxs-lookup"><span data-stu-id="378d9-115">The signed-fractional portion of x.</span></span>

## <a name="type-description"></a><span data-ttu-id="378d9-116">類型描述</span><span class="sxs-lookup"><span data-stu-id="378d9-116">Type Description</span></span>



| <span data-ttu-id="378d9-117">Name</span><span class="sxs-lookup"><span data-stu-id="378d9-117">Name</span></span> | <span data-ttu-id="378d9-118">輸入/輸出</span><span class="sxs-lookup"><span data-stu-id="378d9-118">In/Out</span></span> | [<span data-ttu-id="378d9-119">**範本類型**</span><span class="sxs-lookup"><span data-stu-id="378d9-119">**Template Type**</span></span>](dx-graphics-hlsl-intrinsic-functions.md)                                                  | [<span data-ttu-id="378d9-120">**元件類型**</span><span class="sxs-lookup"><span data-stu-id="378d9-120">**Component Type**</span></span>](dx-graphics-hlsl-intrinsic-functions.md)                 | <span data-ttu-id="378d9-121">大小</span><span class="sxs-lookup"><span data-stu-id="378d9-121">Size</span></span>                         |
|------|--------|----------------------------------------------------------------------------------------------------------------|--------------------------------------------------------------------------------|------------------------------|
| <span data-ttu-id="378d9-122">x</span><span class="sxs-lookup"><span data-stu-id="378d9-122">x</span></span>    | <span data-ttu-id="378d9-123">in</span><span class="sxs-lookup"><span data-stu-id="378d9-123">in</span></span>     | <span data-ttu-id="378d9-124">純 [**量、**](dx-graphics-hlsl-intrinsic-functions.md)**向量** 或 **矩陣**</span><span class="sxs-lookup"><span data-stu-id="378d9-124">[**scalar**](dx-graphics-hlsl-intrinsic-functions.md), **vector**, or **matrix**</span></span> | <span data-ttu-id="378d9-125">[**float**](/windows/desktop/WinProg/windows-data-types)、 [ **int**](/windows/desktop/WinProg/windows-data-types)</span><span class="sxs-lookup"><span data-stu-id="378d9-125">[**float**](/windows/desktop/WinProg/windows-data-types), [**int**](/windows/desktop/WinProg/windows-data-types)</span></span> | <span data-ttu-id="378d9-126">任意</span><span class="sxs-lookup"><span data-stu-id="378d9-126">any</span></span>                          |
| <span data-ttu-id="378d9-127">ip</span><span class="sxs-lookup"><span data-stu-id="378d9-127">ip</span></span>   | <span data-ttu-id="378d9-128">out</span><span class="sxs-lookup"><span data-stu-id="378d9-128">out</span></span>    | <span data-ttu-id="378d9-129">與輸入 x 相同</span><span class="sxs-lookup"><span data-stu-id="378d9-129">same as input x</span></span>                                                                                                | <span data-ttu-id="378d9-130">[**float**](/windows/desktop/WinProg/windows-data-types)、 [ **int**](/windows/desktop/WinProg/windows-data-types)</span><span class="sxs-lookup"><span data-stu-id="378d9-130">[**float**](/windows/desktop/WinProg/windows-data-types), [**int**](/windows/desktop/WinProg/windows-data-types)</span></span> | <span data-ttu-id="378d9-131">) 為輸入 x 的相同維度 (s</span><span class="sxs-lookup"><span data-stu-id="378d9-131">same dimension(s) as input x</span></span> |
| <span data-ttu-id="378d9-132">Ret</span><span class="sxs-lookup"><span data-stu-id="378d9-132">ret</span></span>  | <span data-ttu-id="378d9-133">out</span><span class="sxs-lookup"><span data-stu-id="378d9-133">out</span></span>    | <span data-ttu-id="378d9-134">與輸入 x 相同</span><span class="sxs-lookup"><span data-stu-id="378d9-134">same as input x</span></span>                                                                                                | <span data-ttu-id="378d9-135">[**float**](/windows/desktop/WinProg/windows-data-types)、 [ **int**](/windows/desktop/WinProg/windows-data-types)</span><span class="sxs-lookup"><span data-stu-id="378d9-135">[**float**](/windows/desktop/WinProg/windows-data-types), [**int**](/windows/desktop/WinProg/windows-data-types)</span></span> | <span data-ttu-id="378d9-136">) 為輸入 x 的相同維度 (s</span><span class="sxs-lookup"><span data-stu-id="378d9-136">same dimension(s) as input x</span></span> |



 

## <a name="minimum-shader-model"></a><span data-ttu-id="378d9-137">最小著色器模型</span><span class="sxs-lookup"><span data-stu-id="378d9-137">Minimum Shader Model</span></span>

<span data-ttu-id="378d9-138">下列著色器模型支援此函數。</span><span class="sxs-lookup"><span data-stu-id="378d9-138">This function is supported in the following shader models.</span></span>



| <span data-ttu-id="378d9-139">著色器模型</span><span class="sxs-lookup"><span data-stu-id="378d9-139">Shader Model</span></span>                                                                       | <span data-ttu-id="378d9-140">支援</span><span class="sxs-lookup"><span data-stu-id="378d9-140">Supported</span></span>           |
|------------------------------------------------------------------------------------|---------------------|
| <span data-ttu-id="378d9-141">[著色器模型 2 (DIRECTX HLSL) ](dx-graphics-hlsl-sm2.md) 和更高的著色器模型</span><span class="sxs-lookup"><span data-stu-id="378d9-141">[Shader Model 2 (DirectX HLSL)](dx-graphics-hlsl-sm2.md) and higher shader models</span></span> | <span data-ttu-id="378d9-142">是</span><span class="sxs-lookup"><span data-stu-id="378d9-142">yes</span></span>                 |
| [<span data-ttu-id="378d9-143">著色器模型 1 (DirectX HLSL) </span><span class="sxs-lookup"><span data-stu-id="378d9-143">Shader Model 1 (DirectX HLSL)</span></span>](dx-graphics-hlsl-sm1.md)                          | <span data-ttu-id="378d9-144">是 (\_ \_ 只有) 的 vs 1</span><span class="sxs-lookup"><span data-stu-id="378d9-144">yes (vs\_1\_1 only)</span></span> |



 

## <a name="requirements"></a><span data-ttu-id="378d9-145">規格需求</span><span class="sxs-lookup"><span data-stu-id="378d9-145">Requirements</span></span>



| <span data-ttu-id="378d9-146">需求</span><span class="sxs-lookup"><span data-stu-id="378d9-146">Requirement</span></span> | <span data-ttu-id="378d9-147">值</span><span class="sxs-lookup"><span data-stu-id="378d9-147">Value</span></span> |
|-------------------|--------------------------------------------------------------------------------------------|
| <span data-ttu-id="378d9-148">標頭</span><span class="sxs-lookup"><span data-stu-id="378d9-148">Header</span></span><br/> | <dl> <span data-ttu-id="378d9-149"><dt>Corecrt \_ math。h</dt></span><span class="sxs-lookup"><span data-stu-id="378d9-149"><dt>Corecrt\_math.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="378d9-150">另請參閱</span><span class="sxs-lookup"><span data-stu-id="378d9-150">See also</span></span>

<dl> <dt>

[<span data-ttu-id="378d9-151">**(DirectX HLSL) 內建函式**</span><span class="sxs-lookup"><span data-stu-id="378d9-151">**Intrinsic Functions (DirectX HLSL)**</span></span>](dx-graphics-hlsl-intrinsic-functions.md)
</dt> </dl>

 

