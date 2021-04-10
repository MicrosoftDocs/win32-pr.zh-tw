---
title: 檔案系統重新導向程式
description: Windir \\ System32 目錄是保留給64位 Windows 上的64位應用程式。
ms.assetid: b4d36fe8-8bbb-469b-8ad1-650d559a4c75
keywords:
- 檔案系統重新導向程式 64-位 Windows 程式設計
- 64位 Windows 程式設計指南64位 Windows 程式設計，檔案系統重新導向程式
- WOW64 64 位 Windows 程式設計，檔案系統重新導向程式
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 561d03c8da51bd37a2d97746296bc74e24e43154
ms.sourcegitcommit: 592c9bbd22ba69802dc353bcb5eb30699f9e9403
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/20/2020
ms.locfileid: "104023806"
---
# <a name="file-system-redirector"></a><span data-ttu-id="9f5fe-106">檔案系統重新導向程式</span><span class="sxs-lookup"><span data-stu-id="9f5fe-106">File System Redirector</span></span>

<span data-ttu-id="9f5fe-107">% Windir% \\ System32 目錄是保留給64位 Windows 上的64位應用程式。</span><span class="sxs-lookup"><span data-stu-id="9f5fe-107">The %windir%\\System32 directory is reserved for 64-bit applications on 64-bit Windows.</span></span> <span data-ttu-id="9f5fe-108">當建立64位版本的 dll 時，大部分的 DLL 檔案名都不會變更，因此32位版本的 Dll 會儲存在不同的目錄中。</span><span class="sxs-lookup"><span data-stu-id="9f5fe-108">Most DLL file names were not changed when 64-bit versions of the DLLs were created, so 32-bit versions of the DLLs are stored in a different directory.</span></span> <span data-ttu-id="9f5fe-109">WOW64 會使用 *檔案系統* 重新導向器來隱藏這項差異。</span><span class="sxs-lookup"><span data-stu-id="9f5fe-109">WOW64 hides this difference by using a *file system redirector*.</span></span>

<span data-ttu-id="9f5fe-110">在大部分情況下，只要32位應用程式嘗試存取% windir% \\ System32、% windir% \\ lastgood \\ System32 或% windir% \\regedit.exe，就會將存取重新導向至特定架構的路徑。</span><span class="sxs-lookup"><span data-stu-id="9f5fe-110">In most cases, whenever a 32-bit application attempts to access %windir%\\System32, %windir%\\lastgood\\system32, or %windir%\\regedit.exe, the access is redirected to an architecture-specific path.</span></span>

> [!Note]  
> <span data-ttu-id="9f5fe-111">這些路徑僅提供供參考之用。</span><span class="sxs-lookup"><span data-stu-id="9f5fe-111">These paths are provided for reference only.</span></span> <span data-ttu-id="9f5fe-112">為了相容，應用程式不應該直接使用這些路徑。</span><span class="sxs-lookup"><span data-stu-id="9f5fe-112">For compatibility, applications should not use these paths directly.</span></span> <span data-ttu-id="9f5fe-113">相反地，它們應該呼叫如下所述的 Api。</span><span class="sxs-lookup"><span data-stu-id="9f5fe-113">Instead, they should call the APIs described below.</span></span>

 



