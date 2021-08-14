---
description: 代表可系結至虛擬交換器的實體 Wi-Fi (802.11) 網路介面卡，以提供虛擬機器的外部網路連線能力。
ms.assetid: c6dae491-607c-4f17-aea9-162d910120c2
title: Msvm_WiFiPort 類別
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Msvm_WiFiPort
- Msvm_WiFiPort.RequestStateChange
- Msvm_WiFiPort.SetPowerState
- Msvm_WiFiPort.Reset
- Msvm_WiFiPort.EnableDevice
- Msvm_WiFiPort.OnlineDevice
- Msvm_WiFiPort.QuiesceDevice
- Msvm_WiFiPort.SaveProperties
- Msvm_WiFiPort.RestoreProperties
- Msvm_WiFiPort.InstanceID
- Msvm_WiFiPort.Caption
- Msvm_WiFiPort.Description
- Msvm_WiFiPort.ElementName
- Msvm_WiFiPort.InstallDate
- Msvm_WiFiPort.Name
- Msvm_WiFiPort.OperationalStatus
- Msvm_WiFiPort.StatusDescriptions
- Msvm_WiFiPort.Status
- Msvm_WiFiPort.HealthState
- Msvm_WiFiPort.CommunicationStatus
- Msvm_WiFiPort.DetailedStatus
- Msvm_WiFiPort.OperatingStatus
- Msvm_WiFiPort.PrimaryStatus
- Msvm_WiFiPort.EnabledState
- Msvm_WiFiPort.OtherEnabledState
- Msvm_WiFiPort.RequestedState
- Msvm_WiFiPort.EnabledDefault
- Msvm_WiFiPort.TimeOfLastStateChange
- Msvm_WiFiPort.AvailableRequestedStates
- Msvm_WiFiPort.TransitioningToState
- Msvm_WiFiPort.SystemCreationClassName
- Msvm_WiFiPort.SystemName
- Msvm_WiFiPort.CreationClassName
- Msvm_WiFiPort.DeviceID
- Msvm_WiFiPort.PowerManagementSupported
- Msvm_WiFiPort.PowerManagementCapabilities
- Msvm_WiFiPort.Availability
- Msvm_WiFiPort.StatusInfo
- Msvm_WiFiPort.LastErrorCode
- Msvm_WiFiPort.ErrorDescription
- Msvm_WiFiPort.ErrorCleared
- Msvm_WiFiPort.OtherIdentifyingInfo
- Msvm_WiFiPort.PowerOnHours
- Msvm_WiFiPort.TotalPowerOnHours
- Msvm_WiFiPort.IdentifyingDescriptions
- Msvm_WiFiPort.AdditionalAvailability
- Msvm_WiFiPort.MaxQuiesceTime
- Msvm_WiFiPort.Speed
- Msvm_WiFiPort.MaxSpeed
- Msvm_WiFiPort.RequestedSpeed
- Msvm_WiFiPort.UsageRestriction
- Msvm_WiFiPort.PortType
- Msvm_WiFiPort.OtherPortType
- Msvm_WiFiPort.OtherNetworkPortType
- Msvm_WiFiPort.PortNumber
- Msvm_WiFiPort.LinkTechnology
- Msvm_WiFiPort.OtherLinkTechnology
- Msvm_WiFiPort.PermanentAddress
- Msvm_WiFiPort.NetworkAddresses
- Msvm_WiFiPort.FullDuplex
- Msvm_WiFiPort.AutoSense
- Msvm_WiFiPort.SupportedMaximumTransmissionUnit
- Msvm_WiFiPort.ActiveMaximumTransmissionUnit
- Msvm_WiFiPort.IsBound
api_type:
- DllExport
api_location:
- vmms.exe
ms.openlocfilehash: 66f8e86d83ba5eac09903d0c2be221e24ce24ab92c5060856938810a62f427a2
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/11/2021
ms.locfileid: "117993668"
---
# <a name="msvm_wifiport-class"></a>Msvm \_ WiFiPort 類別

代表可系結至虛擬交換器的實體 Wi-Fi (802.11) 網路介面卡，以提供虛擬機器的外部網路連線能力。

下列語法已簡化受控物件格式 (MOF) 程式碼，並且包含所有繼承的屬性。

## <a name="syntax"></a>語法

