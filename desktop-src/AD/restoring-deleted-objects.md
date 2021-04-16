---
title: 還原已刪除的物件
description: Windows Server 2003 包含 \ 0034; 還原已刪除的物件 \ 0034;特徵。
ms.assetid: b64c5c91-fb76-4323-b78d-f692aa887c96
ms.tgt_platform: multiple
keywords:
- 還原已刪除的物件 AD
- Active Directory、使用、還原已刪除的物件
- 物件 AD，還原已刪除的物件
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 2f8f1d3511bb4246826e677aa239ca594918127a
ms.sourcegitcommit: 803f3ccd65bdefe36bd851b9c6e7280be9489016
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/17/2020
ms.locfileid: "104507859"
---
# <a name="restoring-deleted-objects"></a><span data-ttu-id="0e1d1-106">還原已刪除的物件</span><span class="sxs-lookup"><span data-stu-id="0e1d1-106">Restoring Deleted Objects</span></span>

<span data-ttu-id="0e1d1-107">Windows Server 2003 包含「還原已刪除的物件」功能。</span><span class="sxs-lookup"><span data-stu-id="0e1d1-107">Windows Server 2003 includes the "restore deleted objects" feature.</span></span>

<span data-ttu-id="0e1d1-108">若要啟用已刪除的物件還原，網域中至少有一個網域控制站必須在 Windows Server 2003 或更新版本的 Windows 上執行。</span><span class="sxs-lookup"><span data-stu-id="0e1d1-108">To enable deleted object restoration, at least one domain controller in the domain must be running on Windows Server 2003 or a later version of Windows.</span></span> <span data-ttu-id="0e1d1-109">依預設，只有網域系統管理員可以還原已刪除的物件，不過這可以委派給其他人。</span><span class="sxs-lookup"><span data-stu-id="0e1d1-109">By default, only domain administrators can restore deleted objects, though this can be delegated to others.</span></span>

<span data-ttu-id="0e1d1-110">下列限制適用于還原已刪除的物件：</span><span class="sxs-lookup"><span data-stu-id="0e1d1-110">The following limitations apply to restoring deleted objects:</span></span>

-   <span data-ttu-id="0e1d1-111">物件的標記存留期到期時，物件無法還原，因為當標記存留期到期時，物件會永久刪除。</span><span class="sxs-lookup"><span data-stu-id="0e1d1-111">An object cannot be restored when the tombstone lifetime for the object has expired because when the tombstone lifetime has expired, the object is permanently deleted.</span></span>
-   <span data-ttu-id="0e1d1-112">無法還原存在於命名內容根目錄（例如網域或應用程式分割）的物件。</span><span class="sxs-lookup"><span data-stu-id="0e1d1-112">Objects that exist at the root of the naming context, such as a domain or application partition, cannot be restored.</span></span>
-   <span data-ttu-id="0e1d1-113">無法還原架構物件。</span><span class="sxs-lookup"><span data-stu-id="0e1d1-113">Schema objects cannot be restored.</span></span> <span data-ttu-id="0e1d1-114">不應刪除架構物件。</span><span class="sxs-lookup"><span data-stu-id="0e1d1-114">Schema objects should never be deleted.</span></span>
-   <span data-ttu-id="0e1d1-115">您可以還原已刪除的容器，但在刪除前還原已刪除的物件是很困難的，因為容器下的樹狀結構必須以手動方式重建。</span><span class="sxs-lookup"><span data-stu-id="0e1d1-115">It is possible to restore deleted containers, but the restoration of the deleted objects that were in the container before the deletion is difficult because the tree structure under the container must be manually reconstructed.</span></span>

## <a name="permissions-required-to-restore-a-deleted-object"></a><span data-ttu-id="0e1d1-116">還原已刪除物件所需的許可權</span><span class="sxs-lookup"><span data-stu-id="0e1d1-116">Permissions Required to Restore a Deleted Object</span></span>

