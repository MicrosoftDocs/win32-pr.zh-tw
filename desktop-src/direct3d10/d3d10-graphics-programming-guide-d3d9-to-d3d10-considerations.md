---
description: 下列頁面提供 Direct3D 9 與 Direct3D 10 之間主要差異的基本大綱。 以下大綱提供一些見解，協助開發人員使用 Direct3D 9 體驗來探索及與 Direct3D 10 相關。
ms.assetid: 283b54e0-94cb-47a8-8cfc-5798e0538b9f
title: 'Direct3d 9 至 direct3d 10 考慮 (direct3d 10) '
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 9e6c2dac7da24184bb5cc6a78f8e7d391c7d0f8b7000107915ba5a606188dcf4
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/11/2021
ms.locfileid: "120120008"
---
# <a name="direct3d-9-to-direct3d-10-considerations-direct3d-10"></a>Direct3d 9 至 direct3d 10 考慮 (direct3d 10) 

下列頁面提供 Direct3D 9 與 Direct3D 10 之間主要差異的基本大綱。 以下大綱提供一些見解，協助開發人員使用 Direct3D 9 體驗來探索及與 Direct3D 10 相關。

雖然本主題中的資訊會將 Direct3D 9 與 Direct3D 10 相比較，因為 Direct3D 11 建基於 Direct3D 10 和10.1 的改進，您也需要此資訊，才能從 Direct3D 9 遷移至 Direct3D 11。 如需將 Direct3D 10 移至 Direct3D 11 以外的詳細資訊，請參閱 [遷移至 direct3d 11](../direct3d11/d3d11-programming-guide-migrating.md)。

