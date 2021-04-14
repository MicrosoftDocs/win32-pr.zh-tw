---
title: 通知的運作方式
description: 通知的運作方式
ms.assetid: faf66654-8233-49ac-a0fa-6cae51df0bea
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 9665b327d164a4e105f8adba3328be284fbe1fa0
ms.sourcegitcommit: 5f33645661bf8c825a7a2e73950b1f4ea0f1cd82
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/21/2020
ms.locfileid: "104382990"
---
# <a name="how-notifications-work"></a><span data-ttu-id="bfb7f-103">通知的運作方式</span><span class="sxs-lookup"><span data-stu-id="bfb7f-103">How Notifications Work</span></span>

<span data-ttu-id="bfb7f-104">通知是源自物件應用程式，並透過物件處理常式流向容器。</span><span class="sxs-lookup"><span data-stu-id="bfb7f-104">Notifications originate in the object application and flow to the container by way of the object handler.</span></span> <span data-ttu-id="bfb7f-105">如果物件是連結化物件，則連結化物件會從物件處理常式攔截通知，並直接通知容器。</span><span class="sxs-lookup"><span data-stu-id="bfb7f-105">If the object is a linked object, the linked object intercepts the notifications from the object handler and notifies the container directly.</span></span>

<span data-ttu-id="bfb7f-106">物件應用程式必須管理註冊要求，並追蹤傳送通知的位置，並在適當時傳送這些通知。</span><span class="sxs-lookup"><span data-stu-id="bfb7f-106">An object application must manage registration requests, keeping track of where to send which notifications and sending those notifications when appropriate.</span></span> <span data-ttu-id="bfb7f-107">OLE 提供兩個元件物件來簡化這項工作：複合檔案通知的 OleAdviseHolder 和資料通知的 DataAdviseHolder。</span><span class="sxs-lookup"><span data-stu-id="bfb7f-107">OLE provides two component objects to simplify this task: the OleAdviseHolder for compound document notifications and the DataAdviseHolder for data notifications.</span></span>

<span data-ttu-id="bfb7f-108">物件應用程式會決定提示傳送每個特定通知的條件，以及每個通知的傳送頻率。</span><span class="sxs-lookup"><span data-stu-id="bfb7f-108">Object applications determine the conditions that prompt the sending of each specific notification and the frequency with which each notification should be sent.</span></span> <span data-ttu-id="bfb7f-109">當它適用于傳送多個通知時，會先傳送哪個通知，不重要。可以依任何順序傳送。</span><span class="sxs-lookup"><span data-stu-id="bfb7f-109">When it is appropriate for multiple notifications to be sent, it does not matter which notification is sent first; they can be sent in any order.</span></span>

<span data-ttu-id="bfb7f-110">通知的時間會影響物件應用程式及其容器之間的效能和協調。</span><span class="sxs-lookup"><span data-stu-id="bfb7f-110">The timing of notifications affects the performance and coordination between an object application and its containers.</span></span> <span data-ttu-id="bfb7f-111">雖然通知傳送太頻繁，但傳送的通知太過頻繁，導致同步處理中的容器無法執行。</span><span class="sxs-lookup"><span data-stu-id="bfb7f-111">Whereas notifications sent too frequently slow processing, notifications sent too infrequently result in an out-of-sync container.</span></span> <span data-ttu-id="bfb7f-112">通知頻率可以與應用程式重新繪製的速率進行比較。</span><span class="sxs-lookup"><span data-stu-id="bfb7f-112">Notification frequency can be compared with the rate at which an application repaints.</span></span> <span data-ttu-id="bfb7f-113">因此，使用類似的邏輯來執行通知的時機 (如同用於重新繪製) 是明智的做法。</span><span class="sxs-lookup"><span data-stu-id="bfb7f-113">Therefore, using similar logic for the timing of notifications (as is used for repainting) is wise.</span></span>

## <a name="related-topics"></a><span data-ttu-id="bfb7f-114">相關主題</span><span class="sxs-lookup"><span data-stu-id="bfb7f-114">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="bfb7f-115">**CreateDataAdviseHolder**</span><span class="sxs-lookup"><span data-stu-id="bfb7f-115">**CreateDataAdviseHolder**</span></span>](/windows/win32/api/ole2/nf-ole2-createdataadviseholder)
</dt> <dt>

[<span data-ttu-id="bfb7f-116">**CreateOleAdviseHolder**</span><span class="sxs-lookup"><span data-stu-id="bfb7f-116">**CreateOleAdviseHolder**</span></span>](/windows/desktop/api/Ole2/nf-ole2-createoleadviseholder)
</dt> <dt>

[<span data-ttu-id="bfb7f-117">通知</span><span class="sxs-lookup"><span data-stu-id="bfb7f-117">Notifications</span></span>](notifications.md)
</dt> </dl>

 

 