---
title: 撰寫 RpcNs 服務的 Spn
description: 下列程式碼範例會針對在目錄的 RpcServices 容器中具有專案的 RPC 服務，撰寫 (Spn) 的服務主體名稱。 RPC 服務會使用 RpcNsBindingExport 函式來建立其 RpcServices 專案。
ms.assetid: 4fd585b3-3f9b-4f7f-bc1b-22879587a590
ms.tgt_platform: multiple
keywords:
- 撰寫 RpcNs 服務 AD 的 Spn
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: fb65b377b5bdd041c5a34b05262f7e62f43801c5
ms.sourcegitcommit: 803f3ccd65bdefe36bd851b9c6e7280be9489016
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/17/2020
ms.locfileid: "104462912"
---
# <a name="composing-spns-for-an-rpcns-service"></a><span data-ttu-id="31c31-105">撰寫 RpcNs 服務的 Spn</span><span class="sxs-lookup"><span data-stu-id="31c31-105">Composing SPNs for an RpcNs Service</span></span>

<span data-ttu-id="31c31-106">下列程式碼範例會針對在目錄的 RpcServices 容器中具有專案的 RPC 服務，撰寫 (Spn) 的服務主體名稱。</span><span class="sxs-lookup"><span data-stu-id="31c31-106">The following code example composes the service principal names (SPNs) for an RPC service that has an entry in the RpcServices container in the directory.</span></span> <span data-ttu-id="31c31-107">RPC 服務會使用 [**RpcNsBindingExport**](/windows/desktop/api/rpcnsi/nf-rpcnsi-rpcnsbindingexporta) 函式來建立其 RpcServices 專案。</span><span class="sxs-lookup"><span data-stu-id="31c31-107">An RPC service uses the [**RpcNsBindingExport**](/windows/desktop/api/rpcnsi/nf-rpcnsi-rpcnsbindingexporta) function to create its RpcServices entry.</span></span>

<span data-ttu-id="31c31-108">RPC 服務會使用這個程式碼範例來建立 SPN 或 Spn，以識別服務的實例。</span><span class="sxs-lookup"><span data-stu-id="31c31-108">An RPC service uses this code example to build the SPN or SPNs that identify an instance of the service.</span></span> <span data-ttu-id="31c31-109">此服務會使用此常式來執行下列工作：</span><span class="sxs-lookup"><span data-stu-id="31c31-109">The service uses this routine to perform the following tasks:</span></span>

-   <span data-ttu-id="31c31-110">在安裝或移除服務時，註冊或取消註冊目錄中的 Spn。</span><span class="sxs-lookup"><span data-stu-id="31c31-110">To register or unregister the SPNs in the directory, when the service is installed or removed.</span></span> <span data-ttu-id="31c31-111">如需詳細資訊和程式碼範例，請參閱 [註冊服務的 spn](registering-the-spns-for-a-service.md)。</span><span class="sxs-lookup"><span data-stu-id="31c31-111">For more information and a code example, see [Registering the SPNs for a Service](registering-the-spns-for-a-service.md).</span></span>
-   <span data-ttu-id="31c31-112">當服務啟動時，請向 RPC 驗證服務註冊其本身。</span><span class="sxs-lookup"><span data-stu-id="31c31-112">Register itself with the RPC authentication service when the service starts.</span></span> <span data-ttu-id="31c31-113">如需詳細資訊，請參閱 [RPC 應用程式中的相互驗證](mutual-authentication-in-rpc-applications.md)。</span><span class="sxs-lookup"><span data-stu-id="31c31-113">For more information, see [Mutual Authentication in RPC Applications](mutual-authentication-in-rpc-applications.md).</span></span>

<span data-ttu-id="31c31-114">這個程式碼範例會使用服務之 RpcServices 專案的分辨名稱來組成 SPN。</span><span class="sxs-lookup"><span data-stu-id="31c31-114">This code example uses the distinguished name of the service's RpcServices entry to compose the SPN.</span></span> <span data-ttu-id="31c31-115">呼叫此程式碼之前，請先呼叫 [**RpcNsBindingExport**](/windows/desktop/api/rpcnsi/nf-rpcnsi-rpcnsbindingexporta) 函式來建立服務的 RpcServices 專案。</span><span class="sxs-lookup"><span data-stu-id="31c31-115">Before calling this code, call the [**RpcNsBindingExport**](/windows/desktop/api/rpcnsi/nf-rpcnsi-rpcnsbindingexporta) function to create the service's RpcServices entry.</span></span>

<span data-ttu-id="31c31-116">這個程式碼範例會呼叫 [**DsGetSpn**](/windows/desktop/api/Ntdsapi/nf-ntdsapi-dsgetspna) 函數來建立 SPN。</span><span class="sxs-lookup"><span data-stu-id="31c31-116">This code example calls the [**DsGetSpn**](/windows/desktop/api/Ntdsapi/nf-ntdsapi-dsgetspna) function to build an SPN.</span></span> <span data-ttu-id="31c31-117">SPN 是由服務類別名稱和服務 RpcServices 專案的分辨名稱所組成。</span><span class="sxs-lookup"><span data-stu-id="31c31-117">The SPN is composed from service class name and the distinguished name of the service RpcServices entry.</span></span>


```C++
/**********

    SpnCompose()

    Composes a service principal name from a service name and class.

    Parameters:

    pszServiceName - Contains a null-terminated string that contains 
    the name of the service.

    pszServiceClass - Contains a null-terminated string that contains 
    the name of the service class.

    pspn - Pointer to an LPTSTR array that receives the array of 
    SPNs. This array must freed with the DsFreeSpnArray function when 
    it is no longer required.

    pulSpn - Pointer to a unsigned long that receives the number of 
    elements in the pspn array.

***********/

HRESULT SpnCompose(LPTSTR pszServiceName, 
                   LPTSTR pszServiceClass, 
                   LPTSTR **pspn, 
                   unsigned long *pulSpn) 
{
    HRESULT hr;
    CComPtr<IADs> spRoot;

    // Get the defaultNamingContext for the local domain.
    hr = ADsGetObject(L"LDAP://RootDSE",
                      IID_IADs,
                      (void**)&spRoot);
    if(FAILED(hr))
    {
        return hr;
    }

    // Get the distinguished name of the current domain.
    CComVariant svarDSRoot;
    hr = spRoot->Get(CComBSTR("defaultNamingContext"), &svarDSRoot);
     
    /*
    Compose the DN of the service's entry in the RpcServices 
    container, created by a call to RpcNsBindingExport. The entry 
    for an RPC service is in the System/RpcServices container in the 
    defaultNamingContext of the local domain.
    */
    
    CComBSTR sbstrDsEntryName = "CN=";
    sbstrDsEntryName += pszServiceName;
    sbstrDsEntryName += ",CN=RpcServices,CN=System,";
    sbstrDsEntryName += svarDSRoot.bstrVal;

    USES_CONVERSION;  // Required for the W2T() macro.
    DWORD status;

    /*
    Build the SPN for this service using the DN and the service 
    class.
    */
    status = DsGetSpn(
        DS_SPN_SERVICE, // Type of SPN to create.
        pszServiceClass, // Service class - a name in this case.
        W2T(sbstrDsEntryName), // DN of the RpcServices for 
                               // this RPC service.
        0, // Use the default instance port.
        0, // Number of additional instance names.
        NULL, // No additional instance names.
        NULL, // No additional instance ports.
        pulSpn, // Size of SPN array.
        pspn // Returned SPN(s).
        );
     
    return HRESULT_FROM_WIN32(status);
}
```



 

 