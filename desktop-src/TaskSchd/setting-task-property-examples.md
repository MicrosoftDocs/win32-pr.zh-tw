---
title: 設定工作屬性範例
description: 若要設定工作的屬性，請呼叫 ITaskScheduler Activate 來取出工作物件的介面，然後呼叫適當的 ITask 方法來設定您感興趣的工作屬性。
ms.assetid: df438bff-1ce1-4336-93ee-1e6cab1f1ddd
keywords:
- 設定工作屬性工作排程器
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 2fcb05031961e38314cbc7cd12c20c1d863f54af
ms.sourcegitcommit: 592c9bbd22ba69802dc353bcb5eb30699f9e9403
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/20/2020
ms.locfileid: "106966259"
---
# <a name="setting-task-property-examples"></a>設定工作屬性範例

若要設定工作的屬性，請呼叫 [**ITaskScheduler：： Activate**](/windows/desktop/api/Mstask/nf-mstask-itaskscheduler-activate) 以取出工作物件的介面，然後呼叫適當的 [**ITask**](/windows/desktop/api/Mstask/nn-mstask-itask) 方法來設定您感興趣的工作屬性。

頁面底部所列的程式碼範例會顯示如何設定工作物件的唯一屬性。 針對也適用于工作的其他 [*工作專案*](w.md) 屬性，請參閱 [設定工作專案屬性範例](setting-work-item-property-examples.md)。

> [!Note]  
> 在下列程式碼範例中，不再需要所有介面之後，就會釋放它們。

 

在下列範例中，修改後的工作物件一律會藉由呼叫 [**IPersistFile：： Save**](/windows/win32/api/objidl/nf-objidl-ipersistfile-save)儲存至磁片。  ([**IPersistFile**](/windows/win32/api/objidl/nn-objidl-ipersistfile) 介面是 task 物件所繼承的標準 COM 介面。 ) 

下列程式描述如何設定 task 屬性。

**若要設定 task 屬性**

1.  呼叫 [**CoInitialize**](/windows/win32/api/objbase/nf-objbase-coinitialize) 以初始化 COM 程式庫和 [**CoCreateInstance**](/windows/win32/api/combaseapi/nf-combaseapi-cocreateinstance) ，以取得工作排程器物件。  (這些範例假設工作排程器服務正在執行。 ) 
2.  呼叫 [**ITaskScheduler：： Activate**](/windows/desktop/api/Mstask/nf-mstask-itaskscheduler-activate) 以取得 task 物件的 [**ITask**](/windows/desktop/api/Mstask/nn-mstask-itask) 介面。  (請注意，此範例會取得 "Test Task" 工作。 ) 
3.  呼叫適當的 [**ITask**](/windows/desktop/api/Mstask/nn-mstask-itask) 方法，以設定您感興趣的屬性。
4.  呼叫 [**IPersistFile：： Save**](/windows/win32/api/objidl/nf-objidl-ipersistfile-save) 可將修改過的工作物件儲存至磁片。



| 如需的程式碼範例                                                                                                                                | 請參閱                                                                                             |
|------------------------------------------------------------------------------------------------------------------------------------------------------|-------------------------------------------------------------------------------------------------|
| 設定與已知工作相關聯的應用程式名稱                                                                                     | [C/c + + 程式碼範例：設定應用程式名稱](c-c-code-example-setting-application-name.md)   |
| 設定已知工作的執行時間上限                                                                                                         | [C/c + + 程式碼範例：設定 MaxRunTime](c-c-code-example-setting-maxruntime.md)               |
| 清除與已知工作相關聯的所有命令列參數                                                                                    | [C/c + + 程式碼範例：設定工作參數](c-c-code-example-setting-task-parameters.md)     |
| 此範例會設定測試工作的優先順序，然後儲存工作。 此範例假設本機電腦上已有測試工作。 | [C/c + + 程式碼範例：設定工作優先順序](c-c-code-example-setting-task-priority.md)         |
| 設定已知 [*工作的工作目錄*](w.md)                                                                  | [C/c + + 程式碼範例：設定工作目錄](c-c-code-example-setting-working-directory.md) |



 

## <a name="related-topics"></a>相關主題

<dl> <dt>

[工作排程器1.0 範例](task-scheduler-1-0-examples.md)
</dt> </dl>

 

 