---
title: asuint
description: 以不帶正負號的整數來解讀 x 的位模式。
ms.assetid: 8401001d-f9ee-43da-9756-f311e9f2bb20
keywords:
- asuint HLSL
topic_type:
- apiref
api_name:
- asuint
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
api_location: ''
ms.openlocfilehash: 1a2d351eb36c6910790e2dceb94e3a97951ad850
ms.sourcegitcommit: 592c9bbd22ba69802dc353bcb5eb30699f9e9403
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/20/2020
ms.locfileid: "104971772"
---
# <a name="asuint"></a><span data-ttu-id="8bb92-104">asuint</span><span class="sxs-lookup"><span data-stu-id="8bb92-104">asuint</span></span>

<span data-ttu-id="8bb92-105">以不帶正負號的整數來解讀 *x* 的位模式。</span><span class="sxs-lookup"><span data-stu-id="8bb92-105">Interprets the bit pattern of *x* as an unsigned integer.</span></span>



| <span data-ttu-id="8bb92-106">ret asuint (*x*) </span><span class="sxs-lookup"><span data-stu-id="8bb92-106">ret asuint(*x*)</span></span> |
|-----------------|



 

## <a name="parameters"></a><span data-ttu-id="8bb92-107">參數</span><span class="sxs-lookup"><span data-stu-id="8bb92-107">Parameters</span></span>



| <span data-ttu-id="8bb92-108">項目</span><span class="sxs-lookup"><span data-stu-id="8bb92-108">Item</span></span>                                                   | <span data-ttu-id="8bb92-109">描述</span><span class="sxs-lookup"><span data-stu-id="8bb92-109">Description</span></span>                        |
|--------------------------------------------------------|------------------------------------|
| <span data-ttu-id="8bb92-110"><span id="x"></span><span id="X"></span>*X*</span><span class="sxs-lookup"><span data-stu-id="8bb92-110"><span id="x"></span><span id="X"></span>*x*</span></span><br/> | <span data-ttu-id="8bb92-111">\[在 \] 輸入值中。</span><span class="sxs-lookup"><span data-stu-id="8bb92-111">\[in\] The input value.</span></span><br/> |



 

## <a name="return-value"></a><span data-ttu-id="8bb92-112">傳回值</span><span class="sxs-lookup"><span data-stu-id="8bb92-112">Return Value</span></span>

<span data-ttu-id="8bb92-113">轉譯為不帶正負號整數的輸入。</span><span class="sxs-lookup"><span data-stu-id="8bb92-113">The input interpreted as an unsigned integer.</span></span>

## <a name="type-description"></a><span data-ttu-id="8bb92-114">類型描述</span><span class="sxs-lookup"><span data-stu-id="8bb92-114">Type Description</span></span>



