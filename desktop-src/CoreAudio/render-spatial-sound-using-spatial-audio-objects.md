---
description: 本文提供一些簡單的範例，說明如何使用靜態空間音訊物件、動態空間音訊物件，以及使用 Microsoft 前端相對傳送函式的空間音訊物件 (HRTF) 來執行空間音效。
ms.assetid: C99C342E-0BD9-486A-92AA-F8DCB72C1B00
title: 使用空間音訊物件呈現空間音效
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: cd541026aa3e144ec8333c8ac045a17970735f17
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/07/2021
ms.locfileid: "103688951"
---
# <a name="render-spatial-sound-using-spatial-audio-objects"></a><span data-ttu-id="e15e1-103">使用空間音訊物件呈現空間音效</span><span class="sxs-lookup"><span data-stu-id="e15e1-103">Render Spatial Sound Using Spatial Audio Objects</span></span>

<span data-ttu-id="e15e1-104">本文提供一些簡單的範例，說明如何使用靜態空間音訊物件、動態空間音訊物件，以及使用 Microsoft 前端相對傳送函式的空間音訊物件 (HRTF) 來執行空間音效。</span><span class="sxs-lookup"><span data-stu-id="e15e1-104">This article presents some simple examples that illustrate how to implement spatial sound using static spatial audio objects, dynamic spatial audio objects, and spatial audio objects that use Microsoft's Head Relative Transfer Function (HRTF).</span></span> <span data-ttu-id="e15e1-105">上述三項技術的執行步驟都非常類似，而且本文針對每個技術提供類似的結構化程式碼範例。</span><span class="sxs-lookup"><span data-stu-id="e15e1-105">The implementation steps for all three of these techniques are very similar and this article provides a similarly structured code example for each technique.</span></span> <span data-ttu-id="e15e1-106">如需真實世界空間音訊實作為的完整端對端範例，請參閱 [Microsoft 空間音效範例 github 存放庫](https://github.com/Microsoft/Xbox-ATG-Samples/tree/master/UWPSamples/Audio)。</span><span class="sxs-lookup"><span data-stu-id="e15e1-106">For complete end-to-end examples of real-world spatial audio implementations, see [Microsoft Spatial Sound samples github repository](https://github.com/Microsoft/Xbox-ATG-Samples/tree/master/UWPSamples/Audio).</span></span> <span data-ttu-id="e15e1-107">如需 Windows Sonic 的總覽，請參閱適用于 Xbox 和 Windows 上空間音效支援的 Microsoft 平台層級解決方案，請參閱 [空間音效](spatial-sound.md)。</span><span class="sxs-lookup"><span data-stu-id="e15e1-107">For an overview of Windows Sonic, Microsoft’s platform-level solution for spatial sound support on Xbox and Windows, see [Spatial Sound](spatial-sound.md).</span></span>

## <a name="render-audio-using-static-spatial-audio-objects"></a><span data-ttu-id="e15e1-108">使用靜態空間音訊物件呈現音訊</span><span class="sxs-lookup"><span data-stu-id="e15e1-108">Render audio using static spatial audio objects</span></span>

<span data-ttu-id="e15e1-109">靜態音訊物件是用來呈現音效至 [**AudioObjectType**](/windows/desktop/api/spatialaudioclient/ne-spatialaudioclient-audioobjecttype) 列舉中所定義之18個靜態音訊通道的其中一個。</span><span class="sxs-lookup"><span data-stu-id="e15e1-109">A static audio object is used to render sound to one of 18 static audio channels defined in the [**AudioObjectType**](/windows/desktop/api/spatialaudioclient/ne-spatialaudioclient-audioobjecttype) enumeration.</span></span> <span data-ttu-id="e15e1-110">每個通道都是在不隨著時間移動的固定點上的實際或虛擬化喇叭。</span><span class="sxs-lookup"><span data-stu-id="e15e1-110">Each of these channels represents a real or virtualized speaker at a fixed point in space that does not move over time.</span></span> <span data-ttu-id="e15e1-111">特定裝置上可用的靜態通道取決於所使用的空間音效格式。</span><span class="sxs-lookup"><span data-stu-id="e15e1-111">The static channels that are available on a particular device depend on the spatial sound format being used.</span></span> <span data-ttu-id="e15e1-112">如需支援的格式清單及其通道計數，請參閱 [空間音效](spatial-sound.md)。</span><span class="sxs-lookup"><span data-stu-id="e15e1-112">For a list of the supported formats and their channel counts, see [Spatial Sound](spatial-sound.md).</span></span>

<span data-ttu-id="e15e1-113">當您初始化空間音訊串流時，您必須指定串流將使用的可用靜態通道。</span><span class="sxs-lookup"><span data-stu-id="e15e1-113">When you initialize a spatial audio stream, you must specify which of the available static channels the stream will use.</span></span> <span data-ttu-id="e15e1-114">下列範例常數定義可以用來指定常見的喇叭設定，並取得每個設定的可用通道數目。</span><span class="sxs-lookup"><span data-stu-id="e15e1-114">The following example constant definitions can be used to specify common speaker configurations and get the number of channels available for each one.</span></span>


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



<span data-ttu-id="e15e1-115">轉譯空間音訊的第一個步驟是取得音訊資料將傳送至的音訊端點。</span><span class="sxs-lookup"><span data-stu-id="e15e1-115">The first step in rendering spatial audio is to get the audio endpoint to which audio data will be sent.</span></span> <span data-ttu-id="e15e1-116">建立 [**MMDeviceEnumerator**](/windows/desktop/api/Mmdeviceapi/nn-mmdeviceapi-immdeviceenumerator) 的實例，並呼叫 [**GetDefaultAudioEndpoint**](/windows/desktop/api/Mmdeviceapi/nf-mmdeviceapi-immdeviceenumerator-getdefaultaudioendpoint) 以取得預設音訊轉譯裝置。</span><span class="sxs-lookup"><span data-stu-id="e15e1-116">Create an instance of [**MMDeviceEnumerator**](/windows/desktop/api/Mmdeviceapi/nn-mmdeviceapi-immdeviceenumerator) and call [**GetDefaultAudioEndpoint**](/windows/desktop/api/Mmdeviceapi/nf-mmdeviceapi-immdeviceenumerator-getdefaultaudioendpoint) to get the default audio render device.</span></span>


```C++
HRESULT hr;
Microsoft::WRL::ComPtr<IMMDeviceEnumerator> deviceEnum;
Microsoft::WRL::ComPtr<IMMDevice> defaultDevice;

hr = CoCreateInstance(__uuidof(MMDeviceEnumerator), nullptr, CLSCTX_ALL, __uuidof(IMMDeviceEnumerator), (void**)&deviceEnum);
hr = deviceEnum->GetDefaultAudioEndpoint(EDataFlow::eRender, eMultimedia, &defaultDevice);
```



<span data-ttu-id="e15e1-117">當您建立空間音訊串流時，您必須提供 [WAVEFORMATEX](../medfound/mf-mt-audio-prefer-waveformatex-attribute.md) 結構，以指定資料流程將使用的音訊格式。</span><span class="sxs-lookup"><span data-stu-id="e15e1-117">When you create a spatial audio stream, you must specify the audio format the stream will use by providing a [WAVEFORMATEX](../medfound/mf-mt-audio-prefer-waveformatex-attribute.md) structure.</span></span> <span data-ttu-id="e15e1-118">如果您是從檔案播放音訊，格式通常會由音訊檔案格式決定。</span><span class="sxs-lookup"><span data-stu-id="e15e1-118">If you are playing back audio from a file, the format is typically determined by the audio file format.</span></span> <span data-ttu-id="e15e1-119">此範例使用 mono、32位、48Hz 格式。</span><span class="sxs-lookup"><span data-stu-id="e15e1-119">This example uses a mono, 32-bit, 48Hz format.</span></span>


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



<span data-ttu-id="e15e1-120">轉譯空間音訊的下一步是初始化空間音訊串流。</span><span class="sxs-lookup"><span data-stu-id="e15e1-120">The next step in rendering spatial audio is to initialize a spatial audio stream.</span></span> <span data-ttu-id="e15e1-121">首先，藉由呼叫 [**IMMDevice：： Activate**](/windows/desktop/api/Mmdeviceapi/nf-mmdeviceapi-immdevice-activate)來取得 [**ISpatialAudioClient**](/windows/desktop/api/spatialaudioclient/nn-spatialaudioclient-ispatialaudioclient)的實例。</span><span class="sxs-lookup"><span data-stu-id="e15e1-121">First, get an instance of [**ISpatialAudioClient**](/windows/desktop/api/spatialaudioclient/nn-spatialaudioclient-ispatialaudioclient) by calling [**IMMDevice::Activate**](/windows/desktop/api/Mmdeviceapi/nf-mmdeviceapi-immdevice-activate).</span></span> <span data-ttu-id="e15e1-122">呼叫 [**ISpatialAudioClient：： IsAudioObjectFormatSupported**](/windows/desktop/api/spatialaudioclient/nf-spatialaudioclient-ispatialaudioclient-isaudioobjectformatsupported) ，以確保支援您所使用的音訊格式。</span><span class="sxs-lookup"><span data-stu-id="e15e1-122">Call [**ISpatialAudioClient::IsAudioObjectFormatSupported**](/windows/desktop/api/spatialaudioclient/nf-spatialaudioclient-ispatialaudioclient-isaudioobjectformatsupported) to make sure that the audio format you are using is supported.</span></span> <span data-ttu-id="e15e1-123">建立音訊管線將用來通知應用程式是否已準備好使用音訊資料的事件。</span><span class="sxs-lookup"><span data-stu-id="e15e1-123">Create an event that the audio pipeline will use to notify the app that it is ready for more audio data.</span></span>

