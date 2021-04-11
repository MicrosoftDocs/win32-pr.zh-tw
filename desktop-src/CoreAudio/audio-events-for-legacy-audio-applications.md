---
description: 舊版音訊應用程式的音訊事件
ms.assetid: 91a93b79-2563-4b25-af5d-ca5f7d35d77b
title: 舊版音訊應用程式的音訊事件
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: f0fe99195910b1c1c68c0f3a1b39dd2706dde0be
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/07/2021
ms.locfileid: "104111560"
---
# <a name="audio-events-for-legacy-audio-applications"></a><span data-ttu-id="93685-103">舊版音訊應用程式的音訊事件</span><span class="sxs-lookup"><span data-stu-id="93685-103">Audio Events for Legacy Audio Applications</span></span>

<span data-ttu-id="93685-104">舊版音訊 Api （例如 DirectSound、DirectShow 和 **waveOutXxx** 功能）可讓應用程式取得和設定音訊串流的音量層級。</span><span class="sxs-lookup"><span data-stu-id="93685-104">Legacy audio APIs such as DirectSound, DirectShow, and the **waveOutXxx** functions enable applications to get and set the volume levels of audio streams.</span></span> <span data-ttu-id="93685-105">應用程式可以使用這些 Api 中的磁片區控制功能，在其應用程式視窗中顯示音量滑杆。</span><span class="sxs-lookup"><span data-stu-id="93685-105">Applications can use the volume-control capabilities in these APIs to display volume sliders in their application windows.</span></span>

<span data-ttu-id="93685-106">在 Windows Vista 中，系統音量控制程式 Sndvol 可讓使用者控制個別應用程式的音訊音量層級。</span><span class="sxs-lookup"><span data-stu-id="93685-106">In Windows Vista, the system volume-control program, Sndvol, allows users to control the audio volume levels for individual applications.</span></span> <span data-ttu-id="93685-107">應用程式所顯示的音量滑杆應連結到 Sndvol 中對應的音量滑杆。</span><span class="sxs-lookup"><span data-stu-id="93685-107">The volume sliders that are displayed by applications should be linked to the corresponding volume sliders in Sndvol.</span></span> <span data-ttu-id="93685-108">如果使用者透過應用程式視窗中的音量滑杆來調整應用程式音量，則 Sndvol 中對應的磁片區滑杆會立即移動以指出新的音量層級。</span><span class="sxs-lookup"><span data-stu-id="93685-108">If a user adjusts the application volume through a volume slider in an application window, then the corresponding volume slider in Sndvol immediately moves to indicate the new volume level.</span></span> <span data-ttu-id="93685-109">相反地，如果使用者透過 Sndvol 來調整應用程式音量，則應用程式視窗中的音量滑杆應該會移動以指出新的音量層級。</span><span class="sxs-lookup"><span data-stu-id="93685-109">Conversely, if the user adjusts the application volume through Sndvol, then the volume sliders in the application window should move to indicate the new volume level.</span></span>

<span data-ttu-id="93685-110">在 Windows Vista 中，Sndvol 會立即反映應用程式透過呼叫 **IDirectSoundBuffer：： SetVolume** 方法或 **waveOutSetVolume** 函數所進行的磁片區變更。</span><span class="sxs-lookup"><span data-stu-id="93685-110">In Windows Vista, Sndvol immediately reflects volume changes that an application makes through calls to the **IDirectSoundBuffer::SetVolume** method or **waveOutSetVolume** function.</span></span> <span data-ttu-id="93685-111">不過，舊版音訊 API （例如 DirectSound 或 **waveOutXxx** 函式）不會在使用者透過 Sndvol 變更應用程式磁片區時，提供任何方法來通知應用程式。</span><span class="sxs-lookup"><span data-stu-id="93685-111">However, a legacy audio API such as DirectSound or the **waveOutXxx** functions provides no means to notify an application when the user changes the application volume through Sndvol.</span></span> <span data-ttu-id="93685-112">如果應用程式顯示磁片區滑杆，但未收到磁片區變更的通知，則滑杆將無法反映使用者在 Sndvol 中所做的變更。</span><span class="sxs-lookup"><span data-stu-id="93685-112">If an application displays a volume slider but does not receive notifications of volume changes, then the slider will fail to reflect changes made by the user in Sndvol.</span></span> <span data-ttu-id="93685-113">若要執行適當的行為，應用程式設計工具必須以某種方式彌補舊版音訊 API 缺少通知的情況。</span><span class="sxs-lookup"><span data-stu-id="93685-113">To implement the appropriate behavior, the application designer must somehow compensate for the lack of notifications by the legacy audio API.</span></span>

