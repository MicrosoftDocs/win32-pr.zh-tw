---
title: 設定工作專案屬性範例
description: 若要設定工作專案的屬性，請呼叫 ITaskScheduler Activate 來取出工作專案物件的介面，然後呼叫適當的方法來設定您感興趣的工作屬性。 目前，唯一有效的工作專案是 tasks。
ms.assetid: 80a158de-d312-499d-8ff0-b95e794cf169
keywords:
- 設定工作專案屬性工作排程器
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: e026ea3d2b3f6677a3d229e9289ab9b201e02b94
ms.sourcegitcommit: 592c9bbd22ba69802dc353bcb5eb30699f9e9403
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/20/2020
ms.locfileid: "103933454"
---
# <a name="setting-work-item-property-examples"></a>設定工作專案屬性範例

若要設定工作專案的屬性，請呼叫 [**ITaskScheduler：： Activate**](/windows/desktop/api/Mstask/nf-mstask-itaskscheduler-activate) 來取出工作專案物件的介面，然後呼叫適當的方法來設定您感興趣的工作屬性。 目前，唯一有效的工作專案是 tasks。

頁面底部所列的程式碼範例會顯示如何設定適用于所有工作專案的屬性。 如需工作特有的其他屬性，請參閱 [設定工作屬性範例](setting-task-property-examples.md)。

> [!Note]  
> 在下列程式碼範例中，不再需要所有介面之後，就會釋放它們。

 

在下列範例中，修改過的物件一律會藉由呼叫 [**IPersistFile：： Save**](/windows/win32/api/objidl/nf-objidl-ipersistfile-save)儲存至磁片。  ([**IPersistFile**](/windows/win32/api/objidl/nn-objidl-ipersistfile) 介面是 task 物件所繼承的標準 COM 介面。 ) 

下列程式描述如何設定 task 屬性。

**若要設定 task 屬性**

1.  呼叫 [**CoInitialize**](/windows/win32/api/objbase/nf-objbase-coinitialize) 以初始化 COM 程式庫和 [**CoCreateInstance**](/windows/win32/api/combaseapi/nf-combaseapi-cocreateinstance) ，以取得工作排程器物件。  (這些範例假設工作排程器服務正在執行。 ) 
2.  呼叫 [**ITaskScheduler：： Activate**](/windows/desktop/api/Mstask/nf-mstask-itaskscheduler-activate) 以取得 task 物件的 [**ITask**](/windows/desktop/api/Mstask/nn-mstask-itask) 介面。  (請注意，工作是目前唯一有效的工作專案類型。 ) 
3.  呼叫適當的 [**IScheduledWorkItem**](/windows/desktop/api/Mstask/nn-mstask-ischeduledworkitem) 方法，以設定您感興趣的屬性。 請注意， [**ITask**](/windows/desktop/api/Mstask/nn-mstask-itask)介面會繼承 **IScheduledWorkItem** 方法。
4.  呼叫 [**IPersistFile：： Save**](/windows/win32/api/objidl/nf-objidl-ipersistfile-save) 可將修改過的工作物件儲存至磁片。



| 如需的程式碼範例                            | 請參閱                                                                                                           |
|--------------------------------------------------|---------------------------------------------------------------------------------------------------------------|
| 設定已知工作的帳戶資訊 | [C/c + + 程式碼範例：設定工作帳戶資訊](c-c-code-example-setting-task-account-information.md) |
| 設定已知工作的批註              | [C/c + + 程式碼範例：設定工作批註](c-c-code-example-setting-task-comment.md)                         |



 

## <a name="related-topics"></a>相關主題

<dl> <dt>

[工作排程器1.0 範例](task-scheduler-1-0-examples.md)
</dt> </dl>

 

 