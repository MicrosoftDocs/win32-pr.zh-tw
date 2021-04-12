---
title: 工作排程器腳本物件
description: 下列主題中所述的腳本物件，可讓您以程式設計方式存取 Visual Basic 和 Visual Basic 腳本開發人員的工作排程器中可用的功能。
ms.assetid: 632bc9ae-b300-42ed-9d2c-f1d2d53d44fb
keywords:
- 工作排程器工作排程器、參考、腳本物件
ms.topic: article
ms.date: 05/31/2018
topic_type:
- kbArticle
api_name: ''
api_type: ''
api_location: ''
ms.openlocfilehash: acf9d74ae2bf586941f3b93a6c2cbb3a84836144
ms.sourcegitcommit: a716ca2a6a22a400f02c6b31699cf4da83ee3619
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 11/04/2020
ms.locfileid: "104186647"
---
# <a name="task-scheduler-scripting-objects"></a>工作排程器腳本物件

下列主題中所述的腳本物件，可讓您以程式設計方式存取 Visual Basic 和 Visual Basic 腳本開發人員的工作排程器中可用的功能。


下列物件會在工作排程器2.0 中引進。



| Object                                                         | 描述                                                                                                                                                                                                                                           |
|----------------------------------------------------------------|-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [**動作**](action.md)                                       | 提供所有動作物件所繼承的通用屬性。                                                                                                                                                                              |
| [**Actioncollection 動作**](actioncollection.md)                   | 包含工作所執行的動作。                                                                                                                                                                                                           |
| [**BootTrigger**](boottrigger.md)                             | 表示啟動系統時啟動工作的觸發程式。                                                                                                                                                                                    |
| [**ComHandlerAction**](comhandleraction.md)                   | 表示引發處理常式的動作。                                                                                                                                                                                                            |
| [**DailyTrigger**](dailytrigger.md)                           | 表示根據每日排程啟動工作的觸發程式。                                                                                                                                                                                    |
| [**EmailAction**](emailaction.md)                             | 表示傳送電子郵件訊息的動作。                                                                                                                                                                                                     |
| [**EventTrigger**](eventtrigger.md)                           | 表示在系統事件發生時啟動工作的觸發程式。                                                                                                                                                                                   |
| [**ExecAction**](execaction.md)                               | 表示執行命令列操作的動作。                                                                                                                                                                                          |
| [**IdleSettings**](idlesettings.md)                           | 指定當電腦處於閒置狀態時，工作排程器如何執行工作。                                                                                                                                                            |
| [**IdleTrigger**](idletrigger.md)                             | 表示在發生閒置條件時啟動工作的觸發程式。                                                                                                                                                                                |
| [**LogonTrigger**](logontrigger.md)                           | 表示在使用者登入時啟動工作的觸發程式。                                                                                                                                                                                          |
| [**MonthlyDOWTrigger**](monthlydowtrigger.md)                 | 表示在每月一周的排程上啟動工作的觸發程式。                                                                                                                                                                            |
| [**MonthlyTrigger**](monthlytrigger.md)                       | 表示根據每月排程啟動工作的觸發程式。                                                                                                                                                                                  |
| [**NetworkSettings**](networksettings.md)                     | 提供工作排程器服務用來取得網路設定檔的設定。                                                                                                                                                               |
| [**主要**](principal.md)                                 | 提供主體的安全性認證。                                                                                                                                                                                                    |
| [**RegisteredTask**](registeredtask.md)                       | 提供方法，這些方法可用來立即執行工作、取得工作的任何執行中實例、取得或設定用來註冊工作的認證，以及描述工作的屬性。                                      |
| [**RegisteredTaskCollection**](registeredtaskcollection.md)   | 包含所有已註冊的工作。                                                                                                                                                                                                           |
| [**RegistrationInfo**](registrationinfo.md)                   | 提供可用來描述工作的系統管理資訊。 這項資訊包含詳細資料，例如工作的描述、工作的作者、註冊工作的日期，以及工作的安全描述項。 |
| [**RegistrationTrigger**](registrationtrigger.md)             | 表示在註冊工作時啟動工作的觸發程式。                                                                                                                                                                                  |
| [**RepetitionPattern**](repetitionpattern.md)                 | 定義工作的執行頻率，以及在工作啟動之後重複模式重複的時間長度。                                                                                                                                          |
| [**RunningTask**](runningtask.md)                             | 提供方法來取得和控制執行中工作的資訊。                                                                                                                                                                              |
| [**RunningTaskCollection**](runningtaskcollection.md)         | 用來取得執行中的工作。                                                                                                                                                                                                                      |
| [**SessionStateChangeTrigger**](sessionstatechangetrigger.md) | 用來觸發主控台連線或中斷連線、遠端連線或中斷連線，或工作站鎖定或解除鎖定通知的工作。                                                                                                                   |
| [**ShowMessageAction**](showmessageaction.md)                 | 表示在工作啟動時顯示訊息方塊的動作。                                                                                                                                                                               |
| [**TaskDefinition**](taskdefinition.md)                       | 定義工作的所有元件，例如工作設定、觸發程式、動作和註冊資訊。                                                                                                                                     |
| [**TaskFolder**](taskfolder.md)                               | 提供用來註冊 (在資料夾中建立) 工作、從資料夾中移除工作，以及從資料夾建立或移除子資料夾的方法。                                                                                           |
| [**TaskFolderCollection**](taskfoldercollection.md)           | 計算集合中的資料夾數目，並從集合中取出指定的資料夾。                                                                                                                                                   |
| [**TaskNamedValuePair**](tasknamedvaluepair.md)               | 建立名稱/值組，其中名稱與值相關聯。                                                                                                                                                                             |
| [**TaskNamedValueCollection**](tasknamedvaluecollection.md)   | 包含 [**TaskNamedValuePair**](tasknamedvaluepair.md) 物件名稱-值配對的集合。                                                                                                                                                    |
| [**TaskService**](taskservice.md)                             | 提供工作排程器服務的存取權，以管理已註冊的工作。                                                                                                                                                                          |
| [**TaskSettings**](tasksettings.md)                           | 提供工作排程器服務用來執行工作的設定。                                                                                                                                                                      |
| [**TaskVariables**](taskvariables.md)                         | 定義可作為參數傳遞給工作處理常式的工作變數，以及工作所啟動的外部可執行檔。                                                                                                                         |
| [**TimeTrigger**](timetrigger.md)                             | 表示啟動觸發程式時啟動工作的觸發程式。                                                                                                                                                                                |
| [**觸發**](trigger.md)                                     | 提供所有觸發程式物件所繼承的通用屬性。                                                                                                                                                                             |
| [**TriggerCollection**](triggercollection.md)                 | 用來新增、移除和捕獲工作的觸發程式。                                                                                                                                                                                     |
| [**WeeklyTrigger**](weeklytrigger.md)                         | 表示根據每週排程啟動工作的觸發程式。                                                                                                                                                                                   |



 

## <a name="related-topics"></a>相關主題

<dl> <dt>

[工作排程器參考](task-scheduler-reference.md)
</dt> <dt>

[工作排程器](task-scheduler-start-page.md)
</dt> </dl>

 

 




