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
# <a name="step-7-transport-controls"></a><span data-ttu-id="36829-103">步驟7：傳輸控制項</span><span class="sxs-lookup"><span data-stu-id="36829-103">Step 7: Transport Controls</span></span>

<span data-ttu-id="36829-104">本主題是 [在 DirectShow 中進行音訊/影片播放](audio-video-playback-in-directshow.md)教學課程的步驟7。</span><span class="sxs-lookup"><span data-stu-id="36829-104">This topic is step 7 of the tutorial [Audio/Video Playback in DirectShow](audio-video-playback-in-directshow.md).</span></span> <span data-ttu-id="36829-105">完整的程式碼會顯示在「 [DirectShow 播放」範例](directshow-playback-example.md)中。</span><span class="sxs-lookup"><span data-stu-id="36829-105">The complete code is shown in the topic [DirectShow Playback Example](directshow-playback-example.md).</span></span>

<span data-ttu-id="36829-106">最後一個步驟是新增傳輸控制項 (播放、暫停和停止) 。</span><span class="sxs-lookup"><span data-stu-id="36829-106">The last step is to add transport controls (play, pause, and stop).</span></span> <span data-ttu-id="36829-107">若要播放檔案，請呼叫 [**IMediaControl：： Run**](/windows/desktop/api/Control/nf-control-imediacontrol-run)。</span><span class="sxs-lookup"><span data-stu-id="36829-107">To play the file, call [**IMediaControl::Run**](/windows/desktop/api/Control/nf-control-imediacontrol-run).</span></span>


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



<span data-ttu-id="36829-108">若要暫停，請呼叫 [**IMediaControl：:P ause**](/windows/desktop/api/Control/nf-control-imediacontrol-pause)。</span><span class="sxs-lookup"><span data-stu-id="36829-108">To pause, call [**IMediaControl::Pause**](/windows/desktop/api/Control/nf-control-imediacontrol-pause).</span></span>


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



<span data-ttu-id="36829-109">若要停止，請呼叫 [**IMediaControl：： stop**](/windows/desktop/api/Control/nf-control-imediacontrol-stop)。</span><span class="sxs-lookup"><span data-stu-id="36829-109">To stop, call [**IMediaControl::Stop**](/windows/desktop/api/Control/nf-control-imediacontrol-stop).</span></span>


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



## <a name="related-topics"></a><span data-ttu-id="36829-110">相關主題</span><span class="sxs-lookup"><span data-stu-id="36829-110">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="36829-111">在 DirectShow 播放音訊/影片</span><span class="sxs-lookup"><span data-stu-id="36829-111">Audio/Video Playback in DirectShow</span></span>](audio-video-playback-in-directshow.md)
</dt> <dt>

[<span data-ttu-id="36829-112">DirectShow 播放範例</span><span class="sxs-lookup"><span data-stu-id="36829-112">DirectShow Playback Example</span></span>](directshow-playback-example.md)
</dt> <dt>

[<span data-ttu-id="36829-113">篩選狀態</span><span class="sxs-lookup"><span data-stu-id="36829-113">Filter States</span></span>](filter-states.md)
</dt> </dl>

 

 



