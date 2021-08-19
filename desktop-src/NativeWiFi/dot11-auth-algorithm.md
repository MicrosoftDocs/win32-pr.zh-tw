---
description: 定義無線區域網路驗證演算法。
ms.assetid: ac4097df-46dc-4c64-b72a-7cb9dce8b418
title: 'DOT11_AUTH_ALGORITHM 列舉 (Wlantypes .h) '
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- DOT11_AUTH_ALGORITHM
api_type:
- HeaderDef
api_location:
- wlantypes.h
ms.openlocfilehash: 774b2218a451f4cbaa85e6b77559c0d5761b0b132ebdf9d3f11c15ea6658e7bf
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/11/2021
ms.locfileid: "117798468"
---
# <a name="dot11_auth_algorithm-enumeration"></a>DOT11 \_ AUTH \_ 演算法列舉

**DOT11 \_ AUTH \_ 演算法** 列舉型別定義了無線區域網路驗證演算法。

## <a name="syntax"></a>Syntax


```C++
typedef enum _DOT11_AUTH_ALGORITHM { 
  DOT11_AUTH_ALGO_80211_OPEN        = 1,
  DOT11_AUTH_ALGO_80211_SHARED_KEY  = 2,
  DOT11_AUTH_ALGO_WPA               = 3,
  DOT11_AUTH_ALGO_WPA_PSK           = 4,
  DOT11_AUTH_ALGO_WPA_NONE          = 5,
  DOT11_AUTH_ALGO_RSNA              = 6,
  DOT11_AUTH_ALGO_RSNA_PSK          = 7,
  DOT11_AUTH_ALGO_IHV_START         = 0x80000000,
  DOT11_AUTH_ALGO_IHV_END           = 0xffffffff
} DOT11_AUTH_ALGORITHM, *PDOT11_AUTH_ALGORITHM;
```



## <a name="constants"></a>常數

<dl> <dt>

<span id="DOT11_AUTH_ALGO_80211_OPEN"></span><span id="dot11_auth_algo_80211_open"></span>**DOT11 \_ AUTH \_ ALGO \_ 80211 \_ 開啟**
</dt> <dd>

指定 IEEE 802.11 開放式系統驗證演算法。

</dd> <dt>

<span id="DOT11_AUTH_ALGO_80211_SHARED_KEY"></span><span id="dot11_auth_algo_80211_shared_key"></span>**DOT11 \_ AUTH \_ ALGO \_ 80211 \_ 共用 \_ 金鑰**
</dt> <dd>

指定802.11 共用金鑰驗證演算法，此演算法需要使用預先共用的有線對等隱私權 (WEP) 金鑰進行802.11 驗證。

</dd> <dt>

<span id="DOT11_AUTH_ALGO_WPA"></span><span id="dot11_auth_algo_wpa"></span>**DOT11 \_ AUTH \_ ALGO \_ WPA**
</dt> <dd>

 (WPA) 演算法指定 Wi-Fi 保護的存取。 IEEE 802.1 X 埠驗證是由要求者、驗證器和驗證服務器所執行。 加密金鑰是透過驗證程式進行動態衍生。

此演算法只對 dot11 \_ bss \_ 類型基礎結構的 bss 類型有效 \_ 。

啟用 WPA 演算法時，802.11 站只會與存取點相關聯，而該存取點的指標或探查回應會包含類型 1 (802.1 X) 在 WPA 資訊元素 (IE) 內的驗證套件。

</dd> <dt>

<span id="DOT11_AUTH_ALGO_WPA_PSK"></span><span id="dot11_auth_algo_wpa_psk"></span>**DOT11 \_ AUTH \_ ALGO \_ WPA \_ PSK**
</dt> <dd>

指定使用預先共用金鑰 (PSK) 的 WPA 演算法。 「IEEE 802.1 X 埠驗證」是由要求者和驗證者執行。 加密金鑰是透過在要求者和驗證者上使用的預先共用金鑰來動態衍生。

此演算法只對 **dot11 \_ bss \_ 類型 \_ 基礎結構** 的 bss 類型有效。

啟用 WPA PSK 演算法時，802.11 工作站只會與存取點相關聯，該存取點的指標或探查回應會包含類型2的驗證套件， (預先共用金鑰) 在 WPA IE 內。

