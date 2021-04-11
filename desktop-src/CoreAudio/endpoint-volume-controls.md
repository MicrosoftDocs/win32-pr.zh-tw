---
description: 端點磁片區控制項
ms.assetid: 667c3659-69ae-469d-9ae0-e32a189cbc71
title: 端點磁片區控制項
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 526403be9c600f67791650956bd7e5096f6c9afc
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/07/2021
ms.locfileid: "103936336"
---
# <a name="endpoint-volume-controls"></a>端點磁片區控制項

[**ISimpleAudioVolume**](/windows/desktop/api/Audioclient/nn-audioclient-isimpleaudiovolume)、 [**IChannelAudioVolume**](/windows/desktop/api/Audioclient/nn-audioclient-ichannelaudiovolume)和 [**IAudioStreamVolume**](/windows/desktop/api/Audioclient/nn-audioclient-iaudiostreamvolume)介面可讓用戶端控制 [音訊會話](audio-sessions.md)的音量層級，也就是共用模式音訊串流的集合。 這些介面無法搭配專用模式音訊串流使用。

管理獨佔模式資料流程的應用程式可以透過 [**IAudioEndpointVolume**](/windows/desktop/api/Endpointvolume/nn-endpointvolume-iaudioendpointvolume) 介面控制這些資料流程的磁片區層級。 此介面控制 [音訊端點裝置](audio-endpoint-devices.md)的音量層級。 如果音訊硬體實作為此類控制項，它會使用適用于端點裝置的硬體磁片區控制。 否則， **IAudioEndpointVolume** 介面會在軟體中實行音量控制項。

如果裝置具有硬體磁片區控制，透過 [**IAudioEndpointVolume**](/windows/desktop/api/Endpointvolume/nn-endpointvolume-iaudioendpointvolume) 介面對控制項所做的變更，會影響在共用模式和獨佔模式中的磁片區層級。 如果裝置缺少硬體磁片區和靜音控制項，則透過此介面對軟體磁片區和靜音控制所做的變更，會影響共用模式中的磁片區層級，但不會影響獨佔模式。 在獨佔模式中，應用程式和音訊硬體會直接交換音訊資料，略過軟體控制項。

一般來說，應用程式應該避免使用 [**IAudioEndpointVolume**](/windows/desktop/api/Endpointvolume/nn-endpointvolume-iaudioendpointvolume) 介面來控制共用模式資料流程的磁片區層級。 相反地，應用程式應該針對該用途使用 [**ISimpleAudioVolume**](/windows/desktop/api/Audioclient/nn-audioclient-isimpleaudiovolume)、 [**IChannelAudioVolume**](/windows/desktop/api/Audioclient/nn-audioclient-ichannelaudiovolume)或 [**IAudioStreamVolume**](/windows/desktop/api/Audioclient/nn-audioclient-iaudiostreamvolume) 介面。

如果應用程式顯示的音量控制項使用 [**IAudioEndpointVolume**](/windows/desktop/api/Endpointvolume/nn-endpointvolume-iaudioendpointvolume) 介面來控制音訊端點裝置的音量層級，該音量控制應該鏡像系統磁片區控制程式 Sndvol 所顯示的端點磁片區控制項。 如先前所述，端點磁片區控制項會出現在 [Sndvol] 視窗的左側，並標示為 [ **裝置**] 的群組方塊。 如果使用者透過 Sndvol 中的音量控制項變更裝置的端點磁片區，則應用程式中對應的端點磁片區控制項應該與 Sndvol 中的控制項一致移動。 同樣地，如果使用者透過應用程式視窗中的端點磁片區控制項變更音量層級，Sndvol 中對應的磁片區控制項應該與應用程式的磁片區控制項一致地移動。

為了確保應用程式視窗中的端點磁片區控制會在 Sndvol 中鏡像端點磁片區控制項，應用程式應該執行 [**IAudioEndpointVolumeCallback**](/windows/desktop/api/Endpointvolume/nn-endpointvolume-iaudioendpointvolumecallback) 介面，並註冊該介面以接收通知。 之後，每當使用者變更 Sndvol 中的端點磁片區層級時，應用程式就會透過其 [**IAudioEndpointVolumeCallback：： OnNotify**](/windows/desktop/api/Endpointvolume/nf-endpointvolume-iaudioendpointvolumecallback-onnotify) 方法接收通知呼叫。 在此呼叫過程中， **OnNotify** 方法可以更新應用程式視窗中的端點磁片區控制項，以符合 Sndvol 中所顯示的控制項設定。 同樣地，每當使用者透過應用程式視窗中的音量控制變更端點磁片區層級時，Sndvol 會收到通知，並立即更新其端點音量控制項，以顯示新的磁片區層級。

