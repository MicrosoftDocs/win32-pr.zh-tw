---
title: 編譯著色器
description: 現在讓我們看看如何編譯著色器程式碼的各種方式，以及著色器程式碼副檔名的慣例。
ms.assetid: a4e6b7cd-c5cc-4165-ba73-205155e449c9
ms.topic: article
ms.date: 05/31/2018
topic_type:
- kbArticle
api_name: ''
api_type: ''
api_location: ''
ms.openlocfilehash: 3ea71da99dd68769324b07d3fc76a0c5ca00009d
ms.sourcegitcommit: 592c9bbd22ba69802dc353bcb5eb30699f9e9403
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/20/2020
ms.locfileid: "104315526"
---
# <a name="compiling-shaders"></a><span data-ttu-id="80025-103">編譯著色器</span><span class="sxs-lookup"><span data-stu-id="80025-103">Compiling shaders</span></span>

> [!NOTE]
> <span data-ttu-id="80025-104">本主題涵蓋 `FXC.EXE` 用於著色器模型2到5.1 的編譯器。</span><span class="sxs-lookup"><span data-stu-id="80025-104">This topic covers the `FXC.EXE` compiler used for Shader Models 2 through 5.1.</span></span> <span data-ttu-id="80025-105">針對著色器模型6，您可以改用 `DXC.EXE` ，它是使用 [dxc.exe 和 dxcompiler.dll](https://github.com/microsoft/DirectXShaderCompiler/wiki/Using-dxc.exe-and-dxcompiler.dll)所記載。</span><span class="sxs-lookup"><span data-stu-id="80025-105">For Shader Model 6, you use `DXC.EXE` instead, which is documented in [Using dxc.exe and dxcompiler.dll](https://github.com/microsoft/DirectXShaderCompiler/wiki/Using-dxc.exe-and-dxcompiler.dll).</span></span>

<span data-ttu-id="80025-106">Microsoft Visual Studio 2012 現在可以從 \* 您包含在 c + + 專案中的 hlsl 檔案編譯著色器程式碼。</span><span class="sxs-lookup"><span data-stu-id="80025-106">Microsoft Visual Studio 2012 can now compile shader code from \*.hlsl files that you include in your C++ project.</span></span>

<span data-ttu-id="80025-107">在建立過程中，Visual Studio 2012 會使用 [fxc.exe](/windows/desktop/direct3dtools/fxc) HLSL 程式碼編譯器，將 HLSL 檔案編譯成二進位著色器物件檔案，或編譯成標頭檔中定義的位元組陣列。</span><span class="sxs-lookup"><span data-stu-id="80025-107">As part of the build process, Visual Studio 2012 uses the [fxc.exe](/windows/desktop/direct3dtools/fxc) HLSL code compiler to compile the .hlsl files into binary shader object files or into byte arrays that are defined in header files.</span></span> <span data-ttu-id="80025-108">HLSL 程式碼編譯器如何編譯專案中的每個 HLSL 檔案，取決於您如何指定該檔案的 [ **輸出** 檔案] 屬性。</span><span class="sxs-lookup"><span data-stu-id="80025-108">How the HLSL code compiler compiles each .hlsl file in your project depends on how you specify the **Ouput Files** property for that file.</span></span> <span data-ttu-id="80025-109">如需 HLSL 屬性頁的詳細資訊，請參閱 [HLSL 屬性頁](/previous-versions/visualstudio/visual-studio-2012/jj620902(v=vs.110))。</span><span class="sxs-lookup"><span data-stu-id="80025-109">For more info about HLSL property pages, see [HLSL Property Pages](/previous-versions/visualstudio/visual-studio-2012/jj620902(v=vs.110)).</span></span>

<span data-ttu-id="80025-110">您使用的編譯方法通常取決於 hlsl 檔案的大小 \* 。</span><span class="sxs-lookup"><span data-stu-id="80025-110">The compile method that you use typically depends on the size of your \*.hlsl file.</span></span> <span data-ttu-id="80025-111">如果您在標頭中包含大量的位元組代碼，則會增加應用程式的大小和初始載入時間。</span><span class="sxs-lookup"><span data-stu-id="80025-111">If you include a large amount of byte code in a header, you increase the size and the initial load time of your app.</span></span> <span data-ttu-id="80025-112">您也會強制所有的位元組程式碼都存在於記憶體中，即使在建立著色器之後，這會浪費資源。</span><span class="sxs-lookup"><span data-stu-id="80025-112">You also force all byte code to reside in memory even after the shader is created, which wastes resources.</span></span> <span data-ttu-id="80025-113">但是，當您在標頭中包含位元組程式碼時，可以降低程式碼的複雜度，並簡化著色器的建立工作。</span><span class="sxs-lookup"><span data-stu-id="80025-113">But when you include byte code in a header, you can reduce code complexity and simplify shader creation.</span></span>

<span data-ttu-id="80025-114">現在讓我們看看如何編譯著色器程式碼的各種方式，以及著色器程式碼副檔名的慣例。</span><span class="sxs-lookup"><span data-stu-id="80025-114">Let's now look at various ways to compile your shader code and conventions for file extensions for shader code.</span></span>

-   [<span data-ttu-id="80025-115">使用著色器程式碼副檔名</span><span class="sxs-lookup"><span data-stu-id="80025-115">Using shader code file extensions</span></span>](#using-shader-code-file-extensions)
-   [<span data-ttu-id="80025-116">在組建時編譯至物件檔案</span><span class="sxs-lookup"><span data-stu-id="80025-116">Compiling at build time to object files</span></span>](#compiling-at-build-time-to-object-files)
-   [<span data-ttu-id="80025-117">在組建時編譯至標頭檔</span><span class="sxs-lookup"><span data-stu-id="80025-117">Compiling at build time to header files</span></span>](#compiling-at-build-time-to-header-files)
-   [<span data-ttu-id="80025-118">使用 D3DCompileFromFile 進行編譯</span><span class="sxs-lookup"><span data-stu-id="80025-118">Compiling with D3DCompileFromFile</span></span>](#compiling-with-d3dcompilefromfile)
-   [<span data-ttu-id="80025-119">相關主題</span><span class="sxs-lookup"><span data-stu-id="80025-119">Related Topics</span></span>](#related-topics)
-   [<span data-ttu-id="80025-120">相關主題</span><span class="sxs-lookup"><span data-stu-id="80025-120">Related topics</span></span>](#related-topics)

## <a name="using-shader-code-file-extensions"></a><span data-ttu-id="80025-121">使用著色器程式碼副檔名</span><span class="sxs-lookup"><span data-stu-id="80025-121">Using shader code file extensions</span></span>

<span data-ttu-id="80025-122">若要符合 Microsoft 慣例，請針對您的著色器程式碼使用這些副檔名：</span><span class="sxs-lookup"><span data-stu-id="80025-122">To conform to Microsoft convention, use these file extensions for your shader code:</span></span>

-   <span data-ttu-id="80025-123">副檔名為 hlsl 的檔案具有高階的陰影語言 ([hlsl](dx-graphics-hlsl-reference.md)) 原始程式碼。</span><span class="sxs-lookup"><span data-stu-id="80025-123">A file with the .hlsl extension holds High Level Shading Language ([HLSL](dx-graphics-hlsl-reference.md)) source code.</span></span>
-   <span data-ttu-id="80025-124">有 .Cso 副檔名的檔案會保留所使用的著色器物件。</span><span class="sxs-lookup"><span data-stu-id="80025-124">A file with the .cso extension holds a compiled shader object.</span></span>
-   <span data-ttu-id="80025-125">有 .h 副檔名的檔案是標頭檔案，但在著色器程式碼操作中，此標頭檔案定義位元組陣列，其保留著色器資料。</span><span class="sxs-lookup"><span data-stu-id="80025-125">A file with the .h extension is a header file, but in a shader code context, this header file defines a byte array that holds shader data.</span></span>

## <a name="compiling-at-build-time-to-object-files"></a><span data-ttu-id="80025-126">在組建時編譯至物件檔案</span><span class="sxs-lookup"><span data-stu-id="80025-126">Compiling at build time to object files</span></span>

<span data-ttu-id="80025-127">如果您將 hlsl 檔案編譯成二進位著色器物件檔案，則您的應用程式必須從這些物件檔案讀取資料 (。 cso 是這些物件檔案的預設副檔名) 、將資料指派給位元組陣列，以及從這些位元組陣列建立著色器物件。</span><span class="sxs-lookup"><span data-stu-id="80025-127">If you compile your .hlsl files into binary shader object files, your app needs to read the data from those object files (.cso is the default extension for these object files), assign the data to byte arrays, and create shader objects from those byte arrays.</span></span> <span data-ttu-id="80025-128">例如，若要建立頂點著色器 ([**ID3D11VertexShader**](/windows/desktop/api/d3d11/nn-d3d11-id3d11vertexshader) \* \*) ，請使用包含已編譯頂點著色器位元組程式碼的位元組陣列來呼叫 [**ID3D11Device：： CreateVertexShader**](/windows/desktop/api/d3d11/nf-d3d11-id3d11device-createvertexshader)方法。</span><span class="sxs-lookup"><span data-stu-id="80025-128">For example, to create a vertex shader ([**ID3D11VertexShader**](/windows/desktop/api/d3d11/nn-d3d11-id3d11vertexshader)\*\*), call the [**ID3D11Device::CreateVertexShader**](/windows/desktop/api/d3d11/nf-d3d11-id3d11device-createvertexshader) method with a byte array that contains compiled vertex shader byte code.</span></span> <span data-ttu-id="80025-129">[Direct3D 教學課程範例示範](https://github.com/microsoftarchive/msdn-code-gallery-microsoft/tree/master/Official%20Windows%20Platform%20Sample/Direct3D%20tutorial%20sample)如何從所取得的位元組陣列建立著色器物件。</span><span class="sxs-lookup"><span data-stu-id="80025-129">The [Direct3D tutorial sample](https://github.com/microsoftarchive/msdn-code-gallery-microsoft/tree/master/Official%20Windows%20Platform%20Sample/Direct3D%20tutorial%20sample) shows how to create shader objects from byte arrays that it obtained from .cso binary shader object files.</span></span> <span data-ttu-id="80025-130">在這個來自 [Direct3D 教學課程範例](https://github.com/microsoftarchive/msdn-code-gallery-microsoft/tree/master/Official%20Windows%20Platform%20Sample/Direct3D%20tutorial%20sample)的程式碼範例中，SimpleVertexShader. hlsl 檔案的 [ **輸出** 檔] 屬性會指定編譯到 SimpleVertexShader 的 [] 物件檔案中。</span><span class="sxs-lookup"><span data-stu-id="80025-130">In this example code from the [Direct3D tutorial sample](https://github.com/microsoftarchive/msdn-code-gallery-microsoft/tree/master/Official%20Windows%20Platform%20Sample/Direct3D%20tutorial%20sample), the **Ouput Files** property for the SimpleVertexShader.hlsl file specifies to compile into the SimpleVertexShader.cso object file.</span></span>

```cpp
        auto vertexShaderBytecode = reader->ReadData("SimpleVertexShader.cso");
        ComPtr<ID3D11VertexShader> vertexShader;
        DX::ThrowIfFailed(
            m_d3dDevice->CreateVertexShader(
                vertexShaderBytecode->Data,
                vertexShaderBytecode->Length,
                nullptr,
                &vertexShader
                )
```

## <a name="compiling-at-build-time-to-header-files"></a><span data-ttu-id="80025-131">在組建時編譯至標頭檔</span><span class="sxs-lookup"><span data-stu-id="80025-131">Compiling at build time to header files</span></span>

<span data-ttu-id="80025-132">如果您將 hlsl 檔案編譯成標頭檔中定義的位元組陣列，則必須將這些標頭檔包含在您的程式碼中。</span><span class="sxs-lookup"><span data-stu-id="80025-132">If you compile your .hlsl files into byte arrays that are defined in header files, you need to include those header files in your code.</span></span> <span data-ttu-id="80025-133">[媒體擴充功能範例會示範](https://github.com/microsoftarchive/msdn-code-gallery-microsoft/tree/master/Official%20Windows%20Platform%20Sample/Media%20extensions%20sample)如何從在標頭檔中定義的位元組陣列，以及在編譯時期包含在專案中的位元組陣列建立著色器物件。</span><span class="sxs-lookup"><span data-stu-id="80025-133">The [Media extensions sample](https://github.com/microsoftarchive/msdn-code-gallery-microsoft/tree/master/Official%20Windows%20Platform%20Sample/Media%20extensions%20sample) shows how to create shader objects from byte arrays that are defined in header files and that you include in your project at compile time.</span></span> <span data-ttu-id="80025-134">在這個來自 [媒體擴充範例](https://github.com/microsoftarchive/msdn-code-gallery-microsoft/tree/master/Official%20Windows%20Platform%20Sample/Media%20extensions%20sample)的程式碼範例中，無效. hlsl 檔案的 [ **輸出** 檔] 屬性會指定編譯成無效標頭檔中定義的 *g \_ psshader* 位元組陣列。</span><span class="sxs-lookup"><span data-stu-id="80025-134">In this example code from the [Media extensions sample](https://github.com/microsoftarchive/msdn-code-gallery-microsoft/tree/master/Official%20Windows%20Platform%20Sample/Media%20extensions%20sample), the **Ouput Files** property for the PixelShader.hlsl file specifies to compile into the *g\_psshader* byte array that is defined in the PixelShader.h header file.</span></span>


```C++
#       include "PixelShader.h"
        ComPtr<ID3D11PixelShader> m_pPixelShader;
        hr = pDevice->CreatePixelShader(g_psshader, sizeof(g_psshader), nullptr, &m_pPixelShader);
```



## <a name="compiling-with-d3dcompilefromfile"></a><span data-ttu-id="80025-135">使用 D3DCompileFromFile 進行編譯</span><span class="sxs-lookup"><span data-stu-id="80025-135">Compiling with D3DCompileFromFile</span></span>

<span data-ttu-id="80025-136">您也可以在執行時間使用 [**D3DCompileFromFile**](/windows/win32/api/d3dcompiler/nf-d3dcompiler-d3dcompilefromfile) 函式來編譯著色器程式碼。</span><span class="sxs-lookup"><span data-stu-id="80025-136">You can also use the [**D3DCompileFromFile**](/windows/win32/api/d3dcompiler/nf-d3dcompiler-d3dcompilefromfile) function at run time to compile shader code.</span></span> <span data-ttu-id="80025-137">如需如何執行此作業的詳細資訊，請參閱 [如何：編譯著色器](/windows/desktop/direct3d11/how-to--compile-a-shader)。</span><span class="sxs-lookup"><span data-stu-id="80025-137">For more info about how to do this, see [How To: Compile a Shader](/windows/desktop/direct3d11/how-to--compile-a-shader).</span></span>

> [!Note]  
> <span data-ttu-id="80025-138">Windows Store 應用程式支援使用 [**D3DCompileFromFile**](/windows/win32/api/d3dcompiler/nf-d3dcompiler-d3dcompilefromfile) 進行開發，但不支援部署。</span><span class="sxs-lookup"><span data-stu-id="80025-138">Windows Store apps support using [**D3DCompileFromFile**](/windows/win32/api/d3dcompiler/nf-d3dcompiler-d3dcompilefromfile) for development but not for deployment.</span></span>

 

## <a name="related-topics"></a><span data-ttu-id="80025-139">[相關主題]</span><span class="sxs-lookup"><span data-stu-id="80025-139">Related Topics</span></span>

[<span data-ttu-id="80025-140">HLSL 的程式設計指南</span><span class="sxs-lookup"><span data-stu-id="80025-140">Programming Guide for HLSL</span></span>](dx-graphics-hlsl-pguide.md)


## <a name="related-topics"></a><span data-ttu-id="80025-141">相關主題</span><span class="sxs-lookup"><span data-stu-id="80025-141">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="80025-142">HLSL 的程式設計指南</span><span class="sxs-lookup"><span data-stu-id="80025-142">Programming Guide for HLSL</span></span>](dx-graphics-hlsl-pguide.md)
</dt> </dl>

 

 