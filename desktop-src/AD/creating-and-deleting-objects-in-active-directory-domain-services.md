---
title: 在 Active Directory Domain Services 中建立和刪除物件
description: 在 Active Directory Domain Services 中，用來以程式設計方式建立和刪除物件的程式，取決於所使用的程式設計技術。
ms.assetid: 13f83aea-ad39-4737-af3c-24316a31046d
ms.tgt_platform: multiple
keywords:
- 建立和刪除 Active Directory 物件 Active Directory
- 使用建立和刪除物件的 Active Directory Domain Services Active Directory
- 物件 Active Directory、建立及刪除 Active Directory Domain Services 物件
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 11d3e85ef3c356978faeab059e3969bb657185bd
ms.sourcegitcommit: 803f3ccd65bdefe36bd851b9c6e7280be9489016
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/17/2020
ms.locfileid: "104462896"
---
# <a name="creating-and-deleting-objects-in-active-directory-domain-services"></a><span data-ttu-id="189cd-106">在 Active Directory Domain Services 中建立和刪除物件</span><span class="sxs-lookup"><span data-stu-id="189cd-106">Creating and Deleting Objects in Active Directory Domain Services</span></span>

<span data-ttu-id="189cd-107">在 Active Directory Domain Services 中，用來以程式設計方式建立和刪除物件的程式，取決於所使用的程式設計技術。</span><span class="sxs-lookup"><span data-stu-id="189cd-107">The procedure used to programmatically create and delete objects in Active Directory Domain Services is dependent upon the programming technology used.</span></span> <span data-ttu-id="189cd-108">如需有關使用特定程式設計技術在 Active Directory Domain Services 中建立和刪除物件的詳細資訊，請參閱下表所列的主題。</span><span class="sxs-lookup"><span data-stu-id="189cd-108">For more information about creating and deleting objects in Active Directory Domain Services with a specific programming technology, see the topics listed in the following table.</span></span>



