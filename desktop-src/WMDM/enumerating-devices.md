---
title: 列舉 Windows Media 裝置管理員裝置
description: 列舉裝置
ms.assetid: c5935681-b530-4446-a026-7ddc74084d23
keywords:
- Windows Media 裝置管理員，列舉裝置
- 裝置管理員，列舉裝置
- 程式設計指南，列舉裝置
- 桌面應用程式，列舉裝置
- 建立 Windows Media 裝置管理員應用程式，列舉裝置
- 列舉裝置
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: c3584e625f54ea4e5c601f2a32865515c824cfcd
ms.sourcegitcommit: cba7f424a292fd7f3a8518947b9466439b455419
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 11/23/2019
ms.locfileid: "104092471"
---
# <a name="enumerating-windows-media-device-manager-devices"></a><span data-ttu-id="1c78c-109">列舉 Windows Media 裝置管理員裝置</span><span class="sxs-lookup"><span data-stu-id="1c78c-109">Enumerating Windows Media Device Manager devices</span></span>

<span data-ttu-id="1c78c-110">驗證應用程式之後，您可以開始列舉 Windows Media 裝置管理員所偵測到的裝置。</span><span class="sxs-lookup"><span data-stu-id="1c78c-110">After authenticating an application, you can begin to enumerate the devices detected by Windows Media Device Manager.</span></span> <span data-ttu-id="1c78c-111">列舉是藉由使用 [**IWMDeviceManager2：： EnumDevices2**](/windows/desktop/api/mswmdm/nf-mswmdm-iwmdevicemanager2-enumdevices2)或 [**IWMDeviceManager：： EnumDevices**](/windows/desktop/api/mswmdm/nf-mswmdm-iwmdevicemanager-enumdevices)所取得的列舉介面 [**IWMDMEnumDevice**](/windows/desktop/api/mswmdm/nn-mswmdm-iwmdmenumdevice)來完成。</span><span class="sxs-lookup"><span data-stu-id="1c78c-111">Enumeration is done by using an enumeration interface, [**IWMDMEnumDevice**](/windows/desktop/api/mswmdm/nn-mswmdm-iwmdmenumdevice), obtained by using either [**IWMDeviceManager2::EnumDevices2**](/windows/desktop/api/mswmdm/nf-mswmdm-iwmdevicemanager2-enumdevices2) or [**IWMDeviceManager::EnumDevices**](/windows/desktop/api/mswmdm/nf-mswmdm-iwmdevicemanager-enumdevices).</span></span> <span data-ttu-id="1c78c-112">如果支援，則使用 **EnumDevices2** 方法，因為較早的版本只會傳回裝置上的舊版介面，而新的版本則會傳回舊版和新的介面。</span><span class="sxs-lookup"><span data-stu-id="1c78c-112">If supported, use the **EnumDevices2** method, because the earlier version only returned legacy interfaces on devices, whereas the new version returns both the legacy and the new interfaces.</span></span>

<span data-ttu-id="1c78c-113">取得列舉值之前，您應該決定要使用的列舉視圖。</span><span class="sxs-lookup"><span data-stu-id="1c78c-113">Before obtaining an enumerator, you should decide what enumeration view to use.</span></span> <span data-ttu-id="1c78c-114">有些裝置會將每個存放裝置公開為不同的裝置。</span><span class="sxs-lookup"><span data-stu-id="1c78c-114">Some devices expose each storage as a different device.</span></span> <span data-ttu-id="1c78c-115">例如，裝置上的兩個快閃記憶卡會列舉為不同的裝置。</span><span class="sxs-lookup"><span data-stu-id="1c78c-115">For example, two flash memory cards on a device will enumerate as if they were separate devices.</span></span> <span data-ttu-id="1c78c-116">您可以指定將裝置上的所有存放裝置都列舉成單一裝置。</span><span class="sxs-lookup"><span data-stu-id="1c78c-116">You can specify that all storages on a device are enumerated together as a single device.</span></span> <span data-ttu-id="1c78c-117">您只能在應用程式中設定此喜好設定一次。如果您想要變更它，則必須關閉並重新啟動應用程式。</span><span class="sxs-lookup"><span data-stu-id="1c78c-117">You can set this preference only once in your application; if you want to change it, you must shut down the application and restart it.</span></span> <span data-ttu-id="1c78c-118">不過，請注意，舊版裝置有時候會忽略將個別裝置存放裝置列舉為單一裝置的要求，並繼續個別列舉它們。</span><span class="sxs-lookup"><span data-stu-id="1c78c-118">However, note that legacy devices will sometimes ignore a request to enumerate separate device storages as a single device, and continue to enumerate them separately.</span></span>

