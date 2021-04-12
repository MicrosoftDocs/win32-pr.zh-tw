---
description: Exclusive-Mode 資料流程
ms.assetid: 196cc6fe-91bf-46fa-acc9-38a7a4005875
title: Exclusive-Mode 資料流程
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 7722dd3463346e976f30a77949f56026a2425624
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/07/2021
ms.locfileid: "103936294"
---
# <a name="exclusive-mode-streams"></a>Exclusive-Mode 資料流程

如先前所述，如果應用程式在獨佔模式中開啟資料流程，應用程式就會獨佔使用播放或記錄串流的音訊端點裝置。 相反地，有數個應用程式可以在裝置上開啟共用模式串流，藉以共用音訊端點裝置。

音訊裝置的獨佔模式存取可以封鎖重要的系統音效、防止與其他應用程式的互通性，也會降低使用者體驗。 若要減輕這些問題，使用獨佔模式資料流程的應用程式通常會在應用程式不是前景進程或未主動串流時，會讓出音訊裝置的控制權。

資料流程延遲是資料路徑固有的延遲，可將應用程式的端點緩衝區與音訊端點裝置連接在一起。 若為轉譯資料流程，延遲是指應用程式將範例寫入端點緩衝區至範例透過喇叭聽到的時間所造成的最大延遲。 針對 capture 資料流程，延遲是從音效進入麥克風到應用程式可以從端點緩衝區讀取該音效之樣本的時間最大延遲。

使用獨佔模式資料流程的應用程式通常會這麼做，因為它們需要在音訊端點裝置與存取端點緩衝區的應用程式執行緒之間的資料路徑中有低延遲的情況。 一般而言，這些執行緒會以相對較高的優先順序執行，並將其本身排程為定期間隔執行，其接近或與定期間隔分開，以將連續處理傳遞給音訊硬體。 在每次通過時，音訊硬體都會處理端點緩衝區中的新資料。

若要達到最小的串流延遲，應用程式可能需要兩個特殊的音訊硬體，以及一個輕微載入的電腦系統。 驅動音訊硬體超過其時間限制，或使用競爭的高優先順序工作載入系統，可能會導致低延遲音訊串流發生問題。 例如，針對轉譯資料流程，如果應用程式無法在音訊硬體讀取緩衝區之前寫入至端點緩衝區，或如果硬體無法在緩衝區預定播放的時間之前讀取緩衝區，就會發生問題。 一般來說，要在各種不同的音訊硬體上執行的應用程式，以及廣泛的系統，都應該放寬其時間需求，以避免所有目標環境發生問題。

Windows Vista 有數項功能，可支援需要低延遲音訊串流的應用程式。 如 [使用者模式音訊元件](user-mode-audio-components.md)中所述，執行時間關鍵作業的應用程式可以呼叫多媒體類別排程器服務 (MMCSS) 函式來提高執行緒優先順序，而不會將 CPU 資源拒絕到較低優先順序的應用程式。 此外， [**IAudioClient：： Initialize**](/windows/desktop/api/Audioclient/nf-audioclient-iaudioclient-initialize) 方法支援 AUDCLNT \_ STREAMFLAGS \_ >app >eventcallback 旗標，可讓應用程式的緩衝區服務執行緒在新的緩衝區變成可供音訊裝置使用時，排程執行。 藉由使用這些功能，應用程式執行緒可以降低其執行時間的不確定性，進而降低低延遲音訊串流中發生問題的風險。

