---
title: 使用 WKGUID 系結至 Well-Known 物件
description: 本主題說明如何使用 WKGUID 系結字串系結至物件。
ms.assetid: cc9846c4-415e-48ee-ae08-6631636d3a63
ms.tgt_platform: multiple
keywords:
- 使用 WKGUID AD 系結至 Well-Known 物件
- Active Directory、使用、系結，以及使用 WKGUID 系結至已知的物件
- 知名物件廣告
- 已知物件 AD，系結至使用 WKGUID
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: ddd919efa6e52d7e65c2a7cd5550f3d217f54070
ms.sourcegitcommit: 803f3ccd65bdefe36bd851b9c6e7280be9489016
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/17/2020
ms.locfileid: "103681694"
---
# <a name="binding-to-well-known-objects-using-wkguid"></a><span data-ttu-id="f7f07-107">使用 WKGUID 系結至 Well-Known 物件</span><span class="sxs-lookup"><span data-stu-id="f7f07-107">Binding to Well-Known Objects Using WKGUID</span></span>

<span data-ttu-id="f7f07-108">容器可以有一個或多個重要的子類型可以重新命名或移動。</span><span class="sxs-lookup"><span data-stu-id="f7f07-108">Containers can have one, or more, important subobjects that can be renamed or moved.</span></span> <span data-ttu-id="f7f07-109">可能很難追蹤這些子字串並為其建立正確的系結字串，特別是當重新命名或移動時。</span><span class="sxs-lookup"><span data-stu-id="f7f07-109">It can be difficult to track these subobjects and build correct binding strings for them, especially if they are renamed or moved.</span></span>

<span data-ttu-id="f7f07-110">為了支援這些容器內這些物件的重新命名安全系結，Active Directory Domain Services 有兩個屬性： **wellKnownObjects** 和 **otherWellKnownObjects**。</span><span class="sxs-lookup"><span data-stu-id="f7f07-110">To support rename-safe binding to these objects within these containers, Active Directory Domain Services have two attributes: **wellKnownObjects** and **otherWellKnownObjects**.</span></span> <span data-ttu-id="f7f07-111">這些屬性具有具有二進位的 ADSTYPE DN 屬性語法 \_ \_ \_ 。</span><span class="sxs-lookup"><span data-stu-id="f7f07-111">These attributes have an attribute syntax of ADSTYPE\_DN\_WITH\_BINARY.</span></span> <span data-ttu-id="f7f07-112">它們允許多個值，並在其所設定的容器內包含已知物件的 GUID/DN 元組。</span><span class="sxs-lookup"><span data-stu-id="f7f07-112">They allow multiple values and contain the GUID/DN tuples of well-known objects within the containers on which they are set.</span></span> <span data-ttu-id="f7f07-113">Active Directory 伺服器會維護每個 **wellKnownObjects** 和 **otherWellKnownObjects** 專案的分辨名稱部分，使其包含建立專案時所指定之物件的目前分辨名稱。</span><span class="sxs-lookup"><span data-stu-id="f7f07-113">The Active Directory server maintains the distinguished name portion of each **wellKnownObjects** and **otherWellKnownObjects** entry so that it contains the current distinguished name of the object specified when the entry was created.</span></span>

<span data-ttu-id="f7f07-114">**OtherWellKnownObjects** 屬性可以在任何物件上設定和使用。</span><span class="sxs-lookup"><span data-stu-id="f7f07-114">The **otherWellKnownObjects** property can be set and used on any object.</span></span>

<span data-ttu-id="f7f07-115">**WellKnownObjects** 屬性是在 domainDNS 和設定容器上使用。</span><span class="sxs-lookup"><span data-stu-id="f7f07-115">The **wellKnownObjects** property is used on the domainDNS and configuration containers.</span></span> <span data-ttu-id="f7f07-116">**WellKnownObjects** 屬性是僅限系統的屬性，只能由作業系統修改。</span><span class="sxs-lookup"><span data-stu-id="f7f07-116">The **wellKnownObjects** property is a system-only property and can only be modified by the operating system.</span></span>

<span data-ttu-id="f7f07-117">**DomainDNS** 容器具有下列知名物件：</span><span class="sxs-lookup"><span data-stu-id="f7f07-117">The **domainDNS** container has the following well-known objects:</span></span>

