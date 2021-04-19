---
description: 裝置內容
ms.assetid: ad8753ba-ad20-4122-b0f2-eb165f98db67
title: '裝置屬性 (核心音訊 Api) '
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 14a868e4bb806bd49d934febed164bcd70fba39f
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/07/2021
ms.locfileid: "106970306"
---
# <a name="device-properties-core-audio-apis"></a><span data-ttu-id="349f4-103">裝置屬性 (核心音訊 Api) </span><span class="sxs-lookup"><span data-stu-id="349f4-103">Device Properties (Core Audio APIs)</span></span>

<span data-ttu-id="349f4-104">在列舉 [音訊端點裝置](audio-endpoint-devices.md)的過程中，用戶端應用程式可以詢問端點物件的裝置屬性。</span><span class="sxs-lookup"><span data-stu-id="349f4-104">During the process of enumerating [audio endpoint devices](audio-endpoint-devices.md), a client application can interrogate the endpoint objects for their device properties.</span></span> <span data-ttu-id="349f4-105">裝置屬性會在 MMDevice API 的 **IPropertyStore** 介面執行中公開。</span><span class="sxs-lookup"><span data-stu-id="349f4-105">The device properties are exposed in MMDevice API's implementation of the **IPropertyStore** interface.</span></span> <span data-ttu-id="349f4-106">針對端點物件的 [**IMMDevice**](/windows/desktop/api/Mmdeviceapi/nn-mmdeviceapi-immdevice) 介面參考，用戶端可以藉由呼叫 [**IMMDevice：： OpenPropertyStore**](/windows/desktop/api/Mmdeviceapi/nf-mmdeviceapi-immdevice-openpropertystore) 方法，取得端點物件的屬性存放區的參考。</span><span class="sxs-lookup"><span data-stu-id="349f4-106">Given a reference to the [**IMMDevice**](/windows/desktop/api/Mmdeviceapi/nn-mmdeviceapi-immdevice) interface of an endpoint object, a client can obtain a reference to the endpoint object's property store by calling the [**IMMDevice::OpenPropertyStore**](/windows/desktop/api/Mmdeviceapi/nf-mmdeviceapi-immdevice-openpropertystore) method.</span></span>

<span data-ttu-id="349f4-107">屬性存放區物件會公開 **IPropertyStore** 介面。</span><span class="sxs-lookup"><span data-stu-id="349f4-107">The property-store object exposes an **IPropertyStore** interface.</span></span> <span data-ttu-id="349f4-108">這個介面中的兩個主要方法是 **IPropertyStore：： GetValue**（可取得裝置屬性值）和 **IPropertyStore：： SetValue**（可設定裝置屬性值）。</span><span class="sxs-lookup"><span data-stu-id="349f4-108">The two primary methods in this interface are **IPropertyStore::GetValue**, which gets a device property value, and **IPropertyStore::SetValue**, which sets a device property value.</span></span> <span data-ttu-id="349f4-109">如需 **IPropertyStore** 的詳細資訊，請參閱 Windows SDK 檔。</span><span class="sxs-lookup"><span data-stu-id="349f4-109">For more information about **IPropertyStore**, see the Windows SDK documentation.</span></span>

<span data-ttu-id="349f4-110">MMDevice API 的屬性存放區實作為不同于標準 shell 屬性存放區物件。</span><span class="sxs-lookup"><span data-stu-id="349f4-110">The MMDevice API's implementation of the property store is different from the standard shell property store object.</span></span> <span data-ttu-id="349f4-111">若要變更屬性值，用戶端應用程式必須呼叫 **IPropertyStore：： SetValue** 方法。</span><span class="sxs-lookup"><span data-stu-id="349f4-111">To change a property value, the client application must call the **IPropertyStore::SetValue** method.</span></span> <span data-ttu-id="349f4-112">在此呼叫過程中，新的值會設定並寫入登錄中。</span><span class="sxs-lookup"><span data-stu-id="349f4-112">During this call, the new values are set and written in the registry.</span></span> <span data-ttu-id="349f4-113">因此，應用程式不需要在 **SetValue** 呼叫之後呼叫 **IPropertyStore：： Commit** 方法。</span><span class="sxs-lookup"><span data-stu-id="349f4-113">Therefore, the application does not need to call the **IPropertyStore::Commit** method after the **SetValue** call.</span></span> <span data-ttu-id="349f4-114">只有當用戶端釋放介面指標時，才會關閉登錄的控制碼。</span><span class="sxs-lookup"><span data-stu-id="349f4-114">The handle to the registry is closed only when the client releases the interface pointer.</span></span>

