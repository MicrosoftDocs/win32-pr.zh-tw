---
description: 可用性是指應用程式容忍伺服器資源失敗的能力。
ms.assetid: 5d9a8216-a568-4443-b94f-1b2f2827a4be
title: 可用性設計
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 222583c9f53a1ccc88f2a4f984f445de02a2c976
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/07/2021
ms.locfileid: "104510548"
---
# <a name="designing-for-availability"></a><span data-ttu-id="3ef35-103">可用性設計</span><span class="sxs-lookup"><span data-stu-id="3ef35-103">Designing for Availability</span></span>

<span data-ttu-id="3ef35-104">可用性是指應用程式容忍伺服器資源失敗的能力。</span><span class="sxs-lookup"><span data-stu-id="3ef35-104">Availability is the ability of an application to tolerate failures in server resources.</span></span> <span data-ttu-id="3ef35-105">這表示用戶端會繼續透過失敗提供服務，而且在理想情況下，用戶端的失敗是透明的。</span><span class="sxs-lookup"><span data-stu-id="3ef35-105">This means that the client continues to be served through the failure and that, ideally, the failure is transparent to the client.</span></span> <span data-ttu-id="3ef35-106">顯然，失敗可能來自硬體或軟體來源，因此您必須針對這兩種情況進行開發。</span><span class="sxs-lookup"><span data-stu-id="3ef35-106">Obviously, the failure can come from either hardware or software sources, so you must develop for both cases.</span></span>

<span data-ttu-id="3ef35-107">可用性可能會受到下列因素影響：</span><span class="sxs-lookup"><span data-stu-id="3ef35-107">Availability can be affected by the following factors:</span></span>

-   <span data-ttu-id="3ef35-108">應用程式模型。</span><span class="sxs-lookup"><span data-stu-id="3ef35-108">Application model.</span></span> <span data-ttu-id="3ef35-109">為了達到最高可用性，請確定使用 [Com + 交易](com--transactions.md) 服務來進行重要的應用程式邏輯。</span><span class="sxs-lookup"><span data-stu-id="3ef35-109">For highest availability, ensure that the critical application logic is conducted using the [COM+ transactions](com--transactions.md) service.</span></span> <span data-ttu-id="3ef35-110">此外，使用補償機制可有效確保資源在失敗之後仍處於狀況良好的狀態。</span><span class="sxs-lookup"><span data-stu-id="3ef35-110">In addition, using a compensation mechanism can be effective in ensuring that resources remain in a healthy state after failures.</span></span>
-   <span data-ttu-id="3ef35-111">用戶端模型。</span><span class="sxs-lookup"><span data-stu-id="3ef35-111">Client model.</span></span> <span data-ttu-id="3ef35-112">將「失敗時重試」邏輯整合至用戶端應用程式，並在資源或服務無法使用時，盡力在應用程式中進行正常的效能降低。</span><span class="sxs-lookup"><span data-stu-id="3ef35-112">Integrate "retry on failure" logic into the client application, and strive for a graceful degradation in the application if resources or services are unavailable.</span></span> <span data-ttu-id="3ef35-113">瞭解用戶端從應用程式所預期的內容，並建立可在發生失敗時提供替代方案的設計。</span><span class="sxs-lookup"><span data-stu-id="3ef35-113">Understand what the client is expecting from the application, and create a design that allows for alternatives when a failure occurs.</span></span>
-   <span data-ttu-id="3ef35-114">資料/狀態可用性。</span><span class="sxs-lookup"><span data-stu-id="3ef35-114">Data/state availability.</span></span> <span data-ttu-id="3ef35-115">若要一致地存取持續性資料，請使用 Windows 叢集來提供容錯移轉支援。</span><span class="sxs-lookup"><span data-stu-id="3ef35-115">For consistent access to persistent data, use Windows Clustering to provide failover support.</span></span>
-   <span data-ttu-id="3ef35-116">服務可用性。</span><span class="sxs-lookup"><span data-stu-id="3ef35-116">Service availability.</span></span> <span data-ttu-id="3ef35-117">您可以使用網路負載平衡，以平衡伺服器叢集內的連入 IP 要求。</span><span class="sxs-lookup"><span data-stu-id="3ef35-117">You can use Network Load Balancing to load balance incoming IP requests across a cluster of servers.</span></span>

## <a name="related-topics"></a><span data-ttu-id="3ef35-118">相關主題</span><span class="sxs-lookup"><span data-stu-id="3ef35-118">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="3ef35-119">設計部署</span><span class="sxs-lookup"><span data-stu-id="3ef35-119">Designing for Deployment</span></span>](designing-for-deployment.md)
</dt> <dt>

[<span data-ttu-id="3ef35-120">擴充性設計</span><span class="sxs-lookup"><span data-stu-id="3ef35-120">Designing for Scalability</span></span>](designing-for-scalability.md)
</dt> <dt>

[<span data-ttu-id="3ef35-121">安全性設計</span><span class="sxs-lookup"><span data-stu-id="3ef35-121">Designing for Security</span></span>](designing-for-security.md)
</dt> </dl>

 

 