下列程式碼範例是標頭檔，顯示 [**IAudioEndpointVolumeCallback**](/windows/desktop/api/Endpointvolume/nn-endpointvolume-iaudioendpointvolumecallback) 介面的可能實作為：


```C++
// Epvolume.h -- Implementation of IAudioEndpointVolumeCallback interface

#include <windows.h>
#include <commctrl.h>
#include <mmdeviceapi.h>
#include <endpointvolume.h>
#include "resource.h"

// Dialog handle from dialog box procedure
extern HWND g_hDlg;

// Client's proprietary event-context GUID
extern GUID g_guidMyContext;

// Maximum volume level on trackbar
#define MAX_VOL  100

#define SAFE_RELEASE(punk)  \
              if ((punk) != NULL)  \
                { (punk)->Release(); (punk) = NULL; }

//-----------------------------------------------------------
// Client implementation of IAudioEndpointVolumeCallback
// interface. When a method in the IAudioEndpointVolume
// interface changes the volume level or muting state of the
// endpoint device, the change initiates a call to the
// client's IAudioEndpointVolumeCallback::OnNotify method.
//-----------------------------------------------------------
class CAudioEndpointVolumeCallback : public IAudioEndpointVolumeCallback
{
    LONG _cRef;

public:
    CAudioEndpointVolumeCallback() :
        _cRef(1)
    {
    }

    ~CAudioEndpointVolumeCallback()
    {
    }

    // IUnknown methods -- AddRef, Release, and QueryInterface

    ULONG STDMETHODCALLTYPE AddRef()
    {
        return InterlockedIncrement(&_cRef);
    }

    ULONG STDMETHODCALLTYPE Release()
    {
        ULONG ulRef = InterlockedDecrement(&_cRef);
        if (0 == ulRef)
        {
            delete this;
        }
        return ulRef;

    }

    HRESULT STDMETHODCALLTYPE QueryInterface(REFIID riid, VOID **ppvInterface)
    {
        if (IID_IUnknown == riid)
        {
            AddRef();
            *ppvInterface = (IUnknown*)this;
        }
        else if (__uuidof(IAudioEndpointVolumeCallback) == riid)
        {
            AddRef();
            *ppvInterface = (IAudioEndpointVolumeCallback*)this;
        }
        else
        {
            *ppvInterface = NULL;
            return E_NOINTERFACE;
        }
        return S_OK;
    }

    // Callback method for endpoint-volume-change notifications.

    HRESULT STDMETHODCALLTYPE OnNotify(PAUDIO_VOLUME_NOTIFICATION_DATA pNotify)
    {
        if (pNotify == NULL)
        {
            return E_INVALIDARG;
        }
        if (g_hDlg != NULL && pNotify->guidEventContext != g_guidMyContext)
        {
            PostMessage(GetDlgItem(g_hDlg, IDC_CHECK_MUTE), BM_SETCHECK,
                        (pNotify->bMuted) ? BST_CHECKED : BST_UNCHECKED, 0);

            PostMessage(GetDlgItem(g_hDlg, IDC_SLIDER_VOLUME),
                        TBM_SETPOS, TRUE,
                        LPARAM((UINT32)(MAX_VOL*pNotify->fMasterVolume + 0.5)));
        }
        return S_OK;
    }
};
```