|                              |                                          |                                          |
|------------------------------|------------------------------------------|------------------------------------------|
| <span data-ttu-id="9f5fe-114">原始路徑</span><span class="sxs-lookup"><span data-stu-id="9f5fe-114">Original Path</span></span>                | <span data-ttu-id="9f5fe-115">32位 x86 進程的重新導向路徑</span><span class="sxs-lookup"><span data-stu-id="9f5fe-115">Redirected Path for 32-bit x86 Processes</span></span> | <span data-ttu-id="9f5fe-116">32位 ARM 進程的重新導向路徑</span><span class="sxs-lookup"><span data-stu-id="9f5fe-116">Redirected Path for 32-bit ARM Processes</span></span> |
| <span data-ttu-id="9f5fe-117">% windir% \\ System32</span><span class="sxs-lookup"><span data-stu-id="9f5fe-117">%windir%\\System32</span></span>           | <span data-ttu-id="9f5fe-118">% windir% \\ SysWOW64</span><span class="sxs-lookup"><span data-stu-id="9f5fe-118">%windir%\\SysWOW64</span></span>                       | <span data-ttu-id="9f5fe-119">% windir% \\ SysArm32</span><span class="sxs-lookup"><span data-stu-id="9f5fe-119">%windir%\\SysArm32</span></span>                       |
| <span data-ttu-id="9f5fe-120">% windir% \\ lastgood \\ system32</span><span class="sxs-lookup"><span data-stu-id="9f5fe-120">%windir%\\lastgood\\system32</span></span> | <span data-ttu-id="9f5fe-121">% windir% \\ lastgood \\ SysWOW64</span><span class="sxs-lookup"><span data-stu-id="9f5fe-121">%windir%\\lastgood\\SysWOW64</span></span>             | <span data-ttu-id="9f5fe-122">% windir% \\ lastgood \\ SysArm32</span><span class="sxs-lookup"><span data-stu-id="9f5fe-122">%windir%\\lastgood\\SysArm32</span></span>             |
| <span data-ttu-id="9f5fe-123">% windir% \\regedit.exe</span><span class="sxs-lookup"><span data-stu-id="9f5fe-123">%windir%\\regedit.exe</span></span>        | <span data-ttu-id="9f5fe-124">% windir% \\ SysWOW64 \\regedit.exe</span><span class="sxs-lookup"><span data-stu-id="9f5fe-124">%windir%\\SysWOW64\\regedit.exe</span></span>          | <span data-ttu-id="9f5fe-125">% windir% \\ SysArm32 \\regedit.exe</span><span class="sxs-lookup"><span data-stu-id="9f5fe-125">%windir%\\ SysArm32\\regedit.exe</span></span>         |



 

<span data-ttu-id="9f5fe-126">如果存取導致系統顯示 UAC 提示，則不會發生重新導向。</span><span class="sxs-lookup"><span data-stu-id="9f5fe-126">If the access causes the system to display the UAC prompt, redirection does not occur.</span></span> <span data-ttu-id="9f5fe-127">相反地，會啟動所要求檔案的64位版本。</span><span class="sxs-lookup"><span data-stu-id="9f5fe-127">Instead, the 64-bit version of the requested file is launched.</span></span> <span data-ttu-id="9f5fe-128">若要避免這個問題，請指定 SysWOW64 目錄以避免重新導向，並確保存取32位版本的檔案，或以系統管理員許可權執行32位應用程式，如此就不會顯示 UAC 提示。</span><span class="sxs-lookup"><span data-stu-id="9f5fe-128">To prevent this problem, either specify the SysWOW64 directory to avoid redirection and ensure access to the 32-bit version of the file, or run the 32-bit application with administrator privileges so the UAC prompt is not displayed.</span></span>

<span data-ttu-id="9f5fe-129">**Windows Server 2003 和 WINDOWS XP：  ** 不支援 UAC。</span><span class="sxs-lookup"><span data-stu-id="9f5fe-129">**Windows Server 2003 and Windows XP:  ** UAC is not supported.</span></span>

