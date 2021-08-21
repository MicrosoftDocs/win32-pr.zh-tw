---
title: '可變速率陰影 (VRS) '
description: 變動率陰影 &mdash; 或粗圖元陰影 &mdash; 是一種機制，可讓您以不同于轉譯影像的速率配置轉譯效能/電源。
ms.localizationpriority: high
ms.topic: article
ms.date: 04/08/2019
ms.openlocfilehash: b26d2d67a6e4a5f7b599a9fc65f324b301346fde3170262e80235a25f8cfb88b
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/11/2021
ms.locfileid: "119045283"
---
# <a name="variable-rate-shading-vrs"></a>可變速率陰影 (VRS) 

## <a name="the-motivation-for-vrs"></a>VRS 的動機
由於效能限制，圖形轉譯器無法永遠承受在輸出影像的每個部分提供相同等級的品質。 變動率陰影 &mdash; 或粗圖元陰影 &mdash; 是一種機制，可讓您以不同于轉譯影像的速率配置轉譯效能/電源。

在某些情況下，您可以減少可察覺輸出品質的小比例或減少陰影率;效能的改進，基本上是免費的。

## <a name="without-vrsmdashmulti-sample-anti-aliasing-with-supersampling"></a>不 &mdash; 使用 SUPERSAMPLING VRS 多重範例消除鋸齒
如果沒有變動率的陰影，控制陰影速率的唯一方法就是使用多取樣的消除鋸齒， (MSAA) 搭配以範例為基礎的執行 (也稱為 supersampling) 。

MSAA 是一種可減少幾何別名的機制，而且相較于不使用 MSAA，改善影像的轉譯品質。 MSAA 取樣計數（可以是1x、2x、4x、8x 或16x）會控制每個轉譯目標圖元配置的樣本數。 當配置目標時，必須事先知道 MSAA 取樣計數，之後就無法變更。

Supersampling 會讓圖元著色器針對每個樣本叫用一次，以較高的品質，但相較于每個圖元的執行，效能成本也較高。

您的應用程式可以選擇以圖元為基礎的每個執行，或使用 supersampling 來控制其陰影速率。 這兩個選項不會提供非常細微的控制。 此外，相較于影像的其餘部分，您可能會想要使用較低的特定物件類別的陰影比率。 這類物件可能包括抬頭顯示器元素後方的物件，或透明、模糊 (的欄位、動作等 ) ，或由於 VR 光學的視覺失真。 但這並不可行，因為陰影的品質和成本是在整個影像中修正。

## <a name="with-variable-rate-shading-vrs"></a>使用可變速率的陰影 (VRS) 
變動率的陰影 (VRS) 模型會藉由新增粗略陰影的概念，將 supersampling 與-MSAA 延伸至相反的「粗圖元」方向。 如此一來，陰影的執行頻率會比圖元更粗略。 換句話說，一組圖元可以作為單一單位的陰影，然後將結果廣播到群組中的所有範例。

粗略的陰影 API 可讓您的應用程式指定屬於陰影群組或 *粗圖元* 的圖元數目。 配置轉譯目標之後，您可以改變粗略的圖元大小。 因此，螢幕的不同部分或不同的繪製階段可能會有不同的陰影比例。

以下的表格描述支援哪些 MSAA 層級，以及哪個粗略圖元大小。 在任何平臺上都不支援部分;有些則是根據功能 (*AdditionalShadingRatesSupported*) （以「Cap」表示）有條件地啟用。

![表格顯示 M A 層級的粗略圖元大小。](images/CoarsePixelSizeSupport.PNG "粗圖元大小")

針對下一節所討論的功能層，沒有任何粗略圖元大小和樣本計陣列合，其中硬體需要追蹤每個圖元著色器調用的16個樣本。 這些組合在上表中是以半色調為網底的。

## <a name="feature-tiers"></a>功能層
VRS 的執行有兩個層級，還有兩個可供您查詢的功能。 資料表之後會更詳細地說明每一層。

![表格顯示第1層和第2層中可用的功能。](images/Tiers.PNG "VRS 層")

### <a name="tier-1"></a>第 1 層
- 您只能以每一繪製為基礎來指定網底比例;比起更細微。
- 陰影速率會一致地套用至繪製的位置，而不是與呈現目標中的位置無關。

### <a name="tier-2"></a>第 2 層
- 您可以針對每個繪製來指定陰影速率，如同第1層。 它也可以透過每個繪製的組合來指定，也可以透過下列方式來指定：
  - 每個誘發頂點的語義，以及
  - 螢幕空間影像。
- 這三個來源的陰影比例會使用一組結合器來合併。
- 螢幕空間影像磚大小為16x16 或更小。
- 您的應用程式所要求的陰影速率保證可以精確地傳遞 (，以取得時態性和其他重建篩選) 的精確度。
- 支援 SV_ShadingRate PS 輸入。
- 每個誘發的頂點 (也稱為每個基本) 網底比例，在使用一個使用中且未寫入時，就會是有效的 `SV_ViewportArrayIndex` 。
- 如果 *SupportsPerVertexShadingRateWithMultipleViewports* 功能設定為，則可以搭配多個誘發使用每個頂點的速率 `true` 。 此外，在這種情況下，當寫入時，可以使用該速率 `SV_ViewportArrayIndex` 。

