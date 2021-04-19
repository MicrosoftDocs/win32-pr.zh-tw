---
description: View 類別中的每個屬性都必須有一個稱為 PropertySources 的字串陣列限定詞。
ms.assetid: df89680b-8ea7-4f38-81ba-c4132b944f37
ms.tgt_platform: multiple
title: PropertySources 辨識符號
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- PropertySources
api_type:
- NA
api_location: ''
ms.openlocfilehash: 3809977282a2bdf82d0b51ef8f566541b74fe28a
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/07/2021
ms.locfileid: "106979031"
---
# <a name="propertysources-qualifier"></a>PropertySources 辨識符號

View 類別中的每個屬性都必須有一個稱為 **PropertySources** 的字串陣列限定詞。 **PropertySources** 辨識符號包含來源類別屬性的名稱，或此 view 類別屬性從中取得資料的屬性。 這個陣列中的值順序會對應到針對 [ViewSources 限定詞](viewsources-qualifier.md)定義之來源類別的順序。 下列範例將示範如何定義 union view 類別的屬性，這是來自兩部不同電腦的 [**Win32 \_ LogicalDisk**](/windows/desktop/CIMWin32Prov/win32-logicaldisk) 類別聯集：


```mof
[PropertySources{"DeviceID", "DeviceID"},key] String Devname;
```



第一個 **DeviceID** 屬性會對應到第一個來源查詢中類別的 **deviceid** 屬性。 第二個 **DeviceID** 屬性是第二個來源查詢中類別的 **deviceid** 屬性。

定義聯結視圖類別的屬性時，您必須為每個來源類別屬性定義個別的 view 屬性，除非來源類別屬性是聯結視圖類別的基礎。 下列範例會在與 [**win32 \_ 印表機**](/windows/desktop/CIMWin32Prov/win32-printer) 來源類別和 [**win32 \_ PrinterConfiguration**](/windows/desktop/CIMWin32Prov/win32-printerconfiguration) 來源類別相似的屬性上，于聯結視圖類別中建立屬性：


```mof
[PropertySources{"VerticalResolution", ""}] Uint32 Vres;
[PropertySources{"", "YResolution"}] Uint32 Yres;
```



如果兩個來源類別是由通用屬性聯結，您只能定義單一 view 類別屬性，因為這兩個來源類別屬性的值一律相同。 下列範例示範如何透過通用屬性值加入 [**win32 \_ 印表機**](/windows/desktop/CIMWin32Prov/win32-printer) 類別和 [**win32 \_ PrinterConfiguration**](/windows/desktop/CIMWin32Prov/win32-printerconfiguration) ：


```mof
[PropertySources{"DeviceId", "DeviceName "}] String Name;
```



## <a name="requirements"></a>規格需求



| 需求 | 值 |
|-------------------------------------|--------------------------------|
| 最低支援的用戶端<br/> | Windows Vista<br/>       |
| 最低支援的伺服器<br/> | Windows Server 2008<br/> |



## <a name="see-also"></a>另請參閱

<dl> <dt>

[**視圖提供者專用的限定詞**](qualifiers-specific-to-the-view-provider.md)
</dt> </dl>

 