| <span data-ttu-id="8bb92-115">Name</span><span class="sxs-lookup"><span data-stu-id="8bb92-115">Name</span></span>  | [<span data-ttu-id="8bb92-116">**範本類型**</span><span class="sxs-lookup"><span data-stu-id="8bb92-116">**Template Type**</span></span>](dx-graphics-hlsl-intrinsic-functions.md)                                                  | [<span data-ttu-id="8bb92-117">**元件類型**</span><span class="sxs-lookup"><span data-stu-id="8bb92-117">**Component Type**</span></span>](dx-graphics-hlsl-intrinsic-functions.md)                 | <span data-ttu-id="8bb92-118">大小</span><span class="sxs-lookup"><span data-stu-id="8bb92-118">Size</span></span>                           |
|-------|----------------------------------------------------------------------------------------------------------------|--------------------------------------------------------------------------------|--------------------------------|
| <span data-ttu-id="8bb92-119">*x*</span><span class="sxs-lookup"><span data-stu-id="8bb92-119">*x*</span></span>   | <span data-ttu-id="8bb92-120">純 [**量、**](dx-graphics-hlsl-intrinsic-functions.md)**向量** 或 **矩陣**</span><span class="sxs-lookup"><span data-stu-id="8bb92-120">[**scalar**](dx-graphics-hlsl-intrinsic-functions.md), **vector**, or **matrix**</span></span> | <span data-ttu-id="8bb92-121">[**float**](/windows/desktop/WinProg/windows-data-types)、 [ **int**](/windows/desktop/WinProg/windows-data-types)</span><span class="sxs-lookup"><span data-stu-id="8bb92-121">[**float**](/windows/desktop/WinProg/windows-data-types), [**int**](/windows/desktop/WinProg/windows-data-types)</span></span> | <span data-ttu-id="8bb92-122">任意</span><span class="sxs-lookup"><span data-stu-id="8bb92-122">any</span></span>                            |
| <span data-ttu-id="8bb92-123">*Ret*</span><span class="sxs-lookup"><span data-stu-id="8bb92-123">*ret*</span></span> | <span data-ttu-id="8bb92-124">與輸入 *x* 相同</span><span class="sxs-lookup"><span data-stu-id="8bb92-124">same as input *x*</span></span>                                                                                              | [<span data-ttu-id="8bb92-125">**uint**</span><span class="sxs-lookup"><span data-stu-id="8bb92-125">**uint**</span></span>](/windows/desktop/WinProg/windows-data-types)                                         | <span data-ttu-id="8bb92-126">) 為輸入 *x* 的相同維度 (s</span><span class="sxs-lookup"><span data-stu-id="8bb92-126">same dimension(s) as input *x*</span></span> |



 

## <a name="minimum-shader-model"></a><span data-ttu-id="8bb92-127">最小著色器模型</span><span class="sxs-lookup"><span data-stu-id="8bb92-127">Minimum Shader Model</span></span>

<span data-ttu-id="8bb92-128">下列著色器模型支援此函數。</span><span class="sxs-lookup"><span data-stu-id="8bb92-128">This function is supported in the following shader models.</span></span>



| <span data-ttu-id="8bb92-129">著色器模型</span><span class="sxs-lookup"><span data-stu-id="8bb92-129">Shader Model</span></span>                                                        | <span data-ttu-id="8bb92-130">支援</span><span class="sxs-lookup"><span data-stu-id="8bb92-130">Supported</span></span> |
|---------------------------------------------------------------------|-----------|
| <span data-ttu-id="8bb92-131">[著色器模型 4](dx-graphics-hlsl-sm4.md) 和更高的著色器模型</span><span class="sxs-lookup"><span data-stu-id="8bb92-131">[Shader Model 4](dx-graphics-hlsl-sm4.md) and higher shader models</span></span> | <span data-ttu-id="8bb92-132">是</span><span class="sxs-lookup"><span data-stu-id="8bb92-132">yes</span></span>       |
| [<span data-ttu-id="8bb92-133">著色器模型 3 (DirectX HLSL) </span><span class="sxs-lookup"><span data-stu-id="8bb92-133">Shader Model 3 (DirectX HLSL)</span></span>](dx-graphics-hlsl-sm3.md)           | <span data-ttu-id="8bb92-134">不可以</span><span class="sxs-lookup"><span data-stu-id="8bb92-134">no</span></span>        |
| [<span data-ttu-id="8bb92-135">著色器模型 2 (DirectX HLSL) </span><span class="sxs-lookup"><span data-stu-id="8bb92-135">Shader Model 2 (DirectX HLSL)</span></span>](dx-graphics-hlsl-sm2.md)           | <span data-ttu-id="8bb92-136">不可以</span><span class="sxs-lookup"><span data-stu-id="8bb92-136">no</span></span>        |
| [<span data-ttu-id="8bb92-137">著色器模型 1 (DirectX HLSL) </span><span class="sxs-lookup"><span data-stu-id="8bb92-137">Shader Model 1 (DirectX HLSL)</span></span>](dx-graphics-hlsl-sm1.md)           | <span data-ttu-id="8bb92-138">不可以</span><span class="sxs-lookup"><span data-stu-id="8bb92-138">no</span></span>        |



 

## <a name="see-also"></a><span data-ttu-id="8bb92-139">另請參閱</span><span class="sxs-lookup"><span data-stu-id="8bb92-139">See also</span></span>

<dl> <dt>

[<span data-ttu-id="8bb92-140">**(DirectX HLSL) 內建函式**</span><span class="sxs-lookup"><span data-stu-id="8bb92-140">**Intrinsic Functions (DirectX HLSL)**</span></span>](dx-graphics-hlsl-intrinsic-functions.md)
</dt> </dl>

 

