---
description: 代表網路介面卡的邏輯連接點。 當 Wi-Fi 端點連線到交換器埠時，連接到 Wi-Fi 端點的網路介面卡具有網路連線能力。
ms.assetid: 66ed1503-9c11-4a51-a3a5-21e5d7021197
title: Msvm_WiFiEndpoint 類別
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Msvm_WiFiEndpoint
- Msvm_WiFiEndpoint.RequestStateChange
- Msvm_WiFiEndpoint.InstanceID
- Msvm_WiFiEndpoint.Caption
- Msvm_WiFiEndpoint.Description
- Msvm_WiFiEndpoint.ElementName
- Msvm_WiFiEndpoint.InstallDate
- Msvm_WiFiEndpoint.Name
- Msvm_WiFiEndpoint.OperationalStatus
- Msvm_WiFiEndpoint.StatusDescriptions
- Msvm_WiFiEndpoint.Status
- Msvm_WiFiEndpoint.HealthState
- Msvm_WiFiEndpoint.CommunicationStatus
- Msvm_WiFiEndpoint.DetailedStatus
- Msvm_WiFiEndpoint.OperatingStatus
- Msvm_WiFiEndpoint.PrimaryStatus
- Msvm_WiFiEndpoint.EnabledState
- Msvm_WiFiEndpoint.OtherEnabledState
- Msvm_WiFiEndpoint.RequestedState
- Msvm_WiFiEndpoint.EnabledDefault
- Msvm_WiFiEndpoint.TimeOfLastStateChange
- Msvm_WiFiEndpoint.AvailableRequestedStates
- Msvm_WiFiEndpoint.TransitioningToState
- Msvm_WiFiEndpoint.SystemCreationClassName
- Msvm_WiFiEndpoint.SystemName
- Msvm_WiFiEndpoint.CreationClassName
- Msvm_WiFiEndpoint.NameFormat
- Msvm_WiFiEndpoint.ProtocolType
- Msvm_WiFiEndpoint.ProtocolIFType
- Msvm_WiFiEndpoint.OtherTypeDescription
- Msvm_WiFiEndpoint.LANID
- Msvm_WiFiEndpoint.LANType
- Msvm_WiFiEndpoint.OtherLANType
- Msvm_WiFiEndpoint.MACAddress
- Msvm_WiFiEndpoint.AliasAddresses
- Msvm_WiFiEndpoint.GroupAddresses
- Msvm_WiFiEndpoint.MaxDataSize
- Msvm_WiFiEndpoint.Connected
- Msvm_WiFiEndpoint.EncryptionMethod
- Msvm_WiFiEndpoint.OtherEncryptionMethod
- Msvm_WiFiEndpoint.AuthenticationMethod
- Msvm_WiFiEndpoint.OtherAuthenticationMethod
- Msvm_WiFiEndpoint.IEEE8021xAuthenticationProtocol
- Msvm_WiFiEndpoint.AccessPointAddress
- Msvm_WiFiEndpoint.BSSType
- Msvm_WiFiEndpoint.Associated
api_type:
- DllExport
api_location:
- vmms.exe
ms.openlocfilehash: f4a0a287d85b7a229b0e8e50a10c402fca734429
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/07/2021
ms.locfileid: "103943385"
---
# <a name="msvm_wifiendpoint-class"></a>Msvm \_ WiFiEndpoint 類別

代表網路介面卡的邏輯連接點。 當 Wi-Fi 端點連線到交換器埠時，連接到 Wi-Fi 端點的網路介面卡具有網路連線能力。

下列語法已簡化受控物件格式 (MOF) 程式碼，並且包含所有繼承的屬性。

## <a name="syntax"></a>語法

