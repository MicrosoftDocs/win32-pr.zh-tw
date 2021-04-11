---
description: WMI 使用標準的 Windows 安全描述項來控制 WMI 命名空間的存取權。
ms.assetid: 5cf9886c-04fa-480e-889f-b64a6a70d053
ms.tgt_platform: multiple
title: 存取 WMI 命名空間
ms.topic: article
ms.date: 05/31/2018
topic_type:
- kbArticle
api_name: ''
api_type: ''
api_location: ''
ms.openlocfilehash: 6eaebe5370e97dcb42ddcf79018015ceff9147f8
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/08/2021
ms.locfileid: "103945117"
---
# <a name="access-to-wmi-namespaces"></a><span data-ttu-id="52375-103">存取 WMI 命名空間</span><span class="sxs-lookup"><span data-stu-id="52375-103">Access to WMI Namespaces</span></span>

<span data-ttu-id="52375-104">WMI 使用標準的 Windows *安全描述項* 來控制 WMI 命名空間的存取權。</span><span class="sxs-lookup"><span data-stu-id="52375-104">WMI uses a standard Windows *security descriptor* to control access to WMI namespaces.</span></span> <span data-ttu-id="52375-105">當您透過 WMI "winmgmts" 的名字標記或 [**IWbemLocator：： ConnectServer**](/windows/desktop/api/Wbemcli/nf-wbemcli-iwbemlocator-connectserver) 或 [**wbemscripting.swbemlocator**](swbemlocator-connectserver.md)的呼叫來連線至 wmi 時，您會連接到特定的命名空間。</span><span class="sxs-lookup"><span data-stu-id="52375-105">When you connect to WMI, either through the WMI "winmgmts" moniker or a call to [**IWbemLocator::ConnectServer**](/windows/desktop/api/Wbemcli/nf-wbemcli-iwbemlocator-connectserver) or [**SWbemLocator.ConnectServer**](swbemlocator-connectserver.md), you connect to a specific namespace.</span></span>

<span data-ttu-id="52375-106">本主題將討論下列資訊：</span><span class="sxs-lookup"><span data-stu-id="52375-106">The following information is discussed in this topic:</span></span>

