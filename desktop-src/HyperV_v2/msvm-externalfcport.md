---
description: 表示外部光纖通道埠。
ms.assetid: bab3a243-5ebd-43e0-948e-ea8112e09d0a
title: Msvm_ExternalFcPort 類別
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Msvm_ExternalFcPort
- Msvm_ExternalFcPort.SetPowerState
- Msvm_ExternalFcPort.EnableDevice
- Msvm_ExternalFcPort.OnlineDevice
- Msvm_ExternalFcPort.QuiesceDevice
- Msvm_ExternalFcPort.SaveProperties
- Msvm_ExternalFcPort.RestoreProperties
- Msvm_ExternalFcPort.InstanceID
- Msvm_ExternalFcPort.Caption
- Msvm_ExternalFcPort.Description
- Msvm_ExternalFcPort.ElementName
- Msvm_ExternalFcPort.InstallDate
- Msvm_ExternalFcPort.Name
- Msvm_ExternalFcPort.OperationalStatus
- Msvm_ExternalFcPort.StatusDescriptions
- Msvm_ExternalFcPort.Status
- Msvm_ExternalFcPort.HealthState
- Msvm_ExternalFcPort.CommunicationStatus
- Msvm_ExternalFcPort.DetailedStatus
- Msvm_ExternalFcPort.OperatingStatus
- Msvm_ExternalFcPort.PrimaryStatus
- Msvm_ExternalFcPort.EnabledState
- Msvm_ExternalFcPort.OtherEnabledState
- Msvm_ExternalFcPort.RequestedState
- Msvm_ExternalFcPort.EnabledDefault
- Msvm_ExternalFcPort.TimeOfLastStateChange
- Msvm_ExternalFcPort.AvailableRequestedStates
- Msvm_ExternalFcPort.TransitioningToState
- Msvm_ExternalFcPort.SystemCreationClassName
- Msvm_ExternalFcPort.SystemName
- Msvm_ExternalFcPort.CreationClassName
- Msvm_ExternalFcPort.DeviceID
- Msvm_ExternalFcPort.PowerManagementSupported
- Msvm_ExternalFcPort.PowerManagementCapabilities
- Msvm_ExternalFcPort.Availability
- Msvm_ExternalFcPort.StatusInfo
- Msvm_ExternalFcPort.LastErrorCode
- Msvm_ExternalFcPort.ErrorDescription
- Msvm_ExternalFcPort.ErrorCleared
- Msvm_ExternalFcPort.OtherIdentifyingInfo
- Msvm_ExternalFcPort.PowerOnHours
- Msvm_ExternalFcPort.TotalPowerOnHours
- Msvm_ExternalFcPort.IdentifyingDescriptions
- Msvm_ExternalFcPort.AdditionalAvailability
- Msvm_ExternalFcPort.MaxQuiesceTime
- Msvm_ExternalFcPort.Speed
- Msvm_ExternalFcPort.MaxSpeed
- Msvm_ExternalFcPort.RequestedSpeed
- Msvm_ExternalFcPort.UsageRestriction
- Msvm_ExternalFcPort.PortType
- Msvm_ExternalFcPort.OtherPortType
- Msvm_ExternalFcPort.OtherNetworkPortType
- Msvm_ExternalFcPort.PortNumber
- Msvm_ExternalFcPort.LinkTechnology
- Msvm_ExternalFcPort.OtherLinkTechnology
- Msvm_ExternalFcPort.PermanentAddress
- Msvm_ExternalFcPort.NetworkAddresses
- Msvm_ExternalFcPort.FullDuplex
- Msvm_ExternalFcPort.AutoSense
- Msvm_ExternalFcPort.SupportedMaximumTransmissionUnit
- Msvm_ExternalFcPort.ActiveMaximumTransmissionUnit
- Msvm_ExternalFcPort.SupportedCOS
- Msvm_ExternalFcPort.ActiveCOS
- Msvm_ExternalFcPort.SupportedFC4Types
- Msvm_ExternalFcPort.ActiveFC4Types
- Msvm_ExternalFcPort.IsHyperVCapable
- Msvm_ExternalFcPort.WWNN
- Msvm_ExternalFcPort.WWPN
api_type:
- DllExport
api_location:
- vmms.exe
ms.openlocfilehash: 7f883afd2447c90c3167e8cf3145f8fd50ef2e72
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/07/2021
ms.locfileid: "106970842"
---
# <a name="msvm_externalfcport-class"></a>Msvm \_ ExternalFcPort 類別

> [!NOTE]
> 本文包含「從屬」一詞的參考，Microsoft 已不再使用該字詞。 從軟體中移除該字詞時，我們也會將其從本文中移除。

表示外部光纖通道埠。

