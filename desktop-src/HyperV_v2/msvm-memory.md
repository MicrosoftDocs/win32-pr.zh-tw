---
description: 代表目前配置給虛擬機器的記憶體。
ms.assetid: 4CAA64FC-5A06-409B-9E92-32DF3F47D5FD
title: Msvm_Memory 類別
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Msvm_Memory
- Msvm_Memory.SetPowerState
- Msvm_Memory.EnableDevice
- Msvm_Memory.OnlineDevice
- Msvm_Memory.QuiesceDevice
- Msvm_Memory.SaveProperties
- Msvm_Memory.RestoreProperties
- Msvm_Memory.InstanceID
- Msvm_Memory.Caption
- Msvm_Memory.Description
- Msvm_Memory.ElementName
- Msvm_Memory.InstallDate
- Msvm_Memory.OperationalStatus
- Msvm_Memory.StatusDescriptions
- Msvm_Memory.Status
- Msvm_Memory.HealthState
- Msvm_Memory.CommunicationStatus
- Msvm_Memory.DetailedStatus
- Msvm_Memory.OperatingStatus
- Msvm_Memory.PrimaryStatus
- Msvm_Memory.EnabledState
- Msvm_Memory.OtherEnabledState
- Msvm_Memory.RequestedState
- Msvm_Memory.EnabledDefault
- Msvm_Memory.TimeOfLastStateChange
- Msvm_Memory.AvailableRequestedStates
- Msvm_Memory.TransitioningToState
- Msvm_Memory.SystemCreationClassName
- Msvm_Memory.SystemName
- Msvm_Memory.CreationClassName
- Msvm_Memory.DeviceID
- Msvm_Memory.PowerManagementSupported
- Msvm_Memory.PowerManagementCapabilities
- Msvm_Memory.Availability
- Msvm_Memory.StatusInfo
- Msvm_Memory.LastErrorCode
- Msvm_Memory.ErrorDescription
- Msvm_Memory.ErrorCleared
- Msvm_Memory.OtherIdentifyingInfo
- Msvm_Memory.PowerOnHours
- Msvm_Memory.TotalPowerOnHours
- Msvm_Memory.IdentifyingDescriptions
- Msvm_Memory.AdditionalAvailability
- Msvm_Memory.MaxQuiesceTime
- Msvm_Memory.DataOrganization
- Msvm_Memory.Purpose
- Msvm_Memory.Access
- Msvm_Memory.BlockSize
- Msvm_Memory.NumberOfBlocks
- Msvm_Memory.ConsumableBlocks
- Msvm_Memory.IsBasedOnUnderlyingRedundancy
- Msvm_Memory.SequentialAccess
- Msvm_Memory.ExtentStatus
- Msvm_Memory.NoSinglePointOfFailure
- Msvm_Memory.DataRedundancy
- Msvm_Memory.PackageRedundancy
- Msvm_Memory.DeltaReservation
- Msvm_Memory.Primordial
- Msvm_Memory.Name
- Msvm_Memory.NameFormat
- Msvm_Memory.NameNamespace
- Msvm_Memory.OtherNameNamespace
- Msvm_Memory.OtherNameFormat
- Msvm_Memory.Volatile
- Msvm_Memory.ErrorMethodology
- Msvm_Memory.StartingAddress
- Msvm_Memory.EndingAddress
- Msvm_Memory.ErrorInfo
- Msvm_Memory.OtherErrorDescription
- Msvm_Memory.CorrectableError
- Msvm_Memory.ErrorTime
- Msvm_Memory.ErrorAccess
- Msvm_Memory.ErrorTransferSize
- Msvm_Memory.ErrorData
- Msvm_Memory.ErrorDataOrder
- Msvm_Memory.ErrorAddress
- Msvm_Memory.SystemLevelAddress
- Msvm_Memory.ErrorResolution
- Msvm_Memory.AdditionalErrorData
api_type:
- DllExport
api_location:
- vmms.exe
ms.openlocfilehash: d149c733bfc9ccf408b7798a37a762b947eac23b25888beeda375e77c60417f3
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/11/2021
ms.locfileid: "119148351"
---
# <a name="msvm_memory-class"></a>Msvm \_ Memory 類別

