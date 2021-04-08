---
title: HLSL 協助程式
description: 為了協助效果作者撰寫可連結圖元著色器，d2d1effecthelpers. hlsli 會以 helper 方法和宏的形式來定義一組 HLSL 語言延伸模組。
ms.assetid: 5D0BB99E-7C77-4D45-82E6-F038E4B752A4
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: ec8f43447c16d93ef9e1839ac319c761b975222a
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 09/16/2019
ms.locfileid: "103931980"
---
# <a name="hlsl-helpers"></a>HLSL 協助程式

為了協助效果作者撰寫可連結圖元著色器，d2d1effecthelpers. hlsli 會以 helper 方法和宏的形式來定義一組 HLSL 語言延伸模組。

若要將 d2d1effecthelpers hlsli 加入至您的專案，請 \# 在 HLSL 檔案中加入 include 語句。 d2d1effecthelpers 與其他 Direct2D 標頭位於相同的位置，例如 d2d1 .h;您可以從 HLSL 檔的屬性頁中參考它，方法是將宏 $ (WindowsSDK \_ IncludePath) 新增至其他 Include 目錄屬性。 請注意， \# include 語句必須在任何預處理器指示詞之後，也就是已定義的 D2D \_ 輸入 \_ 計數。

``` syntax
#include <d2d1effecthelpers.hlsli>
```

Direct2D 不支援連結計算或頂點著色器。 但是，如果您的效果同時使用了頂點著色器和圖元著色器，則圖元著色器的輸出仍可連結。

## <a name="preprocessor-directives"></a>前置處理器指示詞

需要預處理器指示詞才能傳達效果的相關資訊。 這包括每個輸入的輸入數目和取樣類型。 下列值應該在相關著色器進入點上方的效果著色器程式碼中定義（如果適用）。

-   `D2D_INPUT_COUNT <N>` ：宣告效果的材質輸入數目。 如果效果有不定數目的輸入，此值必須適當地設定為每個著色器進入點的範圍。 定義此值是必要的。
-   `D2D_INPUT<N>_SIMPLE` ：宣告第 n 個輸入以使用簡單取樣。 如果未定義，則第 n 個輸入預設為 [複雜]。 定義此值是選擇性的。
-   `D2D_INPUT<N>_COMPLEX` ：宣告第 n 個輸入以使用複雜的取樣。 如果未定義，則第 n 個輸入預設為 [複雜]。 定義此值是選擇性的。
-   `D2D_REQUIRES_SCENE_POSITION` ：表示著色器函式會呼叫使用場景位置值的 helper 方法 (亦即， [D2DGetScenePosition](d2dgetsceneposition.md) helper 函數) 。 只有在必要時才會包含這個參數，因為每個連結的著色器只有一個函式可以使用此參數。 定義此值是選擇性的。
-   `D2D_CUSTOM_ENTRY` ：表示圖元著色器函式會使用自訂頂點著色器的輸出，因此會宣告其輸入參數。 所有自訂頂點著色器輸入都會使用複雜的取樣，而且無法使用另一個著色器函式的輸出 (亦即，它們只是可連結後的) 。 定義此值是選擇性的。

例如：

``` syntax
#define D2D_INPUT_COUNT 3
#define D2D_INPUT0_SIMPLE
#define D2D_INPUT1_SIMPLE
#define D2D_INPUT2_COMPLEX
#include <d2d1effecthelpers.hlsli>
          
```

## <a name="helper-functions"></a>輔助函式

Helper 函式可用來取代某些原生 HLSL 內建函式。 在編譯時期，這些 helper 函式會由 Direct2D 重新定義為適當的版本，視編譯目標型別 (完整著色器或匯出函數) 而定。

Helper 函式：

<dl>

[D2DGetInput](d2dgetinput.md)  
[D2DSampleInput](d2dsampleinput.md)  
[D2DSampleInputAtOffset](d2dsampleinputatoffset.md)  
[D2DSampleInputAtPosition](d2dsampleinputatposition.md)  
[D2DGetInputCoordinate](d2dgetinputcoordinate.md)  
[D2DGetScenePosition](d2dgetsceneposition.md)  
[D2D \_ PS \_ 專案](d2d-ps-entry.md)  
</dl>

## <a name="related-topics"></a>相關主題

<dl> <dt>

[效果著色器連結](effect-shader-linking.md)
</dt> </dl>

 

 




