---
description: 指定用戶端資訊
ms.assetid: 275fda71-61ef-4b50-96fe-bdc0c0266646
title: 指定用戶端資訊
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: c4f6ca094b627b6c2cee16ec587a8c850cd17f78
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/08/2021
ms.locfileid: "104194254"
---
# <a name="specifying-client-information"></a><span data-ttu-id="16bce-103">指定用戶端資訊</span><span class="sxs-lookup"><span data-stu-id="16bce-103">Specifying Client Information</span></span>

<span data-ttu-id="16bce-104">第二個引數中提供的用戶端資訊是由某些設備磁碟機用來將裝置效能優化。</span><span class="sxs-lookup"><span data-stu-id="16bce-104">The client information supplied in the second argument is used by some device drivers to optimize device performance.</span></span> <span data-ttu-id="16bce-105">您的應用程式至少應該提供包含其名稱、主要版本號碼、次要版本號碼和修訂編號的字串。</span><span class="sxs-lookup"><span data-stu-id="16bce-105">At a minimum, your application should provide a string containing its name, a major version number, a minor version number, and a revision number.</span></span> <span data-ttu-id="16bce-106">這些是範例應用程式所提供的欄位。</span><span class="sxs-lookup"><span data-stu-id="16bce-106">These are the fields supplied by the sample application.</span></span>


```C++
#define CLIENT_NAME         L"WPD Sample Application"
#define CLIENT_MAJOR_VER    1
#define CLIENT_MINOR_VER    0
#define CLIENT_REVISION     2
```



<span data-ttu-id="16bce-107">`GetClientInformation`範例應用程式中的函式會建立 **IPortableDeviceValues** 介面並于其中填入用戶端資訊。</span><span class="sxs-lookup"><span data-stu-id="16bce-107">The `GetClientInformation` function in the sample application creates and populates an **IPortableDeviceValues** interface with client information.</span></span> <span data-ttu-id="16bce-108">此函式有兩個主要部分。</span><span class="sxs-lookup"><span data-stu-id="16bce-108">This function has two primary parts.</span></span> <span data-ttu-id="16bce-109">第一個部分會藉由呼叫 CoCreateInstance 函數來建立可移植裝置值物件的實例。</span><span class="sxs-lookup"><span data-stu-id="16bce-109">The first part creates an instance of a portable device-values object by calling the CoCreateInstance function.</span></span>


```C++
HRESULT hr = CoCreateInstance(CLSID_PortableDeviceValues,
                              NULL,
                              CLSCTX_INPROC_SERVER,
                              IID_PPV_ARGS(ppClientInformation));
```



<span data-ttu-id="16bce-110">第二個部分會設定可攜式裝置值物件中的用戶端資訊。</span><span class="sxs-lookup"><span data-stu-id="16bce-110">The second part sets the client information in the portable device-values object.</span></span>


```C++
if (SUCCEEDED(hr))
{
    // Attempt to set all bits of client information
    hr = (*ppClientInformation)->SetStringValue(WPD_CLIENT_NAME, CLIENT_NAME);
    if (FAILED(hr))
    {
        printf("! Failed to set WPD_CLIENT_NAME, hr = 0x%lx\n",hr);
    }

    hr = (*ppClientInformation)->SetUnsignedIntegerValue(WPD_CLIENT_MAJOR_VERSION, CLIENT_MAJOR_VER);
    if (FAILED(hr))
    {
        printf("! Failed to set WPD_CLIENT_MAJOR_VERSION, hr = 0x%lx\n",hr);
    }

    hr = (*ppClientInformation)->SetUnsignedIntegerValue(WPD_CLIENT_MINOR_VERSION, CLIENT_MINOR_VER);
    if (FAILED(hr))
    {
        printf("! Failed to set WPD_CLIENT_MINOR_VERSION, hr = 0x%lx\n",hr);
    }

    hr = (*ppClientInformation)->SetUnsignedIntegerValue(WPD_CLIENT_REVISION, CLIENT_REVISION);
    if (FAILED(hr))
    {
        printf("! Failed to set WPD_CLIENT_REVISION, hr = 0x%lx\n",hr);
    }

    //  Some device drivers need to impersonate the caller in order to function correctly.  Since our application does not
    //  need to restrict its identity, specify SECURITY_IMPERSONATION so that we work with all devices.
    hr = (*ppClientInformation)->SetUnsignedIntegerValue(WPD_CLIENT_SECURITY_QUALITY_OF_SERVICE, SECURITY_IMPERSONATION);
    if (FAILED(hr))
    {
        printf("! Failed to set WPD_CLIENT_SECURITY_QUALITY_OF_SERVICE, hr = 0x%lx\n",hr);
    }
}
else
{
    printf("! Failed to CoCreateInstance CLSID_PortableDeviceValues, hr = 0x%lx\n",hr);
}
```



## <a name="related-topics"></a><span data-ttu-id="16bce-111">相關主題</span><span class="sxs-lookup"><span data-stu-id="16bce-111">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="16bce-112">**IPortableDevice 介面**</span><span class="sxs-lookup"><span data-stu-id="16bce-112">**IPortableDevice Interface**</span></span>](/windows/desktop/api/PortableDeviceApi/nn-portabledeviceapi-iportabledevice)
</dt> <dt>

[<span data-ttu-id="16bce-113">**IPortableDeviceValues 介面**</span><span class="sxs-lookup"><span data-stu-id="16bce-113">**IPortableDeviceValues Interface**</span></span>](iportabledevicevalues.md)
</dt> <dt>

[<span data-ttu-id="16bce-114">**程式設計指南**</span><span class="sxs-lookup"><span data-stu-id="16bce-114">**Programming Guide**</span></span>](programming-guide.md)
</dt> </dl>

 

 



