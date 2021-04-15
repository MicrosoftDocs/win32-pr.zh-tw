---
description: 呈現資料流程
ms.assetid: 00bfcfd1-6592-43e3-90ad-730c92aa4cd3
title: 呈現資料流程
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 3d96e720bab43c75b0a3958bb3b6137d3a3d9ef6
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/07/2021
ms.locfileid: "104468325"
---
# <a name="rendering-a-stream"></a><span data-ttu-id="ca5fc-103">呈現資料流程</span><span class="sxs-lookup"><span data-stu-id="ca5fc-103">Rendering a Stream</span></span>

<span data-ttu-id="ca5fc-104">用戶端會呼叫 [**IAudioRenderClient**](/windows/desktop/api/Audioclient/nn-audioclient-iaudiorenderclient) 介面中的方法，將呈現資料寫入至端點緩衝區。</span><span class="sxs-lookup"><span data-stu-id="ca5fc-104">The client calls the methods in the [**IAudioRenderClient**](/windows/desktop/api/Audioclient/nn-audioclient-iaudiorenderclient) interface to write rendering data to an endpoint buffer.</span></span> <span data-ttu-id="ca5fc-105">若是共用模式資料流程，用戶端會與音訊引擎共用端點緩衝區。</span><span class="sxs-lookup"><span data-stu-id="ca5fc-105">For a shared-mode stream, the client shares the endpoint buffer with the audio engine.</span></span> <span data-ttu-id="ca5fc-106">如果是獨佔模式資料流程，用戶端會與音訊裝置共用端點緩衝區。</span><span class="sxs-lookup"><span data-stu-id="ca5fc-106">For an exclusive-mode stream, the client shares the endpoint buffer with the audio device.</span></span> <span data-ttu-id="ca5fc-107">若要要求特定大小的端點緩衝區，用戶端會呼叫 [**IAudioClient：： Initialize**](/windows/desktop/api/Audioclient/nf-audioclient-iaudioclient-initialize) 方法。</span><span class="sxs-lookup"><span data-stu-id="ca5fc-107">To request an endpoint buffer of a particular size, the client calls the [**IAudioClient::Initialize**](/windows/desktop/api/Audioclient/nf-audioclient-iaudioclient-initialize) method.</span></span> <span data-ttu-id="ca5fc-108">為了取得配置的緩衝區大小，這可能與所要求的大小不同，用戶端會呼叫 [**IAudioClient：： GetBufferSize**](/windows/desktop/api/Audioclient/nf-audioclient-iaudioclient-getbuffersize) 方法。</span><span class="sxs-lookup"><span data-stu-id="ca5fc-108">To get the size of the allocated buffer, which might be different from the requested size, the client calls the [**IAudioClient::GetBufferSize**](/windows/desktop/api/Audioclient/nf-audioclient-iaudioclient-getbuffersize) method.</span></span>

<span data-ttu-id="ca5fc-109">若要透過端點緩衝區移動轉譯資料的資料流程，用戶端會交替呼叫 [**IAudioRenderClient：： GetBuffer**](/windows/desktop/api/Audioclient/nf-audioclient-iaudiorenderclient-getbuffer) 方法和 [**IAudioRenderClient：： ReleaseBuffer**](/windows/desktop/api/Audioclient/nf-audioclient-iaudiorenderclient-releasebuffer) 方法。</span><span class="sxs-lookup"><span data-stu-id="ca5fc-109">To move a stream of rendering data through the endpoint buffer, the client alternately calls the [**IAudioRenderClient::GetBuffer**](/windows/desktop/api/Audioclient/nf-audioclient-iaudiorenderclient-getbuffer) method and the [**IAudioRenderClient::ReleaseBuffer**](/windows/desktop/api/Audioclient/nf-audioclient-iaudiorenderclient-releasebuffer) method.</span></span> <span data-ttu-id="ca5fc-110">用戶端會以一連串的資料封包來存取端點緩衝區中的資料。</span><span class="sxs-lookup"><span data-stu-id="ca5fc-110">The client accesses the data in the endpoint buffer as a series of data packets.</span></span> <span data-ttu-id="ca5fc-111">**GetBuffer** 呼叫會抓取下一個封包，讓用戶端可以填入轉譯資料。</span><span class="sxs-lookup"><span data-stu-id="ca5fc-111">The **GetBuffer** call retrieves the next packet so that the client can fill it with rendering data.</span></span> <span data-ttu-id="ca5fc-112">將資料寫入封包之後，用戶端會呼叫 **ReleaseBuffer** 將完成的封包新增至轉譯佇列。</span><span class="sxs-lookup"><span data-stu-id="ca5fc-112">After writing the data to the packet, the client calls **ReleaseBuffer** to add the completed packet to the rendering queue.</span></span>

