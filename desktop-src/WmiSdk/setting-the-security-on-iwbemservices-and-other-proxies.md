---
description: 在 c + + 中，您可以在透過 IWbemLocator：： ConnectServer 連接至 WMI 之前呼叫 CoInitializeSecurity，以設定整個進程的安全性。
ms.assetid: 83c04a96-3829-4c07-91a7-06e5b75b2c12
ms.tgt_platform: multiple
title: 設定 IWbemServices 和其他 proxy 的安全性
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: d593c52091182b1f0580908624e0b4068ed3f8d3
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/08/2021
ms.locfileid: "106984245"
---
# <a name="setting-the-security-on-iwbemservices-and-other-proxies"></a><span data-ttu-id="4b92e-103">設定 IWbemServices 和其他 proxy 的安全性</span><span class="sxs-lookup"><span data-stu-id="4b92e-103">Setting the Security on IWbemServices and Other Proxies</span></span>

<span data-ttu-id="4b92e-104">在 c + + 中，您可以在透過 [**IWbemLocator：： ConnectServer**](/windows/desktop/api/Wbemcli/nf-wbemcli-iwbemlocator-connectserver)連接至 WMI 之前呼叫 [**CoInitializeSecurity**](/windows/win32/api/combaseapi/nf-combaseapi-coinitializesecurity) ，以設定整個進程的安全性。</span><span class="sxs-lookup"><span data-stu-id="4b92e-104">While in C++ you can set the security on the entire process by calling [**CoInitializeSecurity**](/windows/win32/api/combaseapi/nf-combaseapi-coinitializesecurity) before connecting to WMI through [**IWbemLocator::ConnectServer**](/windows/desktop/api/Wbemcli/nf-wbemcli-iwbemlocator-connectserver).</span></span> <span data-ttu-id="4b92e-105">您也可以在取得 WMI proxy 指標的呼叫中，變更驗證等級、模擬等級或驗證服務，例如 [**IWbemServices**](/windows/desktop/api/WbemCli/nn-wbemcli-iwbemservices) 或 [**IWbemCallResult**](/windows/desktop/api/Wbemcli/nn-wbemcli-iwbemcallresult)。</span><span class="sxs-lookup"><span data-stu-id="4b92e-105">You can also change the authentication level, impersonation level, or the authentication service in a call that obtains a pointer to a WMI proxy, such as [**IWbemServices**](/windows/desktop/api/WbemCli/nn-wbemcli-iwbemservices) or [**IWbemCallResult**](/windows/desktop/api/Wbemcli/nn-wbemcli-iwbemcallresult).</span></span> <span data-ttu-id="4b92e-106">呼叫 [**CoSetProxyBlanket**](/windows/win32/api/combaseapi/nf-combaseapi-cosetproxyblanket) 也可讓您變更 (KERBEROS、NTLM 或 negotiate) 的驗證服務。</span><span class="sxs-lookup"><span data-stu-id="4b92e-106">Calling [**CoSetProxyBlanket**](/windows/win32/api/combaseapi/nf-combaseapi-cosetproxyblanket) also allows you to change the authentication service (Kerberos, NTLM, or negotiate).</span></span>

<span data-ttu-id="4b92e-107">腳本和 Visual Basic 應用程式只會透過呼叫 [**SWbemServices**](swbemservices.md) 和其他 automation 物件，間接設定 proxy 上的安全性。</span><span class="sxs-lookup"><span data-stu-id="4b92e-107">Scripts and Visual Basic applications only set security on proxies indirectly through calls to [**SWbemServices**](swbemservices.md) and other automation objects.</span></span> <span data-ttu-id="4b92e-108">如需有關在腳本中設定和變更驗證和模擬的詳細資訊，請參閱 [使用 VBScript 設定預設進程安全性等級](setting-the-default-process-security-level-using-vbscript.md)。</span><span class="sxs-lookup"><span data-stu-id="4b92e-108">For more information about setting and changing authentication and impersonation in script, see [Setting the Default Process Security Level Using VBScript](setting-the-default-process-security-level-using-vbscript.md).</span></span>

