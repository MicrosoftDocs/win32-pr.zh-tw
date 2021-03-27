---
title: Asm 著色器參考
description: 著色器會驅動可程式化圖形管線。
ms.assetid: 2c58815c-83b5-4ae8-a192-ba865b485bd6
ms.topic: article
ms.date: 05/31/2018
topic_type:
- kbArticle
api_name: ''
api_type: ''
api_location: ''
ms.openlocfilehash: 2941f4c32d03187ce08266bf1382cd1d94301ce0
ms.sourcegitcommit: 477b1efe7d9c2f91d5f2ac588a20edf348b1c734
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 12/10/2019
ms.locfileid: "104971644"
---
# <a name="asm-shader-reference"></a><span data-ttu-id="f833b-103">Asm 著色器參考</span><span class="sxs-lookup"><span data-stu-id="f833b-103">Asm Shader Reference</span></span>

<span data-ttu-id="f833b-104">著色器會驅動可程式化圖形管線。</span><span class="sxs-lookup"><span data-stu-id="f833b-104">Shaders drive the programmable graphics pipeline.</span></span>

## <a name="vertex-shader-reference"></a><span data-ttu-id="f833b-105">頂點著色器參考</span><span class="sxs-lookup"><span data-stu-id="f833b-105">Vertex Shader Reference</span></span>

-   [<span data-ttu-id="f833b-106">vs \_ 1 \_ 1</span><span class="sxs-lookup"><span data-stu-id="f833b-106">vs\_1\_1</span></span>](dx9-graphics-reference-asm-vs-1-1.md)
-   [<span data-ttu-id="f833b-107">vs \_ 2 \_ 0</span><span class="sxs-lookup"><span data-stu-id="f833b-107">vs\_2\_0</span></span>](dx9-graphics-reference-asm-vs-2-0.md)
-   [<span data-ttu-id="f833b-108">vs \_ 2 \_ x</span><span class="sxs-lookup"><span data-stu-id="f833b-108">vs\_2\_x</span></span>](dx9-graphics-reference-asm-vs-2-x.md)
-   [<span data-ttu-id="f833b-109">vs \_ 3 \_ 0</span><span class="sxs-lookup"><span data-stu-id="f833b-109">vs\_3\_0</span></span>](dx9-graphics-reference-asm-vs-3-0.md)

<span data-ttu-id="f833b-110">[頂點著色器差異](dx9-graphics-reference-asm-vs-differences.md) 摘要說明頂點著色器版本之間的差異。</span><span class="sxs-lookup"><span data-stu-id="f833b-110">[Vertex Shader Differences](dx9-graphics-reference-asm-vs-differences.md) summarizes the differences between vertex shader versions.</span></span>

## <a name="pixel-shader-reference"></a><span data-ttu-id="f833b-111">圖元著色器參考</span><span class="sxs-lookup"><span data-stu-id="f833b-111">Pixel Shader Reference</span></span>

-   [<span data-ttu-id="f833b-112">ps \_ 1 \_ 1、ps \_ 1 \_ 2、ps \_ 1 \_ 3、ps \_ 1 \_ 4</span><span class="sxs-lookup"><span data-stu-id="f833b-112">ps\_1\_1, ps\_1\_2, ps\_1\_3, ps\_1\_4</span></span>](dx9-graphics-reference-asm-ps-1-x.md)
-   [<span data-ttu-id="f833b-113">ps \_ 2 \_ 0</span><span class="sxs-lookup"><span data-stu-id="f833b-113">ps\_2\_0</span></span>](dx9-graphics-reference-asm-ps-2-0.md)
-   [<span data-ttu-id="f833b-114">ps \_ 2 \_ x</span><span class="sxs-lookup"><span data-stu-id="f833b-114">ps\_2\_x</span></span>](dx9-graphics-reference-asm-ps-2-x.md)
-   [<span data-ttu-id="f833b-115">ps \_ 3 \_ 0</span><span class="sxs-lookup"><span data-stu-id="f833b-115">ps\_3\_0</span></span>](dx9-graphics-reference-asm-ps-3-0.md)

<span data-ttu-id="f833b-116">[圖元著色器差異](dx9-graphics-reference-asm-ps-differences.md) 摘要說明圖元著色器版本之間的差異。</span><span class="sxs-lookup"><span data-stu-id="f833b-116">[Pixel Shader Differences](dx9-graphics-reference-asm-ps-differences.md) summarizes the differences between pixel shader versions.</span></span>

## <a name="shader-model-4-and-5-reference"></a><span data-ttu-id="f833b-117">著色器模型4和5參考</span><span class="sxs-lookup"><span data-stu-id="f833b-117">Shader Model 4 and 5 Reference</span></span>