-   [介紹 Direct3D 10 中的主要結構變更](#overview-of-the-major-structural-changes-in-direct3d-10)
    -   [移除 Fixed 函數](#removal-of-fixed-function)
    -   [裝置物件建立時間驗證](#device-object-creation-time-validation)
-   [引擎抽象/分隔](/windows)
    -   [直接移除 Direct3D 9 相依性](#direct-removal-of-direct3d-9-dependencies)
-   [快速解決應用程式組建問題的訣竅](#tricks-for-quickly-resolving-application-build-issues)
    -   [覆寫 Direct3D 9 類型](#overriding-direct3d-9-types)
    -   [解決連結問題](#resolving-link-issues)
    -   [模擬裝置帽](#simulating-device-caps)
-   [驅動 Direct3D 10 API](#driving-the-direct3d-10-api)
    -   [資源建立](#resource-creation)
    -   [檢視](#views)
    -   [靜態與動態資源存取](#static-versus-dynamic-resource-access)
    -   [Direct3D 10 效果](#direct3d-10-effects)
    -   [HLSL 不會有任何影響](#hlsl-without-effects)
    -   [著色器編譯](#shader-compilation)
    -   [建立著色器資源](#creation-of-shader-resources)
    -   [著色器反映圖層介面](#shader-reflection-layer-interface)
    -   [輸入組合語言版面配置-頂點著色器/輸入資料流程連結](/windows)
    -   [著色器失效程式碼移除的影響](#impact-of-shader-dead-code-removal)
    -   [頂點著色器輸入結構範例](#vertex-shader-input-structure-example)
    -   [狀態物件建立](#state-object-creation)
-   [移植紋理](#porting-textures)
    -   [支援的檔案格式](#file-formats-supported)
    -   [對應材質格式](#mapping-texture-formats)
-   [移植著色器](#porting-shaders)
    -   [Direct3D 10 著色器是在 HLSL 中撰寫的](#direct3d-10-shaders-are-authored-in-hlsl)
    -   [著色器簽章和連結](#shader-signatures-and-linkage)
    -   [HLSL 著色器階段連結](#hlsl-shader-stage-linkages)
    -   [常數緩衝區](#constant-buffers)
    -   [功能層級9和更新版本上 HLSL 的使用者剪輯平面](#user-clip-planes-in-hlsl-on-feature-level-9-and-higher)
-   [要監看的其他 Direct3D 10 差異](#additional-direct3d-10-differences-to-watch-for)
    -   [整數作為輸入](#integers-as-input)
    -   [滑鼠游標](#mouse-cursors)
    -   [將材質對應至 Direct3D 10 中的圖元](#mapping-texels-to-pixels-in-direct3d-10)
    -   [參考計數行為變更](#reference-counting-behavior-changes)
    -   [測試合作層級](#test-cooperative-level)
    -   [StretchRect](#stretchrect)
-   [其他 Direct3D 10.1 差異](#additional-direct3d-101-differences)
-   [相關主題](#related-topics)

## <a name="overview-of-the-major-structural-changes-in-direct3d-10"></a>介紹 Direct3D 10 中的主要結構變更

-   [移除 Fixed 函數](#removal-of-fixed-function)
-   [裝置物件建立時間驗證](#device-object-creation-time-validation)

使用 Direct3D 10 裝置轉譯的程式在結構上類似于 Direct3D 9。

-   設定頂點資料流程來源
-   在 direct3d 10 中設定輸入配置 (在 Direct3D 9 中設定頂點資料流程宣告) 
-   宣告基本拓撲
-   設定紋理
-   設定狀態物件
-   設定著色器
-   Draw

[**Draw**](/windows/desktop/api/D3D10/nf-d3d10-id3d10device-draw)呼叫會將這些作業結合在一起;繪製呼叫之前的呼叫順序是任意的。 Direct3D 10 API 設計的主要差異如下：

-   移除 Fixed 函數
-   已保證移除 CAPS bits-Direct3D 10 的基本功能集
-   更嚴格的管理：資源存取、裝置狀態、著色器常數、著色器連結 (輸入和輸出，以在階段之間) 著色器
-   API 進入點名稱的變更反映了虛擬 GPU 記憶體 (Map () 的使用，而不是鎖定 () ) 。
-   您可以在建立時將調試層新增至裝置
-   基本拓撲現在是與 [**繪製**](/windows/desktop/api/D3D10/nf-d3d10-id3d10device-draw) 呼叫分開的明確狀態 () 
-   明確的著色器常數現在會儲存在常數緩衝區中
-   著色器撰寫完全是在 HLSL 中完成。 HLSL 編譯器現在位於主要 Direct3D 10 DLL 中。
-   新的可程式化階段-幾何著色器
-   移除 BeginScene () /EndScene () 
-   在新元件中執行的通用2D、焦點和介面卡管理功能： DXGI

### <a name="removal-of-fixed-function"></a>移除 Fixed 函數

有時候，即使在可充分利用可程式化管線的 Direct3D 9 引擎中，仍會有一些相依于 fixed 函式 (FF) 管線的區域。 最常見的區域通常與 UI 的螢幕空間對齊呈現相關。 基於這個原因，您可能需要建立 FF 模擬著色器或一組著色器，以提供必要的取代行為。

本檔包含的白皮書包含最常見 FF 行為的取代著色器來源 (參閱固定的函式 [EMU 範例](https://msdn.microsoft.com/library/Ee416406(v=VS.85).aspx)) 。 某些固定函數的圖元行為（包括 Alpha 測試）已移至著色器。

### <a name="device-object-creation-time-validation"></a>裝置物件建立時間驗證

在硬體和軟體中，已從頭開始重新設計 Direct3D 10 管線，主要目的是要降低 (在繪製時間) 的 CPU 額外負荷。 為了降低成本，已指派具有裝置本身所提供明確建立方法的物件給所有類型的裝置資料。 如此一來，就能在建立物件時，而不是在繪製呼叫期間進行嚴格的資料驗證，因為它經常會使用 Direct3D 9。

## <a name="engine-abstractions--separation"></a>引擎抽象/分隔

想要支援 Direct3D 9 和 Direct3D 10 的應用程式（包括遊戲）必須從程式碼基底的其餘部分抽象化轉譯層。 有許多方法可達成此目的，但所有這些方法都是較低層級 Direct3D 裝置之抽象層的設計。 所有系統都應該透過通用層（設計用來提供 GPU 資源和低層級類型管理）來與硬體通訊。

### <a name="direct-removal-of-direct3d-9-dependencies"></a>直接移除 Direct3D 9 相依性

在移植大型、先前測試過的程式碼基底時，請務必將程式碼變更的數量降到最低，以在程式碼中保留先前測試的行為。 最佳做法包括清楚地記錄專案使用批註變更的位置。 針對此工作提供批註標準通常很有用，這可讓您快速流覽程式碼基底。

以下是可用於這項工作的標準單行/開始區塊批註清單範例。



| 項目                                                                                                                                                                             | 描述                                                                                                                                                                                                                                                                                                                    |
|----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span id="___Direct3D_10_REMOVED"></span><span id="___direct3d_10_removed"></span><span id="___DIRECT3D_10_REMOVED"></span>已移除 Direct3D 10<br/>                     | 在程式碼的行/區塊移除的情況下使用此項<br/>                                                                                                                                                                                                                                                                   |
| <span id="___Direct3D_10_NEEDS_UPDATE"></span><span id="___direct3d_10_needs_update"></span><span id="___DIRECT3D_10_NEEDS_UPDATE"></span>Direct3D 10 需要更新<br/> | 這有助於將其他注意事項新增至需要更新批註，以建議應使用哪些工作/新 API，以供稍後造訪行為轉換的程式碼。 大量使用 assert (**false**) 也應該在 \\ \\ Direct3D 10 需要更新時使用，以確保您不會在不知情的情況下執行不當程式碼。<br/> |
| <span id="___Direct3D_10_CHANGED"></span><span id="___direct3d_10_changed"></span><span id="___DIRECT3D_10_CHANGED"></span>Direct3D 10 已變更<br/>                     | 發生重大變更的區域應保留供日後參考，但已批註化<br/>                                                                                                                                                                                                                       |
| <span id="___Direct3D_10_END"></span><span id="___direct3d_10_end"></span><span id="___DIRECT3D_10_END"></span>Direct3D 10 結束<br/>                                     | 結束程式碼區塊辨識符號<br/>                                                                                                                                                                                                                                                                                            |



 

針對多行來源，您也應該使用 C 樣式/ \* \* /批註，但在這些區域周圍新增相關的開始/結束批註。

## <a name="tricks-for-quickly-resolving-application-build-issues"></a>快速解決應用程式組建問題的訣竅

-   [覆寫 Direct3D 9 類型](#overriding-direct3d-9-types)
-   [解決連結問題](#resolving-link-issues)
-   [模擬裝置帽](#simulating-device-caps)

### <a name="overriding-direct3d-9-types"></a>覆寫 Direct3D 9 類型

插入包含 direct3d 10 標頭已不再支援之 Direct3D 9 基底類型之類型定義/覆寫的高階標頭檔時，可能會很有用。 這可協助您將程式碼和介面中的變更量降至最低，其中從 Direct3D 9 類型直接對應至新定義的 Direct3D 10 類型。 這種方法也適用于在一個原始程式檔中將程式程式碼為保持在一起。 在這種情況下，最好是定義版本中性/一般命名的型別，這些型別會描述用於轉譯的一般結構，而這兩者都是在 Direct3D 9 和 Direct3D 10 Api 中。 例如：


```
#if defined(D3D9)
typedef IDirect3DIndexBuffer9   IDirect3DIndexBuffer;
typedef IDirect3DVertexBuffer9  IDirect3DVertexBuffer;
#else //D3D10
typedef ID3D10Buffer            IDirect3DIndexBuffer;
typedef ID3D10Buffer            IDirect3DVertexBuffer
#endif
```



其他的 Direct3D 10 特定範例包括：


```
typedef ID3D10TextureCube   IDirect3DCubeTexture;
typedef ID3D10Texture3D     IDirect3DVolumeTexture;
typedef D3D10_VIEWPORT      D3DVIEWPORT;
typedef ID3D10VertexShader  IDirect3DVertexShader;
typedef ID3D10PixelShader   IDirect3DPixelShader;
```



### <a name="resolving-link-issues"></a>解決連結問題

建議使用最新版本的 Microsoft Visual Studio 來開發 Direct3D 10 和 Windows Vista 應用程式。 不過，您可以使用舊版 Visual Studio 的2003版本，建立相依于 Direct3D 10 的 Windows Vista 應用程式。 Direct3D 10 是 Windows Vista 平臺元件，其相依性 (與下列 lib 上的 Server 2003 SP1 platform SDK) 相同：需要 BufferOverflowU .lib 才能解決任何緩衝區 \_ 安全性檢查連結器問題。

### <a name="simulating-device-caps"></a>模擬裝置帽

許多應用程式包含的程式碼區域相依于可用的裝置 CAP 資料。 解決此問題的方法是覆寫裝置列舉，並強制裝置帽成為合理的值。 規劃重新流覽某些區域，在此情況下，會在可能的情況下完全移除 caps 的端點。

## <a name="driving-the-direct3d-10-api"></a>驅動 Direct3D 10 API

本節著重于 Direct3D 10 API 所造成的行為變更。

-   [資源建立](#resource-creation)
-   [檢視](#views)
-   [靜態與動態資源存取](#static-versus-dynamic-resource-access)
-   [Direct3D 10 效果](#direct3d-10-effects)
-   [HLSL 不會有任何影響](#hlsl-without-effects)
-   [著色器編譯](#shader-compilation)
-   [建立著色器資源](#creation-of-shader-resources)
-   [著色器反映圖層介面](#shader-reflection-layer-interface)
-   [輸入組合語言版面配置-頂點著色器/輸入資料流程連結](/windows)
-   [著色器失效程式碼移除的影響](#impact-of-shader-dead-code-removal)
-   [頂點著色器輸入結構範例](#vertex-shader-input-structure-example)
-   [狀態物件建立](#state-object-creation)

### <a name="resource-creation"></a>資源建立

Direct3D 10 API 將資源設計為泛型緩衝區類型，而這些類型根據計畫的使用方式有特定的系結旗標。 選擇此設計點有助於在管線中近乎普遍地存取管線中的資源，例如轉譯為頂點緩衝區，然後立即繪製結果，而不會中斷 CPU。 下列範例示範頂點緩衝區和索引緩衝區的配置，您可以在其中看到資源描述只與 GPU 資源系結旗標不同。

Direct3D 10 API 已提供紋理協助程式方法來明確建立材質類型資源，但您可以想像，這些是真正的協助程式函式。

-   CreateTexture2D () 
-   CreateTextureCube () 
-   CreateTexture3D () 

以 Direct3D 10 為目標時，您可能會想要在資源建立期間配置更多專案，而不是與 Direct3D 9 搭配使用的專案。 建立轉譯目標緩衝區和材質時，這會變得最明顯，您也需要建立一個可存取緩衝區的視圖，並在裝置上設定資源。

[教學課程1： Direct3D 10 基本概念](https://msdn.microsoft.com/library/Ee416436(v=VS.85).aspx)

> [!Note]  
> Direct3D 10 和更新版本的 Direct3D 會擴充 DDS 檔案格式，以支援新的 DXGI 格式、材質陣列和 cube 對應陣列。 如需有關 DDS 檔案格式延伸模組的詳細資訊，請參閱 [dds 的程式設計指南](../direct3ddds/dx-graphics-dds-pguide.md)。

 

### <a name="views"></a>檢視

View 是特定類型的介面，可將資料儲存在圖元緩衝區中。 資源一次可以有多個已配置的視圖，而且此功能會在此 SDK 所包含的單一行程轉譯為立方體貼圖範例中反白顯示。

[資源存取的程式設計人員指南頁面](d3d10-graphics-programming-guide-resources-access-views.md)

[立方體貼圖範例](https://msdn.microsoft.com/library/Ee416398(v=VS.85).aspx)

### <a name="static-versus-dynamic-resource-access"></a>靜態與動態資源存取

為了達到最佳效能，應用程式應該根據資料的靜態與動態性質來分割資料的使用。 Direct3D 10 的設計目的是要利用這種方法，因此，資源的存取規則在 Direct3D 9 上已大幅加強。 針對靜態資源，您最好在建立期間將資源填入其資料。 如果您的引擎是在 Direct3D 9 的 [建立]、[鎖定]、[填滿]、[解除鎖定] 設計階段點所設計，您可以在資源介面上使用暫存資源和 UpdateSubResource 方法，來延遲從建立時間進行的擴展。

### <a name="direct3d-10-effects"></a>Direct3D 10 效果

使用 Direct3D 10 效果系統不在本文的討論範圍內。 系統已撰寫為可充分利用 Direct3D 10 所提供的架構優點。 如需其用法的詳細資訊，請參閱 [ (Direct3D 10) ](d3d10-graphics-programming-guide-effects.md) 一節中的效果。

### <a name="hlsl-without-effects"></a>HLSL 不會有任何影響

在不使用 Direct3D 10 效果系統的情況下，可能會驅動 Direct3D 10 著色器管線。 請注意，在此情況下，所有的常數緩衝區、著色器、取樣器和材質系結都必須由應用程式本身管理。 如需詳細資訊，請參閱本檔的範例連結和下列各節：

[HLSL 無效果範例](https://msdn.microsoft.com/library/Ee416414(v=VS.85).aspx)

### <a name="shader-compilation"></a>著色器編譯

Direct3D 10 HLSL 編譯器為 HLSL 語言定義帶來了一些增強功能，因此能夠以2種模式操作。 如需 Direct3D 9 樣式內建函式和語義的完整支援，應使用可根據每個編譯來指定的相容性模式旗標來叫用編譯。

您可以在 [HLSL](../direct3dhlsl/dx-graphics-hlsl.md)中找到適用于 Direct3D 10 的著色器模型4.0 特定 HLSL 語言語義和內建函式。 從 Direct3D 9 HLSL 的語法中，最重要的變更是在材質存取區域中。 新的語法是編譯器在相容性模式之外唯一支援的形式。

> [!Note]  
> direct3d 10 編譯器類型 api ([**D3D10CompileShader**](/windows/desktop/api/D3D10Shader/nf-d3d10shader-d3d10compileshader)和 [**D3D10CompileEffectFromMemory**](/windows/desktop/api/D3D10Effect/nf-d3d10effect-d3d10compileeffectfrommemory)) 是由 Windows Vista 和更新版本中執行的 direct3d 10、10.1 和11執行時間所提供。 Direct3D 10 編譯器類型 Api 的功能與 (2006 年12月) 的 DirectX SDK 隨附的 HLSL 編譯器相同。 此 HLSL 編譯器不支援 Direct3D 10.1 設定檔 (vs \_ 4 \_ 1、ps \_ 4 \_ 1、gs \_ 4 \_ 1、fx \_ 4 \_ 1) ，而且缺少一些優化和改進功能。 您可以從最新的舊版 [DIRECTX SDK 版本](/previous-versions/windows/apps/hh452744(v=win.10))取得支援 Direct3D 10.1 設定檔的 HLSL 編譯器。 如需舊版 DirectX SDK 的詳細資訊，請參閱 [什麼是 DIRECTX sdk？](../directx-sdk--august-2009-.md)。 您可以從 Windows SDK 取得最新的 HLSL Fxc.exe 命令列編譯器和[D3DCompiler](../direct3dhlsl/dx-graphics-d3dcompiler-reference.md) api。

 

### <a name="creation-of-shader-resources"></a>建立著色器資源

在 Direct3D 10 效果系統之外建立已編譯的著色器實例，在 direct3d 10 中是以類似于 Direct3D 9 的方式來完成，不過在 Direct3D 10 中，請務必將著色器輸入簽章保留下來以供稍後使用。 預設會將簽章傳回為著色器 blob 的一部分，但可能會進行解壓縮以減少記憶體需求（如有需要）。 如需詳細資訊，請參閱 [在 Direct3D 10 中使用著色](../direct3dhlsl/dx-graphics-hlsl-using-shaders-10.md)器。

### <a name="shader-reflection-layer-interface"></a>著色器反映圖層介面

著色器反映圖層是可取得著色器需求相關資訊的介面。 這在建立輸入元件的連結時特別有用 (請參閱下面) 您可能需要跨越著色器輸入需求，以確保您將正確的輸入結構提供給著色器。 您可以建立一個反映層介面的實例，同時建立已編譯著色器的實例。

著色器反映圖層會取代提供類似功能的 D3DX9 方法。 例如， [**IsParameterUsed**](../direct3d9/id3dxeffect--isparameterused.md) 會被 [**GetDesc**](/windows/desktop/api/D3D10Shader/nf-d3d10shader-id3d10shaderreflectionvariable-getdesc) 方法取代。

### <a name="input-assembler-layouts---vertex-shader--input-stream-linkage"></a>輸入組合語言版面配置-頂點著色器/輸入資料流程連結

 (IA) 的輸入組合語言取代了 Direct3D 9 樣式頂點資料流程宣告，而它的描述結構在表單中非常類似。 IA 的主要差異在於，所建立的 IA 設定物件必須直接對應至著色器輸入簽章的特定格式。 為了將輸入資料流程連結至著色器所建立的對應物件，可用於任何數目的著色器，其中著色器輸入簽章符合用來建立輸入配置的著色器。

為了充分利用靜態資料驅動管線，您應該考慮將輸入資料流程格式排列至可能的著色器輸入簽章，並儘早建立 IA 設定物件實例，並盡可能重複使用它們。

### <a name="impact-of-shader-dead-code-removal"></a>著色器失效程式碼移除的影響

下一節將詳細說明 Direct3D 9 和 Direct3D 10 之間的重大差異，這可能需要在您的引擎程式碼中謹慎處理。 包含條件運算式的著色器通常會在編譯過程中移除特定的程式碼路徑。 在 Direct3D 9 中，可能會移除兩種類型的輸入， (標示為移除) 未使用：簽章輸入 (如下列範例所示) 和常數輸入。 如果常數緩衝區的結尾包含未使用的專案，則著色器中的大小宣告會反映常數緩衝區的大小，但結尾沒有未使用的專案。 這兩種類型的輸入都會保留在簽章或常數緩衝區 Direct3D 10 中，在常數緩衝區結尾沒有未使用的常數輸入時，會有特殊的例外狀況。 這可能會在處理大型著色器和建立輸入配置時，對引擎造成影響。 編譯器中的無效程式碼優化所移除的元素，仍然必須在輸入結構中宣告。 下列範例為其示範：

### <a name="vertex-shader-input-structure-example"></a>頂點著色器輸入結構範例


```
struct VS_INPUT
{
float4 pos: SV_Position;
float2 uv1 : Texcoord1;
float2 uv2 : Texcoord2; *
};
```



\* Direct3D 9 解除程式碼移除會移除著色器中的宣告，因為無法移除條件式的程式碼


```
float4x4  g_WorldViewProjMtx;
static const bool g_bLightMapped = false; // define a compile time constant

VS_INPUT main(VS_INPUT i) 
{
    VS_INPUT o;
    o.pos = mul( i.pos, g_WorldViewProjMtx);
    o.uv1 = i.uv1;
    if ( g_bLightMapped )
    {
        o.uv2 = i.uv2;
    }
    return o;
}
```



或者，您可以使用下列宣告更明顯地指出常數是編譯時間常數：


```
#define LIGHT_MAPPED false
```



在上述範例中，在 Direct3D 9 下，uv2 元素將會因為編譯器中的無效程式碼優化而遭到移除。 在 Direct3D 10 下，仍會移除不正確程式碼，但著色器輸入組合器配置需要輸入資料的定義才能存在。 著色器反映圖層提供以一般方式處理這種情況的方法，讓您可以流覽著色器的輸入需求，並確保您將輸入資料流程的完整描述提供給著色器簽章對應。

以下是在函式簽章中偵測語義名稱/索引是否存在的範例函數：


```
// Returns true if the SemanticName / SemanticIndex is used in the input signature.
// pReflector is a previously acquired shader reflection interface.
bool IsSignatureElementExpected(ID3D10ShaderReflection *pReflector, const LPCSTR SemanticName, UINT SemanticIndex)
{
    D3D10_SHADER_DESC               shaderDesc;
    D3D10_SIGNATURE_PARAMETER_DESC  paramDesc;

    Assert(pReflector);
    Assert(SemanticName);

    pReflector->GetDesc(&shaderDesc);

    for (UINT k=0; k<shaderDesc.InputParameters; k++)
    {
        pReflector->GetInputParameterDesc( k, &paramDesc);
        if (wcscmp( SemanticName, paramDesc.SemanticName)==0 && paramDesc.SemanticIndex == SemanticIndex) 
            return true;
    }

    return false;
}
```



### <a name="state-object-creation"></a>狀態物件建立

移植引擎程式碼時，一開始可能有助於一開始使用一組預設的狀態物件，並停用所有的 Direct3D 9 裝置轉譯狀態/材質狀態設定。 這會導致轉譯成品，但這是啟動並執行專案的最快方法。 您稍後可以使用複合索引鍵來建立狀態物件管理系統，以允許最大重複使用所使用的狀態物件數目。

## <a name="porting-textures"></a>移植紋理

### <a name="file-formats-supported"></a>支援的檔案格式

**D3DXxxCreateXXX** 和 **D3DXxxSaveXXX** 函式會從圖形檔案建立或儲存材質 (例如， [**D3DX10CreateTextureFromFile**](d3dx10createtexturefromfile.md)) 支援 direct3d 10 中的一組不同檔案格式，而不是在 direct3d 9 中執行：



| 檔案格式 | Direct3D 9 | Direct3D 10 |
|-------------|------------|-------------|
| .bmp        | x          | x           |
| .jpg        | x          | x           |
| .tga        | x          |             |
| .png        | x          | x           |
| .dds        | x          | x           |
| ppm        | x          |             |
| .dib        | x          |             |
| 。 hdr        | x          |             |
| .pfm        | x          |             |
| .tiff       |            | x           |
| .gif        |            | x           |
| .tif        |            | x           |



 

如需詳細資訊，請將 Direct3D 9 [**D3DXIMAGE \_ >fileformat**](../direct3d9/d3dximage-fileformat.md) 列舉與 Direct3d 10 的 [**D3DX10 \_ 圖像 \_ 檔 \_ 格式**](d3dx10-image-file-format.md) 列舉進行比較。

> [!Note]  
> Windows 8 已淘汰 D3DX (D3DX 9、D3DX 10 和 D3DX 11) 公用程式程式庫。 針對材質檔案處理，建議您使用 [DirectXTex](https://github.com/Microsoft/DirectXTex)。

 

### <a name="mapping-texture-formats"></a>對應材質格式

下表顯示從 Direct3D 9 到 Direct3D 10 的材質格式對應。 在 DXGI 中無法使用的任何格式內容都必須由公用程式常式進行轉換。



| Direct3D 9 格式                   | Direct3D 10 格式                                                                                                                                                                                                                                   |
|-------------------------------------|------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| D3DFMT \_ 不明                     | DXGI \_ 格式 \_ 未知                                                                                                                                                                                                                                |
| D3DFMT \_ R8G8B8                      | 無法使用                                                                                                                                                                                                                                        |
| D3DFMT \_ A8R8G8B8                    | DXGI \_ format \_ B8G8R8A8 \_ UNORM & DXGI \_ format \_ B8G8R8A8 \_ UNORM \_ SRGB ¹                                                                                                                                                                                 |
| D3DFMT \_ X8R8G8B8                    | DXGI \_ format \_ B8G8R8X8 \_ UNORM & DXGI \_ format \_ B8G8R8X8 \_ UNORM \_ SRGB ¹                                                                                                                                                                                 |
| D3DFMT \_ R5G6B5                      | DXGI \_ 格式 \_ B5G6R5 \_ UNORM ²                                                                                                                                                                                                                         |
| D3DFMT \_ X1R5G5B5                    | 無法使用                                                                                                                                                                                                                                        |
| D3DFMT \_ A1R5G5B5                    | DXGI \_ 格式 \_ B5G5R5A1 \_ UNORM ²                                                                                                                                                                                                                       |
| D3DFMT \_ A4R4G4B4                    | DXGI \_ 格式 \_ B4G4R4A4 \_ UNORM ³                                                                                                                                                                                                                       |
| D3DFMT \_ R3G3B2                      | 無法使用                                                                                                                                                                                                                                        |
| D3DFMT \_ A8                          | DXGI \_ 格式 \_ A8 \_ UNORM                                                                                                                                                                                                                              |
| D3DFMT \_ A8R3G3B2                    | 無法使用                                                                                                                                                                                                                                        |
| D3DFMT \_ X4R4G4B4                    | 無法使用                                                                                                                                                                                                                                        |
| D3DFMT \_ A2B10G10R10                 | DXGI \_ 格式 \_ R10G10B10A2                                                                                                                                                                                                                            |
| D3DFMT \_ A8B8G8R8                    | DXGI \_ format \_ R8G8B8A8 \_ UNORM & DXGI \_ format \_ R8G8B8A8 \_ UNORM \_ SRGB                                                                                                                                                                                  |
| D3DFMT \_ X8B8G8R8                    | 無法使用                                                                                                                                                                                                                                        |
| D3DFMT \_ G16R16                      | DXGI \_ 格式 \_ R16G16 \_ UNORM                                                                                                                                                                                                                          |
| D3DFMT \_ A2R10G10B10                 | 無法使用                                                                                                                                                                                                                                        |
| D3DFMT \_ A16B16G16R16                | DXGI \_ 格式 \_ R16G16B16A16 \_ UNORM                                                                                                                                                                                                                    |
| D3DFMT \_ A8P8                        | 無法使用                                                                                                                                                                                                                                        |
| D3DFMT \_ P8                          | 無法使用                                                                                                                                                                                                                                        |
| D3DFMT 的 \_ L8                          | DXGI \_ 格式 \_ R8 \_ UNORM 注意：在著色器中使用 r swizzle，以將紅色複製到其他元件，以取得 D3D9 行為。                                                                                                                                    |
| D3DFMT \_ A8L8                        | DXGI \_ 格式 \_ R8G8 \_ UNORM 注意：使用著色器中的 swizzle 來複製紅色，並將綠色移至 Alpha 元件以取得 D3D9 行為。                                                                                                            |
| D3DFMT \_ A4L4                        | 無法使用                                                                                                                                                                                                                                        |
| D3DFMT \_ V8U8                        | DXGI \_ 格式 \_ R8G8 \_ SNORM                                                                                                                                                                                                                            |
| D3DFMT \_ L6V5U5                      | 無法使用                                                                                                                                                                                                                                        |
| D3DFMT \_ X8L8V8U8                    | 無法使用                                                                                                                                                                                                                                        |
| D3DFMT \_ Q8W8V8U8                    | DXGI \_ 格式 \_ R8G8B8A8 \_ SNORM                                                                                                                                                                                                                        |
| D3DFMT \_ V16U16                      | DXGI \_ 格式 \_ R16G16 \_ SNORM                                                                                                                                                                                                                          |
| D3DFMT \_ W11V11U10                   | 無法使用                                                                                                                                                                                                                                        |
| D3DFMT \_ A2W10V10U10                 | 無法使用                                                                                                                                                                                                                                        |
| D3DFMT \_ UYVY                        | 無法使用                                                                                                                                                                                                                                        |
| D3DFMT \_ R8G8 \_ B8G8                  | DXGI \_ FORMAT \_ G8R8 \_ G8B8 \_ UNORM (在 DX9 中，資料是由 255.0 f 進行調整，但這可在著色器程式碼) 中處理。                                                                                                                                   |
| D3DFMT \_ YUY2                        | 無法使用                                                                                                                                                                                                                                        |
| D3DFMT \_ G8R8 \_ G8B8                  | DXGI \_ FORMAT \_ R8G8 \_ B8G8 \_ UNORM (在 DX9 中，資料是由 255.0 f 進行調整，但這可在著色器程式碼) 中處理。                                                                                                                                   |
| D3DFMT \_ DXT1                        | DXGI \_ format \_ BC1 \_ UNORM & DXGI \_ format \_ BC1 \_ UNORM \_ SRGB                                                                                                                                                                                            |
| D3DFMT \_ DXT2                        | DXGI \_ format \_ BC1 \_ UNORM & DXGI \_ Format \_ BC1 \_ UNORM \_ SRGB Note： DXT1 和 DXT2 與 API/硬體觀點相同 .。。唯一的差異在於「預乘 Alpha」，可由應用程式追蹤，而不需要個別的格式。 |
| D3DFMT \_ DXT3                        | DXGI \_ format \_ BC2 \_ UNORM & DXGI \_ format \_ BC2 \_ UNORM \_ SRGB                                                                                                                                                                                            |
| D3DFMT \_ DXT4                        | DXGI \_ format \_ BC2 \_ UNORM & DXGI \_ Format \_ BC2 \_ UNORM \_ SRGB Note： DXT3 和 DXT4 與 API/硬體觀點相同 .。。唯一的差異在於「預乘 Alpha」，可由應用程式追蹤，而不需要個別的格式。 |
| D3DFMT \_ DXT5                        | DXGI \_ format \_ BC3 \_ UNORM & DXGI \_ format \_ BC3 \_ UNORM \_ SRGB                                                                                                                                                                                            |
| D3DFMT \_ D16 & D3DFMT \_ D16 \_ 鎖定 | DXGI \_ 格式 \_ D16 \_ UNORM                                                                                                                                                                                                                             |
| D3DFMT \_ D32                         | 無法使用                                                                                                                                                                                                                                        |
| D3DFMT \_ D15S1                       | 無法使用                                                                                                                                                                                                                                        |
| D3DFMT \_ D24S8                       | 無法使用                                                                                                                                                                                                                                        |
| D3DFMT \_ D24X8                       | 無法使用                                                                                                                                                                                                                                        |
| D3DFMT \_ D24X4S4                     | 無法使用                                                                                                                                                                                                                                        |
| D3DFMT \_ D16                         | DXGI \_ 格式 \_ D16 \_ UNORM                                                                                                                                                                                                                             |
| D3DFMT \_ D32F 的 \_ 鎖定              | DXGI \_ 格式 \_ D32 \_ FLOAT                                                                                                                                                                                                                             |
| D3DFMT \_ D24FS8                      | 無法使用                                                                                                                                                                                                                                        |
| D3DFMT \_ S1D15                       | 無法使用                                                                                                                                                                                                                                        |
| D3DFMT \_ S8D24                       | DXGI \_ 格式 \_ D24 \_ UNORM \_ S8 \_ UINT                                                                                                                                                                                                                   |
| D3DFMT \_ X8D24                       | 無法使用                                                                                                                                                                                                                                        |
| D3DFMT \_ X4S4D24                     | 無法使用                                                                                                                                                                                                                                        |
| D3DFMT \_ l16 也                         | DXGI \_ 格式 \_ R16 \_ UNORM 注意：在著色器中使用 r swizzle，以將紅色複製到其他元件，以取得 D3D9 行為。                                                                                                                                   |
| D3DFMT \_ INDEX16                     | DXGI \_ 格式 \_ R16 \_ UINT                                                                                                                                                                                                                              |
| D3DFMT \_ INDEX32                     | DXGI \_ 格式 \_ R32 \_ UINT                                                                                                                                                                                                                              |
| D3DFMT \_ Q16W16V16U16                | DXGI \_ 格式 \_ R16G16B16A16 \_ SNORM                                                                                                                                                                                                                    |
| D3DFMT \_ MULTI2 \_ ARGB8               | 無法使用                                                                                                                                                                                                                                        |
| D3DFMT \_ R16F                        | DXGI \_ 格式 \_ R16 \_ FLOAT                                                                                                                                                                                                                             |
| D3DFMT \_ G16R16F                     | DXGI \_ 格式 \_ R16G16 \_ FLOAT                                                                                                                                                                                                                          |
| D3DFMT \_ A16B16G16R16F               | DXGI \_ 格式 \_ R16G16B16A16 \_ FLOAT                                                                                                                                                                                                                    |
| D3DFMT \_ R32F                        | DXGI \_ 格式 \_ R32 \_ FLOAT                                                                                                                                                                                                                             |
| D3DFMT \_ G32R32F                     | DXGI \_ 格式 \_ R32G32 \_ FLOAT                                                                                                                                                                                                                          |
| D3DFMT \_ A32B32G32R32F               | DXGI \_ 格式 \_ R32G32B32A32 \_ FLOAT                                                                                                                                                                                                                    |
| D3DFMT \_ CxV8U8                      | 無法使用                                                                                                                                                                                                                                        |
| D3DDECLTYPE \_ FLOAT1                 | DXGI \_ 格式 \_ R32 \_ FLOAT                                                                                                                                                                                                                             |
| D3DDECLTYPE \_ FLOAT2                 | DXGI \_ 格式 \_ R32G32 \_ FLOAT                                                                                                                                                                                                                          |
| D3DDECLTYPE \_ FLOAT3                 | DXGI \_ 格式 \_ R32G32B32 \_ FLOAT                                                                                                                                                                                                                       |
| D3DDECLTYPE \_ FLOAT4                 | DXGI \_ 格式 \_ R32G32B32A32 \_ FLOAT                                                                                                                                                                                                                    |
| D3DDECLTYPED3DCOLOR                 | 無法使用                                                                                                                                                                                                                                        |
| D3DDECLTYPE \_ UBYTE4                 | DXGI \_ 格式 \_ R8G8B8A8 \_ Uint Note：著色器會取得 UINT 值，但如果需要 Direct3D 9 樣式的整數浮點數， (0.0 f，1.0 f .。。) ，UINT 只可以轉換成著色器中的 float32。                                                               |
| D3DDECLTYPE \_ SHORT2                 | DXGI \_ 格式 \_ R16G16 \_ 聖馬丁：著色器會取得聖值，但如果需要 Direct3D 9 樣式的整數浮點數，則可以直接將聖值轉換成著色器中的 float32。                                                                                       |
| D3DDECLTYPE \_ SHORT4                 | DXGI \_ 格式 \_ R16G16B16A16 \_ 聖馬丁：著色器會取得聖值，但如果需要 Direct3D 9 樣式的整數浮點數，則可以直接將聖值轉換成著色器中的 float32。                                                                                 |
| D3DDECLTYPE \_ UBYTE4N                | DXGI \_ 格式 \_ R8G8B8A8 \_ UNORM                                                                                                                                                                                                                        |
| D3DDECLTYPE \_ SHORT2N                | DXGI \_ 格式 \_ R16G16 \_ SNORM                                                                                                                                                                                                                          |
| D3DDECLTYPE \_ SHORT4N                | DXGI \_ 格式 \_ R16G16B16A16 \_ SNORM                                                                                                                                                                                                                    |
| D3DDECLTYPE \_ USHORT2N               | DXGI \_ 格式 \_ R16G16 \_ UNORM                                                                                                                                                                                                                          |
| D3DDECLTYPE \_ USHORT4N               | DXGI \_ 格式 \_ R16G16B16A16 \_ UNORM                                                                                                                                                                                                                    |
| D3DDECLTYPE \_ UDEC3                  | 無法使用                                                                                                                                                                                                                                        |
| D3DDECLTYPE \_ DEC3N                  | 無法使用                                                                                                                                                                                                                                        |
| D3DDECLTYPE \_ FLOAT16 \_ 2             | DXGI \_ 格式 \_ R16G16 \_ FLOAT                                                                                                                                                                                                                          |
| D3DDECLTYPE \_ FLOAT16 \_ 4             | DXGI \_ 格式 \_ R16G16B16A16 \_ FLOAT                                                                                                                                                                                                                    |
| FourCC 'ATI1'                       | DXGI \_ 格式 \_ BC4 \_ UNORM                                                                                                                                                                                                                             |
| FourCC 'ATI2'                       | DXGI \_ 格式 \_ BC5 \_ UNORM                                                                                                                                                                                                                             |



 

¹ DXGI 1.1 （包含在 Direct3D 11 執行時間中）包含 BGRA 格式。 不過，對於具有針對 Windows 顯示驅動程式模型的驅動程式所執行之驅動程式的 Direct3D 10 和10.1 裝置，這些格式的支援是選擇性的， (wddm) 適用于 Windows Vista (WDDM 1.0) 。 請考慮改為使用 DXGI \_ 格式 \_ R8G8B8A8 \_ UNORM。 或者，您可以使用 [**D3D10 \_ 建立 \_ 裝置 \_ BGRA \_ 支援**](/windows/desktop/api/D3D10/ne-d3d10-d3d10_create_device_flag) 來建立裝置，以確保只支援安裝 Direct3D 11.0 執行時間和 WDDM 1.1 驅動程式或更高版本的電腦。

² DXGI 1.0 已定義5:6:5 和5:5:5:1 格式，但 Direct3D 2.x 或 Direct3D 11.0 執行時間不支援這些格式。 您可以選擇性地支援 DirectX 11.1 執行時間中的 DXGI 1.2，這是功能層級11.1 視訊卡和 WDDM 1.2 (顯示驅動程式模型（從 Windows 8) 驅動程式開始，且已在10level9 功能層級上支援）。

³ DXGI 1.2 引進4:4:4:4 格式。 這種格式可在 DirectX 11.1 執行時間中選擇支援，這是功能層級11.1 視訊卡和 WDDM 1.2 驅動程式所需，且已在10level9 功能層級上支援。

針對未壓縮的格式，DXGI 已限制任意像素格式模式的支援;所有未壓縮的格式都必須是 RGBA 類型。 這可能需要 swizzling 現有的資產像素格式，我們建議您在可能的情況下，將其計算為離線的前置進程傳遞。

## <a name="porting-shaders"></a>移植著色器

### <a name="direct3d-10-shaders-are-authored-in-hlsl"></a>Direct3D 10 著色器是在 HLSL 中撰寫的

Direct3D 10 會將組合語言的使用限制為僅供偵錯工具使用，因此，在 Direct3D 9 中使用的任何手動寫入元件著色器都必須轉換成 HLSL。

### <a name="shader-signatures-and-linkage"></a>著色器簽章和連結

我們稍早在本檔中討論了輸入元件連結至頂點著色器輸入簽章的需求 (查看上述) 。 請注意，Direct3D 10 執行時間也已加強階段的需求，以暫存著色器之間的連結。 這種變更將會影響著色器來源，其中階段之間的系結可能未在 Direct3D 9 下完整描述。 例如：


```
VS_OUTPUT                       PS_INPUT
float4   pos : SV_POSITION;     float4 pos : SV_POSITION;
float4   uv1 : TEXCOORD1;       float4 uv1 : TEXCOORD1;
float4x3 tangentSp : TEXCOORD2; float4 tangent : TEXCOORD2; *
float4   Color : TEXCOORD6;     float4 color : TEXCOORD6;
```



\* 中斷的 VS PS 連結-雖然圖元著色器可能不會對完整的矩陣有興趣，但連結必須指定完整的 float4x3。

請注意，階段之間的連結語義必須完全相符，但目標階段輸入可能是輸出值的前置詞。 在上述範例中，圖元著色器的位置和 texcoord1 可能是唯一的輸入，但由於順序條件約束，它無法將位置和 texcoord2 做為唯一的輸入。

### <a name="hlsl-shader-stage-linkages"></a>HLSL 著色器階段連結

著色器之間的連結可能會發生在管線中的下列任何點：

-   輸入組合語言至頂點著色器
-   指向圖元著色器的頂點著色器
-   幾何著色器的頂點著色器
-   要串流輸出的頂點著色器
-   幾何著色器至圖元著色器
-   要串流輸出的幾何著色器

### <a name="constant-buffers"></a>常數緩衝區

為了方便從 Direct3D 9 移植內容，在效果系統之外進行常數管理的初始方法可能需要建立包含所有必要常數的單一常數緩衝區。 以預期的更新頻率將常數排序到緩衝區是很重要的。 此組織會將多餘的常數集合減少為最小值。

### <a name="user-clip-planes-in-hlsl-on-feature-level-9-and-higher"></a>功能層級9和更新版本上 HLSL 的使用者剪輯平面

從 Windows 8 開始，您可以 [在 HLSL 函](../direct3dhlsl/dx-graphics-hlsl-function-syntax.md)式宣告（而不是 [SV \_ ClipDistance](../direct3dhlsl/dx-graphics-hlsl-semantics.md) ）中使用 **clipplanes** 函式屬性，讓您的著色器能在 [功能層級](../direct3d11/overviews-direct3d-11-devices-downlevel-intro.md)9 \_ x 以及功能層級10和更高版本上運作。 如需詳細資訊，請參閱「 [功能等級9硬體上的使用者剪輯平面](../direct3dhlsl/user-clip-planes-on-10level9.md)」。

## <a name="additional-direct3d-10-differences-to-watch-for"></a>要監看的其他 Direct3D 10 差異

### <a name="integers-as-input"></a>整數作為輸入

在 Direct3D 9 中，整數資料類型沒有真正的硬體支援，但是 Direct3D 10 硬體支援明確的整數類型。 如果您的端點緩衝區中有浮點數據，則您必須具有 float 輸入。 否則，整數型別將會是浮點值的位模式表示。 除非將值標示為沒有插補，否則不允許圖元著色器輸入的整數類型 (參閱 [插補](../direct3dhlsl/dx-graphics-hlsl-struct.md) 修飾詞) 。

### <a name="mouse-cursors"></a>滑鼠游標

在舊版的 Windows 上，標準的 GDI 滑鼠游標常式在所有全螢幕專屬裝置上都無法正常運作。 已新增 [**SetCursorProperties**](/windows/win32/api/d3d9helper/nf-d3d9helper-idirect3ddevice9-setcursorproperties)、 [**ShowCursor**](/windows/win32/api/d3d9helper/nf-d3d9helper-idirect3ddevice9-showcursor)和 [**SetCursorPosition**](/windows/win32/api/d3d9helper/nf-d3d9helper-idirect3ddevice9-setcursorposition) api 來處理這些情況。 由於 Windows Vista 的 GDI 版本完全瞭解[DXGI](../direct3ddxgi/d3d10-graphics-programming-guide-dxgi.md)介面，因此不需要這個特殊的滑鼠游標 API，因此沒有 Direct3D 10 對等專案。 Direct3D 10 應用程式應該改為使用滑鼠游標的標準 [GDI 滑鼠游標常式](../menurc/cursors.md) 。

### <a name="mapping-texels-to-pixels-in-direct3d-10"></a>將材質對應至 Direct3D 10 中的圖元

在 Direct3D 9 中，材質中心和圖元中心是 (的一半單位，請參閱 [ (Direct3D 9) ) ，直接將材質對應至圖元 ](../direct3d9/directly-mapping-texels-to-pixels.md) 。 在 Direct3D 10 中，材質中心已經是半個單位，因此完全不需要移動頂點座標。

使用 Direct3D 10 可以更簡單地呈現全螢幕四邊形。 全螢幕四邊形應該在 clipspace (-1，1) 中定義，而且只會通過頂點著色器而不會有任何變更。 如此一來，就不需要在每次螢幕解析度變更時重載頂點緩衝區，而圖元著色器中不需要額外的工作來操作材質座標。

### <a name="reference-counting-behavior-changes"></a>參考計數行為變更

不同于先前的 Direct3D 版本，不同的 Set 函數不會保存裝置物件的參考。 這表示應用程式必須確保它會保留物件的參考，只要該物件需要系結至管線。 當物件的參考計數降至零時，該物件會從管線中解除系結，因為它已損毀。 這個參考的樣式也稱為弱式參考，因此裝置物件上的每個系結位置都會保存介面/物件的弱式參考。 除非明確提及，否則應該針對所有 Set 方法採用此行為。 當物件的終結造成系結點設為 **Null** 時，Debug 層會發出警告。 請注意，對裝置 Get 方法（例如 [**OMGetRenderTargets**](/windows/desktop/api/D3D10/nf-d3d10-id3d10device-omgetrendertargets) ）的呼叫會增加所傳回物件的參考計數。

### <a name="test-cooperative-level"></a>測試合作層級

Direct3D 9 API [**TestCooperativeLevel**](/windows/win32/api/d3d9helper/nf-d3d9helper-idirect3ddevice9-testcooperativelevel)的功能類似于在呼叫 [**存在**](/windows/win32/api/dxgi/nf-dxgi-idxgiswapchain-present)時設定 [DXGI \_ 目前的 \_ 測試](../direct3ddxgi/dxgi-present.md)。

### <a name="stretchrect"></a>StretchRect

Direct3D 10 和10.1 中不提供類似 Direct3D 9 [**IDirect3DDevice9：： StretchRect**](/windows/win32/api/d3d9helper/nf-d3d9helper-idirect3ddevice9-stretchrect) 方法的函式。 若要複製資源表面，請使用 [**ID3D10Device：： CopySubresourceRegion**](/windows/desktop/api/D3D10/nf-d3d10-id3d10device-copysubresourceregion)。 針對調整大小作業，使用材質篩選轉譯成材質。 若要將 MSAA 介面轉換成非 MSAA 表面，請使用 [**ID3D10Device：： ResolveSubresource**](/windows/desktop/api/d3d10/nf-d3d10-id3d10device-resolvesubresource)。

## <a name="additional-direct3d-101-differences"></a>其他 Direct3D 10.1 差異

WindowsVista Service Pack 1 (SP1) 包含 Direct3D 10 和 Direct3D 10.1 的次要更新，這會公開下列額外的硬體功能：

-   MSAA 每個範例著色器
-   MSAA 深度讀回
-   每個轉譯目標的獨立 blend 模式
-   Cube 地圖陣列
-   轉譯成區塊壓縮的 (BC) 格式

Direct3D 10.1 更新新增了下列新介面的支援，這些介面衍生自現有的介面：

-   [**ID3D10Device1**](/windows/desktop/api/D3D10_1/nn-d3d10_1-id3d10device1)
-   [**ID3D10BlendState1**](/windows/desktop/api/D3D10_1/nn-d3d10_1-id3d10blendstate1)
-   [**ID3D10ShaderResourceView1**](/windows/desktop/api/d3d10_1/nn-d3d10_1-id3d10shaderresourceview1)

Direct3D 10.1 更新也包含下列其他結構：

-   [**D3D10 \_ 轉譯 \_ 目標 \_ BLEND \_ DESC1**](/windows/desktop/api/d3d10_1/ns-d3d10_1-d3d10_render_target_blend_desc1)
-   [**D3D10 \_ BLEND \_ DESC1**](/windows/desktop/api/D3D10_1/ns-d3d10_1-d3d10_blend_desc1)
-   [**D3D10 \_ 著色器 \_ 資源 \_ 視圖 \_ DESC1**](/windows/desktop/api/d3d10_1/ns-d3d10_1-d3d10_shader_resource_view_desc1)

Direct3D 10.1 API 包含名為功能層級的新概念。 此概念表示您可以使用 Direct3D 10.1 API 來推動 Direct3D 10.0 ([**D3D10 \_ 功能 \_ 等級 \_ 10 \_ 0**](/windows/desktop/api/D3D10_1/ne-d3d10_1-d3d10_feature_level1)) 或 Direct3D 10.1 ([**D3D10 \_ 功能 \_ 等級 \_ 10 \_ 1**](/windows/desktop/api/D3D10_1/ne-d3d10_1-d3d10_feature_level1)) 硬體。 由於 Direct3D 10.1 API 衍生自 Direct3D 10 介面，因此應用程式可以建立 Direct3D 10.1 裝置，然後將其作為 Direct3D 10.0 裝置，但需要新的10.1 特定功能， (前提是 **D3D10 功能層級為 \_ \_ \_ 10 \_ 1** 功能層級存在，而且) 支援這些功能。

> [!Note]  
> Direct3D 10.1 裝置可以使用現有的 10.0 HLSL 著色器設定檔 (vs \_ 4 \_ 0、ps \_ 4 \_ 0、gs \_ 4 \_ 0) 以及新的10.1 設定檔 (vs \_ 4 \_ 1、ps \_ 4 \_ 1、gs \_ 4 \_ 1) 以及其他 HLSL 指示和功能。

 

Windows 7 包含 direct3d 10.1 API 的次要更新，包含在 direct3d 11 執行時間中。 此更新新增了下列功能層級的支援：

-   [**D3D10 \_ 功能 \_ 層級 \_ 9 \_ 1**](/windows/desktop/api/D3D10_1/ne-d3d10_1-d3d10_feature_level1)
-   [**D3D10 \_ 功能 \_ 層級 \_ 9 \_ 2**](/windows/desktop/api/D3D10_1/ne-d3d10_1-d3d10_feature_level1)
-   [**D3D10 \_ 功能 \_ 層級 \_ 9 \_ 3**](/windows/desktop/api/D3D10_1/ne-d3d10_1-d3d10_feature_level1)

Windows 7 還新增了 Direct3D 10.1 的支援，適用于[Windows Advanced 點陣化平臺 (變形) ](../direct3darticles/directx-warp.md)。 您可以使用 [**D3D10 \_ 驅動程式 \_ 類型的 \_ 變形**](/windows/desktop/api/D3D10misc/ne-d3d10misc-d3d10_driver_type)來指定變形驅動程式。

如需 Direct3D 10.1 的詳細資訊，請參閱 [direct3d 10.1 功能](d3d10-graphics-programming-guide-10-1.md) 和 [**D3D10 \_ 功能 \_**](/windows/desktop/api/D3D10_1/ne-d3d10_1-d3d10_feature_level1) 級1列舉。

## <a name="related-topics"></a>相關主題

<dl> <dt>

[Direct3D 10 程式設計手冊](d3d10-graphics-programming-guide.md)
</dt> </dl>

 

 
