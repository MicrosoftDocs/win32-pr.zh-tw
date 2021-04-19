---
description: 如何控制簡報狀態
ms.assetid: 978373ef-b2a4-4035-b889-e28a037c0ab5
title: 如何控制簡報狀態
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: e7a82fe0363a27b9c6f5c054b73ca409835a3dff
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/07/2021
ms.locfileid: "106973695"
---
# <a name="how-to-control-presentation-states"></a><span data-ttu-id="6923d-103">如何控制簡報狀態</span><span class="sxs-lookup"><span data-stu-id="6923d-103">How to Control Presentation States</span></span>

<span data-ttu-id="6923d-104">媒體會話可提供傳輸控制項，例如變更呈現狀態 (播放、暫停和停止播放播放清單的播放案例) 。</span><span class="sxs-lookup"><span data-stu-id="6923d-104">The Media Session provides transport control such as changing presentation states (Play, Pause, and Stop in a playlist-style playback scenario).</span></span> <span data-ttu-id="6923d-105">本主題說明應用程式應該呼叫以變更播放狀態的媒體會話方法。</span><span class="sxs-lookup"><span data-stu-id="6923d-105">This topic describes Media Session methods that an application should call to change the playback state.</span></span>

<span data-ttu-id="6923d-106">下表顯示有效的呈現狀態轉換。</span><span class="sxs-lookup"><span data-stu-id="6923d-106">The following table shows the valid presentation state transitions.</span></span>



| <span data-ttu-id="6923d-107">狀態轉換</span><span class="sxs-lookup"><span data-stu-id="6923d-107">State transition</span></span> | <span data-ttu-id="6923d-108">Description</span><span class="sxs-lookup"><span data-stu-id="6923d-108">Description</span></span>                                                                                |
|------------------|--------------------------------------------------------------------------------------------|
| <span data-ttu-id="6923d-109">播放 > 暫停</span><span class="sxs-lookup"><span data-stu-id="6923d-109">Play -> Pause</span></span> | <span data-ttu-id="6923d-110">呈現頻率會凍結。</span><span class="sxs-lookup"><span data-stu-id="6923d-110">The presentation clock freezes.</span></span>                                                            |
| <span data-ttu-id="6923d-111">Play > 停止</span><span class="sxs-lookup"><span data-stu-id="6923d-111">Play -> Stop</span></span>  | <span data-ttu-id="6923d-112">呈現時鐘已重設。</span><span class="sxs-lookup"><span data-stu-id="6923d-112">The presentation clock is reset.</span></span>                                                           |
| <span data-ttu-id="6923d-113">暫停-> 播放</span><span class="sxs-lookup"><span data-stu-id="6923d-113">Pause -> Play</span></span> | <span data-ttu-id="6923d-114">簡報時鐘會從它在播放期間旁邊的時間繼續進行，以暫停轉換。</span><span class="sxs-lookup"><span data-stu-id="6923d-114">The presentation clock resumes from the time it froze during the Play to Pause transition.</span></span> |
| <span data-ttu-id="6923d-115">暫停-> 停止</span><span class="sxs-lookup"><span data-stu-id="6923d-115">Pause -> Stop</span></span> | <span data-ttu-id="6923d-116">呈現時鐘已重設。</span><span class="sxs-lookup"><span data-stu-id="6923d-116">The presentation clock is reset.</span></span>                                                           |
| <span data-ttu-id="6923d-117">停止 > 播放</span><span class="sxs-lookup"><span data-stu-id="6923d-117">Stop -> Play</span></span>  | <span data-ttu-id="6923d-118">簡報時鐘從簡報的開頭開始。</span><span class="sxs-lookup"><span data-stu-id="6923d-118">The presentation clock starts from the beginning of the presentation.</span></span>                      |
| <span data-ttu-id="6923d-119">停止 > 暫停</span><span class="sxs-lookup"><span data-stu-id="6923d-119">Stop -> Pause</span></span> | <span data-ttu-id="6923d-120">不允許。</span><span class="sxs-lookup"><span data-stu-id="6923d-120">Not allowed.</span></span>                                                                               |



 

## <a name="to-change-presentation-states"></a><span data-ttu-id="6923d-121">變更展示狀態</span><span class="sxs-lookup"><span data-stu-id="6923d-121">To change presentation states</span></span>

