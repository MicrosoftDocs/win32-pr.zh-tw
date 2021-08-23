---
description: 一旦應用程式具有指定裝置的裝置識別碼之後，就可以呼叫 IWiaDevMgr：： CreateDevice 或 IWiaDevMgr2：： CreateDevicemethod，它會建立 IWiaItem 或 IWiaItem2 物件的階層式樹狀結構，代表影像裝置和影像掃描張床，以及該裝置上所包含的資料夾。
ms.assetid: 807695c2-4c42-4318-9a5d-d34ac9014f0f
title: 建立裝置
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 6319e493c6b99e1f23d8f4ccb9be1e10628fae45e8d4ba7df0aa8112be39dba6
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/11/2021
ms.locfileid: "118965897"
---
# <a name="creating-a-device"></a>建立裝置

一旦應用程式具有指定裝置的裝置識別碼之後，就可以呼叫 [**IWiaDevMgr：： CreateDevice**](/windows/desktop/api/wia_xp/nf-wia_xp-iwiadevmgr-createdevice) 或 [**IWiaDevMgr2：： CreateDevice**](-wia-iwiadevmgr2-createdevice.md)方法，它會建立 [**IWiaItem**](/windows/desktop/api/wia_xp/nn-wia_xp-iwiaitem) 或 [**IWiaItem2**](-wia-iwiaitem2.md) 物件的階層式樹狀結構，代表影像裝置和影像掃描張床，以及該裝置上包含的資料夾。

下列來自範例應用程式 WiaSSamp 的範例會實作為參數接受裝置識別碼的函式。 如需如何取得特定裝置之裝置識別碼的詳細資訊，請參閱 [讀取裝置屬性](-wia-reading-device-properties.md)。


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



在此範例中， **pWiaDevMgr** 是 [**IWiaDevMgr**](/windows/desktop/api/wia_xp/nn-wia_xp-iwiadevmgr) 或 [**IWiaDevMgr2**](-wia-iwiadevmgr2.md) 介面的指標，而 **PpWiaDevice** 是一個變數，在呼叫 [**IWiaDevMgr：： CreateDevice**](/windows/desktop/api/wia_xp/nf-wia_xp-iwiadevmgr-createdevice) (或 [**IWiaDevMgr2：： CreateDevice**](-wia-iwiadevmgr2-createdevice.md)) 之後，會包含代表新建立裝置之樹狀結構根項目的指標位址。

 

 



