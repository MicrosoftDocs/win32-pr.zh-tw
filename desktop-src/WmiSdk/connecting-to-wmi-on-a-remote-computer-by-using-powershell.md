---
description: 使用 PowerShell 從遠端連線至 WMI
ms.assetid: 9a06f0c3-2845-48aa-9988-79cc4607ce19
ms.tgt_platform: multiple
title: 使用 PowerShell 從遠端連線至 WMI
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 7a2bb1ad982a20a10dbadd89856d118f1be9bd82
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/07/2021
ms.locfileid: "103692352"
---
# <a name="connecting-to-wmi-remotely-with-powershell"></a><span data-ttu-id="cc7c7-103">使用 PowerShell 從遠端連線至 WMI</span><span class="sxs-lookup"><span data-stu-id="cc7c7-103">Connecting to WMI Remotely with PowerShell</span></span>

<span data-ttu-id="cc7c7-104">Windows PowerShell 提供簡單的機制，以連接到遠端電腦上 Windows Management Instrumentation (WMI) 。</span><span class="sxs-lookup"><span data-stu-id="cc7c7-104">Windows PowerShell provides a simple mechanism to connect to Windows Management Instrumentation (WMI) on a remote computer.</span></span> <span data-ttu-id="cc7c7-105">WMI 中的遠端連線受 [Windows 防火牆](/previous-versions/windows/it-pro/windows-server-2008-R2-and-2008/cc754274(v=ws.11))、DCOM 設定以及 [使用者帳戶控制 (UAC) ](/previous-versions/aa905108(v=msdn.10))的影響。</span><span class="sxs-lookup"><span data-stu-id="cc7c7-105">Remote connections in WMI are affected by the [Windows Firewall](/previous-versions/windows/it-pro/windows-server-2008-R2-and-2008/cc754274(v=ws.11)), DCOM settings, and [User Account Control (UAC)](/previous-versions/aa905108(v=msdn.10)).</span></span> <span data-ttu-id="cc7c7-106">如需有關設定遠端連線的詳細資訊，請參閱 [從 Windows Vista 開始遠端連線至 WMI](connecting-to-wmi-remotely-starting-with-vista.md)。</span><span class="sxs-lookup"><span data-stu-id="cc7c7-106">For more information about configuring remote connections, see [Connecting to WMI Remotely Starting with Windows Vista](connecting-to-wmi-remotely-starting-with-vista.md).</span></span>

