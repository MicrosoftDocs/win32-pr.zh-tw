---
title: 建立新的觸發程式
description: 若要建立觸發程式，您必須使用三個介面。
ms.assetid: c0f121ff-d0a5-4b6c-935c-6f47b4ea26d5
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: f48ecb7b06e5bade6d5ad80e4c9a82794f6a17e8
ms.sourcegitcommit: 592c9bbd22ba69802dc353bcb5eb30699f9e9403
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/20/2020
ms.locfileid: "104376040"
---
# <a name="creating-a-new-trigger"></a>建立新的觸發程式

若要建立觸發程式，您必須使用三個介面。 [**IScheduledWorkItem**](/windows/desktop/api/Mstask/nn-mstask-ischeduledworkitem) 提供 [**IScheduledWorkItem：： CreateTrigger**](/windows/desktop/api/Mstask/nf-mstask-ischeduledworkitem-createtrigger) 方法來建立觸發程式物件、 [**ITaskTrigger**](/windows/desktop/api/Mstask/nn-mstask-itasktrigger) 提供 [**ITaskTrigger：： SetTrigger**](/windows/desktop/api/Mstask/nf-mstask-itasktrigger-settrigger) 方法來設定觸發程式的準則，而 COM 介面 [**IPersistFile**](/windows/win32/api/objidl/nn-objidl-ipersistfile) 提供儲存新觸發程式至磁片的 **儲存** 方法。

下列程式說明如何建立新的觸發程式。

**建立新的觸發程式**

1.  呼叫 [**CoInitialize**](/windows/win32/api/objbase/nf-objbase-coinitialize) 以初始化 COM 程式庫和 [**CoCreateInstance**](/windows/win32/api/combaseapi/nf-combaseapi-cocreateinstance) ，以取得工作排程器物件。  (此範例假設工作排程器服務正在執行。 ) 
2.  呼叫 [**ITaskScheduler：： Activate**](/windows/desktop/api/Mstask/nf-mstask-itaskscheduler-activate) 以取得 task 物件的 [**ITask**](/windows/desktop/api/Mstask/nn-mstask-itask) 介面。  (請注意，此範例會取得 "Test Task" 工作。 ) 
3.  呼叫 [**CreateTrigger**](/windows/desktop/api/Mstask/nf-mstask-ischeduledworkitem-createtrigger) 來建立觸發程式物件。  (請注意， [**CreateTrigger**](/windows/desktop/api/Mstask/nf-mstask-ischeduledworkitem-createtrigger) 繼承自 [**IScheduledWorkItem**](/windows/desktop/api/Mstask/nn-mstask-ischeduledworkitem)。 ) 
4.  定義工作 [**\_ 觸發**](/windows/desktop/api/Mstask/ns-mstask-task_trigger) 程式結構。 請注意，工作 **\_ 觸發** 程式的 wBeginDay、wBeginMonth 和 wBeginYear 成員必須分別設定為有效的日、月和年。
5.  呼叫 [**ITaskTrigger：： SetTrigger**](/windows/desktop/api/Mstask/nf-mstask-itasktrigger-settrigger) 來設定觸發準則。
6.  使用 [**IPersistFile：： save**](/windows/win32/api/objidl/nf-objidl-ipersistfile-save)，將新的觸發程式儲存至磁片。 [**IPersistFile**](/windows/win32/api/objidl/nn-objidl-ipersistfile)介面 (是 [**ITask**](/windows/desktop/api/Mstask/nn-mstask-itask)介面所支援的標準 COM 介面。 ) 
7.  呼叫 [**release**](/windows/win32/api/unknwn/nf-unknwn-iunknown-release) 以釋出所有資源。  (請注意，**版本** 是 [**ITask**](/windows/desktop/api/Mstask/nn-mstask-itask)所繼承的 [**IUnknown**](/windows/win32/api/unknwn/nn-unknwn-iunknown)方法 ) 



| 如需的程式碼範例                       | 請參閱                                                                                         |
|---------------------------------------------|---------------------------------------------------------------------------------------------|
| 為現有的工作建立新的觸發程式 | [C/c + + 程式碼範例：建立工作觸發程式](c-c-code-example-creating-a-task-trigger.md) |



 

## <a name="related-topics"></a>相關主題

<dl> <dt>

[工作排程器1.0 範例](task-scheduler-1-0-examples.md)
</dt> </dl>

 

 