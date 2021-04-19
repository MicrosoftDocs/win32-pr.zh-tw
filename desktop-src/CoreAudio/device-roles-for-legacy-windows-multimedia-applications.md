---
description: 舊版 Windows 多媒體應用程式的裝置角色
ms.assetid: 54dcaa0e-2652-406d-ba24-c8885924acc6
title: 舊版 Windows 多媒體應用程式的裝置角色
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 44a4ad6728659e4c865aed773575268844fe330e
ms.sourcegitcommit: c16214e53680dc71d1c07111b51f72b82a4512d8
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 03/03/2021
ms.locfileid: "106981936"
---
# <a name="device-roles-for-legacy-windows-multimedia-applications"></a><span data-ttu-id="69a6d-103">舊版 Windows 多媒體應用程式的裝置角色</span><span class="sxs-lookup"><span data-stu-id="69a6d-103">Device Roles for Legacy Windows Multimedia Applications</span></span>

> [!Note]  
> <span data-ttu-id="69a6d-104">MMDevice API 支援裝置角色。</span><span class="sxs-lookup"><span data-stu-id="69a6d-104">The MMDevice API supports device roles.</span></span> <span data-ttu-id="69a6d-105">不過，Windows Vista 中的使用者介面並不支援這項功能。</span><span class="sxs-lookup"><span data-stu-id="69a6d-105">However, the user interface in Windows Vista does not implement support for this feature.</span></span> <span data-ttu-id="69a6d-106">裝置角色的使用者介面支援可能會在未來的 Windows 版本中執行。</span><span class="sxs-lookup"><span data-stu-id="69a6d-106">User interface support for device roles might be implemented in a future version of Windows.</span></span> <span data-ttu-id="69a6d-107">如需詳細資訊，請參閱 [Windows Vista 中的裝置角色](device-roles-in-windows-vista.md)。</span><span class="sxs-lookup"><span data-stu-id="69a6d-107">For more information, see [Device Roles in Windows Vista](device-roles-in-windows-vista.md).</span></span>

 

<span data-ttu-id="69a6d-108">舊版 Windows 多媒體 **waveOutXxx** 和 **waveInXxx** 函式不提供任何方法，讓應用程式選取使用者指派給特定 [裝置角色](device-roles.md)的 [音訊端點裝置](audio-endpoint-devices.md)。</span><span class="sxs-lookup"><span data-stu-id="69a6d-108">The legacy Windows multimedia **waveOutXxx** and **waveInXxx** functions provide no means for an application to select the [audio endpoint device](audio-endpoint-devices.md) that the user has assigned to a particular [device role](device-roles.md).</span></span> <span data-ttu-id="69a6d-109">不過，在 Windows Vista 中，核心音訊 Api 可以與 Windows 多媒體應用程式搭配使用，以根據裝置角色啟用裝置選取。</span><span class="sxs-lookup"><span data-stu-id="69a6d-109">However, in Windows Vista, the core audio APIs can be used in conjunction with a Windows multimedia application to enable device selection based on device role.</span></span> <span data-ttu-id="69a6d-110">例如，在 [MMDEVICE API](mmdevice-api.md)的協助下， **waveOutXxx** 應用程式可以識別指派給角色的音訊端點裝置、識別對應的波形輸出裝置，以及呼叫 **waveOutOpen** 函式來開啟裝置的實例。</span><span class="sxs-lookup"><span data-stu-id="69a6d-110">For example, with the help of the [MMDevice API](mmdevice-api.md), a **waveOutXxx** application can identify the audio endpoint device that is assigned to a role, identify the corresponding waveform output device, and call the **waveOutOpen** function to open an instance of the device.</span></span> <span data-ttu-id="69a6d-111">如需 **waveOutXxx** 和 **waveInXxx** 的詳細資訊，請參閱 Windows SDK 檔。</span><span class="sxs-lookup"><span data-stu-id="69a6d-111">For more information about **waveOutXxx** and **waveInXxx**, see the Windows SDK documentation.</span></span>

<span data-ttu-id="69a6d-112">下列程式碼範例顯示如何取得指派給特定裝置角色之轉譯端點裝置的波形裝置識別碼：</span><span class="sxs-lookup"><span data-stu-id="69a6d-112">The following code example shows how to obtain the waveform device ID for the rendering endpoint device that is assigned to a particular device role:</span></span>