<span data-ttu-id="0e1d1-117">刪除物件時，會保留物件安全描述項。</span><span class="sxs-lookup"><span data-stu-id="0e1d1-117">When an object is deleted, the object security descriptor is retained.</span></span> <span data-ttu-id="0e1d1-118">雖然擁有者可以從安全描述項識別，但基於安全性考慮，只有網域系統管理員可以還原已刪除的物件。</span><span class="sxs-lookup"><span data-stu-id="0e1d1-118">Although the owner is identifiable from the security descriptor, for security reasons, only domain administrators are allowed to restore deleted objects.</span></span> <span data-ttu-id="0e1d1-119">網域系統管理員可以授與許可權，以將「重新引發標記」存取權限授與使用者或群組，以將刪除物件還原至其他使用者和群組。</span><span class="sxs-lookup"><span data-stu-id="0e1d1-119">Domain administrators can grant the permission to restore delete objects to other users and groups by granting the user or group the "Reanimate Tombstone" control access right.</span></span> <span data-ttu-id="0e1d1-120">「重新引發標記」控制項存取權會在命名內容根目錄授與。</span><span class="sxs-lookup"><span data-stu-id="0e1d1-120">The "Reanimate Tombstone" control access right is granted at the Naming Context root.</span></span> <span data-ttu-id="0e1d1-121">只有具有物件和其屬性之「讀取」存取權限的使用者，才可以在刪除物件後讀取物件和可存取的屬性。</span><span class="sxs-lookup"><span data-stu-id="0e1d1-121">Only users that had read access permission on an object and its attributes are permitted to read the object and accessible attributes after the object is deleted.</span></span>

> [!Note]  
> <span data-ttu-id="0e1d1-122">授與使用者此許可權可能會造成安全性風險，因為它可能會允許使用者還原可存取使用者通常無法存取之資源的帳戶物件。</span><span class="sxs-lookup"><span data-stu-id="0e1d1-122">Granting a user this permission can be a security risk because it could permit the user to restore an account object that has access to resources that the user would not normally have access to.</span></span> <span data-ttu-id="0e1d1-123">藉由還原帳戶，使用者基本上可以取得此帳戶的控制權，因為使用者必須在帳戶還原時設定帳戶的初始密碼。</span><span class="sxs-lookup"><span data-stu-id="0e1d1-123">By restoring an account, the user essentially gains control of this account because the user must set the initial password on the account when the account is restored.</span></span>

 

<span data-ttu-id="0e1d1-124">若要完整還原已刪除的物件，使用者必須：</span><span class="sxs-lookup"><span data-stu-id="0e1d1-124">To completely restore a deleted object, the user must:</span></span>

-   <span data-ttu-id="0e1d1-125">擁有或屬於具有「重新產生標記」存取權限之群組的成員。</span><span class="sxs-lookup"><span data-stu-id="0e1d1-125">Have, or be a member of a group that has, the "Reanimate Tombstone" control access right.</span></span>

-   <span data-ttu-id="0e1d1-126">對需要更新的每個必要屬性都有寫入權限。</span><span class="sxs-lookup"><span data-stu-id="0e1d1-126">Have write access for each mandatory attribute that requires updating.</span></span>

-   <span data-ttu-id="0e1d1-127">具有相對分辨名稱 (RDN) 的寫入權限。</span><span class="sxs-lookup"><span data-stu-id="0e1d1-127">Have write access to the Relative Distinguished Name (RDN).</span></span>

-   <span data-ttu-id="0e1d1-128">具有需要更新之每個選擇性屬性的寫入權限。</span><span class="sxs-lookup"><span data-stu-id="0e1d1-128">Have write access to each optional attribute that needs to be updated.</span></span>

-   <span data-ttu-id="0e1d1-129">在還原物件之物件類別的目的地容器上具有子建立許可權。</span><span class="sxs-lookup"><span data-stu-id="0e1d1-129">Have child-creation rights on the destination container for the object class of restored object.</span></span>

    > [!Note]  
    > <span data-ttu-id="0e1d1-130">在還原作業期間，不會驗證 **isDeleted** 屬性。</span><span class="sxs-lookup"><span data-stu-id="0e1d1-130">The **isDeleted** attribute is not verified during the restore operation.</span></span> <span data-ttu-id="0e1d1-131">「刪除的物件」容器上的「刪除子」許可權都不會進行驗證。</span><span class="sxs-lookup"><span data-stu-id="0e1d1-131">Neither will the delete-child permission on the "Deleted Objects" container be verified.</span></span>

     

