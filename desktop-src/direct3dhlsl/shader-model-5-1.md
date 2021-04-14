---
title: 著色器模型5。1
description: 本章節包含 HLSL 著色器模型5.1 的參考頁面（使用 D3D12 引進）。
ms.assetid: 814FAC95-7FD5-450F-964B-18E687DBCC56
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: d5fd2f2a2f4ebe86a090ebade8ebf8a033a7c612
ms.sourcegitcommit: fe03c5d92ca6a0d66a114b2303e99c0a19241ffb
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 11/20/2019
ms.locfileid: "104990747"
---
# <a name="shader-model-51"></a><span data-ttu-id="4d12c-103">著色器模型5。1</span><span class="sxs-lookup"><span data-stu-id="4d12c-103">Shader Model 5.1</span></span>

<span data-ttu-id="4d12c-104">本章節包含 HLSL 著色器模型5.1 的參考頁面（使用 D3D12 引進）。</span><span class="sxs-lookup"><span data-stu-id="4d12c-104">This section contains the reference pages for HLSL Shader Model 5.1, introduced with D3D12.</span></span>

<span data-ttu-id="4d12c-105">著色器模型5.1 的功能與 [著色器模型 5](d3d11-graphics-reference-sm5.md)很類似，主要變更是在資源選取專案中提供更大的彈性，方法是允許從著色器內編制描述元陣列的索引。</span><span class="sxs-lookup"><span data-stu-id="4d12c-105">Shader Model 5.1 is functionally very similar to [Shader Model 5](d3d11-graphics-reference-sm5.md), the main change is more flexibility in resource selection by allowing indexing of arrays of descriptors from within a shader.</span></span>



| <span data-ttu-id="4d12c-106">功能</span><span class="sxs-lookup"><span data-stu-id="4d12c-106">Feature</span></span>                   | <span data-ttu-id="4d12c-107">功能</span><span class="sxs-lookup"><span data-stu-id="4d12c-107">Capability</span></span>                                                                |
|---------------------------|---------------------------------------------------------------------------|
| <span data-ttu-id="4d12c-108">指令集</span><span class="sxs-lookup"><span data-stu-id="4d12c-108">Instruction Set</span></span>           | [<span data-ttu-id="4d12c-109">**HLSL 內建函式**</span><span class="sxs-lookup"><span data-stu-id="4d12c-109">**HLSL intrinsic functions**</span></span>](dx-graphics-hlsl-intrinsic-functions.md)  |
| <span data-ttu-id="4d12c-110">頂點著色器最大值</span><span class="sxs-lookup"><span data-stu-id="4d12c-110">Vertex Shader Max</span></span>         | <span data-ttu-id="4d12c-111">沒有限制</span><span class="sxs-lookup"><span data-stu-id="4d12c-111">No restriction</span></span>                                                            |
| <span data-ttu-id="4d12c-112">圖元著色器最大值</span><span class="sxs-lookup"><span data-stu-id="4d12c-112">Pixel Shader Max</span></span>          | <span data-ttu-id="4d12c-113">沒有限制</span><span class="sxs-lookup"><span data-stu-id="4d12c-113">No restriction</span></span>                                                            |
| <span data-ttu-id="4d12c-114">新增著色器設定檔</span><span class="sxs-lookup"><span data-stu-id="4d12c-114">New Shader Profiles Added</span></span> | <span data-ttu-id="4d12c-115">cs \_ 5 \_ 1、ds \_ 5 \_ 1、gs \_ 5 \_ 1、hs \_ 5 \_ 1、ps \_ 5 \_ 1、vs \_ 5 1、 \_ rootsig \_ 1 \_ 0</span><span class="sxs-lookup"><span data-stu-id="4d12c-115">cs\_5\_1, ds\_5\_1, gs\_5\_1, hs\_5\_1, ps\_5\_1, vs\_5\_1, rootsig\_1\_0</span></span> |



 

## <a name="in-this-section"></a><span data-ttu-id="4d12c-116">本節內容</span><span class="sxs-lookup"><span data-stu-id="4d12c-116">In this section</span></span>



| <span data-ttu-id="4d12c-117">主題</span><span class="sxs-lookup"><span data-stu-id="4d12c-117">Topic</span></span>                                                                           | <span data-ttu-id="4d12c-118">描述</span><span class="sxs-lookup"><span data-stu-id="4d12c-118">Description</span></span>                                                           |
|---------------------------------------------------------------------------------|-----------------------------------------------------------------------|
| [<span data-ttu-id="4d12c-119">著色器模型5.1 物件</span><span class="sxs-lookup"><span data-stu-id="4d12c-119">Shader Model 5.1 Objects</span></span>](shader-model-5-1-objects.md)<br/>             | <span data-ttu-id="4d12c-120">下列物件已新增至著色器模型5.1。</span><span class="sxs-lookup"><span data-stu-id="4d12c-120">The following objects have been added to shader model 5.1.</span></span><br/> |
| [<span data-ttu-id="4d12c-121">著色器模型5.1 系統值</span><span class="sxs-lookup"><span data-stu-id="4d12c-121">Shader Model 5.1 System Values</span></span>](shader-model-5-1-system-values.md)<br/> | <span data-ttu-id="4d12c-122">著色器模型5.1 會新增下列新的系統值。</span><span class="sxs-lookup"><span data-stu-id="4d12c-122">Shader Model 5.1 adds the following new system values.</span></span><br/>     |



 

## <a name="related-topics"></a><span data-ttu-id="4d12c-123">相關主題</span><span class="sxs-lookup"><span data-stu-id="4d12c-123">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="4d12c-124">著色器模型與著色器設定檔</span><span class="sxs-lookup"><span data-stu-id="4d12c-124">Shader Models vs Shader Profiles</span></span>](dx-graphics-hlsl-models.md)
</dt> <dt>

[<span data-ttu-id="4d12c-125">適用于 Direct3D 12 的 HLSL 著色器模型5.1 功能</span><span class="sxs-lookup"><span data-stu-id="4d12c-125">HLSL Shader Model 5.1 Features for Direct3D 12</span></span>](hlsl-shader-model-5-1-features-for-direct3d-12.md)
</dt> </dl>

 

 





