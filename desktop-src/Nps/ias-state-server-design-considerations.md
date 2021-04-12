---
title: 狀態伺服器設計考慮
description: 視您的設計而定，您可能需要伺服器來追蹤目前登入網路的使用者。
ms.assetid: 2f8d268b-5518-4ad2-aed6-5971c913db6d
ms.tgt_platform: multiple
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 7a0ef654f3641138075acc667d733b20c94c4840
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 09/16/2019
ms.locfileid: "104372428"
---
# <a name="state-server-design-considerations"></a><span data-ttu-id="c2f8a-103">狀態伺服器設計考慮</span><span class="sxs-lookup"><span data-stu-id="c2f8a-103">State Server Design Considerations</span></span>

> [!Note]  
> <span data-ttu-id="c2f8a-104">從 Windows Server 2008 開始， (IAS) 的網際網路驗證服務已重新命名為網路原則伺服器 (NPS) 。</span><span class="sxs-lookup"><span data-stu-id="c2f8a-104">Internet Authentication Service (IAS) was renamed Network Policy Server (NPS) starting with Windows Server 2008.</span></span> <span data-ttu-id="c2f8a-105">本主題的內容適用于 IAS 和 NPS。</span><span class="sxs-lookup"><span data-stu-id="c2f8a-105">The content of this topic applies to both IAS and NPS.</span></span> <span data-ttu-id="c2f8a-106">在整個文字中，NPS 是用來參考服務的所有版本，包括原本稱為 IAS 的版本。</span><span class="sxs-lookup"><span data-stu-id="c2f8a-106">Throughout the text, NPS is used to refer to all versions of the service, including the versions originally referred to as IAS.</span></span>

 

<span data-ttu-id="c2f8a-107">視您的設計而定，您可能需要伺服器來追蹤目前登入網路的使用者。</span><span class="sxs-lookup"><span data-stu-id="c2f8a-107">Depending on your design, you may need a server to track the users that are currently logged onto the network.</span></span> <span data-ttu-id="c2f8a-108">狀態伺服器的主要挑戰是讓狀態伺服器資料庫中的資訊與實際登入的使用者保持同步。</span><span class="sxs-lookup"><span data-stu-id="c2f8a-108">The main challenge with the state server is keeping the information in the state server database in-sync with who is actually logged on.</span></span> <span data-ttu-id="c2f8a-109">如果狀態伺服器中的資訊不同步，當使用者未獲授權時，使用者可能會成功擁有多個會話。</span><span class="sxs-lookup"><span data-stu-id="c2f8a-109">If the information in the state server is out of sync, users may succeed in having multiple sessions when they aren't authorized to do so.</span></span> <span data-ttu-id="c2f8a-110">此外，沒有多個會話的使用者可能不小心懲罰。</span><span class="sxs-lookup"><span data-stu-id="c2f8a-110">Also, users who do not have multiple sessions could be inadvertently penalized.</span></span>

<span data-ttu-id="c2f8a-111">在執行狀態伺服器時，應考慮下列事項：</span><span class="sxs-lookup"><span data-stu-id="c2f8a-111">The following should be taken into consideration in implementing the state server:</span></span>

