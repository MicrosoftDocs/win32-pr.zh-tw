---
title: 為何 Active Directory Domain Services 使用此複寫模型
description: 本主題說明 Active Directory Domain Services 用於複寫模型的自由格式系統的原因。
ms.assetid: 202df900-6d03-4aa8-9099-016238059ef4
ms.tgt_platform: multiple
keywords:
- 複寫模型 Active Directory，優點
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 538fe291a04953d373ff3cd45cbd4693d3dafab4
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 09/16/2019
ms.locfileid: "103839256"
---
# <a name="why-active-directory-domain-services-uses-this-replication-model"></a><span data-ttu-id="007d7-104">為何 Active Directory Domain Services 使用此複寫模型</span><span class="sxs-lookup"><span data-stu-id="007d7-104">Why Active Directory Domain Services Uses This Replication Model</span></span>

<span data-ttu-id="007d7-105">本主題說明 Active Directory Domain Services 用於複寫模型的自由格式系統的原因。</span><span class="sxs-lookup"><span data-stu-id="007d7-105">This topic explains the reasons for the free-form system used by Active Directory Domain Services for a replication model.</span></span>

<span data-ttu-id="007d7-106">Active Directory Domain Services 是一個自由形式的系統，原因如下：</span><span class="sxs-lookup"><span data-stu-id="007d7-106">Active Directory Domain Services are a free-form system for the following reasons:</span></span>

-   <span data-ttu-id="007d7-107">客戶需要高度分散的解決方案，其中的目錄部分可以散佈在其網路上，並在本機進行管理。</span><span class="sxs-lookup"><span data-stu-id="007d7-107">Customers require a highly distributed solution in which parts of the directory can be spread across their networks and administered locally.</span></span>
-   <span data-ttu-id="007d7-108">大型客戶通常會成長至數百萬個物件、數百個或數千個複本，或兩者。</span><span class="sxs-lookup"><span data-stu-id="007d7-108">Large customers often grow to millions of objects, hundreds or thousands of replicas, or both.</span></span>
-   <span data-ttu-id="007d7-109">許多客戶網路只提供與某些位置的間歇性連線;例如，遠端石油切入平臺並在海洋推出，因此系統必須能夠容忍部分連線或中斷連線的作業。</span><span class="sxs-lookup"><span data-stu-id="007d7-109">Many customer networks provide only intermittent connectivity to some locations; for example, remote oil drilling platforms and ships at sea, so the system must be tolerant of partly connected or disconnected operations.</span></span>

<span data-ttu-id="007d7-110">無法保證對分散式系統目前或未來狀態的完全感知，因為必須傳播狀態變更的知識，而且傳播需要一些時間，在這段期間可能會發生更多狀態變更。</span><span class="sxs-lookup"><span data-stu-id="007d7-110">There is no way to guarantee complete awareness of the current or future state of a distributed system because knowledge of state changes must be propagated and propagation takes time, during which more state changes may occur.</span></span>

<span data-ttu-id="007d7-111">緊密結合的系統會藉由嘗試消除不確定的方式來處理不確定性。</span><span class="sxs-lookup"><span data-stu-id="007d7-111">Tightly coupled systems handle uncertainty by attempting to eliminate it.</span></span> <span data-ttu-id="007d7-112">這是透過更新的限制所完成，要求所有節點或某些多數節點都可供使用，然後才可以執行更新、使用分散式鎖定配置或單一掌控的關鍵資源、限制所有節點的連接，或這些技巧的組合。</span><span class="sxs-lookup"><span data-stu-id="007d7-112">This is accomplished through constraints on updates, requiring all nodes or some majority of nodes to be available before updates can be performed, using distributed locking schemes or single-mastering for critical resources, constraining all nodes to be well-connected, or some combination of these techniques.</span></span> <span data-ttu-id="007d7-113">在分散式系統中，更緊密結合的運算節點是調整規模限制較低的位置。</span><span class="sxs-lookup"><span data-stu-id="007d7-113">The more tightly coupled the computing nodes in a distributed system are, the lower the scaling limit.</span></span>

<span data-ttu-id="007d7-114">自由形式的系統會藉由容許來處理不確定性。</span><span class="sxs-lookup"><span data-stu-id="007d7-114">Free-form systems handle uncertainty by tolerating it.</span></span> <span data-ttu-id="007d7-115">自由形式的系統可讓節點擁有整體系統狀態的不同視圖，並提供演算法來解決衝突。</span><span class="sxs-lookup"><span data-stu-id="007d7-115">A free-form system enables the nodes to have differing views of the overall system state and provides algorithms for resolving conflicts.</span></span>

<span data-ttu-id="007d7-116">因為本機系統管理、中斷連線的作業，以及非常大量節點的擴充性需求，所以將緊密結合的解決方案拒絕為不適合 Active Directory Domain Services。</span><span class="sxs-lookup"><span data-stu-id="007d7-116">Tightly coupled solutions were rejected as unsuitable for Active Directory Domain Services because of the requirements for local administration, disconnected operation, and scalability to very large numbers of nodes.</span></span> <span data-ttu-id="007d7-117">選擇的鬆散結合模型、聚合的多宿主鬆散一致性，滿足所有需求。</span><span class="sxs-lookup"><span data-stu-id="007d7-117">The loosely coupled model chosen, multi-master loose consistency with convergence, satisfies all requirements.</span></span>

 

 




