---
description: WDM 影片捕獲篩選
ms.assetid: 97432b99-e89b-4d69-963d-a959f887e580
title: WDM 影片捕獲篩選
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: e4cce63f3883d8688a8f930d68bfe87a52133441
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/08/2021
ms.locfileid: "106975543"
---
# <a name="wdm-video-capture-filter"></a>WDM 影片捕獲篩選

WDM 影片捕獲篩選器會控制使用 Windows Driver Model (WDM) 驅動程式的類比捕獲裝置。

此篩選實際上是核心模式 KsProxy 外掛程式。 它提供適用于 WDM 驅動程式的屬性頁和 COM 介面，可控制類比捕獲裝置 (也稱為類比視頻解碼器) 。 應用程式可以將它視為篩選。 若要將此篩選新增至篩選圖形，請使用 [系統裝置枚舉器](system-device-enumerator.md)。 它會針對每個使用此外掛程式的裝置傳回唯一的標記。 如需詳細資訊，請參閱 [列舉裝置和篩選](enumerating-devices-and-filters.md) 器，以及 [硬體裝置參與篩選圖形的方式](how-hardware-devices-participate-in-the-filter-graph.md)。 如同任何以 KsProxy 為基礎的篩選準則，篩選準則的易記名稱將取決於基礎驅動程式。

並非所有透過 WDM Video Capture 篩選器公開的裝置都會執行下列所有介面。 應用程式可以使用 **QueryInterface** 來判斷特定裝置所支援的介面。



|                                          |                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                        |
|------------------------------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| 篩選介面                        | 裝置的 WDM 驅動程式可能支援下列一或多項： [**IAMAnalogVideoDecoder**](/windows/desktop/api/Strmif/nn-strmif-iamanalogvideodecoder)、 [**IAMCameraControl**](/windows/desktop/api/Strmif/nn-strmif-iamcameracontrol)、 [**IAMDeviceRemoval**](/windows/desktop/api/Strmif/nn-strmif-iamdeviceremoval)、 [**IAMDroppedFrames**](/windows/desktop/api/Strmif/nn-strmif-iamdroppedframes)、 [**IAMExtDevice**](/windows/desktop/api/Strmif/nn-strmif-iamextdevice)、 [**IAMExtTransport**](/windows/desktop/api/Strmif/nn-strmif-iamexttransport)、 [**IAMFilterMiscFlags**](/windows/desktop/api/Strmif/nn-strmif-iamfiltermiscflags)、 [**IAMTimecodeReader**](/windows/desktop/api/Strmif/nn-strmif-iamtimecodereader)、 [**IAMVideoCompression**](/windows/desktop/api/Strmif/nn-strmif-iamvideocompression)、IAMVideoControl、 [**IAMVideoProcAmp**](/windows/desktop/api/Strmif/nn-strmif-iamvideocontrol)、 [**IBaseFilter**](/windows/desktop/api/Strmif/nn-strmif-iamvideoprocamp)、 [](/windows/desktop/api/Strmif/nn-strmif-ibasefilter) [**IKsPropertySet**](ikspropertyset.md)、IMediaSeeking、 [](/windows/desktop/api/Strmif/nn-strmif-imediaseeking) [**IReferenceClock**](/windows/desktop/api/Strmif/nn-strmif-ireferenceclock)、 **ISpecifyPropertyPages**。 |
| 輸入 Pin 媒體類型                    | 驅動程式相依。                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                      |
| 輸入 Pin 介面                     | 驅動程式相依。                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                      |
| 輸出 Pin 媒體類型                   | 驅動程式相依。                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                      |
| 輸出 Pin 介面                    | 驅動程式可能支援下列一或多項：[**IAMBufferNegotiation**](/windows/desktop/api/Strmif/nn-strmif-iambuffernegotiation)、 [**IAMStreamConfig**](/windows/desktop/api/Strmif/nn-strmif-iamstreamconfig)、 [**IAMStreamControl**](/windows/desktop/api/Strmif/nn-strmif-iamstreamcontrol)、 [**IKsPin**](ikspin.md)、 [**IKsPropertySet**](ikspropertyset.md)、 [**IStreamBuilder**](/windows/desktop/api/Strmif/nn-strmif-istreambuilder)、 [**IMediaSeeking**](/windows/desktop/api/Strmif/nn-strmif-imediaseeking)、 [**IPin**](/windows/desktop/api/Strmif/nn-strmif-ipin)、 [**IQualityControl**](/windows/desktop/api/Strmif/nn-strmif-iqualitycontrol)、 **ISpecifyPropertyPages**<br/>                                                                                                                                                                                                                                                                                                                                       |
| 篩選 CLSID                             | 不適用。                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                        |
| 屬性頁 CLSID                      | 驅動程式相依。                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                      |
| 外掛程式可執行檔                       | kswdmcap.ax                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                            |
| [優點](merit.md)                       | 驅動程式相依。                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                      |
| [篩選準則分類](filter-categories.md) | CLSID \_ VideoInputDeviceCategory                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                        |



 

## <a name="related-topics"></a>相關主題

<dl> <dt>

[DirectShow 篩選](directshow-filters.md)
</dt> <dt>

[影片捕獲](video-capture.md)
</dt> </dl>

 

 