<span data-ttu-id="4b92e-109">在執行不同作業系統的遠端電腦上連線至 WMI 時，變更安全性層級或服務主要是一項考慮。</span><span class="sxs-lookup"><span data-stu-id="4b92e-109">Changing security levels or services is primarily a concern when connecting to WMI on a remote computer that is running a different operating system.</span></span> <span data-ttu-id="4b92e-110">如需詳細資訊，請參閱 [在不同的作業系統之間進行連接](/windows/desktop/WmiSdk/troubleshooting-a-remote-wmi-connection)。</span><span class="sxs-lookup"><span data-stu-id="4b92e-110">For more information, see [Connecting Between Different Operating Systems](/windows/desktop/WmiSdk/troubleshooting-a-remote-wmi-connection).</span></span>

<span data-ttu-id="4b92e-111">用戶端應用程式會使用身分識別連接到 WMI proxy。</span><span class="sxs-lookup"><span data-stu-id="4b92e-111">A client application connects to a WMI proxy using an identity.</span></span> <span data-ttu-id="4b92e-112">身分識別是包含使用者名稱、密碼和授權設定的資料物件。</span><span class="sxs-lookup"><span data-stu-id="4b92e-112">An identity is a data object that consists of a user name, password, and authority settings.</span></span> <span data-ttu-id="4b92e-113">針對 WMI 用戶端應用程式，呼叫 [**IWbemLocator：： ConnectServer**](/windows/desktop/api/Wbemcli/nf-wbemcli-iwbemlocator-connectserver) 介面會建立初始身分識別。</span><span class="sxs-lookup"><span data-stu-id="4b92e-113">For a WMI client application, the call to the [**IWbemLocator::ConnectServer**](/windows/desktop/api/Wbemcli/nf-wbemcli-iwbemlocator-connectserver) interface creates the initial identity.</span></span> <span data-ttu-id="4b92e-114">[**ConnectServer**](swbemlocator-connectserver.md)方法會採用一組三個參數中的身分識別，您可以將其設定為 **Null** 以表示目前的使用者。</span><span class="sxs-lookup"><span data-stu-id="4b92e-114">The [**ConnectServer**](swbemlocator-connectserver.md) method takes the identity in a set of three parameters, which you can set to **NULL** to indicate the current user.</span></span> <span data-ttu-id="4b92e-115">您也可以指定非 **Null** 參數，以指出特定的使用者和網域。</span><span class="sxs-lookup"><span data-stu-id="4b92e-115">You can also specify a non-**NULL** parameter to indicate a specific user and domain.</span></span> <span data-ttu-id="4b92e-116">如果呼叫成功， **ConnectServer** 會傳回可讓您存取各種遠端進程的指標，例如 WMI 服務或 Windows 作業系統。</span><span class="sxs-lookup"><span data-stu-id="4b92e-116">If the call is successful, **ConnectServer** returns a pointer through which you can access a variety of remote processes, such as a WMI service or the Windows operating system directly.</span></span>

<span data-ttu-id="4b92e-117">如同許多 COM 介面， [**ConnectServer**](swbemlocator-connectserver.md) 會傳回 proxy 的指標。</span><span class="sxs-lookup"><span data-stu-id="4b92e-117">Like many COM interfaces, [**ConnectServer**](swbemlocator-connectserver.md) returns a pointer to a proxy.</span></span> <span data-ttu-id="4b92e-118">Proxy 是代表遠端進程的資料物件，例如 WMI 或遠端提供者。</span><span class="sxs-lookup"><span data-stu-id="4b92e-118">A proxy is a data object that represents a remote process, such as WMI or a remote provider.</span></span> <span data-ttu-id="4b92e-119">COM 會使用 proxy 來允許開發人員存取遠端資料，就像是在本機資料一樣。</span><span class="sxs-lookup"><span data-stu-id="4b92e-119">COM uses a proxy to allow developers access to remote data as though the data were local.</span></span>

<span data-ttu-id="4b92e-120">下列 WMI 介面會使用 proxy：</span><span class="sxs-lookup"><span data-stu-id="4b92e-120">The following WMI interfaces use proxies:</span></span>

