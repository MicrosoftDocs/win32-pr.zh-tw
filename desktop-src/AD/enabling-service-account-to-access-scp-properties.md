---
title: 啟用服務帳戶以存取 SCP 屬性
description: 下列程式碼範例會在服務連接點上設定一組存取控制專案 (Ace)  (SCP) 物件。
ms.assetid: 663dcf55-5f0d-49af-8b51-4c1e35b79ef1
ms.tgt_platform: multiple
keywords:
- 啟用服務帳戶以存取 SCP 屬性 AD
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: b49adcd1b4747b1c13a64a5af54c6cc6a42e6afe
ms.sourcegitcommit: 803f3ccd65bdefe36bd851b9c6e7280be9489016
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/17/2020
ms.locfileid: "103842083"
---
# <a name="enabling-service-account-to-access-scp-properties"></a><span data-ttu-id="3127d-104">啟用服務帳戶以存取 SCP 屬性</span><span class="sxs-lookup"><span data-stu-id="3127d-104">Enabling Service Account to Access SCP Properties</span></span>

<span data-ttu-id="3127d-105">下列程式碼範例會在服務連接點上設定一組存取控制專案 (Ace)  (SCP) 物件。</span><span class="sxs-lookup"><span data-stu-id="3127d-105">The following code example sets a pair of Access Control Entries (ACEs) on a service connection point (SCP) object.</span></span> <span data-ttu-id="3127d-106">Ace 會將讀取/寫入存取權授與服務實例執行所在的使用者或電腦帳戶。</span><span class="sxs-lookup"><span data-stu-id="3127d-106">The ACEs grant read/write access to the user or computer account under which the service instance will be running.</span></span> <span data-ttu-id="3127d-107">服務安裝程式會使用與下列類似的程式碼，以確保服務可以在執行時間更新其屬性。</span><span class="sxs-lookup"><span data-stu-id="3127d-107">The service installer uses code similar to the following to ensure that the service can update its properties at run time.</span></span> <span data-ttu-id="3127d-108">如果未設定類似這些 Ace 的 Ace，服務將無法存取 SCP 的屬性。</span><span class="sxs-lookup"><span data-stu-id="3127d-108">If ACEs similar to these these are not set, the service will not have access to the properties of the SCP.</span></span>

<span data-ttu-id="3127d-109">一般來說，服務安裝程式會在建立 SCP 物件之後設定這些 Ace。</span><span class="sxs-lookup"><span data-stu-id="3127d-109">Typically, a service installer will set these ACEs after creating the SCP object.</span></span> <span data-ttu-id="3127d-110">如需詳細資訊，以及建立 SCP 並呼叫此函式的程式碼範例，請參閱 [用戶端如何尋找和使用服務連接點](how-clients-find-and-use-a-service-connection-point.md)。</span><span class="sxs-lookup"><span data-stu-id="3127d-110">For more information, and a code example that creates an SCP and calls this function, see [How Clients Find and Use a Service Connection Point](how-clients-find-and-use-a-service-connection-point.md).</span></span> <span data-ttu-id="3127d-111">如果服務重新設定為以不同的帳戶執行，則必須更新 Ace。</span><span class="sxs-lookup"><span data-stu-id="3127d-111">If the service is reconfigured to run under a different account, the ACEs must be updated.</span></span> <span data-ttu-id="3127d-112">若要成功執行，必須在網域系統管理員的安全性內容中執行此程式碼範例。</span><span class="sxs-lookup"><span data-stu-id="3127d-112">To run successfully, this code example must be run in the security context of a domain administrator.</span></span>

<span data-ttu-id="3127d-113">範例函式的第一個參數會指定要授與存取權的使用者帳戶名稱。</span><span class="sxs-lookup"><span data-stu-id="3127d-113">The first parameter of the sample function specifies the name of the user account to be granted access.</span></span> <span data-ttu-id="3127d-114">函數假設名稱是網域使用者名稱 \*格式 \*\*\*\\*\*\*\* 。</span><span class="sxs-lookup"><span data-stu-id="3127d-114">The function assumes the name is in *Domain ***\\*** UserName* format.</span></span> <span data-ttu-id="3127d-115">如果未指定任何帳戶，則函式會假設服務使用 LocalSystem 帳戶。</span><span class="sxs-lookup"><span data-stu-id="3127d-115">If no account is specified, the function assumes the service uses the LocalSystem account.</span></span> <span data-ttu-id="3127d-116">這表示此函數必須將存取權授與執行服務之主機伺服器的電腦帳戶。</span><span class="sxs-lookup"><span data-stu-id="3127d-116">This means the function must grant access to the computer account of the host server on which the service is running.</span></span> <span data-ttu-id="3127d-117">若要這樣做，程式碼範例會呼叫 [**GetComputerObjectName**](/windows/desktop/api/secext/nf-secext-getcomputerobjectnamea) 函數來取得本機電腦的網域和使用者名稱。</span><span class="sxs-lookup"><span data-stu-id="3127d-117">To do this, the code example calls the [**GetComputerObjectName**](/windows/desktop/api/secext/nf-secext-getcomputerobjectnamea) function to obtain the domain and user name of the local computer.</span></span>

