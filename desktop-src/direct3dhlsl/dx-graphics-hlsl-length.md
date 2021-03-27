---
title: 長度
description: 傳回指定之浮點數向量的長度。
ms.assetid: eb06c87c-d536-448e-becb-762783cc2a77
keywords:
- 長度 HLSL
topic_type:
- apiref
api_name:
- length
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
api_location: ''
ms.openlocfilehash: a7a93b0a7d225a25273a2ab4f8bf1d24656b6ee1
ms.sourcegitcommit: 592c9bbd22ba69802dc353bcb5eb30699f9e9403
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/20/2020
ms.locfileid: "103682496"
---
# <a name="length"></a><span data-ttu-id="36585-104">長度</span><span class="sxs-lookup"><span data-stu-id="36585-104">length</span></span>

<span data-ttu-id="36585-105">傳回指定之浮點數向量的長度。</span><span class="sxs-lookup"><span data-stu-id="36585-105">Returns the length of the specified floating-point vector.</span></span>



| <span data-ttu-id="36585-106">*ret* 長度 (*x*) </span><span class="sxs-lookup"><span data-stu-id="36585-106">*ret* length(*x*)</span></span> |
|-------------------|



 

## <a name="parameters"></a><span data-ttu-id="36585-107">參數</span><span class="sxs-lookup"><span data-stu-id="36585-107">Parameters</span></span>



| <span data-ttu-id="36585-108">項目</span><span class="sxs-lookup"><span data-stu-id="36585-108">Item</span></span>                                                   | <span data-ttu-id="36585-109">描述</span><span class="sxs-lookup"><span data-stu-id="36585-109">Description</span></span>                                     |
|--------------------------------------------------------|-------------------------------------------------|
| <span data-ttu-id="36585-110"><span id="x"></span><span id="X"></span>*X*</span><span class="sxs-lookup"><span data-stu-id="36585-110"><span id="x"></span><span id="X"></span>*x*</span></span><br/> | <span data-ttu-id="36585-111">指定的浮點向量。</span><span class="sxs-lookup"><span data-stu-id="36585-111">The specified floating-point vector.</span></span><br/> |



 

## <a name="return-value"></a><span data-ttu-id="36585-112">傳回值</span><span class="sxs-lookup"><span data-stu-id="36585-112">Return Value</span></span>

<span data-ttu-id="36585-113">表示 *x* 參數長度的浮點純量。</span><span class="sxs-lookup"><span data-stu-id="36585-113">A floating-point scalar that represents the length of the *x* parameter.</span></span>

## <a name="type-description"></a><span data-ttu-id="36585-114">類型描述</span><span class="sxs-lookup"><span data-stu-id="36585-114">Type Description</span></span>



| <span data-ttu-id="36585-115">Name</span><span class="sxs-lookup"><span data-stu-id="36585-115">Name</span></span>  | [<span data-ttu-id="36585-116">**範本類型**</span><span class="sxs-lookup"><span data-stu-id="36585-116">**Template Type**</span></span>](dx-graphics-hlsl-intrinsic-functions.md)                       | [<span data-ttu-id="36585-117">**元件類型**</span><span class="sxs-lookup"><span data-stu-id="36585-117">**Component Type**</span></span>](dx-graphics-hlsl-intrinsic-functions.md) | <span data-ttu-id="36585-118">大小</span><span class="sxs-lookup"><span data-stu-id="36585-118">Size</span></span> |
|-------|-------------------------------------------------------------------------------------|----------------------------------------------------------------|------|
| <span data-ttu-id="36585-119">*x*</span><span class="sxs-lookup"><span data-stu-id="36585-119">*x*</span></span>   | [<span data-ttu-id="36585-120">**向量**</span><span class="sxs-lookup"><span data-stu-id="36585-120">**vector**</span></span>](dx-graphics-hlsl-intrinsic-functions.md) | [<span data-ttu-id="36585-121">**浮動**</span><span class="sxs-lookup"><span data-stu-id="36585-121">**float**</span></span>](/windows/desktop/WinProg/windows-data-types)                        | <span data-ttu-id="36585-122">任意</span><span class="sxs-lookup"><span data-stu-id="36585-122">any</span></span>  |
| <span data-ttu-id="36585-123">*Ret*</span><span class="sxs-lookup"><span data-stu-id="36585-123">*ret*</span></span> | [<span data-ttu-id="36585-124">**純量 (scalar)**</span><span class="sxs-lookup"><span data-stu-id="36585-124">**scalar**</span></span>](dx-graphics-hlsl-intrinsic-functions.md) | [<span data-ttu-id="36585-125">**FLOAT**</span><span class="sxs-lookup"><span data-stu-id="36585-125">**float**</span></span>](/windows/desktop/WinProg/windows-data-types)                        | <span data-ttu-id="36585-126">1</span><span class="sxs-lookup"><span data-stu-id="36585-126">1</span></span>    |



 

## <a name="minimum-shader-model"></a><span data-ttu-id="36585-127">最小著色器模型</span><span class="sxs-lookup"><span data-stu-id="36585-127">Minimum Shader Model</span></span>

<span data-ttu-id="36585-128">下列著色器模型支援此函數。</span><span class="sxs-lookup"><span data-stu-id="36585-128">This function is supported in the following shader models.</span></span>



| <span data-ttu-id="36585-129">著色器模型</span><span class="sxs-lookup"><span data-stu-id="36585-129">Shader Model</span></span>                                                                       | <span data-ttu-id="36585-130">支援</span><span class="sxs-lookup"><span data-stu-id="36585-130">Supported</span></span>           |
|------------------------------------------------------------------------------------|---------------------|
| <span data-ttu-id="36585-131">[著色器模型 2 (DIRECTX HLSL) ](dx-graphics-hlsl-sm2.md) 和更高的著色器模型</span><span class="sxs-lookup"><span data-stu-id="36585-131">[Shader Model 2 (DirectX HLSL)](dx-graphics-hlsl-sm2.md) and higher shader models</span></span> | <span data-ttu-id="36585-132">是</span><span class="sxs-lookup"><span data-stu-id="36585-132">yes</span></span>                 |
| [<span data-ttu-id="36585-133">著色器模型 1 (DirectX HLSL) </span><span class="sxs-lookup"><span data-stu-id="36585-133">Shader Model 1 (DirectX HLSL)</span></span>](dx-graphics-hlsl-sm1.md)                          | <span data-ttu-id="36585-134">是 (\_ \_ 只有) 的 vs 1</span><span class="sxs-lookup"><span data-stu-id="36585-134">yes (vs\_1\_1 only)</span></span> |



 

## <a name="see-also"></a><span data-ttu-id="36585-135">另請參閱</span><span class="sxs-lookup"><span data-stu-id="36585-135">See also</span></span>

<dl> <dt>

[<span data-ttu-id="36585-136">**(DirectX HLSL) 內建函式**</span><span class="sxs-lookup"><span data-stu-id="36585-136">**Intrinsic Functions (DirectX HLSL)**</span></span>](dx-graphics-hlsl-intrinsic-functions.md)
</dt> </dl>

 

