---
title: 搜尋定義域內容
description: 在討論要系結到何處開始搜尋網域中的物件之前，請先瞭解資料如何儲存在 Active Directory Domain Services 中。
ms.assetid: fd0b4556-465b-4338-87cb-375450590c44
ms.tgt_platform: multiple
keywords:
- 網域內容 Active Directory
- 搜尋定義域內容 Active Directory
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 9c18cd879e950fd9c467f6674092947d430d8f87
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 09/16/2019
ms.locfileid: "104020831"
---
# <a name="searching-domain-contents"></a><span data-ttu-id="6b7f5-105">搜尋定義域內容</span><span class="sxs-lookup"><span data-stu-id="6b7f5-105">Searching Domain Contents</span></span>

<span data-ttu-id="6b7f5-106">在討論要系結到何處開始搜尋網域中的物件之前，請先瞭解資料如何儲存在 Active Directory Domain Services 中。</span><span class="sxs-lookup"><span data-stu-id="6b7f5-106">Before discussing where to bind to begin a search for objects in a domain, it is helpful to understand how data is stored in Active Directory Domain Services.</span></span>

<span data-ttu-id="6b7f5-107">如果您有一個具有多個網域的樹系，Active Directory Domain Services 不會將所有物件資料儲存在單一網域控制站上，因為效能、擴充性和可靠性的原因。</span><span class="sxs-lookup"><span data-stu-id="6b7f5-107">If you have a forest with more than one domain, Active Directory Domain Services does not store all object data on a single domain controller — for performance, scalability, and reliability reasons.</span></span> <span data-ttu-id="6b7f5-108">網域控制站只會保存其所屬網域的所有資訊 (它具有網域) 的完整複本。</span><span class="sxs-lookup"><span data-stu-id="6b7f5-108">A domain controller holds all information about only the domain that it is a member of (it has a full replica of the domain).</span></span> <span data-ttu-id="6b7f5-109">但網域控制站不會保存任何其他網域的完整資訊。</span><span class="sxs-lookup"><span data-stu-id="6b7f5-109">But a domain controller does not hold complete information about any other domain.</span></span>

<span data-ttu-id="6b7f5-110">如果您系結至已關閉參考追蹤的網域物件，則可以搜尋該網域中的任何物件，而且只搜尋該網域。</span><span class="sxs-lookup"><span data-stu-id="6b7f5-110">If you bind to the domain object with referral chasing turned off, you can search for any object in that domain and only that domain.</span></span> <span data-ttu-id="6b7f5-111">如需有關參考追蹤的詳細資訊，請參閱 [參考](referrals.md)。</span><span class="sxs-lookup"><span data-stu-id="6b7f5-111">For more information about referral chasing, see [Referrals](referrals.md).</span></span> <span data-ttu-id="6b7f5-112">搜尋可以取得任何屬性，而且可以使用包含任何屬性的查詢篩選準則。</span><span class="sxs-lookup"><span data-stu-id="6b7f5-112">A search can retrieve any property and can use a query filter containing any property.</span></span>

<span data-ttu-id="6b7f5-113">在樹系中，網域會以階層方式排列為網域樹狀結構。</span><span class="sxs-lookup"><span data-stu-id="6b7f5-113">In a forest, domains are arranged hierarchically as domain trees.</span></span> <span data-ttu-id="6b7f5-114">網域樹狀結構可以是單一網域或具有一個或多個子網域的網域。</span><span class="sxs-lookup"><span data-stu-id="6b7f5-114">A domain tree can be just a single domain or a domain with one or more child domains.</span></span> <span data-ttu-id="6b7f5-115">這些子域接著可以有子定義域。</span><span class="sxs-lookup"><span data-stu-id="6b7f5-115">These child domains, in turn, can have child domains beneath them.</span></span> <span data-ttu-id="6b7f5-116">網域樹狀結構也是連續的命名空間。</span><span class="sxs-lookup"><span data-stu-id="6b7f5-116">A domain tree is also a contiguous namespace.</span></span> <span data-ttu-id="6b7f5-117">連續的命名空間表示子定義域是命名階層的接續。</span><span class="sxs-lookup"><span data-stu-id="6b7f5-117">A contiguous namespace means that the child domains are a continuation of the naming hierarchy.</span></span> <span data-ttu-id="6b7f5-118">例如，網域 fabrikam.com (或 DC = Fabrikam，DC = COM) 可以有一個名為 mydivision (mydivision.fabrikam.com 或 DC = mydivision，DC = Fabrikam，DC = COM) 的子域，而該網域接著可能會有一個名為 mydev 的子域 (mydev.mydivision.fabrikam.com 或 DC = mydev，DC = mydivision，DC = Fabrikam，DC = COM) 。</span><span class="sxs-lookup"><span data-stu-id="6b7f5-118">For example, a domain fabrikam.com (or DC=Fabrikam, DC=COM) can have a child domain named mydivision (mydivision.fabrikam.com or DC=mydivision, DC=Fabrikam, DC=COM), which in turn could have a child domain named mydev (mydev.mydivision.fabrikam.com or DC=mydev, DC=mydivision, DC=Fabrikam, DC=COM).</span></span>

