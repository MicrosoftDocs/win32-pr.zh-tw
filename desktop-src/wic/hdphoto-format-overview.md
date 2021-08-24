---
description: 本主題提供可透過 Windows 影像處理元件 (WIC) 取得之原生 HD 相片編解碼器的相關資訊。
ms.assetid: C73752AB-3D6E-4D92-9FDE-CB68B6A9743C
title: HD 相片格式總覽
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 772c295051186069dd7be1a3efa3bfbb4e6ea919b2ab9fbe77ffd52cad1676a1
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/11/2021
ms.locfileid: "119881948"
---
# <a name="hd-photo-format-overview"></a>HD 相片格式總覽

本主題提供可透過 Windows 影像處理元件 (WIC) 取得之原生 HD 相片編解碼器的相關資訊。

> [!IMPORTANT]
>
> HD 相片格式是 JPEG XR 格式的預先標準執行。 JPEG XR 格式已在 Windows 8 中完全實作為。 如需詳細資訊，請參閱 [JPEG XR 編解碼器總覽](jpeg-xr-codec.md) 。

 

本主題包含下列各節。

-   [編解碼器身分識別](#codec-identity)
-   [編碼方式](#encoding)
    -   [編碼器選項](#encoder-options)
-   [解碼](#decoding)
    -   [IWICBitmapSourceTransform 支援](#iwicbitmapsourcetransform-support)

## <a name="codec-identity"></a>編解碼器身分識別

下表提供編解碼器識別資訊。



|   元件            | 描述                                                                     |
|------------------------|---------------------------------------------------------------------------------|
|  (s 的正式名稱)          | HD 相片、Windows 媒體相片                                                   |
| 副檔名 (s)  | wdp                                                                             |
| MIME 類型 (MIME type)              | image/vnd.openxmlformats-officedocument.spreadsheetml.sheet. ms-photo                                                              |
| 檔案簽章 (s)       | 前四個位元組： 0x4949bc00 (版本 0;發行前版本) ，0x4949bc01 (1.0 版)  |



 

下表列出用來識別原生 HD 相片編解碼器元件的 Guid。



| 元件        | 易記名稱            | GUID                                |
|------------------|--------------------------|-------------------------------------|
| 容器格式 | GUID \_ ContainerFormatWmp | 57a37caa-367a-4540-916bf183c5093a4b |
| 解碼器          | CLSID \_ WICWmpDecoder     | a26cec36-234c-4950-ae16e34aace71d0d |
| 編碼器          | CLSID \_ WICWmpEncoder     | ac4ce3cb-e1c1-44cd-82155a1665509ec2 |



 

## <a name="encoding"></a>編碼

WIC 編碼 API 設計成與編解碼器無關，且已啟用 WIC 的編解碼器影像編碼本質上是相同的。 如需使用 WIC API 進行映射編碼的詳細資訊，請參閱 [編碼總覽](-wic-creating-encoder.md)。

### <a name="encoder-options"></a>編碼器選項

已啟用 WIC 的編解碼器在編碼選項層級不同。 編碼器選項反映影像編碼器的功能，而每個原生編解碼器都支援一組這些編碼器選項。 編碼器選項可以是基本的 WIC 支援選項，可供所有 WIC 啟用的程式碼使用 (但不一定支援) 或由影像格式編解碼器所設計的編解碼器專用選項。 為了在編碼過程中管理這些編碼選項，WIC 會使用 [**IPropertyBag2**](/previous-versions/windows/internet-explorer/ie-developer/platform-apis/aa768192(v=vs.85)) 介面。 如需有關使用 **IPropertyBag2** 介面進行 WIC 編碼的詳細資訊，請參閱 [編碼總覽](-wic-creating-encoder.md)。

HD 相片編解碼器會使用基本的 WIC 選項，並提供數個 HD 相片特定的編碼選項。 下表列出原生 HD 相片編解碼器所支援的編碼器選項。

基本 WIC 編碼器選項

| 屬性名稱 | VARTYPE | 值範圍 | 預設值 |
|---------------|---------|-------------|---------------|
| [ImageQuality](#imagequality-option) | VT \_ R4 | 0-1。0 | 0.9 |
| [Lossless](#lossless-option) | VT \_ BOOL | **TRUE**， **FALSE** | **FALSE** |
| [BitmapTransform](#bitmaptransform-option) | VT \_ UI1 | [**WICBitmapTransformOptions**](/windows/desktop/api/Wincodec/ne-wincodec-wicbitmaptransformoptions) |   [**WICBitmapTransformRotate0**](/windows/desktop/api/Wincodec/ne-wincodec-wicbitmaptransformoptions) |

HD 相片特定編碼器選項

| 屬性名稱 | VARTYPE | 值範圍 | 預設值 |
|---------------|---------|-------------|---------------|
| [UseCodecOptions](#usecodecoptions-option) | VT \_ BOOL | **TRUE**， **FALSE** | **FALSE** |
| [品質](#quality-option) | VT \_ UI1 | 1 - 255 | 10 |
| [重疊](#overlap-option) | VT \_ UI1 | 0 - 2 | 1 |
| [圖元](#subsampling-option) | VT \_ UI1 | 0 - 3 | 3如果 ImageQuality > 0.8;否則為 1; |
| [HorizontalTileSlices](#horizontaltileslices-verticaltileslices-options) | VT \_ UI2 | 0 - 4095 |  (影像寬度– 1)  >> 8 |
| [VerticalTileSlices](#horizontaltileslices-verticaltileslices-options) | VT \_ UI2 | 0 - 4095 |  (影像高度– 1)  >> 8 |
| [FrequencyOrder](#frequencyorder-option) | VT \_ BOOL | **TRUE**， **FALSE** | **TRUE** |
| [InterleavedAlpha](#interleavedalpha-option) | VT \_ BOOL | **TRUE**， **FALSE** | **FALSE** |
| [AlphaQuality](#alphaquality-option) | VT \_ UI1 | 1 - 255 | 1 |
| [CompressedDomainTranscode](#compresseddomaintranscode-option) | VT \_ BOOL | **TRUE**， **FALSE** | **TRUE** |
| [ImageDataDiscard](#imagedatadiscard-option) | VT \_ UI1 | 0 - 3 | 0 |
| [AlphaDataDiscard](#alphadatadiscard-option) | VT \_ UI1 | 0 - 4 | 未使用。 |
| [IgnoreOverlap](#ignoreoverlap-option) | VT \_ BOOL | **TRUE**， **FALSE** | **FALSE** |


如果編碼器選項存在於編解碼器不支援的 [**IPropertyBag2**](/previous-versions/windows/internet-explorer/ie-developer/platform-apis/aa768192(v=vs.85)) 選項清單中，則會予以忽略。

### <a name="imagequality-option"></a>ImageQuality 選項

指定所需的影像精確度。 0.0 表示可能的精確度最低，而1.0 指定最高的精確度。 針對 HD 相片影像格式，1.0 值會導致數學不失真的壓縮。

預設值為0.9。

### <a name="compressionquality-option"></a>CompressionQuality 選項

指定所需的壓縮品質。 0.0 表示有效的壓縮架構可用。 一般而言，此架構會產生更快速的編碼，但較大的輸出。 值為1.0 時，可指定最有效率的壓縮架構，這通常會產生較長的編碼，但輸出較小。

HD 相片不支援此編碼器選項。 如果存在於 [**IPropertyBag2**](/previous-versions/windows/internet-explorer/ie-developer/platform-apis/aa768192(v=vs.85)) 參數清單中，則會忽略此值。

### <a name="lossless-option"></a>無損選項

指定是否使用遺失壓縮模式。 針對 HD 相片影像格式，此值會覆寫 [ImageQuality](#imagequality-option) 選項值。

預設值為 **FALSE**。

### <a name="bitmaptransform-option"></a>BitmapTransform 選項

指定影像解碼期間影像的轉換方式。 您必須將此選項設定為其中一個 [**WICBitmapTransformOptions**](/windows/desktop/api/Wincodec/ne-wincodec-wicbitmaptransformoptions) 列舉值。

預設值為 [**WICBitmapTransformOptions：： WICBitmapTransformRotate0**](/windows/desktop/api/Wincodec/ne-wincodec-wicbitmaptransformoptions)。

### <a name="usecodecoptions-option"></a>UseCodecOptions 選項

如果值為 VARIANT \_ ，則為 [品質](#quality-option)、 [重迭](#overlap-option)和次 [取樣](#subsampling-option) 選項，而不是選項值。

預設值為 **FALSE**。

### <a name="quality-option"></a>品質選項

指定影像的壓縮品質。 值為1表示無失真模式。 增加值會產生較高的壓縮比例和較低的影像品質。

預設值是 10。

### <a name="overlap-option"></a>重迭選項

指定重迭處理的層級。

下表列出可用的重迭處理層級。



| 值 | 描述                                                                                                                                                                                 |
|-------|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| 0     | 未啟用重疊處理。                                                                                                                                                           |
| 1     | 已啟用一個重迭處理層級，根據相鄰區塊的值修改4x4 區塊編碼值。                                                                       |
| 2     | 啟用兩個等級的重疊處理。 除了第一個層級處理之外，也會根據相鄰宏區塊的值修改16x16 宏區塊的編碼值。 |



 

預設值為 1。

### <a name="subsampling-option"></a>次取樣選項

指定色度空間中的額外壓縮。 如此一來，您就可以保留亮度詳細資料，同時保有色彩詳細資料的費用。 此選項只適用于 RGB 影像。

下表列出可用的次取樣選項。



| 值 | 描述                                                                                                                                                                                                                                                                                 |
|-------|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| 3     | 4:4:4 編碼會保留完整的色度解析度。                                                                                                                                                                                                                                            |
| 2     | 4:2:2 編碼可將色度解析度減少為1/2 的亮度解析度。                                                                                                                                                                                                                      |
| 1     | 4:2:0 編碼可將色度解析度減少為1/4 的亮度解析度。                                                                                                                                                                                                                      |
| 0     | 4:0:0 編碼會捨棄所有的色度內容，而且只會保留亮度。 由於編解碼器會使用稍微修改的亮度定義來改善效能，因此我們建議您在編碼之前將 RGB 影像轉換成單色，而不是使用這個色度的取樣模式。 |



 

如果 [ImageQuality](#imagequality-option) > 0.8;，預設值為3。否則為1。

### <a name="horizontaltileslices-verticaltileslices-options"></a>HorizontalTileSlices，VerticalTileSlices 選項

請先指定影像的水準和垂直並排圖，然後再執行壓縮編碼，以取得區域解碼的最佳效能。 藉由在編碼期間將影像分割成矩形磚，您就可以將影像的區域解碼，而不需要處理整個壓縮的資料流程。 預設值0不會指定任何細分，因此整個影像會被視為單一磚。 每個參數的值為1時，會建立單一水準和單一垂直分割，將影像有效地分成四個大小相同的磚。 每個參數的最大值4095會將影像分成4096個磚的資料列，每個資料列都有4096個磚。 換句話說，參數值等於水準和垂直磚的數目 (分別) 減1。 磚的寬度或高度絕不能小於16圖元，因此 HD 相片編碼器可能會調整此參數，以維持所需的最小磚大小。 因為每個磚都有相關聯的儲存和處理額外負荷，所以您應該小心選擇這些值來符合特定案例。

[HorizontalTileSlices](/windows)：預設值是 (影像寬度– 1)  >> 8。

[VerticalTileSlices](/windows)：預設值是 (影像高度-1)  >> 8。

### <a name="frequencyorder-option"></a>FrequencyOrder 選項

指定映射必須以頻率順序編碼。 頻率最低的資料會先出現在檔案中，而影像內容會依其頻率（而非其空間方向）來分組。 依頻率順序組織檔案，可為任何以頻率為基礎的解碼提供最佳效能，因此我們建議您這樣做。 HD 相片編碼器的裝置執行可依空間順序組織檔案，以減少編碼期間所需的記憶體使用量。

預設值為 **TRUE** ，建議應用程式和裝置一律使用頻率順序，除非您有使用空間順序的效能或應用程式特定的原因。

### <a name="interleavedalpha-option"></a>InterleavedAlpha 選項

將此選項設定為 **TRUE** ，會指示編解碼器將 Alpha 通道資訊編碼為額外的交錯通道，而不會與影像內容通道產生相互關聯。 當您需要在串流處理案例中使用影像將 Alpha 同時解碼時，此模式非常有用。

將此參數設定為 **FALSE** 會導致平面 Alpha 色板，並以其本身選用的品質值編碼為個別的影像。 您可以使用平面 Alpha 通道，將影像資料和 Alpha 通道分開地解碼。 只有特定 RGB 像素格式支援交錯的 Alpha 通道。 您可以將平面 Alpha 通道與定義 Alpha 色板的任何影像格式產生關聯。

預設值為 **FALSE**。

### <a name="alphaquality-option"></a>AlphaQuality 選項

指定平面 Alpha 通道影像的壓縮品質。 值為1時，會設定不失真模式。 增加值會產生較高的壓縮比例和較低的影像品質。

預設值為 1。

### <a name="compresseddomaintranscode-option"></a>CompressedDomainTranscode 選項

您可以使用 HD 相片執行一些檔案轉換作業，而不需要實際解碼壓縮的資料，並將其重新編碼至目的地檔案。 壓縮的網域作業非常有效率，而且可避免在您將損及重新編碼已壓縮的影像時，通常會發生的任何額外品質損失。

以下是支援的壓縮網域作業：

-   裁剪影像的區域。
-   執行旋轉/翻轉轉換。
-   捨棄頻率資料 (使其可以建立較小的影像檔案。 ) 
-   重新組織空間與頻率順序之間的影像。

HD 相片編碼器會在將 HD 相片解碼編碼為影像來源時，執行壓縮的網域轉碼操作。 根據您選取的編碼選項，編解碼器會盡可能使用壓縮的網域作業。 如果應用程式選擇明確抑制任何壓縮的網域轉碼作業，您應該將 *UseCodecOptions* 選項設定為 **TRUE** ，並將 *CompressedDomainTranscode* 選項設定為 **FALSE**。

當編解碼器執行壓縮的網域作業時，只允許特定的編碼器參數和屬性設定。

-   系統會忽略基本編碼器選項 [ImageQuality](#imagequality-option)、 [CompressionQuality](/windows) 和 [無損](#lossless-option) 。
-   HD 相片特定編碼器選項的 [品質](#quality-option)、重 [迭](#overlap-option)、 [InterleavedAlpha](#interleavedalpha-option) 和 [AlphaQuality](#alphaquality-option) 都會被忽略。
-   如果有的話， [HorizontalTileSlices](/windows) 和 [VerticalTileSlices](/windows) 選項必須設為零。 在壓縮的網域轉碼中，無法變更影像的磚大小。
-   您可以藉由指定適當的 [FrequencyOrdering](/windows) 選項值，在頻率和空間排序之間變更影像組織。
-   您可以根據在 [BitmapTransform](#bitmaptransform-option) 編碼器選項中指定的值來執行基準旋轉和/或水準/垂直翻轉作業。
-   您可以使用 **WriteSource** 編碼器方法的 [**WICRect**](/windows/desktop/api/Wincodec/nf-wincodec-iwicbitmapframeencode-writesource)參數來指定所需的區域，以裁剪影像。
-   您可以藉由在 [ImageDataDiscard](#imagedatadiscard-option) 和/或 [AlphaDataDiscard](#alphadatadiscard-option) 選項中指定適當的值來捨棄影像和/或 Alpha 資料，以減少編碼的檔案大小，並有效減少新映射的解析度。

預設值為 **TRUE** ，建議應用程式和裝置一律使用頻率順序，除非您有特定的效能或應用程式理由使用空間順序。

### <a name="imagedatadiscard-option"></a>ImageDataDiscard 選項

只有當 [CompressedDomainTranscode](#compresseddomaintranscode-option) 選項為 **TRUE** 時，此參數才有效。否則會予以忽略。 [ImageDataDiscard](#imagedatadiscard-option) 指定壓縮的網域轉碼期間要捨棄的影像資料量。 如果影像包含交錯的 Alpha 色板，此資料捨棄也會套用至 Alpha 通道，如本節稍後所述的例外狀況。

允許使用下列值。



| 值 | 描述                                                                                                                                                                                                                                                                                                                                                                                                                  |
|-------|------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| 0     | 不捨棄影像頻率資料。                                                                                                                                                                                                                                                                                                                                                                                        |
| 1     | FlexBits 會遭到捨棄，因此可任意減少轉碼影像的品質，而不會變更影像的有效解析度。 確切的檔案大小縮減或特定品質降低取決於許多因素，而且無法指定或預測。 如果您將它指定為交錯 Alpha 通道，這會 valuereturns 錯誤。                                                    |
| 2     | 高通頻率資料區會被捨棄 (其中也包括 FlexBits) ，可有效地減少轉碼映射的解析度（以四個維度中的4因數為4）。 轉碼影像的實際維度會維持不變，但會失去每個4x4 圖元區塊中的所有詳細資料。 因此，您應該在將轉碼影像解碼時，據以進行下取樣。                            |
| 3     | 高通和低通頻率資料格都會被捨棄 (其中也包含 FlexBits) ，可有效地減少轉碼映射的解析度（在兩個維度中的因數16）。 轉碼影像的實際維度會維持不變，但每個16巨大區塊的圖元都會失去所有詳細資料。 因此，您應該在將轉碼影像解碼時，據以進行下取樣。 |



 

預設值為 0。

### <a name="alphadatadiscard-option"></a>AlphaDataDiscard 選項

只有當 [CompressedDomainTranscode](#compresseddomaintranscode-option) 屬性為 **TRUE** ，且影像包含平面或交錯 Alpha 色板時，此選項才有效。否則會予以忽略。 它會指定壓縮的網域轉碼期間要捨棄的 Alpha 頻率資料量。 平面 Alpha 通道允許下列值。



| 值 | 描述                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                               |
|-------|-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| 0     | 不捨棄影像頻率資料。                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                     |
| 1     | FlexBits 會遭到捨棄，因此可對轉碼影像的平面 Alpha 通道品質進行任意減少，而不需要變更有效的解析度。 確切的檔案大小縮減或特定品質降低取決於許多因素，而且無法指定或預測。                                                                                                                                                                                                                                                |
| 2     | 高通頻率資料區會被捨棄 (其中也包括 FlexBits) ，可有效地減少轉碼圖像平面 Alpha 通道的解析度（在兩個維度中的係數4）。 轉碼影像的實際維度會維持不變，但影像會在每個4x4 圖元區塊中遺失所有的平面 Alpha 通道詳細資料。 因此，每次解碼時，轉碼映射應該會相應縮小取樣。 一般來說，只有當您將 ImageDataDiscard propertyto 設為相同值時，才應該設定這個值。 |
| 3     | 高通和低通頻率資料格都會被捨棄 (其中也包含 FlexBits) ，可有效地減少轉碼映射的解析度（在兩個維度中的因數16）。 轉碼影像的實際維度會維持不變，但影像會在每16x16 巨大區塊的圖元中失去所有詳細資料。 因此，每次解碼時，轉碼映射應該會相應縮小取樣。 一般來說，只有當您將 ImageDataDiscard 屬性設定為相同的值時，才應該設定這個值。               |
| 4     | Alpha 通道會完全捨棄。 轉碼影像的像素格式會變更，以反映 Alpha 色板的移除。                                                                                                                                                                                                                                                                                                                                                                                                               |



 

針對包含交錯 Alpha 通道的影像，除非這個屬性設定為4，否則 Alpha 通道會根據 ImageDataDiscard 屬性的值，與影像資料進行處理。 如果這個屬性設定為4，則會完全捨棄交錯的 Alpha 通道，並據此變更轉碼影像的像素格式。

無預設值。

### <a name="ignoreoverlap-option"></a>IgnoreOverlap 選項

只有當 [CompressedDomainTranscode](#compresseddomaintranscode-option) 屬性為 **TRUE** ，而且只要求一個或多個磚的子領域轉碼時，此選項才有效。 區域的預設作業轉碼 (或解碼) 是擴充要求的區域，以包含重迭的區域邊緣所需的圖元。 當這個參數設定為 **TRUE** 時，會忽略周圍的圖元，而只會解壓縮選取的磚或磚。 同樣地，要求的區域必須完全符合一或多個磚的座標。 如果來源影像未並排顯示，或如果要求的區域指定了任何部分磚，則會忽略此參數。

預設值為 **FALSE**。

## <a name="decoding"></a>解碼

WIC 解碼 API 設計成與編解碼器無關，且已啟用 WIC 的編解碼器影像解碼本質上是相同的。 如需影像解碼的詳細資訊，請參閱 [解碼總覽](-wic-creating-decoder.md)。 如需使用已解碼之影像資料的詳細資訊，請參閱 [點陣圖來源總覽](-wic-bitmapsources.md)。

### <a name="iwicbitmapsourcetransform-support"></a>IWICBitmapSourceTransform 支援

除了所需的介面必須是已啟用 WIC 的編解碼器，原生 HD 相片編碼器也支援 [**IWICBitmapSourceTransform**](/windows/desktop/api/Wincodec/nn-wincodec-iwicbitmapsourcetransform)。 **IWICBitmapSourceTransform** 介面提供用於解碼影像位資料流程的 advanced 選項。 **IWICBitmapSourceTransform** 介面會啟用下列的解碼器選項，而不只是使用 [**IWICBitmapFrameDecode**](/windows/desktop/api/Wincodec/nn-wincodec-iwicbitmapframedecode)傳回完整的映射。

-   解碼影像的矩形子領域。
-   解碼為較低的解析度
-   解碼成不同的像素格式
-   在解碼時執行轉換 (旋轉/翻轉) 

原生 HD 相片編解碼器提供下列 [**IWICBitmapSourceTransform**](/windows/desktop/api/Wincodec/nn-wincodec-iwicbitmapsourcetransform) 介面層級的支援。

### <a name="doessupporttransform"></a>DoesSupportTransform

原生執行支援所有的 [**WICBitmapTransformOptions**](/windows/desktop/api/Wincodec/ne-wincodec-wicbitmaptransformoptions) 轉換。

### <a name="getclosestsize"></a>GetClosestSize

針對小於1/2 的要求，在這兩個維度中，來源影像的維度，HD 相片會傳回下一個最大的整數影像大小，並以二的因數平均整除。 針對所有其他要求的大小，HD 相片會傳回原始影像尺寸。

### <a name="getclosestpixelformat"></a>GetClosestPixelFormat

HD 相片會傳回編碼影像的像素格式。

### <a name="copypixels"></a>CopyPixels

HD 相片接受 [**WICRect**](/windows/desktop/api/Wincodec/ns-wincodec-wicrect) 參數所指定的任何要求區域，並傳回該部分的影像。

*UiWidth* 和 *uiHeight* 參數必須指定 [**GetClosestSize**](/windows/desktop/api/Wincodec/nf-wincodec-iwicbitmapsourcetransform-getclosestsize)函數所傳回的維度。 任何其他值都會傳回錯誤。

*PguidDstFormat* 參數必須指定 [**GetClosestPixelFormat**](/windows/desktop/api/Wincodec/nf-wincodec-iwicbitmapsourcetransform-getclosestpixelformat)函數所傳回的像素格式。 任何其他值都會傳回錯誤。

HD 相片接受 *dstTransform* 參數的任何可允許值。 請注意，此參數的 WIC 所允許的值，與 HD 相片用於轉換元資料標記的值不同。

 

 
