---
description: 指出是否要連接到隱藏的網路。
ms.assetid: 31b859e9-adc7-49e2-91d9-4fb63a35addb
title: 非廣播 (SSIDConfig) 元素
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- nonBroadcast
api_type:
- Schema
api_location: ''
ms.openlocfilehash: 695bede631b19c028a55a2f3ca82ba994ca12ada
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/07/2021
ms.locfileid: "106977798"
---
# <a name="nonbroadcast-ssidconfig-element"></a>非廣播 (SSIDConfig) 元素

非廣播的 (SSIDConfig) 元素指出是否要連接到隱藏的網路。 如果網路未廣播其 SSID，則稱為隱藏的網路。 如果設定檔中設定了多個 Ssid，它們必須全都具有相同的非廣播值。

如果 [**connectionType**](wlan-profileschema-connectiontype-wlanprofile-element.md) 設定為 **ESS**，此值可以是 "true" 或 "false"。 如果這個元素不存在，則預設值為 "false"。

如果 [**connectionType**](wlan-profileschema-connectiontype-wlanprofile-element.md) 設定為 **IBSS**，則這個值必須是 "false"。 如果這個元素不存在，則預設值為 "false"。

Windows **xp （含 SP3）和適用于 WINDOWS XP SP2 的無線區域網路 API：** 不支援這個元素。

``` syntax
<xs:element name="nonBroadcast"
    type="boolean"
    minOccurs="0"
 />
```

元素是由 [**SSIDConfig**](wlan-profileschema-ssidconfig-wlanprofile-element.md) 元素所定義。

## <a name="examples"></a>範例

若要查看使用非 **廣播元素的** 範例設定檔，請參閱 [非廣播設定檔範例](non-broadcast-profile-sample.md)。

## <a name="requirements"></a>規格需求



| 需求 | 值 |
|-------------------------------------|------------------------------------------------------|
| 最低支援的用戶端<br/> | \[僅限 Windows Vista 桌面應用程式\]<br/>       |
| 最低支援的伺服器<br/> | 僅限 Windows Server 2008 \[ desktop 應用程式\]<br/> |



## <a name="see-also"></a>另請參閱

<dl> <dt>

**架構中的元素定義內容**
</dt> <dt>

[**SSIDConfig**](wlan-profileschema-ssidconfig-wlanprofile-element.md)
</dt> <dt>

**架構實例中可能的直屬父元素**
</dt> <dt>

[**SSIDConfig (WLANProfile)**](wlan-profileschema-ssidconfig-wlanprofile-element.md)
</dt> </dl>

 

 




