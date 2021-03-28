---
title: 著色器模型1
description: 著色器模型1是在 DirectX 中建立的第一個著色器模型。 它會將頂點和圖元著色器引進第一個可程式化管線的執行。
ms.assetid: 565ee7b5-1266-4e2f-8c22-c0e60b8c4619
ms.topic: article
ms.date: 05/31/2018
topic_type:
- kbArticle
api_name: ''
api_type: ''
api_location: ''
ms.openlocfilehash: 4ebbc28c1c10ef112bf7be3b500be7f4ecaa6481
ms.sourcegitcommit: ae73f4dd3cf5a3c6a1ea7d191ca32a5b01f6686b
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 09/08/2020
ms.locfileid: "104024245"
---
# <a name="shader-model-1"></a><span data-ttu-id="c4cf1-104">著色器模型1</span><span class="sxs-lookup"><span data-stu-id="c4cf1-104">Shader Model 1</span></span>

<span data-ttu-id="c4cf1-105">著色器模型1是在 DirectX 中建立的第一個著色器模型。</span><span class="sxs-lookup"><span data-stu-id="c4cf1-105">Shader Model 1 was the first shader model created in DirectX.</span></span> <span data-ttu-id="c4cf1-106">它會將頂點和圖元著色器引進第一個可程式化管線的執行。</span><span class="sxs-lookup"><span data-stu-id="c4cf1-106">It introduced vertex and pixel shaders to the first implementation of the programmable pipeline.</span></span>



<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<tbody>
<tr class="odd">
<td><span data-ttu-id="c4cf1-107">功能</span><span class="sxs-lookup"><span data-stu-id="c4cf1-107">Feature</span></span></td>
<td><span data-ttu-id="c4cf1-108">功能</span><span class="sxs-lookup"><span data-stu-id="c4cf1-108">Capability</span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="c4cf1-109">指令集</span><span class="sxs-lookup"><span data-stu-id="c4cf1-109">Instruction Set</span></span></td>
<td><ul>
<li><span data-ttu-id="c4cf1-110"><a href="dx-graphics-hlsl-intrinsic-functions.md"><strong>HLSL 函式</strong></a></span><span class="sxs-lookup"><span data-stu-id="c4cf1-110"><a href="dx-graphics-hlsl-intrinsic-functions.md"><strong>HLSL functions</strong></a></span></span></li>
<li><span data-ttu-id="c4cf1-111">頂點著色器元件指示 (請參閱 <a href="dx9-graphics-reference-asm-vs-instructions-vs-1-1.md">指示-vs_1_1</a>) 。</span><span class="sxs-lookup"><span data-stu-id="c4cf1-111">Vertex shader assembly instructions (see <a href="dx9-graphics-reference-asm-vs-instructions-vs-1-1.md">Instructions - vs_1_1</a>).</span></span> <span data-ttu-id="c4cf1-112"> (ps_1_x) 的圖元著色器指令支援已被取代。</span><span class="sxs-lookup"><span data-stu-id="c4cf1-112">Support for pixel shader instructions (ps_1_x) has been deprecated.</span></span> <span data-ttu-id="c4cf1-113">若要將 ps_1_x 著色器編譯 ps_2_0 著色器，請參閱 <a href="/windows/desktop/direct3dtools/dx-graphics-tools-fxc-using">編譯著色器模型 1</a>。</span><span class="sxs-lookup"><span data-stu-id="c4cf1-113">To compile ps_1_x shaders as ps_2_0 shaders see <a href="/windows/desktop/direct3dtools/dx-graphics-tools-fxc-using">Compiling Shader Model 1</a>.</span></span></li>
</ul></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="c4cf1-114">註冊集</span><span class="sxs-lookup"><span data-stu-id="c4cf1-114">Register Set</span></span></td>
<td><ul>
<li><span data-ttu-id="c4cf1-115"><a href="dx9-graphics-reference-asm-vs-registers-vs-1-1.md">頂點著色器暫存器</a></span><span class="sxs-lookup"><span data-stu-id="c4cf1-115"><a href="dx9-graphics-reference-asm-vs-registers-vs-1-1.md">Vertex shader registers</a></span></span></li>
</ul></td>
</tr>
<tr class="even">
<td><span data-ttu-id="c4cf1-116">頂點著色器最大值</span><span class="sxs-lookup"><span data-stu-id="c4cf1-116">Vertex Shader Max</span></span></td>
<td><span data-ttu-id="c4cf1-117">128指示</span><span class="sxs-lookup"><span data-stu-id="c4cf1-117">128 instructions</span></span></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="c4cf1-118">著色器設定檔</span><span class="sxs-lookup"><span data-stu-id="c4cf1-118">Shader Profiles</span></span></td>
<td><span data-ttu-id="c4cf1-119">vs_1_1</span><span class="sxs-lookup"><span data-stu-id="c4cf1-119">vs_1_1</span></span></td>
</tr>
</tbody>
</table>



 

<span data-ttu-id="c4cf1-120">如需著色器模型1的詳細資訊，請參閱：</span><span class="sxs-lookup"><span data-stu-id="c4cf1-120">For more details on shader model 1, see:</span></span>

-   [<span data-ttu-id="c4cf1-121">頂點著色器</span><span class="sxs-lookup"><span data-stu-id="c4cf1-121">Vertex Shader</span></span>](dx9-graphics-reference-asm-vs-1-1.md)

## <a name="related-topics"></a><span data-ttu-id="c4cf1-122">相關主題</span><span class="sxs-lookup"><span data-stu-id="c4cf1-122">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="c4cf1-123">著色器模型與著色器設定檔</span><span class="sxs-lookup"><span data-stu-id="c4cf1-123">Shader Models vs Shader Profiles</span></span>](dx-graphics-hlsl-models.md)
</dt> </dl>

 

 