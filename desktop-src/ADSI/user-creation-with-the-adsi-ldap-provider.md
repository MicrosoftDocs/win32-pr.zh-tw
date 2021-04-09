---
title: 使用 ADSI LDAP 提供者建立使用者
description: 使用「ADSI LDAP 提供者」時，您只能建立全域使用者帳戶。
ms.assetid: f99f85a8-9ced-4006-b95b-bd5671ba4c60
ms.tgt_platform: multiple
keywords:
- LDAP 提供者 ADSI、使用者物件、使用者建立
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 843bb5bc9d0696c3af7c5f06ce8c76123ae93c3a
ms.sourcegitcommit: 6515eef99ca0d1bbe3e27d4575e9986f5255f277
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 03/10/2021
ms.locfileid: "104035320"
---
# <a name="user-creation-with-the-adsi-ldap-provider"></a><span data-ttu-id="9a179-104">使用 ADSI LDAP 提供者建立使用者</span><span class="sxs-lookup"><span data-stu-id="9a179-104">User Creation with the ADSI LDAP Provider</span></span>

<span data-ttu-id="9a179-105">使用「ADSI LDAP 提供者」時，您只能建立全域使用者帳戶。</span><span class="sxs-lookup"><span data-stu-id="9a179-105">With the ADSI LDAP provider, you can only create a global user account.</span></span> <span data-ttu-id="9a179-106">本機帳戶位於 SAM 資料庫中，且必須使用 WinNT 提供者建立。</span><span class="sxs-lookup"><span data-stu-id="9a179-106">Local accounts reside in the SAM database and must be created using the WinNT provider.</span></span> <span data-ttu-id="9a179-107">如需有關使用 WinNT 提供者來建立使用者物件的詳細資訊，請參閱 [WinNT User 物件](winnt-user-object.md)。</span><span class="sxs-lookup"><span data-stu-id="9a179-107">For more information about creating a user object with the WinNT provider, see [WinNT User Object](winnt-user-object.md).</span></span>

<span data-ttu-id="9a179-108">**建立使用者物件**</span><span class="sxs-lookup"><span data-stu-id="9a179-108">**To create a user object**</span></span>

1.  <span data-ttu-id="9a179-109">系結至使用者物件將位於其中的容器，並取得容器的 [**IADsContainer**](/windows/desktop/api/Iads/nn-iads-iadscontainer) 或 [**IDirectoryObject**](/windows/desktop/api/Iads/nn-iads-idirectoryobject) 介面。</span><span class="sxs-lookup"><span data-stu-id="9a179-109">Bind to the container where the user object will reside and obtain either the [**IADsContainer**](/windows/desktop/api/Iads/nn-iads-iadscontainer) or [**IDirectoryObject**](/windows/desktop/api/Iads/nn-iads-idirectoryobject) interface for the container.</span></span>
2.  <span data-ttu-id="9a179-110">使用 [**IADsContainer**](/windows/desktop/api/Iads/nf-iads-iadscontainer-create) 或 [**IDirectoryObject：： CreateDSObject**](/windows/desktop/api/Iads/nf-iads-idirectoryobject-createdsobject) 方法來建立使用者物件。</span><span class="sxs-lookup"><span data-stu-id="9a179-110">Use the [**IADsContainer.Create**](/windows/desktop/api/Iads/nf-iads-iadscontainer-create) or [**IDirectoryObject::CreateDSObject**](/windows/desktop/api/Iads/nf-iads-idirectoryobject-createdsobject) method to create the user object.</span></span>
3.  <span data-ttu-id="9a179-111">建立使用者物件所需的最小屬性將取決於所使用的目錄服務。</span><span class="sxs-lookup"><span data-stu-id="9a179-111">The minimum attributes required to create a user object will depend on the directory service used.</span></span> <span data-ttu-id="9a179-112">如需建立 Active Directory 使用者的詳細資訊，請參閱 [建立使用者](/windows/desktop/AD/creating-a-user)。</span><span class="sxs-lookup"><span data-stu-id="9a179-112">For more information about creating an Active Directory user, see [Creating a User](/windows/desktop/AD/creating-a-user).</span></span>
4.  <span data-ttu-id="9a179-113">如果使用 [**IADsContainer**](/windows/desktop/api/Iads/nn-iads-iadscontainer) 介面，則在呼叫 [**IADs. SetInfo**](/windows/desktop/api/Iads/nf-iads-iads-setinfo) 方法之前，不會實際建立新的物件。</span><span class="sxs-lookup"><span data-stu-id="9a179-113">If the [**IADsContainer**](/windows/desktop/api/Iads/nn-iads-iadscontainer) interface is used, the new object is not actually created until the [**IADs.SetInfo**](/windows/desktop/api/Iads/nf-iads-iads-setinfo) method is called.</span></span>

    <span data-ttu-id="9a179-114">如果使用 [**IDirectoryObject**](/windows/desktop/api/Iads/nn-iads-idirectoryobject) 介面，則在呼叫 [**CreateDSObject**](/windows/desktop/api/Iads/nf-iads-idirectoryobject-createdsobject) 方法時，就會建立新的物件。</span><span class="sxs-lookup"><span data-stu-id="9a179-114">If the [**IDirectoryObject**](/windows/desktop/api/Iads/nn-iads-idirectoryobject) interface is used, the new object is created when the [**CreateDSObject**](/windows/desktop/api/Iads/nf-iads-idirectoryobject-createdsobject) method is called.</span></span> <span data-ttu-id="9a179-115">您必須在傳遞至 **CreateDSObject** 方法的 [**ADS \_ ATTR \_ INFO**](/windows/desktop/api/Iads/ns-iads-ads_attr_info)陣列中指定最小屬性，包括 [**objectClass**](/windows/desktop/ADSchema/a-objectclass)。</span><span class="sxs-lookup"><span data-stu-id="9a179-115">The minimum attributes, including the [**objectClass**](/windows/desktop/ADSchema/a-objectclass), must be specified in the [**ADS\_ATTR\_INFO**](/windows/desktop/api/Iads/ns-iads-ads_attr_info) array passed to the **CreateDSObject** method.</span></span>

## <a name="example-1"></a><span data-ttu-id="9a179-116">範例 1</span><span class="sxs-lookup"><span data-stu-id="9a179-116">Example 1</span></span>

<span data-ttu-id="9a179-117">下列程式碼範例會建立具有預設屬性的使用者帳戶。</span><span class="sxs-lookup"><span data-stu-id="9a179-117">The following code example creates a user account with the default attributes.</span></span>


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



## <a name="example-2"></a><span data-ttu-id="9a179-118">範例 2</span><span class="sxs-lookup"><span data-stu-id="9a179-118">Example 2</span></span>

<span data-ttu-id="9a179-119">下列程式碼範例會建立具有預設屬性的使用者帳戶。</span><span class="sxs-lookup"><span data-stu-id="9a179-119">The following code example creates a user account with the default attributes.</span></span> <span data-ttu-id="9a179-120">為了簡潔起見，會忽略錯誤檢查。</span><span class="sxs-lookup"><span data-stu-id="9a179-120">For brevity, error checking is omitted.</span></span>


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



 

 