<span data-ttu-id="ca5fc-113">針對轉譯緩衝區， [**IAudioClient：： GetCurrentPadding**](/windows/desktop/api/Audioclient/nf-audioclient-iaudioclient-getcurrentpadding) 方法所報告的填補值，代表已排入佇列以在緩衝區中播放的轉譯資料量。</span><span class="sxs-lookup"><span data-stu-id="ca5fc-113">For a rendering buffer, the padding value that is reported by the [**IAudioClient::GetCurrentPadding**](/windows/desktop/api/Audioclient/nf-audioclient-iaudioclient-getcurrentpadding) method represents the amount of rendering data that is queued up to play in the buffer.</span></span> <span data-ttu-id="ca5fc-114">轉譯應用程式可以使用填補值來判斷它可以安全地寫入緩衝區的新資料量，而不會有覆寫音訊引擎尚未從緩衝區讀取之先前寫入資料的風險。</span><span class="sxs-lookup"><span data-stu-id="ca5fc-114">A rendering application can use the padding value to determine how much new data it can safely write to the buffer without the risk of overwriting previously written data that the audio engine has not yet read from the buffer.</span></span> <span data-ttu-id="ca5fc-115">可用空間只是緩衝區大小減去填補大小。</span><span class="sxs-lookup"><span data-stu-id="ca5fc-115">The available space is simply the buffer size minus the padding size.</span></span> <span data-ttu-id="ca5fc-116">用戶端可以在下一個 [**GetBuffer**](/windows/desktop/api/Audioclient/nf-audioclient-iaudiorenderclient-getbuffer) 呼叫中要求代表部分或全部可用空間的封包大小。</span><span class="sxs-lookup"><span data-stu-id="ca5fc-116">The client can request a packet size that represents some or all of this available space in its next [**GetBuffer**](/windows/desktop/api/Audioclient/nf-audioclient-iaudiorenderclient-getbuffer) call.</span></span>

<span data-ttu-id="ca5fc-117">封包大小是以 *音訊框架* 表示。</span><span class="sxs-lookup"><span data-stu-id="ca5fc-117">The size of a packet is expressed in *audio frames*.</span></span> <span data-ttu-id="ca5fc-118">PCM 串流中的音訊框架是一組範例 (此集合會針對串流) 中的每個通道，各包含一個樣本， (時鐘刻度) 。</span><span class="sxs-lookup"><span data-stu-id="ca5fc-118">An audio frame in a PCM stream is a set of samples (the set contains one sample for each channel in the stream) that play or are recorded at the same time (clock tick).</span></span> <span data-ttu-id="ca5fc-119">因此，音訊框架的大小會是取樣大小乘以資料流程中的通道數目。</span><span class="sxs-lookup"><span data-stu-id="ca5fc-119">Thus, the size of an audio frame is the sample size multiplied by the number of channels in the stream.</span></span> <span data-ttu-id="ca5fc-120">例如，具有16位樣本的身歷聲 (2 通道) 資料流程的框架大小為四個位元組。</span><span class="sxs-lookup"><span data-stu-id="ca5fc-120">For example, the frame size for a stereo (2-channel) stream with 16-bit samples is four bytes.</span></span>

