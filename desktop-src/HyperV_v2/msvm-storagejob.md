---
description: 代表 Microsoft Hyper-V 映射管理服務所建立的儲存體作業工作。
ms.assetid: a1517c1f-7fb6-4203-a5ec-2ecdfcbc4e8c
title: Msvm_StorageJob 類別
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Msvm_StorageJob
- Msvm_StorageJob.KillJob
- Msvm_StorageJob.InstanceID
- Msvm_StorageJob.Caption
- Msvm_StorageJob.Description
- Msvm_StorageJob.ElementName
- Msvm_StorageJob.InstallDate
- Msvm_StorageJob.Name
- Msvm_StorageJob.OperationalStatus
- Msvm_StorageJob.StatusDescriptions
- Msvm_StorageJob.Status
- Msvm_StorageJob.HealthState
- Msvm_StorageJob.CommunicationStatus
- Msvm_StorageJob.DetailedStatus
- Msvm_StorageJob.OperatingStatus
- Msvm_StorageJob.PrimaryStatus
- Msvm_StorageJob.JobStatus
- Msvm_StorageJob.TimeSubmitted
- Msvm_StorageJob.ScheduledStartTime
- Msvm_StorageJob.StartTime
- Msvm_StorageJob.ElapsedTime
- Msvm_StorageJob.JobRunTimes
- Msvm_StorageJob.RunMonth
- Msvm_StorageJob.RunDay
- Msvm_StorageJob.RunDayOfWeek
- Msvm_StorageJob.RunStartInterval
- Msvm_StorageJob.LocalOrUtcTime
- Msvm_StorageJob.UntilTime
- Msvm_StorageJob.Notify
- Msvm_StorageJob.Owner
- Msvm_StorageJob.Priority
- Msvm_StorageJob.PercentComplete
- Msvm_StorageJob.DeleteOnCompletion
- Msvm_StorageJob.ErrorCode
- Msvm_StorageJob.ErrorDescription
- Msvm_StorageJob.ErrorSummaryDescription
- Msvm_StorageJob.RecoveryAction
- Msvm_StorageJob.OtherRecoveryAction
- Msvm_StorageJob.JobState
- Msvm_StorageJob.TimeOfLastStateChange
- Msvm_StorageJob.TimeBeforeRemoval
- Msvm_StorageJob.Cancellable
- Msvm_StorageJob.Child
- Msvm_StorageJob.JobCompletionStatusCode
- Msvm_StorageJob.Parent
- Msvm_StorageJob.JobType
api_type:
- DllExport
api_location:
- vmms.exe
ms.openlocfilehash: 3014cb9a8201d7baceaf39bb760b17c33844abeb
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/08/2021
ms.locfileid: "103852967"
---
# <a name="msvm_storagejob-class"></a>Msvm \_ get-storagejob 類別

代表 Microsoft Hyper-V 映射管理服務所建立的儲存體作業工作。

下列語法已簡化受控物件格式 (MOF) 程式碼，並且包含所有繼承的屬性。

## <a name="syntax"></a>語法

``` syntax
[Dynamic, Provider("VmmsWmiInstanceAndMethodProvider"), AMENDMENT]
class Msvm_StorageJob : CIM_ConcreteJob
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
  uint16   HealthState = 5;
  uint16   CommunicationStatus;
  uint16   DetailedStatus;
  uint16   OperatingStatus;
  uint16   PrimaryStatus;
  string   JobStatus;
  datetime TimeSubmitted;
  datetime ScheduledStartTime;
  datetime StartTime;
  datetime ElapsedTime;
  uint32   JobRunTimes;
  uint8    RunMonth;
  sint8    RunDay;
  sint8    RunDayOfWeek;
  datetime RunStartInterval;
  uint16   LocalOrUtcTime;
  datetime UntilTime;
  string   Notify;
  string   Owner;
  uint32   Priority;
  uint16   PercentComplete;
  boolean  DeleteOnCompletion;
  uint16   ErrorCode;
  string   ErrorDescription;
  string   ErrorSummaryDescription;
  uint16   RecoveryAction;
  string   OtherRecoveryAction;
  uint16   JobState;
  datetime TimeOfLastStateChange;
  datetime TimeBeforeRemoval = 00000000000500.000000:000";
  boolean  Cancellable;
  string   Child;
  UINT32   JobCompletionStatusCode;
  string   Parent;
  uint16   JobType;
};
```

