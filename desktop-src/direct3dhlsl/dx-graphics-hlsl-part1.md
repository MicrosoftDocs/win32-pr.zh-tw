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
# <a name="compiling-shaders"></a>編譯著色器

> [!NOTE]
> 本主題涵蓋 `FXC.EXE` 用於著色器模型2到5.1 的編譯器。 針對著色器模型6，您可以改用 `DXC.EXE` ，它是使用 [dxc.exe 和 dxcompiler.dll](https://github.com/microsoft/DirectXShaderCompiler/wiki/Using-dxc.exe-and-dxcompiler.dll)所記載。

Microsoft Visual Studio 2012 現在可以從 \* 您包含在 c + + 專案中的 hlsl 檔案編譯著色器程式碼。

在建立過程中，Visual Studio 2012 會使用 [fxc.exe](/windows/desktop/direct3dtools/fxc) HLSL 程式碼編譯器，將 HLSL 檔案編譯成二進位著色器物件檔案，或編譯成標頭檔中定義的位元組陣列。 HLSL 程式碼編譯器如何編譯專案中的每個 HLSL 檔案，取決於您如何指定該檔案的 [ **輸出** 檔案] 屬性。 如需 HLSL 屬性頁的詳細資訊，請參閱 [HLSL 屬性頁](/previous-versions/visualstudio/visual-studio-2012/jj620902(v=vs.110))。

您使用的編譯方法通常取決於 hlsl 檔案的大小 \* 。 如果您在標頭中包含大量的位元組代碼，則會增加應用程式的大小和初始載入時間。 您也會強制所有的位元組程式碼都存在於記憶體中，即使在建立著色器之後，這會浪費資源。 但是，當您在標頭中包含位元組程式碼時，可以降低程式碼的複雜度，並簡化著色器的建立工作。

現在讓我們看看如何編譯著色器程式碼的各種方式，以及著色器程式碼副檔名的慣例。

-   [使用著色器程式碼副檔名](#using-shader-code-file-extensions)
-   [在組建時編譯至物件檔案](#compiling-at-build-time-to-object-files)
-   [在組建時編譯至標頭檔](#compiling-at-build-time-to-header-files)
-   [使用 D3DCompileFromFile 進行編譯](#compiling-with-d3dcompilefromfile)
-   [相關主題](#related-topics)
-   [相關主題](#related-topics)

## <a name="using-shader-code-file-extensions"></a>使用著色器程式碼副檔名

若要符合 Microsoft 慣例，請針對您的著色器程式碼使用這些副檔名：

-   副檔名為 hlsl 的檔案具有高階的陰影語言 ([hlsl](dx-graphics-hlsl-reference.md)) 原始程式碼。
-   有 .Cso 副檔名的檔案會保留所使用的著色器物件。
-   有 .h 副檔名的檔案是標頭檔案，但在著色器程式碼操作中，此標頭檔案定義位元組陣列，其保留著色器資料。

## <a name="compiling-at-build-time-to-object-files"></a>在組建時編譯至物件檔案

如果您將 hlsl 檔案編譯成二進位著色器物件檔案，則您的應用程式必須從這些物件檔案讀取資料 (。 cso 是這些物件檔案的預設副檔名) 、將資料指派給位元組陣列，以及從這些位元組陣列建立著色器物件。 例如，若要建立頂點著色器 ([**ID3D11VertexShader**](/windows/desktop/api/d3d11/nn-d3d11-id3d11vertexshader) \* \*) ，請使用包含已編譯頂點著色器位元組程式碼的位元組陣列來呼叫 [**ID3D11Device：： CreateVertexShader**](/windows/desktop/api/d3d11/nf-d3d11-id3d11device-createvertexshader)方法。 [Direct3D 教學課程範例示範](https://github.com/microsoftarchive/msdn-code-gallery-microsoft/tree/master/Official%20Windows%20Platform%20Sample/Direct3D%20tutorial%20sample)如何從所取得的位元組陣列建立著色器物件。 在這個來自 [Direct3D 教學課程範例](https://github.com/microsoftarchive/msdn-code-gallery-microsoft/tree/master/Official%20Windows%20Platform%20Sample/Direct3D%20tutorial%20sample)的程式碼範例中，SimpleVertexShader. hlsl 檔案的 [ **輸出** 檔] 屬性會指定編譯到 SimpleVertexShader 的 [] 物件檔案中。

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

## <a name="compiling-at-build-time-to-header-files"></a>在組建時編譯至標頭檔

如果您將 hlsl 檔案編譯成標頭檔中定義的位元組陣列，則必須將這些標頭檔包含在您的程式碼中。 [媒體擴充功能範例會示範](https://github.com/microsoftarchive/msdn-code-gallery-microsoft/tree/master/Official%20Windows%20Platform%20Sample/Media%20extensions%20sample)如何從在標頭檔中定義的位元組陣列，以及在編譯時期包含在專案中的位元組陣列建立著色器物件。 在這個來自 [媒體擴充範例](https://github.com/microsoftarchive/msdn-code-gallery-microsoft/tree/master/Official%20Windows%20Platform%20Sample/Media%20extensions%20sample)的程式碼範例中，無效. hlsl 檔案的 [ **輸出** 檔] 屬性會指定編譯成無效標頭檔中定義的 *g \_ psshader* 位元組陣列。


```C++
#       include "PixelShader.h"
        ComPtr<ID3D11PixelShader> m_pPixelShader;
        hr = pDevice->CreatePixelShader(g_psshader, sizeof(g_psshader), nullptr, &m_pPixelShader);
```



## <a name="compiling-with-d3dcompilefromfile"></a>使用 D3DCompileFromFile 進行編譯

您也可以在執行時間使用 [**D3DCompileFromFile**](/windows/win32/api/d3dcompiler/nf-d3dcompiler-d3dcompilefromfile) 函式來編譯著色器程式碼。 如需如何執行此作業的詳細資訊，請參閱 [如何：編譯著色器](/windows/desktop/direct3d11/how-to--compile-a-shader)。

> [!Note]  
> Windows Store 應用程式支援使用 [**D3DCompileFromFile**](/windows/win32/api/d3dcompiler/nf-d3dcompiler-d3dcompilefromfile) 進行開發，但不支援部署。

 

## <a name="related-topics"></a>[相關主題]

[HLSL 的程式設計指南](dx-graphics-hlsl-pguide.md)


## <a name="related-topics"></a>相關主題

<dl> <dt>

[HLSL 的程式設計指南](dx-graphics-hlsl-pguide.md)
</dt> </dl>

 

 