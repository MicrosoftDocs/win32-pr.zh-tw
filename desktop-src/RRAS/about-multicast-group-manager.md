---
title: 關於多播群組管理員
description: 本檔說明多播群組管理員 (MGM) 技術。
ms.assetid: 55216742-d67c-4a17-aaf9-0b087938061e
keywords:
- 多播群組管理員 RRAS
- 多播群組管理員 RRAS，說明
- 路由及遠端存取服務 RRAS、多播群組管理員
- 路由及遠端存取服務 RRAS，多播群組管理員，描述
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 034d37b99aaa9ca0139b5425cd5b85e7b3f280e9
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 09/16/2019
ms.locfileid: "106965800"
---
# <a name="about-multicast-group-manager"></a><span data-ttu-id="3bdcf-107">關於多播群組管理員</span><span class="sxs-lookup"><span data-stu-id="3bdcf-107">About Multicast Group Manager</span></span>

<span data-ttu-id="3bdcf-108">本檔說明多播群組管理員 (MGM) 技術。</span><span class="sxs-lookup"><span data-stu-id="3bdcf-108">This documentation describes the Multicast Group Manager (MGM) technology.</span></span>

<span data-ttu-id="3bdcf-109">多播可讓主機只將資料傳送到特別要求接收資料的目的地。</span><span class="sxs-lookup"><span data-stu-id="3bdcf-109">Multicasting allows a host to send data to only those destinations that specifically request to receive the data.</span></span> <span data-ttu-id="3bdcf-110">如此一來，多播與傳送廣播資料不同，因為廣播資料會傳送至所有主機。</span><span class="sxs-lookup"><span data-stu-id="3bdcf-110">In this way, multicasting differs from sending broadcast data, since broadcast data is sent to all hosts.</span></span>

<span data-ttu-id="3bdcf-111">多播會節省網路頻寬，因為多播資料只會由要求資料的主機接收，而資料只會透過任何連結傳送一次。</span><span class="sxs-lookup"><span data-stu-id="3bdcf-111">Multicasting saves network bandwidth because multicast data is only received by those hosts that request the data, and the data travels over any link only once.</span></span> <span data-ttu-id="3bdcf-112">多播會儲存伺服器頻寬，因為伺服器必須每個網路只傳送一個多播訊息，而不是每個接收者一個單播訊息。</span><span class="sxs-lookup"><span data-stu-id="3bdcf-112">Multicasting saves server bandwidth because a server has to send only one multicast message per network instead of one unicast message per receiver.</span></span> <span data-ttu-id="3bdcf-113">常用的多播應用程式範例包括線上會議和網際網路廣播。</span><span class="sxs-lookup"><span data-stu-id="3bdcf-113">Examples of popular multicast applications are online meetings and Internet radio.</span></span>

<span data-ttu-id="3bdcf-114">MGM API 可讓開發人員撰寫多播路由通訊協定，以便與執行多播群組管理員的路由器相交互操作。</span><span class="sxs-lookup"><span data-stu-id="3bdcf-114">The MGM API enables developers to write multicast routing protocols that interoperate with routers running the multicast group manager.</span></span>

<span data-ttu-id="3bdcf-115">在路由器上啟用一個以上的多播路由通訊協定時，多播群組管理員會協調所有路由通訊協定之間的作業。</span><span class="sxs-lookup"><span data-stu-id="3bdcf-115">When more than one multicast routing protocol is enabled on a router, the multicast group manager coordinates operations between all routing protocols.</span></span> <span data-ttu-id="3bdcf-116">多播群組管理員會在群組成員資格變更時，以及當收到來自新來源或目的地為新群組的多播資料時，通知每個路由通訊協定。</span><span class="sxs-lookup"><span data-stu-id="3bdcf-116">The multicast group manager informs each routing protocol when group membership changes occur, and when multicast data from a new source or destined to a new group is received.</span></span>

<span data-ttu-id="3bdcf-117">MGM API 提供下列功能：</span><span class="sxs-lookup"><span data-stu-id="3bdcf-117">The MGM API provides the following features:</span></span>

-   <span data-ttu-id="3bdcf-118">通訊協定註冊</span><span class="sxs-lookup"><span data-stu-id="3bdcf-118">Protocol registration</span></span>
-   <span data-ttu-id="3bdcf-119">群組管理</span><span class="sxs-lookup"><span data-stu-id="3bdcf-119">Group management</span></span>
-   <span data-ttu-id="3bdcf-120">多播轉送專案 (MFE) 列舉</span><span class="sxs-lookup"><span data-stu-id="3bdcf-120">Multicast forwarding entry (MFE) enumeration</span></span>
-   <span data-ttu-id="3bdcf-121">多播路由通訊協定的回呼定義</span><span class="sxs-lookup"><span data-stu-id="3bdcf-121">Callback definitions for multicast routing protocols</span></span>

<span data-ttu-id="3bdcf-122">本總覽說明多播架構的元件、用來與多播群組管理員交互操作的用戶端案例，以及使用 MGM API 的程式設計考慮。</span><span class="sxs-lookup"><span data-stu-id="3bdcf-122">This overview describes the components of the multicast architecture, the client scenarios that are used to interoperate with the multicast group manager, and programming considerations for using the MGM API.</span></span>

 

 




