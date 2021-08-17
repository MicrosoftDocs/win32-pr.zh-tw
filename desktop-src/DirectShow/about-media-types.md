---
description: 瞭解 DirectShow 中的媒體類型。 媒體類型是用來描述數位媒體格式的通用且可擴充的方式。
ms.assetid: 9984ba36-4e43-4886-a073-34b330274c9c
title: '關於媒體類型 (DirectShow) '
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 9fa3034581e443472f1b73c0bc42ca7b8b532a18120df3e067b02ad16f37930e
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/11/2021
ms.locfileid: "119074892"
---
# <a name="about-media-types-directshow"></a>關於媒體類型 (DirectShow) 

由於 DirectShow 是模組化的，因此需要一種方式來描述篩選圖形中每個點的資料格式。 例如，請考慮採用 AVI 播放。 資料會以 RIFF 區塊的資料流程形式進入圖形。 這些會剖析成影片和音訊串流。 影片資料流程是由可能壓縮的影片框架所組成。 解碼之後，影片串流是一系列未壓縮的點陣圖。 音訊串流會經歷類似的程式。

媒體類型： DirectShow 如何表示格式

*媒體類型* 是用來描述數位媒體格式的通用且可擴充的方式。 當兩個篩選準則連線時，它們會同意媒體類型。 媒體類型會識別上游篩選器會傳遞至下游篩選器的資料類型，以及資料的實體版面配置。 如果有兩個篩選器無法同意媒體類型，它們將不會連接。

針對某些應用程式，您永遠都不需要擔心媒體類型。 例如，在檔案播放中，DirectShow 會處理所有詳細資料。 其他類型的應用程式可能必須直接使用媒體類型。

媒體類型是使用 [**AM \_ 媒體 \_ 類型**](/windows/win32/api/strmif/ns-strmif-am_media_type) 結構來定義。 此結構包含下列資訊：

-   **主要類型**：主要類型是定義資料整體分類的 GUID。 主要類型包括影片、音訊、未剖析的位元組資料流程、MIDI 資料等等。
-   **子類型**：子類型是另一個 GUID，可進一步定義格式。 例如，在影片主要類型中，有 RGB-24、RGB-32、UYVY 等等的子類型。 在音訊中，有 PCM 音訊、MPEG-2 承載和其他專案。 子類型提供的資訊高於主要類型，但不會定義格式的所有內容。 例如，影片子類型不會定義影像大小或畫面播放速率。 這些是由格式區塊所定義，如下所述。
-   **格式區塊**：格式區塊是資料區塊，會詳細描述此格式。 格式區塊會與 [**AM \_ 媒體 \_ 類型**](/windows/win32/api/strmif/ns-strmif-am_media_type) 結構分開配置。 **AM \_ 媒體 \_ 類型** 結構的 **pbFormat** 成員會指向格式區塊。

    **PbFormat** 成員是輸入的 **void \** _，因為 format 區塊的配置會根據媒體類型而變更。 例如，PCM 音訊使用 [_ *WAVEFORMATEX* *](/previous-versions/dd757713(v=vs.85))結構。 影片使用各種結構，包括 [**VIDEOINFOHEADER**](/previous-versions/windows/desktop/api/amvideo/ns-amvideo-videoinfoheader) 和 [**VIDEOINFOHEADER2**](/previous-versions/windows/desktop/api/dvdmedia/ns-dvdmedia-videoinfoheader2)。 [**AM \_ 媒體 \_ 類型**](/windows/win32/api/strmif/ns-strmif-am_media_type)結構的 **formattype** 成員是 GUID，用來指定要包含在格式區塊中的結構。 每個格式結構都會被指派一個 GUID。 **CbFormat** 成員會指定格式區塊的大小。 在取值 **pbFormat** 指標之前，請務必先檢查這些值。

如果已填入格式區塊，則主要類型和子類型會包含重複的資訊。 不過，主要類型和子類型可提供便利的方式來識別沒有完整格式區塊的格式。 例如，您可以指定泛型24位 RGB 格式 (MEDIASUBTYPE \_ RGB24) ，而不需要知道 [**VIDEOINFOHEADER**](/previous-versions/windows/desktop/api/amvideo/ns-amvideo-videoinfoheader) 結構所需的所有資訊，例如影像大小和畫面播放速率。

例如，篩選器可能會使用下列程式碼來檢查媒體類型：


```C++
HRESULT CheckMediaType(AM_MEDIA_TYPE *pmt)
{
    if (pmt == NULL) return E_POINTER;

    // Check the major type. We're looking for video.
    if (pmt->majortype != MEDIATYPE_Video)
    {
        return VFW_E_INVALIDMEDIATYPE;
    }

    // Check the subtype. We're looking for 24-bit RGB.
    if (pmt->subtype != MEDIASUBTYPE_RGB24)
    {
        return VFW_E_INVALIDMEDIATYPE;
    }

    // Check the format type and the size of the format block.
    if ((pmt->formattype == FORMAT_VideoInfo) &&
         (pmt->cbFormat >= sizeof(VIDEOINFOHEADER) &&
         (pmt->pbFormat != NULL))
    {
        // Now it's safe to coerce the format block pointer to the
        // correct structure, as defined by the formattype GUID.
        VIDEOINFOHEADER *pVIH = (VIDEOINFOHEADER*)pmt->pbFormat;
    
        // Examine pVIH (not shown). If it looks OK, return S_OK.
        return S_OK;
    }

    return VFW_E_INVALIDMEDIATYPE;
}
```



[**AM \_ 媒體 \_ 類型**](/windows/win32/api/strmif/ns-strmif-am_media_type)結構也包含一些選擇性欄位。 這些可用來提供其他資訊，但不需要篩選來使用它們：

-   **lSampleSize**。 如果此欄位不是零，則會定義每個樣本的大小。 如果是零，則表示樣本大小可能會從範例變更為範例。
-   **bFixedSizeSamples**。 如果這個布林值旗標為 **TRUE**，表示 **lSampleSize** 中的值是有效的。 否則，您應該忽略 **lSampleSize**。
-   **bTemporalCompression**。 如果這個布林值旗標為 **FALSE**，則表示所有框架都是主要畫面格。

## <a name="related-topics"></a>相關主題

<dl> <dt>

[篩選 Graph 及其元件](the-filter-graph-and-its-components.md)
</dt> </dl>

 

 
