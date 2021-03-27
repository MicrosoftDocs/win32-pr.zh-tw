---
title: '常數布林值暫存器 (HLSL 與參考) '
description: 此暫存器是靜態流程式控制制指示中所使用的位集合 (例如，如果 bool 與 else-vs-endif-vs) 。
ms.assetid: bd02d03b-c228-481a-9c98-7442be4cdd07
ms.topic: article
ms.date: 05/31/2018
topic_type:
- kbArticle
api_name: ''
api_type: ''
api_location: ''
ms.openlocfilehash: 9b32841f060a29fce2918daca8f8fd008529bef1
ms.sourcegitcommit: 592c9bbd22ba69802dc353bcb5eb30699f9e9403
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/20/2020
ms.locfileid: "104971748"
---
# <a name="constant-boolean-register-hlsl-vs-reference"></a><span data-ttu-id="96039-103">常數布林值暫存器 (HLSL 與參考) </span><span class="sxs-lookup"><span data-stu-id="96039-103">Constant Boolean register (HLSL VS reference)</span></span>

<span data-ttu-id="96039-104">此暫存器是靜態流程式控制制指示中所使用的位集合 (例如，[如果 bool-vs](if-bool---vs.md)  -  [else-vs](else---vs.md)  -  [endif-vs](endif---vs.md)) 。</span><span class="sxs-lookup"><span data-stu-id="96039-104">This register is a collection of bits used in static flow control instructions (for example, [if bool - vs](if-bool---vs.md) - [else - vs](else---vs.md) - [endif - vs](endif---vs.md)).</span></span> <span data-ttu-id="96039-105">其中有16個，因此著色器可以有16個獨立的分支條件。</span><span class="sxs-lookup"><span data-stu-id="96039-105">There are 16 of them, therefore, a shader can have 16 independent branch conditions.</span></span> <span data-ttu-id="96039-106">您可以使用 [defb-vs](defb---vs.md) 或 [**SetVertexShaderConstantB**](/windows/desktop/api/d3d9helper/nf-d3d9helper-idirect3ddevice9-setvertexshaderconstantb)來設定它們。</span><span class="sxs-lookup"><span data-stu-id="96039-106">They can be set using [defb - vs](defb---vs.md) or [**SetVertexShaderConstantB**](/windows/desktop/api/d3d9helper/nf-d3d9helper-idirect3ddevice9-setvertexshaderconstantb).</span></span>

<span data-ttu-id="96039-107">在 Direct3D 8 和 Direct3D 9 之間變更著色器常數的行為。</span><span class="sxs-lookup"><span data-stu-id="96039-107">The behavior of shader constants has changed between Direct3D 8 and Direct3D 9.</span></span>

-   <span data-ttu-id="96039-108">針對 Direct3D 9，使用 defx 設定的常數會將值指派給著色器常數空間。</span><span class="sxs-lookup"><span data-stu-id="96039-108">For Direct3D 9, constants set with defx assign values to the shader constant space.</span></span> <span data-ttu-id="96039-109">使用 defx 宣告之常數的存留期只限于該著色器的執行。</span><span class="sxs-lookup"><span data-stu-id="96039-109">The lifetime of a constant declared with defx is confined to the execution of that shader only.</span></span> <span data-ttu-id="96039-110">相反地，使用 Api 設定的常數 SetXXXShaderConstantX 會初始化全域空間中的常數。</span><span class="sxs-lookup"><span data-stu-id="96039-110">Conversely, constants set using the APIs SetXXXShaderConstantX initialize constants in global space.</span></span> <span data-ttu-id="96039-111">在呼叫 SetxxxShaderConstants 之前，不會將全域空間中的常數複製到 (著色器) 可見的本機空間。</span><span class="sxs-lookup"><span data-stu-id="96039-111">Constants in global space are not copied to local space (visible to the shader) until SetxxxShaderConstants is called.</span></span>
-   <span data-ttu-id="96039-112">針對 Direct3D 8，使用 defx 或 Api 設定的常數都會將值指派給著色器常數空間。</span><span class="sxs-lookup"><span data-stu-id="96039-112">For Direct3D 8, constants set with defx or the APIs both assign values to the shader constant space.</span></span> <span data-ttu-id="96039-113">每次執行著色器時，目前的著色器都會使用常數，而不考慮用來設定它們的技巧。</span><span class="sxs-lookup"><span data-stu-id="96039-113">Each time the shader is executed, the constants are used by the current shader regardless of the technique used to set them.</span></span>

## <a name="related-topics"></a><span data-ttu-id="96039-114">相關主題</span><span class="sxs-lookup"><span data-stu-id="96039-114">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="96039-115">頂點著色器暫存器</span><span class="sxs-lookup"><span data-stu-id="96039-115">Vertex Shader Registers</span></span>](dx9-graphics-reference-asm-vs-registers.md)
</dt> </dl>

 

 