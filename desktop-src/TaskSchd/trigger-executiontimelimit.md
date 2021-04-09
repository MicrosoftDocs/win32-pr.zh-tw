---
title: Trigger.ExecutionTimeLimit 屬性
description: 針對腳本，取得或設定允許執行觸發程式之工作的最大時間量。
ms.assetid: 9993b362-f8f7-429b-a16a-1845d6f0f5e0
keywords:
- ExecutionTimeLimit 屬性工作排程器
- ExecutionTimeLimit 屬性工作排程器，觸發程式物件
- 觸發程式物件工作排程器，ExecutionTimeLimit 屬性
topic_type:
- apiref
api_name:
- Trigger.ExecutionTimeLimit
api_location:
- taskschd.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 974a9adebf8ca29fe8626c938c37580d0628771b
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 12/12/2020
ms.locfileid: "103934135"
---
# <a name="triggerexecutiontimelimit-property"></a>Trigger.ExecutionTimeLimit 屬性

針對腳本，取得或設定允許執行觸發程式之工作的最大時間量。

## <a name="syntax"></a>Syntax


```VB
Trigger.ExecutionTimeLimit As String
```



## <a name="property-value"></a>屬性值

允許執行觸發程式之工作的最大時間量。 此字串的格式為 PnYnMnDTnHnMnS，其中 nY 是年數，nM 是月數，nD 是天數、t ' 是日期/時間分隔符號、nH 是時數、nM 為分鐘數，而 nS 是以秒為單位的秒數，例如，PT5M 指定 (5 分鐘，P1M4DT2H5M 指定一個月、四天、兩小時和五分鐘的) 。

## <a name="remarks"></a>備註

讀取或寫入工作的 XML 時，會在工作排程器架構的 [**ExecutionTimeLimit**](taskschedulerschema-executiontimelimit-triggerbasetype-element.md) 元素中指定執行時間限制。

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

 

 





