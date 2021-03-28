---
title: '高階著色器語言 (HLSL) '
description: HLSL 是一種類似 C 的高階著色器語言，您可以搭配 DirectX 中的可程式化著色器來使用。
ms.assetid: 09cdd8d6-0cf5-4f7e-b480-f748d2fa9ca9
ms.topic: article
ms.date: 01/11/2021
topic_type:
- kbArticle
api_name: ''
api_type: ''
api_location: ''
ms.custom: contperf-fy21q3
ms.openlocfilehash: c0876cda302d4c6215b640c210e880795273cd6c
ms.sourcegitcommit: de72a1294df274b0a71dc0fdc42d757e5f6df0f3
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 03/05/2021
ms.locfileid: "104973893"
---
# <a name="high-level-shader-language-hlsl"></a><span data-ttu-id="d7336-103">高階著色器語言 (HLSL) </span><span class="sxs-lookup"><span data-stu-id="d7336-103">High-level shader language (HLSL)</span></span>

<span data-ttu-id="d7336-104">HLSL 是一種類似 C 的高階著色器語言，您可以搭配 DirectX 中的可程式化著色器來使用。</span><span class="sxs-lookup"><span data-stu-id="d7336-104">HLSL is the C-like high-level shader language that you use with programmable shaders in DirectX.</span></span>

<span data-ttu-id="d7336-105">例如，您可以使用 HLSL 來撰寫 [頂點著色器](../direct3d11/vertex-shader-stage.md)或 [圖元著色器](../direct3d11/pixel-shader-stage.md)，並在您的 [Direct3D](../direct3d12/directx-12-programming-guide.md) 應用程式中，于轉譯器的執行中使用這些著色器。</span><span class="sxs-lookup"><span data-stu-id="d7336-105">For example, you can use HLSL to write a [vertex shader](../direct3d11/vertex-shader-stage.md), or a [pixel shader](../direct3d11/pixel-shader-stage.md), and use those shaders in the implementation of the renderer in your [Direct3D](../direct3d12/directx-12-programming-guide.md) application.</span></span>

<span data-ttu-id="d7336-106">或者，您也可以使用 HLSL 來撰寫計算著色器，以執行物理模擬。</span><span class="sxs-lookup"><span data-stu-id="d7336-106">Or you could use HLSL to write a compute shader, perhaps to implement a physics simulation.</span></span> <span data-ttu-id="d7336-107">不過，比方說，如果您想要撰寫自己的卷積運算子來 (影像處理) 作為計算著色器中的 HLSL，則在該案例中，如果您改用 [直接 Machine Learning (DirectML) ](../direct3d12/dml.md) ，就會獲得更好的效能。</span><span class="sxs-lookup"><span data-stu-id="d7336-107">However, if for example you're inclined to write your own convolution operator (for image processing) as HLSL in a compute shader, then you'll get better performance in that scenario if you use [Direct Machine Learning (DirectML)](../direct3d12/dml.md) instead.</span></span>

<span data-ttu-id="d7336-108">HLSL 的建立 (從 DirectX 9 開始) 設定可程式化 3D [管線](../direct3d11/overviews-direct3d-11-graphics-pipeline.md)。</span><span class="sxs-lookup"><span data-stu-id="d7336-108">HLSL was created (starting with DirectX 9) to set up the programmable 3D [pipeline](../direct3d11/overviews-direct3d-11-graphics-pipeline.md).</span></span> <span data-ttu-id="d7336-109">您可以使用 HLSL 指示來編寫整個管線的程式。</span><span class="sxs-lookup"><span data-stu-id="d7336-109">You can program the entire pipeline with HLSL instructions.</span></span>

## <a name="where-to-go-next"></a><span data-ttu-id="d7336-110">接下來要前往哪裡</span><span class="sxs-lookup"><span data-stu-id="d7336-110">Where to go next</span></span>

* [<span data-ttu-id="d7336-111">HLSL 程式設計指南</span><span class="sxs-lookup"><span data-stu-id="d7336-111">Programming guide for HLSL</span></span>](./dx-graphics-hlsl-pguide.md)
* [<span data-ttu-id="d7336-112">HLSL 的參考</span><span class="sxs-lookup"><span data-stu-id="d7336-112">Reference for HLSL</span></span>](./dx-graphics-hlsl-reference.md)

### <a name="programming-guide-for-hlsl"></a><span data-ttu-id="d7336-113">HLSL 程式設計指南</span><span class="sxs-lookup"><span data-stu-id="d7336-113">Programming guide for HLSL</span></span>

<span data-ttu-id="d7336-114">如需 HLSL 的概念簡介，請參閱 [HLSL 的程式設計指南](./dx-graphics-hlsl-pguide.md)。</span><span class="sxs-lookup"><span data-stu-id="d7336-114">For a conceptual introduction to HLSL, see the [Programming guide for HLSL](./dx-graphics-hlsl-pguide.md).</span></span>

<span data-ttu-id="d7336-115">程式設計指南會討論不同種類的著色器階段，以及如何建立、編譯、優化、系結和連結著色器。</span><span class="sxs-lookup"><span data-stu-id="d7336-115">The programming guide discusses the different kinds of shader stages, and how to create, compile, optimize, bind, and link shaders.</span></span>

<span data-ttu-id="d7336-116">您也可以在這裡找到有關連續產生的著色器模型版本（已發行）的總覽，以及 HLSL 著色器模型5的最新版說明。</span><span class="sxs-lookup"><span data-stu-id="d7336-116">There you'll also find overviews of, and release notes about, the successive generations of shader model version that have been released, going back as far as HLSL shader model 5.</span></span>

### <a name="reference-for-hlsl"></a><span data-ttu-id="d7336-117">HLSL 的參考</span><span class="sxs-lookup"><span data-stu-id="d7336-117">Reference for HLSL</span></span>

<span data-ttu-id="d7336-118">如需 HLSL 參考檔，請參閱 [HLSL 的參考](./dx-graphics-hlsl-reference.md)。</span><span class="sxs-lookup"><span data-stu-id="d7336-118">For HLSL reference documentation, see the [Reference for HLSL](./dx-graphics-hlsl-reference.md).</span></span>

<span data-ttu-id="d7336-119">參考章節包含 HLSL 內建的語言語法和內建函式的完整清單，以簡化您的程式碼需求。</span><span class="sxs-lookup"><span data-stu-id="d7336-119">The reference section has a complete listing of the language syntax and of the intrinsic functions that are built into HLSL in order to simplify your coding requirements.</span></span>

<span data-ttu-id="d7336-120">此外，您還可以找到著色器模型與設定檔的討論，以及 HLSL 著色器模型1最多的著色器模型參考內容。</span><span class="sxs-lookup"><span data-stu-id="d7336-120">There also you'll find a discussion of shader models versus profiles, and shader model reference content going back as far as HLSL shader model 1.</span></span> <span data-ttu-id="d7336-121">此外也有內容涵蓋元件指示、D3DCompiler 工具，以及著色器可以傳回之錯誤和警告的相關資訊。</span><span class="sxs-lookup"><span data-stu-id="d7336-121">There's also content covering assembly instructions, the D3DCompiler tool, and info about the errors and warnings that a shader can return.</span></span>