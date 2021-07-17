---
title: XInput 和 DirectInput
description: XInput 是一種 API，可讓應用程式從 Xbox Controller 接收 Windows 的輸入。
ms.assetid: 0f29a47b-24ed-c0fa-e9e9-8a061619845c
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 58339616f1e9e3a43529b6853bfc193d359ef11e
ms.sourcegitcommit: b3839bea8d55c981d53cb8802d666bf49093b428
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 07/16/2021
ms.locfileid: "114373193"
---
# <a name="xinput-and-directinput"></a><span data-ttu-id="37827-103">XInput 和 DirectInput</span><span class="sxs-lookup"><span data-stu-id="37827-103">XInput and DirectInput</span></span>

<span data-ttu-id="37827-104">XInput 是一種 API，可讓應用程式從 Xbox Controller 接收 Windows 的輸入。</span><span class="sxs-lookup"><span data-stu-id="37827-104">XInput is an API that allows applications to receive input from the Xbox Controller for Windows.</span></span> <span data-ttu-id="37827-105">本檔說明 Xbox 控制器的 XInput 和 [DirectInput](/previous-versions/windows/desktop/ee416842(v=vs.85)) 執行之間的差異，以及您可以同時支援 XInput 裝置和舊版 DirectInput 裝置的方式。</span><span class="sxs-lookup"><span data-stu-id="37827-105">This document describes the differences between XInput and [DirectInput](/previous-versions/windows/desktop/ee416842(v=vs.85)) implementations of the Xbox Controller and how you can support XInput devices and legacy DirectInput devices at the same time.</span></span>

> [!Note]  
> <span data-ttu-id="37827-106">不建議使用舊版[DirectInput](/previous-versions/windows/desktop/ee416842(v=vs.85)) ，DirectInput 無法用於 Windows Store 應用程式。</span><span class="sxs-lookup"><span data-stu-id="37827-106">Use of legacy [DirectInput](/previous-versions/windows/desktop/ee416842(v=vs.85)) is not recommended, and DirectInput is not available for Windows Store apps.</span></span>

## <a name="the-new-standard-xinput"></a><span data-ttu-id="37827-107">新標準： XInput</span><span class="sxs-lookup"><span data-stu-id="37827-107">The New Standard: XInput</span></span>

<span data-ttu-id="37827-108">XInput 現在可供遊戲開發之用。</span><span class="sxs-lookup"><span data-stu-id="37827-108">XInput is now available for game development.</span></span> <span data-ttu-id="37827-109">這是 Xbox 和 Windows 的新輸入標準。</span><span class="sxs-lookup"><span data-stu-id="37827-109">This is the new input standard for both the Xbox and Windows.</span></span> <span data-ttu-id="37827-110">api 可透過 DirectX SDK 取得，而驅動程式可透過 Windows Update 取得。</span><span class="sxs-lookup"><span data-stu-id="37827-110">The APIs are available through the DirectX SDK, and the driver is available through Windows Update.</span></span>

<span data-ttu-id="37827-111">在 [DirectInput](/previous-versions/windows/desktop/ee416842(v=vs.85))上使用 XInput 有幾個優點：</span><span class="sxs-lookup"><span data-stu-id="37827-111">There are several advantages to using XInput over [DirectInput](/previous-versions/windows/desktop/ee416842(v=vs.85)):</span></span>

-   <span data-ttu-id="37827-112">XInput 比[DirectInput](/previous-versions/windows/desktop/ee416842(v=vs.85))更容易使用，而且需要較少的安裝程式</span><span class="sxs-lookup"><span data-stu-id="37827-112">XInput is easier to use and requires less setup than [DirectInput](/previous-versions/windows/desktop/ee416842(v=vs.85))</span></span>
-   <span data-ttu-id="37827-113">Xbox 和 Windows 程式設計都將使用相同的核心 api 集合，讓程式設計能夠更輕鬆地轉譯跨平臺</span><span class="sxs-lookup"><span data-stu-id="37827-113">Both Xbox and Windows programming will use the same sets of core APIs, allowing programming to translate cross-platform much easier</span></span>
-   <span data-ttu-id="37827-114">Xbox 控制器將會有一個大型安裝的基底</span><span class="sxs-lookup"><span data-stu-id="37827-114">There will be a large installed base of Xbox controllers</span></span>
-   <span data-ttu-id="37827-115">XInput 裝置 (也就是說，Xbox 控制器) 只有在使用 XInput Api 時，才會有震動功能</span><span class="sxs-lookup"><span data-stu-id="37827-115">XInput devices (that is, the Xbox controllers) will have vibration functionality only when using XInput APIs</span></span>
-   <span data-ttu-id="37827-116">針對 Xbox 主控台推出的未來控制器 (也就是，方向盤) 也可以在 Windows</span><span class="sxs-lookup"><span data-stu-id="37827-116">Future controllers released for the Xbox console (that is, steering wheels) will also work on Windows</span></span>

