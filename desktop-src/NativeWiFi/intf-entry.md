---
description: 包含 RPC 用戶端所需介面的詳細資訊。
ms.assetid: 92e734f3-eacb-44dc-9016-88dc6e9f04b6
title: 'INTF_ENTRY 結構 (Wzcsapi .h) '
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- INTF_ENTRY
api_type:
- HeaderDef
api_location:
- wzcsapi.h
ms.openlocfilehash: e08efc8c95374f268efe21f963357e9c4f34ae35
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/07/2021
ms.locfileid: "104512428"
---
# <a name="intf_entry-structure"></a>INTF \_ 專案結構

\[**INTF \_** Windows Vista 和 Windows Server 2008 不再支援此專案。 相反地，請使用 [原生 WIFI API](native-wifi-reference.md)，它會提供類似的功能。 如需詳細資訊，請參閱 [關於原生 WIFI API](about-the-native-wifi-api.md)。\]

包含 RPC 用戶端所需介面的詳細資訊。

## <a name="syntax"></a>語法


```C++
typedef struct {
  LPWSTR   wszGuid;
  LPWSTR   wszDescr;
  DWORD    dwContext;
  ULONG    ulMediaState;
  ULONG    ulMediaType;
  ULONG    ulPhysicalMediaType;
  INT      nInfraMode;
  INT      nAuthMode;
  INT      nWepStatus;
  DWORD    dwCtlFlags;
  DWORD    dwDynFlags;
  DWORD    dwCapabilities;
  RAW_DATA rdNicCapabilities;
  RAW_DATA rdSSID;
  RAW_DATA rdBSSID;
  RAW_DATA rdBSSIDList;
  RAW_DATA rdStSSIDList;
  RAW_DATA rdCtrlData;
} INTF_ENTRY, *PINTF_ENTRY;
```



## <a name="members"></a>成員

<dl> <dt>

**wszGuid**
</dt> <dd>

以下列格式的 Unicode 字串形式表示之介面 GUID 的指標： "{xxxxxxxx-xxxx-xxxx-xxxx-xxxxxxxxxxxx}"。

</dd> <dt>

**wszDescr**
</dt> <dd>

字串的指標，其中包含無線零設定服務 (WZCSVC) 取出的介面描述。

</dd> <dt>

**dwCoNtext**
</dt> <dd>

保留供內部使用。

</dd> <dt>

**ulMediaState**
</dt> <dd>

介面目前的 NDIS 媒體連接狀態。 下表顯示可能的值。



| 值                                                                                                                                                                                                                                                  | 意義                                |
|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|----------------------------------------|
| <span id="MEDIA_STATE_CONNECTED_"></span><span id="media_state_connected_"></span><dl> <dt>**媒體 \_ 狀態 \_ 已連線**</dt> <dt>1</dt> </dl>       | 媒體已連線。<br/>     |
| <span id="MEDIA_STATE_DISCONNECTED"></span><span id="media_state_disconnected"></span><dl> <dt>**媒體 \_狀態已 \_ 中斷**</dt>連線 <dt>0</dt> </dl> | 媒體已中斷連線。<br/>  |
| <span id="MEDIA_STATE_UNKNOWN"></span><span id="media_state_unknown"></span><dl> <dt>**媒體 \_\_未知狀態**</dt> <dt>-1</dt> </dl>               | 媒體狀態不明。<br/> |



 

</dd> <dt>

**ulMediaType**
</dt> <dd>

NIC 目前使用的 NDIS 媒體類型。 進行查詢時，這個成員的值會是 **NdisMedium802 \_ 3** ，如同 *Ndispnp .h* 標頭檔中所定義。

</dd> <dt>

**ulPhysicalMediaType**
</dt> <dd>

介面的 NDIS 媒體類型。 進行查詢時，此成員的值會 **NdisPhysicalMediumWirelessLan** 為 *Ndispnp .h* 標頭檔中所定義。

</dd> <dt>

**nInfraMode**
</dt> <dd>

在介面上設定的目前802.11 基礎結構模式。

</dd> <dt>

**nAuthMode**
</dt> <dd>

在介面上設定的目前802.11 驗證模式。

