---
description: 如何執行清理
ms.assetid: 3cf56caf-5c6d-4318-811a-c8bdc1959148
title: 如何執行清理
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 9dad1f06cb6abe6a570fd85407028450651e32a1
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/07/2021
ms.locfileid: "104512452"
---
# <a name="how-to-perform-scrubbing"></a><span data-ttu-id="d400b-103">如何執行清理</span><span class="sxs-lookup"><span data-stu-id="d400b-103">How to Perform Scrubbing</span></span>

<span data-ttu-id="d400b-104">您可以藉由與時間的視覺標記法（例如捲軸）進行互動，藉以立即搜尋檔案內的特定點。</span><span class="sxs-lookup"><span data-stu-id="d400b-104">Scrubbing is performed to instantaneously seek to specific points within a file by interacting with a visual representation of time, such as a scrollbar.</span></span> <span data-ttu-id="d400b-105">在媒體基礎中，清除表示搜尋檔案並取得一個更新的畫面格。</span><span class="sxs-lookup"><span data-stu-id="d400b-105">In Media Foundation, scrubbing means seeking on a file and getting one updated frame.</span></span>

<span data-ttu-id="d400b-106">如需有關清除的詳細資訊，請參閱 [關於速率控制](about-rate-control.md)。</span><span class="sxs-lookup"><span data-stu-id="d400b-106">For information about scrubbing, see [About Rate Control](about-rate-control.md).</span></span>

## <a name="to-perform-scrubbing"></a><span data-ttu-id="d400b-107">執行清理</span><span class="sxs-lookup"><span data-stu-id="d400b-107">To perform scrubbing</span></span>

1.  <span data-ttu-id="d400b-108">呼叫 [**MFGetService**](/windows/desktop/api/mfidl/nf-mfidl-mfgetservice)以從 [媒體會話](media-session.md)取得 [**IMFRateControl**](/windows/desktop/api/mfidl/nn-mfidl-imfratecontrol)介面。</span><span class="sxs-lookup"><span data-stu-id="d400b-108">Call [**MFGetService**](/windows/desktop/api/mfidl/nf-mfidl-mfgetservice) to get the [**IMFRateControl**](/windows/desktop/api/mfidl/nn-mfidl-imfratecontrol) interface from the [Media Session](media-session.md).</span></span>
    > [!Note]  
    > <span data-ttu-id="d400b-109">請勿從媒體來源取得 [**IMFRateControl**](/windows/desktop/api/mfidl/nn-mfidl-imfratecontrol) 介面。</span><span class="sxs-lookup"><span data-stu-id="d400b-109">Do not get the [**IMFRateControl**](/windows/desktop/api/mfidl/nn-mfidl-imfratecontrol) interface from the media source.</span></span> <span data-ttu-id="d400b-110">一律從媒體會話取得介面。</span><span class="sxs-lookup"><span data-stu-id="d400b-110">Always get the interface from the Media Session.</span></span>

     

2.  <span data-ttu-id="d400b-111">呼叫 [**IMFRateControl：： SetRate**](/windows/desktop/api/mfidl/nf-mfidl-imfratecontrol-setrate) ，將播放速率設定為零。</span><span class="sxs-lookup"><span data-stu-id="d400b-111">Call [**IMFRateControl::SetRate**](/windows/desktop/api/mfidl/nf-mfidl-imfratecontrol-setrate) to set the playback rate to zero.</span></span> <span data-ttu-id="d400b-112">如需呼叫這個方法的詳細資訊，請參閱 [如何設定媒體會話的播放速度](how-to-set-the-playback-rate-on-the-media-session.md)。</span><span class="sxs-lookup"><span data-stu-id="d400b-112">For more information about calling this method, see [How to Set the Playback Rate on the Media Session](how-to-set-the-playback-rate-on-the-media-session.md).</span></span>
3.  <span data-ttu-id="d400b-113">藉由指定要在 **MFTIME** 類型中搜尋的呈現時間，在 **PROPVARIANT** 中建立搜尋位置。</span><span class="sxs-lookup"><span data-stu-id="d400b-113">Create a seek position in a **PROPVARIANT** by specifying the presentation time to seek to in a **MFTIME** type.</span></span>
4.  <span data-ttu-id="d400b-114">呼叫 [**IMFMediaSession：： start**](/windows/desktop/api/mfidl/nf-mfidl-imfmediasession-start) 以搜尋位置開始播放。</span><span class="sxs-lookup"><span data-stu-id="d400b-114">Call [**IMFMediaSession::Start**](/windows/desktop/api/mfidl/nf-mfidl-imfmediasession-start) with the seek position to start playback.</span></span>
5.  <span data-ttu-id="d400b-115">當清除操作完成時，媒體會話會傳送 [MESessionScrubSampleComplete](mesessionscrubsamplecomplete.md) 事件。</span><span class="sxs-lookup"><span data-stu-id="d400b-115">When the scrub operation is complete, the Media Session sends an [MESessionScrubSampleComplete](mesessionscrubsamplecomplete.md) event.</span></span> <span data-ttu-id="d400b-116">請先等候這個事件，再呼叫另一個清除操作的 [ [**開始**](/windows/desktop/api/mfidl/nf-mfidl-imfmediasession-start) ]。</span><span class="sxs-lookup"><span data-stu-id="d400b-116">Wait for this event before calling [**Start**](/windows/desktop/api/mfidl/nf-mfidl-imfmediasession-start) again for another scrubbing operation.</span></span>

