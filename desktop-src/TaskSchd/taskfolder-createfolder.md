---
title: TaskFolder. CreateFolder 方法
description: 針對腳本，建立相關工作的資料夾。
ms.assetid: 4fdc96bc-8c85-4b36-b3ea-bad7a46c3d35
keywords:
- CreateFolder 方法工作排程器
- CreateFolder 方法工作排程器，TaskFolder 物件
- TaskFolder 物件工作排程器，CreateFolder 方法
topic_type:
- apiref
api_name:
- TaskFolder.CreateFolder
api_location:
- taskschd.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 2a5de913ccf98ee8369430425e423813168c083cbde737b5831917a5ee594e1a
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/11/2021
ms.locfileid: "117759018"
---
# <a name="taskfoldercreatefolder-method"></a>TaskFolder. CreateFolder 方法

針對腳本，建立相關工作的資料夾。

## <a name="syntax"></a>語法


```VB
ppFolder = .CreateFolder( _
  ByVal folderName, _
  ByVal sddl _
)
```



## <a name="parameters"></a>參數

<dl> <dt>

*資料夾資料夾* \[在\]
</dt> <dd>

用來識別資料夾的名稱。 如果指定了 " \\ SubFolder1 \\ SubFolder2"，則如果資料夾不存在，就會建立整個資料夾樹狀結構。 這個參數可以是目前 [**TaskFolder**](taskfolder.md) 實例的相對路徑。 根工作資料夾是以反斜線 () 指定 \\ 。 根工作資料夾下的工作資料夾路徑範例是 \\ MyTaskFolder。 '. ' 字元不能用來指定目前的工作資料夾與 ' ... ' 字元不能用來指定路徑中的父工作資料夾。

</dd> <dt>

*sddl* \[在\]
</dt> <dd>

與資料夾相關聯的安全描述項。

</dd> </dl>

## <a name="return-value"></a>傳回值

[**TaskFolder**](taskfolder.md)物件，表示新的子資料夾。

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

 

 





