---
title: Active Directory 網域服務
description: Microsoft Active Directory Domain Services 是以 Windows 2000 Server、Windows Server 2003 以及使用網域控制站的 Microsoft Windows Server 2008 作業系統為基礎的分散式網路基礎。
ms.assetid: 9fc78c72-c59c-4c4d-ace5-00a431645c4b
ms.tgt_platform: multiple
keywords:
- Active Directory Domain Services Active Directory
- Active Directory Active Directory、起始頁
- Active Directory Domain Services Active Directory、起始頁
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 0270f331a68d23ad89a8e5a999f8cabd95487020
ms.sourcegitcommit: 73417d55867c804274a55abe5ca71bcba7006119
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 10/20/2020
ms.locfileid: "104024296"
---
# <a name="active-directory-domain-services"></a><span data-ttu-id="b7e1f-106">Active Directory Domain Services</span><span class="sxs-lookup"><span data-stu-id="b7e1f-106">Active Directory Domain Services</span></span>

## <a name="purpose"></a><span data-ttu-id="b7e1f-107">目的</span><span class="sxs-lookup"><span data-stu-id="b7e1f-107">Purpose</span></span>

<span data-ttu-id="b7e1f-108">Microsoft Active Directory Domain Services 是以 Windows 2000 Server、Windows Server 2003 以及使用網域控制站的 Microsoft Windows Server 2008 作業系統為基礎的分散式網路基礎。</span><span class="sxs-lookup"><span data-stu-id="b7e1f-108">Microsoft Active Directory Domain Services are the foundation for distributed networks built on Windows 2000 Server, Windows Server 2003 and Microsoft Windows Server 2008 operating systems that use domain controllers.</span></span> <span data-ttu-id="b7e1f-109">Active Directory Domain Services 針對網路中的物件（例如使用者、電腦、印表機和服務），提供安全、結構化、階層式的資料存放區。</span><span class="sxs-lookup"><span data-stu-id="b7e1f-109">Active Directory Domain Services provide secure, structured, hierarchical data storage for objects in a network such as users, computers, printers, and services.</span></span> <span data-ttu-id="b7e1f-110">Active Directory Domain Services 提供尋找和使用這些物件的支援。</span><span class="sxs-lookup"><span data-stu-id="b7e1f-110">Active Directory Domain Services provide support for locating and working with these objects.</span></span>

<span data-ttu-id="b7e1f-111">本指南概述基本工作的 Active Directory Domain Services 和範例程式碼，例如搜尋物件和讀取屬性，到更先進的工作，例如服務發行。</span><span class="sxs-lookup"><span data-stu-id="b7e1f-111">This guide provides an overview of Active Directory Domain Services and sample code for basic tasks, such as searching for objects and reading properties, to more advanced tasks such as service publication.</span></span>

<span data-ttu-id="b7e1f-112">Windows 2000 伺服器和更新版本的作業系統提供使用者介面，讓使用者和系統管理員使用 Active Directory Domain Services 中的物件和資料。</span><span class="sxs-lookup"><span data-stu-id="b7e1f-112">Windows 2000 Server and later operating systems provide a user interface for users and administrators to work with the objects and data in Active Directory Domain Services.</span></span> <span data-ttu-id="b7e1f-113">本指南說明如何擴充和自訂該使用者介面。</span><span class="sxs-lookup"><span data-stu-id="b7e1f-113">This guide describes how to extend and customize that user interface.</span></span> <span data-ttu-id="b7e1f-114">它也會描述如何藉由定義新的物件類別和屬性來擴充 Active Directory Domain Services。</span><span class="sxs-lookup"><span data-stu-id="b7e1f-114">It also describes how to extend Active Directory Domain Services by defining new object classes and attributes.</span></span>

