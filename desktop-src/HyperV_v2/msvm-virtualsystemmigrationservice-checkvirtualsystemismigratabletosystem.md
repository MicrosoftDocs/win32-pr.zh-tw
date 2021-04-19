---
description: 判斷指定的虛擬系統是否可以遷移到目的地系統。
ms.assetid: 2E340737-DEE9-4853-ACD8-BEE2A8C69D6D
title: Msvm_VirtualSystemMigrationService 類別的 CheckVirtualSystemIsMigratableToSystem 方法
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Msvm_VirtualSystemMigrationService.CheckVirtualSystemIsMigratableToSystem
api_type:
- COM
api_location:
- vmms.exe
ms.openlocfilehash: 3e8f294f7e30740e3afab8987c734dbbdbd12acf
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/07/2021
ms.locfileid: "106973610"
---
# <a name="checkvirtualsystemismigratabletosystem-method-of-the-msvm_virtualsystemmigrationservice-class"></a>Msvm VirtualSystemMigrationService 類別的 CheckVirtualSystemIsMigratableToSystem 方法 \_

判斷指定的虛擬系統是否可以遷移到目的地系統。

## <a name="syntax"></a>語法


```mof
uint32 CheckVirtualSystemIsMigratableToSystem(
  [in]  Msvm_ComputerSystem REF ComputerSystem,
  [in]  Msvm_ComputerSystem REF DestinationSystem,
  [in]  string                  MigrationSettingData,
  [in]  string                  NewSystemSettingData,
  [in]  string                  NewResourceSettingData[],
  [out] boolean                 IsMigratable
);
```



## <a name="parameters"></a>參數

<dl> <dt>

未進行 \[在\]
</dt> <dd>

[**Msvm \_**](msvm-computersystem.md)實例類別的實例參考，代表要測試其遷移能力的虛擬機器。

</dd> <dt>

*DestinationSystem* \[在\]
</dt> <dd>

[**Msvm \_**](msvm-computersystem.md)實例類別的實例參考，代表要測試遷移能力的虛擬機器。

</dd> <dt>

*MigrationSettingData* \[在\]
</dt> <dd>

[**Msvm \_ VirtualSystemMigrationSettingData**](msvm-virtualsystemmigrationsettingdata.md)類別的內嵌實例，代表遷移作業的設定。

</dd> <dt>

*NewSystemSettingData* \[在\]
</dt> <dd>

[**Msvm \_ VirtualSystemSettingData**](msvm-virtualsystemsettingdata.md)類別的內嵌實例，代表在遷移之後適用于虛擬系統的新屬性。

</dd> <dt>

*NewResourceSettingData* \[在\]
</dt> <dd>

字串陣列，其中包含 [**Msvm \_ ResourceAllocationSettingData**](msvm-resourceallocationsettingdata.md) 類別的內嵌實例，表示在遷移之後，適用于虛擬系統虛擬資源的新屬性。

</dd> <dt>

*IsMigratable* \[擴展\]
</dt> <dd>

接收遷移檢查結果，指出是否可以成功遷移虛擬系統。

</dd> </dl>

## <a name="return-value"></a>傳回值

這個方法會傳回下列其中一個值。

<dl> <dt>

**已完成，沒有錯誤** (0) 
</dt> <dt>

**不支援** (1) 
</dt> <dt>

**失敗** (2) 
</dt> <dt>

**Timeout** (3) 
</dt> <dt>

**不正確參數** (4) 
</dt> <dt>

**不正確狀態** (5) 
</dt> <dt>

 (6) 的 **參數不相容**
</dt> <dt>

**DMTF 保留** ( .。。) 
</dt> <dt>

**方法保留** (4097. 32767) 
</dt> <dt>

**廠商特定** (32768. 65535 ) 
</dt> </dl>

## <a name="requirements"></a>規格需求



| 需求 | 值 |
|-------------------------------------|---------------------------------------------------------------------------------------------------------|
| 最低支援的用戶端<br/> | \[僅 Windows 10 桌面應用程式\]<br/>                                                             |
| 最低支援的伺服器<br/> | 僅限 Windows Server 2016 \[ desktop 應用程式\]<br/>                                                    |
| 命名空間<br/>                | 根 \\ 虛擬化 \\ V2<br/>                                                                     |
| MOF<br/>                      | <dl> <dt>WindowsVirtualization。</dt> </dl> |
| DLL<br/>                      | <dl> <dt>Vmms.exe</dt> </dl>                     |



## <a name="see-also"></a>另請參閱

<dl> <dt>

[**Msvm \_ VirtualSystemMigrationService**](msvm-virtualsystemmigrationservice.md)
</dt> </dl>

 

 




