---
title: 使用 Active Directory 網域服務
description: 本節提供撰寫應用程式的指導方針，這些應用程式會使用或發佈 Active Directory 目錄服務中的資料。
ms.assetid: 2ae20169-08a5-4e15-8430-ea99a917725f
ms.tgt_platform: multiple
keywords:
- Active Directory Active Directory，使用
- Active Directory Domain Services Active Directory，使用
- Active Directory 範例 Active Directory
- Active Directory Domain Services 範例 Active Directory
- 範例 Active Directory
- Active Directory Active Directory 的範例，請參閱 Active Directory Domain Services 範例
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 540b9004311db320decbd15c4f0a29e52ec1302a
ms.sourcegitcommit: 773fa6257ead6c74154ad3cf46d21e49adc900aa
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 09/09/2020
ms.locfileid: "103684169"
---
# <a name="using-active-directory-domain-services"></a><span data-ttu-id="13f04-109">使用 Active Directory 網域服務</span><span class="sxs-lookup"><span data-stu-id="13f04-109">Using Active Directory Domain Services</span></span>

<span data-ttu-id="13f04-110">本節提供撰寫應用程式的指導方針，這些應用程式會使用或發佈 Active Directory 目錄服務中的資料。</span><span class="sxs-lookup"><span data-stu-id="13f04-110">This section provides guidelines for writing applications that use or publish data in an Active Directory directory service.</span></span>

