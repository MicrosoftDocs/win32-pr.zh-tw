---
description: 本主題說明使用 MFPlay 進行音訊/影片播放時，如何控制音訊音量。
ms.assetid: 4cf3dd0f-4c8a-4720-9eb3-d23352f3a85e
title: 管理音訊會話
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 4e5231ca02603279675fabaaac4b96a1cd001906
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/07/2021
ms.locfileid: "104318039"
---
# <a name="managing-the-audio-session"></a><span data-ttu-id="76a7d-103">管理音訊會話</span><span class="sxs-lookup"><span data-stu-id="76a7d-103">Managing the Audio Session</span></span>

<span data-ttu-id="76a7d-104">\[MFPlay 可用於 [需求] 區段中指定的作業系統。</span><span class="sxs-lookup"><span data-stu-id="76a7d-104">\[MFPlay is available for use in the operating systems specified in the Requirements section.</span></span> <span data-ttu-id="76a7d-105">它在後續版本中可能會變更或無法使用。</span><span class="sxs-lookup"><span data-stu-id="76a7d-105">It may be altered or unavailable in subsequent versions.</span></span> <span data-ttu-id="76a7d-106">\]</span><span class="sxs-lookup"><span data-stu-id="76a7d-106">\]</span></span>

<span data-ttu-id="76a7d-107">本主題說明使用 MFPlay 進行音訊/影片播放時，如何控制音訊音量。</span><span class="sxs-lookup"><span data-stu-id="76a7d-107">This topic describes how to control audio volume when using MFPlay for audio/video playback.</span></span>

<span data-ttu-id="76a7d-108">MFPlay 提供下列方法，以在播放期間控制音訊音量。</span><span class="sxs-lookup"><span data-stu-id="76a7d-108">MFPlay provides the following methods to control the audio volume during playback.</span></span>



| <span data-ttu-id="76a7d-109">方法</span><span class="sxs-lookup"><span data-stu-id="76a7d-109">Method</span></span>                                                            | <span data-ttu-id="76a7d-110">描述</span><span class="sxs-lookup"><span data-stu-id="76a7d-110">Description</span></span>                                           |
|-------------------------------------------------------------------|-------------------------------------------------------|
| [<span data-ttu-id="76a7d-111">**IMFPMediaPlayer::SetBalance**</span><span class="sxs-lookup"><span data-stu-id="76a7d-111">**IMFPMediaPlayer::SetBalance**</span></span>](/windows/desktop/api/mfplay/nf-mfplay-imfpmediaplayer-setbalance) | <span data-ttu-id="76a7d-112">設定左右通道之間的平衡。</span><span class="sxs-lookup"><span data-stu-id="76a7d-112">Sets the balance between the left and right channels.</span></span> |
| [<span data-ttu-id="76a7d-113">**IMFPMediaPlayer::SetMute**</span><span class="sxs-lookup"><span data-stu-id="76a7d-113">**IMFPMediaPlayer::SetMute**</span></span>](/windows/desktop/api/mfplay/nf-mfplay-imfpmediaplayer-setmute)       | <span data-ttu-id="76a7d-114">靜音或 unmutes 音訊。</span><span class="sxs-lookup"><span data-stu-id="76a7d-114">Mutes or unmutes the audio.</span></span>                           |
| [<span data-ttu-id="76a7d-115">**IMFPMediaPlayer::SetVolume**</span><span class="sxs-lookup"><span data-stu-id="76a7d-115">**IMFPMediaPlayer::SetVolume**</span></span>](/windows/desktop/api/mfplay/nf-mfplay-imfpmediaplayer-setvolume)   | <span data-ttu-id="76a7d-116">設定磁片區層級。</span><span class="sxs-lookup"><span data-stu-id="76a7d-116">Sets the volume level.</span></span>                                |



 

<span data-ttu-id="76a7d-117">若要瞭解這些方法的行為，您必須知道 Windows 音訊會話 API 的一些術語 (WASAPI) ，它會執行 MFPlay 所使用的低層級音訊功能。</span><span class="sxs-lookup"><span data-stu-id="76a7d-117">To understand the behavior of these methods, you must know some terminology from the Windows Audio Session API (WASAPI), which implements the low-level audio functionality used by MFPlay.</span></span>