<span data-ttu-id="3127d-118">您可以修改下列程式碼範例，以授與服務對 SCP 物件的完整存取權，但最佳做法是只授與服務在執行時間所需的特定存取權限。</span><span class="sxs-lookup"><span data-stu-id="3127d-118">The following code example can be modified to grant the service full access to the SCP object, but the best practice is to grant only the specific access rights that the service requires at run time.</span></span> <span data-ttu-id="3127d-119">在此情況下，函數會將存取權授與兩個屬性。</span><span class="sxs-lookup"><span data-stu-id="3127d-119">In this case, the function grants access to two properties.</span></span>



| <span data-ttu-id="3127d-120">屬性</span><span class="sxs-lookup"><span data-stu-id="3127d-120">Property</span></span>                                                              | <span data-ttu-id="3127d-121">描述</span><span class="sxs-lookup"><span data-stu-id="3127d-121">Description</span></span>                                                          |
|-----------------------------------------------------------------------|----------------------------------------------------------------------|
| [<span data-ttu-id="3127d-122">**serviceDNSName**</span><span class="sxs-lookup"><span data-stu-id="3127d-122">**serviceDNSName**</span></span>](/windows/desktop/ADSchema/a-servicednsname)                       | <span data-ttu-id="3127d-123">正在執行服務的主機伺服器名稱。</span><span class="sxs-lookup"><span data-stu-id="3127d-123">The name of the host server on which the service is running.</span></span>         |
| [<span data-ttu-id="3127d-124">**serviceBindingInformation**</span><span class="sxs-lookup"><span data-stu-id="3127d-124">**serviceBindingInformation**</span></span>](/windows/desktop/ADSchema/a-servicebindinginformation) | <span data-ttu-id="3127d-125">服務啟動時所更新的私用系結資訊。</span><span class="sxs-lookup"><span data-stu-id="3127d-125">Private binding information that the service updates when it starts.</span></span> |



 

<span data-ttu-id="3127d-126">每個屬性都是由屬性的 **attributeSchema** 類別的 **schemaIDGUID** 來識別。</span><span class="sxs-lookup"><span data-stu-id="3127d-126">Each property is identified by the **schemaIDGUID** of the property's **attributeSchema** class.</span></span> <span data-ttu-id="3127d-127">架構中的每個屬性都有自己的唯一 **schemaIDGUID**。</span><span class="sxs-lookup"><span data-stu-id="3127d-127">Every property in the schema has its own unique **schemaIDGUID**.</span></span> <span data-ttu-id="3127d-128">下列程式碼範例會使用字串來指定 Guid。</span><span class="sxs-lookup"><span data-stu-id="3127d-128">The following code example uses strings to specify the GUIDs.</span></span> <span data-ttu-id="3127d-129">GUID 字串具有下列格式，其中每個 "X" 都會以十六進位數位取代： {XXXXXXXX-XXXX-XXXX-XXXX-XXXXXXXXXXXX}。</span><span class="sxs-lookup"><span data-stu-id="3127d-129">The GUID strings have the following format where each "X" is replaced by a hexadecimal digit: {XXXXXXXX-XXXX-XXXX-XXXX-XXXXXXXXXXXX}.</span></span>

<span data-ttu-id="3127d-130">針對指派給屬性以授與或拒絕存取權的 **schemaIDGUID** 值，請參閱 Active Directory 架構參考頁面。</span><span class="sxs-lookup"><span data-stu-id="3127d-130">Refer to the Active Directory Schema reference pages for the **schemaIDGUID** values assigned to the properties to grant or deny access to.</span></span>