<span data-ttu-id="349f4-115">一般來說，協力廠商用戶端應用程式會呼叫 **GetValue** 方法，但不會呼叫 **SetValue** 方法。</span><span class="sxs-lookup"><span data-stu-id="349f4-115">Typically, third-party client applications call the **GetValue** method but not the **SetValue** method.</span></span> <span data-ttu-id="349f4-116">端點管理員會設定端點的基本裝置屬性。</span><span class="sxs-lookup"><span data-stu-id="349f4-116">The endpoint manager sets the basic device properties for endpoints.</span></span> <span data-ttu-id="349f4-117">端點管理員是 Windows Vista 元件，負責偵測音訊端點裝置是否存在。</span><span class="sxs-lookup"><span data-stu-id="349f4-117">The endpoint manager is the Windows Vista component that is responsible for detecting the presence of audio endpoint devices.</span></span>

<span data-ttu-id="349f4-118">下列清單中的每個 PKEY \_ Xxx 屬性識別碼都是 **PROPERTYKEY** 的常數，定義于標頭檔 Functiondiscoverykeys \_ devpkey 中。</span><span class="sxs-lookup"><span data-stu-id="349f4-118">Each PKEY\_Xxx property identifier in the following list is a constant of type **PROPERTYKEY** that is defined in header file Functiondiscoverykeys\_devpkey.h.</span></span> <span data-ttu-id="349f4-119">所有音訊端點裝置都有這三個裝置屬性。</span><span class="sxs-lookup"><span data-stu-id="349f4-119">All audio endpoint devices have these three device properties.</span></span>



| <span data-ttu-id="349f4-120">屬性</span><span class="sxs-lookup"><span data-stu-id="349f4-120">Property</span></span>                                                                         | <span data-ttu-id="349f4-121">描述</span><span class="sxs-lookup"><span data-stu-id="349f4-121">Description</span></span>                                                                                                                                                                                                                                                                       |
|----------------------------------------------------------------------------------|-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [<span data-ttu-id="349f4-122">**PKEY \_ DeviceInterface \_ FriendlyName**</span><span class="sxs-lookup"><span data-stu-id="349f4-122">**PKEY\_DeviceInterface\_FriendlyName**</span></span>](pkey-deviceinterface-friendlyname.md) | <span data-ttu-id="349f4-123">端點裝置所連接之音訊介面卡的易記名稱 (例如「XYZ 音訊介面卡」 ) 。</span><span class="sxs-lookup"><span data-stu-id="349f4-123">The friendly name of the audio adapter to which the endpoint device is attached (for example, "XYZ Audio Adapter").</span></span> <span data-ttu-id="349f4-124">**PROPVARIANT** 成員 **VT** 設定為 vt \_ LPWSTR，而成員 **pwszVal** 指向以 null 結尾的寬字元字串，其中包含易記名稱。</span><span class="sxs-lookup"><span data-stu-id="349f4-124">**PROPVARIANT** member **vt** is set to VT\_LPWSTR and member **pwszVal** points to a null-terminated, wide-character string that contains the friendly name.</span></span> |
| [<span data-ttu-id="349f4-125">**PKEY \_ 裝置 \_ DeviceDesc**</span><span class="sxs-lookup"><span data-stu-id="349f4-125">**PKEY\_Device\_DeviceDesc**</span></span>](pkey-device-devicedesc.md)                       | <span data-ttu-id="349f4-126">端點裝置的裝置描述 (例如「喇叭」 ) 。</span><span class="sxs-lookup"><span data-stu-id="349f4-126">The device description of the endpoint device (for example, "Speakers").</span></span> <span data-ttu-id="349f4-127">**PROPVARIANT** 成員 **VT** 設定為 vt \_ LPWSTR，而成員 **pwszVal** 指向以 null 終止的寬字元字串，其中包含裝置描述。</span><span class="sxs-lookup"><span data-stu-id="349f4-127">**PROPVARIANT** member **vt** is set to VT\_LPWSTR and member **pwszVal** points to a null-terminated, wide-character string that contains the device description.</span></span>                                       |
| [<span data-ttu-id="349f4-128">**PKEY \_ 裝置 \_ FriendlyName**</span><span class="sxs-lookup"><span data-stu-id="349f4-128">**PKEY\_Device\_FriendlyName**</span></span>](pkey-device-friendlyname.md)                   | <span data-ttu-id="349f4-129">端點裝置的易記名稱 (例如「喇叭 (XYZ 音訊介面卡) 」 ) 。</span><span class="sxs-lookup"><span data-stu-id="349f4-129">The friendly name of the endpoint device (for example, "Speakers (XYZ Audio Adapter)").</span></span> <span data-ttu-id="349f4-130">**PROPVARIANT** 成員 **VT** 設定為 vt \_ LPWSTR，而成員 **pwszVal** 指向以 null 結尾的寬字元字串，其中包含易記名稱。</span><span class="sxs-lookup"><span data-stu-id="349f4-130">**PROPVARIANT** member **vt** is set to VT\_LPWSTR and member **pwszVal** points to a null-terminated, wide-character string that contains the friendly name.</span></span>                             |



 

