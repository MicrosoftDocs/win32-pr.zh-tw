---
description: 設計 COM + 應用程式的基本指導方針
ms.assetid: 2d08bd05-5b0c-480c-91fd-b2bf321fc21e
title: 設計 COM + 應用程式的基本指導方針
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 7b6552022c3a9c2f50172164d1ed60811c5272e0
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/07/2021
ms.locfileid: "104111045"
---
# <a name="basic-guidelines-for-designing-com-applications"></a><span data-ttu-id="d0eaa-103">設計 COM + 應用程式的基本指導方針</span><span class="sxs-lookup"><span data-stu-id="d0eaa-103">Basic Guidelines for Designing COM+ Applications</span></span>

<span data-ttu-id="d0eaa-104">若要充分利用 COM +，您可以在建立應用程式時使用幾個基本指導方針：</span><span class="sxs-lookup"><span data-stu-id="d0eaa-104">To take full advantage of COM+, there are a few basic guidelines you can use when creating an application:</span></span>

-   <span data-ttu-id="d0eaa-105">**使用您選擇的資料庫工具，將您的持久狀態模型為資料庫架構。**</span><span class="sxs-lookup"><span data-stu-id="d0eaa-105">**Model your durable state as a database schema, using your database tool of choice.**</span></span> <span data-ttu-id="d0eaa-106">幾乎每個應用程式都必須維持持久狀態。</span><span class="sxs-lookup"><span data-stu-id="d0eaa-106">Almost every application needs to maintain durable state.</span></span> <span data-ttu-id="d0eaa-107">資料庫會提供建立持久且可調整的狀態儲存區所需的服務。</span><span class="sxs-lookup"><span data-stu-id="d0eaa-107">Databases provide the services needed to create durable and scalable storage of state.</span></span> <span data-ttu-id="d0eaa-108">因此，建立 COM + 應用程式的第一個步驟是將應用程式的持久狀態模型為某種資料庫架構。</span><span class="sxs-lookup"><span data-stu-id="d0eaa-108">Therefore, the first step in creating a COM+ application is to model the durable state of your application as some sort of database schema.</span></span> <span data-ttu-id="d0eaa-109">您所使用的資料庫並不重要，大部分的商務資料庫都與 COM + 相容。</span><span class="sxs-lookup"><span data-stu-id="d0eaa-109">It doesn't really matter what database you use; most commercial databases are compatible with COM+.</span></span> <span data-ttu-id="d0eaa-110">Microsoft SQL Server 是一個可供您使用的解決方案的絕佳範例。</span><span class="sxs-lookup"><span data-stu-id="d0eaa-110">Microsoft SQL Server is a good example of one solution you could use.</span></span>

-   <span data-ttu-id="d0eaa-111">**將 COM + 應用程式的邏輯模型為一組 COM 介面。**</span><span class="sxs-lookup"><span data-stu-id="d0eaa-111">**Model the logic of your COM+ application as a set of COM interfaces.**</span></span> <span data-ttu-id="d0eaa-112">當您的架構表示應用程式的狀態資訊之後，就會將應用程式中發生的交換模型為 COM 介面。</span><span class="sxs-lookup"><span data-stu-id="d0eaa-112">Once you have a schema that represents the state information of the application, model the interchanges that happen in the application as COM interfaces.</span></span> <span data-ttu-id="d0eaa-113">這些介面會建立應用程式行為的模型。</span><span class="sxs-lookup"><span data-stu-id="d0eaa-113">These interfaces will model the behavior of the application.</span></span> <span data-ttu-id="d0eaa-114">當您應判斷哪些 COM + 服務最適合您的應用程式時，這也是開發階段。</span><span class="sxs-lookup"><span data-stu-id="d0eaa-114">This is also the development stage when you should determine which COM+ services work best for your application.</span></span>

