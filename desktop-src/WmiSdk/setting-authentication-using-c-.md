---
description: 適用于 WMI 的 IWbemLocator：： ConnectServer 的主要工作之一，是將指標傳回至 IWbemServices proxy。
ms.assetid: bbff43b7-79f8-4c7b-a772-d3d962cf3859
ms.tgt_platform: multiple
title: 使用 c + + 設定驗證
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 293d317ac521d36bf7ff616a0340f86c364ce885
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/08/2021
ms.locfileid: "106975778"
---
# <a name="setting-authentication-using-c"></a><span data-ttu-id="a9e0a-103">使用 c + + 設定驗證</span><span class="sxs-lookup"><span data-stu-id="a9e0a-103">Setting Authentication Using C++</span></span>

<span data-ttu-id="a9e0a-104">適用于 WMI 的 [**IWbemLocator：： ConnectServer**](/windows/desktop/api/Wbemcli/nf-wbemcli-iwbemlocator-connectserver) 的主要工作之一，是將指標傳回至 [**IWbemServices**](/windows/desktop/api/WbemCli/nn-wbemcli-iwbemservices) proxy。</span><span class="sxs-lookup"><span data-stu-id="a9e0a-104">One of the main tasks of [**IWbemLocator::ConnectServer**](/windows/desktop/api/Wbemcli/nf-wbemcli-iwbemlocator-connectserver) for WMI is returning a pointer to an [**IWbemServices**](/windows/desktop/api/WbemCli/nn-wbemcli-iwbemservices) proxy.</span></span> <span data-ttu-id="a9e0a-105">透過 **IWbemServices** proxy，您就可以存取 WMI 基礎結構的功能。</span><span class="sxs-lookup"><span data-stu-id="a9e0a-105">Through the **IWbemServices** proxy, you can access the capabilities of the WMI infrastructure.</span></span> <span data-ttu-id="a9e0a-106">不過， **iwbemservices** proxy 的指標具有用戶端應用程式進程的身分識別，而不是 **iwbemservices** 進程的身分識別。</span><span class="sxs-lookup"><span data-stu-id="a9e0a-106">However, the pointer to the **IWbemServices** proxy has the identity of the client application process and not the identity of the **IWbemServices** process.</span></span> <span data-ttu-id="a9e0a-107">因此，如果您嘗試以指標存取 **IWbemServices** ，您可以收到拒絕存取的程式碼，例如 **E \_ ACCESSDENIED**。</span><span class="sxs-lookup"><span data-stu-id="a9e0a-107">Therefore, if you attempt to access **IWbemServices** with the pointer, you can receive an access-denied code such as **E\_ACCESSDENIED**.</span></span> <span data-ttu-id="a9e0a-108">若要避免拒絕存取的錯誤，您必須使用 [**CoSetProxyBlanket**](/windows/win32/api/combaseapi/nf-combaseapi-cosetproxyblanket) 介面的呼叫來設定新指標的身分識別。</span><span class="sxs-lookup"><span data-stu-id="a9e0a-108">To avoid the access-denied error, you must set the identity of the new pointer with a call to the [**CoSetProxyBlanket**](/windows/win32/api/combaseapi/nf-combaseapi-cosetproxyblanket) interface.</span></span>

<span data-ttu-id="a9e0a-109">提供者可以設定命名空間的安全性，如此就不會傳回任何資料，除非您在與該命名空間的連接中使用封包隱私權 (**PktPrivacy**) 。</span><span class="sxs-lookup"><span data-stu-id="a9e0a-109">A provider can set the security on a namespace so that no data is returned unless you use packet privacy (**PktPrivacy**) in your connection to that namespace.</span></span> <span data-ttu-id="a9e0a-110">這可確保資料會在網路上進行加密。</span><span class="sxs-lookup"><span data-stu-id="a9e0a-110">This ensures that data is encrypted as it crosses the network.</span></span> <span data-ttu-id="a9e0a-111">如果您嘗試設定較低的驗證等級，您將會收到拒絕存取的訊息。</span><span class="sxs-lookup"><span data-stu-id="a9e0a-111">If you try to set a lower authentication level, you will get an access denied message.</span></span> <span data-ttu-id="a9e0a-112">如需詳細資訊，請參閱 [設定命名空間安全描述項](setting-namespace-security-descriptors.md)。</span><span class="sxs-lookup"><span data-stu-id="a9e0a-112">For more information, see [Setting Namepace Security Descriptors](setting-namespace-security-descriptors.md).</span></span>

