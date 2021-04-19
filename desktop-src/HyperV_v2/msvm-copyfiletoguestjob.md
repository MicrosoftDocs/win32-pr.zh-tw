---
description: 代表來賓檔案服務作業。
ms.assetid: 3750707e-e8c8-4188-aed8-1a394d142140
title: Msvm_CopyFileToGuestJob 類別
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Msvm_CopyFileToGuestJob
- Msvm_CopyFileToGuestJob.StartService
- Msvm_CopyFileToGuestJob.StopService
- Msvm_CopyFileToGuestJob.Caption
- Msvm_CopyFileToGuestJob.CreationClassName
- Msvm_CopyFileToGuestJob.Description
- Msvm_CopyFileToGuestJob.InstallDate
- Msvm_CopyFileToGuestJob.Name
- Msvm_CopyFileToGuestJob.Started
- Msvm_CopyFileToGuestJob.StartMode
- Msvm_CopyFileToGuestJob.Status
- Msvm_CopyFileToGuestJob.SystemCreationClassName
- Msvm_CopyFileToGuestJob.SystemName
- Msvm_CopyFileToGuestJob.CopyFileToGuestSettingData
- Msvm_CopyFileToGuestJob.Cancellable
- Msvm_CopyFileToGuestJob.ErrorSummaryDescription
- Msvm_CopyFileToGuestJob.VirtualSystemName
api_type:
- DllExport
api_location:
- vmms.exe
ms.openlocfilehash: 57e27b4ba610eea4559f3b045b2d823661cf4cc9
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/08/2021
ms.locfileid: "106990318"
---
# <a name="msvm_copyfiletoguestjob-class"></a>Msvm \_ CopyFileToGuestJob 類別

代表來賓檔案服務作業。 這個類別衍生自 [**Msvm \_ GuestFileService**](msvm-guestfileservice.md)。

下列語法是簡化自 MOF 程式碼，且包含所有繼承的屬性。

## <a name="syntax"></a>語法

``` syntax
[Dynamic, Provider("VmmsWmiInstanceAndMethodProvider"), AMENDMENT]
class Msvm_CopyFileToGuestJob : CIM_ConcreteJob
{
  string   Caption;
  string   CreationClassName;
  string   Description;
  datetime InstallDate;
  string   Name;
  boolean  Started;
  string   StartMode;
  string   Status;
  string   SystemCreationClassName;
  string   SystemName;
  string   CopyFileToGuestSettingData[];
  boolean  Cancellable;
  string   ErrorSummaryDescription;
  string   VirtualSystemName;
};
```

## <a name="members"></a>成員

**Msvm \_ CopyFileToGuestJob** 類別具有下列類型的成員：