-   <span data-ttu-id="c2f8a-112">狀態伺服器必須在幾秒鐘內讓決策上線。</span><span class="sxs-lookup"><span data-stu-id="c2f8a-112">The state server must make the decision online in a few seconds.</span></span> <span data-ttu-id="c2f8a-113">基於這個理由，狀態伺服器需要可擴充的基礎結構，每秒可支援許多更新和查詢。</span><span class="sxs-lookup"><span data-stu-id="c2f8a-113">For this reason the state server requires a scaleable infrastructure that can support many updates and queries per second.</span></span> <span data-ttu-id="c2f8a-114">關係資料庫不適合同時更新的大型查詢。</span><span class="sxs-lookup"><span data-stu-id="c2f8a-114">Relational databases are not appropriate for such large queries with simultaneous updates.</span></span> <span data-ttu-id="c2f8a-115">關係資料庫主要是為了保持資料一致，並為所有取用者提供一致的資料檢視。</span><span class="sxs-lookup"><span data-stu-id="c2f8a-115">Relational databases are primarily built to keep data consistent and to provide a consistent view of the data to all consumers.</span></span> <span data-ttu-id="c2f8a-116">它們並不是為了快速更新所建立。</span><span class="sxs-lookup"><span data-stu-id="c2f8a-116">They are not built for quick updates.</span></span>
-   <span data-ttu-id="c2f8a-117">多個物件之間的更新交易一致性並不重要。</span><span class="sxs-lookup"><span data-stu-id="c2f8a-117">Transactional consistency on updates between multiple objects is not important.</span></span> <span data-ttu-id="c2f8a-118">這是因為狀態伺服器可容忍很小的商機視窗。</span><span class="sxs-lookup"><span data-stu-id="c2f8a-118">This is because the state server can tolerate a small window of opportunity.</span></span> <span data-ttu-id="c2f8a-119">但是，如果其中一部 RADIUS 伺服器在更新過程中關閉，則單一更新的交易一致性很重要，可減少狀態伺服器處於不一致狀態的機會。</span><span class="sxs-lookup"><span data-stu-id="c2f8a-119">However, transactional consistency of a single update is important to reduce the chances of leaving the state server in an inconsistent state if one of the RADIUS servers is shut down in the middle of the update.</span></span>
-   <span data-ttu-id="c2f8a-120">持續性 (將網路的狀態儲存至持續性儲存體) 不重要，因為持續性資訊很快就會與網路的實際狀態進行同步處理。</span><span class="sxs-lookup"><span data-stu-id="c2f8a-120">Persistence (saving the state of the network to persistent storage) is not important because the persistent information will quickly fall out of sync with the actual state of the network.</span></span>
-   <span data-ttu-id="c2f8a-121">如果網路上支援 ISDN 或其他形式的多重連結，則狀態伺服器應該能夠處理使用這些功能的案例。</span><span class="sxs-lookup"><span data-stu-id="c2f8a-121">If ISDN or other forms of multilink are supported on the network, the state server should be able to handle scenarios that use these features.</span></span>

<span data-ttu-id="c2f8a-122">其中一個可能的設計是同時執行驗證延伸模組 DLL 和授權延伸 DLL。</span><span class="sxs-lookup"><span data-stu-id="c2f8a-122">One possible design is to implement both an Authentication Extension DLL and an Authorization Extension DLL.</span></span> <span data-ttu-id="c2f8a-123">這些 Dll 都可以透過網路與資料庫進行通訊。</span><span class="sxs-lookup"><span data-stu-id="c2f8a-123">Each of these DLLs can communicate over the network with a database.</span></span> <span data-ttu-id="c2f8a-124">授權延伸模組 DLL 可以使用目前登入網路的相關資訊來更新資料庫。</span><span class="sxs-lookup"><span data-stu-id="c2f8a-124">The Authorization Extension DLL can update the database with information about who is currently logged onto the network.</span></span> <span data-ttu-id="c2f8a-125">驗證延伸模組 DLL 可以查詢資料庫以取得這項資訊，以決定是要接受還是拒絕特定使用者的驗證要求;如果使用者已登入，則會拒絕要求。</span><span class="sxs-lookup"><span data-stu-id="c2f8a-125">The Authentication Extension DLL can query the database for this information to decide whether to accept or reject a particular user's authentication request; if the user is already logged on, the request is rejected.</span></span>

<span data-ttu-id="c2f8a-126">讓授權延伸模組 DLL 更新狀態伺服器資料庫的優點是，授權延伸模組 DLL 可以存取已驗證使用者的詳細資訊。</span><span class="sxs-lookup"><span data-stu-id="c2f8a-126">The advantage of having the Authorization Extension DLL update the state-server database is that the Authorization Extension DLL has access to more information about the authenticated user.</span></span> <span data-ttu-id="c2f8a-127">授權延伸模組 DLL 可從 NPS 授權機制存取所有的授權屬性。</span><span class="sxs-lookup"><span data-stu-id="c2f8a-127">The Authorization Extension DLL has access to all of the authorization attributes from the NPS Authorization mechanism.</span></span> <span data-ttu-id="c2f8a-128">例如，有些使用者可能會有允許他們有多個會話的授權。</span><span class="sxs-lookup"><span data-stu-id="c2f8a-128">For example, some users may have authorizations that allow them to have multiple sessions.</span></span> <span data-ttu-id="c2f8a-129">狀態伺服器應該將這類使用者視為特殊案例。</span><span class="sxs-lookup"><span data-stu-id="c2f8a-129">The state server should treat such users as a special case.</span></span>

 

 