<span data-ttu-id="1c78c-119">下列步驟顯示如何列舉連線的裝置：</span><span class="sxs-lookup"><span data-stu-id="1c78c-119">The following steps show how to enumerate connected devices:</span></span>

1.  <span data-ttu-id="1c78c-120">使用 [**IWMDeviceManager3：： SetDeviceEnumPreference**](/windows/desktop/api/mswmdm/nf-mswmdm-iwmdevicemanager3-setdeviceenumpreference)設定裝置列舉喜好設定。</span><span class="sxs-lookup"><span data-stu-id="1c78c-120">Set the device enumeration preference using [**IWMDeviceManager3::SetDeviceEnumPreference**](/windows/desktop/api/mswmdm/nf-mswmdm-iwmdevicemanager3-setdeviceenumpreference).</span></span> <span data-ttu-id="1c78c-121">如果未呼叫這個方法，則預設方法會將儲存體顯示為個別的裝置。</span><span class="sxs-lookup"><span data-stu-id="1c78c-121">If this method is not called, the default method is to show storages as separate devices.</span></span> <span data-ttu-id="1c78c-122">若要判斷個別的「裝置」是否實際上是在相同的裝置上進行存放裝置，請呼叫 [**IWMDMDevice2：： GetCanonicalName**](/windows/desktop/api/mswmdm/nf-mswmdm-iwmdmdevice2-getcanonicalname);來自相同裝置的儲存體將會傳回相同的值，但最後一個 "$" 符號之後的最後一個數位除外。</span><span class="sxs-lookup"><span data-stu-id="1c78c-122">To determine whether individual "devices" are actually storages on the same device, call [**IWMDMDevice2::GetCanonicalName**](/windows/desktop/api/mswmdm/nf-mswmdm-iwmdmdevice2-getcanonicalname); storages from the same device will return identical values, except for the final digit after the last "$" sign.</span></span>
2.  <span data-ttu-id="1c78c-123">查詢 [**IWMDeviceManager**](/windows/desktop/api/mswmdm/nn-mswmdm-iwmdevicemanager) 或 [**IWMDeviceManager2**](/windows/desktop/api/mswmdm/nn-mswmdm-iwmdevicemanager2)，然後呼叫 [**IWMDeviceManager2：： EnumDevices2**](/windows/desktop/api/mswmdm/nf-mswmdm-iwmdevicemanager2-enumdevices2) 來取得裝置列舉值介面 [**IWMDMEnumDevice**](/windows/desktop/api/mswmdm/nn-mswmdm-iwmdmenumdevice)。</span><span class="sxs-lookup"><span data-stu-id="1c78c-123">Query for [**IWMDeviceManager**](/windows/desktop/api/mswmdm/nn-mswmdm-iwmdevicemanager) or [**IWMDeviceManager2**](/windows/desktop/api/mswmdm/nn-mswmdm-iwmdevicemanager2), and then call [**IWMDeviceManager2::EnumDevices2**](/windows/desktop/api/mswmdm/nf-mswmdm-iwmdevicemanager2-enumdevices2) to obtain the device enumerator interface, [**IWMDMEnumDevice**](/windows/desktop/api/mswmdm/nn-mswmdm-iwmdmenumdevice).</span></span> <span data-ttu-id="1c78c-124"> (如果支援的話，請使用 **EnumDevices2**，這樣會更有效率，因為較舊的版本可能不會傳回 MTP 裝置) 。</span><span class="sxs-lookup"><span data-stu-id="1c78c-124">(If supported, use **EnumDevices2**, which is more efficient, as the earlier version may not return MTP devices).</span></span>
3.  <span data-ttu-id="1c78c-125">呼叫 [**IWMDMEnumDevices：： Next**](/windows/desktop/api/mswmdm/nf-mswmdm-iwmdmenumdevice-next) 方法，一次取出一或多個裝置。</span><span class="sxs-lookup"><span data-stu-id="1c78c-125">Call the [**IWMDMEnumDevices::Next**](/windows/desktop/api/mswmdm/nf-mswmdm-iwmdmenumdevice-next) method to retrieve one or more devices at a time.</span></span> <span data-ttu-id="1c78c-126">繼續呼叫這個方法，直到該方法傳回 \_ FALSE 或錯誤訊息為止。</span><span class="sxs-lookup"><span data-stu-id="1c78c-126">Continue to call this method until the method returns S\_FALSE or an error message.</span></span> <span data-ttu-id="1c78c-127">如果一次只抓取一個裝置，您不需要配置陣列來保存裝置。</span><span class="sxs-lookup"><span data-stu-id="1c78c-127">If retrieving only one device at a time, you do not need to allocate an array to hold the devices.</span></span>

