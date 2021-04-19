---
title: " (AD DS) 的推薦"
description: Active Directory Domain Services 在設定容器中的資料分割容器 (crossRefContainer) 中，維護所儲存之交叉參考物件中的參考資料。
ms.assetid: e4d6cc8a-9c2c-4e0f-acca-e9ecdd5e879b
ms.tgt_platform: multiple
keywords:
- 參考廣告
- Active Directory，推薦
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: f63c87fb0248d85ab20191296f9659eb58e460f6
ms.sourcegitcommit: 803f3ccd65bdefe36bd851b9c6e7280be9489016
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/17/2020
ms.locfileid: "106965637"
---
# <a name="referrals-ad-ds"></a><span data-ttu-id="234c6-105"> (AD DS) 的推薦</span><span class="sxs-lookup"><span data-stu-id="234c6-105">Referrals (AD DS)</span></span>

<span data-ttu-id="234c6-106">Active Directory Domain Services 在設定容器中的資料分割容器 ([**crossRefContainer**](/windows/desktop/ADSchema/c-crossrefcontainer)) 中，維護所儲存之 [**交叉**](/windows/desktop/ADSchema/c-crossref)參考物件中的參考資料。</span><span class="sxs-lookup"><span data-stu-id="234c6-106">Active Directory Domain Services maintain referral data in [**crossRef**](/windows/desktop/ADSchema/c-crossref) objects stored in the partitions container ([**crossRefContainer**](/windows/desktop/ADSchema/c-crossrefcontainer)) in the configuration container.</span></span> <span data-ttu-id="234c6-107">在 [決定要搜尋的位置](where-to-search.md) 主題時，會在域樹內的網域內容中討論參考，以及在子樹搜尋上產生從屬網域的參考。</span><span class="sxs-lookup"><span data-stu-id="234c6-107">In the [Deciding Where to Search](where-to-search.md) topic, referrals are discussed in the context of a domain within a domain tree and the generation of referrals to subordinate domains on a subtree search.</span></span>

<span data-ttu-id="234c6-108">Active Directory Domain Services 建立和維護樹系中所有網域的 [**交叉引用**](/windows/desktop/ADSchema/c-crossref) 物件。</span><span class="sxs-lookup"><span data-stu-id="234c6-108">Active Directory Domain Services create and maintains [**crossRef**](/windows/desktop/ADSchema/c-crossref) objects for all domains in the forest.</span></span> <span data-ttu-id="234c6-109">此外，也有設定和架構容器的 **交叉引用** 物件。</span><span class="sxs-lookup"><span data-stu-id="234c6-109">In addition, there are **crossRef** objects for the configuration and schema containers.</span></span> <span data-ttu-id="234c6-110">這些 **交叉** 參考物件可用來產生參考，以回應要求有關樹系中之物件的資料，但不包含在處理要求的目錄伺服器上的查詢。</span><span class="sxs-lookup"><span data-stu-id="234c6-110">These **crossRef** objects are used to generate referrals in response to queries that request data about objects that exist in the forest, but not contained on the directory server handling the request.</span></span> <span data-ttu-id="234c6-111">這些稱為 *內部交互參考*，因為它們參考樹系內的網域、架構和設定容器。</span><span class="sxs-lookup"><span data-stu-id="234c6-111">These are called *internal cross references*, because they refer to domains, schema, and configuration containers within the forest.</span></span>

<span data-ttu-id="234c6-112">如果未啟用參考追蹤，且執行子樹搜尋，則搜尋會傳回符合搜尋準則之指定網域內的所有物件。</span><span class="sxs-lookup"><span data-stu-id="234c6-112">If referral chasing is not enabled and a subtree search is performed, the search will return all objects within the specified domain that meet the search criteria.</span></span> <span data-ttu-id="234c6-113">搜尋也會將參考傳回給任何屬於目錄伺服器網域的直接下階的次級網域。</span><span class="sxs-lookup"><span data-stu-id="234c6-113">The search will also return referrals to any subordinate domains that are direct descendants of the directory server domain.</span></span> <span data-ttu-id="234c6-114">用戶端必須藉由系結至參考所指定的路徑並提交另一個查詢，來解析參考。</span><span class="sxs-lookup"><span data-stu-id="234c6-114">The client must resolve the referrals by binding to the path specified by the referral and submitting another query.</span></span>

