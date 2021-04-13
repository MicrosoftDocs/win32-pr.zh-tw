---
description: 當您在從遠端系統取得資料的本機系統上執行腳本時，WMI 會將您的認證提供給遠端系統上的資料提供者。
ms.assetid: e27ff207-b067-47df-9706-e8af51646d28
ms.tgt_platform: multiple
title: 使用 WMI 委派
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 1e8a624f3d437d977ff73b3854a59cfd634350e7
ms.sourcegitcommit: b7a1da2711221fa99072079bf52399cbdfc6bd9d
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 03/05/2021
ms.locfileid: "104386328"
---
# <a name="delegating-with-wmi"></a><span data-ttu-id="9602d-103">使用 WMI 委派</span><span class="sxs-lookup"><span data-stu-id="9602d-103">Delegating with WMI</span></span>

<span data-ttu-id="9602d-104">當您在從遠端系統取得資料的本機系統上執行腳本時，WMI 會將您的認證提供給遠端系統上的資料提供者。</span><span class="sxs-lookup"><span data-stu-id="9602d-104">When you run a script on a local system that obtains data from a remote system, WMI supplies your credentials to the provider of the data on the remote system.</span></span> <span data-ttu-id="9602d-105">這只需要模擬的模擬層 **級，因為** 只需要一個網路躍點。</span><span class="sxs-lookup"><span data-stu-id="9602d-105">This requires only an impersonation level of **Impersonate**, because only one network hop is required.</span></span> <span data-ttu-id="9602d-106">但是，如果腳本連接至遠端系統上的 WMI，並嘗試在其他遠端系統上開啟記錄檔，則腳本會失敗，除非模擬層級為 **委派**。</span><span class="sxs-lookup"><span data-stu-id="9602d-106">However, if the script connects to WMI on the remote system and attempts to open a log file on an additional remote system, then the script fails unless the impersonation level is **Delegate**.</span></span> <span data-ttu-id="9602d-107">任何牽涉到一個以上網路躍點的作業都需要 **委派** 模擬等級。</span><span class="sxs-lookup"><span data-stu-id="9602d-107">**Delegate** impersonation level is required by any operation that involves more than one network hop.</span></span> <span data-ttu-id="9602d-108">如需 WMI 中 DCOM 安全性的詳細資訊，請參閱 [設定用戶端應用程式處理安全性](setting-client-application-process-security.md)。</span><span class="sxs-lookup"><span data-stu-id="9602d-108">For more information about DCOM security in WMI, see [Setting Client Application Process Security](setting-client-application-process-security.md).</span></span> <span data-ttu-id="9602d-109">如需兩部電腦之間的單一網路躍點連線的詳細資訊，請參閱 [連接到遠端電腦上的 WMI](connecting-to-wmi-on-a-remote-computer.md)。</span><span class="sxs-lookup"><span data-stu-id="9602d-109">For more information about a one-network hop connection between two computers, see [Connecting to WMI on a Remote Computer](connecting-to-wmi-on-a-remote-computer.md).</span></span>

<span data-ttu-id="9602d-110">**使用委派透過另一部電腦連接到電腦**</span><span class="sxs-lookup"><span data-stu-id="9602d-110">**To use delegation to connect to a computer through another computer**</span></span>