-   <span data-ttu-id="f7f07-118">使用者</span><span class="sxs-lookup"><span data-stu-id="f7f07-118">Users</span></span>
-   <span data-ttu-id="f7f07-119">電腦</span><span class="sxs-lookup"><span data-stu-id="f7f07-119">Computers</span></span>
-   <span data-ttu-id="f7f07-120">系統</span><span class="sxs-lookup"><span data-stu-id="f7f07-120">System</span></span>
-   <span data-ttu-id="f7f07-121">網域控制站</span><span class="sxs-lookup"><span data-stu-id="f7f07-121">Domain Controllers</span></span>
-   <span data-ttu-id="f7f07-122">基礎結構</span><span class="sxs-lookup"><span data-stu-id="f7f07-122">Infrastructure</span></span>
-   <span data-ttu-id="f7f07-123">已刪除的物件</span><span class="sxs-lookup"><span data-stu-id="f7f07-123">Deleted Objects</span></span>
-   <span data-ttu-id="f7f07-124">遺失並找到</span><span class="sxs-lookup"><span data-stu-id="f7f07-124">Lost and Found</span></span>

<span data-ttu-id="f7f07-125">設定容器具有已知的物件：已刪除的物件。</span><span class="sxs-lookup"><span data-stu-id="f7f07-125">The configuration container has the well-known object: Deleted Objects.</span></span>

<span data-ttu-id="f7f07-126">這些物件位於 Active Directory 網域服務中的每個 **domainDNS** 和設定容器中。</span><span class="sxs-lookup"><span data-stu-id="f7f07-126">These objects are in every **domainDNS** and configuration container in an Active Directory Domain Service.</span></span>

<span data-ttu-id="f7f07-127">您可以使用 WKGUID 系結格式來系結至已知的物件。</span><span class="sxs-lookup"><span data-stu-id="f7f07-127">You can bind to a well-known object using the WKGUID binding format.</span></span> <span data-ttu-id="f7f07-128">只有 Active Directory Domain Services （也就是 LDAP 提供者）支援與 WKGUID 的系結。</span><span class="sxs-lookup"><span data-stu-id="f7f07-128">Binding with WKGUID is only supported in Active Directory Domain Services, that is, the LDAP provider.</span></span>

> [!IMPORTANT]
> <span data-ttu-id="f7f07-129">請一律使用 WKGUID 系結格式來系結至網域和設定容器中的已知物件（如上所列）。</span><span class="sxs-lookup"><span data-stu-id="f7f07-129">Always use the WKGUID binding format to bind to the well-known objects, as listed above, in the domain and configuration containers.</span></span> <span data-ttu-id="f7f07-130">這樣可確保這些容器可以系結至，即使它們已移動或重新命名也一樣。</span><span class="sxs-lookup"><span data-stu-id="f7f07-130">This ensures that these containers can be bound to even if they are moved or renamed.</span></span>

 

<span data-ttu-id="f7f07-131">WKGUID 系結字串格式如下所示：</span><span class="sxs-lookup"><span data-stu-id="f7f07-131">The WKGUID binding string format is as follows:</span></span>


```C++
LDAP://<servername>/<WKGUID=<XXXXX>,<container DN>>
```



<span data-ttu-id="f7f07-132">「 &lt; 伺服器名稱」 &gt; 是目錄伺服器名稱。</span><span class="sxs-lookup"><span data-stu-id="f7f07-132">"&lt;server name&gt;" is the directory server name.</span></span> <span data-ttu-id="f7f07-133">「 &lt; 伺服器名稱」 &gt; 是選擇性的。</span><span class="sxs-lookup"><span data-stu-id="f7f07-133">The "&lt;server name&gt;" is optional.</span></span>