<span data-ttu-id="93685-114">其中一個解決方案可能是讓應用程式設定計時器，以定期提醒它檢查磁片區層級，以查看是否已變更。</span><span class="sxs-lookup"><span data-stu-id="93685-114">One solution might be for the application to set a timer to periodically remind it to check the volume level to see if it has changed.</span></span>

<span data-ttu-id="93685-115">更簡潔的解決方案是讓應用程式使用核心音訊 Api 的事件通知功能。</span><span class="sxs-lookup"><span data-stu-id="93685-115">A more elegant solution is for the application to use the event notification capabilities of the core audio APIs.</span></span> <span data-ttu-id="93685-116">尤其是，應用程式可以在磁片區變更或其他類型的音訊事件發生時，註冊 [**IAudioSessionEvents**](/windows/desktop/api/Audiopolicy/nn-audiopolicy-iaudiosessionevents) 介面以接收回呼。</span><span class="sxs-lookup"><span data-stu-id="93685-116">In particular, the application can register an [**IAudioSessionEvents**](/windows/desktop/api/Audiopolicy/nn-audiopolicy-iaudiosessionevents) interface to receive callbacks when volume changes or other types of audio events occur.</span></span> <span data-ttu-id="93685-117">當磁片區變更時，磁片區變更回呼常式可以立即更新應用程式的磁片區滑杆以反映變更。</span><span class="sxs-lookup"><span data-stu-id="93685-117">When the volume changes, the volume-change callback routine can immediately update the application's volume slider to reflect the change.</span></span>

<span data-ttu-id="93685-118">下列程式碼範例會示範應用程式如何註冊，以接收磁片區變更和其他音訊事件的通知：</span><span class="sxs-lookup"><span data-stu-id="93685-118">The following code example shows how an application can register to receive notifications of volume changes and other audio events:</span></span>


