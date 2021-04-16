---
description: Windows 10 引進了新的安全性功能，名為虛擬安全模式 (VSM) 。
ms.assetid: 58374CC4-593F-4B91-A5E4-85E29C44F8B4
title: 隔離的使用者模式 (IUM) 進程
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 81a176421174a58abe4ab595bb37ab75434edade
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/07/2021
ms.locfileid: "104566990"
---
# <a name="isolated-user-mode-ium-processes"></a><span data-ttu-id="f6aa6-103">隔離的使用者模式 (IUM) 進程</span><span class="sxs-lookup"><span data-stu-id="f6aa6-103">Isolated User Mode (IUM) Processes</span></span>

<span data-ttu-id="f6aa6-104">Windows 10 引進了新的安全性功能，名為虛擬安全模式 (VSM) 。</span><span class="sxs-lookup"><span data-stu-id="f6aa6-104">Windows 10 introduced a new security feature named Virtual Secure Mode (VSM).</span></span> <span data-ttu-id="f6aa6-105">VSM 利用 Hyper-v 管理程式和第二層位址轉譯 (SLAT) 來建立一組稱為虛擬信任層級的模式 (Vtl) 。</span><span class="sxs-lookup"><span data-stu-id="f6aa6-105">VSM leverages the Hyper-V Hypervisor and Second Level Address Translation (SLAT) to create a set of modes called Virtual Trust Levels (VTLs).</span></span> <span data-ttu-id="f6aa6-106">這個新的軟體架構會建立安全性界限，以防止在某個 VTL 中執行的進程存取另一個 VTL 的記憶體。</span><span class="sxs-lookup"><span data-stu-id="f6aa6-106">This new software architecture creates a security boundary to prevent processes running in one VTL from accessing the memory of another VTL.</span></span> <span data-ttu-id="f6aa6-107">這項隔離的好處包括：減少核心攻擊的額外風險，同時保護密碼雜湊和 Kerberos 金鑰之類的資產。</span><span class="sxs-lookup"><span data-stu-id="f6aa6-107">The benefit of this isolation includes additional mitigation from kernel exploits while protecting assets such as password hashes and Kerberos keys.</span></span>

<span data-ttu-id="f6aa6-108">圖1說明傳統的核心模式和使用者模式程式碼（分別在 CPU ring 0 和 ring 3 中執行）的模型。</span><span class="sxs-lookup"><span data-stu-id="f6aa6-108">Diagram 1 depicts the traditional model of Kernel mode and User mode code running in CPU ring 0 and ring 3, respectively.</span></span> <span data-ttu-id="f6aa6-109">在此新模型中，傳統模型中執行的程式碼會在 VTL0 中執行，而且它無法存取較高許可權的 VTL1，其中安全核心和隔離使用者模式 (IUM) 執行程式碼。</span><span class="sxs-lookup"><span data-stu-id="f6aa6-109">In this new model, the code running in the traditional model executes in VTL0 and it cannot access the higher privileged VTL1, where the Secure Kernel and Isolated User Mode (IUM) execute code.</span></span> <span data-ttu-id="f6aa6-110">Vtl 是階層表示在 VTL1 中執行的任何程式碼，比在 VTL0 中執行的程式碼更有許可權。</span><span class="sxs-lookup"><span data-stu-id="f6aa6-110">The VTLs are hierarchal meaning any code running in VTL1 is more privileged than code running in VTL0.</span></span>

<span data-ttu-id="f6aa6-111">VTL 隔離是由 Hyper-v 虛擬程式所建立，它會在開機時使用第二層位址轉譯 (SLAT) 來指派記憶體。</span><span class="sxs-lookup"><span data-stu-id="f6aa6-111">The VTL isolation is created by the Hyper-V Hypervisor which assigns memory at boot time using Second Level Address Translation (SLAT).</span></span> <span data-ttu-id="f6aa6-112">當系統執行時，它會以動態方式繼續進行，保護安全核心所指定的記憶體需要防止 VTL0，因為它會用來包含秘密。</span><span class="sxs-lookup"><span data-stu-id="f6aa6-112">It continues this dynamically as the system runs, protecting memory the Secure Kernel specifies needing protection from VTL0 because it will be used to contain secrets.</span></span> <span data-ttu-id="f6aa6-113">針對這兩個 Vtl 配置個別的記憶體區塊時，系統會為 VTL1 建立安全的執行時間環境，方法是將專屬的記憶體區塊指派給 VTL1，並使用適當的存取權限來 VTL0。</span><span class="sxs-lookup"><span data-stu-id="f6aa6-113">As separate blocks of memory are allocated for the two VTLs, a secure runtime environment is created for VTL1 by assigning exclusive memory blocks to VTL1 and VTL0 with the appropriate access permissions.</span></span>