<span data-ttu-id="ca5fc-121">下列程式碼範例顯示如何在預設轉譯裝置上播放音訊串流：</span><span class="sxs-lookup"><span data-stu-id="ca5fc-121">The following code example shows how to play an audio stream on the default rendering device:</span></span>


```C++
//-----------------------------------------------------------
// Play an audio stream on the default audio rendering
// device. The PlayAudioStream function allocates a shared
// buffer big enough to hold one second of PCM audio data.
// The function uses this buffer to stream data to the
// rendering device. The inner loop runs every 1/2 second.
//-----------------------------------------------------------

// REFERENCE_TIME time units per second and per millisecond
#define REFTIMES_PER_SEC  10000000
#define REFTIMES_PER_MILLISEC  10000

#define EXIT_ON_ERROR(hres)  \
              if (FAILED(hres)) { goto Exit; }
#define SAFE_RELEASE(punk)  \
              if ((punk) != NULL)  \
                { (punk)->Release(); (punk) = NULL; }

const CLSID CLSID_MMDeviceEnumerator = __uuidof(MMDeviceEnumerator);
const IID IID_IMMDeviceEnumerator = __uuidof(IMMDeviceEnumerator);
const IID IID_IAudioClient = __uuidof(IAudioClient);
const IID IID_IAudioRenderClient = __uuidof(IAudioRenderClient);

HRESULT PlayAudioStream(MyAudioSource *pMySource)
{
    HRESULT hr;
    REFERENCE_TIME hnsRequestedDuration = REFTIMES_PER_SEC;
    REFERENCE_TIME hnsActualDuration;
    IMMDeviceEnumerator *pEnumerator = NULL;
    IMMDevice *pDevice = NULL;
    IAudioClient *pAudioClient = NULL;
    IAudioRenderClient *pRenderClient = NULL;
    WAVEFORMATEX *pwfx = NULL;
    UINT32 bufferFrameCount;
    UINT32 numFramesAvailable;
    UINT32 numFramesPadding;
    BYTE *pData;
    DWORD flags = 0;

    hr = CoCreateInstance(
           CLSID_MMDeviceEnumerator, NULL,
           CLSCTX_ALL, IID_IMMDeviceEnumerator,
           (void**)&pEnumerator);
    EXIT_ON_ERROR(hr)

    hr = pEnumerator->GetDefaultAudioEndpoint(
                        eRender, eConsole, &pDevice);
    EXIT_ON_ERROR(hr)

    hr = pDevice->Activate(
                    IID_IAudioClient, CLSCTX_ALL,
                    NULL, (void**)&pAudioClient);
    EXIT_ON_ERROR(hr)

    hr = pAudioClient->GetMixFormat(&pwfx);
    EXIT_ON_ERROR(hr)

    hr = pAudioClient->Initialize(
                         AUDCLNT_SHAREMODE_SHARED,
                         0,
                         hnsRequestedDuration,
                         0,
                         pwfx,
                         NULL);
    EXIT_ON_ERROR(hr)

    // Tell the audio source which format to use.
    hr = pMySource->SetFormat(pwfx);
    EXIT_ON_ERROR(hr)

    // Get the actual size of the allocated buffer.
    hr = pAudioClient->GetBufferSize(&bufferFrameCount);
    EXIT_ON_ERROR(hr)

    hr = pAudioClient->GetService(
                         IID_IAudioRenderClient,
                         (void**)&pRenderClient);
    EXIT_ON_ERROR(hr)

    // Grab the entire buffer for the initial fill operation.
    hr = pRenderClient->GetBuffer(bufferFrameCount, &pData);
    EXIT_ON_ERROR(hr)

    // Load the initial data into the shared buffer.
    hr = pMySource->LoadData(bufferFrameCount, pData, &flags);
    EXIT_ON_ERROR(hr)

    hr = pRenderClient->ReleaseBuffer(bufferFrameCount, flags);
    EXIT_ON_ERROR(hr)

    // Calculate the actual duration of the allocated buffer.
    hnsActualDuration = (double)REFTIMES_PER_SEC *
                        bufferFrameCount / pwfx->nSamplesPerSec;

    hr = pAudioClient->Start();  // Start playing.
    EXIT_ON_ERROR(hr)

    // Each loop fills about half of the shared buffer.
    while (flags != AUDCLNT_BUFFERFLAGS_SILENT)
    {
        // Sleep for half the buffer duration.
        Sleep((DWORD)(hnsActualDuration/REFTIMES_PER_MILLISEC/2));

        // See how much buffer space is available.
        hr = pAudioClient->GetCurrentPadding(&numFramesPadding);
        EXIT_ON_ERROR(hr)

        numFramesAvailable = bufferFrameCount - numFramesPadding;

        // Grab all the available space in the shared buffer.
        hr = pRenderClient->GetBuffer(numFramesAvailable, &pData);
        EXIT_ON_ERROR(hr)

        // Get next 1/2-second of data from the audio source.
        hr = pMySource->LoadData(numFramesAvailable, pData, &flags);
        EXIT_ON_ERROR(hr)

        hr = pRenderClient->ReleaseBuffer(numFramesAvailable, flags);
        EXIT_ON_ERROR(hr)
    }

    // Wait for last data in buffer to play before stopping.
    Sleep((DWORD)(hnsActualDuration/REFTIMES_PER_MILLISEC/2));

    hr = pAudioClient->Stop();  // Stop playing.
    EXIT_ON_ERROR(hr)

Exit:
    CoTaskMemFree(pwfx);
    SAFE_RELEASE(pEnumerator)
    SAFE_RELEASE(pDevice)
    SAFE_RELEASE(pAudioClient)
    SAFE_RELEASE(pRenderClient)

    return hr;
}
```



