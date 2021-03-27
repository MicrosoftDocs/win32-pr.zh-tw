---
title: '常數 Boolean register (HLSL PS 參考) '
description: 此暫存器是靜態流程式控制制 (指令中使用的位集合，例如，如果 bool-ps---------ps) 。
ms.assetid: fb4abe19-d0cf-48ac-866e-4be60cc86bd6
ms.topic: article
ms.date: 05/31/2018
topic_type:
- kbArticle
api_name: ''
api_type: ''
api_location: ''
ms.openlocfilehash: 4868be7c22ce5a6a1881ad7db8acf0af65330c04
ms.sourcegitcommit: 592c9bbd22ba69802dc353bcb5eb30699f9e9403
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/20/2020
ms.locfileid: "103682820"
---
# <a name="constant-boolean-register-hlsl-ps-reference"></a><span data-ttu-id="fac29-103">常數 Boolean register (HLSL PS 參考) </span><span class="sxs-lookup"><span data-stu-id="fac29-103">Constant Boolean register (HLSL PS reference)</span></span>

<span data-ttu-id="fac29-104">此暫存器是靜態流程式控制制指示中使用的位集合 (例如，[如果 bool-ps](if-bool---ps.md)（ps）-ps  -  [](else---ps.md)  -  [](endif---ps.md)) 。</span><span class="sxs-lookup"><span data-stu-id="fac29-104">This register is a collection of bits used in static flow control instructions (for example, [if bool - ps](if-bool---ps.md) - [else - ps](else---ps.md) - [endif - ps](endif---ps.md)).</span></span> <span data-ttu-id="fac29-105">其中有16個，因此著色器可以有16個獨立的分支條件。</span><span class="sxs-lookup"><span data-stu-id="fac29-105">There are 16 of them, therefore, a shader can have 16 independent branch conditions.</span></span> <span data-ttu-id="fac29-106">您可以使用 [defb-ps](defb---ps.md) 或 [**SetPixelShaderConstantB**](/windows/desktop/api/d3d9helper/nf-d3d9helper-idirect3ddevice9-setpixelshaderconstantb)來設定它們。</span><span class="sxs-lookup"><span data-stu-id="fac29-106">They can be set using [defb - ps](defb---ps.md) or [**SetPixelShaderConstantB**](/windows/desktop/api/d3d9helper/nf-d3d9helper-idirect3ddevice9-setpixelshaderconstantb).</span></span>

<span data-ttu-id="fac29-107">在 Direct3D 8 和 Direct3D 9 之間變更著色器常數的行為。</span><span class="sxs-lookup"><span data-stu-id="fac29-107">The behavior of shader constants has changed between Direct3D 8 and Direct3D 9.</span></span>

-   <span data-ttu-id="fac29-108">針對 Direct3D 9，使用 defx 設定的常數會將值指派給著色器常數空間。</span><span class="sxs-lookup"><span data-stu-id="fac29-108">For Direct3D 9, constants set with defx assign values to the shader constant space.</span></span> <span data-ttu-id="fac29-109">使用 defx 宣告之常數的存留期只限于該著色器的執行。</span><span class="sxs-lookup"><span data-stu-id="fac29-109">The lifetime of a constant declared with defx is confined to the execution of that shader only.</span></span> <span data-ttu-id="fac29-110">相反地，使用 Api 設定的常數 SetXXXShaderConstantX 會初始化全域空間中的常數。</span><span class="sxs-lookup"><span data-stu-id="fac29-110">Conversely, constants set using the APIs SetXXXShaderConstantX initialize constants in global space.</span></span> <span data-ttu-id="fac29-111">在呼叫 SetxxxShaderConstants 之前，不會將全域空間中的常數複製到 (著色器) 可見的本機空間。</span><span class="sxs-lookup"><span data-stu-id="fac29-111">Constants in global space are not copied to local space (visible to the shader) until SetxxxShaderConstants is called.</span></span>
-   <span data-ttu-id="fac29-112">針對 Direct3D 8，使用 defx 或 Api 設定的常數都會將值指派給著色器常數空間。</span><span class="sxs-lookup"><span data-stu-id="fac29-112">For Direct3D 8, constants set with defx or the APIs both assign values to the shader constant space.</span></span> <span data-ttu-id="fac29-113">每次執行著色器時，目前的著色器都會使用常數，而不考慮用來設定它們的技巧。</span><span class="sxs-lookup"><span data-stu-id="fac29-113">Each time the shader is executed, the constants are used by the current shader regardless of the technique used to set them.</span></span>



| <span data-ttu-id="fac29-114">圖元著色器版本</span><span class="sxs-lookup"><span data-stu-id="fac29-114">Pixel shader versions</span></span>     | <span data-ttu-id="fac29-115">1\_1</span><span class="sxs-lookup"><span data-stu-id="fac29-115">1\_1</span></span> | <span data-ttu-id="fac29-116">1\_2</span><span class="sxs-lookup"><span data-stu-id="fac29-116">1\_2</span></span> | <span data-ttu-id="fac29-117">1 \_ 3</span><span class="sxs-lookup"><span data-stu-id="fac29-117">1\_3</span></span> | <span data-ttu-id="fac29-118">1\_4</span><span class="sxs-lookup"><span data-stu-id="fac29-118">1\_4</span></span> | <span data-ttu-id="fac29-119">2 \_ 0</span><span class="sxs-lookup"><span data-stu-id="fac29-119">2\_0</span></span> | <span data-ttu-id="fac29-120">2個 \_ sw</span><span class="sxs-lookup"><span data-stu-id="fac29-120">2\_sw</span></span> | <span data-ttu-id="fac29-121">2 \_ x</span><span class="sxs-lookup"><span data-stu-id="fac29-121">2\_x</span></span> | <span data-ttu-id="fac29-122">3 \_ 0</span><span class="sxs-lookup"><span data-stu-id="fac29-122">3\_0</span></span> | <span data-ttu-id="fac29-123">3個 \_ sw</span><span class="sxs-lookup"><span data-stu-id="fac29-123">3\_sw</span></span> |
|---------------------------|------|------|------|------|------|-------|------|------|-------|
| <span data-ttu-id="fac29-124">常數布林值暫存器</span><span class="sxs-lookup"><span data-stu-id="fac29-124">Constant Boolean register</span></span> |      |      |      |      |      |       | <span data-ttu-id="fac29-125">x</span><span class="sxs-lookup"><span data-stu-id="fac29-125">x</span></span>    | <span data-ttu-id="fac29-126">x</span><span class="sxs-lookup"><span data-stu-id="fac29-126">x</span></span>    | <span data-ttu-id="fac29-127">x</span><span class="sxs-lookup"><span data-stu-id="fac29-127">x</span></span>     |



 

## <a name="related-topics"></a><span data-ttu-id="fac29-128">相關主題</span><span class="sxs-lookup"><span data-stu-id="fac29-128">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="fac29-129">寄存 器</span><span class="sxs-lookup"><span data-stu-id="fac29-129">Registers</span></span>](dx9-graphics-reference-asm-ps-registers.md)
</dt> </dl>

 

 