``` syntax
[Dynamic, Provider("VmmsWmiInstanceAndMethodProvider"), AMENDMENT]
class Msvm_WiFiPort : CIM_WiFiPort
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
  uint16   EnabledState = 2;
  string   OtherEnabledState;
  uint16   RequestedState;
  uint16   EnabledDefault;
  datetime TimeOfLastStateChange;
  uint16   AvailableRequestedStates[];
  uint16   TransitioningToState;
  string   SystemCreationClassName;
  string   SystemName;
  string   CreationClassName;
  string   DeviceID;
  boolean  PowerManagementSupported;
  uint16   PowerManagementCapabilities[];
  uint16   Availability;
  uint16   StatusInfo;
  uint32   LastErrorCode;
  string   ErrorDescription;
  boolean  ErrorCleared;
  string   OtherIdentifyingInfo[];
  uint64   PowerOnHours;
  uint64   TotalPowerOnHours;
  string   IdentifyingDescriptions[];
  uint16   AdditionalAvailability[];
  uint64   MaxQuiesceTime;
  uint64   Speed;
  uint64   MaxSpeed;
  uint64   RequestedSpeed;
  uint16   UsageRestriction;
  uint16   PortType;
  string   OtherPortType;
  string   OtherNetworkPortType;
  uint16   PortNumber;
  uint16   LinkTechnology;
  string   OtherLinkTechnology;
  string   PermanentAddress;
  string   NetworkAddresses[];
  boolean  FullDuplex;
  boolean  AutoSense;
  uint64   SupportedMaximumTransmissionUnit;
  uint64   ActiveMaximumTransmissionUnit;
  boolean  IsBound;
};
```

## <a name="members"></a>成員

**Msvm \_ WiFiPort** 類別具有下列類型的成員：

