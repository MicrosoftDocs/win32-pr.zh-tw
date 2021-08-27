---
title: TaskSettings. RestartCount 屬性
description: 針對腳本，取得或設定工作排程器將嘗試重新開機工作的次數。
ms.assetid: 7d92c2c6-e846-4664-b22a-b2a6ca46c225
keywords:
- RestartCount 屬性工作排程器
- RestartCount 屬性工作排程器，TaskSettings 物件
- TaskSettings 物件工作排程器、RestartCount 屬性
topic_type:
- apiref
api_name:
- TaskSettings.RestartCount
api_location:
- taskschd.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: a3a34e8eef84575548998e39ab47bc5492baca368f7012d5fa096c831539ceb7
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/11/2021
ms.locfileid: "120072408"
---
# <a name="tasksettingsrestartcount-property"></a>TaskSettings. RestartCount 屬性

針對腳本，取得或設定工作排程器將嘗試重新開機工作的次數。

這是可讀寫的屬性。

## <a name="syntax"></a>Syntax


```VB
TaskSettings.RestartCount As Integer
```



## <a name="property-value"></a>屬性值

工作排程器將嘗試重新開機工作的次數。

## <a name="remarks"></a>備註

讀取或寫入工作的 XML 時，此設定會在工作排程器架構的 [**Count**](taskschedulerschema-count-restarttype-element.md) 元素中指定。

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

 

 





