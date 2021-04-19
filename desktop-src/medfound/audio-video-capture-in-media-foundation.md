---
description: Microsoft 媒體基礎支援音訊和影片捕捉。
ms.assetid: 8a9d96f8-1096-4b66-a2ec-8a95d754ea72
title: 媒體基礎中的音訊/影片捕獲
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 506c14ee4ab94a27cfafbe18a97ffa8f05676f1f
ms.sourcegitcommit: c16214e53680dc71d1c07111b51f72b82a4512d8
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 03/03/2021
ms.locfileid: "106981934"
---
# <a name="audiovideo-capture-in-media-foundation"></a><span data-ttu-id="cd632-103">媒體基礎中的音訊/影片捕獲</span><span class="sxs-lookup"><span data-stu-id="cd632-103">Audio/Video Capture in Media Foundation</span></span>

<span data-ttu-id="cd632-104">Microsoft 媒體基礎支援音訊和影片捕捉。</span><span class="sxs-lookup"><span data-stu-id="cd632-104">Microsoft Media Foundation supports audio and video capture.</span></span> <span data-ttu-id="cd632-105">您可以透過 UVC 類別驅動程式支援影片捕獲裝置，而且必須與 UVC 1.1 相容。</span><span class="sxs-lookup"><span data-stu-id="cd632-105">Video capture devices are supported through the UVC class driver and must be compatible with UVC 1.1.</span></span> <span data-ttu-id="cd632-106">您可以透過 Windows 音訊會話 API (WASAPI) 來支援音訊捕獲裝置。</span><span class="sxs-lookup"><span data-stu-id="cd632-106">Audio capture devices are supported through Windows Audio Session API (WASAPI).</span></span>

<span data-ttu-id="cd632-107">捕獲裝置會以媒體來源物件媒體基礎表示，它會公開 [**IMFMediaSource**](/windows/desktop/api/mfidl/nn-mfidl-imfmediasource) 介面。</span><span class="sxs-lookup"><span data-stu-id="cd632-107">A capture device is represented in Media Foundation by a media source object, which exposes the [**IMFMediaSource**](/windows/desktop/api/mfidl/nn-mfidl-imfmediasource) interface.</span></span> <span data-ttu-id="cd632-108">在大部分情況下，應用程式不會直接使用此介面，但會使用較高層級的 API （例如 [來源讀取器](source-reader.md) ）來控制捕獲裝置。</span><span class="sxs-lookup"><span data-stu-id="cd632-108">In most cases, the application will not use this interface directly, but will use a higher-level API such as the [Source Reader](source-reader.md) to control the capture device.</span></span>

## <a name="enumerate-capture-devices"></a><span data-ttu-id="cd632-109">列舉捕獲裝置</span><span class="sxs-lookup"><span data-stu-id="cd632-109">Enumerate Capture Devices</span></span>

<span data-ttu-id="cd632-110">若要列舉系統上的捕獲裝置，請執行下列步驟：</span><span class="sxs-lookup"><span data-stu-id="cd632-110">To enumerate the capture devices on the system, perform the following steps:</span></span>

