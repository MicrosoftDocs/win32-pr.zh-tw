---
description: 本主題說明何時及如何使用 h.264/AVC Remux MFT 和的接收。
ms.assetid: 1DD236D9-775B-4417-BC49-BF52A6B3C8AD
title: 何時及如何使用 h.264/AVC Remux MFT 和數量的接收
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: a6ce5b6d63a21e7a9d6b75acd29690cdeaeba5b0105dcf8d45fe0c93e6b768f3
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/11/2021
ms.locfileid: "119357948"
---
# <a name="when-and-how-to-use-h264avc-remux-mft-and-mp4-sink"></a>何時及如何使用 h.264/AVC Remux MFT 和數量的接收

本主題說明何時及如何使用 h.264/AVC Remux MFT 和的接收。

## <a name="when-to-use-h264avc-remux-mft"></a>使用 h.264/AVC Remux MFT 的時機

MPEG-2 檔案格式需要每個壓縮的範例都以正確的順序包含一張具有 NAL 單位的主要圖片。  (請參閱主要圖片的定義和強制 NAL 單位順序，例如7.4.1.2.3 中的區段、 **NAL 單位順序和程式碼圖片以及存取單位的關聯** 性，以及 h.264 AVC 規格。 ) 它也需要每個壓縮的範例都與簡報時間戳記、解碼時間戳記和取樣持續時間相關聯。

在許多情況下，當應用程式需要在 MPEG 4 檔案容器中錄製 h.264/AVC 影片時，壓縮的範例可能無法滿足上述需求。 例如，一個壓縮的範例可能不會包含完整的主要圖片，也可能不會有正確的呈現時間戳記與其相關聯。 以下是一些應用程式範例：

-   將 AVC 串流的基本影片寫入至 MPEG-2 檔案容器中。
-   錄製攝影機在 MPEG 檔案容器中捕捉到 h.264/AVC 基本影片。
-   在 MPEG-2 檔案容器中錄製 h.264/AVC video 會議。
-   串連 MPEG-2 TS 或 AVC 中的兩個 h.264/影片，並以正確的時間戳記寫入 MPEG-2 檔案容器中。
-   Remux h.264/AVC video，從 AVCHD、MPEG-2 TS/PS 檔案格式到 MPEG 4 檔案格式。
-   Trim/AVC video 檔案，但不包含轉碼。

在這種情況下，應用程式必須使用 h.264/AVC remux MFT 來轉換壓縮的範例，這些範例不包含完整的主要圖片，再將它們寫入 MPEG 4 檔案容器中。

## <a name="how-to-use-h264avc-remux-mft-and-mp4-sink"></a>如何使用 h.264/AVC Remux MFT 和的接收器

將來源輸出媒體類型設定為 **MFVideoFormat \_ H264 \_ ES**，這表示每個範例可能不會包含完整的主要圖片。 將配置接收的輸入媒體類型設定為 **MFVideoFormat \_ H264**。 因此，h.264/AVC remux MFT 的輸入媒體類型是 **MFVideoFormat \_ H264 \_ ES** ，而 H.264/AVC remux mft 的輸出媒體類型是 **MFVideoFormat \_ h264**，會自動插入拓撲解析程式。

H.264/AVC remux 會忽略範例持續時間，因為範例不包含完整主要圖片的範例持續時間沒有明確意義。 而是從畫面播放速率計算範例持續時間。 畫面播放速率是從 sequence 參數計算而來。 如果順序參數中沒有此資訊，則會從輸入媒體類型中的參數計算畫面播放速率。 如果無法使用畫面播放速率資訊，則會使用預設的畫面播放速率 29.97 fps。

H.264/AVC remux MFT 會根據畫面播放速率，以線性方式將解碼時間戳記插入每個壓縮圖片 (DTS) 。 H.264/AVC remux MFT 接受輸入範例中的輸入呈現時間戳記 (PT) ，並將它們傳遞給輸出（如果存在的話）。 它會根據畫面播放速率、先前的點和圖片輸出順序來執行 PT 插補， () .DBP AVC 規格的 **4.5.3 上下加減一點流程** 中所指定的已解碼圖片緩衝處理。 H.264/AVC remux MFT 中的每個輸出範例都應該有時間、DTS 和取樣持續時間。 H.264/AVC remux MFT 也會識別位流中的 IDR 圖片，並將其設定為具有 [MFSampleExtension \_ CLEANPOINT](mfsampleextension-cleanpoint-attribute.md)之 MF 屬性的清理點。

目前，h.264/AVC remux MFT 最多可處理64個重新排序的框架。 如果重新排序的框架數目超過64，而且存在長期參考框架，則 h.264/AVC remux MFT 會為該框架插入錯誤的時間，並在錯誤的時間輸出該框架。

若要具現化 h.264/AVC remux MFT，請在 h.264/AVC remux MFT 上設定正確的輸入和輸出媒體類型、設定配置之接收的輸入媒體類型，以及解析拓撲。

下列範例程式碼示範如何初始化 h.264/AVC remux MFT 和的接收。

若為 h.264/AVC remux MFT，


```C++
hr = CoCreateInstance(
            CLSID_CMSH264RemuxMFT,
            NULL,
            CLSCTX_INPROC_SERVER,
            IID_IMFTransform,
            (void**) &pIMFTransform
            );
```



不需要進一步設定。

針對的是，


```C++
IMFByteStream*  pMFBSOutputFile = NULL;
hr = MFCreateFile(
    MF_ACCESSMODE_READWRITE,
    MF_OPENMODE_DELETE_IF_EXIST,
    MF_FILEFLAGS_NONE,
    m_pszOutputFile,
    &pMFBSOutputFile);
if(FAILED(hr))
{
    Log(L"ERROR>> Failed to create output file for MP4 Sink (hr=0x%x)", hr);
    break;
}

hr = MFCreateMPEG4MediaSink(
    pMFBSOutputFile,
    (guidMajorType == MFMediaType_Video) ? pMediaType : NULL,  // pMediaType comes from the output type of the remux MFT
    (guidMajorType == MFMediaType_Audio) ? pMediaType : NULL,
    &m_pMediaSink);
if(FAILED(hr))
{
    Log(L"ERROR>> Failed to create MP4 Sink (hr=0x%x)", hr);
    break;
}
hr = m_pMediaSink->GetStreamSinkByIndex(0, &pStream);
```



## <a name="related-topics"></a>相關主題

<dl> <dt>

[媒體基礎中支援的媒體格式](supported-media-formats-in-media-foundation.md)
</dt> </dl>

 

 



