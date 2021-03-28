---
title: 'D3DX 函式 (Direct3D 11 圖形) '
description: 本節包含 D3DX 11 函數的相關資訊。
ms.assetid: 7548c02e-c8c2-4629-95ac-d21ca7a39f0a
keywords:
- 函數，DirectX 11 D3DX
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 2b76c1764f464461b4800a9161ac37dcff8c539a
ms.sourcegitcommit: 8fa6614b715bddf14648cce36d2df22e5232801a
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 12/10/2020
ms.locfileid: "104383534"
---
# <a name="d3dx-functions-direct3d-11-graphics"></a><span data-ttu-id="89f0b-104">D3DX 函式 (Direct3D 11 圖形) </span><span class="sxs-lookup"><span data-stu-id="89f0b-104">D3DX Functions (Direct3D 11 Graphics)</span></span>

<span data-ttu-id="89f0b-105">本節包含 D3DX 11 函數的相關資訊。</span><span class="sxs-lookup"><span data-stu-id="89f0b-105">This section contains information about the D3DX 11 functions.</span></span>

> [!Note]  
> <span data-ttu-id="89f0b-106">D3DX (D3DX 9、D3DX 10 和 D3DX 11) 公用程式庫已針對 Windows 8 淘汰，而且不支援 Windows Store 應用程式。</span><span class="sxs-lookup"><span data-stu-id="89f0b-106">The D3DX (D3DX 9, D3DX 10, and D3DX 11) utility library is deprecated for Windows 8 and is not supported for Windows Store apps.</span></span>

 


## <a name="in-this-section"></a><span data-ttu-id="89f0b-107">本節內容</span><span class="sxs-lookup"><span data-stu-id="89f0b-107">In this section</span></span>



