---
description: 包含目前用於 802.1 X 驗證之 802.1 X 連接設定檔的相關資訊。
ms.assetid: ec494c74-bc79-445a-8889-a6f441e95ac5
title: ONEX_CONNECTION_PROFILE 結構
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- ONEX_CONNECTION_PROFILE
api_type:
- NA
api_location: ''
ms.openlocfilehash: 21e02a1f09d3439c64fb8124cd0cfc8140732be9
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/07/2021
ms.locfileid: "106974440"
---
# <a name="onex_connection_profile-structure"></a>ONEX \_ 連接 \_ 設定檔結構

**ONEX 連線 \_ \_ 設定檔** 結構包含目前用於 802.1 X 驗證之 802.1 x 連線設定檔的相關資訊。

## <a name="syntax"></a>語法


```C++
typedef struct _ONEX_CONNECTION_PROFILE {
  DWORD                dwVersion;
  DWORD                dwTotalLen;
  DWORD                fOneXSupplicantFlags  :1;
  DWORD                fsupplicantMode  :1;
  DWORD                fauthMode  :1;
  DWORD                fHeldPeriod  :1;
  DWORD                fAuthPeriod  :1;
  DWORD                fStartPeriod  :1;
  DWORD                fMaxStart  :1;
  DWORD                fMaxAuthFailures  :1;
  DWORD                fNetworkAuthTimeout  :1;
  DWORD                fAllowLogonDialogs  :1;
  DWORD                fNetworkAuthWithUITimeout  :1;
  DWORD                fUserBasedVLan  :1;
  DWORD                dwOneXSupplicantFlags;
  ONEX_SUPPLICANT_MODE supplicantMode;
  ONEX_AUTH_MODE       authMode;
  DWORD                dwHeldPeriod;
  DWORD                dwAuthPeriod;
  DWORD                dwStartPeriod;
  DWORD                dwMaxStart;
  DWORD                dwMaxAuthFailures;
  DWORD                dwNetworkAuthTimeout;
  DWORD                dwNetworkAuthWithUITimeout;
  BOOL                 bAllowLogonDialogs;
  BOOL                 bUserBasedVLan;
} ONEX_CONNECTION_PROFILE, *PONEX_CONNECTION_PROFILE;
```



## <a name="members"></a>成員

<dl> <dt>

**dwVersion**
</dt> <dd>

此 **ONEX \_ 連接 \_ 設定檔** 結構的版本。

</dd> <dt>

**dwTotalLen**
</dt> <dd>

此 **ONEX \_ 連接 \_ 設定檔** 結構的長度（以位元組為單位）。

</dd> <dt>

**fOneXSupplicantFlags**
</dt> <dd>

指出 **ONEX \_ 連接 \_ 設定檔** 結構是否包含 **dwOneXSupplicantFlags** 成員中的有效資料。

</dd> <dt>

**fsupplicantMode**
</dt> <dd>

指出 **ONEX \_ 連接 \_ 設定檔** 結構是否包含 **supplicantMode** 成員中的有效資料。

</dd> <dt>

**fauthMode**
</dt> <dd>

指出 **ONEX \_ 連接 \_ 設定檔** 結構是否包含 **authMode** 成員中的有效資料。

</dd> <dt>

**fHeldPeriod**
</dt> <dd>

指出 **ONEX \_ 連接 \_ 設定檔** 結構是否包含 **dwHeldPeriod** 成員中的有效資料。

</dd> <dt>

**fAuthPeriod**
</dt> <dd>

指出 **ONEX \_ 連接 \_ 設定檔** 結構是否包含 **dwAuthPeriod** 成員中的有效資料。

</dd> <dt>

**fStartPeriod**
</dt> <dd>

指出 **ONEX \_ 連接 \_ 設定檔** 結構是否包含 **dwStartPeriod** 成員中的有效資料。

</dd> <dt>

**fMaxStart**
</dt> <dd>

指出 **ONEX \_ 連接 \_ 設定檔** 結構是否包含 **dwMaxStart** 成員中的有效資料。

</dd> <dt>

**fMaxAuthFailures**
</dt> <dd>

指出 **ONEX \_ 連接 \_ 設定檔** 結構是否包含 **dwMaxAuthFailures** 成員中的有效資料。

</dd> <dt>

**fNetworkAuthTimeout**
</dt> <dd>

指出 **ONEX \_ 連接 \_ 設定檔** 結構是否包含 **dwNetworkAuthTimeout** 成員中的有效資料。

</dd> <dt>

**fAllowLogonDialogs**
</dt> <dd>

