---
description: 尖峰計量
ms.assetid: 02f5d1b4-ba4f-424a-897f-b113d1f7cd6b
title: 尖峰計量
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: e04a15ddd2e5fd91cf60845f2a939715e7a4a992f36aea3b9129e69c30d05961
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/11/2021
ms.locfileid: "119077502"
---
# <a name="peak-meters"></a>尖峰計量

為了支援顯示尖峰計量的 Windows 應用程式， [EndpointVolume API](endpointvolume-api.md)包含 [**IAudioMeterInformation**](/windows/desktop/api/Endpointvolume/nn-endpointvolume-iaudiometerinformation)介面。 此介面代表 [音訊端點裝置](audio-endpoint-devices.md)上的尖峰計量表。 針對轉譯裝置，從尖峰計量取出的值代表在先前的計量期間，輸出資料流程中遇到的最大取樣值。 若為捕獲裝置，從尖峰計量取出的值代表從裝置輸入資料流程中遇到的最大取樣值。

從 [**IAudioMeterInformation**](/windows/desktop/api/Endpointvolume/nn-endpointvolume-iaudiometerinformation) 介面中的方法取得的尖峰計量值是從0.0 到1.0 的正規化範圍中的浮點數。 例如，如果 PCM 串流包含16位範例，而在特定計量期間內的尖峰樣本值為-8914，則尖峰計量所記錄的絕對值為8914，而 **IAudioMeterInformation** 介面所報告的正規化尖峰值為 8914/32768 = 0.272。

如果音訊端點裝置在硬體中實行尖峰計量表， [**IAudioMeterInformation**](/windows/desktop/api/Endpointvolume/nn-endpointvolume-iaudiometerinformation) 介面會使用硬體尖峰計量表。 否則，此介面會在軟體中實行尖峰計量表。

如果裝置具有硬體尖峰計量，則尖峰計量在共用模式和獨佔模式下都是作用中狀態。 如果裝置缺少硬體尖峰計量表，尖峰計量會在共用模式中處於作用中狀態，但不會處於獨佔模式。 在獨佔模式中，應用程式和音訊硬體會直接交換音訊資料，略過軟體尖峰計量 (，這一律會報告尖峰值 0.0) 。

下列 c + + 程式碼範例是 Windows 的應用程式，會顯示預設轉譯裝置的尖峰計量表：


