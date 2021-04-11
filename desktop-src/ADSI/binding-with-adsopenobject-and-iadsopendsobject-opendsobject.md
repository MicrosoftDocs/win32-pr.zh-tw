---
title: 使用 ADsOpenObject 和 IADsOpenDSObject Objdso.opendsobject 系結
description: 當您必須指定替代認證以及需要資料加密時，ADsOpenObject 函式和 IADsOpenDSObject Objdso.opendsobject 方法會用來系結至目錄服務物件。
ms.assetid: 7b8ded11-e04f-40f5-a82a-5972c4df9dea
ms.tgt_platform: multiple
keywords:
- 使用 ADsOpenObject 和 IADsOpenDSObject Objdso.opendsobject ADSI
- ADSI ADSI、using、ADsOpenObject 和 IADsOpenDSObject Objdso.opendsobject 的系結
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: b5a249aa3d51520d0d345b5a098f84480e5b5016
ms.sourcegitcommit: b0ebdefc3dcd5c04bede94091833aa1015a2f95c
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/21/2020
ms.locfileid: "104024086"
---
# <a name="binding-with-adsopenobject-and-iadsopendsobjectopendsobject"></a><span data-ttu-id="b3820-105">使用 ADsOpenObject 和 IADsOpenDSObject：： Objdso.opendsobject 系結</span><span class="sxs-lookup"><span data-stu-id="b3820-105">Binding With ADsOpenObject and IADsOpenDSObject::OpenDSObject</span></span>

<span data-ttu-id="b3820-106">[**ADsOpenObject**](/windows/desktop/api/Adshlp/nf-adshlp-adsopenobject)函式和 [**IADsOpenDSObject：： objdso.opendsobject**](/windows/desktop/api/Iads/nf-iads-iadsopendsobject-opendsobject)方法是在必須指定替代認證以及需要資料加密時，用來系結至目錄服務物件。</span><span class="sxs-lookup"><span data-stu-id="b3820-106">The [**ADsOpenObject**](/windows/desktop/api/Adshlp/nf-adshlp-adsopenobject) function and the [**IADsOpenDSObject::OpenDSObject**](/windows/desktop/api/Iads/nf-iads-iadsopendsobject-opendsobject) method are used to bind to directory service objects when alternate credentials must be specified and when data encryption is required.</span></span>

<span data-ttu-id="b3820-107">可能的話，應該使用呼叫執行緒的認證。</span><span class="sxs-lookup"><span data-stu-id="b3820-107">The credentials of the calling thread should be used when possible.</span></span> <span data-ttu-id="b3820-108">但是，如果必須使用替代認證，則必須使用 [**ADsOpenObject**](/windows/desktop/api/Adshlp/nf-adshlp-adsopenobject) 函數或 [**IADsOpenDSObject：： objdso.opendsobject**](/windows/desktop/api/Iads/nf-iads-iadsopendsobject-opendsobject) 方法。</span><span class="sxs-lookup"><span data-stu-id="b3820-108">However, if alternate credentials must be used, the [**ADsOpenObject**](/windows/desktop/api/Adshlp/nf-adshlp-adsopenobject) function or the [**IADsOpenDSObject::OpenDSObject**](/windows/desktop/api/Iads/nf-iads-iadsopendsobject-opendsobject) method must be used.</span></span> <span data-ttu-id="b3820-109">如果使用替代認證，請務必不要快取密碼。</span><span class="sxs-lookup"><span data-stu-id="b3820-109">If alternate credentials are used, it is important to not cache the password.</span></span> <span data-ttu-id="b3820-110">您可以指定第一個系結作業的使用者名稱和密碼，然後只在後續的系結中指定使用者名稱，來執行多個系結作業。</span><span class="sxs-lookup"><span data-stu-id="b3820-110">Multiple bind operations can be performed by specifying the user name and password for the first bind operation and then specifying only the user name in subsequent binds.</span></span> <span data-ttu-id="b3820-111">只要符合下列條件，系統就會在第一次呼叫時設定會話，並在後續的系結呼叫上使用相同的會話：</span><span class="sxs-lookup"><span data-stu-id="b3820-111">The system sets up a session on the first call and uses the same session on subsequent bind calls as long as the following conditions are met:</span></span>

-   <span data-ttu-id="b3820-112">每個系結作業中都有相同的使用者名稱。</span><span class="sxs-lookup"><span data-stu-id="b3820-112">The same user name in each bind operation.</span></span>
-   <span data-ttu-id="b3820-113">在每個系結作業中執行無伺服器系結或系結至相同的伺服器。</span><span class="sxs-lookup"><span data-stu-id="b3820-113">Implement serverless binding or bind to the same server in each bind operation.</span></span>
-   <span data-ttu-id="b3820-114">從其中一個系結作業中保存物件參考，以維護開啟的會話。</span><span class="sxs-lookup"><span data-stu-id="b3820-114">Maintain an open session by holding on to an object reference from one of the bind operations.</span></span> <span data-ttu-id="b3820-115">釋放最後一個物件參考時，就會關閉會話。</span><span class="sxs-lookup"><span data-stu-id="b3820-115">The session is closed when the last object reference is released.</span></span>

