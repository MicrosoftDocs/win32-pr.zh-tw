---
description: Windows可攜式裝置支援下列屬性屬性。
ms.assetid: 129ee2b8-075c-457a-85ef-658a56eed541
title: '屬性屬性 (PortableDevice) '
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Property
api_type:
- HeaderDef
api_location:
- PortableDevice.h
ms.openlocfilehash: 85bf37b716349aae164594eeb8085e8c6df9dc5445728bbf7d9222705a9cb8c8
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/11/2021
ms.locfileid: "117843561"
---
# <a name="property-attributes-portabledeviceh"></a>屬性屬性 (PortableDevice) 

Windows可攜式裝置支援下列屬性屬性。 下列方法會傳回這些屬性：

-   [**IPortableDeviceCapabilities::GetFixedPropertyAttributes**](/windows/desktop/api/PortableDeviceApi/nf-portabledeviceapi-iportabledevicecapabilities-getfixedpropertyattributes)
-   [**IPortableDeviceProperties::GetPropertyAttributes**](/windows/desktop/api/PortableDeviceApi/nf-portabledeviceapi-iportabledeviceproperties-getpropertyattributes)
-   [**IPortableDeviceServiceCapabilities::GetFormatPropertyAttributes**](/windows/desktop/api/PortableDeviceAPI/nf-portabledeviceapi-iportabledeviceservicecapabilities-getformatpropertyattributes)



| 屬性                                           | VarType         | 描述                                                                                                                                                                                                                                                                                                                                                                                    |
|-----------------------------------------------------|-----------------|------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| **WPD \_ 屬性 \_ 屬性 \_ 可以 \_ 刪除**           | **VT \_ BOOL**    | 指定用戶端是否可以刪除屬性的布林值。 若要刪除屬性，請將其值設定為 VT \_ 空白。                                                                                                                                                                                                                                                                   |
| **WPD \_ 屬性 \_ 屬性 \_ 可以 \_ 讀取**             | **VT \_ BOOL**    | 布林值，指定用戶端是否可以讀取屬性。                                                                                                                                                                                                                                                                                                                       |
| **WPD \_ 屬性 \_ 屬性 \_ 可以 \_ 寫入**            | **VT \_ BOOL**    | 布林值，指定用戶端是否可以修改屬性。                                                                                                                                                                                                                                                                                                                     |
| **WPD \_ 屬性 \_ 屬性 \_ 預設 \_ 值**        | VT \_ *XXXX*      | 由裝置定義的值，這個值會指定屬性的預設值。 這僅適用于可寫入的屬性。                                                                                                                                                                                                                                                               |
| **WPD \_ 屬性 \_ 屬性 \_ 列舉 \_ 元素** | **VT \_ 不明** | [**IPortableDevicePropVariantCollection**](iportabledevicepropvariantcollection.md)介面，包含屬性值的集合，其 **WPD 屬性屬性（attribute） \_ \_ \_ 表單** 屬性（property）是 WPD 屬性（attribute） **\_ \_ \_ 表單 \_ 列舉**。 資料類型取決於正在查詢的屬性。                                                                              |
| **WPD \_ 屬性 \_ 屬性 \_ FAST \_ 屬性**        | **VT \_ BOOL**    | 若為 True，則表示此屬性屬於 *fast properties* 群組。 這些是可快速從裝置取出的屬性。                                                                                                                                                                                                                                                        |
| **WPD \_ 屬性 \_ 屬性 \_ 表單**                  | **VT \_ UI4**     | [**WpdAttributeForm**](wpdattributeform.md)列舉值，這個值會指定這個屬性所允許之有效值的形式。                                                                                                                                                                                                                                                         |
| **WPD \_ 屬性 \_ 屬性 \_ 名稱**                  | **VT \_ LPWSTR**  | 字串，指定屬性的腳本易記名稱。 有效字元為英數位元 \[ a-zA-Z0-9 \] 和 ' \_ '。                                                                                                                                                                                                                                                                    |
| **WPD \_ 屬性 \_ 屬性 \_ 範圍 \_ 最大值**            | VT \_ *XXXX*      | 屬性的最大值，其 **WPD \_ 屬性 \_ 屬性 \_** （attribute）屬性（attribute）屬性（attribute）屬性（attribute）是 **WPD \_ 屬性 \_ \_ \_** 資料類型可以是任何數數值型別。                                                                                                                                                                                                               |
| **WPD \_ 屬性 \_ 屬性 \_ 範圍 \_ 最小值**            | VT \_ *XXXX*      | 屬性的最小值，其 **WPD \_ 屬性 \_ 屬性 \_** （attribute）屬性（attribute）屬性（attribute）屬性（attribute）是 **WPD \_ 屬性 \_ \_ \_** 資料類型可以是任何數數值型別。                                                                                                                                                                                                               |
| **WPD \_ 屬性 \_ 屬性 \_ 範圍 \_ 步驟**           | VT \_ *XXXX*      | 屬性（attribute）的 **WPD \_ 屬性 \_ \_** （attribute）屬性（attribute）屬性（attribute）屬性（attribute **）屬性（ \_ \_ \_ \_** attribute）的 [ 此步驟會指定範圍屬性必須變更的程度。 例如，最小值為10、最大值為20，而步驟為5的屬性，可能會有下列值： **10**、 **15**、 **20**。 資料類型可以是任何數數值型別。 |
| **WPD \_ 屬性 \_ 屬性 \_ 正則 \_ 運算式**   | **VT \_ LPWSTR**  | 正則運算式字串，指定表單為 **WPD \_ 屬性屬性 \_ \_ 表單 \_ 正則 \_ 運算式** 之屬性的可接受值。                                                                                                                                                                                                                                             |
| **WPD \_ 屬性 \_ 屬性 \_ VARTYPE**               | **VT \_ UI4**     | 指定屬性 VARTYPE 的整數，例如 **VT \_ BOOL**。                                                                                                                                                                                                                                                                                                              |
| **WPD \_ 屬性 \_ 屬性 \_ \_ 大小上限**             | **VT \_ UI8**     | 值，指定此屬性值的大小上限（以位元組為單位）。                                                                                                                                                                                                                                                                                                              |



 

## <a name="requirements"></a>規格需求



| 需求 | 值 |
|-------------------|---------------------------------------------------------------------------------------------|
| 標頭<br/> | <dl> <dt>PortableDevice。h</dt> </dl> |



## <a name="see-also"></a>另請參閱

<dl> <dt>

[**屬性**](properties-and-attributes.md)
</dt> </dl>

 

 




