---
description: 捕獲資料流程
ms.assetid: 1d9072dc-4f9b-4111-a747-5eb33ad3ae5b
title: 捕獲資料流程
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 371d4b92b97a26e81074edee68216255d576e614
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/07/2021
ms.locfileid: "103847338"
---
# <a name="capturing-a-stream"></a><span data-ttu-id="82d7a-103">捕獲資料流程</span><span class="sxs-lookup"><span data-stu-id="82d7a-103">Capturing a Stream</span></span>

<span data-ttu-id="82d7a-104">用戶端會呼叫 [**IAudioCaptureClient**](/windows/desktop/api/Audioclient/nn-audioclient-iaudiocaptureclient) 介面中的方法，從端點緩衝區讀取已捕捉的資料。</span><span class="sxs-lookup"><span data-stu-id="82d7a-104">The client calls the methods in the [**IAudioCaptureClient**](/windows/desktop/api/Audioclient/nn-audioclient-iaudiocaptureclient) interface to read captured data from an endpoint buffer.</span></span> <span data-ttu-id="82d7a-105">用戶端會在共用模式下與音訊引擎共用端點緩衝區，並以獨佔模式與音訊裝置共用。</span><span class="sxs-lookup"><span data-stu-id="82d7a-105">The client shares the endpoint buffer with the audio engine in shared mode and with the audio device in exclusive mode.</span></span> <span data-ttu-id="82d7a-106">若要要求特定大小的端點緩衝區，用戶端會呼叫 [**IAudioClient：： Initialize**](/windows/desktop/api/Audioclient/nf-audioclient-iaudioclient-initialize) 方法。</span><span class="sxs-lookup"><span data-stu-id="82d7a-106">To request an endpoint buffer of a particular size, the client calls the [**IAudioClient::Initialize**](/windows/desktop/api/Audioclient/nf-audioclient-iaudioclient-initialize) method.</span></span> <span data-ttu-id="82d7a-107">為了取得配置的緩衝區大小，這可能與所要求的大小不同，用戶端會呼叫 [**IAudioClient：： GetBufferSize**](/windows/desktop/api/Audioclient/nf-audioclient-iaudioclient-getbuffersize) 方法。</span><span class="sxs-lookup"><span data-stu-id="82d7a-107">To get the size of the allocated buffer, which might be different from the requested size, the client calls the [**IAudioClient::GetBufferSize**](/windows/desktop/api/Audioclient/nf-audioclient-iaudioclient-getbuffersize) method.</span></span>

<span data-ttu-id="82d7a-108">若要透過端點緩衝區移動已捕捉資料的資料流程，用戶端會交替呼叫 [**IAudioCaptureClient：： GetBuffer**](/windows/desktop/api/Audioclient/nf-audioclient-iaudiocaptureclient-getbuffer) 方法和 [**IAudioCaptureClient：： ReleaseBuffer**](/windows/desktop/api/Audioclient/nf-audioclient-iaudiocaptureclient-releasebuffer) 方法。</span><span class="sxs-lookup"><span data-stu-id="82d7a-108">To move a stream of captured data through the endpoint buffer, the client alternately calls the [**IAudioCaptureClient::GetBuffer**](/windows/desktop/api/Audioclient/nf-audioclient-iaudiocaptureclient-getbuffer) method and the [**IAudioCaptureClient::ReleaseBuffer**](/windows/desktop/api/Audioclient/nf-audioclient-iaudiocaptureclient-releasebuffer) method.</span></span> <span data-ttu-id="82d7a-109">用戶端會以一連串的資料封包來存取端點緩衝區中的資料。</span><span class="sxs-lookup"><span data-stu-id="82d7a-109">The client accesses the data in the endpoint buffer as a series of data packets.</span></span> <span data-ttu-id="82d7a-110">**GetBuffer** 呼叫會從緩衝區中取出已捕獲資料的下一個封包。</span><span class="sxs-lookup"><span data-stu-id="82d7a-110">The **GetBuffer** call retrieves the next packet of captured data from the buffer.</span></span> <span data-ttu-id="82d7a-111">從封包讀取資料之後，用戶端會呼叫 **ReleaseBuffer** 來釋出封包，並讓它可供更多捕獲的資料使用。</span><span class="sxs-lookup"><span data-stu-id="82d7a-111">After reading the data from the packet, the client calls **ReleaseBuffer** to release the packet and make it available for more captured data.</span></span>

