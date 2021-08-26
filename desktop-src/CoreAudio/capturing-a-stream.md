---
description: 捕獲資料流程
ms.assetid: 1d9072dc-4f9b-4111-a747-5eb33ad3ae5b
title: 捕獲資料流程
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 6dda6fd8527acbfff4072a2b79854eca4c32541f57d462b6073f9f6f39854ddb
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/11/2021
ms.locfileid: "120059028"
---
# <a name="capturing-a-stream"></a>捕獲資料流程

用戶端會呼叫 [**IAudioCaptureClient**](/windows/desktop/api/Audioclient/nn-audioclient-iaudiocaptureclient) 介面中的方法，從端點緩衝區讀取已捕捉的資料。 用戶端會在共用模式下與音訊引擎共用端點緩衝區，並以獨佔模式與音訊裝置共用。 若要要求特定大小的端點緩衝區，用戶端會呼叫 [**IAudioClient：： Initialize**](/windows/desktop/api/Audioclient/nf-audioclient-iaudioclient-initialize) 方法。 為了取得配置的緩衝區大小，這可能與所要求的大小不同，用戶端會呼叫 [**IAudioClient：： GetBufferSize**](/windows/desktop/api/Audioclient/nf-audioclient-iaudioclient-getbuffersize) 方法。

若要透過端點緩衝區移動已捕捉資料的資料流程，用戶端會交替呼叫 [**IAudioCaptureClient：： GetBuffer**](/windows/desktop/api/Audioclient/nf-audioclient-iaudiocaptureclient-getbuffer) 方法和 [**IAudioCaptureClient：： ReleaseBuffer**](/windows/desktop/api/Audioclient/nf-audioclient-iaudiocaptureclient-releasebuffer) 方法。 用戶端會以一連串的資料封包來存取端點緩衝區中的資料。 **GetBuffer** 呼叫會從緩衝區中取出已捕獲資料的下一個封包。 從封包讀取資料之後，用戶端會呼叫 **ReleaseBuffer** 來釋出封包，並讓它可供更多捕獲的資料使用。

封包大小可能會與下一個 [**GetBuffer**](/windows/desktop/api/Audioclient/nf-audioclient-iaudiocaptureclient-getbuffer) 呼叫不同。 在呼叫 **GetBuffer** 之前，用戶端可以選擇呼叫 [**IAudioCaptureClient：： GetNextPacketSize**](/windows/desktop/api/Audioclient/nf-audioclient-iaudiocaptureclient-getnextpacketsize) 方法，事先取得下一個封包的大小。 此外，用戶端可以呼叫 [**IAudioClient：： GetCurrentPadding**](/windows/desktop/api/Audioclient/nf-audioclient-iaudioclient-getcurrentpadding) 方法，以取得緩衝區中可用的已取得資料總量。 在任何瞬間，封包大小一律小於或等於緩衝區中的已捕獲資料總數。

在每個處理階段中，用戶端可以透過下列其中一種方式來處理已捕捉的資料：

-   用戶端會交替呼叫 [**GetBuffer**](/windows/desktop/api/Audioclient/nf-audioclient-iaudiocaptureclient-getbuffer) 和 [**ReleaseBuffer**](/windows/desktop/api/Audioclient/nf-audioclient-iaudiocaptureclient-releasebuffer)，並使用每一對呼叫來讀取一個封包，直到 **GetBuffer** 傳回 AUDCNT \_ S \_ BUFFEREMPTY，表示緩衝區是空的。
-   用戶端會在每對 [**GetBuffer**](/windows/desktop/api/Audioclient/nf-audioclient-iaudiocaptureclient-getbuffer)和 [**ReleaseBuffer**](/windows/desktop/api/Audioclient/nf-audioclient-iaudiocaptureclient-releasebuffer)的呼叫之前呼叫 [**GetNextPacketSize**](/windows/desktop/api/Audioclient/nf-audioclient-iaudiocaptureclient-getnextpacketsize) ，直到 **GetNextPacketSize** 報告封包大小為0，表示緩衝區是空的。

這兩種技術會產生相等的結果。

下列程式碼範例示範如何從預設的擷取裝置錄製音訊串流：


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



在上述範例中，RecordAudioStream 函式會採用單一參數， `pMySink` 也就是屬於用戶端定義類別 MyAudioSink 的物件指標，其中包含兩個函式 CopyData 和 SetFormat。 範例程式碼不包含 MyAudioSink 的執行，因為：

-   任何類別成員都不會直接與 WASAPI 中介面內的任何方法通訊。
-   根據用戶端的需求，可以透過各種方式來執行類別。  (例如，它可能會將捕獲資料寫入至 WAV 檔案。 ) 

不過，這兩種方法的作業相關資訊對了解範例很有用。

CopyData 函式會從指定的緩衝區位置複製指定的音訊框架數目。 RecordAudioStream 函式會使用 CopyData 函數，從共用緩衝區讀取和儲存音訊資料。 SetFormat 函式會指定用於資料的 CopyData 函數格式。

只要 MyAudioSink 物件需要額外的資料，CopyData 函式就會透過其第三個參數輸出值 **FALSE** ，而在上述程式碼範例中，是變數的指標 `bDone` 。 當 MyAudioSink 物件擁有所需的所有資料時，CopyData 函式會將設定 `bDone` 為 **TRUE**，這會導致程式結束 RecordAudioStream 函式中的迴圈。

RecordAudioStream 函式會配置一個持續時間為一秒的共用緩衝區。  (配置的緩衝區可能會有較長的持續時間。 ) 在主要迴圈內，對 Windows [**Sleep**](/windows/desktop/api/synchapi/nf-synchapi-sleep)函式的呼叫會導致程式等候半秒。 在每個 **睡眠** 通話的開頭，共用緩衝區是空的或幾乎空白的。 當 **睡眠** 呼叫傳回時，共用緩衝區大約會填滿填滿資料的一半。

在呼叫 [**IAudioClient：： Initialize**](/windows/desktop/api/Audioclient/nf-audioclient-iaudioclient-initialize) 方法之後，資料流程會保持開啟，直到用戶端釋出其所有對 [**IAudioClient**](/windows/desktop/api/Audioclient/nn-audioclient-iaudioclient) 介面的參考，以及用戶端透過 [**IAudioClient：： GetService**](/windows/desktop/api/Audioclient/nf-audioclient-iaudioclient-getservice) 方法取得的所有服務介面參考。 最終 [**釋放**](/windows/desktop/api/unknwn/nf-unknwn-iunknown-release) 呼叫會關閉資料流程。

## <a name="related-topics"></a>相關主題

<dl> <dt>

[串流管理](stream-management.md)
</dt> </dl>

 

 
