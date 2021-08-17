---
title: RegisteredTask. GetRunTimes 方法
description: 針對腳本，取得已註冊的工作排定在指定時間執行的時間。
ms.assetid: fc3d93eb-3186-419f-9f6f-7d54f8ade1ad
keywords:
- GetRunTimes 方法工作排程器
- GetRunTimes 方法工作排程器，RegisteredTask 物件
- RegisteredTask 物件工作排程器，GetRunTimes 方法
topic_type:
- apiref
api_name:
- RegisteredTask.GetRunTimes
api_location:
- taskschd.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 303dd08c576f31946207241b086fe945b3f1ac275c596496139d19f507670e30
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/11/2021
ms.locfileid: "117759663"
---
# <a name="registeredtaskgetruntimes-method"></a>RegisteredTask. GetRunTimes 方法

針對腳本，取得已註冊的工作排定在指定時間執行的時間。

## <a name="syntax"></a>語法


```VB
RegisteredTask.GetRunTimes( _
  ByVal begin, _
  ByVal end, _
  ByRef count, _
  ByRef rgstTaskTimes _
)
```



## <a name="parameters"></a>參數

<dl> <dt>

*開始* \[在\]
</dt> <dd>

查詢的開始時間。

</dd> <dt>

*結束* \[在\]
</dt> <dd>

查詢的結束時間。

</dd> <dt>

*計數* \[擴展\]
</dt> <dd>

工作將執行的排程時間數目。

</dd> <dt>

*rgstTaskTimes* \[擴展\]
</dt> <dd>

工作將執行的排程時間。

</dd> </dl>

## <a name="return-value"></a>傳回值

這個方法不會傳回值。

## <a name="remarks"></a>備註

如果已註冊的工作包含個別停用的觸發程式，這些觸發程式仍會影響下一次所傳回的排程執行時間（即使已停用）。

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

[**RegisteredTask**](registeredtask.md)
</dt> </dl>

 

 





