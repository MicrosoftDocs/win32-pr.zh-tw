---
title: 正在抓取觸發字串範例
description: 您可以使用 IScheduledWorkItem 或 ITaskTrigger 介面，根據您正在使用的物件類型，取得已知觸發程式的觸發程式字串。
ms.assetid: adfa95b1-54f0-4bcd-a260-ca76fd77d43e
keywords:
- 正在抓取觸發字串工作排程器
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: f44708fdbb4025f5d99409297dda65504a909aec
ms.sourcegitcommit: 592c9bbd22ba69802dc353bcb5eb30699f9e9403
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/20/2020
ms.locfileid: "106968294"
---
# <a name="retrieving-trigger-strings-example"></a>正在抓取觸發字串範例

您可以使用 [**IScheduledWorkItem**](/windows/desktop/api/Mstask/nn-mstask-ischeduledworkitem) 或 [**ITaskTrigger**](/windows/desktop/api/Mstask/nn-mstask-itasktrigger) 介面，根據您正在使用的物件類型，取得已知觸發程式的觸發程式字串。

使用工作 [*物件*](t.md)時，請使用 [**IScheduledWorkItem**](/windows/desktop/api/Mstask/nn-mstask-ischeduledworkitem) 介面的方法來取得工作專案的觸發程式字串。

當您使用工作觸發程式 [*物件*](t.md)時，請使用 [**ITaskTrigger**](/windows/desktop/api/Mstask/nn-mstask-itasktrigger) 介面的方法來取出觸發程式的觸發程式字串。

下列範例示範如何使用 [**IScheduledWorkItem：： GetTriggerString**](/windows/desktop/api/Mstask/nf-mstask-ischeduledworkitem-gettriggerstring) 來顯示與已知工作相關聯之所有觸發程式的字串。

下列程式描述如何取出工作的觸發程式字串。

**取得工作的觸發程式字串**

1.  呼叫 [**CoInitialize**](/windows/win32/api/objbase/nf-objbase-coinitialize) 以初始化 COM 程式庫和 [**CoCreateInstance**](/windows/win32/api/combaseapi/nf-combaseapi-cocreateinstance) ，以取得工作排程器物件。  (此範例假設工作排程器服務正在執行。 ) 
2.  呼叫 [**ITaskScheduler：： Activate**](/windows/desktop/api/Mstask/nf-mstask-itaskscheduler-activate) 以取得 task 物件的 [**ITask**](/windows/desktop/api/Mstask/nn-mstask-itask) 介面。  (請注意，此範例會取得 "Test Task" 工作。 ) 
3.  呼叫 **ITask：： GetTriggerCount** ，找出與工作相關聯的觸發程式數目。  (請注意， [**GetTriggerCount**](/windows/desktop/api/Mstask/nf-mstask-ischeduledworkitem-gettriggercount)是 [**ITask**](/windows/desktop/api/Mstask/nn-mstask-itask)所繼承的 [**IScheduledWorkItem**](/windows/desktop/api/Mstask/nn-mstask-ischeduledworkitem)方法 ) 。
4.  顯示觸發字串，針對與工作相關聯的每個觸發程式呼叫 **ITask：： GetTriggerString** 。  (請注意， [**GetTriggerString**](/windows/desktop/api/Mstask/nf-mstask-ischeduledworkitem-gettriggerstring)是 [**ITask**](/windows/desktop/api/Mstask/nn-mstask-itask)所繼承的 [**IScheduledWorkItem**](/windows/desktop/api/Mstask/nn-mstask-ischeduledworkitem)方法 ) 。
5.  釋放所有資源。 呼叫 [**CoTaskMemFree**](/windows/win32/api/combaseapi/nf-combaseapi-cotaskmemfree) 來釋放觸發字串和 **ITask：： release** 以釋出 [**ITask**](/windows/desktop/api/Mstask/nn-mstask-itask) 介面。  (請注意，[**版本**](/windows/win32/api/unknwn/nf-unknwn-iunknown-release)是 **ITask** 所繼承的 [**IUnknown**](/windows/win32/api/unknwn/nn-unknwn-iunknown)方法 ) 



| 如需的程式碼範例                                                         | 請參閱                                                                                         |
|-------------------------------------------------------------------------------|---------------------------------------------------------------------------------------------|
| 針對與已知工作相關聯的所有觸發程式抓取觸發字串 | [程式碼範例：正在抓取觸發字串](c-c-code-example-retrieving-trigger-strings.md) |



 

## <a name="related-topics"></a>相關主題

<dl> <dt>

[工作排程器1.0 範例](task-scheduler-1-0-examples.md)
</dt> </dl>

 

 