<span data-ttu-id="ca5fc-122">在上述範例中，PlayAudioStream 函式會採用單一參數， `pMySource` 也就是屬於用戶端定義類別 MyAudioSource 的物件指標，其中包含兩個成員函式 LoadData 和 SetFormat。</span><span class="sxs-lookup"><span data-stu-id="ca5fc-122">In the preceding example, the PlayAudioStream function takes a single parameter, `pMySource`, which is a pointer to an object that belongs to a client-defined class, MyAudioSource, with two member functions, LoadData and SetFormat.</span></span> <span data-ttu-id="ca5fc-123">範例程式碼不包含 MyAudioSource 的執行，因為：</span><span class="sxs-lookup"><span data-stu-id="ca5fc-123">The example code does not include the implementation of MyAudioSource because:</span></span>

-   <span data-ttu-id="ca5fc-124">任何類別成員都不會直接與 WASAPI 中介面內的任何方法通訊。</span><span class="sxs-lookup"><span data-stu-id="ca5fc-124">None of the class members communicates directly with any of the methods in the interfaces in WASAPI.</span></span>
-   <span data-ttu-id="ca5fc-125">根據用戶端的需求，可以透過各種方式來執行類別。</span><span class="sxs-lookup"><span data-stu-id="ca5fc-125">The class could be implemented in a variety of ways, depending on the requirements of the client.</span></span> <span data-ttu-id="ca5fc-126"> (例如，它可能會從 WAV 檔讀取轉譯資料，並即時執行資料流程格式的轉換。 ) </span><span class="sxs-lookup"><span data-stu-id="ca5fc-126">(For example, it might read the rendering data from a WAV file and perform on-the-fly conversion to the stream format.)</span></span>

<span data-ttu-id="ca5fc-127">不過，這兩個函式的部分相關資訊對了解此範例很有用。</span><span class="sxs-lookup"><span data-stu-id="ca5fc-127">However, some information about the operation of the two functions is useful for understanding the example.</span></span>

