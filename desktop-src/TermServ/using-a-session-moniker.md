---
title: 使用會話的標記
description: 會話對會話啟用可讓用戶端進程在指定的會話上啟用本機伺服器處理常式。
ms.assetid: de4967b6-6a53-4888-84f9-3fa29cbebe34
ms.tgt_platform: multiple
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 700d251aa1136747529b66b975d4cbedf9b14dcf
ms.sourcegitcommit: 592c9bbd22ba69802dc353bcb5eb30699f9e9403
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/20/2020
ms.locfileid: "104316183"
---
# <a name="using-a-session-moniker"></a><span data-ttu-id="07226-103">使用會話的標記</span><span class="sxs-lookup"><span data-stu-id="07226-103">Using a Session Moniker</span></span>

<span data-ttu-id="07226-104">會話對會話啟用可讓用戶端進程在指定的會話上啟用本機伺服器處理常式。</span><span class="sxs-lookup"><span data-stu-id="07226-104">Session-to-session activation allows a client process to activate a local server process on a specified session.</span></span> <span data-ttu-id="07226-105">您可以使用系統提供的會話標記，以每個會話為基礎來執行此動作。</span><span class="sxs-lookup"><span data-stu-id="07226-105">You can do this on a per-session basis by using a system-supplied session moniker.</span></span> <span data-ttu-id="07226-106">如需建立會話的標記的詳細資訊，請參閱會話 [對會話啟用與會話的標記](session-to-session-activation-with-a-session-moniker.md)。</span><span class="sxs-lookup"><span data-stu-id="07226-106">For more information about creating a session moniker, see [Session-to-Session Activation with a Session Moniker](session-to-session-activation-with-a-session-moniker.md).</span></span>

<span data-ttu-id="07226-107">下列範例示範如何在會話識別碼為3的會話上啟用類別識別碼為 "10000013-0000-0000-0000-000000000001" 的本機伺服器處理常式。</span><span class="sxs-lookup"><span data-stu-id="07226-107">The following example shows how to activate a local server process with the class ID "10000013-0000-0000-0000-000000000001" on the session with the session ID 3.</span></span>

<span data-ttu-id="07226-108">首先，此範例會呼叫 [**CoInitialize**](/windows/win32/api/objbase/nf-objbase-coinitialize) 函式來初始化 COM 程式庫。</span><span class="sxs-lookup"><span data-stu-id="07226-108">First, the sample calls the [**CoInitialize**](/windows/win32/api/objbase/nf-objbase-coinitialize) function to initialize the COM library.</span></span> <span data-ttu-id="07226-109">然後，此範例會呼叫 [**CreateBindCtx**](/windows/win32/api/objbase/nf-objbase-createbindctx) ，以取得 [**IBindCtx**](/windows/win32/api/objidl/nn-objidl-ibindctx) 介面之執行的指標。</span><span class="sxs-lookup"><span data-stu-id="07226-109">Then the sample calls [**CreateBindCtx**](/windows/win32/api/objbase/nf-objbase-createbindctx) to retrieve a pointer to an implementation of the [**IBindCtx**](/windows/win32/api/objidl/nn-objidl-ibindctx) interface.</span></span> <span data-ttu-id="07226-110">這個物件會儲存有關「標記系結」作業的資訊;需要指標才能呼叫 [**IMoniker**](/windows/win32/api/objidl/nn-objidl-imoniker) 介面的方法。</span><span class="sxs-lookup"><span data-stu-id="07226-110">This object stores information about moniker-binding operations; the pointer is required to call methods of the [**IMoniker**](/windows/win32/api/objidl/nn-objidl-imoniker) interface.</span></span> <span data-ttu-id="07226-111">接下來，此範例會呼叫 [MkParseDisplayNameEx](/previous-versions/windows/internet-explorer/ie-developer/platform-apis/ms775113(v=vs.85)) 函式來建立複合會話標記，然後呼叫 [**IMoniker：： BindToObject**](/windows/win32/api/objidl/nf-objidl-imoniker-bindtoobject) 方法，以使用新建立的會話名字標記來啟動用戶端與伺服器進程之間的連接。</span><span class="sxs-lookup"><span data-stu-id="07226-111">Next the sample calls the [MkParseDisplayNameEx](/previous-versions/windows/internet-explorer/ie-developer/platform-apis/ms775113(v=vs.85)) function to create the composite session moniker and then the [**IMoniker::BindToObject**](/windows/win32/api/objidl/nf-objidl-imoniker-bindtoobject) method to activate the connection between the client and the server process, using the newly created session moniker.</span></span> <span data-ttu-id="07226-112">至此，您可以使用介面指標，在物件上執行所需的作業。</span><span class="sxs-lookup"><span data-stu-id="07226-112">At this point you can use the interface pointer to perform the desired operations on the object.</span></span> <span data-ttu-id="07226-113">最後，此範例會釋放系結內容，並呼叫 [**CoUninitialize**](/windows/win32/api/combaseapi/nf-combaseapi-couninitialize) 函式。</span><span class="sxs-lookup"><span data-stu-id="07226-113">Finally, the sample releases the bind context and calls the [**CoUninitialize**](/windows/win32/api/combaseapi/nf-combaseapi-couninitialize) function.</span></span>


