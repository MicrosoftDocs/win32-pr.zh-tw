---
title: 命令封鎖
description: 為了保留作業的完整性，平臺上的軟體不允許執行某些 TPM 命令。
ms.assetid: 47402a4a-5f8d-4648-b3ea-06c95b2a1fc1
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 3f8b9a302f12e7838240ee8bfeac1ea78a3884a1
ms.sourcegitcommit: f0ca63c18dc52c357d3398af7be766d2bdd40be7
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 06/17/2020
ms.locfileid: "104374892"
---
# <a name="command-blocking"></a><span data-ttu-id="82fd6-103">命令封鎖</span><span class="sxs-lookup"><span data-stu-id="82fd6-103">Command Blocking</span></span>

<span data-ttu-id="82fd6-104">為了保留作業的完整性，平臺上的軟體不允許執行某些 TPM 命令。</span><span class="sxs-lookup"><span data-stu-id="82fd6-104">To preserve integrity of operations, certain TPM commands are not allowed to be executed by software on the platform.</span></span> <span data-ttu-id="82fd6-105">例如，某些命令只能由系統軟體執行。</span><span class="sxs-lookup"><span data-stu-id="82fd6-105">For example, some commands are only executed by system software.</span></span> <span data-ttu-id="82fd6-106">當 TBS 封鎖某個命令時，會適當地傳回錯誤。</span><span class="sxs-lookup"><span data-stu-id="82fd6-106">When the TBS blocks a command, an error is returned as appropriate.</span></span> <span data-ttu-id="82fd6-107">根據預設，TBS 會封鎖可能會影響系統隱私權、安全性和穩定性的命令。</span><span class="sxs-lookup"><span data-stu-id="82fd6-107">By default, the TBS blocks commands that could impact system privacy, security, and stability.</span></span> <span data-ttu-id="82fd6-108">此 TB 也假設軟體堆疊的其他部分可能會限制特定命令的存取權給已授權的實體。</span><span class="sxs-lookup"><span data-stu-id="82fd6-108">The TBS also assumes that other parts of the software stack may restrict access to certain commands to authorized entities.</span></span>

<span data-ttu-id="82fd6-109">針對 TPM 1.2 版命令，有三個封鎖的命令清單：由群組原則控制的清單、由本機系統管理員控制的清單，以及預設清單。</span><span class="sxs-lookup"><span data-stu-id="82fd6-109">For TPM version 1.2 commands, there are three lists of blocked commands: a list controlled by group policy, a list controlled by local administrators, and a default list.</span></span> <span data-ttu-id="82fd6-110">如果 TPM 命令位於任何清單上，則會予以封鎖。</span><span class="sxs-lookup"><span data-stu-id="82fd6-110">A TPM command is blocked if it is on any of the lists.</span></span> <span data-ttu-id="82fd6-111">不過，有群組原則旗標可允許 TB 忽略本機清單和預設清單。</span><span class="sxs-lookup"><span data-stu-id="82fd6-111">However, there are group policy flags to allow the TBS to ignore the local list and the default list.</span></span> <span data-ttu-id="82fd6-112">您可以直接編輯或透過群組原則物件編輯器來存取群組原則旗標。</span><span class="sxs-lookup"><span data-stu-id="82fd6-112">The group policy flags can be edited directly or accessed through the Group Policy Object Editor.</span></span>

> [!Note]  
> <span data-ttu-id="82fd6-113">升級至作業系統之後，不會保留本機封鎖的命令清單。</span><span class="sxs-lookup"><span data-stu-id="82fd6-113">The list of locally blocked commands is not preserved after an upgrade to the operating system.</span></span> <span data-ttu-id="82fd6-114">系統會保留封鎖在群組原則清單上的命令。</span><span class="sxs-lookup"><span data-stu-id="82fd6-114">Commands that are blocked on the Group Policy list are preserved.</span></span>

 