指出 **ONEX \_ 連接 \_ 設定檔** 結構是否包含 **bAllowLogonDialogs** 成員中的有效資料。

</dd> <dt>

**fNetworkAuthWithUITimeout**
</dt> <dd>

指出 **ONEX \_ 連接 \_ 設定檔** 結構是否包含 **dwNetworkAuthWithUITimeout** 成員中的有效資料。

</dd> <dt>

**fUserBasedVLan**
</dt> <dd>

指出 **ONEX \_ 連接 \_ 設定檔** 結構是否包含 **bUserBasedVLan** 成員中的有效資料。

</dd> <dt>

**dwOneXSupplicantFlags**
</dt> <dd>

可以存在於設定檔中的一組 802.1 X 旗標。 802.1 X 驗證模組會保留這些旗標供內部使用。

</dd> <dt>

**supplicantMode**
</dt> <dd>

802.1 X 架構中的 supplicantMode 元素，可指定用於 EAPOL-Start 訊息的傳輸方法。 如需詳細資訊，請參閱 802.1 X 配置中的 [**supplicantMode (OneX) 元素**](onexschema-supplicantmode-onex-element.md) 。



| 值                                                                                                                                                                                                                                                                                                                                               | 意義                                                                                                                                                                             |
|-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span id="OneXSupplicantModeInhibitTransmission"></span><span id="onexsupplicantmodeinhibittransmission"></span><span id="ONEXSUPPLICANTMODEINHIBITTRANSMISSION"></span><dl> <dt>**OneXSupplicantModeInhibitTransmission**</dt> <dt>0</dt> </dl> | EAPOL-Start 不會傳送訊息。 僅適用于有線局域網路設定檔。<br/>                                                                                             |
| <span id="OneXSupplicantModeLearn"></span><span id="onexsupplicantmodelearn"></span><span id="ONEXSUPPLICANTMODELEARN"></span><dl> <dt>**OneXSupplicantModeLearn**</dt> <dt>1</dt> </dl>                                                         | 用戶端會根據網路功能決定傳送 EAPOL-Start 封包的時機。 EAPOL-Start 訊息只會在必要時傳送。 僅適用于有線局域網路設定檔。<br/> |
| <span id="OneXSupplicantModeCompliant"></span><span id="onexsupplicantmodecompliant"></span><span id="ONEXSUPPLICANTMODECOMPLIANT"></span><dl> <dt>**OneXSupplicantModeCompliant**</dt> <dt>2</dt> </dl>                                         | EAPOL-Start 的訊息會由 802.1 X 所指定的方式傳輸。 適用于有線和無線局域網路設定檔。<br/>                                                             |



 

</dd> <dt>

**authMode**
</dt> <dd>

802.1 X 架構中的 authMode 元素，可指定用於 802.1 X 驗證的認證類型。 如需詳細資訊，請參閱 802.1 X 配置中的 [**authMode (OneX) 元素**](onexschema-authmode-onex-element.md) 。



| 值                                                                                                                                                                                                                                                                                               | 意義                                                                                                                                                                            |
|-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span id="OneXAuthModeMachineOrUser"></span><span id="onexauthmodemachineoruser"></span><span id="ONEXAUTHMODEMACHINEORUSER"></span><dl> <dt>**OneXAuthModeMachineOrUser**</dt> <dt>0</dt> </dl> | 使用電腦或使用者認證。 當使用者登入時，會使用使用者的認證進行驗證。 當使用者未登入時，會使用電腦認證。<br/> |
| <span id="OneXAuthModeMachineOnly"></span><span id="onexauthmodemachineonly"></span><span id="ONEXAUTHMODEMACHINEONLY"></span><dl> <dt>**OneXAuthModeMachineOnly**</dt> <dt>1</dt> </dl>         | 只使用電腦認證。<br/>                                                                                                                                           |
| <span id="OneXAuthModeUserOnly"></span><span id="onexauthmodeuseronly"></span><span id="ONEXAUTHMODEUSERONLY"></span><dl> <dt>**OneXAuthModeUserOnly**</dt> <dt>2</dt> </dl>                     | 僅使用使用者認證。<br/>                                                                                                                                              |
| <span id="OneXAuthModeGuest"></span><span id="onexauthmodeguest"></span><span id="ONEXAUTHMODEGUEST"></span><dl> <dt>**OneXAuthModeGuest**</dt> <dt>3</dt> </dl>                                 | 僅使用來賓 (空白) 認證。<br/>                                                                                                                                     |
| <span id="OneXAuthModeUnspecified"></span><span id="onexauthmodeunspecified"></span><span id="ONEXAUTHMODEUNSPECIFIED"></span><dl> <dt>**OneXAuthModeUnspecified**</dt> <dt>4</dt> </dl>         | 未指定要使用的認證。<br/>                                                                                                                                   |



 

