---
title: 系結至 Active Directory Domain Services
description: 在 Active Directory Domain Services 中，將程式設計物件與特定 Active Directory Domain Services 物件產生關聯的動作稱為「系結」（binding）。
ms.assetid: f48de4d4-c53a-4e40-a34e-4236c3e6cb21
ms.tgt_platform: multiple
keywords:
- 系結至 Active Directory Domain Services Active Directory
- Active Directory Domain Services Active Directory，系結至
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 6f57aef2b2a3c21ac860d05dd1b7a1e1079d1720
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/07/2021
ms.locfileid: "103936119"
---
# <a name="binding-to-active-directory-domain-services"></a><span data-ttu-id="88338-105">系結至 Active Directory Domain Services</span><span class="sxs-lookup"><span data-stu-id="88338-105">Binding to Active Directory Domain Services</span></span>

<span data-ttu-id="88338-106">在 Active Directory Domain Services 中，將程式設計物件與特定 Active Directory Domain Services 物件產生關聯的動作稱為「系結」（ *binding*）。</span><span class="sxs-lookup"><span data-stu-id="88338-106">In Active Directory Domain Services, the act of associating a programmatic object with a specific Active Directory Domain Services object is known as *binding*.</span></span> <span data-ttu-id="88338-107">當程式設計物件（例如 [**IADs**](/windows/desktop/api/iads/nn-iads-iads) 或 [DirectoryEntry](/dotnet/api/system.directoryservices.directoryentry?view=dotnet-plat-ext-3.1&preserve-view=true) 物件）與特定目錄物件相關聯時，程式設計物件會被視為系結 *至* 目錄物件。</span><span class="sxs-lookup"><span data-stu-id="88338-107">When a programmatic object, such as an [**IADs**](/windows/desktop/api/iads/nn-iads-iads) or [DirectoryEntry](/dotnet/api/system.directoryservices.directoryentry?view=dotnet-plat-ext-3.1&preserve-view=true) object, is associated with a specific directory object, the programmatic object is considered to be *bound to* the directory object.</span></span>

## <a name="binding-functions-and-methods"></a><span data-ttu-id="88338-108">系結函式和方法</span><span class="sxs-lookup"><span data-stu-id="88338-108">Binding Functions and Methods</span></span>

<span data-ttu-id="88338-109">以程式設計方式系結至 Active Directory 物件的方法將取決於所使用的程式設計技術。</span><span class="sxs-lookup"><span data-stu-id="88338-109">The method for programmatically binding to an Active Directory object will depend on the programming technology that is used.</span></span> <span data-ttu-id="88338-110">如需有關使用特定程式設計技術系結至 Active Directory Domain Services 中物件的詳細資訊，請參閱下表所列的主題。</span><span class="sxs-lookup"><span data-stu-id="88338-110">For more information about binding to objects in Active Directory Domain Services with a specific programming technology, see the topics listed in the following table.</span></span>



| <span data-ttu-id="88338-111">程式設計技術</span><span class="sxs-lookup"><span data-stu-id="88338-111">Programming technology</span></span>                                                                       | <span data-ttu-id="88338-112">取得詳細資訊</span><span class="sxs-lookup"><span data-stu-id="88338-112">For more information</span></span>                                                           |
|----------------------------------------------------------------------------------------------|--------------------------------------------------------------------------------|
| [<span data-ttu-id="88338-113">Active Directory 服務介面</span><span class="sxs-lookup"><span data-stu-id="88338-113">Active Directory Service Interfaces</span></span>](/windows/desktop/ADSI/active-directory-service-interfaces-adsi)         | [<span data-ttu-id="88338-114">系結至 ADSI 物件</span><span class="sxs-lookup"><span data-stu-id="88338-114">Binding to an ADSI Object</span></span>](/windows/desktop/ADSI/binding-to-an-adsi-object)                    |
| [<span data-ttu-id="88338-115">輕量型目錄存取協定</span><span class="sxs-lookup"><span data-stu-id="88338-115">Lightweight Directory Access Protocol</span></span>](/previous-versions/windows/desktop/ldap/lightweight-directory-access-protocol-ldap-api) | [<span data-ttu-id="88338-116">建立 LDAP 會話</span><span class="sxs-lookup"><span data-stu-id="88338-116">Establishing an LDAP Session</span></span>](/previous-versions/windows/desktop/ldap/establishing-an-ldap-session)              |
| [<span data-ttu-id="88338-117">System.DirectoryServices</span><span class="sxs-lookup"><span data-stu-id="88338-117">System.DirectoryServices</span></span>](/dotnet/api/system.directoryservices)                 | <span data-ttu-id="88338-118">[系結至目錄物件](/previous-versions/ms180840(v=vs.90))</span><span class="sxs-lookup"><span data-stu-id="88338-118">[Binding to Directory Objects](/previous-versions/ms180840(v=vs.90))</span></span> |



 