<span data-ttu-id="82fd6-115">針對 TPM 2.0 版命令，會反轉封鎖的邏輯;它會使用允許的命令清單。</span><span class="sxs-lookup"><span data-stu-id="82fd6-115">For TPM version 2.0 commands, the logic for blocking is inverted; it uses a list of allowed commands.</span></span> <span data-ttu-id="82fd6-116">當第一次建立清單時，此邏輯會自動封鎖未知的命令。</span><span class="sxs-lookup"><span data-stu-id="82fd6-116">This logic will automatically block commands that were not known when the list was first made.</span></span> <span data-ttu-id="82fd6-117">當 Windows 版本發行之後，將命令新增至 TPM 規格時，會自動封鎖這些新的命令。</span><span class="sxs-lookup"><span data-stu-id="82fd6-117">When commands are added to the TPM specification after a version of Windows has shipped, these new commands are automatically blocked.</span></span> <span data-ttu-id="82fd6-118">只有登錄的更新會將這些新的命令新增至允許的命令清單。</span><span class="sxs-lookup"><span data-stu-id="82fd6-118">Only an update of the registry will add these new commands to the list of allowed commands.</span></span>

<span data-ttu-id="82fd6-119">從 Windows 10 1809 (Windows Server 2019) ，就無法再透過登錄設定來操作允許的 TPM 2.0 命令。</span><span class="sxs-lookup"><span data-stu-id="82fd6-119">Starting with Windows 10 1809 (Windows Server 2019), allowed TPM 2.0 commands can no longer be manipulated through registry settings.</span></span> <span data-ttu-id="82fd6-120">針對這些 Windows 10 版本，TPM 驅動程式中會修正允許的 TPM 2.0 命令。</span><span class="sxs-lookup"><span data-stu-id="82fd6-120">For these Windows 10 versions, the allowed TPM 2.0 commands are fixed in the TPM driver.</span></span> <span data-ttu-id="82fd6-121">TPM 1.2 命令仍可透過登錄變更來封鎖和解除封鎖。</span><span class="sxs-lookup"><span data-stu-id="82fd6-121">TPM 1.2 commands can still be blocked and unblocked through registry changes.</span></span> 

## <a name="direct-registry-access"></a><span data-ttu-id="82fd6-122">Direct Registry 存取</span><span class="sxs-lookup"><span data-stu-id="82fd6-122">Direct Registry Access</span></span>

<span data-ttu-id="82fd6-123">群組原則旗標位於登錄機碼 **HKEY \_ 本機 \_ 電腦** \\ **軟體** \\ **原則** \\ **Microsoft** \\ **Tpm** \\ **BlockedCommands**。</span><span class="sxs-lookup"><span data-stu-id="82fd6-123">The Group Policy flags are under registry key **HKEY\_LOCAL\_MACHINE**\\**Software**\\**Policies**\\**Microsoft**\\**Tpm**\\**BlockedCommands**.</span></span>

<span data-ttu-id="82fd6-124">若要判斷哪些清單應用來封鎖 TPM 命令，有兩個 **DWORD** 值會用來做為布林值旗標：</span><span class="sxs-lookup"><span data-stu-id="82fd6-124">To determine which lists should be used to block TPM commands, there are two **DWORD** values that are used as Boolean flags:</span></span>

-   <span data-ttu-id="82fd6-125">"IgnoreDefaultList"</span><span class="sxs-lookup"><span data-stu-id="82fd6-125">"IgnoreDefaultList"</span></span>

    <span data-ttu-id="82fd6-126">如果 set (值存在且為非零值) ，則 TB 會忽略預設封鎖的命令清單。</span><span class="sxs-lookup"><span data-stu-id="82fd6-126">If set (value exists and is nonzero), the TBS ignores the default blocked-commands list.</span></span>

-   <span data-ttu-id="82fd6-127">"IgnoreLocalList"</span><span class="sxs-lookup"><span data-stu-id="82fd6-127">"IgnoreLocalList"</span></span>

    <span data-ttu-id="82fd6-128">如果 set (值存在且為非零值) ，則 TB 會忽略本機封鎖的命令清單。</span><span class="sxs-lookup"><span data-stu-id="82fd6-128">If set (value exists and is nonzero), the TBS ignores the local blocked-commands list.</span></span>