1.  <span data-ttu-id="9602d-111">在 Active Directory (**Active Directory 消費者和電腦** 在網域控制站 **主控台\*\*\*\*管理** 工作) 中啟用委派。</span><span class="sxs-lookup"><span data-stu-id="9602d-111">Enable delegation in Active Directory (**Active Directory Users and Computers** in **Control Panel** **Administrative Tasks**) on the domain controller.</span></span> <span data-ttu-id="9602d-112">遠端系統上的帳戶必須標示為 **受信任以進行委派** ，而且本機系統上的帳戶不得標示為「 **帳戶必須機密」且無法委派**。</span><span class="sxs-lookup"><span data-stu-id="9602d-112">The account on the remote system must be marked as **Trusted for delegation** and the account on the local system must not be marked as **Account is sensitive and cannot be delegated**.</span></span> <span data-ttu-id="9602d-113">本機系統、遠端系統和網域控制站必須是相同網域或受信任網域中的成員。</span><span class="sxs-lookup"><span data-stu-id="9602d-113">the local system, the remote system, and the domain controller must be members of the same domain or in trusted domains.</span></span>

    <span data-ttu-id="9602d-114">**注意**  使用委派會有安全性風險，因為它可讓您直接控制外部的進程使用您的認證。</span><span class="sxs-lookup"><span data-stu-id="9602d-114">**Note**  Using delegation is a security risk because it gives processes outside of your direct control the ability to use your credentials.</span></span>

2.  <span data-ttu-id="9602d-115">以下列方式修改您的程式碼，以表示您想要使用委派。</span><span class="sxs-lookup"><span data-stu-id="9602d-115">Modify your code in the following manner to indicate that you want to use delegation.</span></span>

    <dl> <dt>

    <span data-ttu-id="9602d-116"><span id="PowerShell"></span><span id="powershell"></span><span id="POWERSHELL"></span>PowerShell</span><span class="sxs-lookup"><span data-stu-id="9602d-116"><span id="PowerShell"></span><span id="powershell"></span><span id="POWERSHELL"></span>PowerShell</span></span>
    </dt> <dd>

    <span data-ttu-id="9602d-117">將 WMI Cmdlet 上的 *-* 模擬參數設定為 **委派**。</span><span class="sxs-lookup"><span data-stu-id="9602d-117">Set the *-Impersonation* parameter on the WMI cmdlet to **Delegate**.</span></span>

    </dd> <dt>

    <span data-ttu-id="9602d-118"><span id="VBScript"></span><span id="vbscript"></span><span id="VBSCRIPT"></span>VBScript</span><span class="sxs-lookup"><span data-stu-id="9602d-118"><span id="VBScript"></span><span id="vbscript"></span><span id="VBSCRIPT"></span>VBScript</span></span>
    </dt> <dd>

    <span data-ttu-id="9602d-119">將 *impersonationLevel* 參數設定為在 [wbemscripting.swbemlocator. ConnectServer](swbemlocator-connectserver.md)或在 [標記](constructing-a-moniker-string.md)字串中 **委派** 的呼叫中 **委派**。</span><span class="sxs-lookup"><span data-stu-id="9602d-119">Set the *impersonationLevel* parameter to **Delegate** in the call to [SWbemLocator.ConnectServer](swbemlocator-connectserver.md) or **Delegate** in the [moniker](constructing-a-moniker-string.md) string.</span></span> <span data-ttu-id="9602d-120">您也可以在 [**SWbemSecurity**](swbemsecurity.md)物件中設定模擬。</span><span class="sxs-lookup"><span data-stu-id="9602d-120">You can also set the impersonation in a [**SWbemSecurity**](swbemsecurity.md)object.</span></span>

    </dd> <dt>

    <span data-ttu-id="9602d-121"><span id="C__"></span><span id="c__"></span>C++</span><span class="sxs-lookup"><span data-stu-id="9602d-121"><span id="C__"></span><span id="c__"></span>C++</span></span>
    </dt> <dd>

    <span data-ttu-id="9602d-122">在 [**CoInitializeSecurity**](/windows/win32/api/combaseapi/nf-combaseapi-coinitializesecurity)或 [**CoSetProxyBlanket**](/windows/win32/api/combaseapi/nf-combaseapi-cosetproxyblanket)的呼叫中，將模擬等級參數設定為 **RPC \_ C \_ IMP \_ 層級 \_ 委派**。</span><span class="sxs-lookup"><span data-stu-id="9602d-122">Set the impersonation level parameter to **RPC\_C\_IMP\_LEVEL\_DELEGATE** in the call to [**CoInitializeSecurity**](/windows/win32/api/combaseapi/nf-combaseapi-coinitializesecurity) or [**CoSetProxyBlanket**](/windows/win32/api/combaseapi/nf-combaseapi-cosetproxyblanket).</span></span> <span data-ttu-id="9602d-123">如需有關何時進行這些呼叫的詳細資訊，請參閱 [初始化 WMI 應用程式的 COM](initializing-com-for-a-wmi-application.md)。</span><span class="sxs-lookup"><span data-stu-id="9602d-123">For more information about when to make these calls, see [Initializing COM for a WMI Application](initializing-com-for-a-wmi-application.md).</span></span>

    <span data-ttu-id="9602d-124">若要在 c + + 中將用戶端身分識別傳遞給遠端 COM 伺服器，請在呼叫 [**CoSetProxyBlanket**](/windows/win32/api/combaseapi/nf-combaseapi-cosetproxyblanket)時設定掩飾。</span><span class="sxs-lookup"><span data-stu-id="9602d-124">To pass the client identity to remote COM servers in C++, set cloaking in the call to [**CoSetProxyBlanket**](/windows/win32/api/combaseapi/nf-combaseapi-cosetproxyblanket).</span></span> <span data-ttu-id="9602d-125">如需詳細資訊，請參閱 [掩蓋](../com/cloaking.md)。</span><span class="sxs-lookup"><span data-stu-id="9602d-125">For more information, see [Cloaking](../com/cloaking.md).</span></span>

    </dd> </dl>