## <a name="restoring-a-deleted-object"></a><span data-ttu-id="0e1d1-132">還原已刪除的物件</span><span class="sxs-lookup"><span data-stu-id="0e1d1-132">Restoring a Deleted Object</span></span>

<span data-ttu-id="0e1d1-133">若要還原已刪除的物件，物件必須先位於 [已刪除的物件] 容器中。</span><span class="sxs-lookup"><span data-stu-id="0e1d1-133">To restore a deleted object, the object must first be located in the Deleted Objects container.</span></span> <span data-ttu-id="0e1d1-134">如需有關如何抓取已刪除之物件的詳細資訊，請參閱抓取 [已刪除的物件](retrieving-deleted-objects.md)。</span><span class="sxs-lookup"><span data-stu-id="0e1d1-134">For more information about retrieving deleted objects, see [Retrieving Deleted Objects](retrieving-deleted-objects.md).</span></span>

<span data-ttu-id="0e1d1-135">找到物件之後，必須在單一 LDAP 作業中完成下列作業。</span><span class="sxs-lookup"><span data-stu-id="0e1d1-135">When the object has been located, the following operations must be completed in a single LDAP operation.</span></span> <span data-ttu-id="0e1d1-136">這需要搭配 [**ldap \_ 伺服器 \_ 顯示 \_ 已刪除的 \_ OID**](/previous-versions/windows/desktop/ldap/ldap-server-show-deleted-oid)控制項來使用 [**ldap \_ modify \_ ext \_ s**](/previous-versions/windows/desktop/api/winldap/nf-winldap-ldap_modify_ext_s)函數。</span><span class="sxs-lookup"><span data-stu-id="0e1d1-136">This requires the use of the [**ldap\_modify\_ext\_s**](/previous-versions/windows/desktop/api/winldap/nf-winldap-ldap_modify_ext_s) function with the [**LDAP\_SERVER\_SHOW\_DELETED\_OID**](/previous-versions/windows/desktop/ldap/ldap-server-show-deleted-oid) control.</span></span>

-   <span data-ttu-id="0e1d1-137">移除 **isDeleted** 屬性值。</span><span class="sxs-lookup"><span data-stu-id="0e1d1-137">Remove the **isDeleted** attribute value.</span></span> <span data-ttu-id="0e1d1-138">**IsDeleted** 屬性值必須移除，而不是設定為 **FALSE**。</span><span class="sxs-lookup"><span data-stu-id="0e1d1-138">The **isDeleted** attribute value must be removed, not set to **FALSE**.</span></span>
-   <span data-ttu-id="0e1d1-139">取代物件的辨別名稱，使其移至 [Deleted Objects] 容器以外的容器。</span><span class="sxs-lookup"><span data-stu-id="0e1d1-139">Replace the distinguished name of the object so that it is moved to a container other than the Deleted Objects container.</span></span> <span data-ttu-id="0e1d1-140">這可以是任何通常可以包含物件的容器。</span><span class="sxs-lookup"><span data-stu-id="0e1d1-140">This can be any container that can normally contain the object.</span></span> <span data-ttu-id="0e1d1-141">您可以在已刪除物件的 **lastKnownParent** 屬性中找到物件先前容器的分辨名稱。</span><span class="sxs-lookup"><span data-stu-id="0e1d1-141">The distinguished name of the previous container of the object can be found in the deleted object's **lastKnownParent** attribute.</span></span> <span data-ttu-id="0e1d1-142">只有在 Windows Server 2003 網域控制站上刪除了物件時，才會設定 **lastKnownParent** 屬性。</span><span class="sxs-lookup"><span data-stu-id="0e1d1-142">The **lastKnownParent** attribute is only set if the object was deleted on a Windows Server 2003 domain controller.</span></span> <span data-ttu-id="0e1d1-143">因此， **lastKnownParent** 屬性的內容可能不正確。</span><span class="sxs-lookup"><span data-stu-id="0e1d1-143">Thus, it is possible that the content of the **lastKnownParent** attribute is inaccurate.</span></span>
-   <span data-ttu-id="0e1d1-144">還原刪除期間已清除之物件的必要屬性。</span><span class="sxs-lookup"><span data-stu-id="0e1d1-144">Restore the mandatory attributes for the object that were cleared during deletion.</span></span>

