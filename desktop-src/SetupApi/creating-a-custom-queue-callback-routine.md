---
description: 除了使用預設佇列回呼之外，您還可以撰寫自訂的回呼常式。
ms.assetid: 68781565-71a2-43bf-ad01-7c1cdc514f7b
title: 建立自訂佇列回呼常式
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: a119836e994709ff2d0fa21e12489af947394119
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/08/2021
ms.locfileid: "103850824"
---
# <a name="creating-a-custom-queue-callback-routine"></a><span data-ttu-id="88d19-103">建立自訂佇列回呼常式</span><span class="sxs-lookup"><span data-stu-id="88d19-103">Creating a Custom Queue Callback Routine</span></span>

<span data-ttu-id="88d19-104">除了使用預設佇列回呼之外，您還可以撰寫自訂的回呼常式。</span><span class="sxs-lookup"><span data-stu-id="88d19-104">In addition to using the default queue callback, you can write a custom callback routine.</span></span> <span data-ttu-id="88d19-105">此函數的形式必須與 [*FileCallback*](/windows/win32/api/setupapi/nc-setupapi-psp_file_callback_a)相同。</span><span class="sxs-lookup"><span data-stu-id="88d19-105">This function must have the same form as [*FileCallback*](/windows/win32/api/setupapi/nc-setupapi-psp_file_callback_a).</span></span> <span data-ttu-id="88d19-106">如果您需要回呼常式以預設佇列回呼常式所提供的方式來處理通知，這會很有用。</span><span class="sxs-lookup"><span data-stu-id="88d19-106">This is useful if you need a callback routine to handle a notification in a manner other than that provided by the default queue callback routine.</span></span>

<span data-ttu-id="88d19-107">如果只需要變更預設佇列回呼常式行為的一小部分，您可以建立自訂的回呼常式來篩選通知，只處理需要特殊行為的程式，以及為其他人呼叫 [**SetupDefaultQueueCallback**](/windows/desktop/api/Setupapi/nf-setupapi-setupdefaultqueuecallbacka) 。</span><span class="sxs-lookup"><span data-stu-id="88d19-107">If only a small portion of the default queue callback routine's behavior needs to be changed, you can create a custom callback routine to filter the notifications, handling only those that require special behavior and calling [**SetupDefaultQueueCallback**](/windows/desktop/api/Setupapi/nf-setupapi-setupdefaultqueuecallbacka) for the others.</span></span>

<span data-ttu-id="88d19-108">例如，如果您想要自訂-處理檔案刪除錯誤，您可以建立自訂回呼函式 *MyCallback*。</span><span class="sxs-lookup"><span data-stu-id="88d19-108">For example, if you wanted to custom-handle file delete errors, you could create a custom callback function, *MyCallback*.</span></span> <span data-ttu-id="88d19-109">此函式會攔截並處理 [**SPFILENOTIFY \_ DELETEERROR**](spfilenotify-deleteerror.md) 通知，並針對所有其他通知呼叫預設佇列回呼函數。</span><span class="sxs-lookup"><span data-stu-id="88d19-109">This function would intercept and process [**SPFILENOTIFY\_DELETEERROR**](spfilenotify-deleteerror.md) notifications, and call the default queue callback function for all other notifications.</span></span> <span data-ttu-id="88d19-110">*MyCallback* 會傳回刪除錯誤通知的值。</span><span class="sxs-lookup"><span data-stu-id="88d19-110">*MyCallback* returns a value for the delete error notifications.</span></span> <span data-ttu-id="88d19-111">對於所有其他通知， *MyCallback* 會將預設佇列回呼常式傳回的任何值傳遞給佇列。</span><span class="sxs-lookup"><span data-stu-id="88d19-111">For all other notifications, *MyCallback* passes whatever value the default queue callback routine returned to the queue.</span></span>

<span data-ttu-id="88d19-112">下圖說明此控制流程。</span><span class="sxs-lookup"><span data-stu-id="88d19-112">This flow of control is illustrated in the following diagram.</span></span>

![顯示自訂回呼函數之資料流程的箭號和方塊](images/callback.png)

> [!IMPORTANT]
> <span data-ttu-id="88d19-114">如果自訂回呼函式呼叫預設佇列回呼常式，它必須將 [**SetupInitDefaultQueueCallback**](/windows/desktop/api/Setupapi/nf-setupapi-setupinitdefaultqueuecallback) 或 [**SetupInitDefaultQueueCallbackEx**](/windows/desktop/api/Setupapi/nf-setupapi-setupinitdefaultqueuecallbackex) 傳回的 void 指標傳遞至預設回呼常式。</span><span class="sxs-lookup"><span data-stu-id="88d19-114">If the custom callback function calls the default queue callback routine, it must pass the void pointer returned by [**SetupInitDefaultQueueCallback**](/windows/desktop/api/Setupapi/nf-setupapi-setupinitdefaultqueuecallback) or [**SetupInitDefaultQueueCallbackEx**](/windows/desktop/api/Setupapi/nf-setupapi-setupinitdefaultqueuecallbackex) to the default callback routine.</span></span>

 

 

 
