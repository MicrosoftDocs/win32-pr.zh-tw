---
description: 本主題是 DirectShow 中音訊/影片播放教學課程的步驟7。
ms.assetid: 2e542a2d-fc71-41d5-9abd-0dfa70719c0f
title: 步驟7：傳輸控制項
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: e8253efab566f5dc14a0d0210a26e84cb0a50113389d54b7a871d818a17296ae
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/11/2021
ms.locfileid: "119072412"
---
# <a name="step-7-transport-controls"></a>步驟7：傳輸控制項

本主題是[DirectShow 中音訊/影片播放](audio-video-playback-in-directshow.md)教學課程的步驟7。 完整的程式碼會顯示在[DirectShow 播放範例](directshow-playback-example.md)的主題中。

最後一個步驟是新增傳輸控制項 (播放、暫停和停止) 。 若要播放檔案，請呼叫 [**IMediaControl：： Run**](/windows/desktop/api/Control/nf-control-imediacontrol-run)。


```C++
HRESULT DShowPlayer::Play()
{
    if (m_state != STATE_PAUSED && m_state != STATE_STOPPED)
    {
        return VFW_E_WRONG_STATE;
    }

    HRESULT hr = m_pControl->Run();
    if (SUCCEEDED(hr))
    {
        m_state = STATE_RUNNING;
    }
    return hr;
}
```



若要暫停，請呼叫 [**IMediaControl：:P ause**](/windows/desktop/api/Control/nf-control-imediacontrol-pause)。


```C++
HRESULT DShowPlayer::Pause()
{
    if (m_state != STATE_RUNNING)
    {
        return VFW_E_WRONG_STATE;
    }

    HRESULT hr = m_pControl->Pause();
    if (SUCCEEDED(hr))
    {
        m_state = STATE_PAUSED;
    }
    return hr;
}
```



若要停止，請呼叫 [**IMediaControl：： stop**](/windows/desktop/api/Control/nf-control-imediacontrol-stop)。


```C++
HRESULT DShowPlayer::Stop()
{
    if (m_state != STATE_RUNNING && m_state != STATE_PAUSED)
    {
        return VFW_E_WRONG_STATE;
    }

    HRESULT hr = m_pControl->Stop();
    if (SUCCEEDED(hr))
    {
        m_state = STATE_STOPPED;
    }
    return hr;
}
```



## <a name="related-topics"></a>相關主題

<dl> <dt>

[DirectShow 中的音訊/影片播放](audio-video-playback-in-directshow.md)
</dt> <dt>

[DirectShow播放範例](directshow-playback-example.md)
</dt> <dt>

[篩選狀態](filter-states.md)
</dt> </dl>

 

 



