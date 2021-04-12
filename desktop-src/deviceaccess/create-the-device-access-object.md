---
title: 執行裝置存取物件
description: 本主題說明如何將裝置存取物件具現化，並使用它來存取裝置。
ms.assetid: 26619A25-67FE-44DC-82DD-36076326748D
ms.topic: article
ms.date: 02/11/2020
ms.openlocfilehash: 60bd634f72b29bb6520223a7933b22a396f99723
ms.sourcegitcommit: 3d718d8f69d3f86eaecf94c5705d761c5a9ef4a1
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 10/20/2020
ms.locfileid: "104463893"
---
# <a name="implement-the-device-access-object"></a>執行裝置存取物件

本主題說明如何將裝置存取物件具現化，並使用它來存取裝置。 具現化的類別會實 [**IDeviceIoControl**](/windows/win32/api/Deviceaccess/nn-deviceaccess-ideviceiocontrol) 和 [**ICreateDeviceAccessAsync**](/windows/win32/api/Deviceaccess/nn-deviceaccess-icreatedeviceaccessasync) 介面。

## <a name="instructions"></a>指示

### <a name="step-1"></a>步驟 1

若要具現化裝置存取物件，您必須先呼叫 [**CreateDeviceAccessInstance**](/windows/win32/api/deviceaccess/nf-deviceaccess-createdeviceaccessinstance) 函數。 如果 **CreateDeviceAccessInstance** 成功，您就可以呼叫 [**wait**](/windows/win32/api/Deviceaccess/nf-deviceaccess-icreatedeviceaccessasync-wait) 方法來等候非同步作業完成。 如果 **Wait** 成功，您可以從 [**GetResult**](/windows/win32/api/Deviceaccess/nf-deviceaccess-icreatedeviceaccessasync-getresult)方法取得 [**IDeviceIoControl**](/windows/win32/api/Deviceaccess/nn-deviceaccess-ideviceiocontrol)物件 (或適當的錯誤) 。

```C++
HRESULT
CMyServer::Initialize(
        PCWSTR   pszDeviceInterfacePath
    )

/*++
Routine Description:

    This routine is called to initialize the Device Access object.
    It's not part of the constructor as the initialization can fail.
    It opens the device and gets the IDeviceIoControl interface to the device instance
    via the broker.

Arguments:
    pszDeviceInterfacePath - the device interface string that needs to be opened

Return Value:

    HRESULT

--*/

{
    HRESULT hr;
    ICreateDeviceAccessAsync *pDeviceAccess;

     //
     // Here's the actual open call.  This will *fail* if your lowbox does
     // not have the capability mapped to the interface class specified.
     // If you are running this as normal user, it will just pass through to
     // create file.
     //

   hr = CreateDeviceAccessInstance(pszDeviceInterfacePath,
                                   GENERIC_READ|GENERIC_WRITE,
                                   &amp;pDeviceAccess);

    if (FAILED(hr)) {
        return hr;
    }

    if (SUCCEEDED(hr)) {
        hr = pDeviceAccess->Wait(INFINITE);
    }

    if (SUCCEEDED(hr)) {
        hr = pDeviceAccess->GetResult(IID_IDeviceIoControl,
                                            (void **)&amp;m_pDeviceIoControl);
    }

    pDeviceAccess->Release();

    return hr;
}
```



### <a name="step-2"></a>步驟 2

這是呼叫 **DeviceIoControlSync** 方法的範例。


```C++
IFACEMETHODIMP 
CMyServer::put_SevenSegmentDisplay(
    BYTE   value
    )
/*++

Routine Description:
    This routine puts the display value into the device.

Arguments:
    
    value - The value to be written to the device.
    
Return Value:

    HRESULT

--*/
{
    BYTE sevenSegment = 0;
    HRESULT hr;

    if (value >= ARRAYSIZE(g_NumberToMask)) {
        return E_INVALIDARG;
    }


    sevenSegment = g_NumberToMask[value];
    hr = m_pDeviceIoControl->DeviceIoControlSync(
                         IOCTL_OSRUSBFX2_SET_7_SEGMENT_DISPLAY,
                         &amp;sevenSegment,
                         sizeof(BYTE),
                         NULL,
                         0,
                         NULL
                         );

    return hr;
}
```



## <a name="remarks"></a>備註

您也可以使用 [**DeviceIoControlAsync**](/windows/win32/api/Deviceaccess/nf-deviceaccess-ideviceiocontrol-deviceiocontrolasync) 方法，以非同步方式傳送 IOCTL。 在這種情況下，您必須執行 [**IDeviceRequestCompletionCallback**](/windows/win32/api/Deviceaccess/nn-deviceaccess-idevicerequestcompletioncallback) 介面。

## <a name="related-topics"></a>相關主題

[自訂驅動程式存取範例](https://github.com/microsoftarchive/msdn-code-gallery-microsoft/tree/411c271e537727d737a53fa2cbe99eaecac00cc0/Official%20Windows%20Platform%20Sample/Custom%20driver%20access%20sample)、 [適用于內部裝置的 UWP 裝置應用程式](/windows-hardware/drivers/devapps/uwp-device-apps-for-specialized-devices)、 [硬體開發人員中心](/windows-hardware/drivers/)
