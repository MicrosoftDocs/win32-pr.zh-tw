---
title: 還原已刪除的物件
description: Windows伺服器2003包括 \ 0034; 還原已刪除的物件 \ 0034;特徵。
ms.assetid: b64c5c91-fb76-4323-b78d-f692aa887c96
ms.tgt_platform: multiple
keywords:
- 還原已刪除的物件 AD
- Active Directory、使用、還原已刪除的物件
- 物件 AD，還原已刪除的物件
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 431bcddcbd15366a6accf9b8368fa8d34377b27af923fb102803b6316462634e
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/11/2021
ms.locfileid: "119025116"
---
# <a name="restoring-deleted-objects"></a>還原已刪除的物件

Windows伺服器2003包含「還原已刪除的物件」功能。

若要啟用已刪除的物件還原，網域中至少必須有一個網域控制站在 Windows Server 2003 或更新版本的 Windows 上執行。 依預設，只有網域系統管理員可以還原已刪除的物件，不過這可以委派給其他人。

下列限制適用于還原已刪除的物件：

-   物件的標記存留期到期時，物件無法還原，因為當標記存留期到期時，物件會永久刪除。
-   無法還原存在於命名內容根目錄（例如網域或應用程式分割）的物件。
-   無法還原架構物件。 不應刪除架構物件。
-   您可以還原已刪除的容器，但在刪除前還原已刪除的物件是很困難的，因為容器下的樹狀結構必須以手動方式重建。

## <a name="permissions-required-to-restore-a-deleted-object"></a>還原已刪除物件所需的許可權

刪除物件時，會保留物件安全描述項。 雖然擁有者可以從安全描述項識別，但基於安全性考慮，只有網域系統管理員可以還原已刪除的物件。 網域系統管理員可以授與許可權，以將「重新引發標記」存取權限授與使用者或群組，以將刪除物件還原至其他使用者和群組。 「重新引發標記」控制項存取權會在命名內容根目錄授與。 只有具有物件和其屬性之「讀取」存取權限的使用者，才可以在刪除物件後讀取物件和可存取的屬性。

> [!Note]  
> 授與使用者此許可權可能會造成安全性風險，因為它可能會允許使用者還原可存取使用者通常無法存取之資源的帳戶物件。 藉由還原帳戶，使用者基本上可以取得此帳戶的控制權，因為使用者必須在帳戶還原時設定帳戶的初始密碼。

 

若要完整還原已刪除的物件，使用者必須：

-   擁有或屬於具有「重新產生標記」存取權限之群組的成員。

-   對需要更新的每個必要屬性都有寫入權限。

-   具有相對分辨名稱 (RDN) 的寫入權限。

-   具有需要更新之每個選擇性屬性的寫入權限。

-   在還原物件之物件類別的目的地容器上具有子建立許可權。

    > [!Note]  
    > 在還原作業期間，不會驗證 **isDeleted** 屬性。 「刪除的物件」容器上的「刪除子」許可權都不會進行驗證。

     

## <a name="restoring-a-deleted-object"></a>還原已刪除的物件

若要還原已刪除的物件，物件必須先位於 [已刪除的物件] 容器中。 如需有關如何抓取已刪除之物件的詳細資訊，請參閱抓取 [已刪除的物件](retrieving-deleted-objects.md)。

找到物件之後，必須在單一 LDAP 作業中完成下列作業。 這需要搭配 [**ldap \_ 伺服器 \_ 顯示 \_ 已刪除的 \_ OID**](/previous-versions/windows/desktop/ldap/ldap-server-show-deleted-oid)控制項來使用 [**ldap \_ modify \_ ext \_ s**](/previous-versions/windows/desktop/api/winldap/nf-winldap-ldap_modify_ext_s)函數。

-   移除 **isDeleted** 屬性值。 **IsDeleted** 屬性值必須移除，而不是設定為 **FALSE**。
-   取代物件的辨別名稱，使其移至 [Deleted Objects] 容器以外的容器。 這可以是任何通常可以包含物件的容器。 您可以在已刪除物件的 **lastKnownParent** 屬性中找到物件先前容器的分辨名稱。 只有在 Windows Server 2003 網域控制站上刪除物件時，才會設定 **lastKnownParent** 屬性。 因此， **lastKnownParent** 屬性的內容可能不正確。
-   還原刪除期間已清除之物件的必要屬性。

> [!Note]  
> **ObjectCategory** 屬性也可以在還原物件時設定，但不是必要的。 如果未指定任何 **objectCategory** 值，則會使用物件之 **ObjectClass** 的預設 **objectCategory** 。

 

還原物件之後，就可以像在刪除它之前一樣存取它。 此時，應還原任何重要的選擇性屬性。 您也必須還原目錄中其他物件的物件參考。

做為安全性措施，使用者物件會在還原時停用。 還原選用的屬性之後，必須啟用使用者物件，以允許使用使用者物件。

如需詳細資訊和示範如何還原已刪除物件的程式碼範例，請參閱下面的 RestoreDeletedObject 函數。

## <a name="restoredeletedobject"></a>RestoreDeletedObject

下列 c + + 程式碼範例顯示如何還原已刪除的物件。


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



 

 