<span data-ttu-id="82d7a-112">封包大小可能會與下一個 [**GetBuffer**](/windows/desktop/api/Audioclient/nf-audioclient-iaudiocaptureclient-getbuffer) 呼叫不同。</span><span class="sxs-lookup"><span data-stu-id="82d7a-112">The packet size can vary from one [**GetBuffer**](/windows/desktop/api/Audioclient/nf-audioclient-iaudiocaptureclient-getbuffer) call to the next.</span></span> <span data-ttu-id="82d7a-113">在呼叫 **GetBuffer** 之前，用戶端可以選擇呼叫 [**IAudioCaptureClient：： GetNextPacketSize**](/windows/desktop/api/Audioclient/nf-audioclient-iaudiocaptureclient-getnextpacketsize) 方法，事先取得下一個封包的大小。</span><span class="sxs-lookup"><span data-stu-id="82d7a-113">Before calling **GetBuffer**, the client has the option of calling the [**IAudioCaptureClient::GetNextPacketSize**](/windows/desktop/api/Audioclient/nf-audioclient-iaudiocaptureclient-getnextpacketsize) method to get the size of the next packet in advance.</span></span> <span data-ttu-id="82d7a-114">此外，用戶端可以呼叫 [**IAudioClient：： GetCurrentPadding**](/windows/desktop/api/Audioclient/nf-audioclient-iaudioclient-getcurrentpadding) 方法，以取得緩衝區中可用的已取得資料總量。</span><span class="sxs-lookup"><span data-stu-id="82d7a-114">In addition, the client can call the [**IAudioClient::GetCurrentPadding**](/windows/desktop/api/Audioclient/nf-audioclient-iaudioclient-getcurrentpadding) method to get the total amount of captured data that is available in the buffer.</span></span> <span data-ttu-id="82d7a-115">在任何瞬間，封包大小一律小於或等於緩衝區中的已捕獲資料總數。</span><span class="sxs-lookup"><span data-stu-id="82d7a-115">At any instant, the packet size is always less than or equal to the total amount of captured data in the buffer.</span></span>

<span data-ttu-id="82d7a-116">在每個處理階段中，用戶端可以透過下列其中一種方式來處理已捕捉的資料：</span><span class="sxs-lookup"><span data-stu-id="82d7a-116">During each processing pass, the client has the option of processing the captured data in one of the following ways:</span></span>

-   <span data-ttu-id="82d7a-117">用戶端會交替呼叫 [**GetBuffer**](/windows/desktop/api/Audioclient/nf-audioclient-iaudiocaptureclient-getbuffer) 和 [**ReleaseBuffer**](/windows/desktop/api/Audioclient/nf-audioclient-iaudiocaptureclient-releasebuffer)，並使用每一對呼叫來讀取一個封包，直到 **GetBuffer** 傳回 AUDCNT \_ S \_ BUFFEREMPTY，表示緩衝區是空的。</span><span class="sxs-lookup"><span data-stu-id="82d7a-117">The client alternately calls [**GetBuffer**](/windows/desktop/api/Audioclient/nf-audioclient-iaudiocaptureclient-getbuffer) and [**ReleaseBuffer**](/windows/desktop/api/Audioclient/nf-audioclient-iaudiocaptureclient-releasebuffer), reading one packet with each pair of calls, until **GetBuffer** returns AUDCNT\_S\_BUFFEREMPTY, indicating that the buffer is empty.</span></span>
-   <span data-ttu-id="82d7a-118">用戶端會在每對 [**GetBuffer**](/windows/desktop/api/Audioclient/nf-audioclient-iaudiocaptureclient-getbuffer)和 [**ReleaseBuffer**](/windows/desktop/api/Audioclient/nf-audioclient-iaudiocaptureclient-releasebuffer)的呼叫之前呼叫 [**GetNextPacketSize**](/windows/desktop/api/Audioclient/nf-audioclient-iaudiocaptureclient-getnextpacketsize) ，直到 **GetNextPacketSize** 報告封包大小為0，表示緩衝區是空的。</span><span class="sxs-lookup"><span data-stu-id="82d7a-118">The client calls [**GetNextPacketSize**](/windows/desktop/api/Audioclient/nf-audioclient-iaudiocaptureclient-getnextpacketsize) before each pair of calls to [**GetBuffer**](/windows/desktop/api/Audioclient/nf-audioclient-iaudiocaptureclient-getbuffer) and [**ReleaseBuffer**](/windows/desktop/api/Audioclient/nf-audioclient-iaudiocaptureclient-releasebuffer) until **GetNextPacketSize** reports a packet size of 0, indicating that the buffer is empty.</span></span>

