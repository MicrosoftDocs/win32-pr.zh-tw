---
title: Direct3D 功能層級
description: 本主題討論 Direct3D 功能等級。
ms.assetid: 5ad0525c-249f-452d-950b-df8fa2addde2
keywords:
- DX 功能等級
- DirectX 功能層級
- 功能等級，DX
- 功能等級，DirectX
ms.topic: article
ms.date: 09/01/2020
ms.openlocfilehash: 9c4717d743e50e91376e57e5d13acbe2cfae41d8
ms.sourcegitcommit: 0b93de98c4afc79a6801a113bc91adbc89e835b9
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 07/03/2021
ms.locfileid: "113282467"
---
# <a name="direct3d-feature-levels"></a>Direct3D 功能層級

> [!NOTE]
> **針對發行前產品的部分相關資訊，在產品正式發行時可能會有大幅修改。Microsoft 對此處提供的資訊，不做任何明確或隱含的瑕疵擔保。**

為了處理新電腦和現有電腦的視訊卡多樣性，Microsoft Direct3D 11 引進了功能等級的概念。 本主題討論 Direct3D 功能等級。

每張視訊卡都能根據安裝的圖形處理單位 () Gpu) 功能，來執行特定層級的 Microsoft DirectX (DX。 在 Microsoft Direct3D 舊版中，可以找出視訊卡實作的 Direct3D 版本，然後隨之程式設計您的應用程式。

使用 Direct3D 11 時，引進了新的典範，稱為功能層級。 功能層級是一組妥善定義的 GPU 功能。 例如，9個 \_ 功能層級會執行在 Microsoft Direct3D 9 中執行的功能，此功能會公開著色器模型 [ps \_ 2 \_ x](../direct3dhlsl/dx9-graphics-reference-asm-ps-2-x.md) 和 [vs \_ 2 \_ x](../direct3dhlsl/dx9-graphics-reference-asm-vs-2-x.md)的功能，而 11 \_ 0 功能層級則會實作為 Direct3D 11 中所實行的功能。

現在當您建立裝置時，您可以嘗試針對您想要要求的功能層級建立裝置。 如果裝置建立運作，該功能層級則存在，否則，硬體不支援該功能層級。 您可以嘗試重新建立較低功能層級的裝置，或您可以選擇離開應用程式。 如需建立裝置的詳細資訊，請參閱 [**D3D11CreateDevice**](/windows/win32/api/D3D11/nf-d3d11-d3d11createdevice) 函式。

您可以使用功能等級開發 Direct3D 9、Microsoft Direct3D 10 或 Direct3D 11 的應用程式，然後在9、10或11個硬體 (上執行，但有一些例外狀況;例如，新的11功能將不會在現有的9張卡片) 上執行。 以下是一些功能層級的其他基本屬性：

- 允許建立裝置的 GPU 符合或超過該功能等級的功能。
- 功能層級一律包含先前或較低功能層級的功能。
- 功能層級不表示效能，而只是功能。 效能取決於硬體實行。
- 當您建立 Direct3D 11 裝置時，請選擇功能等級。

如需有關在特定功能層級上建立 nonhardware 類型裝置之限制的詳細資訊，請參閱 [建立變形和參照裝置的限制](overviews-direct3d-11-devices-limitations.md)。

為了協助您決定要設計的功能層級，請比較每個功能層級的功能。

[ [10Level9 參考](d3d11-graphics-reference-10level9.md) ] 區段會列出各種 [**ID3D11Device**](/windows/win32/api/D3D11/nn-d3d11-id3d11device) 和 [**>id3d11devicecoNtext**](/windows/win32/api/D3D11/nn-d3d11-id3d11devicecontext) 方法在各種10Level9 功能層級的行為方式之間的差異。

## <a name="formats-of-version-numbers"></a>版本號碼的格式

Direct3D 版本、著色器模型和功能層級有三種格式。

- Direct3D 版本使用句點;例如，Direct3D 12.0。
- 著色器模型使用句號;例如，著色器模型5.1。
- 功能層級使用底線;例如，功能層級 12 \_ 0。

## <a name="feature-support-for-feature-levels-12_2-through-9_3"></a>功能層級透過 9_3 12_2 的功能支援

下列功能適用于列出的功能等級。 頂端資料列上的標題是 Direct3D 功能等級。 左邊資料行中的標題是功能。 另請參閱 [資料表的註腳](#footnotes-for-the-tables)。

| 功能 \\ 功能等級 | 12 \_ 2<sup>8</sup> | 12 \_ 1<sup>0</sup> | 12 \_ 0<sup>0</sup> | 11 \_ 1<sup>1</sup> | 11 \_ 0 | 10 \_ 1 | 10 \_ 0 | 9 \_ 3<sup>7</sup> |
|-|-|-|-|-|-|-|-|-|
| 著色器模型 (D3D11)  | N/A | 5.0<sup>2</sup> | 5.0<sup>2</sup> | 5.0<sup>2</sup> | 5.0<sup>2</sup> | 4.x | 4.0 | 2.0 (4 \_ 0 \_ 層級 \_ 9 \_ 3) \[ vs \_ 2 \_ a/ps \_ 2 \_ x \] <sup>5</sup> |
| 著色器模型 (D3D12)  | 6.5 | 5.1<sup>2</sup> | 5.1<sup>2</sup> | 5.1<sup>2</sup> | 5.1<sup>2</sup> | N/A | N/A | N/A |
| [磚資源](tiled-resources.md) | Tier3 | 第2層<sup>6</sup> | 第2層<sup>6</sup> | 選用 | 選用 | 否 | 否 | 否 |
| [保守的點陣化](conservative-rasterization.md) | Tier3 | 第1層<sup>6</sup> | 選用 | 選用 | 否 | 否 | 否 | 否 |
| [轉譯器順序視圖](rasterizer-order-views.md) | 是 | 是 | 選用 | 選用 | 否 | 否 | 否 | 否 |
| [最小/最大篩選](/windows/win32/api/D3D11/ne-d3d11-d3d11_filter) | 是 | 是 | 是 | 選用 | 否 | 否 | 否 | 否 |
| 對應預設緩衝區 | N/A | 選用 | 選用 | 選用 | 選用 | 否 | 否 | 否 |
| [著色器指定的樣板參考值](shader-specified-stencil-reference-value.md) | 選用 | 選用 | 選用 | 選用 | 否 | 否 | 否 | 否 |
| 具類型的未排序存取視圖載入 | 18種格式，更選擇性 | 18種格式，更選擇性 | 18種格式，更選擇性 | 3種格式，更選擇性 | 3種格式，更選擇性 | 否 | 否 | 否 |
| [幾何著色器](/previous-versions/bb205146(v=vs.85)) | 是 | 是 | 是 | 是 | 是 | 是 | 是 | 否 |
| [串流輸出](./d3d10-graphics-programming-guide-output-stream-stage.md) | 是 | 是 | 是 | 是 | 是 | 是 | 是 | 否 |
| [DirectCompute/計算著色器](direct3d-11-advanced-stages-compute-shader.md) | 是 | 是 | 是 | 是 | 是 | 選用 | 選用 | N/A |
| <b>功能 \\ 功能等級</b> | <b>12 \_ 2<sup>8</sup></b> | <b>12 \_ 1<sup>0</sup></b> | <b>12 \_ 0<sup>0</sup></b> | <b>11 \_ 1<sup>1</sup></b> | <b>11 \_ 0</b> | <b>10 \_ 1</b> | <b>10 \_ 0</b> | <b>9 \_ 3<sup>7</sup></b> |
| [輪廓和網域著色器](direct3d-11-advanced-stages-tessellation.md) | 是 | 是 | 是 | 是 | 是 | 否 | 否 | 否 |
| [材質資源陣列](overviews-direct3d-11-resources-textures-intro.md) | 是 | 是 | 是 | 是 | 是 | 是 | 是 | 否 |
| [立方體貼圖資源陣列](overviews-direct3d-11-resources-textures-intro.md) | 是 | 是 | 是 | 是 | 是 | 是 | 否 | 否 |
| [BC4/BC5 壓縮](../direct3d10/d3d10-graphics-programming-guide-resources-block-compression.md) | 是 | 是 | 是 | 是 | 是 | 是 | 是 | 否 |
| [BC6H/BC7 壓縮](texture-block-compression-in-direct3d-11.md) | 是 | 是 | 是 | 是 | 是 | 否 | 否 | 否 |
| [Alpha 到涵蓋範圍](./d3d10-graphics-programming-guide-blend-state.md) | 是 | 是 | 是 | 是 | 是 | 是 | 是 | 否 |
| [擴充格式 (BGRA 等等) ](overviews-direct3d-11-devices-downlevel-exceptions.md) | 是 | 是 | 是 | 是 | 是 | 選用 | 選用 | 是 |
| [10 位元 XR 高彩格式](overviews-direct3d-11-devices-downlevel-exceptions.md) | 是 | 是 | 是 | 是 | 是 | 選用 | 選用 | N/A |
| [ (輸出合併的邏輯作業) ](/windows/win32/api/D3D11/ns-d3d11-d3d11_feature_data_d3d11_options) | 是 | 是 | 是 | 是 | 選用<sup>1</sup> | 選用<sup>1</sup> | 選用<sup>1</sup> | 否 |
| 目標獨立的點陣化 | 是 | 是 | 是 | 是 | 否 | 否 | 否 | 否 |
| [多重轉譯目標 (MRT.LOG) 與 ForcedSampleCount 1](/windows/win32/api/D3D11/ns-d3d11-d3d11_feature_data_d3d11_options) | 是 | 是 | 是 | 是 | 選用<sup>1</sup> | 選用<sup>1</sup> | 選用<sup>1</sup> | 否 |
| UAV 插槽 | 分層<sup>9</sup> | 64 | 64 | 64 | 8 | 1 | 1 | N/A |
| <b>功能 \\ 功能等級</b> | <b>12 \_ 2<sup>8</sup></b> | <b>12 \_ 1<sup>0</sup></b> | <b>12 \_ 0<sup>0</sup></b> | <b>11 \_ 1<sup>1</sup></b> | <b>11 \_ 0</b> | <b>10 \_ 1</b> | <b>10 \_ 0</b> | <b>9 \_ 3<sup>7</sup></b> |
| 每個階段的 UAVs | 是 | 是 | 是 | 是 | 否 | 否 | 否 | N/A |
| [僅限 UAV 轉譯的強制樣本計數上限](/windows/win32/api/D3D11/ns-d3d11-d3d11_feature_data_d3d11_options) | 16 | 16 | 16 | 16 | 8 | N/A | N/A | N/A |
| 常數緩衝區偏移和部分更新 | 是 | 是 | 是 | 是 | 選用<sup>1</sup> | 選用<sup>1</sup> | 選用<sup>1</sup> | 是<sup>1</sup> |
| 每圖元16個位 (bpp) 格式 | 是 | 是 | 是 | 是 | 選用<sup>1</sup> | 選用<sup>1</sup> | 選用<sup>1</sup> | 選用<sup>1</sup> |
| 最大材質維度 | 16384 | 16384 | 16384 | 16384 | 16384 | 8192 | 8192 | 4096 |
| 最大立方體貼圖維度 | 16384 | 16384 | 16384 | 16384 | 16384 | 8192 | 8192 | 4096 |
| 最大磁片區範圍 | 2048 | 2048 | 2048 | 2048 | 2048 | 2048 | 2048 | 256 |
| 最大材質重複 | 16384 | 16384 | 16384 | 16384 | 16384 | 8192 | 8192 | 8192 |
| 最大 Anisotropy | 16 | 16 | 16 | 16 | 16 | 16 | 16 | 16 |
| 最大基本計數 | 2 ^ 32-1 | 2 ^ 32-1 | 2 ^ 32-1 | 2 ^ 32-1 | 2 ^ 32-1 | 2 ^ 32-1 | 2 ^ 32-1 | 1048575 |
| 最大頂點索引 | 2 ^ 32-1 | 2 ^ 32-1 | 2 ^ 32-1 | 2 ^ 32-1 | 2 ^ 32-1 | 2 ^ 32-1 | 2 ^ 32-1 | 1048575 |
| 最大輸入位置 | 32 | 32 | 32 | 32 | 32 | 32 | 16 | 16 |
| 同時呈現目標 | 8 | 8 | 8 | 8 | 8 | 8 | 8 | 4 |
| 遮蔽查詢 | 是 | 是 | 是 | 是 | 是 | 是 | 是 | 是 |
| <b>功能 \\ 功能等級</b> | <b>12 \_ 2<sup>8</sup></b> | <b>12 \_ 1<sup>0</sup></b> | <b>12 \_ 0<sup>0</sup></b> | <b>11 \_ 1<sup>1</sup></b> | <b>11 \_ 0</b> | <b>10 \_ 1</b> | <b>10 \_ 0</b> | <b>9 \_ 3<sup>7</sup></b> |
| 分隔 Alpha Blend | 是 | 是 | 是 | 是 | 是 | 是 | 是 | 是 |
| 鏡像一次 | 是 | 是 | 是 | 是 | 是 | 是 | 是 | 是 |
| 重迭頂點元素 | 是 | 是 | 是 | 是 | 是 | 是 | 是 | 是 |
| 獨立寫入遮罩 | 是 | 是 | 是 | 是 | 是 | 是 | 是 | 是 |
| 實例 | 是 | 是 | 是 | 是 | 是 | 是 | 是 | 是<sup>7</sup> |
| Nonpowers-2 條件<sup>3</sup> | 否 | 否 | 否 | 否 | 否 | 否 | 否 | 是 |
| Nonpowers<sup>無條件為</sup>-2 | 是 | 是 | 是 | 是 | 是 | 是 | 是 | 否 |

## <a name="feature-support-for-feature-levels-9_2-and-9_1"></a>功能層級9_2 和9_1 的功能支援

下列功能適用于列出的功能等級。 頂端資料列上的標題是 Direct3D 功能等級。 左邊資料行中的標題是功能。 另請參閱 [資料表的註腳](#footnotes-for-the-tables)。

| 功能 \\ 功能等級 | 9 \_ 2 | 9 \_ 1 |
|-|-|-|
| 著色器模型 (D3D11)  | 2.0 (4 \_ 0 \_ 層級 \_ 9 \_ 1)  | 2.0 (4 \_ 0 \_ 層級 \_ 9 \_ 1)  |
| 著色器模型 (D3D12)  | N/A | N/A |
| [磚資源](tiled-resources.md) | 否 | 否 |
| [保守的點陣化](conservative-rasterization.md) | 否 | 否 |
| [轉譯器順序視圖](rasterizer-order-views.md) | 否 | 否 |
| [最小/最大篩選](/windows/win32/api/D3D11/ne-d3d11-d3d11_filter) | 否 | 否 |
| 對應預設緩衝區 | 否 | 否 |
| [著色器指定的樣板參考值](shader-specified-stencil-reference-value.md) | 否 | 否 |
| 具類型的未排序存取視圖載入 | 否 | 否 |
| [幾何著色器](/previous-versions/bb205146(v=vs.85)) | 否 | 否 |
| [串流輸出](./d3d10-graphics-programming-guide-output-stream-stage.md) | 否 | 否 |
| [DirectCompute/計算著色器](direct3d-11-advanced-stages-compute-shader.md) | N/A | N/A |
| [輪廓和網域著色器](direct3d-11-advanced-stages-tessellation.md) | 否 | 否 |
| [材質資源陣列](overviews-direct3d-11-resources-textures-intro.md) | 否 | 否 |
| [立方體貼圖資源陣列](overviews-direct3d-11-resources-textures-intro.md) | 否 | 否 |
| [BC4/BC5 壓縮](../direct3d10/d3d10-graphics-programming-guide-resources-block-compression.md) | 否 | 否 |
| <b>功能 \\ 功能等級</b> | <b>9 \_ 2</b> | <b>9 \_ 1</b> |
| [BC6H/BC7 壓縮](texture-block-compression-in-direct3d-11.md) | 否 | 否 |
| [Alpha 到涵蓋範圍](./d3d10-graphics-programming-guide-blend-state.md) | 否 | 否 |
| [擴充格式 (BGRA 等等) ](overviews-direct3d-11-devices-downlevel-exceptions.md) | 是 | 是 |
| [10 位元 XR 高彩格式](overviews-direct3d-11-devices-downlevel-exceptions.md) | N/A | N/A |
| [ (輸出合併的邏輯作業) ](/windows/win32/api/D3D11/ns-d3d11-d3d11_feature_data_d3d11_options) | 否 | 否 |
| 目標獨立的點陣化 | 否 | 否 |
| [多重轉譯目標 (MRT.LOG) 與 ForcedSampleCount 1](/windows/win32/api/D3D11/ns-d3d11-d3d11_feature_data_d3d11_options) | 否 | 否 |
| UAV 插槽 | N/A | N/A |
| 每個階段的 UAVs | N/A | N/A |
| [僅限 UAV 轉譯的強制樣本計數上限](/windows/win32/api/D3D11/ns-d3d11-d3d11_feature_data_d3d11_options) | N/A | N/A |
| 常數緩衝區偏移和部分更新 | 是<sup>1</sup> | 是<sup>1</sup> |
| 每圖元16個位 (bpp) 格式 | 選用<sup>1</sup> | 選用<sup>1</sup> |
| 最大材質維度 | 2048 | 2048 |
| 最大立方體貼圖維度 | 512 | 512 |
| 最大磁片區範圍 | 256 | 256 |
| 最大材質重複 | 2048 | 128 |
| <b>功能 \\ 功能等級</b> | <b>9 \_ 2</b> | <b>9 \_ 1</b> |
| 最大 Anisotropy | 16 | 2 |
| 最大基本計數 | 1048575 | 65535 |
| 最大頂點索引 | 1048575 | 65534 |
| 最大輸入位置 | 16 | 16 |
| 同時呈現目標 | 1 | 1 |
| 遮蔽查詢 | 是 | 否 |
| 分隔 Alpha Blend | 是 | 否 |
| 鏡像一次 | 是 | 否 |
| 重迭頂點元素 | 是 | 否 |
| 獨立寫入遮罩 | 否 | 否 |
| 實例 | 否 | 否 |
| Nonpowers-2 條件<sup>3</sup> | 是 | 是 |
| Nonpowers<sup>無條件為</sup>-2 | 否 | 否 |

## <a name="footnotes-for-the-tables"></a>資料表的註腳

<sup>0</sup> 需要 direct3d 11.3 或 direct3d 12 執行時間。

<sup>1</sup> 需要 Direct3D 11.1 執行時間。

<sup>2</sup> 著色器模型5.0 和更新版本可以選擇性地支援雙精確度著色器、擴充的雙精確度著色器、 **SAD4** 著色器指令和部分精確度著色器。 若要判斷適用于 DirectX 11 的著色器模型5.0 選項，請呼叫 [**ID3D11Device：： CheckFeatureSupport**](/windows/win32/api/D3D11/nf-d3d11-id3d11device-checkfeaturesupport)。 某些相容性取決於您正在執行的硬體。 著色器模型5.1 和更新版本僅透過 DirectX 12 API 支援，不論所使用的功能層級為何。 DirectX 11 最多隻支援著色器模型5.0。 DirectX 12 API 只會往下移至功能等級 11 \_ 0。

<sup>3</sup> 在功能層級 9 \_ 1、9 \_ 2 和 9 \_ 3，顯示裝置支援使用2d 材質，其維度在兩個條件下都不能有兩個的乘冪。 首先，只能建立每個材質的 MIP 對應層級，而第二種情況下，不允許紋理的換行取樣器模式 (也就是說， [**D3D11 \_ 取樣器 \_ DESC**](/windows/win32/api/D3D11/ns-d3d11-d3d11_sampler_desc)的 **AddressU**、 **AddressV** 和 **AddressW** 成員無法設定為 [**D3D11 \_ 材質 \_ 位址 \_ 換行**](/windows/win32/api/D3D11/ne-d3d11-d3d11_texture_address_mode)) 。

<sup>4</sup> 在功能層級為 10 \_ 0、10 \_ 1 和 11 \_ 0 時，顯示裝置無條件支援使用2d 材質，其尺寸不是兩個的乘冪。

<sup>5</sup> 個頂點著色器2a 含256指示、32臨時暫存器、深度4的靜態流程式控制制、深度24的動態流程式控制制和 D3DVS20CAPS \_ PREDICATION。 圖元著色器2x 與512指示、32臨時暫存器、深度4的靜態流程式控制制、深度24的動態流程式控制制、D3DPS20CAPS \_ ARBITRARYSWIZZLE、D3DPS20CAPS \_ GRADIENTINSTRUCTIONS、D3DPS20CAPS \_ PREDICATION、D3DPS20CAPS \_ NODEPENDENTREADLIMIT 和 D3DPS20CAPS \_ NOTEXINSTRUCTIONLIMIT。

<sup>6</sup> 個較高層級的選用。

<sup>7</sup> 針對功能層級9_3，唯一支援的轉譯方法為 **Draw**、 **DrawIndexed** 和 **DrawIndexInstanced**。 此外，對於功能層級9_3，僅支援透過 **Draw** 轉譯的點清單轉譯。

<sup>8</sup> 需要 Direct3D 12 執行時間。

在 Direct3D 12 API 中有<sup>9</sup>個 CBV/SRV/UAV 堆積中的描述項數目有所限制。 如需詳細資訊，請參閱 [硬體層](/windows/win32/direct3d12/hardware-support) 。 在所有階段（以 [資源系結層](https://microsoft.github.io/DirectX-Specs/d3d/ResourceBinding.html#levels-of-hardware-support)為基礎）中，所有描述項資料表中的 UAVs 數目會分別受到限制。

如需不同硬體功能層級的格式支援詳細資訊，請參閱：

- [Direct3D 功能等級12.1 硬體的 DXGI 格式支援](../direct3ddxgi/hardware-support-for-direct3d-12-1-formats.md)
- [Direct3D 功能等級12.0 硬體的 DXGI 格式支援](../direct3ddxgi/hardware-support-for-direct3d-12-0-formats.md)
- [Direct3D 功能等級11.1 硬體的 DXGI 格式支援](../direct3ddxgi/format-support-for-direct3d-11-1-feature-level-hardware.md)
- [Direct3D 功能等級11.0 硬體的 DXGI 格式支援](../direct3ddxgi/format-support-for-direct3d-11-0-feature-level-hardware.md)
- [Direct3D 10Level9 格式的硬體支援](/previous-versions/ff471324(v=vs.85))
- [Direct3D 10.1 格式的硬體支援](/previous-versions/cc627091(v=vs.85))
- [適用于 Direct3D 10 格式的硬體支援](/previous-versions/cc627090(v=vs.85))

## <a name="related-topics"></a>相關主題

* [舊版硬體上的 Direct3D 11](overviews-direct3d-11-devices-downlevel.md)
* [ (Direct3D 12) 的硬體功能層級 ](../direct3d12/hardware-feature-levels.md)