## <a name="group-policy-object-editor"></a><span data-ttu-id="82fd6-129">群組原則物件編輯器</span><span class="sxs-lookup"><span data-stu-id="82fd6-129">Group Policy Object Editor</span></span>

<span data-ttu-id="82fd6-130">**存取群組原則物件編輯器**</span><span class="sxs-lookup"><span data-stu-id="82fd6-130">**To access the Group Policy object editor**</span></span>

1.  <span data-ttu-id="82fd6-131">按一下 [啟動]。</span><span class="sxs-lookup"><span data-stu-id="82fd6-131">Click **Start**.</span></span>
2.  <span data-ttu-id="82fd6-132">按一下 **[執行]** 。</span><span class="sxs-lookup"><span data-stu-id="82fd6-132">Click **Run**.</span></span>
3.  <span data-ttu-id="82fd6-133">在 [開啟舊檔] 方塊中，輸入 **gpedit.msc**。</span><span class="sxs-lookup"><span data-stu-id="82fd6-133">In the **Open** box, type **gpedit.msc**.</span></span> <span data-ttu-id="82fd6-134">按一下 [確定]  。</span><span class="sxs-lookup"><span data-stu-id="82fd6-134">Click **OK**.</span></span> <span data-ttu-id="82fd6-135">群組原則物件編輯器隨即開啟。</span><span class="sxs-lookup"><span data-stu-id="82fd6-135">The Group Policy object editor opens.</span></span>
4.  <span data-ttu-id="82fd6-136">展開 [ **電腦** 設定]。</span><span class="sxs-lookup"><span data-stu-id="82fd6-136">Expand **Computer Configuration**.</span></span>
5.  <span data-ttu-id="82fd6-137">展開 [ **系統管理範本**]。</span><span class="sxs-lookup"><span data-stu-id="82fd6-137">Expand **Administrative Templates**.</span></span>
6.  <span data-ttu-id="82fd6-138">展開 [ **系統**]。</span><span class="sxs-lookup"><span data-stu-id="82fd6-138">Expand **System**.</span></span>
7.  <span data-ttu-id="82fd6-139">展開 [ **信賴平臺模組服務**]。</span><span class="sxs-lookup"><span data-stu-id="82fd6-139">Expand **Trusted Platform Module Services**.</span></span>

<span data-ttu-id="82fd6-140">您可以直接在下列位置編輯特定封鎖 TPM 1.2 命令的清單。</span><span class="sxs-lookup"><span data-stu-id="82fd6-140">The lists of specific blocked TPM1.2 commands can be edited directly in the following locations.</span></span>

-   <span data-ttu-id="82fd6-141">群組原則清單：</span><span class="sxs-lookup"><span data-stu-id="82fd6-141">Group policy list:</span></span>

    ```
    HKEY_LOCAL_MACHINE
       Software
          Policies
             Microsoft
                Tpm
                   BlockedCommands
                      List
    ```

-   <span data-ttu-id="82fd6-142">本機清單：</span><span class="sxs-lookup"><span data-stu-id="82fd6-142">Local list:</span></span>

    ```
    HKEY_LOCAL_MACHINE
       SYSTEM
          CurrentControlSet
             Services
                SharedAccess
                   Parameters
                      Tpm
                         BlockedCommands
                            List
    ```

-   <span data-ttu-id="82fd6-143">預設清單：</span><span class="sxs-lookup"><span data-stu-id="82fd6-143">Default list:</span></span>

    ```
    HKEY_LOCAL_MACHINE
       Software
          Microsoft
             Tpm
                BlockedCommands
                   List
    ```

<span data-ttu-id="82fd6-144">在每個登錄機碼下，都有一個登錄值的清單，也就是 REG \_ SZ 型別。</span><span class="sxs-lookup"><span data-stu-id="82fd6-144">Under each of these registry keys, there is a list of registry values of REG\_SZ type.</span></span> <span data-ttu-id="82fd6-145">每個值都代表封鎖的 TPM 命令。</span><span class="sxs-lookup"><span data-stu-id="82fd6-145">Each value represents a blocked TPM command.</span></span> <span data-ttu-id="82fd6-146">每個登錄機碼都有一個 [值名稱] 欄位和 [值資料] 欄位。</span><span class="sxs-lookup"><span data-stu-id="82fd6-146">Each registry key has a "Value name" field and a "Value data" field.</span></span> <span data-ttu-id="82fd6-147">這兩個欄位 ( 「值名稱」和「值資料」 ) ，應完全符合要封鎖之 TPM 命令序數的十進位值。</span><span class="sxs-lookup"><span data-stu-id="82fd6-147">Both fields ("Value Name" and "Value data"), should exactly match the decimal value of the TPM command ordinal to be blocked.</span></span>