<span data-ttu-id="e15e1-124">填入將用來初始化空間音訊串流的 [**SpatialAudioObjectRenderStreamActivationParams**](/windows/desktop/api/spatialaudioclient/ns-spatialaudioclient-spatialaudioobjectrenderstreamactivationparams) 結構。</span><span class="sxs-lookup"><span data-stu-id="e15e1-124">Populate a [**SpatialAudioObjectRenderStreamActivationParams**](/windows/desktop/api/spatialaudioclient/ns-spatialaudioclient-spatialaudioobjectrenderstreamactivationparams) structure that will be used to initialize the spatial audio stream.</span></span> <span data-ttu-id="e15e1-125">在此範例中， **StaticObjectTypeMask** 欄位設定為本文先前定義的 **ChannelMask \_ 身歷聲** 常數，表示音訊串流只能使用 front 右邊和左方通道。</span><span class="sxs-lookup"><span data-stu-id="e15e1-125">In this example, the **StaticObjectTypeMask** field is set to the **ChannelMask\_Stereo** constant defined previously in this article, meaning that only the front right and left channels can be used by the audio stream.</span></span> <span data-ttu-id="e15e1-126">因為這個範例只會使用靜態音訊物件和沒有動態物件，所以 **MaxDynamicObjectCount** 欄位會設定為0。</span><span class="sxs-lookup"><span data-stu-id="e15e1-126">Because this example uses only static audio objects and no dynamic objects, the **MaxDynamicObjectCount** field is set to 0.</span></span> <span data-ttu-id="e15e1-127">[ **類別目錄** ] 欄位設定為 [ [**音訊 \_ 串流 \_ 類別**](/windows/desktop/api/audiosessiontypes/ne-audiosessiontypes-audio_stream_category) ] 列舉的成員，其定義系統如何與其他音訊來源混合此資料流程的音效。</span><span class="sxs-lookup"><span data-stu-id="e15e1-127">The **Category** field is set to a member of the [**AUDIO\_STREAM\_CATEGORY**](/windows/desktop/api/audiosessiontypes/ne-audiosessiontypes-audio_stream_category) enumeration, which defines how the system mixes the sound from this stream with other audio sources.</span></span>

<span data-ttu-id="e15e1-128">呼叫 [**ISpatialAudioClient：： ActivateSpatialAudioStream**](/windows/desktop/api/spatialaudioclient/nf-spatialaudioclient-ispatialaudioclient-activatespatialaudiostream) 來啟動資料流程。</span><span class="sxs-lookup"><span data-stu-id="e15e1-128">Call [**ISpatialAudioClient::ActivateSpatialAudioStream**](/windows/desktop/api/spatialaudioclient/nf-spatialaudioclient-ispatialaudioclient-activatespatialaudiostream) to activate the stream.</span></span>


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
> <span data-ttu-id="e15e1-129">在 Xbox One 開發工具組上使用 [**ISpatialAudioClient**](/windows/desktop/api/spatialaudioclient/nn-spatialaudioclient-ispatialaudioclient) 介面時 (XDK) 標題，您必須先呼叫 **EnableSpatialAudio** ，然後再呼叫 [**IMMDeviceEnumerator：： EnumAudioEndpoints**](/windows/desktop/api/Mmdeviceapi/nf-mmdeviceapi-immdeviceenumerator-enumaudioendpoints) 或 [**IMMDeviceEnumerator：： GetDefaultAudioEndpoint**](/windows/desktop/api/Mmdeviceapi/nf-mmdeviceapi-immdeviceenumerator-getdefaultaudioendpoint)。</span><span class="sxs-lookup"><span data-stu-id="e15e1-129">When using the [**ISpatialAudioClient**](/windows/desktop/api/spatialaudioclient/nn-spatialaudioclient-ispatialaudioclient) interfaces on an Xbox One Development Kit (XDK) title, you must first call **EnableSpatialAudio** before calling [**IMMDeviceEnumerator::EnumAudioEndpoints**](/windows/desktop/api/Mmdeviceapi/nf-mmdeviceapi-immdeviceenumerator-enumaudioendpoints) or [**IMMDeviceEnumerator::GetDefaultAudioEndpoint**](/windows/desktop/api/Mmdeviceapi/nf-mmdeviceapi-immdeviceenumerator-getdefaultaudioendpoint).</span></span> <span data-ttu-id="e15e1-130">若未這麼做，將會導致 \_ 從啟動的呼叫傳回電子 NOINTERFACE 錯誤。</span><span class="sxs-lookup"><span data-stu-id="e15e1-130">Failure to do so will result in an E\_NOINTERFACE error being returned from the call to Activate.</span></span> <span data-ttu-id="e15e1-131">**EnableSpatialAudio** 僅適用于 XDK 標題，不需要針對 Xbox One 上執行的通用 Windows 平臺應用程式，或任何非 Xbox One 裝置呼叫。</span><span class="sxs-lookup"><span data-stu-id="e15e1-131">**EnableSpatialAudio** is only available for XDK titles, and does not need to be called for Universal Windows Platform apps running on Xbox One, nor for any non-Xbox One devices.</span></span>

 

<span data-ttu-id="e15e1-132">宣告將用來將音訊資料寫入靜態通道的 [**ISpatialAudioObject**](/windows/desktop/api/spatialaudioclient/nn-spatialaudioclient-ispatialaudioobject) 指標。</span><span class="sxs-lookup"><span data-stu-id="e15e1-132">Declare a pointer for an [**ISpatialAudioObject**](/windows/desktop/api/spatialaudioclient/nn-spatialaudioclient-ispatialaudioobject) that will be used to write audio data to a static channel.</span></span> <span data-ttu-id="e15e1-133">一般的應用程式會針對 **StaticObjectTypeMask** 欄位中所指定的每個通道使用物件。</span><span class="sxs-lookup"><span data-stu-id="e15e1-133">Typical apps will use an object for each channel specified in the **StaticObjectTypeMask** field.</span></span> <span data-ttu-id="e15e1-134">為了簡單起見，此範例只會使用單一靜態音訊物件。</span><span class="sxs-lookup"><span data-stu-id="e15e1-134">For simplicity, this example only uses a single static audio object.</span></span>


```C++
// In this simple example, one object will be rendered
Microsoft::WRL::ComPtr<ISpatialAudioObject> audioObjectFrontLeft;
```



<span data-ttu-id="e15e1-135">進入音訊轉譯迴圈之前，請先呼叫 [**ISpatialAudioObjectRenderStream：： Start**](/windows/win32/api/spatialaudioclient/nf-spatialaudioclient-ispatialaudioobjectrenderstreambase-start) 來指示媒體管線開始要求音訊資料。</span><span class="sxs-lookup"><span data-stu-id="e15e1-135">Before entering the audio render loop, call [**ISpatialAudioObjectRenderStream::Start**](/windows/win32/api/spatialaudioclient/nf-spatialaudioclient-ispatialaudioobjectrenderstreambase-start) to instruct the media pipeline to begin requesting audio data.</span></span> <span data-ttu-id="e15e1-136">此範例會使用計數器，在5秒後停止轉譯音訊。</span><span class="sxs-lookup"><span data-stu-id="e15e1-136">This example uses a counter to stop the rendering of audio after 5 seconds.</span></span>

<span data-ttu-id="e15e1-137">在轉譯迴圈內，等候空間音訊串流初始化時所提供的緩衝區完成事件，以發出信號。</span><span class="sxs-lookup"><span data-stu-id="e15e1-137">Inside the render loop, wait for the buffer completion event, provided when the spatial audio stream was initialized, to be signaled.</span></span> <span data-ttu-id="e15e1-138">在等候事件時，您應該設定合理的超時限制，例如 100 ms，因為轉譯類型或端點的任何變更都會導致該事件永遠不會收到信號。</span><span class="sxs-lookup"><span data-stu-id="e15e1-138">You should set a reasonable timeout limit, like 100 ms, when waiting for the event because any change to the render type or endpoint will cause that event to never be signaled.</span></span> <span data-ttu-id="e15e1-139">在此情況下，您可以呼叫 [**ISpatialAudioObjectRenderStream：： Reset**](/windows/win32/api/spatialaudioclient/nf-spatialaudioclient-ispatialaudioobjectrenderstreambase-reset) 以嘗試重設空間音訊串流。</span><span class="sxs-lookup"><span data-stu-id="e15e1-139">In this case, you can call [**ISpatialAudioObjectRenderStream::Reset**](/windows/win32/api/spatialaudioclient/nf-spatialaudioclient-ispatialaudioobjectrenderstreambase-reset) to attempt to reset the spatial audio stream.</span></span>

<span data-ttu-id="e15e1-140">接下來，呼叫 [**ISpatialAudioObjectRenderStream：： BeginUpdatingAudioObjects**](/windows/win32/api/spatialaudioclient/nf-spatialaudioclient-ispatialaudioobjectrenderstreambase-beginupdatingaudioobjects) ，讓系統知道您即將以資料填滿音訊物件的緩衝區。</span><span class="sxs-lookup"><span data-stu-id="e15e1-140">Next, call [**ISpatialAudioObjectRenderStream::BeginUpdatingAudioObjects**](/windows/win32/api/spatialaudioclient/nf-spatialaudioclient-ispatialaudioobjectrenderstreambase-beginupdatingaudioobjects) to let the system know that you are about to fill the audio objects' buffers with data.</span></span> <span data-ttu-id="e15e1-141">這個方法會傳回可用動態音訊物件的數目（在此範例中不使用），以及此資料流程轉譯之音訊物件緩衝區的框架計數。</span><span class="sxs-lookup"><span data-stu-id="e15e1-141">This method returns the number of available dynamic audio objects, not used in this example, and the frame count of the buffer for audio objects rendered by this stream.</span></span>

