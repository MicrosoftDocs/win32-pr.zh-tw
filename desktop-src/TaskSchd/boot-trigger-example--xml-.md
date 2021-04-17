---
title: " (XML) 的開機觸發程式範例"
description: 此範例中的 XML 會定義在系統啟動時啟動「記事本」的工作。
ms.assetid: 6dd7155c-6163-4408-9cef-c313134beeb0
ms.topic: article
ms.date: 05/31/2018
topic_type:
- kbArticle
api_name: ''
api_type: ''
api_location: ''
ms.openlocfilehash: a8f9f5ea10f92979b0798b12a6225f8ba74a38ee
ms.sourcegitcommit: 40dd8501397fc79a643deb528c6c57ac2e9726ce
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/24/2020
ms.locfileid: "104314060"
---
# <a name="boot-trigger-example-xml"></a> (XML) 的開機觸發程式範例

此範例中的 XML 會定義在系統啟動時啟動「記事本」的工作。

若要註冊 XML 中定義的工作，您可以使用 [**ITaskFolder：： RegisterTask**](/windows/desktop/api/taskschd/nf-taskschd-itaskfolder-registertask) 函數 ([**TaskFolder. RegisterTask**](taskfolder-registertask.md) 來撰寫腳本) 或 Schtasks.exe 命令列工具。 如果您使用位於 C： \\ Windows System32 目錄) 的 Schtasks.exe 工具 (\\ ，則可以使用下列命令來註冊工作： **schtasks.exe/create/xml** *<path to the XML file containing the task definition>* **/tn** *<task name>* 。

## <a name="to-define-a-task-to-start-notepad-on-system-boot"></a>定義在系統開機時啟動「記事本」的工作

下列 XML 範例顯示如何使用單一執行動作來定義工作 (啟動 [記事本]) 、啟動系統時啟動工作的單一開機觸發程式，以及其他會影響工作排程器處理工作的其他工作設定。


```XML
<?xml version="1.0" ?>
<!--
This sample schedules a task to start notepad.exe when
the system is booted.
-->
<Task xmlns="http://schemas.microsoft.com/windows/2004/02/mit/task">
    <RegistrationInfo>
        <Date>2005-10-11T13:21:17-08:00</Date>
        <Author>AuthorName</Author>
        <Version>1.0.0</Version>
        <Description>Starts Notepad on system boot.</Description>
    </RegistrationInfo>
    <Triggers>
        <BootTrigger>
            <StartBoundary>2005-10-11T13:21:17-08:00</StartBoundary>
            <EndBoundary>2006-01-01T00:00:00-08:00</EndBoundary>
            <Enabled>true</Enabled>
            <ExecutionTimeLimit>PT5M</ExecutionTimeLimit>
        </BootTrigger>
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

-   [**RegistrationInfo**](taskschedulerschema-registrationinfo-tasktype-element.md)：包含工作的註冊資訊。
-   [**觸發**](taskschedulerschema-triggers-tasktype-element.md)程式：定義啟動工作的觸發程式。
-   [**BootTrigger**](taskschedulerschema-boottrigger-triggergroup-element.md)：定義開機觸發程式。 在此情況下，只會使用兩個子項目：指定啟動和停用觸發程式的時間和結束界限。
-   [**Principal**](taskschedulerschema-principal-principaltype-element.md)：定義工作執行所在的安全性內容。
-   [**設定**](taskschedulerschema-settings-tasktype-element.md)：定義工作排程器用來執行工作的工作設定。
-   [**動作**](taskschedulerschema-actions-tasktype-element.md)：定義工作執行的動作。 在此情況下，執行「記事本」。

## <a name="related-topics"></a>相關主題

<dl> <dt>

[使用工作排程器](using-the-task-scheduler.md)
</dt> </dl>

 

 