<span data-ttu-id="a9e0a-113">如需有關在腳本中設定驗證的詳細資訊，請參閱 [使用 VBScript 設定預設進程安全性層級](setting-the-default-process-security-level-using-vbscript.md)。</span><span class="sxs-lookup"><span data-stu-id="a9e0a-113">For more information about setting authentication in scripting, see [Setting the Default Process Security Level Using VBScript](setting-the-default-process-security-level-using-vbscript.md).</span></span>

## <a name="setting-security-on-a-remote-iunknown-interface"></a><span data-ttu-id="a9e0a-114">在遠端 IUnknown 介面上設定安全性</span><span class="sxs-lookup"><span data-stu-id="a9e0a-114">Setting Security on a Remote IUnknown Interface</span></span>

<span data-ttu-id="a9e0a-115">在某些情況下，需要更多的伺服器存取權，而不只是 proxy 的指標。</span><span class="sxs-lookup"><span data-stu-id="a9e0a-115">In some situations, more access to a server than just a pointer to a proxy is required.</span></span> <span data-ttu-id="a9e0a-116">有時，您可能需要對 proxy 的 [**IUnknown**](/windows/win32/api/unknwn/nn-unknwn-iunknown) 介面進行安全連線。</span><span class="sxs-lookup"><span data-stu-id="a9e0a-116">At times, you may need to gain a secure connection to the [**IUnknown**](/windows/win32/api/unknwn/nn-unknwn-iunknown) interface of the proxy.</span></span> <span data-ttu-id="a9e0a-117">您可以使用 **IUnknown** 來查詢遠端系統，以取得介面和其他必要的技術。</span><span class="sxs-lookup"><span data-stu-id="a9e0a-117">Using **IUnknown**, you can query the remote system for interfaces and other necessary techniques.</span></span>

<span data-ttu-id="a9e0a-118">當 proxy 位於遠端電腦上時，伺服器會將 proxy 的 [**iunknown**](/windows/win32/api/unknwn/nn-unknwn-iunknown) 介面呼叫委派給 **iunknown** 介面。</span><span class="sxs-lookup"><span data-stu-id="a9e0a-118">When a proxy is located on a remote computer, the server delegates all calls to the [**IUnknown**](/windows/win32/api/unknwn/nn-unknwn-iunknown) interface of the proxy to the **IUnknown** interface.</span></span> <span data-ttu-id="a9e0a-119">例如，如果您在 proxy 上呼叫 [**QueryInterface**](/windows/win32/api/unknwn/nf-unknwn-iunknown-queryinterface(q)) ，而要求的介面不是 proxy 的一部分，則 proxy 會將呼叫傳送至遠端伺服器。</span><span class="sxs-lookup"><span data-stu-id="a9e0a-119">For example, if you call [**QueryInterface**](/windows/win32/api/unknwn/nf-unknwn-iunknown-queryinterface(q)) on a proxy and the requested interface was not part of the proxy, the proxy sends the call to the remote server.</span></span> <span data-ttu-id="a9e0a-120">接著，遠端伺服器會檢查是否有適當的介面支援。</span><span class="sxs-lookup"><span data-stu-id="a9e0a-120">In turn, the remote server checks for the appropriate interface support.</span></span> <span data-ttu-id="a9e0a-121">如果伺服器支援介面，COM 會將新的 proxy 封送處理回用戶端，讓應用程式能夠使用新的介面。</span><span class="sxs-lookup"><span data-stu-id="a9e0a-121">If the server does support the interface, COM marshals a new proxy back to the client so that the application can use the new interface.</span></span>

