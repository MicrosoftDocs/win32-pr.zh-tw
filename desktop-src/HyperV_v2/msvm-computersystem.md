---
description: 代表實體電腦系統或虛擬機器。
ms.assetid: 1db9e169-1466-4898-ab95-e9d622fe43cb
title: Msvm_ComputerSystem 類別
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Msvm_ComputerSystem
- Msvm_ComputerSystem.SetPowerState
- Msvm_ComputerSystem.InstanceID
- Msvm_ComputerSystem.Caption
- Msvm_ComputerSystem.Description
- Msvm_ComputerSystem.ElementName
- Msvm_ComputerSystem.InstallDate
- Msvm_ComputerSystem.OperationalStatus
- Msvm_ComputerSystem.StatusDescriptions
- Msvm_ComputerSystem.Status
- Msvm_ComputerSystem.HealthState
- Msvm_ComputerSystem.CommunicationStatus
- Msvm_ComputerSystem.DetailedStatus
- Msvm_ComputerSystem.OperatingStatus
- Msvm_ComputerSystem.PrimaryStatus
- Msvm_ComputerSystem.EnabledState
- Msvm_ComputerSystem.OtherEnabledState
- Msvm_ComputerSystem.RequestedState
- Msvm_ComputerSystem.EnabledDefault
- Msvm_ComputerSystem.TimeOfLastStateChange
- Msvm_ComputerSystem.AvailableRequestedStates
- Msvm_ComputerSystem.TransitioningToState
- Msvm_ComputerSystem.CreationClassName
- Msvm_ComputerSystem.Name
- Msvm_ComputerSystem.PrimaryOwnerName
- Msvm_ComputerSystem.PrimaryOwnerContact
- Msvm_ComputerSystem.Roles
- Msvm_ComputerSystem.NameFormat
- Msvm_ComputerSystem.OtherIdentifyingInfo
- Msvm_ComputerSystem.IdentifyingDescriptions
- Msvm_ComputerSystem.Dedicated
- Msvm_ComputerSystem.OtherDedicatedDescriptions
- Msvm_ComputerSystem.ResetCapability
- Msvm_ComputerSystem.PowerManagementCapabilities
- Msvm_ComputerSystem.OnTimeInMilliseconds
- Msvm_ComputerSystem.ProcessID
- Msvm_ComputerSystem.TimeOfLastConfigurationChange
- Msvm_ComputerSystem.NumberOfNumaNodes
- Msvm_ComputerSystem.ReplicationState
- Msvm_ComputerSystem.ReplicationHealth
- Msvm_ComputerSystem.ReplicationMode
- Msvm_ComputerSystem.FailedOverReplicationType
- Msvm_ComputerSystem.LastReplicationType
- Msvm_ComputerSystem.LastApplicationConsistentReplicationTime
- Msvm_ComputerSystem.LastReplicationTime
- Msvm_ComputerSystem.LastSuccessfulBackupTime
- Msvm_ComputerSystem.EnhancedSessionModeState
api_type:
- DllExport
api_location:
- vmms.exe
ms.openlocfilehash: a8a81d5e1503c868865f1f1fae7238be74f024c1bd1c992f5610ce75b5702ab6
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/11/2021
ms.locfileid: "119531780"
---
# <a name="msvm_computersystem-class"></a>Msvm 的 it \_ 類別

代表實體電腦系統或虛擬機器。

若要取得 VMMS 的資訊，請使用 [**Msvm \_ VirtualSystemManagementService**](msvm-virtualsystemmanagementservice.md) 類別。

下列語法已簡化受控物件格式 (MOF) 程式碼，並且包含所有繼承的屬性。

## <a name="syntax"></a>語法

``` syntax
[Dynamic, Provider("VmmsWmiInstanceAndMethodProvider"), AMENDMENT]
class Msvm_ComputerSystem : CIM_ComputerSystem
{
  string   InstanceID;
  string   Caption;
  string   Description;
  string   ElementName;
  datetime InstallDate;
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
  uint16   RequestedState;
  uint16   EnabledDefault = 2;
  datetime TimeOfLastStateChange;
  uint16   AvailableRequestedStates[];
  uint16   TransitioningToState;
  string   CreationClassName;
  string   Name = "GUID";
  string   PrimaryOwnerName;
  string   PrimaryOwnerContact;
  string   Roles[];
  string   NameFormat;
  string   OtherIdentifyingInfo[];
  string   IdentifyingDescriptions[];
  uint16   Dedicated[];
  string   OtherDedicatedDescriptions[];
  uint16   ResetCapability = 1;
  uint16   PowerManagementCapabilities[];
  uint64   OnTimeInMilliseconds;
  uint32   ProcessID;
  datetime TimeOfLastConfigurationChange;
  uint16   NumberOfNumaNodes;
  uint16   ReplicationState;
  uint16   ReplicationHealth;
  uint16   ReplicationMode;
  uint16   FailedOverReplicationType;
  uint16   LastReplicationType;
  DateTime LastApplicationConsistentReplicationTime;
  DateTime LastReplicationTime;
  DateTime LastSuccessfulBackupTime;
  uint16   EnhancedSessionModeState;
};
```

## <a name="members"></a>成員

**Msvm 的 \_** 非程式類別有下列類型的成員：

