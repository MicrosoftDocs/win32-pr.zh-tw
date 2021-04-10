---
description: 一旦撰寫好效果之後，第一個步驟就是編譯器代碼以檢查語法問題。
ms.assetid: b8d8a0b7-b520-44e4-8691-6eb46202c092
title: 編譯效果 (Direct3D 10)
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: ab6183f2f71b07c482fa24efc4f9fed199216d75
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/07/2021
ms.locfileid: "104187653"
---
# <a name="compile-an-effect-direct3d-10"></a>編譯效果 (Direct3D 10)

一旦撰寫好效果之後，第一個步驟就是編譯器代碼以檢查語法問題。 這是藉由呼叫其中一個編譯 Api 來完成， (例如 D3DX10CompileEffectFromFile、D3DX10CompileEffectFromResource、D3DX10CompileEffectFromMemory) 。 這些 API 會叫用效果編譯器 fxc.exe 編譯器用來編譯 HLSL 程式碼。 這就是為什麼效果中程式碼的語法看起來很像 HLSL 程式碼 (有一些例外狀況會在稍後) 處理。 順便一提，編譯器/hlsl 編譯器 (fxc.exe) 會在 [公用程式] 資料夾的 SDK 中，讓您可以編譯著色器 (或在您選擇時) 離線效果。 請參閱從命令列執行編譯器的檔。

-   [Includes](#includes)
-   [巨集](#macros)
-   [HLSL 著色器旗標](#hlsl-shader-flags)
-   [FX 旗標](#fx-flags)
-   [檢查錯誤](#checking-errors)
-   [相關主題](#related-topics)

以下是從 BasicHLSL10 範例) 編譯效果檔案 (的範例。


```
WCHAR str[MAX_PATH];
DXUTFindDXSDKMediaFileCch( str, MAX_PATH, L"BasicHLSL10.fx" );

hr = D3DX10CompileEffectFromFile( str, NULL, NULL, "fx_4_0", 
    D3D10_SHADER_ENABLE_STRICTNESS, 0, pd3dDevice, NULL, NULL, 
    &l_pBlob_Effect, &l_pBlob_Errors, NULL );
```



## <a name="includes"></a>Includes

其中一個參數是 include 介面。 如果您想要在讀取包含檔案時包含自訂的行為，請產生其中一種。 此自訂行為會在每次建立使用 include 指標) 的效果 (，或編譯使用 include 指標) 的效果 (時執行。 若要執行自訂的 include 行為，請從 Include 介面衍生類別。 這會提供您的類別兩種方法：開啟和關閉。 在 Open 和 Close 方法中執行自訂行為。

## <a name="macros"></a>巨集

效果編譯也可以取得在其他位置定義的宏指標。 例如，假設您要在 BasicHLSL10 中修改效果，以使用兩個宏：零和一。 使用這兩個宏的效果程式碼如下所示。


```
if( bAnimate )
    vAnimatedPos += float4(vNormal, zero) *  
        (sin(g_fTime+5.5)+0.5)*5;
        
    Output.Diffuse.a = one;         
```



以下是兩個宏的宣告。


```
D3D_SHADER_MACRO Shader_Macros[3] = { "zero", "0", "one", "1.0f", NULL, NULL };
```



宏是以 Null 結束的宏陣列;其中每個宏都使用 [**D3D \_ 著色器 \_ 宏**](/windows/win32/api/d3dcommon/ns-d3dcommon-d3d_shader_macro) 結構來定義。

最後，修改編譯效果呼叫以取得宏的指標。


```
D3DX10CreateEffectFromFile( str, Shader_Macros, NULL, 
    D3D10_SHADER_ENABLE_STRICTNESS, 0, pd3dDevice, NULL, NULL, 
    &g_pEffect10, NULL );
```



## <a name="hlsl-shader-flags"></a>HLSL 著色器旗標

著色器旗標會指定 HLSL 編譯器的著色器條件約束。 這些旗標會影響著色器編譯器產生的程式碼，包括：

-   大小考慮：將程式碼優化。
-   調試因素：包含調試資訊，防止流量控制。
-   硬體考慮：編譯目標以及著色器是否可以在舊版硬體上執行。

一般而言，如果您未指定兩個衝突的特性，這些旗標可以邏輯方式結合。 如需旗標的清單，請參閱 [ (Direct3D 10) 的效果常數 ](d3d10-graphics-reference-effect-constants.md)。

## <a name="fx-flags"></a>FX 旗標

這些旗標是在建立效果來定義編譯行為或執行時間效果行為時使用。 如需旗標的清單，請參閱 [ (Direct3D 10) 的效果常數 ](d3d10-graphics-reference-effect-constants.md)。

## <a name="checking-errors"></a>檢查錯誤

如果在編譯期間發生錯誤，則 API 會傳回包含效果編譯器所傳回之錯誤的介面。 這個介面稱為 ID3D10Blob。 但是，它無法直接讀取，但藉由將指標傳回至包含資料 (的緩衝區（這是) 的字串），您就可以看到任何編譯錯誤。

在此範例中，藉由複製第一個變數宣告兩次，將錯誤引入 BasicHLSL。


```
//-------------------------------------------------------------------
// Global variables
//-------------------------------------------------------------------
float4 g_MaterialAmbientColor;      // Material's ambient color

// Declare the same variable twice
float4 g_MaterialAmbientColor;      // Material's ambient color
```



此錯誤會導致編譯器傳回下列錯誤，如 Microsoft Visual Studio 的 [監看式] 視窗的下列螢幕擷取畫面所示。

![visual studio [監看式] 視窗的螢幕擷取畫面](images/effect-compile-errors-2.jpg)

由於錯誤會在 LPVOID 指標中傳回，因此會將它轉換成 [監看式] 視窗中的字元字串。

以下是用來從失敗的編譯傳回錯誤的程式碼。


```
// Read the D3DX effect file
WCHAR str[MAX_PATH];
ID3D10Blob* l_pBlob_Effect = NULL;
ID3D10Blob* l_pBlob_Errors = NULL;
hr = DXUTFindDXSDKMediaFileCch( str, MAX_PATH, L"BasicHLSL10.fx" );
hr = D3DX10CompileEffectFromFile( str, NULL, NULL, 
    D3D10_SHADER_ENABLE_STRICTNESS, 0, NULL, 
    &l_pBlob_Effect, &l_pBlob_Errors );

LPVOID l_pError = NULL;
if( l_pBlob_Errors )
{
    l_pError = l_pBlob_Errors->GetBufferPointer();
    // then cast to a char* to see it in the locals window
}
```



## <a name="related-topics"></a>相關主題

<dl> <dt>

[轉譯 (Direct3D 10) 的效果 ](d3d10-graphics-programming-guide-effects-render.md)
</dt> </dl>

 

 



