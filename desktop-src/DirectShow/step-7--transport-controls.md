---
description: 本主題是在 DirectShow 中進行音訊/影片播放教學課程的步驟7。
ms.assetid: 2e542a2d-fc71-41d5-9abd-0dfa70719c0f
title: 步驟7：傳輸控制項
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: b974ccc8c186b1915d2a6564870a0b177073544e
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/08/2021
ms.locfileid: "106979300"
---
# <a name="step-7-transport-controls"></a>步驟7：傳輸控制項

本主題是 [在 DirectShow 中進行音訊/影片播放](audio-video-playback-in-directshow.md)教學課程的步驟7。 完整的程式碼會顯示在「 [DirectShow 播放」範例](directshow-playback-example.md)中。

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

[在 DirectShow 播放音訊/影片](audio-video-playback-in-directshow.md)
</dt> <dt>

[DirectShow 播放範例](directshow-playback-example.md)
</dt> <dt>

[篩選狀態](filter-states.md)
</dt> </dl>

 

 



