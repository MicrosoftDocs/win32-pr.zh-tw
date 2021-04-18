---
description: 系統事件通知服務可讓行動感知的應用程式接收來自 SENS 監視之系統事件的通知。 當要求的事件發生時，SENS 會通知應用程式。
ms.assetid: 19311dec-4611-4104-b6e4-ff8f7c8af0e7
title: '通知 (系統事件通知服務) '
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 272f0ea60369015328e34d3a83231ab0b254253a
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/08/2021
ms.locfileid: "106971548"
---
# <a name="notifications-system-event-notification-service"></a><span data-ttu-id="c1ebc-104">通知 (系統事件通知服務) </span><span class="sxs-lookup"><span data-stu-id="c1ebc-104">Notifications (System Event Notification Service)</span></span>

<span data-ttu-id="c1ebc-105">系統事件通知服務可讓行動感知的應用程式接收來自 SENS 監視之系統事件的通知。</span><span class="sxs-lookup"><span data-stu-id="c1ebc-105">The System Event Notification Service enables mobile-aware applications to receive notifications from system events that SENS monitors.</span></span> <span data-ttu-id="c1ebc-106">當要求的事件發生時，SENS 會通知應用程式。</span><span class="sxs-lookup"><span data-stu-id="c1ebc-106">When the requested event occurs, SENS notifies the application.</span></span>

<span data-ttu-id="c1ebc-107">SENS 可以通知應用程式有三個系統事件類別：</span><span class="sxs-lookup"><span data-stu-id="c1ebc-107">SENS can notify applications about three classes of system events:</span></span>

-   <span data-ttu-id="c1ebc-108">TCP/IP 網路事件，例如 TCP/IP 網路連接的狀態或連接的品質。</span><span class="sxs-lookup"><span data-stu-id="c1ebc-108">TCP/IP network events, such as the status of a TCP/IP network connection or the quality of the connection.</span></span>
-   <span data-ttu-id="c1ebc-109">使用者登入事件。</span><span class="sxs-lookup"><span data-stu-id="c1ebc-109">User logon events.</span></span>
-   <span data-ttu-id="c1ebc-110">電池和 AC 電源事件。</span><span class="sxs-lookup"><span data-stu-id="c1ebc-110">Battery and AC power events.</span></span>

<span data-ttu-id="c1ebc-111">例如，應用程式可以訂閱下列任何系統事件：</span><span class="sxs-lookup"><span data-stu-id="c1ebc-111">For example, an application can subscribe to any of the following system events:</span></span>

-   <span data-ttu-id="c1ebc-112">建立網路連線能力</span><span class="sxs-lookup"><span data-stu-id="c1ebc-112">Establishment of network connectivity</span></span>
-   <span data-ttu-id="c1ebc-113">當指定的連線 (QOC) 參數時，可在指定的連線品質內達到指定的目的地時發出通知</span><span class="sxs-lookup"><span data-stu-id="c1ebc-113">Notification when a specified destination can be reached within specified Quality of Connection (QOC) parameters</span></span>
-   <span data-ttu-id="c1ebc-114">電腦已切換到電池電源</span><span class="sxs-lookup"><span data-stu-id="c1ebc-114">The computer has switched to battery power</span></span>
-   <span data-ttu-id="c1ebc-115">剩餘電池計量的百分比在指定的參數內</span><span class="sxs-lookup"><span data-stu-id="c1ebc-115">The percentage of remaining battery power is within a specified parameter</span></span>
-   <span data-ttu-id="c1ebc-116">發生使用同步處理管理員的已排程事件</span><span class="sxs-lookup"><span data-stu-id="c1ebc-116">Scheduled events using Synchronization Manager occur</span></span>

<span data-ttu-id="c1ebc-117">**Windows Server 2008 R2 和 windows 7：** 訂閱者最多需要3分鐘的時間，才能回應 [**ISensLogon**](/windows/desktop/api/Sensevts/nn-sensevts-isenslogon) 和 [**ISensLogon2**](/windows/desktop/api/Sensevts/nn-sensevts-isenslogon2) 介面上的通知。</span><span class="sxs-lookup"><span data-stu-id="c1ebc-117">**Windows Server 2008 R2 and Windows 7:** The subscriber has a maximum of 3 minutes to respond to a notification on the [**ISensLogon**](/windows/desktop/api/Sensevts/nn-sensevts-isenslogon) and [**ISensLogon2**](/windows/desktop/api/Sensevts/nn-sensevts-isenslogon2) interfaces.</span></span> <span data-ttu-id="c1ebc-118">3分鐘之後，SENS 會取消對訂閱者的呼叫，並解除封鎖通知執行緒。</span><span class="sxs-lookup"><span data-stu-id="c1ebc-118">After 3 minutes, SENS cancels the call to subscribers and unblocks the notification thread.</span></span> <span data-ttu-id="c1ebc-119">如果需要較長的作業來回應通知，請儘快傳回 **ISensLogon** 或 **ISensLogon2** ，然後開啟另一個執行緒進行處理。</span><span class="sxs-lookup"><span data-stu-id="c1ebc-119">If a lengthy operation is required to respond to the notification, return from **ISensLogon** or **ISensLogon2** as quickly as possible and open another thread for processing.</span></span>

 

 