<span data-ttu-id="349f4-131">某些音訊端點裝置可能會有未出現在上述清單中的其他屬性。</span><span class="sxs-lookup"><span data-stu-id="349f4-131">Some audio endpoint devices might have additional properties that do not appear in the preceding list.</span></span> <span data-ttu-id="349f4-132">如需其他屬性的詳細資訊，請參閱 [音訊端點屬性](audio-endpoint-properties.md)。</span><span class="sxs-lookup"><span data-stu-id="349f4-132">For more information about additional properties, see [Audio Endpoint Properties](audio-endpoint-properties.md).</span></span> <span data-ttu-id="349f4-133">如需 **PROPERTYKEY** 的詳細資訊，請參閱 Windows SDK 檔。</span><span class="sxs-lookup"><span data-stu-id="349f4-133">For more information about **PROPERTYKEY**, see the Windows SDK documentation.</span></span>

<span data-ttu-id="349f4-134">下列程式碼範例會列印系統中所有音訊呈現端點裝置的顯示名稱：</span><span class="sxs-lookup"><span data-stu-id="349f4-134">The following code example prints the display names of all audio-rendering endpoint devices in the system:</span></span>


```C++
//-----------------------------------------------------------
// This function enumerates all active (plugged in) audio
// rendering endpoint devices. It prints the friendly name
// and endpoint ID string of each endpoint device.
//-----------------------------------------------------------
#define EXIT_ON_ERROR(hres)  \
              if (FAILED(hres)) { goto Exit; }
#define SAFE_RELEASE(punk)  \
              if ((punk) != NULL)  \
                { (punk)->Release(); (punk) = NULL; }

const CLSID CLSID_MMDeviceEnumerator = __uuidof(MMDeviceEnumerator);
const IID IID_IMMDeviceEnumerator = __uuidof(IMMDeviceEnumerator);

void PrintEndpointNames()
{
    HRESULT hr = S_OK;
    IMMDeviceEnumerator *pEnumerator = NULL;
    IMMDeviceCollection *pCollection = NULL;
    IMMDevice *pEndpoint = NULL;
    IPropertyStore *pProps = NULL;
    LPWSTR pwszID = NULL;

    hr = CoCreateInstance(
           CLSID_MMDeviceEnumerator, NULL,
           CLSCTX_ALL, IID_IMMDeviceEnumerator,
           (void**)&pEnumerator);
    EXIT_ON_ERROR(hr)

    hr = pEnumerator->EnumAudioEndpoints(
                        eRender, DEVICE_STATE_ACTIVE,
                        &pCollection);
    EXIT_ON_ERROR(hr)

    UINT  count;
    hr = pCollection->GetCount(&count);
    EXIT_ON_ERROR(hr)

    if (count == 0)
    {
        printf("No endpoints found.\n");
    }

    // Each loop prints the name of an endpoint device.
    for (ULONG i = 0; i < count; i++)
    {
        // Get pointer to endpoint number i.
        hr = pCollection->Item(i, &pEndpoint);
        EXIT_ON_ERROR(hr)

        // Get the endpoint ID string.
        hr = pEndpoint->GetId(&pwszID);
        EXIT_ON_ERROR(hr)
        
        hr = pEndpoint->OpenPropertyStore(
                          STGM_READ, &pProps);
        EXIT_ON_ERROR(hr)

        PROPVARIANT varName;
        // Initialize container for property value.
        PropVariantInit(&varName);

        // Get the endpoint's friendly-name property.
        hr = pProps->GetValue(
                       PKEY_Device_FriendlyName, &varName);
        EXIT_ON_ERROR(hr)

        // Print endpoint friendly name and endpoint ID.
        printf("Endpoint %d: \"%S\" (%S)\n",
               i, varName.pwszVal, pwszID);

        CoTaskMemFree(pwszID);
        pwszID = NULL;
        PropVariantClear(&varName);
        SAFE_RELEASE(pProps)
        SAFE_RELEASE(pEndpoint)
    }
    SAFE_RELEASE(pEnumerator)
    SAFE_RELEASE(pCollection)
    return;

Exit:
    printf("Error!\n");
    CoTaskMemFree(pwszID);
    SAFE_RELEASE(pEnumerator)
    SAFE_RELEASE(pCollection)
    SAFE_RELEASE(pEndpoint)
    SAFE_RELEASE(pProps)
}
```



