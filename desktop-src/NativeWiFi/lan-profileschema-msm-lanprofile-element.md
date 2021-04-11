---
description: 包含特定媒體模組 (MSM) 設定。
ms.assetid: fe858701-e0eb-4817-b3c2-ae61e96a4cbe
title: MSM (LANProfile) 元素
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- MSM
api_type:
- Schema
api_location: ''
ms.openlocfilehash: e9e58895ae36a304e713ecdb21b4008a2027e8c8
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/08/2021
ms.locfileid: "104193668"
---
# <a name="msm-lanprofile-element"></a>MSM (LANProfile) 元素

MSM (LANProfile) 元素包含媒體專屬模組 (MSM) 設定。

``` syntax
<xs:element name="MSM">
    <xs:complexType>
        <xs:sequence>
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

**MSM** 元素是由 [**LANProfile**](lan-profileschema-lanprofile-element.md)元素定義。

## <a name="child-elements"></a>子元素



| 元素                                                                 | 類型    | Description                                                                                                                              |
|-------------------------------------------------------------------------|---------|------------------------------------------------------------------------------------------------------------------------------------------|
| [**OneXEnabled**](lan-profileschema-onexenabled-security-element.md)   | boolean | 指定有線網路的自動設定服務是否會嘗試使用 802.1 X 進行埠驗證。<br/>       |
| [**OneXEnforced**](lan-profileschema-onexenforced-security-element.md) | boolean | 指定有線網路的自動設定服務是否需要使用 802.1 X 進行埠驗證。 <br/> |
| [**安全**](lan-profileschema-security-msm-element.md)              |         | 包含安全性設定。 <br/>                                                                                                  |



## <a name="requirements"></a>規格需求



| 需求 | 值 |
|-------------------------------------|------------------------------------------------------|
| 最低支援的用戶端<br/> | \[僅限 Windows Vista 桌面應用程式\]<br/>       |
| 最低支援的伺服器<br/> | 僅限 Windows Server 2008 \[ desktop 應用程式\]<br/> |



## <a name="see-also"></a>另請參閱

<dl> <dt>

**架構中的元素定義內容**
</dt> <dt>

[**LANProfile**](lan-profileschema-lanprofile-element.md)
</dt> <dt>

**架構實例中可能的直屬父元素**
</dt> <dt>

[**LANProfile**](lan-profileschema-lanprofile-element.md)
</dt> </dl>

 

 