```C++
//-----------------------------------------------------------
// This function gets the waveOut ID of the audio endpoint
// device that is currently assigned to the specified device
// role. The caller can use the waveOut ID to open the
// waveOut device that corresponds to the endpoint device.
//-----------------------------------------------------------
#define EXIT_ON_ERROR(hres)  \
              if (FAILED(hres)) { goto Exit; }
#define SAFE_RELEASE(punk)  \
              if ((punk) != NULL)  \
                { (punk)->Release(); (punk) = NULL; }

HRESULT GetWaveOutId(ERole role, int *pWaveOutId)
{
    HRESULT hr;
    IMMDeviceEnumerator *pEnumerator = NULL;
    IMMDevice *pDevice = NULL;
    WCHAR *pstrEndpointIdKey = NULL;
    WCHAR *pstrEndpointId = NULL;

    if (pWaveOutId == NULL)
    {
        return E_POINTER;
    }

    // Create an audio endpoint device enumerator.
    hr = CoCreateInstance(__uuidof(MMDeviceEnumerator),
                          NULL, CLSCTX_INPROC_SERVER,
                          __uuidof(IMMDeviceEnumerator),
                          (void**)&pEnumerator);
    EXIT_ON_ERROR(hr)

    // Get the audio endpoint device that the user has
    // assigned to the specified device role.
    hr = pEnumerator->GetDefaultAudioEndpoint(eRender, role,
                                              &pDevice);
    EXIT_ON_ERROR(hr)

    // Get the endpoint ID string of the audio endpoint device.
    hr = pDevice->GetId(&pstrEndpointIdKey);
    EXIT_ON_ERROR(hr)

    // Get the size of the endpoint ID string.
    size_t  cbEndpointIdKey;

    hr = StringCbLength(pstrEndpointIdKey,
                        STRSAFE_MAX_CCH * sizeof(WCHAR),
                        &cbEndpointIdKey);
    EXIT_ON_ERROR(hr)

    // Include terminating null in string size.
    cbEndpointIdKey += sizeof(WCHAR);

    // Allocate a buffer for a second string of the same size.
    pstrEndpointId = (WCHAR*)CoTaskMemAlloc(cbEndpointIdKey);
    if (pstrEndpointId == NULL)
    {
        EXIT_ON_ERROR(hr = E_OUTOFMEMORY)
    }

    // Each for-loop iteration below compares the endpoint ID
    // string of the audio endpoint device to the endpoint ID
    // string of an enumerated waveOut device. If the strings
    // match, then we've found the waveOut device that is
    // assigned to the specified device role.
    int waveOutId;
    int cWaveOutDevices = waveOutGetNumDevs();

    for (waveOutId = 0; waveOutId < cWaveOutDevices; waveOutId++)
    {
        MMRESULT mmr;
        size_t cbEndpointId;

        // Get the size (including the terminating null) of
        // the endpoint ID string of the waveOut device.
        mmr = waveOutMessage((HWAVEOUT)IntToPtr(waveOutId),
                             DRV_QUERYFUNCTIONINSTANCEIDSIZE,
                             (DWORD_PTR)&cbEndpointId, NULL);
        if (mmr != MMSYSERR_NOERROR ||
            cbEndpointIdKey != cbEndpointId)  // do sizes match?
        {
            continue;  // not a matching device
        }

        // Get the endpoint ID string for this waveOut device.
        mmr = waveOutMessage((HWAVEOUT)IntToPtr(waveOutId),
                             DRV_QUERYFUNCTIONINSTANCEID,
                             (DWORD_PTR)pstrEndpointId,
                             cbEndpointId);
        if (mmr != MMSYSERR_NOERROR)
        {
            continue;
        }

        // Check whether the endpoint ID string of this waveOut
        // device matches that of the audio endpoint device.
        if (lstrcmpi(pstrEndpointId, pstrEndpointIdKey) == 0)
        {
            *pWaveOutId = waveOutId;  // found match
            hr = S_OK;
            break;
        }
    }

    if (waveOutId == cWaveOutDevices)
    {
        // We reached the end of the for-loop above without
        // finding a waveOut device with a matching endpoint
        // ID string. This behavior is quite unexpected.
        hr = E_UNEXPECTED;
    }

Exit:
    SAFE_RELEASE(pEnumerator);
    SAFE_RELEASE(pDevice);
    CoTaskMemFree(pstrEndpointIdKey);  // NULL pointer okay
    CoTaskMemFree(pstrEndpointId);
    return hr;
}
```



