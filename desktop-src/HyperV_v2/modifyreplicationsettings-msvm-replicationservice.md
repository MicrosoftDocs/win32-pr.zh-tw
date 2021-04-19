---
description: 修改虛擬機器的複寫設定。 當用戶端針對複本虛擬機器呼叫這個方法時，它會修改複寫關聯性與擴充複本的複寫設定。
ms.assetid: e68514a5-f508-4047-8dcc-6a95f3e3353e
title: Msvm_ReplicationService 類別的 ModifyReplicationSettings 方法
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Msvm_ReplicationService.ModifyReplicationSettings
api_type:
- COM
api_location:
- vmms.exe
ms.openlocfilehash: d1c932f06350324e0d84559724f7ba0412dfb3e7
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/08/2021
ms.locfileid: "106978272"
---
# <a name="modifyreplicationsettings-method-of-the-msvm_replicationservice-class"></a>Msvm ReplicationService 類別的 ModifyReplicationSettings 方法 \_

修改虛擬機器的複寫設定。 當用戶端針對複本虛擬機器呼叫這個方法時，它會修改複寫關聯性與擴充複本的複寫設定。

## <a name="syntax"></a>語法


```mof
uint32 ModifyReplicationSettings(
  [in]  CIM_ComputerSystem REF ComputerSystem,
  [in]  string                 ReplicationSettingData,
  [out] CIM_ConcreteJob    REF Job
);
```



## <a name="parameters"></a>參數

<dl> <dt>

未進行 \[在\]
</dt> <dd>

[**CIM \_**](/windows/desktop/CIMWin32Prov/cim-computersystem)實例的參考，代表應修改複寫設定的虛擬機器。

</dd> <dt>

*ReplicationSettingData* \[在\]
</dt> <dd>

定義新複寫設定之 [**Msvm \_ ReplicationSettingData**](msvm-replicationsettingdata.md) 類別的字串表示。

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

## <a name="remarks"></a>備註

**ModifyReplicationSettings** 會將 [**Msvm \_ ReplicationSettingData**](msvm-replicationsettingdata.md) 實例 (FRSD) 做為輸入。 虛擬機器與主機對主機提供者相關聯的 FRSD 是預設選項。 針對預設提供者的每個屬性，會驗證輸入 FRSD 是否有有效的設定。 下表摘要說明與外部提供者相關的驗證差異。



| 屬性                                             | 外部提供者                                 |
|------------------------------------------------------|----------------------------------------------------|
| ReplicationProvider                                  | 與預設提供者相同                           |
| AuthenticationType                                   | 忽略                                            |
| CertificateThumbPrint                                | 忽略                                            |
| RootCertificateThumbPrint (RO)                        | 忽略                                            |
| CompressionEnabled                                   | 與預設提供者相同                           |
| BypassProxyServer                                    | 與預設提供者相同                           |
| RecoveryConnectionPoint                              | \*如果提供者有需求，則會忽略 (可能會變更)  |
| RecoveryHostSystem (RO)                               | 忽略                                            |
| PrimaryConnectionPoint (RO)                           | 與預設提供者相同                           |
| PrimaryHostSystem (RO)                                | 與預設提供者相同                           |
| RecoveryServerPortNumber                             | \*如果提供者有需求，則會忽略 (可能會變更)  |
| ReplicateHostKvpItems                                | 忽略                                            |
| ApplicationConsistentSnapshotInterval                | 與預設提供者相同                           |
| RecoveryHistory                                      | 與預設提供者相同                           |
| IncludedDisks\[\]                                    | 與預設提供者相同                           |
| AutoResynchronizeEnabled                             | 與預設提供者相同                           |
| AutoResynchronizeIntervalStart                       | 與預設提供者相同                           |
| AutoResynchronizeIntervalEnd                         | 與預設提供者相同                           |
| EnableWriteOrderPreservationAcrossDisks (已淘汰)  | 與預設提供者相同                           |
| ReplicationInterval                                  | 與預設提供者相同                           |



 

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

[**Msvm \_ ReplicationService**](msvm-replicationservice.md)
</dt> </dl>

 

