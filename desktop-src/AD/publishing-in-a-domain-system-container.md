---
title: 在網域系統容器中發佈
description: 網域分割區的系統容器會保存每個網域的操作資訊。
ms.assetid: 18bb3409-774e-42d9-8f27-6c582d74ca86
ms.tgt_platform: multiple
keywords:
- 在網域系統容器中發佈
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: bdf7d1febd91e3540c7bc2002a36d33346820344
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 09/16/2019
ms.locfileid: "103839275"
---
# <a name="publishing-in-a-domain-system-container"></a><span data-ttu-id="ec3ea-104">在網域系統容器中發佈</span><span class="sxs-lookup"><span data-stu-id="ec3ea-104">Publishing in a Domain System Container</span></span>

<span data-ttu-id="ec3ea-105">網域分割區的系統容器會保存每個網域的操作資訊。</span><span class="sxs-lookup"><span data-stu-id="ec3ea-105">The System container of a domain partition holds per-domain operational information.</span></span> <span data-ttu-id="ec3ea-106">這包括預設的本機安全性原則、檔案連結追蹤、網路會議，以及 Windows 通訊端註冊和解析的容器 (RnR) 和 RPC 名稱服務 (RpcNs) 連接點。</span><span class="sxs-lookup"><span data-stu-id="ec3ea-106">This includes the default local security policy, file link tracking, network meetings, and containers for Windows Sockets registration and resolution (RnR) and RPC name service (RpcNs) connection points.</span></span> <span data-ttu-id="ec3ea-107">預設會隱藏 [系統] 容器，並提供方便的位置來儲存系統管理員感興趣的物件，而不是終端使用者。</span><span class="sxs-lookup"><span data-stu-id="ec3ea-107">The system container is hidden, by default, and provides a convenient place for storing objects that are of interest to administrators, but not to end users.</span></span>

<span data-ttu-id="ec3ea-108">未系結至單一主機的服務可能會想要在網域分割區的系統容器下建立其 Scp。</span><span class="sxs-lookup"><span data-stu-id="ec3ea-108">Services that are not tied to a single host may want to create their SCPs under the System container of a domain partition.</span></span> <span data-ttu-id="ec3ea-109">此替代方案適用于在多部主機上安裝複本的服務，每個複本都會為整個網域中的用戶端提供相同的服務。</span><span class="sxs-lookup"><span data-stu-id="ec3ea-109">This alternative can be useful for services with replicas installed on multiple hosts, each replica providing identical services to clients throughout the domain.</span></span> <span data-ttu-id="ec3ea-110">它可讓您在單一容器下將複寫服務的所有物件分組。</span><span class="sxs-lookup"><span data-stu-id="ec3ea-110">It enables you to group all the objects for the replicated service under a single container.</span></span>

<span data-ttu-id="ec3ea-111">在系統容器中建立服務特定物件的服務必須執行下列動作：</span><span class="sxs-lookup"><span data-stu-id="ec3ea-111">Services that create service-specific objects in the System container must do the following:</span></span>

1.  <span data-ttu-id="ec3ea-112">建立物件類別 **容器** 的子容器，做為系統容器的直屬子系。</span><span class="sxs-lookup"><span data-stu-id="ec3ea-112">Create a sub-container of object class **container** as an immediate child of the System container.</span></span> <span data-ttu-id="ec3ea-113">提供此子容器名稱，以明確地將其識別為與服務有關的名稱。</span><span class="sxs-lookup"><span data-stu-id="ec3ea-113">Give this sub-container a name that clearly identifies it as pertaining to the service.</span></span>
2.  <span data-ttu-id="ec3ea-114">在這個子容器中建立與服務相關的物件。</span><span class="sxs-lookup"><span data-stu-id="ec3ea-114">Create the service-related objects in this sub-container.</span></span> <span data-ttu-id="ec3ea-115">例如，「NetMeeting」使用「會議」容器來發佈網路會議物件。</span><span class="sxs-lookup"><span data-stu-id="ec3ea-115">For example, NetMeeting uses the Meetings container to publish network meeting objects.</span></span>

<span data-ttu-id="ec3ea-116">具有多項產品的廠商可以使用類似的策略，將服務相關的物件群組至所有產品。</span><span class="sxs-lookup"><span data-stu-id="ec3ea-116">A vendor with multiple products can use a similar strategy to group service-related objects for all of its products.</span></span> <span data-ttu-id="ec3ea-117">在此情況下，您可以使用清楚識別廠商的名稱來建立 **容器** 物件;然後，將每個服務的 **容器** 物件建立為廠商容器的子系。</span><span class="sxs-lookup"><span data-stu-id="ec3ea-117">In this case, you could create a **container** object with a name that clearly identifies the vendor; then create **container** objects for each service as children of the vendor container.</span></span> <span data-ttu-id="ec3ea-118">建立廠商專屬的容器做為系統容器的子系。</span><span class="sxs-lookup"><span data-stu-id="ec3ea-118">Create the vendor-specific container as a child of the System container.</span></span>

 

 




