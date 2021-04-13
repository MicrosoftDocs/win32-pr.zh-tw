---
description: Microsoft 媒體基礎是在 Windows Vista 中引進，作為 DirectShow 的取代。 當然，Windows 7 仍支援 DirectShow，但鼓勵開發人員在新的數位媒體應用程式中使用媒體基礎。
ms.assetid: c345c0d9-5325-4f73-b9ec-1673ad10e3e4
title: 媒體基礎的新新
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: e0270c28e5aca2a1f0fdad893743a1e8fb630fa5
ms.sourcegitcommit: c16214e53680dc71d1c07111b51f72b82a4512d8
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 03/03/2021
ms.locfileid: "104321523"
---
# <a name="whats-new-for-media-foundation"></a>媒體基礎的新功能

Microsoft 媒體基礎是在 Windows Vista 中引進，作為 DirectShow 的取代。 當然，Windows 7 仍支援 DirectShow，但鼓勵開發人員在新的數位媒體應用程式中使用媒體基礎。

媒體基礎的改進可摘要如下：

-   更好的格式支援，包括 MPEG 4
-   支援捕獲裝置和硬體編解碼器
-   簡化的程式設計模型
-   平臺的改進

## <a name="better-format-support"></a>更好的格式支援

媒體基礎的音訊/影片管線是在 Windows Vista 中執行，但它支援一組有限的格式和檔案容器，這表示某些應用程式需要在較舊的技術（例如 DirectShow）上切換。 在 Windows 7 中，媒體基礎包含下列新的編解碼器、媒體來源和媒體接收器：

-   AAC 解碼器
-   AAC 編碼器
-   AVI/WAVE 檔案來源
-   DV 影片解碼
-   H.264 video 解碼
-   H.264 影片編碼器
-   MJPEG 解碼器
-   MP3 檔案接收\*
-   3GP 檔案來源
-   3GP 檔案接收

> [!Note]  
> MP3 檔案接收不包含 MP3 音訊編碼器。

 

如需詳細資訊，請參閱 [媒體基礎中支援的媒體格式](supported-media-formats-in-media-foundation.md)。

## <a name="hardware-device-support"></a>硬體裝置支援

媒體基礎現在支援音訊/影片管線中的下列硬體裝置類型：

-   UVC 1.1 影片捕獲裝置，例如網路攝影機
-   音訊捕獲裝置
-   硬體編碼器和解碼器
-   硬體視頻處理器，例如色彩空間轉換器

硬體編解碼器可以執行非常快速的影片轉碼。 例如，應用程式可能會將 Windows Media 視訊 (WMV) 檔傳送到只支援3GP 檔案的行動電話。 使用硬體編碼器，應用程式可以在將檔案傳送到裝置之前，在 backgound 中轉碼該檔案。

硬體裝置會以 proxy 物件媒體基礎表示，並在管線中使用，就像以軟體為基礎的元件一樣。

## <a name="simplified-programming-model"></a>簡化的程式設計模型

在 Windows Vista 中，媒體基礎公開一組相對較低層級的 Api。 這些 Api 很有彈性，但對簡單的工作來說太複雜。 Windows 7 新增了高階 Api，可讓您更輕鬆地以 c + + 撰寫媒體應用程式。 這些新的高層級 Api 包括下列各項。



| API                                | 描述                                                                                                                                                                                                                                                                                                    |
|------------------------------------|----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [來源讀取程式](source-reader.md) | 來源讀取器會從媒體檔案提取原始或解碼的資料。 例如，您可以使用來源讀取器從影片檔案取得縮圖點陣圖，或分析音訊檔案中的波形資料。 您也可以使用來源讀取器來取得音訊或影片捕獲裝置的即時資料。 <br/> |
| [接收寫入器](sink-writer.md)     | 接收寫入器可讓您藉由傳入未壓縮或編碼的資料來撰寫媒體檔案。 例如，您可以使用它來重新編碼影片檔案，或從網路攝影機將即時影片帶到檔案。                                                                                                         |
| [轉碼 API](transcode-api.md) | 這項功能支援最常見的音訊/影片編碼案例。<br/>                                                                                                                                                                                                                               |



 

您仍然可以在媒體基礎中使用低層級 Api。 如果您需要更充分掌控音訊/影片管線，您可能會這麼做。

## <a name="platform-improvements"></a>平臺改善

Windows 7 包含了許多基礎媒體基礎平臺 Api 的增強功能。 Advanced applications 可以直接使用這些 Api;其他應用程式可以間接取得權益。 其改善項目包括︰

-   影片管線中的變更，可減少耗電量和視訊記憶體使用量。
-   [DXVA-hd](dxva-hd.md)： Microsoft DirectX Video 加速 High DEFINITION (DXVA-hd) 是硬體加速影片處理的新 API。 DXVA-HD 提供比先前的 DXVA 影片處理 API 更具彈性的組合模型，而且更適合用於高定義的影片格式。
-   用來列舉來源和解碼器的新機制，其中包括使用值和慣用/封鎖清單。 這項功能可提升系統的整體可靠性。 如需詳細資訊，請參閱下列主題：
    -   [**MFTEnumEx**](/windows/desktop/api/mfapi/nf-mfapi-mftenumex)
    -   [**IMFPluginControl**](/windows/desktop/api/mfobjects/nn-mfobjects-imfplugincontrol)
    -   [編解碼器的優點](codec-merit.md)

