---
title: asint
description: 將 x 的位模式以整數來解讀。
ms.assetid: e17e0a11-ef52-4b23-94b8-5db0b18aff4d
keywords:
- asint HLSL
topic_type:
- apiref
api_name:
- asint
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
api_location: ''
ms.openlocfilehash: ce1b0ca7e1c7b3716be1a3029c5478f96e261ce5
ms.sourcegitcommit: 592c9bbd22ba69802dc353bcb5eb30699f9e9403
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/20/2020
ms.locfileid: "104023866"
---
# <a name="asint"></a><span data-ttu-id="a2dcb-104">asint</span><span class="sxs-lookup"><span data-stu-id="a2dcb-104">asint</span></span>

<span data-ttu-id="a2dcb-105">將 *x* 的位模式以整數來解讀。</span><span class="sxs-lookup"><span data-stu-id="a2dcb-105">Interprets the bit pattern of *x* as an integer.</span></span>



| <span data-ttu-id="a2dcb-106">ret asint (*x*) </span><span class="sxs-lookup"><span data-stu-id="a2dcb-106">ret asint(*x*)</span></span> |
|----------------|



 

## <a name="parameters"></a><span data-ttu-id="a2dcb-107">參數</span><span class="sxs-lookup"><span data-stu-id="a2dcb-107">Parameters</span></span>



| <span data-ttu-id="a2dcb-108">項目</span><span class="sxs-lookup"><span data-stu-id="a2dcb-108">Item</span></span>                                                   | <span data-ttu-id="a2dcb-109">描述</span><span class="sxs-lookup"><span data-stu-id="a2dcb-109">Description</span></span>                        |
|--------------------------------------------------------|------------------------------------|
| <span data-ttu-id="a2dcb-110"><span id="x"></span><span id="X"></span>*X*</span><span class="sxs-lookup"><span data-stu-id="a2dcb-110"><span id="x"></span><span id="X"></span>*x*</span></span><br/> | <span data-ttu-id="a2dcb-111">\[在 \] 輸入值中。</span><span class="sxs-lookup"><span data-stu-id="a2dcb-111">\[in\] The input value.</span></span><br/> |



 

## <a name="return-value"></a><span data-ttu-id="a2dcb-112">傳回值</span><span class="sxs-lookup"><span data-stu-id="a2dcb-112">Return Value</span></span>

<span data-ttu-id="a2dcb-113">轉譯為整數的輸入。</span><span class="sxs-lookup"><span data-stu-id="a2dcb-113">The input interpreted as an integer.</span></span>

## <a name="type-description"></a><span data-ttu-id="a2dcb-114">類型描述</span><span class="sxs-lookup"><span data-stu-id="a2dcb-114">Type Description</span></span>



