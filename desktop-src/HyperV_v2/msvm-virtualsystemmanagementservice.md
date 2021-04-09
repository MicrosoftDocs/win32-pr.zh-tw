---
description: 代表存在於單一主機系統上的虛擬化服務。
ms.assetid: 7f4bd9e0-b034-4882-ad01-f7df740939ae
title: Msvm_VirtualSystemManagementService 類別
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Msvm_VirtualSystemManagementService
- Msvm_VirtualSystemManagementService.InstanceID
- Msvm_VirtualSystemManagementService.Caption
- Msvm_VirtualSystemManagementService.Description
- Msvm_VirtualSystemManagementService.ElementName
- Msvm_VirtualSystemManagementService.InstallDate
- Msvm_VirtualSystemManagementService.Name
- Msvm_VirtualSystemManagementService.OperationalStatus
- Msvm_VirtualSystemManagementService.StatusDescriptions
- Msvm_VirtualSystemManagementService.Status
- Msvm_VirtualSystemManagementService.HealthState
- Msvm_VirtualSystemManagementService.CommunicationStatus
- Msvm_VirtualSystemManagementService.DetailedStatus
- Msvm_VirtualSystemManagementService.OperatingStatus
- Msvm_VirtualSystemManagementService.PrimaryStatus
- Msvm_VirtualSystemManagementService.EnabledState
- Msvm_VirtualSystemManagementService.OtherEnabledState
- Msvm_VirtualSystemManagementService.RequestedState
- Msvm_VirtualSystemManagementService.EnabledDefault
- Msvm_VirtualSystemManagementService.TimeOfLastStateChange
- Msvm_VirtualSystemManagementService.AvailableRequestedStates
- Msvm_VirtualSystemManagementService.TransitioningToState
- Msvm_VirtualSystemManagementService.SystemCreationClassName
- Msvm_VirtualSystemManagementService.SystemName
- Msvm_VirtualSystemManagementService.CreationClassName
- Msvm_VirtualSystemManagementService.PrimaryOwnerName
- Msvm_VirtualSystemManagementService.PrimaryOwnerContact
- Msvm_VirtualSystemManagementService.StartMode
- Msvm_VirtualSystemManagementService.Started
api_type:
- DllExport
api_location:
- vmms.exe
ms.openlocfilehash: 7ee79b9690f1eacdf7dc57a2ebfc2133091a1d55
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/07/2021
ms.locfileid: "103689763"
---
# <a name="msvm_virtualsystemmanagementservice-class"></a>Msvm \_ VirtualSystemManagementService 類別

代表存在於單一主機系統上的虛擬化服務。 **Msvm \_VirtualSystemManagementService** 可用來控制虛擬機器的定義、修改和刪除。 它也有方法可在虛擬機器上執行作業，例如複製、快照，以及匯入或匯出虛擬機器。 若要取得每個虛擬機器資訊，請使用 [**Msvm \_**](msvm-computersystem.md)。

下列語法已簡化受控物件格式 (MOF) 程式碼，並且包含所有繼承的屬性。

## <a name="syntax"></a>語法

``` syntax
[Dynamic, Provider("VmmsWmiInstanceAndMethodProvider"), AMENDMENT]
class Msvm_VirtualSystemManagementService : CIM_VirtualSystemManagementService
{
  string   InstanceID;
  string   Caption = "Virtual System Management Service";
  string   Description = "Service for creating, manipulating, and managing virtual machines";
  string   ElementName = "Hyper-V Virtual System Management Service";
  datetime InstallDate;
  string   Name = "vmms";
  uint16   OperationalStatus[] = { 2 };
  string   StatusDescriptions[] = { "The service is running normally" };
  string   Status;
  uint16   HealthState = 5;
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
  string   SystemCreationClassName = "Msvm_ComputerSystem";
  string   SystemName;
  string   CreationClassName = "Msvm_VirtualSystemManagementService";
  string   PrimaryOwnerName;
  string   PrimaryOwnerContact;
  string   StartMode;
  boolean  Started = True;
};
```

## <a name="members"></a>成員

**Msvm \_ VirtualSystemManagementService** 類別具有下列類型的成員：

