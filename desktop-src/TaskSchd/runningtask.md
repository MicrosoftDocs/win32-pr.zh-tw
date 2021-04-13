---
title: RunningTask 物件
description: 提供方法的腳本物件，這些方法可從執行中的工作取得資訊及控制其運作方式。
ms.assetid: 335e69d8-affa-4845-a067-641184e0f7df
keywords:
- RunningTask 物件工作排程器
- RunningTask 物件工作排程器，說明
topic_type:
- apiref
api_name:
- RunningTask
api_location:
- taskschd.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 261be07f71d0d35f5d3140de1b39574b635a531e
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 12/12/2020
ms.locfileid: "104508863"
---
# <a name="runningtask-object"></a>RunningTask 物件

提供方法的腳本物件，這些方法可從執行中的工作取得資訊及控制其運作方式。

## <a name="members"></a>成員

**RunningTask** 物件具有下列類型的成員：

-   [方法](#methods)
-   [屬性](#properties)

### <a name="methods"></a>方法

**RunningTask** 物件有這些方法。



| 方法                                 | 描述                                                           |
|:---------------------------------------|:----------------------------------------------------------------------|
| [**重新整理**](runningtask-refresh.md) | 重新整理工作的所有本機執行個體變數。<br/> |
| [**停止**](runningtask-stop.md)       | 停止此工作的實例。<br/>                           |



 

### <a name="properties"></a>屬性

**RunningTask** 物件具有這些屬性。



| 屬性                                                      | 存取類型          | Description                                                                         |
|:--------------------------------------------------------------|:---------------------|:------------------------------------------------------------------------------------|
| [**CurrentAction**](runningtask-currentaction.md)<br/> | 唯讀<br/> | 取得正在執行之工作正在執行之目前動作的名稱。<br/> |
| [**EnginePID**](runningtask-enginepid.md)<br/>         | 唯讀<br/> | 取得正在執行工作之引擎 (進程) 的處理序識別碼。<br/>  |
| [**InstanceGuid**](runningtask-instanceguid.md)<br/>   | 唯讀<br/> | 取得此工作實例的 GUID 識別碼。<br/>                  |
| [**Name**](runningtask-name.md)<br/>                   | 唯讀<br/> | 取得工作的名稱。<br/>                                               |
| [**路徑**](runningtask-path.md)<br/>                   | 唯讀<br/> | 取得工作儲存位置的路徑。<br/>                               |
| [**狀態**](runningtask-state.md)<br/>                 | 唯讀<br/> | 取得正在執行之工作的狀態。 <br/>                                     |



 

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
</dt> <dt>

[**RunningTaskCollection**](runningtaskcollection.md)
</dt> <dt>

[**RegisteredTask。執行**](registeredtask-run.md)
</dt> <dt>

[**RegisteredTask.RunEx**](registeredtask-runex.md)
</dt> </dl>

 

 





