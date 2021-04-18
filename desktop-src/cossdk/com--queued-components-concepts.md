---
description: COM + 佇列元件概念
ms.assetid: ff11e251-311f-4612-8f0d-a4cbc5b4d872
title: COM + 佇列元件概念
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 729d1a8983e84d817e402454392ce95fc2b07a35
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/07/2021
ms.locfileid: "106971309"
---
# <a name="com-queued-components-concepts"></a><span data-ttu-id="e9c97-103">COM + 佇列元件概念</span><span class="sxs-lookup"><span data-stu-id="e9c97-103">COM+ Queued Components Concepts</span></span>

<span data-ttu-id="e9c97-104">根據 [訊息佇列](/previous-versions/windows/desktop/legacy/ms711472(v=vs.85)) 服務，com + 佇列元件服務提供簡單的方法，以非同步方式叫用和執行元件。</span><span class="sxs-lookup"><span data-stu-id="e9c97-104">Based on [Message Queuing](/previous-versions/windows/desktop/legacy/ms711472(v=vs.85)) services, the COM+ queued components service provides an easy way to invoke and execute components asynchronously.</span></span> <span data-ttu-id="e9c97-105">無論寄件者或接收者的可用性或存取性，都可以進行處理。</span><span class="sxs-lookup"><span data-stu-id="e9c97-105">Processing can occur without regard to the availability or accessibility of either the sender or the receiver.</span></span>

<span data-ttu-id="e9c97-106">在 COM 方面， *佇列* 是儲存訊息以供稍後抓取的儲存區。</span><span class="sxs-lookup"><span data-stu-id="e9c97-106">In COM terms, a *queue* is a storage area that saves messages for later retrieval.</span></span> <span data-ttu-id="e9c97-107">佇列提供無連接通訊的機制。</span><span class="sxs-lookup"><span data-stu-id="e9c97-107">Queuing provides a mechanism for connectionless communication.</span></span> <span data-ttu-id="e9c97-108">也就是說，寄件者和接收者不會直接連線，而且只會透過佇列進行通訊。</span><span class="sxs-lookup"><span data-stu-id="e9c97-108">That is, the sender and receiver are not connected directly and communicate only through queues.</span></span> <span data-ttu-id="e9c97-109">佇列提供一種方式來保存資訊，直到接收者準備好取得該資訊為止。</span><span class="sxs-lookup"><span data-stu-id="e9c97-109">Queuing provides a way to hold the information until the receiver is ready to obtain it.</span></span> <span data-ttu-id="e9c97-110">傳送者和接收者會間接進行通訊，以便彼此獨立運作，而不會受到另一個影響。</span><span class="sxs-lookup"><span data-stu-id="e9c97-110">The sender and receiver are indirectly communicating so that each can operate independently, unaffected by the other.</span></span>

<span data-ttu-id="e9c97-111">在過去，必須深入瞭解封送處理，才能佇列、傳送和接收非同步訊息。</span><span class="sxs-lookup"><span data-stu-id="e9c97-111">In the past, an in-depth knowledge of marshaling was necessary to queue, send, and receive asynchronous messages.</span></span> <span data-ttu-id="e9c97-112">現在，使用元件開發人員容易理解及使用的方法呼叫，COM + 佇列的元件服務會自動以訊息佇列訊息的形式來封送處理資料。</span><span class="sxs-lookup"><span data-stu-id="e9c97-112">Now, using method calls that are easily understood and used by component developers, the COM+ queued components service automatically marshals data in the form of a Message Queuing message.</span></span> <span data-ttu-id="e9c97-113">而且因為佇列的元件服務提供內建的交易支援，所以不一致的狀態在伺服器發生錯誤時不會危害資料。</span><span class="sxs-lookup"><span data-stu-id="e9c97-113">And because the queued components service offers built-in support for transactions, an inconsistent state cannot compromise data if a server failure occurs.</span></span>

