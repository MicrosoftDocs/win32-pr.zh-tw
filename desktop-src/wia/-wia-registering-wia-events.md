---
description: 應用程式可以藉由呼叫下列其中一種 IWiaDevMgr 或 IWiaDevMgr2 介面方法，註冊以收到 Windows 映像取得 (WIA) 硬體裝置事件的通知： IWiaDevMgr：： RegisterEventCallbackCLSID 或 IWiaDevMgr2：： RegisterEventCallbackCLSIDIWiaDevMgr：： RegisterEventCallbackInterface 或 IWiaDevMgr2：： RegisterEventCallbackInterfaceIWiaDevMgr：： RegisterEventCallbackProgram 或 IWiaDevMgr2：： RegisterEventCallbackProgram
ms.assetid: 0c142083-835f-4bbd-ab32-eb6130f99c59
title: 註冊 WIA 事件
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: aa9fc36540a64211428579bc13b84902490ea103
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/07/2021
ms.locfileid: "103943460"
---
# <a name="registering-wia-events"></a>註冊 WIA 事件

應用程式可以藉由呼叫下列其中一種 [**IWiaDevMgr**](/windows/desktop/api/wia_xp/nn-wia_xp-iwiadevmgr) 或 [**IWiaDevMgr2**](-wia-iwiadevmgr2.md) 介面方法，註冊以收到 WINDOWS 映射取得 (WIA) 硬體裝置事件的通知：

-   [**IWiaDevMgr：： RegisterEventCallbackCLSID**](/windows/desktop/api/wia_xp/nf-wia_xp-iwiadevmgr-registereventcallbackclsid)或 [ **IWiaDevMgr2：： RegisterEventCallbackCLSID**](-wia-iwiadevmgr2-registereventcallbackclsid.md)
-   [**IWiaDevMgr：： RegisterEventCallbackInterface**](/windows/desktop/api/wia_xp/nf-wia_xp-iwiadevmgr-registereventcallbackinterface)或 [ **IWiaDevMgr2：： RegisterEventCallbackInterface**](-wia-iwiadevmgr2-registereventcallbackinterface.md)
-   [**IWiaDevMgr：： RegisterEventCallbackProgram**](/windows/desktop/api/wia_xp/nf-wia_xp-iwiadevmgr-registereventcallbackprogram)或 [ **IWiaDevMgr2：： RegisterEventCallbackProgram**](-wia-iwiadevmgr2-registereventcallbackprogram.md)

所有這些方法都採用參數來指定要通知其應用程式的事件和硬體裝置。 應用程式會針對指定硬體裝置的參數傳遞 **Null** 值，以註冊接收所有 WIA 裝置的事件。

如果應用程式在事件發生時執行， **RegisterEventCallbackInterface** 方法會註冊應用程式以接收 WIA 硬體裝置事件。 當應用程式註冊的事件發生時，WIA 會呼叫應用程式提供之物件的 [**IWiaEventCallback：： ImageEventCallback**](/windows/desktop/api/wia_xp/nf-wia_xp-iwiaeventcallback-imageeventcallback) 方法，以傳輸事件資訊。

**RegisterEventCallbackCLSID** 方法會註冊一個應用程式，該應用程式是註冊的元件物件模型， (COM) 元件來接收 WIA 硬體裝置事件，即使應用程式並未執行也一樣。 除了先前所述的參數之外，此方法還採用參數 *pClsID*，它會指定應用程式的類別識別碼。 當指定的事件發生時，WIA 系統會使用 [CoCreateInstance](/windows/win32/api/combaseapi/nf-combaseapi-cocreateinstance) 函數和 *pClsID* 指定的類別識別碼來建立應用程式的新實例，並呼叫該應用程式的 [**IWiaEventCallback：： ImageEventCallback**](/windows/desktop/api/wia_xp/nf-wia_xp-iwiaeventcallback-imageeventcallback) 方法，以傳輸事件資訊。

**RegisterEventCallbackProgram** 方法會註冊應用程式以接收 WIA 硬體裝置事件，即使在事件發生時應用程式並未執行也一樣。 應用程式不需要是已註冊的 COM 元件。 WIA 使用命令列語句啟動應用程式。 **RegisterEventCallbackProgram** 採用參數 *bstrCommandline*，指定可執行檔應用程式的完整路徑和檔案名。 **RegisterEventCallbackProgram** 存在的目的是為了與未針對 WIA 撰寫之應用程式的回溯相容性，因此應予以避免。 請改用 **RegisterEventCallbackInterface** 或 **RegisterEventCallbackCLSID** 。

為了判斷哪些處理常式是在特定的 WIA 裝置上註冊事件，應用程式會呼叫根專案的 [**IWiaItem：： EnumRegisterEventInfo**](/windows/desktop/api/wia_xp/nf-wia_xp-iwiaitem-enumregistereventinfo) 或 [**IWiaItem2：： EnumRegisterEventInfo**](-wia-iwiaitem2-enumregistereventinfo.md) 方法。 這個方法會建立註冊資訊的列舉物件。 然後，應用程式可以使用該物件的 [**IEnumWIA \_ DEV \_ CAPS**](/windows/desktop/api/wia_xp/nn-wia_xp-ienumwia_dev_caps) 介面，列舉已註冊要接收該裝置事件之處理常式的相關資訊。

如果透過 **RegisterEventCallbackInterface** 和 **RegisterEventCallbackCLSID** 或 **RegisterEventCallbackProgram** 註冊正在執行之應用程式的事件發生，則 WIA 會通知執行中的應用程式，而且不會嘗試啟動應用程式的新實例，因為透過 **RegisterEventCallbackInterface** 的事件註冊優先于 **RegisterEventCallbackCLSID** 和 **RegisterEventCallbackProgram**。

> [!Note]  
> 在多執行緒應用程式中，並不保證事件通知回呼回呼的執行緒是註冊回呼的相同執行緒。

 

 

 