<span data-ttu-id="ca5fc-128">LoadData 函式會將指定的音訊畫面格數目 (第一個參數) 寫入 (第二個參數) 的指定緩衝區位置。</span><span class="sxs-lookup"><span data-stu-id="ca5fc-128">The LoadData function writes a specified number of audio frames (first parameter) to a specified buffer location (second parameter).</span></span> <span data-ttu-id="ca5fc-129"> (音訊框架的大小是資料流程中的通道數目乘以樣本大小。 ) PlayAudioStream 函式會使用 LoadData，以音訊資料填滿共用緩衝區的部分。</span><span class="sxs-lookup"><span data-stu-id="ca5fc-129">(The size of an audio frame is the number of channels in the stream multiplied by the sample size.) The PlayAudioStream function uses LoadData to fill portions of the shared buffer with audio data.</span></span> <span data-ttu-id="ca5fc-130">SetFormat 函式會指定用於資料的 LoadData 函數格式。</span><span class="sxs-lookup"><span data-stu-id="ca5fc-130">The SetFormat function specifies the format for the LoadData function to use for the data.</span></span> <span data-ttu-id="ca5fc-131">如果 LoadData 函式能夠將至少一個框架寫入指定的緩衝區位置，但在寫入指定的框架數之前就會用完資料，則會將無聲寫入其餘的畫面。</span><span class="sxs-lookup"><span data-stu-id="ca5fc-131">If the LoadData function is able to write at least one frame to the specified buffer location but runs out of data before it has written the specified number of frames, then it writes silence to the remaining frames.</span></span>

<span data-ttu-id="ca5fc-132">只要 LoadData 成功寫入至少一個真實資料框架 (不會) 到指定的緩衝區位置，它就會輸出0到第三個參數，在上述程式碼範例中，是變數的輸出指標 `flags` 。</span><span class="sxs-lookup"><span data-stu-id="ca5fc-132">As long as LoadData succeeds in writing at least one frame of real data (not silence) to the specified buffer location, it outputs 0 through its third parameter, which, in the preceding code example, is an output pointer to the `flags` variable.</span></span> <span data-ttu-id="ca5fc-133">當 LoadData 超出資料，而且無法將一個框架甚至寫入指定的緩衝區位置時，它不會將任何內容寫入緩衝區， (甚至無回應) ，而且會將 AUDCLNT BUFFERFLAGS 的值寫入 \_ \_ `flags` 變數。</span><span class="sxs-lookup"><span data-stu-id="ca5fc-133">When LoadData is out of data and cannot write even a single frame to the specified buffer location, it writes nothing to the buffer (not even silence), and it writes the value AUDCLNT\_BUFFERFLAGS\_SILENT to the `flags` variable.</span></span> <span data-ttu-id="ca5fc-134">此 `flags` 變數會將此值傳遞給 [**IAudioRenderClient：： ReleaseBuffer**](/windows/desktop/api/Audioclient/nf-audioclient-iaudiorenderclient-releasebuffer) 方法，該方法會藉由以無回應方式填滿緩衝區中指定的畫面格數目來回應。</span><span class="sxs-lookup"><span data-stu-id="ca5fc-134">The `flags` variable conveys this value to the [**IAudioRenderClient::ReleaseBuffer**](/windows/desktop/api/Audioclient/nf-audioclient-iaudiorenderclient-releasebuffer) method, which responds by filling the specified number of frames in the buffer with silence.</span></span>

