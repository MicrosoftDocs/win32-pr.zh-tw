---
description: 包含有線網路的安全性設定。
ms.assetid: 08470cf4-3722-4cb9-9877-13eca2f7d04e
title: '安全性 (.MSM) 元素 (LAN_policy) '
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
ms.openlocfilehash: 8f66021f61536e8c8f09663e9ec2513b11d1ec87829f5c100b48cbf15d98cdd2
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/11/2021
ms.locfileid: "119685058"
---
# <a name="security-msm-element-lan_policy"></a>安全性 (.MSM) 元素 (LAN_policy) 

安全性 (.MSM) 元素包含有線網路的安全性設定。 這是選擇性的項目。

``` syntax
<xs:element name="security">
    <xs:complexType>
        <xs:sequence>
            <xs:element name="OneXEnforced"
                type="boolean"
             />
            <xs:element name="OneXEnabled"
                type="boolean"
             />
            <xs:any
                processContents="lax"
                minOccurs="0"
                maxOccurs="unbounded"
                namespace="##other"
             />
        </xs:sequence>
    </xs:complexType>
</xs:element>
```

**安全性** 元素是由 [**MSM**](lan-profileschema-msm-lanprofile-element.md)元素所定義。

## <a name="child-elements"></a>子元素



| 元素                                                                 | 類型    | 描述                                                                                                                              |
|-------------------------------------------------------------------------|---------|------------------------------------------------------------------------------------------------------------------------------------------|
| [**OneXEnabled**](lan-profileschema-onexenabled-security-element.md)   | boolean | 指定有線網路的自動設定服務是否會嘗試使用 802.1 X 進行埠驗證。 <br/>      |
| [**OneXEnforced**](lan-profileschema-onexenforced-security-element.md) | boolean | 指定有線網路的自動設定服務是否需要使用 802.1 X 進行埠驗證。 <br/> |



## <a name="requirements"></a>規格需求



| 需求 | 值 |
|-------------------------------------|------------------------------------------------------|
| 最低支援的用戶端<br/> | Windows\[僅限 Vista desktop 應用程式\]<br/>       |
| 最低支援的伺服器<br/> | Windows\[僅限 Server 2008 desktop 應用程式\]<br/> |



## <a name="see-also"></a>另請參閱

<dl> <dt>

**架構中的元素定義內容**
</dt> <dt>

[**MSM**](lan-profileschema-msm-lanprofile-element.md)
</dt> <dt>

**架構實例中可能的直屬父元素**
</dt> <dt>

[**MSM (LANProfile)**](lan-profileschema-msm-lanprofile-element.md)
</dt> </dl>

 

 




