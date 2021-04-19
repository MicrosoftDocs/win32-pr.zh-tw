---
description: 指定提供者裝載模型。 設定這個屬性會使提供者載入具有指定許可權層級的共用主機進程中。
ms.assetid: 1e5c778d-cd29-449b-88e2-fe0c90d0edcd
ms.tgt_platform: multiple
title: 提供者裝載和安全性
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: db6b88a5727f34fbb76baf62dcdf0488e5eb9eb7
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/08/2021
ms.locfileid: "106975851"
---
# <a name="provider-hosting-and-security"></a><span data-ttu-id="2e3ce-104">提供者裝載和安全性</span><span class="sxs-lookup"><span data-stu-id="2e3ce-104">Provider Hosting and Security</span></span>

<span data-ttu-id="2e3ce-105">**\_ \_ Win32Provider** 實例中代表提供者的 [**HostingModel**](--win32provider.md)屬性會指定提供者裝載模型。</span><span class="sxs-lookup"><span data-stu-id="2e3ce-105">The [**HostingModel**](--win32provider.md) property in the **\_\_Win32Provider** instance that represents your provider specifies the provider hosting model.</span></span> <span data-ttu-id="2e3ce-106">設定這個屬性會使提供者載入具有指定許可權層級的共用主機進程中。</span><span class="sxs-lookup"><span data-stu-id="2e3ce-106">Setting this property causes the provider to be loaded into a shared host process that has a specified level of privilege.</span></span>

## <a name="shared-provider-host-process"></a><span data-ttu-id="2e3ce-107">共用提供者主機進程</span><span class="sxs-lookup"><span data-stu-id="2e3ce-107">Shared Provider Host Process</span></span>

<span data-ttu-id="2e3ce-108">WMI 位於具有多個其他服務的共用服務主機中。</span><span class="sxs-lookup"><span data-stu-id="2e3ce-108">WMI resides in a shared service host with several other services.</span></span> <span data-ttu-id="2e3ce-109">若要避免在提供者失敗時停止所有服務，提供者會載入名為 "Wmiprvse.exe" 的個別主控制項進程。</span><span class="sxs-lookup"><span data-stu-id="2e3ce-109">To avoid stopping all the services when a provider fails, providers are loaded into a separate host process named "Wmiprvse.exe".</span></span> <span data-ttu-id="2e3ce-110">具有這個名稱的多個進程可以執行。</span><span class="sxs-lookup"><span data-stu-id="2e3ce-110">More than one process with this name can be running.</span></span> <span data-ttu-id="2e3ce-111">每個都可以在具有不同安全性的不同帳戶下執行。</span><span class="sxs-lookup"><span data-stu-id="2e3ce-111">Each can run under a different account with varying security.</span></span> <span data-ttu-id="2e3ce-112">請注意，從 Windows Vista 開始，請使用 [**winmgmt**](winmgmt.md) 命令，在個別的進程中使用固定通訊埠來執行 WMI。</span><span class="sxs-lookup"><span data-stu-id="2e3ce-112">Be aware that, starting with Windows Vista, use the [**winmgmt**](winmgmt.md) command to run WMI in a separate process by itself using a fixed port.</span></span> <span data-ttu-id="2e3ce-113">如需詳細資訊，請參閱 [從 Vista 開始遠端連線到 WMI](connecting-to-wmi-remotely-starting-with-vista.md)。</span><span class="sxs-lookup"><span data-stu-id="2e3ce-113">For more information, see [Connecting to WMI Remotely Starting with Vista](connecting-to-wmi-remotely-starting-with-vista.md).</span></span>

<span data-ttu-id="2e3ce-114">共用主機可以在 Wmiprvse.exe 主機進程中的下列其中一個系統帳戶下執行：</span><span class="sxs-lookup"><span data-stu-id="2e3ce-114">The shared host can run under one of the following system accounts in a Wmiprvse.exe host process:</span></span>

