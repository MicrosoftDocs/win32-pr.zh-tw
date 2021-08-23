---
description: 刪除指定的 CIM \_ CollectionOfMSEs 物件。
ms.assetid: 2c79e281-44c3-4a91-98d5-fdf973d149c3
title: Msvm_CollectionManagementService 類別的 DestroyCollection 方法
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Msvm_CollectionManagementService.DestroyCollection
api_type:
- COM
api_location:
- vmms.exe
ms.openlocfilehash: 5d85e566d1d33b17e7873a6da225f3c199bf49425cf081646aba251f87cf7ca6
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/11/2021
ms.locfileid: "119427048"
---
# <a name="destroycollection-method-of-the-msvm_collectionmanagementservice-class"></a>Msvm CollectionManagementService 類別的 DestroyCollection 方法 \_

刪除指定的 [**CIM \_ CollectionOfMSEs**](cim-collectionofmses.md) 物件。

## <a name="syntax"></a>語法


```mof
uint32 DestroyCollection(
  [in]  CIM_CollectionOfMSEs REF Collection,
  [out] CIM_ConcreteJob      REF Job
);
```



## <a name="parameters"></a>參數

<dl> <dt>

*集合* \[在\]
</dt> <dd>

要終結的集合。

</dd> <dt>

*作業* \[擴展\]
</dt> <dd>

如果工作已完成) ，則作業 (的參考可以是 null。

</dd> </dl>

## <a name="return-value"></a>傳回值

如果成功，則傳回 0; 如果作業已啟動，則傳回 4096;否則，會傳回錯誤。

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
| 最低支援的用戶端<br/> | Windows 10 \[僅限桌面應用程式\]<br/>                                                             |
| 最低支援的伺服器<br/> | Windows Server 2016<br/>                                                                          |
| 命名空間<br/>                | 根 \\ 虛擬化 \\ v2<br/>                                                                     |
| MOF<br/>                      | <dl> <dt>WindowsVirtualization。</dt> </dl> |
| DLL<br/>                      | <dl> <dt>Vmms.exe</dt> </dl>                     |



## <a name="see-also"></a>另請參閱

<dl> <dt>

[**Msvm \_ CollectionManagementService**](msvm-collectionmanagementservice.md)
</dt> </dl>

 

 