<span data-ttu-id="f6aa6-114">**圖 1-IUM 架構**</span><span class="sxs-lookup"><span data-stu-id="f6aa6-114">**Diagram 1 - IUM Architecture**</span></span>

![圖 1-ium 架構](images/uim-architecture.png)

## <a name="trustlets"></a><span data-ttu-id="f6aa6-116">Trustlets</span><span class="sxs-lookup"><span data-stu-id="f6aa6-116">Trustlets</span></span>

<span data-ttu-id="f6aa6-117">Trustlets (也稱為受信任的進程、安全程式或 IUM 程式，) 是在 VSM 中以 IUM 進程的形式執行的程式。</span><span class="sxs-lookup"><span data-stu-id="f6aa6-117">Trustlets (also known as trusted processes, secure processes, or IUM processes) are programs running as IUM processes in VSM.</span></span> <span data-ttu-id="f6aa6-118">他們藉由將系統呼叫封送處理至 VTL0 環形0中執行的 Windows 核心，來完成系統呼叫。</span><span class="sxs-lookup"><span data-stu-id="f6aa6-118">They complete system calls by marshalling them over to the Windows kernel running in VTL0 ring 0.</span></span> <span data-ttu-id="f6aa6-119">VSM 建立了一個小型的執行環境，其中包含在 VTL1 中執行的小型安全核心， (與 VTL0) 中執行的核心和驅動程式隔離。</span><span class="sxs-lookup"><span data-stu-id="f6aa6-119">VSM creates a small execution environment that includes the small Secure Kernel executing in VTL1 (isolated from the kernel and drivers running in VTL0).</span></span> <span data-ttu-id="f6aa6-120">明確的安全性優點是從 VTL0 核心中執行的驅動程式，將 VTL1 中的 trustlet 使用者模式頁面隔離。</span><span class="sxs-lookup"><span data-stu-id="f6aa6-120">The clear security benefit is isolation of trustlet user mode pages in VTL1 from drivers running in the VTL0 kernel.</span></span> <span data-ttu-id="f6aa6-121">即使 VTL0 的核心模式遭到惡意程式碼入侵，它也無法存取 IUM 進程頁面。</span><span class="sxs-lookup"><span data-stu-id="f6aa6-121">Even if kernel mode of VTL0 is compromised by malware, it will not have access to the IUM process pages.</span></span>