1.  <span data-ttu-id="cd632-111">呼叫 [**MFCreateAttributes**](/windows/desktop/api/mfapi/nf-mfapi-mfcreateattributes) 函數來建立屬性存放區。</span><span class="sxs-lookup"><span data-stu-id="cd632-111">Call the [**MFCreateAttributes**](/windows/desktop/api/mfapi/nf-mfapi-mfcreateattributes) function to create an attribute store.</span></span>
2.  <span data-ttu-id="cd632-112">將 [ [MF \_ DEVSOURCE \_ 屬性 \_ 來源 \_ 類型](mf-devsource-attribute-source-type.md) ] 屬性設定為下列其中一個值：</span><span class="sxs-lookup"><span data-stu-id="cd632-112">Set the [MF\_DEVSOURCE\_ATTRIBUTE\_SOURCE\_TYPE](mf-devsource-attribute-source-type.md) attribute to one of the following values:</span></span>

    | <span data-ttu-id="cd632-113">值</span><span class="sxs-lookup"><span data-stu-id="cd632-113">Value</span></span>                                                    | <span data-ttu-id="cd632-114">描述</span><span class="sxs-lookup"><span data-stu-id="cd632-114">Description</span></span>                      |
    |----------------------------------------------------------|----------------------------------|
    | <span data-ttu-id="cd632-115">**MF \_ DEVSOURCE \_ 屬性 \_ 來源 \_ 類型 \_ AUDCAP \_ GUID**</span><span class="sxs-lookup"><span data-stu-id="cd632-115">**MF\_DEVSOURCE\_ATTRIBUTE\_SOURCE\_TYPE\_AUDCAP\_GUID**</span></span> | <span data-ttu-id="cd632-116">列舉音訊捕獲裝置。</span><span class="sxs-lookup"><span data-stu-id="cd632-116">Enumerate audio capture devices.</span></span> |
    | <span data-ttu-id="cd632-117">**MF \_ DEVSOURCE \_ 屬性 \_ 來源 \_ 類型 \_ VIDCAP \_ GUID**</span><span class="sxs-lookup"><span data-stu-id="cd632-117">**MF\_DEVSOURCE\_ATTRIBUTE\_SOURCE\_TYPE\_VIDCAP\_GUID**</span></span> | <span data-ttu-id="cd632-118">列舉影片捕獲裝置。</span><span class="sxs-lookup"><span data-stu-id="cd632-118">Enumerate video capture devices.</span></span> |

    

     

3.  <span data-ttu-id="cd632-119">呼叫 [**MFEnumDeviceSources**](/windows/desktop/api/mfidl/nf-mfidl-mfenumdevicesources) 函數。</span><span class="sxs-lookup"><span data-stu-id="cd632-119">Call the [**MFEnumDeviceSources**](/windows/desktop/api/mfidl/nf-mfidl-mfenumdevicesources) function.</span></span> <span data-ttu-id="cd632-120">此函數會配置 [**IMFActivate**](/windows/desktop/api/mfobjects/nn-mfobjects-imfactivate) 指標的陣列。</span><span class="sxs-lookup"><span data-stu-id="cd632-120">This function allocates an array of [**IMFActivate**](/windows/desktop/api/mfobjects/nn-mfobjects-imfactivate) pointers.</span></span> <span data-ttu-id="cd632-121">每個指標都代表系統上一個裝置的啟用物件。</span><span class="sxs-lookup"><span data-stu-id="cd632-121">Each pointer represents an activation object for one device on the system.</span></span>
4.  <span data-ttu-id="cd632-122">呼叫 [**IMFActivate：： ActivateObject**](/windows/desktop/api/mfobjects/nf-mfobjects-imfactivate-activateobject) 方法，從其中一個啟用物件建立媒體來源的實例。</span><span class="sxs-lookup"><span data-stu-id="cd632-122">Call the [**IMFActivate::ActivateObject**](/windows/desktop/api/mfobjects/nf-mfobjects-imfactivate-activateobject) method to create an instance of the media source from one of the activation objects.</span></span>

<span data-ttu-id="cd632-123">下列範例會在列舉清單中建立第一個影片捕獲裝置的媒體來源：</span><span class="sxs-lookup"><span data-stu-id="cd632-123">The following example creates a media source for the first video capture device in the enumeration list:</span></span>


```C++
HRESULT CreateVideoCaptureDevice(IMFMediaSource **ppSource)
{
    *ppSource = NULL;

    UINT32 count = 0;

    IMFAttributes *pConfig = NULL;
    IMFActivate **ppDevices = NULL;

    // Create an attribute store to hold the search criteria.
    HRESULT hr = MFCreateAttributes(&pConfig, 1);

    // Request video capture devices.
    if (SUCCEEDED(hr))
    {
        hr = pConfig->SetGUID(
            MF_DEVSOURCE_ATTRIBUTE_SOURCE_TYPE, 
            MF_DEVSOURCE_ATTRIBUTE_SOURCE_TYPE_VIDCAP_GUID
            );
    }

    // Enumerate the devices,
    if (SUCCEEDED(hr))
    {
        hr = MFEnumDeviceSources(pConfig, &ppDevices, &count);
    }

    // Create a media source for the first device in the list.
    if (SUCCEEDED(hr))
    {
        if (count > 0)
        {
            hr = ppDevices[0]->ActivateObject(IID_PPV_ARGS(ppSource));
        }
        else
        {
            hr = MF_E_NOT_FOUND;
        }
    }

    for (DWORD i = 0; i < count; i++)
    {
        ppDevices[i]->Release();
    }
    CoTaskMemFree(ppDevices);
    return hr;
}
```