```C++
//-----------------------------------------------------------
// Register the application to receive notifications when the
// volume level changes on the default process-specific audio
// session (with session GUID value GUID_NULL) on the audio
// endpoint device with the specified data-flow direction
// (eRender or eCapture) and device role.
//-----------------------------------------------------------
#define EXIT_ON_ERROR(hr)  \
              if (FAILED(hr)) { goto Exit; }
#define SAFE_RELEASE(punk)  \
              if ((punk) != NULL)  \
                { (punk)->Release(); (punk) = NULL; }

class AudioVolumeEvents
{
    HRESULT _hrStatus;
    IAudioSessionManager *_pManager;
    IAudioSessionControl *_pControl;
    IAudioSessionEvents *_pAudioEvents;
public:
    AudioVolumeEvents(EDataFlow, ERole, IAudioSessionEvents*);
    ~AudioVolumeEvents();
    HRESULT GetStatus() { return _hrStatus; };
};

// Constructor
AudioVolumeEvents::AudioVolumeEvents(EDataFlow flow, ERole role,
                                     IAudioSessionEvents *pAudioEvents)
{
    IMMDeviceEnumerator *pEnumerator = NULL;
    IMMDevice *pDevice = NULL;

    _hrStatus = S_OK;
    _pManager = NULL;
    _pControl = NULL;
    _pAudioEvents = pAudioEvents;

    if (_pAudioEvents == NULL)
    {
        _hrStatus = E_POINTER;
        return;
    }

    _pAudioEvents->AddRef();

    // Get the enumerator for the audio endpoint devices
    // on this system.
    _hrStatus = CoCreateInstance(__uuidof(MMDeviceEnumerator),
                                 NULL, CLSCTX_INPROC_SERVER,
                                 __uuidof(IMMDeviceEnumerator),
                                 (void**)&pEnumerator);
    EXIT_ON_ERROR(_hrStatus)

    // Get the audio endpoint device with the specified data-flow
    // direction (eRender or eCapture) and device role.
    _hrStatus = pEnumerator->GetDefaultAudioEndpoint(flow, role,
                                                     &pDevice);
    EXIT_ON_ERROR(_hrStatus)

    // Get the session manager for the endpoint device.
    _hrStatus = pDevice->Activate(__uuidof(IAudioSessionManager),
                                  CLSCTX_INPROC_SERVER, NULL,
                                  (void**)&_pManager);
    EXIT_ON_ERROR(_hrStatus)

    // Get the control interface for the process-specific audio
    // session with session GUID = GUID_NULL. This is the session
    // that an audio stream for a DirectSound, DirectShow, waveOut,
    // or PlaySound application stream belongs to by default.
    _hrStatus = _pManager->GetAudioSessionControl(NULL, 0, &_pControl);
    EXIT_ON_ERROR(_hrStatus)

    _hrStatus = _pControl->RegisterAudioSessionNotification(_pAudioEvents);
    EXIT_ON_ERROR(_hrStatus)

Exit:
    SAFE_RELEASE(pEnumerator)
    SAFE_RELEASE(pDevice)
}

// Destructor
AudioVolumeEvents::~AudioVolumeEvents()
{
    if (_pControl != NULL)
    {
        _pControl->UnregisterAudioSessionNotification(_pAudioEvents);
    }
    SAFE_RELEASE(_pManager)
    SAFE_RELEASE(_pControl)
    SAFE_RELEASE(_pAudioEvents)
};
```



<span data-ttu-id="93685-119">上述程式碼範例會執行名為 AudioVolumeEvents 的類別。</span><span class="sxs-lookup"><span data-stu-id="93685-119">The preceding code example implements a class named AudioVolumeEvents.</span></span> <span data-ttu-id="93685-120">在程式初始化期間，音訊應用程式會藉由建立 AudioVolumeEvents 物件來啟用音訊事件通知。</span><span class="sxs-lookup"><span data-stu-id="93685-120">During program initialization, the audio application enables audio-event notifications by creating an AudioVolumeEvents object.</span></span> <span data-ttu-id="93685-121">此類別的函式會採用三個輸入參數：</span><span class="sxs-lookup"><span data-stu-id="93685-121">The constructor for this class takes three input parameters:</span></span>

-   <span data-ttu-id="93685-122">*flow*： [音訊端點裝置](audio-endpoint-devices.md) 的資料流程程方向 ([**EDataFlow**](/windows/win32/api/mmdeviceapi/ne-mmdeviceapi-edataflow) 的列舉值) 。</span><span class="sxs-lookup"><span data-stu-id="93685-122">*flow*—the data-flow direction of the [audio endpoint device](audio-endpoint-devices.md) (an [**EDataFlow**](/windows/win32/api/mmdeviceapi/ne-mmdeviceapi-edataflow) enumeration value).</span></span>
-   <span data-ttu-id="93685-123">*角色*-端點裝置的目前 [裝置角色](device-roles.md) ([**ERole**](/windows/win32/api/mmdeviceapi/ne-mmdeviceapi-erole) 列舉值) 。</span><span class="sxs-lookup"><span data-stu-id="93685-123">*role*—the current [device role](device-roles.md) of the endpoint device (an [**ERole**](/windows/win32/api/mmdeviceapi/ne-mmdeviceapi-erole) enumeration value).</span></span>
-   <span data-ttu-id="93685-124">*pAudioEvents*-物件的指標 ([**IAudioSessionEvents**](/windows/desktop/api/Audiopolicy/nn-audiopolicy-iaudiosessionevents) 介面實例) ，其中包含應用程式所執行的一組回呼常式。</span><span class="sxs-lookup"><span data-stu-id="93685-124">*pAudioEvents*—pointer to an object (an [**IAudioSessionEvents**](/windows/desktop/api/Audiopolicy/nn-audiopolicy-iaudiosessionevents) interface instance) that contains a set of callback routines that are implemented by the application.</span></span>

