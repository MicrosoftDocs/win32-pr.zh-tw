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
# <a name="compiler-functions-hlsl-reference"></a><span data-ttu-id="383a6-104">編譯器函數 (HLSL 參考) </span><span class="sxs-lookup"><span data-stu-id="383a6-104">Compiler functions (HLSL reference)</span></span>

<span data-ttu-id="383a6-105">本節包含下列 Direct3D HLSL 編譯器函數的相關資訊：</span><span class="sxs-lookup"><span data-stu-id="383a6-105">This section contains information about the following Direct3D HLSL compiler functions:</span></span>

## <a name="in-this-section"></a><span data-ttu-id="383a6-106">本節內容</span><span class="sxs-lookup"><span data-stu-id="383a6-106">In this section</span></span>



<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<thead>
<tr class="header">
<th><span data-ttu-id="383a6-107">主題</span><span class="sxs-lookup"><span data-stu-id="383a6-107">Topic</span></span></th>
<th><span data-ttu-id="383a6-108">描述</span><span class="sxs-lookup"><span data-stu-id="383a6-108">Description</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><span data-ttu-id="383a6-109"><a href="d3d11reflect.md"><strong>D3D11Reflect</strong></a></span><span class="sxs-lookup"><span data-stu-id="383a6-109"><a href="d3d11reflect.md"><strong>D3D11Reflect</strong></a></span></span><br/></td>
<td><span data-ttu-id="383a6-110">取得反映介面的指標。</span><span class="sxs-lookup"><span data-stu-id="383a6-110">Gets a pointer to a reflection interface.</span></span><br/></td>
</tr>
<tr class="even">
<td><span data-ttu-id="383a6-111"><a href="/windows/win32/api/d3dcompiler/nf-d3dcompiler-d3dcompile"><strong>D3DCompile</strong></a></span><span class="sxs-lookup"><span data-stu-id="383a6-111"><a href="/windows/win32/api/d3dcompiler/nf-d3dcompiler-d3dcompile"><strong>D3DCompile</strong></a></span></span><br/></td>
<td><span data-ttu-id="383a6-112">將 HLSL 程式碼或效果檔案編譯為指定目標的位元組程式碼。</span><span class="sxs-lookup"><span data-stu-id="383a6-112">Compile HLSL code or an effect file into bytecode for a given target.</span></span><br/></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="383a6-113"><a href="/windows/win32/api/d3dcompiler/nf-d3dcompiler-d3dcompile2"><strong>D3DCompile2</strong></a></span><span class="sxs-lookup"><span data-stu-id="383a6-113"><a href="/windows/win32/api/d3dcompiler/nf-d3dcompiler-d3dcompile2"><strong>D3DCompile2</strong></a></span></span><br/></td>
<td><span data-ttu-id="383a6-114">將 Microsoft 高階著色器語言 (HLSL) 程式碼為指定目標的位元組程式碼。</span><span class="sxs-lookup"><span data-stu-id="383a6-114">Compiles Microsoft High Level Shader Language (HLSL) code into bytecode for a given target.</span></span><br/></td>
</tr>
<tr class="even">
<td><span data-ttu-id="383a6-115"><a href="/windows/win32/api/d3dcompiler/nf-d3dcompiler-d3dcompilefromfile"><strong>D3DCompileFromFile</strong></a></span><span class="sxs-lookup"><span data-stu-id="383a6-115"><a href="/windows/win32/api/d3dcompiler/nf-d3dcompiler-d3dcompilefromfile"><strong>D3DCompileFromFile</strong></a></span></span><br/></td>
<td><blockquote>
[!Note]<br />
<span data-ttu-id="383a6-116">您可以使用此 API 來開發 Windows Store 應用程式，但不能將它用於提交至 Windows Store 的應用程式。</span><span class="sxs-lookup"><span data-stu-id="383a6-116">You can use this API to develop your Windows Store apps, but you can't use it in apps that you submit to the Windows Store.</span></span> <span data-ttu-id="383a6-117">Refer to the section, &quot;Compiling shaders for UWP&quot;, in the remarks for <a href="/windows/win32/api/d3dcompiler/nf-d3dcompiler-d3dcompile2"><strong>D3DCompile2</strong></a>.</span><span class="sxs-lookup"><span data-stu-id="383a6-117">Refer to the section, &quot;Compiling shaders for UWP&quot;, in the remarks for <a href="/windows/win32/api/d3dcompiler/nf-d3dcompiler-d3dcompile2"><strong>D3DCompile2</strong></a>.</span></span>
</blockquote>
<br/> <span data-ttu-id="383a6-118">將 HLSL 程式碼編譯為指定目標的位元組程式碼。</span><span class="sxs-lookup"><span data-stu-id="383a6-118">Compiles HLSL code into bytecode for a given target.</span></span><br/></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="383a6-119"><a href="/windows/win32/api/d3dcompiler/nf-d3dcompiler-d3dcompressshaders"><strong>D3DCompressShaders</strong></a></span><span class="sxs-lookup"><span data-stu-id="383a6-119"><a href="/windows/win32/api/d3dcompiler/nf-d3dcompiler-d3dcompressshaders"><strong>D3DCompressShaders</strong></a></span></span><br/></td>
<td><blockquote>
[!Note]<br />
<span data-ttu-id="383a6-120">您可以使用此 API 來開發 Windows Store 應用程式，但不能將它用於提交至 Windows Store 的應用程式。</span><span class="sxs-lookup"><span data-stu-id="383a6-120">You can use this API to develop your Windows Store apps, but you can't use it in apps that you submit to the Windows Store.</span></span>
</blockquote>
<br/> <span data-ttu-id="383a6-121">將一組著色器壓縮成更精簡的表單。</span><span class="sxs-lookup"><span data-stu-id="383a6-121">Compresses a set of shaders into a more compact form.</span></span> <br/></td>
</tr>
<tr class="even">
<td><span data-ttu-id="383a6-122"><a href="/windows/win32/api/d3dcompiler/nf-d3dcompiler-d3dcreateblob"><strong>D3DCreateBlob</strong></a></span><span class="sxs-lookup"><span data-stu-id="383a6-122"><a href="/windows/win32/api/d3dcompiler/nf-d3dcompiler-d3dcreateblob"><strong>D3DCreateBlob</strong></a></span></span><br/></td>
<td><span data-ttu-id="383a6-123">建立緩衝區。</span><span class="sxs-lookup"><span data-stu-id="383a6-123">Creates a buffer.</span></span><br/></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="383a6-124"><a href="/windows/desktop/api/D3Dcompiler/nf-d3dcompiler-d3dcreatefunctionlinkinggraph"><strong>D3DCreateFunctionLinkingGraph</strong></a></span><span class="sxs-lookup"><span data-stu-id="383a6-124"><a href="/windows/desktop/api/D3Dcompiler/nf-d3dcompiler-d3dcreatefunctionlinkinggraph"><strong>D3DCreateFunctionLinkingGraph</strong></a></span></span><br/></td>
<td><span data-ttu-id="383a6-125">建立函數連結圖形介面。</span><span class="sxs-lookup"><span data-stu-id="383a6-125">Creates a function-linking-graph interface.</span></span> <br/>
<blockquote>
[!Note]<br />
<span data-ttu-id="383a6-126">此函式是 HLSL 著色器連結技術的一部分，可讓您在所有 Direct3D 11 平臺上用來建立先行編譯的 HLSL 函式、將它們封裝至程式庫，並在執行時間將它們連結到完整的著色器。</span><span class="sxs-lookup"><span data-stu-id="383a6-126">This function is part of the HLSL shader linking technology that you can use on all Direct3D 11 platforms to create precompiled HLSL functions, package them into libraries, and link them into full shaders at run time.</span></span>
</blockquote>
<br/></td>
</tr>
<tr class="even">
<td><span data-ttu-id="383a6-127"><a href="/windows/desktop/api/D3Dcompiler/nf-d3dcompiler-d3dcreatelinker"><strong>D3DCreateLinker</strong></a></span><span class="sxs-lookup"><span data-stu-id="383a6-127"><a href="/windows/desktop/api/D3Dcompiler/nf-d3dcompiler-d3dcreatelinker"><strong>D3DCreateLinker</strong></a></span></span><br/></td>
<td><span data-ttu-id="383a6-128">建立連結器介面。</span><span class="sxs-lookup"><span data-stu-id="383a6-128">Creates a linker interface.</span></span> <br/>
<blockquote>
[!Note]<br />
<span data-ttu-id="383a6-129">此函式是 HLSL 著色器連結技術的一部分，可讓您在所有 Direct3D 11 平臺上用來建立先行編譯的 HLSL 函式、將它們封裝至程式庫，並在執行時間將它們連結到完整的著色器。</span><span class="sxs-lookup"><span data-stu-id="383a6-129">This function is part of the HLSL shader linking technology that you can use on all Direct3D 11 platforms to create precompiled HLSL functions, package them into libraries, and link them into full shaders at run time.</span></span>
</blockquote>
<br/></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="383a6-130"><a href="/windows/win32/api/d3dcompiler/nf-d3dcompiler-d3ddecompressshaders"><strong>D3DDecompressShaders</strong></a></span><span class="sxs-lookup"><span data-stu-id="383a6-130"><a href="/windows/win32/api/d3dcompiler/nf-d3dcompiler-d3ddecompressshaders"><strong>D3DDecompressShaders</strong></a></span></span><br/></td>
<td><blockquote>
[!Note]<br />
<span data-ttu-id="383a6-131">您可以使用此 API 來開發 Windows Store 應用程式，但不能將它用於提交至 Windows Store 的應用程式。</span><span class="sxs-lookup"><span data-stu-id="383a6-131">You can use this API to develop your Windows Store apps, but you can't use it in apps that you submit to the Windows Store.</span></span>
</blockquote>
<br/> <span data-ttu-id="383a6-132">從壓縮的集合解壓縮一或多個著色器。</span><span class="sxs-lookup"><span data-stu-id="383a6-132">Decompresses one or more shaders from a compressed set.</span></span> <br/></td>
</tr>
<tr class="even">
<td><span data-ttu-id="383a6-133"><a href="/windows/win32/api/d3dcompiler/nf-d3dcompiler-d3ddisassemble"><strong>D3DDisassemble</strong></a></span><span class="sxs-lookup"><span data-stu-id="383a6-133"><a href="/windows/win32/api/d3dcompiler/nf-d3dcompiler-d3ddisassemble"><strong>D3DDisassemble</strong></a></span></span><br/></td>
<td><span data-ttu-id="383a6-134">反組譯已編譯的 HLSL 程式碼。</span><span class="sxs-lookup"><span data-stu-id="383a6-134">Disassembles compiled HLSL code.</span></span><br/></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="383a6-135"><a href="/windows/win32/api/d3dcompiler/nf-d3dcompiler-d3ddisassemble10effect"><strong>D3DDisassemble10Effect</strong></a></span><span class="sxs-lookup"><span data-stu-id="383a6-135"><a href="/windows/win32/api/d3dcompiler/nf-d3dcompiler-d3ddisassemble10effect"><strong>D3DDisassemble10Effect</strong></a></span></span><br/></td>
<td><span data-ttu-id="383a6-136">從 Direct3D10 效果反組譯已編譯的 HLSL 程式碼。</span><span class="sxs-lookup"><span data-stu-id="383a6-136">Disassembles compiled HLSL code from a Direct3D10 effect.</span></span><br/></td>
</tr>
<tr class="even">
<td><span data-ttu-id="383a6-137"><a href="/windows/win32/api/d3d11shadertracing/nf-d3d11shadertracing-d3ddisassemble11trace"><strong>D3DDisassemble11Trace</strong></a></span><span class="sxs-lookup"><span data-stu-id="383a6-137"><a href="/windows/win32/api/d3d11shadertracing/nf-d3d11shadertracing-d3ddisassemble11trace"><strong>D3DDisassemble11Trace</strong></a></span></span><br/></td>
<td><span data-ttu-id="383a6-138">反組譯追蹤步驟所指定的已編譯 HLSL 程式碼區段。</span><span class="sxs-lookup"><span data-stu-id="383a6-138">Disassembles a section of compiled HLSL code that is specified by shader trace steps.</span></span><br/></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="383a6-139"><a href="/windows/win32/api/d3dcompiler/nf-d3dcompiler-d3ddisassembleregion"><strong>D3DDisassembleRegion</strong></a></span><span class="sxs-lookup"><span data-stu-id="383a6-139"><a href="/windows/win32/api/d3dcompiler/nf-d3dcompiler-d3ddisassembleregion"><strong>D3DDisassembleRegion</strong></a></span></span><br/></td>
<td><span data-ttu-id="383a6-140">反組譯出已編譯 HLSL 程式碼的特定區域。</span><span class="sxs-lookup"><span data-stu-id="383a6-140">Disassembles a specific region of compiled HLSL code.</span></span><br/></td>
</tr>
<tr class="even">
<td><span data-ttu-id="383a6-141"><a href="/windows/win32/api/d3dcompiler/nf-d3dcompiler-d3dgetblobpart"><strong>D3DGetBlobPart</strong></a></span><span class="sxs-lookup"><span data-stu-id="383a6-141"><a href="/windows/win32/api/d3dcompiler/nf-d3dcompiler-d3dgetblobpart"><strong>D3DGetBlobPart</strong></a></span></span><br/></td>
<td><span data-ttu-id="383a6-142">從編譯結果中取出特定部分。</span><span class="sxs-lookup"><span data-stu-id="383a6-142">Retrieves a specific part from a compilation result.</span></span><br/></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="383a6-143"><a href="/windows/win32/api/d3dcompiler/nf-d3dcompiler-d3dgetdebuginfo"><strong>D3DGetDebugInfo</strong></a></span><span class="sxs-lookup"><span data-stu-id="383a6-143"><a href="/windows/win32/api/d3dcompiler/nf-d3dcompiler-d3dgetdebuginfo"><strong>D3DGetDebugInfo</strong></a></span></span><br/></td>
<td><blockquote>
[!Note]<br />
<span data-ttu-id="383a6-144">您可以使用此 API 來開發 Windows Store 應用程式，但不能將它用於提交至 Windows Store 的應用程式。</span><span class="sxs-lookup"><span data-stu-id="383a6-144">You can use this API to develop your Windows Store apps, but you can't use it in apps that you submit to the Windows Store.</span></span>
</blockquote>
<br/> <span data-ttu-id="383a6-145">取得著色器的調試資訊。</span><span class="sxs-lookup"><span data-stu-id="383a6-145">Gets shader debug information.</span></span><br/></td>
</tr>
<tr class="even">
<td><span data-ttu-id="383a6-146"><a href="/windows/win32/api/d3dcompiler/nf-d3dcompiler-d3dgetinputandoutputsignatureblob"><strong>D3DGetInputAndOutputSignatureBlob</strong></a></span><span class="sxs-lookup"><span data-stu-id="383a6-146"><a href="/windows/win32/api/d3dcompiler/nf-d3dcompiler-d3dgetinputandoutputsignatureblob"><strong>D3DGetInputAndOutputSignatureBlob</strong></a></span></span><br/></td>
<td><blockquote>
[!Note]<br /><span data-ttu-id="383a6-147">
<a href="/windows/win32/api/d3dcompiler/nf-d3dcompiler-d3dgetinputandoutputsignatureblob"><strong>D3DGetInputAndOutputSignatureBlob</strong></a> 可能會在 Windows 8.1 之後變更或無法使用。</span><span class="sxs-lookup"><span data-stu-id="383a6-147">
<a href="/windows/win32/api/d3dcompiler/nf-d3dcompiler-d3dgetinputandoutputsignatureblob"><strong>D3DGetInputAndOutputSignatureBlob</strong></a> may be altered or unavailable for releases after Windows 8.1.</span></span> <span data-ttu-id="383a6-148">請改為搭配<a href="/windows/win32/api/d3dcompiler/ne-d3dcompiler-d3d_blob_part"><strong>D3D_BLOB_INPUT_AND_OUTPUT_SIGNATURE_BLOB</strong></a>值使用<a href="/windows/win32/api/d3dcompiler/nf-d3dcompiler-d3dgetblobpart"><strong>D3DGetBlobPart</strong></a> 。</span><span class="sxs-lookup"><span data-stu-id="383a6-148">Instead use <a href="/windows/win32/api/d3dcompiler/nf-d3dcompiler-d3dgetblobpart"><strong>D3DGetBlobPart</strong></a> with the <a href="/windows/win32/api/d3dcompiler/ne-d3dcompiler-d3d_blob_part"><strong>D3D_BLOB_INPUT_AND_OUTPUT_SIGNATURE_BLOB</strong></a> value.</span></span>
</blockquote>
<br/> <span data-ttu-id="383a6-149">從編譯結果取得輸入和輸出簽章。</span><span class="sxs-lookup"><span data-stu-id="383a6-149">Gets the input and output signatures from a compilation result.</span></span><br/></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="383a6-150">[<strong>D3DGetInputSignatureBlob</strong>] (/windows/win32/api/d3dcompiler/nf-d3dcompiler-d3dgetinputsignatureblob) </span><span class="sxs-lookup"><span data-stu-id="383a6-150">[<strong>D3DGetInputSignatureBlob</strong>](/windows/win32/api/d3dcompiler/nf-d3dcompiler-d3dgetinputsignatureblob)</span></span><br/></td>
<td><blockquote>
[!Note]<br /><span data-ttu-id="383a6-151">
<a href="/windows/win32/api/d3dcompiler/nf-d3dcompiler-d3dgetinputsignatureblob"><strong>D3DGetInputSignatureBlob</strong></a> 可能會在 Windows 8.1 之後變更或無法使用。</span><span class="sxs-lookup"><span data-stu-id="383a6-151">
<a href="/windows/win32/api/d3dcompiler/nf-d3dcompiler-d3dgetinputsignatureblob"><strong>D3DGetInputSignatureBlob</strong></a> may be altered or unavailable for releases after Windows 8.1.</span></span> <span data-ttu-id="383a6-152">請改為搭配<a href="/windows/win32/api/d3dcompiler/ne-d3dcompiler-d3d_blob_part"><strong>D3D_BLOB_INPUT_SIGNATURE_BLOB</strong></a>值使用<a href="/windows/win32/api/d3dcompiler/nf-d3dcompiler-d3dgetblobpart"><strong>D3DGetBlobPart</strong></a> 。</span><span class="sxs-lookup"><span data-stu-id="383a6-152">Instead use <a href="/windows/win32/api/d3dcompiler/nf-d3dcompiler-d3dgetblobpart"><strong>D3DGetBlobPart</strong></a> with the <a href="/windows/win32/api/d3dcompiler/ne-d3dcompiler-d3d_blob_part"><strong>D3D_BLOB_INPUT_SIGNATURE_BLOB</strong></a> value.</span></span>
</blockquote>
<br/> <span data-ttu-id="383a6-153">從編譯結果取得輸入簽章。</span><span class="sxs-lookup"><span data-stu-id="383a6-153">Gets the input signature from a compilation result.</span></span><br/></td>
</tr>
<tr class="even">
<td><span data-ttu-id="383a6-154"><a href="/windows/win32/api/d3dcompiler/nf-d3dcompiler-d3dgetoutputsignatureblob"><strong>D3DGetOutputSignatureBlob</strong></a></span><span class="sxs-lookup"><span data-stu-id="383a6-154"><a href="/windows/win32/api/d3dcompiler/nf-d3dcompiler-d3dgetoutputsignatureblob"><strong>D3DGetOutputSignatureBlob</strong></a></span></span><br/></td>
<td><blockquote>
[!Note]<br /><span data-ttu-id="383a6-155">
<a href="/windows/win32/api/d3dcompiler/nf-d3dcompiler-d3dgetoutputsignatureblob"><strong>D3DGetOutputSignatureBlob</strong></a> 可能會在 Windows 8.1 之後變更或無法使用。</span><span class="sxs-lookup"><span data-stu-id="383a6-155">
<a href="/windows/win32/api/d3dcompiler/nf-d3dcompiler-d3dgetoutputsignatureblob"><strong>D3DGetOutputSignatureBlob</strong></a> may be altered or unavailable for releases after Windows 8.1.</span></span> <span data-ttu-id="383a6-156">請改為搭配<a href="/windows/win32/api/d3dcompiler/ne-d3dcompiler-d3d_blob_part"><strong>D3D_BLOB_OUTPUT_SIGNATURE_BLOB</strong></a>值使用<a href="/windows/win32/api/d3dcompiler/nf-d3dcompiler-d3dgetblobpart"><strong>D3DGetBlobPart</strong></a> 。</span><span class="sxs-lookup"><span data-stu-id="383a6-156">Instead use <a href="/windows/win32/api/d3dcompiler/nf-d3dcompiler-d3dgetblobpart"><strong>D3DGetBlobPart</strong></a> with the <a href="/windows/win32/api/d3dcompiler/ne-d3dcompiler-d3d_blob_part"><strong>D3D_BLOB_OUTPUT_SIGNATURE_BLOB</strong></a> value.</span></span>
</blockquote>
<br/> <span data-ttu-id="383a6-157">從編譯結果取得輸出簽章。</span><span class="sxs-lookup"><span data-stu-id="383a6-157">Gets the output signature from a compilation result.</span></span><br/></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="383a6-158"><a href="/windows/win32/api/d3dcompiler/nf-d3dcompiler-d3dgettraceinstructionoffsets"><strong>D3DGetTraceInstructionOffsets</strong></a></span><span class="sxs-lookup"><span data-stu-id="383a6-158"><a href="/windows/win32/api/d3dcompiler/nf-d3dcompiler-d3dgettraceinstructionoffsets"><strong>D3DGetTraceInstructionOffsets</strong></a></span></span><br/></td>
<td><span data-ttu-id="383a6-159">抓取著色器程式碼區段內的指示位元組位移。</span><span class="sxs-lookup"><span data-stu-id="383a6-159">Retrieves the byte offsets for instructions within a section of shader code.</span></span><br/></td>
</tr>
<tr class="even">
<td><span data-ttu-id="383a6-160"><a href="/windows/desktop/api/D3Dcompiler/nf-d3dcompiler-d3dloadmodule"><strong>D3DLoadModule</strong></a></span><span class="sxs-lookup"><span data-stu-id="383a6-160"><a href="/windows/desktop/api/D3Dcompiler/nf-d3dcompiler-d3dloadmodule"><strong>D3DLoadModule</strong></a></span></span><br/></td>
<td><span data-ttu-id="383a6-161">從著色器模組的來源資料建立著色器模組介面。</span><span class="sxs-lookup"><span data-stu-id="383a6-161">Creates a shader module interface from source data for the shader module.</span></span> <br/>
<blockquote>
[!Note]<br />
<span data-ttu-id="383a6-162">此函式是 HLSL 著色器連結技術的一部分，可讓您在所有 Direct3D 11 平臺上用來建立先行編譯的 HLSL 函式、將它們封裝至程式庫，並在執行時間將它們連結到完整的著色器。</span><span class="sxs-lookup"><span data-stu-id="383a6-162">This function is part of the HLSL shader linking technology that you can use on all Direct3D 11 platforms to create precompiled HLSL functions, package them into libraries, and link them into full shaders at run time.</span></span>
</blockquote>
<br/></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="383a6-163"><a href="/windows/win32/api/d3dcompiler/nf-d3dcompiler-d3dpreprocess"><strong>D3DPreprocess</strong></a></span><span class="sxs-lookup"><span data-stu-id="383a6-163"><a href="/windows/win32/api/d3dcompiler/nf-d3dcompiler-d3dpreprocess"><strong>D3DPreprocess</strong></a></span></span><br/></td>
<td><span data-ttu-id="383a6-164">未編譯的 HLSL 程式碼。</span><span class="sxs-lookup"><span data-stu-id="383a6-164">Preprocesses uncompiled HLSL code.</span></span><br/></td>
</tr>
<tr class="even">
<td><span data-ttu-id="383a6-165"><a href="/windows/win32/api/d3dcompiler/nf-d3dcompiler-d3dreadfiletoblob"><strong>D3DReadFileToBlob</strong></a></span><span class="sxs-lookup"><span data-stu-id="383a6-165"><a href="/windows/win32/api/d3dcompiler/nf-d3dcompiler-d3dreadfiletoblob"><strong>D3DReadFileToBlob</strong></a></span></span><br/></td>
<td><blockquote>
[!Note]<br />
<span data-ttu-id="383a6-166">您可以使用此 API 來開發 Windows Store 應用程式，但不能將它用於提交至 Windows Store 的應用程式。</span><span class="sxs-lookup"><span data-stu-id="383a6-166">You can use this API to develop your Windows Store apps, but you can't use it in apps that you submit to the Windows Store.</span></span>
</blockquote>
<br/> <span data-ttu-id="383a6-167">將磁片上的檔案讀取到記憶體中。</span><span class="sxs-lookup"><span data-stu-id="383a6-167">Reads a file that is on disk into memory.</span></span><br/></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="383a6-168"><a href="/windows/win32/api/d3dcompiler/nf-d3dcompiler-d3dreflect"><strong>D3DReflect</strong></a></span><span class="sxs-lookup"><span data-stu-id="383a6-168"><a href="/windows/win32/api/d3dcompiler/nf-d3dcompiler-d3dreflect"><strong>D3DReflect</strong></a></span></span><br/></td>
<td><span data-ttu-id="383a6-169">取得反映介面的指標。</span><span class="sxs-lookup"><span data-stu-id="383a6-169">Gets a pointer to a reflection interface.</span></span><br/></td>
</tr>
<tr class="even">
<td><span data-ttu-id="383a6-170"><a href="/windows/desktop/api/D3Dcompiler/nf-d3dcompiler-d3dreflectlibrary"><strong>D3DReflectLibrary</strong></a></span><span class="sxs-lookup"><span data-stu-id="383a6-170"><a href="/windows/desktop/api/D3Dcompiler/nf-d3dcompiler-d3dreflectlibrary"><strong>D3DReflectLibrary</strong></a></span></span><br/></td>
<td><span data-ttu-id="383a6-171">從包含函式 HLSL 程式庫的來源資料建立程式庫反映介面。</span><span class="sxs-lookup"><span data-stu-id="383a6-171">Creates a library-reflection interface from source data that contains an HLSL library of functions.</span></span> <br/>
<blockquote>
[!Note]<br />
<span data-ttu-id="383a6-172">此函式是 HLSL 著色器連結技術的一部分，可讓您在所有 Direct3D 11 平臺上用來建立先行編譯的 HLSL 函式、將它們封裝至程式庫，並在執行時間將它們連結到完整的著色器。</span><span class="sxs-lookup"><span data-stu-id="383a6-172">This function is part of the HLSL shader linking technology that you can use on all Direct3D 11 platforms to create precompiled HLSL functions, package them into libraries, and link them into full shaders at run time.</span></span>
</blockquote>
<br/></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="383a6-173"><a href="/windows/win32/api/d3dcompiler/nf-d3dcompiler-d3dsetblobpart"><strong>D3DSetBlobPart</strong></a></span><span class="sxs-lookup"><span data-stu-id="383a6-173"><a href="/windows/win32/api/d3dcompiler/nf-d3dcompiler-d3dsetblobpart"><strong>D3DSetBlobPart</strong></a></span></span><br/></td>
<td><span data-ttu-id="383a6-174">設定編譯結果中的資訊。</span><span class="sxs-lookup"><span data-stu-id="383a6-174">Sets information in a compilation result.</span></span><br/></td>
</tr>
<tr class="even">
<td><span data-ttu-id="383a6-175"><a href="/windows/win32/api/d3dcompiler/nf-d3dcompiler-d3dstripshader"><strong>D3DStripShader</strong></a></span><span class="sxs-lookup"><span data-stu-id="383a6-175"><a href="/windows/win32/api/d3dcompiler/nf-d3dcompiler-d3dstripshader"><strong>D3DStripShader</strong></a></span></span><br/></td>
<td><span data-ttu-id="383a6-176">從編譯結果中移除不需要的 blob。</span><span class="sxs-lookup"><span data-stu-id="383a6-176">Removes unwanted blobs from a compilation result.</span></span><br/></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="383a6-177"><a href="/windows/win32/api/d3dcompiler/nf-d3dcompiler-d3dwriteblobtofile"><strong>D3DWriteBlobToFile</strong></a></span><span class="sxs-lookup"><span data-stu-id="383a6-177"><a href="/windows/win32/api/d3dcompiler/nf-d3dcompiler-d3dwriteblobtofile"><strong>D3DWriteBlobToFile</strong></a></span></span><br/></td>
<td><blockquote>
[!Note]<br />
<span data-ttu-id="383a6-178">您可以使用此 API 來開發 Windows Store 應用程式，但不能將它用於提交至 Windows Store 的應用程式。</span><span class="sxs-lookup"><span data-stu-id="383a6-178">You can use this API to develop your Windows Store apps, but you can't use it in apps that you submit to the Windows Store.</span></span>
</blockquote>
<br/> <span data-ttu-id="383a6-179">將記憶體 blob 寫入磁片上的檔案。</span><span class="sxs-lookup"><span data-stu-id="383a6-179">Writes a memory blob to a file on disk.</span></span><br/></td>
</tr>
</tbody>
</table>



 

## <a name="related-topics"></a><span data-ttu-id="383a6-180">相關主題</span><span class="sxs-lookup"><span data-stu-id="383a6-180">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="383a6-181">D3DCompiler 參考</span><span class="sxs-lookup"><span data-stu-id="383a6-181">D3DCompiler Reference</span></span>](dx-graphics-d3dcompiler-reference.md)
</dt> </dl>

