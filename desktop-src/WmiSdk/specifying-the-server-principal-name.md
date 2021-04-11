---
description: Kerberos 驗證服務會指定伺服器主體名稱，以確保它所連接之電腦的身分識別。
ms.assetid: 3d58db28-2e69-4e27-9f27-61529abbf750
ms.tgt_platform: multiple
title: 指定伺服器主體名稱
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 4a2f5aa4053b5ae7452e5f5e9c0ddcac15630ae5
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/07/2021
ms.locfileid: "104114888"
---
# <a name="specifying-the-server-principal-name"></a><span data-ttu-id="457be-103">指定伺服器主體名稱</span><span class="sxs-lookup"><span data-stu-id="457be-103">Specifying the Server Principal Name</span></span>

<span data-ttu-id="457be-104">Kerberos 驗證服務會指定伺服器主體名稱，以確保它所連接之電腦的身分識別。</span><span class="sxs-lookup"><span data-stu-id="457be-104">The Kerberos authentication service specifies the server principal name to ensure the identity of the computer to which it is connecting.</span></span> <span data-ttu-id="457be-105">藉由提供遠端電腦的名稱，在對腳本方法 [**wbemscripting.swbemlocator**](swbemlocator-connectserver.md) 的呼叫中指定伺服器主體名稱。</span><span class="sxs-lookup"><span data-stu-id="457be-105">Specify the server principal name in the call to the scripting method [**SWbemLocator.ConnectServer**](swbemlocator-connectserver.md) by giving the name of the remote computer.</span></span> <span data-ttu-id="457be-106">在 c + + 中，為 proxy 呼叫 [**CoSetProxyBlanket**](/windows/win32/api/combaseapi/nf-combaseapi-cosetproxyblanket)時，于 *pServerPrincName* 參數中指定伺服器主體名稱。</span><span class="sxs-lookup"><span data-stu-id="457be-106">In C++, specify the server principal name in the *pServerPrincName* parameter when calling [**CoSetProxyBlanket**](/windows/win32/api/combaseapi/nf-combaseapi-cosetproxyblanket) for the proxy.</span></span> <span data-ttu-id="457be-107">如需詳細資訊，請參閱 [連接到遠端電腦上的 WMI](connecting-to-wmi-on-a-remote-computer.md)。</span><span class="sxs-lookup"><span data-stu-id="457be-107">For more information, see [Connecting to WMI on a Remote Computer](connecting-to-wmi-on-a-remote-computer.md).</span></span>

<span data-ttu-id="457be-108">Kerberos 需要此參數才能支援相互驗證。</span><span class="sxs-lookup"><span data-stu-id="457be-108">This parameter is required for Kerberos to support mutual authentication.</span></span> <span data-ttu-id="457be-109">不過，使用預設的伺服器主體名稱不允許相互驗證。</span><span class="sxs-lookup"><span data-stu-id="457be-109">However, using the default server principal name does not allow mutual authentication.</span></span> <span data-ttu-id="457be-110">相互驗證很重要的用戶端，必須指定符合 WMI 服務所使用之伺服器身分識別的伺服器主體名稱。</span><span class="sxs-lookup"><span data-stu-id="457be-110">Clients for which mutual authentication is critical, must specify a server principal name that matches the server identity that the WMI service is using.</span></span> <span data-ttu-id="457be-111">如需設定 proxy 安全性的詳細資訊，以及顯示如何設定伺服器主體名稱的 c + + 範例，請參閱 [設定 IWbemServices 和其他 proxy 的安全性](setting-the-security-on-iwbemservices-and-other-proxies.md)。</span><span class="sxs-lookup"><span data-stu-id="457be-111">For more information about setting proxy security and a C++ example showing how to set the server principal name, see [Setting the Security on IWbemServices and Other Proxies](setting-the-security-on-iwbemservices-and-other-proxies.md).</span></span>

<span data-ttu-id="457be-112">如需有關在腳本和 Visual Basic 中設定伺服器主體名稱的詳細資訊，請參閱 [**wbemscripting.swbemlocator. ConnectServer**](swbemlocator-connectserver.md) 及 [連接到遠端電腦上的 WMI](connecting-to-wmi-on-a-remote-computer.md)。</span><span class="sxs-lookup"><span data-stu-id="457be-112">For more information about setting the server principal name in script and Visual Basic, see [**SWbemLocator.ConnectServer**](swbemlocator-connectserver.md) and [Connecting to WMI on a Remote Computer](connecting-to-wmi-on-a-remote-computer.md).</span></span>