<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<thead>
<tr class="header">
<th><span data-ttu-id="89f0b-108">主題</span><span class="sxs-lookup"><span data-stu-id="89f0b-108">Topic</span></span></th>
<th><span data-ttu-id="89f0b-109">描述</span><span class="sxs-lookup"><span data-stu-id="89f0b-109">Description</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><span data-ttu-id="89f0b-110"><a href="d3dx11compilefromfile.md"><strong>D3DX11CompileFromFile</strong></a></span><span class="sxs-lookup"><span data-stu-id="89f0b-110"><a href="d3dx11compilefromfile.md"><strong>D3DX11CompileFromFile</strong></a></span></span><br/></td>
<td><blockquote>
[!Note]<br />
<span data-ttu-id="89f0b-111">D3DX (D3DX 9、D3DX 10 和 D3DX 11) 公用程式庫已針對 Windows 8 淘汰，而且不支援 Windows Store 應用程式。</span><span class="sxs-lookup"><span data-stu-id="89f0b-111">The D3DX (D3DX 9, D3DX 10, and D3DX 11) utility library is deprecated for Windows 8 and is not supported for Windows Store apps.</span></span>
</blockquote>
<br/>
<blockquote>
[!Note]<br />
<span data-ttu-id="89f0b-112">我們建議您不要使用這個函式，而是使用 Fxc.exe 命令列編譯器，或使用其中一個 HLSL 編譯 Api （例如 <a href="/windows/desktop/direct3dhlsl/d3dcompilefromfile"><strong>D3DCompileFromFile</strong></a> API），以離線方式編譯。</span><span class="sxs-lookup"><span data-stu-id="89f0b-112">Instead of using this function, we recommend that you compile offline by using the Fxc.exe command-line compiler or use one of the HLSL compile APIs, like the <a href="/windows/desktop/direct3dhlsl/d3dcompilefromfile"><strong>D3DCompileFromFile</strong></a> API.</span></span>
</blockquote>
<br/> <span data-ttu-id="89f0b-113">從檔案編譯著色器或效果。</span><span class="sxs-lookup"><span data-stu-id="89f0b-113">Compile a shader or an effect from a file.</span></span><br/></td>
</tr>
<tr class="even">
<td><span data-ttu-id="89f0b-114"><a href="d3dx11compilefrommemory.md"><strong>D3DX11CompileFromMemory</strong></a></span><span class="sxs-lookup"><span data-stu-id="89f0b-114"><a href="d3dx11compilefrommemory.md"><strong>D3DX11CompileFromMemory</strong></a></span></span><br/></td>
<td><blockquote>
[!Note]<br />
<span data-ttu-id="89f0b-115">D3DX (D3DX 9、D3DX 10 和 D3DX 11) 公用程式庫已針對 Windows 8 淘汰，而且不支援 Windows Store 應用程式。</span><span class="sxs-lookup"><span data-stu-id="89f0b-115">The D3DX (D3DX 9, D3DX 10, and D3DX 11) utility library is deprecated for Windows 8 and is not supported for Windows Store apps.</span></span>
</blockquote>
<br/>
<blockquote>
[!Note]<br />
<span data-ttu-id="89f0b-116">我們建議您不要使用這個函式，而是使用 Fxc.exe 命令列編譯器，或使用其中一個 HLSL 編譯 Api （例如 <a href="/windows/desktop/direct3dhlsl/d3dcompile"><strong>D3DCompile</strong></a> API），以離線方式編譯。</span><span class="sxs-lookup"><span data-stu-id="89f0b-116">Instead of using this function, we recommend that you compile offline by using the Fxc.exe command-line compiler or use one of the HLSL compile APIs, like the <a href="/windows/desktop/direct3dhlsl/d3dcompile"><strong>D3DCompile</strong></a> API.</span></span>
</blockquote>
<br/> <span data-ttu-id="89f0b-117">編譯已載入記憶體中的著色器或效果。</span><span class="sxs-lookup"><span data-stu-id="89f0b-117">Compile a shader or an effect that is loaded in memory.</span></span><br/></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="89f0b-118"><a href="d3dx11compilefromresource.md"><strong>D3DX11CompileFromResource</strong></a></span><span class="sxs-lookup"><span data-stu-id="89f0b-118"><a href="d3dx11compilefromresource.md"><strong>D3DX11CompileFromResource</strong></a></span></span><br/></td>
<td><blockquote>
[!Note]<br />
<span data-ttu-id="89f0b-119">D3DX (D3DX 9、D3DX 10 和 D3DX 11) 公用程式庫已針對 Windows 8 淘汰，而且不支援 Windows Store 應用程式。</span><span class="sxs-lookup"><span data-stu-id="89f0b-119">The D3DX (D3DX 9, D3DX 10, and D3DX 11) utility library is deprecated for Windows 8 and is not supported for Windows Store apps.</span></span>
</blockquote>
<br/>
<blockquote>
[!Note]<br />
<span data-ttu-id="89f0b-120">我們建議您不要使用此函式，而是使用 <a href="/windows/desktop/menurc/resources-functions">資源</a>函式，然後使用 Fxc.exe 命令列編譯器或使用其中一個 HLSL 編譯 api （例如 <a href="/windows/desktop/direct3dhlsl/d3dcompile"><strong>D3DCompile</strong></a> API），以離線方式編譯。</span><span class="sxs-lookup"><span data-stu-id="89f0b-120">Instead of using this function, we recommend that you use <a href="/windows/desktop/menurc/resources-functions">resource functions</a>, then compile offline by using the Fxc.exe command-line compiler or use one of the HLSL compile APIs, like the <a href="/windows/desktop/direct3dhlsl/d3dcompile"><strong>D3DCompile</strong></a> API.</span></span>
</blockquote>
<br/> <span data-ttu-id="89f0b-121">從資源編譯著色器或效果。</span><span class="sxs-lookup"><span data-stu-id="89f0b-121">Compile a shader or an effect from a resource.</span></span><br/></td>
</tr>
<tr class="even">
<td><span data-ttu-id="89f0b-122"><a href="d3dx11computenormalmap.md"><strong>D3DX11ComputeNormalMap</strong></a></span><span class="sxs-lookup"><span data-stu-id="89f0b-122"><a href="d3dx11computenormalmap.md"><strong>D3DX11ComputeNormalMap</strong></a></span></span><br/></td>
<td><blockquote>
[!Note]<br />
<span data-ttu-id="89f0b-123">D3DX (D3DX 9、D3DX 10 和 D3DX 11) 公用程式庫已針對 Windows 8 淘汰，而且不支援 Windows Store 應用程式。</span><span class="sxs-lookup"><span data-stu-id="89f0b-123">The D3DX (D3DX 9, D3DX 10, and D3DX 11) utility library is deprecated for Windows 8 and is not supported for Windows Store apps.</span></span>
</blockquote>
<br/>
<blockquote>
[!Note]<br />
<span data-ttu-id="89f0b-124">我們建議您不要使用此函式，而是使用 <a href="https://github.com/Microsoft/DirectXTex">DirectXTex</a> 程式庫 <strong>ComputeNormalMap</strong>。</span><span class="sxs-lookup"><span data-stu-id="89f0b-124">Instead of using this function, we recommend that you use the <a href="https://github.com/Microsoft/DirectXTex">DirectXTex</a> library, <strong>ComputeNormalMap</strong>.</span></span>
</blockquote>
<br/> <span data-ttu-id="89f0b-125">將高度地圖轉換成一般地圖。</span><span class="sxs-lookup"><span data-stu-id="89f0b-125">Converts a height map into a normal map.</span></span> <span data-ttu-id="89f0b-126">每個標準的 (x、y、z) 元件都會對應到輸出材質 (r、g、b) 通道。</span><span class="sxs-lookup"><span data-stu-id="89f0b-126">The (x,y,z) components of each normal are mapped to the (r,g,b) channels of the output texture.</span></span><br/></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="89f0b-127"><a href="d3dx11createasynccompilerprocessor.md"><strong>D3DX11CreateAsyncCompilerProcessor</strong></a></span><span class="sxs-lookup"><span data-stu-id="89f0b-127"><a href="d3dx11createasynccompilerprocessor.md"><strong>D3DX11CreateAsyncCompilerProcessor</strong></a></span></span><br/></td>
<td><blockquote>
[!Note]<br />
<span data-ttu-id="89f0b-128">D3DX (D3DX 9、D3DX 10 和 D3DX 11) 公用程式庫已針對 Windows 8 淘汰，而且不支援 Windows Store 應用程式。</span><span class="sxs-lookup"><span data-stu-id="89f0b-128">The D3DX (D3DX 9, D3DX 10, and D3DX 11) utility library is deprecated for Windows 8 and is not supported for Windows Store apps.</span></span> <span data-ttu-id="89f0b-129">請參閱＜備註＞。</span><span class="sxs-lookup"><span data-stu-id="89f0b-129">See Remarks.</span></span>
</blockquote>
<br/> <span data-ttu-id="89f0b-130">建立著色器的非同步資料處理器。</span><span class="sxs-lookup"><span data-stu-id="89f0b-130">Create an asynchronous-data processor for a shader.</span></span><br/></td>
</tr>
<tr class="even">
<td><span data-ttu-id="89f0b-131"><a href="d3dx11createasyncfileloader.md"><strong>D3DX11CreateAsyncFileLoader</strong></a></span><span class="sxs-lookup"><span data-stu-id="89f0b-131"><a href="d3dx11createasyncfileloader.md"><strong>D3DX11CreateAsyncFileLoader</strong></a></span></span><br/></td>
<td><blockquote>
[!Note]<br />
<span data-ttu-id="89f0b-132">D3DX (D3DX 9、D3DX 10 和 D3DX 11) 公用程式庫已針對 Windows 8 淘汰，而且不支援 Windows Store 應用程式。</span><span class="sxs-lookup"><span data-stu-id="89f0b-132">The D3DX (D3DX 9, D3DX 10, and D3DX 11) utility library is deprecated for Windows 8 and is not supported for Windows Store apps.</span></span> <span data-ttu-id="89f0b-133">請參閱＜備註＞。</span><span class="sxs-lookup"><span data-stu-id="89f0b-133">See Remarks.</span></span>
</blockquote>
<br/> <span data-ttu-id="89f0b-134">建立異步檔案載入器。</span><span class="sxs-lookup"><span data-stu-id="89f0b-134">Create an asynchronous-file loader.</span></span><br/></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="89f0b-135"><a href="d3dx11createasyncmemoryloader.md"><strong>D3DX11CreateAsyncMemoryLoader</strong></a></span><span class="sxs-lookup"><span data-stu-id="89f0b-135"><a href="d3dx11createasyncmemoryloader.md"><strong>D3DX11CreateAsyncMemoryLoader</strong></a></span></span><br/></td>
<td><blockquote>
[!Note]<br />
<span data-ttu-id="89f0b-136">D3DX (D3DX 9、D3DX 10 和 D3DX 11) 公用程式庫已針對 Windows 8 淘汰，而且不支援 Windows Store 應用程式。</span><span class="sxs-lookup"><span data-stu-id="89f0b-136">The D3DX (D3DX 9, D3DX 10, and D3DX 11) utility library is deprecated for Windows 8 and is not supported for Windows Store apps.</span></span> <span data-ttu-id="89f0b-137">請參閱＜備註＞。</span><span class="sxs-lookup"><span data-stu-id="89f0b-137">See Remarks.</span></span>
</blockquote>
<br/> <span data-ttu-id="89f0b-138">建立異步記憶體載入器。</span><span class="sxs-lookup"><span data-stu-id="89f0b-138">Create an asynchronous-memory loader.</span></span><br/></td>
</tr>
<tr class="even">
<td><span data-ttu-id="89f0b-139"><a href="d3dx11createasyncresourceloader.md"><strong>D3DX11CreateAsyncResourceLoader</strong></a></span><span class="sxs-lookup"><span data-stu-id="89f0b-139"><a href="d3dx11createasyncresourceloader.md"><strong>D3DX11CreateAsyncResourceLoader</strong></a></span></span><br/></td>
<td><blockquote>
[!Note]<br />
<span data-ttu-id="89f0b-140">D3DX (D3DX 9、D3DX 10 和 D3DX 11) 公用程式庫已針對 Windows 8 淘汰，而且不支援 Windows Store 應用程式。</span><span class="sxs-lookup"><span data-stu-id="89f0b-140">The D3DX (D3DX 9, D3DX 10, and D3DX 11) utility library is deprecated for Windows 8 and is not supported for Windows Store apps.</span></span> <span data-ttu-id="89f0b-141">請參閱＜備註＞。</span><span class="sxs-lookup"><span data-stu-id="89f0b-141">See Remarks.</span></span>
</blockquote>
<br/> <span data-ttu-id="89f0b-142">建立異步資源載入器。</span><span class="sxs-lookup"><span data-stu-id="89f0b-142">Create an asynchronous-resource loader.</span></span><br/></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="89f0b-143"><a href="d3dx11createasyncshaderpreprocessprocessor.md"><strong>D3DX11CreateAsyncShaderPreprocessProcessor</strong></a></span><span class="sxs-lookup"><span data-stu-id="89f0b-143"><a href="d3dx11createasyncshaderpreprocessprocessor.md"><strong>D3DX11CreateAsyncShaderPreprocessProcessor</strong></a></span></span><br/></td>
<td><blockquote>
[!Note]<br />
<span data-ttu-id="89f0b-144">D3DX (D3DX 9、D3DX 10 和 D3DX 11) 公用程式庫已針對 Windows 8 淘汰，而且不支援 Windows Store 應用程式。</span><span class="sxs-lookup"><span data-stu-id="89f0b-144">The D3DX (D3DX 9, D3DX 10, and D3DX 11) utility library is deprecated for Windows 8 and is not supported for Windows Store apps.</span></span> <span data-ttu-id="89f0b-145">請參閱＜備註＞。</span><span class="sxs-lookup"><span data-stu-id="89f0b-145">See Remarks.</span></span>
</blockquote>
<br/> <span data-ttu-id="89f0b-146">以非同步方式建立著色器的資料處理器。</span><span class="sxs-lookup"><span data-stu-id="89f0b-146">Create a data processor for a shader asynchronously.</span></span><br/></td>
</tr>
<tr class="even">
<td><span data-ttu-id="89f0b-147"><a href="d3dx11createasynctextureinfoprocessor.md"><strong>D3DX11CreateAsyncTextureInfoProcessor</strong></a></span><span class="sxs-lookup"><span data-stu-id="89f0b-147"><a href="d3dx11createasynctextureinfoprocessor.md"><strong>D3DX11CreateAsyncTextureInfoProcessor</strong></a></span></span><br/></td>
<td><blockquote>
[!Note]<br />
<span data-ttu-id="89f0b-148">D3DX (D3DX 9、D3DX 10 和 D3DX 11) 公用程式庫已針對 Windows 8 淘汰，而且不支援 Windows Store 應用程式。</span><span class="sxs-lookup"><span data-stu-id="89f0b-148">The D3DX (D3DX 9, D3DX 10, and D3DX 11) utility library is deprecated for Windows 8 and is not supported for Windows Store apps.</span></span> <span data-ttu-id="89f0b-149">請參閱＜備註＞。</span><span class="sxs-lookup"><span data-stu-id="89f0b-149">See Remarks.</span></span>
</blockquote>
<br/> <span data-ttu-id="89f0b-150">建立要搭配 <a href="id3dx11threadpump.md"><strong>執行緒抽取</strong></a>使用的資料處理器。</span><span class="sxs-lookup"><span data-stu-id="89f0b-150">Create a data processor to be used with a <a href="id3dx11threadpump.md"><strong>thread pump</strong></a>.</span></span><br/></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="89f0b-151"><a href="d3dx11createasynctextureprocessor.md"><strong>D3DX11CreateAsyncTextureProcessor</strong></a></span><span class="sxs-lookup"><span data-stu-id="89f0b-151"><a href="d3dx11createasynctextureprocessor.md"><strong>D3DX11CreateAsyncTextureProcessor</strong></a></span></span><br/></td>
<td><blockquote>
[!Note]<br />
<span data-ttu-id="89f0b-152">D3DX (D3DX 9、D3DX 10 和 D3DX 11) 公用程式庫已針對 Windows 8 淘汰，而且不支援 Windows Store 應用程式。</span><span class="sxs-lookup"><span data-stu-id="89f0b-152">The D3DX (D3DX 9, D3DX 10, and D3DX 11) utility library is deprecated for Windows 8 and is not supported for Windows Store apps.</span></span> <span data-ttu-id="89f0b-153">請參閱＜備註＞。</span><span class="sxs-lookup"><span data-stu-id="89f0b-153">See Remarks.</span></span>
</blockquote>
<br/> <span data-ttu-id="89f0b-154">建立要搭配 <a href="id3dx11threadpump.md"><strong>執行緒抽取</strong></a>使用的資料處理器。</span><span class="sxs-lookup"><span data-stu-id="89f0b-154">Create a data processor to be used with a <a href="id3dx11threadpump.md"><strong>thread pump</strong></a>.</span></span><br/></td>
</tr>
<tr class="even">
<td><span data-ttu-id="89f0b-155"><a href="d3dx11createasyncshaderresourceviewprocessor.md"><strong>D3DX11CreateAsyncShaderResourceViewProcessor</strong></a></span><span class="sxs-lookup"><span data-stu-id="89f0b-155"><a href="d3dx11createasyncshaderresourceviewprocessor.md"><strong>D3DX11CreateAsyncShaderResourceViewProcessor</strong></a></span></span><br/></td>
<td><blockquote>
[!Note]<br />
<span data-ttu-id="89f0b-156">D3DX (D3DX 9、D3DX 10 和 D3DX 11) 公用程式庫已針對 Windows 8 淘汰，而且不支援 Windows Store 應用程式。</span><span class="sxs-lookup"><span data-stu-id="89f0b-156">The D3DX (D3DX 9, D3DX 10, and D3DX 11) utility library is deprecated for Windows 8 and is not supported for Windows Store apps.</span></span> <span data-ttu-id="89f0b-157">請參閱＜備註＞。</span><span class="sxs-lookup"><span data-stu-id="89f0b-157">See Remarks.</span></span>
</blockquote>
<br/> <span data-ttu-id="89f0b-158">建立會載入資源的資料處理器，然後為其建立著色器資源檢視。</span><span class="sxs-lookup"><span data-stu-id="89f0b-158">Create a data processor that will load a resource and then create a shader-resource view for it.</span></span> <span data-ttu-id="89f0b-159">資料處理器是 D3DX11 中使用 <a href="id3dx11threadpump.md"><strong>執行緒抽取</strong></a>的非同步資料載入功能的元件。</span><span class="sxs-lookup"><span data-stu-id="89f0b-159">Data processors are a component of the asynchronous data loading feature in D3DX11 that uses <a href="id3dx11threadpump.md"><strong>thread pumps</strong></a>.</span></span><br/></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="89f0b-160"><a href="d3dx11createshaderresourceviewfromfile.md"><strong>D3DX11CreateShaderResourceViewFromFile</strong></a></span><span class="sxs-lookup"><span data-stu-id="89f0b-160"><a href="d3dx11createshaderresourceviewfromfile.md"><strong>D3DX11CreateShaderResourceViewFromFile</strong></a></span></span><br/></td>
<td><blockquote>
[!Note]<br />
<span data-ttu-id="89f0b-161">D3DX (D3DX 9、D3DX 10 和 D3DX 11) 公用程式庫已針對 Windows 8 淘汰，而且不支援 Windows Store 應用程式。</span><span class="sxs-lookup"><span data-stu-id="89f0b-161">The D3DX (D3DX 9, D3DX 10, and D3DX 11) utility library is deprecated for Windows 8 and is not supported for Windows Store apps.</span></span>
</blockquote>
<br/>
<blockquote>
<p>[!Note]<br />
<span data-ttu-id="89f0b-162">我們建議您不要使用這個函式，而是使用下列功能：</span><span class="sxs-lookup"><span data-stu-id="89f0b-162">Instead of using this function, we recommend that you use these:</span></span></p>
<ul>
<li><span data-ttu-id="89f0b-163"><a href="https://github.com/Microsoft/DirectXTK">DirectXTK</a> 程式庫 (runtime) 、 <strong>CreateXXXTextureFromFile</strong> (，其中 XXX 是 DDS 或 WIC) </span><span class="sxs-lookup"><span data-stu-id="89f0b-163"><a href="https://github.com/Microsoft/DirectXTK">DirectXTK</a> library (runtime), <strong>CreateXXXTextureFromFile</strong> (where XXX is DDS or WIC)</span></span></li>
<li><span data-ttu-id="89f0b-164"><a href="https://github.com/Microsoft/DirectXTex">DirectXTex</a> 程式庫 (工具) 、 <strong>LOADFROMXXXFILE</strong> (其中 XXX 是 WIC、DDS 或 TGA;WIC 不支援 DDS 和 TGA;D3DX 9 支援的 TGA 做為遊戲的常用藝術來源格式) 然後 <strong>CreateShaderResourceView</strong></span><span class="sxs-lookup"><span data-stu-id="89f0b-164"><a href="https://github.com/Microsoft/DirectXTex">DirectXTex</a> library (tools), <strong>LoadFromXXXFile</strong> (where XXX is WIC, DDS, or TGA; WIC doesn't support DDS and TGA; D3DX 9 supported TGA as a common art source format for games) then <strong>CreateShaderResourceView</strong></span></span></li>
</ul>
</blockquote>
<br/> <span data-ttu-id="89f0b-165">從檔案建立著色器資源檢視。</span><span class="sxs-lookup"><span data-stu-id="89f0b-165">Create a shader-resource view from a file.</span></span><br/></td>
</tr>
<tr class="even">
<td><span data-ttu-id="89f0b-166"><a href="d3dx11createshaderresourceviewfrommemory.md"><strong>D3DX11CreateShaderResourceViewFromMemory</strong></a></span><span class="sxs-lookup"><span data-stu-id="89f0b-166"><a href="d3dx11createshaderresourceviewfrommemory.md"><strong>D3DX11CreateShaderResourceViewFromMemory</strong></a></span></span><br/></td>
<td><blockquote>
[!Note]<br />
<span data-ttu-id="89f0b-167">D3DX (D3DX 9、D3DX 10 和 D3DX 11) 公用程式庫已針對 Windows 8 淘汰，而且不支援 Windows Store 應用程式。</span><span class="sxs-lookup"><span data-stu-id="89f0b-167">The D3DX (D3DX 9, D3DX 10, and D3DX 11) utility library is deprecated for Windows 8 and is not supported for Windows Store apps.</span></span>
</blockquote>
<br/>
<blockquote>
<p>[!Note]<br />
<span data-ttu-id="89f0b-168">我們建議您不要使用這個函式，而是使用下列功能：</span><span class="sxs-lookup"><span data-stu-id="89f0b-168">Instead of using this function, we recommend that you use these:</span></span></p>
<ul>
<li><span data-ttu-id="89f0b-169"><a href="https://github.com/Microsoft/DirectXTK">DirectXTK</a> 程式庫 (runtime) 、 <strong>CreateXXXTextureFromMemory</strong> (，其中 XXX 是 DDS 或 WIC) </span><span class="sxs-lookup"><span data-stu-id="89f0b-169"><a href="https://github.com/Microsoft/DirectXTK">DirectXTK</a> library (runtime), <strong>CreateXXXTextureFromMemory</strong> (where XXX is DDS or WIC)</span></span></li>
<li><span data-ttu-id="89f0b-170"><a href="https://github.com/Microsoft/DirectXTex">DirectXTex</a> 程式庫 (工具) 、 <strong>LOADFROMXXXMEMORY</strong> (其中 XXX 是 WIC、DDS 或 TGA;WIC 不支援 DDS 和 TGA;D3DX 9 支援的 TGA 做為遊戲的常用藝術來源格式) 然後 <strong>CreateShaderResourceView</strong></span><span class="sxs-lookup"><span data-stu-id="89f0b-170"><a href="https://github.com/Microsoft/DirectXTex">DirectXTex</a> library (tools), <strong>LoadFromXXXMemory</strong> (where XXX is WIC, DDS, or TGA; WIC doesn't support DDS and TGA; D3DX 9 supported TGA as a common art source format for games) then <strong>CreateShaderResourceView</strong></span></span></li>
</ul>
</blockquote>
<br/> <span data-ttu-id="89f0b-171">從記憶體中的檔案建立著色器資源檢視。</span><span class="sxs-lookup"><span data-stu-id="89f0b-171">Create a shader-resource view from a file in memory.</span></span><br/></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="89f0b-172"><a href="d3dx11createshaderresourceviewfromresource.md"><strong>D3DX11CreateShaderResourceViewFromResource</strong></a></span><span class="sxs-lookup"><span data-stu-id="89f0b-172"><a href="d3dx11createshaderresourceviewfromresource.md"><strong>D3DX11CreateShaderResourceViewFromResource</strong></a></span></span><br/></td>
<td><blockquote>
[!Note]<br />
<span data-ttu-id="89f0b-173">D3DX (D3DX 9、D3DX 10 和 D3DX 11) 公用程式庫已針對 Windows 8 淘汰，而且不支援 Windows Store 應用程式。</span><span class="sxs-lookup"><span data-stu-id="89f0b-173">The D3DX (D3DX 9, D3DX 10, and D3DX 11) utility library is deprecated for Windows 8 and is not supported for Windows Store apps.</span></span>
</blockquote>
<br/>
<blockquote>
<p>[!Note]<br />
<span data-ttu-id="89f0b-174">我們建議您不要使用此函式，而是使用 <a href="/windows/desktop/menurc/resources-functions">資源</a>函式，如下所示：</span><span class="sxs-lookup"><span data-stu-id="89f0b-174">Instead of using this function, we recommend that you use <a href="/windows/desktop/menurc/resources-functions">resource functions</a>, then these:</span></span></p>
<ul>
<li><span data-ttu-id="89f0b-175"><a href="https://github.com/Microsoft/DirectXTK">DirectXTK</a> 程式庫 (runtime) 、 <strong>CreateXXXTextureFromMemory</strong> (，其中 XXX 是 DDS 或 WIC) </span><span class="sxs-lookup"><span data-stu-id="89f0b-175"><a href="https://github.com/Microsoft/DirectXTK">DirectXTK</a> library (runtime), <strong>CreateXXXTextureFromMemory</strong> (where XXX is DDS or WIC)</span></span></li>
<li><span data-ttu-id="89f0b-176"><a href="https://github.com/Microsoft/DirectXTex">DirectXTex</a> 程式庫 (工具) 、 <strong>LOADFROMXXXMEMORY</strong> (其中 XXX 是 WIC、DDS 或 TGA;WIC 不支援 DDS 和 TGA;D3DX 9 支援的 TGA 做為遊戲的常用藝術來源格式) 然後 <strong>CreateShaderResourceView</strong></span><span class="sxs-lookup"><span data-stu-id="89f0b-176"><a href="https://github.com/Microsoft/DirectXTex">DirectXTex</a> library (tools), <strong>LoadFromXXXMemory</strong> (where XXX is WIC, DDS, or TGA; WIC doesn't support DDS and TGA; D3DX 9 supported TGA as a common art source format for games) then <strong>CreateShaderResourceView</strong></span></span></li>
</ul>
</blockquote>
<br/> <span data-ttu-id="89f0b-177">從資源建立著色器資源檢視。</span><span class="sxs-lookup"><span data-stu-id="89f0b-177">Create a shader-resource view from a resource.</span></span><br/></td>
</tr>
<tr class="even">
<td><span data-ttu-id="89f0b-178"><a href="d3dx11createtexturefromfile.md"><strong>D3DX11CreateTextureFromFile</strong></a></span><span class="sxs-lookup"><span data-stu-id="89f0b-178"><a href="d3dx11createtexturefromfile.md"><strong>D3DX11CreateTextureFromFile</strong></a></span></span><br/></td>
<td><blockquote>
[!Note]<br />
<span data-ttu-id="89f0b-179">D3DX (D3DX 9、D3DX 10 和 D3DX 11) 公用程式庫已針對 Windows 8 淘汰，而且不支援 Windows Store 應用程式。</span><span class="sxs-lookup"><span data-stu-id="89f0b-179">The D3DX (D3DX 9, D3DX 10, and D3DX 11) utility library is deprecated for Windows 8 and is not supported for Windows Store apps.</span></span>
</blockquote>
<br/>
<blockquote>
<p>[!Note]<br />
<span data-ttu-id="89f0b-180">我們建議您不要使用這個函式，而是使用下列功能：</span><span class="sxs-lookup"><span data-stu-id="89f0b-180">Instead of using this function, we recommend that you use these:</span></span></p>
<ul>
<li><span data-ttu-id="89f0b-181"><a href="https://github.com/Microsoft/DirectXTK">DirectXTK</a> 程式庫 (runtime) 、 <strong>CreateXXXTextureFromFile</strong> (，其中 XXX 是 DDS 或 WIC) </span><span class="sxs-lookup"><span data-stu-id="89f0b-181"><a href="https://github.com/Microsoft/DirectXTK">DirectXTK</a> library (runtime), <strong>CreateXXXTextureFromFile</strong> (where XXX is DDS or WIC)</span></span></li>
<li><span data-ttu-id="89f0b-182"><a href="https://github.com/Microsoft/DirectXTex">DirectXTex</a> 程式庫 (工具) 、 <strong>LOADFROMXXXFILE</strong> (其中 XXX 是 WIC、DDS 或 TGA;WIC 不支援 DDS 和 TGA;D3DX 9 支援的 TGA 做為遊戲的常用藝術來源格式) 然後 <strong>CreateTexture</strong></span><span class="sxs-lookup"><span data-stu-id="89f0b-182"><a href="https://github.com/Microsoft/DirectXTex">DirectXTex</a> library (tools), <strong>LoadFromXXXFile</strong> (where XXX is WIC, DDS, or TGA; WIC doesn't support DDS and TGA; D3DX 9 supported TGA as a common art source format for games) then <strong>CreateTexture</strong></span></span></li>
</ul>
</blockquote>
<br/> <span data-ttu-id="89f0b-183">從檔案建立材質資源。</span><span class="sxs-lookup"><span data-stu-id="89f0b-183">Create a texture resource from a file.</span></span><br/></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="89f0b-184"><a href="d3dx11createtexturefrommemory.md"><strong>D3DX11CreateTextureFromMemory</strong></a></span><span class="sxs-lookup"><span data-stu-id="89f0b-184"><a href="d3dx11createtexturefrommemory.md"><strong>D3DX11CreateTextureFromMemory</strong></a></span></span><br/></td>
<td><blockquote>
[!Note]<br />
<span data-ttu-id="89f0b-185">D3DX (D3DX 9、D3DX 10 和 D3DX 11) 公用程式庫已針對 Windows 8 淘汰，而且不支援 Windows Store 應用程式。</span><span class="sxs-lookup"><span data-stu-id="89f0b-185">The D3DX (D3DX 9, D3DX 10, and D3DX 11) utility library is deprecated for Windows 8 and is not supported for Windows Store apps.</span></span>
</blockquote>
<br/>
<blockquote>
<p>[!Note]<br />
<span data-ttu-id="89f0b-186">我們建議您不要使用這個函式，而是使用下列功能：</span><span class="sxs-lookup"><span data-stu-id="89f0b-186">Instead of using this function, we recommend that you use these:</span></span></p>
<ul>
<li><span data-ttu-id="89f0b-187"><a href="https://github.com/Microsoft/DirectXTK">DirectXTK</a> 程式庫 (runtime) 、 <strong>CreateXXXTextureFromMemory</strong> (，其中 XXX 是 DDS 或 WIC) </span><span class="sxs-lookup"><span data-stu-id="89f0b-187"><a href="https://github.com/Microsoft/DirectXTK">DirectXTK</a> library (runtime), <strong>CreateXXXTextureFromMemory</strong> (where XXX is DDS or WIC)</span></span></li>
<li><span data-ttu-id="89f0b-188"><a href="https://github.com/Microsoft/DirectXTex">DirectXTex</a> 程式庫 (工具) 、 <strong>LOADFROMXXXMEMORY</strong> (其中 XXX 是 WIC、DDS 或 TGA;WIC 不支援 DDS 和 TGA;D3DX 9 支援的 TGA 做為遊戲的常用藝術來源格式) 然後 <strong>CreateTexture</strong></span><span class="sxs-lookup"><span data-stu-id="89f0b-188"><a href="https://github.com/Microsoft/DirectXTex">DirectXTex</a> library (tools), <strong>LoadFromXXXMemory</strong> (where XXX is WIC, DDS, or TGA; WIC doesn't support DDS and TGA; D3DX 9 supported TGA as a common art source format for games) then <strong>CreateTexture</strong></span></span></li>
</ul>
</blockquote>
<br/> <span data-ttu-id="89f0b-189">從位於系統記憶體中的檔案建立材質資源。</span><span class="sxs-lookup"><span data-stu-id="89f0b-189">Create a texture resource from a file residing in system memory.</span></span><br/></td>
</tr>
<tr class="even">
<td><span data-ttu-id="89f0b-190"><a href="d3dx11createtexturefromresource.md"><strong>D3DX11CreateTextureFromResource</strong></a></span><span class="sxs-lookup"><span data-stu-id="89f0b-190"><a href="d3dx11createtexturefromresource.md"><strong>D3DX11CreateTextureFromResource</strong></a></span></span><br/></td>
<td><blockquote>
[!Note]<br />
<span data-ttu-id="89f0b-191">D3DX (D3DX 9、D3DX 10 和 D3DX 11) 公用程式庫已針對 Windows 8 淘汰，而且不支援 Windows Store 應用程式。</span><span class="sxs-lookup"><span data-stu-id="89f0b-191">The D3DX (D3DX 9, D3DX 10, and D3DX 11) utility library is deprecated for Windows 8 and is not supported for Windows Store apps.</span></span>
</blockquote>
<br/>
<blockquote>
<p>[!Note]<br />
<span data-ttu-id="89f0b-192">我們建議您不要使用此函式，而是使用 <a href="/windows/desktop/menurc/resources-functions">資源</a>函式，如下所示：</span><span class="sxs-lookup"><span data-stu-id="89f0b-192">Instead of using this function, we recommend that you use <a href="/windows/desktop/menurc/resources-functions">resource functions</a>, then these:</span></span></p>
<ul>
<li><span data-ttu-id="89f0b-193"><a href="https://github.com/Microsoft/DirectXTK">DirectXTK</a> 程式庫 (runtime) 、 <strong>CreateXXXTextureFromMemory</strong> (，其中 XXX 是 DDS 或 WIC) </span><span class="sxs-lookup"><span data-stu-id="89f0b-193"><a href="https://github.com/Microsoft/DirectXTK">DirectXTK</a> library (runtime), <strong>CreateXXXTextureFromMemory</strong> (where XXX is DDS or WIC)</span></span></li>
<li><span data-ttu-id="89f0b-194"><a href="https://github.com/Microsoft/DirectXTex">DirectXTex</a> 程式庫 (工具) 、 <strong>LOADFROMXXXMEMORY</strong> (其中 XXX 是 WIC、DDS 或 TGA;WIC 不支援 DDS 和 TGA;D3DX 9 支援的 TGA 做為遊戲的常用藝術來源格式) 然後 <strong>CreateTexture</strong></span><span class="sxs-lookup"><span data-stu-id="89f0b-194"><a href="https://github.com/Microsoft/DirectXTex">DirectXTex</a> library (tools), <strong>LoadFromXXXMemory</strong> (where XXX is WIC, DDS, or TGA; WIC doesn't support DDS and TGA; D3DX 9 supported TGA as a common art source format for games) then <strong>CreateTexture</strong></span></span></li>
</ul>
</blockquote>
<br/> <span data-ttu-id="89f0b-195">建立另一個資源的材質。</span><span class="sxs-lookup"><span data-stu-id="89f0b-195">Create a texture from another resource.</span></span><br/></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="89f0b-196"><a href="d3dx11createthreadpump.md"><strong>D3DX11CreateThreadPump</strong></a></span><span class="sxs-lookup"><span data-stu-id="89f0b-196"><a href="d3dx11createthreadpump.md"><strong>D3DX11CreateThreadPump</strong></a></span></span><br/></td>
<td><blockquote>
[!Note]<br />
<span data-ttu-id="89f0b-197">D3DX (D3DX 9、D3DX 10 和 D3DX 11) 公用程式庫已針對 Windows 8 淘汰，而且不支援 Windows Store 應用程式。</span><span class="sxs-lookup"><span data-stu-id="89f0b-197">The D3DX (D3DX 9, D3DX 10, and D3DX 11) utility library is deprecated for Windows 8 and is not supported for Windows Store apps.</span></span> <span data-ttu-id="89f0b-198">請參閱＜備註＞。</span><span class="sxs-lookup"><span data-stu-id="89f0b-198">See Remarks.</span></span>
</blockquote>
<br/> <span data-ttu-id="89f0b-199">建立執行緒抽取。</span><span class="sxs-lookup"><span data-stu-id="89f0b-199">Create a thread pump.</span></span><br/></td>
</tr>
<tr class="even">
<td><span data-ttu-id="89f0b-200"><a href="d3dx11filtertexture.md"><strong>D3DX11FilterTexture</strong></a></span><span class="sxs-lookup"><span data-stu-id="89f0b-200"><a href="d3dx11filtertexture.md"><strong>D3DX11FilterTexture</strong></a></span></span><br/></td>
<td><blockquote>
[!Note]<br />
<span data-ttu-id="89f0b-201">D3DX (D3DX 9、D3DX 10 和 D3DX 11) 公用程式庫已針對 Windows 8 淘汰，而且不支援 Windows Store 應用程式。</span><span class="sxs-lookup"><span data-stu-id="89f0b-201">The D3DX (D3DX 9, D3DX 10, and D3DX 11) utility library is deprecated for Windows 8 and is not supported for Windows Store apps.</span></span>
</blockquote>
<br/>
<blockquote>
[!Note]<br />
<span data-ttu-id="89f0b-202">我們建議您不要使用此函式，而是使用 <a href="https://github.com/Microsoft/DirectXTex">DirectXTex</a> 程式庫 <strong>GenerateMipMaps</strong> 和 <strong>GenerateMipMaps3D</strong>。</span><span class="sxs-lookup"><span data-stu-id="89f0b-202">Instead of using this function, we recommend that you use the <a href="https://github.com/Microsoft/DirectXTex">DirectXTex</a> library, <strong>GenerateMipMaps</strong> and <strong>GenerateMipMaps3D</strong>.</span></span>
</blockquote>
<br/> <span data-ttu-id="89f0b-203">使用特定的材質篩選器產生 mipmap 鏈。</span><span class="sxs-lookup"><span data-stu-id="89f0b-203">Generates mipmap chain using a particular texture filter.</span></span><br/></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="89f0b-204"><a href="d3dx11getimageinfofromfile.md"><strong>D3DX11GetImageInfoFromFile</strong></a></span><span class="sxs-lookup"><span data-stu-id="89f0b-204"><a href="d3dx11getimageinfofromfile.md"><strong>D3DX11GetImageInfoFromFile</strong></a></span></span><br/></td>
<td><blockquote>
[!Note]<br />
<span data-ttu-id="89f0b-205">D3DX (D3DX 9、D3DX 10 和 D3DX 11) 公用程式庫已針對 Windows 8 淘汰，而且不支援 Windows Store 應用程式。</span><span class="sxs-lookup"><span data-stu-id="89f0b-205">The D3DX (D3DX 9, D3DX 10, and D3DX 11) utility library is deprecated for Windows 8 and is not supported for Windows Store apps.</span></span>
</blockquote>
<br/>
<blockquote>
[!Note]<br />
<span data-ttu-id="89f0b-206">我們建議您不要使用這個函式，而是使用 <a href="https://github.com/Microsoft/DirectXTex">DirectXTex</a> 程式庫 <strong>GETMETADATAFROMXXXFILE</strong> (其中 XXX 是 WIC、DDS 或 TGA;WIC 不支援 DDS 和 TGA;D3DX 9 支援 TGA 作為遊戲) 的常用藝術來源格式。</span><span class="sxs-lookup"><span data-stu-id="89f0b-206">Instead of using this function, we recommend that you use the <a href="https://github.com/Microsoft/DirectXTex">DirectXTex</a> library, <strong>GetMetadataFromXXXFile</strong> (where XXX is WIC, DDS, or TGA; WIC doesn't support DDS and TGA; D3DX 9 supported TGA as a common art source format for games).</span></span>
</blockquote>
<br/> <span data-ttu-id="89f0b-207">抓取指定影像檔案的相關資訊。</span><span class="sxs-lookup"><span data-stu-id="89f0b-207">Retrieves information about a given image file.</span></span><br/></td>
</tr>
<tr class="even">
<td><span data-ttu-id="89f0b-208"><a href="d3dx11getimageinfofrommemory.md"><strong>D3DX11GetImageInfoFromMemory</strong></a></span><span class="sxs-lookup"><span data-stu-id="89f0b-208"><a href="d3dx11getimageinfofrommemory.md"><strong>D3DX11GetImageInfoFromMemory</strong></a></span></span><br/></td>
<td><blockquote>
[!Note]<br />
<span data-ttu-id="89f0b-209">D3DX (D3DX 9、D3DX 10 和 D3DX 11) 公用程式庫已針對 Windows 8 淘汰，而且不支援 Windows Store 應用程式。</span><span class="sxs-lookup"><span data-stu-id="89f0b-209">The D3DX (D3DX 9, D3DX 10, and D3DX 11) utility library is deprecated for Windows 8 and is not supported for Windows Store apps.</span></span>
</blockquote>
<br/>
<blockquote>
[!Note]<br />
<span data-ttu-id="89f0b-210">我們建議您不要使用這個函式，而是使用 <a href="https://github.com/Microsoft/DirectXTex">DirectXTex</a> 程式庫 <strong>GETMETADATAFROMXXXMEMORY</strong> (其中 XXX 是 WIC、DDS 或 TGA;WIC 不支援 DDS 和 TGA;D3DX 9 支援 TGA 作為遊戲) 的常用藝術來源格式。</span><span class="sxs-lookup"><span data-stu-id="89f0b-210">Instead of using this function, we recommend that you use the <a href="https://github.com/Microsoft/DirectXTex">DirectXTex</a> library, <strong>GetMetadataFromXXXMemory</strong> (where XXX is WIC, DDS, or TGA; WIC doesn't support DDS and TGA; D3DX 9 supported TGA as a common art source format for games).</span></span>
</blockquote>
<br/> <span data-ttu-id="89f0b-211">取得已載入記憶體之映射的相關資訊。</span><span class="sxs-lookup"><span data-stu-id="89f0b-211">Get information about an image already loaded into memory.</span></span><br/></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="89f0b-212"><a href="d3dx11getimageinfofromresource.md"><strong>D3DX11GetImageInfoFromResource</strong></a></span><span class="sxs-lookup"><span data-stu-id="89f0b-212"><a href="d3dx11getimageinfofromresource.md"><strong>D3DX11GetImageInfoFromResource</strong></a></span></span><br/></td>
<td><blockquote>
[!Note]<br />
<span data-ttu-id="89f0b-213">D3DX (D3DX 9、D3DX 10 和 D3DX 11) 公用程式庫已針對 Windows 8 淘汰，而且不支援 Windows Store 應用程式。</span><span class="sxs-lookup"><span data-stu-id="89f0b-213">The D3DX (D3DX 9, D3DX 10, and D3DX 11) utility library is deprecated for Windows 8 and is not supported for Windows Store apps.</span></span>
</blockquote>
<br/>
<blockquote>
[!Note]<br />
<span data-ttu-id="89f0b-214">我們建議您不要使用此函式，而是使用 <a href="/windows/desktop/menurc/resources-functions">資源</a>函式，然後使用 <a href="https://github.com/Microsoft/DirectXTex">DirectXTex</a> 程式庫 (工具) 、 <strong>LOADFROMXXXMEMORY</strong> (其中 XXX 是 WIC、DDS 或 TGA;WIC 不支援 DDS 和 TGA;D3DX 9 支援 TGA 作為遊戲) 的常用藝術來源格式。</span><span class="sxs-lookup"><span data-stu-id="89f0b-214">Instead of using this function, we recommend that you use <a href="/windows/desktop/menurc/resources-functions">resource functions</a>, then use <a href="https://github.com/Microsoft/DirectXTex">DirectXTex</a> library (tools), <strong>LoadFromXXXMemory</strong> (where XXX is WIC, DDS, or TGA; WIC doesn't support DDS and TGA; D3DX 9 supported TGA as a common art source format for games).</span></span>
</blockquote>
<br/> <span data-ttu-id="89f0b-215">抓取資源中指定影像的相關資訊。</span><span class="sxs-lookup"><span data-stu-id="89f0b-215">Retrieves information about a given image in a resource.</span></span><br/></td>
</tr>
<tr class="even">
<td><span data-ttu-id="89f0b-216"><a href="d3dx11loadtexturefromtexture.md"><strong>D3DX11LoadTextureFromTexture</strong></a></span><span class="sxs-lookup"><span data-stu-id="89f0b-216"><a href="d3dx11loadtexturefromtexture.md"><strong>D3DX11LoadTextureFromTexture</strong></a></span></span><br/></td>
<td><blockquote>
[!Note]<br />
<span data-ttu-id="89f0b-217">D3DX (D3DX 9、D3DX 10 和 D3DX 11) 公用程式庫已針對 Windows 8 淘汰，而且不支援 Windows Store 應用程式。</span><span class="sxs-lookup"><span data-stu-id="89f0b-217">The D3DX (D3DX 9, D3DX 10, and D3DX 11) utility library is deprecated for Windows 8 and is not supported for Windows Store apps.</span></span>
</blockquote>
<br/>
<blockquote>
[!Note]<br />
<span data-ttu-id="89f0b-218">我們建議您不要使用此函式，而是使用 <a href="https://github.com/Microsoft/DirectXTex">DirectXTex</a> 程式庫、重 <strong>設大小</strong>、 <strong>轉換</strong>、 <strong>壓縮</strong>、 <strong>解壓縮</strong>和/或 <strong>CopyRectangle</strong>。</span><span class="sxs-lookup"><span data-stu-id="89f0b-218">Instead of using this function, we recommend that you use the <a href="https://github.com/Microsoft/DirectXTex">DirectXTex</a> library, <strong>Resize</strong>, <strong>Convert</strong>, <strong>Compress</strong>, <strong>Decompress</strong>, and/or <strong>CopyRectangle</strong>.</span></span>
</blockquote>
<br/> <span data-ttu-id="89f0b-219">從材質載入紋理。</span><span class="sxs-lookup"><span data-stu-id="89f0b-219">Load a texture from a texture.</span></span><br/></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="89f0b-220"><a href="d3dx11preprocessshaderfromfile.md"><strong>D3DX11PreprocessShaderFromFile</strong></a></span><span class="sxs-lookup"><span data-stu-id="89f0b-220"><a href="d3dx11preprocessshaderfromfile.md"><strong>D3DX11PreprocessShaderFromFile</strong></a></span></span><br/></td>
<td><blockquote>
[!Note]<br />
<span data-ttu-id="89f0b-221">D3DX (D3DX 9、D3DX 10 和 D3DX 11) 公用程式庫已針對 Windows 8 淘汰，而且不支援 Windows Store 應用程式。</span><span class="sxs-lookup"><span data-stu-id="89f0b-221">The D3DX (D3DX 9, D3DX 10, and D3DX 11) utility library is deprecated for Windows 8 and is not supported for Windows Store apps.</span></span>
</blockquote>
<br/>
<blockquote>
[!Note]<br />
<span data-ttu-id="89f0b-222">我們建議您不要使用此函式，而是使用 <a href="/windows/desktop/direct3dhlsl/d3dpreprocess"><strong>D3DPreprocess</strong></a> API。</span><span class="sxs-lookup"><span data-stu-id="89f0b-222">Instead of using this function, we recommend that you use the <a href="/windows/desktop/direct3dhlsl/d3dpreprocess"><strong>D3DPreprocess</strong></a> API.</span></span>
</blockquote>
<br/> <span data-ttu-id="89f0b-223">在不編譯的情況下，從檔案建立著色器。</span><span class="sxs-lookup"><span data-stu-id="89f0b-223">Create a shader from a file without compiling it.</span></span><br/></td>
</tr>
<tr class="even">
<td><span data-ttu-id="89f0b-224"><a href="d3dx11preprocessshaderfrommemory.md"><strong>D3DX11PreprocessShaderFromMemory</strong></a></span><span class="sxs-lookup"><span data-stu-id="89f0b-224"><a href="d3dx11preprocessshaderfrommemory.md"><strong>D3DX11PreprocessShaderFromMemory</strong></a></span></span><br/></td>
<td><blockquote>
[!Note]<br />
<span data-ttu-id="89f0b-225">D3DX (D3DX 9、D3DX 10 和 D3DX 11) 公用程式庫已針對 Windows 8 淘汰，而且不支援 Windows Store 應用程式。</span><span class="sxs-lookup"><span data-stu-id="89f0b-225">The D3DX (D3DX 9, D3DX 10, and D3DX 11) utility library is deprecated for Windows 8 and is not supported for Windows Store apps.</span></span>
</blockquote>
<br/>
<blockquote>
[!Note]<br />
<span data-ttu-id="89f0b-226">我們建議您不要使用此函式，而是使用 <a href="/windows/desktop/direct3dhlsl/d3dpreprocess"><strong>D3DPreprocess</strong></a> API。</span><span class="sxs-lookup"><span data-stu-id="89f0b-226">Instead of using this function, we recommend that you use the <a href="/windows/desktop/direct3dhlsl/d3dpreprocess"><strong>D3DPreprocess</strong></a> API.</span></span>
</blockquote>
<br/> <span data-ttu-id="89f0b-227">在不編譯的情況下，從記憶體建立著色器。</span><span class="sxs-lookup"><span data-stu-id="89f0b-227">Create a shader from memory without compiling it.</span></span><br/></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="89f0b-228"><a href="d3dx11preprocessshaderfromresource.md"><strong>D3DX11PreprocessShaderFromResource</strong></a></span><span class="sxs-lookup"><span data-stu-id="89f0b-228"><a href="d3dx11preprocessshaderfromresource.md"><strong>D3DX11PreprocessShaderFromResource</strong></a></span></span><br/></td>
<td><blockquote>
[!Note]<br />
<span data-ttu-id="89f0b-229">D3DX (D3DX 9、D3DX 10 和 D3DX 11) 公用程式庫已針對 Windows 8 淘汰，而且不支援 Windows Store 應用程式。</span><span class="sxs-lookup"><span data-stu-id="89f0b-229">The D3DX (D3DX 9, D3DX 10, and D3DX 11) utility library is deprecated for Windows 8 and is not supported for Windows Store apps.</span></span>
</blockquote>
<br/>
<blockquote>
[!Note]<br />
<span data-ttu-id="89f0b-230">我們建議您不要使用此函式，而是使用 <a href="/windows/desktop/direct3dhlsl/d3dpreprocess"><strong>D3DPreprocess</strong></a> API。</span><span class="sxs-lookup"><span data-stu-id="89f0b-230">Instead of using this function, we recommend that you use the <a href="/windows/desktop/direct3dhlsl/d3dpreprocess"><strong>D3DPreprocess</strong></a> API.</span></span>
</blockquote>
<br/> <span data-ttu-id="89f0b-231">從資源建立著色器，而不進行編譯。</span><span class="sxs-lookup"><span data-stu-id="89f0b-231">Create a shader from a resource without compiling it.</span></span><br/></td>
</tr>
<tr class="even">
<td><span data-ttu-id="89f0b-232"><a href="d3dx11savetexturetofile.md"><strong>D3DX11SaveTextureToFile</strong></a></span><span class="sxs-lookup"><span data-stu-id="89f0b-232"><a href="d3dx11savetexturetofile.md"><strong>D3DX11SaveTextureToFile</strong></a></span></span><br/></td>
<td><blockquote>
[!Note]<br />
<span data-ttu-id="89f0b-233">D3DX (D3DX 9、D3DX 10 和 D3DX 11) 公用程式庫已針對 Windows 8 淘汰，而且不支援 Windows Store 應用程式。</span><span class="sxs-lookup"><span data-stu-id="89f0b-233">The D3DX (D3DX 9, D3DX 10, and D3DX 11) utility library is deprecated for Windows 8 and is not supported for Windows Store apps.</span></span>
</blockquote>
<br/>
<blockquote>
[!Note]<br />
<span data-ttu-id="89f0b-234">我們建議您不要使用這個函式，而是使用 <a href="https://github.com/Microsoft/DirectXTex">DirectXTex</a> 程式庫， <strong>CaptureTexture</strong> 接著 <strong>SAVETOXXXFILE</strong> (其中 XXX 是 WIC、DDS 或 TGA;WIC 不支援 DDS 和 TGA;D3DX 9 支援 TGA 作為遊戲) 的常用藝術來源格式。</span><span class="sxs-lookup"><span data-stu-id="89f0b-234">Instead of using this function, we recommend that you use the <a href="https://github.com/Microsoft/DirectXTex">DirectXTex</a> library, <strong>CaptureTexture</strong> then <strong>SaveToXXXFile</strong> (where XXX is WIC, DDS, or TGA; WIC doesn't support DDS and TGA; D3DX 9 supported TGA as a common art source format for games).</span></span> <span data-ttu-id="89f0b-235">針對從呈現目標材質建立螢幕擷取畫面的簡化案例，建議您使用 <a href="https://github.com/Microsoft/DirectXTK">DirectXTK</a> 程式庫 <strong>SaveDDSTextureToFile</strong> 或 <strong>SaveWICTextureToFile</strong>。</span><span class="sxs-lookup"><span data-stu-id="89f0b-235">For the simplified scenario of creating a screen shot from a render target texture, we recommend that you use the <a href="https://github.com/Microsoft/DirectXTK">DirectXTK</a> library, <strong>SaveDDSTextureToFile</strong> or <strong>SaveWICTextureToFile</strong>.</span></span>
</blockquote>
<br/> <span data-ttu-id="89f0b-236">將材質儲存至檔案。</span><span class="sxs-lookup"><span data-stu-id="89f0b-236">Save a texture to a file.</span></span><br/></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="89f0b-237"><a href="d3dx11savetexturetomemory.md"><strong>D3DX11SaveTextureToMemory</strong></a></span><span class="sxs-lookup"><span data-stu-id="89f0b-237"><a href="d3dx11savetexturetomemory.md"><strong>D3DX11SaveTextureToMemory</strong></a></span></span><br/></td>
<td><blockquote>
[!Note]<br />
<span data-ttu-id="89f0b-238">D3DX (D3DX 9、D3DX 10 和 D3DX 11) 公用程式庫已針對 Windows 8 淘汰，而且不支援 Windows Store 應用程式。</span><span class="sxs-lookup"><span data-stu-id="89f0b-238">The D3DX (D3DX 9, D3DX 10, and D3DX 11) utility library is deprecated for Windows 8 and is not supported for Windows Store apps.</span></span>
</blockquote>
<br/>
<blockquote>
[!Note]<br />
<span data-ttu-id="89f0b-239">我們建議您不要使用這個函式，而是使用 <a href="https://github.com/Microsoft/DirectXTex">DirectXTex</a> 程式庫， <strong>CaptureTexture</strong> 接著 <strong>SAVETOXXXMEMORY</strong> (其中 XXX 是 WIC、DDS 或 TGA;WIC 不支援 DDS 和 TGA;D3DX 9 支援 TGA 作為遊戲) 的常用藝術來源格式。</span><span class="sxs-lookup"><span data-stu-id="89f0b-239">Instead of using this function, we recommend that you use the <a href="https://github.com/Microsoft/DirectXTex">DirectXTex</a> library, <strong>CaptureTexture</strong> then <strong>SaveToXXXMemory</strong> (where XXX is WIC, DDS, or TGA; WIC doesn't support DDS and TGA; D3DX 9 supported TGA as a common art source format for games).</span></span>
</blockquote>
<br/> <span data-ttu-id="89f0b-240">將材質儲存至記憶體。</span><span class="sxs-lookup"><span data-stu-id="89f0b-240">Save a texture to memory.</span></span><br/></td>
</tr>
<tr class="even">
<td><span data-ttu-id="89f0b-241"><a href="d3dx11shprojectcubemap.md"><strong>D3DX11SHProjectCubeMap</strong></a></span><span class="sxs-lookup"><span data-stu-id="89f0b-241"><a href="d3dx11shprojectcubemap.md"><strong>D3DX11SHProjectCubeMap</strong></a></span></span><br/></td>
<td><blockquote>
[!Note]<br />
<span data-ttu-id="89f0b-242">D3DX (D3DX 9、D3DX 10 和 D3DX 11) 公用程式庫已針對 Windows 8 淘汰，而且不支援 Windows Store 應用程式。</span><span class="sxs-lookup"><span data-stu-id="89f0b-242">The D3DX (D3DX 9, D3DX 10, and D3DX 11) utility library is deprecated for Windows 8 and is not supported for Windows Store apps.</span></span>
</blockquote>
<br/>
<blockquote>
[!Note]<br />
<span data-ttu-id="89f0b-243">我們建議您不要使用這個函數，而是使用 <a href="https://github.com/Microsoft/DirectXMath/tree/master/SHMath">球形諧波數學</a> 程式庫 <strong>SHProjectCubeMap</strong>。</span><span class="sxs-lookup"><span data-stu-id="89f0b-243">Instead of using this function, we recommend that you use the <a href="https://github.com/Microsoft/DirectXMath/tree/master/SHMath">Spherical Harmonics Math</a> library, <strong>SHProjectCubeMap</strong>.</span></span>
</blockquote>
<br/> <span data-ttu-id="89f0b-244">將 cube 地圖中表示的函式投射到球面諧波。</span><span class="sxs-lookup"><span data-stu-id="89f0b-244">Projects a function represented in a cube map into spherical harmonics.</span></span><br/></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="89f0b-245"><a href="d3dx11unsetalldeviceobjects.md"><strong>D3DX11UnsetAllDeviceObjects</strong></a></span><span class="sxs-lookup"><span data-stu-id="89f0b-245"><a href="d3dx11unsetalldeviceobjects.md"><strong>D3DX11UnsetAllDeviceObjects</strong></a></span></span><br/></td>
<td><blockquote>
[!Note]<br />
<span data-ttu-id="89f0b-246">D3DX (D3DX 9、D3DX 10 和 D3DX 11) 公用程式庫已針對 Windows 8 淘汰，而且不支援 Windows Store 應用程式。</span><span class="sxs-lookup"><span data-stu-id="89f0b-246">The D3DX (D3DX 9, D3DX 10, and D3DX 11) utility library is deprecated for Windows 8 and is not supported for Windows Store apps.</span></span>
</blockquote>
<br/>
<blockquote>
[!Note]<br />
<span data-ttu-id="89f0b-247">我們建議您使用 <a href="/windows/desktop/api/D3D11/nf-d3d11-id3d11devicecontext-clearstate"><strong>>id3d11devicecoNtext：： ClearState</strong></a> 方法，而不是使用此函數。</span><span class="sxs-lookup"><span data-stu-id="89f0b-247">Instead of using this function, we recommend that you use the <a href="/windows/desktop/api/D3D11/nf-d3d11-id3d11devicecontext-clearstate"><strong>ID3D11DeviceContext::ClearState</strong></a> method.</span></span>
</blockquote>
<br/> <span data-ttu-id="89f0b-248">將所有資源的指標設為 <strong>Null</strong>，以移除裝置中的所有資源。</span><span class="sxs-lookup"><span data-stu-id="89f0b-248">Removes all resources from the device by setting their pointers to <strong>NULL</strong>.</span></span> <span data-ttu-id="89f0b-249">這應該會在應用程式關閉時呼叫。</span><span class="sxs-lookup"><span data-stu-id="89f0b-249">This should be called during shutdown of your application.</span></span> <span data-ttu-id="89f0b-250">這有助於確保當某個資源釋出所有資源時，都不會將這些資源系結至裝置。</span><span class="sxs-lookup"><span data-stu-id="89f0b-250">It helps ensure that when one is releasing all of their resources that none of them are bound to the device.</span></span><br/></td>
</tr>
</tbody>
</table>



 

## <a name="related-topics"></a><span data-ttu-id="89f0b-251">相關主題</span><span class="sxs-lookup"><span data-stu-id="89f0b-251">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="89f0b-252">D3DX 11 參考</span><span class="sxs-lookup"><span data-stu-id="89f0b-252">D3DX 11 Reference</span></span>](d3d11-graphics-reference-d3dx11.md)
</dt> </dl>

 

