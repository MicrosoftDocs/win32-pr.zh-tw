---
title: 同步搜尋
description: 裝置搜尋工具物件可啟用同步和非同步搜尋。 同步搜尋已完成，而且只有在找到所有可用的裝置之後，才會將控制權交還給呼叫的應用程式。
ms.assetid: fa22cd53-6468-4958-b4e3-b1a41b3cb2f6
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: c1890829dfe8386cd79627dde039264dc81e473c
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 09/16/2019
ms.locfileid: "106969870"
---
# <a name="synchronous-searching"></a><span data-ttu-id="f3034-104">同步搜尋</span><span class="sxs-lookup"><span data-stu-id="f3034-104">Synchronous Searching</span></span>

<span data-ttu-id="f3034-105">裝置搜尋工具物件可啟用同步和非同步搜尋。</span><span class="sxs-lookup"><span data-stu-id="f3034-105">The Device Finder object enables both synchronous and asynchronous searches.</span></span> <span data-ttu-id="f3034-106">同步搜尋已完成，而且只有在找到所有可用的裝置之後，才會將控制權交還給呼叫的應用程式。</span><span class="sxs-lookup"><span data-stu-id="f3034-106">Synchronous searches are completed and return control to the calling application only after all available devices are found.</span></span> <span data-ttu-id="f3034-107">若要執行同步搜尋，請使用 [**IUPnPDeviceFinder**](/windows/desktop/api/Upnp/nn-upnp-iupnpdevicefinder) 介面的其中一個同步搜尋方法。</span><span class="sxs-lookup"><span data-stu-id="f3034-107">To perform a synchronous search, use one of the synchronous search methods of the [**IUPnPDeviceFinder**](/windows/desktop/api/Upnp/nn-upnp-iupnpdevicefinder) interface.</span></span>

> [!Note]  
> <span data-ttu-id="f3034-108">同步搜尋至少需要九秒的時間才會返回。</span><span class="sxs-lookup"><span data-stu-id="f3034-108">Synchronous searches take at least nine seconds to return.</span></span> <span data-ttu-id="f3034-109">延遲的原因是因為必須多次傳送初始的 UDP 搜尋訊息。</span><span class="sxs-lookup"><span data-stu-id="f3034-109">The delay is caused because the initial UDP search message must be sent multiple times.</span></span> <span data-ttu-id="f3034-110">這是程度基礎網路通訊協定的重複帳戶。</span><span class="sxs-lookup"><span data-stu-id="f3034-110">This duplication accounts for the unreliability of the underlying network protocol.</span></span> <span data-ttu-id="f3034-111">同步搜尋最適合命令列介面。</span><span class="sxs-lookup"><span data-stu-id="f3034-111">Synchronous searches are best for command-line interfaces.</span></span> <span data-ttu-id="f3034-112">不建議針對圖形化使用者介面使用它們。</span><span class="sxs-lookup"><span data-stu-id="f3034-112">They are not recommended for graphical user interfaces.</span></span>

 

<span data-ttu-id="f3034-113">[**IUPnPDeviceFinder：： FindByType**](/windows/desktop/api/Upnp/nf-upnp-iupnpdevicefinder-findbytype)方法會依裝置或服務類型來搜尋。</span><span class="sxs-lookup"><span data-stu-id="f3034-113">The [**IUPnPDeviceFinder::FindByType**](/windows/desktop/api/Upnp/nf-upnp-iupnpdevicefinder-findbytype) method searches by device or service type.</span></span> <span data-ttu-id="f3034-114">這個方法會採用類型 URI 做為輸入參數，並傳回裝置物件的集合。</span><span class="sxs-lookup"><span data-stu-id="f3034-114">This method takes a type URI as an input parameter and returns a collection of Device objects.</span></span> <span data-ttu-id="f3034-115">裝置物件代表個別裝置。</span><span class="sxs-lookup"><span data-stu-id="f3034-115">A Device object represents an individual device.</span></span>

<span data-ttu-id="f3034-116">下列範例示範如何在 VBScript 中執行裝置的同步搜尋。</span><span class="sxs-lookup"><span data-stu-id="f3034-116">The following examples demonstrate how to perform a synchronous search for devices in VBScript.</span></span> <span data-ttu-id="f3034-117">每個腳本都會使用 [**IUPnPDeviceFinder：： FindByType**](/windows/desktop/api/Upnp/nf-upnp-iupnpdevicefinder-findbytype)，以 media player 裝置類型 (服務識別碼) 的類型 URI 進行呼叫， *urn：架構-upnp-org： device： mediaplayer. v 1.00.00*。</span><span class="sxs-lookup"><span data-stu-id="f3034-117">Each script uses [**IUPnPDeviceFinder::FindByType**](/windows/desktop/api/Upnp/nf-upnp-iupnpdevicefinder-findbytype), called with the type URI (service ID) for the media player device type, *urn:schemas-upnp-org:device:mediaplayer.v1.00.00*.</span></span> <span data-ttu-id="f3034-118">方法會傳回對應到所找到媒體播放機裝置的裝置物件集合。</span><span class="sxs-lookup"><span data-stu-id="f3034-118">The method returns a collection of Device objects that corresponds to media player devices that were found.</span></span> <span data-ttu-id="f3034-119">如需從集合解壓縮個別裝置物件的詳細資訊，請參閱 [同步搜尋所傳回的裝置集合](device-collections-returned-by-synchronous-searches.md)。</span><span class="sxs-lookup"><span data-stu-id="f3034-119">For information on extracting individual device objects from a collection, see [Device Collections Returned By Synchronous Searches](device-collections-returned-by-synchronous-searches.md).</span></span>