<span data-ttu-id="b3820-116">[**ADsOpenObject**](/windows/desktop/api/Adshlp/nf-adshlp-adsopenobject) 和 [**IADsOpenDSObject：： objdso.opendsobject**](/windows/desktop/api/Iads/nf-iads-iadsopendsobject-opendsobject) 使用 Windows NT 的 [安全性支援提供者介面 (SSPI)](/windows/desktop/SecAuthN/sspi) 以允許驗證選項的彈性。</span><span class="sxs-lookup"><span data-stu-id="b3820-116">[**ADsOpenObject**](/windows/desktop/api/Adshlp/nf-adshlp-adsopenobject) and [**IADsOpenDSObject::OpenDSObject**](/windows/desktop/api/Iads/nf-iads-iadsopendsobject-opendsobject) use the Windows NT [Security Support Provider Interfaces (SSPI)](/windows/desktop/SecAuthN/sspi) to allow flexibility in authentication options.</span></span> <span data-ttu-id="b3820-117">使用這些介面的主要優點是為 Active Directory 用戶端提供不同類型的驗證，以及加密會話。</span><span class="sxs-lookup"><span data-stu-id="b3820-117">The major advantage of using these interfaces is to provide different types of authentication to Active Directory clients and to encrypt the session.</span></span> <span data-ttu-id="b3820-118">目前，ADSI 不允許傳入憑證。</span><span class="sxs-lookup"><span data-stu-id="b3820-118">Currently, ADSI does not allow certificates to be passed in.</span></span> <span data-ttu-id="b3820-119">因此，您可以使用 SSL 進行加密，然後使用 Kerberos、NTLM 或簡單驗證，視旗標在 *>dwreserved* 參數上的設定方式而定。</span><span class="sxs-lookup"><span data-stu-id="b3820-119">Therefore, you can use SSL for encryption and then Kerberos, NTLM, or simple authentication, depending on how the flags are set on the *dwReserved* parameter.</span></span>

<span data-ttu-id="b3820-120">雖然您一律會取得最高的喜好設定通訊協定，但是您無法在 ADSI 中要求特定的 SSPI 提供者。</span><span class="sxs-lookup"><span data-stu-id="b3820-120">You cannot request a specific SSPI provider in ADSI, although you always get the highest preference protocol.</span></span> <span data-ttu-id="b3820-121">在 Windows 用戶端系結至執行 Windows 的電腦時，此通訊協定為 Kerberos。</span><span class="sxs-lookup"><span data-stu-id="b3820-121">In the case of a Windows client binding to a computer running Windows, the protocol is Kerberos.</span></span> <span data-ttu-id="b3820-122">在網頁的案例中，不允許驗證憑證是可接受的，因為在執行網頁之前會先進行驗證。</span><span class="sxs-lookup"><span data-stu-id="b3820-122">Not allowing a certificate for authentication is acceptable in the case of a webpage because authentication occurs prior to running the webpage.</span></span>

<span data-ttu-id="b3820-123">雖然開啟作業可讓您指定使用者和密碼，但您不應該這麼做。</span><span class="sxs-lookup"><span data-stu-id="b3820-123">Although Open operations allow you to specify a user and password, you should not do so.</span></span> <span data-ttu-id="b3820-124">相反地，請不要指定任何認證，並隱含地使用呼叫端安全性內容的認證。</span><span class="sxs-lookup"><span data-stu-id="b3820-124">Instead, do not specify any credentials and implicitly use the credentials of the caller's security context.</span></span> <span data-ttu-id="b3820-125">若要使用呼叫端的認證搭配 [**ADsOpenObject**](/windows/desktop/api/Adshlp/nf-adshlp-adsopenobject) 或 [**IADsOpenDSObject：： objdso.opendsobject**](/windows/desktop/api/Iads/nf-iads-iadsopendsobject-opendsobject)系結至目錄物件，請指定 **Null** 做為使用者名稱和密碼。</span><span class="sxs-lookup"><span data-stu-id="b3820-125">To bind to a directory object using the caller's credentials with [**ADsOpenObject**](/windows/desktop/api/Adshlp/nf-adshlp-adsopenobject) or [**IADsOpenDSObject::OpenDSObject**](/windows/desktop/api/Iads/nf-iads-iadsopendsobject-opendsobject), specify **NULL** for both user name and password.</span></span>

<span data-ttu-id="b3820-126">最後，若要系結無驗證，請使用 **ADS \_ 無 \_ 驗證** 旗標。</span><span class="sxs-lookup"><span data-stu-id="b3820-126">Finally, to bind with no authentication, use the **ADS\_NO\_AUTHENTICATION** flag.</span></span> <span data-ttu-id="b3820-127">無驗證表示 ADSI 會嘗試系結為目標物件的匿名使用者，且不會執行任何驗證。</span><span class="sxs-lookup"><span data-stu-id="b3820-127">No authentication indicates that ADSI attempts to bind as an anonymous user to the target object and performs no authentication.</span></span> <span data-ttu-id="b3820-128">這相當於在 LDAP 中要求匿名系結，並指出所有使用者都包含在安全性內容中。</span><span class="sxs-lookup"><span data-stu-id="b3820-128">This is equivalent to requesting anonymous binding in LDAP and indicates that all users are included in the security context.</span></span>

