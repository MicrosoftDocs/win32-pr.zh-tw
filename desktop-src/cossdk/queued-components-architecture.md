---
description: COM + 佇列的元件服務藉由提供環境，讓您可以同步的方式叫用元件 (即時) 或非同步 (排入佇列) ，藉以增強 COM 程式設計模型。
ms.assetid: fd455679-b2b3-487f-8494-9ea296ce2c89
title: 已排入佇列的元件架構
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: a8a2f6e1012bd3c11a27a44214ee28e84d5bd404
ms.sourcegitcommit: bf526e267d3991892733bdd229c66d5365cf244a
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 02/05/2021
ms.locfileid: "104552484"
---
# <a name="queued-components-architecture"></a><span data-ttu-id="38c5b-103">已排入佇列的元件架構</span><span class="sxs-lookup"><span data-stu-id="38c5b-103">Queued Components Architecture</span></span>

<span data-ttu-id="38c5b-104">COM + 佇列的元件服務藉由提供環境，讓您可以同步的方式叫用元件 (即時) 或非同步 (排入佇列) ，藉以增強 COM 程式設計模型。</span><span class="sxs-lookup"><span data-stu-id="38c5b-104">The COM+ queued components service enhances the COM programming model by providing an environment in which a component can be invoked either synchronously (real-time) or asynchronously (queued).</span></span> <span data-ttu-id="38c5b-105">元件不需要知道它是在即時或已排入佇列的內容中採用。</span><span class="sxs-lookup"><span data-stu-id="38c5b-105">A component need not be aware of whether it is employed in a real-time or a queued context.</span></span>

<span data-ttu-id="38c5b-106">訊息應用程式就像程式之間的電子郵件交易。</span><span class="sxs-lookup"><span data-stu-id="38c5b-106">Messaging applications are like email transactions between programs.</span></span> <span data-ttu-id="38c5b-107">要求者將訊息傳送至伺服器;當伺服器收到訊息時，就會處理訊息。</span><span class="sxs-lookup"><span data-stu-id="38c5b-107">The requester sends a message to the server; when the server gets to it, the message is processed.</span></span> <span data-ttu-id="38c5b-108">就像電子郵件一樣，訊息系統必須處理網路詳細資料，並確保訊息從用戶端移至伺服器。</span><span class="sxs-lookup"><span data-stu-id="38c5b-108">Like email, a messaging system must handle the network details and ensure that the message moves from the client to the server.</span></span> <span data-ttu-id="38c5b-109">在佇列的元件架構中，訊息佇列會負責這項工作。</span><span class="sxs-lookup"><span data-stu-id="38c5b-109">In the queued components framework, Message Queuing is responsible for this.</span></span>

<span data-ttu-id="38c5b-110">COM + 佇列元件服務是由下列部分所組成：</span><span class="sxs-lookup"><span data-stu-id="38c5b-110">The COM+ queued components service consists of the following parts:</span></span>

