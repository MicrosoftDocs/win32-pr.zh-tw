---
title: 使用者命名屬性
description: 使用者命名屬性會識別使用者物件，例如用於安全性目的的登入名稱和識別碼。
ms.assetid: 2192743c-cedd-4b03-a402-3992d64a4801
ms.tgt_platform: multiple
keywords:
- 使用者命名屬性 AD
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: a504070cf2e78cf5647072ff740d137b4a6e6056
ms.sourcegitcommit: 803f3ccd65bdefe36bd851b9c6e7280be9489016
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/17/2020
ms.locfileid: "103933053"
---
# <a name="user-naming-attributes"></a><span data-ttu-id="ee82f-104">使用者命名屬性</span><span class="sxs-lookup"><span data-stu-id="ee82f-104">User Naming Attributes</span></span>

<span data-ttu-id="ee82f-105">使用者命名屬性會識別使用者物件，例如用於安全性目的的登入名稱和識別碼。</span><span class="sxs-lookup"><span data-stu-id="ee82f-105">User naming attributes identify user objects, such as logon names and IDs used for security purposes.</span></span> <span data-ttu-id="ee82f-106">**Cn**、 **name** 和 **distinguishedName** 屬性都是使用者命名屬性的範例。</span><span class="sxs-lookup"><span data-stu-id="ee82f-106">The **cn**, **name**, and **distinguishedName** attributes are examples of user naming attributes.</span></span> <span data-ttu-id="ee82f-107">使用者物件是安全性主體物件，因此它也包含下列使用者命名屬性：</span><span class="sxs-lookup"><span data-stu-id="ee82f-107">A user object is a security principal object, so it also includes the following user naming attributes:</span></span>