舊版音訊介面卡的驅動程式可能會使用 WaveCyclic 或 WavePci 設備磁碟機介面 (的 DDI) ，而較新的音訊介面卡驅動程式較有可能支援 WaveRT 的 DDI。 針對獨佔模式應用程式，WaveRT 驅動程式可提供比 WaveCyclic 或 WavePci 驅動程式更好的效能，但 WaveRT 驅動程式需要額外的硬體功能。 這些功能包括能夠直接與應用程式共用硬體緩衝區。 使用直接共用時，不需要系統介入，就能在獨佔模式應用程式和音訊硬體之間傳輸資料。 相反地，WaveCyclic 和 WavePci 驅動程式適用于較舊且較不支援的音訊介面卡。 這些介面卡依賴系統軟體來傳輸 (連接到系統 i/o 要求封包的資料區塊，或應用程式緩衝區與硬體緩衝區之間的 Irp) 。 此外，USB 音訊裝置也依賴系統軟體在應用程式緩衝區和硬體緩衝區之間傳輸資料。 為了改善連接到依賴系統進行資料傳輸之音訊裝置的獨佔模式應用程式效能，WASAPI 會自動增加系統執行緒的優先順序，以便在應用程式和硬體之間傳輸資料。 WASAPI 會使用 MMCSS 來提高執行緒優先順序。 在 Windows Vista 中，如果系統執行緒針對 PCM 格式和裝置期限小於10毫秒的獨佔模式音訊播放串流管理資料傳輸，WASAPI 會將 MMCSS 工作名稱 "Pro Audio" 指派給執行緒。 如果串流的裝置期間大於或等於10毫秒，WASAPI 會將 MMCSS 工作名稱 "Audio" 指派給執行緒。 如需有關 WaveCyclic、WavePci 和 WaveRT DDIs 的詳細資訊，請參閱 Windows DDK 檔。 如需有關選取適當裝置期間的詳細資訊，請參閱 [**IAudioClient：： GetDevicePeriod**](/windows/desktop/api/Audioclient/nf-audioclient-iaudioclient-getdeviceperiod)。

如 [會話磁片區控制項](session-volume-controls.md)中所述， [WASAPI](wasapi.md) 會提供 [**ISimpleAudioVolume**](/windows/desktop/api/Audioclient/nn-audioclient-isimpleaudiovolume)、 [**IChannelAudioVolume**](/windows/desktop/api/Audioclient/nn-audioclient-ichannelaudiovolume)和 [**IAudioStreamVolume**](/windows/desktop/api/Audioclient/nn-audioclient-iaudiostreamvolume) 介面，以控制共用模式音訊串流的磁片區層級。 不過，這些介面中的控制項對獨佔模式資料流程沒有任何作用。 相反地，管理獨佔模式串流的應用程式通常會使用 [ENDPOINTVOLUME API](endpointvolume-api.md)中的 [**IAudioEndpointVolume**](/windows/desktop/api/Endpointvolume/nn-endpointvolume-iaudioendpointvolume)介面來控制這些資料流程的磁片區層級。 如需此介面的詳細資訊，請參閱 [端點磁片區控制項](endpoint-volume-controls.md)。

針對系統中的每個播放裝置和捕獲裝置，使用者可以控制裝置是否可以在獨佔模式中使用。 如果使用者停用裝置的獨佔模式使用，則裝置可用來播放或只記錄共用模式串流。

如果使用者啟用裝置的獨佔模式使用，則使用者也可以控制應用程式在獨佔模式中使用裝置的要求，是否會由目前透過裝置播放或記錄共用模式串流的應用程式來執行裝置。 如果已啟用 [先占]，則如果裝置目前不在使用中，或如果裝置是在共用模式中使用，則應用程式對裝置進行獨佔控制權的要求將會成功，但如果另一個應用程式已經有裝置的獨佔控制權，則要求會失敗。 如果停用了 [已停用]，則如果裝置目前不在使用中，則應用程式對裝置進行獨佔控制權的要求將會成功，但如果裝置已在共用模式或獨佔模式中使用，則要求會失敗。

在 Windows Vista 中，音訊端點裝置的預設設定如下：

-   裝置可用來播放或記錄獨佔模式的串流。
-   使用裝置來播放或記錄獨佔模式串流的要求 shutdown 任何目前透過裝置播放或錄製的共用模式串流。

