---
description: 搜尋指定的資料夾中是否有任何與指定之規劃的電腦系統相關聯的快照集定義檔案，並針對此位置中的每個關聯定義檔，在規劃的電腦系統上建立新的快照集。
ms.assetid: d240c24b-f788-4ea9-b3bd-af1f75f4f460
title: Msvm_VirtualSystemManagementService 類別的 ImportSnapshotDefinitions 方法
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Msvm_VirtualSystemManagementService.ImportSnapshotDefinitions
api_type:
- COM
api_location:
- vmms.exe
ms.openlocfilehash: 9ebb36b030786ab88eab899190afcc7f3022286a
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/07/2021
ms.locfileid: "103848517"
---
# <a name="importsnapshotdefinitions-method-of-the-msvm_virtualsystemmanagementservice-class"></a>Msvm VirtualSystemManagementService 類別的 ImportSnapshotDefinitions 方法 \_

搜尋指定的資料夾中是否有任何與指定之規劃的電腦系統相關聯的快照集定義檔案，並針對此位置中的每個關聯定義檔，在規劃的電腦系統上建立新的快照集。

## <a name="syntax"></a>語法


```mof
uint32 ImportSnapshotDefinitions(
  [in]  Msvm_PlannedComputerSystem    REF PlannedSystem,
  [in]  string                            SnapshotFolder,
  [out] Msvm_VirtualSystemSettingData REF ImportedSnapshots[],
  [out] CIM_ConcreteJob               REF Job
);
```



## <a name="parameters"></a>參數

<dl> <dt>

*PlannedSystem* \[在\]
</dt> <dd>

[**Msvm \_ PlannedComputerSystem**](msvm-plannedcomputersystem.md)物件的參考，該物件表示參考要匯入之快照集的計畫虛擬機器。

</dd> <dt>

*SnapshotFolder* \[在\]
</dt> <dd>

可在其中找到此虛擬機器的快照集設定之資料夾的完整路徑。

</dd> <dt>

*ImportedSnapshots* \[擴展\]
</dt> <dd>

如果作業同步完成，則為 [**Msvm \_ VirtualSystemSettingData**](msvm-virtualsystemsettingdata.md) 實例的參考陣列，代表已成功匯入的快照集。

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
| 最低支援的用戶端<br/> | \[僅 Windows 8 桌面應用程式\]<br/>                                                              |
| 最低支援的伺服器<br/> | 僅限 Windows Server 2012 \[ desktop 應用程式\]<br/>                                                    |
| 命名空間<br/>                | 根 \\ 虛擬化 \\ V2<br/>                                                                     |
| MOF<br/>                      | <dl> <dt>WindowsVirtualization。</dt> </dl> |
| DLL<br/>                      | <dl> <dt>Vmms.exe</dt> </dl>                     |



## <a name="see-also"></a>另請參閱

<dl> <dt>

[**Msvm \_ VirtualSystemManagementService**](msvm-virtualsystemmanagementservice.md)
</dt> </dl>

 

