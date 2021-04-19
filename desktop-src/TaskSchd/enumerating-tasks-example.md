---
title: 列舉工作範例
description: 若要列舉工作，您必須呼叫 ITaskScheduler Enum 來建立列舉物件。 然後，使用列舉物件的 IEnumWorkItems 介面來列舉 [排定的工作] 資料夾中的工作。
ms.assetid: 65a8a8af-f4d8-4948-8dd4-b592f1381bfe
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: cd929ebd7d8e9f1a3c372ce212d63dcb29df82b7
ms.sourcegitcommit: 592c9bbd22ba69802dc353bcb5eb30699f9e9403
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/20/2020
ms.locfileid: "106967277"
---
# <a name="enumerating-tasks-example"></a>列舉工作範例

若要列舉工作，您必須呼叫 [**ITaskScheduler：： Enum**](/windows/desktop/api/Mstask/nf-mstask-itaskscheduler-enum) 來建立 [*列舉物件*](e.md)。 然後，使用列舉物件的 [**IEnumWorkItems**](/windows/desktop/api/Mstask/nn-mstask-ienumworkitems) 介面來列舉 [排定的工作] 資料夾中的工作。

下列程式描述如何列舉 [排定的工作] 資料夾中的工作。

**列舉 [排定的工作] 資料夾中的工作**

1.  呼叫 [**CoInitialize**](/windows/win32/api/objbase/nf-objbase-coinitialize) 以初始化 COM 程式庫和 [**CoCreateInstance**](/windows/win32/api/combaseapi/nf-combaseapi-cocreateinstance) ，以取得工作排程器物件。  (此範例假設工作排程器服務正在執行。 ) 
2.  呼叫 [**ITaskScheduler：： Enum**](/windows/desktop/api/Mstask/nf-mstask-itaskscheduler-enum) 來取得列舉物件。
3.  呼叫 [**IEnumWorkItems：： Next**](/windows/desktop/api/Mstask/nf-mstask-ienumworkitems-next) 以取得工作。  (此範例會嘗試在每次呼叫時取出五個工作。 ) 
4.  處理傳回的工作。  (此範例只會將每個工作的名稱列印到螢幕。
5.  釋放資源。 呼叫 [**CoTaskMemFree**](/windows/win32/api/combaseapi/nf-combaseapi-cotaskmemfree) 以釋放用於名稱的記憶體。



| 如需的程式碼範例                                                         | 請參閱                                                                             |
|-------------------------------------------------------------------------------|---------------------------------------------------------------------------------|
| 列舉本機電腦的 [排程工作] 資料夾中的所有工作 | [C/c + + 程式碼範例：列舉工作](c-c-code-example-enumerating-tasks.md) |



 

## <a name="related-topics"></a>相關主題

<dl> <dt>

[工作排程器1.0 範例](task-scheduler-1-0-examples.md)
</dt> </dl>

 

 