---
description: 代表模擬的乙太網路介面卡。
ms.assetid: 8E990C76-7D48-42B0-BB4D-C4C07B1C482A
title: Msvm_EmulatedEthernetPort 類別
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Msvm_EmulatedEthernetPort
- Msvm_EmulatedEthernetPort.SetPowerState
- Msvm_EmulatedEthernetPort.EnableDevice
- Msvm_EmulatedEthernetPort.OnlineDevice
- Msvm_EmulatedEthernetPort.QuiesceDevice
- Msvm_EmulatedEthernetPort.SaveProperties
- Msvm_EmulatedEthernetPort.RestoreProperties
- Msvm_EmulatedEthernetPort.InstanceID
- Msvm_EmulatedEthernetPort.Caption
- Msvm_EmulatedEthernetPort.Description
- Msvm_EmulatedEthernetPort.ElementName
- Msvm_EmulatedEthernetPort.InstallDate
- Msvm_EmulatedEthernetPort.Name
- Msvm_EmulatedEthernetPort.OperationalStatus
- Msvm_EmulatedEthernetPort.StatusDescriptions
- Msvm_EmulatedEthernetPort.Status
- Msvm_EmulatedEthernetPort.HealthState
- Msvm_EmulatedEthernetPort.CommunicationStatus
- Msvm_EmulatedEthernetPort.DetailedStatus
- Msvm_EmulatedEthernetPort.OperatingStatus
- Msvm_EmulatedEthernetPort.PrimaryStatus
- Msvm_EmulatedEthernetPort.EnabledState
- Msvm_EmulatedEthernetPort.OtherEnabledState
- Msvm_EmulatedEthernetPort.RequestedState
- Msvm_EmulatedEthernetPort.EnabledDefault
- Msvm_EmulatedEthernetPort.TimeOfLastStateChange
- Msvm_EmulatedEthernetPort.AvailableRequestedStates
- Msvm_EmulatedEthernetPort.TransitioningToState
- Msvm_EmulatedEthernetPort.SystemCreationClassName
- Msvm_EmulatedEthernetPort.SystemName
- Msvm_EmulatedEthernetPort.CreationClassName
- Msvm_EmulatedEthernetPort.DeviceID
- Msvm_EmulatedEthernetPort.PowerManagementSupported
- Msvm_EmulatedEthernetPort.PowerManagementCapabilities
- Msvm_EmulatedEthernetPort.Availability
- Msvm_EmulatedEthernetPort.StatusInfo
- Msvm_EmulatedEthernetPort.LastErrorCode
- Msvm_EmulatedEthernetPort.ErrorDescription
- Msvm_EmulatedEthernetPort.ErrorCleared
- Msvm_EmulatedEthernetPort.OtherIdentifyingInfo
- Msvm_EmulatedEthernetPort.PowerOnHours
- Msvm_EmulatedEthernetPort.TotalPowerOnHours
- Msvm_EmulatedEthernetPort.IdentifyingDescriptions
- Msvm_EmulatedEthernetPort.AdditionalAvailability
- Msvm_EmulatedEthernetPort.MaxQuiesceTime
- Msvm_EmulatedEthernetPort.Speed
- Msvm_EmulatedEthernetPort.MaxSpeed
- Msvm_EmulatedEthernetPort.RequestedSpeed
- Msvm_EmulatedEthernetPort.UsageRestriction
- Msvm_EmulatedEthernetPort.PortType
- Msvm_EmulatedEthernetPort.OtherPortType
- Msvm_EmulatedEthernetPort.OtherNetworkPortType
- Msvm_EmulatedEthernetPort.PortNumber
- Msvm_EmulatedEthernetPort.LinkTechnology
- Msvm_EmulatedEthernetPort.OtherLinkTechnology
- Msvm_EmulatedEthernetPort.PermanentAddress
- Msvm_EmulatedEthernetPort.NetworkAddresses
- Msvm_EmulatedEthernetPort.FullDuplex
- Msvm_EmulatedEthernetPort.AutoSense
- Msvm_EmulatedEthernetPort.SupportedMaximumTransmissionUnit
- Msvm_EmulatedEthernetPort.ActiveMaximumTransmissionUnit
- Msvm_EmulatedEthernetPort.MaxDataSize
- Msvm_EmulatedEthernetPort.Capabilities
- Msvm_EmulatedEthernetPort.CapabilityDescriptions
- Msvm_EmulatedEthernetPort.EnabledCapabilities
- Msvm_EmulatedEthernetPort.OtherEnabledCapabilities
api_type:
- DllExport
api_location:
- vmms.exe
ms.openlocfilehash: ef4d061d709f83e5069614f169252c06a370106a938b98281afb88b5a11508fc
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/11/2021
ms.locfileid: "118148354"
---
# <a name="msvm_emulatedethernetport-class"></a>Msvm \_ EmulatedEthernetPort 類別

