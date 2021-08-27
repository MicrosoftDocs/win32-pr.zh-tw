---
description: 啟動虛擬機器的複寫。
ms.assetid: 58e89329-1ad4-4473-856d-ebfd7a863fa8
title: Msvm_ReplicationService 類別的 >startreplication 方法
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Msvm_ReplicationService.StartReplication
api_type:
- COM
api_location:
- vmms.exe
ms.openlocfilehash: f774192cf5c65f6fff0d9a1a17df51483984b49efd6be437f0348547eed5082c
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/11/2021
ms.locfileid: "120050488"
---
# <a name="startreplication-method-of-the-msvm_replicationservice-class"></a>Msvm ReplicationService 類別的 >startreplication 方法 \_

啟動虛擬機器的複寫。 當用戶端針對複本虛擬機器呼叫這個方法時，它會啟動具有擴充複本的複寫。

## <a name="syntax"></a>語法


```mof
uint32 StartReplication(
  [in]  CIM_ComputerSystem REF ComputerSystem,
  [in]  uint16                 InitialReplicationType,
  [in]  string                 InitialReplicationExportLocation,
  [in]  datetime               StartTime,
  [out] CIM_ConcreteJob    REF Job
);
```



## <a name="parameters"></a>參數

<dl> <dt>

未進行 \[在\]
</dt> <dd>

[**CIM \_**](/windows/desktop/CIMWin32Prov/cim-computersystem)實例類型的參考，代表應啟動複寫的虛擬機器。

</dd> <dt>

*InitialReplicationType* \[在\]
</dt> <dd>

要用於執行初始複寫的傳輸類型。

<dt>

<span id="Network_Transfer"></span><span id="network_transfer"></span><span id="NETWORK_TRANSFER"></span>

<span id="Network_Transfer"></span><span id="network_transfer"></span><span id="NETWORK_TRANSFER"></span>**網路傳輸** (1) 


</dt> <dd>

網路傳輸。

</dd> <dt>

<span id="Export"></span><span id="export"></span><span id="EXPORT"></span>

<span id="Export"></span><span id="export"></span><span id="EXPORT"></span>**匯出** (2) 


</dt> <dd>

匯出。

</dd> <dt>

<span id="Seeded_Network_Transfer"></span><span id="seeded_network_transfer"></span><span id="SEEDED_NETWORK_TRANSFER"></span>

<span id="Seeded_Network_Transfer"></span><span id="seeded_network_transfer"></span><span id="SEEDED_NETWORK_TRANSFER"></span>**植入網路傳輸** (3) 


</dt> <dd>

植入的網路傳輸。

</dd> </dl> </dd> <dt>

*InitialReplicationExportLocation* \[在\]
</dt> <dd>

如果 *InitialReplicationType* 為 2 (匯出) ，此參數會包含要匯出初始複寫之目錄的完整路徑。 此參數不會用於其他 *InitialReplicationType* 值，而且可以是 **Null**。 您可以重複使用此目錄來匯出多個虛擬機器複寫。 此方法會將每個虛擬機器複寫放在此路徑底下的個別子目錄中。

</dd> <dt>

*StartTime* \[在\]
</dt> <dd>

透過網路連接到復原伺服器的初始複寫排程開始時間。 當 *InitialReplicationType* 為 2 (匯出) 時，會忽略此參數。 如果此參數為 **Null**，則會立即開始初始複寫。

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

**找不到** 檔案 (32779) 
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

[**Msvm \_ ReplicationService**](msvm-replicationservice.md)
</dt> </dl>

 

