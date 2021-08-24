---
title: TaskSettings. DeleteExpiredTaskAfter 屬性
description: 針對腳本，取得或設定在工作到期之後，工作排程器將等待的時間量。
ms.assetid: c57d736c-e3ce-44b8-809e-44f7c0321d70
keywords:
- DeleteExpiredTaskAfter 屬性工作排程器
- DeleteExpiredTaskAfter 屬性工作排程器，TaskSettings 物件
- TaskSettings 物件工作排程器、DeleteExpiredTaskAfter 屬性
topic_type:
- apiref
api_name:
- TaskSettings.DeleteExpiredTaskAfter
api_location:
- taskschd.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 521f07a5712165c282a36bbfe2c3b66769239c53d652ae49a03fa6a50c19cb05
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/11/2021
ms.locfileid: "119658448"
---
# <a name="tasksettingsdeleteexpiredtaskafter-property"></a>TaskSettings. DeleteExpiredTaskAfter 屬性

針對腳本，取得或設定在工作到期之後，工作排程器將等待的時間量。 如果未指定這個屬性的值，工作排程器服務將不會刪除該工作。

這是可讀寫的屬性。

## <a name="syntax"></a>Syntax


```VB
TaskSettings.DeleteExpiredTaskAfter As String
```



## <a name="property-value"></a>屬性值

字串，這個字串會取得或設定工作排程器在工作到期之後刪除工作的等待時間量。 此字串的格式為 PnYnMnDTnHnMnS，其中 nY 是年數，nM 是月數，nD 是天數、t ' 是日期/時間分隔符號、nH 是時數、nM 為分鐘數，而 nS 是以秒為單位的秒數，例如，PT5M 指定 (5 分鐘，P1M4DT2H5M 指定一個月、四天、兩小時和五分鐘的) 。

## <a name="remarks"></a>備註

當所有與工作相關聯的觸發程式都超過結束界限之後，工作就會過期。 觸發程式的結束界限是由所有觸發程式物件所繼承的 [EndBoundary](trigger-endboundary.md) 屬性所指定。

讀取或寫入工作的 XML 時，此設定會指定在工作排程器架構的 [**DeleteExpiredTaskAfter (settingsType)**](taskschedulerschema-deleteexpiredtaskafter-settingstype-element.md) 元素中。

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

 

 





