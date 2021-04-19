---
title: TaskService. NewTask 方法
description: 針對腳本，會傳回空的工作定義物件，以使用設定和屬性填入，然後使用 TaskFolder. RegisterTaskDefinition 方法進行註冊。
ms.assetid: 696d57fc-100a-43e6-a8d9-9ec89be40367
keywords:
- NewTask 方法工作排程器
- NewTask 方法工作排程器，TaskService 物件
- TaskService 物件工作排程器，NewTask 方法
topic_type:
- apiref
api_name:
- TaskService.NewTask
api_location:
- taskschd.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 4f5f10ce90861c76d0a751c54e8282269b7a8986
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 12/12/2020
ms.locfileid: "106966153"
---
# <a name="taskservicenewtask-method"></a>TaskService. NewTask 方法

針對腳本，會傳回空的工作定義物件，以使用設定和屬性填入，然後使用 [**TaskFolder. RegisterTaskDefinition**](taskfolder-registertaskdefinition.md) 方法進行註冊。

## <a name="syntax"></a>語法


```VB
TaskService.NewTask( _
  ByVal flags _
)
```



## <a name="parameters"></a>參數

<dl> <dt>

*旗標* \[在\]
</dt> <dd>

此參數會保留供日後使用，且必須設定為0。

</dd> </dl>

## <a name="return-value"></a>傳回值

指定建立新工作所需之所有資訊的工作定義。

## <a name="requirements"></a>規格需求



| 需求 | 值 |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| 最低支援的用戶端<br/> | \[僅限 Windows Vista 桌面應用程式\]<br/>                                          |
| 最低支援的伺服器<br/> | 僅限 Windows Server 2008 \[ desktop 應用程式\]<br/>                                    |
| 類型程式庫<br/>             | <dl> <dt>Taskschd.msc .tlb</dt> </dl> |
| DLL<br/>                      | <dl> <dt>Taskschd.dll</dt> </dl> |



 

 





