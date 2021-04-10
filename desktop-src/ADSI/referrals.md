---
title: ADSI)  (的參考
description: 當您所查詢的伺服器未包含該資料，但可以找到該資料時，就會發生參考。
ms.assetid: 2068ce7a-0b94-4d25-a18f-97f26863bd1d
ms.tgt_platform: multiple
keywords:
- 參考 ADSI
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: e79e6b2e8a737f6bb40386effd68f7f31d8d490d
ms.sourcegitcommit: b0ebdefc3dcd5c04bede94091833aa1015a2f95c
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/21/2020
ms.locfileid: "104093288"
---
# <a name="referrals-adsi"></a><span data-ttu-id="d6a04-104">ADSI)  (的參考</span><span class="sxs-lookup"><span data-stu-id="d6a04-104">Referrals (ADSI)</span></span>

<span data-ttu-id="d6a04-105">當您所查詢的伺服器未包含該資料，但可以找到該資料時，就會發生參考。</span><span class="sxs-lookup"><span data-stu-id="d6a04-105">Referrals occur when the server you are querying does not contain that data, but can find it.</span></span> <span data-ttu-id="d6a04-106">目標伺服器會傳回結果集，其中可能包含實際資料，以及另一部伺服器的參考，以抓取額外的資料。</span><span class="sxs-lookup"><span data-stu-id="d6a04-106">The target server returns the result set, which may include both the actual data and a referral to another server to retrieve the additional data.</span></span> <span data-ttu-id="d6a04-107">藉由啟用 *參考追蹤*，基礎 ADSI 用戶端程式代碼將會使用該參考資料來嘗試從參考資料中所描述的伺服器取得目標物件。</span><span class="sxs-lookup"><span data-stu-id="d6a04-107">By enabling *referral chasing*, the underlying ADSI client code will use that referral data to attempt to retrieve the target object from the server described in the referral data.</span></span> <span data-ttu-id="d6a04-108">請注意，停用的參考追蹤可能會產生較小的結果集，而啟用參考追蹤可能會導致查詢跨越許多伺服器。</span><span class="sxs-lookup"><span data-stu-id="d6a04-108">Be aware that the disabling referral chasing may result in a smaller result set, whereas enabling referral chasing may cause a query to span many servers.</span></span> <span data-ttu-id="d6a04-109">可能的話，建議的解決方案是使用通用類別目錄。</span><span class="sxs-lookup"><span data-stu-id="d6a04-109">When possible, the recommended solution is to use the global catalog.</span></span>

<span data-ttu-id="d6a04-110">如需 Active Directory 中的參考和參考追蹤的詳細資訊，請參閱 [參考](/windows/desktop/AD/referrals)。</span><span class="sxs-lookup"><span data-stu-id="d6a04-110">For more information about referrals and referral chasing in Active Directory, see [Referrals](/windows/desktop/AD/referrals).</span></span>

<span data-ttu-id="d6a04-111">例如，當用戶端指示伺服器 A () 來查詢使用者物件 (U) 時，可以建議用戶端在伺服器 B 上繼續搜尋 (B) 如果 U 不是位於，但已知是在 B 上。用戶端可以選擇尋求參考。</span><span class="sxs-lookup"><span data-stu-id="d6a04-111">For example, when a client instructs Server A (A) to query a user object (U), A can suggest that the client continue the search on Server B (B) if U does not reside on A, but is known to be on B. The client has the choice of pursuing the referral or not.</span></span> <span data-ttu-id="d6a04-112">搜尋參考可用來讓用戶端不需要針對每部伺服器的功能進行 advanced 辨識。</span><span class="sxs-lookup"><span data-stu-id="d6a04-112">Search referrals free the client from requiring advanced recognition of the capability of each server.</span></span> <span data-ttu-id="d6a04-113">不過，用戶端必須指定伺服器應該進行的參照類型。</span><span class="sxs-lookup"><span data-stu-id="d6a04-113">However, the client must specify the type of referrals a server should make.</span></span>

<span data-ttu-id="d6a04-114">Active Directory 提供搜尋參考服務。</span><span class="sxs-lookup"><span data-stu-id="d6a04-114">Active Directory offers search referral services.</span></span> <span data-ttu-id="d6a04-115">用戶端可以選擇下列任何一種類型的參考追蹤：</span><span class="sxs-lookup"><span data-stu-id="d6a04-115">A client can choose any of the following types of referral chasing:</span></span>

-   <span data-ttu-id="d6a04-116">永遠不會：即使伺服器辨識到另一部伺服器儲存要求的資料，伺服器也不應該產生用戶端的參考。</span><span class="sxs-lookup"><span data-stu-id="d6a04-116">Never: The server should not generate a referral to a client even though it recognizes that another server stores the requested data.</span></span>
-   <span data-ttu-id="d6a04-117">外部：如果要求可在不同目錄樹狀結構的另一部伺服器上解析，則伺服器應產生參考。</span><span class="sxs-lookup"><span data-stu-id="d6a04-117">External: The server should generate referrals if the request can be resolved on another server of a different directory tree.</span></span> <span data-ttu-id="d6a04-118">例如，用戶端會在 "Fabrikam.com" 網域上的 "fab01" 伺服器上查詢 "OU = Sales，DC = Fabrikam，DC = COM"。</span><span class="sxs-lookup"><span data-stu-id="d6a04-118">For example, a client queries "OU=Sales,DC=Fabrikam,DC=COM" on the "fab01" server on the "Fabrikam.com" domain.</span></span> <span data-ttu-id="d6a04-119">不過，此物件不屬於 "fab01"，但已知在 "Fabrikam.com" 網域上的 "arc01" 伺服器上。</span><span class="sxs-lookup"><span data-stu-id="d6a04-119">However, the object does not belong to "fab01", but is known to be on the "arc01" server on the "Fabrikam.com" domain.</span></span> <span data-ttu-id="d6a04-120">因此，"fab01" 會將用戶端參考至 "arc01"。</span><span class="sxs-lookup"><span data-stu-id="d6a04-120">Thus, "fab01" refers the client to "arc01".</span></span>
-   <span data-ttu-id="d6a04-121">次級：如果要求可在伺服器上解析，而伺服器的名稱形成來自源伺服器的連續路徑，伺服器就應該產生參考。</span><span class="sxs-lookup"><span data-stu-id="d6a04-121">Subordinate: The server should generate referrals if the request can be resolved on a server whose name forms a contiguous path from the originating server.</span></span> <span data-ttu-id="d6a04-122">搜尋範圍必須位於子樹層級。</span><span class="sxs-lookup"><span data-stu-id="d6a04-122">The search scope must be at the subtree level.</span></span>

    <span data-ttu-id="d6a04-123">例如，伺服器 A 包含 "DC = Sales，DC = Fabrikam，DC = Com" 中的物件。</span><span class="sxs-lookup"><span data-stu-id="d6a04-123">For example, Server A contains objects in "DC=Sales,DC=Fabrikam,DC=Com".</span></span> <span data-ttu-id="d6a04-124">伺服器 B 包含 "DC = 西雅圖，DC = Sales，DC = Fabrikam，DC = Com" 中的物件。</span><span class="sxs-lookup"><span data-stu-id="d6a04-124">Server B contains objects in "DC=Seattle,DC=Sales,DC=Fabrikam,DC=Com".</span></span> <span data-ttu-id="d6a04-125">請注意，伺服器 B 的名稱會形成伺服器 A 的連續路徑。當用戶端連線到伺服器 A 時，要求子樹搜尋 "DC = Sales，DC = Fabrikam，DC = Com"，並將參考指定為附屬類型時，就會發生下列事件：</span><span class="sxs-lookup"><span data-stu-id="d6a04-125">Be aware that the name of Server B forms a contiguous path from Server A. When a client contacts Server A, requests a subtree search on "DC=Sales,DC=Fabrikam,DC=Com", and specifies the referral to be a subordinate type, the following event occurs:</span></span>

    -   <span data-ttu-id="d6a04-126">Server A 會傳回它在其範圍內所知道的所有物件。</span><span class="sxs-lookup"><span data-stu-id="d6a04-126">Server A returns all objects that it knows within its scope.</span></span>
    -   <span data-ttu-id="d6a04-127">伺服器 A 會通知用戶端，在伺服器 B 上可以找到 "DC = 西雅圖，DC = Sales，DC = Fabrikam，DC = COM" 中的物件。</span><span class="sxs-lookup"><span data-stu-id="d6a04-127">Server A informs the client that objects in "DC=Seattle,DC=Sales,DC=Fabrikam,DC=COM" can be found on Server B.</span></span>

    <span data-ttu-id="d6a04-128">用戶端可以選擇聯繫伺服器 B。如果是的話，就會發生下列事件：</span><span class="sxs-lookup"><span data-stu-id="d6a04-128">The client can choose to contact Server B. If so, the following event occurs:</span></span>

    -   <span data-ttu-id="d6a04-129">伺服器 B 回應要求的物件。</span><span class="sxs-lookup"><span data-stu-id="d6a04-129">Server B responds with the requested objects.</span></span>
    -   <span data-ttu-id="d6a04-130">如果伺服器 B 偵測到連續命名路徑上的其他伺服器，且進程繼續進行。</span><span class="sxs-lookup"><span data-stu-id="d6a04-130">If Server B detects other servers on the contiguous naming path and the process continues.</span></span>

-   <span data-ttu-id="d6a04-131">永遠：如果可以根據外部類型或從屬類型來解析搜尋，伺服器會產生參考。</span><span class="sxs-lookup"><span data-stu-id="d6a04-131">Always: The server generates referrals if the search can be resolved based on either the external type or the subordinate type.</span></span>

> [!Note]  
> <span data-ttu-id="d6a04-132">在 Active Directory 中，通用類別目錄包含給定企業中的所有物件。</span><span class="sxs-lookup"><span data-stu-id="d6a04-132">In Active Directory, the global catalog contains all objects in a given enterprise.</span></span> <span data-ttu-id="d6a04-133">搜尋通用類別目錄伺服器可產生比從一部伺服器到另一部伺服器的參照更佳的效能。</span><span class="sxs-lookup"><span data-stu-id="d6a04-133">Searching a global catalog server yields better performance than pursuing referrals from one server to another.</span></span>

 

<span data-ttu-id="d6a04-134">在大多數情況下，呼叫端的參考追蹤將會是透明的。</span><span class="sxs-lookup"><span data-stu-id="d6a04-134">In most cases, the referral chasing will be transparent to the caller.</span></span> <span data-ttu-id="d6a04-135">如果是參考不同網域或樹系中的物件，基礎 LDAP API 將會嘗試使用目前的認證來系結至參考的目標。</span><span class="sxs-lookup"><span data-stu-id="d6a04-135">If the referral is to an object in a different domain or forest, the underlying LDAP API will attempt to use the current credentials to bind to the target of the referral.</span></span> <span data-ttu-id="d6a04-136">如果成功，則參考追蹤將會是透明的。</span><span class="sxs-lookup"><span data-stu-id="d6a04-136">If this is successful, the referral chasing will be transparent.</span></span> <span data-ttu-id="d6a04-137">如果不成功，則會傳回參考和參考錯誤碼。</span><span class="sxs-lookup"><span data-stu-id="d6a04-137">If this is not successful, the referral and a referral error code will be returned.</span></span>

<span data-ttu-id="d6a04-138">如需有關搭配特定搜尋介面使用參考追蹤選項的詳細資訊，請參閱：</span><span class="sxs-lookup"><span data-stu-id="d6a04-138">For more information about using the referral chasing options with a specific search interface, see:</span></span>

-   [<span data-ttu-id="d6a04-139">使用 >idirectorysearch 的參考追蹤</span><span class="sxs-lookup"><span data-stu-id="d6a04-139">Referral Chasing with IDirectorySearch</span></span>](referral-chasing-with-idirectorysearch.md)
-   [<span data-ttu-id="d6a04-140">使用 ActiveX Data Objects 搜尋</span><span class="sxs-lookup"><span data-stu-id="d6a04-140">Searching with ActiveX Data Objects</span></span>](searching-with-activex-data-objects-ado.md)
-   [<span data-ttu-id="d6a04-141">使用 OLE DB 搜尋</span><span class="sxs-lookup"><span data-stu-id="d6a04-141">Searching with OLE DB</span></span>](searching-with-ole-db.md)

 

 