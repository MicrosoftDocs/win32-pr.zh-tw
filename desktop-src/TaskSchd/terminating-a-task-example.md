---
title: 終止工作範例
description: 您可以藉由呼叫 IScheduledWorkItem Terminate 來終止執行中的工作。
ms.assetid: f8401650-e196-4959-8f23-3d649a55f73d
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 73e632b00a9e957849a5735d31018e3444113190
ms.sourcegitcommit: 592c9bbd22ba69802dc353bcb5eb30699f9e9403
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/20/2020
ms.locfileid: "104186046"
---
# <a name="terminating-a-task-example"></a>終止工作範例

您可以藉由呼叫 [**IScheduledWorkItem：： terminate**](/windows/desktop/api/Mstask/nf-mstask-ischeduledworkitem-terminate)來終止正在執行的工作。

下列程式說明如何在工作正在執行時終止工作。

**若要終止執行中的工作**

1.  呼叫 [**CoInitialize**](/windows/win32/api/objbase/nf-objbase-coinitialize) 以初始化 COM 程式庫和 [**CoCreateInstance**](/windows/win32/api/combaseapi/nf-combaseapi-cocreateinstance) ，以取得工作排程器物件。  (此範例假設工作排程器服務正在執行。 ) 
2.  呼叫 [**ITaskScheduler：： Activate**](/windows/desktop/api/Mstask/nf-mstask-itaskscheduler-activate) 以取得 task 物件的 [**ITask**](/windows/desktop/api/Mstask/nn-mstask-itask) 介面。  (請注意，此範例會取得 "Test Task" 工作。 ) 
3.  呼叫 **ITask：： GetStatus** ，以找出工作是否正在執行。  (請注意， [**GetStatus**](/windows/desktop/api/Mstask/nf-mstask-ischeduledworkitem-getstatus)是 [**ITask**](/windows/desktop/api/Mstask/nn-mstask-itask)所繼承的 [**IScheduledWorkItem**](/windows/desktop/api/Mstask/nn-mstask-ischeduledworkitem)方法 ) 。
4.  檢查工作的狀態，然後呼叫 **ITask：： Terminate** （如果工作正在執行中）。  (請注意， [**Terminate**](/windows/desktop/api/Mstask/nf-mstask-ischeduledworkitem-terminate)是 [**ITask**](/windows/desktop/api/Mstask/nn-mstask-itask)所繼承的 [**IScheduledWorkItem**](/windows/desktop/api/Mstask/nn-mstask-ischeduledworkitem)方法。 ) 



| 如需的程式碼範例                | 請參閱                                                                               |
|--------------------------------------|-----------------------------------------------------------------------------------|
| 驗證已知工作的狀態 | [C/c + + 程式碼範例：終止工作](c-c-code-example-terminating-a-task.md) |



 

## <a name="related-topics"></a>相關主題

<dl> <dt>

[工作排程器1.0 範例](task-scheduler-1-0-examples.md)
</dt> </dl>

 

 