代表目前配置給虛擬機器的記憶體。

下列語法已簡化受控物件格式 (MOF) 程式碼，並且包含所有繼承的屬性。

## <a name="syntax"></a>語法

``` syntax
[Dynamic, Provider("VmmsWmiInstanceAndMethodProvider"), AMENDMENT]
class Msvm_Memory : CIM_Memory
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
  uint16   EnabledDefault;
  datetime TimeOfLastStateChange;
  uint16   AvailableRequestedStates[];
  uint16   TransitioningToState;
  string   SystemCreationClassName;
  string   SystemName;
  uint16   CreationClassName;
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
  uint16   AdditionalAvailability[] = { 6 };
  uint64   MaxQuiesceTime;
  uint16   DataOrganization = 2;
  string   Purpose = "System Memory";
  uint16   Access = 3;
  uint64   BlockSize = 1048576;
  uint64   NumberOfBlocks;
  uint64   ConsumableBlocks;
  boolean  IsBasedOnUnderlyingRedundancy = False;
  boolean  SequentialAccess = False;
  uint16   ExtentStatus[] = 2;
  boolean  NoSinglePointOfFailure = False;
  uint16   DataRedundancy = 1;
  uint16   PackageRedundancy = 0;
  uint8    DeltaReservation = 0;
  boolean  Primordial;
  string   Name = "GUID";
  uint16   NameFormat = 0;
  uint16   NameNamespace = 0;
  string   OtherNameNamespace;
  string   OtherNameFormat;
  boolean  Volatile = True;
  string   ErrorMethodology;
  uint64   StartingAddress = 0;
  uint64   EndingAddress;
  uint16   ErrorInfo;
  string   OtherErrorDescription;
  boolean  CorrectableError;
  datetime ErrorTime;
  uint16   ErrorAccess;
  uint32   ErrorTransferSize;
  uint8    ErrorData[];
  uint16   ErrorDataOrder;
  uint64   ErrorAddress;
  boolean  SystemLevelAddress;
  uint64   ErrorResolution;
  uint8    AdditionalErrorData[];
};
```

## <a name="members"></a>成員

**Msvm \_ Memory** 類別具有下列類型的成員：