<span data-ttu-id="a9e0a-122">如果用戶端沒有遠端伺服器的存取權限，但使用的是使用者的認證，就會發生問題。</span><span class="sxs-lookup"><span data-stu-id="a9e0a-122">Problems arise if the client does not have access permissions to the remote server, yet is using the credentials of a user that does.</span></span> <span data-ttu-id="a9e0a-123">在此情況下，在遠端伺服器上存取 [**QueryInterface**](/windows/win32/api/unknwn/nf-unknwn-iunknown-queryinterface(q)) 的任何嘗試都會失敗。</span><span class="sxs-lookup"><span data-stu-id="a9e0a-123">In this situation, any attempt to access [**QueryInterface**](/windows/win32/api/unknwn/nf-unknwn-iunknown-queryinterface(q)) on the remote server fails.</span></span> <span data-ttu-id="a9e0a-124">Proxy 的最終版本也會失敗，因為目前的使用者沒有遠端伺服器的存取權。</span><span class="sxs-lookup"><span data-stu-id="a9e0a-124">The final release on the proxy fails as well, because the current user does not have access to the remote server.</span></span> <span data-ttu-id="a9e0a-125">在用戶端應用程式失敗最終的 proxy 發行之前，會有一或兩秒延遲的徵兆。</span><span class="sxs-lookup"><span data-stu-id="a9e0a-125">A symptom of this is a one or two second lag before the client application fails the final proxy release.</span></span> <span data-ttu-id="a9e0a-126">發生失敗的原因是，COM 嘗試使用目前使用者的預設安全性設定來存取遠端伺服器，而該設定未包含先允許存取伺服器的修改過的認證。</span><span class="sxs-lookup"><span data-stu-id="a9e0a-126">The failure occurs because COM attempted to access the remote server using the default security settings of the current user, which do not include the modified credentials that allowed access to the server in the first place.</span></span> <span data-ttu-id="a9e0a-127">如需詳細資訊，請參閱 [在 IWbemServices 和其他 proxy 上設定安全性](setting-the-security-on-iwbemservices-and-other-proxies.md)。</span><span class="sxs-lookup"><span data-stu-id="a9e0a-127">For more information, see [Setting the Security on IWbemServices and Other Proxies](setting-the-security-on-iwbemservices-and-other-proxies.md).</span></span>

<span data-ttu-id="a9e0a-128">若要避免連線失敗，請使用 [**CoSetProxyBlanket**](/windows/win32/api/combaseapi/nf-combaseapi-cosetproxyblanket) ，在從 [**IUnknown**](/windows/win32/api/unknwn/nn-unknwn-iunknown)傳回的指標上明確設定安全性驗證。</span><span class="sxs-lookup"><span data-stu-id="a9e0a-128">To avoid the failed connection, use [**CoSetProxyBlanket**](/windows/win32/api/combaseapi/nf-combaseapi-cosetproxyblanket) to explicitly set the security authentication on the pointer returned from [**IUnknown**](/windows/win32/api/unknwn/nn-unknwn-iunknown).</span></span> <span data-ttu-id="a9e0a-129">您可以使用 **CoSetProxyBlanket** 來確定遠端伺服器會收到正確的驗證身分識別。</span><span class="sxs-lookup"><span data-stu-id="a9e0a-129">Using **CoSetProxyBlanket**, you can ensure that the remote server receives the correct authentication identity.</span></span>

<span data-ttu-id="a9e0a-130">下列程式碼範例顯示如何使用 [**CoSetProxyBlanket**](/windows/win32/api/combaseapi/nf-combaseapi-cosetproxyblanket) 來存取遠端 [**IUnknown**](/windows/win32/api/unknwn/nn-unknwn-iunknown) 介面。</span><span class="sxs-lookup"><span data-stu-id="a9e0a-130">The following code example shows how to use [**CoSetProxyBlanket**](/windows/win32/api/combaseapi/nf-combaseapi-cosetproxyblanket) to access a remote [**IUnknown**](/windows/win32/api/unknwn/nn-unknwn-iunknown) interface.</span></span>