```C++
// Peakmeter.cpp -- WinMain and dialog box functions

#include <windows.h>
#include <mmdeviceapi.h>
#include <endpointvolume.h>
#include "resource.h"

static BOOL CALLBACK DlgProc(HWND, UINT, WPARAM, LPARAM);
static void DrawPeakMeter(HWND, float);

// Timer ID and period (in milliseconds)
#define ID_TIMER  1
#define TIMER_PERIOD  125

#define EXIT_ON_ERROR(hr)  \
              if (FAILED(hr)) { goto Exit; }
#define SAFE_RELEASE(punk)  \
              if ((punk) != NULL)  \
                { (punk)->Release(); (punk) = NULL; }

//-----------------------------------------------------------
// WinMain -- Opens a dialog box that contains a peak meter.
//   The peak meter displays the peak sample value that plays
//   through the default rendering device.
//-----------------------------------------------------------
int APIENTRY WinMain(HINSTANCE hInstance,
                     HINSTANCE hPrevInstance,
                     LPSTR lpCmdLine,
                     int nCmdShow)
{
    HRESULT hr;
    IMMDeviceEnumerator *pEnumerator = NULL;
    IMMDevice *pDevice = NULL;
    IAudioMeterInformation *pMeterInfo = NULL;

    if (hPrevInstance)
    {
        return 0;
    }

    CoInitialize(NULL);

    // Get enumerator for audio endpoint devices.
    hr = CoCreateInstance(__uuidof(MMDeviceEnumerator),
                          NULL, CLSCTX_INPROC_SERVER,
                          __uuidof(IMMDeviceEnumerator),
                          (void**)&pEnumerator);
    EXIT_ON_ERROR(hr)

    // Get peak meter for default audio-rendering device.
    hr = pEnumerator->GetDefaultAudioEndpoint(eRender, eConsole, &pDevice);
    EXIT_ON_ERROR(hr)

    hr = pDevice->Activate(__uuidof(IAudioMeterInformation),
                           CLSCTX_ALL, NULL, (void**)&pMeterInfo);
    EXIT_ON_ERROR(hr)

    DialogBoxParam(hInstance, L"PEAKMETER", NULL, (DLGPROC)DlgProc, (LPARAM)pMeterInfo);

Exit:
    if (FAILED(hr))
    {
        MessageBox(NULL, TEXT("This program requires Windows Vista."),
                   TEXT("Error termination"), MB_OK);
    }
    SAFE_RELEASE(pEnumerator)
    SAFE_RELEASE(pDevice)
    SAFE_RELEASE(pMeterInfo)
    CoUninitialize();
    return 0;
}

//-----------------------------------------------------------
// DlgProc -- Dialog box procedure
//-----------------------------------------------------------

BOOL CALLBACK DlgProc(HWND hDlg, UINT message, WPARAM wParam, LPARAM lParam)
{
    static IAudioMeterInformation *pMeterInfo = NULL;
    static HWND hPeakMeter = NULL;
    static float peak = 0;
    HRESULT hr;

    switch (message)
    {
    case WM_INITDIALOG:
        pMeterInfo = (IAudioMeterInformation*)lParam;
        SetTimer(hDlg, ID_TIMER, TIMER_PERIOD, NULL);
        hPeakMeter = GetDlgItem(hDlg, IDC_PEAK_METER);
        return TRUE;

    case WM_COMMAND:
        switch ((int)LOWORD(wParam))
        {
        case IDCANCEL:
            KillTimer(hDlg, ID_TIMER);
            EndDialog(hDlg, TRUE);
            return TRUE;
        }
        break;

    case WM_TIMER:
        switch ((int)wParam)
        {
        case ID_TIMER:
            // Update the peak meter in the dialog box.
            hr = pMeterInfo->GetPeakValue(&peak);
            if (FAILED(hr))
            {
                MessageBox(hDlg, TEXT("The program will exit."),
                           TEXT("Fatal error"), MB_OK);
                KillTimer(hDlg, ID_TIMER);
                EndDialog(hDlg, TRUE);
                return TRUE;
            }
            DrawPeakMeter(hPeakMeter, peak);
            return TRUE;
        }
        break;

    case WM_PAINT:
        // Redraw the peak meter in the dialog box.
        ValidateRect(hPeakMeter, NULL);
        DrawPeakMeter(hPeakMeter, peak);
        break;
    }
    return FALSE;
}

//-----------------------------------------------------------
// DrawPeakMeter -- Draws the peak meter in the dialog box.
//-----------------------------------------------------------

void DrawPeakMeter(HWND hPeakMeter, float peak)
{
    HDC hdc;
    RECT rect;

    GetClientRect(hPeakMeter, &rect);
    hdc = GetDC(hPeakMeter);
    FillRect(hdc, &rect, (HBRUSH)(COLOR_3DSHADOW+1));
    rect.left++;
    rect.top++;
    rect.right = rect.left +
                 max(0, (LONG)(peak*(rect.right-rect.left)-1.5));
    rect.bottom--;
    FillRect(hdc, &rect, (HBRUSH)(COLOR_3DHIGHLIGHT+1));
    ReleaseDC(hPeakMeter, hdc);
}
```



