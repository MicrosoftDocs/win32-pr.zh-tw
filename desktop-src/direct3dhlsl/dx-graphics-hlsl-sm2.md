---
title: 著色器模型2
description: 著色器模型2將其他功能新增至著色器模型1。
ms.assetid: 53c367d2-5b6a-4afa-894a-8ab9927169d5
ms.topic: article
ms.date: 05/31/2018
topic_type:
- kbArticle
api_name: ''
api_type: ''
api_location: ''
ms.openlocfilehash: 88bd2f6292687c5387fadf65f8f43437904168cc
ms.sourcegitcommit: 927b9c371f75f52b8011483edf3a4ba37d11ebe4
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 02/11/2020
ms.locfileid: "104990891"
---
# <a name="shader-model-2"></a><span data-ttu-id="c7cd4-103">著色器模型2</span><span class="sxs-lookup"><span data-stu-id="c7cd4-103">Shader Model 2</span></span>

<span data-ttu-id="c7cd4-104">著色器模型2將其他功能新增至 [著色器模型 1](dx-graphics-hlsl-sm1.md)。</span><span class="sxs-lookup"><span data-stu-id="c7cd4-104">Shader Model 2 added additional capabilities to [shader model 1](dx-graphics-hlsl-sm1.md).</span></span>



<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<tbody>
<tr class="odd">
<td><span data-ttu-id="c7cd4-105">功能</span><span class="sxs-lookup"><span data-stu-id="c7cd4-105">Feature</span></span></td>
<td><span data-ttu-id="c7cd4-106">功能</span><span class="sxs-lookup"><span data-stu-id="c7cd4-106">Capability</span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="c7cd4-107">指令集</span><span class="sxs-lookup"><span data-stu-id="c7cd4-107">Instruction Set</span></span></td>
<td><ul>
<li><span data-ttu-id="c7cd4-108"><a href="dx-graphics-hlsl-intrinsic-functions.md"><strong>HLSL 函式</strong></a></span><span class="sxs-lookup"><span data-stu-id="c7cd4-108"><a href="dx-graphics-hlsl-intrinsic-functions.md"><strong>HLSL functions</strong></a></span></span></li>
<li><span data-ttu-id="c7cd4-109">元件指示 (請參閱 <a href="dx9-graphics-reference-asm-vs-instructions-vs-2-0.md">指示-vs_2_0</a>、 <a href="dx9-graphics-reference-asm-vs-instructions-vs-2-x.md">指示 Vs_2_x</a>、 <a href="dx9-graphics-reference-asm-ps-instructions-ps-2-0.md">ps_2_0 指示</a>、 <a href="dx9-graphics-reference-asm-ps-instructions-ps-2-x.md">ps_2_x 指示</a>) </span><span class="sxs-lookup"><span data-stu-id="c7cd4-109">Assembly instructions (see <a href="dx9-graphics-reference-asm-vs-instructions-vs-2-0.md">Instructions - vs_2_0</a>, <a href="dx9-graphics-reference-asm-vs-instructions-vs-2-x.md">Instructions - vs_2_x</a>, <a href="dx9-graphics-reference-asm-ps-instructions-ps-2-0.md">ps_2_0 Instructions</a>, <a href="dx9-graphics-reference-asm-ps-instructions-ps-2-x.md">ps_2_x Instructions</a>)</span></span></li>
</ul></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="c7cd4-110">註冊集</span><span class="sxs-lookup"><span data-stu-id="c7cd4-110">Register Set</span></span></td>
<td><ul>
<li><span data-ttu-id="c7cd4-111">圖元著色器暫存器 (查看 <a href="dx9-graphics-reference-asm-ps-registers-ps-2-0.md">ps_2_0</a>暫存器、 <a href="dx9-graphics-reference-asm-ps-registers-ps-2-x.md">ps_2_x 註冊</a>) </span><span class="sxs-lookup"><span data-stu-id="c7cd4-111">Pixel shader registers (see <a href="dx9-graphics-reference-asm-ps-registers-ps-2-0.md">ps_2_0 Registers</a>, <a href="dx9-graphics-reference-asm-ps-registers-ps-2-x.md">ps_2_x Registers</a>)</span></span></li>
<li><span data-ttu-id="c7cd4-112">頂點著色器暫存器 (請參閱暫存器 <a href="dx9-graphics-reference-asm-vs-registers-vs-2-0.md">-vs_2_0</a>、暫存器 <a href="dx9-graphics-reference-asm-vs-registers-vs-2-x.md">vs_2_x</a>) </span><span class="sxs-lookup"><span data-stu-id="c7cd4-112">Vertex shader registers (see <a href="dx9-graphics-reference-asm-vs-registers-vs-2-0.md">Registers - vs_2_0</a>, <a href="dx9-graphics-reference-asm-vs-registers-vs-2-x.md">Registers - vs_2_x</a>)</span></span></li>
</ul></td>
</tr>
<tr class="even">
<td><span data-ttu-id="c7cd4-113">圖元著色器最大值</span><span class="sxs-lookup"><span data-stu-id="c7cd4-113">Pixel Shader Max</span></span></td>
<td><ul>
<li><span data-ttu-id="c7cd4-114">ps_2_0-32 材質 + 64 算術</span><span class="sxs-lookup"><span data-stu-id="c7cd4-114">ps_2_0 - 32 texture + 64 arithmetic</span></span></li>
<li><span data-ttu-id="c7cd4-115">ps_2_x-96 的最小值，最多可達 D3DCAPS9 中的插槽數目。D3DPSHADERCAPS2_0. NumInstructionSlots。</span><span class="sxs-lookup"><span data-stu-id="c7cd4-115">ps_2_x - 96 minimum, and up to the number of slots in D3DCAPS9.D3DPSHADERCAPS2_0.NumInstructionSlots.</span></span> <span data-ttu-id="c7cd4-116">請參閱 D3DPSHADERCAPS2_0</span><span class="sxs-lookup"><span data-stu-id="c7cd4-116">See D3DPSHADERCAPS2_0</span></span></li>
</ul></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="c7cd4-117">頂點著色器最大值</span><span class="sxs-lookup"><span data-stu-id="c7cd4-117">Vertex Shader Max</span></span></td>
<td><span data-ttu-id="c7cd4-118">256指示</span><span class="sxs-lookup"><span data-stu-id="c7cd4-118">256 instructions</span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="c7cd4-119">著色器設定檔</span><span class="sxs-lookup"><span data-stu-id="c7cd4-119">Shader Profiles</span></span></td>
<td><span data-ttu-id="c7cd4-120">ps_2_0、ps_2_x、vs_2_0、vs_2_x</span><span class="sxs-lookup"><span data-stu-id="c7cd4-120">ps_2_0, ps_2_x, vs_2_0, vs_2_x</span></span></td>
</tr>
</tbody>
</table>



 

