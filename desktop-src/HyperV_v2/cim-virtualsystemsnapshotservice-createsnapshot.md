---
description: 建立虛擬系統的快照集。
ms.assetid: cad4cb4f-523f-4fda-ac88-8cece7abc227
title: CIM_VirtualSystemSnapshotService 類別的 >icloudblob.createsnapshot 方法
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CIM_VirtualSystemSnapshotService.CreateSnapshot
api_type:
- COM
api_location:
- vmms.exe
ms.openlocfilehash: 8ee1a2e66745ceac50cc00ba6e625a171f18c7d2b54d4e51af2c86f6711675ea
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/11/2021
ms.locfileid: "119532748"
---
# <a name="createsnapshot-method-of-the-cim_virtualsystemsnapshotservice-class"></a>CIM VirtualSystemSnapshotService 類別的 >icloudblob.createsnapshot 方法 \_

建立虛擬系統的快照集。

## <a name="syntax"></a>語法


```mof
uint32 CreateSnapshot(
  [in]      CIM_ComputerSystem           REF AffectedSystem,
  [in]      string                           SnapshotSettings,
  [in]      uint16                           SnapshotType,
  [in, out] CIM_VirtualSystemSettingData REF ResultingSnapshot,
  [out]     CIM_ConcreteJob              REF Job
);
```



## <a name="parameters"></a>參數

<dl> <dt>

*AffectedSystem* \[在\]
</dt> <dd>

受影響之虛擬系統的 CIM 系統可參考。 [**\_**](cim-computersystem.md)

</dd> <dt>

*SnapshotSettings* \[在\]
</dt> <dd>

參數設定。

</dd> <dt>

*SnapshotType* \[在\]
</dt> <dd>

要求的快照集類型：

<dt>

<span id="Full_Snapshot"></span><span id="full_snapshot"></span><span id="FULL_SNAPSHOT"></span>

<span id="Full_Snapshot"></span><span id="full_snapshot"></span><span id="FULL_SNAPSHOT"></span>**完整快照** (2) 


</dt> <dd>

虛擬系統的完整快照集。

</dd> <dt>

<span id="Disk_Snapshot"></span><span id="disk_snapshot"></span><span id="DISK_SNAPSHOT"></span>

<span id="Disk_Snapshot"></span><span id="disk_snapshot"></span><span id="DISK_SNAPSHOT"></span>**磁片快照** (3) 


</dt> <dd>

虛擬系統磁片的快照集。

</dd> <dt>

<span id="DMTF_Reserved"></span><span id="dmtf_reserved"></span><span id="DMTF_RESERVED"></span>

<span id="DMTF_Reserved"></span><span id="dmtf_reserved"></span><span id="DMTF_RESERVED"></span>**DMTF 保留** ( .。。) 


</dt> <dd></dd> <dt>

<span id="Vendor_Specific"></span><span id="vendor_specific"></span><span id="VENDOR_SPECIFIC"></span>

<span id="Vendor_Specific"></span><span id="vendor_specific"></span><span id="VENDOR_SPECIFIC"></span>**廠商特定** (32768. 65535) 


</dt> <dd></dd> </dl> </dd> <dt>

*ResultingSnapshot* \[in、out\]
</dt> <dd>

產生的虛擬系統快照集的 [**CIM \_ VirtualSystemSettingData**](cim-virtualsystemsettingdata.md) 參考。

</dd> <dt>

*作業* \[擴展\]
</dt> <dd>

如果作業的執行時間很長，則可以選擇性地傳回作業。 在此情況下，代表新虛擬系統快照集的 [**cim \_ VirtualSystemSettingData**](cim-virtualsystemsettingdata.md) 類別的實例會透過 [**cim \_ AffectedJobElement**](cim-affectedjobelement.md) 關聯來呈現，而 **AffectedElement** 屬性的值會參考代表虛擬系統快照的 **cim \_ VirtualSystemSettingData** 類別的新實例，而 **ElementEffects** 的值則會設定為 5 (建立) 。

> [!Note]  
> 此參數在 Windows 8.1 中是讀取/寫入。

 

</dd> </dl>

## <a name="return-value"></a>傳回值

成功時，會傳回 0;否則，會傳回錯誤。

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

**不正確類型** (6) 
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

[**CIM \_ VirtualSystemSnapshotService**](cim-virtualsystemsnapshotservice.md)
</dt> </dl>

 

 