**變更播放或錄製裝置的獨佔模式設定**

1.  以滑鼠右鍵按一下通知區域中位於工作列右邊的喇叭圖示，然後選取 [ **播放裝置** ] 或 [ **錄製裝置**]。  (，請從命令提示字元視窗執行 [Windows 多媒體] 控制台 Mmsys.cpl。 如需詳細資訊，請參閱 [裝置 \_ 狀態 \_ XXX 常數](device-state-xxx-constants.md)中的備註。 ) 
2.  在 [ **音效** ] 視窗出現後，選取 [ **播放** ] 或 [ **錄製**]。 接下來，選取裝置名稱清單中的專案， **然後按一下 [** 內容]。
3.  在 [ **屬性** ] 視窗出現後，按一下 [ **Advanced**]。
4.  若要讓應用程式在獨佔模式中使用裝置，請核取標示為 [ **允許應用程式對此裝置進行獨佔控制**] 的方塊。 若要停用裝置的獨佔模式使用，請清除該核取方塊。
5.  如果已啟用裝置的專用模式使用，則您可以指定如果裝置目前現正播放或記錄共用模式串流，則對裝置的獨佔控制要求是否會成功。 若要讓獨佔模式應用程式優先于共用模式應用程式，請核取標示 **為 [提供獨佔模式應用程式優先順序]** 的方塊。 若要在共用模式應用程式上拒絕獨佔模式應用程式優先順序，請清除核取方塊。

下列程式碼範例示範如何在設定為在獨佔模式中使用的音訊轉譯裝置上播放低延遲音訊串流：