### <a name="list-of-capabilities"></a>功能清單
- *AdditionalShadingRatesSupported*
  - 布林值類型。
  - 指出單一取樣轉譯是否支援2x4、4x2 和4x4 的粗圖元大小;以及是否支援 2x MSAA 的粗圖元大小2x4。
- *SupportsPerVertexShadingRateWithMultipleViewports*
  - 布林值類型。
  - 指出每個頂點是否可使用多個可用的區 (也稱為每個基本) 網底比例。

## <a name="specifying-shading-rate"></a>指定網底比例
為了在應用程式中有彈性，有提供各種機制來控制網底的速率。 根據硬體功能層，可以使用不同的機制。

### <a name="command-list"></a>命令清單
這是設定網底速率的最簡單機制。 適用于所有層級。

您的應用程式可以使用 [ **ID3D12GraphicsCommandList5：： RSSetShadingRate** 方法](/windows/desktop/api/d3d12/nf-d3d12-id3d12graphicscommandlist5-rssetshadingrate)來指定粗略的圖元大小。 該 API 會採用單一列舉引數。 此 API 會提供品質層級的整體控制，以轉譯 &mdash; 以每一繪製為基礎的陰影速率。

此狀態的值是透過 [**D3D12_SHADING_RATE**](/windows/desktop/api/d3d12/ne-d3d12-d3d12_shading_rate) 列舉來表示。

#### <a name="coarse-pixel-size-support"></a>粗糙圖元大小支援
所有層都支援 < 1x1、1x2、2x2 和2x2 的陰影比例。

有一項功能 *AdditionalShadingRatesSupported*，指出裝置是否支援2x4、4x2 和4x4。

### <a name="screen-space-image-image-based"></a>以映射為基礎的)  (螢幕空間影像
在第2層和更高版本上，您可以使用螢幕空間影像來指定圖元網底比例。

螢幕空間影像可讓您的應用程式建立「細節層級的 (」 LOD) mask」影像，指出品質不同的區域，例如，動作模糊、欄位深度模糊、透明物件或抬頭顯示器 UI 元素所涵蓋的區域。 影像的解析度是在巨大區塊中;它不在呈現目標的解析中。 換句話說，會以8x8 或16x16 圖元磚的資料細微性來指定陰影速率資料，如 VRS 磚大小所示。

#### <a name="tile-size"></a>圖格大小
您的應用程式可以查詢 API，以取得其裝置支援的 VRS 圖格大小。

磚是正方形，大小則是指材質中的磚寬度或高度。

如果硬體不支援第2層可變速率的陰影，則磚大小的功能查詢會傳回0。

如果 *硬體支援* 第2層可變速率的陰影，則磚大小會是下列其中一個值。

- 8
- 16
- 32

#### <a name="screen-space-image-size"></a>螢幕空間影像大小
針對大小為 {rtWidth，rtHeight} 的轉譯目標，使用名為 **VRSTileSize** 的指定圖格大小，將涵蓋的螢幕空間影像屬於這些維度。

```cpp
{ ceil((float)rtWidth / VRSTileSize), ceil((float)rtHeight / VRSTileSize) }
```

畫面空間影像的左上角 (0，0) 已鎖定為轉譯目標的左上角 (0，0) 。

若要查閱與轉譯目標中特定位置對應之圖格的 (x，y) 座標，請將 (x，y) 的視窗空間座標除以磚大小，忽略小數位。

如果螢幕空間影像大於指定轉譯目標所需的大小，則不會使用右邊和/或底部的額外部分。

如果螢幕空間影像對指定的轉譯目標而言太小，則任何嘗試從影像的實際範圍讀取超過其實際範圍的結果，都會產生預設的網底比例（1x1）。 這是因為螢幕空間影像的左上角 (0、0) 已鎖定到轉譯目標的左上角 (0、0) 和「在轉譯目標範圍之外讀取」，表示讀取 x 和 y 的值太大。

#### <a name="format-layout-resource-properties"></a>格式、配置、資源屬性
此介面的格式是單聲道8位介面 ([**DXGI_FORMAT_R8_UINT**](/windows/desktop/api/dxgiformat/ne-dxgiformat-dxgi_format)) 。

資源是維度 **TEXTURE2D**。

它不能是陣列或 mipped。 它必須明確具有一個 mip 層級。

它有範例計數1和範例品質0。

它有 **未知** 的材質版面配置。 因為不允許跨介面卡，所以隱含地不能是資料列的版面配置。

螢幕空間影像資料填入的預期方式是
1. 使用計算著色器來寫入資料;螢幕空間影像系結為 UAV，或
2. 將資料複製到螢幕空間影像。

建立螢幕空間影像時，允許使用這些旗標。

- 無
- ALLOW_UNORDERED_ACCESS
- DENY_SHADER_RESOURCE

