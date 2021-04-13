---
description: 指定任何使用者是否可以建立所有使用者設定檔。
ms.assetid: b9bdfe85-b9d5-4dcc-a7f8-05cce9702ec3
title: allowEveryoneToCreateAllUserProfiles (globalFlags) 元素
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- allowEveryoneToCreateAllUserProfiles
api_type:
- Schema
api_location: ''
ms.openlocfilehash: 63bc4c76ccecd8c7f774dc0e73621ef3f9b19877
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/07/2021
ms.locfileid: "104511184"
---
# <a name="alloweveryonetocreatealluserprofiles-globalflags-element"></a>allowEveryoneToCreateAllUserProfiles (globalFlags) 元素

**AllowEveryoneToCreateAllUserProfiles** (globalFlags) 元素會指定任何使用者是否可以建立所有使用者設定檔。 電腦上的任何使用者都可以使用所有使用者設定檔，以連線到與設定檔相關聯的無線網路。

如果 **allowEveryoneToCreateAllUserProfiles** 為 TRUE，則任何使用者都可以建立所有使用者設定檔。 如果 **allowEveryoneToCreateAllUserProfiles** 為 FALSE，則不是所有使用者都可以建立所有使用者設定檔，而且會有與 [wlan 安全新增 \_ \_ \_ \_ 所有使用者設定檔] 安全性物件相關聯的 DACL， \_ \_ 其中指定具有建立所有使用者設定檔許可權的使用者或使用者群組。 預設的 DACL 指定只有登入為 Administrators 群組成員的使用者可以建立所有使用者設定檔。 您可以藉由呼叫 [**WlanSetSecuritySettings**](/windows/desktop/api/wlanapi/nf-wlanapi-wlansetsecuritysettings)來變更預設安全性設定。 若要取得目前的安全性設定，請呼叫 [**WlanGetSecuritySettings**](/windows/desktop/api/wlanapi/nf-wlanapi-wlangetsecuritysettings)。

此為必要元素。 當設定檔由自動設定服務建立時，此元素的預設值會是 TRUE。

``` syntax
<xs:element name="allowEveryoneToCreateAllUserProfiles"
    type="boolean"
 />
```

**AllowEveryoneToCreateAllUserProfiles** 元素是由 [**globalFlags**](wlan-policyschema-globalflags-wlanpolicy-element.md)元素定義。

## <a name="requirements"></a>規格需求



| 需求 | 值 |
|-------------------------------------|------------------------------------------------------|
| 最低支援的用戶端<br/> | \[僅限 Windows Vista 桌面應用程式\]<br/>       |
| 最低支援的伺服器<br/> | 僅限 Windows Server 2008 \[ desktop 應用程式\]<br/> |



## <a name="see-also"></a>另請參閱

<dl> <dt>

**架構中的元素定義內容**
</dt> <dt>

[**globalFlags**](wlan-policyschema-globalflags-wlanpolicy-element.md)
</dt> <dt>

**架構實例中可能的直屬父元素**
</dt> <dt>

[**globalFlags (WLANPolicy)**](wlan-policyschema-globalflags-wlanpolicy-element.md)
</dt> </dl>

 

 