<span data-ttu-id="cd632-124">您可以查詢啟用物件中的各種屬性，包括下列各項：</span><span class="sxs-lookup"><span data-stu-id="cd632-124">You can query the activation objects for various attributes, including the following:</span></span>

-   <span data-ttu-id="cd632-125">[ [MF \_ DEVSOURCE 屬性] 的 [ \_ \_ 易記 \_ 名稱](mf-devsource-attribute-friendly-name.md) ] 屬性包含裝置的顯示名稱。</span><span class="sxs-lookup"><span data-stu-id="cd632-125">The [MF\_DEVSOURCE\_ATTRIBUTE\_FRIENDLY\_NAME](mf-devsource-attribute-friendly-name.md) attribute contains the display name of the device.</span></span> <span data-ttu-id="cd632-126">顯示名稱適用于向使用者顯示，但可能不是唯一的。</span><span class="sxs-lookup"><span data-stu-id="cd632-126">The display name is suitable for showing to the user, but might not be unique.</span></span>
-   <span data-ttu-id="cd632-127">針對影片裝置， [MF \_ DEVSOURCE \_ 屬性 \_ 來源 \_ 類型 \_ VIDCAP \_ 符號 \_ 連結](mf-devsource-attribute-source-type-vidcap-symbolic-link.md) 屬性包含裝置的符號連結。</span><span class="sxs-lookup"><span data-stu-id="cd632-127">For video devices, the [MF\_DEVSOURCE\_ATTRIBUTE\_SOURCE\_TYPE\_VIDCAP\_SYMBOLIC\_LINK](mf-devsource-attribute-source-type-vidcap-symbolic-link.md) attribute contains the symbolic link to the device.</span></span> <span data-ttu-id="cd632-128">符號連結可唯一識別系統上的裝置，但不是可讀取的字串。</span><span class="sxs-lookup"><span data-stu-id="cd632-128">The symbolic link uniquely identifies the device on the system, but is not a readable string.</span></span>
-   <span data-ttu-id="cd632-129">針對音訊裝置， [MF \_ DEVSOURCE \_ 屬性 \_ 來源 \_ 類型 \_ AUDCAP \_ 端點 \_ 識別碼](mf-devsource-attribute-source-type-audcap-endpoint-id.md) 屬性包含裝置的音訊端點識別碼。</span><span class="sxs-lookup"><span data-stu-id="cd632-129">For audio devices, the [MF\_DEVSOURCE\_ATTRIBUTE\_SOURCE\_TYPE\_AUDCAP\_ENDPOINT\_ID](mf-devsource-attribute-source-type-audcap-endpoint-id.md) attribute contains the audio endpoint ID of the device.</span></span> <span data-ttu-id="cd632-130">音訊端點識別碼類似于符號連結。</span><span class="sxs-lookup"><span data-stu-id="cd632-130">The audio endpoint ID is similar to a symbolic link.</span></span> <span data-ttu-id="cd632-131">它可唯一識別系統上的裝置，但不是可讀取的字串。</span><span class="sxs-lookup"><span data-stu-id="cd632-131">It uniquely identifies the device on the system, but is not a readable string.</span></span>

<span data-ttu-id="cd632-132">下列範例會採用 [**IMFActivate**](/windows/desktop/api/mfobjects/nn-mfobjects-imfactivate) 指標的陣列，並將每個裝置的顯示名稱列印到 [偵錯工具] 視窗：</span><span class="sxs-lookup"><span data-stu-id="cd632-132">The following example takes an array of [**IMFActivate**](/windows/desktop/api/mfobjects/nn-mfobjects-imfactivate) pointers and prints the display name of each device to the debug window:</span></span>


