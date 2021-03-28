---
title: 使用 Direct3D 10 中的著色器
description: 使用 Direct3D 10 中的著色器
ms.assetid: cff6f901-cb9b-44d5-a75b-9a4029a37215
ms.topic: article
ms.date: 05/31/2018
topic_type:
- kbArticle
api_name: ''
api_type: ''
api_location: ''
ms.openlocfilehash: 0e19275532ce8fd034813d8574f6bdc04d72f966
ms.sourcegitcommit: 592c9bbd22ba69802dc353bcb5eb30699f9e9403
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/20/2020
ms.locfileid: "104315181"
---
# <a name="using-shaders-in-direct3d-10"></a>使用 Direct3D 10 中的著色器

管線有三個著色器階段，而每一個都是使用 HLSL 著色器進行程式設計。 所有 Direct3D 10 著色器都會以 HLSL 撰寫，並以著色器模型4為目標。



|                                                                                                                                                                                                                                                                                                                                                |
|------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Direct3D 9 與 Direct3D 10 之間的差異：<br/> 與可使用中繼元件語言撰寫的 Direct3D 9 著色器模型不同，著色器模型4.0 著色器只會在 HLSL 中撰寫。 仍支援將著色器離線編譯成裝置可耗用的位元組程式碼，並建議用於大部分的案例。<br/> |



 

這個範例只會使用頂點著色器。 由於所有著色器都是從通用著色器核心建立的，因此學習如何使用頂點著色器非常類似于使用幾何或圖元著色器。

一旦您撰寫了 HLSL 著色器 (這個範例會使用頂點著色器 HLSLWithoutFX. vsh) ，您必須為將使用它的特定管線階段做好準備。 若要這樣做，您需要：

