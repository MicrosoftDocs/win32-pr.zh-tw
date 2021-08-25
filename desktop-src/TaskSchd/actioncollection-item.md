---
title: Actioncollection 動作專案屬性
description: 針對腳本，從集合取得指定的動作。
ms.assetid: a5567c82-2d56-4c3e-894c-ca6d432a3358
keywords:
- Item 屬性工作排程器
- 專案屬性工作排程器，Actioncollection 動作物件
- Actioncollection 動作物件工作排程器，Item 屬性
topic_type:
- apiref
api_name:
- ActionCollection.Item
api_location:
- taskschd.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: fff95b707a4a99ce54cba4d175ce9fd094f7a6bd400147d7942a42a39d65bb7f
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/11/2021
ms.locfileid: "119796638"
---
# <a name="actioncollectionitem-property"></a>Actioncollection 動作專案屬性

針對腳本，從集合取得指定的動作。

## <a name="syntax"></a>Syntax


```VB
ActionCollection.Item( _
  ByVal Index _
) As Action
```



## <a name="property-value"></a>屬性值

代表所要求之動作的 [**動作**](action.md) 物件。

## <a name="remarks"></a>備註

集合以1為基礎。 換句話說，集合中第一個專案的索引為1。

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
</dt> <dt>

[**Actioncollection 動作**](actioncollection.md)
</dt> </dl>

 

 





