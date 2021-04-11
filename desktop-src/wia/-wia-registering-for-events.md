---
description: 下列範例會使用 Windows 映像取得 (WIA) 1.0 IWiaDevMgr：： RegisterEventCallbackCLSID 方法，在任何 Windows 映像取得 (WIA) 裝置連線到系統時註冊通知。
ms.assetid: 1f2c7bc9-876a-4693-9439-52735e4b9d5f
title: 註冊事件
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 40fe29be23bda4a3094ff8bcf90ae1ca677e858d
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/07/2021
ms.locfileid: "104113284"
---
# <a name="registering-for-events"></a><span data-ttu-id="3a9ee-103">註冊事件</span><span class="sxs-lookup"><span data-stu-id="3a9ee-103">Registering for Events</span></span>

<span data-ttu-id="3a9ee-104">下列範例會使用 Windows 映像取得 (WIA) 1.0 [**IWiaDevMgr：： RegisterEventCallbackCLSID**](/windows/desktop/api/wia_xp/nf-wia_xp-iwiadevmgr-registereventcallbackclsid) 方法，在任何 Windows 映像取得 (WIA) 裝置連線到系統時註冊通知。</span><span class="sxs-lookup"><span data-stu-id="3a9ee-104">The following example uses the Windows Image Acquisition (WIA) 1.0 [**IWiaDevMgr::RegisterEventCallbackCLSID**](/windows/desktop/api/wia_xp/nf-wia_xp-iwiadevmgr-registereventcallbackclsid) method to register for notification when any Windows Image Acquisition (WIA) device is connected to the system.</span></span> <span data-ttu-id="3a9ee-105">應用程式也可以使用 WIA 1.0 [**IWiaDevMgr：： RegisterEventCallbackInterface**](/windows/desktop/api/wia_xp/nf-wia_xp-iwiadevmgr-registereventcallbackinterface) 和 Wia 1.0 [**IWiaDevMgr：： RegisterEventCallbackProgram**](/windows/desktop/api/wia_xp/nf-wia_xp-iwiadevmgr-registereventcallbackprogram) 來註冊事件。</span><span class="sxs-lookup"><span data-stu-id="3a9ee-105">Applications can also use WIA 1.0 [**IWiaDevMgr::RegisterEventCallbackInterface**](/windows/desktop/api/wia_xp/nf-wia_xp-iwiadevmgr-registereventcallbackinterface) and WIA 1.0 [**IWiaDevMgr::RegisterEventCallbackProgram**](/windows/desktop/api/wia_xp/nf-wia_xp-iwiadevmgr-registereventcallbackprogram) to register for events.</span></span> <span data-ttu-id="3a9ee-106">使用 Windows Vista 和更新版本時，您可以使用 Windows 映像取得 (WIA) 2.0 [**IWiaDevMgr2：： RegisterEventCallbackCLSID**](-wia-iwiadevmgr2-registereventcallbackclsid.md)、 [**IWiaDevMgr2：： RegisterEventCallbackInterface**](-wia-iwiadevmgr2-registereventcallbackinterface.md)或 [**IWiaDevMgr2：： RegisterEventCallbackProgram**](-wia-iwiadevmgr2-registereventcallbackprogram.md) 方法來註冊事件。</span><span class="sxs-lookup"><span data-stu-id="3a9ee-106">With Windows Vista and later, you can use the Windows Image Acquisition (WIA) 2.0 [**IWiaDevMgr2::RegisterEventCallbackCLSID**](-wia-iwiadevmgr2-registereventcallbackclsid.md), [**IWiaDevMgr2::RegisterEventCallbackInterface**](-wia-iwiadevmgr2-registereventcallbackinterface.md), or [**IWiaDevMgr2::RegisterEventCallbackProgram**](-wia-iwiadevmgr2-registereventcallbackprogram.md) methods to register for events.</span></span>

<span data-ttu-id="3a9ee-107">假設此範例取自已註冊為元件物件模型的應用程式， (COM) 跨進程伺服器物件。</span><span class="sxs-lookup"><span data-stu-id="3a9ee-107">It is assumed that the example is taken from an application that is registered as a Component Object Model (COM) out-of-process server object.</span></span>

