---
description: Winlogon 通知套件是一個 DLL，可匯出處理 Winlogon 事件的函式。 例如，當使用者登入系統時，Winlogon 會呼叫每個通知套件的登入事件處理常式函式，以提供事件的相關資訊。
ms.assetid: a2a26bac-93b6-4d94-94fc-42c9821935a0
title: 建立 Winlogon 通知套件
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 0127674967ee3155d42e143a1b142d8c83137c56
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/07/2021
ms.locfileid: "106986929"
---
# <a name="creating-a-winlogon-notification-package"></a><span data-ttu-id="298c0-104">建立 Winlogon 通知套件</span><span class="sxs-lookup"><span data-stu-id="298c0-104">Creating a Winlogon Notification Package</span></span>

<span data-ttu-id="298c0-105">[*Winlogon*](/windows/desktop/SecGloss/w-gly)通知套件是一個 DLL，可匯出處理 Winlogon 事件的函式。</span><span class="sxs-lookup"><span data-stu-id="298c0-105">A [*Winlogon*](/windows/desktop/SecGloss/w-gly) notification package is a DLL that exports functions that handle Winlogon events.</span></span> <span data-ttu-id="298c0-106">例如，當使用者登入系統時，Winlogon 會呼叫每個通知套件的登入事件處理常式函式，以提供事件的相關資訊。</span><span class="sxs-lookup"><span data-stu-id="298c0-106">For example, when a user logs onto the system, Winlogon calls each notification package's logon event handler function to provide information about the event.</span></span>

<span data-ttu-id="298c0-107">在通知套件中執行的事件處理常式函式的名稱會保留給開發人員;Winlogon 會檢查登錄來取得事件處理常式函式的名稱。</span><span class="sxs-lookup"><span data-stu-id="298c0-107">The names of the event handler functions implemented in a notification package are left up to the developer; Winlogon checks the registry to obtain the names of the event handler functions.</span></span> <span data-ttu-id="298c0-108">例如，一個通知套件可能會執行 logon 事件處理常式函式， `WLEventLogon` 而另一個則可能使用 `HandleLogonEvent` 。</span><span class="sxs-lookup"><span data-stu-id="298c0-108">For example, one notification package might implement the logon event handler function as `WLEventLogon` whereas another might use `HandleLogonEvent`.</span></span>

<span data-ttu-id="298c0-109">您不需要針對每個 Winlogon 事件（僅適用于您的應用程式有用的事件）來執行和註冊事件處理常式。</span><span class="sxs-lookup"><span data-stu-id="298c0-109">You do not have to implement and register event handlers for every Winlogon event, only for events that are useful to your application.</span></span> <span data-ttu-id="298c0-110">每個事件處理常式函數都必須使用 [事件處理常式](event-handler-function-prototype.md)函式原型中所述的函式原型。</span><span class="sxs-lookup"><span data-stu-id="298c0-110">Each event handler function must use the function prototype described in [Event Handler Function Prototype](event-handler-function-prototype.md).</span></span> <span data-ttu-id="298c0-111">此原型具有單一參數： [**WLX \_ 通知 \_ 資訊**](/windows/desktop/api/Winwlx/ns-winwlx-wlx_notification_info) 結構，其中包含事件的詳細資料。</span><span class="sxs-lookup"><span data-stu-id="298c0-111">This prototype has a single parameter: a [**WLX\_NOTIFICATION\_INFO**](/windows/desktop/api/Winwlx/ns-winwlx-wlx_notification_info) structure that contains details about the event.</span></span>

<span data-ttu-id="298c0-112">Winlogon 會忽略事件處理常式函數的輸出。</span><span class="sxs-lookup"><span data-stu-id="298c0-112">Winlogon ignores the output of event handler functions.</span></span> <span data-ttu-id="298c0-113">如果處理事件需要與 Winlogon 互動，請使用 [Winlogon 支援功能](authentication-functions.md)。</span><span class="sxs-lookup"><span data-stu-id="298c0-113">If handling an event requires interacting with Winlogon, use the [Winlogon Support Functions](authentication-functions.md).</span></span>

<span data-ttu-id="298c0-114">若要使用 Winlogon 通知套件，必須將 DLL 複製到% SystemRoot% \\ system32 資料夾，並且必須針對通知套件進行登錄更新。</span><span class="sxs-lookup"><span data-stu-id="298c0-114">To use your Winlogon notification package, the DLL must be copied to the %SystemRoot%\\system32 folder, and a registry update must be made for the notification package.</span></span> <span data-ttu-id="298c0-115">如需登錄更新的詳細資訊，請參閱 [註冊 Winlogon 通知套件](registering-a-winlogon-notification-package.md)。</span><span class="sxs-lookup"><span data-stu-id="298c0-115">For information about the registry update, see [Registering a Winlogon Notification Package](registering-a-winlogon-notification-package.md).</span></span>

 

 
