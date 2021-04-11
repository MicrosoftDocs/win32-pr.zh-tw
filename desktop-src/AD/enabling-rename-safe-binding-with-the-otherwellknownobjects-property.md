---
title: 使用 otherWellKnownObjects 屬性啟用 Rename-Safe 系結
description: 容器類別的物件具有 otherWellKnownObjects 屬性，可讓您用來建立 GUID 與容器中子物件 (DN) 的分辨名稱之間的關聯。
ms.assetid: 54f7468b-03e5-46b9-8b43-e3571dccdceb
ms.tgt_platform: multiple
keywords:
- otherWellKnownObjects 屬性
- otherWellKnownObjects 屬性，用於重新命名安全系結
- Active Directory、using、binding、重新命名安全的系結
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: d7114fa6dfb44625433d8da1c57491a13aefa7cc
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 09/16/2019
ms.locfileid: "104183020"
---
# <a name="enabling-rename-safe-binding-with-the-otherwellknownobjects-property"></a><span data-ttu-id="15d7c-106">使用 otherWellKnownObjects 屬性啟用 Rename-Safe 系結</span><span class="sxs-lookup"><span data-stu-id="15d7c-106">Enabling Rename-Safe Binding with the otherWellKnownObjects Property</span></span>

<span data-ttu-id="15d7c-107">容器類別的物件具有 **otherWellKnownObjects** 屬性，可讓您用來建立 GUID 與容器中子物件 (DN) 的分辨名稱之間的關聯。</span><span class="sxs-lookup"><span data-stu-id="15d7c-107">Objects of the Container class have an **otherWellKnownObjects** attribute that you can use to associate a GUID with the distinguished name (DN) of a child object in the container.</span></span> <span data-ttu-id="15d7c-108">如果移動或重新命名子物件，Active Directory 伺服器會更新該子物件之 **otherWellKnownObjects** 值中的 DN。</span><span class="sxs-lookup"><span data-stu-id="15d7c-108">If the child object is moved or renamed, the Active Directory server updates the DN in the **otherWellKnownObjects** value for that child object.</span></span> <span data-ttu-id="15d7c-109">這可讓您使用 WKGUID 系結功能，利用容器的 GUID 和 DN 來系結至子物件，而非子物件的 DN。</span><span class="sxs-lookup"><span data-stu-id="15d7c-109">This enables use of the WKGUID binding feature to bind to the child object using the GUID and the DN of the container rather than the child object's DN.</span></span>

<span data-ttu-id="15d7c-110">**OtherWellKnownObjects** 屬性相當於 **wellKnownObjects** 屬性，但應用程式和服務可以寫入 **otherWellKnownObjects** 值，但只有系統才能寫入 **wellKnownObjects**。</span><span class="sxs-lookup"><span data-stu-id="15d7c-110">The **otherWellKnownObjects** attribute is equivalent to the **wellKnownObjects** attribute except that applications and services can write an **otherWellKnownObjects** value, but only the system can write **wellKnownObjects**.</span></span>

<span data-ttu-id="15d7c-111">在下列情況下，使用 **otherWellKnownObjects** 屬性和 WKGUID 系結會很有説明：在需要重新命名安全系結的情況下，相對於特定的容器物件。</span><span class="sxs-lookup"><span data-stu-id="15d7c-111">Using **otherWellKnownObjects** attribute and WKGUID binding is beneficial in the following situations where rename-safe binding is required in relation to a specific container object.</span></span>

<span data-ttu-id="15d7c-112">如果容器物件包含其他重要物件，或可以重新命名或移動重要物件。</span><span class="sxs-lookup"><span data-stu-id="15d7c-112">If a container object contains other important objects, or if important objects can be renamed or moved.</span></span>

<span data-ttu-id="15d7c-113">如果容器物件的每個實例都有重要的物件。</span><span class="sxs-lookup"><span data-stu-id="15d7c-113">If the important objects exist for each instance of the container object.</span></span> <span data-ttu-id="15d7c-114">例如，系統會使用每個 **domainDNS** 物件的 **wellKnownObjects** 屬性來儲存 [使用者] 容器的值（存在於 **domainDNS** 物件的每個實例中）。</span><span class="sxs-lookup"><span data-stu-id="15d7c-114">For example, the system uses the **wellKnownObjects** attribute of each **domainDNS** object to store a value for the Users container, which exists in every instance of a **domainDNS** object.</span></span> <span data-ttu-id="15d7c-115">這可讓應用程式藉由指定知名的 GUID 和 **domainDNS** 容器的 DN，以重新命名安全的方式系結至 Users 容器。</span><span class="sxs-lookup"><span data-stu-id="15d7c-115">This enables applications to bind to the Users container in a rename-safe way by specifying the well-known GUID and the DN of the **domainDNS** container.</span></span> <span data-ttu-id="15d7c-116">應用程式可以使用類似的容器 **otherWellKnownObjects** 屬性。</span><span class="sxs-lookup"><span data-stu-id="15d7c-116">Applications can use a container's **otherWellKnownObjects** attribute similarly.</span></span>

<span data-ttu-id="15d7c-117">如果您需要重要物件的重新命名安全系結和/或搜尋功能。</span><span class="sxs-lookup"><span data-stu-id="15d7c-117">If you require rename-safe binding and/or search capability on the important objects.</span></span>

<span data-ttu-id="15d7c-118">**新增重新命名安全系結和搜尋功能**</span><span class="sxs-lookup"><span data-stu-id="15d7c-118">**To add rename-safe binding and search capabilities**</span></span>