-   [方法](#methods)
-   [屬性](#properties)

### <a name="methods"></a>方法

**Msvm \_ VirtualSystemManagementService** 類別具有這些方法。



| 方法                                                                                                                 | 描述                                                                                                                                                                                                                                        |
|:-----------------------------------------------------------------------------------------------------------------------|:---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [**AddBootSourceSettings**](msvm-virtualsystemmanagementservice-addbootsourcesettings.md)                             | 在套用至「狀態」虛擬系統設定時，將開機來源新增至虛擬系統設定。<br/>                                                                                                                             |
| [**AddFeatureSettings**](addfeaturesettings-msvm-virtualsystemmanagementservice.md)                                   | 將乙太網路功能設定新增至虛擬機器 Ethernet 連接的設定。<br/>                                                                                                                                           |
| [**AddFibreChannelChap**](addfibrechannelchap-msvm-virtualsystemmanagementservice.md)                                 | 將 DH-CHAP 參數新增到虛擬機器中的綜合光纖通道埠。<br/>                                                                                                                                                         |
| [**AddGuestServiceSettings**](msvm-virtualsystemmanagementservice-addguestservicesettings.md)                         | 將來賓服務設定新增至虛擬系統設定。<br/> 套用至「目前」虛擬系統設定的元件時，可能會修改作用中虛擬系統的副作用來賓服務。<br/>              |
| [**AddKvpItems**](addkvpitems-msvm-virtualsystemmanagementservice.md)                                                 | 將機碼/值組加入至虛擬機器。<br/>                                                                                                                                                                                              |
| [**AddResourceSettings**](addresourcesettings-msvm-virtualsystemmanagementservice.md)                                 | 將資源新增至虛擬機器設定。<br/>                                                                                                                                                                                      |
| [**AddSystemComponentSettings**](msvm-virtualsystemmanagementservice-addsystemcomponentsettings.md)                   | 將一般設定新增至虛擬系統設定。<br/>                                                                                                                                                                                |
| [**DefinePlannedSystem**](msvm-virtualsystemmanagementservice-defineplannedsystem.md)                                 | 定義已規劃的虛擬系統。<br/> 未完全指定的輸入可能會以預設值填入。<br/>                                                                                                              |
| [**DefineSystem**](definesystem-msvm-virtualsystemmanagementservice.md)                                               | 建立新的虛擬機器定義。<br/>                                                                                                                                                                                               |
| [**DestroySystem**](destroysystem-msvm-virtualsystemmanagementservice.md)                                             | 刪除現有的虛擬機器定義。<br/>                                                                                                                                                                                         |
| [**DiagnoseNetworkConnection**](msvm-virtualsystemmanagementservice-diagnosenetworkconnection.md)                     | 在 Windows 網路虛擬化環境中診斷 VM 的網路連線能力。<br/>                                                                                                                                             |
| [**ExportSystemDefinition**](exportsystemdefinition-msvm-virtualsystemmanagementservice.md)                           | 將虛擬機器或虛擬機器的快照集匯出到檔案。<br/>                                                                                                                                                               |
| [**FormatError**](formaterror-msvm-virtualsystemmanagementservice.md)                                                 | 針對指定的內嵌 [**Msvm \_ 錯誤**](msvm-error.md) 實例陣列，傳回格式化的錯誤訊息字串。<br/>                                                                                                               |
| [**GenerateWwpn**](generatewwpn-msvm-virtualsystemmanagementservice.md)                                               | 產生一組全球通訊埠名稱 (WWPNs) 。<br/>                                                                                                                                                                                       |
| [**GetCurrentWwpnFromGenerator**](getcurrentwwpnfromgenerator-msvm-virtualsystemmanagementservice.md)                 | 提供在不保留 WWPN 的情況下，預覽目前全球埠名稱 (WWPN) 的功能。<br/>                                                                                                                                |
| [**GetDefinitionFileSummaryInformation**](getdefinitionfilesummaryinformation-msvm-virtualsystemmanagementservice.md) | 傳回指定之虛擬機器定義檔的虛擬機器摘要資訊。<br/>                                                                                                                                         |
| [**GetSizeOfSystemFiles**](getsizeofsystemfiles-msvm-virtualsystemmanagementservice.md)                               | 抓取虛擬機器的系統檔案大小總計。<br/>                                                                                                                                                                        |
| [**GetSummaryInformation**](getsummaryinformation-msvm-virtualsystemmanagementservice.md)                             | 傳回虛擬機器摘要資訊。<br/>                                                                                                                                                                                            |
| [**GetVirtualSystemThumbnailImage**](getvirtualsystemthumbnailimage-msvm-virtualsystemmanagementservice.md)           | 抓取現有虛擬機器的縮圖影像。<br/>                                                                                                                                                                             |
| [**ImportSnapshotDefinitions**](importsnapshotdefinitions-msvm-virtualsystemmanagementservice.md)                     | 搜尋指定的資料夾中是否有任何與指定之規劃的電腦系統相關聯的快照集定義檔案，並針對此位置中的每個關聯定義檔，在規劃的電腦系統上建立新的快照集。<br/> |
| [**ImportSystemDefinition**](importsystemdefinition-msvm-virtualsystemmanagementservice.md)                           | 根據指定的虛擬機器定義，建立新的規劃的電腦系統。<br/>                                                                                                                                                |
| [**ModifyDiskMergeSettings**](modifydiskmergesettings-msvm-virtualsystemmanagementservice.md)                         | 修改磁片合併設定資料。<br/>                                                                                                                                                                                                   |
| [**ModifyFeatureSettings**](modifyfeaturesettings-msvm-virtualsystemmanagementservice.md)                             | 修改虛擬機器乙太網路連接的目前功能設定。<br/>                                                                                                                                                         |
| [**ModifyGuestServiceSettings**](msvm-virtualsystemmanagementservice-modifyguestservicesettings.md)                   | 修改來賓服務設定。<br/> 套用至「目前」虛擬系統設定的元件時，可能會修改作用中虛擬系統的副作用來賓服務。<br/>                                            |
| [**ModifyKvpItems**](modifykvpitems-msvm-virtualsystemmanagementservice.md)                                           | 修改虛擬機器上現有的機碼值組。<br/>                                                                                                                                                                                 |
| [**ModifyResourceSettings**](modifyresourcesettings-msvm-virtualsystemmanagementservice.md)                           | 修改虛擬資源設定。<br/>                                                                                                                                                                                                     |
| [**ModifyServiceSettings**](modifyservicesettings-msvm-virtualsystemmanagementservice.md)                             | 修改服務的設定資料。<br/>                                                                                                                                                                                                    |
| [**ModifySystemComponentSettings**](msvm-virtualsystemmanagementservice-modifysystemcomponentsettings.md)             | 修改一般系統元件設定。<br/>                                                                                                                                                                                             |
| [**ModifySystemSettings**](modifysystemsettings-msvm-virtualsystemmanagementservice.md)                               | 修改虛擬機器設定。<br/>                                                                                                                                                                                                      |
| [**RealizePlannedSystem**](realizeplannedsystem-msvm-virtualsystemmanagementservice.md)                               | 驗證已規劃的虛擬機器設定，並將其轉換為實現的虛擬機器。<br/>                                                                                                                                 |
| [**RemoveBootSourceSettings**](msvm-virtualsystemmanagementservice-removebootsourcesettings.md)                       | 從虛擬系統組態移除虛擬資源設定。<br/> 套用至「目前」虛擬系統設定的元件時，可能會移除作用中虛擬系統的副作用資源。<br/>            |
| [**RemoveFeatureSettings**](removefeaturesettings-msvm-virtualsystemmanagementservice.md)                             | 從虛擬機器乙太網路連接移除功能設定。<br/>                                                                                                                                                                    |
| [**RemoveFibreChannelChap**](removefibrechannelchap-msvm-virtualsystemmanagementservice.md)                           | 從虛擬機器中的綜合光纖通道埠移除 DH CHAP 參數。<br/>                                                                                                                                                    |
| [**RemoveGuestServiceSettings**](msvm-virtualsystemmanagementservice-removeguestservicesettings.md)                   | 從虛擬系統組態中移除來賓服務設定。<br/> 套用至「目前」虛擬系統設定的元件時，可能會修改作用中虛擬系統的副作用來賓服務。<br/>         |
| [**RemoveKvpItems**](removekvpitems-msvm-virtualsystemmanagementservice.md)                                           | 從虛擬機器移除現有的機碼值組。<br/>                                                                                                                                                                                |
| [**RemoveResourceSettings**](removeresourcesettings-msvm-virtualsystemmanagementservice.md)                           | 從虛擬機器設定移除虛擬資源設定。<br/>                                                                                                                                                                 |
| [**RemoveSystemComponentSettings**](msvm-virtualsystemmanagementservice-removesystemcomponentsettings.md)             | 從虛擬系統組態中移除一般元件設定。<br/>                                                                                                                                                                 |
| [**RequestStateChange**](msvm-virtualsystemmanagementservice-requeststatechange.md)                                   | 不支援這個方法。<br/>                                                                                                                                                                                                           |
| [**SetGuestNetworkAdapterConfiguration**](setguestnetworkadapterconfiguration-msvm-virtualsystemmanagementservice.md) | 設定客體作業系統內的網路介面卡。<br/>                                                                                                                                                                      |
| [**SetInitialMachineConfigurationData**](msvm-virtualsystemmanagementservice-setinitialmachineconfigurationdata.md)   | 設定 VM 的初始電腦設定資料。<br/>                                                                                                                                                                                         |
| [**StartService**](msvm-virtualsystemmanagementservice-startservice.md)                                               | 不支援這個方法。<br/>                                                                                                                                                                                                           |
| [**StopService**](msvm-virtualsystemmanagementservice-stopservice.md)                                                 | 不支援這個方法。<br/>                                                                                                                                                                                                           |
| [**TestNetworkConnection**](msvm-virtualsystemmanagementservice-testnetworkconnection.md)                             | 在 Windows 網路虛擬化環境中測試 VM 的網路連線能力。<br/>                                                                                                                                                 |
| [**UpgradeSystemVersion**](msvm-virtualsystemmanagementservice-upgradesystemversion.md)                               | 升級虛擬系統。<br/> 套用至「目前」虛擬系統組態的系統設定時<br/>                                                                                                                 |
| [**ValidatePlannedSystem**](validateplannedsystem-msvm-virtualsystemmanagementservice.md)                             | 驗證指定的計畫系統。<br/>                                                                                                                                                                                                 |



 

### <a name="properties"></a>屬性

**Msvm \_ VirtualSystemManagementService** 類別具有這些屬性。

<dl> <dt>

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

物件的簡短描述。 這個屬性繼承自 [**CIM \_ ManagedElement**](/previous-versions/windows/desktop/iscsitarg/cim-managedelement)，一律設定為「Hyper-v 虛擬系統管理服務」。

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
</dt> <dt>

限定詞： **Key**、 **MaxLen** ( 256 ) 
</dt> </dl>

建立實例時所使用之類別或子類別的名稱。 這個屬性繼承自 [**CIM \_ 服務**](/windows/desktop/CIMWin32Prov/cim-service)，一律設定為 "Msvm \_ VirtualSystemManagementService"。

</dd> <dt>

**說明**
</dt> <dd> <dl> <dt>

資料類型： **字串**
</dt> <dt>

存取類型：唯讀
</dt> </dl>

對物件的描述。 這個屬性是從 [**CIM \_ ManagedElement**](/previous-versions/windows/desktop/iscsitarg/cim-managedelement)繼承而來，而且一律會設定為「用於建立、操作及管理虛擬機器的服務」。

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

**ElementName**
</dt> <dd> <dl> <dt>

資料類型： **字串**
</dt> <dt>

存取類型：唯讀
</dt> </dl>

物件的顯示名稱。 這個屬性繼承自 [**CIM \_ ManagedElement**](/previous-versions/windows/desktop/iscsitarg/cim-managedelement)，一律設定為「Hyper-v 虛擬系統管理服務」。

</dd> <dt>

**EnabledDefault**
</dt> <dd> <dl> <dt>

資料類型： **uint16**
</dt> <dt>

存取類型：唯讀
</dt> </dl>

系統管理員的預設或啟動設定，適用于元素的啟用狀態。 這個屬性繼承自 [**CIM \_ EnabledLogicalElement**](/previous-versions//cc136818(v=vs.85))，而且一律設定為 2 (啟用) 。



| 值                                                                        | 意義            |
|------------------------------------------------------------------------------|--------------------|
| <dl> <dt>2</dt> </dl> | 已啟用<br/> |



 

</dd> <dt>

**EnabledState**
</dt> <dd> <dl> <dt>

資料類型： **uint16**
</dt> <dt>

存取類型：唯讀
</dt> </dl>

專案的已啟用和停用狀態。 這個屬性也可以指出這些要求狀態之間的轉換。 這個屬性繼承自 [**CIM \_ EnabledLogicalElement**](/previous-versions//cc136818(v=vs.85))，而且一律設定為 2 (啟用) 。



| 值                                                                        | 意義            |
|------------------------------------------------------------------------------|--------------------|
| <dl> <dt>2</dt> </dl> | 已啟用<br/> |



 

</dd> <dt>

**HealthState**
</dt> <dd> <dl> <dt>

資料類型： **uint16**
</dt> <dt>

存取類型：唯讀
</dt> </dl>

專案目前的健康情況。 這個屬性會表示此元素的健全狀況，但不一定是它的子元件。 可能的值為0到30，其中5表示元素完全狀況良好，而30表示元素完全無法正常運作。 這個屬性繼承自 [**CIM \_ ManagedSystemElement**](/windows/desktop/CIMWin32Prov/cim-managedsystemelement)，而且一律設定為 5 (確定) 。



| 值                                                                        | 意義                                 |
|------------------------------------------------------------------------------|-----------------------------------------|
| <dl> <dt>5</dt> </dl> | 健全狀況狀態為 [正常]。<br/> |



 

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

**名稱**
</dt> <dd> <dl> <dt>

資料類型： **字串**
</dt> <dt>

存取類型：唯讀
</dt> <dt>

限定詞： **Key**、 **MaxLen** ( 256 ) 
</dt> </dl>

已知物件的標籤。 這個屬性繼承自 [**CIM \_ ManagedSystemElement**](/windows/desktop/CIMWin32Prov/cim-managedsystemelement)，而且一律設定為 "vmms"。

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

物件的目前狀態。 這個屬性繼承自 [**CIM \_ ManagedSystemElement**](/windows/desktop/CIMWin32Prov/cim-managedsystemelement)，而且每個陣列元素一律設定為 2 (確定) 。

</dd> <dt>

**OtherEnabledState**
</dt> <dd> <dl> <dt>

資料類型： **字串**
</dt> <dt>

存取類型：唯讀
</dt> </dl>

描述當 **EnabledState** 屬性設定為 1 ( "Other" ) 時，專案已啟用或停用狀態的字串。 當 **EnabledState** 是1以外的任何值時，這個屬性必須設定為 **Null** 。 這個屬性繼承自 [**CIM \_ EnabledLogicalElement**](/previous-versions//cc136818(v=vs.85))，而且一律設定為 **Null**。

</dd> <dt>

**PrimaryOwnerContact**
</dt> <dd> <dl> <dt>

資料類型： **字串**
</dt> <dt>

存取類型：唯讀
</dt> <dt>

限定詞： **MaxLen** ( 256 ) 
</dt> </dl>

有關如何聯繫服務主要擁有者的任何資訊 (例如電話號碼、電子郵件地址等等) 。 這個屬性繼承自 [**CIM \_ 服務**](/windows/desktop/CIMWin32Prov/cim-service)，一律設為 **Null**。

</dd> <dt>

**PrimaryOwnerName**
</dt> <dd> <dl> <dt>

資料類型： **字串**
</dt> <dt>

存取類型：唯讀
</dt> <dt>

限定詞： **MaxLen** ( 64 ) 
</dt> </dl>

服務的主要擁有者名稱（如果有定義的話）。 主要擁有者是服務的初始支援連絡人。 這個屬性繼承自 [**CIM \_ 服務**](/windows/desktop/CIMWin32Prov/cim-service)，一律設為 **Null**。

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

**RequestedState**
</dt> <dd> <dl> <dt>

資料類型： **uint16**
</dt> <dt>

存取類型：唯讀
</dt> </dl>

上次要求或預期的專案狀態。 元素的實際狀態是由 **EnabledState** 表示。 系統會提供這個屬性來比較專案的最後一個要求和目前狀態。 [**CIM \_ EnabledLogicalElement**](/previous-versions//cc136818(v=vs.85))類別的特定實例可能不支援 **RequestedState** 屬性。 如果發生這種情況，則會使用值 12 ( 「不適用」 ) 。 這個屬性繼承自 **CIM \_ EnabledLogicalElement**，而且一律設定為 12 (不適用) 。



| 值                                                                         | 意義                    |
|-------------------------------------------------------------------------------|----------------------------|
| <dl> <dt>12</dt> </dl> | 不適用。<br/> |



 

</dd> <dt>

**已開始**
</dt> <dd> <dl> <dt>

資料類型： **布林值**
</dt> <dt>

存取類型：唯讀
</dt> </dl>

指出服務目前是否正在執行。 這個屬性繼承自 [**CIM \_ 服務**](/windows/desktop/CIMWin32Prov/cim-service)，一律設定為 **True**。

</dd> <dt>

**StartMode**
</dt> <dd> <dl> <dt>

資料類型： **字串**
</dt> <dt>

存取類型：唯讀
</dt> <dt>

限定詞： **MaxLen** ( 10 ) 
</dt> </dl>

字串值，表示服務是由系統自動啟動、作業系統還是只在要求時才啟動。 這個屬性繼承自 [**CIM \_ 服務**](/windows/desktop/CIMWin32Prov/cim-service)，一律設為 **Null**。

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

描述各種 **OperationalStatus** 陣列值的字串。 這個屬性繼承自 [**CIM \_ ManagedSystemElement**](/windows/desktop/CIMWin32Prov/cim-managedsystemelement)，而且每個陣列元素一律設定為「服務正在正常執行」。

</dd> <dt>

**SystemCreationClassName**
</dt> <dd> <dl> <dt>

資料類型： **字串**
</dt> <dt>

存取類型：唯讀
</dt> <dt>

限定詞： **Key**、 **MaxLen** ( 256 ) 
</dt> </dl>

範圍系統的建立類別名稱。 這個屬性是從 [**CIM \_ 服務**](/windows/desktop/CIMWin32Prov/cim-service)繼承而來的，而且一律設定為「Msvm 的程式集」 \_ 。

</dd> <dt>

**SystemName**
</dt> <dd> <dl> <dt>

資料類型： **字串**
</dt> <dt>

存取類型：唯讀
</dt> <dt>

限定詞： **Key**、 **MaxLen** ( 256 ) 
</dt> </dl>

主控電腦系統的 NetBIOS 名稱。 這個屬性繼承自 [**CIM \_ 服務**](/windows/desktop/CIMWin32Prov/cim-service)。

</dd> <dt>

**TimeOfLastStateChange**
</dt> <dd> <dl> <dt>

資料類型： **datetime**
</dt> <dt>

存取類型：唯讀
</dt> </dl>

專案的已啟用狀態上次變更的日期或時間。 這個屬性繼承自 [**CIM \_ EnabledLogicalElement**](/previous-versions//cc136818(v=vs.85))。

</dd> <dt>

**TransitioningToState**
</dt> <dd> <dl> <dt>

資料類型： **uint16**
</dt> <dt>

存取類型：唯讀
</dt> </dl>

指出實例正在轉換的目標狀態。 這個屬性繼承自 [**CIM \_ EnabledLogicalElement**](/previous-versions//cc136818(v=vs.85))，而且一律設定為 **Null**。

</dd> </dl>

## <a name="remarks"></a>備註

存取 **Msvm \_ VirtualSystemManagementService** 類別可能受 UAC 篩選所限制。 如需詳細資訊，請參閱 [使用者帳戶控制和 WMI](/windows/desktop/WmiSdk/user-account-control-and-wmi)。

## <a name="requirements"></a>規格需求



| 需求 | 值 |
|-------------------------------------|---------------------------------------------------------------------------------------------------------|
| 最低支援的用戶端<br/> | \[僅 Windows 8 桌面應用程式\]<br/>                                                              |
| 最低支援的伺服器<br/> | 僅限 Windows Server 2012 \[ desktop 應用程式\]<br/>                                                    |
| 命名空間<br/>                | 根 \\ 虛擬化 \\ V2<br/>                                                                     |
| MOF<br/>                      | <dl> <dt>WindowsVirtualization。</dt> </dl> |
| DLL<br/>                      | <dl> <dt>Vmms.exe</dt> </dl>                     |



## <a name="see-also"></a>另請參閱

<dl> <dt>

[**CIM \_ VirtualSystemManagementService**](cim-virtualsystemmanagementservice.md)
</dt> <dt>

[**CIM \_ VirtualSystemManagementService**](/previous-versions//cc136952(v=vs.85))
</dt> <dt>

[**Msvm \_ VirtualSystemManagementService (V1)**](/previous-versions/windows/desktop/legacy/cc136940(v=vs.85))
</dt> <dt>

[虛擬系統管理類別](virtual-system-management-classes.md)
</dt> </dl>

 

