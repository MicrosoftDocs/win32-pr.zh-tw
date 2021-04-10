---
description: 參數為效果變數。
ms.assetid: vs|directx_sdk|~\parameters.htm
title: " (Direct3D 9) 的參數"
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 2e5c78a4f6c0518c99b61be10b721d98b17630ab
ms.sourcegitcommit: a47bd86f517de76374e4fff33cfeb613eb259a7e
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/06/2021
ms.locfileid: "104109889"
---
# <a name="parameters-direct3d-9"></a><span data-ttu-id="969ea-103"> (Direct3D 9) 的參數</span><span class="sxs-lookup"><span data-stu-id="969ea-103">Parameters (Direct3D 9)</span></span>

<span data-ttu-id="969ea-104">參數為效果變數。</span><span class="sxs-lookup"><span data-stu-id="969ea-104">Parameters are effect variables.</span></span>

## <a name="syntax"></a><span data-ttu-id="969ea-105">Syntax</span><span class="sxs-lookup"><span data-stu-id="969ea-105">Syntax</span></span>

<span data-ttu-id="969ea-106">*使用類型識別碼* \[ ：*語義* \] \[ < *注釋 (s)* > \] \[ =  *運算式* \] ;</span><span class="sxs-lookup"><span data-stu-id="969ea-106">*usage type ID* \[: *semantic*\] \[<*annotation(s)*>\] \[= *expression*\];</span></span>

<span data-ttu-id="969ea-107">您可以使用 [**ID3DXEffect**](id3dxeffect.md) 或 [**ID3DXEffectCompiler**](id3dxeffectcompiler.md)，從應用程式讀取和寫入參數。</span><span class="sxs-lookup"><span data-stu-id="969ea-107">Parameters can be read from and written to by the application with [**ID3DXEffect**](id3dxeffect.md) or [**ID3DXEffectCompiler**](id3dxeffectcompiler.md).</span></span>

<span data-ttu-id="969ea-108">您可以在函式和技術中參考參數， (特別是在) 狀態指派的右側。</span><span class="sxs-lookup"><span data-stu-id="969ea-108">Parameters can be referenced in functions and in techniques (specifically, in the right side of state assignments).</span></span>



