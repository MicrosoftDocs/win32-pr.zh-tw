---
title: User 物件屬性
description: 使用者物件具有多個屬性。 本節記載 Windows、系統管理工具和 Windows 通訊錄 (WAB) 所使用的重要屬性。 它不會描述所有屬性;許多屬性不會用於使用者物件。
ms.assetid: c173c5d1-2680-4b9c-961d-251fba6e2c7c
ms.tgt_platform: multiple
keywords:
- User 物件屬性廣告
- Users AD、User 物件屬性
- 物件 AD、使用者、屬性
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 4f9c90d8d5f28c41971f5f6910cfb8bef1fafd6f
ms.sourcegitcommit: 803f3ccd65bdefe36bd851b9c6e7280be9489016
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/17/2020
ms.locfileid: "103933037"
---
# <a name="user-object-attributes"></a><span data-ttu-id="264cc-108">User 物件屬性</span><span class="sxs-lookup"><span data-stu-id="264cc-108">User Object Attributes</span></span>

<span data-ttu-id="264cc-109">使用者物件具有多個屬性。</span><span class="sxs-lookup"><span data-stu-id="264cc-109">A user object has multiple attributes.</span></span> <span data-ttu-id="264cc-110">本節記載 Windows、系統管理工具和 Windows 通訊錄 (WAB) 所使用的重要屬性。</span><span class="sxs-lookup"><span data-stu-id="264cc-110">This section documents key attributes used by Windows, administrative tools, and the Windows Address Book (WAB).</span></span> <span data-ttu-id="264cc-111">它不會描述所有屬性;許多屬性不會用於使用者物件。</span><span class="sxs-lookup"><span data-stu-id="264cc-111">It does not describe all attributes; many attributes are not used for the user object.</span></span>

<span data-ttu-id="264cc-112">某些屬性會儲存在目錄中（例如 [**cn**](/windows/desktop/ADSchema/a-cn)、 [**nTSecurityDescriptor**](/windows/desktop/ADSchema/a-ntsecuritydescriptor)、 [**objectGUID**](/windows/desktop/ADSchema/a-objectguid)等），並複寫到網域內的所有網域控制站。</span><span class="sxs-lookup"><span data-stu-id="264cc-112">Some attributes are stored in the directory, such as [**cn**](/windows/desktop/ADSchema/a-cn), [**nTSecurityDescriptor**](/windows/desktop/ADSchema/a-ntsecuritydescriptor), [**objectGUID**](/windows/desktop/ADSchema/a-objectguid), and so on, and replicated to all domain controllers within a domain.</span></span> <span data-ttu-id="264cc-113">這些屬性的子集也會複寫到通用類別目錄。</span><span class="sxs-lookup"><span data-stu-id="264cc-113">A subset of these attributes is also replicated to the global catalog.</span></span>

<span data-ttu-id="264cc-114">非複寫的屬性會儲存在每個網域控制站上，但不會複寫到其他位置，例如 [**badPwdCount**](/windows/desktop/ADSchema/a-badpwdcount)、 [**lastLogon**](/windows/desktop/ADSchema/a-lastlogon)、 [**lastLogoff**](/windows/desktop/ADSchema/a-lastlogoff)等等。</span><span class="sxs-lookup"><span data-stu-id="264cc-114">Non-replicated attributes are stored on each domain controller, but are not replicated elsewhere, such as [**badPwdCount**](/windows/desktop/ADSchema/a-badpwdcount), [**lastLogon**](/windows/desktop/ADSchema/a-lastlogon), [**lastLogoff**](/windows/desktop/ADSchema/a-lastlogoff), and so on.</span></span> <span data-ttu-id="264cc-115">非複寫的屬性是與特定網域控制站相關的屬性。</span><span class="sxs-lookup"><span data-stu-id="264cc-115">The non-replicated attributes are attributes that pertain to a particular domain controller.</span></span> <span data-ttu-id="264cc-116">例如， **lastLogon** 是使用者網路登入的最後一個日期和時間，會由傳回該屬性的特定網域控制站進行驗證。</span><span class="sxs-lookup"><span data-stu-id="264cc-116">For example, **lastLogon** is the last date and time that the user network logon was validated by the particular domain controller that is returning the property.</span></span>