```C++
void DebugShowDeviceNames(IMFActivate **ppDevices, UINT count)
{
    for (DWORD i = 0; i < count; i++)
    {
        HRESULT hr = S_OK;
        WCHAR *szFriendlyName = NULL;
    
        // Try to get the display name.
        UINT32 cchName;
        hr = ppDevices[i]->GetAllocatedString(
            MF_DEVSOURCE_ATTRIBUTE_FRIENDLY_NAME,
            &szFriendlyName, &cchName);

        if (SUCCEEDED(hr))
        {
            OutputDebugString(szFriendlyName);
            OutputDebugString(L"\n");
        }
        CoTaskMemFree(szFriendlyName);
    }
}
```



<span data-ttu-id="cd632-133">如果您已經知道影片裝置的符號連結，還有另一種方式可建立裝置的媒體來源：</span><span class="sxs-lookup"><span data-stu-id="cd632-133">If you already know the symbolic link for a video device, there is another way to create the media source for the device:</span></span>

1.  <span data-ttu-id="cd632-134">呼叫 [**MFCreateAttributes**](/windows/desktop/api/mfapi/nf-mfapi-mfcreateattributes) 以建立屬性存放區。</span><span class="sxs-lookup"><span data-stu-id="cd632-134">Call [**MFCreateAttributes**](/windows/desktop/api/mfapi/nf-mfapi-mfcreateattributes) to create an attribute store.</span></span>
2.  <span data-ttu-id="cd632-135">將 [ [mf \_ DEVSOURCE \_ 屬性 \_ 來源 \_ 類型](mf-devsource-attribute-source-type.md) ] 屬性設定為 [ **mf \_ DEVSOURCE \_ 屬性 \_ 來源 \_ 類型 \_ VIDCAP \_ GUID**]。</span><span class="sxs-lookup"><span data-stu-id="cd632-135">Set the [MF\_DEVSOURCE\_ATTRIBUTE\_SOURCE\_TYPE](mf-devsource-attribute-source-type.md) attribute to **MF\_DEVSOURCE\_ATTRIBUTE\_SOURCE\_TYPE\_VIDCAP\_GUID**.</span></span>
3.  <span data-ttu-id="cd632-136">將 [ [MF \_ DEVSOURCE \_ 屬性 \_ 來源 \_ 類型 \_ VIDCAP \_ 符號 \_ 連結](mf-devsource-attribute-source-type-vidcap-symbolic-link.md) ] 屬性設定為符號連結。</span><span class="sxs-lookup"><span data-stu-id="cd632-136">Set the [MF\_DEVSOURCE\_ATTRIBUTE\_SOURCE\_TYPE\_VIDCAP\_SYMBOLIC\_LINK](mf-devsource-attribute-source-type-vidcap-symbolic-link.md) attribute to the symbolic link.</span></span>
4.  <span data-ttu-id="cd632-137">請呼叫 [**MFCreateDeviceSource**](/windows/desktop/api/mfidl/nf-mfidl-mfcreatedevicesource) 或 [**MFCreateDeviceSourceActivate**](/windows/desktop/api/mfidl/nf-mfidl-mfcreatedevicesourceactivate) 函數。</span><span class="sxs-lookup"><span data-stu-id="cd632-137">Call either the [**MFCreateDeviceSource**](/windows/desktop/api/mfidl/nf-mfidl-mfcreatedevicesource) or [**MFCreateDeviceSourceActivate**](/windows/desktop/api/mfidl/nf-mfidl-mfcreatedevicesourceactivate) function.</span></span> <span data-ttu-id="cd632-138">前者會傳回 [**IMFMediaSource**](/windows/desktop/api/mfidl/nn-mfidl-imfmediasource) 指標。</span><span class="sxs-lookup"><span data-stu-id="cd632-138">The former returns an [**IMFMediaSource**](/windows/desktop/api/mfidl/nn-mfidl-imfmediasource) pointer.</span></span> <span data-ttu-id="cd632-139">後者會傳回啟用物件的 [**IMFActivate**](/windows/desktop/api/mfobjects/nn-mfobjects-imfactivate) 指標。</span><span class="sxs-lookup"><span data-stu-id="cd632-139">The latter returns an [**IMFActivate**](/windows/desktop/api/mfobjects/nn-mfobjects-imfactivate) pointer to an activation object.</span></span> <span data-ttu-id="cd632-140">您可以使用啟用物件來建立來源。</span><span class="sxs-lookup"><span data-stu-id="cd632-140">You can use the activation object to create the source.</span></span> <span data-ttu-id="cd632-141"> (啟用物件可以封送處理至另一個進程，因此如果您想要在另一個進程中建立來源，則會很有用。</span><span class="sxs-lookup"><span data-stu-id="cd632-141">(An activation object can be marshaled to another process, so it is useful if you want to create the source in another process.</span></span> <span data-ttu-id="cd632-142">如需詳細資訊，請參閱 [啟用物件](activation-objects.md)。 ) </span><span class="sxs-lookup"><span data-stu-id="cd632-142">For more information, see [Activation Objects](activation-objects.md).)</span></span>