```C++
//-----------------------------------------------------------
// Play an exclusive-mode stream on the default audio
// rendering device. The PlayExclusiveStream function uses
// event-driven buffering and MMCSS to play the stream at
// the minimum latency supported by the device.
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

HRESULT PlayExclusiveStream(MyAudioSource *pMySource)
{
    HRESULT hr;
    REFERENCE_TIME hnsRequestedDuration = 0;
    IMMDeviceEnumerator *pEnumerator = NULL;
    IMMDevice *pDevice = NULL;
    IAudioClient *pAudioClient = NULL;
    IAudioRenderClient *pRenderClient = NULL;
    WAVEFORMATEX *pwfx = NULL;
    HANDLE hEvent = NULL;
    HANDLE hTask = NULL;
    UINT32 bufferFrameCount;
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

    // Call a helper function to negotiate with the audio
    // device for an exclusive-mode stream format.
    hr = GetStreamFormat(pAudioClient, &pwfx);
    EXIT_ON_ERROR(hr)

    // Initialize the stream to play at the minimum latency.
    hr = pAudioClient->GetDevicePeriod(NULL, &hnsRequestedDuration);
    EXIT_ON_ERROR(hr)

    hr = pAudioClient->Initialize(
                         AUDCLNT_SHAREMODE_EXCLUSIVE,
                         AUDCLNT_STREAMFLAGS_EVENTCALLBACK,
                         hnsRequestedDuration,
                         hnsRequestedDuration,
                         pwfx,
                         NULL);
    EXIT_ON_ERROR(hr)

    // Tell the audio source which format to use.
    hr = pMySource->SetFormat(pwfx);
    EXIT_ON_ERROR(hr)

    // Create an event handle and register it for
    // buffer-event notifications.
    hEvent = CreateEvent(NULL, FALSE, FALSE, NULL);
    if (hEvent == NULL)
    {
        hr = E_FAIL;
        goto Exit;
    }

    hr = pAudioClient->SetEventHandle(hEvent);
    EXIT_ON_ERROR(hr);

    // Get the actual size of the two allocated buffers.
    hr = pAudioClient->GetBufferSize(&bufferFrameCount);
    EXIT_ON_ERROR(hr)

    hr = pAudioClient->GetService(
                         IID_IAudioRenderClient,
                         (void**)&pRenderClient);
    EXIT_ON_ERROR(hr)

    // To reduce latency, load the first buffer with data
    // from the audio source before starting the stream.
    hr = pRenderClient->GetBuffer(bufferFrameCount, &pData);
    EXIT_ON_ERROR(hr)

    hr = pMySource->LoadData(bufferFrameCount, pData, &flags);
    EXIT_ON_ERROR(hr)

    hr = pRenderClient->ReleaseBuffer(bufferFrameCount, flags);
    EXIT_ON_ERROR(hr)

    // Ask MMCSS to temporarily boost the thread priority
    // to reduce glitches while the low-latency stream plays.
    DWORD taskIndex = 0;
    hTask = AvSetMmThreadCharacteristics(TEXT("Pro Audio"), &taskIndex);
    if (hTask == NULL)
    {
        hr = E_FAIL;
        EXIT_ON_ERROR(hr)
    }

    hr = pAudioClient->Start();  // Start playing.
    EXIT_ON_ERROR(hr)

    // Each loop fills one of the two buffers.
    while (flags != AUDCLNT_BUFFERFLAGS_SILENT)
    {
        // Wait for next buffer event to be signaled.
        DWORD retval = WaitForSingleObject(hEvent, 2000);
        if (retval != WAIT_OBJECT_0)
        {
            // Event handle timed out after a 2-second wait.
            pAudioClient->Stop();
            hr = ERROR_TIMEOUT;
            goto Exit;
        }

        // Grab the next empty buffer from the audio device.
        hr = pRenderClient->GetBuffer(bufferFrameCount, &pData);
        EXIT_ON_ERROR(hr)

        // Load the buffer with data from the audio source.
        hr = pMySource->LoadData(bufferFrameCount, pData, &flags);
        EXIT_ON_ERROR(hr)

        hr = pRenderClient->ReleaseBuffer(bufferFrameCount, flags);
        EXIT_ON_ERROR(hr)
    }

    // Wait for the last buffer to play before stopping.
    Sleep((DWORD)(hnsRequestedDuration/REFTIMES_PER_MILLISEC));

    hr = pAudioClient->Stop();  // Stop playing.
    EXIT_ON_ERROR(hr)

Exit:
    if (hEvent != NULL)
    {
        CloseHandle(hEvent);
    }
    if (hTask != NULL)
    {
        AvRevertMmThreadCharacteristics(hTask);
    }
    CoTaskMemFree(pwfx);
    SAFE_RELEASE(pEnumerator)
    SAFE_RELEASE(pDevice)
    SAFE_RELEASE(pAudioClient)
    SAFE_RELEASE(pRenderClient)

    return hr;
}
```



在上述程式碼範例中，PlayExclusiveStream 函式會在應用程式執行緒中執行，該執行緒會在播放轉譯資料流程時服務端點的緩衝區。 函數會採用單一參數 pMySource，它是屬於用戶端定義之類別 MyAudioSource 的物件指標。 此類別具有兩個在程式碼範例中呼叫的成員函式，LoadData 和 SetFormat。 轉譯 [資料流程](rendering-a-stream.md)中描述的是 MyAudioSource。

PlayExclusiveStream 函式會呼叫協助程式函式（GetStreamFormat），該函式會與預設轉譯裝置協調以判斷裝置是否支援適合應用程式使用的獨佔模式串流格式。 GetStreamFormat 函式的程式碼不會出現在程式碼範例中;這是因為其執行的詳細資料完全取決於應用程式的需求。 不過，您可以直接描述 GetStreamFormat 函式的作業，它會呼叫 [**IAudioClient：： IsFormatSupported**](/windows/desktop/api/Audioclient/nf-audioclient-iaudioclient-isformatsupported) 方法一或多次，以判斷裝置是否支援適當的格式。 應用程式的需求會決定 GetStreamFormat 呈現給 **IsFormatSupported** 方法的格式，以及呈現這些格式的順序。 如需 **IsFormatSupported** 的詳細資訊，請參閱 [裝置格式](device-formats.md)。