<span data-ttu-id="3127d-131">下列程式碼範例會使用 [**IADsSecurityDescriptor**](/windows/desktop/api/iads/nn-iads-iadssecuritydescriptor)、 [**IADsAccessControlList**](/windows/desktop/api/iads/nn-iads-iadsaccesscontrollist)和 [**IADsAccessControlEntry**](/windows/desktop/api/iads/nn-iads-iadsaccesscontrolentry) 介面來執行下列作業。</span><span class="sxs-lookup"><span data-stu-id="3127d-131">The following code example uses the [**IADsSecurityDescriptor**](/windows/desktop/api/iads/nn-iads-iadssecuritydescriptor), [**IADsAccessControlList**](/windows/desktop/api/iads/nn-iads-iadsaccesscontrollist), and [**IADsAccessControlEntry**](/windows/desktop/api/iads/nn-iads-iadsaccesscontrolentry) interfaces to perform the following operations.</span></span>

1.  <span data-ttu-id="3127d-132">取得 SCP 物件的安全描述項。</span><span class="sxs-lookup"><span data-stu-id="3127d-132">Obtain the security descriptor of the SCP object.</span></span>
2.  <span data-ttu-id="3127d-133">在 (DACL) 安全描述項的任意存取控制清單中，設定適當的 Ace。</span><span class="sxs-lookup"><span data-stu-id="3127d-133">Set the appropriate ACEs in the discretionary access control list (DACL) of the security descriptor.</span></span>
3.  <span data-ttu-id="3127d-134">修改 SCP 物件的安全描述項。</span><span class="sxs-lookup"><span data-stu-id="3127d-134">Modify the security descriptor of the SCP object.</span></span>