## <a name="binding-strings"></a><span data-ttu-id="88338-119">系結字串</span><span class="sxs-lookup"><span data-stu-id="88338-119">Binding Strings</span></span>

<span data-ttu-id="88338-120">所有系結函數和方法都需要系結字串。</span><span class="sxs-lookup"><span data-stu-id="88338-120">All bind functions and methods require a binding string.</span></span> <span data-ttu-id="88338-121">系結字串的形式視提供者而定。</span><span class="sxs-lookup"><span data-stu-id="88338-121">The form of the binding string depends on the provider.</span></span> <span data-ttu-id="88338-122">有兩個提供者（LDAP 和 WinNT）支援 Active Directory Domain Services。</span><span class="sxs-lookup"><span data-stu-id="88338-122">Active Directory Domain Services are supported by two providers, LDAP and WinNT.</span></span>

<span data-ttu-id="88338-123">從 Windows 2000 開始，LDAP 提供者會用來存取 Active Directory Domain Services。</span><span class="sxs-lookup"><span data-stu-id="88338-123">Beginning with Windows 2000, the LDAP provider is used to access Active Directory Domain Services.</span></span> <span data-ttu-id="88338-124">LDAP 系結字串可採用下列其中一種形式：</span><span class="sxs-lookup"><span data-stu-id="88338-124">The LDAP binding string can take one of the following forms:</span></span>

-   <span data-ttu-id="88338-125">"LDAP:// <host name> / <object name> "</span><span class="sxs-lookup"><span data-stu-id="88338-125">"LDAP://<host name>/<object name>"</span></span>
-   <span data-ttu-id="88338-126">"GC:// <host name> / <object name> "</span><span class="sxs-lookup"><span data-stu-id="88338-126">"GC://<host name>/<object name>"</span></span>

<span data-ttu-id="88338-127">在上述範例中，"LDAP：" 會指定 LDAP 提供者。</span><span class="sxs-lookup"><span data-stu-id="88338-127">In the examples above, "LDAP:" specifies the LDAP provider.</span></span> <span data-ttu-id="88338-128">"GC：" 使用 LDAP 提供者系結至通用類別目錄服務，以執行快速查詢。</span><span class="sxs-lookup"><span data-stu-id="88338-128">"GC:" uses the LDAP provider to bind to the Global Catalog service to execute fast queries.</span></span>

<span data-ttu-id="88338-129">「 &lt; 主機名稱」 &gt; 會指定要系結的伺服器，而且是選擇性的。</span><span class="sxs-lookup"><span data-stu-id="88338-129">"&lt;host name&gt;" specifies the server to bind to and is optional.</span></span> <span data-ttu-id="88338-130">可能的話，請不要指定伺服器。</span><span class="sxs-lookup"><span data-stu-id="88338-130">If possible, do not specify a server.</span></span> <span data-ttu-id="88338-131">也可以系結至不同網域中的物件。</span><span class="sxs-lookup"><span data-stu-id="88338-131">It is also possible to bind to an object in a different domain.</span></span> <span data-ttu-id="88338-132">若要這樣做，請將網域命名系統 (DNS) 目標網域的名稱做為「 &lt; 主機名稱」 &gt; 。</span><span class="sxs-lookup"><span data-stu-id="88338-132">To do this pass the domain naming system (DNS) name of the target domain for "&lt;host name&gt;".</span></span> <span data-ttu-id="88338-133">例如，若要系結至 fabrikam.com 之 >domain2.contoso.com 網域中的 Users 容器，系結字串會是 "LDAP://domain2.fabrikam.com/CN=Users,DC=domain2,DC=fabrikam,DC=com"。</span><span class="sxs-lookup"><span data-stu-id="88338-133">For example, to bind to the Users container in the domain2 domain of fabrikam.com, the binding string would be "LDAP://domain2.fabrikam.com/CN=Users,DC=domain2,DC=fabrikam,DC=com".</span></span>

<span data-ttu-id="88338-134">「 &lt; 物件名稱」 &gt; 代表 Active Directory Domain Services 中的特定物件。</span><span class="sxs-lookup"><span data-stu-id="88338-134">"&lt;object name&gt;" represents a specific object in Active Directory Domain Services.</span></span> <span data-ttu-id="88338-135">物件名稱可以是辨別名稱或物件 GUID。</span><span class="sxs-lookup"><span data-stu-id="88338-135">The object name can be a distinguished name or an object GUID.</span></span>

