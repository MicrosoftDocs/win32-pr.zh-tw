---
description: 包含共用金鑰資訊。
ms.assetid: 9f401441-256c-4702-9503-f87b2b9cf0ee
title: sharedKey (安全性) 元素
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- sharedKey
api_type:
- Schema
api_location: ''
ms.openlocfilehash: bfd138044e4849e5b0a42ab396561331bea9a338
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/08/2021
ms.locfileid: "106992050"
---
# <a name="sharedkey-security-element"></a>sharedKey (安全性) 元素

SharedKey (security) 元素包含共用金鑰資訊。 只有在驗證和加密配對需要 WEP 或 PSK 金鑰時，才需要這個元素。

``` syntax
<xs:element name="sharedKey"
    minOccurs="0"
>
    <xs:complexType>
        <xs:sequence>
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
            <xs:element name="protected"
                type="boolean"
             />
            <xs:element name="keyMaterial"
                type="string"
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



| 元素                                                                 | 類型                                                              | Description                                                                                                                                                                  |
|-------------------------------------------------------------------------|-------------------------------------------------------------------|------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [**keyMaterial**](wlan-profileschema-keymaterial-sharedkey-element.md) | [string](/dotnet/api/system.string)   | 包含網路金鑰或複雜密碼。<br/>                                                                                                                           |
| [**keyType**](wlan-profileschema-keytype-sharedkey-element.md)         |                                                                   | 索引鍵的類型。<br/>                                                                                                                                                      |
| [**受保護**](wlan-profileschema-protected-sharedkey-element.md)     | [boolean](/dotnet/api/system.boolean) | 指出金鑰是否已加密。<br/> Windows **xp （含 SP3）和適用于 WINDOWS XP SP2 的無線區域網路 API：** 這個元素的值必須為 FALSE。<br/> |



## <a name="remarks"></a>備註

若為 Windows Vista 和 Windows Server 2008，與 **sharedKey** 元素相關聯的資料會在儲存至設定檔存放區之前加密。

若為 windows XP （含 SP3）和 Windows XP （含 SP2）的無線區域網路 API，則不會加密資料。

## <a name="examples"></a>範例

若要查看使用 **sharedKey** 元素的範例設定檔，請參閱 [非廣播設定檔範例](non-broadcast-profile-sample.md)、 [WPA-個人設定檔範例](wpa-personal-profile-sample.md)和 [WPA2 個人設定檔](wpa2-personal-profile-sample.md)範例。

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

[**安全**](wlan-profileschema-security-msm-element.md)
</dt> <dt>

**架構實例中可能的直屬父元素**
</dt> <dt>

[**(MSM) 的安全性**](wlan-profileschema-security-msm-element.md)
</dt> </dl>

 

 
