---
description: 原生 JPEG XR 編解碼器可透過 Windows 影像處理元件 (WIC) 取得。 編解碼器支援的 JPEG XR 格式，是專為消費者和專業數位攝影所設計。
ms.assetid: CB8D1A5F-B544-462E-8927-F45512CED873
title: JPEG XR 編解碼器總覽
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: f32ffa397667b325d4e49eadf4d8ce42d49e8a88
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/08/2021
ms.locfileid: "106985295"
---
# <a name="jpeg-xr-codec-overview"></a>JPEG XR 編解碼器總覽

原生 JPEG XR 編解碼器可透過 Windows 影像處理元件 (WIC) 取得。 編解碼器支援的 JPEG XR 格式，是專為消費者和專業數位攝影所設計。

JPEG XR 格式最多可達到原始 JPEG 格式的壓縮效率兩倍，並減少較不明顯的壓縮成品。 JPEG XR 的功能包括：

-   支援單色、RGB、CMYK 和 n 聲道影像
-   8-、16和32位的整數格式
-   使用固定點或浮點色彩值的高動態範圍、寬範圍格式
-   漸進式解碼
-   使用相同壓縮演算法的失真或無損編碼
-   支援在大型影像中解碼感興趣的區域

JPEG XR 格式是在下列標準檔中定義：

-   ITU-T T. 832： *資訊技術– JPEG XR 影像編碼系統–影像編碼規格*
-   ISO/IEC 29199-2:2010： *資訊技術— JPEG XR 影像編碼系統-第2部分：影像編碼規格*

JPEG XR 標準主要是以 [HD 相片](hdphoto-format-overview.md) 格式為基礎，但是這兩種格式之間有一些差異。 在 Windows 8 中，已更新 HD 相片編解碼器以支援 JPEG XR。 編碼器現在一律會輸出符合 JPEG XR 規範的位串流。 此解碼器可以解碼 JPEG XR 和 HD 相片影像。

我們已對 JPEG XR 編解碼器進行大幅的效能改進，相對於 HD 相片編解碼器。 例如，子解析影像解碼（例如縮圖產生）已改善，以及低解析度影像解碼。 建議您使用 JPEG XR 格式，而不是使用 HD 相片格式。

## <a name="codec-information"></a>編解碼器資訊



|                     |                                                                         |
|---------------------|-------------------------------------------------------------------------|
| 副檔名 | "jxr" 和 "wdp"                                                         |
| 容器 GUID      | **GUID \_ ContainerFormatWmp**                                            |
| 解碼器 GUID        | **CLSID \_ WICWmpDecoder**                                                |
| 編碼器 GUID        | **CLSID \_ WICWmpEncoder**                                                |
| 設定檔支援     | 編碼器和解碼最多可支援主要設定檔，最高可達層級128。 |



 

## <a name="codec-features"></a>編解碼器功能

### <a name="high-dynamic-range"></a>高動態範圍

JPEG XR 支援使用浮點或固定點色彩的高動態範圍影像。 在這些色彩格式中，圖元的數值範圍大於可見範圍，因此您可以在中繼處理階段中調整可見範圍的上方或下方的色彩。

-   固定點：在固定點標記法中，0代表黑色，而1.0 表示最大飽和度。 JPEG XR 編解碼器支援16位和32位的固定點格式。 若為16位，1.0 = 0x2000h，可為可見範圍 \[ 0 ... 1 提供 13 \] 位。 總範圍是–4.0 到 + 3.999，並以線性方式對應。 若為32位、1.0 = 0x01000000h，可見範圍為24位，而總範圍為–128到 + 127.999。
-   浮點數：在浮點表示中，0代表黑色，而1.0 代表最大飽和度。 JPEG XR 編解碼器支援16位和32位的浮點數格式。

### <a name="tiles"></a>磚

框架可以分割成矩形子領域加寬，稱為 *磚*。 磚是包含巨大區塊矩形陣列的影像區域。 磚可讓影像的區域進行解碼，而不需要處理整個影像。

在編碼期間，藉由設定 **HorizontalTileSlices** 和 **VerticalTileSlices** 屬性來選取圖格數目。 磚大小下限為16×16圖元。 編碼器會調整磚數目以維持這項限制。 每個磚都有相關聯的儲存和處理額外負荷，因此您應該考慮特定案例所需的磚數目。

