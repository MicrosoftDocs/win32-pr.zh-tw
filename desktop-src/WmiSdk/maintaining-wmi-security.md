---
description: WMI 安全性著重在保護對命名空間資料的存取。 WMI 會先將存取權授與 WMI 控制和 DCOM 設定所指定的使用者群組，然後提供者判斷使用者是否應該具有命名空間資料的存取權。
ms.assetid: 88a2538a-ae30-4a1a-9d16-f0cd9419b2ed
ms.tgt_platform: multiple
title: 維護 WMI 安全性
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: f25cbf4a29567b263d6bd279aac9e2e6e21c523e
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/08/2021
ms.locfileid: "106978253"
---
# <a name="maintaining-wmi-security"></a><span data-ttu-id="69f8c-104">維護 WMI 安全性</span><span class="sxs-lookup"><span data-stu-id="69f8c-104">Maintaining WMI Security</span></span>

<span data-ttu-id="69f8c-105">WMI 安全性著重在保護對命名空間資料的存取。</span><span class="sxs-lookup"><span data-stu-id="69f8c-105">WMI security focuses on protecting access to namespace data.</span></span> <span data-ttu-id="69f8c-106">WMI 會先將存取權授與 [*Wmi 控制*](gloss-w.md) 和 DCOM 設定所指定的使用者群組，然後提供者判斷使用者是否應該具有命名空間資料的存取權。</span><span class="sxs-lookup"><span data-stu-id="69f8c-106">WMI first grants access to groups of users as specified by the [*WMI Control*](gloss-w.md) and DCOM settings and then providers determine if the user should have access to namespace data.</span></span>

<span data-ttu-id="69f8c-107">本主題將討論下列各節：</span><span class="sxs-lookup"><span data-stu-id="69f8c-107">The following sections are discussed in this topic:</span></span>

