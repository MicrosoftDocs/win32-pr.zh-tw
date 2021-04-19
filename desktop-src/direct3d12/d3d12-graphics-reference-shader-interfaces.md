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
# <a name="shader-interfaces-direct3d-12-graphics"></a><span data-ttu-id="dd9f9-104"> (Direct3D 12 圖形) 的著色器介面</span><span class="sxs-lookup"><span data-stu-id="dd9f9-104">Shader Interfaces (Direct3D 12 Graphics)</span></span>

<span data-ttu-id="dd9f9-105">d3d12shader 會宣告下列介面。</span><span class="sxs-lookup"><span data-stu-id="dd9f9-105">d3d12shader.h declares the following interfaces.</span></span>

## <a name="in-this-section"></a><span data-ttu-id="dd9f9-106">本節內容</span><span class="sxs-lookup"><span data-stu-id="dd9f9-106">In this section</span></span>



<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<thead>
<tr class="header">
<th><span data-ttu-id="dd9f9-107">主題</span><span class="sxs-lookup"><span data-stu-id="dd9f9-107">Topic</span></span></th>
<th><span data-ttu-id="dd9f9-108">描述</span><span class="sxs-lookup"><span data-stu-id="dd9f9-108">Description</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><span data-ttu-id="dd9f9-109"><a href="/windows/desktop/api/d3d12shader/nn-d3d12shader-id3d12functionparameterreflection"><strong>ID3D12FunctionParameterReflection</strong></a></span><span class="sxs-lookup"><span data-stu-id="dd9f9-109"><a href="/windows/desktop/api/d3d12shader/nn-d3d12shader-id3d12functionparameterreflection"><strong>ID3D12FunctionParameterReflection</strong></a></span></span><br/></td>
<td><span data-ttu-id="dd9f9-110">函數參數反映介面會存取函式參數資訊。</span><span class="sxs-lookup"><span data-stu-id="dd9f9-110">A function-parameter-reflection interface accesses function-parameter info.</span></span> <br/>
<blockquote>
[!Note]<br />
<span data-ttu-id="dd9f9-111">此介面是 HLSL 著色器連結技術的一部分，可讓您在所有 Direct3D 12 平臺上用來建立先行編譯的 HLSL 函式、將它們封裝成程式庫，並在執行時間將它們連結到完整的著色器。</span><span class="sxs-lookup"><span data-stu-id="dd9f9-111">This interface is part of the HLSL shader linking technology that you can use on all Direct3D 12 platforms to create precompiled HLSL functions, package them into libraries, and link them into full shaders at run time.</span></span>
</blockquote>
<br/></td>
</tr>
<tr class="even">
<td><span data-ttu-id="dd9f9-112"><a href="/windows/desktop/api/d3d12shader/nn-d3d12shader-id3d12functionreflection"><strong>ID3D12FunctionReflection</strong></a></span><span class="sxs-lookup"><span data-stu-id="dd9f9-112"><a href="/windows/desktop/api/d3d12shader/nn-d3d12shader-id3d12functionreflection"><strong>ID3D12FunctionReflection</strong></a></span></span><br/></td>
<td><span data-ttu-id="dd9f9-113">函數反映介面會存取函式資訊。</span><span class="sxs-lookup"><span data-stu-id="dd9f9-113">A function-reflection interface accesses function info.</span></span> <br/>
<blockquote>
[!Note]<br />
<span data-ttu-id="dd9f9-114">此介面是 HLSL 著色器連結技術的一部分，可讓您在所有 Direct3D 12 平臺上用來建立先行編譯的 HLSL 函式、將它們封裝成程式庫，並在執行時間將它們連結到完整的著色器。</span><span class="sxs-lookup"><span data-stu-id="dd9f9-114">This interface is part of the HLSL shader linking technology that you can use on all Direct3D 12 platforms to create precompiled HLSL functions, package them into libraries, and link them into full shaders at run time.</span></span>
</blockquote>
<br/></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="dd9f9-115"><a href="/windows/desktop/api/d3d12shader/nn-d3d12shader-id3d12libraryreflection"><strong>ID3D12LibraryReflection</strong></a></span><span class="sxs-lookup"><span data-stu-id="dd9f9-115"><a href="/windows/desktop/api/d3d12shader/nn-d3d12shader-id3d12libraryreflection"><strong>ID3D12LibraryReflection</strong></a></span></span><br/></td>
<td><span data-ttu-id="dd9f9-116">程式庫反映介面會存取程式庫資訊。</span><span class="sxs-lookup"><span data-stu-id="dd9f9-116">A library-reflection interface accesses library info.</span></span> <br/>
<blockquote>
[!Note]<br />
<span data-ttu-id="dd9f9-117">此介面是 HLSL 著色器連結技術的一部分，可讓您在所有 Direct3D 12 平臺上用來建立先行編譯的 HLSL 函式、將它們封裝成程式庫，並在執行時間將它們連結到完整的著色器。</span><span class="sxs-lookup"><span data-stu-id="dd9f9-117">This interface is part of the HLSL shader linking technology that you can use on all Direct3D 12 platforms to create precompiled HLSL functions, package them into libraries, and link them into full shaders at run time.</span></span>
</blockquote>
<br/></td>
</tr>
<tr class="even">
<td><span data-ttu-id="dd9f9-118"><a href="/windows/desktop/api/d3d12shader/nn-d3d12shader-id3d12shaderreflection"><strong>ID3D12ShaderReflection</strong></a></span><span class="sxs-lookup"><span data-stu-id="dd9f9-118"><a href="/windows/desktop/api/d3d12shader/nn-d3d12shader-id3d12shaderreflection"><strong>ID3D12ShaderReflection</strong></a></span></span><br/></td>
<td><span data-ttu-id="dd9f9-119">著色器反映介面會存取著色器資訊。</span><span class="sxs-lookup"><span data-stu-id="dd9f9-119">A shader-reflection interface accesses shader information.</span></span> <br/></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="dd9f9-120"><a href="/windows/desktop/api/d3d12shader/nn-d3d12shader-id3d12shaderreflectionconstantbuffer"><strong>ID3D12ShaderReflectionConstantBuffer</strong></a></span><span class="sxs-lookup"><span data-stu-id="dd9f9-120"><a href="/windows/desktop/api/d3d12shader/nn-d3d12shader-id3d12shaderreflectionconstantbuffer"><strong>ID3D12ShaderReflectionConstantBuffer</strong></a></span></span><br/></td>
<td><span data-ttu-id="dd9f9-121">此著色器反映介面可提供常數緩衝區的存取權。</span><span class="sxs-lookup"><span data-stu-id="dd9f9-121">This shader-reflection interface provides access to a constant buffer.</span></span> <br/></td>
</tr>
<tr class="even">
<td><span data-ttu-id="dd9f9-122"><a href="/windows/desktop/api/d3d12shader/nn-d3d12shader-id3d12shaderreflectiontype"><strong>ID3D12ShaderReflectionType</strong></a></span><span class="sxs-lookup"><span data-stu-id="dd9f9-122"><a href="/windows/desktop/api/d3d12shader/nn-d3d12shader-id3d12shaderreflectiontype"><strong>ID3D12ShaderReflectionType</strong></a></span></span><br/></td>
<td><span data-ttu-id="dd9f9-123">此著色器反映介面可提供變數類型的存取。</span><span class="sxs-lookup"><span data-stu-id="dd9f9-123">This shader-reflection interface provides access to variable type.</span></span> <br/></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="dd9f9-124"><a href="/windows/desktop/api/d3d12shader/nn-d3d12shader-id3d12shaderreflectionvariable"><strong>ID3D12ShaderReflectionVariable</strong></a></span><span class="sxs-lookup"><span data-stu-id="dd9f9-124"><a href="/windows/desktop/api/d3d12shader/nn-d3d12shader-id3d12shaderreflectionvariable"><strong>ID3D12ShaderReflectionVariable</strong></a></span></span><br/></td>
<td><span data-ttu-id="dd9f9-125">此著色器反映介面可提供變數的存取權。</span><span class="sxs-lookup"><span data-stu-id="dd9f9-125">This shader-reflection interface provides access to a variable.</span></span> <br/></td>
</tr>
</tbody>
</table>



 

## <a name="related-topics"></a><span data-ttu-id="dd9f9-126">相關主題</span><span class="sxs-lookup"><span data-stu-id="dd9f9-126">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="dd9f9-127">Direct3D 12 參考</span><span class="sxs-lookup"><span data-stu-id="dd9f9-127">Direct3D 12 Reference</span></span>](direct3d-12-reference.md)
</dt> <dt>

[<span data-ttu-id="dd9f9-128">著色器參考</span><span class="sxs-lookup"><span data-stu-id="dd9f9-128">Shader Reference</span></span>](d3d12-graphics-reference-shader-reference.md)
</dt> </dl>

 

 





