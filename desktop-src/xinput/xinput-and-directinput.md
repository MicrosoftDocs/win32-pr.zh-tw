---
title: XInput 和 DirectInput
description: XInput 是可讓應用程式從適用于 Windows 的 Xbox Controller 接收輸入的 API。
ms.assetid: 0f29a47b-24ed-c0fa-e9e9-8a061619845c
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 2dcdbc31a66d4928b52ae5d097cab0e877f6f078
ms.sourcegitcommit: 48d4947b16f1ed1eaf6fae2b75954b736dd25450
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/29/2020
ms.locfileid: "103683208"
---
# <a name="xinput-and-directinput"></a>XInput 和 DirectInput

XInput 是可讓應用程式從適用于 Windows 的 Xbox Controller 接收輸入的 API。 本檔說明 Xbox 控制器的 XInput 和 [DirectInput](/previous-versions/windows/desktop/ee416842(v=vs.85)) 執行之間的差異，以及您可以同時支援 XInput 裝置和舊版 DirectInput 裝置的方式。

> [!Note]  
> 不建議使用舊版 [DirectInput](/previous-versions/windows/desktop/ee416842(v=vs.85)) ，DirectInput 無法用於 Windows Store 應用程式。

## <a name="the-new-standard-xinput"></a>新標準： XInput

XInput 現在可供遊戲開發之用。 這是 Xbox 和 Windows 的新輸入標準。 Api 可透過 DirectX SDK 取得，而驅動程式可透過 Windows Update 取得。

在 [DirectInput](/previous-versions/windows/desktop/ee416842(v=vs.85))上使用 XInput 有幾個優點：

-   XInput 比[DirectInput](/previous-versions/windows/desktop/ee416842(v=vs.85))更容易使用，而且需要較少的安裝程式
-   Xbox 和 Windows 程式設計都將使用相同的核心 Api 集合，讓程式設計能夠更輕鬆地轉譯跨平臺
-   Xbox 控制器將會有一個大型安裝的基底
-   XInput 裝置 (也就是說，Xbox 控制器) 只有在使用 XInput Api 時，才會有震動功能
-   針對 Xbox 主控台推出的未來控制器 (也就是，方向盤) 也可以在 Windows 上運作

### <a name="using-the-xbox-controller-with-directinput"></a>搭配使用 Xbox 控制器與 DirectInput

Xbox 控制器會在 [DirectInput](/previous-versions/windows/desktop/ee416842(v=vs.85))上正確列舉，並且可以搭配 DirectInputAPIs 使用。 不過，XInput 所提供的某些功能將會從 DirectInput 的執行中遺失：

-   左和右觸發程式按鈕將作為單一按鈕，而不是獨立的
-   振動效果將無法使用
-   查詢耳機裝置將無法使用

[DirectInput](/previous-versions/windows/desktop/ee416842(v=vs.85))中的左和右觸發程式組合是依設計而成。 遊戲一律假設在沒有任何使用者與裝置互動時，會將 DirectInput 裝置軸置中。 不過，Xbox 控制器的設計是在未持有觸發程式時，註冊最小值，而不是置中。 因此，較舊的遊戲會採用使用者互動。

解決方法是合併觸發程式、將觸發程式設定為正面方向，並將另一個觸發程式設為負面方向，因此沒有使用者互動表示 [DirectInput](/previous-versions/windows/desktop/ee416842(v=vs.85)) 「控制項」。

為了個別測試觸發程式值，您必須使用 XInput。

## <a name="xinput-and-directinput-side-by-side"></a>XInput 和 DirectInput 並存

藉由僅支援 XInput，您的遊戲將無法搭配舊版 [DirectInput](/previous-versions/windows/desktop/ee416842(v=vs.85)) 裝置使用。 XInput 將無法辨識這些裝置。

如果您想要讓遊戲支援舊版 [DirectInput](/previous-versions/windows/desktop/ee416842(v=vs.85)) 裝置，您可以使用 DirectInput 和 XInput 並存。 列舉 DirectInput 裝置時，會正確地列舉所有 DirectInput 裝置。 所有 XInput 裝置都將顯示為 XInput 和 DirectInput 裝置，但不應該透過 DirectInput 來處理。 您必須判斷哪些 DirectInput 裝置是舊版裝置，哪些是 XInput 裝置，並將它們從 DirectInput 裝置的列舉中移除。

若要這樣做，請將下列程式碼插入您的 DirectInput 列舉回呼：

