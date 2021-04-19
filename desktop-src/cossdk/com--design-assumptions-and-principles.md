---
description: Microsoft 分散式程式設計模型包含數種技術，包括 MSMQ、IIS、DCOM 和 COM +。 所有這些服務都是針對分散式應用程式所設計。
ms.assetid: c72bbd47-0219-40ba-a7d5-2a6b725972d0
title: COM + 設計假設和原則
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: d7dea86c404896a3d6095d39ebd6031767f6ccdd
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/07/2021
ms.locfileid: "106973187"
---
# <a name="com-design-assumptions-and-principles"></a><span data-ttu-id="60baa-104">COM + 設計假設和原則</span><span class="sxs-lookup"><span data-stu-id="60baa-104">COM+ Design Assumptions and Principles</span></span>

<span data-ttu-id="60baa-105">Microsoft 分散式程式設計模型包含數種技術，包括 MSMQ、IIS、DCOM 和 COM +。</span><span class="sxs-lookup"><span data-stu-id="60baa-105">The Microsoft distributed programming model consists of several technologies, including MSMQ, IIS, DCOM, and COM+.</span></span> <span data-ttu-id="60baa-106">所有這些服務都是針對分散式應用程式所設計。</span><span class="sxs-lookup"><span data-stu-id="60baa-106">All of these services were designed for use by distributed applications.</span></span>

<span data-ttu-id="60baa-107">COM + 的開發目的是要讓您更輕鬆地建立分散式應用程式。</span><span class="sxs-lookup"><span data-stu-id="60baa-107">COM+ was developed to make creating distributed applications easier.</span></span> <span data-ttu-id="60baa-108">整體架構是以一組假設和原則為基礎。</span><span class="sxs-lookup"><span data-stu-id="60baa-108">The overall architecture is based on a set of assumptions and principles.</span></span>

## <a name="assumptions"></a><span data-ttu-id="60baa-109">假設</span><span class="sxs-lookup"><span data-stu-id="60baa-109">Assumptions</span></span>

<span data-ttu-id="60baa-110">這些假設如下：</span><span class="sxs-lookup"><span data-stu-id="60baa-110">The assumptions are as follows:</span></span>

-   <span data-ttu-id="60baa-111">**COM + 應用程式會跨多個伺服器支援多個使用者。**</span><span class="sxs-lookup"><span data-stu-id="60baa-111">**The COM+ application will support multiple users across multiple servers.**</span></span> <span data-ttu-id="60baa-112">換句話說，您要建立分散式應用程式，而這些使用者會在程式碼執行所在的不同主機電腦上。</span><span class="sxs-lookup"><span data-stu-id="60baa-112">In other words, you are building a distributed application, and these multiple users are going to be on different host computers from where the code runs.</span></span> <span data-ttu-id="60baa-113">使用者會透過網際網路或私人網路來存取程式碼。</span><span class="sxs-lookup"><span data-stu-id="60baa-113">Users are going to access the code via the Internet or via a private network.</span></span> <span data-ttu-id="60baa-114">使用者介面會透過瀏覽器或自訂應用程式呈現，例如以 Microsoft Visual Basic 或 MFC 撰寫的表單架構應用程式。</span><span class="sxs-lookup"><span data-stu-id="60baa-114">The user interface is going to be presented via browser or perhaps a custom application, such as a form-based application written with Microsoft Visual Basic or MFC.</span></span> <span data-ttu-id="60baa-115">該使用者介面即將位於用戶端電腦上。</span><span class="sxs-lookup"><span data-stu-id="60baa-115">That user interface is going to be located on the client computer.</span></span>
-   <span data-ttu-id="60baa-116">**您可以透過將應用程式部署到多部伺服器電腦，將 COM + 應用程式設為可調整，並提供更高的可用性和可靠性。**</span><span class="sxs-lookup"><span data-stu-id="60baa-116">**The COM+ application can be made scalable and can provide greater availability and reliability by deploying the application across multiple server computers.**</span></span> <span data-ttu-id="60baa-117">如此一來，您就可以平衡應用程式的工作負載，並使用 Windows 叢集來提供容錯能力。</span><span class="sxs-lookup"><span data-stu-id="60baa-117">By doing this, you can balance the workload of the application and provide fault tolerance by using Windows Clustering.</span></span>
-   <span data-ttu-id="60baa-118">**如果發生錯誤，當您使用交易時，將會維護從 COM + 應用程式儲存在資料庫中之保存資料的狀態。**</span><span class="sxs-lookup"><span data-stu-id="60baa-118">**If things go wrong, the state of the persisted data, stored in a database, from a COM+ application will be maintained if you are using transactions.**</span></span> <span data-ttu-id="60baa-119">應用程式狀態必須存活可能發生的事故，例如應用程式錯誤、系統損毀或網路失敗。</span><span class="sxs-lookup"><span data-stu-id="60baa-119">The application state must survive accidents that can occur, such as application errors, system crashes, or network failures.</span></span>

