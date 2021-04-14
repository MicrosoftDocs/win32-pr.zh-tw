---
title: asfloat
description: 以浮點數的形式來解讀 x 的位模式。
ms.assetid: 48e1e0cb-8578-4e6d-8c46-2b8b201906c1
keywords:
- asfloat HLSL
topic_type:
- apiref
api_name:
- asfloat
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
api_location: ''
ms.openlocfilehash: 9a5701d959fb59519318dd7f2e91b6790f4c0b6e
ms.sourcegitcommit: 592c9bbd22ba69802dc353bcb5eb30699f9e9403
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/20/2020
ms.locfileid: "104990990"
---
# <a name="asfloat"></a><span data-ttu-id="62315-104">asfloat</span><span class="sxs-lookup"><span data-stu-id="62315-104">asfloat</span></span>

<span data-ttu-id="62315-105">以浮點數的形式來解讀 *x* 的位模式。</span><span class="sxs-lookup"><span data-stu-id="62315-105">Interprets the bit pattern of *x* as a floating-point number.</span></span>



| <span data-ttu-id="62315-106">ret asfloat (*x*) </span><span class="sxs-lookup"><span data-stu-id="62315-106">ret asfloat(*x*)</span></span> |
|------------------|



 

## <a name="parameters"></a><span data-ttu-id="62315-107">參數</span><span class="sxs-lookup"><span data-stu-id="62315-107">Parameters</span></span>



| <span data-ttu-id="62315-108">項目</span><span class="sxs-lookup"><span data-stu-id="62315-108">Item</span></span>                                                   | <span data-ttu-id="62315-109">描述</span><span class="sxs-lookup"><span data-stu-id="62315-109">Description</span></span>                        |
|--------------------------------------------------------|------------------------------------|
| <span data-ttu-id="62315-110"><span id="x"></span><span id="X"></span>*X*</span><span class="sxs-lookup"><span data-stu-id="62315-110"><span id="x"></span><span id="X"></span>*x*</span></span><br/> | <span data-ttu-id="62315-111">\[在 \] 輸入值中。</span><span class="sxs-lookup"><span data-stu-id="62315-111">\[in\] The input value.</span></span><br/> |



 

## <a name="return-value"></a><span data-ttu-id="62315-112">傳回值</span><span class="sxs-lookup"><span data-stu-id="62315-112">Return Value</span></span>

<span data-ttu-id="62315-113">解釋為浮點數的輸入。</span><span class="sxs-lookup"><span data-stu-id="62315-113">The input interpreted as a floating-point number.</span></span>

## <a name="type-description"></a><span data-ttu-id="62315-114">類型描述</span><span class="sxs-lookup"><span data-stu-id="62315-114">Type Description</span></span>