下表根據 *NtDDNdis .h* 標頭檔中定義的 **NDIS \_ 802 \_ 11 \_ 驗證 \_ 模式** 列舉，顯示參數的可能值。



| 值                                                                                                                                                                                                                                                                                                            | 意義                                                                                                                                                                                                                                                 |
|------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span id="Ndis802_11AuthModeOpen"></span><span id="ndis802_11authmodeopen"></span><span id="NDIS802_11AUTHMODEOPEN"></span><dl> <dt>**Ndis802 \_ 11AuthModeOpen**</dt> <dt>1</dt> </dl>                         | IEEE 802.11 開啟系統驗證。<br/>                                                                                                                                                                                                      |
| <span id="Ndis802_11AuthModeShared"></span><span id="ndis802_11authmodeshared"></span><span id="NDIS802_11AUTHMODESHARED"></span><dl> <dt>**Ndis802 \_ 11AuthModeShared**</dt> <dt>2</dt> </dl>                 | IEEE 802.11 共用驗證，使用預先共用的有線對等隱私權 (WEP) 金鑰。 <br/>                                                                                                                                                |
| <span id="Ndis802_11AuthModeAutoSwitch"></span><span id="ndis802_11authmodeautoswitch"></span><span id="NDIS802_11AUTHMODEAUTOSWITCH"></span><dl> <dt>**Ndis802 \_ 11AuthModeAutoSwitch**</dt> <dt>3</dt> </dl> | 自動切換模式。 使用自動切換模式時，無線網路介面卡 (NIC) 會先嘗試共用驗證模式。 如果共用模式失敗，則 NIC 會嘗試使用 open 驗證模式。 <br/>                                    |
| <span id="Ndis802_11AuthModeWPA"></span><span id="ndis802_11authmodewpa"></span><span id="NDIS802_11AUTHMODEWPA"></span><dl> <dt>**Ndis802 \_ 11AuthModeWPA**</dt> <dt>4</dt> </dl>                             |  (WPA 的無線保護存取) 安全性。 驗證是透過 IEEE 802.1 X 在要求者、驗證器和驗證服務器之間執行。 加密金鑰是動態的，並且會透過驗證程式來衍生。 <br/>     |
| <span id="Ndis802_11AuthModeWPAPSK"></span><span id="ndis802_11authmodewpapsk"></span><span id="NDIS802_11AUTHMODEWPAPSK"></span><dl> <dt>**Ndis802 \_ 11AuthModeWPAPSK**</dt> <dt>5</dt> </dl>                 | 使用預先共用金鑰的 WPA 安全性。 驗證是透過 IEEE 802.1 X 在要求者和驗證器之間執行。 加密金鑰是動態的，而且是透過要求者和驗證器所使用的預先共用金鑰所衍生。 <br/> |
| <span id="Ndis802_11AuthModeWPANone"></span><span id="ndis802_11authmodewpanone"></span><span id="NDIS802_11AUTHMODEWPANONE"></span><dl> <dt>**Ndis802 \_ 11AuthModeWPANone**</dt> <dt>6</dt> </dl>             | WPA 安全性。 使用未使用 IEEE 802.1 X 驗證的預先共用金鑰執行驗證。 加密金鑰是靜態的，而且是透過預先共用的金鑰來衍生。 此模式只適用于臨機操作網路類型。 <br/>             |
| <span id="Ndis802_11AuthModeWPA2"></span><span id="ndis802_11authmodewpa2"></span><span id="NDIS802_11AUTHMODEWPA2"></span><dl> <dt>**Ndis802 \_ 11AuthModeWPA2**</dt> <dt>7</dt> </dl>                         | WPA2 安全性。 驗證是透過 IEEE 802.1 X 在要求者、驗證器和驗證服務器之間執行。 加密金鑰是動態的，並且會透過驗證程式來衍生。 <br/>                               |
| <span id="Ndis802_11AuthModeWPA2PSK"></span><span id="ndis802_11authmodewpa2psk"></span><span id="NDIS802_11AUTHMODEWPA2PSK"></span><dl> <dt>**Ndis802 \_ 11AuthModeWPA2PSK**</dt> <dt>8</dt> </dl>             | 指定 WPA2 安全性。 驗證是透過 IEEE 802 1X 在要求者與驗證器之間執行。 加密金鑰是動態的，而且是透過要求者和驗證器所使用的預先共用金鑰所衍生。 <br/>             |
| <span id="Ndis802_11AuthModeMax"></span><span id="ndis802_11authmodemax"></span><span id="NDIS802_11AUTHMODEMAX"></span><dl> <dt>**Ndis802 \_ 11AuthModeMax**</dt> <dt>9</dt> </dl>                             | **NDIS \_ 802 \_ 11 \_ 驗證 \_ 模式** 列舉值的最大可能值。 這不是驗證模式的合法值。 <br/>                                                                                        |



 

