---
title: 觸發程式類型
description: 以時間為基礎和以事件為基礎的觸發程式如下所述，可讓您以各種不同的方式啟動工作。
ms.assetid: 2f577103-3892-49ce-9a3b-7a4839da8a83
keywords:
- 觸發程式工作排程器，類型
- 開機觸發程式工作排程器
- 啟動觸發程式工作排程器，說明
- 註冊觸發程式工作排程器
- 註冊觸發程式工作排程器，說明
- 行事曆觸發程式工作排程器
- 行事曆觸發程式工作排程器，說明
- 每日觸發程式工作排程器
- 每日觸發程式工作排程器，說明
- 每週觸發程式工作排程器
- 每週觸發程式工作排程器，說明
- 每月觸發程式工作排程器
- 每月觸發程式工作排程器，說明
- monthlyDOW 觸發程式工作排程器
- monthlyDOW 觸發程式工作排程器，說明
- 事件觸發程式工作排程器
- 事件觸發程式工作排程器，描述
- 登入觸發程式工作排程器
- 登入觸發程式工作排程器，說明
- 閒置觸發程式工作排程器
- 閒置觸發程式工作排程器，說明
- 星期幾觸發程式工作排程器
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 9a0e09b6ecc1ac3c817f374e70c6756fa09afc78ccaac7e549f3f04ad074c8d0
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/11/2021
ms.locfileid: "120099688"
---
# <a name="trigger-types"></a>觸發程式類型

以時間為基礎和以事件為基礎的觸發程式如下所述，可讓您以各種不同的方式啟動工作。

## <a name="task-scheduler-20-triggers"></a>工作排程器2.0 觸發程式

下列觸發程式類型是由 [**TASK \_ trigger \_ TYPE2**](/windows/desktop/api/taskschd/ne-taskschd-task_trigger_type2) 列舉所定義。

