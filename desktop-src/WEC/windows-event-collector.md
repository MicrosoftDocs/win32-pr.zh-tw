---
title: Windows 事件收集器
description: 您可以在本機電腦上訂閱接收和儲存事件 (事件收集器) 從遠端電腦轉送 (事件來源) 。
ms.assetid: 7725e06d-4df1-4b3e-9f2f-2b8bdd805cb6
ms.tgt_platform: multiple
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 3c4ef9e0cb647236daa55771222f25b7e0e370ef
ms.sourcegitcommit: 592c9bbd22ba69802dc353bcb5eb30699f9e9403
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/20/2020
ms.locfileid: "106999588"
---
# <a name="windows-event-collector"></a><span data-ttu-id="cfc3c-103">Windows 事件收集器</span><span class="sxs-lookup"><span data-stu-id="cfc3c-103">Windows Event Collector</span></span>

<span data-ttu-id="cfc3c-104">您可以在本機電腦上訂閱接收和儲存事件 (事件收集器) 從遠端電腦轉送 (事件來源) 。</span><span class="sxs-lookup"><span data-stu-id="cfc3c-104">You can subscribe to receive and store events on a local computer (event collector) that are forwarded from a remote computer (event source).</span></span> <span data-ttu-id="cfc3c-105">[Windows 事件收集器函數](windows-event-collector-functions.md)支援使用 WS-Management 通訊協定來訂閱事件。</span><span class="sxs-lookup"><span data-stu-id="cfc3c-105">The [Windows Event Collector functions](windows-event-collector-functions.md) support subscribing to events by using the WS-Management protocol.</span></span> <span data-ttu-id="cfc3c-106">如需 WS-MANAGEMENT 的詳細資訊，請參閱 [關於 Windows 遠端管理](/windows/desktop/WinRM/about-windows-remote-management)。</span><span class="sxs-lookup"><span data-stu-id="cfc3c-106">For more information about WS-Management, see [About Windows Remote Management](/windows/desktop/WinRM/about-windows-remote-management).</span></span>

## <a name="event-forwarding-and-event-collection-architecture"></a><span data-ttu-id="cfc3c-107">事件轉送和事件集合架構</span><span class="sxs-lookup"><span data-stu-id="cfc3c-107">Event Forwarding and Event Collection Architecture</span></span>

<span data-ttu-id="cfc3c-108">事件收集可讓系統管理員從遠端電腦取得事件，並將它們儲存在收集器電腦上的本機事件記錄檔中。</span><span class="sxs-lookup"><span data-stu-id="cfc3c-108">Event collection allows administrators to get events from remote computers and store them in a local event log on the collector computer.</span></span> <span data-ttu-id="cfc3c-109">事件的目的地記錄檔路徑是訂用帳戶的屬性。</span><span class="sxs-lookup"><span data-stu-id="cfc3c-109">The destination log path for the events is a property of the subscription.</span></span> <span data-ttu-id="cfc3c-110">轉寄事件中的所有資料都會儲存在收集器電腦事件記錄檔中， (不會遺失任何資訊) 。</span><span class="sxs-lookup"><span data-stu-id="cfc3c-110">All data in the forwarded event is saved in the collector computer event log (none of the information is lost).</span></span> <span data-ttu-id="cfc3c-111">事件轉送的其他相關資訊也會新增至事件。</span><span class="sxs-lookup"><span data-stu-id="cfc3c-111">Additional information related to the event forwarding is also added to the event.</span></span> <span data-ttu-id="cfc3c-112">如需如何讓電腦接收收集到的事件或轉寄事件的詳細資訊，請參閱 [設定電腦以轉送和收集](/previous-versions/windows/it-pro/windows-server-2008-R2-and-2008/cc748890(v=ws.11))事件。</span><span class="sxs-lookup"><span data-stu-id="cfc3c-112">For more information about how to enable a computer to receive collected events or forward events, see [Configure Computers to Forward and Collect Events](/previous-versions/windows/it-pro/windows-server-2008-R2-and-2008/cc748890(v=ws.11)).</span></span>

