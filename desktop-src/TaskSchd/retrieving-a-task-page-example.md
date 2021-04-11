---
title: 正在抓取工作頁面範例
description: 若要取出工作頁面，您必須呼叫 ITask QueryInterface 來取出 IProvideTaskPage 介面，然後呼叫 IProvideTaskPage GetPage。 GetPage 方法會傳回頁面的控制碼，然後可用來顯示您所要求的頁面。
ms.assetid: 97525419-c480-465a-97c6-e701043c0af2
keywords:
- 正在抓取工作頁面工作排程器
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: fd570edf3309b9b9ff0eada291d02a10850885ae
ms.sourcegitcommit: 592c9bbd22ba69802dc353bcb5eb30699f9e9403
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/20/2020
ms.locfileid: "104023643"
---
# <a name="retrieving-a-task-page-example"></a>正在抓取工作頁面範例

若要取出工作頁面，您必須呼叫 **ITask：： QueryInterface** 來取出 [**IProvideTaskPage**](/windows/desktop/api/Mstask/nn-mstask-iprovidetaskpage) 介面，然後呼叫 [**IProvideTaskPage：： GetPage**](/windows/desktop/api/Mstask/nf-mstask-iprovidetaskpage-getpage)。 **GetPage** 方法會傳回頁面的控制碼，然後可用來顯示您所要求的頁面。

> [!Note]  
> 在下列程式碼範例中，不再需要所有介面之後，就會釋放它們。

 

下列程式說明如何建立新的觸發程式。

**建立新的觸發程式**

1.  呼叫 [**CoInitialize**](/windows/win32/api/objbase/nf-objbase-coinitialize) 以初始化 COM 程式庫和 [**CoCreateInstance**](/windows/win32/api/combaseapi/nf-combaseapi-cocreateinstance) ，以取得工作排程器物件。  (此範例假設工作排程器服務正在執行。 ) 
2.  呼叫 [**ITaskScheduler：： Activate**](/windows/desktop/api/Mstask/nf-mstask-itaskscheduler-activate) 以取得 task 物件的 [**ITask**](/windows/desktop/api/Mstask/nn-mstask-itask) 介面。  (請注意，此範例會取得 "Test Task" 工作。 ) 
3.  呼叫 **ITask：： QueryInterface** 以抓取 [**IProvideTaskPage**](/windows/desktop/api/Mstask/nn-mstask-iprovidetaskpage) 介面和 [**IProvideTaskPage：： GetPage**](/windows/desktop/api/Mstask/nf-mstask-iprovidetaskpage-getpage) 取得頁面。
4.  使用傳回的頁面控點顯示頁面。



| 如需的程式碼範例                                   | 請參閱                                                                   |
|---------------------------------------------------------|-----------------------------------------------------------------------|
| 取出和顯示已知工作的工作頁面 | [正在抓取工作頁面](c-c-code-example-retrieving-a-task-page.md) |



 

## <a name="related-topics"></a>相關主題

<dl> <dt>

[工作排程器1.0 範例](task-scheduler-1-0-examples.md)
</dt> </dl>

 

 