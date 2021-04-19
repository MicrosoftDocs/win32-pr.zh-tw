---
title: " (Direct3D 12 圖形) 的著色器介面"
description: D3d12shader 會宣告下列介面。
ms.assetid: 791d2c91-3791-47fe-b887-8117ecc798ba
keywords:
- 介面，Direct3D 12 著色器
ms.localizationpriority: low
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 16f111572aacca36f12600b0cf334895684064e5
ms.sourcegitcommit: 8fa6614b715bddf14648cce36d2df22e5232801a
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 12/10/2020
ms.locfileid: "106967705"
---
# <a name="shader-interfaces-direct3d-12-graphics"></a> (Direct3D 12 圖形) 的著色器介面

d3d12shader 會宣告下列介面。

## <a name="in-this-section"></a>本節內容



<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<thead>
<tr class="header">
<th>主題</th>
<th>描述</th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><a href="/windows/desktop/api/d3d12shader/nn-d3d12shader-id3d12functionparameterreflection"><strong>ID3D12FunctionParameterReflection</strong></a><br/></td>
<td>函數參數反映介面會存取函式參數資訊。 <br/>
<blockquote>
[!Note]<br />
此介面是 HLSL 著色器連結技術的一部分，可讓您在所有 Direct3D 12 平臺上用來建立先行編譯的 HLSL 函式、將它們封裝成程式庫，並在執行時間將它們連結到完整的著色器。
</blockquote>
<br/></td>
</tr>
<tr class="even">
<td><a href="/windows/desktop/api/d3d12shader/nn-d3d12shader-id3d12functionreflection"><strong>ID3D12FunctionReflection</strong></a><br/></td>
<td>函數反映介面會存取函式資訊。 <br/>
<blockquote>
[!Note]<br />
此介面是 HLSL 著色器連結技術的一部分，可讓您在所有 Direct3D 12 平臺上用來建立先行編譯的 HLSL 函式、將它們封裝成程式庫，並在執行時間將它們連結到完整的著色器。
</blockquote>
<br/></td>
</tr>
<tr class="odd">
<td><a href="/windows/desktop/api/d3d12shader/nn-d3d12shader-id3d12libraryreflection"><strong>ID3D12LibraryReflection</strong></a><br/></td>
<td>程式庫反映介面會存取程式庫資訊。 <br/>
<blockquote>
[!Note]<br />
此介面是 HLSL 著色器連結技術的一部分，可讓您在所有 Direct3D 12 平臺上用來建立先行編譯的 HLSL 函式、將它們封裝成程式庫，並在執行時間將它們連結到完整的著色器。
</blockquote>
<br/></td>
</tr>
<tr class="even">
<td><a href="/windows/desktop/api/d3d12shader/nn-d3d12shader-id3d12shaderreflection"><strong>ID3D12ShaderReflection</strong></a><br/></td>
<td>著色器反映介面會存取著色器資訊。 <br/></td>
</tr>
<tr class="odd">
<td><a href="/windows/desktop/api/d3d12shader/nn-d3d12shader-id3d12shaderreflectionconstantbuffer"><strong>ID3D12ShaderReflectionConstantBuffer</strong></a><br/></td>
<td>此著色器反映介面可提供常數緩衝區的存取權。 <br/></td>
</tr>
<tr class="even">
<td><a href="/windows/desktop/api/d3d12shader/nn-d3d12shader-id3d12shaderreflectiontype"><strong>ID3D12ShaderReflectionType</strong></a><br/></td>
<td>此著色器反映介面可提供變數類型的存取。 <br/></td>
</tr>
<tr class="odd">
<td><a href="/windows/desktop/api/d3d12shader/nn-d3d12shader-id3d12shaderreflectionvariable"><strong>ID3D12ShaderReflectionVariable</strong></a><br/></td>
<td>此著色器反映介面可提供變數的存取權。 <br/></td>
</tr>
</tbody>
</table>



 

## <a name="related-topics"></a>相關主題

<dl> <dt>

[Direct3D 12 參考](direct3d-12-reference.md)
</dt> <dt>

[著色器參考](d3d12-graphics-reference-shader-reference.md)
</dt> </dl>

 

 





