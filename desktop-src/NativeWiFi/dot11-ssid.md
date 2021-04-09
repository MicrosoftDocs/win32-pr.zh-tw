---
description: 包含介面的 SSID。
ms.assetid: f2b15ef9-99ee-4505-8575-224112024d7a
title: 'DOT11_SSID 結構 (Wlantypes .h) '
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- DOT11_SSID
api_type:
- HeaderDef
api_location:
- wlantypes.h
ms.openlocfilehash: e319d22db33a627be631f9b6b0ee36591bc7a5bd
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/08/2021
ms.locfileid: "103849916"
---
# <a name="dot11_ssid-structure"></a>DOT11 \_ SSID 結構

**DOT11 \_ ssid** 結構包含介面的 ssid。

## <a name="syntax"></a>語法


```C++
typedef struct _DOT11_SSID {
  ULONG uSSIDLength;
  UCHAR ucSSID[DOT11_SSID_MAX_LENGTH];
} DOT11_SSID, *PDOT11_SSID;
```



## <a name="members"></a>成員

<dl> <dt>

**uSSIDLength**
</dt> <dd>

**UcSSID** 陣列的長度（以位元組為單位）。

</dd> <dt>

**ucSSID**
</dt> <dd>

SSID。 DOT11 \_ SSID \_ 最大 \_ 長度設為32。

</dd> </dl>

## <a name="remarks"></a>備註

**UcSSID** 成員所指定的 SSID 不是以 null 結束的 ASCII 字串。 SSID 的長度取決於 **uSSIDLength** 成員。

萬用字元 SSID 是其 **uSSIDLength** 成員設定為零的 ssid。 當所需的 SSID 設定為萬用字元 SSID 時，802.11 工作站可以連接到任何基本的服務集 (BSS) 網路。

## <a name="requirements"></a>規格需求



| 需求 | 值 |
|-------------------------------------|-------------------------------------------------------------------------------------------------------------|
| 最低支援的用戶端<br/> | Windows Vista、Windows XP （僅含 SP3） \[ 桌面應用程式\]<br/>                                         |
| 最低支援的伺服器<br/> | 僅限 Windows Server 2008 \[ desktop 應用程式\]<br/>                                                        |
| 可轉散發套件<br/>          | 適用于 Windows XP SP2 的無線區域網路 API<br/>                                                         |
| 標頭<br/>                   | <dl> <dt>Wlantypes (包含 Windot11) </dt> </dl> |



## <a name="see-also"></a>另請參閱

<dl> <dt>

[**WLAN \_ 連接 \_ 參數**](/windows/desktop/api/wlanapi/ns-wlanapi-wlan_connection_parameters)
</dt> <dt>

[**WlanGetNetworkBssList**](/windows/desktop/api/Wlanapi/nf-wlanapi-wlangetnetworkbsslist)
</dt> <dt>

[**WlanScan**](/windows/desktop/api/wlanapi/nf-wlanapi-wlanscan)
</dt> </dl>

 

 




