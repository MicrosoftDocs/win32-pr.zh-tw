---
title: 正在抓取工作屬性範例
description: 若要抓取工作的屬性，請呼叫 ITaskScheduler Activate 來取得工作物件的介面，然後呼叫適當的 ITask 方法來取出您感興趣的工作屬性。
ms.assetid: 9ec9d836-c735-4a32-96b1-3dbd0a31b22a
keywords:
- 正在工作排程器中抓取工作屬性
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 7e2b42bc8044171834b6d99e97c41e3f5c7048ff
ms.sourcegitcommit: 592c9bbd22ba69802dc353bcb5eb30699f9e9403
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/20/2020
ms.locfileid: "104316048"
---
# <a name="retrieving-task-property-examples"></a>正在抓取工作屬性範例

若要抓取工作的屬性，請呼叫 [**ITaskScheduler：： Activate**](/windows/desktop/api/Mstask/nf-mstask-itaskscheduler-activate) 以取得工作物件的介面，然後呼叫適當的 [**ITask**](/windows/desktop/api/Mstask/nn-mstask-itask) 方法來取出您感興趣的工作屬性。 頁面底部所列的程式碼範例會顯示如何取出不同的工作屬性。

頁面底部所列的程式碼範例會顯示如何抓取工作物件特有的屬性。 針對也適用于工作的其他 [*工作專案*](w.md) 屬性，請參閱抓取 [工作專案範例](retrieving-work-item-property-examples.md)。

> [!Note]  
> 在下列程式碼範例中，不再需要所有介面之後，就會釋放它們。

 

請注意，如果您要抓取 (的字串屬性，例如應用程式名稱、參數或工作目錄) ，您必須呼叫 [CoTaskMemFree](/windows/win32/api/combaseapi/nf-combaseapi-cotaskmemfree) 來釋放為傳回字串所配置的記憶體。

下列程式描述如何取出工作屬性。

**若要取出 task 屬性**

1.  呼叫 [**CoInitialize**](/windows/win32/api/objbase/nf-objbase-coinitialize) 以初始化 COM 程式庫和 [**CoCreateInstance**](/windows/win32/api/combaseapi/nf-combaseapi-cocreateinstance) ，以取得工作排程器物件。  (這些範例假設工作排程器服務正在執行。 ) 
2.  呼叫 [**ITaskScheduler：： Activate**](/windows/desktop/api/Mstask/nf-mstask-itaskscheduler-activate) 以取得 task 物件的 [**ITask**](/windows/desktop/api/Mstask/nn-mstask-itask) 介面。  (請注意，此範例會取得 "Test Task" 工作。 ) 
3.  呼叫適當的 [**ITask**](/windows/desktop/api/Mstask/nn-mstask-itask) 方法，以取得您感興趣的屬性。
4.  視需要處理屬性。  (這些範例會將屬性列印到畫面。 ) 
5.  如果傳回的屬性是字串，請呼叫 [CoTaskMemFree](/windows/win32/api/combaseapi/nf-combaseapi-cotaskmemfree) 來釋放針對傳回字串所配置的記憶體。



| 如需的程式碼範例                                                                                                                           | 請參閱                                                                                                                     |
|-------------------------------------------------------------------------------------------------------------------------------------------------|-------------------------------------------------------------------------------------------------------------------------|
| 抓取與指定工作相關聯之應用程式的名稱                                                                             | [C/c + + 程式碼範例：正在抓取工作應用程式名稱](c-c-code-example-retrieving-the-task-application-name.md)   |
| 抓取工作可執行檔最大時間量，並在畫面上顯示該數位                                                 | [C/c + + 程式碼範例：正在抓取工作 MaxRunTime](c-c-code-example-retrieving-the-task-maxruntime.md)               |
| 抓取工作執行時所執行的參數字串，並在畫面上顯示該字串                                  | [C/c + + 程式碼範例：正在抓取工作參數](c-c-code-example-retrieving-task-parameters.md)                       |
| 正在抓取工作的 [*優先權層級*](p.md)                                                                    | [C/c + + 程式碼範例：正在抓取工作優先順序](c-c-code-example-retrieving-task-priority.md)                           |
| 抓取 [*工作的工作目錄*](w.md) ，並顯示幕幕上工作目錄的路徑 | [C/c + + 程式碼範例：取出工作工作目錄](c-c-code-example-retrieving-the-task-working-directory.md) |



 

## <a name="related-topics"></a>相關主題

<dl> <dt>

[工作排程器1.0 範例](task-scheduler-1-0-examples.md)
</dt> </dl>

 

 