</dd> <dt>

**dwHeldPeriod**
</dt> <dd>

802.1 X 架構中的 heldPeriod 專案，指定用戶端在驗證嘗試失敗之後不會重新嘗試驗證的時間長度（以秒為單位）。 如需詳細資訊，請參閱 802.1 X 配置中的 [**heldPeriod (OneX) 元素**](onexschema-heldperiod-onex-element.md) 。

</dd> <dt>

**dwAuthPeriod**
</dt> <dd>

802.1 X 架構中的 authPeriod 元素，可指定用戶端等候驗證器回應的時間長度上限（以秒為單位）。 如果在指定的期間內未收到回應，用戶端會假設網路上沒有任何驗證器存在。 如需詳細資訊，請參閱 802.1 X 配置中的 [**authPeriod (OneX) 元素**](onexschema-authperiod-onex-element.md) 。

</dd> <dt>

**dwStartPeriod**
</dt> <dd>

802.1 X 架構中的 startPeriod 元素，可指定傳送 EAPOL-Start 之前等候的時間長度（以秒為單位）。 傳送 EAPOL-Start 訊息以啟動 802.1 X 驗證程式。 如需詳細資訊，請參閱 802.1 X 配置中的 [**startPeriod (OneX) 元素**](onexschema-startperiod-onex-element.md) 。

</dd> <dt>

**dwMaxStart**
</dt> <dd>

802.1 X 架構中的 maxStart 元素，可指定傳送 EAPOL-Start 訊息的數目上限。 在傳送 EAPOL-Start 訊息的數目上限之後，用戶端會假設網路上沒有任何驗證器存在。 如需詳細資訊，請參閱 802.1 X 配置中的 [**maxStart (OneX) 元素**](onexschema-maxstart-onex-element.md) 。

</dd> <dt>

**dwMaxAuthFailures**
</dt> <dd>

802.1 X 架構中的 maxAuthFailures 元素，可指定一組認證所允許的驗證失敗次數上限。 如需詳細資訊，請參閱 802.1 X 架構中的 [**maxAuthFailures (OneX)**](onexschema-maxauthfailures-onex-element.md) 元素。

</dd> <dt>

**dwNetworkAuthTimeout**
</dt> <dd>

在正常登入進行之前等候 802.1 X 驗證完成的時間（以秒為單位）。 此值用於單一登入 (SSO) 案例。 在 802.1 X 設定檔中，此值會預設為10秒。 如需詳細資訊，請參閱 802.1 X 架構中的 [**maxDelay (singleSignOn) 元素**](onexschema-maxdelay-singlesignon-element.md) 。

</dd> <dt>

**dwNetworkAuthWithUITimeout**
</dt> <dd>

如果使用者介面對話方塊需要使用者輸入，則在每個登入的 SSO 中顯示時，等候連接的最長持續時間（以秒為單位）。

在 Windows Vista SP1 和更新版本上，此值會硬式編碼為10分鐘，且無法設定。 在 Windows Vista 發行至製造業時，此值在 802.1 X 設定檔中的預設值為60秒，而且是由架構中的 **maxDelayWithAdditionalDialogs** 元素所控制。

在 Windows Vista SP1 和更新版本中，會忽略並取代 802.1 X 架構中的 **maxDelayWithAdditionalDialogs** 元素。

</dd> <dt>

**bAllowLogonDialogs**
</dt> <dd>

值，指定是否允許在使用預先登錄 SSO 時顯示 EAP 對話方塊。 如需詳細資訊，請參閱 802.1 X 架構中的 **allowAdditionalDialogs** 元素。

</dd> <dt>

**bUserBasedVLan**
</dt> <dd>

802.1 X 架構中的 userBasedVirtualLan 元素，可指定裝置所使用的虛擬 LAN (VLAN) 是否會根據使用者的認證而變更。 有些網路存取伺服器 (NAS) 裝置會在使用者驗證之後變更 VLAN。 當 userBasedVirtualLan 為 TRUE 時，NAS 可能會在使用者驗證之後變更裝置的 VLAN。 如需詳細資訊，請參閱 802.1 X 配置中的 [**userBasedVirtualLan (singleSignOn) 元素**](onexschema-userbasedvirtuallan-singlesignon-element.md) 。

</dd> </dl>

## <a name="remarks"></a>備註

802.1 X 模組會使用 **ONEX 連線 \_ \_ 設定檔** 結構，這是 Windows Vista 和更新版本支援的新無線設定元件。

