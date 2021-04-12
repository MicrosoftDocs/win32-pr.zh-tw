---
title: 服務連接點屬性
description: ServiceConnectionPoint 類別的屬性足以應付大部分的服務。
ms.assetid: 08888d2c-b46e-4b86-87e4-0c061ea147a0
ms.tgt_platform: multiple
keywords:
- 服務連接點屬性
- 服務連接點 AD，屬性
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 511bbba8acf50a185f1bdd8b55d9b7f8ce684817
ms.sourcegitcommit: 803f3ccd65bdefe36bd851b9c6e7280be9489016
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/17/2020
ms.locfileid: "104092623"
---
# <a name="service-connection-point-properties"></a><span data-ttu-id="2efab-105">服務連接點屬性</span><span class="sxs-lookup"><span data-stu-id="2efab-105">Service Connection Point Properties</span></span>

<span data-ttu-id="2efab-106">**ServiceConnectionPoint** 類別的屬性足以應付大部分的服務。</span><span class="sxs-lookup"><span data-stu-id="2efab-106">The attributes of the **serviceConnectionPoint** class are sufficient for most services.</span></span> <span data-ttu-id="2efab-107">Active Directory Domain Services 不會定義使用屬性的方式，因此服務的用戶端必須能夠解讀和使用服務 Scp 中的資料。</span><span class="sxs-lookup"><span data-stu-id="2efab-107">Active Directory Domain Services do not define how the attributes are used, so the clients of your service must be able to interpret and use the data in your service SCPs.</span></span> <span data-ttu-id="2efab-108">必須發行其他相關資料的服務，可以藉由建立 **serviceConnectionPoint** 類別的子類別來延伸 Active Directory 架構，讓子類別成為相異名稱。</span><span class="sxs-lookup"><span data-stu-id="2efab-108">Services that must publish additional data about themselves can extend the Active Directory schema by creating a subclass of the **serviceConnectionPoint** class, giving the subclass a distinct name.</span></span> <span data-ttu-id="2efab-109">如需架構延伸的詳細資訊，請參閱 [擴充架構](extending-the-schema.md)。</span><span class="sxs-lookup"><span data-stu-id="2efab-109">For more information about schema extensions, see [Extending the Schema](extending-the-schema.md).</span></span>

<span data-ttu-id="2efab-110">SCP 最重要的屬性是 **關鍵字**、 **serviceDNSName**、 **serviceDNSNameType**、 **serviceClassName** 和 **serviceBindingInformation**。</span><span class="sxs-lookup"><span data-stu-id="2efab-110">The most important attributes of an SCP are **keywords**, **serviceDNSName**, **serviceDNSNameType**, **serviceClassName**, and **serviceBindingInformation**.</span></span> <span data-ttu-id="2efab-111">用戶端應用程式會在目錄中搜尋 **關鍵字** 值以找出您的 SCP。</span><span class="sxs-lookup"><span data-stu-id="2efab-111">Client applications search the directory for **keywords** values to locate your SCP.</span></span> <span data-ttu-id="2efab-112">找到您的 SCP 之後，用戶端就可以讀取其他屬性來取得服務資料。</span><span class="sxs-lookup"><span data-stu-id="2efab-112">When your SCP is found, clients can read other attributes to retrieve service data.</span></span>



