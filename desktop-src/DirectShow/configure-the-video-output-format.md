---
description: 設定影片輸出格式
ms.assetid: 1969072e-575e-49b4-88db-4c7e7a5a1c37
title: 設定影片輸出格式
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: d09ac64d7f43e6c39377277544867491a93a6f3e
ms.sourcegitcommit: a47bd86f517de76374e4fff33cfeb613eb259a7e
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/06/2021
ms.locfileid: "104569605"
---
# <a name="configure-the-video-output-format"></a>設定影片輸出格式

> [!Note]  
> 本主題所述的功能已被取代。 若要設定捕獲裝置的輸出格式，應用程式應該在 *pmt* 參數中使用 [**IAMStreamConfig：： >iformatprovider.getformat**](/windows/desktop/api/Strmif/nf-strmif-iamstreamconfig-getformat)所傳回的 [**AM \_ 媒體 \_ 類型**](/windows/win32/api/strmif/ns-strmif-am_media_type)結構。

 

捕獲裝置可支援一系列的輸出格式。 例如，裝置可能支援16位 RGB、32位 RGB 和 YUYV。 在這些格式中，裝置可以支援一系列的框架大小。

在 WDM 裝置中， [**IAMStreamConfig**](/windows/desktop/api/Strmif/nn-strmif-iamstreamconfig) 介面是用來報告裝置支援的格式，以及設定格式。  (舊版 VFW 裝置時，請使用 [影片格式 VFW] 對話方塊（如 [顯示 VFW Capture 對話方塊](display-vfw-capture-dialog-boxes.md)中所述）。 ) **IAMStreamConfig** 介面會公開于 capture 篩選器的捕獲 pin、預覽 pin 或兩者上。 使用 [**ICaptureGraphBuilder2：： FindInterface**](/windows/desktop/api/Strmif/nf-strmif-icapturegraphbuilder2-findinterface) 方法取得介面指標：


```C++
IAMStreamConfig *pConfig = NULL;
hr = pBuild->FindInterface(
    &PIN_CATEGORY_PREVIEW, // Preview pin.
    0,    // Any media type.
    pCap, // Pointer to the capture filter.
    IID_IAMStreamConfig, (void**)&pConfig);
```



裝置具有所支援的媒體類型清單。 針對每個媒體類型，裝置也會提供一組功能。 其中包括適用于該格式的畫面格大小範圍、裝置可以延展或縮減影像的程度，以及畫面播放速率的範圍。

若要取得媒體類型的數目，請呼叫 [**IAMStreamConfig：： GetNumberOfCapabilities**](/windows/desktop/api/Strmif/nf-strmif-iamstreamconfig-getnumberofcapabilities) 方法。 方法會傳回兩個值：

-   媒體類型的數目。
-   保存功能資訊之結構的大小。

大小值是必要的，因為 [**IAMStreamConfig**](/windows/desktop/api/Strmif/nn-strmif-iamstreamconfig) 介面同時用於音訊和影片 (，而且可以擴充至) 的其他媒體類型。 針對影片，這些功能會使用 [**影片串流設定 \_ \_ \_ caps**](/windows/win32/api/strmif/ns-strmif-video_stream_config_caps) 結構來描述，而音訊則使用 [**音訊 \_ 串流 \_ 設定 \_ caps**](/windows/win32/api/strmif/ns-strmif-audio_stream_config_caps) 結構。

若要列舉媒體類型，請使用以零為基底的索引來呼叫 [**IAMStreamConfig：： GetStreamCaps**](/windows/desktop/api/Strmif/nf-strmif-iamstreamconfig-getstreamcaps) 方法。 **GetStreamCaps** 方法會傳回媒體類型和對應的功能結構：


```C++
int iCount = 0, iSize = 0;
hr = pConfig->GetNumberOfCapabilities(&iCount, &iSize);

// Check the size to make sure we pass in the correct structure.
if (iSize == sizeof(VIDEO_STREAM_CONFIG_CAPS))
{
    // Use the video capabilities structure.

    for (int iFormat = 0; iFormat < iCount; iFormat++)
    {
        VIDEO_STREAM_CONFIG_CAPS scc;
        AM_MEDIA_TYPE *pmtConfig;
        hr = pConfig->GetStreamCaps(iFormat, &pmtConfig, (BYTE*)&scc);
        if (SUCCEEDED(hr))
        {
            /* Examine the format, and possibly use it. */

            // Delete the media type when you are done.
            DeleteMediaType(pmtConfig);
        }
}
```



請注意如何為 [**GetStreamCaps**](/windows/desktop/api/Strmif/nf-strmif-iamstreamconfig-getstreamcaps) 方法配置結構。 方法會配置媒體類型結構，而呼叫端會配置功能結構。 將功能結構強制轉型為位元組陣列指標。 當您完成媒體類型之後，請刪除 [**AM \_ 媒體 \_ 類型**](/windows/win32/api/strmif/ns-strmif-am_media_type) 結構以及媒體類型的格式區塊。

您可以將裝置設定為使用 [**GetStreamCaps**](/windows/desktop/api/Strmif/nf-strmif-iamstreamconfig-getstreamcaps) 方法中傳回的格式。 只要以媒體類型呼叫 [**IAMStreamConfig：： SetFormat**](/windows/desktop/api/Strmif/nf-strmif-iamstreamconfig-setformat) ：