## <a name="subscriptions"></a><span data-ttu-id="cfc3c-113">訂用帳戶</span><span class="sxs-lookup"><span data-stu-id="cfc3c-113">Subscriptions</span></span>

<span data-ttu-id="cfc3c-114">下列清單描述事件訂閱的類型：</span><span class="sxs-lookup"><span data-stu-id="cfc3c-114">The following list describes the types of event subscriptions:</span></span>

-   <span data-ttu-id="cfc3c-115">來源起始的訂用帳戶：可讓您在事件收集器電腦上定義事件訂閱，而不需要定義事件來源電腦。</span><span class="sxs-lookup"><span data-stu-id="cfc3c-115">Source-initiated subscriptions: allows you to define an event subscription on an event collector computer without defining the event source computers.</span></span> <span data-ttu-id="cfc3c-116">然後，您可以使用群組原則設定) 將事件轉寄至事件收集器電腦，來設定多個遠端事件來源電腦 (。</span><span class="sxs-lookup"><span data-stu-id="cfc3c-116">Multiple remote event source computers can then be set up (using a group policy setting) to forward events to the event collector computer.</span></span> <span data-ttu-id="cfc3c-117">如需詳細資訊，請參閱 [設定來源起始的訂用](setting-up-a-source-initiated-subscription.md)帳戶。</span><span class="sxs-lookup"><span data-stu-id="cfc3c-117">For more information, see [Setting up a Source Initiated Subscription](setting-up-a-source-initiated-subscription.md).</span></span> <span data-ttu-id="cfc3c-118">當您不知道或不想要指定將轉寄事件的所有事件來源電腦時，此訂閱類型會很有用。</span><span class="sxs-lookup"><span data-stu-id="cfc3c-118">This subscription type is useful when you do not know or you do not want to specify all the event sources computers that will forward events.</span></span>
-   <span data-ttu-id="cfc3c-119">收集器起始的訂閱：如果您知道將轉寄事件的所有事件來源電腦，可讓您建立事件訂閱。</span><span class="sxs-lookup"><span data-stu-id="cfc3c-119">Collector-initiated subscriptions: allows you to create an event subscription if you know all the event source computers that will forward events.</span></span> <span data-ttu-id="cfc3c-120">您可以在建立訂閱時指定所有事件來源。</span><span class="sxs-lookup"><span data-stu-id="cfc3c-120">You specify all the event sources at the time the subscription is created.</span></span> <span data-ttu-id="cfc3c-121">如需詳細資訊，請參閱 [建立收集器起始的訂用](creating-an-event-collector-subscription.md)帳戶。</span><span class="sxs-lookup"><span data-stu-id="cfc3c-121">For more information, see [Creating a Collector Initiated Subscription](creating-an-event-collector-subscription.md).</span></span>

## <a name="windows-event-collector-functions"></a><span data-ttu-id="cfc3c-122">Windows 事件收集器函式</span><span class="sxs-lookup"><span data-stu-id="cfc3c-122">Windows Event Collector Functions</span></span>

<span data-ttu-id="cfc3c-123">如需使用事件收集器函式的詳細資訊和程式碼範例，請參閱 [使用 Windows 事件收集器](using-windows-event-collector.md)。</span><span class="sxs-lookup"><span data-stu-id="cfc3c-123">For more information and code examples that use the Event Collector functions, see [Using Windows Event Collector](using-windows-event-collector.md).</span></span>

<span data-ttu-id="cfc3c-124">如需用來收集和轉送事件之函式的詳細資訊，請參閱 [Windows 事件收集器](windows-event-collector-functions.md)函式。</span><span class="sxs-lookup"><span data-stu-id="cfc3c-124">For more information about the functions used to collect and forward events, see [Windows Event Collector functions](windows-event-collector-functions.md).</span></span>

 

 