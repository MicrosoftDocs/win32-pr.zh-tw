---
description: 依物件格式抓取多個物件的屬性
ms.assetid: c3f5edfd-8a6a-4bbd-9787-a4268c38f18f
title: 依物件格式抓取多個物件的屬性
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 0a352704b3ce5d063c544a41c467f372554bc901
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/08/2021
ms.locfileid: "104469316"
---
# <a name="retrieving-properties-for-multiple-objects-by-object-format"></a>依物件格式抓取多個物件的屬性

除了大量抓取物件識別碼集合的屬性之外，應用程式也可以針對特定類型的所有物件，執行屬性的大量抓取。 如先前的範例所示，針對特定類型進行大量抓取需要設備磁碟機支援大量檢索。

您的應用程式可以使用下表所述的介面來執行大量抓取。



| 介面                                                                                      | 描述                                                        |
|------------------------------------------------------------------------------------------------|--------------------------------------------------------------------|
| [**IPortableDeviceContent 介面**](/windows/desktop/api/portabledeviceapi/nn-portabledeviceapi-iportabledevicecontent)                             | 提供內容特定方法的存取權。                   |
| [**IPortableDeviceKeyCollection 介面**](iportabledevicekeycollection.md)                 | 用來識別要取出的屬性。                   |
| [**IPortableDeviceProperties 介面**](/windows/desktop/api/portabledeviceapi/nn-portabledeviceapi-iportabledeviceproperties)                       | 用來判斷指定的驅動程式是否支援大量作業。 |
| [**IPortableDevicePropertiesBulk 介面**](/windows/desktop/api/PortableDeviceApi/nn-portabledeviceapi-iportabledevicepropertiesbulk)               | 支援大量抓取作業。                             |
| [**IPortableDevicePropVariantCollection 介面**](iportabledevicepropvariantcollection.md) | 用來儲存大量作業的物件識別碼。       |



 

範例應用程式 ContentProperties .cpp 模組中的 ReadContentPropertiesBulkFilteringFormat 函式會示範特定類型或格式之物件的大量抓取作業。

在 ReadContentPropertiesBulkFilteringFormat 函式中找到的程式碼與在 ReadContentPropertiesBulk 函數中找到的程式碼幾乎完全相同。 如需此函式的完整描述， (參閱為 [多個物件取得屬性](retrieving-properties-for-multiple-objects.md) 。 ) 

當作業排入佇列時，會發生主要的差異。 依類型或格式篩選時，會呼叫 [**IPortableDevicePropertiesBulk：： QueueGetValuesByObjectFormat**](/windows/desktop/api/PortableDeviceApi/nf-portabledeviceapi-iportabledevicepropertiesbulk-queuegetvaluesbyobjectformat) 方法，而不是 [**IPortableDevicePropertiesBulk：： QueueGetValuesByObjectList**](/windows/desktop/api/PortableDeviceApi/nf-portabledeviceapi-iportabledevicepropertiesbulk-queuegetvaluesbyobjectlist) 方法。


```C++
hr = pPropertiesBulk->QueueGetValuesByObjectFormat(WPD_OBJECT_FORMAT_WMA,
                                                   WPD_DEVICE_OBJECT_ID,
                                                   100,
                                                   pPropertiesToRead,
                                                   pCallback,
                                                   &guidContext);
```



## <a name="related-topics"></a>相關主題

<dl> <dt>

[**IPortableDevice 介面**](/windows/desktop/api/PortableDeviceApi/nn-portabledeviceapi-iportabledevice)
</dt> <dt>

[**IPortableDeviceContent 介面**](/windows/desktop/api/portabledeviceapi/nn-portabledeviceapi-iportabledevicecontent)
</dt> <dt>

[**IPortableDeviceKeyCollection 介面**](iportabledevicekeycollection.md)
</dt> <dt>

[**IPortableDeviceProperties 介面**](/windows/desktop/api/portabledeviceapi/nn-portabledeviceapi-iportabledeviceproperties)
</dt> <dt>

[**IPortableDevicePropertiesBulk 介面**](/windows/desktop/api/PortableDeviceApi/nn-portabledeviceapi-iportabledevicepropertiesbulk)
</dt> <dt>

[**IPortableDevicePropVariantCollection 介面**](iportabledevicepropvariantcollection.md)
</dt> <dt>

[**程式設計指南**](programming-guide.md)
</dt> </dl>

 

 



