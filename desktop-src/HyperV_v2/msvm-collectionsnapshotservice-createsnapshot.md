---
description: 建立虛擬系統集合的快照集。
ms.assetid: 2512d82f-06b9-4613-b920-d3a9be884a75
title: Msvm_CollectionSnapshotService 類別的 >icloudblob.createsnapshot 方法
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Msvm_CollectionSnapshotService.CreateSnapshot
api_type:
- COM
api_location:
- vmms.exe
ms.openlocfilehash: 251213d0ff7a98d922a4dec761252479f911e66e2304596a97858fe0b7dc5fbf
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/11/2021
ms.locfileid: "119426908"
---
# <a name="createsnapshot-method-of-the-msvm_collectionsnapshotservice-class"></a>Msvm CollectionSnapshotService 類別的 >icloudblob.createsnapshot 方法 \_

建立虛擬系統集合的快照集。

## <a name="syntax"></a>語法


```mof
uint32 CreateSnapshot(
  [in]      CIM_CollectionOfMSEs REF Collection,
  [in]      string                   SnapshotSettings,
  [in]      uint16                   SnapshotType,
  [in, out] CIM_Collection       REF ResultingSnapshotCollection,
  [out]     CIM_ConcreteJob      REF Job
);
```



## <a name="parameters"></a>參數

<dl> <dt>

*集合* \[在\]
</dt> <dd>

參考描述受影響之虛擬系統集合的 [**CIM \_ CollectionOfMSEs**](cim-collectionofmses.md) 。

</dd> <dt>

*SnapshotSettings* \[在\]
</dt> <dd>

包含參數設定。

</dd> <dt>

*SnapshotType* \[在\]
</dt> <dd>

要求的快照集類型：

<dt>

<span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>

<span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>**未知** 的 (0) 


</dt> <dd></dd> <dt>

<span id="Standard_Snapshot"></span><span id="standard_snapshot"></span><span id="STANDARD_SNAPSHOT"></span>

<span id="Standard_Snapshot"></span><span id="standard_snapshot"></span><span id="STANDARD_SNAPSHOT"></span>**標準快照** (1) 


</dt> <dd>

虛擬系統的標準快照集。

</dd> <dt>

<span id="Recovery_Snapshot"></span><span id="recovery_snapshot"></span><span id="RECOVERY_SNAPSHOT"></span>

<span id="Recovery_Snapshot"></span><span id="recovery_snapshot"></span><span id="RECOVERY_SNAPSHOT"></span>**修復快照** (2) 


</dt> <dd>

復原案例的快照，包括容錯移轉複寫和備份。

</dd> <dt>

<span id="DMTF_Reserved"></span><span id="dmtf_reserved"></span><span id="DMTF_RESERVED"></span>

<span id="DMTF_Reserved"></span><span id="dmtf_reserved"></span><span id="DMTF_RESERVED"></span>**DMTF 保留** ( .。。) 


</dt> <dd></dd> <dt>

<span id="Vendor_Specific"></span><span id="vendor_specific"></span><span id="VENDOR_SPECIFIC"></span>

<span id="Vendor_Specific"></span><span id="vendor_specific"></span><span id="VENDOR_SPECIFIC"></span>**廠商特定** (32768. 65535) 


</dt> <dd></dd> </dl> </dd> <dt>

*ResultingSnapshotCollection* \[in、out\]
</dt> <dd>

成功時，傳回包含虛擬系統快照 [**集的 CIM \_ 集合**](cim-collection.md) 參考。

</dd> <dt>

*作業* \[擴展\]
</dt> <dd>

如果以非同步方式執行作業，則會傳回選擇性的參考。 如果有，則會使用 [**CIM \_ ConcreteJob**](cim-concretejob.md) 實例的傳回參考來監視進度，並取得方法的結果。

</dd> </dl>

## <a name="return-value"></a>傳回值

成功時，會傳回 0 (完成) 或 4096 (作業已啟動) ;否則，會傳回錯誤。

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
| 最低支援的用戶端<br/> | Windows 10 \[僅限桌面應用程式\]<br/>                                                             |
| 最低支援的伺服器<br/> | Windows Server 2016<br/>                                                                          |
| 命名空間<br/>                | 根 \\ 虛擬化 \\ v2<br/>                                                                     |
| MOF<br/>                      | <dl> <dt>WindowsVirtualization。</dt> </dl> |
| DLL<br/>                      | <dl> <dt>Vmms.exe</dt> </dl>                     |



## <a name="see-also"></a>另請參閱

<dl> <dt>

[**Msvm \_ CollectionSnapshotService**](msvm-collectionsnapshotservice.md)
</dt> </dl>

 

 




