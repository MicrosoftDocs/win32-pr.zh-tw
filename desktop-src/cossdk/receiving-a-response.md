---
description: 接收回應
ms.assetid: 48919608-a102-43e2-9ca0-80b17344b5eb
title: 接收回應
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 9e9e05ec392b7db828ad1efd1360c4d4fb232210
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/07/2021
ms.locfileid: "104510706"
---
# <a name="receiving-a-response"></a><span data-ttu-id="f5352-103">接收回應</span><span class="sxs-lookup"><span data-stu-id="f5352-103">Receiving a Response</span></span>

<span data-ttu-id="f5352-104">由於已排入佇列的元件是設計來以非同步方式運作，因此用戶端應用程式應該不會在等候佇列要求的回應時封鎖。</span><span class="sxs-lookup"><span data-stu-id="f5352-104">Because queued components are designed to work asynchronously, client applications should not block while waiting for a response from a queued request.</span></span> <span data-ttu-id="f5352-105">不過，這對於用戶端應用程式或用戶端電腦上的相關應用程式來說，最終會很有用。</span><span class="sxs-lookup"><span data-stu-id="f5352-105">Nevertheless, it is often useful for the client application or a related application on the client machine to receive a response eventually.</span></span> <span data-ttu-id="f5352-106">例如，用戶端可能會想要在要求的交易順利完成時收到通知。</span><span class="sxs-lookup"><span data-stu-id="f5352-106">For example, a client may want to be notified when a requested transaction has been completed successfully.</span></span>

<span data-ttu-id="f5352-107">有許多方式可讓佇列元件以非同步方式將回應傳回給呼叫端。</span><span class="sxs-lookup"><span data-stu-id="f5352-107">There are a variety of ways for a queued component to send a response back to its caller asynchronously.</span></span> <span data-ttu-id="f5352-108">例如，它可能會傳送電子郵件。</span><span class="sxs-lookup"><span data-stu-id="f5352-108">For example, it could send an email.</span></span> <span data-ttu-id="f5352-109">或者，伺服器也可以發佈鬆散結合的事件，讓用戶端訂閱。</span><span class="sxs-lookup"><span data-stu-id="f5352-109">Alternatively, the server could publish loosely coupled events to which the client could subscribe.</span></span>

<span data-ttu-id="f5352-110">用戶端從伺服器上執行的佇列元件取得回應的另一種方式，是讓用戶端將呼叫的方法傳遞給通知物件。</span><span class="sxs-lookup"><span data-stu-id="f5352-110">Another way for a client to obtain a response from a queued component that runs on a server is for the client to pass the called method a notification object.</span></span> <span data-ttu-id="f5352-111">通知物件是在用戶端上執行之已排入佇列的元件實例。</span><span class="sxs-lookup"><span data-stu-id="f5352-111">A notification object is an instance of a queued component that runs on the client.</span></span> <span data-ttu-id="f5352-112">這類通知物件可能相當簡單，只包含用來表示錯誤值的整數，或者可能相當複雜，其中包含在用戶端上回複交易所需的所有資訊。</span><span class="sxs-lookup"><span data-stu-id="f5352-112">Such a notification object might be quite simple, containing only an integer that is used to represent an error value, or it might be quite complex, containing all the information necessary to roll back a transaction on the client.</span></span> <span data-ttu-id="f5352-113">無論是哪一種情況，呼叫端用戶端都必須在伺服器上執行佇列元件的回應時，傳遞通知物件做為輸入參數。</span><span class="sxs-lookup"><span data-stu-id="f5352-113">In either case, the calling client passes a notification object as an input parameter whenever it desires a response from a queued component that runs on a server.</span></span> <span data-ttu-id="f5352-114">因為通知物件已排入佇列，所以伺服器可以在其方法上呼叫來改變其狀態，而用戶端之後可以將其讀取。</span><span class="sxs-lookup"><span data-stu-id="f5352-114">Because the notification object is queued, the server can call on its methods to alter its state, which can subsequently be read out by the client.</span></span> <span data-ttu-id="f5352-115">在此案例中，會在用戶端和伺服器上使用 COM + 佇列的元件服務，以允許雙向進行非同步通訊。</span><span class="sxs-lookup"><span data-stu-id="f5352-115">In this scenario, the COM+ queued components service is used on both the client and the server to allow asynchronous communication in both directions.</span></span>

 

 



