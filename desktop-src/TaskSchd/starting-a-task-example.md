---
title: 啟動工作範例
description: 若要啟動工作，請呼叫 ITask 介面的 Run 方法。 Run 是一個非同步方法，它會嘗試執行工作，並在工作啟動時立即傳回。 工作排程器服務必須執行，這個方法才能成功。
ms.assetid: 90f197de-7a32-4e4b-b4c0-d3f706e47de1
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: f4176bf793e72acd3930d6e1e5cbc3d73e91c1d558e342a5a9804aa8f87526cf
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/11/2021
ms.locfileid: "119139331"
---
# <a name="starting-a-task-example"></a>啟動工作範例

若要啟動工作，請呼叫 [**ITask**](/windows/desktop/api/Mstask/nn-mstask-itask)介面的 [**Run**](/windows/desktop/api/Mstask/nf-mstask-ischeduledworkitem-run)方法。 **Run** 是一個非同步方法，它會嘗試執行工作，並在工作啟動時立即傳回。 工作排程器服務必須執行，這個方法才能成功。

下列程式說明如何啟動工作。

**若要啟動工作**

1.  呼叫 [**CoInitialize**](/windows/win32/api/objbase/nf-objbase-coinitialize) 以初始化 COM 程式庫和 [**CoCreateInstance**](/windows/win32/api/combaseapi/nf-combaseapi-cocreateinstance) ，以取得工作排程器物件。  (此範例假設工作排程器服務正在執行。 ) 
2.  呼叫 [**ITaskScheduler：： Activate**](/windows/desktop/api/Mstask/nf-mstask-itaskscheduler-activate) 以取得 task 物件的 [**ITask**](/windows/desktop/api/Mstask/nn-mstask-itask) 介面。  (請注意，此範例會取得 "Test Task" 工作。 ) 
3.  呼叫 [**Run**](/windows/desktop/api/Mstask/nf-mstask-ischeduledworkitem-run) 來啟動工作。 請注意，這個方法是由 [**ITask**](/windows/desktop/api/Mstask/nn-mstask-itask) 介面所繼承。
4.  視需要繼續處理。
5.  呼叫 **ITask：： Release** 可釋放資源和 [**CoUninitialize**](/windows/win32/api/combaseapi/nf-combaseapi-couninitialize) ，以將 COM 解除初始化。 此範例會呼叫 [**Release**](/windows/win32/api/unknwn/nf-unknwn-iunknown-release) 以釋放 [**ITask**](/windows/desktop/api/Mstask/nn-mstask-itask) 介面的指標。  (請注意，**版本** 是 **ITask** 所繼承的 [**IUnknown**](/windows/win32/api/unknwn/nn-unknwn-iunknown)方法 ) 



| 如需的程式碼範例    | 請參閱                                                                         |
|--------------------------|-----------------------------------------------------------------------------|
| 執行現有的工作 | [C/c + + 程式碼範例：啟動工作](c-c-code-example-starting-a-task.md) |



 

## <a name="related-topics"></a>相關主題

<dl> <dt>

[工作排程器1.0 範例](task-scheduler-1-0-examples.md)
</dt> </dl>

 

 