<span data-ttu-id="e15e1-142">如果尚未建立靜態空間音訊物件，請呼叫 [**ISpatialAudioObjectRenderStream：： ActivateSpatialAudioObject**](/windows/desktop/api/spatialaudioclient/nf-spatialaudioclient-ispatialaudioobjectrenderstream-activatespatialaudioobject)來建立一個或多個，並從 [**AudioObjectType**](/windows/desktop/api/spatialaudioclient/ne-spatialaudioclient-audioobjecttype) 列舉中傳遞值，指出物件音訊呈現的靜態通道。</span><span class="sxs-lookup"><span data-stu-id="e15e1-142">If a static spatial audio object has not yet been created, create one or more by calling [**ISpatialAudioObjectRenderStream::ActivateSpatialAudioObject**](/windows/desktop/api/spatialaudioclient/nf-spatialaudioclient-ispatialaudioobjectrenderstream-activatespatialaudioobject), passing in a value from the [**AudioObjectType**](/windows/desktop/api/spatialaudioclient/ne-spatialaudioclient-audioobjecttype) enumeration indicating the static channel to which the object's audio is rendered.</span></span>

<span data-ttu-id="e15e1-143">接下來，呼叫 [**ISpatialAudioObject：： GetBuffer**](/windows/win32/api/spatialaudioclient/nf-spatialaudioclient-ispatialaudioobjectbase-getbuffer) 取得空間音訊物件之音訊緩衝區的指標。</span><span class="sxs-lookup"><span data-stu-id="e15e1-143">Next, call [**ISpatialAudioObject::GetBuffer**](/windows/win32/api/spatialaudioclient/nf-spatialaudioclient-ispatialaudioobjectbase-getbuffer) to get a pointer to the spatial audio object's audio buffer.</span></span> <span data-ttu-id="e15e1-144">這個方法也會傳回緩衝區的大小（以位元組為單位）。</span><span class="sxs-lookup"><span data-stu-id="e15e1-144">This method also returns the size of the buffer, in bytes.</span></span> <span data-ttu-id="e15e1-145">此範例使用 helper 方法 **WriteToAudioObjectBuffer**，以音訊資料填滿緩衝區。</span><span class="sxs-lookup"><span data-stu-id="e15e1-145">This example uses a helper method, **WriteToAudioObjectBuffer**, to fill the buffer with audio data.</span></span> <span data-ttu-id="e15e1-146">本文稍後會顯示這個方法。</span><span class="sxs-lookup"><span data-stu-id="e15e1-146">This method is shown later in this article.</span></span> <span data-ttu-id="e15e1-147">寫入緩衝區之後，此範例會檢查是否已達到物件的5秒存留期，如果是，則會呼叫 [**ISpatialAudioObject：： SetEndOfStream**](/windows/win32/api/spatialaudioclient/nf-spatialaudioclient-ispatialaudioobjectbase-setendofstream) ，讓音訊管線知道將不會再使用這個物件來撰寫音訊，並將物件設定為 **nullptr** 來釋出其資源。</span><span class="sxs-lookup"><span data-stu-id="e15e1-147">After writing to the buffer, the example checks to see if the 5 second lifetime of the object has been reached, and if so, [**ISpatialAudioObject::SetEndOfStream**](/windows/win32/api/spatialaudioclient/nf-spatialaudioclient-ispatialaudioobjectbase-setendofstream) is called to let the audio pipeline know that no more audio will be written using this object and the object is set to **nullptr** to free up its resources.</span></span>

<span data-ttu-id="e15e1-148">將資料寫入所有音訊物件之後，請呼叫 [**ISpatialAudioObjectRenderStream：： EndUpdatingAudioObjects**](/windows/win32/api/spatialaudioclient/nf-spatialaudioclient-ispatialaudioobjectrenderstreambase-endupdatingaudioobjects) ，讓系統知道資料已可供轉譯。</span><span class="sxs-lookup"><span data-stu-id="e15e1-148">After writing data to all of your audio objects, call [**ISpatialAudioObjectRenderStream::EndUpdatingAudioObjects**](/windows/win32/api/spatialaudioclient/nf-spatialaudioclient-ispatialaudioobjectrenderstreambase-endupdatingaudioobjects) to let the system know the data is ready for rendering.</span></span> <span data-ttu-id="e15e1-149">您只能在呼叫 **BeginUpdatingAudioObjects** 和 **EndUpdatingAudioObjects** 之間呼叫 **GetBuffer** 。</span><span class="sxs-lookup"><span data-stu-id="e15e1-149">You can only call **GetBuffer** in between a call to **BeginUpdatingAudioObjects** and **EndUpdatingAudioObjects**.</span></span>


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



<span data-ttu-id="e15e1-150">當您完成轉譯空間音訊時，請呼叫 [**ISpatialAudioObjectRenderStream：： stop**](/windows/win32/api/spatialaudioclient/nf-spatialaudioclient-ispatialaudioobjectrenderstreambase-stop)來停止空間音訊串流。</span><span class="sxs-lookup"><span data-stu-id="e15e1-150">When you are done rendering spatial audio, stop the spatial audio stream by calling [**ISpatialAudioObjectRenderStream::Stop**](/windows/win32/api/spatialaudioclient/nf-spatialaudioclient-ispatialaudioobjectrenderstreambase-stop).</span></span> <span data-ttu-id="e15e1-151">如果您不打算再次使用資料流程，請呼叫 [**ISpatialAudioObjectRenderStream：： Reset**](/windows/win32/api/spatialaudioclient/nf-spatialaudioclient-ispatialaudioobjectrenderstreambase-reset)來釋出其資源。</span><span class="sxs-lookup"><span data-stu-id="e15e1-151">If you are not going to use the stream again, free its resources by calling [**ISpatialAudioObjectRenderStream::Reset**](/windows/win32/api/spatialaudioclient/nf-spatialaudioclient-ispatialaudioobjectrenderstreambase-reset).</span></span>


```C++
// Stop the stream
hr = spatialAudioStream->Stop();

// Don't want to start again, so reset the stream to free its resources
hr = spatialAudioStream->Reset();

CloseHandle(bufferCompletionEvent);
```



<span data-ttu-id="e15e1-152">**WriteToAudioObjectBuffer** helper 方法會寫入樣本的完整緩衝區或應用程式定義的時間限制所指定的剩餘樣本數。</span><span class="sxs-lookup"><span data-stu-id="e15e1-152">The **WriteToAudioObjectBuffer** helper method writes either a full buffer of samples or the number of remaining samples specified by our app-defined time limit.</span></span> <span data-ttu-id="e15e1-153">您也可以根據來源音訊檔案中剩餘的樣本數，判斷這一點。</span><span class="sxs-lookup"><span data-stu-id="e15e1-153">This could also be determined, for example, by the number of samples remaining in a source audio file.</span></span> <span data-ttu-id="e15e1-154">會產生簡單的 sin wave，以 *頻率* 輸入參數來調整的頻率，並寫入緩衝區。</span><span class="sxs-lookup"><span data-stu-id="e15e1-154">A simple sin wave, the frequency of which is scaled by the *frequency* input parameter, is generated and written to the buffer.</span></span>


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



## <a name="render-audio-using-dynamic-spatial-audio-objects"></a><span data-ttu-id="e15e1-155">使用動態空間音訊物件呈現音訊</span><span class="sxs-lookup"><span data-stu-id="e15e1-155">Render audio using dynamic spatial audio objects</span></span>

<span data-ttu-id="e15e1-156">動態物件可讓您從空間中的任意位置（相對於使用者）呈現音訊。</span><span class="sxs-lookup"><span data-stu-id="e15e1-156">Dynamic objects allow you to render audio from an arbitrary position in space, relative to the user.</span></span> <span data-ttu-id="e15e1-157">動態音訊物件的位置和數量可以隨著時間變更。</span><span class="sxs-lookup"><span data-stu-id="e15e1-157">The position and volume of a dynamic audio object can be changed over time.</span></span> <span data-ttu-id="e15e1-158">遊戲通常會使用遊戲世界中3D 物件的位置來指定動態音訊物件與其相關聯的位置。</span><span class="sxs-lookup"><span data-stu-id="e15e1-158">Games will typically use the position of a 3D object in the game world to specify the position of the dynamic audio object associated with it.</span></span> <span data-ttu-id="e15e1-159">下列範例會使用簡單結構 **My3dObject**，來儲存代表物件所需的最少資料集。</span><span class="sxs-lookup"><span data-stu-id="e15e1-159">The following example will use a simple structure, **My3dObject**, to store the minimum set of data needed to represent an object.</span></span> <span data-ttu-id="e15e1-160">這項資料包括 [**ISpatialAudioObject**](/windows/desktop/api/spatialaudioclient/nn-spatialaudioclient-ispatialaudioobject)的指標、物件的位置、速度、數量和音調頻率，以及儲存物件呈現音效的框架總數的值。</span><span class="sxs-lookup"><span data-stu-id="e15e1-160">This data includes a pointer to an [**ISpatialAudioObject**](/windows/desktop/api/spatialaudioclient/nn-spatialaudioclient-ispatialaudioobject), the position, velocity, volume, and tone frequency for the object, and a value that stores the total number of frames for which the object should render sound.</span></span>


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