<span data-ttu-id="76a7d-118">在 WASAPI 中，每個音訊串流都只屬於一個 *音訊會話*，也就是一組相關的音訊串流。</span><span class="sxs-lookup"><span data-stu-id="76a7d-118">In WASAPI, every audio stream belongs to exactly one *audio session*, which is a group of related audio streams.</span></span> <span data-ttu-id="76a7d-119">一般而言，應用程式會維護單一音訊會話，但應用程式可以建立一個以上的會話。</span><span class="sxs-lookup"><span data-stu-id="76a7d-119">Typically, an application maintains a single audio session, although applications can create more than one session.</span></span> <span data-ttu-id="76a7d-120">系統音量控制程式 (Sndvol) 會顯示每個音訊會話的音量控制項。</span><span class="sxs-lookup"><span data-stu-id="76a7d-120">The system volume-control program (Sndvol) displays a volume control for each audio session.</span></span> <span data-ttu-id="76a7d-121">透過 Sndvol，使用者可以從應用程式外部調整音訊會話的音量。</span><span class="sxs-lookup"><span data-stu-id="76a7d-121">Through Sndvol, a user can adjust the volume of an audio session from outside of the application.</span></span> <span data-ttu-id="76a7d-122">下圖說明此程式。</span><span class="sxs-lookup"><span data-stu-id="76a7d-122">The following image illustrates this process.</span></span>

![此圖顯示透過音量控制傳遞給說話者的音訊串流;應用程式和 sndvol 點對音量控制](images/audio-session.gif)

<span data-ttu-id="76a7d-124">在 MFPlay 中，媒體專案可以有一或多個作用中音訊串流 (通常只有一個) 。</span><span class="sxs-lookup"><span data-stu-id="76a7d-124">In MFPlay, a media item can have one or more active audio streams (typically only one).</span></span> <span data-ttu-id="76a7d-125">MFPlay 會在內部使用 [串流音訊](streaming-audio-renderer.md) 轉譯器 (SAR) 來轉譯音訊串流。</span><span class="sxs-lookup"><span data-stu-id="76a7d-125">Internally, MFPlay uses the [Streaming Audio Renderer](streaming-audio-renderer.md) (SAR) to render the audio streams.</span></span> <span data-ttu-id="76a7d-126">除非您設定此設定，否則會將應用程式的預設音訊會話加入。</span><span class="sxs-lookup"><span data-stu-id="76a7d-126">Unless you configure it otherwise, the SAR joins the application's default audio session.</span></span>

<span data-ttu-id="76a7d-127">MFPlay 音訊方法只會控制屬於目前媒體專案的資料流程。</span><span class="sxs-lookup"><span data-stu-id="76a7d-127">The MFPlay audio methods control only the streams that belong to the current media item.</span></span> <span data-ttu-id="76a7d-128">它們不會影響屬於相同音訊會話之任何其他資料流程的磁片區。</span><span class="sxs-lookup"><span data-stu-id="76a7d-128">They do not affect the volume for any other streams that belong to the same audio session.</span></span> <span data-ttu-id="76a7d-129">就 WASAPI 而言，MFPlay 方法會控制 *每個通道* 的磁片區層級，而不是主要磁片區層級。</span><span class="sxs-lookup"><span data-stu-id="76a7d-129">In terms of WASAPI, the MFPlay methods control the *per-channel* volume levels, not the master volume level.</span></span> <span data-ttu-id="76a7d-130">下圖說明此程式。</span><span class="sxs-lookup"><span data-stu-id="76a7d-130">The following image illustrates this process.</span></span>

![圖表類似于前一個資料流程，但第二個數據流從媒體專案開始，而應用程式指向第二個數據流和音量控制項](images/audio-session02.gif)

