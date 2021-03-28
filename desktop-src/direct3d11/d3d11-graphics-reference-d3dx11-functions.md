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
# <a name="d3dx-functions-direct3d-11-graphics"></a>D3DX 函式 (Direct3D 11 圖形) 

本節包含 D3DX 11 函數的相關資訊。

> [!Note]  
> D3DX (D3DX 9、D3DX 10 和 D3DX 11) 公用程式庫已針對 Windows 8 淘汰，而且不支援 Windows Store 應用程式。

 


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
<td><a href="d3dx11compilefromfile.md"><strong>D3DX11CompileFromFile</strong></a><br/></td>
<td><blockquote>
[!Note]<br />
D3DX (D3DX 9、D3DX 10 和 D3DX 11) 公用程式庫已針對 Windows 8 淘汰，而且不支援 Windows Store 應用程式。
</blockquote>
<br/>
<blockquote>
[!Note]<br />
我們建議您不要使用這個函式，而是使用 Fxc.exe 命令列編譯器，或使用其中一個 HLSL 編譯 Api （例如 <a href="/windows/desktop/direct3dhlsl/d3dcompilefromfile"><strong>D3DCompileFromFile</strong></a> API），以離線方式編譯。
</blockquote>
<br/> 從檔案編譯著色器或效果。<br/></td>
</tr>
<tr class="even">
<td><a href="d3dx11compilefrommemory.md"><strong>D3DX11CompileFromMemory</strong></a><br/></td>
<td><blockquote>
[!Note]<br />
D3DX (D3DX 9、D3DX 10 和 D3DX 11) 公用程式庫已針對 Windows 8 淘汰，而且不支援 Windows Store 應用程式。
</blockquote>
<br/>
<blockquote>
[!Note]<br />
我們建議您不要使用這個函式，而是使用 Fxc.exe 命令列編譯器，或使用其中一個 HLSL 編譯 Api （例如 <a href="/windows/desktop/direct3dhlsl/d3dcompile"><strong>D3DCompile</strong></a> API），以離線方式編譯。
</blockquote>
<br/> 編譯已載入記憶體中的著色器或效果。<br/></td>
</tr>
<tr class="odd">
<td><a href="d3dx11compilefromresource.md"><strong>D3DX11CompileFromResource</strong></a><br/></td>
<td><blockquote>
[!Note]<br />
D3DX (D3DX 9、D3DX 10 和 D3DX 11) 公用程式庫已針對 Windows 8 淘汰，而且不支援 Windows Store 應用程式。
</blockquote>
<br/>
<blockquote>
[!Note]<br />
我們建議您不要使用此函式，而是使用 <a href="/windows/desktop/menurc/resources-functions">資源</a>函式，然後使用 Fxc.exe 命令列編譯器或使用其中一個 HLSL 編譯 api （例如 <a href="/windows/desktop/direct3dhlsl/d3dcompile"><strong>D3DCompile</strong></a> API），以離線方式編譯。
</blockquote>
<br/> 從資源編譯著色器或效果。<br/></td>
</tr>
<tr class="even">
<td><a href="d3dx11computenormalmap.md"><strong>D3DX11ComputeNormalMap</strong></a><br/></td>
<td><blockquote>
[!Note]<br />
D3DX (D3DX 9、D3DX 10 和 D3DX 11) 公用程式庫已針對 Windows 8 淘汰，而且不支援 Windows Store 應用程式。
</blockquote>
<br/>
<blockquote>
[!Note]<br />
我們建議您不要使用此函式，而是使用 <a href="https://github.com/Microsoft/DirectXTex">DirectXTex</a> 程式庫 <strong>ComputeNormalMap</strong>。
</blockquote>
<br/> 將高度地圖轉換成一般地圖。 每個標準的 (x、y、z) 元件都會對應到輸出材質 (r、g、b) 通道。<br/></td>
</tr>
<tr class="odd">
<td><a href="d3dx11createasynccompilerprocessor.md"><strong>D3DX11CreateAsyncCompilerProcessor</strong></a><br/></td>
<td><blockquote>
[!Note]<br />
D3DX (D3DX 9、D3DX 10 和 D3DX 11) 公用程式庫已針對 Windows 8 淘汰，而且不支援 Windows Store 應用程式。 請參閱＜備註＞。
</blockquote>
<br/> 建立著色器的非同步資料處理器。<br/></td>
</tr>
<tr class="even">
<td><a href="d3dx11createasyncfileloader.md"><strong>D3DX11CreateAsyncFileLoader</strong></a><br/></td>
<td><blockquote>
[!Note]<br />
D3DX (D3DX 9、D3DX 10 和 D3DX 11) 公用程式庫已針對 Windows 8 淘汰，而且不支援 Windows Store 應用程式。 請參閱＜備註＞。
</blockquote>
<br/> 建立異步檔案載入器。<br/></td>
</tr>
<tr class="odd">
<td><a href="d3dx11createasyncmemoryloader.md"><strong>D3DX11CreateAsyncMemoryLoader</strong></a><br/></td>
<td><blockquote>
[!Note]<br />
D3DX (D3DX 9、D3DX 10 和 D3DX 11) 公用程式庫已針對 Windows 8 淘汰，而且不支援 Windows Store 應用程式。 請參閱＜備註＞。
</blockquote>
<br/> 建立異步記憶體載入器。<br/></td>
</tr>
<tr class="even">
<td><a href="d3dx11createasyncresourceloader.md"><strong>D3DX11CreateAsyncResourceLoader</strong></a><br/></td>
<td><blockquote>
[!Note]<br />
D3DX (D3DX 9、D3DX 10 和 D3DX 11) 公用程式庫已針對 Windows 8 淘汰，而且不支援 Windows Store 應用程式。 請參閱＜備註＞。
</blockquote>
<br/> 建立異步資源載入器。<br/></td>
</tr>
<tr class="odd">
<td><a href="d3dx11createasyncshaderpreprocessprocessor.md"><strong>D3DX11CreateAsyncShaderPreprocessProcessor</strong></a><br/></td>
<td><blockquote>
[!Note]<br />
D3DX (D3DX 9、D3DX 10 和 D3DX 11) 公用程式庫已針對 Windows 8 淘汰，而且不支援 Windows Store 應用程式。 請參閱＜備註＞。
</blockquote>
<br/> 以非同步方式建立著色器的資料處理器。<br/></td>
</tr>
<tr class="even">
<td><a href="d3dx11createasynctextureinfoprocessor.md"><strong>D3DX11CreateAsyncTextureInfoProcessor</strong></a><br/></td>
<td><blockquote>
[!Note]<br />
D3DX (D3DX 9、D3DX 10 和 D3DX 11) 公用程式庫已針對 Windows 8 淘汰，而且不支援 Windows Store 應用程式。 請參閱＜備註＞。
</blockquote>
<br/> 建立要搭配 <a href="id3dx11threadpump.md"><strong>執行緒抽取</strong></a>使用的資料處理器。<br/></td>
</tr>
<tr class="odd">
<td><a href="d3dx11createasynctextureprocessor.md"><strong>D3DX11CreateAsyncTextureProcessor</strong></a><br/></td>
<td><blockquote>
[!Note]<br />
D3DX (D3DX 9、D3DX 10 和 D3DX 11) 公用程式庫已針對 Windows 8 淘汰，而且不支援 Windows Store 應用程式。 請參閱＜備註＞。
</blockquote>
<br/> 建立要搭配 <a href="id3dx11threadpump.md"><strong>執行緒抽取</strong></a>使用的資料處理器。<br/></td>
</tr>
<tr class="even">
<td><a href="d3dx11createasyncshaderresourceviewprocessor.md"><strong>D3DX11CreateAsyncShaderResourceViewProcessor</strong></a><br/></td>
<td><blockquote>
[!Note]<br />
D3DX (D3DX 9、D3DX 10 和 D3DX 11) 公用程式庫已針對 Windows 8 淘汰，而且不支援 Windows Store 應用程式。 請參閱＜備註＞。
</blockquote>
<br/> 建立會載入資源的資料處理器，然後為其建立著色器資源檢視。 資料處理器是 D3DX11 中使用 <a href="id3dx11threadpump.md"><strong>執行緒抽取</strong></a>的非同步資料載入功能的元件。<br/></td>
</tr>
<tr class="odd">
<td><a href="d3dx11createshaderresourceviewfromfile.md"><strong>D3DX11CreateShaderResourceViewFromFile</strong></a><br/></td>
<td><blockquote>
[!Note]<br />
D3DX (D3DX 9、D3DX 10 和 D3DX 11) 公用程式庫已針對 Windows 8 淘汰，而且不支援 Windows Store 應用程式。
</blockquote>
<br/>
<blockquote>
<p>[!Note]<br />
我們建議您不要使用這個函式，而是使用下列功能：</p>
<ul>
<li><a href="https://github.com/Microsoft/DirectXTK">DirectXTK</a> 程式庫 (runtime) 、 <strong>CreateXXXTextureFromFile</strong> (，其中 XXX 是 DDS 或 WIC) </li>
<li><a href="https://github.com/Microsoft/DirectXTex">DirectXTex</a> 程式庫 (工具) 、 <strong>LOADFROMXXXFILE</strong> (其中 XXX 是 WIC、DDS 或 TGA;WIC 不支援 DDS 和 TGA;D3DX 9 支援的 TGA 做為遊戲的常用藝術來源格式) 然後 <strong>CreateShaderResourceView</strong></li>
</ul>
</blockquote>
<br/> 從檔案建立著色器資源檢視。<br/></td>
</tr>
<tr class="even">
<td><a href="d3dx11createshaderresourceviewfrommemory.md"><strong>D3DX11CreateShaderResourceViewFromMemory</strong></a><br/></td>
<td><blockquote>
[!Note]<br />
D3DX (D3DX 9、D3DX 10 和 D3DX 11) 公用程式庫已針對 Windows 8 淘汰，而且不支援 Windows Store 應用程式。
</blockquote>
<br/>
<blockquote>
<p>[!Note]<br />
我們建議您不要使用這個函式，而是使用下列功能：</p>
<ul>
<li><a href="https://github.com/Microsoft/DirectXTK">DirectXTK</a> 程式庫 (runtime) 、 <strong>CreateXXXTextureFromMemory</strong> (，其中 XXX 是 DDS 或 WIC) </li>
<li><a href="https://github.com/Microsoft/DirectXTex">DirectXTex</a> 程式庫 (工具) 、 <strong>LOADFROMXXXMEMORY</strong> (其中 XXX 是 WIC、DDS 或 TGA;WIC 不支援 DDS 和 TGA;D3DX 9 支援的 TGA 做為遊戲的常用藝術來源格式) 然後 <strong>CreateShaderResourceView</strong></li>
</ul>
</blockquote>
<br/> 從記憶體中的檔案建立著色器資源檢視。<br/></td>
</tr>
<tr class="odd">
<td><a href="d3dx11createshaderresourceviewfromresource.md"><strong>D3DX11CreateShaderResourceViewFromResource</strong></a><br/></td>
<td><blockquote>
[!Note]<br />
D3DX (D3DX 9、D3DX 10 和 D3DX 11) 公用程式庫已針對 Windows 8 淘汰，而且不支援 Windows Store 應用程式。
</blockquote>
<br/>
<blockquote>
<p>[!Note]<br />
我們建議您不要使用此函式，而是使用 <a href="/windows/desktop/menurc/resources-functions">資源</a>函式，如下所示：</p>
<ul>
<li><a href="https://github.com/Microsoft/DirectXTK">DirectXTK</a> 程式庫 (runtime) 、 <strong>CreateXXXTextureFromMemory</strong> (，其中 XXX 是 DDS 或 WIC) </li>
<li><a href="https://github.com/Microsoft/DirectXTex">DirectXTex</a> 程式庫 (工具) 、 <strong>LOADFROMXXXMEMORY</strong> (其中 XXX 是 WIC、DDS 或 TGA;WIC 不支援 DDS 和 TGA;D3DX 9 支援的 TGA 做為遊戲的常用藝術來源格式) 然後 <strong>CreateShaderResourceView</strong></li>
</ul>
</blockquote>
<br/> 從資源建立著色器資源檢視。<br/></td>
</tr>
<tr class="even">
<td><a href="d3dx11createtexturefromfile.md"><strong>D3DX11CreateTextureFromFile</strong></a><br/></td>
<td><blockquote>
[!Note]<br />
D3DX (D3DX 9、D3DX 10 和 D3DX 11) 公用程式庫已針對 Windows 8 淘汰，而且不支援 Windows Store 應用程式。
</blockquote>
<br/>
<blockquote>
<p>[!Note]<br />
我們建議您不要使用這個函式，而是使用下列功能：</p>
<ul>
<li><a href="https://github.com/Microsoft/DirectXTK">DirectXTK</a> 程式庫 (runtime) 、 <strong>CreateXXXTextureFromFile</strong> (，其中 XXX 是 DDS 或 WIC) </li>
<li><a href="https://github.com/Microsoft/DirectXTex">DirectXTex</a> 程式庫 (工具) 、 <strong>LOADFROMXXXFILE</strong> (其中 XXX 是 WIC、DDS 或 TGA;WIC 不支援 DDS 和 TGA;D3DX 9 支援的 TGA 做為遊戲的常用藝術來源格式) 然後 <strong>CreateTexture</strong></li>
</ul>
</blockquote>
<br/> 從檔案建立材質資源。<br/></td>
</tr>
<tr class="odd">
<td><a href="d3dx11createtexturefrommemory.md"><strong>D3DX11CreateTextureFromMemory</strong></a><br/></td>
<td><blockquote>
[!Note]<br />
D3DX (D3DX 9、D3DX 10 和 D3DX 11) 公用程式庫已針對 Windows 8 淘汰，而且不支援 Windows Store 應用程式。
</blockquote>
<br/>
<blockquote>
<p>[!Note]<br />
我們建議您不要使用這個函式，而是使用下列功能：</p>
<ul>
<li><a href="https://github.com/Microsoft/DirectXTK">DirectXTK</a> 程式庫 (runtime) 、 <strong>CreateXXXTextureFromMemory</strong> (，其中 XXX 是 DDS 或 WIC) </li>
<li><a href="https://github.com/Microsoft/DirectXTex">DirectXTex</a> 程式庫 (工具) 、 <strong>LOADFROMXXXMEMORY</strong> (其中 XXX 是 WIC、DDS 或 TGA;WIC 不支援 DDS 和 TGA;D3DX 9 支援的 TGA 做為遊戲的常用藝術來源格式) 然後 <strong>CreateTexture</strong></li>
</ul>
</blockquote>
<br/> 從位於系統記憶體中的檔案建立材質資源。<br/></td>
</tr>
<tr class="even">
<td><a href="d3dx11createtexturefromresource.md"><strong>D3DX11CreateTextureFromResource</strong></a><br/></td>
<td><blockquote>
[!Note]<br />
D3DX (D3DX 9、D3DX 10 和 D3DX 11) 公用程式庫已針對 Windows 8 淘汰，而且不支援 Windows Store 應用程式。
</blockquote>
<br/>
<blockquote>
<p>[!Note]<br />
我們建議您不要使用此函式，而是使用 <a href="/windows/desktop/menurc/resources-functions">資源</a>函式，如下所示：</p>
<ul>
<li><a href="https://github.com/Microsoft/DirectXTK">DirectXTK</a> 程式庫 (runtime) 、 <strong>CreateXXXTextureFromMemory</strong> (，其中 XXX 是 DDS 或 WIC) </li>
<li><a href="https://github.com/Microsoft/DirectXTex">DirectXTex</a> 程式庫 (工具) 、 <strong>LOADFROMXXXMEMORY</strong> (其中 XXX 是 WIC、DDS 或 TGA;WIC 不支援 DDS 和 TGA;D3DX 9 支援的 TGA 做為遊戲的常用藝術來源格式) 然後 <strong>CreateTexture</strong></li>
</ul>
</blockquote>
<br/> 建立另一個資源的材質。<br/></td>
</tr>
<tr class="odd">
<td><a href="d3dx11createthreadpump.md"><strong>D3DX11CreateThreadPump</strong></a><br/></td>
<td><blockquote>
[!Note]<br />
D3DX (D3DX 9、D3DX 10 和 D3DX 11) 公用程式庫已針對 Windows 8 淘汰，而且不支援 Windows Store 應用程式。 請參閱＜備註＞。
</blockquote>
<br/> 建立執行緒抽取。<br/></td>
</tr>
<tr class="even">
<td><a href="d3dx11filtertexture.md"><strong>D3DX11FilterTexture</strong></a><br/></td>
<td><blockquote>
[!Note]<br />
D3DX (D3DX 9、D3DX 10 和 D3DX 11) 公用程式庫已針對 Windows 8 淘汰，而且不支援 Windows Store 應用程式。
</blockquote>
<br/>
<blockquote>
[!Note]<br />
我們建議您不要使用此函式，而是使用 <a href="https://github.com/Microsoft/DirectXTex">DirectXTex</a> 程式庫 <strong>GenerateMipMaps</strong> 和 <strong>GenerateMipMaps3D</strong>。
</blockquote>
<br/> 使用特定的材質篩選器產生 mipmap 鏈。<br/></td>
</tr>
<tr class="odd">
<td><a href="d3dx11getimageinfofromfile.md"><strong>D3DX11GetImageInfoFromFile</strong></a><br/></td>
<td><blockquote>
[!Note]<br />
D3DX (D3DX 9、D3DX 10 和 D3DX 11) 公用程式庫已針對 Windows 8 淘汰，而且不支援 Windows Store 應用程式。
</blockquote>
<br/>
<blockquote>
[!Note]<br />
我們建議您不要使用這個函式，而是使用 <a href="https://github.com/Microsoft/DirectXTex">DirectXTex</a> 程式庫 <strong>GETMETADATAFROMXXXFILE</strong> (其中 XXX 是 WIC、DDS 或 TGA;WIC 不支援 DDS 和 TGA;D3DX 9 支援 TGA 作為遊戲) 的常用藝術來源格式。
</blockquote>
<br/> 抓取指定影像檔案的相關資訊。<br/></td>
</tr>
<tr class="even">
<td><a href="d3dx11getimageinfofrommemory.md"><strong>D3DX11GetImageInfoFromMemory</strong></a><br/></td>
<td><blockquote>
[!Note]<br />
D3DX (D3DX 9、D3DX 10 和 D3DX 11) 公用程式庫已針對 Windows 8 淘汰，而且不支援 Windows Store 應用程式。
</blockquote>
<br/>
<blockquote>
[!Note]<br />
我們建議您不要使用這個函式，而是使用 <a href="https://github.com/Microsoft/DirectXTex">DirectXTex</a> 程式庫 <strong>GETMETADATAFROMXXXMEMORY</strong> (其中 XXX 是 WIC、DDS 或 TGA;WIC 不支援 DDS 和 TGA;D3DX 9 支援 TGA 作為遊戲) 的常用藝術來源格式。
</blockquote>
<br/> 取得已載入記憶體之映射的相關資訊。<br/></td>
</tr>
<tr class="odd">
<td><a href="d3dx11getimageinfofromresource.md"><strong>D3DX11GetImageInfoFromResource</strong></a><br/></td>
<td><blockquote>
[!Note]<br />
D3DX (D3DX 9、D3DX 10 和 D3DX 11) 公用程式庫已針對 Windows 8 淘汰，而且不支援 Windows Store 應用程式。
</blockquote>
<br/>
<blockquote>
[!Note]<br />
我們建議您不要使用此函式，而是使用 <a href="/windows/desktop/menurc/resources-functions">資源</a>函式，然後使用 <a href="https://github.com/Microsoft/DirectXTex">DirectXTex</a> 程式庫 (工具) 、 <strong>LOADFROMXXXMEMORY</strong> (其中 XXX 是 WIC、DDS 或 TGA;WIC 不支援 DDS 和 TGA;D3DX 9 支援 TGA 作為遊戲) 的常用藝術來源格式。
</blockquote>
<br/> 抓取資源中指定影像的相關資訊。<br/></td>
</tr>
<tr class="even">
<td><a href="d3dx11loadtexturefromtexture.md"><strong>D3DX11LoadTextureFromTexture</strong></a><br/></td>
<td><blockquote>
[!Note]<br />
D3DX (D3DX 9、D3DX 10 和 D3DX 11) 公用程式庫已針對 Windows 8 淘汰，而且不支援 Windows Store 應用程式。
</blockquote>
<br/>
<blockquote>
[!Note]<br />
我們建議您不要使用此函式，而是使用 <a href="https://github.com/Microsoft/DirectXTex">DirectXTex</a> 程式庫、重 <strong>設大小</strong>、 <strong>轉換</strong>、 <strong>壓縮</strong>、 <strong>解壓縮</strong>和/或 <strong>CopyRectangle</strong>。
</blockquote>
<br/> 從材質載入紋理。<br/></td>
</tr>
<tr class="odd">
<td><a href="d3dx11preprocessshaderfromfile.md"><strong>D3DX11PreprocessShaderFromFile</strong></a><br/></td>
<td><blockquote>
[!Note]<br />
D3DX (D3DX 9、D3DX 10 和 D3DX 11) 公用程式庫已針對 Windows 8 淘汰，而且不支援 Windows Store 應用程式。
</blockquote>
<br/>
<blockquote>
[!Note]<br />
我們建議您不要使用此函式，而是使用 <a href="/windows/desktop/direct3dhlsl/d3dpreprocess"><strong>D3DPreprocess</strong></a> API。
</blockquote>
<br/> 在不編譯的情況下，從檔案建立著色器。<br/></td>
</tr>
<tr class="even">
<td><a href="d3dx11preprocessshaderfrommemory.md"><strong>D3DX11PreprocessShaderFromMemory</strong></a><br/></td>
<td><blockquote>
[!Note]<br />
D3DX (D3DX 9、D3DX 10 和 D3DX 11) 公用程式庫已針對 Windows 8 淘汰，而且不支援 Windows Store 應用程式。
</blockquote>
<br/>
<blockquote>
[!Note]<br />
我們建議您不要使用此函式，而是使用 <a href="/windows/desktop/direct3dhlsl/d3dpreprocess"><strong>D3DPreprocess</strong></a> API。
</blockquote>
<br/> 在不編譯的情況下，從記憶體建立著色器。<br/></td>
</tr>
<tr class="odd">
<td><a href="d3dx11preprocessshaderfromresource.md"><strong>D3DX11PreprocessShaderFromResource</strong></a><br/></td>
<td><blockquote>
[!Note]<br />
D3DX (D3DX 9、D3DX 10 和 D3DX 11) 公用程式庫已針對 Windows 8 淘汰，而且不支援 Windows Store 應用程式。
</blockquote>
<br/>
<blockquote>
[!Note]<br />
我們建議您不要使用此函式，而是使用 <a href="/windows/desktop/direct3dhlsl/d3dpreprocess"><strong>D3DPreprocess</strong></a> API。
</blockquote>
<br/> 從資源建立著色器，而不進行編譯。<br/></td>
</tr>
<tr class="even">
<td><a href="d3dx11savetexturetofile.md"><strong>D3DX11SaveTextureToFile</strong></a><br/></td>
<td><blockquote>
[!Note]<br />
D3DX (D3DX 9、D3DX 10 和 D3DX 11) 公用程式庫已針對 Windows 8 淘汰，而且不支援 Windows Store 應用程式。
</blockquote>
<br/>
<blockquote>
[!Note]<br />
我們建議您不要使用這個函式，而是使用 <a href="https://github.com/Microsoft/DirectXTex">DirectXTex</a> 程式庫， <strong>CaptureTexture</strong> 接著 <strong>SAVETOXXXFILE</strong> (其中 XXX 是 WIC、DDS 或 TGA;WIC 不支援 DDS 和 TGA;D3DX 9 支援 TGA 作為遊戲) 的常用藝術來源格式。 針對從呈現目標材質建立螢幕擷取畫面的簡化案例，建議您使用 <a href="https://github.com/Microsoft/DirectXTK">DirectXTK</a> 程式庫 <strong>SaveDDSTextureToFile</strong> 或 <strong>SaveWICTextureToFile</strong>。
</blockquote>
<br/> 將材質儲存至檔案。<br/></td>
</tr>
<tr class="odd">
<td><a href="d3dx11savetexturetomemory.md"><strong>D3DX11SaveTextureToMemory</strong></a><br/></td>
<td><blockquote>
[!Note]<br />
D3DX (D3DX 9、D3DX 10 和 D3DX 11) 公用程式庫已針對 Windows 8 淘汰，而且不支援 Windows Store 應用程式。
</blockquote>
<br/>
<blockquote>
[!Note]<br />
我們建議您不要使用這個函式，而是使用 <a href="https://github.com/Microsoft/DirectXTex">DirectXTex</a> 程式庫， <strong>CaptureTexture</strong> 接著 <strong>SAVETOXXXMEMORY</strong> (其中 XXX 是 WIC、DDS 或 TGA;WIC 不支援 DDS 和 TGA;D3DX 9 支援 TGA 作為遊戲) 的常用藝術來源格式。
</blockquote>
<br/> 將材質儲存至記憶體。<br/></td>
</tr>
<tr class="even">
<td><a href="d3dx11shprojectcubemap.md"><strong>D3DX11SHProjectCubeMap</strong></a><br/></td>
<td><blockquote>
[!Note]<br />
D3DX (D3DX 9、D3DX 10 和 D3DX 11) 公用程式庫已針對 Windows 8 淘汰，而且不支援 Windows Store 應用程式。
</blockquote>
<br/>
<blockquote>
[!Note]<br />
我們建議您不要使用這個函數，而是使用 <a href="https://github.com/Microsoft/DirectXMath/tree/master/SHMath">球形諧波數學</a> 程式庫 <strong>SHProjectCubeMap</strong>。
</blockquote>
<br/> 將 cube 地圖中表示的函式投射到球面諧波。<br/></td>
</tr>
<tr class="odd">
<td><a href="d3dx11unsetalldeviceobjects.md"><strong>D3DX11UnsetAllDeviceObjects</strong></a><br/></td>
<td><blockquote>
[!Note]<br />
D3DX (D3DX 9、D3DX 10 和 D3DX 11) 公用程式庫已針對 Windows 8 淘汰，而且不支援 Windows Store 應用程式。
</blockquote>
<br/>
<blockquote>
[!Note]<br />
我們建議您使用 <a href="/windows/desktop/api/D3D11/nf-d3d11-id3d11devicecontext-clearstate"><strong>>id3d11devicecoNtext：： ClearState</strong></a> 方法，而不是使用此函數。
</blockquote>
<br/> 將所有資源的指標設為 <strong>Null</strong>，以移除裝置中的所有資源。 這應該會在應用程式關閉時呼叫。 這有助於確保當某個資源釋出所有資源時，都不會將這些資源系結至裝置。<br/></td>
</tr>
</tbody>
</table>



 

## <a name="related-topics"></a>相關主題

<dl> <dt>

[D3DX 11 參考](d3d11-graphics-reference-d3dx11.md)
</dt> </dl>

 