<span data-ttu-id="264cc-117">使用者物件也具有未儲存在目錄中的已建立屬性，但網域控制站會計算這些屬性，例如 [**canonicalName**](/windows/desktop/ADSchema/a-canonicalname)、 [**distinguishedName**](/windows/desktop/ADSchema/a-distinguishedname)、 [**allowedAttributes**](/windows/desktop/ADSchema/a-allowedattributes)等等。</span><span class="sxs-lookup"><span data-stu-id="264cc-117">A user object also has constructed attributes that are not stored in the directory, but are calculated by the domain controller, such as [**canonicalName**](/windows/desktop/ADSchema/a-canonicalname), [**distinguishedName**](/windows/desktop/ADSchema/a-distinguishedname), [**allowedAttributes**](/windows/desktop/ADSchema/a-allowedattributes), and so on.</span></span>

<span data-ttu-id="264cc-118">使用者物件的屬性會分類為：</span><span class="sxs-lookup"><span data-stu-id="264cc-118">Attributes for user objects are classified as:</span></span>

<dl> <dt>

<span data-ttu-id="264cc-119"><span id="Base_Object_Attributes"></span><span id="base_object_attributes"></span><span id="BASE_OBJECT_ATTRIBUTES"></span>基底物件屬性</span><span class="sxs-lookup"><span data-stu-id="264cc-119"><span id="Base_Object_Attributes"></span><span id="base_object_attributes"></span><span id="BASE_OBJECT_ATTRIBUTES"></span>Base Object Attributes</span></span>
</dt> <dd>

<span data-ttu-id="264cc-120">此類別包含所有目錄物件（例如 [**objectClass**](/windows/desktop/ADSchema/a-objectclass)、 [**nTSecurityDescriptor**](/windows/desktop/ADSchema/a-ntsecuritydescriptor)等）所需的屬性。</span><span class="sxs-lookup"><span data-stu-id="264cc-120">This category includes attributes required for all directory objects, such as [**objectClass**](/windows/desktop/ADSchema/a-objectclass), [**nTSecurityDescriptor**](/windows/desktop/ADSchema/a-ntsecuritydescriptor), and so on.</span></span>

</dd> <dt>

<span data-ttu-id="264cc-121"><span id="Naming_Attributes"></span><span id="naming_attributes"></span><span id="NAMING_ATTRIBUTES"></span>命名屬性</span><span class="sxs-lookup"><span data-stu-id="264cc-121"><span id="Naming_Attributes"></span><span id="naming_attributes"></span><span id="NAMING_ATTRIBUTES"></span>Naming Attributes</span></span>
</dt> <dd>

<span data-ttu-id="264cc-122">這個類別包含用來參考或識別物件的屬性，例如 [**distinguishedName**](/windows/desktop/ADSchema/a-distinguishedname)、 [**objectGUID**](/windows/desktop/ADSchema/a-objectguid)、 [**objectSID**](/windows/desktop/ADSchema/a-objectsid)等等。</span><span class="sxs-lookup"><span data-stu-id="264cc-122">This category includes attributes used to refer to or identify the object, such as [**distinguishedName**](/windows/desktop/ADSchema/a-distinguishedname), [**objectGUID**](/windows/desktop/ADSchema/a-objectguid), [**objectSID**](/windows/desktop/ADSchema/a-objectsid), and so on.</span></span> <span data-ttu-id="264cc-123">如需有關為使用者物件命名屬性的詳細資訊，請參閱 [使用者命名屬性](naming-properties.md)。</span><span class="sxs-lookup"><span data-stu-id="264cc-123">For more information about naming attributes for user objects, see [User Naming Attributes](naming-properties.md).</span></span>

</dd> <dt>

<span data-ttu-id="264cc-124"><span id="Security_Attributes"></span><span id="security_attributes"></span><span id="SECURITY_ATTRIBUTES"></span>安全性屬性</span><span class="sxs-lookup"><span data-stu-id="264cc-124"><span id="Security_Attributes"></span><span id="security_attributes"></span><span id="SECURITY_ATTRIBUTES"></span>Security Attributes</span></span>
</dt> <dd>

<span data-ttu-id="264cc-125">此類別包含登入和存取控制的屬性。</span><span class="sxs-lookup"><span data-stu-id="264cc-125">This category includes attributes for logon and access control.</span></span> <span data-ttu-id="264cc-126">如需有關使用者物件之安全性屬性的詳細資訊，請參閱 [使用者安全性屬性](security-properties.md)。</span><span class="sxs-lookup"><span data-stu-id="264cc-126">For more information about security attributes for user objects, see [User Security Attributes](security-properties.md).</span></span>

</dd> <dt>

<span data-ttu-id="264cc-127"><span id="Address_Book_Attributes"></span><span id="address_book_attributes"></span><span id="ADDRESS_BOOK_ATTRIBUTES"></span>通訊錄屬性</span><span class="sxs-lookup"><span data-stu-id="264cc-127"><span id="Address_Book_Attributes"></span><span id="address_book_attributes"></span><span id="ADDRESS_BOOK_ATTRIBUTES"></span>Address Book Attributes</span></span>
</dt> <dd>

