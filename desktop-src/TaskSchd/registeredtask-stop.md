---
title: RegisteredTask. Stop 方法
description: 若為腳本，請立即停止已註冊的工作。
ms.assetid: e4a533d8-5cf0-46ba-a603-f7a9c59ab0fd
keywords:
- Stop 方法工作排程器
- Stop 方法工作排程器，RegisteredTask 物件
- RegisteredTask 物件工作排程器，Stop 方法
topic_type:
- apiref
api_name:
- RegisteredTask.Stop
api_location:
- taskschd.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 0496a3b9c8adad0ad4095b6c8aed3888940fd699750350117f4bf503c442f4c8
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/11/2021
ms.locfileid: "119681658"
---
# <a name="registeredtaskstop-method"></a>RegisteredTask. Stop 方法

若為腳本，請立即停止已註冊的工作。

## <a name="syntax"></a>語法


```VB
RegisteredTask.Stop( _
  ByVal flags _
)
```



## <a name="parameters"></a>參數

<dl> <dt>

*旗標* \[在\]
</dt> <dd>

保留的。 必須為零。

</dd> </dl>

## <a name="return-value"></a>傳回值

這個方法不會傳回值。

## <a name="remarks"></a>備註

**RegisteredTask** 停止函式會停止工作的所有實例。

系統帳戶使用者可以停止工作，具有系統管理員群組許可權的使用者可以停止工作，且如果使用者有權執行和讀取工作，則使用者可以停止工作。 使用者可以停止在與使用者帳戶相同的認證下執行的工作實例。 在所有其他情況下，使用者會被拒絕存取來停止工作。

## <a name="requirements"></a>規格需求



| 需求 | 值 |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| 最低支援的用戶端<br/> | Windows\[僅限 Vista desktop 應用程式\]<br/>                                          |
| 最低支援的伺服器<br/> | Windows\[僅限 Server 2008 desktop 應用程式\]<br/>                                    |
| 類型程式庫<br/>             | <dl> <dt>Taskschd.msc .tlb</dt> </dl> |
| DLL<br/>                      | <dl> <dt>Taskschd.dll</dt> </dl> |



## <a name="see-also"></a>另請參閱

<dl> <dt>

[**RegisteredTask**](registeredtask.md)
</dt> </dl>

 

 