-   [<span data-ttu-id="2e3ce-115">LocalSystem</span><span class="sxs-lookup"><span data-stu-id="2e3ce-115">LocalSystem</span></span>](/windows/desktop/Services/localsystem-account)
-   [<span data-ttu-id="2e3ce-116">NetworkService</span><span class="sxs-lookup"><span data-stu-id="2e3ce-116">NetworkService</span></span>](/windows/desktop/Services/networkservice-account)
-   [<span data-ttu-id="2e3ce-117">LocalService</span><span class="sxs-lookup"><span data-stu-id="2e3ce-117">LocalService</span></span>](/windows/desktop/Services/localservice-account)

<span data-ttu-id="2e3ce-118">提供者也可以是本機 COM 伺服器 ( .exe) 或自我裝載，這不需要 WMI 提供者主機。</span><span class="sxs-lookup"><span data-stu-id="2e3ce-118">A provider can also be a local COM server (.exe), or self-hosted, which does not require a WMI provider host.</span></span>

## <a name="setting-the-hosting-model"></a><span data-ttu-id="2e3ce-119">設定裝載模型</span><span class="sxs-lookup"><span data-stu-id="2e3ce-119">Setting the Hosting Model</span></span>

<span data-ttu-id="2e3ce-120">因為 LocalSystem 是具有特殊許可權的帳戶，所以建議您在 Wmiprvse.exe 進程中執行提供者時，將 [**HostingModel**](--win32provider.md) 設定為 **NetworkServiceHost** 。</span><span class="sxs-lookup"><span data-stu-id="2e3ce-120">Because LocalSystem is a privileged account, it is recommended that you set [**HostingModel**](--win32provider.md) to **NetworkServiceHost** when a provider is running in a Wmiprvse.exe process.</span></span> <span data-ttu-id="2e3ce-121">NetworkServiceHost 帳戶適用于不需要廣泛許可權的服務，但需要從遠端與其他系統通訊。</span><span class="sxs-lookup"><span data-stu-id="2e3ce-121">NetworkServiceHost account is for services that do not require extensive privileges, but do need to communicate remotely with other systems.</span></span>

<span data-ttu-id="2e3ce-122">如果您未設定 [**HostingModel**](--win32provider.md) 屬性的值，WMI 會將預設值設定為 **NetworkServiceHostOrSelfHost**。</span><span class="sxs-lookup"><span data-stu-id="2e3ce-122">If you do not set a value for the [**HostingModel**](--win32provider.md) property, WMI will set a default value of **NetworkServiceHostOrSelfHost**.</span></span> <span data-ttu-id="2e3ce-123">如果 **HostingModel** 值設定為 **LocalSystemHost**，WMI 會使用追蹤，在 Windows 事件記錄檔中產生事件5603和5604。</span><span class="sxs-lookup"><span data-stu-id="2e3ce-123">If the **HostingModel** value is set to **LocalSystemHost**, WMI uses tracing to generate events 5603 and 5604 in the Windows Event Log.</span></span> <span data-ttu-id="2e3ce-124">由於本機 [LocalSystem](/windows/desktop/Services/localsystem-account) 帳戶具有高度許可權，因此不建議使用此設定。</span><span class="sxs-lookup"><span data-stu-id="2e3ce-124">Because the local [LocalSystem](/windows/desktop/Services/localsystem-account) account is highly privileged, this setting is not recommended.</span></span> <span data-ttu-id="2e3ce-125">您可以在 **事件檢視器** 中查看這些事件。</span><span class="sxs-lookup"><span data-stu-id="2e3ce-125">You can view these events in the **Event Viewer**.</span></span> <span data-ttu-id="2e3ce-126">如需詳細資訊，請參閱 [追蹤 WMI 活動](tracing-wmi-activity.md)。</span><span class="sxs-lookup"><span data-stu-id="2e3ce-126">For more information, see [Tracing WMI Activity](tracing-wmi-activity.md).</span></span>

