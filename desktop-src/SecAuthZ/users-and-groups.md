---
description: 說明授權管理員 API 中的使用者和群組定義。
ms.assetid: 783be0b2-7894-4780-900d-98918f824a04
title: 使用者和群組
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: c7c40ee9234fa8d6259282855011cfc3fc008d6e
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/08/2021
ms.locfileid: "106992186"
---
# <a name="users-and-groups"></a><span data-ttu-id="171fa-103">使用者和群組</span><span class="sxs-lookup"><span data-stu-id="171fa-103">Users and Groups</span></span>

<span data-ttu-id="171fa-104">在授權管理員中，授權原則的收件者會以下列群組表示：</span><span class="sxs-lookup"><span data-stu-id="171fa-104">In Authorization Manager, recipients of authorization policy are represented by the following groups:</span></span>

-   <span data-ttu-id="171fa-105">Windows 使用者和群組</span><span class="sxs-lookup"><span data-stu-id="171fa-105">Windows Users and Groups</span></span>

    <span data-ttu-id="171fa-106">這些群組包含安全性主體的使用者、電腦和內建組。</span><span class="sxs-lookup"><span data-stu-id="171fa-106">These groups include users, computers, and built-in groups for security principals.</span></span>

-   <span data-ttu-id="171fa-107">LDAP 查詢群組</span><span class="sxs-lookup"><span data-stu-id="171fa-107">LDAP Query Groups</span></span>

    <span data-ttu-id="171fa-108">這些群組中的成員資格會視需要從輕量型目錄存取協定 (LDAP) 查詢進行動態計算。</span><span class="sxs-lookup"><span data-stu-id="171fa-108">Membership in these groups is dynamically calculated as needed from Lightweight Directory Access Protocol (LDAP) queries.</span></span> <span data-ttu-id="171fa-109">LDAP 查詢群組是一種應用程式群組。</span><span class="sxs-lookup"><span data-stu-id="171fa-109">An LDAP query group is a type of application group.</span></span>

-   <span data-ttu-id="171fa-110">基本應用程式群組</span><span class="sxs-lookup"><span data-stu-id="171fa-110">Basic Application Groups</span></span>

    <span data-ttu-id="171fa-111">這些群組是由 LDAP 查詢群組、Windows 使用者和群組，以及其他基本應用程式群組所組成。</span><span class="sxs-lookup"><span data-stu-id="171fa-111">These groups consist of LDAP query groups, Windows users and groups, and other basic application groups.</span></span>

## <a name="windows-users-and-groups"></a><span data-ttu-id="171fa-112">Windows 使用者和群組</span><span class="sxs-lookup"><span data-stu-id="171fa-112">Windows Users and Groups</span></span>

<span data-ttu-id="171fa-113">這些與整個 Windows 作業系統所使用的使用者和群組相同。</span><span class="sxs-lookup"><span data-stu-id="171fa-113">These are the same as the users and groups used throughout the Windows operating system.</span></span>

## <a name="ldap-query-groups"></a><span data-ttu-id="171fa-114">LDAP 查詢群組</span><span class="sxs-lookup"><span data-stu-id="171fa-114">LDAP Query Groups</span></span>

<span data-ttu-id="171fa-115">在授權管理員中，您可以使用 LDAP 查詢，將使用者的屬性與使用者在 Active Directory 中的物件相符。</span><span class="sxs-lookup"><span data-stu-id="171fa-115">In Authorization Manager, you can use LDAP queries to match the user's attributes with those of the user's object in Active Directory.</span></span>

<span data-ttu-id="171fa-116">例如，下列查詢會尋找每個成員，但不包括所有的。</span><span class="sxs-lookup"><span data-stu-id="171fa-116">For example, the following query finds everyone except Andy.</span></span>


```C++
(&(objectCategory=person)(objectClass=user)(!cn=andy))
```



<span data-ttu-id="171fa-117">下列查詢會在 www.fabrikam.com 中尋找某人別名的所有成員。</span><span class="sxs-lookup"><span data-stu-id="171fa-117">The following query finds all members of the someone alias at www.fabrikam.com.</span></span>


```C++
(memberOf=CN=someone,OU=litwareinc,DC=Fabrikam,DC=com)
```



## <a name="basic-application-groups"></a><span data-ttu-id="171fa-118">基本應用程式群組</span><span class="sxs-lookup"><span data-stu-id="171fa-118">Basic Application Groups</span></span>

<span data-ttu-id="171fa-119">在授權管理員 API 中，應用程式群組是由 [**IAzApplicationGroup**](/windows/desktop/api/Azroles/nn-azroles-iazapplicationgroup) 物件表示。</span><span class="sxs-lookup"><span data-stu-id="171fa-119">In the Authorization Manager API, an application group is represented by an [**IAzApplicationGroup**](/windows/desktop/api/Azroles/nn-azroles-iazapplicationgroup) object.</span></span> <span data-ttu-id="171fa-120">基本應用程式群組是一種應用程式群組。</span><span class="sxs-lookup"><span data-stu-id="171fa-120">A basic application group is a type of application group.</span></span>

<span data-ttu-id="171fa-121">若要定義基本的應用程式群組成員資格，請定義誰是成員，並定義誰不是成員。</span><span class="sxs-lookup"><span data-stu-id="171fa-121">To define basic application group membership, define who is a member and define who is not a member.</span></span> <span data-ttu-id="171fa-122">這兩個步驟都是以相同的方式執行。</span><span class="sxs-lookup"><span data-stu-id="171fa-122">Both of these steps are carried out in the same way.</span></span> <span data-ttu-id="171fa-123">指定零個或多個 Windows 使用者和群組、先前定義的基本應用程式群組或 LDAP 查詢群組。</span><span class="sxs-lookup"><span data-stu-id="171fa-123">Specify zero or more Windows users and groups, previously defined basic application groups, or LDAP query groups.</span></span> <span data-ttu-id="171fa-124">基本應用程式群組的成員資格是藉由從群組中移除任何非成員來計算。</span><span class="sxs-lookup"><span data-stu-id="171fa-124">The membership of the basic application group is calculated by removing any nonmembers from the group.</span></span> <span data-ttu-id="171fa-125">授權管理員會在執行時間自動執行此程式。</span><span class="sxs-lookup"><span data-stu-id="171fa-125">Authorization Manager does this automatically at run time.</span></span>

<span data-ttu-id="171fa-126">基本應用程式群組中的 Nonmembership 優先于成員資格。</span><span class="sxs-lookup"><span data-stu-id="171fa-126">Nonmembership in a basic application group takes precedence over membership.</span></span>

<span data-ttu-id="171fa-127">不允許迴圈成員資格定義;這些錯誤訊息會導致下列錯誤訊息：「無法新增擁有者。</span><span class="sxs-lookup"><span data-stu-id="171fa-127">Circular membership definitions are not allowed; they result in the following error message: "Cannot add GroupName.</span></span> <span data-ttu-id="171fa-128">發生下列問題：已偵測到迴圈。」</span><span class="sxs-lookup"><span data-stu-id="171fa-128">The following problem occurred: A loop has been detected."</span></span>

## <a name="related-topics"></a><span data-ttu-id="171fa-129">相關主題</span><span class="sxs-lookup"><span data-stu-id="171fa-129">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="171fa-130">在 c + + 中定義使用者群組</span><span class="sxs-lookup"><span data-stu-id="171fa-130">Defining Groups of Users in C++</span></span>](defining-groups-of-users-in-c--.md)
</dt> </dl>

 

 