## <a name="examples"></a><span data-ttu-id="9602d-126">範例</span><span class="sxs-lookup"><span data-stu-id="9602d-126">Examples</span></span>

<span data-ttu-id="9602d-127">下列程式碼範例會示範將模擬設定為 **委派** 的標記字串。</span><span class="sxs-lookup"><span data-stu-id="9602d-127">The following code example shows a moniker string that sets the impersonation to **Delegate**.</span></span> <span data-ttu-id="9602d-128">請注意，授權單位必須設定為 Kerberos。</span><span class="sxs-lookup"><span data-stu-id="9602d-128">Be aware that the authority must be set to Kerberos.</span></span>


```vb
set objWMIServices = Getobject("winmgmts:{impersonationLevel=Delegate,authority=kerberos:MyDomain\Computer_B}!\\ComputerB\Root\CIMv2")
```



<span data-ttu-id="9602d-129">下列程式碼範例將示範如何使用 [**Wbemscripting.swbemlocator ConnectServer**](swbemlocator-connectserver.md)將模擬設定為 4) 的 **值 (。**</span><span class="sxs-lookup"><span data-stu-id="9602d-129">The following code example shows how to set impersonation to **Delegate** (a value of 4) using [**SWbemLocator.ConnectServer**](swbemlocator-connectserver.md).</span></span>


```vb
Set objLocator = CreateObject("WbemScripting.SWbemLocator")
Set objWMIService = objLocator.ConnectServer(Computer_B, _
                                             "Root\CIMv2", _
                                             AdminAccount, _
                                             MyPassword, _
                                             "kerberos:Domain\Computer_B")
objWMIService.Security_.ImpersonationLevel = 4
```



## <a name="related-topics"></a><span data-ttu-id="9602d-130">相關主題</span><span class="sxs-lookup"><span data-stu-id="9602d-130">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="9602d-131">保護遠端 WMI 連接</span><span class="sxs-lookup"><span data-stu-id="9602d-131">Securing a Remote WMI Connection</span></span>](securing-a-remote-wmi-connection.md)
</dt> <dt>

[<span data-ttu-id="9602d-132">使用 WMI 從遠端建立進程</span><span class="sxs-lookup"><span data-stu-id="9602d-132">Creating Processes Remotely with WMI</span></span>](creating-processes-remotely.md)
</dt> </dl>

 

 
