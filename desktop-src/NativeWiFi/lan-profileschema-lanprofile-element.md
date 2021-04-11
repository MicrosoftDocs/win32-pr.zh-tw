---
description: 包含有線網路設定檔。
ms.assetid: f5f9fcdc-febf-4730-8be4-5e1885d9ab08
title: LANProfile 元素
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- LANProfile
api_type:
- Schema
api_location: ''
ms.openlocfilehash: 58ad88c9f975455bdd2d77a0ef8ee028d9027d9f
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/08/2021
ms.locfileid: "104193670"
---
# <a name="lanprofile-element"></a>LANProfile 元素

LANProfile 元素包含有線網路設定檔。 此元素是有線網路設定檔的唯一根項目。

LANProfile 元素的目標命名空間為 `https://www.microsoft.com/networking/LAN/profile/v1` 。

``` syntax
<xs:element name="LANProfile">
    <xs:complexType>
        <xs:sequence>
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

## <a name="child-elements"></a>子元素



| 元素                                                                 | 類型    | Description                                                                                                                              |
|-------------------------------------------------------------------------|---------|------------------------------------------------------------------------------------------------------------------------------------------|
| [**MSM**](lan-profileschema-msm-lanprofile-element.md)                 |         | 包含特定媒體模組 (MSM) 設定。 <br/>                                                                               |
| [**OneXEnabled**](lan-profileschema-onexenabled-security-element.md)   | boolean | 指定有線網路的自動設定服務是否會嘗試使用 802.1 X 進行埠驗證。 <br/>      |
| [**OneXEnforced**](lan-profileschema-onexenforced-security-element.md) | boolean | 指定有線網路的自動設定服務是否需要使用 802.1 X 進行埠驗證。 <br/> |
| [**安全**](lan-profileschema-security-msm-element.md)              |         | 包含安全性設定。 <br/>                                                                                                  |



## <a name="remarks"></a>備註

若要查看樹狀結構中子專案的清單，請參閱 [LAN \_ 設定檔架構元素](lan-profileschema-elements.md)。

## <a name="requirements"></a>規格需求



| 需求 | 值 |
|-------------------------------------|------------------------------------------------------|
| 最低支援的用戶端<br/> | \[僅限 Windows Vista 桌面應用程式\]<br/>       |
| 最低支援的伺服器<br/> | 僅限 Windows Server 2008 \[ desktop 應用程式\]<br/> |



 

 




