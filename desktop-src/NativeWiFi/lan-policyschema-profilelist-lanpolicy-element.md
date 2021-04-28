---
description: profileList (LANPolicy) 元素-包含要在網域或電腦層級套用的配置檔案清單。
ms.assetid: 4f010449-0c6b-4a01-8253-4f82cd628f0a
title: profileList (LANPolicy) 元素
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
ms.openlocfilehash: 5d18ebc99f48bf72599afe750863d684b8158608
ms.sourcegitcommit: 95685061d5b0333bbf9e6ebd208dde8190f97005
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 04/28/2021
ms.locfileid: "108090776"
---
# <a name="profilelist-lanpolicy-element"></a>profileList (LANPolicy) 元素

ProfileList (LANPolicy) 元素包含要在網域或電腦層級套用的配置檔案清單。 設定檔必須以 [LAN \_ 設定檔架構](lan-profileschema-schema.md)為基礎，並以 [**LANProfile**](lan-profileschema-lanprofile-element.md)的根項目為基礎。 將會忽略以任何其他架構為基礎的設定檔。

當 [**enableAutoConfig**](lan-policyschema-enableautoconfig-globalflags-element.md) 設定為 FALSE 時，此元素不能出現在 LAN 原則設定檔中。 當 **enableAutoConfig** 設定為 TRUE 時，則需要這個元素。

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

**ProfileList** 元素是由 [**LANPolicy**](lan-policyschema-lanpolicy-element.md)元素定義。

## <a name="remarks"></a>備註

此元素只可包含一個網路設定檔。 如果在原則中指定一個以上的設定檔，則只會套用第一個網路。

## <a name="requirements"></a>規格需求



| 需求 | 值 |
|-------------------------------------|------------------------------------------------------|
| 最低支援的用戶端<br/> | \[僅限 Windows Vista 桌面應用程式\]<br/>       |
| 最低支援的伺服器<br/> | 僅限 Windows Server 2008 \[ desktop 應用程式\]<br/> |



## <a name="see-also"></a>另請參閱

<dl> <dt>

**架構中的元素定義內容**
</dt> <dt>

[**LANPolicy**](lan-policyschema-lanpolicy-element.md)
</dt> <dt>

**架構實例中可能的直屬父元素**
</dt> <dt>

[**LANPolicy**](lan-policyschema-lanpolicy-element.md)
</dt> </dl>

 

 




