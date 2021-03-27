---
title: 'log2 (Corecrt \_ math .h) '
description: 傳回指定值的以2為底數的對數。
ms.assetid: 0bc75697-92c0-4de5-89bd-2ce824baa03e
keywords:
- log2 HLSL
topic_type:
- apiref
api_name:
- log2
api_location:
- corecrt_math.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 81692071b7886fa3e3096d785bccf80c7eff937a
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 03/15/2021
ms.locfileid: "103946244"
---
# <a name="log2"></a><span data-ttu-id="728e4-104">log2</span><span class="sxs-lookup"><span data-stu-id="728e4-104">log2</span></span>

<span data-ttu-id="728e4-105">傳回指定值的以2為底數的對數。</span><span class="sxs-lookup"><span data-stu-id="728e4-105">Returns the base-2 logarithm of the specified value.</span></span>



| <span data-ttu-id="728e4-106">*ret* log2 (*x*) </span><span class="sxs-lookup"><span data-stu-id="728e4-106">*ret* log2(*x*)</span></span> |
|-----------------|



 

## <a name="parameters"></a><span data-ttu-id="728e4-107">參數</span><span class="sxs-lookup"><span data-stu-id="728e4-107">Parameters</span></span>



| <span data-ttu-id="728e4-108">項目</span><span class="sxs-lookup"><span data-stu-id="728e4-108">Item</span></span>                                                   | <span data-ttu-id="728e4-109">描述</span><span class="sxs-lookup"><span data-stu-id="728e4-109">Description</span></span>                            |
|--------------------------------------------------------|----------------------------------------|
| <span data-ttu-id="728e4-110"><span id="x"></span><span id="X"></span>*X*</span><span class="sxs-lookup"><span data-stu-id="728e4-110"><span id="x"></span><span id="X"></span>*x*</span></span><br/> | <span data-ttu-id="728e4-111">\[在 \] 指定的值中。</span><span class="sxs-lookup"><span data-stu-id="728e4-111">\[in\] The specified value.</span></span><br/> |



 

## <a name="return-value"></a><span data-ttu-id="728e4-112">傳回值</span><span class="sxs-lookup"><span data-stu-id="728e4-112">Return Value</span></span>

<span data-ttu-id="728e4-113">*X* 參數的以2為底數的對數。</span><span class="sxs-lookup"><span data-stu-id="728e4-113">The base-2 logarithm of the *x* parameter.</span></span> <span data-ttu-id="728e4-114">如果 *x* 參數為負值，則此函式會傳回不定。</span><span class="sxs-lookup"><span data-stu-id="728e4-114">If the *x* parameter is negative, this function returns indefinite.</span></span> <span data-ttu-id="728e4-115">如果 *x* 參數為0，則此函式會傳回 + INF。</span><span class="sxs-lookup"><span data-stu-id="728e4-115">If the *x* parameter is 0, this function returns +INF.</span></span>

## <a name="type-description"></a><span data-ttu-id="728e4-116">類型描述</span><span class="sxs-lookup"><span data-stu-id="728e4-116">Type Description</span></span>



