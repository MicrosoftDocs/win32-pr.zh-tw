---
description: 概念模型：應用程式需求
ms.assetid: 124b329b-f745-45b4-b266-7c177c76a5cd
title: 概念模型：應用程式需求
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: a5a287ff940f154bf104bbb50f6362bf573d9223
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/07/2021
ms.locfileid: "104111020"
---
# <a name="the-conceptual-model-application-requirements"></a><span data-ttu-id="dd2d4-103">概念模型：應用程式需求</span><span class="sxs-lookup"><span data-stu-id="dd2d4-103">The Conceptual Model: Application Requirements</span></span>

<span data-ttu-id="dd2d4-104">設計概念模型時，您需要定義商務問題以及解決這些問題所需的功能。</span><span class="sxs-lookup"><span data-stu-id="dd2d4-104">When designing the conceptual model, you need to define the business problems and the functions required to solve those problems.</span></span> <span data-ttu-id="dd2d4-105">最佳做法是與實際使用應用程式的人員討論、與廣大的使用者見面，以及盡可能納入最多的商務或使用者案例。</span><span class="sxs-lookup"><span data-stu-id="dd2d4-105">A best-practices approach is to talk with people who will actually use the application, meet with a broad range of users, and include as many business or user scenarios as possible.</span></span> <span data-ttu-id="dd2d4-106">判斷系統可能使用者的身分識別和數量，以及相關資料的大小與範圍。</span><span class="sxs-lookup"><span data-stu-id="dd2d4-106">Determine the identities and number of the system's potential users, as well as the size and scope of the data involved.</span></span> <span data-ttu-id="dd2d4-107">雖然收集這項資訊可能是設計流程中最不的技術層面，但這是最重要的一環。</span><span class="sxs-lookup"><span data-stu-id="dd2d4-107">Although gathering this information may be the least technical aspect of the design process, it is one of the most important.</span></span> <span data-ttu-id="dd2d4-108">若要開發成功的應用程式，您需要清楚瞭解需要解決的商務問題和流程。</span><span class="sxs-lookup"><span data-stu-id="dd2d4-108">To develop a successful application, you need a clear understanding of the business problems and processes that need to be addressed.</span></span>

<span data-ttu-id="dd2d4-109">判斷應用程式需求時，請記住下列考慮：</span><span class="sxs-lookup"><span data-stu-id="dd2d4-109">While determining the application requirements, keep the following considerations in mind:</span></span>

