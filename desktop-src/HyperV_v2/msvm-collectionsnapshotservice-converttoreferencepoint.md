---
description: 將現有的集合快照集轉換為參考點集合。 快照集集合被刪除為副作用。 只有修復快照集可以轉換成參考點。
ms.assetid: 6b304782-9e5e-43b1-af7d-08617d65850c
title: Msvm_CollectionSnapshotService 類別的 ConvertToReferencePoint 方法
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Msvm_CollectionSnapshotService.ConvertToReferencePoint
api_type:
- COM
api_location:
- vmms.exe
ms.openlocfilehash: 97faedea1cdb852e26f6b94211586e5539075c0a225bf98f1a10cf45305d7296
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/11/2021
ms.locfileid: "118148864"
---
# <a name="converttoreferencepoint-method-of-the-msvm_collectionsnapshotservice-class"></a>Msvm CollectionSnapshotService 類別的 ConvertToReferencePoint 方法 \_

將現有的集合快照集轉換為參考點集合。 快照集集合被刪除為副作用。 只有修復快照集可以轉換成參考點。

## <a name="syntax"></a>語法


```mof
uint32 ConvertToReferencePoint(
  [in]      Msvm_SnapshotCollection       REF AffectedSnapshotCollection,
  [in, out] Msvm_ReferencePointCollection REF ResultingReferencePointCollection,
  [out]     CIM_ConcreteJob               REF Job
);
```



## <a name="parameters"></a>參數

<dl> <dt>

*AffectedSnapshotCollection* \[在\]
</dt> <dd>

參考包含受影響之虛擬系統快照集集合的 [**Msvm \_ SnapshotCollection**](msvm-snapshotcollection.md) 。

</dd> <dt>

*ResultingReferencePointCollection* \[in、out\]
</dt> <dd>

[**Msvm \_ ReferencePointCollection**](msvm-referencepointcollection.md)的參考，其中包含產生的虛擬系統參考點集合

</dd> <dt>

*作業* \[擴展\]
</dt> <dd>

如果作業的執行時間很長，則可以選擇性地傳回作業。

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

 

 