<span data-ttu-id="76a7d-132">請務必瞭解這項功能對 MFPlay 的影響。</span><span class="sxs-lookup"><span data-stu-id="76a7d-132">It is important to understand some implications of this feature of MFPlay.</span></span> <span data-ttu-id="76a7d-133">首先，應用程式可以調整播放磁片區，而不會影響其他音訊串流。</span><span class="sxs-lookup"><span data-stu-id="76a7d-133">First, an application can adjust the playback volume without affecting other audio streams.</span></span> <span data-ttu-id="76a7d-134">您可以使用這項功能，因為 MFPlay 會建立 MFPlay 物件的兩個實例並個別調整磁片區，以執行跨淡化的音訊。</span><span class="sxs-lookup"><span data-stu-id="76a7d-134">You could use this feature if MFPlay to implement audio cross-fading, by creating two instances of the MFPlay object and adjusting the volume separately.</span></span>

<span data-ttu-id="76a7d-135">如果您使用 MFPlay 方法來變更音量或靜音狀態，則變更不會出現在 Sndvol 中。</span><span class="sxs-lookup"><span data-stu-id="76a7d-135">If you use MFPlay methods to change the volume or mute state, the changes do not appear in Sndvol.</span></span> <span data-ttu-id="76a7d-136">例如，您可以呼叫 [**SetMute**](/windows/desktop/api/mfplay/nf-mfplay-imfpmediaplayer-setmute) 將音訊靜音，但是 Sndvol 不會將會話顯示為靜音。</span><span class="sxs-lookup"><span data-stu-id="76a7d-136">For example, you can call [**SetMute**](/windows/desktop/api/mfplay/nf-mfplay-imfpmediaplayer-setmute) to mute the audio, but Sndvol will not show the session as muted.</span></span> <span data-ttu-id="76a7d-137">相反地，如果使用 SndVol 來調整會話磁片區，則變更不會反映在 [**IMFPMediaPlayer：： GetVolume**](/windows/desktop/api/mfplay/nf-mfplay-imfpmediaplayer-getvolume) 或 [**IMFPMediaPlayer：： GetMute**](/windows/desktop/api/mfplay/nf-mfplay-imfpmediaplayer-getmute)傳回的值中。</span><span class="sxs-lookup"><span data-stu-id="76a7d-137">Conversely, if SndVol is used to adjust the session volume, the changes are not reflected in the values returned by [**IMFPMediaPlayer::GetVolume**](/windows/desktop/api/mfplay/nf-mfplay-imfpmediaplayer-getvolume) or [**IMFPMediaPlayer::GetMute**](/windows/desktop/api/mfplay/nf-mfplay-imfpmediaplayer-getmute).</span></span>

<span data-ttu-id="76a7d-138">針對 MFPlay player 物件的每個實例，有效的磁片區層級等於 *fPlayerVolume* × *FSessionVolume*，其中 *fPlayerVolume* 是 [**GetVolume**](/windows/desktop/api/mfplay/nf-mfplay-imfpmediaplayer-getvolume)所傳回的值，而 *fSessionVolume* 是會話的主要磁碟區。</span><span class="sxs-lookup"><span data-stu-id="76a7d-138">For each instance of the MFPlay player object, the effective volume level equals *fPlayerVolume* × *fSessionVolume*, where *fPlayerVolume* is the value returned by [**GetVolume**](/windows/desktop/api/mfplay/nf-mfplay-imfpmediaplayer-getvolume), and *fSessionVolume* is the master volume for the session.</span></span>

<span data-ttu-id="76a7d-139">針對簡單的播放案例，最好使用 WASAPI 來控制整個會話的音訊音量，而不是使用 MFPlay 方法。</span><span class="sxs-lookup"><span data-stu-id="76a7d-139">For simple playback scenarios, it might be preferable to use the WASAPI to control the audio volume for the entire session, rather than use the MFPlay methods.</span></span>

## <a name="example-code"></a><span data-ttu-id="76a7d-140">範例程式碼</span><span class="sxs-lookup"><span data-stu-id="76a7d-140">Example Code</span></span>

<span data-ttu-id="76a7d-141">以下是 c + + 類別，可處理 WASAPI 中的基本工作：</span><span class="sxs-lookup"><span data-stu-id="76a7d-141">What follows is a C++ class that handles the basic tasks in WASAPI:</span></span>