<span data-ttu-id="e15e1-161">動態音訊物件的執行步驟與上述靜態音訊物件的步驟大致相同。</span><span class="sxs-lookup"><span data-stu-id="e15e1-161">The implementation steps for dynamic audio objects is largely the same as the steps for static audio objects described above.</span></span> <span data-ttu-id="e15e1-162">首先，取得音訊端點。</span><span class="sxs-lookup"><span data-stu-id="e15e1-162">First, get an audio endpoint.</span></span>


```C++
HRESULT hr;
Microsoft::WRL::ComPtr<IMMDeviceEnumerator> deviceEnum;
Microsoft::WRL::ComPtr<IMMDevice> defaultDevice;

hr = CoCreateInstance(__uuidof(MMDeviceEnumerator), nullptr, CLSCTX_ALL, __uuidof(IMMDeviceEnumerator), (void**)&deviceEnum);
hr = deviceEnum->GetDefaultAudioEndpoint(EDataFlow::eRender, eMultimedia, &defaultDevice);
```



<span data-ttu-id="e15e1-163">接下來，初始化空間音訊串流。</span><span class="sxs-lookup"><span data-stu-id="e15e1-163">Next, initialize the spatial audio stream.</span></span> <span data-ttu-id="e15e1-164">藉由呼叫 [**IMMDevice：： Activate**](/windows/desktop/api/Mmdeviceapi/nf-mmdeviceapi-immdevice-activate)來取得 [**ISpatialAudioClient**](/windows/desktop/api/spatialaudioclient/nn-spatialaudioclient-ispatialaudioclient)的實例。</span><span class="sxs-lookup"><span data-stu-id="e15e1-164">Get an instance of [**ISpatialAudioClient**](/windows/desktop/api/spatialaudioclient/nn-spatialaudioclient-ispatialaudioclient) by calling [**IMMDevice::Activate**](/windows/desktop/api/Mmdeviceapi/nf-mmdeviceapi-immdevice-activate).</span></span> <span data-ttu-id="e15e1-165">呼叫 [**ISpatialAudioClient：： IsAudioObjectFormatSupported**](/windows/desktop/api/spatialaudioclient/nf-spatialaudioclient-ispatialaudioclient-isaudioobjectformatsupported) ，以確保支援您所使用的音訊格式。</span><span class="sxs-lookup"><span data-stu-id="e15e1-165">Call [**ISpatialAudioClient::IsAudioObjectFormatSupported**](/windows/desktop/api/spatialaudioclient/nf-spatialaudioclient-ispatialaudioclient-isaudioobjectformatsupported) to make sure that the audio format you are using is supported.</span></span> <span data-ttu-id="e15e1-166">建立音訊管線將用來通知應用程式是否已準備好使用音訊資料的事件。</span><span class="sxs-lookup"><span data-stu-id="e15e1-166">Create an event that the audio pipeline will use to notify the app that it is ready for more audio data.</span></span>

<span data-ttu-id="e15e1-167">呼叫 [**ISpatialAudioClient：： GetMaxDynamicObjectCount**](/windows/desktop/api/spatialaudioclient/nf-spatialaudioclient-ispatialaudioclient-getmaxdynamicobjectcount) ，以取出系統支援的動態物件數目。</span><span class="sxs-lookup"><span data-stu-id="e15e1-167">Call [**ISpatialAudioClient::GetMaxDynamicObjectCount**](/windows/desktop/api/spatialaudioclient/nf-spatialaudioclient-ispatialaudioclient-getmaxdynamicobjectcount) to retrieve the number of dynamic objects supported by the system.</span></span> <span data-ttu-id="e15e1-168">如果這個呼叫傳回0，則表示目前的裝置上不支援或啟用動態空間音訊物件。</span><span class="sxs-lookup"><span data-stu-id="e15e1-168">If this call returns 0, then dynamic spatial audio objects are not supported or enabled on the current device.</span></span> <span data-ttu-id="e15e1-169">如需啟用空間音訊的詳細資訊，以及可用於不同空間音訊格式之動態音訊物件數目的詳細資訊，請參閱 [空間音效](spatial-sound.md)。</span><span class="sxs-lookup"><span data-stu-id="e15e1-169">For information on enabling spatial audio and for details on the number of dynamic audio objects available for different spatial audio formats, see [Spatial Sound](spatial-sound.md).</span></span>

<span data-ttu-id="e15e1-170">填入 [**SpatialAudioObjectRenderStreamActivationParams**](/windows/desktop/api/spatialaudioclient/ns-spatialaudioclient-spatialaudioobjectrenderstreamactivationparams) 結構時，請將 [ **MaxDynamicObjectCount** ] 欄位設定為您的應用程式將使用的動態物件最大數目。</span><span class="sxs-lookup"><span data-stu-id="e15e1-170">When populating the [**SpatialAudioObjectRenderStreamActivationParams**](/windows/desktop/api/spatialaudioclient/ns-spatialaudioclient-spatialaudioobjectrenderstreamactivationparams) structure, set the **MaxDynamicObjectCount** field to the maximum number of dynamic objects your app will use.</span></span>

<span data-ttu-id="e15e1-171">呼叫 [**ISpatialAudioClient：： ActivateSpatialAudioStream**](/windows/desktop/api/spatialaudioclient/nf-spatialaudioclient-ispatialaudioclient-activatespatialaudiostream) 來啟動資料流程。</span><span class="sxs-lookup"><span data-stu-id="e15e1-171">Call [**ISpatialAudioClient::ActivateSpatialAudioStream**](/windows/desktop/api/spatialaudioclient/nf-spatialaudioclient-ispatialaudioclient-activatespatialaudiostream) to activate the stream.</span></span>


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



<span data-ttu-id="e15e1-172">以下是一些需要的應用程式特定程式碼支援此範例，此範例會動態產生隨機定位的音訊物件，並將它們儲存在向量中。</span><span class="sxs-lookup"><span data-stu-id="e15e1-172">The following is some app-specific code to needed support this example, which will dynamically spawn randomly positioned audio objects and store them in a vector.</span></span>


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



<span data-ttu-id="e15e1-173">進入音訊轉譯迴圈之前，請先呼叫 [**ISpatialAudioObjectRenderStream：： Start**](/windows/win32/api/spatialaudioclient/nf-spatialaudioclient-ispatialaudioobjectrenderstreambase-start) 來指示媒體管線開始要求音訊資料。</span><span class="sxs-lookup"><span data-stu-id="e15e1-173">Before entering the audio render loop, call [**ISpatialAudioObjectRenderStream::Start**](/windows/win32/api/spatialaudioclient/nf-spatialaudioclient-ispatialaudioobjectrenderstreambase-start) to instruct the media pipeline to begin requesting audio data.</span></span>

<span data-ttu-id="e15e1-174">在轉譯迴圈內，等候我們在空間音訊串流初始化時所提供的緩衝區完成事件收到信號。</span><span class="sxs-lookup"><span data-stu-id="e15e1-174">Inside the render loop, wait for the buffer completion event we provided when the spatial audio stream was initialized to be signaled.</span></span> <span data-ttu-id="e15e1-175">在等候事件時，您應該設定合理的超時限制，例如 100 ms，因為轉譯類型或端點的任何變更都會導致該事件永遠不會收到信號。</span><span class="sxs-lookup"><span data-stu-id="e15e1-175">You should set a reasonable timeout limit, like 100 ms, when waiting for the event because any change to the render type or endpoint will cause that event to never be signaled.</span></span> <span data-ttu-id="e15e1-176">在此情況下，您可以呼叫 [**ISpatialAudioObjectRenderStream：： Reset**](/windows/win32/api/spatialaudioclient/nf-spatialaudioclient-ispatialaudioobjectrenderstreambase-reset) 以嘗試重設空間音訊串流。</span><span class="sxs-lookup"><span data-stu-id="e15e1-176">In this case, you can call [**ISpatialAudioObjectRenderStream::Reset**](/windows/win32/api/spatialaudioclient/nf-spatialaudioclient-ispatialaudioobjectrenderstreambase-reset) to attempt to reset the spatial audio stream.</span></span>

<span data-ttu-id="e15e1-177">接下來，呼叫 [**ISpatialAudioObjectRenderStream：： BeginUpdatingAudioObjects**](/windows/win32/api/spatialaudioclient/nf-spatialaudioclient-ispatialaudioobjectrenderstreambase-beginupdatingaudioobjects) ，讓系統知道您即將以資料填滿音訊物件的緩衝區。</span><span class="sxs-lookup"><span data-stu-id="e15e1-177">Next, call [**ISpatialAudioObjectRenderStream::BeginUpdatingAudioObjects**](/windows/win32/api/spatialaudioclient/nf-spatialaudioclient-ispatialaudioobjectrenderstreambase-beginupdatingaudioobjects) to let the system know that you are about to fill the audio objects' buffers with data.</span></span> <span data-ttu-id="e15e1-178">這個方法會傳回此資料流程轉譯之音訊物件的可用動態音訊物件數目和緩衝區的框架計數。</span><span class="sxs-lookup"><span data-stu-id="e15e1-178">This method returns the number of available dynamic audio objects and the frame count of the buffer for audio objects rendered by this stream.</span></span>

