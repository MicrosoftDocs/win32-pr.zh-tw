---
title: WeeklyTrigger. WeeksInterval 屬性
description: 針對腳本，取得或設定排程中周之間的間隔。
ms.assetid: 7992dee2-1725-4325-9fe9-eaff84fa5adc
keywords:
- WeeksInterval 屬性工作排程器
- WeeksInterval 屬性工作排程器，WeeklyTrigger 物件
- WeeklyTrigger 物件工作排程器、WeeksInterval 屬性
topic_type:
- apiref
api_name:
- WeeklyTrigger.WeeksInterval
api_location:
- taskschd.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 547ebc8617d625df3dd0e8dba167bb60682185dfb13897c49524d1894789c933
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/11/2021
ms.locfileid: "120080258"
---
# <a name="weeklytriggerweeksinterval-property"></a>WeeklyTrigger. WeeksInterval 屬性

針對腳本，取得或設定排程中周之間的間隔。

## <a name="syntax"></a>Syntax


```VB
WeeklyTrigger.WeeksInterval As short
```



## <a name="property-value"></a>屬性值

排程中周之間的間隔。

## <a name="remarks"></a>備註

間隔1會產生每週排程。 間隔2會產生每隔一周的排程。

針對工作讀取或撰寫您自己的 XML 時，每週排程的間隔是使用工作排程器架構的 [**WeeksInterval**](taskschedulerschema-weeksinterval-weeklyscheduletype-element.md) 元素來指定。

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

 

 





