---
description: 指出是否已啟用聯邦資訊處理標準 (FIPS) 模式。
ms.assetid: 4c62c96c-82e7-4174-b833-95ee10b29344
title: FIPSMode (authEncryption) 元素
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- FIPSMode
api_type:
- Schema
api_location: ''
ms.openlocfilehash: 62a60670622084e3179e9720022c68ad5909ab4c
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/07/2021
ms.locfileid: "103690828"
---
# <a name="fipsmode-authencryption-element"></a>FIPSMode (authEncryption) 元素

**FIPSMode** (authEncryption) 元素指出是否已啟用聯邦資訊處理標準 (FIPS) 模式。 當無線連線以 FIPS 模式運作時，連接的安全性層級會符合 FIPS 140-2 標準。 如需有關 FIPS 的詳細資訊，請參閱 [Fips 首頁](https://www.itl.nist.gov/fipspubs/)。

這是選擇性的項目。 如果設定檔中未指定此元素，則不會啟用 FIPS 模式。

只有在符合下列條件時， **FIPSMode** 才可以設定為 TRUE：

-   [**ConnectionType**](wlan-profileschema-connectiontype-wlanprofile-element.md)元素的值為 (， `ESS` 也就是連線是) 的基礎結構連接。
-   [**Authentication**](wlan-profileschema-authentication-authencryption-element.md)元素的值為 `WPA2` 或 `WPA2PSK` 。
-   [**加密**](wlan-profileschema-encryption-authencryption-element.md)元素的值為 `AES` 。

不同于 WLAN 設定檔架構中的大部分元素 \_ ，此元素位於 `https://www.microsoft.com/networking/WLAN/profile/v2` 命名空間中。

如果無線介面的微型埠驅動程式不支援 FIPS 模式， **FIPSMode** 元素的值會被忽略。

Windows **xp （含 SP3）和適用于 WINDOWS XP SP2 的無線區域網路 API：** 不支援這個元素。 如果設定檔中有 **FIPSMode** ，則會忽略元素。

``` syntax
<xs:element name="FIPSMode"
    type="boolean"
 />
```

元素是由 [**authEncryption**](wlan-profileschema-authencryption-security-element.md) 元素所定義。

## <a name="remarks"></a>備註

您可以使用 **netsh wlan set profileparameter** 命令，在命令列設定這個參數。 如需詳細資訊，請參閱 [無線區域網路 (wlan) 的 Netsh 命令 ](/previous-versions/windows/it-pro/windows-server-2008-R2-and-2008/cc755301(v=ws.10))。

## <a name="examples"></a>範例

若要查看使用 **FIPSMode** 元素的範例設定檔，請參閱 [FIPS 設定檔範例](fips-profile-sample.md)。

## <a name="requirements"></a>規格需求



| 需求 | 值 |
|-------------------------------------|------------------------------------------------------|
| 最低支援的用戶端<br/> | \[僅限 Windows Vista 桌面應用程式\]<br/>       |
| 最低支援的伺服器<br/> | 僅限 Windows Server 2008 \[ desktop 應用程式\]<br/> |



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

 

 
