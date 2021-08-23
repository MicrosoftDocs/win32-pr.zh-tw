---
description: 將快照集集合套用至虛擬電腦系統的集合。
ms.assetid: c76c552a-ae07-4dab-a938-740d77447a53
title: Msvm_CollectionSnapshotService 類別的 ApplySnapshot 方法
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Msvm_CollectionSnapshotService.ApplySnapshot
api_type:
- COM
api_location:
- vmms.exe
ms.openlocfilehash: f4dd36db457099aaa9c134593fa385f21480e036e15629d10c32e716e604a462
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/11/2021
ms.locfileid: "119426928"
---
# <a name="applysnapshot-method-of-the-msvm_collectionsnapshotservice-class"></a>Msvm CollectionSnapshotService 類別的 ApplySnapshot 方法 \_

將快照集集合套用至虛擬電腦系統的集合。

## <a name="syntax"></a>語法


```mof
uint32 ApplySnapshot(
  [in]  CIM_Collection  REF SnapshotCollection,
  [out] CIM_ConcreteJob REF Job
);
```



## <a name="parameters"></a>參數

<dl> <dt>

*SnapshotCollection* \[在\]
</dt> <dd>

[**CIM \_ 集合**](cim-collection.md)的參考，代表要套用的快照集集合。

</dd> <dt>

*作業* \[擴展\]
</dt> <dd>

如果以非同步方式執行作業，則會傳回選擇性的參考。 如果有，則會使用 [**CIM \_ ConcreteJob**](cim-concretejob.md) 實例的傳回參考來監視進度，並取得方法的結果。

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
| 最低支援的用戶端<br/> | Windows 10， \[ 僅限1703版桌面應用程式\]<br/>                                               |
| 最低支援的伺服器<br/> | Windows Server 2016<br/>                                                                          |
| 命名空間<br/>                | 根 \\ 虛擬化 \\ v2<br/>                                                                     |
| MOF<br/>                      | <dl> <dt>WindowsVirtualization。</dt> </dl> |
| DLL<br/>                      | <dl> <dt>Vmms.exe</dt> </dl>                     |



## <a name="see-also"></a>另請參閱

<dl> <dt>

[**Msvm \_ CollectionSnapshotService**](msvm-collectionsnapshotservice.md)
</dt> </dl>

 

 