上述程式碼範例中的 CAudioEndpointVolumeCallback 類別是 [**IAudioEndpointVolumeCallback**](/windows/desktop/api/Endpointvolume/nn-endpointvolume-iaudioendpointvolumecallback) 介面的實作為。 由於 **IAudioEndpointVolumeCallback** 繼承自 [**iunknown**](/windows/desktop/api/unknwn/nn-unknwn-iunknown)，因此類別定義包含 **iunknown** 方法 [**AddRef**](/windows/desktop/api/unknwn/nf-unknwn-iunknown-addref)、 [**Release**](/windows/desktop/api/unknwn/nf-unknwn-iunknown-release)和 [**QueryInterface**](/windows/desktop/api/unknwn/nf-unknwn-iunknown-queryinterface(q))的實作為。 每次下列其中一個方法變更端點磁片區層級時，就會呼叫類別定義中的 [**OnNotify**](/windows/desktop/api/Endpointvolume/nf-endpointvolume-iaudioendpointvolumecallback-onnotify) 方法：

-   [**IAudioEndpointVolume::SetChannelVolumeLevel**](/windows/desktop/api/Endpointvolume/nf-endpointvolume-iaudioendpointvolume-setchannelvolumelevel)
-   [**IAudioEndpointVolume::SetChannelVolumeLevelScalar**](/windows/desktop/api/Endpointvolume/nf-endpointvolume-iaudioendpointvolume-setchannelvolumelevelscalar)
-   [**IAudioEndpointVolume::SetMasterVolumeLevel**](/windows/desktop/api/Endpointvolume/nf-endpointvolume-iaudioendpointvolume-setmastervolumelevel)
-   [**IAudioEndpointVolume::SetMasterVolumeLevelScalar**](/windows/desktop/api/Endpointvolume/nf-endpointvolume-iaudioendpointvolume-setmastervolumelevelscalar)
-   [**IAudioEndpointVolume::SetMute**](/windows/desktop/api/Endpointvolume/nf-endpointvolume-iaudioendpointvolume-setmute)
-   [**IAudioEndpointVolume::VolumeStepDown**](/windows/desktop/api/Endpointvolume/nf-endpointvolume-iaudioendpointvolume-volumestepdown)
-   [**IAudioEndpointVolume::VolumeStepUp**](/windows/desktop/api/Endpointvolume/nf-endpointvolume-iaudioendpointvolume-volumestepup)

上述程式碼範例中的 [**OnNotify**](/windows/desktop/api/Endpointvolume/nf-endpointvolume-iaudioendpointvolumecallback-onnotify) 方法執行會將訊息傳送至應用程式視窗中的音量控制項，以更新顯示的音量層級。

應用程式會呼叫 [**IAudioEndpointVolume：： RegisterControlChangeNotify**](/windows/desktop/api/Endpointvolume/nf-endpointvolume-iaudioendpointvolume-registercontrolchangenotify) 方法來註冊其 [**IAudioEndpointVolumeCallback**](/windows/desktop/api/Endpointvolume/nn-endpointvolume-iaudioendpointvolumecallback) 介面，以接收通知。 當應用程式不再需要通知時，它會呼叫 [**IAudioEndpointVolume：： UnregisterControlChangeNotify**](/windows/desktop/api/Endpointvolume/nf-endpointvolume-iaudioendpointvolume-unregistercontrolchangenotify) 方法來刪除註冊。

下列程式碼範例是 Windows 應用程式，它會呼叫 [**RegisterControlChangeNotify**](/windows/desktop/api/Endpointvolume/nf-endpointvolume-iaudioendpointvolume-registercontrolchangenotify) 和 [**UnregisterControlChangeNotify**](/windows/desktop/api/Endpointvolume/nf-endpointvolume-iaudioendpointvolume-unregistercontrolchangenotify) 方法，以在上述程式碼範例中註冊和取消註冊 CAudioEndpointVolumeCallback 類別：


