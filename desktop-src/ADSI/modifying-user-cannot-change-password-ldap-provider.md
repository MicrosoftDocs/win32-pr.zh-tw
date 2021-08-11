---
title: 修改使用者無法變更 LDAP 提供者) 的密碼 (
description: 使用者變更其密碼的能力是可以授與或拒絕的許可權。
ms.assetid: 9d5c2d6a-9997-4d0c-b896-bf1b578e64ac
ms.tgt_platform: multiple
keywords:
- 修改使用者無法變更 LDAP 提供者) ADSI 的密碼 (
- 使用者無法變更密碼 (LDAP 提供者) ADSI，修改
- LDAP 提供者 ADSI、使用者管理範例、使用者必須在下次登入時變更密碼，以及修改
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: ec664f9a79e0de4ff0b75ae31abd8dc1532cd17c0d3d35a934e094da45eb3383
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/11/2021
ms.locfileid: "118179016"
---
# <a name="modifying-user-cannot-change-password-ldap-provider"></a>修改使用者無法變更 LDAP 提供者) 的密碼 (

使用者變更其密碼的能力是可以授與或拒絕的許可權。 若要拒絕此許可權，請在安全描述項的任意存取控制清單中，將兩個 Ace 設定為 **\_ ACETYPE \_ \_ 拒絕存取 \_ 物件** ace 類型之使用者物件的 (DACL) 。 一個 ACE 會拒絕使用者的許可權，而另一個 ACE 會拒絕 Everyone 群組的許可權。 這兩個 Ace 都是物件特定的拒絕 Ace，可指定用來變更密碼的擴充許可權 GUID。 若要授與此許可權，請使用 **ADS \_ ACETYPE \_ ACCESS 允許的 \_ \_ 物件** Ace 類型來設定相同的 ace。

下列程式描述如何修改或加入此許可權的 Ace。

**修改或加入此許可權的 Ace**

1.  系結至使用者物件。
2.  從 user 物件的 **ntSecurityDescriptor** 屬性取得 [**IADsSecurityDescriptor**](/windows/desktop/api/Iads/nn-iads-iadssecuritydescriptor)物件。
3.  從 [**IADsSecurityDescriptor objdescriptor.discretionaryacl**](iadssecuritydescriptor-property-methods.md)屬性取得安全描述項的 [**IADsAccessControlList**](/windows/desktop/api/Iads/nn-iads-iadsaccesscontrollist)介面。
4.  列舉物件的 Ace，並搜尋具有 [**IADsAccessControlEntry ObjectType**](iadsaccesscontrolentry-property-methods.md) 屬性之變更密碼 GUID ( {AB721A53-1E2F-11D0-9819-00AA0040529B} ) 的 ace，以及 \\ **IADsAccessControlEntry 的** 屬性的 "EVERYONE" 或 "NT 授權單位"。

    > [!Note]  
    > "Everyone" 和 "NT 授權單位 \\ SELF" 字串會根據網域中第一個網域控制站的語言進行當地語系化。 因此，不應該直接使用字串。 您應該在執行時間取得帳戶名稱，方法是呼叫 [**LookupAccountSid**](/windows/desktop/api/winbase/nf-winbase-lookupaccountsida) 函式，並使用 "Everyone" ( "s-1-1-0" ) 和 "NT 授權單位 \\ SELF" ( "S-1-5-10" ) 已知的安全性主體。 讀取使用者所顯示的 **GetSidAccountName**、 **GetSidAccountName \_ Everyone** 和 **GetSidAccountName \_ Self** c + + 範例函式 [無法 (LDAP 提供者變更密碼)](reading-user-cannot-change-password-ldap-provider.md) 示範如何進行這項操作。

     

5.  如果使用者無法變更密碼或 **ads \_ AceType \_ 存取 \_ 允許的 \_ 物件**（如果使用者可以變更其密碼），請修改找到之 ace 的 [**IADsAccessControlEntry. AceType**](iadsaccesscontrolentry-property-methods.md)屬性，以 **\_ AceType \_ 拒絕存取的 \_ \_ 物件**。
6.  如果找不到「Everyone」 ACE，請建立新的 [**IADsAccessControlEntry**](/windows/desktop/api/Iads/nn-iads-iadsaccesscontrolentry) 物件，其中包含下表所示的屬性值，並使用 [**IADsAccessControlList. AddAce**](/windows/desktop/api/Iads/nf-iads-iadsaccesscontrollist-addace) 方法將新的專案新增至 ACL。
7.  如果找不到「NT 授權單位」 \\ ACE，請使用下表所示的相同屬性值建立新的 [**IADsAccessControlEntry**](/windows/desktop/api/Iads/nn-iads-iadsaccesscontrolentry) 物件，但是 [**信任者**](iadsaccesscontrolentry-property-methods.md) 屬性包含 SID "S-1-5-10" ( "NT 授權單位 \\ self" ) 的帳戶名稱。 使用 [**IADsAccessControlList. AddAce**](/windows/desktop/api/Iads/nf-iads-iadsaccesscontrollist-addace) 方法將專案新增至 ACL。
8.  若要更新物件的 **ntSecurityDescriptor** 屬性，請使用在步驟2中取得的相同 [**IADsSecurityDescriptor**](/windows/desktop/api/Iads/nn-iads-iadssecuritydescriptor)來呼叫 [**IADs. Put**](/windows/desktop/api/Iads/nf-iads-iads-put)方法。
9.  使用 [**IADs. SetInfo**](/windows/desktop/api/Iads/nf-iads-iads-setinfo) 方法來認可伺服器的本機變更。
10. 如果其中一個 Ace 已建立，您就必須重新排列 ACL，使 Ace 的順序正確。 若要這樣做，請使用物件的 LDAP ADsPath 呼叫 [**GetNamedSecurityInfo**](/windows/desktop/api/aclapi/nf-aclapi-getnamedsecurityinfoa) 函式，然後使用相同的 DACL 來呼叫 [**SetNamedSecurityInfo**](/windows/desktop/api/aclapi/nf-aclapi-setnamedsecurityinfoa) 函數。 加入 Ace 時，會自動進行重新排列。

下表列出 [**IADsAccessControlEntry**](/windows/desktop/api/Iads/nn-iads-iadsaccesscontrolentry) 物件屬性值。



| IADsAccessControlEntry 屬性                                        | 值                                                                                                                                                                 |
|------------------------------------------------------------------------|-----------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [**AccessMask**](iadsaccesscontrolentry-property-methods.md)          | **ADS \_ 正確的 \_ DS \_ 控制 \_ 存取**                                                                                                                                   |
| [**AceType**](iadsaccesscontrolentry-property-methods.md)             | **廣告 \_ACETYPE \_ \_ 拒絕存取 \_ 物件** 如果使用者無法變更其密碼或 **ADS \_ ACETYPE \_ 存取允許的 \_ \_ 物件** （如果使用者可以變更其密碼）。 |
| [**AceFlags**](iadsaccesscontrolentry-property-methods.md)            | 0                                                                                                                                                                     |
| [**標誌**](iadsaccesscontrolentry-property-methods.md)               | **ADS \_ 旗標 \_ 物件 \_ 類型 \_ 存在**                                                                                                                                  |
| [**ObjectType**](iadsaccesscontrolentry-property-methods.md)          | "{AB721A53-1E2F-11D0-9819-00AA0040529B}"，也就是字串格式的變更密碼 GUID。                                                                            |
| [**InheritedObjectType**](iadsaccesscontrolentry-property-methods.md) | 未使用                                                                                                                                                              |
| [**受託 人**](iadsaccesscontrolentry-property-methods.md)             | SID "S-1-1-0" 的帳戶名稱 (每個人) 。                                                                                                                            |



 

## <a name="example-code"></a>範例程式碼

下列程式碼範例示範如何取得介面來變更 DACL。 您可以藉由設定 **ADS \_ 安全性 \_ 資訊 \_ DACL** 選項來使用 [**IADsObjectOptions**](/windows/desktop/api/Iads/nn-iads-iadsobjectoptions)介面。

> [!Note]  
> 若要使用此範例中記載的程式碼，您必須是系統管理員。 如果您不是系統管理員，則需要加入更多程式碼，以使用可讓使用者變更用戶端快取重新排回 Active Directory 網域服務方式的介面。

 


```C++
//
// Obtain an IADsObjectOptions interface from the object whose
// DACL you wish to modify.
//
long CanReadSetDACL = ADS_SECURITY_INFO_DACL;

CComPtr<IADsObjectOptions> spObjOps;

hr = pads->QueryInterface(IID_IADsObjectOptions, (void**)&spObjOps);

if(SUCCEEDED(hr))

{

//
// Set the option mask you want to change. In this case
// we want to change the objects security information, so we'll
// use the ADS_OPTION_SECURITY_MASK. Since we want to modify the 
// DACL, we'll set the variant to ADS_SEDCURITY_INFO_DACL flag. 
//

    CComVariant svar;
    svar = CanReadSetDACL;
    hr = spObjOps->SetOption(ADS_OPTION_SECURITY_MASK, svar); 

}
//
// The smart pointer declared for pObjOptions can be released
// or it will be destroyed and released once the pointer goes 
// out of scope.
//

```



下列程式碼範例顯示如何使用 LDAP 提供者修改使用者無法變更密碼許可權。 這個程式碼範例會使用上面定義的 **GetObjectACE** 公用程式函數。

此範例會使用 GetSidAccountName 中所示的「 **\_ 所有人** 」和 **GetSidAccountName \_ 自我** c + + 範例函式， [ (LDAP 提供者) 變更密碼](reading-user-cannot-change-password-ldap-provider.md)。


```C++
#include <aclapi.h>

#define CHANGE_PASSWORD_GUID_W L"{AB721A53-1E2F-11D0-9819-00AA0040529B}"

/***************************************************************************

    CreateACE()

    Creates an ACE and returns the IDispatch pointer for the ACE. This 
    pointer can be passed directly to IADsAccessControlList::AddAce.

    bstrTrustee - Contains the Trustee for the ACE.

    bstrObjectType - Contains the ObjectType for the ACE.

    lAccessMask - Contains the AccessMask for the ACE.

    lACEType - Contains the ACEType for the ACE.

    lACEFlags - Contains the ACEFlags for the ACE.

    lFlags - Contains the Flags for the ACE.

***************************************************************************/

IDispatch* CreateACE(BSTR bstrTrustee, 
                     BSTR bstrObjectType, 
                     long lAccessMask, 
                     long lACEType, 
                     long lACEFlags, 
                     long lFlags)
{
    HRESULT hr;
    IDispatch *pDisp = NULL;
    IADsAccessControlEntry *pACE = NULL;

    hr = CoCreateInstance(CLSID_AccessControlEntry,
                          NULL,
                          CLSCTX_INPROC_SERVER,
                          IID_IADsAccessControlEntry,
                          (void**)&pACE);
    if(SUCCEEDED(hr)) 
    {
        hr = pACE->put_Trustee(bstrTrustee); 
        hr = pACE->put_ObjectType(bstrObjectType);
        hr = pACE->put_AccessMask(lAccessMask); 
        hr = pACE->put_AceType(lACEType);
        hr = pACE->put_AceFlags(lACEFlags);
        hr = pACE->put_Flags(lFlags);

        hr = pACE->QueryInterface(IID_IDispatch, (LPVOID*)&pDisp);

        pACE->Release();
    }

    return pDisp;
}

/***************************************************************************

    ReorderACEs()

    Causes the ACEs of an object DACL to be reordered properly. The ACEs are 
    automatically put in the proper order when they are added to the DACL. 
    On older systems however, this does not occur automatically, so this 
    function is necessary so the deny ACEs are ordered in the list before 
    the allow ACEs.

    pwszDN - A null-terminated Unicode string that contains the LDAP 
    ADsPath of the DS object to reorder the DACL for.

***************************************************************************/

HRESULT ReorderACEs(LPCWSTR pwszDN)
{
    HRESULT hr = E_FAIL;
    DWORD dwResult;
    ACL *pdacl;
    PSECURITY_DESCRIPTOR psd;
    
    dwResult = GetNamedSecurityInfoW(   (LPWSTR)pwszDN,
                                        SE_DS_OBJECT_ALL,
                                        DACL_SECURITY_INFORMATION,
                                        NULL,
                                        NULL,
                                        &pdacl,
                                        NULL,
                                        &psd);

    if(ERROR_SUCCESS == dwResult)
    {
        dwResult = SetNamedSecurityInfoW(   (LPWSTR)pwszDN,
                                            SE_DS_OBJECT_ALL,
                                            DACL_SECURITY_INFORMATION,
                                            NULL,
                                            NULL,
                                            pdacl,
                                            NULL);

        LocalFree(psd);
        
        if(ERROR_SUCCESS == dwResult)
        {
            hr = S_OK;
        }
    }
    
    return hr;
}

/***************************************************************************

    SetUserCannotChangePassword()

    Sets the "User Cannot Change Password" permission using the LDAP provider 
    to the specified setting. To do this, find the existing 
    ACEs and modify the AceType. If the ACE is not found, a new one of the 
    proper type is created and added. The ACEs should always be present, but 
    it is possible that the default DACL excludes them, so this situation 
    will be handled correctly.

    pwszUserDN - A null-terminated Unicode string that contains the LDAP 
    ADsPath of the user object to modify.

    pwszUsername - A null-terminated Unicode string that contains the user 
    name to use for authorization. If this is NULL, the credentials of the 
    current user are used.

    pwszPassword - A null-terminated Unicode string that contains the 
    password to use for authorization. This is ignored if pwszUsername is 
    NULL.

    fCannotChangePassword - Contains the new setting for the privilege. 
    Contains nonzero if the user cannot change their password or zero if 
    the can change their password.

***************************************************************************/

HRESULT SetUserCannotChangePassword(LPCWSTR pwszUserDN, 
                                    LPCWSTR pwszUsername, 
                                    LPCWSTR pwszPassword,
                                    BOOL fCannotChangePassword)
{
    HRESULT hr;

    CComBSTR sbstrEveryone;
    hr = GetSidAccountName_Everyone(&sbstrEveryone);
    if(FAILED(hr))
    {
        return hr;
    }

    CComBSTR sbstrSelf;
    hr = GetSidAccountName_Self(&sbstrSelf);
    if(FAILED(hr))
    {
        return hr;
    }

    if(NULL == pwszUserDN)
    {
        return E_INVALIDARG;
    }
    
    IADs *pads;

    hr = ADsOpenObject( pwszUserDN,
                        pwszUsername,
                        pwszPassword,
                        ADS_SECURE_AUTHENTICATION,
                        IID_IADs, 
                        (LPVOID*)&pads);

    if(SUCCEEDED(hr))
    {
        CComBSTR sbstrSecDesc = "ntSecurityDescriptor";
        CComVariant svar;
        
        hr = pads->Get(sbstrSecDesc, &svar);
        if(SUCCEEDED(hr))
        {
            IADsSecurityDescriptor *psd;

            hr = svar.pdispVal->QueryInterface(IID_IADsSecurityDescriptor, (LPVOID*)&psd);
            if(SUCCEEDED(hr))
            {
                IDispatch *pDisp;

                hr = psd->get_DiscretionaryAcl(&pDisp);
                if(SUCCEEDED(hr))
                {
                    IADsAccessControlList *pACL;

                    hr = pDisp->QueryInterface(IID_IADsAccessControlList, (void**)&pACL);
                    if(SUCCEEDED(hr)) 
                    {
                        BOOL fMustReorder = FALSE;
                        /*
                        Get the existing ACE for the change password permission 
                        for Everyone. If it exists, just modify the existing 
                        ACE. If it does not exist, create a new one and add it 
                        to the ACL.
                        */
                        IADsAccessControlEntry *pACEEveryone = NULL;
                        hr = GetObjectACE(pACL, CHANGE_PASSWORD_GUID_W, sbstrEveryone, &pACEEveryone);
                        if(pACEEveryone)
                        {
                            hr = pACEEveryone->put_AceType(fCannotChangePassword ? 
                                ADS_ACETYPE_ACCESS_DENIED_OBJECT : 
                                ADS_ACETYPE_ACCESS_ALLOWED_OBJECT);

                            pACEEveryone->Release();
                        }
                        else
                        {
                            IDispatch *pDispEveryone = NULL;
                            
                            pDispEveryone = CreateACE(sbstrEveryone, 
                                CComBSTR(CHANGE_PASSWORD_GUID_W),
                                ADS_RIGHT_DS_CONTROL_ACCESS, 
                                fCannotChangePassword ? 
                                    ADS_ACETYPE_ACCESS_DENIED_OBJECT : 
                                    ADS_ACETYPE_ACCESS_ALLOWED_OBJECT, 
                                0,
                                ADS_FLAG_OBJECT_TYPE_PRESENT);
                            
                            if(pDispEveryone)
                            {
                                //add the new ACE for everyone
                                hr = pACL->AddAce(pDispEveryone);

                                pDispEveryone->Release();

                                fMustReorder = TRUE;
                            }                            
                        }
                        
                        /*
                        Get the existing ACE for the change password permission 
                        for Self. If it exists, just modify the existing 
                        ACE. If it does not exist, create a new one and add it 
                        to the ACL.
                        */
                        IADsAccessControlEntry *pACESelf = NULL;
                        hr = GetObjectACE(pACL, CHANGE_PASSWORD_GUID_W, sbstrSelf, &pACESelf);
                        if(pACESelf)
                        {
                            hr = pACESelf->put_AceType(fCannotChangePassword ? 
                                ADS_ACETYPE_ACCESS_DENIED_OBJECT : 
                                ADS_ACETYPE_ACCESS_ALLOWED_OBJECT);
                        
                            pACESelf->Release();
                        }
                        else
                        {
                            IDispatch *pDispSelf = NULL;
                            
                            pDispSelf = CreateACE(sbstrSelf, 
                                CComBSTR(CHANGE_PASSWORD_GUID_W),
                                ADS_RIGHT_DS_CONTROL_ACCESS, 
                                fCannotChangePassword ? 
                                    ADS_ACETYPE_ACCESS_DENIED_OBJECT : 
                                    ADS_ACETYPE_ACCESS_ALLOWED_OBJECT, 
                                0,
                                ADS_FLAG_OBJECT_TYPE_PRESENT);

                            if(pDispSelf)
                            {
                                //add the new ACE for self
                                hr = pACL->AddAce(pDispSelf);

                                pDispSelf->Release();

                                fMustReorder = TRUE;
                            }                            
                        }

                        //update the security descriptor property
                        hr = pads->Put(sbstrSecDesc, svar);
                        
                        //commit the changes
                        hr = pads->SetInfo();

                        if(fMustReorder)
                        {
                            ReorderACEs(pwszUserDN);
                        }

                        pACL->Release();
                    }

                    pDisp->Release();
                }
                
                psd->Release();
            }
        }
    }

    return hr;
}
```



下列程式碼範例顯示如何使用 LDAP 提供者修改使用者無法變更密碼許可權。

> [!Note]  
> 下列範例只會在主要語言為英文的網域上運作，因為 "Everyone" 和 "NT 授權單位 \\ SELF" 字串會根據網域中第一個網域控制站的語言進行當地語系化。 在不呼叫 [**LookupAccountSid**](/windows/desktop/api/winbase/nf-winbase-lookupaccountsida)函式的情況下，Visual Basic 沒有辦法取得已知安全性主體的帳戶名稱。 如果使用 Visual Basic，建議您使用 winnt 提供者來修改使用者無法變更密碼許可權，如[修改使用者無法變更密碼 (WinNT 提供者) ](modifying-user-cannot-change-password-winnt-provider.md)中所示。

 


```VB
'******************************************************************************
'
'    SetUserCannotChangePassword
'
'    Sets the "User Cannot Change Password" permission using the LDAP provider
'    to the specified setting. This is accomplished by finding the existing
'    ACEs and modifying the AceType. The ACEs should always be present, but
'    it is possible that the default DACL excludes them. This function will not
'    work correctly if both ACEs are not present.
'
'    strUserDN - A string that contains the LDAP ADsPath of the user object to
'    modify.
'
'    strUsername - A string that contains the user name to use for
'    authorization. If this is an empty string, the credentials of the current
'    user are used.
'
'    strPassword - A string that contains the password to use for authorization.
'    This is ignored if strUsername is empty.
'
'    fCannotChangePassword - Contains the new setting for the privilege.
'    Contains True if the user cannot change their password or False if
'    the can change their password.
'
'******************************************************************************
Sub SetUserCannotChangePassword(strUserDN As String, strUsername As String, strPassword As String, fUserCannotChangePassword As Boolean)
    Dim oUser As IADs
    Dim oSecDesc As IADsSecurityDescriptor
    Dim oACL As IADsAccessControlList
    Dim oACE As IADsAccessControlEntry
    
    fEveryone = False
    fSelf = False
    
    If "" <> strUsername Then
        Dim dso As IADsOpenDSObject
        
        ' Bind to the group with the specified user name and password.
        Set dso = GetObject("LDAP:")
        Set oUser = dso.OpenDSObject(strUserDN, strUsername, strPassword, 1)
    Else
        ' Bind to the group with the current credentials.
        Set oUser = GetObject(strUserDN)
    End If
    
    Set oSecDesc = oUser.Get("ntSecurityDescriptor")
    Set oACL = oSecDesc.DiscretionaryAcl
    
    ' Modify the existing entries.
    For Each oACE In oACL
        If UCase(oACE.ObjectType) = UCase(CHANGE_PASSWORD_GUID) Then
            If oACE.Trustee = "Everyone" Then
                ' Modify the ace type of the entry.
                If fUserCannotChangePassword Then
                    oACE.AceType = ADS_ACETYPE_ACCESS_DENIED_OBJECT
                Else
                    oACE.AceType = ADS_ACETYPE_ACCESS_ALLOWED_OBJECT
                End If
            End If
        
            If oACE.Trustee = "NT AUTHORITY\SELF" Then
                ' Modify the ace type of the entry.
                If fUserCannotChangePassword Then
                    oACE.AceType = ADS_ACETYPE_ACCESS_DENIED_OBJECT
                Else
                    oACE.AceType = ADS_ACETYPE_ACCESS_ALLOWED_OBJECT
                End If
            End If
        End If
    Next
    
    ' Update the ntSecurityDescriptor property.
    oUser.Put "ntSecurityDescriptor", oSecDesc
    
    ' Commit the changes to the server.
    oUser.SetInfo
End Sub
```



 

 