1.  <span data-ttu-id="15d7c-119">在該容器內建立重要物件時，將值新增至容器物件的 **otherWellKnownObjects** 屬性。</span><span class="sxs-lookup"><span data-stu-id="15d7c-119">Add a value to the **otherWellKnownObjects** property of the container object when the important object is created within that container.</span></span> <span data-ttu-id="15d7c-120">值包含表示已知物件的 GUID。</span><span class="sxs-lookup"><span data-stu-id="15d7c-120">The value contains the GUID that represents the well-known object.</span></span> <span data-ttu-id="15d7c-121">請注意，這不是該物件的 **objectGUID** 和 **distinguishedName** 。</span><span class="sxs-lookup"><span data-stu-id="15d7c-121">Be aware that this is not the **objectGUID** and the **distinguishedName** for that object.</span></span>
2.  <span data-ttu-id="15d7c-122">使用 WKGUID 系結功能來系結或搜尋重要的物件。</span><span class="sxs-lookup"><span data-stu-id="15d7c-122">Use the WKGUID binding feature to bind to or search the important object.</span></span>

<span data-ttu-id="15d7c-123">**OtherWellKnownObjects** 屬性可以有多個值，並在其所設定的容器內包含已知物件的 GUID/DN 元組。</span><span class="sxs-lookup"><span data-stu-id="15d7c-123">The **otherWellKnownObjects** attribute can have multiple values and contains the GUID/DN tuples of well-known objects within the containers on which they are set.</span></span> <span data-ttu-id="15d7c-124">**OtherWellKnownObjects** 屬性具有 DNWithBinary 語法，其中的值具有下列格式：</span><span class="sxs-lookup"><span data-stu-id="15d7c-124">The **otherWellKnownObjects** attribute has the DNWithBinary syntax in which values have the following form:</span></span>


```C++
B:<char count>:<well known GUID>:<object DN>
```



<span data-ttu-id="15d7c-125">在此範例中，「 &lt; char count」 &gt; 是「知名 GUID」中的十六進位數位計數 &lt; ，也 &gt; 就是 32 (GUID 中的十六進位位數) **otherWellKnownObjects** 和 **wellKnownObjects** 的數目。</span><span class="sxs-lookup"><span data-stu-id="15d7c-125">In this example, "&lt;char count&gt;" is the count of hexadecimal digits in "&lt;well known GUID&gt;", which is 32 (number of hex digits in a GUID) for both **otherWellKnownObjects** and **wellKnownObjects**.</span></span> <span data-ttu-id="15d7c-126">「 &lt; 知名 guid」 &gt; 是已知 guid 的十六進位數位標記法。</span><span class="sxs-lookup"><span data-stu-id="15d7c-126">"&lt;well known GUID&gt;" is the hexadecimal digit representation of the well-known GUID.</span></span> <span data-ttu-id="15d7c-127">「 &lt; 物件 DN」 &gt; 是此 WKO 值所代表之物件的辨別名稱。</span><span class="sxs-lookup"><span data-stu-id="15d7c-127">"&lt;object DN&gt;" is the distinguished name of the object represented by this WKO value.</span></span> <span data-ttu-id="15d7c-128">伺服器會維護每個 **wellKnownObjects** 和 **OtherWellKnownObjects** 值的 ObjectDN 部分，使其包含最初在建立值時所指定之物件的目前分辨名稱。</span><span class="sxs-lookup"><span data-stu-id="15d7c-128">The server maintains the ObjectDN portion of each **wellKnownObjects** and **otherWellKnownObjects** value so that it contains the current distinguished name of the object originally specified when the value was created.</span></span>

<span data-ttu-id="15d7c-129">例如，如果 {df447b5e-aa5b-11d2-8d53-00c04f79ab81} 是 Fabrikam.com 網域中 MyContainer 容器中 MyObject 物件的已知 GUID，則 **otherWellKnownObjects** 值會指定已知的 Guid 和 MYOBJECT 的 DN：</span><span class="sxs-lookup"><span data-stu-id="15d7c-129">For example, if {df447b5e-aa5b-11d2-8d53-00c04f79ab81} is the well-known GUID of the MyObject object in the MyContainer container in the Fabrikam.com domain, the **otherWellKnownObjects** value would specify the well-known GUID and the DN of MyObject:</span></span>


```C++
B:32:df447b5eaa5b11d28d5300c04f79ab81:cn=MyObject,cn=MyContainer,dc=Fabrikam,dc=com
```



<span data-ttu-id="15d7c-130">若要系結至此物件，請使用下列 WKGUID 系結字串，以指定物件的已知 GUID 以及容器的 DN：</span><span class="sxs-lookup"><span data-stu-id="15d7c-130">To bind to this object, use the following WKGUID binding string that specifies the well-known GUID of the object and the DN of the container:</span></span>


```C++
LDAP://<WKGUID=df447b5eaa5b11d28d5300c04f79ab81,cn=MyContainer,dc=Fabrikam,dc=com>
```



<span data-ttu-id="15d7c-131">系結至此物件之後，您可以使用 ADSI COM 介面來搜尋、讀取、修改或刪除物件。</span><span class="sxs-lookup"><span data-stu-id="15d7c-131">After binding to this object, you can use the ADSI COM interfaces to search, read, modify, or delete the object.</span></span>

<span data-ttu-id="15d7c-132">如需詳細資訊和示範如何將物件加入至 **otherWellKnownObjects** 屬性的程式碼範例，請參閱 [建立容器物件的範例程式碼](example-code-for-creating-a-container-object.md)。</span><span class="sxs-lookup"><span data-stu-id="15d7c-132">For more information and a code example that shows how to add an object to the **otherWellKnownObjects** attribute, see [Example Code for Creating a Container Object](example-code-for-creating-a-container-object.md).</span></span>

 

 