-   <span data-ttu-id="4b92e-121">[**IWbemServices**](/windows/desktop/api/WbemCli/nn-wbemcli-iwbemservices) ([**SWbemServices**](swbemservices.md) 腳本物件) </span><span class="sxs-lookup"><span data-stu-id="4b92e-121">[**IWbemServices**](/windows/desktop/api/WbemCli/nn-wbemcli-iwbemservices) ([**SWbemServices**](swbemservices.md) scripting object)</span></span>
-   [<span data-ttu-id="4b92e-122">**IEnumWbemClassObject**</span><span class="sxs-lookup"><span data-stu-id="4b92e-122">**IEnumWbemClassObject**</span></span>](/windows/desktop/api/Wbemcli/nn-wbemcli-ienumwbemclassobject)
-   [<span data-ttu-id="4b92e-123">**IWbemCallResult**</span><span class="sxs-lookup"><span data-stu-id="4b92e-123">**IWbemCallResult**</span></span>](/windows/desktop/api/Wbemcli/nn-wbemcli-iwbemcallresult)
-   <span data-ttu-id="4b92e-124">[**IWbemRefresher**](/windows/desktop/api/Wbemcli/nn-wbemcli-iwbemrefresher) ([**SWbemRefresher**](swbemrefresher.md) 腳本物件) </span><span class="sxs-lookup"><span data-stu-id="4b92e-124">[**IWbemRefresher**](/windows/desktop/api/Wbemcli/nn-wbemcli-iwbemrefresher) ([**SWbemRefresher**](swbemrefresher.md) scripting object)</span></span>

    <span data-ttu-id="4b92e-125">WMI 重新整理程式是特殊案例，因為它會傳遞 [**IWbemServices**](/windows/desktop/api/WbemCli/nn-wbemcli-iwbemservices) 指標，而其安全性設定必須正確設定。</span><span class="sxs-lookup"><span data-stu-id="4b92e-125">The WMI Refresher is a special case because it is passed an [**IWbemServices**](/windows/desktop/api/WbemCli/nn-wbemcli-iwbemservices) pointer, whose security settings must be properly set.</span></span> <span data-ttu-id="4b92e-126">如需使用重新整理程式物件的詳細資訊，請參閱使用 [c + + 存取效能資料](accessing-performance-data-in-c--.md)。</span><span class="sxs-lookup"><span data-stu-id="4b92e-126">For more information about using refresher objects, see [Accessing Performance Data in C++](accessing-performance-data-in-c--.md).</span></span>

<span data-ttu-id="4b92e-127">當您收到遠端進程的指標之後，您可以進行兩項作業。</span><span class="sxs-lookup"><span data-stu-id="4b92e-127">After you receive a pointer to a remote process, you can do one of two things.</span></span> <span data-ttu-id="4b92e-128">如果您知道進程的功能，您可以選擇在指標上設定安全性，並正常存取進程。</span><span class="sxs-lookup"><span data-stu-id="4b92e-128">If you know what the process does, you can choose to set the security on the pointer and access the process normally.</span></span> <span data-ttu-id="4b92e-129">大部分的 WMI 服務指標都是如此。</span><span class="sxs-lookup"><span data-stu-id="4b92e-129">This is the case with most pointers to a WMI service.</span></span> <span data-ttu-id="4b92e-130">如需詳細資訊，請參閱 [設定 WMI 連接的安全性層級](setting-the-security-levels-on-a-wmi-connection.md)。</span><span class="sxs-lookup"><span data-stu-id="4b92e-130">For more information, see [Setting the Security Levels on a WMI Connection](setting-the-security-levels-on-a-wmi-connection.md).</span></span> <span data-ttu-id="4b92e-131">或者，您必須透過呼叫 proxy 上的 [**iunknown**](/windows/win32/api/unknwn/nn-unknwn-iunknown)介面，在 proxy 上存取不同的 COM 介面，例如 [**Iunknown：： Release**](/windows/win32/api/unknwn/nf-unknwn-iunknown-release)。</span><span class="sxs-lookup"><span data-stu-id="4b92e-131">Alternately, you need to access a different COM interface on the proxy, such as [**IUnknown::Release**](/windows/win32/api/unknwn/nf-unknwn-iunknown-release), through a call to the [**IUnknown**](/windows/win32/api/unknwn/nn-unknwn-iunknown) interface on the proxy.</span></span>

## <a name="defaults-and-recommendations"></a><span data-ttu-id="4b92e-132">預設值和建議</span><span class="sxs-lookup"><span data-stu-id="4b92e-132">Defaults and Recommendations</span></span>