``` syntax
[Dynamic, Provider("VmmsWmiInstanceAndMethodProvider"), AMENDMENT]
class Msvm_WiFiEndpoint : CIM_WiFiEndpoint
{
  string   InstanceID;
  string   Caption;
  string   Description;
  string   ElementName;
  datetime InstallDate;
  string   Name;
  uint16   OperationalStatus[];
  string   StatusDescriptions[];
  string   Status;
  uint16   HealthState;
  uint16   CommunicationStatus;
  uint16   DetailedStatus;
  uint16   OperatingStatus;
  uint16   PrimaryStatus;
  uint16   EnabledState;
  string   OtherEnabledState;
  uint16   RequestedState;
  uint16   EnabledDefault = 2;
  datetime TimeOfLastStateChange;
  uint16   AvailableRequestedStates[];
  uint16   TransitioningToState;
  string   SystemCreationClassName;
  string   SystemName;
  string   CreationClassName;
  string   NameFormat;
  uint16   ProtocolType;
  uint16   ProtocolIFType = 71;
  string   OtherTypeDescription;
  string   LANID;
  uint16   LANType;
  string   OtherLANType;
  string   MACAddress;
  string   AliasAddresses[];
  string   GroupAddresses[];
  uint32   MaxDataSize;
  boolean  Connected;
  uint16   EncryptionMethod;
  string   OtherEncryptionMethod;
  uint16   AuthenticationMethod;
  string   OtherAuthenticationMethod;
  uint16   IEEE8021xAuthenticationProtocol;
  string   AccessPointAddress;
  uint16   BSSType;
  boolean  Associated;
};
```

## <a name="members"></a>成員

**Msvm \_ WiFiEndpoint** 類別具有下列類型的成員：

