---
description: 當使用者應用程式透過 WMI 提供者向系統上的物件要求資料時，模擬表示提供者會顯示代表用戶端安全性層級的認證，而不是提供者。
ms.assetid: 6d54f234-45aa-445b-ad50-7d5a9946c134
ms.tgt_platform: multiple
title: 模擬用戶端
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 162857d90c8bddb70d90eb2e10efbc08537299d9
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/08/2021
ms.locfileid: "103850772"
---
# <a name="impersonating-a-client"></a><span data-ttu-id="9c389-103">模擬用戶端</span><span class="sxs-lookup"><span data-stu-id="9c389-103">Impersonating a Client</span></span>

<span data-ttu-id="9c389-104">當使用者應用程式透過 WMI 提供者向系統上的物件要求資料時，模擬表示提供者所呈現的認證代表用戶端的安全性層級，而不是提供者的認證。</span><span class="sxs-lookup"><span data-stu-id="9c389-104">When a user application requests data from objects on the system through a WMI provider, impersonation means the provider presents credentials that represent the client's security level rather than the provider's.</span></span> <span data-ttu-id="9c389-105">模擬可防止用戶端取得系統上資訊的未經授權存取權。</span><span class="sxs-lookup"><span data-stu-id="9c389-105">Impersonation prevents a client from obtaining unauthorized access to information on the system.</span></span>

<span data-ttu-id="9c389-106">本主題將討論下列各節：</span><span class="sxs-lookup"><span data-stu-id="9c389-106">The following sections are discussed in this topic:</span></span>