### <a name="using-the-xbox-controller-with-directinput"></a><span data-ttu-id="37827-117">搭配使用 Xbox 控制器與 DirectInput</span><span class="sxs-lookup"><span data-stu-id="37827-117">Using the Xbox Controller with DirectInput</span></span>

<span data-ttu-id="37827-118">Xbox 控制器會在 [DirectInput](/previous-versions/windows/desktop/ee416842(v=vs.85))上正確列舉，並且可以搭配 DirectInputAPIs 使用。</span><span class="sxs-lookup"><span data-stu-id="37827-118">The Xbox Controller is properly enumerated on [DirectInput](/previous-versions/windows/desktop/ee416842(v=vs.85)), and can be used with the DirectInputAPIs.</span></span> <span data-ttu-id="37827-119">不過，XInput 所提供的某些功能將會從 DirectInput 的執行中遺失：</span><span class="sxs-lookup"><span data-stu-id="37827-119">However, some functionality provided by XInput will be missing from the DirectInput implementation:</span></span>

-   <span data-ttu-id="37827-120">左和右觸發程式按鈕將作為單一按鈕，而不是獨立的</span><span class="sxs-lookup"><span data-stu-id="37827-120">The left and right trigger buttons will act as a single button, not independently</span></span>
-   <span data-ttu-id="37827-121">振動效果將無法使用</span><span class="sxs-lookup"><span data-stu-id="37827-121">The vibration effects will not be available</span></span>
-   <span data-ttu-id="37827-122">查詢耳機裝置將無法使用</span><span class="sxs-lookup"><span data-stu-id="37827-122">Querying for headset devices will not be available</span></span>

<span data-ttu-id="37827-123">[DirectInput](/previous-versions/windows/desktop/ee416842(v=vs.85))中的左和右觸發程式組合是依設計而成。</span><span class="sxs-lookup"><span data-stu-id="37827-123">The combination of the left and right triggers in [DirectInput](/previous-versions/windows/desktop/ee416842(v=vs.85)) is by design.</span></span> <span data-ttu-id="37827-124">遊戲一律假設在沒有任何使用者與裝置互動時，會將 DirectInput 裝置軸置中。</span><span class="sxs-lookup"><span data-stu-id="37827-124">Games have always assumed that DirectInput device axes are centered when there is no user interaction with the device.</span></span> <span data-ttu-id="37827-125">不過，Xbox 控制器的設計是在未持有觸發程式時，註冊最小值，而不是置中。</span><span class="sxs-lookup"><span data-stu-id="37827-125">However, the Xbox controller was designed to register minimum value, not center, when the triggers are not being held.</span></span> <span data-ttu-id="37827-126">因此，較舊的遊戲會採用使用者互動。</span><span class="sxs-lookup"><span data-stu-id="37827-126">Older games would therefore assume user interaction.</span></span>

<span data-ttu-id="37827-127">解決方法是合併觸發程式、將觸發程式設定為正面方向，並將另一個觸發程式設為負面方向，因此沒有使用者互動表示 [DirectInput](/previous-versions/windows/desktop/ee416842(v=vs.85)) 「控制項」。</span><span class="sxs-lookup"><span data-stu-id="37827-127">The solution was to combine the triggers, setting one trigger to a positive direction and the other to a negative direction, so no user interaction is indicative to [DirectInput](/previous-versions/windows/desktop/ee416842(v=vs.85)) of the "control" being at center.</span></span>

<span data-ttu-id="37827-128">為了個別測試觸發程式值，您必須使用 XInput。</span><span class="sxs-lookup"><span data-stu-id="37827-128">In order to test the trigger values separately, you must use XInput.</span></span>

## <a name="xinput-and-directinput-side-by-side"></a><span data-ttu-id="37827-129">XInput 和 DirectInput 並存</span><span class="sxs-lookup"><span data-stu-id="37827-129">XInput and DirectInput Side by Side</span></span>