> [!Note]  
> <span data-ttu-id="13f04-111">下列檔適用于電腦程式設計人員。</span><span class="sxs-lookup"><span data-stu-id="13f04-111">The following documentation is for computer programmers.</span></span> <span data-ttu-id="13f04-112">如果您嘗試解決 Active Directory 首頁列印錯誤，請參閱 Microsoft 社區頁面的 [下列建議](https://answers.microsoft.com/windows/forum/all/clicking-find-printer-shows-error-the-active/52bfd961-ff62-4397-b8cf-a0708f0cb3d2) ：如果沒有説明，請嘗試從 [TechNet](https://social.technet.microsoft.com/Forums/windowsserver/d6212275-24d6-4168-830a-9441f861cb76/error-message-when-attempting-to-print-active-directory-domain-service-is-currently-unavailable?forum=winserverprint)提出這些建議。</span><span class="sxs-lookup"><span data-stu-id="13f04-112">If you are trying to resolve an Active Directory home printing error, see the [following suggestion](https://answers.microsoft.com/windows/forum/all/clicking-find-printer-shows-error-the-active/52bfd961-ff62-4397-b8cf-a0708f0cb3d2) from the Microsoft community pages; if that doesn't help, try these recommendations from [TechNet](https://social.technet.microsoft.com/Forums/windowsserver/d6212275-24d6-4168-830a-9441f861cb76/error-message-when-attempting-to-print-active-directory-domain-service-is-currently-unavailable?forum=winserverprint).</span></span>

 

<span data-ttu-id="13f04-113">Active Directory Domain Services 符合輕量型目錄存取協定3.0 （由 RFC 2251 和其他 Rfc 所定義）。</span><span class="sxs-lookup"><span data-stu-id="13f04-113">Active Directory Domain Services are compliant with Lightweight Directory Access Protocol 3.0, which is defined by RFC 2251 and other RFCs.</span></span> <span data-ttu-id="13f04-114">您可以使用下列任何 API 集合來存取 Active Directory Domain Services。</span><span class="sxs-lookup"><span data-stu-id="13f04-114">Any of the following API sets can be used to access Active Directory Domain Services.</span></span> <span data-ttu-id="13f04-115">每個 API 集合都有優缺點，取決於程式設計語言、程式設計環境和預定的執行方法。</span><span class="sxs-lookup"><span data-stu-id="13f04-115">Each API set has advantages and disadvantages that depend on the programming language, programming environment, and intended method of execution.</span></span> <span data-ttu-id="13f04-116">本指南中的大部分範例都會使用「ADSI」（C 和 c + + 等語言所支援的）以及符合自動化規範的語言，例如 Microsoft Visual Basic 和 Visual Basic Scripting Edition。</span><span class="sxs-lookup"><span data-stu-id="13f04-116">The majority of the examples in this guide use ADSI, which is supported by languages such as C and C++, as well as automation-compliant languages such as Microsoft Visual Basic and Visual Basic Scripting Edition.</span></span>

<span data-ttu-id="13f04-117">如需特定 Active Directory Domain Services 技術的詳細資訊，請參閱：</span><span class="sxs-lookup"><span data-stu-id="13f04-117">For more information about specific Active Directory Domain Services technologies, see:</span></span>

-   [<span data-ttu-id="13f04-118">輕量型目錄存取協定</span><span class="sxs-lookup"><span data-stu-id="13f04-118">Lightweight Directory Access Protocol</span></span>](/previous-versions/windows/desktop/ldap/lightweight-directory-access-protocol-ldap-api)
-   [<span data-ttu-id="13f04-119">Active Directory 服務介面</span><span class="sxs-lookup"><span data-stu-id="13f04-119">Active Directory Service Interfaces</span></span>](../adsi/active-directory-service-interfaces-adsi.md)
-   [<span data-ttu-id="13f04-120">System.DirectoryServices</span><span class="sxs-lookup"><span data-stu-id="13f04-120">System.DirectoryServices</span></span>](/dotnet/api/system.directoryservices)

<span data-ttu-id="13f04-121">本節將討論下列主題：</span><span class="sxs-lookup"><span data-stu-id="13f04-121">This section discusses the following topics:</span></span>

-   [<span data-ttu-id="13f04-122">系結至 Active Directory Domain Services</span><span class="sxs-lookup"><span data-stu-id="13f04-122">Binding to Active Directory Domain Services</span></span>](binding-to-active-directory-domain-services.md)
-   [<span data-ttu-id="13f04-123">在 Active Directory Domain Services 中搜尋</span><span class="sxs-lookup"><span data-stu-id="13f04-123">Searching in Active Directory Domain Services</span></span>](searching-in-active-directory-domain-services.md)
-   [<span data-ttu-id="13f04-124">在 Active Directory Domain Services 中建立和刪除物件</span><span class="sxs-lookup"><span data-stu-id="13f04-124">Creating and Deleting Objects in Active Directory Domain Services</span></span>](creating-and-deleting-objects-in-active-directory-domain-services.md)
-   [<span data-ttu-id="13f04-125">移動物件</span><span class="sxs-lookup"><span data-stu-id="13f04-125">Moving Objects</span></span>](moving-objects.md)
-   [<span data-ttu-id="13f04-126">在 Active Directory Domain Services 中讀取和寫入物件的屬性</span><span class="sxs-lookup"><span data-stu-id="13f04-126">Reading and Writing Attributes of Objects in Active Directory Domain Services</span></span>](reading-and-writing-attributes-of-objects-in-active-directory-domain-services.md)
-   [<span data-ttu-id="13f04-127">控制 Active Directory Domain Services 中的物件存取</span><span class="sxs-lookup"><span data-stu-id="13f04-127">Controlling Access to Objects in Active Directory Domain Services</span></span>](controlling-access-to-objects-in-active-directory-domain-services.md)
-   [<span data-ttu-id="13f04-128">擴充架構</span><span class="sxs-lookup"><span data-stu-id="13f04-128">Extending the Schema</span></span>](extending-the-schema.md)
-   [<span data-ttu-id="13f04-129">擴充目錄物件的消費者介面</span><span class="sxs-lookup"><span data-stu-id="13f04-129">Extending the User Interface for Directory Objects</span></span>](extending-the-user-interface-for-directory-objects.md)
-   [<span data-ttu-id="13f04-130">管理使用者</span><span class="sxs-lookup"><span data-stu-id="13f04-130">Managing Users</span></span>](managing-users.md)
-   [<span data-ttu-id="13f04-131">管理群組</span><span class="sxs-lookup"><span data-stu-id="13f04-131">Managing Groups</span></span>](managing-groups.md)
-   [<span data-ttu-id="13f04-132">追蹤變更</span><span class="sxs-lookup"><span data-stu-id="13f04-132">Tracking Changes</span></span>](tracking-changes.md)
-   [<span data-ttu-id="13f04-133">服務發行</span><span class="sxs-lookup"><span data-stu-id="13f04-133">Service Publication</span></span>](service-publication.md)
-   [<span data-ttu-id="13f04-134">服務登入帳戶</span><span class="sxs-lookup"><span data-stu-id="13f04-134">Service Logon Accounts</span></span>](service-logon-accounts.md)
-   [<span data-ttu-id="13f04-135">使用 Kerberos 進行相互驗證</span><span class="sxs-lookup"><span data-stu-id="13f04-135">Mutual Authentication Using Kerberos</span></span>](mutual-authentication-using-kerberos.md)
-   [<span data-ttu-id="13f04-136">備份與還原 Active Directory</span><span class="sxs-lookup"><span data-stu-id="13f04-136">Backing Up and Restoring Active Directory</span></span>](backing-up-and-restoring-an-active-directory-server.md)
-   [<span data-ttu-id="13f04-137">儲存動態資料</span><span class="sxs-lookup"><span data-stu-id="13f04-137">Storing Dynamic Data</span></span>](storing-dynamic-data.md)
-   [<span data-ttu-id="13f04-138">應用程式目錄分割</span><span class="sxs-lookup"><span data-stu-id="13f04-138">Application Directory Partitions</span></span>](application-directory-partitions.md)
-   [<span data-ttu-id="13f04-139">偵測網域的操作模式</span><span class="sxs-lookup"><span data-stu-id="13f04-139">Detecting the Operation Mode of a Domain</span></span>](detecting-the-operation-mode-of-a-domain.md)

 

 