-   [方法](#methods)
-   [屬性](#properties)

### <a name="methods"></a>方法

**Msvm \_ Memory** 類別具有這些方法。



| 方法                                                       | 描述                              |
|:-------------------------------------------------------------|:-----------------------------------------|
| **EnableDevice**                                             | 不支援這個方法。<br/> |
| **OnlineDevice**                                             | 不支援這個方法。<br/> |
| **QuiesceDevice**                                            | 不支援這個方法。<br/> |
| [**RequestStateChange**](msvm-memory-requeststatechange.md) | 要求狀態變更。<br/>      |
| [**重設**](msvm-memory-reset.md)                           | 重設虛擬記憶體。<br/>    |
| **RestoreProperties**                                        | 不支援這個方法。<br/> |
| **SaveProperties**                                           | 不支援這個方法。<br/> |
| **SetPowerState**                                            | 不支援這個方法。<br/> |



 

### <a name="properties"></a>屬性

**Msvm \_ Memory** 類別具有這些屬性。

<dl> <dt>

**存取**
</dt> <dd> <dl> <dt>

資料類型： **uint16**
</dt> <dt>

存取類型：唯讀
</dt> </dl>

描述媒體的讀取/寫入屬性。 這個屬性繼承自 [**CIM \_ StorageExtent**](/windows/desktop/CIMWin32Prov/cim-storageextent)，預設會設定為 3 (讀取/寫入支援的) 。

</dd> <dt>

**AdditionalAvailability**
</dt> <dd> <dl> <dt>

資料類型： **uint16** 陣列
</dt> <dt>

存取類型：唯讀
</dt> </dl>

這個屬性繼承自 [**CIM \_ LogicalDevice**](/windows/desktop/CIMWin32Prov/cim-logicaldevice)，且設定為 6 (不適用) 。

</dd> <dt>

**AdditionalErrorData**
</dt> <dd> <dl> <dt>

資料類型： **uint8** 陣列
</dt> <dt>

存取類型：唯讀
</dt> </dl>

這個屬性繼承自 [**CIM \_ 記憶體**](/windows/desktop/CIMWin32Prov/cim-memory)，但未使用。

</dd> <dt>

**可用性**
</dt> <dd> <dl> <dt>

資料類型： **uint16**
</dt> <dt>

存取類型：唯讀
</dt> </dl>

這個屬性繼承自 [**CIM \_ LogicalDevice**](/windows/desktop/CIMWin32Prov/cim-logicaldevice)。

</dd> <dt>

**AvailableRequestedStates**
</dt> <dd> <dl> <dt>

資料類型： **uint16** 陣列
</dt> <dt>

存取類型：唯讀
</dt> </dl>

指出 **RequestStateChange** 方法的 *RequestedState* 參數可能的值。 這個屬性繼承自 [**CIM \_ EnabledLogicalElement**](/previous-versions//cc136818(v=vs.85))。

</dd> <dt>

**BlockSize**
</dt> <dd> <dl> <dt>

資料類型： **uint64**
</dt> <dt>

存取類型：唯讀
</dt> </dl>

形成儲存範圍之區塊的大小（以位元組為單位）。 如果變數區塊大小，則應該指定最大區塊大小（以位元組為單位）。 如果區塊大小未知，或區塊概念無效 (例如，針對匯總延伸區、記憶體或邏輯磁片) ，請輸入 1 (一個) 。 這個屬性繼承自 [**CIM \_ StorageExtent**](/windows/desktop/CIMWin32Prov/cim-storageextent)，一律設為1048576。

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

**ConsumableBlocks**
</dt> <dd> <dl> <dt>

資料類型： **uint64**
</dt> <dt>

存取類型：唯讀
</dt> </dl>

使用 BasedOn 關聯將儲存範圍分層時 **，可** 供取用的區塊數目上限（大小上限）。 這個屬性繼承自 [**CIM \_ StorageExtent**](/windows/desktop/CIMWin32Prov/cim-storageextent)，而且一律設定為 **Null**。

</dd> <dt>

**CorrectableError**
</dt> <dd> <dl> <dt>

資料類型： **布林值**
</dt> <dt>

存取類型：唯讀
</dt> </dl>

這個屬性繼承自 [**CIM \_ 記憶體**](/windows/desktop/CIMWin32Prov/cim-memory)，但未使用。

</dd> <dt>

**CreationClassName**
</dt> <dd> <dl> <dt>

資料類型： **uint16**
</dt> <dt>

存取類型：唯讀
</dt> </dl>

建立實例時所使用之類別或子類別的名稱。 這個屬性繼承自 [**CIM \_ LogicalDevice**](/windows/desktop/CIMWin32Prov/cim-logicaldevice)。

</dd> <dt>

**DataOrganization**
</dt> <dd> <dl> <dt>

資料類型： **uint16**
</dt> <dt>

存取類型：唯讀
</dt> </dl>

使用的資料組織類型。 這個屬性繼承自 [**CIM \_ StorageExtent**](/windows/desktop/CIMWin32Prov/cim-storageextent)，而且一律設定為2。

</dd> <dt>

**DataRedundancy**
</dt> <dd> <dl> <dt>

資料類型： **uint16**
</dt> <dt>

存取類型：唯讀
</dt> </dl>

目前維護之資料的完整複本數目。 這個屬性繼承自 [**CIM \_ StorageExtent**](/windows/desktop/CIMWin32Prov/cim-storageextent)，而且一律設定為1。

</dd> <dt>

**DeltaReservation**
</dt> <dd> <dl> <dt>

資料類型： **uint8**
</dt> <dt>

存取類型：唯讀
</dt> </dl>

Delta 保留的目前值。 這個屬性繼承自 [**CIM \_ StorageExtent**](/windows/desktop/CIMWin32Prov/cim-storageextent)，而且一律設定為0。

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

系統管理員的預設或啟動設定，適用于元素的啟用狀態。 這個屬性繼承自 [**CIM \_ EnabledLogicalElement**](/previous-versions//cc136818(v=vs.85))。

</dd> <dt>

**EnabledState**
</dt> <dd> <dl> <dt>

資料類型： **uint16**
</dt> <dt>

存取類型：唯讀
</dt> </dl>

專案的已啟用和停用狀態。 也可以指出這些要求狀態之間的轉換。 這個屬性繼承自 [**CIM \_ EnabledLogicalElement**](/previous-versions//cc136818(v=vs.85))。



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

**EndingAddress**
</dt> <dd> <dl> <dt>

資料類型： **uint64**
</dt> <dt>

存取類型：唯讀
</dt> </dl>

連續記憶體區塊的結束位址。 由於 **StartingAddress** 屬性一律為0，因此這個值一律會反映虛擬機器中的總記憶體量。

</dd> <dt>

**ErrorAccess**
</dt> <dd> <dl> <dt>

資料類型： **uint16**
</dt> <dt>

存取類型：唯讀
</dt> </dl>

這個屬性繼承自 [**CIM \_ 記憶體**](/windows/desktop/CIMWin32Prov/cim-memory)，但未使用。

</dd> <dt>

**ErrorAddress**
</dt> <dd> <dl> <dt>

資料類型： **uint64**
</dt> <dt>

存取類型：唯讀
</dt> </dl>

這個屬性繼承自 [**CIM \_ 記憶體**](/windows/desktop/CIMWin32Prov/cim-memory)，但未使用。

</dd> <dt>

**ErrorCleared**
</dt> <dd> <dl> <dt>

資料類型： **布林值**
</dt> <dt>

存取類型：唯讀
</dt> </dl>

這個屬性繼承自 [**CIM \_ LogicalDevice**](/windows/desktop/CIMWin32Prov/cim-logicaldevice)，但不會使用它。

</dd> <dt>

**ErrorData**
</dt> <dd> <dl> <dt>

資料類型： **uint8** 陣列
</dt> <dt>

存取類型：唯讀
</dt> </dl>

這個屬性繼承自 [**CIM \_ 記憶體**](/windows/desktop/CIMWin32Prov/cim-memory)，但未使用。

</dd> <dt>

**ErrorDataOrder**
</dt> <dd> <dl> <dt>

資料類型： **uint16**
</dt> <dt>

存取類型：唯讀
</dt> </dl>

這個屬性繼承自 [**CIM \_ 記憶體**](/windows/desktop/CIMWin32Prov/cim-memory)，但未使用。

</dd> <dt>

**ErrorDescription**
</dt> <dd> <dl> <dt>

資料類型： **字串**
</dt> <dt>

存取類型：唯讀
</dt> </dl>

這個屬性繼承自 [**CIM \_ LogicalDevice**](/windows/desktop/CIMWin32Prov/cim-logicaldevice)，但不會使用它。

</dd> <dt>

**ErrorInfo**
</dt> <dd> <dl> <dt>

資料類型： **uint16**
</dt> <dt>

存取類型：唯讀
</dt> </dl>

這個屬性繼承自 [**CIM \_ 記憶體**](/windows/desktop/CIMWin32Prov/cim-memory)，但未使用。

</dd> <dt>

**ErrorMethodology**
</dt> <dd> <dl> <dt>

資料類型： **字串**
</dt> <dt>

存取類型：唯讀
</dt> </dl>

描述此儲存範圍所支援之錯誤偵測和更正類型的字串。 這個屬性會繼承自 [**CIM \_ 記憶體**](/windows/desktop/CIMWin32Prov/cim-memory)，而且一律會設定為 **Null**。

</dd> <dt>

**ErrorResolution**
</dt> <dd> <dl> <dt>

資料類型： **uint64**
</dt> <dt>

存取類型：唯讀
</dt> </dl>

這個屬性繼承自 [**CIM \_ 記憶體**](/windows/desktop/CIMWin32Prov/cim-memory)，但未使用。

</dd> <dt>

**ErrorTime**
</dt> <dd> <dl> <dt>

資料類型： **datetime**
</dt> <dt>

存取類型：唯讀
</dt> </dl>

這個屬性繼承自 [**CIM \_ 記憶體**](/windows/desktop/CIMWin32Prov/cim-memory) ，但未使用。

</dd> <dt>

**ErrorTransferSize**
</dt> <dd> <dl> <dt>

資料類型： **uint32**
</dt> <dt>

存取類型：唯讀
</dt> </dl>

這個屬性繼承自 [**CIM \_ 記憶體**](/windows/desktop/CIMWin32Prov/cim-memory)，但未使用。

</dd> <dt>

**ExtentStatus**
</dt> <dd> <dl> <dt>

資料類型： **uint16** 陣列
</dt> <dt>

存取類型：唯讀
</dt> </dl>

儲存體範圍的其他狀態資訊超出在 **OperationalStatus** 中捕捉到的範圍，以及繼承自 [**CIM \_ ManagedSystemElement**](/windows/desktop/CIMWin32Prov/cim-managedsystemelement)的其他屬性。 這項額外資訊 (例如，「停用保護」、值 = 9) 是在 **VolumeStatus** 屬性中捕捉。 這個屬性繼承自 [**CIM \_ StorageExtent**](/windows/desktop/CIMWin32Prov/cim-storageextent)，而且一律設定為 2 (無/不適用) 。

</dd> <dt>

**HealthState**
</dt> <dd> <dl> <dt>

資料類型： **uint16**
</dt> <dt>

存取類型：唯讀
</dt> </dl>

專案目前的健康情況。 這個屬性會表示此元素的健全狀況，但不一定是它的子元件。 可能的值為0到30，其中5表示元素完全狀況良好，而30表示元素完全無法正常運作。 這個屬性繼承自 [**CIM \_ ManagedSystemElement**](/windows/desktop/CIMWin32Prov/cim-managedsystemelement)，而且一律設定為5。

</dd> <dt>

**IdentifyingDescriptions**
</dt> <dd> <dl> <dt>

資料類型： **字串** 陣列
</dt> <dt>

存取類型：唯讀
</dt> </dl>

這個屬性會繼承自 [**CIM \_ LogicalDevice**](/windows/desktop/CIMWin32Prov/cim-logicaldevice)，而且會設定為 **Null**。

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

**IsBasedOnUnderlyingRedundancy**
</dt> <dd> <dl> <dt>

資料類型： **布林值**
</dt> <dt>

存取類型：唯讀
</dt> </dl>

如果基礎儲存範圍參與儲存體的冗余群組，**則為 True** 。 這個屬性繼承自 [**CIM \_ StorageExtent**](/windows/desktop/CIMWin32Prov/cim-storageextent)，一律設為 **False**。

</dd> <dt>

**LastErrorCode**
</dt> <dd> <dl> <dt>

資料類型： **uint32**
</dt> <dt>

存取類型：唯讀
</dt> </dl>

這個屬性繼承自 [**CIM \_ LogicalDevice**](/windows/desktop/CIMWin32Prov/cim-logicaldevice)，但不會使用它。

</dd> <dt>

**MaxQuiesceTime**
</dt> <dd> <dl> <dt>

資料類型： **uint64**
</dt> <dt>

存取類型：唯讀
</dt> </dl>

這個屬性繼承自 [**CIM \_ LogicalDevice**](/windows/desktop/CIMWin32Prov/cim-logicaldevice)，但不會使用它。

</dd> <dt>

**名稱**
</dt> <dd> <dl> <dt>

資料類型： **字串**
</dt> <dt>

存取類型：唯讀
</dt> <dt>

限定詞： **MaxLen** (1024) ，覆 **寫** ( "Name" ) 
</dt> </dl>

已知物件的標籤。 子類別化時，可以將這個屬性覆寫為索引鍵屬性。 這個屬性繼承自 [**CIM \_ StorageExtent**](/windows/desktop/CIMWin32Prov/cim-storageextent)，而且一律設定為 "*GUID*"。

</dd> <dt>

**NameFormat**
</dt> <dd> <dl> <dt>

資料類型： **uint16**
</dt> <dt>

存取類型：唯讀
</dt> </dl>

這個屬性繼承自 [**CIM \_ StorageExtent**](/windows/desktop/CIMWin32Prov/cim-storageextent)，而且一律設定為0。

</dd> <dt>

**NameNamespace**
</dt> <dd> <dl> <dt>

資料類型： **uint16**
</dt> <dt>

存取類型：唯讀
</dt> </dl>

這個屬性繼承自 [**CIM \_ StorageExtent**](/windows/desktop/CIMWin32Prov/cim-storageextent)，而且一律設定為0。

</dd> <dt>

**NoSinglePointOfFailure**
</dt> <dd> <dl> <dt>

資料類型： **布林值**
</dt> <dt>

存取類型：唯讀
</dt> </dl>

如果不存在單一失敗點，**則為 True** 。 這個屬性繼承自 [**CIM \_ StorageExtent**](/windows/desktop/CIMWin32Prov/cim-storageextent)，一律設為 **False**。

</dd> <dt>

**NumberOfBlocks**
</dt> <dd> <dl> <dt>

資料類型： **uint64**
</dt> <dt>

存取類型：唯讀
</dt> </dl>

計算值，表示除以 **區塊** 的總記憶體量。 這個屬性繼承自 [**CIM \_ StorageExtent**](/windows/desktop/CIMWin32Prov/cim-storageextent)。

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

當 **EnabledState** 屬性設定為 1 (其他) 時，元素的啟用或停用狀態。 當 **EnabledState** 是1以外的任何值時，這個屬性必須設定為 **Null** 。 這個屬性繼承自 [**CIM \_ EnabledLogicalElement**](/previous-versions//cc136818(v=vs.85))，而且一律設定為 **Null**。

</dd> <dt>

**OtherErrorDescription**
</dt> <dd> <dl> <dt>

資料類型： **字串**
</dt> <dt>

存取類型：唯讀
</dt> </dl>

這個屬性繼承自 [**CIM \_ 記憶體**](/windows/desktop/CIMWin32Prov/cim-memory)，但未使用。

</dd> <dt>

**OtherIdentifyingInfo**
</dt> <dd> <dl> <dt>

資料類型： **字串** 陣列
</dt> <dt>

存取類型：唯讀
</dt> </dl>

這個屬性會繼承自 [**CIM \_ LogicalDevice**](/windows/desktop/CIMWin32Prov/cim-logicaldevice)，而且會設定為 **Null**。

</dd> <dt>

**OtherNameFormat**
</dt> <dd> <dl> <dt>

資料類型： **字串**
</dt> <dt>

存取類型：唯讀
</dt> </dl>

當 **NameFormat** 屬性包含值 1 (其他 ") 時， **Name** 屬性的命名空間。 這個屬性繼承自 [**CIM \_ StorageExtent**](/windows/desktop/CIMWin32Prov/cim-storageextent)，而且一律設定為 **Null**。

</dd> <dt>

**OtherNameNamespace**
</dt> <dd> <dl> <dt>

資料類型： **字串**
</dt> <dt>

存取類型：唯讀
</dt> </dl>

當 **NameNamespace** 屬性包含值 1 (其他) 時， **Name** 屬性的命名空間。 這個屬性繼承自 [**CIM \_ StorageExtent**](/windows/desktop/CIMWin32Prov/cim-storageextent)，而且一律設定為 **Null**。

</dd> <dt>

**PackageRedundancy**
</dt> <dd> <dl> <dt>

資料類型： **uint16**
</dt> <dt>

存取類型：唯讀
</dt> </dl>

目前無法在不遺失資料的情況下失敗的實體封裝數目。 這個屬性繼承自 [**CIM \_ StorageExtent**](/windows/desktop/CIMWin32Prov/cim-storageextent)，而且一律設定為0。

</dd> <dt>

**PowerManagementCapabilities**
</dt> <dd> <dl> <dt>

資料類型： **uint16** 陣列
</dt> <dt>

存取類型：唯讀
</dt> </dl>

這個屬性繼承自 [**CIM \_ LogicalDevice**](/windows/desktop/CIMWin32Prov/cim-logicaldevice)，但不會使用它。

</dd> <dt>

**PowerManagementSupported**
</dt> <dd> <dl> <dt>

資料類型： **布林值**
</dt> <dt>

存取類型：唯讀
</dt> </dl>

這個屬性繼承自 [**CIM \_ LogicalDevice**](/windows/desktop/CIMWin32Prov/cim-logicaldevice)，但不會使用它。

</dd> <dt>

**PowerOnHours**
</dt> <dd> <dl> <dt>

資料類型： **uint64**
</dt> <dt>

存取類型：唯讀
</dt> </dl>

這個屬性繼承自 [**CIM \_ LogicalDevice**](/windows/desktop/CIMWin32Prov/cim-logicaldevice)，但不會使用它。

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

**原始**
</dt> <dd> <dl> <dt>

資料類型： **布林值**
</dt> <dt>

存取類型：唯讀
</dt> </dl>

如果包含的系統沒有建立或刪除此操作專案的能力，則 **為 True** 。 這個屬性繼承自 [**CIM \_ StorageExtent**](/windows/desktop/CIMWin32Prov/cim-storageextent)。

</dd> <dt>

**目的**
</dt> <dd> <dl> <dt>

資料類型： **字串**
</dt> <dt>

存取類型：唯讀
</dt> </dl>

描述媒體及其用途的字串。 這個屬性繼承自 [**CIM \_ StorageExtent**](/windows/desktop/CIMWin32Prov/cim-storageextent)，而且一律設定為「系統記憶體」。

</dd> <dt>

**RequestedState**
</dt> <dd> <dl> <dt>

資料類型： **uint16**
</dt> <dt>

存取類型：唯讀
</dt> </dl>

上次要求或預期的專案狀態。 元素的實際狀態是由 **EnabledState** 表示。 這個屬性是用來比較最後一個要求和目前啟用或停用的狀態。 特定的 [**CIM \_ EnabledLogicalElement**](/previous-versions//cc136818(v=vs.85)) 實例可能不支援 **RequestStateChange** 方法。 如果發生這種情況，則會使用值 12 (不適用) 。 這個屬性繼承自 **CIM \_ EnabledLogicalElement**。

</dd> <dt>

**SequentialAccess**
</dt> <dd> <dl> <dt>

資料類型： **布林值**
</dt> <dt>

存取類型：唯讀
</dt> </dl>

如果媒體存取裝置依序存取儲存體，則 **為 True** 。 磁帶磁碟分割是依序存取的儲存範圍範例。 儲存體磁片區、磁碟分割和邏輯磁片代表隨機存取的範圍。 這個屬性繼承自 [**CIM \_ StorageExtent**](/windows/desktop/CIMWin32Prov/cim-storageextent)，一律設為 **False**。

</dd> <dt>

**StartingAddress**
</dt> <dd> <dl> <dt>

資料類型： **uint64**
</dt> <dt>

存取類型：唯讀
</dt> </dl>

由應用程式或作業系統參考，且由記憶體控制器針對這個記憶體物件所對應的起始位址。 這個屬性繼承自 [**CIM \_ 記憶體**](/windows/desktop/CIMWin32Prov/cim-memory)，一律設為0。

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

**StatusInfo**
</dt> <dd> <dl> <dt>

資料類型： **uint16**
</dt> <dt>

存取類型：唯讀
</dt> </dl>

這個屬性繼承自 [**CIM \_ LogicalDevice**](/windows/desktop/CIMWin32Prov/cim-logicaldevice)，但不會使用它。

</dd> <dt>

**SystemCreationClassName**
</dt> <dd> <dl> <dt>

資料類型： **字串**
</dt> <dt>

存取類型：唯讀
</dt> </dl>

範圍系統的建立類別名稱。 這個屬性繼承自 [**CIM \_ LogicalDevice**](/windows/desktop/CIMWin32Prov/cim-logicaldevice)。

</dd> <dt>

**SystemLevelAddress**
</dt> <dd> <dl> <dt>

資料類型： **布林值**
</dt> <dt>

存取類型：唯讀
</dt> </dl>

這個屬性繼承自 [**CIM \_ 記憶體**](/windows/desktop/CIMWin32Prov/cim-memory)，但未使用。

</dd> <dt>

**SystemName**
</dt> <dd> <dl> <dt>

資料類型： **字串**
</dt> <dt>

存取類型：唯讀
</dt> </dl>

範圍虛擬機器的唯一識別碼。 這個屬性繼承自 [**CIM \_ LogicalDevice**](/windows/desktop/CIMWin32Prov/cim-logicaldevice)。

</dd> <dt>

**TimeOfLastStateChange**
</dt> <dd> <dl> <dt>

資料類型： **datetime**
</dt> <dt>

存取類型：唯讀
</dt> </dl>

專案的已啟用狀態上次變更的日期或時間。 這個屬性繼承自 [**CIM \_ EnabledLogicalElement**](/previous-versions//cc136818(v=vs.85))，而且一律設定為 "Null"。

</dd> <dt>

**TotalPowerOnHours**
</dt> <dd> <dl> <dt>

資料類型： **uint64**
</dt> <dt>

存取類型：唯讀
</dt> </dl>

這個屬性繼承自 [**CIM \_ LogicalDevice**](/windows/desktop/CIMWin32Prov/cim-logicaldevice)，但不會使用它。

</dd> <dt>

**TransitioningToState**
</dt> <dd> <dl> <dt>

資料類型： **uint16**
</dt> <dt>

存取類型：唯讀
</dt> </dl>

指出實例正在轉換的目標狀態。 這個屬性繼承自 [**CIM \_ EnabledLogicalElement**](/previous-versions//cc136818(v=vs.85))。

</dd> <dt>

**揮發 性**
</dt> <dd> <dl> <dt>

資料類型： **布林值**
</dt> <dt>

存取類型：唯讀
</dt> </dl>

指出記憶體是否為 volatile。 這個屬性繼承自 [**CIM \_ 記憶體**](/windows/desktop/CIMWin32Prov/cim-memory)，一律設定為 **True**。

</dd> </dl>

## <a name="remarks"></a>備註

**Msvm \_ 記憶體** 類別的存取權可能受 UAC 篩選所限制。 如需詳細資訊，請參閱 [使用者帳戶控制和 WMI](/windows/desktop/WmiSdk/user-account-control-and-wmi)。

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

[**CIM \_ 記憶體**](cim-memory.md)
</dt> <dt>

[**CIM \_ 記憶體**](/windows/desktop/CIMWin32Prov/cim-memory)
</dt> <dt>

[記憶體類別](memory-classes.md)
</dt> </dl>

 