-   <span data-ttu-id="6923d-122">呼叫 [**IMFMediaSession：:P ause**](/windows/desktop/api/mfidl/nf-mfidl-imfmediasession-pause) 方法以暫停播放。</span><span class="sxs-lookup"><span data-stu-id="6923d-122">Call the [**IMFMediaSession::Pause**](/windows/desktop/api/mfidl/nf-mfidl-imfmediasession-pause) method to pause playback.</span></span>

    ```C++
    hr = pMediaSession->Pause();
    ```

    

    <span data-ttu-id="6923d-123">在呼叫這個方法之前，應用程式必須呼叫 [**IMFMediaSession：： GetSessionCapabilities**](/windows/desktop/api/mfidl/nf-mfidl-imfmediasession-getsessioncapabilities) 方法，以找出媒體來源是否支援暫停狀態。</span><span class="sxs-lookup"><span data-stu-id="6923d-123">Before calling this method, the application must call the [**IMFMediaSession::GetSessionCapabilities**](/windows/desktop/api/mfidl/nf-mfidl-imfmediasession-getsessioncapabilities) method to discover whether the media source supports the Pause state.</span></span> <span data-ttu-id="6923d-124">如果有的話，這個方法會傳回 *pdwCaps* 參數中的 **MFSESSIONCAP \_ PAUSE** 。</span><span class="sxs-lookup"><span data-stu-id="6923d-124">If it does, this method returns **MFSESSIONCAP\_PAUSE** in the *pdwCaps* parameter.</span></span>

    <span data-ttu-id="6923d-125">暫停：暫時停止媒體會話、簡報時鐘，以及目前簡報的資料流程接收。</span><span class="sxs-lookup"><span data-stu-id="6923d-125">Pause temporarily stops the Media Session, the presentation clock, and the stream sink for the current presentation.</span></span> <span data-ttu-id="6923d-126">在呼叫成功完成之後，應用程式會收到 [MESessionPaused](mesessionpaused.md) 事件。</span><span class="sxs-lookup"><span data-stu-id="6923d-126">After the call completes successfully, the application receives a [MESessionPaused](mesessionpaused.md) event.</span></span>

-   <span data-ttu-id="6923d-127">呼叫 [**IMFMediaSession：： stop**](/windows/desktop/api/mfidl/nf-mfidl-imfmediasession-stop) 方法以停止播放。</span><span class="sxs-lookup"><span data-stu-id="6923d-127">Call the [**IMFMediaSession::Stop**](/windows/desktop/api/mfidl/nf-mfidl-imfmediasession-stop) method to stop playback.</span></span>

    ```C++
    hr = pMediaSession->Stop();
    ```

    

    <span data-ttu-id="6923d-128">這個方法會停止媒體來源、對應的時鐘和串流接收器，藉以停止媒體會話。</span><span class="sxs-lookup"><span data-stu-id="6923d-128">This method stops the Media Session by stopping the media source, the corresponding clocks, and stream sinks.</span></span> <span data-ttu-id="6923d-129">如果媒體會話控制 [Sequencer 來源](sequencer-source.md)，則會由 sequencer 來源停止基礎原生來源。</span><span class="sxs-lookup"><span data-stu-id="6923d-129">If the Media Session is controlling the [Sequencer Source](sequencer-source.md), the underlying native sources are stopped by the sequencer source.</span></span> <span data-ttu-id="6923d-130">停止媒體會話之後，應用程式會收到 [MESessionStopped](mesessionstopped.md) 事件。</span><span class="sxs-lookup"><span data-stu-id="6923d-130">After the Media Session is stopped, the application receives a [MESessionStopped](mesessionstopped.md) event.</span></span>

-   <span data-ttu-id="6923d-131">呼叫 [**IMFMediaSession：： start**](/windows/desktop/api/mfidl/nf-mfidl-imfmediasession-start) 方法以開始播放或搜尋至新位置。</span><span class="sxs-lookup"><span data-stu-id="6923d-131">Call the [**IMFMediaSession::Start**](/windows/desktop/api/mfidl/nf-mfidl-imfmediasession-start) method to start playback or seek to a new position.</span></span>

    ```C++
    hr = pMediaSession->Start(NULL, &var);
    ```

    

    <span data-ttu-id="6923d-132">這個方法會從暫停和停止狀態啟動媒體會話。</span><span class="sxs-lookup"><span data-stu-id="6923d-132">This method starts the Media Session from Pause and Stop states.</span></span> <span data-ttu-id="6923d-133">媒體會話負責設定管線中的資料流程。</span><span class="sxs-lookup"><span data-stu-id="6923d-133">The Media Session is responsible for setting up the data flow in the pipeline.</span></span> <span data-ttu-id="6923d-134">此方法會指示媒體會話啟動簡報時鐘。</span><span class="sxs-lookup"><span data-stu-id="6923d-134">This method instructs the Media Session to start the presentation clock.</span></span> <span data-ttu-id="6923d-135">在這個呼叫之後，媒體會話會將 [MESessionStarted](mesessionstarted.md) 事件傳送至應用程式。</span><span class="sxs-lookup"><span data-stu-id="6923d-135">After this call, Media Session sends a [MESessionStarted](mesessionstarted.md) event to the application.</span></span>

## <a name="related-topics"></a><span data-ttu-id="6923d-136">相關主題</span><span class="sxs-lookup"><span data-stu-id="6923d-136">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="6923d-137">媒體會話</span><span class="sxs-lookup"><span data-stu-id="6923d-137">Media Session</span></span>](media-session.md)
</dt> </dl>

 

 



