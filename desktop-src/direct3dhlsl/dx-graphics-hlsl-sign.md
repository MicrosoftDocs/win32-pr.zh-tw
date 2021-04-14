---
title: Sign
description: 傳回 x 的正負號。
ms.assetid: 3e2e04e8-0ffc-4721-a5d8-1ccfa6ca2a1a
keywords:
- 簽署 HLSL
topic_type:
- apiref
api_name:
- sign
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
api_location: ''
ms.openlocfilehash: fc177e72e116394ffd6241e0616b84c9066a68a7
ms.sourcegitcommit: 592c9bbd22ba69802dc353bcb5eb30699f9e9403
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/20/2020
ms.locfileid: "104991006"
---
# <a name="sign"></a><span data-ttu-id="ec17e-104">Sign</span><span class="sxs-lookup"><span data-stu-id="ec17e-104">sign</span></span>

<span data-ttu-id="ec17e-105">傳回 *x* 的正負號。</span><span class="sxs-lookup"><span data-stu-id="ec17e-105">Returns the sign of *x*.</span></span>



| <span data-ttu-id="ec17e-106">*ret* sign (*x*) </span><span class="sxs-lookup"><span data-stu-id="ec17e-106">*ret* sign(*x*)</span></span> |
|-----------------|



 

## <a name="parameters"></a><span data-ttu-id="ec17e-107">參數</span><span class="sxs-lookup"><span data-stu-id="ec17e-107">Parameters</span></span>



| <span data-ttu-id="ec17e-108">項目</span><span class="sxs-lookup"><span data-stu-id="ec17e-108">Item</span></span>                                                   | <span data-ttu-id="ec17e-109">描述</span><span class="sxs-lookup"><span data-stu-id="ec17e-109">Description</span></span>                        |
|--------------------------------------------------------|------------------------------------|
| <span data-ttu-id="ec17e-110"><span id="x"></span><span id="X"></span>*X*</span><span class="sxs-lookup"><span data-stu-id="ec17e-110"><span id="x"></span><span id="X"></span>*x*</span></span><br/> | <span data-ttu-id="ec17e-111">\[在 \] 輸入值中。</span><span class="sxs-lookup"><span data-stu-id="ec17e-111">\[in\] The input value.</span></span><br/> |



 

## <a name="return-value"></a><span data-ttu-id="ec17e-112">傳回值</span><span class="sxs-lookup"><span data-stu-id="ec17e-112">Return Value</span></span>

<span data-ttu-id="ec17e-113">如果 *x* 小於零，則傳回-1;如果 *x* 等於零，則為 0;如果 *x* 大於零，則為1。</span><span class="sxs-lookup"><span data-stu-id="ec17e-113">Returns -1 if *x* is less than zero; 0 if *x* equals zero; and 1 if *x* is greater than zero.</span></span>

## <a name="type-description"></a><span data-ttu-id="ec17e-114">類型描述</span><span class="sxs-lookup"><span data-stu-id="ec17e-114">Type Description</span></span>