| <span data-ttu-id="728e4-117">Name</span><span class="sxs-lookup"><span data-stu-id="728e4-117">Name</span></span>  | [<span data-ttu-id="728e4-118">**範本類型**</span><span class="sxs-lookup"><span data-stu-id="728e4-118">**Template Type**</span></span>](dx-graphics-hlsl-intrinsic-functions.md)                                                  | [<span data-ttu-id="728e4-119">**元件類型**</span><span class="sxs-lookup"><span data-stu-id="728e4-119">**Component Type**</span></span>](dx-graphics-hlsl-intrinsic-functions.md) | <span data-ttu-id="728e4-120">大小</span><span class="sxs-lookup"><span data-stu-id="728e4-120">Size</span></span>                           |
|-------|----------------------------------------------------------------------------------------------------------------|----------------------------------------------------------------|--------------------------------|
| <span data-ttu-id="728e4-121">*x*</span><span class="sxs-lookup"><span data-stu-id="728e4-121">*x*</span></span>   | <span data-ttu-id="728e4-122">純 [**量、**](dx-graphics-hlsl-intrinsic-functions.md)**向量** 或 **矩陣**</span><span class="sxs-lookup"><span data-stu-id="728e4-122">[**scalar**](dx-graphics-hlsl-intrinsic-functions.md), **vector**, or **matrix**</span></span> | [<span data-ttu-id="728e4-123">**浮動**</span><span class="sxs-lookup"><span data-stu-id="728e4-123">**float**</span></span>](/windows/desktop/WinProg/windows-data-types)                        | <span data-ttu-id="728e4-124">任意</span><span class="sxs-lookup"><span data-stu-id="728e4-124">any</span></span>                            |
| <span data-ttu-id="728e4-125">*Ret*</span><span class="sxs-lookup"><span data-stu-id="728e4-125">*ret*</span></span> | <span data-ttu-id="728e4-126">與輸入 *x* 相同</span><span class="sxs-lookup"><span data-stu-id="728e4-126">same as input *x*</span></span>                                                                                              | [<span data-ttu-id="728e4-127">**浮動**</span><span class="sxs-lookup"><span data-stu-id="728e4-127">**float**</span></span>](/windows/desktop/WinProg/windows-data-types)                        | <span data-ttu-id="728e4-128">) 為輸入 *x* 的相同維度 (s</span><span class="sxs-lookup"><span data-stu-id="728e4-128">same dimension(s) as input *x*</span></span> |



 

## <a name="minimum-shader-model"></a><span data-ttu-id="728e4-129">最小著色器模型</span><span class="sxs-lookup"><span data-stu-id="728e4-129">Minimum Shader Model</span></span>

<span data-ttu-id="728e4-130">下列著色器模型支援此函數。</span><span class="sxs-lookup"><span data-stu-id="728e4-130">This function is supported in the following shader models.</span></span>



| <span data-ttu-id="728e4-131">著色器模型</span><span class="sxs-lookup"><span data-stu-id="728e4-131">Shader Model</span></span>                                                                       | <span data-ttu-id="728e4-132">支援</span><span class="sxs-lookup"><span data-stu-id="728e4-132">Supported</span></span>           |
|------------------------------------------------------------------------------------|---------------------|
| <span data-ttu-id="728e4-133">[著色器模型 2 (DIRECTX HLSL) ](dx-graphics-hlsl-sm2.md) 和更高的著色器模型</span><span class="sxs-lookup"><span data-stu-id="728e4-133">[Shader Model 2 (DirectX HLSL)](dx-graphics-hlsl-sm2.md) and higher shader models</span></span> | <span data-ttu-id="728e4-134">是</span><span class="sxs-lookup"><span data-stu-id="728e4-134">yes</span></span>                 |
| [<span data-ttu-id="728e4-135">著色器模型 1 (DirectX HLSL) </span><span class="sxs-lookup"><span data-stu-id="728e4-135">Shader Model 1 (DirectX HLSL)</span></span>](dx-graphics-hlsl-sm1.md)                          | <span data-ttu-id="728e4-136">是 (\_ \_ 只有) 的 vs 1</span><span class="sxs-lookup"><span data-stu-id="728e4-136">yes (vs\_1\_1 only)</span></span> |



 

## <a name="requirements"></a><span data-ttu-id="728e4-137">規格需求</span><span class="sxs-lookup"><span data-stu-id="728e4-137">Requirements</span></span>



| <span data-ttu-id="728e4-138">需求</span><span class="sxs-lookup"><span data-stu-id="728e4-138">Requirement</span></span> | <span data-ttu-id="728e4-139">值</span><span class="sxs-lookup"><span data-stu-id="728e4-139">Value</span></span> |
|-------------------|--------------------------------------------------------------------------------------------|
| <span data-ttu-id="728e4-140">標頭</span><span class="sxs-lookup"><span data-stu-id="728e4-140">Header</span></span><br/> | <dl> <span data-ttu-id="728e4-141"><dt>Corecrt \_ math。h</dt></span><span class="sxs-lookup"><span data-stu-id="728e4-141"><dt>Corecrt\_math.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="728e4-142">另請參閱</span><span class="sxs-lookup"><span data-stu-id="728e4-142">See also</span></span>

<dl> <dt>

[<span data-ttu-id="728e4-143">**(DirectX HLSL) 內建函式**</span><span class="sxs-lookup"><span data-stu-id="728e4-143">**Intrinsic Functions (DirectX HLSL)**</span></span>](dx-graphics-hlsl-intrinsic-functions.md)
</dt> </dl>

 