<span data-ttu-id="37827-130">藉由僅支援 XInput，您的遊戲將無法搭配舊版 [DirectInput](/previous-versions/windows/desktop/ee416842(v=vs.85)) 裝置使用。</span><span class="sxs-lookup"><span data-stu-id="37827-130">By supporting XInput only, your game will not work with legacy [DirectInput](/previous-versions/windows/desktop/ee416842(v=vs.85)) devices.</span></span> <span data-ttu-id="37827-131">XInput 將無法辨識這些裝置。</span><span class="sxs-lookup"><span data-stu-id="37827-131">XInput will not recognize these devices.</span></span>

<span data-ttu-id="37827-132">如果您想要讓遊戲支援舊版 [DirectInput](/previous-versions/windows/desktop/ee416842(v=vs.85)) 裝置，您可以使用 DirectInput 和 XInput 並存。</span><span class="sxs-lookup"><span data-stu-id="37827-132">If you want your game to support legacy [DirectInput](/previous-versions/windows/desktop/ee416842(v=vs.85)) devices, you may use DirectInput and XInput side by side.</span></span> <span data-ttu-id="37827-133">列舉 DirectInput 裝置時，會正確地列舉所有 DirectInput 裝置。</span><span class="sxs-lookup"><span data-stu-id="37827-133">When enumerating your DirectInput devices, all DirectInput devices will enumerate correctly.</span></span> <span data-ttu-id="37827-134">所有 XInput 裝置都將顯示為 XInput 和 DirectInput 裝置，但不應該透過 DirectInput 來處理。</span><span class="sxs-lookup"><span data-stu-id="37827-134">All XInput devices will show up as both XInput and DirectInput devices, but they should not be handled through DirectInput.</span></span> <span data-ttu-id="37827-135">您必須判斷哪些 DirectInput 裝置是舊版裝置，哪些是 XInput 裝置，並將它們從 DirectInput 裝置的列舉中移除。</span><span class="sxs-lookup"><span data-stu-id="37827-135">You will need to determine which of your DirectInput devices are legacy devices, and which are XInput devices, and remove them from the enumeration of DirectInput devices.</span></span>

<span data-ttu-id="37827-136">若要這樣做，請將下列程式碼插入您的 DirectInput 列舉回呼：</span><span class="sxs-lookup"><span data-stu-id="37827-136">To do this, insert this code into your DirectInput enumeration callback:</span></span>

