---
title: 觸發程式介面
description: 用來管理觸發程式的 Api 會根據工作排程器的版本而有所不同。 不過，在這兩種情況下，這些 Api 可讓您建立新的觸發程式、取出和更新現有的觸發程式，以及刪除不再需要的觸發程式。
ms.assetid: 94c11f11-72e2-404f-b396-ab7b1be71942
keywords:
- 觸發程式工作排程器、介面
- 觸發程式工作排程器、介面、描述
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: f5515f2b1e2f5b4a7694dec28bb8831c690da0d303cda53338714c1b0e03ddaa
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/11/2021
ms.locfileid: "119002180"
---
# <a name="trigger-interfaces"></a>觸發程式介面

用來管理觸發程式的 Api 會根據工作排程器的版本而有所不同。 不過，在這兩種情況下，這些 Api 可讓您建立新的觸發程式、取出和更新現有的觸發程式，以及刪除不再需要的觸發程式。


使用工作排程器2.0 開發的應用程式可以使用物件和介面，來建立、取出、修改和刪除工作的觸發程式。

在下圖中，工作會使用觸發程式屬性來指定觸發程式的集合。 此集合包含一個或多個個別的觸發程式 Api，其中每個 API 指定了特定的觸發程式類型。 例如，在下圖中，觸發程式集合包含開機觸發程式、登入觸發程式和每日觸發程式。

![工作排程器2.0 觸發程式介面](images/tsktri4.png)

### <a name="object-apis-for-scripting-development"></a>腳本開發的物件 Api

如需有關用來指定觸發程式之物件的方法和屬性的詳細資訊，請參閱：

-   [**TaskDefinition**](taskdefinition.md)
-   [**TriggerCollection**](triggercollection.md)
-   [**觸發程序**](trigger.md)
-   [**BootTrigger**](boottrigger.md)
-   [**DailyTrigger**](dailytrigger.md)
-   [**EventTrigger**](eventtrigger.md)
-   [**IdleTrigger**](idletrigger.md)
-   [**LogonTrigger**](logontrigger.md)
-   [**MonthlyDOWTrigger**](monthlydowtrigger.md)
-   [**MonthlyTrigger**](monthlytrigger.md)
-   [**RegistrationTrigger**](registrationtrigger.md)
-   [**TimeTrigger**](timetrigger.md)
-   [**WeeklyTrigger**](weeklytrigger.md)

### <a name="interfaces-apis-for-c-development"></a>適用于 c + + 開發的介面 Api

如需有關用來指定觸發程式之介面的方法和屬性的詳細資訊，請參閱：

-   [**ITaskDefinition**](/windows/desktop/api/taskschd/nn-taskschd-itaskdefinition)
-   [**ITriggerCollection**](/windows/desktop/api/taskschd/nn-taskschd-itriggercollection)
-   [**ITrigger**](/windows/desktop/api/taskschd/nn-taskschd-itrigger)
-   [**IBootTrigger**](/windows/desktop/api/taskschd/nn-taskschd-iboottrigger)
-   [**IDailyTrigger**](/windows/desktop/api/taskschd/nn-taskschd-idailytrigger)
-   [**IEventTrigger**](/windows/desktop/api/taskschd/nn-taskschd-ieventtrigger)
-   [**IIdleTrigger**](/windows/win32/api/taskschd/nn-taskschd-iidletrigger)
-   [**ILogonTrigger**](/windows/desktop/api/taskschd/nn-taskschd-ilogontrigger)
-   [**IMonthlyDOWTrigger**](/windows/desktop/api/taskschd/nn-taskschd-imonthlydowtrigger)
-   [**IMonthlyTrigger**](/windows/desktop/api/taskschd/nn-taskschd-imonthlytrigger)
-   [**IRegistrationTrigger**](/windows/desktop/api/taskschd/nn-taskschd-iregistrationtrigger)
-   [**ITimeTrigger**](/windows/desktop/api/taskschd/nn-taskschd-itimetrigger)
-   [**IWeeklyTrigger**](/windows/desktop/api/taskschd/nn-taskschd-iweeklytrigger)

## <a name="task-scheduler-10-trigger-interfaces"></a>工作排程器1.0 觸發程式介面

使用工作排程器1.0 開發的現有應用程式，可以使用工作排程器1.0 介面中可用的方法，來建立、抓取、修改及刪除 [*工作專案*](w.md)的觸發程式。 不過，請注意，所有工作排程器1.0 介面、列舉和結構都已過時，不應該用於開發新的應用程式。

下圖顯示用來執行這項操作的兩個介面。 [**IScheduledWorkItem**](/windows/desktop/api/Mstask/nn-mstask-ischeduledworkitem)介面可用來管理與工作專案相關聯的所有觸發程式 (這類管理包括為工作專案) 建立新的觸發程式。 [**ITaskTrigger**](/windows/desktop/api/Mstask/nn-mstask-itasktrigger)介面可用來管理特定的觸發程式。

![工作排程器1.0 觸發程式介面](images/tsktri2.png)

[**IScheduledWorkItem**](/windows/desktop/api/Mstask/nn-mstask-ischeduledworkitem)介面提供的方法可為工作專案建立新的觸發程式、抓取與工作專案相關聯的觸發程式數目、抓取與工作專案相關聯的觸發程式 [*結構*](t.md)、取得與工作專案相關聯的觸發程式 [*字串*](t.md)，以及刪除觸發程式。

一旦觸發程式物件可供使用，您就可以使用 [**ITaskTrigger**](/windows/desktop/api/Mstask/nn-mstask-itasktrigger) 介面來抓取觸發程式結構和觸發程式的字串，並設定用來引發觸發程式的準則。 只有當您使用工作 [*觸發程式物件*](t.md)時，才會使用此介面。

## <a name="related-topics"></a>相關主題

<dl> <dt>

[工作觸發程式](task-triggers.md)
</dt> <dt>

[觸發程式類型](trigger-types.md)
</dt> <dt>

[觸發程式結構](trigger-structures.md)
</dt> </dl>

 

 