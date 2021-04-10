---
description: 您可以防止未經授權的使用者接收他們不應擁有存取權的事件。
ms.assetid: 59788643-f57d-458f-91ab-26552218523b
ms.tgt_platform: multiple
title: 安全地提供事件
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: d2c92ed1de08dde4891365440f559544a0b26de5
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/08/2021
ms.locfileid: "104194144"
---
# <a name="providing-events-securely"></a><span data-ttu-id="f2415-103">安全地提供事件</span><span class="sxs-lookup"><span data-stu-id="f2415-103">Providing Events Securely</span></span>

<span data-ttu-id="f2415-104">您可以防止未經授權的使用者接收他們不應擁有存取權的事件。</span><span class="sxs-lookup"><span data-stu-id="f2415-104">You can prevent unauthorized users from receiving events to which they should not have access.</span></span> <span data-ttu-id="f2415-105">您的事件提供者可以提供自己事件類別的實例，就像 [系統登錄提供者](/previous-versions/windows/desktop/regprov/system-registry-provider) 提供 [**RegistryKeyChangeEvent**](/previous-versions/windows/desktop/regprov/registrykeychangeevent)等類別一樣。</span><span class="sxs-lookup"><span data-stu-id="f2415-105">Your event provider can supply instances of its own event classes, just as the [System Registry Provider](/previous-versions/windows/desktop/regprov/system-registry-provider) supplies classes such as [**RegistryKeyChangeEvent**](/previous-versions/windows/desktop/regprov/registrykeychangeevent).</span></span> <span data-ttu-id="f2415-106">您的事件提供者也可以傳遞內部事件，例如 [**\_ \_ InstanceCreationEvent**](--instancecreationevent.md)。</span><span class="sxs-lookup"><span data-stu-id="f2415-106">Your event provider can also deliver intrinsic events such as [**\_\_InstanceCreationEvent**](--instancecreationevent.md).</span></span> <span data-ttu-id="f2415-107">如需詳細資訊，請參閱 [撰寫事件提供者](writing-an-event-provider.md)。</span><span class="sxs-lookup"><span data-stu-id="f2415-107">For more information, see [Writing an Event Provider](writing-an-event-provider.md).</span></span>

<span data-ttu-id="f2415-108">事件提供者可以透過下列方式控制事件收件者的存取：</span><span class="sxs-lookup"><span data-stu-id="f2415-108">An event provider can control access to event recipients in the following ways:</span></span>

-   <span data-ttu-id="f2415-109">藉由執行 [**IWbemEventProviderSecurity：： AccessCheck**](/windows/desktop/api/Wbemprov/nn-wbemprov-iwbemeventprovidersecurity) 來使用存取控制是最有效率的方式。</span><span class="sxs-lookup"><span data-stu-id="f2415-109">Using access control by implementing [**IWbemEventProviderSecurity::AccessCheck**](/windows/desktop/api/Wbemprov/nn-wbemprov-iwbemeventprovidersecurity) is the most efficient way.</span></span>

    <span data-ttu-id="f2415-110">此提供者會判斷取用者是否有權接收要求的事件。</span><span class="sxs-lookup"><span data-stu-id="f2415-110">The provider determines whether the consumer has privileges to receive a requested event.</span></span> <span data-ttu-id="f2415-111">如果取用者沒有足夠的許可權可註冊，WMI 會傳回拒絕存取錯誤。</span><span class="sxs-lookup"><span data-stu-id="f2415-111">If the consumer lacks sufficient privileges to register, WMI returns an access denied error.</span></span> <span data-ttu-id="f2415-112">當提供者可以決定誰可以接收事件時，請使用此模式。</span><span class="sxs-lookup"><span data-stu-id="f2415-112">Use this mode when the provider can make the decision about who can receive events.</span></span> <span data-ttu-id="f2415-113">例如，提供者可能會提供安全性相關事件，而且可能會要求取用者具有啟用 **SeSecurityPrivilege** 許可權的系統管理員許可權。</span><span class="sxs-lookup"><span data-stu-id="f2415-113">For example, a provider may supply security related events and can require that the consumer have administrator privileges with the **SeSecurityPrivilege** privilege enabled.</span></span>

-   <span data-ttu-id="f2415-114">在用來引發事件的接收器上執行 [**IWbemEventSink：： SetSinkSecurity**](/windows/desktop/api/Wbemprov/nf-wbemprov-iwbemeventsink-setsinksecurity) ，可讓您在所有傳遞的事件的接收上，將安全描述項 (SD) 。</span><span class="sxs-lookup"><span data-stu-id="f2415-114">Implementing [**IWbemEventSink::SetSinkSecurity**](/windows/desktop/api/Wbemprov/nf-wbemprov-iwbemeventsink-setsinksecurity) on the sink used to raise events allows the setting of a security descriptor (SD) on a sink for all the events passing through.</span></span>

    <span data-ttu-id="f2415-115">WMI 會根據 SD 執行存取檢查。</span><span class="sxs-lookup"><span data-stu-id="f2415-115">WMI performs access checks based on the SD.</span></span> <span data-ttu-id="f2415-116">當提供者無法決定誰可以取用其事件時，請使用此模式，但可以決定特定接收的 SD。</span><span class="sxs-lookup"><span data-stu-id="f2415-116">Use this mode when the provider cannot make the decision regarding who is allowed to consume its events, but can decide on an SD for a specific sink.</span></span> <span data-ttu-id="f2415-117">例如，如果您的事件提供者藉由呼叫 [**IWbemEventSink：： GetRestrictedSink**](/windows/desktop/api/Wbemprov/nf-wbemprov-iwbemeventsink-getrestrictedsink)取得數個接收器，且您想要每個接收的安全描述項，請使用 [**IWbemEventSink：： SetSinkSecurity**](/windows/desktop/api/Wbemprov/nf-wbemprov-iwbemeventsink-setsinksecurity) 。</span><span class="sxs-lookup"><span data-stu-id="f2415-117">For example, use [**IWbemEventSink::SetSinkSecurity**](/windows/desktop/api/Wbemprov/nf-wbemprov-iwbemeventsink-setsinksecurity) if your event provider obtained several sinks by calls to [**IWbemEventSink::GetRestrictedSink**](/windows/desktop/api/Wbemprov/nf-wbemprov-iwbemeventsink-getrestrictedsink) and you want a security descriptor for each sink.</span></span>

