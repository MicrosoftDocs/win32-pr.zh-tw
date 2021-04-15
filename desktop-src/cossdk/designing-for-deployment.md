---
description: 設計部署
ms.assetid: 31244998-34f5-4fd8-95f6-adcc134bcaf3
title: 設計部署
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 2e60ac561bd05d08253433e52c7f00c2def54df3
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/07/2021
ms.locfileid: "104468109"
---
# <a name="designing-for-deployment"></a><span data-ttu-id="77476-103">設計部署</span><span class="sxs-lookup"><span data-stu-id="77476-103">Designing for Deployment</span></span>

<span data-ttu-id="77476-104">規劃 COM + 應用程式的範圍是您應該提早考慮的重要設計工作。</span><span class="sxs-lookup"><span data-stu-id="77476-104">Planning the scope of COM+ applications is an important design task you should consider early on.</span></span> <span data-ttu-id="77476-105">使用 COM + 執行的分散式系統應設計為具有最少個別設定的部署，以及最有效率地使用每個進程。</span><span class="sxs-lookup"><span data-stu-id="77476-105">Distributed systems that are intended to run using COM+ should be designed for deployment with the least amount of individual configuration and to most efficiently use each process.</span></span> <span data-ttu-id="77476-106">您也可以使用這些技術，讓您在部署 COM + 應用程式時達到最佳效能。</span><span class="sxs-lookup"><span data-stu-id="77476-106">There are also techniques you can use that will enable you to achieve optimal performance when deploying a COM+ application.</span></span> <span data-ttu-id="77476-107"> (需詳細資訊，請參閱 [部署以加快通訊速度](deploying-for-faster-communication.md)) </span><span class="sxs-lookup"><span data-stu-id="77476-107">(For more information, see [Deploying for Faster Communication](deploying-for-faster-communication.md).)</span></span>

<span data-ttu-id="77476-108">使用 [元件服務] 系統管理工具來查看時，每個 COM + 應用程式都會顯示為一個資料夾，其中包含以邏輯方式分組的元件集。</span><span class="sxs-lookup"><span data-stu-id="77476-108">When viewed with the Component Services administrative tool, each COM+ application appears as a folder within which sets of components are logically grouped.</span></span> <span data-ttu-id="77476-109">雖然您可以在 COM + 應用程式 **元件** 資料夾之間移動個別元件 (換句話說，從某個應用程式到另一個) ，在 com + 應用層級（例如安全性）設定的數個服務可能會不同。</span><span class="sxs-lookup"><span data-stu-id="77476-109">While you can move individual components between COM+ application **Components** folders (in other words, from one application to another), several services set at the COM+ application level, such as security, may differ.</span></span> <span data-ttu-id="77476-110">這些服務設定可能會影響可攜性。</span><span class="sxs-lookup"><span data-stu-id="77476-110">These service settings can affect portability.</span></span>

## <a name="a-com-server-application-defines-a-process-boundary"></a><span data-ttu-id="77476-111">COM + 伺服器應用程式定義進程界限</span><span class="sxs-lookup"><span data-stu-id="77476-111">A COM+ Server Application Defines a Process Boundary</span></span>

<span data-ttu-id="77476-112">當您建立新的 COM + 伺服器應用程式時，您實際上是定義新的進程界限。</span><span class="sxs-lookup"><span data-stu-id="77476-112">When you create a new COM+ server application, you are really defining a new process boundary.</span></span> <span data-ttu-id="77476-113"> (記下以下說明的程式庫應用程式例外狀況。 ) 此程式會成為 COM + 應用程式中所包含元件的控制應用程式實例。</span><span class="sxs-lookup"><span data-stu-id="77476-113">(Note the exception for library applications explained below.) This process becomes the controlling application instance for the components that are contained in the COM+ application.</span></span> <span data-ttu-id="77476-114">當程式第一次呼叫 COM + 應用程式時，這些元件都會在 COM + 可執行程式的新實例中執行同進程。</span><span class="sxs-lookup"><span data-stu-id="77476-114">These components all run in-process in a new instance of the COM+ executable program whenever a program calls into a COM+ application for the first time.</span></span> <span data-ttu-id="77476-115">這表示指定的 COM + 應用程式 **元件** 資料夾內的所有元件都是在作為 DCOM 伺服器的單一進程空間中執行。</span><span class="sxs-lookup"><span data-stu-id="77476-115">This means that all of the components within a given COM+ application's **Components** folder run in a single process space that serves as the DCOM server.</span></span> <span data-ttu-id="77476-116">在 COM + 應用程式中，COM + 會管理記憶體、與分散式交易協調器 (DTC) 、及時元件實例啟用、損毀偵測和復原，以及以角色為基礎的安全性。</span><span class="sxs-lookup"><span data-stu-id="77476-116">Within the COM+ application, COM+ manages memory, coordination with the Distributed Transaction Coordinator (DTC), just-in-time component instance activation, crash detection and recovery, and role-based security.</span></span>