[**ONEX \_ 結果 \_ 更新 \_ 資料**](/windows/desktop/api/dot1x/ns-dot1x-onex_result_update_data)報含 802.1 x 驗證狀態變更的資訊。 當 [**wlan \_ 通知 \_ 資料**](/previous-versions/windows/desktop/legacy/ms706902(v=vs.85))結構的 **NotificationSource** 成員是 **wlan \_ 通知 \_ 來源 \_ ONEX** ，且收到通知之 **wlan \_ 通知 \_ 資料** 結構的 **NotificationCode** 成員為 **OneXNotificationTypeResultUpdate** 時，會傳回 **ONEX \_ 結果 \_ 更新 \_ 資料** 結構。 針對此通知， **WLAN \_ 通知 \_ 資料** 結構的 **.pdata** 成員會指向包含 802.1 x 驗證狀態變更相關資訊的 **ONEX \_ 結果 \_ 更新 \_ 資料** 結構。

如果已設定 [**onex \_ 結果 \_ 更新 \_ 資料**](/windows/desktop/api/dot1x/ns-dot1x-onex_result_update_data)結構中的 **fOneXAuthParams** 成員，則 **onex \_ 結果 \_ 更新 \_ 資料** 結構的 **AuthParams** 成員會包含一個 [**onex \_ 變數 \_ BLOB**](/windows/desktop/api/dot1x/ns-dot1x-onex_variable_blob)結構，其中包含從 **onex \_ 變數 \_ blob** 的 **dwOffset** 成員開始內嵌的 [**onex \_ AUTH \_ PARAMS**](/windows/desktop/api/dot1x/ns-dot1x-onex_auth_params)結構。 **Onex \_ AUTH \_ PARAMS** 結構的 **oneXConnProfile** 成員包含一個 **Onex \_ 變數 \_ BLOB** 結構，其中的 **Onex \_ 連接 \_ 設定檔** 結構是從 **onex \_ 變數 \_ blob** 的 **dwOffset** 成員開始。

在公用標頭檔中未定義 **ONEX \_ 連接 \_ 設定檔** 結構。

## <a name="requirements"></a>規格需求



| 需求 | 值 |
|-------------------------------------|------------------------------------------------------|
| 最低支援的用戶端<br/> | \[僅限 Windows Vista 桌面應用程式\]<br/>       |
| 最低支援的伺服器<br/> | 僅限 Windows Server 2008 \[ desktop 應用程式\]<br/> |



## <a name="see-also"></a>另請參閱

<dl> <dt>

[關於當的架構](about-the-acm-architecture.md)
</dt> <dt>

[OneX 架構](onexschema-schema.md)
</dt> <dt>

[**authMode (OneX) 元素**](onexschema-authmode-onex-element.md)
</dt> <dt>

[**authPeriod (OneX) 元素**](onexschema-authperiod-onex-element.md)
</dt> <dt>

[**heldPeriod (OneX) 元素**](onexschema-heldperiod-onex-element.md)
</dt> <dt>

[**maxAuthFailures (OneX)**](onexschema-maxauthfailures-onex-element.md)
</dt> <dt>

[**maxStart (OneX) 元素**](onexschema-maxstart-onex-element.md)
</dt> <dt>

[**startPeriod (OneX) 元素**](onexschema-startperiod-onex-element.md)
</dt> <dt>

[**supplicantMode (OneX) 元素**](onexschema-supplicantmode-onex-element.md)
</dt> <dt>

[**userBasedVirtualLan (singleSignOn) 元素**](onexschema-userbasedvirtuallan-singlesignon-element.md)
</dt> <dt>

[**ONEX \_ AUTH \_ 參數**](/windows/desktop/api/dot1x/ns-dot1x-onex_auth_params)
</dt> <dt>

[**ONEX \_ 通知 \_ 類型**](/windows/desktop/api/dot1x/ne-dot1x-onex_notification_type)
</dt> <dt>

[**ONEX \_ 結果 \_ 更新 \_ 資料**](/windows/desktop/api/dot1x/ns-dot1x-onex_result_update_data)
</dt> <dt>

[**OneX 架構元素**](onexschema-onex-element.md)
</dt> <dt>

[**ONEX \_ 變數 \_ BLOB**](/windows/desktop/api/dot1x/ns-dot1x-onex_variable_blob)
</dt> <dt>

[**WLAN \_ 通知 \_ 資料**](/previous-versions/windows/desktop/legacy/ms706902(v=vs.85))
</dt> <dt>

[**WlanRegisterNotification**](/windows/desktop/api/wlanapi/nf-wlanapi-wlanregisternotification)
</dt> </dl>

 

 