代表模擬的乙太網路介面卡。 當虛擬機器未在來賓中安裝任何整合線路時，會使用此介面卡來執行綜合乙太網路埠。

> [!Note]  
> 第2代虛擬機器無法使用此類別。

 

下列語法已簡化受控物件格式 (MOF) 程式碼，並且包含所有繼承的屬性。

## <a name="syntax"></a>語法

``` syntax
[Dynamic, Provider("VmmsWmiInstanceAndMethodProvider"), AMENDMENT]
class Msvm_EmulatedEthernetPort : CIM_EthernetPort
{
  string   InstanceID;
  string   Caption = "Ethernet Port";
  string   Description = "Microsoft Emulated Ethernet Port";
  string   ElementName = "Legacy Network Adapter";
  datetime InstallDate;
  string   Name = "Ethernet Port";
  uint16   OperationalStatus[] = 2;
  string   StatusDescriptions[] = "OK";
  string   Status;
  uint16   HealthState = 5;
  uint16   CommunicationStatus;
  uint16   DetailedStatus;
  uint16   OperatingStatus;
  uint16   PrimaryStatus;
  uint16   EnabledState = 5;
  string   OtherEnabledState;
  uint16   RequestedState = 12;
  uint16   EnabledDefault = 2;
  datetime TimeOfLastStateChange;
  uint16   AvailableRequestedStates[];
  uint16   TransitioningToState;
  string   SystemCreationClassName = "Msvm_ComputerSystem";
  string   SystemName;
  string   CreationClassName = "Msvm_EmulatedEthernetPort";
  string   DeviceID = "Microsoft:GUID\device-specific data";
  boolean  PowerManagementSupported;
  uint16   PowerManagementCapabilities[];
  uint16   Availability;
  uint16   StatusInfo;
  uint32   LastErrorCode;
  string   ErrorDescription;
  boolean  ErrorCleared;
  string   OtherIdentifyingInfo[];
  uint64   PowerOnHours;
  uint16   TotalPowerOnHours;
  string   IdentifyingDescriptions[];
  uint16   AdditionalAvailability[] = 6;
  uint64   MaxQuiesceTime;
  uint64   Speed = 1000000000;
  uint64   MaxSpeed = 1000000000;
  uint64   RequestedSpeed = 1000000000;
  uint16   UsageRestriction = 4;
  uint16   PortType = 1;
  string   OtherPortType = "Virtual Ethernet";
  string   OtherNetworkPortType;
  uint16   PortNumber;
  uint16   LinkTechnology = 2;
  string   OtherLinkTechnology;
  string   PermanentAddress;
  string   NetworkAddresses[];
  boolean  FullDuplex = True;
  boolean  AutoSense = True;
  string   SupportedMaximumTransmissionUnit = 1500;
  uint64   ActiveMaximumTransmissionUnit = 1500;
  uint32   MaxDataSize = 1500;
  uint16   Capabilities[];
  string   CapabilityDescriptions[];
  uint16   EnabledCapabilities[];
  string   OtherEnabledCapabilities[];
};
```

## <a name="members"></a>成員

**Msvm \_ EmulatedEthernetPort** 類別具有下列類型的成員：