-   [方法](#methods)
-   [屬性](#properties)

### <a name="methods"></a>方法

**Msvm \_ WiFiEndpoint** 類別具有這些方法。



| 方法                 | 描述                              |
|:-----------------------|:-----------------------------------------|
| **RequestStateChange** | 不支援這個方法。<br/> |



 

### <a name="properties"></a>屬性

**Msvm \_ WiFiEndpoint** 類別具有這些屬性。

<dl> <dt>

**AccessPointAddress**
</dt> <dd> <dl> <dt>

資料類型： **字串**
</dt> <dt>

存取類型：唯讀
</dt> </dl>

包含目前與 Wi-Fi 端點相關聯之存取點的 MAC 位址。 如果 Wi-Fi 端點目前沒有相關聯，則 **AccessPointAddress** 應該是 **Null**。 MAC 位址的格式應為12個十六進位數位 (例如 "010203040506" ) ，每一組代表以標準位 (順序表示之 MAC 位址的六個八位八位組中的其中一個（例如，在字串) 的第一個字元的低序位位中找到群組位址位）。

</dd> <dt>

**AliasAddresses**
</dt> <dd> <dl> <dt>

資料類型： **字串** 陣列
</dt> <dt>

存取類型：唯讀
</dt> </dl>

可能用來與 LAN 端點通訊的其他單播位址。 這個屬性繼承自 [**CIM \_ LANEndpoint**](/previous-versions//cc136865(v=vs.85))。

</dd> <dt>

**相關聯**
</dt> <dd> <dl> <dt>

資料類型： **布林值**
</dt> <dt>

存取類型：唯讀
</dt> </dl>

指出 Wi-Fi 端點目前是否與存取點或用戶端相關聯。

如果 Wi-Fi 端點與存取點或用戶端工作站相關聯，則會包含 **True** ;否則 **為 False**。

</dd> <dt>

**AuthenticationMethod**
</dt> <dd> <dl> <dt>

資料類型： **uint16**
</dt> <dt>

存取類型：唯讀
</dt> </dl>

指定用來驗證 Wi-Fi 端點和網路彼此的方法。

<dl> <dt>

<span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>**未知** 的 (0) 
</dt> <dt>

<span id="Other"></span><span id="other"></span><span id="OTHER"></span>**其他** (1) 
</dt> <dt>

<span id="Open_System"></span><span id="open_system"></span><span id="OPEN_SYSTEM"></span>**開啟 System** (2) 
</dt> <dt>

<span id="Shared_Key"></span><span id="shared_key"></span><span id="SHARED_KEY"></span>**共用金鑰** (3) 
</dt> <dt>

<span id="WPA_PSK"></span><span id="wpa_psk"></span>**WPA PSK** (4) 
</dt> <dt>

<span id="WPA_IEEE_802.1x"></span><span id="wpa_ieee_802.1x"></span><span id="WPA_IEEE_802.1X"></span>**WPA IEEE 802.1 x** (5) 
</dt> <dt>

<span id="WPA2_PSK"></span><span id="wpa2_psk"></span>**WPA2 PSK** (6) 
</dt> <dt>

<span id="WPA2_IEEE_802.1x"></span><span id="wpa2_ieee_802.1x"></span><span id="WPA2_IEEE_802.1X"></span>**WPA2 IEEE 802.1 x** (7) 
</dt> <dt>

<span id="CCKM_IEEE_802.1x"></span><span id="cckm_ieee_802.1x"></span><span id="CCKM_IEEE_802.1X"></span>**CCKM IEEE 802.1 x** (8) 
</dt> <dt>

<span id="DMTF_Reserved_"></span><span id="dmtf_reserved_"></span><span id="DMTF_RESERVED_"></span>**DMTF 保留** (9。 )
</dt> </dl>

</dd> <dt>

**AvailableRequestedStates**
</dt> <dd> <dl> <dt>

資料類型： **uint16** 陣列
</dt> <dt>

存取類型：唯讀
</dt> </dl>

指出用於起始狀態變更之 [**RequestStateChange**](/previous-versions/windows/desktop/iscsitarg/requeststatechange-cim-enabledlogicalelement)方法的 *RequestedState* 參數可能的值。 列出的值將會是與 **cim \_ EnabledLogicalElementCapabilities** 相關聯的實例之 **RequestedStatesSupported** 屬性中所含值的子集，其中選取的值是 [**cim \_ EnabledLogicalElement**](/previous-versions//cc136818(v=vs.85))目前狀態的函式。 如果實作為目前狀態的函式，則這個屬性可以是非 **Null** 的值。 如果實作為目前狀態的函式無法判斷可能的值集，這個屬性將會是 **Null** 。

這個屬性繼承自 [**CIM \_ EnabledLogicalElement**](/previous-versions//cc136818(v=vs.85))。

<dl> <dt>

<span id="Enabled"></span><span id="enabled"></span><span id="ENABLED"></span>**已啟用** (2) 
</dt> <dt>

<span id="Disabled"></span><span id="disabled"></span><span id="DISABLED"></span>**停用** (3) 
</dt> <dt>

<span id="Shut_Down"></span><span id="shut_down"></span><span id="SHUT_DOWN"></span>**關機** (4) 
</dt> <dt>

<span id="Offline"></span><span id="offline"></span><span id="OFFLINE"></span>**離線** (6) 
</dt> <dt>

<span id="Test"></span><span id="test"></span><span id="TEST"></span>**測試** (7) 
</dt> <dt>

<span id="Defer"></span><span id="defer"></span><span id="DEFER"></span>**延** 後 (8) 
</dt> <dt>

<span id="Quiesce"></span><span id="quiesce"></span><span id="QUIESCE"></span>**靜止** (9) 
</dt> <dt>

<span id="Reboot"></span><span id="reboot"></span><span id="REBOOT"></span>**重新開機** (10) 
</dt> <dt>

<span id="Reset"></span><span id="reset"></span><span id="RESET"></span>**重設** (11) 
</dt> <dt>

<span id="DMTF_Reserved_"></span><span id="dmtf_reserved_"></span><span id="DMTF_RESERVED_"></span>**DMTF 保留** ( .。。 )
</dt> </dl>

</dd> <dt>

**BSSType**
</dt> <dd> <dl> <dt>

資料類型： **uint16**
</dt> <dt>

存取類型：唯讀
</dt> </dl>

指出對應至實例之網路的基本服務集 (BSS) 類型。 基本服務集是由單一協調功能所控制的一組工作站。



| 值                                                                                                                                                                                                                                                      | 意義                                                                            |
|------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|------------------------------------------------------------------------------------|
| <span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span><dl> <dt>**未知**</dt>的 <dt>0</dt> </dl>                                |                                                                                    |
| <span id="Independent"></span><span id="independent"></span><span id="INDEPENDENT"></span><dl> <dt>**獨立**</dt> <dt>2</dt> </dl>                | Wi-Fi 端點會直接關聯至另一個用戶端工作站。<br/>    |
| <span id="Infrastructure"></span><span id="infrastructure"></span><span id="INFRASTRUCTURE"></span><dl> <dt>**基礎結構**</dt> <dt>3</dt> </dl>    | Wi-Fi 端點會使用存取點與網路相關聯。<br/> |
| <span id="DMTF_Reserved_"></span><span id="dmtf_reserved_"></span><span id="DMTF_RESERVED_"></span><dl> <dt> **DMTF 保留**</dt> <dt>4。</dt> </dl> |                                                                                    |



 

</dd> <dt>

**標題**
</dt> <dd> <dl> <dt>

資料類型： **字串**
</dt> <dt>

存取類型：唯讀
</dt> </dl>

物件的簡短描述。 這個屬性繼承自 [**CIM \_ ManagedElement**](/previous-versions/windows/desktop/iscsitarg/cim-managedelement)。

</dd> <dt>

**CommunicationStatus**
</dt> <dd> <dl> <dt>

資料類型： **uint16**
</dt> <dt>

存取類型：唯讀
</dt> </dl>

指出檢測與基礎受管理元素通訊的能力。 **Null** 值表示不會執行此屬性。 這個屬性繼承自 [**CIM \_ ManagedSystemElement**](/windows/desktop/CIMWin32Prov/cim-managedsystemelement)。

</dd> <dt>

**已連接**
</dt> <dd> <dl> <dt>

資料類型： **布林值**
</dt> <dt>

存取類型：唯讀
</dt> </dl>

如果 Wi-Fi 端點連接到交換器埠，這個屬性會設定為 **True** 。

</dd> <dt>

**CreationClassName**
</dt> <dd> <dl> <dt>

資料類型： **字串**
</dt> <dt>

存取類型：唯讀
</dt> <dt>

限定詞： **Key**、 **MaxLen** ( 256 ) 
</dt> </dl>

建立實例時所使用之類別或子類別的名稱。 這個屬性繼承自 [**CIM \_ ServiceAccessPoint**](/windows/desktop/CIMWin32Prov/cim-serviceaccesspoint)。

</dd> <dt>

**說明**
</dt> <dd> <dl> <dt>

資料類型： **字串**
</dt> <dt>

存取類型：唯讀
</dt> </dl>

對物件的描述。 這個屬性繼承自 [**CIM \_ ManagedElement**](/previous-versions/windows/desktop/iscsitarg/cim-managedelement)。

</dd> <dt>

**DetailedStatus**
</dt> <dd> <dl> <dt>

資料類型： **uint16**
</dt> <dt>

存取類型：唯讀
</dt> </dl>

補充具有其他狀態詳細資料的 **PrimaryStatus** 屬性。 **Null** 值表示不會執行此屬性。 這個屬性繼承自 [**CIM \_ ManagedSystemElement**](/windows/desktop/CIMWin32Prov/cim-managedsystemelement)。

</dd> <dt>

**ElementName**
</dt> <dd> <dl> <dt>

資料類型： **字串**
</dt> <dt>

存取類型：唯讀
</dt> </dl>

物件的顯示名稱。 這個屬性繼承自 [**CIM \_ ManagedElement**](/previous-versions/windows/desktop/iscsitarg/cim-managedelement)。

</dd> <dt>

**EnabledDefault**
</dt> <dd> <dl> <dt>

資料類型： **uint16**
</dt> <dt>

存取類型：唯讀
</dt> </dl>

系統管理員的預設或啟動設定，適用于元素的啟用狀態。 這個屬性會繼承自 [**CIM \_ EnabledLogicalElement**](/previous-versions//cc136818(v=vs.85)) ，而且會是下列其中一個值。

<dl> <dt>

<span id="Enabled"></span><span id="enabled"></span><span id="ENABLED"></span>**已啟用** (2) 
</dt> <dt>

<span id="Disabled"></span><span id="disabled"></span><span id="DISABLED"></span>**停用** (3) 
</dt> <dt>

<span id="Enabled_but_Offline"></span><span id="enabled_but_offline"></span><span id="ENABLED_BUT_OFFLINE"></span>**已啟用但離線** (6) 
</dt> </dl>

</dd> <dt>

**EnabledState**
</dt> <dd> <dl> <dt>

資料類型： **uint16**
</dt> <dt>

存取類型：唯讀
</dt> </dl>

指定已規劃系統的啟用狀態。 這個屬性繼承自 [**CIM \_ EnabledLogicalElement**](/previous-versions//cc136818(v=vs.85))，它可以是下列值之一。



| 值                                                                                                                                                                                                                                                                       | 意義                                                                          |
|-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|----------------------------------------------------------------------------------|
| <span id="Disabled"></span><span id="disabled"></span><span id="DISABLED"></span><dl> <dt>**停用**</dt> <dt>3</dt> </dl>                                             | 系統已關閉。<br/>                                             |
| <span id="Not_Applicable"></span><span id="not_applicable"></span><span id="NOT_APPLICABLE"></span><dl> <dt>**不適用**</dt> <dt>5</dt> </dl>                     | 元素不支援啟用或停用。<br/>               |
| <span id="Enabled_but_Offline"></span><span id="enabled_but_offline"></span><span id="ENABLED_BUT_OFFLINE"></span><dl> <dt>**已啟用但離線**</dt> <dt>6</dt> </dl> | 系統已啟用但離線。 將會捨棄任何新的要求。<br/> |



 

</dd> <dt>

**EncryptionMethod**
</dt> <dd> <dl> <dt>

資料類型： **uint16**
</dt> <dt>

存取類型：唯讀
</dt> </dl>

指定用來保護 Wi-Fi 端點所傳送和接收之資料機密性的加密方法。

<dl> <dt>

<span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>**未知** 的 (0) 
</dt> <dt>

<span id="Other"></span><span id="other"></span><span id="OTHER"></span>**其他** (1) 
</dt> <dt>

<span id="WEP"></span><span id="wep"></span>**WEP** (2) 
</dt> <dt>

<span id="TKIP"></span><span id="tkip"></span>**TKIP** (3) 
</dt> <dt>

<span id="CCMP"></span><span id="ccmp"></span>**CCMP** (4) 
</dt> <dt>

<span id="None"></span><span id="none"></span><span id="NONE"></span>**無** (5) 
</dt> <dt>

<span id="DMTF_Reserved_"></span><span id="dmtf_reserved_"></span><span id="DMTF_RESERVED_"></span>**DMTF 保留** (6。 )
</dt> </dl>

</dd> <dt>

**GroupAddresses**
</dt> <dd> <dl> <dt>

資料類型： **字串** 陣列
</dt> <dt>

存取類型：唯讀
</dt> </dl>

LAN 端點接聽的多播位址。 這個屬性繼承自 [**CIM \_ LANEndpoint**](/previous-versions//cc136865(v=vs.85))。

</dd> <dt>

**HealthState**
</dt> <dd> <dl> <dt>

資料類型： **uint16**
</dt> <dt>

存取類型：唯讀
</dt> </dl>

專案目前的健康情況。 這個屬性會表示此元素的健全狀況，但不一定是它的子元件。 可能的值為0到30，其中5表示元素完全狀況良好，而30表示元素完全無法正常運作。 這個屬性繼承自 [**CIM \_ ManagedSystemElement**](/windows/desktop/CIMWin32Prov/cim-managedsystemelement)。

</dd> <dt>

**IEEE8021xAuthenticationProtocol**
</dt> <dd> <dl> <dt>

資料類型： **uint16**
</dt> <dt>

存取類型：唯讀
</dt> </dl>

包含可延伸的驗證通訊協定 (EAP) 類型，只有在 **AuthenticationMethod** 包含 5 (WPA ieee 802.1 x) 、7 (WPA2 ieee 802.1 x) 或 8 (CCKM ieee 802.1 x) 時才適用。

<dl> <dt>

<span id="EAP-TLS"></span><span id="eap-tls"></span>**Eap-tls** (0) 
</dt> <dt>

<span id="EAP-TTLS_MSCHAPv2"></span><span id="eap-ttls_mschapv2"></span><span id="EAP-TTLS_MSCHAPV2"></span>**EAP-TTLS/eap-mschapv2** (1) 
</dt> <dt>

<span id="PEAPv0_EAP-MSCHAPv2"></span><span id="peapv0_eap-mschapv2"></span><span id="PEAPV0_EAP-MSCHAPV2"></span>**PEAPv0/EAP-eap-mschapv2** (2) 
</dt> <dt>

<span id="PEAPv1_EAP-GTC"></span><span id="peapv1_eap-gtc"></span><span id="PEAPV1_EAP-GTC"></span>**PEAPv1/EAP-GTC** (3) 
</dt> <dt>

<span id="EAP-FAST_MSCHAPv2"></span><span id="eap-fast_mschapv2"></span><span id="EAP-FAST_MSCHAPV2"></span>**Eap-fast/eap-mschapv2** (4) 
</dt> <dt>

<span id="EAP-FAST_GTC"></span><span id="eap-fast_gtc"></span>**Eap-fast/GTC** (5) 
</dt> <dt>

<span id="EAP-MD5"></span><span id="eap-md5"></span>**EAP-MD5** (6) 
</dt> <dt>

<span id="EAP-PSK"></span><span id="eap-psk"></span>**Eap-tls** (7) 
</dt> <dt>

<span id="EAP-SIM"></span><span id="eap-sim"></span>**EAP-SIM** (8) 
</dt> <dt>

<span id="EAP-AKA"></span><span id="eap-aka"></span>**EAP-也稱為** (9) 
</dt> <dt>

<span id="EAP-FAST_TLS"></span><span id="eap-fast_tls"></span>**Eap-fast/TLS** (10) 
</dt> <dt>

<span id="DMTF_Reserved_"></span><span id="dmtf_reserved_"></span><span id="DMTF_RESERVED_"></span>**DMTF 保留** (11 )
</dt> </dl>

</dd> <dt>

**InstallDate**
</dt> <dd> <dl> <dt>

資料類型： **datetime**
</dt> <dt>

存取類型：唯讀
</dt> </dl>

建立虛擬機器設定的日期和時間。 這個屬性繼承自 [**CIM \_ ManagedSystemElement**](/windows/desktop/CIMWin32Prov/cim-managedsystemelement)。

</dd> <dt>

**InstanceID**
</dt> <dd> <dl> <dt>

資料類型： **字串**
</dt> <dt>

存取類型：唯讀
</dt> <dt>

限定詞：索引 **鍵**
</dt> </dl>

唯一識別此類別的實例。 這個屬性繼承自 [**CIM \_ ManagedElement**](/previous-versions/windows/desktop/iscsitarg/cim-managedelement)。

</dd> <dt>

**LANID**
</dt> <dd> <dl> <dt>

資料類型： **字串**
</dt> <dt>

存取類型：唯讀
</dt> </dl>

端點所連接之 LAN 區段的標籤或識別碼。 如果端點目前非使用中/已連線，或這項資訊未知，則這個屬性會是 **Null**。 這個屬性繼承自 [**CIM \_ LANEndpoint**](/previous-versions//cc136865(v=vs.85))。

</dd> <dt>

**LANType**
</dt> <dd> <dl> <dt>

資料類型： **uint16**
</dt> <dt>

存取類型：唯讀
</dt> </dl>

這個屬性已被取代，代替 **ProtocolType** 屬性。 這個屬性繼承自 [**CIM \_ LANEndpoint**](/previous-versions//cc136865(v=vs.85))。

</dd> <dt>

**MACAddress**
</dt> <dd> <dl> <dt>

資料類型： **字串**
</dt> <dt>

存取類型：唯讀
</dt> <dt>

限定詞： **MaxLen** ( 12 ) 
</dt> </dl>

與 LAN 端點通訊時使用的 MAC 位址。 MAC 位址的格式為十二個十六進位數位 (例如 "010203040506" ) ，其中每一組代表根據 RFC 2469 的標準位順序，其中一個 MAC 位址的六個八位。 這個屬性繼承自 [**CIM \_ LANEndpoint**](/previous-versions//cc136865(v=vs.85))。

</dd> <dt>

**MaxDataSize**
</dt> <dd> <dl> <dt>

資料類型： **uint32**
</dt> <dt>

存取類型：唯讀
</dt> <dt>

限定詞： **單位** ( "Bits" ) 
</dt> </dl>

LAN 端點可能傳送或接收之資訊欄位的最大大小（以位數為單位）。 這個屬性繼承自 [**CIM \_ LANEndpoint**](/previous-versions//cc136865(v=vs.85))。

</dd> <dt>

**名稱**
</dt> <dd> <dl> <dt>

資料類型： **字串**
</dt> <dt>

存取類型：唯讀
</dt> </dl>

已知物件的標籤。 這個屬性繼承自 [**CIM \_ ManagedSystemElement**](/windows/desktop/CIMWin32Prov/cim-managedsystemelement)。

</dd> <dt>

**NameFormat**
</dt> <dd> <dl> <dt>

資料類型： **字串**
</dt> <dt>

存取類型：唯讀
</dt> <dt>

限定詞： **MaxLen** ( 256 ) 
</dt> </dl>

包含已選取的命名啟發式，以確保 **Name** 屬性的值是唯一的。 這個屬性繼承自 [**CIM \_ ProtocolEndpoint**](/previous-versions/windows/desktop/iscsitarg/cim-protocolendpoint)。

</dd> <dt>

**OperatingStatus**
</dt> <dd> <dl> <dt>

資料類型： **uint16**
</dt> <dt>

存取類型：唯讀
</dt> </dl>

提供專案操作條件的目前狀態資訊，並可用於提供關於 **EnabledState** 屬性值的詳細資料。 **Null** 值表示不會執行此屬性。 這個屬性繼承自 [**CIM \_ ManagedSystemElement**](/windows/desktop/CIMWin32Prov/cim-managedsystemelement)。

</dd> <dt>

**OperationalStatus**
</dt> <dd> <dl> <dt>

資料類型： **uint16** 陣列
</dt> <dt>

存取類型：唯讀
</dt> </dl>

物件的目前狀態。 這個屬性繼承自 [**CIM \_ ManagedSystemElement**](/windows/desktop/CIMWin32Prov/cim-managedsystemelement)。

</dd> <dt>

**OtherAuthenticationMethod**
</dt> <dd> <dl> <dt>

資料類型： **字串**
</dt> <dt>

存取類型：唯讀
</dt> </dl>

只有當 **AuthenticationMethod** 包含 1 (其他) 時，才會指定802.11 驗證方法。 此字串的格式為廠商專屬。

</dd> <dt>

**OtherEnabledState**
</dt> <dd> <dl> <dt>

資料類型： **字串**
</dt> <dt>

存取類型：唯讀
</dt> </dl>

描述當 **EnabledState** 屬性設定為 1 ( "Other" ) 時，專案已啟用或停用狀態的字串。 當 **EnabledState** 是1以外的任何值時，這個屬性必須設定為 **Null** 。 這個屬性繼承自 [**CIM \_ EnabledLogicalElement**](/previous-versions//cc136818(v=vs.85))。

</dd> <dt>

**OtherEncryptionMethod**
</dt> <dd> <dl> <dt>

資料類型： **字串**
</dt> <dt>

存取類型：唯讀
</dt> </dl>

只有在 **EncryptionMethod** 包含 1 (其他) 時，才會指定802.11 加密方法。 此字串的格式為廠商專屬。

</dd> <dt>

**OtherLANType**
</dt> <dd> <dl> <dt>

資料類型： **字串**
</dt> <dt>

存取類型：唯讀
</dt> </dl>

這個屬性已被取代，代替 **OtherTypeDescription** 屬性。 這個屬性繼承自 [**CIM \_ LANEndpoint**](/previous-versions//cc136865(v=vs.85))。

</dd> <dt>

**OtherTypeDescription**
</dt> <dd> <dl> <dt>

資料類型： **字串**
</dt> <dt>

存取類型：唯讀
</dt> <dt>

限定詞： **MaxLen** ( 64 ) 
</dt> </dl>

描述當這個類別的 **ProtocolIFType** 屬性 (或其任何子類別) 設定為 1 (其他) 時，通訊協定端點型別的字串。 當 **ProtocolIFType** 屬性是1以外的任何值時，這個屬性應該設為 **Null** 。 這個屬性繼承自 [**CIM \_ ProtocolEndpoint**](/previous-versions/windows/desktop/iscsitarg/cim-protocolendpoint)。

</dd> <dt>

**PrimaryStatus**
</dt> <dd> <dl> <dt>

資料類型： **uint16**
</dt> <dt>

存取類型：唯讀
</dt> </dl>

提供高層級的狀態資訊。 這個屬性應該與 **DetailedStatus** 屬性一起使用，以提供元素和其子元件的高階和詳細健全狀況狀態資訊。 **Null** 值表示不會執行此屬性。 這個屬性繼承自 [**CIM \_ ManagedSystemElement**](/windows/desktop/CIMWin32Prov/cim-managedsystemelement)。

</dd> <dt>

**ProtocolIFType**
</dt> <dd> <dl> <dt>

資料類型： **uint16**
</dt> <dt>

存取類型：唯讀
</dt> </dl>

屬性是用來分類和分類這個類別的實例。 如果 **ProtocolIFType** 設定為 1 (其他) ，則應該在 **OtherTypeDescription** 屬性中提供類型資訊。 這個屬性繼承自 [**CIM \_ ProtocolEndpoint**](/previous-versions/windows/desktop/iscsitarg/cim-protocolendpoint)。

> [!Note]  
> **ProtocolIFType** 是與 [IANA ifType MIB](https://www.iana.org/assignments/ianaiftype-mib)同步的列舉。 也會包含其他以 DMTF 定義的值。

 

<dl> <dt>

<span id="Other"></span><span id="other"></span><span id="OTHER"></span>**其他** (1) 
</dt> <dt>

<span id="IEEE_802.11"></span><span id="ieee_802.11"></span>**IEEE 802.11** (71) 
</dt> <dt>

<span id="IANA_Reserved"></span><span id="iana_reserved"></span><span id="IANA_RESERVED"></span>**IANA 保留** (225. 4095) 
</dt> <dt>

<span id="DMTF_Reserved"></span><span id="dmtf_reserved"></span><span id="DMTF_RESERVED"></span>**DMTF 保留** 的 (a334-18f799d361d1. 32767) 
</dt> <dt>

<span id="Vendor_Reserved_"></span><span id="vendor_reserved_"></span><span id="VENDOR_RESERVED_"></span>**廠商保留** (32768。 )
</dt> </dl>

</dd> <dt>

**ProtocolType**
</dt> <dd> <dl> <dt>

資料類型： **uint16**
</dt> <dt>

存取類型：唯讀
</dt> </dl>

這個屬性已被取代，代替 **ProtocolIFType** 屬性。 這個屬性繼承自 [**CIM \_ ProtocolEndpoint**](/previous-versions/windows/desktop/iscsitarg/cim-protocolendpoint)。

</dd> <dt>

**RequestedState**
</dt> <dd> <dl> <dt>

資料類型： **uint16**
</dt> <dt>

存取類型：唯讀
</dt> </dl>

上次要求或預期的管理服務狀態。 這個屬性繼承自 [**CIM \_ EnabledLogicalElement**](/previous-versions//cc136818(v=vs.85))。

</dd> <dt>

**狀態**
</dt> <dd> <dl> <dt>

資料類型： **字串**
</dt> <dt>

存取類型：唯讀
</dt> </dl>

描述元素的狀態。 這個屬性繼承自 [**CIM \_ ManagedSystemElement**](/windows/desktop/CIMWin32Prov/cim-managedsystemelement)。

正常

錯誤

降級

不明

「Pred 失敗」

入門

從而

維護

強調

"NonRecover"

「無連絡人」

「遺失通訊」

</dd> <dt>

**StatusDescriptions**
</dt> <dd> <dl> <dt>

資料類型： **字串** 陣列
</dt> <dt>

存取類型：唯讀
</dt> </dl>

描述各種 **OperationalStatus** 陣列值的字串。 這個屬性繼承自 [**CIM \_ ManagedSystemElement**](/windows/desktop/CIMWin32Prov/cim-managedsystemelement)。

</dd> <dt>

**SystemCreationClassName**
</dt> <dd> <dl> <dt>

資料類型： **字串**
</dt> <dt>

存取類型：唯讀
</dt> </dl>

裝載系統的建立類別名稱。 這個屬性繼承自 [**CIM \_ ServiceAccessPoint**](/windows/desktop/CIMWin32Prov/cim-serviceaccesspoint)。

</dd> <dt>

**SystemName**
</dt> <dd> <dl> <dt>

資料類型： **字串**
</dt> <dt>

存取類型：唯讀
</dt> <dt>

限定詞： **Key**、 **MaxLen** ( 256 ) 
</dt> </dl>

主控系統的名稱。 這個屬性繼承自 [**CIM \_ ServiceAccessPoint**](/windows/desktop/CIMWin32Prov/cim-serviceaccesspoint)。

</dd> <dt>

**TimeOfLastStateChange**
</dt> <dd> <dl> <dt>

資料類型： **datetime**
</dt> <dt>

存取類型：唯讀
</dt> </dl>

專案的已啟用狀態上次變更的日期和時間。 這個屬性繼承自 [**CIM \_ EnabledLogicalElement**](/previous-versions//cc136818(v=vs.85))。

</dd> <dt>

**TransitioningToState**
</dt> <dd> <dl> <dt>

資料類型： **uint16**
</dt> <dt>

存取類型：唯讀
</dt> </dl>

指出實例正在轉換的目標狀態。 這個屬性繼承自 [**CIM \_ EnabledLogicalElement**](/previous-versions//cc136818(v=vs.85))。

</dd> </dl>

## <a name="requirements"></a>規格需求



| 需求 | 值 |
|-------------------------------------|---------------------------------------------------------------------------------------------------------|
| 最低支援的用戶端<br/> | \[僅 Windows 8 桌面應用程式\]<br/>                                                              |
| 最低支援的伺服器<br/> | 僅限 Windows Server 2012 \[ desktop 應用程式\]<br/>                                                    |
| 命名空間<br/>                | 根 \\ 虛擬化 \\ V2<br/>                                                                     |
| MOF<br/>                      | <dl> <dt>WindowsVirtualization。</dt> </dl> |
| DLL<br/>                      | <dl> <dt>Vmms.exe</dt> </dl>                     |



 

