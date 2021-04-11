---
description: 如何判斷支援的費率
ms.assetid: 7f2b64e1-1062-4f77-b8e0-62b6d962ae8b
title: 如何判斷支援的費率
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 1f67e9753604f51e85c641e616e8b69944b96618
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/07/2021
ms.locfileid: "104191708"
---
# <a name="how-to-determine-supported-rates"></a><span data-ttu-id="7e512-103">如何判斷支援的費率</span><span class="sxs-lookup"><span data-stu-id="7e512-103">How to Determine Supported Rates</span></span>

<span data-ttu-id="7e512-104">在變更播放速率之前，應用程式應該檢查管線中的物件是否支援播放速率。</span><span class="sxs-lookup"><span data-stu-id="7e512-104">Before changing the playback rate, an application should check whether the playback rate is supported by the objects in the pipeline.</span></span> <span data-ttu-id="7e512-105">[**IMFRateSupport**](/windows/desktop/api/mfidl/nn-mfidl-imfratesupport)介面會提供方法來取得最大的向前和反向速率、最接近所要求速率的支援速率，以及最慢的速率。</span><span class="sxs-lookup"><span data-stu-id="7e512-105">The [**IMFRateSupport**](/windows/desktop/api/mfidl/nn-mfidl-imfratesupport) interface provides methods to get the maximum forward and reverse rates, the supported rate nearest to a requested rate, and the slowest rate.</span></span> <span data-ttu-id="7e512-106">每個速率查詢都可以指定播放方向，以及是否使用 thinning。</span><span class="sxs-lookup"><span data-stu-id="7e512-106">Each of these rate queries can specify the playback direction and whether to use thinning.</span></span> <span data-ttu-id="7e512-107">您可以使用 [**IMFRateControl**](/windows/desktop/api/mfidl/nn-mfidl-imfratecontrol) 介面來查詢確切的播放速率。</span><span class="sxs-lookup"><span data-stu-id="7e512-107">The exact playback rate is queried by using the [**IMFRateControl**](/windows/desktop/api/mfidl/nn-mfidl-imfratecontrol) interface.</span></span>

<span data-ttu-id="7e512-108">如需變更播放速率的詳細資訊，請參閱 [如何設定媒體會話的播放速度](how-to-set-the-playback-rate-on-the-media-session.md)。</span><span class="sxs-lookup"><span data-stu-id="7e512-108">For information about changing playback rates, see [How to Set the Playback Rate on the Media Session](how-to-set-the-playback-rate-on-the-media-session.md).</span></span>

<span data-ttu-id="7e512-109">如需播放速率的一般資訊，請參閱 [關於速率控制](about-rate-control.md)。</span><span class="sxs-lookup"><span data-stu-id="7e512-109">For general information about playback rates, see [About Rate Control](about-rate-control.md).</span></span>

## <a name="to-determine-the-current-playback-rate"></a><span data-ttu-id="7e512-110">判斷目前的播放速率</span><span class="sxs-lookup"><span data-stu-id="7e512-110">To determine the current playback rate</span></span>

1.  <span data-ttu-id="7e512-111">取得媒體會話的速率控制服務。</span><span class="sxs-lookup"><span data-stu-id="7e512-111">Get the rate control service from the Media Session.</span></span>

    ```C++
    IMFRateControl *pRateControl = NULL;
    hr = MFGetService(
           pMediaSession, 
           MF_RATE_CONTROL_SERVICE,
           IID_IMFRateControl, 
           (void**) &pRateControl );
    ```

    

    <span data-ttu-id="7e512-112">在 [**MFGetService**](/windows/desktop/api/mfidl/nf-mfidl-mfgetservice)的 *>punkobject* 參數中傳遞初始化的 [**IMFMediaSession**](/windows/desktop/api/mfidl/nn-mfidl-imfmediasession)介面指標。</span><span class="sxs-lookup"><span data-stu-id="7e512-112">Pass an initialized [**IMFMediaSession**](/windows/desktop/api/mfidl/nn-mfidl-imfmediasession) interface pointer in the *punkObject* parameter of [**MFGetService**](/windows/desktop/api/mfidl/nf-mfidl-mfgetservice).</span></span>

    <span data-ttu-id="7e512-113">應用程式必須透過媒體會話來查詢速率控制服務。</span><span class="sxs-lookup"><span data-stu-id="7e512-113">The application must query for the rate control service through the Media Session.</span></span> <span data-ttu-id="7e512-114">就內部而言，媒體會話會查詢拓撲中的物件。</span><span class="sxs-lookup"><span data-stu-id="7e512-114">Internally, the Media Session queries the objects in the topology.</span></span>