<span data-ttu-id="e15e1-179">當產生計數器達到指定的值時，我們會藉由呼叫 [**ISpatialAudioObjectRenderStream：： ActivateSpatialAudioObject**](/windows/desktop/api/spatialaudioclient/nf-spatialaudioclient-ispatialaudioobjectrenderstream-activatespatialaudioobject) 來指定 [**AudioObjectType \_ dynamic**](/windows/desktop/api/spatialaudioclient/ne-spatialaudioclient-audioobjecttype)來啟用新的動態音訊物件。</span><span class="sxs-lookup"><span data-stu-id="e15e1-179">Whenever the spawn counter reaches the specified value, we will activate a new dynamic audio object by calling [**ISpatialAudioObjectRenderStream::ActivateSpatialAudioObject**](/windows/desktop/api/spatialaudioclient/nf-spatialaudioclient-ispatialaudioobjectrenderstream-activatespatialaudioobject) specifying [**AudioObjectType\_Dynamic**](/windows/desktop/api/spatialaudioclient/ne-spatialaudioclient-audioobjecttype).</span></span> <span data-ttu-id="e15e1-180">如果已配置所有可用的動態音訊物件，此方法將會傳回 **SPLAUDCLNT \_ E \_ NO \_ \_ objects 物件**。</span><span class="sxs-lookup"><span data-stu-id="e15e1-180">If all available dynamic audio objects have already been allocated, this method will return **SPLAUDCLNT\_E\_NO\_MORE\_OBJECTS**.</span></span> <span data-ttu-id="e15e1-181">在此情況下，您可以根據應用程式特定的優先順序，選擇釋放一或多個先前啟用的音訊物件。</span><span class="sxs-lookup"><span data-stu-id="e15e1-181">In this case, you can choose to release one or more previously activated audio objects based on your app-specific prioritization.</span></span> <span data-ttu-id="e15e1-182">建立動態音訊物件之後，會將它新增至新的 **My3dObject** 結構，具有隨機化位置、速度、磁片區和頻率值，然後將其新增至使用中物件的清單。</span><span class="sxs-lookup"><span data-stu-id="e15e1-182">After the dynamic audio object has been created, it is added to a new **My3dObject** structure, with randomized position, velocity, volume, and frequency values, which is then added to the list of active objects.</span></span>

<span data-ttu-id="e15e1-183">接下來，逐一查看所有使用中的物件（在此範例中以應用程式定義的 **My3dObject** 結構表示）。</span><span class="sxs-lookup"><span data-stu-id="e15e1-183">Next, iterate over all of the active objects, represented in this example with the app-defined **My3dObject** structure.</span></span> <span data-ttu-id="e15e1-184">針對每個音訊物件，呼叫 [**ISpatialAudioObject：： GetBuffer**](/windows/win32/api/spatialaudioclient/nf-spatialaudioclient-ispatialaudioobjectbase-getbuffer) 來取得空間音訊物件之音訊緩衝區的指標。</span><span class="sxs-lookup"><span data-stu-id="e15e1-184">For each audio object, call [**ISpatialAudioObject::GetBuffer**](/windows/win32/api/spatialaudioclient/nf-spatialaudioclient-ispatialaudioobjectbase-getbuffer) to get a pointer to the spatial audio object's audio buffer.</span></span> <span data-ttu-id="e15e1-185">這個方法也會傳回緩衝區的大小（以位元組為單位）。</span><span class="sxs-lookup"><span data-stu-id="e15e1-185">This method also returns the size of the buffer, in bytes.</span></span> <span data-ttu-id="e15e1-186">Helper 方法 **WriteToAudioObjectBuffer**，用來將音訊資料填滿緩衝區。</span><span class="sxs-lookup"><span data-stu-id="e15e1-186">The helper method, **WriteToAudioObjectBuffer**, to fill the buffer with audio data.</span></span> <span data-ttu-id="e15e1-187">寫入緩衝區之後，此範例會藉由呼叫 [**ISpatialAudioObject：： SetPosition**](/windows/desktop/api/spatialaudioclient/nf-spatialaudioclient-ispatialaudioobject-setposition)來更新動態音訊物件的位置。</span><span class="sxs-lookup"><span data-stu-id="e15e1-187">After writing to the buffer, the example updates the position of the dynamic audio object by calling [**ISpatialAudioObject::SetPosition**](/windows/desktop/api/spatialaudioclient/nf-spatialaudioclient-ispatialaudioobject-setposition).</span></span> <span data-ttu-id="e15e1-188">您也可以藉由呼叫 [**SetVolume**](/windows/desktop/api/spatialaudioclient/nf-spatialaudioclient-ispatialaudioobject-setvolume)來修改音訊物件的音量。</span><span class="sxs-lookup"><span data-stu-id="e15e1-188">The volume of the audio object can also be modified by calling [**SetVolume**](/windows/desktop/api/spatialaudioclient/nf-spatialaudioclient-ispatialaudioobject-setvolume).</span></span> <span data-ttu-id="e15e1-189">如果您未更新物件的位置或數量，則會保留最後一次設定時的位置和磁片區。</span><span class="sxs-lookup"><span data-stu-id="e15e1-189">If you don't update the position or volume of the object, it will retain the position and volume from the last time it was set.</span></span> <span data-ttu-id="e15e1-190">如果已達到物件的應用程式定義存留期，則會呼叫 [**ISpatialAudioObject：： SetEndOfStream**](/windows/win32/api/spatialaudioclient/nf-spatialaudioclient-ispatialaudioobjectbase-setendofstream) ，讓音訊管線知道將不會使用此物件來寫入音訊，並將物件設定為 **nullptr** 以釋出其資源。</span><span class="sxs-lookup"><span data-stu-id="e15e1-190">If the object's app-defined lifetime has been reached, [**ISpatialAudioObject::SetEndOfStream**](/windows/win32/api/spatialaudioclient/nf-spatialaudioclient-ispatialaudioobjectbase-setendofstream) is called to let the audio pipeline know that no more audio will be written using this object and the object is set to **nullptr** to free up its resources.</span></span>

<span data-ttu-id="e15e1-191">將資料寫入所有音訊物件之後，請呼叫 [**ISpatialAudioObjectRenderStream：： EndUpdatingAudioObjects**](/windows/win32/api/spatialaudioclient/nf-spatialaudioclient-ispatialaudioobjectrenderstreambase-endupdatingaudioobjects) ，讓系統知道資料已可供轉譯。</span><span class="sxs-lookup"><span data-stu-id="e15e1-191">After writing data to all of your audio objects, call [**ISpatialAudioObjectRenderStream::EndUpdatingAudioObjects**](/windows/win32/api/spatialaudioclient/nf-spatialaudioclient-ispatialaudioobjectrenderstreambase-endupdatingaudioobjects) to let the system know the data is ready for rendering.</span></span> <span data-ttu-id="e15e1-192">您只能在呼叫 **BeginUpdatingAudioObjects** 和 **EndUpdatingAudioObjects** 之間呼叫 **GetBuffer** 。</span><span class="sxs-lookup"><span data-stu-id="e15e1-192">You can only call **GetBuffer** in between a call to **BeginUpdatingAudioObjects** and **EndUpdatingAudioObjects**.</span></span>


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



<span data-ttu-id="e15e1-193">當您完成轉譯空間音訊時，請呼叫 [**ISpatialAudioObjectRenderStream：： stop**](/windows/win32/api/spatialaudioclient/nf-spatialaudioclient-ispatialaudioobjectrenderstreambase-stop)來停止空間音訊串流。</span><span class="sxs-lookup"><span data-stu-id="e15e1-193">When you are done rendering spatial audio, stop the spatial audio stream by calling [**ISpatialAudioObjectRenderStream::Stop**](/windows/win32/api/spatialaudioclient/nf-spatialaudioclient-ispatialaudioobjectrenderstreambase-stop).</span></span> <span data-ttu-id="e15e1-194">如果您不打算再次使用資料流程，請呼叫 [**ISpatialAudioObjectRenderStream：： Reset**](/windows/win32/api/spatialaudioclient/nf-spatialaudioclient-ispatialaudioobjectrenderstreambase-reset)來釋出其資源。</span><span class="sxs-lookup"><span data-stu-id="e15e1-194">If you are not going to use the stream again, free its resources by calling [**ISpatialAudioObjectRenderStream::Reset**](/windows/win32/api/spatialaudioclient/nf-spatialaudioclient-ispatialaudioobjectrenderstreambase-reset).</span></span>


```C++
// Stop the stream 
hr = spatialAudioStream->Stop();

// We don't want to start again, so reset the stream to free it's resources.
hr = spatialAudioStream->Reset();

CloseHandle(bufferCompletionEvent);
```



## <a name="render-audio-using-dynamic-spatial-audio-objects-for-hrtf"></a><span data-ttu-id="e15e1-195">針對 HRTF 使用動態空間音訊物件呈現音訊</span><span class="sxs-lookup"><span data-stu-id="e15e1-195">Render audio using dynamic spatial audio objects for HRTF</span></span>

