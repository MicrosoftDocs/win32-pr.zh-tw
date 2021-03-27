---
title: '常數整數 register (HLSL PS 參考) '
description: 常數整數暫存器只能由迴圈-ps 和 rep-ps 使用。
ms.assetid: 85720ec0-b6aa-4a24-910c-3ad0468300dc
ms.topic: article
ms.date: 05/31/2018
topic_type:
- kbArticle
api_name: ''
api_type: ''
api_location: ''
ms.openlocfilehash: 9b03a27a95f84ae30a70147caaf5662e1949cf18
ms.sourcegitcommit: 592c9bbd22ba69802dc353bcb5eb30699f9e9403
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/20/2020
ms.locfileid: "104971749"
---
# <a name="constant-integer-register-hlsl-ps-reference"></a><span data-ttu-id="2f2f8-103">常數整數 register (HLSL PS 參考) </span><span class="sxs-lookup"><span data-stu-id="2f2f8-103">Constant integer register (HLSL PS reference)</span></span>

<span data-ttu-id="2f2f8-104">常數整數暫存器只能由 [迴圈-ps](loop---ps.md) 和 [rep-ps](rep---ps.md)使用。</span><span class="sxs-lookup"><span data-stu-id="2f2f8-104">Constant integer registers are used only by [loop - ps](loop---ps.md) and [rep - ps](rep---ps.md).</span></span>

<span data-ttu-id="2f2f8-105">您可以使用 [defi-ps](defi---ps.md) 或 [**SetPixelShaderConstantI**](/windows/desktop/api/d3d9helper/nf-d3d9helper-idirect3ddevice9-setpixelshaderconstanti)來設定它們。</span><span class="sxs-lookup"><span data-stu-id="2f2f8-105">They can be set using [defi - ps](defi---ps.md) or [**SetPixelShaderConstantI**](/windows/desktop/api/d3d9helper/nf-d3d9helper-idirect3ddevice9-setpixelshaderconstanti).</span></span>

<span data-ttu-id="2f2f8-106">當做 [迴圈 ps](loop---ps.md) 指令的引數使用時：</span><span class="sxs-lookup"><span data-stu-id="2f2f8-106">When used as an argument to the [loop - ps](loop---ps.md) instruction:</span></span>

-   <span data-ttu-id="2f2f8-107">. x 是反復專案計數。</span><span class="sxs-lookup"><span data-stu-id="2f2f8-107">.x is the iteration count.</span></span> <span data-ttu-id="2f2f8-108"> ([代表-ps](rep---ps.md) 只會使用此元件) 。</span><span class="sxs-lookup"><span data-stu-id="2f2f8-108">([rep - ps](rep---ps.md) uses only this component).</span></span>
-   <span data-ttu-id="2f2f8-109">. y 是迴圈計數器的起始值。</span><span class="sxs-lookup"><span data-stu-id="2f2f8-109">.y is the initial value for the loop counter.</span></span>
-   <span data-ttu-id="2f2f8-110">. z 是迴圈計數器的遞增步驟。</span><span class="sxs-lookup"><span data-stu-id="2f2f8-110">.z is the increment step for the loop counter.</span></span>



