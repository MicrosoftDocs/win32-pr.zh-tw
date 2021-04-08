---
title: " (XML) 的每日觸發程式範例"
description: 此範例中的 XML 會定義一項工作，該工作會在每天上午 8 00 啟動「記事本」。
ms.assetid: b7818071-12b6-41df-85b9-282c08cf6e31
ms.topic: article
ms.date: 05/31/2018
topic_type:
- kbArticle
api_name: ''
api_type: ''
api_location: ''
ms.openlocfilehash: fe673a764e6e7e4e3ae5089022da2232821d9184
ms.sourcegitcommit: 40dd8501397fc79a643deb528c6c57ac2e9726ce
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/24/2020
ms.locfileid: "103679524"
---
# <a name="daily-trigger-example-xml"></a> (XML) 的每日觸發程式範例

此範例中的 XML 會定義一項工作，該工作會在每天上午8:00 啟動「記事本」。 此範例也會顯示如何設定觸發程式的重複模式，以重複執行工作。

若要註冊 XML 中定義的工作，您可以使用 [**ITaskFolder：： RegisterTask**](/windows/desktop/api/taskschd/nf-taskschd-itaskfolder-registertask) 函數 ([**TaskFolder. RegisterTask**](taskfolder-registertask.md) 來撰寫腳本) 或 Schtasks.exe 命令列工具。 如果您使用位於 C： \\ Windows System32 目錄) 的 Schtasks.exe 工具 (\\ ，則可以使用下列命令來註冊工作： **schtasks.exe/create/xml** *<path to the XML file containing the task definition>* **/tn** *<task name>* 。

## <a name="to-define-a-task-to-start-notepad-every-day-at-800-am"></a>定義在每天上午8:00 啟動「記事本」的工作

下列 XML 範例示範如何使用單一執行動作來定義工作 (啟動 [記事本]) 、單一行事曆觸發程式 (在每天上午8:00 點啟動工作) ，以及其他數個會影響工作如何由工作排程器處理的工作設定。


```XML
<?xml version="1.0" ?>
<!--
This sample schedules a task to start on a daily basis.
-->
<Task xmlns="http://schemas.microsoft.com/windows/2004/02/mit/task">
    <RegistrationInfo>
        <Date>2005-10-11T13:21:17-08:00</Date>
        <Author>AuthorName</Author>
        <Version>1.0.0</Version>
        <Description>Notepad starts every day.</Description>
    </RegistrationInfo>
    <Triggers>
        <CalendarTrigger>
            <StartBoundary>2005-10-11T13:21:17-08:00</StartBoundary>
            <EndBoundary>2006-01-01T00:00:00-08:00</EndBoundary>
            <Repetition>
                <Interval>PT1M</Interval>
                <Duration>PT4M</Duration>
            </Repetition>
            <ScheduleByDay>
                <DaysInterval>1</DaysInterval>
            </ScheduleByDay>
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

    定義每日行事曆觸發程式。 在此情況下，會使用四個子項目：指定觸發程式啟動和停用時間、每日排程，以及工作的重複模式的開始和結束界限。 [**StartBoundary**](taskschedulerschema-startboundary-triggerbasetype-element.md)元素是行事曆觸發程式的必要元素。

-   [**ScheduleByDay**](taskschedulerschema-schedulebyday-calendartriggertype-element.md)

    定義每日排程。 在此情況下，間隔會設定為每天執行工作。

-   [**Principal**](taskschedulerschema-principal-principaltype-element.md)：定義工作執行所在的安全性內容。
-   [**設定**](taskschedulerschema-settings-tasktype-element.md)

    定義工作排程器用來執行工作的工作設定。

-   [**動作**](taskschedulerschema-actions-tasktype-element.md)

    定義工作執行的動作 (在此案例中，執行 [記事本]) 。

## <a name="related-topics"></a>相關主題

<dl> <dt>

[使用工作排程器](using-the-task-scheduler.md)
</dt> </dl>

 

 




