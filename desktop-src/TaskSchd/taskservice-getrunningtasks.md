---
title: TaskService. GetRunningTasks 方法
description: 針對腳本，會取得正在執行之工作的集合。
ms.assetid: bae3c035-a6b2-4ca5-970b-d4bc808068ad
keywords:
- GetRunningTasks 方法工作排程器
- GetRunningTasks 方法工作排程器，TaskService 物件
- TaskService 物件工作排程器，GetRunningTasks 方法
topic_type:
- apiref
api_name:
- TaskService.GetRunningTasks
api_location:
- taskschd.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: dec585b9ed46af9a283e337c8f200687c512cd36
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 12/12/2020
ms.locfileid: "103686547"
---
# <a name="taskservicegetrunningtasks-method"></a>TaskService. GetRunningTasks 方法

針對腳本，會取得正在執行之工作的集合。

> [!Note]  
> **TaskService** 只會傳回執行中工作的集合，而這些工作是在使用者的安全性內容中執行。 例如，針對 Administrators 群組的成員， **GetRunningTasks** 會傳回所有執行中工作的集合，但是針對 users 群組的成員， **GetRunningTasks** 只會傳回在 users 群組安全性內容下執行的工作集合。

 

## <a name="syntax"></a>語法


```VB
TaskService.GetRunningTasks( _
  ByVal flags _
)
```



## <a name="parameters"></a>參數

<dl> <dt>

*旗標* \[在\]
</dt> <dd>

傳入1以傳回所有執行中的工作，包括隱藏的工作。 傳入0以傳回非隱藏工作的執行中工作集合。

</dd> </dl>

## <a name="return-value"></a>傳回值

包含目前正在執行之工作的 [**RunningTaskCollection**](runningtaskcollection.md) 物件。

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
</dt> </dl>

 

 