-   <span data-ttu-id="76a7d-142">控制會話的音量和靜音狀態。</span><span class="sxs-lookup"><span data-stu-id="76a7d-142">Controlling the volume and mute state for the session.</span></span>
-   <span data-ttu-id="76a7d-143">在磁片區或靜音狀態變更時收到通知。</span><span class="sxs-lookup"><span data-stu-id="76a7d-143">Getting notifications whenever the volume or mute state change.</span></span>

### <a name="class-declaration"></a><span data-ttu-id="76a7d-144">類別宣告</span><span class="sxs-lookup"><span data-stu-id="76a7d-144">Class Declaration</span></span>

<span data-ttu-id="76a7d-145">`CAudioSessionVolume`類別宣告會實 [**IAudioSessionEvents**](/windows/win32/api/audiopolicy/nn-audiopolicy-iaudiosessionevents)介面，也就是音訊會話事件的回呼介面。</span><span class="sxs-lookup"><span data-stu-id="76a7d-145">The `CAudioSessionVolume` class declaration implements the [**IAudioSessionEvents**](/windows/win32/api/audiopolicy/nn-audiopolicy-iaudiosessionevents) interface, which is the callback interface for audio session events.</span></span>


```C++
class CAudioSessionVolume : public IAudioSessionEvents
{
public:
    // Static method to create an instance of the object.
    static HRESULT CreateInstance(
        UINT uNotificationMessage,
        HWND hwndNotification,
        CAudioSessionVolume **ppAudioSessionVolume
    );

    // IUnknown methods.
    STDMETHODIMP QueryInterface(REFIID iid, void** ppv);
    STDMETHODIMP_(ULONG) AddRef();
    STDMETHODIMP_(ULONG) Release();

    // IAudioSessionEvents methods.

    STDMETHODIMP OnSimpleVolumeChanged(
        float NewVolume,
        BOOL NewMute,
        LPCGUID EventContext
        );

    // The remaining audio session events do not require any action.
    STDMETHODIMP OnDisplayNameChanged(LPCWSTR,LPCGUID)
    {
        return S_OK;
    }

    STDMETHODIMP OnIconPathChanged(LPCWSTR,LPCGUID)
    {
        return S_OK;
    }

    STDMETHODIMP OnChannelVolumeChanged(DWORD,float[],DWORD,LPCGUID)
    {
        return S_OK;
    }

    STDMETHODIMP OnGroupingParamChanged(LPCGUID,LPCGUID)
    {
        return S_OK;
    }

    STDMETHODIMP OnStateChanged(AudioSessionState)
    {
        return S_OK;
    }

    STDMETHODIMP OnSessionDisconnected(AudioSessionDisconnectReason)
    {
        return S_OK;
    }

    // Other methods
    HRESULT EnableNotifications(BOOL bEnable);
    HRESULT GetVolume(float *pflVolume);
    HRESULT SetVolume(float flVolume);
    HRESULT GetMute(BOOL *pbMute);
    HRESULT SetMute(BOOL bMute);
    HRESULT SetDisplayName(const WCHAR *wszName);

protected:
    CAudioSessionVolume(UINT uNotificationMessage, HWND hwndNotification);
    ~CAudioSessionVolume();

    HRESULT Initialize();

protected:
    LONG m_cRef;                        // Reference count.
    UINT m_uNotificationMessage;        // Window message to send when an audio event occurs.
    HWND m_hwndNotification;            // Window to receives messages.
    BOOL m_bNotificationsEnabled;       // Are audio notifications enabled?

    IAudioSessionControl    *m_pAudioSession;
    ISimpleAudioVolume      *m_pSimpleAudioVolume;
};
```



<span data-ttu-id="76a7d-146">當 `CAudioSessionVolume` 物件收到音訊會話事件時，它會將私用視窗訊息張貼至應用程式。</span><span class="sxs-lookup"><span data-stu-id="76a7d-146">When the `CAudioSessionVolume` object receives an audio session event, it posts a private window message to the application.</span></span> <span data-ttu-id="76a7d-147">視窗控制碼和視窗訊息會以參數的形式提供給靜態 `CAudioSessionVolume::CreateInstance` 方法。</span><span class="sxs-lookup"><span data-stu-id="76a7d-147">The window handle and the window message are given as parameters to the static `CAudioSessionVolume::CreateInstance` method.</span></span>