不允許這些旗標。

- ALLOW_RENDER_TARGET
- ALLOW_DEPTH_STENCIL
- ALLOW_CROSS_ADAPTER
- ALLOW_SIMULTANEOUS_ACCESS
- VIDEO_DECODE_REFERENCE_ONLY

無法上傳或 READBACK 資源的堆積類型。

無法 SIMULTANEOUS_ACCESS 資源。 不允許使用跨介面卡的資源。

#### <a name="data"></a>資料
螢幕空間影像的每個位元組都對應至 [**D3D12_SHADING_RATE**](/windows/desktop/api/d3d12/ne-d3d12-d3d12_shading_rate)  列舉的值。

#### <a name="resource-state"></a>資源狀態
當資源作為螢幕空間影像使用時，需要轉換成隻讀狀態。 針對此目的，會定義唯讀狀態 [**D3D12_RESOURCE_STATE_SHADING_RATE_SOURCE**](/windows/desktop/api/d3d12/ne-d3d12-d3d12_resource_states)。

映射資源會轉換為該狀態，使其再次成為可寫入的狀態。

#### <a name="setting-the-image"></a>設定影像
指定著色器速率的螢幕空間影像是在命令清單上設定的。

已設定為陰影速率來源的資源無法從任何著色器階段讀取或寫入。

您 `null` 可以設定螢幕空間影像來指定著色器速率。 這樣做的效果是從螢幕空間影像的比重一直一直使用。 畫面空間影像一開始可以被視為設定為 `null` 。

#### <a name="promotion-and-decay"></a>升級與衰減
螢幕空間影像資源對於升階或衰減沒有任何特別的含意。

### <a name="per-primitive-attribute"></a>每個基本屬性
每個基本型別的屬性加入了將陰影速率詞彙指定為誘發頂點屬性的功能。 這個屬性是平面陰影 &mdash; ，也就是將它傳播至目前三角形或線條基本型別中的所有圖元。 相較于其他的陰影比率規範，使用每個基本型別的屬性可以更精細地控制影像品質。

每個基本屬性是名為的可設定語義 `SV_ShadingRate` 。 `SV_ShadingRate` 存在於 [HLSL 著色器模型 6.4](/windows/desktop/direct3dhlsl/hlsl-shader-model-6-4-features-for-direct3d-12)中。

如果有 VS 或 GS 集 `SV_ShadingRate` ，但未啟用 VRS，則語義設定沒有任何作用。 如果未針對每個基本型別指定任何值 `SV_ShadingRate` ，則會假設為每個基本的貢獻的陰影比率值為1x1。

### <a name="combining-shading-rate-factors"></a>組合網底比例因數
使用此圖表時，會依序套用不同的陰影速率來源。

![圖表會顯示標示為 A、誘發頂點網底速率、標示為 B、在結合器套用的管線狀態，然後以影像為基礎的陰影速率（標示為 B）套用於結合器。](images/Combiners.PNG "網底結合器")

A 和 B 的每一對都會使用結合器結合。

\* 依頂點屬性指定著色器速率時。

- 如果使用幾何著色器，則可以透過該顏色來指定陰影速率。
- 如果未使用幾何著色器，則會以誘發頂點指定網底比例。

#### <a name="list-of-combiners"></a>結合器清單
支援下列結合器。 使用結合器 (C) 和兩個輸入 (A 和 B) 。

- **傳遞**。 C. xy = xy。
- 覆 **寫**。 C. xy = b. xy。
- **品質較高**。 C. xy = min (xy、b. xy) 。
- **品質較低**。 C. xy = (xy、b. xy) 的最大值。
- **將成本 B 相對** 于。C. xy = min (maxRate，xy + b. xy) 。

其中 `maxRate` 是裝置上最大的粗略圖元允許維度。 這會是

- **D3D12_AXIS_SHADING_RATE_2X** (也就是 1) 的值（如果 AdditionalShadingRatesSupported 為） `false` 。
- 如果 AdditionalShadingRatesSupported 為， **D3D12_AXIS_SHADING_RATE_4X** (，也就是 2) 的值 `true` 。

您可以透過 [**ID3D12GraphicsCommandList5：： RSSetShadingRate**](/windows/desktop/api/d3d12/nf-d3d12-id3d12graphicscommandlist5-rssetshadingrate)，在命令清單上設定可變速率網底的結合器選項。

如果未曾設定任何結合器，則會保持為預設值，也就是通過。

如果結合器的來源是不允許在支援資料表中的 [**D3D12_AXIS_SHADING_RATE**](/windows/desktop/api/d3d12/ne-d3d12-d3d12_axis_shading_rate)，則會將輸入清理 *為支援的* 陰影比率。

如果結合器的輸出未對應到平臺上支援的陰影速率，則會將結果清理 *為支援的* 陰影速率。

### <a name="default-state-and-state-clearing"></a>預設狀態和狀態清除
所有的陰影比例來源，亦即

- 在命令清單上指定的 [管線狀態-指定的速率 (]) ，
- 螢幕空間影像指定的速率，以及
- 每個基本屬性

