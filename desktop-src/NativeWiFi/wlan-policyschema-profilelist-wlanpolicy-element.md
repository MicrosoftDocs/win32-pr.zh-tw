---
description: 包含要在網域或電腦層級套用的配置檔案清單。
ms.assetid: b78cb095-a1da-4b1b-91d3-c5085325be05
title: profileList (WLANPolicy) 元素
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- profileList
api_type:
- Schema
api_location: ''
ms.openlocfilehash: 9c11fbeb41b43faa31b170dcc856bb0823631001
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/08/2021
ms.locfileid: "106980487"
---
# <a name="profilelist-wlanpolicy-element"></a>profileList (WLANPolicy) 元素

ProfileList (WLANPolicy) 元素包含要在網域或電腦層級套用的配置檔案清單。 這是選擇性的項目。 如果這個元素存在，它必須包含至少一個設定檔。

設定檔應該以 [WLAN \_ 設定檔架構](wlan-profileschema-schema.md)為基礎，其根項目為 [**WLANProfile**](wlan-profileschema-wlanprofile-element.md)。

``` syntax
<xs:element name="profileList">
    <xs:complexType>
        <xs:sequence>
            <xs:any
                processContents="lax"
                maxOccurs="unbounded"
                namespace="##other"
             />
        </xs:sequence>
    </xs:complexType>
</xs:element>
```

**ProfileList** 元素是由 [**WLANPolicy**](wlan-policyschema-wlanpolicy-element.md)元素定義。

## <a name="requirements"></a>規格需求



| 需求 | 值 |
|-------------------------------------|------------------------------------------------------|
| 最低支援的用戶端<br/> | \[僅限 Windows Vista 桌面應用程式\]<br/>       |
| 最低支援的伺服器<br/> | 僅限 Windows Server 2008 \[ desktop 應用程式\]<br/> |



## <a name="see-also"></a>另請參閱

<dl> <dt>

**架構中的元素定義內容**
</dt> <dt>

[**WLANPolicy**](wlan-policyschema-wlanpolicy-element.md)
</dt> <dt>

**架構實例中可能的直屬父元素**
</dt> <dt>

[**WLANPolicy**](wlan-policyschema-wlanpolicy-element.md)
</dt> </dl>

 

 




