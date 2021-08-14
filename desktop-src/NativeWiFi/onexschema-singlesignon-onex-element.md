---
description: 指定單一登入 (SSO) 網路設定資訊。
ms.assetid: c0a26f15-77fd-43e9-a6af-54e9b46f03fa
title: singleSignOn (OneX) 元素
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- singleSignOn
api_type:
- Schema
api_location: ''
ms.openlocfilehash: 5d0e002133366527624a0954df9054272cc08d894ba8dc3121b8a86b807caab6
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/11/2021
ms.locfileid: "117798029"
---
# <a name="singlesignon-onex-element"></a>singleSignOn (OneX) 元素

SingleSignOn (OneX) 元素會指定單一登入 (SSO) 網路設定資訊。

這是選擇性的項目。 如果網路不需要，請不要在設定檔中使用 singleSignOn 元素。

**Windows xp 搭配 SP3 和適用于 Windows XP SP2 的無線區域網路 API：** 如果設定檔中有此元素，將會予以忽略。

``` syntax
<xs:element name="singleSignOn">
    <xs:complexType>
        <xs:sequence>
            <xs:element name="type"
                minOccurs="1"
            >
                <xs:simpleType>
                    <xs:restriction
                        base="string"
                    >
                        <xs:enumeration
                            value="preLogon"
                         />
                        <xs:enumeration
                            value="postLogon"
                         />
                    </xs:restriction>
                </xs:simpleType>
            </xs:element>
            <xs:element name="maxDelay"
                minOccurs="0"
            >
                <xs:simpleType>
                    <xs:restriction
                        base="integer"
                    >
                        <xs:enumeration
                            value="0"
                         />
                        <xs:enumeration
                            value="120"
                         />
                    </xs:restriction>
                </xs:simpleType>
            </xs:element>
            <xs:element name="userBasedVirtualLan"
                type="boolean"
                minOccurs="0"
             />
        </xs:sequence>
    </xs:complexType>
</xs:element>
```

**SingleSignOn** 元素是由 [**OneX**](onexschema-onex-element.md)元素所定義。

## <a name="child-elements"></a>子元素



| 元素                                                                            | 類型    | Description                                                                                                                                                                                                                  |
|------------------------------------------------------------------------------------|---------|------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [**maxDelay**](onexschema-maxdelay-singlesignon-element.md)                       |         | 指定單一登入連線嘗試失敗之前的延遲上限（以秒為單位）。<br/>                                                                                                                      |
| [**類型**](onexschema-type-singlesignon-element.md)                               |         | 指定何時執行單一登入。 當設定為時 `preLogon` ，會在使用者登入之前執行單一登入。 當設定為時 `postLogon` ，會在使用者登入後立即執行單一登入。<br/> |
| [**userBasedVirtualLan**](onexschema-userbasedvirtuallan-singlesignon-element.md) | boolean | 指定裝置所使用的虛擬 LAN (VLAN) 是否會根據使用者的認證而變更。<br/>                                                                                                                   |



## <a name="remarks"></a>備註

您可以使用 **netsh wlan set profileparameter** 命令，在命令列設定這個參數。 如需詳細資訊，請參閱 [無線區域網路 (wlan) 的 Netsh 命令 ](/previous-versions/windows/it-pro/windows-server-2008-R2-and-2008/cc755301(v=ws.10))。

## <a name="requirements"></a>規格需求



| 需求 | 值 |
|-------------------------------------|------------------------------------------------------|
| 最低支援的用戶端<br/> | Windows\[僅限 Vista desktop 應用程式\]<br/>       |
| 最低支援的伺服器<br/> | Windows\[僅限 Server 2008 desktop 應用程式\]<br/> |



## <a name="see-also"></a>另請參閱

<dl> <dt>

**架構中的元素定義內容**
</dt> <dt>

[**OneX**](onexschema-onex-element.md)
</dt> <dt>

**架構實例中可能的直屬父元素**
</dt> <dt>

[**OneX**](onexschema-onex-element.md)
</dt> </dl>

 

 