## <a name="members"></a>成員

**Msvm \_ get-storagejob** 類別具有下列類型的成員：

-   [方法](#methods)
-   [屬性](#properties)

### <a name="methods"></a>方法

**Msvm \_ get-storagejob** 類別具有這些方法。



| 方法                                                           | 描述                                                                                                                                                                                                                                                                                                                |
|:-----------------------------------------------------------------|:---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [**GetError**](msvm-storagejob-geterror.md)                     | 捕獲描述作業失敗原因的錯誤。<br/>                                                                                                                                                                                                                                               |
| [**GetErrorEx**](geterrorex-msvm-storagejob.md)                 | 當作業正在執行或已終止但沒有錯誤時，此方法不會傳回 [**Msvm \_ 錯誤**](msvm-error.md) 實例。 但是，如果工作因為某些內部問題而失敗，或由於用戶端已終止作業，則會傳回一或多個 **Msvm \_ 錯誤** 實例。<br/> |
| **KillJob**                                                      | 不支援這個方法。<br/>                                                                                                                                                                                                                                                                                   |
| [**RequestStateChange**](msvm-storagejob-requeststatechange.md) | 要求狀態變更。<br/>                                                                                                                                                                                                                                                                                        |



 

### <a name="properties"></a>屬性

**Msvm \_ get-storagejob** 類別具有這些屬性。

<dl> <dt>

**可取消**
</dt> <dd> <dl> <dt>

資料類型： **布林值**
</dt> <dt>

存取類型：唯讀
</dt> </dl>

指出是否可以取消作業。 這個屬性的值不保證取消作業的要求將會成功。

</dd> <dt>

**標題**
</dt> <dd> <dl> <dt>

資料類型： **字串**
</dt> <dt>

存取類型：唯讀
</dt> </dl>

物件的簡短描述。 這個屬性繼承自 [**CIM \_ ManagedElement**](/previous-versions/windows/desktop/iscsitarg/cim-managedelement)。

</dd> <dt>

**子系**
</dt> <dd> <dl> <dt>

資料類型： **字串**
</dt> <dt>

存取類型：唯讀
</dt> </dl>

非同步作業失敗時，這個屬性會包含此作業所影響之 VHD 子系的完整路徑。

</dd> <dt>

**CommunicationStatus**
</dt> <dd> <dl> <dt>

資料類型： **uint16**
</dt> <dt>

存取類型：唯讀
</dt> </dl>

指出檢測與基礎受管理元素通訊的能力。 **Null** 值表示不會執行此屬性。 這個屬性繼承自 [**CIM \_ ManagedSystemElement**](/windows/desktop/CIMWin32Prov/cim-managedsystemelement)。

</dd> <dt>

**DeleteOnCompletion**
</dt> <dd> <dl> <dt>

資料類型： **布林值**
</dt> <dt>

存取類型：唯讀
</dt> </dl>

指定作業是否應該在完成時自動刪除。 這個屬性繼承自 [**CIM \_ 工作**](/windows/desktop/CIMWin32Prov/cim-job)。

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

**經過時間**
</dt> <dd> <dl> <dt>

資料類型： **datetime**
</dt> <dt>

存取類型：唯讀
</dt> </dl>

作業已執行的時間長度。 這個屬性繼承自 [**CIM \_ 工作**](/windows/desktop/CIMWin32Prov/cim-job)。

</dd> <dt>

**ElementName**
</dt> <dd> <dl> <dt>

資料類型： **字串**
</dt> <dt>

存取類型：唯讀
</dt> </dl>

物件的顯示名稱。 這個屬性繼承自 [**CIM \_ ManagedElement**](/previous-versions/windows/desktop/iscsitarg/cim-managedelement)。

</dd> <dt>

**ErrorCode**
</dt> <dd> <dl> <dt>

資料類型： **uint16**
</dt> <dt>

存取類型：唯讀
</dt> </dl>

特定廠商的錯誤碼。 如果作業已完成而沒有錯誤，則值必須設為零。 這個屬性繼承自 [**CIM \_ 工作**](/windows/desktop/CIMWin32Prov/cim-job)。

</dd> <dt>

**ErrorDescription**
</dt> <dd> <dl> <dt>

資料類型： **字串**
</dt> <dt>

存取類型：唯讀
</dt> </dl>

包含廠商錯誤描述的字串。 這個屬性繼承自 [**CIM \_ 工作**](/windows/desktop/CIMWin32Prov/cim-job)。

</dd> <dt>

**ErrorSummaryDescription**
</dt> <dd> <dl> <dt>

資料類型： **字串**
</dt> <dt>

存取類型：唯讀
</dt> <dt>

限定詞： [**ModelCorrespondence**](/windows/desktop/WmiSdk/standard-qualifiers) ( 「[**CIM \_ 作業**](cim-job.md)」。**ErrorCode**") 
</dt> </dl>

錯誤的摘要描述（如果有的話）。 這個屬性繼承自 [**CIM \_ 工作**](/windows/desktop/CIMWin32Prov/cim-job)。

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
</dt> </dl>

唯一識別此類別的實例。 這個屬性繼承自 [**CIM \_ ManagedElement**](/previous-versions/windows/desktop/iscsitarg/cim-managedelement)。

</dd> <dt>

**JobCompletionStatusCode**
</dt> <dd> <dl> <dt>

資料類型： **UINT32**
</dt> <dt>

存取類型：唯讀
</dt> </dl>

描述非同步作業完成狀態的 **HRESULT** 程式碼。

</dd> <dt>

**JobRunTimes**
</dt> <dd> <dl> <dt>

資料類型： **uint32**
</dt> <dt>

存取類型：唯讀
</dt> </dl>

作業應該執行的次數。 值為1表示作業不是週期性的，而任何非零值則表示作業將重複發生的次數限制。 零表示作業可以處理的次數沒有任何限制，但會在到達 **UntilTime** 之後終止，否則會以手動方式結束作業，以終止作業。 這個屬性繼承自 [**CIM \_ 工作**](/windows/desktop/CIMWin32Prov/cim-job)。

</dd> <dt>

**JobState**
</dt> <dd> <dl> <dt>

資料類型： **uint16**
</dt> <dt>

存取類型：唯讀
</dt> </dl>

作業的操作狀態。 它也可以指出這些狀態之間的轉換，例如，6 (關閉) 和 3 (啟動) 。 這個屬性繼承自 [**CIM \_ ConcreteJob**](/previous-versions//cc136808(v=vs.85))。



| 值                                                                                                                                                                                                                                                                     | 意義                                                                                                                                                                                                                                            |
|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span id="New"></span><span id="new"></span><span id="NEW"></span><dl> <dt>**新**</dt> <dt>2</dt> </dl>                                                               | 作業從未啟動。<br/>                                                                                                                                                                                                         |
| <span id="Starting"></span><span id="starting"></span><span id="STARTING"></span><dl> <dt>**開始**</dt> <dt>3</dt> </dl>                                           | 作業會從「新增」、「已暫停」或「服務」狀態移至「正在執行」狀態。<br/>                                                                                                                                            |
| <span id="Running"></span><span id="running"></span><span id="RUNNING"></span><dl> <dt>**正在**</dt>執行 <dt>4</dt> </dl>                                               | 工作正在執行。<br/>                                                                                                                                                                                                                     |
| <span id="Suspended"></span><span id="suspended"></span><span id="SUSPENDED"></span><dl> 已 <dt>**暫**</dt>止 <dt>5</dt> </dl>                                       | 作業已停止，但可以順暢的方式重新開機。<br/>                                                                                                                                                                       |
| <span id="Shutting_Down"></span><span id="shutting_down"></span><span id="SHUTTING_DOWN"></span><dl> 正在 <dt>**關閉**</dt> <dt>6</dt> </dl>                       | 作業正在移至「已完成」、「已終止」或「已終止」狀態。<br/>                                                                                                                                                                    |
| <span id="Completed"></span><span id="completed"></span><span id="COMPLETED"></span><dl> <dt>**完成**</dt> <dt>7</dt> </dl>                                       | 作業已正常完成。<br/>                                                                                                                                                                                                         |
| <span id="Terminated"></span><span id="terminated"></span><span id="TERMINATED"></span><dl> <dt>**終止**</dt> <dt>8</dt> </dl>                                   | 作業已由「終止」狀態變更要求停止。 作業和其所有基礎進程都已結束，而且只能以新的作業重新開機。 只有當工作為特定作業時，才需要重新開機作業。<br/> |
| <span id="Killed"></span><span id="killed"></span><span id="KILLED"></span><dl> 已 <dt>**終止**</dt> <dt>9</dt> </dl>                                                   | 作業已由「終止」狀態變更要求停止。 基礎進程可能仍在執行中，而且可能需要進行清除以釋出資源。<br/>                                                                            |
| <span id="Exception"></span><span id="exception"></span><span id="EXCEPTION"></span><dl> <dt>**例外**</dt>狀況 <dt>10</dt> </dl>                                      | 作業處於異常狀態，可能表示發生錯誤狀況。 工作的實際狀態可能會透過工作專屬的物件提供。<br/>                                                                           |
| <span id="Service"></span><span id="service"></span><span id="SERVICE"></span><dl> <dt>**服務**</dt> <dt>11</dt> </dl>                                              | 作業處於支援問題探索、解決或兩者的廠商特定狀態。<br/>                                                                                                                                          |
| <span id="DMTF_Reserved"></span><span id="dmtf_reserved"></span><span id="DMTF_RESERVED"></span><dl> <dt>**DMTF 保留**</dt>的 <dt>12 32767</dt> </dl>                | 保留的。<br/>                                                                                                                                                                                                                               |
| <span id="Vendor_Reserved_"></span><span id="vendor_reserved_"></span><span id="VENDOR_RESERVED_"></span><dl> <dt>**廠商保留**</dt>的 <dt>32768 65535</dt> </dl> | 保留的。<br/>                                                                                                                                                                                                                               |



 

</dd> <dt>

**JobStatus**
</dt> <dd> <dl> <dt>

資料類型： **字串**
</dt> <dt>

存取類型：唯讀
</dt> </dl>

表示作業狀態的字串。 這個屬性繼承自 [**CIM \_ 工作**](/windows/desktop/CIMWin32Prov/cim-job)。

</dd> <dt>

**JobType**
</dt> <dd> <dl> <dt>

資料類型： **uint16**
</dt> <dt>

存取類型：唯讀
</dt> </dl>

這個 **Msvm \_ get-storagejob** 實例所追蹤的非同步操作類型。

<dt>

<span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>

<span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>**未知** 的 (0) 


</dt> <dd></dd> <dt>

<span id="VHD_Creation"></span><span id="vhd_creation"></span><span id="VHD_CREATION"></span>

<span id="VHD_Creation"></span><span id="vhd_creation"></span><span id="VHD_CREATION"></span>**VHD 建立** (1) 


</dt> <dd>

建立虛擬硬碟 (VHD) 映射。

</dd> <dt>

<span id="Floppy_Creation"></span><span id="floppy_creation"></span><span id="FLOPPY_CREATION"></span>

<span id="Floppy_Creation"></span><span id="floppy_creation"></span><span id="FLOPPY_CREATION"></span> (2) 的 **軟碟建立**


</dt> <dd>

 (.VFD) 建立虛擬磁片映射。

</dd> <dt>

<span id="Compaction"></span><span id="compaction"></span><span id="COMPACTION"></span>

<span id="Compaction"></span><span id="compaction"></span><span id="COMPACTION"></span>**壓縮** (3) 


</dt> <dd>

壓縮 VHD 映射的大小。

</dd> <dt>

<span id="Expansion"></span><span id="expansion"></span><span id="EXPANSION"></span>

<span id="Expansion"></span><span id="expansion"></span><span id="EXPANSION"></span>**擴充** (4) 


</dt> <dd>

擴充 VHD 映射的大小。

</dd> <dt>

<span id="Merging"></span><span id="merging"></span><span id="MERGING"></span>

<span id="Merging"></span><span id="merging"></span><span id="MERGING"></span>**合併** (5) 


</dt> <dd>

將多個 VHD 映射合併成單一映射。

</dd> <dt>

<span id="Conversion"></span><span id="conversion"></span><span id="CONVERSION"></span>

<span id="Conversion"></span><span id="conversion"></span><span id="CONVERSION"></span>**轉換** (6) 


</dt> <dd>

轉換虛擬硬碟映射的類型。

</dd> <dt>

<span id="Loopback_Mount"></span><span id="loopback_mount"></span><span id="LOOPBACK_MOUNT"></span>

<span id="Loopback_Mount"></span><span id="loopback_mount"></span><span id="LOOPBACK_MOUNT"></span>**回送掛接** (7) 


</dt> <dd>

裝載父磁碟分割上的虛擬硬碟

</dd> <dt>

<span id="Get_VHD_Info"></span><span id="get_vhd_info"></span><span id="GET_VHD_INFO"></span>

<span id="Get_VHD_Info"></span><span id="get_vhd_info"></span><span id="GET_VHD_INFO"></span>**取得 VHD 資訊** (8) 


</dt> <dd>

在管理作業系統上掛接 VHD。

</dd> <dt>

<span id="Validate_VHD_Image"></span><span id="validate_vhd_image"></span><span id="VALIDATE_VHD_IMAGE"></span>

<span id="Validate_VHD_Image"></span><span id="validate_vhd_image"></span><span id="VALIDATE_VHD_IMAGE"></span> (9) **驗證 VHD 映射**


</dt> <dd></dd> </dl>

</dd> <dt>

**LocalOrUtcTime**
</dt> <dd> <dl> <dt>

資料類型： **uint16**
</dt> <dt>

存取類型：唯讀
</dt> </dl>

指出 **RunStartInterval** 和 **UntilTime** 屬性中所表示的時間是否代表當地時間或 UTC 時間。 這個屬性繼承自 [**CIM \_ 工作**](/windows/desktop/CIMWin32Prov/cim-job)。

<dl> <dt>

<span id="Local_Time"></span><span id="local_time"></span><span id="LOCAL_TIME"></span>**本地時間** (1) 
</dt> <dt>

<span id="UTC_Time_"></span><span id="utc_time_"></span><span id="UTC_TIME_"></span>**UTC 時間** (2 ) 
</dt> </dl>

</dd> <dt>

**名稱**
</dt> <dd> <dl> <dt>

資料類型： **字串**
</dt> <dt>

存取類型：唯讀
</dt> </dl>

已知物件的標籤。 這個屬性繼承自 [**CIM \_ ManagedSystemElement**](/windows/desktop/CIMWin32Prov/cim-managedsystemelement)。

</dd> <dt>

**通知**
</dt> <dd> <dl> <dt>

資料類型： **字串**
</dt> <dt>

存取類型：唯讀
</dt> </dl>

在作業完成或失敗時收到通知的使用者。 這個屬性繼承自 [**CIM \_ 工作**](/windows/desktop/CIMWin32Prov/cim-job)。

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

**OtherRecoveryAction**
</dt> <dd> <dl> <dt>

資料類型： **字串**
</dt> <dt>

存取類型：唯讀
</dt> </dl>

字串，描述當實例的 **RecoveryAction** 屬性為 1 (其他) 時的復原動作。 這個屬性繼承自 [**CIM \_ 工作**](/windows/desktop/CIMWin32Prov/cim-job)。

</dd> <dt>

**擁有者**
</dt> <dd> <dl> <dt>

資料類型： **字串**
</dt> <dt>

存取類型：唯讀
</dt> </dl>

提交作業的使用者。 這個屬性繼承自 [**CIM \_ 工作**](/windows/desktop/CIMWin32Prov/cim-job)。

</dd> <dt>

**父系**
</dt> <dd> <dl> <dt>

資料類型： **字串**
</dt> <dt>

存取類型：唯讀
</dt> </dl>

非同步作業失敗時，這個屬性會包含此作業所影響之 VHD 父系的檔案路徑。

</dd> <dt>

**PercentComplete**
</dt> <dd> <dl> <dt>

資料類型： **uint16**
</dt> <dt>

存取類型：唯讀
</dt> <dt>

限定詞： **MinValue** ( 0 ) ， **int32.maxvalue ( 100** ) ， **單位** ( "Percent" ) 
</dt> </dl>

作業的完成百分比。 這個屬性繼承自 [**CIM \_ 工作**](/windows/desktop/CIMWin32Prov/cim-job)。

</dd> <dt>

**PrimaryStatus**
</dt> <dd> <dl> <dt>

資料類型： **uint16**
</dt> <dt>

存取類型：唯讀
</dt> </dl>

提供高層級的狀態資訊。 這個屬性應該與 **DetailedStatus** 屬性一起使用，以提供元素和其子元件的高階和詳細健全狀況狀態。 **Null** 值表示不會執行此屬性。 這個屬性繼承自 [**CIM \_ ManagedSystemElement**](/windows/desktop/CIMWin32Prov/cim-managedsystemelement)。

</dd> <dt>

**優先順序**
</dt> <dd> <dl> <dt>

資料類型： **uint32**
</dt> <dt>

存取類型：唯讀
</dt> </dl>

作業執行的重要性。 這個屬性繼承自 [**CIM \_ 工作**](/windows/desktop/CIMWin32Prov/cim-job)。

</dd> <dt>

**RecoveryAction**
</dt> <dd> <dl> <dt>

資料類型： **uint16**
</dt> <dt>

存取類型：唯讀
</dt> </dl>

描述未成功執行的作業所要採取的復原動作。 這個屬性繼承自 [**CIM \_ 工作**](/windows/desktop/CIMWin32Prov/cim-job)。

<dl> <dt>

<span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>**未知** 的 (0) 
</dt> <dt>

<span id="Other"></span><span id="other"></span><span id="OTHER"></span>**其他** (1) 
</dt> <dt>

<span id="Do_Not_Continue"></span><span id="do_not_continue"></span><span id="DO_NOT_CONTINUE"></span>**請勿繼續** (2) 
</dt> <dt>

<span id="Continue_With_Next_Job"></span><span id="continue_with_next_job"></span><span id="CONTINUE_WITH_NEXT_JOB"></span>**繼續進行下一個工作** (3) 
</dt> <dt>

<span id="Re-run_Job"></span><span id="re-run_job"></span><span id="RE-RUN_JOB"></span> (4) **重新執行作業**
</dt> <dt>

<span id="Run_Recovery_Job_"></span><span id="run_recovery_job_"></span><span id="RUN_RECOVERY_JOB_"></span>**執行復原工作** (5 ) 
</dt> </dl>

</dd> <dt>

**RunDay**
</dt> <dd> <dl> <dt>

資料類型： **sint8**
</dt> <dt>

存取類型：唯讀
</dt> <dt>

限定詞： **MinValue** (-31 ) 、 **int32.maxvalue ( 31** ) 
</dt> </dl>

應處理作業之月份的日期。 根據 **RunDayOfWeek** 的值，此屬性有不同的解釋。

當 **RunDayOfWeek** 為0，而 **RunDay** 為正數時， **RunDay** 會定義處理作業的月份日期。 例如，如果 **RunDayOfWeek** 為0，而 **RunDay** 為12，則會在當月 <sup>的12天</sup> 處理工作。

當 **RunDayOfWeek** 為0，而 **RunDay** 為負數時， **RunDay** 會定義處理工作的當月最後一天之前的天數。  1表示當月最後一天，2表示當月最後一天之前的一天，依此類推。 例如，如果 **RunDayOfWeek** 是0，而 **RunDay** 是1，則會在當月的最後一天處理工作。

當 **RunDayOfWeek** 不是0時， **RunDayOfWeek** 是將處理作業的星期幾（相對於 **RunDay**）。 例如，如果 **RunDay** 為15，而 **RunDayOfWeek** 為 7 (+ 星期六) ，則工作會在每 <sup>月15日</sup> 的第一個星期六或之後處理。 如果 **RunDay** 為20，而 **RunDayOfWeek** 為 7 ( 星期六) ，則會在當月 <sup>的20天</sup> 前或之前的第一個星期六處理工作。 如果 **RunDay** 是1，而 **RunDayOfWeek** 是 1 ( 星期日) ，則會在當月的最後一個星期日處理工作。

這個屬性繼承自 [**CIM \_ 工作**](/windows/desktop/CIMWin32Prov/cim-job)。

</dd> <dt>

**RunDayOfWeek**
</dt> <dd> <dl> <dt>

資料類型： **sint8**
</dt> <dt>

存取類型：唯讀
</dt> </dl>

與 **RunDay** 搭配使用的正整數或負整數，表示處理作業的周中日或月中的日。 如需詳細資訊，請參閱 **RunDay** 屬性的描述。 這個屬性繼承自 [**CIM \_ 工作**](/windows/desktop/CIMWin32Prov/cim-job)。

<dl> <dt>

<span id="-Saturday"></span><span id="-saturday"></span><span id="-SATURDAY"></span>**-星期六** ( 7) 
</dt> <dt>

<span id="-Friday"></span><span id="-friday"></span><span id="-FRIDAY"></span>**-星期五** ( 6) 
</dt> <dt>

<span id="-Thursday"></span><span id="-thursday"></span><span id="-THURSDAY"></span>**-星期四** ( 5) 
</dt> <dt>

<span id="-Wednesday"></span><span id="-wednesday"></span><span id="-WEDNESDAY"></span>**-星期三** ( 4) 
</dt> <dt>

<span id="-Tuesday"></span><span id="-tuesday"></span><span id="-TUESDAY"></span>**-星期二** ( 3) 
</dt> <dt>

<span id="-Monday"></span><span id="-monday"></span><span id="-MONDAY"></span>**-星期一** ( 2) 
</dt> <dt>

<span id="-Sunday"></span><span id="-sunday"></span><span id="-SUNDAY"></span>**-星期日** ( 1) 
</dt> <dt>

<span id="ExactDayOfMonth"></span><span id="exactdayofmonth"></span><span id="EXACTDAYOFMONTH"></span>**ExactDayOfMonth** (0) 
</dt> <dt>

<span id="Sunday"></span><span id="sunday"></span><span id="SUNDAY"></span>**星期日** (1) 
</dt> <dt>

<span id="Monday"></span><span id="monday"></span><span id="MONDAY"></span>**星期一** (2) 
</dt> <dt>

<span id="Tuesday"></span><span id="tuesday"></span><span id="TUESDAY"></span>**星期二** (3) 
</dt> <dt>

<span id="Wednesday"></span><span id="wednesday"></span><span id="WEDNESDAY"></span>**星期三** (4) 
</dt> <dt>

<span id="Thursday"></span><span id="thursday"></span><span id="THURSDAY"></span>**星期四** (5) 
</dt> <dt>

<span id="Friday"></span><span id="friday"></span><span id="FRIDAY"></span>**星期五** (6) 
</dt> <dt>

<span id="Saturday_"></span><span id="saturday_"></span><span id="SATURDAY_"></span>**星期六** (7 ) 
</dt> </dl>

</dd> <dt>

**RunMonth**
</dt> <dd> <dl> <dt>

資料類型： **uint8**
</dt> <dt>

存取類型：唯讀
</dt> </dl>

應處理作業的月份。 這個屬性繼承自 [**CIM \_ 工作**](/windows/desktop/CIMWin32Prov/cim-job)。

<dl> <dt>

<span id="January"></span><span id="january"></span><span id="JANUARY"></span>**1 月** (0) 
</dt> <dt>

<span id="February"></span><span id="february"></span><span id="FEBRUARY"></span>**二月** (1) 
</dt> <dt>

<span id="March"></span><span id="march"></span><span id="MARCH"></span>**3 月** (2) 
</dt> <dt>

<span id="April"></span><span id="april"></span><span id="APRIL"></span>**四月** (3) 
</dt> <dt>

<span id="May"></span><span id="may"></span><span id="MAY"></span>**5 月** (4) 
</dt> <dt>

<span id="June"></span><span id="june"></span><span id="JUNE"></span>**6 月** (5) 
</dt> <dt>

<span id="July"></span><span id="july"></span><span id="JULY"></span>**7 月** (6) 
</dt> <dt>

<span id="August"></span><span id="august"></span><span id="AUGUST"></span>**8 月** (7) 
</dt> <dt>

<span id="September"></span><span id="september"></span><span id="SEPTEMBER"></span>**9 月** (8) 
</dt> <dt>

<span id="October"></span><span id="october"></span><span id="OCTOBER"></span>**10 月** (9) 
</dt> <dt>

<span id="November"></span><span id="november"></span><span id="NOVEMBER"></span>**11 月** (10) 
</dt> <dt>

<span id="December_"></span><span id="december_"></span><span id="DECEMBER_"></span>**12 月** (11 ) 
</dt> </dl>

</dd> <dt>

**RunStartInterval**
</dt> <dd> <dl> <dt>

資料類型： **datetime**
</dt> <dt>

存取類型：唯讀
</dt> </dl>

應處理作業的午夜之後的時間間隔。 這個屬性繼承自 [**CIM \_ 工作**](/windows/desktop/CIMWin32Prov/cim-job)。

</dd> <dt>

**ScheduledStartTime**
</dt> <dd> <dl> <dt>

資料類型： **datetime**
</dt> <dt>

存取類型：唯讀
</dt> </dl>

這個屬性繼承自 [**CIM \_ 工作**](/windows/desktop/CIMWin32Prov/cim-job)。

</dd> <dt>

**StartTime**
</dt> <dd> <dl> <dt>

資料類型： **datetime**
</dt> <dt>

存取類型：唯讀
</dt> </dl>

作業開始的時間。 這個屬性繼承自 [**CIM \_ 工作**](/windows/desktop/CIMWin32Prov/cim-job)。

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

**TimeBeforeRemoval**
</dt> <dd> <dl> <dt>

資料類型： **datetime**
</dt> <dt>

存取類型：唯讀
</dt> </dl>

作業完成執行後的保留時間（以分鐘為單位），這是在該執行中的成功或失敗。 無論 **DeleteOnCompletion** 屬性的值為何，此作業都必須保持存在一段時間。 預設為五分鐘。 這個屬性繼承自 [**CIM \_ ConcreteJob**](/previous-versions//cc136808(v=vs.85))，而且一律設定為00000000000500.000000：000。

</dd> <dt>

**TimeOfLastStateChange**
</dt> <dd> <dl> <dt>

資料類型： **datetime**
</dt> <dt>

存取類型：唯讀
</dt> </dl>

上次修改虛擬機器狀態的時間。 這個屬性繼承自 [**CIM \_ EnabledLogicalElement**](/previous-versions//cc136818(v=vs.85))。

</dd> <dt>

**TimeSubmitted**
</dt> <dd> <dl> <dt>

資料類型： **datetime**
</dt> <dt>

存取類型：唯讀
</dt> </dl>

提交作業的時間。 這個屬性繼承自 [**CIM \_ 工作**](/windows/desktop/CIMWin32Prov/cim-job)。

</dd> <dt>

**UntilTime**
</dt> <dd> <dl> <dt>

資料類型： **datetime**
</dt> <dt>

存取類型：唯讀
</dt> </dl>

作業無效或應該停止的時間。 這個屬性繼承自 [**CIM \_ 工作**](/windows/desktop/CIMWin32Prov/cim-job)。

</dd> </dl>

## <a name="remarks"></a>備註

存取 **Msvm \_ get-storagejob** 類別可能受 UAC 篩選所限制。 如需詳細資訊，請參閱 [使用者帳戶控制和 WMI](/windows/desktop/WmiSdk/user-account-control-and-wmi)。

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

[**CIM \_ ConcreteJob**](cim-concretejob.md)
</dt> <dt>

[**CIM \_ ConcreteJob**](/previous-versions//cc136808(v=vs.85))
</dt> <dt>

[儲存類別](storage-classes.md)
</dt> </dl>

 