<span data-ttu-id="9f5fe-130">某些子目錄豁免于重新導向。</span><span class="sxs-lookup"><span data-stu-id="9f5fe-130">Certain subdirectories are exempt from redirection.</span></span> <span data-ttu-id="9f5fe-131">這些子目錄的存取權不會重新導向至% windir% \\ SysWOW64：</span><span class="sxs-lookup"><span data-stu-id="9f5fe-131">Access to these subdirectories is not redirected to %windir%\\SysWOW64:</span></span> <dl> <span data-ttu-id="9f5fe-132">% windir% \\ system32 \\ catroot</span><span class="sxs-lookup"><span data-stu-id="9f5fe-132">%windir%\\system32\\catroot</span></span>  
<span data-ttu-id="9f5fe-133">% windir% \\ system32 \\ catroot2</span><span class="sxs-lookup"><span data-stu-id="9f5fe-133">%windir%\\system32\\catroot2</span></span>  
<span data-ttu-id="9f5fe-134">% windir% \\ system32 \\ driverstore</span><span class="sxs-lookup"><span data-stu-id="9f5fe-134">%windir%\\system32\\driverstore</span></span>  
<span data-ttu-id="9f5fe-135">% windir% \\ system32 \\ 驅動程式 \\ 等</span><span class="sxs-lookup"><span data-stu-id="9f5fe-135">%windir%\\system32\\drivers\\etc</span></span>  
<span data-ttu-id="9f5fe-136">% windir% \\ system32 記錄檔 \\</span><span class="sxs-lookup"><span data-stu-id="9f5fe-136">%windir%\\system32\\logfiles</span></span>  
<span data-ttu-id="9f5fe-137">% windir% \\ system32 多工 \\ 緩衝處理</span><span class="sxs-lookup"><span data-stu-id="9f5fe-137">%windir%\\system32\\spool</span></span>  
</dl>

<span data-ttu-id="9f5fe-138">**Windows server 2008、Windows Vista、Windows server 2003 和 WINDOWS XP：  **% windir% \\ system32 \\ driverstore 已重新導向。</span><span class="sxs-lookup"><span data-stu-id="9f5fe-138">**Windows Server 2008, Windows Vista, Windows Server 2003 and Windows XP:  **%windir%\\system32\\driverstore is redirected.</span></span>

<span data-ttu-id="9f5fe-139">若要取出32位系統目錄的名稱，64位應用程式應該使用 [**GetSystemWow64Directory2**](/windows/desktop/api/wow64apiset/nf-wow64apiset-getsystemwow64directory2a) 函式 (Windows 10、1511版) 或 [**GetSystemWow64Directory**](/windows/desktop/api/shlobj_core/nf-shlobj_core-shgetknownfolderpath) 函數。</span><span class="sxs-lookup"><span data-stu-id="9f5fe-139">To retrieve the name of the 32-bit system directory, 64-bit applications should use the [**GetSystemWow64Directory2**](/windows/desktop/api/wow64apiset/nf-wow64apiset-getsystemwow64directory2a) function (Windows 10, version 1511) or the [**GetSystemWow64Directory**](/windows/desktop/api/shlobj_core/nf-shlobj_core-shgetknownfolderpath) function.</span></span>