-   [<span data-ttu-id="9c389-107">註冊提供者進行模擬</span><span class="sxs-lookup"><span data-stu-id="9c389-107">Registering a Provider for Impersonation</span></span>](#registering-a-provider-for-impersonation)
-   [<span data-ttu-id="9c389-108">設定提供者內的模擬層級</span><span class="sxs-lookup"><span data-stu-id="9c389-108">Setting Impersonation Levels Within a Provider</span></span>](#setting-impersonation-levels-within-a-provider)
-   [<span data-ttu-id="9c389-109">維護提供者中的安全性層級</span><span class="sxs-lookup"><span data-stu-id="9c389-109">Maintaining Security Levels in a Provider</span></span>](#maintaining-security-levels-in-a-provider)
-   [<span data-ttu-id="9c389-110">處理提供者中的拒絕存取訊息</span><span class="sxs-lookup"><span data-stu-id="9c389-110">Handling Access Denied Messages in a Provider</span></span>](#handling-access-denied-messages-in-a-provider)
-   [<span data-ttu-id="9c389-111">報告部分實例</span><span class="sxs-lookup"><span data-stu-id="9c389-111">Reporting Partial Instances</span></span>](#reporting-partial-instances)
-   [<span data-ttu-id="9c389-112">報告部分列舉</span><span class="sxs-lookup"><span data-stu-id="9c389-112">Reporting Partial Enumerations</span></span>](#reporting-partial-enumerations)
-   [<span data-ttu-id="9c389-113">對拒絕存取程式碼進行偵錯工具</span><span class="sxs-lookup"><span data-stu-id="9c389-113">Debugging Your Access Denied Code</span></span>](#debugging-your-access-denied-code)
-   [<span data-ttu-id="9c389-114">相關主題</span><span class="sxs-lookup"><span data-stu-id="9c389-114">Related topics</span></span>](#related-topics)

<span data-ttu-id="9c389-115">WMI 通常會以高安全性層級的系統管理服務來執行，並使用 LocalServer 安全性內容。</span><span class="sxs-lookup"><span data-stu-id="9c389-115">WMI typically runs as an administrative service at a high security level, using the LocalServer security context.</span></span> <span data-ttu-id="9c389-116">使用系統管理服務會提供 WMI 存取特殊許可權資訊的方法。</span><span class="sxs-lookup"><span data-stu-id="9c389-116">Using an administrative service gives WMI the means to access privileged information.</span></span> <span data-ttu-id="9c389-117">當呼叫提供者取得資訊時，WMI 會將其安全識別碼 (SID) 傳送給提供者，讓提供者能夠存取相同高安全性層級的資訊。</span><span class="sxs-lookup"><span data-stu-id="9c389-117">When calling a provider for information, WMI passes its security identifier (SID) to the provider, enabling the provider to access information at the same high security level.</span></span>

<span data-ttu-id="9c389-118">在 WMI 應用程式啟動過程中，Windows 作業系統會為 WMI 應用程式提供開始處理常式之使用者的安全性內容。</span><span class="sxs-lookup"><span data-stu-id="9c389-118">During the WMI application launch process, the Windows operating system gives the WMI application the security context of the user who began the process.</span></span> <span data-ttu-id="9c389-119">使用者的安全性內容通常是比 LocalServer 更低的安全性層級，因此使用者可能沒有許可權可以存取 WMI 可用的所有資訊。</span><span class="sxs-lookup"><span data-stu-id="9c389-119">The security context of the user is typically a lower security level than LocalServer, so the user may not have permission to access all of the information available to WMI.</span></span> <span data-ttu-id="9c389-120">當使用者應用程式要求動態資訊時，WMI 會將使用者的 SID 傳遞給對應的提供者。</span><span class="sxs-lookup"><span data-stu-id="9c389-120">When the user application asks for dynamic information, WMI passes the SID of the user to the corresponding provider.</span></span> <span data-ttu-id="9c389-121">如果有適當的寫入，則提供者會嘗試使用使用者 SID （而不是提供者 SID）來存取訊號。</span><span class="sxs-lookup"><span data-stu-id="9c389-121">If written appropriately, the provider attempts to access information with the user SID, rather than the provider SID.</span></span>

<span data-ttu-id="9c389-122">若要讓提供者成功模擬用戶端應用程式，用戶端應用程式和提供者必須符合下列準則：</span><span class="sxs-lookup"><span data-stu-id="9c389-122">For the provider to successfully impersonate the client application, the client application and provider must meet the following criteria:</span></span>

-   <span data-ttu-id="9c389-123">用戶端應用程式必須使用 **RPC \_ c \_ IMP \_ level \_** 模擬或 **RPC \_ c \_ IMP \_ 層級 \_ 委派** 的 COM 連接安全性層級來呼叫 WMI。</span><span class="sxs-lookup"><span data-stu-id="9c389-123">The client application must call WMI with a COM connection security level of **RPC\_C\_IMP\_LEVEL\_IMPERSONATE** or **RPC\_C\_IMP\_LEVEL\_DELEGATE**.</span></span> <span data-ttu-id="9c389-124">如需詳細資訊，請參閱 [維護 WMI 安全性](maintaining-wmi-security.md)。</span><span class="sxs-lookup"><span data-stu-id="9c389-124">For more information, see [Maintaining WMI Security](maintaining-wmi-security.md).</span></span>
-   <span data-ttu-id="9c389-125">提供者必須以模擬提供者的形式向 WMI 註冊。</span><span class="sxs-lookup"><span data-stu-id="9c389-125">The provider must register with WMI as an impersonation provider.</span></span> <span data-ttu-id="9c389-126">如需詳細資訊，請參閱 [註冊提供者以進行](#registering-a-provider-for-impersonation)模擬。</span><span class="sxs-lookup"><span data-stu-id="9c389-126">For more information, see [Registering a Provider for Impersonation](#registering-a-provider-for-impersonation).</span></span>
-   <span data-ttu-id="9c389-127">提供者必須先切換至用戶端應用程式的安全性層級，才能存取特殊許可權資訊。</span><span class="sxs-lookup"><span data-stu-id="9c389-127">The provider must switch to the security level of the client application before accessing privileged information.</span></span> <span data-ttu-id="9c389-128">如需詳細資訊，請參閱 [設定提供者內的模擬層級](#setting-impersonation-levels-within-a-provider)。</span><span class="sxs-lookup"><span data-stu-id="9c389-128">For more information, see [Setting Impersonation Levels Within a Provider](#setting-impersonation-levels-within-a-provider).</span></span>
-   <span data-ttu-id="9c389-129">如果拒絕存取這項資訊，則提供者必須正確地處理錯誤狀況。</span><span class="sxs-lookup"><span data-stu-id="9c389-129">The provider must correctly handle error conditions if access to this information is denied.</span></span> <span data-ttu-id="9c389-130">如需詳細資訊，請參閱 [處理提供者中的拒絕存取訊息](#handling-access-denied-messages-in-a-provider)。</span><span class="sxs-lookup"><span data-stu-id="9c389-130">For more information, see [Handling Access Denied Messages in a Provider](#handling-access-denied-messages-in-a-provider).</span></span>

## <a name="registering-a-provider-for-impersonation"></a><span data-ttu-id="9c389-131">註冊提供者進行模擬</span><span class="sxs-lookup"><span data-stu-id="9c389-131">Registering a Provider for Impersonation</span></span>

<span data-ttu-id="9c389-132">WMI 只會將用戶端應用程式的 SID 傳遞給已註冊為模擬提供者的提供者。</span><span class="sxs-lookup"><span data-stu-id="9c389-132">WMI only passes the SID of a client application to providers who have registered as impersonation providers.</span></span> <span data-ttu-id="9c389-133">若要讓提供者執行模擬，您必須修改提供者註冊程式。</span><span class="sxs-lookup"><span data-stu-id="9c389-133">Enabling a provider to perform impersonation requires that you modify the provider registration process.</span></span>

<span data-ttu-id="9c389-134">下列程式說明如何註冊提供者以進行模擬。</span><span class="sxs-lookup"><span data-stu-id="9c389-134">The following procedure describes how to register a provider for impersonation.</span></span> <span data-ttu-id="9c389-135">此程式假設您已瞭解註冊程式。</span><span class="sxs-lookup"><span data-stu-id="9c389-135">The procedure assumes that you already understand the registration process.</span></span> <span data-ttu-id="9c389-136">如需註冊程式的詳細資訊，請參閱 [註冊提供者](registering-a-provider.md)。</span><span class="sxs-lookup"><span data-stu-id="9c389-136">For more information about the registration process, see [Registering a Provider](registering-a-provider.md).</span></span>

<span data-ttu-id="9c389-137">**註冊提供者進行模擬**</span><span class="sxs-lookup"><span data-stu-id="9c389-137">**To register a provider for impersonation**</span></span>

1.  <span data-ttu-id="9c389-138">將代表提供者的 [**\_ \_ Win32Provider**](--win32provider.md)類別的 [**ImpersonationLevel**](swbemsecurity-impersonationlevel.md)屬性設定為1。</span><span class="sxs-lookup"><span data-stu-id="9c389-138">Set the [**ImpersonationLevel**](swbemsecurity-impersonationlevel.md) property of the [**\_\_Win32Provider**](--win32provider.md) class that represents your provider to 1.</span></span>

    <span data-ttu-id="9c389-139">[**ImpersonationLevel**](swbemsecurity-impersonationlevel.md)屬性會記錄提供者是否支援模擬。</span><span class="sxs-lookup"><span data-stu-id="9c389-139">The [**ImpersonationLevel**](swbemsecurity-impersonationlevel.md) property documents whether the provider supports impersonation or not.</span></span> <span data-ttu-id="9c389-140">將 **ImpersonationLevel** 設定為0，表示提供者不會模擬用戶端，並在與 WMI 相同的使用者內容中執行所有要求的作業。</span><span class="sxs-lookup"><span data-stu-id="9c389-140">Setting **ImpersonationLevel** to 0 indicates that the provider does not impersonate the client and performs all requested operations in the same user context as WMI.</span></span> <span data-ttu-id="9c389-141">將 **ImpersonationLevel** 設定為1，表示提供者使用模擬呼叫來檢查代表用戶端執行的作業。</span><span class="sxs-lookup"><span data-stu-id="9c389-141">Setting **ImpersonationLevel** to 1 indicates that the provider uses impersonation calls to check operations performed on behalf of the client.</span></span>

2.  <span data-ttu-id="9c389-142">將相同 [**\_ \_ Win32Provider**](--win32provider.md)類別的 **PerUserInitialization** 屬性設定為 **TRUE**。</span><span class="sxs-lookup"><span data-stu-id="9c389-142">Set the **PerUserInitialization** property of the same [**\_\_Win32Provider**](--win32provider.md) class to **TRUE**.</span></span>

> [!Note]  
> <span data-ttu-id="9c389-143">如果您註冊提供者，並將 [**\_ \_ Win32Provider**](--win32provider.md)屬性 **InitializeAsAdminFirst** 設定為 **TRUE**，則提供者只會在初始化階段使用管理層級執行緒安全性權杖。</span><span class="sxs-lookup"><span data-stu-id="9c389-143">If you register a provider with the [**\_\_Win32Provider**](--win32provider.md) property **InitializeAsAdminFirst** set to **TRUE**, then the provider uses the administration-level thread security token only during the initialization phase.</span></span> <span data-ttu-id="9c389-144">呼叫 [**CoImpersonateClient**](/windows/win32/api/combaseapi/nf-combaseapi-coimpersonateclient) 時，提供者會使用 WMI 的安全性內容，而不會使用用戶端的安全性內容。</span><span class="sxs-lookup"><span data-stu-id="9c389-144">While a call to [**CoImpersonateClient**](/windows/win32/api/combaseapi/nf-combaseapi-coimpersonateclient) does not fail, the provider uses the security context of WMI and not of the client.</span></span>

 

<span data-ttu-id="9c389-145">下列程式碼範例示範如何註冊提供者以進行模擬。</span><span class="sxs-lookup"><span data-stu-id="9c389-145">The following code example shows how to register a provider for impersonation.</span></span>

``` syntax
instance of __Win32Provider
{
    CLSID = "{FD4F53E0-65DC-11d1-AB64-00C04FD9159E}";
    ImpersonationLevel = 1;
    Name = "MS_NT_EVENTLOG_PROVIDER";
    PerUserInitialization = TRUE;
};
```

## <a name="setting-impersonation-levels-within-a-provider"></a><span data-ttu-id="9c389-146">設定提供者內的模擬層級</span><span class="sxs-lookup"><span data-stu-id="9c389-146">Setting Impersonation Levels Within a Provider</span></span>

<span data-ttu-id="9c389-147">如果您使用 [**\_ \_ Win32Provider**](--win32provider.md)類別屬性 [**ImpersonationLevel**](swbemsecurity-impersonationlevel.md)設定為1來註冊提供者，則 WMI 會呼叫您的提供者來模擬不同的用戶端。</span><span class="sxs-lookup"><span data-stu-id="9c389-147">If you register a provider with the [**\_\_Win32Provider**](--win32provider.md) class property [**ImpersonationLevel**](swbemsecurity-impersonationlevel.md) set to 1, then WMI calls your provider to impersonate various clients.</span></span> <span data-ttu-id="9c389-148">若要處理這些呼叫，請在您的 [**IWbemServices**](/windows/desktop/api/WbemCli/nn-wbemcli-iwbemservices)介面的執行中使用 [**CoImpersonateClient**](/windows/win32/api/combaseapi/nf-combaseapi-coimpersonateclient)和 [**CoRevertToSelf**](/windows/win32/api/combaseapi/nf-combaseapi-coreverttoself) COM 函數。</span><span class="sxs-lookup"><span data-stu-id="9c389-148">To handle these calls, use the [**CoImpersonateClient**](/windows/win32/api/combaseapi/nf-combaseapi-coimpersonateclient) and [**CoRevertToSelf**](/windows/win32/api/combaseapi/nf-combaseapi-coreverttoself) COM functions in your implementation of the [**IWbemServices**](/windows/desktop/api/WbemCli/nn-wbemcli-iwbemservices) interface.</span></span>

<span data-ttu-id="9c389-149">[**CoImpersonateClient**](/windows/win32/api/combaseapi/nf-combaseapi-coimpersonateclient)函式可讓伺服器模擬發出呼叫的用戶端。</span><span class="sxs-lookup"><span data-stu-id="9c389-149">The [**CoImpersonateClient**](/windows/win32/api/combaseapi/nf-combaseapi-coimpersonateclient) function allows a server to impersonate the client that made the call.</span></span> <span data-ttu-id="9c389-150">藉由將 **CoImpersonateClient** 呼叫放入 [**IWbemServices**](/windows/desktop/api/WbemCli/nn-wbemcli-iwbemservices)的執行，您可以讓您的提供者設定提供者的執行緒 token，使其符合用戶端的執行緒 token，進而模擬用戶端。</span><span class="sxs-lookup"><span data-stu-id="9c389-150">By placing a call to **CoImpersonateClient** into your implementation of [**IWbemServices**](/windows/desktop/api/WbemCli/nn-wbemcli-iwbemservices), you allow your provider to set the thread token of the provider to match the thread token of the client, and thus impersonate the client.</span></span> <span data-ttu-id="9c389-151">如果您未呼叫 **CoImpersonateClient**，則您的提供者會以系統管理員層級的安全性執行程式碼，進而造成潛在的安全性弱點。</span><span class="sxs-lookup"><span data-stu-id="9c389-151">If you do not call **CoImpersonateClient**, your provider executes code at an administrator level of security, thereby creating a potential security vulnerability.</span></span> <span data-ttu-id="9c389-152">如果您的提供者暫時需要以系統管理員身分執行，或要手動執行存取檢查，請呼叫 [**CoRevertToSelf**](/windows/win32/api/combaseapi/nf-combaseapi-coreverttoself)。</span><span class="sxs-lookup"><span data-stu-id="9c389-152">If your provider temporarily needs to act as an administrator or perform the access check manually, then call [**CoRevertToSelf**](/windows/win32/api/combaseapi/nf-combaseapi-coreverttoself).</span></span>

<span data-ttu-id="9c389-153">相較于 [**CoImpersonateClient**](/windows/win32/api/combaseapi/nf-combaseapi-coimpersonateclient)， [**CoRevertToSelf**](/windows/win32/api/combaseapi/nf-combaseapi-coreverttoself) 是處理執行緒模擬層級的 COM 函數。</span><span class="sxs-lookup"><span data-stu-id="9c389-153">In contrast to [**CoImpersonateClient**](/windows/win32/api/combaseapi/nf-combaseapi-coimpersonateclient), [**CoRevertToSelf**](/windows/win32/api/combaseapi/nf-combaseapi-coreverttoself) is a COM function that handles thread impersonation levels.</span></span> <span data-ttu-id="9c389-154">在此情況下， **CoRevertToSelf** 會將模擬等級變更回原始的模擬設定。</span><span class="sxs-lookup"><span data-stu-id="9c389-154">In this case, **CoRevertToSelf** changes the impersonation level back to the original impersonation setting.</span></span> <span data-ttu-id="9c389-155">一般情況下，提供者一開始是系統管理員，而且會根據其是否正在進行代表呼叫端或本身呼叫的呼叫，在 **CoImpersonateClient** 和 **CoRevertToSelf** 之間進行替代。</span><span class="sxs-lookup"><span data-stu-id="9c389-155">In general, the provider is initially an administrator and alternates between **CoImpersonateClient** and **CoRevertToSelf** depending on whether it is making a call that represents the caller or its own calls.</span></span> <span data-ttu-id="9c389-156">提供者必須負責正確地放置這些呼叫，如此才不會向終端使用者公開安全性漏洞。</span><span class="sxs-lookup"><span data-stu-id="9c389-156">It is the responsibility of the provider to place these calls correctly so as not to expose a security hole to the end user.</span></span> <span data-ttu-id="9c389-157">例如，提供者應該只在模擬的程式碼序列內呼叫原生 Windows 函數。</span><span class="sxs-lookup"><span data-stu-id="9c389-157">For example, the provider should only call native Windows functions within the impersonated code sequence.</span></span>

> [!Note]  
> <span data-ttu-id="9c389-158">[**CoImpersonateClient**](/windows/win32/api/combaseapi/nf-combaseapi-coimpersonateclient)和 [**CoRevertToSelf**](/windows/win32/api/combaseapi/nf-combaseapi-coreverttoself)的目的是設定提供者的安全性。</span><span class="sxs-lookup"><span data-stu-id="9c389-158">The purpose of [**CoImpersonateClient**](/windows/win32/api/combaseapi/nf-combaseapi-coimpersonateclient) and [**CoRevertToSelf**](/windows/win32/api/combaseapi/nf-combaseapi-coreverttoself) is to set security for a provider.</span></span> <span data-ttu-id="9c389-159">如果您判斷您的模擬失敗，您應該透過 [**IWbemObjectSink：： SetStatus**](/windows/desktop/api/Wbemcli/nf-wbemcli-iwbemobjectsink-setstatus)將適當的完成程式碼傳回至 WMI。</span><span class="sxs-lookup"><span data-stu-id="9c389-159">If you determine that your impersonation has failed, you should return an appropriate completion code to WMI through [**IWbemObjectSink::SetStatus**](/windows/desktop/api/Wbemcli/nf-wbemcli-iwbemobjectsink-setstatus).</span></span> <span data-ttu-id="9c389-160">如需詳細資訊，請參閱 [處理提供者中的拒絕存取訊息](#handling-access-denied-messages-in-a-provider)。</span><span class="sxs-lookup"><span data-stu-id="9c389-160">For more information, see [Handling Access Denied Messages in a Provider](#handling-access-denied-messages-in-a-provider).</span></span>

 

## <a name="maintaining-security-levels-in-a-provider"></a><span data-ttu-id="9c389-161">維護提供者中的安全性層級</span><span class="sxs-lookup"><span data-stu-id="9c389-161">Maintaining Security Levels in a Provider</span></span>

<span data-ttu-id="9c389-162">提供者無法在 [**IWbemServices**](/windows/desktop/api/WbemCli/nn-wbemcli-iwbemservices)的執行中呼叫 [**CoImpersonateClient**](/windows/win32/api/combaseapi/nf-combaseapi-coimpersonateclient)一次，並假設提供者的持續時間內會保留模擬認證。</span><span class="sxs-lookup"><span data-stu-id="9c389-162">Providers cannot call [**CoImpersonateClient**](/windows/win32/api/combaseapi/nf-combaseapi-coimpersonateclient) one time in an implementation of [**IWbemServices**](/windows/desktop/api/WbemCli/nn-wbemcli-iwbemservices) and assume that the impersonation credentials remain in place for the duration of the provider.</span></span> <span data-ttu-id="9c389-163">相反地，在執行過程中多次呼叫 **CoImpersonateClient** ，以防止 WMI 變更認證。</span><span class="sxs-lookup"><span data-stu-id="9c389-163">Instead, call **CoImpersonateClient** multiple times during the course of an implementation to keep WMI from changing the credentials.</span></span>

<span data-ttu-id="9c389-164">為提供者設定模擬的主要考慮是重新進入。</span><span class="sxs-lookup"><span data-stu-id="9c389-164">The main concern for setting impersonation for a provider is reentrancy.</span></span> <span data-ttu-id="9c389-165">在此內容中，當提供者呼叫 WMI 以取得資訊並等候 WMI 回呼提供者時，就會發生重新進入。</span><span class="sxs-lookup"><span data-stu-id="9c389-165">In this context, reentrancy is when a provider makes a call to WMI for information and waits until WMI calls back into the provider.</span></span> <span data-ttu-id="9c389-166">基本上，執行的執行緒會離開提供者程式碼，只會在日後重新輸入程式碼。</span><span class="sxs-lookup"><span data-stu-id="9c389-166">In essence, the thread of execution leaves the provider code, only to reenter the code at a later date.</span></span> <span data-ttu-id="9c389-167">「重入」是 COM 設計的一部分，而且通常不會有問題。</span><span class="sxs-lookup"><span data-stu-id="9c389-167">Reentry is a part of the design of COM, and is generally not a concern.</span></span> <span data-ttu-id="9c389-168">不過，當執行的執行緒進入 WMI 時，執行緒會採用 WMI 的模擬層級。</span><span class="sxs-lookup"><span data-stu-id="9c389-168">However, when the thread of execution enters WMI, the thread takes on the impersonation levels of WMI.</span></span> <span data-ttu-id="9c389-169">當執行緒返回提供者時，您必須使用另一個 [**CoImpersonateClient**](/windows/win32/api/combaseapi/nf-combaseapi-coimpersonateclient)呼叫來重設模擬層級。</span><span class="sxs-lookup"><span data-stu-id="9c389-169">When the thread returns to the provider, you must reset the impersonation levels with another call to [**CoImpersonateClient**](/windows/win32/api/combaseapi/nf-combaseapi-coimpersonateclient).</span></span>

<span data-ttu-id="9c389-170">若要保護您的提供者中的安全性漏洞，您應該只在模擬用戶端時，將可重新進入的呼叫加入至 WMI。</span><span class="sxs-lookup"><span data-stu-id="9c389-170">To protect yourself from security holes in your provider, you should make reentrant calls into WMI only while impersonating the client.</span></span> <span data-ttu-id="9c389-171">也就是說，在您呼叫 [**CoImpersonateClient**](/windows/win32/api/combaseapi/nf-combaseapi-coimpersonateclient) 之後，以及在呼叫 [**CoRevertToSelf**](/windows/win32/api/combaseapi/nf-combaseapi-coreverttoself)之前，應該發出 WMI 的呼叫。</span><span class="sxs-lookup"><span data-stu-id="9c389-171">That is, calls to WMI should be made after you call [**CoImpersonateClient**](/windows/win32/api/combaseapi/nf-combaseapi-coimpersonateclient) and before you call [**CoRevertToSelf**](/windows/win32/api/combaseapi/nf-combaseapi-coreverttoself).</span></span> <span data-ttu-id="9c389-172">因為 **CoRevertToSelf** 會將模擬設定為使用者層級的 wmi 正在執行，通常是 LocalSystem，在呼叫 **CoRevertToSelf** 之後可重新進入 wmi 的呼叫，可讓使用者和任何呼叫的提供者都有更多功能。</span><span class="sxs-lookup"><span data-stu-id="9c389-172">Because **CoRevertToSelf** causes the impersonation to be set to the user level WMI is running, generally LocalSystem, reentrant calls to WMI after calling **CoRevertToSelf** could give the user, and any providers called, a lot more capabilities than they should have.</span></span>

> [!Note]  
> <span data-ttu-id="9c389-173">如果您呼叫系統函數或其他介面方法，則不保證會維護呼叫內容。</span><span class="sxs-lookup"><span data-stu-id="9c389-173">If you call a system function or another interface method, the call context is not guaranteed to be maintained.</span></span>

 

## <a name="handling-access-denied-messages-in-a-provider"></a><span data-ttu-id="9c389-174">處理提供者中的拒絕存取訊息</span><span class="sxs-lookup"><span data-stu-id="9c389-174">Handling Access Denied Messages in a Provider</span></span>

<span data-ttu-id="9c389-175">當用戶端要求沒有存取權的類別或資訊時，會出現大部分的拒絕存取錯誤訊息。</span><span class="sxs-lookup"><span data-stu-id="9c389-175">Most Access Denied error messages appear when a client requests a class or information to which they do not have access.</span></span> <span data-ttu-id="9c389-176">如果提供者傳回拒絕存取的錯誤訊息至 WMI，而 WMI 將此訊息傳遞至用戶端，則用戶端可以推斷該資訊是否存在。</span><span class="sxs-lookup"><span data-stu-id="9c389-176">If the provider returns an Access Denied error message to WMI and WMI passes this on to the client, the client can infer that the information exists.</span></span> <span data-ttu-id="9c389-177">在某些情況下，這可能會違反安全性。</span><span class="sxs-lookup"><span data-stu-id="9c389-177">In some situations, this can be a breach of security.</span></span> <span data-ttu-id="9c389-178">因此，您的提供者不應將訊息傳播至用戶端。</span><span class="sxs-lookup"><span data-stu-id="9c389-178">Therefore, your provider should not propagate the message to the client.</span></span> <span data-ttu-id="9c389-179">相反地，不應該公開提供者所提供的一組類別。</span><span class="sxs-lookup"><span data-stu-id="9c389-179">Instead, the set of classes that the provider would have supplied should not be exposed.</span></span> <span data-ttu-id="9c389-180">同樣地，動態執行個體提供者應該呼叫基礎資料來源，以判斷如何處理拒絕存取訊息。</span><span class="sxs-lookup"><span data-stu-id="9c389-180">Similarly, a dynamic instance provider should call to the underlying data source to determine how to deal with Access Denied messages.</span></span> <span data-ttu-id="9c389-181">提供者必須負責將該原理複寫至 WMI 環境。</span><span class="sxs-lookup"><span data-stu-id="9c389-181">It is the responsibility of the provider to replicate that philosophy into the WMI environment.</span></span> <span data-ttu-id="9c389-182">如需詳細資訊，請參閱 [報告部分實例](#reporting-partial-instances) 和 [報告部分](#reporting-partial-enumerations)列舉。</span><span class="sxs-lookup"><span data-stu-id="9c389-182">For more information, see [Reporting Partial Instances](#reporting-partial-instances) and [Reporting Partial Enumerations](#reporting-partial-enumerations).</span></span>

<span data-ttu-id="9c389-183">當您判斷您的提供者應該如何處理拒絕存取訊息時，您必須撰寫程式碼並對其進行偵錯工具。</span><span class="sxs-lookup"><span data-stu-id="9c389-183">When you determine how your provider should handle Access Denied messages, you must write and debug your code.</span></span> <span data-ttu-id="9c389-184">在進行偵錯工具時，您通常很方便分辨因為低模擬而造成的拒絕，以及因您的程式碼錯誤而造成的拒絕。</span><span class="sxs-lookup"><span data-stu-id="9c389-184">While debugging, it is often convenient to distinguish between a denial due to low impersonation, and a denial due to an error in your code.</span></span> <span data-ttu-id="9c389-185">您可以在程式碼中使用簡單的測試來判斷差異。</span><span class="sxs-lookup"><span data-stu-id="9c389-185">You can use a simple test in your code to determine the difference.</span></span> <span data-ttu-id="9c389-186">如需詳細資訊，請參閱 [偵錯工具拒絕存取程式碼](#debugging-your-access-denied-code)。</span><span class="sxs-lookup"><span data-stu-id="9c389-186">For more information, see [Debugging your Access Denied Code](#debugging-your-access-denied-code).</span></span>

## <a name="reporting-partial-instances"></a><span data-ttu-id="9c389-187">報告部分實例</span><span class="sxs-lookup"><span data-stu-id="9c389-187">Reporting Partial Instances</span></span>

<span data-ttu-id="9c389-188">拒絕存取訊息的其中一種常見的情況是 WMI 無法提供所有資訊來填滿實例。</span><span class="sxs-lookup"><span data-stu-id="9c389-188">One common occurrence of an Access Denied message is when WMI cannot provide all the information to fill an instance.</span></span> <span data-ttu-id="9c389-189">例如，用戶端可能會有權查看硬碟物件，但可能沒有許可權可查看硬碟上有多少可用的空間。</span><span class="sxs-lookup"><span data-stu-id="9c389-189">For example, a client may have the authority to view a hard disk drive object, but may not have authority to see how much space is available on the hard disk drive itself.</span></span> <span data-ttu-id="9c389-190">當提供者因為存取違規而無法完全填滿具有屬性的實例時，您的提供者必須判斷如何處理任何情況。</span><span class="sxs-lookup"><span data-stu-id="9c389-190">Your provider must determine how to handle any situation when the provider cannot completely fill an instance with properties due to an access violation.</span></span>

<span data-ttu-id="9c389-191">WMI 不需要單一回應對實例具有部分存取權的用戶端。</span><span class="sxs-lookup"><span data-stu-id="9c389-191">WMI does not require a single response to clients that have partial access to an instance.</span></span> <span data-ttu-id="9c389-192">相反地，WMI 1.x 版允許提供者下列其中一個選項：</span><span class="sxs-lookup"><span data-stu-id="9c389-192">Instead, WMI version 1.x allows the provider one of the following options:</span></span>

-   <span data-ttu-id="9c389-193">使用 **WBEM \_ E \_ \_ 拒絕存取** 來使整個作業失敗，並不會傳回任何實例。</span><span class="sxs-lookup"><span data-stu-id="9c389-193">Fail the entire operation with **WBEM\_E\_ACCESS\_DENIED** and return no instances.</span></span>

    <span data-ttu-id="9c389-194">傳回錯誤物件以及 **WBEM \_ E \_ \_ 拒絕存取**，以描述拒絕的原因。</span><span class="sxs-lookup"><span data-stu-id="9c389-194">Return an error object along with **WBEM\_E\_ACCESS\_DENIED**, to describe the reason for the denial.</span></span>

-   <span data-ttu-id="9c389-195">傳回所有可用的屬性，並以 **Null** 填滿無法使用的屬性。</span><span class="sxs-lookup"><span data-stu-id="9c389-195">Return all available properties, and fill unavailable properties with **NULL**.</span></span>

> [!Note]  
> <span data-ttu-id="9c389-196">請確定傳回 **WBEM \_ E \_ \_ 拒絕存取** 未在您的企業中建立安全性漏洞。</span><span class="sxs-lookup"><span data-stu-id="9c389-196">Make sure that returning **WBEM\_E\_ACCESS\_DENIED** does not create a security hole in your enterprise.</span></span>

 

## <a name="reporting-partial-enumerations"></a><span data-ttu-id="9c389-197">報告部分列舉</span><span class="sxs-lookup"><span data-stu-id="9c389-197">Reporting Partial Enumerations</span></span>

<span data-ttu-id="9c389-198">存取違規的另一項常見的情況是 WMI 無法傳回所有列舉。</span><span class="sxs-lookup"><span data-stu-id="9c389-198">Another common occurrence of an access violation is when WMI cannot return all of an enumeration.</span></span> <span data-ttu-id="9c389-199">例如，用戶端可能會有存取權來查看所有區域網路電腦物件，但可能無法存取其網域以外的電腦物件。</span><span class="sxs-lookup"><span data-stu-id="9c389-199">For example, a client may have access to view all of the local network computer objects, but may not have access to view computer objects outside of his domain.</span></span> <span data-ttu-id="9c389-200">當列舉因存取違規而無法完成時，您的提供者必須決定如何處理任何情況。</span><span class="sxs-lookup"><span data-stu-id="9c389-200">Your provider must determine how to handle any situation when an enumeration cannot be completed due to an access violation.</span></span>

<span data-ttu-id="9c389-201">與執行個體提供者一樣，WMI 不需要對部分列舉進行單一回應。</span><span class="sxs-lookup"><span data-stu-id="9c389-201">As with an instance provider, WMI does not require a single response to a partial enumeration.</span></span> <span data-ttu-id="9c389-202">相反地，WMI 1.x 版允許提供者使用下列其中一個選項：</span><span class="sxs-lookup"><span data-stu-id="9c389-202">Instead, WMI version 1.x allows a provider one of the following options:</span></span>

-   <span data-ttu-id="9c389-203">針對提供者可存取的所有實例，傳回 **WBEM \_ S \_ \_** 。</span><span class="sxs-lookup"><span data-stu-id="9c389-203">Return **WBEM\_S\_NO\_ERROR** for all instances that the provider can access.</span></span>

    <span data-ttu-id="9c389-204">如果您使用此選項，使用者就不會察覺到某些實例無法使用。</span><span class="sxs-lookup"><span data-stu-id="9c389-204">If you use this option, the user is not aware that some instances were not available.</span></span> <span data-ttu-id="9c389-205">許多提供者（例如使用結構化查詢語言 (SQL)  (SQL) 具有資料列層級安全性）的提供者，會使用呼叫端的安全性層級來定義結果集，以傳回成功的部分結果。</span><span class="sxs-lookup"><span data-stu-id="9c389-205">A number of providers, such as those using Structured Query Language (SQL) with row-level security, return successful partial results using the security level of the caller to define the result set.</span></span>

-   <span data-ttu-id="9c389-206">使用 **WBEM \_ E \_ \_ 拒絕存取** 來使整個作業失敗，並不會傳回任何實例。</span><span class="sxs-lookup"><span data-stu-id="9c389-206">Fail the entire operation with **WBEM\_E\_ACCESS\_DENIED** and return no instances.</span></span>

    <span data-ttu-id="9c389-207">提供者可以選擇性地包含描述用戶端情況的錯誤物件。</span><span class="sxs-lookup"><span data-stu-id="9c389-207">The provider may optionally include an error object that describes the situation to the client.</span></span> <span data-ttu-id="9c389-208">請注意，某些提供者可能會以序列方式存取資料來源，而且在透過列舉中途之前可能不會發生拒絕。</span><span class="sxs-lookup"><span data-stu-id="9c389-208">Note that some providers may access data sources serially and may not encounter denials until partway through the enumeration.</span></span>

-   <span data-ttu-id="9c389-209">傳回所有可存取的實例，但也會傳回 nonerror 狀態碼 **WBEM \_ S \_ \_ 拒絕存取**。</span><span class="sxs-lookup"><span data-stu-id="9c389-209">Return all of the instances that can be accessed but also return the nonerror status code **WBEM\_S\_ACCESS\_DENIED**.</span></span>

    <span data-ttu-id="9c389-210">提供者應該在列舉期間記下拒絕，並可繼續提供實例，並完成 nonerror 狀態碼。</span><span class="sxs-lookup"><span data-stu-id="9c389-210">The provider should note the denial during enumeration and may continue providing instances, finishing up with the nonerror status code.</span></span> <span data-ttu-id="9c389-211">提供者也可以選擇在第一次拒絕時終止列舉。</span><span class="sxs-lookup"><span data-stu-id="9c389-211">The provider may also elect to terminate the enumeration at the first denial.</span></span> <span data-ttu-id="9c389-212">此選項的理由是不同的提供者具有不同的抓取範例。</span><span class="sxs-lookup"><span data-stu-id="9c389-212">The justification for this option is that different providers have different retrieval paradigms.</span></span> <span data-ttu-id="9c389-213">在探索存取違規之前，提供者可能已經提供實例。</span><span class="sxs-lookup"><span data-stu-id="9c389-213">A provider may have already delivered instances before discovering an access violation.</span></span> <span data-ttu-id="9c389-214">有些提供者可能會選擇繼續提供其他實例，而其他則可能想要終止。</span><span class="sxs-lookup"><span data-stu-id="9c389-214">Some providers may elect to continue providing other instances and others may wish to terminate.</span></span>

<span data-ttu-id="9c389-215">由於 COM 的結構，因此您無法在錯誤物件以外的錯誤中封送處理回任何資訊。</span><span class="sxs-lookup"><span data-stu-id="9c389-215">Due to the structure of COM, you cannot marshal back any information during an error except for an error object.</span></span> <span data-ttu-id="9c389-216">因此，您無法同時傳回信息和錯誤碼。</span><span class="sxs-lookup"><span data-stu-id="9c389-216">Therefore, you cannot return both information and an error code.</span></span> <span data-ttu-id="9c389-217">如果您選擇傳回信息，則必須改為使用 nonerror 狀態碼。</span><span class="sxs-lookup"><span data-stu-id="9c389-217">If you choose to return information, you must use a nonerror status code instead.</span></span>

## <a name="debugging-your-access-denied-code"></a><span data-ttu-id="9c389-218">對拒絕存取程式碼進行偵錯工具</span><span class="sxs-lookup"><span data-stu-id="9c389-218">Debugging Your Access Denied Code</span></span>

<span data-ttu-id="9c389-219">某些應用程式可能會使用低於 **RPC \_ C \_ IMP \_ 層級 \_** 模擬的模擬層級。</span><span class="sxs-lookup"><span data-stu-id="9c389-219">Some applications may use impersonation levels lower than **RPC\_C\_IMP\_LEVEL\_IMPERSONATE**.</span></span> <span data-ttu-id="9c389-220">在此情況下，用戶端應用程式提供者所做的大部分模擬呼叫將會失敗。</span><span class="sxs-lookup"><span data-stu-id="9c389-220">In this case, most impersonation calls made by the provider for the client application will fail.</span></span> <span data-ttu-id="9c389-221">若要成功設計和執行提供者，您必須記住這個概念。</span><span class="sxs-lookup"><span data-stu-id="9c389-221">To successfully design and implement a provider, you must keep this idea in mind.</span></span>

<span data-ttu-id="9c389-222">依預設，只能存取提供者的其他模擬層級是 **RPC \_ C \_ IMP \_ level \_ 識別**。</span><span class="sxs-lookup"><span data-stu-id="9c389-222">By default, the only other level of impersonation that can access a provider is **RPC\_C\_IMP\_LEVEL\_IDENTIFY**.</span></span> <span data-ttu-id="9c389-223">在用戶端應用程式使用 **RPC \_ C \_ IMP \_ 層級 \_ 識別** 的情況下， [**CoImpersonateClient**](/windows/win32/api/combaseapi/nf-combaseapi-coimpersonateclient) 不會傳回錯誤碼。</span><span class="sxs-lookup"><span data-stu-id="9c389-223">In cases where a client application uses **RPC\_C\_IMP\_LEVEL\_IDENTIFY**, [**CoImpersonateClient**](/windows/win32/api/combaseapi/nf-combaseapi-coimpersonateclient) does not return an error code.</span></span> <span data-ttu-id="9c389-224">相反地，提供者只會模擬用戶端以供識別之用。</span><span class="sxs-lookup"><span data-stu-id="9c389-224">Instead, the provider impersonates the client for identification purposes only.</span></span> <span data-ttu-id="9c389-225">因此，提供者所呼叫的大部分 Windows 方法都會傳回拒絕存取訊息。</span><span class="sxs-lookup"><span data-stu-id="9c389-225">Therefore, most Windows methods called by the provider will return an access denied message.</span></span> <span data-ttu-id="9c389-226">這在實務上是無害的，因為不允許使用者進行任何不適當的動作。</span><span class="sxs-lookup"><span data-stu-id="9c389-226">This is harmless in practice, as users will not be permitted to do anything inappropriate.</span></span> <span data-ttu-id="9c389-227">不過，在提供者開發期間，它可能會很有用，以得知用戶端是否真的經過模擬。</span><span class="sxs-lookup"><span data-stu-id="9c389-227">However, it may be useful during provider development to know whether the client was truly impersonated or not.</span></span>

<span data-ttu-id="9c389-228">程式碼需要下列參考，且必須 \# 要有語句才能正確編譯。</span><span class="sxs-lookup"><span data-stu-id="9c389-228">The code requires the following references and \#include statements to compile correctly.</span></span>


```C++
#define _WIN32_DCOM
#include <iostream>
using namespace std;
#include <wbemidl.h>
```



<span data-ttu-id="9c389-229">下列程式碼範例示範如何判斷提供者是否已成功模擬用戶端應用程式。</span><span class="sxs-lookup"><span data-stu-id="9c389-229">The following code example shows how to determine whether a provider has successfully impersonated a client application.</span></span>


```C++
DWORD dwImp = 0;
HANDLE hThreadTok;
DWORD dwBytesReturned;
BOOL bRes;

// You must call this before trying to open a thread token!
CoImpersonateClient();

bRes = OpenThreadToken(
    GetCurrentThread(),
    TOKEN_QUERY,
    TRUE,
    &hThreadTok
);

if (bRes == FALSE)
{
    printf("Unable to read thread token (%d)\n", GetLastError());
    return 0;
}

bRes = GetTokenInformation(
    hThreadTok,
    TokenImpersonationLevel, 
    &dwImp,
    sizeof(DWORD),
    &dwBytesReturned
);

if (!bRes)
{
    printf("Unable to read impersonation level\n");
    CloseHandle(hThreadTok);
    return 0;
}

switch (dwImp)
{
case SecurityAnonymous:
    printf("SecurityAnonymous\n");
    break;

case SecurityIdentification:
    printf("SecurityIdentification\n");
    break;

case SecurityImpersonation:
    printf("SecurityImpersonation\n");
    break;

case SecurityDelegation:
    printf("SecurityDelegation\n");
    break;

default:
    printf("Error. Unable to determine impersonation level\n");
    break;
}

CloseHandle(hThreadTok);
```



## <a name="related-topics"></a><span data-ttu-id="9c389-230">相關主題</span><span class="sxs-lookup"><span data-stu-id="9c389-230">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="9c389-231">開發 WMI 提供者</span><span class="sxs-lookup"><span data-stu-id="9c389-231">Developing a WMI Provider</span></span>](developing-a-wmi-provider.md)
</dt> <dt>

[<span data-ttu-id="9c389-232">設定命名空間安全描述項</span><span class="sxs-lookup"><span data-stu-id="9c389-232">Setting Namepace Security Descriptors</span></span>](setting-namespace-security-descriptors.md)
</dt> <dt>

[<span data-ttu-id="9c389-233">保護您的提供者</span><span class="sxs-lookup"><span data-stu-id="9c389-233">Securing Your Provider</span></span>](securing-your-provider.md)
</dt> </dl>

 

 
