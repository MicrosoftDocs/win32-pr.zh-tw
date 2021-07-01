---
title: 著色器模型與著色器設定檔
description: 著色器模型與著色器設定檔
ms.assetid: 6224f05e-20b1-42ea-96fb-63dd0edb720e
ms.topic: article
ms.date: 05/31/2018
topic_type:
- kbArticle
api_name: ''
api_type: ''
api_location: ''
ms.openlocfilehash: 963e68d5875c3ee512e7e0d6ee7c243db72f4400
ms.sourcegitcommit: b32433cc0394159c7263809ae67615ab5792d40d
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 06/30/2021
ms.locfileid: "113119613"
---
# <a name="shader-models-vs-shader-profiles"></a><span data-ttu-id="46dbb-103">著色器模型與著色器設定檔</span><span class="sxs-lookup"><span data-stu-id="46dbb-103">Shader Models vs Shader Profiles</span></span>

<span data-ttu-id="46dbb-104">適用于 DirectX 的高階網底語言會實行一連串的著色器模型。</span><span class="sxs-lookup"><span data-stu-id="46dbb-104">The High Level Shading Language for DirectX implements a series of shader models.</span></span> <span data-ttu-id="46dbb-105">您可以使用 HLSL，為 Direct3D 管線建立類似 C 的可程式化著色器。</span><span class="sxs-lookup"><span data-stu-id="46dbb-105">Using HLSL, you can create C-like programmable shaders for the Direct3D pipeline.</span></span> <span data-ttu-id="46dbb-106">每個著色器模型都是以模型的功能為基礎，並以較少的限制來執行更多的功能。</span><span class="sxs-lookup"><span data-stu-id="46dbb-106">Each shader model builds on the capabilities of the model before it, implementing more functionality with fewer restrictions.</span></span>

<span data-ttu-id="46dbb-107">著色器模型1以 DirectX 8 開始，並包含元件層級和類似 C 的指令。</span><span class="sxs-lookup"><span data-stu-id="46dbb-107">Shader model 1 started with DirectX 8 and included assembly level and C-like instructions.</span></span> <span data-ttu-id="46dbb-108">此模型有許多由早期可程式化著色器硬體所造成的限制。</span><span class="sxs-lookup"><span data-stu-id="46dbb-108">This model has many limitations caused by early programmable shader hardware.</span></span> <span data-ttu-id="46dbb-109">著色器模型2和3會大幅擴充指令數目，而常數著色器可以使用。</span><span class="sxs-lookup"><span data-stu-id="46dbb-109">Shader model 2 and 3 greatly expanded on the number of instructions, and constants shaders could use.</span></span> <span data-ttu-id="46dbb-110">它們比著色器模型1強大許多，但仍會提供第一個著色器模型的一些現有限制。</span><span class="sxs-lookup"><span data-stu-id="46dbb-110">They are much more powerful than shader model 1, but still carry some of the existing limitations of the first shader model.</span></span>

