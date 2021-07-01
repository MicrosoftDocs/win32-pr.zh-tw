---
description: 對等
ms.assetid: a85fe46c-ce5f-4978-aa37-a3666560426b
title: 對等
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: ed371f203d34166f1d84462a363326adc32100ae
ms.sourcegitcommit: b32433cc0394159c7263809ae67615ab5792d40d
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 06/30/2021
ms.locfileid: "113118603"
---
# <a name="peer-to-peer"></a><span data-ttu-id="cbe2b-103">對等</span><span class="sxs-lookup"><span data-stu-id="cbe2b-103">Peer-to-Peer</span></span>

## <a name="purpose"></a><span data-ttu-id="cbe2b-104">目的</span><span class="sxs-lookup"><span data-stu-id="cbe2b-104">Purpose</span></span>

<span data-ttu-id="cbe2b-105">對等技術是用來協助跨分散式網路進行即時通訊和協同作業。</span><span class="sxs-lookup"><span data-stu-id="cbe2b-105">Peer-to-peer technologies are used to facilitate real-time communication and collaboration across distributed networks.</span></span>

<span data-ttu-id="cbe2b-106">在對等模型中，如果沒有使用網際網路伺服器，每位電腦使用者都可以執行下列動作：</span><span class="sxs-lookup"><span data-stu-id="cbe2b-106">In the peer-to-peer model, without using Internet servers, each PC user can do the following:</span></span>

-   <span data-ttu-id="cbe2b-107">Exchange 資料</span><span class="sxs-lookup"><span data-stu-id="cbe2b-107">Exchange data</span></span>
-   <span data-ttu-id="cbe2b-108">共用資源</span><span class="sxs-lookup"><span data-stu-id="cbe2b-108">Share resources</span></span>
-   <span data-ttu-id="cbe2b-109">尋找其他使用者</span><span class="sxs-lookup"><span data-stu-id="cbe2b-109">Locate other users</span></span>
-   <span data-ttu-id="cbe2b-110">通訊</span><span class="sxs-lookup"><span data-stu-id="cbe2b-110">Communicate</span></span>
-   <span data-ttu-id="cbe2b-111">即時共同作業</span><span class="sxs-lookup"><span data-stu-id="cbe2b-111">Collaborate directly in real time</span></span>

<span data-ttu-id="cbe2b-112">藉由使用點對點技術，協調電腦 CPU 週期和存放裝置使用的應用程式，可以在連線到網際網路的小型或大型電腦群組之間共用資源。</span><span class="sxs-lookup"><span data-stu-id="cbe2b-112">By using peer-to-peer technologies, applications that coordinate the use of computer CPU cycles and storage can share resources among small or large groups of computers connected to the Internet.</span></span>

## <a name="where-applicable"></a><span data-ttu-id="cbe2b-113">適用時</span><span class="sxs-lookup"><span data-stu-id="cbe2b-113">Where applicable</span></span>

<span data-ttu-id="cbe2b-114">開發人員可以使用對等基礎結構來建立各式各樣的分散式、臨機操作和點對點應用程式。</span><span class="sxs-lookup"><span data-stu-id="cbe2b-114">Developers can use the Peer Infrastructure to create a wide range of distributed, ad-hoc, and peer-to-peer applications.</span></span>

## <a name="developer-audience"></a><span data-ttu-id="cbe2b-115">開發人員對象</span><span class="sxs-lookup"><span data-stu-id="cbe2b-115">Developer audience</span></span>

<span data-ttu-id="cbe2b-116">使用對等基礎結構的開發人員應該熟悉 C 程式設計概念。</span><span class="sxs-lookup"><span data-stu-id="cbe2b-116">Developers using the Peer Infrastructure should be familiar with C programming concepts.</span></span> <span data-ttu-id="cbe2b-117">使用 PNRP Winsock 命名空間提供者的開發人員應該熟悉 Winsock API。</span><span class="sxs-lookup"><span data-stu-id="cbe2b-117">Developers using the PNRP Winsock Namespace Provider should be familiar with the Winsock API.</span></span>

## <a name="run-time-requirements"></a><span data-ttu-id="cbe2b-118">執行階段需求求</span><span class="sxs-lookup"><span data-stu-id="cbe2b-118">Run-time requirements</span></span>

<span data-ttu-id="cbe2b-119">Windows Vista、Windows XP Service Pack 2 (SP2) 和更新版本，以及適用于 windows xp 的 Advanced 網路套件（適用于 windows xp Service Pack 1 (SP1) ）也支援對等基礎結構。</span><span class="sxs-lookup"><span data-stu-id="cbe2b-119">The Peer Infrastructure is supported in Windows Vista, Windows XP with Service Pack 2 (SP2) and later as well the Advanced Networking Pack for Windows XP available for Windows XP with Service Pack 1 (SP1).</span></span> <span data-ttu-id="cbe2b-120">對等基礎結構需要安裝並起始 IPv6，才能讓對等網路應用程式運作。</span><span class="sxs-lookup"><span data-stu-id="cbe2b-120">The Peer-to-Peer Infrastructure requires that IPv6 be installed and initiated to allow peer networking applications to function.</span></span> <span data-ttu-id="cbe2b-121">只有在 Windows Vista 中才支援使用對等共同作業。</span><span class="sxs-lookup"><span data-stu-id="cbe2b-121">Use of Peer-to-Peer Collaboration is only supported in Windows Vista .</span></span>