<span data-ttu-id="c7cd4-121">如需著色器模型2的詳細資訊，請參閱：</span><span class="sxs-lookup"><span data-stu-id="c7cd4-121">For more details on shader model 2, see:</span></span>

-   <span data-ttu-id="c7cd4-122">[圖元著色器 2.0](dx9-graphics-reference-asm-ps-2-0.md)、[圖元著色器](dx9-graphics-reference-asm-ps-2-x.md)2。x</span><span class="sxs-lookup"><span data-stu-id="c7cd4-122">[Pixel Shader 2.0](dx9-graphics-reference-asm-ps-2-0.md), [Pixel Shader 2.x](dx9-graphics-reference-asm-ps-2-x.md)</span></span>
-   <span data-ttu-id="c7cd4-123">[頂點著色器 2.0](dx9-graphics-reference-asm-vs-2-0.md)、[頂點著色器](dx9-graphics-reference-asm-vs-2-x.md)2。x</span><span class="sxs-lookup"><span data-stu-id="c7cd4-123">[Vertex Shader 2.0](dx9-graphics-reference-asm-vs-2-0.md), [Vertex Shader 2.x](dx9-graphics-reference-asm-vs-2-x.md)</span></span>

## <a name="related-topics"></a><span data-ttu-id="c7cd4-124">相關主題</span><span class="sxs-lookup"><span data-stu-id="c7cd4-124">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="c7cd4-125">著色器模型與著色器設定檔</span><span class="sxs-lookup"><span data-stu-id="c7cd4-125">Shader Models vs Shader Profiles</span></span>](dx-graphics-hlsl-models.md)
</dt> </dl>

 

 