## <a name="sdk-changes"></a>SDK 變更

-   新的標頭和程式庫檔案： [媒體基礎的標頭和程式庫](media-foundation-headers-and-libraries.md)
-   DLL 和 .lib 變更： [Windows 7 中的程式庫變更](media-foundation-headers-and-libraries.md)
-   新的 SDK 範例：
    -   [音訊剪輯範例](audio-clip-sample.md)
    -   [DXVA-HD 範例](dxva-hd-sample.md)
    -   [MFCaptureD3D 範例](mfcaptured3d-sample.md)
    -   [MFCaptureToFile 範例](mfcapturetofile-sample.md)
    -   [轉碼範例](transcode-sample.md)
    -   [VideoThumbnail 範例](videothumbnail-sample.md)
-   [TopoEdit](topoedit.md)的改善：
    -   支援轉碼。 請參閱 [使用 TopoEdit 建立轉碼拓撲](building-a-transcode-topology-with-topoedit.md)。
    -   支援音訊和影片捕捉。 請參閱 [ [拓撲] 功能表](topology-menu.md)。

## <a name="new-in-windows-8"></a>Windows 8 的新功能

使用 Windows 8 媒體基礎的一些新更新包括：

-   [**IMFCaptureEngine**](/windows/desktop/api/mfcaptureengine/nn-mfcaptureengine-imfcaptureengine)會控制一或多個 capture 裝置。 如需屬性清單，請參閱「 [捕獲引擎」屬性](capture-engine-attributes.md) 。 其他新的 media capture 相關介面為 [**IMFCapturePhotoSink**](/windows/desktop/api/mfcaptureengine/nn-mfcaptureengine-imfcapturephotosink)、 [**IMFCapturePreviewSink**](/windows/desktop/api/mfcaptureengine/nn-mfcaptureengine-imfcapturepreviewsink)、 [**IMFCaptureRecordSink**](/windows/desktop/api/mfcaptureengine/nn-mfcaptureengine-imfcapturerecordsink)、 [**IMFCaptureSink**](/windows/desktop/api/mfcaptureengine/nn-mfcaptureengine-imfcapturesink)和 [**IMFCaptureSource**](/windows/desktop/api/mfcaptureengine/nn-mfcaptureengine-imfcapturesource)。
-   下列媒體基礎類別延伸模組是 Windows 8 的新功能：
    -   [**IMFMediaEngineEx**](/windows/desktop/api/mfmediaengine/nn-mfmediaengine-imfmediaengineex)
    -   [**IMFMediaSourceEx**](/windows/desktop/api/mfidl/nn-mfidl-imfmediasourceex)
    -   [**IMFRealTimeClientEx**](/windows/desktop/api/mfidl/nn-mfidl-imfrealtimeclientex)
    -   [**IMFSinkWriterEx**](/windows/desktop/api/mfreadwrite/nn-mfreadwrite-imfsinkwriterex)
    -   [**IMFSourceReaderEx**](/windows/desktop/api/mfreadwrite/nn-mfreadwrite-imfsourcereaderex)
    -   [**IMFVideoSampleAllocatorEx**](/windows/desktop/api/mfidl/nn-mfidl-imfvideosampleallocatorex)
    -   [**IMFWorkQueueServicesEx**](/windows/desktop/api/mfidl/nn-mfidl-imfworkqueueservicesex)
-   [Direct3D 11 VIDEO API](direct3d-11-video-apis.md) 是 Windows 8 的新。 Windows 8 桌面應用程式仍然可以使用 [direct3d 9 VIDEO api](direct3d-video-apis.md)，但 Windows Store 應用程式必須使用新的 Direct3d 11 video api。 如需有關 Microsoft Direct3D 11 Video 的詳細資訊，請參閱 [媒體基礎中的支援 Direct3D 11 影片解碼](supporting-direct3d-11-video-decoding-in-media-foundation.md)。
-   媒體基礎工作佇列已有更新和改進。 如需詳細資訊，請參閱 [工作佇列和執行緒改善](media-foundation-work-queue-and-threading-improvements.md) 。
-   H.264 [UVC 1.5 攝影機編碼器](camera-encoder-h264-uvc-1-5.md)。
-   如需可搭配 Windows Store 應用程式使用媒體基礎 API 的清單，請參閱 [適用于 Windows store 應用程式的 Win32 和 COM (多媒體) ](media-foundation-headers-and-libraries.md)。
-   媒體基礎不包含在 Windows 8 的 N 和 KN 版本中。 如需詳細資訊，請參閱 [Microsoft Windows Media Feature Pack 的 N 和 KN 版本的所有 Windows 8 版本](https://support.microsoft.com/kb/2703761)。

## <a name="related-topics"></a>相關主題

<dl> <dt>

[關於媒體基礎](about-the-media-foundation-sdk.md)
</dt> <dt>

[Microsoft 媒體基礎](microsoft-media-foundation-sdk.md)
</dt> </dl>

 

 