-   [方法](#methods)
-   [屬性](#properties)

### <a name="methods"></a>方法

**Msvm \_ EmulatedEthernetPort** 類別具有這些方法。



| 方法                                                                     | 描述                              |
|:---------------------------------------------------------------------------|:-----------------------------------------|
| **EnableDevice**                                                           | 不支援這個方法。<br/> |
| **OnlineDevice**                                                           | 不支援這個方法。<br/> |
| **QuiesceDevice**                                                          | 不支援這個方法。<br/> |
| [**RequestStateChange**](msvm-emulatedethernetport-requeststatechange.md) | 要求狀態變更。<br/>      |
| [**重設**](msvm-emulatedethernetport-reset.md)                           | 重設模擬裝置。<br/>   |
| **RestoreProperties**                                                      | 不支援這個方法。<br/> |
| **SaveProperties**                                                         | 不支援這個方法。<br/> |
| **SetPowerState**                                                          | 不支援這個方法。<br/> |



 

### <a name="properties"></a>屬性

**Msvm \_ EmulatedEthernetPort** 類別具有這些屬性。

<dl> <dt>

**ActiveMaximumTransmissionUnit**
</dt> <dd> <dl> <dt>

資料類型： **uint64**
</dt> <dt>

存取類型：唯讀
</dt> </dl>

可以支援的作用中或已協商的最大傳輸單位 (MTU) 。 這個屬性繼承自 [**CIM \_ NetworkPort**](/previous-versions/windows/desktop/iscsitarg/cim-networkport)，一律設為1500。

</dd> <dt>

**AdditionalAvailability**
</dt> <dd> <dl> <dt>

資料類型： **uint16** 陣列
</dt> <dt>

存取類型：唯讀
</dt> </dl>

裝置的任何額外可用性和狀態，超出 **可用性** 屬性中指定的範圍。 這個屬性繼承自 [**CIM \_ LogicalDevice**](/windows/desktop/CIMWin32Prov/cim-logicaldevice)，而且一律設定為 6 ( 「不適用」 ) 。

</dd> <dt>

**自動感測**
</dt> <dd> <dl> <dt>

資料類型： **布林值**
</dt> <dt>

存取類型：唯讀
</dt> </dl>

指出網路埠是否能夠自動判斷連接之網路媒體的速度或其他通訊特性。 這個屬性繼承自 [**CIM \_ NetworkPort**](/previous-versions/windows/desktop/iscsitarg/cim-networkport)，而且一律設定為 **True**。

</dd> <dt>

**可用性**
</dt> <dd> <dl> <dt>

資料類型： **uint16**
</dt> <dt>

存取類型：唯讀
</dt> </dl>

裝置的主要可用性和狀態。 這個屬性繼承自 [**CIM \_ LogicalDevice**](/windows/desktop/CIMWin32Prov/cim-logicaldevice)，而且一律設定為 **Null**。

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

**Capabilities**
</dt> <dd> <dl> <dt>

資料類型： **uint16** 陣列
</dt> <dt>

存取類型：唯讀
</dt> </dl>

乙太網路埠的功能。 這個屬性繼承自 [**CIM \_ EthernetPort**](/previous-versions/windows/desktop/iscsitarg/cim-ethernetport) ，而且不會使用。

</dd> <dt>

**CapabilityDescriptions**
</dt> <dd> <dl> <dt>

資料類型： **字串** 陣列
</dt> <dt>

存取類型：唯讀
</dt> </dl>

自由格式字串的陣列，可針對 **功能** 陣列中所指出的任何乙太網路埠功能提供更詳細的說明。 請注意，這個陣列的每個專案都與位於相同索引的 **功能** 陣列中的專案相關。 這個屬性繼承自 [**CIM \_ EthernetPort**](/previous-versions/windows/desktop/iscsitarg/cim-ethernetport) ，而且不會使用。

</dd> <dt>

**標題**
</dt> <dd> <dl> <dt>

資料類型： **字串**
</dt> <dt>

存取類型：唯讀
</dt> </dl>

物件的簡短描述。 這個屬性繼承自 [**CIM \_ ManagedElement**](/previous-versions/windows/desktop/iscsitarg/cim-managedelement)，一律設為「Ethernet 埠」。

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

建立實例時所使用之類別或子類別的名稱。 搭配這個類別的其他重要屬性使用時，此屬性可讓這個類別和其子類別的所有實例都能唯一識別。 這個屬性繼承自 [**CIM \_ LogicalDevice**](/windows/desktop/CIMWin32Prov/cim-logicaldevice)，而且一律設定為 "Msvm \_ EmulatedEthernetPort"。

</dd> <dt>

**說明**
</dt> <dd> <dl> <dt>

資料類型： **字串**
</dt> <dt>

存取類型：唯讀
</dt> </dl>

對物件的描述。 這個屬性繼承自 [**CIM \_ ManagedElement**](/previous-versions/windows/desktop/iscsitarg/cim-managedelement)，一律設為「Microsoft 模擬乙太網路埠」。

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

用來唯一命名邏輯裝置的位址或其他識別資訊。 這個屬性繼承自 [**CIM \_ LogicalDevice**](/windows/desktop/CIMWin32Prov/cim-logicaldevice)，且一律設定為 "Microsoft：*GUID* \\ *裝置特定資料*"。

</dd> <dt>

**ElementName**
</dt> <dd> <dl> <dt>

資料類型： **字串**
</dt> <dt>

存取類型：唯讀
</dt> </dl>

物件的顯示名稱。 這個屬性繼承自 [**CIM \_ ManagedElement**](/previous-versions/windows/desktop/iscsitarg/cim-managedelement)，一律設為「傳統網路介面卡」。

</dd> <dt>

**EnabledCapabilities**
</dt> <dd> <dl> <dt>

資料類型： **uint16** 陣列
</dt> <dt>

存取類型：唯讀
</dt> </dl>

從所有支援的專案清單中啟用的功能，這些功能都是在 **功能** 陣列中定義。 這個屬性繼承自 [**CIM \_ EthernetPort**](/previous-versions/windows/desktop/iscsitarg/cim-ethernetport)，但不會使用它。

</dd> <dt>

**EnabledDefault**
</dt> <dd> <dl> <dt>

資料類型： **uint16**
</dt> <dt>

存取類型：唯讀
</dt> </dl>

系統管理員的預設或啟動設定，適用于元素的啟用狀態。 這個屬性繼承自 [**CIM \_ EnabledLogicalElement**](/previous-versions//cc136818(v=vs.85)) ，而且一律設定為 2 ( 「已啟用」 ) 。

</dd> <dt>

**EnabledState**
</dt> <dd> <dl> <dt>

資料類型： **uint16**
</dt> <dt>

存取類型：唯讀
</dt> </dl>

專案的已啟用和停用狀態。 這個屬性繼承自 [**CIM \_ EnabledLogicalElement**](/previous-versions//cc136818(v=vs.85))，而且一律設定為 5 ( 「不適用」 ) 。

</dd> <dt>

**ErrorCleared**
</dt> <dd> <dl> <dt>

資料類型： **布林值**
</dt> <dt>

存取類型：唯讀
</dt> </dl>

指出現在是否已清除 **LastErrorCode** 中報告的錯誤。 這個屬性繼承自 [**CIM \_ LogicalDevice**](/windows/desktop/CIMWin32Prov/cim-logicaldevice) ，而且不會使用。

</dd> <dt>

**ErrorDescription**
</dt> <dd> <dl> <dt>

資料類型： **字串**
</dt> <dt>

存取類型：唯讀
</dt> </dl>

字串，提供 **LastErrorCode** 中所記錄錯誤的詳細資訊，以及可採取之任何矯正措施的相關資訊。 這個屬性繼承自 [**CIM \_ LogicalDevice**](/windows/desktop/CIMWin32Prov/cim-logicaldevice) ，而且不會使用。

</dd> <dt>

**FullDuplex**
</dt> <dd> <dl> <dt>

資料類型： **布林值**
</dt> <dt>

存取類型：唯讀
</dt> </dl>

指出埠是否以全雙工模式運作。 這個屬性繼承自 [**CIM \_ NetworkPort**](/previous-versions/windows/desktop/iscsitarg/cim-networkport)，而且一律設定為 **True**。

</dd> <dt>

**HealthState**
</dt> <dd> <dl> <dt>

資料類型： **uint16**
</dt> <dt>

存取類型：唯讀
</dt> </dl>

專案目前的健康情況。 這個屬性會表示此元素的健全狀況，但不一定是它的子元件。 這個屬性繼承自 [**CIM \_ ManagedSystemElement**](/windows/desktop/CIMWin32Prov/cim-managedsystemelement)，而且一律設定為 5 ( 「確定」 ) 。

</dd> <dt>

**IdentifyingDescriptions**
</dt> <dd> <dl> <dt>

資料類型： **字串** 陣列
</dt> <dt>

存取類型：唯讀
</dt> </dl>

自由格式字串的陣列，提供 **OtherIdentifyingInfo** 陣列中專案背後的說明和詳細資料。 這個陣列的每個專案都與 **OtherIdentifyingInfo** 中位於相同索引的專案相關。 這個屬性繼承自 [**CIM \_ LogicalDevice**](/windows/desktop/CIMWin32Prov/cim-logicaldevice) ，而且不會使用。

</dd> <dt>

**InstallDate**
</dt> <dd> <dl> <dt>

資料類型： **datetime**
</dt> <dt>

存取類型：唯讀
</dt> </dl>

**日期時間** 值，指出物件的安裝時間。 缺少值並不表示物件未安裝。 這個屬性繼承自 [**CIM \_ ManagedSystemElement**](/windows/desktop/CIMWin32Prov/cim-managedsystemelement)。

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

**LastErrorCode**
</dt> <dd> <dl> <dt>

資料類型： **uint32**
</dt> <dt>

存取類型：唯讀
</dt> </dl>

邏輯裝置所報告的最後一個錯誤碼。 這個屬性繼承自 [**CIM \_ LogicalDevice**](/windows/desktop/CIMWin32Prov/cim-logicaldevice) ，而且不會使用。

</dd> <dt>

**LinkTechnology**
</dt> <dd> <dl> <dt>

資料類型： **uint16**
</dt> <dt>

存取類型：唯讀
</dt> </dl>

連結的類型。 當設定為 1 ( "Other" ) 時，相關的屬性 **OtherLinkTechnology** 會包含連結類型的字串描述。 這個屬性繼承自 [**CIM \_ NetworkPort**](/previous-versions/windows/desktop/iscsitarg/cim-networkport) ，而且一律設定為 2 ( 「Ethernet」 ) 。

</dd> <dt>

**MaxDataSize**
</dt> <dd> <dl> <dt>

資料類型： **uint32**
</dt> <dt>

存取類型：唯讀
</dt> </dl>

將接收或傳送的資訊 (非 MAC) 欄位的大小上限。 這個屬性繼承自 [**CIM \_ EthernetPort**](/previous-versions/windows/desktop/iscsitarg/cim-ethernetport)，一律設為1500。

</dd> <dt>

**MaxQuiesceTime**
</dt> <dd> <dl> <dt>

資料類型： **uint64**
</dt> <dt>

存取類型：唯讀
</dt> </dl>

這個屬性繼承自 [**CIM \_ LogicalDevice**](/windows/desktop/CIMWin32Prov/cim-logicaldevice) ，而且不會使用。

</dd> <dt>

**MaxSpeed**
</dt> <dd> <dl> <dt>

資料類型： **uint64**
</dt> <dt>

存取類型：唯讀
</dt> </dl>

埠的最大頻寬（以每秒位數為單位）。 這個屬性繼承自 [**CIM \_ LogicalPort**](/previous-versions//cc136869(v=vs.85))，一律設為1000000000。

</dd> <dt>

**名稱**
</dt> <dd> <dl> <dt>

資料類型： **字串**
</dt> <dt>

存取類型：唯讀
</dt> </dl>

已知物件的標籤。 子類別化時，可以將這個屬性覆寫為索引鍵屬性。 這個屬性繼承自 [**CIM \_ ManagedSystemElement**](/windows/desktop/CIMWin32Prov/cim-managedsystemelement)，且一律設定為「Ethernet 埠」。

</dd> <dt>

**NetworkAddresses**
</dt> <dd> <dl> <dt>

資料類型： **字串** 陣列
</dt> <dt>

存取類型：唯讀
</dt> </dl>

Ethernet/802.3 MAC 位址（格式化為十二個十六進位數位） (例如 "010203040506" ) ，其中每一組代表以標準位 (順序表示之 MAC 位址的六個八位八位組中的其中一個（在字串) 的第一個字元的低序位位中找到）。 這個屬性繼承自 [**CIM \_ EthernetPort**](/previous-versions/windows/desktop/iscsitarg/cim-ethernetport) ，而且不會使用。

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

專案的目前狀態。 這個屬性繼承自 [**CIM \_ ManagedSystemElement**](/windows/desktop/CIMWin32Prov/cim-managedsystemelement)，而且一律設定為 2 ( 「確定」 ) 。

</dd> <dt>

**OtherEnabledCapabilities**
</dt> <dd> <dl> <dt>

資料類型： **字串** 陣列
</dt> <dt>

存取類型：唯讀
</dt> </dl>

自由格式字串的陣列，可針對指定為「其他」的任何已啟用功能提供更詳細的說明。 這個屬性繼承自 [**CIM \_ EthernetPort**](/previous-versions/windows/desktop/iscsitarg/cim-ethernetport) ，而且不會使用。

</dd> <dt>

**OtherEnabledState**
</dt> <dd> <dl> <dt>

資料類型： **字串**
</dt> <dt>

存取類型：唯讀
</dt> </dl>

描述當 **EnabledState** 屬性設定為 1 ( "Other" ) 時，專案已啟用或停用狀態的字串。 當 **EnabledState** 是1以外的任何值時，這個屬性必須設定為 **Null** 。 這個屬性繼承自 [**CIM \_ EnabledLogicalElement**](/previous-versions//cc136818(v=vs.85)) ，而且不會使用。

</dd> <dt>

**OtherIdentifyingInfo**
</dt> <dd> <dl> <dt>

資料類型： **字串** 陣列
</dt> <dt>

存取類型：唯讀
</dt> </dl>

除了可用來識別邏輯裝置的裝置識別碼資訊以外的任何資料。 例如，您可以使用這個屬性來保存裝置的作業系統顯示名稱。 這個屬性繼承自 [**CIM \_ LogicalDevice**](/windows/desktop/CIMWin32Prov/cim-logicaldevice) ，而且不會使用。

</dd> <dt>

**OtherLinkTechnology**
</dt> <dd> <dl> <dt>

資料類型： **字串**
</dt> <dt>

存取類型：唯讀
</dt> </dl>

當 LinkTechnology 設定為 1 ( "Other" ) 時，描述的字串值。 這個屬性繼承自 [**CIM \_ NetworkPort**](/previous-versions/windows/desktop/iscsitarg/cim-networkport)，但不會使用它。

</dd> <dt>

**OtherNetworkPortType**
</dt> <dd> <dl> <dt>

資料類型： **字串**
</dt> <dt>

存取類型：唯讀
</dt> </dl>

這個屬性會繼承自 [**CIM \_ NetworkPort**](/previous-versions/windows/desktop/iscsitarg/cim-networkport) ，而且會設定為 **Null**。

</dd> <dt>

**OtherPortType**
</dt> <dd> <dl> <dt>

資料類型： **字串**
</dt> <dt>

存取類型：唯讀
</dt> </dl>

當 **PortType** 設定為 1 ( "Other" ) 時，模組的類型。 這個屬性繼承自 [**CIM \_ LogicalPort**](/previous-versions//cc136869(v=vs.85)) ，一律設為「虛擬乙太網路」。

</dd> <dt>

**PermanentAddress**
</dt> <dd> <dl> <dt>

資料類型： **字串**
</dt> <dt>

存取類型：唯讀
</dt> </dl>

硬式編碼在埠中的網路位址。 您可以使用固件升級或軟體設定來變更此位址。 進行這項變更時，應同時更新欄位。 如果網路介面卡沒有任何硬式編碼位址，則應該保留空白。 這個屬性繼承自 [**CIM \_ NetworkPort**](/previous-versions/windows/desktop/iscsitarg/cim-networkport)。

</dd> <dt>

**PortNumber**
</dt> <dd> <dl> <dt>

資料類型： **uint16**
</dt> <dt>

存取類型：唯讀
</dt> </dl>

網路埠的編號通常相對於邏輯模組或網路元素。 這個屬性繼承自 [**CIM \_ NetworkPort**](/previous-versions/windows/desktop/iscsitarg/cim-networkport)。



| 值                                                                        | 意義                             |
|------------------------------------------------------------------------------|-------------------------------------|
| <dl> <dt>0</dt> </dl> | 未模擬 NIC。<br/> |
| <dl> <dt>1</dt> </dl> | NIC 會模擬。<br/>     |



 

</dd> <dt>

**PortType**
</dt> <dd> <dl> <dt>

資料類型： **uint16**
</dt> <dt>

存取類型：唯讀
</dt> </dl>

目前為埠啟用的特定模式。 當設定為 1 ( "Other" ) 時，相關的屬性 **OtherPortType** 會包含埠類型的字串描述。 這個屬性繼承自 [**CIM \_ EthernetPort**](/previous-versions/windows/desktop/iscsitarg/cim-ethernetport)，而且一律設定為 1 ( 「其他」 ) 。

</dd> <dt>

**PowerManagementCapabilities**
</dt> <dd> <dl> <dt>

資料類型： **uint16** 陣列
</dt> <dt>

存取類型：唯讀
</dt> </dl>

裝置的電源管理功能。 這個屬性繼承自 [**CIM \_ LogicalDevice**](/windows/desktop/CIMWin32Prov/cim-logicaldevice) ，而且不會使用。

</dd> <dt>

**PowerManagementSupported**
</dt> <dd> <dl> <dt>

資料類型： **布林值**
</dt> <dt>

存取類型：唯讀
</dt> </dl>

指出裝置是否可以受電源管理。 這個屬性繼承自 [**CIM \_ LogicalDevice**](/windows/desktop/CIMWin32Prov/cim-logicaldevice) ，而且不會使用。

</dd> <dt>

**PowerOnHours**
</dt> <dd> <dl> <dt>

資料類型： **uint64**
</dt> <dt>

存取類型：唯讀
</dt> </dl>

自上次電源週期起，此裝置已電源的連續小時數。 這個屬性繼承自 [**CIM \_ LogicalDevice**](/windows/desktop/CIMWin32Prov/cim-logicaldevice) ，而且不會使用。

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

存取類型：唯讀
</dt> </dl>

要求的埠頻寬（以每秒位數為單位）。 實際的頻寬會以 LogicalPort 報告。 這個屬性繼承自 [**CIM \_ LogicalPort**](/previous-versions//cc136869(v=vs.85))，一律設為1000000000。

</dd> <dt>

**RequestedState**
</dt> <dd> <dl> <dt>

資料類型： **uint16**
</dt> <dt>

存取類型：唯讀
</dt> </dl>

上次要求或預期的管理服務狀態。 當 **EnabledState** 設定為5時 ( 「不適用」 ) ，則此屬性不會有任何意義。 這個屬性繼承自 [**CIM \_ EnabledLogicalElement**](/previous-versions//cc136818(v=vs.85))，而且一律設定為 12 ( 「不適用」 ) 。

</dd> <dt>

**速度**
</dt> <dd> <dl> <dt>

資料類型： **uint64**
</dt> <dt>

存取類型：唯讀
</dt> </dl>

埠目前的頻寬（以每秒位數為單位）。 對於頻寬不同的埠，或無法精確估計的埠，這個屬性應該包含名義的頻寬。 這個屬性繼承自 [**CIM \_ NetworkPort**](/previous-versions/windows/desktop/iscsitarg/cim-networkport)，一律設為1000000000。

</dd> <dt>

**狀態**
</dt> <dd> <dl> <dt>

資料類型： **字串**
</dt> <dt>

存取類型：唯讀
</dt> </dl>

這個屬性繼承自 [**CIM \_ ManagedSystemElement**](/windows/desktop/CIMWin32Prov/cim-managedsystemelement)，但不會使用它。

</dd> <dt>

**StatusDescriptions**
</dt> <dd> <dl> <dt>

資料類型： **字串** 陣列
</dt> <dt>

存取類型：唯讀
</dt> </dl>

描述各種 **OperationalStatus** 陣列值的字串。 這個陣列中的專案與在 **OperationalStatus** 中相同陣列索引的專案相互關聯。 這個屬性繼承自 [**CIM \_ ManagedSystemElement**](/windows/desktop/CIMWin32Prov/cim-managedsystemelement)，而且一律設定為 "OK"。

</dd> <dt>

**StatusInfo**
</dt> <dd> <dl> <dt>

資料類型： **uint16**
</dt> <dt>

存取類型：唯讀
</dt> </dl>

邏輯裝置的狀態。 這個屬性繼承自 [**CIM \_ LogicalDevice**](/windows/desktop/CIMWin32Prov/cim-logicaldevice) ，而且不會使用。

</dd> <dt>

**SupportedMaximumTransmissionUnit**
</dt> <dd> <dl> <dt>

資料類型： **字串**
</dt> <dt>

存取類型：唯讀
</dt> <dt>

限定詞： **單位** ( "Bytes" ) 
</dt> </dl>

可支援的最大傳輸單位 (MTU) （以位元組為單位）。 這個屬性繼承自 [**CIM \_ NetworkPort**](/previous-versions/windows/desktop/iscsitarg/cim-networkport)，一律設為1500。

</dd> <dt>

**SystemCreationClassName**
</dt> <dd> <dl> <dt>

資料類型： **字串**
</dt> <dt>

存取類型：唯讀
</dt> </dl>

範圍系統的建立類別名稱。 這個屬性會繼承自 [**CIM \_ LogicalDevice**](/windows/desktop/CIMWin32Prov/cim-logicaldevice)，而且一律會設定為 "Msvm \_ 。

</dd> <dt>

**SystemName**
</dt> <dd> <dl> <dt>

資料類型： **字串**
</dt> <dt>

存取類型：唯讀
</dt> </dl>

**GUID** 形式的虛擬機器識別碼。 這個屬性繼承自 [**CIM \_ LogicalDevice**](/windows/desktop/CIMWin32Prov/cim-logicaldevice)。

</dd> <dt>

**TimeOfLastStateChange**
</dt> <dd> <dl> <dt>

資料類型： **datetime**
</dt> <dt>

存取類型：唯讀
</dt> </dl>

專案的 **EnabledState** 上次變更的日期或時間。 如果未變更元素的狀態，且已填入此屬性，則必須將它設定為0間隔值。 如果已要求狀態變更，但遭到拒絕或尚未處理，則必須更新屬性。 這個屬性繼承自 [**CIM \_ EnabledLogicalElement**](/previous-versions//cc136818(v=vs.85)) ，而且不會使用。

</dd> <dt>

**TotalPowerOnHours**
</dt> <dd> <dl> <dt>

資料類型： **uint16**
</dt> <dt>

存取類型：唯讀
</dt> </dl>

此裝置已獲得電源的總時數。 這個屬性繼承自 [**CIM \_ LogicalDevice**](/windows/desktop/CIMWin32Prov/cim-logicaldevice) ，而且不會使用。

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

在某些情況下，邏輯埠可能會識別為前端或後端埠。 如果埠的使用沒有限制，則值應該設定為 4 ( 「不受限制」 ) 。 這個屬性繼承自 [**CIM \_ LogicalPort**](/previous-versions//cc136869(v=vs.85)) ，而且一律設定為 4 ( 「不受限制」 ) 。

</dd> </dl>

## <a name="remarks"></a>備註

存取 **Msvm \_ EmulatedEthernetPort** 類別可能受 UAC 篩選所限制。 如需詳細資訊，請參閱 [使用者帳戶控制和 WMI](/windows/desktop/WmiSdk/user-account-control-and-wmi)。

## <a name="examples"></a>範例

請參閱 [查詢網路物件](querying-networking-objects.md)。

## <a name="requirements"></a>規格需求



| 需求 | 值 |
|-------------------------------------|---------------------------------------------------------------------------------------------------------|
| 最低支援的用戶端<br/> | Windows 8 \[僅限桌面應用程式\]<br/>                                                              |
| 最低支援的伺服器<br/> | Windows Server 2012 \[僅限桌面應用程式\]<br/>                                                    |
| 命名空間<br/>                | 根 \\ 虛擬化 \\ V2<br/>                                                                     |
| MOF<br/>                      | <dl> <dt>WindowsVirtualization。</dt> </dl> |
| DLL<br/>                      | <dl> <dt>Vmms.exe</dt> </dl>                     |



## <a name="see-also"></a>另請參閱

<dl> <dt>

[**CIM \_ EthernetPort**](cim-ethernetport.md)
</dt> <dt>

[**CIM \_ EthernetPort**](/previous-versions/windows/desktop/iscsitarg/cim-ethernetport)
</dt> </dl>

 