<span data-ttu-id="e9c97-114">本章節中的下列主題包含有關設計和寫入已排入佇列之元件的背景資訊。</span><span class="sxs-lookup"><span data-stu-id="e9c97-114">The following topics in this section contain background information about designing and writing queued components.</span></span>



| <span data-ttu-id="e9c97-115">主題</span><span class="sxs-lookup"><span data-stu-id="e9c97-115">Topic</span></span>                                                                           | <span data-ttu-id="e9c97-116">描述</span><span class="sxs-lookup"><span data-stu-id="e9c97-116">Description</span></span>                                                                                                           |
|---------------------------------------------------------------------------------|-----------------------------------------------------------------------------------------------------------------------|
| [<span data-ttu-id="e9c97-117">佇列處理的優點</span><span class="sxs-lookup"><span data-stu-id="e9c97-117">Benefits of Queued Processing</span></span>](benefits-of-queued-processing.md)<br/>   | <span data-ttu-id="e9c97-118">說明使用 COM + 佇列元件進行程式設計的優點。</span><span class="sxs-lookup"><span data-stu-id="e9c97-118">Describes the benefits of programming with COM+ queued components.</span></span><br/>                                         |
| [<span data-ttu-id="e9c97-119">已排入佇列的元件架構</span><span class="sxs-lookup"><span data-stu-id="e9c97-119">Queued Components Architecture</span></span>](queued-components-architecture.md)<br/> | <span data-ttu-id="e9c97-120">描述 COM + 佇列元件服務的架構。</span><span class="sxs-lookup"><span data-stu-id="e9c97-120">Describes the architecture of the COM+ queued components service.</span></span><br/>                                          |
| [<span data-ttu-id="e9c97-121">交易式訊息佇列</span><span class="sxs-lookup"><span data-stu-id="e9c97-121">Transactional Message Queuing</span></span>](transactional-message-queuing.md)<br/>   | <span data-ttu-id="e9c97-122">描述 COM + 佇列元件服務如何處理交易。</span><span class="sxs-lookup"><span data-stu-id="e9c97-122">Describes how transactions are handled by the COM+ queued components service.</span></span><br/>                              |
| [<span data-ttu-id="e9c97-123">已排入佇列的元件安全性</span><span class="sxs-lookup"><span data-stu-id="e9c97-123">Queued Components Security</span></span>](queued-components-security.md)<br/>         | <span data-ttu-id="e9c97-124">描述用戶端訊息和其含意的驗證原則選項。</span><span class="sxs-lookup"><span data-stu-id="e9c97-124">Describes the policy options for authentication of client messages and their implications.</span></span><br/>                 |
| [<span data-ttu-id="e9c97-125">開發已排入佇列的元件</span><span class="sxs-lookup"><span data-stu-id="e9c97-125">Developing Queued Components</span></span>](developing-queued-components.md)<br/>     | <span data-ttu-id="e9c97-126">描述撰寫 queuable 元件時的程式設計考慮。</span><span class="sxs-lookup"><span data-stu-id="e9c97-126">Describes programming considerations when writing queuable components.</span></span><br/>                                     |
| [<span data-ttu-id="e9c97-127">佇列元件錯誤</span><span class="sxs-lookup"><span data-stu-id="e9c97-127">Queued Components Errors</span></span>](queued-components-errors.md)<br/>             | <span data-ttu-id="e9c97-128">描述當您使用 COM + 佇列元件服務時，可能會遇到的最常見錯誤類型。</span><span class="sxs-lookup"><span data-stu-id="e9c97-128">Describes the most common types of errors you may encounter when using the COM+ queued components service.</span></span><br/> |



 

## <a name="related-topics"></a><span data-ttu-id="e9c97-129">相關主題</span><span class="sxs-lookup"><span data-stu-id="e9c97-129">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="e9c97-130">COM + 佇列的元件工作</span><span class="sxs-lookup"><span data-stu-id="e9c97-130">COM+ Queued Components Tasks</span></span>](com--queued-components-tasks.md)
</dt> </dl>

 

 