</dd> <dt>

<span id="DOT11_AUTH_ALGO_WPA_NONE"></span><span id="dot11_auth_algo_wpa_none"></span>**DOT11 \_ AUTH \_ ALGO \_ WPA \_ NONE**
</dt> <dd>

不支援這個值。

</dd> <dt>

<span id="DOT11_AUTH_ALGO_RSNA"></span><span id="dot11_auth_algo_rsna"></span>**DOT11 \_ AUTH \_ ALGO \_ RSNA**
</dt> <dd>

指定 802.11 i 穩固的安全性網路關聯 (RSNA) 演算法。 WPA2 就是其中一種演算法。 IEEE 802.1 X 埠驗證是由要求者、驗證器和驗證服務器所執行。 加密金鑰是透過驗證程式進行動態衍生。

此演算法只對 **dot11 \_ bss \_ 類型 \_ 基礎結構** 的 bss 類型有效。

啟用 RSNA 演算法時，802.11 站只會與一個存取點相關聯，該存取點的指標或探查回應會包含 RSN IE 內類型 1 (802.1 X) 的驗證套件。

</dd> <dt>

<span id="DOT11_AUTH_ALGO_RSNA_PSK"></span><span id="dot11_auth_algo_rsna_psk"></span>**DOT11 \_ AUTH \_ ALGO \_ RSNA \_ PSK**
</dt> <dd>

指定使用 PSK 的 802.11 i RSNA 演算法。 「IEEE 802.1 X 埠驗證」是由要求者和驗證者執行。 加密金鑰是透過在要求者和驗證者上使用的預先共用金鑰來動態衍生。

此演算法只對 **dot11 \_ bss \_ 類型 \_ 基礎結構** 的 bss 類型有效。

當啟用 RSNA PSK 演算法時，802.11 站只會與存取點產生關聯，而該存取點的指標或探查回應會包含類型2的驗證套件， (預先共用金鑰) 在 RSN IE 內。

</dd> <dt>

<span id="DOT11_AUTH_ALGO_IHV_START"></span><span id="dot11_auth_algo_ihv_start"></span>**DOT11 \_ AUTH \_ ALGO \_ IHV \_ START**
</dt> <dd>

表示範圍的開頭，此範圍會指定由 IHV 開發的專屬驗證演算法。

只有當微型埠驅動程式是在可延伸工作站 (ExtSTA) 模式下運作時， **DOT11 \_ AUTH \_ ALGO \_ IHV \_ 啟動** 列舉值才有效。

</dd> <dt>

<span id="DOT11_AUTH_ALGO_IHV_END"></span><span id="dot11_auth_algo_ihv_end"></span>**DOT11 \_ AUTH \_ ALGO \_ IHV \_ END**
</dt> <dd>

表示範圍的結尾，此範圍會指定由 IHV 開發的專屬驗證演算法。

只有當微型埠驅動程式是以 ExtSTA 模式運作時， **DOT11 \_ AUTH \_ ALGO \_ IHV \_ END** 列舉值才有效。

</dd> </dl>

## <a name="requirements"></a>規格需求



| 需求 | 值 |
|-------------------------------------|-------------------------------------------------------------------------------------------------------------|
| 最低支援的用戶端<br/> | WindowsVista，Windows XP 只提供 SP3 \[ desktop 應用程式\]<br/>                                         |
| 最低支援的伺服器<br/> | Windows\[僅限 Server 2008 desktop 應用程式\]<br/>                                                        |
| 可轉散發套件<br/>          | 適用于 Windows XP SP2 的無線區域網路 API<br/>                                                         |
| 標頭<br/>                   | <dl> <dt>Wlantypes (包含 Windot11) </dt> </dl> |



## <a name="see-also"></a>另請參閱

<dl> <dt>

[**DOT11 \_ AUTH \_ CIPHER \_ 配對**](dot11-auth-cipher-pair.md)
</dt> <dt>

[**可用的 WLAN \_ \_ 網路**](/windows/desktop/api/wlanapi/ns-wlanapi-wlan_available_network)
</dt> <dt>

[**WLAN \_ 安全性 \_ 屬性**](/windows/desktop/api/wlanapi/ns-wlanapi-wlan_security_attributes)
</dt> </dl>

 

 




