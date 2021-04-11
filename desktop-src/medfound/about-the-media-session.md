---
description: 關於媒體會話
ms.assetid: 09f50b11-0e0a-42b6-a7bf-bb0135343351
title: 關於媒體會話
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: dc490e63f623fb3c2d5efde5a80f1988566f9345
ms.sourcegitcommit: c16214e53680dc71d1c07111b51f72b82a4512d8
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 03/03/2021
ms.locfileid: "103945590"
---
# <a name="about-the-media-session"></a><span data-ttu-id="23101-103">關於媒體會話</span><span class="sxs-lookup"><span data-stu-id="23101-103">About the Media Session</span></span>

<span data-ttu-id="23101-104">媒體會話會公開 [**IMFMediaSession**](/windows/desktop/api/mfidl/nn-mfidl-imfmediasession) 介面。</span><span class="sxs-lookup"><span data-stu-id="23101-104">The Media Session exposes the [**IMFMediaSession**](/windows/desktop/api/mfidl/nn-mfidl-imfmediasession) interface.</span></span> <span data-ttu-id="23101-105">有兩種方式可以建立媒體會話，視您的應用程式是否支援受保護的內容而定：</span><span class="sxs-lookup"><span data-stu-id="23101-105">There are two ways to create the Media Session, depending on whether your application will support protected content:</span></span>

-   <span data-ttu-id="23101-106">如果您的應用程式不支援受保護的內容，您可以藉由呼叫 [**MFCreateMediaSession**](/windows/desktop/api/mfidl/nf-mfidl-mfcreatemediasession)來建立媒體會話。</span><span class="sxs-lookup"><span data-stu-id="23101-106">If your application does not support protected content, you can create the Media Session by calling the [**MFCreateMediaSession**](/windows/desktop/api/mfidl/nf-mfidl-mfcreatemediasession).</span></span> <span data-ttu-id="23101-107">此函式會在應用程式進程內建立媒體會話。</span><span class="sxs-lookup"><span data-stu-id="23101-107">This function creates the Media Session inside the application process.</span></span>
-   <span data-ttu-id="23101-108">若要支援受保護的內容，請呼叫 [**MFCreatePMPMediaSession**](/windows/desktop/api/mfidl/nf-mfidl-mfcreatepmpmediasession)來建立媒體會話。</span><span class="sxs-lookup"><span data-stu-id="23101-108">To support protected content, create the Media Session by calling [**MFCreatePMPMediaSession**](/windows/desktop/api/mfidl/nf-mfidl-mfcreatepmpmediasession).</span></span> <span data-ttu-id="23101-109">此函式會在受保護的媒體路徑內建立媒體會話， (PMP) 進程。</span><span class="sxs-lookup"><span data-stu-id="23101-109">This function creates the Media Session inside the Protected Media Path (PMP) process.</span></span> <span data-ttu-id="23101-110">應用程式會接收 proxy 物件的指標，此物件會將跨進程界限的方法呼叫封送處理。</span><span class="sxs-lookup"><span data-stu-id="23101-110">The application receives a pointer to a proxy object that marshals method calls across the process boundary.</span></span> <span data-ttu-id="23101-111">請注意，PMP 媒體會話可以用來播放清楚的內容，以及受保護的內容。</span><span class="sxs-lookup"><span data-stu-id="23101-111">Note that the PMP Media Session can be used to play clear content, as well as protected content.</span></span>

<span data-ttu-id="23101-112">任何使用媒體會話的應用程式將會遵循下列一般步驟：</span><span class="sxs-lookup"><span data-stu-id="23101-112">Any application that uses the Media Session will follow these general steps:</span></span>

