---
description: 決定當更慣用的網路在範圍內時，自動連線網路的漫遊行為。
ms.assetid: 095dc797-1249-43aa-a8b7-5fa6eaee2a74
title: autoSwitch (WLANProfile) 元素
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- autoSwitch
api_type:
- Schema
api_location: ''
ms.openlocfilehash: 7ae05b18f58927e05c952edbbfc1b6a6190cec19
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/07/2021
ms.locfileid: "103848405"
---
# <a name="autoswitch-wlanprofile-element"></a>autoSwitch (WLANProfile) 元素

當較慣用的網路在範圍內時，autoSwitch (WLANProfile) 元素會決定自動連線網路的漫遊行為。 . 這是選擇性的項目。

如果 autoSwitch 是 "true"，而 [**connectionMode**](wlan-profileschema-connectionmode-wlanprofile-element.md) 設定為 "auto"，則當更慣用的網路進入範圍時，就必須嘗試連線到更慣用的網路。 慣用的無線網路清單中會有較高優先順序的網路。 連線到另一個網路時，會發生此連接嘗試。

如果 [**connectionMode**](wlan-profileschema-connectionmode-wlanprofile-element.md) 設定為 "auto"，此值可以是 "true" 或 "false"。

如果 [**connectionMode**](wlan-profileschema-connectionmode-wlanprofile-element.md) 設定為 "manual"，此值必須設定為 "false"。 此元素不會影響手動連接的網路。

設定為 "true" 的 autoSwitch 值會導致較高頻率的新網路定期掃描。 這可能會導致這些定期掃描的無線頻率污染增加，以及無線網路介面卡使用的耗電量增加。

**安裝了無線局域網路服務的 windows 7 和 Windows Server 2008 R2：** 變更會在已安裝無線局域網路服務的 Windows 7 和 Windows Server 2008 R2 上執行，以將無線網路效能優化。 這些變更的設計目的是要減少無線網路的無線頻率污染、耗電量和即時流量中斷。 當無線局域網路設定檔中未設定此元素時， **autoSwitch** 的預設設定已變更。 在安裝了無線局域網路服務的 Windows 7 和 Windows Server 2008 R2 上，預設設定會變更為 "false"。 Windows Server 2008 和 Windows Vista 上的預設設定為 "true"。 建議將無線局域網路設定檔中的應用程式所使用的 **autoSwitch** 元素值設定為 "false"，以降低定期掃描新網路的頻率，除非應用程式絕對必須將此值設定為 "true"。

Windows **xp （含 SP3）和適用于 WINDOWS XP SP2 的無線區域網路 API：** 不支援這個元素。

``` syntax
<xs:element name="autoSwitch"
    type="boolean"
 />
```

**AutoSwitch** 元素是由 [**WLANProfile**](wlan-profileschema-wlanprofile-element.md)元素定義。

## <a name="examples"></a>範例

若要查看使用 **autoSwitch** 元素的範例設定檔，請參閱 [無線設定檔範例](wireless-profile-samples.md)。

## <a name="requirements"></a>規格需求



| 需求 | 值 |
|-------------------------------------|------------------------------------------------------|
| 最低支援的用戶端<br/> | \[僅限 Windows Vista 桌面應用程式\]<br/>       |
| 最低支援的伺服器<br/> | 僅限 Windows Server 2008 \[ desktop 應用程式\]<br/> |



## <a name="see-also"></a>另請參閱

<dl> <dt>

**架構中的元素定義內容**
</dt> <dt>

[**WLANProfile**](wlan-profileschema-wlanprofile-element.md)
</dt> <dt>

**架構實例中可能的直屬父元素**
</dt> <dt>

[**WLANProfile**](wlan-profileschema-wlanprofile-element.md)
</dt> </dl>

 

 




