---
description: 提供虛擬機器的複寫統計資料。
ms.assetid: 52d944a7-9309-4b56-97b7-e050a9501c57
title: Msvm_ReplicationStatistics 類別
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Msvm_ReplicationStatistics
- Msvm_ReplicationStatistics.InstanceID
- Msvm_ReplicationStatistics.Caption
- Msvm_ReplicationStatistics.Description
- Msvm_ReplicationStatistics.ElementName
- Msvm_ReplicationStatistics.StartStatisticTime
- Msvm_ReplicationStatistics.EndStatisticTime
- Msvm_ReplicationStatistics.ReplicationSuccessCount
- Msvm_ReplicationStatistics.ReplicationSize
- Msvm_ReplicationStatistics.MaxReplicationSize
- Msvm_ReplicationStatistics.ReplicationLatency
- Msvm_ReplicationStatistics.ReplicationMissCount
- Msvm_ReplicationStatistics.MaxReplicationLatency
- Msvm_ReplicationStatistics.NetworkFailureCount
- Msvm_ReplicationStatistics.ReplicationFailureCount
- Msvm_ReplicationStatistics.PendingReplicationSize
- Msvm_ReplicationStatistics.ApplicationConsistentSnapshotFailureCount
- Msvm_ReplicationStatistics.ReplicationHealth
- Msvm_ReplicationStatistics.LastTestFailoverTime
api_type:
- DllExport
api_location:
- vmms.exe
ms.openlocfilehash: 3f18501c2da875a9c3514549271fbc91620abef2
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/08/2021
ms.locfileid: "106991878"
---
# <a name="msvm_replicationstatistics-class"></a>Msvm \_ ReplicationStatistics 類別

提供虛擬機器的複寫統計資料。 這些統計資料涵蓋 [**Msvm \_ ReplicationServiceSettingData**](msvm-replicationservicesettingdata.md)類別的 **MonitoringStartTime** 和 **MonitoringInterval** 屬性所指定的持續時間。

下列語法已簡化受控物件格式 (MOF) 程式碼，並且包含所有繼承的屬性。

## <a name="syntax"></a>語法

``` syntax
[Dynamic, Provider("VmmsWmiInstanceAndMethodProvider"), AMENDMENT]
class Msvm_ReplicationStatistics : CIM_ManagedElement
{
  string   InstanceID;
  string   Caption;
  string   Description;
  string   ElementName;
  datetime StartStatisticTime;
  datetime EndStatisticTime;
  uint32   ReplicationSuccessCount;
  uint64   ReplicationSize;
  uint64   MaxReplicationSize;
  uint32   ReplicationLatency;
  uint32   ReplicationMissCount;
  uint32   MaxReplicationLatency;
  uint32   NetworkFailureCount;
  uint32   ReplicationFailureCount;
  uint64   PendingReplicationSize;
  uint32   ApplicationConsistentSnapshotFailureCount;
  uint32   ReplicationHealth;
  datetime LastTestFailoverTime;
};
```

## <a name="members"></a>成員

**Msvm \_ ReplicationStatistics** 類別具有下列類型的成員：

