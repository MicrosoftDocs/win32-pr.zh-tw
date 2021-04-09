---
title: 使用 GetObject 和 ADsGetObject 的系結
description: GetObject 和 ADsGetObject 函式是用來系結至目錄服務物件，而不進行驗證。
ms.assetid: 15d8116a-8ec1-48b5-bf62-411fdff7c8b8
ms.tgt_platform: multiple
keywords:
- ADSI ADSI、using、與 GetObject 和 ADsGetObject 的系結
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 5f61d5aba2c2c49e97ddcfc0f727d0cd4c17a164
ms.sourcegitcommit: b0ebdefc3dcd5c04bede94091833aa1015a2f95c
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/21/2020
ms.locfileid: "103933600"
---
# <a name="binding-with-getobject-and-adsgetobject"></a><span data-ttu-id="c78a6-104">使用 GetObject 和 ADsGetObject 的系結</span><span class="sxs-lookup"><span data-stu-id="c78a6-104">Binding With GetObject and ADsGetObject</span></span>

<span data-ttu-id="c78a6-105">**GetObject** 和 [**ADsGetObject**](/windows/desktop/api/Adshlp/nf-adshlp-adsgetobject)函式是用來系結至目錄服務物件，而不進行驗證。</span><span class="sxs-lookup"><span data-stu-id="c78a6-105">The **GetObject** and [**ADsGetObject**](/windows/desktop/api/Adshlp/nf-adshlp-adsgetobject) functions are used to bind to directory service objects with no authentication.</span></span> <span data-ttu-id="c78a6-106">存取目錄服務資料時，不需要應用程式提供認證。</span><span class="sxs-lookup"><span data-stu-id="c78a6-106">The application is not required to provide credentials when accessing directory service data.</span></span> <span data-ttu-id="c78a6-107">ADSI 使用呼叫執行緒的安全性內容。</span><span class="sxs-lookup"><span data-stu-id="c78a6-107">ADSI uses the security context of the calling thread.</span></span> <span data-ttu-id="c78a6-108">但是，如果安全驗證失敗，ADSI 會嘗試以 null 使用者名稱和 null 密碼來執行簡單的系結。</span><span class="sxs-lookup"><span data-stu-id="c78a6-108">However, if secure authentication fails, ADSI attempts to perform a simple bind with a null user name and null password.</span></span> <span data-ttu-id="c78a6-109">如果簡單系結成功，則系結的使用者內容為 Guest。</span><span class="sxs-lookup"><span data-stu-id="c78a6-109">If the simple bind succeeds, the user context for the binding is Guest.</span></span> <span data-ttu-id="c78a6-110">簡單的系結會使用純文字驗證。</span><span class="sxs-lookup"><span data-stu-id="c78a6-110">A simple bind uses plaintext authentication.</span></span> <span data-ttu-id="c78a6-111">因為不會透過網路傳輸任何使用者名稱或密碼，所以這不是安全性問題。</span><span class="sxs-lookup"><span data-stu-id="c78a6-111">Because no user name or password is transmitted over the network, this is not a security issue.</span></span>

<span data-ttu-id="c78a6-112">**GetObject** 函式是用來系結至支援自動化之語言（例如 Visual Basic）的目錄服務物件。</span><span class="sxs-lookup"><span data-stu-id="c78a6-112">The **GetObject** function is used to bind to directory service objects in languages that support automation, such as Visual Basic.</span></span> <span data-ttu-id="c78a6-113">**GetObject** 函數需要一個標記字串。</span><span class="sxs-lookup"><span data-stu-id="c78a6-113">The **GetObject** function requires a moniker string.</span></span> <span data-ttu-id="c78a6-114">在 ADSI 中，系結字串是標記字串。</span><span class="sxs-lookup"><span data-stu-id="c78a6-114">In ADSI, the binding string is the moniker string.</span></span>

