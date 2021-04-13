---
description: 本主題說明如何在使用者系統上列舉影片捕獲裝置，以及如何建立裝置的實例。
ms.assetid: b1267478-329b-4e46-a2ed-1ec11d2e2e6d
title: 列舉影片捕獲裝置
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 57ccdbcf9df284cdccda09939d2d8a27174a2299
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/07/2021
ms.locfileid: "104386030"
---
# <a name="enumerating-video-capture-devices"></a><span data-ttu-id="b14ed-103">列舉影片捕獲裝置</span><span class="sxs-lookup"><span data-stu-id="b14ed-103">Enumerating Video Capture Devices</span></span>

<span data-ttu-id="b14ed-104">本主題說明如何列舉使用者系統上的影片捕獲裝置，以及如何建立裝置的實例。</span><span class="sxs-lookup"><span data-stu-id="b14ed-104">This topic describes how to enumerate the video capture devices on the user's system, and how create an instance of a device.</span></span>

<span data-ttu-id="b14ed-105">若要列舉系統上的影片捕獲裝置，請執行下列動作：</span><span class="sxs-lookup"><span data-stu-id="b14ed-105">To enumerate the video capture devices on the system, do the following:</span></span>

1.  <span data-ttu-id="b14ed-106">呼叫 [**MFCreateAttributes**](/windows/desktop/api/mfapi/nf-mfapi-mfcreateattributes) 以建立屬性存放區。</span><span class="sxs-lookup"><span data-stu-id="b14ed-106">Call [**MFCreateAttributes**](/windows/desktop/api/mfapi/nf-mfapi-mfcreateattributes) to create an attribute store.</span></span> <span data-ttu-id="b14ed-107">此函式會接收 [**IMFAttributes**](/windows/desktop/api/mfobjects/nn-mfobjects-imfattributes) 指標。</span><span class="sxs-lookup"><span data-stu-id="b14ed-107">This function receives an [**IMFAttributes**](/windows/desktop/api/mfobjects/nn-mfobjects-imfattributes) pointer.</span></span>
2.  <span data-ttu-id="b14ed-108">呼叫 [**IMFAttributes：： SetGUID**](/windows/desktop/api/mfobjects/nf-mfobjects-imfattributes-setguid) 來設定 [MF \_ DEVSOURCE \_ 屬性 \_ 來源 \_ 類型](mf-devsource-attribute-source-type.md) 屬性。</span><span class="sxs-lookup"><span data-stu-id="b14ed-108">Call [**IMFAttributes::SetGUID**](/windows/desktop/api/mfobjects/nf-mfobjects-imfattributes-setguid) to set the [MF\_DEVSOURCE\_ATTRIBUTE\_SOURCE\_TYPE](mf-devsource-attribute-source-type.md) attribute.</span></span> <span data-ttu-id="b14ed-109">將屬性值設定為 [ **MF \_ DEVSOURCE \_ 屬性 \_ 來源 \_ 類型 \_ VIDCAP \_ GUID**]。</span><span class="sxs-lookup"><span data-stu-id="b14ed-109">Set the attribute value to **MF\_DEVSOURCE\_ATTRIBUTE\_SOURCE\_TYPE\_VIDCAP\_GUID**.</span></span>
3.  <span data-ttu-id="b14ed-110">呼叫 [**MFEnumDeviceSources**](/windows/desktop/api/mfidl/nf-mfidl-mfenumdevicesources)。</span><span class="sxs-lookup"><span data-stu-id="b14ed-110">Call [**MFEnumDeviceSources**](/windows/desktop/api/mfidl/nf-mfidl-mfenumdevicesources).</span></span> <span data-ttu-id="b14ed-111">此函式會接收 [**IMFActivate**](/windows/desktop/api/mfobjects/nn-mfobjects-imfactivate) 指標和陣列大小的陣列。</span><span class="sxs-lookup"><span data-stu-id="b14ed-111">This function receives an array of [**IMFActivate**](/windows/desktop/api/mfobjects/nn-mfobjects-imfactivate) pointers and the array size.</span></span> <span data-ttu-id="b14ed-112">每個指標都代表不同的影片捕獲裝置。</span><span class="sxs-lookup"><span data-stu-id="b14ed-112">Each pointer represents a distinct video capture device.</span></span>