## <a name="principles"></a><span data-ttu-id="60baa-120">原則</span><span class="sxs-lookup"><span data-stu-id="60baa-120">Principles</span></span>

<span data-ttu-id="60baa-121">除了這三個假設之外，下列準則還涵蓋 COM + 程式設計模型：</span><span class="sxs-lookup"><span data-stu-id="60baa-121">In addition to these three assumptions, the following principles pervade the COM+ programming model:</span></span>

-   <span data-ttu-id="60baa-122">**應用程式邏輯將位於伺服器電腦上，而不是在用戶端電腦上。**</span><span class="sxs-lookup"><span data-stu-id="60baa-122">**The application logic will reside on server computers, not on client computers.**</span></span> <span data-ttu-id="60baa-123">有三個主要原因要執行這項操作：</span><span class="sxs-lookup"><span data-stu-id="60baa-123">There are three major reasons to do this:</span></span>
    -   <span data-ttu-id="60baa-124">用戶端電腦可能沒有執行應用程式邏輯所需的處理能力或功能。</span><span class="sxs-lookup"><span data-stu-id="60baa-124">The client computer may not have the processing power or features needed to run the application logic.</span></span> <span data-ttu-id="60baa-125">此外，保留伺服器上的應用程式邏輯可簡化部署。</span><span class="sxs-lookup"><span data-stu-id="60baa-125">In addition, keeping the application logic on the server simplifies deployment.</span></span>
    -   <span data-ttu-id="60baa-126">伺服器電腦通常較接近資料，而這項資料最常用於資料庫。</span><span class="sxs-lookup"><span data-stu-id="60baa-126">The server computers are often closer to the data, and this data is most often in a database.</span></span> <span data-ttu-id="60baa-127">因為您的應用程式正在存取資料庫，所以您想要對資料庫連接的成本非常敏感。</span><span class="sxs-lookup"><span data-stu-id="60baa-127">Because your application is accessing databases, you want to be very sensitive to the cost of database connections.</span></span> <span data-ttu-id="60baa-128">藉由將大部分的邏輯放在伺服器電腦上，您就可以共用資料庫連接並大幅改善效能。</span><span class="sxs-lookup"><span data-stu-id="60baa-128">By putting most of the logic on the server computers, you can share database connections and get a significant performance improvement.</span></span> <span data-ttu-id="60baa-129">也可以共用伺服器電腦上的其他資源，也有效能上的好處。</span><span class="sxs-lookup"><span data-stu-id="60baa-129">There are other resources on the server computers that can be shared as well, again with a performance benefit.</span></span>
    -   <span data-ttu-id="60baa-130">讓應用程式邏輯位於伺服器電腦上，可讓您控制應用程式的安全性內容。</span><span class="sxs-lookup"><span data-stu-id="60baa-130">Having application logic reside on server computers keeps control of the security context with the application.</span></span> <span data-ttu-id="60baa-131">如果您在伺服器電腦上所執行的應用程式元件（而不是在用戶端電腦上）維護該安全性，您可以更充分掌控安全性。</span><span class="sxs-lookup"><span data-stu-id="60baa-131">You have more control over security if you maintain that security on application components running on server computers rather than on client computers.</span></span>