-   [編譯著色器](#compile-a-shader)
-   [建立著色器物件](#create-a-shader-object)
-   [設定著色器物件](#set-the-shader-object)
-   [針對所有3個著色器階段重複](#repeat-for-all-3-shader-stages)

這些步驟必須針對管線中的每個著色器重複執行。

## <a name="compile-a-shader"></a>編譯著色器

第一個步驟是編譯著色器，以檢查您是否已正確編碼 HLSL 語句。 這是藉由呼叫 D3D10CompileShader 並提供數個參數來完成，如下所示：


```
    IPD3D10Blob * pBlob;
    
        
    // Compile the vertex shader from the file
    D3D10CompileShader( strPath, strlen( strPath ), "HLSLWithoutFX.vsh", 
        NULL, NULL, "Ripple", "vs_4_0", dwShaderFlags, &pBlob, NULL );
```



此函數會採用下列參數：

-   檔案名 ( 的檔案名，以及包含著色器的位元組 ) 長度（以位元組為單位）。 此範例只會在 HLSLWithoutFX 檔案中使用頂點著色器 (，其中副檔名是頂點著色器) 的縮寫。
-   著色器函數名稱。 此範例會從 Ripple 函式編譯頂點著色器，此函式會採用單一輸入，並傳回輸出結構 (函式是來自 HLSLWithoutFX 範例) ：
    ```
    VS_OUTPUT Ripple( in float2 vPosition : POSITION )
    ```

    

-   著色器所使用之所有宏的指標。 使用 D3D10 \_ 著色器 \_ 宏可協助定義您的宏; 只要建立包含所有宏 (名稱的名稱字串，其中每個名稱都以空格分隔) 和每個宏主體 (的定義字串（以空格分隔）) 。 這兩個字串都必須以 Null 結束。
-   您需要包含的任何其他檔案的指標，以使您的著色器進行編譯。 這會使用具有兩個使用者執行方法的 ID3D10Include 介面：開啟和關閉。 若要進行這項工作，您必須執行開放式和 Close 方法的主體;在 Open 方法中，新增您要用來開啟所需檔案的程式碼，在 Close 函式中，新增程式碼以在完成這些檔案時加以關閉。
-   要編譯的著色器函式名稱。 此著色器會編譯 Ripple 函數。
-   編譯時要設為目標的著色器設定檔。 由於您可以將函式編譯成頂點、幾何或圖元著色器，因此設定檔會告知編譯器要將哪一種著色器類型以及要比較程式碼的著色器模型。
-   著色器編譯器旗標。 這些旗標會告訴編譯器要將哪些資訊放入編譯的輸出，以及您想要如何優化輸出程式碼：速度、偵錯工具等。如需可用旗標的清單，請參閱 [效果常數 (Direct3D 10) ](/windows/desktop/direct3d10/d3d10-graphics-reference-effect-constants) 。 此範例包含一些程式碼，您可以使用這些程式碼來設定專案的編譯器旗標值，這主要是您是否要產生偵錯工具資訊的問題。
-   緩衝區的指標，其中包含已編譯的著色器程式碼。 緩衝區也包含編譯器旗標所要求的任何內嵌的 debug 錯和符號表資訊。
-   包含在編譯期間遇到之錯誤和警告清單的緩衝區指標，如果您在編譯著色器時執行偵錯工具，就會在偵錯工具輸出中看到相同的訊息。 如果您不想要傳回給緩衝區的錯誤，則 **Null** 是可接受的值。

如果著色器編譯成功，則會以 ID3D10Blob 介面傳回著色器程式碼的指標。 因為指標是由 DWORD 陣列所組成的記憶體位置，所以稱為 Blob 介面。 系統會提供介面，讓您可以在下一個步驟中取得所需的已編譯著色器指標。

自2006年12月起的 SDK 起，DirectX 10 HLSL 編譯器現在是 DirectX 9 和 DirectX 10 中的預設編譯器。 請參閱 [效果-編譯器工具](/windows/desktop/direct3dtools/fxc) 以取得詳細資料。

### <a name="get-a-pointer-to-a-compiled-shader"></a>取得已編譯著色器的指標

數個 API 方法需要已編譯著色器的指標。 這個引數通常稱為 *pShaderBytecode* ，因為它指向以位元組碼序清單示的已編譯著色器。 若要取得已編譯之著色器的指標，請先呼叫 [**D3D10CompileShader**](/windows/desktop/api/d3d10shader/nf-d3d10shader-d3d10compileshader) 或類似的函式來編譯著色器。 如果編譯成功，則會在 [**ID3D10Blob**](/windows/desktop/api/d3dcommon/nn-d3dcommon-id3d10blob) 介面中傳回已編譯的著色器。 最後，使用 [**GetBufferPointer**](/windows/desktop/api/d3dcommon/nf-d3dcommon-id3d10blob-getbufferpointer) 方法來傳回指標。

## <a name="create-a-shader-object"></a>建立著色器物件

編譯著色器之後，請呼叫 CreateVertexShader 來建立著色器物件：


```
    ID3D10VertexShader ** ppVertexShader
    ID3D10Blob pBlob;


    // Create the vertex shader
    hr = pd3dDevice->CreateVertexShader( (DWORD*)pBlob->GetBufferPointer(),
        pBlob->GetBufferSize(), &ppVertexShader );

    // Release the pointer to the compiled shader once you are done with it
    pBlob->Release();
```



若要建立著色器物件，請將已編譯的著色器指標傳遞至 CreateVertexShader。 因為您必須先成功編譯著色器，否則除非您的電腦上有記憶體問題，否則此呼叫幾乎當然會通過。

您可以根據自己的需要建立任意數量的著色器物件，並只保留其指標。 這項相同的機制適用于幾何和圖元著色器，假設您符合著色器設定檔 (當您在呼叫 create 方法) 時，)  (的介面名稱。

## <a name="set-the-shader-object"></a>設定著色器物件

最後一個步驟是將著色器設定為管線階段。 因為管線中有三個著色器階段，所以您需要進行三個 API 呼叫，每個階段各一個。


```
    // Set a vertex shader
    pd3dDevice->VSSetShader( g_pVS10 );
```



對 VSSetShader 的呼叫會將指標移至在步驟1中建立的頂點著色器。 這會設定裝置中的著色器。 端點著色器階段現在會以其頂點著色器程式碼進行初始化，剩下的就是初始化任何著色器變數。

## <a name="repeat-for-all-3-shader-stages"></a>針對所有3個著色器階段重複

重複執行這組相同的步驟，以建立任何頂點或圖元著色器，或甚至是輸出至圖元著色器的幾何著色器。

## <a name="related-topics"></a>[相關主題]

[編譯著色器](dx-graphics-hlsl-part1.md)


## <a name="related-topics"></a>相關主題

<dl> <dt>

[HLSL 的程式設計指南](dx-graphics-hlsl-pguide.md)
</dt> </dl>

 

