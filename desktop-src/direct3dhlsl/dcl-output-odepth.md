---
title: 'dcl_output oDepth (sm4-asm) '
description: 'dcl \_ 輸出 oDepth (sm4-asm) '
ms.assetid: 7ee3026d-507f-4aa8-8335-d92c5f649f46
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- apiref
api_name: ''
api_type: ''
api_location: ''
ms.openlocfilehash: 43580a542c1a66961cfa7434c65cd8d271fb0367
ms.sourcegitcommit: fe03c5d92ca6a0d66a114b2303e99c0a19241ffb
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 11/20/2019
ms.locfileid: "104313755"
---
# <a name="dcl_output-odepth-sm4---asm"></a><span data-ttu-id="4088b-103">dcl \_ 輸出 oDepth (sm4-asm) </span><span class="sxs-lookup"><span data-stu-id="4088b-103">dcl\_output oDepth (sm4 - asm)</span></span>

<span data-ttu-id="4088b-104">宣告圖元著色器會使用輸出深度暫存器。</span><span class="sxs-lookup"><span data-stu-id="4088b-104">Declares that a pixel shader will use the output-depth register.</span></span>



| <span data-ttu-id="4088b-105">dcl \_ 輸出 oDepth</span><span class="sxs-lookup"><span data-stu-id="4088b-105">dcl\_output oDepth</span></span> |
|--------------------|



 

<span data-ttu-id="4088b-106">輸出深度暫存器中的值會用於深度比較 (如果已啟用深度比較) 。</span><span class="sxs-lookup"><span data-stu-id="4088b-106">The value in the output-depth register is used during a depth comparison (if depth compare is enabled).</span></span>

<span data-ttu-id="4088b-107">此指示適用于下列著色器階段：</span><span class="sxs-lookup"><span data-stu-id="4088b-107">This instruction applies to the following shader stages:</span></span>



| <span data-ttu-id="4088b-108">頂點著色器</span><span class="sxs-lookup"><span data-stu-id="4088b-108">Vertex Shader</span></span> | <span data-ttu-id="4088b-109">幾何著色器</span><span class="sxs-lookup"><span data-stu-id="4088b-109">Geometry Shader</span></span> | <span data-ttu-id="4088b-110">像素著色器</span><span class="sxs-lookup"><span data-stu-id="4088b-110">Pixel Shader</span></span> |
|---------------|-----------------|--------------|
|               |                 | <span data-ttu-id="4088b-111">x</span><span class="sxs-lookup"><span data-stu-id="4088b-111">x</span></span>            |



 

<span data-ttu-id="4088b-112">包含此指令的目的是協助您在元件中進行著色器的偵錯工具。您無法使用著色器模型4來撰寫元件語言中的著色器。</span><span class="sxs-lookup"><span data-stu-id="4088b-112">This instruction is included to aid in debugging a shader in assembly; you cannot author a shader in assembly language using Shader Model 4.</span></span>

## <a name="example"></a><span data-ttu-id="4088b-113">範例</span><span class="sxs-lookup"><span data-stu-id="4088b-113">Example</span></span>

<span data-ttu-id="4088b-114">以下是一些範例。</span><span class="sxs-lookup"><span data-stu-id="4088b-114">Here are some examples.</span></span>


```
dcl_output oDepth
```



## <a name="minimum-shader-model"></a><span data-ttu-id="4088b-115">最小著色器模型</span><span class="sxs-lookup"><span data-stu-id="4088b-115">Minimum Shader Model</span></span>

<span data-ttu-id="4088b-116">下列著色器模型支援此函數。</span><span class="sxs-lookup"><span data-stu-id="4088b-116">This function is supported in the following shader models.</span></span>



| <span data-ttu-id="4088b-117">著色器模型</span><span class="sxs-lookup"><span data-stu-id="4088b-117">Shader Model</span></span>                                              | <span data-ttu-id="4088b-118">支援</span><span class="sxs-lookup"><span data-stu-id="4088b-118">Supported</span></span> |
|-----------------------------------------------------------|-----------|
| [<span data-ttu-id="4088b-119">著色器模型5</span><span class="sxs-lookup"><span data-stu-id="4088b-119">Shader Model 5</span></span>](d3d11-graphics-reference-sm5.md)        | <span data-ttu-id="4088b-120">是</span><span class="sxs-lookup"><span data-stu-id="4088b-120">yes</span></span>       |
| [<span data-ttu-id="4088b-121">著色器模型4。1</span><span class="sxs-lookup"><span data-stu-id="4088b-121">Shader Model 4.1</span></span>](dx-graphics-hlsl-sm4.md)              | <span data-ttu-id="4088b-122">是</span><span class="sxs-lookup"><span data-stu-id="4088b-122">yes</span></span>       |
| [<span data-ttu-id="4088b-123">著色器模型4</span><span class="sxs-lookup"><span data-stu-id="4088b-123">Shader Model 4</span></span>](dx-graphics-hlsl-sm4.md)                | <span data-ttu-id="4088b-124">是</span><span class="sxs-lookup"><span data-stu-id="4088b-124">yes</span></span>       |
| [<span data-ttu-id="4088b-125">著色器模型 3 (DirectX HLSL) </span><span class="sxs-lookup"><span data-stu-id="4088b-125">Shader Model 3 (DirectX HLSL)</span></span>](dx-graphics-hlsl-sm3.md) | <span data-ttu-id="4088b-126">不可以</span><span class="sxs-lookup"><span data-stu-id="4088b-126">no</span></span>        |
| [<span data-ttu-id="4088b-127">著色器模型 2 (DirectX HLSL) </span><span class="sxs-lookup"><span data-stu-id="4088b-127">Shader Model 2 (DirectX HLSL)</span></span>](dx-graphics-hlsl-sm2.md) | <span data-ttu-id="4088b-128">不可以</span><span class="sxs-lookup"><span data-stu-id="4088b-128">no</span></span>        |
| [<span data-ttu-id="4088b-129">著色器模型 1 (DirectX HLSL) </span><span class="sxs-lookup"><span data-stu-id="4088b-129">Shader Model 1 (DirectX HLSL)</span></span>](dx-graphics-hlsl-sm1.md) | <span data-ttu-id="4088b-130">不可以</span><span class="sxs-lookup"><span data-stu-id="4088b-130">no</span></span>        |



 

## <a name="related-topics"></a><span data-ttu-id="4088b-131">相關主題</span><span class="sxs-lookup"><span data-stu-id="4088b-131">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="4088b-132">著色器模型4元件 (DirectX HLSL) </span><span class="sxs-lookup"><span data-stu-id="4088b-132">Shader Model 4 Assembly (DirectX HLSL)</span></span>](dx-graphics-hlsl-sm4-asm.md)
</dt> </dl>

 

 