2.  <span data-ttu-id="7e512-115">呼叫 [**IMFRateControl：： GetRate**](/windows/desktop/api/mfidl/nf-mfidl-imfratecontrol-getrate) 方法，以取得目前的播放速率。</span><span class="sxs-lookup"><span data-stu-id="7e512-115">Call the [**IMFRateControl::GetRate**](/windows/desktop/api/mfidl/nf-mfidl-imfratecontrol-getrate) method to get the current playback rate.</span></span>

    ```C++
    hr = pRateControl->GetRate(&bThin, &rate);
    ```

    

    <span data-ttu-id="7e512-116">[**GetRate**](/windows/desktop/api/mfidl/nf-mfidl-imfratecontrol-getrate)的 *pfThin* 參數會接收 **BOOL** 值，指出資料流程目前是否正在 thinned。</span><span class="sxs-lookup"><span data-stu-id="7e512-116">The *pfThin* parameter of [**GetRate**](/windows/desktop/api/mfidl/nf-mfidl-imfratecontrol-getrate) receives a **BOOL** value that indicates whether the stream is currently being thinned.</span></span> <span data-ttu-id="7e512-117">如果應用程式不想查詢資料流程的 thinning 支援，則必須傳遞 **Null** 。</span><span class="sxs-lookup"><span data-stu-id="7e512-117">The application must pass **NULL** if it does not want to query thinning support for the stream.</span></span> <span data-ttu-id="7e512-118">*PflRate* 參數會接收目前的播放速率。</span><span class="sxs-lookup"><span data-stu-id="7e512-118">The *pflRate* parameter receives the current playback rate.</span></span>

## <a name="to-determine-the-nearest-supported-rate"></a><span data-ttu-id="7e512-119">判斷最接近的支援速率</span><span class="sxs-lookup"><span data-stu-id="7e512-119">To determine the nearest supported rate</span></span>

1.  <span data-ttu-id="7e512-120">取得媒體會話的費率支援服務。</span><span class="sxs-lookup"><span data-stu-id="7e512-120">Get the rate support service from the Media Session.</span></span>

    ```C++
    IMFRateSupport *pRateSupport = NULL;
    hr = MFGetService(
           pMediaSession, 
           MF_RATE_CONTROL_SERVICE,
           IID_IMFRateSupport, 
           (void**) &pRateSupport );
    ```

    

    <span data-ttu-id="7e512-121">在 [**MFGetService**](/windows/desktop/api/mfidl/nf-mfidl-mfgetservice)的 *>punkobject* 參數中傳遞初始化的 [**IMFMediaSession**](/windows/desktop/api/mfidl/nn-mfidl-imfmediasession)介面指標。</span><span class="sxs-lookup"><span data-stu-id="7e512-121">Pass an initialized [**IMFMediaSession**](/windows/desktop/api/mfidl/nn-mfidl-imfmediasession) interface pointer in the *punkObject* parameter of [**MFGetService**](/windows/desktop/api/mfidl/nf-mfidl-mfgetservice).</span></span>

