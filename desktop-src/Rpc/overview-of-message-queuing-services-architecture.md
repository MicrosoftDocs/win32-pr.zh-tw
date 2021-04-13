---
title: 訊息佇列服務架構總覽
description: 訊息佇列服務 (MSMQ) 使用網站/企業模型。 一般而言，網站是實體位置，例如建築物。 企業包含一或多個網站，並代表一個組織。
ms.assetid: f5c54c58-8ec5-49b7-a184-aed9a8100960
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: f2226c185d32cb628529b34ba33d5569bd51ac28
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 09/16/2019
ms.locfileid: "104301563"
---
# <a name="overview-of-message-queuing-services-architecture"></a><span data-ttu-id="b1abf-105">訊息佇列服務架構總覽</span><span class="sxs-lookup"><span data-stu-id="b1abf-105">Overview of Message Queuing Services Architecture</span></span>

<span data-ttu-id="b1abf-106">訊息佇列服務 (MSMQ) 使用網站/企業模型。</span><span class="sxs-lookup"><span data-stu-id="b1abf-106">Message Queuing Services (MSMQ) uses a site/enterprise model.</span></span> <span data-ttu-id="b1abf-107">一般而言，網站是實體位置，例如建築物。</span><span class="sxs-lookup"><span data-stu-id="b1abf-107">Typically, a site is a physical location, such as a building.</span></span> <span data-ttu-id="b1abf-108">企業包含一或多個網站，並代表一個組織。</span><span class="sxs-lookup"><span data-stu-id="b1abf-108">An enterprise consists of one or more sites and represents an organization.</span></span>

<span data-ttu-id="b1abf-109">下圖說明 MSMQ 服務的架構。</span><span class="sxs-lookup"><span data-stu-id="b1abf-109">The following diagram illustrates the architecture of the MSMQ Service.</span></span>

![msmq 架構](images/msmq.png)

<span data-ttu-id="b1abf-111">MSMQ 的核心是訊息佇列資訊服務 (MQIS) 資料庫，這會在 SQL Server 上執行。</span><span class="sxs-lookup"><span data-stu-id="b1abf-111">At the heart of MSMQ is the Message Queue Information Service (MQIS) database, which runs on top of SQL Server.</span></span> <span data-ttu-id="b1abf-112">企業有單一的主要 MQIS，稱為「主要企業控制器」。</span><span class="sxs-lookup"><span data-stu-id="b1abf-112">An enterprise has a single master MQIS, called the Primary Enterprise Controller.</span></span> <span data-ttu-id="b1abf-113">每個網站都有自己的 MQIS，稱為 *主要網站控制器* 以及零或多個 *備份網站控制器*。</span><span class="sxs-lookup"><span data-stu-id="b1abf-113">Each site has its own MQIS, called a *primary site controller* and zero or more *backup site controllers*.</span></span> <span data-ttu-id="b1abf-114">最後，有個別的用戶端電腦，每個電腦都有自己的佇列管理員，並以服務的形式執行。</span><span class="sxs-lookup"><span data-stu-id="b1abf-114">Finally, there are the individual client computers, each of which has its own queue manager, implemented as a service.</span></span> <span data-ttu-id="b1abf-115">主要企業控制器也可以是主要網站控制器，而且任何控制器也可以是用戶端。</span><span class="sxs-lookup"><span data-stu-id="b1abf-115">The Primary Enterprise Controller can also be a Primary Site Controller, and any controller can also be a client.</span></span>

<span data-ttu-id="b1abf-116">訊息佇列可以是公用或私用。</span><span class="sxs-lookup"><span data-stu-id="b1abf-116">Message queues can be either public or private.</span></span> <span data-ttu-id="b1abf-117">公用佇列會在 Active Directory 中註冊，並可在網路上存取。</span><span class="sxs-lookup"><span data-stu-id="b1abf-117">Public queues are registered in Active Directory and are accessible across the network.</span></span> <span data-ttu-id="b1abf-118">公用佇列中的訊息會路由傳送到整個企業，在 MSMQ 的控制之下。</span><span class="sxs-lookup"><span data-stu-id="b1abf-118">Messages in a public queue are routed throughout the enterprise, under the control of MSMQ.</span></span> <span data-ttu-id="b1abf-119">用戶端應用程式訊息會在網站控制器的佇列管理員之間移動，以從用戶端的佇列管理員移至目的地佇列。</span><span class="sxs-lookup"><span data-stu-id="b1abf-119">Client application messages move from the client's queue manager to the destination queue by traveling between the queue managers of the site controllers.</span></span>

<span data-ttu-id="b1abf-120">私用佇列是由本機佇列管理員維護，而且不會在 Active Directory 中註冊。</span><span class="sxs-lookup"><span data-stu-id="b1abf-120">Private queues are maintained by the local queue manager and are not registered in Active Directory.</span></span> <span data-ttu-id="b1abf-121">私用佇列訊息的範圍僅限於它們所在的電腦。</span><span class="sxs-lookup"><span data-stu-id="b1abf-121">The scope of private queue messages is limited to the computer on which they reside.</span></span>

 

 




