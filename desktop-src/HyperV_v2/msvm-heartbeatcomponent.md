---
description: 表示心跳服務的狀態，此服務會透過定期報告心跳來負責監視虛擬機器的狀態。
ms.assetid: 72DB3CD9-B083-4483-BCCD-DC8C140DDBF4
title: Msvm_HeartbeatComponent 類別
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Msvm_HeartbeatComponent
- Msvm_HeartbeatComponent.SetPowerState
- Msvm_HeartbeatComponent.EnableDevice
- Msvm_HeartbeatComponent.OnlineDevice
- Msvm_HeartbeatComponent.QuiesceDevice
- Msvm_HeartbeatComponent.SaveProperties
- Msvm_HeartbeatComponent.RestoreProperties
- Msvm_HeartbeatComponent.InstanceID
- Msvm_HeartbeatComponent.Caption
- Msvm_HeartbeatComponent.Description
- Msvm_HeartbeatComponent.ElementName
- Msvm_HeartbeatComponent.InstallDate
- Msvm_HeartbeatComponent.Name
- Msvm_HeartbeatComponent.OperationalStatus
- Msvm_HeartbeatComponent.StatusDescriptions
- Msvm_HeartbeatComponent.Status
- Msvm_HeartbeatComponent.HealthState
- Msvm_HeartbeatComponent.CommunicationStatus
- Msvm_HeartbeatComponent.DetailedStatus
- Msvm_HeartbeatComponent.OperatingStatus
- Msvm_HeartbeatComponent.PrimaryStatus
- Msvm_HeartbeatComponent.EnabledState
- Msvm_HeartbeatComponent.OtherEnabledState
- Msvm_HeartbeatComponent.RequestedState
- Msvm_HeartbeatComponent.EnabledDefault
- Msvm_HeartbeatComponent.TimeOfLastStateChange
- Msvm_HeartbeatComponent.AvailableRequestedStates
- Msvm_HeartbeatComponent.TransitioningToState
- Msvm_HeartbeatComponent.SystemCreationClassName
- Msvm_HeartbeatComponent.SystemName
- Msvm_HeartbeatComponent.CreationClassName
- Msvm_HeartbeatComponent.DeviceID
- Msvm_HeartbeatComponent.PowerManagementSupported
- Msvm_HeartbeatComponent.PowerManagementCapabilities
- Msvm_HeartbeatComponent.Availability
- Msvm_HeartbeatComponent.StatusInfo
- Msvm_HeartbeatComponent.LastErrorCode
- Msvm_HeartbeatComponent.ErrorDescription
- Msvm_HeartbeatComponent.ErrorCleared
- Msvm_HeartbeatComponent.OtherIdentifyingInfo
- Msvm_HeartbeatComponent.PowerOnHours
- Msvm_HeartbeatComponent.TotalPowerOnHours
- Msvm_HeartbeatComponent.IdentifyingDescriptions
- Msvm_HeartbeatComponent.AdditionalAvailability
- Msvm_HeartbeatComponent.MaxQuiesceTime
api_type:
- DllExport
api_location:
- vmms.exe
ms.openlocfilehash: bdea278fb6fdce57e938ce3cf2e53f8f453cbd98e73591c6710341157683e3b9
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/11/2021
ms.locfileid: "118147814"
---
# <a name="msvm_heartbeatcomponent-class"></a>Msvm \_ HeartbeatComponent 類別

表示心跳服務的狀態，此服務會透過定期報告心跳來負責監視虛擬機器的狀態。

下列語法已簡化受控物件格式 (MOF) 程式碼，並且包含所有繼承的屬性。

## <a name="syntax"></a>語法

``` syntax
[Dynamic, Provider("VmmsWmiInstanceAndMethodProvider"), AMENDMENT]
class Msvm_HeartbeatComponent : CIM_LogicalDevice
{
  string   InstanceID;
  string   Caption = "Heartbeat";
  string   Description = "Microsoft Heartbeat Service";
  string   ElementName = "Heartbeat";
  datetime InstallDate;
  string   Name;
  uint16   OperationalStatus[];
  string   StatusDescriptions[];
  string   Status;
  uint16   HealthState = 5;
  uint16   CommunicationStatus;
  uint16   DetailedStatus;
  uint16   OperatingStatus;
  uint16   PrimaryStatus;
  uint16   EnabledState = 2;
  string   OtherEnabledState;
  uint16   RequestedState = 12;
  uint16   EnabledDefault = 7;
  datetime TimeOfLastStateChange;
  uint16   AvailableRequestedStates[];
  uint16   TransitioningToState;
  string   SystemCreationClassName = "Msvm_ComputerSystem";
  string   SystemName;
  string   CreationClassName = "Msvm_HeartbeatComponent";
  string   DeviceID = "Microsoft:VMGUID\GUID";
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
  uint16   AdditionalAvailability[] = 6;
  uint64   MaxQuiesceTime;
};
```