| <span data-ttu-id="a2dcb-115">Name</span><span class="sxs-lookup"><span data-stu-id="a2dcb-115">Name</span></span>  | [<span data-ttu-id="a2dcb-116">**範本類型**</span><span class="sxs-lookup"><span data-stu-id="a2dcb-116">**Template Type**</span></span>](dx-graphics-hlsl-intrinsic-functions.md)                                                  | [<span data-ttu-id="a2dcb-117">**元件類型**</span><span class="sxs-lookup"><span data-stu-id="a2dcb-117">**Component Type**</span></span>](dx-graphics-hlsl-intrinsic-functions.md)                  | <span data-ttu-id="a2dcb-118">大小</span><span class="sxs-lookup"><span data-stu-id="a2dcb-118">Size</span></span>                           |
|-------|----------------------------------------------------------------------------------------------------------------|---------------------------------------------------------------------------------|--------------------------------|
| <span data-ttu-id="a2dcb-119">*x*</span><span class="sxs-lookup"><span data-stu-id="a2dcb-119">*x*</span></span>   | <span data-ttu-id="a2dcb-120">純 [**量、**](dx-graphics-hlsl-intrinsic-functions.md)**向量** 或 **矩陣**</span><span class="sxs-lookup"><span data-stu-id="a2dcb-120">[**scalar**](dx-graphics-hlsl-intrinsic-functions.md), **vector**, or **matrix**</span></span> | <span data-ttu-id="a2dcb-121">[**float**](/windows/desktop/WinProg/windows-data-types)、 [ **uint**](/windows/desktop/WinProg/windows-data-types)</span><span class="sxs-lookup"><span data-stu-id="a2dcb-121">[**float**](/windows/desktop/WinProg/windows-data-types), [**uint**](/windows/desktop/WinProg/windows-data-types)</span></span> | <span data-ttu-id="a2dcb-122">任意</span><span class="sxs-lookup"><span data-stu-id="a2dcb-122">any</span></span>                            |
| <span data-ttu-id="a2dcb-123">*Ret*</span><span class="sxs-lookup"><span data-stu-id="a2dcb-123">*ret*</span></span> | <span data-ttu-id="a2dcb-124">與輸入 *x* 相同</span><span class="sxs-lookup"><span data-stu-id="a2dcb-124">same as input *x*</span></span>                                                                                              | [<span data-ttu-id="a2dcb-125">**int**</span><span class="sxs-lookup"><span data-stu-id="a2dcb-125">**int**</span></span>](/windows/desktop/WinProg/windows-data-types)                                           | <span data-ttu-id="a2dcb-126">) 為輸入 *x* 的相同維度 (s</span><span class="sxs-lookup"><span data-stu-id="a2dcb-126">same dimension(s) as input *x*</span></span> |



 

## <a name="minimum-shader-model"></a><span data-ttu-id="a2dcb-127">最小著色器模型</span><span class="sxs-lookup"><span data-stu-id="a2dcb-127">Minimum Shader Model</span></span>

<span data-ttu-id="a2dcb-128">下列著色器模型支援此函數。</span><span class="sxs-lookup"><span data-stu-id="a2dcb-128">This function is supported in the following shader models.</span></span>



| <span data-ttu-id="a2dcb-129">著色器模型</span><span class="sxs-lookup"><span data-stu-id="a2dcb-129">Shader Model</span></span>                                                        | <span data-ttu-id="a2dcb-130">支援</span><span class="sxs-lookup"><span data-stu-id="a2dcb-130">Supported</span></span> |
|---------------------------------------------------------------------|-----------|
| <span data-ttu-id="a2dcb-131">[著色器模型 4](dx-graphics-hlsl-sm4.md) 和更高的著色器模型</span><span class="sxs-lookup"><span data-stu-id="a2dcb-131">[Shader Model 4](dx-graphics-hlsl-sm4.md) and higher shader models</span></span> | <span data-ttu-id="a2dcb-132">是</span><span class="sxs-lookup"><span data-stu-id="a2dcb-132">yes</span></span>       |
| [<span data-ttu-id="a2dcb-133">著色器模型 3 (DirectX HLSL) </span><span class="sxs-lookup"><span data-stu-id="a2dcb-133">Shader Model 3 (DirectX HLSL)</span></span>](dx-graphics-hlsl-sm3.md)           | <span data-ttu-id="a2dcb-134">不可以</span><span class="sxs-lookup"><span data-stu-id="a2dcb-134">no</span></span>        |
| [<span data-ttu-id="a2dcb-135">著色器模型 2 (DirectX HLSL) </span><span class="sxs-lookup"><span data-stu-id="a2dcb-135">Shader Model 2 (DirectX HLSL)</span></span>](dx-graphics-hlsl-sm2.md)           | <span data-ttu-id="a2dcb-136">不可以</span><span class="sxs-lookup"><span data-stu-id="a2dcb-136">no</span></span>        |
| [<span data-ttu-id="a2dcb-137">著色器模型 1 (DirectX HLSL) </span><span class="sxs-lookup"><span data-stu-id="a2dcb-137">Shader Model 1 (DirectX HLSL)</span></span>](dx-graphics-hlsl-sm1.md)           | <span data-ttu-id="a2dcb-138">不可以</span><span class="sxs-lookup"><span data-stu-id="a2dcb-138">no</span></span>        |



 

## <a name="see-also"></a><span data-ttu-id="a2dcb-139">另請參閱</span><span class="sxs-lookup"><span data-stu-id="a2dcb-139">See also</span></span>

<dl> <dt>

[<span data-ttu-id="a2dcb-140">**(DirectX HLSL) 內建函式**</span><span class="sxs-lookup"><span data-stu-id="a2dcb-140">**Intrinsic Functions (DirectX HLSL)**</span></span>](dx-graphics-hlsl-intrinsic-functions.md)
</dt> </dl>

 