<span data-ttu-id="88338-136">如需 LDAP 系結字串的詳細資訊，請參閱 [Ldap ADsPath](/windows/desktop/ADSI/ldap-adspath)。</span><span class="sxs-lookup"><span data-stu-id="88338-136">For more information about LDAP binding strings, see [LDAP ADsPath](/windows/desktop/ADSI/ldap-adspath).</span></span>

<span data-ttu-id="88338-137">針對 Windows NT 4.0，會使用 WinNT 提供者來存取目錄資料，例如使用者、使用者群組、電腦、服務，以及 Windows 2000 中的其他網路物件。</span><span class="sxs-lookup"><span data-stu-id="88338-137">For Windows NT 4.0, the WinNT provider is used for access to directory data such as users, user groups, computers, services, and other network objects in the Windows 2000.</span></span> <span data-ttu-id="88338-138">相較于 LDAP 提供者，Windows 2000 和更新版本系統上的 WinNT 提供者具有有限的功能。</span><span class="sxs-lookup"><span data-stu-id="88338-138">The WinNT provider on Windows 2000 and later systems has limited functionality compared to the LDAP provider.</span></span> <span data-ttu-id="88338-139">如需 WinNT 系結字串的詳細資訊，請參閱 [Winnt ADsPath](/windows/desktop/ADSI/winnt-adspath)。</span><span class="sxs-lookup"><span data-stu-id="88338-139">For more information about WinNT binding strings, see [WinNT ADsPath](/windows/desktop/ADSI/winnt-adspath).</span></span>

<span data-ttu-id="88338-140">"LDAP://" 或 "GC://" 的 ADsPath 可以用來系結至命名空間的根目錄。</span><span class="sxs-lookup"><span data-stu-id="88338-140">An ADsPath of "LDAP://" or "GC://" can be used to bind to the root of the namespace.</span></span> <span data-ttu-id="88338-141">系結至命名空間的根目錄時，所提供的命名空間物件不會包含任何屬性，而且會包含 LDAP 的網域物件和容器物件，其中包含樹系中所有網域的部分複本以進行 GC。</span><span class="sxs-lookup"><span data-stu-id="88338-141">When bound to the root of the namespace, the supplied namespace object contains no properties and contains the domain object for LDAP and a container object containing a partial replica of all domains in the forest for GC.</span></span>

<span data-ttu-id="88338-142">如需 Active Directory Domain Services 中系結的詳細資訊，請參閱：</span><span class="sxs-lookup"><span data-stu-id="88338-142">For more information about binding in Active Directory Domain Services, see:</span></span>

-   [<span data-ttu-id="88338-143">無伺服器系結和 RootDSE</span><span class="sxs-lookup"><span data-stu-id="88338-143">Serverless Binding and RootDSE</span></span>](serverless-binding-and-rootdse.md)
-   [<span data-ttu-id="88338-144">系結至通用類別目錄</span><span class="sxs-lookup"><span data-stu-id="88338-144">Binding to the Global Catalog</span></span>](binding-to-the-global-catalog.md)
-   [<span data-ttu-id="88338-145">使用 objectGUID 系結至物件</span><span class="sxs-lookup"><span data-stu-id="88338-145">Using objectGUID to Bind to an Object</span></span>](using-objectguid-to-bind-to-an-object.md)
-   [<span data-ttu-id="88338-146">使用 WKGUID 系結至 Well-Known 物件</span><span class="sxs-lookup"><span data-stu-id="88338-146">Binding to Well-Known Objects Using WKGUID</span></span>](binding-to-well-known-objects-using-wkguid.md)
-   [<span data-ttu-id="88338-147">使用 SID 系結至物件</span><span class="sxs-lookup"><span data-stu-id="88338-147">Binding to an Object Using a SID</span></span>](binding-to-an-object-using-a-sid.md)
-   [<span data-ttu-id="88338-148">使用 otherWellKnownObjects 屬性啟用 Rename-Safe 系結</span><span class="sxs-lookup"><span data-stu-id="88338-148">Enabling Rename-Safe Binding with the otherWellKnownObjects Property</span></span>](enabling-rename-safe-binding-with-the-otherwellknownobjects-property.md)
-   [<span data-ttu-id="88338-149">驗證</span><span class="sxs-lookup"><span data-stu-id="88338-149">Authentication</span></span>](authentication.md)

 

 
