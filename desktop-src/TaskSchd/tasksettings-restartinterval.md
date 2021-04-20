---
title: TaskSettings. RestartInterval 屬性
description: 針對腳本，取得或設定值，這個值會指定工作排程器嘗試重新開機工作的時間長度。
ms.assetid: ad6f254d-55a8-478e-984e-a459f22043b5
keywords:
- RestartInterval 屬性工作排程器
- RestartInterval 屬性工作排程器，TaskSettings 物件
- TaskSettings 物件工作排程器、RestartInterval 屬性
topic_type:
- apiref
api_name:
- TaskSettings.RestartInterval
api_location:
- taskschd.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: f127c5d434b5cb1e6dec6d8a3c68ee343fa00ffc
ms.sourcegitcommit: b3a9abea47dea7374eac0f9a95a652ac6977fb2e
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 04/20/2021
ms.locfileid: "107734143"
---
# <a name="tasksettingsrestartinterval-property"></a>TaskSettings. RestartInterval 屬性

針對腳本，取得或設定值，這個值會指定工作排程器嘗試重新開機工作的時間長度。

這是可讀寫的屬性。

## <a name="syntax"></a>Syntax


```VB
TaskSettings.RestartInterval As String
```



## <a name="property-value"></a>屬性值

值，指定工作排程器將嘗試重新開機工作的時間長度。 如果設定這個屬性，也必須設定 [**RestartCount**](tasksettings-restartcount.md) 屬性。 此字串的格式為 `P<days>DT<hours>H<minutes>M<seconds>S` (例如，"PT5M" 為5分鐘、"PT1H" 為1小時，而 "PT20M" 為20分鐘) 。 允許的時間上限為31天，而允許的最短時間為1分鐘。

## <a name="remarks"></a>備註

讀取或寫入工作的 XML 時，此設定會在工作排程器架構的 [**Interval**](taskschedulerschema-interval-restarttype-element.md) 元素中指定。

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

 

 





