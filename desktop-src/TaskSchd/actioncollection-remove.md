---
title: Actioncollection 動作方法
description: 針對腳本，會從集合中移除指定的動作。
ms.assetid: ae1da6a9-5851-4ccb-80dc-75d7a99e7c6a
keywords:
- 移除方法工作排程器
- Remove 方法工作排程器，Actioncollection 動作物件
- Actioncollection 動作物件工作排程器、Remove 方法
topic_type:
- apiref
api_name:
- ActionCollection.Remove
api_location:
- taskschd.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: e110f870f4f192051b47cb3b65f0ebb41a490708
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 12/12/2020
ms.locfileid: "103686148"
---
# <a name="actioncollectionremove-method"></a>Actioncollection 動作方法

針對腳本，會從集合中移除指定的動作。

## <a name="syntax"></a>語法


```VB
ActionCollection.Remove( _
  ByVal index _
)
```



## <a name="parameters"></a>參數

<dl> <dt>

*索引* \[在\]
</dt> <dd>

要移除之動作的索引。

</dd> </dl>

## <a name="return-value"></a>傳回值

這個方法不會傳回值。

## <a name="remarks"></a>備註

移除專案時，請注意集合中第一個專案的索引是1，而最後一個專案的索引是 [**Actioncollection 動作計數**](actioncollection-count.md) 屬性的值。

## <a name="requirements"></a>規格需求



| 需求 | 值 |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| 最低支援的用戶端<br/> | \[僅限 Windows Vista 桌面應用程式\]<br/>                                          |
| 最低支援的伺服器<br/> | 僅限 Windows Server 2008 \[ desktop 應用程式\]<br/>                                    |
| 類型程式庫<br/>             | <dl> <dt>Taskschd.msc .tlb</dt> </dl> |
| DLL<br/>                      | <dl> <dt>Taskschd.dll</dt> </dl> |



## <a name="see-also"></a>另請參閱

<dl> <dt>

[工作排程器](task-scheduler-start-page.md)
</dt> <dt>

[**Actioncollection 動作**](actioncollection.md)
</dt> </dl>

 

 