<span data-ttu-id="93685-125">此函式會提供流程和角色值作為 [**IMMDeviceEnumerator：： GetDefaultAudioEndpoint**](/windows/desktop/api/Mmdeviceapi/nf-mmdeviceapi-immdeviceenumerator-getdefaultaudioendpoint) 方法的輸入參數。</span><span class="sxs-lookup"><span data-stu-id="93685-125">The constructor supplies the flow and role values as input parameters to the [**IMMDeviceEnumerator::GetDefaultAudioEndpoint**](/windows/desktop/api/Mmdeviceapi/nf-mmdeviceapi-immdeviceenumerator-getdefaultaudioendpoint) method.</span></span> <span data-ttu-id="93685-126">方法會建立 [**IMMDevice**](/windows/desktop/api/Mmdeviceapi/nn-mmdeviceapi-immdevice) 物件，該物件會使用指定的資料流程程方向和裝置角色封裝音訊端點裝置。</span><span class="sxs-lookup"><span data-stu-id="93685-126">The method creates an [**IMMDevice**](/windows/desktop/api/Mmdeviceapi/nn-mmdeviceapi-immdevice) object that encapsulates the audio endpoint device with the specified data-flow direction and device role.</span></span>

<span data-ttu-id="93685-127">應用程式會執行 *pAudioEvents* 所指向的物件。</span><span class="sxs-lookup"><span data-stu-id="93685-127">The application implements the object pointed to by *pAudioEvents*.</span></span> <span data-ttu-id="93685-128">上述程式碼範例中未顯示執行的 (。</span><span class="sxs-lookup"><span data-stu-id="93685-128">(The implementation is not shown in the preceding code example.</span></span> <span data-ttu-id="93685-129">如需執行 **IAudioSessionEvents** 介面的程式碼範例，請參閱 [音訊會話事件](audio-session-events.md)。 ) 此介面中的每個方法都會收到特定音訊事件種類的通知。</span><span class="sxs-lookup"><span data-stu-id="93685-129">For a code example that implements an **IAudioSessionEvents** interface, see [Audio Session Events](audio-session-events.md).) Each method in this interface receives notifications of a particular type of audio event.</span></span> <span data-ttu-id="93685-130">如果應用程式對特定事件種類不感興趣，則該事件種類的方法應該不會執行任何動作，但會傳回 \_ [確定]。</span><span class="sxs-lookup"><span data-stu-id="93685-130">If the application is not interested in a particular event type, then the method for that event type should do nothing but return S\_OK.</span></span>

<span data-ttu-id="93685-131">[**IAudioSessionEvents：： OnSimpleVolumeChanged**](/windows/desktop/api/Audiopolicy/nf-audiopolicy-iaudiosessionevents-onsimplevolumechanged)方法會接收磁片區變更的通知。</span><span class="sxs-lookup"><span data-stu-id="93685-131">The [**IAudioSessionEvents::OnSimpleVolumeChanged**](/windows/desktop/api/Audiopolicy/nf-audiopolicy-iaudiosessionevents-onsimplevolumechanged) method receives notifications of volume changes.</span></span> <span data-ttu-id="93685-132">一般來說，這個方法會更新應用程式的磁片區滑杆。</span><span class="sxs-lookup"><span data-stu-id="93685-132">Typically, this method updates the application's volume slider.</span></span>

