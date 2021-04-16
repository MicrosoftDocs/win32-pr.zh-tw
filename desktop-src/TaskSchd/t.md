---
title: 'T (工作排程器) '
description: A B C D E F G H I J K L M N O P Q R S T U V W X Y Z
ROBOTS: NOINDEX, NOFOLLOW
ms.assetid: d4c6d7ba-7bca-420d-a4dc-4daea816f99c
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 2730cdbe3a13456aed0e613a614d43a0e56e6673
ms.sourcegitcommit: 8fa6614b715bddf14648cce36d2df22e5232801a
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 12/10/2020
ms.locfileid: "104508244"
---
# <a name="t-task-scheduler"></a>T (工作排程器) 

B C D [E](e.md) F G H [I](i.md) J K L M N O [P](p.md) Q R [S](s.md) T [W](w.md) X Y Z

<dl> <dt>

<span id="_msb_task_objects_gly"></span><span id="_MSB_TASK_OBJECTS_GLY"></span>**工作物件**
</dt> <dd>

物件的實例，提供管理工作的方法。 這包括設定和抓取屬性的方法;執行、終止和刪除工作;以及建立新的觸發程式並抓取舊的觸發程式。

工作物件是由呼叫 [**IScheduledWorkItem：： CreateTrigger**](/windows/desktop/api/Mstask/nf-mstask-ischeduledworkitem-createtrigger) 和 [**IScheduledWorkItem：： GetTrigger**](/windows/desktop/api/Mstask/nf-mstask-ischeduledworkitem-gettrigger)所建立。

</dd> <dt>

<span id="_msb_task_scheduler_objects_gly"></span><span id="_MSB_TASK_SCHEDULER_OBJECTS_GLY"></span>**工作排程器物件**
</dt> <dd>

物件的實例，代表工作排程器服務。 此物件支援兩個介面： **IUnknown** 和 [**ITaskScheduler**](/windows/desktop/api/Mstask/nn-mstask-itaskscheduler) (目前的工作是工作排程器服務) 所支援的唯一工作專案類型。

工作排程器物件是由對 **CoCreateInstance** 的呼叫所建立。

</dd> <dt>

<span id="_msb_task_trigger_objects_gly"></span><span id="_MSB_TASK_TRIGGER_OBJECTS_GLY"></span>**工作觸發程式物件**
</dt> <dd>

物件的實例，提供用來設定和抓取工作觸發程式的方法。 此物件支援兩個介面： **IUnknown** 和 [**ITaskTrigger**](/windows/desktop/api/Mstask/nn-mstask-itasktrigger)。

工作觸發程式物件是由呼叫 [**IScheduledWorkItem：： CreateTrigger**](/windows/desktop/api/Mstask/nf-mstask-ischeduledworkitem-createtrigger) 和 [**IScheduledWorkItem：： GetTrigger**](/windows/desktop/api/Mstask/nf-mstask-ischeduledworkitem-gettrigger)所建立。

另請參閱： *觸發* 程式。

</dd> <dt>

<span id="_msb_tasks_gly"></span><span id="_MSB_TASKS_GLY"></span>**任務**
</dt> <dd>

工作排程器可以執行的任何專案。 這些專案可能包含工作將執行的作業系統所支援的下列任何 () ： Win32®應用程式、Win16 應用程式、OS/2 應用程式、MS-DOS®應用程式、批次檔 (\* .bat) 、命令檔 (\* .cmd) ，或任何正確註冊的檔案類型。

</dd> <dt>

<span id="_msb_tasks_folder_gly"></span><span id="_MSB_TASKS_FOLDER_GLY"></span>**Tasks 資料夾**
</dt> <dd>

列出所有工作檔案 (目前的資料夾，工作是唯一可用的工作專案) 。 這些檔案包含工作的相關資訊。 這些檔案的名稱會反映工作的名稱。

您可以藉由取得下列值的資料，從登錄取出 Tasks 資料夾的位置：

```
HKEY_LOCAL_MACHINE
   SOFTWARE
      Microsoft
         SchedulingAgent
            TasksFolder
```

</dd> <dt>

<span id="_msb_triggers_gly"></span><span id="_MSB_TRIGGERS_GLY"></span>**觸發器**
</dt> <dd>

當符合時，會造成工作執行的一組準則。 工作排程器提供以時間為基礎和以事件為基礎的觸發程式，可指定工作開始時間、重複條件及其他參數。

</dd> <dt>

<span id="_msb_trigger_strings_gly"></span><span id="_MSB_TRIGGER_STRINGS_GLY"></span>**觸發字串**
</dt> <dd>

描述觸發程式的字串。 這個字串是由工作排程器服務所建立，並出現在工作排程器的使用者介面中，其格式類似于「每日下午2：5/11/97」。

</dd> <dt>

<span id="_msb_trigger_structures_gly"></span><span id="_MSB_TRIGGER_STRUCTURES_GLY"></span>**觸發程式結構**
</dt> <dd>

在設定或抓取定義觸發程式的準則時，所使用的工作 [**\_ 觸發**](/windows/desktop/api/Mstask/ns-mstask-task_trigger) 程式結構。 準則包括觸發程式的觸發時間，以及觸發程式的類型。

</dd> </dl>

 

 