-   <span data-ttu-id="60baa-132">**交易是核心。**</span><span class="sxs-lookup"><span data-stu-id="60baa-132">**Transactions are the core.**</span></span> <span data-ttu-id="60baa-133">根據設計，交易會穿透 COM + 程式設計模型，讓您瞭解它們是非常重要的。</span><span class="sxs-lookup"><span data-stu-id="60baa-133">By design, transactions so permeate the COM+ programming model that it is very important for you to understand them.</span></span> <span data-ttu-id="60baa-134">雖然您可以在不使用交易的情況下使用 COM + 的許多服務，但如果您選擇不使用交易，您就無法充分利用您可使用的 COM + 服務。</span><span class="sxs-lookup"><span data-stu-id="60baa-134">While you can make use of many of the services of COM+ without using transactions, if you choose not to use them, you cannot take full advantage of the COM+ services available to you.</span></span> <span data-ttu-id="60baa-135">使用交易的一些重要優點包括下列各項：</span><span class="sxs-lookup"><span data-stu-id="60baa-135">Some important benefits of using transactions include the following:</span></span>
    -   <span data-ttu-id="60baa-136">交易是並行管理問題的合理解決方案。</span><span class="sxs-lookup"><span data-stu-id="60baa-136">Transactions are a reasonable solution for the problem of concurrency management.</span></span> <span data-ttu-id="60baa-137">此外，交易也有助於防止當機，且具有良好的錯誤復原模式。</span><span class="sxs-lookup"><span data-stu-id="60baa-137">Also, transactions help protect against crashes and have a good error recovery model.</span></span> <span data-ttu-id="60baa-138">此外，交易也會成為跨多個系統管理工作的絕佳方法。</span><span class="sxs-lookup"><span data-stu-id="60baa-138">In addition, transactions turn out to be a great way to manage tasks across multiple systems.</span></span>
    -   <span data-ttu-id="60baa-139">您可以設計以交易為基礎的 COM + 應用程式，以使用 resource manager 和資料庫，以協助保護大部分的狀態資訊。</span><span class="sxs-lookup"><span data-stu-id="60baa-139">You can design a transaction-based COM+ application to work with a resource manager and a database, which helps protect most state information.</span></span> <span data-ttu-id="60baa-140">藉由將狀態保留在資料庫中，或由資源管理員管理的其他儲存體中，您就不需要在應用程式所建立的實際物件內保留很多狀態。</span><span class="sxs-lookup"><span data-stu-id="60baa-140">By keeping state inside a database or some other storage managed by a resource manager, you don't have to keep much state inside the actual objects your application creates.</span></span> <span data-ttu-id="60baa-141">雖然這是來自純粹面向物件模型的離開，但它很適合用來建立具有錯誤復原的分散式應用程式。</span><span class="sxs-lookup"><span data-stu-id="60baa-141">While this is a departure from a pure object-oriented model, it works well for creating distributed applications with error recovery.</span></span>
-   <span data-ttu-id="60baa-142">**應用程式功能是以 COM 物件的形式建立，包裝用來與其他系統或技術通訊的通訊協定。**</span><span class="sxs-lookup"><span data-stu-id="60baa-142">**Application functionality is built as COM objects, wrapping the protocols used to communicate with other systems or technologies.**</span></span> <span data-ttu-id="60baa-143">因為您可能正在建立將會結合數個技術或舊版系統的元件，所以請規劃使用各種不同的通訊協定。</span><span class="sxs-lookup"><span data-stu-id="60baa-143">Because you are probably building components that are going to stitch together several technologies or legacy systems, plan on using a variety of communication protocols.</span></span> <span data-ttu-id="60baa-144">使用 HTTP 進行用戶端/伺服器通訊，或透過網際網路進行應用程式對應用程式的通訊。</span><span class="sxs-lookup"><span data-stu-id="60baa-144">Use HTTP for client/server communication or application-to-application communication over the Internet.</span></span> <span data-ttu-id="60baa-145">使用 DCOM 在伺服器上進行應用程式對應用程式或元件對元件通訊。</span><span class="sxs-lookup"><span data-stu-id="60baa-145">Use DCOM for application-to-application or component-to-component communication on the server.</span></span>

## <a name="related-topics"></a><span data-ttu-id="60baa-146">相關主題</span><span class="sxs-lookup"><span data-stu-id="60baa-146">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="60baa-147">設計 COM + 應用程式的基本指導方針</span><span class="sxs-lookup"><span data-stu-id="60baa-147">Basic Guidelines for Designing COM+ Applications</span></span>](basic-guidelines-for-designing-com--applications.md)
</dt> <dt>

[<span data-ttu-id="60baa-148">使用 UML 設計 COM + 應用程式</span><span class="sxs-lookup"><span data-stu-id="60baa-148">Designing the COM+ Application Using UML</span></span>](designing-the-com--application-using-uml.md)
</dt> <dt>

[<span data-ttu-id="60baa-149">使用 COM + 的一般設計秘訣</span><span class="sxs-lookup"><span data-stu-id="60baa-149">General Design Tips for Using COM+</span></span>](general-design-tips-for-using-com-.md)
</dt> <dt>

[<span data-ttu-id="60baa-150">優化與 COM + 商務邏輯層的互動</span><span class="sxs-lookup"><span data-stu-id="60baa-150">Optimizing Interactions with the COM+ Business Logic Tier</span></span>](optimizing-interactions-with-the-com--business-logic-tier.md)
</dt> <dt>

[<span data-ttu-id="60baa-151">用來建立分散式應用程式的其他 Microsoft 工具</span><span class="sxs-lookup"><span data-stu-id="60baa-151">Other Microsoft Tools for Building Distributed Applications</span></span>](other-microsoft-tools-for-building-distributed-applications.md)
</dt> </dl>

 

 



