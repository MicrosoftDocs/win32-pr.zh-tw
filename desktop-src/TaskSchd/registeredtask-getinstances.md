---
title: RegisteredTask. GetInstances 方法
description: 針對腳本，會傳回已註冊工作的所有目前執行中實例。
ms.assetid: 01fea94e-fdec-4edf-886a-f6d9b566f201
keywords:
- GetInstances 方法工作排程器
- GetInstances 方法工作排程器，RegisteredTask 物件
- RegisteredTask 物件工作排程器，GetInstances 方法
topic_type:
- apiref
api_name:
- RegisteredTask.GetInstances
api_location:
- taskschd.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 78b1579df1124fcd6d26ea658730190b5eb0f5de
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 12/12/2020
ms.locfileid: "104105245"
---
# <a name="registeredtaskgetinstances-method"></a>RegisteredTask. GetInstances 方法

針對腳本，會傳回已註冊工作的所有目前執行中實例。

> [!Note]  
> **RegisteredTask** 只會傳回目前正在執行之已註冊工作的實例，該工作是在使用者的安全性內容中執行。 例如，針對 Administrators 群組的成員， **GetInstances** 會傳回目前正在執行之已註冊工作的所有實例，但是針對 users 群組的成員， **GetInstances** 只會傳回目前正在執行之已註冊工作的實例，該工作是在 users 群組的安全性內容下執行。

 

## <a name="syntax"></a>語法


```VB
RegisteredTask.GetInstances( _
  ByVal flags, _
  ByRef runningTasks _
)
```



## <a name="parameters"></a>參數

<dl> <dt>

*flags* 
</dt> <dd>

此參數會保留供日後使用，且必須設定為0。

</dd> <dt>

*runningTasks* \[擴展\]
</dt> <dd>

[**RunningTaskCollection**](runningtaskcollection.md)物件，其中包含目前正在執行之工作的所有實例。

</dd> </dl>

## <a name="return-value"></a>傳回值

這個方法不會傳回值。

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

[**RegisteredTask**](registeredtask.md)
</dt> </dl>

 

 





