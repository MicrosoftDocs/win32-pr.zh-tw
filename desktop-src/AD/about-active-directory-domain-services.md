---
title: 關於 Active Directory Domain Services
description: 本指南提供在針對支援 Active Directory 的作業系統設計的分散式應用程式中整合 Microsoft Active Directory 的基本資訊。
ms.assetid: cc6c63dd-ae22-40a7-8312-0a4648bb92bd
ms.tgt_platform: multiple
keywords:
- Active Directory Active Directory，關於
- Active Directory Domain Services Active Directory，關於
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 4d8dafb89533d796f0651ad08b913eacda1d0fe9
ms.sourcegitcommit: 592c9bbd22ba69802dc353bcb5eb30699f9e9403
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/20/2020
ms.locfileid: "104023520"
---
# <a name="about-active-directory-domain-services"></a><span data-ttu-id="70cc8-105">關於 Active Directory Domain Services</span><span class="sxs-lookup"><span data-stu-id="70cc8-105">About Active Directory Domain Services</span></span>

## <a name="writing-powerful-applications-that-use-active-directory-domain-services"></a><span data-ttu-id="70cc8-106">撰寫使用 Active Directory Domain Services 的強大應用程式</span><span class="sxs-lookup"><span data-stu-id="70cc8-106">Writing Powerful Applications that Use Active Directory Domain Services</span></span>

<span data-ttu-id="70cc8-107">本指南提供在針對支援 Active Directory Domain Services 的作業系統設計的分散式應用程式中整合 Active Directory Domain Services 的基本資訊，包括：</span><span class="sxs-lookup"><span data-stu-id="70cc8-107">This guide provides essential information for integrating Active Directory Domain Services in distributed applications designed for operating systems that support Active Directory Domain Services, including:</span></span>

-   <span data-ttu-id="70cc8-108">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="70cc8-108">Windows Server 2008</span></span>
-   <span data-ttu-id="70cc8-109">Windows Server 2008 R2</span><span class="sxs-lookup"><span data-stu-id="70cc8-109">Windows Server 2008 R2</span></span>
-   <span data-ttu-id="70cc8-110">Windows Server 2012</span><span class="sxs-lookup"><span data-stu-id="70cc8-110">Windows Server 2012</span></span>
-   <span data-ttu-id="70cc8-111">Windows Server 2012 R2</span><span class="sxs-lookup"><span data-stu-id="70cc8-111">Windows Server 2012 R2</span></span>
-   <span data-ttu-id="70cc8-112">Windows Server 2016</span><span class="sxs-lookup"><span data-stu-id="70cc8-112">Windows Server 2016</span></span>