<span data-ttu-id="e15e1-196">另一組 Api、 [**ISpatialAudioRenderStreamForHrtf**](/windows/win32/api/spatialaudiohrtf/nn-spatialaudiohrtf-ispatialaudioobjectrenderstreamforhrtf) 和 [**ISpatialAudioObjectForHrtf**](/windows/desktop/api/spatialaudiohrtf/nn-spatialaudiohrtf-ispatialaudioobjectforhrtf)，可讓您使用 Microsoft 的前端相對傳送函式的空間音訊， (HRTF) 來 attenuate 音效，以模擬發射器在空間中的位置（相對於一段時間可以變更）。</span><span class="sxs-lookup"><span data-stu-id="e15e1-196">Another set of APIs, [**ISpatialAudioRenderStreamForHrtf**](/windows/win32/api/spatialaudiohrtf/nn-spatialaudiohrtf-ispatialaudioobjectrenderstreamforhrtf) and [**ISpatialAudioObjectForHrtf**](/windows/desktop/api/spatialaudiohrtf/nn-spatialaudiohrtf-ispatialaudioobjectforhrtf), enable spatial audio that uses Microsoft's Head-relative Transfer Function (HRTF) to attenuate sounds to simulate the emitter's position in space, relative to the user, which can be changed over time.</span></span> <span data-ttu-id="e15e1-197">除了定位之外，HRTF 音訊物件還可讓您指定空間的方向、發出音效的 directivity （例如錐形或 cardioid 圖形），以及物件隨著虛擬接聽程式移近和更近的衰減模型。</span><span class="sxs-lookup"><span data-stu-id="e15e1-197">In addition to position, HRTF audio objects allow you to specify an orientation in space, a directivity in which sound is emitted, such as a cone or cardioid shape, and a decay model as the object moves nearer and further from the virtual listener.</span></span> <span data-ttu-id="e15e1-198">請注意，只有當使用者選取耳機用 Windows Sonic 作為裝置的空間音訊引擎時，才能使用這些 HRTF 介面。</span><span class="sxs-lookup"><span data-stu-id="e15e1-198">Note that these HRTF interfaces are only available when the user has selected Windows Sonic for Headphones as the spatial audio engine for the device.</span></span> <span data-ttu-id="e15e1-199">如需設定裝置以使用耳機用 Windows Sonic 的詳細資訊，請參閱 [空間音效](spatial-sound.md)。</span><span class="sxs-lookup"><span data-stu-id="e15e1-199">For information on configuring a device to use Windows Sonic for Headphones, see [Spatial Sound](spatial-sound.md).</span></span>

<span data-ttu-id="e15e1-200">[**ISpatialAudioRenderStreamForHrtf**](/windows/win32/api/spatialaudiohrtf/nn-spatialaudiohrtf-ispatialaudioobjectrenderstreamforhrtf)和 [**ISpatialAudioObjectForHrtf**](/windows/desktop/api/spatialaudiohrtf/nn-spatialaudiohrtf-ispatialaudioobjectforhrtf) api 可讓應用程式直接明確地使用耳機用 Windows Sonic 轉譯路徑。</span><span class="sxs-lookup"><span data-stu-id="e15e1-200">The [**ISpatialAudioRenderStreamForHrtf**](/windows/win32/api/spatialaudiohrtf/nn-spatialaudiohrtf-ispatialaudioobjectrenderstreamforhrtf) and [**ISpatialAudioObjectForHrtf**](/windows/desktop/api/spatialaudiohrtf/nn-spatialaudiohrtf-ispatialaudioobjectforhrtf) APIs allow an application to explicitly use the Windows Sonic for Headphones render path directly.</span></span> <span data-ttu-id="e15e1-201">這些 Api 不支援空間音效格式，例如 Dolby Atmos for Home Theater 或 Dolby Atmos for Headphones，也不支援透過 **音效** 控制台切換取用者控制的輸出格式，也不支援透過喇叭播放。</span><span class="sxs-lookup"><span data-stu-id="e15e1-201">These APIs do not support spatial sound formats such as Dolby Atmos for Home Theater or Dolby Atmos for Headphones, nor consumer-controlled output format switching via the **Sound** control panel, nor playback over speakers.</span></span> <span data-ttu-id="e15e1-202">這些介面適用于想要使用耳機用 Windows Sonic 特定功能的 Windows Mixed Reality 應用程式 (例如，以程式設計方式指定的環境預設值和以距離為基礎的 rolloff，) 的一般內容撰寫管線之外。</span><span class="sxs-lookup"><span data-stu-id="e15e1-202">These interfaces are intended for use in Windows Mixed Reality applications that want to use Windows Sonic for Headphones-specific capabilities (such as environmental presets and distance-based rolloff specified programmatically, outside of typical content authoring pipelines).</span></span> <span data-ttu-id="e15e1-203">大部分的遊戲和虛擬實境案例都偏好改用 [**ISpatialAudioClient**](/windows/desktop/api/spatialaudioclient/nn-spatialaudioclient-ispatialaudioclient) 。</span><span class="sxs-lookup"><span data-stu-id="e15e1-203">Most games and virtual reality scenarios will prefer to use [**ISpatialAudioClient**](/windows/desktop/api/spatialaudioclient/nn-spatialaudioclient-ispatialaudioclient) instead.</span></span> <span data-ttu-id="e15e1-204">這兩個 API 集合的執行步驟幾乎相同，因此您可以在執行時間執行這兩種技術和切換，視目前裝置上可用的功能而定。</span><span class="sxs-lookup"><span data-stu-id="e15e1-204">The implementation steps for both API sets are almost identical, so it is possible to implement both technologies and switch at runtime depending on which feature is available on the current device.</span></span>

<span data-ttu-id="e15e1-205">混合現實應用程式通常會使用虛擬世界中3D 物件的位置，來指定與其相關聯之動態音訊物件的位置。</span><span class="sxs-lookup"><span data-stu-id="e15e1-205">Mixed-reality apps will typically use the position of a 3D object in the virtual world to specify the position of the dynamic audio object associated with it.</span></span> <span data-ttu-id="e15e1-206">下列範例會使用簡單結構 **My3dObjectForHrtf**，來儲存代表物件所需的最少資料集。</span><span class="sxs-lookup"><span data-stu-id="e15e1-206">The following example will use a simple structure, **My3dObjectForHrtf**, to store the minimum set of data needed to represent an object.</span></span> <span data-ttu-id="e15e1-207">這項資料包括 [**ISpatialAudioObjectForHrtf**](/windows/desktop/api/spatialaudiohrtf/nn-spatialaudiohrtf-ispatialaudioobjectforhrtf)的指標、物件的位置、方向、速度和音調頻率，以及儲存物件呈現音效的框架總數的值。</span><span class="sxs-lookup"><span data-stu-id="e15e1-207">This data includes a pointer to an [**ISpatialAudioObjectForHrtf**](/windows/desktop/api/spatialaudiohrtf/nn-spatialaudiohrtf-ispatialaudioobjectforhrtf), the position, orientation, velocity, and tone frequency for the object, and a value that stores the total number of frames for which the object should render sound.</span></span>


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



<span data-ttu-id="e15e1-208">動態 HRTF 音訊物件的執行步驟與上一節所述動態音訊物件的步驟大致相同。</span><span class="sxs-lookup"><span data-stu-id="e15e1-208">The implementation steps for dynamic HRTF audio objects is largely the same as the steps for dynamic audio objects described in the previous section.</span></span> <span data-ttu-id="e15e1-209">首先，取得音訊端點。</span><span class="sxs-lookup"><span data-stu-id="e15e1-209">First, get an audio endpoint.</span></span>


```C++
HRESULT hr;
Microsoft::WRL::ComPtr<IMMDeviceEnumerator> deviceEnum;
Microsoft::WRL::ComPtr<IMMDevice> defaultDevice;

hr = CoCreateInstance(__uuidof(MMDeviceEnumerator), nullptr, CLSCTX_ALL, __uuidof(IMMDeviceEnumerator), (void**)&deviceEnum);
hr = deviceEnum->GetDefaultAudioEndpoint(EDataFlow::eRender, eMultimedia, &defaultDevice);
```



<span data-ttu-id="e15e1-210">接下來，初始化空間音訊串流。</span><span class="sxs-lookup"><span data-stu-id="e15e1-210">Next, initialize the spatial audio stream.</span></span> <span data-ttu-id="e15e1-211">藉由呼叫 [**IMMDevice：： Activate**](/windows/desktop/api/Mmdeviceapi/nf-mmdeviceapi-immdevice-activate)來取得 [**ISpatialAudioClient**](/windows/desktop/api/spatialaudioclient/nn-spatialaudioclient-ispatialaudioclient)的實例。</span><span class="sxs-lookup"><span data-stu-id="e15e1-211">Get an instance of [**ISpatialAudioClient**](/windows/desktop/api/spatialaudioclient/nn-spatialaudioclient-ispatialaudioclient) by calling [**IMMDevice::Activate**](/windows/desktop/api/Mmdeviceapi/nf-mmdeviceapi-immdevice-activate).</span></span> <span data-ttu-id="e15e1-212">呼叫 [**ISpatialAudioClient：： IsAudioObjectFormatSupported**](/windows/desktop/api/spatialaudioclient/nf-spatialaudioclient-ispatialaudioclient-isaudioobjectformatsupported) ，以確保支援您所使用的音訊格式。</span><span class="sxs-lookup"><span data-stu-id="e15e1-212">Call [**ISpatialAudioClient::IsAudioObjectFormatSupported**](/windows/desktop/api/spatialaudioclient/nf-spatialaudioclient-ispatialaudioclient-isaudioobjectformatsupported) to make sure that the audio format you are using is supported.</span></span> <span data-ttu-id="e15e1-213">建立音訊管線將用來通知應用程式是否已準備好使用音訊資料的事件。</span><span class="sxs-lookup"><span data-stu-id="e15e1-213">Create an event that the audio pipeline will use to notify the app that it is ready for more audio data.</span></span>

