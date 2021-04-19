---
description: 暫時和永久取用者具有不同的方法來保護事件傳遞。
ms.assetid: cd02e5db-f9e2-438b-9632-0a1387a6d4e3
ms.tgt_platform: multiple
title: 安全地接收事件
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: f27d156213553ee17a346d780cbea0ff82beca83
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/08/2021
ms.locfileid: "106987239"
---
# <a name="receiving-events-securely"></a><span data-ttu-id="8dcc9-103">安全地接收事件</span><span class="sxs-lookup"><span data-stu-id="8dcc9-103">Receiving Events Securely</span></span>

<span data-ttu-id="8dcc9-104">暫時和永久取用者具有不同的方法來保護事件傳遞。</span><span class="sxs-lookup"><span data-stu-id="8dcc9-104">Temporary and permanent consumers have different methods of securing event delivery.</span></span>

<span data-ttu-id="8dcc9-105">本主題將討論下列各節：</span><span class="sxs-lookup"><span data-stu-id="8dcc9-105">The following sections are discussed in this topic:</span></span>

-   [<span data-ttu-id="8dcc9-106">保護暫時性取用者</span><span class="sxs-lookup"><span data-stu-id="8dcc9-106">Securing Temporary Consumers</span></span>](#securing-temporary-consumers)
-   [<span data-ttu-id="8dcc9-107">保障永久消費者的安全</span><span class="sxs-lookup"><span data-stu-id="8dcc9-107">Securing Permanent Consumers</span></span>](#securing-permanent-consumers)
-   [<span data-ttu-id="8dcc9-108">保護永久訂用帳戶</span><span class="sxs-lookup"><span data-stu-id="8dcc9-108">Securing the Permanent Subscription</span></span>](#securing-the-permanent-subscription)
-   [<span data-ttu-id="8dcc9-109">設定 Administrator-Only SD</span><span class="sxs-lookup"><span data-stu-id="8dcc9-109">Setting an Administrator-Only SD</span></span>](#setting-an-administrator-only-sd)
-   [<span data-ttu-id="8dcc9-110">模擬事件提供者身分識別</span><span class="sxs-lookup"><span data-stu-id="8dcc9-110">Impersonating the Event Provider Identity</span></span>](#impersonating-the-event-provider-identity)
-   [<span data-ttu-id="8dcc9-111">Sid 和永久訂閱</span><span class="sxs-lookup"><span data-stu-id="8dcc9-111">SIDs and Permanent Subscriptions</span></span>](#sids-and-permanent-subscriptions)
-   [<span data-ttu-id="8dcc9-112">使用網域帳戶建立永久訂閱</span><span class="sxs-lookup"><span data-stu-id="8dcc9-112">Creating Permanent Subscriptions Using Domain Accounts</span></span>](#creating-permanent-subscriptions-using-domain-accounts)
-   [<span data-ttu-id="8dcc9-113">相關主題</span><span class="sxs-lookup"><span data-stu-id="8dcc9-113">Related topics</span></span>](#related-topics)

## <a name="securing-temporary-consumers"></a><span data-ttu-id="8dcc9-114">保護暫時性取用者</span><span class="sxs-lookup"><span data-stu-id="8dcc9-114">Securing Temporary Consumers</span></span>

<span data-ttu-id="8dcc9-115">暫時的取用 [*者*](gloss-t.md) 會執行，直到系統重新開機或 WMI 已停止，但在引發特定事件時無法啟動。</span><span class="sxs-lookup"><span data-stu-id="8dcc9-115">A [*temporary consumers*](gloss-t.md) runs until the system is rebooted or WMI is stopped but cannot be started if a specific event is raised.</span></span> <span data-ttu-id="8dcc9-116">例如，對 [**SWbemServices.ExecNotificationQueryAsync**](swbemservices-execnotificationqueryasync.md) 的呼叫會建立暫時的取用者。</span><span class="sxs-lookup"><span data-stu-id="8dcc9-116">For example, a call to [**SWbemServices.ExecNotificationQueryAsync**](swbemservices-execnotificationqueryasync.md) creates a temporary consumer.</span></span>

<span data-ttu-id="8dcc9-117">[**SWbemServices.ExecNotificationQuery**](swbemservices-execnotificationquery.md)或 [**IWbemServices：： ExecNotificationQuery**](/windows/desktop/api/WbemCli/nf-wbemcli-iwbemservices-execnotificationquery)的呼叫會建立暫存事件取用者。</span><span class="sxs-lookup"><span data-stu-id="8dcc9-117">The calls [**SWbemServices.ExecNotificationQuery**](swbemservices-execnotificationquery.md) or [**IWbemServices::ExecNotificationQuery**](/windows/desktop/api/WbemCli/nf-wbemcli-iwbemservices-execnotificationquery) create temporary event consumers.</span></span> <span data-ttu-id="8dcc9-118">暫時取用者無法控制誰將事件提供給他們所建立的事件 [*接收*](gloss-s.md) 。</span><span class="sxs-lookup"><span data-stu-id="8dcc9-118">Temporary consumers cannot control who provides events to the event [*sink*](gloss-s.md) they create.</span></span>

<span data-ttu-id="8dcc9-119">[**ExecNotificationQuery**](swbemservices-execnotificationquery.md)方法的呼叫可以同步、[*半同步方式*](gloss-s.md)或非同步方式進行。</span><span class="sxs-lookup"><span data-stu-id="8dcc9-119">Calls to [**ExecNotificationQuery**](swbemservices-execnotificationquery.md) methods can be made synchronously, [*semisynchronously*](gloss-s.md), or asynchronously.</span></span> <span data-ttu-id="8dcc9-120">例如，根據 *iflags* 參數的設定方式而定， [**SWbemServices.ExecNotificationQuery**](swbemservices-execnotificationquery.md)是可呼叫半同步方式的同步方法。</span><span class="sxs-lookup"><span data-stu-id="8dcc9-120">For example, [**SWbemServices.ExecNotificationQuery**](swbemservices-execnotificationquery.md) is a synchronous method that can be called semisynchronously, depending on how the *iflags* parameter is set.</span></span> <span data-ttu-id="8dcc9-121">[**SWbemServices.ExecNotificationQueryAsync**](swbemservices-execnotificationqueryasync.md) 是非同步呼叫。</span><span class="sxs-lookup"><span data-stu-id="8dcc9-121">[**SWbemServices.ExecNotificationQueryAsync**](swbemservices-execnotificationqueryasync.md) is an asynchronous call.</span></span>

<span data-ttu-id="8dcc9-122">請注意，針對這些呼叫的非同步版本，其接收的回呼可能不會在與腳本呼叫相同的驗證層級傳回。</span><span class="sxs-lookup"><span data-stu-id="8dcc9-122">Be aware that the callback to the sink for the asynchronous versions of these calls might not be returned at the same authentication level as the call the script made.</span></span> <span data-ttu-id="8dcc9-123">因此，建議您使用半同步，而不是非同步呼叫。</span><span class="sxs-lookup"><span data-stu-id="8dcc9-123">Therefore, it is recommended that you use semisynchronous instead of asynchronous calls.</span></span> <span data-ttu-id="8dcc9-124">如果您需要非同步通訊，請參閱 [呼叫方法](calling-a-method.md) 並 [在非同步呼叫上設定安全性](setting-security-on-an-asynchronous-call.md)。</span><span class="sxs-lookup"><span data-stu-id="8dcc9-124">If you require asynchronous communication, see [Calling a Method](calling-a-method.md) and [Setting Security on an Asynchronous Call](setting-security-on-an-asynchronous-call.md).</span></span>

<span data-ttu-id="8dcc9-125">腳本訂閱者無法檢查事件提供者的存取權限，以提供事件給腳本所建立的接收。</span><span class="sxs-lookup"><span data-stu-id="8dcc9-125">Scripting subscribers cannot check the access rights of an event provider to provide events to the sink created by the script.</span></span> <span data-ttu-id="8dcc9-126">因此，建議 [**SWbemServices.ExecNotificationQuery**](swbemservices-execnotificationquery.md) 的呼叫會使用呼叫的半值形式，並使用特定的安全性設定。</span><span class="sxs-lookup"><span data-stu-id="8dcc9-126">Therefore, it is recommended that calls to [**SWbemServices.ExecNotificationQuery**](swbemservices-execnotificationquery.md) use the semisynchronous form of the call and use specific security settings.</span></span> <span data-ttu-id="8dcc9-127">如需詳細資訊，請參閱 [使用 VBScript 進行半同步呼叫](making-a-semisynchronous-call-with-vbscript.md)。</span><span class="sxs-lookup"><span data-stu-id="8dcc9-127">For more information, see [Making a Semisynchronous Call with VBScript](making-a-semisynchronous-call-with-vbscript.md).</span></span>

## <a name="securing-permanent-consumers"></a><span data-ttu-id="8dcc9-128">保障永久消費者的安全</span><span class="sxs-lookup"><span data-stu-id="8dcc9-128">Securing Permanent Consumers</span></span>

<span data-ttu-id="8dcc9-129">[*永久取用者*](gloss-p.md)具有從事件提供者的事件永久訂用帳戶，該事件提供者會在作業系統重新開機後保存。</span><span class="sxs-lookup"><span data-stu-id="8dcc9-129">A [*permanent consumers*](gloss-p.md) has a permanent subscription to events from an event provider that will persist after the operating system is restarted.</span></span> <span data-ttu-id="8dcc9-130">支援永久取用者的事件提供者是 [*事件*](gloss-e.md)取用者。</span><span class="sxs-lookup"><span data-stu-id="8dcc9-130">An event provider that supports permanent consumers is a [*event consumer provider*](gloss-e.md).</span></span> <span data-ttu-id="8dcc9-131">如果事件發生時，事件提供者未執行，則 WMI 會在需要傳遞事件時啟動提供者。</span><span class="sxs-lookup"><span data-stu-id="8dcc9-131">If the event provider is not running when an event occurs, then WMI starts the provider when it needs to deliver events.</span></span> <span data-ttu-id="8dcc9-132">WMI 會根據 [**\_ \_ EventConsumerProviderRegistration**](--eventconsumerproviderregistration.md)實例識別要傳遞事件的取用者提供者，這會將取用者提供者 [**\_ \_ Win32Provider**](--win32provider.md)實例與取用者提供者所定義的 [*邏輯取用者類別*](gloss-l.md)產生關聯。</span><span class="sxs-lookup"><span data-stu-id="8dcc9-132">WMI identifies which consumer provider the events should be delivered to, based on the [**\_\_EventConsumerProviderRegistration**](--eventconsumerproviderregistration.md) instance, which associates the consumer provider [**\_\_Win32Provider**](--win32provider.md) instance with a [*logical consumer class*](gloss-l.md) defined by the consumer provider.</span></span> <span data-ttu-id="8dcc9-133">如需取用者提供者角色的詳細資訊，請參閱 [撰寫事件](writing-an-event-consumer-provider.md)取用者提供者。</span><span class="sxs-lookup"><span data-stu-id="8dcc9-133">For more information about the role of consumer providers, see [Writing an Event Consumer Provider](writing-an-event-consumer-provider.md).</span></span>

<span data-ttu-id="8dcc9-134">永久取用者可以控制傳送事件的物件，而事件提供者可以控制誰存取其事件。</span><span class="sxs-lookup"><span data-stu-id="8dcc9-134">Permanent consumers can control who sends them events and event providers can control who accesses their events.</span></span>

<span data-ttu-id="8dcc9-135">用戶端腳本和應用程式會在訂用帳戶中建立邏輯取用者類別的實例。</span><span class="sxs-lookup"><span data-stu-id="8dcc9-135">Client scripts and applications create instances of the logical consumer class as part of a subscription.</span></span> <span data-ttu-id="8dcc9-136">邏輯取用者類別會定義事件所包含的資訊、用戶端可如何處理事件，以及事件的傳遞方式。</span><span class="sxs-lookup"><span data-stu-id="8dcc9-136">The logical consumer class defines what information the event contains, what the client can do with the event, and how the event is delivered.</span></span>

<span data-ttu-id="8dcc9-137">WMI [標準取用者類別](standard-consumer-classes.md) 提供邏輯取用者類別角色的範例。</span><span class="sxs-lookup"><span data-stu-id="8dcc9-137">The WMI [Standard Consumer Classes](standard-consumer-classes.md) provide examples of the role of logical consumer classes.</span></span> <span data-ttu-id="8dcc9-138">如需詳細資訊，請參閱 [使用標準取用者監視及回應事件](monitoring-and-responding-to-events-with-standard-consumers.md)。</span><span class="sxs-lookup"><span data-stu-id="8dcc9-138">For more information, see [Monitoring and Responding to Events with Standard Consumers](monitoring-and-responding-to-events-with-standard-consumers.md).</span></span>

## <a name="securing-the-permanent-subscription"></a><span data-ttu-id="8dcc9-139">保護永久訂用帳戶</span><span class="sxs-lookup"><span data-stu-id="8dcc9-139">Securing the Permanent Subscription</span></span>

<span data-ttu-id="8dcc9-140">永久訂用帳戶有可能會導致 WMI 中的安全性問題，因此有下列安全性需求：</span><span class="sxs-lookup"><span data-stu-id="8dcc9-140">Permanent subscriptions have greater potential to cause security problems in WMI and therefore have the following security requirements:</span></span>

-   <span data-ttu-id="8dcc9-141">邏輯取用者實例、 [**\_ \_ >eventfilter**](--eventfilter.md)和 [**\_ \_ FilterToConsumerBinding**](--filtertoconsumerbinding.md)實例必須在 **CreatorSID** 屬性中擁有相同的個別安全識別碼 (SID) 。</span><span class="sxs-lookup"><span data-stu-id="8dcc9-141">The logical consumer instance, the [**\_\_EventFilter**](--eventfilter.md), and the [**\_\_FilterToConsumerBinding**](--filtertoconsumerbinding.md) instances must have the same individual security identifier (SID) in the **CreatorSID** property.</span></span> <span data-ttu-id="8dcc9-142">如需詳細資訊，請參閱 [在永久訂用帳戶的所有實例中保留相同的 SID](#sids-and-permanent-subscriptions)。</span><span class="sxs-lookup"><span data-stu-id="8dcc9-142">For more information, see [Keeping the same SID in all instances of a permanent subscription](#sids-and-permanent-subscriptions).</span></span>
-   <span data-ttu-id="8dcc9-143">建立訂用帳戶的帳戶必須是具有本機系統管理員許可權的網域帳戶或本機系統管理員群組帳戶。</span><span class="sxs-lookup"><span data-stu-id="8dcc9-143">The account that creates the subscription must be either a domain account with local administrator privileges or the local Administrators group account.</span></span> <span data-ttu-id="8dcc9-144">使用系統管理員群組 SID 可讓訂用帳戶在本機電腦上繼續運作，即使它已與網路中斷連線也一樣。</span><span class="sxs-lookup"><span data-stu-id="8dcc9-144">Using the Administrators group SID allows the subscription to continue to work on the local computer, even if it is disconnected from the network.</span></span> <span data-ttu-id="8dcc9-145">使用網域帳戶可讓使用者進行確切的識別。</span><span class="sxs-lookup"><span data-stu-id="8dcc9-145">Using a domain account allows exact identification of the user.</span></span>

    <span data-ttu-id="8dcc9-146">但是，如果電腦未連線，而且建立帳戶是網域帳戶，則取用者會失敗，因為 WMI 無法驗證帳戶的身分識別。</span><span class="sxs-lookup"><span data-stu-id="8dcc9-146">However, if the computer is not connected and the creating account is a domain account, the consumer fails because WMI cannot verify the identity of the account.</span></span> <span data-ttu-id="8dcc9-147">若要避免訂用帳戶在電腦與網路中斷連線時失敗，請使用訂用帳戶的系統管理員群組 SID。</span><span class="sxs-lookup"><span data-stu-id="8dcc9-147">To avoid subscription failure if the computer is disconnected from the network, use the Administrators group SID for a subscription.</span></span> <span data-ttu-id="8dcc9-148">在此情況下，您應該確定 LocalSystem 帳戶可以存取網域上的群組成員資格資料。</span><span class="sxs-lookup"><span data-stu-id="8dcc9-148">In this case, you should ensure that the LocalSystem account can access group membership data on the domain.</span></span> <span data-ttu-id="8dcc9-149">某些事件取用者提供者有特別高的安全性需求，因為 rogue 訂用帳戶可能會造成很大的損害。</span><span class="sxs-lookup"><span data-stu-id="8dcc9-149">Some event consumer providers have particularly high security requirements, since a rogue subscription can cause great damage.</span></span> <span data-ttu-id="8dcc9-150">例如，標準取用者 [**ActiveScriptEventConsumer**](activescripteventconsumer.md) 和 [**CommandLineEventConsumer**](commandlineeventconsumer.md)。</span><span class="sxs-lookup"><span data-stu-id="8dcc9-150">Examples are the standard consumers, [**ActiveScriptEventConsumer**](activescripteventconsumer.md) and [**CommandLineEventConsumer**](commandlineeventconsumer.md).</span></span>

-   <span data-ttu-id="8dcc9-151">您可以設定永久訂用帳戶，只接受來自特定事件提供者身分識別的事件。</span><span class="sxs-lookup"><span data-stu-id="8dcc9-151">You can configure the permanent subscription to only accept events from specific event provider identities.</span></span> <span data-ttu-id="8dcc9-152">將 [**\_ \_ >eventfilter**](--eventfilter.md)實例之 **EventAccess** 屬性中的安全描述項設定為事件提供者身分識別。</span><span class="sxs-lookup"><span data-stu-id="8dcc9-152">Set the security descriptor in the **EventAccess** property of the [**\_\_EventFilter**](--eventfilter.md) instance to the event provider identities.</span></span> <span data-ttu-id="8dcc9-153">WMI 會將事件提供者的身分識別與安全描述項進行比較，以判斷提供者是否有 **WBEM \_ 正確的 \_ 發行** 存取權。</span><span class="sxs-lookup"><span data-stu-id="8dcc9-153">WMI compares the identity of the event provider to the security descriptor to determine if the provider has **WBEM\_RIGHT\_PUBLISH** access.</span></span> <span data-ttu-id="8dcc9-154">如需詳細資訊，請參閱 [WMI 安全性常數](wmi-security-constants.md)。</span><span class="sxs-lookup"><span data-stu-id="8dcc9-154">For more information, see [WMI Security Constants](wmi-security-constants.md).</span></span>

    <span data-ttu-id="8dcc9-155">如果篩選準則允許存取事件提供者身分識別，則它也會信任事件。</span><span class="sxs-lookup"><span data-stu-id="8dcc9-155">If the filter allows access to the event provider identity, then it also trusts the event.</span></span> <span data-ttu-id="8dcc9-156">這可讓接收事件的取用者引發委派的事件。</span><span class="sxs-lookup"><span data-stu-id="8dcc9-156">This allows the consumer that received the event to raise a delegated event.</span></span>

    <span data-ttu-id="8dcc9-157">**注意** **EventAccess** 中安全描述項的預設值是 **Null**，可允許存取所有人。</span><span class="sxs-lookup"><span data-stu-id="8dcc9-157">**Note**  The default for the security descriptor in **EventAccess** is **NULL**, which allows access to everyone.</span></span> <span data-ttu-id="8dcc9-158">建議您限制 [**\_ \_ >eventfilter**](--eventfilter.md)訂閱實例中的存取，以取得更好的事件安全性。</span><span class="sxs-lookup"><span data-stu-id="8dcc9-158">Limiting access in the subscription instance of [**\_\_EventFilter**](--eventfilter.md) is recommended for better event security.</span></span>

## <a name="setting-an-administrator-only-sd"></a><span data-ttu-id="8dcc9-159">設定 Administrator-Only SD</span><span class="sxs-lookup"><span data-stu-id="8dcc9-159">Setting an Administrator-Only SD</span></span>

<span data-ttu-id="8dcc9-160">下列 c + + 程式碼範例會在 [**\_ \_ >eventfilter**](--eventfilter.md)實例上建立僅限系統管理員的安全描述項。</span><span class="sxs-lookup"><span data-stu-id="8dcc9-160">The following C++ code example creates an administrator-only security descriptor on the [**\_\_EventFilter**](--eventfilter.md) instance.</span></span> <span data-ttu-id="8dcc9-161">此範例會使用 [安全描述項定義語言](/windows/desktop/SecAuthZ/security-descriptor-definition-language) (SDDL) 來建立安全描述項。</span><span class="sxs-lookup"><span data-stu-id="8dcc9-161">This example creates the security descriptor using [Security Descriptor Definition Language](/windows/desktop/SecAuthZ/security-descriptor-definition-language) (SDDL).</span></span> <span data-ttu-id="8dcc9-162">如需有關 **WBEM \_ 正確 \_ 訂閱** 的詳細資訊，請參閱 [WMI 安全性常數](wmi-security-constants.md)。</span><span class="sxs-lookup"><span data-stu-id="8dcc9-162">For more information about **WBEM\_RIGHT\_SUBSCRIBE**, see [WMI Security Constants](wmi-security-constants.md).</span></span>


```C++
// Create SD that allows only administrators 
//    to send events to this filter. 
// The SDDL settings are O:BAG:BAD:(A;;0x80;;;BA)
// Set the EventAccess property in the 
//    IWbemClassObject of the __EventFilter instance. 
   long lMask = WBEM_RIGHT_PUBLISH;
     WCHAR wBuf[MAX_PATH];
     _ltow( lMask, wBuf, 16 );
 
HRESULT hRes = pEventFilterInstance->Put( L"EventAccess", 0,
    &_variant_t( L"O:BAG:BAD:(A;;0x80;;;BA)" ), NULL );
```



<span data-ttu-id="8dcc9-163">上述程式碼範例需要下列參考和 \# include 語句。</span><span class="sxs-lookup"><span data-stu-id="8dcc9-163">The previous code example requires the following reference and \#include statements.</span></span>


```C++
#define _WIN32_DCOM
#include <wbemidl.h>
#include <comdef.h>

#pragma comment(lib, "wbemuuid.lib")
```



## <a name="impersonating-the-event-provider-identity"></a><span data-ttu-id="8dcc9-164">模擬事件提供者身分識別</span><span class="sxs-lookup"><span data-stu-id="8dcc9-164">Impersonating the Event Provider Identity</span></span>

<span data-ttu-id="8dcc9-165">永久取用者可能需要模擬事件提供者來處理事件。</span><span class="sxs-lookup"><span data-stu-id="8dcc9-165">A permanent consumer may need to impersonate the event provider to process the event.</span></span> <span data-ttu-id="8dcc9-166">當下列條件存在時，永久取用者只能模擬事件提供者：</span><span class="sxs-lookup"><span data-stu-id="8dcc9-166">Permanent consumers can only impersonate the event provider when the following conditions exist:</span></span>

-   <span data-ttu-id="8dcc9-167">[**\_ \_ FilterToConsumerBinding**](--filtertoconsumerbinding.md)的實例的 **MaintainSecurityCoNtext** 屬性設定為 **True**。</span><span class="sxs-lookup"><span data-stu-id="8dcc9-167">The instance of [**\_\_FilterToConsumerBinding**](--filtertoconsumerbinding.md) has the **MaintainSecurityContext** property set to **True**.</span></span>
-   <span data-ttu-id="8dcc9-168">事件會在產生事件時，在提供者所在的相同安全性內容中傳遞。</span><span class="sxs-lookup"><span data-stu-id="8dcc9-168">An event is delivered in the same security context that the provider was in when it generated the event.</span></span> <span data-ttu-id="8dcc9-169">只有實作為 DLL 的取用者（同進程取用者）可以在提供者的安全性內容中接收事件。</span><span class="sxs-lookup"><span data-stu-id="8dcc9-169">Only a consumer implemented as a DLL, an in-process consumer, can receive events in the security context of the provider.</span></span> <span data-ttu-id="8dcc9-170">如需有關同進程提供者和取用者安全性的詳細資訊，請參閱 [提供者裝載和安全性](provider-hosting-and-security.md)。</span><span class="sxs-lookup"><span data-stu-id="8dcc9-170">For more information about security of in-process providers and consumers, see [Provider Hosting and Security](provider-hosting-and-security.md).</span></span>
-   <span data-ttu-id="8dcc9-171">事件提供者正在允許模擬的進程中執行。</span><span class="sxs-lookup"><span data-stu-id="8dcc9-171">The event provider is running in a process that allows impersonation.</span></span>

<span data-ttu-id="8dcc9-172">執行取用者進程的帳戶必須具有 WMI 儲存機制的 **完整 \_ 寫入** 許可權 (也稱為 CIM 存放庫) 。</span><span class="sxs-lookup"><span data-stu-id="8dcc9-172">The account running the consumer process must have **FULL\_WRITE** access to the WMI repository (also known as the CIM repository).</span></span> <span data-ttu-id="8dcc9-173">在訂用帳戶中， [**\_ \_ FilterToConsumerBinding**](--filtertoconsumerbinding.md)、 [**\_ \_ EventConsumer**](--eventconsumer.md)和 [**\_ \_ >eventfilter**](--eventfilter.md)實例的 **CreatorSID** 屬性中必須有相同的個別安全識別碼 (SID) 值。</span><span class="sxs-lookup"><span data-stu-id="8dcc9-173">In the subscription, the [**\_\_FilterToConsumerBinding**](--filtertoconsumerbinding.md), [**\_\_EventConsumer**](--eventconsumer.md), and [**\_\_EventFilter**](--eventfilter.md) instances must have the same individual security identifier (SID) value in the **CreatorSID** property.</span></span> <span data-ttu-id="8dcc9-174">WMI 會將 SID 儲存在每個實例的 **CreatorSID** 中。</span><span class="sxs-lookup"><span data-stu-id="8dcc9-174">WMI stores the SID in the **CreatorSID** for each instance.</span></span>

## <a name="sids-and-permanent-subscriptions"></a><span data-ttu-id="8dcc9-175">Sid 和永久訂閱</span><span class="sxs-lookup"><span data-stu-id="8dcc9-175">SIDs and Permanent Subscriptions</span></span>

<span data-ttu-id="8dcc9-176">當系結、取用者和篩選準則不是由相同的使用者建立時，永久訂閱無法運作，這表示 [**\_ \_ FilterToConsumerBinding**](--filtertoconsumerbinding.md)、 [**\_ \_ EventConsumer**](--eventconsumer.md)和 [**\_ \_ >eventfilter**](--eventfilter.md)在 **CreatorSID** 屬性中必須有相同的個別安全識別碼 (SID) 值。</span><span class="sxs-lookup"><span data-stu-id="8dcc9-176">A permanent subscription does not work when the binding, the consumer, and the filter are not created by the same user, which means that the [**\_\_FilterToConsumerBinding**](--filtertoconsumerbinding.md), [**\_\_EventConsumer**](--eventconsumer.md), and [**\_\_EventFilter**](--eventfilter.md) must have the same individual security identifier (SID) value in the **CreatorSID** property.</span></span> <span data-ttu-id="8dcc9-177">Windows Management Instrumentation (WMI) 儲存此值。</span><span class="sxs-lookup"><span data-stu-id="8dcc9-177">Windows Management Instrumentation (WMI) stores this value.</span></span>

## <a name="creating-permanent-subscriptions-using-domain-accounts"></a><span data-ttu-id="8dcc9-178">使用網域帳戶建立永久訂閱</span><span class="sxs-lookup"><span data-stu-id="8dcc9-178">Creating Permanent Subscriptions Using Domain Accounts</span></span>

<span data-ttu-id="8dcc9-179">使用網域帳戶來建立永久訂閱時，必須考慮幾個問題。</span><span class="sxs-lookup"><span data-stu-id="8dcc9-179">Several issues must be considered when using domain accounts to create permanent subscriptions.</span></span> <span data-ttu-id="8dcc9-180">每個永久訂用帳戶在沒有使用者登入時仍可運作，這表示他們在內建的 LocalSystem 帳戶下運作。</span><span class="sxs-lookup"><span data-stu-id="8dcc9-180">Every permanent subscription should still work when no user is logged on, which means they function under the built-in LocalSystem account.</span></span>

<span data-ttu-id="8dcc9-181">如果網域使用者是安全機密取用者的永久訂用帳戶建立者 ([**ActiveScriptEventConsumer**](activescripteventconsumer.md)、 [**CommandLineEventConsumer**](commandlineeventconsumer.md)) ，則 WMI 會驗證 [**\_ \_ >eventfilter**](--eventfilter.md)類別、 [**\_ \_ FilterToConsumerBinding**](--filtertoconsumerbinding.md)類別和取用者實例的 **CreatorSID** 屬性是否屬於本機 Administrators 群組成員的使用者。</span><span class="sxs-lookup"><span data-stu-id="8dcc9-181">If a domain user is the creator of a permanent subscription for security sensitive consumers ([**ActiveScriptEventConsumer**](activescripteventconsumer.md), [**CommandLineEventConsumer**](commandlineeventconsumer.md)), then WMI verifies whether the **CreatorSID** property of the [**\_\_EventFilter**](--eventfilter.md) class, [**\_\_FilterToConsumerBinding**](--filtertoconsumerbinding.md) class, and the consumer instances belong to a user who is member of local Administrators group.</span></span>

<span data-ttu-id="8dcc9-182">下列程式碼範例會顯示如何指定 **CreatorSID** 屬性。</span><span class="sxs-lookup"><span data-stu-id="8dcc9-182">The following code example shows how you can specify the **CreatorSID** property.</span></span>

``` syntax
 instance of __EventFilter as $FILTER
    {
        // this is the Administrators SID in array of bytes format
        CreatorSID = {1,2,0,0,0,0,0,5,32,0,0,0,32,2,0,0};    
        // Add filter code here ...
    }

    instance of ActiveScriptEventConsumer as $CONSUMER
    {
       CreatorSID = {1,2,0,0,0,0,0,5,32,0,0,0,32,2,0,0};
       // Add consumer code here ...
    }

    instance of __FilterToConsumerBinding
    {
       CreatorSID = {1,2,0,0,0,0,0,5,32,0,0,0,32,2,0,0};
       Consumer = $CONSUMER;
       Filter = $FILTER;
       // Add binding code here ...
    }
```

<span data-ttu-id="8dcc9-183">針對跨網域狀況，請將已驗證的使用者新增至「Windows 授權存取群組」。</span><span class="sxs-lookup"><span data-stu-id="8dcc9-183">For cross domain situations, add Authenticated Users to the "Windows Authorization Access Group".</span></span>

## <a name="related-topics"></a><span data-ttu-id="8dcc9-184">相關主題</span><span class="sxs-lookup"><span data-stu-id="8dcc9-184">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="8dcc9-185">保護 WMI 事件</span><span class="sxs-lookup"><span data-stu-id="8dcc9-185">Securing WMI Events</span></span>](securing-wmi-events.md)
</dt> <dt>

[<span data-ttu-id="8dcc9-186">接收 WMI 事件</span><span class="sxs-lookup"><span data-stu-id="8dcc9-186">Receiving a WMI Event</span></span>](receiving-a-wmi-event.md)
</dt> </dl>

 

 
