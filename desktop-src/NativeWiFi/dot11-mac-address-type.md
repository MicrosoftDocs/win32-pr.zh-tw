---
description: 用來定義 IEEE 媒體存取控制 (MAC) 位址。
ms.assetid: c1335127-a2d2-4f44-a895-1abbc5eaf98d
title: 'DOT11_MAC_ADDRESS (Windot11) '
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- kbSyntax
api_name: ''
api_type: ''
api_location: ''
ms.openlocfilehash: da6b2d625037395ca26aa4616a5f7ee7588a4111c358015c0ccff3be8e032796
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/11/2021
ms.locfileid: "117798458"
---
# <a name="dot11_mac_address"></a>DOT11 \_ MAC \_ 位址

**DOT11 \_ mac \_ 位址** 類型可用來定義 IEEE 媒體存取控制 (mac) 位址。


```C++
typedef UCHAR DOT11_MAC_ADDRESS[6];
typedef DOT11_MAC_ADDRESS* PDOT11_MAC_ADDRESS;
```



<dl> <dt>

**DOT11 \_ MAC \_ 位址 \[ 6\]**
</dt> <dd>

單播、多播或廣播格式的 MAC 位址。

</dd> <dt>

**PDOT11 \_ MAC \_ 位址**
</dt> <dd>

單播、多播或廣播格式的 MAC 位址指標。

</dd> </dl>

## <a name="requirements"></a>規格需求



| 需求 | 值 |
|-------------------------------------|------------------------------------------------------------------------------------------------------------|
| 最低支援的用戶端<br/> | WindowsVista，Windows XP 只提供 SP3 \[ desktop 應用程式\]<br/>                                        |
| 最低支援的伺服器<br/> | Windows\[僅限 Server 2008 desktop 應用程式\]<br/>                                                       |
| 可轉散發套件<br/>          | 適用于 Windows XP SP2 的無線區域網路 API<br/>                                                        |
| 標頭<br/>                   | <dl> <dt>Windot11 (包含 Windot11) </dt> </dl> |



## <a name="see-also"></a>另請參閱

<dl> <dt>

[**DOT11 \_ BSSID \_ 清單**](dot11-bssid-list.md)
</dt> <dt>

[**WLAN \_ 關聯 \_ 屬性**](/windows/desktop/api/wlanapi/ns-wlanapi-wlan_association_attributes)
</dt> <dt>

[**WLAN \_ BSS \_ 專案**](/windows/desktop/api/wlanapi/ns-wlanapi-wlan_bss_entry)
</dt> </dl>

 

 




