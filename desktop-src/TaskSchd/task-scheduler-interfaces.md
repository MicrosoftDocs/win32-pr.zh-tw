---
title: 工作排程器介面
description: 下列主題中所述的介面，可讓您以程式設計方式存取工作排程器中可用的功能。
ms.assetid: 04d23e14-574b-4c50-880b-69cf0f40e782
keywords:
- 工作排程器工作排程器、參考、介面
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 0d9c088c1388da273b0b0a17c92e21be18e1a983
ms.sourcegitcommit: a716ca2a6a22a400f02c6b31699cf4da83ee3619
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 11/04/2020
ms.locfileid: "106968313"
---
# <a name="task-scheduler-interfaces"></a>工作排程器介面

下列主題中所述的介面，可讓您以程式設計方式存取工作排程器中可用的功能。

這些主題包含介面的描述、介面所定義之屬性和方法的清單，以及使用介面時應注意的任何特殊情況的備註。


下列是在 Windows Vista 作業系統中使用的工作排程器2.0 中引進的介面。



| 介面                                                        | 描述                                                                                                                                                                                                                                                                                       |
|------------------------------------------------------------------|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [**IAction**](/windows/desktop/api/taskschd/nn-taskschd-iaction)                                       | 提供所有動作物件所繼承的通用屬性。                                                                                                                                                                                                                          |
| [**IActionCollection**](/windows/desktop/api/taskschd/nn-taskschd-iactioncollection)                   | 包含工作所執行的動作。 其方法可以用來新增、移除和取出工作的動作。                                                                                                                                                          |
| [**IBootTrigger**](/windows/desktop/api/taskschd/nn-taskschd-iboottrigger)                             | 表示啟動系統時啟動工作的觸發程式。                                                                                                                                                                                                                               |
| [**IComHandlerAction**](/windows/desktop/api/taskschd/nn-taskschd-icomhandleraction)                   | 表示引發處理常式的動作。                                                                                                                                                                                                                                                        |
| [**IDailyTrigger**](/windows/desktop/api/taskschd/nn-taskschd-idailytrigger)                           | 表示根據每日排程啟動工作的觸發程式。                                                                                                                                                                                                                                |
| [**IEmailAction**](/windows/desktop/api/taskschd/nn-taskschd-iemailaction)                             | 表示傳送電子郵件訊息的動作。                                                                                                                                                                                                                                                 |
| [**IEventTrigger**](/windows/desktop/api/taskschd/nn-taskschd-ieventtrigger)                           | 表示在系統事件發生時啟動工作的觸發程式。                                                                                                                                                                                                                               |
| [**IExecAction**](/windows/desktop/api/taskschd/nn-taskschd-iexecaction)                               | 表示執行命令列操作的動作。                                                                                                                                                                                                                                      |
| [**IIdleSettings**](/windows/desktop/api/taskschd/nn-taskschd-iidlesettings)                           | 指定當電腦處於閒置狀態時，工作排程器如何執行工作。                                                                                                                                                                                                        |
| [**IIdleTrigger**](/windows/win32/api/taskschd/nn-taskschd-iidletrigger)                             | 代表當電腦進入閒置狀態時啟動工作的觸發程式。                                                                                                                                                                                                                |
| [**ILogonTrigger**](/windows/desktop/api/taskschd/nn-taskschd-ilogontrigger)                           | 表示在使用者登入時啟動工作的觸發程式。                                                                                                                                                                                                                                      |
| [**IMaintenanceSettings**](/windows/desktop/api/taskschd/nn-taskschd-imaintenancesettings)             | 提供工作排程器在自動維護期間用來執行工作的設定。                                                                                                                                                                                                  |
| [**IMonthlyDOWTrigger**](/windows/desktop/api/taskschd/nn-taskschd-imonthlydowtrigger)                 | 表示在每月一周的排程上啟動工作的觸發程式。                                                                                                                                                                                                                        |
| [**IMonthlyTrigger**](/windows/desktop/api/taskschd/nn-taskschd-imonthlytrigger)                       | 表示根據每月排程啟動工作的觸發程式。                                                                                                                                                                                                                              |
| [**INetworkSettings**](/windows/desktop/api/taskschd/nn-taskschd-inetworksettings)                     | 提供工作排程器服務用來取得網路設定檔的設定。                                                                                                                                                                                                           |
| [**IPrincipal**](/windows/desktop/api/taskschd/nn-taskschd-iprincipal)                                 | 提供主體的安全性認證。                                                                                                                                                                                                                                                |
| [**IPrincipal2**](/windows/desktop/api/taskschd/nn-taskschd-iprincipal2)                               | 提供主體的額外安全性認證。                                                                                                                                                                                                                                         |
| [**IRegisteredTask**](/windows/desktop/api/taskschd/nn-taskschd-iregisteredtask)                       | 提供方法，這些方法可用來立即執行工作、取得工作的任何執行中實例、取得或設定用來註冊工作的認證，以及描述工作的屬性。                                                                                  |
| [**IRegisteredTaskCollection**](/windows/desktop/api/taskschd/nn-taskschd-iregisteredtaskcollection)   | 包含所有已註冊的工作。                                                                                                                                                                                                                                                       |
| [**IRegistrationInfo**](/windows/desktop/api/taskschd/nn-taskschd-iregistrationinfo)                   | 提供可用來描述工作的系統管理資訊。 這項資訊包含詳細資料，例如工作的描述、工作的作者、註冊工作的日期，以及工作的安全描述項。                                             |
| [**IRegistrationTrigger**](/windows/desktop/api/taskschd/nn-taskschd-iregistrationtrigger)             | 表示在註冊工作時啟動工作的觸發程式。                                                                                                                                                                                                                              |
| [**IRepetitionPattern**](/windows/desktop/api/taskschd/nn-taskschd-irepetitionpattern)                 | 定義工作的執行頻率，以及在工作啟動之後重複模式重複的時間長度。                                                                                                                                                                                      |
| [**IRunningTask**](/windows/desktop/api/taskschd/nn-taskschd-irunningtask)                             | 提供方法來取得和控制執行中工作的資訊。                                                                                                                                                                                                                          |
| [**IRunningTaskCollection**](/windows/desktop/api/taskschd/nn-taskschd-irunningtaskcollection)         | 提供用來控制正在執行之工作的集合。                                                                                                                                                                                                                                      |
| [**ISessionStateChangeTrigger**](/windows/desktop/api/taskschd/nn-taskschd-isessionstatechangetrigger) | 觸發主控台連線或中斷連線、遠端連線或中斷連線，或工作站鎖定或解除鎖定通知的工作。                                                                                                                                                                      |
| [**IShowMessageAction**](/windows/desktop/api/taskschd/nn-taskschd-ishowmessageaction)                 | 表示在工作啟動時顯示訊息方塊的動作。                                                                                                                                                                                                                           |
| [**ITaskDefinition**](/windows/desktop/api/taskschd/nn-taskschd-itaskdefinition)                       | 定義工作的所有元件，例如工作設定、觸發程式、動作和註冊資訊。                                                                                                                                                                                 |
| [**ITaskFolder**](/windows/desktop/api/taskschd/nn-taskschd-itaskfolder)                               | 提供用來註冊 (在資料夾中建立) 工作、從資料夾中移除工作，以及從資料夾建立或移除子資料夾的方法。                                                                                                                                       |
| [**ITaskFolderCollection**](/windows/desktop/api/taskschd/nn-taskschd-itaskfoldercollection)           | 提供包含工作之資料夾集合的資訊和控制項。                                                                                                                                                                                                                  |
| [**ITaskHandler**](/windows/desktop/api/taskschd/nn-taskschd-itaskhandler)                             | 定義工作排程器服務呼叫以管理 COM 處理常式的方法。                                                                                                                                                                                                        |
| [**ITaskHandlerStatus**](/windows/desktop/api/taskschd/nn-taskschd-itaskhandlerstatus)                 | 提供 COM 處理常式用來通知工作排程器有關處理常式狀態的方法。                                                                                                                                                                                  |
| [**ITaskNamedValuePair**](/windows/desktop/api/taskschd/nn-taskschd-itasknamedvaluepair)               | 建立名稱/值組，其中名稱與值相關聯。                                                                                                                                                                                                                         |
| [**ITaskNamedValueCollection**](/windows/desktop/api/taskschd/nn-taskschd-itasknamedvaluecollection)   | 包含 [**ITaskNamedValuePair**](/windows/desktop/api/taskschd/nn-taskschd-itasknamedvaluepair) 介面名稱/值配對的集合。                                                                                                                                                                                           |
| [**ITaskService**](/windows/desktop/api/taskschd/nn-taskschd-itaskservice)                             | 提供工作排程器服務的存取權，以管理已註冊的工作。                                                                                                                                                                                                                      |
| [**ITaskSettings**](/windows/desktop/api/taskschd/nn-taskschd-itasksettings)                           | 提供工作排程器服務用來執行工作的設定。                                                                                                                                                                                                                   |
| [**ITaskSettings2**](/windows/desktop/api/taskschd/nn-taskschd-itasksettings2)                         | 提供工作排程器用來執行工作的其他設定。                                                                                                                                                                                                                    |
| [**ITaskVariables**](/windows/desktop/api/taskschd/nn-taskschd-itaskvariables)                         | 定義可作為參數傳遞給工作處理常式的工作變數，以及工作所啟動的外部可執行檔。 需要對工作變數輸入和輸出資料的工作處理常式，應該在 [**ITaskVariables**](/windows/desktop/api/taskschd/nn-taskschd-itaskvariables)的服務指標上進行查詢介面。 |
| [**ITimeTrigger**](/windows/desktop/api/taskschd/nn-taskschd-itimetrigger)                             | 表示啟動觸發程式時啟動工作的觸發程式。                                                                                                                                                                                                                            |
| [**ITrigger**](/windows/desktop/api/taskschd/nn-taskschd-itrigger)                                     | 提供所有觸發程式介面所繼承的通用屬性。                                                                                                                                                                                                                      |
| [**ITriggerCollection**](/windows/desktop/api/taskschd/nn-taskschd-itriggercollection)                 | 提供方法，這些方法可用來加入、移除和取得工作的觸發程式。                                                                                                                                                                                                        |
| [**IWeeklyTrigger**](/windows/desktop/api/taskschd/nn-taskschd-iweeklytrigger)                         | 表示根據每週排程啟動工作的觸發程式。                                                                                                                                                                                                                               |



 


> [!WARNING]
> 工作排程器1.0 介面只能在 Windows 2000、Windows XP 及 Windows Server 2003 作業系統中使用。 它們已在 Windows Vista 中淘汰，未來可能會完全移除。 請改用上面所列的工作排程器2.0 介面。

 

 

 