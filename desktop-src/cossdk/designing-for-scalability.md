---
description: 擴充功能可讓應用程式以線性方式增加資源使用量來服務額外的負載。
ms.assetid: 8249f1af-9c96-4545-ad6a-3736c6e63c6d
title: 擴充性設計
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 54ab0aa9d67afaac14c6d8f59df34183bde36113
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/07/2021
ms.locfileid: "106970910"
---
# <a name="designing-for-scalability"></a><span data-ttu-id="4008c-103">擴充性設計</span><span class="sxs-lookup"><span data-stu-id="4008c-103">Designing for Scalability</span></span>

<span data-ttu-id="4008c-104">擴充功能可讓應用程式以線性方式增加資源使用量來服務額外的負載。</span><span class="sxs-lookup"><span data-stu-id="4008c-104">Scalability is the ability of an application to service an additional load with a linear increase in resource usage.</span></span> <span data-ttu-id="4008c-105">在任何分散式應用程式中，擴充性都很重要。</span><span class="sxs-lookup"><span data-stu-id="4008c-105">Scalability is important in any distributed application.</span></span> <span data-ttu-id="4008c-106">擴充性的限制通常會在應用程式的設計中，以資源使用和不小心建立的相依性為中心。</span><span class="sxs-lookup"><span data-stu-id="4008c-106">Limits to scalability usually center around resource use and dependencies inadvertently created in the application's design.</span></span>

<span data-ttu-id="4008c-107">下列清單說明擴充性問題並建議解決方案：</span><span class="sxs-lookup"><span data-stu-id="4008c-107">The following list describes scalability issues and suggests solutions:</span></span>

-   <span data-ttu-id="4008c-108">電腦內部資源。</span><span class="sxs-lookup"><span data-stu-id="4008c-108">Intra-computer resources.</span></span> <span data-ttu-id="4008c-109">可用的執行緒和記憶體數目可以限制擴充性。</span><span class="sxs-lookup"><span data-stu-id="4008c-109">The number of threads and memory available can limit scalability.</span></span> <span data-ttu-id="4008c-110">針對您的應用程式使用最有效率的執行緒模型。</span><span class="sxs-lookup"><span data-stu-id="4008c-110">Use a threading model that is most efficient for your application.</span></span>
-   <span data-ttu-id="4008c-111">電腦間資源。</span><span class="sxs-lookup"><span data-stu-id="4008c-111">Inter-computer resources.</span></span> <span data-ttu-id="4008c-112">散發應用程式工作負載的可用電腦數目可能會影響擴充性。</span><span class="sxs-lookup"><span data-stu-id="4008c-112">The number of available computers to distribute the application workload can affect scalability.</span></span>
-   <span data-ttu-id="4008c-113">用戶端親和性。</span><span class="sxs-lookup"><span data-stu-id="4008c-113">Client affinity.</span></span> <span data-ttu-id="4008c-114">應用程式可能會不慎建立兩種親和性的情況：應用程式相依于用戶端隨其要求傳送的資料狀態;以及應用程式需要用戶端特定狀態的情況。</span><span class="sxs-lookup"><span data-stu-id="4008c-114">Two situations of affinity can be inadvertently created by an application: a situation where the application depends on state from data the client sends with its request; and a situation where the application requires a client-specific state.</span></span> <span data-ttu-id="4008c-115">避免在用戶端與應用程式之間設計狀態相依性。</span><span class="sxs-lookup"><span data-stu-id="4008c-115">Avoid designing state dependency between the client and the application.</span></span>
-   <span data-ttu-id="4008c-116">伺服器親和性。</span><span class="sxs-lookup"><span data-stu-id="4008c-116">Server affinity.</span></span> <span data-ttu-id="4008c-117">COM + 應用程式可以藉由建立伺服器親和性來限制其擴充性，而應用程式相依于前往特定的伺服器電腦以取得相關資訊。</span><span class="sxs-lookup"><span data-stu-id="4008c-117">A COM+ application can limit its scalability by creating a server affinity, where the application depends on going to a particular server computer for information.</span></span> <span data-ttu-id="4008c-118">許多資料庫導向應用程式可能會發生這個親和性。</span><span class="sxs-lookup"><span data-stu-id="4008c-118">This affinity can occur with many database-oriented applications.</span></span> <span data-ttu-id="4008c-119">避免伺服器親和性瓶頸的最佳方式，就是將資料分割到各種伺服器電腦上。</span><span class="sxs-lookup"><span data-stu-id="4008c-119">The best way to avoid a server-affinity bottleneck is to partition data onto various server computers.</span></span> <span data-ttu-id="4008c-120">例如，根據最常存取的金鑰將客戶資料分割在不同的伺服器上，或使用客戶的姓氏將客戶資料庫跨越數部伺服器 (例如 Server1： a-f、Server2： g-m、Server3： n-z) 。</span><span class="sxs-lookup"><span data-stu-id="4008c-120">For example, divide customer data among servers by the most frequently accessed key, or span a customer database over several servers using the customer's last name (for example, Server1: a-f, Server2: g-m, Server3: n-z).</span></span>
    > [!Note]  
    > <span data-ttu-id="4008c-121">資料分割可以在程式設計邏輯中增加很多複雜性，而且只有在嘗試增加擴充性的其他選項之後才應完成。</span><span class="sxs-lookup"><span data-stu-id="4008c-121">Data partitioning can add a great deal of complexity to the programming logic and should be done only after other options to increase scalability have been tried.</span></span>

     