<span data-ttu-id="c78a6-115">在不直接支援自動化的語言中（例如 C 或 c + +），ADSI 會提供 [**ADsGetObject**](/windows/desktop/api/Adshlp/nf-adshlp-adsgetobject) 函數來系結至目錄服務物件。</span><span class="sxs-lookup"><span data-stu-id="c78a6-115">In languages that do not directly support automation, such as C or C++, ADSI provides the [**ADsGetObject**](/windows/desktop/api/Adshlp/nf-adshlp-adsgetobject) function to bind to directory service objects.</span></span> <span data-ttu-id="c78a6-116">或者， [**MkParseDisplayName**](/windows/win32/api/objbase/nf-objbase-mkparsedisplayname) 和 [**MkParseDisplayNameEx**](/previous-versions/windows/internet-explorer/ie-developer/platform-apis/ms775113(v=vs.85)) 函數可以用來達到與 **GetObject** 相同的結果。</span><span class="sxs-lookup"><span data-stu-id="c78a6-116">Alternatively, the [**MkParseDisplayName**](/windows/win32/api/objbase/nf-objbase-mkparsedisplayname) and [**MkParseDisplayNameEx**](/previous-versions/windows/internet-explorer/ie-developer/platform-apis/ms775113(v=vs.85)) functions can be used to achieve the same result as **GetObject**.</span></span>

<span data-ttu-id="c78a6-117">針對在 LocalSystem 帳戶下執行的服務， **GetObject** 和 [**ADsGetObject**](/windows/desktop/api/Adshlp/nf-adshlp-adsgetobject) 所使用的安全性內容取決於服務執行所在的電腦。</span><span class="sxs-lookup"><span data-stu-id="c78a6-117">For a service running under the LocalSystem account, the security context used by **GetObject** and [**ADsGetObject**](/windows/desktop/api/Adshlp/nf-adshlp-adsgetobject) depends on the computer on which the service is running.</span></span> <span data-ttu-id="c78a6-118">如果服務是在網域控制站上以 LocalSystem 身分執行，則服務具有 Active Directory 的完整系統層級存取權。</span><span class="sxs-lookup"><span data-stu-id="c78a6-118">If the service is running as LocalSystem on a domain controller, the service has full system-level access to Active Directory.</span></span> <span data-ttu-id="c78a6-119">如果服務不是在 DC 上執行，服務就會針對執行該服務之電腦的電腦帳戶授與存取權和許可權;這比系統層級的存取強大。</span><span class="sxs-lookup"><span data-stu-id="c78a6-119">If the service is not running on a DC, the service has the access rights and privileges granted to the computer account for the computer on which the service is running; this is significantly less powerful than system-level access.</span></span>

## <a name="examples"></a><span data-ttu-id="c78a6-120">範例</span><span class="sxs-lookup"><span data-stu-id="c78a6-120">Examples</span></span>

<span data-ttu-id="c78a6-121">下列 Visual Basic 程式碼範例顯示如何使用 **GetObject** 函數系結至物件。</span><span class="sxs-lookup"><span data-stu-id="c78a6-121">The following Visual Basic code example shows how to use the **GetObject** function to bind to an object.</span></span>


```VB
Dim myUser as IADs
Set myUser = GetObject("LDAP://CN=jeffsmith,DC=fabrikam,DC=com")
```



<span data-ttu-id="c78a6-122">下列 c + + 程式碼範例示範如何使用 [**ADsGetObject**](/windows/desktop/api/Adshlp/nf-adshlp-adsgetobject) 函數系結至物件。</span><span class="sxs-lookup"><span data-stu-id="c78a6-122">The following C++ code example shows how to use the [**ADsGetObject**](/windows/desktop/api/Adshlp/nf-adshlp-adsgetobject) function to bind to an object.</span></span>


```C++
IADs *pObject;
HRESULT hr;

// Initialize COM.
CoInitialize(NULL);

hr = ADsGetObject(L"LDAP://CN=jeffsmith,DC=fabrikam,DC=com", 
        IID_IADs,
        (void**) &pObject);

if(SUCCEEDED(hr))
{
    // Use the object.

    // Release the object.
    pObject->Release()
}

// Uninitialize COM.
CoUninitialize();
```



 

 