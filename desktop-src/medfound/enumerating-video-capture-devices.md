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
# <a name="enumerating-video-capture-devices"></a>列舉影片捕獲裝置

本主題說明如何列舉使用者系統上的影片捕獲裝置，以及如何建立裝置的實例。

若要列舉系統上的影片捕獲裝置，請執行下列動作：

1.  呼叫 [**MFCreateAttributes**](/windows/desktop/api/mfapi/nf-mfapi-mfcreateattributes) 以建立屬性存放區。 此函式會接收 [**IMFAttributes**](/windows/desktop/api/mfobjects/nn-mfobjects-imfattributes) 指標。
2.  呼叫 [**IMFAttributes：： SetGUID**](/windows/desktop/api/mfobjects/nf-mfobjects-imfattributes-setguid) 來設定 [MF \_ DEVSOURCE \_ 屬性 \_ 來源 \_ 類型](mf-devsource-attribute-source-type.md) 屬性。 將屬性值設定為 [ **MF \_ DEVSOURCE \_ 屬性 \_ 來源 \_ 類型 \_ VIDCAP \_ GUID**]。
3.  呼叫 [**MFEnumDeviceSources**](/windows/desktop/api/mfidl/nf-mfidl-mfenumdevicesources)。 此函式會接收 [**IMFActivate**](/windows/desktop/api/mfobjects/nn-mfobjects-imfactivate) 指標和陣列大小的陣列。 每個指標都代表不同的影片捕獲裝置。

若要建立 capture 裝置的實例：

-   呼叫 [**IMFActivate：： ActivateObject**](/windows/desktop/api/mfobjects/nf-mfobjects-imfactivate-activateobject) 來取得 [**IMFMediaSource**](/windows/desktop/api/mfidl/nn-mfidl-imfmediasource) 介面的指標。

下列程式碼顯示這些步驟：


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



建立媒體來源之後，請釋放介面指標並釋放陣列的記憶體：


```C++
    SafeRelease(&pAttributes);

    for (DWORD i = 0; i < count; i++)
    {
        SafeRelease(&ppDevices[i]);
    }
    CoTaskMemFree(ppDevices);
```



## <a name="related-topics"></a>相關主題

<dl> <dt>

[影片捕獲](video-capture.md)
</dt> </dl>

 

 



