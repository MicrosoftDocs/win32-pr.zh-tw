---
description: 三層式架構模型，也就是邏輯設計模型的基本架構，將應用程式元件分成三個服務層級。
ms.assetid: a03327c1-e427-4c07-b3d4-808ce81c2c96
title: 使用 Three-Tier 架構模型
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: e20b765a6d103f3c349ffd9a44853f495c64a070
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/07/2021
ms.locfileid: "104385989"
---
# <a name="using-a-three-tier-architecture-model"></a><span data-ttu-id="3aa2c-103">使用 Three-Tier 架構模型</span><span class="sxs-lookup"><span data-stu-id="3aa2c-103">Using a Three-Tier Architecture Model</span></span>

<span data-ttu-id="3aa2c-104">三層式架構模型（ [邏輯設計模型](the-logical-model--application-definition-and-planning.md)的基本架構）會將應用程式的元件分割成三個服務層級。</span><span class="sxs-lookup"><span data-stu-id="3aa2c-104">The three-tier architecture model, which is the fundamental framework for the [logical design model](the-logical-model--application-definition-and-planning.md), segments an application's components into three tiers of services.</span></span> <span data-ttu-id="3aa2c-105">這些層級不一定會對應到網路上不同電腦上的實體位置，而是對應到應用程式的邏輯層。</span><span class="sxs-lookup"><span data-stu-id="3aa2c-105">These tiers do not necessarily correspond to physical locations on various computers on a network, but rather to logical layers of the application.</span></span> <span data-ttu-id="3aa2c-106">根據系統需求而定，應用程式的片段在實體拓撲中的散發方式可能會變更。</span><span class="sxs-lookup"><span data-stu-id="3aa2c-106">How the pieces of an application are distributed in a physical topology can change, depending on the system requirements.</span></span>

<span data-ttu-id="3aa2c-107">以下是配置給每一層的服務的簡短說明：</span><span class="sxs-lookup"><span data-stu-id="3aa2c-107">Following are brief descriptions of the services allocated to each tier:</span></span>

-   <span data-ttu-id="3aa2c-108">**展示層（或使用者服務層）可讓使用者存取應用程式。**</span><span class="sxs-lookup"><span data-stu-id="3aa2c-108">**The presentation tier, or user services layer, gives a user access to the application.**</span></span> <span data-ttu-id="3aa2c-109">這一層會向使用者呈現資料，並選擇性地允許資料操作和資料輸入。</span><span class="sxs-lookup"><span data-stu-id="3aa2c-109">This layer presents data to the user and optionally permits data manipulation and data entry.</span></span> <span data-ttu-id="3aa2c-110">這一層的兩個主要使用者介面類別型是傳統的應用程式和 Web 應用程式。</span><span class="sxs-lookup"><span data-stu-id="3aa2c-110">The two main types of user interface for this layer are the traditional application and the Web-based application.</span></span> <span data-ttu-id="3aa2c-111">Web 應用程式現在通常包含傳統應用程式所使用的大部分資料操作功能。</span><span class="sxs-lookup"><span data-stu-id="3aa2c-111">Web-based applications now often contain most of the data manipulation features that traditional applications use.</span></span> <span data-ttu-id="3aa2c-112">這可透過使用動態 HTML 和用戶端資料來源和資料指標來完成。</span><span class="sxs-lookup"><span data-stu-id="3aa2c-112">This is accomplished through use of Dynamic HTML and client-side data sources and data cursors.</span></span>

    > [!Note]  
    > <span data-ttu-id="3aa2c-113">在三層式應用程式中，用戶端應用程式將會 skinnier 至用戶端伺服器應用程式，因為它不會包含目前位於仲介層的服務元件。</span><span class="sxs-lookup"><span data-stu-id="3aa2c-113">In a three-tiered application, the client-side application will be skinnier than a client-server application because it will not contain the service components now located in the middle tier.</span></span> <span data-ttu-id="3aa2c-114">這會降低使用者的負擔，但系統會有更多的網路流量，因為元件是分散在不同的電腦上。</span><span class="sxs-lookup"><span data-stu-id="3aa2c-114">This results in less overhead for the user, but more network traffic for the system because components are distributed among different machines.</span></span>

     

