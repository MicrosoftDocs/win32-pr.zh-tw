---
description: 用戶端介面
ms.assetid: fbe53f17-940a-485e-82b2-c11ae39b3300
title: 用戶端介面
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 6b44db8fdd42b20fb2ff7a3224bccf5214147069baa9187facdb1c832c375a59
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/11/2021
ms.locfileid: "119590390"
---
# <a name="client-interfaces"></a>用戶端介面

應用程式會使用下列介面所支援的方法，在可攜式裝置上執行作業。 這些作業包括開啟裝置的連線、從裝置中取出資料、將資料寫入至裝置等等。



| 介面                                                                              | 描述                                                                                                                                                                                                                         |
|----------------------------------------------------------------------------------------|-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [**IEnumPortableDeviceObjectIDs**](/windows/desktop/api/PortableDeviceApi/nn-portabledeviceapi-ienumportabledeviceobjectids)                   | 列舉可攜式裝置上的物件。                                                                                                                                                                                        |
| [**IPortableDevice**](/windows/desktop/api/PortableDeviceApi/nn-portabledeviceapi-iportabledevice)                                             | 提供對可攜式裝置的低層級存取。                                                                                                                                                                                     |
| [**IPortableDeviceCapabilities**](/windows/desktop/api/portabledeviceapi/nn-portabledeviceapi-iportabledevicecapabilities)                     | 抓取各種裝置功能，包括支援的格式、命令和功能物件。                                                                                                                          |
| [**IPortableDeviceContent**](/windows/desktop/api/portabledeviceapi/nn-portabledeviceapi-iportabledevicecontent)                               | 提供方法來建立、列舉和刪除裝置上的內容。                                                                                                                                                              |
| [**IPortableDeviceDataStream**](/windows/desktop/api/PortableDeviceApi/nn-portabledeviceapi-iportabledevicedatastream)                         | 公開用於資料傳輸的 **IStream** 上的其他方法。                                                                                                                                                               |
| [**IPortableDeviceEventCallback**](/windows/desktop/api/PortableDeviceApi/nn-portabledeviceapi-iportabledeviceeventcallback)                   | 由應用程式執行以接收非同步回呼。                                                                                                                                                                   |
| [**IPortableDeviceManager**](/windows/desktop/api/PortableDeviceApi/nn-portabledeviceapi-iportabledevicemanager)                               | 列舉已連線到電腦的裝置，並提供簡單的方法來要求裝置的安裝資訊 (包括製造商、易記名稱和描述) 。                                       |
| [**IPortableDeviceProperties**](/windows/desktop/api/portabledeviceapi/nn-portabledeviceapi-iportabledeviceproperties)                         | 在裝置上讀取和寫入物件的屬性。                                                                                                                                                                              |
| [**IPortableDevicePropertiesBulk**](/windows/desktop/api/PortableDeviceApi/nn-portabledeviceapi-iportabledevicepropertiesbulk)                 | 以非同步方式在裝置上讀取和寫入多個物件的多個屬性。                                                                                                                                               |
| [**IPortableDevicePropertiesBulkCallback**](/windows/desktop/api/PortableDeviceApi/nn-portabledeviceapi-iportabledevicepropertiesbulkcallback) | 由應用程式執行，以追蹤使用 **IPortableDevicePropertiesBulk** 介面開始之非同步作業的進度。                                                                          |
| [**IPortableDeviceResources**](/windows/desktop/api/PortableDeviceApi/nn-portabledeviceapi-iportabledeviceresources)                           | 提供物件資料的存取權。                                                                                                                                                                                                |
| [**IPortableDeviceService**](/windows/desktop/api/PortableDeviceAPI/nn-portabledeviceapi-iportabledeviceservice)                               | 僅 Windows 7。 提供可移植裝置服務的低層級存取。                                                                                                                                                             |
| [**IPortableDeviceServiceCapabilities**](/windows/desktop/api/portabledeviceapi/nn-portabledeviceapi-iportabledevicecapabilities)              | 僅 Windows 7。 抓取各種服務功能，包括支援的格式、命令、方法和轉譯設定檔。                                                                                                |
| [**IPortableDeviceServiceMethods**](/windows/desktop/api/PortableDeviceAPI/nn-portabledeviceapi-iportabledeviceservicemethods)                 | 僅 Windows 7。 以同步和非同步方式在服務上叫用方法。                                                                                                                                                      |
| [**IPortableDeviceServiceMethodCallback**](/windows/desktop/api/PortableDeviceAPI/nn-portabledeviceapi-iportabledeviceservicemethodcallback)   | 僅 Windows 7。 由應用程式所執行，藉由呼叫 [ **IPortableDeviceServiceMethods：： InvokeAsync** 來追蹤非同步服務方法作業的完成。](/windows/desktop/api/PortableDeviceAPI/nf-portabledeviceapi-iportabledeviceservicemethods-invokeasync) |
| [**IPortableDeviceServiceManager**](/windows/desktop/api/PortableDeviceAPI/nn-portabledeviceapi-iportabledeviceservicemanager)                 | 僅 Windows 7。 列舉裝置所支援的服務，並抓取與服務相關聯的裝置。                                                                                                             |



 

下圖顯示應用程式如何取得其所需的大部分介面。 並非所有介面的方法或應用程式所執行的介面都會顯示出來。

![顯示建立和抓取大部分必要用戶端介面的圖表](images/wpd-sdk-interface-diagram.gif)

## <a name="related-topics"></a>相關主題

<dl> <dt>

[**程式設計參考**](programming-reference.md)
</dt> </dl>

 

 