<span data-ttu-id="93685-133">在上述程式碼範例中，AudioVolumeEvents 類別的函式會在會話 GUID 值 GUID Null 所識別的進程特定 [音訊會話](audio-sessions.md) 上註冊通知 \_ 。</span><span class="sxs-lookup"><span data-stu-id="93685-133">In the preceding code example, the constructor for the AudioVolumeEvents class registers for notifications on the process-specific [audio session](audio-sessions.md) that is identified by session GUID value GUID\_NULL.</span></span> <span data-ttu-id="93685-134">根據預設，舊版音訊 Api （例如 DirectSound、DirectShow 和 **waveOutXxx** 函式）會將它們的串流指派給此會話。</span><span class="sxs-lookup"><span data-stu-id="93685-134">By default, legacy audio APIs such as DirectSound, DirectShow, and the **waveOutXxx** functions assign their streams to this session.</span></span> <span data-ttu-id="93685-135">不過，DirectSound 或 DirectShow 應用程式可以選擇覆寫預設行為，並將其串流指派給跨進程會話，或指派給 guid 值（GUID 為 Null 以外）所識別的會話 \_ 。</span><span class="sxs-lookup"><span data-stu-id="93685-135">However, a DirectSound or DirectShow application can, as an option, override the default behavior and assign its streams to a cross-process session or to a session that is identified by a GUID value other than GUID\_NULL.</span></span> <span data-ttu-id="93685-136"> (目前未提供 **waveOutXxx** 應用程式的機制，以類似的方式覆寫預設行為。如需使用此行為的 directshow 應用程式程式碼範例 ) ，請參閱 [directshow 應用程式的裝置角色](device-roles-for-directshow-applications.md)。</span><span class="sxs-lookup"><span data-stu-id="93685-136">(No mechanism is currently provided for a **waveOutXxx** application to override the default behavior in a similar manner.) For a code example of a DirectShow application with this behavior, see [Device Roles for DirectShow Applications](device-roles-for-directshow-applications.md).</span></span> <span data-ttu-id="93685-137">若要容納這類應用程式，您可以修改上述程式碼範例中的函式，以接受兩個額外的輸入參數，也就是會話 GUID 和旗標，以指出要監視的會話是跨進程或進程特定的會話。</span><span class="sxs-lookup"><span data-stu-id="93685-137">To accommodate such an application, you can modify the constructor in the preceding code example to accept two additional input parameters—a session GUID and a flag to indicate whether the session that is to be monitored is a cross-process or process-specific session.</span></span> <span data-ttu-id="93685-138">將這些參數傳遞至函式中 [**IAudioSessionManager：： GetAudioSessionControl**](/windows/desktop/api/Audiopolicy/nf-audiopolicy-iaudiosessionmanager-getaudiosessioncontrol) 方法的呼叫。</span><span class="sxs-lookup"><span data-stu-id="93685-138">Pass these parameters to the call to the [**IAudioSessionManager::GetAudioSessionControl**](/windows/desktop/api/Audiopolicy/nf-audiopolicy-iaudiosessionmanager-getaudiosessioncontrol) method in the constructor.</span></span>

<span data-ttu-id="93685-139">在函式呼叫 [**IAudioSessionControl：： RegisterAudioSessionNotification**](/windows/desktop/api/Audiopolicy/nf-audiopolicy-iaudiosessioncontrol-registeraudiosessionnotification) 方法來註冊通知之後，只要有 [**IAudioSessionControl**](/windows/desktop/api/Audiopolicy/nn-audiopolicy-iaudiosessioncontrol) 或 [**IAudioSessionManager**](/windows/desktop/api/Audiopolicy/nn-audiopolicy-iaudiosessionmanager) 介面存在，應用程式就會繼續接收通知。</span><span class="sxs-lookup"><span data-stu-id="93685-139">After the constructor calls the [**IAudioSessionControl::RegisterAudioSessionNotification**](/windows/desktop/api/Audiopolicy/nf-audiopolicy-iaudiosessioncontrol-registeraudiosessionnotification) method to register for notifications, the application continues to receive notifications for only as long as either the [**IAudioSessionControl**](/windows/desktop/api/Audiopolicy/nn-audiopolicy-iaudiosessioncontrol) or [**IAudioSessionManager**](/windows/desktop/api/Audiopolicy/nn-audiopolicy-iaudiosessionmanager) interface exists.</span></span> <span data-ttu-id="93685-140">上述程式碼範例中的 AudioVolumeEvents 物件會保存這些介面的參考，直到呼叫它的函式為止。</span><span class="sxs-lookup"><span data-stu-id="93685-140">The AudioVolumeEvents object in the preceding code example holds references to these interfaces until its destructor is called.</span></span> <span data-ttu-id="93685-141">此行為可確保應用程式會在 AudioVolumeEvents 物件的存留期內繼續接收通知。</span><span class="sxs-lookup"><span data-stu-id="93685-141">This behavior ensures that the application will continue to receive notifications for the lifetime of the AudioVolumeEvents object.</span></span>