-   <span data-ttu-id="4008c-122">物件存留期。</span><span class="sxs-lookup"><span data-stu-id="4008c-122">Object lifetime.</span></span> <span data-ttu-id="4008c-123">COM + 應用程式必須密切注意物件的存留期，才能進行擴充。</span><span class="sxs-lookup"><span data-stu-id="4008c-123">To be scalable, a COM+ application must pay close attention to the life span of objects.</span></span> <span data-ttu-id="4008c-124">當物件存在時，就會耗用資源。</span><span class="sxs-lookup"><span data-stu-id="4008c-124">While an object exists, it is consuming resources.</span></span> <span data-ttu-id="4008c-125">請務必確定保存到昂貴資源之物件的存留期是謹慎管理的。</span><span class="sxs-lookup"><span data-stu-id="4008c-125">It is important to make sure that the lifetimes of objects that hold onto expensive resources are carefully managed.</span></span> <span data-ttu-id="4008c-126">針對不耗用昂貴資源的高需求物件， [Com + 物件](com--object-pooling.md) 共用可以增加擴充性，因為您可以系統管理員調整共用值，以利用您可能擁有的任何硬體。</span><span class="sxs-lookup"><span data-stu-id="4008c-126">For high-demand objects that don't consume expensive resources, [COM+ object pooling](com--object-pooling.md) can increase scalability because you can administratively adjust the pooling values to take advantage of whatever hardware you might have.</span></span> <span data-ttu-id="4008c-127">這是控制連接的自然方式：例如，如果您有20個 SQL 連接的授權，您可以使用 [最大集區] 設定來指定。</span><span class="sxs-lookup"><span data-stu-id="4008c-127">And it's a natural way to govern connections: For example, if you have a license for 20 SQL connections, you can dictate that with the Max Pool setting.</span></span>
-   <span data-ttu-id="4008c-128">應用程式元件群組。</span><span class="sxs-lookup"><span data-stu-id="4008c-128">Application component grouping.</span></span> <span data-ttu-id="4008c-129">為了增強 COM + 應用程式的擴充性，中介層元件應該分成時間相依和與時間無關的服務。</span><span class="sxs-lookup"><span data-stu-id="4008c-129">To enhance the scalability of a COM+ application, the middle-tier components should be divided into time-dependent and time-independent services.</span></span> <span data-ttu-id="4008c-130">這可讓您專注于可能使用 Microsoft Windows 服務來執行必要的元件動作。</span><span class="sxs-lookup"><span data-stu-id="4008c-130">This allows you to focus on possibly using a Microsoft Windows service to implement a required component action.</span></span> <span data-ttu-id="4008c-131">例如，您可以選擇使用 [訊息佇列](/previous-versions/windows/desktop/legacy/ms711472(v=vs.85)) 或 [com + 佇列元件](com--queued-components.md) 等服務來處理與時間無關的非同步工作。</span><span class="sxs-lookup"><span data-stu-id="4008c-131">For example, you could elect to use a service such as [Message Queuing](/previous-versions/windows/desktop/legacy/ms711472(v=vs.85)) or [COM+ queued components](com--queued-components.md) to handle time-independent, asynchronous tasks.</span></span>

## <a name="related-topics"></a><span data-ttu-id="4008c-132">相關主題</span><span class="sxs-lookup"><span data-stu-id="4008c-132">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="4008c-133">可用性設計</span><span class="sxs-lookup"><span data-stu-id="4008c-133">Designing for Availability</span></span>](designing-for-availability.md)
</dt> <dt>

[<span data-ttu-id="4008c-134">設計部署</span><span class="sxs-lookup"><span data-stu-id="4008c-134">Designing for Deployment</span></span>](designing-for-deployment.md)
</dt> <dt>

[<span data-ttu-id="4008c-135">安全性設計</span><span class="sxs-lookup"><span data-stu-id="4008c-135">Designing for Security</span></span>](designing-for-security.md)
</dt> </dl>

 

 



