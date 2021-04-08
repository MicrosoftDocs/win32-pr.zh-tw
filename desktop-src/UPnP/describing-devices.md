---
title: 描述裝置
description: 有兩種方式可以取得裝置物件。
ms.assetid: a83fbf21-586e-4b92-9875-476d820c377d
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 5abc84f15f6b52328585e05abfd95503087124b5
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 09/16/2019
ms.locfileid: "103840528"
---
# <a name="describing-devices"></a><span data-ttu-id="5335c-103">描述裝置</span><span class="sxs-lookup"><span data-stu-id="5335c-103">Describing Devices</span></span>

<span data-ttu-id="5335c-104">有兩種方式可以取得裝置物件：</span><span class="sxs-lookup"><span data-stu-id="5335c-104">There are two ways to obtain device objects:</span></span>

-   <span data-ttu-id="5335c-105">使用 [**IUPnPDescriptionDocument**](/windows/desktop/api/Upnp/nn-upnp-iupnpdescriptiondocument) 介面。</span><span class="sxs-lookup"><span data-stu-id="5335c-105">Using the [**IUPnPDescriptionDocument**](/windows/desktop/api/Upnp/nn-upnp-iupnpdescriptiondocument) interface.</span></span> <span data-ttu-id="5335c-106">**IUPnPDescriptionDocument** 介面是唯一可安全編寫腳本的介面。</span><span class="sxs-lookup"><span data-stu-id="5335c-106">The **IUPnPDescriptionDocument** interface is the only interface that is safe for scripting.</span></span>
-   <span data-ttu-id="5335c-107">使用 [**IUPnPDeviceFinder**](/windows/desktop/api/Upnp/nn-upnp-iupnpdevicefinder) 介面取得 [**IUPnPDevices**](/windows/desktop/api/Upnp/nn-upnp-iupnpdevices) 介面。</span><span class="sxs-lookup"><span data-stu-id="5335c-107">Using the [**IUPnPDeviceFinder**](/windows/desktop/api/Upnp/nn-upnp-iupnpdevicefinder) interface to obtain an [**IUPnPDevices**](/windows/desktop/api/Upnp/nn-upnp-iupnpdevices) interface.</span></span>

<span data-ttu-id="5335c-108">這兩種方法都會傳回裝置集合。</span><span class="sxs-lookup"><span data-stu-id="5335c-108">Both methods return Devices collections.</span></span> <span data-ttu-id="5335c-109">然後，應用程式會使用裝置方法來取得裝置的相關屬性。</span><span class="sxs-lookup"><span data-stu-id="5335c-109">Applications then use the Device methods to retrieve properties about devices.</span></span>

<span data-ttu-id="5335c-110">應用程式能夠取得下列類型的資訊：</span><span class="sxs-lookup"><span data-stu-id="5335c-110">Applications are able to retrieve the following types of information:</span></span>

-   <span data-ttu-id="5335c-111">裝置階層資訊，包括根裝置、父裝置和子裝置。</span><span class="sxs-lookup"><span data-stu-id="5335c-111">Device hierarchy information, including root devices, parent devices, and child devices.</span></span>
-   <span data-ttu-id="5335c-112">裝置屬性，包括 UDNs、統一資源識別項 (Uri) 和使用者可讀取的名稱。</span><span class="sxs-lookup"><span data-stu-id="5335c-112">Device properties, including UDNs, uniform resource identifiers (URIs), and user-readable names.</span></span>
-   <span data-ttu-id="5335c-113">製造商資訊，包括名稱和相關的網頁。</span><span class="sxs-lookup"><span data-stu-id="5335c-113">Manufacturer information, including names and related Web pages.</span></span>
-   <span data-ttu-id="5335c-114">模型資訊，包括名稱、數位、UPC、序號和裝置描述。</span><span class="sxs-lookup"><span data-stu-id="5335c-114">Model information, including the name, number, UPC, serial numbers and device descriptions.</span></span>
-   <span data-ttu-id="5335c-115">顯示資訊，包括用來控制裝置的 URL，以及要從中下載圖示的 Url。</span><span class="sxs-lookup"><span data-stu-id="5335c-115">Display information, including the URL to control the device, and URLs from which icons are downloaded.</span></span>
-   <span data-ttu-id="5335c-116">特定裝置所提供的服務。</span><span class="sxs-lookup"><span data-stu-id="5335c-116">Services provided by a particular device.</span></span>

<span data-ttu-id="5335c-117">應用程式也會使用 [**IUPnPDeviceDocumentAccess**](/windows/desktop/api/Upnp/nn-upnp-iupnpdevicedocumentaccess) 介面取得裝置描述檔的 URL。</span><span class="sxs-lookup"><span data-stu-id="5335c-117">Applications also obtain the URL of the device description document using the [**IUPnPDeviceDocumentAccess**](/windows/desktop/api/Upnp/nn-upnp-iupnpdevicedocumentaccess) interface.</span></span> <span data-ttu-id="5335c-118">然後，應用程式會載入描述檔，並使用 [**IUPnPDevice**](/windows/desktop/api/Upnp/nn-upnp-iupnpdevice) 介面未公開的裝置和服務屬性。</span><span class="sxs-lookup"><span data-stu-id="5335c-118">The application then load the description document and work with device and service properties that are not exposed by the [**IUPnPDevice**](/windows/desktop/api/Upnp/nn-upnp-iupnpdevice) interface.</span></span> <span data-ttu-id="5335c-119">這個介面不能用在腳本中，因為它不是預設介面。</span><span class="sxs-lookup"><span data-stu-id="5335c-119">This interface cannot be used in scripting, because it is not the default interface.</span></span>