2.  <span data-ttu-id="7e512-122">呼叫 [**IMFRateSupport：： IsRateSupported**](/windows/desktop/api/mfidl/nf-mfidl-imfratesupport-isratesupported) 方法，以取得最接近所要求播放速率的支援速率。</span><span class="sxs-lookup"><span data-stu-id="7e512-122">Call the [**IMFRateSupport::IsRateSupported**](/windows/desktop/api/mfidl/nf-mfidl-imfratesupport-isratesupported) method to retrieve the supported rate nearest to a requested playback rate.</span></span>

    ```C++
    float rateRequested = 4.0;
    float actualRate = 0;
    hr = pRateSupport->IsRateSupported(
           TRUE, 
           rateRequested, 
           &actualRate );
    ```

    

    <span data-ttu-id="7e512-123">此範例會查詢 thinning 是否支援播放速率4.0。</span><span class="sxs-lookup"><span data-stu-id="7e512-123">The example queries whether a playback rate of 4.0 is supported with thinning.</span></span> <span data-ttu-id="7e512-124">這是藉由在 [**IsRateSupported**](/windows/desktop/api/mfidl/nf-mfidl-imfratesupport-isratesupported)的 *fThin* 參數中傳遞 **TRUE** 來表示。</span><span class="sxs-lookup"><span data-stu-id="7e512-124">This is indicated by passing **TRUE** in the *fThin* parameter of [**IsRateSupported**](/windows/desktop/api/mfidl/nf-mfidl-imfratesupport-isratesupported).</span></span> <span data-ttu-id="7e512-125">如果支援此速率， *actualRate* 會包含播放速率4.0，而呼叫會成功，且傳回值為 \_ [正常]。</span><span class="sxs-lookup"><span data-stu-id="7e512-125">If this rate is supported, *actualRate* contains the playback rate of 4.0, and the call succeeds with a return value of S\_OK.</span></span> <span data-ttu-id="7e512-126">如果不支援確切的播放速率，則會在 *actualRate* 中收到最接近的支援速率。</span><span class="sxs-lookup"><span data-stu-id="7e512-126">If the exact playback rate is not supported, the nearest supported rate is received in *actualRate*.</span></span> <span data-ttu-id="7e512-127">如果速率不受支援，而且沒有最接近的播放速率，則呼叫會傳回適當的錯誤碼。</span><span class="sxs-lookup"><span data-stu-id="7e512-127">If the rate is not supported and there is no available nearest playback rate, the call returns an appropriate error code.</span></span>

    <span data-ttu-id="7e512-128">這些值可能會隨著載入的管線元件而變更。</span><span class="sxs-lookup"><span data-stu-id="7e512-128">These values can change depending on which pipeline components are loaded.</span></span> <span data-ttu-id="7e512-129">因此，您應該在每次載入新的 topololgy 時，重新查詢這些值。</span><span class="sxs-lookup"><span data-stu-id="7e512-129">Therefore, you should query the values again whenever you load a new topololgy.</span></span>

    <span data-ttu-id="7e512-130">如果不支援所需的播放率，有一個選項是個別查詢拓撲中的每個物件，以找出特定的元件是否不支援費率。</span><span class="sxs-lookup"><span data-stu-id="7e512-130">If the desired playback rate is not supported, one option is to query each object in the topology individually, to find out if a particular component does not support the rate.</span></span> <span data-ttu-id="7e512-131">您可以在沒有此元件的情況下重建拓撲，然後以所需的速率進行播放。</span><span class="sxs-lookup"><span data-stu-id="7e512-131">You might be able to rebuild the topology without this component and then play at the desired rate.</span></span> <span data-ttu-id="7e512-132">例如，如果音訊轉譯器以外的每個元件都支援指定的速率，您就可以重建沒有音訊分支的拓撲，並以所需的速率來播放（沒有音訊）。</span><span class="sxs-lookup"><span data-stu-id="7e512-132">For example, if every component except the audio renderer supports a given rate, you could rebuild the topology without the audio branch and play at the desired rate without audio.</span></span>

