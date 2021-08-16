---
description: 包含獨立硬體廠商所使用的各種安全性設定。
ms.assetid: 237c5d98-3f3c-4279-b2ad-b0d05df041f9
title: 安全性 (IHV) 元素
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- security
api_type:
- Schema
api_location: ''
ms.openlocfilehash: e4baeadc5e53dc53d0a526b62c4905da1a778a1015f58321ae8b96e4aa52dfcc
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/11/2021
ms.locfileid: "119912748"
---
# <a name="security-ihv-element"></a>安全性 (IHV) 元素

安全性 (IHV) 元素包含獨立硬體廠商所使用的各種安全性設定。

Microsoft 安全性設定和 IHV 安全性設定都是互斥的。 如果相同的設定檔中有這兩組安全性設定，則設定檔無效。

**Windows xp 搭配 SP3 和適用于 Windows XP SP2 的無線區域網路 API：** 不支援這個元素。

``` syntax
<xs:element name="security">
    <xs:complexType>
        <xs:sequence>
            <xs:any
                processContents="lax"
                namespace="##other"
             />
        </xs:sequence>
    </xs:complexType>
</xs:element>
```

**安全性** 元素是由 [**IHV**](wlan-profileschema-ihv-wlanprofile-element.md)元素所定義。

## <a name="requirements"></a>規格需求



| 需求 | 值 |
|-------------------------------------|------------------------------------------------------|
| 最低支援的用戶端<br/> | Windows\[僅限 Vista desktop 應用程式\]<br/>       |
| 最低支援的伺服器<br/> | Windows\[僅限 Server 2008 desktop 應用程式\]<br/> |



## <a name="see-also"></a>另請參閱

<dl> <dt>

**架構中的元素定義內容**
</dt> <dt>

[**IHV**](wlan-profileschema-ihv-wlanprofile-element.md)
</dt> <dt>

**架構實例中可能的直屬父元素**
</dt> <dt>

[**IHV (WLANProfile)**](wlan-profileschema-ihv-wlanprofile-element.md)
</dt> </dl>

 

 




