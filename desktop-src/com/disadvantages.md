---
title: 缺點
description: 缺點
ms.assetid: ce6885d9-7056-42bc-85d1-27ce32b1be5e
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 7a22e409414a1df60e2dd9dff3adbfc6000b953a
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 09/16/2019
ms.locfileid: "104507393"
---
# <a name="disadvantages"></a><span data-ttu-id="bdc46-103">缺點</span><span class="sxs-lookup"><span data-stu-id="bdc46-103">Disadvantages</span></span>

<span data-ttu-id="bdc46-104">同進程伺服器使用本機伺服器的編輯功能，提供物件處理常式的速度和大小優勢。</span><span class="sxs-lookup"><span data-stu-id="bdc46-104">In-process servers provide the speed and size advantage of an object handler with the editing capability of a local server.</span></span> <span data-ttu-id="bdc46-105">那麼，為什麼您會選擇將您的 OLE 應用程式實作為本機伺服器，而不是同進程伺服器？</span><span class="sxs-lookup"><span data-stu-id="bdc46-105">So why would you ever choose to implement your OLE application as a local server rather than an in-process server?</span></span> <span data-ttu-id="bdc46-106">有幾個原因：</span><span class="sxs-lookup"><span data-stu-id="bdc46-106">There are several reasons:</span></span>

-   <span data-ttu-id="bdc46-107">安全性。</span><span class="sxs-lookup"><span data-stu-id="bdc46-107">Security.</span></span> <span data-ttu-id="bdc46-108">只有本機伺服器的位址空間與用戶端隔離。</span><span class="sxs-lookup"><span data-stu-id="bdc46-108">Only a local server has its address space isolated from that of the client.</span></span> <span data-ttu-id="bdc46-109">同進程伺服器會共用用戶端的位址空間和處理內容，因此在發生錯誤或惡意程式設計時可能較不穩定。</span><span class="sxs-lookup"><span data-stu-id="bdc46-109">An in-process server shares the address space and process context of the client and can therefore be less robust in the face of faults or malicious programming.</span></span>
-   <span data-ttu-id="bdc46-110">粒 度。</span><span class="sxs-lookup"><span data-stu-id="bdc46-110">Granularity.</span></span> <span data-ttu-id="bdc46-111">本機伺服器可以在許多不同的用戶端上裝載其物件的多個實例，在多個用戶端中的物件之間共用伺服器狀態的方式，可能是實作為同進程伺服器，而這只是載入至每個用戶端的 DLL。</span><span class="sxs-lookup"><span data-stu-id="bdc46-111">A local server can host multiple instances of its object across many different clients, sharing server state between objects in multiple clients in ways that would be difficult or impossible if implemented as an in-process server, which is simply a DLL loaded into each client.</span></span>
-   <span data-ttu-id="bdc46-112">相容性。</span><span class="sxs-lookup"><span data-stu-id="bdc46-112">Compatibility.</span></span> <span data-ttu-id="bdc46-113">如果您選擇執行同進程伺服器，就會放棄不支援這類伺服器的 OLE 1 相容性。</span><span class="sxs-lookup"><span data-stu-id="bdc46-113">If you choose to implement an in-process server, you relinquish compatibility with OLE 1, which does not support such servers.</span></span> <span data-ttu-id="bdc46-114">這並不是許多開發人員的考慮，但如果是，則是重要的考慮。</span><span class="sxs-lookup"><span data-stu-id="bdc46-114">This will not be a consideration for many developers, but if it is, then it is of critical concern.</span></span>
-   <span data-ttu-id="bdc46-115">無法支援連結。</span><span class="sxs-lookup"><span data-stu-id="bdc46-115">Inability to support links.</span></span> <span data-ttu-id="bdc46-116">同進程伺服器不能作為連結來源。</span><span class="sxs-lookup"><span data-stu-id="bdc46-116">An in-process server cannot serve as a link source.</span></span> <span data-ttu-id="bdc46-117">因為 DLL 無法自行執行，所以無法建立要連結的檔案物件。</span><span class="sxs-lookup"><span data-stu-id="bdc46-117">Since a DLL cannot run by itself, it cannot create a file object to be linked to.</span></span>

<span data-ttu-id="bdc46-118">儘管有這些缺點，同進程伺服器可能是其速度和大小的絕佳選擇，如果符合您的所有其他需求。</span><span class="sxs-lookup"><span data-stu-id="bdc46-118">Despite these disadvantages, an in-process server can be an excellent choice for its speed and size — if it fits all your other requirements.</span></span>

## <a name="related-topics"></a><span data-ttu-id="bdc46-119">相關主題</span><span class="sxs-lookup"><span data-stu-id="bdc46-119">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="bdc46-120">優點</span><span class="sxs-lookup"><span data-stu-id="bdc46-120">Advantages</span></span>](advantages.md)
</dt> <dt>

[<span data-ttu-id="bdc46-121">同進程伺服器</span><span class="sxs-lookup"><span data-stu-id="bdc46-121">In-Process Servers</span></span>](in-process-servers.md)
</dt> </dl>

 

 