<span data-ttu-id="82fd6-148">您可以直接在下列位置編輯特定的允許 TPM 2.0 命令清單。</span><span class="sxs-lookup"><span data-stu-id="82fd6-148">The list of specific allowed TPM 2.0 commands can be edited directly in the following location.</span></span> <span data-ttu-id="82fd6-149">在登錄機碼底下，有一個登錄值的登錄值清單 \_ 。</span><span class="sxs-lookup"><span data-stu-id="82fd6-149">Under the registry key, there is a list of registry values of REG\_DWORD type.</span></span> <span data-ttu-id="82fd6-150">每個值都代表一個允許的 TPM 2.0 命令。</span><span class="sxs-lookup"><span data-stu-id="82fd6-150">Each value represents an allowed TPM 2.0 command.</span></span> <span data-ttu-id="82fd6-151">每個登錄值都有 **名稱** 和 **值** 欄位。</span><span class="sxs-lookup"><span data-stu-id="82fd6-151">Each registry value has a **name** and a **value** field.</span></span> <span data-ttu-id="82fd6-152">**名稱** 符合應允許的十六進位 TPM 2.0 命令序數。</span><span class="sxs-lookup"><span data-stu-id="82fd6-152">The **name** matches the hexadecimal TPM 2.0 command ordinal that should be allowed.</span></span> <span data-ttu-id="82fd6-153">如果允許命令， **值** 的值會是1。</span><span class="sxs-lookup"><span data-stu-id="82fd6-153">The **value** has a value of 1 if the command is allowed.</span></span> <span data-ttu-id="82fd6-154">如果命令序數不存在或值為0，則會封鎖此命令。</span><span class="sxs-lookup"><span data-stu-id="82fd6-154">If a command ordinal is not present or has a value of 0, the command will be blocked.</span></span>

-   <span data-ttu-id="82fd6-155">預設清單：</span><span class="sxs-lookup"><span data-stu-id="82fd6-155">Default list:</span></span>

    ```
    HKEY_LOCAL_MACHINE
       Software
          Microsoft
             Tpm
                AllowedW8Commands
                   List
    ```

<span data-ttu-id="82fd6-156">針對 Windows 8、Windows Server 2012 和更新版本， **BlockedCommands** 和 **AllowedW8Commands** 登錄機碼分別會判斷系統管理員帳戶的封鎖或允許 TPM 命令。</span><span class="sxs-lookup"><span data-stu-id="82fd6-156">For Windows 8, Windows Server 2012 and later, the **BlockedCommands** and **AllowedW8Commands** registry keys respectively determine the blocked or allowed TPM commands for administrator accounts.</span></span> <span data-ttu-id="82fd6-157">使用者帳戶會在 **BlockedUserCommands** 和 **AllowedW8UserCommands** 登錄機碼中分別有封鎖或允許的 TPM 命令清單。</span><span class="sxs-lookup"><span data-stu-id="82fd6-157">User accounts have a list of blocked or allowed TPM commands in the **BlockedUserCommands** and **AllowedW8UserCommands** registry keys respectively.</span></span> <span data-ttu-id="82fd6-158">在 Windows 10 1607 版中，已針對 AppContainer 應用程式導入了新的登錄機碼： **BlockedAppContainerCommands** 和 **AllowedW8AppContainerCommands**。</span><span class="sxs-lookup"><span data-stu-id="82fd6-158">In Windows 10, version 1607, new registry keys have been introduces for AppContainer applications: **BlockedAppContainerCommands** and **AllowedW8AppContainerCommands**.</span></span>

 

 