<span data-ttu-id="264cc-128">此類別包括電子郵件和使用者資料的屬性。</span><span class="sxs-lookup"><span data-stu-id="264cc-128">This category includes attributes for email and user data.</span></span> <span data-ttu-id="264cc-129">如需有關使用者物件通訊錄屬性的詳細資訊，請參閱 [使用者通訊錄屬性](address-book-properties.md)。</span><span class="sxs-lookup"><span data-stu-id="264cc-129">For more information about address book attributes for user objects, see [User Address Book Attributes](address-book-properties.md).</span></span>

</dd> <dt>

<span data-ttu-id="264cc-130"><span id="Application_Specific_Attributes"></span><span id="application_specific_attributes"></span><span id="APPLICATION_SPECIFIC_ATTRIBUTES"></span>應用程式特定屬性</span><span class="sxs-lookup"><span data-stu-id="264cc-130"><span id="Application_Specific_Attributes"></span><span id="application_specific_attributes"></span><span id="APPLICATION_SPECIFIC_ATTRIBUTES"></span>Application Specific Attributes</span></span>
</dt> <dd>

<span data-ttu-id="264cc-131">此類別包含特定應用程式的使用者特定設定資料。</span><span class="sxs-lookup"><span data-stu-id="264cc-131">This category includes user-specific configuration data for specific applications.</span></span>

</dd> </dl>

<span data-ttu-id="264cc-132">如需有關讀取和修改使用者物件屬性的詳細資訊，請參閱 [在 Active Directory Domain Services 中讀取和寫入物件的屬性](reading-and-writing-attributes-of-objects-in-active-directory-domain-services.md)。</span><span class="sxs-lookup"><span data-stu-id="264cc-132">For more information about reading and modifying attributes for a user object, see [Reading and Writing Attributes of Objects in Active Directory Domain Services](reading-and-writing-attributes-of-objects-in-active-directory-domain-services.md).</span></span>

<span data-ttu-id="264cc-133">如需使用者類別的詳細資訊，包括類別的 [**mayContain**](/windows/desktop/ADSchema/a-maycontain) 和 [**mustContain**](/windows/desktop/ADSchema/a-mustcontain) 屬性的完整清單，請參閱 [**使用者**](/windows/desktop/ADSchema/c-user)。</span><span class="sxs-lookup"><span data-stu-id="264cc-133">For more information about the User class, including a complete list of the [**mayContain**](/windows/desktop/ADSchema/a-maycontain) and [**mustContain**](/windows/desktop/ADSchema/a-mustcontain) attributes of the class, see [**User**](/windows/desktop/ADSchema/c-user).</span></span>

## <a name="setting-passwords"></a><span data-ttu-id="264cc-134">設定密碼</span><span class="sxs-lookup"><span data-stu-id="264cc-134">Setting Passwords</span></span>

<span data-ttu-id="264cc-135">無法直接修改使用者的密碼，因為這牽涉到透過網路傳送未加密的密碼。</span><span class="sxs-lookup"><span data-stu-id="264cc-135">The password for a user cannot be modified directly because this would involve sending an unencrypted password over the network.</span></span> <span data-ttu-id="264cc-136">若要設定使用者的密碼，必須使用 [**IADsUser**](/windows/desktop/api/iads/nf-iads-iadsuser-changepassword) 或 [**IADsUser. SetPassword**](/windows/desktop/api/iads/nf-iads-iadsuser-setpassword) 方法。</span><span class="sxs-lookup"><span data-stu-id="264cc-136">To set the password for a user, it is necessary to use the [**IADsUser.ChangePassword**](/windows/desktop/api/iads/nf-iads-iadsuser-changepassword) or [**IADsUser.SetPassword**](/windows/desktop/api/iads/nf-iads-iadsuser-setpassword) method.</span></span> <span data-ttu-id="264cc-137">當應用程式允許使用者變更自己的密碼時，會使用 **IADsUser. ChangePassword** 方法。</span><span class="sxs-lookup"><span data-stu-id="264cc-137">The **IADsUser.ChangePassword** method is used when the application is allowing the user to change their own password.</span></span> <span data-ttu-id="264cc-138">當應用程式可讓系統管理員重設密碼時，會使用 **IADsUser. SetPassword** 方法。</span><span class="sxs-lookup"><span data-stu-id="264cc-138">The **IADsUser.SetPassword** method is used when the application enables an administrator to reset a password.</span></span>

 

 