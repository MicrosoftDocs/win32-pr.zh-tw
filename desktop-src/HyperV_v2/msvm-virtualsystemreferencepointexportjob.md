---
description: 此類別代表虛擬系統參考點匯出作業工作。
ms.assetid: 3d8e117c-4863-441a-9264-c33f05fbc5ef
title: Msvm_VirtualSystemReferencePointExportJob 類別
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Msvm_VirtualSystemReferencePointExportJob
- Msvm_VirtualSystemReferencePointExportJob.Cancellable
- Msvm_VirtualSystemReferencePointExportJob.ErrorSummaryDescription
- Msvm_VirtualSystemReferencePointExportJob.ExportDirectory
- Msvm_VirtualSystemReferencePointExportJob.VirtualMachineId
- Msvm_VirtualSystemReferencePointExportJob.ReferencePointId
- Msvm_VirtualSystemReferencePointExportJob.BaseReferencePointId
- Msvm_VirtualSystemReferencePointExportJob.ExportedDisks
- Msvm_VirtualSystemReferencePointExportJob.ExportedLogFilePaths
- Msvm_VirtualSystemReferencePointExportJob.ExportedConfigFilePath
- Msvm_VirtualSystemReferencePointExportJob.ExportedRuntimeFilePath
- Msvm_VirtualSystemReferencePointExportJob.ExportedGuestStateFilePath
api_type:
- DllExport
api_location:
- vmms.exe
ms.openlocfilehash: 04b5d8f27efae4817062917541af9bb488cec32c
ms.sourcegitcommit: c16214e53680dc71d1c07111b51f72b82a4512d8
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 03/03/2021
ms.locfileid: "104514296"
---
# <a name="msvm_virtualsystemreferencepointexportjob-class"></a>Msvm \_ VirtualSystemReferencePointExportJob 類別

此類別代表虛擬系統參考點匯出作業工作。

下列語法已經過受管理物件格式 (MOF) 程式碼簡化，並包含所有已繼承的屬性。

## <a name="syntax"></a>語法

``` syntax
[Dynamic, Provider("VmmsWmiInstanceAndMethodProvider"), AMENDMENT]
class Msvm_VirtualSystemReferencePointExportJob : CIM_ConcreteJob
{
  boolean Cancellable;
  string  ErrorSummaryDescription;
  string  ExportDirectory;
  string  VirtualMachineId;
  string  ReferencePointId;
  string  BaseReferencePointId;
  string  ExportedDisks[];
  string  ExportedLogFilePaths[];
  string  ExportedConfigFilePath;
  string  ExportedRuntimeFilePath;
  string  ExportedGuestStateFilePath;
};
```

## <a name="members"></a>成員

**Msvm \_ VirtualSystemReferencePointExportJob** 類別具有下列類型的成員：

-   [方法](#methods)
-   [屬性](#properties)

### <a name="methods"></a>方法

**Msvm \_ VirtualSystemReferencePointExportJob** 類別具有這些方法。



| 方法                                                                                     | 描述                                        |
|:-------------------------------------------------------------------------------------------|:---------------------------------------------------|
| [**GetError**](msvm-virtualsystemreferencepointexportjob-geterror.md)                     | 捕獲錯誤。<br/>                    |
| [**GetErrorEx**](msvm-virtualsystemreferencepointexportjob-geterrorex.md)                 | 抓取其他錯誤資訊。<br/> |
| [**RequestStateChange**](msvm-virtualsystemreferencepointexportjob-requeststatechange.md) | 要求狀態變更。<br/>                |



 

### <a name="properties"></a>屬性

**Msvm \_ VirtualSystemReferencePointExportJob** 類別具有這些屬性。

<dl> <dt>

**BaseReferencePointId**
</dt> <dd> <dl> <dt>

資料類型： **字串**
</dt> <dt>

存取類型：唯讀
</dt> </dl>

在匯出作業中當做基底使用之參考點的 GUID。

</dd> <dt>

**可取消**
</dt> <dd> <dl> <dt>

資料類型： **布林值**
</dt> <dt>

存取類型：唯讀
</dt> </dl>

指出是否可以取消作業。 這個屬性的值不保證取消作業的要求將會成功。

</dd> <dt>

**ErrorSummaryDescription**
</dt> <dd> <dl> <dt>

資料類型： **字串**
</dt> <dt>

存取類型：唯讀
</dt> <dt>

限定詞： [**ModelCorrespondence**](/windows/desktop/WmiSdk/standard-qualifiers) ( 「[**CIM \_ 作業**](cim-job.md)」。**ErrorCode**") 
</dt> </dl>

包含錯誤摘要描述。

</dd> <dt>

**ExportDirectory**
</dt> <dd> <dl> <dt>

資料類型： **字串**
</dt> <dt>

存取類型：唯讀
</dt> </dl>

匯出位置。

</dd> <dt>

**ExportedConfigFilePath**
</dt> <dd> <dl> <dt>

資料類型： **字串**
</dt> <dt>

存取類型：唯讀
</dt> </dl>

匯出設定檔案的路徑。

</dd> <dt>

**ExportedDisks**
</dt> <dd> <dl> <dt>

資料類型： **字串** 陣列
</dt> <dt>

存取類型：唯讀
</dt> </dl>

已匯出記錄檔之虛擬磁片的實例識別碼。

</dd> <dt>

**ExportedGuestStateFilePath**
</dt> <dd> <dl> <dt>

資料類型： **字串**
</dt> <dt>

存取類型：唯讀
</dt> </dl>

匯出的來賓狀態檔案的路徑。

> [!Note]  
> 在 Windows 10 1709 版中新增。

 

</dd> <dt>

**ExportedLogFilePaths**
</dt> <dd> <dl> <dt>

資料類型： **字串** 陣列
</dt> <dt>

存取類型：唯讀
</dt> </dl>

已匯出之記錄檔的路徑。

</dd> <dt>

**ExportedRuntimeFilePath**
</dt> <dd> <dl> <dt>

資料類型： **字串**
</dt> <dt>

存取類型：唯讀
</dt> </dl>

匯出之執行時間狀態檔案的路徑。

</dd> <dt>

**ReferencePointId**
</dt> <dd> <dl> <dt>

資料類型： **字串**
</dt> <dt>

存取類型：唯讀
</dt> </dl>

匯出之參考點的 GUID。

</dd> <dt>

**VirtualMachineId**
</dt> <dd> <dl> <dt>

資料類型： **字串**
</dt> <dt>

存取類型：唯讀
</dt> </dl>

已匯出記錄檔之虛擬機器的 GUID。

</dd> </dl>

## <a name="requirements"></a>規格需求



| 需求 | 值 |
|-------------------------------------|---------------------------------------------------------------------------------------------------------|
| 最低支援的用戶端<br/> | Windows 10， \[ 僅限1703版桌面應用程式\]<br/>                                               |
| 最低支援的伺服器<br/> | Windows Server 2016<br/>                                                                          |
| 命名空間<br/>                | 根 \\ 虛擬化 \\ v2<br/>                                                                     |
| MOF<br/>                      | <dl> <dt>WindowsVirtualization。</dt> </dl> |
| DLL<br/>                      | <dl> <dt>Vmms.exe</dt> </dl>                     |



## <a name="see-also"></a>另請參閱

<dl> <dt>

[**CIM \_ ConcreteJob**](cim-concretejob.md)
</dt> </dl>

 

