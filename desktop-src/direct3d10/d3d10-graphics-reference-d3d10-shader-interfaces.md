---
description: 本節包含下列著色器介面的相關資訊：
ms.assetid: d8770b45-a05c-4dd8-9fa7-08fb4330d734
title: " (Direct3D 10 圖形) 的著色器介面"
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 838a65d263533d0b2225515664e21c2d93114495
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/07/2021
ms.locfileid: "104468285"
---
# <a name="shader-interfaces-direct3d-10-graphics"></a><span data-ttu-id="10f49-103"> (Direct3D 10 圖形) 的著色器介面</span><span class="sxs-lookup"><span data-stu-id="10f49-103">Shader Interfaces (Direct3D 10 Graphics)</span></span>

<span data-ttu-id="10f49-104">本節包含下列著色器介面的相關資訊：</span><span class="sxs-lookup"><span data-stu-id="10f49-104">This section contains information about the following shader interfaces:</span></span>

<span data-ttu-id="10f49-105">這些著色器介面都會管理已編譯的著色器。</span><span class="sxs-lookup"><span data-stu-id="10f49-105">Each of these shader interfaces manages a compiled shader.</span></span> <span data-ttu-id="10f49-106">介面是在編譯著色器時建立，然後傳遞至需要存取已編譯著色器的各種 Api;例如，將著色器系結至管線階段或取得著色器簽章時。</span><span class="sxs-lookup"><span data-stu-id="10f49-106">The interface is created when a shader is compiled, and is then passed to various APIs that need access to a compiled shader; such as when binding a shader to a pipeline stage or getting a shader signature.</span></span>



| <span data-ttu-id="10f49-107">Pipeline-Stage 介面</span><span class="sxs-lookup"><span data-stu-id="10f49-107">Pipeline-Stage Interfaces</span></span>                                      | <span data-ttu-id="10f49-108">Description</span><span class="sxs-lookup"><span data-stu-id="10f49-108">Description</span></span>                                                                                                                                 |
|----------------------------------------------------------------|---------------------------------------------------------------------------------------------------------------------------------------------|
| [<span data-ttu-id="10f49-109">**ID3D10GeometryShader 介面**</span><span class="sxs-lookup"><span data-stu-id="10f49-109">**ID3D10GeometryShader Interface**</span></span>](/windows/win32/api/d3d10/nn-d3d10-id3d10geometryshader) | <span data-ttu-id="10f49-110">幾何著色器會在 [幾何著色器階段](d3d10-graphics-programming-guide-pipeline-stages.md)中執行每個基本處理。</span><span class="sxs-lookup"><span data-stu-id="10f49-110">A geometry-shader implements per-primitive processing in the [geometry-shader stage](d3d10-graphics-programming-guide-pipeline-stages.md).</span></span> |
| [<span data-ttu-id="10f49-111">**ID3D10PixelShader 介面**</span><span class="sxs-lookup"><span data-stu-id="10f49-111">**ID3D10PixelShader Interface**</span></span>](/windows/win32/api/d3d10/nn-d3d10-id3d10pixelshader)       | <span data-ttu-id="10f49-112">圖元著色器會在 [圖元著色器階段](d3d10-graphics-programming-guide-pipeline-stages.md)中執行每圖元處理。</span><span class="sxs-lookup"><span data-stu-id="10f49-112">A pixel-shader implements per-pixel processing in the [pixel-shader stage](d3d10-graphics-programming-guide-pipeline-stages.md).</span></span>           |
| [<span data-ttu-id="10f49-113">**ID3D10VertexShader 介面**</span><span class="sxs-lookup"><span data-stu-id="10f49-113">**ID3D10VertexShader Interface**</span></span>](/windows/win32/api/d3d10/nn-d3d10-id3d10vertexshader)     | <span data-ttu-id="10f49-114">頂點著色器會在 [頂點著色器階段](d3d10-graphics-programming-guide-pipeline-stages.md)中執行每個頂點的處理。</span><span class="sxs-lookup"><span data-stu-id="10f49-114">A vertex-shader implements per-vertex processing in the [vertex-shader stage](d3d10-graphics-programming-guide-pipeline-stages.md).</span></span>        |



 

<span data-ttu-id="10f49-115">著色器-反映介面可讓應用程式在設計/撰寫時間檢查著色器的內容。</span><span class="sxs-lookup"><span data-stu-id="10f49-115">Shader-reflection interfaces allow an application to inspect the contents of a shader at design/author time.</span></span> <span data-ttu-id="10f49-116">著色器反映不適合用于在執行時間設定變數，因為它是著色器資料的鏡像，因此不支援設定資料的方法。</span><span class="sxs-lookup"><span data-stu-id="10f49-116">Shader reflection is not useful for setting variables at runtime as it is a mirror of the shader data, and therefore supports no methods for setting data.</span></span>