<span data-ttu-id="349f4-135">上述程式碼範例中的 FAILED 巨集定義在標頭檔 Winerror.h 中。</span><span class="sxs-lookup"><span data-stu-id="349f4-135">The FAILED macro in the preceding code example is defined in header file Winerror.h.</span></span>

<span data-ttu-id="349f4-136">在上述程式碼範例中，PrintEndpointNames 函數中的 **for** 迴圈主體會呼叫 [**IMMDevice：： GetId**](/windows/desktop/api/Mmdeviceapi/nf-mmdeviceapi-immdevice-getid)方法，以取得 **IMMDevice** 介面實例所代表之音訊端點裝置的 [端點識別碼字串](endpoint-id-strings.md)。</span><span class="sxs-lookup"><span data-stu-id="349f4-136">In the preceding code example, the **for**-loop body in the PrintEndpointNames function calls the [**IMMDevice::GetId**](/windows/desktop/api/Mmdeviceapi/nf-mmdeviceapi-immdevice-getid) method to obtain the [endpoint ID string](endpoint-id-strings.md) for the audio endpoint device that is represented by the **IMMDevice** interface instance.</span></span> <span data-ttu-id="349f4-137">此字串可唯一識別與系統中所有其他音訊端點裝置相關的裝置。</span><span class="sxs-lookup"><span data-stu-id="349f4-137">The string uniquely identifies the device with respect to all of the other audio endpoint devices in the system.</span></span> <span data-ttu-id="349f4-138">用戶端可以藉由呼叫 [**IMMDeviceEnumerator：： GetDevice**](/windows/desktop/api/Mmdeviceapi/nf-mmdeviceapi-immdeviceenumerator-getdevice) 方法，使用端點識別碼字串來建立音訊端點裝置的實例，或在不同的進程中建立實例。</span><span class="sxs-lookup"><span data-stu-id="349f4-138">A client can use the endpoint ID string to create an instance of the audio endpoint device at a later time or in a different process by calling the [**IMMDeviceEnumerator::GetDevice**](/windows/desktop/api/Mmdeviceapi/nf-mmdeviceapi-immdeviceenumerator-getdevice) method.</span></span> <span data-ttu-id="349f4-139">用戶端應將端點識別碼字串的內容視為不透明。</span><span class="sxs-lookup"><span data-stu-id="349f4-139">Clients should treat the contents of the endpoint ID string as opaque.</span></span> <span data-ttu-id="349f4-140">也就是說，用戶端不應該嘗試剖析字串的內容，以取得裝置的相關資訊。</span><span class="sxs-lookup"><span data-stu-id="349f4-140">That is, clients should not attempt to parse the contents of the string to obtain information about the device.</span></span> <span data-ttu-id="349f4-141">原因是字串格式未定義，而且可能會從一個 MMDevice API 的執行變更為下一個。</span><span class="sxs-lookup"><span data-stu-id="349f4-141">The reason is that the string format is undefined and might change from one implementation of the MMDevice API to the next.</span></span>

