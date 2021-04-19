---
description: 從 Windows Vista 開始，服務控制管理員 (SCM) 支援使用傳輸控制)  (通訊協定的遠端程序呼叫， (RPC/NP) 的具名管道。
ms.assetid: c51732f6-c22f-4726-afaa-13a8948ac44f
title: 服務和 RPC/TCP
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 3fdb2ef3b21f280ba4e5078d302813de41a5a43a
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/08/2021
ms.locfileid: "106987355"
---
# <a name="services-and-rpctcp"></a><span data-ttu-id="e1079-103">服務和 RPC/TCP</span><span class="sxs-lookup"><span data-stu-id="e1079-103">Services and RPC/TCP</span></span>

<span data-ttu-id="e1079-104">從 Windows Vista 開始，服務控制管理員 (SCM) 支援使用傳輸控制)  (通訊協定的遠端程序呼叫， (RPC/NP) 的具名管道。</span><span class="sxs-lookup"><span data-stu-id="e1079-104">Starting with Windows Vista, the service control manager (SCM) supports remote procedure calls over both Transmission Control Protocol (RPC/TCP) and named pipes (RPC/NP).</span></span> <span data-ttu-id="e1079-105">用戶端 SCM 函式預設會使用 RPC/TCP。</span><span class="sxs-lookup"><span data-stu-id="e1079-105">Client-side SCM functions use RPC/TCP by default.</span></span>

<span data-ttu-id="e1079-106">RPC/TCP 適用于從遠端使用 SCM 功能的大部分應用程式，例如遠端系統管理或監視工具。</span><span class="sxs-lookup"><span data-stu-id="e1079-106">RPC/TCP is appropriate for most applications that use SCM functions remotely, such as remote administration or monitoring tools.</span></span> <span data-ttu-id="e1079-107">不過，針對相容性和效能，有些應用程式可能需要藉由設定本主題中所述的登錄值來停用 RPC/TCP。</span><span class="sxs-lookup"><span data-stu-id="e1079-107">However, for compatibility and performance, some applications might need to disable RPC/TCP by setting the registry values described in this topic.</span></span>

<span data-ttu-id="e1079-108">當服務呼叫遠端 SCM 函數時，用戶端 SCM 會先嘗試使用 RPC/TCP 來與伺服器端 SCM 通訊。</span><span class="sxs-lookup"><span data-stu-id="e1079-108">When a service calls a remote SCM function, the client-side SCM first attempts to use RPC/TCP to communicate with the server-side SCM.</span></span> <span data-ttu-id="e1079-109">如果伺服器執行的是支援 RPC/TCP 的 Windows 版本，並允許 RPC/TCP 流量，RPC/TCPP 連接將會成功。</span><span class="sxs-lookup"><span data-stu-id="e1079-109">If the server is running a version of Windows that supports RPC/TCP and allows RPC/TCP traffic, the RPC/TCPP connection will succeed.</span></span> <span data-ttu-id="e1079-110">如果伺服器執行的 Windows 版本不支援 RPC/TCP，或支援 RPC/TCP，但在只允許具名管道流量的防火牆後方運作，則 RPC/TCP 連接逾時，且 SCM 會重試與 RPC/NP 的連接。</span><span class="sxs-lookup"><span data-stu-id="e1079-110">If the server is running a version of Windows that does not support RPC/TCP, or supports RPC/TCP but is operating behind a firewall which allows only named pipe traffic, the RPC/TCP connection times out and the SCM retries the connection with RPC/NP.</span></span> <span data-ttu-id="e1079-111">最後，這將會成功，但可能需要一些時間 (通常超過20秒的) ，導致 [**OpenSCManager**](/windows/desktop/api/Winsvc/nf-winsvc-openscmanagera) 函式顯示為封鎖。</span><span class="sxs-lookup"><span data-stu-id="e1079-111">This will succeed eventually but can take some time (typically more than 20 seconds), causing the [**OpenSCManager**](/windows/desktop/api/Winsvc/nf-winsvc-openscmanagera) function to appear blocked.</span></span>

<span data-ttu-id="e1079-112">TCP 不包含使用 **net use** 命令指定的使用者認證。</span><span class="sxs-lookup"><span data-stu-id="e1079-112">TCP does not carry user credentials specified with a **net use** command.</span></span> <span data-ttu-id="e1079-113">因此，如果啟用了 RPC/TCP，並使用 **sc.exe** 來嘗試存取指定的服務，則命令可能會失敗並拒絕存取。</span><span class="sxs-lookup"><span data-stu-id="e1079-113">Therefore, if RPC/TCP is enabled and **sc.exe** is used to attempt to access the specified service, the command could fail with access denied.</span></span> <span data-ttu-id="e1079-114">在用戶端上停用 RPC/TCP 會導致 **sc.exe** 命令使用具有使用者認證的具名管道，因此命令將會成功。</span><span class="sxs-lookup"><span data-stu-id="e1079-114">Disabling RPC/TCP on the client side causes the **sc.exe** command to use a named pipe that does carry user credentials, so the command will succeed.</span></span> <span data-ttu-id="e1079-115">如需 sc.exe 的詳細資訊，請參閱 [使用 SC 控制服務](controlling-a-service-using-sc.md)。</span><span class="sxs-lookup"><span data-stu-id="e1079-115">For information about sc.exe, see [Controlling a Service Using SC](controlling-a-service-using-sc.md).</span></span>

> [!Note]  
> <span data-ttu-id="e1079-116">服務不應該將明確的認證提供給 **net use** 命令，因為這些認證可能會在服務界限之外不慎共用。</span><span class="sxs-lookup"><span data-stu-id="e1079-116">A service should not provide explicit credentials to a **net use** command, because those credentials might be inadvertently shared outside of the service boundaries.</span></span> <span data-ttu-id="e1079-117">相反地，服務應該使用 [用戶端](/windows/desktop/SecAuthZ/client-impersonation) 模擬來模擬使用者。</span><span class="sxs-lookup"><span data-stu-id="e1079-117">Instead, the service should use [client impersonation](/windows/desktop/SecAuthZ/client-impersonation) to impersonate the user.</span></span>

 

### <a name="rpctcp-registry-values"></a><span data-ttu-id="e1079-118">RPC/TCP 登錄值</span><span class="sxs-lookup"><span data-stu-id="e1079-118">RPC/TCP Registry Values</span></span>

<span data-ttu-id="e1079-119">RPC/TCP 是由 **SCMApiConnectionParam**、 **DisableRPCOverTCP** 和 **DisableRemoteScmEndpoints** 登錄值所控制，這些值全都位於 **HKEY \_ 本機 \_ 電腦** \\ **系統** \\ **CurrentControlSet** \\ **Control** 機碼下。</span><span class="sxs-lookup"><span data-stu-id="e1079-119">RPC/TCP is controlled by the **SCMApiConnectionParam**, **DisableRPCOverTCP**, and **DisableRemoteScmEndpoints** registry values, which are all under the **HKEY\_LOCAL\_MACHINE**\\**SYSTEM**\\**CurrentControlSet**\\**Control** key.</span></span> <span data-ttu-id="e1079-120">所有這些值都有 REG \_ DWORD 資料類型。</span><span class="sxs-lookup"><span data-stu-id="e1079-120">All of these values have a REG\_DWORD data type.</span></span> <span data-ttu-id="e1079-121">下列程式示範如何使用這些登錄值來控制 RPC/TCP。</span><span class="sxs-lookup"><span data-stu-id="e1079-121">The following procedures show how to use these registry values to control RPC/TCP.</span></span>

<span data-ttu-id="e1079-122">下列程式描述如何在用戶端上停用 RPC/TCP。</span><span class="sxs-lookup"><span data-stu-id="e1079-122">The following procedure describes how to disable RPC/TCP on the client side.</span></span>

<span data-ttu-id="e1079-123">**若要在用戶端上停用 RPC/TCP**</span><span class="sxs-lookup"><span data-stu-id="e1079-123">**To disable RPC/TCP on the client side**</span></span>

1.  <span data-ttu-id="e1079-124">將 **SCMApiConnectionParam** 登錄值與 mask 值0x80000000 合併。</span><span class="sxs-lookup"><span data-stu-id="e1079-124">Combine the **SCMApiConnectionParam** registry value with the mask value 0x80000000.</span></span>
2.  <span data-ttu-id="e1079-125">重新開機呼叫 [**OpenSCManager**](/windows/desktop/api/Winsvc/nf-winsvc-openscmanagera) 函式的應用程式。</span><span class="sxs-lookup"><span data-stu-id="e1079-125">Restart the application that calls the [**OpenSCManager**](/windows/desktop/api/Winsvc/nf-winsvc-openscmanagera) function.</span></span>

<span data-ttu-id="e1079-126">下列程式描述如何在伺服器端停用 TCP。</span><span class="sxs-lookup"><span data-stu-id="e1079-126">The following procedure describes how to disable TCP on the server side.</span></span>

<span data-ttu-id="e1079-127">**若要在伺服器端停用 TCP**</span><span class="sxs-lookup"><span data-stu-id="e1079-127">**To disable TCP on the server side**</span></span>

1.  <span data-ttu-id="e1079-128">將 **DisableRPCOverTCP** 登錄值設定為1。</span><span class="sxs-lookup"><span data-stu-id="e1079-128">Set the **DisableRPCOverTCP** registry value to 1.</span></span>
2.  <span data-ttu-id="e1079-129">重新啟動伺服器。</span><span class="sxs-lookup"><span data-stu-id="e1079-129">Restart the server.</span></span>

<span data-ttu-id="e1079-130">下列程式說明如何在伺服器上停用 RPC/TCP 和 RPC/NP (例如，以減少受攻擊面) 。</span><span class="sxs-lookup"><span data-stu-id="e1079-130">The following procedure describes how to disable both RPC/TCP and RPC/NP on the server (for example, to reduce the attack surface).</span></span>

<span data-ttu-id="e1079-131">**若要在伺服器上停用 RPC/TCP 和 RPC/NP**</span><span class="sxs-lookup"><span data-stu-id="e1079-131">**To disable both RPC/TCP and RPC/NP on the server**</span></span>

1.  <span data-ttu-id="e1079-132">將 **DisableRemoteScmEndpoints** 登錄值設定為1。</span><span class="sxs-lookup"><span data-stu-id="e1079-132">Set the **DisableRemoteScmEndpoints** registry value to 1.</span></span>
2.  <span data-ttu-id="e1079-133">重新啟動伺服器。</span><span class="sxs-lookup"><span data-stu-id="e1079-133">Restart the server.</span></span>

<span data-ttu-id="e1079-134">**SCMApiConnectionParam** 登錄值也可以用來指定 RPC/TCP 逾時間隔（以毫秒為單位）。</span><span class="sxs-lookup"><span data-stu-id="e1079-134">The **SCMApiConnectionParam** registry value can also be used to specify the RPC/TCP time-out interval, in milliseconds.</span></span> <span data-ttu-id="e1079-135">例如，值為30000時，會指定30秒的逾時間隔。</span><span class="sxs-lookup"><span data-stu-id="e1079-135">For example, a value of 30,000 specifies a time-out interval of 30 seconds.</span></span> <span data-ttu-id="e1079-136">預設值為 21000 (21 秒) 。</span><span class="sxs-lookup"><span data-stu-id="e1079-136">The default is 21,000 (21 seconds).</span></span>

 

 
