---
description: 一旦應用程式具有指定裝置的裝置識別碼之後，就可以呼叫 IWiaDevMgr：： CreateDevice 或 IWiaDevMgr2：： CreateDevicemethod，它會建立 IWiaItem 或 IWiaItem2 物件的階層式樹狀結構，代表影像裝置和影像掃描張床，以及該裝置上所包含的資料夾。
ms.assetid: 807695c2-4c42-4318-9a5d-d34ac9014f0f
title: 建立裝置
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 2622d22a55c4273dcc13cc1421537b94037a3bb8
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/07/2021
ms.locfileid: "106989417"
---
# <a name="creating-a-device"></a><span data-ttu-id="00295-103">建立裝置</span><span class="sxs-lookup"><span data-stu-id="00295-103">Creating a Device</span></span>

<span data-ttu-id="00295-104">一旦應用程式具有指定裝置的裝置識別碼之後，就可以呼叫 [**IWiaDevMgr：： CreateDevice**](/windows/desktop/api/wia_xp/nf-wia_xp-iwiadevmgr-createdevice) 或 [**IWiaDevMgr2：： CreateDevice**](-wia-iwiadevmgr2-createdevice.md)方法，它會建立 [**IWiaItem**](/windows/desktop/api/wia_xp/nn-wia_xp-iwiaitem) 或 [**IWiaItem2**](-wia-iwiaitem2.md) 物件的階層式樹狀結構，代表影像裝置和影像掃描張床，以及該裝置上包含的資料夾。</span><span class="sxs-lookup"><span data-stu-id="00295-104">Once an application has the device ID of a given device, it can call the [**IWiaDevMgr::CreateDevice**](/windows/desktop/api/wia_xp/nf-wia_xp-iwiadevmgr-createdevice) or [**IWiaDevMgr2::CreateDevice**](-wia-iwiadevmgr2-createdevice.md)method, which creates a hierarchical tree of [**IWiaItem**](/windows/desktop/api/wia_xp/nn-wia_xp-iwiaitem) or [**IWiaItem2**](-wia-iwiaitem2.md) objects that represent an imaging device and the image scanning beds, and folders contained on that device.</span></span>

<span data-ttu-id="00295-105">下列來自範例應用程式 WiaSSamp 的範例會實作為參數接受裝置識別碼的函式。</span><span class="sxs-lookup"><span data-stu-id="00295-105">The following example from the sample application WiaSSamp implements a function that takes a device ID as a parameter.</span></span> <span data-ttu-id="00295-106">如需如何取得特定裝置之裝置識別碼的詳細資訊，請參閱 [讀取裝置屬性](-wia-reading-device-properties.md)。</span><span class="sxs-lookup"><span data-stu-id="00295-106">For information about how to obtain a device ID for a particular device, see [Reading Device Properties](-wia-reading-device-properties.md).</span></span>


```
    //XP or earlier:
    HRESULT CreateWiaDevice( IWiaDevMgr *pWiaDevMgr, BSTR bstrDeviceID, IWiaItem **ppWiaDevice ) 
    //Vista or later:
    HRESULT CreateWiaDevice( IWiaDevMgr2 *pWiaDevMgr, BSTR bstrDeviceID, IWiaItem2 **ppWiaDevice ) 
    {
        //
        // Validate arguments
        //
        if (NULL == pWiaDevMgr || NULL == bstrDeviceID || NULL == ppWiaDevice)
        {
            return E_INVALIDARG;
        }

        //
        // Initialize out variables
        //
        *ppWiaDevice = NULL;

        //
        // Create the WIA Device
        //
        HRESULT hr = pWiaDevMgr->CreateDevice( bstrDeviceID, ppWiaDevice );

        //
        // Return the result of creating the device
        //
        return hr;
    }
```



<span data-ttu-id="00295-107">在此範例中， **pWiaDevMgr** 是 [**IWiaDevMgr**](/windows/desktop/api/wia_xp/nn-wia_xp-iwiadevmgr) 或 [**IWiaDevMgr2**](-wia-iwiadevmgr2.md) 介面的指標，而 **PpWiaDevice** 是一個變數，在呼叫 [**IWiaDevMgr：： CreateDevice**](/windows/desktop/api/wia_xp/nf-wia_xp-iwiadevmgr-createdevice) (或 [**IWiaDevMgr2：： CreateDevice**](-wia-iwiadevmgr2-createdevice.md)) 之後，會包含代表新建立裝置之樹狀結構根項目的指標位址。</span><span class="sxs-lookup"><span data-stu-id="00295-107">In this example, **pWiaDevMgr** is a pointer to the [**IWiaDevMgr**](/windows/desktop/api/wia_xp/nn-wia_xp-iwiadevmgr) or [**IWiaDevMgr2**](-wia-iwiadevmgr2.md) interface, and **ppWiaDevice** is a variable that, after the call to [**IWiaDevMgr::CreateDevice**](/windows/desktop/api/wia_xp/nf-wia_xp-iwiadevmgr-createdevice) (or to [**IWiaDevMgr2::CreateDevice**](-wia-iwiadevmgr2-createdevice.md)), contains the address of a pointer to the root item of the tree that represents the newly created device.</span></span>

 

 



