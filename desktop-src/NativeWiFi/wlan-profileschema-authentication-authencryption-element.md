---
description: 指定要用來連接到無線區域網路的驗證方法。
ms.assetid: fb6c5cce-05d6-41a2-acf4-9ae2713079dd
title: 驗證 (authEncryption) 元素
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- authentication
api_type:
- Schema
api_location: ''
ms.openlocfilehash: 02895da685c78484c907af51745264abb81086da
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/07/2021
ms.locfileid: "104191739"
---
# <a name="authentication-authencryption-element"></a>驗證 (authEncryption) 元素

Authentication (authEncryption) 元素會指定要用來連線到無線區域網路的驗證方法。

``` syntax
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
```

元素是由 [**authEncryption**](wlan-profileschema-authencryption-security-element.md) 元素所定義。

## <a name="remarks"></a>備註

下表描述列舉值。



| 值   | 描述                            |
|---------|----------------------------------------|
| 開啟    | 開啟802.11 驗證。            |
| 共用  | 共用的802.11 驗證。          |
| WPA     | WPA-Enterprise 802.11 驗證。  |
| WPAPSK  | WPA-Personal 802.11 驗證。    |
| WPA2    | WPA2-Enterprise 802.11 驗證。 |
| WPA2PSK | WPA2-Personal 802.11 驗證。   |



 

如需802.11 驗證方法的詳細資訊，請參閱 [WPA](https://en.wikipedia.org/wiki/Wi-Fi_Protected_Access)、 [802.1 x](https://ieeexplore.ieee.org/document/1438730)和 [802.11 i](https://standards.ieee.org/findstds/standard/802.11i-2004.html) 規格。

## <a name="examples"></a>範例

若要查看使用 **驗證** 元素的範例設定檔，請參閱 [無線設定檔範例](wireless-profile-samples.md)。

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

[**authEncryption**](wlan-profileschema-authencryption-security-element.md)
</dt> <dt>

**架構實例中可能的直屬父元素**
</dt> <dt>

[**authEncryption (安全性)**](wlan-profileschema-authencryption-security-element.md)
</dt> </dl>

 

 