</dd> <dt>

**nWepStatus**
</dt> <dd>

在介面上設定的目前802.11 加密模式。

</dd> <dt>

**dwCtlFlags**
</dt> <dd>

控制旗標的位元遮罩值，表示 WZCSVC 在介面上的運作方式。

下表顯示可能的位值。



| 值                                                                                                                                                                                                                                 | 意義                                                                                                                                                                                                                                                                                     |
|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span id="INTFCTL_CM_MASK"></span><span id="intfctl_cm_mask"></span><dl> <dt>**INTFCTL \_CM \_ 遮罩**</dt> <dt>0x0007</dt> </dl>      | 網路篩選模式的位元遮罩。 INTFCTL \_ CM \_ MASK & dwCtlFlags 會產生類型 NDIS \_ 802 \_ 11 \_ 網路 \_ 基礎結構的值。 產生的值會指出 WZCSVC 只會連線到基礎結構網路、臨機操作網路，或連線至這兩種網路類型。<br/> |
| <span id="INTFCTL_ENABLED"></span><span id="intfctl_enabled"></span><dl> <dt>**INTFCTL \_啟用**</dt> <dt>0x8000</dt> </dl>       | 指出 WZCSVC 是否應設定介面。<br/>                                                                                                                                                                                                                         |
| <span id="INTFCTL_FALLBACK"></span><span id="intfctl_fallback"></span><dl> <dt>**INTFCTL \_回退**</dt> <dt>0x4000</dt> </dl>    | 如果無法使用慣用網路，此值會指出 WZCSVC 是否應該自動設定要與任何可用網路相關聯的 NIC。<br/>                                                                                                                       |
| <span id="INTFCTL_OIDSSUPP_"></span><span id="intfctl_oidssupp_"></span><dl> <dt> **INTFCTL \_ OIDSSUPP**</dt> <dt>0x2000</dt> </dl> | 指出 NIC 驅動程式是否支援 WZCSVC 運作所需的所有 802.11 Oid。<br/>                                                                                                                                                                                    |
| <span id="INTFCTL_VOLATILE_"></span><span id="intfctl_volatile_"></span><dl> <dt> **INTFCTL \_ VOLATILE**</dt> <dt>0x1000</dt> </dl> | 指出此介面的服務參數是否應該保留在登錄中。 <br/> 如果設定了這個值，這些參數就會是暫時性的，不應該保留在登錄中。<br/>                                                                 |
| <span id="INTFCTL_POLICY_"></span><span id="intfctl_policy_"></span><dl> <dt> **INTFCTL \_ 原則**</dt> <dt>0x0800</dt> </dl>       | 指出此介面的服務參數是否由群組原則推送。<br/> 如果設定此值，則會依群組原則將服務參數推送至本機電腦。<br/>                                                                         |
| <span id="INTFCTL_8021XSUPP"></span><span id="intfctl_8021xsupp"></span><dl> <dt>**INTFCTL \_ 8021XSUPP**</dt> <dt>0x1000</dt> </dl> | 指出是否已啟用 802.1 X 支援。<br/>                                                                                                                                                                                                                                     |



 

</dd> <dt>

**dwDynFlags**
</dt> <dd>

動態旗標的位元遮罩，可控制介面上動態 (非持續性和非靜態) 行為。

這些位有助於以 WZCSVC 在介面上的運作方式觸發動態、暫時的變更。 這些位都不會保存在登錄中，因此這些設定將不會在系統重新開機或裝置停用和啟用順序時存活。

下表顯示可能的位值。