<span data-ttu-id="f7f07-134">" &lt; XXXXX &gt; " 是 GUID 的十六進位值的字串標記法，代表已知的物件。</span><span class="sxs-lookup"><span data-stu-id="f7f07-134">"&lt;XXXXX&gt;" is the string representation of the hexadecimal value of the GUID that represents the well-known object.</span></span> <span data-ttu-id="f7f07-135">GUID 字串是在 "XXXXXXXXXXXXXXXXXXXXXXXXXXXXXXXX" 表單中指定，而且與 [**StringFromGUID2**](/windows/win32/api/combaseapi/nf-combaseapi-stringfromguid2) 函數所產生的 guid 字串格式不同，其格式為 "{xxxxxxxx-xxxx-xxxx-xxxx-xxxxxxxxxxxx}"。</span><span class="sxs-lookup"><span data-stu-id="f7f07-135">The GUID string is specified in the "XXXXXXXXXXXXXXXXXXXXXXXXXXXXXXXX" form and is not the same form as the GUID string produced by the [**StringFromGUID2**](/windows/win32/api/combaseapi/nf-combaseapi-stringfromguid2) function, which takes the form "{XXXXXXXX-XXXX-XXXX-XXXX-XXXXXXXXXXXX}".</span></span> <span data-ttu-id="f7f07-136">如需詳細資訊和示範如何從 GUID 建立可系結字串的程式碼範例，請參閱 [建立 guid 之可系結字串表示的範例程式碼](example-code-for-creating-a-bindable-string-representation-of-a-guid.md)。</span><span class="sxs-lookup"><span data-stu-id="f7f07-136">For more information and a code example that shows how to create a bindable string from a GUID, see [Example Code for Creating a Bindable String Representation of a GUID](example-code-for-creating-a-bindable-string-representation-of-a-guid.md).</span></span>

