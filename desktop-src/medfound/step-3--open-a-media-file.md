---
description: 本主題是教學課程的步驟3，說明如何使用媒體基礎來播放媒體檔案。
ms.assetid: cc0d2b60-64d7-49f3-844f-97487cab8466
title: 步驟3：開啟媒體檔案
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 15b50f036b84806f96e4349f77a3f06e02e08764
ms.sourcegitcommit: c16214e53680dc71d1c07111b51f72b82a4512d8
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 03/03/2021
ms.locfileid: "104027670"
---
# <a name="step-3-open-a-media-file"></a>步驟3：開啟媒體檔案

本主題是教學課程的步驟3， [說明如何使用媒體基礎來播放媒體](how-to-play-unprotected-media-files.md)檔案。 完整的程式碼會顯示在「 [媒體會話播放」範例](media-session-playback-example.md)中。

`CPlayer::OpenURL`方法會從 URL 開啟媒體檔案。


```C++
//  Open a URL for playback.
HRESULT CPlayer::OpenURL(const WCHAR *sURL)
{
    // 1. Create a new media session.
    // 2. Create the media source.
    // 3. Create the topology.
    // 4. Queue the topology [asynchronous]
    // 5. Start playback [asynchronous - does not happen in this method.]

    IMFTopology *pTopology = NULL;
    IMFPresentationDescriptor* pSourcePD = NULL;

    // Create the media session.
    HRESULT hr = CreateSession();
    if (FAILED(hr))
    {
        goto done;
    }

    // Create the media source.
    hr = CreateMediaSource(sURL, &m_pSource);
    if (FAILED(hr))
    {
        goto done;
    }

    // Create the presentation descriptor for the media source.
    hr = m_pSource->CreatePresentationDescriptor(&pSourcePD);
    if (FAILED(hr))
    {
        goto done;
    }

    // Create a partial topology.
    hr = CreatePlaybackTopology(m_pSource, pSourcePD, m_hwndVideo, &pTopology);
    if (FAILED(hr))
    {
        goto done;
    }

    // Set the topology on the media session.
    hr = m_pSession->SetTopology(0, pTopology);
    if (FAILED(hr))
    {
        goto done;
    }

    m_state = OpenPending;

    // If SetTopology succeeds, the media session will queue an 
    // MESessionTopologySet event.

done:
    if (FAILED(hr))
    {
        m_state = Closed;
    }

    SafeRelease(&pSourcePD);
    SafeRelease(&pTopology);
    return hr;
}
```



這個方法會執行下列步驟：

1.  呼叫 **CPlayer：： CreateSession** 來建立媒體會話的新實例。 請參閱 [步驟4：建立媒體會話](step-4--create-the-media-session.md)。
2.  從 URL 建立媒體來源。 此步驟的完整程式碼會顯示在 [使用來源解析程式](using-the-source-resolver.md)的主題中。
3.  呼叫 [**IMFMediaSource：： CreatePresentationDescriptor**](/windows/desktop/api/mfidl/nf-mfidl-imfmediasource-createpresentationdescriptor) 來取得媒體來源的展示描述項。 展示描述項描述來源檔案中的每個資料流程。
4.  建立播放拓撲。 此步驟的程式碼會顯示在 [建立播放拓撲](creating-playback-topologies.md)的主題中。
5.  呼叫 [**IMFMediaSession：： SetTopology**](/windows/desktop/api/mfidl/nf-mfidl-imfmediasession-settopology) 來設定媒體會話上的拓撲。

[**SetTopology**](/windows/desktop/api/mfidl/nf-mfidl-imfmediasession-settopology)方法會以非同步方式完成。 完成時，會呼叫 CPlayer 物件的 [**IMFAsyncCallback：： Invoke**](/windows/desktop/api/mfobjects/nf-mfobjects-imfasynccallback-invoke) 方法;請參閱 [步驟5：處理媒體會話事件](step-5--handle-media-session-events.md)。

下一 [步：步驟4：建立媒體會話](step-4--create-the-media-session.md)

## <a name="related-topics"></a>相關主題

<dl> <dt>

[音訊/視訊播放](audio-video-playback.md)
</dt> <dt>

[如何使用媒體基礎播放媒體檔案](how-to-play-unprotected-media-files.md)
</dt> </dl>

 

 