```C++
hr = pConfig->SetFormat(pmtConfig);
```



如果未連接 pin，則會在連接時嘗試使用此格式。 如果已連接 pin，則會嘗試使用新的格式重新連接。 在任一種情況下，下游篩選器可能會拒絕此格式。

您也可以先修改媒體類型，再將它傳遞給 [**SetFormat**](/windows/desktop/api/Strmif/nf-strmif-iamstreamconfig-setformat) 方法。 這是 [**影片串流設定 \_ \_ \_ CAPS**](/windows/win32/api/strmif/ns-strmif-video_stream_config_caps) 結構的來源。 它描述所有變更媒體類型的有效方式。 若要使用這項資訊，您必須瞭解該特定媒體類型的詳細資料。

例如，假設 [**GetStreamCaps**](/windows/desktop/api/Strmif/nf-strmif-iamstreamconfig-getstreamcaps) 傳回24位 RGB 格式，框架大小為 320 x 240 圖元。 您可以藉由檢查媒體類型的主要類型、子類型和格式區塊，來取得這項資訊：


```C++
if ((pmtConfig.majortype == MEDIATYPE_Video) &&
    (pmtConfig.subtype == MEDIASUBTYPE_RGB24) &&
    (pmtConfig.formattype == FORMAT_VideoInfo) &&
    (pmtConfig.cbFormat >= sizeof (VIDEOINFOHEADER)) &&
    (pmtConfig.pbFormat != NULL))
{
    VIDEOINFOHEADER *pVih = (VIDEOINFOHEADER*)pmtConfig.pbFormat;
    // pVih contains the detailed format information.
    LONG lWidth = pVih->bmiHeader.biWidth;
    LONG lHeight = pVih->bmiHeader.biHeight;
}
```



[**影片 \_ 串流設定 \_ \_ CAPS**](/windows/win32/api/strmif/ns-strmif-video_stream_config_caps)結構會提供可用於此媒體類型的最小和最大寬度和高度。 它也會提供「步驟」大小，以定義您可以調整寬度或高度的增量。 例如，裝置可能會傳回下列內容：

-   MinOutputSize： 160 x 120
-   MaxOutputSize： 320 x 240
-   OutputGranularityX：8圖元 (水準步驟大小) 
-   OutputGranularityY：8圖元 (垂直步驟大小) 

指定這些數位之後，您可以將寬度設定為範圍 (160、168、176、.。。304、312、320) 和高度至範圍 (120、128、136、.。。104、112、120) 。 下圖說明此程序。

![影片格式大小](images/strmcap3.png)

若要設定新的框架大小，請直接修改 [**GetStreamCaps**](/windows/desktop/api/Strmif/nf-strmif-iamstreamconfig-getstreamcaps)中傳回的 [**AM \_ 媒體 \_ 類型**](/windows/win32/api/strmif/ns-strmif-am_media_type)結構：


```C++
pVih->bmiHeader.biWidth = 160;
pVih->bmiHeader.biHeight = 120;
pVih->bmiHeader.biSizeImage = DIBSIZE(pVih->bmiHeader);
```



然後將媒體類型傳遞給 [**SetFormat**](/windows/desktop/api/Strmif/nf-strmif-iamstreamconfig-setformat) 方法，如先前所述。

[**影片 \_ 串流設定 \_ \_ 帽**](/windows/win32/api/strmif/ns-strmif-video_stream_config_caps)的 **MinFrameInterval** 和 **MaxFrameInterval** 成員是每個影片框架的最小和最大長度，您可以依照下列方式轉譯為畫面播放速率：

`frames per second = 10,000,000 / frame duration`

若要要求特定的畫面播放速率，請在媒體類型中修改 [**VIDEOINFOHEADER**](/previous-versions/windows/desktop/api/amvideo/ns-amvideo-videoinfoheader)或 [**VIDEOINFOHEADER2**](/previous-versions/windows/desktop/api/dvdmedia/ns-dvdmedia-videoinfoheader2)結構中的 **AvgTimePerFrame** 值。 裝置可能不支援最小值與最大值之間的每個可能值，因此驅動程式會使用最接近的值。 若要查看驅動程式實際使用的值，請在呼叫 [**SetFormat**](/windows/desktop/api/Strmif/nf-strmif-iamstreamconfig-setformat)之後呼叫 [**IAMStreamConfig：： >iformatprovider.getformat**](/windows/desktop/api/Strmif/nf-strmif-iamstreamconfig-getformat) 。

某些驅動程式可能會針對 **MaxFrameInterval** 的值報告 **MAXLONGLONG** (0x7FFFFFFFFFFFFFFF) ，這表示沒有最大的持續時間。 不過，您可能會想要在應用程式中強制執行最小畫面播放速率，例如 1 fps。

## <a name="related-topics"></a>相關主題

<dl> <dt>

[關於媒體類型](about-media-types.md)
</dt> <dt>

[設定影片捕獲裝置](configuring-a-video-capture-device.md)
</dt> </dl>

 

 