-   <span data-ttu-id="38c5b-111">用戶端或傳送端) 的錄製器 (</span><span class="sxs-lookup"><span data-stu-id="38c5b-111">Recorder (for the client or send side)</span></span>
-   <span data-ttu-id="38c5b-112">伺服器或接收端的接聽程式 () </span><span class="sxs-lookup"><span data-stu-id="38c5b-112">Listener (for the server or receive side)</span></span>
-   <span data-ttu-id="38c5b-113">伺服器或接收端的播放程式 () </span><span class="sxs-lookup"><span data-stu-id="38c5b-113">Player (for the server or receive side)</span></span>

![此圖顯示從用戶端到伺服器的路徑：用戶端、錄製器、佇列、接聽程式、播放程式、伺服器。](images/d732774b-1ca6-45ad-bce0-a95b0bfc3edb.png)

## <a name="the-recorder"></a><span data-ttu-id="38c5b-115">錄製器</span><span class="sxs-lookup"><span data-stu-id="38c5b-115">The Recorder</span></span>

<span data-ttu-id="38c5b-116">在典型的佇列元件案例中，用戶端會呼叫已排入佇列的元件。</span><span class="sxs-lookup"><span data-stu-id="38c5b-116">In a typical queued components scenario, the client calls a queued component.</span></span> <span data-ttu-id="38c5b-117">對已排入佇列的元件錄製器進行呼叫，這會將它封裝成訊息的一部分，並將其放在佇列中。</span><span class="sxs-lookup"><span data-stu-id="38c5b-117">The call is made to the queued components recorder, which packages it as part of a message to the server and puts it in a queue.</span></span> <span data-ttu-id="38c5b-118">錄製器會將用戶端的安全性內容封送處理到訊息中，並記錄用戶端的所有方法呼叫。</span><span class="sxs-lookup"><span data-stu-id="38c5b-118">The recorder marshals the client's security context into the message and records all of the client's method calls.</span></span> <span data-ttu-id="38c5b-119">在其作為伺服器元件之 proxy 的角色中，錄製器會從 COM + 目錄中的 queuable 介面選取介面。</span><span class="sxs-lookup"><span data-stu-id="38c5b-119">In its role as proxy for the server component, the recorder selects interfaces from the queuable interfaces in the COM+ catalog.</span></span>

<span data-ttu-id="38c5b-120">錄製的表示會以訊息的形式傳送至訊息佇列，以傳送至伺服器。</span><span class="sxs-lookup"><span data-stu-id="38c5b-120">A representation of the recording is sent to Message Queuing as a message to be sent to a server.</span></span> <span data-ttu-id="38c5b-121">當已排入佇列的元件具有 [必要] 或 [受支援] 的交易屬性設定時，只有當用戶端交易認可，且 [訊息佇列] 佇列是交易式時（這是正常建立的預設值），訊息佇列才會接受訊息的傳遞。</span><span class="sxs-lookup"><span data-stu-id="38c5b-121">When the queued component has the transaction attribute setting of Required or Supported, Message Queuing accepts delivery of the message only if the client-side transaction commits and the Message Queuing queue is transactional, which is the default normally established.</span></span> <span data-ttu-id="38c5b-122">當 [交易屬性] 設定為 [需要新的] 時，即使用戶端交易中止，訊息佇列仍可以接受訊息。</span><span class="sxs-lookup"><span data-stu-id="38c5b-122">When the transaction attribute setting is Requires New, Message Queuing can accept the message even if the client-side transaction aborts.</span></span> <span data-ttu-id="38c5b-123">如需交易的詳細資訊，請參閱交易式 [訊息佇列](transactional-message-queuing.md)。</span><span class="sxs-lookup"><span data-stu-id="38c5b-123">For more information on transactions, see [Transactional Message Queuing](transactional-message-queuing.md).</span></span>

## <a name="the-listener"></a><span data-ttu-id="38c5b-124">接聽程式</span><span class="sxs-lookup"><span data-stu-id="38c5b-124">The Listener</span></span>

<span data-ttu-id="38c5b-125">已排入佇列的元件接聽程式會從佇列中取出訊息，並將它傳遞給佇列元件播放機。</span><span class="sxs-lookup"><span data-stu-id="38c5b-125">The queued components listener retrieves the message from the queue and passes it to the queued components player.</span></span>

## <a name="the-player"></a><span data-ttu-id="38c5b-126">播放機</span><span class="sxs-lookup"><span data-stu-id="38c5b-126">The Player</span></span>

<span data-ttu-id="38c5b-127">播放程式會在伺服器端拆收用戶端的安全性內容，然後再叫用伺服器元件，並進行相同的方法呼叫。</span><span class="sxs-lookup"><span data-stu-id="38c5b-127">The player unmarshals the client's security context at the server side and then invokes the server component and makes the same method calls.</span></span> <span data-ttu-id="38c5b-128">除非用戶端元件完成，而且記錄方法的交易呼叫認可，否則播放程式不會播放方法呼叫。</span><span class="sxs-lookup"><span data-stu-id="38c5b-128">The method calls are not played back by the player until the client component completes and the transaction that recorded the method calls commits.</span></span>

## <a name="the-message-mover"></a><span data-ttu-id="38c5b-129">訊息移動器</span><span class="sxs-lookup"><span data-stu-id="38c5b-129">The Message Mover</span></span>

<span data-ttu-id="38c5b-130">排入佇列的元件訊息移動器是一種公用程式，可將所有失敗的訊息佇列訊息從一個佇列移至另一個佇列，以便重試。</span><span class="sxs-lookup"><span data-stu-id="38c5b-130">The queued components message mover is a utility that moves all failed Message Queuing messages from one queue to another so that they can be retried.</span></span> <span data-ttu-id="38c5b-131">訊息移動器公用程式是可使用 VBScript 叫用的自動化物件;如需詳細資訊，請參閱 [處理錯誤](handling-errors-in-queued-components.md)。</span><span class="sxs-lookup"><span data-stu-id="38c5b-131">The message mover utility is an Automation object that can be invoked with a VBScript; for more information, see [Handling Errors](handling-errors-in-queued-components.md).</span></span>

 

 