-   [方法](#methods)
-   [屬性](#properties)

### <a name="methods"></a>方法

**Msvm 的 \_** it 類別有這些方法。



| 方法                                                                                         | 描述                                                                                                                                                                                                                                                                                                                         |
|:-----------------------------------------------------------------------------------------------|:------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [**InjectNonMaskableInterrupt**](injectnonmaskableinterrupt-msvm-computersystem.md)           | 將非遮罩式插斷插入虛擬機器中。 只有代表虛擬機器的 Msvm 同機類別 **\_** 實例才支援這個方法。<br/> **Windows 8.1：** 在 Windows 8.1 和 Windows Server 2012 R2 之前，不支援這個方法。<br/>                                    |
| [**RequestReplicationStateChange**](msvm-computersystem-requestreplicationstatechange.md)     | 要求將虛擬機器的複寫狀態變更為指定的值。 只有代表虛擬機器的 Msvm 同機類別 **\_** 實例才支援這個方法。<br/>                                                                                                        |
| [**RequestReplicationStateChangeEx**](msvm-requestreplicationstatechangeex-computersystem.md) | 要求將虛擬機器的複寫狀態變更為指定的值。 只有代表虛擬機器的 Msvm 同機類別 **\_** 實例才支援這個方法。<br/> **Windows 8.1：** 在 Windows 8.1 和 Windows Server 2012 R2 之前，不支援這個方法。<br/> |
| [**RequestStateChange**](requeststatechange-msvm-computersystem.md)                           | 要求變更虛擬機器的狀態。 只有代表虛擬機器的 Msvm 同機類別 **\_** 實例才支援這個方法。<br/>                                                                                                                                           |
| **SetPowerState**                                                                              | 不支援這個方法。<br/>                                                                                                                                                                                                                                                                                            |



 

### <a name="properties"></a>屬性

**Msvm 的 \_** it 類別具有這些屬性。

<dl> <dt>

**AvailableRequestedStates**
</dt> <dd> <dl> <dt>

資料類型： **uint16** 陣列
</dt> <dt>

存取類型：唯讀
</dt> </dl>

指出用於起始狀態變更之 [**RequestStateChange**](/previous-versions/windows/desktop/iscsitarg/requeststatechange-cim-enabledlogicalelement)方法的 *RequestedState* 參數可能的值。 列出的值將會是與 **cim \_ EnabledLogicalElementCapabilities** 相關聯的實例之 **RequestedStatesSupported** 屬性中所含值的子集，其中選取的值是 [**cim \_ EnabledLogicalElement**](/previous-versions//cc136818(v=vs.85))物件目前狀態的函式。 如果實作為目前狀態的函式，則這個屬性可以是非 **Null** 的值。 如果實作為目前狀態的函式無法判斷可能的值集，這個屬性將會是 **Null** 。

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

物件的簡短描述。 這個屬性繼承自 [**CIM \_ ManagedElement**](/previous-versions/windows/desktop/iscsitarg/cim-managedelement) 類別，而且它將包含下列其中一個值。



| 值                                                                                                | 意義                                                  |
|------------------------------------------------------------------------------------------------------|----------------------------------------------------------|
| <dl> <dt>「虛擬機器」</dt> </dl>         | 實例代表虛擬機器。<br/>    |
| <dl> <dt>「主控電腦系統」</dt> </dl> | 實例代表主控電腦。<br/> |



 

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

建立實例時所使用之類別或子類別的名稱。 這個屬性會繼承自 [**CIM \_ 系統**](/windows/desktop/CIMWin32Prov/cim-system)，且一律設定為「Msvm 的系統組態」 \_ 。

</dd> <dt>

**專用**
</dt> <dd> <dl> <dt>

資料類型： **uint16** 陣列
</dt> <dt>

存取類型：唯讀
</dt> </dl>

指出電腦系統是否為特殊用途的系統 (專用於特定用途) ，而不是一般用途的系統。 這個屬性繼承自 [**CIM 的 \_ 程式集**](/windows/desktop/CIMWin32Prov/cim-computersystem)，且一律設定為 0 (並非專用) 。

</dd> <dt>

**說明**
</dt> <dd> <dl> <dt>

資料類型： **字串**
</dt> <dt>

存取類型：唯讀
</dt> </dl>

對物件的描述。 這個屬性是從 [**CIM \_ ManagedElement**](/previous-versions/windows/desktop/iscsitarg/cim-managedelement)繼承而來，它會包含下列其中一個值。



| 值                                                                                                          | 意義                                                  |
|----------------------------------------------------------------------------------------------------------------|----------------------------------------------------------|
| <dl> <dt>「Microsoft 虛擬電腦系統」</dt> </dl> | 實例代表虛擬機器。<br/>    |
| <dl> <dt>「Microsoft 主控電腦系統」</dt> </dl> | 實例代表主控電腦。<br/> |



 

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

物件的顯示名稱。 這個屬性繼承自 [**CIM \_ ManagedElement**](/previous-versions/windows/desktop/iscsitarg/cim-managedelement)，一律設定為虛擬機器的電腦顯示名稱或管理作業系統的 NetBIOS 名稱。

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

專案的已啟用和停用狀態。 這個屬性也可以指出這些要求狀態之間的轉換。 這個屬性繼承自 [**CIM \_ EnabledLogicalElement**](/previous-versions//cc136818(v=vs.85)) 類別，它會設定為 2 (針對實體電腦啟用) ，或針對虛擬機器使用下列其中一個值。 如需這些狀態的圖形化視圖，請參閱備註。



| 值                                                                                                                                                                                                                                                                       | 意義                                                                                                                                                                                                         |
|-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span><dl> <dt>**未知**</dt>的 <dt>0</dt> </dl>                                                 | 無法判斷元素的狀態。<br/>                                                                                                                                                    |
| <span id="Other"></span><span id="other"></span><span id="OTHER"></span><dl> <dt>**其他**</dt> <dt>1</dt> </dl>                                                         |                                                                                                                                                                                                                 |
| <span id="Enabled"></span><span id="enabled"></span><span id="ENABLED"></span><dl> <dt>**已啟用**</dt> <dt>2</dt> </dl>                                                 | 元素正在執行。<br/>                                                                                                                                                                              |
| <span id="Disabled"></span><span id="disabled"></span><span id="DISABLED"></span><dl> <dt>**停用**</dt> <dt>3</dt> </dl>                                             | 元素已關閉。<br/>                                                                                                                                                                           |
| <span id="Shutting_Down"></span><span id="shutting_down"></span><span id="SHUTTING_DOWN"></span><dl> 正在 <dt>**關閉**</dt> <dt>4</dt> </dl>                         | 專案正在進入已停用狀態的進程。<br/>                                                                                                                                          |
| <span id="Not_Applicable"></span><span id="not_applicable"></span><span id="NOT_APPLICABLE"></span><dl> <dt>**不適用**</dt> <dt>5</dt> </dl>                     | 元素不支援啟用或停用。<br/>                                                                                                                                              |
| <span id="Enabled_but_Offline"></span><span id="enabled_but_offline"></span><span id="ENABLED_BUT_OFFLINE"></span><dl> <dt>**已啟用但離線**</dt> <dt>6</dt> </dl> | 元素可能正在完成命令，而且會捨棄任何新的要求。<br/>                                                                                                                         |
| <span id="In_Test"></span><span id="in_test"></span><span id="IN_TEST"></span><dl> <dt>**在測試**</dt> <dt>7</dt>中 </dl>                                                 | 元素處於測試狀態。<br/>                                                                                                                                                                      |
| <span id="Deferred"></span><span id="deferred"></span><span id="DEFERRED"></span><dl> <dt>**延**</dt>後 <dt>8</dt> </dl>                                             | 元素可能正在完成命令，但它會將任何新的要求排在佇列中。<br/>                                                                                                                        |
| <span id="Quiesce"></span><span id="quiesce"></span><span id="QUIESCE"></span><dl> <dt>**靜止**</dt> <dt>9</dt> </dl>                                                 | 元素已啟用但處於受限模式。 專案的行為類似于啟用狀態 (2) ，但只會處理一組受限制的命令。 所有其他要求則會排入佇列。<br/> |
| <span id="Starting"></span><span id="starting"></span><span id="STARTING"></span><dl> <dt>**起始**</dt> <dt>10</dt> </dl>                                            | 元素正在進入啟用狀態 (2) 。 新的要求會排入佇列。<br/>                                                                                                             |



 

</dd> <dt>

**EnhancedSessionModeState**
</dt> <dd> <dl> <dt>

資料類型： **uint16**
</dt> <dt>

存取類型：唯讀
</dt> </dl>

指定虛擬機器上增強型會話模式的目前狀態。

Hyper-v WMI 提供者會在每次 **Msvm \_** 系統類型的 **EnhancedSessionModeState** 變更時引發 [**\_ \_ InstanceModificationEvent**](/windows/desktop/WmiSdk/--instancemodificationevent) 。 如果使用中的 vmconnection 會話收到 **\_ \_ InstanceModificationEvent**，則會在使用者啟用該設定時，嘗試切換至增強的會話模式。

**Windows 8.1：** 在 Windows 8.1 和 Windows Server 2012 R2 之前，不支援這個值。

**EnhancedSessionModeState** 可以是下列其中一個值：

<dt>

<span id="Allowed_and_available"></span><span id="allowed_and_available"></span><span id="ALLOWED_AND_AVAILABLE"></span>

<span id="Allowed_and_available"></span><span id="allowed_and_available"></span><span id="ALLOWED_AND_AVAILABLE"></span>**允許和可用** (2) 


</dt> <dd>

虛擬機器允許並提供增強模式。

</dd> <dt>

<span id="Not_allowed"></span><span id="not_allowed"></span><span id="NOT_ALLOWED"></span>

<span id="Not_allowed"></span><span id="not_allowed"></span><span id="NOT_ALLOWED"></span>**不允許** (3) 


</dt> <dd>

虛擬機器上不允許增強模式。

</dd> <dt>

<span id="Allowed_but_not_available"></span><span id="allowed_but_not_available"></span><span id="ALLOWED_BUT_NOT_AVAILABLE"></span>

<span id="Allowed_but_not_available"></span><span id="allowed_but_not_available"></span><span id="ALLOWED_BUT_NOT_AVAILABLE"></span>**允許但無法使用** (6) 


</dt> <dd>

允許使用增強模式，但目前無法在虛擬機器上使用。

</dd> </dl>

</dd> <dt>

**FailedOverReplicationType**
</dt> <dd> <dl> <dt>

資料類型： **uint16**
</dt> <dt>

存取類型：唯讀
</dt> <dt>

限定詞：已 [**淘汰**](/windows/desktop/WmiSdk/standard-wmi-qualifiers) ( "[**Msvm \_ ReplicationRelationship**](msvm-replicationrelationship.md).**FailedOverReplicationType**") 
</dt> </dl>

在容錯移轉操作期間套用的復原資料點類型。

> [!Note]  
> 從 Windows 8.1 開始，這個屬性已被取代。相反地，請在 [**Msvm \_ ReplicationRelationship**](msvm-replicationrelationship.md)類別中使用相同名稱的屬性，以取得主要或擴充關聯性的值。

 

可能的值包括：

<dt>

<span id="None"></span><span id="none"></span><span id="NONE"></span>

**無** (0) 


</dt> <dd></dd> <dt>

<span id="Regular"></span><span id="regular"></span><span id="REGULAR"></span>

**一般** (1) 


</dt> <dd></dd> <dt>

<span id="Application_consistent"></span><span id="application_consistent"></span><span id="APPLICATION_CONSISTENT"></span>

**應用程式一致** (2) 


</dt> <dd></dd> <dt>

<span id="Planned"></span><span id="planned"></span><span id="PLANNED"></span>

**規劃** 的 (3) 


</dt> <dd></dd> </dl>

</dd> <dt>

**HealthState**
</dt> <dd> <dl> <dt>

資料類型： **uint16**
</dt> <dt>

存取類型：唯讀
</dt> </dl>

指定元素目前的健康情況。 這個屬性會表示此元素的健全狀況，但不一定是它的子元件。

發生重大錯誤時，請檢查事件記錄檔以取得詳細資料。 **EnabledState** 屬性也可以包含詳細資訊。 例如，當磁碟空間不足時， **HealthState** 會設定為25、虛擬機器暫停，而 **EnabledState** 設定為 32768 (暫停) 。

這個屬性繼承自 [**CIM \_ ManagedSystemElement**](/windows/desktop/CIMWin32Prov/cim-managedsystemelement)。



| 值                                                                                                                                                                                                                                                            | 意義                                                                                                                                                                                                                                                                                                        |
|------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span id="OK"></span><span id="ok"></span><dl> <dt>**確定**</dt> <dt>5</dt> </dl>                                                                               | 虛擬機器完全正常運作，且在正常指令引數內運作，而且沒有錯誤。<br/>                                                                                                                                                                                    |
| <span id="Major_Failure"></span><span id="major_failure"></span><span id="MAJOR_FAILURE"></span><dl> <dt>**重大失敗**</dt> <dt>20</dt> </dl>             | 虛擬機器發生重大故障。 當包含虛擬機器 Vhd 的一或多個磁片的磁碟空間不足，且虛擬機器已暫停時，就會使用此值。<br/>                                                                                                   |
| <span id="Critical_failure"></span><span id="critical_failure"></span><span id="CRITICAL_FAILURE"></span><dl> <dt>**重大失敗**</dt> <dt>25</dt> </dl> | 元素沒有作用，而且可能無法復原。 這可能表示虛擬機器 (Vmwp.exe) 的工作者進程沒有回應控制或資訊要求，或是包含虛擬機器 Vhd 的一或多個磁片磁碟空間不足。<br/> |



 

</dd> <dt>

**IdentifyingDescriptions**
</dt> <dd> <dl> <dt>

資料類型： **字串** 陣列
</dt> <dt>

存取類型：唯讀
</dt> </dl>

這個屬性繼承自 [**CIM 的 \_ 程式集**](/windows/desktop/CIMWin32Prov/cim-computersystem)，且一律設定為 **Null**。

</dd> <dt>

**InstallDate**
</dt> <dd> <dl> <dt>

資料類型： **datetime**
</dt> <dt>

存取類型：唯讀
</dt> </dl>

虛擬機器設定為虛擬機器建立的日期和時間，或針對管理作業系統的 **Null**。 這個屬性繼承自 [**CIM \_ ManagedSystemElement**](/windows/desktop/CIMWin32Prov/cim-managedsystemelement)。

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

在 Windows 8 中，每個電腦系統或虛擬機器都有單一的 [**ReplicationSettingData**](msvm-replicationsettingdata.md)實例。 針對 Windows 8.1，復原虛擬機器有兩個 **ReplicationSettingData** 實例。 這種變更會區分設定資料與複寫關聯性。



| 屬性名稱  | Windows 8 值               | Windows 8.1 值                          |
|----------------|-------------------------------|--------------------------------------------|
| **InstanceID** | Microsoft： <vmguid> \\ HVR | Microsoft： <vmguid> \\ HVR \\<0/1> |



 

在 Windows 8.1 值中，0表示 primary，1表示擴充複寫。 如需擴充複寫的詳細資訊，請參閱 [**Msvm \_ ReplicationRelationship**](msvm-replicationrelationship.md)。

</dd> <dt>

**LastApplicationConsistentReplicationTime**
</dt> <dd> <dl> <dt>

資料類型： **DateTime**
</dt> <dt>

存取類型：唯讀
</dt> <dt>

限定詞：已 [**淘汰**](/windows/desktop/WmiSdk/standard-wmi-qualifiers) ( "[**Msvm \_ ReplicationRelationship**](msvm-replicationrelationship.md).**LastApplicationConsistentReplicationTime**") 
</dt> </dl>

為虛擬機器收到最後一個應用程式一致複寫的時間。

> [!Note]  
> 從 Windows 8.1 開始，這個屬性已被取代。相反地，請在 [**Msvm \_ ReplicationRelationship**](msvm-replicationrelationship.md)類別中使用相同名稱的屬性，以取得主要或擴充關聯性的值。

 

</dd> <dt>

**LastReplicationTime**
</dt> <dd> <dl> <dt>

資料類型： **DateTime**
</dt> <dt>

存取類型：唯讀
</dt> <dt>

限定詞：已 [**淘汰**](/windows/desktop/WmiSdk/standard-wmi-qualifiers) ( "[**Msvm \_ ReplicationRelationship**](msvm-replicationrelationship.md).**LastReplicationTime**") 
</dt> </dl>

復原虛擬機器時，收到最後一次複寫的時間。

> [!Note]  
> 從 Windows 8.1 開始，這個屬性已被取代。相反地，請在 [**Msvm \_ ReplicationRelationship**](msvm-replicationrelationship.md)類別中使用相同名稱的屬性，以取得主要或擴充關聯性的值。

 

</dd> <dt>

**LastReplicationType**
</dt> <dd> <dl> <dt>

資料類型： **uint16**
</dt> <dt>

存取類型：唯讀
</dt> <dt>

限定詞：已 [**淘汰**](/windows/desktop/WmiSdk/standard-wmi-qualifiers) ( "[**Msvm \_ ReplicationRelationship**](msvm-replicationrelationship.md).**LastReplicationType**") 
</dt> </dl>

針對虛擬機器所收到的最後一個複寫類型。

> [!Note]  
> 從 Windows 8.1 開始，這個屬性已被取代。相反地，請在 [**Msvm \_ ReplicationRelationship**](msvm-replicationrelationship.md)類別中使用相同名稱的屬性，以取得主要或擴充關聯性的值。

 

可能的值包括：

<dt>

<span id="None"></span><span id="none"></span><span id="NONE"></span>

**無** (0) 


</dt> <dd></dd> <dt>

<span id="Regular"></span><span id="regular"></span><span id="REGULAR"></span>

**一般** (1) 


</dt> <dd></dd> <dt>

<span id="Application_consistent"></span><span id="application_consistent"></span><span id="APPLICATION_CONSISTENT"></span>

**應用程式一致** (2) 


</dt> <dd></dd> <dt>

<span id="Planned"></span><span id="planned"></span><span id="PLANNED"></span>

**規劃** 的 (3) 


</dt> <dd></dd> </dl>

</dd> <dt>

**LastSuccessfulBackupTime**
</dt> <dd> <dl> <dt>

資料類型： **DateTime**
</dt> <dt>

存取類型：唯讀
</dt> </dl>

虛擬機器上一次成功備份的完成時間。

</dd> <dt>

**名稱**
</dt> <dd> <dl> <dt>

資料類型： **字串**
</dt> <dt>

存取類型：唯讀
</dt> </dl>

已知物件的標籤。 這個屬性繼承自 [**CIM \_ 系統**](/windows/desktop/CIMWin32Prov/cim-system)，且一律設定為 "*GUID*"。

</dd> <dt>

**NameFormat**
</dt> <dd> <dl> <dt>

資料類型： **字串**
</dt> <dt>

存取類型：唯讀
</dt> </dl>

識別如何產生系統名稱的字串，使用子類別的啟發式法。 這個屬性繼承自 [**CIM 的 \_ 程式集**](/windows/desktop/CIMWin32Prov/cim-computersystem)，且一律設定為 **Null**。

</dd> <dt>

**NumberOfNumaNodes**
</dt> <dd> <dl> <dt>

資料類型： **uint16**
</dt> <dt>

存取類型：唯讀
</dt> </dl>

電腦系統 (NUMA) 節點的非統一記憶體存取數量。 當 **Msvm \_** 的電腦代表主控電腦系統時，此屬性會包含實體 NUMA 節點的計數。 當 **Msvm \_** 的電腦代表虛擬機器時，此屬性包含虛擬 NUMA 節點的數目，這些節點會透過 ACPI 系統資源親和性表格 (SRAT) 呈現給客體作業系統。

</dd> <dt>

**OnTimeInMilliseconds**
</dt> <dd> <dl> <dt>

資料類型： **uint64**
</dt> <dt>

存取類型：唯讀
</dt> <dt>

限定詞： [**單位**](/windows/desktop/WmiSdk/standard-qualifiers) ( "毫秒" ) 
</dt> </dl>

若為虛擬機器，此屬性會指出電腦上次開啟、重設或還原後的時間（以毫秒為單位）。 這次會排除虛擬機器處於暫停狀態的時間。 若為管理作業系統，這個屬性會設定為 **Null**。

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

陣列，其中包含物件的目前狀態。 這個屬性繼承自 [**CIM \_ ManagedSystemElement**](/windows/desktop/CIMWin32Prov/cim-managedsystemelement)。 位於索引零 (0) 的值是下列其中一個值。



| 值                                                                                                                                                                                                                                                                   | 意義                                                                                                                                                                                                                                                           |
|-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span id="OK"></span><span id="ok"></span><dl> <dt>**確定**</dt> <dt>2</dt> </dl>                                                                                      | 虛擬機器正常運作，且正常運作。<br/>                                                                                                                                                                                              |
| <span id="Degraded"></span><span id="degraded"></span><span id="DEGRADED"></span><dl> <dt>**降級**</dt> <dt>3</dt> </dl>                                         | 虛擬機器只能部分運作。 這表示無法存取包含設定的儲存體。 處於此狀態的虛擬機器只能關閉或刪除。 <br/>                                               |
| <span id="Predictive_Failure"></span><span id="predictive_failure"></span><span id="PREDICTIVE_FAILURE"></span><dl> <dt>**預測性失敗**</dt> <dt>5</dt> </dl> | 虛擬機器可正常運作，但未來可能會失敗。 這表示包含虛擬機器虛擬硬碟的存放裝置可用空間不足。 如果沒有可用的磁碟空間，將會暫停虛擬機器。<br/> |
| <span id="Stopped"></span><span id="stopped"></span><span id="STOPPED"></span><dl> <dt>**已停止**</dt> <dt>10</dt> </dl>                                            | 不支援這個值。 如果虛擬機器已停止，則 [ **EnabledState** ] 屬性的值會是3， ([已停用]) 。<br/>                                                                                                                       |
| <span id="In_Service"></span><span id="in_service"></span><span id="IN_SERVICE"></span><dl> <dt>**在服務**</dt> <dt>11</dt>中 </dl>                                | 虛擬機器正在處理要求。<br/>                                                                                                                                                                                                           |
| <span id="Dormant"></span><span id="dormant"></span><span id="DORMANT"></span><dl> <dt>**休眠**</dt> <dt>15</dt> </dl>                                            | 不支援這個值。 如果虛擬機器已暫停或暫停，則 [ **EnabledState** ] 屬性的值會是 32769 ([已暫停]) 或 32768 (暫停) 。<br/>                                                                                    |



 

位於索引 1 (1) 的值是選擇性的，並包含次要狀態資訊。 用戶端應該使用索引零 (0) 的主要狀態，以判斷是否可以將新的要求發行至虛擬機器。 如果 **operationalstatus** \[ 0 \] 是 2 (確定) ，則由 **OperationalStatus** 1 指出的作業 \[ \] 可能會中斷。

在 **OperationalStatus** \[ 1 的值 \] 是下列其中一個值。



| 值                                                                                                                                                                                                                                                                                                   | 意義                                                                                       |
|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|-----------------------------------------------------------------------------------------------|
| <span id="Creating_Snapshot"></span><span id="creating_snapshot"></span><span id="CREATING_SNAPSHOT"></span><dl> <dt>**正在建立快照**</dt>集 <dt>32768</dt> </dl>                                 | 正在為虛擬機器建立快照集。<br/>             |
| <span id="Applying_Snapshot"></span><span id="applying_snapshot"></span><span id="APPLYING_SNAPSHOT"></span><dl> 正在套用 <dt>**快照**</dt>集 <dt>32769</dt> </dl>                                 | 正在將快照集套用到虛擬機器。<br/>              |
| <span id="Deleting_Snapshot"></span><span id="deleting_snapshot"></span><span id="DELETING_SNAPSHOT"></span><dl> <dt>**正在刪除快照**</dt>集 <dt>32770</dt> </dl>                                 | 正在從虛擬機器刪除快照集。<br/>            |
| <span id="Waiting_to_Start"></span><span id="waiting_to_start"></span><span id="WAITING_TO_START"></span><dl> <dt>**正在等候開始**</dt> <dt>32771</dt> </dl>                                     | 虛擬機器將會在自動啟動延遲經過之後啟動。<br/> |
| <span id="Merging_Disks"></span><span id="merging_disks"></span><span id="MERGING_DISKS"></span><dl> <dt>**合併磁片**</dt> <dt>32772</dt> </dl>                                                 | 先前已刪除之快照集的虛擬硬碟正在合併。<br/>             |
| <span id="Exporting_Virtual_Machine"></span><span id="exporting_virtual_machine"></span><span id="EXPORTING_VIRTUAL_MACHINE"></span><dl> <dt>**正在匯出虛擬機器**</dt> <dt>32773</dt> </dl> | 正在匯出虛擬機器。<br/>                                             |
| <span id="Migrating_Virtual_Machine"></span><span id="migrating_virtual_machine"></span><span id="MIGRATING_VIRTUAL_MACHINE"></span><dl> 正在 <dt>**遷移虛擬機器**</dt> <dt>32774</dt> </dl> | 虛擬機器正在從一部實體電腦即時移轉至另一部電腦。<br/>  |



 

</dd> <dt>

**OtherDedicatedDescriptions**
</dt> <dd> <dl> <dt>

資料類型： **字串** 陣列
</dt> <dt>

存取類型：唯讀
</dt> </dl>

描述當 **專用** 陣列包含值 2 (其他) 時，如何或為何專用系統的字串。 這個屬性繼承自 [**CIM 的 \_ 程式集**](/windows/desktop/CIMWin32Prov/cim-computersystem)，且一律設定為 **Null**。

</dd> <dt>

**OtherEnabledState**
</dt> <dd> <dl> <dt>

資料類型： **字串**
</dt> <dt>

存取類型：唯讀
</dt> </dl>

當 **EnabledState** 屬性設定為 1 (其他) 時，已啟用或停用虛擬機器的狀態。 當 **EnabledState** 是1以外的任何值時，這個屬性必須設定為 **Null** 。 這個屬性繼承自 [**CIM \_ EnabledLogicalElement**](/previous-versions//cc136818(v=vs.85))，而且一律設定為 **Null**。

</dd> <dt>

**OtherIdentifyingInfo**
</dt> <dd> <dl> <dt>

資料類型： **字串** 陣列
</dt> <dt>

存取類型：唯讀
</dt> </dl>

這個屬性繼承自 [**CIM 的 \_ 程式集**](/windows/desktop/CIMWin32Prov/cim-computersystem)，且一律設定為 **Null**。

</dd> <dt>

**PowerManagementCapabilities**
</dt> <dd> <dl> <dt>

資料類型： **uint16** 陣列
</dt> <dt>

存取類型：唯讀
</dt> </dl>

這個屬性繼承自 [**CIM 的 \_ 程式**](/windows/desktop/CIMWin32Prov/cim-computersystem)，但不會使用它。

</dd> <dt>

**PrimaryOwnerContact**
</dt> <dd> <dl> <dt>

資料類型： **字串**
</dt> <dt>

存取類型：唯讀
</dt> </dl>

指出如何達到主要系統擁有者 (的字串，例如電話號碼或電子郵件地址) 。 這個屬性繼承自 [**CIM \_ 系統**](/windows/desktop/CIMWin32Prov/cim-system)，且一律設定為 **Null**。

</dd> <dt>

**PrimaryOwnerName**
</dt> <dd> <dl> <dt>

資料類型： **字串**
</dt> <dt>

存取類型：唯讀
</dt> </dl>

主要系統擁有者的名稱。 這個屬性繼承自 [**CIM \_ 系統**](/windows/desktop/CIMWin32Prov/cim-system)，且一律設定為 **Null**。

</dd> <dt>

**PrimaryStatus**
</dt> <dd> <dl> <dt>

資料類型： **uint16**
</dt> <dt>

存取類型：唯讀
</dt> </dl>

提供高層級的狀態資訊。 這個屬性應該與 **DetailedStatus** 屬性一起使用，以提供元素和其子元件的高階和詳細健全狀況狀態資訊。 **Null** 值表示不會執行此屬性。 這個屬性繼承自 [**CIM \_ ManagedSystemElement**](/windows/desktop/CIMWin32Prov/cim-managedsystemelement)。

</dd> <dt>

**ProcessID**
</dt> <dd> <dl> <dt>

資料類型： **uint32**
</dt> <dt>

存取類型：唯讀
</dt> </dl>

執行此虛擬機器的進程識別碼。 此值可用來唯一識別正在執行虛擬機器之系統上的 Vmwp.exe 實例。

</dd> <dt>

**ReplicationHealth**
</dt> <dd> <dl> <dt>

資料類型： **uint16**
</dt> <dt>

存取類型：唯讀
</dt> <dt>

限定詞：已 [**淘汰**](/windows/desktop/WmiSdk/standard-wmi-qualifiers) ( "[**Msvm \_ ReplicationRelationship**](msvm-replicationrelationship.md).**ReplicationHealth**") 
</dt> </dl>

虛擬機器的複寫健全狀況。

> [!Note]  
> 從 Windows 8.1 開始，這個屬性已被取代。相反地，請在 [**Msvm \_ ReplicationRelationship**](msvm-replicationrelationship.md)類別中使用相同名稱的屬性，以取得主要或擴充關聯性的值。

 

可能的值包括：

<dt>

<span id="Not_applicable"></span><span id="not_applicable"></span><span id="NOT_APPLICABLE"></span>

**不適用** (0) 


</dt> <dd></dd> <dt>

<span id="Ok"></span><span id="ok"></span><span id="OK"></span>

**確定** (1) 


</dt> <dd></dd> <dt>

<span id="Warning"></span><span id="warning"></span><span id="WARNING"></span>

**警告** (2) 


</dt> <dd></dd> <dt>

<span id="Critical"></span><span id="critical"></span><span id="CRITICAL"></span>

**重大** (3) 


</dt> <dd></dd> </dl>

</dd> <dt>

**ReplicationMode**
</dt> <dd> <dl> <dt>

資料類型： **uint16**
</dt> <dt>

存取類型：唯讀
</dt> </dl>

指定虛擬機器的複寫模式。 這會是下列其中一個值。

<dt>

<span id="None"></span><span id="none"></span><span id="NONE"></span>

<span id="None"></span><span id="none"></span><span id="NONE"></span>**無** (0) 


</dt> <dd></dd> <dt>

<span id="Primary"></span><span id="primary"></span><span id="PRIMARY"></span>

<span id="Primary"></span><span id="primary"></span><span id="PRIMARY"></span>**主要** (1) 


</dt> <dd></dd> <dt>

<span id="Replica"></span><span id="replica"></span><span id="REPLICA"></span>

<span id="Replica"></span><span id="replica"></span><span id="REPLICA"></span>**複本** (2) 


</dt> <dd>

復原

</dd> <dt>

<span id="Test_Replica"></span><span id="test_replica"></span><span id="TEST_REPLICA"></span>

<span id="Test_Replica"></span><span id="test_replica"></span><span id="TEST_REPLICA"></span>**測試複本** (3) 


</dt> <dd>

複本

</dd> <dt>

<span id="Extended_Replica"></span><span id="extended_replica"></span><span id="EXTENDED_REPLICA"></span>

<span id="Extended_Replica"></span><span id="extended_replica"></span><span id="EXTENDED_REPLICA"></span>**擴充複本** (4) 


</dt> <dd></dd> </dl>

</dd> <dt>

**ReplicationState**
</dt> <dd> <dl> <dt>

資料類型： **uint16**
</dt> <dt>

存取類型：唯讀
</dt> <dt>

限定詞：已 [**淘汰**](/windows/desktop/WmiSdk/standard-wmi-qualifiers) ( "[**Msvm \_ ReplicationRelationship**](msvm-replicationrelationship.md).**ReplicationState**") 
</dt> </dl>

虛擬機器的複寫狀態。

> [!Note]  
> 從 Windows 8.1 開始，這個屬性已被取代。相反地，請在 [**Msvm \_ ReplicationRelationship**](msvm-replicationrelationship.md)類別中使用相同名稱的屬性，以取得主要或擴充關聯性的值。

 

可能的值包括：

<dt>

<span id="Disabled"></span><span id="disabled"></span><span id="DISABLED"></span>

**停用** (0) 


</dt> <dd></dd> <dt>

<span id="Ready_for_replication"></span><span id="ready_for_replication"></span><span id="READY_FOR_REPLICATION"></span>

**準備好** 複寫 (1) 


</dt> <dd></dd> <dt>

<span id="Waiting_to_complete_initial_replication"></span><span id="waiting_to_complete_initial_replication"></span><span id="WAITING_TO_COMPLETE_INITIAL_REPLICATION"></span>

**等候完成初始** 複寫 (2) 


</dt> <dd></dd> <dt>

<span id="Replicating"></span><span id="replicating"></span><span id="REPLICATING"></span>

複寫 **(3**) 


</dt> <dd></dd> <dt>

<span id="Synced_replication_complete"></span><span id="synced_replication_complete"></span><span id="SYNCED_REPLICATION_COMPLETE"></span>

**同步複寫完成** (4) 


</dt> <dd></dd> <dt>

<span id="Recovered"></span><span id="recovered"></span><span id="RECOVERED"></span>

已 **復原** (5) 


</dt> <dd></dd> <dt>

<span id="Committed"></span><span id="committed"></span><span id="COMMITTED"></span>

**認可** (6) 


</dt> <dd></dd> <dt>

<span id="Suspended"></span><span id="suspended"></span><span id="SUSPENDED"></span>

已 **暫** 止 (7) 


</dt> <dd></dd> <dt>

<span id="Critical"></span><span id="critical"></span><span id="CRITICAL"></span>

**重大** (8) 


</dt> <dd></dd> <dt>

<span id="Waiting_to_start_resynchronization"></span><span id="waiting_to_start_resynchronization"></span><span id="WAITING_TO_START_RESYNCHRONIZATION"></span>

**等候啟動重新同步** (9) 


</dt> <dd></dd> <dt>

<span id="Resynchronizing"></span><span id="resynchronizing"></span><span id="RESYNCHRONIZING"></span>

重新 **同步** 處理 (10) 


</dt> <dd></dd> <dt>

<span id="Resynchronization_suspended"></span><span id="resynchronization_suspended"></span><span id="RESYNCHRONIZATION_SUSPENDED"></span>

**重新同步** 處理已暫停 (11) 


</dt> <dd></dd> <dt>

<span id="Failover_in_progress"></span><span id="failover_in_progress"></span><span id="FAILOVER_IN_PROGRESS"></span>

**正在進行容錯移轉** (12) 


</dt> <dd></dd> <dt>

<span id="Failback_in_progress"></span><span id="failback_in_progress"></span><span id="FAILBACK_IN_PROGRESS"></span>

**正在進行容錯回復** (13) 


</dt> <dd></dd> <dt>

<span id="Failback_complete"></span><span id="failback_complete"></span><span id="FAILBACK_COMPLETE"></span>

容錯 **回復完成** (14) 


</dt> <dd></dd> </dl>

</dd> <dt>

**RequestedState**
</dt> <dd> <dl> <dt>

資料類型： **uint16**
</dt> <dt>

存取類型：唯讀
</dt> </dl>

傳遞給 [**RequestStateChange**](requeststatechange-msvm-computersystem.md) 方法的虛擬機器最後要求或預期狀態，或 12 (不適用) 如果沒有狀態變更正在進行中。 元素的實際狀態是由 **EnabledState** 表示。 這個屬性是用來比較最後一個要求和目前啟用或停用的狀態。 這個屬性繼承自 [**CIM \_ EnabledLogicalElement**](/previous-versions//cc136818(v=vs.85))。

</dd> <dt>

**ResetCapability**
</dt> <dd> <dl> <dt>

資料類型： **uint16**
</dt> <dt>

存取類型：唯讀
</dt> </dl>

這個屬性繼承自 [**CIM 的 \_ 程式集**](/windows/desktop/CIMWin32Prov/cim-computersystem)，且一律設定為 1 (其他) 。

</dd> <dt>

**角色**
</dt> <dd> <dl> <dt>

資料類型： **字串** 陣列
</dt> <dt>

存取類型：唯讀
</dt> </dl>

字串陣列，描述系統在資訊技術環境中扮演的角色。 這個屬性繼承自 [**CIM \_ 系統**](/windows/desktop/CIMWin32Prov/cim-system)，且一律設定為 **Null**。

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
</dt> <dt>

限定詞： **ArrayType** ( 「已編制索引」 ) 
</dt> </dl>

陣列，其中包含描述對應之 **OperationalStatus** 陣列值的字串。 例如，如果服務) 中的 11 (是指派給 **OperationalStatus** \[ 0 的值 \] ，則 **StatusDescriptions** \[ 0 \] 可能會包含虛擬機器處理要求的原因說明。 這個屬性繼承自 [**CIM \_ ManagedSystemElement**](/windows/desktop/CIMWin32Prov/cim-managedsystemelement)。

</dd> <dt>

**TimeOfLastConfigurationChange**
</dt> <dd> <dl> <dt>

資料類型： **datetime**
</dt> <dt>

存取類型：唯讀
</dt> </dl>

上次修改虛擬機器組態檔的日期和時間。 設定檔會在特定虛擬機器操作期間進行修改，以及新增、修改或移除任何虛擬機器或裝置設定時。

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

指出實例正在轉換的目標狀態。 這個屬性繼承自 [**CIM \_ EnabledLogicalElement**](/previous-versions//cc136818(v=vs.85))，但不會使用它。

</dd> </dl>

## <a name="remarks"></a>備註

下圖顯示 **EnabledState** 值。

![適用于 windows server 2008 r2 之 enabledstate 值的狀態圖表](images/msvm-computersystem-enabledstate-win2008r2.png)

當 Msvm 的系統類型 **\_** 屬性變更時，WMI 提供者會指出描述變更的 [**\_ \_ InstanceModificationEvent**](/windows/desktop/WmiSdk/--instancemodificationevent)事件。 先前的狀態是包含在 **PreviousInstance** 屬性中，而新的狀態則包含在 **TargetInstance** 屬性中。 這個事件是非同步;處理 **\_ \_ InstanceModificationEvent** 事件時， **TargetInstance** 屬性可能不會反映目前的狀態。

UAC 篩選可能會限制對 Msvm 的 [未使用] 類別的存取。 **\_** 如需詳細資訊，請參閱 [使用者帳戶控制和 WMI](/windows/desktop/WmiSdk/user-account-control-and-wmi)。

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

[**CIM \_ 未進行**](cim-computersystem.md)
</dt> <dt>

[**\_\_InstanceModificationEvent**](/windows/desktop/WmiSdk/--instancemodificationevent)
</dt> <dt>

[**CIM \_ 未進行**](/windows/desktop/CIMWin32Prov/cim-computersystem)
</dt> <dt>

[**Msvm) 的， \_ (V1**](/previous-versions/windows/desktop/virtual/msvm-computersystem)
</dt> <dt>

[虛擬系統類別](virtual-system-classes.md)
</dt> </dl>

 