### <a name="getting-the-wasapi-interface-pointers"></a><span data-ttu-id="76a7d-148">取得 WASAPI 介面指標</span><span class="sxs-lookup"><span data-stu-id="76a7d-148">Getting the WASAPI Interface Pointers</span></span>

<span data-ttu-id="76a7d-149">`CAudioSessionVolume` 使用兩個主要 WASAPI 介面：</span><span class="sxs-lookup"><span data-stu-id="76a7d-149">`CAudioSessionVolume` uses two main WASAPI interfaces:</span></span>

-   <span data-ttu-id="76a7d-150">[**IAudioSessionControl**](/windows/win32/api/audiopolicy/nn-audiopolicy-iaudiosessioncontrol) 會管理音訊會話。</span><span class="sxs-lookup"><span data-stu-id="76a7d-150">[**IAudioSessionControl**](/windows/win32/api/audiopolicy/nn-audiopolicy-iaudiosessioncontrol) manages the audio session.</span></span>
-   <span data-ttu-id="76a7d-151">[**ISimpleAudioVolume**](/windows/win32/api/audioclient/nn-audioclient-isimpleaudiovolume) 控制會話的音量層級和靜音狀態。</span><span class="sxs-lookup"><span data-stu-id="76a7d-151">[**ISimpleAudioVolume**](/windows/win32/api/audioclient/nn-audioclient-isimpleaudiovolume) controls the volume level and mute state of the session.</span></span>

<span data-ttu-id="76a7d-152">若要取得這些介面，您必須列舉 SAR 所使用的音訊端點。</span><span class="sxs-lookup"><span data-stu-id="76a7d-152">To get these interfaces, you must enumerate the audio endpoint that is used by the SAR.</span></span> <span data-ttu-id="76a7d-153">*音訊端點* 是用來捕捉或取用音訊資料的硬體裝置。</span><span class="sxs-lookup"><span data-stu-id="76a7d-153">An *audio endpoint* is a hardware device that captures or consumes audio data.</span></span> <span data-ttu-id="76a7d-154">針對音訊播放，端點只是喇叭或其他音訊輸出。</span><span class="sxs-lookup"><span data-stu-id="76a7d-154">For audio playback, an endpoint is simply a speaker or other audio output.</span></span> <span data-ttu-id="76a7d-155">根據預設，SAR 會使用 **eConsole** 裝置角色的預設端點。</span><span class="sxs-lookup"><span data-stu-id="76a7d-155">By default, the SAR uses the default endpoint for the **eConsole** device role.</span></span> <span data-ttu-id="76a7d-156">*裝置角色* 是指派給端點的角色。</span><span class="sxs-lookup"><span data-stu-id="76a7d-156">A *device role* is an assigned role for an endpoint.</span></span> <span data-ttu-id="76a7d-157">裝置角色是由 [**ERole**](/windows/win32/api/mmdeviceapi/ne-mmdeviceapi-erole) 列舉所指定，它記載于 [核心音訊 api](../coreaudio/core-audio-apis-in-windows-vista.md)中。</span><span class="sxs-lookup"><span data-stu-id="76a7d-157">Device roles are specified by the [**ERole**](/windows/win32/api/mmdeviceapi/ne-mmdeviceapi-erole) enumeration, which is documented in [Core Audio APIs](../coreaudio/core-audio-apis-in-windows-vista.md).</span></span>

<span data-ttu-id="76a7d-158">下列程式碼示範如何列舉端點和取得 WASAPI 介面。</span><span class="sxs-lookup"><span data-stu-id="76a7d-158">The following code shows how to enumerate the endpoint and get the WASAPI interfaces.</span></span>


