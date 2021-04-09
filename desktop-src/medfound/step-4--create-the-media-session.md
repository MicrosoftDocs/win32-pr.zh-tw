---
description: 本主題是教學課程的步驟4，說明如何使用媒體基礎來播放媒體檔案。
ms.assetid: fe5e852f-fe0c-439d-b0c5-d32593b587cb
title: 步驟4：建立媒體會話
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 8b4c6c9e36552247cb294a7d0d6996fcc0b8a6ec
ms.sourcegitcommit: c16214e53680dc71d1c07111b51f72b82a4512d8
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 03/03/2021
ms.locfileid: "103945720"
---
# <a name="step-4-create-the-media-session"></a>步驟4：建立媒體會話

本主題是教學課程的步驟4， [說明如何使用媒體基礎來播放媒體](how-to-play-unprotected-media-files.md)檔案。 完整的程式碼會顯示在「 [媒體會話播放」範例](media-session-playback-example.md)中。

會 `CPlayer::CreateSession` 建立媒體會話的新實例。


```C++
//  Create a new instance of the media session.
HRESULT CPlayer::CreateSession()
{
    // Close the old session, if any.
    HRESULT hr = CloseSession();
    if (FAILED(hr))
    {
        goto done;
    }

    assert(m_state == Closed);

    // Create the media session.
    hr = MFCreateMediaSession(NULL, &m_pSession);
    if (FAILED(hr))
    {
        goto done;
    }

    // Start pulling events from the media session
    hr = m_pSession->BeginGetEvent((IMFAsyncCallback*)this, NULL);
    if (FAILED(hr))
    {
        goto done;
    }

    m_state = Ready;

done:
    return hr;
}
```



這個方法會執行下列步驟：

1.  呼叫 `CPlayer::CloseSession` 以關閉任何先前的媒體會話實例。
2.  呼叫 [**MFCreateMediaSession**](/windows/desktop/api/mfidl/nf-mfidl-mfcreatemediasession) 來建立媒體會話的新實例。
3.  呼叫 [**IMFMediaEventGenerator：： BeginGetEvent**](/windows/desktop/api/mfobjects/nf-mfobjects-imfmediaeventgenerator-begingetevent) 方法，以要求媒體會話中的下一個事件。 **BeginGetEvent** 的第一個參數是 **CPlayer** 物件本身的指標，它會 implents [**IMFAsyncCallback**](/windows/desktop/api/mfobjects/nn-mfobjects-imfasynccallback)介面。

事件處理會在步驟5中說明。

下一 [步：步驟5：處理媒體會話事件](step-5--handle-media-session-events.md)

## <a name="related-topics"></a>相關主題

<dl> <dt>

[音訊/視訊播放](audio-video-playback.md)
</dt> <dt>

[如何使用媒體基礎播放媒體檔案](how-to-play-unprotected-media-files.md)
</dt> </dl>

 

 