1.  <span data-ttu-id="23101-113">建立拓撲。</span><span class="sxs-lookup"><span data-stu-id="23101-113">Create a topology.</span></span>
2.  <span data-ttu-id="23101-114">藉由呼叫 [**IMFMediaSession：： SetTopology**](/windows/desktop/api/mfidl/nf-mfidl-imfmediasession-settopology)，在媒體會話上將拓撲排入佇列。</span><span class="sxs-lookup"><span data-stu-id="23101-114">Queue the topology on the Media Session by calling [**IMFMediaSession::SetTopology**](/windows/desktop/api/mfidl/nf-mfidl-imfmediasession-settopology).</span></span>
3.  <span data-ttu-id="23101-115">藉由呼叫 [**IMFMediaSession：： Start**](/windows/desktop/api/mfidl/nf-mfidl-imfmediasession-start)、 [**IMFMediaSession：:P ause**](/windows/desktop/api/mfidl/nf-mfidl-imfmediasession-pause)或 [**IMFMediaSession：： Stop**](/windows/desktop/api/mfidl/nf-mfidl-imfmediasession-stop)來控制資料的流程。</span><span class="sxs-lookup"><span data-stu-id="23101-115">Control the flow of data by calling [**IMFMediaSession::Start**](/windows/desktop/api/mfidl/nf-mfidl-imfmediasession-start), [**IMFMediaSession::Pause**](/windows/desktop/api/mfidl/nf-mfidl-imfmediasession-pause), or [**IMFMediaSession::Stop**](/windows/desktop/api/mfidl/nf-mfidl-imfmediasession-stop).</span></span>
4.  <span data-ttu-id="23101-116">在應用程式結束之前，呼叫 [**IMFMediaSession：： close**](/windows/desktop/api/mfidl/nf-mfidl-imfmediasession-close) 以關閉媒體會話。</span><span class="sxs-lookup"><span data-stu-id="23101-116">Before the application exits, call [**IMFMediaSession::Close**](/windows/desktop/api/mfidl/nf-mfidl-imfmediasession-close) to close the Media Session.</span></span>
5.  <span data-ttu-id="23101-117">藉由呼叫 [**IMFMediaSource：： Shutdown**](/windows/desktop/api/mfidl/nf-mfidl-imfmediasource-shutdown)，關閉應用程式所建立的任何媒體來源。</span><span class="sxs-lookup"><span data-stu-id="23101-117">Shut down any media sources that the application created, by calling [**IMFMediaSource::Shutdown**](/windows/desktop/api/mfidl/nf-mfidl-imfmediasource-shutdown).</span></span>
6.  <span data-ttu-id="23101-118">藉由呼叫 [**IMFMediaSession：： Shutdown**](/windows/desktop/api/mfidl/nf-mfidl-imfmediasession-shutdown)來關閉媒體會話。</span><span class="sxs-lookup"><span data-stu-id="23101-118">Shut down the Media Session by calling [**IMFMediaSession::Shutdown**](/windows/desktop/api/mfidl/nf-mfidl-imfmediasession-shutdown).</span></span>

<span data-ttu-id="23101-119">使用媒體會話時，應用程式不應該直接啟動、暫停或停止媒體來源。</span><span class="sxs-lookup"><span data-stu-id="23101-119">When using the Media Session, the application should not directly start, pause, or stop the media source.</span></span> <span data-ttu-id="23101-120">所有狀態變更都必須藉由呼叫 [**IMFMediaSession**](/windows/desktop/api/mfidl/nn-mfidl-imfmediasession) 方法來啟動。</span><span class="sxs-lookup"><span data-stu-id="23101-120">All state changes must be initiated by calling [**IMFMediaSession**](/windows/desktop/api/mfidl/nn-mfidl-imfmediasession) methods.</span></span> <span data-ttu-id="23101-121">媒體會話會處理媒體來源中的狀態變更。</span><span class="sxs-lookup"><span data-stu-id="23101-121">State changes in the media source are handled by the Media Session.</span></span>

<span data-ttu-id="23101-122">許多其他詳細資料將取決於您應用程式的特定功能。</span><span class="sxs-lookup"><span data-stu-id="23101-122">Many other details will depend on the specific functionality of your application.</span></span>

## <a name="protected-content"></a><span data-ttu-id="23101-123">受保護內容</span><span class="sxs-lookup"><span data-stu-id="23101-123">Protected Content</span></span>

<span data-ttu-id="23101-124">若要播放受保護的內容，您必須藉由呼叫 [**MFCreatePMPMediaSession**](/windows/desktop/api/mfidl/nf-mfidl-mfcreatepmpmediasession)，在受保護的媒體路徑 (PMP) 內建立媒體會話。</span><span class="sxs-lookup"><span data-stu-id="23101-124">To play protected content, you must create the Media Session inside the protected media path (PMP), by calling [**MFCreatePMPMediaSession**](/windows/desktop/api/mfidl/nf-mfidl-mfcreatepmpmediasession).</span></span> <span data-ttu-id="23101-125">此函式會在 PMP 內建立媒體會話的實例，並將指標傳回給跨進程界限封送處理介面的 proxy 物件。</span><span class="sxs-lookup"><span data-stu-id="23101-125">This function creates an instance of the Media Session inside the PMP and returns a pointer to a proxy object that marshals interfaces across the process boundary.</span></span>

<span data-ttu-id="23101-126">在大部分的情況下，在 PMP 內使用媒體會話對應用程式而言是透明的。</span><span class="sxs-lookup"><span data-stu-id="23101-126">In most respects, using the Media Session inside the PMP is transparent to the application.</span></span> <span data-ttu-id="23101-127">不過，應用程式可能需要叫用可讓使用者播放內容的特定動作。</span><span class="sxs-lookup"><span data-stu-id="23101-127">However, the application might need to invoke certain actions that enable the user to play the content.</span></span> <span data-ttu-id="23101-128">例如，使用者可能需要取得 DRM 授權。</span><span class="sxs-lookup"><span data-stu-id="23101-128">For example, the user might need to obtain a DRM license.</span></span> <span data-ttu-id="23101-129">媒體基礎使用 [**IMFContentEnabler**](/windows/desktop/api/mfidl/nn-mfidl-imfcontentenabler) 介面定義這些動作的一般機制。</span><span class="sxs-lookup"><span data-stu-id="23101-129">Media Foundation defines a generic mechanism for these actions using the [**IMFContentEnabler**](/windows/desktop/api/mfidl/nn-mfidl-imfcontentenabler) interface.</span></span>