> [!Note]  
> <span data-ttu-id="0e1d1-145">**ObjectCategory** 屬性也可以在還原物件時設定，但不是必要的。</span><span class="sxs-lookup"><span data-stu-id="0e1d1-145">The **objectCategory** attribute can also be set when the object is restored, but is not required.</span></span> <span data-ttu-id="0e1d1-146">如果未指定任何 **objectCategory** 值，則會使用物件之 **ObjectClass** 的預設 **objectCategory** 。</span><span class="sxs-lookup"><span data-stu-id="0e1d1-146">If no **objectCategory** value is specified, the default **objectCategory** for the object's **objectClass** is used.</span></span>

 

<span data-ttu-id="0e1d1-147">還原物件之後，就可以像在刪除它之前一樣存取它。</span><span class="sxs-lookup"><span data-stu-id="0e1d1-147">After the object is restored, it can be accessed as it was before it was deleted.</span></span> <span data-ttu-id="0e1d1-148">此時，應還原任何重要的選擇性屬性。</span><span class="sxs-lookup"><span data-stu-id="0e1d1-148">At this point, any optional attributes that are important should be restored.</span></span> <span data-ttu-id="0e1d1-149">您也必須還原目錄中其他物件的物件參考。</span><span class="sxs-lookup"><span data-stu-id="0e1d1-149">Any references to the object from other objects in the directory must also be restored.</span></span>

<span data-ttu-id="0e1d1-150">做為安全性措施，使用者物件會在還原時停用。</span><span class="sxs-lookup"><span data-stu-id="0e1d1-150">As a security measure, user objects are disabled when they are restored.</span></span> <span data-ttu-id="0e1d1-151">還原選用的屬性之後，必須啟用使用者物件，以允許使用使用者物件。</span><span class="sxs-lookup"><span data-stu-id="0e1d1-151">User objects must be enabled after restoring the optional attributes to allow the user object to be used.</span></span>

<span data-ttu-id="0e1d1-152">如需詳細資訊和示範如何還原已刪除物件的程式碼範例，請參閱下面的 RestoreDeletedObject 函數。</span><span class="sxs-lookup"><span data-stu-id="0e1d1-152">For more information and a code example that shows how to restore a deleted object, see the RestoreDeletedObject function below.</span></span>

## <a name="restoredeletedobject"></a><span data-ttu-id="0e1d1-153">RestoreDeletedObject</span><span class="sxs-lookup"><span data-stu-id="0e1d1-153">RestoreDeletedObject</span></span>

<span data-ttu-id="0e1d1-154">下列 c + + 程式碼範例顯示如何還原已刪除的物件。</span><span class="sxs-lookup"><span data-stu-id="0e1d1-154">The following C++ code example shows how to restore a deleted object.</span></span>