## <a name="search-for-devices-by-type-in-vbscript"></a><span data-ttu-id="f3034-120">在 VBScript 中依類型搜尋裝置</span><span class="sxs-lookup"><span data-stu-id="f3034-120">Search for Devices by Type in VBScript</span></span>


```VB
Dim deviceFinder

Set deviceFinder = CreateObject( "UPnP.UPnPDeviceFinder" )

Dim devices

Set devices = deviceFinder.FindByType( "urn:schemas-upnp-org:device:multidisk-dvd", 0 )
```



## <a name="search-for-device-by-type-in-c"></a><span data-ttu-id="f3034-121">在 c + + 中依類型搜尋裝置</span><span class="sxs-lookup"><span data-stu-id="f3034-121">Search for Device by Type in C++</span></span>

<span data-ttu-id="f3034-122">下列範例示範如何使用 c + + 進行媒體播放機裝置的同步搜尋。</span><span class="sxs-lookup"><span data-stu-id="f3034-122">The following example demonstrates a synchronous search for media player devices using C++.</span></span> <span data-ttu-id="f3034-123">函數會接受 [**IUPnPDeviceFinder**](/windows/desktop/api/Upnp/nn-upnp-iupnpdevicefinder) 介面的指標作為輸入，並傳回 [**IUPnPDevices**](/windows/desktop/api/Upnp/nn-upnp-iupnpdevices) 介面指標。</span><span class="sxs-lookup"><span data-stu-id="f3034-123">The function takes a pointer to the [**IUPnPDeviceFinder**](/windows/desktop/api/Upnp/nn-upnp-iupnpdevicefinder) interface as input, and returns the [**IUPnPDevices**](/windows/desktop/api/Upnp/nn-upnp-iupnpdevices) interface pointer.</span></span>

<span data-ttu-id="f3034-124">此範例會先配置一個 **BSTR** 來代表裝置類型 URI，然後將它傳遞給 [**IUPnPDeviceFinder：： FindByType**](/windows/desktop/api/Upnp/nf-upnp-iupnpdevicefinder-findbytype) 方法。</span><span class="sxs-lookup"><span data-stu-id="f3034-124">The example first allocates a **BSTR** to represent the device type URI and then passes this to the [**IUPnPDeviceFinder::FindByType**](/windows/desktop/api/Upnp/nf-upnp-iupnpdevicefinder-findbytype) method.</span></span> <span data-ttu-id="f3034-125">它也會將本機 [**IUPnPDevices**](/windows/desktop/api/Upnp/nn-upnp-iupnpdevices) 指標的位址傳遞到緩衝區中，方法接著會在該緩衝區中儲存找到的裝置集合。</span><span class="sxs-lookup"><span data-stu-id="f3034-125">It also passes the address of a local [**IUPnPDevices**](/windows/desktop/api/Upnp/nn-upnp-iupnpdevices) pointer in the buffer in which the method then stores the collection of devices found.</span></span> <span data-ttu-id="f3034-126">如果函式呼叫成功，則會將指標傳回至這個集合。</span><span class="sxs-lookup"><span data-stu-id="f3034-126">If the function call is successful, it returns the pointer to this collection.</span></span>


```C++
#include <windows.h>
#include <upnp.h>
#include <stdio.h>

#pragma comment(lib, "oleaut32.lib")

IUPnPDevices *FindMediaPlayerDevices(IUPnPDeviceFinder *pDeviceFinder)
{
    HRESULT         hr = S_OK;
    IUPnPDevices    * pFoundDevices = NULL;
    BSTR            bstrTypeURI = NULL;

    bstrTypeURI = 
        SysAllocString(L"urn:schemas-upnp-org:device:multidisk-dvd");

    if (bstrTypeURI)
    {
        hr = pDeviceFinder->FindByType(bstrTypeURI, 
                                       0,
                                       &pFoundDevices);

        if (SUCCEEDED(hr))
        {
            wprintf(L"FindMediaPlayerDevices(): "
                    L"Search returned successfully\n");
        }
        else
        {
            fwprintf(stderr, L"FindMediaPlayerDevices(): "
                     L"FindByType search failed - returned "
                     L"HRESULT 0x%x\n",
                     hr);
            pFoundDevices = NULL;
        }
        SysFreeString(bstrTypeURI);
    }
    else
    {
        fwprintf(stderr, L"FindMediaPlayerDevices(): "
                 L"Could not allocate BSTR for type URI\n");
    }

    return pFoundDevices;
}
```



 

 




