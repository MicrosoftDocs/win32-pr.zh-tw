---
title: TaskService. GetFolder 方法
description: 針對腳本，會取得已註冊工作的資料夾。
ms.assetid: 57e5b411-1fb6-4ee1-9802-ed2adbb4fdf8
keywords:
- GetFolder 方法工作排程器
- GetFolder 方法工作排程器，TaskService 物件
- TaskService 物件工作排程器，GetFolder 方法
topic_type:
- apiref
api_name:
- TaskService.GetFolder
api_location:
- taskschd.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 74504e9cad124f8cbc9ec23e896ba4dec7d7f50c
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 12/12/2020
ms.locfileid: "106976980"
---
# <a name="taskservicegetfolder-method"></a>TaskService. GetFolder 方法

針對腳本，會取得已註冊工作的資料夾。

## <a name="syntax"></a>語法


```VB
TaskService.GetFolder( _
  ByVal path _
)
```



## <a name="parameters"></a>參數

<dl> <dt>

*路徑* \[在\]
</dt> <dd>

要抓取之資料夾的路徑。 請勿在路徑中的最後一個資料夾名稱後面使用反斜線。 根工作資料夾是以反斜線 (指定 \) 。 根工作資料夾下的工作資料夾路徑範例是 \\ MyTaskFolder。 '. ' 字元不能用來指定目前的工作資料夾與 ' ... ' 字元不能用來指定路徑中的父工作資料夾。

</dd> </dl>

## <a name="return-value"></a>傳回值

所要求之資料夾的 [**TaskFolder**](taskfolder.md) 物件。

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

 

 