預設值為 **D3D12_SHADING_RATE_1X1**。 預設結合器是 {通過，通過}。

如果未指定任何螢幕空間影像，則會從該來源推斷網底比例（1x1）。

如果未指定每個基本型別的屬性，則會從該來源推斷出網底比例（1x1）。

[ID3D12CommandList：： ClearState](/windows/desktop/api/d3d12/nf-d3d12-id3d12graphicscommandlist-clearstate) 會將管線狀態指定的速率重設為預設值，並將螢幕空間影像的選取範圍重設為預設值「沒有螢幕空間影像」。

## <a name="querying-shading-rate-by-using-sv_shadingrate"></a>使用 SV_ShadingRate 來查詢陰影率
知道硬體在任何給定的圖元著色器調用中所選取的陰影速率，會很有用。 這可能會在您的 PS 程式碼中啟用各種優化。 僅限 PS 系統變數提供了 `SV_ShadingRate` 陰影速率的相關資訊。

### <a name="type"></a>類型
此語義的型別為 uint。

### <a name="data-interpretation"></a>資料轉譯
資料會被解讀為 [**D3D12_SHADING_RATE**](/windows/desktop/api/d3d12/ne-d3d12-d3d12_shading_rate) 列舉的值。

### <a name="if-vrs-is-not-being-used"></a>如果未使用 VRS
如果未使用粗略的圖元陰影，則 `SV_ShadingRate` 會以1x1 的值讀回，表示正常的圖元。

### <a name="behavior-under-sample-based-execution"></a>以範例為基礎執行的行為
如果圖元著色器輸入， `SV_ShadingRate` 而且也使用以範例為基礎的執行 &mdash; ，例如，藉由輸入 `SV_SampleIndex` 或使用範例插補關鍵字，它就會失敗編譯。

> ### <a name="remarks-on-deferred-shading"></a>延後陰影的備註
>
> 延後的陰影應用程式的光源可能需要知道螢幕的哪個區域所使用的陰影速率。 如此一來，就能以較粗的速率啟動「照明」分派。 `SV_ShadingRate`如果將變數寫出至 gbuffer，就可以使用該變數來完成此動作。

## <a name="depth-and-stencil"></a>深度和樣板
使用粗略圖元網底時，一律會計算深度和樣板和涵蓋範圍，並以完整樣本解析度來發出。

## <a name="using-the-shading-rate-requested"></a>使用要求的陰影率
針對所有層級，如果要求的是陰影率，而且在裝置和 MSAA 層級組合上支援，則這是硬體所提供的陰影速率。