<span data-ttu-id="234c6-115">如果開啟了參考追蹤並執行子樹搜尋，則基礎 LDAP API 會自動嘗試系結至任何參考，並將搜尋結果新增至結果集。</span><span class="sxs-lookup"><span data-stu-id="234c6-115">If referral chasing is turned on and a subtree search is performed, the underlying LDAP API will automatically attempt to bind to any referrals and add the search results to the result set.</span></span> <span data-ttu-id="234c6-116">在大多數情況下，呼叫端的參考追蹤將會是透明的。</span><span class="sxs-lookup"><span data-stu-id="234c6-116">In most cases, the referral chasing will be transparent to the caller.</span></span> <span data-ttu-id="234c6-117">如果是參考不同網域或樹系中的物件，基礎 LDAP API 將會嘗試使用目前的認證來系結至參考的目標。</span><span class="sxs-lookup"><span data-stu-id="234c6-117">If the referral is to an object in a different domain or forest, the underlying LDAP API will attempt to use the current credentials to bind to the target of the referral.</span></span> <span data-ttu-id="234c6-118">如果成功，則參考追蹤將會是透明的。</span><span class="sxs-lookup"><span data-stu-id="234c6-118">If this is successful, the referral chasing will be transparent.</span></span> <span data-ttu-id="234c6-119">如果不成功，則會傳回參考和參考錯誤碼。</span><span class="sxs-lookup"><span data-stu-id="234c6-119">If this is not successful, the referral and a referral error code will be returned.</span></span>

<span data-ttu-id="234c6-120">如需設定「參考追蹤」搜尋喜好設定的詳細資訊，請參閱 [指定其他搜尋選項](specifying-other-search-options.md)。</span><span class="sxs-lookup"><span data-stu-id="234c6-120">For more information about setting the referral chasing search preference, see [Specifying Other Search Options](specifying-other-search-options.md).</span></span>