<span data-ttu-id="6b7f5-119">如果您系結至網域物件 (並針對網域樹狀結構中的網域開啟) 的參考追蹤，您將會在其中搜尋該網域和整個階層。</span><span class="sxs-lookup"><span data-stu-id="6b7f5-119">If you bind to a domain object (with referral chasing turned on) for a domain within a domain tree, you will search that domain and the entire hierarchy within it.</span></span> <span data-ttu-id="6b7f5-120">搜尋可以取得任何屬性，而且可以使用包含任何屬性的查詢篩選準則。</span><span class="sxs-lookup"><span data-stu-id="6b7f5-120">The search can retrieve any property and can use a query filter containing any property.</span></span>

<span data-ttu-id="6b7f5-121">如果網域控制站只包含其專屬網域的完整複本，您可以在網域樹狀目錄上執行子樹搜尋。</span><span class="sxs-lookup"><span data-stu-id="6b7f5-121">If a domain controller contains a full replica of only its own domain, you can perform a subtree search on a domain tree.</span></span> <span data-ttu-id="6b7f5-122">網域保存其子定義域的參考。</span><span class="sxs-lookup"><span data-stu-id="6b7f5-122">A domain holds references to its child domains.</span></span> <span data-ttu-id="6b7f5-123">當網域控制站針對其本身的網域處理子樹搜尋要求時，網域控制站會搜尋該網域，然後將對其每個子域的參考傳回給用戶端。</span><span class="sxs-lookup"><span data-stu-id="6b7f5-123">When a domain controller processes a subtree search request against its own domain, the domain controller searches that domain and then returns referrals to each of its child domains to the client.</span></span> <span data-ttu-id="6b7f5-124">參考是指目錄伺服器通訊的方式，它不包含完成要求所需的資訊 (例如查詢) 但是參考可能包含必要資訊的伺服器。</span><span class="sxs-lookup"><span data-stu-id="6b7f5-124">A referral is the way that a directory server communicates that it does not contain the information required to complete a request (such as a query) but has a reference to a server that may contain the required information.</span></span> <span data-ttu-id="6b7f5-125">在樹系搜尋網域樹狀結構的案例中，會傳回每個直接子域的參考，以便在每個子網域中的網域控制站繼續搜尋。</span><span class="sxs-lookup"><span data-stu-id="6b7f5-125">In the case of a subtree search of a domain tree, a referral is returned for each direct child domain so that the search can be continued at a domain controller in each child domain.</span></span> <span data-ttu-id="6b7f5-126">如果開啟了參考追蹤，LDAP 用戶端程式庫 (Wldap32.dll) 會使用這些參照來系結至每個子網域中的網域控制站，然後繼續搜尋。</span><span class="sxs-lookup"><span data-stu-id="6b7f5-126">If referral chasing is turned on, the LDAP client library (Wldap32.dll) uses those referrals to bind to a domain controller in each child domain and continue the search.</span></span> <span data-ttu-id="6b7f5-127">如果關閉了參考追蹤，LDAP 用戶端便無法解析參考，且搜尋已完成。</span><span class="sxs-lookup"><span data-stu-id="6b7f5-127">If referral chasing is turned off, the LDAP client does not resolve the referrals and the search is complete.</span></span>

<span data-ttu-id="6b7f5-128">如果子域的網域控制站連線速度很慢，子樹會在已開啟參考追蹤的網域樹狀目錄上搜尋，可能會很耗時。</span><span class="sxs-lookup"><span data-stu-id="6b7f5-128">A subtree search on a domain tree with referral chasing turned on can be time-consuming if there is a slow connection to the domain controllers for the child domains.</span></span> <span data-ttu-id="6b7f5-129">如果您只想要搜尋單一網域，您應該關閉參考追蹤，以避免不必要地搜尋子域。</span><span class="sxs-lookup"><span data-stu-id="6b7f5-129">If you want to search only a single domain, you should turn referral chasing off to avoid having to search the child domains unnecessarily.</span></span>

 

 