```C++
HRESULT CAudioSessionVolume::Initialize()
{
    HRESULT hr = S_OK;

    IMMDeviceEnumerator *pDeviceEnumerator = NULL;
    IMMDevice *pDevice = NULL;
    IAudioSessionManager *pAudioSessionManager = NULL;

    // Get the enumerator for the audio endpoint devices.
    hr = CoCreateInstance(
        __uuidof(MMDeviceEnumerator),
        NULL,
        CLSCTX_INPROC_SERVER,
        IID_PPV_ARGS(&pDeviceEnumerator)
        );

    if (FAILED(hr))
    {
        goto done;
    }

    // Get the default audio endpoint that the SAR will use.
    hr = pDeviceEnumerator->GetDefaultAudioEndpoint(
        eRender,
        eConsole,   // The SAR uses 'eConsole' by default.
        &pDevice
        );

    if (FAILED(hr))
    {
        goto done;
    }

    // Get the session manager for this device.
    hr = pDevice->Activate(
        __uuidof(IAudioSessionManager),
        CLSCTX_INPROC_SERVER,
        NULL,
        (void**) &pAudioSessionManager
        );

    if (FAILED(hr))
    {
        goto done;
    }

    // Get the audio session.
    hr = pAudioSessionManager->GetAudioSessionControl(
        &GUID_NULL,     // Get the default audio session.
        FALSE,          // The session is not cross-process.
        &m_pAudioSession
        );


    if (FAILED(hr))
    {
        goto done;
    }

    hr = pAudioSessionManager->GetSimpleAudioVolume(
        &GUID_NULL, 0, &m_pSimpleAudioVolume
        );

done:
    SafeRelease(&pDeviceEnumerator);
    SafeRelease(&pDevice);
    SafeRelease(&pAudioSessionManager);
    return hr;
}
```



### <a name="controlling-the-volume"></a><span data-ttu-id="76a7d-159">控制磁片區</span><span class="sxs-lookup"><span data-stu-id="76a7d-159">Controlling the Volume</span></span>

<span data-ttu-id="76a7d-160">`CAudioSessionVolume`控制音訊音量的方法會呼叫相同的 [**ISimpleAudioVolume**](/windows/win32/api/audioclient/nn-audioclient-isimpleaudiovolume)方法。</span><span class="sxs-lookup"><span data-stu-id="76a7d-160">The `CAudioSessionVolume` methods that control the audio volume call the equivalent [**ISimpleAudioVolume**](/windows/win32/api/audioclient/nn-audioclient-isimpleaudiovolume) methods.</span></span> <span data-ttu-id="76a7d-161">例如，會 `CAudioSessionVolume::SetVolume` 呼叫 [**ISimpleAudioVolume：： SetMasterVolume**](/windows/win32/api/audioclient/nf-audioclient-isimpleaudiovolume-setmastervolume)，如下列程式碼所示。</span><span class="sxs-lookup"><span data-stu-id="76a7d-161">For example, `CAudioSessionVolume::SetVolume` calls [**ISimpleAudioVolume::SetMasterVolume**](/windows/win32/api/audioclient/nf-audioclient-isimpleaudiovolume-setmastervolume), as shown in the following code.</span></span>


```C++
HRESULT CAudioSessionVolume::SetVolume(float flVolume)
{
    if (m_pSimpleAudioVolume == NULL)
    {
        return E_FAIL;
    }
    else
    {
        return m_pSimpleAudioVolume->SetMasterVolume(
            flVolume,
            &AudioSessionVolumeCtx  // Event context.
            );
    }
}
```



## <a name="complete-caudiosessionvolume-code"></a><span data-ttu-id="76a7d-162">完成 CAudioSessionVolume 程式碼</span><span class="sxs-lookup"><span data-stu-id="76a7d-162">Complete CAudioSessionVolume Code</span></span>

<span data-ttu-id="76a7d-163">以下是類別方法的完整清單 `CAudioSessionVolume` 。</span><span class="sxs-lookup"><span data-stu-id="76a7d-163">Here is the complete listing for the methods of the `CAudioSessionVolume` class.</span></span>