<span data-ttu-id="cc7c7-107">本主題中的範例是 [以 Vbscript 連接到遠端電腦上的 WMI](connecting-to-wmi-on-a-remote-computer.md)為基礎。</span><span class="sxs-lookup"><span data-stu-id="cc7c7-107">The examples in this topic are based on the VBScripts from [Connecting to WMI on a Remote Computer](connecting-to-wmi-on-a-remote-computer.md).</span></span> <span data-ttu-id="cc7c7-108">本主題中的所有範例都會使用 [>get-wmiobject 指令程式](/previous-versions//dd315295(v=technet.10)) 。</span><span class="sxs-lookup"><span data-stu-id="cc7c7-108">All of the examples in this topic use the [Get-WmiObject](/previous-versions//dd315295(v=technet.10)) cmdlet.</span></span> <span data-ttu-id="cc7c7-109">如需詳細資訊，請參閱 [>get-wmiobject](/previous-versions//dd315295(v=technet.10))。</span><span class="sxs-lookup"><span data-stu-id="cc7c7-109">For more information, see [Get-WmiObject](/previous-versions//dd315295(v=technet.10)).</span></span>

## <a name="windows-powershell-examples"></a><span data-ttu-id="cc7c7-110">Windows PowerShell 範例</span><span class="sxs-lookup"><span data-stu-id="cc7c7-110">Windows PowerShell examples</span></span>

<span data-ttu-id="cc7c7-111">建立遠端電腦的連線時，使用者可以指定連線資訊，例如遠端電腦名稱稱、認證，以及連線的驗證層級。</span><span class="sxs-lookup"><span data-stu-id="cc7c7-111">When creating a connection to a remote computer, a user can specify the connection information such as the remote computer name, credentials, and the authentication level for the connection.</span></span> <span data-ttu-id="cc7c7-112">下列範例說明如何使用不同的認證組來連接到遠端電腦，以及如何存取 WMI 資訊。</span><span class="sxs-lookup"><span data-stu-id="cc7c7-112">The following examples illustrate how to connect to a remote computer by using different sets of credentials and how to access WMI information.</span></span>

<span data-ttu-id="cc7c7-113">下列 Windows PowerShell 範例會示範如何設定模擬等級：</span><span class="sxs-lookup"><span data-stu-id="cc7c7-113">The following Windows PowerShell example shows setting the impersonation level:</span></span>


```PowerShell

Get-WmiObject -Namespace "root\cimv2" -Class Win32_Process -Impersonation 3 -ComputerName Computer_B
```



<span data-ttu-id="cc7c7-114">在上述範例中，使用者會使用與登入 (網域和使用者名稱) 相同的認證，連接到遠端電腦。</span><span class="sxs-lookup"><span data-stu-id="cc7c7-114">In the preceding example, the user connects to a remote computer by using the same credentials (domain and user name) that they logged on with.</span></span> <span data-ttu-id="cc7c7-115">使用者也要求使用模擬。</span><span class="sxs-lookup"><span data-stu-id="cc7c7-115">The user also requested to use impersonation.</span></span> <span data-ttu-id="cc7c7-116">與原始 VBScript 範例不同的是，不需要使用「標記」字串，因為模擬層級是由「模擬」屬性所設定。</span><span class="sxs-lookup"><span data-stu-id="cc7c7-116">Unlike the original VBScript example, a moniker string is not needed because the impersonation level is set by the "Impersonation" property.</span></span> <span data-ttu-id="cc7c7-117">根據預設，模擬層級設定為 3 (模擬) 。</span><span class="sxs-lookup"><span data-stu-id="cc7c7-117">By default, the impersonation level is set to 3 (Impersonate).</span></span>

<span data-ttu-id="cc7c7-118">此範例會列出在遠端電腦上執行的 [**Win32 \_ 進程**](/windows/desktop/CIMWin32Prov/win32-process) 類別的所有實例。</span><span class="sxs-lookup"><span data-stu-id="cc7c7-118">The example lists all the instances of the [**Win32\_Process**](/windows/desktop/CIMWin32Prov/win32-process) class that are running on remote computer.</span></span>

> [!Note]  
> <span data-ttu-id="cc7c7-119">您應該指定要在遠端電腦上連接的 WMI 命名空間，因為不同電腦上的預設命名空間可能不相同。</span><span class="sxs-lookup"><span data-stu-id="cc7c7-119">You should specify the WMI namespace to connect to on the remote computer because it is possible that the default namespace is not the same on different computers.</span></span>

 

<span data-ttu-id="cc7c7-120">下列 Windows PowerShell 範例示範如何使用不同的認證連接到遠端電腦，以及如何將模擬等級設定為3，也就是模擬：</span><span class="sxs-lookup"><span data-stu-id="cc7c7-120">The following Windows PowerShell example shows how to connect to a remote computer with different credentials and to set the impersonation level to 3, which is Impersonate:</span></span>


```PowerShell

$Computer = "atl-dc-01"

Get-WmiObject -Namespace "root\cimv2" -Class Win32_Process -Impersonation 3 -Credential `
FABRIKAM\administrator -ComputerName $Computer
```



<span data-ttu-id="cc7c7-121">在上述範例中，電腦名稱稱已指派給 $Computer 變數。</span><span class="sxs-lookup"><span data-stu-id="cc7c7-121">In the preceding example, the computer name was assigned to the $Computer variable.</span></span> <span data-ttu-id="cc7c7-122">使用者會使用特定的認證來連線到遠端電腦 (網域和使用者名稱) ，並要求驗證層級的模擬。</span><span class="sxs-lookup"><span data-stu-id="cc7c7-122">The user connects to a remote computer by using specific credentials (domain and user name) and requests impersonation for the authentication level.</span></span>

> [!Note]  
> <span data-ttu-id="cc7c7-123">使用「音符號」（ (\`) ）來表示分行符號。</span><span class="sxs-lookup"><span data-stu-id="cc7c7-123">The grave-accent character (\`) is used to indicate a line break.</span></span> <span data-ttu-id="cc7c7-124">它相當於 VBScript 中 () 的底線字元 \_ 。</span><span class="sxs-lookup"><span data-stu-id="cc7c7-124">It is equivalent to the underscore character (\_) in VBScript.</span></span>

 

<span data-ttu-id="cc7c7-125">下列 Windows PowerShell 範例會在每一部電腦上建立遠端電腦名稱稱陣列，然後顯示隨插即用裝置（ [**Win32 \_ PnPEntity**](/windows/desktop/CIMWin32Prov/win32-pnpentity)的實例）的名稱，以連接到同一網域中的一組遠端電腦：</span><span class="sxs-lookup"><span data-stu-id="cc7c7-125">The following Windows PowerShell example connects to a group of remote computers in the same domain by creating an array of remote computer names and then displaying names of the Plug and Play devices—instances of [**Win32\_PnPEntity**](/windows/desktop/CIMWin32Prov/win32-pnpentity)—on each computer:</span></span>


```PowerShell
$ArrComputers = "Computer1", "Computer2", "Computer3"
foreach ($Computer in $ArrComputers) 
{
write-host ""
write-host "===================================="
write-host "Computer: $Computer"
write-host "===================================="

write-host "-----------------------------------"
write-host "Win32_PnPEntity instance"
write-host "-----------------------------------"

$ColItems = Get-WmiObject -Class Win32_PnPEntity -Namespace "root\cimv2" -Computer $Computer
$ColItems[0..47] | Format-List Name, Status
}
```



> [!Note]  
> <span data-ttu-id="cc7c7-126">若要執行上述 Windows PowerShell 腳本，您必須是遠端電腦上的系統管理員。</span><span class="sxs-lookup"><span data-stu-id="cc7c7-126">To run the preceding Windows PowerShell script, you must be an administrator on the remote computers.</span></span> <span data-ttu-id="cc7c7-127">此外，與上述範例相關，請注意下列事項：</span><span class="sxs-lookup"><span data-stu-id="cc7c7-127">Also, relating to the preceding example, note the following:</span></span>

 

-   <span data-ttu-id="cc7c7-128">陣列中的電腦名稱稱必須以引號括住，因為它們是字串。</span><span class="sxs-lookup"><span data-stu-id="cc7c7-128">The computer names in the array must be enclosed in quotation marks because they are strings.</span></span>
-   <span data-ttu-id="cc7c7-129">[>get-wmiobject](/previous-versions//dd315295(v=technet.10))所傳回的物件會指派給 $ColItems 變數。</span><span class="sxs-lookup"><span data-stu-id="cc7c7-129">The objects returned by the [Get-WmiObject](/previous-versions//dd315295(v=technet.10)) are assigned to the $ColItems variable.</span></span>
-   <span data-ttu-id="cc7c7-130">範圍運算子會 \[ \] 將隨插即用裝置的清單限制為48個實例。</span><span class="sxs-lookup"><span data-stu-id="cc7c7-130">The range operator \[\] limited the list of Plug and Play devices to 48 instances.</span></span> <span data-ttu-id="cc7c7-131">如需詳細資訊，請參閱 [關於 \_ 運算子](/previous-versions//dd347588(v=technet.10))。</span><span class="sxs-lookup"><span data-stu-id="cc7c7-131">For more information, see [About\_Operators](/previous-versions//dd347588(v=technet.10)).</span></span>
-   <span data-ttu-id="cc7c7-132">" \| " 是管線字元。</span><span class="sxs-lookup"><span data-stu-id="cc7c7-132">The "\|" is the pipeline character.</span></span> <span data-ttu-id="cc7c7-133">ColItems 傳回的物件會傳送至 [格式清單]( /previous-versions//dd347700(v=technet.10)) Cmdlet。</span><span class="sxs-lookup"><span data-stu-id="cc7c7-133">The object returned by ColItems is sent to the [Format-List]( /previous-versions//dd347700(v=technet.10)) cmdlet.</span></span>

<span data-ttu-id="cc7c7-134">下列 Windows PowerShell 範例可讓您連接到不同網域上的遠端電腦。</span><span class="sxs-lookup"><span data-stu-id="cc7c7-134">The following Windows PowerShell example enables you to connect to a remote computer on a different domain.</span></span> <span data-ttu-id="cc7c7-135">此範例也會顯示遠端電腦上 [**Win32 \_ 進程**](/windows/desktop/CIMWin32Prov/win32-process) 實例的處理常式名稱。</span><span class="sxs-lookup"><span data-stu-id="cc7c7-135">This example also displays the process names for instances of [**Win32\_Process**](/windows/desktop/CIMWin32Prov/win32-process) on the remote computer.</span></span>


```PowerShell
$Computer = "FullComputerName" 
$Domain = "DOMAIN"
$Credential = Get-Credential
$ColItems = Get-WmiObject -Class Win32_Process -Authority "ntlmdomain:$Domain" `
-Credential $Credential -Locale "MS_409" -Namespace "root\cimv2"  -ComputerName $Computer

foreach ($ObjItem in $colItems) 
{
write-host "Process Name:" $ObjItem.name
}
```



> [!Note]  
> <span data-ttu-id="cc7c7-136">若要執行上述 Windows PowerShell 腳本，您必須是遠端電腦上的系統管理員。</span><span class="sxs-lookup"><span data-stu-id="cc7c7-136">To run the preceding Windows PowerShell script, you must be an administrator on the remote computer.</span></span>

 

<span data-ttu-id="cc7c7-137">在上述範例中，使用者會連接到不同網域的遠端電腦，並指定慣用的地區設定。</span><span class="sxs-lookup"><span data-stu-id="cc7c7-137">In the preceding example, the user connects to a remote computer on a different domain and specifies a preferred locale.</span></span> <span data-ttu-id="cc7c7-138">[取得認證](/previous-versions//dd315327(v=technet.10))命令會要求使用者的認證，並將認證指派給物件。</span><span class="sxs-lookup"><span data-stu-id="cc7c7-138">The [Get-Credential](/previous-versions//dd315327(v=technet.10)) command requests the user's credentials and assigns the credentials to an object.</span></span> <span data-ttu-id="cc7c7-139">此範例也會列出電腦上執行的 [**Win32 \_ 進程**](/windows/desktop/CIMWin32Prov/win32-process) 類別的實例名稱。</span><span class="sxs-lookup"><span data-stu-id="cc7c7-139">The example also lists the names of instances of the [**Win32\_Process**](/windows/desktop/CIMWin32Prov/win32-process) class that are running on the computer.</span></span>

## <a name="related-topics"></a><span data-ttu-id="cc7c7-140">相關主題</span><span class="sxs-lookup"><span data-stu-id="cc7c7-140">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="cc7c7-141">連接至遠端電腦上的 WMI</span><span class="sxs-lookup"><span data-stu-id="cc7c7-141">Connecting to WMI on a Remote Computer</span></span>](connecting-to-wmi-on-a-remote-computer.md)
</dt> </dl>

 

 
