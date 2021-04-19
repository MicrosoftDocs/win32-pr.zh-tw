---
description: 本節說明 Windows 屬性系統介面。
ms.assetid: d81fe8df-9fd6-4ace-a47f-214cbba6f30c
title: '介面 (Windows 屬性系統) '
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 5003458683fb9b2443df0301676b601901817d54
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/08/2021
ms.locfileid: "106976919"
---
# <a name="interfaces-windows-property-system"></a>介面 (Windows 屬性系統) 

本節說明 Windows 屬性系統介面。



| 主題                                                                                        | 目錄                                                                                                                                                                                                                                                                                                                                                                                   |
|----------------------------------------------------------------------------------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [**IPropertyChange**](/windows/win32/api/propsys/nn-propsys-ipropertychange)                                                 | 公開封裝變更至單一屬性的方法。                                                                                                                                                                                                                                                                                                                          |
| [**IPropertyChangeArray**](/windows/win32/api/propsys/nn-propsys-ipropertychangearray)                                       | 公開數個可傳遞至 [**IFileOperation**](/windows/win32/api/shobjidl_core/nn-shobjidl_core-ifileoperation)之多個變更作業的方法。                                                                                                                                                                                                                                                                   |
| [**IPropertyDescription**](/windows/win32/api/propsys/nn-propsys-ipropertydescription)                                       | 公開列舉和取得個別屬性描述詳細資料的方法。                                                                                                                                                                                                                                                                                                       |
| [**IPropertyDescription2**](/windows/win32/api/propsys/nn-propsys-ipropertydescription2)                                     | 公開列舉和取得個別屬性描述詳細資料的方法。                                                                                                                                                                                                                                                                                                       |
| [**IPropertyDescriptionAliasInfo**](/windows/win32/api/propsys/nn-propsys-ipropertydescriptionaliasinfo)                     | 公開方法，以取得專案的「排序依據」資料行屬性。 此介面是由想要抓取指定屬性之主要或次要排序資料行的 UI 物件所使用。                                                                                                                                                                                                |
| [**IPropertyDescriptionList**](/windows/win32/api/propsys/nn-propsys-ipropertydescriptionlist)                               | 公開方法，這些方法會從呈現為清單的屬性描述集合中解壓縮資訊。                                                                                                                                                                                                                                                                                   |
| [**IPropertyDescriptionRelatedPropertyInfo**](/windows/win32/api/propsys/nn-propsys-ipropertydescriptionrelatedpropertyinfo) | 提供抓取 [**IPropertyDescription**](/windows/win32/api/propsys/nn-propsys-ipropertydescription) 介面的方法。                                                                                                                                                                                                                                                                                       |
| [**IPropertyDescriptionSearchInfo**](/windows/win32/api/propsys/nn-propsys-ipropertydescriptionsearchinfo)                   | 公開屬性的搜尋相關資訊。 這個介面所提供的資訊來自于指定屬性的 [propertyDescription](./propdesc-schema-propertydescription.md) 架構、 [searchInfo](./propdesc-schema-searchinfo.md) 元素。 Windows Search 索引子會使用這項資訊。 大部分呼叫的應用程式都不需要呼叫這個介面。 |
| [**IPropertyEnumType**](/windows/win32/api/propsys/nn-propsys-ipropertyenumtype)                                             | 公開從列舉資訊中提取資料的方法。 [**IPropertyEnumType**](/windows/win32/api/propsys/nn-propsys-ipropertyenumtype)可讓您以程式設計方式在執行時間存取 [屬性架構](./propdesc-schema-entry.md)中的 [enum](./propdesc-schema-enum.md)和 [enumRange](./propdesc-schema-enumrange.md)元素。                                                                 |
| [**IPropertyEnumType2**](/windows/win32/api/propsys/nn-propsys-ipropertyenumtype2)                                           | 公開從列舉資訊中提取資料的方法。 [**IPropertyEnumType2**](/windows/win32/api/propsys/nn-propsys-ipropertyenumtype2) 會擴充 [**IPropertyEnumType**](/windows/win32/api/propsys/nn-propsys-ipropertyenumtype)。                                                                                                                                                                                                               |
| [**IPropertyEnumTypeList**](/windows/win32/api/propsys/nn-propsys-ipropertyenumtypelist)                                     | 公開列舉屬性可能值的方法。                                                                                                                                                                                                                                                                                                                         |
| [**IPropertyStore**](/windows/win32/api/propsys/nn-propsys-ipropertystore)                                                   | 公開列舉、取得和設定屬性值的方法。                                                                                                                                                                                                                                                                                                                     |
| [**IPropertyStoreCache**](/windows/win32/api/propsys/nn-propsys-ipropertystorecache)                                         | 公開方法，可讓處理常式管理每個屬性的各種狀態。                                                                                                                                                                                                                                                                                                           |
| [**IPropertyStoreCapabilities**](/windows/win32/api/propsys/nn-propsys-ipropertystorecapabilities)                           | 公開方法，這個方法會判斷使用者是否可以在 UI 中編輯屬性。                                                                                                                                                                                                                                                                                                   |
| [**IPropertyStoreFactory**](/windows/win32/api/propsys/nn-propsys-ipropertystorefactory)                                     | 公開方法以取得 [**IPropertyStore**](/windows/win32/api/propsys/nn-propsys-ipropertystore) 物件。                                                                                                                                                                                                                                                                                                               |
| [**IPropertySystem**](/windows/win32/api/propsys/nn-propsys-ipropertysystem)                                                 | 公開取得屬性描述、註冊及取消註冊屬性架構、列舉屬性描述，以及以類型嚴格的方式格式化屬性值的方法。                                                                                                                                                                                                                |
| [**IPropertyUI**](/windows/win32/api/shobjidl_core/nn-shobjidl_core-ipropertyui)                                                         | 開發人員應該改用 [**IPropertyDescription**](/windows/win32/api/propsys/nn-propsys-ipropertydescription) 。                                                                                                                                                                                                                                                                                                      |



 

## <a name="related-topics"></a>相關主題

<dl> <dt>

[Windows 屬性](props.md)
</dt> <dt>

[屬性描述架構](property-description-schema.md)
</dt> <dt>

[屬性集](property-sets.md)
</dt> <dt>

[函數](functions.md)
</dt> <dt>

[結構](structures.md)
</dt> <dt>

[常數、列舉和旗標](constants--enumerations--and-flags.md)
</dt> </dl>

 

 
