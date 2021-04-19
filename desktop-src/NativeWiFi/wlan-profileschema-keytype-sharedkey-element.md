---
description: 指出共用金鑰是否為網路金鑰或密碼片語。
ms.assetid: 2cc909bb-7de6-492b-81ca-ddde93c17f63
title: keyType (sharedKey) 元素
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- keyType
api_type:
- Schema
api_location: ''
ms.openlocfilehash: 134f9da4100c9479255507d4686dd19d3d484dea
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/08/2021
ms.locfileid: "106974704"
---
# <a name="keytype-sharedkey-element"></a>keyType (sharedKey) 元素

KeyType (sharedKey) 元素會指出共用金鑰是否為網路金鑰或密碼片語。

``` syntax
<xs:element name="keyType">
    <xs:simpleType>
        <xs:restriction
            base="string"
        >
            <xs:enumeration
                value="networkKey"
             />
            <xs:enumeration
                value="passPhrase"
             />
        </xs:restriction>
    </xs:simpleType>
</xs:element>
```

元素是由 [**sharedKey**](wlan-profileschema-sharedkey-security-element.md) 元素所定義。

## <a name="remarks"></a>備註

當 [**加密**](wlan-profileschema-encryption-authencryption-element.md) 元素的值為 WEP 時， **keyType** 必須設為 **networkKey**。

## <a name="examples"></a>範例

若要查看使用 **keyType** 元素的範例設定檔，請參閱 [非廣播設定檔範例](non-broadcast-profile-sample.md)、 [WPA-個人設定檔範例](wpa-personal-profile-sample.md)和 [WPA2 個人設定檔](wpa2-personal-profile-sample.md)範例。

## <a name="requirements"></a>規格需求



| 需求 | 值 |
|-------------------------------------|---------------------------------------------------------------------|
| 最低支援的用戶端<br/> | Windows Vista、Windows XP （僅含 SP3） \[ 桌面應用程式\]<br/> |
| 最低支援的伺服器<br/> | 僅限 Windows Server 2008 \[ desktop 應用程式\]<br/>                |
| 可轉散發套件<br/>          | 適用于 Windows XP SP2 的無線區域網路 API<br/>                 |



## <a name="see-also"></a>另請參閱

<dl> <dt>

**架構中的元素定義內容**
</dt> <dt>

[**sharedKey**](wlan-profileschema-sharedkey-security-element.md)
</dt> <dt>

**架構實例中可能的直屬父元素**
</dt> <dt>

[**sharedKey (安全性)**](wlan-profileschema-sharedkey-security-element.md)
</dt> </dl>

 

 




