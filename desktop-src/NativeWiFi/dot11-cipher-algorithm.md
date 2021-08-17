---
description: 定義用於資料加密和解密的密碼演算法。
ms.assetid: 6b634d76-a159-438e-8fc6-5f05b326ed68
title: 'DOT11_CIPHER_ALGORITHM 列舉 (Wlantypes .h) '
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- DOT11_CIPHER_ALGORITHM
api_type:
- HeaderDef
api_location:
- wlantypes.h
ms.openlocfilehash: c99ef5b648c5503743de6f51ce7d035d75dbe1f3e5593d473a374813f4000566
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/11/2021
ms.locfileid: "119780238"
---
# <a name="dot11_cipher_algorithm-enumeration"></a>DOT11 \_ 加密 \_ 演算法列舉

**DOT11 \_ CIPHER \_ 演算法** 列舉型別會定義用於資料加密和解密的密碼演算法。

## <a name="syntax"></a>Syntax


```C++
typedef enum _DOT11_CIPHER_ALGORITHM { 
  DOT11_CIPHER_ALGO_NONE           = 0x00,
  DOT11_CIPHER_ALGO_WEP40          = 0x01,
  DOT11_CIPHER_ALGO_TKIP           = 0x02,
  DOT11_CIPHER_ALGO_CCMP           = 0x04,
  DOT11_CIPHER_ALGO_WEP104         = 0x05,
  DOT11_CIPHER_ALGO_WPA_USE_GROUP  = 0x100,
  DOT11_CIPHER_ALGO_RSN_USE_GROUP  = 0x100,
  DOT11_CIPHER_ALGO_WEP            = 0x101,
  DOT11_CIPHER_ALGO_IHV_START      = 0x80000000,
  DOT11_CIPHER_ALGO_IHV_END        = 0xffffffff
} DOT11_CIPHER_ALGORITHM, *PDOT11_CIPHER_ALGORITHM;
```



## <a name="constants"></a>常數

<dl> <dt>

<span id="DOT11_CIPHER_ALGO_NONE"></span><span id="dot11_cipher_algo_none"></span>**DOT11 \_ 加密 \_ ALGO \_ 無**
</dt> <dd>

指定不啟用或支援任何加密演算法。

</dd> <dt>

<span id="DOT11_CIPHER_ALGO_WEP40"></span><span id="dot11_cipher_algo_wep40"></span>**DOT11 \_ CIPHER \_ ALGO \_ WEP40**
</dt> <dd>

指定有線對等隱私權 (WEP) 演算法，這是 802.11-1999 標準中指定的 RC4 型演算法。 此列舉值會以40位加密金鑰指定 WEP 密碼演算法。

</dd> <dt>

<span id="DOT11_CIPHER_ALGO_TKIP"></span><span id="dot11_cipher_algo_tkip"></span>**DOT11 \_ CIPHER \_ ALGO \_ TKIP**
</dt> <dd>

指定 (TKIP) 演算法的暫時金鑰完整性通訊協定，這是以 RC4 為基礎的加密套件，以 WPA 規格和 IEEE 802.11 i-2004 標準中定義的演算法為基礎。 此加密也會使用 Michael 訊息完整性代碼 (MIC) 演算法來進行偽造保護。

</dd> <dt>

<span id="DOT11_CIPHER_ALGO_CCMP"></span><span id="dot11_cipher_algo_ccmp"></span>**DOT11 \_ CIPHER \_ ALGO \_ CCMP**
</dt> <dd>

指定 AES CCMP 演算法，如同 IEEE 802.11 i-2004 標準和 RFC 3610 中所指定。 進階加密標準 (AES) 是 FIPS PUB 197 中定義的加密演算法。

</dd> <dt>

<span id="DOT11_CIPHER_ALGO_WEP104"></span><span id="dot11_cipher_algo_wep104"></span>**DOT11 \_ CIPHER \_ ALGO \_ WEP104**
</dt> <dd>

使用104位加密金鑰指定 WEP 密碼演算法。

</dd> <dt>

<span id="DOT11_CIPHER_ALGO_WPA_USE_GROUP"></span><span id="dot11_cipher_algo_wpa_use_group"></span>**DOT11 \_ CIPHER \_ ALGO \_ WPA \_ USE \_ GROUP**
</dt> <dd>

指定 Wi-Fi 保護的存取 (WPA) 使用群組金鑰加密套件。 如需有關使用群組金鑰加密套件的詳細資訊，請參閱 IEEE 802.11 i-2004 標準的 < 子句7.3.2.25.1。

</dd> <dt>

<span id="DOT11_CIPHER_ALGO_RSN_USE_GROUP"></span><span id="dot11_cipher_algo_rsn_use_group"></span>**DOT11 \_ CIPHER \_ ALGO \_ RSN \_ USE \_ GROUP**
</dt> <dd>

指定健全的安全性網路 (RSN) 使用群組金鑰加密套件。 如需有關使用群組金鑰加密套件的詳細資訊，請參閱 IEEE 802.11 i-2004 標準的 < 子句7.3.2.25.1。

</dd> <dt>

<span id="DOT11_CIPHER_ALGO_WEP"></span><span id="dot11_cipher_algo_wep"></span>**DOT11 \_ CIPHER \_ ALGO \_ WEP**
</dt> <dd>

指定具有任何長度之加密金鑰的 WEP 加密演算法。

</dd> <dt>

<span id="DOT11_CIPHER_ALGO_IHV_START"></span><span id="dot11_cipher_algo_ihv_start"></span>**DOT11 \_ CIPHER \_ ALGO \_ IHV \_ 開始**
</dt> <dd>

指定範圍的開頭，此範圍用來定義獨立硬體廠商 (IHV) 所開發的專屬加密演算法。

</dd> <dt>

<span id="DOT11_CIPHER_ALGO_IHV_END"></span><span id="dot11_cipher_algo_ihv_end"></span>**DOT11 \_ CIPHER \_ ALGO \_ IHV \_ END**
</dt> <dd>

指定範圍的結尾，此範圍用來定義由 IHV 所開發的專屬加密演算法。

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

 

 