| <span data-ttu-id="62315-115">Name</span><span class="sxs-lookup"><span data-stu-id="62315-115">Name</span></span>  | [<span data-ttu-id="62315-116">**範本類型**</span><span class="sxs-lookup"><span data-stu-id="62315-116">**Template Type**</span></span>](dx-graphics-hlsl-intrinsic-functions.md)                                                  | [<span data-ttu-id="62315-117">**元件類型**</span><span class="sxs-lookup"><span data-stu-id="62315-117">**Component Type**</span></span>](dx-graphics-hlsl-intrinsic-functions.md)                                                         | <span data-ttu-id="62315-118">大小</span><span class="sxs-lookup"><span data-stu-id="62315-118">Size</span></span>                           |
|-------|----------------------------------------------------------------------------------------------------------------|------------------------------------------------------------------------------------------------------------------------|--------------------------------|
| <span data-ttu-id="62315-119">*x*</span><span class="sxs-lookup"><span data-stu-id="62315-119">*x*</span></span>   | <span data-ttu-id="62315-120">純 [**量、**](dx-graphics-hlsl-intrinsic-functions.md)**向量** 或 **矩陣**</span><span class="sxs-lookup"><span data-stu-id="62315-120">[**scalar**](dx-graphics-hlsl-intrinsic-functions.md), **vector**, or **matrix**</span></span> | <span data-ttu-id="62315-121">[**float**](/windows/desktop/WinProg/windows-data-types)、 [**int**](/windows/desktop/WinProg/windows-data-types)、 [**uint**](/windows/desktop/WinProg/windows-data-types)</span><span class="sxs-lookup"><span data-stu-id="62315-121">[**float**](/windows/desktop/WinProg/windows-data-types), [**int**](/windows/desktop/WinProg/windows-data-types), [**uint**](/windows/desktop/WinProg/windows-data-types)</span></span> | <span data-ttu-id="62315-122">任意</span><span class="sxs-lookup"><span data-stu-id="62315-122">any</span></span>                            |
| <span data-ttu-id="62315-123">*Ret*</span><span class="sxs-lookup"><span data-stu-id="62315-123">*ret*</span></span> | <span data-ttu-id="62315-124">與輸入 *x* 相同</span><span class="sxs-lookup"><span data-stu-id="62315-124">same as input *x*</span></span>                                                                                              | [<span data-ttu-id="62315-125">**浮動**</span><span class="sxs-lookup"><span data-stu-id="62315-125">**float**</span></span>](/windows/desktop/WinProg/windows-data-types)                                                                                | <span data-ttu-id="62315-126">) 為輸入 *x* 的相同維度 (s</span><span class="sxs-lookup"><span data-stu-id="62315-126">same dimension(s) as input *x*</span></span> |



 

## <a name="function-overloads"></a><span data-ttu-id="62315-127">函數多載</span><span class="sxs-lookup"><span data-stu-id="62315-127">Function Overloads</span></span>

<dl> <span data-ttu-id="62315-128">' float <x> asfloat (float <x> 值) ; `  
`float <x> asfloat (int <x> 值) ; `  
`float <x> asfloat (uint <x> 值) ; '</span><span class="sxs-lookup"><span data-stu-id="62315-128">`float<x> asfloat(float<x> value);`  
`float<x> asfloat(int<x> value);`  
`float<x> asfloat(uint<x> value);`</span></span>
</dl>

## <a name="minimum-shader-model"></a><span data-ttu-id="62315-129">最小著色器模型</span><span class="sxs-lookup"><span data-stu-id="62315-129">Minimum Shader Model</span></span>

<span data-ttu-id="62315-130">下列著色器模型支援此函數。</span><span class="sxs-lookup"><span data-stu-id="62315-130">This function is supported in the following shader models.</span></span>



| <span data-ttu-id="62315-131">著色器模型</span><span class="sxs-lookup"><span data-stu-id="62315-131">Shader Model</span></span>                                                        | <span data-ttu-id="62315-132">支援</span><span class="sxs-lookup"><span data-stu-id="62315-132">Supported</span></span> |
|---------------------------------------------------------------------|-----------|
| <span data-ttu-id="62315-133">[著色器模型 4](dx-graphics-hlsl-sm4.md) 和更高的著色器模型</span><span class="sxs-lookup"><span data-stu-id="62315-133">[Shader Model 4](dx-graphics-hlsl-sm4.md) and higher shader models</span></span> | <span data-ttu-id="62315-134">是</span><span class="sxs-lookup"><span data-stu-id="62315-134">yes</span></span>       |
| [<span data-ttu-id="62315-135">著色器模型 3 (DirectX HLSL) </span><span class="sxs-lookup"><span data-stu-id="62315-135">Shader Model 3 (DirectX HLSL)</span></span>](dx-graphics-hlsl-sm3.md)           | <span data-ttu-id="62315-136">不可以</span><span class="sxs-lookup"><span data-stu-id="62315-136">no</span></span>        |
| [<span data-ttu-id="62315-137">著色器模型 2 (DirectX HLSL) </span><span class="sxs-lookup"><span data-stu-id="62315-137">Shader Model 2 (DirectX HLSL)</span></span>](dx-graphics-hlsl-sm2.md)           | <span data-ttu-id="62315-138">不可以</span><span class="sxs-lookup"><span data-stu-id="62315-138">no</span></span>        |
| [<span data-ttu-id="62315-139">著色器模型 1 (DirectX HLSL) </span><span class="sxs-lookup"><span data-stu-id="62315-139">Shader Model 1 (DirectX HLSL)</span></span>](dx-graphics-hlsl-sm1.md)           | <span data-ttu-id="62315-140">不可以</span><span class="sxs-lookup"><span data-stu-id="62315-140">no</span></span>        |



 

## <a name="remarks"></a><span data-ttu-id="62315-141">備註</span><span class="sxs-lookup"><span data-stu-id="62315-141">Remarks</span></span>

<span data-ttu-id="62315-142">舊版編譯器不正確地允許 `asfloat(bool)` ，但請注意，不支援 bool 輸入。</span><span class="sxs-lookup"><span data-stu-id="62315-142">Older compilers incorrectly allowed `asfloat(bool)`, but note that bool inputs are not supported.</span></span>

## <a name="see-also"></a><span data-ttu-id="62315-143">另請參閱</span><span class="sxs-lookup"><span data-stu-id="62315-143">See also</span></span>

<dl> <dt>

[<span data-ttu-id="62315-144">**(DirectX HLSL) 內建函式**</span><span class="sxs-lookup"><span data-stu-id="62315-144">**Intrinsic Functions (DirectX HLSL)**</span></span>](dx-graphics-hlsl-intrinsic-functions.md)
</dt> </dl>

 