```C++
static const GUID AudioSessionVolumeCtx =
{ 0x2715279f, 0x4139, 0x4ba0, { 0x9c, 0xb1, 0xb3, 0x51, 0xf1, 0xb5, 0x8a, 0x4a } };


CAudioSessionVolume::CAudioSessionVolume(
    UINT uNotificationMessage,
    HWND hwndNotification
    )
    : m_cRef(1),
      m_uNotificationMessage(uNotificationMessage),
      m_hwndNotification(hwndNotification),
      m_bNotificationsEnabled(FALSE),
      m_pAudioSession(NULL),
      m_pSimpleAudioVolume(NULL)
{
}

CAudioSessionVolume::~CAudioSessionVolume()
{
    EnableNotifications(FALSE);

    SafeRelease(&m_pAudioSession);
    SafeRelease(&m_pSimpleAudioVolume);
};


//  Creates an instance of the CAudioSessionVolume object.

/* static */
HRESULT CAudioSessionVolume::CreateInstance(
    UINT uNotificationMessage,
    HWND hwndNotification,
    CAudioSessionVolume **ppAudioSessionVolume
    )
{

    CAudioSessionVolume *pAudioSessionVolume = new (std::nothrow)
        CAudioSessionVolume(uNotificationMessage, hwndNotification);

    if (pAudioSessionVolume == NULL)
    {
        return E_OUTOFMEMORY;
    }

    HRESULT hr = pAudioSessionVolume->Initialize();
    if (SUCCEEDED(hr))
    {
        *ppAudioSessionVolume = pAudioSessionVolume;
    }
    else
    {
        pAudioSessionVolume->Release();
    }

    return hr;
}


//  Initializes the CAudioSessionVolume object.

HRESULT CAudioSessionVolume::Initialize()
{
    HRESULT hr = S_OK;

    IMMDeviceEnumerator *pDeviceEnumerator = NULL;
    IMMDevice *pDevice = NULL;
    IAudioSessionManager *pAudioSessionManager = NULL;

    // Get the enumerator for the audio endpoint devices.
    hr = CoCreateInstance(
        __uuidof(MMDeviceEnumerator),
        NULL,
        CLSCTX_INPROC_SERVER,
        IID_PPV_ARGS(&pDeviceEnumerator)
        );

    if (FAILED(hr))
    {
        goto done;
    }

    // Get the default audio endpoint that the SAR will use.
    hr = pDeviceEnumerator->GetDefaultAudioEndpoint(
        eRender,
        eConsole,   // The SAR uses 'eConsole' by default.
        &pDevice
        );

    if (FAILED(hr))
    {
        goto done;
    }

    // Get the session manager for this device.
    hr = pDevice->Activate(
        __uuidof(IAudioSessionManager),
        CLSCTX_INPROC_SERVER,
        NULL,
        (void**) &pAudioSessionManager
        );

    if (FAILED(hr))
    {
        goto done;
    }

    // Get the audio session.
    hr = pAudioSessionManager->GetAudioSessionControl(
        &GUID_NULL,     // Get the default audio session.
        FALSE,          // The session is not cross-process.
        &m_pAudioSession
        );


    if (FAILED(hr))
    {
        goto done;
    }

    hr = pAudioSessionManager->GetSimpleAudioVolume(
        &GUID_NULL, 0, &m_pSimpleAudioVolume
        );

done:
    SafeRelease(&pDeviceEnumerator);
    SafeRelease(&pDevice);
    SafeRelease(&pAudioSessionManager);
    return hr;
}

STDMETHODIMP CAudioSessionVolume::QueryInterface(REFIID riid, void **ppv)
{
    static const QITAB qit[] =
    {
        QITABENT(CAudioSessionVolume, IAudioSessionEvents),
        { 0 },
    };
    return QISearch(this, qit, riid, ppv);
}

STDMETHODIMP_(ULONG) CAudioSessionVolume::AddRef()
{
    return InterlockedIncrement(&m_cRef);
}

STDMETHODIMP_(ULONG) CAudioSessionVolume::Release()
{
    LONG cRef = InterlockedDecrement( &m_cRef );
    if (cRef == 0)
    {
        delete this;
    }
    return cRef;
}


// Enables or disables notifications from the audio session. For example, the
// application is notified if the user mutes the audio through the system
// volume-control program (Sndvol).

HRESULT CAudioSessionVolume::EnableNotifications(BOOL bEnable)
{
    HRESULT hr = S_OK;

    if (m_hwndNotification == NULL || m_pAudioSession == NULL)
    {
        return E_FAIL;
    }

    if (m_bNotificationsEnabled == bEnable)
    {
        // No change.
        return S_OK;
    }

    if (bEnable)
    {
        hr = m_pAudioSession->RegisterAudioSessionNotification(this);
    }
    else
    {
        hr = m_pAudioSession->UnregisterAudioSessionNotification(this);
    }

    if (SUCCEEDED(hr))
    {
        m_bNotificationsEnabled = bEnable;
    }

    return hr;
}


// Gets the session volume level.

HRESULT CAudioSessionVolume::GetVolume(float *pflVolume)
{
    if ( m_pSimpleAudioVolume == NULL)
    {
        return E_FAIL;
    }
    else
    {
        return m_pSimpleAudioVolume->GetMasterVolume(pflVolume);
    }
}

//  Sets the session volume level.
//
//  flVolume: Ranges from 0 (silent) to 1 (full volume)

HRESULT CAudioSessionVolume::SetVolume(float flVolume)
{
    if (m_pSimpleAudioVolume == NULL)
    {
        return E_FAIL;
    }
    else
    {
        return m_pSimpleAudioVolume->SetMasterVolume(
            flVolume,
            &AudioSessionVolumeCtx  // Event context.
            );
    }
}


//  Gets the muting state of the session.

HRESULT CAudioSessionVolume::GetMute(BOOL *pbMute)
{
    if (m_pSimpleAudioVolume == NULL)
    {
        return E_FAIL;
    }
    else
    {
        return m_pSimpleAudioVolume->GetMute(pbMute);
    }
}

//  Mutes or unmutes the session audio.

HRESULT CAudioSessionVolume::SetMute(BOOL bMute)
{
    if (m_pSimpleAudioVolume == NULL)
    {
        return E_FAIL;
    }
    else
    {
        return m_pSimpleAudioVolume->SetMute(
            bMute,
            &AudioSessionVolumeCtx  // Event context.
            );
    }
}

//  Sets the display name for the session audio.

HRESULT CAudioSessionVolume::SetDisplayName(const WCHAR *wszName)
{
    if (m_pAudioSession == NULL)
    {
        return E_FAIL;
    }
    else
    {
        return m_pAudioSession->SetDisplayName(wszName, NULL);
    }
}


//  Called when the session volume level or muting state changes.
//  (Implements IAudioSessionEvents::OnSimpleVolumeChanged.)

HRESULT CAudioSessionVolume::OnSimpleVolumeChanged(
    float NewVolume,
    BOOL NewMute,
    LPCGUID EventContext
    )
{
    // Check if we should post a message to the application.

    if ( m_bNotificationsEnabled &&
        (*EventContext != AudioSessionVolumeCtx) &&
        (m_hwndNotification != NULL)
        )
    {
        // Notifications are enabled, AND
        // We did not trigger the event ourselves, AND
        // We have a valid window handle.

        // Post the message.
        ::PostMessage(
            m_hwndNotification,
            m_uNotificationMessage,
            *((WPARAM*)(&NewVolume)),  // Coerce the float.
            (LPARAM)NewMute
            );
    }
    return S_OK;
}
```



## <a name="requirements"></a><span data-ttu-id="76a7d-164">規格需求</span><span class="sxs-lookup"><span data-stu-id="76a7d-164">Requirements</span></span>

<span data-ttu-id="76a7d-165">MFPlay 需要 Windows 7。</span><span class="sxs-lookup"><span data-stu-id="76a7d-165">MFPlay requires Windows 7.</span></span>

## <a name="related-topics"></a><span data-ttu-id="76a7d-166">相關主題</span><span class="sxs-lookup"><span data-stu-id="76a7d-166">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="76a7d-167">使用 MFPlay 進行音訊/影片播放</span><span class="sxs-lookup"><span data-stu-id="76a7d-167">Using MFPlay for Audio/Video Playback</span></span>](using-mfplay-for-audio-video-playback.md)
</dt> </dl>

 

 