<span data-ttu-id="457be-113">不同于 Windows Management Instrumentation (WMI) 的大部分安全性通訊協定，以及 (COM) 的元件物件模型，您無法在 [**CoInitializeSecurity**](/windows/win32/api/combaseapi/nf-combaseapi-coinitializesecurity)的呼叫中設定伺服器主體。</span><span class="sxs-lookup"><span data-stu-id="457be-113">Unlike most security protocols for Windows Management Instrumentation (WMI) and Component Object Model (COM), you cannot set the server principal in a call to [**CoInitializeSecurity**](/windows/win32/api/combaseapi/nf-combaseapi-coinitializesecurity).</span></span> <span data-ttu-id="457be-114">不過，您可以使用 [**IWbemLocator：： ConnectServer**](/windows/desktop/api/Wbemcli/nf-wbemcli-iwbemlocator-connectserver)的 *BstrAuthority* 參數或 [**CoSetProxyBlanket**](/windows/win32/api/combaseapi/nf-combaseapi-cosetproxyblanket)的 *pServerPrincName* 參數來設定伺服器主體。</span><span class="sxs-lookup"><span data-stu-id="457be-114">However, you can set the server principal with the *bstrAuthority* parameter for [**IWbemLocator::ConnectServer**](/windows/desktop/api/Wbemcli/nf-wbemcli-iwbemlocator-connectserver), or the *pServerPrincName* parameter for [**CoSetProxyBlanket**](/windows/win32/api/combaseapi/nf-combaseapi-cosetproxyblanket).</span></span>

<span data-ttu-id="457be-115">本主題中的程式碼範例需要下列 \# include 語句才能正確編譯。</span><span class="sxs-lookup"><span data-stu-id="457be-115">The code example in this topic requires the following \#include statement to correctly compile.</span></span>


```C++
#include <wbemidl.h>
```



<span data-ttu-id="457be-116">下列程式碼範例示範如何使用 [**ConnectServer**](/windows/desktop/api/Wbemcli/nf-wbemcli-iwbemlocator-connectserver)設定伺服器主體名稱。</span><span class="sxs-lookup"><span data-stu-id="457be-116">The following code example shows how to set the server principal name with [**ConnectServer**](/windows/desktop/api/Wbemcli/nf-wbemcli-iwbemlocator-connectserver).</span></span>


```C++
IWbemServices* g_pNameSpace = NULL;

// Namespace to which to connect
BSTR  bstrNameSpace = 
SysAllocString( L"\\\\MyMachine\\root\default" );

// The bstrAuthority string contains the server
// principal name MyDomain\\MyMachine
// and the authentication service, which is Kerberos.
BSTR  bstrAuthority = 
SysAllocString( L"kerberos:MyDomain\\MyMachine"  );

HRESULT hr = NULL;
IWbemLocator* pWbemLocator = 0;

  hr = pWbemLocator->ConnectServer(
          bstrNameSpace,  // NameSpace name
          NULL,           // User name
          NULL,           // Password
          NULL,           // Locale
          0L,             // Security flags
          bstrAuthority,  // Authority, server principal name
          NULL,           // WBEM context
          &g_pNameSpace   // Namespace
          );

  // Free memory resources.
  g_pNameSpace->Release();
  SysFreeString(bstrNameSpace);
  SysFreeString(bstrAuthority);
```



## <a name="related-topics"></a><span data-ttu-id="457be-117">相關主題</span><span class="sxs-lookup"><span data-stu-id="457be-117">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="457be-118">使用 VBScript 設定驗證服務</span><span class="sxs-lookup"><span data-stu-id="457be-118">Setting the Authentication Service Using VBScript</span></span>](setting-the-authentication-service-using-vbscript.md)
</dt> <dt>

[<span data-ttu-id="457be-119">使用 c + + 設定驗證</span><span class="sxs-lookup"><span data-stu-id="457be-119">Setting Authentication Using C++</span></span>](setting-authentication-using-c-.md)
</dt> <dt>

[<span data-ttu-id="457be-120">設定 IWbemServices 和其他 proxy 的安全性</span><span class="sxs-lookup"><span data-stu-id="457be-120">Setting the Security on IWbemServices and Other Proxies</span></span>](setting-the-security-on-iwbemservices-and-other-proxies.md)
</dt> </dl>

 

 
