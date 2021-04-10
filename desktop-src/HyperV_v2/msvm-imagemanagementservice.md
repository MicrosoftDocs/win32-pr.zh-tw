---
description: 管理虛擬機器的虛擬媒體 ( .vhd、.vhdx、.iso 或 .vfd 檔案) 。
ms.assetid: 7caa720e-37cf-454e-8634-f2bd82bcf83d
title: Msvm_ImageManagementService 類別
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Msvm_ImageManagementService
- Msvm_ImageManagementService.InstanceID
- Msvm_ImageManagementService.Caption
- Msvm_ImageManagementService.Description
- Msvm_ImageManagementService.ElementName
- Msvm_ImageManagementService.InstallDate
- Msvm_ImageManagementService.OperationalStatus
- Msvm_ImageManagementService.StatusDescriptions
- Msvm_ImageManagementService.Status
- Msvm_ImageManagementService.HealthState
- Msvm_ImageManagementService.CommunicationStatus
- Msvm_ImageManagementService.DetailedStatus
- Msvm_ImageManagementService.OperatingStatus
- Msvm_ImageManagementService.PrimaryStatus
- Msvm_ImageManagementService.EnabledState
- Msvm_ImageManagementService.OtherEnabledState
- Msvm_ImageManagementService.RequestedState
- Msvm_ImageManagementService.EnabledDefault
- Msvm_ImageManagementService.TimeOfLastStateChange
- Msvm_ImageManagementService.AvailableRequestedStates
- Msvm_ImageManagementService.TransitioningToState
- Msvm_ImageManagementService.SystemCreationClassName
- Msvm_ImageManagementService.SystemName
- Msvm_ImageManagementService.CreationClassName
- Msvm_ImageManagementService.Name
- Msvm_ImageManagementService.PrimaryOwnerName
- Msvm_ImageManagementService.PrimaryOwnerContact
- Msvm_ImageManagementService.StartMode
- Msvm_ImageManagementService.Started
api_type:
- DllExport
api_location:
- vmms.exe
ms.openlocfilehash: 36a45041ec41b8fbd87801a65fa2b28ac99da6a8
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/07/2021
ms.locfileid: "103690863"
---
# <a name="msvm_imagemanagementservice-class"></a>Msvm \_ ImageManagementService 類別

管理虛擬機器的虛擬媒體 ( .vhd、.vhdx、.iso 或 .vfd 檔案) 。

下列語法已簡化受控物件格式 (MOF) 程式碼，並且包含所有繼承的屬性。

## <a name="syntax"></a>語法

``` syntax
[Dynamic, Provider("VmmsWmiInstanceAndMethodProvider"), AMENDMENT]
class Msvm_ImageManagementService : CIM_Service
{
  string   InstanceID;
  string   Caption = "Hyper-V Image Management Service";
  string   Description = "Provides Image Management servicing for Hyper-V";
  string   ElementName = "Hyper-V Image Management Service";
  datetime InstallDate;
  uint16   OperationalStatus[] = { 2 };
  string   StatusDescriptions[] = { "OK" };
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
  string   CreationClassName = "Msvm_ImageManagementService";
  string   Name = "vhdsvc";
  string   PrimaryOwnerName;
  string   PrimaryOwnerContact;
  string   StartMode;
  boolean  Started = True;
};
```

## <a name="members"></a>成員

**Msvm \_ ImageManagementService** 類別具有下列類型的成員：

