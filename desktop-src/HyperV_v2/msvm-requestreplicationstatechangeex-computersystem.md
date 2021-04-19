---
description: 要求虛擬機器複寫關聯性的複寫狀態變更為指定的值。
ms.assetid: 8EC78CCC-2997-4239-A20C-BA56F848ECB6
title: Msvm_ComputerSystem：： RequestReplicationStateChangeEx 方法
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Msvm_ComputerSystem.RequestReplicationStateChangeEx
api_type:
- COM
api_location:
- vmms.exe
ms.openlocfilehash: d77db9dff90f985991c8e9013ea4f239cb6479f5
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/08/2021
ms.locfileid: "106987216"
---
# <a name="msvm_computersystemrequestreplicationstatechangeex-method"></a>Msvm \_ ：： RequestReplicationStateChangeEx 方法

要求虛擬機器複寫關聯性的複寫狀態變更為指定的值。 當狀態變更正在進行時， **ReplicationState** 屬性會變更為 *RequestedState* 參數的值。 只有代表虛擬機器的 Msvm 同機類別 [**\_**](msvm-computersystem.md) 實例才支援這個方法。

## <a name="syntax"></a>語法


```C++
uint32 RequestReplicationStateChangeEx(
  [in]  string              ReplicationRelationship,
  [in]  uint16              RequestedState,
  [out] CIM_ConcreteJob Job,
  [in]  datetime            TimeoutPeriod
);
```



## <a name="parameters"></a>參數

<dl> <dt>

*ReplicationRelationship* \[在\]
</dt> <dd>

[**Msvm \_ ReplicationRelationship**](msvm-replicationrelationship.md)類別之內嵌實例的字串表示，這個類別會定義狀態變更要求的複寫關聯性。 這是選擇性參數。 未指定時，會在主要複寫關聯性上執行要求。

</dd> <dt>

*RequestedState* \[在\]
</dt> <dd>

新的複寫狀態。 必須是下列其中一個值。

<dt>

<span id="Ready_to_start_initial_replication"></span><span id="ready_to_start_initial_replication"></span><span id="READY_TO_START_INITIAL_REPLICATION"></span>

<span id="Ready_to_start_initial_replication"></span><span id="ready_to_start_initial_replication"></span><span id="READY_TO_START_INITIAL_REPLICATION"></span>**準備開始初始** 複寫 (1) 


</dt> <dd>

準備開始初始複寫。

</dd> <dt>

<span id="Waiting_to_complete_initial_replication"></span><span id="waiting_to_complete_initial_replication"></span><span id="WAITING_TO_COMPLETE_INITIAL_REPLICATION"></span>

<span id="Waiting_to_complete_initial_replication"></span><span id="waiting_to_complete_initial_replication"></span><span id="WAITING_TO_COMPLETE_INITIAL_REPLICATION"></span>**等候完成初始** 複寫 (2) 


</dt> <dd>

正在等候完成初始複寫。

</dd> <dt>

<span id="Replicating"></span><span id="replicating"></span><span id="REPLICATING"></span>

<span id="Replicating"></span><span id="replicating"></span><span id="REPLICATING"></span>複寫 **(3**) 


</dt> <dd>

複寫。

</dd> <dt>

<span id="Synced_replication_complete"></span><span id="synced_replication_complete"></span><span id="SYNCED_REPLICATION_COMPLETE"></span>

<span id="Synced_replication_complete"></span><span id="synced_replication_complete"></span><span id="SYNCED_REPLICATION_COMPLETE"></span>**同步複寫完成** (4) 


</dt> <dd>

同步的複寫完成。

</dd> <dt>

<span id="Suspend"></span><span id="suspend"></span><span id="SUSPEND"></span>

<span id="Suspend"></span><span id="suspend"></span><span id="SUSPEND"></span>**暫** 止 (7) 


</dt> <dd>

暫止複寫。

</dd> <dt>

<span id="Cancel_Resynchronize"></span><span id="cancel_resynchronize"></span><span id="CANCEL_RESYNCHRONIZE"></span>

<span id="Cancel_Resynchronize"></span><span id="cancel_resynchronize"></span><span id="CANCEL_RESYNCHRONIZE"></span>**取消重新同步** 處理 (9) 


</dt> <dd>

取消重新同步處理。

</dd> </dl> </dd> <dt>

*作業* \[擴展\]
</dt> <dd>

如果以非同步方式執行作業，則為所傳回之 [**Msvm \_ ConcreteJob**](msvm-concretejob.md) 物件的選擇性參考。 如果有，則會使用傳回的參考來監視進度，並取得方法的結果。

</dd> <dt>

*TimeoutPeriod* \[在\]
</dt> <dd>

不使用這個參數。

</dd> </dl>

## <a name="return-value"></a>傳回值

這個方法會傳回下列其中一個值。



| 傳回碼/值                                                                                                                                                                | Description                                                                                                                 |
|----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|-----------------------------------------------------------------------------------------------------------------------------|
| <dl> <dt>**已完成，沒有錯誤**</dt> <dt>0</dt> </dl>                    | Success<br/>                                                                                                          |
| <dl> <dt>**已檢查方法參數-作業已啟動**</dt> <dt>4096</dt> </dl> | 轉換是非同步。<br/>                                                                                  |
| <dl> <dt>**失敗**</dt> <dt>32768</dt> </dl>                                 |                                                                                                                             |
| <dl> <dt>**拒絕存取**</dt> <dt>32769</dt> </dl>                          |                                                                                                                             |
| <dl> <dt>**不支援**</dt> <dt>32770</dt> </dl>                          |                                                                                                                             |
| <dl> <dt>**狀態為未知**</dt> <dt>32771</dt> </dl>                      |                                                                                                                             |
| <dl> <dt>**Timeout**</dt> <dt>32772</dt> </dl>                                |                                                                                                                             |
| <dl> <dt>**不正確參數**</dt> <dt>32773</dt> </dl>                      | 不支援其中一個參數所指定的值。<br/>                                                   |
| <dl> <dt>**系統使用中**</dt> <dt>32774</dt> </dl>                       |                                                                                                                             |
| <dl> <dt>**此操作的狀態無效**</dt> <dt>32775</dt> </dl>       | 在目前的複寫模式或狀態中，不支援在 *RequestedState* 參數中指定的值。<br/> |
| <dl> <dt>**不正確的資料類型**</dt> <dt>32776</dt> </dl>                    |                                                                                                                             |
| <dl> <dt>**系統無法使用**</dt> <dt>32777</dt> </dl>                |                                                                                                                             |
| <dl> <dt>**記憶體不足**</dt> <dt>32778</dt> </dl>                          |                                                                                                                             |
| <dl> <dt>**找不到**</dt>檔案 <dt>32779</dt> </dl>                         |                                                                                                                             |



 

## <a name="requirements"></a>規格需求



| 需求 | 值 |
|-------------------------------------|---------------------------------------------------------------------------------------------------------|
| 最低支援的用戶端<br/> | \[僅 Windows 8.1 桌面應用程式\]<br/>                                                            |
| 最低支援的伺服器<br/> | 僅限 Windows Server 2016 \[ desktop 應用程式\]<br/>                                                    |
| 命名空間<br/>                | \\\\根 \\ 虛擬化 \\ V2<br/>                                                                 |
| MOF<br/>                      | <dl> <dt>WindowsVirtualization。</dt> </dl> |
| DLL<br/>                      | <dl> <dt>Vmms.exe</dt> </dl>                     |



## <a name="see-also"></a>另請參閱

<dl> <dt>

[**Msvm \_**](msvm-computersystem.md)
</dt> </dl>

 

 




