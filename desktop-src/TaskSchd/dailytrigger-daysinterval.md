---
title: DailyTrigger. DaysInterval 屬性
description: 針對腳本，取得或設定排程中天數之間的間隔。
ms.assetid: 13e9f6fd-62ee-4b19-8b3d-a6808e146340
keywords:
- DaysInterval 屬性工作排程器
- DaysInterval 屬性工作排程器，DailyTrigger 物件
- DailyTrigger 物件工作排程器、DaysInterval 屬性
topic_type:
- apiref
api_name:
- DailyTrigger.DaysInterval
api_location:
- taskschd.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: d4355e6c2a26b197224141018fa5a1d85e7d31e211ac47dc84a9e8c9ef3750fd
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/11/2021
ms.locfileid: "119139491"
---
# <a name="dailytriggerdaysinterval-property"></a>DailyTrigger. DaysInterval 屬性

針對腳本，取得或設定排程中天數之間的間隔。

## <a name="syntax"></a>Syntax


```VB
DailyTrigger.DaysInterval As short
```



## <a name="property-value"></a>屬性值

排程中天數之間的間隔。

## <a name="remarks"></a>備註

間隔1會產生每日排程。 間隔2會產生每隔一天的排程。

針對工作讀取或撰寫您自己的 XML 時，會使用工作排程器架構的 [**DaysInterval**](taskschedulerschema-daysinterval-dailyscheduletype-element.md) 元素來指定每日排程的間隔。

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
</dt> <dt>

[**DailyTrigger**](dailytrigger.md)
</dt> </dl>

 

 





