---
title: 度
description: 將指定的值從弧度轉換成度數。
ms.assetid: e60a3ec4-9177-457a-8314-a5788f353633
keywords:
- 度數 HLSL
topic_type:
- apiref
api_name:
- degrees
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
api_location: ''
ms.openlocfilehash: 47d8bba0ee43da81a18baaeaffca0e3c917e460d
ms.sourcegitcommit: 592c9bbd22ba69802dc353bcb5eb30699f9e9403
ms.translationtype: HT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/20/2020
ms.locfileid: "104375696"
---
# <a name="degrees"></a><span data-ttu-id="ae9f6-104">度</span><span class="sxs-lookup"><span data-stu-id="ae9f6-104">degrees</span></span>

<span data-ttu-id="ae9f6-105">將指定的值從弧度轉換成度數。</span><span class="sxs-lookup"><span data-stu-id="ae9f6-105">Converts the specified value from radians to degrees.</span></span>



| <span data-ttu-id="ae9f6-106">*ret* 度數 (*x*) </span><span class="sxs-lookup"><span data-stu-id="ae9f6-106">*ret* degrees(*x*)</span></span> |
|--------------------|



 

## <a name="parameters"></a><span data-ttu-id="ae9f6-107">參數</span><span class="sxs-lookup"><span data-stu-id="ae9f6-107">Parameters</span></span>



| <span data-ttu-id="ae9f6-108">項目</span><span class="sxs-lookup"><span data-stu-id="ae9f6-108">Item</span></span>                                                   | <span data-ttu-id="ae9f6-109">描述</span><span class="sxs-lookup"><span data-stu-id="ae9f6-109">Description</span></span>                            |
|--------------------------------------------------------|----------------------------------------|
| <span data-ttu-id="ae9f6-110"><span id="x"></span><span id="X"></span>*X*</span><span class="sxs-lookup"><span data-stu-id="ae9f6-110"><span id="x"></span><span id="X"></span>*x*</span></span><br/> | <span data-ttu-id="ae9f6-111">\[在 \] 指定的值中。</span><span class="sxs-lookup"><span data-stu-id="ae9f6-111">\[in\] The specified value.</span></span><br/> |



 

## <a name="return-value"></a><span data-ttu-id="ae9f6-112">傳回值</span><span class="sxs-lookup"><span data-stu-id="ae9f6-112">Return Value</span></span>

<span data-ttu-id="ae9f6-113">將 *x* 參數從弧度轉換成度數的結果。</span><span class="sxs-lookup"><span data-stu-id="ae9f6-113">The result of converting the *x* parameter from radians to degrees.</span></span>

## <a name="type-description"></a><span data-ttu-id="ae9f6-114">類型描述</span><span class="sxs-lookup"><span data-stu-id="ae9f6-114">Type Description</span></span>