-   [屬性](#properties)

### <a name="properties"></a>屬性

**Msvm \_ ReplicationStatistics** 類別具有這些屬性。

<dl> <dt>

**ApplicationConsistentSnapshotFailureCount**
</dt> <dd> <dl> <dt>

資料類型： **uint32**
</dt> <dt>

存取類型：唯讀
</dt> </dl>

VSS 快照集失敗的總數。

</dd> <dt>

**標題**
</dt> <dd> <dl> <dt>

資料類型： **字串**
</dt> <dt>

存取類型：唯讀
</dt> </dl>

物件的簡短描述。 這個屬性繼承自 [**CIM \_ ManagedElement**](/previous-versions/windows/desktop/iscsitarg/cim-managedelement)，一律設為 **Null**。

</dd> <dt>

**說明**
</dt> <dd> <dl> <dt>

資料類型： **字串**
</dt> <dt>

存取類型：唯讀
</dt> </dl>

對物件的描述。 這個屬性繼承自 [**CIM \_ ManagedElement**](/previous-versions/windows/desktop/iscsitarg/cim-managedelement)，一律設為 **Null**。

</dd> <dt>

**ElementName**
</dt> <dd> <dl> <dt>

資料類型： **字串**
</dt> <dt>

存取類型：唯讀
</dt> </dl>

物件的顯示名稱。 這個屬性繼承自 [**CIM \_ ManagedElement**](/previous-versions/windows/desktop/iscsitarg/cim-managedelement)，一律設為 **Null**。

</dd> <dt>

**EndStatisticTime**
</dt> <dd> <dl> <dt>

資料類型： **datetime**
</dt> <dt>

存取類型：唯讀
</dt> </dl>

Hyper-v 複本服務停止收集複寫統計資料的時間（UTC）。 此時，新的複寫統計資料迴圈隨即啟動。

</dd> <dt>

**InstanceID**
</dt> <dd> <dl> <dt>

資料類型： **字串**
</dt> <dt>

存取類型：唯讀
</dt> <dt>

限定詞：索引 **鍵**
</dt> </dl>

唯一識別此類別的實例。 這個屬性繼承自 [**CIM \_ ManagedElement**](/previous-versions/windows/desktop/iscsitarg/cim-managedelement)，一律設為 **Null**。

</dd> <dt>

**LastTestFailoverTime**
</dt> <dd> <dl> <dt>

資料類型： **datetime**
</dt> <dt>

存取類型：唯讀
</dt> </dl>

指出上次為復原伺服器上已啟用複寫的虛擬機器建立測試複本系統的時間。

</dd> <dt>

**MaxReplicationLatency**
</dt> <dd> <dl> <dt>

資料類型： **uint32**
</dt> <dt>

存取類型：唯讀
</dt> </dl>

完成單一複寫週期所需的最大時間量（以秒為單位）。

</dd> <dt>

**MaxReplicationSize**
</dt> <dd> <dl> <dt>

資料類型： **uint64**
</dt> <dt>

存取類型：唯讀
</dt> </dl>

傳輸至復原主機系統的複寫資料上限（以位元組為單位）。 這代表在此間隔中，透過單一週期傳送的複寫資料大小上限。

</dd> <dt>

**NetworkFailureCount**
</dt> <dd> <dl> <dt>

資料類型： **uint32**
</dt> <dt>

存取類型：唯讀
</dt> </dl>

具有復原主機系統的複寫通道所遇到的網路錯誤總數。

</dd> <dt>

**PendingReplicationSize**
</dt> <dd> <dl> <dt>

資料類型： **uint64**
</dt> <dt>

存取類型：唯讀
</dt> </dl>

暫止複寫的資料大小（以位元組為單位）。

</dd> <dt>

**ReplicationFailureCount**
</dt> <dd> <dl> <dt>

資料類型： **uint32**
</dt> <dt>

存取類型：唯讀
</dt> </dl>

複寫失敗的總數。 這包括複寫操作的錯誤。

</dd> <dt>

**ReplicationHealth**
</dt> <dd> <dl> <dt>

資料類型： **uint32**
</dt> <dt>

存取類型：唯讀
</dt> </dl>

虛擬機器的複寫健全狀況。 這會是下列其中一個值。

<dl> <dt>

<span id="Not_applicable"></span><span id="not_applicable"></span><span id="NOT_APPLICABLE"></span>**不適用** (0) 
</dt> <dt>

<span id="Ok"></span><span id="ok"></span><span id="OK"></span>**確定** (1) 
</dt> <dt>

<span id="Warning"></span><span id="warning"></span><span id="WARNING"></span>**警告** (2) 
</dt> <dt>

<span id="Critical_________________"></span><span id="critical_________________"></span><span id="CRITICAL_________________"></span>**重大** (3) 
</dt> </dl>

</dd> <dt>

**ReplicationLatency**
</dt> <dd> <dl> <dt>

資料類型： **uint32**
</dt> <dt>

存取類型：唯讀
</dt> </dl>

將資料傳輸至復原主機系統時的複寫延遲總計（以秒為單位）。

</dd> <dt>

**ReplicationMissCount**
</dt> <dd> <dl> <dt>

資料類型： **uint32**
</dt> <dt>

存取類型：唯讀
</dt> </dl>

遺漏的複寫週期數。 這可能是因為工作負載過重、網路問題或複寫錯誤所導致。

</dd> <dt>

**ReplicationSize**
</dt> <dd> <dl> <dt>

資料類型： **uint64**
</dt> <dt>

存取類型：唯讀
</dt> </dl>

傳輸至復原主機系統的複寫資料總量（以位元組為單位）。

</dd> <dt>

**ReplicationSuccessCount**
</dt> <dd> <dl> <dt>

資料類型： **uint32**
</dt> <dt>

存取類型：唯讀
</dt> </dl>

虛擬機器的成功複寫總數。

</dd> <dt>

**StartStatisticTime**
</dt> <dd> <dl> <dt>

資料類型： **datetime**
</dt> <dt>

存取類型：唯讀
</dt> </dl>

Hyper-v 複本服務開始收集複寫統計資料的時間（UTC）。

</dd> </dl>

## <a name="requirements"></a>規格需求



| 需求 | 值 |
|-------------------------------------|---------------------------------------------------------------------------------------------------------|
| 最低支援的用戶端<br/> | \[僅 Windows 8 桌面應用程式\]<br/>                                                              |
| 最低支援的伺服器<br/> | 僅限 Windows Server 2012 \[ desktop 應用程式\]<br/>                                                    |
| 命名空間<br/>                | 根 \\ 虛擬化 \\ V2<br/>                                                                     |
| MOF<br/>                      | <dl> <dt>WindowsVirtualization。</dt> </dl> |
| DLL<br/>                      | <dl> <dt>Vmms.exe</dt> </dl>                     |



 

