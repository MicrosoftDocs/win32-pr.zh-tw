---
title: TriggerCollection 方法
description: 針對腳本，從工作所用的觸發程式集合中移除指定的觸發程式。
ms.assetid: 30dccf16-2b4c-4776-9c19-f82ddd859d45
keywords:
- 觸發程式工作排程器，移除
- 移除方法工作排程器
- Remove 方法工作排程器，TriggerCollection 物件
- TriggerCollection 物件工作排程器、Remove 方法
topic_type:
- apiref
api_name:
- TriggerCollection.Remove
api_location:
- taskschd.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: d1ff3fda5119f4b487ba7f04546ea94e0a601a4749e1aa6aad7a9120907cd6cc
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/11/2021
ms.locfileid: "120099640"
---
# <a name="triggercollectionremove-method"></a>TriggerCollection 方法

針對腳本，從工作所用的觸發程式集合中移除指定的觸發程式。

## <a name="syntax"></a>語法


```VB
TriggerCollection.Remove( _
  ByVal index _
)
```



## <a name="parameters"></a>參數

<dl> <dt>

*索引* \[在\]
</dt> <dd>

要移除之觸發程式的索引。

</dd> </dl>

## <a name="return-value"></a>傳回值

這個方法不會傳回值。

## <a name="remarks"></a>備註

移除專案時，請注意集合中第一個專案的索引是1，而最後一個專案的索引是 [**TriggerCollection 計數**](triggercollection-count.md) 屬性的值。

## <a name="requirements"></a>規格需求



| 需求 | 值 |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| 最低支援的用戶端<br/> | Windows\[僅限 Vista desktop 應用程式\]<br/>                                          |
| 最低支援的伺服器<br/> | Windows\[僅限 Server 2008 desktop 應用程式\]<br/>                                    |
| 類型程式庫<br/>             | <dl> <dt>Taskschd.msc .tlb</dt> </dl> |
| DLL<br/>                      | <dl> <dt>Taskschd.dll</dt> </dl> |



## <a name="see-also"></a>另請參閱

<dl> <dt>

[工作排程器](task-scheduler-start-page.md)
</dt> </dl>

 

 





