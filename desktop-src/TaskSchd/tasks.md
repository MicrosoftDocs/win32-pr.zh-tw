---
title: 工作
description: 工作是工作排程器服務執行的排程工作。
ms.assetid: 24c43834-5731-4b14-9409-7d7cf20b1a71
keywords:
- 工作工作排程器
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: efbb4ef41915ec70c98b59c9a7ba74c00f283ce6
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 09/16/2019
ms.locfileid: "106976324"
---
# <a name="tasks"></a>工作

工作是工作排程器服務執行的排程工作。 工作是由不同的元件所組成，但是工作必須包含觸發程式，工作排程器使用此觸發程式來啟動工作，以及描述工作排程器將執行哪些工作的動作。

當工作建立時，它會儲存在工作資料夾中。 您可以透過 [**ITaskFolder**](/windows/desktop/api/taskschd/nn-taskschd-itaskfolder) 介面 ([**TaskFolder**](taskfolder.md) 來存取工作資料夾，以編寫腳本) ，而且可以透過 [**IRegisteredTask**](/windows/desktop/api/taskschd/nn-taskschd-iregisteredtask) 介面存取工作資料夾， ([**RegisteredTask**](registeredtask.md) 在建立時使用腳本) 。 您可以變更工作和工作資料夾 (Acl) 的存取控制清單，以授與或拒絕特定使用者和群組對工作或工作資料夾的存取權。 這可以藉由使用 [**IRegisteredTask：： SetSecurityDescriptor**](/windows/desktop/api/taskschd/nf-taskschd-iregisteredtask-setsecuritydescriptor) 方法、 [**ITaskFolder：： SetSecurityDescriptor**](/windows/desktop/api/taskschd/nf-taskschd-itaskfolder-setsecuritydescriptor) 方法，或在使用 [**RegisterTaskDefinition**](/windows/desktop/api/taskschd/nf-taskschd-itaskfolder-registertaskdefinition) 或 [**RegisterTask**](/windows/desktop/api/taskschd/nf-taskschd-itaskfolder-registertask) 方法註冊工作時指定安全描述項來完成。

> [!Note]  
> 如果本機系統帳戶拒絕存取工作檔案或工作資料夾，工作排程器服務可能會產生非預期的結果。

 

## <a name="components-of-a-task"></a>工作的元件

下圖顯示工作元件。

![工作元件](images/taskcomponents.png)

下列清單包含每個工作元件的簡短描述：

-   觸發程式：工作排程器使用事件或以時間為基礎的觸發程式，以瞭解何時啟動工作。 每項工作都可以指定一或多個觸發程式來啟動工作。

    如需觸發程式的詳細資訊，請參閱工作 [觸發](task-triggers.md)程式。

-   動作：這些是工作所執行的動作，也就是實際的工作。 每項工作都可以指定一或多個動作來完成其工作。

    如需動作的詳細資訊，請參閱工作 [動作](task-actions.md)。

-   主體：主體會定義執行工作的安全性內容。 例如，主體可能會定義可以執行工作的特定使用者或使用者群組。

    如需主體的詳細資訊，請參閱工作 [的安全性](security-contexts-for-running-tasks.md)內容。