<span data-ttu-id="9f5fe-140">應用程式應該使用 [**SHGetKnownFolderPath**](https://www.bing.com/search?q=**SHGetKnownFolderPath**) 函式來判斷% ProgramFiles% 的目錄名稱。</span><span class="sxs-lookup"><span data-stu-id="9f5fe-140">Applications should use the [**SHGetKnownFolderPath**](https://www.bing.com/search?q=**SHGetKnownFolderPath**) function to determine the %ProgramFiles% directory name.</span></span>

<span data-ttu-id="9f5fe-141">**Windows Server 2003 和 WINDOWS XP：** 應用程式應該使用 [**SHGetSpecialFolderPath**](/windows/win32/api/shlobj_core/nf-shlobj_core-shgetspecialfolderpatha) 函式來判斷% ProgramFiles% 的目錄名稱。</span><span class="sxs-lookup"><span data-stu-id="9f5fe-141">**Windows Server 2003 and Windows XP:** Applications should use the [**SHGetSpecialFolderPath**](/windows/win32/api/shlobj_core/nf-shlobj_core-shgetspecialfolderpatha) function to determine the %ProgramFiles% directory name.</span></span>

<span data-ttu-id="9f5fe-142">應用程式可以使用 [**Wow64DisableWow64FsRedirection**](/windows/desktop/api/wow64apiset/nf-wow64apiset-wow64disablewow64fsredirection)、 [**Wow64EnableWow64FsRedirection**](/windows/desktop/api/winbase/nf-winbase-wow64enablewow64fsredirection)和 [**WOW64REVERTWOW64FSREDIRECTION**](/windows/desktop/api/wow64apiset/nf-wow64apiset-wow64revertwow64fsredirection) 函式來控制 WOW64 檔案系統重新導向器。</span><span class="sxs-lookup"><span data-stu-id="9f5fe-142">Applications can control the WOW64 file system redirector using the [**Wow64DisableWow64FsRedirection**](/windows/desktop/api/wow64apiset/nf-wow64apiset-wow64disablewow64fsredirection), [**Wow64EnableWow64FsRedirection**](/windows/desktop/api/winbase/nf-winbase-wow64enablewow64fsredirection), and [**Wow64RevertWow64FsRedirection**](/windows/desktop/api/wow64apiset/nf-wow64apiset-wow64revertwow64fsredirection) functions.</span></span> <span data-ttu-id="9f5fe-143">停用檔案系統重新導向會影響呼叫執行緒所執行的所有檔案作業，因此只有在單一 [**CreateFile**](/windows/desktop/api/fileapi/nf-fileapi-createfilea) 呼叫需要時才會停用，並且在函式傳回之後立即重新啟用。</span><span class="sxs-lookup"><span data-stu-id="9f5fe-143">Disabling file system redirection affects all file operations performed by the calling thread, so it should be disabled only when necessary for a single [**CreateFile**](/windows/desktop/api/fileapi/nf-fileapi-createfilea) call and re-enabled again immediately after the function returns.</span></span> <span data-ttu-id="9f5fe-144">停用較長期間的檔案系統重新導向可能會導致32位應用程式無法載入系統 Dll，導致應用程式失敗。</span><span class="sxs-lookup"><span data-stu-id="9f5fe-144">Disabling file system redirection for longer periods can prevent 32-bit applications from loading system DLLs, causing the applications to fail.</span></span>

<span data-ttu-id="9f5fe-145">32位應用程式可以藉由將% windir% \\ Sysnative 取代為% windir% System32 來存取原生系統目錄 \\ 。</span><span class="sxs-lookup"><span data-stu-id="9f5fe-145">32-bit applications can access the native system directory by substituting %windir%\\Sysnative for %windir%\\System32.</span></span> <span data-ttu-id="9f5fe-146">WOW64 會將 Sysnative 辨識為特殊別名，用來指出檔案系統不應重新導向存取。</span><span class="sxs-lookup"><span data-stu-id="9f5fe-146">WOW64 recognizes Sysnative as a special alias used to indicate that the file system should not redirect the access.</span></span> <span data-ttu-id="9f5fe-147">這項機制很有彈性且容易使用，因此建議您最好使用此機制來略過檔案系統重新導向。</span><span class="sxs-lookup"><span data-stu-id="9f5fe-147">This mechanism is flexible and easy to use, therefore, it is the recommended mechanism to bypass file system redirection.</span></span> <span data-ttu-id="9f5fe-148">請注意，64位應用程式無法使用 Sysnative 別名，因為它是虛擬目錄，而不是真正的目錄。</span><span class="sxs-lookup"><span data-stu-id="9f5fe-148">Note that 64-bit applications cannot use the Sysnative alias as it is a virtual directory not a real one.</span></span>

<span data-ttu-id="9f5fe-149">**Windows Server 2003 和 WINDOWS XP：** 從 Windows Vista 開始，已新增 Sysnative 別名。</span><span class="sxs-lookup"><span data-stu-id="9f5fe-149">**Windows Server 2003 and Windows XP:** The Sysnative alias was added starting with Windows Vista.</span></span>

 

 