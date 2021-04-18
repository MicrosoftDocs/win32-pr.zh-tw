---
title: TaskSettings.ExecutionTimeLimit 屬性
description: 針對腳本，取得或設定可以完成工作的時間量。
ms.assetid: 5b8b8d4b-e705-4407-95c9-bf8baacb58c1
keywords:
- ExecutionTimeLimit 屬性工作排程器
- ExecutionTimeLimit 屬性工作排程器，TaskSettings 物件
- TaskSettings 物件工作排程器、ExecutionTimeLimit 屬性
topic_type:
- apiref
api_name:
- TaskSettings.ExecutionTimeLimit
api_location:
- taskschd.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: de01d68fa7fe6c21f022d8a21863887e57016c5c
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 12/12/2020
ms.locfileid: "106967358"
---
# <a name="tasksettingsexecutiontimelimit-property"></a>TaskSettings.ExecutionTimeLimit 屬性

針對腳本，取得或設定可以完成工作的時間量。 根據預設，工作會在開始執行時停止72小時。 您可以變更此設定來變更此設定。

這是可讀寫的屬性。

## <a name="syntax"></a>Syntax


```VB
TaskSettings.ExecutionTimeLimit As String
```



## <a name="property-value"></a>屬性值

允許完成工作的時間量。 此字串的格式為 PnYnMnDTnHnMnS，其中 nY 是年數，nM 是月數，nD 是天數、t ' 是日期/時間分隔符號、nH 是時數、nM 為分鐘數，而 nS 是以秒為單位的秒數，例如，PT5M 指定 (5 分鐘，P1M4DT2H5M 指定一個月、四天、兩小時和五分鐘的) 。 PT0S 的值會讓工作無限期地執行。 當此參數設定為 [無] 時，執行時間限制為 [無限]。

## <a name="remarks"></a>備註

讀取或寫入工作的 XML 時，此設定會在工作排程器架構的 [**ExecutionTimeLimit**](taskschedulerschema-executiontimelimit-settingstype-element.md) 元素中指定。

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

 

 