## <a name="to-determine-the-slowest-supported-rate"></a><span data-ttu-id="7e512-133">判斷最慢的支援速率</span><span class="sxs-lookup"><span data-stu-id="7e512-133">To determine the slowest supported rate</span></span>

1.  <span data-ttu-id="7e512-134">取得媒體會話的費率支援服務。</span><span class="sxs-lookup"><span data-stu-id="7e512-134">Get the rate support service from the Media Session.</span></span>

    ```C++
    IMFRateSupport *pRateSupport = NULL;
    hr = MFGetService(
           pMediaSession, 
           MF_RATE_CONTROL_SERVICE,
           IID_IMFRateSupport, 
           (void**) &pRateSupport );
    ```

    

    <span data-ttu-id="7e512-135">在 [**MFGetService**](/windows/desktop/api/mfidl/nf-mfidl-mfgetservice)的 *>punkobject* 參數中傳遞初始化的 [**IMFMediaSession**](/windows/desktop/api/mfidl/nn-mfidl-imfmediasession)介面指標。</span><span class="sxs-lookup"><span data-stu-id="7e512-135">Pass an initialized [**IMFMediaSession**](/windows/desktop/api/mfidl/nn-mfidl-imfmediasession) interface pointer in the *punkObject* parameter of [**MFGetService**](/windows/desktop/api/mfidl/nf-mfidl-mfgetservice).</span></span>

2.  <span data-ttu-id="7e512-136">呼叫 [**IMFRateSupport：： GetSlowestRate**](/windows/desktop/api/mfidl/nf-mfidl-imfratesupport-getslowestrate) 方法，以取得最慢的支援速率。</span><span class="sxs-lookup"><span data-stu-id="7e512-136">Call the [**IMFRateSupport::GetSlowestRate**](/windows/desktop/api/mfidl/nf-mfidl-imfratesupport-getslowestrate) method to retrieve the slowest supported rate.</span></span>

    ```C++
    float slowestRate = 0;
    hr = pRateSupport->GetSlowestRate(
           MFRATE_REVERSE, 
           TRUE, 
           &slowestRate);
    ```

    

    <span data-ttu-id="7e512-137">此範例會使用 thinning 來查詢最慢的反向播放速率。</span><span class="sxs-lookup"><span data-stu-id="7e512-137">The example queries for the slowest reverse playback rate with thinning.</span></span> <span data-ttu-id="7e512-138">[**GetSlowestRate**](/windows/desktop/api/mfidl/nf-mfidl-imfratesupport-getslowestrate)的 *slowestRate* 參數中會收到下限速率。</span><span class="sxs-lookup"><span data-stu-id="7e512-138">The lower bound rate is received in *slowestRate* parameter of [**GetSlowestRate**](/windows/desktop/api/mfidl/nf-mfidl-imfratesupport-getslowestrate).</span></span>

    <span data-ttu-id="7e512-139">如果不支援反向播放或 thinning，呼叫會傳回適當的錯誤碼。</span><span class="sxs-lookup"><span data-stu-id="7e512-139">If reverse playback or thinning is not supported, the call returns an appropriate error code.</span></span>

## <a name="related-topics"></a><span data-ttu-id="7e512-140">相關主題</span><span class="sxs-lookup"><span data-stu-id="7e512-140">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="7e512-141">媒體會話</span><span class="sxs-lookup"><span data-stu-id="7e512-141">Media Session</span></span>](media-session.md)
</dt> <dt>

[<span data-ttu-id="7e512-142">速率控制</span><span class="sxs-lookup"><span data-stu-id="7e512-142">Rate Control</span></span>](rate-control.md)
</dt> <dt>

[<span data-ttu-id="7e512-143">搜尋、向前快轉及反向播放</span><span class="sxs-lookup"><span data-stu-id="7e512-143">Seeking, Fast Forward, and Reverse Play</span></span>](seeking--fast-forward--and-reverse-play.md)
</dt> </dl>

 

 



