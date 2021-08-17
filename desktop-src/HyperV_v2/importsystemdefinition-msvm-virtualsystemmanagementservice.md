---
description: 根據指定的虛擬機器定義，建立新的規劃的電腦系統。
ms.assetid: 885d399f-5bcf-4f34-b2f1-582cbfcd7c10
title: Msvm_VirtualSystemManagementService 類別的 ImportSystemDefinition 方法
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Msvm_VirtualSystemManagementService.ImportSystemDefinition
api_type:
- COM
api_location:
- vmms.exe
ms.openlocfilehash: ee8dd5bb7d17684216b747717c0adf32011dafa543f05c91a0c1264da89caf2a
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/11/2021
ms.locfileid: "118149734"
---
# <a name="importsystemdefinition-method-of-the-msvm_virtualsystemmanagementservice-class"></a>Msvm VirtualSystemManagementService 類別的 ImportSystemDefinition 方法 \_

根據指定的虛擬機器定義，建立新的規劃的電腦系統。

## <a name="syntax"></a>語法


```mof
uint32 ImportSystemDefinition(
  [in]  string                         SystemDefinitionFile,
  [in]  string                         SnapshotFolder,
  [in]  boolean                        GenerateNewSystemIdentifier,
  [out] Msvm_PlannedComputerSystem REF ImportedSystem,
  [out] CIM_ConcreteJob            REF Job
);
```



## <a name="parameters"></a>參數

<dl> <dt>

*SystemDefinitionFile* \[在\]
</dt> <dd>

系統定義檔的完整路徑 (.xml 或 .exp) 代表要匯入的虛擬機器。 主機系統或虛擬化平臺不能使用定義檔。

</dd> <dt>

*SnapshotFolder* \[在\]
</dt> <dd>

可在其中找到此虛擬機器的快照集設定之資料夾的完整路徑。 系統會搜尋此資料夾，以找出虛擬機器定義所參考的任何快照集。 在此位置中找不到的任何參考快照集都必須使用 [**DestroySnapshot**](destroysnapshot-msvm-virtualsystemsnapshotservice.md) 方法來刪除，或在實現規劃的電腦系統之前使用 [**ImportSnapshotDefinitions**](importsnapshotdefinitions-msvm-virtualsystemmanagementservice.md) 方法匯入。

</dd> <dt>

*GenerateNewSystemIdentifier* \[在\]
</dt> <dd>

指出是否要重複使用虛擬機器的唯一識別碼。 如果此參數為 **True**，則會產生新的系統識別碼。 如果此參數為 **False**，則會使用現有的系統識別碼。

</dd> <dt>

*ImportedSystem* \[擴展\]
</dt> <dd>

如果作業同步完成，則為代表已匯入虛擬機器之 [**Msvm \_ PlannedComputerSystem**](msvm-plannedcomputersystem.md) 物件的參考。

</dd> <dt>

*作業* \[擴展\]
</dt> <dd>

如果作業是以非同步方式執行，這個方法會傳回4096，而此參數會包含衍生自 [**CIM \_ ConcreteJob**](/previous-versions//cc136808(v=vs.85))之物件的參考。

</dd> </dl>

## <a name="return-value"></a>傳回值

這個方法會傳回下列其中一個值。

<dl> <dt>

**已完成，沒有錯誤** (0) 
</dt> <dt>

**已檢查方法參數-工作已啟動** (4096) 
</dt> <dt>

**無法** (32768) 
</dt> <dt>

**拒絕存取** (32769) 
</dt> <dt>

**不支援** (32770) 
</dt> <dt>

**狀態未知** (32771) 
</dt> <dt>

**Timeout** (32772) 
</dt> <dt>

**不正確參數** (32773) 
</dt> <dt>

**系統正在使用中** (32774) 
</dt> <dt>

**此操作的狀態無效** (32775) 
</dt> <dt>

**不正確的資料類型** (32776) 
</dt> <dt>

**系統無法使用** (32777) 
</dt> <dt>

**記憶體不足** (32778) 
</dt> <dt>

**使用中的** 檔案 (32779) 
</dt> </dl>

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

[**Msvm \_ VirtualSystemManagementService**](msvm-virtualsystemmanagementservice.md)
</dt> </dl>

 

