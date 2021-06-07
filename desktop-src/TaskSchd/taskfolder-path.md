---
title: TaskFolder 路徑屬性
description: 針對腳本，取得資料夾儲存位置的路徑。
ms.assetid: a0b28527-4875-4fe4-b2dd-08abbdc87ccc
keywords:
- 路徑屬性工作排程器
- Path 屬性工作排程器，TaskFolder 物件
- TaskFolder 物件工作排程器，Path 屬性
topic_type:
- apiref
api_name:
- TaskFolder.Path
api_location:
- taskschd.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 26c917a7f03a28f7b5c379673229976897af9b5f
ms.sourcegitcommit: cb87082135319cbdc5df541e3071eebb83a58972
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 06/04/2021
ms.locfileid: "111387007"
---
# <a name="taskfolderpath-property"></a>TaskFolder 路徑屬性

針對腳本，取得資料夾儲存位置的路徑。

## <a name="syntax"></a>Syntax


```VB
TaskFolder.Path As String
```



## <a name="property-value"></a>屬性值

資料夾儲存位置的路徑。 根工作資料夾是以反斜線 () 指定 \\ 。 根工作資料夾下的工作資料夾路徑範例是 \\ MyTaskFolder。

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

 

 





