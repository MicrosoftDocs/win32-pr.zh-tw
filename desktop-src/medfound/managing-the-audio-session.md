---
description: 本主題說明使用 MFPlay 進行音訊/影片播放時，如何控制音訊音量。
ms.assetid: 4cf3dd0f-4c8a-4720-9eb3-d23352f3a85e
title: 管理音訊會話
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 8573bd7145cc792d3178d51cead18c3a8694dde9281644b37439a377f18bec96
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/11/2021
ms.locfileid: "118062819"
---
# <a name="managing-the-audio-session"></a>管理音訊會話

\[MFPlay 可用於 [需求] 區段中指定的作業系統。 它在後續版本中可能會變更或無法使用。 \]

本主題說明使用 MFPlay 進行音訊/影片播放時，如何控制音訊音量。

MFPlay 提供下列方法，以在播放期間控制音訊音量。



| 方法                                                            | 描述                                           |
|-------------------------------------------------------------------|-------------------------------------------------------|
| [**IMFPMediaPlayer::SetBalance**](/windows/desktop/api/mfplay/nf-mfplay-imfpmediaplayer-setbalance) | 設定左右通道之間的平衡。 |
| [**IMFPMediaPlayer::SetMute**](/windows/desktop/api/mfplay/nf-mfplay-imfpmediaplayer-setmute)       | 靜音或 unmutes 音訊。                           |
| [**IMFPMediaPlayer::SetVolume**](/windows/desktop/api/mfplay/nf-mfplay-imfpmediaplayer-setvolume)   | 設定磁片區層級。                                |



 

若要瞭解這些方法的行為，您必須知道 Windows 音訊會話 API 的一些術語 (WASAPI) ，它會執行 MFPlay 所使用的低層級音訊功能。

在 WASAPI 中，每個音訊串流都只屬於一個 *音訊會話*，也就是一組相關的音訊串流。 一般而言，應用程式會維護單一音訊會話，但應用程式可以建立一個以上的會話。 系統音量控制程式 (Sndvol) 會顯示每個音訊會話的音量控制項。 透過 Sndvol，使用者可以從應用程式外部調整音訊會話的音量。 下圖說明此程式。

![此圖顯示透過音量控制傳遞給說話者的音訊串流;應用程式和 sndvol 點對音量控制](images/audio-session.gif)

在 MFPlay 中，媒體專案可以有一或多個作用中音訊串流 (通常只有一個) 。 MFPlay 會在內部使用 [串流音訊](streaming-audio-renderer.md) 轉譯器 (SAR) 來轉譯音訊串流。 除非您設定此設定，否則會將應用程式的預設音訊會話加入。

MFPlay 音訊方法只會控制屬於目前媒體專案的資料流程。 它們不會影響屬於相同音訊會話之任何其他資料流程的磁片區。 就 WASAPI 而言，MFPlay 方法會控制 *每個通道* 的磁片區層級，而不是主要磁片區層級。 下圖說明此程式。

![圖表類似于前一個資料流程，但第二個數據流從媒體專案開始，而應用程式指向第二個數據流和音量控制項](images/audio-session02.gif)

請務必瞭解這項功能對 MFPlay 的影響。 首先，應用程式可以調整播放磁片區，而不會影響其他音訊串流。 您可以使用這項功能，因為 MFPlay 會建立 MFPlay 物件的兩個實例並個別調整磁片區，以執行跨淡化的音訊。

如果您使用 MFPlay 方法來變更音量或靜音狀態，則變更不會出現在 Sndvol 中。 例如，您可以呼叫 [**SetMute**](/windows/desktop/api/mfplay/nf-mfplay-imfpmediaplayer-setmute) 將音訊靜音，但是 Sndvol 不會將會話顯示為靜音。 相反地，如果使用 SndVol 來調整會話磁片區，則變更不會反映在 [**IMFPMediaPlayer：： GetVolume**](/windows/desktop/api/mfplay/nf-mfplay-imfpmediaplayer-getvolume) 或 [**IMFPMediaPlayer：： GetMute**](/windows/desktop/api/mfplay/nf-mfplay-imfpmediaplayer-getmute)傳回的值中。

針對 MFPlay player 物件的每個實例，有效的磁片區層級等於 *fPlayerVolume* × *FSessionVolume*，其中 *fPlayerVolume* 是 [**GetVolume**](/windows/desktop/api/mfplay/nf-mfplay-imfpmediaplayer-getvolume)所傳回的值，而 *fSessionVolume* 是會話的主要磁碟區。

針對簡單的播放案例，最好使用 WASAPI 來控制整個會話的音訊音量，而不是使用 MFPlay 方法。

## <a name="example-code"></a>範例程式碼

以下是 c + + 類別，可處理 WASAPI 中的基本工作：

-   控制會話的音量和靜音狀態。
-   在磁片區或靜音狀態變更時收到通知。

### <a name="class-declaration"></a>類別宣告

`CAudioSessionVolume`類別宣告會實 [**IAudioSessionEvents**](/windows/win32/api/audiopolicy/nn-audiopolicy-iaudiosessionevents)介面，也就是音訊會話事件的回呼介面。


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



當 `CAudioSessionVolume` 物件收到音訊會話事件時，它會將私用視窗訊息張貼至應用程式。 視窗控制碼和視窗訊息會以參數的形式提供給靜態 `CAudioSessionVolume::CreateInstance` 方法。

### <a name="getting-the-wasapi-interface-pointers"></a>取得 WASAPI 介面指標

`CAudioSessionVolume` 使用兩個主要 WASAPI 介面：

-   [**IAudioSessionControl**](/windows/win32/api/audiopolicy/nn-audiopolicy-iaudiosessioncontrol) 會管理音訊會話。
-   [**ISimpleAudioVolume**](/windows/win32/api/audioclient/nn-audioclient-isimpleaudiovolume) 控制會話的音量層級和靜音狀態。

若要取得這些介面，您必須列舉 SAR 所使用的音訊端點。 *音訊端點* 是用來捕捉或取用音訊資料的硬體裝置。 針對音訊播放，端點只是喇叭或其他音訊輸出。 根據預設，SAR 會使用 **eConsole** 裝置角色的預設端點。 *裝置角色* 是指派給端點的角色。 裝置角色是由 [**ERole**](/windows/win32/api/mmdeviceapi/ne-mmdeviceapi-erole) 列舉所指定，它記載于 [核心音訊 api](../coreaudio/core-audio-apis-in-windows-vista.md)中。

下列程式碼示範如何列舉端點和取得 WASAPI 介面。


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



### <a name="controlling-the-volume"></a>控制磁片區

`CAudioSessionVolume`控制音訊音量的方法會呼叫相同的 [**ISimpleAudioVolume**](/windows/win32/api/audioclient/nn-audioclient-isimpleaudiovolume)方法。 例如，會 `CAudioSessionVolume::SetVolume` 呼叫 [**ISimpleAudioVolume：： SetMasterVolume**](/windows/win32/api/audioclient/nf-audioclient-isimpleaudiovolume-setmastervolume)，如下列程式碼所示。


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



## <a name="complete-caudiosessionvolume-code"></a>完成 CAudioSessionVolume 程式碼

以下是類別方法的完整清單 `CAudioSessionVolume` 。


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



## <a name="requirements"></a>規格需求

MFPlay 需要 Windows 7。

## <a name="related-topics"></a>相關主題

<dl> <dt>

[使用 MFPlay 進行音訊/影片播放](using-mfplay-for-audio-video-playback.md)
</dt> </dl>

 

 