<span data-ttu-id="69a6d-113">在上述程式碼範例中，GetWaveOutId 函式會接受裝置角色 (eConsole、eMultimedia 或 eCommunications) 做為輸入參數。</span><span class="sxs-lookup"><span data-stu-id="69a6d-113">In the preceding code example, the GetWaveOutId function accepts a device role (eConsole, eMultimedia, or eCommunications) as an input parameter.</span></span> <span data-ttu-id="69a6d-114">第二個參數是一個指標，函式會透過此指標來寫入指派給指定角色之波形輸出裝置的波形裝置識別碼。</span><span class="sxs-lookup"><span data-stu-id="69a6d-114">The second parameter is a pointer through which the function writes the waveform device ID for the waveform output device that is assigned to the specified role.</span></span> <span data-ttu-id="69a6d-115">然後，應用程式可以使用此識別碼呼叫 **waveOutOpen** 來開啟裝置。</span><span class="sxs-lookup"><span data-stu-id="69a6d-115">The application can then call **waveOutOpen** with this ID to open the device.</span></span>

<span data-ttu-id="69a6d-116">上述程式碼範例中的主要迴圈包含 **waveOutMessage** 函數的兩個呼叫。</span><span class="sxs-lookup"><span data-stu-id="69a6d-116">The main loop in the preceding code example contains two calls to the **waveOutMessage** function.</span></span> <span data-ttu-id="69a6d-117">第一個呼叫會傳送 WINSPOOL.DRV \_ QUERYFUNCTIONINSTANCEIDSIZE 訊息，以位元組為單位，取得 *waveOutId* 參數所識別之波形裝置的 [端點識別碼字串](endpoint-id-strings.md)大小（以位元組為單位）。</span><span class="sxs-lookup"><span data-stu-id="69a6d-117">The first call sends a DRV\_QUERYFUNCTIONINSTANCEIDSIZE message to retrieve the size, in bytes, of the [endpoint ID string](endpoint-id-strings.md) of the waveform device that is identified by the *waveOutId* parameter.</span></span> <span data-ttu-id="69a6d-118"> (端點識別碼字串可識別以波形裝置抽象化為基礎的音訊端點裝置。 ) 此呼叫所報告的大小，包括字串結尾的結束 null 字元的空間。</span><span class="sxs-lookup"><span data-stu-id="69a6d-118">(The endpoint ID string identifies the audio endpoint device that underlies the waveform device abstraction.) The size reported by this call includes the space for the terminating null character at the end of the string.</span></span> <span data-ttu-id="69a6d-119">此程式可以使用大小資訊來配置夠大的緩衝區，以包含整個端點識別碼字串。</span><span class="sxs-lookup"><span data-stu-id="69a6d-119">The program can use the size information to allocate a buffer that is large enough to contain the entire endpoint ID string.</span></span>

<span data-ttu-id="69a6d-120">**WaveOutMessage** 的第二個呼叫會傳送 winspool.drv \_ QUERYFUNCTIONINSTANCEID 訊息，以抓取波形輸出裝置的裝置識別碼字串。</span><span class="sxs-lookup"><span data-stu-id="69a6d-120">The second call to **waveOutMessage** sends a DRV\_QUERYFUNCTIONINSTANCEID message to retrieve the device ID string of the waveform output device.</span></span> <span data-ttu-id="69a6d-121">範例程式碼會將此字串與具有指定裝置角色之音訊端點裝置的裝置識別碼字串進行比較。</span><span class="sxs-lookup"><span data-stu-id="69a6d-121">The example code compares this string to the device ID string of the audio endpoint device with the specified device role.</span></span> <span data-ttu-id="69a6d-122">如果字串相符，則函式會將波形裝置識別碼寫入至參數 *pWaveOutId* 所指向的位置。</span><span class="sxs-lookup"><span data-stu-id="69a6d-122">If the strings match, then the function writes the waveform device ID to the location pointed to by parameter *pWaveOutId*.</span></span> <span data-ttu-id="69a6d-123">呼叫端可以使用此識別碼來開啟具有指定裝置角色的波形輸出裝置。</span><span class="sxs-lookup"><span data-stu-id="69a6d-123">The caller can use this ID to open the waveform output device that has the specified device role.</span></span>