<span data-ttu-id="cd632-143">下列範例會採用影片裝置的符號連結，並建立媒體來源。</span><span class="sxs-lookup"><span data-stu-id="cd632-143">The following example takes the symbolic link of a video device and creates a media source.</span></span>


```C++
HRESULT CreateVideoCaptureDevice(PCWSTR *pszSymbolicLink, IMFMediaSource **ppSource)
{
    *ppSource = NULL;
    
    IMFAttributes *pAttributes = NULL;
    IMFMediaSource *pSource = NULL;

    HRESULT hr = MFCreateAttributes(&pAttributes, 2);

    // Set the device type to video.
    if (SUCCEEDED(hr))
    {
        hr = pAttributes->SetGUID(
            MF_DEVSOURCE_ATTRIBUTE_SOURCE_TYPE,
            MF_DEVSOURCE_ATTRIBUTE_SOURCE_TYPE_VIDCAP_GUID
            );
    }


    // Set the symbolic link.
    if (SUCCEEDED(hr))
    {
        hr = pAttributes->SetString(
            MF_DEVSOURCE_ATTRIBUTE_SOURCE_TYPE_VIDCAP_SYMBOLIC_LINK,
            (LPCWSTR)pszSymbolicLink
            );            
    }

    if (SUCCEEDED(hr))
    {
        hr = MFCreateDeviceSource(pAttributes, ppSource);
    }

    SafeRelease(&pAttributes);
    return hr;    
}
```



<span data-ttu-id="cd632-144">從音訊端點識別碼建立音訊裝置有相當的方式：</span><span class="sxs-lookup"><span data-stu-id="cd632-144">There is an equivalent way to create an audio device from the audio endpoint ID:</span></span>

1.  <span data-ttu-id="cd632-145">呼叫 [**MFCreateAttributes**](/windows/desktop/api/mfapi/nf-mfapi-mfcreateattributes) 以建立屬性存放區。</span><span class="sxs-lookup"><span data-stu-id="cd632-145">Call [**MFCreateAttributes**](/windows/desktop/api/mfapi/nf-mfapi-mfcreateattributes) to create an attribute store.</span></span>
2.  <span data-ttu-id="cd632-146">將 [ [mf \_ DEVSOURCE \_ 屬性 \_ 來源 \_ 類型](mf-devsource-attribute-source-type.md) ] 屬性設定為 [ **mf \_ DEVSOURCE \_ 屬性 \_ 來源 \_ 類型 \_ AUDCAP \_ GUID**]。</span><span class="sxs-lookup"><span data-stu-id="cd632-146">Set the [MF\_DEVSOURCE\_ATTRIBUTE\_SOURCE\_TYPE](mf-devsource-attribute-source-type.md) attribute to **MF\_DEVSOURCE\_ATTRIBUTE\_SOURCE\_TYPE\_AUDCAP\_GUID**.</span></span>
3.  <span data-ttu-id="cd632-147">將 [ [MF \_ DEVSOURCE \_ 屬性 \_ 來源 \_ 類型 \_ AUDCAP \_ 端點 \_ 識別碼](mf-devsource-attribute-source-type-audcap-endpoint-id.md) ] 屬性設定為端點識別碼。</span><span class="sxs-lookup"><span data-stu-id="cd632-147">Set the [MF\_DEVSOURCE\_ATTRIBUTE\_SOURCE\_TYPE\_AUDCAP\_ENDPOINT\_ID](mf-devsource-attribute-source-type-audcap-endpoint-id.md) attribute to the endpoint ID.</span></span>
4.  <span data-ttu-id="cd632-148">請呼叫 [**MFCreateDeviceSource**](/windows/desktop/api/mfidl/nf-mfidl-mfcreatedevicesource) 或 [**MFCreateDeviceSourceActivate**](/windows/desktop/api/mfidl/nf-mfidl-mfcreatedevicesourceactivate) 函數。</span><span class="sxs-lookup"><span data-stu-id="cd632-148">Call either the [**MFCreateDeviceSource**](/windows/desktop/api/mfidl/nf-mfidl-mfcreatedevicesource) or [**MFCreateDeviceSourceActivate**](/windows/desktop/api/mfidl/nf-mfidl-mfcreatedevicesourceactivate) function.</span></span>