## <a name="members"></a>成員

**Msvm \_ HeartbeatComponent** 類別具有下列類型的成員：

-   [方法](#methods)
-   [屬性](#properties)

### <a name="methods"></a>方法

**Msvm \_ HeartbeatComponent** 類別具有這些方法。



| 方法                                                                   | 描述                              |
|:-------------------------------------------------------------------------|:-----------------------------------------|
| **EnableDevice**                                                         | 不支援這個方法。<br/> |
| **OnlineDevice**                                                         | 不支援這個方法。<br/> |
| **QuiesceDevice**                                                        | 不支援這個方法。<br/> |
| [**RequestStateChange**](msvm-heartbeatcomponent-requeststatechange.md) | 要求狀態變更。<br/>      |
| [**重設**](msvm-heartbeatcomponent-reset.md)                           | 重設虛擬裝置。<br/>    |
| **RestoreProperties**                                                    | 不支援這個方法。<br/> |
| **SaveProperties**                                                       | 不支援這個方法。<br/> |
| **SetPowerState**                                                        | 不支援這個方法。<br/> |



 

### <a name="properties"></a>屬性

**Msvm \_ HeartbeatComponent** 類別具有這些屬性。

<dl> <dt>

**AdditionalAvailability**
</dt> <dd> <dl> <dt>

資料類型： **uint16** 陣列
</dt> <dt>

存取類型：唯讀
</dt> </dl>

裝置的任何額外可用性和狀態。 這個屬性繼承自 [**CIM \_ LogicalDevice**](/windows/desktop/CIMWin32Prov/cim-logicaldevice)，而且一律設定為 6 (不適用) 。

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

物件的簡短描述。 這個屬性繼承自 [**CIM \_ ManagedElement**](/previous-versions/windows/desktop/iscsitarg/cim-managedelement) 類別，且一律設定為「心跳」。

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

範圍系統的建立類別名稱。 這個屬性繼承自 [**CIM \_ LogicalDevice**](/windows/desktop/CIMWin32Prov/cim-logicaldevice)，而且一律設定為 "Msvm \_ HeartbeatComponent"。

</dd> <dt>

**說明**
</dt> <dd> <dl> <dt>

資料類型： **字串**
</dt> <dt>

存取類型：唯讀
</dt> </dl>

對物件的描述。 這個屬性繼承自 [**CIM \_ ManagedElement**](/previous-versions/windows/desktop/iscsitarg/cim-managedelement)，一律設為「Microsoft 心跳服務」。

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

用來唯一命名邏輯裝置的位址或其他識別資訊。 這個屬性繼承自 [**CIM \_ LogicalDevice**](/windows/desktop/CIMWin32Prov/cim-logicaldevice)，而且一律設定為 "Microsoft：*VMGUID* \\ *GUID*"，其中 *VMGUID* 是與此裝置相關聯之 [**Msvm 的 \_**](msvm-computersystem.md) [**名稱**] 屬性。

</dd> <dt>

**ElementName**
</dt> <dd> <dl> <dt>

資料類型： **字串**
</dt> <dt>

存取類型：唯讀
</dt> </dl>

物件的顯示名稱。 這個屬性是從 [**CIM \_ ManagedElement**](/previous-versions/windows/desktop/iscsitarg/cim-managedelement)繼承而來，而且一律會設定為「心跳」。

</dd> <dt>

**EnabledDefault**
</dt> <dd> <dl> <dt>

資料類型： **uint16**
</dt> <dt>

存取類型：唯讀
</dt> </dl>

這個屬性繼承自 [**CIM \_ EnabledLogicalElement**](/previous-versions//cc136818(v=vs.85))，而且一律設定為 7 (沒有預設) 。

</dd> <dt>

**EnabledState**
</dt> <dd> <dl> <dt>

資料類型： **uint16**
</dt> <dt>

存取類型：唯讀
</dt> </dl>

專案的已啟用和停用狀態。 這個屬性會繼承自 [**CIM \_ EnabledLogicalElement**](/previous-versions//cc136818(v=vs.85)) ，而且會是下列其中一個值。



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

指出現在是否已清除 **LastErrorCode** 中報告的錯誤。 這個屬性會繼承自 [**CIM \_ LogicalDevice**](/windows/desktop/CIMWin32Prov/cim-logicaldevice) ，但不會使用。

</dd> <dt>

**ErrorDescription**
</dt> <dd> <dl> <dt>

資料類型： **字串**
</dt> <dt>

存取類型：唯讀
</dt> </dl>

字串，提供 **LastErrorCode** 中所記錄錯誤的詳細資訊，以及可採取之任何矯正措施的相關資訊。 這個屬性會繼承自 [**CIM \_ LogicalDevice**](/windows/desktop/CIMWin32Prov/cim-logicaldevice) ，但不會使用。

</dd> <dt>

**HealthState**
</dt> <dd> <dl> <dt>

資料類型： **uint16**
</dt> <dt>

存取類型：唯讀
</dt> </dl>

專案目前的健康情況。 這個屬性繼承自 [**CIM \_ ManagedSystemElement**](/windows/desktop/CIMWin32Prov/cim-managedsystemelement)，而且一律設定為 5 (確定) 。

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

整合服務安裝到虛擬機器的日期和時間。 這個屬性繼承自 [**CIM \_ ManagedSystemElement**](/windows/desktop/CIMWin32Prov/cim-managedsystemelement)。

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

邏輯裝置所報告的最後一個錯誤碼。 這個屬性繼承自 [**CIM \_ LogicalDevice**](/windows/desktop/CIMWin32Prov/cim-logicaldevice)，但不會使用它。

</dd> <dt>

**MaxQuiesceTime**
</dt> <dd> <dl> <dt>

資料類型： **uint64**
</dt> <dt>

存取類型：唯讀
</dt> </dl>

這個屬性已被取代。 這個屬性繼承自 [**CIM \_ LogicalDevice**](/windows/desktop/CIMWin32Prov/cim-logicaldevice)，但不會使用它。

</dd> <dt>

**名稱**
</dt> <dd> <dl> <dt>

資料類型： **字串**
</dt> <dt>

存取類型：唯讀
</dt> </dl>

已知物件的標籤。 這個屬性繼承自 [**CIM \_ ManagedSystemElement**](/windows/desktop/CIMWin32Prov/cim-managedsystemelement)。

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
</dt> <dt>

限定詞：覆 [**寫**](/windows/desktop/WmiSdk/standard-qualifiers) ( "OperationalStatus" ) ， [**ArrayType**](/windows/desktop/WmiSdk/standard-qualifiers) ( "Indexed" ) 
</dt> </dl>

專案的目前狀態。 這個屬性繼承自 [**CIM \_ ManagedSystemElement**](/windows/desktop/CIMWin32Prov/cim-managedsystemelement)。

以下是「 **OperationalStatus** \[ 0」屬性值的可能值 \] 。

<dt>

<span id="OK"></span><span id="ok"></span>

<span id="OK"></span><span id="ok"></span>**確定** (2) 


</dt> <dd>

服務正常運作。 **OperationalStatus** \[ 1 \] 和 **StatusDescriptions** \[ 1 \] 屬性值可能包含詳細資訊。

</dd> <dt>

<span id="Degraded"></span><span id="degraded"></span><span id="DEGRADED"></span>

<span id="Degraded"></span><span id="degraded"></span><span id="DEGRADED"></span> (3) **降級**


</dt> <dd>

服務正常運作，但來賓服務已協商相容的通訊協定版本。 **OperationalStatus** \[ 1 \] 和 **StatusDescriptions** \[ 1 \] 屬性值可能包含詳細資訊。

</dd> <dt>

<span id="Non-Recoverable_Error"></span><span id="non-recoverable_error"></span><span id="NON-RECOVERABLE_ERROR"></span>

<span id="Non-Recoverable_Error"></span><span id="non-recoverable_error"></span><span id="NON-RECOVERABLE_ERROR"></span>**無法復原的錯誤** (7) 


</dt> <dd>

來賓不支援相容的通訊協定版本。 **OperationalStatus** \[ 1 \] 和 **StatusDescriptions** \[ 1 \] 屬性值可能包含詳細資訊。

</dd> <dt>

<span id="No_Contact"></span><span id="no_contact"></span><span id="NO_CONTACT"></span>

<span id="No_Contact"></span><span id="no_contact"></span><span id="NO_CONTACT"></span>**沒有連絡人** (12) 


</dt> <dd>

尚未安裝或尚未連線到來賓服務。

</dd> <dt>

<span id="Lost_Communication"></span><span id="lost_communication"></span><span id="LOST_COMMUNICATION"></span>

<span id="Lost_Communication"></span><span id="lost_communication"></span><span id="LOST_COMMUNICATION"></span>**遺失通訊** (13) 


</dt> <dd>

來賓服務已不會再回應正常。

</dd> <dt>

<span id="Paused"></span><span id="paused"></span><span id="PAUSED"></span>

<span id="Paused"></span><span id="paused"></span><span id="PAUSED"></span>已 **暫停** (15) 


</dt> <dd>

虛擬機器已暫停。

</dd> </dl>

**OperationalStatus** \[ 1 \] 屬性值表示結合的應用程式狀態值。 這會是下列其中一個值。

> [!Note]  
> 您可以使用 [**SetApplicationState**](ivmapplicationhealthmonitor-setapplicationstate.md) 方法，在虛擬機器上設定應用程式的狀態。

 

<dt>

<span id="OK"></span><span id="ok"></span>

<span id="OK"></span><span id="ok"></span>**確定** (2) 


</dt> <dd>

在虛擬機器中執行的應用程式會正常運作。

</dd> <dt>

<span id="Protocol_Mismatch"></span><span id="protocol_mismatch"></span><span id="PROTOCOL_MISMATCH"></span>

<span id="Protocol_Mismatch"></span><span id="protocol_mismatch"></span><span id="PROTOCOL_MISMATCH"></span>**通訊協定不相符** (32775) 


</dt> <dd>

來賓和主機元件正在執行不同的通訊協定版本。

</dd> <dt>

<span id="Application_Critical_State"></span><span id="application_critical_state"></span><span id="APPLICATION_CRITICAL_STATE"></span>

<span id="Application_Critical_State"></span><span id="application_critical_state"></span><span id="APPLICATION_CRITICAL_STATE"></span>**應用程式重大狀態** (32782) 


</dt> <dd>

虛擬機器內的一或多個應用程式處於重大狀態。

</dd> <dt>

<span id="Communication_Timed_Out"></span><span id="communication_timed_out"></span><span id="COMMUNICATION_TIMED_OUT"></span>

<span id="Communication_Timed_Out"></span><span id="communication_timed_out"></span><span id="COMMUNICATION_TIMED_OUT"></span>**通訊超時** (32783) 


</dt> <dd>

等候來賓元件的回應計時。

</dd> <dt>

<span id="Communication_Failed"></span><span id="communication_failed"></span><span id="COMMUNICATION_FAILED"></span>

<span id="Communication_Failed"></span><span id="communication_failed"></span><span id="COMMUNICATION_FAILED"></span>**通訊失敗** (32784) 


</dt> <dd>

無法與來賓元件通訊。

</dd> </dl>

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

除了裝置識別碼資訊以外的任何其他資料，可用來識別邏輯裝置。 這個屬性繼承自 [**CIM \_ LogicalDevice**](/windows/desktop/CIMWin32Prov/cim-logicaldevice) ，一律設為 **Null**。

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

此裝置自上一次電源週期起開啟電源的連續小時數。 這個屬性會繼承自 [**CIM \_ LogicalDevice**](/windows/desktop/CIMWin32Prov/cim-logicaldevice) ，但不會使用。

</dd> <dt>

**PrimaryStatus**
</dt> <dd> <dl> <dt>

資料類型： **uint16**
</dt> <dt>

存取類型：唯讀
</dt> </dl>

提供高層級的狀態資訊。 這個屬性應該與 **DetailedStatus** 屬性一起使用，以提供元素和其子元件的高階和詳細健全狀況狀態資訊。 **Null** 值表示不會執行此屬性。 這個屬性繼承自 [**CIM \_ ManagedSystemElement**](/windows/desktop/CIMWin32Prov/cim-managedsystemelement)。

</dd> <dt>

**RequestedState**
</dt> <dd> <dl> <dt>

資料類型： **uint16**
</dt> <dt>

存取類型：唯讀
</dt> </dl>

上次要求或預期的專案狀態。 這個屬性繼承自 [**CIM \_ EnabledLogicalElement**](/previous-versions//cc136818(v=vs.85))，而且一律設定為 12 (不適用) 。

</dd> <dt>

**狀態**
</dt> <dd> <dl> <dt>

資料類型： **字串**
</dt> <dt>

存取類型：唯讀
</dt> </dl>

物件的目前狀態。 這個屬性會繼承自 [**CIM \_ ManagedSystemElement**](/windows/desktop/CIMWin32Prov/cim-managedsystemelement) ，但不會使用。

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

範圍系統的名稱。 這個屬性會繼承自 [**CIM \_ LogicalDevice**](/windows/desktop/CIMWin32Prov/cim-logicaldevice) ，而且是與此信號服務相關聯之 [**Msvm \_ 的同**](msvm-computersystem.md) 類型名稱。

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

指出實例正在轉換的目標狀態。 這個屬性繼承自 [**CIM \_ EnabledLogicalElement**](/previous-versions//cc136818(v=vs.85))，但不會使用它。

</dd> </dl>

## <a name="remarks"></a>備註

存取 **Msvm \_ HeartbeatComponent** 類別可能受 UAC 篩選所限制。 如需詳細資訊，請參閱 [使用者帳戶控制和 WMI](/windows/desktop/WmiSdk/user-account-control-and-wmi)。

## <a name="examples"></a>範例

下列 c # 範例會取得虛擬機器的應用程式健康情況狀態。 您可以在 [虛擬化範例 (V2) 的一般公用程式 ](common-utilities-for-the-virtualization-samples-v2.md)中找到參考的公用程式。

> [!IMPORTANT]
> 若要正確運作，必須使用系統管理員許可權來執行下列程式碼。

 


```CSharp
private UInt16 OperationalStatusOk = 2;
private UInt16 OperationalStatusApplicationCriticalState = 32782;

/// <summary>
/// Gets the applications status in the VM.
/// </summary>
/// <param name="hostMachine">The hostname of the machine on which
/// the VM is running.</param>
/// <param name="vmName">The VM name.</param>
public
void
GetAppHealthStatus(
    string hostMachine,
    string vmName
    )
{
    ManagementScope scope = new ManagementScope(
        @"\\" + hostMachine + @"\root\virtualization\v2", null);

    ManagementObject heartBeatComponent = null;

    // Get the VM object and its heart beat component.
    using (ManagementObject vm = WmiUtilities.GetVirtualMachine(vmName, scope))
    using (ManagementObjectCollection heartBeatCollection =
        vm.GetRelated("Msvm_HeartbeatComponent", "Msvm_SystemDevice",
            null, null, null, null, false, null))
    {
        foreach (ManagementObject element in heartBeatCollection)
        {
            heartBeatComponent = element;
            break;
        }
    }

    if (heartBeatComponent == null)
    {
        Console.WriteLine("The VM is not running.");
        return;
    }

    using (heartBeatComponent)
    {
        UInt16[] operationalStatus = (UInt16[])heartBeatComponent["OperationalStatus"];
        UInt16 vmStatus = operationalStatus[0];

        if (vmStatus != OperationalStatusOk)
        {
            Console.WriteLine("The VM heartbeat status is not OK");
            return;
        }

        if (operationalStatus.Length != 2)
        {
            Console.WriteLine("The required Integration Components are not running " +
                "or not installed.");
            return;
        }

        UInt16 appStatus = operationalStatus[1];
        if (appStatus == OperationalStatusOk)
        {
            Console.WriteLine("The VM applications health status: OK");
        }
        else if (appStatus == OperationalStatusApplicationCriticalState)
        {
            Console.WriteLine("The VM applications health status: Critical");
        }
        else
        {
            throw new ManagementException("Unknown application health status");
        }
    }
}
```



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

[**CIM \_ LogicalDevice**](cim-logicaldevice.md)
</dt> <dt>

[**CIM \_ LogicalDevice**](/windows/desktop/CIMWin32Prov/cim-logicaldevice)
</dt> <dt>

[**Msvm \_ HeartbeatComponent**](/previous-versions/windows/desktop/virtual/msvm-heartbeatcomponent)
</dt> </dl>

 