### <a name="image-stream-output"></a>影像資料流程輸出

JPEG XR 標準定義了 JPEG XR 檔案的兩個部分：

-   影像位資料流程，定義于標準的主體中。
-   映射容器。 檔案包含了 Exif 和 XMP 中繼資料，並定義于標準的附錄 A 中。

標準可將影像串流內嵌在另一種類型的檔案容器內，因此可能會被允許。 編碼器支援僅限資料流程模式，會輸出沒有映射容器的原始影像位串流。 應用程式可以將位資料流程儲存為一些其他的容器格式。

若要啟用僅限資料流程模式，請設定 **StreamOnly** 屬性。

### <a name="image-quality-settings"></a>影像品質設定

數個編解碼器屬性會控制編碼器的輸出影像品質。

-   [ImageQuality](#imagequality) 是在 WIC 編解碼器之間的通用屬性。 它會將影像品質指定為0.0 –1.0 的單一浮點值，
-   [ [品質](#image-quality-settings)]、[重 [迭](#overlap)] 和 [ [取樣](#subsampling) ] 屬性能讓您更充分掌控品質設定。

若要使用「 [品質](#image-quality-settings)」、「重 [迭](#overlap)」和「 [取樣](#subsampling) 」屬性，請將 [UseCodecOptions](#usecodecoptions) 屬性設定為 **VARIANT \_ TRUE**。

如果 [UseCodecOptions](#usecodecoptions) 是 **Variant \_ false** (**Variant \_ false** 是) 編碼器使用 [ImageQuality](#imagequality) 屬性的預設值。 編碼器會透過查閱資料表，將 ImageQuality 的值對應到 [品質](#image-quality-settings)、重 [迭](#overlap)和次 [取樣](#subsampling) 。

編碼器不支援 **CompressionQuality** 屬性。

### <a name="compressed-domain-transcode"></a>壓縮的網域轉碼

JPEG XR 編解碼器可以執行某些影像轉換，而不需要實際解碼壓縮的資料並重新編碼。 壓縮的網域作業非常有效率，而且可避免在您將損及重新編碼已壓縮的影像時，通常會發生的任何額外品質損失。

以下是支援的壓縮網域作業：

-   裁剪影像的區域。
-   旋轉或翻轉影像。
-   捨棄頻率資料來建立較小的影像檔案。
-   重新組織空間與頻率順序之間的影像。

如果來源影像是 JPEG XR 影像，JPEG XR 編碼器會使用壓縮的網域轉碼（如果可能的話）。 當編碼器執行壓縮的網域作業時，它會忽略下列編解碼器屬性： [AlphaQuality](#alphaquality)、 [ImageQuality](#imagequality)、InterleavedAlpha [、不](#lossless)失真重[迭](#overlap)和[品質](#image-quality-settings)。 [](#interleavedalpha) 如果 [HorizontalTileSlices](/windows) 和 [VerticalTileSlices](/windows) 屬性存在，您必須將它們設定為零。 您無法在壓縮的網域轉碼中變更影像的磚大小。

下列清單說明如何執行影像轉換。

-   若要裁剪影像，請在 **WriteSource** 方法的 [**WICRect**](/windows/desktop/api/Wincodec/nf-wincodec-iwicbitmapframeencode-writesource)參數中設定所需的區域。
-   若要旋轉或翻轉影像，請設定 [BitmapTransform](#bitmaptransform) 屬性。
-   若要捨棄映射中的頻率資料，請設定 [ImageDataDiscard](#imagedatadiscard) 屬性。 若要捨棄 Alpha 通道中的頻率資料，請設定 [AlphaDataDiscard](#alphadatadiscard) 屬性。 捨棄頻率資料可減少編碼的檔案大小，並可減少解析度。
-   若要在頻率和空間排序之間變更影像組織，請設定 [FrequencyOrdering](/windows) 屬性。

若要停用壓縮的網域轉碼，並強制編碼器重新編碼影像，請將 [UseCodecOptions](#usecodecoptions) 設定為 **variant \_ TRUE** ，並將 [CompressedDomainTranscode](#compresseddomaintranscode) 設定為 **variant \_ FALSE**。

## <a name="encoder-options"></a>編碼器選項

若要設定編碼屬性，請使用 [**IPropertyBag2**](/previous-versions/windows/internet-explorer/ie-developer/platform-apis/aa768192(v=vs.85)) 介面。 如需詳細資訊，請參閱 [編碼總覽](-wic-creating-encoder.md)。

下列清單指定編碼器選項。

-   [AlphaDataDiscard](#alphadatadiscard)
-   [AlphaQuality](#alphaquality)
-   [BitmapTransform](#bitmaptransform)
-   [CompressedDomainTranscode](#compresseddomaintranscode)
-   [FrequencyOrder](#frequencyorder)
-   [HorizontalTileSlices](#horizontaltileslices)
-   [IgnoreOverlap](#ignoreoverlap)
-   [ImageDataDiscard](#imagedatadiscard)
-   [ImageQuality](#imagequality)
-   [InterleavedAlpha](#interleavedalpha)
-   [Lossless](#lossless)
-   [重疊](#overlap)
-   [ProgressiveMode](#progressivemode)
-   [品質](#image-quality-settings)
-   [StreamOnly](#streamonly)
-   [圖元](#subsampling)
-   [UseCodecOptions](#usecodecoptions)
-   [VerticalTileSlices](#verticaltileslices)

### <a name="alphadatadiscard"></a>AlphaDataDiscard

設定壓縮的網域轉碼期間要捨棄的 Alpha 頻率資料量。



| 資料類型 | VARTYPE     | 範圍 | 預設 |
|-----------|-------------|-------|---------|
| **UCHAR** | **VT \_ UI1** | 0–4   | 無    |



 

只有當 [CompressedDomainTranscode](#compresseddomaintranscode) 屬性設定為 **VARIANT \_ TRUE** ，且影像包含平面 Alpha 色板或交錯 Alpha 色板時，才會套用這個屬性; 否則會忽略此屬性。

針對包含平面 Alpha 色板的影像，下列值是有效的。



| 值 | 描述                                                                                                                                                                                                                                                                                                                                                                                                                                                                |
|-------|----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| 0     | 不捨棄影像頻率資料。                                                                                                                                                                                                                                                                                                                                                                                                                                      |
| 1     | Flexbits 會被捨棄。 這可任意減少轉碼影像的平面 Alpha 通道品質。 ，而不會變更有效的解決方式。 檔案大小和品質的確切縮減取決於許多因素，而且無法完全指定。                                                                                                                                                                                           |
| 2     | 會捨棄高通過頻率的資料區，包括 flexbits。 這可有效地將平面 Alpha 通道的解析度減少為兩個維度的4倍。 轉碼影像的實際維度會維持不變，但影像會遺失 Alpha 通道圖元每個4x4 區塊中的所有詳細資料。 一般來說，只有當 [ImageDataDiscard](#imagedatadiscard) 屬性具有相同的值時，才應該設定這個值。                            |
| 3     | 系統會捨棄「高階」和「低通路」頻率資料格（包括 flexbits）。 這項 ffectively 可減少平面 Alpha 通道的解析度，因為這兩個維度的因數都是16。 轉碼影像的實際維度會維持不變，但影像會在每16x16 巨大區塊的 Alpha 通道圖元中遺失所有詳細資料。 一般來說，只有當 [ImageDataDiscard](#imagedatadiscard) 屬性具有相同的值時，才應該設定這個值。 |
| 4     | 完全捨棄 Alpha 色頻 (Alpha Channel)。 轉碼影像的像素格式會變更，以反映 Alpha 色板的移除。                                                                                                                                                                                                                                                                                                                                |



 

針對包含交錯 Alpha 色板的影像，下列值有效。



| 值 | 描述                                                                                                                                 |
|-------|---------------------------------------------------------------------------------------------------------------------------------------------|
| 4     | 完全捨棄 Alpha 色頻 (Alpha Channel)。 轉碼影像的像素格式會變更，以反映 Alpha 色板的移除。 |



 

針對交錯 Alpha，除非這個屬性設定為4，否則 Alpha 通道會根據 [ImageDataDiscard](#imagedatadiscard) 屬性的值，處理與影像資料相同的處理。

### <a name="alphaquality"></a>AlphaQuality

設定平面 Alpha 通道影像的壓縮品質。



| 資料類型 | VARTYPE     | 範圍 | 預設 |
|-----------|-------------|-------|---------|
| **UCHAR** | **VT \_ UI1** | 1–255 | 1       |



 

當影像具有 Alpha 色板，且 [InterleavedAlpha](#interleavedalpha) 屬性為 **VARIANT \_ FALSE** 時，就會套用此屬性。 值1表示無失真模式。 增加值會產生較高的壓縮比例和較低的影像品質。

### <a name="bitmaptransform"></a>BitmapTransform

指定是否在解碼時旋轉或翻轉影像。



| 資料類型 | VARTYPE     | 範圍                                                                     | 預設                       |
|-----------|-------------|---------------------------------------------------------------------------|-------------------------------|
| **UCHAR** | **VT \_ UI1** | [**WICBitmapTransformOptions**](/windows/desktop/api/Wincodec/ne-wincodec-wicbitmaptransformoptions) | **WICBitmapTransformRotate0** |



 

### <a name="compresseddomaintranscode"></a>CompressedDomainTranscode

啟用或停用壓縮的網域轉碼。



| 資料類型         | VARTYPE      | 預設           |
|-------------------|--------------|-------------------|
| **VARIANT \_ BOOL** | **VT \_ BOOL** | **VARIANT \_ TRUE** |



 

若要停用壓縮的網域作業，請將此屬性設定為 **VARIANT \_ FALSE**。

### <a name="frequencyorder"></a>FrequencyOrder

依頻率順序啟用編碼。 JPEG XR 編碼器的裝置執行可依空間順序組織檔案，以減少編碼期間所需的記憶體。



| 資料類型         | VARTYPE      | 預設           |
|-------------------|--------------|-------------------|
| **VARIANT \_ BOOL** | **VT \_ BOOL** | **VARIANT \_ TRUE** |



 

-   **變異 \_TRUE**：頻率順序。 頻率最低的資料會先出現在檔案中，而影像內容會依其頻率（而非其空間方向）來分組。 依頻率順序組織檔案，可為任何以頻率為基礎的解碼提供最佳效能。
-   **變異 \_FALSE**：空間順序。 空間順序可減少編碼期間所需的記憶體

除非您有使用空間順序的效能或應用程式特定的原因，否則建議使用頻率順序。

### <a name="horizontaltileslices"></a>HorizontalTileSlices

設定水準磚的數目。



| 資料類型  | VARTYPE     | 範圍  | 預設                      |
|------------|-------------|--------|------------------------------|
| **USHORT** | **VT \_ UI2** | 0–4095 |  (影像寬度– 1)  >> 8 |



 

值是水準細分的數目;亦即水準磚的數目–1。

### <a name="ignoreoverlap"></a>IgnoreOverlap

指定編碼器在壓縮的網域轉碼期間處理磚邊界的方式。



| 資料類型         | VARTYPE      | 預設            |
|-------------------|--------------|--------------------|
| **VARIANT \_ BOOL** | **VT \_ BOOL** | **VARIANT \_ FALSE** |



 

只有當 [CompressedDomainTranscode](#compresseddomaintranscode) 屬性設定為 **VARIANT \_ TRUE** ，而且只執行一或多個磚的子領域轉碼時，才會套用此屬性。

區域轉碼的預設作業是擴充要求的區域，以包含重迭區域邊緣所需的周圍圖元。 如果這個屬性設定為 **VARIANT \_ TRUE**，則編解碼器會忽略周圍的圖元，而只會解壓縮選取的磚或磚。 如果來源影像未並排顯示或要求的區域包含部分磚，則會忽略此參數。

### <a name="imagedatadiscard"></a>ImageDataDiscard

設定壓縮的網域轉碼期間要捨棄的映射頻率資料量。



| 資料類型 | VARTYPE     | 範圍 | 預設 |
|-----------|-------------|-------|---------|
| **UCHAR** | **VT \_ UI1** | 0–3   | 0       |



 

只有當 [CompressedDomainTranscode](#compresseddomaintranscode) 屬性設定為 **VARIANT \_ TRUE** 時，才會套用這個屬性; 否則會予以忽略。



| 值 | 描述                                                                                                                                                                                                                                                                                                                                                                                                       |
|-------|-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| 0     | 不捨棄影像頻率資料。                                                                                                                                                                                                                                                                                                                                                                             |
| 1     | Flexbits 會被捨棄。 這可任意減少轉碼影像的品質，而不會變更影像的有效解析度。 檔案大小和品質的確切縮減取決於許多因素，而且無法完全指定。 這個值會傳回針對交錯 Alpha 色板指定的錯誤。                                                                                |
| 2     | 會捨棄高通過頻率的資料區，包括 flexbits。 這可減少轉碼影像的解析度，因為這兩個維度的因數為4。 轉碼影像的實際維度會維持不變，但影像會遺失每個4x4 圖元區塊中的所有詳細資料。 因此，每次解碼轉碼映射時，應據以 >downsampled。                             |
| 3     | 系統會捨棄「高階」和「低通路」頻率資料格（包括 flexbits）。 這可減少轉碼影像的解析度，因為這兩個維度的因數都是16。 轉碼影像的實際維度會維持不變，但影像會在每16x16 巨大區塊的圖元中失去所有詳細資料。 因此，每次解碼轉碼映射時，應據以 >downsampled。 |



 

如果影像包含交錯的 Alpha 色板，除非[AlphaDataDiscard](#alphadatadiscard)屬性設定為4，否則會將[ImageDataDiscard](#imagedatadiscard)的值套用至 Alpha 色板，在此情況下會捨棄 Alpha 色板。

若是平面 Alpha，捨棄的頻率資料是由 [AlphaDataDiscard](#alphadatadiscard) 屬性所控制。

### <a name="imagequality"></a>ImageQuality

設定影像品質。



| 資料類型 | VARTYPE    | 範圍 | 預設 |
|-----------|------------|-------|---------|
| **FLOAT** | **VT \_ R4** | 0–1。0 | 0.9     |



 

層級1.0 提供數學無損的壓縮。

層級0.0 是最低品質設定。

### <a name="interleavedalpha"></a>InterleavedAlpha

指定是否要編碼交錯的 Alpha 或平面 Alpha。



| 資料類型         | VARTYPE      | 預設            |
|-------------------|--------------|--------------------|
| **VARIANT \_ BOOL** | **VT \_ BOOL** | **VARIANT \_ FALSE** |



 

-   **變異 \_TRUE**：交錯的 Alpha。 Alpha 色板資訊會編碼為額外的交錯通道，而且沒有與影像內容通道的相互關聯。 當影像正在串流時，此模式非常適合用來在影像中同時解碼 Alpha。
-   VARIANT \_ FALSE：平面 Alpha。 平面 Alpha 通道會編碼為個別的影像。 影像資料和 Alpha 通道會獨立解碼。 （選擇性）您可以藉由設定 [AlphaQuality](#alphaquality) 屬性來設定 Alpha 色板的品質等級。

只有某些 RGB 像素格式支援交錯 Alpha。 任何定義 Alpha 色板的影像格式都支援平面 Alpha。

### <a name="lossless"></a>Lossless

啟用遺失壓縮。



| 資料類型         | VARTYPE      | 預設        |
|-------------------|--------------|----------------|
| **VARIANT \_ BOOL** | **VT \_ BOOL** | VARIANT \_ FALSE |



 

如果值為 **VARIANT \_ TRUE**，編碼器會使用不失真壓縮。 當設定為 **VARIANT \_ TRUE** 時，此屬性會覆寫 [ImageQuality](#imagequality) 屬性。

### <a name="overlap"></a>重疊

設定重迭篩選的層級。 使用重迭篩選時，會跨區塊和巨大區塊界限套用轉換係數。 這可以減少封鎖構件。



| 資料類型 | VARTYPE     | 範圍 | 預設 |
|-----------|-------------|-------|---------|
| **UCHAR** | **VT \_ UI1** | 0–4   | 1       |



 



| 值 | 描述                                   |
|-------|-----------------------------------------------|
| 0     | 無重迭。                                   |
| 1     | 一個重迭層級，軟平並排。 (預設值。) |
| 2     | 兩個重迭層級，軟平並排。           |
| 3     | 一個重迭層級，硬平圖             |
| 4     | 重迭的兩個層級，硬平圖。           |



 

定義：

-   一個重迭層級：會根據連續的區塊來修改4x4 區塊的編碼值。
-   重迭的兩個層級：套用第一個重迭層級。 此外，會根據鄰近的巨大區塊修改16x16 巨大區塊的編碼值。
-   軟圖格：重迭篩選會套用到磚邊界。
-   硬磚：重迭篩選不會套用到磚邊界。 硬圖格可以沿著磚邊界引進一些視覺構件。

如果設定此屬性，也請將 [UseCodecOptions](#usecodecoptions) 設定為 **VARIANT \_ TRUE**。

### <a name="progressivemode"></a>ProgressiveMode

啟用或停用漸進式編碼。



| 資料類型         | VARTYPE      | 預設            |
|-------------------|--------------|--------------------|
| **VARIANT \_ BOOL** | **VT \_ BOOL** | **VARIANT \_ FALSE** |



 



| 值              | 描述                |
|--------------------|----------------------------|
| **VARIANT \_ TRUE**  | 順序模式 (預設) 。 |
| **VARIANT \_ FALSE** | 漸進模式。          |



 

### <a name="quality"></a>品質

設定壓縮品質。



| 資料類型 | VARTYPE     | 範圍 | 預設 |
|-----------|-------------|-------|---------|
| **UCHAR** | **VT \_ UI1** | 1–255 | 1       |



 

值1表示無失真模式。 增加值會產生較高的壓縮比例和較低的影像品質。

如果設定此屬性，也請將 [UseCodecOptions](#usecodecoptions) 設定為 **VARIANT \_ TRUE**。

### <a name="streamonly"></a>StreamOnly

啟用或停用僅限資料流程模式。



| 資料類型         | VARTYPE      | 預設            |
|-------------------|--------------|--------------------|
| **VARIANT \_ BOOL** | **VT \_ BOOL** | **VARIANT \_ FALSE** |



 



| 值              | 描述                                                            |
|--------------------|------------------------------------------------------------------------|
| **VARIANT \_ TRUE**  | 編碼器會輸出未經處理中繼資料的原始影像資料流程。             |
| **VARIANT \_ FALSE** | 編碼器會輸出容器格式 (影像串流以及中繼資料) 。 |



 

### <a name="subsampling"></a>圖元

設定色度的取樣。 這個屬性只適用于 RGB 影像。



| 資料類型 | VARTYPE     | 範圍 | 預設                                                  |
|-----------|-------------|-------|----------------------------------------------------------|
| **UCHAR** | **VT \_ UI1** | 0–3   | 3如果 [ImageQuality](#imagequality) > 0.8;否則為1 |



 



<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<thead>
<tr class="header">
<th>值</th>
<th>描述</th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td>3</td>
<td>4:4:4 編碼。 保留完整的色度解析度。</td>
</tr>
<tr class="even">
<td>2</td>
<td>4:2:2 編碼。 色度解析度是1/2 的亮度解析度。</td>
</tr>
<tr class="odd">
<td>1</td>
<td>4:2:0 編碼。 色度解析度是1/4 的亮度解析度。</td>
</tr>
<tr class="even">
<td>0</td>
<td>4:0:0 編碼。 捨棄所有的色度值，並只保留亮度。
<blockquote>
[!Note]<br />
不建議使用此模式，因為編解碼器會使用稍微修改的亮度定義來改善效能。 相反地，最好先將影像轉換成單色再進行編碼。
</blockquote>
<br/></td>
</tr>
</tbody>
</table>



 

4:2:2 和4:2:0 會保留亮度詳細資料，同時保有色彩詳細資料的費用。

如果設定此屬性，也請將 [UseCodecOptions](#usecodecoptions) 設定為 **VARIANT \_ TRUE**。

### <a name="usecodecoptions"></a>UseCodecOptions

指定是否使用 [ [品質](#image-quality-settings)]、[重 [迭](#overlap)] 和 [ [取樣](#subsampling) ] 屬性，而非 [一般 [ImageQuality](#imagequality) ] 屬性。



| 資料類型         | VARTYPE      | 預設            |
|-------------------|--------------|--------------------|
| **VARIANT \_ BOOL** | **VT \_ BOOL** | **VARIANT \_ FALSE** |



 

### <a name="verticaltileslices"></a>VerticalTileSlices

設定水準磚的數目。



| 資料類型  | VARTYPE     | 範圍  | 預設                       |
|------------|-------------|--------|-------------------------------|
| **USHORT** | **VT \_ UI2** | 0–4095 |  (影像高度– 1)  >> 8 |



 

值是垂直細分的數目;也就是垂直磚的數目–1。

## <a name="supported-color-formats"></a>支援的色彩格式

如需這些格式的詳細資訊，請參閱 [原生像素格式](-wic-codec-native-pixel-formats.md)。

-   **整數 RGB 格式**
    -   GUID \_ WICPixelFormat24bppRGB
    -   GUID \_ WICPixelFormat24bppBGR
    -   GUID \_ WICPixelFormat32bppBGR
    -   GUID \_ WICPixelFormat48bppRGB
    -   GUID \_ WICPixelFormat32bppBGRA
    -   GUID \_ WICPixelFormat64bppRGBA
    -   GUID \_ WICPixelFormat32bppPBGRA
    -   GUID \_ WICPixelFormat64bppPRGBA
-   **固定點 RGB 格式**
    -   GUID \_ WICPixelFormat48bppRGBFixedPoint
    -   GUID \_ WICPixelFormat64bppRGBFixedPoint
    -   GUID \_ WICPixelFormat96bppRGBFixedPoint
    -   GUID \_ WICPixelFormat128bppRGBFixedPoint
    -   GUID \_ WICPixelFormat128bppRGBAFixedPoint
-   **浮點數 RGB 格式**
    -   GUID \_ WICPixelFormat48bppRGBHalf
    -   GUID \_ WICPixelFormat64bppRGBHalf
    -   GUID \_ WICPixelFormat128bppRGBFloat
    -   GUID \_ WICPixelFormat64bppRGBAFixedPoint
    -   GUID \_ WICPixelFormat64bppRGBAHalf
    -   GUID \_ WICPixelFormat128bppRGBAFloat
    -   GUID \_ WICPixelFormat128bppPRGBAFloat
-   **灰階格式**
    -   GUID \_ WICPixelFormat8bppGray
    -   GUID \_ WICPixelFormat16bppGray
    -   GUID \_ WICPixelFormat16bppGrayFixedPoint
    -   GUID \_ WICPixelFormat16bppGrayHalf
    -   GUID \_ WICPixelFormat32bppGrayFixedPoint
    -   GUID \_ WICPixelFormat32bppGrayFloat
-   **壓縮格式**
    -   GUID \_ WICPixelFormat16bppBGR555
    -   GUID \_ WICPixelFormat16bppBGR565
    -   GUID \_ WICPixelFormat32bppBGR101010
    -   GUID \_ WICPixelFormat32bppRGBE
-   **CMYK 格式**
    -   GUID \_ WICPixelFormat40bppCMYKAlpha
    -   GUID \_ WICPixelFormat64bppCMYK
    -   GUID \_ WICPixelFormat80bppCMYKAlpha
-   **N 通道格式**
    -   GUID \_ WICPixelFormat32bpp4Channels
    -   GUID \_ WICPixelFormat40bpp5Channels
    -   GUID \_ WICPixelFormat48bpp6Channels
    -   GUID \_ WICPixelFormat56bpp7Channels
    -   GUID \_ WICPixelFormat64bpp8Channels
    -   GUID \_ WICPixelFormat32bpp3ChannelsAlpha
    -   GUID \_ WICPixelFormat40bpp4ChannelsAlpha
    -   GUID \_ WICPixelFormat48bpp5ChannelsAlpha
    -   GUID \_ WICPixelFormat56bpp6ChannelsAlpha
    -   GUID \_ WICPixelFormat64bpp7ChannelsAlpha
    -   GUID \_ WICPixelFormat72bpp8ChannelsAlpha
    -   GUID \_ WICPixelFormat48bpp3Channels
    -   GUID \_ WICPixelFormat64bpp4Channels
    -   GUID \_ WICPixelFormat80bpp5Channels
    -   GUID \_ WICPixelFormat96bpp6Channels
    -   GUID \_ WICPixelFormat128bpp8Channels
    -   GUID \_ WICPixelFormat64bpp3ChannelsAlpha
    -   GUID \_ WICPixelFormat80bpp4ChannelsAlpha
    -   GUID \_ WICPixelFormat96bpp5ChannelsAlpha
    -   GUID \_ WICPixelFormat112bpp6ChannelsAlpha
    -   GUID \_ WICPixelFormat128bpp7ChannelsAlpha
    -   GUID \_ WICPixelFormat144bpp8ChannelsAlpha

 

 
