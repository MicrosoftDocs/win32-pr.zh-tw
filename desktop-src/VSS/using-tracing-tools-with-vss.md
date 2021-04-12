---
description: 若要收集 VSS 基礎結構的追蹤資訊，您可以使用 VssTrace 工具、Logman 工具或 Tracelog.exe 工具。
ms.assetid: afe2a0ed-1a8e-4f8b-be9e-241d55cd9ef6
title: 使用追蹤工具搭配 VSS
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 073a2ae9ba2ba2771abdc37ff0291764ed5e9efd
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/07/2021
ms.locfileid: "104191364"
---
# <a name="using-tracing-tools-with-vss"></a><span data-ttu-id="ab24e-103">使用追蹤工具搭配 VSS</span><span class="sxs-lookup"><span data-stu-id="ab24e-103">Using Tracing Tools with VSS</span></span>

<span data-ttu-id="ab24e-104">若要收集 VSS 基礎結構的追蹤資訊，您可以使用 VssTrace 工具、Logman 工具或 Tracelog.exe 工具。</span><span class="sxs-lookup"><span data-stu-id="ab24e-104">To collect tracing information for the VSS infrastructure, you can use the VssTrace tool, the Logman tool, or the Tracelog tool.</span></span> <span data-ttu-id="ab24e-105">VssTrace 可在 Microsoft Windows 軟體開發套件 (SDK) 中取得，而且可用來在 Windows 7 和更新版本的 Windows 作業系統上追蹤 VSS 應用程式。</span><span class="sxs-lookup"><span data-stu-id="ab24e-105">VssTrace is available in the Microsoft Windows Software Development Kit (SDK) and can be used to trace VSS applications on Windows 7 and later versions of the Windows operating system.</span></span> <span data-ttu-id="ab24e-106">Logman 是追蹤事件和效能計數器的追蹤控制器;它也可以用來在 Windows 7 和更新版本的 Windows 作業系統上追蹤 VSS 應用程式。</span><span class="sxs-lookup"><span data-stu-id="ab24e-106">Logman is a trace controller for trace events and performance counters; it can also be used to trace VSS applications on Windows 7 and later versions of the Windows operating system.</span></span> <span data-ttu-id="ab24e-107">Tracelog.exe 包含在 Windows 驅動程式套件 (WDK) 中。</span><span class="sxs-lookup"><span data-stu-id="ab24e-107">Tracelog is included in the Windows Driver Kit (WDK).</span></span>

<span data-ttu-id="ab24e-108">若要使用追蹤工具搭配 [自動化系統復原 (asr) ](using-vss-automated-system-recovery-for-disaster-recovery.md)，請參閱搭配 [Asr 應用程式使用追蹤工具](using-tracing-tools-with-vss-asr-applications.md)。</span><span class="sxs-lookup"><span data-stu-id="ab24e-108">To use tracing tools with [Automated System Recovery (ASR)](using-vss-automated-system-recovery-for-disaster-recovery.md), see [Using Tracing Tools with ASR Applications](using-tracing-tools-with-vss-asr-applications.md).</span></span>

> [!Note]  
> <span data-ttu-id="ab24e-109">VssTrace、Logman 和 Tracelog.exe 都需要系統管理員許可權。</span><span class="sxs-lookup"><span data-stu-id="ab24e-109">VssTrace, Logman, and Tracelog all require administrator privilege.</span></span>

 

<span data-ttu-id="ab24e-110">如需每個工具的相關資訊，請參閱下列各節：</span><span class="sxs-lookup"><span data-stu-id="ab24e-110">For information about each tool, see the following sections:</span></span>

