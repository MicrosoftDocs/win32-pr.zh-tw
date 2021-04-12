---
title: 建立閒置觸發程式範例
description: 若要建立閒置觸發程式，您必須在建立觸發程式時指定閒置觸發程式，而且必須設定工作的閒置時間。 如需有關閒置條件的詳細資訊，請參閱工作閒置條件。
ms.assetid: d36a621c-4011-4c3d-b6f4-b56d1f50983c
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: e6a7f8333c79d05dfade609f028f93a816e61adf
ms.sourcegitcommit: 592c9bbd22ba69802dc353bcb5eb30699f9e9403
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/20/2020
ms.locfileid: "104315925"
---
# <a name="creating-an-idle-trigger-example"></a>建立閒置觸發程式範例

若要建立閒置觸發程式，您必須在建立觸發程式時指定閒置觸發程式，而且必須設定工作的閒置時間。 如需有關閒置條件的詳細資訊，請參閱工作 [閒置條件](task-idle-conditions.md)。

建立閒置觸發程式之後，請呼叫 [**IPersistFile：： save**](/windows/win32/api/objidl/nf-objidl-ipersistfile-save) ，以將新的觸發程式儲存至磁片。

下列程式描述如何建立已知工作的閒置觸發程式。

**若要建立已知工作的閒置觸發程式**

1.  呼叫 [**CoInitialize**](/windows/win32/api/objbase/nf-objbase-coinitialize) 以初始化 COM 程式庫和 [**CoCreateInstance**](/windows/win32/api/combaseapi/nf-combaseapi-cocreateinstance) ，以取得工作排程器物件。  (此範例假設工作排程器服務正在執行。 ) 
2.  呼叫 [**ITaskScheduler：： Activate**](/windows/desktop/api/Mstask/nf-mstask-itaskscheduler-activate) 以取得 task 物件的 [**ITask**](/windows/desktop/api/Mstask/nn-mstask-itask) 介面。  (請注意，此範例會取得 "Test Task" 工作。 ) 
3.  呼叫 [**SetIdleWait**](/windows/desktop/api/Mstask/nf-mstask-ischeduledworkitem-setidlewait) 可設定系統必須保持閒置多久的時間，才會引發觸發程式。  (請注意， **SetIdleWait** 繼承自 [**IScheduledWorkItem**](/windows/desktop/api/Mstask/nn-mstask-ischeduledworkitem)。 ) 
4.  定義工作 [**\_ 觸發**](/windows/desktop/api/Mstask/ns-mstask-task_trigger) 程式結構，並呼叫 [**CreateTrigger**](/windows/desktop/api/Mstask/nf-mstask-ischeduledworkitem-createtrigger) 來建立閒置觸發程式。  (請注意， **CreateTrigger** 繼承自 [**IScheduledWorkItem**](/windows/desktop/api/Mstask/nn-mstask-ischeduledworkitem)。 ) 
5.  使用 [**IPersistFile：： save**](/windows/win32/api/objidl/nf-objidl-ipersistfile-save)，將新的閒置觸發程式儲存至磁片。 [**IPersistFile**](/windows/win32/api/objidl/nn-objidl-ipersistfile)介面 (是 [**ITask**](/windows/desktop/api/Mstask/nn-mstask-itask)介面所支援的標準 COM 介面。 ) 
6.  呼叫 **ITask：： release** 以釋放所有資源。  (請注意，[**版本**](/windows/win32/api/unknwn/nf-unknwn-iunknown-release)是 [**ITask**](/windows/desktop/api/Mstask/nn-mstask-itask)所繼承的 [**IUnknown**](/windows/win32/api/unknwn/nn-unknwn-iunknown)方法 ) 



| 如需的程式碼範例                         | 請參閱                                                                                           |
|-----------------------------------------------|-----------------------------------------------------------------------------------------------|
| 建立現有工作的閒置觸發程式 | [C/c + + 程式碼範例：建立閒置觸發程式](c-c-code-example-creating-an-idle-trigger.md) |



 

## <a name="related-topics"></a>相關主題

<dl> <dt>

[工作排程器1.0 範例](task-scheduler-1-0-examples.md)
</dt> </dl>

 

 