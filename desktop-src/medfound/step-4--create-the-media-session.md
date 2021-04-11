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
# <a name="step-4-create-the-media-session"></a><span data-ttu-id="4630c-103">步驟4：建立媒體會話</span><span class="sxs-lookup"><span data-stu-id="4630c-103">Step 4: Create the Media Session</span></span>

<span data-ttu-id="4630c-104">本主題是教學課程的步驟4， [說明如何使用媒體基礎來播放媒體](how-to-play-unprotected-media-files.md)檔案。</span><span class="sxs-lookup"><span data-stu-id="4630c-104">This topic is step 4 of the tutorial [How to Play Media Files with Media Foundation](how-to-play-unprotected-media-files.md).</span></span> <span data-ttu-id="4630c-105">完整的程式碼會顯示在「 [媒體會話播放」範例](media-session-playback-example.md)中。</span><span class="sxs-lookup"><span data-stu-id="4630c-105">The complete code is shown in the topic [Media Session Playback Example](media-session-playback-example.md).</span></span>

<span data-ttu-id="4630c-106">會 `CPlayer::CreateSession` 建立媒體會話的新實例。</span><span class="sxs-lookup"><span data-stu-id="4630c-106">The `CPlayer::CreateSession` creates a new instance of the Media Session.</span></span>


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



<span data-ttu-id="4630c-107">這個方法會執行下列步驟：</span><span class="sxs-lookup"><span data-stu-id="4630c-107">This method performs the following steps:</span></span>

1.  <span data-ttu-id="4630c-108">呼叫 `CPlayer::CloseSession` 以關閉任何先前的媒體會話實例。</span><span class="sxs-lookup"><span data-stu-id="4630c-108">Calls `CPlayer::CloseSession` to close any previous instance of the Media Session.</span></span>
2.  <span data-ttu-id="4630c-109">呼叫 [**MFCreateMediaSession**](/windows/desktop/api/mfidl/nf-mfidl-mfcreatemediasession) 來建立媒體會話的新實例。</span><span class="sxs-lookup"><span data-stu-id="4630c-109">Calls [**MFCreateMediaSession**](/windows/desktop/api/mfidl/nf-mfidl-mfcreatemediasession) to create a new instance of the Media Session.</span></span>
3.  <span data-ttu-id="4630c-110">呼叫 [**IMFMediaEventGenerator：： BeginGetEvent**](/windows/desktop/api/mfobjects/nf-mfobjects-imfmediaeventgenerator-begingetevent) 方法，以要求媒體會話中的下一個事件。</span><span class="sxs-lookup"><span data-stu-id="4630c-110">Calls the [**IMFMediaEventGenerator::BeginGetEvent**](/windows/desktop/api/mfobjects/nf-mfobjects-imfmediaeventgenerator-begingetevent) method to request the next event from the Media Session.</span></span> <span data-ttu-id="4630c-111">**BeginGetEvent** 的第一個參數是 **CPlayer** 物件本身的指標，它會 implents [**IMFAsyncCallback**](/windows/desktop/api/mfobjects/nn-mfobjects-imfasynccallback)介面。</span><span class="sxs-lookup"><span data-stu-id="4630c-111">The first parameter to **BeginGetEvent** is a pointer to the **CPlayer** object itself, which implents the [**IMFAsyncCallback**](/windows/desktop/api/mfobjects/nn-mfobjects-imfasynccallback) interface.</span></span>

<span data-ttu-id="4630c-112">事件處理會在步驟5中說明。</span><span class="sxs-lookup"><span data-stu-id="4630c-112">Event handling is described in step 5.</span></span>

<span data-ttu-id="4630c-113">下一 [步：步驟5：處理媒體會話事件](step-5--handle-media-session-events.md)</span><span class="sxs-lookup"><span data-stu-id="4630c-113">Next: [Step 5: Handle Media Session Events](step-5--handle-media-session-events.md)</span></span>

## <a name="related-topics"></a><span data-ttu-id="4630c-114">相關主題</span><span class="sxs-lookup"><span data-stu-id="4630c-114">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="4630c-115">音訊/視訊播放</span><span class="sxs-lookup"><span data-stu-id="4630c-115">Audio/Video Playback</span></span>](audio-video-playback.md)
</dt> <dt>

[<span data-ttu-id="4630c-116">如何使用媒體基礎播放媒體檔案</span><span class="sxs-lookup"><span data-stu-id="4630c-116">How to Play Media Files with Media Foundation</span></span>](how-to-play-unprotected-media-files.md)
</dt> </dl>

 

 



