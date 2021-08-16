---
description: 本文提供一些簡單的範例，說明如何使用靜態空間音訊物件、動態空間音訊物件，以及使用 Microsoft 前端相對傳送函式的空間音訊物件 (HRTF) 來執行空間音效。
ms.assetid: C99C342E-0BD9-486A-92AA-F8DCB72C1B00
title: 使用空間音訊物件呈現空間音效
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 0a9498b1792ed884624afef859f3f8c70d6001d91be5dff15211717651dc4767
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/11/2021
ms.locfileid: "119642498"
---
# <a name="render-spatial-sound-using-spatial-audio-objects"></a>使用空間音訊物件呈現空間音效

本文提供一些簡單的範例，說明如何使用靜態空間音訊物件、動態空間音訊物件，以及使用 Microsoft 前端相對傳送函式的空間音訊物件 (HRTF) 來執行空間音效。 上述三項技術的執行步驟都非常類似，而且本文針對每個技術提供類似的結構化程式碼範例。 如需真實世界空間音訊實作為的完整端對端範例，請參閱 [Microsoft 空間音效範例 github 存放庫](https://github.com/Microsoft/Xbox-ATG-Samples/tree/master/UWPSamples/Audio)。 如需 Windows Sonic 的總覽，請參閱適用于 Xbox 和 Windows 上的空間音效支援的 Microsoft 平台層級解決方案，請參閱[空間音效](spatial-sound.md)。

## <a name="render-audio-using-static-spatial-audio-objects"></a>使用靜態空間音訊物件呈現音訊

靜態音訊物件是用來呈現音效至 [**AudioObjectType**](/windows/desktop/api/spatialaudioclient/ne-spatialaudioclient-audioobjecttype) 列舉中所定義之18個靜態音訊通道的其中一個。 每個通道都是在不隨著時間移動的固定點上的實際或虛擬化喇叭。 特定裝置上可用的靜態通道取決於所使用的空間音效格式。 如需支援的格式清單及其通道計數，請參閱 [空間音效](spatial-sound.md)。

當您初始化空間音訊串流時，您必須指定串流將使用的可用靜態通道。 下列範例常數定義可以用來指定常見的喇叭設定，並取得每個設定的可用通道數目。


```C++
const AudioObjectType ChannelMask_Mono = AudioObjectType_FrontCenter;
const AudioObjectType ChannelMask_Stereo = (AudioObjectType)(AudioObjectType_FrontLeft | AudioObjectType_FrontRight);
const AudioObjectType ChannelMask_2_1 = (AudioObjectType)(ChannelMask_Stereo | AudioObjectType_LowFrequency);
const AudioObjectType ChannelMask_Quad = (AudioObjectType)(AudioObjectType_FrontLeft | AudioObjectType_FrontRight | AudioObjectType_BackLeft | AudioObjectType_BackRight);
const AudioObjectType ChannelMask_4_1 = (AudioObjectType)(ChannelMask_Quad | AudioObjectType_LowFrequency);
const AudioObjectType ChannelMask_5_1 = (AudioObjectType)(AudioObjectType_FrontLeft | AudioObjectType_FrontRight | AudioObjectType_FrontCenter | AudioObjectType_LowFrequency | AudioObjectType_SideLeft | AudioObjectType_SideRight);
const AudioObjectType ChannelMask_7_1 = (AudioObjectType)(ChannelMask_5_1 | AudioObjectType_BackLeft | AudioObjectType_BackRight);

const UINT32 MaxStaticObjectCount_7_1_4 = 12;
const AudioObjectType ChannelMask_7_1_4 = (AudioObjectType)(ChannelMask_7_1 | AudioObjectType_TopFrontLeft | AudioObjectType_TopFrontRight | AudioObjectType_TopBackLeft | AudioObjectType_TopBackRight);

const UINT32 MaxStaticObjectCount_7_1_4_4 = 16;
const AudioObjectType ChannelMask_7_1_4_4 = (AudioObjectType)(ChannelMask_7_1_4 | AudioObjectType_BottomFrontLeft | AudioObjectType_BottomFrontRight |AudioObjectType_BottomBackLeft | AudioObjectType_BottomBackRight);

const UINT32 MaxStaticObjectCount_8_1_4_4 = 17;
const AudioObjectType ChannelMask_8_1_4_4 = (AudioObjectType)(ChannelMask_7_1_4_4 | AudioObjectType_BackCenter);
```



轉譯空間音訊的第一個步驟是取得音訊資料將傳送至的音訊端點。 建立 [**MMDeviceEnumerator**](/windows/desktop/api/Mmdeviceapi/nn-mmdeviceapi-immdeviceenumerator) 的實例，並呼叫 [**GetDefaultAudioEndpoint**](/windows/desktop/api/Mmdeviceapi/nf-mmdeviceapi-immdeviceenumerator-getdefaultaudioendpoint) 以取得預設音訊轉譯裝置。


```C++
HRESULT hr;
Microsoft::WRL::ComPtr<IMMDeviceEnumerator> deviceEnum;
Microsoft::WRL::ComPtr<IMMDevice> defaultDevice;

hr = CoCreateInstance(__uuidof(MMDeviceEnumerator), nullptr, CLSCTX_ALL, __uuidof(IMMDeviceEnumerator), (void**)&deviceEnum);
hr = deviceEnum->GetDefaultAudioEndpoint(EDataFlow::eRender, eMultimedia, &defaultDevice);
```



當您建立空間音訊串流時，您必須提供 [WAVEFORMATEX](../medfound/mf-mt-audio-prefer-waveformatex-attribute.md) 結構，以指定資料流程將使用的音訊格式。 如果您是從檔案播放音訊，格式通常會由音訊檔案格式決定。 此範例使用 mono、32位、48Hz 格式。


```C++
WAVEFORMATEX format;
format.wFormatTag = WAVE_FORMAT_IEEE_FLOAT;
format.wBitsPerSample = 32;
format.nChannels = 1;
format.nSamplesPerSec = 48000;
format.nBlockAlign = (format.wBitsPerSample >> 3) * format.nChannels;
format.nAvgBytesPerSec = format.nBlockAlign * format.nSamplesPerSec;
format.cbSize = 0;
```



轉譯空間音訊的下一步是初始化空間音訊串流。 首先，藉由呼叫 [**IMMDevice：： Activate**](/windows/desktop/api/Mmdeviceapi/nf-mmdeviceapi-immdevice-activate)來取得 [**ISpatialAudioClient**](/windows/desktop/api/spatialaudioclient/nn-spatialaudioclient-ispatialaudioclient)的實例。 呼叫 [**ISpatialAudioClient：： IsAudioObjectFormatSupported**](/windows/desktop/api/spatialaudioclient/nf-spatialaudioclient-ispatialaudioclient-isaudioobjectformatsupported) ，以確保支援您所使用的音訊格式。 建立音訊管線將用來通知應用程式是否已準備好使用音訊資料的事件。

填入將用來初始化空間音訊串流的 [**SpatialAudioObjectRenderStreamActivationParams**](/windows/desktop/api/spatialaudioclient/ns-spatialaudioclient-spatialaudioobjectrenderstreamactivationparams) 結構。 在此範例中， **StaticObjectTypeMask** 欄位設定為本文先前定義的 **ChannelMask \_ 身歷聲** 常數，表示音訊串流只能使用 front 右邊和左方通道。 因為這個範例只會使用靜態音訊物件和沒有動態物件，所以 **MaxDynamicObjectCount** 欄位會設定為0。 [ **類別目錄** ] 欄位設定為 [ [**音訊 \_ 串流 \_ 類別**](/windows/desktop/api/audiosessiontypes/ne-audiosessiontypes-audio_stream_category) ] 列舉的成員，其定義系統如何與其他音訊來源混合此資料流程的音效。

呼叫 [**ISpatialAudioClient：： ActivateSpatialAudioStream**](/windows/desktop/api/spatialaudioclient/nf-spatialaudioclient-ispatialaudioclient-activatespatialaudiostream) 來啟動資料流程。


```C++
Microsoft::WRL::ComPtr<ISpatialAudioClient> spatialAudioClient;

// Activate ISpatialAudioClient on the desired audio-device 
hr = defaultDevice->Activate(__uuidof(ISpatialAudioClient), CLSCTX_INPROC_SERVER, nullptr, (void**)&spatialAudioClient);

hr = spatialAudioClient->IsAudioObjectFormatSupported(&format);

// Create the event that will be used to signal the client for more data
HANDLE bufferCompletionEvent = CreateEvent(nullptr, FALSE, FALSE, nullptr);

SpatialAudioObjectRenderStreamActivationParams streamParams;
streamParams.ObjectFormat = &format;
streamParams.StaticObjectTypeMask = ChannelMask_Stereo;
streamParams.MinDynamicObjectCount = 0;
streamParams.MaxDynamicObjectCount = 0;
streamParams.Category = AudioCategory_SoundEffects;
streamParams.EventHandle = bufferCompletionEvent;
streamParams.NotifyObject = nullptr;

PROPVARIANT activationParams;
PropVariantInit(&activationParams);
activationParams.vt = VT_BLOB;
activationParams.blob.cbSize = sizeof(streamParams);
activationParams.blob.pBlobData = reinterpret_cast<BYTE *>(&streamParams);

Microsoft::WRL::ComPtr<ISpatialAudioObjectRenderStream> spatialAudioStream;
hr = spatialAudioClient->ActivateSpatialAudioStream(&activationParams, __uuidof(spatialAudioStream), (void**)&spatialAudioStream);
```



> [!Note]  
> 在 Xbox One 開發工具組上使用 [**ISpatialAudioClient**](/windows/desktop/api/spatialaudioclient/nn-spatialaudioclient-ispatialaudioclient)介面時 (XDK) 標題，您必須先呼叫 **EnableSpatialAudio** ，然後再呼叫 [**IMMDeviceEnumerator：： EnumAudioEndpoints**](/windows/desktop/api/Mmdeviceapi/nf-mmdeviceapi-immdeviceenumerator-enumaudioendpoints)或 [**IMMDeviceEnumerator：： GetDefaultAudioEndpoint**](/windows/desktop/api/Mmdeviceapi/nf-mmdeviceapi-immdeviceenumerator-getdefaultaudioendpoint)。 若未這麼做，將會導致 \_ 從啟動的呼叫傳回電子 NOINTERFACE 錯誤。 **EnableSpatialAudio** 僅適用于 XDK 標題，不需要針對 Xbox One 上執行的通用 Windows 平臺應用程式，或任何非 Xbox One 裝置呼叫。

 

宣告將用來將音訊資料寫入靜態通道的 [**ISpatialAudioObject**](/windows/desktop/api/spatialaudioclient/nn-spatialaudioclient-ispatialaudioobject) 指標。 一般的應用程式會針對 **StaticObjectTypeMask** 欄位中所指定的每個通道使用物件。 為了簡單起見，此範例只會使用單一靜態音訊物件。


```C++
// In this simple example, one object will be rendered
Microsoft::WRL::ComPtr<ISpatialAudioObject> audioObjectFrontLeft;
```



進入音訊轉譯迴圈之前，請先呼叫 [**ISpatialAudioObjectRenderStream：： Start**](/windows/win32/api/spatialaudioclient/nf-spatialaudioclient-ispatialaudioobjectrenderstreambase-start) 來指示媒體管線開始要求音訊資料。 此範例會使用計數器，在5秒後停止轉譯音訊。

在轉譯迴圈內，等候空間音訊串流初始化時所提供的緩衝區完成事件，以發出信號。 在等候事件時，您應該設定合理的超時限制，例如 100 ms，因為轉譯類型或端點的任何變更都會導致該事件永遠不會收到信號。 在此情況下，您可以呼叫 [**ISpatialAudioObjectRenderStream：： Reset**](/windows/win32/api/spatialaudioclient/nf-spatialaudioclient-ispatialaudioobjectrenderstreambase-reset) 以嘗試重設空間音訊串流。

接下來，呼叫 [**ISpatialAudioObjectRenderStream：： BeginUpdatingAudioObjects**](/windows/win32/api/spatialaudioclient/nf-spatialaudioclient-ispatialaudioobjectrenderstreambase-beginupdatingaudioobjects) ，讓系統知道您即將以資料填滿音訊物件的緩衝區。 這個方法會傳回可用動態音訊物件的數目（在此範例中不使用），以及此資料流程轉譯之音訊物件緩衝區的框架計數。

如果尚未建立靜態空間音訊物件，請呼叫 [**ISpatialAudioObjectRenderStream：： ActivateSpatialAudioObject**](/windows/desktop/api/spatialaudioclient/nf-spatialaudioclient-ispatialaudioobjectrenderstream-activatespatialaudioobject)來建立一個或多個，並從 [**AudioObjectType**](/windows/desktop/api/spatialaudioclient/ne-spatialaudioclient-audioobjecttype) 列舉中傳遞值，指出物件音訊呈現的靜態通道。

接下來，呼叫 [**ISpatialAudioObject：： GetBuffer**](/windows/win32/api/spatialaudioclient/nf-spatialaudioclient-ispatialaudioobjectbase-getbuffer) 取得空間音訊物件之音訊緩衝區的指標。 這個方法也會傳回緩衝區的大小（以位元組為單位）。 此範例使用 helper 方法 **WriteToAudioObjectBuffer**，以音訊資料填滿緩衝區。 本文稍後會顯示這個方法。 寫入緩衝區之後，此範例會檢查是否已達到物件的5秒存留期，如果是，則會呼叫 [**ISpatialAudioObject：： SetEndOfStream**](/windows/win32/api/spatialaudioclient/nf-spatialaudioclient-ispatialaudioobjectbase-setendofstream) ，讓音訊管線知道將不會再使用這個物件來撰寫音訊，並將物件設定為 **nullptr** 來釋出其資源。

將資料寫入所有音訊物件之後，請呼叫 [**ISpatialAudioObjectRenderStream：： EndUpdatingAudioObjects**](/windows/win32/api/spatialaudioclient/nf-spatialaudioclient-ispatialaudioobjectrenderstreambase-endupdatingaudioobjects) ，讓系統知道資料已可供轉譯。 您只能在呼叫 **BeginUpdatingAudioObjects** 和 **EndUpdatingAudioObjects** 之間呼叫 **GetBuffer** 。


```C++
// Start streaming / rendering 
hr = spatialAudioStream->Start();

// This example will render 5 seconds of audio samples
UINT totalFrameCount = format.nSamplesPerSec * 5;

bool isRendering = true;
while (isRendering)
{
    // Wait for a signal from the audio-engine to start the next processing pass
    if (WaitForSingleObject(bufferCompletionEvent, 100) != WAIT_OBJECT_0)
    {
        hr = spatialAudioStream->Reset();

        if (hr != S_OK)
        {
            // handle the error
            break;
        }
    }

    UINT32 availableDynamicObjectCount;
    UINT32 frameCount;

    // Begin the process of sending object data and metadata
    // Get the number of dynamic objects that can be used to send object-data
    // Get the frame count that each buffer will be filled with 
    hr = spatialAudioStream->BeginUpdatingAudioObjects(&availableDynamicObjectCount, &frameCount);

    BYTE* buffer;
    UINT32 bufferLength;

    if (audioObjectFrontLeft == nullptr)
    {
        hr = spatialAudioStream->ActivateSpatialAudioObject(AudioObjectType::AudioObjectType_FrontLeft, &audioObjectFrontLeft);
        if (hr != S_OK) break;
    }

    // Get the buffer to write audio data
    hr = audioObjectFrontLeft->GetBuffer(&buffer, &bufferLength);

    if (totalFrameCount >= frameCount)
    {
        // Write audio data to the buffer
        WriteToAudioObjectBuffer(reinterpret_cast<float*>(buffer), frameCount, 200.0f, format.nSamplesPerSec);

        totalFrameCount -= frameCount;
    }
    else
    {
        // Write audio data to the buffer
        WriteToAudioObjectBuffer(reinterpret_cast<float*>(buffer), totalFrameCount, 750.0f, format.nSamplesPerSec);

        // Set end of stream for the last buffer 
        hr = audioObjectFrontLeft->SetEndOfStream(totalFrameCount);

        audioObjectFrontLeft = nullptr; // Release the object

        isRendering = false;
    }

    // Let the audio engine know that the object data are available for processing now
    hr = spatialAudioStream->EndUpdatingAudioObjects();
};
```



當您完成轉譯空間音訊時，請呼叫 [**ISpatialAudioObjectRenderStream：： stop**](/windows/win32/api/spatialaudioclient/nf-spatialaudioclient-ispatialaudioobjectrenderstreambase-stop)來停止空間音訊串流。 如果您不打算再次使用資料流程，請呼叫 [**ISpatialAudioObjectRenderStream：： Reset**](/windows/win32/api/spatialaudioclient/nf-spatialaudioclient-ispatialaudioobjectrenderstreambase-reset)來釋出其資源。


```C++
// Stop the stream
hr = spatialAudioStream->Stop();

// Don't want to start again, so reset the stream to free its resources
hr = spatialAudioStream->Reset();

CloseHandle(bufferCompletionEvent);
```



**WriteToAudioObjectBuffer** helper 方法會寫入樣本的完整緩衝區或應用程式定義的時間限制所指定的剩餘樣本數。 您也可以根據來源音訊檔案中剩餘的樣本數，判斷這一點。 會產生簡單的 sin wave，以 *頻率* 輸入參數來調整的頻率，並寫入緩衝區。


```C++
void WriteToAudioObjectBuffer(FLOAT* buffer, UINT frameCount, FLOAT frequency, UINT samplingRate)
{
    const double PI = 4 * atan2(1.0, 1.0);
    static double _radPhase = 0.0;

    double step = 2 * PI * frequency / samplingRate;

    for (UINT i = 0; i < frameCount; i++)
    {
        double sample = sin(_radPhase);

        buffer[i] = FLOAT(sample);

        _radPhase += step; // next frame phase

        if (_radPhase >= 2 * PI)
        {
            _radPhase -= 2 * PI;
        }
    }
}
```



## <a name="render-audio-using-dynamic-spatial-audio-objects"></a>使用動態空間音訊物件呈現音訊

動態物件可讓您從空間中的任意位置（相對於使用者）呈現音訊。 動態音訊物件的位置和數量可以隨著時間變更。 遊戲通常會使用遊戲世界中3D 物件的位置來指定動態音訊物件與其相關聯的位置。 下列範例會使用簡單結構 **My3dObject**，來儲存代表物件所需的最少資料集。 這項資料包括 [**ISpatialAudioObject**](/windows/desktop/api/spatialaudioclient/nn-spatialaudioclient-ispatialaudioobject)的指標、物件的位置、速度、數量和音調頻率，以及儲存物件呈現音效的框架總數的值。


```C++
struct My3dObject
{
    Microsoft::WRL::ComPtr<ISpatialAudioObject> audioObject;
    Windows::Foundation::Numerics::float3 position;
    Windows::Foundation::Numerics::float3 velocity;
    float volume;
    float frequency; // in Hz
    UINT totalFrameCount;
};
```



動態音訊物件的執行步驟與上述靜態音訊物件的步驟大致相同。 首先，取得音訊端點。


```C++
HRESULT hr;
Microsoft::WRL::ComPtr<IMMDeviceEnumerator> deviceEnum;
Microsoft::WRL::ComPtr<IMMDevice> defaultDevice;

hr = CoCreateInstance(__uuidof(MMDeviceEnumerator), nullptr, CLSCTX_ALL, __uuidof(IMMDeviceEnumerator), (void**)&deviceEnum);
hr = deviceEnum->GetDefaultAudioEndpoint(EDataFlow::eRender, eMultimedia, &defaultDevice);
```



接下來，初始化空間音訊串流。 藉由呼叫 [**IMMDevice：： Activate**](/windows/desktop/api/Mmdeviceapi/nf-mmdeviceapi-immdevice-activate)來取得 [**ISpatialAudioClient**](/windows/desktop/api/spatialaudioclient/nn-spatialaudioclient-ispatialaudioclient)的實例。 呼叫 [**ISpatialAudioClient：： IsAudioObjectFormatSupported**](/windows/desktop/api/spatialaudioclient/nf-spatialaudioclient-ispatialaudioclient-isaudioobjectformatsupported) ，以確保支援您所使用的音訊格式。 建立音訊管線將用來通知應用程式是否已準備好使用音訊資料的事件。

呼叫 [**ISpatialAudioClient：： GetMaxDynamicObjectCount**](/windows/desktop/api/spatialaudioclient/nf-spatialaudioclient-ispatialaudioclient-getmaxdynamicobjectcount) ，以取出系統支援的動態物件數目。 如果這個呼叫傳回0，則表示目前的裝置上不支援或啟用動態空間音訊物件。 如需啟用空間音訊的詳細資訊，以及可用於不同空間音訊格式之動態音訊物件數目的詳細資訊，請參閱 [空間音效](spatial-sound.md)。

填入 [**SpatialAudioObjectRenderStreamActivationParams**](/windows/desktop/api/spatialaudioclient/ns-spatialaudioclient-spatialaudioobjectrenderstreamactivationparams) 結構時，請將 [ **MaxDynamicObjectCount** ] 欄位設定為您的應用程式將使用的動態物件最大數目。

呼叫 [**ISpatialAudioClient：： ActivateSpatialAudioStream**](/windows/desktop/api/spatialaudioclient/nf-spatialaudioclient-ispatialaudioclient-activatespatialaudiostream) 來啟動資料流程。


```C++
// Activate ISpatialAudioClient on the desired audio-device 
Microsoft::WRL::ComPtr<ISpatialAudioClient> spatialAudioClient;
hr = defaultDevice->Activate(__uuidof(ISpatialAudioClient), CLSCTX_INPROC_SERVER, nullptr, (void**)&spatialAudioClient);

hr = spatialAudioClient->IsAudioObjectFormatSupported(&format);

// Create the event that will be used to signal the client for more data
HANDLE bufferCompletionEvent = CreateEvent(nullptr, FALSE, FALSE, nullptr);

UINT32 maxDynamicObjectCount;
hr = spatialAudioClient->GetMaxDynamicObjectCount(&maxDynamicObjectCount);

if (maxDynamicObjectCount == 0)
{
    // Dynamic objects are unsupported
    return;
}

// Set the maximum number of dynamic audio objects that will be used
SpatialAudioObjectRenderStreamActivationParams streamParams;
streamParams.ObjectFormat = &format;
streamParams.StaticObjectTypeMask = AudioObjectType_None;
streamParams.MinDynamicObjectCount = 0;
streamParams.MaxDynamicObjectCount = min(maxDynamicObjectCount, 4);
streamParams.Category = AudioCategory_GameEffects;
streamParams.EventHandle = bufferCompletionEvent;
streamParams.NotifyObject = nullptr;

PROPVARIANT pv;
PropVariantInit(&pv);
pv.vt = VT_BLOB;
pv.blob.cbSize = sizeof(streamParams);
pv.blob.pBlobData = (BYTE *)&streamParams;

Microsoft::WRL::ComPtr<ISpatialAudioObjectRenderStream> spatialAudioStream;;
hr = spatialAudioClient->ActivateSpatialAudioStream(&pv, __uuidof(spatialAudioStream), (void**)&spatialAudioStream);
```



以下是一些需要的應用程式特定程式碼支援此範例，此範例會動態產生隨機定位的音訊物件，並將它們儲存在向量中。


```C++
// Used for generating a vector of randomized My3DObject structs
std::vector<My3dObject> objectVector;
std::default_random_engine gen;
std::uniform_real_distribution<> pos_dist(-25, 25); // uniform distribution for random position
std::uniform_real_distribution<> vel_dist(-1, 1); // uniform distribution for random velocity
std::uniform_real_distribution<> vol_dist(0.5, 1.0); // uniform distribution for random volume
std::uniform_real_distribution<> pitch_dist(40, 400); // uniform distribution for random pitch
int spawnCounter = 0;
```



進入音訊轉譯迴圈之前，請先呼叫 [**ISpatialAudioObjectRenderStream：： Start**](/windows/win32/api/spatialaudioclient/nf-spatialaudioclient-ispatialaudioobjectrenderstreambase-start) 來指示媒體管線開始要求音訊資料。

在轉譯迴圈內，等候我們在空間音訊串流初始化時所提供的緩衝區完成事件收到信號。 在等候事件時，您應該設定合理的超時限制，例如 100 ms，因為轉譯類型或端點的任何變更都會導致該事件永遠不會收到信號。 在此情況下，您可以呼叫 [**ISpatialAudioObjectRenderStream：： Reset**](/windows/win32/api/spatialaudioclient/nf-spatialaudioclient-ispatialaudioobjectrenderstreambase-reset) 以嘗試重設空間音訊串流。

接下來，呼叫 [**ISpatialAudioObjectRenderStream：： BeginUpdatingAudioObjects**](/windows/win32/api/spatialaudioclient/nf-spatialaudioclient-ispatialaudioobjectrenderstreambase-beginupdatingaudioobjects) ，讓系統知道您即將以資料填滿音訊物件的緩衝區。 這個方法會傳回此資料流程轉譯之音訊物件的可用動態音訊物件數目和緩衝區的框架計數。

當產生計數器達到指定的值時，我們會藉由呼叫 [**ISpatialAudioObjectRenderStream：： ActivateSpatialAudioObject**](/windows/desktop/api/spatialaudioclient/nf-spatialaudioclient-ispatialaudioobjectrenderstream-activatespatialaudioobject) 來指定 [**AudioObjectType \_ dynamic**](/windows/desktop/api/spatialaudioclient/ne-spatialaudioclient-audioobjecttype)來啟用新的動態音訊物件。 如果已配置所有可用的動態音訊物件，此方法將會傳回 **SPLAUDCLNT \_ E \_ NO \_ \_ objects 物件**。 在此情況下，您可以根據應用程式特定的優先順序，選擇釋放一或多個先前啟用的音訊物件。 建立動態音訊物件之後，會將它新增至新的 **My3dObject** 結構，具有隨機化位置、速度、磁片區和頻率值，然後將其新增至使用中物件的清單。

接下來，逐一查看所有使用中的物件（在此範例中以應用程式定義的 **My3dObject** 結構表示）。 針對每個音訊物件，呼叫 [**ISpatialAudioObject：： GetBuffer**](/windows/win32/api/spatialaudioclient/nf-spatialaudioclient-ispatialaudioobjectbase-getbuffer) 來取得空間音訊物件之音訊緩衝區的指標。 這個方法也會傳回緩衝區的大小（以位元組為單位）。 Helper 方法 **WriteToAudioObjectBuffer**，用來將音訊資料填滿緩衝區。 寫入緩衝區之後，此範例會藉由呼叫 [**ISpatialAudioObject：： SetPosition**](/windows/desktop/api/spatialaudioclient/nf-spatialaudioclient-ispatialaudioobject-setposition)來更新動態音訊物件的位置。 您也可以藉由呼叫 [**SetVolume**](/windows/desktop/api/spatialaudioclient/nf-spatialaudioclient-ispatialaudioobject-setvolume)來修改音訊物件的音量。 如果您未更新物件的位置或數量，則會保留最後一次設定時的位置和磁片區。 如果已達到物件的應用程式定義存留期，則會呼叫 [**ISpatialAudioObject：： SetEndOfStream**](/windows/win32/api/spatialaudioclient/nf-spatialaudioclient-ispatialaudioobjectbase-setendofstream) ，讓音訊管線知道將不會使用此物件來寫入音訊，並將物件設定為 **nullptr** 以釋出其資源。

將資料寫入所有音訊物件之後，請呼叫 [**ISpatialAudioObjectRenderStream：： EndUpdatingAudioObjects**](/windows/win32/api/spatialaudioclient/nf-spatialaudioclient-ispatialaudioobjectrenderstreambase-endupdatingaudioobjects) ，讓系統知道資料已可供轉譯。 您只能在呼叫 **BeginUpdatingAudioObjects** 和 **EndUpdatingAudioObjects** 之間呼叫 **GetBuffer** 。


```C++
// Start streaming / rendering 
hr = spatialAudioStream->Start();

do
{
    // Wait for a signal from the audio-engine to start the next processing pass
    if (WaitForSingleObject(bufferCompletionEvent, 100) != WAIT_OBJECT_0)
    {
        break;
    }

    UINT32 availableDynamicObjectCount;
    UINT32 frameCount;

    // Begin the process of sending object data and metadata
    // Get the number of active objects that can be used to send object-data
    // Get the frame count that each buffer will be filled with 
    hr = spatialAudioStream->BeginUpdatingAudioObjects(&availableDynamicObjectCount, &frameCount);

    BYTE* buffer;
    UINT32 bufferLength;

    // Spawn a new dynamic audio object every 200 iterations
    if (spawnCounter % 200 == 0 && spawnCounter < 1000)
    {
        // Activate a new dynamic audio object
        Microsoft::WRL::ComPtr<ISpatialAudioObject> audioObject;
        hr = spatialAudioStream->ActivateSpatialAudioObject(AudioObjectType::AudioObjectType_Dynamic, &audioObject);

        // If SPTLAUDCLNT_E_NO_MORE_OBJECTS is returned, there are no more available objects
        if (SUCCEEDED(hr))
        {
            // Init new struct with the new audio object.
            My3dObject obj = {
                audioObject,
                Windows::Foundation::Numerics::float3(static_cast<float>(pos_dist(gen)), static_cast<float>(pos_dist(gen)), static_cast<float>(pos_dist(gen))),
                Windows::Foundation::Numerics::float3(static_cast<float>(vel_dist(gen)), static_cast<float>(vel_dist(gen)), static_cast<float>(vel_dist(gen))),
                static_cast<float>(static_cast<float>(vol_dist(gen))),
                static_cast<float>(static_cast<float>(pitch_dist(gen))),
                format.nSamplesPerSec * 5 // 5 seconds of audio samples
            };

            objectVector.insert(objectVector.begin(), obj);
        }
    }
    spawnCounter++;

    // Loop through all dynamic audio objects
    std::vector<My3dObject>::iterator it = objectVector.begin();
    while (it != objectVector.end())
    {
        it->audioObject->GetBuffer(&buffer, &bufferLength);

        if (it->totalFrameCount >= frameCount)
        {
            // Write audio data to the buffer
            WriteToAudioObjectBuffer(reinterpret_cast<float*>(buffer), frameCount, it->frequency, format.nSamplesPerSec);

            // Update the position and volume of the audio object
            it->audioObject->SetPosition(it->position.x, it->position.y, it->position.z);
            it->position += it->velocity;
            it->audioObject->SetVolume(it->volume);

            it->totalFrameCount -= frameCount;

            ++it;
        }
        else
        {
            // If the audio object reaches its lifetime, set EndOfStream and release the object

            // Write audio data to the buffer
            WriteToAudioObjectBuffer(reinterpret_cast<float*>(buffer), it->totalFrameCount, it->frequency, format.nSamplesPerSec);

            // Set end of stream for the last buffer 
            hr = it->audioObject->SetEndOfStream(it->totalFrameCount);

            it->audioObject = nullptr; // Release the object

            it->totalFrameCount = 0;

            it = objectVector.erase(it);
        }
    }

    // Let the audio-engine know that the object data are available for processing now
    hr = spatialAudioStream->EndUpdatingAudioObjects();
} while (objectVector.size() > 0);
```



當您完成轉譯空間音訊時，請呼叫 [**ISpatialAudioObjectRenderStream：： stop**](/windows/win32/api/spatialaudioclient/nf-spatialaudioclient-ispatialaudioobjectrenderstreambase-stop)來停止空間音訊串流。 如果您不打算再次使用資料流程，請呼叫 [**ISpatialAudioObjectRenderStream：： Reset**](/windows/win32/api/spatialaudioclient/nf-spatialaudioclient-ispatialaudioobjectrenderstreambase-reset)來釋出其資源。


```C++
// Stop the stream 
hr = spatialAudioStream->Stop();

// We don't want to start again, so reset the stream to free it's resources.
hr = spatialAudioStream->Reset();

CloseHandle(bufferCompletionEvent);
```



## <a name="render-audio-using-dynamic-spatial-audio-objects-for-hrtf"></a>針對 HRTF 使用動態空間音訊物件呈現音訊

另一組 Api、 [**ISpatialAudioRenderStreamForHrtf**](/windows/win32/api/spatialaudiohrtf/nn-spatialaudiohrtf-ispatialaudioobjectrenderstreamforhrtf) 和 [**ISpatialAudioObjectForHrtf**](/windows/desktop/api/spatialaudiohrtf/nn-spatialaudiohrtf-ispatialaudioobjectforhrtf)，可讓您使用 Microsoft 的前端相對傳送函式的空間音訊， (HRTF) 來 attenuate 音效，以模擬發射器在空間中的位置（相對於一段時間可以變更）。 除了定位之外，HRTF 音訊物件還可讓您指定空間的方向、發出音效的 directivity （例如錐形或 cardioid 圖形），以及物件隨著虛擬接聽程式移近和更近的衰減模型。 請注意，只有當使用者選取耳機用 Windows Sonic 作為裝置的空間音訊引擎時，才能使用這些 HRTF 介面。 如需設定裝置以使用耳機用 Windows Sonic 的詳細資訊，請參閱[空間音效](spatial-sound.md)。

[**ISpatialAudioRenderStreamForHrtf**](/windows/win32/api/spatialaudiohrtf/nn-spatialaudiohrtf-ispatialaudioobjectrenderstreamforhrtf)和 [**ISpatialAudioObjectForHrtf**](/windows/desktop/api/spatialaudiohrtf/nn-spatialaudiohrtf-ispatialaudioobjectforhrtf) api 可讓應用程式直接明確地使用耳機用 Windows Sonic 轉譯路徑。 這些 api 不支援空間音效格式，例如 Dolby Atmos for Home Theater 或 Dolby Atmos for Headphones，也不支援透過 **音效** 控制台切換取用者控制的輸出格式，也不支援透過喇叭播放。 這些介面適用于想要使用耳機用 Windows Sonic 特定功能的 Windows Mixed Reality 應用程式 (例如，以程式設計方式指定的環境預設值和以距離為基礎的 rolloff，) 的一般內容撰寫管線之外。 大部分的遊戲和虛擬實境案例都偏好改用 [**ISpatialAudioClient**](/windows/desktop/api/spatialaudioclient/nn-spatialaudioclient-ispatialaudioclient) 。 這兩個 API 集合的執行步驟幾乎相同，因此您可以在執行時間執行這兩種技術和切換，視目前裝置上可用的功能而定。

混合現實應用程式通常會使用虛擬世界中3D 物件的位置，來指定與其相關聯之動態音訊物件的位置。 下列範例會使用簡單結構 **My3dObjectForHrtf**，來儲存代表物件所需的最少資料集。 這項資料包括 [**ISpatialAudioObjectForHrtf**](/windows/desktop/api/spatialaudiohrtf/nn-spatialaudiohrtf-ispatialaudioobjectforhrtf)的指標、物件的位置、方向、速度和音調頻率，以及儲存物件呈現音效的框架總數的值。


```C++
struct My3dObjectForHrtf
{
    Microsoft::WRL::ComPtr<ISpatialAudioObjectForHrtf> audioObject;
    Windows::Foundation::Numerics::float3 position;
    Windows::Foundation::Numerics::float3 velocity;
    float yRotationRads;
    float deltaYRotation;
    float frequency; // in Hz
    UINT totalFrameCount;
};
```



動態 HRTF 音訊物件的執行步驟與上一節所述動態音訊物件的步驟大致相同。 首先，取得音訊端點。


```C++
HRESULT hr;
Microsoft::WRL::ComPtr<IMMDeviceEnumerator> deviceEnum;
Microsoft::WRL::ComPtr<IMMDevice> defaultDevice;

hr = CoCreateInstance(__uuidof(MMDeviceEnumerator), nullptr, CLSCTX_ALL, __uuidof(IMMDeviceEnumerator), (void**)&deviceEnum);
hr = deviceEnum->GetDefaultAudioEndpoint(EDataFlow::eRender, eMultimedia, &defaultDevice);
```



接下來，初始化空間音訊串流。 藉由呼叫 [**IMMDevice：： Activate**](/windows/desktop/api/Mmdeviceapi/nf-mmdeviceapi-immdevice-activate)來取得 [**ISpatialAudioClient**](/windows/desktop/api/spatialaudioclient/nn-spatialaudioclient-ispatialaudioclient)的實例。 呼叫 [**ISpatialAudioClient：： IsAudioObjectFormatSupported**](/windows/desktop/api/spatialaudioclient/nf-spatialaudioclient-ispatialaudioclient-isaudioobjectformatsupported) ，以確保支援您所使用的音訊格式。 建立音訊管線將用來通知應用程式是否已準備好使用音訊資料的事件。

呼叫 [**ISpatialAudioClient：： GetMaxDynamicObjectCount**](/windows/desktop/api/spatialaudioclient/nf-spatialaudioclient-ispatialaudioclient-getmaxdynamicobjectcount) ，以取出系統支援的動態物件數目。 如果這個呼叫傳回0，則表示目前的裝置上不支援或啟用動態空間音訊物件。 如需啟用空間音訊的詳細資訊，以及可用於不同空間音訊格式之動態音訊物件數目的詳細資訊，請參閱 [空間音效](spatial-sound.md)。

填入 [**SpatialAudioHrtfActivationParams**](/windows/desktop/api/spatialaudiohrtf/ns-spatialaudiohrtf-spatialaudiohrtfactivationparams) 結構時，請將 [ **MaxDynamicObjectCount** ] 欄位設定為您的應用程式將使用的動態物件最大數目。 HRTF 的啟動參數支援一些額外的參數，例如 [**SpatialAudioHrtfDistanceDecay**](/windows/desktop/api/spatialaudiohrtf/ns-spatialaudiohrtf-spatialaudiohrtfdistancedecay)、 [**SpatialAudioHrtfDirectivityUnion**](/windows/desktop/api/spatialaudiohrtf/ns-spatialaudiohrtf-spatialaudiohrtfdirectivityunion)、 [**SpatialAudioHrtfEnvironmentType**](/windows/desktop/api/spatialaudiohrtf/ne-spatialaudiohrtf-spatialaudiohrtfenvironmenttype)和 [**SpatialAudioHrtfOrientation**](spatialaudiohrtforientation.md)，其會為從資料流程建立的新物件指定這些設定的預設值。 這些參數是選擇性的。 將欄位設定為 **nullptr** 以提供沒有預設值。

呼叫 [**ISpatialAudioClient：： ActivateSpatialAudioStream**](/windows/desktop/api/spatialaudioclient/nf-spatialaudioclient-ispatialaudioclient-activatespatialaudiostream) 來啟動資料流程。


```C++
// Activate ISpatialAudioClient on the desired audio-device 
Microsoft::WRL::ComPtr<ISpatialAudioClient> spatialAudioClient;
hr = defaultDevice->Activate(__uuidof(ISpatialAudioClient), CLSCTX_INPROC_SERVER, nullptr, (void**)&spatialAudioClient);

Microsoft::WRL::ComPtr<ISpatialAudioObjectRenderStreamForHrtf>  spatialAudioStreamForHrtf;
hr = spatialAudioClient->IsSpatialAudioStreamAvailable(__uuidof(spatialAudioStreamForHrtf), NULL);

hr = spatialAudioClient->IsAudioObjectFormatSupported(&format);

// Create the event that will be used to signal the client for more data
HANDLE bufferCompletionEvent = CreateEvent(nullptr, FALSE, FALSE, nullptr);

UINT32 maxDynamicObjectCount;
hr = spatialAudioClient->GetMaxDynamicObjectCount(&maxDynamicObjectCount);

SpatialAudioHrtfActivationParams streamParams;
streamParams.ObjectFormat = &format;
streamParams.StaticObjectTypeMask = AudioObjectType_None;
streamParams.MinDynamicObjectCount = 0;
streamParams.MaxDynamicObjectCount = min(maxDynamicObjectCount, 4);
streamParams.Category = AudioCategory_GameEffects;
streamParams.EventHandle = bufferCompletionEvent;
streamParams.NotifyObject = NULL;

SpatialAudioHrtfDistanceDecay decayModel;
decayModel.CutoffDistance = 100;
decayModel.MaxGain = 3.98f;
decayModel.MinGain = float(1.58439 * pow(10, -5));
decayModel.Type = SpatialAudioHrtfDistanceDecayType::SpatialAudioHrtfDistanceDecay_NaturalDecay;
decayModel.UnityGainDistance = 1;

streamParams.DistanceDecay = &decayModel;

SpatialAudioHrtfDirectivity directivity;
directivity.Type = SpatialAudioHrtfDirectivityType::SpatialAudioHrtfDirectivity_Cone;
directivity.Scaling = 1.0f;

SpatialAudioHrtfDirectivityCone cone;
cone.directivity = directivity;
cone.InnerAngle = 0.1f;
cone.OuterAngle = 0.2f;

SpatialAudioHrtfDirectivityUnion directivityUnion;
directivityUnion.Cone = cone;
streamParams.Directivity = &directivityUnion;

SpatialAudioHrtfEnvironmentType environment = SpatialAudioHrtfEnvironmentType::SpatialAudioHrtfEnvironment_Large;
streamParams.Environment = &environment;

SpatialAudioHrtfOrientation orientation = { 1,0,0,0,1,0,0,0,1 }; // identity matrix
streamParams.Orientation = &orientation;

PROPVARIANT pv;
PropVariantInit(&pv);
pv.vt = VT_BLOB;
pv.blob.cbSize = sizeof(streamParams);
pv.blob.pBlobData = (BYTE *)&streamParams;

hr = spatialAudioClient->ActivateSpatialAudioStream(&pv, __uuidof(spatialAudioStreamForHrtf), (void**)&spatialAudioStreamForHrtf);
```



以下是一些需要的應用程式特定程式碼支援此範例，此範例會動態產生隨機定位的音訊物件，並將它們儲存在向量中。


```C++
// Used for generating a vector of randomized My3DObject structs
std::vector<My3dObjectForHrtf> objectVector;
std::default_random_engine gen;
std::uniform_real_distribution<> pos_dist(-10, 10); // uniform distribution for random position
std::uniform_real_distribution<> vel_dist(-.02, .02); // uniform distribution for random velocity
std::uniform_real_distribution<> yRotation_dist(-3.14, 3.14); // uniform distribution for y-axis rotation
std::uniform_real_distribution<> deltaYRotation_dist(.01, .02); // uniform distribution for y-axis rotation
std::uniform_real_distribution<> pitch_dist(40, 400); // uniform distribution for random pitch

int spawnCounter = 0;
```



進入音訊轉譯迴圈之前，請先呼叫 [**ISpatialAudioObjectRenderStreamForHrtf：： Start**](/previous-versions/windows/desktop/legacy/mt779304(v=vs.85)) 來指示媒體管線開始要求音訊資料。

在轉譯迴圈內，等候我們在空間音訊串流初始化時所提供的緩衝區完成事件收到信號。 在等候事件時，您應該設定合理的超時限制，例如 100 ms，因為轉譯類型或端點的任何變更都會導致該事件永遠不會收到信號。 在此情況下，您可以呼叫 [**ISpatialAudioRenderStreamForHrtf：： Reset**](/previous-versions/windows/desktop/legacy/mt779303(v=vs.85)) 以嘗試重設空間音訊串流。

接下來，呼叫 [**ISpatialAudioRenderStreamForHrtf：： BeginUpdatingAudioObjects**](/previous-versions/windows/desktop/legacy/mt779299(v=vs.85)) ，讓系統知道您即將以資料填滿音訊物件的緩衝區。 這個方法會傳回可用動態音訊物件的數目（在此範例中不使用），以及此資料流程轉譯之音訊物件緩衝區的框架計數。

當產生計數器達到指定的值時，我們會藉由呼叫 [**ISpatialAudioRenderStreamForHrtf：： ActivateSpatialAudioObjectForHrtf**](/windows/win32/api/spatialaudiohrtf/nf-spatialaudiohrtf-ispatialaudioobjectrenderstreamforhrtf-activatespatialaudioobjectforhrtf) 來指定 [**AudioObjectType \_ dynamic**](/windows/desktop/api/spatialaudioclient/ne-spatialaudioclient-audioobjecttype)來啟用新的動態音訊物件。 如果已配置所有可用的動態音訊物件，此方法將會傳回 **SPLAUDCLNT \_ E \_ NO \_ \_ objects 物件**。 在此情況下，您可以根據應用程式特定的優先順序，選擇釋放一或多個先前啟用的音訊物件。 建立動態音訊物件之後，會將它新增至新的 **My3dObjectForHrtf** 結構，具有隨機化位置、旋轉、速度、磁片區和頻率值，然後新增至使用中物件的清單。

接下來，逐一查看所有使用中的物件（在此範例中以應用程式定義的 **My3dObjectForHrtf** 結構表示）。 針對每個音訊物件，呼叫 [**ISpatialAudioObjectForHrtf：： GetBuffer**](/previous-versions/windows/desktop/legacy/mt779271(v=vs.85)) 來取得空間音訊物件之音訊緩衝區的指標。 這個方法也會傳回緩衝區的大小（以位元組為單位）。 先前在本文中列出的 helper 方法 **WriteToAudioObjectBuffer**，可將音訊資料填滿緩衝區。 寫入緩衝區之後，此範例會藉由呼叫 [**ISpatialAudioObjectForHrtf：： SetPosition**](/windows/desktop/api/spatialaudiohrtf/nf-spatialaudiohrtf-ispatialaudioobjectforhrtf-setposition) 和 [**ISpatialAudioObjectForHrtf：： SETORIENTATION**](/windows/desktop/api/spatialaudiohrtf/nf-spatialaudiohrtf-ispatialaudioobjectforhrtf-setorientation)來更新 HRTF 音訊物件的位置和方向。 在此範例中，helper 方法（ **CalculateEmitterConeOrientationMatrix**）是用來根據3d 物件指向的方向來計算方向矩陣。 此方法的執行如下所示。 您也可以藉由呼叫 [**ISpatialAudioObjectForHrtf：： SetGain**](/windows/desktop/api/spatialaudiohrtf/nf-spatialaudiohrtf-ispatialaudioobjectforhrtf-setgain)來修改音訊物件的磁片區。 如果您未更新物件的位置、方向或數量，則會保留上一次設定時的位置、方向和磁片區。 如果已達到物件的應用程式定義存留期，則會呼叫 [**ISpatialAudioObjectForHrtf：： SetEndOfStream**](/previous-versions/windows/desktop/legacy/mt779275(v=vs.85)) ，讓音訊管線知道將不會使用此物件來寫入音訊，並將物件設定為 **nullptr** 以釋出其資源。

將資料寫入所有音訊物件之後，請呼叫 [**ISpatialAudioRenderStreamForHrtf：： EndUpdatingAudioObjects**](/previous-versions/windows/desktop/legacy/mt779300(v=vs.85)) ，讓系統知道資料已可供轉譯。 您只能在呼叫 **BeginUpdatingAudioObjects** 和 **EndUpdatingAudioObjects** 之間呼叫 **GetBuffer** 。


```C++
// Start streaming / rendering 
hr = spatialAudioStreamForHrtf->Start();

do
{
    // Wait for a signal from the audio-engine to start the next processing pass
    if (WaitForSingleObject(bufferCompletionEvent, 100) != WAIT_OBJECT_0)
    {
        break;
    }

    UINT32 availableDynamicObjectCount;
    UINT32 frameCount;

    // Begin the process of sending object data and metadata
    // Get the number of active objects that can be used to send object-data
    // Get the frame count that each buffer will be filled with 
    hr = spatialAudioStreamForHrtf->BeginUpdatingAudioObjects(&availableDynamicObjectCount, &frameCount);

    BYTE* buffer;
    UINT32 bufferLength;

    // Spawn a new dynamic audio object every 200 iterations
    if (spawnCounter % 200 == 0 && spawnCounter < 1000)
    {
        // Activate a new dynamic audio object
        Microsoft::WRL::ComPtr<ISpatialAudioObjectForHrtf> audioObject;
        hr = spatialAudioStreamForHrtf->ActivateSpatialAudioObjectForHrtf(AudioObjectType::AudioObjectType_Dynamic, &audioObject);

        // If SPTLAUDCLNT_E_NO_MORE_OBJECTS is returned, there are no more available objects
        if (SUCCEEDED(hr))
        {
            // Init new struct with the new audio object.
            My3dObjectForHrtf obj = { audioObject,
                Windows::Foundation::Numerics::float3(static_cast<float>(pos_dist(gen)), static_cast<float>(pos_dist(gen)), static_cast<float>(pos_dist(gen))),
                Windows::Foundation::Numerics::float3(static_cast<float>(vel_dist(gen)), static_cast<float>(vel_dist(gen)), static_cast<float>(vel_dist(gen))),
                static_cast<float>(static_cast<float>(yRotation_dist(gen))),
                static_cast<float>(static_cast<float>(deltaYRotation_dist(gen))),
                static_cast<float>(static_cast<float>(pitch_dist(gen))),
                format.nSamplesPerSec * 5 // 5 seconds of audio samples
            };

            objectVector.insert(objectVector.begin(), obj);
        }
    }
    spawnCounter++;

    // Loop through all dynamic audio objects
    std::vector<My3dObjectForHrtf>::iterator it = objectVector.begin();
    while (it != objectVector.end())
    {
        it->audioObject->GetBuffer(&buffer, &bufferLength);

        if (it->totalFrameCount >= frameCount)
        {
            // Write audio data to the buffer
            WriteToAudioObjectBuffer(reinterpret_cast<float*>(buffer), frameCount, it->frequency, format.nSamplesPerSec);

            // Update the position and volume of the audio object
            it->audioObject->SetPosition(it->position.x, it->position.y, it->position.z);
            it->position += it->velocity;


            Windows::Foundation::Numerics::float3 emitterDirection = Windows::Foundation::Numerics::float3(cos(it->yRotationRads), 0, sin(it->yRotationRads));
            Windows::Foundation::Numerics::float3 listenerDirection = Windows::Foundation::Numerics::float3(0, 0, 1);
            DirectX::XMFLOAT4X4 rotationMatrix;

            DirectX::XMMATRIX rotation = CalculateEmitterConeOrientationMatrix(emitterDirection, listenerDirection);
            XMStoreFloat4x4(&rotationMatrix, rotation);

            SpatialAudioHrtfOrientation orientation = {
                rotationMatrix._11, rotationMatrix._12, rotationMatrix._13,
                rotationMatrix._21, rotationMatrix._22, rotationMatrix._23,
                rotationMatrix._31, rotationMatrix._32, rotationMatrix._33
            };

            it->audioObject->SetOrientation(&orientation);
            it->yRotationRads += it->deltaYRotation;

            it->totalFrameCount -= frameCount;

            ++it;
        }
        else
        {
            // If the audio object reaches its lifetime, set EndOfStream and release the object

            // Write audio data to the buffer
            WriteToAudioObjectBuffer(reinterpret_cast<float*>(buffer), it->totalFrameCount, it->frequency, format.nSamplesPerSec);

            // Set end of stream for the last buffer 
            hr = it->audioObject->SetEndOfStream(it->totalFrameCount);

            it->audioObject = nullptr; // Release the object

            it->totalFrameCount = 0;

            it = objectVector.erase(it);
        }
    }

    // Let the audio-engine know that the object data are available for processing now
    hr = spatialAudioStreamForHrtf->EndUpdatingAudioObjects();

} while (objectVector.size() > 0);
```



當您完成轉譯空間音訊時，請呼叫 [**ISpatialAudioRenderStreamForHrtf：： stop**](/previous-versions/windows/desktop/legacy/mt779305(v=vs.85))來停止空間音訊串流。 如果您不打算再次使用資料流程，請呼叫 [**ISpatialAudioRenderStreamForHrtf：： Reset**](/previous-versions/windows/desktop/legacy/mt779303(v=vs.85))來釋出其資源。


```C++
// Stop the stream 
hr = spatialAudioStreamForHrtf->Stop();

// We don't want to start again, so reset the stream to free it's resources.
hr = spatialAudioStreamForHrtf->Reset();

CloseHandle(bufferCompletionEvent);
```



下列程式碼範例示範 **CalculateEmitterConeOrientationMatrix** helper 方法的執行方式，此方法是在上述範例中用來根據3d 物件指向的方向來計算方向矩陣。


```C++
DirectX::XMMATRIX CalculateEmitterConeOrientationMatrix(Windows::Foundation::Numerics::float3 listenerOrientationFront, Windows::Foundation::Numerics::float3 emitterDirection)
{
    DirectX::XMVECTOR vListenerDirection = DirectX::XMLoadFloat3(&listenerOrientationFront);
    DirectX::XMVECTOR vEmitterDirection = DirectX::XMLoadFloat3(&emitterDirection);
    DirectX::XMVECTOR vCross = DirectX::XMVector3Cross(vListenerDirection, vEmitterDirection);
    DirectX::XMVECTOR vDot = DirectX::XMVector3Dot(vListenerDirection, vEmitterDirection);
    DirectX::XMVECTOR vAngle = DirectX::XMVectorACos(vDot);
    float angle = DirectX::XMVectorGetX(vAngle);

    // The angle must be non-zero
    if (fabsf(angle) > FLT_EPSILON)
    {
        // And less than PI
        if (fabsf(angle) < DirectX::XM_PI)
        {
            return DirectX::XMMatrixRotationAxis(vCross, angle);
        }

        // If equal to PI, find any other non-collinear vector to generate the perpendicular vector to rotate about
        else
        {
            DirectX::XMFLOAT3 vector = { 1.0f, 1.0f, 1.0f };
            if (listenerOrientationFront.x != 0.0f)
            {
                vector.x = -listenerOrientationFront.x;
            }
            else if (listenerOrientationFront.y != 0.0f)
            {
                vector.y = -listenerOrientationFront.y;
            }
            else // if (_listenerOrientationFront.z != 0.0f)
            {
                vector.z = -listenerOrientationFront.z;
            }
            DirectX::XMVECTOR vVector = DirectX::XMLoadFloat3(&vector);
            vVector = DirectX::XMVector3Normalize(vVector);
            vCross = DirectX::XMVector3Cross(vVector, vEmitterDirection);
            return DirectX::XMMatrixRotationAxis(vCross, angle);
        }
    }

    // If the angle is zero, use an identity matrix
    return DirectX::XMMatrixIdentity();
}
```



## <a name="related-topics"></a>相關主題

<dl> <dt>

[空間音效](spatial-sound.md)
</dt> <dt>

[**ISpatialAudioClient**](/windows/desktop/api/spatialaudioclient/nn-spatialaudioclient-ispatialaudioclient)
</dt> <dt>

[**ISpatialAudioObject**](/windows/desktop/api/spatialaudioclient/nn-spatialaudioclient-ispatialaudioobject)
</dt> </dl>

 

 