```cpp
#include <wbemidl.h>
#include <oleauto.h>
#include <wmsstd.h>

//-----------------------------------------------------------------------------
// Enum each PNP device using WMI and check each device ID to see if it contains 
// "IG_" (ex. "VID_045E&PID_028E&IG_00").  If it does, then it's an XInput device
// Unfortunately this information can not be found by just using DirectInput 
//-----------------------------------------------------------------------------
BOOL IsXInputDevice( const GUID* pGuidProductFromDirectInput )
{
    IWbemLocator*           pIWbemLocator  = NULL;
    IEnumWbemClassObject*   pEnumDevices   = NULL;
    IWbemClassObject*       pDevices[20]   = {0};
    IWbemServices*          pIWbemServices = NULL;
    BSTR                    bstrNamespace  = NULL;
    BSTR                    bstrDeviceID   = NULL;
    BSTR                    bstrClassName  = NULL;
    DWORD                   uReturned      = 0;
    bool                    bIsXinputDevice= false;
    UINT                    iDevice        = 0;
    VARIANT                 var;
    HRESULT                 hr;

    // CoInit if needed
    hr = CoInitialize(NULL);
    bool bCleanupCOM = SUCCEEDED(hr);

    // So we can call VariantClear() later, even if we never had a successful IWbemClassObject::Get().
    VariantInit(&var);

    // Create WMI
    hr = CoCreateInstance( __uuidof(WbemLocator),
                           NULL,
                           CLSCTX_INPROC_SERVER,
                           __uuidof(IWbemLocator),
                           (LPVOID*) &pIWbemLocator);
    if( FAILED(hr) || pIWbemLocator == NULL )
        goto LCleanup;

    bstrNamespace = SysAllocString( L"\\\\.\\root\\cimv2" );if( bstrNamespace == NULL ) goto LCleanup;        
    bstrClassName = SysAllocString( L"Win32_PNPEntity" );   if( bstrClassName == NULL ) goto LCleanup;        
    bstrDeviceID  = SysAllocString( L"DeviceID" );          if( bstrDeviceID == NULL )  goto LCleanup;        
    
    // Connect to WMI 
    hr = pIWbemLocator->ConnectServer( bstrNamespace, NULL, NULL, 0L, 
                                       0L, NULL, NULL, &pIWbemServices );
    if( FAILED(hr) || pIWbemServices == NULL )
        goto LCleanup;

    // Switch security level to IMPERSONATE. 
    CoSetProxyBlanket( pIWbemServices, RPC_C_AUTHN_WINNT, RPC_C_AUTHZ_NONE, NULL, 
                       RPC_C_AUTHN_LEVEL_CALL, RPC_C_IMP_LEVEL_IMPERSONATE, NULL, EOAC_NONE );                    

    hr = pIWbemServices->CreateInstanceEnum( bstrClassName, 0, NULL, &pEnumDevices ); 
    if( FAILED(hr) || pEnumDevices == NULL )
        goto LCleanup;

    // Loop over all devices
    for( ;; )
    {
        // Get 20 at a time
        hr = pEnumDevices->Next( 10000, 20, pDevices, &uReturned );
        if( FAILED(hr) )
            goto LCleanup;
        if( uReturned == 0 )
            break;

        for( iDevice=0; iDevice<uReturned; iDevice++ )
        {
            // For each device, get its device ID
            hr = pDevices[iDevice]->Get( bstrDeviceID, 0L, &var, NULL, NULL );
            if( SUCCEEDED( hr ) && var.vt == VT_BSTR && var.bstrVal != NULL )
            {
                // Check if the device ID contains "IG_".  If it does, then it's an XInput device
                    // This information can not be found from DirectInput 
                if( wcsstr( var.bstrVal, L"IG_" ) )
                {
                    // If it does, then get the VID/PID from var.bstrVal
                    DWORD dwPid = 0, dwVid = 0;
                    WCHAR* strVid = wcsstr( var.bstrVal, L"VID_" );
                    if( strVid && swscanf( strVid, L"VID_%4X", &dwVid ) != 1 )
                        dwVid = 0;
                    WCHAR* strPid = wcsstr( var.bstrVal, L"PID_" );
                    if( strPid && swscanf( strPid, L"PID_%4X", &dwPid ) != 1 )
                        dwPid = 0;

                    // Compare the VID/PID to the DInput device
                    DWORD dwVidPid = MAKELONG( dwVid, dwPid );
                    if( dwVidPid == pGuidProductFromDirectInput->Data1 )
                    {
                        bIsXinputDevice = true;
                        goto LCleanup;
                    }
                }
            }
            VariantClear(&var);
            SAFE_RELEASE( pDevices[iDevice] );
        }
    }

LCleanup:
    VariantClear(&var);
    if(bstrNamespace)
        SysFreeString(bstrNamespace);
    if(bstrDeviceID)
        SysFreeString(bstrDeviceID);
    if(bstrClassName)
        SysFreeString(bstrClassName);
    for( iDevice=0; iDevice<20; iDevice++ )
        SAFE_RELEASE( pDevices[iDevice] );
    SAFE_RELEASE( pEnumDevices );
    SAFE_RELEASE( pIWbemLocator );
    SAFE_RELEASE( pIWbemServices );

    if( bCleanupCOM )
        CoUninitialize();

    return bIsXinputDevice;
}


//-----------------------------------------------------------------------------
// Name: EnumJoysticksCallback()
// Desc: Called once for each enumerated joystick. If we find one, create a
//       device interface on it so we can play with it.
//-----------------------------------------------------------------------------
BOOL CALLBACK EnumJoysticksCallback( const DIDEVICEINSTANCE* pdidInstance,
                                     VOID* pContext )
{
    HRESULT hr;

    if( IsXInputDevice( &pdidInstance->guidProduct ) )
        return DIENUM_CONTINUE;

     // Device is verified not XInput, so add it to the list of DInput devices

     return DIENUM_CONTINUE;    
}
```

## <a name="related-topics"></a>相關主題

[使用 XInput 開始使用](getting-started-with-xinput.md)

[程式設計參考](programming-reference.md)
