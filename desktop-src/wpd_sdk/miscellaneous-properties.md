---
description: Windows可攜式裝置支援下列其他屬性。
ms.assetid: 0f2a5684-a94f-4a51-8f72-527204e4ebfa
title: '其他屬性 (PortableDevice .h) '
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Miscellaneous
api_type:
- HeaderDef
api_location:
- PortableDevice.h
ms.openlocfilehash: bdc093d877a180f6c7072ff9365e96edfe7d9e2c006fdcb745c58e92df3b179f
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/11/2021
ms.locfileid: "119704428"
---
# <a name="miscellaneous-properties"></a>其他屬性

Windows可攜式裝置支援下列其他屬性。



| 屬性                                       | VarType         | 描述                                                                                                                                                                                                                                                                                                                                                                                                                                                                                          |
|------------------------------------------------|-----------------|------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| **WPD \_ API \_ 選項 \_ 使用 \_ CLEAR \_ 資料流程 \_** | **VT \_ BOOL**    | 布林值，指定為數據傳輸建立的資料流程是否為明確的，也就是不包含 DRM。用戶端可以設定此選項，方法是將它加入至傳遞給 [**IPortableDeviceContent：： CreateObjectWithPropertiesAndData**](/windows/desktop/api/PortableDeviceApi/nf-portabledeviceapi-iportabledevicecontent-createobjectwithpropertiesanddata)的物件屬性。<br/>                                                                                                                                                   |
| **WPD \_ 服務 \_ 版本**                      | **VT \_ LPWSTR**  | 字串，指定指定之裝置服務的執行版本。                                                                                                                                                                                                                                                                                                                                                                                                                        |
| **\_允許 WPD 資料夾 \_ 內容 \_ 類型 \_**       | **VT \_ 不明** | 值，指定可以是此資料夾之直接子系的物件類型。 子資料夾可以有不同的功能。這個屬性是 [**IPortableDevicePropVariantCollection**](iportabledevicepropvariantcollection.md) ，其包含 \_ 指定允許物件類型的 VT CLSID 值。<br/> 如需 Windows 可攜式裝置所定義之物件類型的清單，請參閱[物件的需求](requirements-for-objects.md)。<br/>                                         |
| **WPD \_ 功能 \_ 物件 \_ 類別**          | **VT \_ CLSID**   | 值，指定物件的功能類別。                                                                                                                                                                                                                                                                                                                                                                                                                                             |
| **WPD \_ 轉譯 \_ 資訊 \_ 設定檔**      | **VT \_ 不明** | 保存多個 [**IPortableDeviceValues**](iportabledevicevalues.md)介面的 [**IPortableDeviceValuesCollection**](iportabledevicevaluescollection.md) ，其中每個介面都包含物件所支援之設定檔的屬性設定。                                                                                                                                                                                                                                            |
| **WPD \_ 物件 \_ 提示 \_ 位置 \_ 顯示 \_ 名稱** | **VT \_ LPWSTR**  | 如果物件是提示位置，這個屬性會指出要對使用者顯示的提示特定名稱，而不是物件名稱。驅動程式可以指定各種物件類型的位置提示。 這些是保留特定物件類型之資料夾的慣用儲存位置。 對等專案會是 Windows 中影像檔案的 [我的圖片] 資料夾。 如果這個屬性不存在，通常會改用 [WPD \_ 物件 \_ 名稱](object-properties.md) 。<br/> |



 

## <a name="requirements"></a>規格需求



| 需求 | 值 |
|-------------------|---------------------------------------------------------------------------------------------|
| 標頭<br/> | <dl> <dt>PortableDevice。h</dt> </dl> |



## <a name="see-also"></a>另請參閱

<dl> <dt>

[**WPD 屬性和屬性**](properties-and-attributes.md)
</dt> </dl>

 

 