```C++
//***************************************************************************
//
//  RestoreDeletedObject()
//
//  Restores a deleted object. 
//
//  pwszDeletedDN - Contains the fully qualified distinguished name of the 
//  deleted object.
//
//  pwszDestContainerDN - Contains the fully qualified distinguished name of 
//  the folder that the deleted object should be moved to.
//
//  Returns S_OK if successful or an HRESULT or LDAP error code otherwise.
//
//***************************************************************************

HRESULT RestoreDeletedObject(LPCWSTR pwszDeletedDN, LPCWSTR pwszDestContainerDN)
{
    if((NULL == pwszDeletedDN) || (NULL == pwszDestContainerDN))
    {
        return E_POINTER;
    }
    
    HRESULT hr = E_FAIL;

    // Build the new distinguished name.
    LPWSTR pwszNewDN = new WCHAR[lstrlenW(pwszDeletedDN) + lstrlenW(pwszDestContainerDN) + 1];
    if(pwszNewDN)
    {
        wcscpy_s(pwszNewDN, pwszDeletedDN);

        // Search for the first 0x0A character. This is the delimiter in the deleted object name.
        LPWSTR pwszChar;
        for(pwszChar = pwszNewDN; *pwszChar; pwszChar = CharNextW(pwszChar))
        {
            if(('\\' == *pwszChar) && ('0' == *(pwszChar + 1)) && ('A' == *(pwszChar + 2)))
            {
                break;
            }
            
        }

        if(0 != *pwszChar)
        {
            // Truncate the name string at the delimiter.
            *pwszChar = 0;

            // Add the last known parent DN to complete the DN.
            wcscat_s(pwszNewDN, L",");
            wcscat_s(pwszNewDN, pwszDestContainerDN);

            PLDAP ld;

            // Initialize LDAP.
            ld = ldap_init(NULL, LDAP_PORT);
            if(NULL != ld) 
            {
                ULONG ulRC;
                ULONG version = LDAP_VERSION3;

                // Set the LDAP version.
                ulRC = ldap_set_option(ld, LDAP_OPT_PROTOCOL_VERSION, (void*)&version);
                if(LDAP_SUCCESS == ulRC)
                {
                    // Establish a connection with the server.
                    ulRC = ldap_connect(ld, NULL);
                    if(LDAP_SUCCESS == ulRC)
                    {                    
                        // Bind to the LDAP server.
                        ulRC = ldap_bind_s(ld, NULL, NULL, LDAP_AUTH_NEGOTIATE);
                        if(LDAP_SUCCESS == ulRC)
                        {
                            // Setup the new values.
                            LPWSTR rgNewVals[] = {pwszNewDN, NULL};

                            /*
                            Remove the isDeleted attribute. This cannot be set 
                            to FALSE or the restore operation will not work.
                            */
                            LDAPModW modIsDeleted = { LDAP_MOD_DELETE, L"isDeleted", NULL };

                            /*
                            Set the new DN, in effect, moving the deleted 
                            object to where it resided before the deletion.
                            */
                            LDAPModW modDN = { LDAP_MOD_REPLACE, L"distinguishedName", rgNewVals };
                            
                            // Initialize the LDAPMod structure.
                            PLDAPModW ldapMods[] = 
                            {
                                &modIsDeleted,
                                &modDN,
                                NULL
                            };

                            /*
                            Use the LDAP_SERVER_SHOW_DELETED_OID control to 
                            modify deleted objects.
                            */
                            LDAPControlW showDeletedControl;
                            showDeletedControl.ldctl_oid = LDAP_SERVER_SHOW_DELETED_OID_W;
                            showDeletedControl.ldctl_value.bv_len = 0;
                            showDeletedControl.ldctl_value.bv_val = NULL;
                            showDeletedControl.ldctl_iscritical = TRUE;

                            // Initialzie the LDAPControl structure
                            PLDAPControlW ldapControls[] = { &showDeletedControl, NULL };

                            /*
                            Modify the specified attributes. This must performed 
                            in one step, which is why the LDAP APIs must be used 
                            to restore a deleted object.
                            */
                            ulRC = ldap_modify_ext_sW(ld, (PWCHAR)pwszDeletedDN, ldapMods, ldapControls, NULL);
                            if(LDAP_SUCCESS == ulRC)
                            {
                                hr = S_OK;
                            }
                            else if(LDAP_ALREADY_EXISTS == ulRC)
                            {
                                /*
                                An object already exists with the specified name 
                                in the specified target container. At this point, 
                                a new name must be selected.
                                */
                            }
                        }
                    }
                }

                if(LDAP_SUCCESS != ulRC)
                {
                    hr = ulRC;
                    
                    OutputDebugString(ldap_err2string(ulRC));
                }

                // Release the LDAP session.
                ldap_unbind(ld);
            }
        }
        else
        {
            /*
            If the end of the string is reached before the delimiter is found, just 
            end and fail.
            */
            hr = E_INVALIDARG;
        }
    
        delete pwszNewDN;
    }
    else
    {
        hr = E_OUTOFMEMORY;
    }

    return hr;
}

```



 

 