-   <span data-ttu-id="dd2d4-110">效能需求。</span><span class="sxs-lookup"><span data-stu-id="dd2d4-110">Performance requirements.</span></span> <span data-ttu-id="dd2d4-111">應用程式工作的預期回應時間為何？</span><span class="sxs-lookup"><span data-stu-id="dd2d4-111">What is the expected response time for application tasks?</span></span> <span data-ttu-id="dd2d4-112">需要關閉伺服器的容錯移轉支援？</span><span class="sxs-lookup"><span data-stu-id="dd2d4-112">What failover support for down servers is needed?</span></span> <span data-ttu-id="dd2d4-113">有哪些小時的可用性？</span><span class="sxs-lookup"><span data-stu-id="dd2d4-113">What are the hours of availability?</span></span>
-   <span data-ttu-id="dd2d4-114">環境。</span><span class="sxs-lookup"><span data-stu-id="dd2d4-114">Environment.</span></span> <span data-ttu-id="dd2d4-115">有哪些伺服器可供使用？</span><span class="sxs-lookup"><span data-stu-id="dd2d4-115">What servers are available?</span></span> <span data-ttu-id="dd2d4-116">是否已規劃其他伺服器來處理任何調整需求？</span><span class="sxs-lookup"><span data-stu-id="dd2d4-116">Are additional servers planned to handle any scaling requirements?</span></span>
-   <span data-ttu-id="dd2d4-117">部署。</span><span class="sxs-lookup"><span data-stu-id="dd2d4-117">Deployment.</span></span> <span data-ttu-id="dd2d4-118">應用程式將如何與目前的系統整合？</span><span class="sxs-lookup"><span data-stu-id="dd2d4-118">How will the application integrate with a current system?</span></span> <span data-ttu-id="dd2d4-119">應用程式會與其他系統互動嗎？</span><span class="sxs-lookup"><span data-stu-id="dd2d4-119">What other systems will the application interact with?</span></span> <span data-ttu-id="dd2d4-120">其他系統所使用的作業系統有哪些？</span><span class="sxs-lookup"><span data-stu-id="dd2d4-120">What operating systems do the other systems use?</span></span> <span data-ttu-id="dd2d4-121">應該支援哪些通訊協定？</span><span class="sxs-lookup"><span data-stu-id="dd2d4-121">What communication protocols should be supported?</span></span> <span data-ttu-id="dd2d4-122">您可以使用哪個 API 來與其他系統互動？</span><span class="sxs-lookup"><span data-stu-id="dd2d4-122">What API can you use to interact with the other systems?</span></span> <span data-ttu-id="dd2d4-123">其他系統位於網路上的何處？</span><span class="sxs-lookup"><span data-stu-id="dd2d4-123">Where are the other systems located on the network?</span></span> <span data-ttu-id="dd2d4-124">電腦使用的限制有哪些？</span><span class="sxs-lookup"><span data-stu-id="dd2d4-124">What restrictions on machine use are in place?</span></span> <span data-ttu-id="dd2d4-125">允許存取哪些使用者帳戶？</span><span class="sxs-lookup"><span data-stu-id="dd2d4-125">What user accounts are allowed access?</span></span>
-   <span data-ttu-id="dd2d4-126">位置。</span><span class="sxs-lookup"><span data-stu-id="dd2d4-126">Location.</span></span> <span data-ttu-id="dd2d4-127">相對於用戶端的資料位於何處？</span><span class="sxs-lookup"><span data-stu-id="dd2d4-127">Where is the data located in relation to the client?</span></span> <span data-ttu-id="dd2d4-128">資料是從遠端存取，還是在本機？</span><span class="sxs-lookup"><span data-stu-id="dd2d4-128">Is the data remotely accessed, or is it local?</span></span>
-   <span data-ttu-id="dd2d4-129">安全性。</span><span class="sxs-lookup"><span data-stu-id="dd2d4-129">Security.</span></span> <span data-ttu-id="dd2d4-130">是否有加密或完整性檢查需求？</span><span class="sxs-lookup"><span data-stu-id="dd2d4-130">Are there encryption or integrity checking requirements?</span></span> <span data-ttu-id="dd2d4-131">是否有驗證或資料保護需求？</span><span class="sxs-lookup"><span data-stu-id="dd2d4-131">Are there authentication or data protection requirements?</span></span>
-   <span data-ttu-id="dd2d4-132">存取權限。</span><span class="sxs-lookup"><span data-stu-id="dd2d4-132">Access rights.</span></span> <span data-ttu-id="dd2d4-133">誰有權執行特定作業的條件約束？</span><span class="sxs-lookup"><span data-stu-id="dd2d4-133">Are there constraints on who is allowed to perform certain operations?</span></span> <span data-ttu-id="dd2d4-134">如果是，您應該先記錄哪些作業需要授權，然後記載可擁有授權的使用者類型。</span><span class="sxs-lookup"><span data-stu-id="dd2d4-134">If so, you should first document which operations require authorization and then document the types of users who can have authorization.</span></span> <span data-ttu-id="dd2d4-135">這些需求可能會對應用程式的各個部分的執行方式造成很大的影響。</span><span class="sxs-lookup"><span data-stu-id="dd2d4-135">These requirements can have a big impact on how parts of the application are implemented.</span></span>

## <a name="related-topics"></a><span data-ttu-id="dd2d4-136">相關主題</span><span class="sxs-lookup"><span data-stu-id="dd2d4-136">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="dd2d4-137">邏輯模型：應用程式定義和規劃</span><span class="sxs-lookup"><span data-stu-id="dd2d4-137">The Logical Model: Application Definition and Planning</span></span>](the-logical-model--application-definition-and-planning.md)
</dt> <dt>

[<span data-ttu-id="dd2d4-138">實體模型：應用程式架構</span><span class="sxs-lookup"><span data-stu-id="dd2d4-138">The Physical Model: Application Architecture</span></span>](the-physical-model--application-architecture.md)
</dt> </dl>

 

 