<span data-ttu-id="3a9ee-108">[**IWiaDevMgr：： RegisterEventCallbackCLSID**](/windows/desktop/api/wia_xp/nf-wia_xp-iwiadevmgr-registereventcallbackclsid) (或 [**IWiaDevMgr2：： RegisterEventCallbackCLSID**](-wia-iwiadevmgr2-registereventcallbackclsid.md)) 的呼叫如下所示：</span><span class="sxs-lookup"><span data-stu-id="3a9ee-108">The call to [**IWiaDevMgr::RegisterEventCallbackCLSID**](/windows/desktop/api/wia_xp/nf-wia_xp-iwiadevmgr-registereventcallbackclsid) (or [**IWiaDevMgr2::RegisterEventCallbackCLSID**](-wia-iwiadevmgr2-registereventcallbackclsid.md)) is as follows:</span></span>


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



<span data-ttu-id="3a9ee-109">在先前的程式碼中， **pWiaDevMgr** 是 [**IWiaDevMgr**](/windows/desktop/api/wia_xp/nn-wia_xp-iwiadevmgr) (或 [**IWiaDevMgr2**](-wia-iwiadevmgr2.md)) 介面的有效指標，wia \_ 登錄 \_ 事件 \_ 回呼是一個常數，指定此呼叫要註冊事件，而不是針對事件取消註冊， \_ 則 wia 事件裝置已 \_ \_ 連線是一個常數，指定應用程式在裝置連線到使用者的電腦時，註冊要收到通知。 **pCLSID** 是應用程式已註冊之 CLSID 的指標， **bstrName** 是應用程式的名稱， **bstrDescription** 是應用程式的文字描述，而 **bstrIcon** 是要用於註冊事件之應用程式圖示的影像檔名稱。</span><span class="sxs-lookup"><span data-stu-id="3a9ee-109">In the previous code, **pWiaDevMgr** is a valid pointer to the [**IWiaDevMgr**](/windows/desktop/api/wia_xp/nn-wia_xp-iwiadevmgr) (or [**IWiaDevMgr2**](-wia-iwiadevmgr2.md)) interface, WIA\_REGISTER\_EVENT\_CALLBACK is a constant that specifies that this call is to register for the event as opposed to unregistering for the event, WIA\_EVENT\_DEVICE\_CONNECTED is a constant that specifies that the application is registering to be notified whenever a device is connected to the user's computer, **pCLSID** is a pointer to the registered CLSID of the application, **bstrName** is the name of the application, **bstrDescription** is a text description of the application, and **bstrIcon** is the name of an image file to be used for the icon for the application registering for the event.</span></span>

<span data-ttu-id="3a9ee-110">然後，應用程式必須執行 [**IWiaEventCallback：： ImageEventCallback**](/windows/desktop/api/wia_xp/nf-wia_xp-iwiaeventcallback-imageeventcallback) 方法，該方法會在應用程式註冊的事件發生時呼叫。</span><span class="sxs-lookup"><span data-stu-id="3a9ee-110">The application must then implement the [**IWiaEventCallback::ImageEventCallback**](/windows/desktop/api/wia_xp/nf-wia_xp-iwiaeventcallback-imageeventcallback) method, which is called whenever an event occurs for which the application is registered.</span></span>

<span data-ttu-id="3a9ee-111">應用程式可以使用 [**IWiaItem：： EnumRegisterEventInfo**](/windows/desktop/api/wia_xp/nf-wia_xp-iwiaitem-enumregistereventinfo) (或 [**IWiaItem2：：) EnumRegisterEventInfo**](-wia-iwiaitem2-enumregistereventinfo.md) 方法來列舉所註冊之事件的相關資訊。</span><span class="sxs-lookup"><span data-stu-id="3a9ee-111">An application can use the [**IWiaItem::EnumRegisterEventInfo**](/windows/desktop/api/wia_xp/nf-wia_xp-iwiaitem-enumregistereventinfo) (or [**IWiaItem2::EnumRegisterEventInfo**](-wia-iwiaitem2-enumregistereventinfo.md)) method to enumerate the information about events for which it is registered.</span></span>

 

 



