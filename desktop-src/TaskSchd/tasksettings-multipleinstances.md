---
title: TaskSettings. MultipleInstances 屬性
description: 針對腳本，取得或設定原則，以定義工作排程器處理工作之多個實例的方式。
ms.assetid: a25be615-fbb9-47fe-805a-5b93eab95f47
keywords:
- MultipleInstances 屬性工作排程器
- MultipleInstances 屬性工作排程器，TaskSettings 物件
- TaskSettings 物件工作排程器、MultipleInstances 屬性
topic_type:
- apiref
api_name:
- TaskSettings.MultipleInstances
api_location:
- taskschd.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 2ff0091b9051840fea4c37869b51902f0c5f4c7cfed43a47c4f3924b398fe3e3
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/11/2021
ms.locfileid: "119059686"
---
# <a name="tasksettingsmultipleinstances-property"></a>TaskSettings. MultipleInstances 屬性

針對腳本，取得或設定原則，以定義工作排程器處理工作之多個實例的方式。

這是可讀寫的屬性。

## <a name="syntax"></a>Syntax


```VB
TaskSettings.MultipleInstances As Integer
```



## <a name="property-value"></a>屬性值

[**工作 \_實例 \_ 原則**](/windows/desktop/api/taskschd/ne-taskschd-task_instances_policy) 常數。



| 值                                                                                                                                                                                                                                                               | 意義                                                                                          |
|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|--------------------------------------------------------------------------------------------------|
| <span id="TASK_INSTANCES_PARALLEL"></span><span id="task_instances_parallel"></span><dl> <dt>**工作 \_實例 \_ 平行**</dt> <dt>0</dt> </dl>                 | 當工作的現有實例正在執行時，啟動新的實例。<br/>              |
| <span id="TASK_INSTANCES_QUEUE"></span><span id="task_instances_queue"></span><dl> <dt>**工作 \_實例 \_ 佇列**</dt> <dt>1</dt> </dl>                          | 在工作的所有其他實例完成之後，啟動工作的新實例。<br/> |
| <span id="TASK_INSTANCES_IGNORE_NEW"></span><span id="task_instances_ignore_new"></span><dl> <dt>**工作 \_實例 \_ 忽略 \_ 新**</dt>的 <dt>2</dt> </dl>          | 如果工作的現有實例正在執行，則不會啟動新的實例。<br/>         |
| <span id="TASK_INSTANCES_STOP_EXISTING"></span><span id="task_instances_stop_existing"></span><dl> <dt>**工作 \_實例 \_ 停止 \_ 現有**</dt>的 <dt>3</dt> </dl> | 停止工作的現有實例，然後再啟動新的實例。<br/>                 |



 

## <a name="remarks"></a>備註

讀取或寫入工作的 XML 時，此設定會在工作排程器架構的 [**MultipleInstancesPolicy**](taskschedulerschema-multipleinstancespolicy-settingstype-element.md) 元素中指定。

## <a name="requirements"></a>規格需求



| 需求 | 值 |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| 最低支援的用戶端<br/> | Windows\[僅限 Vista desktop 應用程式\]<br/>                                          |
| 最低支援的伺服器<br/> | Windows\[僅限 Server 2008 desktop 應用程式\]<br/>                                    |
| 類型程式庫<br/>             | <dl> <dt>Taskschd.msc .tlb</dt> </dl> |
| DLL<br/>                      | <dl> <dt>Taskschd.dll</dt> </dl> |



## <a name="see-also"></a>另請參閱

<dl> <dt>

[**工作 \_ 實例 \_ 原則**](/windows/desktop/api/taskschd/ne-taskschd-task_instances_policy)
</dt> <dt>

[工作排程器](task-scheduler-start-page.md)
</dt> </dl>

 

 