```C++
// Epvolume.cpp -- WinMain and dialog box functions

#include "stdafx.h"
#include "Epvolume.h"

HWND g_hDlg = NULL;
GUID g_guidMyContext = GUID_NULL;

static IAudioEndpointVolume *g_pEndptVol = NULL;
static BOOL CALLBACK DlgProc(HWND, UINT, WPARAM, LPARAM);

#define EXIT_ON_ERROR(hr)  \
              if (FAILED(hr)) { goto Exit; }
#define ERROR_CANCEL(hr)  \
              if (FAILED(hr)) {  \
                  MessageBox(hDlg, TEXT("The program will exit."),  \
                             TEXT("Fatal error"), MB_OK);  \
                  EndDialog(hDlg, TRUE); return TRUE; }

//-----------------------------------------------------------
// WinMain -- Registers an IAudioEndpointVolumeCallback
//   interface to monitor endpoint volume level, and opens
//   a dialog box that displays a volume control that will
//   mirror the endpoint volume control in SndVol.
//-----------------------------------------------------------
int APIENTRY WinMain(HINSTANCE hInstance,
                     HINSTANCE hPrevInstance,
                     LPSTR lpCmdLine,
                     int nCmdShow)
{
    HRESULT hr = S_OK;
    IMMDeviceEnumerator *pEnumerator = NULL;
    IMMDevice *pDevice = NULL;
    CAudioEndpointVolumeCallback EPVolEvents;

    if (hPrevInstance)
    {
        return 0;
    }

    CoInitialize(NULL);

    hr = CoCreateGuid(&g_guidMyContext);
    EXIT_ON_ERROR(hr)

    // Get enumerator for audio endpoint devices.
    hr = CoCreateInstance(__uuidof(MMDeviceEnumerator),
                          NULL, CLSCTX_INPROC_SERVER,
                          __uuidof(IMMDeviceEnumerator),
                          (void**)&pEnumerator);
    EXIT_ON_ERROR(hr)

    // Get default audio-rendering device.
    hr = pEnumerator->GetDefaultAudioEndpoint(eRender, eConsole, &pDevice);
    EXIT_ON_ERROR(hr)

    hr = pDevice->Activate(__uuidof(IAudioEndpointVolume),
                           CLSCTX_ALL, NULL, (void**)&g_pEndptVol);
    EXIT_ON_ERROR(hr)

    hr = g_pEndptVol->RegisterControlChangeNotify(
                     (IAudioEndpointVolumeCallback*)&EPVolEvents);
    EXIT_ON_ERROR(hr)

    InitCommonControls();
    DialogBox(hInstance, L"VOLUMECONTROL", NULL, (DLGPROC)DlgProc);

Exit:
    if (FAILED(hr))
    {
        MessageBox(NULL, TEXT("This program requires Windows Vista."),
                   TEXT("Error termination"), MB_OK);
    }
    if (pEnumerator != NULL)
    {
        g_pEndptVol->UnregisterControlChangeNotify(
                    (IAudioEndpointVolumeCallback*)&EPVolEvents);
    }
    SAFE_RELEASE(pEnumerator)
    SAFE_RELEASE(pDevice)
    SAFE_RELEASE(g_pEndptVol)
    CoUninitialize();
    return 0;
}

//-----------------------------------------------------------
// DlgProc -- Dialog box procedure
//-----------------------------------------------------------

BOOL CALLBACK DlgProc(HWND hDlg, UINT message, WPARAM wParam, LPARAM lParam)
{
    HRESULT hr;
    BOOL bMute;
    float fVolume;
    int nVolume;
    int nChecked;

    switch (message)
    {
    case WM_INITDIALOG:
        g_hDlg = hDlg;
        SendDlgItemMessage(hDlg, IDC_SLIDER_VOLUME, TBM_SETRANGEMIN, FALSE, 0);
        SendDlgItemMessage(hDlg, IDC_SLIDER_VOLUME, TBM_SETRANGEMAX, FALSE, MAX_VOL);
        hr = g_pEndptVol->GetMute(&bMute);
        ERROR_CANCEL(hr)
        SendDlgItemMessage(hDlg, IDC_CHECK_MUTE, BM_SETCHECK,
                           bMute ? BST_CHECKED : BST_UNCHECKED, 0);
        hr = g_pEndptVol->GetMasterVolumeLevelScalar(&fVolume);
        ERROR_CANCEL(hr)
        nVolume = (int)(MAX_VOL*fVolume + 0.5);
        SendDlgItemMessage(hDlg, IDC_SLIDER_VOLUME, TBM_SETPOS, TRUE, nVolume);
        return TRUE;

    case WM_HSCROLL:
        switch (LOWORD(wParam))
        {
        case SB_THUMBPOSITION:
        case SB_THUMBTRACK:
        case SB_LINERIGHT:
        case SB_LINELEFT:
        case SB_PAGERIGHT:
        case SB_PAGELEFT:
        case SB_RIGHT:
        case SB_LEFT:
            // The user moved the volume slider in the dialog box.
            SendDlgItemMessage(hDlg, IDC_CHECK_MUTE, BM_SETCHECK, BST_UNCHECKED, 0);
            hr = g_pEndptVol->SetMute(FALSE, &g_guidMyContext);
            ERROR_CANCEL(hr)
            nVolume = SendDlgItemMessage(hDlg, IDC_SLIDER_VOLUME, TBM_GETPOS, 0, 0);
            fVolume = (float)nVolume/MAX_VOL;
            hr = g_pEndptVol->SetMasterVolumeLevelScalar(fVolume, &g_guidMyContext);
            ERROR_CANCEL(hr)
            return TRUE;
        }
        break;

    case WM_COMMAND:
        switch ((int)LOWORD(wParam))
        {
        case IDC_CHECK_MUTE:
            // The user selected the Mute check box in the dialog box.
            nChecked = SendDlgItemMessage(hDlg, IDC_CHECK_MUTE, BM_GETCHECK, 0, 0);
            bMute = (BST_CHECKED == nChecked);
            hr = g_pEndptVol->SetMute(bMute, &g_guidMyContext);
            ERROR_CANCEL(hr)
            return TRUE;
        case IDCANCEL:
            EndDialog(hDlg, TRUE);
            return TRUE;
        }
        break;
    }
    return FALSE;
}
```