<span data-ttu-id="cd632-149">下列範例會使用音訊端點識別碼並建立媒體來源。</span><span class="sxs-lookup"><span data-stu-id="cd632-149">The following example takes an audio endpoint ID and creates a media source.</span></span>


```C++
HRESULT CreateAudioCaptureDevice(PCWSTR *pszEndPointID, IMFMediaSource **ppSource)
{
    *ppSource = NULL;
    
    IMFAttributes *pAttributes = NULL;
    IMFMediaSource *pSource = NULL;

    HRESULT hr = MFCreateAttributes(&pAttributes, 2);

    // Set the device type to audio.
    if (SUCCEEDED(hr))
    {
        hr = pAttributes->SetGUID(
            MF_DEVSOURCE_ATTRIBUTE_SOURCE_TYPE,
            MF_DEVSOURCE_ATTRIBUTE_SOURCE_TYPE_AUDCAP_GUID
            );
    }

    // Set the endpoint ID.
    if (SUCCEEDED(hr))
    {
        hr = pAttributes->SetString(
            MF_DEVSOURCE_ATTRIBUTE_SOURCE_TYPE_AUDCAP_ENDPOINT_ID,
            (LPCWSTR)pszEndPointID
            ); 
    }

    if (SUCCEEDED(hr))
    {
        hr = MFCreateDeviceSource(pAttributes, ppSource);
    }

    SafeRelease(&pAttributes);
    return hr;    
}
```



## <a name="use-a-capture-device"></a><span data-ttu-id="cd632-150">使用 capture 裝置</span><span class="sxs-lookup"><span data-stu-id="cd632-150">Use a capture device</span></span>

<span data-ttu-id="cd632-151">建立 capture 裝置的媒體來源之後，請使用 [來源讀取器](source-reader.md) 從裝置取得資料。</span><span class="sxs-lookup"><span data-stu-id="cd632-151">After you create the media source for a capture device, use the [Source Reader](source-reader.md) to get data from the device.</span></span> <span data-ttu-id="cd632-152">來源讀取器會提供包含捕獲音訊資料或影片畫面的媒體範例。</span><span class="sxs-lookup"><span data-stu-id="cd632-152">The Source Reader delivers media samples that contain the capture audio data or video frames.</span></span> <span data-ttu-id="cd632-153">下一步取決於您的應用程式案例：</span><span class="sxs-lookup"><span data-stu-id="cd632-153">The next step depends on your application scenario:</span></span>

-   <span data-ttu-id="cd632-154">影片預覽：使用 Microsoft Direct3D 或 Direct2D 來顯示影片。</span><span class="sxs-lookup"><span data-stu-id="cd632-154">Video preview: Use Microsoft Direct3D or Direct2D to display the video.</span></span>
-   <span data-ttu-id="cd632-155">檔案捕獲：使用 [接收寫入器](sink-writer.md) 對檔案進行編碼。</span><span class="sxs-lookup"><span data-stu-id="cd632-155">File capture: Use the [Sink Writer](sink-writer.md) to encode the file.</span></span>
-   <span data-ttu-id="cd632-156">音訊預覽：使用 [WASAPI](/windows/desktop/CoreAudio/wasapi)。</span><span class="sxs-lookup"><span data-stu-id="cd632-156">Audio preview: Use [WASAPI](/windows/desktop/CoreAudio/wasapi).</span></span>

