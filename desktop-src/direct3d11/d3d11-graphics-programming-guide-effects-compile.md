---
title: '將效果編譯 (Direct3D 11) '
description: 在撰寫效果之後，下一步是要編譯器代碼以檢查語法問題。
ms.assetid: 7624d55e-6466-4156-8f31-30f0d25a2883
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: c3df304a7b657af19984008bd90a1be4bfe5219c
ms.sourcegitcommit: 592c9bbd22ba69802dc353bcb5eb30699f9e9403
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/20/2020
ms.locfileid: "103933356"
---
# <a name="compile-an-effect-direct3d-11"></a>將效果編譯 (Direct3D 11) 

在撰寫效果之後，下一步是要編譯器代碼以檢查語法問題。

若要這麼做，請呼叫其中一個編譯 Api ([**D3DX11CompileFromFile**](d3dx11compilefromfile.md)、 [**D3DX11CompileFromMemory**](d3dx11compilefrommemory.md)或 [**D3DX11CompileFromResource**](d3dx11compilefromresource.md) ) 。 這些 Api 會叫用效果編譯器 fxc.exe，以編譯 HLSL 程式碼。 這就是為什麼效果中的程式碼語法看起來非常類似 HLSL 程式碼的原因。  (有一些例外狀況會在稍後) 處理。 您可以在 [公用程式] 資料夾的 SDK 中使用效果編譯器/hlsl 編譯器 fxc.exe，以在您選擇的情況下離線編譯著色器 (或效果) 。 請參閱從命令列執行編譯器的檔。