| <span data-ttu-id="2f2f8-111">圖元著色器版本</span><span class="sxs-lookup"><span data-stu-id="2f2f8-111">Pixel shader versions</span></span>     | <span data-ttu-id="2f2f8-112">1\_1</span><span class="sxs-lookup"><span data-stu-id="2f2f8-112">1\_1</span></span> | <span data-ttu-id="2f2f8-113">1\_2</span><span class="sxs-lookup"><span data-stu-id="2f2f8-113">1\_2</span></span> | <span data-ttu-id="2f2f8-114">1 \_ 3</span><span class="sxs-lookup"><span data-stu-id="2f2f8-114">1\_3</span></span> | <span data-ttu-id="2f2f8-115">1\_4</span><span class="sxs-lookup"><span data-stu-id="2f2f8-115">1\_4</span></span> | <span data-ttu-id="2f2f8-116">2 \_ 0</span><span class="sxs-lookup"><span data-stu-id="2f2f8-116">2\_0</span></span> | <span data-ttu-id="2f2f8-117">2個 \_ sw</span><span class="sxs-lookup"><span data-stu-id="2f2f8-117">2\_sw</span></span> | <span data-ttu-id="2f2f8-118">2 \_ x</span><span class="sxs-lookup"><span data-stu-id="2f2f8-118">2\_x</span></span> | <span data-ttu-id="2f2f8-119">3 \_ 0</span><span class="sxs-lookup"><span data-stu-id="2f2f8-119">3\_0</span></span> | <span data-ttu-id="2f2f8-120">3個 \_ sw</span><span class="sxs-lookup"><span data-stu-id="2f2f8-120">3\_sw</span></span> |
|---------------------------|------|------|------|------|------|-------|------|------|-------|
| <span data-ttu-id="2f2f8-121">常數整數暫存器</span><span class="sxs-lookup"><span data-stu-id="2f2f8-121">Constant Integer Register</span></span> |      |      |      |      |      |       | <span data-ttu-id="2f2f8-122">x</span><span class="sxs-lookup"><span data-stu-id="2f2f8-122">x</span></span>    | <span data-ttu-id="2f2f8-123">x</span><span class="sxs-lookup"><span data-stu-id="2f2f8-123">x</span></span>    | <span data-ttu-id="2f2f8-124">x</span><span class="sxs-lookup"><span data-stu-id="2f2f8-124">x</span></span>     |



 

<span data-ttu-id="2f2f8-125">在 Direct3D 8 和 Direct3D 9 之間變更著色器常數的行為。</span><span class="sxs-lookup"><span data-stu-id="2f2f8-125">The behavior of shader constants has changed between Direct3D 8 and Direct3D 9.</span></span>

-   <span data-ttu-id="2f2f8-126">針對 Direct3D 9，使用 defx 設定的常數會將值指派給著色器常數空間。</span><span class="sxs-lookup"><span data-stu-id="2f2f8-126">For Direct3D 9, constants set with defx assign values to the shader constant space.</span></span> <span data-ttu-id="2f2f8-127">使用 defx 宣告之常數的存留期只限于該著色器的執行。</span><span class="sxs-lookup"><span data-stu-id="2f2f8-127">The lifetime of a constant declared with defx is confined to the execution of that shader only.</span></span> <span data-ttu-id="2f2f8-128">相反地，使用 Api 設定的常數 SetXXXShaderConstantX 會初始化全域空間中的常數。</span><span class="sxs-lookup"><span data-stu-id="2f2f8-128">Conversely, constants set using the APIs SetXXXShaderConstantX initialize constants in global space.</span></span> <span data-ttu-id="2f2f8-129">在呼叫 SetxxxShaderConstants 之前，不會將全域空間中的常數複製到 (著色器) 可見的本機空間。</span><span class="sxs-lookup"><span data-stu-id="2f2f8-129">Constants in global space are not copied to local space (visible to the shader) until SetxxxShaderConstants is called.</span></span>
-   <span data-ttu-id="2f2f8-130">針對 Direct3D 8，使用 defx 或 Api 設定的常數都會將值指派給著色器常數空間。</span><span class="sxs-lookup"><span data-stu-id="2f2f8-130">For Direct3D 8, constants set with defx or the APIs both assign values to the shader constant space.</span></span> <span data-ttu-id="2f2f8-131">每次執行著色器時，目前的著色器都會使用常數，而不考慮用來設定它們的技巧。</span><span class="sxs-lookup"><span data-stu-id="2f2f8-131">Each time the shader is executed, the constants are used by the current shader regardless of the technique used to set them.</span></span>

## <a name="related-topics"></a><span data-ttu-id="2f2f8-132">相關主題</span><span class="sxs-lookup"><span data-stu-id="2f2f8-132">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="2f2f8-133">寄存 器</span><span class="sxs-lookup"><span data-stu-id="2f2f8-133">Registers</span></span>](dx9-graphics-reference-asm-ps-registers.md)
</dt> </dl>

 

 