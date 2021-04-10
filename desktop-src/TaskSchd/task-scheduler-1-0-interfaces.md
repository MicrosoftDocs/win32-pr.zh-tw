---
title: 工作排程器1.0 介面
description: 下列主題中所述的介面，可讓您以程式設計方式存取 Windows 2000、Windows XP 及 Windows Server 2003 作業系統中使用的工作排程器功能。
ms.assetid: 25f9c1ad-1859-4788-a876-6f4faa6e556e
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 2bab12b59d4b4561ecbe46c09a76c69209574c9d
ms.sourcegitcommit: a716ca2a6a22a400f02c6b31699cf4da83ee3619
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 11/04/2020
ms.locfileid: "104186651"
---
# <a name="task-scheduler-10-interfaces"></a>工作排程器1.0 介面

\[\[此 API 可能會在後續版本的作業系統或產品中變更或無法使用。 請改用[工作排程器2.0 介面](task-scheduler-2-0-interfaces.md)或[工作排程器2.0 列舉類型](task-scheduler-2-0-enumerated-types.md)。 \]\]

下列主題中所述的介面，可讓您以程式設計方式存取 Windows 2000、Windows XP 及 Windows Server 2003 作業系統中使用的工作排程器功能。

這些主題包含介面的描述、介面所定義之屬性和方法的清單，以及使用介面時應注意的任何特殊情況的備註。


下列是工作排程器1.0 引進的介面。



| 介面                                        | 描述                                                                                                                                                                                                                           |
|--------------------------------------------------|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [**IEnumWorkItems**](/windows/desktop/api/Mstask/nn-mstask-ienumworkitems)         | 提供列舉 [排定的工作] [*資料夾*](s.md)中之工作的方法。                                                                                                              |
| [**IProvideTaskPage**](/windows/desktop/api/Mstask/nn-mstask-iprovidetaskpage)     | 提供方法來存取工作的屬性工作表設定。                                                                                                                                                                 |
| [**IScheduledWorkItem**](/windows/desktop/api/Mstask/nn-mstask-ischeduledworkitem) | 提供管理特定 [*工作專案*](w.md)的方法。                                                                                                                                                 |
| [**ITask**](/windows/desktop/api/Mstask/nn-mstask-itask)                           | 提供執行工作、取得或設定工作資訊，以及終止工作的方法。 它衍生自 [**IScheduledWorkItem**](/windows/desktop/api/Mstask/nn-mstask-ischeduledworkitem) 介面，並繼承該介面的所有方法。 |
| [**ITaskScheduler**](/windows/desktop/api/Mstask/nn-mstask-itaskscheduler)         | 提供排程工作的方法。                                                                                                                                                                                            |
| [**ITaskTrigger**](/windows/desktop/api/Mstask/nn-mstask-itasktrigger)             | 提供用來存取和設定工作觸發程式的方法。 觸發程式會指定工作開始時間、重複準則，以及控制工作執行時間的其他參數。                                                     |



 

 

 