<span data-ttu-id="82d7a-119">這兩種技術會產生相等的結果。</span><span class="sxs-lookup"><span data-stu-id="82d7a-119">The two techniques yield equivalent results.</span></span>

<span data-ttu-id="82d7a-120">下列程式碼範例示範如何從預設的擷取裝置錄製音訊串流：</span><span class="sxs-lookup"><span data-stu-id="82d7a-120">The following code example shows how to record an audio stream from the default capture device:</span></span>


```C++
//-----------------------------------------------------------
// Record an audio stream from the default audio capture
// device. The RecordAudioStream function allocates a shared
// buffer big enough to hold one second of PCM audio data.
// The function uses this buffer to stream data from the
// capture device. The main loop runs every 1/2 second.
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
const IID IID_IAudioCaptureClient = __uuidof(IAudioCaptureClient);

HRESULT RecordAudioStream(MyAudioSink *pMySink)
{
    HRESULT hr;
    REFERENCE_TIME hnsRequestedDuration = REFTIMES_PER_SEC;
    REFERENCE_TIME hnsActualDuration;
    UINT32 bufferFrameCount;
    UINT32 numFramesAvailable;
    IMMDeviceEnumerator *pEnumerator = NULL;
    IMMDevice *pDevice = NULL;
    IAudioClient *pAudioClient = NULL;
    IAudioCaptureClient *pCaptureClient = NULL;
    WAVEFORMATEX *pwfx = NULL;
    UINT32 packetLength = 0;
    BOOL bDone = FALSE;
    BYTE *pData;
    DWORD flags;

    hr = CoCreateInstance(
           CLSID_MMDeviceEnumerator, NULL,
           CLSCTX_ALL, IID_IMMDeviceEnumerator,
           (void**)&pEnumerator);
    EXIT_ON_ERROR(hr)

    hr = pEnumerator->GetDefaultAudioEndpoint(
                        eCapture, eConsole, &pDevice);
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

    // Get the size of the allocated buffer.
    hr = pAudioClient->GetBufferSize(&bufferFrameCount);
    EXIT_ON_ERROR(hr)

    hr = pAudioClient->GetService(
                         IID_IAudioCaptureClient,
                         (void**)&pCaptureClient);
    EXIT_ON_ERROR(hr)

    // Notify the audio sink which format to use.
    hr = pMySink->SetFormat(pwfx);
    EXIT_ON_ERROR(hr)

    // Calculate the actual duration of the allocated buffer.
    hnsActualDuration = (double)REFTIMES_PER_SEC *
                     bufferFrameCount / pwfx->nSamplesPerSec;

    hr = pAudioClient->Start();  // Start recording.
    EXIT_ON_ERROR(hr)

    // Each loop fills about half of the shared buffer.
    while (bDone == FALSE)
    {
        // Sleep for half the buffer duration.
        Sleep(hnsActualDuration/REFTIMES_PER_MILLISEC/2);

        hr = pCaptureClient->GetNextPacketSize(&packetLength);
        EXIT_ON_ERROR(hr)

        while (packetLength != 0)
        {
            // Get the available data in the shared buffer.
            hr = pCaptureClient->GetBuffer(
                                   &pData,
                                   &numFramesAvailable,
                                   &flags, NULL, NULL);
            EXIT_ON_ERROR(hr)

            if (flags & AUDCLNT_BUFFERFLAGS_SILENT)
            {
                pData = NULL;  // Tell CopyData to write silence.
            }

            // Copy the available capture data to the audio sink.
            hr = pMySink->CopyData(
                              pData, numFramesAvailable, &bDone);
            EXIT_ON_ERROR(hr)

            hr = pCaptureClient->ReleaseBuffer(numFramesAvailable);
            EXIT_ON_ERROR(hr)

            hr = pCaptureClient->GetNextPacketSize(&packetLength);
            EXIT_ON_ERROR(hr)
        }
    }

    hr = pAudioClient->Stop();  // Stop recording.
    EXIT_ON_ERROR(hr)

Exit:
    CoTaskMemFree(pwfx);
    SAFE_RELEASE(pEnumerator)
    SAFE_RELEASE(pDevice)
    SAFE_RELEASE(pAudioClient)
    SAFE_RELEASE(pCaptureClient)

    return hr;
}
```



