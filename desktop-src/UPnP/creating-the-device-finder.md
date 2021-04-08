---
title: 建立裝置搜尋工具
description: 下列範例示範如何在 c + +、Visual Basic 和 VBScript 中建立裝置搜尋工具物件的實例。
ms.assetid: 0084a64d-458e-471c-a6be-aeb6ed0962d0
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: c3a12fc7e269f2c0ce5b577fe2f49b6d13fe3b5a
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 09/16/2019
ms.locfileid: "103840531"
---
# <a name="creating-the-device-finder"></a><span data-ttu-id="efd8c-103">建立裝置搜尋工具</span><span class="sxs-lookup"><span data-stu-id="efd8c-103">Creating the Device Finder</span></span>

<span data-ttu-id="efd8c-104">下列範例示範如何在 c + +、Visual Basic 和 VBScript 中建立裝置搜尋工具物件的實例。</span><span class="sxs-lookup"><span data-stu-id="efd8c-104">The following examples demonstrate how to create an instance of the Device Finder object in C++, Visual Basic, and VBScript.</span></span> <span data-ttu-id="efd8c-105">指令碼語言使用 (ProgID) [**UPnPDeviceFinder**](/windows/desktop/api/Upnp/nn-upnp-iupnpdevicefinder) 的程式設計識別碼來識別裝置搜尋工具類別。</span><span class="sxs-lookup"><span data-stu-id="efd8c-105">The script languages use the programmatic ID (ProgID) [**UPnP.UPnPDeviceFinder**](/windows/desktop/api/Upnp/nn-upnp-iupnpdevicefinder) to identify the Device Finder class.</span></span> <span data-ttu-id="efd8c-106">C + + 程式碼使用類別識別碼。</span><span class="sxs-lookup"><span data-stu-id="efd8c-106">The C++ code uses the class identifier.</span></span>

## <a name="c-example"></a><span data-ttu-id="efd8c-107">C + + 範例</span><span class="sxs-lookup"><span data-stu-id="efd8c-107">C++ Example</span></span>


```C++
HRESULT hr = S_OK;
IUPnPDeviceFinder *pDeviceFinder = NULL;

hr = CoCreateInstance(CLSID_UPnPDeviceFinder, 
                      NULL,
                      CLSCTX_INPROC_SERVER,
                      IID_IUPnPDeviceFinder,
                      (void **) &pDeviceFinder);
```



<span data-ttu-id="efd8c-108">如這個 c + + 範例所示，裝置搜尋工具物件會公開預設介面 [**IUPnPDeviceFinder**](/windows/desktop/api/Upnp/nn-upnp-iupnpdevicefinder)。</span><span class="sxs-lookup"><span data-stu-id="efd8c-108">As this C++ example indicates, the Device Finder object exposes a default interface, [**IUPnPDeviceFinder**](/windows/desktop/api/Upnp/nn-upnp-iupnpdevicefinder).</span></span> <span data-ttu-id="efd8c-109">這個介面的方法會根據以 UPnP 為基礎之裝置的有效搜尋準則來執行搜尋。</span><span class="sxs-lookup"><span data-stu-id="efd8c-109">The methods of this interface perform searches according to the valid search criteria for a UPnP-based device.</span></span> <span data-ttu-id="efd8c-110">這個介面具備自動化功能，因此可以透過腳本來呼叫其方法。</span><span class="sxs-lookup"><span data-stu-id="efd8c-110">This interface is Automation capable, so its methods can be called by scripting code.</span></span>

## <a name="vbscript-example"></a><span data-ttu-id="efd8c-111">VBScript 範例</span><span class="sxs-lookup"><span data-stu-id="efd8c-111">VBScript Example</span></span>


```VB
Dim deviceFinder

Set deviceFinder = CreateObject( "UPnP.UPnPDeviceFinder" )
```



 

 