-   [範例](#example)
-   [Includes](#includes)
-   [搜尋 Include 檔](#searching-for-include-files)
-   [巨集](#macros)
-   [HLSL 著色器旗標](#hlsl-shader-flags)
-   [FX 旗標](#fx-flags)
-   [檢查錯誤](#checking-errors)
-   [相關主題](#related-topics)

## <a name="example"></a>範例

以下是編譯效果檔案的範例。


```
WCHAR str[MAX_PATH];
DXUTFindDXSDKMediaFileCch( str, MAX_PATH, L"BasicHLSL10.fx" );

hr = D3DX11CompileFromFile( str, NULL, NULL, pFunctionName, pProfile, D3D10_SHADER_ENABLE_STRICTNESS, NULL, NULL, &pBlob, &pErrorBlob, NULL );
```



## <a name="includes"></a>Includes

編譯 Api 的一個參數是包含介面。 如果您想要在編譯器讀取 include 檔時包含自訂的行為，請產生其中一種。 編譯器會在每次建立或編譯使用 include 指標) 的效果 (時，執行這個自訂行為。 若要執行自訂的 include 行為，請從 [**ID3DInclude**](/windows/desktop/api/D3Dcommon/nn-d3dcommon-id3dinclude) 介面衍生類別。 這可為您的類別提供兩種方法： [**開啟**](/windows/desktop/api/D3DCommon/nf-d3dcommon-id3dinclude-open) 和 [**關閉**](/windows/desktop/api/D3DCommon/nf-d3dcommon-id3dinclude-close)。 在這些方法中執行自訂行為。

## <a name="searching-for-include-files"></a>搜尋 Include 檔

編譯器在 *pParentData* 參數中傳遞給包含處理常式 [**Open**](/windows/desktop/api/D3DCommon/nf-d3dcommon-id3dinclude-open) 方法的指標，可能不會指向包含 \# 編譯器編譯著色器程式碼所需之 include 檔的容器。 也就是說，編譯器可能會在 *pParentData* 中傳遞 **Null** 。 因此，我們建議您的 include 處理常式搜尋自己的內容包含位置清單。 您的 include 處理常式可以動態地加入新的 include 位置，因為它會在呼叫其 **Open** 方法時接收這些位置。

在下列範例中，假設著色器程式碼的 include 檔案都儲存在 *somewhereelse* 目錄中。 當編譯器呼叫 include 處理常式的 [**open**](/windows/desktop/api/D3DCommon/nf-d3dcommon-id3dinclude-open) 方法來開啟和讀取 *somewhereelse \\ foo .h* 的內容時，include 處理常式可以儲存 **somewhereelse** 目錄的位置。 稍後，當編譯器呼叫 include 處理常式的 **open** 方法來開啟和讀取 *bar* 的內容時，include 處理常式可以在 *somewhereelse* 目錄中自動搜尋 *bar. h*。


```
Main.hlsl:
#include "somewhereelse\foo.h"

Foo.h:
#include "bar.h"
```



## <a name="macros"></a>巨集

效果編譯也可以取得在其他位置定義的宏指標。 例如，假設您想要修改 BasicHLSL10 中的效果，以使用兩個宏：零和一。 使用這兩個宏的效果程式碼如下所示。


```
if( bAnimate )
    vAnimatedPos += float4(vNormal, zero) *  
        (sin(g_fTime+5.5)+0.5)*5;
        
    Output.Diffuse.a = one;         
```



以下是兩個宏的宣告。


```
D3D10_SHADER_MACRO Shader_Macros[3] = { "zero", "0", "one", "1.0f", NULL, NULL };
```



宏是以 Null 結束的宏陣列;其中每個宏都是使用 [**D3D10 \_ 著色器 \_ 宏**](/windows/desktop/api/d3dcommon/ns-d3dcommon-d3d_shader_macro) 結構來定義。

修改編譯效果呼叫以取得宏的指標。


```
D3DX11CompileFromFile( str, Shader_Macros, NULL, pFunctionName, 
                       pProfile, D3D10_SHADER_ENABLE_STRICTNESS, NULL, 
                       NULL, &pBlob, &pErrorBlob, NULL );    
```



## <a name="hlsl-shader-flags"></a>HLSL 著色器旗標

著色器旗標會指定 HLSL 編譯器的著色器條件約束。 這些旗標會以下列方式影響著色器編譯器產生的程式碼：

-   優化程式碼大小。
-   包含可防止流量控制的調試資訊。
-   會影響編譯目標，以及著色器是否可以在舊版硬體上執行。

如果您未指定兩個衝突的特性，這些旗標可以邏輯方式結合。 如需旗標的清單，請參閱 [D3D10 \_ 著色器常數](/windows/desktop/direct3d10/d3d10-shader)。

## <a name="fx-flags"></a>FX 旗標

當您建立效果來定義編譯行為或執行時間效果行為時，請使用這些旗標。 如需旗標的清單，請參閱 [D3D10 \_ 效果常數](/windows/desktop/direct3d10/d3d10-effect)。

## <a name="checking-errors"></a>檢查錯誤

如果在編譯期間發生錯誤，則 API 會傳回包含效果編譯器錯誤的介面。 這個介面稱為 [**ID3DBlob**](/previous-versions/windows/desktop/legacy/ff728743(v=vs.85))。 它無法直接讀取;不過，藉由將指標傳回至包含資料 (的緩衝區（這是) 的字串），您可以看到任何編譯錯誤。

此範例包含 BasicHLSL 中的錯誤，第一個變數宣告會出現兩次。


```
//-------------------------------------------------------------------
// Global variables
//-------------------------------------------------------------------
float4 g_MaterialAmbientColor;      // Material's ambient color

// Declare the same variable twice
float4 g_MaterialAmbientColor;      // Material's ambient color
```



此錯誤會導致編譯器傳回下列錯誤，如 Microsoft Visual Studio 中監看式視窗的下列螢幕擷取畫面所示。

![visual studio 監看式視窗的螢幕擷取畫面，其中包含0x01997fb8 錯誤](images/effect-compile-errors-2.jpg)

因為編譯器會在 LPVOID 指標中傳回錯誤，所以會將它轉換成監看式視窗中的字元字串。

以下是從失敗的編譯傳回錯誤的程式碼。


```
// Read the D3DX effect file
WCHAR str[MAX_PATH];
ID3DBlob*   l_pBlob_Effect = NULL;
ID3DBlob*   l_pBlob_Errors = NULL;
hr = DXUTFindDXSDKMediaFileCch( str, MAX_PATH, L"BasicHLSL10.fx" );
hr = D3DX11CompileFromFile( str, NULL, NULL, pFunctionName, 
                       pProfile, D3D10_SHADER_ENABLE_STRICTNESS, NULL, 
                       NULL, &pBlob, &pErrorBlob, NULL );      

LPVOID l_pError = NULL;
if( pErrorBlob )
{
    l_pError = pErrorBlob->GetBufferPointer();
    // then cast to a char* to see it in the locals window
}
```



## <a name="related-topics"></a>相關主題

<dl> <dt>

[轉譯 (Direct3D 11) 的效果 ](d3d11-graphics-programming-guide-effects-render.md)
</dt> </dl>

 

 