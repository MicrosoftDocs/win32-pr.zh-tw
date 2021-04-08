---
description: 如何設定媒體會話的播放率
ms.assetid: 3663b63f-127c-49fc-923a-d05521fe3d35
title: 如何設定媒體會話的播放率
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: deed8bf480bba1bf1e7d86a41a75b8f41f61046b
ms.sourcegitcommit: c16214e53680dc71d1c07111b51f72b82a4512d8
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 03/03/2021
ms.locfileid: "103696202"
---
# <a name="how-to-set-the-playback-rate-on-the-media-session"></a><span data-ttu-id="d1224-103">如何設定媒體會話的播放率</span><span class="sxs-lookup"><span data-stu-id="d1224-103">How to Set the Playback Rate on the Media Session</span></span>

<span data-ttu-id="d1224-104">若要執行向前快轉和倒轉等播放功能，應用程式可能需要變更媒體資料流程的播放速度。</span><span class="sxs-lookup"><span data-stu-id="d1224-104">To implement playback functionality such as fast forward and rewind, applications may need to change the playback rate for a media stream.</span></span> <span data-ttu-id="d1224-105">媒體基礎提供應用程式必須用來動態設定播放速率的速率控制服務。</span><span class="sxs-lookup"><span data-stu-id="d1224-105">Media Foundation provides the rate control service that the applications must use to set the playback rate dynamically.</span></span>

<span data-ttu-id="d1224-106">在設定播放速率之前，應用程式應該檢查媒體來源是否支援速率。</span><span class="sxs-lookup"><span data-stu-id="d1224-106">Before setting the playback rate, an application should check whether the rate is supported by the media source.</span></span> <span data-ttu-id="d1224-107">如需查詢支援費率的詳細資訊，請參閱 [如何判斷支援的費率](how-to-determine-supported-rates.md)。</span><span class="sxs-lookup"><span data-stu-id="d1224-107">For information about querying for supported rates, see [How to Determine Supported Rates](how-to-determine-supported-rates.md).</span></span>

<span data-ttu-id="d1224-108">如需播放速率的詳細資訊，請參閱 [關於速率控制](about-rate-control.md)。</span><span class="sxs-lookup"><span data-stu-id="d1224-108">For information about playback rates, see [About Rate Control](about-rate-control.md).</span></span>

## <a name="to-set-the-playback-rate"></a><span data-ttu-id="d1224-109">設定播放速率</span><span class="sxs-lookup"><span data-stu-id="d1224-109">To set the playback rate</span></span>

1.  <span data-ttu-id="d1224-110">呼叫 [**MFGetService**](/windows/desktop/api/mfidl/nf-mfidl-mfgetservice) 以取得媒體會話的速率控制物件。</span><span class="sxs-lookup"><span data-stu-id="d1224-110">Call [**MFGetService**](/windows/desktop/api/mfidl/nf-mfidl-mfgetservice) to get the rate control object from the Media Session.</span></span>

    <span data-ttu-id="d1224-111">呼叫 [**MFGetService**](/windows/desktop/api/mfidl/nf-mfidl-mfgetservice) 的應用程式必須確保下列各項：</span><span class="sxs-lookup"><span data-stu-id="d1224-111">Applications calling [**MFGetService**](/windows/desktop/api/mfidl/nf-mfidl-mfgetservice) must ensure the following:</span></span>

    -   <span data-ttu-id="d1224-112">*>punkobject* 參數包含已初始化的 [**IMFMediaSession**](/windows/desktop/api/mfidl/nn-mfidl-imfmediasession)介面指標。</span><span class="sxs-lookup"><span data-stu-id="d1224-112">The *punkObject* parameter contains an initialized [**IMFMediaSession**](/windows/desktop/api/mfidl/nn-mfidl-imfmediasession) interface pointer.</span></span>
    -   <span data-ttu-id="d1224-113">在 *ppvObject* 參數中收到的速率控制物件會釋放，以避免記憶體流失。</span><span class="sxs-lookup"><span data-stu-id="d1224-113">The rate control object received in the *ppvObject* parameter is released to avoid memory leaks.</span></span>