| <span data-ttu-id="969ea-109">項目</span><span class="sxs-lookup"><span data-stu-id="969ea-109">Item</span></span>                                                                                 | <span data-ttu-id="969ea-110">描述</span><span class="sxs-lookup"><span data-stu-id="969ea-110">Description</span></span>                                                                                                                                                     |
|--------------------------------------------------------------------------------------|-----------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="969ea-111"><span id="usage"></span><span id="USAGE"></span>*使用*</span><span class="sxs-lookup"><span data-stu-id="969ea-111"><span id="usage"></span><span id="USAGE"></span>*usage*</span></span><br/>                   | <span data-ttu-id="969ea-112">參數的範圍。</span><span class="sxs-lookup"><span data-stu-id="969ea-112">Scope of the parameter.</span></span> <span data-ttu-id="969ea-113">請參閱 [ (Direct3D 9) 的使用方式和常 ](usages-and-literals.md)值。</span><span class="sxs-lookup"><span data-stu-id="969ea-113">See [Usages and Literals (Direct3D 9)](usages-and-literals.md).</span></span><br/>                                                             |
| <span data-ttu-id="969ea-114"><span id="type"></span><span id="TYPE"></span>*類型*</span><span class="sxs-lookup"><span data-stu-id="969ea-114"><span id="type"></span><span id="TYPE"></span>*type*</span></span><br/>                      | <span data-ttu-id="969ea-115">HLSL 型別的任何有效 [參考](../direct3dhlsl/dx-graphics-hlsl-reference.md) 。</span><span class="sxs-lookup"><span data-stu-id="969ea-115">Any valid [Reference for HLSL](../direct3dhlsl/dx-graphics-hlsl-reference.md) type.</span></span><br/>                                                                        |
| <span data-ttu-id="969ea-116"><span id="ID"></span><span id="id"></span>*Id*</span><span class="sxs-lookup"><span data-stu-id="969ea-116"><span id="ID"></span><span id="id"></span>*ID*</span></span><br/>                            | <span data-ttu-id="969ea-117">唯一名稱。</span><span class="sxs-lookup"><span data-stu-id="969ea-117">A unique name.</span></span><br/>                                                                                                                                       |
| <span data-ttu-id="969ea-118"><span id="semantic"></span><span id="SEMANTIC"></span>*語義*</span><span class="sxs-lookup"><span data-stu-id="969ea-118"><span id="semantic"></span><span id="SEMANTIC"></span>*semantic*</span></span><br/>          | <span data-ttu-id="969ea-119">識別碼規則後面的標記，通常表示參數的使用方式。</span><span class="sxs-lookup"><span data-stu-id="969ea-119">A tag following identifier rules that typically indicates the usage of the parameter.</span></span> <span data-ttu-id="969ea-120">必須是特定類型。</span><span class="sxs-lookup"><span data-stu-id="969ea-120">Must be a particular type.</span></span><br/>                                     |
| <span data-ttu-id="969ea-121"><span id="annotations"></span><span id="ANNOTATIONS"></span>*注釋*</span><span class="sxs-lookup"><span data-stu-id="969ea-121"><span id="annotations"></span><span id="ANNOTATIONS"></span>*annotations*</span></span><br/> | <span data-ttu-id="969ea-122">零個或更多的使用者專屬資訊。</span><span class="sxs-lookup"><span data-stu-id="969ea-122">Zero or more pieces of user-specific information.</span></span> <span data-ttu-id="969ea-123">可以是任何類型。</span><span class="sxs-lookup"><span data-stu-id="969ea-123">May be any type.</span></span> <span data-ttu-id="969ea-124">請參閱 [使用批註將資訊新增至效果參數](using-an-effect.md)。</span><span class="sxs-lookup"><span data-stu-id="969ea-124">See [Add Information to Effect Parameters with Annotations](using-an-effect.md).</span></span><br/> |
| <span data-ttu-id="969ea-125"><span id="expression"></span><span id="EXPRESSION"></span>*表達*</span><span class="sxs-lookup"><span data-stu-id="969ea-125"><span id="expression"></span><span id="EXPRESSION"></span>*expression*</span></span><br/>    | <span data-ttu-id="969ea-126">初始化參數的值。</span><span class="sxs-lookup"><span data-stu-id="969ea-126">Initializes the parameter's value.</span></span> <span data-ttu-id="969ea-127">請參閱 [ (Direct3D 9) 的運算式 ](expressions.md)。</span><span class="sxs-lookup"><span data-stu-id="969ea-127">See [Expressions (Direct3D 9)](expressions.md).</span></span><br/>                                                                  |



 

<span data-ttu-id="969ea-128">參數可以初始化為 HLSL 運算式的任何有效 [參考](../direct3dhlsl/dx-graphics-hlsl-reference.md) ，以縮減為常值。</span><span class="sxs-lookup"><span data-stu-id="969ea-128">Parameters can be initialized to any valid [Reference for HLSL](../direct3dhlsl/dx-graphics-hlsl-reference.md) expression that reduces to a literal value.</span></span>

<span data-ttu-id="969ea-129">執行狀態指派或函式呼叫時，不會變更參數值。</span><span class="sxs-lookup"><span data-stu-id="969ea-129">Parameter values are not changed by the execution of state assignment or function calls.</span></span>

## <a name="related-topics"></a><span data-ttu-id="969ea-130">相關主題</span><span class="sxs-lookup"><span data-stu-id="969ea-130">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="969ea-131">效果格式</span><span class="sxs-lookup"><span data-stu-id="969ea-131">Effect Format</span></span>](dx9-graphics-reference-effects-file-format.md)
</dt> </dl>

 

 