> [!Note]  
> <span data-ttu-id="b7e1f-115">下列檔適用于電腦程式設計人員。</span><span class="sxs-lookup"><span data-stu-id="b7e1f-115">The following documentation is for computer programmers.</span></span> <span data-ttu-id="b7e1f-116">如果您是嘗試偵測列印錯誤或家用網路問題的使用者，請參閱 [Microsoft 社區論壇](https://answers.microsoft.com)。</span><span class="sxs-lookup"><span data-stu-id="b7e1f-116">If you are an end-user trying to debug a printing error or home network issue, see the [Microsoft community forums](https://answers.microsoft.com).</span></span>

 

## <a name="where-applicable"></a><span data-ttu-id="b7e1f-117">適用時</span><span class="sxs-lookup"><span data-stu-id="b7e1f-117">Where applicable</span></span>

<span data-ttu-id="b7e1f-118">網路系統管理員撰寫可存取 Active Directory Domain Services 的腳本和應用程式，以自動化一般管理工作，例如新增使用者和群組、管理印表機，以及設定網路資源的許可權。</span><span class="sxs-lookup"><span data-stu-id="b7e1f-118">Network administrators write scripts and applications that access Active Directory Domain Services to automate common administrative tasks, such as adding users and groups, managing printers, and setting permissions for network resources.</span></span>

<span data-ttu-id="b7e1f-119">獨立軟體廠商和使用者開發人員可以使用 Active Directory Domain Services 程式設計，以目錄啟用其產品和應用程式。</span><span class="sxs-lookup"><span data-stu-id="b7e1f-119">Independent software vendors and end-user developers can use Active Directory Domain Services programming to directory-enable their products and applications.</span></span> <span data-ttu-id="b7e1f-120">服務可以在 Active Directory Domain Services 中自行發佈;用戶端可以使用 Active Directory Domain Services 來尋找服務，而且兩者都可以使用 Active Directory Domain Services 來找出並使用網路上的其他物件。</span><span class="sxs-lookup"><span data-stu-id="b7e1f-120">Services can publish themselves in Active Directory Domain Services; clients can use Active Directory Domain Services to find services, and both can use Active Directory Domain Services to locate and work with other objects on a network.</span></span>

## <a name="developer-audience"></a><span data-ttu-id="b7e1f-121">開發人員對象</span><span class="sxs-lookup"><span data-stu-id="b7e1f-121">Developer audience</span></span>

<span data-ttu-id="b7e1f-122">存取 Active Directory Domain Services 中資料的應用程式可以使用 [Active Directory 服務介面](../adsi/active-directory-service-interfaces-adsi.md) Api、 [輕量型目錄存取協定](/previous-versions/windows/desktop/ldap/lightweight-directory-access-protocol-ldap-api) api 或 [DirectoryServices](/dotnet/api/system.directoryservices) 命名空間來撰寫。</span><span class="sxs-lookup"><span data-stu-id="b7e1f-122">Applications that access data in Active Directory Domain Services can be written using the [Active Directory Service Interfaces](../adsi/active-directory-service-interfaces-adsi.md) API, [Lightweight Directory Access Protocol](/previous-versions/windows/desktop/ldap/lightweight-directory-access-protocol-ldap-api) API, or the [System.DirectoryServices](/dotnet/api/system.directoryservices) namespace.</span></span>

## <a name="run-time-requirements"></a><span data-ttu-id="b7e1f-123">執行階段需求求</span><span class="sxs-lookup"><span data-stu-id="b7e1f-123">Run-time requirements</span></span>

<span data-ttu-id="b7e1f-124">Active Directory Domain Services 在 Windows 2000 和更新版本的網域控制站上執行。</span><span class="sxs-lookup"><span data-stu-id="b7e1f-124">Active Directory Domain Services run on Windows 2000 and later domain controllers.</span></span> <span data-ttu-id="b7e1f-125">不過，您可以撰寫用戶端應用程式，並在 Windows Vista、Windows Server 2003、Windows XP、Windows 2000、Windows NT 4.0、Windows 98 和 Windows 95 上執行。</span><span class="sxs-lookup"><span data-stu-id="b7e1f-125">However, client applications can be written for and run on Windows Vista, Windows Server 2003, Windows XP, Windows 2000, Windows NT 4.0, Windows 98, and Windows 95.</span></span>

## <a name="in-this-section"></a><span data-ttu-id="b7e1f-126">本節內容</span><span class="sxs-lookup"><span data-stu-id="b7e1f-126">In this section</span></span>

<dl> <dt>

[<span data-ttu-id="b7e1f-127">關於 Active Directory Domain Services</span><span class="sxs-lookup"><span data-stu-id="b7e1f-127">About Active Directory Domain Services</span></span>](about-active-directory-domain-services.md)
</dt> <dd>

<span data-ttu-id="b7e1f-128">Active Directory Domain Services 的一般資訊。</span><span class="sxs-lookup"><span data-stu-id="b7e1f-128">General information about Active Directory Domain Services.</span></span>

</dd> <dt>

[<span data-ttu-id="b7e1f-129">使用 Active Directory 網域服務</span><span class="sxs-lookup"><span data-stu-id="b7e1f-129">Using Active Directory Domain Services</span></span>](using-active-directory-domain-services.md)
</dt> <dd>

<span data-ttu-id="b7e1f-130">Active Directory Domain Services 程式設計指南。</span><span class="sxs-lookup"><span data-stu-id="b7e1f-130">Active Directory Domain Services programming guide.</span></span>

</dd> <dt>

[<span data-ttu-id="b7e1f-131">Active Directory Domain Services 參考</span><span class="sxs-lookup"><span data-stu-id="b7e1f-131">Active Directory Domain Services Reference</span></span>](active-directory-domain-services-reference.md)
</dt> <dd>

<span data-ttu-id="b7e1f-132">Active Directory Domain Services 程式設計參考。</span><span class="sxs-lookup"><span data-stu-id="b7e1f-132">Active Directory Domain Services programming reference.</span></span>

</dd> </dl>

 

 