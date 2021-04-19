---
description: 終結虛擬系統。
ms.assetid: 8d2504dc-ce23-4257-9dfd-6a35dfd84b2d
title: CIM_VirtualSystemManagementService 類別的 DestroySystem 方法
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CIM_VirtualSystemManagementService.DestroySystem
api_type:
- COM
api_location:
- vmms.exe
ms.openlocfilehash: 41355970bb70063b8e90deb8f49b5e6f4b439017
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/07/2021
ms.locfileid: "106983577"
---
# <a name="destroysystem-method-of-the-cim_virtualsystemmanagementservice-class"></a>CIM VirtualSystemManagementService 類別的 DestroySystem 方法 \_

終結虛擬系統。

受參考的虛擬系統已終結，包括其範圍內的任何元素。 虛擬資源會傳回到其資源集區，這可能表示將這些資源的終結 (實) 的相依。 如果虛擬系統在叫用作業時處於作用中狀態，則會先將它停用，然後再損毀。 如果快照集是從虛擬系統建立的，也會損毀。

## <a name="syntax"></a>語法


```mof
uint32 DestroySystem(
  [in]  CIM_ComputerSystem REF AffectedSystem,
  [out] CIM_ConcreteJob    REF Job
);
```



## <a name="parameters"></a>參數

<dl> <dt>

*AffectedSystem* \[在\]
</dt> <dd>

參考 CIM 的類別實例， [**代表 \_**](cim-computersystem.md) 要終結的虛擬電腦系統。

</dd> <dt>

*作業* \[擴展\]
</dt> <dd>

如果作業的執行時間很長，則可以選擇性地傳回代表作業的 [**CIM \_ ConcreteJob**](cim-concretejob.md) 。

</dd> </dl>

## <a name="return-value"></a>傳回值

成功時傳回 0;否則，會傳回錯誤。

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

**DMTF 保留** ( .。。) 
</dt> <dt>

**已檢查方法參數-工作已啟動** (4096) 
</dt> <dt>

**方法保留** (4097. 32767) 
</dt> <dt>

**廠商特定** (32768. 65535) 
</dt> </dl>

## <a name="requirements"></a>規格需求



| 需求 | 值 |
|-------------------------------------|---------------------------------------------------------------------------------------------------------|
| 最低支援的用戶端<br/> | Windows 8.1<br/>                                                                                  |
| 最低支援的伺服器<br/> | Windows Server 2012 R2<br/>                                                                       |
| 命名空間<br/>                | 根 \\ 虛擬化 \\ v2<br/>                                                                     |
| MOF<br/>                      | <dl> <dt>WindowsVirtualization。</dt> </dl> |
| DLL<br/>                      | <dl> <dt>Vmms.exe</dt> </dl>                     |



## <a name="see-also"></a>另請參閱

<dl> <dt>

[**CIM \_ VirtualSystemManagementService**](cim-virtualsystemmanagementservice.md)
</dt> </dl>

 

 