## <a name="example"></a><span data-ttu-id="d400b-117">範例</span><span class="sxs-lookup"><span data-stu-id="d400b-117">Example</span></span>

<span data-ttu-id="d400b-118">下列程式碼範例顯示如何執行清除。</span><span class="sxs-lookup"><span data-stu-id="d400b-118">The following code example shows how to perform scrubbing.</span></span>


```C++
HRESULT SkipToPosition (MFTIME SeekTime, IMFMediaSession *pMediaSession)
{
    PROPVARIANT var;
    PropVariantInit(&var);

    IMFRateControl *pRateControl = NULL;

    // Get the rate control service.
    HRESULT hr = MFGetService(pMediaSession, MF_RATE_CONTROL_SERVICE, IID_PPV_ARGS(&pRateControl));

    // Set the playback rate to zero without thinning.
    if(SUCCEEDED(hr))
    {
        hr = pRateControl ->SetRate( FALSE, 0.0F); 
    }

    // Create the Media Session start position.
    if( SeekTime == PRESENTATION_CURRENT_POSITION )
    {
        var.vt = VT_EMPTY;
    }
    else
    {
        var.vt = VT_I8;
        var.hVal.QuadPart = SeekTime;
    }

    // Start the Media Session.
    if(SUCCEEDED(hr))
    {
        hr = pMediaSession->Start( NULL, &var);
    }

// Clean up.
    SafeRelease(&pRateControl);
    PropVariantClear(&var)
    return hr;
}
```



<span data-ttu-id="d400b-119">成功的清除作業會在所有資料流程接收更新為新的框架，而且清除作業順利完成之後，產生 [MESessionScrubSampleComplete](mesessionscrubsamplecomplete.md) 事件。</span><span class="sxs-lookup"><span data-stu-id="d400b-119">A successful scrubbing operation generates the [MESessionScrubSampleComplete](mesessionscrubsamplecomplete.md) event after all the stream sinks are updated with the new frame and the scrubbing operation completes successfully.</span></span> <span data-ttu-id="d400b-120">清除影片檔案會顯示已 seeked 至，但不會產生音訊輸出的畫面格。</span><span class="sxs-lookup"><span data-stu-id="d400b-120">Scrubbing a video file displays the frame that was seeked to, but does not generate an audio output.</span></span>

<span data-ttu-id="d400b-121">應用程式可以藉由將播放速率設定為零，然後在 [**IMFMediaSession：： Start**](/windows/desktop/api/mfidl/nf-mfidl-imfmediasession-start)的呼叫中將設定為 **VT \_ 空白** 的 **PROPVARIANT** ，來執行框架逐步執行。</span><span class="sxs-lookup"><span data-stu-id="d400b-121">The application can perform frame stepping by setting the playback rate to zero and then passing a **PROPVARIANT** that is set to **VT\_EMPTY** in the call to [**IMFMediaSession::Start**](/windows/desktop/api/mfidl/nf-mfidl-imfmediasession-start).</span></span>

## <a name="related-topics"></a><span data-ttu-id="d400b-122">相關主題</span><span class="sxs-lookup"><span data-stu-id="d400b-122">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="d400b-123">媒體會話</span><span class="sxs-lookup"><span data-stu-id="d400b-123">Media Session</span></span>](media-session.md)
</dt> <dt>

[<span data-ttu-id="d400b-124">速率控制</span><span class="sxs-lookup"><span data-stu-id="d400b-124">Rate Control</span></span>](rate-control.md)
</dt> </dl>

 

 



