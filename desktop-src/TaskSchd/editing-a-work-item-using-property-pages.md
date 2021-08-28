---
title: 使用屬性頁編輯工作專案
description: 您可以使用工作排程器服務所提供的圖形使用者介面，來編輯工作專案的屬性。
ms.assetid: 2d7992ce-fa70-41cc-a8e7-74687171537f
keywords:
- 編輯工作專案工作排程器
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 0121a9e3100922ecdd1d529aa81b498d377724959abb5c3380337df82817e338
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/11/2021
ms.locfileid: "120100428"
---
# <a name="editing-a-work-item-using-property-pages"></a>使用屬性頁編輯工作專案

您可以使用工作排程器服務所提供的圖形使用者介面，來編輯工作專案的屬性。  (目前唯一有效的工作專案是 tasks。 ) 

下列程式描述如何使用其屬性頁來編輯工作。

**若要使用其屬性頁編輯工作**

1.  呼叫 [**CoInitialize**](/windows/win32/api/objbase/nf-objbase-coinitialize) 以初始化 COM 程式庫和 [**CoCreateInstance**](/windows/win32/api/combaseapi/nf-combaseapi-cocreateinstance) ，以取得工作排程器物件。  (這些範例假設工作排程器服務正在執行。 ) 
2.  呼叫 [**ITaskScheduler：： Activate**](/windows/desktop/api/Mstask/nf-mstask-itaskscheduler-activate) 以取得 task 物件的 [**ITask**](/windows/desktop/api/Mstask/nn-mstask-itask) 介面。  (請注意，工作是目前唯一有效的工作專案類型。 ) 
3.  呼叫 [**IScheduledWorkItem：： EditWorkItem**](/windows/desktop/api/Mstask/nf-mstask-ischeduledworkitem-editworkitem) 來顯示工作的屬性頁。
4.  視需要編輯工作的屬性，然後按一下 [確定] 以接受新的值，並移除顯示的屬性頁。



| 如需的程式碼範例                                                                                      | 請參閱                                                                                 |
|------------------------------------------------------------------------------------------------------------|-------------------------------------------------------------------------------------|
| 顯示已知工作的屬性頁，並允許使用者編輯工作專案的屬性 | [C/c + + 程式碼範例：編輯工作專案](c-c-code-example-editing-a-work-item.md) |



 

## <a name="related-topics"></a>相關主題

<dl> <dt>

[工作排程器1.0 範例](task-scheduler-1-0-examples.md)
</dt> </dl>

 

 