<span data-ttu-id="93685-142">DirectSound 或舊版 Windows 多媒體應用程式可能會允許使用者從以易記名稱識別的可用裝置清單中，明確地選取裝置，而不是根據裝置角色來隱含地選取音訊裝置。</span><span class="sxs-lookup"><span data-stu-id="93685-142">Instead of implicitly selecting an audio device based on its device role, a DirectSound or legacy Windows multimedia application might allow the user to explicitly select a device from a list of available devices that are identified by their friendly names.</span></span> <span data-ttu-id="93685-143">若要支援此行為，必須修改上述的程式碼範例，以產生所選裝置的音訊事件通知。</span><span class="sxs-lookup"><span data-stu-id="93685-143">To support this behavior, the preceding code example must be modified to generate audio-event notifications for the selected device.</span></span> <span data-ttu-id="93685-144">需要進行兩個修改。</span><span class="sxs-lookup"><span data-stu-id="93685-144">Two modifications are required.</span></span> <span data-ttu-id="93685-145">首先，變更函式定義以接受 [端點識別碼字串](endpoint-id-strings.md) 做為輸入參數， (取代程式碼範例) 中的流程和角色參數。</span><span class="sxs-lookup"><span data-stu-id="93685-145">First, change the constructor definition to accept an [endpoint ID string](endpoint-id-strings.md) as an input parameter (in place of the flow and role parameters in the code example).</span></span> <span data-ttu-id="93685-146">這個字串會識別對應于所選 DirectSound 或舊版波形裝置的音訊端點裝置。</span><span class="sxs-lookup"><span data-stu-id="93685-146">This string identifies the audio endpoint device that corresponds to the selected DirectSound or legacy waveform device.</span></span> <span data-ttu-id="93685-147">其次，將 [**IMMDeviceEnumerator：： GetDefaultAudioEndpoint**](/windows/desktop/api/Mmdeviceapi/nf-mmdeviceapi-immdeviceenumerator-getdefaultaudioendpoint) 方法的呼叫取代為 [**IMMDeviceEnumerator：： GetDevice**](/windows/desktop/api/Mmdeviceapi/nf-mmdeviceapi-immdeviceenumerator-getdevice) 方法的呼叫。</span><span class="sxs-lookup"><span data-stu-id="93685-147">Second, replace the call to the [**IMMDeviceEnumerator::GetDefaultAudioEndpoint**](/windows/desktop/api/Mmdeviceapi/nf-mmdeviceapi-immdeviceenumerator-getdefaultaudioendpoint) method with a call to the [**IMMDeviceEnumerator::GetDevice**](/windows/desktop/api/Mmdeviceapi/nf-mmdeviceapi-immdeviceenumerator-getdevice) method.</span></span> <span data-ttu-id="93685-148">**GetDevice** 呼叫會採用端點識別碼字串做為輸入參數，並建立由字串識別之端點裝置的實例。</span><span class="sxs-lookup"><span data-stu-id="93685-148">The **GetDevice** call takes the endpoint ID string as an input parameter and creates an instance of the endpoint device that is identified by the string.</span></span>