<span data-ttu-id="82d7a-121">在上述範例中，RecordAudioStream 函式會採用單一參數， `pMySink` 也就是屬於用戶端定義類別 MyAudioSink 的物件指標，其中包含兩個函式 CopyData 和 SetFormat。</span><span class="sxs-lookup"><span data-stu-id="82d7a-121">In the preceding example, the RecordAudioStream function takes a single parameter, `pMySink`, which is a pointer to an object that belongs to a client-defined class, MyAudioSink, with two functions, CopyData and SetFormat.</span></span> <span data-ttu-id="82d7a-122">範例程式碼不包含 MyAudioSink 的執行，因為：</span><span class="sxs-lookup"><span data-stu-id="82d7a-122">The example code does not include the implementation of MyAudioSink because:</span></span>

-   <span data-ttu-id="82d7a-123">任何類別成員都不會直接與 WASAPI 中介面內的任何方法通訊。</span><span class="sxs-lookup"><span data-stu-id="82d7a-123">None of the class members communicates directly with any of the methods in the interfaces in WASAPI.</span></span>
-   <span data-ttu-id="82d7a-124">根據用戶端的需求，可以透過各種方式來執行類別。</span><span class="sxs-lookup"><span data-stu-id="82d7a-124">The class could be implemented in a variety of ways, depending on the requirements of the client.</span></span> <span data-ttu-id="82d7a-125"> (例如，它可能會將捕獲資料寫入至 WAV 檔案。 ) </span><span class="sxs-lookup"><span data-stu-id="82d7a-125">(For example, it might write the capture data to a WAV file.)</span></span>

<span data-ttu-id="82d7a-126">不過，這兩種方法的作業相關資訊對了解範例很有用。</span><span class="sxs-lookup"><span data-stu-id="82d7a-126">However, information about the operation of the two methods is useful for understanding the example.</span></span>

<span data-ttu-id="82d7a-127">CopyData 函式會從指定的緩衝區位置複製指定的音訊框架數目。</span><span class="sxs-lookup"><span data-stu-id="82d7a-127">The CopyData function copies a specified number of audio frames from a specified buffer location.</span></span> <span data-ttu-id="82d7a-128">RecordAudioStream 函式會使用 CopyData 函數，從共用緩衝區讀取和儲存音訊資料。</span><span class="sxs-lookup"><span data-stu-id="82d7a-128">The RecordAudioStream function uses the CopyData function to read and save the audio data from the shared buffer.</span></span> <span data-ttu-id="82d7a-129">SetFormat 函式會指定用於資料的 CopyData 函數格式。</span><span class="sxs-lookup"><span data-stu-id="82d7a-129">The SetFormat function specifies the format for the CopyData function to use for the data.</span></span>

