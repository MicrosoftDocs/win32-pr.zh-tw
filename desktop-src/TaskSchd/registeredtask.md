---
title: RegisteredTask 物件
description: 腳本物件，提供用來立即執行工作的方法、取得工作的任何執行中實例、取得或設定用來註冊工作的認證，以及描述工作的屬性。
ms.assetid: d280f22b-4dd1-44df-be12-286fb1c029a3
keywords:
- RegisteredTask 物件工作排程器
- RegisteredTask 物件工作排程器，說明
topic_type:
- apiref
api_name:
- RegisteredTask
api_location:
- taskschd.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: c7ce300375e5122a7b63266c0cd21cdddf34606b
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 12/12/2020
ms.locfileid: "103685650"
---
# <a name="registeredtask-object"></a>RegisteredTask 物件

腳本物件，提供用來立即執行工作的方法、取得工作的任何執行中實例、取得或設定用來註冊工作的認證，以及描述工作的屬性。

## <a name="members"></a>成員

**RegisteredTask** 物件具有下列類型的成員：

-   [方法](#methods)
-   [屬性](#properties)

### <a name="methods"></a>方法

**RegisteredTask** 物件有這些方法。



| 方法                                                                | 描述                                                                                     |
|:----------------------------------------------------------------------|:------------------------------------------------------------------------------------------------|
| [**GetInstances**](registeredtask-getinstances.md)                   | 傳回目前正在執行之已註冊工作的所有實例。<br/>             |
| [**GetRunTimes**](/windows/desktop/api/taskschd/nf-taskschd-iregisteredtask-getruntimes)                    | 取得已註冊的工作排定在指定時間執行的時間。<br/> |
| [**GetSecurityDescriptor**](registeredtask-getsecuritydescriptor.md) | 取得用來做為已註冊工作之認證的安全描述項。<br/>    |
| [**執行**](registeredtask-run.md)                                     | 立即執行已註冊的工作。<br/>                                                |
| [**RunEx**](registeredtask-runex.md)                                 | 使用指定的旗標和會話識別碼，立即執行已註冊的工作。<br/> |
| [**SetSecurityDescriptor**](registeredtask-setsecuritydescriptor.md) | 設定用來作為已註冊工作認證的安全描述項。<br/>    |
| [**停止**](registeredtask-stop.md)                                   | 立即停止已註冊的工作。<br/>                                               |



 

### <a name="properties"></a>屬性

**RegisteredTask** 物件具有這些屬性。



| 屬性                                                                   | 存取類型           | Description                                                                               |
|:---------------------------------------------------------------------------|:----------------------|:------------------------------------------------------------------------------------------|
| [**定義**](registeredtask-definition.md)<br/>                 | 唯讀<br/>  | 取得工作的定義。<br/>                                               |
| [**啟用**](registeredtask-enabled.md)<br/>                       | 讀取/寫入<br/> | 取得或設定布林值，這個值會指出是否已啟用註冊的工作。<br/>  |
| [**LastRunTime**](registeredtask-lastruntime.md)<br/>               | 唯讀<br/>  | 取得上次執行註冊工作的時間。<br/>                                |
| [**LastTaskResult**](registeredtask-lasttaskresult.md)<br/>         | 唯讀<br/>  | 取得上次執行註冊工作時所傳回的結果。<br/> |
| [**Name**](registeredtask-name.md)<br/>                             | 唯讀<br/>  | 取得已註冊工作的名稱。<br/>                                          |
| [**NextRunTime**](registeredtask-nextruntime.md)<br/>               | 唯讀<br/>  | 取得已註冊的工作下次排程執行的時間。<br/>               |
| [**NumberOfMissedRuns**](registeredtask-numberofmissedruns.md)<br/> | 唯讀<br/>  | 取得已註冊的工作已錯過排程執行的次數。<br/>       |
| [**路徑**](registeredtask-path.md)<br/>                             | 唯讀<br/>  | 取得已註冊的工作儲存位置的路徑。<br/>                          |
| [**狀態**](registeredtask-state.md)<br/>                           | 唯讀<br/>  | 取得已註冊工作的操作狀態。<br/>                             |
| [**XML**](registeredtask-xml.md)<br/>                               | 唯讀<br/>  | 取得已註冊工作的 XML 格式註冊資訊。<br/>       |



 

## <a name="examples"></a>範例

如需此腳本物件的詳細資訊和範例程式碼，請參閱 [時間觸發程式範例 (腳本) ](time-trigger-example--scripting-.md) ，以及 [顯示 (腳本) 的工作名稱和狀態 ](displaying-task-names-and-state--scripting-.md)。

## <a name="requirements"></a>規格需求



| 需求 | 值 |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| 最低支援的用戶端<br/> | \[僅限 Windows Vista 桌面應用程式\]<br/>                                          |
| 最低支援的伺服器<br/> | 僅限 Windows Server 2008 \[ desktop 應用程式\]<br/>                                    |
| 類型程式庫<br/>             | <dl> <dt>Taskschd.msc .tlb</dt> </dl> |
| DLL<br/>                      | <dl> <dt>Taskschd.dll</dt> </dl> |



 

 