<span data-ttu-id="cd632-157">如果您想要將音訊捕獲與影片捕獲結合，請使用 *匯總媒體來源*。</span><span class="sxs-lookup"><span data-stu-id="cd632-157">If you want to combine audio capture with video capture, use the *aggregate media source*.</span></span> <span data-ttu-id="cd632-158">匯總媒體來源包含媒體來源的集合，並將其所有串流合併為單一媒體來源物件。</span><span class="sxs-lookup"><span data-stu-id="cd632-158">The aggregate media source contains a collection of media sources and combines all of their streams into a single media source object.</span></span> <span data-ttu-id="cd632-159">若要建立匯總媒體來源的實例，請呼叫 [**MFCreateAggregateSource**](/windows/desktop/api/mfidl/nf-mfidl-mfcreateaggregatesource) 函數。</span><span class="sxs-lookup"><span data-stu-id="cd632-159">To create an instance of the aggregate media source, call the [**MFCreateAggregateSource**](/windows/desktop/api/mfidl/nf-mfidl-mfcreateaggregatesource) function.</span></span>

## <a name="shut-down-the-capture-device"></a><span data-ttu-id="cd632-160">關閉捕獲裝置</span><span class="sxs-lookup"><span data-stu-id="cd632-160">Shut down the capture device</span></span>

<span data-ttu-id="cd632-161">當不再需要 capture 裝置時，您必須在透過呼叫 [**MFCreateDeviceSource**](/windows/desktop/api/mfidl/nf-mfidl-mfcreatedevicesource)或 [**IMFActivate：： ActivateObject**](/windows/desktop/api/mfobjects/nf-mfobjects-imfactivate-activateobject)取得的 [**IMFMediaSource**](/windows/desktop/api/mfidl/nn-mfidl-imfmediasource)物件上呼叫 [**Shutdown**](/windows/desktop/api/mfidl/nf-mfidl-imfmediasource-shutdown) ，以關閉裝置。</span><span class="sxs-lookup"><span data-stu-id="cd632-161">When the capture device is no longer needed, you must shut down the device by calling [**Shutdown**](/windows/desktop/api/mfidl/nf-mfidl-imfmediasource-shutdown) on the [**IMFMediaSource**](/windows/desktop/api/mfidl/nn-mfidl-imfmediasource) object you obtained by calling [**MFCreateDeviceSource**](/windows/desktop/api/mfidl/nf-mfidl-mfcreatedevicesource) or [**IMFActivate::ActivateObject**](/windows/desktop/api/mfobjects/nf-mfobjects-imfactivate-activateobject).</span></span> <span data-ttu-id="cd632-162">無法呼叫 **關機** 可能會導致記憶體連結，因為系統可能會保留 **IMFMediaSource** 資源的參考，直到呼叫 **關機** 為止。</span><span class="sxs-lookup"><span data-stu-id="cd632-162">Failure to call **Shutdown** can result in memory links because the system may keep a reference to **IMFMediaSource** resources until **Shutdown** is called.</span></span>


```C++
if (g_pSource)
{
    g_pSource->Shutdown();
    g_pSource->Release();
    g_pSource = NULL;
}
```



<span data-ttu-id="cd632-163">如果您將包含符號連結的字串配置到 capture 裝置，您也應該釋放此物件。</span><span class="sxs-lookup"><span data-stu-id="cd632-163">If you allocated a string containing the symbolic link to a capture device, you should release this object as well.</span></span>


```C++
    CoTaskMemFree(g_pwszSymbolicLink);
    g_pwszSymbolicLink = NULL;

    g_cchSymbolicLink = 0;
```



## <a name="related-topics"></a><span data-ttu-id="cd632-164">相關主題</span><span class="sxs-lookup"><span data-stu-id="cd632-164">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="cd632-165">音訊/視訊擷取</span><span class="sxs-lookup"><span data-stu-id="cd632-165">Audio/Video Capture</span></span>](audio-video-capture.md)
</dt> </dl>

 

 
