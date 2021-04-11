---
description: COMREPL 是一個公用程式，它會將指定來源電腦的 COM + 類別目錄複寫到一或多部目的電腦。
ms.assetid: 11aa7603-61f1-4af0-b6f9-81f484788052
title: COMREPL 複製公用程式
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: a08ecd77a679b6fc150e7a91fc0214eb829792dd
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/07/2021
ms.locfileid: "103936439"
---
# <a name="the-comrepl-replication-utility"></a><span data-ttu-id="afd1a-103">COMREPL 複製公用程式</span><span class="sxs-lookup"><span data-stu-id="afd1a-103">The COMREPL Replication Utility</span></span>

<span data-ttu-id="afd1a-104">COMREPL 是一個公用程式，它會將指定來源電腦的 COM + 類別目錄複寫到一或多部目的電腦。</span><span class="sxs-lookup"><span data-stu-id="afd1a-104">COMREPL is a utility that will replicate the COM+ catalog from a given source computer to one or more target computers.</span></span> <span data-ttu-id="afd1a-105">請考慮代表「主要設定」的來源電腦。</span><span class="sxs-lookup"><span data-stu-id="afd1a-105">Think of the source computer representing a "master configuration."</span></span> <span data-ttu-id="afd1a-106">COMREPL 用來複寫此主要設定，以維護一組設定相同的電腦。</span><span class="sxs-lookup"><span data-stu-id="afd1a-106">COMREPL is used to replicate this master configuration to maintain a set of identically configured computers.</span></span>

<span data-ttu-id="afd1a-107">複寫的單位是主要電腦上的整個 COM + 設定。</span><span class="sxs-lookup"><span data-stu-id="afd1a-107">The unit of replication is the entire COM+ configuration on the master computer.</span></span> <span data-ttu-id="afd1a-108">主要複本上的所有 COM + 應用程式都會複寫到目的電腦;全部或沒有東西。</span><span class="sxs-lookup"><span data-stu-id="afd1a-108">All COM+ applications on the master are replicated to the target computers; it's all or nothing.</span></span> <span data-ttu-id="afd1a-109">此外，先前安裝在目的電腦上的所有 COM + 應用程式（COM + 預先安裝的應用程式除外）將會在複寫過程中刪除。</span><span class="sxs-lookup"><span data-stu-id="afd1a-109">In addition, all COM+ applications previously installed on the target computers, with the exception of the COM+ preinstalled applications, will be deleted as part of the replication process.</span></span>

<span data-ttu-id="afd1a-110">COMREPL 只會複寫 COM + 設定資料。</span><span class="sxs-lookup"><span data-stu-id="afd1a-110">COMREPL replicates only COM+ configuration data.</span></span> <span data-ttu-id="afd1a-111">這包括 COM + 應用程式和 COM + 特定電腦設定。</span><span class="sxs-lookup"><span data-stu-id="afd1a-111">This includes COM+ applications and COM+ specific computer settings.</span></span> <span data-ttu-id="afd1a-112">Microsoft Internet Information Services (IIS) 都有類似的公用程式 (IISSync) ，這會使用 COMREPL 來複寫 IIS 和 COM + 設定。</span><span class="sxs-lookup"><span data-stu-id="afd1a-112">Microsoft Internet Information Services (IIS) has a similar utility (IISSync), which makes use of COMREPL to replicate IIS and COM+ configuration.</span></span>

<span data-ttu-id="afd1a-113">如需啟動和使用 COMREPL 的詳細資訊，請參閱本節中的下列主題：</span><span class="sxs-lookup"><span data-stu-id="afd1a-113">For detailed information on launching and using COMREPL, see the following topics in this section:</span></span>

-   [<span data-ttu-id="afd1a-114">使用 COMREPL</span><span class="sxs-lookup"><span data-stu-id="afd1a-114">Using COMREPL</span></span>](using-comrepl.md)
-   [<span data-ttu-id="afd1a-115">複寫的內容</span><span class="sxs-lookup"><span data-stu-id="afd1a-115">What Gets Replicated</span></span>](what-gets-replicated.md)
-   [<span data-ttu-id="afd1a-116">複寫階段</span><span class="sxs-lookup"><span data-stu-id="afd1a-116">Replication Phases</span></span>](replication-phases.md)
-   [<span data-ttu-id="afd1a-117">檔案管理</span><span class="sxs-lookup"><span data-stu-id="afd1a-117">File Management</span></span>](file-management.md)
-   [<span data-ttu-id="afd1a-118">記錄和錯誤報表</span><span class="sxs-lookup"><span data-stu-id="afd1a-118">Logging and Error Reporting</span></span>](logging-and-error-reporting.md)

## <a name="related-topics"></a><span data-ttu-id="afd1a-119">相關主題</span><span class="sxs-lookup"><span data-stu-id="afd1a-119">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="afd1a-120">建立 COM + 應用程式的安裝套件</span><span class="sxs-lookup"><span data-stu-id="afd1a-120">Creating Installation Packages for COM+ Applications</span></span>](creating-installation-packages-for-com--applications.md)
</dt> <dt>

[<span data-ttu-id="afd1a-121">部署應用程式 proxy</span><span class="sxs-lookup"><span data-stu-id="afd1a-121">Deploying Application Proxies</span></span>](deploying-application-proxies.md)
</dt> <dt>

[<span data-ttu-id="afd1a-122">COM + 類別目錄</span><span class="sxs-lookup"><span data-stu-id="afd1a-122">The COM+ Catalog</span></span>](the-com--catalog.md)
</dt> </dl>

 

 



