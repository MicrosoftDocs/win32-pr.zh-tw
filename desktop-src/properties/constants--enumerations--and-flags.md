---
description: 本節說明 Windows 屬性系統常數、列舉和旗標。
ms.assetid: ff735b9c-e444-4e6f-8e80-0b2a5d770386
title: '常數、列舉和旗標 (Windows 屬性系統) '
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 24e39d357ae741ae49c4fa98c886e8c08b3594a2ea3a7e4e045def96abe8c2fd
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/11/2021
ms.locfileid: "119718207"
---
# <a name="constants-enumerations-and-flags"></a>常數、列舉和旗標

本節說明 Windows 屬性系統常數、列舉和旗標。



| 主題                                                                              | 目錄                                                                                                                                                                                                                                                                                                                                                                                   |
|------------------------------------------------------------------------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [**GETPROPERTYSTOREFLAGS**](/windows/desktop/api/Propsys/ne-propsys-getpropertystoreflags)                             | 指出旗標，這些旗標會修改建立屬性存放區的方法所抓取的屬性存放區物件，例如 [**IShellItem2：： GetPropertyStore**](/windows/win32/api/shobjidl_core/nf-shobjidl_core-ishellitem2-getpropertystore) 或 [**IPropertyStoreFactory：： GetPropertyStore**](/windows/win32/api/propsys/nf-propsys-ipropertystorefactory-getpropertystore)。<br/>                                                                                        |
| [**PDOPSTATUS**](/windows/win32/api/shobjidl_core/ne-shobjidl_core-pdopstatus)                                                 | 提供作業狀態旗標。<br/>                                                                                                                                                                                                                                                                                                                                                |
| [**PKA \_ 旗標**](/windows/win32/api/propsys/ne-propsys-pka_flags)                                                  | 描述屬性變更陣列行為。<br/>                                                                                                                                                                                                                                                                                                                                       |
| [**PROPDESC \_ 匯總 \_ 類型**](/windows/win32/api/propsys/ne-propsys-propdesc_aggregation_type)                 | 描述當選取多個專案時，如何顯示內容值。 針對特定的屬性，PROPDESC \_ 匯總 \_ 類型會描述當選取多個具有屬性值的專案時，應該如何顯示內容，例如值是否應該加總、平均，或只以預設的「多值」字串顯示。<br/> |
| [**PROPDESC \_ COLUMNINDEX \_ 類型**](/windows/win32/api/propsys/ne-propsys-propdesc_columnindex_type)                 | 指出是否可以編制屬性的索引。<br/>                                                                                                                                                                                                                                                                                                                             |
| [**PROPDESC \_ 條件 \_ 類型**](/windows/win32/api/propsys/ne-propsys-propdesc_condition_type)                     | 描述在 Windows Vista 的查詢產生器 UI 中顯示內容時所要使用的條件類型，但 Windows 7 和更新版本中則不會顯示。<br/>                                                                                                                                                                                                                                      |
| [**PROPDESC \_ ENUMFILTER**](/windows/win32/api/propsys/ne-propsys-propdesc_enumfilter)                              | 描述傳回之屬性描述的篩選清單。<br/>                                                                                                                                                                                                                                                                                                          |
| [**PROPDESC \_ 格式 \_ 旗標**](/windows/win32/api/propsys/ne-propsys-propdesc_format_flags)                         | 由屬性描述協助程式函數（例如 [**PSFormatForDisplay**](/windows/win32/api/propsys/nf-propsys-psformatfordisplay)）用來表示屬性字串的格式。<br/>                                                                                                                                                                                                                         |
| [**PROPDESC \_ RELATIVEDESCRIPTION \_ 類型**](/windows/win32/api/propsys/ne-propsys-propdesc_relativedescription_type) | 描述屬性描述的相對描述型別，由 [displayInfo](./propdesc-schema-displayinfo.md)元素的 *relativeDescriptionType* 屬性所決定。<br/>                                                                                                                                                                                   |
| [**PROPDESC \_ SEARCHINFO \_ 旗標**](/windows/win32/api/propsys/ne-propsys-propdesc_searchinfo_flags)                 | 決定是否要以 Windows Search 來編制屬性的索引。<br/>                                                                                                                                                                                                                                                                                                             |
| [**PROPDESC \_ 類型 \_ 旗標**](/windows/win32/api/propsys/ne-propsys-propdesc_type_flags)                             | 描述屬性 propdesc 檔中 [typeInfo](./propdesc-schema-typeinfo.md) 元素的屬性。<br/>                                                                                                                                                                                                                                                                |
| [**PROPDESC \_ 視圖 \_ 旗標**](/windows/win32/api/propsys/ne-propsys-propdesc_view_flags)                             | 這些旗標描述屬性描述清單字串中的屬性。<br/>                                                                                                                                                                                                                                                                                                           |
| [**PROPERTYUI \_ 旗標**](/windows/win32/api/shobjidl_core/ne-shobjidl_core-_propertyui_flags)                                    | 指定屬性功能。<br/>                                                                                                                                                                                                                                                                                                                                                    |
| [**PROPVAR \_ 比較 \_ 單位**](/windows/win32/api/propvarutil/ne-propvarutil-propvar_compare_unit)                           | 這些旗標會與特定的 [**PROPVARIANT**](/windows/win32/api/propidlbase/ns-propidlbase-propvariant) 結構比較相關聯。<br/>                                                                                                                                                                                                                                                                               |
| [**PSC \_ 州**](/windows/win32/api/propsys/ne-propsys-psc_state)                                                  | 指定屬性的狀態。 它們是由裝載記憶體中屬性存放區快取的程式碼手動設定。<br/>                                                                                                                                                                                                                                                        |



 

## <a name="related-topics"></a>相關主題

<dl> <dt>

[Windows 屬性](props.md)
</dt> <dt>

[屬性描述架構](property-description-schema.md)
</dt> <dt>

[屬性集](property-sets.md)
</dt> <dt>

[介面](interfaces.md)
</dt> <dt>

[函數](functions.md)
</dt> <dt>

[結構](structures.md)
</dt> </dl>

 

 