-   [<span data-ttu-id="52375-107">WMI 命名空間安全性</span><span class="sxs-lookup"><span data-stu-id="52375-107">WMI Namespace Security</span></span>](#wmi-namespace-security)
-   [<span data-ttu-id="52375-108">WMI 命名空間的審核</span><span class="sxs-lookup"><span data-stu-id="52375-108">WMI Namespace Auditing</span></span>](#wmi-namespace-auditing)
-   [<span data-ttu-id="52375-109">命名空間事件的類型</span><span class="sxs-lookup"><span data-stu-id="52375-109">Types of Namespace Events</span></span>](#types-of-namespace-events)
-   [<span data-ttu-id="52375-110">命名空間存取設定</span><span class="sxs-lookup"><span data-stu-id="52375-110">Namespace Access Settings</span></span>](#namespace-access-settings)
-   [<span data-ttu-id="52375-111">WMI 命名空間的預設許可權</span><span class="sxs-lookup"><span data-stu-id="52375-111">Default Permissions on WMI Namespaces</span></span>](#default-permissions-on-wmi-namespaces)
-   [<span data-ttu-id="52375-112">相關主題</span><span class="sxs-lookup"><span data-stu-id="52375-112">Related topics</span></span>](#related-topics)

## <a name="wmi-namespace-security"></a><span data-ttu-id="52375-113">WMI 命名空間安全性</span><span class="sxs-lookup"><span data-stu-id="52375-113">WMI Namespace Security</span></span>

<span data-ttu-id="52375-114">WMI 會將連接到命名空間之使用者的 [*存取權杖*](/windows/desktop/SecGloss/a-gly) 與命名空間的 [*安全描述項*](/windows/desktop/SecGloss/s-gly) 進行比較，以維護命名空間安全性。</span><span class="sxs-lookup"><span data-stu-id="52375-114">WMI maintains namespace security by comparing the [*access token*](/windows/desktop/SecGloss/a-gly) of the user connecting to the namespace with the [*security descriptor*](/windows/desktop/SecGloss/s-gly) of the namespace.</span></span> <span data-ttu-id="52375-115">如需 Windows 安全性的詳細資訊，請參閱 [存取 WMI 安全物件](access-to-wmi-securable-objects.md)。</span><span class="sxs-lookup"><span data-stu-id="52375-115">For more information about Windows security, see [Access to WMI Securable Objects](access-to-wmi-securable-objects.md).</span></span>

<span data-ttu-id="52375-116">請注意，從 Windows Vista 開始， [使用者帳戶控制 (UAC)](https://www.microsoft.com/technet/windowsvista/security/uac.mspx) 會影響對 wmi 資料的存取權，以及可使用 [*wmi 控制項*](gloss-w.md)設定的內容。</span><span class="sxs-lookup"><span data-stu-id="52375-116">Be aware that, starting with Windows Vista, [User Account Control (UAC)](https://www.microsoft.com/technet/windowsvista/security/uac.mspx) affects access to WMI data and what can be configured with the [*WMI Control*](gloss-w.md).</span></span> <span data-ttu-id="52375-117">如需詳細資訊，請參閱 [WMI 命名空間的預設許可權](#default-permissions-on-wmi-namespaces) 以及 [使用者帳戶控制和 WMI](user-account-control-and-wmi.md)。</span><span class="sxs-lookup"><span data-stu-id="52375-117">For more information, see [Default Permissions on WMI Namespaces](#default-permissions-on-wmi-namespaces) and [User Account Control and WMI](user-account-control-and-wmi.md).</span></span>

<span data-ttu-id="52375-118">從遠端電腦連線時，也會影響對 WMI 命名空間的存取。</span><span class="sxs-lookup"><span data-stu-id="52375-118">Access to WMI namespaces is also affected when the connection is from a remote computer.</span></span> <span data-ttu-id="52375-119">如需詳細資訊，請參閱 [連接到遠端電腦上的 wmi](connecting-to-wmi-on-a-remote-computer.md)、 [保護遠端 WMI](securing-a-remote-wmi-connection.md)連線，以及 [透過 Windows 防火牆連接](/windows/desktop/WmiSdk/connecting-to-wmi-remotely-starting-with-vista)。</span><span class="sxs-lookup"><span data-stu-id="52375-119">For more information, see [Connecting to WMI on a Remote Computer](connecting-to-wmi-on-a-remote-computer.md), [Securing a Remote WMI Connection](securing-a-remote-wmi-connection.md), and [Connecting Through Windows Firewall](/windows/desktop/WmiSdk/connecting-to-wmi-remotely-starting-with-vista).</span></span>

<span data-ttu-id="52375-120">提供者必須依賴連接的模擬設定，以判斷用戶端腳本或應用程式是否應該接收資料。</span><span class="sxs-lookup"><span data-stu-id="52375-120">Providers must rely on the impersonation setting for the connection to determine if the client script or application should receive data.</span></span> <span data-ttu-id="52375-121">如需腳本和用戶端應用程式的詳細資訊，請參閱 [設定用戶端應用程式處理安全性](setting-client-application-process-security.md)。</span><span class="sxs-lookup"><span data-stu-id="52375-121">For more information about script and client applications, see [Setting Client Application Process Security](setting-client-application-process-security.md).</span></span> <span data-ttu-id="52375-122">如需 [*提供者*](gloss-p.md) 模擬的詳細資訊，請參閱 [開發 WMI 提供者](developing-a-wmi-provider.md)。</span><span class="sxs-lookup"><span data-stu-id="52375-122">For more information about [*provider*](gloss-p.md) impersonation, see [Developing a WMI Provider](developing-a-wmi-provider.md).</span></span>

## <a name="wmi-namespace-auditing"></a><span data-ttu-id="52375-123">WMI 命名空間的審核</span><span class="sxs-lookup"><span data-stu-id="52375-123">WMI Namespace Auditing</span></span>

<span data-ttu-id="52375-124">WMI 會使用命名空間 [*系統存取控制清單 (SACL)*](/windows/desktop/SecGloss/s-gly) 來審核命名空間活動。</span><span class="sxs-lookup"><span data-stu-id="52375-124">WMI uses the namespace [*System access control lists (SACL)*](/windows/desktop/SecGloss/s-gly) to audit namespace activity.</span></span> <span data-ttu-id="52375-125">若要啟用 WMI 命名空間的審核，請使用 [*Wmi 控制項*](gloss-w.md)上的 [**安全性**] 索引標籤，變更命名空間的 [審核設定]。</span><span class="sxs-lookup"><span data-stu-id="52375-125">To enable auditing of WMI namespaces, use the **Security** tab on the [*WMI Control*](gloss-w.md) to change the auditing settings for the namespace.</span></span>

<span data-ttu-id="52375-126">安裝作業系統時，不會啟用審核。</span><span class="sxs-lookup"><span data-stu-id="52375-126">Auditing is not enabled during the installation of the operating system.</span></span> <span data-ttu-id="52375-127">若要啟用 [審核]，請按一下標準 **安全性** 視窗中的 [**審核**] 索引標籤。</span><span class="sxs-lookup"><span data-stu-id="52375-127">To enable auditing, click the **Auditing** tab in the standard **Security** window.</span></span> <span data-ttu-id="52375-128">然後您可以新增一個審核專案。</span><span class="sxs-lookup"><span data-stu-id="52375-128">Then you can add an auditing entry.</span></span>

<span data-ttu-id="52375-129">本機電腦的群組原則必須設定為 [允許審核]。</span><span class="sxs-lookup"><span data-stu-id="52375-129">Group Policy for the local computer must be set to allow auditing.</span></span> <span data-ttu-id="52375-130">您可以執行 gpedit.msc MMC 嵌入式管理單元來啟用審核，並在 [電腦設定] 下設定 [**電腦** 設定] 視窗設定 [本機  >    >    >  **原則**  >  **稽核原則**] 下的 [audit 物件存取]。</span><span class="sxs-lookup"><span data-stu-id="52375-130">You can enable auditing by running the Gpedit.msc MMC snap-in and setting **Audit Object Access** under **Computer Configuration** > **Windows Settings** > **Security Settings** > **Local Policies** > **Audit Policy**.</span></span>

<span data-ttu-id="52375-131">審核專案會編輯命名空間的 SACL。</span><span class="sxs-lookup"><span data-stu-id="52375-131">An auditing entry edits the SACL of the namespace.</span></span> <span data-ttu-id="52375-132">當您新增審核專案時，它可以是使用者、群組、電腦或內建的安全性主體。</span><span class="sxs-lookup"><span data-stu-id="52375-132">When you add an auditing entry, it is either a user, group, computer, or built-in security principal.</span></span> <span data-ttu-id="52375-133">加入專案之後，您可以設定產生安全性記錄事件的存取作業。</span><span class="sxs-lookup"><span data-stu-id="52375-133">After adding the entry, you can set the access operations that result in Security Log events.</span></span> <span data-ttu-id="52375-134">例如，您可以在 [群組驗證的使用者] 中按一下 [執行方法]。</span><span class="sxs-lookup"><span data-stu-id="52375-134">For example, for the group Authenticated Users, you can click Execute Methods.</span></span> <span data-ttu-id="52375-135">每當 [已驗證的使用者] 群組的成員在該命名空間中執行方法時，此設定就會產生安全性記錄檔事件。</span><span class="sxs-lookup"><span data-stu-id="52375-135">This setting results in Security Log events whenever a member of the Authenticated Users group executes a method in that namespace.</span></span> <span data-ttu-id="52375-136">WMI 事件的事件識別碼為4662。</span><span class="sxs-lookup"><span data-stu-id="52375-136">The Event ID for WMI events is 4662.</span></span>

<span data-ttu-id="52375-137">您的帳戶必須位於系統管理員群組中，並以較高的許可權執行，才能變更 [審核設定]。</span><span class="sxs-lookup"><span data-stu-id="52375-137">Your account must be in the Administrators group and running under elevated privilege to change the auditing settings.</span></span> <span data-ttu-id="52375-138">內建的系統管理員帳戶也可以變更命名空間的安全性或審核。</span><span class="sxs-lookup"><span data-stu-id="52375-138">The built-in Administrator account can also change the security or auditing for a namespace.</span></span> <span data-ttu-id="52375-139">如需在提高許可權模式下執行的詳細資訊，請參閱 [使用者帳戶控制和 WMI](user-account-control-and-wmi.md)。</span><span class="sxs-lookup"><span data-stu-id="52375-139">For more information about running in elevated mode, see [User Account Control and WMI](user-account-control-and-wmi.md).</span></span>

<span data-ttu-id="52375-140">WMI 審核會產生嘗試存取 WMI 命名空間的成功或失敗事件。</span><span class="sxs-lookup"><span data-stu-id="52375-140">WMI auditing generates success or failure events for attempts to access WMI namespaces.</span></span> <span data-ttu-id="52375-141">服務不會審核提供者作業成功或失敗。</span><span class="sxs-lookup"><span data-stu-id="52375-141">The service does not audit the success or failure of provider operations.</span></span> <span data-ttu-id="52375-142">例如，當腳本連線至 WMI 和命名空間時，可能會失敗，因為執行腳本的帳戶無法存取該命名空間，或可能嘗試操作（例如編輯 DACL），但未授與。</span><span class="sxs-lookup"><span data-stu-id="52375-142">For example, when a script connects to WMI and a namespace, it may fail because the account under which the script is running does not have access to that the namespace or may attempt an operation, such as editing the DACL, that is not granted.</span></span>

<span data-ttu-id="52375-143">如果您是以 Administrators 群組中的帳戶執行，則可以在 **事件檢視器** 使用者介面中查看命名空間審核事件。</span><span class="sxs-lookup"><span data-stu-id="52375-143">If you are running under an account in the Administrators group, you can view the namespace auditing events in the **Event Viewer** user interface.</span></span>

## <a name="types-of-namespace-events"></a><span data-ttu-id="52375-144">命名空間事件的類型</span><span class="sxs-lookup"><span data-stu-id="52375-144">Types of Namespace Events</span></span>

<span data-ttu-id="52375-145">WMI 會追蹤安全性事件記錄檔中的下列事件種類：</span><span class="sxs-lookup"><span data-stu-id="52375-145">WMI traces the following types of events in the Security Event Log:</span></span>

-   <span data-ttu-id="52375-146">稽核成功</span><span class="sxs-lookup"><span data-stu-id="52375-146">Audit Success</span></span>

    <span data-ttu-id="52375-147">作業必須成功完成兩個步驟，才能成功進行審核。</span><span class="sxs-lookup"><span data-stu-id="52375-147">The operation must successfully complete two steps for an Audit Success.</span></span> <span data-ttu-id="52375-148">首先，WMI 會根據用戶端 SID 和命名空間 DACL，授與用戶端應用程式或腳本的存取權。</span><span class="sxs-lookup"><span data-stu-id="52375-148">First, WMI grants access to the client application or script based on the client SID and the namespace DACL.</span></span> <span data-ttu-id="52375-149">其次，要求的作業符合該使用者或群組的命名空間 SACL 中的存取權限。</span><span class="sxs-lookup"><span data-stu-id="52375-149">Second, the requested operation matches the access rights in the namespace SACL for that user or group.</span></span>

-   <span data-ttu-id="52375-150">Audit 失敗</span><span class="sxs-lookup"><span data-stu-id="52375-150">Audit Failure</span></span>

    <span data-ttu-id="52375-151">WMI 拒絕存取命名空間，但要求的作業符合該使用者或群組的命名空間 SACL 中的存取權限。</span><span class="sxs-lookup"><span data-stu-id="52375-151">WMI denies access to the namespace, but the requested operation matches the access rights in the namespace SACL for that user or group.</span></span>

## <a name="namespace-access-settings"></a><span data-ttu-id="52375-152">命名空間存取設定</span><span class="sxs-lookup"><span data-stu-id="52375-152">Namespace Access Settings</span></span>

<span data-ttu-id="52375-153">您可以在 WMI 控制項上，查看各種帳戶的命名空間存取權限。</span><span class="sxs-lookup"><span data-stu-id="52375-153">You can view the namespace access rights for various accounts on the WMI Control.</span></span> <span data-ttu-id="52375-154">這些常數會在 [**命名空間存取權限常數**](namespace-access-rights-constants.md)中描述。</span><span class="sxs-lookup"><span data-stu-id="52375-154">These constants are described in [**Namespace Access Rights Constants**](namespace-access-rights-constants.md).</span></span> <span data-ttu-id="52375-155">您可以使用 WMI 控制或以程式設計方式變更 WMI 命名空間的存取權。</span><span class="sxs-lookup"><span data-stu-id="52375-155">You can change the access to a WMI namespace using the WMI Control or programmatically.</span></span> <span data-ttu-id="52375-156">如需詳細資訊，請參閱 [變更安全物件的存取安全性](changing-access-security-on-securable-objects.md)。</span><span class="sxs-lookup"><span data-stu-id="52375-156">For more information, see [Changing Access Security on Securable Objects](changing-access-security-on-securable-objects.md).</span></span>

<span data-ttu-id="52375-157">除了遠端啟用許可權之外，WMI 會針對下列清單所列的所有存取權限進行變更。</span><span class="sxs-lookup"><span data-stu-id="52375-157">WMI audits changes in all of the access permissions listed in the following list except for the Remote Enable permission.</span></span> <span data-ttu-id="52375-158">這些變更會記錄為與編輯安全性許可權相對應的 audit success 或失敗。</span><span class="sxs-lookup"><span data-stu-id="52375-158">The changes are logged as audit success or failure corresponding to the Edit Security permission.</span></span>

<dl> <dt>

<span data-ttu-id="52375-159"><span id="Execute_Methods"></span><span id="execute_methods"></span><span id="EXECUTE_METHODS"></span>Execute 方法</span><span class="sxs-lookup"><span data-stu-id="52375-159"><span id="Execute_Methods"></span><span id="execute_methods"></span><span id="EXECUTE_METHODS"></span>Execute Methods</span></span>
</dt> <dd>

<span data-ttu-id="52375-160">允許使用者執行 WMI 類別上定義的方法。</span><span class="sxs-lookup"><span data-stu-id="52375-160">Permits the user to execute methods defined on WMI classes.</span></span> <span data-ttu-id="52375-161">對應至 **WBEM \_ 方法 \_ 執行** 存取權限常數。</span><span class="sxs-lookup"><span data-stu-id="52375-161">Corresponds to the **WBEM\_METHOD\_EXECUTE** access permission constant.</span></span>

</dd> <dt>

<span data-ttu-id="52375-162"><span id="Full_Write"></span><span id="full_write"></span><span id="FULL_WRITE"></span>完整寫入</span><span class="sxs-lookup"><span data-stu-id="52375-162"><span id="Full_Write"></span><span id="full_write"></span><span id="FULL_WRITE"></span>Full Write</span></span>
</dt> <dd>

<span data-ttu-id="52375-163">允許靜態和動態的 WMI 類別和類別實例的完整讀取、寫入和刪除許可權。</span><span class="sxs-lookup"><span data-stu-id="52375-163">Permits full read, write, and delete access to WMI classes and class instances, both static and dynamic.</span></span> <span data-ttu-id="52375-164">對應至 **WBEM \_ FULL \_ WRITE \_ REP** 存取權限常數。</span><span class="sxs-lookup"><span data-stu-id="52375-164">Corresponds to the **WBEM\_FULL\_WRITE\_REP** access permission constant.</span></span>

</dd> <dt>

<span data-ttu-id="52375-165"><span id="Partial_Write"></span><span id="partial_write"></span><span id="PARTIAL_WRITE"></span>部分寫入</span><span class="sxs-lookup"><span data-stu-id="52375-165"><span id="Partial_Write"></span><span id="partial_write"></span><span id="PARTIAL_WRITE"></span>Partial Write</span></span>
</dt> <dd>

<span data-ttu-id="52375-166">允許靜態 WMI 類別實例的寫入存取權。</span><span class="sxs-lookup"><span data-stu-id="52375-166">Permits write access to static WMI class instances.</span></span> <span data-ttu-id="52375-167">對應至 **WBEM \_ 部分 \_ 寫入 \_ 代表** 存取權限常數。</span><span class="sxs-lookup"><span data-stu-id="52375-167">Corresponds to the **WBEM\_PARTIAL\_WRITE\_REP** access permission constant.</span></span>

</dd> <dt>

<span data-ttu-id="52375-168"><span id="Provider_Write"></span><span id="provider_write"></span><span id="PROVIDER_WRITE"></span>提供者寫入</span><span class="sxs-lookup"><span data-stu-id="52375-168"><span id="Provider_Write"></span><span id="provider_write"></span><span id="PROVIDER_WRITE"></span>Provider Write</span></span>
</dt> <dd>

<span data-ttu-id="52375-169">允許動態 WMI 類別實例的寫入存取權。</span><span class="sxs-lookup"><span data-stu-id="52375-169">Permits write access to dynamic WMI class instances.</span></span> <span data-ttu-id="52375-170">對應至 **WBEM \_ 寫入 \_ 提供者** 存取權限常數。</span><span class="sxs-lookup"><span data-stu-id="52375-170">Corresponds to the **WBEM\_WRITE\_PROVIDER** access permission constant.</span></span>

</dd> <dt>

<span data-ttu-id="52375-171"><span id="Enable_Account"></span><span id="enable_account"></span><span id="ENABLE_ACCOUNT"></span>啟用帳戶</span><span class="sxs-lookup"><span data-stu-id="52375-171"><span id="Enable_Account"></span><span id="enable_account"></span><span id="ENABLE_ACCOUNT"></span>Enable Account</span></span>
</dt> <dd>

<span data-ttu-id="52375-172">允許 WMI 類別實例的讀取權限。</span><span class="sxs-lookup"><span data-stu-id="52375-172">Permits read access to WMI class instances.</span></span> <span data-ttu-id="52375-173">對應至 **WBEM \_ 啟用** 存取權限常數。</span><span class="sxs-lookup"><span data-stu-id="52375-173">Corresponds to the **WBEM\_ENABLE** access permission constant.</span></span>

</dd> <dt>

<span data-ttu-id="52375-174"><span id="Remote_Enable"></span><span id="remote_enable"></span><span id="REMOTE_ENABLE"></span>遠端啟用</span><span class="sxs-lookup"><span data-stu-id="52375-174"><span id="Remote_Enable"></span><span id="remote_enable"></span><span id="REMOTE_ENABLE"></span>Remote Enable</span></span>
</dt> <dd>

<span data-ttu-id="52375-175">允許遠端電腦存取命名空間。</span><span class="sxs-lookup"><span data-stu-id="52375-175">Permits access to the namespace by remote computers.</span></span> <span data-ttu-id="52375-176">對應至 **WBEM \_ 遠端 \_ 訪問** 存取權限常數。</span><span class="sxs-lookup"><span data-stu-id="52375-176">Corresponds to the **WBEM\_REMOTE\_ACCESS** access permission constant.</span></span>

</dd> <dt>

<span data-ttu-id="52375-177"><span id="Read_Security"></span><span id="read_security"></span><span id="READ_SECURITY"></span>讀取安全性</span><span class="sxs-lookup"><span data-stu-id="52375-177"><span id="Read_Security"></span><span id="read_security"></span><span id="READ_SECURITY"></span>Read Security</span></span>
</dt> <dd>

<span data-ttu-id="52375-178">允許對 DACL 設定的唯讀存取。</span><span class="sxs-lookup"><span data-stu-id="52375-178">Permits read-only access to DACL settings.</span></span> <span data-ttu-id="52375-179">對應至 **讀取 \_ 控制** 存取權限常數。</span><span class="sxs-lookup"><span data-stu-id="52375-179">Corresponds to the **READ\_CONTROL** access permission constant.</span></span>

</dd> <dt>

<span data-ttu-id="52375-180"><span id="Edit_Security"></span><span id="edit_security"></span><span id="EDIT_SECURITY"></span>編輯安全性</span><span class="sxs-lookup"><span data-stu-id="52375-180"><span id="Edit_Security"></span><span id="edit_security"></span><span id="EDIT_SECURITY"></span>Edit Security</span></span>
</dt> <dd>

<span data-ttu-id="52375-181">允許 DACL 設定的寫入權限。</span><span class="sxs-lookup"><span data-stu-id="52375-181">Permits write access to DACL settings.</span></span> <span data-ttu-id="52375-182">對應至 **寫入 \_ DAC** 存取權限常數。</span><span class="sxs-lookup"><span data-stu-id="52375-182">Corresponds to the **WRITE\_DAC** access permission constant.</span></span>

</dd> </dl>

## <a name="default-permissions-on-wmi-namespaces"></a><span data-ttu-id="52375-183">WMI 命名空間的預設許可權</span><span class="sxs-lookup"><span data-stu-id="52375-183">Default Permissions on WMI Namespaces</span></span>

<span data-ttu-id="52375-184">預設安全性群組為：</span><span class="sxs-lookup"><span data-stu-id="52375-184">The default security groups are:</span></span>

-   <span data-ttu-id="52375-185">驗證的使用者</span><span class="sxs-lookup"><span data-stu-id="52375-185">Authenticated Users</span></span>
-   <span data-ttu-id="52375-186">LOCAL SERVICE</span><span class="sxs-lookup"><span data-stu-id="52375-186">LOCAL SERVICE</span></span>
-   <span data-ttu-id="52375-187">NETWORK SERVICE</span><span class="sxs-lookup"><span data-stu-id="52375-187">NETWORK SERVICE</span></span>
-   <span data-ttu-id="52375-188">本機電腦上的系統管理員 () </span><span class="sxs-lookup"><span data-stu-id="52375-188">Administrators (on the local computer)</span></span>

<span data-ttu-id="52375-189">已驗證的使用者、本機服務和網路服務的預設存取權限為：</span><span class="sxs-lookup"><span data-stu-id="52375-189">The default access permissions for the Authenticated Users, LOCAL SERVICE, and NETWORK SERVICE are:</span></span>

-   <span data-ttu-id="52375-190">執行方法</span><span class="sxs-lookup"><span data-stu-id="52375-190">Execute Methods</span></span>
-   <span data-ttu-id="52375-191">全部寫入</span><span class="sxs-lookup"><span data-stu-id="52375-191">Full Write</span></span>
-   <span data-ttu-id="52375-192">啟用帳戶</span><span class="sxs-lookup"><span data-stu-id="52375-192">Enable Account</span></span>

<span data-ttu-id="52375-193">Administrators 群組中的帳戶擁有擁有權限，包括編輯安全描述項。</span><span class="sxs-lookup"><span data-stu-id="52375-193">Accounts in the Administrators group have all rights available to them, including editing security descriptors.</span></span> <span data-ttu-id="52375-194">不過，由於使用者帳戶控制 (UAC) ，因此 WMI 控制項或腳本必須以更高的安全性執行。</span><span class="sxs-lookup"><span data-stu-id="52375-194">However, because of User Account Control (UAC), the WMI Control or the script must be running at elevated security.</span></span> <span data-ttu-id="52375-195">如需詳細資訊，請參閱 [使用者帳戶控制和 WMI](user-account-control-and-wmi.md)。</span><span class="sxs-lookup"><span data-stu-id="52375-195">For more information, see [User Account Control and WMI](user-account-control-and-wmi.md).</span></span>

<span data-ttu-id="52375-196">有時腳本或應用程式必須啟用系統管理員許可權（例如 **SeSecurityPrivilege**），才能執行作業。</span><span class="sxs-lookup"><span data-stu-id="52375-196">Sometimes a script or application must enable an administrator privilege, such as **SeSecurityPrivilege**, to carry out an operation.</span></span> <span data-ttu-id="52375-197">例如，腳本可以執行 [**Win32 \_ printer**](/windows/desktop/CIMWin32Prov/win32-printer)類別的 [**GetSecurityDescriptor**](/windows/desktop/CIMWin32Prov/getsecuritydescriptor-method-in-class-win32-printer)方法，而不需要 **SeSecurityPrivilege** ，並且在印表機物件 [*安全描述項*](/windows/desktop/SecGloss/s-gly) [*(DACL) 的任意存取控制清單*](/windows/desktop/SecGloss/d-gly)中取得安全性資訊。</span><span class="sxs-lookup"><span data-stu-id="52375-197">For example, a script can execute the [**GetSecurityDescriptor**](/windows/desktop/CIMWin32Prov/getsecuritydescriptor-method-in-class-win32-printer) method of the [**Win32\_Printer**](/windows/desktop/CIMWin32Prov/win32-printer) class without **SeSecurityPrivilege** and get the security information in the [*discretionary access control list (DACL)*](/windows/desktop/SecGloss/d-gly) of the printer object [*security descriptor*](/windows/desktop/SecGloss/s-gly).</span></span> <span data-ttu-id="52375-198">不過，除非 **SeSecurityPrivilege** 許可權可供帳戶使用且已啟用，否則 SACL 資訊不會傳回給腳本。</span><span class="sxs-lookup"><span data-stu-id="52375-198">However, the SACL information is not returned to the script unless the **SeSecurityPrivilege** privilege is available and enabled for the account.</span></span> <span data-ttu-id="52375-199">如果帳戶沒有可用的許可權，則無法啟用。</span><span class="sxs-lookup"><span data-stu-id="52375-199">If the account does not have the privilege available, then it cannot be enabled.</span></span> <span data-ttu-id="52375-200">如需詳細資訊，請參閱 [執行特殊許可權作業](executing-privileged-operations.md)。</span><span class="sxs-lookup"><span data-stu-id="52375-200">For more information, see [Executing Privileged Operations](executing-privileged-operations.md).</span></span>

## <a name="related-topics"></a><span data-ttu-id="52375-201">相關主題</span><span class="sxs-lookup"><span data-stu-id="52375-201">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="52375-202">關於 WMI</span><span class="sxs-lookup"><span data-stu-id="52375-202">About WMI</span></span>](about-wmi.md)
</dt> </dl>

 

 
