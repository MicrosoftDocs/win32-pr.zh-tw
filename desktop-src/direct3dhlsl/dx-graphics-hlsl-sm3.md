---
title: 著色器模型3
description: 著色器模型3將其他功能新增至著色器模型2。
ms.assetid: bd09f86e-946f-4281-bc48-1db5cd32b2ae
ms.topic: article
ms.date: 05/31/2018
topic_type:
- kbArticle
api_name: ''
api_type: ''
api_location: ''
ms.openlocfilehash: 9c53b8252f617c6ee3b95512a5d930a93f646479
ms.sourcegitcommit: ae73f4dd3cf5a3c6a1ea7d191ca32a5b01f6686b
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 09/08/2020
ms.locfileid: "104383049"
---
# <a name="shader-model-3-hlsl-reference"></a><span data-ttu-id="4fb2c-103">著色器模型 3 (HLSL 參考) </span><span class="sxs-lookup"><span data-stu-id="4fb2c-103">Shader Model 3 (HLSL reference)</span></span>

<span data-ttu-id="4fb2c-104">著色器模型3將其他功能新增至 [著色器模型 2](dx-graphics-hlsl-sm2.md)。</span><span class="sxs-lookup"><span data-stu-id="4fb2c-104">Shader Model 3 added additional capabilities to [shader model 2](dx-graphics-hlsl-sm2.md).</span></span>



<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<tbody>
<tr class="odd">
<td><span data-ttu-id="4fb2c-105">功能</span><span class="sxs-lookup"><span data-stu-id="4fb2c-105">Feature</span></span></td>
<td><span data-ttu-id="4fb2c-106">功能</span><span class="sxs-lookup"><span data-stu-id="4fb2c-106">Capability</span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="4fb2c-107">指令集</span><span class="sxs-lookup"><span data-stu-id="4fb2c-107">Instruction Set</span></span></td>
<td><ul>
<li><span data-ttu-id="4fb2c-108"><a href="dx-graphics-hlsl-intrinsic-functions.md"><strong>HLSL 函式</strong></a></span><span class="sxs-lookup"><span data-stu-id="4fb2c-108"><a href="dx-graphics-hlsl-intrinsic-functions.md"><strong>HLSL functions</strong></a></span></span></li>
<li><span data-ttu-id="4fb2c-109">元件指示 (請參閱 <a href="dx9-graphics-reference-asm-ps-instructions-ps-3-0.md">Ps_3_0 指示</a>、 <a href="dx9-graphics-reference-asm-vs-instructions-vs-3-0.md">指示-vs_3_0</a>) </span><span class="sxs-lookup"><span data-stu-id="4fb2c-109">Assembly instructions (see <a href="dx9-graphics-reference-asm-ps-instructions-ps-3-0.md">ps_3_0 Instructions</a>, <a href="dx9-graphics-reference-asm-vs-instructions-vs-3-0.md">Instructions - vs_3_0</a>)</span></span></li>
</ul></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="4fb2c-110">註冊集</span><span class="sxs-lookup"><span data-stu-id="4fb2c-110">Register Set</span></span></td>
<td><ul>
<li><span data-ttu-id="4fb2c-111">圖元著色器暫存器 (查看 <a href="dx9-graphics-reference-asm-ps-registers-ps-3-0.md">Ps_3_0 註冊</a>) </span><span class="sxs-lookup"><span data-stu-id="4fb2c-111">Pixel shader registers (see <a href="dx9-graphics-reference-asm-ps-registers-ps-3-0.md">ps_3_0 Registers</a>)</span></span></li>
<li><span data-ttu-id="4fb2c-112">頂點著色器註冊 (請參閱暫存器 <a href="dx9-graphics-reference-asm-vs-registers-vs-3-0.md">-vs_3_0</a>) </span><span class="sxs-lookup"><span data-stu-id="4fb2c-112">Vertex shader registers (see <a href="dx9-graphics-reference-asm-vs-registers-vs-3-0.md">Registers - vs_3_0</a>)</span></span></li>
</ul></td>
</tr>
<tr class="even">
<td><span data-ttu-id="4fb2c-113">圖元著色器最大值</span><span class="sxs-lookup"><span data-stu-id="4fb2c-113">Pixel Shader Max</span></span></td>
<td><span data-ttu-id="4fb2c-114">最小值為512，最多可達 D3DCAPS9 中的插槽數目。MaxPixelShader30InstructionSlots (請參閱 <a href="/windows/desktop/api/d3d9caps/ns-d3d9caps-d3dpshadercaps2_0"><strong>D3DPSHADERCAPS2_0</strong></a>) 。</span><span class="sxs-lookup"><span data-stu-id="4fb2c-114">512 minimum, and up to the number of slots in D3DCAPS9.MaxPixelShader30InstructionSlots (see <a href="/windows/desktop/api/d3d9caps/ns-d3d9caps-d3dpshadercaps2_0"><strong>D3DPSHADERCAPS2_0</strong></a>).</span></span></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="4fb2c-115">頂點著色器最大值</span><span class="sxs-lookup"><span data-stu-id="4fb2c-115">Vertex Shader Max</span></span></td>
<td><span data-ttu-id="4fb2c-116">最小值為512，最多可達 D3DCAPS9 中的插槽數目。MaxVertexShader30InstructionSlots (參閱 <a href="/windows/desktop/api/d3d9caps/ns-d3d9caps-d3dcaps9"><strong>D3DCAPS9</strong></a>) 。</span><span class="sxs-lookup"><span data-stu-id="4fb2c-116">512 minimum, and up to the number of slots in D3DCAPS9.MaxVertexShader30InstructionSlots (see <a href="/windows/desktop/api/d3d9caps/ns-d3d9caps-d3dcaps9"><strong>D3DCAPS9</strong></a>).</span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="4fb2c-117">著色器設定檔</span><span class="sxs-lookup"><span data-stu-id="4fb2c-117">Shader Profiles</span></span></td>
<td><span data-ttu-id="4fb2c-118">ps_3_0，vs_3_0</span><span class="sxs-lookup"><span data-stu-id="4fb2c-118">ps_3_0, vs_3_0</span></span></td>
</tr>
</tbody>
</table>



 

<span data-ttu-id="4fb2c-119">如需模型3著色器的詳細資訊，請參閱：</span><span class="sxs-lookup"><span data-stu-id="4fb2c-119">For more details on model 3 shaders, see:</span></span>

-   [<span data-ttu-id="4fb2c-120">圖元著色器3。0</span><span class="sxs-lookup"><span data-stu-id="4fb2c-120">Pixel Shader 3.0</span></span>](dx9-graphics-reference-asm-ps-3-0.md)
-   [<span data-ttu-id="4fb2c-121">頂點著色器3。0</span><span class="sxs-lookup"><span data-stu-id="4fb2c-121">Vertex Shader 3.0</span></span>](dx9-graphics-reference-asm-vs-3-0.md)

## <a name="related-topics"></a><span data-ttu-id="4fb2c-122">相關主題</span><span class="sxs-lookup"><span data-stu-id="4fb2c-122">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="4fb2c-123">著色器模型與著色器設定檔</span><span class="sxs-lookup"><span data-stu-id="4fb2c-123">Shader Models vs Shader Profiles</span></span>](dx-graphics-hlsl-models.md)
</dt> </dl>

 

 