---
description: 指定漫遊時慣用網路提供者的清單。
ms.assetid: 5873fcd7-8e89-4edd-8dc5-f43675919c55
title: DataRoamingPartners (MBNProfile) 元素
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- DataRoamingPartners
api_type:
- Schema
ms.openlocfilehash: 7f721abd608dd241c399f16eee90369ebcf19594
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/07/2021
ms.locfileid: "106970194"
---
# <a name="dataroamingpartners-mbnprofile-element"></a>DataRoamingPartners (MBNProfile) 元素

**DataRoamingPartners (MBNProfile)** 元素會指定漫遊時慣用網路提供者的清單。

行動寬頻服務會使用此元素來選取漫遊時所提供的慣用網路。

元素具有下列子項目，必須至少定義一次，但可以定義多次。

-   [**提供者**](schema-provider-dataroamingpartners-element.md)

此元素最多可有一次。

這是選擇性的項目。

``` syntax
<xs:element name="DataRoamingPartners">
    <xs:complexType>
        <xs:sequence>
            <xs:element name="Provider"
                type="providerType"
                maxOccurs="unbounded"
             />
        </xs:sequence>
    </xs:complexType>
</xs:element>
```

**DataRoamingPartners** 元素是由 [**MBNProfile**](schema-mbnprofile-element.md)元素定義。

## <a name="child-elements"></a>子元素



| 元素                                                         | 類型                                                    | Description                                            |
|-----------------------------------------------------------------|---------------------------------------------------------|--------------------------------------------------------|
| [**提供者**](schema-provider-dataroamingpartners-element.md) | [**providerType**](schema-providertype-complextype.md) | 行動電話通訊網路的名稱和提供者識別碼。<br/> |



## <a name="requirements"></a>規格需求



| 需求 | 值 |
|-------------------------------------|---------------------------------------------------|
| 最低支援的用戶端<br/> | Windows 7 \[ 桌面應用程式 \| UWP 應用程式\]<br/> |
| 最低支援的伺服器<br/> | 都不支援<br/>                         |



## <a name="see-also"></a>另請參閱

<dl> <dt>

**架構中的元素定義內容**
</dt> <dt>

[**MBNProfile**](schema-mbnprofile-element.md)
</dt> <dt>

**架構實例中可能的直屬父元素**
</dt> <dt>

[**MBNProfile**](schema-mbnprofile-element.md)
</dt> </dl>

 

 




