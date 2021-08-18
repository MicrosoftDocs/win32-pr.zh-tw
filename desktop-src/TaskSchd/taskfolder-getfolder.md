---
title: TaskFolder. GetFolder 屬性
description: 針對腳本，取得包含指定位置之工作的資料夾。
ms.assetid: 73e60b10-7a8c-4b07-9f8c-be7715f4e032
keywords:
- GetFolder 屬性工作排程器
- GetFolder 屬性工作排程器，TaskFolder 物件
- TaskFolder 物件工作排程器、GetFolder 屬性
topic_type:
- apiref
api_name:
- TaskFolder.GetFolder
api_location:
- taskschd.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 7668b2486a316fe2bf799762401459ec7da2602ff52a4d5d3dc9ddb4dd888e61
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/11/2021
ms.locfileid: "117758981"
---
# <a name="taskfoldergetfolder-property"></a>TaskFolder. GetFolder 屬性

針對腳本，取得包含指定位置之工作的資料夾。

## <a name="syntax"></a>Syntax


```VB
TaskFolder.GetFolder( _
  ByVal path _
)
```



## <a name="property-value"></a>屬性值

資料夾) 路徑 (位置。 請勿在路徑中的最後一個資料夾名稱後面使用反斜線。 根工作資料夾是以反斜線 () 指定 \\ 。 根工作資料夾下的工作資料夾路徑範例是 \\ MyTaskFolder。 '. ' 字元不能用來指定目前的工作資料夾與 ' ... ' 字元不能用來指定路徑中的父工作資料夾。

## <a name="error-codes"></a>錯誤碼

位於指定位置的資料夾。 資料夾是 [**TaskFolder**](taskfolder.md) 物件。

## <a name="requirements"></a>規格需求



| 需求 | 值 |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| 最低支援的用戶端<br/> | Windows\[僅限 Vista desktop 應用程式\]<br/>                                          |
| 最低支援的伺服器<br/> | Windows\[僅限 Server 2008 desktop 應用程式\]<br/>                                    |
| 類型程式庫<br/>             | <dl> <dt>Taskschd.msc .tlb</dt> </dl> |
| DLL<br/>                      | <dl> <dt>Taskschd.dll</dt> </dl> |



 

 





