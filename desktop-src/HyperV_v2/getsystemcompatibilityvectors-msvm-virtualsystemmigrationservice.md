---
description: 取得 \_ 可用來檢查虛擬機器 (VM) 以裝載相容性的 Msvm CompatibilityVector 實例清單。
ms.assetid: 3881D9A0-07C2-4275-925D-F3C3A36B79B4
title: Msvm_VirtualSystemMigrationService：： GetSystemCompatibilityVectors 方法
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Msvm_VirtualSystemMigrationService.GetSystemCompatibilityVectors
api_type:
- COM
api_location:
- vmms.exe
ms.openlocfilehash: 19eb9fe54c9a20e635d706eff9b22eb0e78cb8347b27fcdcaff0f419e60a6112
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/11/2021
ms.locfileid: "119427658"
---
# <a name="msvm_virtualsystemmigrationservicegetsystemcompatibilityvectors-method"></a>Msvm \_ VirtualSystemMigrationService：： GetSystemCompatibilityVectors 方法

取得可用來檢查虛擬機器 (VM) 以裝載相容性的 [**Msvm \_ CompatibilityVector**](msvm-compatibilityvector.md) 實例清單。

## <a name="syntax"></a>語法


```C++
uint32 GetSystemCompatibilityVectors(
  [in]  CIM_ComputerSystem   ComputerSystem,
  [out] Msvm_CompatibilityVector CompatibilityVectors[]
);
```



## <a name="parameters"></a>參數

<dl> <dt>

未進行 \[在\]
</dt> <dd>

[**Msvm \_**](msvm-computersystem.md)的同機類別的參考，代表要取得其相容性向量的 VM。 如果此參數參考主控電腦系統，則 *CompatibilityVectors* 參數中所傳回的資料可以用來判斷主控電腦系統上的任何 vm 是否可以快速遷移到另一個主控電腦系統。

</dd> <dt>

*CompatibilityVectors* \[擴展\]
</dt> <dd>

[**Msvm \_ CompatibilityVector**](msvm-compatibilityvector.md)實例的陣列，其中包含 vm 或主控電腦系統的相容性資訊。

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
</dt> </dl>

## <a name="remarks"></a>備註

當虛擬機器在 VM 電腦系統上執行時， **GetSystemCompatibilityVectors** 會取得虛擬機器的相容性資訊 (vm)  () 或在主機電腦系統上執行 (時的主機) 。 用戶端的相容性資訊會保持不變，而資訊會提供方法來比較主機相容性資訊與 VM 的相容性資訊。

## <a name="requirements"></a>規格需求



| 需求 | 值 |
|-------------------------------------|---------------------------------------------------------------------------------------------------------|
| 最低支援的用戶端<br/> | Windows 8.1 \[僅限桌面應用程式\]<br/>                                                            |
| 最低支援的伺服器<br/> | Windows Server 2012\[僅限 R2 desktop 應用程式\]<br/>                                                 |
| 命名空間<br/>                | \\\\根 \\ 虛擬化 \\ V2<br/>                                                                 |
| MOF<br/>                      | <dl> <dt>WindowsVirtualization。</dt> </dl> |
| DLL<br/>                      | <dl> <dt>Vmms.exe</dt> </dl>                     |



## <a name="see-also"></a>另請參閱

<dl> <dt>

[**Msvm \_ CompatibilityVector**](msvm-compatibilityvector.md)
</dt> <dt>

[**Msvm \_ VirtualSystemMigrationService**](msvm-virtualsystemmigrationservice.md)
</dt> </dl>

 

 




