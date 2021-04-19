---
description: 影片處理器 MFT 是 Microsoft 媒體基礎轉換 (MFT) ，可執行 colorspace 轉換、影片調整大小、去交錯、畫面播放速率轉換、旋轉、裁剪、空間左方和右視圖打開包裝，以及鏡像。
ms.assetid: 1476995A-9692-4B08-8EF7-7DB6321BEC24
title: '視頻處理器 MFT (Camerauicontrol .h) '
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 53783b42073414e4dc440546698bf295b404dcc0
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 03/22/2021
ms.locfileid: "106995067"
---
# <a name="video-processor-mft"></a>視頻處理器 MFT

影片處理器 MFT 是 Microsoft 媒體基礎轉換 (MFT) ，可執行 colorspace 轉換、影片調整大小、去交錯、畫面播放速率轉換、旋轉、裁剪、空間左方和右視圖打開包裝，以及鏡像。

## <a name="clsid"></a>CLSID

CLSID \_ VideoProcessorMFT

## <a name="interfaces"></a>介面

-   [**IMFRealTimeClientEx**](/windows/desktop/api/mfidl/nn-mfidl-imfrealtimeclientex)
-   [**IMFTransform**](/windows/desktop/api/mftransform/nn-mftransform-imftransform)
-   [**IMFVideoProcessorControl**](/windows/desktop/api/mfidl/nn-mfidl-imfvideoprocessorcontrol)

## <a name="input-formats"></a>輸入格式

-   **MFVideoFormat \_ ARGB32**
-   **MFVideoFormat \_ AYUV**
-   **MFVideoFormat \_ I420**
-   **MFVideoFormat \_ IYUV**
-   **MFVideoFormat \_ NV11**
-   **MFVideoFormat \_ NV12**
-   **MFVideoFormat \_ RGB24**
-   **MFVideoFormat \_ RGB32**
-   **MFVideoFormat \_ RGB555**
-   **MFVideoFormat \_ RGB565**
-   **MFVideoFormat \_ RGB8**
-   **MFVideoFormat \_ UYVY**
-   **MFVideoFormat \_ v410**
-   **MFVideoFormat \_ Y216**
-   **MFVideoFormat \_ Y41P**
-   **MFVideoFormat \_ Y41T**
-   **MFVideoFormat \_ Y42T**
-   **MFVideoFormat \_ YUY2**
-   **MFVideoFormat \_ YV12**
-   **MFVideoFormat \_ YVYU**

## <a name="output-formats"></a>輸出格式

-   **MFVideoFormat \_ ARGB32**
-   **MFVideoFormat \_ AYUV**
-   **MFVideoFormat \_ I420**
-   **MFVideoFormat \_ IYUV**
-   **MFVideoFormat \_ NV12**
-   **MFVideoFormat \_ RGB24**
-   **MFVideoFormat \_ RGB32**
-   **MFVideoFormat \_ RGB555**
-   **MFVideoFormat \_ RGB565**
-   **MFVideoFormat \_ UYVY**
-   **MFVideoFormat \_ Y216**
-   **MFVideoFormat \_ YUY2**
-   **MFVideoFormat \_ YV12**

不支援每個輸入和輸出格式的組合。 若要測試是否支援轉換，請設定輸入類型，然後呼叫 [**IMFTransform：： GetOutputAvailableType**](/windows/desktop/api/mftransform/nf-mftransform-imftransform-getoutputavailabletype)。

如需這些格式的詳細資訊，請參閱 [影片子類型 guid](video-subtype-guids.md)。

## <a name="remarks"></a>備註

您可以使用下列其中一種方式來建立影片處理器的實例：

-   藉由呼叫 [**MFTEnumEx**](/windows/desktop/api/mfapi/nf-mfapi-mftenumex)。 影片處理器會註冊在 [MFT 類別] 的 [ **\_ \_ 視頻 \_ 處理器** ] 類別之下。
-   藉由呼叫 COM 函式， **CoCreateInstance** 將 clsid **clsid \_ VideoProcessorMFT** 傳遞給它。

下列備註適用于在 **視頻處理器 MFT** 中使用來源矩形和目的地矩形。 來源和目的地矩形會以 [**IMFVideoProcessorControl：： SetDestinationRectangle**](/windows/desktop/api/mfidl/nf-mfidl-imfvideoprocessorcontrol-setdestinationrectangle) 和 [**SetSourceRectangle**](/windows/desktop/api/mfidl/nf-mfidl-imfvideoprocessorcontrol-setsourcerectangle) 設定，而某些時間使用 [**IMFMediaEngineEx：： UpdateVideoStream**](/windows/desktop/api/mfmediaengine/nf-mfmediaengine-imfmediaengineex-updatevideostream)。

-   來源矩形應該對齊並舍入，以符合輸入至視頻處理器之畫面格的色彩格式需求。 這點很重要，因為像是420和422的格式有關于可建立和存取之維度和位移的需求。 例如，當輸入格式為420時，{1，0，319，240} (左、上、右、下) 的來源矩形會舍入為 {2，0，320，240}。
-   目的地和來源矩形一律會壓制，以納入其各自的框架中，也就是來源框架和目的地矩形的來源矩形。 這表示負數值沒有意義，它們一律會壓制為0。
-   來源矩形位於目的框架的座標系統中，減去任何目的地矩形。 這表示轉換（例如旋轉）在來源矩形上是「復原」。 因此，您不需要知道影片是旋轉或立體解壓縮。 例如，您可以在影片標記的最上方繪製一個矩形， (相對於影片標籤) 的相對座標，將其正規化 (範圍0到 1) 並將其以來源矩形的形式傳遞，且應該如預期般運作，即使影片正在旋轉也一樣。

影片處理器支援使用 Microsoft Direct3D 11 的 GPU 加速影片處理。 For more information, see [MF\_SA\_D3D11\_AWARE](mf-sa-d3d11-aware.md).

### <a name="stereoscopic-video"></a>Stereoscopic 影片

影片處理器支援3D 影片畫面上的「觀看解壓縮」操作：

如果輸入框架包含兩個在相同框架中封裝的視圖，則影片處理器可以將這些視圖分割成不同的緩衝區，或將基底視圖解壓縮並捨棄第二個視圖。 若要啟用視圖解壓縮，請將 [ [MF \_ 啟用 \_ 3DVIDEO \_ 輸出](mf-enable-3dvideo-output.md) ] 屬性設定為 **MF3DVideoOutputType \_ 身歷聲** 或 **MF3DVideoOutputType \_ 基礎**。

## <a name="requirements"></a>規格需求



| 需求 | 值 |
|-------------------|----------------------------------------------------------------------------------------------|
| 標頭<br/> | <dl> <dt>Camerauicontrol。h</dt> </dl> |



## <a name="see-also"></a>另請參閱

<dl> <dt>

[數位訊號處理器](windowsmediadigitalsignalprocessors.md)
</dt> </dl>

 

 




