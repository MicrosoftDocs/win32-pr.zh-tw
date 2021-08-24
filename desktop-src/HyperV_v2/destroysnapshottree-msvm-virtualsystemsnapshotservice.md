---
description: 移除虛擬機器的現有快照集及其所有子系。
ms.assetid: d7a6442a-41a5-4e82-8ec8-dbc8e14d9a89
title: Msvm_VirtualSystemSnapshotService 類別的 DestroySnapshotTree 方法
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Msvm_VirtualSystemSnapshotService.DestroySnapshotTree
api_type:
- COM
api_location:
- vmms.exe
ms.openlocfilehash: eaa589b7f6c228624f14edbf5254e5b3f5c0cf7d5b6f19c696397d0b70d6e14e
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/11/2021
ms.locfileid: "119254238"
---
# <a name="destroysnapshottree-method-of-the-msvm_virtualsystemsnapshotservice-class"></a>Msvm VirtualSystemSnapshotService 類別的 DestroySnapshotTree 方法 \_

移除虛擬機器的現有快照集及其所有子系。

## <a name="syntax"></a>語法


```mof
uint32 DestroySnapshotTree(
  [in]  CIM_VirtualSystemSettingData REF SnapshotSettingData,
  [out] CIM_ConcreteJob              REF Job
);
```



## <a name="parameters"></a>參數

<dl> <dt>

*SnapshotSettingData* \[在\]
</dt> <dd>

[**CIM \_ VirtualSystemSettingData**](/previous-versions//cc136954(v=vs.85))參考，代表要終結的虛擬機器快照集樹狀結構。

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

[**Msvm \_ VirtualSystemSnapshotService**](msvm-virtualsystemsnapshotservice.md)
</dt> <dt>

[**RemoveVirtualSystemSnapshotTree (V1)**](/previous-versions/windows/desktop/virtual/removevirtualsystemsnapshottree-msvm-virtualsystemmanagementservice)
</dt> </dl>

 