在 GetStreamFormat 呼叫之後，PlayExclusiveStream 函式會呼叫 [**IAudioClient：： GetDevicePeriod**](/windows/desktop/api/Audioclient/nf-audioclient-iaudioclient-getdeviceperiod) 方法，以取得音訊硬體所支援的最小裝置期限。 接下來，此函式會呼叫 [**IAudioClient：： Initialize**](/windows/desktop/api/Audioclient/nf-audioclient-iaudioclient-initialize) 方法，要求等於最小期間的緩衝區持續時間。 如果呼叫成功， **Initialize** 方法會配置兩個端點緩衝區，而每個緩衝區都等於最短期間的持續時間。 之後，當音訊串流開始執行時，應用程式和音訊硬體將會以 "乒乓球" 的方式共用兩個緩衝區，也就是當應用程式寫入某個緩衝區時，硬體會從其他緩衝區讀取。

在啟動資料流程之前，PlayExclusiveStream 函式會執行下列動作：

-   建立並註冊事件控制碼，當緩衝區變成可供填滿時，它會接收通知。
-   使用來自音訊來源的資料填滿第一個緩衝區，以減少當聽到初始音效時，從資料流程開始執行的延遲。
-   呼叫 **AvSetMmThreadCharacteristics** 函式，要求 MMCSS 提高 PlayExclusiveStream 執行所線上程的優先順序。  (當資料流程停止執行時， **AvRevertMmThreadCharacteristics** 函式呼叫會還原原始的執行緒優先順序。 ) 

如需 **AvSetMmThreadCharacteristics** 和 **AvRevertMmThreadCharacteristics** 的詳細資訊，請參閱 Windows SDK 檔。

當資料流程正在執行時，上述程式碼範例中 **while** 迴圈的每個反復專案都會填滿一個端點緩衝區。 在反復專案之間， **WaitForSingleObject** 函式呼叫會等待事件控制碼收到信號。 當控制碼收到信號時，迴圈主體會執行下列動作：

1.  呼叫 [**IAudioRenderClient：： GetBuffer**](/windows/desktop/api/Audioclient/nf-audioclient-iaudiorenderclient-getbuffer) 方法以取得下一個緩衝區。
2.  填滿緩衝區。
3.  呼叫 [**IAudioRenderClient：： ReleaseBuffer**](/windows/desktop/api/Audioclient/nf-audioclient-iaudiorenderclient-releasebuffer) 方法以釋放緩衝區。

如需 **WaitForSingleObject** 的詳細資訊，請參閱 Windows SDK 檔。

如果音訊介面卡是由 WaveRT 驅動程式所控制，則事件處理常式的信號會系結至來自音訊硬體的 DMA-傳輸通知。 若是 USB 音訊裝置，或由 WaveCyclic 或 WavePci 驅動程式控制的音訊裝置，事件控制碼的信號會系結至將資料從應用程式緩衝區傳輸到硬體緩衝區的 Irp 完成。

上述程式碼範例會將音訊硬體和電腦系統推送至其效能限制。 首先，為了減少資料流程延遲，應用程式會排程緩衝區服務執行緒，以使用音訊硬體將支援的最短裝置期限。 其次，為了確保執行緒可靠地在每個裝置期間內執行， **AvSetMmThreadCharacteristics** 函式呼叫會將 TaskName 參數設定為 "Pro Audio"，也就是在 Windows Vista 中，預設工作名稱的優先順序最高。 請考慮應用程式的時間需求是否可能會被放寬，而不會危及其實用性。 例如，應用程式可能會將其緩衝區服務執行緒排程為使用長度超過最小值的期間。 較長的期間可能會安全地允許使用較低的執行緒優先順序。

## <a name="related-topics"></a>相關主題

<dl> <dt>

[串流管理](stream-management.md)
</dt> </dl>

 

 