下列語法已簡化受控物件格式 (MOF) 程式碼，並且包含所有繼承的屬性。

## <a name="syntax"></a>語法

``` syntax
[Dynamic, Provider("VmmsWmiInstanceAndMethodProvider"), AMENDMENT]
class Msvm_ExternalFcPort : CIM_FCPort
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
  uint16   RequestedState = 12;
  uint16   EnabledDefault = 2;
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
  uint16   SupportedCOS[];
  uint16   ActiveCOS[];
  uint16   SupportedFC4Types[];
  uint16   ActiveFC4Types[];
  boolean  IsHyperVCapable;
  string   WWNN;
  string   WWPN;
};
```

## <a name="members"></a>成員

**Msvm \_ ExternalFcPort** 類別具有下列類型的成員：

-   [方法](#methods)
-   [屬性](#properties)

### <a name="methods"></a>方法

**Msvm \_ ExternalFcPort** 類別具有這些方法。



| 方法                                                               | 描述                              |
|:---------------------------------------------------------------------|:-----------------------------------------|
| **EnableDevice**                                                     | 不支援這個方法。<br/> |
| **OnlineDevice**                                                     | 不支援這個方法。<br/> |
| **QuiesceDevice**                                                    | 不支援這個方法。<br/> |
| [**RequestStateChange**](msvm-externalfcport-requeststatechange.md) | 要求狀態變更<br/>       |
| [**重設**](msvm-externalfcport-reset.md)                           | 重設虛擬裝置。<br/>    |
| **RestoreProperties**                                                | 不支援這個方法。<br/> |
| **SaveProperties**                                                   | 不支援這個方法。<br/> |
| **SetPowerState**                                                    | 不支援這個方法。<br/> |



 

### <a name="properties"></a>屬性

**Msvm \_ ExternalFcPort** 類別具有這些屬性。

<dl> <dt>

**ActiveCOS**
</dt> <dd> <dl> <dt>

資料類型： **uint16** 陣列
</dt> <dt>

存取類型：唯讀
</dt> </dl>

整數陣列，指出作用中服務的類別。 支援的 COS 是由 **SupportedCOS** 屬性所指定。 這個屬性繼承自 **CIM \_ FCPort**。

<dl> <dt>

<span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>**未知** 的 (0) 
</dt> <dt>

<span id="1"></span>**1** (1) 
</dt> <dt>

<span id="2"></span>**2** (2) 
</dt> <dt>

<span id="3"></span>**3** (3) 
</dt> <dt>

<span id="4"></span>**4** (4) 
</dt> <dt>

<span id="5"></span>**5** (5) 
</dt> <dt>

<span id="6"></span>**6** (6) 
</dt> <dt>

<span id="F"></span><span id="f"></span>**F** (7 ) 
</dt> </dl>

</dd> <dt>

**ActiveFC4Types**
</dt> <dd> <dl> <dt>

資料類型： **uint16** 陣列
</dt> <dt>

存取類型：唯讀
</dt> </dl>

整數陣列，指出目前正在執行的光纖通道 FC-4 通訊協定。 所有支援的通訊協定清單都是由 **SupportedFC4Types** 屬性所指定。 這個屬性繼承自 **CIM \_ FCPort**。

<dl> <dt>

<span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>**未知** 的 (0) 
</dt> <dt>

<span id="Other"></span><span id="other"></span><span id="OTHER"></span>**其他** (1) 
</dt> <dt>

<span id="ISO_IEC_8802_-_2_LLC"></span><span id="iso_iec_8802_-_2_llc"></span>**ISO/IEC 8802-2 LLC** (4) 
</dt> <dt>

<span id="IP_over_FC"></span><span id="ip_over_fc"></span><span id="IP_OVER_FC"></span>透過 **FC 的 IP** (5) 
</dt> <dt>

<span id="SCSI_-_FCP"></span><span id="scsi_-_fcp"></span>**SCSI-FCP** (8) 
</dt> <dt>

<span id="SCSI_-_GPP"></span><span id="scsi_-_gpp"></span>**SCSI-GPP** (9) 
</dt> <dt>

<span id="IPI_-_3_Master"></span><span id="ipi_-_3_master"></span><span id="IPI_-_3_MASTER"></span>**IPI-3 主要** (17) 
</dt> <dt>

<span id="IPI_-_3_Slave"></span><span id="ipi_-_3_slave"></span><span id="IPI_-_3_SLAVE"></span>**IPI-3 從屬** (18) 
</dt> <dt>

<span id="IPI_-_3_Peer"></span><span id="ipi_-_3_peer"></span><span id="IPI_-_3_PEER"></span>**IPI-3 對等** (19) 
</dt> <dt>

<span id="CP_IPI_-_3_Master"></span><span id="cp_ipi_-_3_master"></span><span id="CP_IPI_-_3_MASTER"></span>**CP IPI-3 主要** (21) 
</dt> <dt>

<span id="CP_IPI_-_3_Slave"></span><span id="cp_ipi_-_3_slave"></span><span id="CP_IPI_-_3_SLAVE"></span>**CP IPI-3 從屬** (22) 
</dt> <dt>

<span id="CP_IPI_-_3_Peer"></span><span id="cp_ipi_-_3_peer"></span><span id="CP_IPI_-_3_PEER"></span>**CP IPI-3 對等** (23) 
</dt> <dt>

<span id="SBCCS_Channel"></span><span id="sbccs_channel"></span><span id="SBCCS_CHANNEL"></span>**SBCCS Channel** (25) 
</dt> <dt>

<span id="SBCCS_Control_Unit"></span><span id="sbccs_control_unit"></span><span id="SBCCS_CONTROL_UNIT"></span>**SBCCS Control Unit** (26) 
</dt> <dt>

<span id="FC-SB-2_Channel"></span><span id="fc-sb-2_channel"></span><span id="FC-SB-2_CHANNEL"></span>**FC-SB-2 Channel** (27) 
</dt> <dt>

<span id="FC-SB-2_Control_Unit"></span><span id="fc-sb-2_control_unit"></span><span id="FC-SB-2_CONTROL_UNIT"></span>**FC-SB-2 控制單位** (28) 
</dt> <dt>

<span id="Fibre_Channel_Services__FC-GS__FC-GS-2__FC-GS-3_"></span><span id="fibre_channel_services__fc-gs__fc-gs-2__fc-gs-3_"></span><span id="FIBRE_CHANNEL_SERVICES__FC-GS__FC-GS-2__FC-GS-3_"></span>**光纖通道 Services (fc-gs、fc-gs-2、fc-gs-3)** (32) 
</dt> <dt>

<span id="FC-SW"></span><span id="fc-sw"></span>**FC-SW** (34) 
</dt> <dt>

<span id="FC_-_SNMP"></span><span id="fc_-_snmp"></span>**FC-SNMP** (36) 
</dt> <dt>

<span id="HIPPI_-_FP"></span><span id="hippi_-_fp"></span>**HIPPI-FP** (64) 
</dt> <dt>

<span id="BBL_Control"></span><span id="bbl_control"></span><span id="BBL_CONTROL"></span>**BBL Control** (80) 
</dt> <dt>

<span id="BBL_FDDI_Encapsulated_LAN_PDU"></span><span id="bbl_fddi_encapsulated_lan_pdu"></span><span id="BBL_FDDI_ENCAPSULATED_LAN_PDU"></span>**BBL FDDI 封裝區域網路 PDU** (81) 
</dt> <dt>

<span id="BBL_802.3_Encapsulated_LAN_PDU"></span><span id="bbl_802.3_encapsulated_lan_pdu"></span><span id="BBL_802.3_ENCAPSULATED_LAN_PDU"></span>**BBL 802.3 封裝的 LAN PDU** (82) 
</dt> <dt>

<span id="FC_-_VI"></span><span id="fc_-_vi"></span>**FC-VI** (88) 
</dt> <dt>

<span id="FC_-_AV"></span><span id="fc_-_av"></span>**FC-AV** (96) 
</dt> <dt>

<span id="Vendor_unique"></span><span id="vendor_unique"></span><span id="VENDOR_UNIQUE"></span>**廠商唯一** (255) 
</dt> </dl>

</dd> <dt>

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

裝置的任何額外可用性和狀態。 這個屬性繼承自 [**CIM \_ LogicalDevice**](/windows/desktop/CIMWin32Prov/cim-logicaldevice)，但不會使用它。

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

裝置的主要可用性和狀態。 這個屬性繼承自 [**CIM \_ LogicalDevice**](/windows/desktop/CIMWin32Prov/cim-logicaldevice)，但不會使用它。

</dd> <dt>

**AvailableRequestedStates**
</dt> <dd> <dl> <dt>

資料類型： **uint16** 陣列
</dt> <dt>

存取類型：唯讀
</dt> </dl>

指出 **RequestStateChange** 方法的 *RequestedState* 參數可能的值。 這個屬性繼承自 [**CIM \_ EnabledLogicalElement**](/previous-versions//cc136818(v=vs.85))，而且一律設定為 **Null**。

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

<dl> <dt>

<span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>**未知** 的 (0) 
</dt> <dt>

<span id="Not_Available"></span><span id="not_available"></span><span id="NOT_AVAILABLE"></span> (1) **無法使用**
</dt> <dt>

<span id="Communication_OK"></span><span id="communication_ok"></span><span id="COMMUNICATION_OK"></span>**通訊正常** (2) 
</dt> <dt>

<span id="Lost_Communication"></span><span id="lost_communication"></span><span id="LOST_COMMUNICATION"></span>**遺失通訊** (3) 
</dt> <dt>

<span id="No_Contact"></span><span id="no_contact"></span><span id="NO_CONTACT"></span>**沒有連絡人** (4) 
</dt> <dt>

<span id="DMTF_Reserved"></span><span id="dmtf_reserved"></span><span id="DMTF_RESERVED"></span>**DMTF 保留** ( .。。) 
</dt> <dt>

<span id="Vendor_Reserved_"></span><span id="vendor_reserved_"></span><span id="VENDOR_RESERVED_"></span>**廠商保留** (0x8000。 )
</dt> </dl>

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

補充 **PrimaryStatus** 屬性與其他狀態詳細資料。 **Null** 值表示不會執行此屬性。 這個屬性繼承自 [**CIM \_ ManagedSystemElement**](/windows/desktop/CIMWin32Prov/cim-managedsystemelement)。

<dl> <dt>

<span id="Not_Available"></span><span id="not_available"></span><span id="NOT_AVAILABLE"></span> (0) **無法使用**
</dt> <dt>

<span id="No_Additional_Information"></span><span id="no_additional_information"></span><span id="NO_ADDITIONAL_INFORMATION"></span>**沒有其他資訊** (1) 
</dt> <dt>

<span id="Stressed"></span><span id="stressed"></span><span id="STRESSED"></span>**壓力** (2) 
</dt> <dt>

<span id="Predictive_Failure"></span><span id="predictive_failure"></span><span id="PREDICTIVE_FAILURE"></span>**預測性失敗** (3) 
</dt> <dt>

<span id="Non-Recoverable_Error"></span><span id="non-recoverable_error"></span><span id="NON-RECOVERABLE_ERROR"></span>**無法復原的錯誤** (4) 
</dt> <dt>

<span id="Supporting_Entity_in_Error"></span><span id="supporting_entity_in_error"></span><span id="SUPPORTING_ENTITY_IN_ERROR"></span>**錯誤中的支援實體** (5) 
</dt> <dt>

<span id="DMTF_Reserved"></span><span id="dmtf_reserved"></span><span id="DMTF_RESERVED"></span>**DMTF 保留** ( .。。) 
</dt> <dt>

<span id="Vendor_Reserved_"></span><span id="vendor_reserved_"></span><span id="VENDOR_RESERVED_"></span>**廠商保留** (0x8000。 )
</dt> </dl>

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

系統管理員的預設或啟動設定，適用于元素的 **EnabledState** 屬性。 這個屬性繼承自 [**CIM \_ EnabledLogicalElement**](/previous-versions//cc136818(v=vs.85))，而且一律設定為 2 (啟用) 。

</dd> <dt>

**EnabledState**
</dt> <dd> <dl> <dt>

資料類型： **uint16**
</dt> <dt>

存取類型：唯讀
</dt> </dl>

專案的已啟用和停用狀態。 這個屬性繼承自 [**CIM \_ EnabledLogicalElement**](/previous-versions//cc136818(v=vs.85))，它會是下列其中一個值。



| 值                                                                                                                                                                                                                                                                       | 意義                                                                                                                                                                                                                |
|-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span><dl> <dt>**未知**</dt>的 <dt>0</dt> </dl>                                                 | 無法判斷元素的狀態。<br/>                                                                                                                                                           |
| <span id="Other"></span><span id="other"></span><span id="OTHER"></span><dl> <dt>**其他**</dt> <dt>1</dt> </dl>                                                         |                                                                                                                                                                                                                        |
| <span id="Enabled"></span><span id="enabled"></span><span id="ENABLED"></span><dl> <dt>**已啟用**</dt> <dt>2</dt> </dl>                                                 | 元素正在執行。<br/>                                                                                                                                                                                     |
| <span id="Disabled"></span><span id="disabled"></span><span id="DISABLED"></span><dl> <dt>**停用**</dt> <dt>3</dt> </dl>                                             | 元素已關閉。<br/>                                                                                                                                                                                  |
| <span id="Shutting_Down"></span><span id="shutting_down"></span><span id="SHUTTING_DOWN"></span><dl> 正在 <dt>**關閉**</dt> <dt>4</dt> </dl>                         | 專案正在進入已停用狀態的進程。<br/>                                                                                                                                                 |
| <span id="Not_Applicable"></span><span id="not_applicable"></span><span id="NOT_APPLICABLE"></span><dl> <dt>**不適用**</dt> <dt>5</dt> </dl>                     | 元素不支援啟用或停用。<br/>                                                                                                                                                     |
| <span id="Enabled_but_Offline"></span><span id="enabled_but_offline"></span><span id="ENABLED_BUT_OFFLINE"></span><dl> <dt>**已啟用但離線**</dt> <dt>6</dt> </dl> | 元素可能正在完成命令，而且會捨棄任何新的要求。<br/>                                                                                                                                |
| <span id="In_Test"></span><span id="in_test"></span><span id="IN_TEST"></span><dl> <dt>**在測試**</dt> <dt>7</dt>中 </dl>                                                 | 元素處於測試狀態。<br/>                                                                                                                                                                             |
| <span id="Deferred"></span><span id="deferred"></span><span id="DEFERRED"></span><dl> <dt>**延**</dt>後 <dt>8</dt> </dl>                                             | 元素可能正在完成命令，但它會將任何新的要求排在佇列中。<br/>                                                                                                                               |
| <span id="Quiesce"></span><span id="quiesce"></span><span id="QUIESCE"></span><dl> <dt>**靜止**</dt> <dt>9</dt> </dl>                                                 | 已啟用元素，但它處於受限模式。 專案的行為類似于啟用狀態 (2) ，但只會處理一組受限制的命令。 所有其他要求則會排入佇列。<br/> |
| <span id="Starting"></span><span id="starting"></span><span id="STARTING"></span><dl> <dt>**起始**</dt> <dt>10</dt> </dl>                                            | 元素正在進入啟用狀態 (2) 。 新的要求會排入佇列。<br/>                                                                                                                    |



 

</dd> <dt>

**ErrorCleared**
</dt> <dd> <dl> <dt>

資料類型： **布林值**
</dt> <dt>

存取類型：唯讀
</dt> </dl>

指出現在是否已清除 **LastErrorCode** 中報告的錯誤。 這個屬性繼承自 [**CIM \_ LogicalDevice**](/windows/desktop/CIMWin32Prov/cim-logicaldevice)，但不會使用它。

</dd> <dt>

**ErrorDescription**
</dt> <dd> <dl> <dt>

資料類型： **字串**
</dt> <dt>

存取類型：唯讀
</dt> </dl>

字串，提供 **LastErrorCode** 中所記錄錯誤的詳細資訊，以及可採取之任何矯正措施的相關資訊。 這個屬性繼承自 [**CIM \_ LogicalDevice**](/windows/desktop/CIMWin32Prov/cim-logicaldevice)，但不會使用它。

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

自由格式字串的陣列，可提供 **OtherIdentifyingInfo** 屬性陣列中專案背後的說明和詳細資料。 這個屬性繼承自 [**CIM \_ LogicalDevice**](/windows/desktop/CIMWin32Prov/cim-logicaldevice)，但不會使用它。

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

**IsHyperVCapable**
</dt> <dd> <dl> <dt>

資料類型： **布林值**
</dt> <dt>

存取類型：唯讀
</dt> </dl>

如果此屬性為 **True**，則此光纖通道埠可以連線至交換器，因此可提供虛擬機器的連線能力。 如果此屬性為 **False**，則虛擬機器無法使用此埠光纖通道架構。

</dd> <dt>

**LastErrorCode**
</dt> <dd> <dl> <dt>

資料類型： **uint32**
</dt> <dt>

存取類型：唯讀
</dt> </dl>

邏輯裝置所報告的最後一個錯誤碼。 這個屬性繼承自 [**CIM \_ LogicalDevice**](/windows/desktop/CIMWin32Prov/cim-logicaldevice)，但不會使用它。

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

這個屬性已被取代。 這個屬性繼承自 [**CIM \_ LogicalDevice**](/windows/desktop/CIMWin32Prov/cim-logicaldevice)，但不會使用它。

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

<dl> <dt>

<span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>**未知** 的 (0) 
</dt> <dt>

<span id="Not_Available"></span><span id="not_available"></span><span id="NOT_AVAILABLE"></span> (1) **無法使用**
</dt> <dt>

<span id="Servicing"></span><span id="servicing"></span><span id="SERVICING"></span>**服務** (2) 
</dt> <dt>

<span id="Starting"></span><span id="starting"></span><span id="STARTING"></span>**開始** (3) 
</dt> <dt>

<span id="Stopping"></span><span id="stopping"></span><span id="STOPPING"></span>**停止** (4) 
</dt> <dt>

<span id="Stopped"></span><span id="stopped"></span><span id="STOPPED"></span>**已停止** (5) 
</dt> <dt>

<span id="Aborted"></span><span id="aborted"></span><span id="ABORTED"></span>已 **中止** (6) 
</dt> <dt>

<span id="Dormant"></span><span id="dormant"></span><span id="DORMANT"></span>**休眠** (7) 
</dt> <dt>

<span id="Completed"></span><span id="completed"></span><span id="COMPLETED"></span>**已完成** (8) 
</dt> <dt>

<span id="Migrating"></span><span id="migrating"></span><span id="MIGRATING"></span>**遷移** (9) 
</dt> <dt>

<span id="Emigrating"></span><span id="emigrating"></span><span id="EMIGRATING"></span>**Emigrating** (10) 
</dt> <dt>

<span id="Immigrating"></span><span id="immigrating"></span><span id="IMMIGRATING"></span>**Immigrating** (11) 
</dt> <dt>

<span id="Snapshotting"></span><span id="snapshotting"></span><span id="SNAPSHOTTING"></span>**快照** (12) 
</dt> <dt>

<span id="Shutting_Down"></span><span id="shutting_down"></span><span id="SHUTTING_DOWN"></span>正在 **關閉** (13) 
</dt> <dt>

<span id="In_Test"></span><span id="in_test"></span><span id="IN_TEST"></span>**在測試** (14) 
</dt> <dt>

<span id="Transitioning"></span><span id="transitioning"></span><span id="TRANSITIONING"></span>**轉換** (15) 
</dt> <dt>

<span id="In_Service"></span><span id="in_service"></span><span id="IN_SERVICE"></span>**在服務** (16) 
</dt> <dt>

<span id="DMTF_Reserved"></span><span id="dmtf_reserved"></span><span id="DMTF_RESERVED"></span>**DMTF 保留** ( .。。) 
</dt> <dt>

<span id="Vendor_Reserved_"></span><span id="vendor_reserved_"></span><span id="VENDOR_RESERVED_"></span>**廠商保留** (0x8000。 )
</dt> </dl>

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

描述當 **EnabledState** 屬性設定為 1 (其他) 時，專案已啟用或停用狀態的字串。 當 **EnabledState** 屬性是1以外的任何值時，這個屬性必須設定為 **Null** 。 這個屬性繼承自 [**CIM \_ EnabledLogicalElement**](/previous-versions//cc136818(v=vs.85))，而且一律設定為 **Null**。

</dd> <dt>

**OtherIdentifyingInfo**
</dt> <dd> <dl> <dt>

資料類型： **字串** 陣列
</dt> <dt>

存取類型：唯讀
</dt> </dl>

除了裝置識別碼資訊以外的任何其他資料，可用來識別邏輯裝置。 這個屬性繼承自 [**CIM \_ LogicalDevice**](/windows/desktop/CIMWin32Prov/cim-logicaldevice)，但不會使用它。

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

裝置的電源管理功能。 這個屬性繼承自 [**CIM \_ LogicalDevice**](/windows/desktop/CIMWin32Prov/cim-logicaldevice)，但不會使用它。

</dd> <dt>

**PowerManagementSupported**
</dt> <dd> <dl> <dt>

資料類型： **布林值**
</dt> <dt>

存取類型：唯讀
</dt> </dl>

指出裝置是否可以受電源管理。 這個屬性繼承自 [**CIM \_ LogicalDevice**](/windows/desktop/CIMWin32Prov/cim-logicaldevice)，但不會使用它。

</dd> <dt>

**PowerOnHours**
</dt> <dd> <dl> <dt>

資料類型： **uint64**
</dt> <dt>

存取類型：唯讀
</dt> </dl>

此裝置自上一次電源週期起開啟電源的連續小時數。 這個屬性繼承自 [**CIM \_ LogicalDevice**](/windows/desktop/CIMWin32Prov/cim-logicaldevice)，但不會使用它。

</dd> <dt>

**PrimaryStatus**
</dt> <dd> <dl> <dt>

資料類型： **uint16**
</dt> <dt>

存取類型：唯讀
</dt> </dl>

提供高層級的狀態資訊。 這個屬性應該與 **DetailedStatus** 屬性一起使用，以提供元素和其子元件的高階和詳細健全狀況狀態。 **Null** 值表示不會執行此屬性。 這個屬性繼承自 [**CIM \_ ManagedSystemElement**](/windows/desktop/CIMWin32Prov/cim-managedsystemelement)。

<dl> <dt>

<span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>**未知** 的 (0) 
</dt> <dt>

<span id="OK"></span><span id="ok"></span>**確定** (1) 
</dt> <dt>

<span id="Degraded"></span><span id="degraded"></span><span id="DEGRADED"></span> (2) **降級**
</dt> <dt>

<span id="Error"></span><span id="error"></span><span id="ERROR"></span>**錯誤** (3) 
</dt> <dt>

<span id="DMTF_Reserved"></span><span id="dmtf_reserved"></span><span id="DMTF_RESERVED"></span>**DMTF 保留** ( .。。) 
</dt> <dt>

<span id="Vendor_Reserved_"></span><span id="vendor_reserved_"></span><span id="VENDOR_RESERVED_"></span>**廠商保留** (0x8000。 )
</dt> </dl>

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

上次要求或預期的專案狀態。 這個屬性繼承自 [**CIM \_ EnabledLogicalElement**](/previous-versions//cc136818(v=vs.85))，而且一律設定為 12 (不適用) 。

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

物件的目前狀態。 這個屬性繼承自 [**CIM \_ ManagedSystemElement**](/windows/desktop/CIMWin32Prov/cim-managedsystemelement)，但不會使用它。

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

邏輯裝置的目前狀態。 這個屬性繼承自 [**CIM \_ LogicalDevice**](/windows/desktop/CIMWin32Prov/cim-logicaldevice)，但不會使用它。

</dd> <dt>

**SupportedCOS**
</dt> <dd> <dl> <dt>

資料類型： **uint16** 陣列
</dt> <dt>

存取類型：唯讀
</dt> </dl>

整數陣列，表示支援的光纖通道服務 (COS) 類別。 作用中的 COS 是由 **ActiveCOS** 屬性所指定。 這個屬性繼承自 **CIM \_ FCPort**。

<dl> <dt>

<span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>**未知** 的 (0) 
</dt> <dt>

<span id="1"></span>**1** (1) 
</dt> <dt>

<span id="2"></span>**2** (2) 
</dt> <dt>

<span id="3"></span>**3** (3) 
</dt> <dt>

<span id="4"></span>**4** (4) 
</dt> <dt>

<span id="5"></span>**5** (5) 
</dt> <dt>

<span id="6"></span>**6** (6) 
</dt> <dt>

<span id="F_"></span><span id="f_"></span>**F** (7 ) 
</dt> </dl>

</dd> <dt>

**SupportedFC4Types**
</dt> <dd> <dl> <dt>

資料類型： **uint16** 陣列
</dt> <dt>

存取類型：唯讀
</dt> </dl>

整數陣列，表示支援的光纖通道 FC-4 通訊協定。 作用中且正在執行的通訊協定是由 **ActiveFC4Types** 屬性所指定。 這個屬性繼承自 **CIM \_ FCPort**。

<dl> <dt>

<span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>**未知** 的 (0) 
</dt> <dt>

<span id="Other"></span><span id="other"></span><span id="OTHER"></span>**其他** (1) 
</dt> <dt>

<span id="ISO_IEC_8802_-_2_LLC"></span><span id="iso_iec_8802_-_2_llc"></span>**ISO/IEC 8802-2 LLC** (4) 
</dt> <dt>

<span id="IP_over_FC"></span><span id="ip_over_fc"></span><span id="IP_OVER_FC"></span>透過 **FC 的 IP** (5) 
</dt> <dt>

<span id="SCSI_-_FCP"></span><span id="scsi_-_fcp"></span>**SCSI-FCP** (8) 
</dt> <dt>

<span id="SCSI_-_GPP"></span><span id="scsi_-_gpp"></span>**SCSI-GPP** (9) 
</dt> <dt>

<span id="IPI_-_3_Master"></span><span id="ipi_-_3_master"></span><span id="IPI_-_3_MASTER"></span>**IPI-3 主要** (17) 
</dt> <dt>

<span id="IPI_-_3_Slave"></span><span id="ipi_-_3_slave"></span><span id="IPI_-_3_SLAVE"></span>**IPI-3 從屬** (18) 
</dt> <dt>

<span id="IPI_-_3_Peer"></span><span id="ipi_-_3_peer"></span><span id="IPI_-_3_PEER"></span>**IPI-3 對等** (19) 
</dt> <dt>

<span id="CP_IPI_-_3_Master"></span><span id="cp_ipi_-_3_master"></span><span id="CP_IPI_-_3_MASTER"></span>**CP IPI-3 主要** (21) 
</dt> <dt>

<span id="CP_IPI_-_3_Slave"></span><span id="cp_ipi_-_3_slave"></span><span id="CP_IPI_-_3_SLAVE"></span>**CP IPI-3 從屬** (22) 
</dt> <dt>

<span id="CP_IPI_-_3_Peer"></span><span id="cp_ipi_-_3_peer"></span><span id="CP_IPI_-_3_PEER"></span>**CP IPI-3 對等** (23) 
</dt> <dt>

<span id="SBCCS_Channel"></span><span id="sbccs_channel"></span><span id="SBCCS_CHANNEL"></span>**SBCCS Channel** (25) 
</dt> <dt>

<span id="SBCCS_Control_Unit"></span><span id="sbccs_control_unit"></span><span id="SBCCS_CONTROL_UNIT"></span>**SBCCS Control Unit** (26) 
</dt> <dt>

<span id="FC-SB-2_Channel"></span><span id="fc-sb-2_channel"></span><span id="FC-SB-2_CHANNEL"></span>**FC-SB-2 Channel** (27) 
</dt> <dt>

<span id="FC-SB-2_Control_Unit"></span><span id="fc-sb-2_control_unit"></span><span id="FC-SB-2_CONTROL_UNIT"></span>**FC-SB-2 控制單位** (28) 
</dt> <dt>

<span id="Fibre_Channel_Services__FC-GS__FC-GS-2__FC-GS-3_"></span><span id="fibre_channel_services__fc-gs__fc-gs-2__fc-gs-3_"></span><span id="FIBRE_CHANNEL_SERVICES__FC-GS__FC-GS-2__FC-GS-3_"></span>**光纖通道 Services (fc-gs、fc-gs-2、fc-gs-3)** (32) 
</dt> <dt>

<span id="FC-SW"></span><span id="fc-sw"></span>**FC-SW** (34) 
</dt> <dt>

<span id="FC_-_SNMP"></span><span id="fc_-_snmp"></span>**FC-SNMP** (36) 
</dt> <dt>

<span id="HIPPI_-_FP"></span><span id="hippi_-_fp"></span>**HIPPI-FP** (64) 
</dt> <dt>

<span id="BBL_Control"></span><span id="bbl_control"></span><span id="BBL_CONTROL"></span>**BBL Control** (80) 
</dt> <dt>

<span id="BBL_FDDI_Encapsulated_LAN_PDU"></span><span id="bbl_fddi_encapsulated_lan_pdu"></span><span id="BBL_FDDI_ENCAPSULATED_LAN_PDU"></span>**BBL FDDI 封裝區域網路 PDU** (81) 
</dt> <dt>

<span id="BBL_802.3_Encapsulated_LAN_PDU"></span><span id="bbl_802.3_encapsulated_lan_pdu"></span><span id="BBL_802.3_ENCAPSULATED_LAN_PDU"></span>**BBL 802.3 封裝的 LAN PDU** (82) 
</dt> <dt>

<span id="FC_-_VI"></span><span id="fc_-_vi"></span>**FC-VI** (88) 
</dt> <dt>

<span id="FC_-_AV"></span><span id="fc_-_av"></span>**FC-AV** (96) 
</dt> <dt>

<span id="Vendor_unique"></span><span id="vendor_unique"></span><span id="VENDOR_UNIQUE"></span>**廠商唯一** (255) 
</dt> </dl>

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

專案的已啟用狀態上次變更的日期或時間。 這個屬性繼承自 [**CIM \_ EnabledLogicalElement**](/previous-versions//cc136818(v=vs.85))，而且一律設定為 **Null**。

</dd> <dt>

**TotalPowerOnHours**
</dt> <dd> <dl> <dt>

資料類型： **uint64**
</dt> <dt>

存取類型：唯讀
</dt> </dl>

此裝置已獲得電源的總時數。 這個屬性繼承自 [**CIM \_ LogicalDevice**](/windows/desktop/CIMWin32Prov/cim-logicaldevice)，但不會使用它。

</dd> <dt>

**TransitioningToState**
</dt> <dd> <dl> <dt>

資料類型： **uint16**
</dt> <dt>

存取類型：唯讀
</dt> </dl>

指出實例正在轉換的目標狀態。 這個屬性繼承自 [**CIM \_ EnabledLogicalElement**](/previous-versions//cc136818(v=vs.85))，而且一律設定為 **Null**。

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

</dd> <dt>

**WWNN**
</dt> <dd> <dl> <dt>

資料類型： **字串**
</dt> <dt>

存取類型：唯讀
</dt> </dl>

此光纖通道埠的全球節點名稱。

</dd> <dt>

**WWPN**
</dt> <dd> <dl> <dt>

資料類型： **字串**
</dt> <dt>

存取類型：唯讀
</dt> </dl>

此光纖通道埠的全球埠名稱。

</dd> </dl>

## <a name="requirements"></a>規格需求



| 需求 | 值 |
|-------------------------------------|---------------------------------------------------------------------------------------------------------|
| 最低支援的用戶端<br/> | \[僅 Windows 8 桌面應用程式\]<br/>                                                              |
| 最低支援的伺服器<br/> | 僅限 Windows Server 2012 \[ desktop 應用程式\]<br/>                                                    |
| 命名空間<br/>                | 根 \\ 虛擬化 \\ V2<br/>                                                                     |
| MOF<br/>                      | <dl> <dt>WindowsVirtualization。</dt> </dl> |
| DLL<br/>                      | <dl> <dt>Vmms.exe</dt> </dl>                     |



 