<span data-ttu-id="1c78c-128">由於使用者可以在您的應用程式執行時，從電腦附加或移除裝置，因此最好是執行裝置連線或移除的通知。</span><span class="sxs-lookup"><span data-stu-id="1c78c-128">Because users can attach or remove devices from the computer while your application is running, it is a good idea to implement notification of device connection or removal.</span></span> <span data-ttu-id="1c78c-129">這是藉由執行 [**IWMDMNotification**](/windows/desktop/api/mswmdm/nn-mswmdm-iwmdmnotification) 介面並註冊它來完成。</span><span class="sxs-lookup"><span data-stu-id="1c78c-129">This is done by implementing the [**IWMDMNotification**](/windows/desktop/api/mswmdm/nn-mswmdm-iwmdmnotification) interface and registering it.</span></span> <span data-ttu-id="1c78c-130">如需有關這個的詳細資訊，請參閱 [啟用通知](enabling-notifications.md)。</span><span class="sxs-lookup"><span data-stu-id="1c78c-130">For more information on this, see [Enabling Notifications](enabling-notifications.md).</span></span>

<span data-ttu-id="1c78c-131">下列 c + + 程式碼會列舉裝置，並要求每個裝置的相關資訊。</span><span class="sxs-lookup"><span data-stu-id="1c78c-131">The following C++ code enumerates devices and requests information about each device.</span></span>