```cpp
#include <wbemidl.h>
#include <oleauto.h>

#ifndef SAFE_RELEASE
#define SAFE_RELEASE(p) { if (p) { (p)->Release(); (p) = nullptr; } }
#endif

//-----------------------------------------------------------------------------
// Enum each PNP device using WMI and check each device ID to see if it contains 
// "IG_" (ex. "VID_045E&PID_028E&IG_00").  If it does, then it's an XInput device
// Unfortunately this information can not be found by just using DirectInput 
//-----------------------------------------------------------------------------
BOOL IsXInputDevice( const GUID* pGuidProductFromDirectInput )
{
    IWbemLocator*           pIWbemLocator = nullptr;
    IEnumWbemClassObject*   pEnumDevices = nullptr;
    IWbemClassObject*       pDevices[20] = {};
    IWbemServices*          pIWbemServices = nullptr;
    BSTR                    bstrNamespace = nullptr;
    BSTR                    bstrDeviceID = nullptr;
    BSTR                    bstrClassName = nullptr;
    bool                    bIsXinputDevice = false;
    
    // CoInit if needed
    HRESULT hr = CoInitialize(nullptr);
    bool bCleanupCOM = SUCCEEDED(hr);

    // So we can call VariantClear() later, even if we never had a successful IWbemClassObject::Get().
    VARIANT var = {};
    VariantInit(&var);

    // Create WMI
    hr = CoCreateInstance(__uuidof(WbemLocator),
        nullptr,
        CLSCTX_INPROC_SERVER,
        __uuidof(IWbemLocator),
        (LPVOID*)&pIWbemLocator);
    if (FAILED(hr) || pIWbemLocator == nullptr)
        goto LCleanup;

    bstrNamespace = SysAllocString(L"\\\\.\\root\\cimv2");  if (bstrNamespace == nullptr) goto LCleanup;
    bstrClassName = SysAllocString(L"Win32_PNPEntity");     if (bstrClassName == nullptr) goto LCleanup;
    bstrDeviceID = SysAllocString(L"DeviceID");             if (bstrDeviceID == nullptr)  goto LCleanup;
    
    // Connect to WMI 
    hr = pIWbemLocator->ConnectServer(bstrNamespace, nullptr, nullptr, 0L,
        0L, nullptr, nullptr, &pIWbemServices);
    if (FAILED(hr) || pIWbemServices == nullptr)
        goto LCleanup;

    // Switch security level to IMPERSONATE. 
    hr = CoSetProxyBlanket(pIWbemServices,
        RPC_C_AUTHN_WINNT, RPC_C_AUTHZ_NONE, nullptr,
        RPC_C_AUTHN_LEVEL_CALL, RPC_C_IMP_LEVEL_IMPERSONATE,
        nullptr, EOAC_NONE);
    if ( FAILED(hr) )
        goto LCleanup;

    hr = pIWbemServices->CreateInstanceEnum(bstrClassName, 0, nullptr, &pEnumDevices);
    if (FAILED(hr) || pEnumDevices == nullptr)
        goto LCleanup;

    // Loop over all devices
    for (;;)
    {
        ULONG uReturned = 0;
        hr = pEnumDevices->Next(10000, _countof(pDevices), pDevices, &uReturned);
        if (FAILED(hr))
            goto LCleanup;
        if (uReturned == 0)
            break;

        for (size_t iDevice = 0; iDevice < uReturned; ++iDevice)
        {
            // For each device, get its device ID
            hr = pDevices[iDevice]->Get(bstrDeviceID, 0L, &var, nullptr, nullptr);
            if (SUCCEEDED(hr) && var.vt == VT_BSTR && var.bstrVal != nullptr)
            {
                // Check if the device ID contains "IG_".  If it does, then it's an XInput device
                // This information can not be found from DirectInput 
                if (wcsstr(var.bstrVal, L"IG_"))
                {
                    // If it does, then get the VID/PID from var.bstrVal
                    DWORD dwPid = 0, dwVid = 0;
                    WCHAR* strVid = wcsstr(var.bstrVal, L"VID_");
                    if (strVid && swscanf_s(strVid, L"VID_%4X", &dwVid) != 1)
                        dwVid = 0;
                    WCHAR* strPid = wcsstr(var.bstrVal, L"PID_");
                    if (strPid && swscanf_s(strPid, L"PID_%4X", &dwPid) != 1)
                        dwPid = 0;

                    // Compare the VID/PID to the DInput device
                    DWORD dwVidPid = MAKELONG(dwVid, dwPid);
                    if (dwVidPid == pGuidProductFromDirectInput->Data1)
                    {
                        bIsXinputDevice = true;
                        goto LCleanup;
                    }
                }
            }
            VariantClear(&var);
            SAFE_RELEASE(pDevices[iDevice]);
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
        
    for (size_t iDevice = 0; iDevice < _countof(pDevices); ++iDevice)
        SAFE_RELEASE(pDevices[iDevice]);

    SAFE_RELEASE(pEnumDevices);
    SAFE_RELEASE(pIWbemLocator);
    SAFE_RELEASE(pIWbemServices);

    if(bCleanupCOM)
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
    if( IsXInputDevice( &pdidInstance->guidProduct ) )
        return DIENUM_CONTINUE;

     // Device is verified not XInput, so add it to the list of DInput devices

     return DIENUM_CONTINUE;    
}
```

> <span data-ttu-id="37827-137">這段程式碼有稍微改良的版本位於舊版 DirectInput [搖桿](https://github.com/walbourn/directx-sdk-samples/tree/master/DirectInput/Joystick) 範例中。</span><span class="sxs-lookup"><span data-stu-id="37827-137">A slightly improved version of this code is in the legacy DirectInput [Joystick](https://github.com/walbourn/directx-sdk-samples/tree/master/DirectInput/Joystick) sample.</span></span>

## <a name="related-topics"></a><span data-ttu-id="37827-138">相關主題</span><span class="sxs-lookup"><span data-stu-id="37827-138">Related topics</span></span>

[<span data-ttu-id="37827-139">使用 XInput 開始使用</span><span class="sxs-lookup"><span data-stu-id="37827-139">Getting Started With XInput</span></span>](getting-started-with-xinput.md)

[<span data-ttu-id="37827-140">程式設計參考</span><span class="sxs-lookup"><span data-stu-id="37827-140">Programming Reference</span></span>](programming-reference.md)