| <span data-ttu-id="ae9f6-115">Name</span><span class="sxs-lookup"><span data-stu-id="ae9f6-115">Name</span></span>  | [<span data-ttu-id="ae9f6-116">**範本類型**</span><span class="sxs-lookup"><span data-stu-id="ae9f6-116">**Template Type**</span></span>](dx-graphics-hlsl-intrinsic-functions.md)                                                  | [<span data-ttu-id="ae9f6-117">**元件類型**</span><span class="sxs-lookup"><span data-stu-id="ae9f6-117">**Component Type**</span></span>](dx-graphics-hlsl-intrinsic-functions.md) | <span data-ttu-id="ae9f6-118">大小</span><span class="sxs-lookup"><span data-stu-id="ae9f6-118">Size</span></span>                           |
|-------|----------------------------------------------------------------------------------------------------------------|----------------------------------------------------------------|--------------------------------|
| <span data-ttu-id="ae9f6-119">*x*</span><span class="sxs-lookup"><span data-stu-id="ae9f6-119">*x*</span></span>   | <span data-ttu-id="ae9f6-120">純 [**量、**](dx-graphics-hlsl-intrinsic-functions.md)**向量** 或 **矩陣**</span><span class="sxs-lookup"><span data-stu-id="ae9f6-120">[**scalar**](dx-graphics-hlsl-intrinsic-functions.md), **vector**, or **matrix**</span></span> | [<span data-ttu-id="ae9f6-121">**浮動**</span><span class="sxs-lookup"><span data-stu-id="ae9f6-121">**float**</span></span>](/windows/desktop/WinProg/windows-data-types)                        | <span data-ttu-id="ae9f6-122">任意</span><span class="sxs-lookup"><span data-stu-id="ae9f6-122">any</span></span>                            |
| <span data-ttu-id="ae9f6-123">*Ret*</span><span class="sxs-lookup"><span data-stu-id="ae9f6-123">*ret*</span></span> | <span data-ttu-id="ae9f6-124">與輸入 *x* 相同</span><span class="sxs-lookup"><span data-stu-id="ae9f6-124">same as input *x*</span></span>                                                                                              | [<span data-ttu-id="ae9f6-125">**浮動**</span><span class="sxs-lookup"><span data-stu-id="ae9f6-125">**float**</span></span>](/windows/desktop/WinProg/windows-data-types)                        | <span data-ttu-id="ae9f6-126">) 為輸入 *x* 的相同維度 (s</span><span class="sxs-lookup"><span data-stu-id="ae9f6-126">same dimension(s) as input *x*</span></span> |



 

## <a name="minimum-shader-model"></a><span data-ttu-id="ae9f6-127">最小著色器模型</span><span class="sxs-lookup"><span data-stu-id="ae9f6-127">Minimum Shader Model</span></span>

<span data-ttu-id="ae9f6-128">下列著色器模型支援此函數。</span><span class="sxs-lookup"><span data-stu-id="ae9f6-128">This function is supported in the following shader models.</span></span>



| <span data-ttu-id="ae9f6-129">著色器模型</span><span class="sxs-lookup"><span data-stu-id="ae9f6-129">Shader Model</span></span>                                                                       | <span data-ttu-id="ae9f6-130">支援</span><span class="sxs-lookup"><span data-stu-id="ae9f6-130">Supported</span></span> |
|------------------------------------------------------------------------------------|-----------|
| <span data-ttu-id="ae9f6-131">[著色器模型 2 (DIRECTX HLSL) ](dx-graphics-hlsl-sm2.md) 和更高的著色器模型</span><span class="sxs-lookup"><span data-stu-id="ae9f6-131">[Shader Model 2 (DirectX HLSL)](dx-graphics-hlsl-sm2.md) and higher shader models</span></span> | <span data-ttu-id="ae9f6-132">是</span><span class="sxs-lookup"><span data-stu-id="ae9f6-132">yes</span></span>       |
| [<span data-ttu-id="ae9f6-133">著色器模型 1 (DirectX HLSL) </span><span class="sxs-lookup"><span data-stu-id="ae9f6-133">Shader Model 1 (DirectX HLSL)</span></span>](dx-graphics-hlsl-sm1.md)                          | <span data-ttu-id="ae9f6-134">vs \_ 1 \_ 1</span><span class="sxs-lookup"><span data-stu-id="ae9f6-134">vs\_1\_1</span></span>  |



 

## <a name="see-also"></a><span data-ttu-id="ae9f6-135">另請參閱</span><span class="sxs-lookup"><span data-stu-id="ae9f6-135">See also</span></span>

<dl> <dt>

[<span data-ttu-id="ae9f6-136">**(DirectX HLSL) 內建函式**</span><span class="sxs-lookup"><span data-stu-id="ae9f6-136">**Intrinsic Functions (DirectX HLSL)**</span></span>](dx-graphics-hlsl-intrinsic-functions.md)
</dt> </dl>

 