```C++
HRESULT CWMDMController::EnumDevices()
{
    HRESULT hr = S_OK;

    // Change behavior to show devices as one object, not each storage as a device.
    // This can be called only once for each instance of this application.
    CComQIPtr<IWMDeviceManager3>pDevMgr3(m_IWMDMDeviceMgr);
    hr = pDevMgr3->SetDeviceEnumPreference(DO_NOT_VIRTUALIZE_STORAGES_AS_DEVICES);
    
    // Get number of attached devices.
    DWORD iDevices = 0;
    hr = m_IWMDMDeviceMgr->GetDeviceCount(&iDevices);
    if (hr == S_OK)
    {
        // TODO: Display count of devices.
    }

    //
    // Get a device enumerator to enumerate devices.
    //
    CComPtr<IWMDeviceManager2> pDevMgr2;
    hr = m_IWMDMDeviceMgr->QueryInterface (__uuidof(IWMDeviceManager2), (void**) &pDevMgr2);
    if (hr == S_OK)
    {
        // TODO: Display message indicating that application obtained IWMDeviceManager2.
    }
    else
    {
        // TODO: Display message indicating that we couldn't 
        // get IWMDeviceManager2 in EnumDevices.
        return hr;
    }
   CComPtr<IWMDMEnumDevice> pEnumDevice;
   hr = pDevMgr2->EnumDevices2(&pEnumDevice);
    if (hr != S_OK)
    {
        // TODO: Display messaging indicating that an error occurred 
        // in calling EnumDevices2.
        return hr;
    }

    // Length of all the strings we'll send in. 
    const UINT MAX_CHARS = 100;

    // Iterate through devices.
    while(TRUE)
    {
        // Get a device handle.
        IWMDMDevice *pIWMDMDevice;
        ULONG ulFetched = 0;
        hr = pEnumDevice->Next(1, &pIWMDMDevice, &ulFetched);
        if ((hr != S_OK) || (ulFetched != 1))
        {
            break;
        }
        
        // Get a display icon for the device.
        ULONG deviceIcon = 0;
        hr = pIWMDMDevice->GetDeviceIcon(&deviceIcon);

        // Print the device manufacturer.
        WCHAR manufacturer[MAX_CHARS];
        hr = pIWMDMDevice->GetManufacturer((LPWSTR)&manufacturer, MAX_CHARS);
        if (hr == S_OK)
        {
            // TODO: Display manufacturer name.
        }

        // Get the device name.
        WCHAR name[MAX_CHARS];
        hr = pIWMDMDevice->GetName((LPWSTR)&name, MAX_CHARS);
        if (hr == S_OK)
        {
            // TODO: Display name.
        }

        // TODO: Get other device information if wanted.

        // Obtain an IWMDMDevice2 interface and call some methods.
        CComQIPtr<IWMDMDevice2> pIWMDMDevice2(pIWMDMDevice);
        if (pIWMDMDevice2 != NULL)
        {
            // Get the canonical name.
            WCHAR canonicalName[MAX_CHARS];
            hr = pIWMDMDevice2->GetCanonicalName(canonicalName, MAX_CHARS);
            if (hr == S_OK)
            {
                // TODO: Display canonical name.
            }
        }

        // Obtain an IWMDMDevice3 interface and call some methods.
        CComQIPtr<IWMDMDevice3>pIWMDMDevice3(pIWMDMDevice);
        if (pIWMDMDevice3 != NULL)
        {
            // Find out what protocol is being used.
            PROPVARIANT val;
            PropVariantInit(&val);
            hr = pIWMDMDevice3->GetProperty(g_wszWMDMDeviceProtocol, &val);

            if (hr == S_OK)
            {
                if (*val.puuid == WMDM_DEVICE_PROTOCOL_RAPI)
                {
                    // TODO: Display message indicating device is a RAPI device.
                }
                else if (*val.puuid == WMDM_DEVICE_PROTOCOL_MTP)
                {
                    / /TODO: Display message indicating device is an MTP device.
                }
                else if (*val.puuid == WMDM_DEVICE_PROTOCOL_MSC)
                {
                    // TODO: Display message indicating device is an MSC device.
                }
                else
                {
                    // TODO: Display message indicating that the 
                    // application encountered an unknown protocol.
                }
                PropVariantClear(&val);
            }
        }

        // Examine the device capabilities. You could use some of these
        // to enable or disable the application's UI elements.
        CComQIPtr<IWMDMDeviceControl> pDeviceControl(pIWMDMDevice);
        if (pDeviceControl != NULL)
        {
            DWORD caps = 0;
            hr = pDeviceControl->GetCapabilities(&caps);
            if (caps & WMDM_DEVICECAP_CANPLAY)
            {
                // TODO: Display message indicating that the media 
                // device can play MP3 audio.
            }
            // TODO: Test for other capabilities here.
        }
    } // Get the next device.
    return hr;
}
```



## <a name="related-topics"></a><span data-ttu-id="1c78c-132">相關主題</span><span class="sxs-lookup"><span data-stu-id="1c78c-132">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="1c78c-133">**建立 Windows Media 裝置管理員應用程式**</span><span class="sxs-lookup"><span data-stu-id="1c78c-133">**Creating a Windows Media Device Manager Application**</span></span>](creating-a-windows-media-device-manager-application.md)
</dt> </dl>

 

 