<span data-ttu-id="ca5fc-135">在呼叫 [**IAudioClient：： Initialize**](/windows/desktop/api/Audioclient/nf-audioclient-iaudioclient-initialize) 方法時，上述範例中的 PlayAudioStream 函式會要求持續期間為一秒的共用緩衝區。</span><span class="sxs-lookup"><span data-stu-id="ca5fc-135">In its call to the [**IAudioClient::Initialize**](/windows/desktop/api/Audioclient/nf-audioclient-iaudioclient-initialize) method, the PlayAudioStream function in the preceding example requests a shared buffer that has a duration of one second.</span></span> <span data-ttu-id="ca5fc-136"> (配置的緩衝區可能會有較長的持續時間。 ) 在其初始呼叫 [**IAudioRenderClient：： GetBuffer**](/windows/desktop/api/Audioclient/nf-audioclient-iaudiorenderclient-getbuffer) 和 [**IAudioRenderClient：： ReleaseBuffer**](/windows/desktop/api/Audioclient/nf-audioclient-iaudiorenderclient-releasebuffer) 方法時，此函式會先填滿整個緩衝區，然後再呼叫 [**IAudioClient：： Start**](/windows/desktop/api/Audioclient/nf-audioclient-iaudioclient-start) 方法來開始播放緩衝區。</span><span class="sxs-lookup"><span data-stu-id="ca5fc-136">(The allocated buffer might have a slightly longer duration.) In its initial calls to the [**IAudioRenderClient::GetBuffer**](/windows/desktop/api/Audioclient/nf-audioclient-iaudiorenderclient-getbuffer) and [**IAudioRenderClient::ReleaseBuffer**](/windows/desktop/api/Audioclient/nf-audioclient-iaudiorenderclient-releasebuffer) methods, the function fills the entire buffer before calling the [**IAudioClient::Start**](/windows/desktop/api/Audioclient/nf-audioclient-iaudioclient-start) method to begin playing the buffer.</span></span>

<span data-ttu-id="ca5fc-137">在主要迴圈內，此函式會以半秒的間隔反復填滿一半的緩衝區。</span><span class="sxs-lookup"><span data-stu-id="ca5fc-137">Within the main loop, the function iteratively fills half of the buffer at half-second intervals.</span></span> <span data-ttu-id="ca5fc-138">在對主要迴圈中的每個 Windows [**睡眠**](/windows/win32/api/synchapi/nf-synchapi-sleep) 函數呼叫之前，緩衝區已滿或幾乎已滿。</span><span class="sxs-lookup"><span data-stu-id="ca5fc-138">Just before each call to the Windows [**Sleep**](/windows/win32/api/synchapi/nf-synchapi-sleep) function in the main loop, the buffer is full or nearly full.</span></span> <span data-ttu-id="ca5fc-139">當 **睡眠** 呼叫傳回時，緩衝區大約是一半滿。</span><span class="sxs-lookup"><span data-stu-id="ca5fc-139">When the **Sleep** call returns, the buffer is about half full.</span></span> <span data-ttu-id="ca5fc-140">迴圈會在 LoadData 函式的最後一個呼叫之後結束，將 `flags` 變數設為 AUDCLNT \_ BUFFERFLAGS \_ 無訊息值。</span><span class="sxs-lookup"><span data-stu-id="ca5fc-140">The loop ends after the final call to the LoadData function sets the `flags` variable to the value AUDCLNT\_BUFFERFLAGS\_SILENT.</span></span> <span data-ttu-id="ca5fc-141">屆時，緩衝區包含至少一個實際資料的畫面格，而且最多可以包含一半的實際資料。</span><span class="sxs-lookup"><span data-stu-id="ca5fc-141">At that point, the buffer contains at least one frame of real data, and it might contain as much as a half second of real data.</span></span> <span data-ttu-id="ca5fc-142">緩衝區的其餘部分包含無回應。</span><span class="sxs-lookup"><span data-stu-id="ca5fc-142">The remainder of the buffer contains silence.</span></span> <span data-ttu-id="ca5fc-143">迴圈之後的 **睡眠** 呼叫會提供足夠的時間 (半秒) 來播放所有剩餘的資料。</span><span class="sxs-lookup"><span data-stu-id="ca5fc-143">The **Sleep** call that follows the loop provides sufficient time (a half second) to play all of the remaining data.</span></span> <span data-ttu-id="ca5fc-144">在呼叫 [**IAudioClient：： Stop**](/windows/desktop/api/Audioclient/nf-audioclient-iaudioclient-stop) 方法停止音訊串流之前，資料後面的無聲會防止不必要的聲音。</span><span class="sxs-lookup"><span data-stu-id="ca5fc-144">The silence that follows the data prevents unwanted sounds before the call to the [**IAudioClient::Stop**](/windows/desktop/api/Audioclient/nf-audioclient-iaudioclient-stop) method stops the audio stream.</span></span> <span data-ttu-id="ca5fc-145">如需 **睡眠** 的詳細資訊，請參閱 Windows SDK 檔。</span><span class="sxs-lookup"><span data-stu-id="ca5fc-145">For more information about **Sleep**, see the Windows SDK documentation.</span></span>