在上述程式碼範例中， [**WinMain**](/windows/desktop/api/winbase/nf-winbase-winmain) 函式會呼叫 [**CoCreateInstance**](/windows/desktop/api/combaseapi/nf-combaseapi-cocreateinstance) 函數來建立 [**IMMDeviceEnumerator**](/windows/desktop/api/Mmdeviceapi/nn-mmdeviceapi-immdeviceenumerator) 介面的實例，並呼叫 [**IMMDeviceEnumerator：： GetDefaultAudioEndpoint**](/windows/desktop/api/Mmdeviceapi/nf-mmdeviceapi-immdeviceenumerator-getdefaultaudioendpoint) 方法來取得預設轉譯裝置的 [**IMMDevice**](/windows/desktop/api/Mmdeviceapi/nn-mmdeviceapi-immdevice) 介面。 **WinMain** 會呼叫 [**IMMDevice：： Activate**](/windows/desktop/api/Mmdeviceapi/nf-mmdeviceapi-immdevice-activate) 方法來取得裝置的 [**IAudioEndpointVolume**](/windows/desktop/api/Endpointvolume/nn-endpointvolume-iaudioendpointvolume) 介面，然後呼叫 [**RegisterControlChangeNotify**](/windows/desktop/api/Endpointvolume/nf-endpointvolume-iaudioendpointvolume-registercontrolchangenotify) 來註冊應用程式，以接收端點磁片區變更的通知。 接下來， **WinMain** 會開啟對話方塊，以顯示裝置的端點音量控制項。 對話方塊也會顯示一個核取方塊，指出裝置是否已靜音。 對話方塊中的 [端點音量控制和靜音] 核取方塊會反映 Sndvol 所顯示之端點磁片區控制和靜音核取方塊的設定。 如需有關 **WinMain** 和 **CoCreateInstance** 的詳細資訊，請參閱 Windows SDK 檔。 如需 **IMMDeviceEnumerator** 和 **IMMDevice** 的詳細資訊，請參閱 [列舉音訊裝置](enumerating-audio-devices.md)。

上述程式碼範例中的對話方塊程式 DlgProc 會處理使用者對音量進行的變更，並透過對話方塊中的控制項將設定靜音。 當 DlgProc 呼叫 [**SetMasterVolumeLevelScalar**](/windows/desktop/api/Endpointvolume/nf-endpointvolume-iaudioendpointvolume-setmastervolumelevelscalar) 或 [**SetMute**](/windows/desktop/api/Endpointvolume/nf-endpointvolume-iaudioendpointvolume-setmute)時，Sndvol 會收到變更的通知，並在其視窗中更新對應的控制項，以反映新的音量或靜音設定。 如果使用者透過 Sndvol 視窗中的控制項來更新磁片區和靜音設定，而不是使用對話方塊，則 CAudioEndpointVolumeCallback 類別中的 [**OnNotify**](/windows/desktop/api/Endpointvolume/nf-endpointvolume-iaudioendpointvolumecallback-onnotify) 方法會更新對話方塊中的控制項，以顯示新的設定。

