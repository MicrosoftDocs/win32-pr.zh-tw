---
description: 指定要用於此設定檔的驗證和加密組。
ms.assetid: d7a69b82-3f04-49eb-80cc-675d5a0a559a
title: authEncryption (安全性) 元素
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- authEncryption
api_type:
- Schema
api_location: ''
ms.openlocfilehash: 03d132bf75a68154f7e2b7d2408b2be7564c7a67
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/07/2021
ms.locfileid: "106976783"
---
# <a name="authencryption-security-element"></a>authEncryption (安全性) 元素

AuthEncryption (security) 元素會指定要用於此設定檔的驗證和加密組。

``` syntax
<xs:element name="authEncryption">
    <xs:complexType>
        <xs:sequence>
            <xs:element name="authentication">
                <xs:simpleType>
                    <xs:restriction
                        base="string"
                    >
                        <xs:enumeration
                            value="open"
                         />
                        <xs:enumeration
                            value="shared"
                         />
                        <xs:enumeration
                            value="WPA"
                         />
                        <xs:enumeration
                            value="WPAPSK"
                         />
                        <xs:enumeration
                            value="WPA2"
                         />
                        <xs:enumeration
                            value="WPA2PSK"
                         />
                    </xs:restriction>
                </xs:simpleType>
            </xs:element>
            <xs:element name="encryption">
                <xs:simpleType>
                    <xs:restriction
                        base="string"
                    >
                        <xs:enumeration
                            value="none"
                         />
                        <xs:enumeration
                            value="WEP"
                         />
                        <xs:enumeration
                            value="TKIP"
                         />
                        <xs:enumeration
                            value="AES"
                         />
                    </xs:restriction>
                </xs:simpleType>
            </xs:element>
            <xs:element name="useOneX"
                type="boolean"
                minOccurs="0"
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

元素是由 [**安全性**](wlan-profileschema-security-msm-element.md) 元素所定義。

## <a name="child-elements"></a>子元素



| 元素                                                                            | 類型                                                              | Description                                                                                      |
|------------------------------------------------------------------------------------|-------------------------------------------------------------------|--------------------------------------------------------------------------------------------------|
| [**認證**](wlan-profileschema-authentication-authencryption-element.md) |                                                                   | 指定必須用來連接到無線區域網路的驗證方法。<br/> |
| [**加密**](wlan-profileschema-encryption-authencryption-element.md)         |                                                                   | 設定用來連接到無線區域網路的資料加密。<br/>                       |
| [**useOneX**](wlan-profileschema-useonex-authencryption-element.md)               | [boolean](/dotnet/api/system.boolean) | 指出是否使用 802.1 X。<br/>                                                     |



## <a name="remarks"></a>備註

[**FIPSMode**](wlan-profileschema-fipsmode-authencryption-element.md)元素可以插入做為 **authEncryption** 元素的子系。

## <a name="examples"></a>範例

若要查看使用 **authEncryption** 元素的範例設定檔，請參閱 [無線設定檔範例](wireless-profile-samples.md)。 若要查看使用 [**FIPSMode**](wlan-profileschema-fipsmode-authencryption-element.md) 元素的範例設定檔，請參閱 [FIPS 設定檔範例](fips-profile-sample.md)。

## <a name="requirements"></a>規格需求



| 需求 | 值 |
|-------------------------------------|---------------------------------------------------------------------|
| 最低支援的用戶端<br/> | Windows Vista、Windows XP （僅含 SP3） \[ 桌面應用程式\]<br/> |
| 最低支援的伺服器<br/> | 僅限 Windows Server 2008 \[ desktop 應用程式\]<br/>                |
| 可轉散發套件<br/>          | 適用于 Windows XP SP2 的無線區域網路 API<br/>                 |



## <a name="see-also"></a>另請參閱

<dl> <dt>

[無線設定檔範例](wireless-profile-samples.md)
</dt> <dt>

**架構中的元素定義內容**
</dt> <dt>

[**安全**](wlan-profileschema-security-msm-element.md)
</dt> <dt>

**架構實例中可能的直屬父元素**
</dt> <dt>

[**(MSM) 的安全性**](wlan-profileschema-security-msm-element.md)
</dt> </dl>

 

 
