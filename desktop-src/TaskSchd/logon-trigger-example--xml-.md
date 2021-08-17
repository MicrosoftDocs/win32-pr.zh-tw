---
title: " (XML) 的登入觸發程式範例"
description: 此範例中的 XML 會定義在使用者登入時開始記事本的工作。
ms.assetid: c1cce95f-7558-489e-b092-c82d55b42165
ms.topic: article
ms.date: 05/31/2018
topic_type:
- kbArticle
api_name: ''
api_type: ''
api_location: ''
ms.openlocfilehash: f7e92216748a799c5cf8a3ae32393db2b33c680861b2a5d3249eb19c527474e0
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/11/2021
ms.locfileid: "117760055"
---
# <a name="logon-trigger-example-xml"></a> (XML) 的登入觸發程式範例

此範例中的 XML 會定義在使用者登入時開始記事本的工作。

若要註冊 XML 中定義的工作，您可以使用 [**ITaskFolder：： RegisterTask**](/windows/desktop/api/taskschd/nf-taskschd-itaskfolder-registertask) 函數 ([**TaskFolder. RegisterTask**](taskfolder-registertask.md) 來撰寫腳本) 或 Schtasks.exe 命令列工具。 如果您使用位於 C： \\ Windows System32 目錄) 的 Schtasks.exe 工具 (\\ ，則可以使用下列命令來註冊工作： **schtasks.exe/create/xml** *<path to the XML file containing the task definition>* **/tn** *<task name>* 。

## <a name="to-define-a-task-to-start-notepad-on-system-boot"></a>定義啟動系統開機記事本的工作

下列 XML 範例示範如何使用單一執行動作來定義工作 (啟動記事本) 、在使用者登入時啟動工作的單一登入觸發程式，以及其他會影響如何工作排程器處理工作的其他工作設定。

> [!Note]  
> 將 **UserId** 元素的值設定為工作註冊電腦上的使用者名稱。

 


```XML
<?xml version="1.0" ?>
<!--
This sample schedules a task to start notepad.exe when a user logs on.
-->
<Task xmlns="http://schemas.microsoft.com/windows/2004/02/mit/task">
    <RegistrationInfo>
        <Date>2005-10-11T13:21:17-08:00</Date>
        <Author>AuthorName</Author>
        <Version>1.0.0</Version>
        <Description>Starts Notepad when a specified user logs on.</Description>
    </RegistrationInfo>
    <Triggers>
        <LogonTrigger>
            <StartBoundary>2005-10-11T13:21:17-08:00</StartBoundary>
            <EndBoundary>2006-01-01T00:00:00-08:00</EndBoundary>
            <Enabled>true</Enabled>
            <UserId>DOMAIN_NAME\UserName</UserId>
        </LogonTrigger>
    </Triggers>
    <Principals>
        <Principal>
            <GroupId>Builtin\Administrators</GroupId>
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

以下是使用此範例時要牢記在心的一些重要元素：

-   [**RegistrationInfo**](taskschedulerschema-registrationinfo-tasktype-element.md)：包含工作的註冊資訊。
-   [**觸發**](taskschedulerschema-triggers-tasktype-element.md)程式：定義啟動工作的觸發程式。
-   [**LogonTrigger**](taskschedulerschema-logontrigger-triggergroup-element.md)：定義登入觸發程式。 在此情況下，會使用三個子項目：指定觸發程式啟動和停用時間的開始和結束界限，以及使用者識別碼的 [**UserId**](taskschedulerschema-userid-logontriggertype-element.md) 元素。 此工作會在此使用者登入電腦時啟動。
-   [**Principal**](taskschedulerschema-principal-principaltype-element.md)：定義工作執行所在的安全性內容。
-   [**設定**](taskschedulerschema-settings-tasktype-element.md)：定義工作排程器用來執行工作的工作設定。
-   [**動作**](taskschedulerschema-actions-tasktype-element.md)：定義工作執行的動作。 在此情況下，執行記事本。

## <a name="related-topics"></a>相關主題

<dl> <dt>

[使用工作排程器](using-the-task-scheduler.md)
</dt> </dl>

 

 