<span data-ttu-id="e15e1-214">呼叫 [**ISpatialAudioClient：： GetMaxDynamicObjectCount**](/windows/desktop/api/spatialaudioclient/nf-spatialaudioclient-ispatialaudioclient-getmaxdynamicobjectcount) ，以取出系統支援的動態物件數目。</span><span class="sxs-lookup"><span data-stu-id="e15e1-214">Call [**ISpatialAudioClient::GetMaxDynamicObjectCount**](/windows/desktop/api/spatialaudioclient/nf-spatialaudioclient-ispatialaudioclient-getmaxdynamicobjectcount) to retrieve the number of dynamic objects supported by the system.</span></span> <span data-ttu-id="e15e1-215">如果這個呼叫傳回0，則表示目前的裝置上不支援或啟用動態空間音訊物件。</span><span class="sxs-lookup"><span data-stu-id="e15e1-215">If this call returns 0, then dynamic spatial audio objects are not supported or enabled on the current device.</span></span> <span data-ttu-id="e15e1-216">如需啟用空間音訊的詳細資訊，以及可用於不同空間音訊格式之動態音訊物件數目的詳細資訊，請參閱 [空間音效](spatial-sound.md)。</span><span class="sxs-lookup"><span data-stu-id="e15e1-216">For information on enabling spatial audio and for details on the number of dynamic audio objects available for different spatial audio formats, see [Spatial Sound](spatial-sound.md).</span></span>

<span data-ttu-id="e15e1-217">填入 [**SpatialAudioHrtfActivationParams**](/windows/desktop/api/spatialaudiohrtf/ns-spatialaudiohrtf-spatialaudiohrtfactivationparams) 結構時，請將 [ **MaxDynamicObjectCount** ] 欄位設定為您的應用程式將使用的動態物件最大數目。</span><span class="sxs-lookup"><span data-stu-id="e15e1-217">When populating the [**SpatialAudioHrtfActivationParams**](/windows/desktop/api/spatialaudiohrtf/ns-spatialaudiohrtf-spatialaudiohrtfactivationparams) structure, set the **MaxDynamicObjectCount** field to the maximum number of dynamic objects your app will use.</span></span> <span data-ttu-id="e15e1-218">HRTF 的啟動參數支援一些額外的參數，例如 [**SpatialAudioHrtfDistanceDecay**](/windows/desktop/api/spatialaudiohrtf/ns-spatialaudiohrtf-spatialaudiohrtfdistancedecay)、 [**SpatialAudioHrtfDirectivityUnion**](/windows/desktop/api/spatialaudiohrtf/ns-spatialaudiohrtf-spatialaudiohrtfdirectivityunion)、 [**SpatialAudioHrtfEnvironmentType**](/windows/desktop/api/spatialaudiohrtf/ne-spatialaudiohrtf-spatialaudiohrtfenvironmenttype)和 [**SpatialAudioHrtfOrientation**](spatialaudiohrtforientation.md)，其會為從資料流程建立的新物件指定這些設定的預設值。</span><span class="sxs-lookup"><span data-stu-id="e15e1-218">The activation params for HRTF supports a few additional parameters, such as a [**SpatialAudioHrtfDistanceDecay**](/windows/desktop/api/spatialaudiohrtf/ns-spatialaudiohrtf-spatialaudiohrtfdistancedecay), a [**SpatialAudioHrtfDirectivityUnion**](/windows/desktop/api/spatialaudiohrtf/ns-spatialaudiohrtf-spatialaudiohrtfdirectivityunion), a [**SpatialAudioHrtfEnvironmentType**](/windows/desktop/api/spatialaudiohrtf/ne-spatialaudiohrtf-spatialaudiohrtfenvironmenttype), and a [**SpatialAudioHrtfOrientation**](spatialaudiohrtforientation.md), which specify the default values of these settings for new objects created from the stream.</span></span> <span data-ttu-id="e15e1-219">這些參數是選擇性的。</span><span class="sxs-lookup"><span data-stu-id="e15e1-219">These parameters are optional.</span></span> <span data-ttu-id="e15e1-220">將欄位設定為 **nullptr** 以提供沒有預設值。</span><span class="sxs-lookup"><span data-stu-id="e15e1-220">Set the fields to **nullptr** to provide no default values.</span></span>

<span data-ttu-id="e15e1-221">呼叫 [**ISpatialAudioClient：： ActivateSpatialAudioStream**](/windows/desktop/api/spatialaudioclient/nf-spatialaudioclient-ispatialaudioclient-activatespatialaudiostream) 來啟動資料流程。</span><span class="sxs-lookup"><span data-stu-id="e15e1-221">Call [**ISpatialAudioClient::ActivateSpatialAudioStream**](/windows/desktop/api/spatialaudioclient/nf-spatialaudioclient-ispatialaudioclient-activatespatialaudiostream) to activate the stream.</span></span>


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



<span data-ttu-id="e15e1-222">以下是一些需要的應用程式特定程式碼支援此範例，此範例會動態產生隨機定位的音訊物件，並將它們儲存在向量中。</span><span class="sxs-lookup"><span data-stu-id="e15e1-222">The following is some app-specific code to needed support this example, which will dynamically spawn randomly positioned audio objects and store them in a vector.</span></span>


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



<span data-ttu-id="e15e1-223">進入音訊轉譯迴圈之前，請先呼叫 [**ISpatialAudioObjectRenderStreamForHrtf：： Start**](/previous-versions/windows/desktop/legacy/mt779304(v=vs.85)) 來指示媒體管線開始要求音訊資料。</span><span class="sxs-lookup"><span data-stu-id="e15e1-223">Before entering the audio render loop, call [**ISpatialAudioObjectRenderStreamForHrtf::Start**](/previous-versions/windows/desktop/legacy/mt779304(v=vs.85)) to instruct the media pipeline to begin requesting audio data.</span></span>

<span data-ttu-id="e15e1-224">在轉譯迴圈內，等候我們在空間音訊串流初始化時所提供的緩衝區完成事件收到信號。</span><span class="sxs-lookup"><span data-stu-id="e15e1-224">Inside the render loop, wait for the buffer completion event we provided when the spatial audio stream was initialized to be signaled.</span></span> <span data-ttu-id="e15e1-225">在等候事件時，您應該設定合理的超時限制，例如 100 ms，因為轉譯類型或端點的任何變更都會導致該事件永遠不會收到信號。</span><span class="sxs-lookup"><span data-stu-id="e15e1-225">You should set a reasonable timeout limit, like 100 ms, when waiting for the event because any change to the render type or endpoint will cause that event to never be signaled.</span></span> <span data-ttu-id="e15e1-226">在此情況下，您可以呼叫 [**ISpatialAudioRenderStreamForHrtf：： Reset**](/previous-versions/windows/desktop/legacy/mt779303(v=vs.85)) 以嘗試重設空間音訊串流。</span><span class="sxs-lookup"><span data-stu-id="e15e1-226">In this case, you can call [**ISpatialAudioRenderStreamForHrtf::Reset**](/previous-versions/windows/desktop/legacy/mt779303(v=vs.85)) to attempt to reset the spatial audio stream.</span></span>

<span data-ttu-id="e15e1-227">接下來，呼叫 [**ISpatialAudioRenderStreamForHrtf：： BeginUpdatingAudioObjects**](/previous-versions/windows/desktop/legacy/mt779299(v=vs.85)) ，讓系統知道您即將以資料填滿音訊物件的緩衝區。</span><span class="sxs-lookup"><span data-stu-id="e15e1-227">Next, call [**ISpatialAudioRenderStreamForHrtf::BeginUpdatingAudioObjects**](/previous-versions/windows/desktop/legacy/mt779299(v=vs.85)) to let the system know that you are about to fill the audio objects' buffers with data.</span></span> <span data-ttu-id="e15e1-228">這個方法會傳回可用動態音訊物件的數目（在此範例中不使用），以及此資料流程轉譯之音訊物件緩衝區的框架計數。</span><span class="sxs-lookup"><span data-stu-id="e15e1-228">This method returns the number of available dynamic audio objects, not used in this example, and the frame count of the buffer for audio objects rendered by this stream.</span></span>

<span data-ttu-id="e15e1-229">當產生計數器達到指定的值時，我們會藉由呼叫 [**ISpatialAudioRenderStreamForHrtf：： ActivateSpatialAudioObjectForHrtf**](/windows/win32/api/spatialaudiohrtf/nf-spatialaudiohrtf-ispatialaudioobjectrenderstreamforhrtf-activatespatialaudioobjectforhrtf) 來指定 [**AudioObjectType \_ dynamic**](/windows/desktop/api/spatialaudioclient/ne-spatialaudioclient-audioobjecttype)來啟用新的動態音訊物件。</span><span class="sxs-lookup"><span data-stu-id="e15e1-229">Whenever the spawn counter reaches the specified value, we will activate a new dynamic audio object by calling [**ISpatialAudioRenderStreamForHrtf::ActivateSpatialAudioObjectForHrtf**](/windows/win32/api/spatialaudiohrtf/nf-spatialaudiohrtf-ispatialaudioobjectrenderstreamforhrtf-activatespatialaudioobjectforhrtf) specifying [**AudioObjectType\_Dynamic**](/windows/desktop/api/spatialaudioclient/ne-spatialaudioclient-audioobjecttype).</span></span> <span data-ttu-id="e15e1-230">如果已配置所有可用的動態音訊物件，此方法將會傳回 **SPLAUDCLNT \_ E \_ NO \_ \_ objects 物件**。</span><span class="sxs-lookup"><span data-stu-id="e15e1-230">If all available dynamic audio objects have already been allocated, this method will return **SPLAUDCLNT\_E\_NO\_MORE\_OBJECTS**.</span></span> <span data-ttu-id="e15e1-231">在此情況下，您可以根據應用程式特定的優先順序，選擇釋放一或多個先前啟用的音訊物件。</span><span class="sxs-lookup"><span data-stu-id="e15e1-231">In this case, you can choose to release one or more previously activated audio objects based on your app-specific prioritization.</span></span> <span data-ttu-id="e15e1-232">建立動態音訊物件之後，會將它新增至新的 **My3dObjectForHrtf** 結構，具有隨機化位置、旋轉、速度、磁片區和頻率值，然後新增至使用中物件的清單。</span><span class="sxs-lookup"><span data-stu-id="e15e1-232">After the dynamic audio object has been created, it is added to a new **My3dObjectForHrtf** structure, with randomized position, rotation, velocity, volume, and frequency values, which is then added to the list of active objects.</span></span>