## <a name="visual-basic-example"></a><span data-ttu-id="5335c-120">Visual Basic 範例</span><span class="sxs-lookup"><span data-stu-id="5335c-120">Visual Basic Example</span></span>

<span data-ttu-id="5335c-121">下列範例程式碼顯示 [**IUPnPDeviceDocumentAccess：： GetDocumentURL**](/windows/desktop/api/Upnp/nf-upnp-iupnpdevicedocumentaccess-getdocumenturl)的使用方式。</span><span class="sxs-lookup"><span data-stu-id="5335c-121">The following sample code shows the usage of [**IUPnPDeviceDocumentAccess::GetDocumentURL**](/windows/desktop/api/Upnp/nf-upnp-iupnpdevicedocumentaccess-getdocumenturl).</span></span>


```VB
Sub GetDocumentURL()
Dim pDescDoc As IUPnPDeviceDocumentAccess
Dim strDescDocURL As String

'currentDevice is UPnPDevice object containing the current UPnP Device 
'We are trying to get IUPnPDeviceDocumentAccess interface in the UPnP Device object
Set pDescDoc = currentDevice

If Not (pDescDoc is Nothing) Then
  'Description Document URL is got from device
  strDescDocURL = pDescDoc.GetDocumentURL 
End If
```



## <a name="c-example"></a><span data-ttu-id="5335c-122">C + + 範例</span><span class="sxs-lookup"><span data-stu-id="5335c-122">C++ Example</span></span>

<span data-ttu-id="5335c-123">下列範例程式碼顯示 [**IUPnPDeviceDocumentAccess：： GetDocumentURL**](/windows/desktop/api/Upnp/nf-upnp-iupnpdevicedocumentaccess-getdocumenturl)的使用方式。</span><span class="sxs-lookup"><span data-stu-id="5335c-123">The following sample code shows the usage of [**IUPnPDeviceDocumentAccess::GetDocumentURL**](/windows/desktop/api/Upnp/nf-upnp-iupnpdevicedocumentaccess-getdocumenturl).</span></span>


```C++
#include <windows.h>
#include <upnp.h>
#include <stdio.h>

#pragma comment(lib, "ole32.lib")
#pragma comment(lib, "oleaut32.lib")

int GetDeviceDocumentUrl () 
{
  HRESULT hr = S_OK;
  // List of interfaces needed
  IUPnPDeviceFinder *pDevFinder=NULL;
  IUPnPDevice *pDevice =NULL;
  IUPnPDeviceDocumentAccess* pDeviceDocument=NULL;
  BSTR bstrDeviceUDN =NULL;
  BSTR bstrDeviceDocumentURL = NULL; 

  bstrDeviceUDN = SysAllocString(L"uuid:234324234324");
  if(bstrDeviceUDN == NULL){
    printf("ERROR: Could not allocate memory\n");
    return -1;
  }  

  //CoInitialize the program so that we can create COM objects
  CoInitializeEx(NULL, COINIT_MULTITHREADED);

  //now try to instantiate the DeviceFinder object
  hr = CoCreateInstance(  CLSID_UPnPDeviceFinder, 
              NULL,
              CLSCTX_INPROC_SERVER,
              IID_IUPnPDeviceFinder,
              (LPVOID *) &pDevFinder); 

  if(!SUCCEEDED(hr)){
    printf("\nERROR: CoCreateInstance on IUPnPDeviceFinder returned HRESULT %x",hr);
    goto cleanup;
  }

  printf("\nGot a pointer to the IUPnPDeviceFinder Interface");

  printf("\n Finding the device of given UDN\n");
  hr =pDevFinder->FindByUDN(bstrDeviceUDN, &pDevice);
  if(hr!=S_OK)
  {
    printf("\nERROR: FindByUDN for %S returned HRESULT %x", bstrDeviceUDN, hr);
    goto cleanup;
  }

  printf("\n\tFindByUDN for device of UDN %S succeeded", bstrDeviceUDN);
  //Now query pDevice for IUPnPDeviceDocumentAccess
  hr = pDevice->QueryInterface(IID_IUPnPDeviceDocumentAccess, (VOID **)&pDeviceDocument);
  if(SUCCEEDED(hr)){
    // We have got a pointer to the IUPnPDeviceDocumentAccess interface.
    // GetDocumentURL is available only in Windows XP. 
    hr = pDeviceDocument->GetDocumentURL(&bstrDeviceDocumentURL);
    if(SUCCEEDED(hr))
      printf("\nThe Device Document URL is %S \n", bstrDeviceDocumentURL);
  }
    
cleanup:
  //release references to all interfaces 
  if(pDevFinder)
    pDevFinder->Release();
  if(pDevice)
    pDevice->Release();
  if(pDeviceDocument)
    pDeviceDocument->Release();
  
  // Free the bstr strings
  if(bstrDeviceDocumentURL)
    SysFreeString(bstrDeviceDocumentURL);
  if(bstrDeviceUDN)
    SysFreeString(bstrDeviceUDN);
  CoUninitialize();
  return 0;
}
```



 

 




