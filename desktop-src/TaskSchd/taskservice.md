---
title: TaskService 物件
description: 針對腳本，提供存取工作排程器服務來管理已註冊的工作。
ms.assetid: 6ddd43dc-d027-4792-a53b-07fe4d4a3576
keywords:
- TaskService 物件工作排程器
- TaskService 物件工作排程器，說明
topic_type:
- apiref
api_name:
- TaskService
- HighestVersion
api_location:
- taskschd.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 74f20840a5580d0188354ca6b65ab3ce5b7402d57ea7346462d2f990ecfe34cf
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/11/2021
ms.locfileid: "119658648"
---
# <a name="taskservice-object"></a>TaskService 物件

針對腳本，提供存取工作排程器服務來管理已註冊的工作。

在呼叫任何其他 **TaskService** 方法之前，應該先呼叫 [**連線 TaskService**](taskservice-connect.md)方法。

## <a name="members"></a>成員

**TaskService** 物件具有下列類型的成員：

-   [方法](#methods)
-   [屬性](#properties)

### <a name="methods"></a>方法

**TaskService** 物件有這些方法。



| 方法                                                 | 描述                                                                                                                                                                                                          |
|:-------------------------------------------------------|:---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [**連線**](taskservice-connect.md)                 | 連接至遠端電腦，並將此介面上的所有後續呼叫與遠端會話產生關聯。<br/>                                                                                                 |
| [**GetFolder**](taskservice-getfolder.md)             | 取得已註冊工作的資料夾路徑。<br/>                                                                                                                                                            |
| [**GetRunningTasks**](taskservice-getrunningtasks.md) | 取得正在執行之工作的集合。<br/>                                                                                                                                                                       |
| [**NewTask**](taskservice-newtask.md)                 | 傳回要填入設定和屬性的空白工作定義物件，然後使用 [**TaskFolder. RegisterTaskDefinition**](taskfolder-registertaskdefinition.md) 方法進行註冊。<br/> |



 

### <a name="properties"></a>屬性

**TaskService** 物件具有這些屬性。



| 屬性                                                          | 描述                                                                                                                 |
|:------------------------------------------------------------------|:----------------------------------------------------------------------------------------------------------------------------|
| [**連線**](taskservice-connected.md)<br/>             | 取得布林值，指出您是否連接到工作排程器服務。<br/>                          |
| [**ConnectedDomain**](taskservice-connecteddomain.md)<br/> | 取得 [**TargetServer**](taskservice-targetserver.md) 電腦所連接之網域的名稱。<br/> |
| [**>connecteduser**](taskservice-connecteduser.md)<br/>     | 取得連接到工作排程器服務之使用者的名稱。<br/>                                       |
| HighestVersion<br/>                                         | 取得電腦支援之工作排程器的最高版本。<br/>                                             |
| [**TargetServer**](taskservice-targetserver.md)<br/>       | 取得正在執行使用者所連接之工作排程器服務的電腦名稱稱。<br/>          |



 

## <a name="examples"></a>範例

如需此腳本物件的詳細資訊和範例程式碼，請參閱[時間觸發程式範例 (腳本) ](time-trigger-example--scripting-.md)、[事件觸發程式範例 (腳本) ](https://www.bing.com/search?q=Event+Trigger+Example+(Scripting))、[每日觸發程式範例 (腳本](daily-trigger-example--scripting-.md)) 、[註冊觸發](registration-trigger-example--scripting-.md)程式範例 (腳本) 、[每週觸發](weekly-trigger-example--scripting-.md)程式範例 (腳本) 、[登入觸發](logon-trigger-example--scripting-.md)程式範例 (腳本) ，或顯示 (腳本[) 的工作](boot-trigger-example--scripting-.md)[名稱和狀態](displaying-task-names-and-state--scripting-.md)。

## <a name="requirements"></a>規格需求



| 需求 | 值 |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| 最低支援的用戶端<br/> | Windows\[僅限 Vista desktop 應用程式\]<br/>                                          |
| 最低支援的伺服器<br/> | Windows\[僅限 Server 2008 desktop 應用程式\]<br/>                                    |
| 類型程式庫<br/>             | <dl> <dt>Taskschd.msc .tlb</dt> </dl> |
| DLL<br/>                      | <dl> <dt>Taskschd.dll</dt> </dl> |



## <a name="see-also"></a>另請參閱

<dl> <dt>

[工作排程器](task-scheduler-start-page.md)
</dt> </dl>

 

 





