---
title: 正在抓取工作專案屬性範例
description: 若要抓取工作專案的屬性，請呼叫 ITaskScheduler Activate 來取出工作專案物件的介面，然後呼叫適當的方法來取出您感興趣的工作屬性。
ms.assetid: d9723dea-1a82-4993-b4d0-bc7d944e775f
keywords:
- 正在工作排程器中抓取工作專案屬性
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 3519f3f995e4a5c49a58f0c8be590b34a82381bfd534b61bac6ff8aba05de33c
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/11/2021
ms.locfileid: "119059976"
---
# <a name="retrieving-work-item-property-examples"></a>正在抓取工作專案屬性範例

若要抓取工作專案的屬性，請呼叫 [**ITaskScheduler：： Activate**](/windows/desktop/api/Mstask/nf-mstask-itaskscheduler-activate) 以抓取工作專案物件的介面，然後呼叫適當的方法來取出您感興趣的工作屬性。 目前，唯一有效的工作專案是 tasks。

此頁面底部所列的程式碼範例會示範如何取得套用至所有工作專案的屬性。 如需工作特有的其他屬性，請參閱 [設定工作屬性範例](setting-task-property-examples.md)。

> [!Note]  
> 在下列程式碼範例中，不再需要所有介面之後，就會釋放它們。

 

請注意，如果您要抓取字串屬性 (例如) 的工作專案批註，則必須呼叫 [**CoTaskMemFree**](/windows/win32/api/combaseapi/nf-combaseapi-cotaskmemfree) 來釋放為傳回字串所配置的記憶體。

下列程式描述如何取出工作屬性。

**若要取出 task 屬性**

1.  呼叫 [**CoInitialize**](/windows/win32/api/objbase/nf-objbase-coinitialize) 以初始化 COM 程式庫和 [**CoCreateInstance**](/windows/win32/api/combaseapi/nf-combaseapi-cocreateinstance) ，以取得工作排程器物件。  (這些範例假設工作排程器服務正在執行。 ) 
2.  呼叫 [**ITaskScheduler：： Activate**](/windows/desktop/api/Mstask/nf-mstask-itaskscheduler-activate) 以取得 task 物件的 [**ITask**](/windows/desktop/api/Mstask/nn-mstask-itask) 介面。  (請注意，工作是目前唯一有效的工作專案類型。 ) 
3.  呼叫適當的方法，以取得您感興趣的屬性。
4.  視需要處理屬性。  (這些範例只會將屬性列印到畫面。 ) 
5.  如果傳回的屬性是字串，請呼叫 [**CoTaskMemFree**](/windows/win32/api/combaseapi/nf-combaseapi-cotaskmemfree) 來釋放針對傳回字串所配置的記憶體。



| 如需的程式碼範例                                                                        | 請參閱                                                                                                                       |
|----------------------------------------------------------------------------------------------|---------------------------------------------------------------------------------------------------------------------------|
| 取出已知工作的帳戶資訊                                           | [C/c + + 程式碼範例：正在抓取工作帳戶資訊](c-c-code-example-retrieving-task-account-information.md)       |
| 取出已知工作的批註字串                                                | [C/c + + 程式碼範例：抓取工作批註](c-c-code-example-retrieving-a-task-comment.md)                           |
| 抓取工作建立者的名稱，並將它顯示在畫面上               | [C/c + + 程式碼範例：正在抓取工作建立者](c-c-code-example-retrieving-the-task-creator.md)                       |
| 取出已知工作所傳回的最後一個結束代碼                                       | [C/c + + 程式碼範例：正在抓取工作結束代碼](c-c-code-example-retrieving-task-exit-code.md)                           |
| 抓取工作的閒置等待時間，並將它顯示在螢幕上                    | [C/c + + 程式碼範例：正在抓取工作閒置-等候時間](c-c-code-example-retrieving-task-idle-wait-time.md)                 |
| 取出工作上次執行的時間，並將它顯示在螢幕上                    | [C/c + + 程式碼範例：取出工作 MostRecentRun 時間](c-c-code-example-retrieving-the-task-mostrecentrun-time.md) |
| 在下一次工作排程執行，並在畫面上顯示該時間時，正在進行抓取 | [C/c + + 程式碼範例：取出工作 NextRun 時間](c-c-code-example-retrieving-the-task-nextrun-time.md)             |
| 抓取工作的執行時間，並將其顯示在畫面上                       | [C/c + + 程式碼範例：正在抓取工作執行時間](c-c-code-example-retrieving-task-run-times.md)                           |
| 抓取工作的目前狀態，並將其顯示在畫面上                    | [C/c + + 程式碼範例：正在抓取工作狀態](c-c-code-example-retrieving-task-status.md)                                 |



 

## <a name="related-topics"></a>相關主題

<dl> <dt>

[工作排程器1.0 範例](task-scheduler-1-0-examples.md)
</dt> </dl>

 

 