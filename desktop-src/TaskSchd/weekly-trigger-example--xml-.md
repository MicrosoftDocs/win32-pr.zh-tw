---
title: " (XML) 的每週觸發程式範例"
description: 此範例中的 XML 會定義以每週為基礎啟動 [記事本] 的工作。
ms.assetid: 1911e8b1-2583-440c-a6ed-d71080b60987
ms.topic: article
ms.date: 05/31/2018
topic_type:
- kbArticle
api_name: ''
api_type: ''
api_location: ''
ms.openlocfilehash: bf8c2683311aecc427e9570a0452c746375eca01
ms.sourcegitcommit: 40dd8501397fc79a643deb528c6c57ac2e9726ce
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/24/2020
ms.locfileid: "104374166"
---
# <a name="weekly-trigger-example-xml"></a> (XML) 的每週觸發程式範例

此範例中的 XML 會定義以每週為基礎啟動 [記事本] 的工作。

若要註冊 XML 中定義的工作，您可以使用 [**ITaskFolder：： RegisterTask**](/windows/desktop/api/taskschd/nf-taskschd-itaskfolder-registertask) 函數 ([**TaskFolder. RegisterTask**](taskfolder-registertask.md) 來撰寫腳本) 或 Schtasks.exe 命令列工具。 如果您使用位於 C： \\ Windows System32 目錄) 的 Schtasks.exe 工具 (\\ ，則可以使用下列命令來註冊工作： **schtasks.exe/create/xml** *<path to the XML file containing the task definition>* **/tn** *<task name>* 。

## <a name="to-define-a-task-to-start-notepad-every-other-week-on-monday-at-800-am"></a>將工作定義為在星期一上午8:00 點開始每隔一周啟動記事本

下列 XML 範例示範如何使用單一執行動作來定義工作 (啟動 [記事本]) 、單一行事曆觸發程式 (在星期一的上午8:00 點開始每隔一周進行工作) ，以及其他會影響工作排程器處理工作方式的其他工作設定。


```XML
<?xml version="1.0" ?>
<!--
This sample schedules a task to start on a bi-weekly basis.
-->
<Task xmlns="http://schemas.microsoft.com/windows/2004/02/mit/task">
    <RegistrationInfo>
        <Date>2005-05-01T09:00:00</Date>
        <Author>AuthorName</Author>
        <Version>1.0.0</Version>
        <Description>Notepad starts every other week on Monday at 8:00am.</Description>
    </RegistrationInfo>
    <Triggers>
        <CalendarTrigger>
            <StartBoundary>2005-05-02T08:00:00</StartBoundary>
            <EndBoundary>2006-01-01T00:00:00</EndBoundary>
            <ScheduleByWeek>
                <WeeksInterval>2</WeeksInterval>
                <DaysOfWeek>
                    <Monday/>
                </DaysOfWeek>
            </ScheduleByWeek>
        </CalendarTrigger>
    </Triggers>
    <Principals>
        <Principal>
            <UserId>Administrator</UserId>
            <LogonType>InteractiveToken</LogonType>
        </Principal>
    </Principals>
    <Settings>
        <Enabled>true</Enabled>
        <AllowStartOnDemand>true</AllowStartOnDemand>
        <AllowHardTerminate>true</AllowHardTerminate>
    </Settings>
    <Actions>
        <Exec>
            <Command>notepad.exe</Command>
        </Exec>
    </Actions>
</Task>
```



## <a name="taskscheduler-schema-elements"></a>TaskScheduler 架構元素

以下是使用此範例時要牢記在心的一些重要元素。

-   [**RegistrationInfo**](taskschedulerschema-registrationinfo-tasktype-element.md)

    包含工作的註冊資訊。

-   [**觸發程序**](taskschedulerschema-triggers-tasktype-element.md)

    定義啟動工作的觸發程式。

-   [**CalendarTrigger**](taskschedulerschema-calendartrigger-triggergroup-element.md)

    定義每週行事曆觸發程式。 在此情況下，只會使用四個子項目：指定啟動和停用觸發程式的時間、每週排程，以及執行工作的星期幾。 [**StartBoundary**](taskschedulerschema-startboundary-triggerbasetype-element.md)元素是行事曆觸發程式的必要元素。

-   [**ScheduleByWeek**](taskschedulerschema-schedulebyweek-calendartriggertype-element.md)

    定義每週排程。 在此情況下，間隔設定為在星期一每隔一周執行工作。

-   [**主要**](taskschedulerschema-principal-principaltype-element.md)

    定義工作執行所在的安全性內容。

-   [**設定**](taskschedulerschema-settings-tasktype-element.md)

    定義工作排程器用來執行工作的工作設定。

-   [**動作**](taskschedulerschema-actions-tasktype-element.md)

    定義工作執行的動作 (在此案例中，執行 [記事本]) 。

## <a name="related-topics"></a>相關主題

<dl> <dt>

[使用工作排程器](using-the-task-scheduler.md)
</dt> </dl>

 

 