-   設定：這些是工作排程器用來執行工作的設定，這些設定是針對工作本身以外的條件。 例如，這些設定可以指定工作與其他工作相關的優先順序、是否可以執行工作的多個實例、在電腦處於閒置狀態時如何處理工作，以及其他條件。

    如需工作設定的詳細資訊，請參閱腳本) 的 [**ITaskSettings**](/windows/desktop/api/taskschd/nn-taskschd-itasksettings) ([**TaskSettings**](tasksettings.md) 。

    > [!Note]  
    > 根據預設，工作會在開始執行時停止72小時。 您可以藉由變更 [**ExecutionTimeLimit**](/windows/desktop/api/taskschd/nf-taskschd-itasksettings-get_executiontimelimit) 設定來變更。

     

-   註冊資訊：這是在註冊工作時所收集的系統管理資訊。 例如，此資訊描述工作的作者、註冊工作的日期、工作的 XML 描述，以及其他資訊。

    如需工作註冊資訊的詳細資訊，請參閱工作 [註冊資訊](task-registration-information.md)。

-   Data：這是工作作者所提供之工作的其他檔。 例如，此資料可能包含使用者執行工作時可供使用者使用的 XML 說明。

## <a name="task-apis"></a>工作 Api

工作排程器2.0 提供兩組 Api：工作排程器2.0 的一組腳本物件和介面。 如需詳細資訊，請參閱 [工作排程器參考](task-scheduler-reference.md)。

[](/windows/desktop/api/taskschd/nf-taskschd-itasksettings-get_compatibility) \_ \_ 如果工作必須從 Windows XP、Windows Server 2003 或 windows 2000 電腦存取或修改，則透過 [相容性] 屬性所設定的工作相容性只應設定為 [工作相容性 V1]。 否則，建議您使用工作排程器2.0 相容性，因為它有更多功能。

從工作排程器2.0 開始，腳本) 的 [**ITaskService**](/windows/desktop/api/taskschd/nn-taskschd-itaskservice) 介面 ([**TaskService**](taskservice.md) ，是用來在指定的資料夾中建立工作的起點。 腳本) 的 [**ITaskDefinition**](/windows/desktop/api/taskschd/nn-taskschd-itaskdefinition) 介面 ([**TaskDefinition**](taskdefinition.md) 用來保存工作的所有元件，例如設定、動作和觸發程式。 [**ITaskTrigger**](/windows/desktop/api/Mstask/nn-mstask-itasktrigger)、 [**IAction**](/windows/desktop/api/taskschd/nn-taskschd-iaction)和 [**ITaskSettings**](/windows/desktop/api/taskschd/nn-taskschd-itasksettings) api 提供的屬性，可用來定義工作的其他元件。 工作排程器1.0 提供僅為了回溯相容性所支援的 [**ITask**](/windows/desktop/api/Mstask/nn-mstask-itask) 介面。

針對腳本，工作排程器介面會對應到具有類似名稱、屬性和方法的腳本物件。 例如， [**TaskService**](taskservice.md) 腳本物件具有與 [**ITaskService**](/windows/desktop/api/taskschd/nn-taskschd-itaskservice) 介面相同的屬性和方法。

如需有關如何使用工作排程器介面、腳本物件和 XML 的詳細資訊和範例，請參閱 [使用工作排程器](using-the-task-scheduler.md)。

### <a name="task-scheduler-10-tasks"></a>工作排程器1.0 工作

工作排程器1.0 工作是工作排程器可執行檔任何應用程式或檔案類型。 這些可能包括工作執行所在作業系統所支援的下列任何 () ： Win32 應用程式、Win16 應用程式、OS/2 應用程式、MS-DOS 應用程式、批次檔 (\* .bat) 、命令檔 (\* .cmd) 或任何正確註冊的檔案類型。

描述工作的資料會保存在儲存在 [排程工作] 資料夾中的工作檔案。 如需詳細資訊，請參閱排程的工作 [*資料夾*](s.md)。 這些工作檔的名稱包括工作的名稱，後面接著一個. 作業副檔名。

如需新增工作排程器1.0 工作的詳細資訊，請參閱 [加入工作專案](adding-work-items.md)。

如需列舉工作排程器1.0 工作的詳細資訊，請參閱列舉工作（ [task](enumerating-tasks.md)）。

若為 Windows Server 2003、Windows XP 或 Windows 2000 電腦，可在 Windows Vista 電腦上建立、監視或控制工作，則應該在 Windows Vista 電腦上完成下列操作，而且呼叫 [**ITaskScheduler：： SetTargetComputer**](/windows/desktop/api/Mstask/nf-mstask-itaskscheduler-settargetcomputer) 方法的使用者必須是遠端 Windows vista 電腦上的 Administrators 群組成員。

**若要在 Windows 防火牆中啟用「共用檔案和印表機」例外狀況**

1.  按一下 [開始]，然後按一下 [控制台]。
2.  在 **主控台** 中，按一下 [ **傳統視圖** ]，然後按兩下 [ **Windows 防火牆** ] 圖示。
3.  在 [ **Windows 防火牆** ] 視窗中，按一下 [ **例外** 狀況] 索引標籤，然後選取 [檔案 **和印表機共用例外** ] 核取方塊。

**啟用「遠端登入」服務**

-   開啟 [命令提示字元] 視窗，然後輸入下列命令： **net start "Remote Registry"**。

## <a name="related-topics"></a>相關主題

<dl> <dt>

[關於工作排程器](about-the-task-scheduler.md)
</dt> <dt>

[工作觸發程式](task-triggers.md)
</dt> <dt>

[工作動作](task-actions.md)
</dt> <dt>

[**ITaskDefinition**](/windows/desktop/api/taskschd/nn-taskschd-itaskdefinition)
</dt> <dt>

[**TaskDefinition**](taskdefinition.md)
</dt> <dt>

[**ITaskService**](/windows/desktop/api/taskschd/nn-taskschd-itaskservice)
</dt> <dt>

[**TaskService**](taskservice.md)
</dt> </dl>

 

 




