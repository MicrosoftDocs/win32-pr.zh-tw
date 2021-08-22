---
description: 終結現有的參考點集合。 這個方法可能會損毀其他相依于受影響之參考點集合的參考點。
ms.assetid: 72c116f4-f844-494c-96ea-e97c49a2af7e
title: Msvm_CollectionReferencePointService 類別的 DestroyReferencePoint 方法
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Msvm_CollectionReferencePointService.DestroyReferencePoint
api_type:
- COM
api_location:
- vmms.exe
ms.openlocfilehash: 95745646c410c2752f146fc05042b26215f41ef23d3637701497ad565e06583c
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/11/2021
ms.locfileid: "119531988"
---
# <a name="destroyreferencepoint-method-of-the-msvm_collectionreferencepointservice-class"></a>Msvm CollectionReferencePointService 類別的 DestroyReferencePoint 方法 \_

終結現有的參考點集合。 這個方法可能會損毀其他相依于受影響之參考點集合的參考點。

## <a name="syntax"></a>語法


```mof
uint32 DestroyReferencePoint(
  [in]  CIM_Collection  REF AffectedReferencePointCollection,
  [out] CIM_ConcreteJob REF Job
);
```



## <a name="parameters"></a>參數

<dl> <dt>

*AffectedReferencePointCollection* \[在\]
</dt> <dd>

參考受影響的虛擬系統參考點集合。

</dd> <dt>

*作業* \[擴展\]
</dt> <dd>

如果作業的執行時間很長，則可以選擇性地傳回作業。

</dd> </dl>

## <a name="return-value"></a>傳回值

如果成功，則會傳回 0 (沒有錯誤) ，或 4096 (作業已啟動) ;否則，會傳回錯誤。

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

[**Msvm \_ CollectionReferencePointService**](msvm-collectionreferencepointservice.md)
</dt> </dl>

 

 