-   <span data-ttu-id="d0eaa-115">**建立元件 Dll，其中包含使用實體資料結構描述的元件，並將資料的邏輯觀點公開 (給此清單中的第一個專案) ，以及在邏輯資料模型中所實行的元件， (此清單) 的第二個專案。**</span><span class="sxs-lookup"><span data-stu-id="d0eaa-115">**Build component DLLs that contain components that use the physical data schema and expose a logical view of the data to other components (the first item in this list), as well as components that are implemented in terms of the logical data model (the second item in this list).**</span></span> <span data-ttu-id="d0eaa-116">當您擁有邏輯的結構和狀態資訊之後，就可以開始撰寫程式碼，而且現在可以撰寫以 DLL 為基礎的 COM 元件，這些元件會根據定義的架構來執行介面。</span><span class="sxs-lookup"><span data-stu-id="d0eaa-116">Once you have the structure of the logic and the state information, you can begin to write code and can now write DLL-based COM components that implement the interfaces in terms of the defined schema.</span></span> <span data-ttu-id="d0eaa-117">您的元件只是用來處理資料庫資訊的操作工具，而且您的元件 Dll 可讓您建立可正常運作且可順利調整的 COM + 應用程式。</span><span class="sxs-lookup"><span data-stu-id="d0eaa-117">Your components simply act as manipulators for working with your database information, and your component DLLs enable you build a COM+ application that works and that scales successfully.</span></span>

-   <span data-ttu-id="d0eaa-118">**使用您所選取的 COM + 服務，在 COM + 環境中部署元件。**</span><span class="sxs-lookup"><span data-stu-id="d0eaa-118">**Deploy the components in the COM+ environment using the COM+ services you've selected.**</span></span> <span data-ttu-id="d0eaa-119">建立應用程式之後，您就可以在網路或伺服器叢集上部署應用程式。</span><span class="sxs-lookup"><span data-stu-id="d0eaa-119">Once you have built the application, you can then deploy the application across a network or server cluster.</span></span> <span data-ttu-id="d0eaa-120">您現在可以根據可用的資源進行決策，並可為每個元件量身打造以獲得最大效能。</span><span class="sxs-lookup"><span data-stu-id="d0eaa-120">You can now make decisions based on resources available, and you can tailor each component for maximum performance.</span></span>

## <a name="related-topics"></a><span data-ttu-id="d0eaa-121">相關主題</span><span class="sxs-lookup"><span data-stu-id="d0eaa-121">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="d0eaa-122">COM + 設計假設和原則</span><span class="sxs-lookup"><span data-stu-id="d0eaa-122">COM+ Design Assumptions and Principles</span></span>](com--design-assumptions-and-principles.md)
</dt> <dt>

[<span data-ttu-id="d0eaa-123">使用 UML 設計 COM + 應用程式</span><span class="sxs-lookup"><span data-stu-id="d0eaa-123">Designing the COM+ Application Using UML</span></span>](designing-the-com--application-using-uml.md)
</dt> <dt>

[<span data-ttu-id="d0eaa-124">使用 COM + 的一般設計秘訣</span><span class="sxs-lookup"><span data-stu-id="d0eaa-124">General Design Tips for Using COM+</span></span>](general-design-tips-for-using-com-.md)
</dt> <dt>

[<span data-ttu-id="d0eaa-125">優化與 COM + 商務邏輯層的互動</span><span class="sxs-lookup"><span data-stu-id="d0eaa-125">Optimizing Interactions with the COM+ Business Logic Tier</span></span>](optimizing-interactions-with-the-com--business-logic-tier.md)
</dt> <dt>

[<span data-ttu-id="d0eaa-126">用來建立分散式應用程式的其他 Microsoft 工具</span><span class="sxs-lookup"><span data-stu-id="d0eaa-126">Other Microsoft Tools for Building Distributed Applications</span></span>](other-microsoft-tools-for-building-distributed-applications.md)
</dt> </dl>

 

 



