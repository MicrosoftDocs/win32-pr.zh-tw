---
title: 著色器介面 (Direct3D 11 圖形)
description: 本節包含著色器介面的相關資訊。
ms.assetid: 1791d2c9-3791-47fe-b887-a8117ecc798b
keywords:
- 介面、Direct3D 11 著色器
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 41fcecdff6f35b634ecbbeca0b85bc5ba42fd1e5
ms.sourcegitcommit: 9b5faa61c38b2d0c432b7f2dbee8c127b0e28a7e
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/19/2021
ms.locfileid: "122479454"
---
# <a name="shader-interfaces-direct3d-11-graphics"></a>著色器介面 (Direct3D 11 圖形)

本節包含著色器介面的相關資訊。

這些著色器介面都會管理已編譯的著色器。 介面是在編譯著色器時建立，然後傳遞至需要存取已編譯著色器的各種 Api;例如，將著色器系結至管線階段或取得著色器簽章時。


## <a name="in-this-section"></a>本節內容




| 主題 | 描述 | 
|-------|-------------|
| <a href="/windows/desktop/api/D3D11/nn-d3d11-id3d11classinstance"><strong>ID3D11ClassInstance</strong></a><br /> | 此介面會封裝 HLSL 類別。<br /> | 
| <a href="/windows/desktop/api/D3D11/nn-d3d11-id3d11classlinkage"><strong>ID3D11ClassLinkage</strong></a><br /> | 此介面會封裝 HLSL 動態連結。<br /> | 
| <a href="/windows/desktop/api/d3d11/nn-d3d11-id3d11computeshader"><strong>ID3D11ComputeShader</strong></a><br /> | 計算著色器介面會管理可執行程式， (可控制計算著色器階段的計算著色器) 。<br /> | 
| <a href="/windows/desktop/api/d3d11/nn-d3d11-id3d11domainshader"><strong>ID3D11DomainShader</strong></a><br /> | 網域著色器介面會管理可執行程式， (可控制網域著色器階段的網域著色器) 。<br /> | 
| <a href="/windows/desktop/api/D3D11Shader/nn-d3d11shader-id3d11functionlinkinggraph"><strong>ID3D11FunctionLinkingGraph</strong></a><br /> | 函式連結-圖形介面是用來建立著色器，其中包含一系列將值傳遞給彼此的先行編譯函式呼叫。 <br /><blockquote>[!Note]<br />此介面是 HLSL 著色器連結技術的一部分，可讓您在所有 Direct3D 11 平臺上用來建立先行編譯的 HLSL 函式、將它們封裝成程式庫，並在執行時間將它們連結到完整的著色器。</blockquote><br /> | 
| <a href="/windows/desktop/api/D3D11Shader/nn-d3d11shader-id3d11functionreflection"><strong>ID3D11FunctionReflection</strong></a><br /> | 函數反映介面會存取函式資訊。 <br /><blockquote>[!Note]<br />此介面是 HLSL 著色器連結技術的一部分，可讓您在所有 Direct3D 11 平臺上用來建立先行編譯的 HLSL 函式、將它們封裝成程式庫，並在執行時間將它們連結到完整的著色器。</blockquote><br /> | 
| <a href="/windows/desktop/api/D3D11Shader/nn-d3d11shader-id3d11functionparameterreflection"><strong>ID3D11FunctionParameterReflection</strong></a><br /> | 函數參數反映介面會存取函式參數資訊。 <br /><blockquote>[!Note]<br />此介面是 HLSL 著色器連結技術的一部分，可讓您在所有 Direct3D 11 平臺上用來建立先行編譯的 HLSL 函式、將它們封裝成程式庫，並在執行時間將它們連結到完整的著色器。</blockquote><br /> | 
| <a href="/windows/desktop/api/d3d11/nn-d3d11-id3d11geometryshader"><strong>ID3D11GeometryShader</strong></a><br /> | 幾何著色器介面會管理可執行程式 (幾何著色器) ，可控制幾何著色器階段。<br /> | 
| <a href="/windows/desktop/api/d3d11/nn-d3d11-id3d11hullshader"><strong>ID3D11HullShader</strong></a><br /> | 輪廓著色器介面會管理可執行程式， (可控制輪廓著色器階段的輪廓著色器) 。<br /> | 
| <a href="/windows/desktop/api/D3D11Shader/nn-d3d11shader-id3d11libraryreflection"><strong>ID3D11LibraryReflection</strong></a><br /> | 程式庫反映介面會存取程式庫資訊。 <br /><blockquote>[!Note]<br />此介面是 HLSL 著色器連結技術的一部分，可讓您在所有 Direct3D 11 平臺上用來建立先行編譯的 HLSL 函式、將它們封裝成程式庫，並在執行時間將它們連結到完整的著色器。</blockquote><br /> | 
| <a href="/windows/desktop/api/D3D11Shader/nn-d3d11shader-id3d11linker"><strong>ID3D11Linker</strong></a><br /> | 連結器介面可用來連結著色器模組。 <br /><blockquote>[!Note]<br />此介面是 HLSL 著色器連結技術的一部分，可讓您在所有 Direct3D 11 平臺上用來建立先行編譯的 HLSL 函式、將它們封裝成程式庫，並在執行時間將它們連結到完整的著色器。</blockquote><br /> | 
| <a href="/windows/desktop/api/D3D11Shader/nn-d3d11shader-id3d11linkingnode"><strong>ID3D11LinkingNode</strong></a><br /> | 連結節點介面用於著色器連結。 <br /><blockquote>[!Note]<br />此介面是 HLSL 著色器連結技術的一部分，可讓您在所有 Direct3D 11 平臺上用來建立先行編譯的 HLSL 函式、將它們封裝成程式庫，並在執行時間將它們連結到完整的著色器。</blockquote><br /> | 
| <a href="/windows/desktop/api/D3D11Shader/nn-d3d11shader-id3d11module"><strong>ID3D11Module</strong></a><br /> | 模組介面會建立用於資源重新系結的模組實例。 <br /><blockquote>[!Note]<br />此介面是 HLSL 著色器連結技術的一部分，可讓您在所有 Direct3D 11 平臺上用來建立先行編譯的 HLSL 函式、將它們封裝成程式庫，並在執行時間將它們連結到完整的著色器。</blockquote><br /> | 
| <a href="/windows/desktop/api/D3D11Shader/nn-d3d11shader-id3d11moduleinstance"><strong>ID3D11ModuleInstance</strong></a><br /> | 模組實例介面是用來重新系結資源。 <br /><blockquote>[!Note]<br />此介面是 HLSL 著色器連結技術的一部分，可讓您在所有 Direct3D 11 平臺上用來建立先行編譯的 HLSL 函式、將它們封裝成程式庫，並在執行時間將它們連結到完整的著色器。</blockquote><br /> | 
| <a href="/windows/desktop/api/d3d11/nn-d3d11-id3d11pixelshader"><strong>ID3D11PixelShader</strong></a><br /> | 圖元著色器介面會管理可執行程式， (可控制圖元著色器階段的圖元著色器) 。<br /> | 
| <a href="/windows/desktop/api/D3D11Shader/nn-d3d11shader-id3d11shaderreflection"><strong>ID3D11ShaderReflection</strong></a><br /> | 著色器反映介面會存取著色器資訊。<br /> | 
| <a href="/windows/desktop/api/D3D11Shader/nn-d3d11shader-id3d11shaderreflectionconstantbuffer"><strong>ID3D11ShaderReflectionConstantBuffer</strong></a><br /> | 此著色器反映介面可提供常數緩衝區的存取權。<br /> | 
| <a href="/windows/desktop/api/D3D11Shader/nn-d3d11shader-id3d11shaderreflectiontype"><strong>ID3D11ShaderReflectionType</strong></a><br /> | 此著色器反映介面可提供變數類型的存取。<br /> | 
| <a href="/windows/desktop/api/D3D11Shader/nn-d3d11shader-id3d11shaderreflectionvariable"><strong>ID3D11ShaderReflectionVariable</strong></a><br /> | 此著色器反映介面可提供變數的存取權。<br /> | 
| <a href="/windows/desktop/api/D3D11ShaderTracing/nn-d3d11shadertracing-id3d11shadertrace"><strong>ID3D11ShaderTrace</strong></a><br /> | <a href="/windows/desktop/api/D3D11ShaderTracing/nn-d3d11shadertracing-id3d11shadertrace"><strong>ID3D11ShaderTrace</strong></a>介面會實方法來取得著色器執行的追蹤。<br /> | 
| <a href="/windows/desktop/api/D3D11ShaderTracing/nn-d3d11shadertracing-id3d11shadertracefactory"><strong>ID3D11ShaderTraceFactory</strong></a><br /> | <a href="/windows/desktop/api/D3D11ShaderTracing/nn-d3d11shadertracing-id3d11shadertracefactory"><strong>ID3D11ShaderTraceFactory</strong></a>介面會實作為產生著色器追蹤資訊物件的方法。<br /> | 
| <a href="/windows/desktop/api/d3d11/nn-d3d11-id3d11vertexshader"><strong>ID3D11VertexShader</strong></a><br /> | 頂點著色器介面會管理可執行程式， (可控制頂點著色器階段的頂點著色器) 。<br /> | 




 

## <a name="related-topics"></a>相關主題

<dl> <dt>

[著色器參考](d3d11-graphics-reference-d3d11-shader.md)
</dt> </dl>

 

