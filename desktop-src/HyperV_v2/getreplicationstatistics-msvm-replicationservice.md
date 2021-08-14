---
description: 抓取虛擬機器的複寫統計資料，並在虛擬機器的主要複寫關聯性上運作。
ms.assetid: 24f3f572-fa85-4680-be77-7e835e6471c5
title: Msvm_ReplicationService 類別的 GetReplicationStatistics 方法
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Msvm_ReplicationService.GetReplicationStatistics
api_type:
- COM
api_location:
- vmms.exe
ms.openlocfilehash: 767ea873b725523e3d430708dc5485d3d24c62e07e5cebac001b020ee996bd63
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/11/2021
ms.locfileid: "118392912"
---
# <a name="getreplicationstatistics-method-of-the-msvm_replicationservice-class"></a>Msvm ReplicationService 類別的 GetReplicationStatistics 方法 \_

抓取虛擬機器的複寫統計資料，並在虛擬機器的主要複寫關聯性上運作。

> [!Note]  
> 從 Windows 8.1 開始，建議您不再使用 **GetReplicationStatistics** 來取出複寫統計資料。 相反地，請使用 [**GetReplicationStatisticsEx**](getreplicationstatisticsex-msvm-replicationservice.md)。

 

## <a name="syntax"></a>語法


```mof
uint32 GetReplicationStatistics(
  [in]  CIM_ComputerSystem REF ComputerSystem,
  [out] string                 ReplicationStatistics[],
  [out] string                 ReplicationHealthIssues[],
  [out] CIM_ConcreteJob    REF Job
);
```



## <a name="parameters"></a>參數

<dl> <dt>

未進行 \[在\]
</dt> <dd>

[**CIM \_**](/windows/desktop/CIMWin32Prov/cim-computersystem)實例的參考，代表要取得其複寫統計資料的虛擬機器。

</dd> <dt>

*ReplicationStatistics* \[擴展\]
</dt> <dd>

如果成功，則會收到 [**Msvm \_ ReplicationStatistics**](msvm-replicationstatistics.md) 類別的內嵌實例，其中包含所要求之虛擬機器的複寫統計資料。

</dd> <dt>

*ReplicationHealthIssues* \[擴展\]
</dt> <dd>

如果成功，會接收 [**Msvm \_ 錯誤**](msvm-error.md) 類別的內嵌實例陣列，指出所要求之虛擬機器的任何複寫警告或錯誤。

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

**System 使用** (32774) 
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

[**ResetReplicationStatistics**](resetreplicationstatistics-msvm-replicationservice.md)
</dt> <dt>

[**Msvm \_ ReplicationService**](msvm-replicationservice.md)
</dt> </dl>

 

