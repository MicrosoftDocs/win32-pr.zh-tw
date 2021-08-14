---
description: 除了使用預設佇列回呼之外，您還可以撰寫自訂的回呼常式。
ms.assetid: 68781565-71a2-43bf-ad01-7c1cdc514f7b
title: 建立自訂佇列回呼常式
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: f0602e32ef97ea962ca91375318bb563c0809da0dc4877aa6c9439644b52408e
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/11/2021
ms.locfileid: "118887502"
---
# <a name="creating-a-custom-queue-callback-routine"></a>建立自訂佇列回呼常式

除了使用預設佇列回呼之外，您還可以撰寫自訂的回呼常式。 此函數的形式必須與 [*FileCallback*](/windows/win32/api/setupapi/nc-setupapi-psp_file_callback_a)相同。 如果您需要回呼常式以預設佇列回呼常式所提供的方式來處理通知，這會很有用。

如果只需要變更預設佇列回呼常式行為的一小部分，您可以建立自訂的回呼常式來篩選通知，只處理需要特殊行為的程式，以及為其他人呼叫 [**SetupDefaultQueueCallback**](/windows/desktop/api/Setupapi/nf-setupapi-setupdefaultqueuecallbacka) 。

例如，如果您想要自訂-處理檔案刪除錯誤，您可以建立自訂回呼函式 *MyCallback*。 此函式會攔截並處理 [**SPFILENOTIFY \_ DELETEERROR**](spfilenotify-deleteerror.md) 通知，並針對所有其他通知呼叫預設佇列回呼函數。 *MyCallback* 會傳回刪除錯誤通知的值。 對於所有其他通知， *MyCallback* 會將預設佇列回呼常式傳回的任何值傳遞給佇列。

下圖說明此控制流程。

![顯示自訂回呼函數之資料流程的箭號和方塊](images/callback.png)

> [!IMPORTANT]
> 如果自訂回呼函式呼叫預設佇列回呼常式，它必須將 [**SetupInitDefaultQueueCallback**](/windows/desktop/api/Setupapi/nf-setupapi-setupinitdefaultqueuecallback) 或 [**SetupInitDefaultQueueCallbackEx**](/windows/desktop/api/Setupapi/nf-setupapi-setupinitdefaultqueuecallbackex) 傳回的 void 指標傳遞至預設回呼常式。

 

 

 