```C++
// Initialize COM.

HRESULT hr = CoInitialize(NULL);
if (FAILED(hr)) exit(0);  // Handle errors here.

// Get interface pBindCtx.

IBindCtx* pBindCtx;
hr = CreateBindCtx(NULL, &pBindCtx);
if (FAILED(hr)) exit(0);  // Handle errors here.

// Get moniker pMoniker.

OLECHAR string[] =
    L"Session:3!clsid:10000013-0000-0000-0000-000000000001";
ULONG ulParsed;
IMoniker* pMoniker;
hr = MkParseDisplayNameEx( pBindCtx,
                           string,
                           &ulParsed,
                           &pMoniker
                          );
if (FAILED(hr)) exit(0);  // Handle errors here.

// Get object factory pSessionTestFactory.

IUnknown* pSessionTestFactory;
hr = pMoniker->BindToObject( pBindCtx,
                             NULL,
                             IID_IUnknown,
                             (void**)&pSessionTestFactory
                            );
if (FAILED(hr)) exit(0);  // Handle errors here.

//
// Make, use, and destroy object here.
//
pSessionTestFactory->Release();
pSessionTestFactory = NULL;

pMoniker->Release();  // Release moniker.

pBindCtx->Release();  // Release interface.

CoUninitialize();  // Release COM.
```



<span data-ttu-id="07226-114">因為 "{類別的類別識別碼（class）標記}" 也是命名類別標記的方式，所以您可以使用下列字串，將複合的標記名稱 (為類別標記所組成的會話標記) ，而不是上述範例中顯示的方式。</span><span class="sxs-lookup"><span data-stu-id="07226-114">Because "{class id of the class moniker}" is also a way to name a class moniker, you can use the following string to name the composite moniker (the session moniker composed with the class moniker) instead of the way show in the preceding example.</span></span>

``` syntax
OLECHAR string[] = 
    L"Session:3!{0000031A-0000-0000-C000-000000000046}:
    10000013-0000-0000-0000-000000000001";
```

> [!Note]  
> <span data-ttu-id="07226-115">如果相同的使用者在跨會話啟用期間登入每個會話，您可以成功地啟用任何設定為在 RunAs 互動式使用者啟用模式中執行的伺服器進程。</span><span class="sxs-lookup"><span data-stu-id="07226-115">If the same user is logged on to each session during a cross-session activation, you can successfully activate any server process configured to run in the RunAs Interactive User activation mode.</span></span> <span data-ttu-id="07226-116">如果有不同的使用者登入每個會話，則伺服器必須呼叫 [**CoInitializeSecurity**](/windows/win32/api/combaseapi/nf-combaseapi-coinitializesecurity) 函式來設定適當的使用者權限，才能成功啟用，而且用戶端與伺服器之間可能會發生連接。</span><span class="sxs-lookup"><span data-stu-id="07226-116">If different users are logged on to each session, the server must call the [**CoInitializeSecurity**](/windows/win32/api/combaseapi/nf-combaseapi-coinitializesecurity) function to set the appropriate user rights before a successful activation and connection can occur between the client and the server.</span></span> <span data-ttu-id="07226-117">達成此目的的方法之一，是讓伺服器執行自訂 [**IAccessControl**](/windows/win32/api/iaccess/nn-iaccess-iaccesscontrol) 介面，並將實作為傳遞至 **CoInitializeSecurity**。</span><span class="sxs-lookup"><span data-stu-id="07226-117">One way to accomplish this would be for the server to implement a custom [**IAccessControl**](/windows/win32/api/iaccess/nn-iaccess-iaccesscontrol) interface and pass the implementation to **CoInitializeSecurity**.</span></span> <span data-ttu-id="07226-118">在任何情況下，用戶端使用者都必須具有在伺服器上執行之應用程式所指定的適當 [**啟動**](../com/launchpermission.md) 和 [**存取權限**](../com/accesspermission.md) 。</span><span class="sxs-lookup"><span data-stu-id="07226-118">In any case, the client user must have the appropriate [**Launch**](../com/launchpermission.md) and [**Access Permissions**](../com/accesspermission.md) that are specified by the application running on the server.</span></span> <span data-ttu-id="07226-119">如需詳細資訊，請參閱 [COM 中的安全性](../com/security-in-com.md)。</span><span class="sxs-lookup"><span data-stu-id="07226-119">For more information see [Security in COM](../com/security-in-com.md).</span></span>

 

<span data-ttu-id="07226-120">For more information about system-supplied monikers and monikers and activation modes, see [Monikers](../com/monikers.md), the [**IMoniker**](/windows/win32/api/objidl/nn-objidl-imoniker) interface, and [AppId Key](/windows/desktop/com/appid-key) in the COM documentation in the Platform Software Development Kit (SDK).</span><span class="sxs-lookup"><span data-stu-id="07226-120">For more information about system-supplied monikers and monikers and activation modes, see [Monikers](../com/monikers.md), the [**IMoniker**](/windows/win32/api/objidl/nn-objidl-imoniker) interface, and [AppId Key](/windows/desktop/com/appid-key) in the COM documentation in the Platform Software Development Kit (SDK).</span></span>

 

 