-   <span data-ttu-id="f2415-118">設定事件的 **安全 \_ 描述項** 屬性，可讓您設定每個事件的 SD。</span><span class="sxs-lookup"><span data-stu-id="f2415-118">Setting the **SECURITY\_DESCRIPTOR** property of an event allows for the setting of an SD for each event.</span></span>

    <span data-ttu-id="f2415-119">當傳遞至接收的每個事件都可以有不同的安全描述項時，請使用此方法。</span><span class="sxs-lookup"><span data-stu-id="f2415-119">Use this approach when each event delivered to the sink can have different security descriptors.</span></span> <span data-ttu-id="f2415-120">若要使用此方法，請從 [**\_ \_ 事件**](--event.md)或 [**\_ \_ ExtrinsicEvent**](--extrinsicevent.md)衍生提供者所定義的任何外建事件類別，讓您的類別包含 **安全 \_ 描述項** 屬性。</span><span class="sxs-lookup"><span data-stu-id="f2415-120">To use this approach, derive any of the extrinsic event classes defined by your provider from [**\_\_Event**](--event.md) or [**\_\_ExtrinsicEvent**](--extrinsicevent.md) so that your class contains the **SECURITY\_DESCRIPTOR** property.</span></span> <span data-ttu-id="f2415-121">例如，您的事件提供者可能會透過接收來發行安全和一般事件。</span><span class="sxs-lookup"><span data-stu-id="f2415-121">For example, your event provider may publish both secure and normal events through a sink.</span></span> <span data-ttu-id="f2415-122">在此情況下，請使用系統管理員帳戶安全描述項進行安全事件，並針對可供任何人接收的一般事件使用 **Null** 安全描述項。</span><span class="sxs-lookup"><span data-stu-id="f2415-122">In this case, use the Administrators account security descriptor for secure events and a **NULL** security descriptor for normal events that can be received by anyone.</span></span>

## <a name="securing-events-by-decoupled-event-providers"></a><span data-ttu-id="f2415-123">藉由分離事件提供者來保護事件</span><span class="sxs-lookup"><span data-stu-id="f2415-123">Securing Events by Decoupled Event Providers</span></span>

<span data-ttu-id="f2415-124">分離的事件提供者與 nondecoupled 事件提供者在向 WMI 註冊的方式不同。</span><span class="sxs-lookup"><span data-stu-id="f2415-124">Decoupled event providers differ from nondecoupled event providers in the way that they register with WMI.</span></span> <span data-ttu-id="f2415-125">從低耦合提供者的事件呼叫 [**IWbemEventProviderSecurity：： AccessCheck**](/windows/desktop/api/Wbemprov/nf-wbemprov-iwbemeventprovidersecurity-accesscheck) 絕不會傳播用戶端存取權杖。</span><span class="sxs-lookup"><span data-stu-id="f2415-125">The call to [**IWbemEventProviderSecurity::AccessCheck**](/windows/desktop/api/Wbemprov/nf-wbemprov-iwbemeventprovidersecurity-accesscheck) for events from a decoupled provider never propagates the client access token.</span></span> <span data-ttu-id="f2415-126">WMI 會以與 nondecoupled 事件提供者相同的方式來處理存取控制。</span><span class="sxs-lookup"><span data-stu-id="f2415-126">WMI handles the access control in the same manner as for nondecoupled event providers.</span></span> <span data-ttu-id="f2415-127">如需有關撰寫低耦合提供者的詳細資訊，請參閱 [將提供者併入應用程式](incorporating-a-provider-in-an-application.md)。</span><span class="sxs-lookup"><span data-stu-id="f2415-127">For more information about writing a decoupled provider, see [Incorporating a Provider in an Application](incorporating-a-provider-in-an-application.md).</span></span>

<span data-ttu-id="f2415-128">只有在 **主控台** 的 **WMI 控制** 中設定 **完整 \_ 寫入** 許可權的系統管理員，才可以引發命名空間的事件。</span><span class="sxs-lookup"><span data-stu-id="f2415-128">Only administrators with the **FULL\_WRITE** privilege set in **WMI Control** of the **Control Panel** are allowed to raise events for a namespace.</span></span> <span data-ttu-id="f2415-129">如需詳細資訊，請參閱 [使用 WMI 控制項設定命名空間安全性](setting-namespace-security-with-the-wmi-control.md)。</span><span class="sxs-lookup"><span data-stu-id="f2415-129">For more information, see [Setting Namespace Security with the WMI Control](setting-namespace-security-with-the-wmi-control.md).</span></span>

## <a name="related-topics"></a><span data-ttu-id="f2415-130">相關主題</span><span class="sxs-lookup"><span data-stu-id="f2415-130">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="f2415-131">保護 WMI 事件</span><span class="sxs-lookup"><span data-stu-id="f2415-131">Securing WMI Events</span></span>](securing-wmi-events.md)
</dt> </dl>

 

 
