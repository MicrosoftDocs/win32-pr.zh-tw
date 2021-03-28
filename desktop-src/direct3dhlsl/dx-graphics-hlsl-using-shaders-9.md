---
title: 在 Direct3D 9 中使用著色器
description: 在 Direct3D 9 中使用著色器
ms.assetid: 8d8f5124-fbf3-4af5-8399-43ba28aa6eb9
ms.topic: article
ms.date: 05/31/2018
topic_type:
- kbArticle
api_name: ''
api_type: ''
api_location: ''
ms.openlocfilehash: 6455b47d24c1c83683ce8b85c48990bb32e221ae
ms.sourcegitcommit: 592c9bbd22ba69802dc353bcb5eb30699f9e9403
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/20/2020
ms.locfileid: "104990903"
---
# <a name="using-shaders-in-direct3d-9"></a>在 Direct3D 9 中使用著色器

-   [針對特定硬體編譯著色器](#compiling-a-shader-for-specific-hardware)
-   [初始化著色器常數](#initializing-shader-constants)
-   [將著色器參數系結至特定的註冊](#binding-a-shader-parameter-to-a-particular-register)
-   [呈現可程式化著色器](#rendering-a-programmable-shader)
-   [調試著色器](#debugging-shaders)
-   [相關主題](#related-topics)

## <a name="compiling-a-shader-for-specific-hardware"></a>針對特定硬體編譯著色器

第一次將著色器新增至 DirectX 8.0 中的 Microsoft DirectX。 屆時，已定義數個虛擬著色器機器，每個機器大致對應于前幾個3D 圖形廠商所產生的特定圖形處理器。 每個虛擬著色器機器都有設計組合語言。 寫入著色器模型的程式 (名稱與 \_ 1 \_ 1 和 ps \_ 1 \_ 1-ps \_ 1 \_ 4) 相對較短，通常是由開發人員直接以適當的元件語言撰寫。 應用程式會使用 [**D3DXAssembleShader**](/windows/desktop/direct3d9/d3dxassembleshader) 將這個人類可讀取的元件語言程式碼傳遞至 D3DX 程式庫，並取得著色器的二進位標記法，然後再使用 [**CreateVertexShader**](/windows/desktop/api/d3d9/nf-d3d9-idirect3ddevice9-createvertexshader) 或 [**CreatePixelShader**](/windows/desktop/api/d3d9/nf-d3d9-idirect3ddevice9-createpixelshader)來傳遞。 如需詳細資訊，請參閱軟體發展工具組 (SDK) 。

Direct3D 9 的情況很類似。 應用程式會使用 [**D3DXCompileShader**](/windows/desktop/direct3d9/d3dxcompileshader) 將 HLSL 著色器傳遞給 D3DX，並取得已編譯著色器的二進位標記法，然後使用 [**CreatePixelShader**](/windows/desktop/api/d3d9/nf-d3d9-idirect3ddevice9-createpixelshader) 或 [**CreateVertexShader**](/windows/desktop/api/d3d9/nf-d3d9-idirect3ddevice9-createvertexshader)將它傳遞給 Microsoft Direct3D。 執行時間不知道任何關於 HLSL 的作業，只是二進位的元件著色器模型。 這很好用，因為這表示 HLSL 編譯器可以獨立于 Direct3D 執行時間進行更新。 您也可以使用 [fxc.exe](/windows/desktop/direct3dtools/fxc)，離線編譯著色器。

除了開發 HLSL 編譯器之外，Direct3D 9 也引進了元件層級的著色器模型，以公開最新一代圖形硬體的功能。 應用程式開發人員可以在元件中使用這些新模型 (vs \_ 2 \_ 0、vs \_ 3 \_ 0、ps \_ 2 \_ 0、ps \_ 3 \_ 0) ，但我們預期大部分的開發人員都可以移至 HLSL 進行著色器開發。

當然，撰寫 HLSL 程式以表示特定網底演算法的能力並不會自動讓它在任何指定的硬體上執行。 應用程式會呼叫 D3DX，使用 [**D3DXCompileShader**](/windows/desktop/direct3d9/d3dxcompileshader)將著色器編譯成二進位元件程式碼。 這個進入點的其中一個限制是參數，其定義 (或編譯目標的元件層級模型，) HLSL 編譯器應該使用這些模型來表示最後的著色器程式碼。 如果應用程式在執行時間執行 HLSL 著色器編譯 (而不是編譯時間或離線) ，則應用程式可以檢查 Direct3D 裝置的功能，並選取要比對的編譯目標。 如果 HLSL 著色器中表示的演算法太複雜而無法在選取的編譯目標上執行，編譯將會失敗。 這表示，雖然 HLSL 對著色器開發有很大的好處，但它並不能讓開發人員從將遊戲交付給具有不同功能之圖形裝置的目標物件。 作為遊戲開發人員，您仍然必須管理視覺效果的分層式方法;這表示為更多功能的圖形卡片撰寫更好的著色器，並為較舊的卡片撰寫更基本的版本。 不過，有了妥善撰寫的 HLSL，就可以大幅分階段減緩這種負擔。

許多開發人員會在應用程式載入時間或第一次使用時，選擇在客戶的電腦上使用 D3DX 編譯 HLSL 著色器，而不是在出貨之前，將其著色器從 HLSL 編譯成二進位程式碼。 這會讓其 HLSL 的原始程式碼遠離窺探的眼睛，也可確保其應用程式執行的所有著色器都已通過其內部品質保證程式。 離線編譯著色器的方便公用程式是 [fxc.exe](/windows/desktop/direct3dtools/fxc)。 此工具有許多選項，可讓您用來編譯指定之編譯目標的程式碼。 如果您想要將您的著色器優化，或通常會在更詳細的層級上瞭解虛擬著色器電腦的功能，在開發期間，將拆解的輸出視為非常教育。 以下摘要說明這些選項：

## <a name="initializing-shader-constants"></a>初始化著色器常數

著色器常數包含在常數資料表中。 您可以使用 [**ID3DXConstantTable**](/windows/desktop/direct3d9/id3dxconstanttable) 介面來存取此。 全域著色器變數可以在著色器程式碼中初始化。 這些會藉由呼叫 [**SetDefaults**](/windows/desktop/direct3d9/id3dxconstanttable--setdefaults)在執行時間初始化。

## <a name="binding-a-shader-parameter-to-a-particular-register"></a>將著色器參數系結至特定的註冊

編譯器會自動將暫存器指派給全域變數。 編譯器會將環境指派給取樣器 register s0、SparkleNoise 至取樣器 register s1，以及 k \_ s 到常數登錄 c0 (假設尚未針對下列三個全域變數指派) 的其他取樣器或常數暫存器：


```
sampler Environment;
sampler SparkleNoise;
float4 k_s;
```



您也可以將變數系結至特定的註冊。 若要強制編譯器指派給特定的註冊，請使用下列語法：


```
register(RegisterName)
```



其中 register 是特定暫存器的名稱。 下列範例示範特定的暫存器指派語法，其中取樣器環境會系結至取樣器 register s1、SparkleNoise 會系結至取樣器 register s0，而 k s 將會系結 \_ 至常數暫存器 c12：


```
sampler Environment : register(s1);
sampler SparkleNoise : register(s0);
float4 k_s : register(c12);
```



## <a name="rendering-a-programmable-shader"></a>呈現可程式化著色器

著色器的呈現方式是在裝置中設定目前的著色器、初始化著色器常數、告知裝置有不同輸入資料的來源，最後呈現基本專案。 每個都可以藉由分別呼叫下列方法來完成：

-   [**SetVertexShader**](/windows/desktop/api/d3d9helper/nf-d3d9helper-idirect3ddevice9-setvertexshader)
-   [**SetVertexShaderConstantF**](/windows/desktop/api/d3d9helper/nf-d3d9helper-idirect3ddevice9-setvertexshaderconstantf)
-   [**SetStreamSource**](/windows/desktop/api/d3d9helper/nf-d3d9helper-idirect3ddevice9-setstreamsource)
-   [**DrawPrimitive**](/windows/desktop/api/d3d9/nf-d3d9-idirect3ddevice9-drawprimitive)

## <a name="debugging-shaders"></a>調試著色器

適用于 Microsoft Visual Studio .NET 的 DirectX 擴充功能可在 Visual Studio .NET 整合式開發環境中，提供完全整合的 HLSL 偵錯工具 (IDE) 。 為了準備著色器的偵錯工具，您必須在您的電腦上安裝正確的工具 (請參閱 [Visual Studio (Direct3D 9) ) 中的偵錯工具著色 ](dx-graphics-hlsl-debug-visual-studio.md) 器。

## <a name="related-topics"></a>相關主題

<dl> <dt>

[HLSL 的程式設計指南](dx-graphics-hlsl-pguide.md)
</dt> </dl>

 

 