在上述程式碼範例中， [**WinMain**](/windows/win32/api/winbase/nf-winbase-winmain) 函式會呼叫 [**CoCreateInstance**](/windows/win32/api/combaseapi/nf-combaseapi-cocreateinstance) 函數來建立 [**IMMDeviceEnumerator**](/windows/desktop/api/Mmdeviceapi/nn-mmdeviceapi-immdeviceenumerator) 介面的實例，並呼叫 [**IMMDeviceEnumerator：： GetDefaultAudioEndpoint**](/windows/desktop/api/Mmdeviceapi/nf-mmdeviceapi-immdeviceenumerator-getdefaultaudioendpoint) 方法來取得預設轉譯裝置的 [**IMMDevice**](/windows/desktop/api/Mmdeviceapi/nn-mmdeviceapi-immdevice) 介面。 **WinMain** 會呼叫 [**IMMDevice：： Activate**](/windows/desktop/api/Mmdeviceapi/nf-mmdeviceapi-immdevice-activate) 方法來取得裝置的 [**IAudioMeterInformation**](/windows/desktop/api/Endpointvolume/nn-endpointvolume-iaudiometerinformation) 介面，並開啟對話方塊來顯示裝置的尖峰計量表。 如需有關 **WinMain** 和 **CoCreateInstance** 的詳細資訊，請參閱 Windows SDK 檔。 如需 **IMMDeviceEnumerator** 和 **IMMDevice** 的詳細資訊，請參閱 [列舉音訊裝置](enumerating-audio-devices.md)。

在上述程式碼範例中，DlgProc 函數會在對話方塊中顯示尖峰計量表。 在處理 WM \_ INITDIALOG 訊息時，DlgProc 會呼叫 [**SetTimer**](/windows/win32/api/winuser/nf-winuser-settimer) 函數來設定計時器，以定期產生 WM \_ 計時器訊息。 當 DlgProc 收到 WM \_ 計時器訊息時，它會呼叫 [**IAudioMeterInformation：： GetPeakValue**](/windows/desktop/api/Endpointvolume/nf-endpointvolume-iaudiometerinformation-getpeakvalue) 來取得資料流程的最新尖峰計量讀取。 然後，DlgProc 會呼叫 DrawPeakMeter 函式，以在對話方塊中繪製更新過的尖峰計量表。 如需 **SetTimer** 和 wm \_ INITDIALOG 和 wm 計時器訊息的詳細資訊 \_ ，請參閱 Windows SDK 檔。

您可以輕鬆地修改上述的程式碼範例，以顯示預設捕獲裝置的尖峰計量表。 在 [**WinMain**](/windows/win32/api/winbase/nf-winbase-winmain) 函式中，將 [**IMMDeviceEnumerator：： GetDefaultAudioEndpoint**](/windows/desktop/api/Mmdeviceapi/nf-mmdeviceapi-immdeviceenumerator-getdefaultaudioendpoint) 呼叫中的第一個參數值，從 eRender 變更為 eCapture。

下列程式碼範例是定義上述程式碼範例中所顯示控制項的資源腳本：


```C++
// Peakmeter.rc -- Resource script

#include "resource.h"
#include "windows.h"

//
// Dialog
//
PEAKMETER DIALOGEX 0, 0, 150, 34
STYLE DS_MODALFRAME | WS_CAPTION | WS_SYSMENU | DS_SETFONT
CAPTION "Peak Meter"
FONT 8, "Arial Rounded MT Bold", 400, 0, 0x0
BEGIN
    CTEXT      "",IDC_PEAK_METER,34,14,82,5
    LTEXT      "Min",IDC_STATIC_MINVOL,10,12,20,12
    RTEXT      "Max",IDC_STATIC_MAXVOL,120,12,20,12
END
```



下列程式碼範例是定義上述程式碼範例中所示控制項識別碼的資源標頭檔：


```C++
// Resource.h -- Control identifiers

#define IDC_STATIC_MINVOL      1001
#define IDC_STATIC_MAXVOL      1002
#define IDC_PEAK_METER         1003
```



## <a name="related-topics"></a>相關主題

<dl> <dt>

[音量控制項](volume-controls.md)
</dt> </dl>

 

 