<span data-ttu-id="69a6d-124">Windows Vista 支援 WINSPOOL.DRV \_ QUERYFUNCTIONINSTANCEIDSIZE 和 Winspool.drv \_ QUERYFUNCTIONINSTANCEID 訊息。</span><span class="sxs-lookup"><span data-stu-id="69a6d-124">Windows Vista supports the DRV\_QUERYFUNCTIONINSTANCEIDSIZE and DRV\_QUERYFUNCTIONINSTANCEID messages.</span></span> <span data-ttu-id="69a6d-125">舊版 Windows 不支援這些功能，包括 Windows Server 2003、Windows XP 及 Windows 2000。</span><span class="sxs-lookup"><span data-stu-id="69a6d-125">They are not supported in earlier versions of Windows, including Windows Server 2003, Windows XP, and Windows 2000.</span></span>

<span data-ttu-id="69a6d-126">上述程式碼範例中的函式會取得轉譯裝置的波形裝置識別碼，但是只要進行一些修改，您就可以調整它以取得捕獲裝置的波形裝置識別碼。</span><span class="sxs-lookup"><span data-stu-id="69a6d-126">The function in the preceding code example obtains the waveform device ID for a rendering device, but, with a few modifications, it can be adapted to obtain the waveform device ID for a capture device.</span></span> <span data-ttu-id="69a6d-127">然後，應用程式可以使用此識別碼呼叫 **waveInOpen** 來開啟裝置。</span><span class="sxs-lookup"><span data-stu-id="69a6d-127">The application can then call **waveInOpen** with this ID to open the device.</span></span> <span data-ttu-id="69a6d-128">若要變更上述的程式碼範例，以取得指派給特定角色之音訊捕獲端點裝置的波形裝置識別碼，請執行下列動作：</span><span class="sxs-lookup"><span data-stu-id="69a6d-128">To change the preceding code example to get the waveform device ID for the audio-capture endpoint device that is assigned to a particular role, do the following:</span></span>

-   <span data-ttu-id="69a6d-129">以對應的 **waveInXxx** 函式呼叫取代上述範例中的所有 **waveOutXxx** 函式呼叫。</span><span class="sxs-lookup"><span data-stu-id="69a6d-129">Replace all of the **waveOutXxx** function calls in the preceding example with the corresponding **waveInXxx** function calls.</span></span>
-   <span data-ttu-id="69a6d-130">將控制碼類型 HWAVEOUT 變更為 HWAVEIN。</span><span class="sxs-lookup"><span data-stu-id="69a6d-130">Change handle type HWAVEOUT to HWAVEIN.</span></span>
-   <span data-ttu-id="69a6d-131">將 [**ERole**](/windows/win32/api/mmdeviceapi/ne-mmdeviceapi-erole) 列舉常數 eRender 取代為 eCapture。</span><span class="sxs-lookup"><span data-stu-id="69a6d-131">Replace [**ERole**](/windows/win32/api/mmdeviceapi/ne-mmdeviceapi-erole) enumeration constant eRender with eCapture.</span></span>

<span data-ttu-id="69a6d-132">在 Windows Vista 中， **waveOutOpen** 和 **waveInOpen** 函式一律會將其建立的音訊串流指派給預設會話，也就是由會話 guid 值 guid Null 所識別的進程特定會話 \_ 。</span><span class="sxs-lookup"><span data-stu-id="69a6d-132">In Windows Vista, the **waveOutOpen** and **waveInOpen** functions always assign the audio streams that they create to the default session—the process-specific session that is identified by the session GUID value GUID\_NULL.</span></span>

## <a name="related-topics"></a><span data-ttu-id="69a6d-133">相關主題</span><span class="sxs-lookup"><span data-stu-id="69a6d-133">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="69a6d-134">與舊版音訊 Api 的互通性</span><span class="sxs-lookup"><span data-stu-id="69a6d-134">Interoperability with Legacy Audio APIs</span></span>](interoperability-with-legacy-audio-apis.md)
</dt> </dl>

 

 