-   [<span data-ttu-id="69f8c-108">命名空間安全性</span><span class="sxs-lookup"><span data-stu-id="69f8c-108">Namespace Security</span></span>](#namespace-security)
-   [<span data-ttu-id="69f8c-109">分散式元件物件模型 (DCOM) 安全性設定。</span><span class="sxs-lookup"><span data-stu-id="69f8c-109">Distributed Component Object Model (DCOM) Security Settings.</span></span>](#distributed-component-object-model-dcom-security-settings)
-   [<span data-ttu-id="69f8c-110">WMI、共用服務主機和驗證</span><span class="sxs-lookup"><span data-stu-id="69f8c-110">WMI, Shared Service Hosts, and Authentication</span></span>](#wmi-shared-service-hosts-and-authentication)
-   [<span data-ttu-id="69f8c-111">WMI 用戶端腳本和應用程式的安全性</span><span class="sxs-lookup"><span data-stu-id="69f8c-111">Security for WMI Client Scripts and Applications</span></span>](#security-for-wmi-client-scripts-and-applications)
-   [<span data-ttu-id="69f8c-112">相關主題</span><span class="sxs-lookup"><span data-stu-id="69f8c-112">Related topics</span></span>](#related-topics)

## <a name="namespace-security"></a><span data-ttu-id="69f8c-113">命名空間安全性</span><span class="sxs-lookup"><span data-stu-id="69f8c-113">Namespace Security</span></span>

<span data-ttu-id="69f8c-114">命名空間安全性相依于標準 Windows 使用者 [*安全識別碼 (SID)*](gloss-s.md) 和 WMI 命名空間的 [*安全描述項*](gloss-s.md) 。</span><span class="sxs-lookup"><span data-stu-id="69f8c-114">Namespace security depends on standard Windows user [*security identifiers (SID)*](gloss-s.md) and the [*security descriptor*](gloss-s.md) for the WMI namespace.</span></span>

<span data-ttu-id="69f8c-115">您可以藉由執行下列動作來設定命名空間安全性：</span><span class="sxs-lookup"><span data-stu-id="69f8c-115">You can set namespace security by performing the following actions:</span></span>

-   <span data-ttu-id="69f8c-116">使用 WMI 控制或建立命名空間時，授與或拒絕使用者命名空間的存取權限。</span><span class="sxs-lookup"><span data-stu-id="69f8c-116">Grant or deny access rights to namespaces for users using the WMI Control or when the namespace is created.</span></span> <span data-ttu-id="69f8c-117">如需詳細資訊，請參閱 [使用 WMI 控制項設定命名空間安全性](setting-namespace-security-with-the-wmi-control.md) 以及建立 [命名空間時設定命名空間安全性](setting-namespace-security-when-the-namespace-is-created.md)。</span><span class="sxs-lookup"><span data-stu-id="69f8c-117">For more information, see [Setting Namespace Security with the WMI Control](setting-namespace-security-with-the-wmi-control.md) and [Setting Namespace Security When the Namespace is Created](setting-namespace-security-when-the-namespace-is-created.md).</span></span>
-   <span data-ttu-id="69f8c-118">使用 WMI 控制 [安全性] 索引標籤來建立安全性審核。</span><span class="sxs-lookup"><span data-stu-id="69f8c-118">Use the WMI Control Security tab to establish security auditing.</span></span> <span data-ttu-id="69f8c-119">安全性審核會在使用者失敗或成功時，產生事件記錄專案，例如將資料寫入至 WMI 物件或讀取安全描述項。</span><span class="sxs-lookup"><span data-stu-id="69f8c-119">Security auditing results in event log entries when a user fails or succeeds in an audited action, such as writing data to a WMI object or reading the security descriptor.</span></span> <span data-ttu-id="69f8c-120">如需詳細資訊，請參閱 [WMI 命名空間的存取](access-to-wmi-namespaces.md)。</span><span class="sxs-lookup"><span data-stu-id="69f8c-120">For more information, see [Access to WMI Namespaces](access-to-wmi-namespaces.md).</span></span>
-   <span data-ttu-id="69f8c-121">使用定義命名空間的 MOF 檔案，要求使用者建立加密的連接。</span><span class="sxs-lookup"><span data-stu-id="69f8c-121">Use the MOF file that defines the namespace to require a user to make an encrypted connection.</span></span> <span data-ttu-id="69f8c-122">如需詳細資訊，請參閱 [要求命名空間的加密連接](requiring-an-encrypted-connection-to-a-namespace.md)。</span><span class="sxs-lookup"><span data-stu-id="69f8c-122">For more information, see [Requiring an Encrypted Connection to a Namespace](requiring-an-encrypted-connection-to-a-namespace.md).</span></span>

## <a name="distributed-component-object-model-dcom-security-settings"></a><span data-ttu-id="69f8c-123">分散式元件物件模型 (DCOM) 安全性設定。</span><span class="sxs-lookup"><span data-stu-id="69f8c-123">Distributed Component Object Model (DCOM) Security Settings.</span></span>

<span data-ttu-id="69f8c-124">DCOM 安全性需要驗證設定和模擬設定。</span><span class="sxs-lookup"><span data-stu-id="69f8c-124">DCOM security requires an authentication setting and an impersonation setting.</span></span> <span data-ttu-id="69f8c-125">驗證表示一個進程會將本身識別為另一個進程。</span><span class="sxs-lookup"><span data-stu-id="69f8c-125">Authentication means that one process identifies itself to another.</span></span> <span data-ttu-id="69f8c-126">模擬會識別用戶端授與伺服器以呼叫不同進程的授權單位。</span><span class="sxs-lookup"><span data-stu-id="69f8c-126">Impersonation identifies the authority that a client grants a server to call different processes.</span></span> <span data-ttu-id="69f8c-127">在安全性檢查期間，伺服器會模擬用戶端。</span><span class="sxs-lookup"><span data-stu-id="69f8c-127">During a security check, the server impersonates the client.</span></span> <span data-ttu-id="69f8c-128">如需詳細資訊，請參閱 [保護 c + + 用戶端和提供者](securing-c---clients-and-providers.md) ，或 [保護腳本用戶端](securing-scripting-clients.md)。</span><span class="sxs-lookup"><span data-stu-id="69f8c-128">For more information, see [Securing C++ Clients and Providers](securing-c---clients-and-providers.md) or [Securing Scripting Clients](securing-scripting-clients.md).</span></span>

<span data-ttu-id="69f8c-129">腳本和 C/c + +/C # 應用程式會在連線至 WMI 命名空間時建立驗證和模擬層級，或使用預設設定。</span><span class="sxs-lookup"><span data-stu-id="69f8c-129">Scripts and C/C++/C# applications either establish an authentication and impersonation levels when they connect to a WMI namespace or they use the default settings.</span></span> <span data-ttu-id="69f8c-130">遠端電腦的連線需要與本機電腦上的 WMI 命名空間不同的設定。</span><span class="sxs-lookup"><span data-stu-id="69f8c-130">Connections to remote computers require different settings than to the WMI namespaces on the local computer.</span></span> <span data-ttu-id="69f8c-131">如需詳細資訊，請參閱 [連接到遠端電腦上的 WMI](connecting-to-wmi-on-a-remote-computer.md)。</span><span class="sxs-lookup"><span data-stu-id="69f8c-131">For more information, see [Connecting to WMI on a Remote Computer](connecting-to-wmi-on-a-remote-computer.md).</span></span>

## <a name="wmi-shared-service-hosts-and-authentication"></a><span data-ttu-id="69f8c-132">WMI、共用服務主機和驗證</span><span class="sxs-lookup"><span data-stu-id="69f8c-132">WMI, Shared Service Hosts, and Authentication</span></span>

<span data-ttu-id="69f8c-133">WMI 存在於共用服務主機中，有數個其他服務在 NetworkService 帳戶下執行。</span><span class="sxs-lookup"><span data-stu-id="69f8c-133">WMI resides in a shared service host with several other services running under the NetworkService account.</span></span> <span data-ttu-id="69f8c-134">在 Svchost 進程中，WMI 與主機中的其他進程共用相同的驗證。</span><span class="sxs-lookup"><span data-stu-id="69f8c-134">In a Svchost process, WMI shares the same authentication as the other processes in the host.</span></span>

<span data-ttu-id="69f8c-135">從 WMI 將提供者 Dll 載入至不同的服務主機進程。</span><span class="sxs-lookup"><span data-stu-id="69f8c-135">Provider DLLs are loaded into separate service host processes from WMI.</span></span> <span data-ttu-id="69f8c-136">代表提供者之 [**\_ \_ Win32Provider**](--win32provider.md)系統類別中的 **HostingModel** 屬性會指定提供者執行時所使用的系統帳戶。</span><span class="sxs-lookup"><span data-stu-id="69f8c-136">The **HostingModel** property in the [**\_\_Win32Provider**](--win32provider.md) system class that represents a provider specifies the system account under which the provider runs.</span></span> <span data-ttu-id="69f8c-137">設定這個屬性會使提供者載入具有指定許可權層級的共用主機進程中。</span><span class="sxs-lookup"><span data-stu-id="69f8c-137">Setting this property causes the provider to be loaded into a shared host process that has a specified level of privilege.</span></span> <span data-ttu-id="69f8c-138">如需詳細資訊，請參閱 [提供者裝載和安全性](provider-hosting-and-security.md)。</span><span class="sxs-lookup"><span data-stu-id="69f8c-138">For more information, see [Provider Hosting and Security](provider-hosting-and-security.md).</span></span>

## <a name="security-for-wmi-client-scripts-and-applications"></a><span data-ttu-id="69f8c-139">WMI 用戶端腳本和應用程式的安全性</span><span class="sxs-lookup"><span data-stu-id="69f8c-139">Security for WMI Client Scripts and Applications</span></span>

<span data-ttu-id="69f8c-140">腳本和應用程式必須建立正確的安全性，以連接到本機和遠端電腦上的 WMI 命名空間。</span><span class="sxs-lookup"><span data-stu-id="69f8c-140">Scripts and applications must establish the correct security to connect to WMI namespaces on local and remote computers.</span></span> <span data-ttu-id="69f8c-141">如需詳細資訊，請參閱 [保護 c + + 用戶端和提供者](securing-c---clients-and-providers.md)、 [保護腳本用戶端](securing-scripting-clients.md)安全，以及 [保護 WMI 事件](securing-wmi-events.md)。</span><span class="sxs-lookup"><span data-stu-id="69f8c-141">For more information, see [Securing C++ Clients and Providers](securing-c---clients-and-providers.md), [Securing Scripting Clients](securing-scripting-clients.md), and [Securing WMI Events](securing-wmi-events.md).</span></span>

<span data-ttu-id="69f8c-142">下表列出有關維護 WMI 安全性的主題。</span><span class="sxs-lookup"><span data-stu-id="69f8c-142">The following table lists the topics on maintaining WMI security.</span></span>



| <span data-ttu-id="69f8c-143">主題</span><span class="sxs-lookup"><span data-stu-id="69f8c-143">Topic</span></span>                                                                                              | <span data-ttu-id="69f8c-144">描述</span><span class="sxs-lookup"><span data-stu-id="69f8c-144">Description</span></span>                                                                                                                                                           |
|----------------------------------------------------------------------------------------------------|-----------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [<span data-ttu-id="69f8c-145">保護 WMI 命名空間</span><span class="sxs-lookup"><span data-stu-id="69f8c-145">Securing WMI Namespaces</span></span>](securing-wmi-namespaces.md)                                             | <span data-ttu-id="69f8c-146">您可以透過 WMI 控制項，將命名空間資料存取限制為已授權的使用者。</span><span class="sxs-lookup"><span data-stu-id="69f8c-146">You can limit namespace data access to authorized users through the WMI Control.</span></span>                                                                                      |
| [<span data-ttu-id="69f8c-147">保護您的提供者</span><span class="sxs-lookup"><span data-stu-id="69f8c-147">Securing Your Provider</span></span>](securing-your-provider.md)                                               | <span data-ttu-id="69f8c-148">撰寫安全提供者的相關資訊。</span><span class="sxs-lookup"><span data-stu-id="69f8c-148">Information about writing secure providers.</span></span>                                                                                                                           |
| [<span data-ttu-id="69f8c-149">保護 c + + 用戶端和提供者</span><span class="sxs-lookup"><span data-stu-id="69f8c-149">Securing C++ Clients and Providers</span></span>](securing-c---clients-and-providers.md)                       | <span data-ttu-id="69f8c-150">C + + 提供者和用戶端應用程式都必須執行許多相同的作業來維護 WMI 安全性。</span><span class="sxs-lookup"><span data-stu-id="69f8c-150">Both C++ providers and client applications must perform many of the same operations to maintain WMI security.</span></span>                                                         |
| [<span data-ttu-id="69f8c-151">保護腳本用戶端</span><span class="sxs-lookup"><span data-stu-id="69f8c-151">Securing Scripting Clients</span></span>](securing-scripting-clients.md)                                       | <span data-ttu-id="69f8c-152">腳本和 Visual Basic 應用程式 (automation 用戶端) 必須設定適當的安全性，以存取 WMI 資料和事件。</span><span class="sxs-lookup"><span data-stu-id="69f8c-152">Scripts and Visual Basic applications (automation clients) must set appropriate security to get access to WMI data and events.</span></span>                                        |
| [<span data-ttu-id="69f8c-153">保護 WMI 事件</span><span class="sxs-lookup"><span data-stu-id="69f8c-153">Securing WMI Events</span></span>](securing-wmi-events.md)                                                     | <span data-ttu-id="69f8c-154">WMI 事件是由事件提供者傳遞給暫時或永久的取用者。</span><span class="sxs-lookup"><span data-stu-id="69f8c-154">WMI events are delivered by the event provider to a temporary or permanent consumer.</span></span> <span data-ttu-id="69f8c-155">事件是以事件類別實例的形式傳遞。</span><span class="sxs-lookup"><span data-stu-id="69f8c-155">Events are delivered in the form of an instance of an event class.</span></span>               |
| [<span data-ttu-id="69f8c-156">變更安全物件的存取安全性</span><span class="sxs-lookup"><span data-stu-id="69f8c-156">Changing Access Security on Securable Objects</span></span>](changing-access-security-on-securable-objects.md) | <span data-ttu-id="69f8c-157">使用適當的許可權，您可以在 WMI 物件上呼叫方法，這些物件代表可讀取或變更安全物件安全描述項的安全物件。</span><span class="sxs-lookup"><span data-stu-id="69f8c-157">With appropriate permissions, you can call methods on the WMI objects that represent securable objects that read or change security descriptors on securable objects.</span></span> |



 

## <a name="related-topics"></a><span data-ttu-id="69f8c-158">相關主題</span><span class="sxs-lookup"><span data-stu-id="69f8c-158">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="69f8c-159">使用 WMI</span><span class="sxs-lookup"><span data-stu-id="69f8c-159">Using WMI</span></span>](using-wmi.md)
</dt> </dl>

 

 