<span data-ttu-id="b14ed-113">若要建立 capture 裝置的實例：</span><span class="sxs-lookup"><span data-stu-id="b14ed-113">To create an instance of a capture device:</span></span>

-   <span data-ttu-id="b14ed-114">呼叫 [**IMFActivate：： ActivateObject**](/windows/desktop/api/mfobjects/nf-mfobjects-imfactivate-activateobject) 來取得 [**IMFMediaSource**](/windows/desktop/api/mfidl/nn-mfidl-imfmediasource) 介面的指標。</span><span class="sxs-lookup"><span data-stu-id="b14ed-114">Call [**IMFActivate::ActivateObject**](/windows/desktop/api/mfobjects/nf-mfobjects-imfactivate-activateobject) to get a pointer to the [**IMFMediaSource**](/windows/desktop/api/mfidl/nn-mfidl-imfmediasource) interface.</span></span>

<span data-ttu-id="b14ed-115">下列程式碼顯示這些步驟：</span><span class="sxs-lookup"><span data-stu-id="b14ed-115">The following code shows these steps:</span></span>


```C++
HRESULT CreateVideoDeviceSource(IMFMediaSource **ppSource)
{
    *ppSource = NULL;

    IMFMediaSource *pSource = NULL;
    IMFAttributes *pAttributes = NULL;
    IMFActivate **ppDevices = NULL;

    // Create an attribute store to specify the enumeration parameters.
    HRESULT hr = MFCreateAttributes(&pAttributes, 1);
    if (FAILED(hr))
    {
        goto done;
    }

    // Source type: video capture devices
    hr = pAttributes->SetGUID(
        MF_DEVSOURCE_ATTRIBUTE_SOURCE_TYPE, 
        MF_DEVSOURCE_ATTRIBUTE_SOURCE_TYPE_VIDCAP_GUID
        );
    if (FAILED(hr))
    {
        goto done;
    }

    // Enumerate devices.
    UINT32 count;
    hr = MFEnumDeviceSources(pAttributes, &ppDevices, &count);
    if (FAILED(hr))
    {
        goto done;
    }

    if (count == 0)
    {
        hr = E_FAIL;
        goto done;
    }

    // Create the media source object.
    hr = ppDevices[0]->ActivateObject(IID_PPV_ARGS(&pSource));
    if (FAILED(hr))
    {
        goto done;
    }

    *ppSource = pSource;
    (*ppSource)->AddRef();

done:
    SafeRelease(&pAttributes);

    for (DWORD i = 0; i < count; i++)
    {
        SafeRelease(&ppDevices[i]);
    }
    CoTaskMemFree(ppDevices);
    SafeRelease(&pSource);
    return hr;
}
```



<span data-ttu-id="b14ed-116">建立媒體來源之後，請釋放介面指標並釋放陣列的記憶體：</span><span class="sxs-lookup"><span data-stu-id="b14ed-116">After you create media source, release the interface pointers and free the memory for the array:</span></span>


```C++
    SafeRelease(&pAttributes);

    for (DWORD i = 0; i < count; i++)
    {
        SafeRelease(&ppDevices[i]);
    }
    CoTaskMemFree(ppDevices);
```



## <a name="related-topics"></a><span data-ttu-id="b14ed-117">相關主題</span><span class="sxs-lookup"><span data-stu-id="b14ed-117">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="b14ed-118">影片捕獲</span><span class="sxs-lookup"><span data-stu-id="b14ed-118">Video Capture</span></span>](video-capture.md)
</dt> </dl>

 

 