<span data-ttu-id="f7f07-137">若要系結至物件中 **otherWellKnownObjects** 所指定的物件，請指定 " &lt; XXXXX &gt; " 作為物件已知物件 GUID 的系結字串形式。</span><span class="sxs-lookup"><span data-stu-id="f7f07-137">To bind to an object specified in **otherWellKnownObjects** in an object, specify "&lt;XXXXX&gt;" as the bind string form of the well-known object GUID of the object.</span></span> <span data-ttu-id="f7f07-138">如需詳細資訊，請參閱 [讀取物件的 objectGUID 和建立 GUID 的字串表示](reading-an-objectampaposs-objectguid-and-creating-a-string-representation-of-the-guid.md)。</span><span class="sxs-lookup"><span data-stu-id="f7f07-138">For more information, see [Reading an Object's objectGUID and Creating a String Representation of the GUID](reading-an-objectampaposs-objectguid-and-creating-a-string-representation-of-the-guid.md).</span></span> <span data-ttu-id="f7f07-139">如需有關在物件上設定 **otherWellKnownObjects** 屬性的詳細資訊，請參閱 [使用 otherWellKnownObjects 屬性啟用 Rename-Safe](enabling-rename-safe-binding-with-the-otherwellknownobjects-property.md)系結。</span><span class="sxs-lookup"><span data-stu-id="f7f07-139">For more information about setting the **otherWellKnownObjects** property on objects, see [Enabling Rename-Safe Binding with the otherWellKnownObjects Property](enabling-rename-safe-binding-with-the-otherwellknownobjects-property.md).</span></span>

<span data-ttu-id="f7f07-140">若要系結至 domainDNS 或設定容器中的 **wellKnownObjects** 所指定的物件，請指定 " &lt; XXXXX &gt; " 作為下列其中一個常數（如下表所示），如 Ntdsapi. h 中所定義。</span><span class="sxs-lookup"><span data-stu-id="f7f07-140">To bind to an object specified in **wellKnownObjects** in domainDNS or configuration containers, specify "&lt;XXXXX&gt;" as one of the following constants, listed in the following table, as defined in Ntdsapi.h.</span></span>



| <span data-ttu-id="f7f07-141">容器</span><span class="sxs-lookup"><span data-stu-id="f7f07-141">Container</span></span>          | <span data-ttu-id="f7f07-142">GUID 識別碼</span><span class="sxs-lookup"><span data-stu-id="f7f07-142">GUID Identifier</span></span>                         |
|--------------------|-----------------------------------------|
| <span data-ttu-id="f7f07-143">使用者</span><span class="sxs-lookup"><span data-stu-id="f7f07-143">Users</span></span>              | <span data-ttu-id="f7f07-144">GUID \_ 使用者 \_ 容器 \_ W</span><span class="sxs-lookup"><span data-stu-id="f7f07-144">GUID\_USERS\_CONTAINER\_W</span></span>               |
| <span data-ttu-id="f7f07-145">電腦</span><span class="sxs-lookup"><span data-stu-id="f7f07-145">Computers</span></span>          | <span data-ttu-id="f7f07-146">GUID \_ COMPUTRS \_ 容器 \_ W</span><span class="sxs-lookup"><span data-stu-id="f7f07-146">GUID\_COMPUTRS\_CONTAINER\_W</span></span>            |
| <span data-ttu-id="f7f07-147">系統</span><span class="sxs-lookup"><span data-stu-id="f7f07-147">System</span></span>             | <span data-ttu-id="f7f07-148">GUID \_ 系統 \_ 容器 \_ W</span><span class="sxs-lookup"><span data-stu-id="f7f07-148">GUID\_SYSTEMS\_CONTAINER\_W</span></span>             |
| <span data-ttu-id="f7f07-149">網域控制站</span><span class="sxs-lookup"><span data-stu-id="f7f07-149">Domain Controllers</span></span> | <span data-ttu-id="f7f07-150">GUID \_ 域 \_ 控制器 \_ 容器 \_ W</span><span class="sxs-lookup"><span data-stu-id="f7f07-150">GUID\_DOMAIN\_CONTROLLERS\_CONTAINER\_W</span></span> |
| <span data-ttu-id="f7f07-151">基礎結構</span><span class="sxs-lookup"><span data-stu-id="f7f07-151">Infrastructure</span></span>     | <span data-ttu-id="f7f07-152">GUID \_ 基礎結構 \_ 容器 \_ W</span><span class="sxs-lookup"><span data-stu-id="f7f07-152">GUID\_INFRASTRUCTURE\_CONTAINER\_W</span></span>      |
| <span data-ttu-id="f7f07-153">已刪除的物件</span><span class="sxs-lookup"><span data-stu-id="f7f07-153">Deleted Objects</span></span>    | <span data-ttu-id="f7f07-154">GUID \_ 刪除的 \_ 物件 \_ 容器 \_ W</span><span class="sxs-lookup"><span data-stu-id="f7f07-154">GUID\_DELETED\_OBJECTS\_CONTAINER\_W</span></span>    |
| <span data-ttu-id="f7f07-155">遺失並找到</span><span class="sxs-lookup"><span data-stu-id="f7f07-155">Lost and Found</span></span>     | <span data-ttu-id="f7f07-156">GUID \_ LOSTANDFOUND \_ 容器 \_ W</span><span class="sxs-lookup"><span data-stu-id="f7f07-156">GUID\_LOSTANDFOUND\_CONTAINER\_W</span></span>        |



 

<span data-ttu-id="f7f07-157">例如，若要系結至網域中的使用者容器，請指定 **GUID \_ 使用者容器（ \_ \_ W** ）作為 " &lt; XXXXX &gt; "。</span><span class="sxs-lookup"><span data-stu-id="f7f07-157">For example, to bind to the user container in a domain, specify **GUID\_USERS\_CONTAINER\_W** as "&lt;XXXXX&gt;".</span></span>

<span data-ttu-id="f7f07-158">「 &lt; 容器 DN」 &gt; 是容器物件的辨別名稱，此物件在其 **wellKnownObjects** 屬性中會以值表示。</span><span class="sxs-lookup"><span data-stu-id="f7f07-158">"&lt;container DN&gt;" is the distinguished name of the container object that has this object represented as a value in its **wellKnownObjects** property.</span></span> <span data-ttu-id="f7f07-159">例如，若要系結至網域中的使用者容器，請將網域辨別名稱指定為「 &lt; 容器 DN」 &gt; 。</span><span class="sxs-lookup"><span data-stu-id="f7f07-159">For example, to bind to the users container in a domain, specify the domain distinguished name as the "&lt;container DN&gt;".</span></span>

<span data-ttu-id="f7f07-160">例如，若要系結至網域 Fabrikam.com 的 users 容器，請使用下列系結字串。</span><span class="sxs-lookup"><span data-stu-id="f7f07-160">For example, to bind to the users container of the domain Fabrikam.com, use the following binding string.</span></span>

``` syntax
LDAP://<WKGUID=a9d1ca15768811d1aded00c04fd8d5cd,dc=Fabrikam,dc=com>
```

<span data-ttu-id="f7f07-161">如需詳細資訊和示範如何系結至已知 GUID 的程式碼範例，請參閱系結 [至已知物件的範例程式碼](example-code-for-binding-to-well-known-objects.md)。</span><span class="sxs-lookup"><span data-stu-id="f7f07-161">For more information and a code example that shows how to bind to a well-known GUID, see [Example Code for Binding to Well Known Objects](example-code-for-binding-to-well-known-objects.md).</span></span>

 

 