<span data-ttu-id="f833b-118">[著色器模型4元件](dx-graphics-hlsl-sm4-asm.md)和[著色器模型5元件](shader-model-5-assembly--directx-hlsl-.md)章節描述著色器模型4和5支援的指示。</span><span class="sxs-lookup"><span data-stu-id="f833b-118">The [Shader Model 4 Assembly](dx-graphics-hlsl-sm4-asm.md) and [Shader Model 5 Assembly](shader-model-5-assembly--directx-hlsl-.md) sections describe the instructions that shader model 4 and 5 support.</span></span>

## <a name="behavior-of-constant-registers-in-assembly-shaders"></a><span data-ttu-id="f833b-119">元件著色器中常數暫存器的行為</span><span class="sxs-lookup"><span data-stu-id="f833b-119">Behavior of Constant Registers in Assembly Shaders</span></span>

<span data-ttu-id="f833b-120">有兩種方式可以在元件著色器中設定常數暫存器：</span><span class="sxs-lookup"><span data-stu-id="f833b-120">There are two ways to set constant registers in an assembly shader:</span></span>

-   <span data-ttu-id="f833b-121">使用其中一個 def 指令來宣告元件程式碼中的著色器常數 \* 。</span><span class="sxs-lookup"><span data-stu-id="f833b-121">Declare a shader constant in assembly code using one of the def\* instructions.</span></span>
-   <span data-ttu-id="f833b-122">使用其中一個 Set \* \* \* ShaderConstant \* API 方法。</span><span class="sxs-lookup"><span data-stu-id="f833b-122">Use one of the Set\*\*\*ShaderConstant\* API methods.</span></span>

### <a name="direct3d-9-shader-constants"></a><span data-ttu-id="f833b-123">Direct3D 9 著色器常數</span><span class="sxs-lookup"><span data-stu-id="f833b-123">Direct3D 9 Shader Constants</span></span>

<span data-ttu-id="f833b-124">在 Direct3D 9 中，指定著色器中已定義常數的存留期僅限於執行該著色器 (且不可覆寫) 。</span><span class="sxs-lookup"><span data-stu-id="f833b-124">In Direct3D 9 the lifetime of defined constants in a given shader is confined to the execution of that shader only (and is non-overridable).</span></span> <span data-ttu-id="f833b-125">在 Direct3D 9 中定義的常數在著色器以外沒有任何副作用。</span><span class="sxs-lookup"><span data-stu-id="f833b-125">Defined constants in Direct3D 9 have no side effects outside of the shader.</span></span>

<span data-ttu-id="f833b-126">以下是使用 Direct3D 9 的範例：</span><span class="sxs-lookup"><span data-stu-id="f833b-126">Here's an example using Direct3D 9:</span></span>


```
Given: 
    Create shader1 which references c4 and defines it with the def instruction

Scenario 1:
    Call Set***Shader shader1
    Call Set***ShaderConstant* to set c4
    Call Draw
    Result: The shader will see the def'd value in c4

    
Given: 
    Scenario 1 has just completed
    Create shader2 (which references c4 but does not use the def instruction
      to define it) 

Scenario 2: 
    Call Set***Shader shader2
    Call Draw
    Result: The shader will see the value last set in c4 by 
     Set***ShaderConstant* in scenario 1. This is because shader 2 
     didn't def c4.
```



<span data-ttu-id="f833b-127">在 Direct3D 9 中，呼叫 Get \* \* \* ShaderConstant \* 只會取得透過 set ShaderConstant 所設定的常數值 \* \* \* \* 。</span><span class="sxs-lookup"><span data-stu-id="f833b-127">In Direct3D 9, calling Get\*\*\*ShaderConstant\* will only retrieve constant values set via Set\*\*\*ShaderConstant\*.</span></span>

### <a name="direct3d-8-shader-constants"></a><span data-ttu-id="f833b-128">Direct3D 8 著色器常數</span><span class="sxs-lookup"><span data-stu-id="f833b-128">Direct3D 8 Shader Constants</span></span>

<span data-ttu-id="f833b-129">此行為在 Direct3D 8.x 中不同。</span><span class="sxs-lookup"><span data-stu-id="f833b-129">This behavior is different in Direct3D 8.x.</span></span>


```
Given:
    Create shader1 which references c4 and defines it with the def instruction

Scenario 1 (repeated with Direct3D 8):
    Call Set***Shader with shader1
    Call Set***ShaderConstant to set c4
    Call Draw
    Result: The shader will see the value in c4 from Set***ShaderConstant
```