<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<thead>
<tr class="header">
<th><span data-ttu-id="2efab-113">屬性</span><span class="sxs-lookup"><span data-stu-id="2efab-113">Attribute</span></span></th>
<th><span data-ttu-id="2efab-114">描述</span><span class="sxs-lookup"><span data-stu-id="2efab-114">Description</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><span data-ttu-id="2efab-115"><strong>關鍵 字</strong></span><span class="sxs-lookup"><span data-stu-id="2efab-115"><strong>keywords</strong></span></span><br/></td>
<td><span data-ttu-id="2efab-116"><strong>關鍵字</strong>屬性可包含多個字串值，以識別您的服務。</span><span class="sxs-lookup"><span data-stu-id="2efab-116">The <strong>keywords</strong> attribute can contain multiple string values that identify your service.</span></span> <span data-ttu-id="2efab-117">此屬性包含在通用類別目錄中，這表示企業樹系的任何網域中的用戶端可以在通用類別目錄中搜尋與您的服務相關聯的關鍵字。</span><span class="sxs-lookup"><span data-stu-id="2efab-117">This attribute is included in the Global Catalog, which means that clients in any domain of an enterprise forest can search the Global Catalog for keywords associated with your service.</span></span> <span data-ttu-id="2efab-118">這個屬性也會編制索引，以改善查詢效能。</span><span class="sxs-lookup"><span data-stu-id="2efab-118">This attribute is also indexed, which improves query performance.</span></span> <span data-ttu-id="2efab-119">建立 SCP 的安裝程式會設定 <strong>關鍵字</strong> 屬性的值。</span><span class="sxs-lookup"><span data-stu-id="2efab-119">The installer that creates the SCP sets the values of the <strong>keywords</strong> attribute.</span></span> <span data-ttu-id="2efab-120">一般而言，使用中的服務不會修改這些值。</span><span class="sxs-lookup"><span data-stu-id="2efab-120">Typically, these values are not modified by the active service.</span></span><br/> <span data-ttu-id="2efab-121">您應該包含在 SCP 中的確切關鍵字，取決於用戶端搜尋服務的方式。</span><span class="sxs-lookup"><span data-stu-id="2efab-121">The exact keywords you should include in your SCP depend on how clients search for your service.</span></span> <span data-ttu-id="2efab-122">要使用的最佳關鍵字是 GUID 字串，因為 Guid 在樹系中保證是唯一的。</span><span class="sxs-lookup"><span data-stu-id="2efab-122">The best keywords to use are GUID strings because GUIDs are guaranteed to be unique in a forest.</span></span> <span data-ttu-id="2efab-123">使用 RPC 程式庫中 <a href="/windows/desktop/api/rpcdce/nf-rpcdce-uuidtostring"><strong>UuidToString</strong></a> 函數所傳回的 GUID 字串格式。</span><span class="sxs-lookup"><span data-stu-id="2efab-123">Use the GUID string format returned by the <a href="/windows/desktop/api/rpcdce/nf-rpcdce-uuidtostring"><strong>UuidToString</strong></a> function in the RPC library.</span></span> <span data-ttu-id="2efab-124">如果用戶端可能會使用它們來搜尋您的服務，您也可以包含人們可讀取的名稱。</span><span class="sxs-lookup"><span data-stu-id="2efab-124">You can also include human-readable names, if clients may use them to search for your service.</span></span> <span data-ttu-id="2efab-125">SCP 中的關鍵字應該包含 GUID 字串及/或名稱，以識別與服務相關的下列資料：</span><span class="sxs-lookup"><span data-stu-id="2efab-125">The keywords in an SCP should include GUID strings and/or names that identify the following data about your service:</span></span>
<ul>
<li><span data-ttu-id="2efab-126">您的公司或組織：例如 Fabrikam。</span><span class="sxs-lookup"><span data-stu-id="2efab-126">Your company or organization: for example, Fabrikam.</span></span></li>
<li><span data-ttu-id="2efab-127">產品或服務：例如 SQL Server。</span><span class="sxs-lookup"><span data-stu-id="2efab-127">The product or service: for example, SQL Server.</span></span> <span data-ttu-id="2efab-128">這可讓用戶端應用程式尋找該類型服務的 Scp。</span><span class="sxs-lookup"><span data-stu-id="2efab-128">This enables client applications to find SCPs for services of that type.</span></span></li>
<li><span data-ttu-id="2efab-129">產品或服務的特定版本，例如7.5。</span><span class="sxs-lookup"><span data-stu-id="2efab-129">The specific version of the product or service, such as 7.5.</span></span></li>
<li><span data-ttu-id="2efab-130">針對針對某一類型服務發佈一組特定資料或功能的 Scp，請包含可識別特定實例的 GUID 字串或名稱。</span><span class="sxs-lookup"><span data-stu-id="2efab-130">For SCPs that publish a specific set of data or capabilities for a type of service, include a GUID string or name that identifies the specific instance.</span></span> <span data-ttu-id="2efab-131">例如，資料庫服務可以發行特定資料庫的 SCP。</span><span class="sxs-lookup"><span data-stu-id="2efab-131">For example, a database service could publish an SCP for a specific database.</span></span> <span data-ttu-id="2efab-132">在此情況下，SCP 會包含用來識別服務的產品 GUID，以及用來識別資料庫的另一個 GUID。</span><span class="sxs-lookup"><span data-stu-id="2efab-132">In this case, the SCP would include a product GUID to identify the service and another GUID to identify the database.</span></span></li>
</ul>
<br/></td>
</tr>
<tr class="even">
<td><span data-ttu-id="2efab-133"><strong>serviceDNSName</strong> 和 <strong>serviceDNSNameType</strong></span><span class="sxs-lookup"><span data-stu-id="2efab-133"><strong>serviceDNSName</strong> and <strong>serviceDNSNameType</strong></span></span><br/></td>
<td><span data-ttu-id="2efab-134">用戶端應用程式會使用 <strong>serviceDNSName</strong> 和 <strong>serviceDNSNameType</strong> 屬性來判斷服務的主機電腦。</span><span class="sxs-lookup"><span data-stu-id="2efab-134">Client applications use the <strong>serviceDNSName</strong> and <strong>serviceDNSNameType</strong> attributes to determine the service's host computer.</span></span> <span data-ttu-id="2efab-135"><strong>ServiceDNSNameType</strong>值指出<strong>serviceDNSName</strong>所指定的 DNS 名稱類型，通常 &quot; 是 &quot; <strong>serviceDNSName</strong>包含主機名稱， &quot; &quot; 如果<strong>serviceDNSName</strong>包含 srv 記錄名稱，則為 srv。</span><span class="sxs-lookup"><span data-stu-id="2efab-135">The <strong>serviceDNSNameType</strong> value indicates the type of DNS name specified by <strong>serviceDNSName</strong> usually &quot;A&quot; if <strong>serviceDNSName</strong> contains a host name or &quot;SRV&quot; if <strong>serviceDNSName</strong> contains a SRV record name.</span></span><br/> <span data-ttu-id="2efab-136"><strong>ServiceDNSName</strong>值通常是服務主機電腦的 DNS 名稱。</span><span class="sxs-lookup"><span data-stu-id="2efab-136">The <strong>serviceDNSName</strong> value is typically the DNS name of the service's host computer.</span></span> <span data-ttu-id="2efab-137">您的服務安裝程式可以呼叫 <a href="/windows/desktop/api/sysinfoapi/nf-sysinfoapi-getcomputernameexa"><strong>GetComputerNameEx</strong></a> 函數來取得本機電腦的 DNS 名稱。</span><span class="sxs-lookup"><span data-stu-id="2efab-137">Your service installer can call the <a href="/windows/desktop/api/sysinfoapi/nf-sysinfoapi-getcomputernameexa"><strong>GetComputerNameEx</strong></a> function to get the DNS name of the local computer.</span></span><br/> <span data-ttu-id="2efab-138">對於具有 DNS SRV 記錄的服務， <strong>serviceDNSName</strong> 可以是 SRV 記錄的名稱。</span><span class="sxs-lookup"><span data-stu-id="2efab-138">For services that have DNS SRV records, <strong>serviceDNSName</strong> can be the name of the SRV record.</span></span> <span data-ttu-id="2efab-139">用戶端應用程式會使用 DNS Api 來取得所有符合此名稱的 SRV 記錄。</span><span class="sxs-lookup"><span data-stu-id="2efab-139">A client application uses the DNS APIs to retrieve all the SRV records that match this name.</span></span> <span data-ttu-id="2efab-140">然後，用戶端會從其中一個 SRV 記錄抓取 DNS 主機名稱。</span><span class="sxs-lookup"><span data-stu-id="2efab-140">The client then retrieves the DNS host name from one of the SRV records.</span></span> <span data-ttu-id="2efab-141">這項技術適用于複寫的服務，因為 SRV 記錄也包含可讓用戶端選取最佳複本的資料。</span><span class="sxs-lookup"><span data-stu-id="2efab-141">This technique is useful for replicated services because SRV records also include data that enables the client to select the best replica.</span></span><br/></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="2efab-142"><strong>serviceBindingInformation</strong></span><span class="sxs-lookup"><span data-stu-id="2efab-142"><strong>serviceBindingInformation</strong></span></span><br/></td>
<td><span data-ttu-id="2efab-143">多值屬性，包含儲存系結至服務所需資料的字串值。</span><span class="sxs-lookup"><span data-stu-id="2efab-143">A multi-value property that contains string values that store data required to bind to a service.</span></span> <span data-ttu-id="2efab-144">這個屬性會進行索引，並複寫至通用類別目錄。</span><span class="sxs-lookup"><span data-stu-id="2efab-144">This property is indexed and is replicated to the Global Catalog.</span></span><br/> <span data-ttu-id="2efab-145"><strong>ServiceBindingInformation</strong>的內容是發佈 SCP 的服務所特有;用戶端必須解讀系結資料。</span><span class="sxs-lookup"><span data-stu-id="2efab-145">The content of <strong>serviceBindingInformation</strong> is specific to the service that published the SCP; clients must interpret the binding data.</span></span> <span data-ttu-id="2efab-146">在最常見的情況下，系結資料包含在服務主機電腦上的埠號碼。</span><span class="sxs-lookup"><span data-stu-id="2efab-146">In the most common case, the binding data consists of a port number on the service host computer.</span></span><br/></td>
</tr>
<tr class="even">
<td><span data-ttu-id="2efab-147"><strong>serviceClassName</strong></span><span class="sxs-lookup"><span data-stu-id="2efab-147"><strong>serviceClassName</strong></span></span><br/></td>
<td><span data-ttu-id="2efab-148">單一值屬性，識別 SCP 所表示的服務類別。</span><span class="sxs-lookup"><span data-stu-id="2efab-148">A single-value property that identifies the class of service represented by the SCP.</span></span> <span data-ttu-id="2efab-149">這是發佈 SCP 之服務特定的描述性字串;例如，SqlServer。</span><span class="sxs-lookup"><span data-stu-id="2efab-149">This is a descriptive string specific to the service that published the SCP; for example, SqlServer.</span></span> <span data-ttu-id="2efab-150">針對支援相互驗證的服務，用戶端可以使用此屬性以及服務主機電腦的 DNS 名稱，形成服務主體名稱。</span><span class="sxs-lookup"><span data-stu-id="2efab-150">For services that support mutual authentication, clients can use this property, along with the DNS name of the service's host computer, to form a service principal name.</span></span> <span data-ttu-id="2efab-151">如需詳細資訊，請參閱 <a href="mutual-authentication-using-kerberos.md">使用 Kerberos 進行相互驗證</a>。</span><span class="sxs-lookup"><span data-stu-id="2efab-151">For more information, see <a href="mutual-authentication-using-kerberos.md">Mutual Authentication Using Kerberos</a>.</span></span><br/></td>
</tr>
</tbody>
</table>



 

 