<span data-ttu-id="82d7a-130">只要 MyAudioSink 物件需要額外的資料，CopyData 函式就會透過其第三個參數輸出值 **FALSE** ，而在上述程式碼範例中，是變數的指標 `bDone` 。</span><span class="sxs-lookup"><span data-stu-id="82d7a-130">As long as the MyAudioSink object requires additional data, the CopyData function outputs the value **FALSE** through its third parameter, which, in the preceding code example, is a pointer to the variable `bDone`.</span></span> <span data-ttu-id="82d7a-131">當 MyAudioSink 物件擁有所需的所有資料時，CopyData 函式會將設定 `bDone` 為 **TRUE**，這會導致程式結束 RecordAudioStream 函式中的迴圈。</span><span class="sxs-lookup"><span data-stu-id="82d7a-131">When the MyAudioSink object has all the data that it requires, the CopyData function sets `bDone` to **TRUE**, which causes the program to exit the loop in the RecordAudioStream function.</span></span>

<span data-ttu-id="82d7a-132">RecordAudioStream 函式會配置一個持續時間為一秒的共用緩衝區。</span><span class="sxs-lookup"><span data-stu-id="82d7a-132">The RecordAudioStream function allocates a shared buffer that has a duration of one second.</span></span> <span data-ttu-id="82d7a-133"> (配置的緩衝區可能會有較長的持續時間。 ) 在主要迴圈內，對 Windows [**Sleep**](/windows/desktop/api/synchapi/nf-synchapi-sleep) 函式的呼叫會導致程式等候半秒。</span><span class="sxs-lookup"><span data-stu-id="82d7a-133">(The allocated buffer might have a slightly longer duration.) Within the main loop, the call to the Windows [**Sleep**](/windows/desktop/api/synchapi/nf-synchapi-sleep) function causes the program to wait for a half second.</span></span> <span data-ttu-id="82d7a-134">在每個 **睡眠** 通話的開頭，共用緩衝區是空的或幾乎空白的。</span><span class="sxs-lookup"><span data-stu-id="82d7a-134">At the start of each **Sleep** call, the shared buffer is empty or nearly empty.</span></span> <span data-ttu-id="82d7a-135">當 **睡眠** 呼叫傳回時，共用緩衝區大約會填滿填滿資料的一半。</span><span class="sxs-lookup"><span data-stu-id="82d7a-135">By the time the **Sleep** call returns, the shared buffer is about half filled with capture data.</span></span>

<span data-ttu-id="82d7a-136">在呼叫 [**IAudioClient：： Initialize**](/windows/desktop/api/Audioclient/nf-audioclient-iaudioclient-initialize) 方法之後，資料流程會保持開啟，直到用戶端釋出其所有對 [**IAudioClient**](/windows/desktop/api/Audioclient/nn-audioclient-iaudioclient) 介面的參考，以及用戶端透過 [**IAudioClient：： GetService**](/windows/desktop/api/Audioclient/nf-audioclient-iaudioclient-getservice) 方法取得的所有服務介面參考。</span><span class="sxs-lookup"><span data-stu-id="82d7a-136">Following the call to the [**IAudioClient::Initialize**](/windows/desktop/api/Audioclient/nf-audioclient-iaudioclient-initialize) method, the stream remains open until the client releases all of its references to the [**IAudioClient**](/windows/desktop/api/Audioclient/nn-audioclient-iaudioclient) interface and to all references to service interfaces that the client obtained through the [**IAudioClient::GetService**](/windows/desktop/api/Audioclient/nf-audioclient-iaudioclient-getservice) method.</span></span> <span data-ttu-id="82d7a-137">最終 [**釋放**](/windows/desktop/api/unknwn/nf-unknwn-iunknown-release) 呼叫會關閉資料流程。</span><span class="sxs-lookup"><span data-stu-id="82d7a-137">The final [**Release**](/windows/desktop/api/unknwn/nf-unknwn-iunknown-release) call closes the stream.</span></span>

## <a name="related-topics"></a><span data-ttu-id="82d7a-138">相關主題</span><span class="sxs-lookup"><span data-stu-id="82d7a-138">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="82d7a-139">串流管理</span><span class="sxs-lookup"><span data-stu-id="82d7a-139">Stream Management</span></span>](stream-management.md)
</dt> </dl>

 

 
