---
title: RegisteredTask. NextRunTime 屬性
description: 針對腳本，取得下次排程執行的已註冊工作的時間。
ms.assetid: f63298a8-c9fa-4fea-ad0b-2c8739aced19
keywords:
- NextRunTime 屬性工作排程器
- NextRunTime 屬性工作排程器，RegisteredTask 物件
- RegisteredTask 物件工作排程器、NextRunTime 屬性
topic_type:
- apiref
api_name:
- RegisteredTask.NextRunTime
api_location:
- taskschd.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 850c0215555fd24b729b1d71acaff9fa7083c0f53289f28e4228b8e57ff40e52
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/11/2021
ms.locfileid: "119060046"
---
# <a name="registeredtasknextruntime-property"></a>RegisteredTask. NextRunTime 屬性

針對腳本，取得下次排程執行的已註冊工作的時間。

## <a name="syntax"></a>Syntax


```VB
RegisteredTask.NextRunTime As String
```



## <a name="property-value"></a>屬性值

下次排定要執行的已註冊工作時間。

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

 

 





