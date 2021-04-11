---
description: 捕獲錯誤。
ms.assetid: a30cb74a-4e41-4981-b355-6f46b4b75ce6
title: Msvm_VirtualSystemReferencePointExportJob 類別的 GetError 方法
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Msvm_VirtualSystemReferencePointExportJob.GetError
api_type:
- COM
api_location:
- vmms.exe
ms.openlocfilehash: b26995171059389f7f7afb3fb90e3506b39affd5
ms.sourcegitcommit: c16214e53680dc71d1c07111b51f72b82a4512d8
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 03/03/2021
ms.locfileid: "104027644"
---
# <a name="geterror-method-of-the-msvm_virtualsystemreferencepointexportjob-class"></a>Msvm VirtualSystemReferencePointExportJob 類別的 GetError 方法 \_

捕獲錯誤。

## <a name="syntax"></a>語法


```mof
uint32 GetError(
  [out] string Error
);
```



## <a name="parameters"></a>參數

<dl> <dt>

*錯誤* \[擴展\]
</dt> <dd>

取出的錯誤。

</dd> </dl>

## <a name="return-value"></a>傳回值

成功時，會傳回 0;否則，會包含錯誤。

<dl> <dt>

**已完成，沒有錯誤** (0) 
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

**System 使用** (32774) 
</dt> <dt>

**此操作的狀態無效** (32775) 
</dt> <dt>

**不正確的資料類型** (32776) 
</dt> <dt>

**系統無法使用** (32777) 
</dt> <dt>

**記憶體不足** (32778) 
</dt> </dl>

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

[**Msvm \_ VirtualSystemReferencePointExportJob**](msvm-virtualsystemreferencepointexportjob.md)
</dt> </dl>

 

 