<span data-ttu-id="b3820-129">如果驗證旗標設定為零，ADSI 會執行簡單的系結，以純文字形式傳送。</span><span class="sxs-lookup"><span data-stu-id="b3820-129">If the authentication flags are set to zero, ADSI performs a simple bind, sent as plaintext.</span></span>

> [!Caution]  
> <span data-ttu-id="b3820-130">如果指定使用者名稱和密碼但未指定驗證旗標，則會透過網路以純文字傳輸使用者名稱和密碼，這會造成安全性風險。</span><span class="sxs-lookup"><span data-stu-id="b3820-130">If a user name and password are specified without specifying authentication flags, the user name and password are transmitted over the network in plaintext, which is a security risk.</span></span> <span data-ttu-id="b3820-131">請勿指定使用者名稱和密碼，而不指定驗證旗標。</span><span class="sxs-lookup"><span data-stu-id="b3820-131">Do not specify a user name and password without specifying authentication flags.</span></span>

 

## <a name="examples"></a><span data-ttu-id="b3820-132">範例</span><span class="sxs-lookup"><span data-stu-id="b3820-132">Examples</span></span>

<span data-ttu-id="b3820-133">下列 Visual Basic 程式碼範例顯示如何使用 [**IADsOpenDSObject：： objdso.opendsobject**](/windows/desktop/api/Iads/nf-iads-iadsopendsobject-opendsobject) 方法。</span><span class="sxs-lookup"><span data-stu-id="b3820-133">The following Visual Basic code example shows how to use the [**IADsOpenDSObject::OpenDSObject**](/windows/desktop/api/Iads/nf-iads-iadsopendsobject-opendsobject) method.</span></span>


```VB
Dim openDS As IADsOpenDSObject
Dim usr As IADsUser
 
Set openDS = GetObject("LDAP:")
 
openDS.OpenDSObject("LDAP://CN=jeffsmith,DC=fabrikam,DC=com",
    NULL, 
    NULL,
    ADS_SECURE_AUTHENTICATION)
```



<span data-ttu-id="b3820-134">下列 c + + 程式碼範例示範如何使用 [**ADsOpenObject**](/windows/desktop/api/Adshlp/nf-adshlp-adsopenobject) 函數。</span><span class="sxs-lookup"><span data-stu-id="b3820-134">The following C++ code example shows how to use the [**ADsOpenObject**](/windows/desktop/api/Adshlp/nf-adshlp-adsopenobject) function.</span></span>


```C++
IADs *pObject;
HRESULT hr;

hr = ADsOpenObject(L"LDAP://CN=jeffsmith,DC=fabrikam,DC=com",
    NULL, 
    NULL,
    ADS_SECURE_AUTHENTICATION, 
    IID_IADs,
    (void**)&pObject);
if(SUCCEEDED(hr))
{
    // Use the object.

    // Release the object.
    pObject->Release()
}
```



<span data-ttu-id="b3820-135">[**IADsOpenDSObject**](/windows/desktop/api/Iads/nn-iads-iadsopendsobject)介面也可以在 c + + 中使用，但它會複製 [**ADsOpenObject**](/windows/desktop/api/Adshlp/nf-adshlp-adsopenobject)函數。</span><span class="sxs-lookup"><span data-stu-id="b3820-135">The [**IADsOpenDSObject**](/windows/desktop/api/Iads/nn-iads-iadsopendsobject) interface can also be used in C++, but it duplicates the [**ADsOpenObject**](/windows/desktop/api/Adshlp/nf-adshlp-adsopenobject) function.</span></span>

<span data-ttu-id="b3820-136">下列 c + + 程式碼範例示範如何使用 [**IADsOpenDSObject**](/windows/desktop/api/Iads/nn-iads-iadsopendsobject) 介面執行與上述程式碼範例中相同的系結作業。</span><span class="sxs-lookup"><span data-stu-id="b3820-136">The following C++ code example shows how to use the [**IADsOpenDSObject**](/windows/desktop/api/Iads/nn-iads-iadsopendsobject) interface to perform the same bind operation as in the code example above.</span></span>


```C++
IADsOpenDSObject *pDSO;
HRESULT hr;
 
hr = ADsGetObject(L"LDAP:", IID_IADsOpenDSObject, (void**)&pDSO);
if(SUCCEEDED(hr))
{
    IDispatch *pDisp;

    hr = pDSO->OpenDSObject(CComBSTR("LDAP://CN=jeffsmith,DC=fabrikam,DC=com"),
        NULL,
        NULL,
        ADS_SECURE_AUTHENTICATION, 
        &pDisp);
    if(SUCCEEDED(hr))
    {
        IADs *pObject;

        hr = pDisp->QueryInterface(IID_IADs, (void**) &pObject);
        if(SUCCEEDED(hr))
        {
            // Use the object.

            // Release the object.
            pObject->Release();
        }

        pDisp->Release();
    }
    
    pDSO->Release();
}
```



 

 