-   <span data-ttu-id="3aa2c-115">**仲介層（或商務服務層）包含商務和資料規則。**</span><span class="sxs-lookup"><span data-stu-id="3aa2c-115">**The middle tier, or business services layer, consists of business and data rules.**</span></span> <span data-ttu-id="3aa2c-116">中介層也稱為 *商務邏輯層*，可讓 com + 開發人員解決任務關鍵性商務問題，並達到主要的生產力優勢。</span><span class="sxs-lookup"><span data-stu-id="3aa2c-116">Also referred to as the *business logic tier*, the middle tier is where COM+ developers can solve mission-critical business problems and achieve major productivity advantages.</span></span> <span data-ttu-id="3aa2c-117">組成此層的元件可以存在於伺服器機器上，以協助資源分享。</span><span class="sxs-lookup"><span data-stu-id="3aa2c-117">The components that make up this layer can exist on a server machine, to assist in resource sharing.</span></span> <span data-ttu-id="3aa2c-118">這些元件可以用來強制執行商務規則，例如商務演算法和法律或政府法規，以及資料規則，這些規則是設計用來在特定或多個資料庫中保持一致的資料結構。</span><span class="sxs-lookup"><span data-stu-id="3aa2c-118">These components can be used to enforce business rules, such as business algorithms and legal or governmental regulations, and data rules, which are designed to keep the data structures consistent within either specific or multiple databases.</span></span> <span data-ttu-id="3aa2c-119">因為這些中介層元件未系結至特定的用戶端，所以可供所有應用程式使用，並可移至不同的位置，因為回應時間和其他規則需要。</span><span class="sxs-lookup"><span data-stu-id="3aa2c-119">Because these middle-tier components are not tied to a specific client, they can be used by all applications and can be moved to different locations, as response time and other rules require.</span></span> <span data-ttu-id="3aa2c-120">例如，您可以在用戶端上放置簡單的編輯，以將網路往返降到最低，或將資料規則放在預存程式中。</span><span class="sxs-lookup"><span data-stu-id="3aa2c-120">For example, simple edits can be placed on the client side to minimize network round-trips, or data rules can be placed in stored procedures.</span></span>

-   <span data-ttu-id="3aa2c-121">**資料層或資料服務層會與持續性資料互動，通常儲存在資料庫或永久儲存體中。**</span><span class="sxs-lookup"><span data-stu-id="3aa2c-121">**The data tier, or data services layer, interacts with persistent data usually stored in a database or in permanent storage.**</span></span> <span data-ttu-id="3aa2c-122">這是實際的 DBMS 存取層。</span><span class="sxs-lookup"><span data-stu-id="3aa2c-122">This is the actual DBMS access layer.</span></span> <span data-ttu-id="3aa2c-123">它可透過商務服務層存取，並在使用者服務層級進行。</span><span class="sxs-lookup"><span data-stu-id="3aa2c-123">It can be accessed through the business services layer and on occasion by the user services layer.</span></span> <span data-ttu-id="3aa2c-124">這一層包含 (的資料存取元件，而不是原始的 DBMS 連接) 協助資源分享，並允許設定用戶端，而不需要在每個用戶端上安裝 DBMS 程式庫和 ODBC 驅動程式。</span><span class="sxs-lookup"><span data-stu-id="3aa2c-124">This layer consists of data access components (rather than raw DBMS connections) to aid in resource sharing and to allow clients to be configured without installing the DBMS libraries and ODBC drivers on each client.</span></span>

<span data-ttu-id="3aa2c-125">在應用程式的生命週期期間，三層式方法可提供重複使用性、彈性、管理性、可維護性和擴充性等優點。</span><span class="sxs-lookup"><span data-stu-id="3aa2c-125">During an application's life cycle, the three-tier approach provides benefits such as reusability, flexibility, manageability, maintainability, and scalability.</span></span> <span data-ttu-id="3aa2c-126">您可以共用和重複使用您所建立的元件和服務，也可以視需要將它們分散到電腦的網路上。</span><span class="sxs-lookup"><span data-stu-id="3aa2c-126">You can share and reuse the components and services you create, and you can distribute them across a network of computers as needed.</span></span> <span data-ttu-id="3aa2c-127">您可以將大型和複雜的專案分成更簡單的專案，並將它們指派給不同的程式設計人員或程式設計團隊。</span><span class="sxs-lookup"><span data-stu-id="3aa2c-127">You can divide large and complex projects into simpler projects and assign them to different programmers or programming teams.</span></span> <span data-ttu-id="3aa2c-128">您也可以在伺服器上部署元件和服務來協助保持最新的變更，而且您可以在應用程式的使用者群、資料和交易量增加的成長中重新部署它們。</span><span class="sxs-lookup"><span data-stu-id="3aa2c-128">You can also deploy components and services on a server to help keep up with changes, and you can redeploy them as growth of the application's user base, data, and transaction volume increases.</span></span>

## <a name="related-topics"></a><span data-ttu-id="3aa2c-129">相關主題</span><span class="sxs-lookup"><span data-stu-id="3aa2c-129">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="3aa2c-130">邏輯模型：應用程式定義和規劃</span><span class="sxs-lookup"><span data-stu-id="3aa2c-130">The Logical Model: Application Definition and Planning</span></span>](the-logical-model--application-definition-and-planning.md)
</dt> </dl>

 

 