| <span data-ttu-id="ec17e-115">Name</span><span class="sxs-lookup"><span data-stu-id="ec17e-115">Name</span></span>  | [<span data-ttu-id="ec17e-116">**範本類型**</span><span class="sxs-lookup"><span data-stu-id="ec17e-116">**Template Type**</span></span>](dx-graphics-hlsl-intrinsic-functions.md)                                                  | [<span data-ttu-id="ec17e-117">**元件類型**</span><span class="sxs-lookup"><span data-stu-id="ec17e-117">**Component Type**</span></span>](dx-graphics-hlsl-intrinsic-functions.md)                 | <span data-ttu-id="ec17e-118">大小</span><span class="sxs-lookup"><span data-stu-id="ec17e-118">Size</span></span>                           |
|-------|----------------------------------------------------------------------------------------------------------------|--------------------------------------------------------------------------------|--------------------------------|
| <span data-ttu-id="ec17e-119">*x*</span><span class="sxs-lookup"><span data-stu-id="ec17e-119">*x*</span></span>   | <span data-ttu-id="ec17e-120">純 [**量、**](dx-graphics-hlsl-intrinsic-functions.md)**向量** 或 **矩陣**</span><span class="sxs-lookup"><span data-stu-id="ec17e-120">[**scalar**](dx-graphics-hlsl-intrinsic-functions.md), **vector**, or **matrix**</span></span> | <span data-ttu-id="ec17e-121">[**float**](/windows/desktop/WinProg/windows-data-types)、 [ **int**](/windows/desktop/WinProg/windows-data-types)</span><span class="sxs-lookup"><span data-stu-id="ec17e-121">[**float**](/windows/desktop/WinProg/windows-data-types), [**int**](/windows/desktop/WinProg/windows-data-types)</span></span> | <span data-ttu-id="ec17e-122">任意</span><span class="sxs-lookup"><span data-stu-id="ec17e-122">any</span></span>                            |
| <span data-ttu-id="ec17e-123">*Ret*</span><span class="sxs-lookup"><span data-stu-id="ec17e-123">*ret*</span></span> | <span data-ttu-id="ec17e-124">與輸入 *x* 相同</span><span class="sxs-lookup"><span data-stu-id="ec17e-124">same as input *x*</span></span>                                                                                              | [<span data-ttu-id="ec17e-125">**int**</span><span class="sxs-lookup"><span data-stu-id="ec17e-125">**int**</span></span>](/windows/desktop/WinProg/windows-data-types)                                          | <span data-ttu-id="ec17e-126">) 為輸入 *x* 的相同維度 (s</span><span class="sxs-lookup"><span data-stu-id="ec17e-126">same dimension(s) as input *x*</span></span> |



 

## <a name="minimum-shader-model"></a><span data-ttu-id="ec17e-127">最小著色器模型</span><span class="sxs-lookup"><span data-stu-id="ec17e-127">Minimum Shader Model</span></span>

<span data-ttu-id="ec17e-128">下列著色器模型支援此函數。</span><span class="sxs-lookup"><span data-stu-id="ec17e-128">This function is supported in the following shader models.</span></span>



| <span data-ttu-id="ec17e-129">著色器模型</span><span class="sxs-lookup"><span data-stu-id="ec17e-129">Shader Model</span></span>                                                                       | <span data-ttu-id="ec17e-130">支援</span><span class="sxs-lookup"><span data-stu-id="ec17e-130">Supported</span></span>                   |
|------------------------------------------------------------------------------------|-----------------------------|
| <span data-ttu-id="ec17e-131">[著色器模型 2 (DIRECTX HLSL) ](dx-graphics-hlsl-sm2.md) 和更高的著色器模型</span><span class="sxs-lookup"><span data-stu-id="ec17e-131">[Shader Model 2 (DirectX HLSL)](dx-graphics-hlsl-sm2.md) and higher shader models</span></span> | <span data-ttu-id="ec17e-132">是</span><span class="sxs-lookup"><span data-stu-id="ec17e-132">yes</span></span>                         |
| [<span data-ttu-id="ec17e-133">著色器模型 1 (DirectX HLSL) </span><span class="sxs-lookup"><span data-stu-id="ec17e-133">Shader Model 1 (DirectX HLSL)</span></span>](dx-graphics-hlsl-sm1.md)                          | <span data-ttu-id="ec17e-134">是 (vs \_ 1 \_ 1 和 ps \_ 1 \_ 4) </span><span class="sxs-lookup"><span data-stu-id="ec17e-134">yes (vs\_1\_1 and ps\_1\_4)</span></span> |



 

## <a name="see-also"></a><span data-ttu-id="ec17e-135">另請參閱</span><span class="sxs-lookup"><span data-stu-id="ec17e-135">See also</span></span>

<dl> <dt>

[<span data-ttu-id="ec17e-136">**(DirectX HLSL) 內建函式**</span><span class="sxs-lookup"><span data-stu-id="ec17e-136">**Intrinsic Functions (DirectX HLSL)**</span></span>](dx-graphics-hlsl-intrinsic-functions.md)
</dt> </dl>

 

