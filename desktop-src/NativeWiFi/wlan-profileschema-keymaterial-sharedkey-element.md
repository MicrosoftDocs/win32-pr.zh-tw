---
description: 包含網路金鑰或複雜密碼。
ms.assetid: d2ed407e-5eaa-477b-8c4d-a47795048e0b
title: keyMaterial (sharedKey) 元素
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- keyMaterial
api_type:
- Schema
api_location: ''
ms.openlocfilehash: 59f3fc25fda5f4bf4221417636ac25ab7d0f9a15
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/08/2021
ms.locfileid: "104192965"
---
# <a name="keymaterial-sharedkey-element"></a>keyMaterial (sharedKey) 元素

KeyMaterial (sharedKey) 元素包含網路金鑰或複雜密碼。 如果 [**protected**](wlan-profileschema-protected-sharedkey-element.md) 專案的值為 TRUE，則此金鑰材料會加密;否則，就不會加密金鑰內容。 加密金鑰內容以十六進位形式表示。

``` syntax
<xs:element name="keyMaterial"
    type="string"
 />
```

元素是由 [**sharedKey**](wlan-profileschema-sharedkey-security-element.md) 元素所定義。

## <a name="remarks"></a>備註

KeyMaterial 元素的有效值範圍會依 [**驗證和**](wlan-profileschema-authentication-authencryption-element.md)[**加密**](wlan-profileschema-encryption-authencryption-element.md)元素所指定的驗證和加密類型而有所不同。 它也會因 [**keyType**](wlan-profileschema-keytype-sharedkey-element.md)而異。

下表顯示某些驗證和加密配對的有效 **keyMaterial** 值。



| [**驗證**](wlan-profileschema-authentication-authencryption-element.md) 值 | [**加密**](wlan-profileschema-encryption-authencryption-element.md) 值 | [**keyType**](wlan-profileschema-keytype-sharedkey-element.md) 值 | 有效的 **keyMaterial** 值                                                                                                                                                                   |
|------------------------------------------------------------------------------------------|----------------------------------------------------------------------------------|-----------------------------------------------------------------------|------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| 開啟或共用                                                                           | WEP                                                                              | networkKey                                                            | 此元素包含5或13個 ANSI 字元的 WEP 金鑰，或10或26個十六進位字元。                                                                                             |
| WPAPSK 或 WPA2PSK                                                                        | TKIP 或 AES                                                                      | passPhrase                                                            | 此元素包含8到 63 ASCII 字元的複雜密碼，也就是從32到126的8到 63 ANSI 字元。 索引鍵值必須符合 802.11 i 所指定的需求。 |
| WPAPSK 或 WPA2PSK                                                                        | TKIP 或 AES                                                                      | networkKey                                                            | 此元素包含64十六進位字元的索引鍵。                                                                                                                                      |



 

在上述指定 ANSI 或 ASCII 字元的情況下，可以輸入 Unicode 字元。 但是，如果提供的 Unicode 字元無法對應至 ANSI 或 ASCII 字元，則會拒絕所提供的金鑰內容。

[**WlanGetProfile**](/windows/desktop/api/wlanapi/nf-wlanapi-wlangetprofile)所傳回的金鑰內容一律會加密。 此外，如果將未加密的金鑰材料傳遞給 [**WlanSetProfile**](/windows/desktop/api/wlanapi/nf-wlanapi-wlansetprofile)，則金鑰內容會在儲存于設定檔存放區之前自動進行加密。

Windows **xp （含 SP3）和適用于 WINDOWS XP SP2 的無線區域網路 API：** 金鑰內容永遠不會加密。

如果您的進程在 LocalSystem 帳戶內容中執行，則您可以藉由呼叫 [**CryptUnprotectData**](/windows/win32/api/dpapi/nf-dpapi-cryptunprotectdata)來解密金鑰內容。

## <a name="examples"></a>範例

若要查看使用 **keyMaterial** 元素的範例設定檔，請參閱 [非廣播設定檔範例](non-broadcast-profile-sample.md)、 [WPA-個人設定檔範例](wpa-personal-profile-sample.md)和 [WPA2 個人設定檔](wpa2-personal-profile-sample.md)範例。

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

 

 