<span data-ttu-id="23101-130">如需詳細資訊，請參閱下列主題：</span><span class="sxs-lookup"><span data-stu-id="23101-130">For more information, see the following topics:</span></span>

-   [<span data-ttu-id="23101-131">受保護的媒體路徑</span><span class="sxs-lookup"><span data-stu-id="23101-131">Protected Media Path</span></span>](protected-media-path.md)
-   [<span data-ttu-id="23101-132">如何播放受保護的媒體檔案</span><span class="sxs-lookup"><span data-stu-id="23101-132">How to Play Protected Media Files</span></span>](how-to-play-protected-media-files.md)

## <a name="presentation-clock"></a><span data-ttu-id="23101-133">簡報時鐘</span><span class="sxs-lookup"><span data-stu-id="23101-133">Presentation Clock</span></span>

<span data-ttu-id="23101-134">媒體會話會管理簡報時鐘的所有層面：</span><span class="sxs-lookup"><span data-stu-id="23101-134">The Media Session manages all aspects of the presentation clock:</span></span>

-   <span data-ttu-id="23101-135">建立簡報時鐘。</span><span class="sxs-lookup"><span data-stu-id="23101-135">Creating the presentation clock.</span></span>

-   <span data-ttu-id="23101-136">選取時間來源。</span><span class="sxs-lookup"><span data-stu-id="23101-136">Selecting the time source.</span></span>

-   <span data-ttu-id="23101-137">通知媒體接收時鐘</span><span class="sxs-lookup"><span data-stu-id="23101-137">Notifying the media sinks about the clock</span></span>

-   <span data-ttu-id="23101-138">視需要啟動、停止和暫停時鐘。</span><span class="sxs-lookup"><span data-stu-id="23101-138">Starting, stopping, and pausing the clock as necessary.</span></span>

-   <span data-ttu-id="23101-139">關閉時鐘。</span><span class="sxs-lookup"><span data-stu-id="23101-139">Shutting down the clock.</span></span>

<span data-ttu-id="23101-140">若要取得簡報時鐘的指標，請在媒體會話上呼叫 [**IMFMediaSession：： GetClock**](/windows/desktop/api/mfidl/nf-mfidl-imfmediasession-getclock) 。</span><span class="sxs-lookup"><span data-stu-id="23101-140">To get a pointer to the presentation clock, call [**IMFMediaSession::GetClock**](/windows/desktop/api/mfidl/nf-mfidl-imfmediasession-getclock) on the Media Session.</span></span> <span data-ttu-id="23101-141">簡報時鐘不會傳回有效的時間，直到媒體會話以 MF [](mesessiontopologystatus.md) \_ TOPOSTATUS READY 旗標傳送 MESessionTopologyStatus 事件為止 \_ 。</span><span class="sxs-lookup"><span data-stu-id="23101-141">The presentation clock does not return a valid time until the Media Session sends the [MESessionTopologyStatus](mesessiontopologystatus.md) event with the MF\_TOPOSTATUS\_READY flag.</span></span> <span data-ttu-id="23101-142">在那之前， **GetClock** 會傳回 MF \_ E \_ 時鐘 \_ NO \_ TIME \_ SOURCE。</span><span class="sxs-lookup"><span data-stu-id="23101-142">Until then, **GetClock** returns MF\_E\_CLOCK\_NO\_TIME\_SOURCE.</span></span>

<span data-ttu-id="23101-143">使用媒體會話的應用程式應該永遠不會啟動、停止或暫停簡報時鐘;變更頻率率;或關閉時鐘。</span><span class="sxs-lookup"><span data-stu-id="23101-143">An application that uses the Media Session should never start, stop, or pause the presentation clock; change the clock rate; or shut down the clock.</span></span>

<span data-ttu-id="23101-144">當應用程式呼叫 [**IMFMediaSession：： Start**](/windows/desktop/api/mfidl/nf-mfidl-imfmediasession-start)時，媒體會話會啟動簡報時鐘，其開始時間等於 **Start** 方法中指定的起始位置。</span><span class="sxs-lookup"><span data-stu-id="23101-144">When the application calls [**IMFMediaSession::Start**](/windows/desktop/api/mfidl/nf-mfidl-imfmediasession-start), the Media Session starts the presentation clock with a starting time equal to the starting position specified in the **Start** method.</span></span> <span data-ttu-id="23101-145">如需媒體會話的詳細資訊，請參閱 [媒體會話](media-session.md)。</span><span class="sxs-lookup"><span data-stu-id="23101-145">For more information about the Media Session, see [Media Session](media-session.md).</span></span>

## <a name="related-topics"></a><span data-ttu-id="23101-146">相關主題</span><span class="sxs-lookup"><span data-stu-id="23101-146">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="23101-147">媒體會話</span><span class="sxs-lookup"><span data-stu-id="23101-147">Media Session</span></span>](media-session.md)
</dt> </dl>

 

 