2.  <span data-ttu-id="d1224-114">呼叫 [**IMFRateControl：： SetRate**](/windows/desktop/api/mfidl/nf-mfidl-imfratecontrol-setrate) 方法來設定播放速率。</span><span class="sxs-lookup"><span data-stu-id="d1224-114">Call the [**IMFRateControl::SetRate**](/windows/desktop/api/mfidl/nf-mfidl-imfratecontrol-setrate) method to set the playback rate.</span></span> <span data-ttu-id="d1224-115">以非同步方式完成 **SetRate** 之後，應用程式會收到 [MESessionRateChanged](mesessionratechanged.md) 事件。</span><span class="sxs-lookup"><span data-stu-id="d1224-115">After **SetRate** completes asynchronously, the application receives the [MESessionRateChanged](mesessionratechanged.md) event.</span></span>

## <a name="example"></a><span data-ttu-id="d1224-116">範例</span><span class="sxs-lookup"><span data-stu-id="d1224-116">Example</span></span>

<span data-ttu-id="d1224-117">下列程式碼示範如何透過呼叫 [**SetRate**](/windows/desktop/api/mfidl/nf-mfidl-imfclockstatesink-onclocksetrate) 方法來設定播放速率。</span><span class="sxs-lookup"><span data-stu-id="d1224-117">The following code shows how to set the playback rate by calling the [**SetRate**](/windows/desktop/api/mfidl/nf-mfidl-imfclockstatesink-onclocksetrate) method.</span></span>


```C++
///////////////////////////////////////////////////////////////////////
//  Name: SetPlaybackRate
//  Description: 
//      Gets the rate control service from Media Session.
//      Sets the playback rate to the specified rate.
//  Parameter:
//      pMediaSession: [in] Media session object to query.
//      rateRequested: [in] Playback rate to set.
//      bThin: [in] Indicates whether to use thinning.
///////////////////////////////////////////////////////////////////////

HRESULT SetPlaybackRate(
          IMFMediaSession *pMediaSession, 
          float rateRequested, 
          BOOL bThin)
{
    HRESULT hr = S_OK;
    IMFRateControl *pRateControl = NULL;

    // Get the rate control object from the Media Session.
    hr = MFGetService( 
           pMediaSession, 
           MF_RATE_CONTROL_SERVICE, 
           IID_IMFRateControl, 
           (void**) &pRateControl ); 

    // Set the playback rate.
    if(SUCCEEDED(hr))
    {
        hr = pRateControl ->SetRate( bThin, rateRequested); 
    }

    // Clean up.
    SAFE_RELEASE(pRateControl );

    return hr;
}
```



<span data-ttu-id="d1224-118">應用程式必須先停止或暫停，然後才能將負數或零的比率轉換成正面的速率。</span><span class="sxs-lookup"><span data-stu-id="d1224-118">The application must be stopped or paused before it can make a transition from a negative or zero rate to a positive rate.</span></span> <span data-ttu-id="d1224-119">如需這些狀態的詳細資訊，請參閱 [如何控制呈現狀態](how-to-control-presentation-states.md)。</span><span class="sxs-lookup"><span data-stu-id="d1224-119">For information about these states, see [How to Control Presentation States](how-to-control-presentation-states.md).</span></span>

## <a name="related-topics"></a><span data-ttu-id="d1224-120">相關主題</span><span class="sxs-lookup"><span data-stu-id="d1224-120">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="d1224-121">媒體會話</span><span class="sxs-lookup"><span data-stu-id="d1224-121">Media Session</span></span>](media-session.md)
</dt> <dt>

[<span data-ttu-id="d1224-122">速率控制</span><span class="sxs-lookup"><span data-stu-id="d1224-122">Rate Control</span></span>](rate-control.md)
</dt> <dt>

[<span data-ttu-id="d1224-123">搜尋、向前快轉及反向播放</span><span class="sxs-lookup"><span data-stu-id="d1224-123">Seeking, Fast Forward, and Reverse Play</span></span>](seeking--fast-forward--and-reverse-play.md)
</dt> </dl>

 

 



