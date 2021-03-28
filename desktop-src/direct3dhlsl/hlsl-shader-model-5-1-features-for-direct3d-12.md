---
title: HLSL 著色器模型5。1
description: 本節說明著色器模型5.1 的功能，在實務上適用于 D3D12 和 D3D 11.3。 所有 DirectX 12 硬體都支援著色器模型5.1。
ms.assetid: 6EF38EB9-71CB-4591-AAE2-F3FFC23E73B8
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 1e13620fe81f3c1e7d3de1589f82171667834a26
ms.sourcegitcommit: 592c9bbd22ba69802dc353bcb5eb30699f9e9403
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/20/2020
ms.locfileid: "104463249"
---
# <a name="hlsl-shader-model-51"></a><span data-ttu-id="b15d1-104">HLSL 著色器模型5。1</span><span class="sxs-lookup"><span data-stu-id="b15d1-104">HLSL Shader Model 5.1</span></span>

<span data-ttu-id="b15d1-105">本節將描述著色器模型5.1 的功能，因為它們在實務上會套用至 D3D12。</span><span class="sxs-lookup"><span data-stu-id="b15d1-105">This section describes the features of Shader Model 5.1 as they apply in practice to D3D12.</span></span> <span data-ttu-id="b15d1-106">所有 DirectX 12 硬體都支援著色器模型5.1。</span><span class="sxs-lookup"><span data-stu-id="b15d1-106">All DirectX 12 hardware supports Shader Model 5.1.</span></span>

## <a name="in-this-section"></a><span data-ttu-id="b15d1-107">本節內容</span><span class="sxs-lookup"><span data-stu-id="b15d1-107">In this section</span></span>



| <span data-ttu-id="b15d1-108">主題</span><span class="sxs-lookup"><span data-stu-id="b15d1-108">Topic</span></span>                                                                         | <span data-ttu-id="b15d1-109">描述</span><span class="sxs-lookup"><span data-stu-id="b15d1-109">Description</span></span>                                                                                                                                              |
|-------------------------------------------------------------------------------|----------------------------------------------------------------------------------------------------------------------------------------------------------|
| [<span data-ttu-id="b15d1-110">SM 5.1 的位元組位元組變更</span><span class="sxs-lookup"><span data-stu-id="b15d1-110">Bytecode changes in SM5.1</span></span>](bytecode-changes-in-sm5-1.md)<br/>         | <span data-ttu-id="b15d1-111">SM 5.1 變更如何在指示中宣告和參考資源暫存器。</span><span class="sxs-lookup"><span data-stu-id="b15d1-111">SM5.1 changes how resource registers are declared and referenced in instructions.</span></span> <br/>                                                            |
| [<span data-ttu-id="b15d1-112">HLSL 指定的根簽章</span><span class="sxs-lookup"><span data-stu-id="b15d1-112">HLSL Specified Root Signature</span></span>](hlsl-specified-root-signature.md)<br/> | <span data-ttu-id="b15d1-113">[根](/windows/desktop/direct3d12/root-signatures)簽章 (資源的索引鍵資料表和 D3D12) 的其他元素，可以在 HLSL 中指定為字串。</span><span class="sxs-lookup"><span data-stu-id="b15d1-113">A [Root Signature](/windows/desktop/direct3d12/root-signatures) (a key table of resources and other elements for D3D12) can be specified in HLSL as a string.</span></span> <br/> |



 

<span data-ttu-id="b15d1-114">如需著色器語言的語法變更詳細資料，請參閱 [著色器模型 5.1](shader-model-5-1.md)。</span><span class="sxs-lookup"><span data-stu-id="b15d1-114">For details of the syntax changes to the shader language, refer to [Shader Model 5.1](shader-model-5-1.md).</span></span>

## <a name="related-topics"></a><span data-ttu-id="b15d1-115">相關主題</span><span class="sxs-lookup"><span data-stu-id="b15d1-115">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="b15d1-116">HLSL 的程式設計指南</span><span class="sxs-lookup"><span data-stu-id="b15d1-116">Programming Guide for HLSL</span></span>](dx-graphics-hlsl-pguide.md)
</dt> </dl>

 

