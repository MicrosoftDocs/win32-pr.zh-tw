---
description: 指出是否加密共用金鑰。
ms.assetid: 9206ef74-cd3e-4374-bea9-0c10505d10bf
title: protected (sharedKey) 元素
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- protected
api_type:
- Schema
api_location: ''
ms.openlocfilehash: 0b48ef0e07e5502ea8577904facc52f9f7e69838
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/07/2021
ms.locfileid: "106970792"
---
# <a name="protected-sharedkey-element"></a>protected (sharedKey) 元素

Protected (sharedKey) 元素會指出共用金鑰是否已加密。

``` syntax
<xs:element name="protected"
    type="boolean"
 />
```

元素是由 [**sharedKey**](wlan-profileschema-sharedkey-security-element.md) 元素所定義。

## <a name="remarks"></a>備註

若為 Windows Vista 和 Windows Server 2008，如果設定檔是從設定檔存放區取出 (例如，藉由呼叫 [**WlanGetProfile**](/windows/desktop/api/wlanapi/nf-wlanapi-wlangetprofile)) ，則 **受保護** 的永遠會有 TRUE 值。

適用于 Windows XP Service Pack 3 的設定檔 (SP3) 或適用于 Windows XP Service Pack 2 (SP2) 的無線區域網路 API， **受保護** 的值必須為 FALSE。

## <a name="examples"></a>範例

若要使用 **受保護** 的元素來查看範例設定檔，請參閱 [無線設定檔範例](wireless-profile-samples.md)。

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

 

 