| 觸發程序                                                                                                                                                                                                                                                                                                                                                                                                                | 描述                                                                                                                                                                                  |
|------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| 事件觸發程式 (以事件為基礎的觸發程式) 用於腳本開發，請參閱 [**EventTrigger**](eventtrigger.md)。<br/> 針對 c + + 開發，請參閱 [**IEventTrigger**](/windows/desktop/api/taskschd/nn-taskschd-ieventtrigger)。<br/> 如需 XML 開發，請參閱 [**EventTrigger 元素**](taskschedulerschema-eventtrigger-triggergroup-element.md)。<br/>                                                                                             | 在特定系統事件發生時啟動工作。                                                                                                                                         |
| 時間觸發程式 (以時間為基礎的觸發程式) 進行腳本開發，請參閱 [**TimeTrigger**](timetrigger.md)。<br/> 針對 c + + 開發，請參閱 [**ITimeTrigger**](/windows/desktop/api/taskschd/nn-taskschd-itimetrigger)。<br/> 如需 XML 開發，請參閱 [**TimeTrigger 元素**](taskschedulerschema-timetrigger-triggergroup-element.md)。<br/>                                                                                                      | 在特定日期和時間啟動工作。                                                                                                                                                 |
| 每日觸發程式 (以時間為基礎的行事曆觸發程式) 進行腳本開發，請參閱 [**DailyTrigger**](dailytrigger.md)。<br/> 針對 c + + 開發，請參閱 [**IDailyTrigger**](/windows/desktop/api/taskschd/nn-taskschd-idailytrigger)。<br/> 如需 XML 開發，請參閱 [**CalendarTrigger 元素**](taskschedulerschema-calendartrigger-triggergroup-element.md)。<br/>                                                                                | 在每日排程的特定時間啟動工作。 例如，工作會在每天上午8:00 或每隔一天開始。                                                                |
| 每週觸發程式 (以時間為基礎的行事曆觸發程式) 進行腳本開發，請參閱 [**WeeklyTrigger**](weeklytrigger.md)。<br/> 針對 c + + 開發，請參閱 [**IWeeklyTrigger**](/windows/desktop/api/taskschd/nn-taskschd-iweeklytrigger)。<br/> 如需 XML 開發，請參閱 [**CalendarTrigger 元素**](taskschedulerschema-calendartrigger-triggergroup-element.md)。<br/>                                                                           | 在每週排程的特定時間啟動工作。 例如，工作會在每週的特定一天或每隔一周的特定一天，于上午8:00 開始。 |
| 每月觸發程式 (以時間為基礎的行事曆觸發程式) 進行腳本開發，請參閱 [**MonthlyTrigger**](monthlytrigger.md)。<br/> 針對 c + + 開發，請參閱 [**IMonthlyTrigger**](/windows/desktop/api/taskschd/nn-taskschd-imonthlytrigger)。<br/> 如需 XML 開發，請參閱 [**CalendarTrigger 元素**](taskschedulerschema-calendartrigger-triggergroup-element.md)。<br/>                                                                      | 依每月排程，在特定時間啟動工作。 例如，工作會在每月特定日子的特定月份從上午8:00 開始。                                          |
| 每月每週的 (DOW) 觸發程式 (以時間為基礎的行事曆觸發程式) 進行腳本開發，請參閱 [**MonthlyDOWTrigger**](monthlydowtrigger.md)。<br/> 針對 c + + 開發，請參閱 [**IMonthlyDOWTrigger**](/windows/desktop/api/taskschd/nn-taskschd-imonthlydowtrigger)。<br/> 如需 XML 開發，請參閱 [**CalendarTrigger 元素**](taskschedulerschema-calendartrigger-triggergroup-element.md)。<br/>                                        | 在每個月的每日排程上，于特定時間啟動工作。 例如，工作會在一周的特定日子、每月的周數和一年中的月份，從上午8:00 開始。      |
| 閒置觸發程式 (以事件為基礎的觸發程式) 進行腳本開發，請參閱 [**IdleTrigger**](idletrigger.md)。<br/> 針對 c + + 開發，請參閱 [**IIdleTrigger**](/windows/win32/api/taskschd/nn-taskschd-iidletrigger)。<br/> 如需 XML 開發，請參閱 [**IdleTrigger 元素**](taskschedulerschema-idletrigger-triggergroup-element.md)。<br/>                                                                                                     | 當電腦進入閒置狀態時，就會啟動工作。                                                                                                                                      |
| 註冊觸發程式 (以事件為基礎的觸發程式) 進行腳本開發，請參閱 [**RegistrationTrigger**](registrationtrigger.md)。<br/> 針對 c + + 開發，請參閱 [**IRegistrationTrigger**](/windows/desktop/api/taskschd/nn-taskschd-iregistrationtrigger)。<br/> 如需 XML 開發，請參閱 [**RegistrationTrigger 元素**](taskschedulerschema-registrationtrigger-triggergroup-element.md)。<br/>                                             | 在工作註冊或更新時啟動工作。                                                                                                                                      |
| 開機觸發程式 (以事件為基礎的觸發程式) 進行腳本開發，請參閱 [**BootTrigger**](boottrigger.md)。<br/> 針對 c + + 開發，請參閱 [**IBootTrigger**](/windows/desktop/api/taskschd/nn-taskschd-iboottrigger)。<br/> 如需 XML 開發，請參閱 [**BootTrigger 元素**](taskschedulerschema-boottrigger-triggergroup-element.md)。<br/>                                                                                                     | 當系統開機時啟動工作。                                                                                                                                                   |
| 登入觸發程式 (以事件為基礎的觸發程式) 進行腳本開發，請參閱 [**LogonTrigger**](logontrigger.md)。<br/> 針對 c + + 開發，請參閱 [**ILogonTrigger**](/windows/desktop/api/taskschd/nn-taskschd-ilogontrigger)。<br/> 如需 XML 開發，請參閱 [**LogonTrigger 元素**](taskschedulerschema-logontrigger-triggergroup-element.md)。<br/>                                                                                              | 在使用者登入時啟動工作。                                                                                                                                                         |
| 會話狀態變更觸發程式 (以事件為基礎的觸發程式) 進行腳本開發，請參閱 [**SessionStateChangeTrigger**](sessionstatechangetrigger.md)。<br/> 針對 c + + 開發，請參閱 [**ISessionStateChangeTrigger**](/windows/desktop/api/taskschd/nn-taskschd-isessionstatechangetrigger)。<br/> 如需 XML 開發，請參閱 [**SessionStateChangeTrigger 元素**](taskschedulerschema-sessionstatechangetrigger-triggergroup-element.md)。<br/> | 在終端機伺服器會話變更狀態時啟動工作。                                                                                                                                |



 

## <a name="task-scheduler-10-triggers"></a>工作排程器1.0 觸發程式

下列觸發程式類型是由工作 [**觸發程式 \_ \_ 類型**](/windows/desktop/api/Mstask/ne-mstask-task_trigger_type) 列舉所定義。 若要執行下列任何觸發程式，請參閱 [**工作 \_ 觸發**](/windows/desktop/api/Mstask/ns-mstask-task_trigger) 程式結構。

-   觸發程式：一次啟動工作。
-   每日觸發程式：依每日間隔啟動工作。
-   每週觸發程式：以每週排程啟動工作。
-   每月觸發程式：依每月排程啟動工作。
-   每月 DOW 觸發程式：依每月一周的排程啟動工作。
-   閒置觸發程式：當電腦處於閒置狀態時啟動工作。
-   系統啟動觸發程式：啟動電腦時啟動工作。
-   登入觸發程式：在特定使用者登入時啟動工作。

## <a name="related-topics"></a>相關主題

<dl> <dt>

[工作觸發程式](task-triggers.md)
</dt> <dt>

[觸發程式介面](trigger-interfaces.md)
</dt> <dt>

[觸發程式結構](trigger-structures.md)
</dt> </dl>

 

