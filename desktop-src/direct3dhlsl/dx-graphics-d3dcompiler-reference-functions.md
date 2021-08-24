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
ms.openlocfilehash: 43d9bf2feb572d7b410d702dbc456af7c18be0ee
ms.sourcegitcommit: 9b5faa61c38b2d0c432b7f2dbee8c127b0e28a7e
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/19/2021
ms.locfileid: "122465805"
---
# <a name="compiler-functions-hlsl-reference"></a>編譯器函數 (HLSL 參考) 

本節包含下列 Direct3D HLSL 編譯器函數的相關資訊：

## <a name="in-this-section"></a>本節內容




| 主題 | 描述 | 
|-------|-------------|
| <a href="d3d11reflect.md"><strong>D3D11Reflect</strong></a><br /> | 取得反映介面的指標。<br /> | 
| <a href="/windows/win32/api/d3dcompiler/nf-d3dcompiler-d3dcompile"><strong>D3DCompile</strong></a><br /> | 將 HLSL 程式碼或效果檔案編譯為指定目標的位元組程式碼。<br /> | 
| <a href="/windows/win32/api/d3dcompiler/nf-d3dcompiler-d3dcompile2"><strong>D3DCompile2</strong></a><br /> | 將 Microsoft 高階著色器語言 (HLSL) 程式碼為指定目標的位元組程式碼。<br /> | 
| <a href="/windows/win32/api/d3dcompiler/nf-d3dcompiler-d3dcompilefromfile"><strong>D3DCompileFromFile</strong></a><br /> | <blockquote>[!Note]<br />您可以使用此 API 來開發 Windows 存放區應用程式，但無法在您提交至 Windows 存放區的應用程式中使用它。 Refer to the section, "Compiling shaders for UWP", in the remarks for <a href="/windows/win32/api/d3dcompiler/nf-d3dcompiler-d3dcompile2"><strong>D3DCompile2</strong></a>.</blockquote><br /> 將 HLSL 程式碼編譯為指定目標的位元組程式碼。<br /> | 
| <a href="/windows/win32/api/d3dcompiler/nf-d3dcompiler-d3dcompressshaders"><strong>D3DCompressShaders</strong></a><br /> | <blockquote>[!Note]<br />您可以使用此 API 來開發 Windows 存放區應用程式，但無法在您提交至 Windows 存放區的應用程式中使用它。</blockquote><br /> 將一組著色器壓縮成更精簡的表單。 <br /> | 
| <a href="/windows/win32/api/d3dcompiler/nf-d3dcompiler-d3dcreateblob"><strong>D3DCreateBlob</strong></a><br /> | 建立緩衝區。<br /> | 
| <a href="/windows/desktop/api/D3Dcompiler/nf-d3dcompiler-d3dcreatefunctionlinkinggraph"><strong>D3DCreateFunctionLinkingGraph</strong></a><br /> | 建立函數連結圖形介面。 <br /><blockquote>[!Note]<br />此函式是 HLSL 著色器連結技術的一部分，可讓您在所有 Direct3D 11 平臺上用來建立先行編譯的 HLSL 函式、將它們封裝至程式庫，並在執行時間將它們連結到完整的著色器。</blockquote><br /> | 
| <a href="/windows/desktop/api/D3Dcompiler/nf-d3dcompiler-d3dcreatelinker"><strong>D3DCreateLinker</strong></a><br /> | 建立連結器介面。 <br /><blockquote>[!Note]<br />此函式是 HLSL 著色器連結技術的一部分，可讓您在所有 Direct3D 11 平臺上用來建立先行編譯的 HLSL 函式、將它們封裝至程式庫，並在執行時間將它們連結到完整的著色器。</blockquote><br /> | 
| <a href="/windows/win32/api/d3dcompiler/nf-d3dcompiler-d3ddecompressshaders"><strong>D3DDecompressShaders</strong></a><br /> | <blockquote>[!Note]<br />您可以使用此 API 來開發 Windows 存放區應用程式，但無法在您提交至 Windows 存放區的應用程式中使用它。</blockquote><br /> 從壓縮的集合解壓縮一或多個著色器。 <br /> | 
| <a href="/windows/win32/api/d3dcompiler/nf-d3dcompiler-d3ddisassemble"><strong>D3DDisassemble</strong></a><br /> | 反組譯已編譯的 HLSL 程式碼。<br /> | 
| <a href="/windows/win32/api/d3dcompiler/nf-d3dcompiler-d3ddisassemble10effect"><strong>D3DDisassemble10Effect</strong></a><br /> | 從 Direct3D10 效果反組譯已編譯的 HLSL 程式碼。<br /> | 
| <a href="/windows/win32/api/d3d11shadertracing/nf-d3d11shadertracing-d3ddisassemble11trace"><strong>D3DDisassemble11Trace</strong></a><br /> | 反組譯追蹤步驟所指定的已編譯 HLSL 程式碼區段。<br /> | 
| <a href="/windows/win32/api/d3dcompiler/nf-d3dcompiler-d3ddisassembleregion"><strong>D3DDisassembleRegion</strong></a><br /> | 反組譯出已編譯 HLSL 程式碼的特定區域。<br /> | 
| <a href="/windows/win32/api/d3dcompiler/nf-d3dcompiler-d3dgetblobpart"><strong>D3DGetBlobPart</strong></a><br /> | 從編譯結果中取出特定部分。<br /> | 
| <a href="/windows/win32/api/d3dcompiler/nf-d3dcompiler-d3dgetdebuginfo"><strong>D3DGetDebugInfo</strong></a><br /> | <blockquote>[!Note]<br />您可以使用此 API 來開發 Windows 存放區應用程式，但無法在您提交至 Windows 存放區的應用程式中使用它。</blockquote><br /> 取得著色器的調試資訊。<br /> | 
| <a href="/windows/win32/api/d3dcompiler/nf-d3dcompiler-d3dgetinputandoutputsignatureblob"><strong>D3DGetInputAndOutputSignatureBlob</strong></a><br /> | <blockquote>[!Note]<br /><a href="/windows/win32/api/d3dcompiler/nf-d3dcompiler-d3dgetinputandoutputsignatureblob"><strong>D3DGetInputAndOutputSignatureBlob</strong></a>可能會在 Windows 8.1 之後變更或無法使用。 請改為搭配<a href="/windows/win32/api/d3dcompiler/ne-d3dcompiler-d3d_blob_part"><strong>D3D_BLOB_INPUT_AND_OUTPUT_SIGNATURE_BLOB</strong></a>值使用<a href="/windows/win32/api/d3dcompiler/nf-d3dcompiler-d3dgetblobpart"><strong>D3DGetBlobPart</strong></a> 。</blockquote><br /> 從編譯結果取得輸入和輸出簽章。<br /> | 
| [<strong>D3DGetInputSignatureBlob</strong>](/windows/win32/api/d3dcompiler/nf-d3dcompiler-d3dgetinputsignatureblob)<br /> | <blockquote>[!Note]<br /><a href="/windows/win32/api/d3dcompiler/nf-d3dcompiler-d3dgetinputsignatureblob"><strong>D3DGetInputSignatureBlob</strong></a>可能會在 Windows 8.1 之後變更或無法使用。 請改為搭配<a href="/windows/win32/api/d3dcompiler/ne-d3dcompiler-d3d_blob_part"><strong>D3D_BLOB_INPUT_SIGNATURE_BLOB</strong></a>值使用<a href="/windows/win32/api/d3dcompiler/nf-d3dcompiler-d3dgetblobpart"><strong>D3DGetBlobPart</strong></a> 。</blockquote><br /> 從編譯結果取得輸入簽章。<br /> | 
| <a href="/windows/win32/api/d3dcompiler/nf-d3dcompiler-d3dgetoutputsignatureblob"><strong>D3DGetOutputSignatureBlob</strong></a><br /> | <blockquote>[!Note]<br /><a href="/windows/win32/api/d3dcompiler/nf-d3dcompiler-d3dgetoutputsignatureblob"><strong>D3DGetOutputSignatureBlob</strong></a>可能會在 Windows 8.1 之後變更或無法使用。 請改為搭配<a href="/windows/win32/api/d3dcompiler/ne-d3dcompiler-d3d_blob_part"><strong>D3D_BLOB_OUTPUT_SIGNATURE_BLOB</strong></a>值使用<a href="/windows/win32/api/d3dcompiler/nf-d3dcompiler-d3dgetblobpart"><strong>D3DGetBlobPart</strong></a> 。</blockquote><br /> 從編譯結果取得輸出簽章。<br /> | 
| <a href="/windows/win32/api/d3dcompiler/nf-d3dcompiler-d3dgettraceinstructionoffsets"><strong>D3DGetTraceInstructionOffsets</strong></a><br /> | 抓取著色器程式碼區段內的指示位元組位移。<br /> | 
| <a href="/windows/desktop/api/D3Dcompiler/nf-d3dcompiler-d3dloadmodule"><strong>D3DLoadModule</strong></a><br /> | 從著色器模組的來源資料建立著色器模組介面。 <br /><blockquote>[!Note]<br />此函式是 HLSL 著色器連結技術的一部分，可讓您在所有 Direct3D 11 平臺上用來建立先行編譯的 HLSL 函式、將它們封裝至程式庫，並在執行時間將它們連結到完整的著色器。</blockquote><br /> | 
| <a href="/windows/win32/api/d3dcompiler/nf-d3dcompiler-d3dpreprocess"><strong>D3DPreprocess</strong></a><br /> | 未編譯的 HLSL 程式碼。<br /> | 
| <a href="/windows/win32/api/d3dcompiler/nf-d3dcompiler-d3dreadfiletoblob"><strong>D3DReadFileToBlob</strong></a><br /> | <blockquote>[!Note]<br />您可以使用此 API 來開發 Windows 存放區應用程式，但無法在您提交至 Windows 存放區的應用程式中使用它。</blockquote><br /> 將磁片上的檔案讀取到記憶體中。<br /> | 
| <a href="/windows/win32/api/d3dcompiler/nf-d3dcompiler-d3dreflect"><strong>D3DReflect</strong></a><br /> | 取得反映介面的指標。<br /> | 
| <a href="/windows/desktop/api/D3Dcompiler/nf-d3dcompiler-d3dreflectlibrary"><strong>D3DReflectLibrary</strong></a><br /> | 從包含函式 HLSL 程式庫的來源資料建立程式庫反映介面。 <br /><blockquote>[!Note]<br />此函式是 HLSL 著色器連結技術的一部分，可讓您在所有 Direct3D 11 平臺上用來建立先行編譯的 HLSL 函式、將它們封裝至程式庫，並在執行時間將它們連結到完整的著色器。</blockquote><br /> | 
| <a href="/windows/win32/api/d3dcompiler/nf-d3dcompiler-d3dsetblobpart"><strong>D3DSetBlobPart</strong></a><br /> | 設定編譯結果中的資訊。<br /> | 
| <a href="/windows/win32/api/d3dcompiler/nf-d3dcompiler-d3dstripshader"><strong>D3DStripShader</strong></a><br /> | 從編譯結果中移除不需要的 blob。<br /> | 
| <a href="/windows/win32/api/d3dcompiler/nf-d3dcompiler-d3dwriteblobtofile"><strong>D3DWriteBlobToFile</strong></a><br /> | <blockquote>[!Note]<br />您可以使用此 API 來開發 Windows 存放區應用程式，但無法在您提交至 Windows 存放區的應用程式中使用它。</blockquote><br /> 將記憶體 blob 寫入磁片上的檔案。<br /> | 




 

## <a name="related-topics"></a>相關主題

<dl> <dt>

[D3DCompiler 參考](dx-graphics-d3dcompiler-reference.md)
</dt> </dl>

