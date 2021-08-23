---
title: 使用 ADSI LDAP 提供者建立使用者
description: 使用「ADSI LDAP 提供者」時，您只能建立全域使用者帳戶。
ms.assetid: f99f85a8-9ced-4006-b95b-bd5671ba4c60
ms.tgt_platform: multiple
keywords:
- LDAP 提供者 ADSI、使用者物件、使用者建立
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: d32d076805b9480ed0344712f7b023efab4ef0a025f367cc9c5ebb0bb7dfc0e3
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/11/2021
ms.locfileid: "119023066"
---
# <a name="user-creation-with-the-adsi-ldap-provider"></a>使用 ADSI LDAP 提供者建立使用者

使用「ADSI LDAP 提供者」時，您只能建立全域使用者帳戶。 本機帳戶位於 SAM 資料庫中，且必須使用 WinNT 提供者建立。 如需有關使用 WinNT 提供者來建立使用者物件的詳細資訊，請參閱 [WinNT User 物件](winnt-user-object.md)。

**建立使用者物件**

1.  系結至使用者物件將位於其中的容器，並取得容器的 [**IADsContainer**](/windows/desktop/api/Iads/nn-iads-iadscontainer) 或 [**IDirectoryObject**](/windows/desktop/api/Iads/nn-iads-idirectoryobject) 介面。
2.  使用 [**IADsContainer**](/windows/desktop/api/Iads/nf-iads-iadscontainer-create) 或 [**IDirectoryObject：： CreateDSObject**](/windows/desktop/api/Iads/nf-iads-idirectoryobject-createdsobject) 方法來建立使用者物件。
3.  建立使用者物件所需的最小屬性將取決於所使用的目錄服務。 如需建立 Active Directory 使用者的詳細資訊，請參閱 [建立使用者](/windows/desktop/AD/creating-a-user)。
4.  如果使用 [**IADsContainer**](/windows/desktop/api/Iads/nn-iads-iadscontainer) 介面，則在呼叫 [**IADs. SetInfo**](/windows/desktop/api/Iads/nf-iads-iads-setinfo) 方法之前，不會實際建立新的物件。

    如果使用 [**IDirectoryObject**](/windows/desktop/api/Iads/nn-iads-idirectoryobject) 介面，則在呼叫 [**CreateDSObject**](/windows/desktop/api/Iads/nf-iads-idirectoryobject-createdsobject) 方法時，就會建立新的物件。 您必須在傳遞至 **CreateDSObject** 方法的 [**ADS \_ ATTR \_ INFO**](/windows/desktop/api/Iads/ns-iads-ads_attr_info)陣列中指定最小屬性，包括 [**objectClass**](/windows/desktop/ADSchema/a-objectclass)。

## <a name="example-1"></a>範例 1

下列程式碼範例會建立具有預設屬性的使用者帳戶。


```VB
Dim ou As IADs
Dim usr as IADsUser

On Error GoTo Cleanup

Set ou = GetObject("LDAP://OU=Finance,DC=Fabrikam,DC=COM")
Set usr = ou.Create("user", "cn=Jeff Smith")
usr.Put "samAccountName", "jeffsmith"
usr.SetInfo

Cleanup:
   If (Err.Number <> 0) Then
      MsgBox ("An error has occurred. " &  Err.Number)
   End If
   Set ou = Nothing
   Set usr = Nothing
```



## <a name="example-2"></a>範例 2

下列程式碼範例會建立具有預設屬性的使用者帳戶。 為了簡潔起見，會忽略錯誤檢查。


```C++
#include <activeds.h>

int main()
{
   HRESULT hr = CoInitialize(NULL);

   IADsContainer *pCont;
   IADsUser *pUser;

   LPWSTR adsPath = L"LDAP://serv1/CN=Users,dc=Fabrikam,dc=com";
   LPWSTR usrPass = NULL;
   LPWSTR usrName = NULL;

   // Add code to securely get the user name and password or leave
   // as NULL to use the current security context.

   hr = ADsOpenObject(adsPath, 
                      usrName,
                      usrPass,
                      ADS_SECURE_AUTHENTICATION,
                      IID_IADsContainer,
                      (void**)&pCont);

   IDispatch *pDisp;
   hr = pCont->Create(CComBSTR("user"), CComBSTR("cn=Jeff Smith"), &pDisp);
   pCont->Release();

   hr = pDisp->QueryInterface(IID_IADsUser,(void**)&pUser);
   pDisp->Release();

   VARIANT var;
   VariantInit(&var);
   V_BSTR(&var) = L"jeffsmith";
   V_VT(&var)=VT_BSTR;
   hr = pUser->Put(CComBSTR("samAccountName"), var);

   hr = pUser->SetInfo();

   VariantClear(&var);
   pUser->Release();

   CoUninitialize();

   return 0;
}
```



 

 