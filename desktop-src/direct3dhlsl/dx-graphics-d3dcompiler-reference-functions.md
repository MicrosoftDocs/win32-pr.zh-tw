---
title: '編譯器函數 (HLSL 參考) '
description: 本節包含下列 Direct3D HLSL 編譯器函數的相關資訊
ms.assetid: aacc5207-3ec8-4031-b5c9-f7c0fb7b7095
keywords:
- 函數，編譯器
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- apiref
api_name: ''
api_type: ''
api_location: ''
ms.openlocfilehash: ee63fa17cc9216fdb92f69fed4d77bc65bb49048
ms.sourcegitcommit: 11f52354f570aacaf1ba2a266b2e507abd73352a
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 03/19/2021
ms.locfileid: "104974785"
---
# <a name="compiler-functions-hlsl-reference"></a>編譯器函數 (HLSL 參考) 

本節包含下列 Direct3D HLSL 編譯器函數的相關資訊：

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
<td><a href="d3d11reflect.md"><strong>D3D11Reflect</strong></a><br/></td>
<td>取得反映介面的指標。<br/></td>
</tr>
<tr class="even">
<td><a href="/windows/win32/api/d3dcompiler/nf-d3dcompiler-d3dcompile"><strong>D3DCompile</strong></a><br/></td>
<td>將 HLSL 程式碼或效果檔案編譯為指定目標的位元組程式碼。<br/></td>
</tr>
<tr class="odd">
<td><a href="/windows/win32/api/d3dcompiler/nf-d3dcompiler-d3dcompile2"><strong>D3DCompile2</strong></a><br/></td>
<td>將 Microsoft 高階著色器語言 (HLSL) 程式碼為指定目標的位元組程式碼。<br/></td>
</tr>
<tr class="even">
<td><a href="/windows/win32/api/d3dcompiler/nf-d3dcompiler-d3dcompilefromfile"><strong>D3DCompileFromFile</strong></a><br/></td>
<td><blockquote>
[!Note]<br />
您可以使用此 API 來開發 Windows Store 應用程式，但不能將它用於提交至 Windows Store 的應用程式。 Refer to the section, &quot;Compiling shaders for UWP&quot;, in the remarks for <a href="/windows/win32/api/d3dcompiler/nf-d3dcompiler-d3dcompile2"><strong>D3DCompile2</strong></a>.
</blockquote>
<br/> 將 HLSL 程式碼編譯為指定目標的位元組程式碼。<br/></td>
</tr>
<tr class="odd">
<td><a href="/windows/win32/api/d3dcompiler/nf-d3dcompiler-d3dcompressshaders"><strong>D3DCompressShaders</strong></a><br/></td>
<td><blockquote>
[!Note]<br />
您可以使用此 API 來開發 Windows Store 應用程式，但不能將它用於提交至 Windows Store 的應用程式。
</blockquote>
<br/> 將一組著色器壓縮成更精簡的表單。 <br/></td>
</tr>
<tr class="even">
<td><a href="/windows/win32/api/d3dcompiler/nf-d3dcompiler-d3dcreateblob"><strong>D3DCreateBlob</strong></a><br/></td>
<td>建立緩衝區。<br/></td>
</tr>
<tr class="odd">
<td><a href="/windows/desktop/api/D3Dcompiler/nf-d3dcompiler-d3dcreatefunctionlinkinggraph"><strong>D3DCreateFunctionLinkingGraph</strong></a><br/></td>
<td>建立函數連結圖形介面。 <br/>
<blockquote>
[!Note]<br />
此函式是 HLSL 著色器連結技術的一部分，可讓您在所有 Direct3D 11 平臺上用來建立先行編譯的 HLSL 函式、將它們封裝至程式庫，並在執行時間將它們連結到完整的著色器。
</blockquote>
<br/></td>
</tr>
<tr class="even">
<td><a href="/windows/desktop/api/D3Dcompiler/nf-d3dcompiler-d3dcreatelinker"><strong>D3DCreateLinker</strong></a><br/></td>
<td>建立連結器介面。 <br/>
<blockquote>
[!Note]<br />
此函式是 HLSL 著色器連結技術的一部分，可讓您在所有 Direct3D 11 平臺上用來建立先行編譯的 HLSL 函式、將它們封裝至程式庫，並在執行時間將它們連結到完整的著色器。
</blockquote>
<br/></td>
</tr>
<tr class="odd">
<td><a href="/windows/win32/api/d3dcompiler/nf-d3dcompiler-d3ddecompressshaders"><strong>D3DDecompressShaders</strong></a><br/></td>
<td><blockquote>
[!Note]<br />
您可以使用此 API 來開發 Windows Store 應用程式，但不能將它用於提交至 Windows Store 的應用程式。
</blockquote>
<br/> 從壓縮的集合解壓縮一或多個著色器。 <br/></td>
</tr>
<tr class="even">
<td><a href="/windows/win32/api/d3dcompiler/nf-d3dcompiler-d3ddisassemble"><strong>D3DDisassemble</strong></a><br/></td>
<td>反組譯已編譯的 HLSL 程式碼。<br/></td>
</tr>
<tr class="odd">
<td><a href="/windows/win32/api/d3dcompiler/nf-d3dcompiler-d3ddisassemble10effect"><strong>D3DDisassemble10Effect</strong></a><br/></td>
<td>從 Direct3D10 效果反組譯已編譯的 HLSL 程式碼。<br/></td>
</tr>
<tr class="even">
<td><a href="/windows/win32/api/d3d11shadertracing/nf-d3d11shadertracing-d3ddisassemble11trace"><strong>D3DDisassemble11Trace</strong></a><br/></td>
<td>反組譯追蹤步驟所指定的已編譯 HLSL 程式碼區段。<br/></td>
</tr>
<tr class="odd">
<td><a href="/windows/win32/api/d3dcompiler/nf-d3dcompiler-d3ddisassembleregion"><strong>D3DDisassembleRegion</strong></a><br/></td>
<td>反組譯出已編譯 HLSL 程式碼的特定區域。<br/></td>
</tr>
<tr class="even">
<td><a href="/windows/win32/api/d3dcompiler/nf-d3dcompiler-d3dgetblobpart"><strong>D3DGetBlobPart</strong></a><br/></td>
<td>從編譯結果中取出特定部分。<br/></td>
</tr>
<tr class="odd">
<td><a href="/windows/win32/api/d3dcompiler/nf-d3dcompiler-d3dgetdebuginfo"><strong>D3DGetDebugInfo</strong></a><br/></td>
<td><blockquote>
[!Note]<br />
您可以使用此 API 來開發 Windows Store 應用程式，但不能將它用於提交至 Windows Store 的應用程式。
</blockquote>
<br/> 取得著色器的調試資訊。<br/></td>
</tr>
<tr class="even">
<td><a href="/windows/win32/api/d3dcompiler/nf-d3dcompiler-d3dgetinputandoutputsignatureblob"><strong>D3DGetInputAndOutputSignatureBlob</strong></a><br/></td>
<td><blockquote>
[!Note]<br />
<a href="/windows/win32/api/d3dcompiler/nf-d3dcompiler-d3dgetinputandoutputsignatureblob"><strong>D3DGetInputAndOutputSignatureBlob</strong></a> 可能會在 Windows 8.1 之後變更或無法使用。 請改為搭配<a href="/windows/win32/api/d3dcompiler/ne-d3dcompiler-d3d_blob_part"><strong>D3D_BLOB_INPUT_AND_OUTPUT_SIGNATURE_BLOB</strong></a>值使用<a href="/windows/win32/api/d3dcompiler/nf-d3dcompiler-d3dgetblobpart"><strong>D3DGetBlobPart</strong></a> 。
</blockquote>
<br/> 從編譯結果取得輸入和輸出簽章。<br/></td>
</tr>
<tr class="odd">
<td>[<strong>D3DGetInputSignatureBlob</strong>] (/windows/win32/api/d3dcompiler/nf-d3dcompiler-d3dgetinputsignatureblob) <br/></td>
<td><blockquote>
[!Note]<br />
<a href="/windows/win32/api/d3dcompiler/nf-d3dcompiler-d3dgetinputsignatureblob"><strong>D3DGetInputSignatureBlob</strong></a> 可能會在 Windows 8.1 之後變更或無法使用。 請改為搭配<a href="/windows/win32/api/d3dcompiler/ne-d3dcompiler-d3d_blob_part"><strong>D3D_BLOB_INPUT_SIGNATURE_BLOB</strong></a>值使用<a href="/windows/win32/api/d3dcompiler/nf-d3dcompiler-d3dgetblobpart"><strong>D3DGetBlobPart</strong></a> 。
</blockquote>
<br/> 從編譯結果取得輸入簽章。<br/></td>
</tr>
<tr class="even">
<td><a href="/windows/win32/api/d3dcompiler/nf-d3dcompiler-d3dgetoutputsignatureblob"><strong>D3DGetOutputSignatureBlob</strong></a><br/></td>
<td><blockquote>
[!Note]<br />
<a href="/windows/win32/api/d3dcompiler/nf-d3dcompiler-d3dgetoutputsignatureblob"><strong>D3DGetOutputSignatureBlob</strong></a> 可能會在 Windows 8.1 之後變更或無法使用。 請改為搭配<a href="/windows/win32/api/d3dcompiler/ne-d3dcompiler-d3d_blob_part"><strong>D3D_BLOB_OUTPUT_SIGNATURE_BLOB</strong></a>值使用<a href="/windows/win32/api/d3dcompiler/nf-d3dcompiler-d3dgetblobpart"><strong>D3DGetBlobPart</strong></a> 。
</blockquote>
<br/> 從編譯結果取得輸出簽章。<br/></td>
</tr>
<tr class="odd">
<td><a href="/windows/win32/api/d3dcompiler/nf-d3dcompiler-d3dgettraceinstructionoffsets"><strong>D3DGetTraceInstructionOffsets</strong></a><br/></td>
<td>抓取著色器程式碼區段內的指示位元組位移。<br/></td>
</tr>
<tr class="even">
<td><a href="/windows/desktop/api/D3Dcompiler/nf-d3dcompiler-d3dloadmodule"><strong>D3DLoadModule</strong></a><br/></td>
<td>從著色器模組的來源資料建立著色器模組介面。 <br/>
<blockquote>
[!Note]<br />
此函式是 HLSL 著色器連結技術的一部分，可讓您在所有 Direct3D 11 平臺上用來建立先行編譯的 HLSL 函式、將它們封裝至程式庫，並在執行時間將它們連結到完整的著色器。
</blockquote>
<br/></td>
</tr>
<tr class="odd">
<td><a href="/windows/win32/api/d3dcompiler/nf-d3dcompiler-d3dpreprocess"><strong>D3DPreprocess</strong></a><br/></td>
<td>未編譯的 HLSL 程式碼。<br/></td>
</tr>
<tr class="even">
<td><a href="/windows/win32/api/d3dcompiler/nf-d3dcompiler-d3dreadfiletoblob"><strong>D3DReadFileToBlob</strong></a><br/></td>
<td><blockquote>
[!Note]<br />
您可以使用此 API 來開發 Windows Store 應用程式，但不能將它用於提交至 Windows Store 的應用程式。
</blockquote>
<br/> 將磁片上的檔案讀取到記憶體中。<br/></td>
</tr>
<tr class="odd">
<td><a href="/windows/win32/api/d3dcompiler/nf-d3dcompiler-d3dreflect"><strong>D3DReflect</strong></a><br/></td>
<td>取得反映介面的指標。<br/></td>
</tr>
<tr class="even">
<td><a href="/windows/desktop/api/D3Dcompiler/nf-d3dcompiler-d3dreflectlibrary"><strong>D3DReflectLibrary</strong></a><br/></td>
<td>從包含函式 HLSL 程式庫的來源資料建立程式庫反映介面。 <br/>
<blockquote>
[!Note]<br />
此函式是 HLSL 著色器連結技術的一部分，可讓您在所有 Direct3D 11 平臺上用來建立先行編譯的 HLSL 函式、將它們封裝至程式庫，並在執行時間將它們連結到完整的著色器。
</blockquote>
<br/></td>
</tr>
<tr class="odd">
<td><a href="/windows/win32/api/d3dcompiler/nf-d3dcompiler-d3dsetblobpart"><strong>D3DSetBlobPart</strong></a><br/></td>
<td>設定編譯結果中的資訊。<br/></td>
</tr>
<tr class="even">
<td><a href="/windows/win32/api/d3dcompiler/nf-d3dcompiler-d3dstripshader"><strong>D3DStripShader</strong></a><br/></td>
<td>從編譯結果中移除不需要的 blob。<br/></td>
</tr>
<tr class="odd">
<td><a href="/windows/win32/api/d3dcompiler/nf-d3dcompiler-d3dwriteblobtofile"><strong>D3DWriteBlobToFile</strong></a><br/></td>
<td><blockquote>
[!Note]<br />
您可以使用此 API 來開發 Windows Store 應用程式，但不能將它用於提交至 Windows Store 的應用程式。
</blockquote>
<br/> 將記憶體 blob 寫入磁片上的檔案。<br/></td>
</tr>
</tbody>
</table>



 

## <a name="related-topics"></a>相關主題

<dl> <dt>

[D3DCompiler 參考](dx-graphics-d3dcompiler-reference.md)
</dt> </dl>

