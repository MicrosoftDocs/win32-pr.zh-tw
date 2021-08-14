---
title: TaskNamedValueCollection 物件
description: 腳本物件，其中包含 TaskNamedValuePair 物件名稱/值組的集合。
ms.assetid: 4cc7ce8a-a352-4092-b001-071f9c5cd864
keywords:
- TaskNamedValueCollection 物件工作排程器
- TaskNamedValueCollection 物件工作排程器，說明
topic_type:
- apiref
api_name:
- TaskNamedValueCollection
api_location:
- taskschd.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 297b52df30c7b17190e91e323f104f0e8df68bed751b28264603e9ca5135dbd9
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/11/2021
ms.locfileid: "118357465"
---
# <a name="tasknamedvaluecollection-object"></a>TaskNamedValueCollection 物件

腳本物件，其中包含 [**TaskNamedValuePair**](tasknamedvaluepair.md) 物件名稱/值組的集合。

## <a name="members"></a>成員

**TaskNamedValueCollection** 物件具有下列類型的成員：

-   [方法](#methods)
-   [屬性](#properties)

### <a name="methods"></a>方法

**TaskNamedValueCollection** 物件有這些方法。



| 方法                                            | 描述                                                        |
|:--------------------------------------------------|:-------------------------------------------------------------------|
| [**清除**](tasknamedvaluecollection-clear.md)   | 清除整個名稱/值組的集合。<br/>       |
| [**建立**](tasknamedvaluecollection-create.md) | 在集合中建立成對的名稱/值。<br/>            |
| [**移除**](tasknamedvaluecollection-remove.md) | 從集合中移除選取的名稱/值組。<br/> |



 

### <a name="properties"></a>屬性

**TaskNamedValueCollection** 物件具有這些屬性。



| 屬性                                                   | 描述                                                        |
|:-----------------------------------------------------------|:-------------------------------------------------------------------|
| [**計數**](tasknamedvaluecollection-count.md)<br/> | 取得集合中的名稱/值組數目。<br/>  |
| [**項目**](tasknamedvaluecollection-item.md)<br/>   | 從集合中取得指定的名稱/值組。<br/> |



 

## <a name="requirements"></a>規格需求



| 需求 | 值 |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| 最低支援的用戶端<br/> | Windows\[僅限 Vista desktop 應用程式\]<br/>                                          |
| 最低支援的伺服器<br/> | Windows\[僅限 Server 2008 desktop 應用程式\]<br/>                                    |
| 類型程式庫<br/>             | <dl> <dt>Taskschd.msc .tlb</dt> </dl> |
| DLL<br/>                      | <dl> <dt>Taskschd.dll</dt> </dl> |



## <a name="see-also"></a>另請參閱

<dl> <dt>

[**EventTrigger. ValueQueries**](eventtrigger-valuequeries.md)
</dt> <dt>

[**EmailAction.HeaderFields**](emailaction-headerfields.md)
</dt> </dl>

 

 





