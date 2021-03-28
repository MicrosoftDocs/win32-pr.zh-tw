---
title: '常數 float register (HLSL PS 參考) '
description: 4D 浮點數常數的圖元著色器輸入暫存器。
ms.assetid: e4f46a48-c81e-4105-901b-332b92fa6195
ms.topic: article
ms.date: 05/31/2018
topic_type:
- kbArticle
api_name: ''
api_type: ''
api_location: ''
ms.openlocfilehash: 05bb382b745d172ea4b81f9920154e7c79a58c2d
ms.sourcegitcommit: 592c9bbd22ba69802dc353bcb5eb30699f9e9403
ms.translationtype: HT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/20/2020
ms.locfileid: "104376188"
---
# <a name="constant-float-register-hlsl-ps-reference"></a><span data-ttu-id="d6779-103">常數 float register (HLSL PS 參考) </span><span class="sxs-lookup"><span data-stu-id="d6779-103">Constant float register (HLSL PS reference)</span></span>

<span data-ttu-id="d6779-104">4D 浮點數常數的圖元著色器輸入暫存器。</span><span class="sxs-lookup"><span data-stu-id="d6779-104">Pixel shader input register for a 4D floating-point constant.</span></span>

<span data-ttu-id="d6779-105">您可以使用 [def （ps）](def---ps.md) 或 [**SetPixelShaderConstantF**](/windows/desktop/api/d3d9helper/nf-d3d9helper-idirect3ddevice9-setpixelshaderconstantf)來設定它們。</span><span class="sxs-lookup"><span data-stu-id="d6779-105">They can be set using [def - ps](def---ps.md) or [**SetPixelShaderConstantF**](/windows/desktop/api/d3d9helper/nf-d3d9helper-idirect3ddevice9-setpixelshaderconstantf).</span></span>

<span data-ttu-id="d6779-106">在 Direct3D 8 和 Direct3D 9 之間變更著色器常數的行為。</span><span class="sxs-lookup"><span data-stu-id="d6779-106">The behavior of shader constants has changed between Direct3D 8 and Direct3D 9.</span></span>

-   <span data-ttu-id="d6779-107">針對 Direct3D 9，使用 defx 設定的常數會將值指派給著色器常數空間。</span><span class="sxs-lookup"><span data-stu-id="d6779-107">For Direct3D 9, constants set with defx assign values to the shader constant space.</span></span> <span data-ttu-id="d6779-108">使用 defx 宣告之常數的存留期只限于該著色器的執行。</span><span class="sxs-lookup"><span data-stu-id="d6779-108">The lifetime of a constant declared with defx is confined to the execution of that shader only.</span></span> <span data-ttu-id="d6779-109">相反地，使用 Api 設定的常數 SetXXXShaderConstantX 會初始化全域空間中的常數。</span><span class="sxs-lookup"><span data-stu-id="d6779-109">Conversely, constants set using the APIs SetXXXShaderConstantX initialize constants in global space.</span></span> <span data-ttu-id="d6779-110">在呼叫 SetxxxShaderConstants 之前，不會將全域空間中的常數複製到 (著色器) 可見的本機空間。</span><span class="sxs-lookup"><span data-stu-id="d6779-110">Constants in global space are not copied to local space (visible to the shader) until SetxxxShaderConstants is called.</span></span>
-   <span data-ttu-id="d6779-111">針對 Direct3D 8，使用 defx 或 Api 設定的常數都會將值指派給著色器常數空間。</span><span class="sxs-lookup"><span data-stu-id="d6779-111">For Direct3D 8, constants set with defx or the APIs both assign values to the shader constant space.</span></span> <span data-ttu-id="d6779-112">每次執行著色器時，目前的著色器都會使用常數，而不考慮用來設定它們的技巧。</span><span class="sxs-lookup"><span data-stu-id="d6779-112">Each time the shader is executed, the constants are used by the current shader regardless of the technique used to set them.</span></span>

## <a name="examples"></a><span data-ttu-id="d6779-113">範例</span><span class="sxs-lookup"><span data-stu-id="d6779-113">Examples</span></span>

<span data-ttu-id="d6779-114">以下是在著色器中宣告兩個浮點常數的範例。</span><span class="sxs-lookup"><span data-stu-id="d6779-114">Here is an example declaring two floating-point constants within a shader.</span></span>


```
def c40, 0.0f,0.0f,0.0f,0.0f;
```



<span data-ttu-id="d6779-115">每次呼叫 [**SetPixelShader**](/windows/desktop/api/d3d9helper/nf-d3d9helper-idirect3ddevice9-setpixelshader) 時，就會載入這些常數。</span><span class="sxs-lookup"><span data-stu-id="d6779-115">These constants are loaded every time [**SetPixelShader**](/windows/desktop/api/d3d9helper/nf-d3d9helper-idirect3ddevice9-setpixelshader) is called.</span></span>

<span data-ttu-id="d6779-116">如果您要使用 API 來設定常數值，則不需要著色器宣告。</span><span class="sxs-lookup"><span data-stu-id="d6779-116">If you are setting constant values with the API, there is no shader declaration required.</span></span>

## <a name="related-topics"></a><span data-ttu-id="d6779-117">相關主題</span><span class="sxs-lookup"><span data-stu-id="d6779-117">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="d6779-118">寄存 器</span><span class="sxs-lookup"><span data-stu-id="d6779-118">Registers</span></span>](dx9-graphics-reference-asm-ps-registers.md)
</dt> </dl>

 

 