如果使用者透過對話方塊中的控制項來變更磁片區，則 CAudioEndpointVolumeCallback 類別中的 [**OnNotify**](/windows/desktop/api/Endpointvolume/nf-endpointvolume-iaudioendpointvolumecallback-onnotify) 方法不會傳送訊息，以更新對話方塊中的控制項。 若要這樣做，這會是多餘的。 **OnNotify** 只會在磁片區變更源自 Sndvol 或某個其他應用程式時，才更新對話方塊中的控制項。 [**SetMasterVolumeLevelScalar**](/windows/desktop/api/Endpointvolume/nf-endpointvolume-iaudioendpointvolume-setmastervolumelevelscalar)和 [**SetMute**](/windows/desktop/api/Endpointvolume/nf-endpointvolume-iaudioendpointvolume-setmute)方法中的第二個參數會在 DlgProc 函式中呼叫，這是一個方法傳遞至 **OnNotify** 的事件內容 GUID 指標。 **OnNotify** 會檢查事件內容 GUID 的值，以判斷對話方塊是否為磁片區變更的來源。 如需事件內容 Guid 的詳細資訊，請參閱 **IAudioEndpointVolumeCallback：： OnNotify**。

當使用者結束對話方塊時，上述程式碼範例中的 [**UnregisterControlChangeNotify**](/windows/desktop/api/Endpointvolume/nf-endpointvolume-iaudioendpointvolume-unregistercontrolchangenotify) 呼叫會在程式終止之前刪除 CAudioEndpointVolumeCallback 類別的註冊。

您可以輕鬆地修改上述的程式碼範例，以顯示預設捕獲裝置的音量和靜音控制項。 在 [**WinMain**](/windows/desktop/api/winbase/nf-winbase-winmain) 函數中，將 [**IMMDeviceEnumerator：： GetDefaultAudioEndpoint**](/windows/desktop/api/Mmdeviceapi/nf-mmdeviceapi-immdeviceenumerator-getdefaultaudioendpoint) 方法呼叫中的第一個參數值，從 eRender 變更為 eCapture。

下列程式碼範例是定義上述程式碼範例中所示之音量和靜音控制項的資源腳本：


```C++
// Epvolume.rc -- Resource script

#include "resource.h"
#include "windows.h"
#include "commctrl.h"

//
// Dialog box
//
VOLUMECONTROL DIALOGEX 0, 0, 160, 60
STYLE DS_MODALFRAME | WS_CAPTION | WS_SYSMENU | DS_SETFONT
CAPTION "Audio Endpoint Volume"
FONT 8, "Arial Rounded MT Bold", 400, 0, 0x0
BEGIN
    LTEXT      "Min",IDC_STATIC_MINVOL,10,10,20,12
    RTEXT      "Max",IDC_STATIC_MAXVOL,130,10,20,12
    CONTROL    "",IDC_SLIDER_VOLUME,"msctls_trackbar32",
               TBS_BOTH | TBS_NOTICKS | WS_TABSTOP,10,20,140,12
    CONTROL    "Mute",IDC_CHECK_MUTE,"Button",
               BS_AUTOCHECKBOX | WS_TABSTOP,20,40,70,12
END
```



下列程式碼範例是定義上述程式碼範例中所示控制項識別碼的資源標頭檔：


```C++
// Resource.h -- Control identifiers (epvolume)

#define IDC_SLIDER_VOLUME      1001
#define IDC_CHECK_MUTE         1002
#define IDC_STATIC_MINVOL      1003
#define IDC_STATIC_MAXVOL      1004
```



上述程式碼範例會合並以形成簡單的應用程式，以控制和監視預設轉譯裝置的端點磁片區。 當裝置的狀態變更時，更有用的應用程式可能會另外通知使用者。 例如，裝置可能已停用、已拔下或移除。 如需監視這些事件種類的詳細資訊，請參閱 [裝置事件](device-events.md)。

## <a name="related-topics"></a>相關主題

<dl> <dt>

[音量控制項](volume-controls.md)
</dt> </dl>

 

 