-   <span data-ttu-id="ee82f-108">[userPrincipalName](#userprincipalname) —使用者的登入名稱</span><span class="sxs-lookup"><span data-stu-id="ee82f-108">[userPrincipalName](#userprincipalname) — the logon name for the user</span></span>
-   <span data-ttu-id="ee82f-109">[objectGUID](#objectguid) —使用者的唯一識別碼</span><span class="sxs-lookup"><span data-stu-id="ee82f-109">[objectGUID](#objectguid) — the unique identifier of a user</span></span>
-   <span data-ttu-id="ee82f-110">[sAMAccountName](#samaccountname) -支援舊版 Windows 的登入名稱</span><span class="sxs-lookup"><span data-stu-id="ee82f-110">[sAMAccountName](#samaccountname) — a logon name that supports previous version of Windows</span></span>
-   <span data-ttu-id="ee82f-111">[objectSid](#objectsid) -使用者的安全識別碼 (SID) </span><span class="sxs-lookup"><span data-stu-id="ee82f-111">[objectSid](#objectsid) — security identifier (SID) of the user</span></span>
-   <span data-ttu-id="ee82f-112">[sIDHistory](#sidhistory) ：使用者物件的先前 sid</span><span class="sxs-lookup"><span data-stu-id="ee82f-112">[sIDHistory](#sidhistory) — the previous SIDs for the user object</span></span>

> [!Note]  
> <span data-ttu-id="ee82f-113">您可以使用 [Active Directory 使用者和電腦] MMC 嵌入式管理單元來查看和管理這些屬性，該嵌入式管理單元可在 [遠端伺服器管理工具 (RSAT) ](https://www.microsoft.com/download/details.aspx?id=45520)中取得。</span><span class="sxs-lookup"><span data-stu-id="ee82f-113">You can view and manage these attributes using the Active Directory User and Computers MMC snap-in, which is available in the [Remote Server Administration Tools (RSAT)](https://www.microsoft.com/download/details.aspx?id=45520).</span></span>

 

## <a name="userprincipalname"></a><span data-ttu-id="ee82f-114">userPrincipalName</span><span class="sxs-lookup"><span data-stu-id="ee82f-114">userPrincipalName</span></span>

<span data-ttu-id="ee82f-115">**UserPrincipalName** 屬性是使用者的登入名稱。</span><span class="sxs-lookup"><span data-stu-id="ee82f-115">The **userPrincipalName** attribute is the logon name for the user.</span></span> <span data-ttu-id="ee82f-116">屬性是由 (UPN) 的使用者主體名稱所組成，這是最常見的 Windows 使用者登入名稱。</span><span class="sxs-lookup"><span data-stu-id="ee82f-116">The attribute consists of a user principal name (UPN), which is the most common logon name for Windows users.</span></span> <span data-ttu-id="ee82f-117">使用者通常會使用其 UPN 來登入網域。</span><span class="sxs-lookup"><span data-stu-id="ee82f-117">Users typically use their UPN to log on to a domain.</span></span> <span data-ttu-id="ee82f-118">這個屬性是單一值的索引字串。</span><span class="sxs-lookup"><span data-stu-id="ee82f-118">This attribute is an indexed string that is single-valued.</span></span>

<span data-ttu-id="ee82f-119">UPN 是使用者的網際網路樣式登入名稱，以網際網路標準 RFC 822 為基礎。</span><span class="sxs-lookup"><span data-stu-id="ee82f-119">A UPN is an Internet-style login name for a user based on the Internet standard RFC 822.</span></span> <span data-ttu-id="ee82f-120">UPN 比分辨名稱短，而且更容易記住。</span><span class="sxs-lookup"><span data-stu-id="ee82f-120">The UPN is shorter than a distinguished name and easier to remember.</span></span> <span data-ttu-id="ee82f-121">依照慣例，這應該對應到使用者的電子郵件名稱。</span><span class="sxs-lookup"><span data-stu-id="ee82f-121">By convention, this should map to the user's email name.</span></span> <span data-ttu-id="ee82f-122">UPN 的點是合併電子郵件和登入命名空間，讓使用者只需要記住單一名稱。</span><span class="sxs-lookup"><span data-stu-id="ee82f-122">The point of the UPN is to consolidate the email and logon namespaces so that the user only needs to remember a single name.</span></span>

### <a name="upn-format"></a><span data-ttu-id="ee82f-123">UPN 格式</span><span class="sxs-lookup"><span data-stu-id="ee82f-123">UPN Format</span></span>

<span data-ttu-id="ee82f-124">UPN 是由 UPN 前置詞 (使用者帳戶名稱) 和 UPN 尾碼 (DNS 網域名稱) 所組成。</span><span class="sxs-lookup"><span data-stu-id="ee82f-124">A UPN consists of a UPN prefix (the user account name) and a UPN suffix (a DNS domain name).</span></span> <span data-ttu-id="ee82f-125">前置詞會使用 \"\@\" 符號與尾碼連結。</span><span class="sxs-lookup"><span data-stu-id="ee82f-125">The prefix is joined with the suffix using the "@" symbol.</span></span> <span data-ttu-id="ee82f-126">例如，"someone@ example.com"。</span><span class="sxs-lookup"><span data-stu-id="ee82f-126">For example, "someone@ example.com".</span></span> <span data-ttu-id="ee82f-127">在目錄樹系的所有安全性主體物件之間，UPN 必須是唯一的。</span><span class="sxs-lookup"><span data-stu-id="ee82f-127">A UPN must be unique among all security principal objects within a directory forest.</span></span> <span data-ttu-id="ee82f-128">這表示可以重複使用 UPN 的前置詞，而不是使用相同的尾碼。</span><span class="sxs-lookup"><span data-stu-id="ee82f-128">This means the prefix of a UPN can be reused, just not with the same suffix.</span></span>

<span data-ttu-id="ee82f-129">UPN 尾碼具有下列限制：</span><span class="sxs-lookup"><span data-stu-id="ee82f-129">A UPN suffix has the following restrictions:</span></span>

-   <span data-ttu-id="ee82f-130">它必須是網域的 DNS 名稱，但不需要是包含使用者之網域的名稱。</span><span class="sxs-lookup"><span data-stu-id="ee82f-130">It must be the DNS name of a domain, but does not need to be the name of the domain that contains the user.</span></span>
-   <span data-ttu-id="ee82f-131">它必須是目前網域樹系中的網功能變數名稱稱，或是設定容器內分割區容器的 **upnSuffixes** 屬性中所列的替代名稱。</span><span class="sxs-lookup"><span data-stu-id="ee82f-131">It must be the name of a domain in the current domain forest, or an alternate name listed in the **upnSuffixes** attribute of the Partitions container within the Configuration container.</span></span>

### <a name="upn-management"></a><span data-ttu-id="ee82f-132">UPN 管理</span><span class="sxs-lookup"><span data-stu-id="ee82f-132">UPN Management</span></span>

<span data-ttu-id="ee82f-133">建立使用者帳戶時，可以指派 UPN 但不需要。</span><span class="sxs-lookup"><span data-stu-id="ee82f-133">A UPN can be assigned, but is not required, when a user account is created.</span></span> <span data-ttu-id="ee82f-134">建立 UPN 時，不會影響使用者物件的其他屬性變更（例如重新命名或移動的使用者）。</span><span class="sxs-lookup"><span data-stu-id="ee82f-134">When a UPN is created, it is unaffected by changes to other attributes of the user object such as the user being renamed or moved.</span></span> <span data-ttu-id="ee82f-135">這可讓使用者在重建目錄時保留相同的登入名稱。</span><span class="sxs-lookup"><span data-stu-id="ee82f-135">This allows the user to keep the same login name if a directory is restructured.</span></span> <span data-ttu-id="ee82f-136">不過，系統管理員可以變更 UPN。</span><span class="sxs-lookup"><span data-stu-id="ee82f-136">However, an administrator can change a UPN.</span></span> <span data-ttu-id="ee82f-137">當您建立新的使用者物件時，您應該檢查本機網域和通用類別目錄是否有建議的名稱，以確保它不存在。</span><span class="sxs-lookup"><span data-stu-id="ee82f-137">When you create a new user object, you should check the local domain and the global catalog for the proposed name to ensure it does not already exist.</span></span>

<span data-ttu-id="ee82f-138">當使用者使用 UPN 登入網域時，會藉由搜尋本機網域和通用類別目錄來驗證 UPN。</span><span class="sxs-lookup"><span data-stu-id="ee82f-138">When a user uses a UPN to log on to a domain, the UPN is validated by searching the local domain and then the global catalog.</span></span> <span data-ttu-id="ee82f-139">如果在通用類別目錄中找不到 UPN，則登入嘗試會失敗。</span><span class="sxs-lookup"><span data-stu-id="ee82f-139">If the UPN is not found in the global catalog, the logon attempt fails.</span></span>

## <a name="objectguid"></a><span data-ttu-id="ee82f-140">objectGUID</span><span class="sxs-lookup"><span data-stu-id="ee82f-140">objectGUID</span></span>

<span data-ttu-id="ee82f-141">**ObjectGUID** 屬性是使用者的唯一識別碼。</span><span class="sxs-lookup"><span data-stu-id="ee82f-141">The **objectGUID** attribute is the unique identifier of a user.</span></span> <span data-ttu-id="ee82f-142">屬性是單一值的128位全域唯一識別碼 (GUID) ，而且會儲存為 [**ADS \_ 八進位 \_ 字串**](/windows/win32/api/iads/ns-iads-ads_octet_string) 結構。</span><span class="sxs-lookup"><span data-stu-id="ee82f-142">The attribute is a single-valued 128-bit Globally Unique Identifier (GUID), and is stored as an [**ADS\_OCTET\_STRING**](/windows/win32/api/iads/ns-iads-ads_octet_string) structure.</span></span> <span data-ttu-id="ee82f-143">建立使用者物件時，Active Directory server 會建立 GUID。</span><span class="sxs-lookup"><span data-stu-id="ee82f-143">The GUID is created by the Active Directory server when a user object is created.</span></span>

<span data-ttu-id="ee82f-144">因為物件的辨別名稱會在物件重新命名或移動時發生變更，所以分辨名稱不是物件的可靠識別碼。</span><span class="sxs-lookup"><span data-stu-id="ee82f-144">Because an object's distinguished name changes if the object is renamed or moved, the distinguished name is not a reliable identifier of an object.</span></span> <span data-ttu-id="ee82f-145">在 Active Directory Domain Services 中，即使物件已重新命名或移動，物件的 **objectGUID** 屬性也永遠不會變更。</span><span class="sxs-lookup"><span data-stu-id="ee82f-145">In Active Directory Domain Services, an object's **objectGUID** attribute never changes, even if the object is renamed or moved.</span></span> <span data-ttu-id="ee82f-146">您可以在 [IADs 屬性方法](/windows/desktop/ADSI/iads-property-methods)中使用 **GUID** 屬性方法，以取出 **objectGUID** 的字串形式。</span><span class="sxs-lookup"><span data-stu-id="ee82f-146">You can retrieve the string form of the **objectGUID** using the **GUID** property method in [IADs Property Methods](/windows/desktop/ADSI/iads-property-methods).</span></span>

## <a name="samaccountname"></a><span data-ttu-id="ee82f-147">sAMAccountName</span><span class="sxs-lookup"><span data-stu-id="ee82f-147">sAMAccountName</span></span>

<span data-ttu-id="ee82f-148">**SAMAccountName** 屬性是用來支援舊版 Windows 用戶端和伺服器的登入名稱，例如 Windows NT 4.0、windows 95、windows 98 和 LAN Manager。</span><span class="sxs-lookup"><span data-stu-id="ee82f-148">The **sAMAccountName** attribute is a logon name used to support clients and servers from previous version of Windows, such as Windows NT 4.0, Windows 95, Windows 98, and LAN Manager.</span></span> <span data-ttu-id="ee82f-149">登入名稱必須少於或等於20個字元，而且在網域內的所有安全性主體物件中都是唯一的。</span><span class="sxs-lookup"><span data-stu-id="ee82f-149">The logon name must be 20 or fewer characters and be unique among all security principal objects within the domain.</span></span>

## <a name="objectsid"></a><span data-ttu-id="ee82f-150">objectSid</span><span class="sxs-lookup"><span data-stu-id="ee82f-150">objectSid</span></span>

<span data-ttu-id="ee82f-151">**ObjectSid** 屬性是使用者 (SID) 的安全識別碼。</span><span class="sxs-lookup"><span data-stu-id="ee82f-151">The **objectSid** attribute is the security identifier (SID) of the user.</span></span> <span data-ttu-id="ee82f-152">在與 Windows 安全性互動期間，系統會使用 SID 來識別使用者及其群組成員資格。</span><span class="sxs-lookup"><span data-stu-id="ee82f-152">The SID is used by the system to identify a user and their group memberships during interactions with Windows security.</span></span> <span data-ttu-id="ee82f-153">屬性是單一值。</span><span class="sxs-lookup"><span data-stu-id="ee82f-153">The attribute is single-valued.</span></span> <span data-ttu-id="ee82f-154">SID 是唯一的二進位值，用來將使用者識別為安全性主體。</span><span class="sxs-lookup"><span data-stu-id="ee82f-154">The SID is a unique binary value used to identify the user as a security principal.</span></span>

<span data-ttu-id="ee82f-155">建立使用者時，系統會設定 SID。</span><span class="sxs-lookup"><span data-stu-id="ee82f-155">The SID is set by the system when the user is created.</span></span> <span data-ttu-id="ee82f-156">每個使用者都有一個由 Windows 網域發出的唯一 SID，並儲存在目錄中使用者物件的 **objectSid** 屬性中。</span><span class="sxs-lookup"><span data-stu-id="ee82f-156">Each user has a unique SID issued by a Windows domain and stored in the **objectSid** attribute of the user object in the directory.</span></span> <span data-ttu-id="ee82f-157">每次使用者登入時，系統會從目錄抓取使用者的 SID，並將其放在使用者的存取權杖中。</span><span class="sxs-lookup"><span data-stu-id="ee82f-157">Each time a user logs on, the system retrieves the user's SID from the directory and places it in the user's access token.</span></span> <span data-ttu-id="ee82f-158">使用者的 SID 也會用來取得使用者所屬群組的 Sid，並將其放在使用者的存取權杖中。</span><span class="sxs-lookup"><span data-stu-id="ee82f-158">The user's SID is also used to retrieve the SIDs for the groups of which the user is a member and places them in the user's access token.</span></span> <span data-ttu-id="ee82f-159">使用 SID 做為使用者或群組的唯一識別碼時，無法再次使用它來識別另一個使用者或群組。</span><span class="sxs-lookup"><span data-stu-id="ee82f-159">When a SID has been used as the unique identifier for a user or group, it cannot be used again to identify another user or group.</span></span>

## <a name="sidhistory"></a><span data-ttu-id="ee82f-160">sIDHistory</span><span class="sxs-lookup"><span data-stu-id="ee82f-160">sIDHistory</span></span>

<span data-ttu-id="ee82f-161">**SIDHistory** 屬性包含使用者物件先前的 sid。</span><span class="sxs-lookup"><span data-stu-id="ee82f-161">The **sIDHistory** attribute contains the previous SIDs for the user object.</span></span> <span data-ttu-id="ee82f-162">這是多重值的屬性。</span><span class="sxs-lookup"><span data-stu-id="ee82f-162">This is a multi-valued attribute.</span></span> <span data-ttu-id="ee82f-163">如果使用者已移至另一個網域，則使用者物件具有先前的 Sid。</span><span class="sxs-lookup"><span data-stu-id="ee82f-163">A user object has previous SIDs if the user was moved to another domain.</span></span> <span data-ttu-id="ee82f-164">只要將使用者物件移至新的網域，就會建立新的 SID 並指派 **objectSid** 屬性，並將先前的 sid 新增至 **sIDHistory** 屬性。</span><span class="sxs-lookup"><span data-stu-id="ee82f-164">Whenever a user object is moved to a new domain, a new SID is created and assigned the **objectSid** attribute, and the previous SID is added to the **sIDHistory** attribute.</span></span>

## <a name="related-topics"></a><span data-ttu-id="ee82f-165">相關主題</span><span class="sxs-lookup"><span data-stu-id="ee82f-165">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="ee82f-166">User 物件屬性</span><span class="sxs-lookup"><span data-stu-id="ee82f-166">User Object Attributes</span></span>](user-object-attributes.md)
</dt> </dl>

 

 