<span data-ttu-id="4b92e-133">元件物件模型的分散式版本 (DCOM) 將預設驗證服務 (Kerberos、NTLM 或 Negotiate) 進行協調，而您無法使用 [**CoInitializeSecurity**](/windows/win32/api/combaseapi/nf-combaseapi-coinitializesecurity)指定預設驗證服務。</span><span class="sxs-lookup"><span data-stu-id="4b92e-133">The distributed version of the Component Object Model (DCOM) negotiates the default authentication service (Kerberos, NTLM, or Negotiate), and you cannot specify the default authentication service using [**CoInitializeSecurity**](/windows/win32/api/combaseapi/nf-combaseapi-coinitializesecurity).</span></span> <span data-ttu-id="4b92e-134">在 [**CoSetProxyBlanket**](/windows/win32/api/combaseapi/nf-combaseapi-cosetproxyblanket)的驗證服務參數中指定 **RPC \_ C \_ 驗證 \_ 預設值**，可讓 DCOM 選取適當的服務。</span><span class="sxs-lookup"><span data-stu-id="4b92e-134">Specifying **RPC\_C\_AUTHN\_DEFAULT** in the authentication service parameter of [**CoSetProxyBlanket**](/windows/win32/api/combaseapi/nf-combaseapi-cosetproxyblanket) allows DCOM to select the appropriate service.</span></span> <span data-ttu-id="4b92e-135">針對遠端連線，預設服務是 Negotiate，這是在 Kerberos 和非 Kerberos 網域中運作的應用程式所建議的服務。</span><span class="sxs-lookup"><span data-stu-id="4b92e-135">For remote connections the default service is Negotiate, which is the recommended service for applications functioning in both Kerberos and non-Kerberos domains.</span></span> <span data-ttu-id="4b92e-136">針對本機連接，預設驗證服務為 NT LAN Manager (NTLM) 。</span><span class="sxs-lookup"><span data-stu-id="4b92e-136">For local connections, the default authentication service is NT LAN Manager (NTLM).</span></span>

<span data-ttu-id="4b92e-137">下列程式碼範例顯示所使用的預設驗證服務。</span><span class="sxs-lookup"><span data-stu-id="4b92e-137">The following code example shows the default authentication service being used.</span></span>


```C++
// The pWbemServices variable is of type IWbemServices*

HRESULT hr = CoSetProxyBlanket(
     pWbemServices,                //Proxy
     RPC_C_AUTHN_DEFAULT,          //Authentication service 
     RPC_C_AUTHZ_DEFAULT,          //Authorization service 
     COLE_DEFAULT_PRINCIPAL,       //Server principal name used 
                                       // by authentication service
     RPC_C_AUTHN_LEVEL_DEFAULT,    //Authentication level
     RPC_C_IMP_LEVEL_IMPERSONATE,  //Impersonation level
     COLE_DEFAULT_AUTHINFO,       //Client identity
     EOAC_DEFAULT                  //Capability flags
     );
```



<span data-ttu-id="4b92e-138">本主題中的程式碼範例需要下列參考和 \# include 語句。</span><span class="sxs-lookup"><span data-stu-id="4b92e-138">The code example in this topic requires the following reference and \#include statements.</span></span>


```C++
#define _WIN32_DCOM
#include <wbemidl.h>
#include <comdef.h>

#pragma comment(lib, "wbemuuid.lib")
```



<span data-ttu-id="4b92e-139">針對腳本，建議您使用 DCOM 針對遠端呼叫所選取的預設值。</span><span class="sxs-lookup"><span data-stu-id="4b92e-139">For scripting, it is recommended that you use the defaults that DCOM selects for remote calls.</span></span> <span data-ttu-id="4b92e-140">在本機電腦上，您不能指定驗證服務來呼叫 WMI。</span><span class="sxs-lookup"><span data-stu-id="4b92e-140">On the local machine you cannot specify an authentication service for calls to WMI.</span></span> <span data-ttu-id="4b92e-141">如需詳細資訊，請參閱 [使用 VBScript 設定驗證服務](setting-the-authentication-service-using-vbscript.md) 和 [建立標記字串](constructing-a-moniker-string.md)。</span><span class="sxs-lookup"><span data-stu-id="4b92e-141">For more information, see [Setting the Authentication Service Using VBScript](setting-the-authentication-service-using-vbscript.md) and [Constructing a Moniker String](constructing-a-moniker-string.md).</span></span>

 

 