## <a name="in-this-section"></a><span data-ttu-id="cbe2b-122">本節內容</span><span class="sxs-lookup"><span data-stu-id="cbe2b-122">In this section</span></span>



| <span data-ttu-id="cbe2b-123">主題</span><span class="sxs-lookup"><span data-stu-id="cbe2b-123">Topic</span></span>                                                     | <span data-ttu-id="cbe2b-124">描述</span><span class="sxs-lookup"><span data-stu-id="cbe2b-124">Description</span></span>                                                                                         |
|-----------------------------------------------------------|-----------------------------------------------------------------------------------------------------|
| [<span data-ttu-id="cbe2b-125">對等基礎結構</span><span class="sxs-lookup"><span data-stu-id="cbe2b-125">Peer Infrastructure</span></span>](peer-infrastructure.md)<br/> | <span data-ttu-id="cbe2b-126">對等基礎結構和對等名稱解析通訊協定的相關資訊 (PNRP) 。</span><span class="sxs-lookup"><span data-stu-id="cbe2b-126">Information about the Peer Infrastructure and the Peer Name Resolution Protocol (PNRP).</span></span> <br/> |
| [<span data-ttu-id="cbe2b-127">對等共同作業</span><span class="sxs-lookup"><span data-stu-id="cbe2b-127">Peer Collaboration</span></span>](peer-collaboration.md)<br/>   | <span data-ttu-id="cbe2b-128">對等共同作業 API 特定的資訊和參考資料。</span><span class="sxs-lookup"><span data-stu-id="cbe2b-128">Information and reference material specific to the Peer Collaboration API.</span></span><br/>               |
| [<span data-ttu-id="cbe2b-129">對等分佈</span><span class="sxs-lookup"><span data-stu-id="cbe2b-129">Peer Distribution</span></span>](peer-distribution.md)<br/>     | <span data-ttu-id="cbe2b-130">對等散發 API 的特定資訊和參考資料。</span><span class="sxs-lookup"><span data-stu-id="cbe2b-130">Information and reference material specific to the Peer Distribution API.</span></span><br/>                |



 

## <a name="additional-resources"></a><span data-ttu-id="cbe2b-131">其他資源</span><span class="sxs-lookup"><span data-stu-id="cbe2b-131">Additional resources</span></span>

<span data-ttu-id="cbe2b-132">您可以在下列位置找到有關點對點技術的進一步資訊：</span><span class="sxs-lookup"><span data-stu-id="cbe2b-132">Further information regarding Peer-to-Peer technologies can be found at the following locations:</span></span>

| <span data-ttu-id="cbe2b-133">主題</span><span class="sxs-lookup"><span data-stu-id="cbe2b-133">Topic</span></span>                                                                                                          | <span data-ttu-id="cbe2b-134">描述</span><span class="sxs-lookup"><span data-stu-id="cbe2b-134">Description</span></span>                                                                                                               |
|-----------------------------------------------------------------------------------------------------------|----------------------------------------------------------------------------------------------------------------|
| [<span data-ttu-id="cbe2b-135">Windows 對等網路資源</span><span class="sxs-lookup"><span data-stu-id="cbe2b-135">Windows Peer Networking Resources</span></span>](https://www.microsoft.com/p2p)                       | <span data-ttu-id="cbe2b-136">存取已發佈的白皮書、範例和簡報，詳述對等網路技術。</span><span class="sxs-lookup"><span data-stu-id="cbe2b-136">Access published white-papers, samples, and presentations detailing the Peer Networking technology.</span></span><br/> |
| [<span data-ttu-id="cbe2b-137">Microsoft 對等網路的 Blog</span><span class="sxs-lookup"><span data-stu-id="cbe2b-137">Microsoft Peer Networking Blog</span></span>](/archive/blogs/p2p/)                          | <span data-ttu-id="cbe2b-138">閱讀來自 Microsoft 對等網路團隊的最新 blog 專案。</span><span class="sxs-lookup"><span data-stu-id="cbe2b-138">Read the latest blog entries from Microsoft's Peer Networking Team.</span></span><br/>                                 |
| [<span data-ttu-id="cbe2b-139">MSDN 對等網路論壇</span><span class="sxs-lookup"><span data-stu-id="cbe2b-139">MSDN Peer Networking Forum</span></span>](https://social.msdn.microsoft.com/forums/peertopeer/threads/)                              | <span data-ttu-id="cbe2b-140">討論對等技術，並與其他開發人員共同作業。</span><span class="sxs-lookup"><span data-stu-id="cbe2b-140">Discuss Peer technologies and collaborate with other developers.</span></span><br/>                                    |
| [<span data-ttu-id="cbe2b-141">適用于 IT 專業人員的 TechNet 對等網路資源</span><span class="sxs-lookup"><span data-stu-id="cbe2b-141">TechNet Peer Networking Resources for IT Professionals</span></span>](https://technet.microsoft.com/library/bb742623.aspx) | <span data-ttu-id="cbe2b-142">IT 專業人員角色特有的概念對等網路總覽和指引。</span><span class="sxs-lookup"><span data-stu-id="cbe2b-142">A conceptual Peer Networking overview, as well as guidance, specific to the IT Professional role.</span></span> <br/>  |



 

 