| <span data-ttu-id="189cd-109">程式設計技術</span><span class="sxs-lookup"><span data-stu-id="189cd-109">Programming technology</span></span>                                                                       | <span data-ttu-id="189cd-110">取得詳細資訊</span><span class="sxs-lookup"><span data-stu-id="189cd-110">For more information</span></span>                                                            |
|----------------------------------------------------------------------------------------------|---------------------------------------------------------------------------------|
| [<span data-ttu-id="189cd-111">Active Directory 服務介面</span><span class="sxs-lookup"><span data-stu-id="189cd-111">Active Directory Service Interfaces</span></span>](/windows/desktop/ADSI/active-directory-service-interfaces-adsi)         | [<span data-ttu-id="189cd-112">建立和刪除物件</span><span class="sxs-lookup"><span data-stu-id="189cd-112">Creating and Deleting Objects</span></span>](/windows/desktop/ADSI/creating-and-deleting-objects)             |
| [<span data-ttu-id="189cd-113">輕量型目錄存取協定</span><span class="sxs-lookup"><span data-stu-id="189cd-113">Lightweight Directory Access Protocol</span></span>](/previous-versions/windows/desktop/ldap/lightweight-directory-access-protocol-ldap-api) | [<span data-ttu-id="189cd-114">修改目錄專案</span><span class="sxs-lookup"><span data-stu-id="189cd-114">Modifying a Directory Entry</span></span>](/previous-versions/windows/desktop/ldap/modifying-a-directory-entry)                 |
| [<span data-ttu-id="189cd-115">System.DirectoryServices</span><span class="sxs-lookup"><span data-stu-id="189cd-115">System.DirectoryServices</span></span>](/dotnet/api/system.directoryservices) | <span data-ttu-id="189cd-116">[建立、刪除、重新命名和移動物件](https://msdn.microsoft.com/library/ms180850(v=VS.80).aspx)</span><span class="sxs-lookup"><span data-stu-id="189cd-116">[Create, Delete, Rename and Move Objects](https://msdn.microsoft.com/library/ms180850(v=VS.80).aspx)</span></span> |



 

## <a name="creating-an-object"></a><span data-ttu-id="189cd-117">建立物件</span><span class="sxs-lookup"><span data-stu-id="189cd-117">Creating an Object</span></span>

<span data-ttu-id="189cd-118">一般情況下，建立物件所需的唯一屬性是 **cn** 和 **objectClass** 屬性。</span><span class="sxs-lookup"><span data-stu-id="189cd-118">In general, the only attributes required for an object to be created are the **cn** and **objectClass** attributes.</span></span> <span data-ttu-id="189cd-119">不過，建立物件並不一定會讓它成為功能物件。</span><span class="sxs-lookup"><span data-stu-id="189cd-119">Just creating an object does not necessarily make it a functional object however.</span></span> <span data-ttu-id="189cd-120">某些類型的物件（例如使用者和群組）具有其他必要屬性，可讓它們正常運作。</span><span class="sxs-lookup"><span data-stu-id="189cd-120">Certain types of objects, such as users and groups, have additional required attributes to make them functional.</span></span> <span data-ttu-id="189cd-121">如需建立特定物件類型的詳細資訊，請參閱[在定義域中](creating-groups-in-a-domain.md)[建立使用者](creating-a-user.md)和建立群組。</span><span class="sxs-lookup"><span data-stu-id="189cd-121">For more information about creating specific types of objects, see [Creating a User](creating-a-user.md) and [Creating Groups in a Domain](creating-groups-in-a-domain.md).</span></span>

<span data-ttu-id="189cd-122">**Windows Server 2003：** 在 WWindows 伺服器2003或更新版本上執行的網域控制站上建立 [**使用者**](/windows/desktop/ADSchema/c-user)、 [**群組**](/windows/desktop/ADSchema/c-group)或 [**電腦**](/windows/desktop/ADSchema/c-computer) 類別的物件時，網域控制站會自動將物件的 [**sAMAccountName**](/windows/desktop/ADSchema/a-samaccountname) 屬性設定為唯一字串（如果未指定的話）。</span><span class="sxs-lookup"><span data-stu-id="189cd-122">**Windows Server 2003:** When an object of the [**user**](/windows/desktop/ADSchema/c-user), [**group**](/windows/desktop/ADSchema/c-group), or [**computer**](/windows/desktop/ADSchema/c-computer) class is created on a domain controller that is running on WWindows Server 2003 or later, the domain controller automatically sets the [**sAMAccountName**](/windows/desktop/ADSchema/a-samaccountname) attribute for the object to a unique string, if one is not specified.</span></span>

## <a name="deleting-an-object"></a><span data-ttu-id="189cd-123">刪除物件</span><span class="sxs-lookup"><span data-stu-id="189cd-123">Deleting an Object</span></span>

<span data-ttu-id="189cd-124">刪除物件時，Active Directory 伺服器會執行下列動作：</span><span class="sxs-lookup"><span data-stu-id="189cd-124">The Active Directory server performs the following actions when an object is deleted:</span></span>

-   <span data-ttu-id="189cd-125">已刪除之物件的 **isDeleted** 屬性設定為 **TRUE**。</span><span class="sxs-lookup"><span data-stu-id="189cd-125">The **isDeleted** attribute of the deleted object is set to **TRUE**.</span></span> <span data-ttu-id="189cd-126">將 IsDeleted 屬性值設為 **TRUE** 的物件會被 [*稱為「*](/previous-versions/windows/desktop/legacy/ms681941(v=vs.85))標記」（  ）。</span><span class="sxs-lookup"><span data-stu-id="189cd-126">Objects with an **isDeleted** attribute value set to **TRUE** are called [*tombstones*](/previous-versions/windows/desktop/legacy/ms681941(v=vs.85)).</span></span>
-   <span data-ttu-id="189cd-127">已刪除的物件會移至其命名內容的 Deleted Objects 容器。</span><span class="sxs-lookup"><span data-stu-id="189cd-127">The deleted object is moved to the Deleted Objects container for its naming context.</span></span> <span data-ttu-id="189cd-128">如果 [物件 **systemFlags** ] 屬性包含0x02000000 旗標，則物件不會移至 [已刪除的物件] 容器。</span><span class="sxs-lookup"><span data-stu-id="189cd-128">If the object **systemFlags** property contains the 0x02000000 flag, the object is not moved to the Deleted Objects container.</span></span> <span data-ttu-id="189cd-129">如需有關系結至已刪除物件容器之內容和列舉的詳細資訊，請參閱 [取出已刪除的物件](retrieving-deleted-objects.md)。</span><span class="sxs-lookup"><span data-stu-id="189cd-129">For more information about binding to and enumerating the contents of the Deleted Objects container, see [Retrieving Deleted Objects](retrieving-deleted-objects.md).</span></span>
-   <span data-ttu-id="189cd-130">刪除的物件容器是平面的，因此所有物件都位於已刪除物件容器中的相同層級上。</span><span class="sxs-lookup"><span data-stu-id="189cd-130">The Deleted Objects container is flat, so all objects reside at the same level within the Deleted Objects container.</span></span> <span data-ttu-id="189cd-131">因此，已刪除之物件的相對辨別名稱會變更，以確保該名稱在已刪除的物件容器中是唯一的。</span><span class="sxs-lookup"><span data-stu-id="189cd-131">Thus, the relative distinguished name of the deleted object is changed to ensure that the name is unique within the Deleted Objects container.</span></span> <span data-ttu-id="189cd-132">如果原始名稱的長度超過75個字元，則會截斷為75個字元。</span><span class="sxs-lookup"><span data-stu-id="189cd-132">If the original name is longer than 75 characters, it is truncated to 75 characters.</span></span> <span data-ttu-id="189cd-133">接著會將下列內容附加至新名稱：</span><span class="sxs-lookup"><span data-stu-id="189cd-133">The following are then appended to the new name:</span></span>
    1.  <span data-ttu-id="189cd-134">0x0A 字元</span><span class="sxs-lookup"><span data-stu-id="189cd-134">A 0x0A character</span></span>
    2.  <span data-ttu-id="189cd-135">字串 "DEL："</span><span class="sxs-lookup"><span data-stu-id="189cd-135">The string "DEL:"</span></span>
    3.  <span data-ttu-id="189cd-136">唯一 GUID 的字串格式，例如 "947e3228-70c9-4311-8b7a-e5c9b5bd4432"</span><span class="sxs-lookup"><span data-stu-id="189cd-136">The string form of a unique GUID, such as "947e3228-70c9-4311-8b7a-e5c9b5bd4432"</span></span>

    <span data-ttu-id="189cd-137">已刪除的物件名稱範例如下：</span><span class="sxs-lookup"><span data-stu-id="189cd-137">An example of a deleted object name is:</span></span>
    ```C++
    Jeff Smith\0ADEL:947e3228-70c9-4311-8b7a-e5c9b5bd4432
    ```

    

-   <span data-ttu-id="189cd-138">已刪除之物件的大部分屬性值都會被移除。</span><span class="sxs-lookup"><span data-stu-id="189cd-138">Most attribute values for the deleted object are removed.</span></span> <span data-ttu-id="189cd-139">系統會自動保留下列屬性：</span><span class="sxs-lookup"><span data-stu-id="189cd-139">The following attributes are automatically retained:</span></span>

    -   <span data-ttu-id="189cd-140">**attributeID**</span><span class="sxs-lookup"><span data-stu-id="189cd-140">**attributeID**</span></span>
    -   <span data-ttu-id="189cd-141">**attributeSyntax**</span><span class="sxs-lookup"><span data-stu-id="189cd-141">**attributeSyntax**</span></span>
    -   <span data-ttu-id="189cd-142">**distinguishedName**</span><span class="sxs-lookup"><span data-stu-id="189cd-142">**distinguishedName**</span></span>
    -   <span data-ttu-id="189cd-143">**dNReferenceUpdate**</span><span class="sxs-lookup"><span data-stu-id="189cd-143">**dNReferenceUpdate**</span></span>
    -   <span data-ttu-id="189cd-144">**flatName**</span><span class="sxs-lookup"><span data-stu-id="189cd-144">**flatName**</span></span>
    -   <span data-ttu-id="189cd-145">**governsID**</span><span class="sxs-lookup"><span data-stu-id="189cd-145">**governsID**</span></span>
    -   <span data-ttu-id="189cd-146">**groupType**</span><span class="sxs-lookup"><span data-stu-id="189cd-146">**groupType**</span></span>
    -   <span data-ttu-id="189cd-147">**instanceType**</span><span class="sxs-lookup"><span data-stu-id="189cd-147">**instanceType**</span></span>
    -   <span data-ttu-id="189cd-148">**lDAPDisplayName**</span><span class="sxs-lookup"><span data-stu-id="189cd-148">**lDAPDisplayName**</span></span>
    -   <span data-ttu-id="189cd-149">**legacyExchangeDN**</span><span class="sxs-lookup"><span data-stu-id="189cd-149">**legacyExchangeDN**</span></span>
    -   <span data-ttu-id="189cd-150">**CreatorSID**</span><span class="sxs-lookup"><span data-stu-id="189cd-150">**mS-DS-CreatorSID**</span></span>
    -   <span data-ttu-id="189cd-151">**mSMQOwnerID**</span><span class="sxs-lookup"><span data-stu-id="189cd-151">**mSMQOwnerID**</span></span>
    -   <span data-ttu-id="189cd-152">**name**</span><span class="sxs-lookup"><span data-stu-id="189cd-152">**name**</span></span>
    -   <span data-ttu-id="189cd-153">**nCName**</span><span class="sxs-lookup"><span data-stu-id="189cd-153">**nCName**</span></span>
    -   <span data-ttu-id="189cd-154">**objectClass**</span><span class="sxs-lookup"><span data-stu-id="189cd-154">**objectClass**</span></span>
    -   <span data-ttu-id="189cd-155">**objectGUID**</span><span class="sxs-lookup"><span data-stu-id="189cd-155">**objectGUID**</span></span>
    -   <span data-ttu-id="189cd-156">**objectSid**</span><span class="sxs-lookup"><span data-stu-id="189cd-156">**objectSid**</span></span>
    -   <span data-ttu-id="189cd-157">**oMSyntax**</span><span class="sxs-lookup"><span data-stu-id="189cd-157">**oMSyntax**</span></span>
    -   <span data-ttu-id="189cd-158">**proxiedObjectName**</span><span class="sxs-lookup"><span data-stu-id="189cd-158">**proxiedObjectName**</span></span>
    -   <span data-ttu-id="189cd-159">**replPropertyMetaData**</span><span class="sxs-lookup"><span data-stu-id="189cd-159">**replPropertyMetaData**</span></span>
    -   <span data-ttu-id="189cd-160">**sAMAccountName**</span><span class="sxs-lookup"><span data-stu-id="189cd-160">**sAMAccountName**</span></span>
    -   <span data-ttu-id="189cd-161">**securityIdentifier**</span><span class="sxs-lookup"><span data-stu-id="189cd-161">**securityIdentifier**</span></span>
    -   <span data-ttu-id="189cd-162">**subClassOf**</span><span class="sxs-lookup"><span data-stu-id="189cd-162">**subClassOf**</span></span>
    -   <span data-ttu-id="189cd-163">**systemFlags**</span><span class="sxs-lookup"><span data-stu-id="189cd-163">**systemFlags**</span></span>
    -   <span data-ttu-id="189cd-164">**trustAttributes**</span><span class="sxs-lookup"><span data-stu-id="189cd-164">**trustAttributes**</span></span>
    -   <span data-ttu-id="189cd-165">**trustDirection**</span><span class="sxs-lookup"><span data-stu-id="189cd-165">**trustDirection**</span></span>
    -   <span data-ttu-id="189cd-166">**trustPartner**</span><span class="sxs-lookup"><span data-stu-id="189cd-166">**trustPartner**</span></span>
    -   <span data-ttu-id="189cd-167">**trustType**</span><span class="sxs-lookup"><span data-stu-id="189cd-167">**trustType**</span></span>
    -   <span data-ttu-id="189cd-168">**userAccountControl**</span><span class="sxs-lookup"><span data-stu-id="189cd-168">**userAccountControl**</span></span>
    -   <span data-ttu-id="189cd-169">**uSNChanged**</span><span class="sxs-lookup"><span data-stu-id="189cd-169">**uSNChanged**</span></span>
    -   <span data-ttu-id="189cd-170">**uSNCreated**</span><span class="sxs-lookup"><span data-stu-id="189cd-170">**uSNCreated**</span></span>
    -   <span data-ttu-id="189cd-171">**whenCreated**</span><span class="sxs-lookup"><span data-stu-id="189cd-171">**whenCreated**</span></span>

    <span data-ttu-id="189cd-172">包含0x00000008 之 **searchFlags** 屬性值的其他屬性也會保留下來。</span><span class="sxs-lookup"><span data-stu-id="189cd-172">Other attributes that have a **searchFlags** attribute value that contains 0x00000008 are also retained.</span></span>

    <span data-ttu-id="189cd-173">下列屬性值一律會從已刪除的物件中移除：</span><span class="sxs-lookup"><span data-stu-id="189cd-173">The following attribute values are always removed from a deleted object:</span></span>

    -   <span data-ttu-id="189cd-174">**objectCategory**</span><span class="sxs-lookup"><span data-stu-id="189cd-174">**objectCategory**</span></span>
    -   <span data-ttu-id="189cd-175">**samAccountType**</span><span class="sxs-lookup"><span data-stu-id="189cd-175">**samAccountType**</span></span>

-   <span data-ttu-id="189cd-176">系統會保留已刪除之物件的安全描述項，並且不會傳播可繼承的存取控制專案。</span><span class="sxs-lookup"><span data-stu-id="189cd-176">The security descriptor of the deleted object is retained and inheritable access control entries are not propagated.</span></span> <span data-ttu-id="189cd-177">在刪除物件時，安全描述項會保持原樣。</span><span class="sxs-lookup"><span data-stu-id="189cd-177">The security descriptor is retained as-is at the time the object is deleted.</span></span>
-   <span data-ttu-id="189cd-178">已刪除之物件的連結會被清除。</span><span class="sxs-lookup"><span data-stu-id="189cd-178">Links to and from the deleted object are cleared.</span></span> <span data-ttu-id="189cd-179">這會在刪除物件之後于背景中執行。</span><span class="sxs-lookup"><span data-stu-id="189cd-179">This is performed in the background after the object is deleted.</span></span> <span data-ttu-id="189cd-180">如果刪除的物件會在清除所有連結之前還原，則會收到錯誤。</span><span class="sxs-lookup"><span data-stu-id="189cd-180">If the deleted object is restored before all of the links are cleared, an error will be received.</span></span>
-   <span data-ttu-id="189cd-181">如果在 Windows Server 2003 網域控制站上刪除物件，已刪除之物件的 **lastKnownParent** 屬性會設為刪除該物件時所包含之容器的分辨名稱。</span><span class="sxs-lookup"><span data-stu-id="189cd-181">If the object is deleted on a Windows Server 2003 domain controller, the **lastKnownParent** attribute of the deleted object is set to the distinguished name of the container where the object was contained when it was deleted.</span></span>

<span data-ttu-id="189cd-182">已刪除的物件會保留在 [已刪除的物件] 容器中一段時間，稱為「*標記存留期」。*</span><span class="sxs-lookup"><span data-stu-id="189cd-182">The deleted object remains in the Deleted Objects container for a period of time known as the *tombstone lifetime*.</span></span> <span data-ttu-id="189cd-183">依預設，標記存留期為60天，但系統管理員可以變更此值。</span><span class="sxs-lookup"><span data-stu-id="189cd-183">By default, the tombstone lifetime is 60 days, but this value can be changed by the system administrator.</span></span> <span data-ttu-id="189cd-184">在標記存留期到期之後，物件會從目錄服務中永久移除。</span><span class="sxs-lookup"><span data-stu-id="189cd-184">After the tombstone lifetime expires, the object is permanently removed from the Directory Service.</span></span> <span data-ttu-id="189cd-185">為了避免遺失刪除作業，應用程式必須比標記存留期更頻繁地執行增量同步處理。</span><span class="sxs-lookup"><span data-stu-id="189cd-185">To avoid missing a delete operation, an application must perform incremental synchronizations more frequently than the tombstone lifetime.</span></span>

<span data-ttu-id="189cd-186">Windows Server 2003 新增了還原已刪除物件的功能。</span><span class="sxs-lookup"><span data-stu-id="189cd-186">Windows Server 2003 adds the ability to restore deleted objects.</span></span> <span data-ttu-id="189cd-187">如需有關已刪除物件還原的詳細資訊，請參閱 [還原已刪除的物件](restoring-deleted-objects.md)。</span><span class="sxs-lookup"><span data-stu-id="189cd-187">For more information about deleted object restoration, see [Restoring Deleted Objects](restoring-deleted-objects.md).</span></span>

<span data-ttu-id="189cd-188">當刪除專案時，不能修改物件的任何屬性。</span><span class="sxs-lookup"><span data-stu-id="189cd-188">When an item is deleted, none of the attributes of the object can be modified.</span></span> <span data-ttu-id="189cd-189">在 Windows Server 2003 中，可以修改已刪除物件上 (**ntSecurityDescriptor** 屬性) 的安全描述項。</span><span class="sxs-lookup"><span data-stu-id="189cd-189">In Windows Server 2003, it is possible to modify the security descriptor (the **ntSecurityDescriptor** attribute) on a deleted object.</span></span> <span data-ttu-id="189cd-190">這是為了在還原物件的人員沒有強制屬性的寫入權限時，允許還原物件。</span><span class="sxs-lookup"><span data-stu-id="189cd-190">This is to allow restoration of objects when the person restoring the object does not have write permissions to mandatory attributes.</span></span> <span data-ttu-id="189cd-191">若要更新已刪除之物件上的安全描述項，呼叫者除了一般 **寫入 \_ DAC** 和 **寫入 \_ 擁有** 者存取權之外，還必須具有命名內容的「重新產生標記」存取權限。</span><span class="sxs-lookup"><span data-stu-id="189cd-191">To update the security descriptor on a deleted object, the caller must have the "Reanimate Tombstone" control access right on the naming context, in addition to regular **WRITE\_DAC** and **WRITE\_OWNER** access.</span></span> <span data-ttu-id="189cd-192">即使安全描述項的限制，系統管理員仍可先取得物件的擁有權，假設系統管理員具有「 **SE \_ 取得 \_ 擁有權」 \_ 名稱** 許可權，然後修改安全描述項。</span><span class="sxs-lookup"><span data-stu-id="189cd-192">Even if the security descriptor is restrictive, the administrator can first take ownership of the object, assuming the administrator has the **SE\_TAKE\_OWNERSHIP\_NAME** privilege, and then modify the security descriptor.</span></span> <span data-ttu-id="189cd-193">若要這樣做，請在 [**ldap \_ 伺服器 \_ 顯示 \_ 已刪除的 \_ OID**](/previous-versions/windows/desktop/ldap/ldap-server-show-deleted-oid)控制項時，使用 [**ldap \_ modify \_ ext \_ s**](/previous-versions/windows/desktop/api/winldap/nf-winldap-ldap_modify_ext_s)函數。</span><span class="sxs-lookup"><span data-stu-id="189cd-193">To do this, use the [**ldap\_modify\_ext\_s**](/previous-versions/windows/desktop/api/winldap/nf-winldap-ldap_modify_ext_s) function with the [**LDAP\_SERVER\_SHOW\_DELETED\_OID**](/previous-versions/windows/desktop/ldap/ldap-server-show-deleted-oid) control.</span></span> <span data-ttu-id="189cd-194">修改清單必須包含 **ntSecurityDescriptor** 屬性的單一屬性取代。</span><span class="sxs-lookup"><span data-stu-id="189cd-194">The modification list must contain a single attribute replacement for the **ntSecurityDescriptor** attribute.</span></span>

 

 