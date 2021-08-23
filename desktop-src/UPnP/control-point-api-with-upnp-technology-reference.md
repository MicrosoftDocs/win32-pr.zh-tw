---
title: 控制點 API 參考
description: 下列介面是具有 UPnP 技術之控制點 API 的一部分。 控制點 API 支援 microsoft Visual Basic 腳本版本 (VBScript) 、Microsoft Visual Basic 和 c + +。
ms.assetid: 6f73bf8c-0423-430f-a654-58d076712aae
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 24b3dab16874ebeb7b43ef1e8cf28def13d3ef1d7169a5aae4836b39da66636b
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/11/2021
ms.locfileid: "119058116"
---
# <a name="control-point-api-reference"></a>控制點 API 參考

下列介面是具有 UPnP 技術之控制點 API 的一部分。 控制點 API 支援 microsoft Visual Basic 腳本版本 (VBScript) 、Microsoft Visual Basic 和 c + +。



| 介面                                                                                      | 描述                                                                                                                                                                                                                    |
|------------------------------------------------------------------------------------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [**IUPnPAddressFamilyControl**](/windows/desktop/api/Upnp/nn-upnp-iupnpaddressfamilycontrol)                                 | 讓應用程式能夠存取裝置搜尋工具物件的位址家族旗標。                                                                                                                                          |
| [**IUPnPDescriptionDocument**](/windows/desktop/api/Upnp/nn-upnp-iupnpdescriptiondocument)                                   | 讓應用程式載入裝置描述。 這個介面可以安全地進行腳本處理。                                                                                                                                     |
| [**IUPnPDescriptionDocumentCallback**](/windows/desktop/api/Upnp/nn-upnp-iupnpdescriptiondocumentcallback)                   | 讓應用程式接收非同步載入作業的結果。                                                                                                                                               |
| [**IUPnPDevice**](/windows/desktop/api/Upnp/nn-upnp-iupnpdevice)                                                             | 讓應用程式取得特定裝置的相關資訊。                                                                                                                                                        |
| [**IUPnPDeviceDocumentAccess**](/windows/desktop/api/Upnp/nn-upnp-iupnpdevicedocumentaccess)                                 | 讓應用程式取得裝置描述檔的 URL。                                                                                                                                                     |
| [**IUPnPDeviceDocumentAccessEx**](/windows/desktop/api/Upnp/nn-upnp-iupnpdevicedocumentaccessex)                             | 提供方法，以取得特定裝置的整個 XML 裝置描述檔。                                                                                                                                  |
| [**IUPnPDeviceFinder**](/windows/desktop/api/Upnp/nn-upnp-iupnpdevicefinder)                                                 | 讓應用程式尋找裝置。                                                                                                                                                                                       |
| [**IUPnPDeviceFinderAddCallbackWithInterface**](/windows/desktop/api/Upnp/nn-upnp-iupnpdevicefinderaddcallbackwithinterface) | 讓應用程式能夠接收來自 UPnP 架構的非同步搜尋結果，以及裝置通告所透過的網路介面卡 GUID。                                                  |
| [**IUPnPDeviceFinderCallback**](/windows/desktop/api/Upnp/nn-upnp-iupnpdevicefindercallback)                                 | 讓應用程式能夠接收來自 UPnP 架構的非同步搜尋結果。                                                                                                                                         |
| [**IUPnPDevices**](/windows/desktop/api/Upnp/nn-upnp-iupnpdevices)                                                           | 列舉裝置的集合。                                                                                                                                                                                            |
| [**IUPnPHttpHeaderControl**](/windows/desktop/api/Upnp/nn-upnp-iupnphttpheadercontrol)                                       | 可讓應用程式從實 [**IUPnPDeviceFinder**](/windows/desktop/api/Upnp/nn-upnp-iupnpdevicefinder) 或 [**IUPnPDescriptionDocument**](/windows/desktop/api/Upnp/nn-upnp-iupnpdescriptiondocument) 介面的類別實例中，設定「使用者代理程式」 HTTP 標頭。 |
| [**IUPnPService**](/windows/desktop/api/Upnp/nn-upnp-iupnpservice)                                                           | 可讓應用程式取出服務的狀態資訊和叫用動作。                                                                                                                                         |
| [**IUPnPServiceAsync**](/windows/desktop/api/Upnp/nn-upnp-iupnpserviceasync)                                                 | 以非同步方式查詢狀態變數，並在服務實例上叫用動作。                                                                                                                                           |
| [**IUPnPServiceCallback**](/windows/desktop/api/Upnp/nn-upnp-iupnpservicecallback)                                           | 讓應用程式在事件發生時，接收來自 UPnP 架構的通知。                                                                                                                                      |
| [**IUPnPServices**](/windows/desktop/api/Upnp/nn-upnp-iupnpservices)                                                         | 列舉服務的集合。                                                                                                                                                                                           |



 

 

 




