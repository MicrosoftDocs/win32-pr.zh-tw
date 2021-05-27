---
title: 效果著色器連結
description: Direct2D 會使用稱為效果著色器的優化連結，此連結會將多個效果圖形轉譯傳遞合併成單一階段。
ms.assetid: 431A5B39-6C84-442D-AC66-0F341E10DF2C
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 75b6bad2170f2b897a5cf8ac3086a74945efa8bf
ms.sourcegitcommit: f848119a8faa29b27585f4df53f6e50ee9666684
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 05/27/2021
ms.locfileid: "110549233"
---
# <a name="effect-shader-linking"></a>效果著色器連結

Direct2D 會使用稱為效果著色器的優化連結，此連結會將多個效果圖形轉譯傳遞合併成單一階段。

-   [效果著色器連結總覽](#overview-of-effect-shader-linking)
-   [使用效果著色器連結](#using-effect-shader-linking)
-   [撰寫著色器連結相容的自訂效果](#authoring-a-shader-linking-compatible-custom-effect)
-   [連結相容效果著色器範例](#example-linking-compatible-effect-shader)
-   [編譯連結相容-著色器](#compiling-a-linking-compatible-shader)
    -   [步驟1：編譯匯出函數](#step-1-compile-the-export-function)
    -   [步驟2：編譯完整的著色器並內嵌匯出函式](#step-2-compile-the-full-shader-and-embed-the-export-function)
-   [匯出函式規格](#export-function-specifications)
-   [相關主題](#related-topics)

## <a name="overview-of-effect-shader-linking"></a>效果著色器連結總覽

效果著色器連結優化是以 HLSL 著色器連結為基礎，這是一項 Direct3D 11.2 功能，可讓您藉由連結預先編譯的著色器函式，在執行時間產生圖元和頂點著色器。 下圖說明效果圖形中效果著色器連結的概念。 第一個圖顯示具有四個轉譯轉換的典型 Direct2D 效果圖形。 如果沒有著色器連結，每個轉換都會取用轉譯行程，且需要中繼介面;此圖表總共需要4個階段和3個中繼。

![沒有著色器連結的轉換圖形：4階段和3中繼。](images/shader-transform-graph.png)

第二張圖顯示相同的效果圖形，其中每個轉譯轉換都已取代為可連結函式版本。 Direct2D 可以連結整個圖形，並在不需要任何中繼的情況下執行。 這可大幅降低 GPU 執行時間，並減少最大的 GPU 記憶體耗用量。

![具有著色器連結的轉換圖形：1次傳遞、0中繼。](images/shader-linking-graph.png)



 

效果著色器連結會在效果內的個別轉換上運作;這表示即使是具有單一效果的圖表，如果該效果有多個有效的轉換，也可能會受益于著色器連結。

## <a name="using-effect-shader-linking"></a>使用效果著色器連結

如果您要建立使用效果的 Direct2D 應用程式，則不需要執行任何動作，即可利用效果著色器連結。 Direct2D 會自動分析效果圖形，以決定連結每個轉換的最佳方式。

效果作者負責以支援效果著色器連結的方式來實行其效果;如需詳細資訊，請參閱下面的 [編寫著色器連結相容的自訂效果](#authoring-a-shader-linking-compatible-custom-effect) 一節。 所有內建效果都支援著色器連結。

Direct2D 只會在有用的情況下連結連續的轉譯轉換。 決定是否要連結兩個轉換時，會考慮多個因素。 例如，如果其中一個轉換使用頂點或計算著色器，則不會執行著色器連結，因為只有圖元著色器可以連結。 此外，如果未撰寫效果以與著色器連結相容，則周圍的轉換將不會與它連結。

如果有這類連結危險，Direct2D 就不會將任何轉換連結到危險的旁邊，但仍會嘗試連結圖形的其餘部分。

![具有連結危險的轉換圖形：2個通過，1個中繼。](images/shader-linking-graph-hazard.png)

## <a name="authoring-a-shader-linking-compatible-custom-effect"></a>撰寫著色器連結相容的自訂效果

如果您要撰寫自己的自訂 Direct2D 效果，您必須確定其轉換支援效果著色器連結。 這需要一些從先前的自訂效果執行的微小變更。 如果您自訂效果內的轉換不支援著色器連結，則 Direct2D 不會將它與效果圖形中任何與其連續的轉換連結。

如果您是自訂效果的作者，您應該留意幾項重要概念和需求：

-   **沒有變更效果介面的執行**

    您不需要修改任何執行各種效果介面的程式碼，例如 [ID2D1DrawTransform](/windows/win32/api/d2d1effectauthor/nn-d2d1effectauthor-id2d1drawtransform)。

-   **提供完整和匯出函式版本的著色器**

    您必須提供由 Direct2D 可連結之效果著色器的匯出函式版本。 此外，您也必須繼續提供原始的完整著色器;這是因為 Direct2D 會在執行時間根據著色器連結是否要套用至圖形中的特定連結來選取適當的著色器版本。

    如果轉換只透過 [ID2D1EffectCoNtext：： LoadPixelShader](/windows/win32/api/d2d1effectauthor/nf-d2d1effectauthor-id2d1effectcontext-loadpixelshader)) 提供完整的圖元著色器 blob (，則不會連結到連續的轉換。

- **Helper 函式**

    Direct2D 會提供 [HLSL helper](hlsl-helpers.md) 函式和宏，以自動產生著色器的完整和匯出函式版本。 這些協助程式可在 d2d1effecthelpers. hlsli 中找到。 此外，HLSL 編譯器 (FXC.EXE) 可讓您在完整著色器中，將匯出函數著色器插入私用欄位。 如此一來，您只需要撰寫一次著色器，並同時將這兩個版本傳遞至 Direct2D。 D2d1effecthelpers. hlsli 和 FXC.EXE 編譯器都會包含 Windows SDK 的一部分。

    Helper 函式：

  - [D2DGetInput](d2dgetinput.md)  
  - [D2DSampleInput](d2dsampleinput.md)  
  - [D2DSampleInputAtOffset](d2dsampleinputatoffset.md)  
  - [D2DSampleInputAtPosition](d2dsampleinputatposition.md)  
  - [D2DGetInputCoordinate](d2dgetinputcoordinate.md)  
  - [D2DGetScenePosition](d2dgetsceneposition.md)  
  - [D2D \_ PS \_ 專案](d2d-ps-entry.md)  

  您也可以手動撰寫每個著色器的兩個版本，並將它們編譯兩次，只要符合以下所述的匯出函式 [規格](#export-function-specifications) 中所述的規格。

-   **僅圖元著色器**

    Direct2D 不支援連結計算或頂點著色器。 但是，如果您的效果同時使用了頂點和圖元著色器，則圖元著色器的輸出仍可連結。

-   **簡單與複雜的取樣**

    著色器函式連結的運作方式是將一個圖元著色器的輸出連接到後續圖元著色器傳遞的輸入。 只有當取用的圖元著色器只需要單一輸入值來執行計算時，才可能發生這種情況;此值通常是從頂點著色器所發出的材質座標取樣輸入材質。 這類圖元著色器是用來執行簡單的取樣。

    ![灰階轉換是簡單取樣的範例。 特定輸出圖元的值只會取決於對應的輸入圖元值。](images/simple-sampling.png)

    某些圖元著色器（例如高斯模糊）會從多個輸入範例計算其輸出，而不只是單一樣本。 這類圖元著色器稱為執行複雜的取樣。

    

    ![高斯模糊是複雜取樣的範例。 中央輸出圖元的值取決於多個輸入圖元。](images/complex-sampling.png)

    
    只有具有簡單輸入的著色器函式可以有其他著色器函式提供的輸入。 具有複雜輸入的著色器函數必須提供輸入材質給範例。 這表示 Direct2D 不會將具有複雜輸入的著色器連結到其前身。

    使用「 [DIRECT2D HLSL](hlsl-helpers.md)協助程式」時，您必須在 HLSL 中指出著色器是否使用複雜或簡單的輸入。

## <a name="example-linking-compatible-effect-shader"></a>連結相容效果著色器範例

使用 D2D 協助程式時，下列程式碼片段代表簡單連結相容效果著色器：

```syntax
#define D2D_INPUT_COUNT 1
#define D2D_INPUT0_SIMPLE
#include “d2d1effecthelpers.hlsli”

D2D_PS_ENTRY(LinkingCompatiblePixelShader)
{
    float4 input = D2DGetInput(0);
    input.rgb *= input.a;
    return input;
}          
```

在這個簡短的範例中，請注意，不會宣告任何函式參數，每個輸入的輸入和類型數目是在輸入函式之前宣告，而是藉由呼叫 [D2DGetInput](d2dgetinput.md)來取出輸入，而且必須先定義預處理器指示詞，才能包含 helper 檔案。

連結相容的著色器必須同時提供一般的單一傳遞圖元著色器和匯出著色器函數。 當您搭配著色器編譯腳本使用時， [D2D \_ PS \_ 專案](d2d-ps-entry.md) 宏可讓您從相同的程式碼產生這些專案。

編譯完整的著色器時，宏會展開至下列程式碼，其中包含與 D2D 效果相容的輸入簽章。

```syntax
Texture2D<float4> InputTexture0;
SamplerState InputSampler0;

float4 LinkingCompatiblePixelShader(
    float4 pos   : SV_POSITION,
    float4 posScene : SCENE_POSITION,
    float4 uv0  : TEXCOORD0
    ) : SV_Target
    {
        float4 input = InputTexture0.Sample(InputSampler0, uv0.xy);
        input.rgb *= input.a;
        return input;
    }    
```

當編譯相同程式碼的匯出函數版本時，會產生下列程式碼：

```syntax
// Shader function version
export float4 LinkingCompatiblePixelShader_Function(
    float4 input0 : INPUT0)
    {
        input.rgb *= input.a;
        return input;
    }      
```

請注意，通常透過取樣 Texture2D 來取出的材質輸入已取代為函式輸入 (input0) 。

若要查看完整的逐步說明，瞭解您需要如何撰寫連結相容效果，請參閱 [自訂效果教學](custom-effects.md) 課程和 [Direct2D 自訂影像效果範例](https://github.com/microsoft/Windows-universal-samples/tree/master/Samples/D2DCustomEffects)。

## <a name="compiling-a-linking-compatible-shader"></a>編譯連結相容-著色器

若要可連結，傳遞給 D2D 的圖元著色器 blob 必須同時包含著色器的完整和匯出函式版本。 將已編譯的匯出函式內嵌至 D3D \_ BLOB 私用 \_ 資料區域，即可完成此作業 \_ 。

使用 D2D 協助程式函式撰寫著色器時，必須在編譯時定義 D2D 編譯目標。 編譯目標型別是 D2D \_ 完整 \_ 著色器和 d2d \_ 函數。

編譯連結相容效果著色器的程式有兩個步驟：

-   [編譯匯出函數](#step-1-compile-the-export-function)
-   [編譯完整的著色器並內嵌匯出函式](#step-2-compile-the-full-shader-and-embed-the-export-function)

> [!Note]  
> 使用 Visual Studio 編譯效果時，您應該建立一個批次檔來執行這兩個 FXC.EXE 命令，並執行這個批次檔做為編譯步驟之前執行的自訂群組建步驟。

 

### <a name="step-1-compile-the-export-function"></a>步驟1：編譯匯出函數

```syntax
fxc /T <shadermodel> <MyShaderFile>.hlsl /D D2D_FUNCTION /D D2D_ENTRY=<entry> /Fl <MyShaderFile>.fxlib           
```

若要編譯著色器的匯出函式版本，您必須將下列旗標傳遞給 FXC.EXE。



|    旗標                            |    描述                       |
|--------------------------------|-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| 一起 <ShaderModel>         | 設定 <ShaderModel> 為適當的圖元著色器設定檔，如 [fxc.exe 語法](/windows/desktop/direct3dtools/dx-graphics-tools-fxc-syntax)中所定義。 這必須是 [HLSL 著色器連結] 下所列的其中一個設定檔。 |
| <MyShaderFile>.hlsl      | 設定 <MyShaderFile> 為 HLSL 檔案的名稱。                                                                                                                                                                                                    |
| /D D2D \_ 函數               | 此定義會指示 FXC.EXE 編譯著色器的匯出函式版本。                                                                                                                                                                       |
| /D D2D \_ 專案 =<entry>    | 設定 <entry> 為您在 [D2D \_ PS \_ 專案](d2d-ps-entry.md) 宏中定義的 HLSL 進入點名稱。                                                                                                                                    |
| /Fl <MyShaderFile> . fxlib | 設定 <MyShaderfile> 為您要儲存著色器匯出函式版本的位置。 請注意，fxlib 副檔名只是為了方便識別。                                                                                              |

### <a name="step-2-compile-the-full-shader-and-embed-the-export-function"></a>步驟2：編譯完整的著色器並內嵌匯出函式

```syntax
fxc /T ps_<shadermodel> <MyShaderFile>.hlsl /D D2D_FULL_SHADER /D D2D_ENTRY=<entry> /E <entry> /setprivate <MyShaderFile>.fxlib /Fo <MyShader>.cso /Fh <MyShader>.h           
```

若要使用內嵌的匯出版本編譯著色器的完整版本，您必須將下列旗標傳遞給 FXC.EXE。



|    旗標                                    |    描述                     |
|----------------------------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| 一起 <ShaderModel>                 | 設定 <ShaderModel> 為適當的圖元著色器設定檔，如 [fxc.exe 語法](/windows/desktop/direct3dtools/dx-graphics-tools-fxc-syntax)中所定義。 這必須是對應至步驟1中所指定連結設定檔的圖元著色器設定檔。 |
| <MyShaderFile>.hlsl              | 設定 <MyShaderFile> 為 HLSL 檔案的名稱。                                                                                                                                                                                                                               |
| /D D2D \_ 完整 \_ 著色器                   | 此定義會指示 FXC.EXE 編譯完整版的著色器。                                                                                                                                                                                                             |
| /D D2D \_ 專案 =<entry>            | 設定 <entry> 為您在 D2D \_ PS 專案 () 宏中定義的 HLSL 進入點名稱 \_ 。                                                                                                                                                                                 |
| /E <entry>                       | 設定 <entry> 為您在 D2D \_ PS 專案 () 宏中定義的 HLSL 進入點名稱 \_ 。                                                                                                                                                                                 |
| /setprivate <MyShaderFile> . fxlib | 此引數會指示 FXC.EXE 將步驟1中產生的匯出函式著色器內嵌至 D3D \_ BLOB \_ 私用 \_ 資料區域。                                                                                                                                                          |
| /Fo <MyShader>               | 設定 <MyShader> 為，您要在其中儲存最後一個合併的編譯著色器。                                                                                                                                                                                                 |
| /Fh <MyShader> 。h                 | 設定 <MyShader> 為您要在其中儲存最後一個合併的標頭。                                                                                                                                                                                                          |

## <a name="export-function-specifications"></a>匯出函式規格

雖然不建議使用，但不建議使用 D2D 提供的協助程式撰寫相容效果著色器。 請務必小心，以確保完整的著色器和匯出函式輸入簽章都符合 D2D 規格。

完整著色器的規格與先前的 Windows 版本相同。 簡單地說，圖元著色器輸入參數必須是 SV \_ 位置、場景 \_ 位置和一個 TEXCOORD 的每個效果輸入。

針對 export 函式，函式必須傳回 float4，而且其輸入必須是下列其中一種類型：

-   簡單輸入

    ```syntax
    float4 d2d_inputN : INPUTN         
    ```

    針對簡單的輸入，D2D 會在輸入材質和著色器函式之間插入範例函式，否則會由另一個著色器函式的輸出提供輸入。

-   複雜輸入

    ```syntax
    float4 d2d_uvN  : TEXCOORDN                
    ```

    針對複雜的輸入，D2D 只會傳遞材質座標，如 Windows 8 檔中所述。

-   輸出位置

    ```syntax
    float4 d2d_posScene : SCENE_POSITION                
    ```

    只能定義一個場景 \_ 位置輸入。 只有在必要時才會包含這個參數，因為每個連結的著色器只有一個函式可以使用此參數。

必須如上面所述定義此語義，因為 D2D 將檢查此語義，以決定如何將函數連結在一起。 如果任何函式輸入不符合上述其中一個類型，則會拒絕著色器連結的函式。

## <a name="related-topics"></a>相關主題

<dl> <dt>

[HLSL 協助程式](hlsl-helpers.md)
</dt> <dt>

[ID3D11Linker 介面](/windows/desktop/api/d3d11shader/nn-d3d11shader-id3d11linker)
</dt> <dt>

[ID3D11FunctionLinkingGraph 介面](/windows/desktop/api/d3d11shader/nn-d3d11shader-id3d11functionlinkinggraph)
</dt> </dl>

 

 