```C++
SEC_WINNT_AUTH_IDENTITY_W* pAuthIdentity = 
   new SEC_WINNT_AUTH_IDENTITY_W;
ZeroMemory(pAuthIdentity, sizeof(SEC_WINNT_AUTH_IDENTITY_W));

pAuthIdentity->User = new WCHAR[32];
StringCbCopyW(pAuthIdentity->User,sizeof(L"MyUser"),L"MyUser");
pAuthIdentity->UserLength = wcslen(pAuthIdentity->User);

pAuthIdentity->Domain = new WCHAR[32];
StringCbCopyW(pAuthIdentity->Domain,sizeof(L"MyDomain"),L"MyDomain");
pAuthIdentity->DomainLength = wcslen(pAuthIdentity->Domain);

pAuthIdentity->Password = new WCHAR[32];
pAuthIdentity->Password[0] = NULL;
pAuthIdentity->PasswordLength = wcslen( pAuthIdentity->Password);

pAuthIdentity->Flags = SEC_WINNT_AUTH_IDENTITY_UNICODE;

IWbemServices* pWbemServices = 0;

// Set proxy security
hr = CoSetProxyBlanket(pWbemServices, 
                       RPC_C_AUTHN_DEFAULT, 
                       RPC_C_AUTHZ_NONE, 
                       COLE_DEFAULT_PRINCIPAL, 
                       RPC_C_AUTHN_LEVEL_DEFAULT, 
                       RPC_C_IMP_LEVEL_IMPERSONATE, 
                       pAuthIdentity, 
                       EOAC_NONE 
);
if (FAILED(hr))
{
   cout << "Count not set proxy blanket. Error code = 0x"
        << hex << hr << endl;
   pWbemServices->Release();
   return 1;
}

// Set IUnknown security
IUnknown*    pUnk = NULL;
pWbemServices->QueryInterface(IID_IUnknown, (void**) &pUnk);

hr = CoSetProxyBlanket(pUnk, 
                       RPC_C_AUTHN_DEFAULT, 
                       RPC_C_AUTHZ_NONE, 
                       COLE_DEFAULT_PRINCIPAL, 
                       RPC_C_AUTHN_LEVEL_DEFAULT, 
                       RPC_C_IMP_LEVEL_IMPERSONATE, 
                       pAuthIdentity, 
                       EOAC_NONE 
);
if (FAILED(hr))
{
   cout << "Count not set proxy blanket. Error code = 0x"
        << hex << hr << endl;
   pUnk->Release();
   pWbemServices->Release();
   delete [] pAuthIdentity->User;
   delete [] pAuthIdentity->Domain;
   delete [] pAuthIdentity->Password;
   delete pAuthIdentity;   
   return 1;
}

// cleanup IUnknown
pUnk->Release();

//
// Perform a bunch of operations
//

// Cleanup
pWbemServices->Release();

delete [] pAuthIdentity->User;
delete [] pAuthIdentity->Domain;
delete [] pAuthIdentity->Password;

delete pAuthIdentity;
```



> [!Note]  
> <span data-ttu-id="a9e0a-131">當您在 proxy 的 [**IUnknown**](/windows/win32/api/unknwn/nn-unknwn-iunknown) 介面上設定安全性時，COM 會建立一份無法釋放的 proxy，直到您呼叫 [**CoUninitialize**](/windows/win32/api/combaseapi/nf-combaseapi-couninitialize)為止。</span><span class="sxs-lookup"><span data-stu-id="a9e0a-131">When you set security on the [**IUnknown**](/windows/win32/api/unknwn/nn-unknwn-iunknown) interface of a proxy, COM creates a copy of the proxy that cannot be released until you call [**CoUninitialize**](/windows/win32/api/combaseapi/nf-combaseapi-couninitialize).</span></span>

 

## <a name="related-topics"></a><span data-ttu-id="a9e0a-132">相關主題</span><span class="sxs-lookup"><span data-stu-id="a9e0a-132">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="a9e0a-133">在 WMI 中設定驗證</span><span class="sxs-lookup"><span data-stu-id="a9e0a-133">Setting Authentication in WMI</span></span>](setting-authentication-in-wmi.md)
</dt> </dl>

 

 