<span data-ttu-id="f6aa6-122">啟用 VSM 之後， (LSASS) 環境的本地安全機構會以 trustlet 的形式執行。</span><span class="sxs-lookup"><span data-stu-id="f6aa6-122">With VSM enabled, the Local Security Authority (LSASS) environment runs as a trustlet.</span></span> <span data-ttu-id="f6aa6-123">LSASS 會管理本機系統原則、使用者驗證，以及處理機密安全性資料（例如密碼雜湊和 Kerberos 金鑰）的審核。</span><span class="sxs-lookup"><span data-stu-id="f6aa6-123">LSASS manages the local system policy, user authentication, and auditing while handling sensitive security data such as password hashes and Kerberos keys.</span></span> <span data-ttu-id="f6aa6-124">為了充分利用 VSM 的安全性優勢，名為)  (LSAISO.exe 的 trustlet 會在 VTL1 中執行，並透過 RPC 通道與 VTL0 中執行的 LSASS.exe 進行通訊。</span><span class="sxs-lookup"><span data-stu-id="f6aa6-124">To leverage the security benefits of VSM, a trustlet named LSAISO.exe (LSA Isolated) runs in VTL1 and communicates with LSASS.exe running in VTL0 through an RPC channel.</span></span> <span data-ttu-id="f6aa6-125">LSAISO 秘密會先經過加密，再將它們傳送到以 VSM 正常模式執行的 LSASS，而且 LSAISO 的頁面會受到保護，以防止惡意程式碼在 VTL0 中執行。</span><span class="sxs-lookup"><span data-stu-id="f6aa6-125">The LSAISO secrets are encrypted before sending them over to LSASS running in VSM Normal Mode and the pages of LSAISO are protected from malicious code running in VTL0.</span></span>

<span data-ttu-id="f6aa6-126">**圖2– LSASS Trustlet 設計**</span><span class="sxs-lookup"><span data-stu-id="f6aa6-126">**Diagram 2 – LSASS Trustlet Design**</span></span>

![<span data-ttu-id="f6aa6-127">圖2– lsass trustlet 設計</span><span class="sxs-lookup"><span data-stu-id="f6aa6-127">diagram 2 – lsass trustlet design</span></span> ](images/lsass-trustlet-design.png)

## <a name="isolated-user-mode-ium-implications"></a><span data-ttu-id="f6aa6-128">隔離的使用者模式 (IUM) 含意</span><span class="sxs-lookup"><span data-stu-id="f6aa6-128">Isolated User Mode (IUM) Implications</span></span>

<span data-ttu-id="f6aa6-129">您無法附加到 IUM 進程，而是抑制偵錯工具 VTL1 程式碼的能力。</span><span class="sxs-lookup"><span data-stu-id="f6aa6-129">It is not possible to attach to an IUM process, inhibiting the ability to debug VTL1 code.</span></span> <span data-ttu-id="f6aa6-130">這包括事後剖析記憶體傾印的偵錯工具，以及附加偵錯工具來進行即時的偵錯工具。</span><span class="sxs-lookup"><span data-stu-id="f6aa6-130">This includes post mortem debugging of memory dumps and attaching the Debugging Tools for live debugging.</span></span> <span data-ttu-id="f6aa6-131">它也包含特殊許可權帳戶或核心驅動程式的嘗試，以將 DLL 載入至 IUM 程式、插入執行緒或傳遞使用者模式。</span><span class="sxs-lookup"><span data-stu-id="f6aa6-131">It also includes attempts by privileged accounts or kernel drivers to load a DLL into an IUM process, to inject a thread, or deliver a user-mode APC.</span></span> <span data-ttu-id="f6aa6-132">這類嘗試可能會導致整個系統不穩定。</span><span class="sxs-lookup"><span data-stu-id="f6aa6-132">Such attempts may result in destabilization of the entire system.</span></span> <span data-ttu-id="f6aa6-133">會危及 Trustlet 安全性的 Windows Api 可能會以非預期的方式失敗。</span><span class="sxs-lookup"><span data-stu-id="f6aa6-133">Windows APIs that would compromise the security of a Trustlet may fail in unexpected ways.</span></span> <span data-ttu-id="f6aa6-134">例如，將 DLL 載入至 Trustlet 可在 VTL0 中使用，但不能在 VTL1 中使用。</span><span class="sxs-lookup"><span data-stu-id="f6aa6-134">For example, loading a DLL into a Trustlet will make it available in VTL0 but not VTL1.</span></span> <span data-ttu-id="f6aa6-135">如果目標執行緒在 Trustlet 中，QueueUserApc 可能會無訊息地失敗。</span><span class="sxs-lookup"><span data-stu-id="f6aa6-135">QueueUserApc may silently fail if the target thread is in a Trustlet.</span></span> <span data-ttu-id="f6aa6-136">當針對 Trustlets 使用時，其他 Api （例如 CreateRemoteThread、VirtualAllocEx 和 Read/WriteProcessMemory）也將無法如預期般運作。</span><span class="sxs-lookup"><span data-stu-id="f6aa6-136">Other APIs, such as CreateRemoteThread, VirtualAllocEx, and Read/WriteProcessMemory will also not work as expected when used against Trustlets.</span></span>

<span data-ttu-id="f6aa6-137">使用下面的範例程式碼，以防止呼叫任何嘗試將程式碼附加或插入至 IUM 進程的函式。</span><span class="sxs-lookup"><span data-stu-id="f6aa6-137">Use the sample code below to prevent calling any functions which attempt to attach or inject code into an IUM process.</span></span> <span data-ttu-id="f6aa6-138">這包括將 Apc 排入佇列以在 trustlet 中執行程式碼的核心驅動程式。</span><span class="sxs-lookup"><span data-stu-id="f6aa6-138">This includes kernel drivers that queue APCs for execution of code in a trustlet.</span></span>

## <a name="remarks"></a><span data-ttu-id="f6aa6-139">備註</span><span class="sxs-lookup"><span data-stu-id="f6aa6-139">Remarks</span></span>

<span data-ttu-id="f6aa6-140">如果 IsSecureProcess 的傳回狀態為 success，請檢查 SecureProcess \_ Out \_ 參數，以判斷進程是否為 IUM 進程。</span><span class="sxs-lookup"><span data-stu-id="f6aa6-140">If the return status of IsSecureProcess is success, examine the SecureProcess \_Out\_ parameter to determine if the process is an IUM process.</span></span> <span data-ttu-id="f6aa6-141">系統會將 IUM 處理常式標示為「安全進程」。</span><span class="sxs-lookup"><span data-stu-id="f6aa6-141">IUM processes are marked by the system to be “Secure Processes”.</span></span> <span data-ttu-id="f6aa6-142">TRUE 的布林值結果表示目標進程的類型為 IUM。</span><span class="sxs-lookup"><span data-stu-id="f6aa6-142">A Boolean result of TRUE means the target process is of type IUM.</span></span>


```C++
NTSTATUS
IsSecureProcess(
   _In_ HANDLE ProcessHandle,
   _Out_ BOOLEAN *SecureProcess
   )
{
   NTSTATUS status;

       // definition included in ntddk.h  
   PROCESS_EXTENDED_BASIC_INFORMATION extendedInfo = {0};
 
   PAGED_CODE(); 
  
   extendedInfo.Size = sizeof(extendedInfo);

   // Query for the process information  
   status = ZwQueryInformationProcess(
                  ProcessHandle, ProcessBasicInformation, &extendedInfo,
                  sizeof(extendedInfo), NULL);

   if (NT_SUCCESS(status)) {
      *SecureProcess = (BOOLEAN)(extendedInfo.IsSecureProcess != 0);
   }
 
          return status;
}
```



<span data-ttu-id="f6aa6-143">Windows 10 的 WDK "Windows 驅動程式套件-Windows 10.0.15063.0" 包含處理常式 \_ 延伸 \_ 基本資訊結構所需的定義 \_ 。</span><span class="sxs-lookup"><span data-stu-id="f6aa6-143">The WDK for Windows 10, “Windows Driver Kit - Windows 10.0.15063.0”, contains the required definition of the PROCESS\_EXTENDED\_BASIC\_INFORMATION structure.</span></span> <span data-ttu-id="f6aa6-144">結構的更新版本是在 ntddk 中以新的 IsSecureProcess 欄位定義。</span><span class="sxs-lookup"><span data-stu-id="f6aa6-144">The updated version of the structure is defined in ntddk.h with the new IsSecureProcess field.</span></span>


```C++
typedef struct _PROCESS_EXTENDED_BASIC_INFORMATION {
    SIZE_T Size;    // Ignored as input, written with structure size on output
    PROCESS_BASIC_INFORMATION BasicInfo;
    union {
        ULONG Flags;
        struct {
            ULONG IsProtectedProcess : 1;
            ULONG IsWow64Process : 1;
            ULONG IsProcessDeleting : 1;
            ULONG IsCrossSessionCreate : 1;
            ULONG IsFrozen : 1;
            ULONG IsBackground : 1;
            ULONG IsStronglyNamed : 1;
            ULONG IsSecureProcess : 1;
            ULONG IsSubsystemProcess : 1;
            ULONG SpareBits : 23;
        } DUMMYSTRUCTNAME;
    } DUMMYUNIONNAME;
} PROCESS_EXTENDED_BASIC_INFORMATION, *PPROCESS_EXTENDED_BASIC_INFORMATION;
```



 

 



