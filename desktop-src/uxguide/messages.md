---
title: " (設計基本概念的訊息) "
description: 訊息是使用者在使用您的應用程式時，所需的任何訊息類型或想要查看的訊息。 瞭解如何在您的應用程式中呈現錯誤、警告、確認和通知。
ms.assetid: 700F1F1F-B41D-4C0A-B2EC-91C84E46E526
ms.topic: article
ms.date: 10/20/2020
ms.openlocfilehash: dba3296c9824b2153184c45b6a021ea823b4d151
ms.sourcegitcommit: 3bdf30edb314e0fcd17dc4ddbc70e4ec7d3596e6
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 02/10/2021
ms.locfileid: "106988087"
---
# <a name="messages-design-basics"></a><span data-ttu-id="32e81-104"> (設計基本概念的訊息) </span><span class="sxs-lookup"><span data-stu-id="32e81-104">Messages (Design basics)</span></span>

> [!NOTE]
> <span data-ttu-id="32e81-105">此設計指南是針對 Windows 7 所建立，而且尚未針對較新版本的 Windows 更新。</span><span class="sxs-lookup"><span data-stu-id="32e81-105">This design guide was created for Windows 7 and has not been updated for newer versions of Windows.</span></span> <span data-ttu-id="32e81-106">大部分的指引仍然適用于準則，但展示和範例不會反映我們目前的 [設計指引](/windows/uwp/design/)。</span><span class="sxs-lookup"><span data-stu-id="32e81-106">Much of the guidance still applies in principle, but the presentation and examples do not reflect our [current design guidance](/windows/uwp/design/).</span></span>

<span data-ttu-id="32e81-107">訊息是使用者在使用您的應用程式時，所需的任何訊息類型或想要查看的訊息。</span><span class="sxs-lookup"><span data-stu-id="32e81-107">Messages are any kind of message users need or want to see as they use your app.</span></span> <span data-ttu-id="32e81-108">瞭解如何在您的應用程式中呈現錯誤、警告、確認和通知。</span><span class="sxs-lookup"><span data-stu-id="32e81-108">Learn how to present errors, warning, confirmations, and notifications in your app.</span></span>

## <a name="in-this-section"></a><span data-ttu-id="32e81-109">本節內容</span><span class="sxs-lookup"><span data-stu-id="32e81-109">In this section</span></span>



| <span data-ttu-id="32e81-110">主題</span><span class="sxs-lookup"><span data-stu-id="32e81-110">Topic</span></span>                                        | <span data-ttu-id="32e81-111">描述</span><span class="sxs-lookup"><span data-stu-id="32e81-111">Description</span></span>                                                                                                                                                                                                                                                                                                                                     |
|----------------------------------------------|-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [<span data-ttu-id="32e81-112">錯誤訊息</span><span class="sxs-lookup"><span data-stu-id="32e81-112">Error Messages</span></span>](mess-error.md)<br/>  | <span data-ttu-id="32e81-113">錯誤訊息會警示使用者已發生的問題。</span><span class="sxs-lookup"><span data-stu-id="32e81-113">An error message alerts users of a problem that has already occurred.</span></span> <span data-ttu-id="32e81-114">相反地，警告訊息會警示使用者可能會在未來發生問題的狀況。</span><span class="sxs-lookup"><span data-stu-id="32e81-114">By contrast, a warning message alerts users of a condition that might cause a problem in the future.</span></span> <span data-ttu-id="32e81-115">您可以使用強制回應對話方塊、就地訊息、通知或氣球來顯示錯誤訊息。</span><span class="sxs-lookup"><span data-stu-id="32e81-115">Error messages can be presented using modal dialog boxes, in-place messages, notifications, or balloons.</span></span><br/>                                                  |
| [<span data-ttu-id="32e81-116">警告訊息</span><span class="sxs-lookup"><span data-stu-id="32e81-116">Warning Messages</span></span>](mess-warn.md)<br/> | <span data-ttu-id="32e81-117">警告訊息是強制回應對話方塊、就地訊息、通知或氣球，會警示使用者可能會在未來發生問題的狀況。</span><span class="sxs-lookup"><span data-stu-id="32e81-117">A warning message is a modal dialog box, in-place message, notification, or balloon that alerts the user of a condition that might cause a problem in the future.</span></span><br/>                                                                                                                                                                    |
| [<span data-ttu-id="32e81-118">確認</span><span class="sxs-lookup"><span data-stu-id="32e81-118">Confirmations</span></span>](mess-confirm.md)<br/> | <span data-ttu-id="32e81-119">確認是一個強制回應對話方塊，會詢問使用者是否要繼續執行動作。</span><span class="sxs-lookup"><span data-stu-id="32e81-119">A confirmation is a modal dialog box that asks if the user wants to proceed with an action.</span></span><br/>                                                                                                                                                                                                                                          |
| [<span data-ttu-id="32e81-120">通知</span><span class="sxs-lookup"><span data-stu-id="32e81-120">Notifications</span></span>](mess-notif.md)<br/>   | <span data-ttu-id="32e81-121">通知會通知使用者與目前使用者活動不相關的事件，方法是在通知區域中的圖示上短暫顯示批註。</span><span class="sxs-lookup"><span data-stu-id="32e81-121">A notification informs users of events that are unrelated to the current user activity, by briefly displaying a balloon from an icon in the notification area.</span></span> <span data-ttu-id="32e81-122">通知可能是由使用者動作或重要的系統事件所造成，或可能提供 Microsoft Windows 或應用程式可能有用的資訊。</span><span class="sxs-lookup"><span data-stu-id="32e81-122">The notification could result from a user action or significant system event, or could offer potentially useful information from Microsoft Windows or an application.</span></span><br/> |



 

 