-   [方法](#methods)
-   [屬性](#properties)

### <a name="methods"></a>方法

**Msvm \_ CopyFileToGuestJob** 類別具有這些方法。



| 方法                                                                   | 描述                                                           |
|:-------------------------------------------------------------------------|:----------------------------------------------------------------------|
| [**CopyFilesToGuest**](copyfilestoguest-msvm-guestfileservice.md)       | 將檔案從 Hyper-v 主機複製到虛擬機器。<br/> |
| [**GetError**](geterror-msvm-copyfiletoguestjob.md)                     | 捕獲作業的錯誤物件。<br/>                    |
| [**GetErrorEx**](geterrorex-msvm-copyfiletoguestjob.md)                 | 捕獲作業的錯誤物件。<br/>                   |
| [**RequestStateChange**](requeststatechange-msvm-copyfiletoguestjob.md) | 變更作業的狀態。<br/>                              |
| **StartService**                                                         | 不支援這個方法。<br/>                              |
| **StopService**                                                          | 不支援這個方法。<br/>                              |



 

### <a name="properties"></a>屬性

**Msvm \_ CopyFileToGuestJob** 類別具有這些屬性。

<dl> <dt>

**可取消**
</dt> <dd> <dl> <dt>

資料類型： **布林值**
</dt> <dt>

存取類型：唯讀
</dt> </dl>

指出是否可以取消作業。 這個屬性的值不保證取消作業的要求將會成功。 若 **為 TRUE**，則工作可以取消;否則 **為 FALSE**。

</dd> <dt>

**標題**
</dt> <dd> <dl> <dt>

資料類型： **字串**
</dt> <dt>

存取類型：唯讀
</dt> </dl>

物件的簡短文字描述。 這個屬性繼承自 [**CIM \_ ManagedSystemElement**](/windows/desktop/CIMWin32Prov/cim-managedsystemelement)。

</dd> <dt>

**CopyFileToGuestSettingData**
</dt> <dd> <dl> <dt>

資料類型： **字串** 陣列
</dt> <dt>

存取類型：唯讀
</dt> </dl>

設定用來複製檔案的資料。

</dd> <dt>

**CreationClassName**
</dt> <dd> <dl> <dt>

資料類型： **字串**
</dt> <dt>

存取類型：唯讀
</dt> </dl>

建立實例時所使用之類別或子類別的名稱。 搭配類別的其他索引鍵屬性使用時，此屬性可讓類別和其子類別的所有實例都能唯一識別。

</dd> <dt>

**說明**
</dt> <dd> <dl> <dt>

資料類型： **字串**
</dt> <dt>

存取類型：唯讀
</dt> </dl>

物件的文字描述。 這個屬性繼承自 [**CIM \_ ManagedSystemElement**](/windows/desktop/CIMWin32Prov/cim-managedsystemelement)。

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

**InstallDate**
</dt> <dd> <dl> <dt>

資料類型： **datetime**
</dt> <dt>

存取類型：唯讀
</dt> </dl>

物件的安裝日期和時間。 這個屬性不需要值來表示已安裝物件。 這個屬性繼承自 [**CIM \_ ManagedSystemElement**](/windows/desktop/CIMWin32Prov/cim-managedsystemelement)。

</dd> <dt>

**名稱**
</dt> <dd> <dl> <dt>

資料類型： **字串**
</dt> <dt>

存取類型：唯讀
</dt> </dl>

服務的唯一識別碼，也會提供所管理功能的指示。 如需功能的詳細資訊，請參閱物件的 **Description** 屬性。 這個屬性繼承自 [**CIM \_ ManagedSystemElement**](/windows/desktop/CIMWin32Prov/cim-managedsystemelement)。

</dd> <dt>

**已開始**
</dt> <dd> <dl> <dt>

資料類型： **布林值**
</dt> <dt>

存取類型：唯讀
</dt> </dl>

若 **為 TRUE**，表示服務已啟動。

</dd> <dt>

**StartMode**
</dt> <dd> <dl> <dt>

資料類型： **字串**
</dt> <dt>

存取類型：唯讀
</dt> </dl>

指出服務是否自動啟動 (例如，作業系統) ，或只在要求時啟動。

包括下列值：

<dl><span id="Automatic"></span><span id="automatic"></span><span id="AUTOMATIC"></span><dt>

**自動**
</dt><span id="Manual"></span><span id="manual"></span><span id="MANUAL"></span><dt>

**》**
</dt> </dl>

</dd> <dt>

**狀態**
</dt> <dd> <dl> <dt>

資料類型： **字串**
</dt> <dt>

存取類型：唯讀
</dt> </dl>

物件的目前狀態。 這個屬性繼承自 [**CIM \_ ManagedSystemElement**](/windows/desktop/CIMWin32Prov/cim-managedsystemelement)。

包括下列值：

<dl><span id="OK"></span><span id="ok"></span><dt>

**正常**
</dt><span id="Error"></span><span id="error"></span><span id="ERROR"></span><dt>

**錯誤**
</dt><span id="Degraded"></span><span id="degraded"></span><span id="DEGRADED"></span><dt>

**降級**
</dt><span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span><dt>

**不明**
</dt><span id="Pred_Fail"></span><span id="pred_fail"></span><span id="PRED_FAIL"></span><dt>

**「Pred 失敗」**
</dt><span id="Starting"></span><span id="starting"></span><span id="STARTING"></span><dt>

**入門**
</dt><span id="Stopping"></span><span id="stopping"></span><span id="STOPPING"></span><dt>

**從而**
</dt><span id="Service"></span><span id="service"></span><span id="SERVICE"></span><dt>

**維護**
</dt><span id="Stressed"></span><span id="stressed"></span><span id="STRESSED"></span><dt>

**強調**
</dt><span id="NonRecover"></span><span id="nonrecover"></span><span id="NONRECOVER"></span><dt>

**"NonRecover"**
</dt><span id="No_Contact"></span><span id="no_contact"></span><span id="NO_CONTACT"></span><dt>

**「無連絡人」**
</dt><span id="Lost_Comm"></span><span id="lost_comm"></span><span id="LOST_COMM"></span><dt>

**「遺失通訊」**
</dt> </dl>

</dd> <dt>

**SystemCreationClassName**
</dt> <dd> <dl> <dt>

資料類型： **字串**
</dt> <dt>

存取類型：唯讀
</dt> </dl>

設定系統建立類別名稱的範圍。

</dd> <dt>

**SystemName**
</dt> <dd> <dl> <dt>

資料類型： **字串**
</dt> <dt>

存取類型：唯讀
</dt> </dl>

裝載服務的系統名稱。

</dd> <dt>

**VirtualSystemName**
</dt> <dd> <dl> <dt>

資料類型： **字串**
</dt> <dt>

存取類型：唯讀
</dt> </dl>

受影響之虛擬系統的 GUID。

</dd> </dl>

## <a name="requirements"></a>規格需求



| 需求 | 值 |
|-------------------------------------|---------------------------------------------------------------------------------------------------------|
| 最低支援的用戶端<br/> | \[僅 Windows 8.1 桌面應用程式\]<br/>                                                            |
| 最低支援的伺服器<br/> | 僅限 Windows Server 2012 R2 \[ desktop 應用程式\]<br/>                                                 |
| 命名空間<br/>                | 根 \\ 虛擬化 \\ V2<br/>                                                                     |
| MOF<br/>                      | <dl> <dt>WindowsVirtualization。</dt> </dl> |
| DLL<br/>                      | <dl> <dt>Vmms.exe</dt> </dl>                     |



## <a name="see-also"></a>另請參閱

<dl> <dt>

[**CIM \_ ConcreteJob**](cim-concretejob.md)
</dt> <dt>

[**Msvm \_ GuestFileService**](msvm-guestfileservice.md)
</dt> <dt>

[**Msvm \_ GuestService**](msvm-guestservice.md)
</dt> </dl>

 

