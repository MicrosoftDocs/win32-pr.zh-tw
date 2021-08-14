---
title: 工作排程器1.0 的閒置觸發程式
description: 閒置觸發程式是以事件為基礎的觸發程式，會在電腦閒置之後引發特定次數。 有多個條件會定義電腦何時閒置，例如當沒有鍵盤或滑鼠輸入時。
ms.assetid: f2e0b120-dadc-470f-8349-42843149bb60
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 349b6ce078479df841773661bfe07b098f95d1124a68803b8b472b226d9b5df6
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/11/2021
ms.locfileid: "117760084"
---
# <a name="idle-triggers-for-task-scheduler-10"></a>工作排程器1.0 的閒置觸發程式

閒置觸發程式是以事件為基礎的觸發程式，會在電腦閒置之後引發特定次數。 有多個條件會定義電腦何時閒置，例如當沒有鍵盤或滑鼠輸入時。

閒置觸發程式的建立方式，是在工作觸發程式 \_ \_ 結構的 \_ \_ 工作觸發程式 [**\_ \_ 類型**](/windows/desktop/api/Mstask/ne-mstask-task_trigger_type) 成員 [**\_**](/windows/desktop/api/Mstask/ns-mstask-task_trigger) 中指定閒置的工作事件觸發程式。 當系統閒置了工作專案的閒置等候時間所指定的時間量時，就會引發閒置觸發程式。

> [!Note]  
> 當 \_ \_ \_ 指定閒置的工作事件觸發程式時 \_ ，會忽略工作 [**\_ 觸發**](/windows/desktop/api/Mstask/ns-mstask-task_trigger)程式結構的 **wStartHour**、 **wStartMinute** 和 **類型** 成員。

 

您可以藉由呼叫 [**IScheduledWorkItem：： SetIdleWait**](/windows/desktop/api/Mstask/nf-mstask-ischeduledworkitem-setidlewait) 方法來設定工作專案的空閒等候時間。 這個方法會以分鐘為單位來設定時間 (，) 系統必須保持閒置，才能引發觸發程式和執行工作專案。

若要取出工作的閒置時間，請呼叫 [**IScheduledWorkItem：： GetIdleWait**](/windows/desktop/api/Mstask/nf-mstask-ischeduledworkitem-getidlewait) 方法。

## <a name="related-topics"></a>相關主題

<dl> <dt>

[工作觸發程式](task-triggers.md)
</dt> </dl>

 

 