-   [<span data-ttu-id="ab24e-111">使用 VssTrace</span><span class="sxs-lookup"><span data-stu-id="ab24e-111">Using VssTrace</span></span>](#using-vsstrace)
    -   [<span data-ttu-id="ab24e-112">VssTrace Command-Line 選項</span><span class="sxs-lookup"><span data-stu-id="ab24e-112">VssTrace Command-Line Options</span></span>](#vsstrace-command-line-options)
-   [<span data-ttu-id="ab24e-113">使用 Logman</span><span class="sxs-lookup"><span data-stu-id="ab24e-113">Using Logman</span></span>](#using-logman)
-   [<span data-ttu-id="ab24e-114">使用 Tracelog.exe</span><span class="sxs-lookup"><span data-stu-id="ab24e-114">Using Tracelog</span></span>](#using-tracelog)

## <a name="using-vsstrace"></a><span data-ttu-id="ab24e-115">使用 VssTrace</span><span class="sxs-lookup"><span data-stu-id="ab24e-115">Using VssTrace</span></span>

<span data-ttu-id="ab24e-116">若要從命令列執行 VssTrace 工具，請使用下列語法：</span><span class="sxs-lookup"><span data-stu-id="ab24e-116">To run the VssTrace tool from the command line, use the following syntax:</span></span>

<span data-ttu-id="ab24e-117">**vsstrace** *命令列選項*</span><span class="sxs-lookup"><span data-stu-id="ab24e-117">**vsstrace** *command-line-options*</span></span>

<span data-ttu-id="ab24e-118">若要顯示 VssTrace 工具的簡潔命令列說明，請使用下列語法：</span><span class="sxs-lookup"><span data-stu-id="ab24e-118">To display concise command-line help for the VssTrace tool, use the following syntax:</span></span>

<span data-ttu-id="ab24e-119">**vsstrace-說明**</span><span class="sxs-lookup"><span data-stu-id="ab24e-119">**vsstrace -help**</span></span>

<span data-ttu-id="ab24e-120">若要顯示 VssTrace 工具的詳細命令列說明，請使用下列語法：</span><span class="sxs-lookup"><span data-stu-id="ab24e-120">To display detailed command-line help for the VssTrace tool, use the following syntax:</span></span>

<span data-ttu-id="ab24e-121">**vsstrace-全部協助**</span><span class="sxs-lookup"><span data-stu-id="ab24e-121">**vsstrace -help all**</span></span>

### <a name="vsstrace-command-line-options"></a><span data-ttu-id="ab24e-122">VssTrace Command-Line 選項</span><span class="sxs-lookup"><span data-stu-id="ab24e-122">VssTrace Command-Line Options</span></span>

<span data-ttu-id="ab24e-123">VssTrace 工具會使用下列命令列選項：</span><span class="sxs-lookup"><span data-stu-id="ab24e-123">The VssTrace tool uses the following command-line options:</span></span>

<dl> <dt>

<span data-ttu-id="ab24e-124"><span id="-f_Flags"></span><span id="-f_flags"></span><span id="-F_FLAGS"></span>**-f** *旗標*</span><span class="sxs-lookup"><span data-stu-id="ab24e-124"><span id="-f_Flags"></span><span id="-f_flags"></span><span id="-F_FLAGS"></span>**-f** *Flags*</span></span>
</dt> <dd>

<span data-ttu-id="ab24e-125">啟用旗 *標* 位元遮罩所指定之旗標的模組。</span><span class="sxs-lookup"><span data-stu-id="ab24e-125">Enable the modules whose flags are specified by the *Flags* bitmask.</span></span> <span data-ttu-id="ab24e-126">每個旗標都對應至一個 VSS 模組。</span><span class="sxs-lookup"><span data-stu-id="ab24e-126">Each flag corresponds to a VSS module.</span></span> <span data-ttu-id="ab24e-127">如果 *旗標* 為零，則不會啟用任何模組。</span><span class="sxs-lookup"><span data-stu-id="ab24e-127">If *Flags* is zero, no modules are enabled.</span></span> <span data-ttu-id="ab24e-128">請注意，大部分的模組預設都會啟用。</span><span class="sxs-lookup"><span data-stu-id="ab24e-128">Note that most modules are enabled by default.</span></span> <span data-ttu-id="ab24e-129">這個選項可以與 **+** _模組_ 選項結合。</span><span class="sxs-lookup"><span data-stu-id="ab24e-129">This option can be combined with the **+**_Module_ option.</span></span> <span data-ttu-id="ab24e-130">例如， **vsstrace-f 0 + WRITER + COORD** 會停用依預設啟用的所有模組的追蹤，並啟用 VSS 寫入器和 vss 服務的追蹤。</span><span class="sxs-lookup"><span data-stu-id="ab24e-130">For example, **vsstrace -f 0 +WRITER +COORD** disables tracing of all of the modules that are enabled by default and enables tracing of VSS writers and the VSS service.</span></span> <span data-ttu-id="ab24e-131">另外， **vsstrace + f 0XFFFF COORD** 也可以追蹤所有模組，但 VSS 服務除外。</span><span class="sxs-lookup"><span data-stu-id="ab24e-131">Alternatively, **vsstrace +f 0xffff -COORD** enables tracing of all modules except the VSS service.</span></span>

> [!Note]  
> <span data-ttu-id="ab24e-132">如果您搭配使用 **-f** 選項與 **+** _模組_ 選項， **-f** 必須出現在 **+** _模組_ 選項之前。</span><span class="sxs-lookup"><span data-stu-id="ab24e-132">If you use the **-f** option together with the **+**_Module_ option, the **-f** must appear before the **+**_Module_ option.</span></span>

 

<span data-ttu-id="ab24e-133">下表列出每個可用模組的模組名稱和旗標。</span><span class="sxs-lookup"><span data-stu-id="ab24e-133">The following table lists the module name and flag for each available module.</span></span>

| <span data-ttu-id="ab24e-134">模組</span><span class="sxs-lookup"><span data-stu-id="ab24e-134">Module</span></span> | <span data-ttu-id="ab24e-135">旗標</span><span class="sxs-lookup"><span data-stu-id="ab24e-135">Flag</span></span>       | <span data-ttu-id="ab24e-136">預設已啟用</span><span class="sxs-lookup"><span data-stu-id="ab24e-136">Enabled by default</span></span> | <span data-ttu-id="ab24e-137">追蹤的專案</span><span class="sxs-lookup"><span data-stu-id="ab24e-137">Items traced</span></span>                                                                                                                                  |
|--------|------------|--------------------|-----------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="ab24e-138">EXCEPT</span><span class="sxs-lookup"><span data-stu-id="ab24e-138">EXCEPT</span></span> | <span data-ttu-id="ab24e-139">0x00000001</span><span class="sxs-lookup"><span data-stu-id="ab24e-139">0x00000001</span></span> | <span data-ttu-id="ab24e-140">Yes</span><span class="sxs-lookup"><span data-stu-id="ab24e-140">Yes</span></span>                | <span data-ttu-id="ab24e-141">C + + 例外狀況處理。</span><span class="sxs-lookup"><span data-stu-id="ab24e-141">C++ exception handling.</span></span>                                                                                                                       |
| <span data-ttu-id="ab24e-142">COORD</span><span class="sxs-lookup"><span data-stu-id="ab24e-142">COORD</span></span>  | <span data-ttu-id="ab24e-143">0x00000002</span><span class="sxs-lookup"><span data-stu-id="ab24e-143">0x00000002</span></span> | <span data-ttu-id="ab24e-144">Yes</span><span class="sxs-lookup"><span data-stu-id="ab24e-144">Yes</span></span>                | <span data-ttu-id="ab24e-145">VSS 服務，也稱為 VSS 協調器。</span><span class="sxs-lookup"><span data-stu-id="ab24e-145">The VSS service, which is also called the VSS coordinator.</span></span>                                                                                    |
| <span data-ttu-id="ab24e-146">SWPRV</span><span class="sxs-lookup"><span data-stu-id="ab24e-146">SWPRV</span></span>  | <span data-ttu-id="ab24e-147">0x00000004</span><span class="sxs-lookup"><span data-stu-id="ab24e-147">0x00000004</span></span> | <span data-ttu-id="ab24e-148">Yes</span><span class="sxs-lookup"><span data-stu-id="ab24e-148">Yes</span></span>                | <span data-ttu-id="ab24e-149">VSS 系統陰影複製提供者服務。</span><span class="sxs-lookup"><span data-stu-id="ab24e-149">The VSS System Shadow Copy Provider service.</span></span>                                                                                                  |
| <span data-ttu-id="ab24e-150">BUCOMP</span><span class="sxs-lookup"><span data-stu-id="ab24e-150">BUCOMP</span></span> | <span data-ttu-id="ab24e-151">0x00000008</span><span class="sxs-lookup"><span data-stu-id="ab24e-151">0x00000008</span></span> | <span data-ttu-id="ab24e-152">Yes</span><span class="sxs-lookup"><span data-stu-id="ab24e-152">Yes</span></span>                | <span data-ttu-id="ab24e-153">VSS 要求者和備份元資料處理。</span><span class="sxs-lookup"><span data-stu-id="ab24e-153">The VSS requester and backup metadata processing.</span></span>                                                                                             |
| <span data-ttu-id="ab24e-154">WRITER</span><span class="sxs-lookup"><span data-stu-id="ab24e-154">WRITER</span></span> | <span data-ttu-id="ab24e-155">0x00000010</span><span class="sxs-lookup"><span data-stu-id="ab24e-155">0x00000010</span></span> | <span data-ttu-id="ab24e-156">Yes</span><span class="sxs-lookup"><span data-stu-id="ab24e-156">Yes</span></span>                | <span data-ttu-id="ab24e-157">VSS 寫入器作業和 VSS 託管的寫入器，例如 Windows 登錄寫入器。</span><span class="sxs-lookup"><span data-stu-id="ab24e-157">VSS writer operations and VSS hosted writer implementations, such as the Windows Registry writer.</span></span>                                             |
| <span data-ttu-id="ab24e-158">VSSAPI</span><span class="sxs-lookup"><span data-stu-id="ab24e-158">VSSAPI</span></span> | <span data-ttu-id="ab24e-159">0x00000020</span><span class="sxs-lookup"><span data-stu-id="ab24e-159">0x00000020</span></span> | <span data-ttu-id="ab24e-160">Yes</span><span class="sxs-lookup"><span data-stu-id="ab24e-160">Yes</span></span>                | <span data-ttu-id="ab24e-161">VSSAPI.DLL 匯出的 VSS API 的其他函式。</span><span class="sxs-lookup"><span data-stu-id="ab24e-161">Miscellaneous functions of the VSS API exported by VSSAPI.DLL.</span></span>                                                                                |
| <span data-ttu-id="ab24e-162">HWDIAG</span><span class="sxs-lookup"><span data-stu-id="ab24e-162">HWDIAG</span></span> | <span data-ttu-id="ab24e-163">0x00000040</span><span class="sxs-lookup"><span data-stu-id="ab24e-163">0x00000040</span></span> | <span data-ttu-id="ab24e-164">Yes</span><span class="sxs-lookup"><span data-stu-id="ab24e-164">Yes</span></span>                | <span data-ttu-id="ab24e-165">VSS 硬體提供者基礎結構和操作。</span><span class="sxs-lookup"><span data-stu-id="ab24e-165">VSS hardware provider infrastructure and operations.</span></span>                                                                                          |
| <span data-ttu-id="ab24e-166">ADMIN</span><span class="sxs-lookup"><span data-stu-id="ab24e-166">ADMIN</span></span>  | <span data-ttu-id="ab24e-167">0x00000080</span><span class="sxs-lookup"><span data-stu-id="ab24e-167">0x00000080</span></span> | <span data-ttu-id="ab24e-168">Yes</span><span class="sxs-lookup"><span data-stu-id="ab24e-168">Yes</span></span>                | <span data-ttu-id="ab24e-169">VSS 命令列公用程式，例如 VSSADMIN.EXE 和 DISKSHADOW.EXE。</span><span class="sxs-lookup"><span data-stu-id="ab24e-169">VSS command line utilities such as VSSADMIN.EXE and DISKSHADOW.EXE.</span></span>                                                                           |
| <span data-ttu-id="ab24e-170">VSSUI</span><span class="sxs-lookup"><span data-stu-id="ab24e-170">VSSUI</span></span>  | <span data-ttu-id="ab24e-171">0x00000100</span><span class="sxs-lookup"><span data-stu-id="ab24e-171">0x00000100</span></span> | <span data-ttu-id="ab24e-172">Yes</span><span class="sxs-lookup"><span data-stu-id="ab24e-172">Yes</span></span>                | <span data-ttu-id="ab24e-173">共用資料夾陰影複製設定使用者介面 (UI) 。</span><span class="sxs-lookup"><span data-stu-id="ab24e-173">The Shadow Copies for Shared Folders configuration user interface (UI).</span></span> <span data-ttu-id="ab24e-174">UI 僅適用于 Windows Server 作業系統。</span><span class="sxs-lookup"><span data-stu-id="ab24e-174">The UI is available only on Windows Server operating systems.</span></span>         |
| <span data-ttu-id="ab24e-175">TEST</span><span class="sxs-lookup"><span data-stu-id="ab24e-175">TEST</span></span>   | <span data-ttu-id="ab24e-176">0x00000200</span><span class="sxs-lookup"><span data-stu-id="ab24e-176">0x00000200</span></span> | <span data-ttu-id="ab24e-177">Yes</span><span class="sxs-lookup"><span data-stu-id="ab24e-177">Yes</span></span>                | <span data-ttu-id="ab24e-178">不適用。</span><span class="sxs-lookup"><span data-stu-id="ab24e-178">Not applicable.</span></span> <span data-ttu-id="ab24e-179"> (此追蹤模組已保留。 ) </span><span class="sxs-lookup"><span data-stu-id="ab24e-179">(This tracing module is reserved.)</span></span>                                                                                            |
| <span data-ttu-id="ab24e-180">IOCTL</span><span class="sxs-lookup"><span data-stu-id="ab24e-180">IOCTL</span></span>  | <span data-ttu-id="ab24e-181">0x00000400</span><span class="sxs-lookup"><span data-stu-id="ab24e-181">0x00000400</span></span> | <span data-ttu-id="ab24e-182">Yes</span><span class="sxs-lookup"><span data-stu-id="ab24e-182">Yes</span></span>                | <span data-ttu-id="ab24e-183">VSS 服務藉由呼叫 [**DeviceIoControl**](/windows/win32/api/ioapiset/nf-ioapiset-deviceiocontrol) 函式所起始的 FSCTL 和 IOCTL 作業詳細資料。</span><span class="sxs-lookup"><span data-stu-id="ab24e-183">Details of FSCTL and IOCTL operations that the VSS service has initiated by calling the [**DeviceIoControl**](/windows/win32/api/ioapiset/nf-ioapiset-deviceiocontrol) function.</span></span> |
| <span data-ttu-id="ab24e-184">根</span><span class="sxs-lookup"><span data-stu-id="ab24e-184">GEN</span></span>    | <span data-ttu-id="ab24e-185">0x00000800</span><span class="sxs-lookup"><span data-stu-id="ab24e-185">0x00000800</span></span> | <span data-ttu-id="ab24e-186">Yes</span><span class="sxs-lookup"><span data-stu-id="ab24e-186">Yes</span></span>                | <span data-ttu-id="ab24e-187">一般 VSS 公用程式函式，例如配置器、字串類別以及登錄和磁片區作業。</span><span class="sxs-lookup"><span data-stu-id="ab24e-187">General VSS utility functions, such as allocators, string classes, and registry and volume operations.</span></span>                                        |
| <span data-ttu-id="ab24e-188">WRXML</span><span class="sxs-lookup"><span data-stu-id="ab24e-188">WRXML</span></span>  | <span data-ttu-id="ab24e-189">0x00001000</span><span class="sxs-lookup"><span data-stu-id="ab24e-189">0x00001000</span></span> | <span data-ttu-id="ab24e-190">No</span><span class="sxs-lookup"><span data-stu-id="ab24e-190">No</span></span>                 | <span data-ttu-id="ab24e-191">寫入器中繼資料的 XML 處理。</span><span class="sxs-lookup"><span data-stu-id="ab24e-191">XML processing for writer metadata.</span></span> <span data-ttu-id="ab24e-192">此課程模組的雜訊程度非常高。</span><span class="sxs-lookup"><span data-stu-id="ab24e-192">This module has a very high level of noise.</span></span>                                                               |
| <span data-ttu-id="ab24e-193">VSSXML</span><span class="sxs-lookup"><span data-stu-id="ab24e-193">VSSXML</span></span> | <span data-ttu-id="ab24e-194">0x00002000</span><span class="sxs-lookup"><span data-stu-id="ab24e-194">0x00002000</span></span> | <span data-ttu-id="ab24e-195">No</span><span class="sxs-lookup"><span data-stu-id="ab24e-195">No</span></span>                 | <span data-ttu-id="ab24e-196">XML 處理基類。</span><span class="sxs-lookup"><span data-stu-id="ab24e-196">XML processing base classes.</span></span> <span data-ttu-id="ab24e-197">此課程模組的雜訊程度非常高。</span><span class="sxs-lookup"><span data-stu-id="ab24e-197">This module has a very high level of noise.</span></span>                                                                      |



 

</dd> <dt>

<span data-ttu-id="ab24e-198"><span id="_Module"></span><span id="_module"></span><span id="_MODULE"></span>**+**_模組_</span><span class="sxs-lookup"><span data-stu-id="ab24e-198"><span id="_Module"></span><span id="_module"></span><span id="_MODULE"></span>**+**_Module_</span></span>
</dt> <dd>

<span data-ttu-id="ab24e-199">啟用 *模組* 指定的模組。</span><span class="sxs-lookup"><span data-stu-id="ab24e-199">Enable the module specified by *Module*.</span></span> <span data-ttu-id="ab24e-200">一次只能啟用一個以上的模組。</span><span class="sxs-lookup"><span data-stu-id="ab24e-200">More than one module can be enabled at a time.</span></span> <span data-ttu-id="ab24e-201">若要列出可用的模組，請在命令列提示字元中輸入 **vsstrace – help 模組** 。</span><span class="sxs-lookup"><span data-stu-id="ab24e-201">To list the available modules, type **vsstrace –help modules** at the command-line prompt.</span></span>

</dd> <dt>

<span data-ttu-id="ab24e-202"><span id="-Module"></span><span id="-module"></span><span id="-MODULE"></span>**-**_模組_</span><span class="sxs-lookup"><span data-stu-id="ab24e-202"><span id="-Module"></span><span id="-module"></span><span id="-MODULE"></span>**-**_Module_</span></span>
</dt> <dd>

<span data-ttu-id="ab24e-203">停用 *模組* 所指定的模組。</span><span class="sxs-lookup"><span data-stu-id="ab24e-203">Disable the module specified by *Module*.</span></span> <span data-ttu-id="ab24e-204">若要列出可用的模組，請在命令列提示字元中輸入 **vsstrace – help 模組** 。</span><span class="sxs-lookup"><span data-stu-id="ab24e-204">To list the available modules, type **vsstrace –help modules** at the command-line prompt.</span></span>

</dd> <dt>

<span data-ttu-id="ab24e-205"><span id="_pid_ProcessId"></span><span id="_pid_processid"></span><span id="_PID_PROCESSID"></span>**+ pid** *ProcessId*</span><span class="sxs-lookup"><span data-stu-id="ab24e-205"><span id="_pid_ProcessId"></span><span id="_pid_processid"></span><span id="_PID_PROCESSID"></span>**+pid** *ProcessId*</span></span>
</dt> <dd>

<span data-ttu-id="ab24e-206">啟用 *ProcessId* 所指定的進程。</span><span class="sxs-lookup"><span data-stu-id="ab24e-206">Enable the process specified by *ProcessId*.</span></span> <span data-ttu-id="ab24e-207">若要啟用所有處理常式，請使用 " \* " 作為 *ProcessId* 的值。</span><span class="sxs-lookup"><span data-stu-id="ab24e-207">To enable all processes, use "\*" for the value of *ProcessId*.</span></span> <span data-ttu-id="ab24e-208">一次可以指定一個以上的 **pid** 選項。</span><span class="sxs-lookup"><span data-stu-id="ab24e-208">More than one **pid** option can be specified at a time.</span></span> <span data-ttu-id="ab24e-209">選項的順序會決定要啟用或停用的進程。</span><span class="sxs-lookup"><span data-stu-id="ab24e-209">The order of the options determines which processes are enabled or disabled.</span></span> <span data-ttu-id="ab24e-210">例如，若只要啟用其處理序識別碼為0xe8c 的進程，請使用 **vsstrace-pid \* + pid 0xe8c**。</span><span class="sxs-lookup"><span data-stu-id="ab24e-210">For example, to enable only the process whose process identifier is 0xe8c, use **vsstrace -pid \* +pid 0xe8c**.</span></span>

</dd> <dt>

<span data-ttu-id="ab24e-211"><span id="-pid_ProcessId"></span><span id="-pid_processid"></span><span id="-PID_PROCESSID"></span>**-pid** *ProcessId*</span><span class="sxs-lookup"><span data-stu-id="ab24e-211"><span id="-pid_ProcessId"></span><span id="-pid_processid"></span><span id="-PID_PROCESSID"></span>**-pid** *ProcessId*</span></span>
</dt> <dd>

<span data-ttu-id="ab24e-212">停用 *ProcessId* 所指定的進程。</span><span class="sxs-lookup"><span data-stu-id="ab24e-212">Disable the process specified by *ProcessId*.</span></span> <span data-ttu-id="ab24e-213">若要停用所有進程，請使用 " \* " 作為 *ProcessId* 的值。</span><span class="sxs-lookup"><span data-stu-id="ab24e-213">To disable all processes, use "\*" for the value of *ProcessId*.</span></span> <span data-ttu-id="ab24e-214">一次可以指定一個以上的 **pid** 選項。</span><span class="sxs-lookup"><span data-stu-id="ab24e-214">More than one **pid** option can be specified at a time.</span></span> <span data-ttu-id="ab24e-215">選項的順序會決定要啟用或停用的進程。</span><span class="sxs-lookup"><span data-stu-id="ab24e-215">The order of the options determines which processes are enabled or disabled.</span></span> <span data-ttu-id="ab24e-216">例如，若要停用進程識別碼為0xe8c 的進程以外的所有進程，請使用 **vsstrace-pid \* + pid 0xe8c**。</span><span class="sxs-lookup"><span data-stu-id="ab24e-216">For example, to disable all processes except the process whose process identifier is 0xe8c, use **vsstrace -pid \* +pid 0xe8c**.</span></span>

</dd> <dt>

<span data-ttu-id="ab24e-217"><span id="_tid_ThreadId"></span><span id="_tid_threadid"></span><span id="_TID_THREADID"></span>**+ tid** *ThreadId*</span><span class="sxs-lookup"><span data-stu-id="ab24e-217"><span id="_tid_ThreadId"></span><span id="_tid_threadid"></span><span id="_TID_THREADID"></span>**+tid** *ThreadId*</span></span>
</dt> <dd>

<span data-ttu-id="ab24e-218">啟用 *ThreadId* 所指定的執行緒。</span><span class="sxs-lookup"><span data-stu-id="ab24e-218">Enable the thread specified by *ThreadId*.</span></span> <span data-ttu-id="ab24e-219">若要啟用所有線程，請使用 " \* " 作為 *ThreadId* 的值。</span><span class="sxs-lookup"><span data-stu-id="ab24e-219">To enable all threads, use "\*" for the value of *ThreadId*.</span></span> <span data-ttu-id="ab24e-220">一次可以指定一個以上的 **tid** 選項。</span><span class="sxs-lookup"><span data-stu-id="ab24e-220">More than one **tid** option can be specified at a time.</span></span> <span data-ttu-id="ab24e-221">選項的順序會決定哪些執行緒已啟用或停用。</span><span class="sxs-lookup"><span data-stu-id="ab24e-221">The order of the options determines which threads are enabled or disabled.</span></span> <span data-ttu-id="ab24e-222">例如，若只要啟用其處理序識別碼為0x31a 的執行緒，請使用 **vsstrace-tid \* + tid 0x31a**。</span><span class="sxs-lookup"><span data-stu-id="ab24e-222">For example, to enable only the thread whose process identifier is 0x31a, use **vsstrace -tid \* +tid 0x31a**.</span></span>

</dd> <dt>

<span data-ttu-id="ab24e-223"><span id="-tid_ThreadId"></span><span id="-tid_threadid"></span><span id="-TID_THREADID"></span>**-tid** *ThreadId*</span><span class="sxs-lookup"><span data-stu-id="ab24e-223"><span id="-tid_ThreadId"></span><span id="-tid_threadid"></span><span id="-TID_THREADID"></span>**-tid** *ThreadId*</span></span>
</dt> <dd>

<span data-ttu-id="ab24e-224">停用 *ThreadId* 指定的執行緒。</span><span class="sxs-lookup"><span data-stu-id="ab24e-224">Disable the thread specified by *ThreadId*.</span></span> <span data-ttu-id="ab24e-225">若要停用所有線程，請使用 " \* " 作為 *ThreadId* 的值。</span><span class="sxs-lookup"><span data-stu-id="ab24e-225">To disable all threads, use "\*" for the value of *ThreadId*.</span></span> <span data-ttu-id="ab24e-226">一次可以指定一個以上的 **tid** 選項。</span><span class="sxs-lookup"><span data-stu-id="ab24e-226">More than one **tid** option can be specified at a time.</span></span> <span data-ttu-id="ab24e-227">選項的順序會決定哪些執行緒已啟用或停用。</span><span class="sxs-lookup"><span data-stu-id="ab24e-227">The order of the options determines which threads are enabled or disabled.</span></span> <span data-ttu-id="ab24e-228">例如，若要停用進程識別碼為0x31a 之執行緒以外的所有線程，請使用 **vsstrace-tid \* + tid 0x31a**。</span><span class="sxs-lookup"><span data-stu-id="ab24e-228">For example, to disable all threads except the thread whose process identifier is 0x31a, use **vsstrace -tid \* +tid 0x31a**.</span></span>

</dd> <dt>

<span data-ttu-id="ab24e-229"><span id="-l_Level"></span><span id="-l_level"></span><span id="-L_LEVEL"></span>**-l** *層級*</span><span class="sxs-lookup"><span data-stu-id="ab24e-229"><span id="-l_Level"></span><span id="-l_level"></span><span id="-L_LEVEL"></span>**-l** *Level*</span></span>
</dt> <dd>

<span data-ttu-id="ab24e-230">使用 *層級* 所指定的追蹤層級。</span><span class="sxs-lookup"><span data-stu-id="ab24e-230">Use the tracing level specified by *Level*.</span></span> <span data-ttu-id="ab24e-231">層級愈高，追蹤輸出越詳細越好。</span><span class="sxs-lookup"><span data-stu-id="ab24e-231">The higher the level, the more verbose the trace output.</span></span> <span data-ttu-id="ab24e-232">每個層級都包含所有較低的層級。</span><span class="sxs-lookup"><span data-stu-id="ab24e-232">Each level includes all of the lower levels.</span></span> <span data-ttu-id="ab24e-233">預設層級為170。</span><span class="sxs-lookup"><span data-stu-id="ab24e-233">The default level is 170.</span></span> <span data-ttu-id="ab24e-234">可用的層級如下。</span><span class="sxs-lookup"><span data-stu-id="ab24e-234">The following levels are available.</span></span>



| <span data-ttu-id="ab24e-235">層級</span><span class="sxs-lookup"><span data-stu-id="ab24e-235">Level</span></span> | <span data-ttu-id="ab24e-236">追蹤輸出中包含的資訊</span><span class="sxs-lookup"><span data-stu-id="ab24e-236">Information included in the trace output</span></span> |
|-------|------------------------------------------|
| <span data-ttu-id="ab24e-237">000</span><span class="sxs-lookup"><span data-stu-id="ab24e-237">000</span></span>   | <span data-ttu-id="ab24e-238">無</span><span class="sxs-lookup"><span data-stu-id="ab24e-238">None</span></span>                                     |
| <span data-ttu-id="ab24e-239">020</span><span class="sxs-lookup"><span data-stu-id="ab24e-239">020</span></span>   | <span data-ttu-id="ab24e-240">嚴重錯誤</span><span class="sxs-lookup"><span data-stu-id="ab24e-240">Fatal errors</span></span>                             |
| <span data-ttu-id="ab24e-241">030</span><span class="sxs-lookup"><span data-stu-id="ab24e-241">030</span></span>   | <span data-ttu-id="ab24e-242">未處理的例外狀況</span><span class="sxs-lookup"><span data-stu-id="ab24e-242">Unhandled exceptions</span></span>                     |
| <span data-ttu-id="ab24e-243">040</span><span class="sxs-lookup"><span data-stu-id="ab24e-243">040</span></span>   | <span data-ttu-id="ab24e-244">Errors</span><span class="sxs-lookup"><span data-stu-id="ab24e-244">Errors</span></span>                                   |
| <span data-ttu-id="ab24e-245">050</span><span class="sxs-lookup"><span data-stu-id="ab24e-245">050</span></span>   | <span data-ttu-id="ab24e-246">判斷提示</span><span class="sxs-lookup"><span data-stu-id="ab24e-246">Assertions</span></span>                               |
| <span data-ttu-id="ab24e-247">060</span><span class="sxs-lookup"><span data-stu-id="ab24e-247">060</span></span>   | <span data-ttu-id="ab24e-248">警告</span><span class="sxs-lookup"><span data-stu-id="ab24e-248">Warnings</span></span>                                 |
| <span data-ttu-id="ab24e-249">080</span><span class="sxs-lookup"><span data-stu-id="ab24e-249">080</span></span>   | <span data-ttu-id="ab24e-250">例外狀況處理</span><span class="sxs-lookup"><span data-stu-id="ab24e-250">Exception handling</span></span>                       |
| <span data-ttu-id="ab24e-251">100</span><span class="sxs-lookup"><span data-stu-id="ab24e-251">100</span></span>   | <span data-ttu-id="ab24e-252">事件記錄檔活動</span><span class="sxs-lookup"><span data-stu-id="ab24e-252">Event Log activity</span></span>                       |
| <span data-ttu-id="ab24e-253">120</span><span class="sxs-lookup"><span data-stu-id="ab24e-253">120</span></span>   | <span data-ttu-id="ab24e-254">一般資訊</span><span class="sxs-lookup"><span data-stu-id="ab24e-254">General information</span></span>                      |
| <span data-ttu-id="ab24e-255">140</span><span class="sxs-lookup"><span data-stu-id="ab24e-255">140</span></span>   | <span data-ttu-id="ab24e-256">程式碼流程</span><span class="sxs-lookup"><span data-stu-id="ab24e-256">Code flow</span></span>                                |
| <span data-ttu-id="ab24e-257">160</span><span class="sxs-lookup"><span data-stu-id="ab24e-257">160</span></span>   | <span data-ttu-id="ab24e-258">函數 enter 和 exit</span><span class="sxs-lookup"><span data-stu-id="ab24e-258">Function enter and exit</span></span>                  |
| <span data-ttu-id="ab24e-259">170</span><span class="sxs-lookup"><span data-stu-id="ab24e-259">170</span></span>   | <span data-ttu-id="ab24e-260">函數傳回值</span><span class="sxs-lookup"><span data-stu-id="ab24e-260">Function return values</span></span>                   |
| <span data-ttu-id="ab24e-261">180</span><span class="sxs-lookup"><span data-stu-id="ab24e-261">180</span></span>   | <span data-ttu-id="ab24e-262">函數參數 (簡易) </span><span class="sxs-lookup"><span data-stu-id="ab24e-262">Function parameters (terse)</span></span>              |
| <span data-ttu-id="ab24e-263">190</span><span class="sxs-lookup"><span data-stu-id="ab24e-263">190</span></span>   | <span data-ttu-id="ab24e-264">函數參數 (詳細資訊) </span><span class="sxs-lookup"><span data-stu-id="ab24e-264">Function parameters (verbose)</span></span>            |
| <span data-ttu-id="ab24e-265">200</span><span class="sxs-lookup"><span data-stu-id="ab24e-265">200</span></span>   | <span data-ttu-id="ab24e-266">詳細資訊層級1</span><span class="sxs-lookup"><span data-stu-id="ab24e-266">Verbose information level 1</span></span>              |
| <span data-ttu-id="ab24e-267">210</span><span class="sxs-lookup"><span data-stu-id="ab24e-267">210</span></span>   | <span data-ttu-id="ab24e-268">詳細資訊層級2</span><span class="sxs-lookup"><span data-stu-id="ab24e-268">Verbose information level 2</span></span>              |
| <span data-ttu-id="ab24e-269">220</span><span class="sxs-lookup"><span data-stu-id="ab24e-269">220</span></span>   | <span data-ttu-id="ab24e-270">詳細資訊層級3</span><span class="sxs-lookup"><span data-stu-id="ab24e-270">Verbose information level 3</span></span>              |
| <span data-ttu-id="ab24e-271">230</span><span class="sxs-lookup"><span data-stu-id="ab24e-271">230</span></span>   | <span data-ttu-id="ab24e-272">快速程式碼層級1</span><span class="sxs-lookup"><span data-stu-id="ab24e-272">Fast Code Level 1</span></span>                        |
| <span data-ttu-id="ab24e-273">240</span><span class="sxs-lookup"><span data-stu-id="ab24e-273">240</span></span>   | <span data-ttu-id="ab24e-274">快速程式碼層級2</span><span class="sxs-lookup"><span data-stu-id="ab24e-274">Fast Code Level 2</span></span>                        |
| <span data-ttu-id="ab24e-275">250</span><span class="sxs-lookup"><span data-stu-id="ab24e-275">250</span></span>   | <span data-ttu-id="ab24e-276">快速程式碼層級3</span><span class="sxs-lookup"><span data-stu-id="ab24e-276">Fast Code Level 3</span></span>                        |
| <span data-ttu-id="ab24e-277">255</span><span class="sxs-lookup"><span data-stu-id="ab24e-277">255</span></span>   | <span data-ttu-id="ab24e-278">全部</span><span class="sxs-lookup"><span data-stu-id="ab24e-278">All</span></span>                                      |



 

</dd> <dt>

<span data-ttu-id="ab24e-279"><span id="_indent"></span><span id="_INDENT"></span>**+ 縮排**</span><span class="sxs-lookup"><span data-stu-id="ab24e-279"><span id="_indent"></span><span id="_INDENT"></span>**+indent**</span></span>
</dt> <dd>

<span data-ttu-id="ab24e-280">在每個函式和子界限上縮排格式化的追蹤輸出。</span><span class="sxs-lookup"><span data-stu-id="ab24e-280">Indent the formatted trace output at each function and subfunction boundary.</span></span>

</dd> <dt>

<span data-ttu-id="ab24e-281"><span id="-indent"></span><span id="-INDENT"></span>**-縮排**</span><span class="sxs-lookup"><span data-stu-id="ab24e-281"><span id="-indent"></span><span id="-INDENT"></span>**-indent**</span></span>
</dt> <dd>

<span data-ttu-id="ab24e-282">請勿縮排格式化的追蹤輸出。</span><span class="sxs-lookup"><span data-stu-id="ab24e-282">Do not indent the formatted trace output.</span></span>

</dd> <dt>

<span data-ttu-id="ab24e-283"><span id="-etl_EtlFile"></span><span id="-etl_etlfile"></span><span id="-ETL_ETLFILE"></span>**-etl** *EtlFile*</span><span class="sxs-lookup"><span data-stu-id="ab24e-283"><span id="-etl_EtlFile"></span><span id="-etl_etlfile"></span><span id="-ETL_ETLFILE"></span>**-etl** *EtlFile*</span></span>
</dt> <dd>

<span data-ttu-id="ab24e-284">將 *EtlFile* 所指定的 Logman 輸出檔轉換為可讀取的文字格式。</span><span class="sxs-lookup"><span data-stu-id="ab24e-284">Convert the Logman output file specified by *EtlFile* into a readable text format.</span></span>

</dd> <dt>

<span data-ttu-id="ab24e-285"><span id="-o_OutputFile"></span><span id="-o_outputfile"></span><span id="-O_OUTPUTFILE"></span>**-o** *OutputFile*</span><span class="sxs-lookup"><span data-stu-id="ab24e-285"><span id="-o_OutputFile"></span><span id="-o_outputfile"></span><span id="-O_OUTPUTFILE"></span>**-o** *OutputFile*</span></span>
</dt> <dd>

<span data-ttu-id="ab24e-286">將追蹤資訊儲存至 *OutputFile* 所指定的輸出檔案。</span><span class="sxs-lookup"><span data-stu-id="ab24e-286">Save the tracing information to the output file specified by *OutputFile*.</span></span> <span data-ttu-id="ab24e-287">為了達到最佳效能，輸出檔案應該位於不屬於陰影複製的磁片區上。</span><span class="sxs-lookup"><span data-stu-id="ab24e-287">For best performance, the output file should be located on a volume that is not part of the shadow copy.</span></span>

</dd> <dt>

<span data-ttu-id="ab24e-288"><span id="-help_HelpOption"></span><span id="-help_helpoption"></span><span id="-HELP_HELPOPTION"></span>**-help** *HelpOption*</span><span class="sxs-lookup"><span data-stu-id="ab24e-288"><span id="-help_HelpOption"></span><span id="-help_helpoption"></span><span id="-HELP_HELPOPTION"></span>**-help** *HelpOption*</span></span>
</dt> <dd>

<span data-ttu-id="ab24e-289">顯示 *HelpOption* 所指定的命令列說明。</span><span class="sxs-lookup"><span data-stu-id="ab24e-289">Display the command-line help as specified by *HelpOption*.</span></span> <span data-ttu-id="ab24e-290">有效的 *HelpOption* 值為 **模組**、 **層級** 和 **全部**。</span><span class="sxs-lookup"><span data-stu-id="ab24e-290">The valid *HelpOption* values are **modules**, **levels**, and **all**.</span></span> <span data-ttu-id="ab24e-291">指定 **模組** 會導致列出模組。</span><span class="sxs-lookup"><span data-stu-id="ab24e-291">Specifying **modules** causes the modules to be listed.</span></span> <span data-ttu-id="ab24e-292">指定 **層級** 會列出可用的層級。</span><span class="sxs-lookup"><span data-stu-id="ab24e-292">Specifying **levels** causes the available levels to be listed.</span></span> <span data-ttu-id="ab24e-293">指定 [ **全部** ] 會顯示詳細的說明。</span><span class="sxs-lookup"><span data-stu-id="ab24e-293">Specifying **all** causes detailed help to be displayed.</span></span> <span data-ttu-id="ab24e-294">如果未使用任何選項，則會顯示簡潔的說明。</span><span class="sxs-lookup"><span data-stu-id="ab24e-294">If no options are used, concise help is displayed.</span></span>

</dd> </dl>

## <a name="using-logman"></a><span data-ttu-id="ab24e-295">使用 Logman</span><span class="sxs-lookup"><span data-stu-id="ab24e-295">Using Logman</span></span>

<span data-ttu-id="ab24e-296">下列程式說明如何搭配使用 Logman 與 VSS 應用程式。</span><span class="sxs-lookup"><span data-stu-id="ab24e-296">The following procedure describes how to use Logman with your VSS application.</span></span>

<span data-ttu-id="ab24e-297">**搭配使用 Logman 與 VSS 應用程式**</span><span class="sxs-lookup"><span data-stu-id="ab24e-297">**To use Logman with your VSS application**</span></span>

1.  <span data-ttu-id="ab24e-298">使用下列命令來開始追蹤：</span><span class="sxs-lookup"><span data-stu-id="ab24e-298">Use the following command to start tracing:</span></span>

    <span data-ttu-id="ab24e-299">**logman 啟動 vss-o** *x： \\ \* \* \* ets-p {9138500e-3648-4edb-aa4c-859e9f7b7c38} 0xfff 170*\*</span><span class="sxs-lookup"><span data-stu-id="ab24e-299">**logman start vss -o** *x:\\*\*\*vss.etl -ets -p {9138500e-3648-4edb-aa4c-859e9f7b7c38} 0xfff 170*\*</span></span>

    > [!Note]  
    > <span data-ttu-id="ab24e-300">以您想要 \\ 儲存追蹤記錄檔的目錄路徑取代 "x："。</span><span class="sxs-lookup"><span data-stu-id="ab24e-300">Replace "x:\\" with the path to the directory where you would like the trace log file to be stored.</span></span>

     

2.  <span data-ttu-id="ab24e-301">使用下列命令停止追蹤：</span><span class="sxs-lookup"><span data-stu-id="ab24e-301">Use the following command to stop tracing:</span></span>

    <span data-ttu-id="ab24e-302">**logman 停止 vss-ets**</span><span class="sxs-lookup"><span data-stu-id="ab24e-302">**logman stop vss -ets**</span></span>

<span data-ttu-id="ab24e-303">追蹤記錄檔為 *x： \\*.vss。</span><span class="sxs-lookup"><span data-stu-id="ab24e-303">The trace log file is *x:\\* vss.etl.</span></span>

<span data-ttu-id="ab24e-304">如需 Logman 工具的詳細資訊，請參閱 [Logman](/previous-versions/windows/it-pro/windows-server-2012-R2-and-2012/cc753820(v=ws.11))。</span><span class="sxs-lookup"><span data-stu-id="ab24e-304">For more information about the Logman tool, see [Logman](/previous-versions/windows/it-pro/windows-server-2012-R2-and-2012/cc753820(v=ws.11)).</span></span>

## <a name="using-tracelog"></a><span data-ttu-id="ab24e-305">使用 Tracelog.exe</span><span class="sxs-lookup"><span data-stu-id="ab24e-305">Using Tracelog</span></span>

<span data-ttu-id="ab24e-306">下列程式說明如何使用 Tracelog.exe。</span><span class="sxs-lookup"><span data-stu-id="ab24e-306">The following procedure describes how to use Tracelog.</span></span>

<span data-ttu-id="ab24e-307">**使用 Tracelog.exe**</span><span class="sxs-lookup"><span data-stu-id="ab24e-307">**To use Tracelog**</span></span>

1.  <span data-ttu-id="ab24e-308">建立名為 .vss 的文字檔，其中只包含下列文字：</span><span class="sxs-lookup"><span data-stu-id="ab24e-308">Create a text file named vss.ctl that contains only the following text:</span></span>

    <span data-ttu-id="ab24e-309">**9138500e-3648-4edb-aa4c-859e9f7b7c38 vss**</span><span class="sxs-lookup"><span data-stu-id="ab24e-309">**9138500e-3648-4edb-aa4c-859e9f7b7c38 vss**</span></span>

2.  <span data-ttu-id="ab24e-310">使用下列命令來開始追蹤：</span><span class="sxs-lookup"><span data-stu-id="ab24e-310">Use the following command to start tracing:</span></span>

    <span data-ttu-id="ab24e-311">**tracelog.exe-啟動 vss-f** *x： \\ \* \* \* .vss-guid .vss-旗標 0xff-level 0xaa*\*</span><span class="sxs-lookup"><span data-stu-id="ab24e-311">**tracelog -start vss -f** *x:\\*\*\*vss.etl -guid vss.ctl -flag 0xff -level 0xaa*\*</span></span>

    > [!Note]  
    > <span data-ttu-id="ab24e-312">以您想要 \\ 儲存追蹤記錄檔的目錄路徑取代 "x："。</span><span class="sxs-lookup"><span data-stu-id="ab24e-312">Replace "x:\\" with the path to the directory where you would like the trace log file to be stored.</span></span>

     

3.  <span data-ttu-id="ab24e-313">使用下列命令停止追蹤：</span><span class="sxs-lookup"><span data-stu-id="ab24e-313">Use the following command to stop tracing:</span></span>

    <span data-ttu-id="ab24e-314">**tracelog.exe-停止 vss**</span><span class="sxs-lookup"><span data-stu-id="ab24e-314">**tracelog -stop vss**</span></span>

<span data-ttu-id="ab24e-315">追蹤記錄檔為 *x： \\*.vss。</span><span class="sxs-lookup"><span data-stu-id="ab24e-315">The trace log file is *x:\\* vss.etl.</span></span>

<span data-ttu-id="ab24e-316">如需 Tracelog.exe 工具的詳細資訊，請參閱 [tracelog.exe](https://msdn.microsoft.com/library/ms797927.aspx)。</span><span class="sxs-lookup"><span data-stu-id="ab24e-316">For more information about the Tracelog tool, see [Tracelog](https://msdn.microsoft.com/library/ms797927.aspx).</span></span>

 

 