<span data-ttu-id="2e3ce-127">將低耦合提供者的 [**HostingModel**](--win32provider.md) 屬性設定為「分離： Com」。</span><span class="sxs-lookup"><span data-stu-id="2e3ce-127">Set the [**HostingModel**](--win32provider.md) property for decoupled providers as "Decoupled:Com".</span></span> <span data-ttu-id="2e3ce-128">藉 [**由在 .NET Framework 中新增**](/previous-versions//hh872326(v=vs.85)) 檢測類別所建立的提供者是低耦合提供者。</span><span class="sxs-lookup"><span data-stu-id="2e3ce-128">Providers created by adding instrumentation classes from [**Microsoft.Management.Infrastructure**](/previous-versions//hh872326(v=vs.85)) in the .NET Framework are decoupled providers.</span></span> <span data-ttu-id="2e3ce-129">不再 ) 支援 (的 **系統管理。** 如需建立低耦合提供者的詳細資訊，請參閱 [在應用程式中併入提供者](incorporating-a-provider-in-an-application.md)。</span><span class="sxs-lookup"><span data-stu-id="2e3ce-129">(**System.Management.Instrumentation** is no longer supported.) For more information about creating a decoupled provider, see [Incorporating a Provider in an Application](incorporating-a-provider-in-an-application.md).</span></span>

<span data-ttu-id="2e3ce-130">裝載模型是在代表提供者之 **\_ \_ Win32Provider** 實例的 [**HostingModel**](--win32provider.md)屬性中指定。</span><span class="sxs-lookup"><span data-stu-id="2e3ce-130">The hosting model is specified in the [**HostingModel**](--win32provider.md) property in the **\_\_Win32Provider** instance that represents your provider.</span></span>

<span data-ttu-id="2e3ce-131">**設定提供者的裝載模型**</span><span class="sxs-lookup"><span data-stu-id="2e3ce-131">**To set the hosting model for a provider**</span></span>

1.  <span data-ttu-id="2e3ce-132">在定義您提供者的 MOF 檔案中，建立 [**\_ \_ Win32Provider**](--win32provider.md)的實例。</span><span class="sxs-lookup"><span data-stu-id="2e3ce-132">In the MOF file that defines your provider, create an instance of [**\_\_Win32Provider**](--win32provider.md).</span></span>
2.  <span data-ttu-id="2e3ce-133">**將名稱屬性中** 的提供者指派給提供者，並將提供者 COM 物件 (clsid) 的類別識別碼指派給 **CLSID** 屬性。</span><span class="sxs-lookup"><span data-stu-id="2e3ce-133">Assign a name to the provider in the **Name** property and assign the class identifier (CLSID) of the provider COM object to the **Clsid** property.</span></span>

    <span data-ttu-id="2e3ce-134">下列程式碼範例 **會將名稱屬性的** 名稱，以及提供者 COM 物件的 CSLID 指派給 **Clsid** 屬性。</span><span class="sxs-lookup"><span data-stu-id="2e3ce-134">The following code example assigns a name to the **Name** property and the CSLID of the provider COM object to the **Clsid** property.</span></span>

    ``` syntax
    Instance of __Win32Provider as $NewProvider
    {
        Name = "MyProvider";
        Clsid = "{.......}";
    }
    ```

3.  <span data-ttu-id="2e3ce-135">將適當的共用主機值指派給 [**HostingModel**](--win32provider.md) 屬性。</span><span class="sxs-lookup"><span data-stu-id="2e3ce-135">Assign the appropriate shared host value to the [**HostingModel**](--win32provider.md) property.</span></span> <span data-ttu-id="2e3ce-136">共用的主機值（例如 "NetworkServiceHost"）是在 [**MSFT \_ 提供者**](/previous-versions/windows/desktop/wmisystemprov/msft-providers)類別的 **HostingSpecification** 屬性中定義。</span><span class="sxs-lookup"><span data-stu-id="2e3ce-136">Shared host values such as "NetworkServiceHost" are defined in the **HostingSpecification** property of [**MSFT\_Providers**](/previous-versions/windows/desktop/wmisystemprov/msft-providers) class.</span></span>

    <span data-ttu-id="2e3ce-137">下列程式碼範例會將共用主機值指派給 [**HostingModel**](--win32provider.md) 屬性。</span><span class="sxs-lookup"><span data-stu-id="2e3ce-137">The following code example assigns a shared host value to the [**HostingModel**](--win32provider.md) property.</span></span>

    ``` syntax
    HostingModel = "NetworkServiceHost";
    ```

<span data-ttu-id="2e3ce-138">下列程式碼範例顯示如何在 NetworkServiceHost 中註冊提供者。</span><span class="sxs-lookup"><span data-stu-id="2e3ce-138">The following code example shows how to register a provider in NetworkServiceHost.</span></span>

``` syntax
Instance of __Win32Provider as $NewProvider
{
    Name = "MyProvider";
    Clsid = "{.......}";
    HostingModel = "NetworkServiceHost";
}
```

<span data-ttu-id="2e3ce-139">如果您有多個提供者，您可以註冊您的提供者，使其位於特定的實例中，以將它們群組至特定的服務主機。</span><span class="sxs-lookup"><span data-stu-id="2e3ce-139">If you have multiple providers, you can group them into a specific service host by registering your provider so that it resides in the specific instance.</span></span>

<span data-ttu-id="2e3ce-140">下列程式碼範例也會在 NetworkServiceHost 中註冊提供者。</span><span class="sxs-lookup"><span data-stu-id="2e3ce-140">The following code example also registers a provider in NetworkServiceHost.</span></span> <span data-ttu-id="2e3ce-141">[**MSFT \_ 提供者**](/previous-versions/windows/desktop/wmisystemprov/msft-providers)類別會定義兩個合併用來建立 [**\_ \_ Win32Provider**](--win32provider.md) **HostingModel** 屬性之值的值。</span><span class="sxs-lookup"><span data-stu-id="2e3ce-141">The [**MSFT\_Providers**](/previous-versions/windows/desktop/wmisystemprov/msft-providers) class defines values for the two values that combine to create the [**\_\_Win32Provider**](--win32provider.md) **HostingModel** property.</span></span> <span data-ttu-id="2e3ce-142">在此範例中，"NetworkServiceHost" 值來自 **MSFT \_ 提供者** 的 **HostingSpecification** 屬性，而 "LocalServiceHost" 來自 **HostingGroup** 屬性。</span><span class="sxs-lookup"><span data-stu-id="2e3ce-142">In the example, "NetworkServiceHost" value comes from the **HostingSpecification** property of **MSFT\_Providers** and "LocalServiceHost" comes from the **HostingGroup** property.</span></span>

``` syntax
Instance of __Win32Provider as $NewProvider
{
    Name = "MyProvider";
    Clsid = "{.......}";
    HostingModel = "NetworkServiceHost:MySharedHost";
}
```

<span data-ttu-id="2e3ce-143">未分離且裝載于 Wmiprvse 程式中的提供者有特殊開發問題。</span><span class="sxs-lookup"><span data-stu-id="2e3ce-143">Special development issues exist for providers that are not decoupled and are hosted in the Wmiprvse process.</span></span> <span data-ttu-id="2e3ce-144">如需詳細資訊，請參閱 [偵錯工具提供者](debugging-providers.md)。</span><span class="sxs-lookup"><span data-stu-id="2e3ce-144">For more information, see [Debugging Providers](debugging-providers.md).</span></span>

<span data-ttu-id="2e3ce-145">如果您要撰寫包含屬性或類別提供者註冊的提供者，則並非所有線程模型都能運作。</span><span class="sxs-lookup"><span data-stu-id="2e3ce-145">If you are writing a provider that contains property or class provider registration, not all threading models work.</span></span> <span data-ttu-id="2e3ce-146">如需詳細資訊，請參閱 [選擇正確的註冊](choosing-correct-registration.md)。</span><span class="sxs-lookup"><span data-stu-id="2e3ce-146">For more information, see [Choosing Correct Registration](choosing-correct-registration.md).</span></span>

## <a name="hostingmodel-values-for-in-process-providers"></a><span data-ttu-id="2e3ce-147">In-Process 提供者的 HostingModel 值</span><span class="sxs-lookup"><span data-stu-id="2e3ce-147">HostingModel Values for In-Process Providers</span></span>

<span data-ttu-id="2e3ce-148">下列清單針對 Wmiprvse.exe 進程中執行的提供者，列出要在 [**\_ \_ Win32Provider**](--win32provider.md)實例中使用的提供者裝載模型值。</span><span class="sxs-lookup"><span data-stu-id="2e3ce-148">The following list lists the provider hosting model values to use in the [**\_\_Win32Provider**](--win32provider.md) instance for providers that run in a Wmiprvse.exe process.</span></span>



| <span data-ttu-id="2e3ce-149">[ **\_ \_ Win32Provider. HostingModel** 中的值](--win32provider.md)</span><span class="sxs-lookup"><span data-stu-id="2e3ce-149">Value in [**\_\_Win32Provider.HostingModel**](--win32provider.md)</span></span> | <span data-ttu-id="2e3ce-150">Description</span><span class="sxs-lookup"><span data-stu-id="2e3ce-150">Description</span></span>                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                       |
|--------------------------------------------------------------------|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="2e3ce-151">**SelfHost**</span><span class="sxs-lookup"><span data-stu-id="2e3ce-151">**SelfHost**</span></span>                                                       | <span data-ttu-id="2e3ce-152">提供者會開始使用本機伺服器執行，而不是同進程。</span><span class="sxs-lookup"><span data-stu-id="2e3ce-152">The provider starts using the local server implementation instead of in-process.</span></span> <span data-ttu-id="2e3ce-153">提供者執行之進程的安全性內容會決定提供者的安全性內容。</span><span class="sxs-lookup"><span data-stu-id="2e3ce-153">The security context of the process in which the provider runs determines the provider security context.</span></span>                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                         |
| <span data-ttu-id="2e3ce-154">**LocalSystemHost**</span><span class="sxs-lookup"><span data-stu-id="2e3ce-154">**LocalSystemHost**</span></span>                                                | <span data-ttu-id="2e3ce-155">提供者（如果實作為同進程）會載入至在 [LocalSystem](/windows/desktop/Services/localsystem-account) 內容下執行的共用提供者主機。</span><span class="sxs-lookup"><span data-stu-id="2e3ce-155">The provider, if implemented as in-process, is loaded into a shared provider host running under [LocalSystem](/windows/desktop/Services/localsystem-account) context.</span></span> <span data-ttu-id="2e3ce-156">從 Windows Vista 開始，如果 WMI 提供者的 [**HostingModel**](--win32provider.md) (**\_ \_ Win32Provider**， **LocalSystemHost** 就不再是預設的裝載模型。未指定 HostingModel 屬性) 。</span><span class="sxs-lookup"><span data-stu-id="2e3ce-156">Starting with Windows Vista, **LocalSystemHost** is no longer the default hosting model if the [**HostingModel**](--win32provider.md) of a WMI provider (**\_\_Win32Provider**.**HostingModel** property) is unspecified.</span></span> <span data-ttu-id="2e3ce-157">如需詳細資訊，請參閱 [裝載模型的安全性](#provider-hosting-and-security)。</span><span class="sxs-lookup"><span data-stu-id="2e3ce-157">For more information, see [Security of Hosting Models](#provider-hosting-and-security).</span></span>                                                                                                                                                                                                                                                                               |
| <span data-ttu-id="2e3ce-158">**LocalSystemHostOrSelfHost**</span><span class="sxs-lookup"><span data-stu-id="2e3ce-158">**LocalSystemHostOrSelfHost**</span></span>                                      | <span data-ttu-id="2e3ce-159">此提供者會自我裝載，或載入至在 [LocalSystem](/windows/desktop/Services/localsystem-account) 帳戶下執行的 Wmiprvse.exe 進程。</span><span class="sxs-lookup"><span data-stu-id="2e3ce-159">The provider is self-hosted or loaded into the Wmiprvse.exe process running under the [LocalSystem](/windows/desktop/Services/localsystem-account) account.</span></span> <span data-ttu-id="2e3ce-160">由於 LocalSystem 是具有高度許可權的帳戶，因此會在 Security NT 事件記錄檔中產生專案，以通知系統管理員在此受信任狀態下執行的提供者。</span><span class="sxs-lookup"><span data-stu-id="2e3ce-160">Because LocalSystem is a highly privileged account, an entry is generated in the Security NT Event Log to notify administrators of a provider running in this trusted status.</span></span>                                                                                                                                                                                                                                                                                                                                                                                                                              |
| <span data-ttu-id="2e3ce-161">**NetworkServiceHost**</span><span class="sxs-lookup"><span data-stu-id="2e3ce-161">**NetworkServiceHost**</span></span>                                             | <span data-ttu-id="2e3ce-162">提供者（如果實作為同進程）會載入至在 [NetworkService](/windows/desktop/Services/networkservice-account) 帳戶下執行的 Wmiprvse.exe 進程。</span><span class="sxs-lookup"><span data-stu-id="2e3ce-162">The provider, if implemented as in-process, is loaded into the Wmiprvse.exe process running under [NetworkService](/windows/desktop/Services/networkservice-account) account.</span></span> <span data-ttu-id="2e3ce-163">從 Windows Vista 開始，如果 WMI 提供者的 [**HostingModel**](--win32provider.md) (**\_ \_ Win32Provider**，這就是預設的裝載模型。未指定 HostingModel 屬性) 。</span><span class="sxs-lookup"><span data-stu-id="2e3ce-163">Starting with Windows Vista, this is the default hosting model if the [**HostingModel**](--win32provider.md) of a WMI provider (**\_\_Win32Provider**.**HostingModel** property) is unspecified.</span></span> <span data-ttu-id="2e3ce-164">如需詳細資訊，請參閱 [裝載模型的安全性](#provider-hosting-and-security)。</span><span class="sxs-lookup"><span data-stu-id="2e3ce-164">For more information, see [Security of Hosting Models](#provider-hosting-and-security).</span></span><br/> <span data-ttu-id="2e3ce-165">**NetworkServiceHost** 具有有限的許可權，因此可降低權限提高攻擊的可能性。</span><span class="sxs-lookup"><span data-stu-id="2e3ce-165">**NetworkServiceHost** has limited privileges and therefore reduces the possibility of an elevation of privilege attack.</span></span> <span data-ttu-id="2e3ce-166">如果提供者只在本機電腦上運作，請將 [**HostingModel**](--win32provider.md) 屬性設定為 **LocalServiceHost**。</span><span class="sxs-lookup"><span data-stu-id="2e3ce-166">If the provider only operates within the local computer, then set the [**HostingModel**](--win32provider.md) property to **LocalServiceHost**.</span></span><br/> |
| <span data-ttu-id="2e3ce-167">**NetworkServiceHostOrSelfHost**</span><span class="sxs-lookup"><span data-stu-id="2e3ce-167">**NetworkServiceHostOrSelfHost**</span></span>                                   | <span data-ttu-id="2e3ce-168">此提供者會自我裝載，或載入至在 [NetworkService](/windows/desktop/Services/networkservice-account) 帳戶下執行的 WmiPrvse.exe 進程。</span><span class="sxs-lookup"><span data-stu-id="2e3ce-168">The provider is self-hosted or loaded into the WmiPrvse.exe process running under the [NetworkService](/windows/desktop/Services/networkservice-account) account.</span></span> <span data-ttu-id="2e3ce-169">當 **\_ \_ Win32Provider** 中的 [**HostingModel**](--win32provider.md)屬性為 **Null** 時， **NetworkServiceHostOrSelfHost** 是預設的設定。</span><span class="sxs-lookup"><span data-stu-id="2e3ce-169">**NetworkServiceHostOrSelfHost** is the default configuration when the [**HostingModel**](--win32provider.md) property in **\_\_Win32Provider** is **NULL**.</span></span> <span data-ttu-id="2e3ce-170">由於 **NetworkServiceHostOrSelfHost** 是預設值，因此舊版作業系統的提供者可以在 windows Vista、windows Server 2008 和更新版本的作業系統中繼續運作。</span><span class="sxs-lookup"><span data-stu-id="2e3ce-170">Because **NetworkServiceHostOrSelfHost** is the default, providers from earlier operating systems can continue to work in Windows Vista, Windows Server 2008, and later operating systems.</span></span>                                                                                                                                                                                                                                             |
| <span data-ttu-id="2e3ce-171">**LocalServiceHost**</span><span class="sxs-lookup"><span data-stu-id="2e3ce-171">**LocalServiceHost**</span></span>                                               | <span data-ttu-id="2e3ce-172">提供者（如果實作為同進程）會載入至 [LocalService](/windows/desktop/Services/localservice-account) 帳戶下執行的 Wmiprvse.exe 進程。</span><span class="sxs-lookup"><span data-stu-id="2e3ce-172">The provider, if implemented as in-process, is loaded into the Wmiprvse.exe process running under the [LocalService](/windows/desktop/Services/localservice-account) account.</span></span> <span data-ttu-id="2e3ce-173">這是建議的服務裝載模型，因為 LocalService 具有有限的許可權。</span><span class="sxs-lookup"><span data-stu-id="2e3ce-173">This is the recommended hosting model for services because LocalService has limited privileges.</span></span>                                                                                                                                                                                                                                                                                                                                                                                                                                                                                          |



 

## <a name="hostingmodel-values-for-decoupled-providers"></a><span data-ttu-id="2e3ce-174">HostingModel 低耦合提供者的值</span><span class="sxs-lookup"><span data-stu-id="2e3ce-174">HostingModel Values for Decoupled Providers</span></span>

<span data-ttu-id="2e3ce-175">下列清單列出低耦合提供者的提供者裝載模型值。</span><span class="sxs-lookup"><span data-stu-id="2e3ce-175">The following list lists the provider hosting model values for decoupled providers.</span></span>

<dl> <dt>

<span data-ttu-id="2e3ce-176"><span id="Decoupled_Com"></span><span id="decoupled_com"></span><span id="DECOUPLED_COM"></span>**分離： Com**</span><span class="sxs-lookup"><span data-stu-id="2e3ce-176"><span id="Decoupled_Com"></span><span id="decoupled_com"></span><span id="DECOUPLED_COM"></span>**Decoupled:Com**</span></span>
</dt> <dd>

<span data-ttu-id="2e3ce-177">提供者是在另一個進程中裝載的低耦合提供者，也就是 WMI 的用戶端。</span><span class="sxs-lookup"><span data-stu-id="2e3ce-177">The provider is a decoupled provider hosted in a separate process that is a client to WMI.</span></span>

<span data-ttu-id="2e3ce-178">下列範例顯示 [**HostingModel**](--win32provider.md) 屬性設定為 **FALSE** 的 FoldIdentity 規範，允許提供者模擬用戶端。</span><span class="sxs-lookup"><span data-stu-id="2e3ce-178">The following example shows the FoldIdentity specifier for the [**HostingModel**](--win32provider.md) property set to **FALSE**, which allows the provider to impersonate the client.</span></span>

``` syntax
Decoupled:Com:FoldIdentity(FALSE)
```

<span data-ttu-id="2e3ce-179">如果未指定 FoldIdentity，FoldIdentity 值預設會設定為 **TRUE** 。</span><span class="sxs-lookup"><span data-stu-id="2e3ce-179">If FoldIdentity is not specified, the FoldIdentity value is set to **TRUE** by default.</span></span> <span data-ttu-id="2e3ce-180">基於安全性理由，建議您不要指定 FoldIdentity (FALSE) 因為具有模擬委派的 rogue 應用程式可能會影響整個網域。</span><span class="sxs-lookup"><span data-stu-id="2e3ce-180">For security reasons, it is recommended that you not specify FoldIdentity(FALSE) since a rogue application with impersonation of Delegate can affect an entire domain.</span></span>

<span data-ttu-id="2e3ce-181">下列範例會以建議的方式顯示 [**HostingModel**](--win32provider.md) 屬性集，相當於設定 FOLDIDENTITY (TRUE) 。</span><span class="sxs-lookup"><span data-stu-id="2e3ce-181">The following example shows the [**HostingModel**](--win32provider.md) property set in the recommended manner that is equivalent to setting FoldIdentity(TRUE).</span></span>

``` syntax
Decoupled:Com
```

</dd> <dt>

<span data-ttu-id="2e3ce-182"><span id="Decoupled_Noncom"></span><span id="decoupled_noncom"></span><span id="DECOUPLED_NONCOM"></span>**分離： Noncom**</span><span class="sxs-lookup"><span data-stu-id="2e3ce-182"><span id="Decoupled_Noncom"></span><span id="decoupled_noncom"></span><span id="DECOUPLED_NONCOM"></span>**Decoupled:Noncom**</span></span>
</dt> <dd>

<span data-ttu-id="2e3ce-183">僅供內部使用。</span><span class="sxs-lookup"><span data-stu-id="2e3ce-183">For internal use only.</span></span> <span data-ttu-id="2e3ce-184">不支援。</span><span class="sxs-lookup"><span data-stu-id="2e3ce-184">Not supported.</span></span>

</dd> </dl>

## <a name="security-of-hosting-models"></a><span data-ttu-id="2e3ce-185">裝載模型的安全性</span><span class="sxs-lookup"><span data-stu-id="2e3ce-185">Security of Hosting Models</span></span>

<span data-ttu-id="2e3ce-186">在大多數情況下， **LocalSystem** 是不必要的，而且 **NetworkServiceHost** 內容更適合。</span><span class="sxs-lookup"><span data-stu-id="2e3ce-186">For most situations, **LocalSystem** is unnecessary and the **NetworkServiceHost** context is more appropriate.</span></span> <span data-ttu-id="2e3ce-187">大部分的 WMI 提供者都必須模擬用戶端安全性內容，以代表 WMI 用戶端執行要求的作業。</span><span class="sxs-lookup"><span data-stu-id="2e3ce-187">Most WMI Providers must impersonate the client security context to perform requested operations on behalf of the WMI client.</span></span> <span data-ttu-id="2e3ce-188">從 Windows Vista 開始，缺少裝載模型定義並執行的 WMI 提供 **者將無法** 正常執行。</span><span class="sxs-lookup"><span data-stu-id="2e3ce-188">Starting with Windows Vista, a WMI provider that lacks a hosting model definition and executes as if it is running under **LocalSystem** will not run properly.</span></span> <span data-ttu-id="2e3ce-189">若要修正這種情況，請變更預期的裝載模型，並確定 WMI 提供者程式碼會模擬 WMI 用戶端，以在用戶端安全性內容中執行作業。</span><span class="sxs-lookup"><span data-stu-id="2e3ce-189">To correct this situation, change the expected hosting model and ensure that the WMI provider code performs the operations in the client security context by impersonating the WMI client.</span></span> <span data-ttu-id="2e3ce-190">LocalSystem 很少需要。</span><span class="sxs-lookup"><span data-stu-id="2e3ce-190">LocalSystem is rarely an requirement.</span></span> <span data-ttu-id="2e3ce-191">如果您的提供者必須擁有該層級的許可權，請使用 MOF 檔案中的下列語句來指定裝載模型。</span><span class="sxs-lookup"><span data-stu-id="2e3ce-191">If your provider must have that level of privilege, specify the hosting model with the following statement in the MOF file.</span></span>

``` syntax
HostingModel=LocalSystemHost
```

## <a name="related-topics"></a><span data-ttu-id="2e3ce-192">相關主題</span><span class="sxs-lookup"><span data-stu-id="2e3ce-192">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="2e3ce-193">選擇正確的註冊</span><span class="sxs-lookup"><span data-stu-id="2e3ce-193">Choosing Correct Registration</span></span>](choosing-correct-registration.md)
</dt> <dt>

[<span data-ttu-id="2e3ce-194">存取 WMI 命名空間</span><span class="sxs-lookup"><span data-stu-id="2e3ce-194">Access to WMI Namespaces</span></span>](access-to-wmi-namespaces.md)
</dt> <dt>

[<span data-ttu-id="2e3ce-195">保護 WMI 命名空間</span><span class="sxs-lookup"><span data-stu-id="2e3ce-195">Securing WMI Namespaces</span></span>](securing-wmi-namespaces.md)
</dt> <dt>

[<span data-ttu-id="2e3ce-196">提供者設定和疑難排解類別</span><span class="sxs-lookup"><span data-stu-id="2e3ce-196">Provider Configuration and Troubleshooting Classes</span></span>](provider-configuration-and-troubleshooting-classes.md)
</dt> <dt>

[<span data-ttu-id="2e3ce-197">**MSFT \_ 提供者**</span><span class="sxs-lookup"><span data-stu-id="2e3ce-197">**MSFT\_Providers**</span></span>](/previous-versions/windows/desktop/wmisystemprov/msft-providers)
</dt> <dt>

[<span data-ttu-id="2e3ce-198">維護 WMI 安全性</span><span class="sxs-lookup"><span data-stu-id="2e3ce-198">Maintaining WMI Security</span></span>](maintaining-wmi-security.md)
</dt> </dl>

 