<span data-ttu-id="349f4-142">上述程式碼範例中 PrintEndpointNames 函式所取得的易記裝置名稱和端點識別碼字串，與 DirectSound 在裝置列舉期間提供的易記裝置名稱和端點識別碼字串相同。</span><span class="sxs-lookup"><span data-stu-id="349f4-142">The friendly device names and endpoint ID strings that are obtained by the PrintEndpointNames function in the preceding code example are identical to the friendly device names and endpoint ID strings that are provided by DirectSound during device enumeration.</span></span> <span data-ttu-id="349f4-143">如需詳細資訊，請參閱 [舊版音訊應用程式的音訊事件](audio-events-for-legacy-audio-applications.md)。</span><span class="sxs-lookup"><span data-stu-id="349f4-143">For more information, see [Audio Events for Legacy Audio Applications](audio-events-for-legacy-audio-applications.md).</span></span>

<span data-ttu-id="349f4-144">在上述程式碼範例中，PrintEndpointNames 函式會呼叫 **CoCreateInstance** 函數，以建立系統中音訊端點裝置的列舉值。</span><span class="sxs-lookup"><span data-stu-id="349f4-144">In the preceding code example, the PrintEndpointNames function calls the **CoCreateInstance** function to create an enumerator for the audio endpoint devices in the system.</span></span> <span data-ttu-id="349f4-145">除非呼叫程式之前呼叫 **CoInitialize** 或 **CoInitializeEx** 函式來初始化 COM 程式庫，否則 **CoCreateInstance** 呼叫會失敗。</span><span class="sxs-lookup"><span data-stu-id="349f4-145">Unless the calling program previously called either the **CoInitialize** or **CoInitializeEx** function to initialize the COM library, the **CoCreateInstance** call will fail.</span></span> <span data-ttu-id="349f4-146">如需有關 **CoCreateInstance**、 **CoInitialize** 和 **CoInitializeEx** 的詳細資訊，請參閱 Windows SDK 檔。</span><span class="sxs-lookup"><span data-stu-id="349f4-146">For more information about **CoCreateInstance**, **CoInitialize**, and **CoInitializeEx**, see the Windows SDK documentation.</span></span>

<span data-ttu-id="349f4-147">如需 **IMMDeviceEnumerator**、 **IMMDeviceCollection** 和 **IMMDevice** 介面的詳細資訊，請參閱 [MMDevice API](mmdevice-api.md)。</span><span class="sxs-lookup"><span data-stu-id="349f4-147">For more information about the **IMMDeviceEnumerator**, **IMMDeviceCollection**, and **IMMDevice** interfaces, see [MMDevice API](mmdevice-api.md).</span></span>

## <a name="related-topics"></a><span data-ttu-id="349f4-148">相關主題</span><span class="sxs-lookup"><span data-stu-id="349f4-148">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="349f4-149">音訊端點裝置</span><span class="sxs-lookup"><span data-stu-id="349f4-149">Audio Endpoint Devices</span></span>](audio-endpoint-devices.md)
</dt> </dl>

 

 



