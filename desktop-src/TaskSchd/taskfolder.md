---
title: TaskFolder 物件
description: 提供方法的腳本物件，此物件會提供用來註冊 (在資料夾中建立) 工作、從資料夾中移除工作，以及從資料夾建立或移除子資料夾的方法。
ms.assetid: f6fd09ec-2777-4903-83b5-e3ac1aa472a0
keywords:
- TaskFolder 物件工作排程器
- TaskFolder 物件工作排程器，說明
topic_type:
- apiref
api_name:
- TaskFolder
api_location:
- taskschd.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: e1ccad9331cf3df12ea5752fdd7e5ac94bfbeba6
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 12/12/2020
ms.locfileid: "104509123"
---
# <a name="taskfolder-object"></a>TaskFolder 物件

提供方法的腳本物件，此物件會提供用來註冊 (在資料夾中建立) 工作、從資料夾中移除工作，以及從資料夾建立或移除子資料夾的方法。

## <a name="members"></a>成員

**TaskFolder** 物件具有下列類型的成員：

-   [方法](#methods)
-   [屬性](#properties)

### <a name="methods"></a>方法

**TaskFolder** 物件有這些方法。



| 方法                                                              | 描述                                                                                                                                    |
|:--------------------------------------------------------------------|:-----------------------------------------------------------------------------------------------------------------------------------------------|
| [**CreateFolder**](taskfolder-createfolder.md)                     | 建立相關工作的資料夾。<br/>                                                                                                 |
| [**DeleteFolder**](taskfolder-deletefolder.md)                     | 刪除父資料夾中的子資料夾。<br/>                                                                                         |
| [**DeleteTask**](taskfolder-deletetask.md)                         | 從資料夾刪除工作。<br/>                                                                                                     |
| [**GetFolder**](taskfolder-getfolder.md)                           | 取得資料夾，其中包含指定位置的工作。<br/>                                                                          |
| [**GetFolders**](taskfolder-getfolders.md)                         | 取得資料夾中的所有子資料夾。<br/>                                                                                              |
| [**GetSecurityDescriptor**](taskfolder-getsecuritydescriptor.md)   | 取得資料夾的安全描述項。<br/>                                                                                        |
| [**GetTask**](taskfolder-gettask.md)                               | 取得資料夾中位於指定位置的工作。<br/>                                                                                    |
| [**GetTasks**](taskfolder-gettasks.md)                             | 取得資料夾中的所有工作。<br/>                                                                                                   |
| [**RegisterTask**](taskfolder-registertask.md)                     | 註冊 (會使用 XML 來定義工作，以在資料夾中建立) 新工作。<br/>                                                          |
| [**RegisterTaskDefinition**](taskfolder-registertaskdefinition.md) | 註冊 (會使用 [**ITaskDefinition**](/windows/desktop/api/taskschd/nn-taskschd-itaskdefinition) 介面來定義工作，以在指定的位置建立) 工作。<br/> |
| [**SetSecurityDescriptor**](taskfolder-setsecuritydescriptor.md)   | 設定資料夾的安全描述項。<br/>                                                                                        |



 

### <a name="properties"></a>屬性

**TaskFolder** 物件具有這些屬性。



| 屬性                                   | 存取類型          | Description                                                                        |
|:-------------------------------------------|:---------------------|:-----------------------------------------------------------------------------------|
| [**Name**](taskfolder-name.md)<br/> | 唯讀<br/> | 取得用來識別包含工作之資料夾的名稱。<br/> |
| [**路徑**](taskfolder-path.md)<br/> | 唯讀<br/> | 取得儲存資料夾的路徑。<br/>                            |



 

## <a name="examples"></a>範例

如需此腳本物件的詳細資訊和範例程式碼，請參閱[時間觸發程式範例 (腳本) ](time-trigger-example--scripting-.md)、[事件觸發程式範例 (腳本) ](https://www.bing.com/search?q=Event+Trigger+Example+(Scripting))、[每日觸發程式範例 (腳本](daily-trigger-example--scripting-.md)) 、[註冊觸發](registration-trigger-example--scripting-.md)程式範例 (腳本) 、[每週觸發](weekly-trigger-example--scripting-.md)程式範例 (腳本) 、[登入觸發](logon-trigger-example--scripting-.md)程式範例 (腳本) ，或顯示 (腳本[) 的工作](boot-trigger-example--scripting-.md)[名稱和狀態](displaying-task-names-and-state--scripting-.md)。

## <a name="requirements"></a>規格需求



| 需求 | 值 |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| 最低支援的用戶端<br/> | \[僅限 Windows Vista 桌面應用程式\]<br/>                                          |
| 最低支援的伺服器<br/> | 僅限 Windows Server 2008 \[ desktop 應用程式\]<br/>                                    |
| 類型程式庫<br/>             | <dl> <dt>Taskschd.msc .tlb</dt> </dl> |
| DLL<br/>                      | <dl> <dt>Taskschd.dll</dt> </dl> |



## <a name="see-also"></a>另請參閱

<dl> <dt>

[工作排程器物件](task-scheduler-objects.md)
</dt> <dt>

[工作排程器](task-scheduler-start-page.md)
</dt> </dl>

 

 