-   [方法](#methods)
-   [屬性](#properties)

### <a name="methods"></a>方法

**Msvm \_ WiFiPort** 類別具有這些方法。



| 方法                 | 描述                              |
|:-----------------------|:-----------------------------------------|
| **EnableDevice**       | 不支援這個方法。<br/> |
| **OnlineDevice**       | 不支援這個方法。<br/> |
| **QuiesceDevice**      | 不支援這個方法。<br/> |
| **RequestStateChange** | 不支援這個方法。<br/> |
| **重設**              | 不支援這個方法。<br/> |
| **RestoreProperties**  | 不支援這個方法。<br/> |
| **SaveProperties**     | 不支援這個方法。<br/> |
| **SetPowerState**      | 不支援這個方法。<br/> |



 

### <a name="properties"></a>屬性

**Msvm \_ WiFiPort** 類別具有這些屬性。

<dl> <dt>

**ActiveMaximumTransmissionUnit**
</dt> <dd> <dl> <dt>

資料類型： **uint64**
</dt> <dt>

存取類型：唯讀
</dt> <dt>

限定詞： **單位** ( "Bytes" ) 
</dt> </dl>

使用中或已協商的最大傳輸單位 (MTU) 可支援，以位元組為單位。 這個屬性繼承自 [**CIM \_ NetworkPort**](/previous-versions/windows/desktop/iscsitarg/cim-networkport)。

</dd> <dt>

**AdditionalAvailability**
</dt> <dd> <dl> <dt>

資料類型： **uint16** 陣列
</dt> <dt>

存取類型：唯讀
</dt> </dl>

裝置的任何額外可用性和狀態。 這個屬性繼承自 [**CIM \_ LogicalDevice**](/windows/desktop/CIMWin32Prov/cim-logicaldevice)。

</dd> <dt>

**自動感測**
</dt> <dd> <dl> <dt>

資料類型： **布林值**
</dt> <dt>

存取類型：唯讀
</dt> </dl>

指出埠是否能夠自動判斷連接之網路媒體的速度或其他通訊特性。 這個屬性繼承自 [**CIM \_ NetworkPort**](/previous-versions/windows/desktop/iscsitarg/cim-networkport)。

</dd> <dt>

**可用性**
</dt> <dd> <dl> <dt>

資料類型： **uint16**
</dt> <dt>

存取類型：唯讀
</dt> </dl>

裝置的主要可用性和狀態。 這個屬性繼承自 [**CIM \_ LogicalDevice**](/windows/desktop/CIMWin32Prov/cim-logicaldevice)。

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

**標題**
</dt> <dd> <dl> <dt>

資料類型： **字串**
</dt> <dt>

存取類型：唯讀
</dt> </dl>

物件的簡短描述。 這個屬性繼承自 [**CIM \_ ManagedElement**](/previous-versions/windows/desktop/iscsitarg/cim-managedelement) 類別。

</dd> <dt>

**CommunicationStatus**
</dt> <dd> <dl> <dt>

資料類型： **uint16**
</dt> <dt>

存取類型：唯讀
</dt> </dl>

指出檢測與基礎受管理元素通訊的能力。 **Null** 值表示不會執行此屬性。 這個屬性繼承自 [**CIM \_ ManagedSystemElement**](/windows/desktop/CIMWin32Prov/cim-managedsystemelement)。

</dd> <dt>

**CreationClassName**
</dt> <dd> <dl> <dt>

資料類型： **字串**
</dt> <dt>

存取類型：唯讀
</dt> </dl>

範圍系統的建立類別名稱。 這個屬性繼承自 [**CIM \_ LogicalDevice**](/windows/desktop/CIMWin32Prov/cim-logicaldevice)。

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

**DeviceID**
</dt> <dd> <dl> <dt>

資料類型： **字串**
</dt> <dt>

存取類型：唯讀
</dt> </dl>

用來唯一命名邏輯裝置的位址或其他識別資訊。 這個屬性繼承自 [**CIM \_ LogicalDevice**](/windows/desktop/CIMWin32Prov/cim-logicaldevice)。

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

系統管理員的預設或啟動設定，適用于元素的 **EnabledState** 屬性。 這個屬性繼承自 [**CIM \_ EnabledLogicalElement**](/previous-versions//cc136818(v=vs.85))。

</dd> <dt>

**EnabledState**
</dt> <dd> <dl> <dt>

資料類型： **uint16**
</dt> <dt>

存取類型：唯讀
</dt> </dl>

專案的已啟用和停用狀態。 這個屬性繼承自 [**CIM \_ EnabledLogicalElement**](/previous-versions//cc136818(v=vs.85))，它會是下列其中一個值。



| 值                                                                                                                                                                                                                           | 意義                               |
|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|---------------------------------------|
| <span id="Enabled"></span><span id="enabled"></span><span id="ENABLED"></span><dl> <dt>**已啟用**</dt> <dt>2</dt> </dl>     | 元素正在執行。<br/>    |
| <span id="Disabled"></span><span id="disabled"></span><span id="DISABLED"></span><dl> <dt>**停用**</dt> <dt>3</dt> </dl> | 元素已關閉。<br/> |



 

</dd> <dt>

**ErrorCleared**
</dt> <dd> <dl> <dt>

資料類型： **布林值**
</dt> <dt>

存取類型：唯讀
</dt> </dl>

指出現在是否已清除 **LastErrorCode** 中報告的錯誤。 這個屬性繼承自 [**CIM \_ LogicalDevice**](/windows/desktop/CIMWin32Prov/cim-logicaldevice)。

</dd> <dt>

**ErrorDescription**
</dt> <dd> <dl> <dt>

資料類型： **字串**
</dt> <dt>

存取類型：唯讀
</dt> </dl>

字串，提供 **LastErrorCode** 中所記錄錯誤的詳細資訊，以及可採取之任何矯正措施的相關資訊。 這個屬性繼承自 [**CIM \_ LogicalDevice**](/windows/desktop/CIMWin32Prov/cim-logicaldevice)。

</dd> <dt>

**FullDuplex**
</dt> <dd> <dl> <dt>

資料類型： **布林值**
</dt> <dt>

存取類型：唯讀
</dt> </dl>

指出埠是否以全雙工模式運作。 這個屬性繼承自 [**CIM \_ NetworkPort**](/previous-versions/windows/desktop/iscsitarg/cim-networkport)。

</dd> <dt>

**HealthState**
</dt> <dd> <dl> <dt>

資料類型： **uint16**
</dt> <dt>

存取類型：唯讀
</dt> </dl>

專案目前的健康情況。 這個屬性繼承自 [**CIM \_ ManagedSystemElement**](/windows/desktop/CIMWin32Prov/cim-managedsystemelement)。

</dd> <dt>

**IdentifyingDescriptions**
</dt> <dd> <dl> <dt>

資料類型： **字串** 陣列
</dt> <dt>

存取類型：唯讀
</dt> </dl>

自由格式字串的陣列，可提供 **OtherIdentifyingInfo** 屬性陣列中專案背後的說明和詳細資料。 這個屬性繼承自 [**CIM \_ LogicalDevice**](/windows/desktop/CIMWin32Prov/cim-logicaldevice)。

</dd> <dt>

**InstallDate**
</dt> <dd> <dl> <dt>

資料類型： **datetime**
</dt> <dt>

存取類型：唯讀
</dt> </dl>

安裝物件的日期和時間。 這個屬性不需要值來表示已安裝物件。 這個屬性繼承自 [**CIM \_ ManagedSystemElement**](/windows/desktop/CIMWin32Prov/cim-managedsystemelement)。

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

**IsBound**
</dt> <dd> <dl> <dt>

資料類型： **布林值**
</dt> <dt>

存取類型：唯讀
</dt> </dl>

指定 Wi-Fi 埠是否系結至虛擬機器網路架構。 這會是下列其中一個值。



| 值                                                                                                                                                        | 意義                                                                                 |
|--------------------------------------------------------------------------------------------------------------------------------------------------------------|-----------------------------------------------------------------------------------------|
| <span id="True"></span><span id="true"></span><span id="TRUE"></span><dl> <dt>**真**</dt> </dl>     | Wi-Fi 埠會系結至虛擬機器網路架構。 <br/>     |
| <span id="False"></span><span id="false"></span><span id="FALSE"></span><dl> <dt>**否**</dt> </dl> | Wi-Fi 埠未系結至虛擬機器網路架構。 <br/> |



 

</dd> <dt>

**LastErrorCode**
</dt> <dd> <dl> <dt>

資料類型： **uint32**
</dt> <dt>

存取類型：唯讀
</dt> </dl>

邏輯裝置所報告的最後一個錯誤碼。 這個屬性繼承自 [**CIM \_ LogicalDevice**](/windows/desktop/CIMWin32Prov/cim-logicaldevice)。

</dd> <dt>

**LinkTechnology**
</dt> <dd> <dl> <dt>

資料類型： **uint16**
</dt> <dt>

存取類型：唯讀
</dt> </dl>

指定埠的連結技術類型。 當設定為1時 (其他) ， **OtherLinkTechnology** 屬性會包含連結類型的字串描述。 這個屬性繼承自 [**CIM \_ NetworkPort**](/previous-versions/windows/desktop/iscsitarg/cim-networkport)。

<dl> <dt>

<span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>**未知** 的 (0) 
</dt> <dt>

<span id="Other"></span><span id="other"></span><span id="OTHER"></span>**其他** (1) 
</dt> <dt>

<span id="Ethernet"></span><span id="ethernet"></span><span id="ETHERNET"></span>**Ethernet** (2) 
</dt> <dt>

<span id="IB"></span><span id="ib"></span>**IB** (3) 
</dt> <dt>

<span id="FC"></span><span id="fc"></span>**FC** (4) 
</dt> <dt>

<span id="FDDI"></span><span id="fddi"></span>**FDDI** (5) 
</dt> <dt>

<span id="ATM"></span><span id="atm"></span>**ATM** (6) 
</dt> <dt>

<span id="Token_Ring"></span><span id="token_ring"></span><span id="TOKEN_RING"></span>**權杖環** (7) 
</dt> <dt>

<span id="Frame_Relay"></span><span id="frame_relay"></span><span id="FRAME_RELAY"></span>**框架轉送** (8) 
</dt> <dt>

<span id="Infrared"></span><span id="infrared"></span><span id="INFRARED"></span>**紅外線** (9) 
</dt> <dt>

<span id="BlueTooth"></span><span id="bluetooth"></span><span id="BLUETOOTH"></span>**藍牙** (10) 
</dt> <dt>

<span id="Wireless_LAN_"></span><span id="wireless_lan_"></span><span id="WIRELESS_LAN_"></span>**無線區域網路** (11 ) 
</dt> </dl>

</dd> <dt>

**MaxQuiesceTime**
</dt> <dd> <dl> <dt>

資料類型： **uint64**
</dt> <dt>

存取類型：唯讀
</dt> </dl>

這個屬性已被取代。 這個屬性繼承自 [**CIM \_ LogicalDevice**](/windows/desktop/CIMWin32Prov/cim-logicaldevice)。

</dd> <dt>

**MaxSpeed**
</dt> <dd> <dl> <dt>

資料類型： **uint64**
</dt> <dt>

存取類型：唯讀
</dt> <dt>

限定詞： **單位** ( 「每秒位數」 ) 
</dt> </dl>

埠的最大頻寬（以每秒位數為單位）。 這個屬性繼承自 [**CIM \_ LogicalPort**](/previous-versions//cc136869(v=vs.85))。

</dd> <dt>

**名稱**
</dt> <dd> <dl> <dt>

資料類型： **字串**
</dt> <dt>

存取類型：唯讀
</dt> </dl>

已知物件的標籤。 這個屬性繼承自 [**CIM \_ ManagedSystemElement**](/windows/desktop/CIMWin32Prov/cim-managedsystemelement)。

</dd> <dt>

**NetworkAddresses**
</dt> <dd> <dl> <dt>

資料類型： **字串** 陣列
</dt> <dt>

存取類型：唯讀
</dt> <dt>

限定詞： **MaxLen** ( 64 ) 
</dt> </dl>

包含埠之 MAC 位址的字串陣列。 這個屬性繼承自 [**CIM \_ NetworkPort**](/previous-versions/windows/desktop/iscsitarg/cim-networkport)。

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

**OtherEnabledState**
</dt> <dd> <dl> <dt>

資料類型： **字串**
</dt> <dt>

存取類型：唯讀
</dt> </dl>

描述當 **EnabledState** 屬性設定為 1 (其他) 時，專案已啟用或停用狀態的字串。 當 **EnabledState** 屬性是1以外的任何值時，這個屬性必須設定為 **Null** 。 這個屬性繼承自 [**CIM \_ EnabledLogicalElement**](/previous-versions//cc136818(v=vs.85))。

</dd> <dt>

**OtherIdentifyingInfo**
</dt> <dd> <dl> <dt>

資料類型： **字串** 陣列
</dt> <dt>

存取類型：唯讀
</dt> </dl>

除了裝置識別碼資訊以外的任何其他資料，可用來識別邏輯裝置。 這個屬性繼承自 [**CIM \_ LogicalDevice**](/windows/desktop/CIMWin32Prov/cim-logicaldevice)。

</dd> <dt>

**OtherLinkTechnology**
</dt> <dd> <dl> <dt>

資料類型： **字串**
</dt> <dt>

存取類型：唯讀
</dt> </dl>

描述 **LinkTechnology** 設定為1， (其他) 的字串值。 這個屬性繼承自 [**CIM \_ NetworkPort**](/previous-versions/windows/desktop/iscsitarg/cim-networkport)。

</dd> <dt>

**OtherNetworkPortType**
</dt> <dd> <dl> <dt>

資料類型： **字串**
</dt> <dt>

存取類型：唯讀
</dt> </dl>

使用這個屬性會取代 **PortType** 屬性。 這個屬性繼承自 [**CIM \_ NetworkPort**](/previous-versions/windows/desktop/iscsitarg/cim-networkport)。

</dd> <dt>

**OtherPortType**
</dt> <dd> <dl> <dt>

資料類型： **字串**
</dt> <dt>

存取類型：唯讀
</dt> </dl>

描述當 **PortType** 設定為1時 (其他) 的模組類型。 這個屬性繼承自 [**CIM \_ LogicalPort**](/previous-versions//cc136869(v=vs.85))。

</dd> <dt>

**PermanentAddress**
</dt> <dd> <dl> <dt>

資料類型： **字串**
</dt> <dt>

存取類型：唯讀
</dt> <dt>

限定詞： **MaxLen** ( 64 ) 
</dt> </dl>

硬式編碼在埠中的網路位址。 您可以使用固件升級或軟體設定來變更這個硬式編碼的位址。 進行這項變更時，應同時更新欄位。 如果網路介面卡沒有任何硬式編碼位址，則此屬性應為 **Null** 。 這個屬性繼承自 [**CIM \_ NetworkPort**](/previous-versions/windows/desktop/iscsitarg/cim-networkport)。

</dd> <dt>

**PortNumber**
</dt> <dd> <dl> <dt>

資料類型： **uint16**
</dt> <dt>

存取類型：唯讀
</dt> </dl>

連接埠號碼。 這個屬性繼承自 [**CIM \_ NetworkPort**](/previous-versions/windows/desktop/iscsitarg/cim-networkport)。

</dd> <dt>

**PortType**
</dt> <dd> <dl> <dt>

資料類型： **uint16**
</dt> <dt>

存取類型：唯讀
</dt> </dl>

目前為埠啟用的特定模式。 當設定為1時 (其他) ，相關的 **OtherPortType** 屬性會包含埠類型的字串描述。 這個屬性繼承自 [**CIM \_ LogicalPort**](/previous-versions//cc136869(v=vs.85))。

<dl> <dt>

<span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>**未知** 的 (0) 
</dt> <dt>

<span id="Other"></span><span id="other"></span><span id="OTHER"></span>**其他** (1) 
</dt> <dt>

<span id="__50_Copper___________________10BaseT"></span><span id="__50_copper___________________10baset"></span><span id="__50_COPPER___________________10BASET"></span>**50 銅的 10baset** (50) 
</dt> <dt>

<span id="10-100BaseT"></span><span id="10-100baset"></span><span id="10-100BASET"></span>**10-100BaseT** (51) 
</dt> <dt>

<span id="100BaseT"></span><span id="100baset"></span><span id="100BASET"></span>**100BaseT** (52) 
</dt> <dt>

<span id="1000BaseT"></span><span id="1000baset"></span><span id="1000BASET"></span>**1000BaseT** (53) 
</dt> <dt>

<span id="2500BaseT"></span><span id="2500baset"></span><span id="2500BASET"></span>**2500BaseT** (54) 
</dt> <dt>

<span id="10GBaseT"></span><span id="10gbaset"></span><span id="10GBASET"></span>**10GBaseT** (55) 
</dt> <dt>

<span id="10GBase-CX4"></span><span id="10gbase-cx4"></span><span id="10GBASE-CX4"></span>**10gbase-t-CX4** (56) 
</dt> <dt>

<span id="__100_Fibre___________________100Base-FX"></span><span id="__100_fibre___________________100base-fx"></span><span id="__100_FIBRE___________________100BASE-FX"></span>**100 光纖 100base-tx-FX** (100) 
</dt> <dt>

<span id="100Base-SX"></span><span id="100base-sx"></span><span id="100BASE-SX"></span>**100base-tx-SX** (101) 
</dt> <dt>

<span id="1000Base-SX"></span><span id="1000base-sx"></span><span id="1000BASE-SX"></span>**1000base-t-SX** (102) 
</dt> <dt>

<span id="1000Base-LX"></span><span id="1000base-lx"></span><span id="1000BASE-LX"></span>**1000base-t-LX** (103) 
</dt> <dt>

<span id="1000Base-CX"></span><span id="1000base-cx"></span><span id="1000BASE-CX"></span>**1000base-t-CX** (104) 
</dt> <dt>

<span id="10GBase-SR"></span><span id="10gbase-sr"></span><span id="10GBASE-SR"></span>**10gbase-t-SR** (105) 
</dt> <dt>

<span id="10GBase-SW"></span><span id="10gbase-sw"></span><span id="10GBASE-SW"></span>**10gbase-t-SW** (106) 
</dt> <dt>

<span id="10GBase-LX4"></span><span id="10gbase-lx4"></span><span id="10GBASE-LX4"></span>**LX4** (107) 
</dt> <dt>

<span id="10GBase-LR"></span><span id="10gbase-lr"></span><span id="10GBASE-LR"></span>**10gbase-t-LR** (108) 
</dt> <dt>

<span id="10GBase-LW"></span><span id="10gbase-lw"></span><span id="10GBASE-LW"></span>**LW** (109) 
</dt> <dt>

<span id="10GBase-ER"></span><span id="10gbase-er"></span><span id="10GBASE-ER"></span>**10gbase-t-ER** (110) 
</dt> <dt>

<span id="10GBase-EW"></span><span id="10gbase-ew"></span><span id="10GBASE-EW"></span> (111) **的**
</dt> <dt>

<span id="Vendor_Reserved_"></span><span id="vendor_reserved_"></span><span id="VENDOR_RESERVED_"></span>**廠商保留** (16，000. 65535 ) 
</dt> </dl>

</dd> <dt>

**PowerManagementCapabilities**
</dt> <dd> <dl> <dt>

資料類型： **uint16** 陣列
</dt> <dt>

存取類型：唯讀
</dt> </dl>

裝置的電源管理功能。 這個屬性繼承自 [**CIM \_ LogicalDevice**](/windows/desktop/CIMWin32Prov/cim-logicaldevice)。

</dd> <dt>

**PowerManagementSupported**
</dt> <dd> <dl> <dt>

資料類型： **布林值**
</dt> <dt>

存取類型：唯讀
</dt> </dl>

指出裝置是否可以受電源管理。 這個屬性繼承自 [**CIM \_ LogicalDevice**](/windows/desktop/CIMWin32Prov/cim-logicaldevice)。

</dd> <dt>

**PowerOnHours**
</dt> <dd> <dl> <dt>

資料類型： **uint64**
</dt> <dt>

存取類型：唯讀
</dt> </dl>

此裝置自上一次電源週期起開啟電源的連續小時數。 這個屬性繼承自 [**CIM \_ LogicalDevice**](/windows/desktop/CIMWin32Prov/cim-logicaldevice)。

</dd> <dt>

**PrimaryStatus**
</dt> <dd> <dl> <dt>

資料類型： **uint16**
</dt> <dt>

存取類型：唯讀
</dt> </dl>

提供高層級的狀態資訊。 這個屬性應該與 **DetailedStatus** 屬性一起使用，以提供元素和其子元件的高階和詳細健全狀況狀態資訊。 **Null** 值表示不會執行此屬性。 這個屬性繼承自 [**CIM \_ ManagedSystemElement**](/windows/desktop/CIMWin32Prov/cim-managedsystemelement)。

</dd> <dt>

**RequestedSpeed**
</dt> <dd> <dl> <dt>

資料類型： **uint64**
</dt> <dt>

存取類型：僅限寫入
</dt> <dt>

限定詞： **單位** ( 「每秒位數」 ) 
</dt> </dl>

要求的埠頻寬（以每秒位數為單位）。 實際的頻寬會在 [ **速度** ] 屬性中報告。 這個屬性繼承自 [**CIM \_ LogicalPort**](/previous-versions//cc136869(v=vs.85))。

</dd> <dt>

**RequestedState**
</dt> <dd> <dl> <dt>

資料類型： **uint16**
</dt> <dt>

存取類型：唯讀
</dt> </dl>

上次要求或預期的專案狀態。 這個屬性繼承自 [**CIM \_ EnabledLogicalElement**](/previous-versions//cc136818(v=vs.85))。

</dd> <dt>

**速度**
</dt> <dd> <dl> <dt>

資料類型： **uint64**
</dt> <dt>

存取類型：唯讀
</dt> <dt>

限定詞： **單位** ( 「每秒位數」 ) 
</dt> </dl>

埠的頻寬（以每秒位數為單位）。 這個屬性繼承自 [**CIM \_ LogicalPort**](/previous-versions//cc136869(v=vs.85))。

</dd> <dt>

**狀態**
</dt> <dd> <dl> <dt>

資料類型： **字串**
</dt> <dt>

存取類型：唯讀
</dt> </dl>

物件的目前狀態。 這個屬性繼承自 [**CIM \_ ManagedSystemElement**](/windows/desktop/CIMWin32Prov/cim-managedsystemelement)。

</dd> <dt>

**StatusDescriptions**
</dt> <dd> <dl> <dt>

資料類型： **字串** 陣列
</dt> <dt>

存取類型：唯讀
</dt> </dl>

描述各種 **OperationalStatus** 陣列值的字串。 這個屬性繼承自 [**CIM \_ ManagedSystemElement**](/windows/desktop/CIMWin32Prov/cim-managedsystemelement)。

</dd> <dt>

**StatusInfo**
</dt> <dd> <dl> <dt>

資料類型： **uint16**
</dt> <dt>

存取類型：唯讀
</dt> </dl>

邏輯裝置的目前狀態。 這個屬性繼承自 [**CIM \_ LogicalDevice**](/windows/desktop/CIMWin32Prov/cim-logicaldevice)。

</dd> <dt>

**SupportedMaximumTransmissionUnit**
</dt> <dd> <dl> <dt>

資料類型： **uint64**
</dt> <dt>

存取類型：唯讀
</dt> <dt>

限定詞： **單位** ( "Bytes" ) 
</dt> </dl>

可支援的最大傳輸單位 (MTU) （以位元組為單位）。 這個屬性繼承自 [**CIM \_ NetworkPort**](/previous-versions/windows/desktop/iscsitarg/cim-networkport)。

</dd> <dt>

**SystemCreationClassName**
</dt> <dd> <dl> <dt>

資料類型： **字串**
</dt> <dt>

存取類型：唯讀
</dt> </dl>

範圍系統的建立類別名稱。 這個屬性繼承自 [**CIM \_ LogicalDevice**](/windows/desktop/CIMWin32Prov/cim-logicaldevice)。

</dd> <dt>

**SystemName**
</dt> <dd> <dl> <dt>

資料類型： **字串**
</dt> <dt>

存取類型：唯讀
</dt> </dl>

範圍系統的名稱。 這個屬性繼承自 [**CIM \_ LogicalDevice**](/windows/desktop/CIMWin32Prov/cim-logicaldevice)。

</dd> <dt>

**TimeOfLastStateChange**
</dt> <dd> <dl> <dt>

資料類型： **datetime**
</dt> <dt>

存取類型：唯讀
</dt> </dl>

專案的已啟用狀態上次變更的日期或時間。 這個屬性繼承自 [**CIM \_ EnabledLogicalElement**](/previous-versions//cc136818(v=vs.85))。

</dd> <dt>

**TotalPowerOnHours**
</dt> <dd> <dl> <dt>

資料類型： **uint64**
</dt> <dt>

存取類型：唯讀
</dt> </dl>

此裝置開機的總時數。 這個屬性繼承自 [**CIM \_ LogicalDevice**](/windows/desktop/CIMWin32Prov/cim-logicaldevice)。

</dd> <dt>

**TransitioningToState**
</dt> <dd> <dl> <dt>

資料類型： **uint16**
</dt> <dt>

存取類型：唯讀
</dt> </dl>

指出實例正在轉換的目標狀態。 這個屬性繼承自 [**CIM \_ EnabledLogicalElement**](/previous-versions//cc136818(v=vs.85))，但不會使用它。

</dd> <dt>

**UsageRestriction**
</dt> <dd> <dl> <dt>

資料類型： **uint16**
</dt> <dt>

存取類型：唯讀
</dt> </dl>

在某些情況下，邏輯埠可能會識別為前端或後端埠。 這種情況的範例之一，就是可能有後端埠與磁片磁碟機和前端埠通訊以與主機通訊的存放裝置陣列。 如果埠的使用沒有限制，則值應該設定為 4 (不受限制的) 。 這個屬性繼承自 [**CIM \_ LogicalPort**](/previous-versions//cc136869(v=vs.85))。

<dl> <dt>

<span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>**未知** 的 (0) 
</dt> <dt>

<span id="Front-end_only"></span><span id="front-end_only"></span><span id="FRONT-END_ONLY"></span>**前端** (2) 
</dt> <dt>

<span id="Back-end_only"></span><span id="back-end_only"></span><span id="BACK-END_ONLY"></span> (3) 的 **後端**
</dt> <dt>

<span id="Not_restricted_"></span><span id="not_restricted_"></span><span id="NOT_RESTRICTED_"></span>**不受限制** (4 ) 
</dt> </dl>

</dd> </dl>

## <a name="requirements"></a>規格需求



| 需求 | 值 |
|-------------------------------------|---------------------------------------------------------------------------------------------------------|
| 最低支援的用戶端<br/> | Windows 8 \[僅限桌面應用程式\]<br/>                                                              |
| 最低支援的伺服器<br/> | Windows Server 2012 \[僅限桌面應用程式\]<br/>                                                    |
| 命名空間<br/>                | 根 \\ 虛擬化 \\ V2<br/>                                                                     |
| MOF<br/>                      | <dl> <dt>WindowsVirtualization。</dt> </dl> |
| DLL<br/>                      | <dl> <dt>Vmms.exe</dt> </dl>                     |



 

