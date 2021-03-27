---
title: '常數整數 Register (HLSL 與參考) '
description: 常數整數暫存器只會用於迴圈-vs 和 rep-vs。
ms.assetid: da9916d4-655b-4c98-99a4-1abfa66459b5
ms.topic: article
ms.date: 05/31/2018
topic_type:
- kbArticle
api_name: ''
api_type: ''
api_location: ''
ms.openlocfilehash: 4cf2612eccb891ce0cffd04955e4997173e84007
ms.sourcegitcommit: 592c9bbd22ba69802dc353bcb5eb30699f9e9403
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/20/2020
ms.locfileid: "104971760"
---
# <a name="constant-integer-register-hlsl-vs-reference"></a><span data-ttu-id="a79a0-103">常數整數 Register (HLSL 與參考) </span><span class="sxs-lookup"><span data-stu-id="a79a0-103">Constant Integer Register (HLSL VS reference)</span></span>

<span data-ttu-id="a79a0-104">常數整數暫存器只會用於 [迴圈-vs](loop---vs.md) 和 [rep-vs](rep---vs.md)。</span><span class="sxs-lookup"><span data-stu-id="a79a0-104">Constant integer registers are used only by [loop - vs](loop---vs.md) and [rep - vs](rep---vs.md).</span></span>

<span data-ttu-id="a79a0-105">您可以使用 [defi-vs](defi---vs.md) 或 [**SetVertexShaderConstantI**](/windows/desktop/api/d3d9helper/nf-d3d9helper-idirect3ddevice9-setvertexshaderconstanti)來設定它們。</span><span class="sxs-lookup"><span data-stu-id="a79a0-105">They can be set using [defi - vs](defi---vs.md) or [**SetVertexShaderConstantI**](/windows/desktop/api/d3d9helper/nf-d3d9helper-idirect3ddevice9-setvertexshaderconstanti).</span></span>

<span data-ttu-id="a79a0-106">當做迴圈的引數使用時 [（vs](loop---vs.md) 指令）：</span><span class="sxs-lookup"><span data-stu-id="a79a0-106">When used as an argument to the [loop - vs](loop---vs.md) instruction:</span></span>

-   <span data-ttu-id="a79a0-107">. x 是反復專案計數。</span><span class="sxs-lookup"><span data-stu-id="a79a0-107">.x is the iteration count.</span></span> <span data-ttu-id="a79a0-108"> ([rep-vs](rep---vs.md) 只會) 使用此元件。</span><span class="sxs-lookup"><span data-stu-id="a79a0-108">([rep - vs](rep---vs.md) uses only this component).</span></span>
-   <span data-ttu-id="a79a0-109">. y 是迴圈計數器的起始值。</span><span class="sxs-lookup"><span data-stu-id="a79a0-109">.y is the initial value for the loop counter.</span></span>
-   <span data-ttu-id="a79a0-110">. z 是迴圈計數器的遞增步驟。</span><span class="sxs-lookup"><span data-stu-id="a79a0-110">.z is the increment step for the loop counter.</span></span>

<span data-ttu-id="a79a0-111">在 Direct3D 8 和 Direct3D 9 之間變更著色器常數的行為。</span><span class="sxs-lookup"><span data-stu-id="a79a0-111">The behavior of shader constants has changed between Direct3D 8 and Direct3D 9.</span></span>

-   <span data-ttu-id="a79a0-112">針對 Direct3D 9，使用 defx 設定的常數會將值指派給著色器常數空間。</span><span class="sxs-lookup"><span data-stu-id="a79a0-112">For Direct3D 9, constants set with defx assign values to the shader constant space.</span></span> <span data-ttu-id="a79a0-113">使用 defx 宣告之常數的存留期只限于該著色器的執行。</span><span class="sxs-lookup"><span data-stu-id="a79a0-113">The lifetime of a constant declared with defx is confined to the execution of that shader only.</span></span> <span data-ttu-id="a79a0-114">相反地，使用 Api 設定的常數 SetXXXShaderConstantX 會初始化全域空間中的常數。</span><span class="sxs-lookup"><span data-stu-id="a79a0-114">Conversely, constants set using the APIs SetXXXShaderConstantX initialize constants in global space.</span></span> <span data-ttu-id="a79a0-115">在呼叫 SetxxxShaderConstants 之前，不會將全域空間中的常數複製到 (著色器) 可見的本機空間。</span><span class="sxs-lookup"><span data-stu-id="a79a0-115">Constants in global space are not copied to local space (visible to the shader) until SetxxxShaderConstants is called.</span></span>
-   <span data-ttu-id="a79a0-116">針對 Direct3D 8，使用 defx 或 Api 設定的常數都會將值指派給著色器常數空間。</span><span class="sxs-lookup"><span data-stu-id="a79a0-116">For Direct3D 8, constants set with defx or the APIs both assign values to the shader constant space.</span></span> <span data-ttu-id="a79a0-117">每次執行著色器時，目前的著色器都會使用常數，而不考慮用來設定它們的技巧。</span><span class="sxs-lookup"><span data-stu-id="a79a0-117">Each time the shader is executed, the constants are used by the current shader regardless of the technique used to set them.</span></span>

## <a name="related-topics"></a><span data-ttu-id="a79a0-118">相關主題</span><span class="sxs-lookup"><span data-stu-id="a79a0-118">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="a79a0-119">頂點著色器暫存器</span><span class="sxs-lookup"><span data-stu-id="a79a0-119">Vertex Shader Registers</span></span>](dx9-graphics-reference-asm-vs-registers.md)
</dt> </dl>

 

 