<span data-ttu-id="f833b-130">在 Direct3D 8.x 中，Set \* \* \* ShaderConstant 會立即生效。</span><span class="sxs-lookup"><span data-stu-id="f833b-130">In Direct3D 8.x Set\*\*\*ShaderConstant takes effect immediately.</span></span> <span data-ttu-id="f833b-131">假設有下列情況：</span><span class="sxs-lookup"><span data-stu-id="f833b-131">Consider this scenario:</span></span>


```
Given:
    Create shader1 which references c4 and defines it with the def instruction
    
Scenario 3:
    Call Set***Shader with shader1
    Call Draw
    Result: The shader will see the def'd value in c4

Given:
    Scenario 3 has just completed
    Create shader2 (which references c4 but does not use the def instruction 
      to define it)     
    
Scenario 4 :    
    Call Set***Shader with shader2
    Call Draw
    Result: The shader will see the def'd value in c4 (set by def in shader 1)
```



<span data-ttu-id="f833b-132">不想要的結果是設定著色器的順序可能會影響個別著色器觀察到的行為。</span><span class="sxs-lookup"><span data-stu-id="f833b-132">The undesirable result is that the order in which the shaders are set could affect the observed behavior of individual shaders.</span></span>

## <a name="shader-driver-model-requirements"></a><span data-ttu-id="f833b-133">著色器驅動程式模型需求</span><span class="sxs-lookup"><span data-stu-id="f833b-133">Shader Driver Model Requirements</span></span>

<span data-ttu-id="f833b-134">Direct3D 9 介面受限於 DirectX 7 層級和更新版本的設備磁碟機介面 (DDI) 驅動程式。</span><span class="sxs-lookup"><span data-stu-id="f833b-134">Direct3D 9 interfaces are restricted to device driver interface (DDI) drivers that are DirectX 7-level and above.</span></span> <span data-ttu-id="f833b-135">若要檢查 DDI 層級，請執行 [DirectX 診斷工具](https://msdn.microsoft.com/library/Ee416792(v=VS.85).aspx) ，並檢查儲存的文字檔。</span><span class="sxs-lookup"><span data-stu-id="f833b-135">To check the DDI level, run the [DirectX Diagnostic Tool](https://msdn.microsoft.com/library/Ee416792(v=VS.85).aspx) and examine the saved text file.</span></span>

<span data-ttu-id="f833b-136">針對參考，Direct3D 8 介面只適用于 DirectX 6 層級和更新版本的 DDI 驅動程式。</span><span class="sxs-lookup"><span data-stu-id="f833b-136">For reference, Direct3D 8 interfaces work only on DDI drivers that are DirectX 6-level and above.</span></span>

## <a name="shader-binary-format"></a><span data-ttu-id="f833b-137">著色器二進位格式</span><span class="sxs-lookup"><span data-stu-id="f833b-137">Shader Binary Format</span></span>

<span data-ttu-id="f833b-138">著色器指令資料流程的位配置是在 D3d9types 中定義。</span><span class="sxs-lookup"><span data-stu-id="f833b-138">The bitwise layout of the shader instruction stream is defined in D3d9types.h.</span></span> <span data-ttu-id="f833b-139">如果您想要設計自己的著色器編譯器或建築工具，並且想要更多有關著色器權杖資料流程的詳細資訊，請參閱 Direct3D 9 驅動程式開發工具組 (DDK) 。</span><span class="sxs-lookup"><span data-stu-id="f833b-139">If you want to design your own shader compiler or construction tools and you want more information about the shader token stream, refer to the Direct3D 9 Driver Development Kit (DDK).</span></span>

## <a name="c-like-shader-language"></a><span data-ttu-id="f833b-140">類似 C 著色器語言</span><span class="sxs-lookup"><span data-stu-id="f833b-140">C-like Shader Language</span></span>

<span data-ttu-id="f833b-141">請參閱 [HLSL 參考](dx-graphics-hlsl-reference.md) ，以體驗類似 C 的著色器語言。</span><span class="sxs-lookup"><span data-stu-id="f833b-141">See [HLSL Reference](dx-graphics-hlsl-reference.md) to experience a C-like shader language.</span></span>

## <a name="related-topics"></a><span data-ttu-id="f833b-142">相關主題</span><span class="sxs-lookup"><span data-stu-id="f833b-142">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="f833b-143">HLSL 的參考</span><span class="sxs-lookup"><span data-stu-id="f833b-143">Reference for HLSL</span></span>](dx-graphics-hlsl-reference.md)
</dt> </dl>

 

 