<span data-ttu-id="46dbb-111">從 Windows Vista 開始，著色器模型4是完整的重新設計。</span><span class="sxs-lookup"><span data-stu-id="46dbb-111">Starting with Windows Vista, shader model 4 is a complete redesign.</span></span> <span data-ttu-id="46dbb-112">它可讓您在電腦) 的硬體限制內 (無限制的指令和常數、具有樣板化的物件，讓紋理取樣更簡潔且更有效率，而且具有任何著色器模型的最少限制。</span><span class="sxs-lookup"><span data-stu-id="46dbb-112">It allows unlimited instructions and constants (within hardware constraints of your machine), has templated objects to make texture sampling cleaner and more efficient, and has the fewest restrictions of any shader model.</span></span> <span data-ttu-id="46dbb-113">但是，它只需要 Windows Driver Model，才能在 Windows Vista (或更新版本) 作業系統上使用。</span><span class="sxs-lookup"><span data-stu-id="46dbb-113">It does however require the Windows Driver Model which is only available on the Windows Vista (or later) operating system.</span></span>

## <a name="shader-profiles"></a><span data-ttu-id="46dbb-114">著色器設定檔</span><span class="sxs-lookup"><span data-stu-id="46dbb-114">Shader Profiles</span></span>

<span data-ttu-id="46dbb-115">著色器設定檔是編譯著色器的目標;下表列出每個著色器模型所支援的著色器設定檔。</span><span class="sxs-lookup"><span data-stu-id="46dbb-115">A shader profile is the target for compiling a shader; this table lists the shader profiles that are supported by each shader model.</span></span>



| <span data-ttu-id="46dbb-116">著色器模型</span><span class="sxs-lookup"><span data-stu-id="46dbb-116">Shader model</span></span>                                                   | <span data-ttu-id="46dbb-117">著色器設定檔</span><span class="sxs-lookup"><span data-stu-id="46dbb-117">Shader profiles</span></span>                                                                                                                                                                                                                                                                                                      |
|----------------------------------------------------|-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [<span data-ttu-id="46dbb-118">著色器模型1</span><span class="sxs-lookup"><span data-stu-id="46dbb-118">Shader Model 1</span></span>](dx-graphics-hlsl-sm1.md)         | <span data-ttu-id="46dbb-119">vs \_ 1 \_ 1</span><span class="sxs-lookup"><span data-stu-id="46dbb-119">vs\_1\_1</span></span>                                                                                                                                                                                                                                                                                              |
| [<span data-ttu-id="46dbb-120">著色器模型2</span><span class="sxs-lookup"><span data-stu-id="46dbb-120">Shader Model 2</span></span>](dx-graphics-hlsl-sm2.md)         | <span data-ttu-id="46dbb-121">ps \_ 2 \_ 0、ps \_ 2 \_ x、vs \_ 2 \_ 0、vs \_ 2 \_ x、ps \_ 4 \_ 0 \_ 層級 \_ 9 \_ 0、ps \_ 4 \_ 0 \_ 層級 \_ 9 \_ 1、ps \_ 4 \_ 0 \_ 層級 \_ 9 \_ 3、vs \_ 4 0 層級 9 \_ \_ \_ \_ 0、vs \_ 4 \_ 0 層級 \_ \_ 9 \_ 1、vs \_ 4 0 層級 9 \_ \_ \_ \_ 3、lib \_ 4 \_ 0 \_ 層級 \_ 9 \_ 1、lib \_ 4 \_ 0 層級 \_ \_ 9 \_ 3</span><span class="sxs-lookup"><span data-stu-id="46dbb-121">ps\_2\_0, ps\_2\_x, vs\_2\_0, vs\_2\_x, ps\_4\_0\_level\_9\_0, ps\_4\_0\_level\_9\_1, ps\_4\_0\_level\_9\_3, vs\_4\_0\_level\_9\_0, vs\_4\_0\_level\_9\_1, vs\_4\_0\_level\_9\_3, lib\_4\_0\_level\_9\_1, lib\_4\_0\_level\_9\_3</span></span>                                                                      |
| [<span data-ttu-id="46dbb-122">著色器模型3</span><span class="sxs-lookup"><span data-stu-id="46dbb-122">Shader Model 3</span></span>](dx-graphics-hlsl-sm3.md)         | <span data-ttu-id="46dbb-123">ps \_ 3 \_ 0、vs \_ 3 \_ 0</span><span class="sxs-lookup"><span data-stu-id="46dbb-123">ps\_3\_0, vs\_3\_0</span></span>                                                                                                                                                                                                                                                                                    |
| [<span data-ttu-id="46dbb-124">著色器模型4</span><span class="sxs-lookup"><span data-stu-id="46dbb-124">Shader Model 4</span></span>](dx-graphics-hlsl-sm4.md)         | <span data-ttu-id="46dbb-125">cs \_ 4 \_ 0、gs \_ 4 \_ 0、ps \_ 4 \_ 0、vs \_ 4 \_ 0、cs \_ 4 \_ 1、gs \_ 4 \_ 1、ps \_ 4 \_ 1、vs \_ 4 \_ 1、lib \_ 4 \_ 0、lib \_ 4 \_ 1</span><span class="sxs-lookup"><span data-stu-id="46dbb-125">cs\_4\_0, gs\_4\_0, ps\_4\_0, vs\_4\_0, cs\_4\_1, gs\_4\_1, ps\_4\_1, vs\_4\_1, lib\_4\_0, lib\_4\_1</span></span>                                                                                                                                                                                                  |
| [<span data-ttu-id="46dbb-126">著色器模型5</span><span class="sxs-lookup"><span data-stu-id="46dbb-126">Shader Model 5</span></span>](d3d11-graphics-reference-sm5.md) | <span data-ttu-id="46dbb-127">cs \_ 5 \_ 0、ds \_ 5 \_ 0、gs \_ 5 \_ 0、hs \_ 5 \_ 0、ps \_ 5 \_ 0、vs \_ 5 \_ 0、lib \_ 5 \_ 0 (雖然 gs \_ 4 \_ 0、gs \_ 4 \_ 1、ps \_ 4 \_ 0、ps \_ 4 \_ 1、vs \_ 4 \_ 0 和 vs \_ 4 \_ 1 是在著色器模型4.0 中引進，但著色器模型5也會將這些著色器設定檔的支援新增至結構 ) 化</span><span class="sxs-lookup"><span data-stu-id="46dbb-127">cs\_5\_0, ds\_5\_0, gs\_5\_0, hs\_5\_0, ps\_5\_0, vs\_5\_0, lib\_5\_0 (Although gs\_4\_0, gs\_4\_1, ps\_4\_0, ps\_4\_1, vs\_4\_0, and vs\_4\_1 were introduced in shader model 4.0, shader model 5 adds support to these shader profiles for structured buffers and byte address buffers.)</span></span><br/> |
| [<span data-ttu-id="46dbb-128">著色器模型6</span><span class="sxs-lookup"><span data-stu-id="46dbb-128">Shader Model 6</span></span>](shader-model-6-0.md)             | <span data-ttu-id="46dbb-129">cs \_ 6 \_ 0、ds \_ 6 \_ 0、gs \_ 6 \_ 0、hs \_ 6 \_ 0、ps \_ 6 \_ 0、vs \_ 6 \_ 0、lib \_ 6 \_ 0</span><span class="sxs-lookup"><span data-stu-id="46dbb-129">cs\_6\_0, ds\_6\_0, gs\_6\_0, hs\_6\_0, ps\_6\_0, vs\_6\_0, lib\_6\_0</span></span>                                                                                                                                                                                                                                 |

<span data-ttu-id="46dbb-130">Direct3D 9 與 Direct3D 10 之間的差異：</span><span class="sxs-lookup"><span data-stu-id="46dbb-130">Differences between Direct3D 9 and Direct3D 10:</span></span>

- <span data-ttu-id="46dbb-131">Direct3D 9 引進了著色器模型1、2和3。</span><span class="sxs-lookup"><span data-stu-id="46dbb-131">Direct3D 9 introduced shader models 1, 2, and 3.</span></span>
- <span data-ttu-id="46dbb-132">Direct3D 10 引進了著色器模型4。</span><span class="sxs-lookup"><span data-stu-id="46dbb-132">Direct3D 10 introduced shader model 4.</span></span>
- <span data-ttu-id="46dbb-133">Direct3D 10.1 引進了著色器模型4.1。</span><span class="sxs-lookup"><span data-stu-id="46dbb-133">Direct3D 10.1 introduced shader model 4.1.</span></span>



 

## <a name="effect-profiles"></a><span data-ttu-id="46dbb-134">效果設定檔</span><span class="sxs-lookup"><span data-stu-id="46dbb-134">Effect Profiles</span></span>

<span data-ttu-id="46dbb-135">效果設定檔是用來編譯效果/著色器的目標;下表列出每個 Direct3D 版本所支援的效果設定檔。</span><span class="sxs-lookup"><span data-stu-id="46dbb-135">An effect profile is the target for compiling an effect/shader; this table lists the effect profiles that are supported by each version of Direct3D.</span></span>

<span data-ttu-id="46dbb-136">Direct3D 9 與 Direct3D 10 之間的差異：</span><span class="sxs-lookup"><span data-stu-id="46dbb-136">Differences between Direct3D 9 and Direct3D 10:</span></span>

- <span data-ttu-id="46dbb-137">Direct3D 9 引進了效果-架構設定檔 fx \_ 1 \_ 0 和 fx \_ 2 \_ 0。</span><span class="sxs-lookup"><span data-stu-id="46dbb-137">Direct3D 9 introduced effect-framework profiles fx\_1\_0 and fx\_2\_0.</span></span>
- <span data-ttu-id="46dbb-138">Direct3D 10 引進了效果-架構設定檔 fx \_ 4 \_ 0。</span><span class="sxs-lookup"><span data-stu-id="46dbb-138">Direct3D 10 introduced effect-framework profile fx\_4\_0.</span></span>
- <span data-ttu-id="46dbb-139">Direct3D 10.1 引進了效果-架構設定檔 fx \_ 4 \_ 1。</span><span class="sxs-lookup"><span data-stu-id="46dbb-139">Direct3D 10.1 introduced effect-framework profile fx\_4\_1.</span></span>
- <span data-ttu-id="46dbb-140">Direct3D 11 引進效果-framework 設定檔 fx \_ 5 \_ 0。</span><span class="sxs-lookup"><span data-stu-id="46dbb-140">Direct3D 11 introduced effect-framework profile fx\_5\_0.</span></span>

> [!Note]  
> <span data-ttu-id="46dbb-141">這些舊版效果設定檔已淘汰。</span><span class="sxs-lookup"><span data-stu-id="46dbb-141">These legacy effects profiles are deprecated.</span></span>

 

## <a name="related-topics"></a><span data-ttu-id="46dbb-142">相關主題</span><span class="sxs-lookup"><span data-stu-id="46dbb-142">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="46dbb-143">HLSL 的參考</span><span class="sxs-lookup"><span data-stu-id="46dbb-143">Reference for HLSL</span></span>](dx-graphics-hlsl-reference.md)
</dt> </dl>

 

 