<span data-ttu-id="e15e1-233">接下來，逐一查看所有使用中的物件（在此範例中以應用程式定義的 **My3dObjectForHrtf** 結構表示）。</span><span class="sxs-lookup"><span data-stu-id="e15e1-233">Next, iterate over all of the active objects, represented in this example with the app-defined **My3dObjectForHrtf** structure.</span></span> <span data-ttu-id="e15e1-234">針對每個音訊物件，呼叫 [**ISpatialAudioObjectForHrtf：： GetBuffer**](/previous-versions/windows/desktop/legacy/mt779271(v=vs.85)) 來取得空間音訊物件之音訊緩衝區的指標。</span><span class="sxs-lookup"><span data-stu-id="e15e1-234">For each audio object, call [**ISpatialAudioObjectForHrtf::GetBuffer**](/previous-versions/windows/desktop/legacy/mt779271(v=vs.85)) to get a pointer to the spatial audio object's audio buffer.</span></span> <span data-ttu-id="e15e1-235">這個方法也會傳回緩衝區的大小（以位元組為單位）。</span><span class="sxs-lookup"><span data-stu-id="e15e1-235">This method also returns the size of the buffer, in bytes.</span></span> <span data-ttu-id="e15e1-236">先前在本文中列出的 helper 方法 **WriteToAudioObjectBuffer**，可將音訊資料填滿緩衝區。</span><span class="sxs-lookup"><span data-stu-id="e15e1-236">The helper method, **WriteToAudioObjectBuffer**, listed previously in this article, to fill the buffer with audio data.</span></span> <span data-ttu-id="e15e1-237">寫入緩衝區之後，此範例會藉由呼叫 [**ISpatialAudioObjectForHrtf：： SetPosition**](/windows/desktop/api/spatialaudiohrtf/nf-spatialaudiohrtf-ispatialaudioobjectforhrtf-setposition) 和 [**ISpatialAudioObjectForHrtf：： SETORIENTATION**](/windows/desktop/api/spatialaudiohrtf/nf-spatialaudiohrtf-ispatialaudioobjectforhrtf-setorientation)來更新 HRTF 音訊物件的位置和方向。</span><span class="sxs-lookup"><span data-stu-id="e15e1-237">After writing to the buffer, the example updates the position and orientation of the HRTF audio object by calling [**ISpatialAudioObjectForHrtf::SetPosition**](/windows/desktop/api/spatialaudiohrtf/nf-spatialaudiohrtf-ispatialaudioobjectforhrtf-setposition) and [**ISpatialAudioObjectForHrtf::SetOrientation**](/windows/desktop/api/spatialaudiohrtf/nf-spatialaudiohrtf-ispatialaudioobjectforhrtf-setorientation).</span></span> <span data-ttu-id="e15e1-238">在此範例中，helper 方法（ **CalculateEmitterConeOrientationMatrix**）是用來根據3d 物件指向的方向來計算方向矩陣。</span><span class="sxs-lookup"><span data-stu-id="e15e1-238">In this example, a helper method, **CalculateEmitterConeOrientationMatrix**, is used to calculate the orientation matrix given the direction the 3D object is pointing.</span></span> <span data-ttu-id="e15e1-239">此方法的執行如下所示。</span><span class="sxs-lookup"><span data-stu-id="e15e1-239">The implementation of this method is shown below.</span></span> <span data-ttu-id="e15e1-240">您也可以藉由呼叫 [**ISpatialAudioObjectForHrtf：： SetGain**](/windows/desktop/api/spatialaudiohrtf/nf-spatialaudiohrtf-ispatialaudioobjectforhrtf-setgain)來修改音訊物件的磁片區。</span><span class="sxs-lookup"><span data-stu-id="e15e1-240">The volume of the audio object can also be modified by calling [**ISpatialAudioObjectForHrtf::SetGain**](/windows/desktop/api/spatialaudiohrtf/nf-spatialaudiohrtf-ispatialaudioobjectforhrtf-setgain).</span></span> <span data-ttu-id="e15e1-241">如果您未更新物件的位置、方向或數量，則會保留上一次設定時的位置、方向和磁片區。</span><span class="sxs-lookup"><span data-stu-id="e15e1-241">If you don't update the position, orientation, or volume of the object, it will retain the position, orientation, and volume from the last time it was set.</span></span> <span data-ttu-id="e15e1-242">如果已達到物件的應用程式定義存留期，則會呼叫 [**ISpatialAudioObjectForHrtf：： SetEndOfStream**](/previous-versions/windows/desktop/legacy/mt779275(v=vs.85)) ，讓音訊管線知道將不會使用此物件來寫入音訊，並將物件設定為 **nullptr** 以釋出其資源。</span><span class="sxs-lookup"><span data-stu-id="e15e1-242">If the object's app-defined lifetime has been reached, [**ISpatialAudioObjectForHrtf::SetEndOfStream**](/previous-versions/windows/desktop/legacy/mt779275(v=vs.85)) is called to let the audio pipeline know that no more audio will be written using this object and the object is set to **nullptr** to free up its resources.</span></span>

<span data-ttu-id="e15e1-243">將資料寫入所有音訊物件之後，請呼叫 [**ISpatialAudioRenderStreamForHrtf：： EndUpdatingAudioObjects**](/previous-versions/windows/desktop/legacy/mt779300(v=vs.85)) ，讓系統知道資料已可供轉譯。</span><span class="sxs-lookup"><span data-stu-id="e15e1-243">After writing data to all of your audio objects, call [**ISpatialAudioRenderStreamForHrtf::EndUpdatingAudioObjects**](/previous-versions/windows/desktop/legacy/mt779300(v=vs.85)) to let the system know the data is ready for rendering.</span></span> <span data-ttu-id="e15e1-244">您只能在呼叫 **BeginUpdatingAudioObjects** 和 **EndUpdatingAudioObjects** 之間呼叫 **GetBuffer** 。</span><span class="sxs-lookup"><span data-stu-id="e15e1-244">You can only call **GetBuffer** in between a call to **BeginUpdatingAudioObjects** and **EndUpdatingAudioObjects**.</span></span>


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



<span data-ttu-id="e15e1-245">當您完成轉譯空間音訊時，請呼叫 [**ISpatialAudioRenderStreamForHrtf：： stop**](/previous-versions/windows/desktop/legacy/mt779305(v=vs.85))來停止空間音訊串流。</span><span class="sxs-lookup"><span data-stu-id="e15e1-245">When you are done rendering spatial audio, stop the spatial audio stream by calling [**ISpatialAudioRenderStreamForHrtf::Stop**](/previous-versions/windows/desktop/legacy/mt779305(v=vs.85)).</span></span> <span data-ttu-id="e15e1-246">如果您不打算再次使用資料流程，請呼叫 [**ISpatialAudioRenderStreamForHrtf：： Reset**](/previous-versions/windows/desktop/legacy/mt779303(v=vs.85))來釋出其資源。</span><span class="sxs-lookup"><span data-stu-id="e15e1-246">If you are not going to use the stream again, free its resources by calling [**ISpatialAudioRenderStreamForHrtf::Reset**](/previous-versions/windows/desktop/legacy/mt779303(v=vs.85)).</span></span>


```C++
// Stop the stream 
hr = spatialAudioStreamForHrtf->Stop();

// We don't want to start again, so reset the stream to free it's resources.
hr = spatialAudioStreamForHrtf->Reset();

CloseHandle(bufferCompletionEvent);
```



<span data-ttu-id="e15e1-247">下列程式碼範例示範 **CalculateEmitterConeOrientationMatrix** helper 方法的執行方式，此方法是在上述範例中用來根據3d 物件指向的方向來計算方向矩陣。</span><span class="sxs-lookup"><span data-stu-id="e15e1-247">The following code example shows the implementation of the **CalculateEmitterConeOrientationMatrix** helper method which was used in the example above to calculate the orientation matrix given the direction the 3D object is pointing.</span></span>


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



## <a name="related-topics"></a><span data-ttu-id="e15e1-248">相關主題</span><span class="sxs-lookup"><span data-stu-id="e15e1-248">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="e15e1-249">空間音效</span><span class="sxs-lookup"><span data-stu-id="e15e1-249">Spatial Sound</span></span>](spatial-sound.md)
</dt> <dt>

[<span data-ttu-id="e15e1-250">**ISpatialAudioClient**</span><span class="sxs-lookup"><span data-stu-id="e15e1-250">**ISpatialAudioClient**</span></span>](/windows/desktop/api/spatialaudioclient/nn-spatialaudioclient-ispatialaudioclient)
</dt> <dt>

[<span data-ttu-id="e15e1-251">**ISpatialAudioObject**</span><span class="sxs-lookup"><span data-stu-id="e15e1-251">**ISpatialAudioObject**</span></span>](/windows/desktop/api/spatialaudioclient/nn-spatialaudioclient-ispatialaudioobject)
</dt> </dl>

 

 
