---
title: TaskFolder. GetTask 屬性
description: 針對腳本，取得資料夾中位於指定位置的工作。
ms.assetid: c0ad4402-dd63-499f-964c-0eada5665d1b
keywords:
- GetTask 屬性工作排程器
- GetTask 屬性工作排程器，TaskFolder 物件
- TaskFolder 物件工作排程器、GetTask 屬性
topic_type:
- apiref
api_name:
- TaskFolder.GetTask
api_location:
- taskschd.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: b697b8fa2d0715dcf0282c5f32490bfccec79fec
ms.sourcegitcommit: cb87082135319cbdc5df541e3071eebb83a58972
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 06/04/2021
ms.locfileid: "111387674"
---
# <a name="taskfoldergettask-property"></a>TaskFolder. GetTask 屬性

針對腳本，取得資料夾中位於指定位置的工作。

## <a name="syntax"></a>Syntax


```VB
TaskFolder.GetTask( _
  ByVal path _
)
```



## <a name="property-value"></a>屬性值

路徑 (位置) 至資料夾中的工作。 根工作資料夾是以反斜線 () 指定 \\ 。 根工作資料夾下的工作資料夾路徑範例是 \\ MyTaskFolder。 '. ' 字元不能用來指定目前的工作資料夾與 ' ... ' 字元不能用來指定路徑中的父工作資料夾。

## <a name="error-codes"></a>錯誤碼

指定位置的工作。 此工作是 [**RegisteredTask**](registeredtask.md) 物件。

## <a name="requirements"></a>規格需求



| 需求 | 值 |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| 最低支援的用戶端<br/> | \[僅限 Windows Vista 桌面應用程式\]<br/>                                          |
| 最低支援的伺服器<br/> | 僅限 Windows Server 2008 \[ desktop 應用程式\]<br/>                                    |
| 類型程式庫<br/>             | <dl> <dt>Taskschd.msc .tlb</dt> </dl> |
| DLL<br/>                      | <dl> <dt>Taskschd.dll</dt> </dl> |



 

 