<span data-ttu-id="234c6-121">除了 [**dnsRoot**](/windows/desktop/ADSchema/a-dnsroot) (網域的 DNS 名稱) 和 [**nCName**](/windows/desktop/ADSchema/a-ncname) (網域) 屬性的分辨名稱之外，[**交叉引用**](/windows/desktop/ADSchema/c-crossref)物件也包含網域 (的 **nETBIOSName**) NetBIOS 名稱，以及代表網域的直接父系網域 (屬性之 **交叉引用** 物件的 **trustParent**) 辨別名稱。</span><span class="sxs-lookup"><span data-stu-id="234c6-121">In addition to the [**dnsRoot**](/windows/desktop/ADSchema/a-dnsroot) (DNS name of the domain) and [**nCName**](/windows/desktop/ADSchema/a-ncname) (distinguished name for the domain) properties, the [**crossRef**](/windows/desktop/ADSchema/c-crossref) object also contains the **nETBIOSName** (NetBIOS name of the domain) and **trustParent** (distinguished name for the **crossRef** object that represents the domain's direct parent domain) properties.</span></span>

<span data-ttu-id="234c6-122">Active Directory Domain Services 也可以有參考樹系外部物件的 *外部交互參考* 。</span><span class="sxs-lookup"><span data-stu-id="234c6-122">Active Directory Domain Services can also have *external cross references* that refer to objects outside of the forest.</span></span> <span data-ttu-id="234c6-123">外部交互參照必須由系統管理員明確加入。</span><span class="sxs-lookup"><span data-stu-id="234c6-123">External cross references must be added explicitly by an administrator.</span></span> <span data-ttu-id="234c6-124">請注意，外部交互參考的目標伺服器必須有 DNS 根目錄;也就是說，它必須遵守 RFC 2247。</span><span class="sxs-lookup"><span data-stu-id="234c6-124">Be aware that the target server of the external cross reference must have a DNS root; that is, it must adhere to RFC 2247.</span></span>

<span data-ttu-id="234c6-125">外部交互參考是指任何其他樹系上的物件，只要名稱在目標樹系中是唯一的。</span><span class="sxs-lookup"><span data-stu-id="234c6-125">An external cross reference refers to an object on any other forest, as long as the name is unique in the target forest.</span></span> <span data-ttu-id="234c6-126">例如，貴公司所使用的 LDAP 用戶端應用程式可以將作業提交至您的目錄伺服器以進行 Fabrikam.com。</span><span class="sxs-lookup"><span data-stu-id="234c6-126">For example, LDAP client applications that are used by your company can submit operations to your directory servers for Fabrikam.com.</span></span> <span data-ttu-id="234c6-127">您可以建立 Fabrikam.com 的 [**交叉引用**](/windows/desktop/ADSchema/c-crossref) 物件。</span><span class="sxs-lookup"><span data-stu-id="234c6-127">You create a [**crossRef**](/windows/desktop/ADSchema/c-crossref) object for Fabrikam.com.</span></span> <span data-ttu-id="234c6-128">現在，您的目錄伺服器可以將參考傳回給 Fabrikam.com 網域中的物件，而用戶端可以重新尋找參考，而不是傳回「找不到物件」錯誤。</span><span class="sxs-lookup"><span data-stu-id="234c6-128">Now, instead of returning an Object Not Found error, your directory servers can return a referral to an object in the Fabrikam.com domain and the clients can chase the referral.</span></span> <span data-ttu-id="234c6-129">例如，如果您有一個具有下列辨別名稱的物件：</span><span class="sxs-lookup"><span data-stu-id="234c6-129">For example, if you have an object with the following distinguished name:</span></span>


```C++
CN=SomeObject,OU=SomeOU,DC=Fabrikam,DC=Com
```



<span data-ttu-id="234c6-130">您可以為名稱為 "ChildOfSomeObject" 的物件加入外部交互參考。</span><span class="sxs-lookup"><span data-stu-id="234c6-130">You can add an external cross reference for an object with the name "ChildOfSomeObject".</span></span>


```C++
CN=ChildOfSomeObject,CN=SomeObject,OU=SomeOU,DC=Fabrikam,DC=Com
```



<span data-ttu-id="234c6-131">包含 "SomeObject" 的子樹搜尋也會傳回 "ChildOfSomeObject" 的參考。</span><span class="sxs-lookup"><span data-stu-id="234c6-131">A subtree search that contains "SomeObject" will also return a referral to "ChildOfSomeObject".</span></span> <span data-ttu-id="234c6-132">請注意，在參照所指定的位址上必須有 LDAP 伺服器 ([**交叉**](/windows/desktop/ADSchema/c-crossref) 參考物件) 的其中一個屬性，而且此 ldap 伺服器必須提供 "ChildOfSomeObject" 所識別的命名空間。</span><span class="sxs-lookup"><span data-stu-id="234c6-132">Be aware that there must be an LDAP server at the address that is specified by the referral (one of the properties on the [**crossRef**](/windows/desktop/ADSchema/c-crossref) object) and that this LDAP server must serve the namespace that is identified by "ChildOfSomeObject".</span></span>

<span data-ttu-id="234c6-133">由於 [**交叉引用**](/windows/desktop/ADSchema/c-crossref) 物件儲存在設定容器中，因此每個網域控制站 (DC) 都有所有 **交叉交叉** 物件的複本。</span><span class="sxs-lookup"><span data-stu-id="234c6-133">Because [**crossRef**](/windows/desktop/ADSchema/c-crossref) objects are stored in the configuration container, each domain controller (DC) has a copy of all **crossRef** objects.</span></span> <span data-ttu-id="234c6-134">因此，每個 DC 都包含樹系中每個網域以及其高階/附屬關聯性的相關資料。</span><span class="sxs-lookup"><span data-stu-id="234c6-134">Therefore, every DC contains data about every domain in the forest as well as their superior/subordinate relationships.</span></span> <span data-ttu-id="234c6-135">這可讓每個 DC 為樹系中的任何網域產生參考，以及在子樹搜尋上未探索從屬網域、架構或設定容器的參考。</span><span class="sxs-lookup"><span data-stu-id="234c6-135">This enables each DC to generate referrals to any domain in the forest and referrals for unexplored subordinate domain, schema, or configuration containers on a subtree search.</span></span>

<span data-ttu-id="234c6-136">如需有關參考的詳細資訊，請參閱：</span><span class="sxs-lookup"><span data-stu-id="234c6-136">For more information about referrals, see:</span></span>

-   [<span data-ttu-id="234c6-137">當您產生參考時</span><span class="sxs-lookup"><span data-stu-id="234c6-137">When Referrals Are Generated</span></span>](when-referrals-are-generated.md)
-   [<span data-ttu-id="234c6-138">建立外部參考</span><span class="sxs-lookup"><span data-stu-id="234c6-138">Creating an External Referral</span></span>](creating-an-external-referral.md)

<span data-ttu-id="234c6-139">如需詳細資訊和示範如何取得分割區容器之辨別名稱的程式碼範例，請參閱 [尋找分割區容器的範例程式碼](example-code-for-locating-the-partitions-container.md)。</span><span class="sxs-lookup"><span data-stu-id="234c6-139">For more information and a code example that shows how to obtain the distinguished name of the partitions container, see [Example Code for Locating the Partitions Container](example-code-for-locating-the-partitions-container.md).</span></span>

 

 