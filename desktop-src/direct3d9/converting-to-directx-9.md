---
description: Microsoft Direct3D 9 中的下列功能已變更。 如果您使用這些功能，請參閱下面所列的變更，協助您將應用程式移植到 Direct3D 9。
ms.assetid: 6f5b2cc1-5415-4af8-a964-051a5af42680
title: 轉換成 Direct3D 9
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: becdb878ad462bfc0157fb15b3c9c1ef2ba158dd
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/07/2021
ms.locfileid: "106971323"
---
# <a name="converting-to-direct3d-9"></a>轉換成 Direct3D 9

Microsoft Direct3D 9 中的下列功能已變更。 如果您使用這些功能，請參閱下面所列的變更，協助您將應用程式移植到 Direct3D 9。

-   [BaseVertexIndex 變更](#basevertexindex-changes)
-   [CreateImageSurface 變更](#createimagesurface-changes)
-   [D3DENUM \_ 沒有 \_ WHQL \_ 層級變更](/windows)
-   [建立資源變更](#create-resource-changes)
-   [EnumAdapterModes 變更](#enumadaptermodes-changes)
-   [取得/SetStreamSource \_ 變更](#getsetstreamsource-changes)
-   [多級取樣品質變更](#multisampling-quality-changes)
-   [ResourceManagerDiscardBytes 變更](#resourcemanagerdiscardbytes-changes)
-   [SetSoftwareVertexProcessing 變更](#setsoftwarevertexprocessing-changes)
-   [紋理取樣器變更](#texture-sampler-changes)
-   [頂點宣告變更](#vertex-declaration-changes)
-   [間隔 \_ 和 \_ SwapEffects \_ 變更](#intervals-and-swapeffects-changes)

## <a name="basevertexindex-changes"></a>BaseVertexIndex 變更

在 DirectX 8.x 中，IDirect3DDevice8：： SetIndices 需要索引緩衝區的指標，以及頂點緩衝區中開始位置的 BaseVertexIndex。 將不同物件批次處理到頂點緩衝區的應用程式必須先切換索引緩衝區 (或呼叫 IDirect3DDevice8：： SetIndices) ，然後再呼叫 IDirect3DDevice8：:D rawIndexedPrimitive。

在 Direct3D 9 中，頂點緩衝區 *BaseVertexIndex* 中的開始位置已移至 IDirect3DDevice9：:D rawindexedprimitive，而且其資料類型從 DWORD 變更為整數。


```
HRESULT IDirect3DDevice9::DrawIndexedPrimitive( 
    D3DPRIMITIVETYPE PrimType, 
    INT BaseVertexIndex, 
    UINT minIndex, 
    UINT NumVertices, 
    UINT startIndex, 
    UINT primCount); 

HRESULT SetIndices(IDirect3DIndexBuffer9* pIndexData); 
```



## <a name="createimagesurface-changes"></a>CreateImageSurface 變更

IDirect3DDevice8：： CreateImageSurface 已重新命名為 [**CreateOffscreenPlainSurface**](/windows/win32/api/d3d9helper/nf-d3d9helper-idirect3ddevice9-createoffscreenplainsurface)。 已新增採用 D3DPOOL 類型的其他參數。 D3DPOOL 的 \_ 臨時將會傳回與 IDirect3DDevice8：： CreateImageSurface 所建立之介面具有相同特性的介面。 D3DPOOL \_ 預設值是搭配 [**StretchRect**](/windows/desktop/api) 和 [**ColorFill**](/windows/win32/api/d3d9helper/nf-d3d9helper-idirect3ddevice9-colorfill)使用的適當集區。

## <a name="d3denum_no_whql_level-changes"></a>D3DENUM \_ 沒有 \_ WHQL \_ 層級變更

應用程式現在必須明確要求 Microsoft Windows 硬體品質實驗室 (的 WHQL) ，因為回應的時間相當長 (幾秒鐘) 。 D3DENUM \_ 未 \_ \_ 移除 whql 層級，且已 \_ 新增 D3DENUM whql \_ 等級。

## <a name="create-resource-changes"></a>建立資源變更

控制碼已新增至數個方法，應設定為 **Null**。 受影響的方法包括：

-   [**CreateTexture**](/windows/win32/api/d3d9helper/nf-d3d9helper-idirect3ddevice9-createtexture)
-   [**CreateVolumeTexture**](/windows/win32/api/d3d9helper/nf-d3d9helper-idirect3ddevice9-createvolumetexture)
-   [**CreateCubeTexture**](/windows/win32/api/d3d9helper/nf-d3d9helper-idirect3ddevice9-createcubetexture)
-   [**CreateVertexBuffer**](/windows/win32/api/d3d9helper/nf-d3d9helper-idirect3ddevice9-createvertexbuffer)
-   [**CreateIndexBuffer**](/windows/win32/api/d3d9helper/nf-d3d9helper-idirect3ddevice9-createindexbuffer)
-   [**CreateRenderTarget**](/windows/win32/api/d3d9helper/nf-d3d9helper-idirect3ddevice9-createrendertarget)
-   [**CreateDepthStencilSurface**](/windows/win32/api/d3d9helper/nf-d3d9helper-idirect3ddevice9-createdepthstencilsurface)
-   [**CreateOffscreenPlainSurface**](/windows/win32/api/d3d9helper/nf-d3d9helper-idirect3ddevice9-createoffscreenplainsurface)

## <a name="enumadaptermodes-changes"></a>EnumAdapterModes 變更

[**EnumAdapterModes**](/windows/win32/api/d3d9/nf-d3d9-idirect3d9-enumadaptermodes)現在會採用 D3DFORMAT。


```
HRESULT IDirect3D9::EnumAdapterModes( 
       UINT Adapter, 
       D3DFORMAT Format, 
       UINT Mode, 
       D3DDISPLAYMODE *pMode); 
```



此格式支援一組展開的顯示模式。 為了保護應用程式不會列舉應用程式隨附時未衍生的格式，應用程式必須告訴 Direct3D 應該列舉的顯示模式格式。 顯示模式的產生陣列只會隨著寬度、高度和重新整理率不同。

應用程式會指定像素格式，且列舉會限制為完全符合格式的顯示模式。 以下是允許的格式清單：

-   D3DFMT \_ A1R5G5B5
-   D3DFMT \_ A2B10G10R10
-   D3DFMT \_ A8R8G8B8
-   D3DFMT \_ R5G6B5
-   D3DFMT \_ X1R5G5B5
-   D3DFMT \_ X8R8G8B8

列舉等同于相同格式的 Alpha 和 nonAlpha 版本。 傳回的格式一律會填入應用程式所提供的相同格式。

這個方法會將565和555視為對等，並傳回格式正確的版本。 只有當應用程式鎖定背景緩衝區，而且應用程式必須設定明確旗標才能完成此動作時，才會發生差異。

## <a name="getsetstreamsource-changes"></a>取得/SetStreamSource 變更

已將一個參數加入至 [**GetStreamSource**](/windows/desktop/api) 和 [**SetStreamSource**](/windows/win32/api/d3d9helper/nf-d3d9helper-idirect3ddevice9-setstreamsource) 方法。 位移是資料流程開頭與頂點資料開頭之間的位元組數目。 其測量單位是位元組。 這可讓管線支援資料流程位移。 若要找出裝置是否支援資料流程位移，請參閱 D3DDEVCAPS2 \_ STREAMOFFSET。


```
HRESULT GetStreamSource(
    UINT StreamNumber,
    IDirect3DVertexBuffer9 **ppStreamData,
    UINT *pOffsetInBytes,
    UINT *pStride);
```



## <a name="multisampling-quality-changes"></a>多級取樣品質變更

先前只有 D3DMULTISAMPLE \_ 類型列舉。 Direct3D 9 會保留此列舉，並為列舉的每個元素加入品質層級的概念。 品質層級表示在視覺品質與效能之間的取捨，方法是以 D3DRS MULTISAMPLEMASK) 的意義，指出 (的遮罩樣本數目 \_ 。

應用程式應該選擇所需的遮罩樣本數目，然後參閱 pQualityLevels。 如果是非零值，則這個值表示應用程式可以透過 MultiSampleQuality 傳遞至各種建立函式的品質層級數目。 因為驅動程式會將其所有的多型配置以 D3DMULTISAMPLE NONMASKABLE 的品質層級公開 \_ ，所以如果您的應用程式不需要遮罩範例，您可以透過這種類型來列舉所有可用的取樣。

D3DPRASTERCAPS \_ STRETCHBLTMULTISAMPLE caps bit 已淘汰。 這個位用來表示取樣方法不支援寫入遮罩，而且無法在 [**BeginScene**](/windows/desktop/api) 和 [**EndScene**](/windows/win32/api/d3d9helper/nf-d3d9helper-idirect3ddevice9-endscene)之間切換。 這類 nonmaskable 方法現在會透過 D3DMULTISAMPLE \_ nonmaskable 公開。


```
HRESULT CheckDeviceMultiSampleType( 
       UINT Adapter, 
       D3DDEVTYPE DeviceType, 
       D3DFORMAT SurfaceFormat, 
       BOOL Windowed, 
       D3DMULTISAMPLE_TYPE MultiSampleType, 
       DWORD * pQualityLevels); 
```



每個可遮罩樣本數目的最大值各有不同。 例如，D3DMULTISAMPLE \_ 4 \_ 範例可能有三個品質層級，而 D3DMULTISAMPLE \_ 2 個 \_ 範例可能只有一個。 每個遮罩樣本數目最多有八個品質層級 (不允許驅動程式表達更) 。 品質範圍從零到 (\* pQualityLevels-1) 。

## <a name="resourcemanagerdiscardbytes-changes"></a>ResourceManagerDiscardBytes 變更

ResourceManagerDiscardBytes 已由 IDirect3DDevice9：： EvictManagedResources 取代。 它可以收回所有資源，包括 Direct3D 和驅動程式資源。

資源管理員現在會在資源 (管理或非受管理) 因為沒有足夠的視訊記憶體而無法建立時，進行諮詢。 系統會自動要求管理員釋放足夠的資源，才能成功建立。 在 DirectX 8.0 中，這並不是自動化的流程。

## <a name="setsoftwarevertexprocessing-changes"></a>SetSoftwareVertexProcessing 變更

應用程式可以建立混合模式裝置，以使用軟體和硬體頂點處理。

若要在 DirectX 8.x 的兩個頂點處理模式之間切換，請呼叫 IDirect3DDevice8：： Graphicsdevice。 這已由 [**SetSoftwareVertexProcessing**](/windows/win32/api/d3d9helper/nf-d3d9helper-idirect3ddevice9-setsoftwarevertexprocessing) 取代，以簡化狀態欄塊所造成的問題。 狀態欄塊不會記錄這個新的方法。

## <a name="texture-sampler-changes"></a>紋理取樣器變更

Direct3D 9 在一次使用圖元著色器 2 0 模型最多支援16個材質介面 \_ ; 不過，材質座標的數目維持限制為8。 材質階段狀態是與表面、座標集合、頂點處理和圖元處理相關聯。 為了在編譯時期管理這些差異， [**SetTextureStageState**](/windows/win32/api/d3d9helper/nf-d3d9helper-idirect3ddevice9-settexturestagestate) 已分為兩種方法：

-   IDirect3DDevice9：： SetTextureStageState 仍會用於材質座標狀態，例如換行模式和材質座標產生。
-   [**SetSamplerState**](/windows/win32/api/d3d9helper/nf-d3d9helper-idirect3ddevice9-setsamplerstate) 已加入，現在將用於篩選、平平接、固定、MIPLOD 等等。 這最多可以使用十六個取樣器。

### <a name="settexturestagestate-changes"></a>SetTextureStageState 變更

IDirect3DDevice9：： SetTextureStageState 現在會設定下列狀態：

-   固定函式頂點處理狀態。 此狀態控制紋理座標的操作 D3DTSS \_ TEXTURETRANSFORMFLAGS 和 D3DTSS \_ TEXCOORDINDEX。 最多可以將 (設定為8個，因為一律支援8個材質座標) 。 D3DTSS \_ TEXCOORDINDEX 是固定的函式頂點處理狀態。 如果使用可程式化的頂點著色器，則會忽略此狀態。
-   固定的函式圖元著色器狀態 (舊版 TextureStageState) 。

    -   D3DTSS \_ ALPHAARG0
    -   D3DTSS \_ ALPHAARG1
    -   D3DTSS \_ ALPHAARG2
    -   D3DTSS \_ ALPHAOP
    -   D3DTSS \_ BUMPENVLOFFSET
    -   D3DTSS \_ BUMPENVLSCALE
    -   D3DTSS \_ BUMPENVMAT00
    -   D3DTSS \_ BUMPENVMAT01
    -   D3DTSS \_ BUMPENVMAT10
    -   D3DTSS \_ BUMPENVMAT11
    -   D3DTSS \_ COLORARG0
    -   D3DTSS \_ COLORARG1
    -   D3DTSS \_ COLORARG2
    -   D3DTSS \_ COLOROP
    -   D3DTSS \_ RESULTARG

    可以設定的固定函式圖元著色器狀態數目小於或等於 MaxTextureBlendStages 所代表的數位。

應用程式可用的紋理取樣器數目取決於圖元著色器版本，如下表所示。



| Name                    | Number                                                         |
|-------------------------|----------------------------------------------------------------|
| ps \_ 1 \_ 1 到 ps \_ 1 \_ 3    | 4紋理取樣器                                             |
| ps \_ 1 \_ 4                | 6紋理取樣器                                             |
| ps \_ 2 \_ 0                | 16個材質取樣器                                            |
| 固定函式管線 | MaxTextureBlendStages/MaxSimultaneousTextures 材質取樣器 |



 

在 Direct3D 9 中支援置換對應的裝置將會支援額外的取樣器 (D3DDMAPSAMPLER) ，以取樣鑲嵌單位中的置換地圖。

### <a name="setsamplerstate-changes"></a>SetSamplerState 變更

IDirect3DDevice9：： SetSamplerState 會將取樣器狀態 (，包括鑲嵌單位中用來取樣置換地圖) 。 這些已重新命名為 D3DSAMP \_ 前置詞，以在從 DirectX 8.x 移植時啟用編譯時期錯誤偵測。 這些狀態包括：

-   D3DSAMP \_ ADDRESSU
-   D3DSAMP \_ ADDRESSV
-   D3DSAMP \_ ADDRESSW
-   D3DSAMP \_ 邊框
-   D3DSAMP \_ MAGFILTER
-   D3DSAMP \_ MAXANISOTROPY
-   D3DSAMP \_ MAXMIPLEVEL
-   D3DSAMP \_ MINFILTER
-   D3DSAMP \_ MIPFILTER
-   D3DSAMP \_ MIPMAPLODBIAS

## <a name="vertex-declaration-changes"></a>頂點宣告變更

頂點宣告現在會與建立頂點著色器分離。 頂點宣告現在會使用元件物件模型 (COM) 介面。

針對 DirectX 8.x，頂點宣告會系結至頂點著色器。

-   針對固定函式管線，使用彈性頂點格式來呼叫 [**SetVertexShader**](/windows/win32/api/d3d9helper/nf-d3d9helper-idirect3ddevice9-setvertexshader) ， (FVF 頂點緩衝區的) 代碼。
-   針對頂點著色器，請使用先前建立頂點著色器的控制碼來呼叫 IDirect3DDevice9：： SetVertexShader。 著色器包含頂點宣告。

針對 Direct3D 9，頂點宣告會從頂點著色器分離出來，而且可以搭配 fixed 函數管線或著色器使用。

-   對於 fixed 函數管線，不需要呼叫 IDirect3DDevice9：： SetVertexShader。 但是，如果您想要切換至固定函式管線，且先前已使用頂點著色器，請呼叫 IDirect3DDevice9：： SetVertexShader (**Null**) 。 完成這項操作之後，您仍然需要呼叫 [**SetFVF**](/windows/win32/api/d3d9helper/nf-d3d9helper-idirect3ddevice9-setfvf) 來宣告 FVF 程式碼。
-   使用頂點著色器時，請使用頂點著色器物件來呼叫 IDirect3DDevice9：： SetVertexShader。 此外，呼叫 IDirect3DDevice9：： SetFVF 來設定頂點宣告。 這會使用 FVF 中隱含的資訊。 您可以呼叫 [**SetVertexDeclaration**](/windows/win32/api/d3d9helper/nf-d3d9helper-idirect3ddevice9-setvertexdeclaration)取代 IDirect3DDevice9：： SetFVF，因為它支援無法以 FVF 表示的頂點宣告。

## <a name="intervals-and-swapeffects-changes"></a>間隔和 SwapEffects 變更

有幾項變更可讓使用者更充分掌控監視器重新整理速率、呈現速率，以及前端緩衝區與背景緩衝區的繪製。 如下所示：

-   已移除一個交換效果、D3DSWAPEFFECT \_ 複製 \_ VSYNC，以及一個表示速率（D3DPRESENT \_ 率 \_ 無限制）。
-   已重新命名 D3DPRESENT \_ 參數。\_PresentationIntervals 的全螢幕 PresentationInterval。
-   新增 D3DPRESENT \_ 間隔 \_ 立即，這表示簡報不會與垂直同步處理同步。如同 DirectX 8.x，D3DPRESENT \_ INTERVAL \_ 預設值定義為零，相當於 D3DPRESENT \_ INTERVAL \_ 1。 D3DPRESENT \_ 間隔 \_ 預設是將 D3DPRESENT \_ 參數初始化為零的便利性。

如需模式和所支援間隔的詳細說明，請參閱 D3DPRESENT。

## <a name="related-topics"></a>相關主題

<dl> <dt>

[Direct3D 9 圖形](dx9-graphics.md)
</dt> </dl>

 

 