| 值                                                                                                                                                                                                                            | 意義                                                                                                                                            |
|----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|----------------------------------------------------------------------------------------------------------------------------------------------------|
| <span id="INTFDYN_NOSCAN"></span><span id="intfdyn_noscan"></span><dl> <dt>**INTFDYN \_NOSCAN**</dt> <dt>0x00000001</dt> </dl> | 指出 WZCSVC 不應要求介面進行主動掃描，但改為在 NIC 驅動程式中使用快取的值。<br/> |



 

</dd> <dt>

**dwCapabilities**
</dt> <dd>

指定驅動程式功能。



| 值                                                                                                                                                                                                                                                         | 意義                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                              |
|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span id="INTFCAP_MAX_CIPHER_MASK"></span><span id="intfcap_max_cipher_mask"></span><dl> <dt>**INTFCAP \_最大 \_ 密碼 \_ 遮罩**</dt> <dt>0x000000ff</dt> </dl> | 此成員的較低順序位可用來指出支援的最大加密。 可能的值是 Windows SDK 中所包含的 *NtDDNdis .h* 標頭檔中， **NDIS \_ 802 \_ 11 \_ WEP \_ 狀態** 結構中所定義的一些列舉值。<br/> Ndis802 \_ 11Encryption1Enabled 值 (2) 表示支援 WEP。 不支援 TKIP 和 AES，而且傳輸金鑰可能或可能無法使用。 <br/> Ndis802 \_ 11Encryption2Enabled 值 (9) 指出支援 TKIP 和 WEP。 AES 不受支援，且有可用的傳輸金鑰。 <br/> Ndis802 \_ 11Encryption3Enabled 值 (11) 指出支援 AES、TKIP 和 WEP，且有可用的傳輸金鑰。 <br/> Ndis802 \_ 11EncryptionNotSupported (8) 指出不支援 WEP 金鑰。 <br/> |
| <span id="INTFCAP_SSN"></span><span id="intfcap_ssn"></span><dl> <dt>**INTFCAP \_SSN**</dt> <dt>0x00000100</dt> </dl>                                       | 指出支援簡單的安全網路 (SSN) 這是 802.11 i 的子集。 <br/> SSN 會定期變更加密金鑰，而非 WEP (有線對等的隱私權) 標準（使用靜態金鑰）。 為了讓 SSN 能夠運作，最大支援的密碼至少應該是 TKIP。 SSN 是由一家廠商協會在2002中開發，做為在 IEEE 802.11 i 標準完成時改善無線區域網路安全性的過渡方法。<br/>                                                                                                                                                                                                                                                                                                                                                                                            |
| <span id="INTFCAP_80211I"></span><span id="intfcap_80211i"></span><dl> <dt>**INTFCAP \_ 80211I**</dt> <dt>0x00000200</dt> </dl>                              | 指出 IEEE 802.11 i 標準的支援。<br/>                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                          |



 

</dd> <dt>

**rdNicCapabilities**
</dt> <dd>

適用于 802.11 i 的一組功能。

[**WZCQueryInterface**](wzcqueryinterface.md)函式會在呼叫時傳回 **rdNicCapabilities** 的資料，並在 *dwInflags* 參數中傳遞 **INTF \_ 功能** 旗標。 如果函式呼叫成功，**原始 \_ 資料** 結構的 **.pdata** 成員就會包含 **INTF \_ 80211 \_ 功能** 結構。

</dd> <dt>

**rdSSID**
</dt> <dd>

包含目前在介面上設定之 802.11 SSID 的二進位資料。

[**WZCQueryInterface**](wzcqueryinterface.md)函式會在呼叫時傳回 **rdSSID** 的資料，並在 *dwInflags* 參數中傳遞 **INTF 的 \_ SSID** 旗標。 如果函式呼叫成功，**原始 \_ 資料** 結構 **的 DwDataLen** 成員會包含 **Ndis \_ 802 \_ 11 \_ ssid** 結構的 **>ssidlength** 成員，而 **原始 \_ 資料** 結構的 **.pdata** 成員則包含 **ndis \_ 802 \_ 11 \_ ssid** 結構的 **ssid** 成員。

**NDIS \_ 802 \_ 11 \_ SSID** 結構定義于 *Ntddndis .h* 標頭檔中。

</dd> <dt>

**rdBSSID**
</dt> <dd>

包含在介面上設定 802.11 BSSID 的二進位資料。