> [!Note]  
> <span data-ttu-id="70cc8-113">這些主題適用于軟體發展人員。</span><span class="sxs-lookup"><span data-stu-id="70cc8-113">These topics are for software developers.</span></span> <span data-ttu-id="70cc8-114">如需支援問題，請參閱 [Microsoft 支援服務](https://windows.microsoft.com/windows/support#1tc)。</span><span class="sxs-lookup"><span data-stu-id="70cc8-114">For support issues, see [Microsoft Support](https://windows.microsoft.com/windows/support#1tc).</span></span> <span data-ttu-id="70cc8-115">如需管理 Active Directory 的詳細資訊，請參閱 TechNet 上的 [Active Directory Domain Services](/previous-versions/windows/it-pro/windows-server-2008-R2-and-2008/cc770946(v=ws.10)) 。</span><span class="sxs-lookup"><span data-stu-id="70cc8-115">For information about administering Active Directory, see [Active Directory Domain Services](/previous-versions/windows/it-pro/windows-server-2008-R2-and-2008/cc770946(v=ws.10)) at TechNet.</span></span>

 

## <a name="fundamental-directory-features"></a><span data-ttu-id="70cc8-116">基本目錄功能</span><span class="sxs-lookup"><span data-stu-id="70cc8-116">Fundamental Directory Features</span></span>

<span data-ttu-id="70cc8-117">目錄服務是分散式應用程式的基礎服務。</span><span class="sxs-lookup"><span data-stu-id="70cc8-117">A directory service is a fundamental service for distributed applications.</span></span> <span data-ttu-id="70cc8-118">目錄服務必須提供下表所列的功能。</span><span class="sxs-lookup"><span data-stu-id="70cc8-118">A directory service must provide the features listed in the following table.</span></span>



| <span data-ttu-id="70cc8-119">功能</span><span class="sxs-lookup"><span data-stu-id="70cc8-119">Feature</span></span>               | <span data-ttu-id="70cc8-120">描述</span><span class="sxs-lookup"><span data-stu-id="70cc8-120">Description</span></span>                                                                                         |
|-----------------------|-----------------------------------------------------------------------------------------------------|
| <span data-ttu-id="70cc8-121">位置透明度</span><span class="sxs-lookup"><span data-stu-id="70cc8-121">Location transparency</span></span> | <span data-ttu-id="70cc8-122">能夠在沒有物件位址的情況下尋找使用者、群組、網路服務或資源的資料</span><span class="sxs-lookup"><span data-stu-id="70cc8-122">Able to find user, group, networked service, or resource, data without the object address</span></span>           |
| <span data-ttu-id="70cc8-123">物件資料</span><span class="sxs-lookup"><span data-stu-id="70cc8-123">Object data</span></span>           | <span data-ttu-id="70cc8-124">能夠在階層式樹狀結構中儲存使用者、群組、組織和服務資料</span><span class="sxs-lookup"><span data-stu-id="70cc8-124">Able to store user, group, organization, and service data in a hierarchical tree</span></span>                    |
| <span data-ttu-id="70cc8-125">豐富查詢</span><span class="sxs-lookup"><span data-stu-id="70cc8-125">Rich query</span></span>            | <span data-ttu-id="70cc8-126">藉由查詢物件屬性來尋找物件</span><span class="sxs-lookup"><span data-stu-id="70cc8-126">Able to locate an object by querying for object properties</span></span>                                          |
| <span data-ttu-id="70cc8-127">高可用性</span><span class="sxs-lookup"><span data-stu-id="70cc8-127">High availability</span></span>     | <span data-ttu-id="70cc8-128">能夠在可有效率地讀取/寫入作業的位置找出目錄的複本</span><span class="sxs-lookup"><span data-stu-id="70cc8-128">Able to locate a replica of the directory at a location that is efficient for read/write operations</span></span> |



 

## <a name="advanced-features-of-active-directory-domain-services"></a><span data-ttu-id="70cc8-129">Active Directory Domain Services 的 Advanced 功能</span><span class="sxs-lookup"><span data-stu-id="70cc8-129">Advanced Features of Active Directory Domain Services</span></span>

<span data-ttu-id="70cc8-130">Active Directory Domain Services 提供下表所列的功能。</span><span class="sxs-lookup"><span data-stu-id="70cc8-130">Active Directory Domain Services provides the features listed in the following table.</span></span>



<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<thead>
<tr class="header">
<th><span data-ttu-id="70cc8-131">功能</span><span class="sxs-lookup"><span data-stu-id="70cc8-131">Feature</span></span></th>
<th><span data-ttu-id="70cc8-132">描述</span><span class="sxs-lookup"><span data-stu-id="70cc8-132">Description</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><span data-ttu-id="70cc8-133">網際網路標準的支援</span><span class="sxs-lookup"><span data-stu-id="70cc8-133">Support for Internet standards</span></span></td>
<td><span data-ttu-id="70cc8-134">Active Directory Domain Services 會根據已發佈的網際網路標準（例如 LDAP 和 DNS）來實行其功能。</span><span class="sxs-lookup"><span data-stu-id="70cc8-134">Active Directory Domain Services implements its features in accordance with published Internet standards such as LDAP and DNS.</span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="70cc8-135">緊密整合且彈性的安全性</span><span class="sxs-lookup"><span data-stu-id="70cc8-135">Tightly integrated and flexible security</span></span></td>
<td><span data-ttu-id="70cc8-136">優點包括︰</span><span class="sxs-lookup"><span data-stu-id="70cc8-136">Advantages include:</span></span><br/>
<ul>
<li><span data-ttu-id="70cc8-137">選擇驗證套件。</span><span class="sxs-lookup"><span data-stu-id="70cc8-137">Choice of authentication packages.</span></span> <span data-ttu-id="70cc8-138">Kerberos、安全通訊端層 (SSL) 或組合;例如，建立用於加密的 SSL 通道，然後使用 Kerberos 進行驗證。</span><span class="sxs-lookup"><span data-stu-id="70cc8-138">Kerberos, Secure Sockets Layer (SSL), or a combination; for example, establish an SSL channel for encryption and then use Kerberos for authentication.</span></span></li>
<li><span data-ttu-id="70cc8-139">使用 Active Directory Domain Services 中的使用者和群組，集中管理服務和資源存取。</span><span class="sxs-lookup"><span data-stu-id="70cc8-139">Central management of service and resource access by using the users and groups in Active Directory Domain Services.</span></span></li>
<li><span data-ttu-id="70cc8-140">管理委派，讓中央系統管理員可以委派系統管理工作，例如密碼變更或特定物件的建立和刪除。</span><span class="sxs-lookup"><span data-stu-id="70cc8-140">Delegation of administration so that central administrators can delegate administrative tasks such as password changing or specific object creation and deletion.</span></span></li>
<li><span data-ttu-id="70cc8-141">Active Directory 伺服器在 Windows 作業系統的檔案系統上使用相同的存取控制機制。</span><span class="sxs-lookup"><span data-stu-id="70cc8-141">The Active Directory server uses the same access control mechanisms used on file systems in the Windows operating systems.</span></span> <span data-ttu-id="70cc8-142">因此，在檔案系統上管理存取控制的相同工具也適用于 Active Directory Domain Services。</span><span class="sxs-lookup"><span data-stu-id="70cc8-142">Thus, the same tools that manage access control on a file system work for Active Directory Domain Services.</span></span></li>
<li><span data-ttu-id="70cc8-143">全方位的公開金鑰基礎結構。</span><span class="sxs-lookup"><span data-stu-id="70cc8-143">Comprehensive Public Key infrastructure.</span></span> <span data-ttu-id="70cc8-144">Microsoft 憑證伺服器和智慧卡支援已與 Active Directory Domain Services 整合，以提供智慧卡登入和憑證管理。</span><span class="sxs-lookup"><span data-stu-id="70cc8-144">The Microsoft Certificate Server and Smart Card support are integrated with Active Directory Domain Services to provide Smart Card logon and Certificate management.</span></span></li>
</ul></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="70cc8-145">容易程式化</span><span class="sxs-lookup"><span data-stu-id="70cc8-145">Easily programmable</span></span></td>
<td><span data-ttu-id="70cc8-146">您可以使用 <a href="/windows/desktop/ADSI/active-directory-service-interfaces-adsi">Active Directory 服務介面</a> Api、 <a href="/previous-versions/windows/desktop/ldap/lightweight-directory-access-protocol-ldap-api">輕量型目錄存取協定</a> api 或 <a href="/dotnet/api/system.directoryservices">DirectoryServices</a> 命名空間，以程式設計方式存取和管理 Active Directory 伺服器。</span><span class="sxs-lookup"><span data-stu-id="70cc8-146">The Active Directory server can be programmatically accessed and administered using the <a href="/windows/desktop/ADSI/active-directory-service-interfaces-adsi">Active Directory Service Interfaces</a> API, <a href="/previous-versions/windows/desktop/ldap/lightweight-directory-access-protocol-ldap-api">Lightweight Directory Access Protocol</a> API, or the <a href="/dotnet/api/system.directoryservices">System.DirectoryServices</a> namespace.</span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="70cc8-147">啟用目錄的系統服務</span><span class="sxs-lookup"><span data-stu-id="70cc8-147">Directory enabled system services</span></span></td>
<td><span data-ttu-id="70cc8-148">您可以藉由建立 Windows Installer 套件，並使用 Windows 作業系統中提供的應用程式部署功能，輕鬆地將您的用戶端應用程式部署到分散式桌面。</span><span class="sxs-lookup"><span data-stu-id="70cc8-148">Your client application can be easily deployed to distributed desktops by creating a Windows Installer package and using the application deployment feature available in the Windows operating systems.</span></span></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="70cc8-149">主要應用程式整合</span><span class="sxs-lookup"><span data-stu-id="70cc8-149">Key application integration</span></span></td>
<td><span data-ttu-id="70cc8-150">重要的分散式應用程式（例如 Exchange）會與 Active Directory Domain Services 整合。</span><span class="sxs-lookup"><span data-stu-id="70cc8-150">Key distributed applications, such as Exchange, are integrated with Active Directory Domain Services.</span></span> <span data-ttu-id="70cc8-151">因此，公司可以減少要管理的目錄服務數目。</span><span class="sxs-lookup"><span data-stu-id="70cc8-151">Thus, companies can reduce the number of directory services to be managed.</span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="70cc8-152">豐富且可擴充的架構</span><span class="sxs-lookup"><span data-stu-id="70cc8-152">Rich and extensible schema</span></span></td>
<td><span data-ttu-id="70cc8-153">架構會定義可寫入和讀取目錄服務的物件和屬性。</span><span class="sxs-lookup"><span data-stu-id="70cc8-153">The schema defines what objects and properties can be written and read from a directory service.</span></span> <span data-ttu-id="70cc8-154">Active Directory 的架構很豐富。</span><span class="sxs-lookup"><span data-stu-id="70cc8-154">The Active Directory Schema is rich.</span></span> <span data-ttu-id="70cc8-155">服務需要的大部分物件和屬性都可以使用。</span><span class="sxs-lookup"><span data-stu-id="70cc8-155">Most of the objects and properties a service requires are available.</span></span> <span data-ttu-id="70cc8-156">如果沒有，分散式應用程式可以擴充架構以支援應用程式需求。</span><span class="sxs-lookup"><span data-stu-id="70cc8-156">If not, a distributed application can extend the schema to support the application requirements.</span></span></td>
</tr>
</tbody>
</table>



 

<span data-ttu-id="70cc8-157">如需 Active Directory Domain Services 的詳細資訊，請參閱：</span><span class="sxs-lookup"><span data-stu-id="70cc8-157">For more information about Active Directory Domain Services, see:</span></span>

-   [<span data-ttu-id="70cc8-158">Active Directory Domain Services 的核心概念</span><span class="sxs-lookup"><span data-stu-id="70cc8-158">Core Concepts of Active Directory Domain Services</span></span>](core-concepts-of-active-directory-domain-services.md)
-   [<span data-ttu-id="70cc8-159">Active Directory 架構</span><span class="sxs-lookup"><span data-stu-id="70cc8-159">Active Directory Architecture</span></span>](active-directory-domain-services-architecture.md)
-   [<span data-ttu-id="70cc8-160">Active Directory 架構</span><span class="sxs-lookup"><span data-stu-id="70cc8-160">Active Directory Schema</span></span>](active-directory-schema.md)