-   [方法](#methods)
-   [屬性](#properties)

### <a name="methods"></a>方法

**Msvm \_ ImageManagementService** 類別具有這些方法。



| 方法                                                                                                           | 描述                                                                                                                                                                                                                                 |
|:-----------------------------------------------------------------------------------------------------------------|:--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [**AttachVirtualHardDisk**](attachvirtualharddisk-msvm-imagemanagementservice.md)                               | 以回送模式連接虛擬磁片影像檔。<br/>                                                                                                                                                                             |
| [**CompactVirtualHardDisk**](compactvirtualharddisk-msvm-imagemanagementservice.md)                             | 壓縮虛擬硬碟檔案。<br/>                                                                                                                                                                                               |
| [**ConvertVirtualHardDisk**](convertvirtualharddisk-msvm-imagemanagementservice.md)                             | 將現有的虛擬硬碟轉換成不同的類型或格式。<br/>                                                                                                                                                            |
| [**ConvertVirtualHardDiskToVHDSet**](msvm-imagemanagementservice-convertvirtualharddisktovhdset.md)             | 藉由建立新的 VHD 設定檔案與現有的虛擬硬碟來轉換虛擬硬碟檔案。<br/>                                                                                                                       |
| [**CreateVirtualFloppyDisk**](createvirtualfloppydisk-msvm-imagemanagementservice.md)                           | 建立虛擬磁片檔案。<br/>                                                                                                                                                                                              |
| [**CreateVirtualHardDisk**](createvirtualharddisk-msvm-imagemanagementservice.md)                               | 建立虛擬硬碟檔案。<br/>                                                                                                                                                                                                |
| [**DeleteVHDSnapshot**](msvm-imagemanagementservice-deletevhdsnapshot.md)                                       | 刪除 VHD 設定檔內的 VHD 快照集專案。<br/>                                                                                                                                                                              |
| [**FindMountedStorageImageInstance**](msvm-imagemanagementservice-findmountedstorageimageinstance.md)           | 尋找 \_ 指定磁片映射路徑的 Msvm MountedStorageImage 物件。<br/>                                                                                                                                                            |
| [**GetVHDSetInformation**](msvm-imagemanagementservice-getvhdsetinformation.md)                                 | 抓取 VHD 設定檔案的相關資訊。<br/>                                                                                                                                                                                      |
| [**GetVHDSnapshotInformation**](msvm-imagemanagementservice-getvhdsnapshotinformation.md)                       | 抓取 VHD 設定檔中 VHD 快照集的相關資訊。<br/>                                                                                                                                                                |
| [**GetVirtualDiskChanges**](msvm-imagemanagementservice-getvirtualdiskchanges.md)                               | 從提供的復原變更追蹤識別碼或 VHDSet 快照集識別碼之後，抓取虛擬磁片指定區域的變更清單。<br/>                                                                                     |
| [**GetVirtualHardDiskSettingData**](getvirtualharddisksettingdata-msvm-imagemanagementservice.md)               | 抓取與虛擬硬碟檔案相關聯的設定資料。<br/>                                                                                                                                                                  |
| [**GetVirtualHardDiskState**](getvirtualharddiskstate-msvm-imagemanagementservice.md)                           | 捕獲虛擬硬碟檔案的狀態。<br/>                                                                                                                                                                                      |
| [**MergeVirtualHardDisk**](mergevirtualharddisk-msvm-imagemanagementservice.md)                                 | 使用鏈中的一或多個父虛擬硬碟，合併差異鏈中的子系虛擬硬碟。<br/>                                                                                                                |
| [**OptimizeVHDSet**](msvm-imagemanagementservice-optimizevhdset.md)                                             | 將 VHD 設定檔案優化，以使用較少的磁碟空間。<br/>                                                                                                                                                                                 |
| [**RequestStateChange**](msvm-imagemanagementservice-requeststatechange.md)                                     | 要求狀態變更。<br/>                                                                                                                                                                                                         |
| [**ResizeVirtualHardDisk**](resizevirtualharddisk-msvm-imagemanagementservice.md)                               | 調整現有虛擬硬碟的大小。<br/>                                                                                                                                                                                           |
| [**SetParentVirtualHardDisk**](setparentvirtualharddisk-msvm-imagemanagementservice.md)                         | 更新指定分葉和子虛擬硬碟檔案的父系。<br/>                                                                                                                                                     |
| [**SetVHDSnapshotInformation**](msvm-imagemanagementservice-setvhdsnapshotinformation.md)                       | 編輯 VHD 設定檔內的 VHD 快照集專案。 如果已有問題的快照集識別碼，則會以新的專案覆寫現有的快照集專案。 否則，新的專案會新增至 VHD 設定檔案。<br/> |
| [**SetVirtualHardDiskSettingData**](setvirtualharddisksettingdata-msvm-imagemanagementservice.md)               | 設定虛擬硬碟檔案。<br/>                                                                                                                                                                                                   |
| [**StartService**](msvm-imagemanagementservice-startservice.md)                                                 | 啟動服務。<br/>                                                                                                                                                                                                              |
| [**StopService**](msvm-imagemanagementservice-stopservice.md)                                                   | 停止服務。<br/>                                                                                                                                                                                                               |
| [**ValidatePersistentReservationSupport**](msvm-imagemanagementservice-validatepersistentreservationsupport.md) | 驗證檔案系統是否可以支援啟用持續性保留的虛擬硬碟。<br/>                                                                                                                            |
| [**ValidateVirtualHardDisk**](validatevirtualharddisk-msvm-imagemanagementservice.md)                           | 驗證是否可在唯讀模式中開啟虛擬磁片映射。<br/>                                                                                                                                                          |



 

### <a name="properties"></a>屬性

**Msvm \_ ImageManagementService** 類別具有這些屬性。

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

物件的簡短描述。 這個屬性會繼承自 [**CIM \_ ManagedElement**](/previous-versions/windows/desktop/iscsitarg/cim-managedelement)，而且一律會設定為「Hyper-v 映射管理服務」。

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

建立實例時所使用之類別或子類別的名稱。 這個屬性繼承自 [**CIM \_ 服務**](/windows/desktop/CIMWin32Prov/cim-service)，一律設定為 "Msvm \_ ImageManagementService"。

</dd> <dt>

**說明**
</dt> <dd> <dl> <dt>

資料類型： **字串**
</dt> <dt>

存取類型：唯讀
</dt> </dl>

對物件的描述。 這個屬性是從 [**CIM \_ ManagedElement**](/previous-versions/windows/desktop/iscsitarg/cim-managedelement)繼承而來的，而且一律設定為「為 Hyper-v 提供映射管理服務」。

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

物件的顯示名稱。 這個屬性會繼承自 [**CIM \_ ManagedElement**](/previous-versions/windows/desktop/iscsitarg/cim-managedelement)，而且一律會設定為「Hyper-v 映射管理服務」。

</dd> <dt>

**EnabledDefault**
</dt> <dd> <dl> <dt>

資料類型： **uint16**
</dt> <dt>

存取類型：唯讀
</dt> </dl>

系統管理員的預設或啟動設定，適用于元素的啟用狀態。 這個屬性繼承自 [**CIM \_ EnabledLogicalElement**](/previous-versions//cc136818(v=vs.85))，而且一律設定為 2 (啟用) 。

</dd> <dt>

**EnabledState**
</dt> <dd> <dl> <dt>

資料類型： **uint16**
</dt> <dt>

存取類型：唯讀
</dt> </dl>

專案的已啟用和停用狀態。 也可以指出這些要求狀態之間的轉換。 這個屬性繼承自 [**CIM \_ EnabledLogicalElement**](/previous-versions//cc136818(v=vs.85))，而且一律設定為 2 (啟用) 。

</dd> <dt>

**HealthState**
</dt> <dd> <dl> <dt>

資料類型： **uint16**
</dt> <dt>

存取類型：唯讀
</dt> </dl>

專案目前的健康情況。 這個屬性會表示此元素的健全狀況，但不一定是它的子元件。 可能的值為0到30，其中5表示元素完全狀況良好，而30表示元素完全無法正常運作。 這個屬性繼承自 [**CIM \_ ManagedSystemElement**](/windows/desktop/CIMWin32Prov/cim-managedsystemelement)，而且一律設定為5。

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

限定詞： **Key**、 **Override** ( "Name" ) 、 **MaxLen** (256) 
</dt> </dl>

已知物件的標籤。 這個屬性繼承自 [**CIM \_ 服務**](/windows/desktop/CIMWin32Prov/cim-service)，一律設定為 "vhdsvc"。

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

當 **EnabledState** 屬性設定為 1 (其他) 時，元素的啟用或停用狀態。 當 **EnabledState** 是1以外的任何值時，這個屬性必須設定為 **Null** 。 這個屬性繼承自 [**CIM \_ EnabledLogicalElement**](/previous-versions//cc136818(v=vs.85))，而且一律設定為 **Null**。

</dd> <dt>

**PrimaryOwnerContact**
</dt> <dd> <dl> <dt>

資料類型： **字串**
</dt> <dt>

存取類型：唯讀
</dt> </dl>

提供如何達到服務主要擁有者的相關資訊 (例如，電話號碼、電子郵件地址等等) 的字串。 這個屬性繼承自 [**CIM \_ 服務**](/windows/desktop/CIMWin32Prov/cim-service)，一律設為 **Null**。

</dd> <dt>

**PrimaryOwnerName**
</dt> <dd> <dl> <dt>

資料類型： **字串**
</dt> <dt>

存取類型：唯讀
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

上次要求或預期的專案狀態。 元素的實際狀態是由 **EnabledState** 表示。 這個屬性是用來比較最後一個要求和目前啟用或停用的狀態。 **EnabledLogicalElement** 的特定實例可能不支援 **RequestedStateChange**。 如果發生這種情況，則會使用值 12 (不適用) 。 這個屬性繼承自 [**CIM \_ EnabledLogicalElement**](/previous-versions//cc136818(v=vs.85))，而且一律設定為 12 (不適用) 。

</dd> <dt>

**已開始**
</dt> <dd> <dl> <dt>

資料類型： **布林值**
</dt> <dt>

存取類型：唯讀
</dt> </dl>

指出服務是否已啟動。 這個屬性繼承自 [**CIM \_ 服務**](/windows/desktop/CIMWin32Prov/cim-service)，一律設定為 **True**。

</dd> <dt>

**StartMode**
</dt> <dd> <dl> <dt>

資料類型： **字串**
</dt> <dt>

存取類型：唯讀
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

描述各種 **OperationalStatus** 陣列值的字串。 這個屬性繼承自 [**CIM \_ ManagedSystemElement**](/windows/desktop/CIMWin32Prov/cim-managedsystemelement)。

</dd> <dt>

**SystemCreationClassName**
</dt> <dd> <dl> <dt>

資料類型： **字串**
</dt> <dt>

存取類型：唯讀
</dt> </dl>

範圍系統的建立類別名稱。 這個屬性是從 [**CIM \_ 服務**](/windows/desktop/CIMWin32Prov/cim-service)繼承而來的，而且一律設定為「Msvm 的程式集」 \_ 。

</dd> <dt>

**SystemName**
</dt> <dd> <dl> <dt>

資料類型： **字串**
</dt> <dt>

存取類型：唯讀
</dt> </dl>

主控電腦系統的名稱。 這個屬性繼承自 [**CIM \_ 服務**](/windows/desktop/CIMWin32Prov/cim-service)。

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

存取 **Msvm \_ ImageManagementService** 類別可能受 UAC 篩選所限制。 如需詳細資訊，請參閱 [使用者帳戶控制和 WMI](/windows/desktop/WmiSdk/user-account-control-and-wmi)。

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

[**CIM \_ 服務**](cim-service.md)
</dt> <dt>

[**CIM \_ 服務**](/windows/desktop/CIMWin32Prov/cim-service)
</dt> <dt>

[儲存類別](storage-classes.md)
</dt> </dl>

 