<span data-ttu-id="93685-149">為 DirectSound 裝置或舊版波形裝置取得端點識別碼字串的技術如下所示。</span><span class="sxs-lookup"><span data-stu-id="93685-149">The technique for obtaining the endpoint ID string for a DirectSound device or legacy waveform device is as follows.</span></span>

<span data-ttu-id="93685-150">首先，在裝置列舉期間，DirectSound 會提供每個列舉裝置的端點識別碼字串。</span><span class="sxs-lookup"><span data-stu-id="93685-150">First, during device enumeration, DirectSound supplies the endpoint ID string for each enumerated device.</span></span> <span data-ttu-id="93685-151">若要開始裝置列舉，應用程式會將回呼函式指標當作輸入參數傳遞給 **DirectSoundCreate** 或 **DirectSoundCaptureCreate** 函數。</span><span class="sxs-lookup"><span data-stu-id="93685-151">To begin device enumeration, the application passes a callback function pointer as an input parameter to the **DirectSoundCreate** or **DirectSoundCaptureCreate** function.</span></span> <span data-ttu-id="93685-152">回呼函數的定義為：</span><span class="sxs-lookup"><span data-stu-id="93685-152">The definition of the callback function is:</span></span>


```C++
BOOL DSEnumCallback(
  LPGUID  lpGuid,
  LPCSTR  lpcstrDescription,
  LPCSTR  lpcstrModule,
  LPVOID  lpContext
);
```



<span data-ttu-id="93685-153">在 Windows Vista 中， *lpcstrModule* 參數會指向端點識別碼字串。</span><span class="sxs-lookup"><span data-stu-id="93685-153">In Windows Vista, the *lpcstrModule* parameter points to the endpoint ID string.</span></span> <span data-ttu-id="93685-154"> (在舊版 Windows 中，包括 Windows Server 2003、Windows XP 及 Windows 2000， *lpcstrModule* 參數會指向裝置的驅動程式模組名稱。 ) *lpcstrDescription* 參數指向包含裝置易記名稱的字串。</span><span class="sxs-lookup"><span data-stu-id="93685-154">(In earlier versions of Windows, including Windows Server 2003, Windows XP, and Windows 2000, the *lpcstrModule* parameter points to the name of the driver module for the device.) The *lpcstrDescription* parameter points to a string that contains the friendly name of the device.</span></span> <span data-ttu-id="93685-155">如需 DirectSound 裝置列舉的詳細資訊，請參閱 Windows SDK 檔。</span><span class="sxs-lookup"><span data-stu-id="93685-155">For more information about DirectSound device enumeration, see the Windows SDK documentation.</span></span>

<span data-ttu-id="93685-156">其次，若要取得舊版波形裝置的端點識別碼字串，請使用 **waveOutMessage** 或 **waveInMessage** 函式，將 winspool.drv \_ QUERYFUNCTIONINSTANCEID 訊息傳送到波形設備磁碟機。</span><span class="sxs-lookup"><span data-stu-id="93685-156">Second, to obtain the endpoint ID string for a legacy waveform device, use the **waveOutMessage** or **waveInMessage** function to send a DRV\_QUERYFUNCTIONINSTANCEID message to the waveform device driver.</span></span> <span data-ttu-id="93685-157">如需示範如何使用此訊息的程式碼範例，請參閱 [舊版 Windows 多媒體應用程式的裝置角色](device-roles-for-legacy-windows-multimedia-applications.md)。</span><span class="sxs-lookup"><span data-stu-id="93685-157">For a code example that shows the use of this message, see [Device Roles for Legacy Windows Multimedia Applications](device-roles-for-legacy-windows-multimedia-applications.md).</span></span>

## <a name="related-topics"></a><span data-ttu-id="93685-158">相關主題</span><span class="sxs-lookup"><span data-stu-id="93685-158">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="93685-159">與舊版音訊 Api 的互通性</span><span class="sxs-lookup"><span data-stu-id="93685-159">Interoperability with Legacy Audio APIs</span></span>](interoperability-with-legacy-audio-apis.md)
</dt> </dl>

 

 



