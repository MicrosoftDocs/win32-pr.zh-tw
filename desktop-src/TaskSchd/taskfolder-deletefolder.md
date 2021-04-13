---
title: TaskFolder. DeleteFolder 方法
description: 針對腳本，會從父資料夾刪除子資料夾。
ms.assetid: 0d6a9a60-7909-4945-8186-3495e6fe9bc4
keywords:
- DeleteFolder 方法工作排程器
- DeleteFolder 方法工作排程器，TaskFolder 物件
- TaskFolder 物件工作排程器，DeleteFolder 方法
topic_type:
- apiref
api_name:
- TaskFolder.DeleteFolder
api_location:
- taskschd.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 6ea9b8aaa7da7710cedc49e10d6be2a203f62b34
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 12/12/2020
ms.locfileid: "104465817"
---
# <a name="taskfolderdeletefolder-method"></a>TaskFolder. DeleteFolder 方法

針對腳本，會從父資料夾刪除子資料夾。

## <a name="syntax"></a>語法


```VB
TaskFolder.DeleteFolder( _
  ByVal folderName, _
  ByVal flags _
)
```



## <a name="parameters"></a>參數

<dl> <dt>

*資料夾資料夾* \[在\]
</dt> <dd>

要移除之子資料夾的名稱。 根工作資料夾是以反斜線 (指定 \) 。 這個參數可以是您想要刪除之資料夾的相對路徑。 根工作資料夾下的工作資料夾路徑範例是 \\ MyTaskFolder。 '. ' 字元不能用來指定目前的工作資料夾與 ' ... ' 字元不能用來指定路徑中的父工作資料夾。

</dd> <dt>

*旗標* \[在\]
</dt> <dd>

不支援。

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

[**TaskFolder**](taskfolder.md)
</dt> <dt>

[工作排程器](task-scheduler-start-page.md)
</dt> </dl>

 

 





