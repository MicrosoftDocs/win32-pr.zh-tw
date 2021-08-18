---
description: 下列範例會使用 Windows 映像取得 (wia) 1.0 IWiaDevMgr：： RegisterEventCallbackCLSID 方法，在任何 Windows 影像取得 (WIA) 裝置連線到系統時註冊通知。
ms.assetid: 1f2c7bc9-876a-4693-9439-52735e4b9d5f
title: 註冊事件
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: dc7a72614533ccc7c2f72bb4f2cf105107cc88ef8030cf306d31d6d9ffa5b4d5
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/11/2021
ms.locfileid: "118965547"
---
# <a name="registering-for-events"></a>註冊事件

下列範例會使用 Windows 映像取得 (wia) 1.0 [**IWiaDevMgr：： RegisterEventCallbackCLSID**](/windows/desktop/api/wia_xp/nf-wia_xp-iwiadevmgr-registereventcallbackclsid)方法，在任何 Windows 影像取得 (WIA) 裝置連線到系統時註冊通知。 應用程式也可以使用 WIA 1.0 [**IWiaDevMgr：： RegisterEventCallbackInterface**](/windows/desktop/api/wia_xp/nf-wia_xp-iwiadevmgr-registereventcallbackinterface) 和 Wia 1.0 [**IWiaDevMgr：： RegisterEventCallbackProgram**](/windows/desktop/api/wia_xp/nf-wia_xp-iwiadevmgr-registereventcallbackprogram) 來註冊事件。 使用 Windows Vista 和更新版本時，您可以使用 Windows 影像取得 (WIA) 2.0 [**IWiaDevMgr2：： RegisterEventCallbackCLSID**](-wia-iwiadevmgr2-registereventcallbackclsid.md)、 [**IWiaDevMgr2：： RegisterEventCallbackInterface**](-wia-iwiadevmgr2-registereventcallbackinterface.md)或 [**IWiaDevMgr2：： RegisterEventCallbackProgram**](-wia-iwiadevmgr2-registereventcallbackprogram.md)方法來註冊事件。

假設此範例取自已註冊為元件物件模型的應用程式， (COM) 跨進程伺服器物件。

[**IWiaDevMgr：： RegisterEventCallbackCLSID**](/windows/desktop/api/wia_xp/nf-wia_xp-iwiadevmgr-registereventcallbackclsid) (或 [**IWiaDevMgr2：： RegisterEventCallbackCLSID**](-wia-iwiadevmgr2-registereventcallbackclsid.md)) 的呼叫如下所示：


```
    pWiaDevMgr->RegisterEventCallbackCLSID( WIA_REGISTER_EVENT_CALLBACK,
                                            NULL,
                                            WIA_EVENT_DEVICE_CONNECTED,
                                            pCLSID,
                                            bstrName,
                                            bstrDescription,
                                            bstrIcon
                                            );
```



在先前的程式碼中， **pWiaDevMgr** 是 [**IWiaDevMgr**](/windows/desktop/api/wia_xp/nn-wia_xp-iwiadevmgr) (或 [**IWiaDevMgr2**](-wia-iwiadevmgr2.md)) 介面的有效指標，wia \_ 登錄 \_ 事件 \_ 回呼是一個常數，指定此呼叫要註冊事件，而不是針對事件取消註冊， \_ 則 wia 事件裝置已 \_ \_ 連線是一個常數，指定應用程式在裝置連線到使用者的電腦時，註冊要收到通知。 **pCLSID** 是應用程式已註冊之 CLSID 的指標， **bstrName** 是應用程式的名稱， **bstrDescription** 是應用程式的文字描述，而 **bstrIcon** 是要用於註冊事件之應用程式圖示的影像檔名稱。

然後，應用程式必須執行 [**IWiaEventCallback：： ImageEventCallback**](/windows/desktop/api/wia_xp/nf-wia_xp-iwiaeventcallback-imageeventcallback) 方法，該方法會在應用程式註冊的事件發生時呼叫。

應用程式可以使用 [**IWiaItem：： EnumRegisterEventInfo**](/windows/desktop/api/wia_xp/nf-wia_xp-iwiaitem-enumregistereventinfo) (或 [**IWiaItem2：：) EnumRegisterEventInfo**](-wia-iwiaitem2-enumregistereventinfo.md) 方法來列舉所註冊之事件的相關資訊。

 

 