## <a name="calling-across-com-application-boundaries"></a><span data-ttu-id="77476-117">跨 COM + 應用程式界限呼叫</span><span class="sxs-lookup"><span data-stu-id="77476-117">Calling Across COM+ Application Boundaries</span></span>

<span data-ttu-id="77476-118">因為每個 COM + 應用程式通常會實作為個別可執行檔，所以將分散式應用程式分割成多個 COM + 應用程式的影響會在某個 COM + 應用程式中的元件呼叫另一個 COM + 應用程式中的元件時，引進跨進程 COM 呼叫。</span><span class="sxs-lookup"><span data-stu-id="77476-118">Because each COM+ application normally is implemented as a separate executable, the effect of splitting a distributed application across multiple COM+ applications introduces out-of-process COM calls when components in one COM+ application call the components in another COM+ application.</span></span> <span data-ttu-id="77476-119">這會導致效能降低，因為跨進程的封送處理 COM 參數會產生額外的負擔。</span><span class="sxs-lookup"><span data-stu-id="77476-119">This introduces performance degradation due to the extra burden that marshaling COM parameters across processes imposes.</span></span>

> [!Note]  
> <span data-ttu-id="77476-120">造成此效能的影響不會發生任何問題，您只需要知道，就會發生這種情形。</span><span class="sxs-lookup"><span data-stu-id="77476-120">There is nothing inherently wrong with incurring this performance penalty; you just need to be aware that it is going to occur.</span></span> <span data-ttu-id="77476-121">根據所需的回應時間、將同時要求商務服務的使用者數目，以及每個元件新增到每個 COM + 應用程式的額外啟動負擔，您可能會發現可接受對跨應用程式呼叫造成的效能衝擊。</span><span class="sxs-lookup"><span data-stu-id="77476-121">Depending on the required response time, the number of users that will simultaneously request business services, and the added start-up burden that each component adds to each COM+ application, you may find that the performance hit attributable to cross-application calls is acceptable.</span></span>

 

<span data-ttu-id="77476-122">消除跨 COM + 應用程式界限呼叫之效能損失的其中一種可能性，是將指定的 COM + 應用程式標示為程式庫應用程式。</span><span class="sxs-lookup"><span data-stu-id="77476-122">One possibility that eliminates the performance penalty of calling across COM+ application boundaries is to mark a given COM+ application as a library application.</span></span> <span data-ttu-id="77476-123">COM + 程式庫應用程式是在建立它的用戶端的進程中執行。</span><span class="sxs-lookup"><span data-stu-id="77476-123">A COM+ library application runs in the process of the client that creates it.</span></span> <span data-ttu-id="77476-124">當然，不會有任何效能提升的成本。</span><span class="sxs-lookup"><span data-stu-id="77476-124">Of course, no performance gain has zero cost.</span></span> <span data-ttu-id="77476-125">在此情況下，取捨牽涉到 COM + 程式庫應用程式的限制。</span><span class="sxs-lookup"><span data-stu-id="77476-125">In this case, the trade-off involves the limitations of COM+ library applications.</span></span> <span data-ttu-id="77476-126">雖然程式庫應用程式可以使用以角色為基礎的安全性，但它無法支援已排入佇列的元件或遠端存取。</span><span class="sxs-lookup"><span data-stu-id="77476-126">While a library application can use role-based security, it cannot support queued components or remote access.</span></span>

## <a name="related-topics"></a><span data-ttu-id="77476-127">相關主題</span><span class="sxs-lookup"><span data-stu-id="77476-127">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="77476-128">部署以加快通訊速度</span><span class="sxs-lookup"><span data-stu-id="77476-128">Deploying for Faster Communication</span></span>](deploying-for-faster-communication.md)
</dt> <dt>

[<span data-ttu-id="77476-129">可用性設計</span><span class="sxs-lookup"><span data-stu-id="77476-129">Designing for Availability</span></span>](designing-for-availability.md)
</dt> <dt>

[<span data-ttu-id="77476-130">擴充性設計</span><span class="sxs-lookup"><span data-stu-id="77476-130">Designing for Scalability</span></span>](designing-for-scalability.md)
</dt> <dt>

[<span data-ttu-id="77476-131">安全性設計</span><span class="sxs-lookup"><span data-stu-id="77476-131">Designing for Security</span></span>](designing-for-security.md)
</dt> </dl>

 

 