[**WZCQueryInterface**](wzcqueryinterface.md)函式會在呼叫時傳回 **rdBSSID** 的資料，並在 *dwInflags* 參數中傳遞 **INTF \_ BSSID** 旗標。 如果函式呼叫成功，**原始 \_ 資料** 結構的 **DwDataLen** 成員會包含 **ndis \_ 802 \_ 11 \_ mac \_ 位址** 結構的大小，而 **原始 \_ 資料** 結構的 **.pdata** 成員則包含 **ndis \_ 802 \_ 11 \_ mac \_ 位址** 結構。

**NDIS \_ 802 \_ 11 \_ MAC \_ 位址** 結構定義于 *Ntddndis .h* 標頭檔中。

</dd> <dt>

**rdBSSIDList**
</dt> <dd>

二進位資料，其中包含 WZCSVC 最後一次取出的 BSSIDs 清單。

[**WZCQueryInterface**](wzcqueryinterface.md)函式會在呼叫時傳回 **rdBSSIDList** 的資料，並在 *dwInflags* 參數中傳遞 **INTF \_ BSSIDLIST** 旗標。 如果函式呼叫成功，**原始 \_ 資料** 結構的 **dwDataLen** 成員就會包含緩衝區的長度以及傳回的資料，而 **原始 \_ 資料** 結構的 **.pdata** 成員會包含 **WZC \_ 802 \_ 11 \_ CONFIG \_ LIST** 結構。

</dd> <dt>

**rdStSSIDList**
</dt> <dd>

包含針對此介面設定之慣用網路清單的二進位資料。

[**WZCQueryInterface**](wzcqueryinterface.md)函式會在呼叫時傳回 **rdStSSIDList** 的資料，並在 *dwInflags* 參數中傳遞 **INTF \_ PREFLIST** 旗標。 如果函式呼叫成功，**原始 \_ 資料** 結構的 **dwDataLen** 成員就會包含緩衝區的長度以及傳回的資料，而 **原始 \_ 資料** 結構的 **.pdata** 成員會包含 **WZC \_ 802 \_ 11 \_ CONFIG \_ LIST** 結構。

如果其中一個慣用的網路目前已連線，則網路的 **WZC \_ WLAN \_** 設定結構的 **dwCtlFlags** 成員會將 **WZCCTL \_ 媒體 \_ 連線** (0x0400) 位組。

</dd> <dt>

**rdCtrlData**
</dt> <dd>

在介面上設定其他參數時，與其他控制項旗標搭配使用的二進位資料。

</dd> </dl>

## <a name="remarks"></a>備註

[**WZCQueryInterface**](wzcqueryinterface.md)和 [**WZCRefreshInterface**](wzcrefreshinterface.md)函數會使用 **INTF \_ 專案** 結構。

**原始 \_ 資料** 結構的定義如下：


```C++
typedef struct
{
    DWORD   dwDataLen;
    LPBYTE  pData;
} RAW_DATA, *PRAW_DATA;
```



*.Pdata* 成員指向二進位資料。 *DwDataLen* 指出 *.pdata* 所指向的位元組數目。

> [!Note]  
> Windows SDK 中無法使用 *Wzcsapi .h* 標頭檔。

 

## <a name="requirements"></a>規格需求



| 需求 | 值 |
|-------------------------------------|--------------------------------------------------------------------------------------|
| 最低支援的用戶端<br/> | 僅限 Windows XP （含 SP2） \[ 桌面應用程式\]<br/>                                 |
| 最低支援的伺服器<br/> | 僅限 Windows Server 2003 \[ desktop 應用程式\]<br/>                                 |
| 用戶端支援結束<br/>    | Windows XP （含 SP3）<br/>                                                       |
| 伺服器支援結束<br/>    | Windows Server 2003<br/>                                                       |
| 標頭<br/>                   | <dl> <dt>Wzcsapi。h</dt> </dl> |



## <a name="see-also"></a>另請參閱

<dl> <dt>

[**WZCEnumInterfaces**](wzcenuminterfaces.md)
</dt> <dt>

[**WZCQueryInterface**](wzcqueryinterface.md)
</dt> <dt>

[**WZCRefreshInterface**](wzcrefreshinterface.md)
</dt> </dl>

 

 