要求的陰影速率表示計算為結合器輸出的陰影速率 (請參閱本主題中的 [合併陰影比例因數](#combining-shading-rate-factors) 一節) 。

在取樣計數小於或等於四的轉譯作業中，支援的陰影比例為1x1、1x2、2x1 或2x2。 如果 *AdditionalShadingRatesSupported* 功能為 `true` ，則可以使用2x4、4x2 和4x4 來支援某些取樣計數的陰影比例 (請參閱本主題中的 [使用可變速率陰影 (VRS)](#with-variable-rate-shading-vrs) 一節中的表格) 。

## <a name="screen-space-derivatives"></a>螢幕空間衍生
圖元對相鄰圖元漸層的計算會受到粗略圖元陰影的影響。 例如，使用2x2 粗圖元時，漸層的大小會與未使用粗圖元時的大小兩倍。 視您想要的功能而定，您的應用程式可能會想要調整著色器來彌補這一點 &mdash; 。

因為 mips 是根據螢幕空間導數選擇的，所以使用粗略圖元陰影會影響 mip 選取專案。 使用粗略圖元陰影會導致選取較不詳細的 mips，相較于不使用粗圖元時。

## <a name="attribute-interpolation"></a>屬性插補
圖元著色器的輸入可能會根據其來源頂點插補。 由於變動率陰影會影響每個圖元著色器調用所寫入的目的地區域，因此會與屬性插補互動。 三種類型的插補是中央、距心和樣本。

### <a name="center"></a>Center
粗略圖元的中心插補位置是完全粗略圖元區域的幾何中心。 `SV_Position` 一律插在粗略圖元區域的中央。

### <a name="centroid"></a>質心
當您搭配 MSAA 使用粗略的圖元陰影時，對於每個微調圖元，仍會寫入配置給目標 MSAA 層級的完整樣本數。 因此，距心插補位置會將所有範例視為粗圖元內的正確圖元。 話雖如此，距心插補位置會定義為第一個涵蓋的範例（以樣本索引的遞增順序排列）。 範例的有效涵蓋範圍是和-ed，並具有對應的轉譯器狀態 SampleMask 位。

> [!NOTE]
> 在第1層使用粗圖元網底時，SampleMask 一律為完整遮罩。 如果 SampleMask 設定為不是完整遮罩，則會在第1層停用粗圖元網底。

### <a name="sample-based-execution"></a>以範例為基礎的執行
使用範例插補功能所造成的範例型執行（或 *supersampling*） &mdash; &mdash; 可用於粗略的圖元陰影，並會導致每個取樣叫用圖元著色器。 針對取樣計數 N 的目標，圖元著色器會每個微調圖元叫用 N 次。

### <a name="evaluateattributesnapped"></a>EvaluateAttributeSnapped
提取模型內建函式與第1層的粗略圖元陰影不相容。 如果嘗試在第1層使用具有粗圖元網底的提取模型內建函式，則會自動停用粗圖元網底。

可以 `EvaluateAttributeSnapped` 在第2層上搭配使用內建和粗圖元陰影。 它的語法與往常一樣。

```hlsl
numeric EvaluateAttributeSnapped(   
    in attrib numeric value, 
    in int2 offset);
```

針對內容， `EvaluateAttributeSnapped` 有一個具有兩個欄位的 offset 參數。 使用時若未使用粗圖元陰影，則只會使用在完整32的低序位四個位。 這四個位代表範圍 [-8，7]。 此範圍橫跨圖元內的16x16 方格。 範圍是包含圖元的上邊緣和左邊緣，而底部和右邊的邊緣則否。 位移 (-8、-8) 位於左上角，而位移 (7，7) 是右下角。 位移 (0，0) 是圖元的中心。

搭配使用粗圖元網底時， `EvaluateAttributeSnapped` 的 offset 參數能夠指定更大範圍的位置。 Offset 參數會為每個微調圖元選取16x16 格線，而且有多個精細圖元。 所用的可表示範圍和後續的位數目，取決於粗略圖元的大小。 會包含粗略圖元的上邊緣和左邊緣，而底部和右邊則不會。

下表說明 `EvaluateAttributeSnapped` 每個粗略圖元大小的 offset 參數的解釋。

#### <a name="evaluateattributesnappeds-offset-range"></a>EvaluateAttributeSnapped 的位移範圍

|粗圖元大小  |可索引範圍             |表示範圍大小  |需要的位數 {x，y}  |可用位的二進位遮罩          |    
|------------------:|---------------------------:|-------------------------:|-----------------------------:|-----------------------------------:|    
|1x1 (良好)          |{ \[ -8、7 \] 、 \[ -8、7 \] }      |{16，16}                  |{4，4}                        |{000000000000xxxx, 000000000000xxxx}|    
|1x2                |{ \[ -8、7 \] 、 \[ -16、15 \] }    |{16，32}                  |{4，5}                        |{000000000000xxxx, 00000000000xxxxx}|    
|2 x 1                |{ \[ -16、15 \] 、 \[ -8、7 \] }    |{32，16}                  |{5，4}                        |{00000000000xxxxx, 000000000000xxxx}|    
|2 x 2                |{ \[ -16、15 \] 、 \[ -16、15 \] }  |{32，32}                  |{5，5}                        |{00000000000xxxxx, 00000000000xxxxx}|    
|2x4                |{ \[ -16、15 \] 、 \[ -32、31 \] }  |{32，64}                  |{5，6}                        |{00000000000xxxxx, 0000000000xxxxxx}|    
|4 x 2                |{ \[ -32、31 \] 、 \[ -16、15 \] }  |{64，32}                  |{6，5}                        |{0000000000xxxxxx, 00000000000xxxxx}|    
|4x4                |{ \[ -32，31 \] ， \[ -32，31 \] }  |{64，64}                  |{6，6}                        |{0000000000xxxxxx, 0000000000xxxxxx}|   

下表是從固定點轉換成十進位和小數標記法的指南。 二進位遮罩中的第一個可用位是正負號位，而二進位遮罩的其餘部分則包含數位部分。

傳入的四位值的數位配置 `EvaluateAttributeSnapped` 並不是可變速率的陰影所特有。 它是為了完整性而重述。

適用于四位值。

| 二進位值 | Decimal  | 小數 |
|-------------:|---------:|-----------:|
|         1000 |-0.5 f     |-8/16     |
|         1001 |-0.4375 f  |-7/16|    |
|         1010 |-0.375 f   |-6/16|    |
|         1011 |-0.3125 f  |-5/16     |
|         1100 |-0.25 f    |-4/16     |
|         1101 |-0.1875 f  |-3/16     |
|         1110 |-0.125 f   |-2/16     |
|         1111 |-0.0625 f  |-1/16      |
|         0000 |0.0f      |0 / 16      |
|         0001 |-0.0625 f  |1 / 16      |
|         0010 |-0.125 f   |2 / 16      |
|         0011 |-0.1875 f  |3 / 16      |
|         0100 |-0.25 f    |4 / 16      |
|         0101 |-0.3125 f  |5 / 16      |
|         0110 |-0.375 f   |6 / 16      |
|         0111 |-0.4375 f  |7 / 16      |

適用于五位值。

| 二進位值 | Decimal  | 小數 |
|-------------:|---------:|-----------:|
|        10000 |-1        |-16/16    |
|        10001 |-0.9375   |-15/16    |
|        10010 |-0.875    |-14/16    |
|        10011 |-0.8125   |-13/16    |
|        10100 |-0.75     |-12/16    |
|        10101 |-0.6875   |-11/16    |
|        10110 |-0.625    |-10/16    |
|        10111 |-0.5625   |-9/16     |
|        11000 |-0。5      |-8/16     |
|        11001 |-0.4375   |-7/16     |
|        11010 |-0.375    |-6/16     |
|        11011 |-0.3125   |-5/16     |
|        11100 |-0.25     |-4/16     |
|        11101 |-0.1875   |-3/16     |
|        11110 |-0.125    |-2/16     |
|        11111 |-0.0625   |-1/16     |
|        00000 |0         |0 / 16      |
|        00001 |0.0625    |1 / 16      |
|        00010 |0.125     |2 / 16      |
|        00011 |0.1875    |3 / 16      |
|        00100 |0.25      |4 / 16      |
|        00101 |0.3125    |5 / 16      |
|        00110 |0.375     |6 / 16      |
|        00111 |0.4375    |7 / 16      |
|        01000 |0.5       |8 / 16      |
|        01001 |0.5625    |9 / 16      |
|        01010 |0.625     |10 / 16     |
|        01011 |0.6875    |11 / 16     |
|        01100 |0.75      |12 / 16     |
|        01101 |0.8125    |13 / 16     |
|        01110 |0.875     |14 / 16     |
|        01111 |0.9375    |15 / 16     |

適用于六位值。

| 二進位值 | Decimal  | 小數 |
|-------------:|---------:|-----------:|
|       100000 |-2        |-32/16    |
|       100001 |-1.9375   |-31/16    |
|       100010 |-1.875    |-30/16    |
|       100011 |-1.8125   |-29/16    |
|       100100 |-1.75     |-28/16    |
|       100101 |-1.6875   |-27/16    |
|       100110 |-1.625    |-26/16    |
|       100111 |-1.5625   |-25/16    |
|       101000 |-1。5      |-24/16    |
|       101001 |-1.4375   |-23/16    |
|       101010 |-1.375    |-22/16    |
|       101011 |-1.3125   |-21/16    |
|       101100 |-1.25     |-20/16    |
|       101101 |-1.1875   |-19/16    |
|       101110 |-1.125    |-18/16    |
|       101111 |-1.0625   |-17/16    |
|       110000 |-1        |-16/16    |
|       110001 |-0.9375   |-15/16    |
|       110010 |-0.875    |-14/16    |
|       110011 |-0.8125   |-13/16    |
|       110100 |-0.75     |-12/16    |
|       110101 |-0.6875   |-11/16    |
|       110110 |-0.625    |-10/16    |
|       110111 |-0.5625   |-9/16     |
|       111000 |-0。5      |-8/16     |
|       111001 |-0.4375   |-7/16     |
|       111010 |-0.375    |-6/16     |
|       111011 |-0.3125   |-5/16     |
|       111100 |-0.25     |-4/16     |
|       111101 |-0.1875   |-3/16     |
|       111110 |-0.125    |-2/16     |
|       111111 |-0.0625   |-1/16     |
|       000000 |0         |0 / 16      |
|       000001 |0.0625    |1 / 16      |
|       000010 |0.125     |2 / 16      |
|       000011 |0.1875    |3 / 16      |
|       000100 |0.25      |4 / 16      |
|       000101 |0.3125    |5 / 16      |
|       000110 |0.375     |6 / 16      |
|       000111 |0.4375    |7 / 16      |
|       001000 |0.5       |8 / 16      |
|       001001 |0.5625    |9 / 16      |
|       001010 |0.625     |10 / 16     |
|       001011 |0.6875    |11 / 16     |
|       001100 |0.75      |12 / 16     |
|       001101 |0.8125    |13 / 16     |
|       001110 |0.875     |14 / 16     |
|       001111 |0.9375    |15 / 16     |
|       010000 |1         |16 / 16     |
|       010001 |1.0625    |17 / 16     |
|       010010 |1.125     |18 / 16     |
|       010011 |1.1875    |19 / 16     |
|       010100 |1.25      |20 / 16     |
|       010101 |1.3125    |21 / 16     |
|       010110 |1.375     |22 / 16     |
|       010111 |1.4375    |23 / 16     |
|       011000 |1.5       |24 / 16     |
|       011001 |1.5625    |25 / 16     |
|       011010 |1.625     |26 / 16     |
|       011011 |1.6875    |27 / 16     |
|       011100 |1.75      |28 / 16     |
|       011101 |1.8125    |29 / 16     |
|       011110 |1.875     |30 / 16     |
|       011111 |1.9375    |31 / 16     |

使用粗圖元陰影時，evaluateable 位置的格線會以與正確圖元的相同方式，在 `EvaluateAttributeSnapped` 粗圖元中心放置。

## <a name="setsamplepositions"></a>SetSamplePositions
當 API [**ID3D12GraphicsCommandList1：： SetSamplePositions**](/windows/desktop/api/d3d12/nf-d3d12-id3d12graphicscommandlist1-setsamplepositions) 與粗略的陰影搭配使用時，api 會將範例位置設定為精細圖元。

## <a name="sv_coverage"></a>SV_Coverage
如果在 `SV_Coverage` 第1層將宣告為著色器輸入或輸出，則會停用粗圖元網底。

您可以 `SV_Coverage` 在第2層使用具有粗略圖元陰影的語義，並反映正在寫入的 MSAA 目標範例。

當使用粗圖元網底時， &mdash; 可讓多個來源圖元組成磚 &mdash; ，涵蓋範圍遮罩代表來自該磚的所有樣本。

指定粗圖元網底與 MSAA 的相容性時，所需指定的涵蓋範圍位數目可能會不同。 例如，使用 [**D3D12_SHADING_RATE_2x2**](/windows/desktop/api/d3d12/ne-d3d12-d3d12_shading_rate)的 4x MSAA 資源，每個粗略的圖元都會寫入四個精細的圖元，而每個精細圖元都有四個樣本。 這表示每個粗略的圖元都會寫入總計 4 * 4 = 16 個樣本。

### <a name="number-of-coverage-bits-needed"></a>所需的涵蓋範圍位數目
下表指出每個粗略圖元大小和 MSAA 層級組合需要多少涵蓋區位。

![表格顯示粗的圖元大小、精細圖元數，以及 M S 的層級。](images/NumberOfCoverageBits.PNG "涵蓋範圍位")

如表格中所示，使用透過 Direct3D 12 公開的變動率陰影功能，一次不能使用粗略圖元來寫入超過16個樣本。 This restriction is due to Direct3D 12's constraints regarding which MSAA levels are allowed with which coarse pixel size (see the table in the [With variable-rate shading (VRS)](#with-variable-rate-shading-vrs) section in this topic).

### <a name="ordering-and-format-of-bits-in-the-coverage-mask"></a>涵蓋範圍遮罩中的位順序和格式
涵蓋範圍遮罩的位會遵循妥善定義的順序。 遮罩是由左到右的 coverages 所組成，然後由上到下 (資料行主要) 順序。 涵蓋範圍位是涵蓋範圍語義的低序位位，而且會密集封裝在一起。

下表顯示支援的粗略圖元大小和 MSAA 層級組合的涵蓋範圍遮罩格式。

![表格顯示粗略的圖元大小、粗略圖元的圖表，以及 1 x M S 的涵蓋範圍位。](images/Coverage1x.PNG "涵蓋範圍：1x")

下表會 2x MSAA 圖元，其中每個圖元都有兩個索引0和1的樣本。

在圖元上放置樣本標籤的位置是為了說明之用，不一定要在該圖元上傳達樣本的空間 {X，Y} 位置;尤其是假設範例位置可以用程式設計方式變更。 範例是由其以0為基礎的索引所參考。

![表格顯示粗略的圖元大小、粗圖元圖表，以及 2 x M S 的涵蓋範圍位。](images/Coverage2x.PNG "涵蓋範圍：2倍")

下表顯示4x 個 MSAA 圖元，其中的每個圖元都有四個範例的索引0、1、2和3。

![表格顯示粗略的圖元大小、粗圖元圖表，以及 4 x M S 的涵蓋範圍位。](images/Coverage4x.PNG "涵蓋範圍：4x")

## <a name="discard"></a>捨棄
使用 HLSL 語義搭配 `discard` 粗略的圖元陰影時，會捨棄粗略的圖元。

## <a name="target-independent-rasterization-tir"></a>目標獨立的點陣化 (TIR) 
使用粗圖元網底時，不支援 TIR。

## <a name="raster-order-views-rovs"></a> (ROVs) 的點陣順序視圖
ROV interlocks 會指定為以精細的圖元細微性運作。 如果每個樣本都執行了陰影，則 interlocks 會在取樣的細微性上運作。

## <a name="conservative-rasterization"></a>保守的點陣化
您可以使用保守的點陣化與可變速率的陰影。 當您搭配使用保守式柵格化與粗圖元網底時，在粗略圖元內的精確圖元會獲得完整的涵蓋範圍。

### <a name="coverage"></a>涵蓋範圍
使用保守的點陣化時，涵蓋範圍語義包含所涵蓋之正確圖元的完整遮罩，而0代表未涵蓋的精確圖元。

## <a name="bundles"></a>束
您可以針對組合呼叫可變速率的陰影 Api。

## <a name="render-passes"></a>轉譯階段
您可以在轉譯 [階段](/windows/desktop/direct3d12/direct3d-12-render-passes)中呼叫可變速率的陰影 api。

## <a name="calling-the-vrs-apis"></a>呼叫 VRS Api
下一節說明您的應用程式透過 Direct3D 12 存取可變速率陰影的方式。

### <a name="capability-querying"></a>功能查詢

若要查詢介面卡的可變速率陰影功能，請呼叫 [**ID3D12Device：： CheckFeatureSupport**](/windows/desktop/api/d3d12/nf-d3d12-id3d12device-checkfeaturesupport) （ [**D3D12_FEATURE：:D 3D12_FEATURE_D3D12_OPTIONS6**](/windows/desktop/api/d3d12/ne-d3d12-d3d12_feature)），並為函式提供 [ **D3D12_FEATURE_DATA_D3D12_OPTIONS6** 結構](/windows/desktop/api/d3d12/ns-d3d12-d3d12_feature_data_d3d12_options6)以供您填入。 **D3D12_FEATURE_DATA_D3D12_OPTIONS6** 結構包含數個成員，包括列舉型別 [**D3D12_VARIABLE_SHADING_RATE_TIER**](/windows/desktop/api/d3d12/ne-d3d12-d3d12_variable_shading_rate_tier) (D3D12_FEATURE_DATA_D3D12_OPTIONS6：： VariableShadingRateTier) 的成員，以及一個指出是否支援背景處理 (D3D12_FEATURE_DATA_D3D12_OPTIONS6：： BackgroundProcessingSupported) 。

例如，若要查詢第1層功能，您可以這麼做。

```cpp
D3D12_FEATURE_DATA_D3D12_OPTIONS6 options;
return 
    SUCCEEDED(m_device->CheckFeatureSupport(
        D3D12_FEATURE_D3D12_OPTIONS6, 
        &options, 
        sizeof(options))) && 
    options.ShadingRateTier == D3D12_VARIABLE_SHADING_RATE_TIER_1;
```

### <a name="shading-rates"></a>網底比例

[ **D3D12_SHADING_RATE** 列舉](/windows/desktop/api/d3d12/ne-d3d12-d3d12_shading_rate)中的值會進行組織，如此一來，就可以輕鬆地將陰影速率可分解為兩個軸，其中每個軸的值會根據 [ **D3D12_AXIS_SHADING_RATE** 列舉](/windows/desktop/api/d3d12/ne-d3d12-d3d12_axis_shading_rate)，以對數間距表示。

您可以撰寫宏來撰寫兩個軸網底比例，以像這樣的陰影比例。

```cpp
#define D3D12_MAKE_COARSE_SHADING_RATE(x,y) ((x) << 2 | (y))
D3D12_MAKE_COARSE_SHADING_RATE(
    D3D12_AXIS_SHADING_RATE_2X, 
    D3D12_AXIS_SHADING_RATE_1X)
```

平臺也提供這些宏，定義于中 `d3d12.h` 。

```cpp
#define D3D12_GET_COARSE_SHADING_RATE_X_AXIS(x) ((x) >> 2 )
#define D3D12_GET_COARSE_SHADING_RATE_Y_AXIS(y) ((y) & 3 )
```

這些可以用來仔細分析和瞭解 `SV_ShaderRate` 。

> [!NOTE]
> 這項資料轉譯的目的是要說明可由著色器操作的螢幕空間影像。 上述各節將進一步討論。 但是，並沒有理由讓所有地方都能使用不一致的粗略圖元大小定義，包括設定命令層級的陰影速率。

### <a name="setting-command-level-shading-rate-and-combiners"></a>設定命令層級的陰影比率和結合器
您可以透過 [**ID3D12GraphicsCommandList5：： RSSetShadingRate**](/windows/desktop/api/d3d12/nf-d3d12-id3d12graphicscommandlist5-rssetshadingrate) 方法來指定陰影比率和選擇性的結合器。 您可以針對基底網底比例傳遞 [**D3D12_SHADING_RATE**](/windows/desktop/api/d3d12/ne-d3d12-d3d12_shading_rate) 值，並將 [D3D12_SHADING_RATE_COMBINER](/windows/desktop/api/d3d12/ne-d3d12-d3d12_shading_rate_combiner) 值的選擇性陣列傳遞給。

### <a name="preparing-the-screen-space-image"></a>準備螢幕空間影像
指定可用陰影率影像的唯讀資源狀態，定義為 [D3D12_RESOURCE_STATES：:D 3D12_RESOURCE_STATE_SHADING_RATE_SOURCE](/windows/desktop/api/d3d12/ne-d3d12-d3d12_resource_states)。

### <a name="setting-the-screen-space-image"></a>設定螢幕空間影像
您可以透過 [**ID3D12GraphicsCommandList5：： RSSetShadingRateImage**](/windows/desktop/api/d3d12/nf-d3d12-id3d12graphicscommandlist5-rssetshadingrateimage) 方法指定螢幕空間影像。

```cpp
m_commandList->RSSetShadingRateImage(screenSpaceImage);
```

### <a name="querying-the-tile-size"></a>查詢磚大小
您可以從 [**D3D12_FEATURE_DATA_D3D12_OPTIONS6：： ShadingRateImageTileSize**](/windows/desktop/api/d3d12/ns-d3d12-d3d12_feature_data_d3d12_options6) 成員查詢磚大小。 請參閱上述的 [功能查詢](#capability-querying) 。

由於水準和垂直維度一律相同，因此會取出一個維度。 如果系統的功能 [**D3D12_SHADING_RATE_TIER_NOT_SUPPORTED**](/windows/desktop/api/d3d12/ne-d3d12-d3d12_variable_shading_rate_tier)，則傳回的磚大小為0。