```C++
#include <atlbase.h>

//******************************
//
//  AllowAccessToScpProperties()
//
//******************************

HRESULT AllowAccessToScpProperties(
    LPWSTR wszAccountSAM,   // Service account to allow access.
    IADs *pSCPObject)       // IADs pointer to the SCP object.
{
    HRESULT hr = E_FAIL;
    IADsAccessControlList *pACL = NULL;
    IADsSecurityDescriptor *pSD = NULL;
    IDispatch *pDisp = NULL;
    IADsAccessControlEntry *pACE1 = NULL;
    IADsAccessControlEntry *pACE2 = NULL;
    IDispatch *pDispACE = NULL;
    long lFlags = 0L;
    CComBSTR sbstrTrustee;
    CComBSTR sbstrSecurityDescriptor = L"nTSecurityDescriptor";
    VARIANT varSD;

    if(NULL == pSCPObject)
    {
        return E_INVALIDARG;
    }
    
    VariantInit(&varSD);
     
    /*
    If no service account is specified, service runs under 
    LocalSystem. Allow access to the computer account of the 
    service's host.
    */
    if (wszAccountSAM) 
    {
        sbstrTrustee = wszAccountSAM;
    }
    else
    {
        LPWSTR pwszComputerName;
        DWORD dwLen;
        
        // Get the size required for the SAM account name.
        dwLen = 0;
        GetComputerObjectNameW(NameSamCompatible, 
            NULL, &dwLen);
        
        pwszComputerName = new WCHAR[dwLen + 1];
        if(NULL == pwszComputerName)
        {
            hr = E_OUTOFMEMORY;
            goto cleanup;
        }

        /*
        Get the SAM account name of the computer object for 
        the server.
        */
        if(!GetComputerObjectNameW(NameSamCompatible,
            pwszComputerName, &dwLen))
        {
            delete pwszComputerName;
            
            hr = HRESULT_FROM_WIN32(GetLastError());
            goto cleanup;
        }

        sbstrTrustee = pwszComputerName;
        wprintf(L"GetComputerObjectName: %s\n", pwszComputerName);
        delete pwszComputerName;
    } 

    // Get the nTSecurityDescriptor.
    hr = pSCPObject->Get(sbstrSecurityDescriptor, &varSD);
    if (FAILED(hr) || (varSD.vt != VT_DISPATCH)) 
    {
        _tprintf(TEXT("Get nTSecurityDescriptor failed: 0x%x\n"), hr);
        goto cleanup;
    } 
     
    /*
    Use the V_DISPATCH macro to get the IDispatch pointer from 
    VARIANT structure and QueryInterface for an 
    IADsSecurityDescriptor pointer.
    */
    hr = V_DISPATCH( &varSD )->QueryInterface(
        IID_IADsSecurityDescriptor,
        (void**)&pSD);
    if (FAILED(hr)) 
    {
        _tprintf(
            TEXT("Cannot get IADsSecurityDescriptor: 0x%x\n"), 
            hr);
        goto cleanup;
    } 
     
    /*
    Get an IADsAccessControlList pointer to the security 
    descriptor's DACL.
    */
    hr = pSD->get_DiscretionaryAcl(&pDisp);
    if (SUCCEEDED(hr))
    {
        hr = pDisp->QueryInterface(
            IID_IADsAccessControlList,
            (void**)&pACL);
    }
    if (FAILED(hr)) 
    {
        _tprintf(TEXT("Cannot get DACL: 0x%x\n"), hr);
        goto cleanup;
    } 
     
    // Create the COM object for the first ACE.
    hr = CoCreateInstance(CLSID_AccessControlEntry,
                        NULL,
                        CLSCTX_INPROC_SERVER,
                        IID_IADsAccessControlEntry,
                        (void **)&pACE1);
     
    // Create the COM object for the second ACE.
    if (SUCCEEDED(hr))
    {
        hr = CoCreateInstance(CLSID_AccessControlEntry,
                        NULL,
                        CLSCTX_INPROC_SERVER,
                        IID_IADsAccessControlEntry,
                        (void **)&pACE2);
    }
    if (FAILED(hr)) 
    {
        _tprintf(TEXT("Cannot create ACEs: 0x%x\n"), hr);
        goto cleanup;
    } 
     
    // Set the properties of the two ACEs.
                                
    // Allow read and write access to the property.
    hr = pACE1->put_AccessMask(
        ADS_RIGHT_DS_READ_PROP | ADS_RIGHT_DS_WRITE_PROP);
    hr = pACE2->put_AccessMask( 
        ADS_RIGHT_DS_READ_PROP | ADS_RIGHT_DS_WRITE_PROP);
                                
    // Set the trustee, which is either the service account or the 
    // host computer account.
    hr = pACE1->put_Trustee( sbstrTrustee );
    hr = pACE2->put_Trustee( sbstrTrustee );
                                
    // Set the ACE type.
    hr = pACE1->put_AceType( ADS_ACETYPE_ACCESS_ALLOWED_OBJECT );
    hr = pACE2->put_AceType( ADS_ACETYPE_ACCESS_ALLOWED_OBJECT );
                                
    // Set AceFlags to zero because ACE is not inheritable.
    hr = pACE1->put_AceFlags( 0 );
    hr = pACE2->put_AceFlags( 0 );
     
    // Set Flags to indicate an ACE that protects a specified object.
    hr = pACE1->put_Flags( ADS_FLAG_OBJECT_TYPE_PRESENT );
    hr = pACE2->put_Flags( ADS_FLAG_OBJECT_TYPE_PRESENT );
     
    // Set ObjectType to the schemaIDGUID of the attribute.
    // serviceDNSName
    hr = pACE1->put_ObjectType( 
        L"{28630eb8-41d5-11d1-a9c1-0000f80367c1}"); 
    // serviceBindingInformation
    hr = pACE2->put_ObjectType( 
        L"{b7b1311c-b82e-11d0-afee-0000f80367c1}"); 
     
    /*
    Add the ACEs to the DACL. Need an IDispatch pointer for 
    each ACE to pass to the AddAce method.
    */
    hr = pACE1->QueryInterface(IID_IDispatch,(void**)&pDispACE);
    if (SUCCEEDED(hr))
    {
        hr = pACL->AddAce(pDispACE);
    }
    if (FAILED(hr)) 
    {
        _tprintf(TEXT("Cannot add first ACE: 0x%x\n"), hr);
        goto cleanup;
    }
    else 
    {
        if (pDispACE)
            pDispACE->Release();
    
        pDispACE = NULL;
    }
     
    // Repeat for the second ACE.
    hr = pACE2->QueryInterface(IID_IDispatch, (void**)&pDispACE);
    if (SUCCEEDED(hr))
    {
        hr = pACL->AddAce(pDispACE);
    }
    if (FAILED(hr)) 
    {
        _tprintf(TEXT("Cannot add second ACE: 0x%x\n"), hr);
        goto cleanup;
    }
     
    // Write the modified DACL back to the security descriptor.
    hr = pSD->put_DiscretionaryAcl(pDisp);
    if (SUCCEEDED(hr))
    {
        /*
        Write the ntSecurityDescriptor property to the 
        property cache.
        */
        hr = pSCPObject->Put(sbstrSecurityDescriptor, varSD);
        if (SUCCEEDED(hr))
        {
            // SetInfo updates the SCP object in the directory.
            hr = pSCPObject->SetInfo();
        }
    }
                                    
    cleanup:
    if (pDispACE)
        pDispACE->Release();
                        
    if (pACE1)
        pACE1->Release();
                    
    if (pACE2)
        pACE2->Release();
                    
    if (pACL)
        pACL->Release();
               
    if (pDisp)
        pDisp->Release();
            
    if (pSD)
        pSD->Release();
 
    VariantClear(&varSD);
 
    return hr;
}
```



 

 