<span data-ttu-id="ca5fc-146">在呼叫 [**IAudioClient：： Initialize**](/windows/desktop/api/Audioclient/nf-audioclient-iaudioclient-initialize) 方法之後，資料流程會保持開啟，直到用戶端釋出其所有對 [**IAudioClient**](/windows/desktop/api/Audioclient/nn-audioclient-iaudioclient) 介面的參考，以及用戶端透過 [**IAudioClient：： GetService**](/windows/desktop/api/Audioclient/nf-audioclient-iaudioclient-getservice) 方法取得的所有服務介面參考。</span><span class="sxs-lookup"><span data-stu-id="ca5fc-146">Following the call to the [**IAudioClient::Initialize**](/windows/desktop/api/Audioclient/nf-audioclient-iaudioclient-initialize) method, the stream remains open until the client releases all of its references to the [**IAudioClient**](/windows/desktop/api/Audioclient/nn-audioclient-iaudioclient) interface and to all references to service interfaces that the client obtained through the [**IAudioClient::GetService**](/windows/desktop/api/Audioclient/nf-audioclient-iaudioclient-getservice) method.</span></span> <span data-ttu-id="ca5fc-147">最終 [**釋放**](/windows/win32/api/unknwn/nf-unknwn-iunknown-release) 呼叫會關閉資料流程。</span><span class="sxs-lookup"><span data-stu-id="ca5fc-147">The final [**Release**](/windows/win32/api/unknwn/nf-unknwn-iunknown-release) call closes the stream.</span></span>

<span data-ttu-id="ca5fc-148">上述程式碼範例中的 PlayAudioStream 函式會呼叫 [**CoCreateInstance**](/windows/win32/api/combaseapi/nf-combaseapi-cocreateinstance) 函數，以建立系統中音訊端點裝置的列舉值。</span><span class="sxs-lookup"><span data-stu-id="ca5fc-148">The PlayAudioStream function in the preceding code example calls the [**CoCreateInstance**](/windows/win32/api/combaseapi/nf-combaseapi-cocreateinstance) function to create an enumerator for the audio endpoint devices in the system.</span></span> <span data-ttu-id="ca5fc-149">除非呼叫程式之前呼叫 **CoCreateInstance** 或 [**CoInitializeEx**](/windows/win32/api/combaseapi/nf-combaseapi-coinitializeex) 函式來初始化 COM 程式庫，否則 **CoCreateInstance** 呼叫會失敗。</span><span class="sxs-lookup"><span data-stu-id="ca5fc-149">Unless the calling program previously called either the **CoCreateInstance** or [**CoInitializeEx**](/windows/win32/api/combaseapi/nf-combaseapi-coinitializeex) function to initialize the COM library, the **CoCreateInstance** call will fail.</span></span> <span data-ttu-id="ca5fc-150">如需有關 **cocreateinstance**、 **cocreateinstance** 和 **CoInitializeEx** 的詳細資訊，請參閱 Windows SDK 檔。</span><span class="sxs-lookup"><span data-stu-id="ca5fc-150">For more information about **CoCreateInstance**, **CoCreateInstance**, and **CoInitializeEx**, see the Windows SDK documentation.</span></span>

## <a name="related-topics"></a><span data-ttu-id="ca5fc-151">相關主題</span><span class="sxs-lookup"><span data-stu-id="ca5fc-151">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="ca5fc-152">串流管理</span><span class="sxs-lookup"><span data-stu-id="ca5fc-152">Stream Management</span></span>](stream-management.md)
</dt> </dl>

 

 