| <span data-ttu-id="10f49-117">Shader-Reflection 介面</span><span class="sxs-lookup"><span data-stu-id="10f49-117">Shader-Reflection Interfaces</span></span>                                                                   | <span data-ttu-id="10f49-118">Description</span><span class="sxs-lookup"><span data-stu-id="10f49-118">Description</span></span>                                                                        |
|------------------------------------------------------------------------------------------------|------------------------------------------------------------------------------------|
| [<span data-ttu-id="10f49-119">**ID3D10ShaderReflection 介面**</span><span class="sxs-lookup"><span data-stu-id="10f49-119">**ID3D10ShaderReflection Interface**</span></span>](/windows/desktop/api/D3D10Shader/nn-d3d10shader-id3d10shaderreflection)                             | <span data-ttu-id="10f49-120">COM 介面，可在作者時從編譯的著色器讀取資訊。</span><span class="sxs-lookup"><span data-stu-id="10f49-120">A COM interface for reading information from a compiled shader at author time.</span></span>     |
| [<span data-ttu-id="10f49-121">**ID3D10ShaderReflectionConstantBuffer 介面**</span><span class="sxs-lookup"><span data-stu-id="10f49-121">**ID3D10ShaderReflectionConstantBuffer Interface**</span></span>](/windows/desktop/api/D3D10Shader/nn-d3d10shader-id3d10shaderreflectionconstantbuffer) | <span data-ttu-id="10f49-122">取得著色器反射常數緩衝區介面的 helper 介面。</span><span class="sxs-lookup"><span data-stu-id="10f49-122">A helper interface for getting a shader-reflection constant-buffer interface.</span></span>      |
| [<span data-ttu-id="10f49-123">**ID3D10ShaderReflectionType 介面**</span><span class="sxs-lookup"><span data-stu-id="10f49-123">**ID3D10ShaderReflectionType Interface**</span></span>](/windows/desktop/api/D3D10Shader/nn-d3d10shader-id3d10shaderreflectiontype)                     | <span data-ttu-id="10f49-124">用來取得著色器反映類型介面的 helper 介面。</span><span class="sxs-lookup"><span data-stu-id="10f49-124">A helper interface for getting a shader-reflection-type interface.</span></span>                 |
| [<span data-ttu-id="10f49-125">**ID3D10ShaderReflectionVariable 介面**</span><span class="sxs-lookup"><span data-stu-id="10f49-125">**ID3D10ShaderReflectionVariable Interface**</span></span>](/windows/desktop/api/D3D10Shader/nn-d3d10shader-id3d10shaderreflectionvariable)             | <span data-ttu-id="10f49-126">取得著色器反射變數介面的 helper 介面。</span><span class="sxs-lookup"><span data-stu-id="10f49-126">A helper interface for getting a shader-reflection-variable interface.</span></span>             |
| [<span data-ttu-id="10f49-127">**ID3D10ShaderResourceView 介面**</span><span class="sxs-lookup"><span data-stu-id="10f49-127">**ID3D10ShaderResourceView Interface**</span></span>](/windows/desktop/api/d3d10/nn-d3d10-id3d10shaderresourceview)                         | <span data-ttu-id="10f49-128">著色器反映介面，可從著色器資源檢視讀取資訊。</span><span class="sxs-lookup"><span data-stu-id="10f49-128">A shader-reflection interface for reading information from a shader-resource view.</span></span> |



 

<span data-ttu-id="10f49-129">著色器反映 Api 會將一個 COM 著色器反映介面 ([**ID3D10ShaderReflection 介面**](/windows/desktop/api/D3D10Shader/nn-d3d10shader-id3d10shaderreflection)) 和數個非 COM 協助程式介面 (其餘介面) 。</span><span class="sxs-lookup"><span data-stu-id="10f49-129">Shader reflection APIs implement one COM shader reflection interface ([**ID3D10ShaderReflection Interface**](/windows/desktop/api/D3D10Shader/nn-d3d10shader-id3d10shaderreflection)) and several non-COM helper interfaces (the rest of the interfaces).</span></span> <span data-ttu-id="10f49-130">建立著色器反映物件時，會建立 **ID3D10ShaderReflection 介面**。</span><span class="sxs-lookup"><span data-stu-id="10f49-130">**ID3D10ShaderReflection Interface** is created when a shader reflection object is created.</span></span> <span data-ttu-id="10f49-131">它會遵循標準 COM 規則;建立介面會增加參考計數，而且當不再需要介面時，必須釋放該介面。</span><span class="sxs-lookup"><span data-stu-id="10f49-131">It follows standard COM rules; creating the interface increases a reference count and the interface must be released when it is no longer needed.</span></span> <span data-ttu-id="10f49-132">其餘的著色器反映介面是不會繼承自 IUnknown 的 helper 介面。</span><span class="sxs-lookup"><span data-stu-id="10f49-132">The remaining shader-reflection interfaces are helper interfaces that do not inherit from IUnknown.</span></span> <span data-ttu-id="10f49-133">這表示它們在建立時不會變更任何參考計數，而且當您完成時，不需要終結它們。</span><span class="sxs-lookup"><span data-stu-id="10f49-133">This means that they do not change any reference count when they are created, and they do not need to be destroyed when you are finished with them.</span></span>

## <a name="related-topics"></a><span data-ttu-id="10f49-134">相關主題</span><span class="sxs-lookup"><span data-stu-id="10f49-134">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="10f49-135">著色器參考</span><span class="sxs-lookup"><span data-stu-id="10f49-135">Shader Reference</span></span>](d3d10-graphics-reference-d3d10-shader.md)
</dt> </dl>

 

 
