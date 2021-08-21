---
description: 指定要用來連接到無線區域網路的資料加密類型。
ms.assetid: 0ba24106-bd6f-465a-af80-ce85501756b9
title: " (authEncryption) 元素加密"
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- encryption
api_type:
- Schema
api_location: ''
ms.openlocfilehash: 2fe0d969892a82debe36951f34aa88343e50d9978b7522e3dd53f34b500a0571
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/11/2021
ms.locfileid: "117984438"
---
# <a name="encryption-authencryption-element"></a> (authEncryption) 元素加密

Encryption (authEncryption) 元素會指定要用來連線到無線區域網路的資料加密類型。

``` syntax
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
```

元素是由 [**authEncryption**](wlan-profileschema-authencryption-security-element.md) 元素所定義。

## <a name="remarks"></a>備註

當 **加密** 元素的值為 WEP 時， [**keyType**](wlan-profileschema-keytype-sharedkey-element.md) 必須設為 **networkKey**。

AES 加密方法如 [802.1 x](https://ieeexplore.ieee.org/document/1438730) 和 [802.11 i](https://standards.ieee.org/findstds/standard/802.11i-2004.html) 規格中所指定。

## <a name="examples"></a>範例

若要查看使用 **加密** 元素的範例設定檔，請參閱 [無線設定檔範例](wireless-profile-samples.md)。

## <a name="requirements"></a>規格需求



| 需求 | 值 |
|-------------------------------------|---------------------------------------------------------------------|
| 最低支援的用戶端<br/> | WindowsVista，Windows XP 只提供 SP3 \[ desktop 應用程式\]<br/> |
| 最低支援的伺服器<br/> | Windows\[僅限 Server 2008 desktop 應用程式\]<br/>                |
| 可轉散發套件<br/>          | 適用于 Windows XP SP2 的無線區域網路 API<br/>                 |



## <a name="see-also"></a>另請參閱

<dl> <dt>

**架構中的元素定義內容**
</dt> <dt>

[**authEncryption**](wlan-profileschema-authencryption-security-element.md)
</dt> <dt>

**架構實例中可能的直屬父元素**
</dt> <dt>

[**authEncryption (安全性)**](wlan-profileschema-authencryption-security-element.md)
</dt> </dl>

 

 




